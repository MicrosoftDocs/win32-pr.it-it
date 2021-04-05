---
title: Elemento data (taskType)
description: Definisce i dati aggiuntivi associati all'attività, ma in caso contrario non viene utilizzato dal servizio Utilità di pianificazione.
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- Utilità di pianificazione elemento dati
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740826"
---
# <a name="data-tasktype-element"></a>Elemento data (taskType)

Definisce i dati aggiuntivi associati all'attività, ma in caso contrario non viene utilizzato dal servizio Utilità di pianificazione.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

L'elemento **dati** è definito dal tipo complesso [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                          | Derivato da                                                 | Descrizione                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Attività**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Definisce l'attività eseguita dal servizio Utilità di pianificazione.<br/> |



## <a name="remarks"></a>Commenti

Come esempio di questo tipo di dati, il servizio Avvisi e registri di prestazioni usa questa proprietà come contenitore di archiviazione per la query del contatore delle prestazioni associata a un'attività.

Per lo sviluppo in C++, i dati di un'attività vengono specificati utilizzando la [**proprietà Data di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).

Per lo sviluppo di script, i dati di un'attività vengono specificati utilizzando la proprietà [**TaskDefinition. Data**](taskdefinition-data.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





