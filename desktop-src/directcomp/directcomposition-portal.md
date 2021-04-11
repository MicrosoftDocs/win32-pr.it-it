---
title: DirectComposition
description: In questo argomento viene illustrato lo scopo di Microsoft DirectComposition, vengono identificati i requisiti in fase di esecuzione e viene descritto lo sfondo di programmazione necessario per utilizzare Microsoft DirectComposition in modo efficace.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- API DirectComposition
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb34a4bb3bb7c0ffe370777888e20704fd0165d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329180"
---
# <a name="directcomposition"></a><span data-ttu-id="3c66a-106">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3c66a-106">DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="3c66a-107">Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3c66a-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="3c66a-108">Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="3c66a-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

## <a name="purpose"></a><span data-ttu-id="3c66a-109">Scopo</span><span class="sxs-lookup"><span data-stu-id="3c66a-109">Purpose</span></span>

<span data-ttu-id="3c66a-110">Microsoft DirectComposition è un componente di Windows che consente la composizione di bitmap a prestazioni elevate con trasformazioni, effetti e animazioni.</span><span class="sxs-lookup"><span data-stu-id="3c66a-110">Microsoft DirectComposition is a Windows component that enables high-performance bitmap composition with transforms, effects, and animations.</span></span> <span data-ttu-id="3c66a-111">Gli sviluppatori di applicazioni possono usare l'API DirectComposition per creare interfacce utente visivamente accattivanti che presentano transizioni animate da un oggetto visivo all'altro fluide e ricche di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3c66a-111">Application developers can use the DirectComposition API to create visually engaging user interfaces that feature rich and fluid animated transitions from one visual to another.</span></span>

<span data-ttu-id="3c66a-112">DirectComposition consente transizioni avanzate e fluide ottenendo un framerate elevato, usando hardware grafico e operando in modo indipendente dal thread dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="3c66a-112">DirectComposition enables rich and fluid transitions by achieving a high framerate, using graphics hardware, and operating independently of the UI thread.</span></span> <span data-ttu-id="3c66a-113">DirectComposition può accettare il contenuto bitmap disegnato da diverse librerie di rendering, incluse le bitmap Microsoft DirectX, e le bitmap sottoposte a rendering in una finestra (bitmap HWND).</span><span class="sxs-lookup"><span data-stu-id="3c66a-113">DirectComposition can accept bitmap content drawn by different rendering libraries, including Microsoft DirectX bitmaps, and bitmaps rendered to a window (HWND bitmaps).</span></span> <span data-ttu-id="3c66a-114">DirectComposition supporta inoltre un'ampia gamma di trasformazioni, come le trasformazioni affini 2D e le trasformazioni di prospettiva 3D, nonché gli effetti di base come il ritaglio e l'opacità.</span><span class="sxs-lookup"><span data-stu-id="3c66a-114">Also, DirectComposition supports a variety of transformations, such as 2D affine transforms and 3D perspective transforms, as well as basic effects such as clipping and opacity.</span></span>

<span data-ttu-id="3c66a-115">DirectComposition è progettato per semplificare il processo di composizione di oggetti [*visivi*](directcomposition-glossary.md) e di creazione di transizioni animate.</span><span class="sxs-lookup"><span data-stu-id="3c66a-115">DirectComposition is designed to simplify the process of composing [*visuals*](directcomposition-glossary.md) and creating animated transitions.</span></span> <span data-ttu-id="3c66a-116">Se l'applicazione contiene già codice di rendering o usa già l'API DirectX consigliata, è sufficiente eseguire una quantità minima di lavoro per usare DirectComposition in modo efficace.</span><span class="sxs-lookup"><span data-stu-id="3c66a-116">If your application already contains rendering code or already uses the recommended DirectX API, you only need to do a minimal amount of work to use DirectComposition effectively.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3c66a-117">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="3c66a-117">Developer audience</span></span>

<span data-ttu-id="3c66a-118">L'API DirectComposition è destinata a sviluppatori di grafica esperti e altamente idonei che conoscono C/C++, hanno una conoscenza approfondita del Component Object Model (COM) e hanno familiarità con i concetti di programmazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="3c66a-118">The DirectComposition API is intended for experienced and highly-capable graphics developers who know C/C++, have a solid understanding of the Component Object Model (COM), and are familiar with Windows programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3c66a-119">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="3c66a-119">Run-time requirements</span></span>

<span data-ttu-id="3c66a-120">DirectComposition è stato introdotto in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3c66a-120">DirectComposition was introduced in Windows 8.</span></span> <span data-ttu-id="3c66a-121">È incluso nelle piattaforme a 32 bit, a 64 e a ARM.</span><span class="sxs-lookup"><span data-stu-id="3c66a-121">It is included in 32-bit, 64-bit, and ARM platforms.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3c66a-122">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="3c66a-122">In this section</span></span>



| <span data-ttu-id="3c66a-123">Argomento</span><span class="sxs-lookup"><span data-stu-id="3c66a-123">Topic</span></span>                                                                       | <span data-ttu-id="3c66a-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c66a-124">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c66a-125">Perché usare DirectComposition?</span><span class="sxs-lookup"><span data-stu-id="3c66a-125">Why use DirectComposition?</span></span>](why-use-directcomposition-.md)<br/>     | <span data-ttu-id="3c66a-126">In questo argomento vengono descritte le funzionalità e i vantaggi di DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3c66a-126">This topic describes the capabilities and benefits of DirectComposition.</span></span> <br/>                                                                           |
| [<span data-ttu-id="3c66a-127">Come usare DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3c66a-127">How to Use DirectComposition</span></span>](how-to-use-directcomposition.md)<br/> | <span data-ttu-id="3c66a-128">In questa sezione vengono descritte le procedure consigliate per l'utilizzo dell'API DirectComposition e viene illustrato come utilizzare l'API per eseguire diverse attività comuni.</span><span class="sxs-lookup"><span data-stu-id="3c66a-128">This section describes best practices for using the DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span> <br/> |
| [<span data-ttu-id="3c66a-129">Concetti di DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3c66a-129">DirectComposition concepts</span></span>](directcomposition-concepts.md)<br/>     | <span data-ttu-id="3c66a-130">Questa sezione fornisce una panoramica concettuale di DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3c66a-130">This section provides a conceptual overview of DirectComposition.</span></span><br/>                                                                                   |
| [<span data-ttu-id="3c66a-131">Riferimento a DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3c66a-131">DirectComposition reference</span></span>](reference.md)<br/>                     | <span data-ttu-id="3c66a-132">Questa sezione fornisce informazioni di riferimento dettagliate per gli elementi che costituiscono l'API DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3c66a-132">This section provides detailed reference information for the elements that make up the DirectComposition API.</span></span><br/>                                       |
| [<span data-ttu-id="3c66a-133">Esempi di DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3c66a-133">DirectComposition samples</span></span>](directcomposition-code-samples.md)<br/>  | <span data-ttu-id="3c66a-134">Le applicazioni di esempio seguenti illustrano come usare l'API DirectComposition e dimostrarne le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3c66a-134">The following sample applications show how to use the DirectComposition API and demonstrate its capabilities.</span></span> <br/>                                      |
| [<span data-ttu-id="3c66a-135">Glossario DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3c66a-135">DirectComposition glossary</span></span>](directcomposition-glossary.md)<br/>     | <span data-ttu-id="3c66a-136">In questo argomento vengono definiti i termini di DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3c66a-136">This topic defines DirectComposition terms.</span></span> <br/>                                                                                                        |



 

 

 





