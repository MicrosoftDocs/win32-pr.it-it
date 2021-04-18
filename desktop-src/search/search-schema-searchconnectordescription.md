---
description: L' <searchConnectorDescriptionType> elemento è il contenitore di livello principale per la definizione del connettore di ricerca.
ms.assetid: a6b45864-210d-4099-804d-7548fd8eb562
title: Elemento searchConnectorDescriptionType (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7edb69647567b7e18e25e11dcd0fc773d0be7902
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306071"
---
# <a name="searchconnectordescriptiontype-element-search-connector-schema"></a>Elemento searchConnectorDescriptionType (schema del connettore di ricerca)

L' <searchConnectorDescriptionType> elemento è il contenitore di livello principale per la definizione del connettore di ricerca.

-   [Sintassi](#syntax)
-   [Informazioni sull'elemento](#element-information)
-   [Attributes (Attributi)](#attributes)
-   [Osservazioni:](#remarks)
-   [Esempio di un file di descrizione del connettore di ricerca](#example-of-a-search-connector-description-file)
-   [Argomenti correlati](#related-topics)

## <a name="syntax"></a>Sintassi


```
<!-- searchConnectorDescriptionType -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
   <xs:complexType name="searchConnectorDescriptionType">
      <xs:all>
         <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
         <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/
         <xs:element name="description" type="xs:string" minOccurs="0"/>
         <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
         <xs:element name="imageLink" minOccurs="0">
            <xs:complexType>
               <xs:sequence>
                  <xs:element name="url" type="xs:anyURI"/>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="author" type="xs:string" minOccurs="0"/>
         <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
         <xs:element name="templateInfo" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="folderType" minOccurs="0"/>
               </xs:all>
            </xs:complexType>
         </xs:element>
         <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0"/>
         <xs:element name="locationProvider" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
               </xs:all>
               <xs:attribute name="clsid" use="required"/>
               <xs:attribute name="codebase" type="xs:string"/>
            </xs:complexType>
         </xs:element>
         <xs:element name="scope" minOccurs="0">
            <xs:complexType>
               <xs:sequence minOccurs="0">
                  <xs:element name="scopeItem" maxOccurs="unbounded">
                     <xs:complexType>
                        <xs:all>
                           <xs:element name="mode" default="Include">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Include"/>
                                    <xs:enumeration value="Exclude"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="depth" default="Shallow" minOccurs="0">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Shallow"/>
                                    <xs:enumeration value="Deep"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="url" type="xs:anyURI"/>
                        </xs:all>
                     </xs:complexType>
                  </xs:element>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0"/>
         <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="domain" type="xs:string" minOccurs="0"/>
         <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isIndexed" type="xs:boolean" minOccurs="0"/>
      </xs:all>
      <xs:attribute name="publisher" type="xs:string"/>
      <xs:attribute name="product" type="xs:string"/>
   </xs:complexType>
</xs:schema>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre | Elementi figlio                                                                                                           |
|----------------|--------------------------------------------------------------------------------------------------------------------------|
|                | [Elemento isSearchOnlyItem (schema del connettore di ricerca)](search-schema-sconn-issearchonlyitem.md)                           |
|                | [Elemento isDefaultSaveLocation (schema del connettore di ricerca)](search-schema-sconn-isdefaultsavelocation.md)                 |
|                | [Elemento isDefaultNonOwnerSaveLocation (schema del connettore di ricerca)](search-schema-sconn-isdefaultnonownersavelocation.md) |
|                | [Elemento Description (schema del connettore di ricerca)](search-schema-sconn-description.md)                                     |
|                | [Elemento iconReference (schema del connettore di ricerca)](search-schema-sconn-iconreference.md)                                 |
|                | [Elemento Collegamentoimmagine (schema del connettore di ricerca)](search-schema-sconn-imagelink.md)                                         |
|                | [Elemento Author (Schema connettore di ricerca)](search-schema-sconn-author.md)                                               |
|                | [Elemento dateCreated (schema del connettore di ricerca)](search-schema-sconn-datecreated.md)                                     |
|                | [Elemento templateInfo (schema del connettore di ricerca)](search-schema-sconn-templateinfo.md)                                   |
|                | [Elemento locationProvider (schema del connettore di ricerca)](search-schema-sconn-locationprovider.md)                           |
|                | [Elemento Scope (Schema connettore di ricerca)](search-schema-sconn-scope.md)                                                 |
|                | [Elemento propertyStore (schema del connettore di ricerca)](search-schema-sconn-propertystore.md)                                 |
|                | [Elemento includeInStartMenuScope (schema del connettore di ricerca)](search-schema-sconn-includeinstartmenuscope.md)             |
|                | [Elemento Domain (Schema connettore di ricerca)](search-schema-sconn-domain.md)                                               |
|                | [Elemento supportsAdvancedQuerySyntax (schema del connettore di ricerca)](search-schema-sconn-supportsadvancedquerysyntax.md)     |
|                | [Elemento SetIndex (schema del connettore di ricerca)](search-schema-sconn-isindexed.md)                                         |



 

## <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                      |
|-----------|----------------------------------------------------------------------------------|
| publisher | facoltativo. Nome visualizzato del server di pubblicazione che fornisce il connettore di ricerca.      |
| product   | facoltativo. Nome visualizzato del prodotto a cui si applica il connettore di ricerca. |



 

## <a name="remarks"></a>Commenti

Non è possibile usare i connettori di ricerca per la ricerca federata nelle librerie. Lo schema per i connettori di ricerca della libreria è un'estensione dello schema descritto qui e include informazioni specifiche per le librerie.

## <a name="example-of-a-search-connector-description-file"></a>Esempio di un file di descrizione del connettore di ricerca

Di seguito è riportato un esempio di un file di descrizione del connettore di ricerca per un servizio Web di ricerca federata.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



Di seguito è riportato un esempio di un file di descrizione del connettore di ricerca per un gestore di protocollo MAPI.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Panoramica dello schema di descrizione del connettore di ricerca](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> </dl>

 

 



