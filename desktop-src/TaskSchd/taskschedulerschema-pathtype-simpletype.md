---
title: Tipo semplice pathType
description: Definisce il numero minimo e massimo di caratteri per una stringa che definisce un percorso di file.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- Utilità di pianificazione di tipo semplice pathType
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302685"
---
# <a name="pathtype-simple-type"></a>Tipo semplice pathType

Definisce il numero minimo e massimo di caratteri per una stringa che definisce un percorso di file. Il percorso non può essere una stringa vuota e deve essere composto da meno di 260 caratteri.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





