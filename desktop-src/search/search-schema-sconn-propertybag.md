---
description: "&lt;L'elemento propertyBag &gt; obbligatorio specifica un set di una o più proprietà usate da questo provider di posizione."
ms.assetid: 63f8f2e4-3b52-4d6e-8d3a-2e133aac0e86
title: Elemento propertyBag (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c186e9502c48a1fc052acf28bc8bd8063085b8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883331"
---
# <a name="propertybag-element-search-connector-schema"></a>Elemento propertyBag (schema del connettore di ricerca)

&lt;L'elemento propertyBag &gt; obbligatorio specifica un set di una o più proprietà usate da questo provider di posizione.

## <a name="syntax"></a>Sintassi


```
<!-- propertyBag -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
                            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
                        </xs:element>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                                                 | Elementi figlio                                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Elemento locationProvider (schema del connettore di ricerca)](search-schema-sconn-locationprovider.md) | [Elemento property (schema del connettore di ricerca)](search-schema-sconn-locationproviderproperty.md) |



 

## <a name="example-of-a-propertybag-element-and-property-elements"></a>Esempio di un elemento PropertyBag e di elementi property


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



