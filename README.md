# Global supply-demand ecosystem service models for ARIES

This project contains a baseline conceptualization of ecosystem services (ES) supply 
and demand for the [ARIES](http://aries.integratedmodelling.org) platform. The logical 
statements, data and models provided here are used in ARIES to answer queries for 
commonly recognized ES value metrics when not enough information is available to 
build detailed, dynamic flow models. 

The models built by ARIES using this knowledge have, in general, similar resolution 
and conceptual detail as those available in other ES assessment toolkits such as 
InVEST or ESTIMAP. Some of the methods implemented in this project are inspired by 
or derived from others; when so, sources are credited in the documentation built 
during each ARIES session.

The latest version of the content of this project is served by the ARIES semantic 
network and is thus available to any user of the ARIES platform, i.e. anyone who 
is using the k.LAB Explorer or Modeler software (locally or, when available, online) 
and has obtained a certificate that includes ARIES. No further downloads or installations 
are required. Details on how to obtain a certificate can be found at the [ARIES](http://aries.integratedmodelling.org) 
or the [Integrated Modelling Partnership](http://www.integratedmodelling.org)} web 
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
* Outdoors recreation
* Pollination
* Sediment retention

Areas in development for a forthcoming release in the short term include:

* Mariculture suitability
* Water availability

In addition, this project provides a bridge to Multiple Criteria Analysis models 
that allow automated *trade-off analysis* between diverse ES metrics, combined with 
user-specified weights that encode priorities according to the point of view of one 
or more stakeholders.

## Example queries

As ARIES operates on conceptual queries, the model content provided here does not 
implement monolithic "models" of ES, but rather provides the logical and computational 
underpinning to _resolve_ ES-related user queries in a user-selected spatial and 
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
    * Realized value of Outdoors Recreation
    * Potential value of Outdoors Recreation
    * Demanded value of Outdoors Recreation
    * value of Outdoors Recreation (production function combining supply and demand)
    * Net value of Outdoors Recreation (surplus/deficit)
* Pollination:
    * Occurrence of Pollinator Insect caused by Weather
    * Occurrence of Pollinator Insect caused by Landscape
    * Occurrence of Pollinator Insect
    * Net value of Pollination (surplus/deficit)
* Sediment retention:
    * Potential Removed Soil Mass [in t/ha or other units]
    * Retained Soil Mass caused by Vegetation [as above]

For all of these queries, ARIES will build a spatially explicit observation, in most 
situations as a raster GIS coverage of user-selected resolution. The results will 
reflect the contents of the ARIES semantic web at the time of query; nearly all supporting 
data are currently available at spatial resolution ranging between 1km and 90m.

# Platform

This project is written in the k.IM semantic modeling language and requires the k.LAB 
software stack version 0.10.0 or higher. Like in all k.LAB applications, each model 
in this project is _logically_ self-contained and can be run in isolation; each is 
expressed in the terms of the [IM worldview]() and must be run within the [k.LAB network]() 
in order to resolve every logical dependency to data or models appropriate for the 
context and scale of interest.

# Documentation

Models written in k.IM are close to the English language and aim to be _naturally_ 
readable. A look at the k.IM files in the src/ directory should provide enough detail 
as is. Documentation templates for each model are also included in this project, 
formatted for the k.LAB documentation engine, so that each run can self-document 
into a detailed human-readable report. 

A scientific article about the models included in this project is in review at the 
time of this writing, and will be linked here as soon as publicly available.

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
