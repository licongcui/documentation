### Physio-MIMI Overview

> Physio-MIMI (Multi-Modality, Multi-Resource Information Integration environment) is an NCRR-funded, multi-CTSA site project designed to develop novel, flexible informatics methodologies, tools and infrastructure to facilitate the collection, management, and analysis of clinical and physiological data.

> <small>http://physiomimi.case.edu</small>

### Physio-MIMI VISAGE Interface
>VISAGE (VISual AGgregator and Explorer) is the query interface developed for Physio-MIMI. The goal is for VISAGE to be directly used by clinical researchers, for activities such as data exploration seeking to formulate, clarify, and determine the availability of support for potential hypotheses as well as for cohort identification for clinical trials.

> VISAGE has two main components: 

> 1. Query Builder, with ontology-driven terminology support and visual controls such as slider bar and checkboxes; 

> 2. Query Manager, which stores and labels queries for reuse and sharing;

> Go to Physio-MIMI website https://mimi.case.edu<sup>[Fig01]</sup>. Sign in if you already have an account registered, otherwise please Sign Up to request access (red box).

![Fig01](http://femi.case.edu:3003/physiomimi-01-login.png)
**Fig01: The Physio-MIMI website login page.**

> After you successfully login, you will see the **Query Builder** page<sup>[Fig02]</sup>. 

- In the "Area for data source selection" (red box 1), you can select data sources of interest (e.g., SHHS). 

- In the "Area for searching variable term" (red box 2), you can search for a specific variable term like "ahi" in the text box. Then a list of candidate variable terms, which partially match the search term, are automatically displayed. 

- Clicking an appropriate candidate term (red arrow) will add a corresponding individual query widget to the "Area for query composition" (red box 3), where you can specify the query based on the "shhs1" table only or both tables "shhs1" and "shhs2" using checkboxes. 

- In the "Area for grouping query widgets" (red box 4), you can logically group query widgets by flipping the Boolean connectors, such as ANDs and ORs. 

- Clicking the "Query" button on the bottom right corner of the "Area for query composition" will generate the number of unique patients satisfying the composed query criteria.

![Fig02](http://femi.case.edu:3003/physiomimi-02-querybuilder.png)
**Fig02: The Query Builder interface. This shows a sample query specification for unique number of subjects in SHHS1 with Age between 45 and 60, Gender as female, Obstructive Apnea Hypopnea Index (OAHI) at 4% desat between 30 and 40.**

> While you are exploring or done with the query composition, you can also scroll down and save constructed query<sup>[Fig03]</sup>.

![Fig03](http://femi.case.edu:3003/physiomimi-03-savequery.png)
**Fig03: The Save Query Widget.**

> Clicking the "Save Query" button will lead you to the **Query Manager** page, where you can manage the saved queries<sup>[Fig04]</sup>. Clicking a name of a saved query like "Sample Query" (red box) will link to the Query Builder page with query widgets automatically displayed for the saved query<sup>[Fig02]</sup>.

<div class="panel panel-default">
  <div class="panel-body">
  <a href=":images_path://physiomimi-04-querymanager.png?inline=1">
    <img src=":images_path://physiomimi-04-querymanager.png">
  </a>
  </div>
  <div class="panel-footer">
    <h3 class="panel-title">Fig04: The Query Manager Interface.</h3>
  </div>
</div>
![Fig04](http://femi.case.edu:3003/physiomimi-04-querymanager.png)
**Fig04: The Query Manager Interface.**

### Publications related to Physio-MIMI

> Zhang GQ, Siegler T, Saxman P, Sandberg N, Mueller R, Johnson N, Hunscher D, Arabandi S.
VISAGE: A Query Interface for Clinical Research. AMIA Summits on Translational Science Proceedings 2010, pp. 76-80.

> Zhang GQ, Cui L, Teagno J, Kaebler D, Koroukian S, Xu R. Merging Ontology Navigation with Query Construction for Web-based Medicare Data Exploration. AMIA Summits on Translational Science Proceedings 2013, pp. 285-9.

> Cui L, Mueller R, Sahoo SS, Zhang GQ. Querying Complex Federated Clinical Data Using Ontological Mapping and Subsumption Reasoning. IEEE International Conference on Healthcare Informatics 2013 (ICHI 2013), pp. 351-360.


<div class="center">
  <a href="http://physiomimi.case.edu" class="btn btn-lg btn-primary">
    Learn More!
    <span class="glyphicon glyphicon-new-window"></span>
  </a>
</div>
