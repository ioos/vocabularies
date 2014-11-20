vocabularies
============

_IOOS Instructions and Guidelines for use of Controlled Vocabularies in IOOS-compliant data services_

# Proposed Outline and Revision Goals

+ [Introduction](#introduction)
+ [Referencing Vocabulary Terms](#referencing-vocabulary-terms)
  + TODO Short description
+ [Vocabulary Selection and Use](#vocabulary-selection-and-use)
  + TODO Short description
+ [Vocabulary Search Testing](#vocabulary-search-testing)
  + TODO Short description (Not sure this belongs on this page but it's probably fine for now.  It feels out of place but maybe all we need is a better transition)
+ [References](#references)

# Introduction

Controlled vocabularies clarify the meaning of common concepts and enable more interoperable data systems through more precise definitions and machine readable online references.  This document describes the policies and relevant controlled vocabularies that have been adopted or developed by the IOOS community, including context and specific instructions for use and implementation in data services. They primarily target SOS service requests, but are of general applicability in other services and IOOS DMAC areas as well. The content is intended primarily to serve consumers and providers, including software developers and data managers.  

All controlled [vocabularies and vocabulary mappings developed or adopted by IOOS](http://mmisw.org/ont/ioos) (except for [Darwin Core biological terms](http://rs.tdwg.org/dwc/terms/)) are currently hosted on the [Marine Metadata Interoperability (MMI) Ontology Registry and Repository](http://mmisw.org/orr/#b). These IOOS-endorsed vocabularies encompass all vocabularies required to support SOS and other data services: platform types, observed properties (also known as parameters, variables or phenomena), organizations, societal sectors, data decriptor definitions, etc.

# Referencing Vocabulary Terms

Terms on MMI-hosted vocabularies are accessible as URL references pointing to human-readable HTML pages; URL's are also available for machine-friendly formats like JSON and RDF. In IOOS SOS and other data services, vocabulary terms must be referenced using complete, valid MMI term URL's, or if the service syntax requires it, the URL separated into two parts: vocabulary base URL and term name. For example:
  * Complete MMI term URL: [http://mmisw.org/ont/ioos/parameter/acidity](http://mmisw.org/ont/ioos/parameter/acidity)
  * MMI term URL separated into its two parts: http://mmisw.org/ont/ioos/parameter and [acidity](http://mmisw.org/ont/ioos/parameter/acidity)

MMI vocabulary terms are case sensitive and must be referenced accordingly.

Specific term referencing patterns vary depending on service response encoding standards. [http://code.google.com/p/ioostech/source/browse/#svn/trunk/templates/Milestone1.0 IOOS SOS Milestone 1.0 response templates] provide complete illustrations of all SOS vocabulary term referencing patterns.

REST access to machine-friendly formats for MMI terms is straightforward, and is obtained by simply adding a format extension to the term reference URL; for example, see the [JSON](http://mmisw.org/ont/ioos/parameter/acidity.json) and [RDF](http://mmisw.org/ont/ioos/parameter/acidity.rdf) responses available for the acidity example above.

# Vocabulary Selection and Use 

The first step to using controlled vocabularies is finding an appropriate one. [Criteria for selecting the best controlled vocabulary should be based on:](http://cf-pcmdi.llnl.gov/documents/cf-standard-names/about) Content; Is it community-maintained? Is it well-managed? Is it interoperable? IOOS-endorsed vocabularies described in this document generally meet these criteria; all terms found on these vocabularies are supported.

Vocabulary users are required to search terms from IOOS-endorsed registered vocabularies on MMI or other well-established, community maintained vocabulary systems before proposing new terms. 

The [Climate and Forecast (CF) Standard Names Parameter Vocabulary](http://marinemetadata.org/orrcf) plays a central role in IOOS vocabulary policies. It is intended to be the first-priority source for observed property names and definitions to be referenced in IOOS SOS service requests. In the case of CF compliant netCDF files or OPeNDAP equivalent, the CF standard names parameter vocabulary is the only appropriate vocabulary to use for the standard_name variable attribute. This preference exists to support interoperability with the wider community using CF. However, the scope of CF standard names is limited, and as such this vocabulary will often be insufficient.

The steps below provide an outline of the general term identification and selection process to be followed by data providers:

1. Search Primary Vocabularies When available and in wide use, IOOS will strive to adopt and support existing community vocabularies. Such "primary", IOOS-endorsed vocabularies should be searched first for selecting terms. Currently the use of primary community vocabularies is largely limited to [Observed Properties](#Observed_Properties).
2. Search Secondary Vocabularies. When a relevant term is not found among primary vocabularies, IOOS-maintained "secondary" vocabularies should be searched. [Such vocabularies are hosted on MMI](http://mmisw.org/ont/ioos) and are described in the sections below, by vocabulary topic.
3. Propose and Adopt New Terms. When primary and secondary vocabularies don't contain a relevant term, a new term can be adopted by borrowing from other, non-IOOS vocabularies, or developing it following common naming conventions [such as CF Standard Names naming conventions](http://cf-pcmdi.llnl.gov/documents/cf-standard-names/guidelines). The data provider does not need approval before implementing new terms. However, the provider must confer with the IOOS Program Office about new terms, in order to maintain the highest level of interoperability. The IOOS Program will facilitate the process to include new terms in the appropriate IOOS registered vocabulary or seek approval of term with the CF standard community or another accepted vocabulary standards group. The IOOS Program will notify the data provider when the term has been registered.

This section describes the categories and specific instances of controlled vocabularies IOOS currently supports. Brief instructions for usage are provided, including links to more detailed resources. [Additional, related concepts are also used in IOOS services](#Other_vocabularies_and_vocabulary-related_concepts), some of which have also been implemented as MMI vocabularies but have not been fully endorsed and described by IOOS.

## Observed Properties 

IOOS supports the inclusion and standard referencing of a large set of observed properties (also referred to as phenomena, parameters, or variables). Any property encompassed by the following vocabularies is supported:

1. _Primary Vocabularies_
  * [Climate & Forecast (CF) Standard Names Parameter Vocabulary](http://cf-pcmdi.llnl.gov/documents/cf-standard-names/about)
  * The MMI-hosted vocabulary is located at http://mmisw.org/ont/cf/parameter. CF standard names focus on atmospheric and ocean physical and chemical terms, and pay limited attention to areas like biology and ecology.
  * For biological and biodiversity applications the [Darwin Core (DwC) biological terms](http://rs.tdwg.org/dwc/terms/ ).
1. _Secondary Vocabularies_
  * [IOOS Parameter Vocabulary v.2.0](http://mmisw.org/ont/ioos/parameter). An MMI-hosted vocabulary created via an IOOS community polling of terms in use by the 11 RA's in 2009-2010, and a follow-up process of QA/QC, refinement and consolidation of duplicates. It encompasses additional physical, chemical and biological terms not found among CF Standard Names. For convenience and completeness, this vocabulary incorporates CF terms that are widely used in IOOS. [An MMI-based ontological mapping](http://mmisw.org/ont/ioos/map_ioos_cf) has been created between IOOS Parameter and CF terms, such that a reference to a term in one vocabulary is automatically linked to an appropriate term on the other vocabulary if such a match exists.
  * [IOOS Biologicah Data Terminology](http://mmisw.org/ont/ioos/biological).  A vocabulary that lists biological data fields with names, descriptions, and format notes. It was based on ratified Darwin Core, Dublin Core and proposed IOOS vocabularies. XML guide was based on Darwin core XML guidance. CF Conventions had been applied to biological data definition at the field level. 

[Haines et al (2012) (1)](#references) have provided a detailed discussion of IOOS vocabulary strategy and use regarding observed properties, focusing mainly on physical and chemical properties (CF Standard Names and IOOS Parameter Vocabulary, above).

**Usage in SOS request parameters and XML responses.** 
See the IOOS SOS Milestone 1.0 [response templates](https://github.com/ioos/sos-guidelines/tree/master/template/milestone1.0) for complete implementation details and direct reference.

| *SOS Operation*| *Request parameters*| *Response: XML block (XPath)*|
|---------------------| :----------------------: |------------------:|
| GetCapabilities| - | /sos:Capabilities/ows:OperationsMetadata/ows:Operation/ows:Parameter/ows:AllowedValues/ows:Value|
| GetCapabilities| - | /sos:Capabilities/sos:Contents/sos:ObservationOfferingList/sos:ObservationOffering/sos:observedProperty|
| GetObservation| |TimeSeries feature-type, multi-sensor response|
|GetObservation| observedProperty|/om:observedProperty|
|GetObservation| observedProperty| /om:result/swe:DataStream/swe:DataChoice/swe:item/swe:DataRecord/swe:field/swe:Quantity|
|DescribeSensor| -| /sml:SensorML/sml:member/sml:System/sml:components/sml:ComponentList/sml:component/sml:System/sml:outputs/sml:OutputList/sml:output/swe:Quantity[@definition]|

- None, Not applicable_

`*` Preceded by /om:!ObservationCollection/om:member/om:Observation_

### Selecting a vocabulary term 
TODO: This section seems redundant with above.  Combine the two.

The term identification and selection  [procedure](#Vocabulary_Selection_and_Use) described above should be used. a search for terms should start with Primary Vocabularies for observed properties, particularly the [CF Standard Names parameter vocabulary](http://mmisw.org/ont/cf/parameter). Where equivalent or nearly equivalent terms exist, CF terms are preferred over DwC terms. If an appropriate observed property term is not found among primary vocabularies, the secondary IOOS vocabularies listed above should be searched. 

If the desired parameter is not found on primary or secondary vocabularies, IOOS should be notified and engaged to discuss adding the term to the IOOS Parameter Vocabulary, following a publicized and accepted process that's reasonably fast and a reasonably small burden on participants. In parallel, IOOS will maintain an engagement with the CF community to discuss adding parameters that are not currently present.

### Composite Properties 

The CF standard names vocabulary only defines scalar properties. Previously, IOOS defined three composite ("vector") properties made up of two or more scalar properties: *winds*, *waves* and *currents*. These composite properties are supported via the IOOS Parameter Vocabulary and should be referenced like any other term there (eg: http://mmisw.org/ont/ioos/parameter/wave). [Additional descriptions of IOOS guidance regarding composite properties are available from the IOOS SOS Milestone 1.0 WSDD](https://github.com/ioos/sos-guidelines/tree/master/doc/wsdd)

## Station Platform Types

The [IOOS Platform Vocabulary](http://mmisw.org/ont/ioos/platform) references and defines platform types used to describe each station asset. This vocabulary was developed by IOOS (with guidance from MMI) in 2012-2013 through a concerted effort drawing from current needs and previous IOOS and MMI experiences. [This effort, the vocabulary itself, and instructions for usage are described elsewhere](http://code.google.com/p/ioostech/wiki/PlatformVocabulary). The vocabulary of approximately 35 terms provides a consistent terminology to describe a wide array of platform types on which sensors are attached and data sets collected. These terms must be used as classifier entries in [SOS DescribeSensor SensorML responses](http://code.google.com/p/ioostech/source/browse/trunk/templates/Milestone1.0/SML-DescribeSensor-Station.xml).

## Organization Descriptors and Roles

IOOS has implemented as MMI vocabularies two kinds of organization or institutional descriptors: *Organization Identifier* and *Organization Societal Sector*.


The MMI-hosted [IOOS Partner Organization vocabulary](http://mmisw.org/ont/ioos/organization) provides list of organizations that serve in one or more IOOS partnership roles. The organization roles currently defined by IOOS are: [sponsor](http://mmisw.org/ont/ioos/definition/sponsor), [operator](http://mmisw.org/ont/ioos/definition/operator), [publisher](http://mmisw.org/ont/ioos/definition/publisher), and [parentNetwork](http://mmisw.org/ont/ioos/definition/parentNetwork).

All organizations, including IOOS, IOOS Regional Associations (RAs) and Federal Agencies, should be referenced using terms corresponding to standard RA and agency acronyms (eg, GLOS, SECOORA, USACE) as listed in the  [IOOS Partner Organization vocabulary](http://mmisw.org/ont/ioos/organization). 

[Asset platform sponsorship](http://mmisw.org/ont/ioos/definition/sponsor) is defined as financial or other kinds of support. Platforms that are partially or fully supported by IOOS must be attributed with a sponsor classifier entry of "IOOS" on the SOS DescribeSensor response; more than one sponsor organizations may be listed, as appropriate.

Usage in SOS request parameters and XML responses. See the [IOOS SOS Milestone 1.0 response templates] (http://code.google.com/p/ioostech/source/browse/#svn/trunk/templates/Milestone1.0) for complete implementation details and direct reference. 

|*SOS Operation*|*Response: XML block (XPath)*| *Comment* |
|---------------------| :----------------------: |------------------:|
|GetCapabilities |/sos:Capabilities/ows:OperationsMetadata/ows:Operation/ows:Parameter/ows:AllowedValues/ows:Value |*Required* Keywords|
|GetObservation|-|No Organization reference|
|DescribeSensor|/sml:classification/sml:ClassifierList?/sml:classifier[@name="ParentNetwork?"]/sml:Term[@definition="http://mmisw.org/ont/ioos/definition/parentNetwork"]/sml:value | *Required ParentNetwork? Also use <sml:codeSpace xlink:href="http://mmisw.org/ont/ioos/organization"/> |
|DescribeSensor|/sml:classification/sml:ClassifierList?/sml:classifier[@name="publisher"]/sml:Term[@definition="http://mmisw.org/ont/ioos/definition/publisher"]/sml:value| *Required* Publisher. Also use <sml:codeSpace xlink:href="http://mmisw.org/ont/ioos/organization"/> |
|DescribeSensor| /sml:contact[@xlink:role="http://mmisw.org/ont/ioos/definition/publisher"]/sml:ResponsibleParty?/sml:organizationName |Required. Publisher (under contact information)| 
- _None, Not applicable_

`*` _Preceded by /sml:SensorML/sml:member/sml:System_

### IOOS Organization Societal Sectors
The [IOOS Organizational Societal Sector vocabulary](http://mmisw.org/ont/ioos/sector) distinguishes between different segments of government (eg, federal, state, municipal), and academic, tribal, industry and other divisions. It is currently used primarily to specify the [operator sector](http://mmisw.org/ont/ioos/definition/operatorSector), corresponding to the organization that manages and operates the monitoring station.
The operator's societal sector is attributed as an operatorSector classifier in the SOS DescribeSensor response.
The sector vocabulary does not distinguish *international*, non-US organizations as such, and should be applicable within their national contexts; for example, a Canadian provincial agency should be described with the term "gov_state". The identification of international providers is handled by specifying a required country name in the SensorML Operator role contact information. US-based organizations must be assigned "USA" as the country name.

### General and SWE Definitions
The [IOOS Vocabulary and Category Definitions](http://mmisw.org/ont/ioos/definition) is an MMI vocabulary used for clarifying the meaning of roles, classifiers and other general terms used throughout the SOS web services, particularly the DescribeSensor SensorML response. It defines commonly used categories to facilitate interpretation, and may be of general value beyond the SOS services.
The [IOOS SOS SWE Element Definitions Vocabulary](http://mmisw.org/ont/ioos/swe_element_type) is a narrower MMI vocabulary of definitions that reflect specific IOOS conventions for use in standard SOS SWE elements. References available on the [MMI vocabulary page](http://mmisw.org/ont/ioos/swe_element_type) give examples of where to use these terms in IOOS SWE SOS templates.

### Keywords 
Recommendations for Keywords usage have yet to be developed. In the meantime, for local to regional provider the relevant IOOS RA should be used as a keyword, using the spelling from the [IOOS Organization vocabulary](http://mmisw.org/ont/ioos/organization). Additional recommended keywords include geographical regions and parameters (observed properties) served.

## Higher-level categories and vocabulary mappings
The background, IOOS use, and mappings of high-level categories and vocabulary mappings vocabularies for observed properties is partially described in [(1)](#references). Terms from these vocabularies may be useful as service Keywords and for other data-discovery uses. These MMI-based resources include:
  * [IOOS Core Variable Vocabulary](http://mmisw.org/ont/ioos/core_variable IOOS Core Variable Vocabulary).
  * [IOOS Societal Benefit Areas](http://mmisw.org/ont/ioos/societal_areas)
  * [IOOS Category Vocabulary](http://mmisw.org/ont/ioos/category)

## Units of Measure
Units of Measure do not make up a vocabulary per se, but rather a mix of vocabulary terms and a syntax for combinations. At this time, IOOS encourages but does not require the use of [UCUM](http://unitsofmeasure.org/) or [UDUNITS](http://www.unidata.ucar.edu/software/udunits/); UDUNITS is the de-facto standard in the CF convention. Versions of these units systems should be kept in mind (eg, UDUNITS-1 vs UDUNITS-2). [ERDDAP/NOAA CoastWatch](http://coastwatch.pfeg.noaa.gov/erddap/convert/units.html) has a very useful page that includes comparisons of UDUNITS and UCUM, converters among the units systems, and a discussion of UDUNITS-1 and UDUNITS-2]. Another relevant effort is [QUDT](http://www.qudt.org/ QUDT), previously sponsored by NASA and now managed by a group that includes OGC O&M developer Simon Cox.

# Vocabulary Search Testing
## Testing capability of SPARQL queries to assist catalog searches
Most catalog services provide some search mechanisms of the metadata fields. However, these tend to be limited to exact matches or specific fields but not able to find data that is somewhat related or same data that is labeled differently. Searching for like or similar terms is an important step towards improving the search capability within data catalogs like THREDDS or geoportal catalog services. In this section, IOOS is testing automated search capabilities and discovery of terms based on relationships established in mapping vocabulary. This is an attempt to create a tunnel or mechanism by which more intelligent searches can be made.
But what is returned is only as good as the SPARQL query and the mappings in the vocabulary.

## SPARQL Endpoint
Numerous examples exist in PERL, Python, and HTML Forms that illustrate how to issue SPARQL queries to vocabulary search services. SPARQL Endpoints can return the data in different formats (HTML, JSON, CSV, RDF, N3), but accessing all these formats is not always obvious. Of the Python code, SparqlWrapper seems to be the most robust (note: a github fork is also available). The MMI Endpoint returns XML, CSV, JSON, and HTML.
As a proof-of-concept, python script examples were created to show how to submit a SPARQL query with a JSON return, being the easiest format of response to work with python.

## SPARQL - IOOS Examples
* [IOOS Vocabulary SPARQL Query Development Example Page](http://www.unc.edu/~haines/orrioos.html)

## SPARQL - Python Examples
* [using urllib2 example_sparql_urllib2.ipynb](http://nbviewer.ipython.org/github/nccoos/ioos-vocabulary-search/blob/master/examples/example_sparql_urllib2.ipynb)
* [using SPARQLWrapper example_sparql_wrapper.py](http://nbviewer.ipython.org/github/nccoos/ioos-vocabulary-search/blob/master/examples/example_sparql_wrapper.ipynb)

## CSW - Python Examples
* [Using OWSLIB-CSW to access NGDC Geoportal CSW (example_csw_ngdc_geoportal.ipynb)] (http://nbviewer.ipython.org/github/nccoos/ioos-vocabulary-search/blob/master/examples/example_csw_ngdc_geoportal.ipynb)

## Visualizing Vocabularies, Mappings, and Search Results
Developing recipes for geoportal programmers to issue SPARQL queries to MMI ORR is one key to demonstrating how MMI ORR can enhance catalog search. Another key to this development is to visualize what the search results are. Visualizing the terms and their mappings will be the next step in making registered vocabs on MMI ORR more useful.

### Examples
* [CF Standard Name Browser](http://mmisw.org/cfsn) ([Wiki](https://github.com/mmisw/cfsn/wiki))
* [IOOS Parameter Vocabulary Visualizer](http://www.unc.edu/usr-bin/haines/orrviz.py) ([Code](https://github.com/nccoos/ioos-vocabulary-viz))


# References

(1) Haines, S., V. Subramanian, E. Mayorga, D. Snowden, R. Ragsdale, C. Rueda and M. Howard. 2012. IOOS vocabulary and ontology strategy for observed properties. Proc. MTS/IEEE Oceans'12 (Hampton Roads, VA), [doi:10.1109/OCEANS.2012.6405083](http://dx.doi.org/10.1109/OCEANS.2012.6405083). Final, submitted paper is available [here as pdf](http://ioostech.googlecode.com/files/IOOSVocabPaper_MTSOceans2012_HainesEtal_Final_copyrighted.pdf).

(2) Graybeal, J., A. W. Isenor, and C. Rueda. 2012. Semantic mediation of vocabularies for ocean observing systems. Computers & Geosciences 40: 120-131, [doi:10.1016/j.cageo.2011.08.002]()  [pdf available here](https://marinemetadata.org/news/mmisemanticpaper2011)
