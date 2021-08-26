---
title: Tipo semplice HexInt32Type (schema eventi)
description: Definisce un tipo esadecimale a 4 byte. | Tipo semplice HexInt32Type (schema eventi)
ms.assetid: f4b5226d-2a5e-4756-b4c5-30cfbf13568e
keywords:
- Tipo semplice HexInt32Type EventLog
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25c977bca3ecf7b883b87a535b40b44024ded2a54025bdcb1ac107254ce932fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904751"
---
# <a name="hexint32type-simple-type-event-schema"></a>Tipo semplice HexInt32Type (schema eventi)

Definisce un tipo esadecimale a 4 byte.

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il **tipo semplice HexInt32Type** è una **stringa** limitata dal modello seguente:

-   `0[xX][0-9A-Fa-f]{1,8}`

    Il valore può contenere da uno a otto caratteri esadecimali(ad esempio, 0xa o 0xac7bd361).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





