---
title: Utilità di pianificazione Scripting Objects
description: Gli oggetti di scripting descritti negli argomenti seguenti forniscono l'accesso a livello di codice alle funzionalità disponibili all'interno del Utilità di pianificazione per gli sviluppatori di Visual Basic e Visual Basic script.
ms.assetid: 632bc9ae-b300-42ed-9d2c-f1d2d53d44fb
keywords:
- Utilità di pianificazione Utilità di pianificazione , riferimento, oggetti di scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f42eac1c9e8904933cedba54d1b51e5cc63919279de93286bfa658be1f60b11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100111"
---
# <a name="task-scheduler-scripting-objects"></a>Utilità di pianificazione Scripting Objects

Gli oggetti di scripting descritti negli argomenti seguenti forniscono l'accesso a livello di codice alle funzionalità disponibili all'interno del Utilità di pianificazione per gli sviluppatori di Visual Basic e Visual Basic script.


Gli oggetti seguenti sono stati introdotti in Utilità di pianificazione 2.0.



| Oggetto                                                         | Descrizione                                                                                                                                                                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Azione**](action.md)                                       | Fornisce le proprietà comuni ereditate da tutti gli oggetti azione.                                                                                                                                                                              |
| [**Actioncollection**](actioncollection.md)                   | Contiene le azioni eseguite dall'attività.                                                                                                                                                                                                           |
| [**BootTrigger**](boottrigger.md)                             | Rappresenta un trigger che avvia un'attività all'avvio del sistema.                                                                                                                                                                                    |
| [**ComHandlerAction**](comhandleraction.md)                   | Rappresenta un'azione che genera un gestore.                                                                                                                                                                                                            |
| [**DailyTrigger**](dailytrigger.md)                           | Rappresenta un trigger che avvia un'attività in base a una pianificazione giornaliera.                                                                                                                                                                                    |
| [**EmailAction**](emailaction.md)                             | Rappresenta un'azione che invia un messaggio di posta elettronica.                                                                                                                                                                                                     |
| [**EventTrigger**](eventtrigger.md)                           | Rappresenta un trigger che avvia un'attività quando si verifica un evento di sistema.                                                                                                                                                                                   |
| [**ExecAction**](execaction.md)                               | Rappresenta un'azione che esegue un'operazione della riga di comando.                                                                                                                                                                                          |
| [**IdleSettings**](idlesettings.md)                           | Specifica il modo in cui Utilità di pianificazione le attività quando il computer si trova in una condizione di inattività.                                                                                                                                                            |
| [**IdleTrigger**](idletrigger.md)                             | Rappresenta un trigger che avvia un'attività quando si verifica una condizione di inattività.                                                                                                                                                                                |
| [**LogonTrigger**](logontrigger.md)                           | Rappresenta un trigger che avvia un'attività quando un utente accede.                                                                                                                                                                                          |
| [**MonthlyDOWTrigger**](monthlydowtrigger.md)                 | Rappresenta un trigger che avvia un'attività in base a una pianificazione giornaliera mensile.                                                                                                                                                                            |
| [**MonthlyTrigger**](monthlytrigger.md)                       | Rappresenta un trigger che avvia un'attività in base a una pianificazione mensile.                                                                                                                                                                                  |
| [**NetworkSettings**](networksettings.md)                     | Fornisce le impostazioni utilizzate dal Utilità di pianificazione per ottenere un profilo di rete.                                                                                                                                                               |
| [**Principale**](principal.md)                                 | Fornisce le credenziali di sicurezza per un'entità.                                                                                                                                                                                                    |
| [**RegisteredTask**](registeredtask.md)                       | Fornisce i metodi usati per eseguire l'attività immediatamente, ottenere tutte le istanze in esecuzione dell'attività, ottenere o impostare le credenziali usate per registrare l'attività e le proprietà che descrivono l'attività.                                      |
| [**RegisteredTaskCollection**](registeredtaskcollection.md)   | Contiene tutte le attività registrate.                                                                                                                                                                                                           |
| [**RegistrationInfo**](registrationinfo.md)                   | Fornisce le informazioni amministrative che possono essere usate per descrivere l'attività. Queste informazioni includono dettagli quali una descrizione dell'attività, l'autore dell'attività, la data di registrazione dell'attività e il descrittore di sicurezza dell'attività. |
| [**RegistrationTrigger**](registrationtrigger.md)             | Rappresenta un trigger che avvia un'attività quando l'attività viene registrata.                                                                                                                                                                                  |
| [**Pattern di ripetizione**](repetitionpattern.md)                 | Definisce la frequenza di esecuzione dell'attività e la durata della ripetizione del criterio di ripetizione dopo l'avvio dell'attività.                                                                                                                                          |
| [**RunningTask**](runningtask.md)                             | Fornisce i metodi per ottenere informazioni da e controllare un'attività in esecuzione.                                                                                                                                                                              |
| [**RunningTaskCollection**](runningtaskcollection.md)         | Usato per recuperare un'attività in esecuzione.                                                                                                                                                                                                                      |
| [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) | Consente di attivare attività per la connessione o la disconnessione della console, la connessione remota o la disconnessione o le notifiche di blocco o sblocco della workstation.                                                                                                                   |
| [**ShowMessageAction**](showmessageaction.md)                 | Rappresenta un'azione che mostra una finestra di messaggio quando viene attivata un'attività.                                                                                                                                                                               |
| [**TaskDefinition**](taskdefinition.md)                       | Definisce tutti i componenti di un'attività, ad esempio le impostazioni dell'attività, i trigger, le azioni e le informazioni di registrazione.                                                                                                                                     |
| [**Cartella attività**](taskfolder.md)                               | Fornisce i metodi utilizzati per registrare (creare) attività nella cartella, rimuovere le attività dalla cartella e creare o rimuovere sottocartelle dalla cartella.                                                                                           |
| [**TaskFolderCollection**](taskfoldercollection.md)           | Conta il numero di cartelle nella raccolta e recupera una cartella specificata dalla raccolta.                                                                                                                                                   |
| [**TaskNamedValuePair**](tasknamedvaluepair.md)               | Crea una coppia nome-valore in cui il nome è associato al valore.                                                                                                                                                                             |
| [**TaskNamedValueCollection**](tasknamedvaluecollection.md)   | Contiene una raccolta di [**coppie nome-valore oggetto TaskNamedValuePair.**](tasknamedvaluepair.md)                                                                                                                                                    |
| [**TaskService**](taskservice.md)                             | Fornisce l'accesso al Utilità di pianificazione per la gestione delle attività registrate.                                                                                                                                                                          |
| [**TaskSettings**](tasksettings.md)                           | Fornisce le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.                                                                                                                                                                      |
| [**AttivitàVariables**](taskvariables.md)                         | Definisce le variabili di attività che possono essere passate come parametri ai gestori attività e ai file eseguibili esterni avviati dalle attività.                                                                                                                         |
| [**TimeTrigger**](timetrigger.md)                             | Rappresenta un trigger che avvia un'attività quando il trigger viene attivato.                                                                                                                                                                                |
| [**Trigger**](trigger.md)                                     | Fornisce le proprietà comuni ereditate da tutti gli oggetti trigger.                                                                                                                                                                             |
| [**Triggercollection**](triggercollection.md)                 | Usato per aggiungere, rimuovere e recuperare i trigger di un'attività.                                                                                                                                                                                     |
| [**WeeklyTrigger**](weeklytrigger.md)                         | Rappresenta un trigger che avvia un'attività in base a una pianificazione settimanale.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione riferimento](task-scheduler-reference.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 




