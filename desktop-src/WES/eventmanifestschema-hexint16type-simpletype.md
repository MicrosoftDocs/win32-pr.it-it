---
title: Tipo semplice UInt16Type
description: Definisce un tipo short senza segno.
ms.assetid: 2200bb14-8f38-43fd-aed3-2a6b3ac33ed5
keywords:
- Log eventi di tipo semplice UInt16Type
topic_type:
- apiref
api_name:
- UInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e687f42a43a12266267a0531ce078e8c6b5d1031
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743231"
---
# <a name="uint16type-simple-type"></a>Tipo semplice UInt16Type

Definisce un tipo short senza segno. Il valore può essere specificato come un Integer a 2 byte o un valore esadecimale compreso nell'intervallo compreso tra 0 e 65.535.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





