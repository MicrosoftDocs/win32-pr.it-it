---
description: Definisce il tipo che contiene i valori validi per l'attributo del tipo per l'elemento Margin.
ms.assetid: 5448ead5-0249-4cc7-9f2a-d2181e2af734
title: Tipo semplice MarginTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MarginTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4e8a09e98611fabc54a029c9cac9cb37dfc1373f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233548"
---
# <a name="margintypetype-simple-type"></a>Tipo semplice MarginTypeType

Definisce il tipo che contiene i valori validi per l'attributo del **tipo** per l' [elemento Margin](margin-element.md).

``` syntax
<xs:simpleType name="MarginTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Left|Right"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il tipo semplice **MarginTypeType** è una **stringa** limitata dal modello seguente:

-   `Left|Right`

## <a name="remarks"></a>Commenti

I valori validi per l'attributo **Type** per l' [elemento Margin](margin-element.md) sono "left" e "Right".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                     |



 

 




