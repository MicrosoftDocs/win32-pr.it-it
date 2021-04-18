---
description: Contiene un elenco di profili da applicare a livello di dominio o di computer.
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: Elemento Profiler (LANPolicy)
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
ms.openlocfilehash: b85c284262c070f7a9349933f99ad858cf047913
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314760"
---
# <a name="profilelist-lanpolicy-element"></a>Elemento Profiler (LANPolicy)

L'elemento Profiler (LANPolicy) contiene un elenco di profili da applicare a livello di dominio o di computer. I profili devono essere basati sullo [ \_ schema del profilo LAN](lan-profileschema-schema.md), con un elemento radice di [**LANProfile**](lan-profileschema-lanprofile-element.md). I profili basati su qualsiasi altro schema verranno ignorati.

Quando [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) è impostato su false, questo elemento non deve essere presente in un profilo criteri LAN. Quando **enableAutoConfig** è impostato su true, questo elemento è obbligatorio.

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

L'elemento **Profiler** è definito dall'elemento [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .

## <a name="remarks"></a>Commenti

Questo elemento deve contenere esattamente un profilo di rete. Se nei criteri è specificato più di un profilo, verrà applicata solo la prima rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




