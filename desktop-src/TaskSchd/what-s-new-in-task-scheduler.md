---
title: Novità di Utilità di pianificazione
description: Elenco di nuove funzionalità introdotte da diverse versioni di Utilità di pianificazione.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Utilità di pianificazione Utilità di pianificazione, novità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5245ab4e681af937924cfbd217095009d80d6a11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305343"
---
# <a name="whats-new-in-task-scheduler"></a>Novità di Utilità di pianificazione

Le modifiche seguenti riepilogano le novità di versioni diverse di Utilità di pianificazione.

## <a name="windows-10-and-windows-server-2016"></a>Windows 10 (e Windows Server 2016)

Le modifiche Utilità di pianificazione seguenti sono state introdotte in Windows 10.

-   Quando lo screen saver batteria è acceso, le attività di Windows Utilità di pianificazione vengono attivate solo se l'attività è:

    -   Non impostato per **avviare l'attività solo se il computer è inattivo... (l'** attività non usa [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))
    -   Non impostato per l'esecuzione durante la manutenzione automatica (l'attività non usa [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))
    -   È impostato per l' **esecuzione solo quando l'utente è connesso** (l'attività [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) è un **\_ \_ \_ token interattivo di accesso attività** o un **\_ \_ gruppo di accesso attività**)

    Tutti gli altri trigger vengono posticipati fino a quando il risparmio di batteria non è disattivato. Per ulteriori informazioni sull'accesso allo stato di batteria saver nell'applicazione, vedere [**\_ \_ stato di alimentazione del sistema**](/windows/desktop/api/winbase/ns-winbase-system_power_status). Per informazioni generali sul risparmio di batteria, vedere [batteria saver (nelle linee guida del componente hardware)](/windows-hardware/design/component-guidelines/battery-saver).

-   Per motivi di sicurezza, un utente non amministratore non può visualizzare né gestire un'attività Utilità di pianificazione di Windows creata da un altro utente.

## <a name="windows-8"></a>Windows 8

In Windows 8 sono state introdotte le seguenti Utilità di pianificazione 2,0 modifiche:

-   Supporto di PowerShell: gli utenti possono gestire (creare, eliminare, modificare, avviare, arrestare e così via in modo esplicito) Windows Utilità di pianificazione le attività usando il modulo ScheduledTasks di PowerShell.
-   Password gestite: gli amministratori possono usare gli account Active Directory password gestite come entità attività. Queste attività non richiedono più un criterio di reimpostazione della password applicato.
-   API changes (modifiche API): introduce due nuove impostazioni attività con l'interfaccia [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) .
    -   [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): le attività che usano queste impostazioni vengono considerate come un nuovo tipo di attività pianificate che vengono richiamate durante il periodo di manutenzione automatico del sistema operativo, in base alla periodicità e alla scadenza specificate.
    -   [**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): le attività impostate per essere volatili sono sempre disabilitate in un avvio del sistema operativo e devono essere riabilitate in modo esplicito quando necessario. Le attività volatili sono utilizzate dai cluster di failover per garantire che sia pianificata una sola istanza di attività in un cluster alla volta.
-   Il motore di pianificazione unificato supporta ora le funzionalità seguenti:
    -   Tipo di accesso S4U, tramite l'elemento [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .
    -   Valori di query XPath per i trigger di evento, tramite l'elemento [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) .
    -   Non consentire la terminazione dell'attività, tramite l'elemento [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) .
-   Funzionalità deprecate in questa versione
    -   Azione: [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (è possibile usare [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) con il cmdlet [Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) di [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)come soluzione alternativa).
    -   Azione: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).
    -   AT.exe utilità cmdline

## <a name="windows-7"></a>Windows 7

In Windows 7 sono state introdotte le modifiche seguenti Utilità di pianificazione 2,0:

-   Utilizzando il motore di pianificazione unificato fornito dal sistema operativo sottostante.
-   Possibilità di rifiutare l'avvio delle attività nelle sessioni remote (RAIL) delle applicazioni remote.
-   Protezione avanzata delle attività (solo per le attività in esecuzione come "servizio di rete" o "servizio locale"):

    -   Possibilità di assegnare un tipo di ID di sicurezza (SID) del token di processo (ad esempio, Unrestricted o None) a un'attività.
    -   Consentire agli sviluppatori di attività di richiedere il set esatto di privilegi richiesti dall'attività.

-   Modifiche API:

    -   Supporto per la protezione avanzata delle attività: la nuova funzionalità di protezione avanzata delle attività è stata introdotta con la nuova interfaccia IPrincipal2.
    -   In sono state introdotte due nuove impostazioni attività con la nuova interfaccia ITaskSettings2.

        -   DisallowStartOnRemoteAppSession: la nuova impostazione DisallowStartOnRemoteAppSession può rifiutare l'avvio di un'attività se attivata nelle sessioni [remote (Rail) integrate delle applicazioni](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) .
        -   UseUnifiedSchedulingEngine: l'uso dell'impostazione UseUnifiedSchedulingEngine fornisce un comportamento coeso per le attività e i servizi di Windows perché viene gestito in modo uniforme da un motore di pianificazione comune a livello di sistema. Sebbene sia consigliabile utilizzare un motore unificato, non supporta alcune delle funzionalità Utilità di pianificazione. Se la combinazione di proprietà non consentirà l'esecuzione dell'attività in un motore unificato, la registrazione di tale oggetto verrà rifiutata.
        -   Le funzionalità delle attività che non sono supportate dal motore di pianificazione unificato includono:

            -   Tipi di accesso:

                -   [\_ \_ \_ \_ password o token interattivo di accesso all'attività \_](./taskschedulerschema-logontype-principaltype-element.md)

            -   Criteri per più istanze:

                -   [**\_ \_ arresto esistente delle istanze dell'attività \_**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   Azioni:

                -   [Inviare e-mail](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [Visualizzare il messaggio](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   Impostazioni:

                -   [Impostazioni di rete delle attività](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [Non consentire la terminazione dell'attività](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   Trigger:

                -   [Limite tempo di esecuzione del trigger](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [Modelli di ripetizione per i trigger di calendario]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [Valori di query XPath per i trigger di evento]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   Tipi [di trigger giornalieri](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) e mensili [mensili](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md)

## <a name="windows-vista"></a>Windows Vista

Per lo sviluppo di applicazioni che utilizzano il servizio Utilità di pianificazione in Windows Vista, è necessario utilizzare l'API Utilità di pianificazione 2,0. Per ulteriori informazioni, vedere [utilità di pianificazione riferimento](task-scheduler-reference.md) e [utilizzo del utilità di pianificazione](using-the-task-scheduler.md).

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a>Windows 2000, Windows XP e Windows Server 2003

L'API Utilità di pianificazione 2,0 non è disponibile. Usare Utilità di pianificazione 1,0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[Informazioni sul Utilità di pianificazione](about-the-task-scheduler.md)
</dt> </dl>

 

 
