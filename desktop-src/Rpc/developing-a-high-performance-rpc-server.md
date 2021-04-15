---
title: Sviluppo di un server RPC a prestazioni elevate
description: Le informazioni contenute in questa sezione si applicano alle sequenze remote del protocollo ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ np e a Windows 2000 e Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- RPC (Remote Procedure Call), procedure consigliate, sviluppo di un server a prestazioni elevate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a18319c1f4ade80ae026b68c8f5540030b992b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473990"
---
# <a name="developing-a-high-performance-rpc-server"></a><span data-ttu-id="879e5-104">Sviluppo di un server RPC a prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="879e5-104">Developing a High Performance RPC Server</span></span>

<span data-ttu-id="879e5-105">Le informazioni contenute in questa sezione si applicano alle sequenze remote del protocollo: [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)e a Windows 2000 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="879e5-105">The information in this section applies to remote protocol sequences: [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn\_http**](/windows/desktop/Midl/ncacn-http), [**ncacn\_np**](/windows/desktop/Midl/ncacn-np), and to Windows 2000 and Windows XP.</span></span>

<span data-ttu-id="879e5-106">In questa sezione vengono illustrati tre aspetti principali delle prestazioni del server RPC:</span><span class="sxs-lookup"><span data-stu-id="879e5-106">This section addresses three primary aspects of RPC server performance:</span></span>

-   [<span data-ttu-id="879e5-107">Latenza di rete e velocità effettiva</span><span class="sxs-lookup"><span data-stu-id="879e5-107">Network Latency and Throughput</span></span>](network-latency-and-throughput.md)
-   [<span data-ttu-id="879e5-108">Scalabilità</span><span class="sxs-lookup"><span data-stu-id="879e5-108">Scalability</span></span>](scalability.md)
-   [<span data-ttu-id="879e5-109">Suggerimenti sulle prestazioni RPC varie</span><span class="sxs-lookup"><span data-stu-id="879e5-109">Miscellaneous RPC Performance Tips</span></span>](miscellaneous-rpc-performance-tips.md)

<span data-ttu-id="879e5-110">La lunghezza del percorso del codice è un'altra considerazione primaria per le prestazioni RPC.</span><span class="sxs-lookup"><span data-stu-id="879e5-110">Code path length is another primary performance consideration for RPC.</span></span> <span data-ttu-id="879e5-111">La lunghezza del percorso del codice è in genere ben riconosciuta e, poiché la letteratura e gli strumenti sono ampiamente disponibili in questo argomento, questo articolo non risolve il problema.</span><span class="sxs-lookup"><span data-stu-id="879e5-111">Code path length is generally well understood, and since literature and tools are widely available on that topic, this article does not address it.</span></span>

<span data-ttu-id="879e5-112">Una regola importante e stabilita per le prestazioni generali da ricordare considerando le prestazioni RPC è la seguente: individuare il collo di bottiglia nel sistema e risolverlo.</span><span class="sxs-lookup"><span data-stu-id="879e5-112">An important and established general performance rule to remember while considering RPC performance is this: find the bottleneck in the system, and work to resolve that.</span></span> <span data-ttu-id="879e5-113">Il collo di bottiglia del controllo potrebbe non essere la programmazione RPC e, in tal caso, l'ottimizzazione delle prestazioni in RPC non comporterà un miglioramento delle prestazioni fino a quando non verrà risolto il collo di bottiglia.</span><span class="sxs-lookup"><span data-stu-id="879e5-113">The gating bottleneck may not be the RPC programming, and if that is the case, performance tuning in RPC will not result in enhanced performance until that bottleneck is addressed.</span></span> <span data-ttu-id="879e5-114">Ad esempio, un sistema afflitto dalla contesa di risorse non necessita di un uso più efficiente della rete.</span><span class="sxs-lookup"><span data-stu-id="879e5-114">For example, a system plagued by resource contention does not need to make more efficient use of the network.</span></span>

<span data-ttu-id="879e5-115">Se il sistema viene distribuito in diversi ambienti, è consigliabile assicurarsi che tutti gli aspetti siano ben ottimizzati, in quanto ambienti diversi possono produrre colli di bottiglia delle prestazioni diversi.</span><span class="sxs-lookup"><span data-stu-id="879e5-115">If your system is deployed in various environments, it is a good idea to make sure all aspects of it are well tuned, as different environments can produce varied performance bottlenecks.</span></span>

 

 