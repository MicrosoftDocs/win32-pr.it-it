---
description: Definisce i tipi di rete wireless.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: Tipo semplice networkTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d0acb998c879e718a0e201418610bb0aa6db8c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317112"
---
# <a name="networktypetype-simple-type"></a>Tipo semplice networkTypeType

Il tipo semplice networkTypeType definisce i tipi di rete wireless. Esistono due tipi di reti: reti di infrastruttura (SSE) e reti ad hoc (IBSS).

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valori di enumerazione

Il tipo semplice **networkTypeType** definisce i valori seguenti.



| Valore | Descrizione |
|-------|-------------|
| IBSS  |             |
| ESS   |             |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




