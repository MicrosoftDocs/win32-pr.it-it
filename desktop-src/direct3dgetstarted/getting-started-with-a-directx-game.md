---
title: Introduzione a DirectX per Windows
description: La creazione di un gioco Microsoft DirectX per Windows è una sfida per un nuovo sviluppatore. In questo articolo vengono esaminati rapidamente i concetti e i passaggi necessari per iniziare lo sviluppo di un gioco con DirectX e C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae09cd127a30401ae0493f5dd770fe1e67607b45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300000"
---
# <a name="get-started-with-directx-for-windows"></a><span data-ttu-id="b9b92-104">Introduzione a DirectX per Windows</span><span class="sxs-lookup"><span data-stu-id="b9b92-104">Get started with DirectX for Windows</span></span>

<span data-ttu-id="b9b92-105">La creazione di un gioco Microsoft DirectX per Windows è una sfida per un nuovo sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="b9b92-105">Creating a Microsoft DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="b9b92-106">In questo articolo vengono esaminati rapidamente i concetti e i passaggi necessari per iniziare lo sviluppo di un gioco con DirectX e C++.</span><span class="sxs-lookup"><span data-stu-id="b9b92-106">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span>

<span data-ttu-id="b9b92-107">A questo punto, procedere con l'esercitazione.</span><span class="sxs-lookup"><span data-stu-id="b9b92-107">Let's get started.</span></span>

## <a name="what-skills-do-you-need"></a><span data-ttu-id="b9b92-108">Quali competenze sono necessarie?</span><span class="sxs-lookup"><span data-stu-id="b9b92-108">What skills do you need?</span></span>

<span data-ttu-id="b9b92-109">Per sviluppare un gioco in DirectX per Windows, è necessario disporre di alcune competenze di base.</span><span class="sxs-lookup"><span data-stu-id="b9b92-109">To develop a game in DirectX for Windows, you must have a few basic skills.</span></span> <span data-ttu-id="b9b92-110">In particolare, è necessario essere in grado di:</span><span class="sxs-lookup"><span data-stu-id="b9b92-110">Specifically, you must be able to:</span></span>

-   <span data-ttu-id="b9b92-111">Leggi e Scrivi codice C++ moderno (C++ 11 più semplice) ed è familiare con i principi di progettazione e i modelli di base di C++, come i modelli e il modello Factory.</span><span class="sxs-lookup"><span data-stu-id="b9b92-111">Read and write modern C++ code (C++11 helps the most), and be familiar with basic C++ design principles and patterns like templates and the factory model.</span></span> <span data-ttu-id="b9b92-112">È anche necessario avere familiarità con le librerie C++ comuni, come la libreria di modelli standard, e in particolare con gli operatori di cast, i tipi di puntatore e le strutture di dati della libreria di modelli standard, ad esempio std:: Vector.</span><span class="sxs-lookup"><span data-stu-id="b9b92-112">You must also be familiar with common C++ libraries like the Standard Template Library, and specifically with the casting operators, pointer types, and the standard template library data structures (such as std::vector).</span></span>
-   <span data-ttu-id="b9b92-113">Informazioni sulla geometria di base, sulla trigonometria e sull'algebra lineare.</span><span class="sxs-lookup"><span data-stu-id="b9b92-113">Understand basic geometry, trigonometry, and linear algebra.</span></span> <span data-ttu-id="b9b92-114">Gran parte del codice che si troverà negli esempi presuppone che si conoscano queste forme di matematica e le regole comuni.</span><span class="sxs-lookup"><span data-stu-id="b9b92-114">Much of the code you will find in the examples assumes you understand these forms of mathematics and their common rules.</span></span>
-   <span data-ttu-id="b9b92-115">Hanno familiarità con COM, in particolare [**Microsoft:: WRL:: ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (puntatore intelligente).</span><span class="sxs-lookup"><span data-stu-id="b9b92-115">Have familiarity with COM—especially [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (smart pointer).</span></span>
-   <span data-ttu-id="b9b92-116">Informazioni sulle fondamenta della grafica e della tecnologia grafica, in particolare grafica 3D.</span><span class="sxs-lookup"><span data-stu-id="b9b92-116">Understand the foundations of graphics and graphics technology, particularly 3D graphics.</span></span> <span data-ttu-id="b9b92-117">Sebbene DirectX abbia una propria terminologia, si basa comunque su una conoscenza ben definita dei principi grafici 3D generali.</span><span class="sxs-lookup"><span data-stu-id="b9b92-117">While DirectX itself has its own terminology, it still builds upon a well-established understanding of general 3D graphics principles.</span></span>
-   <span data-ttu-id="b9b92-118">Comprendere il concetto di ciclo di messaggi perché verrà implementato un ciclo che resta in ascolto del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="b9b92-118">Understand the concept of a message loop, because you'll be implementing a loop that listens to the Windows operating system.</span></span>

## <a name="and-were-off"></a><span data-ttu-id="b9b92-119">E ci siamo disattivati.</span><span class="sxs-lookup"><span data-stu-id="b9b92-119">And we're off!</span></span>

<span data-ttu-id="b9b92-120">Sei pronto per iniziare?</span><span class="sxs-lookup"><span data-stu-id="b9b92-120">Ready to start?</span></span> <span data-ttu-id="b9b92-121">Esaminiamo prima di tutto.</span><span class="sxs-lookup"><span data-stu-id="b9b92-121">Let's review before we head on.</span></span> <span data-ttu-id="b9b92-122">Precisamente:</span><span class="sxs-lookup"><span data-stu-id="b9b92-122">You have:</span></span>

-   <span data-ttu-id="b9b92-123">Installazione aggiornata e funzionante di Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="b9b92-123">An updated and working installation of Windows 8.1.</span></span>
-   <span data-ttu-id="b9b92-124">Installazione di [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span><span class="sxs-lookup"><span data-stu-id="b9b92-124">An installation of [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span></span>
-   <span data-ttu-id="b9b92-125">Uno spirito intrepido e il desiderio di saperne di più sullo sviluppo di giochi DirectX.</span><span class="sxs-lookup"><span data-stu-id="b9b92-125">An intrepid spirit and a desire to learn more about DirectX game development!</span></span>

## <a name="next-steps"></a><span data-ttu-id="b9b92-126">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="b9b92-126">Next steps</span></span>



|                                                                                                    |                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9b92-127">Usare le risorse del dispositivo DirectX</span><span class="sxs-lookup"><span data-stu-id="b9b92-127">Work with DirectX device resources</span></span>](work-with-dxgi.md)                                           | <span data-ttu-id="b9b92-128">Informazioni su come usare DXGI per creare un dispositivo di grafica virtualizzato e creare e configurare una catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="b9b92-128">Learn how to use DXGI to create a virtualized graphics device, and create and configure a swap chain.</span></span>     |
| [<span data-ttu-id="b9b92-129">Informazioni sulla pipeline di rendering Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="b9b92-129">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md) | <span data-ttu-id="b9b92-130">Informazioni su come collegare la classe delle risorse del dispositivo DirectX e creare usando la pipeline grafica Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b9b92-130">Learn how to hook into the DirectX device resources class, and draw using the Direct3D graphics pipeline.</span></span> |
| [<span data-ttu-id="b9b92-131">Usare shader e risorse shader</span><span class="sxs-lookup"><span data-stu-id="b9b92-131">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)               | <span data-ttu-id="b9b92-132">Informazioni su come scrivere programmi shader HLSL per le fasi della pipeline grafica Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b9b92-132">Learn how to write HLSL shader programs for Direct3D graphics pipeline stages.</span></span>                            |



 

 

 