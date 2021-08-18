---
description: Novità per Windows 7. Elemento Container per elementi relatedProperty.
ms.assetid: F8BAAE5C-A7EA-487a-B829-91A27E24B58D
title: relatedPropertyInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 203c6e0e65943e90c6106f5e49e1792e6b47345a930f5368bd22df3a1c03885d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970960"
---
# <a name="relatedpropertyinfo"></a>relatedPropertyInfo

Novità per Windows 7. Elemento Container per [elementi relatedProperty.](./propdesc-schema-relatedproperty.md) Deve essere presente un solo [elemento relatedPropertyInfo]() per ogni [elemento propertyDescription.](./propdesc-schema-propertydescription.md)

## <a name="syntax"></a>Sintassi


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedPropertyInfo">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
                    <xs:attribute name="propertyName" type="canonical-name" use="required"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:unique name="No_two_relatedProperties_can_have_the_same_relationship_name">
        <xs:selector xpath="s:relatedProperty"/>
        <xs:field    xpath="@relationshipName"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                   | Elementi figlio                                           |
|------------------------------------------------------------------|----------------------------------------------------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | [relatedProperty](./propdesc-schema-relatedproperty.md) |



 

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

 

 
