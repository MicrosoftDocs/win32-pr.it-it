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
ms.openlocfilehash: 2d2392f2240ca9ca61525b27993e16bcab979a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312121"
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

Il tipo semplice **HexInt32Type** è **xs: String** limitato dal modello seguente:

-   `0[xX][0-9A-Fa-f]{1,8}`

    Il valore può contenere da uno a otto caratteri esadecimali, ad esempio 0xA o 0xac7bd361.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




