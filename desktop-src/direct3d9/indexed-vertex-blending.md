---
description: La fusione di vertici indicizzati estende il supporto per la fusione dei vertici in Direct3D per consentire l'utilizzo di matrici per la fusione.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Fusione di vertici indicizzati (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cfe7b45831317fdf9e92525ed74bbd27323e99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480716"
---
# <a name="indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="76b58-103">Fusione di vertici indicizzati (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="76b58-103">Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="76b58-104">La fusione di vertici indicizzati estende il supporto per la fusione dei vertici in Direct3D per consentire l'utilizzo di matrici per la fusione.</span><span class="sxs-lookup"><span data-stu-id="76b58-104">Indexed vertex blending extends the vertex blending support in Direct3D to allow matrices to be used for blending.</span></span> <span data-ttu-id="76b58-105">A queste matrici viene fatto riferimento tramite un indice della matrice.</span><span class="sxs-lookup"><span data-stu-id="76b58-105">These matrices are referred to by using a matrix index.</span></span> <span data-ttu-id="76b58-106">Questi indici vengono forniti in base ai singoli vertici e fanno riferimento a una tavolozza di un massimo di 256 matrici.</span><span class="sxs-lookup"><span data-stu-id="76b58-106">These indices are supplied on a per-vertex basis and refer to a palette of up to 256 matrices.</span></span> <span data-ttu-id="76b58-107">Ogni indice è a 8 bit e ogni vertice può avere un massimo di quattro indici, che consente di unire quattro matrici per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="76b58-107">Each index is 8 bits and each vertex can have up to four indices, which allows four matrices to be blended per vertex.</span></span> <span data-ttu-id="76b58-108">Gli indici vengono compressi in un valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="76b58-108">The indices are packed into a DWORD.</span></span> <span data-ttu-id="76b58-109">Poiché gli indici vengono specificati per ogni vertice, fino a 12 matrici possono influire su un singolo triangolo e qualsiasi matrice nella tavolozza può influire sui vertici di una chiamata di progetto.</span><span class="sxs-lookup"><span data-stu-id="76b58-109">Because indices are specified on a per-vertex basis, up to 12 matrices can affect a single triangle, and any matrix in the palette can affect the vertices of one draw call.</span></span> <span data-ttu-id="76b58-110">Questo approccio offre i vantaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="76b58-110">This approach has the following advantages.</span></span>

-   <span data-ttu-id="76b58-111">Consente a più matrici di influenzare un singolo triangolo.</span><span class="sxs-lookup"><span data-stu-id="76b58-111">It enables more matrices to affect a single triangle.</span></span>
-   <span data-ttu-id="76b58-112">Consente di passare triangoli più Blend nella stessa chiamata di progetto.</span><span class="sxs-lookup"><span data-stu-id="76b58-112">It enables more blended triangles to be passed in the same draw call.</span></span>
-   <span data-ttu-id="76b58-113">Rende la fusione dei vertici indipendente dagli indici dei triangoli.</span><span class="sxs-lookup"><span data-stu-id="76b58-113">It makes vertex blending independent of triangle indices.</span></span> <span data-ttu-id="76b58-114">In questo modo, le mesh progressive funzionano insieme alla fusione dei vertici.</span><span class="sxs-lookup"><span data-stu-id="76b58-114">This enables progressive meshes to work in conjunction with vertex blending.</span></span>

<span data-ttu-id="76b58-115">Uno svantaggio di questo approccio è che non funziona con le primitive di superficie curva quando si verifica il mosaico prima dell'elaborazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="76b58-115">One disadvantage of this approach is that it does not work with curved-surface primitives when tessellation occurs before vertex processing.</span></span>

<span data-ttu-id="76b58-116">Il diagramma seguente illustra il modo in cui quattro matrici possono influenzare un vertice.</span><span class="sxs-lookup"><span data-stu-id="76b58-116">The following diagram demonstrates how four matrices can affect a vertex.</span></span> <span data-ttu-id="76b58-117">Ogni vertice è costituito da un massimo di quattro indici, pertanto quattro matrici possono essere combinate per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="76b58-117">Each vertex has up to four indices, so four matrices can be blended per vertex.</span></span> <span data-ttu-id="76b58-118">Il diagramma usa le matrici indicizzate a 0, 2, 5 e 6.</span><span class="sxs-lookup"><span data-stu-id="76b58-118">The diagram uses the matrices indexed at 0, 2, 5, and 6.</span></span>

![diagramma della fusione dei vertici indicizzati con 4 di 256 matrici disponibili](images/dword1.png)

<span data-ttu-id="76b58-120">Il diagramma seguente illustra il modo in cui fino a 12 matrici possono influenzare un triangolo.</span><span class="sxs-lookup"><span data-stu-id="76b58-120">The following diagram demonstrates how up to 12 matrices can affect a triangle.</span></span> <span data-ttu-id="76b58-121">Utilizzando gli indici specificati per ogni vertice, fino a 12 matrici possono influire sul triangolo.</span><span class="sxs-lookup"><span data-stu-id="76b58-121">Using indices specified on a per-vertex basis, up to 12 matrices can affect the triangle.</span></span>

![diagramma della fusione dei vertici indicizzati per un triangolo usando 12 di 256 matrici disponibili](images/dword2.png)

<span data-ttu-id="76b58-123">L'equazione seguente determina il caso generale per il modo in cui le matrici hanno effetto su un vertice.</span><span class="sxs-lookup"><span data-stu-id="76b58-123">The following equation determines the general case for how matrices effect a vertex.</span></span>

![equazione della fusione dei vertici indicizzati](images/indexedvblend.png)

<span data-ttu-id="76b58-125">V <sub>Model</sub> è la posizione del vertice dello spazio del modello di input.</span><span class="sxs-lookup"><span data-stu-id="76b58-125">V <sub>model</sub> is the input model space vertex position.</span></span> <span data-ttu-id="76b58-126">Index0.. Index3 sono gli indici di matrice per vertice compressi in un valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="76b58-126">Index0..Index3 are the per-vertex matrix indices packed into a DWORD.</span></span> <span data-ttu-id="76b58-127">M \[ \] è la matrice di matrici globali che vengono indicizzate in.</span><span class="sxs-lookup"><span data-stu-id="76b58-127">M\[\] is the array of world matrices that get indexed into.</span></span> <span data-ttu-id="76b58-128">b ₀.. b ₂ sono i pesi di Blend.</span><span class="sxs-lookup"><span data-stu-id="76b58-128">b₀..b₂ are the blend weights.</span></span> <span data-ttu-id="76b58-129">V<sub>World</sub> è la posizione del vertice dello spazio globale di output.</span><span class="sxs-lookup"><span data-stu-id="76b58-129">V<sub>world</sub> is the output world space vertex position.</span></span>

<span data-ttu-id="76b58-130">Per altre informazioni sulla combinazione di vertici indicizzati, vedere [uso della combinazione di vertici indicizzati (Direct3D 9)](using-indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="76b58-130">For more information about indexed vertex blending, see [Using Indexed Vertex Blending (Direct3D 9)](using-indexed-vertex-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="76b58-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76b58-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76b58-132">Blending Geometry</span><span class="sxs-lookup"><span data-stu-id="76b58-132">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



