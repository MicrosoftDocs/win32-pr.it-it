---
title: Tipo semplice pathType
description: Definisce il numero minimo e massimo di caratteri per una stringa che definisce un percorso di file.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- Tipo semplice pathType Utilità di pianificazione
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 289e91b3d7139001bfab22c81bfb0f9e9871033f6296286373c5bde18fdc366d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758380"
---
# <a name="pathtype-simple-type"></a>Tipo semplice pathType

Definisce il numero minimo e massimo di caratteri per una stringa che definisce un percorso di file. Il percorso non può essere una stringa vuota e deve contenere meno di 260 caratteri.

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





