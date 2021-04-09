---
title: Oggetto RegisteredTask
description: Oggetto di scripting che fornisce i metodi utilizzati per eseguire immediatamente l'attività, ottenere tutte le istanze in esecuzione dell'attività, ottenere o impostare le credenziali utilizzate per registrare l'attività e le proprietà che descrivono l'attività.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- Utilità di pianificazione oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- RegisteredTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ce300375e5122a7b63266c0cd21cdddf34606b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740471"
---
# <a name="registeredtask-object"></a>Oggetto RegisteredTask

Oggetto di scripting che fornisce i metodi utilizzati per eseguire immediatamente l'attività, ottenere tutte le istanze in esecuzione dell'attività, ottenere o impostare le credenziali utilizzate per registrare l'attività e le proprietà che descrivono l'attività.

## <a name="members"></a>Membri

L'oggetto **RegisteredTask** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **RegisteredTask** dispone di questi metodi.



| Metodo                                                                | Descrizione                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**GetInstances**](registeredtask-getinstances.md)                   | Restituisce tutte le istanze dell'attività registrata attualmente in esecuzione.<br/>             |
| [**Getruntimes**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | Ottiene le ore pianificate per l'esecuzione dell'attività registrata durante un periodo di tempo specificato.<br/> |
| [**GetSecurityDescriptor**](registeredtask-getsecuritydescriptor.md) | Ottiene il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.<br/>    |
| [**Correre**](registeredtask-run.md)                                     | Esegue immediatamente l'attività registrata.<br/>                                                |
| [**RunEx**](registeredtask-runex.md)                                 | Esegue immediatamente l'attività registrata utilizzando i flag specificati e un identificatore di sessione.<br/> |
| [**SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md) | Imposta il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.<br/>    |
| [**Interrompere**](registeredtask-stop.md)                                   | Arresta immediatamente l'attività registrata.<br/>                                               |



 

### <a name="properties"></a>Proprietà

L'oggetto **RegisteredTask** dispone di queste proprietà.



| Proprietà                                                                   | Tipo di accesso           | Descrizione                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**Definizione**](registeredtask-definition.md)<br/>                 | Sola lettura<br/>  | Ottiene la definizione dell'attività.<br/>                                               |
| [**Abilitato**](registeredtask-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica se l'attività registrata è abilitata.<br/>  |
| [**LastRunTime**](registeredtask-lastruntime.md)<br/>               | Sola lettura<br/>  | Ottiene l'ora dell'ultima esecuzione dell'attività registrata.<br/>                                |
| [**LastTaskResult**](registeredtask-lasttaskresult.md)<br/>         | Sola lettura<br/>  | Ottiene i risultati restituiti l'ultima volta in cui è stata eseguita l'attività registrata.<br/> |
| [**Nome**](registeredtask-name.md)<br/>                             | Sola lettura<br/>  | Ottiene il nome dell'attività registrata.<br/>                                          |
| [**NextRunTime**](registeredtask-nextruntime.md)<br/>               | Sola lettura<br/>  | Ottiene l'ora in cui è pianificata l'esecuzione successiva dell'attività registrata.<br/>               |
| [**NumberOfMissedRuns**](registeredtask-numberofmissedruns.md)<br/> | Sola lettura<br/>  | Ottiene il numero di volte in cui l'attività registrata ha perso un'esecuzione pianificata.<br/>       |
| [**Percorso**](registeredtask-path.md)<br/>                             | Sola lettura<br/>  | Ottiene il percorso in cui è archiviata l'attività registrata.<br/>                          |
| [**State**](registeredtask-state.md)<br/>                           | Sola lettura<br/>  | Ottiene lo stato operativo dell'attività registrata.<br/>                             |
| [**XML**](registeredtask-xml.md)<br/>                               | Sola lettura<br/>  | Ottiene le informazioni di registrazione in formato XML per l'attività registrata.<br/>       |



 

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere l' [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md) e la [visualizzazione di nomi e Stati delle attività (scripting)](displaying-task-names-and-state--scripting-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





