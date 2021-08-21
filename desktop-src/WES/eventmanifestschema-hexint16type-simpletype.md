---
title: Tipo semplice UInt16Type
description: Definisce un tipo short senza segno.
ms.assetid: 2200bb14-8f38-43fd-aed3-2a6b3ac33ed5
keywords:
- EventLog di tipo semplice UInt16Type
topic_type:
- apiref
api_name:
- UInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3398b0ad92724c8b7f415bd85e8101d7c74cc6a9391e1f95349f6ef629dff0c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343725"
---
# <a name="uint16type-simple-type"></a>Tipo semplice UInt16Type

Definisce un tipo short senza segno. Il valore può essere specificato come intero a 2 byte o come valore esadecimale compreso nell'intervallo compreso tra 0 e 65.535.

``` syntax
<xs:simpleType name="UInt16Type">
    <xs:union
        memberValues="unsignedShort HexInt16Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





