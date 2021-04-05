---
title: Infrastruttura WinEvents
description: Il sistema operativo Microsoft Windows include una funzionalità, denominata WinEvents, che consente ai processi e alle applicazioni in esecuzione sul desktop di Windows di scambiare determinati tipi di informazioni.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8846582a6d18f304cc08e3cb13ddb444cb278d7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "103720016"
---
# <a name="winevents"></a>WinEvents

Il sistema operativo Microsoft Windows include una funzionalità, denominata *winEvents*, che consente ai processi e alle applicazioni in esecuzione sul desktop di Windows di scambiare determinati tipi di informazioni. Gli strumenti di accessibilità che usano automazione interfaccia utente Microsoft e Microsoft Active Accessibility sono tra gli utenti principali del WinEvents.

Nel contesto dell'accessibilità, i provider di automazione interfaccia utente e i server Microsoft Active Accessibility usano WinEvents per notificare ai client le modifiche apportate all'interfaccia utente di un'applicazione, ad esempio quando un elemento dell'interfaccia utente è stato creato o eliminato definitivamente oppure quando il nome, lo stato o il valore di un elemento è stato modificato.

In questa sezione vengono forniti suggerimenti, linee guida ed esempi per aiutare i client a gestire WinEvents e a consentire ai server di determinare quando attivare il WinEvent appropriato.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Che cosa sono WinEvents?](what-are-winevents.md)
-   [Registrazione di una funzione hook](registering-a-hook-function.md)
-   [Eventi a livello di sistema e di Object-Level](system-level-and-object-level-events.md)
-   [Funzioni hook nel contesto e out-of-context](in-context-and-out-of-context-hook-functions.md)
-   [Protezione contro la rientranza nelle funzioni hook](guarding-against-reentrancy-in-hook-functions.md)
-   [Allocazione di ID WinEvent](allocation-of-winevent-ids.md)

Per una panoramica del processo di notifica degli eventi in Microsoft Active Accessibility, vedere [winEvents](winevents-overview.md) nella [Panoramica tecnica](technical-overview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Infrastruttura comune](common-infrastructure.md)
</dt> </dl>

 

 




