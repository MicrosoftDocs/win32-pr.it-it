---
title: Tipo semplice HexInt32Type (schema EventManifest)
description: Definisce un tipo esadecimale a 4 byte. | Tipo semplice HexInt32Type (schema EventManifest)
ms.assetid: b1006593-c6f2-4669-b242-758ce9977565
keywords:
- EventLog di tipo semplice HexInt32Type
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c78a101ec9854b8820b7c9170ea43f06258528de9fdc9d4b02bb41945ba3a7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248101"
---
# <a name="hexint32type-simple-type-eventmanifest-schema"></a>Tipo semplice HexInt32Type (schema EventManifest)

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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





