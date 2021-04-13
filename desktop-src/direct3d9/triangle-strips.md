---
description: Una striscia triangolare è una serie di triangoli connessi.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Strisce triangolari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2766529a37b994e5fe30815ca6300476f06c7d4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568453"
---
# <a name="triangle-strips"></a><span data-ttu-id="c9880-103">Strisce triangolari</span><span class="sxs-lookup"><span data-stu-id="c9880-103">Triangle Strips</span></span>

<span data-ttu-id="c9880-104">Una striscia triangolare è una serie di triangoli connessi.</span><span class="sxs-lookup"><span data-stu-id="c9880-104">A triangle strip is a series of connected triangles.</span></span> <span data-ttu-id="c9880-105">Poiché i triangoli sono connessi, non è necessario che l'applicazione specifichi ripetutamente tutti e tre i vertici per ogni triangolo.</span><span class="sxs-lookup"><span data-stu-id="c9880-105">Because the triangles are connected, the application does not need to repeatedly specify all three vertices for each triangle.</span></span> <span data-ttu-id="c9880-106">Ad esempio, per definire la striscia di triangolo seguente sono necessari solo sette vertici.</span><span class="sxs-lookup"><span data-stu-id="c9880-106">For example, you need only seven vertices to define the following triangle strip.</span></span>

![illustrazione di una striscia di triangolo con sette vertici](images/tristrip.png)

<span data-ttu-id="c9880-108">Il sistema usa i vertici V1, V2 e V3 per creare il primo triangolo; V2, V4 e V3 per creare il secondo triangolo; V3, V4 e V5 per creare il terzo; V4, V6 e V5 per creare il quarto; E così via.</span><span class="sxs-lookup"><span data-stu-id="c9880-108">The system uses vertices v1, v2, and v3 to draw the first triangle; v2, v4, and v3 to draw the second triangle; v3, v4, and v5 to draw the third; v4, v6, and v5 to draw the fourth; and so on.</span></span> <span data-ttu-id="c9880-109">Si noti che i vertici del secondo e del quarto triangoli non sono ordinati. Questa operazione è necessaria per garantire che tutti i triangoli siano disegnati in un orientamento orario.</span><span class="sxs-lookup"><span data-stu-id="c9880-109">Notice that the vertices of the second and fourth triangles are out of order; this is required to make sure that all the triangles are drawn in a clockwise orientation.</span></span>

<span data-ttu-id="c9880-110">La maggior parte degli oggetti nelle scene 3D è costituita da strisce di triangolo.</span><span class="sxs-lookup"><span data-stu-id="c9880-110">Most objects in 3D scenes are composed of triangle strips.</span></span> <span data-ttu-id="c9880-111">Questo è dovuto al fatto che le strisce triangolari possono essere utilizzate per specificare oggetti complessi in modo da utilizzare in modo efficiente la memoria e i tempi di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="c9880-111">This is because triangle strips can be used to specify complex objects in a way that makes efficient use of memory and processing time.</span></span>

<span data-ttu-id="c9880-112">Nella figura seguente viene illustrata una striscia di triangolo sottoposta a rendering.</span><span class="sxs-lookup"><span data-stu-id="c9880-112">The following illustration depicts a rendered triangle strip.</span></span>

![illustrazione di una striscia di triangolo sottoposta a rendering](images/tstrip2.png)

<span data-ttu-id="c9880-114">Il codice seguente illustra come creare vertici per questa striscia di triangolo.</span><span class="sxs-lookup"><span data-stu-id="c9880-114">The following code shows how to create vertices for this triangle strip.</span></span>


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



<span data-ttu-id="c9880-115">L'esempio di codice seguente illustra come eseguire il rendering di questa striscia di triangolo in Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="c9880-115">The code example below shows how to render this triangle strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



<span data-ttu-id="c9880-116">Usare una striscia di triangolo per eseguire il rendering di triangoli non connessi tra loro.</span><span class="sxs-lookup"><span data-stu-id="c9880-116">Use a triangle strip to render triangles that are not connected to one another.</span></span> <span data-ttu-id="c9880-117">A tale scopo, specificare un triangolo degenerato (ovvero un triangolo la cui area è zero) nell'elenco dei triangoli.</span><span class="sxs-lookup"><span data-stu-id="c9880-117">To do this, specify a degenerate triangle (that is, a triangle whose area is zero) in the triangle list.</span></span> <span data-ttu-id="c9880-118">Viene creata una linea tra i due triangoli che non verrà sottoposta a rendering.</span><span class="sxs-lookup"><span data-stu-id="c9880-118">This creates a line between the two triangles which will not render.</span></span> <span data-ttu-id="c9880-119">Per eseguire il rendering solo dei primi e degli ultimi triangoli dell'esempio precedente, modificare il buffer del vertice come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c9880-119">To render only the first and last triangles from the previous example, modify the vertex buffer as shown here:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c9880-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9880-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9880-121">Primitives</span><span class="sxs-lookup"><span data-stu-id="c9880-121">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
