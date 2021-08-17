---
title: Tipo semplice nonEmptyStringType
description: Definisce i valori utilizzati per una stringa di testo non vuota.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- Tipo semplice nonEmptyString Utilità di pianificazione
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6359240c2baba14460ab4478c31c490725646130ea2181efdcb8e92a94090d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758417"
---
# <a name="nonemptystringtype-simple-type"></a>Tipo semplice nonEmptyStringType

Definisce i valori utilizzati per una stringa di testo non vuota.

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valori di enumerazione

Il **tipo semplice nonEmptyString** definisce il valore seguente.



| Valore | Descrizione                                            |
|-------|--------------------------------------------------------|
| 1     | La stringa contiene almeno un carattere.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





