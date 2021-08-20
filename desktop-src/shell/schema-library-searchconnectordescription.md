---
description: <searchConnectorDescription>L'elemento è l'elemento contenitore di primo livello di una definizione del connettore di ricerca.
ms.assetid: 383CAA20-56CA-4bdc-AC79-E57A1D59785C
title: Elemento searchConnectorDescription (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91be0345ae2770e28437f13cdc754a1855f050210b85a03a4eb5c6c3726af98b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858250"
---
# <a name="searchconnectordescription-element-library-schema"></a>Elemento searchConnectorDescription (schema della libreria)

<searchConnectorDescription>L'elemento è l'elemento contenitore di primo livello di una definizione del connettore di ricerca. L'elemento è un'estensione del tipo di elemento associato ai connettori di ricerca federata Windows. Tuttavia, non è possibile includere connettori di ricerca per Windows Ricerca federata o gestori di protocollo in una <searchConnectorDescription> <searchConnectorDescriptionType> libreria.

## <a name="syntax"></a>Sintassi

``` syntax
<!-- searchConnectorDescription -->
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

Vedere la documentazione dello schema in [Windows Ricerca](/previous-versions/bb268030(v=msdn.10))



| Elemento padre                                                                                               | Elementi figlio                        |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [Elemento searchConnectorDescriptionList (schema di libreria)](schema-library-searchconnectordescriptionlist.md) | <isSearchOnlyI.tem>             |
|                                                                                                              | <description>                   |
|                                                                                                              | <iconReference>                 |
|                                                                                                              | <imageLink>                     |
|                                                                                                              | <author>                        |
|                                                                                                              | <dateCreated>                   |
|                                                                                                              | <templateInfo>                  |
|                                                                                                              | <locationProvider>              |
|                                                                                                              | <scope>                         |
|                                                                                                              | <propertyStore>                 |
|                                                                                                              | <domain>                        |
|                                                                                                              | <supportsAdvancedQuerySyntax>   |
|                                                                                                              | <isDefaultSaveLocation>         |
|                                                                                                              | <isDefaultNonOwnerSaveLocation> |
|                                                                                                              | <isIndexed>                     |
|                                                                                                              | <simpleLocation>                |
|                                                                                                              | <includeInStartMenu>            |



 

## <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                      |
|-----------|----------------------------------------------------------------------------------|
| publisher | facoltativo. Nome visualizzato del server di pubblicazione che fornisce il connettore di ricerca.      |
| product   | facoltativo. Nome visualizzato del prodotto a cui si applica il connettore di ricerca. |



 

## <a name="remarks"></a>Commenti

L'elemento di una libreria usa la stessa definizione dello schema di <searchConnectorDescription> <searchConnectorDescription> per Windows ricerca federata. Anche se usano gli stessi schemi, i connettori di Windows ricerca federata non possono essere inclusi in una libreria.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Schema di descrizione della libreria](library-schema-entry.md)
</dt> <dt>

[Schema di descrizione del connettore di ricerca](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
