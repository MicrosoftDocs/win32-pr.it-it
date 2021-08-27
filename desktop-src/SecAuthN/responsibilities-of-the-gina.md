---
description: Elenca e spiega le responsabilità di GINA.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Responsabilità di GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28e4d2189d1d4258566a5e4baab357dc446a8f1c4ea409d7af328a85bf84c217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919039"
---
# <a name="responsibilities-of-the-gina"></a>Responsabilità di GINA

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 

Una [*DLL GINA*](../secgloss/g-gly.md) ha le responsabilità seguenti:

-   Monitoraggio della firma di accesso condiviso

    L'account DIA è responsabile del riconoscimento di una sequenza di attenzione [*sicura,*](../secgloss/s-gly.md) del monitoraggio degli eventi di firma di accesso condiviso e della notifica a Winlogon quando si è verificata una firma di accesso condiviso. Si noti che è possibile definire più di una firma di accesso condiviso e che il set di sass definiti può cambiare nel tempo. Ad esempio, può essere presente un set di sass quando [*Winlogon*](../secgloss/w-gly.md) è nello stato disconnesso e un altro set quando è nello stato connesso.

    Winlogon fornisce servizi per facilitare l'uso della firma di accesso condiviso CTRL+ALT+CANC.

-   Elaborazione della firma di accesso condiviso

    Uno dei motivi per cui è possibile sostituire l'applicazione GINA è fornire meccanismi di identificazione e autenticazione alternativi. A tale scopo, GINA deve presentare tutte le interfacce utente risultanti dal riconoscimento di una firma di accesso condiviso. Quando nessun utente è connesso, GINA è responsabile della presentazione delle opzioni di identificazione e autenticazione, nonché di qualsiasi altra opzione consentita non autenticata. Quando un utente è connesso, l'istanza di GINA è responsabile della presentazione delle opzioni pertinenti all'utente e dell'esecuzione di qualsiasi azione ritenuta appropriata. Ad esempio, in un sistema che include un [*smart card*](../secgloss/s-gly.md), potrebbe essere appropriato bloccare automaticamente la workstation se l'utente rimuove la smart card.

-   Attivazione della shell

    Quando un utente accede, l'istanza di GINA è responsabile della creazione di uno o più processi iniziali per tale utente. In questa documentazione si presuppone che questi processi iniziali presentino un'interfaccia all'utente. Tuttavia, i processi possono essere effettivamente qualsiasi processo e non devono necessariamente interagire con l'utente. Questi processi vengono definiti shell utente *o* semplicemente *shell*. Come parte dell'attivazione della shell, l'istanza di GINA deve assegnare il token dell'utente appena connesso ai processi. Winlogon fornisce un servizio per assistere l'istanza di GINA nell'assegnazione del token.

 

 
