# DELEGATED REGULATION (EU) 2015/962 supplementing the ITS Directive (2010/40/EU)
## Provision of EU-wide real-time traffic information services
### Static data

**Road network links and their physical attributes – _geometry_:** the minimum information required for representing in a centerline or more precise manner the geometry of a road network’s links that connect two positions and therefore form a continuous path (without branches).
>Considering that road links constitute curvilinear elements, their geometry, according to INSPIRE data specifications, can be represented through the GM_Curve object included in the GM_Object hierarchy (ISO 19107).

>Alternatively, geometry can be provided through a piecewise linear representation.

>Reference/additional info: https://inspire.ec.europa.eu/id/document/tg/tn

**Road network links and their physical attributes – _road width_:** the minimum information required for indicating the width of a road network’s links.
>This information is addressed as encompassing in a discretized and systematic manner various components of the road surface, including driving lanes, hard shoulders, medians, parking space, and the roadside.[^1]
[^1]: Despite the fact that traffic capacity is the main concern of various RTTI-related use cases, lateral clearance constitutes a contextual factor for determining free-flow speed and, in turn, traffic capacity.

**Road network links and their physical attributes – _number of lanes_:** the minimum information required for indicating the number of lanes of a road network’s links.
>This information may be limited to regular traffic lanes or extended to cover additional components of the road surface (see above). In the latter case, it should additionally provide insights into which of those components can serve vehicular traffic and their respective contribution to directional traffic capacity.

**Road network links and their physical attributes – _gradients_:** the minimum information required for indicating the degree of inclination (or the rate ascent/descent) of a road network’s links.
>This information is typically identified as the maximum gradient along specific links of the road network to highlight restrictions for particular vehicle classes. Provided information may consider the direction of a given road network link, indicating whether the slope ascends (positive value) or descends (negative value), thus providing insights into the direction of elevation change.

**Road network links and their physical attributes – _junctions_:** the minimum information required for identifying the location of a junction and its relationship with the remaining entities of the road network.
>Considering that road network nodes may be used for technical reasons, e.g., defining an additional/separate road link between two positions that exhibit different physical attributes (e.g., substantially different road width or higher/lower number of lanes), junctions may be addressed in a separate manner as decision/choice nodes through which traffic can be diverted to another route.

>The relationship of a given junction with the remaining network can be expressed via the indication of the whether it is a start/end junction of a given link.

![Figure 1](/Figures/RTTI_fig_1.png)
> Reference/additional info: https://inspire.ec.europa.eu/id/document/tg/tn

**Road classification:** the minimum information required for distinguishing the links of a road network encompassing form of way, functional, or other concerns.
>According to INSPIRE data specification on transport networks (based on EuroRoads and GDF specifications), ‘form of way classification’ considers the physical properties of each road link (including accessible mobility modes), whereas ‘functional classification’ considers the importance of each road link within the road network. It is important to note that ‘form of way classification’ and ‘functional classification’ elements may vary in meaning across different European countries due to the lack of harmonization.

![Figure 2](/Figures/RTTI_fig_2.png)
>Reference/additional info: https://inspire.ec.europa.eu/id/document/tg/tn

**Traffic signs reflecting traffic regulations and identifying dangers:** the minimum information required for disseminating the location, type, and direction of signs (or panels) reflecting various traffic regulations and potential hazards on the road (e.g., warning signs).
>The following conditions/restrictions are mentioned in the Delegated Regulation (EU) 2015/962:
•	Access conditions for tunnels (legal or physical restrictions/limitations on vehicles to access a specific tunnel)\
•	Access conditions for bridges (legal or physical restrictions/limitations on vehicles to access a specific bridge)\
•	Permanent access restrictions (permanent legal or physical restrictions/limitations on vehicles to access a specific road link of any type)\
•	Other traffic regulations (other traffic regulations that apply along specific road links of any type)

>Considering that traffic signs correspond to specific points on a road link and may apply to specific directions, their location can be encoded through either the point or linear location referencing methods mentioned in the description of the SRTI data categories.

>Access restrictions/limitations can on a case-by-case basis be weight-, vehicle type-, and propulsion technology-related or depend on infrastructure categorization (e.g., tunnel categories).

