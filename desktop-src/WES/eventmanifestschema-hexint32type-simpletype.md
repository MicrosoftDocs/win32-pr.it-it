---
title: Tipo semplice UInt32Type (registro eventi di Windows)
description: Definisce un tipo di Unsigned Integer.
ms.assetid: 11e99c26-3be7-4fac-b3e1-97cb0428a886
keywords:
- Log eventi di tipo semplice UInt32Type
topic_type:
- apiref
api_name:
- UInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2a24326197c72b08032f5144fea1a69fbe68089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964170"
---
# <a name="uint32type-simple-type-windows-event-log"></a>Tipo semplice UInt32Type (registro eventi di Windows)

Definisce un tipo di Unsigned Integer. Il valore può essere specificato come un Integer a 4 byte o un valore esadecimale compreso nell'intervallo compreso tra 0 e 4.294.967.295.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





