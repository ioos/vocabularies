#Platform Vocabulary

## Introduction

The [IOOS Platform Vocabulary](http://mmisw.org/orr/#http://mmisw.org/ont/ioos/platform) is a controlled vocabulary for platform types with definitions, references used for the definition, and links to example images. It is registered at [MMI-ORR](http://mmisw.org/ont/ioos/platform). It provides oceanographic data users consistent terminology to describe a wide array of different platform types from which sensors are attached and data sets collected.

By mapping the terms within this one vocabulary, a simple hierarchy of terms is provided. The list of IOOS Platform types was mapped hierarchically by using simple relationships between the terms within the vocabulary to identify general platform types. This was done by using the MMI-ORR Mapping Tool. By using this method some of the specific types of platforms can be members of more than one general type where one-to-many relationships are warranted. For example, a profiling_buoy can be a buoy platform type but also can be a profiler platform type.

As part of developing the IOOS Platform Vocabulary it was important to identify what are valid terms for the vocabulary and identify what we mean by an asset, platform, sensor(s) and station. The following definitions helped to refine what terms should go in the IOOS Platform Vocabulary.

*Platform
  A structure or vehicle designed to hold one or more sensors such that the intended oceanographic or atmospheric variable(s) can be monitored or measured in a manner designed for the ocean observing system or scientific hypotheses.  
*Sensor 
  A converter that measures a physical quantity and converts it into a signal which can be read by an observer or by an (today mostly electronic) instrument. Pasted from [http://en.wikipedia.org/wiki/Sensor <http://en.wikipedia.org/wiki/Sensor>] 
*Station 
  A fixed location where a platform might be deployed or observations taken for a finite period of time.
*Asset
  Any tangible or intangible system that is capable of being owned or controlled to produce something of value. For example, a temperature sensor or a buoy may be considered assets. Similarly, a dataset of salinity measurements or model output of surface currents may be also considered assets. 
*Observational Asset
  In situ fixed, in situ mobile, and remote sensing assets measuring atmospheric and oceanic variables. All non-modeling assets, including platforms, instruments, sensors, and variables, fit into this category.

Platform Vocabulary Guidelines
  1. No capitalization
  2. No acronyms (Remotely Operated Vehicle)
  3. Hierarchy is structured based on motility and environment.

Developing a List of Terms 

With a firm definition of what a platform is, potential platform types were extracted from the 2011 IOOS Asset Inventory ([#Appendix_B__List_of_IOOS_Platform_Vocabulary_Terms Appendix B]), IOOS Regional Build-Out Plans ([#Appendix_C__Regional_Build_Out_Platform_Definitions Appendix C]) and SECOORA and NANOOS Asset Inventories ([#Appendix_D__SECOORA_and_NANOOS_Asset_Definitions Appendix D]).  This approach provided the most complete list of possible platforms related to assets within Regional Associations and within IOOS. This larger list was organized into a general hierarchy provided in ([#Appendix_A_Proposed_Hierarchical_structure Appendix A]).

Developing the Vocabulary 

Each term was researched and definitions provided. Many of the resources and references are provided for each definition.  In addition, most of the platform types are provided with links to one or two images found through Internet Search engines like Google Images that were appropriate to the definition provided.  An example entry is given in tableform. 


Term	
*drifting_buoy	

Definition
*Drifting buoys are free drifting platforms with a float or buoys that keep the drifter at the surface and underwater sails or sock that catch the current. They have sensors to make meteorological and oceanographic measurements, such as air pressure and water temperature, and by tracking their positions the surface currents can be determined. Some drifters also have sensors to measure wind and salinity.	

Images
*http://www.metoffice.gov.uk/weather/marine/observations/gathering_data/images/drifting_buoy.jpg, http://www.aoml.noaa.gov/phod/dac/drifterpic1.jpg, http://filemaker2-server.cbl.umces.edu/sensorimages/7265-SLDMB.gif

References
*UK Met Office, Observations from drifting buoys, http://www.metoffice.gov.uk/weather/marine/observations/gathering_data/buoys.html












	
|| Term || Definition || Images	|| Reference || 
|| {{{drifting_buoy}}} || {{{Drifting buoys are free drifting platforms with a float or buoys that keep the drifter at the surface and underwater sails or sock that catch the current. They have sensors to make meteorological and oceanographic measurements, such as air pressure and water temperature, and by tracking their positions the surface currents can be determined. Some drifters also have sensors to measure wind and salinity.}}}|| {{{http://www.metoffice.gov.uk/weather/marine/observations/gathering_data/images/drifting_buoy.jpg, http://www.aoml.noaa.gov/phod/dac/drifterpic1.jpg, http://filemaker2-server.cbl.umces.edu/sensorimages/7265-SLDMB.gif}}} ||{{{UK Met Office, Observations from drifting buoys, http://www.metoffice.gov.uk/weather/marine/observations/gathering_data/buoys.html}}}||

==Displaying Images (STILL TO DO)==

One of the future tasks will be to be able to display Images saved within registered vocabulary.  This probably can be accomplished using css style-sheets.  For example it would be nice to display or show the images provided in the Images field such as this example.

||[http://www.metoffice.gov.uk/weather/marine/observations/gathering_data/images/drifting_buoy.jpg]||[http://filemaker2-server.cbl.umces.edu/sensorimages/7265-SLDMB.gif]|| 

==Animal Platform Terms (STILL TO DO)==

One main category of platform type not addressed in this version, is the "animal" (mammal, fish, etc) platform types.  This category covers using animals that are tagged and tracked and even carry micro-sensors, such as CTD. In this case data descriptors would identify an animal or the type of animal as the platform type.  We need to decide what granularity we should use to address the hierarchy or find how mapping can accomodate finding, and using recommended scientific name and common name.  For example, if common name = northern elephant seal and if scientific name = Mirounga angustirostris, the platform term would be a combination of the two.  We recommend to use both common names and scientific names so that it can be searched by either.
The scientific and common name for animals can be found here URL: [http://www.marinespecies.org/]

= Developing the Hierarchy (Mapping) = 

Within the IOOS Platform Vocabulary, some types of platforms can be considered more general while others have more specific characteristics such as motility and associated environments. 

For example, a fixed platform can be a pier, dock, bridge, tower, pylon, stationed drilling rig, wind turbine, or moored buoy.  However, some of these are stationed on land, near a river, or the shoreline, or offshore.  It also might be installed with an intended purpose like tide gauge station, or a wave buoy, or a river discharge but still have other instruments such as meteorological sensors.

The categories are mapped using simple broaderThan (>) and narrowerThan (<) relationships using the MMI-ORR Mapping Tool.

= IOOS SOS Implementation = 

The Platform Vocabulary is an essential part of fulfilling the development of the IOOS SOS templates.  However, version 1.0 of the templates were complete without final guidance on the controlled vocabulary used in the templates to describe platformType.  This was unavoidable as we had to make progress.  The immediate goal is to complete the platform vocabulary before release of the version 1.1 and it is expected the vocabulary will be resolved before that.  

{{{
<sml:classifier name="platformType">
   <sml:Term definition="http://mmisw.org/ont/ioos/definition/platformType">
      <sml:codeSpace xlink:href="http://mmisw.org/ont/ioos/platform/moored_buoy"/>
      <sml:value>MOORED BUOY</sml:value>
   </sml:Term>
</sml:classifier>
}}}

Any term within [http://mmisw.org/ont/ioos/platform IOOS Platform Vocabulary] can be used for {{{<sml:classifier name="platformType">}}}.  Chosing the most appropriate one is assisted by viewing the hierarchy through SPARQL query that uses the relationship mappings.  

=SPARQL Queries=

SPARQL searches can list the hierarchical categories, thus helping data managers pick platformType for SOS and allow IOOS Asset Inventory to search SOS based on different categories.  Others queries can show relationships to other registered vocabularies.

In general, SPARQL queries can be done against the MMI Ontology Registry and Repository (ORR)SPARQL endpoint at [http://mmisw.org/ont/?sparql] using HTTP GET and POST requests. A web based [http://mmisw.org/ont/sparql.html form] is accessible on the MMI Website for submitting SPARQL queries.  Some specific Platform Vocabulary example queries are provided here:

    * [http://mmisw.org/ont/?sparql=PREFIX+ioos%3A+%3Chttp%3A%2F%2Fmmisw.org%2Font%2Fioos%2Fplatform%2F%3E%0D%0ASELECT+DISTINCT+%3Fcat+%3Fplatform+%3Fdefinition%0D%0AWHERE%0D%0A++++{%3Fplatform+a+ioos%3APlatform+.%0D%0A+++++%3Fplatform+ioos%3ADefinition+%3Fdefinition+.%0D%0A+++++%3Fcat+skos%3AnarrowMatch+%3Fplatform+.%0D%0A+++++}%0D%0AORDER+BY+%3Fcat+%3Fplatform%0D%0A List Platform Terms by General Platform Types]
{{{
PREFIX ioos: <http://mmisw.org/ont/ioos/platform/>
SELECT DISTINCT ?cat ?platform ?definition
WHERE
    {?platform a ioos:Platform .
     ?platform ioos:Definition ?definition .
     ?cat skos:narrowMatch ?platform .
     }
ORDER BY ?cat ?platform
}}}
    * [http://mmisw.org/ont/?sparql=PREFIX+ioos%3A+%3Chttp%3A%2F%2Fmmisw.org%2Font%2Fioos%2Fplatform%2F%3E%0D%0ASELECT+DISTINCT+%3Fcat%0D%0AWHERE+{%3Fp+a+ioos%3APlatform+.%0D%0A+++++++%3Fcat+skos%3AnarrowMatch+%3Fp+.%0D%0A++++++}+%0D%0AORDER+BY+%3Fcat%0D%0A List General Platform Types]
{{{
PREFIX ioos: <http://mmisw.org/ont/ioos/platform/>
SELECT DISTINCT ?cat
WHERE {?p a ioos:Platform .
       ?cat skos:narrowMatch ?p .
      } 
ORDER BY ?cat
}}}

= Platform Vocabulary Use Cases =
The following use cases help derive requirements for the IOOS Platform Vocabulary.  These use cases are draft examples and include an initial set of guidelines for the vocabulary. 

  # The Program Office has a requirement to report assets in broad categories (e.g. buoys, HF radars, fixed stations near or on the coasts) for data calls and budgetary reports.  The platform vocabulary should be hierarchical so that the assets may be reported according to few large classes (less than 10).
  # Definitions for the platform vocabulary must be prescriptive to avoid misclassification.  In the previous version of the IOOS Asset Inventory, similar assets were assigned different platforms across the Regional Associations.  
  # The platform vocabulary must be able to handle mixed platforms (combined shore sensors measuring water temperature and met sensors measuring wind speed). 
  # If a hierarchical structure is used for the vocabulary, the platform must be able to be uniquely identified using the MMI framework, and the structure should be transparent.  For example, if wave buoy is a subclass of buoy, and the Platform Type is listed as wave buoy, then the XPath provided should direct you to a page where wave buoy is noted as a subclass of buoy.  

= Existing Platform Vocabularies =
MMI Platform Vocabulary: 
    * [http://mmisw.org/ont/mmi/platform Platform Ontology] 

BODC (SeaDataNet): 

    * [http://www.seadatanet.org/Standards-Software/Common-Vocabularies SeaDataNet Common Vocabularies]
    * [http://seadatanet.maris2.nl/v_bodc_vocab/search.asp?name=(L06)%20SeaVoX+Platform+Categories&l=L06 L06 SeaVoX Platform Categories]
    * [http://seadatanet.maris2.nl/v_bodc_vocab/search.asp?name=(L061)%20SeaVoX+Platform+Classes&l=L061 L061 SeaVoX Platform Classes]
    * [http://seadatanet.maris2.nl/v_bodc_vocab/search.asp?name=(L062)%20SeaVoX+Platform+Class+Categories&l=L062 L062 SeaVoX Platform Class Categories]

= Who to Contact =

John Ten Hoeve, Rob Ragdale, Hassan Moustahfid. and Sara Haines, to date, have been most active in developing the Platform Vocabulary.  If you are interested please or have comments or addtions, contact Rob Ragsdale (Rob.Ragsdale@noaa.gov), Hassan Moustahfid (Hassan.Moustahfid@noaa.gov) or John Ten Hoeve (John.tenhoeve@noaa.gov).  

=Appendices=
==Appendix A Proposed Hierarchical structure==

A hierarchical structure has been proposed for the Platform Vocabulary in order meet reporting requirements, for example from the IOOS Asset Inventory or IOOS Catalog.  Here is an example to provide context to this proposal: 

|| Platform Type            || Subclass                 || Subclass ||
|| Animal                   || Fish                     || Tuna     ||
||                          ||                          || Shark    ||
||                          || Mammal                   || Whale    ||
|| Buoy                     || Moored Buoy              ||          ||  
||                          || Moored Profiling Buoy    ||          ||
||                          || Drifting Buoy            ||          ||
||                          || Drifting Profiling Buoy  ||          ||
||                          || Wave Buoy                ||          ||
|| Cabled Array             || Subclass                 ||          ||
|| Fixed Drilling Platform  ||                          ||          ||
|| Fixed Station            || Station                  || Dock     ||
||                          ||                          || Pier    ||   
||                          ||                          || Tower    ||
||                          || Fixed Inland Station     || Tower    ||
||                          ||                          || Roof     ||  
||                          || Fixed Off-shore Station  || Tower    ||  
||                          ||                          || Mooring  || 
|| Radar                    ||                          ||          ||
|| Sampling Location        ||                          ||          ||
|| Satellite                ||                          ||          ||
|| Vehicle                  || Aircraft                 ||          ||
||                          || Autonomous Underwater Vehicle ||     || 
||                          || Glider                   ||          ||
||                          || Towed Vehicle            ||          ||
||                          || Vehicle                  ||          ||
||                          || Vessel                   ||          ||

== Appendix B. List of IOOS Platform Vocabulary Terms ==
This is the complete list of IOOS Platform Vocabulary Terms used in the 2011 IOOS Asset Inventory.  

|| Acoustic Doppler Current Profiler            ||
|| Acoustic System ||
|| ADCP||
||ADCP (SELF-CONTAINED)||
||ADCP Profiler||
||AIRCRAFT||
||AIS||
||AUV||
||BUOY||
||CABLED ARRAY||
||Coastal Met||
||Coastal Wave/Met||
||CTD||
||CTD/MET||
||Doppler Radar||
||DRIFTER||
||Drifter||
||Drifter Buoy||
||Field Station||
||FIXED BOTTOM STATION||
||FIXED MET STATION||
||FIXED SHORE STATION||
||FIXED TIDE GAGE||
||FIXED WQ STATION||
||GLIDER||
||HF Radar||
||Ice Profiling Sonar||
||IR Camera||
||Met Station||
||MOORING||
||OTHER||
||OTHER - TOWED VEHICLE||
||Passive Acoustic Recorder||
||PIER||
||PRESSURE SENSOR||
||Research Ship||
||RIB Boat||
||ROV||
||Sailing Vessel||
||SeaBird CTD||
||SL ADCP Profiler||
||SMAST Pier||
||SODAR||
||Subsurface Mooring||
||SUB-SURFACE MOORING||
||Tide Gauge||
||TOWER||
||UUV||
||VEHICLE||
||VESSEL||
||WATER LEVEL STATION||
||Wave Buoy||
||Weather Stations||
||X-band Radar||
||Ship, research||
||Ship, fishing||
||Ship, other||
||Buoy, moored||
||Buoy, drifting||
||Autonomous Underwater Vehicle||
||Glider||
||Animal||
||aircraft||
||satellite||

== Appendix C. Regional Build-Out Platform Definitions ==

The following were extracted from IOOS Regional Build-Out Plans.

*SECOORA*

|| *Gliders, Profilers and AUVs:* || 
|| Underwater Gliders are autonomous underwater vehicles (AUVs) and Profilers programmed to survey the ocean in transects. They can be used for physical and/or water quality sampling (HABs, outfalls, hazardous spills), or with acoustic sea gliders, tracking fish and marine mammals as well as monitoring ambient noise and mapping habitat. || 
|| *AXBTs, AXCTDs, AXCPs* || 
|| Airborne expendable bathythermograph; airborne expendable Conductivity, Temperature, depth; airborne expendable current profilers ||

*NANOOS*

|| *Shore Stations (weather)* || 
|| Meteorological stations provide wind speed and direction, air temperature, sea surface temperature, barometric pressure, humidity, AIS, and rainfall levels. || 
|| *Shore Stations (water) * || 
|| Fixed stations provide water properties at discrete depths, either just surface or surface and deeper. ||
|| *Single-Purpose Buoys * || 
|| Buoys measure waves and SST. ||
|| *Multi-Purpose Buoys * || 
|| Multidisciplinary long-term moorings for shallow water (100 m depth) with a surface buoy and a suite of sensors in the water column below to provide water column conditions at specific depth. ||
|| *Biogeochemical Profiling * || 
|| Automated sensors on  piers  to measure temperature, salinity, chlorophyll, turbidity and water level at frequent intervals in the nearshore coastal ocean.  Add carbon dioxide and oxygen sensors to track ocean acidification and hypoxia in the nearshore environment. ||
|| *Estuarine fixed * || 
|| Fixed stations provide water properties at discrete depths, either just surface or surface and deeper. ||

*CeNCOOS*

|| *Shore Stations (weather; cameras; AIS)* || 
|| Stations measuring meteorological variables and located on coastal lands, piers or docks. We have also included AIS transmitters and automated cameras regularly imaging the ocean, bays or estuaries in this column. || 
|| *Shore Stations (ocean)* || 
|| Stations attached to piers, docks or other structures connected to the shoreline with sensors submerged in water. || 
|| *Moorings* || 
|| Stations attached to a float located at the surface or within the water column and moored to the seafloor.  Sensors may be located at the surface or anywhere in the water column. || 
|| *Seafloor Mounted Stations* || 
|| Stations mounted on the seafloor with no flotation above, e.g. poles, tripods. Measurments may be from anywhere in the water column between the seafloor and the surface. || 
|| *Underwater Gliders: Coastal* || 
|| Spray Underwater Gliders are buoyancy driven profiling autonomous underwater vehicles programmed to survey the ocean || 
|| *Ships/ propeller-driven AUVs* || 
|| Ships are used to make a variety of measurements along fixed regularly occupied transect lines, and also to rapidly respond to changing events and conditions  || 
|| *Jet skis, ATVs* || 
|| Small manueverable vehicles for use in shallow water, or on the beach. || 
|| *Drifters* || 
|| Low cost devices with drogue designed to follow near surface currents.   || 
|| *Animals* || 
|| CTD, light, and other sensors may be attached to animals, such as elephant seals, that travel long distances || 

== Appendix D. SECOORA and NANOOS Asset Definitions ==

*SECOORA Asset Map -- Platform Types*
Identifies which of several platform types that best describes a platform. Valid values are:

||PlatformType||
||Buoy||
||HF Radar||
||Drifter||
||Ship||
||Tower||
||AUV||
||ROV||
||Cabled Array||
||Fixed Bottom Station||
||Sub-surface Mooring||
||Aircraft||
||Satellite Imagery Downlink||
||Other (anything not covered in the above list) ||

*NANOOS Asset classes:*
  * _Stationary In-Situ Observations (SISO)_. Current types: Buoy, Fixed Shore Station, River Gage, Land Station, Seabed Cabled Observatory
  * _Moving-Location observations (MLOC)_. Cruises, AUV's
  * _Gridded Regular and Irregular Data (GRID)_. Models (forecasts), remote sensing imagery, etc.



=Discussion Forum=

*Sara Haines - 11/28/12*

The Platform Vocab wiki page is a great start.  The use cases really help to understand what the issues are.  Nice addition. Here are my  questions and comments to consider (mostly with regard to the table and but also to help refine use cases).
 
1. Are cameras and radars sensors? Should we classify stations with subclass HFR and webcam stations

2. A cabled array is a set of platforms. 

3. Drifters, buoys, and floats?? not sure how to categorize or map with fixed-station, fixed-profiling, profiling, profile-drifting types of these platforms (discuss more)

4. There should be definitions for each of the platform types (this might help the above comments and questions)


*John Ten Hoeve - 11/29/12*

Thanks for the comments Sara.  You bring up a lot of good points that Rob and I were struggling with here.  

1. We were particularly struggling with the compromise between having accurate terms for platforms but also employing jargon that people have already used.  HFR is a great example, as you noted.  It's technically a sensor, but what would be the platform?  Shore station possibly?  That's why I initially included it as a platform in the table to be more specific.  

2.  I agree with your take on cabled array - it's really a set of platforms but I'm not sure how data from cabled arrays will be handled through web services yet, for instance, SOS.  Will each element of the array be considered a different platform in the world of SOS (i.e. a different DescribeSensor file for each subsurface mooring of the cabled array?)  If so, then the cabled array may be a network and the individual elements, platforms?  In that case, cabled array maybe wouldn't have to be in the platform vocabulary?

3.  I also had trouble with buoys, drifters, floats, and moorings.  I agree that this need some thought.  My best attempt was in the table on the wiki.

4.  I agree that definitions would help a lot

5.  Another issue with the hierarchical framework is that if the lowest element of the hierarchy is used to populate the PlatformType field, then there may be similar terms used across different branches of the hierarchical tree.  I know that in SOS at least you could trace the hierarchy by using the MMI reference, but it still may be confusing for people who only want to look at the term.  Is it worth it to make terms more explicit?  In other words, instead of "Fixed Station"/"Inland Station"/"Dock" in the hierarchy, have a term like "Fixed Station - Inland Station - Dock"


*John Ten Hoeve - 12/13/12*

Some thoughts from the teleconference today:

1.  One of the primary goals is a list of terms and precise definitions

2.  Do we want a hierarchical structure a flat structure?

3.  The vocabulary should be consistent with the international community

4.  Look to other vocabularies for examples and guidance

5.  Hassan's Comment: We need a list of synonyms for the platform vocabulary and we should also be mindful of the specific attributes of those platforms

*John Ten Hoeve - 01/02/13*

Another thought while reading regional progress reports: Since one mooring platform name can have surface and bottom nodes, there may be a need for a term that describes these types of platforms.

*??? - ??/??/??*

  * The work on an IOOS Non-Federal Asset Inventory in mid 2011 (previously led by Sam Walker) also used some relevant semi-controlled vocabularies; these should be examined.

*Derrick Snowden - ??/??/??*

_DPS Comment: There is a significant conflict in our use of station and platform as synonyms that will be especially evident when we get to the point of tracing lineage within SensorML.  In my mind a platform is a piece of equipment that hosts or carries one or more instruments or sensors.  It can be moved, it has a beginning and ending, and most importantly it's configuration can be modified which raises the requirement to trace the lineage of any data originating from a platform.  A station on the other hand is a fixed location at which a platform might be deployed for a finite period of time.  The station may persist longer than any one platform deployment at that site.  Think of the many different instruments that have derived CO2 at the Mauna Loa site where the [http://en.wikipedia.org/wiki/Keeling_Curve Keeling Curve] was observed as an example of this concept. What are the implications if we adopt this view of those two terms?_
  
See also [DescribeSensorMetadataForIOOSSOS discussion by Micah, in wiki page DescribeSensorMetadataForIOOSSOS].

*Note from Emilio - ??/??/??*

Describe and make the [http://nvs.nanoos.org NVS] asset/platform-type map icons available through this wiki later on. See Mayorga et al, 2010 ("NVS DMAC" Oceans'10 paper).

* Questions from Emilio? - ??/??/??*

Document existing practices and options regarding controlled vocabularies for "platform types" in SensorML DescribeSensor responses. [http://mmisw.org/ont/mmi/platform/ MMI vocabulary]. Note the use of Classification terms from http://mmisw.org/ont/mmi/platform/ . Consequences for IOOS Catalog, including the use of NVS asset-type map icons.

Station Classifiers (in sml:classification/sml:ClassifierList) used in the NANOOS SOS as a draft incomplete implementation, borrowing from either NDBC or NOS/COOPS and possibly others:
{{{
<sml:classifier name="System Type Identifier">
    <sml:Term definition="urn:ioos:def:classifier:NOAA::systemTypeID">
        <sml:codeSpace xlink:href="http://mmisw.org/ont/mmi/platform/" />
        <sml:value>Platform</sml:value>
    </sml:Term>
</sml:classifier>
<sml:classifier name="Platform Type">
    <sml:Term definition="urn:ioos:def:classifier:NOAA:platformType">
        <sml:codeSpace xlink:href="http://nvs.nanoos.org"/>
        <sml:value>MOORED BUOY</sml:value>
    </sml:Term>
</sml:classifier>
}}}

A question I've had about this implementation is, _what the heck is "urn:ioos:def:classifier:NOAA:" referring to?_ I know these urn's don't have to correspond to anything that's documented (much less actual URL's), but are these instances referring to anything that's been discussed or decided before?

*Sara Haines* - 04/02/2013

Do we need to distinguish or articulate that the platform vocabulary is about types and their definitions and not a list of platform identifiers (e.g. )