>According to CEN/TS 17268 (TN-ITS model), other traffic regulations may involve mandatory turns to be taken, prohibited turns, prohibited stopping, prohibited use of audible devices, mandatory use of snow chains. CEN/TS 17268 TN-ITS model supports the provision of any traffic sign defined in the ISO 14826 graphic data dictionary (GDD).

>Reference/additional info: https://inspire.ec.europa.eu/id/document/tg/tn

**Speed limits:** the minimum information required for describing the speed limits (minimum and/or maximum) that apply on a road network link given a set of applicable conditions.
>Considering INSPIRE data specification on transport networks, information that should be provided for identifying a speed limit involves: a) an indication of whether it corresponds to a maximum or minimum speed, b) the value of the maximum or minimum speed (as applies), c) an indication of the direction that the speed limit is applicable, d) an indication of the lanes including the start lane (counted from the right hand) for which the speed limit applies, e) an indication of the applicable vehicle type, e) an indication of the period during which the speed limit is valid, and f) an indication of the weather conditions the speed limit is dependent on.

>The vehicle class dependent nature of speed limits is also recognized in the PIARC data dictionary.

>Reference/additional info: https://inspire.ec.europa.eu/id/document/tg/tn;  https://www.piarc.org/en/activities/Road-Dictionary-Terminology-Road-Transport/Dictionary-Terminology-Translation-Definition-Term-Search 

**Traffic circulation plans:** the minimum information required for disseminating and describing the content of plans that are developed by local authorities to control and guide traffic flows in response to known and recurring traffic conditions as well as in consideration of seasonality effects and existing limitation and constraints (e.g., existence of school zones).

>Traffic Circulation Plans (TCPs) are crafted by local authorities to manage and direct traffic flows based on recurring traffic conditions, seasonal variations, and pre-existing restrictions (such as school zones). These plans enclose strategies and measures, including, for example, the designation of particular road links that certain users or vehicle types should avoid, aimed at improving traffic flow conditions and achieving societal objectives like lowering emissions and minimizing accidents. The strategies implemented within TCPs are part of a broader, more enduring “traffic control policy”, meaning that the imposed measures remain active and applicable irrespective of the level of achievement of their overarching goal. TCPs are reviewed and updated by local authorities with a certain time frequency.

>On the other hand, Traffic Management Plans (TMPs) provide for the allocation of traffic control measures in response to specific predefined (or not) traffic scenarios, such as the management of heavy congestion or the closure of strategic routes due to extreme weather events, maintenance works, or a serious road accident. The objective of TMPs is to anticipate arrangements for controlling and guiding traffic flows in real-time conditions and informing road users about the traffic situation in a consistent and timely manner. TMPs, which differ in detail according to local circumstances, apply in the following cases:\
•	major traffic accidents\
•	congested traffic\
•	extreme weather conditions\
•	natural or technological catastrophes\
•	special events (sports, cultural, leisure) resulting in unusually high traffic volumes, capacity constraints, or temporary road closures.

>TMPs are either proactive or reactive to traffic conditions and events. They may be planned in advance (e.g., for managing cross-border traffic flows or in relation to specific weather events and road closures) and involve several traffic management authorities (e.g., more than one TMCs) due to the need for activating various traffic management measures, often requiring negotiation, acceptance, confirmation, and feedback. TMP may also be built in response to unexpected conditions and events (reactively) through real-time negotiation.

>The structural components of TMPs are:\
•	Title of the plan\
•	Concerned area\
•	Precise localization (location markers) and traffic direction\
•	Map-based information (indication of section(s) closed, diversions, rerouting, etc.)\
•	Applicable measures/traffic management procedures\
•	Coordinating actor\
•	Description of TMP workflow (activation request → implementation request → acknowledgements → implementation and information → suspension/deactivation request → acknowledgements)\
•	Actions of stakeholders and competent authorities\
•	Information and communication actions (e.g., traffic signs, radio messages, etc.)\
•	Related traffic restrictions (e.g., along the diversion routes)

>TCPs can be defined in a similar fashion to TMPs or in a more simplified manner. However, the key difference between TCPs and TMPs is that TMPs are deactivated when the event or condition (scenario) that has triggered their activation is resolved (which is not the case for TCPs).

