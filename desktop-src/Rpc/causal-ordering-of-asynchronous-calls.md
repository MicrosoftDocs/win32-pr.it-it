---
title: Ordinamento causale di chiamate asincrone
description: In un'applicazione RPC asincrona è possibile che un thread client effettui una seconda chiamata asincrona su un handle di binding prima del completamento di una precedente chiamata eseguita su tale handle.
ms.assetid: 69beb3a4-39ae-4e3f-bb7d-31519278334d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754ae4733e5a3936bdd28fef72b9560fb9c9dfcd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044635"
---
# <a name="causal-ordering-of-asynchronous-calls"></a>Ordinamento causale di chiamate asincrone

In un'applicazione RPC asincrona è possibile che un thread client effettui una seconda chiamata asincrona su un handle di binding prima del completamento di una precedente chiamata eseguita su tale handle. La libreria di runtime RPC gestisce questa situazione come segue:

-   Il meccanismo RPC asincrono garantisce che le chiamate asincrone effettuate sullo stesso handle di associazione sullo stesso thread, allo stesso livello di sicurezza, vengano inviate nell'ordine in cui sono state effettuate. L'esecuzione effettiva delle chiamate può non essere eseguita in ordine.
-   Come per le chiamate sincrone, le chiamate asincrone a procedure remote da thread client diversi vengono eseguite simultaneamente.
-   Se una chiamata asincrona da un'applicazione client è seguita da una o più chiamate sincrone, la chiamata asincrona può essere eseguita durante l'esecuzione delle chiamate sincrone. Indipendentemente dallo stato della chiamata asincrona, le chiamate sincrone vengono eseguite nell'ordine in cui vengono ricevute dal server.
-   Se un'applicazione client seleziona un ordinamento non causale per un particolare handle di associazione, Disabilita la serializzazione per tale handle. Le applicazioni abilitano l'ordinamento non causale chiamando [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) con il parametro *Option* impostato su RPC \_ C \_ opt \_ binding \_ noncausale e il parametro *OptionValue* impostato su **true**. Per informazioni dettagliate, vedere [costanti delle opzioni di binding](binding-option-constants.md).

 

 




