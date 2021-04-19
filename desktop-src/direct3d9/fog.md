---
description: L'aggiunta di una nebbia a una scena 3D può migliorare il realismo, fornire un ambiente o impostare un mood e nascondere gli artefatti a volte quando viene visualizzata la geometria distanti.
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: Nebbia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b9ed234bef0f3dea76baa98390f25e9b2003a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303806"
---
# <a name="fog-direct3d-9"></a><span data-ttu-id="85120-103">Nebbia (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85120-103">Fog (Direct3D 9)</span></span>

<span data-ttu-id="85120-104">L'aggiunta di una nebbia a una scena 3D può migliorare il realismo, fornire un ambiente o impostare un mood e nascondere gli artefatti a volte quando viene visualizzata la geometria distanti.</span><span class="sxs-lookup"><span data-stu-id="85120-104">Adding fog to a 3D scene can enhance realism, provide ambiance or set a mood, and obscure artifacts sometimes caused when distant geometry comes into view.</span></span> <span data-ttu-id="85120-105">Direct3D supporta due modelli di nebbia, la nebbia dei pixel e la nebbia dei vertici, ognuno con funzionalità e interfaccia di programmazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="85120-105">Direct3D supports two fog models, pixel fog and vertex fog, each with its own features and programming interface.</span></span>

<span data-ttu-id="85120-106">In sostanza, la nebbia viene implementata combinando il colore degli oggetti in una scena con un colore di nebbia scelto in base alla profondità di un oggetto in una scena o la relativa distanza dal punto di vista.</span><span class="sxs-lookup"><span data-stu-id="85120-106">Essentially, fog is implemented by blending the color of objects in a scene with a chosen fog color based on the depth of an object in a scene or its distance from the viewpoint.</span></span> <span data-ttu-id="85120-107">Man mano che gli oggetti crescono più distanti, il colore originale si mescola sempre più con il colore di nebbia scelto, creando l'illusione che l'oggetto sia sempre più nascosto da piccole particelle fluttuanti nella scena.</span><span class="sxs-lookup"><span data-stu-id="85120-107">As objects grow more distant, their original color blends more and more with the chosen fog color, creating the illusion that the object is being increasingly obscured by tiny particles floating in the scene.</span></span> <span data-ttu-id="85120-108">Nella figura seguente viene mostrata una scena di cui viene eseguito il rendering senza nebbia e viene visualizzata una scena simile con la nebbia abilitata.</span><span class="sxs-lookup"><span data-stu-id="85120-108">The following illustration shows a scene rendered without fog, and a similar scene rendered with fog enabled.</span></span>

![illustrazione della stessa scena con e senza nebbia](images/fogcomp.png)

<span data-ttu-id="85120-110">In questa illustrazione, la scena a sinistra ha un orizzonte chiaro, oltre il quale non è visibile alcuno scenario, anche se sarebbe visibile nel mondo reale.</span><span class="sxs-lookup"><span data-stu-id="85120-110">In this illustration, the scene on the left has a clear horizon, beyond which no scenery is visible, even though it would be visible in the real world.</span></span> <span data-ttu-id="85120-111">La scena a destra nasconde l'orizzonte usando un colore di nebbia identico al colore di sfondo, facendo in modo che i poligoni sembrino dissolversi nella distanza.</span><span class="sxs-lookup"><span data-stu-id="85120-111">The scene on the right obscures the horizon by using a fog color identical to the background color, making polygons appear to fade into the distance.</span></span> <span data-ttu-id="85120-112">Combinando gli effetti di nebbia discreti con la progettazione della scena creativa è possibile aggiungere umore e ammorbidire il colore degli oggetti in una scena.</span><span class="sxs-lookup"><span data-stu-id="85120-112">By combining discrete fog effects with creative scene design you can add mood and soften the color of objects in a scene.</span></span>

