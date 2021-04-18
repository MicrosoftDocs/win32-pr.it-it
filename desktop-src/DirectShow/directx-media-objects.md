---
description: Oggetti multimediali DirectX
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: Oggetti multimediali DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2119fc8cce602bc1cc085886edd6852320aca180
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320456"
---
# <a name="directx-media-objects"></a><span data-ttu-id="d09d3-103">Oggetti multimediali DirectX</span><span class="sxs-lookup"><span data-stu-id="d09d3-103">DirectX Media Objects</span></span>

> [!Note]  
> <span data-ttu-id="d09d3-104">DMOs sono stati sostituiti da [trasformazioni di Media Foundation](/windows/desktop/medfound/media-foundation-transforms) (MFTS).</span><span class="sxs-lookup"><span data-stu-id="d09d3-104">DMOs have been superseded by [Media Foundation Transforms](/windows/desktop/medfound/media-foundation-transforms) (MFTs).</span></span> <span data-ttu-id="d09d3-105">Le interfacce DMO sono ancora supportate.</span><span class="sxs-lookup"><span data-stu-id="d09d3-105">The DMO interfaces are still supported.</span></span> <span data-ttu-id="d09d3-106">Tuttavia, se si scrive un codec personalizzato o un plug-in di elaborazione audio/video, è consigliabile implementarlo come MFT.</span><span class="sxs-lookup"><span data-stu-id="d09d3-106">However, if you are writing a custom codec or audio/video processing plug-in, you should consider implementing it as an MFT.</span></span>

 

<span data-ttu-id="d09d3-107">Gli oggetti multimediali DirectX (DMOs) sono componenti di streaming di dati basati su COM.</span><span class="sxs-lookup"><span data-stu-id="d09d3-107">DirectX Media Objects (DMOs) are COM-based data-streaming components.</span></span> <span data-ttu-id="d09d3-108">Per alcuni aspetti, DMOs sono simili ai filtri Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d09d3-108">In some respects, DMOs are similar to Microsoft DirectShow filters.</span></span> <span data-ttu-id="d09d3-109">Analogamente ai filtri DirectShow, DMOs accetta i dati di input e li usa per produrre dati di output.</span><span class="sxs-lookup"><span data-stu-id="d09d3-109">Like DirectShow filters, DMOs take input data and use it to produce output data.</span></span> <span data-ttu-id="d09d3-110">Tuttavia, le API (Application Programming Interface) per DMOs sono molto più semplici delle API corrispondenti per DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d09d3-110">However, the application programming interfaces (APIs) for DMOs are much simpler than the corresponding APIs for DirectShow.</span></span> <span data-ttu-id="d09d3-111">Di conseguenza, DMOs sono più facili da creare, testare e usare.</span><span class="sxs-lookup"><span data-stu-id="d09d3-111">As a result, DMOs are easier to create, test, and use.</span></span> <span data-ttu-id="d09d3-112">DMOs può essere usato in molti scenari:</span><span class="sxs-lookup"><span data-stu-id="d09d3-112">DMOs can be used in many scenarios:</span></span>

-   <span data-ttu-id="d09d3-113">Le applicazioni basate su DirectShow possono usare DMOs tramite un filtro DirectShow denominato filtro [wrapper DMO](dmo-wrapper-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d09d3-113">Applications based on DirectShow can use DMOs through a DirectShow filter called the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="d09d3-114">La distinzione tra Filters e DMOs è trasparente per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d09d3-114">The distinction between filters and DMOs is transparent to the application.</span></span> <span data-ttu-id="d09d3-115">L'applicazione non chiama direttamente le API DMO.</span><span class="sxs-lookup"><span data-stu-id="d09d3-115">The application does not directly call the DMO APIs.</span></span>
-   <span data-ttu-id="d09d3-116">Le applicazioni basate su Microsoft DirectSound possono usare l'effetto audio DMOs.</span><span class="sxs-lookup"><span data-stu-id="d09d3-116">Applications based on Microsoft DirectSound can use audio effect DMOs.</span></span> <span data-ttu-id="d09d3-117">Anche in questo caso, l'applicazione viene protetta dalle API DMO di basso livello dalle API DirectSound di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="d09d3-117">Again, the application is shielded from the low-level DMO APIs by the higher-level DirectSound APIs.</span></span>
-   <span data-ttu-id="d09d3-118">Le applicazioni possono usare direttamente DMOs.</span><span class="sxs-lookup"><span data-stu-id="d09d3-118">Applications can use DMOs directly.</span></span>

<span data-ttu-id="d09d3-119">Pertanto, scrivendo un DMO, viene creato un componente che può essere utilizzato in un'ampia gamma di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d09d3-119">Thus, by writing a DMO, you create a component that can be used in a wide range of applications.</span></span> <span data-ttu-id="d09d3-120">Questa documentazione contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d09d3-120">This documentation contains the following sections:</span></span>

-   [<span data-ttu-id="d09d3-121">Informazioni su DMOs</span><span class="sxs-lookup"><span data-stu-id="d09d3-121">About DMOs</span></span>](about-dmos.md)
-   [<span data-ttu-id="d09d3-122">Uso di DMOs</span><span class="sxs-lookup"><span data-stu-id="d09d3-122">Using DMOs</span></span>](using-dmos.md)
-   [<span data-ttu-id="d09d3-123">Scrittura di un DMO</span><span class="sxs-lookup"><span data-stu-id="d09d3-123">Writing a DMO</span></span>](writing-a-dmo.md)
-   [<span data-ttu-id="d09d3-124">Parametri dei supporti</span><span class="sxs-lookup"><span data-stu-id="d09d3-124">Media Parameters</span></span>](media-parameters.md)
-   [<span data-ttu-id="d09d3-125">Guida di riferimento a DMO</span><span class="sxs-lookup"><span data-stu-id="d09d3-125">DMO Reference</span></span>](dmo-reference.md)

## <a name="related-topics"></a><span data-ttu-id="d09d3-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d09d3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d09d3-127">DirectShow</span><span class="sxs-lookup"><span data-stu-id="d09d3-127">DirectShow</span></span>](directshow.md)
</dt> </dl>

 

 
