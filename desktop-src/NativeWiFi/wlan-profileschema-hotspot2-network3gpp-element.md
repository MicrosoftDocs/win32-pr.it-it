---
description: Elenco di ID PLMN (Public Land Mobile Network).
ms.assetid: 2e5e23c0-e98f-48f8-97b8-c5f88c80c51e
title: Elemento Network3GPP (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network3GPP
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7e19a7ccbc1579eb02ed47da82afe1eeaf8fed53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308884"
---
# <a name="network3gpp-hotspot2-element"></a>Elemento Network3GPP (Hotspot2)

Elenco di ID PLMN (Public Land Mobile Network).

``` syntax
<xs:element name="Network3GPP"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="PLMNID"
                minOccurs="0"
                maxOccurs="256"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="5"
                         />
                        <xs:maxLength
                            value="6"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L'elemento è definito dall'elemento [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento | Tipo | Descrizione                                                                                                             |
|---------|------|-------------------------------------------------------------------------------------------------------------------------|
| PLMNID  |      | ID singolo PLMN. Si tratta di un numero decimale di 5 o 6 cifre corrispondente a MCC/multiparte di una rete 3GPP.<br/> |



 

 




