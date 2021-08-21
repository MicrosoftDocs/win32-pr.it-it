---
title: Novità di Utilità di pianificazione
description: Elenco delle nuove funzionalità introdotte dalle diverse versioni di Utilità di pianificazione.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Utilità di pianificazione Utilità di pianificazione , novità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3592cc5efd08afe4737e9af429d52fa41216b6c756a64faeaa45f6cc5c0774b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354783"
---
# <a name="whats-new-in-task-scheduler"></a>Novità di Utilità di pianificazione

Le modifiche seguenti riepilogano le novità delle diverse versioni di Utilità di pianificazione.

## <a name="windows-10-and-windows-server-2016"></a>Windows 10 (e Windows Server 2016)

Le modifiche Utilità di pianificazione seguenti sono state introdotte in Windows 10.

-   Quando risparmio batteria è attivata, Windows Utilità di pianificazione attività vengono attivate solo se l'attività è:

    -   Non impostato su **Avvia l'attività solo se il computer è inattivo(** l'attività non usa [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))
    -   Non impostato per l'esecuzione durante la manutenzione automatica (l'attività non usa [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))
    -   È impostato su **Esegui solo quando l'utente è connesso** (l'attività [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) è **TASK LOGON INTERACTIVE \_ \_ \_ TOKEN** o **TASK LOGON \_ \_ GROUP**)

    Tutti gli altri trigger vengono posticilati finché risparmio batteria è disattivata. Per altre informazioni sull'accesso risparmio batteria stato dell'applicazione, vedere [**STATO DI ALIMENTAZIONE DEL \_ \_ SISTEMA**](/windows/desktop/api/winbase/ns-winbase-system_power_status). Per informazioni generali sulle risparmio batteria, vedere [risparmio batteria (nelle linee guida per i componenti hardware).](/windows-hardware/design/component-guidelines/battery-saver)

-   Per motivi di sicurezza, un utente non amministratore non può visualizzare né gestire un'Windows Utilità di pianificazione attività creata da un altro utente.

## <a name="windows-8"></a>Windows 8

Le modifiche Utilità di pianificazione 2.0 seguenti sono state introdotte in Windows 8:

-   Supporto di PowerShell: gli utenti possono gestire (creare, eliminare, modificare, avviare, arrestare in modo esplicito e così via) Windows Utilità di pianificazione attività usando il modulo Di PowerShell ScheduledTasks.
-   Password gestite: gli amministratori possono usare gli account password gestite di Active Directory come entità attività. Queste attività non richiedono più criteri di reimpostazione della password applicati.
-   Modifiche dell'API: sono state introdotte due nuove impostazioni delle attività [**con l'interfaccia ITaskSettings3.**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3)
    -   [**MaintenanceSettings:**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings)le attività che usano queste impostazioni vengono considerate come un nuovo tipo di attività pianificate che vengono richiamate durante l'orario di manutenzione automatica del sistema operativo, in base alla periodicità e alla scadenza specificate.
    -   [**Volatile:**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile)le attività impostate come volatili vengono sempre disabilitate all'avvio di un sistema operativo e devono essere ri abilitate nuovamente in modo esplicito quando necessario. Le attività volatili vengono utilizzate dai cluster di failover per garantire che in un cluster sia pianificata una sola istanza di attività alla volta.
-   Il motore di pianificazione unificato supporta ora le funzionalità seguenti:
    -   Tipo logon S4U, tramite [**l'elemento LogonType.**](taskschedulerschema-logontype-principaltype-element.md)
    -   Valori di query XPath per i trigger di evento, tramite [**l'elemento ValueQueries.**](taskschedulerschema-valuequeries-eventtriggertype-element.md)
    -   Non consentire la terminazione rigida dell'attività tramite [**l'elemento AllowHardTerminate.**](taskschedulerschema-allowhardterminate-settingstype-element.md)
-   Funzionalità deprecate in questa versione
    -   Azione: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (è possibile usare [**IExecAction con**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) il cmdlet [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)[Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) come soluzione alternativa).
    -   Azione: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).
    -   AT.exe utilità della riga di comando

## <a name="windows-7"></a>Windows 7

Le modifiche Utilità di pianificazione 2.0 seguenti sono state introdotte in Windows 7:

-   Uso del motore di pianificazione unificato fornito dal sistema operativo sottostante.
-   Possibilità di rifiutare le attività di avvio nelle sessioni RAIL (Remote Applications Integrated Locally).
-   Protezione avanzata della sicurezza delle attività (solo per le attività in esecuzione come "NETWORK SERVICE" o "LOCAL SERVICE"):

    -   Possibilità di assegnare un tipo di ID di sicurezza (SID) del token di processo (ad esempio, senza restrizioni o nessuno) a un'attività.
    -   Consentire agli sviluppatori di attività di richiedere il set esatto di privilegi necessari per l'attività.

-   Modifiche all'API:

    -   Supporto della protezione avanzata delle attività: con la nuova interfaccia IPrincipal2 è stata introdotta la nuova funzionalità di protezione avanzata della sicurezza delle attività.
    -   Sono state introdotte due nuove impostazioni delle attività con la nuova interfaccia ITaskSettings2.

        -   DisallowStartOnRemoteAppSession: la nuova impostazione DisallowStartOnRemoteAppSession può rifiutare l'avvio di un'attività se attivata in sessioni [RAIL (Remote Applications Integrated Locally).](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546)
        -   UseUnifiedSchedulingEngine: l'uso dell'impostazione UseUnifiedSchedulingEngine offre un comportamento coerente per attività e servizi di Windows perché viene gestito in modo uniforme da un motore di pianificazione comune a livello di sistema. Anche se è consigliabile usare un motore unificato, non supporta alcune delle Utilità di pianificazione funzionalità. Se la combinazione di proprietà non consente l'esecuzione dell'attività in un motore unificato, la registrazione di tali proprietà verrà rifiutata.
        -   Le funzionalità delle attività non supportate dal motore di pianificazione unificato includono:

            -   Tipi di accesso:

                -   [TOKEN \_ INTERATTIVO DI ACCESSO ATTIVITÀ O \_ \_ \_ \_ PASSWORD](./taskschedulerschema-logontype-principaltype-element.md)

            -   Criteri per istanze multiple:

                -   [**LE ISTANZE \_ DELLE ATTIVITÀ \_ INTERROMPINO \_ L'ESECUZIONE ESISTENTE**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   Azioni:

                -   [Inviare e-mail](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [Visualizzare il messaggio](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   Impostazioni:

                -   [Impostazioni di rete delle attività](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [Non consentire la terminazione rigida dell'attività](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   Trigger:

                -   [Limite di tempo di esecuzione del trigger](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [Modelli di ripetizione per i trigger del calendario]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [Valori di query XPath per i trigger di evento]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   [Tipi di](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) trigger [giornalieri mensili e](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) mensili

## <a name="windows-vista"></a>Windows Vista

L Utilità di pianificazione aPI 2.0 deve essere usata nello sviluppo di applicazioni che usano il servizio Utilità di pianificazione in Windows Vista. Per altre informazioni, vedere [Utilità di pianificazione e](task-scheduler-reference.md) [Using the Utilità di pianificazione](using-the-task-scheduler.md).

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a>Windows 2000, Windows XP e Windows Server 2003

L Utilità di pianificazione API 2.0 non è disponibile. Usare Utilità di pianificazione 1.0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[Informazioni sul Utilità di pianificazione](about-the-task-scheduler.md)
</dt> </dl>

 

 
