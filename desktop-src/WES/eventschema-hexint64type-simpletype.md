---
title: Tipo semplice HexInt64Type (schema di eventi)
description: Definisce un tipo esadecimale a 8 byte. | Tipo semplice HexInt64Type (schema di eventi)
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
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
ms.openlocfilehash: e290c2326415664fbbae3feed9628b86452b10c6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321705"
---
# <a name="hexint64type-simple-type-event-schema"></a>Tipo semplice HexInt64Type (schema di eventi)

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

Il tipo semplice **HexInt64Type** è una **stringa** limitata dal modello seguente:

-   `0[xX][0-9A-Fa-f]{1,16}`

    Il valore può contenere da uno a sedici caratteri esadecimali, ad esempio 0xA o 0xac7bd361004fe190.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





