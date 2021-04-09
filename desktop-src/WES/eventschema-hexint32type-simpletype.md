---
title: Tipo semplice HexInt32Type (schema di eventi)
description: Definisce un tipo esadecimale a 4 byte. | Tipo semplice HexInt32Type (schema di eventi)
ms.assetid: f4b5226d-2a5e-4756-b4c5-30cfbf13568e
keywords:
- Log eventi di tipo semplice HexInt32Type
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c9bd7a11d0e648cc451ec837f0f8711ca334d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969124"
---
# <a name="hexint32type-simple-type-event-schema"></a>Tipo semplice HexInt32Type (schema di eventi)

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

Il tipo semplice **HexInt32Type** è una **stringa** limitata dal modello seguente:

-   `0[xX][0-9A-Fa-f]{1,8}`

    Il valore può contenere da uno a otto caratteri esadecimali, ad esempio 0xA o 0xac7bd361.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





