---
description: Elenca e spiega le responsabilità di GINA.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Responsabilità di GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3481aea9f5a92a485c42fb00b43d7062012d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049976"
---
# <a name="responsibilities-of-the-gina"></a>Responsabilità di GINA

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 

Una dll [*Gina*](../secgloss/g-gly.md) ha le responsabilità seguenti:

-   Monitoraggio SAS

    GINA è responsabile del riconoscimento di una [*Secure Attention Sequence*](../secgloss/s-gly.md) (SAS), del monitoraggio degli eventi SAS e della notifica di Winlogon quando si verifica una firma di accesso condiviso. Si noti che è possibile definire più di una firma di accesso condiviso e il set di SASs definito può variare nel tempo. Ad esempio, può essere presente un set di SASs quando [*Winlogon*](../secgloss/w-gly.md) si trova nello stato disconnesso e un altro set quando si trova nello stato connesso.

    Winlogon fornisce servizi per consentire a GINA di usare la firma di accesso condiviso CTRL + ALT + CANC.

-   Elaborazione SAS

    Uno dei motivi per cui GINA può essere sostituita è fornire meccanismi di identificazione e autenticazione alternativi. A tale scopo, è necessario che GINA presenti tutte le interfacce utente derivanti dal riconoscimento di una firma di accesso condiviso. Quando nessun utente è connesso, GINA è responsabile della presentazione delle opzioni di identificazione e autenticazione, nonché di eventuali altre opzioni consentite che non vengono autenticate. Quando un utente è connesso, GINA è responsabile della presentazione delle opzioni rilevanti per l'utente, nonché dell'esecuzione di qualsiasi azione ritenuta appropriata. Ad esempio, in un sistema che include una [*Smart Card*](../secgloss/s-gly.md), potrebbe essere opportuno bloccare automaticamente la workstation se l'utente rimuove la smart card.

-   Attivazione della shell

    Quando un utente esegue l'accesso, GINA è responsabile della creazione di uno o più processi iniziali per tale utente. In questa documentazione si presuppone che questi processi iniziali presentino un'interfaccia per l'utente. Tuttavia, i processi possono essere effettivamente processi e non devono necessariamente interagire con l'utente. Questi processi sono detti *Shell utente* o solo la *Shell*. Come parte dell'attivazione della shell, GINA deve assegnare il token dell'utente appena connesso ai processi. Winlogon fornisce un servizio per aiutare la GINA ad assegnare il token.

 

 
