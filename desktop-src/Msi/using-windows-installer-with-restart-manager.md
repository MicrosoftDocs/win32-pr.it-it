---
description: Le applicazioni che utilizzano Windows Installer 4,0 per l'installazione e la manutenzione in Windows Vista utilizzano automaticamente Gestione riavvio per ridurre i riavvii del sistema.
ms.assetid: 821739ff-f7a7-4192-ad34-254aa7d74d13
title: Uso di Windows Installer con Gestione riavvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4160b2241c75ec7305accd1ab4d1295a54fa9f65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308176"
---
# <a name="using-windows-installer-with-restart-manager"></a>Uso di Windows Installer con Gestione riavvio

Le applicazioni che utilizzano Windows Installer 4,0 per l'installazione e la manutenzione in Windows Vista utilizzano automaticamente [Gestione riavvio](../rstmgr/restart-manager-portal.md) per ridurre i riavvii del sistema. Il comportamento predefinito in Windows Vista consiste nell'arrestare le applicazioni anziché arrestare e riavviare il sistema operativo laddove possibile. Nei casi in cui un riavvio del sistema è inevitabile, i programmi di installazione possono usare l'API di [Gestione riavvio](../rstmgr/restart-manager-portal.md) per pianificare i riavvii in modo da ridurre al minimo l'alterazione del flusso di lavoro dell'utente.

Windows Installer gli sviluppatori possono eseguire le azioni seguenti per preparare il pacchetto in modo che funzioni con [Gestione riavvio](../rstmgr/restart-manager-portal.md).

-   Aggiungere la finestra di dialogo [MsiRMFilesInUse](msirmfilesinuse-dialog.md) al pacchetto. Se la finestra di dialogo MsiRMFilesInUse è presente nel pacchetto, l'utente di Windows Vista che esegue un'installazione al livello completo dell' [interfaccia utente](user-interface-levels.md) dell'interfaccia utente ha la possibilità di chiudere e riavviare automaticamente le applicazioni. Un pacchetto di installazione può contenere informazioni per la finestra di dialogo MsiRMFilesInUse e la finestra di dialogo [filesinus](filesinuse-dialog.md) . La finestra di dialogo MsiRMFilesInUse viene visualizzata solo se il pacchetto è installato con almeno Windows Installer 4,0 in Windows Vista e in caso contrario viene ignorato. I pacchetti esistenti che non hanno la finestra di dialogo MsiRMFilesInUse continuano a funzionare usando la finestra di dialogo filesinusale. È possibile utilizzare una trasformazione di personalizzazione per aggiungere una finestra di dialogo MsiRMFilesInUse a pacchetti esistenti.

    Gli utenti finali eseguono in genere installazioni al livello completo dell' [interfaccia utente](user-interface-levels.md)dell'interfaccia utente. Le installazioni di base dell'interfaccia utente o a livello di interfaccia utente ridotto consentono all'utente di usare [Gestione riavvio](../rstmgr/restart-manager-portal.md) per ridurre i riavvii del sistema anche se la finestra di dialogo [MsiRMFilesInUse](msirmfilesinuse-dialog.md) non è presente. Le installazioni a livello di interfaccia utente invisibile all'utente arrestano sempre le applicazioni e i servizi e in Windows Vista utilizzano sempre Gestione riavvio.

-   Registrare le applicazioni per un riavvio utilizzando la funzione [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) . Gestione riavvio può riavviare solo le applicazioni che sono state registrate per il riavvio. Gestione riavvio riavvia le applicazioni registrate dopo l'installazione. Se l'installazione richiede un riavvio del sistema, gestione riavvio riavvia l'applicazione registrata dopo il riavvio del sistema.
-   Specificare INSTALLLOGMODE \_ RMFILESINUSE quando si Abilita un gestore dell'interfaccia utente esterno con le funzioni [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) e [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) . Windows Installer invierà un \_ messaggio INSTALLMESSAGE RMFILESINUSE per i gestori dell'interfaccia utente esterni che supportano [Gestione riavvio](../rstmgr/restart-manager-portal.md). Se nessuna interfaccia utente registrata o interna gestisce il messaggio INSTALLMESSAGE \_ RMFILESINUSE, il programma di installazione invia un \_ messaggio filesinus INSTALLMESSAGE per i gestori dell'interfaccia utente che supportano la finestra di dialogo [filesinusale](filesinuse-dialog.md) . Per ulteriori informazioni, vedere [utilizzo di gestione riavvio con un'interfaccia utente esterna](using-restart-manager-with-an-external-ui-.md).
-   Le azioni personalizzate possono aggiungere risorse appartenenti a una sessione di [Gestione riavvio](../rstmgr/restart-manager-portal.md) . L'azione personalizzata deve essere sequenziata prima dell'azione [InstallValidate](installvalidate-action.md) . Le azioni personalizzate possono utilizzare la proprietà [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md) per ottenere la chiave della sessione e devono chiamare le funzioni [**RmJoinSession**](/windows/win32/api/restartmanager/nf-restartmanager-rmjoinsession) e [**RmEndSession**](/windows/win32/api/restartmanager/nf-restartmanager-rmendsession) dell'API di gestione riavvio. Le azioni personalizzate non possono rimuovere risorse appartenenti a una sessione di gestione riavvio. Le azioni personalizzate non devono tentare di arrestare o riavviare le applicazioni usando le funzioni [**RmShutdown**](/windows/win32/api/restartmanager/nf-restartmanager-rmshutdown), [**RmGetList**](/windows/win32/api/restartmanager/nf-restartmanager-rmgetlist) e [**RmRestart**](/windows/win32/api/restartmanager/nf-restartmanager-rmrestart) .
-   Gli autori di pacchetti possono basare una condizione nella [tabella LaunchCondition](launchcondition-table.md) della proprietà [**MsiSystemRebootPending**](msisystemrebootpending.md) per impedire l'installazione del pacchetto quando un riavvio del sistema è in sospeso.
-   Gli autori e gli amministratori di pacchetti possono controllare l'interazione di Windows Installer e gestione riavvio usando le proprietà [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md), [**MSIDISABLERMRESTART**](msidisablermrestart.md), [**MSIRMSHUTDOWN**](msirmshutdown.md) e [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) .
-   Le applicazioni e i servizi devono seguire le linee guida descritte nella sezione [utilizzo di gestione riavvio](../rstmgr/using-restart-manager.md) della documentazione di [Gestione riavvio](../rstmgr/restart-manager-portal.md) .

 

 
