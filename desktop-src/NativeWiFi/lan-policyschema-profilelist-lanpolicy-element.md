---
description: 'Elemento profileList (LANPolicy): contiene un elenco di profili da applicare a livello di dominio o di computer.'
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: Elemento profileList (LANPolicy)
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
ms.openlocfilehash: 25582be51d3206c17076c702bb159f13b012d5964a10cc4ebd7908459447fcc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801121"
---
# <a name="profilelist-lanpolicy-element"></a>Elemento profileList (LANPolicy)

L'elemento profileList (LANPolicy) contiene un elenco di profili da applicare a livello di dominio o computer. I profili devono essere basati sullo [ \_ schema del profilo LAN](lan-profileschema-schema.md), con un elemento radice [**di LANProfile**](lan-profileschema-lanprofile-element.md). I profili basati su qualsiasi altro schema verranno ignorati.

Quando [**enableAutoConfig è**](lan-policyschema-enableautoconfig-globalflags-element.md) impostato su FALSE, questo elemento non deve essere presente in un profilo di criteri LAN. Quando **enableAutoConfig** è impostato su TRUE, questo elemento è obbligatorio.

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

**L'elemento profileList** è definito dall'elemento [**LANPolicy.**](lan-policyschema-lanpolicy-element.md)

## <a name="remarks"></a>Commenti

Questo elemento deve contenere esattamente un profilo di rete. Se nei criteri è specificato più di un profilo, verrà applicata solo la prima rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




