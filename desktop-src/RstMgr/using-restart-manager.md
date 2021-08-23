---
title: Uso di Gestione riavvio
description: Le sezioni seguenti descrivono l'uso dell'API Gestione riavvio.
ms.assetid: 78448d5e-20f6-45b6-b833-7d7791e5e4c6
keywords:
- Riavviare Manager Restart Mgr , usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90826091aa4a3cdf39e0a1f063a211255ec4ef9cf84b06214eb172150ac3b8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009999"
---
# <a name="using-restart-manager"></a>Uso di Gestione riavvio

Le sezioni seguenti descrivono l'uso dell'API Gestione riavvio. Le applicazioni e i servizi devono anche seguire le [linee guida per applicazioni e servizi.](guidelines-for-applications-and-services.md)

## <a name="using-the-microsoft-windows-installer"></a>Uso del programma di installazione di Microsoft Windows

[Microsoft Windows Installer](/windows/desktop/Msi/windows-installer-portal) versione 4.0 è il servizio di installazione delle applicazioni di Windows Vista o Windows Server 2008. Le applicazioni che usano il Windows Installer versione 4.0 per l'installazione e la manutenzione usano automaticamente Gestione riavvio per ridurre i riavvii del sistema. I programmi di installazione personalizzati possono anche essere progettati per chiamare l'API Restart Manager per arrestare e riavviare direttamente applicazioni e servizi per evitare di richiedere un riavvio del sistema. Nei casi in cui un riavvio del sistema è inevitabile, i programmi di installazione possono usare la funzione [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) o [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) per pianificarla in modo da ridurre al minimo l'interruzione per l'utente. I Windows installer interattivi devono implementare un'interfaccia utente che include una finestra di dialogo [MsiRMFilesInUse.](/windows/desktop/Msi/msirmfilesinuse-dialog) Per altre informazioni, vedere [Using Windows Installer with Restart Manager](/windows/desktop/Msi/using-windows-installer-with-restart-manager) (Uso del programma di installazione di Windows con Gestione riavvio) nella documentazione Windows Installer SDK.

## <a name="using-the-restart-manager-api-with-custom-installers"></a>Uso dell'API Gestione riavvio con programmi di installazione personalizzati

I programmi di installazione personalizzati o un pacchetto Windows installer che contiene azioni personalizzate che causano un riavvio del sistema possono usare l'API Gestione riavvio per arrestare e riavviare applicazioni e servizi.

-   Tutte le operazioni eseguite tramite l'API Gestione riavvio devono essere associate a una sessione. Nel sistema è possibile aprire contemporaneamente un massimo di 64 sessioni di Restart Manager per sessione utente. Il programma di installazione primario avvia e termina la sessione di Gestione riavvio. Per altre informazioni sull'uso di Gestione riavvio con un singolo programma di installazione, vedere Uso di [Gestione riavvio con un programma di installazione primario](using-restart-manager-with-a-primary-installer.md).
-   Se necessario per l'installazione, uno o più programmi di installazione secondari possono essere aggiunti alla sessione di Gestione riavvio e possono essere eseguiti in-process o out-of-process del programma di installazione primario. I programmi di installazione secondari richiedono che la chiave di sessione sia fornita dal programma di installazione primario per partecipare a una sessione. Per altre informazioni e un esempio di uso dei programmi di installazione secondari, vedere Uso di [Gestione riavvio con un programma di installazione secondario](using-restart-manager-with-a-secondary-installer.md).
-   I programmi di installazione interattivi devono implementare un'interfaccia utente che include una finestra di dialogo [MsiRMFilesInUse](/windows/desktop/Msi/msirmfilesinuse-dialog) che può chiedere agli utenti di chiudere applicazioni e servizi. Per altre informazioni, vedere [Using Windows Installer with Restart Manager](/windows/desktop/Msi/using-windows-installer-with-restart-manager) (Uso del programma di installazione di Windows con Gestione riavvio) nella documentazione Windows Installer SDK.
-   I programmi di installazione possono chiamare l'API Gestione riavvio per modificare, annullare e ottenere lo stato dell'operazione di Gestione riavvio corrente. Per altre informazioni, vedere gli argomenti seguenti: [Recupero dello](getting-the-status-of-a-restart-manager-operation.md) stato di un'operazione di Gestione riavvio [e Annullamento dell'operazione corrente di Gestione riavvio](canceling-the-current-restart-manager-operation.md).
-   I programmi di installazione non devono disabilitare file system reindirizzamento prima di chiamare l'API Restart Manager. Alcuni programmi di installazione a 32 bit eseguiti in Windows a 64 bit potrebbero non essere in grado di registrare un file nella directory %windir% \\ system32.

 

 