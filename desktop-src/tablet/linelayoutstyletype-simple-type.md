---
description: Definisce i valori validi per l'attributo Style dell'elemento LineLayout.
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: Tipo semplice LineLayoutStyleType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2aa0a42ca2f295cdcccad05931ba651d4018ba377d8d10f09f85b82dcaaea8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031839"
---
# <a name="linelayoutstyletype-simple-type"></a>Tipo semplice LineLayoutStyleType

Definisce i valori validi per **l'attributo Style** dell'elemento [LineLayout.](linelayout-element.md)

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il **tipo semplice LineLayoutStyleType** è una stringa limitata dal modello seguente:

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a>Commenti

I valori validi per **l'attributo Style** [dell'elemento LineLayout](linelayout-element.md) sono:

-   Nessuno
-   Tinta unita
-   Trattino
-   Punto
-   DashDot
-   DashDotDot
-   Double

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



 

 




