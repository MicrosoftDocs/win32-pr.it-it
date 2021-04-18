---
description: Una striscia di linea è una primitiva composta da segmenti di linea collegati.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Strisce di linea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dee7eb79b583ad04dc0ed576a7d9426e8dda9fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521953"
---
# <a name="line-strips"></a><span data-ttu-id="83cc4-103">Strisce di linea</span><span class="sxs-lookup"><span data-stu-id="83cc4-103">Line Strips</span></span>

<span data-ttu-id="83cc4-104">Una striscia di linea è una primitiva composta da segmenti di linea collegati.</span><span class="sxs-lookup"><span data-stu-id="83cc4-104">A line strip is a primitive that is composed of connected line segments.</span></span> <span data-ttu-id="83cc4-105">L'applicazione può usare strisce di riga per la creazione di poligoni che non sono chiusi.</span><span class="sxs-lookup"><span data-stu-id="83cc4-105">Your application can use line strips for creating polygons that are not closed.</span></span> <span data-ttu-id="83cc4-106">Un poligono chiuso è un poligono il cui ultimo vertice è connesso al primo vertice da un segmento di linea.</span><span class="sxs-lookup"><span data-stu-id="83cc4-106">A closed polygon is a polygon whose last vertex is connected to its first vertex by a line segment.</span></span> <span data-ttu-id="83cc4-107">Se l'applicazione crea poligoni in base alle strisce di riga, non è garantito che i vertici siano complanari.</span><span class="sxs-lookup"><span data-stu-id="83cc4-107">If your application makes polygons based on line strips, the vertices are not guaranteed to be coplanar.</span></span>

<span data-ttu-id="83cc4-108">Nell'illustrazione seguente viene mostrata una striscia di riga sottoposta a rendering.</span><span class="sxs-lookup"><span data-stu-id="83cc4-108">The following illustration shows a rendered line strip.</span></span>

![illustrazione di una striscia di linea](images/linstrip.gif)

<span data-ttu-id="83cc4-110">Nel codice seguente viene illustrato come creare vertici per questa striscia di riga.</span><span class="sxs-lookup"><span data-stu-id="83cc4-110">The following code shows how to create vertices for this line strip.</span></span>


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



<span data-ttu-id="83cc4-111">L'esempio di codice seguente illustra come eseguire il rendering di una striscia di riga in Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span><span class="sxs-lookup"><span data-stu-id="83cc4-111">The code example below shows how to render a line strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a><span data-ttu-id="83cc4-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83cc4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83cc4-113">Primitives</span><span class="sxs-lookup"><span data-stu-id="83cc4-113">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
