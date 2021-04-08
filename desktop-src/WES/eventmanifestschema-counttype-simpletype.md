---
title: Tipo semplice CountType
description: Definisce un tipo di conteggio utilizzato per specificare il numero di elementi in una matrice.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- Log eventi di tipo semplice CountType
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f91b19df4182f5cff305de0429a308d0c5db234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743839"
---
# <a name="counttype-simple-type"></a>Tipo semplice CountType

Definisce un tipo di conteggio utilizzato per specificare il numero di elementi in una matrice. Il valore può essere specificato come valore xs: unsignedShort o come stringa che fa riferimento al nome del nodo dell'elemento dati che contiene il valore short unsiged.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





