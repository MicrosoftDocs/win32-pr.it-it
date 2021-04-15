---
title: Oggetto TaskFolder
description: Oggetto di scripting che fornisce i metodi utilizzati per registrare (creare) attività nella cartella, rimuovere attività dalla cartella e creare o rimuovere sottocartelle dalla cartella.
ms.assetid: f6fd09ec-2777-4903-83b5-e3ac1aa472a0
keywords:
- Utilità di pianificazione oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- TaskFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ccad9331cf3df12ea5752fdd7e5ac94bfbeba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518598"
---
# <a name="taskfolder-object"></a>Oggetto TaskFolder

Oggetto di scripting che fornisce i metodi utilizzati per registrare (creare) attività nella cartella, rimuovere attività dalla cartella e creare o rimuovere sottocartelle dalla cartella.

## <a name="members"></a>Membri

L'oggetto **TaskFolder** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **TaskFolder** dispone di questi metodi.



| Metodo                                                              | Descrizione                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFolder**](taskfolder-createfolder.md)                     | Crea una cartella per le attività correlate.<br/>                                                                                                 |
| [**DeleteFolder**](taskfolder-deletefolder.md)                     | Elimina una sottocartella dalla cartella padre.<br/>                                                                                         |
| [**DeleteTask**](taskfolder-deletetask.md)                         | Elimina un'attività dalla cartella.<br/>                                                                                                     |
| [**GetFolder**](taskfolder-getfolder.md)                           | Ottiene una cartella che contiene le attività in una posizione specificata.<br/>                                                                          |
| [**GetFolders**](taskfolder-getfolders.md)                         | Ottiene tutte le sottocartelle nella cartella.<br/>                                                                                              |
| [**GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)   | Ottiene il descrittore di sicurezza per la cartella.<br/>                                                                                        |
| [**GetTask**](taskfolder-gettask.md)                               | Ottiene un'attività in una posizione specificata in una cartella.<br/>                                                                                    |
| [**GetTasks**](taskfolder-gettasks.md)                             | Ottiene tutte le attività nella cartella.<br/>                                                                                                   |
| [**L'RegisterTask**](taskfolder-registertask.md)                     | Registra (Crea) una nuova attività nella cartella usando XML per definire l'attività.<br/>                                                          |
| [**RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) | Registra (Crea) un'attività in una posizione specificata usando l'interfaccia [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) per definire un'attività.<br/> |
| [**SetSecurityDescriptor**](taskfolder-setsecuritydescriptor.md)   | Imposta il descrittore di sicurezza per la cartella.<br/>                                                                                        |



 

### <a name="properties"></a>Proprietà

L'oggetto **TaskFolder** dispone di queste proprietà.



| Proprietà                                   | Tipo di accesso          | Descrizione                                                                        |
|:-------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [**Nome**](taskfolder-name.md)<br/> | Sola lettura<br/> | Ottiene il nome utilizzato per identificare la cartella che contiene un'attività.<br/> |
| [**Percorso**](taskfolder-path.md)<br/> | Sola lettura<br/> | Ottiene il percorso in cui è archiviata la cartella.<br/>                            |



 

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md), [esempio di trigger di evento (scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [esempio di trigger giornaliero (scripting)](daily-trigger-example--scripting-.md), esempio di trigger di [registrazione (script)](registration-trigger-example--scripting-.md), esempio di [trigger settimanale (scripting)](weekly-trigger-example--scripting-.md), [esempio di trigger LOGON (scripting](logon-trigger-example--scripting-.md)), [esempio di trigger di avvio (](boot-trigger-example--scripting-.md)scripting) o [visualizzazione di nomi e Stati delle attività (script)](displaying-task-names-and-state--scripting-.md).

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
</dt> </dl>

 

 





