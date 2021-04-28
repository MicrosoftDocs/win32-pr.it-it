---
description: 'Elemento profileList (WLANPolicy): contiene un elenco di profili da applicare a livello di dominio o computer.'
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: Elemento profileList (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4c7478f38ba7336738325bac6872866cd570288b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109199"
---
# <a name="profilelist-wlanpolicy-element"></a>Elemento profileList (WLANPolicy)

L'elemento profileList (WLANPolicy) contiene un elenco di profili da applicare a livello di dominio o computer. Questo elemento è facoltativo. Se questo elemento è presente, deve contenere almeno un profilo.

I profili devono essere basati sullo [ \_ schema del profilo WLAN](wlan-profileschema-schema.md), con un elemento radice [**di WLANProfile**](wlan-profileschema-wlanprofile-element.md).

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**L'elemento profileList** è definito dall'elemento [**WLANPolicy.**](wlan-policyschema-wlanpolicy-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Criteri WLAN**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**Criteri WLAN**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




