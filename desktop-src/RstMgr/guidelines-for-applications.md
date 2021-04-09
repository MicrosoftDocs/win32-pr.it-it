---
title: Linee guida per le applicazioni
description: Le applicazioni in esecuzione in Windows Vista e Windows Server 2008 devono rispettare queste linee guida per garantire che Gestione riavvio possa arrestare e riavviare le applicazioni, se necessario, per installare gli aggiornamenti.
ms.assetid: 97b1df63-65a9-47b4-891b-e4a754882b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebace21e09956c68d34c90775c5ea646a8b2dd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729626"
---
# <a name="guidelines-for-applications"></a>Linee guida per le applicazioni

Le applicazioni in esecuzione in Windows Vista e Windows Server 2008 devono rispettare queste linee guida per garantire che Gestione riavvio possa arrestare e riavviare le applicazioni, se necessario, per installare gli aggiornamenti. I servizi possono usare le linee guida descritte in [linee guida per i servizi](guidelines-for-services.md).

-   Gestione riavvio esegue una query sulle applicazioni GUI per l'arresto inviando una notifica [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) con il parametro *lParam* impostato su **ENDSESSION \_ CLOSEAPP** (0x1). Le applicazioni non devono essere arrestate quando ricevono un messaggio **WM \_ QUERYENDSESSION** perché un'altra applicazione potrebbe non essere pronta per l'arresto. Le applicazioni GUI devono ascoltare il messaggio **WM \_ QUERYENDSESSION** e restituire il valore **true** se l'applicazione è preparata per l'arresto e il riavvio. Se nessuna applicazione restituisce un valore **false**, gestione riavvio Invia un messaggio [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) con il parametro *lParam* impostato su **ENDSESSION \_ CLOSEAPP** (0x1) e il parametro *wParam* impostato su **true**. Le applicazioni devono essere arrestate solo quando ricevono il messaggio **WM \_ ENDSESSION** . Gestione riavvio invia anche un messaggio [**WM \_ Close**](../winmsg/wm-close.md) per le applicazioni GUI che non si arrestano alla ricezione di **WM \_ ENDSESSION**. Se un'applicazione GUI risponde a un messaggio **WM \_ QUERYENDSESSION** restituendo un valore **false**, l'arresto viene annullato. Tuttavia, se l'arresto è forzato, l'applicazione viene terminata indipendentemente.
-   Quando un'applicazione GUI riceve un messaggio [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) , l'applicazione deve prepararsi a arrestarsi entro il periodo di timeout specificato. Come minimo, le applicazioni devono essere preparate salvando tutti i dati utente e le informazioni sullo stato necessarie dopo un riavvio. È consigliabile che le applicazioni Salvino periodicamente i dati e lo stato dell'utente.
-   Gestione riavvio invia una notifica **di \_ \_ evento CTRL C** alle applicazioni console che devono essere arrestate e riavviate. Quando un'applicazione console riceve una notifica di **\_ \_ evento CTRL C** , l'applicazione deve eseguire le operazioni necessarie per preparare un arresto entro il periodo di timeout specificato. Come minimo, le applicazioni console devono definire una funzione [*HandlerRoutine*](/windows/console/handlerroutine) per gestire la notifica degli **eventi di CTRL \_ C \_** e salvare tutti i dati utente e le informazioni sullo stato che saranno necessari dopo un riavvio. È consigliabile che le applicazioni Salvino periodicamente i dati e lo stato dell'utente.
-   Se le applicazioni non vengono arrestate in risposta ai messaggi di chiusura, i programmi di installazione possono usare l'opzione **RmForceShutdown** della funzione [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) per forzare l'arresto dell'applicazione. Quando il programma di installazione specifica un arresto forzato, gestione riavvio tenta di arrestare correttamente le applicazioni inviando i messaggi di arresto, ma forza l'arresto in caso di errore. È possibile forzare l'arresto di applicazioni GUI e applicazioni console per consentire l'installazione di un aggiornamento critico della sicurezza. Poiché questo può comportare la perdita di dati, le applicazioni devono gestire i messaggi di arresto e arrestare la pulizia quando necessario.
-   Le applicazioni devono registrarsi per un riavvio tramite la funzione [**RegisterApplicationRestart**](/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart) . Gestione riavvio può riavviare solo le applicazioni che sono state registrate per il riavvio. Questo è l'unico modo in cui gestione riavvio è in grado di determinare il comando della riga di comando da usare durante il riavvio dell'applicazione. Se l'applicazione deve riaprirsi con alcuni dati o uno stato salvato, tali informazioni devono essere incluse nel comando della riga di comando registrato per l'applicazione.
    > [!Note]  
    > Se l'applicazione riavviata deve essere eseguita nella stessa directory in cui è stata eseguita prima di essere arrestata, l'applicazione deve salvare le informazioni della directory e quindi passare alla directory dopo il riavvio.

     

    > [!Note]  
    > La funzione [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) non riavvia le applicazioni che non vengono eseguite come utente attualmente connesso. Ad esempio, la funzione **RmRestart** non riavvia le applicazioni avviate con il comando **RunAs** che non vengono eseguite come utente attualmente connesso. Queste applicazioni devono essere riavviate manualmente.

     

-   Quando Gestione riavvio determina che è necessario riavviare il sistema per installare un aggiornamento, non arresta alcun servizio e applicazioni. Al contrario, lascia al programma di installazione di decidere quando pianificare un riavvio del sistema e installare l'aggiornamento. I programmi di installazione possono ridurre l'interruzione degli utenti causati da aggiornamenti che richiedono un riavvio del sistema tramite la funzione [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) con il flag **EWX \_ RESTARTAPPS** o la funzione [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) con il flag **Shutdown \_ RESTARTAPPS** . L'uso di questi flag garantisce che le applicazioni registrate per il riavvio vengano riavviate dopo un riavvio del sistema, riducendo al minimo l'effetto sull'utente.

 

 