>Reference/additional info: https://rno-its.piarc.org/en/network-operations-rno-activities-planning-and-reporting/traffic-management-plans

**Freight delivery regulations:** the minimum information required for disseminating regulations for delivering freight, such as designation of certain road links or areas, loading/unloading permissions or prohibitions, and time-related restrictions.
>Freight delivery regulations are typically developed by local authorities to help manage traffic flow and reduce the impact of freight vehicles on the road network. Their goal is to balance the needs of freight and passenger transportation. Freight delivery regulations may enclose additional information for clarifying the applicable type of freight (e.g., dangerous goods).

**Location of tolling stations:** the minimum information required for identifying the location (e.g., coordinates of a specific point, location along a linear element, mileage) of tollbooths (physical or virtual) collecting automatically or manually tolls from passing traffic.

**Identification of tolled roads, applicable fixed road user charges and available payment methods:** the minimum information required for indicating that tolls apply on a road link as well as for disseminating information about the applicable road user charges and available payment methods.

>Fixed road user charges are typically vehicle class dependent. A commonly used classification of vehicles for determining the applicable charges along European highways/motorways is the following:\
•	Class 1: Motorcycles, tricycle vehicles\
•	Class 2: Light vehicles (with or without trailer and height less than a threshold value)\
•	Class 3: Trucks, busses, and other heavy-duty vehicles with less than 4 axes (with or without trailer and height greater than a threshold value)\
•	Class 4: Trucks and other heavy-duty vehicles with 4 or more axes

>Fixed road user charges may also be time condition dependent. Time conditions can be discerned into (weekday/weekend) rush and regular periods. 

>Available payment methods in tolled roads may include a) on cash, b) by credit/debit card, c) electronic payment, and d) via toll stickers. Electronic payment can contextually be associated with a free-flow tolling system.

**Location of parking places and service areas:** the minimum information required for identifying the location of a) places[^2] where vehicles are allowed to park and b) places (typically along motorways) where drivers can stop, rest, and get access to available service facilities and amenities (alternatively expressed as rest areas).

>Safe and secure truck parking areas are not explicitly mentioned in this definition as they fall into the scope of DR (EU) 885/2015. SSTPAs can be addressed as a subset of rest areas (or in a separate manner if they strictly operate as such).

>Location information can be provided as coordinates, locations along linear elements, or areal locations. As regards service areas, it shall be clarified whether locations refer to entries/exits locations and/or center of gravity.

[^2]: "The location of places where vehicles are allowed to park" is present in Transmodel/NeTEx and thus an overlap with EU 2017/1926 exists. Since it is important to exactly relate parking locations to Public Transport access points this is an appropriate overlap for integrating data sets.

**Location of charging points for electric vehicles and the conditions for their use:** the minimum information required for disseminating the geographic location of charging infrastructure (charging pools), dedicated to electric vehicles, including the exact position of charging points along with the conditions for their use.

>A charging pool denotes an area equipped with one or more charging stations. These charging stations can take the form of fixed wall-mounted appliances (wallboxes) or self-standing units, both of which are connected to an electrical supply point. Depending on the number of charging points integrated into a single station, they can facilitate the simultaneous charging of multiple electric vehicles. A charging point may be fitted with several connectors but can only charge one vehicle at a time.

>The minimum information package must encompass the exact location of the charging infrastructure, contact options, opening times, a list of accepted payment methods, as well as information on the connector type. Information on location may be separated into exit and entrance location for larger areas or areas with strict rules for driving directions (e.g., along motorways).

>Based on the functional mapping of IDACS data requirements to DATEX II RSPs as well as the service profile of the DATEX II data model for energy infrastructure, the conditions for the use of charging points for electric vehicles may encompass the following aspects: a) opening hours (i.e., the period in which a charging point is accessible to the public), b) supported payment methods (e.g., active RFID chip, via an app, via calypso, on cash, by credit card, by debit card, etc.), c) available charging modes considering IEC 61851-1 specifications, d) available connectors (e.g., plugs, sockets, induction plates, etc.), e) whether it is possible, not possible, or mandatory for users to make a reservation, f) the types of vehicles that can be charged (e.g., electric buses, electric cars, electric motorcycles, electric bikes, electric boats, motorhomes, others), g) the maximum and minimum delivery amount, h) the available voltage and charging power, and i) information on the applied pricing policy (e.g., charging time based, delivery unit based, contract, flat rate, other).

