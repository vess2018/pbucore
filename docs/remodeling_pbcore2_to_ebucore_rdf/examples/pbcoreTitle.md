# Handling `pbcoreTitle`

```xml
<pbcoreDescriptionDocument>
  <pbcoreTitle titleType="Full">NOVA: Pocahontas Revealed</pbcoreTitle>
</pbcoreDescriptionDocument>
```


```xml
# EBUCore RDF-XML option 1: redefining rdf:Type

<rdf:Description about="http://example.com#12345">
  <rdf:type rdf:resource="ebucore:EditorialObject" />
  <ebucore:Title>NOVA: Pocahontas Revealed</ebucore:Title>
  <!-- titleType="Full" may be handled by dynamically changing rdf:Type -->
</rdf:Description>
```

```xml
# EBUCore RDF-XML option 1: using subproperty

<rdf:Description about="ebucore:EditorialObject">
  <!-- where ebucore:fullTitle has not yet been created -->
  <ebucore:fullTitle>NOVA: Pocahontas Revealed</ebucore:fullTitle>
</rdf:Description>
```



```xml

# PBCore sample

<pbcoreDescriptionDocument>
  <pbcoreTitle titleType="Program">
    News Local/State
  </pbcoreTitle>
  <pbcoreTitle titleType="Episode">
    Judge Orders U Of I To Release Salaita Emails
  </pbcoreTitle>
</pbcoreDescritionDocument>
```

```xml
# EBUCore RDF-XML option 3: Using subproperties that don't exist yet.

<rdf:Description about="http://example.com#12345">
  <rdf:type rdf:resource="ebucore:EditorialObject" />
  <ebucore:programTitle>News Local/State</ebucore:programTitle>
  <ebucore:episodeTitle>Judge Orders U Of I To Release Salaita Emails</ebucore:episodeTitle>
</rdf:Description>
```