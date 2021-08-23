---
description: Elenco di identificatori dell'area di autenticazione NAI (Network Access Identifier).
ms.assetid: e77802ee-4017-4f04-ae71-5d6d0de8fcf3
title: Elemento NAIRealm (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAIRealm
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 084ee3ce04a560ce50c3ab0391f808bc09aed1bb90da6a34b86755b9b64ae772
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684211"
---
# <a name="nairealm-hotspot2-element"></a>Elemento NAIRealm (Hotspot2)

Elenco di identificatori dell'area di autenticazione NAI (Network Access Identifier). Le voci in questo elenco sono in genere nel formato `user@domain` . L'elenco dell'area di autenticazione NAI è il metodo preferito per identificare la maggior parte degli operatori non mobili, ad esempio mso, operatori wireline e sedi pubbliche.

``` syntax
<xs:element name="NAIRealm"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                maxOccurs="256"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="255"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L'elemento è definito [**dall'elemento Hotspot2.**](wlan-profileschema-hotspot2-element.md)

## <a name="child-elements"></a>Elementi figlio



| Elemento | Tipo | Descrizione                                                   |
|---------|------|---------------------------------------------------------------|
| name    |      | Un singolo identificatore dell'area di autenticazione. In genere nel formato `user@domain` . |



 

 



