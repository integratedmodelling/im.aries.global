# Global supply-demand ecosystem service models for ARIES

This project contains a baseline conceptualization of ecosystem services (ES) supply 
and demand for the [ARIES](http://aries.integratedmodelling.org) platform. The logical 
statements, data and models provided here are used in ARIES to answer queries for 
commonly recognized ES value metrics when not enough information is available to 
build detailed, dynamic flow models. A [published article](https://www.sciencedirect.com/science/article/pii/S0048969718338737#bb0130) in Science of The Total Environment describes in detail the philosophy behind the models, their scope and their limitations.

The models built by ARIES using this knowledge have, in general, similar resolution 
and conceptual detail as those available in other ES assessment toolkits such as 
InVEST or ESTIMAP. Some of the methods implemented in this project are inspired by 
or derived from others; when so, sources are credited in the documentation built 
during each ARIES session.

The latest version of the content of this project is served by the ARIES semantic 
network and is thus available to any user of the ARIES platform, i.e. anyone who 
is using the k.LAB Explorer or Modeler software (locally or, when available, online) 
and has obtained a k.LAB certificate that includes ARIES. No further downloads or installations 
are required. Details on how to obtain a certificate and the software can be found at the 
[ARIES](http://aries.integratedmodelling.org) or the 
[Integrated Modelling Partnership](http://www.integratedmodelling.org) web 
sites.

The models can run everywhere on the globe without user input. Customization of data, 
models and scenarios is possible using the k.LAB Modeler at the time of this writing. 
Drag-and-drop input of user data, as well as scenario analysis, will be made possible 
through the k.LAB Explorer in 2019.

# Contents and use

As released, the project contains fully specified model content concerning the following 
ES problem areas:

* Riverine flood regulation
* Carbon storage
* Outdoor recreation
* Pollination
* Sediment retention

Areas in development for a forthcoming release in the short term include:

* Water availability (based on hydrological calculations)
* Biodiversity value (based on machine learning of expert opinion)
* Mariculture suitability

In addition, this project provides a bridge to Multiple Criteria Analysis models 
that allow automated *trade-off analysis* between diverse ES metrics, combined with 
user-specified weights that encode priorities according to the point of view of one 
or more stakeholders.

## Example queries

As ARIES operates on conceptual queries, the model content provided here does not 
implement monolithic "models" of ES, but rather provides the logical and computational 
underpinnings to _resolve_ ES-related user queries in a user-selected spatial and 
temporal context. These can be entered in the ARIES Explorer interface as English 
sentences, as exemplified below, or chosen from a customizable "palette" of concepts 
of interest.

Some example queries per each ES category whose value is available globally at regional 
to country scales and with seasonal to annual temporal scale:

* Flood regulation:
    * probability of Flood
    * Potential value of FloodRegulation
    * Demanded value of FloodRegulation
    * Net value of FloodRegulation (surplus/deficit)
* Outdoors recreation:
    * Potential value of Outdoor Recreation (Recreation Opportunity Spectrum)
    * Theoretical value of Outdoor Recreation
    * Demanded value of Outdoor Recreation
    * value of Outdoor Recreation (production function combining supply and demand)
    * Net value of Outdoor Recreation (surplus/deficit)
* Pollination:
    * Occurrence of Pollinator Insect caused by Weather
    * Occurrence of Pollinator Insect caused by Landscape
    * Occurrence of Pollinator Insect
    * Net value of Pollination (surplus/deficit)
* Sediment retention:
    * Potential Removed Soil Mass
    * Retained Soil Mass caused by Vegetation
* Carbon storage:
    * Organic Carbon Mass      [total soil and vegetation storage]
    * Vegetation Carbon Mass   [total vegetation storage]
    * Soil Organic Carbon Mass [total soil storage]
    * Mangrove Carbon Mass     [mangrove above and below-ground storage]
      
For all of these queries, ARIES will build a spatially explicit observation, in most 
situations as a raster GIS coverage of user-selected resolution. The results will 
reflect the contents of the ARIES semantic web at the time of query; nearly all supporting 
data are currently available at spatial resolution ranging between 1km and 90m.

# Platform

This project is written in the k.IM semantic modeling language and requires the k.LAB 
software stack version 0.10.0 or higher. Like in all k.LAB applications, each model 
in this project represents a complete strategy to observe one concept, and can be run in isolation or as a dependency of other models. Each is 
expressed in the terms of the concepts contained in the [IM worldview](http://www.integratedmodelling.org/?page_id=540) and must be run within the [k.LAB network](http://www.integratedmodelling.org/?page_id=471) 
in order to resolve every logical dependency to data or models appropriate for the 
context and scale of interest.

# Documentation

Models written in k.IM are close to the English language and aim to be _naturally_ 
readable. A look at the k.IM files in the src/ directory should provide enough detail 
as is. Documentation templates for each model are also included in this project, 
formatted for the k.LAB documentation engine, so that each run can self-document 
into a detailed human-readable report. 

More details on the models and their derivation are available in Martinez-López et al. (2018).

# License

These models, like the entirety of the k.LAB infrastructure that runs them, are open 
source, released under the terms of the Affero General Public License 3.0 or any 
higher version.

The intellectual property of this content belongs to the Integrated Modelling Partnership 
and all individually listed authors.

# Contact

Inquiries about ARIES, k.LAB or any of the models included in this project should 
be directed to info@integratedmodelling.org.

## Authors (alphabetical)

* Kenneth J. Bagstad (kbagstad@usgs.gov)
* Stefano Balbi (stefano.balbi@bc3research.org)
* Ainhoa Magrach (ainhoa.magrach@bc3research.org)
* Javier Martínez-Lopez (javier.martinez@bc3research.org)
* Ferdinando Villa (ferdinando.villa@bc3research.org)
* Brian Voigt (bvoigt@uvm.edu)

## References

Javier Martínez-López, Kenneth J. Bagstad, Stefano Balbi, Ainhoa Magrach, Brian Voigt, Ioannis Athanasiadis, Marta Pascual, Simon Willcock, Ferdinando Villa. Towards globally customizable ecosystem service models,
Science of The Total Environment. Volume 650, Part 2,
(2019), 2325-2336 DOI https://doi.org/10.1016/j.scitotenv.2018.09.371.
