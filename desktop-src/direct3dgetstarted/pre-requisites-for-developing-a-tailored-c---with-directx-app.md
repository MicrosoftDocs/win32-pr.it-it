---
title: Prerequisiti per lo sviluppo con DirectX
description: Quando si inizia a sviluppare un'app di Windows con DirectX, tenere presenti i prerequisiti in questa pagina. Sono incluse le tecnologie che è necessario tenere presente prima di approfondire il problema.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- App DirectX, prerequisiti
- App DirectX, app di Windows Store
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5e09484bef67546047214702fab7d2d0a5c48d
ms.sourcegitcommit: 6394972f1e8b01229db602469df6bb137e31d776
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/16/2020
ms.locfileid: "104474717"
---
# <a name="prerequisites-for-developing-with-directx"></a><span data-ttu-id="9b5ce-106">Prerequisiti per lo sviluppo con DirectX</span><span class="sxs-lookup"><span data-stu-id="9b5ce-106">Prerequisites for developing with DirectX</span></span>

<span data-ttu-id="9b5ce-107">Quando si inizia a sviluppare un'app di Windows con DirectX, tenere presenti i prerequisiti in questa pagina.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-107">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="9b5ce-108">Sono incluse le tecnologie che è necessario tenere presente prima di approfondire il problema.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-108">This includes the technologies you need to know before you dive in.</span></span>

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a><span data-ttu-id="9b5ce-109">Cosa si deve sapere per sviluppare un gioco Windows con DirectX?</span><span class="sxs-lookup"><span data-stu-id="9b5ce-109">What should I know to develop a Windows game using DirectX?</span></span>

<span data-ttu-id="9b5ce-110">Prima di iniziare a sviluppare un'app di Windows Store con DirectX, è necessario saper programmare in Windows con C++.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-110">Before you start to develop a Windows Store app using DirectX, you need to know how to program in Windows with C++.</span></span> <span data-ttu-id="9b5ce-111">Le app di Windows che usano DirectX sono sviluppate a un basso livello di programmazione, il che significa che l'utente sarà esposto a numerose funzionalità del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-111">Windows apps using DirectX are developed at a low level of programming, which means that you will be exposed to many features of the operating system.</span></span> <span data-ttu-id="9b5ce-112">Sono inclusi la gestione della memoria e delle risorse e l'interfaccia per il dispositivo grafico stesso.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-112">These include memory and resource management, and the interface for the graphics device itself.</span></span> <span data-ttu-id="9b5ce-113">Se non si ha familiarità con il gioco o lo sviluppo di app grafiche, è possibile trovare questo problema.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-113">If you are new to game or graphics app development, you may find this challenging.</span></span> <span data-ttu-id="9b5ce-114">Tuttavia, è anche possibile ritenerlo, perché la formazione per lo sviluppo di giochi a questo livello crea più possibilità per la progettazione e lo sviluppo di app per giochi e grafica.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-114">But you will also find it rewarding, because learning game development at this level creates far, far greater possibilities for game and graphics app design and development.</span></span>

<span data-ttu-id="9b5ce-115">Sarà anche necessario comprendere le nozioni di base della programmazione grafica 2D e 3D e della matematica, perché molte delle API da usare sono state sviluppate tenendo conto di questi principi.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-115">You'll also need to understand the basics of 2D and 3D graphics programming and mathematics, because many of the APIs you'll use were developed with these principles in mind.</span></span> <span data-ttu-id="9b5ce-116">Se si ha familiarità con le operazioni sottostanti, sarà più semplice comprenderne i parametri e i risultati.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-116">It'll be easier for you to understand their parameters and results if you are familiar with the operations behind them.</span></span>

<span data-ttu-id="9b5ce-117">Come minimo, è necessario comprendere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="9b5ce-117">At a minimum, you should have a grasp of the following:</span></span>

-   <span data-ttu-id="9b5ce-118">Programmazione di Windows C/C++.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-118">Windows C/C++ programming.</span></span> <span data-ttu-id="9b5ce-119">Ciò significa che è possibile comprendere i puntatori e i riferimenti, gli eventi e i callback e, forse, alcune librerie comuni come ATL.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-119">This means that you understand pointers and references, events and callbacks, and perhaps a few of the common libraries like ATL.</span></span>
-   <span data-ttu-id="9b5ce-120">Programmazione Win32.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-120">Win32 programming.</span></span> <span data-ttu-id="9b5ce-121">È possibile comprendere come vengono create le finestre e come vengono elaborati gli eventi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-121">You understand how windows are created, and how user interface events are processed.</span></span> <span data-ttu-id="9b5ce-122">Si comprende anche un po' di API Win32 COM ed essenziali.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-122">You also understand a little bit about COM and essential Win32 APIs.</span></span>
-   <span data-ttu-id="9b5ce-123">Algebra lineare e trigonometria.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-123">Linear algebra and trigonometry.</span></span> <span data-ttu-id="9b5ce-124">Sebbene non sia fondamentale, si avrà un tempo più semplice se si ha familiarità con i concetti di queste due discipline matematiche, perché costituiscono la base di gran parte della programmazione grafica 3D.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-124">While not essential, you'll have an easier time if you are familiar with concepts from these two math disciplines, because they are the foundation of much of 3D graphics programming.</span></span>
-   <span data-ttu-id="9b5ce-125">Terminologia e concetti grafici di base, ad esempio bitmap, trame, vertici, mesh e Viewport.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-125">Basic graphics terminology and concepts, such as bitmaps, textures, vertices, meshes, and viewports.</span></span>

