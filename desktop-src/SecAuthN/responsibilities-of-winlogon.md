---
description: Elenca e illustra le responsabilità di Winlogon.
ms.assetid: 5aef4164-11bd-4acc-b851-de982e35d2b5
title: Responsabilità di Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6561bea11c48eb474c0ff56c5c0aa5ebfa0c22d9d6689aa55a6a208bbbc683e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919029"
---
# <a name="responsibilities-of-winlogon"></a>Responsabilità di Winlogon

[*Winlogon*](../secgloss/w-gly.md) ha le responsabilità seguenti:

-   Stazione finestra e protezione desktop

    Winlogon imposta la protezione della stazione finestra e dei desktop corrispondenti per garantire che ognuno sia accessibile correttamente. In generale, ciò significa che il sistema locale avrà accesso completo a questi oggetti e che un utente connesso in modo interattivo avrà accesso in lettura all'oggetto stazione finestra e accesso completo all'oggetto desktop dell'applicazione.

-   Riconoscimento della firma di accesso condiviso standard

    Winlogon dispone di hook speciali nel server User32 che consentono [](../secgloss/s-gly.md) di monitorare gli eventi della sequenza di attenzione sicura (SAS) CTRL+ALT+CANC. Winlogon rende disponibili queste informazioni sugli eventi di firma di accesso condiviso da usare come firma di accesso condiviso o come parte della firma di accesso condiviso. In generale, le unità DIA devono monitorare le sass di per sé; Tuttavia, qualsiasi [*GINA*](../secgloss/g-gly.md) che abbia la firma di accesso condiviso STANDARD CTRL+ALT+CANC standard come una delle saS riconoscite deve usare il supporto Winlogon fornito a questo scopo.

-   Invio di routine di firma di accesso condiviso

    Quando Winlogon rileva un evento di firma di accesso condiviso o quando una firma di accesso condiviso viene recapitata a Winlogon da GINA, Winlogon imposta lo stato di conseguenza, modifica il desktop Winlogon e chiama una delle funzioni di elaborazione SAS di GINA.

-   Caricamento del profilo utente

    Quando gli utenti a log on, i profili utente vengono caricati nel Registro di sistema. In questo modo, i processi dell'utente possono usare la chiave speciale del Registro di sistema HKEY \_ CURRENT \_ USER. Winlogon esegue questa operazione automaticamente dopo un accesso riuscito, ma prima dell'attivazione della shell per l'utente appena connesso.

-   Assegnazione della sicurezza alla shell utente

    Quando un utente accede, l'istanza di GINA è responsabile della creazione di uno o più processi iniziali per tale utente. Winlogon offre una funzione di supporto per l'applicazione della sicurezza dell'utente appena connesso a questi processi. Tuttavia, il modo migliore per eseguire questa operazione è chiamare la funzione [**Windows CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)e consentire al sistema di fornire il servizio.

-   Controllo dello screen saver

    Winlogon monitora l'attività di tastiera e mouse per determinare quando attivare gli screen saver. Dopo aver attivato screen saver, Winlogon continua a monitorare l'attività della tastiera e del mouse per determinare quando terminare il screen saver. Se il screen saver è contrassegnato come sicuro, Winlogon considera la workstation bloccata. Quando è presente un'attività tramite mouse o tastiera, Winlogon richiama la funzione [**WlxDisplayLockedNotice**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaylockednotice) di GINA e riprende il comportamento della workstation bloccata. Se il screen saver non è sicuro, qualsiasi attività della tastiera o del mouse termina il screen saver senza notifica all'istanza di GINA.

-   Supporto di più provider di rete

    Più reti installate in un Windows sistema possono essere incluse nel processo di autenticazione e nelle operazioni di aggiornamento delle password. Questa inclusione consente ad altre reti di raccogliere informazioni di identificazione e autenticazione tutte contemporaneamente durante il normale accesso, usando il desktop sicuro di Winlogon. Alcuni dei parametri necessari nei servizi Winlogon disponibili per LEA supportano in modo esplicito questi provider di rete aggiuntivi.

 

 
