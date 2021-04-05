---
title: Creare la prima app di Windows con DirectX
description: Questa sezione descrive il motivo per cui si usa il modello C++ per lo sviluppo di applicazioni Windows Store e fornisce esercitazioni e procedure di base per iniziare a sviluppare app DirectX.
ms.assetid: b632ba9c-1c30-4d21-ac79-7f2a193956fe
keywords:
- App DirectX, Guida introduttiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5e3afed57244789c0e3e06ab71ec39e581305c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707153"
---
# <a name="create-your-first-windows-app-using-directx"></a><span data-ttu-id="9795b-104">Creare la prima app di Windows con DirectX</span><span class="sxs-lookup"><span data-stu-id="9795b-104">Create your first Windows app using DirectX</span></span>

<span data-ttu-id="9795b-105">Se si conosce DirectX, è possibile sviluppare un'app DirectX usando C++ nativo e HLSL per sfruttare al meglio l'hardware grafico.</span><span class="sxs-lookup"><span data-stu-id="9795b-105">If you know DirectX, you can develop a DirectX app using native C++ and HLSL to take full advantage of graphics hardware.</span></span>

<span data-ttu-id="9795b-106">Usare questa esercitazione di base per iniziare a sviluppare app DirectX, quindi usare la roadmap per continuare a esplorare DirectX.</span><span class="sxs-lookup"><span data-stu-id="9795b-106">Use this basic tutorial to get started with DirectX app development, then use the roadmap to continue exploring DirectX.</span></span>

## <a name="windows-desktop-app-with-c-and-directx"></a><span data-ttu-id="9795b-107">App desktop di Windows con C++ e DirectX</span><span class="sxs-lookup"><span data-stu-id="9795b-107">Windows desktop app with C++ and DirectX</span></span>

<span data-ttu-id="9795b-108">Un'app desktop di Windows con DirectX è un'app sviluppata con API C++ e DirectX native.</span><span class="sxs-lookup"><span data-stu-id="9795b-108">A Windows desktop app with DirectX is an app developed using native C++ and DirectX APIs.</span></span> <span data-ttu-id="9795b-109">Questo modello è più complesso di un'app scritta in un Framework gestito, ma offre una maggiore flessibilità e un maggiore accesso alle risorse di sistema, soprattutto ai dispositivi grafici.</span><span class="sxs-lookup"><span data-stu-id="9795b-109">This model is more complex than an app written in a managed framework, but it provides greater flexibility and greater access to system resources especially graphics devices.</span></span> <span data-ttu-id="9795b-110">Quindi, si tratta di un modello efficace per gli sviluppatori esperti.</span><span class="sxs-lookup"><span data-stu-id="9795b-110">So, it is a good model for the experienced developer.</span></span>

## <a name="why-develop-a-windows-app-with-directx"></a><span data-ttu-id="9795b-111">Perché sviluppare un'app di Windows con DirectX?</span><span class="sxs-lookup"><span data-stu-id="9795b-111">Why develop a Windows app with DirectX?</span></span>

<span data-ttu-id="9795b-112">La risposta è semplice: si vuole creare un gioco con un uso intensivo di grafica o multimediale e può usare le funzionalità supportate da molti dispositivi grafici.</span><span class="sxs-lookup"><span data-stu-id="9795b-112">The answer is simple: you want to make a game that is graphics- or multimedia-intensive, and can use the features that many graphics devices support.</span></span> <span data-ttu-id="9795b-113">Questo non è facile se non si ha familiarità con lo sviluppo di giochi o lo sviluppo di Windows e C/C++, ma c'è una buona notizia: DirectX 11 è ancora la versione più semplice e coesa di Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="9795b-113">This won't be easy if you are new to game development or to Windows development and C/C++, but there's some good news: DirectX 11 is the simplest and most cohesive version of Microsoft DirectX yet.</span></span> <span data-ttu-id="9795b-114">È anche il più potente e ricco di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="9795b-114">It's also the most powerful and feature-rich.</span></span> <span data-ttu-id="9795b-115">Se l'obiettivo è quello di padroneggiare lo sviluppo di giochi e apprendere le tecniche di rendering più avanzate, DirectX può fornire la possibilità di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="9795b-115">If your goal is to master game development and learn the most advanced rendering techniques, then DirectX can provide the opportunity for you to do that.</span></span>