>Reference/additional info: https://docs.datex2.eu/reference_profiles/rsp/alternativefuel/function2rsp.html; https://docs.datex2.eu/energy/index.html; CEN/TC 278/WG 8 N47.

**Location of compressed natural gas, liquefied natural gas, liquefied petroleum gas, and hydrogen stations:** the minimum information required for disseminating the geographic location of compressed natural gas, liquefied natural gas, liquefied petroleum gas and hydrogen refueling stations.

>Each station must have at least one refill point allowing the refuelling of one vehicle at a time. The minimum information package must encompass the exact location of the whole infrastructure (including refueling points), contact options, opening times, a list of accepted payment methods, as well as information on the allowed vehicle characteristics (e.g., size, weight).  Information on location may be separated into exit and entrance location for larger areas or areas with strict rules for driving directions (e.g., along motorways). Additionally, crucial details involve specifying the provided type of fuel.

**Location of public transport stops and interchange points:** the minimum information required for identifying the location of a) designated places at which public transport vehicles can stop with the aim of allowing passengers to embark and disembark and b) facilities allowing passengers to transfer between different modes of public transport (such as from bus to train, or from tram to bus) and carriers, thus encouraging intermodal transport practices and operations.[^3] [^4]

[^3]: The "location of public transport stops and interchange points" is a data category which exists in Transmodel/NeTEx and in INSPIRE. This represents an overlap with DR (EU) 2017/1926, namely: the location may be represented as a Postal Address, as a Road Address or as coordinates in a specific location referencing system. INSPIRE is the reference for the Postal Address format, whereas NeTEx is a reference for the Road Address format (see conclusions of the project "Inspire support to MMTIS").

