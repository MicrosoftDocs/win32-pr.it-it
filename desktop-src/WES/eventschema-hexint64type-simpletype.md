---
title: Tipo semplice HexInt64Type (schema eventi)
description: Definisce un tipo esadecimale a 8 byte. | Tipo semplice HexInt64Type (schema eventi)
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
keywords:
- EventLog di tipo semplice HexInt64Type
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fcc4e3cea12be0fecaf7cef2dcd6f9687f4aa4340f9eaca4f8a6bad10c88eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120146"
---
# <a name="hexint64type-simple-type-event-schema"></a>Tipo semplice HexInt64Type (schema eventi)

Definisce un tipo esadecimale a 8 byte.

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il **tipo semplice HexInt64Type** è una **stringa** limitata dal modello seguente:

-   `0[xX][0-9A-Fa-f]{1,16}`

    Il valore può contenere da uno a sedici caratteri esadecimali(ad esempio, 0xa o 0xac7bd361004fe190).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





