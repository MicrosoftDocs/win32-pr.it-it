---
title: Elemento count (restartType)
description: Specifica il numero di volte in cui il Utilità di pianificazione tenterà di riavviare l'attività.
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- Conteggio Utilità di pianificazione elementi
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475970"
---
# <a name="count-restarttype-element"></a>Elemento count (restartType)

Specifica il numero di volte in cui il Utilità di pianificazione tenterà di riavviare l'attività.

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento è definito dal tipo complesso [**restartType**](taskschedulerschema-restarttype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                               | Derivato da                                                       | Descrizione                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md) | [**restartType**](taskschedulerschema-restarttype-complextype.md) | Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se l'attività non riesce per qualsiasi motivo.<br/> |



## <a name="remarks"></a>Commenti

Se questo elemento viene specificato, è necessario specificare anche l'elemento [**Interval**](taskschedulerschema-interval-restarttype-element.md) per indicare al utilità di pianificazione per quanto tempo provare a riavviare l'attività.

Per lo sviluppo in C++, vedere [**la proprietà RestartCount di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).

Per lo sviluppo di script, vedere [**TaskSettings. RestartCount**](tasksettings-restartcount.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





