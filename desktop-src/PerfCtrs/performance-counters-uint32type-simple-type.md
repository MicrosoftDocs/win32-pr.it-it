---
description: 'Tipo semplice UInt32Type (contatori delle prestazioni): definisce un tipo integer senza segno.'
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Tipo semplice UInt32Type (contatori delle prestazioni)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92eafff1be2c1dc924a7041ad45cadfca994d03d776f61a3c866d6c3c2f6f380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033381"
---
# <a name="uint32type-simple-type-performance-counters"></a>Tipo semplice UInt32Type (contatori delle prestazioni)

Definisce un tipo integer senza segno.

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Commenti

È possibile specificare il valore come intero a 4 byte o valore esadecimale compreso nell'intervallo compreso tra 0 e 4.294.967.295.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 




