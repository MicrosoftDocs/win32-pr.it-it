---
description: Quando si utilizza un server terminal, può interessare le installazioni di Windows Installer seguenti. Gli sviluppatori del programma di installazione devono sempre verificare che il pacchetto di Windows Installer venga installato come previsto quando gli utenti utilizzano anche un server terminal.
ms.assetid: deda9efa-a0fc-4b4e-a531-650ac201fd84
title: Uso di Windows Installer con un Terminal Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d471fa19b4588a01a2730af44fa5e9d978d18859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484660"
---
# <a name="using-windows-installer-with-a-terminal-server"></a>Uso di Windows Installer con un Terminal Server

Quando si utilizza un server terminal, può interessare le installazioni di Windows Installer seguenti. Gli sviluppatori del programma di installazione devono sempre verificare che il pacchetto di Windows Installer venga installato come previsto quando gli utenti utilizzano anche un server terminal.

-   Nei sistemi operativi precedenti a Windows Server 2008 e Windows Vista, i criteri di sistema [EnableAdminTSRemote](enableadmintsremote.md) devono essere impostati in modo da consentire agli amministratori di eseguire installazioni nella sessione client. A partire da Windows Server 2008 e Windows Vista, il criterio EnableAdminTSRemote non ha più alcun effetto. Indipendentemente dall'impostazione, gli amministratori e gli amministratori non possono eseguire un'installazione nella sessione client o nella sessione della console. Gli amministratori e gli amministratori non possono sempre eseguire le installazioni Windows Installer nella sessione della console.
-   Il Windows Installer impedisce l'installazione nel [contesto di installazione](installation-context.md) per utente se il[criterio di sistema](system-policy.md) [DisableUserInstalls](disableuserinstalls.md)è impostato su 1. In questo caso, il programma di installazione ignora tutte le applicazioni registrate come per singolo utente e cerca solo le applicazioni registrate come per computer.
-   Quando un amministratore esegue un'installazione in una sessione client di un server terminal ospitato in Windows 2000, è necessario che l'installazione usi un percorso UNC e non una lettera di unità mappata.

Quando si sviluppa un componente Windows Installer che può essere utilizzato con un server terminal, gli sviluppatori devono attenersi alle linee guida seguenti.

-   Scrivere tutte le informazioni del registro di sistema **HKCU** nella  \\ parte **software** HKCU del registro di sistema.
-   Non è consigliabile archiviare le informazioni di configurazione nei file INI.
-   Consente di scrivere le informazioni per utente nel registro di sistema quando l'applicazione viene eseguita per la prima volta e non in fase di installazione. Se è necessario scrivere le informazioni per utente nel registro di sistema al momento dell'installazione, separare le informazioni per utente e per computer in componenti Windows Installer diversi. Creare il pacchetto in modo che il programma di installazione non tenti di convalidare e riparare i componenti contenenti informazioni per utente durante l'installazione dell'applicazione.
-   Un pacchetto usato solo per le installazioni per computer deve scrivere le variabili di ambiente nell'ambiente del computer includendo \* nella colonna nome della [tabella dell'ambiente](environment-table.md). Se il pacchetto può essere usato per installazioni per utente o per computer, usare due componenti. Includere il componente per utente nella tabella dei [componenti](condition-table.md) e immettere le impostazioni utente nella tabella dell'ambiente. Includere il componente per computer nella tabella dei componenti e immettere le impostazioni del computer nella tabella dell'ambiente. Controllare quale componente viene installato utilizzando istruzioni condizionali basate sulla proprietà [**ALLUSERS**](allusers.md) nel campo condition della tabella Component.
-   Quando si eseguono installazioni per computer da un server terminal, il programma di installazione scrive le variabili di ambiente per ogni utente in **HKCU** \\ **.** \\ **Ambiente** predefinito. Poiché il server terminal non esegue la replica di questa sezione del registro di sistema, l'installazione non imposta le variabili di ambiente per singolo utente.
-   Poiché un server può essere configurato per impedire agli utenti di ripristinare le applicazioni, l'applicazione deve gestire il caso di chiavi del registro di sistema mancanti normalmente.

Le condizioni seguenti si applicano quando un pacchetto di Windows Installer che utilizza [azioni personalizzate](custom-actions.md) dll, exe o script viene installato nel contesto di installazione per computer in un server terminal. In questo caso, il programma di installazione imposta la proprietà [**TerminalServer**](terminalserver.md) .

-   Le azioni personalizzate posticipate vengono eseguite nel contesto del sistema locale, a meno che l'azione non includa l'attributo **msidbCustomActionTypeTSAware** . Questo vale anche se l'azione personalizzata rappresenta l'utente in un sistema che non è un server terminal. Si noti che se un'azione personalizzata con l'attributo **msidbCustomActionTypeTSAware** modifica il registro di sistema dell'utente, il programma di installazione non verifica automaticamente che tali modifiche vengano apportate anche nel registro di sistema di ogni utente del computer.
-   Qualsiasi operazione del registro di sistema in un'azione personalizzata posticipata che legge dall'hive del registro di sistema **HKCU** Visualizza l'hive del registro di sistema predefinito del sistema e non l'hive del registro di sistema dell'utente corrente.
-   Tutte le operazioni del registro di sistema in un'azione personalizzata posticipata che scrivono in **HKCU** \\ **software** vengono rilevate dal programma di installazione e copiate a ogni utente del computer al successivo accesso dell'utente.
-   Qualsiasi operazione del registro di sistema in un'azione personalizzata posticipata che scrive in **HKCU**, ma che non si trova sotto la  \\ chiave del registro di sistema HKCU **software** , non viene rilevata dal programma di installazione o copiata.

Per ulteriori informazioni, vedere [Servizi terminal](../termserv/terminal-services-portal.md) in Microsoft Windows Software Development Kit (SDK).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[EnableAdminTSRemote](enableadmintsremote.md)
</dt> <dt>

[**Proprietà TerminalServer**](terminalserver.md)
</dt> <dt>

[**Proprietà RemoteAdminTS**](remoteadmints.md)
</dt> <dt>

[Servizi terminal](../termserv/terminal-services-portal.md)
</dt> </dl>

 

 
