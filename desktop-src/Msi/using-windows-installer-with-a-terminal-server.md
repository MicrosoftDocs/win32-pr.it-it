---
description: Quando si usa un server terminal, Windows le installazioni del programma di installazione seguenti. Gli sviluppatori del programma di installazione devono sempre verificare che il pacchetto Windows Installer sia installato come previsto quando gli utenti usano anche un server terminal.
ms.assetid: deda9efa-a0fc-4b4e-a531-650ac201fd84
title: Uso Windows programma di installazione con Terminal Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9aba70bc9430f0bc55c7e234b19764a14b138a4d5053de5c1cc6b9aee37692d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995831"
---
# <a name="using-windows-installer-with-a-terminal-server"></a>Uso Windows programma di installazione con Terminal Server

Quando si usa un server terminal, Windows le installazioni del programma di installazione seguenti. Gli sviluppatori del programma di installazione devono sempre verificare che il pacchetto Windows Installer sia installato come previsto quando gli utenti usano anche un server terminal.

-   Nei sistemi operativi precedenti Windows Server 2008 e Windows Vista è necessario impostare i criteri di sistema [EnableAdminTSRemote](enableadmintsremote.md) per consentire agli amministratori di eseguire installazioni nella sessione client. A partire Windows Server 2008 e Windows Vista, il criterio EnableAdminTSRemote non ha più alcun effetto. Indipendentemente dall'impostazione, gli amministratori e gli utenti non amministratori possono eseguire un'installazione nella sessione client o nella sessione della console. Gli amministratori e gli utenti non amministratori possono sempre Windows installazioni del programma di installazione nella sessione della console.
-   Il Windows installer impedisce l'installazione [](installation-context.md) nel contesto di installazione per utente se il criterio di sistema [DisableUserInstalls](disableuserinstalls.md)[è](system-policy.md) impostato su 1. In questo caso, il programma di installazione ignora tutte le applicazioni registrate in base all'utente e cerca solo le applicazioni registrate in base al computer.
-   Quando un amministratore esegue un'installazione in una sessione client di un server terminal ospitato in Windows 2000, l'installazione deve utilizzare un percorso UNC e non una lettera di unità mappata.

Gli sviluppatori devono rispettare le linee guida seguenti quando sviluppano un Windows programma di installazione che può essere usato con un server terminal.

-   Scrivere tutte le informazioni del Registro di sistema **HKCU** nella **parte HKCU** \\ **Software** del Registro di sistema.
-   Non è consigliabile archiviare le informazioni di configurazione nei file INI.
-   Scrivere le informazioni per utente nel Registro di sistema quando l'applicazione viene eseguita per la prima volta e non al momento dell'installazione. Se è necessario scrivere informazioni per utente nel Registro di sistema in fase di installazione, separare le informazioni per utente e per computer in diversi componenti del Windows Installer. Creare il pacchetto in modo che il programma di installazione non tenti di convalidare e ripristinare i componenti contenenti informazioni per utente durante l'installazione dell'applicazione.
-   Un pacchetto usato solo per le installazioni per computer deve scrivere le variabili di ambiente nell'ambiente del computer includendo nella \* colonna Nome della tabella [dell'ambiente](environment-table.md). Se il pacchetto può essere usato per installazioni per utente o per computer, usare due componenti. Includere il componente per utente nella tabella [dei componenti e](condition-table.md) immettere le impostazioni utente nella tabella dell'ambiente. Includere il componente per computer nella tabella dei componenti e immettere le impostazioni del computer nella tabella dell'ambiente. Controllare quale componente viene installato usando istruzioni condizionali basate sulla proprietà [**ALLUSERS**](allusers.md) nel campo Condizione della tabella dei componenti.
-   Quando si eseguono installazioni per computer da un server terminal, il programma di installazione scrive le variabili di ambiente per utente in **HKCU.** \\ **Ambiente** \\ **predefinito.** Poiché il server terminal non replica questa sezione del Registro di sistema, l'installazione non imposta le variabili di ambiente per utente.
-   Poiché un server può essere configurato per impedire agli utenti di ripristinare le applicazioni, l'applicazione deve gestire normalmente il caso di chiavi del Registro di sistema mancanti.

Quanto segue si applica quando un pacchetto del programma di installazione di Windows che usa azioni personalizzate DLL, EXE o [script](custom-actions.md) viene installato nel contesto di installazione per computer in un server terminal. In questo caso, il programma di installazione imposta la [**proprietà TerminalServer.**](terminalserver.md)

-   Le azioni personalizzate posticipate vengono eseguite nel contesto del sistema locale, a meno che l'azione non abbia l'attributo **msidbCustomActionTypeTSAware.** Questo vale anche se l'azione personalizzata rappresenta l'utente in un sistema che non è un server terminal. Si noti che se un'azione personalizzata con l'attributo **msidbCustomActionTypeTSAware** modifica il Registro di sistema dell'utente, il programma di installazione non garantisce automaticamente che tali modifiche siano apportate anche nel Registro di sistema di ogni utente del computer.
-   Tutte le operazioni del Registro di sistema in un'azione personalizzata posticipata che leggono dall'hive del Registro di sistema **HKCU** vedono l'hive del Registro di sistema predefinito del sistema e non l'hive del Registro di sistema dell'utente corrente.
-   Tutte le operazioni del Registro di sistema in un'azione personalizzata posticipata che scrivono in **HKCU** Software vengono rilevate dal programma di installazione e copiate in ogni utente del computer al successivo accesso \\  dell'utente.
-   Tutte le operazioni del Registro di sistema in un'azione personalizzata posticipata che scrivono in **HKCU**, ma non sono nella chiave del Registro di sistema **HKCU** Software, non vengono rilevate dal programma di installazione \\  o copiate.

Per altre informazioni, vedere [Servizi terminal](../termserv/terminal-services-portal.md) in Microsoft Windows Software Development Kit (SDK).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[EnableAdminTSRemote](enableadmintsremote.md)
</dt> <dt>

[**TerminalServer - proprietà**](terminalserver.md)
</dt> <dt>

[**RemoteAdminTS - proprietà**](remoteadmints.md)
</dt> <dt>

[Servizi terminal](../termserv/terminal-services-portal.md)
</dt> </dl>

 

 
