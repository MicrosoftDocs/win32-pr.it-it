---
description: I parametri di nebbia sono controllati tramite gli Stati di rendering del dispositivo.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Parametri di nebbia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876401"
---
# <a name="fog-parameters-direct3d-9"></a><span data-ttu-id="a28b9-103">Parametri di nebbia (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a28b9-103">Fog Parameters (Direct3D 9)</span></span>

<span data-ttu-id="a28b9-104">I parametri di nebbia sono controllati tramite gli Stati di rendering del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a28b9-104">Fog parameters are controlled through device render states.</span></span> <span data-ttu-id="a28b9-105">I tipi di nebbia pixel e vertex supportano tutte le formule di nebbia introdotte nelle [formule di nebbia (Direct3D 9)](fog-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="a28b9-105">Both pixel and vertex fog types support all the fog formulas introduced in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="a28b9-106">Il tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) definisce le costanti che è possibile usare per identificare la formula di nebbia che si vuole venga usata da Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a28b9-106">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type defines constants that you can use to identify the fog formula you want Microsoft Direct3D to use.</span></span> <span data-ttu-id="a28b9-107">Lo \_ stato di rendering FOGTABLEMODE di D3DRS controlla la modalità di nebbia utilizzata da Direct3D per la nebbia dei pixel e lo \_ stato di rendering FOGVERTEXMODE di D3DRS controlla la modalità per la nebbia dei vertici.</span><span class="sxs-lookup"><span data-stu-id="a28b9-107">The D3DRS\_FOGTABLEMODE render state controls the fog mode that Direct3D uses for pixel fog, and the D3DRS\_FOGVERTEXMODE render state controls the mode for vertex fog.</span></span>

<span data-ttu-id="a28b9-108">Quando si usa la formula di nebbia lineare, si impostano le distanze iniziale e finale tramite gli \_ Stati di rendering D3DRS FOGSTART e D3DRS \_ FOGEND.</span><span class="sxs-lookup"><span data-stu-id="a28b9-108">When using the linear fog formula, you set the starting and ending distances through the D3DRS\_FOGSTART and D3DRS\_FOGEND render states.</span></span> <span data-ttu-id="a28b9-109">Il modo in cui i valori vengono interpretati dal sistema dipende dal tipo di nebbia usata dall'applicazione: la nebbia dei pixel o dei vertici e, quando si usa la nebbia dei pixel, se si usa la profondità basata su z o w.</span><span class="sxs-lookup"><span data-stu-id="a28b9-109">How the system interprets these values depends on the type of fog your application uses - pixel or vertex fog - and, when using pixel fog, if z-based or w-based depth is being used.</span></span> <span data-ttu-id="a28b9-110">Nella tabella seguente sono riepilogati i tipi di nebbia e le rispettive unità di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="a28b9-110">The following table summarizes fog types and their start and end units.</span></span>



| <span data-ttu-id="a28b9-111">Tipo di nebbia</span><span class="sxs-lookup"><span data-stu-id="a28b9-111">Fog type</span></span>  | <span data-ttu-id="a28b9-112">Unità di inizio/fine nebbia</span><span class="sxs-lookup"><span data-stu-id="a28b9-112">Fog start/end units</span></span>      |
|-----------|--------------------------|
| <span data-ttu-id="a28b9-113">Pixel (Z)</span><span class="sxs-lookup"><span data-stu-id="a28b9-113">Pixel (Z)</span></span> | <span data-ttu-id="a28b9-114">Spazio del dispositivo \[ 0,0, 1.0\]</span><span class="sxs-lookup"><span data-stu-id="a28b9-114">Device space \[0.0,1.0\]</span></span> |
| <span data-ttu-id="a28b9-115">Pixel (W)</span><span class="sxs-lookup"><span data-stu-id="a28b9-115">Pixel (W)</span></span> | <span data-ttu-id="a28b9-116">Spazio fotocamera</span><span class="sxs-lookup"><span data-stu-id="a28b9-116">Camera space</span></span>             |
| <span data-ttu-id="a28b9-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="a28b9-117">Vertex</span></span>    | <span data-ttu-id="a28b9-118">Spazio fotocamera</span><span class="sxs-lookup"><span data-stu-id="a28b9-118">Camera space</span></span>             |



 

<span data-ttu-id="a28b9-119">Lo \_ stato di rendering FOGDENSITY di D3DRS controlla la densità di nebbia applicata quando è abilitata una formula di nebbia esponenziale.</span><span class="sxs-lookup"><span data-stu-id="a28b9-119">The D3DRS\_FOGDENSITY render state controls the fog density applied when an exponential fog formula is enabled.</span></span> <span data-ttu-id="a28b9-120">La densità di nebbia è essenzialmente un fattore di ponderazione, compreso tra 0,0 e 1,0 (inclusi), che consente di ridimensionare il valore di distanza nell'esponente.</span><span class="sxs-lookup"><span data-stu-id="a28b9-120">Fog density is essentially a weighting factor, ranging from 0.0 to 1.0 (inclusive), that scales the distance value in the exponent.</span></span>

<span data-ttu-id="a28b9-121">Il colore usato dal sistema per la fusione di nebbia viene controllato tramite lo \_ stato di rendering del dispositivo FogColor di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="a28b9-121">The color that the system uses for fog blending is controlled through the D3DRS\_FOGCOLOR device render state.</span></span> <span data-ttu-id="a28b9-122">Per altre informazioni, vedere [colore di nebbia (Direct3D 9)](fog-color.md) e [blending di nebbia (Direct3D 9)](fog-blending.md).</span><span class="sxs-lookup"><span data-stu-id="a28b9-122">For more information, see [Fog Color (Direct3D 9)](fog-color.md) and [Fog Blending (Direct3D 9)](fog-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a28b9-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a28b9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a28b9-124">Tipi di nebbia</span><span class="sxs-lookup"><span data-stu-id="a28b9-124">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
