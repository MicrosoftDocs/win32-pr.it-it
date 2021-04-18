---
description: Un elenco di triangolo è un elenco di triangoli isolati. Potrebbero essere vicini o meno. Un elenco di triangolo deve avere almeno tre vertici e il numero totale di vertici deve essere divisibile per tre.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Elenchi di triangolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230cac9b4120d31821d70db022ab50d311d7b73e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304367"
---
# <a name="triangle-lists"></a><span data-ttu-id="56b4d-105">Elenchi di triangolo</span><span class="sxs-lookup"><span data-stu-id="56b4d-105">Triangle Lists</span></span>

<span data-ttu-id="56b4d-106">Un elenco di triangolo è un elenco di triangoli isolati.</span><span class="sxs-lookup"><span data-stu-id="56b4d-106">A triangle list is a list of isolated triangles.</span></span> <span data-ttu-id="56b4d-107">Potrebbero essere vicini o meno.</span><span class="sxs-lookup"><span data-stu-id="56b4d-107">They might or might not be near each other.</span></span> <span data-ttu-id="56b4d-108">Un elenco di triangolo deve avere almeno tre vertici e il numero totale di vertici deve essere divisibile per tre.</span><span class="sxs-lookup"><span data-stu-id="56b4d-108">A triangle list must have at least three vertices and the total number of vertices must be divisible by three.</span></span>

<span data-ttu-id="56b4d-109">Usare gli elenchi di triangolo per creare un oggetto composto da parti non contigue.</span><span class="sxs-lookup"><span data-stu-id="56b4d-109">Use triangle lists to create an object that is composed of disjoint pieces.</span></span> <span data-ttu-id="56b4d-110">Ad esempio, un modo per creare un muro di campo forzato in un gioco 3D consiste nel specificare un elenco esteso di piccoli triangoli non connessi.</span><span class="sxs-lookup"><span data-stu-id="56b4d-110">For instance, one way to create a force-field wall in a 3D game is to specify a large list of small, unconnected triangles.</span></span> <span data-ttu-id="56b4d-111">Applicare quindi un materiale e una trama che sembrano emettere luce nell'elenco dei triangoli.</span><span class="sxs-lookup"><span data-stu-id="56b4d-111">Then apply a material and texture that appears to emit light to the triangle list.</span></span> <span data-ttu-id="56b4d-112">Ogni triangolo nella parete sembra illuminare.</span><span class="sxs-lookup"><span data-stu-id="56b4d-112">Each triangle in the wall appears to glow.</span></span> <span data-ttu-id="56b4d-113">La scena dietro la parete diventa parzialmente visibile attraverso i gap tra i triangoli, in quanto un lettore potrebbe aspettarsi quando si esamina un campo forzato.</span><span class="sxs-lookup"><span data-stu-id="56b4d-113">The scene behind the wall becomes partially visible through the gaps between the triangles, as a player might expect when looking at a force field.</span></span>

<span data-ttu-id="56b4d-114">Gli elenchi di triangolo sono utili anche per creare primitive con spigoli acuti e ombreggiati con ombreggiatura Gouraud.</span><span class="sxs-lookup"><span data-stu-id="56b4d-114">Triangle lists are also useful for creating primitives that have sharp edges and are shaded with Gouraud shading.</span></span> <span data-ttu-id="56b4d-115">Vedere [vettori normali per visi e vertici (Direct3D 9)](face-and-vertex-normal-vectors.md).</span><span class="sxs-lookup"><span data-stu-id="56b4d-115">See [Face and Vertex Normal Vectors (Direct3D 9)](face-and-vertex-normal-vectors.md).</span></span>

<span data-ttu-id="56b4d-116">Nella figura seguente viene illustrato un elenco di triangolo di cui è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="56b4d-116">The following illustration depicts a rendered triangle list.</span></span>

![illustrazione di un elenco di triangolo sottoposto a rendering](images/trilist.png)

<span data-ttu-id="56b4d-118">Il codice seguente illustra come creare vertici per questo elenco di triangolo.</span><span class="sxs-lookup"><span data-stu-id="56b4d-118">The following code shows how to create vertices for this triangle list.</span></span>


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}

};
```



<span data-ttu-id="56b4d-119">L'esempio di codice seguente illustra come eseguire il rendering di questo elenco di triangolo in Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="56b4d-119">The code example below shows how to render this triangle list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



<span data-ttu-id="56b4d-120">È anche possibile usare le strisce di triangolo per eseguire il rendering di triangoli non connessi tra loro.</span><span class="sxs-lookup"><span data-stu-id="56b4d-120">You can also use triangle strips to render triangles that are not connected to one another.</span></span> <span data-ttu-id="56b4d-121">A tale scopo, specificare un triangolo degenerato (ovvero un triangolo con dimensioni pari a zero) nell'elenco; verrà creata una linea tra i due triangoli che non verranno visualizzati durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="56b4d-121">To do this, specify a degenerate triangle (that is, a triangle with zero size) in the list; this will create a line between the two triangles which will not appear during rendering.</span></span> <span data-ttu-id="56b4d-122">Ad esempio, per eseguire il rendering solo del primo e dell'ultimo triangolo dell'esempio precedente, inizializzare il buffer dei vertici con i vertici seguenti:</span><span class="sxs-lookup"><span data-stu-id="56b4d-122">For example, to render only the first and last triangle from the previous example, initialize the vertex buffer with the following vertices:</span></span>


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a><span data-ttu-id="56b4d-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="56b4d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56b4d-124">Primitives</span><span class="sxs-lookup"><span data-stu-id="56b4d-124">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
