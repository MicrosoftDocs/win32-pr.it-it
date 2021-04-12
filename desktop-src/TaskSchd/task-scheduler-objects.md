---
title: Oggetti di scripting Utilità di pianificazione
description: Gli oggetti di scripting descritti negli argomenti seguenti forniscono l'accesso a livello di codice alle funzionalità disponibili all'interno del Utilità di pianificazione per Visual Basic e Visual Basic sviluppatori di script.
ms.assetid: 632bc9ae-b300-42ed-9d2c-f1d2d53d44fb
keywords:
- Utilità di pianificazione Utilità di pianificazione, riferimento, oggetti di scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acf9d74ae2bf586941f3b93a6c2cbb3a84836144
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104224572"
---
# <a name="task-scheduler-scripting-objects"></a>Oggetti di scripting Utilità di pianificazione

Gli oggetti di scripting descritti negli argomenti seguenti forniscono l'accesso a livello di codice alle funzionalità disponibili all'interno del Utilità di pianificazione per Visual Basic e Visual Basic sviluppatori di script.


Gli oggetti seguenti sono introdotti in Utilità di pianificazione 2,0.



| Oggetto                                                         | Descrizione                                                                                                                                                                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Azione**](action.md)                                       | Fornisce le proprietà comuni ereditate da tutti gli oggetti azione.                                                                                                                                                                              |
| [**ActionCollection**](actioncollection.md)                   | Contiene le azioni eseguite dall'attività.                                                                                                                                                                                                           |
| [**BootTrigger**](boottrigger.md)                             | Rappresenta un trigger che avvia un'attività quando viene avviato il sistema.                                                                                                                                                                                    |
| [**ComHandlerAction**](comhandleraction.md)                   | Rappresenta un'azione che attiva un gestore.                                                                                                                                                                                                            |
| [**DailyTrigger**](dailytrigger.md)                           | Rappresenta un trigger che avvia un'attività in base a una pianificazione giornaliera.                                                                                                                                                                                    |
| [**EmailAction**](emailaction.md)                             | Rappresenta un'azione che invia un messaggio di posta elettronica.                                                                                                                                                                                                     |
| [**EventTrigger**](eventtrigger.md)                           | Rappresenta un trigger che avvia un'attività quando si verifica un evento di sistema.                                                                                                                                                                                   |
| [**ExecAction**](execaction.md)                               | Rappresenta un'azione che esegue un'operazione della riga di comando.                                                                                                                                                                                          |
| [**IdleSettings**](idlesettings.md)                           | Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in una condizione di inattività.                                                                                                                                                            |
| [**IdleTrigger**](idletrigger.md)                             | Rappresenta un trigger che avvia un'attività quando si verifica una condizione di inattività.                                                                                                                                                                                |
| [**LogonTrigger**](logontrigger.md)                           | Rappresenta un trigger che avvia un'attività quando un utente esegue l'accesso.                                                                                                                                                                                          |
| [**MonthlyDOWTrigger**](monthlydowtrigger.md)                 | Rappresenta un trigger che avvia un'attività in base a una pianificazione mensile del giorno della settimana.                                                                                                                                                                            |
| [**MonthlyTrigger**](monthlytrigger.md)                       | Rappresenta un trigger che avvia un'attività in base a una pianificazione mensile.                                                                                                                                                                                  |
| [**NetworkSettings**](networksettings.md)                     | Fornisce le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.                                                                                                                                                               |
| [**Principale**](principal.md)                                 | Fornisce le credenziali di sicurezza per un'entità.                                                                                                                                                                                                    |
| [**RegisteredTask**](registeredtask.md)                       | Fornisce i metodi utilizzati per eseguire immediatamente l'attività, ottenere tutte le istanze in esecuzione dell'attività, ottenere o impostare le credenziali utilizzate per registrare l'attività e le proprietà che descrivono l'attività.                                      |
| [**RegisteredTaskCollection**](registeredtaskcollection.md)   | Contiene tutte le attività registrate.                                                                                                                                                                                                           |
| [**RegistrationInfo**](registrationinfo.md)                   | Fornisce le informazioni amministrative che possono essere utilizzate per descrivere l'attività. Queste informazioni includono dettagli quali una descrizione dell'attività, l'autore dell'attività, la data di registrazione dell'attività e il descrittore di sicurezza dell'attività. |
| [**RegistrationTrigger**](registrationtrigger.md)             | Rappresenta un trigger che avvia un'attività quando l'attività è registrata.                                                                                                                                                                                  |
| [**RepetitionPattern**](repetitionpattern.md)                 | Definisce la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.                                                                                                                                          |
| [**RunningTask**](runningtask.md)                             | Fornisce i metodi per ottenere informazioni da e controllare un'attività in esecuzione.                                                                                                                                                                              |
| [**RunningTaskCollection**](runningtaskcollection.md)         | Utilizzato per recuperare un'attività in esecuzione.                                                                                                                                                                                                                      |
| [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) | Consente di attivare le attività per la connessione o la disconnessione della console, la connessione remota o la disconnessione o le notifiche di blocco o sblocco della workstation.                                                                                                                   |
| [**ShowMessageAction**](showmessageaction.md)                 | Rappresenta un'azione che visualizza una finestra di messaggio quando un'attività viene attivata.                                                                                                                                                                               |
| [**TaskDefinition**](taskdefinition.md)                       | Definisce tutti i componenti di un'attività, ad esempio le impostazioni di attività, i trigger, le azioni e le informazioni di registrazione.                                                                                                                                     |
| [**TaskFolder**](taskfolder.md)                               | Fornisce i metodi utilizzati per registrare (creare) attività nella cartella, rimuovere attività dalla cartella e creare o rimuovere sottocartelle dalla cartella.                                                                                           |
| [**TaskFolderCollection**](taskfoldercollection.md)           | Conta il numero di cartelle nella raccolta e recuperare una cartella specificata dalla raccolta.                                                                                                                                                   |
| [**TaskNamedValuePair**](tasknamedvaluepair.md)               | Crea una coppia nome-valore in cui il nome è associato al valore.                                                                                                                                                                             |
| [**TaskNamedValueCollection**](tasknamedvaluecollection.md)   | Contiene una raccolta di coppie nome-valore dell'oggetto [**TaskNamedValuePair**](tasknamedvaluepair.md) .                                                                                                                                                    |
| [**TaskService**](taskservice.md)                             | Consente di accedere al servizio Utilità di pianificazione per la gestione delle attività registrate.                                                                                                                                                                          |
| [**TaskSettings**](tasksettings.md)                           | Fornisce le impostazioni utilizzate dai servizi Utilità di pianificazione per eseguire l'attività.                                                                                                                                                                      |
| [**TaskVariables**](taskvariables.md)                         | Definisce le variabili di attività che possono essere passate come parametri ai gestori attività e ai file eseguibili esterni avviate dalle attività.                                                                                                                         |
| [**TimeTrigger**](timetrigger.md)                             | Rappresenta un trigger che avvia un'attività quando viene attivato il trigger.                                                                                                                                                                                |
| [**Trigger**](trigger.md)                                     | Fornisce le proprietà comuni ereditate da tutti gli oggetti trigger.                                                                                                                                                                             |
| [**TriggerCollection**](triggercollection.md)                 | Utilizzato per aggiungere, rimuovere e recuperare i trigger di un'attività.                                                                                                                                                                                     |
| [**WeeklyTrigger**](weeklytrigger.md)                         | Rappresenta un trigger che avvia un'attività in base a una pianificazione settimanale.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento Utilità di pianificazione](task-scheduler-reference.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 




