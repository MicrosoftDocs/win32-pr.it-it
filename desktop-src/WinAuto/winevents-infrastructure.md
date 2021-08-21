---
title: Infrastruttura WinEvents
description: Il sistema operativo Microsoft Windows include una funzionalità, denominata WinEvents, che consente ai processi e alle applicazioni in esecuzione sul desktop Windows di scambiare determinati tipi di informazioni.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8662cdcbfa9546ce04dc787e7089f68ba1c03137c41067c20792f7da111cf2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563286"
---
# <a name="winevents"></a>WinEvents

Il sistema operativo Microsoft Windows include una funzionalità, denominata *WinEvents,* che consente ai processi e alle applicazioni in esecuzione sul desktop Windows di scambiare determinati tipi di informazioni. Gli strumenti di accessibilità che usano Microsoft Automazione interfaccia utente e Microsoft Active Accessibility sono tra gli utenti principali di WinEvents.

Nel contesto dell'accessibilità, i provider Automazione interfaccia utente e i server Microsoft Active Accessibility usano WinEvents per notificare ai client le modifiche nell'interfaccia utente di un'applicazione, ad esempio quando un elemento dell'interfaccia utente è stato creato o eliminato o quando è stato modificato il nome, lo stato o il valore di un elemento.

In questa sezione vengono forniti suggerimenti, linee guida ed esempi per aiutare i client a gestire WinEvent e a determinare quando attivare l'evento WinEvent appropriato.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Che cosa sono gli eventi WinEvent?](what-are-winevents.md)
-   [Registrazione di una funzione Hook](registering-a-hook-function.md)
-   [Eventi a livello di sistema e Object-Level eventi](system-level-and-object-level-events.md)
-   [Funzioni hook in contesto e fuori contesto](in-context-and-out-of-context-hook-functions.md)
-   [Protezione dalla reentrancy nelle funzioni hook](guarding-against-reentrancy-in-hook-functions.md)
-   [Allocazione di ID WinEvent](allocation-of-winevent-ids.md)

Per una panoramica del processo di notifica degli eventi in Microsoft Active Accessibility, vedere [WinEvents](winevents-overview.md) nella [panoramica tecnica](technical-overview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Infrastruttura comune](common-infrastructure.md)
</dt> </dl>

 

 




