---
description: Il mapping dell'ambiente è una tecnica che simula superfici altamente riflettenti senza usare l'analisi dei raggi.
ms.assetid: vs|directx_sdk|~\environment_mapping.htm
title: Mapping dell'ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686f15b2f097550206f9c02cfc4104e7c9f6c030
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745951"
---
# <a name="environment-mapping-direct3d-9"></a><span data-ttu-id="52b42-103">Mapping dell'ambiente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="52b42-103">Environment Mapping (Direct3D 9)</span></span>

<span data-ttu-id="52b42-104">Il mapping dell'ambiente è una tecnica che simula superfici altamente riflettenti senza usare l'analisi dei raggi.</span><span class="sxs-lookup"><span data-stu-id="52b42-104">Environment mapping is a technique that simulates highly reflective surfaces without using ray tracing.</span></span> <span data-ttu-id="52b42-105">In pratica, il mapping dell'ambiente applica una mappa di trama speciale che contiene un'immagine della scena che circonda un oggetto per l'oggetto stesso.</span><span class="sxs-lookup"><span data-stu-id="52b42-105">In practice, environment mapping applies a special texture map that contains an image of the scene surrounding an object to the object itself.</span></span> <span data-ttu-id="52b42-106">Il risultato è simile all'aspetto di una superficie riflettente, sufficientemente vicino da ingannare l'occhio, senza incorrere in alcun calcolo complesso implicato nella traccia dei raggi.</span><span class="sxs-lookup"><span data-stu-id="52b42-106">The result approximates the appearance of a reflective surface, close enough to fool the eye, without incurring any of the complex computations involved in ray tracing.</span></span>

<span data-ttu-id="52b42-107">Nella figura seguente viene illustrato un tipo di mapping dell'ambiente denominato mapping di ambienti sferici.</span><span class="sxs-lookup"><span data-stu-id="52b42-107">The following illustration demonstrates a type of environment mapping called spherical environment mapping.</span></span> <span data-ttu-id="52b42-108">Per informazioni dettagliate, vedere [mapping di ambienti sferici](spherical-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="52b42-108">For details, see [Spherical Environment Mapping](spherical-environment-mapping.md).</span></span>

![illustrazione di una teiera con una trama applicata che riflette gli ambienti](images/spheremapped-teapot.png)

<span data-ttu-id="52b42-110">La teiera in questa immagine sembra rifletterne gli ambienti; si tratta in realtà di una trama applicata all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="52b42-110">The teapot in this image appears to reflect its surroundings; this is actually a texture being applied to the object.</span></span> <span data-ttu-id="52b42-111">Poiché il mapping dell'ambiente usa una trama, combinata con coordinate di trama calcolate in modo specifico, può essere eseguita in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="52b42-111">Because environment mapping uses a texture, combined with specially computed texture coordinates, it can be performed in real-time.</span></span>

<span data-ttu-id="52b42-112">In questa sezione vengono fornite informazioni sull'esecuzione di due tipi comuni di mapping dell'ambiente con Direct3D.</span><span class="sxs-lookup"><span data-stu-id="52b42-112">This section provides information about performing two common types of environment mapping with Direct3D.</span></span> <span data-ttu-id="52b42-113">Sono disponibili molti tipi di mapping dell'ambiente in uso nel settore della grafica, ma gli argomenti seguenti sono destinati alle due forme più comuni: mapping dell'ambiente cubico e mapping di ambienti sferici.</span><span class="sxs-lookup"><span data-stu-id="52b42-113">There are many types of environment mapping in use throughout the graphics industry, but the following topics target the two most common forms: cubic environment mapping and spherical environment mapping.</span></span>

-   [<span data-ttu-id="52b42-114">Mapping dell'ambiente cubico</span><span class="sxs-lookup"><span data-stu-id="52b42-114">Cubic Environment Mapping</span></span>](cubic-environment-mapping.md)
-   [<span data-ttu-id="52b42-115">Mapping di ambienti sferici</span><span class="sxs-lookup"><span data-stu-id="52b42-115">Spherical Environment Mapping</span></span>](spherical-environment-mapping.md)

## <a name="related-topics"></a><span data-ttu-id="52b42-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52b42-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52b42-117">Pipeline pixel</span><span class="sxs-lookup"><span data-stu-id="52b42-117">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



