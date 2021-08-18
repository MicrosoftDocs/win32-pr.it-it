---
description: Il Windows può determinare quando è necessario un riavvio del sistema e richiedere automaticamente all'utente di riavviare al termine dell'installazione.
ms.assetid: 10117d2c-c2c8-456f-9fce-a89c2d69d3c1
title: Riavvii del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e5ff72b91b50a3da03fbfb0c52ff351af907c7f89b400120c463dab233f288
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626831"
---
# <a name="system-reboots"></a>Riavvii del sistema

Il Windows può determinare quando è necessario un riavvio del sistema e richiedere automaticamente all'utente di riavviare al termine dell'installazione. Ad esempio, il programma di installazione richiede automaticamente un riavvio se deve sostituire i file in uso durante l'installazione.

Le applicazioni che usano [Windows Installer](windows-installer-portal.md) versione 4.0 o successiva per l'installazione e la manutenzione usano automaticamente Gestione [riavvio](../rstmgr/restart-manager-portal.md) per ridurre i riavvii del sistema. Windows Il programma di installazione versione 4.0 o successiva include proprietà e criteri che consentono all'autore e agli amministratori del pacchetto di controllare l'interazione di Windows Installer con Gestione riavvio. Per altre informazioni, vedere [Using Windows Installer with Restart Manager](using-windows-installer-with-restart-manager.md).

Gli autori dei pacchetti di installazione possono pianificare ed eliminare i riavvii usando azioni standard nelle tabelle di sequenza e impostando le proprietà. Le azioni e le proprietà seguenti vengono usate per gestire i riavvii del sistema.



| Azione, finestra di dialogo o proprietà                                                | Breve descrizione                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Azione ForceReboot](forcereboot-action.md)                                   | Richiede all'utente un riavvio durante l'installazione.                                                                                                        |
| [Azione ScheduleReboot](schedulereboot-action.md)                             | Richiede all'utente un riavvio al termine dell'installazione.                                                                                                 |
| [**Proprietà REBOOT**](reboot.md)                                              | Forza o elimina determinati prompt automatici per il riavvio del sistema.                                                                                           |
| [**Proprietà REBOOTPROMPT**](rebootprompt.md)                                  | Elimina la visualizzazione delle richieste di riavvio per l'utente. Tutti i riavvii necessari vengono e completati automaticamente.                                                           |
| [**Proprietà AFTERREBOOT**](afterreboot.md)                                    | Comunemente usato in una condizione imposta all'azione ForceReboot.                                                                                               |
| [Azione InstallValidate](installvalidate-action.md)                           | Visualizza la finestra di dialogo FileInUsa, se necessario, offrendo agli utenti la possibilità di arrestare i processi ed evitare alcuni riavvii del sistema.                              |
| [Finestra di dialogo FileInUsa](filesinuse-dialog.md)                                     | Offre agli utenti la possibilità di arrestare i processi per evitare alcuni riavvii del sistema.                                                                              |
| [Finestra di dialogo MsiRMFilesInUse](msirmfilesinuse-dialog.md)                           | Offre agli utenti la possibilità di usare [Gestione riavvio per](../rstmgr/restart-manager-portal.md) chiudere e riavviare le applicazioni. Disponibile a partire da Windows Installer versione 4.0. |
| [**Proprietà ReplacedInUseFiles**](replacedinusefiles.md)                      | Impostare se il programma di installazione viene installato su un file in uso. Questa proprietà viene usata dalle azioni personalizzate per rilevare che è necessario un riavvio.                                |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)                   | Proprietà per disabilitare Windows'interazione del programma di installazione con [Gestione riavvio.](../rstmgr/restart-manager-portal.md) Disponibile a partire da Windows Installer versione 4.0.          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)                             | Specifica il modo in cui [Gestione riavvio](../rstmgr/restart-manager-portal.md) chiude e riavvia le applicazioni. Disponibile a partire da Windows Installer versione 4.0.                  |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)                                         | Specifica il modo in cui [Gestione riavvio](../rstmgr/restart-manager-portal.md) chiude e riavvia le applicazioni. Disponibile a partire da Windows Installer versione 4.0.                  |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)                       | Il programma di installazione imposta questa proprietà se il riavvio del sistema operativo è in sospeso. Disponibile a partire da Windows Installer versione 4.0.                         |
| [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) | Criteri per disabilitare l Windows del programma di installazione con [Gestione riavvio.](../rstmgr/restart-manager-portal.md) Disponibile a partire da Windows Installer versione 4.0.                |



 

ERROR \_ INSTALL SUSPEND indica che \_ l'installazione non è stata completata o non è stata completata. L'installazione deve riprendere prima del completamento. Potrebbe essere necessario riavviare il sistema prima di poter riprendere l'installazione.

Il Windows di installazione restituisce il codice di errore ERROR \_ INSTALL SUSPEND quando viene eseguita \_ [l'azione ForceReboot.](forcereboot-action.md) Restituisce ERROR SUCCESS REBOOT REQUIRED se è necessario un riavvio prima di eseguire l'applicazione e RESTITUISCE ERROR SUCCESS REBOOT INITIATED se il programma di installazione \_ ha effettivamente avviato un \_ \_ \_ \_ \_ riavvio. Si noti che poiché i riavvii sono asincroni, il riavvio può effettivamente verificarsi prima che venga restituito il codice di errore. Per altre informazioni, vedere [Codici di errore.](error-codes.md)

Le azioni personalizzate possono forzare la richiesta di riavvio al termine di un'installazione chiamando [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode). Le azioni personalizzate possono anche verificare la presenza di una richiesta di riavvio in sospeso chiamando [**MsiGetMode.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)

## <a name="filesinuse-dialog"></a>Finestra di dialogo FileInUsa

Il programma di installazione può determinare quando è necessario un riavvio del sistema e richiedere all'utente di riavviare il sistema. In genere, è necessario un riavvio del sistema perché il programma di installazione sta tentando di installare un file attualmente in uso. Se [l'azione InstallValidate](installvalidate-action.md) rileva l'installazione di un file in uso, viene visualizzata la [finestra di dialogo FilesInUse](filesinuse-dialog.md).

Se si prevede che il programma di installazione visualizza un oggetto FilesInUseDialog, ma non lo è, ciò potrebbe essere dovuto a uno dei motivi seguenti:

-   I file in uso non sono eseguibili.
-   Il programma di installazione non sta effettivamente tentando di installare tali file.
-   Il processo che contiene tali file è il processo che richiama l'installazione.
-   Il processo che contiene tali file è uno che non dispone di una finestra con un titolo associato.

Per altre informazioni, vedere [Registrazione delle richieste di riavvio.](logging-of-reboot-requests.md)

 

 
