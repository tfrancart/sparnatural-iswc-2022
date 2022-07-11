## Sparnatural : an intuitive visual SPARQL query builder
{:#sparnatural}

[Sparnatural](cite:cites sparnatural) provides an innovative search paradigm to explore and discover these knowledge graphs. A [presentation video](cite:cites sparnatural-video) demonstrates its features. Technically speaking, Sparnatural is a visual SPARQL query builder, written in Javascript, operating purely on the client. Its only requirement is a [CORS-enabled](cite:cites cors) SPARQL endpoint to which the queries can be sent. Sparnatural is open-source, under a LGPL license.

Sparnatural visually displays the query pattern with connectors and indentation, as in he following screenshot taken from the ANF demonstrator:

<figure id="sparnatural-query">
<img src="img/example-query.png" alt="A Sparnatural example query">
<figcaption markdown="block">
A query edited in Sparnatural : _"Archive records that have as provenance a Person who is a member of an organization of type 'Notarial Office', and that are of type 'bill of sale' or 'civil status document'"_
</figcaption>
</figure>

Each line in the query mimics the structure of an RDF triple with a subject type, a predicate, an object type and optionnaly some values. At each step, dropdown lists enable the user to directly see the available types of entities and links in the graph.

Values of a criteria can be selected with either dropdown lists, autocompleted search fields, date ranges (at either year or date precision) with calendar selection, tree selector to browse a hierarchy, boolean criteria, or plain text search criteria.

The set of columns in the result set can be controlled by activating the "eye" icon on the arrows in the query pattern that should be included as columns in the result set. The bottom part of the query editor can be opened to further control the order of columns, their names and sort options.

The interface allows rapid "trial and error" interactions, allowing the users to build their own mental representation of the structure of the graph.

Sparnatural also offers the ability to load predefined queries, enabling data publishers to propose sample queries that can be loaded in one click. This can serve as query templates that the users can modify.

While `OPTIONAL` and `FILTER NOT EXISTS` are supported, Sparnatural does not have the objective of covering 100% of SPARQL keywords; currently it does not support `UNION`, `SERVICE`, `FROM`, or Aggregate functions such as `COUNT`.

Sparnatural can be combined with the [YASGUI](cite:cites yasgui) SPARQL results display component to print the results of the generated SPARQL query.

