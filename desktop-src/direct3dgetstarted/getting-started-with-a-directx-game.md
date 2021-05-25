---
title: Introduzione a DirectX per Windows
description: La creazione di un gioco Microsoft DirectX per Windows è una sfida per un nuovo sviluppatore. Qui vengono esaminati rapidamente i concetti coinvolti e i passaggi da eseguire per iniziare a sviluppare un gioco usando DirectX e C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bac8ca2805fed9ec42faf9deda9ddd51da39685
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343586"
---
# <a name="get-started-with-directx-for-windows"></a><span data-ttu-id="74233-104">Introduzione a DirectX per Windows</span><span class="sxs-lookup"><span data-stu-id="74233-104">Get started with DirectX for Windows</span></span>

<span data-ttu-id="74233-105">La creazione di un gioco Microsoft DirectX per Windows è una sfida per un nuovo sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="74233-105">Creating a Microsoft DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="74233-106">Qui vengono esaminati rapidamente i concetti coinvolti e i passaggi da eseguire per iniziare a sviluppare un gioco usando DirectX e C++.</span><span class="sxs-lookup"><span data-stu-id="74233-106">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span>

<span data-ttu-id="74233-107">A questo punto, procedere con l'esercitazione.</span><span class="sxs-lookup"><span data-stu-id="74233-107">Let's get started.</span></span>

## <a name="what-skills-do-you-need"></a><span data-ttu-id="74233-108">Quali competenze sono necessarie?</span><span class="sxs-lookup"><span data-stu-id="74233-108">What skills do you need?</span></span>

<span data-ttu-id="74233-109">Per sviluppare un gioco in DirectX per Windows, è necessario avere alcune competenze di base.</span><span class="sxs-lookup"><span data-stu-id="74233-109">To develop a game in DirectX for Windows, you must have a few basic skills.</span></span> <span data-ttu-id="74233-110">In particolare, è necessario essere in grado di:</span><span class="sxs-lookup"><span data-stu-id="74233-110">Specifically, you must be able to:</span></span>

-   <span data-ttu-id="74233-111">Leggere e scrivere codice C++ moderno (C++11 è più utile) e acquisire familiarità con i principi e i modelli di progettazione C++ di base, ad esempio i modelli e il modello factory.</span><span class="sxs-lookup"><span data-stu-id="74233-111">Read and write modern C++ code (C++11 helps the most), and be familiar with basic C++ design principles and patterns like templates and the factory model.</span></span> <span data-ttu-id="74233-112">È anche necessario avere familiarità con le librerie C++ comuni, ad esempio la libreria di modelli standard, in particolare con gli operatori di cast, i tipi di puntatore e le strutture di dati della libreria modello standard (ad esempio std::vector).</span><span class="sxs-lookup"><span data-stu-id="74233-112">You must also be familiar with common C++ libraries like the Standard Template Library, and specifically with the casting operators, pointer types, and the standard template library data structures (such as std::vector).</span></span>
-   <span data-ttu-id="74233-113">Comprendere la geometria di base, la trigonometria e l'algebra lineare.</span><span class="sxs-lookup"><span data-stu-id="74233-113">Understand basic geometry, trigonometry, and linear algebra.</span></span> <span data-ttu-id="74233-114">Gran parte del codice che si trova negli esempi presuppone che si comprendino queste forme di matematica e le relative regole comuni.</span><span class="sxs-lookup"><span data-stu-id="74233-114">Much of the code you will find in the examples assumes you understand these forms of mathematics and their common rules.</span></span>
-   <span data-ttu-id="74233-115">Avere familiarità con COM, in particolare [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (puntatore intelligente).</span><span class="sxs-lookup"><span data-stu-id="74233-115">Have familiarity with COM—especially [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (smart pointer).</span></span>
-   <span data-ttu-id="74233-116">Comprendere le basi della tecnologia grafica e grafica, in particolare la grafica 3D.</span><span class="sxs-lookup"><span data-stu-id="74233-116">Understand the foundations of graphics and graphics technology, particularly 3D graphics.</span></span> <span data-ttu-id="74233-117">Anche se DirectX stesso ha una propria terminologia, si basa ancora su una conoscenza consolidata dei principi generali della grafica 3D.</span><span class="sxs-lookup"><span data-stu-id="74233-117">While DirectX itself has its own terminology, it still builds upon a well-established understanding of general 3D graphics principles.</span></span>
-   <span data-ttu-id="74233-118">Comprendere il concetto di ciclo di messaggi, perché verrà implementato un ciclo in ascolto sul sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="74233-118">Understand the concept of a message loop, because you'll be implementing a loop that listens to the Windows operating system.</span></span>

## <a name="and-were-off"></a><span data-ttu-id="74233-119">E siamo spenti.</span><span class="sxs-lookup"><span data-stu-id="74233-119">And we're off!</span></span>

<span data-ttu-id="74233-120">Sei pronto per iniziare?</span><span class="sxs-lookup"><span data-stu-id="74233-120">Ready to start?</span></span> <span data-ttu-id="74233-121">Si esamini prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="74233-121">Let's review before we head on.</span></span> <span data-ttu-id="74233-122">Precisamente:</span><span class="sxs-lookup"><span data-stu-id="74233-122">You have:</span></span>

-   <span data-ttu-id="74233-123">Un'installazione aggiornata e funzionante di Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="74233-123">An updated and working installation of Windows 8.1.</span></span>
-   <span data-ttu-id="74233-124">Installazione di [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span><span class="sxs-lookup"><span data-stu-id="74233-124">An installation of [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span></span>
-   <span data-ttu-id="74233-125">Un'intrepida voglia di saperne di più sullo sviluppo di giochi DirectX.</span><span class="sxs-lookup"><span data-stu-id="74233-125">An intrepid spirit and a desire to learn more about DirectX game development!</span></span>

## <a name="next-steps"></a><span data-ttu-id="74233-126">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="74233-126">Next steps</span></span>



| <span data-ttu-id="74233-127">Argomento</span><span class="sxs-lookup"><span data-stu-id="74233-127">Topic</span></span>                                                                                                   | <span data-ttu-id="74233-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74233-128">Description</span></span>                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74233-129">Usare le risorse del dispositivo DirectX</span><span class="sxs-lookup"><span data-stu-id="74233-129">Work with DirectX device resources</span></span>](work-with-dxgi.md)                                           | <span data-ttu-id="74233-130">Informazioni su come usare DXGI per creare un dispositivo grafico virtualizzato e creare e configurare una catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="74233-130">Learn how to use DXGI to create a virtualized graphics device, and create and configure a swap chain.</span></span>     |
| [<span data-ttu-id="74233-131">Informazioni sulla pipeline di rendering Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="74233-131">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md) | <span data-ttu-id="74233-132">Informazioni su come eseguire l'hook alla classe delle risorse del dispositivo DirectX e disegnare usando la pipeline grafica Direct3D.</span><span class="sxs-lookup"><span data-stu-id="74233-132">Learn how to hook into the DirectX device resources class, and draw using the Direct3D graphics pipeline.</span></span> |
| [<span data-ttu-id="74233-133">Usare shader e risorse shader</span><span class="sxs-lookup"><span data-stu-id="74233-133">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)               | <span data-ttu-id="74233-134">Informazioni su come scrivere programmi shader HLSL per le fasi della pipeline grafica Direct3D.</span><span class="sxs-lookup"><span data-stu-id="74233-134">Learn how to write HLSL shader programs for Direct3D graphics pipeline stages.</span></span>                            |



 

 

 