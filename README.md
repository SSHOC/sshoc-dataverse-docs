# Social Sciences and Humantities Open Cloud (SSHOC) Dataverse tasks

SSHOC Dataverse project, task 5.2 has a two parallel tracks of the development: 

* Core development team is working on the modification and extension of the Dataverse core functionality. All tasks of this team will get label Core.
* Application development team will create new or will integrate existent tools that will be published on Dataverse App Store website. Tasks of this team will be labelled as App.

Important: all new Dataverse SSHOC functionality should be delivered to IQSS repositories for further maintenance, Docker images published on Docker Hub and deployed on Kubernetes platform.

Philipp Conzett (CLARIN/UiT, Norway)


* (Core) Compliance with CLARIN metadata requirements
* (App) Controlled vocabulary(ies) for CLARIN resources
* (Core) Compliance with OpenAIRE requirements/recommendations
* (Core) Translation of Dataverse into Norwegian
* (App) eduGAIN log-in support
* (Core) Separate metadata record from data record
* (App) RDF compliance, e.g. JSON-LD, incl. SPARQL endpoint
* (Task) Developments should be deployed in the Dataverse main (Harvard) distribution
* (Task) Plan for CoreTrustSeal sertification

Tomasz Parkoła (Poznan, Poland):


* (Task) setup dataverse for DARIAH community (PSNC together with GWDG) - does it make sense to have one dataverse for whole DARIAH?
* (App) integration with marketplace (not obvious, but maybe we could expose on marketplace collections of data from specific dataverse instances if they are really interesting for DH)
* (App) authentication mechanism embedded in Dataverse, which allows integration with DARIAH SSO. There might be already such a feature, but maybe needs some adjustments. Dataverse supports OpenId/OAuthh and SAML. In addition we could also integrate instances of Dataverse with PIONIER ID (Polish AAI infrastrusture for Univerisities, R&D, etc.). 
* (App) integration with digital repositories / digital libraries in the sense that when submitting publications with datasets, the datasets are ingested into Dataverse, the publication ingested into digital repository and both interlinked with DOIs. Dataverse supports SWORD protocol which could be used in this context. 
* (App) integration of dataverse with long-term preservation tools, so that the items/datasets stay preserved over long time. This could be done as a plug-in in dataverse - once object is submitted to dataverse it is then also transferred to the long-term preservation tool. Why this is marked as an App? 

Péter Király (Göttingen, Germany)


* (App) automatically publish data into Dariah repository (or into other domain specific repository) from Dataverse
* (App) investigation the possibilities of extending the feature set of Dataverse in a pluggable way, so how to develop individual piece of software which work together with Dataverse, but not part of it (plugins, modules, whatever we name them.)
* (Task) improving the DevOp apects of Dataverse, making the software updates, installation etc. a bit more straightforward
* (App, Core) develop further the custom metadata supporting functionalities in Dataverse. Current issues:
the process has two steps: adding fields into Dataverse then adding fields into Solr -- it should be done in one step. We should explode the Solr API for schema management
* Dataverse versions which supports new Solr versions come with a Solr schema file, which overwrites all previously defined custom fields using dynamic Solr fields would be more flexible than playing with the schema. The Dataverse developers said, that they are afraid of performance issues. We might conduct a performance measurement test to reject or approve this.

Slava Tykhonov (DANS-KNAW, Netherlands)
* Leading all technical development efforts
* (Core/App) Translation of the User Interface and SOLR and applications to maintain the translations
* (App) CESSDA metadata fully supported and adjustable 
* (App) Edugain/SURFconext federated login support
* (Core, App) Support of external controlled vocabularies (CESSDA CV Service)
* (App) Extension of Plugin with support of other PID providers (Philipp: e.g. ISLRN; cf. http://islrn.org/)
* (App) Development and integration of extra [data previewers](https://github.com/SSHOC/dataverse-previewers) as addition to ones maintained by [Global Dataverse Community Consortium (GDCC)](http://github.com/gdcc/dataverse_tests):
  * PDF preview
  * DDI Explorer
  * Text files
  * HTML preview
  * Spreadsheet 
  * Images
  * Video
  * Audio
  * JSON
  * GeoJSON/Shapefiles/Map using [Apache Superset integration with Dataverse](https://github.com/SSHOC/dataverse-superset)
  * XML (?)
* (App) The integration of external storage applications in the Cloud (Swift Object Storage). Tomasz Parkoła comment: Ceph would be an option for us too, as we mainly use Ceph in our datacentre.
* (Core) Adjustable pipeline for multilingual support based on [Weblate as a service](https://github.com/SSHOC/weblate-docker)
* (Core, App) Archiving pipeline from Dataverse to another Trusted Digital Repositories (Dataverse Bridge to Fedora, Islandora, Zenodo)
* (App) Development of Dataverse Metrics as a service (optional)
* (Task) Helping Harvard to develop of Dataverse App Store website
* (App) Sensitive Data Support (DataTags with GDPR, optional) 


Stefan Kasberger (AUSSDA, Austria)


* (App) the development of [pyDataverse module](https://pydataverse.readthedocs.io/en/latest/) to support (meta)data migration tasks and automation
* (App) NESSTAR migration tool, [DDI Converter](https://github.com/SSHOC/dataverse-ddi-converter-tool) development deployment on Root-Server via Docker. 
* (Core) [Preview of data](https://github.com/SSHOC/dataverse-previewers) (CSV, etc) for easy first understanding and exploration.
* (Core) Feedback Functionality for users (in general and on data level)
* (Core) Compliance with CMM.

