---
title: Tipo semplice UInt8Type
description: Definisce un tipo di byte senza segno.
ms.assetid: bda12d06-683f-4183-a84b-2bc3159c4eff
keywords:
- EventLog di tipo semplice UInt8Type
topic_type:
- apiref
api_name:
- UInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a48c21e34edecbf4dfb4f9c2e87c85a77e3f500ec42b8607f1de004e7679ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511311"
---
# <a name="uint8type-simple-type"></a>Tipo semplice UInt8Type

Definisce un tipo di byte senza segno. Il valore può essere specificato come intero a 1 byte o valore esadecimale compreso nell'intervallo compreso tra 0 e 255.

``` syntax
<xs:simpleType name="UInt8Type">
    <xs:union
        memberValues="unsignedByte HexInt8Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





