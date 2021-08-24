---
description: Definisce un tipo esadecimale a 4 byte.
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: Tipo semplice HexInt32Type (contatori delle prestazioni)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08b9ea7e483f6580e3f896a6a3f54a65e9117597538564889df8a5afb2fe795f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033481"
---
# <a name="hexint32type-simple-type-performance-counters"></a>Tipo semplice HexInt32Type (contatori delle prestazioni)

Definisce un tipo esadecimale a 4 byte.

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il **tipo semplice HexInt32Type** è **un tipo xs:string** limitato dal modello seguente:

-   `0[xX][0-9A-Fa-f]{1,8}`

    Il valore può contenere da uno a otto caratteri esadecimali(ad esempio, 0xa o 0xac7bd361).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 




