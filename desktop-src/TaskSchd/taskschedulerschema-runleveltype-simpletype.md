---
title: Tipo semplice runLevelType
description: Definisce i valori possibili per l'elemento RunLevel (principalType).
ms.assetid: d6b73dc5-97ac-4f94-99c1-c241a25cc252
keywords:
- Utilità di pianificazione di tipo semplice runLevelType
topic_type:
- apiref
api_name:
- runLevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d037dceeb3e6e4957cc96a17a2ac511a03a94b94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302220"
---
# <a name="runleveltype-simple-type"></a>Tipo semplice runLevelType

Definisce i valori possibili per l'elemento [**runlevel (PrincipalType)**](taskschedulerschema-runlevel-principaltype-element.md) .

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

Il tipo semplice **runLevelType** definisce i valori seguenti.



| Valore            | Descrizione                                               |
|------------------|-----------------------------------------------------------|
| LeastPrivilege   | Le attività vengono eseguite con i privilegi minimi (LUA).<br/> |
| HighestAvailable | Le attività vengono eseguite con i privilegi più elevati.<br/>     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





