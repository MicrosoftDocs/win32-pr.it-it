---
title: Ordinamento causale delle chiamate asincrone
description: In un'applicazione RPC asincrona un thread client può effettuare una seconda chiamata asincrona su un handle di associazione prima del completamento di una chiamata precedente effettuata su tale handle.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbafc5f9166d28a80d514abd4ebea20ab01ea32f542561e2108feae4a5769458
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932295"
---
# <a name="causal-ordering-of-asynchronous-calls"></a>Ordinamento causale delle chiamate asincrone

In un'applicazione RPC asincrona un thread client può effettuare una seconda chiamata asincrona su un handle di associazione prima del completamento di una chiamata precedente effettuata su tale handle. La libreria di runtime RPC gestisce questa situazione nel modo seguente:

-   Il meccanismo RPC asincrono garantisce che le chiamate asincrone effettuate sullo stesso handle di associazione, nello stesso thread, allo stesso livello di sicurezza, siano inviati nell'ordine in cui sono state effettuate. L'esecuzione effettiva delle chiamate può non essere in ordine.
-   Come per le chiamate sincrone, le chiamate di procedura remota asincrone da thread client diversi vengono eseguite contemporaneamente.
-   Se una chiamata asincrona da un'applicazione client è seguita da una o più chiamate sincrone, la chiamata asincrona può essere eseguita durante l'esecuzione delle chiamate sincrone. Indipendentemente dallo stato della chiamata asincrona, le chiamate sincrone vengono eseguite nell'ordine in cui vengono ricevute dal server.
-   Se un'applicazione client seleziona l'ordinamento noncausale per un handle di associazione specifico, disabilita la serializzazione per tale handle. Le applicazioni abilitano l'ordinamento noncausale chiamando [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) con il parametro *Option* impostato su RPC \_ C OPT BINDING \_ \_ \_ NONCAUSAL   e il parametro OptionValue impostato su TRUE. Per informazioni dettagliate, vedere [Costanti delle opzioni di associazione](binding-option-constants.md).

 

 




