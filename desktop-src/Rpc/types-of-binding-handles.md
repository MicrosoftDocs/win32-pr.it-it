---
title: Tipi di handle di associazione
description: Gli handle di associazione possono essere automatici, impliciti o espliciti.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a09b858dfc677d06cf5885dc7a5f7a6ba599eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045076"
---
# <a name="types-of-binding-handles"></a><span data-ttu-id="ab924-103">Tipi di handle di associazione</span><span class="sxs-lookup"><span data-stu-id="ab924-103">Types of Binding Handles</span></span>

<span data-ttu-id="ab924-104">Gli handle di associazione possono essere automatici, impliciti o espliciti.</span><span class="sxs-lookup"><span data-stu-id="ab924-104">Binding handles can be automatic, implicit, or explicit.</span></span> <span data-ttu-id="ab924-105">Si differenziano per la quantità di controllo che l'applicazione ha sul processo di binding.</span><span class="sxs-lookup"><span data-stu-id="ab924-105">They differ in the amount of control the application has over the binding process.</span></span> <span data-ttu-id="ab924-106">Come suggerisce il nome, l'associazione automatica gestisce l'associazione automatica.</span><span class="sxs-lookup"><span data-stu-id="ab924-106">As the name suggests, automatic binding handles automate binding.</span></span> <span data-ttu-id="ab924-107">Le applicazioni client e server non necessitano di codice per gestire il processo di associazione.</span><span class="sxs-lookup"><span data-stu-id="ab924-107">The client and server applications do not need code to handle the binding process.</span></span> <span data-ttu-id="ab924-108">Gli handle di associazione impliciti consentono ai programmi client di configurare l'handle di associazione prima che l'associazione venga svolta.</span><span class="sxs-lookup"><span data-stu-id="ab924-108">Implicit binding handles allow client programs to configure the binding handle before the binding takes place.</span></span> <span data-ttu-id="ab924-109">Una volta che il client ha stabilito un'associazione, la libreria di runtime RPC gestisce il resto.</span><span class="sxs-lookup"><span data-stu-id="ab924-109">After the client establishes a binding, the RPC run-time library handles the rest.</span></span> <span data-ttu-id="ab924-110">Gli handle di binding espliciti spostano il controllo completo sul processo di associazione nel codice sorgente del client e dei programmi server.</span><span class="sxs-lookup"><span data-stu-id="ab924-110">Explicit binding handles move complete control over the binding process into the source code of the client and the server programs.</span></span> <span data-ttu-id="ab924-111">Con questo controllo si presenta una maggiore complessità.</span><span class="sxs-lookup"><span data-stu-id="ab924-111">With this control comes increased complexity.</span></span> <span data-ttu-id="ab924-112">L'applicazione deve chiamare funzioni RPC per gestire l'associazione.</span><span class="sxs-lookup"><span data-stu-id="ab924-112">Your application must call RPC functions to manage the binding.</span></span> <span data-ttu-id="ab924-113">Non viene eseguita automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ab924-113">It does not happen automatically.</span></span> <span data-ttu-id="ab924-114">Sono consigliati gli handle di binding espliciti.</span><span class="sxs-lookup"><span data-stu-id="ab924-114">Explicit binding handles are recommended.</span></span>

<span data-ttu-id="ab924-115">Nel diagramma seguente vengono illustrate le differenze tra gli handle di binding automatici, impliciti ed espliciti.</span><span class="sxs-lookup"><span data-stu-id="ab924-115">The following diagram illustrates the differences between automatic, implicit, and explicit binding handles.</span></span>

![differenze tra handle di binding automatici, impliciti ed espliciti](images/bhand.png)

<span data-ttu-id="ab924-117">Inoltre, ogni handle di associazione è primitivo o personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ab924-117">In addition, every binding handle is either primitive or custom.</span></span> <span data-ttu-id="ab924-118">Ogni tipo di handle di associazione viene discusso negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab924-118">Each type of binding handle is discussed in the following topics:</span></span>

-   [<span data-ttu-id="ab924-119">Handle di binding automatici</span><span class="sxs-lookup"><span data-stu-id="ab924-119">Automatic Binding Handles</span></span>](automatic-binding-handles.md)
-   [<span data-ttu-id="ab924-120">Handle di binding impliciti</span><span class="sxs-lookup"><span data-stu-id="ab924-120">Implicit Binding Handles</span></span>](implicit-binding-handles.md)
-   [<span data-ttu-id="ab924-121">Handle di binding espliciti</span><span class="sxs-lookup"><span data-stu-id="ab924-121">Explicit Binding Handles</span></span>](explicit-binding-handles.md)
-   [<span data-ttu-id="ab924-122">Handle di binding primitivi e personalizzati</span><span class="sxs-lookup"><span data-stu-id="ab924-122">Primitive and Custom Binding Handles</span></span>](primitive-and-custom-binding-handles.md)

 

 




