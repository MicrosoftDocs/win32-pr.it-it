---
title: Tipo semplice CountType
description: Definisce un tipo di conteggio utilizzato per specificare il numero di elementi in una matrice.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- Tipo semplice CountType EventLog
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63476d70a9bb5b336449a65707664c05c56a20b4c2c9fa4888c0c3125f129d90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863621"
---
# <a name="counttype-simple-type"></a>Tipo semplice CountType

Definisce un tipo di conteggio utilizzato per specificare il numero di elementi in una matrice. Il valore può essere specificato come valore xs:unsignedShort o come stringa che fa riferimento al nome del nodo dell'elemento di dati che contiene il valore short non impostato.

``` syntax
<xs:simpleType name="CountType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





