---
description: Elenca e spiega le responsabilità di Winlogon.
ms.assetid: 5aef4164-11bd-4acc-b851-de982e35d2b5
title: Responsabilità di Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7842df1d4194dc7086f658a13f6725af8fa0d88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967392"
---
# <a name="responsibilities-of-winlogon"></a>Responsabilità di Winlogon

[*Winlogon*](../secgloss/w-gly.md) ha le responsabilità seguenti:

-   Windows Station e Desktop Protection

    Winlogon imposta la protezione della stazione della finestra e dei desktop corrispondenti per assicurarsi che ogni sia accessibile correttamente. In generale, questo significa che il sistema locale avrà accesso completo a questi oggetti e che un utente connesso in modo interattivo disporrà dell'accesso in lettura all'oggetto della stazione della finestra e dell'accesso completo all'oggetto desktop dell'applicazione.

-   Riconoscimento SAS standard

    In Winlogon sono presenti Hook speciali nel server user32 che consentono di monitorare gli eventi di firma di accesso condiviso (SAS, [*Secure Attention Sequence*](../secgloss/s-gly.md) ). Winlogon rende disponibili le informazioni sull'evento SAS a GINAs da usare come firma di accesso condiviso o come parte della firma di accesso condiviso. In generale, GINAs deve monitorare SASs autonomamente; Tuttavia, qualsiasi [*Gina*](../secgloss/g-gly.md) con la firma di accesso condiviso standard con la combinazione di tasti CTRL + ALT + CANC come uno dei SASs it riconosce deve usare il supporto Winlogon fornito a questo scopo.

-   Invio di routine SAS

    Quando Winlogon rileva un evento SAS o quando una firma di accesso condiviso viene recapitata a Winlogon da GINA, Winlogon imposta lo stato in base alle modifiche apportate al desktop Winlogon e chiama una delle funzioni di elaborazione della firma di accesso condiviso di GINA.

-   Caricamento del profilo utente

    Quando gli utenti accedono, i relativi profili utente vengono caricati nel registro di sistema. In questo modo, i processi dell'utente possono usare la chiave del registro di sistema speciale HKEY \_ Current \_ User. Winlogon esegue questa operazione automaticamente dopo un accesso riuscito, ma prima dell'attivazione della Shell per l'utente appena connesso.

-   Assegnazione di sicurezza alla shell utente

    Quando un utente esegue l'accesso, GINA è responsabile della creazione di uno o più processi iniziali per tale utente. Winlogon fornisce una funzione di supporto affinché GINA applichi la sicurezza dell'utente appena connesso a questi processi. Tuttavia, il modo migliore per eseguire questa operazione è che GINA chiama la funzione di Windows [**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)e consente al sistema di fornire il servizio.

-   Controllo screen saver

    Winlogon monitora l'attività della tastiera e del mouse per determinare quando attivare i salvaschermi. Dopo l'attivazione del screen saver, Winlogon continua a monitorare l'attività della tastiera e del mouse per determinare quando terminare l'screen saver. Se la screen saver è contrassegnata come sicura, Winlogon considera la workstation bloccata. Quando si verifica un'attività di mouse o tastiera, Winlogon richiama la funzione [**WlxDisplayLockedNotice**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaylockednotice) di Gina e il comportamento della workstation bloccato riprende. Se il screen saver non è sicuro, qualsiasi attività della tastiera o del mouse termina l'screen saver senza notifica a GINA.

-   Supporto per più provider di rete

    Più reti installate in un sistema Windows possono essere incluse nel processo di autenticazione e nelle operazioni di aggiornamento delle password. Questa inclusione consente alle reti aggiuntive di raccogliere informazioni di identificazione e autenticazione in una sola volta durante il normale accesso, usando il desktop sicuro di Winlogon. Alcuni dei parametri richiesti nei servizi Winlogon disponibili per le GINA supportano in modo esplicito questi provider di rete aggiuntivi.

 

 
