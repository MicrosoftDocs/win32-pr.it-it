---
title: Svantaggi
description: Svantaggi
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a22e409414a1df60e2dd9dff3adbfc6000b953a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516006"
---
# <a name="disadvantages"></a><span data-ttu-id="2c46c-103">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="2c46c-103">Disadvantages</span></span>

<span data-ttu-id="2c46c-104">I server in-process forniscono la velocità e le dimensioni vantaggiose di un gestore di oggetti con la funzionalità di modifica di un server locale.</span><span class="sxs-lookup"><span data-stu-id="2c46c-104">In-process servers provide the speed and size advantage of an object handler with the editing capability of a local server.</span></span> <span data-ttu-id="2c46c-105">Quindi, perché scegliere di implementare l'applicazione OLE come server locale anziché come server in-process?</span><span class="sxs-lookup"><span data-stu-id="2c46c-105">So why would you ever choose to implement your OLE application as a local server rather than an in-process server?</span></span> <span data-ttu-id="2c46c-106">Esistono diversi motivi:</span><span class="sxs-lookup"><span data-stu-id="2c46c-106">There are several reasons:</span></span>

-   <span data-ttu-id="2c46c-107">Sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2c46c-107">Security.</span></span> <span data-ttu-id="2c46c-108">Solo un server locale ha lo spazio degli indirizzi isolato rispetto a quello del client.</span><span class="sxs-lookup"><span data-stu-id="2c46c-108">Only a local server has its address space isolated from that of the client.</span></span> <span data-ttu-id="2c46c-109">Un server in-process condivide lo spazio di indirizzi e il contesto di processo del client e pertanto può essere meno affidabile in caso di errori o di programmazione dannosa.</span><span class="sxs-lookup"><span data-stu-id="2c46c-109">An in-process server shares the address space and process context of the client and can therefore be less robust in the face of faults or malicious programming.</span></span>
-   <span data-ttu-id="2c46c-110">Granularità.</span><span class="sxs-lookup"><span data-stu-id="2c46c-110">Granularity.</span></span> <span data-ttu-id="2c46c-111">Un server locale può ospitare più istanze del relativo oggetto in molti client diversi, condividendo lo stato del server tra oggetti in più client in modi che sarebbero difficili o impossibili se implementati come server in-process, che è semplicemente una DLL caricata in ogni client.</span><span class="sxs-lookup"><span data-stu-id="2c46c-111">A local server can host multiple instances of its object across many different clients, sharing server state between objects in multiple clients in ways that would be difficult or impossible if implemented as an in-process server, which is simply a DLL loaded into each client.</span></span>
-   <span data-ttu-id="2c46c-112">Compatibilità.</span><span class="sxs-lookup"><span data-stu-id="2c46c-112">Compatibility.</span></span> <span data-ttu-id="2c46c-113">Se si sceglie di implementare un server in-process, si rinuncia alla compatibilità con OLE 1, che non supporta tali server.</span><span class="sxs-lookup"><span data-stu-id="2c46c-113">If you choose to implement an in-process server, you relinquish compatibility with OLE 1, which does not support such servers.</span></span> <span data-ttu-id="2c46c-114">Questo non è un aspetto da considerare per molti sviluppatori, ma, in caso contrario, si tratta di un problema critico.</span><span class="sxs-lookup"><span data-stu-id="2c46c-114">This will not be a consideration for many developers, but if it is, then it is of critical concern.</span></span>
-   <span data-ttu-id="2c46c-115">Impossibilità di supportare i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="2c46c-115">Inability to support links.</span></span> <span data-ttu-id="2c46c-116">Un server in-process non può fungere da origine di collegamento.</span><span class="sxs-lookup"><span data-stu-id="2c46c-116">An in-process server cannot serve as a link source.</span></span> <span data-ttu-id="2c46c-117">Poiché una DLL non può essere eseguita da sola, non può creare un oggetto file a cui essere collegato.</span><span class="sxs-lookup"><span data-stu-id="2c46c-117">Since a DLL cannot run by itself, it cannot create a file object to be linked to.</span></span>

<span data-ttu-id="2c46c-118">Nonostante questi svantaggi, un server in-process può essere un'ottima scelta per la velocità e le dimensioni, se è adatto a tutti gli altri requisiti.</span><span class="sxs-lookup"><span data-stu-id="2c46c-118">Despite these disadvantages, an in-process server can be an excellent choice for its speed and size — if it fits all your other requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c46c-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c46c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c46c-120">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="2c46c-120">Advantages</span></span>](advantages.md)
</dt> <dt>

[<span data-ttu-id="2c46c-121">Server in-process</span><span class="sxs-lookup"><span data-stu-id="2c46c-121">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




