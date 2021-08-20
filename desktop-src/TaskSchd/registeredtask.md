---
title: Oggetto RegisteredTask
description: Oggetto di scripting che fornisce i metodi usati per eseguire l'attività immediatamente, ottenere tutte le istanze in esecuzione dell'attività, ottenere o impostare le credenziali usate per registrare l'attività e le proprietà che descrivono l'attività.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- Oggetto RegisteredTask Utilità di pianificazione
- Oggetto RegisteredTask Utilità di pianificazione , descritto
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
ms.openlocfilehash: e90dc83c47b37343c41489ca2d7b3288f727086e769e83104b57ca5b6de13b2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681641"
---
# <a name="registeredtask-object"></a>Oggetto RegisteredTask

Oggetto di scripting che fornisce i metodi usati per eseguire l'attività immediatamente, ottenere tutte le istanze in esecuzione dell'attività, ottenere o impostare le credenziali usate per registrare l'attività e le proprietà che descrivono l'attività.

## <a name="members"></a>Membri

**L'oggetto RegisteredTask** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto RegisteredTask** dispone di questi metodi.



| Metodo                                                                | Descrizione                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**GetInstances**](registeredtask-getinstances.md)                   | Restituisce tutte le istanze dell'attività registrata attualmente in esecuzione.<br/>             |
| [**GetRunTimes**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | Ottiene gli orari in cui è pianificata l'esecuzione dell'attività registrata durante un periodo di tempo specificato.<br/> |
| [**GetSecurityDescriptor**](registeredtask-getsecuritydescriptor.md) | Ottiene il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.<br/>    |
| [**Esegui**](registeredtask-run.md)                                     | Esegue immediatamente l'attività registrata.<br/>                                                |
| [**RunEx**](registeredtask-runex.md)                                 | Esegue immediatamente l'attività registrata usando i flag specificati e un identificatore di sessione.<br/> |
| [**SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md) | Imposta il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.<br/>    |
| [**Fermare**](registeredtask-stop.md)                                   | Arresta immediatamente l'attività registrata.<br/>                                               |



 

### <a name="properties"></a>Proprietà

**L'oggetto RegisteredTask** ha queste proprietà.



| Proprietà                                                                   | Tipo di accesso           | Descrizione                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**Definizione**](registeredtask-definition.md)<br/>                 | Sola lettura<br/>  | Ottiene la definizione dell'attività.<br/>                                               |
| [**Abilitato**](registeredtask-enabled.md)<br/>                       | Lettura/Scrittura<br/> | Ottiene o imposta un valore booleano che indica se l'attività registrata è abilitata.<br/>  |
| [**LastRunTime**](registeredtask-lastruntime.md)<br/>               | Sola lettura<br/>  | Ottiene l'ora dell'ultima esecuzione dell'attività registrata.<br/>                                |
| [**LastTaskResult**](registeredtask-lasttaskresult.md)<br/>         | Sola lettura<br/>  | Ottiene i risultati restituiti all'ultima esecuzione dell'attività registrata.<br/> |
| [**Nome**](registeredtask-name.md)<br/>                             | Sola lettura<br/>  | Ottiene il nome dell'attività registrata.<br/>                                          |
| [**NextRunTime**](registeredtask-nextruntime.md)<br/>               | Sola lettura<br/>  | Ottiene l'ora della successiva esecuzione pianificata dell'attività registrata.<br/>               |
| [**NumberOfMissedRuns**](registeredtask-numberofmissedruns.md)<br/> | Sola lettura<br/>  | Ottiene il numero di volte in cui l'attività registrata ha perso un'esecuzione pianificata.<br/>       |
| [**Percorso**](registeredtask-path.md)<br/>                             | Sola lettura<br/>  | Ottiene il percorso in cui è archiviata l'attività registrata.<br/>                          |
| [**Stato**](registeredtask-state.md)<br/>                           | Sola lettura<br/>  | Ottiene lo stato operativo dell'attività registrata.<br/>                             |
| [**XML**](registeredtask-xml.md)<br/>                               | Sola lettura<br/>  | Ottiene le informazioni di registrazione in formato XML per l'attività registrata.<br/>       |



 

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questo oggetto di scripting, vedere Esempio di trigger temporale [(scripting)](time-trigger-example--scripting-.md) e Visualizzazione di nomi e stati delle attività [(scripting).](displaying-task-names-and-state--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





