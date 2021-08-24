---
title: Oggetto TaskService
description: Per lo scripting, fornisce l'accesso al Utilità di pianificazione per la gestione delle attività registrate.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- Oggetto TaskService Utilità di pianificazione
- Oggetto TaskService Utilità di pianificazione , descritto
topic_type:
- apiref
api_name:
- TaskService
- HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f20840a5580d0188354ca6b65ab3ce5b7402d57ea7346462d2f990ecfe34cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658651"
---
# <a name="taskservice-object"></a>Oggetto TaskService

Per lo scripting, fornisce l'accesso al Utilità di pianificazione per la gestione delle attività registrate.

Il [**metodo TaskService.Connessione**](taskservice-connect.md) deve essere chiamato prima di chiamare qualsiasi altro **metodo TaskService.**

## <a name="members"></a>Membri

**L'oggetto TaskService** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto TaskService** dispone di questi metodi.



| Metodo                                                 | Descrizione                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Connettere**](taskservice-connect.md)                 | Si connette a un computer remoto e associa tutte le chiamate successive su questa interfaccia a una sessione remota.<br/>                                                                                                 |
| [**GetFolder**](taskservice-getfolder.md)             | Ottiene il percorso di una cartella di attività registrate.<br/>                                                                                                                                                            |
| [**GetRunningTasks**](taskservice-getrunningtasks.md) | Ottiene una raccolta di attività in esecuzione.<br/>                                                                                                                                                                       |
| [**NewTask**](taskservice-newtask.md)                 | Restituisce un oggetto definizione di attività vuoto da riempire con impostazioni e proprietà e quindi registrato usando il [**metodo TaskFolder.RegisterTaskDefinition.**](taskfolder-registertaskdefinition.md)<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto TaskService** ha queste proprietà.



| Proprietà                                                          | Descrizione                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Connesso**](taskservice-connected.md)<br/>             | Ottiene un valore booleano che indica se si è connessi al Utilità di pianificazione servizio.<br/>                          |
| [**ConnectedDomain**](taskservice-connecteddomain.md)<br/> | Ottiene il nome del dominio a cui è connesso il computer [**TargetServer.**](taskservice-targetserver.md)<br/> |
| [**ConnectedUser**](taskservice-connecteduser.md)<br/>     | Ottiene il nome dell'utente connesso al Utilità di pianificazione servizio.<br/>                                       |
| HighestVersion<br/>                                         | Ottiene la versione più elevata Utilità di pianificazione supportata da un computer.<br/>                                             |
| [**TargetServer**](taskservice-targetserver.md)<br/>       | Ottiene il nome del computer che esegue il servizio Utilità di pianificazione cui l'utente è connesso.<br/>          |



 

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questo oggetto di scripting, vedere Time [Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md)o [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





