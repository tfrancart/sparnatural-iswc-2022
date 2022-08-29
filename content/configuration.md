## Ontology-driven configuration of Sparnatural
{:#configuration}

Sparnatural is configured by an OWL ontology, defining which classes and relationships are shown in the interface. The ontology defines the (multilingual) labels and tooltips, icons, or which value selection widget should be used for each predicate. The dropdown list and autocomplete widgets are also associated with a SPARQL query that populates the list or the autocomplete suggestions.

A key aspect of that configuration ontology is that it does not need to be the same as the ontology of the underlying knowledge graph. Classes or properties can be removed to show only part of the graph; they can be labelled differently, and documented with user-oriented tooltips; shortcuts can be proposed: a single predicate in the search interface can correspond to a property path in the underlying graph structure, traversing multiple entities; classes presented to users can be subsets of the (in general relatively abstract) classes of the underlying graph ontology.

The mapping to the underlying graph ontology is done through the use of an annotation (`sparnatural-config:sparqlString`) enabling to replace the corresponding class or property identifier in the SPARQL query by another string. The final SPARQL query generation is done in two steps: first, a SPARQL query based on the search interface ontology is built, and then identifiers in it are replaced by their mapping to the graph structure.

The decoupling of the search ontology from the graph structure enables to show the same graph in different ways to different categories of users. The configuration ontologies can also be shared, such as the [generic configuration for the ANF demonstrator](cite:cites sparnatural-anf-config-A), or the [BNF demonstrator](cite:cites sparnatural-bnf-config).


