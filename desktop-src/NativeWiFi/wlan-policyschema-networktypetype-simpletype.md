---
description: Definisce i tipi di rete wireless.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: Tipo semplice networkTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 40184bb027f80826baa3ad56090755a2cd9ec630f9eb105e402d30a6ecf2661c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800111"
---
# <a name="networktypetype-simple-type"></a>Tipo semplice networkTypeType

Il tipo semplice networkTypeType definisce i tipi di rete wireless. Esistono due tipi di reti: reti di infrastruttura (ESS) e reti ad hoc (IBSS).

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valori di enumerazione

Il **tipo semplice networkTypeType** definisce i valori seguenti.



| Valore | Descrizione |
|-------|-------------|
| IBSS  |             |
| Ess   |             |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 




