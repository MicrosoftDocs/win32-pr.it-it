---
description: L' <propertyStore> elemento facoltativo specifica il percorso di un IPropertyStore basato su XML per archiviare i metadati aperti per questo connettore di ricerca. Questo elemento non ha attributi e un solo elemento figlio.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: Elemento propertyStore (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f8cda6457de764b00519a81a1134e7eecc8638
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750330"
---
# <a name="propertystore-element-search-connector-schema"></a>Elemento propertyStore (schema del connettore di ricerca)

L' <propertyStore> elemento facoltativo specifica il percorso di un IPropertyStore basato su XML per archiviare i metadati aperti per questo connettore di ricerca. Questo elemento non ha attributi e un solo elemento figlio.

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
| [Elemento searchConnectorDescriptionType (schema del connettore di ricerca)](search-schema-searchconnectordescription.md) | [Elemento Property di propertyStore (schema del connettore di ricerca)](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a>Esempio

Nell'esempio seguente viene illustrato un <propertyStore> elemento con due <property> elementi.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



