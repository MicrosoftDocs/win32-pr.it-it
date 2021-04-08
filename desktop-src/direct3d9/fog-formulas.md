---
description: Le applicazioni C++ possono controllare il modo in cui la nebbia influisce sul colore degli oggetti in una scena modificando il modo in cui Microsoft Direct3D calcola gli effetti della nebbia rispetto alla distanza.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Formule Fog (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150a00d491f1e3fc1ea1444209449c1c2a825d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876402"
---
# <a name="fog-formulas-direct3d-9"></a><span data-ttu-id="840a7-103">Formule Fog (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="840a7-103">Fog Formulas (Direct3D 9)</span></span>

<span data-ttu-id="840a7-104">Le applicazioni C++ possono controllare il modo in cui la nebbia influisce sul colore degli oggetti in una scena modificando il modo in cui Microsoft Direct3D calcola gli effetti della nebbia rispetto alla distanza.</span><span class="sxs-lookup"><span data-stu-id="840a7-104">C++ applications can control how fog affects the color of objects in a scene by changing how Microsoft Direct3D computes fog effects over distance.</span></span> <span data-ttu-id="840a7-105">Il tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) contiene membri che identificano le tre formule di nebbia.</span><span class="sxs-lookup"><span data-stu-id="840a7-105">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type contains members that identify the three fog formulas.</span></span> <span data-ttu-id="840a7-106">Tutte le formule calcolano un fattore di nebbia come funzione di distanza, dati i parametri impostati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="840a7-106">All formulas calculate a fog factor as a function of distance, given parameters that your application sets.</span></span>

## <a name="linear-fog"></a><span data-ttu-id="840a7-107">Nebbia lineare</span><span class="sxs-lookup"><span data-stu-id="840a7-107">Linear Fog</span></span>

<span data-ttu-id="840a7-108">Viene impostato con l' \_ equazione lineare D3DFOG seguente.</span><span class="sxs-lookup"><span data-stu-id="840a7-108">This is set with the following D3DFOG\_LINEAR equation.</span></span>

![equazione della nebbia lineare Direct3D](images/fogliner.png)

<span data-ttu-id="840a7-110">dove</span><span class="sxs-lookup"><span data-stu-id="840a7-110">where</span></span>

-   <span data-ttu-id="840a7-111">Start è la distanza con cui iniziano gli effetti di nebbia.</span><span class="sxs-lookup"><span data-stu-id="840a7-111">start is the distance at which fog effects begin.</span></span>
-   <span data-ttu-id="840a7-112">End è la distanza con cui gli effetti della nebbia non aumentano più.</span><span class="sxs-lookup"><span data-stu-id="840a7-112">end is the distance at which fog effects no longer increase.</span></span>
-   <span data-ttu-id="840a7-113">d rappresenta la profondità o la distanza dal punto di vista.</span><span class="sxs-lookup"><span data-stu-id="840a7-113">d represents depth, or the distance from the viewpoint.</span></span> <span data-ttu-id="840a7-114">Per la nebbia basata sull'intervallo, il valore di d è la distanza tra la posizione della fotocamera e un vertice.</span><span class="sxs-lookup"><span data-stu-id="840a7-114">For range based fog, the value for d is the distance between the camera position and a vertex.</span></span> <span data-ttu-id="840a7-115">Per la nebbia non basata sull'intervallo, il valore di d è il valore assoluto della coordinata Z nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="840a7-115">For non-range based fog, the value for d is the absolute value of the Z-coordinate in camera space.</span></span>

## <a name="exponential-fog"></a><span data-ttu-id="840a7-116">Nebbia esponenziale</span><span class="sxs-lookup"><span data-stu-id="840a7-116">Exponential Fog</span></span>

<span data-ttu-id="840a7-117">Le formule lineare ed esponenziale sono supportate sia per la nebbia dei pixel che per il vertice.</span><span class="sxs-lookup"><span data-stu-id="840a7-117">Linear and exponential formulas are supported for both pixel fog and vertex fog.</span></span>

<span data-ttu-id="840a7-118">Questa impostazione viene impostata con l' \_ equazione exp D3DFOG seguente.</span><span class="sxs-lookup"><span data-stu-id="840a7-118">This is set with the following D3DFOG\_EXP equation.</span></span>

![equazione della nebbia esponenziale Direct3D](images/fogexp.png)

<span data-ttu-id="840a7-120">dove</span><span class="sxs-lookup"><span data-stu-id="840a7-120">where</span></span>

-   <span data-ttu-id="840a7-121">e è la base dei logaritmi naturali (approssimativamente 2,71828).</span><span class="sxs-lookup"><span data-stu-id="840a7-121">e is the base of natural logarithms (approximately 2.71828).</span></span>
-   <span data-ttu-id="840a7-122">la densità è una densità di nebbia arbitraria che può variare da 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="840a7-122">density is an arbitrary fog density that can range from 0.0 to 1.0.</span></span>
-   <span data-ttu-id="840a7-123">d rappresenta la profondità o la distanza dal punto di vista, come indicato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="840a7-123">d represents depth, or the distance from the viewpoint, as stated earlier.</span></span>

