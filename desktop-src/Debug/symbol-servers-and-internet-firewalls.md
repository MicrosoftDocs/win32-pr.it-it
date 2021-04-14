---
description: Alcuni sistemi usano firewall o server proxy Internet che richiedono l'autenticazione per tutto il traffico Internet.
ms.assetid: b79e9a6f-2ffb-4ec0-ac2d-63e79ecfc26c
title: Server di simboli e firewall Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2a85a5d0ee2d41e6ffee40bbb275155bdf1e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523066"
---
# <a name="symbol-server-and-internet-firewalls"></a>Server di simboli e firewall Internet

Alcuni sistemi usano firewall o server proxy Internet che richiedono l'autenticazione per tutto il traffico Internet. Le versioni precedenti del server di simboli non possono accedere ai simboli da Internet, a meno che il sistema non abbia utilizzato un client firewall che gestisse l'autenticazione in modo trasparente.

A partire da dbghelp 6,1, il server di simboli supporta i server proxy che richiedono l'autenticazione. Il server dei simboli utilizza qualsiasi server configurato come predefinito nelle impostazioni LAN del computer. Per trovarlo, aprire l'elemento **Opzioni Internet** nel pannello di controllo, fare clic sulla scheda **connessioni** e fare clic su **Impostazioni LAN**. Questa operazione può essere eseguita anche da Internet Explorer scegliendo **Opzioni Internet** dal menu **strumenti** . Il server dei simboli è stato testato su molte marche di server proxy usando i metodi di autenticazione di base e di richiesta-risposta.

Per definire un server proxy specifico per il server di simboli da utilizzare, impostare la \_ variabile di ambiente del proxy del simbolo NT sul \_ \_ nome (o indirizzo IP) del server proxy, seguito dal numero di porta. Separare i due valori con i due punti. Ad esempio:

**imposta \_ \_Proxy del simbolo NT \_ =**_myProxyServer_*_: 80_*

Quando si usa il debugger WinDbg, configurare il percorso dei simboli in modo che punti all'archivio simboli che si vuole usare. L'unica differenza è che nel sistema verrà visualizzata una finestra di dialogo in cui è necessario immettere l'ID utente e la password da passare al server proxy. Se si immettono informazioni non corrette, la finestra di dialogo verrà visualizzata nuovamente. Se si fa clic sul pulsante **Annulla** , la finestra di dialogo viene rilasciata e il server di simboli verrà disabilitato per l'utilizzo tramite Internet.

Quando si usano le versioni più recenti di cdb.exe o ntsd.exe, questa funzionalità è disattivata per impostazione predefinita. Tuttavia, è possibile abilitare o disabilitare questa funzionalità usando il comando. sym Extension come indicato di seguito:

-   Per attivare la richiesta di conferma dell'ID utente e della password: **! sym Prompts**.
-   Per disattivare la richiesta di conferma dell'ID utente e della password: **! sym richiede off**.

Se si attiva la richiesta, sarà necessario ricaricare i simboli con il comando. Reload.

L'API DbgHelp è stata espansa per supportare queste modifiche. La funzione [**SymbolServerSetOptions**](/previous-versions//ms680676(v=vs.85)) supporta l' \_ opzione proxy SSRVOPT. Se il parametro data è **null**, viene utilizzato il proxy predefinito definito in **Opzioni Internet** . In caso contrario, viene passata una stringa con terminazione zero che specifica il nome e il numero di porta del server proxy. Il nome e la porta sono separati da due punti, come indicato di seguito: *myProxyServer*: 80. La funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) supporta l' \_ opzione SYMOPT No \_ Prompts. Questa operazione disattiva la richiesta di convalida dal server di simboli.

 

 
