---
description: Winlogon mantiene lo stato della workstation usato da GINA per determinare quali azioni di autenticazione sono necessarie.
ms.assetid: e04175c4-bb43-4f76-8ceb-50282a1ebed0
title: Stati di Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fef22cdd172572b1d5032990abae929712dc0be29a926524520c7ce6f9bbfe69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915055"
---
# <a name="winlogon-states"></a>Stati di Winlogon

[*Winlogon*](../secgloss/w-gly.md) mantiene lo stato della workstation usato da [*GINA*](../secgloss/g-gly.md) per determinare quali azioni di autenticazione sono necessarie.

In qualsiasi momento, Winlogon si trova in uno dei tre stati seguenti:

-   [Stato disconnessione](#logged-off-state)
-   [Stato di accesso](#logged-on-state)
-   [Stato di blocco della workstation](#workstation-locked-state)

Questi tre stati sono illustrati nella figura seguente.

![stati winlogon](images/winlogonst.png)

## <a name="logged-off-state"></a>Logged-Off stato

Quando Winlogon è nello stato disconnesso, agli utenti viene richiesto di identificarsi e fornire informazioni di autenticazione. Se un utente fornisce informazioni corrette sull'account utente e nessuna restrizione le impedisce, l'utente è connesso e viene eseguito un programma shell (ad esempio Windows Explorer) nel desktop dell'applicazione. Winlogon viene modificato nello stato connesso.

## <a name="logged-on-state"></a>Logged-On stato

Quando Winlogon è nello stato connesso, gli utenti possono interagire con la shell, attivare altre applicazioni ed eseguire il proprio lavoro. Dallo stato connesso, gli utenti possono arrestare tutto il lavoro e disconnettersi o bloccare le workstation (lasciando tutto il lavoro sul posto). Se l'utente decide di disconnettersi, Winlogon terminerà [](../secgloss/l-gly.md) tutti i processi associati a tale sessione di accesso e la workstation sarà disponibile per un altro utente. Se invece l'utente decide di bloccare la workstation, Winlogon cambia nello stato di blocco della workstation.

## <a name="workstation-locked-state"></a>Workstation-Locked stato

Quando Winlogon è nello stato bloccato dalla workstation, viene visualizzato un desktop protetto finché l'utente non sblocca la workstation fornendo le stesse informazioni di identificazione e autenticazione dell'utente che ha eseguito l'accesso in origine o finché un amministratore non forza una disconnessione. Se la workstation è sbloccata, viene visualizzato il desktop dell'applicazione e il lavoro può riprendere. Se, tuttavia, un amministratore sblocca la workstation (fornendo le informazioni di identificazione e autenticazione di un account amministratore), i processi dell'utente connesso vengono terminati e Winlogon cambia nello stato disconnesso.

È possibile eseguire diverse azioni in ognuno degli stati di Winlogon. Una DLL GINA può implementare azioni che non fanno parte del sistema operativo Windows standard. Ad esempio, un sistema di sicurezza elevato potrebbe bloccare automaticamente una workstation ogni 10 minuti e forzare gli utenti a eseguire nuovamente l'autenticazione.

Per informazioni sulla creazione di desktop e sulla registrazione di una sequenza [*di*](../secgloss/s-gly.md) attenzione sicura, vedere [Inizializzazione di Winlogon](initializing-winlogon.md). Per informazioni sulle operazioni di timeout, vedere [Operazioni di timeout](supported-dialog-box-service-time-out-operations.md)del servizio Dialog Box supportate . Per informazioni sull'invio di messaggi a GINA mentre viene visualizzata una finestra di dialogo, vedere [Invio di messaggi a GINA](sending-messages-to-the-gina.md). Per informazioni sulle funzioni di supporto, vedere [Funzioni di supporto di Winlogon](authentication-functions.md).

 

 
