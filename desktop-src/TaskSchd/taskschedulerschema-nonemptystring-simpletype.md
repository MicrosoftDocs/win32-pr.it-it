---
title: Tipo semplice nonEmptyStringType
description: Definisce i valori utilizzati per una stringa di testo non vuota.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- Utilità di pianificazione di tipo semplice nonEmptyString
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400749"
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

Il tipo semplice **nonEmptyString** definisce il valore seguente.



| Valore | Descrizione                                            |
|-------|--------------------------------------------------------|
| 1     | La stringa contiene almeno un carattere.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