<span data-ttu-id="840a7-124">Questa impostazione viene impostata con l' \_ equazione D3DFOG exp2 seguente.</span><span class="sxs-lookup"><span data-stu-id="840a7-124">This is set with the following D3DFOG\_EXP2 equation.</span></span>

![equazione di Direct3D esponenziale 2 Fog](images/fogexp2.png)

<span data-ttu-id="840a7-126">dove</span><span class="sxs-lookup"><span data-stu-id="840a7-126">where</span></span>

-   <span data-ttu-id="840a7-127">e è la base dei logaritmi naturali come indicato sopra.</span><span class="sxs-lookup"><span data-stu-id="840a7-127">e is the base of natural logarithms as stated above.</span></span>
-   <span data-ttu-id="840a7-128">la densità è una densità di nebbia arbitraria che può variare da 0,0 a 1,0 come indicato sopra.</span><span class="sxs-lookup"><span data-stu-id="840a7-128">density is an arbitrary fog density that can range from 0.0 to 1.0 as stated above.</span></span>
-   <span data-ttu-id="840a7-129">d rappresenta la profondità o la distanza dal punto di vista, come indicato sopra.</span><span class="sxs-lookup"><span data-stu-id="840a7-129">d represents depth, or the distance from the viewpoint, as stated above.</span></span>

> [!Note]  
> <span data-ttu-id="840a7-130">Il sistema archivia il fattore di nebbia nel componente alfa del colore speculare per un vertice.</span><span class="sxs-lookup"><span data-stu-id="840a7-130">The system stores the fog factor in the alpha component of the specular color for a vertex.</span></span> <span data-ttu-id="840a7-131">Se l'applicazione esegue una trasformazione e un'illuminazione proprie, è possibile inserire manualmente i valori del fattore di nebbia, che verranno applicati dal sistema durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="840a7-131">If your application performs its own transformation and lighting, you can insert fog factor values manually, to be applied by the system during rendering.</span></span>

 

<span data-ttu-id="840a7-132">Il grafico seguente mostra queste formule, usando i valori comuni come nei parametri della formula.</span><span class="sxs-lookup"><span data-stu-id="840a7-132">The following graph shows these formulas, using common values as in the formula parameters.</span></span>

![grafico delle formule di nebbia rispetto alla distanza e alla quantità di colore](images/foggraph.png)

<span data-ttu-id="840a7-134">D3DFOG \_ Linear è 1,0 all'inizio e 0,0 alla fine.</span><span class="sxs-lookup"><span data-stu-id="840a7-134">D3DFOG\_LINEAR is 1.0 at start and 0.0 at end.</span></span> <span data-ttu-id="840a7-135">Non viene misurato in relazione ai piani vicini o lontani.</span><span class="sxs-lookup"><span data-stu-id="840a7-135">It is not measured relative to the near or far planes.</span></span>

<span data-ttu-id="840a7-136">Quando Direct3D calcola gli effetti di nebbia, usa il fattore di nebbia di una delle equazioni precedenti nell'equazione di fusione seguente.</span><span class="sxs-lookup"><span data-stu-id="840a7-136">When Direct3D calculates fog effects, it uses the fog factor from one of the preceding equations in the following blending equation.</span></span>

![equazione degli effetti di nebbia per Direct3D](images/fogcalc.png)

<span data-ttu-id="840a7-138">Questa formula ridimensiona in modo efficace il colore del poligono corrente C per il fattore di nebbia f e aggiunge il prodotto al colore di nebbia C, ridimensionato dall'inverso bit per bit del fattore di nebbia.</span><span class="sxs-lookup"><span data-stu-id="840a7-138">This formula effectively scales the color of the current polygon C by the fog factor f, and adds the product to the fog color C, scaled by the bitwise inverse of the fog factor.</span></span> <span data-ttu-id="840a7-139">Il valore di colore risultante è una combinazione del colore di nebbia e del colore originale, come fattore di distanza.</span><span class="sxs-lookup"><span data-stu-id="840a7-139">The resulting color value is a blend of the fog color and the original color, as a factor of distance.</span></span> <span data-ttu-id="840a7-140">La formula si applica a tutti i dispositivi supportati in Microsoft DirectX 7,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="840a7-140">The formula applies to all devices supported in Microsoft DirectX 7.0 and later.</span></span> <span data-ttu-id="840a7-141">Per il dispositivo ramp legacy, il fattore di nebbia ridimensiona i componenti del colore speculare e diffuso, che vengono fissati nell'intervallo tra 0,0 e 1,0 inclusi.</span><span class="sxs-lookup"><span data-stu-id="840a7-141">For the legacy ramp device, the fog factor scales the diffuse and specular color components, clamped to the range of 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="840a7-142">Il fattore di nebbia inizia in genere a 1,0 per il piano vicino e viene ridotto a 0,0 sul piano lontano.</span><span class="sxs-lookup"><span data-stu-id="840a7-142">The fog factor typically starts at 1.0 for the near plane and decreases to 0.0 at the far plane.</span></span>

## <a name="related-topics"></a><span data-ttu-id="840a7-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="840a7-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="840a7-144">Tipi di nebbia</span><span class="sxs-lookup"><span data-stu-id="840a7-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
