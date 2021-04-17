---
description: La modalità di ombreggiatura utilizzata per eseguire il rendering di un poligono ha un effetto profondo sull'aspetto. Le modalità di ombreggiatura determinano l'intensità del colore e dell'illuminazione in qualsiasi punto su una faccia poligonale. Direct3D supporta due modalità di ombreggiatura.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Modalità di ombreggiatura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84e791bed0098838760f10f6605f716444e7688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104556414"
---
# <a name="shading-modes-direct3d-9"></a><span data-ttu-id="89f09-105">Modalità di ombreggiatura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="89f09-105">Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="89f09-106">La modalità di ombreggiatura utilizzata per eseguire il rendering di un poligono ha un effetto profondo sull'aspetto.</span><span class="sxs-lookup"><span data-stu-id="89f09-106">The shading mode used to render a polygon has a profound effect on its appearance.</span></span> <span data-ttu-id="89f09-107">Le modalità di ombreggiatura determinano l'intensità del colore e dell'illuminazione in qualsiasi punto su una faccia poligonale.</span><span class="sxs-lookup"><span data-stu-id="89f09-107">Shading modes determine the intensity of color and lighting at any point on a polygon face.</span></span> <span data-ttu-id="89f09-108">Direct3D supporta due modalità di ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="89f09-108">Direct3D supports two shading modes.</span></span>

-   [<span data-ttu-id="89f09-109">Ombreggiatura flat</span><span class="sxs-lookup"><span data-stu-id="89f09-109">Flat Shading</span></span>](#flat-shading)
-   [<span data-ttu-id="89f09-110">Ombreggiatura Gouraud</span><span class="sxs-lookup"><span data-stu-id="89f09-110">Gouraud Shading</span></span>](#gouraud-shading)

## <a name="flat-shading"></a><span data-ttu-id="89f09-111">Ombreggiatura flat</span><span class="sxs-lookup"><span data-stu-id="89f09-111">Flat Shading</span></span>

<span data-ttu-id="89f09-112">Nella modalità di ombreggiatura flat la pipeline di rendering Direct3D esegue il rendering di un poligono, utilizzando il colore del materiale del poligono al primo vertice come colore per l'intero poligono.</span><span class="sxs-lookup"><span data-stu-id="89f09-112">In the flat shading mode, the Direct3D rendering pipeline renders a polygon, using the color of the polygon material at its first vertex as the color for the entire polygon.</span></span> <span data-ttu-id="89f09-113">gli oggetti 3D di cui viene eseguito il rendering con ombreggiatura piatta hanno bordi visibilmente nitidi tra i poligoni se non sono complanari.</span><span class="sxs-lookup"><span data-stu-id="89f09-113">3D objects that are rendered with flat shading have visibly sharp edges between polygons if they are not coplanar.</span></span>

<span data-ttu-id="89f09-114">Nell'illustrazione seguente viene mostrata una teiera con ombreggiatura piatta.</span><span class="sxs-lookup"><span data-stu-id="89f09-114">The following illustration shows a teapot rendered with flat shading.</span></span> <span data-ttu-id="89f09-115">Il contorno di ogni poligono è chiaramente visibile.</span><span class="sxs-lookup"><span data-stu-id="89f09-115">The outline of each polygon is clearly visible.</span></span> <span data-ttu-id="89f09-116">L'ombreggiatura piatta è la forma più veloce di ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="89f09-116">Flat shading is the fastest form of shading.</span></span>

![illustrazione di una teiera usando l'ombreggiatura piatta](images/flattea.png)

## <a name="gouraud-shading"></a><span data-ttu-id="89f09-118">Ombreggiatura Gouraud</span><span class="sxs-lookup"><span data-stu-id="89f09-118">Gouraud Shading</span></span>

<span data-ttu-id="89f09-119">Quando Direct3D esegue il rendering di un poligono usando l'ombreggiatura Gouraud, calcola un colore per ogni vertice usando i parametri di illuminazione e normale del vertice.</span><span class="sxs-lookup"><span data-stu-id="89f09-119">When Direct3D renders a polygon using Gouraud shading, it computes a color for each vertex by using the vertex normal and lighting parameters.</span></span> <span data-ttu-id="89f09-120">Esegue quindi l'interpolazione del colore sulla superficie dei poligoni. l'interpolazione viene eseguita in modo lineare.</span><span class="sxs-lookup"><span data-stu-id="89f09-120">Then, it interpolates the color across the face of the polygons The interpolation is done linearly.</span></span> <span data-ttu-id="89f09-121">Se, ad esempio, il componente rosso del colore del vertice 1 è 0,8 e il componente rosso del vertice 2 è 0,4, usando la modalità di ombreggiatura Gouraud e il modello di colore RGB, il modulo di illuminazione Direct3D assegna un componente rosso di 0,6 al pixel al punto medio della linea tra questi vertici.</span><span class="sxs-lookup"><span data-stu-id="89f09-121">For example, if the red component of the color of vertex 1 is 0.8 and the red component of vertex 2 is 0.4, using the Gouraud shading mode and the RGB color model, the Direct3D lighting module assigns a red component of 0.6 to the pixel at the midpoint of the line between these vertices.</span></span>

<span data-ttu-id="89f09-122">Nella figura seguente viene illustrata l'ombreggiatura Gouraud.</span><span class="sxs-lookup"><span data-stu-id="89f09-122">The following illustration demonstrates Gouraud shading.</span></span> <span data-ttu-id="89f09-123">Questa teiera è costituita da molti poligoni triangolari bidimensionali.</span><span class="sxs-lookup"><span data-stu-id="89f09-123">This teapot is composed of many flat, triangular polygons.</span></span> <span data-ttu-id="89f09-124">Tuttavia, l'ombreggiatura Gouraud fa sì che la superficie dell'oggetto appaia curva e smussata.</span><span class="sxs-lookup"><span data-stu-id="89f09-124">However, Gouraud shading makes the surface of the object appear curved and smooth.</span></span>

![illustrazione della teiera usando l'ombreggiatura Gouraud](images/gourtea.png)

<span data-ttu-id="89f09-126">L'ombreggiatura Gouraud può essere usata anche per visualizzare oggetti con spigoli acuti.</span><span class="sxs-lookup"><span data-stu-id="89f09-126">Gouraud shading can also be used to display objects with sharp edges.</span></span>

<span data-ttu-id="89f09-127">Per altre informazioni, vedere [vettori normali per visi e vertici (Direct3D 9)](face-and-vertex-normal-vectors.md).</span><span class="sxs-lookup"><span data-stu-id="89f09-127">For more information, see [Face and Vertex Normal Vectors (Direct3D 9)](face-and-vertex-normal-vectors.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="89f09-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89f09-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89f09-129">Ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="89f09-129">Shading</span></span>](shading.md)
</dt> </dl>

 

 



