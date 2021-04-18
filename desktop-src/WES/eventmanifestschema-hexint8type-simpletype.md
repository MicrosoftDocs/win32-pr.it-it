---
title: Tipo semplice UInt8Type
description: Definisce un tipo di byte senza segno.
ms.assetid: bda12d06-683f-4183-a84b-2bc3159c4eff
keywords:
- Log eventi di tipo semplice UInt8Type
topic_type:
- apiref
api_name:
- UInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3236d7416cbb199037813a8ae870d4f87718081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301553"
---
# <a name="uint8type-simple-type"></a>Tipo semplice UInt8Type

Definisce un tipo di byte senza segno. Il valore può essere specificato come valore integer a 1 byte o esadecimale compreso nell'intervallo compreso tra 0 e 255.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





