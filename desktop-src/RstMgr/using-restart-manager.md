---
title: Utilizzo di gestione riavvio
description: Le sezioni seguenti descrivono l'uso dell'API di gestione riavvio.
ms.assetid: 78448d5e-20f6-45b6-b833-7d7791e5e4c6
keywords:
- Riavviare Gestione riavvio, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4ac72edb9f2395bbd67236806c3ab3029372cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872838"
---
# <a name="using-restart-manager"></a>Utilizzo di gestione riavvio

Le sezioni seguenti descrivono l'uso dell'API di gestione riavvio. Le applicazioni e i servizi devono seguire anche le [linee guida per le applicazioni e i servizi](guidelines-for-applications-and-services.md).

## <a name="using-the-microsoft-windows-installer"></a>Uso della Microsoft Windows Installer

Il [Microsoft Windows Installer](/windows/desktop/Msi/windows-installer-portal) versione 4,0 è il servizio di installazione dell'applicazione di Windows Vista o windows Server 2008. Le applicazioni che usano la versione di Windows Installer 4,0 per l'installazione e la manutenzione utilizzano automaticamente Gestione riavvio per ridurre i riavvii del sistema. I programmi di installazione personalizzati possono anche essere progettati per chiamare l'API di gestione riavvio per arrestare e riavviare direttamente le applicazioni e i servizi per evitare di richiedere un riavvio del sistema. Nei casi in cui un riavvio del sistema è inevitabile, i programmi di installazione possono usare la funzione [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) o [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) per pianificarla in modo da ridurre al minimo l'interferenza dell'utente. I pacchetti Windows Installer interattivi devono implementare un'interfaccia utente che include una finestra di dialogo [MsiRMFilesInUse](/windows/desktop/Msi/msirmfilesinuse-dialog) . Per ulteriori informazioni, vedere [utilizzo di Windows Installer con Gestione riavvio](/windows/desktop/Msi/using-windows-installer-with-restart-manager) nella documentazione di Windows Installer SDK.

## <a name="using-the-restart-manager-api-with-custom-installers"></a>Uso dell'API di gestione riavvio con i programmi di installazione personalizzati

I programmi di installazione personalizzati o un pacchetto di Windows Installer contenente azioni personalizzate che determinano un riavvio del sistema possono utilizzare l'API di gestione riavvio per arrestare e riavviare le applicazioni e i servizi.

-   Tutte le operazioni eseguite tramite l'API di gestione riavvio devono essere associate a una sessione. Un massimo di 64 sessioni di gestione riavvio per ogni sessione utente può essere aperto contemporaneamente nel sistema. Il programma di installazione principale viene avviato e termina la sessione di gestione riavvio. Per ulteriori informazioni sull'utilizzo di gestione riavvio con un singolo programma di installazione, vedere [utilizzo di gestione riavvio con un programma di installazione primario](using-restart-manager-with-a-primary-installer.md).
-   Se necessario per l'installazione, uno o più programmi di installazione secondari possono essere aggiunti alla sessione di gestione riavvio e possono essere eseguiti in-process o out-of-process del programma di installazione primario. Per i programmi di installazione secondari è necessario che la chiave della sessione venga fornita dal programma di installazione primario per partecipare a una sessione. Per ulteriori informazioni e un esempio di utilizzo di programmi di installazione secondari, vedere [utilizzo di gestione riavvio con un programma di installazione secondario](using-restart-manager-with-a-secondary-installer.md).
-   I programmi di installazione interattiva devono implementare un'interfaccia utente che include una finestra di dialogo [MsiRMFilesInUse](/windows/desktop/Msi/msirmfilesinuse-dialog) che può richiedere agli utenti di chiudere le applicazioni e i servizi. Per ulteriori informazioni, vedere [utilizzo di Windows Installer con Gestione riavvio](/windows/desktop/Msi/using-windows-installer-with-restart-manager) nella documentazione di Windows Installer SDK.
-   I programmi di installazione possono chiamare l'API di gestione riavvio per modificare, annullare e ottenere lo stato dell'operazione corrente di gestione riavvio. Per ulteriori informazioni, vedere gli argomenti seguenti: [recupero dello stato di un'operazione di gestione riavvio](getting-the-status-of-a-restart-manager-operation.md) e [annullamento dell'operazione corrente di gestione riavvio](canceling-the-current-restart-manager-operation.md).
-   I programmi di installazione non devono disabilitare il reindirizzamento file system prima di chiamare l'API di gestione riavvio. Alcuni programmi di installazione a 32 bit vengono eseguiti in Windows a 64 bit potrebbe non essere in grado di registrare un file nella directory% windir% \\ system32.

 

 