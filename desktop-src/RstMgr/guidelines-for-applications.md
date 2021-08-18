---
title: Linee guida per le applicazioni
description: Le applicazioni in esecuzione in Windows Vista e Windows Server 2008 devono rispettare queste linee guida per garantire che Gestione riavvio possa arrestare e riavviare le applicazioni se necessario per installare gli aggiornamenti.
ms.assetid: 97b1df63-65a9-47b4-891b-e4a754882b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9624f578a04267b94bde41bbdf8e3312e7b8ae0f4fb84280212ea51c2db7e2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010129"
---
# <a name="guidelines-for-applications"></a>Linee guida per le applicazioni

Le applicazioni in esecuzione in Windows Vista e Windows Server 2008 devono rispettare queste linee guida per garantire che Gestione riavvio possa arrestare e riavviare le applicazioni se necessario per installare gli aggiornamenti. I servizi possono usare le linee guida descritte in [Linee guida per i servizi](guidelines-for-services.md).

-   Gestione riavvio esegue query sulle applicazioni GUI per l'arresto inviando una notifica [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) con il parametro *lParam* impostato su **ENDSESSION \_ CLOSEAPP** (0x1). Le applicazioni non devono essere arrestate quando ricevono un messaggio **WM \_ QUERYENDSESSION** perché un'altra applicazione potrebbe non essere pronta per l'arresto. Le applicazioni GUI devono restare in ascolto del messaggio **WM \_ QUERYENDSESSION** e restituire il valore **TRUE** se l'applicazione è pronta per l'arresto e il riavvio. Se nessuna applicazione restituisce il valore **FALSE,** Gestione riavvio invia un messaggio [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) con il parametro *lParam* impostato su **ENDSESSION \_ CLOSEAPP** (0x1) e il parametro *wparam* impostato su **TRUE.** Le applicazioni devono essere arrestate solo quando ricevono il **messaggio \_ ENDSESSION WM.** Gestione riavvio invia anche un [**messaggio WM \_ CLOSE**](../winmsg/wm-close.md) per le applicazioni GUI che non vengono arrestate alla ricezione **di WM \_ ENDSESSION.** Se un'applicazione GUI risponde a un messaggio **WM \_ QUERYENDSESSION** restituisce il valore **FALSE,** l'arresto viene annullato. Tuttavia, se l'arresto viene forzato, l'applicazione viene terminata indipendentemente.
-   Quando un'applicazione GUI riceve un [**messaggio \_ ENDSESSION WM,**](/windows/desktop/Shutdown/wm-endsession) l'applicazione deve prepararsi per l'arresto entro il periodo di timeout specificato. Come minimo, le applicazioni devono prepararsi salvando i dati utente e le informazioni sullo stato necessari dopo un riavvio. È consigliabile che le applicazioni salvano periodicamente i dati utente e lo stato.
-   Gestione riavvio invia una **notifica \_ CTRL C \_ EVENT** alle applicazioni console che devono essere arrestate e riavviate. Quando un'applicazione console riceve una notifica **DI EVENTO CTRL \_ C, \_** l'applicazione deve eseguire le azioni necessarie per preparare l'arresto entro il periodo di timeout specificato. Come minimo, le applicazioni console devono definire una funzione [*HandlerRoutine*](/windows/console/handlerroutine) per gestire la notifica **DELL'EVENTO CTRL \_ C \_** e salvare i dati utente e le informazioni sullo stato che saranno necessari dopo un riavvio. È consigliabile che le applicazioni salvano periodicamente i dati utente e lo stato.
-   Se le applicazioni non vengono arrestate in risposta ai messaggi di arresto, i programmi di installazione possono usare l'opzione **RmForceShutdown** della funzione [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) per forzare l'arresto delle applicazioni. Quando il programma di installazione specifica un arresto forzato, Gestione riavvio tenta di arrestare correttamente le applicazioni inviando i messaggi di arresto, ma forza l'arresto in caso di errore. È possibile forzare l'arresto delle applicazioni GUI e delle applicazioni console per abilitare l'installazione di un aggiornamento della sicurezza critico. Poiché ciò può comportare la perdita di dati, le applicazioni devono gestire i messaggi di arresto e arrestarsi correttamente quando necessario.
-   Le applicazioni devono registrarsi per un riavvio usando la [**funzione RegisterApplicationRestart.**](/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart) Gestione riavvio può riavviare solo le applicazioni registrate per il riavvio. Questo è l'unico modo in cui Gestione riavvio può determinare il comando della riga di comando da usare quando si riavvia l'applicazione. Se l'applicazione deve essere riaperta con uno stato o dati salvati, queste informazioni devono essere incluse nel comando della riga di comando registrato per l'applicazione.
    > [!Note]  
    > Se l'applicazione riavviata deve essere eseguita nella stessa directory in cui è stata eseguita prima dell'arresto, l'applicazione deve salvare le informazioni sulla directory e quindi passare alla directory dopo il riavvio.

     

    > [!Note]  
    > La [**funzione RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) non riavvia le applicazioni che non vengono eseguite come utente attualmente connesso. Ad esempio, la **funzione RmRestart** non riavvia le applicazioni avviate con il comando **RunAs** che non vengono eseguite come utente attualmente connesso. Queste applicazioni devono essere riavviate manualmente.

     

-   Quando Gestione riavvio determina che è necessario un riavvio del sistema per installare un aggiornamento, non arresta applicazioni e servizi. Ma lascia al programma di installazione di decidere quando pianificare un riavvio del sistema e installare l'aggiornamento. I programmi di installazione possono ridurre l'interruzione per gli utenti causati da aggiornamenti che richiedono un riavvio del sistema usando la funzione [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) con il flag **EWX \_ RESTARTAPPS** o la funzione [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) con il flag **SHUTDOWN \_ RESTARTAPPS.** L'uso di questi flag garantisce che le applicazioni registrate per il riavvio siano riavviate dopo un riavvio del sistema, riducendo al minimo l'impatto sull'utente.

 

 