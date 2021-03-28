---
description: L' <searchConnectorDescription> elemento è l'elemento contenitore di primo livello di una definizione del connettore di ricerca.
ms.assetid: 383CAA20-56CA-4bdc-AC79-E57A1D59785C
title: Elemento searchConnectorDescription (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa6c213d43a648ebea51b58b4c3103a0ee42f13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980471"
---
# <a name="searchconnectordescription-element-library-schema"></a><span data-ttu-id="14dfc-103">Elemento searchConnectorDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="14dfc-103">searchConnectorDescription Element (Library Schema)</span></span>

<span data-ttu-id="14dfc-104">L' <searchConnectorDescription> elemento è l'elemento contenitore di primo livello di una definizione del connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="14dfc-104">The <searchConnectorDescription> element is the top level container element of a search connector definition.</span></span> <span data-ttu-id="14dfc-105">L' <searchConnectorDescription> elemento è un'estensione del <searchConnectorDescriptionType> tipo di elemento associato ai connettori di ricerca federata di Windows; tuttavia, non è possibile includere i connettori di ricerca per la ricerca federata di Windows o i gestori di protocollo in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="14dfc-105">The <searchConnectorDescription> element is an extension of the <searchConnectorDescriptionType> element type associated with Windows Federated Search connectors; however, you cannot include search connectors for Windows Federated Search or protocol handlers in a library.</span></span>

## <a name="syntax"></a><span data-ttu-id="14dfc-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14dfc-106">Syntax</span></span>

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

## <a name="element-information"></a><span data-ttu-id="14dfc-107">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="14dfc-107">Element Information</span></span>

<span data-ttu-id="14dfc-108">Vedere la documentazione dello schema in [Windows Search](/previous-versions/bb268030(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="14dfc-108">Refer to the schema documentation in [Windows Search](/previous-versions/bb268030(v=msdn.10))</span></span>



| <span data-ttu-id="14dfc-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="14dfc-109">Parent Element</span></span>                                                                                               | <span data-ttu-id="14dfc-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="14dfc-110">Child Elements</span></span>                        |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [<span data-ttu-id="14dfc-111">Elemento searchConnectorDescriptionList (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="14dfc-111">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md) | <span data-ttu-id="14dfc-112"><isSearchOnlyI. tem></span><span class="sxs-lookup"><span data-stu-id="14dfc-112"><isSearchOnlyI.tem></span></span>             |
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



 

## <a name="attributes"></a><span data-ttu-id="14dfc-113">Attributi</span><span class="sxs-lookup"><span data-stu-id="14dfc-113">Attributes</span></span>



| <span data-ttu-id="14dfc-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="14dfc-114">Attribute</span></span> | <span data-ttu-id="14dfc-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14dfc-115">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="14dfc-116">publisher</span><span class="sxs-lookup"><span data-stu-id="14dfc-116">publisher</span></span> | <span data-ttu-id="14dfc-117">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="14dfc-117">Optional.</span></span> <span data-ttu-id="14dfc-118">Nome visualizzato del server di pubblicazione che fornisce il connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="14dfc-118">The display name of the publisher providing the search connector.</span></span>      |
| <span data-ttu-id="14dfc-119">product</span><span class="sxs-lookup"><span data-stu-id="14dfc-119">product</span></span>   | <span data-ttu-id="14dfc-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="14dfc-120">Optional.</span></span> <span data-ttu-id="14dfc-121">Nome visualizzato del prodotto a cui si applica il connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="14dfc-121">The display name of the product to which the search connector applies.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="14dfc-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="14dfc-122">Remarks</span></span>

<span data-ttu-id="14dfc-123">L' <searchConnectorDescription> elemento di una libreria utilizza la stessa definizione dello schema di <searchConnectorDescription> per la ricerca federata di Windows.</span><span class="sxs-lookup"><span data-stu-id="14dfc-123">The <searchConnectorDescription> element of a library uses the same schema definition as the <searchConnectorDescription> for Windows Federated Search.</span></span> <span data-ttu-id="14dfc-124">Sebbene usino gli stessi schemi, i connettori di ricerca per la ricerca federata di Windows non possono essere inclusi in una libreria.</span><span class="sxs-lookup"><span data-stu-id="14dfc-124">Although they use the same schemas, search connectors for Windows Federated search cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14dfc-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14dfc-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14dfc-126">Schema Descrizione libreria</span><span class="sxs-lookup"><span data-stu-id="14dfc-126">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="14dfc-127">Cerca nello schema di descrizione del connettore</span><span class="sxs-lookup"><span data-stu-id="14dfc-127">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