## <a name="what-does-directx-provide-me"></a><span data-ttu-id="9b5ce-126">Che cosa offre DirectX?</span><span class="sxs-lookup"><span data-stu-id="9b5ce-126">What does DirectX provide me?</span></span>

<span data-ttu-id="9b5ce-127">DirectX è il set principale di API grafiche che verrà usato per sviluppare giochi di Windows.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-127">DirectX is the primary set of graphics APIs you'll use to develop Windows games.</span></span> <span data-ttu-id="9b5ce-128">Di seguito sono riportate le categorie di funzionalità con cui è necessario acquisire familiarità quando si decide come sviluppare il gioco.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-128">Here are the categories of features that you must become familiar with when you decide how to develop your game.</span></span>



| <span data-ttu-id="9b5ce-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="9b5ce-129">Library</span></span>     | <span data-ttu-id="9b5ce-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b5ce-130">Description</span></span>                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5ce-131">Direct3D</span><span class="sxs-lookup"><span data-stu-id="9b5ce-131">Direct3D</span></span>    | <span data-ttu-id="9b5ce-132">Un set di librerie potente, orientato alle prestazioni e con accelerazione hardware per il rendering di immagini 3D.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-132">A powerful, performance-oriented, hardware-accelerated set of libraries for rendering 3D graphics.</span></span>                                              |
| <span data-ttu-id="9b5ce-133">Direct2D</span><span class="sxs-lookup"><span data-stu-id="9b5ce-133">Direct2D</span></span>    | <span data-ttu-id="9b5ce-134">Set di librerie grafiche 2D per la bitmap con accelerazione hardware e il disegno vettoriale 2D.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-134">A set of 2D graphics libraries for hardware-accelerated bitmap and vector 2D drawing.</span></span>                                                           |
| <span data-ttu-id="9b5ce-135">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="9b5ce-135">DirectXMath</span></span> | <span data-ttu-id="9b5ce-136">Raccolta di operazioni matematiche comuni e ottimizzate utilizzate in grafica 2D e 3D, ad esempio operazioni di vettori e matrici.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-136">A library of common, optimized math operations used in 2D and 3D graphics, such as vector and matrix operations.</span></span>                                |
| <span data-ttu-id="9b5ce-137">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="9b5ce-137">DirectWrite</span></span> | <span data-ttu-id="9b5ce-138">Libreria di rendering e di API di layout di testo 2D.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-138">A library of 2D text rendering and layout APIs.</span></span> <span data-ttu-id="9b5ce-139">Supporta sia l'accelerazione hardware che la rasterizzazione del software.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-139">It supports both hardware acceleration and software rasterization.</span></span>                              |
| <span data-ttu-id="9b5ce-140">XAudio2</span><span class="sxs-lookup"><span data-stu-id="9b5ce-140">XAudio2</span></span>     | <span data-ttu-id="9b5ce-141">API audio multipiattaforma di basso livello per Microsoft Windows che fornisce un'elaborazione dei segnali e una base di mixaggio audio per lo sviluppo di giochi.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-141">A low-level, cross-platform audio API for Microsoft Windows that provides a signal processing and audio mixing foundation for game development.</span></span> |
| <span data-ttu-id="9b5ce-142">XInput</span><span class="sxs-lookup"><span data-stu-id="9b5ce-142">XInput</span></span>      | <span data-ttu-id="9b5ce-143">Raccolta che supporta vari controlli di gioco tradizionali, con particolare attenzione al modello di controller Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-143">A library that supports various traditional gaming controls, with an emphasis on the Xbox 360 controller model.</span></span>                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a><span data-ttu-id="9b5ce-144">Quali strumenti sono necessari per sviluppare un gioco Windows con DirectX?</span><span class="sxs-lookup"><span data-stu-id="9b5ce-144">What tools do I need to develop a Windows game with DirectX?</span></span>

<span data-ttu-id="9b5ce-145">Per iniziare a usare questa esercitazione, è necessario:</span><span class="sxs-lookup"><span data-stu-id="9b5ce-145">To get started with this tutorial, you need:</span></span>

-   <span data-ttu-id="9b5ce-146">Windows 8.1 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9b5ce-146">Windows 8.1 or greater</span></span>
-   <span data-ttu-id="9b5ce-147">Microsoft Visual Studio 2013 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9b5ce-147">Microsoft Visual Studio 2013 or greater</span></span>

 

 




