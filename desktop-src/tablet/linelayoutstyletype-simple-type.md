---
description: Definisce i valori validi per l'attributo di stile dell'elemento LineLayout.
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
ms.openlocfilehash: 67b07d9de51e16148905768d7a6f268038bb1afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318699"
---
# <a name="linelayoutstyletype-simple-type"></a>Tipo semplice LineLayoutStyleType

Definisce i valori validi per l'attributo di **stile** dell' [elemento LineLayout](linelayout-element.md).

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

Il tipo semplice **LineLayoutStyleType** è una stringa limitata dal modello seguente:

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a>Commenti

I valori validi per l'attributo di **stile** dell' [elemento LineLayout](linelayout-element.md) sono i seguenti:

-   nessuno
-   Tinta unita
-   Trattino
-   Punto
-   DashDot
-   DashDotDot
-   Double

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



 

 




