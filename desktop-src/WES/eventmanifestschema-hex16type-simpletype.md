---
title: Tipo semplice HexInt16Type
description: Definisce un tipo esadecimale a 2 byte.
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- EventLog di tipo semplice HexInt16Type
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5f441071daa84f162a1dacbd16513fe2550b99d34d24ed90205ff4d8d184493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055960"
---
# <a name="hexint16type-simple-type"></a>Tipo semplice HexInt16Type

Definisce un tipo esadecimale a 2 byte.

``` syntax
<xs:simpleType name="HexInt16Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,4}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il **tipo semplice HexInt16Type** è una **stringa** limitata dal modello seguente:

-   `0[xX][0-9A-Fa-f]{1,4}`

    Il valore può contenere da uno a quattro caratteri esadecimali(ad esempio, 0xa o 0xac7b).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





