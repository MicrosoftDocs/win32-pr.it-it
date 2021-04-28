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
ms.openlocfilehash: 32f8a4bbf00f569ba98dfc031f62717b1afc8734
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114579"
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
| Client minimo supportato<br/> | Solo app desktop di Windows \[ Vista\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



 

 




