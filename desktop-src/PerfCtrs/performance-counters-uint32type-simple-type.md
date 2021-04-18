---
description: Definisce un tipo di Unsigned Integer.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Tipo semplice UInt32Type (contatori delle prestazioni)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c32901167bcf181e5400ddb1d3b91ed7383965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312106"
---
# <a name="uint32type-simple-type-performance-counters"></a>Tipo semplice UInt32Type (contatori delle prestazioni)

Definisce un tipo di Unsigned Integer.

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Commenti

È possibile specificare il valore come valore integer a 4 byte o esadecimale nell'intervallo compreso tra 0 e 4.294.967.295.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




