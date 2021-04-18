---
description: Durante il rendering, la pipeline interpola i dati dei vertici in ogni triangolo.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Interpolazione di triangolo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 405cbecd6123145d412a3e7f58f727bdf5b5a3e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304364"
---
# <a name="triangle-interpolation-direct3d-9"></a><span data-ttu-id="7e85a-103">Interpolazione di triangolo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7e85a-103">Triangle Interpolation (Direct3D 9)</span></span>

<span data-ttu-id="7e85a-104">Durante il rendering, la pipeline interpola i dati dei vertici in ogni triangolo.</span><span class="sxs-lookup"><span data-stu-id="7e85a-104">During rendering, the pipeline interpolates vertex data across each triangle.</span></span> <span data-ttu-id="7e85a-105">I dati dei vertici possono essere un'ampia varietà di dati e possono includere (ma non limitati): il colore diffuso, il colore speculare, l'alfa diffusa (opacità del triangolo), l'alfa speculare e un fattore di nebbia (tratto da Alpha speculare per la pipeline Vertex della funzione fissa e dal registro di nebbia per la pipeline dei vertici programmabile).</span><span class="sxs-lookup"><span data-stu-id="7e85a-105">Vertex data can be a broad variety of data and can include (but is not limited to): diffuse color, specular color, diffuse alpha (triangle opacity), specular alpha, and a fog factor (taken from specular alpha for fixed function vertex pipeline and from fog register for programmable vertex pipeline).</span></span> <span data-ttu-id="7e85a-106">I dati dei vertici vengono definiti dalla [dichiarazione del vertice (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="7e85a-106">The vertex data is defined by the [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

<span data-ttu-id="7e85a-107">Per alcuni dati dei vertici, l'interpolazione dipende dalla modalità di ombreggiatura corrente, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7e85a-107">For some vertex data, the interpolation is dependent on the current shading mode, as shown in the following table.</span></span>



| <span data-ttu-id="7e85a-108">Modalità ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="7e85a-108">Shading mode</span></span> | <span data-ttu-id="7e85a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e85a-109">Description</span></span>                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e85a-110">Semplice</span><span class="sxs-lookup"><span data-stu-id="7e85a-110">Flat</span></span>         | <span data-ttu-id="7e85a-111">Solo il fattore di nebbia viene interpolato in modalità ombreggiatura piatta.</span><span class="sxs-lookup"><span data-stu-id="7e85a-111">Only the fog factor is interpolated in flat shade mode.</span></span> <span data-ttu-id="7e85a-112">Per tutti gli altri valori interpolati, il colore del primo vertice nel triangolo viene applicato nell'intero quadrante.</span><span class="sxs-lookup"><span data-stu-id="7e85a-112">For all other interpolated values, the color of the first vertex in the triangle is applied across the entire face.</span></span> |
| <span data-ttu-id="7e85a-113">Gouraud</span><span class="sxs-lookup"><span data-stu-id="7e85a-113">Gouraud</span></span>      | <span data-ttu-id="7e85a-114">L'interpolazione lineare viene eseguita tra tutti e tre i vertici.</span><span class="sxs-lookup"><span data-stu-id="7e85a-114">Linear interpolation is performed between all three vertices.</span></span>                                                                                                               |



 

<span data-ttu-id="7e85a-115">Il colore e il colore speculare sono trattati in modo diverso, a seconda del modello colori.</span><span class="sxs-lookup"><span data-stu-id="7e85a-115">The diffuse color and specular color are treated differently, depending on the color model.</span></span> <span data-ttu-id="7e85a-116">Nel modello di colore RGB, il sistema usa i componenti di colore rosso, verde e blu nell'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="7e85a-116">In the RGB color model, the system uses the red, green, and blue color components in the interpolation.</span></span>

<span data-ttu-id="7e85a-117">Il componente alfa di un colore viene considerato come un valore interpolato separato perché i driver di dispositivo possono implementare la trasparenza in due modi diversi: usando la combinazione di trame o l'uso di punteggiatura.</span><span class="sxs-lookup"><span data-stu-id="7e85a-117">The alpha component of a color is treated as a separate interpolated value because device drivers can implement transparency in two different ways: by using texture blending or by using stippling.</span></span>

<span data-ttu-id="7e85a-118">Usare il membro ShadeCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per determinare le forme di interpolazione supportate dal driver di dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="7e85a-118">Use the ShadeCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure to determine what forms of interpolation the current device driver supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e85a-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e85a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e85a-120">Sistemi di coordinate e geometria</span><span class="sxs-lookup"><span data-stu-id="7e85a-120">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



