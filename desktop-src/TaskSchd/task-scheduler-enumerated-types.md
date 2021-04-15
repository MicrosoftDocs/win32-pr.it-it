---
title: Utilità di pianificazione tipi enumerati
description: Elenca le enumerazioni usate dalle API Utilità di pianificazione.
ms.assetid: 9779d32b-0142-41bb-88e2-df79a3b0c1b2
keywords:
- Utilità di pianificazione Utilità di pianificazione, riferimento, tipi enumerati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a70c4a939d176516d47f6af8bc0825b414bf1de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104517229"
---
# <a name="task-scheduler-enumerated-types"></a>Utilità di pianificazione tipi enumerati

Vengono descritti i tipi enumerati che definiscono le costanti utilizzate dalle API Utilità di pianificazione.


I tipi enumerati seguenti sono introdotti in Utilità di pianificazione 2,0.



| Enumerazione                                                                  | Descrizione                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**\_tipo di azione attività \_**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | Definisce il tipo di azioni che possono essere eseguite da un'attività.                                                             |
| [**compatibilità delle attività \_**](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | Definisce le versioni di Utilità di pianificazione o il comando AT con cui è compatibile l'attività.                      |
| [**creazione di attività \_**](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | Definisce il modo in cui il servizio di Utilità di pianificazione crea, aggiorna o Disabilita l'attività.                                   |
| [**\_flag di enumerazione delle attività \_**](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | Definisce il modo in cui il Utilità di pianificazione enumera le attività registrate.                                              |
| [**\_criteri istanze \_ attività**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | Definisce il modo in cui il Utilità di pianificazione gestisce le istanze esistenti dell'attività quando avvia una nuova istanza dell'attività. |
| [**\_tipo di accesso attività**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | Definisce la tecnica di accesso necessaria per eseguire un'attività.                                                          |
| [**\_tipo di PROCESSTOKENSID attività**](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)              | Definisce i tipi di SID di processo che possono essere utilizzati dalle attività.                                                         |
| [**\_flag esecuzione \_ attività**](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | Definisce la modalità di esecuzione di un'attività.                                                                                       |
| [**\_tipo di runlevel attività \_**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | Definisce i flag di elevazione LUA che specificano con quale livello di privilegio verrà eseguita l'attività.                         |
| [**\_tipo di \_ \_ modifica stato sessione attività \_**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | Definisce i tipi di Terminal Server modifica dello stato della sessione che è possibile usare per avviare un'attività.               |
| [**\_stato attività**](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | Definisce i diversi stati in cui può trovarsi un'attività registrata.                                                   |
| [**\_Trigger attività \_ tipo2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | Definisce il tipo di trigger che può essere utilizzato dalle attività.                                                          |



 


> [!WARNING]
> Le enumerazioni Utilità di pianificazione 1,0 sono disponibili solo nei sistemi operativi Windows 2000, Windows XP e Windows Server 2003. Sono deprecati a partire da Windows Vista e possono essere rimossi completamente in futuro. Usare invece le enumerazioni Utilità di pianificazione 2,0 elencate in precedenza.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[Riferimento Utilità di pianificazione](task-scheduler-reference.md)
</dt> </dl>

 

 




