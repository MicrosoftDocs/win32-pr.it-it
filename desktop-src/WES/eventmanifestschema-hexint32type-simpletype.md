---
title: Tipo semplice UInt32Type (registro eventi di Windows)
description: 'Tipo semplice UInt32Type (registro eventi di Windows): definisce un tipo integer senza segno.'
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- EventLog di tipo semplice UInt32Type
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 631bb3e8424db8a5d781aaa43df6096730aaa4d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090569"
---
# <a name="uint32type-simple-type-windows-event-log"></a>Tipo semplice UInt32Type (registro eventi di Windows)

Definisce un tipo integer senza segno. Il valore può essere specificato come intero a 4 byte o valore esadecimale compreso nell'intervallo compreso tra 0 e 4.294.967.295.

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="unsignedInt HexInt32Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



 

 





