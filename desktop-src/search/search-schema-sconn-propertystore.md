---
description: L'elemento propertyStore facoltativo specifica il percorso di un IPropertyStore basato su XML per archiviare i metadati aperti &lt; &gt; per questo connettore di ricerca. Questo elemento non ha attributi e un solo elemento figlio.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: Elemento propertyStore (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c617f560e0471062064bcec8020dd5e6efa026
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886792"
---
# <a name="propertystore-element-search-connector-schema"></a>Elemento propertyStore (schema del connettore di ricerca)

L'elemento propertyStore facoltativo specifica il percorso di un IPropertyStore basato su XML per archiviare i metadati aperti &lt; &gt; per questo connettore di ricerca. Questo elemento non ha attributi e un solo elemento figlio.

## <a name="syntax"></a>Sintassi


```
<!-- propertyStore -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0">
            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                                                                   | Elementi figlio                                                                                            |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (schema del connettore di ricerca)](search-schema-searchconnectordescription.md) | [Elemento property di propertyStore (schema del connettore di ricerca)](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a>Esempio

L'esempio seguente mostra un &lt; elemento propertyStore &gt; con due &lt; elementi &gt; property.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