<span data-ttu-id="9795b-116">Ciò premesso, la pianificazione del gioco o dell'app interattiva in tempo reale è essenziale.</span><span class="sxs-lookup"><span data-stu-id="9795b-116">That said, planning your game (or interactive, real-time app) is essential.</span></span> <span data-ttu-id="9795b-117">Se non si ha familiarità con lo sviluppo di giochi e se il gioco non prevede requisiti grafici complessi, provare a svilupparlo invece con .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="9795b-117">If you are new to game development, and your game doesn't have demanding graphics requirements, consider developing it with the .NET framework instead.</span></span> <span data-ttu-id="9795b-118">Sono inoltre disponibili molti pacchetti di sviluppo di giochi e grafica "middleware" per le piattaforme Windows e alcuni non richiedono competenze di programmazione significative.</span><span class="sxs-lookup"><span data-stu-id="9795b-118">Also, many "middleware" graphics and game development packages are available for Windows platforms, and some do not require significant programming skills.</span></span>

<span data-ttu-id="9795b-119">Chi è sicuro o semplicemente sogna di creare un gioco con grafica ad alta fedeltà (o un'app con contenuto grafico complesso), quindi leggere.</span><span class="sxs-lookup"><span data-stu-id="9795b-119">If you are confident, or simply have a dream of making a game with high-fidelity graphics (or an app with complex graphics content), then read on!</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9795b-120">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="9795b-120">In this section</span></span>



| <span data-ttu-id="9795b-121">Argomento</span><span class="sxs-lookup"><span data-stu-id="9795b-121">Topic</span></span>                                                                                                                     | <span data-ttu-id="9795b-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9795b-122">Description</span></span>                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9795b-123">Prerequisiti per lo sviluppo con DirectX</span><span class="sxs-lookup"><span data-stu-id="9795b-123">Prerequisites for developing with DirectX</span></span>](pre-requisites-for-developing-a-tailored-c---with-directx-app.md)<br/> | <span data-ttu-id="9795b-124">Quando si inizia a sviluppare un'app di Windows con DirectX, tenere presenti i prerequisiti in questa pagina.</span><span class="sxs-lookup"><span data-stu-id="9795b-124">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="9795b-125">Sono incluse le tecnologie che è necessario tenere presente prima di approfondire il problema.</span><span class="sxs-lookup"><span data-stu-id="9795b-125">This includes the technologies you need to know before you dive in.</span></span><br/>                            |
| [<span data-ttu-id="9795b-126">Introduzione a DirectX per Windows</span><span class="sxs-lookup"><span data-stu-id="9795b-126">Get started with DirectX for Windows</span></span>](getting-started-with-a-directx-game.md)<br/>                                | <span data-ttu-id="9795b-127">La creazione di un gioco DirectX per Windows è una sfida per un nuovo sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="9795b-127">Creating a DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="9795b-128">In questo articolo vengono esaminati rapidamente i concetti e i passaggi necessari per iniziare lo sviluppo di un gioco con DirectX e C++.</span><span class="sxs-lookup"><span data-stu-id="9795b-128">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span><br/> |
| [<span data-ttu-id="9795b-129">Roadmap per app DirectX desktop</span><span class="sxs-lookup"><span data-stu-id="9795b-129">Roadmap for Desktop DirectX apps</span></span>](roadmap-for-metro-style-apps-using-directx.md)<br/>                             | <span data-ttu-id="9795b-130">Di seguito sono riportate le risorse principali che consentono di iniziare a usare DirectX e C++ per sviluppare app desktop con utilizzo intensivo di grafica, come i giochi.</span><span class="sxs-lookup"><span data-stu-id="9795b-130">Here are key resources to help you get started with using DirectX and C++ to develop graphics-intensive Desktop apps, like games.</span></span> <br/>                                                                 |



 

 

 