[^4]:TN-ITS CEN/TS 17268 supports IFOPT (in alignment with European Norm IFOPT (EN 28701:2012).

**Location of delivery areas:** the minimum information required for identifying the physical location of designated points along a road network or on specific road links reserved for loading/unloading operations.

>Delivery areas can be of multiple types (e.g., instaboxes, warehouse storage, loading zone, etc.). Moreover, their accessibility may be public or restricted.

### Dynamic data

**Dynamic road status – _road closures_:** dynamic information disseminating the closure of road links of any type.
>Road closures are typically directional and discerned into planned and unplanned.

>**Planned road closures:** Correspond to **scheduled** shutdowns of entire road links (all lanes per direction) or sections of a given road link for various reasons, such as large public events. Such closure are typically announced in advance to enable road users plan alternative routes and minimize disruption to their travel plans and diaries.\
>**Unplanned road closures:** Correspond to **unexpected** shutdown of entire road links (all lanes per direction) or sections of a given road link without prior notice due to unforeseen events, such as sudden infrastructure failures. Such closures typically disrupt traffic flow in a mode-agnostic or mode-specific manner, causing substantial delays.

>The unambiguous description of road closures requires the provision of information about their time validity (applies to planned road closures) or time of occurrence (applies to unplanned road closures).

>Reference/additional info: TISA RTTI 5 Star Rating Scheme

**Dynamic road status – _lane closures_:** dynamic information disseminating the closure of a lane on road links of any type.
>Lane closures can be discerned into planned and unplanned in a similar fashion with "road closures".

>Their unambiguous description requires the provision of information about their time validity (applies to planned lane closures) or time of occurrence (applies to unplanned lane closures).

**Dynamic road status – _bridge closures_:** dynamic information disseminating the closure of road links corresponding to bridges.
>Bridge closures can be discerned into planned and unplanned in a similar fashion with "road closures".

>Their unambiguous description requires the provision of information about their time validity (applies to planned bridge closures) or time of occurrence (applies to unplanned bridge closures).

**Dynamic road status – _overtaking bans on heavy goods vehicles_:** dynamic information disseminating the prohibition of overtaking by heavy goods vehicles on specific segments of a road link (or on the entire link) due to adverse on-going conditions.
>Adverse conditions may on a case-by-case basis include: (a) adverse weather (e.g., heavy rain, ice, strong winds on bridges), (b) on-going road construction or maintenance activities, (c) traffic congestion, (d) accident or hazardous material spills, (d) visibility restrictions, and (e) special events.

>The unambiguous description of overtaking bans on heavy goods vehicles requires the provision of information about the time of their enforcement.

**Dynamic road status – _roadworks_:** dynamic information disseminating that roadworks take place on a specific segment/section of a road link (or on the entire road link).
>Roadworks typically affect (fully or partially) individual lanes and seldom all lanes of a given direction, such that travel in this direction is still possible. In case that roadworks affect all lanes, such that travel in a given direction is no longer possible, they match with road closures.

>Roadworks are also discerned into planned and unplanned.

>**Planned roadworks**: Correspond to **scheduled** maintenance, construction, or repair activities carried out on entire road links or specific segments/sections. Such activities are typically pre-arranged and annouced in advance by local authorities or road operators to minimize traffic disturbances and enable road users plan alternative routes.\
>**Unplanned roadworks**: Correspond to maintenance, repair, or construction activities that are undertaken **unexpectedly** and without prior scheduling. Such activities are typically initiated in response to urgent issues, such as road damage or infrastructure failures that require immediate actions.

>The unambiguous description of roadworks requires the provision of information about their time validity (i.e., start/estimated end time - if both possible for unplanned roadworks). The provision of such information facilitates their classification into _short-term_ and _long-term_ ones.

>Reference/additional info: TISA RTTI 5 Star Rating Scheme

**Dynamic road status – _accidents and incidents_:** dynamic information disseminating the occurrence of an accident or incident on a specific segment/section of a road link.
>"Accidents" and "incidents" are used to describe different types of situations/events with implications on prevailing traffic conditions (obstruction).

>**Accidents:** Typically correspond to unexpected situations/events that may result in damage to vehicles, injuries, or loss of life. Such situations/events may include collisions between vehicles, single-vehicle accidents (e.g., running off the road or hitting a stationary object), or accidents between vehicles and pedestrians, cyclists, or other vulnerable road users.\
>**Incidents:** Typically encompass a broader range of situations/events, i.e., any unplanned or unexpected situation/event that disrupts the normal flow of traffic, even if it does not involve a collision or injuries. This may include breakdowns, vehicle fires, spilled cargo, road debris, or even non-traffic-related situations/events like protests or animals on the roadway.

>The unambiguous description of accidents/incidents requires the provision of information about their type and time of occurrence.

**Dynamic road status – _dynamic speed limits_:** dynamic information disseminating temporary changes in the speed limit applying on a specific segment (or on the entire road link).
>The unambiguous description of dynamic speed limits requires the provision of information about their type (e.g., minimum or maximum speed limit), applicable fleets, and time validity.

>Please also consult the "Speed limits" static data category.

**Dynamic road status – _direction of travel on reversible lanes_:** dynamic information disseminating the active direction of travel on a reversible lane of a specific segment of a road link (or on the entire road link).
>The unambiguous description of direction of travel on reversible lanes requires the provision of information about its time validity.

**Dynamic road status – _poor road conditions_:** dynamic information disseminating the prevalence of poor conditions on a specific segment/section of a road link (or on the entire road link).
>Poor road conditions may happen due to various reasons. For more details, please consult SRTI data categories.

>The unambiguous description of poor road conditions requires the provision of information about the time of their occurrence and type (optionally).

**Dynamic road status – _temporary traffic management measures_:** dynamic information disseminating temporary traffic management measures in response to the current state of or conditions on particular segments, links, or parts of the road network, which can change over time due to several factors (e.g., road works, weather conditions, special events).
>Temporary/dynamic traffic management measures are usually developed by traffic managers with the aim of controlling and guiding traffic flows in response to unexpected/non-recurring traffic disturbances, but also with the aim of increasing road safety.

>Therefore, they are linked to Traffic Management Plans (TMPs). For more details, please consult the descriptions under the "Traffic circulation plans" static data category.

**Dynamic road status – _variable road user charges and available payment methods_:** dynamic information disseminating variable road user charges responding to a congestion/emission pricing policy scheme and the available payment methods.
>The conditions mentioned in fixed road user charges are assumed to be dynamically adapted in the context of non-fixed road user charges to reflect the prevailing traffic/air quality conditions in line with applied access control, congestion pricing, or low emission mobility policies.

>In line with the description of the "tolled roads" static data category, available payment methods may include a) on cash, b) by credit card, c) electronic payment, and d) via toll stickers. Electronic payment can contextually be associated with a variable free-flow tolling system.

