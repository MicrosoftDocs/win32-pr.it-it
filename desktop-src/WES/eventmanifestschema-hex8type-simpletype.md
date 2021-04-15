---
title: Tipo semplice HexInt8Type
description: Definisce un tipo esadecimale a 1 byte.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- Log eventi di tipo semplice HexInt8Type
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68e56340ee535531fb6711dcf01a72d92665cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479204"
---
# <a name="hexint8type-simple-type"></a>Tipo semplice HexInt8Type

Definisce un tipo esadecimale a 1 byte.

``` syntax
<xs:simpleType name="HexInt8Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,2}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il tipo semplice **HexInt8Type** è una [stringa](/dotnet/api/system.string) limitata dal modello seguente:

-   `0[xX][0-9A-Fa-f]{1,2}`

    Il valore può contenere da uno a due caratteri esadecimali, ad esempio 0xA o 0xAC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

