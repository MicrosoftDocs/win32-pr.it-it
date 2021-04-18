---
description: Il Windows Installer può determinare quando è necessario riavviare il sistema e richiedere automaticamente all'utente di riavviare il computer al termine dell'installazione.
ms.assetid: 10117d2c-c2c8-456f-9fce-a89c2d69d3c1
title: Riavvio del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b32149bbcd43e284f45d7cabcba94a080be5262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308673"
---
# <a name="system-reboots"></a>Riavvio del sistema

Il Windows Installer può determinare quando è necessario riavviare il sistema e richiedere automaticamente all'utente di riavviare il computer al termine dell'installazione. Ad esempio, il programma di installazione richiede automaticamente un riavvio se è necessario sostituire i file in uso durante l'installazione.

Le applicazioni che utilizzano [Windows Installer](windows-installer-portal.md) versione 4,0 o successive per l'installazione e la manutenzione utilizzano automaticamente [Gestione riavvio](../rstmgr/restart-manager-portal.md) per ridurre i riavvii del sistema. Windows Installer versione 4,0 o versioni successive dispone di proprietà e criteri che consentono all'autore del pacchetto e agli amministratori di controllare l'interazione di Windows Installer con Gestione riavvio. Per ulteriori informazioni, vedere [utilizzo di Windows Installer con Gestione riavvio](using-windows-installer-with-restart-manager.md).

Gli autori dei pacchetti di installazione possono pianificare ed evitare i riavvii utilizzando le azioni standard nelle tabelle di sequenza e impostando le proprietà. Per gestire i riavvii del sistema vengono utilizzate le azioni e le proprietà seguenti.



| Azione, finestra di dialogo o proprietà                                                | Breve descrizione                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Azione ForceReboot](forcereboot-action.md)                                   | Richiede all'utente di riavviare il computer durante l'installazione.                                                                                                        |
| [Azione ScheduleReboot](schedulereboot-action.md)                             | Richiede all'utente di riavviare il computer al termine dell'installazione.                                                                                                 |
| [**Riavvia proprietà**](reboot.md)                                              | Forza o Disattiva determinati prompt automatici per il riavvio del sistema.                                                                                           |
| [**Proprietà REBOOTPROMPT**](rebootprompt.md)                                  | Disattiva la visualizzazione dei prompt per i riavvii per l'utente. Tutti i riavvii necessari avvengono automaticamente.                                                           |
| [**Proprietà AFTERREBOOT**](afterreboot.md)                                    | Utilizzato comunemente in una condizione imposta sull'azione ForceReboot.                                                                                               |
| [Azione InstallValidate](installvalidate-action.md)                           | Visualizza la finestra di dialogo filesinusale, se necessario, per consentire agli utenti di arrestare i processi ed evitare alcuni riavvii del sistema.                              |
| [Finestra di dialogo filesinus](filesinuse-dialog.md)                                     | Fornisce agli utenti la possibilità di arrestare i processi per evitare alcuni riavvii del sistema.                                                                              |
| [Finestra di dialogo MsiRMFilesInUse](msirmfilesinuse-dialog.md)                           | Fornisce agli utenti la possibilità di usare [Gestione riavvio](../rstmgr/restart-manager-portal.md) per chiudere e riavviare le applicazioni. Disponibile a partire dalla versione Windows Installer 4,0. |
| [**Proprietà ReplacedInUseFiles**](replacedinusefiles.md)                      | Impostare se il programma di installazione viene installato su un file in uso. Questa proprietà viene utilizzata dalle azioni personalizzate per rilevare che è necessario riavviare il computer.                                |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)                   | Per disabilitare Windows Installer interazione con [Gestione riavvio](../rstmgr/restart-manager-portal.md). Disponibile a partire dalla versione Windows Installer 4,0.          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)                             | Specifica il modo in cui [Gestione riavvio](../rstmgr/restart-manager-portal.md) chiude e riavvia le applicazioni. Disponibile a partire dalla versione Windows Installer 4,0.                  |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)                                         | Specifica il modo in cui [Gestione riavvio](../rstmgr/restart-manager-portal.md) chiude e riavvia le applicazioni. Disponibile a partire dalla versione Windows Installer 4,0.                  |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)                       | Questa proprietà viene impostata dal programma di installazione se è in sospeso il riavvio del sistema operativo. Disponibile a partire dalla versione Windows Installer 4,0.                         |
| [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) | Criteri per disabilitare Windows Installer interazione con [Gestione riavvio](../rstmgr/restart-manager-portal.md). Disponibile a partire dalla versione Windows Installer 4,0.                |



 

ERRORE \_ installazione \_ sospensione indica che l'installazione non è stata completata o non è stata completata. Per completare l'installazione, è necessario riprenderla. Potrebbe essere necessario riavviare il sistema prima di poter riprendere l'installazione.

Il Windows Installer restituisce il codice di errore \_ install \_ Suspend Quando viene eseguita l' [azione ForceReboot](forcereboot-action.md) . Viene restituito un errore di \_ \_ riavvio \_ necessario se è necessario riavviare prima di eseguire l'applicazione e viene restituito \_ l'errore \_ riavvio completato \_ se il programma di installazione ha effettivamente avviato un riavvio. Si noti che poiché i riavvii sono asincroni, il riavvio può effettivamente verificarsi prima della restituzione del codice di errore. Per ulteriori informazioni, vedere [codici di errore](error-codes.md).

Le azioni personalizzate possono forzare la richiesta di riavvio al termine di un'installazione chiamando [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode). Le azioni personalizzate possono inoltre verificare la presenza di un prompt di riavvio in sospeso chiamando [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode).

## <a name="filesinuse-dialog"></a>Finestra di dialogo filesinus

Il programma di installazione può determinare quando è necessario riavviare il sistema e richiedere all'utente una richiesta di riavvio. In genere, è necessario riavviare il sistema perché il programma di installazione sta tentando di installare un file attualmente in uso. Se l' [azione InstallValidate](installvalidate-action.md) rileva l'installazione di un file in uso, viene visualizzata la [finestra di dialogo filesinusale](filesinuse-dialog.md).

Se si prevede che il programma di installazione visualizzi un FilesInUseDialog, ma ciò potrebbe essere dovuto a uno dei motivi seguenti:

-   I file in uso non sono eseguibili.
-   Il programma di installazione non sta effettivamente tentando di installare tali file.
-   Il processo che contiene questi file è il processo che richiama l'installazione.
-   Il processo che contiene questi file non dispone di una finestra con un titolo associato.

Per ulteriori informazioni, vedere [registrazione di richieste di riavvio](logging-of-reboot-requests.md).

 

 
