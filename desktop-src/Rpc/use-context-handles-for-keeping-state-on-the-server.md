---
title: Usare gli handle di contesto per mantenere lo stato nel server
description: Usare gli handle di contesto per mantenere lo stato nel server
ms.assetid: ee511745-04cf-445d-a02b-41734aabc193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90bf14632ed1821a1a097a64951f6ca9aef751d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221489"
---
# <a name="use-context-handles-for-keeping-state-on-the-server"></a><span data-ttu-id="bd790-103">Usare gli handle di contesto per mantenere lo stato nel server</span><span class="sxs-lookup"><span data-stu-id="bd790-103">Use Context Handles for Keeping State on the Server</span></span>

<span data-ttu-id="bd790-104">**Procedura consigliata:** Ogni volta che lo stato viene mantenuto nel server tra le chiamate, utilizzare gli handle del contesto.</span><span class="sxs-lookup"><span data-stu-id="bd790-104">**Best practice:** Whenever state is kept on the server between calls, use context handles.</span></span>

<span data-ttu-id="bd790-105">Gli handle di contesto sono spesso intimidatori per i nuovi programmatori RPC e l'overhead degli handle del contesto di apprendimento potrebbe non essere inizialmente degno di sforzo.</span><span class="sxs-lookup"><span data-stu-id="bd790-105">Context handles are often intimidating for new RPC programmers, and the overhead of learning context handles may not initially appear worth the effort.</span></span> <span data-ttu-id="bd790-106">Vale la pena perché gli handle di contesto hanno soluzioni predefinite per molti problemi comuni riscontrati nella programmazione di rete che altrimenti sarebbe necessario implementare da zero.</span><span class="sxs-lookup"><span data-stu-id="bd790-106">It is worth it because context handles have built-in solutions for many common pitfalls encountered in network programming that otherwise would have to be implemented from scratch.</span></span> <span data-ttu-id="bd790-107">Informazioni sugli handle di contesto pagano i dividendi in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="bd790-107">Understanding context handles pays dividends later.</span></span>

 

 