<span data-ttu-id="85120-113">Direct3D offre due modi per aggiungere la nebbia a una scena: la nebbia dei pixel e la nebbia del vertice, denominate per la modalità di applicazione degli effetti di nebbia.</span><span class="sxs-lookup"><span data-stu-id="85120-113">Direct3D provides two ways to add fog to a scene: pixel fog and vertex fog, named for how the fog effects are applied.</span></span> <span data-ttu-id="85120-114">Per informazioni dettagliate, vedere [pixel Fog (Direct3D 9)](pixel-fog.md) e [Vertex Fog (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="85120-114">For details, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span> <span data-ttu-id="85120-115">In breve, la nebbia dei pixel, detta anche nebbia della tabella, è implementata nel driver di dispositivo e la nebbia del vertice viene implementata nel motore di illuminazione Direct3D.</span><span class="sxs-lookup"><span data-stu-id="85120-115">In short, pixel fog - also called table fog - is implemented in the device driver and vertex fog is implemented in the Direct3D lighting engine.</span></span> <span data-ttu-id="85120-116">Un'applicazione può implementare la nebbia con un vertex shader e contemporaneamente la nebbia pixel, se lo si desidera.</span><span class="sxs-lookup"><span data-stu-id="85120-116">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

> [!Note]  
> <span data-ttu-id="85120-117">Indipendentemente dal fatto che si usi la nebbia pixel o vertex, l'applicazione deve fornire una matrice di proiezione conforme per assicurarsi che gli effetti di nebbia siano applicati correttamente.</span><span class="sxs-lookup"><span data-stu-id="85120-117">Regardless of whether you use pixel or vertex fog, your application must provide a compliant projection matrix to ensure that fog effects are properly applied.</span></span> <span data-ttu-id="85120-118">Questa restrizione si applica anche alle applicazioni che non utilizzano il motore di trasformazione e illuminazione Direct3D.</span><span class="sxs-lookup"><span data-stu-id="85120-118">This restriction applies even to applications that do not use the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="85120-119">Per ulteriori informazioni su come fornire una matrice appropriata, vedere [proiezione Transform (Direct3D 9)](projection-transform.md).</span><span class="sxs-lookup"><span data-stu-id="85120-119">For additional details about how you can provide an appropriate matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

 

<span data-ttu-id="85120-120">Gli argomenti seguenti introducono la nebbia e presentano informazioni sull'uso di varie funzionalità di nebbia nelle applicazioni Direct3D.</span><span class="sxs-lookup"><span data-stu-id="85120-120">The following topics introduce fog and present information about using various fog features in Direct3D applications.</span></span>

-   [<span data-ttu-id="85120-121">Formule Fog (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85120-121">Fog Formulas (Direct3D 9)</span></span>](fog-formulas.md)
-   [<span data-ttu-id="85120-122">Parametri di nebbia (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85120-122">Fog Parameters (Direct3D 9)</span></span>](fog-parameters.md)
-   [<span data-ttu-id="85120-123">Blending di nebbia (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85120-123">Fog Blending (Direct3D 9)</span></span>](fog-blending.md)
-   [<span data-ttu-id="85120-124">Colore nebbia (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85120-124">Fog Color (Direct3D 9)</span></span>](fog-color.md)
-   [<span data-ttu-id="85120-125">Nebbia vertice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85120-125">Vertex Fog (Direct3D 9)</span></span>](vertex-fog.md)
-   [<span data-ttu-id="85120-126">Nebbia pixel (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85120-126">Pixel Fog (Direct3D 9)</span></span>](pixel-fog.md)

<span data-ttu-id="85120-127">La fusione di nebbia è controllata dagli Stati di rendering; non fa parte della pipeline di pixel programmabile.</span><span class="sxs-lookup"><span data-stu-id="85120-127">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85120-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85120-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85120-129">Rendering Direct3D</span><span class="sxs-lookup"><span data-stu-id="85120-129">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



