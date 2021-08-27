---
title: Tipo semplice runLevelType
description: Definisce i valori possibili per l'elemento RunLevel (principalType).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- RunLevelType tipo semplice Utilità di pianificazione
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ce534008ce0138293a773e4f5fa4a5270a2d4b27aad54dd062eafe286ab8ba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991071"
---
# <a name="runleveltype-simple-type"></a>Tipo semplice runLevelType

Definisce i valori possibili per [**l'elemento RunLevel (principalType).**](taskschedulerschema-runlevel-principaltype-element.md)

``` syntax
<xs:simpleType name="runLevelType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="LeastPrivilege"
         />
        <xs:enumeration
            value="HighestAvailable"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valori di enumerazione

Il **tipo semplice runLevelType** definisce i valori seguenti.



| Valore            | Descrizione                                               |
|------------------|-----------------------------------------------------------|
| LeastPrivilege   | Le attività vengono eseguite con i privilegi minimi (LUA).<br/> |
| HighestAvailable | Le attività vengono eseguite con i privilegi più elevati.<br/>     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





