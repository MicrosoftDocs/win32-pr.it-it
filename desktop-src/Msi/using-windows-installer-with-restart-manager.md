---
description: Le applicazioni che usano Windows Installer 4.0 per l'installazione e la manutenzione in Windows Vista usano automaticamente Gestione riavvio per ridurre i riavvii del sistema.
ms.assetid: 821739ff-f7a7-4192-ad34-254aa7d74d13
title: Uso Windows programma di installazione con Gestione riavvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf361cf20d6f56dc25bd43c9077c65a25eeebdae1c6b512dfcde3e756448a7b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141151"
---
# <a name="using-windows-installer-with-restart-manager"></a>Uso Windows programma di installazione con Gestione riavvio

Le applicazioni che usano Windows Installer 4.0 per l'installazione e la manutenzione in Windows Vista usano automaticamente Gestione [riavvio](../rstmgr/restart-manager-portal.md) per ridurre i riavvii del sistema. Il comportamento predefinito in Windows Vista è arrestare le applicazioni anziché arrestare e riavviare il sistema operativo quando possibile. Nei casi in cui un riavvio del sistema è inevitabile, i programmi di installazione possono usare l'API di [Gestione](../rstmgr/restart-manager-portal.md) riavvio per pianificare i riavvii in modo da ridurre al minimo l'interruzione del flusso di lavoro dell'utente.

Windows Gli sviluppatori di programmi di installazione possono eseguire le azioni seguenti per preparare il pacchetto per l'utilizzo con [Gestione riavvio.](../rstmgr/restart-manager-portal.md)

-   Aggiungere la [finestra di dialogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) al pacchetto. Se la finestra di dialogo MsiRMFilesInUse è presente nel pacchetto, l'utente [](user-interface-levels.md) di Windows Vista che esegue un'installazione a livello di interfaccia utente completa ha la possibilità di chiudere e riavviare automaticamente le applicazioni. Un pacchetto di installazione può contenere informazioni sia per la finestra di dialogo MsiRMFilesInUse che per la finestra di dialogo [FilesInUse](filesinuse-dialog.md) . La finestra di dialogo MsiRMFilesInUse viene visualizzata solo se il pacchetto è installato con almeno Windows Installer 4.0 in Windows Vista e in caso contrario viene ignorato. I pacchetti esistenti che non dispongono della finestra di dialogo MsiRMFilesInUse continuano a funzionare usando la finestra di dialogo FilesInUse. È possibile usare una trasformazione di personalizzazione per aggiungere una finestra di dialogo MsiRMFilesInUse ai pacchetti esistenti.

    Gli utenti finali eseguono in genere installazioni a livello di [interfaccia utente completa.](user-interface-levels.md) Le installazioni a livello di interfaccia utente di [](../rstmgr/restart-manager-portal.md) base o a livello di interfaccia utente ridotta offrono all'utente la possibilità di usare Gestione riavvio per ridurre i riavvii del sistema anche se la finestra di dialogo [MsiRMFilesInUse](msirmfilesinuse-dialog.md) non è presente. Le installazioni a livello di interfaccia utente invisibile all'utente arrestano sempre le applicazioni e i servizi e Windows Vista usano sempre Gestione riavvio.

-   Registrare le applicazioni per un riavvio [**usando la funzione RegisterApplicationRestart.**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) Gestione riavvio può riavviare solo le applicazioni registrate per il riavvio. Gestione riavvio riavvia le applicazioni registrate dopo l'installazione. Se l'installazione richiede un riavvio del sistema, Gestione riavvio riavvia l'applicazione registrata dopo il riavvio del sistema.
-   Specificare INSTALLLOGMODE RMFILESINUSE quando si abilita un gestore dell'interfaccia utente esterno con le funzioni \_ [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) e [**MsiSetExternalUIRecord.**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) Windows Il programma di installazione invierà un messaggio INSTALLMESSAGE RMFILESINUSE per i gestori dell'interfaccia utente esterni che \_ supportano [Gestione riavvio.](../rstmgr/restart-manager-portal.md) Se nessuna interfaccia utente registrata o interna gestisce il messaggio INSTALLMESSAGE RMFILESINUSE, il programma di installazione invia un messaggio INSTALLMESSAGE FILESINUSE per i gestori dell'interfaccia utente che supportano la finestra di dialogo \_ \_ [FilesInUse.](filesinuse-dialog.md) Per altre informazioni, vedere Uso [di Gestione riavvio con un'interfaccia utente esterna.](using-restart-manager-with-an-external-ui-.md)
-   Le azioni personalizzate possono aggiungere risorse appartenenti a una [sessione di Gestione riavvio.](../rstmgr/restart-manager-portal.md) L'azione personalizzata deve essere sequenziata prima [dell'azione InstallValidate.](installvalidate-action.md) Le azioni personalizzate possono usare la proprietà [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md) per ottenere la chiave di sessione e devono chiamare le funzioni [**RmJoinSession**](/windows/win32/api/restartmanager/nf-restartmanager-rmjoinsession) e [**RmEndSession**](/windows/win32/api/restartmanager/nf-restartmanager-rmendsession) dell'API di Gestione riavvio. Le azioni personalizzate non possono rimuovere le risorse appartenenti a una sessione di Gestione riavvio. Le azioni personalizzate non devono tentare di arrestare o riavviare le applicazioni usando le funzioni [**RmShutdown**](/windows/win32/api/restartmanager/nf-restartmanager-rmshutdown), [**RmGetList**](/windows/win32/api/restartmanager/nf-restartmanager-rmgetlist) [**e RmRestart.**](/windows/win32/api/restartmanager/nf-restartmanager-rmrestart)
-   Gli autori di pacchetti possono basare una condizione nella tabella [LaunchCondition](launchcondition-table.md) sulla proprietà [**MsiSystemRebootPending**](msisystemrebootpending.md) per impedire l'installazione del pacchetto quando un riavvio del sistema è in sospeso.
-   Gli autori e gli amministratori di pacchetti possono controllare l'interazione del programma di installazione di Windows e di Gestione riavvio usando le proprietà [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md), [**MSIDISABLERMRESTART**](msidisablermrestart.md), [**MSIRMSHUTDOWN**](msirmshutdown.md) e i criteri [DisableAutomaticApplicationShutdown.](disableautomaticapplicationshutdown.md)
-   Le applicazioni e i servizi devono seguire le linee guida descritte nella [sezione Uso](../rstmgr/using-restart-manager.md) di Gestione riavvio della documentazione di [Gestione riavvio.](../rstmgr/restart-manager-portal.md)

 

 
