---
description: Alcuni sistemi usano firewall Internet o server proxy che richiedono l'autenticazione per tutto il traffico Internet.
ms.assetid: b79e9a6f-2ffb-4ec0-ac2d-63e79ecfc26c
title: Server di simboli e firewall Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a998b5bd2aea2685ac060df6ddd8acdcd904c9997a0da8dfbf8fdc636ac90f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004862"
---
# <a name="symbol-server-and-internet-firewalls"></a>Server di simboli e firewall Internet

Alcuni sistemi usano firewall Internet o server proxy che richiedono l'autenticazione per tutto il traffico Internet. Le versioni precedenti del server di simboli non potevano accedere ai simboli da Internet a meno che il sistema non usava un client firewall che gestiva l'autenticazione in modo trasparente.

A partire da Dbghelp 6.1, il server di simboli supporta i server proxy che richiedono tale autenticazione. Il server di simboli usa qualsiasi server configurato come predefinito nelle impostazioni LAN del computer. A tale scopo, aprire l'elemento **Opzioni Internet**  in Pannello di controllo, fare clic sulla scheda Connessioni e fare clic su **LAN Impostazioni**. Questa operazione può essere eseguita anche Internet Explorer scegliendo **Opzioni Internet** **dal** menu Strumenti. Il server di simboli è stato testato su molti marchi di server proxy usando metodi di autenticazione sia di base che di risposta alle richieste di verifica.

Per definire un server proxy specifico da usare per il server di simboli, impostare la variabile di ambiente NT SYMBOL PROXY sul nome (o indirizzo IP) del server proxy, seguito dal \_ \_ numero di \_ porta. Separare i due valori con due punti. Esempio:

**set \_ NT \_ SYMBOL \_ PROXY=**_myproxyserver_*_:80_*

Quando si usa il debugger windbg, configurare il percorso dei simboli in modo che punti all'archivio simboli che si vuole usare. L'unica differenza è che il sistema visualizza una finestra di dialogo in cui è necessario immettere l'ID utente e la password per passare al server proxy. Se si immettono informazioni non corrette, la finestra di dialogo verrà visualizzata di nuovo. Se si fa clic **sul pulsante** Annulla, la finestra di dialogo viene chiusa e il server di simboli verrà disabilitato per l'uso tramite Internet.

Quando si usano le versioni più recenti cdb.exe o ntsd.exe, questa funzionalità è disattivata per impostazione predefinita. È tuttavia possibile abilitare o disabilitare questa funzionalità usando il comando !sym extension come indicato di seguito:

-   Per attivare la richiesta di ID utente e password: **!sym prompts**.
-   Per disattivare la richiesta di ID utente e password: **!sym prompts off**.

Se si attiva la richiesta, sarà necessario ricaricare i simboli con il comando .reload.

L'API DbgHelp è stata espansa per supportare queste modifiche. La [**funzione SymbolServerSetOptions**](/previous-versions//ms680676(v=vs.85)) supporta l'opzione PROXY SSRVOPT. \_ Se il parametro di dati è **NULL,** viene usato il proxy predefinito definito in **Opzioni Internet.** In caso contrario, viene passata una stringa con terminazione zero che specifica il nome e il numero di porta del server proxy. Il nome e la porta sono separati da due punti nel modo seguente: *myproxyserver*:80. La [**funzione SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) supporta l'opzione SYMOPT \_ NO \_ PROMPTS. In questo modo vengono disattivate tutte le richieste di convalida dal server di simboli.

 

 