**Dynamic road status – _availability of parking places_:** dynamic information reflecting the state and/or status of on-street and off-street parking infrastructure.
>Based on the documentation of the DATEX II parking publication, parking infrastructure encompasses urban or interurban parking sites and on-street parking places. Therefore, the dynamic information provided about parking sites should encompass both their state (e.g., open, full, closed) and status (i.e., number of available parking spots).

>Reference/additional info: https://docs.datex2.eu/downloads/parkinglight.html

**Dynamic road status – _availability of delivery areas_:** dynamic information reflecting the availability of designated places along a road network reserved for loading/unloading operations.

**Dynamic road status – _cost of parking_:** dynamic information reflecting the applicable cost of parking on charged parking infrastructure.
>Cost of parking can be defined in ex-ante context, considering, for example, time duration and time condition dependent aspects, or be dynamically adapted to existing parking demand. The latter case falls into the scope of the current data category.

**Dynamic road status – _availability of charging points for electric vehicles_:** dynamic information reflecting the state and status of charging points and stations for electric vehicles.

**Dynamic road status – _weather conditions affecting road surface and visibility_:** dynamic information disseminating the prevalence of (adverse) weather conditions affecting road surface and visibility and, thus, implying accident hazards for road users.
>The unambiguous description of weather conditions affecting road surface and visibility requires the provision of information about the time of their occurrence, type (optionally), and affected parts of the road network.

**Traffic data – _traffic volume_:** dynamic information indicating the number of vehicles, distinguished (or not) into light and heavy vehicles, passing through a specific point (road section) within a specified time period per direction.
>Traffic volume denotes the number of vehicles or persons passing a point (road section) within a defined time period, while flow rate denotes the number of vehicles or persons passing a given point per unit time (e.g., vehicles/hour).

**Traffic data – _speed_:** dynamic information indicating the travel speed of vehicles passing from a specific point or along a specific road segment within a given time aggregation interval.
>Speed values along specific road segments typically refer to average speeds (or harmonic/interquartile mean speeds) corresponding to a given time aggregation interval.

>Speed values on specific points typically refer to road section averages (e.g., obtained from inductive loop detectors).

**Traffic data – _location and length of queues_:** dynamic information indicating the point of a traffic queue dissipation and its total length.
>Vehicles are said to be in queue when the inflow rate in a road section exceeds the outflow rate.

>The point of traffic queue dissipation typically coincides with junctions/intersections in congested urban road networks. However, in sparse road networks queueing can happen upstream at a junction/intersection for various reasons, such as road accidents.

>The length of a queue may be simply defined as the interval between the point of queue dissipation and the last vehicle in queue. It can be measured in distance units or by the number of queueing objects.

>Reference/additional info: https://www.piarc.org/en/activities/Road-Dictionary-Terminology-Road-Transport/Dictionary-Terminology-Translation-Definition-Term-Search?q=queue&s=en&t1=&t2=&scope=term=queue

**Traffic data – _travel times_:** dynamic information indicating the time required for observed vehicles to cross a specific road link or to travel from a given point to another over a specified route under prevailing traffic conditions.
>According to PIARC data dictionary, travel time is defined as the time spent between two defined points.

>Reference/additional info: https://www.piarc.org/en/activities/Road-Dictionary-Terminology-Road-Transport/Dictionary-Terminology-Translation-Definition-Term-Search?q=travel%20time&s=en&t1=&t2=&scope=term=travel%20time

**Traffic data – _waiting times at border crossings to non-EU Member States_:** dynaming information indicating the average time required for vehicles to wait between their arrival at the queue of a border crossing (if any) and their departure.
>The scope of this data category is limited to border crossings from EU Member States to non-EU Member States.
