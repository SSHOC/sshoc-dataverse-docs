## Context
This external controlled vocabularies functionality was developed by Data Archiving and Networked Services (DANS-KNAW), the Netherlands, and funded by [SSHOC](https://sshopencloud.eu/), "Social Sciences and Humanities Open Cloud". SSHOC has received funding from the European Union’s Horizon 2020 project call H2020-INFRAEOSC-04-2018, grant agreement #823782.
 
Please watch [this online presentation](https://www.youtube.com/embed/g6-pVE3i_5I), read [the document with requirements](https://docs.google.com/document/d/1txdcFuxskRx_tLsDQ7KKLFTMR_r9IBhorDu3V_r445w/edit?ts=5fdbca9a) and join [Dataverse Working Group on Ontologies and Controlled Vocabularies](https://dataverse.org/community-calls) if you have some questions and want to contribute.

Pull Requests: [#7712](https://github.com/IQSS/dataverse/pull/7712) [#7946](https://github.com/IQSS/dataverse/pull/7946)
 
## Motivation
(Note: the text below is adapted from an analysis document by @qqmyers and @4tikhonov. Some of the initial requirements have been dropped and a few others have been added.)
 
### Current CVOC-support
Dataverse supports use of internally managed controlled vocabularies as part of metadata blocks. Any metadata block field can be associated with a fixed list of terms that are the allowed values for that field. The user interface for entering values supports picking from a drop-down list of all available values. The display interface simply shows the value used. (The Geospatial block country field is an example).
 
Dataverse also allows un-verified entry of metadata from external controlled vocabularies. In these cases, a compound field is often used so that the user can specify the name/URI of the vocabulary used. Examples include the keyword and topic fields which include subfields for the vocabulary URI and name, and the term (value in the vocabulary) chosen (without a field for a URL of the value itself).
 
### New feature: externally managed controlled vocabularies, with URI-defined terms
In order to overcome the limitations of the currently available options a new feature is proposed: the ability to configure a compound field with four subfields for: vocabulary name, vocabulary URL, term and term URL respectively.
 
Requirements:
 
* Enable metadata fields to be associated with external vocabularies.
* Enable Dataverse to store the URI for vocabulary values.
* Support auto-complete for internal/external CVOCs.
* Allow fields to be associated with multiple vocabularies and/or support controlled and free-text values (e.g. for keywords).
* Gracefully handle situations where an external vocabulary is temporarily or permanently off-line.
* Change the display to allow linking out to an external page for a given term.
* Support migration of existing fields/values to any new CVOC-capability
* Support use of CVOCs as query terms, e.g. in advanced search, or adding a link/button to find datasets with the same CVOC near the term itself in metadata displays.
* CVOC term entry via API.
* Fields that are associated with a single vocabulary should preselect the vocabulary.
* URL-subfields must not be editable by the user, as they are auto-filled based on a selection from a list.

