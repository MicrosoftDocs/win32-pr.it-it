---
title: Tipo semplice HexInt64Type
description: Definisce un tipo esadecimale a 8 byte. | Tipo semplice HexInt64Type
ms.assetid: 2e81ec2b-cf67-42df-92a0-bf45b6dca051
keywords:
- Log eventi di tipo semplice HexInt64Type
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8947e594bb067140510b0b5d2046a898018a291e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104401869"
---
# <a name="hexint64type-simple-type"></a>Tipo semplice HexInt64Type

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

Il tipo semplice **HexInt64Type** è una [stringa](/dotnet/api/system.string) limitata dal modello seguente:

-   `0[xX][0-9A-Fa-f]{1,16}`

    Il valore può contenere da uno a sedici caratteri esadecimali, ad esempio 0xA o 0xac7bd361004fe190.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

