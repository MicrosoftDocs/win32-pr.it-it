---
title: Tipo semplice UInt64Type (schema EventManifest)
description: Definisce un tipo long senza segno.
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- EventLog di tipo semplice UInt64Type
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 088cdead48fb62adf816b6065e211afcc994ec618db8b7e9a0597e6f72c1780e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511341"
---
# <a name="uint64type-simple-type"></a>Tipo semplice UInt64Type

Definisce un tipo long senza segno. Il valore può essere specificato come intero a 8 byte o come valore esadecimale compreso nell'intervallo compreso tra 0 e 18.446.744.073.709.551.615.

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





