---
title: Oggetto TaskService
description: Per gli script, fornisce l'accesso al servizio Utilità di pianificazione per la gestione delle attività registrate.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- Utilità di pianificazione oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, descritto
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
ms.openlocfilehash: 762cd2445c3c6b720bba0f01ae48b787abc1fb38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478371"
---
# <a name="taskservice-object"></a>Oggetto TaskService

Per gli script, fornisce l'accesso al servizio Utilità di pianificazione per la gestione delle attività registrate.

Prima di chiamare uno degli altri metodi **TaskService** , è necessario chiamare il metodo [**TaskService. Connect**](taskservice-connect.md) .

## <a name="members"></a>Membri

L'oggetto **TaskService** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **TaskService** dispone di questi metodi.



| Metodo                                                 | Descrizione                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Connettersi**](taskservice-connect.md)                 | Si connette a un computer remoto e associa tutte le chiamate successive a questa interfaccia con una sessione remota.<br/>                                                                                                 |
| [**GetFolder**](taskservice-getfolder.md)             | Ottiene il percorso di una cartella di attività registrate.<br/>                                                                                                                                                            |
| [**GetRunningTasks**](taskservice-getrunningtasks.md) | Ottiene una raccolta di attività in esecuzione.<br/>                                                                                                                                                                       |
| [**NewTask**](taskservice-newtask.md)                 | Restituisce un oggetto definizione di attività vuoto da compilare con le impostazioni e le proprietà e quindi registrato utilizzando il metodo [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **TaskService** dispone di queste proprietà.



| Proprietà                                                          | Descrizione                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Connesso**](taskservice-connected.md)<br/>             | Ottiene un valore booleano che indica se si è connessi al servizio Utilità di pianificazione.<br/>                          |
| [**ConnectedDomain**](taskservice-connecteddomain.md)<br/> | Ottiene il nome del dominio a cui è connesso il computer [**TargetServer**](taskservice-targetserver.md) .<br/> |
| [**ConnectedUser**](taskservice-connecteduser.md)<br/>     | Ottiene il nome dell'utente connesso al servizio Utilità di pianificazione.<br/>                                       |
| HighestVersion<br/>                                         | Ottiene la versione più recente di Utilità di pianificazione supportata da un computer.<br/>                                             |
| [**TargetServer**](taskservice-targetserver.md)<br/>       | Ottiene il nome del computer in cui è in esecuzione il servizio Utilità di pianificazione a cui è connesso l'utente.<br/>          |



 

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

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





