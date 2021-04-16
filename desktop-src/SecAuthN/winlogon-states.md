---
description: Winlogon gestisce lo stato della workstation usato da GINA per determinare le azioni di autenticazione necessarie.
ms.assetid: e04175c4-bb43-4f76-8ceb-50282a1ebed0
title: Stati di Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d2e4ec690d6bdda15fb8e350969b36e01d5c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571553"
---
# <a name="winlogon-states"></a>Stati di Winlogon

[*Winlogon*](../secgloss/w-gly.md) gestisce lo stato della workstation usato da [*Gina*](../secgloss/g-gly.md) per determinare le azioni di autenticazione necessarie.

In qualsiasi momento, Winlogon è in uno dei tre stati seguenti:

-   [Stato di connessione](#logged-off-state)
-   [Stato di accesso](#logged-on-state)
-   [Stato di blocco della workstation](#workstation-locked-state)

Questi tre Stati sono illustrati nella figura seguente.

![Stati di Winlogon](images/winlogonst.png)

## <a name="logged-off-state"></a>Stato Logged-Off

Quando Winlogon si trova nello stato di disconnessione, agli utenti viene richiesto di identificarsi e fornire informazioni di autenticazione. Se un utente fornisce informazioni corrette sull'account utente e nessuna restrizione lo impedisce, l'utente è connesso e viene eseguito un programma shell, ad esempio Esplora risorse, nel desktop dell'applicazione. Winlogon passa allo stato connesso.

## <a name="logged-on-state"></a>Stato Logged-On

Quando Winlogon si trova nello stato connesso, gli utenti possono interagire con la shell, attivare applicazioni aggiuntive ed eseguire le operazioni. Dallo stato connesso, gli utenti possono arrestare tutto il lavoro e disconnettersi o bloccare le workstation (lasciando tutto il lavoro sul posto). Se l'utente decide di disconnettersi, Winlogon interromperà tutti i processi associati alla [*sessione di accesso*](../secgloss/l-gly.md) e la workstation sarà disponibile per un altro utente. Se, invece, l'utente decide di bloccare la workstation, Winlogon passa allo stato di blocco della workstation.

## <a name="workstation-locked-state"></a>Stato Workstation-Locked

Quando Winlogon si trova nello stato di blocco della workstation, viene visualizzato un desktop sicuro fino a quando l'utente sblocca la workstation fornendo le stesse informazioni di identificazione e autenticazione dell'utente che ha eseguito l'accesso in origine o fino a quando un amministratore non forza la disconnessione. Se la workstation è sbloccata, viene visualizzato il desktop dell'applicazione e il lavoro può essere ripreso. Se, tuttavia, un amministratore Sblocca la workstation (fornendo le informazioni di identificazione e autenticazione di un account amministratore), i processi dell'utente connesso vengono interrotti e Winlogon passa allo stato di disconnessione.

In ogni stato di Winlogon è possibile eseguire una serie di azioni diverse. Una DLL GINA può implementare azioni che non fanno parte del sistema operativo Windows standard. Ad esempio, un sistema di sicurezza elevato potrebbe bloccare automaticamente una workstation ogni 10 minuti e forzare gli utenti a eseguire nuovamente l'autenticazione.

Per informazioni sulla creazione di desktop e la registrazione di una [*Secure Attention Sequence*](../secgloss/s-gly.md) (SAS), vedere [inizializzazione di Winlogon](initializing-winlogon.md). Per informazioni sulle operazioni di timeout, vedere [operazioni di tempo di servizio della finestra di dialogo supportate](supported-dialog-box-service-time-out-operations.md). Per informazioni sull'invio di messaggi a GINA mentre viene visualizzata una finestra di dialogo, vedere [invio di messaggi a Gina](sending-messages-to-the-gina.md). Per informazioni sulle funzioni di supporto, vedere [funzioni di supporto di Winlogon](authentication-functions.md).

 

 
