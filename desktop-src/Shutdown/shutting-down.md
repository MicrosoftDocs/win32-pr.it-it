---
description: "Ci sono tre modi per arrestare l'applicazione di computer locali o remoti: arrestare il systemshut di sistema e riavviare itshut per difetto l'applicazione, arrestare e riavviare il sistema e riavviare le applicazioni registrate per il riavvio"
ms.assetid: acadf58f-3f68-4fa1-bdcf-8f85c8479263
title: Chiusura in corso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e436dd9e3b115112e63b0440b4d51de4c7f9f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317666"
---
# <a name="shutting-down"></a>Chiusura in corso

È possibile arrestare i computer locali o remoti per un'applicazione in tre modi:

-   arrestare il sistema
-   arrestare il sistema e riavviarlo
-   arrestare l'applicazione, arrestare e riavviare il sistema e riavviare tutte le applicazioni registrate per il riavvio

Per arrestare il sistema, utilizzare la funzione [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) con il flag di \_ chiusura EWX. Per un esempio, vedere [come arrestare il sistema](how-to-shut-down-the-system.md). Per arrestare e riavviare il sistema, usare il flag di \_ riavvio EWX. Per riavviare le applicazioni che sono state registrate per il riavvio usando la funzione [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) , usare il \_ flag RESTARTAPPS di EXW.

Le funzioni [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna), [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)e [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) avviano un timer e visualizzano una finestra di dialogo in cui viene richiesto all'utente di disconnettersi. Quando questa finestra di dialogo viene visualizzata, la funzione [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) può arrestare il timer e impedire l'arresto del computer. Tuttavia, se il timer scade, il computer viene arrestato. Queste funzioni possono anche riavviare il computer dopo un'operazione di arresto. Per ulteriori informazioni, vedere [visualizzazione della finestra di dialogo Arresta](displaying-the-shutdown-dialog-box.md).

## <a name="shutdown-notifications"></a>Notifiche di arresto

Le applicazioni con una finestra e una coda di messaggi ricevono notifiche di chiusura tramite i messaggi [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) e [**WM \_ ENDSESSION**](wm-endsession.md) . Queste applicazioni devono restituire **true** per indicare che possono essere interrotte. Le applicazioni non devono bloccare l'arresto del sistema, a meno che non sia assolutamente necessario. Le applicazioni devono eseguire qualsiasi pulizia necessaria durante l'elaborazione di **WM \_ ENDSESSION**. Le applicazioni con dati non salvati potrebbero salvare i dati in un percorso temporaneo e ripristinarli al successivo avvio dell'applicazione. È consigliabile che le applicazioni salvino i dati e lo stato di frequente; ad esempio, salvare automaticamente i dati tra le operazioni di salvataggio avviate dall'utente per ridurre la quantità di dati da salvare al momento dell'arresto.

Le applicazioni console ricevono notifiche di chiusura nelle routine del gestore. Per registrare un gestore della console, usare la funzione [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) .

Le applicazioni di servizio ricevono notifiche di chiusura nelle routine del gestore. Per registrare un gestore di controllo del servizio, utilizzare la funzione [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) .

## <a name="blocking-shutdown"></a>Arresto blocco

Se un'applicazione deve bloccare un potenziale arresto del sistema, può chiamare la funzione [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) . Il chiamante fornisce una stringa del motivo che verrà visualizzata all'utente. La stringa del motivo dovrebbe essere breve e chiara, fornendo all'utente le informazioni necessarie per decidere se continuare l'arresto del sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come arrestare il sistema](how-to-shut-down-the-system.md)
</dt> </dl>

 

 
