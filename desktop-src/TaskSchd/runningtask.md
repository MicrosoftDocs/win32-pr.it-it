---
title: Oggetto RunningTask
description: Oggetto di scripting che fornisce i metodi per ottenere informazioni da e controllare un'attività in esecuzione.
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- Utilità di pianificazione oggetto RunningTask
- Oggetto RunningTask Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- RunningTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261be07f71d0d35f5d3140de1b39574b635a531e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518208"
---
# <a name="runningtask-object"></a>Oggetto RunningTask

Oggetto di scripting che fornisce i metodi per ottenere informazioni da e controllare un'attività in esecuzione.

## <a name="members"></a>Membri

L'oggetto **RunningTask** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **RunningTask** dispone di questi metodi.



| Metodo                                 | Descrizione                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [**Aggiorna**](runningtask-refresh.md) | Aggiorna tutte le variabili di istanza locale dell'attività.<br/> |
| [**Interrompere**](runningtask-stop.md)       | Arresta questa istanza dell'attività.<br/>                           |



 

### <a name="properties"></a>Proprietà

L'oggetto **RunningTask** dispone di queste proprietà.



| Proprietà                                                      | Tipo di accesso          | Descrizione                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**CurrentAction**](runningtask-currentaction.md)<br/> | Sola lettura<br/> | Ottiene il nome dell'azione corrente eseguita dall'attività in esecuzione.<br/> |
| [**EnginePID**](runningtask-enginepid.md)<br/>         | Sola lettura<br/> | Ottiene l'ID di processo per il motore (processo) che esegue l'attività.<br/>  |
| [**: InstanceGuid**](runningtask-instanceguid.md)<br/>   | Sola lettura<br/> | Ottiene l'identificatore GUID per questa istanza dell'attività.<br/>                  |
| [**Nome**](runningtask-name.md)<br/>                   | Sola lettura<br/> | Ottiene il nome dell'attività.<br/>                                               |
| [**Percorso**](runningtask-path.md)<br/>                   | Sola lettura<br/> | Ottiene il percorso in cui è archiviata l'attività.<br/>                               |
| [**State**](runningtask-state.md)<br/>                 | Sola lettura<br/> | Ottiene lo stato dell'attività in esecuzione. <br/>                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Utilità di pianificazione](task-scheduler-objects.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**RunningTaskCollection**](runningtaskcollection.md)
</dt> <dt>

[**RegisteredTask. Run**](registeredtask-run.md)
</dt> <dt>

[**RegisteredTask.RunEx**](registeredtask-runex.md)
</dt> </dl>

 

 





