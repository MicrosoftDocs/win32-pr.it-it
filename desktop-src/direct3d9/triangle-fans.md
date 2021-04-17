---
description: Una ventola a triangolo è simile a una striscia di triangolo, con la differenza che tutti i triangoli condividono un vertice, come illustrato nella figura seguente.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Ventilatori a triangolo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2357af0d999cc759453e34cd278f61064a637cfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566987"
---
# <a name="triangle-fans-direct3d-9"></a><span data-ttu-id="2da59-103">Ventilatori a triangolo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2da59-103">Triangle Fans (Direct3D 9)</span></span>

<span data-ttu-id="2da59-104">Una ventola a triangolo è simile a una striscia di triangolo, con la differenza che tutti i triangoli condividono un vertice, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2da59-104">A triangle fan is similar to a triangle strip, except that all the triangles share one vertex, as shown in the following illustration.</span></span>

![illustrazione di una ventola a triangolo](images/trifan.gif)

<span data-ttu-id="2da59-106">Il sistema usa i vertici V2, V3 e V1 per creare il primo triangolo; V3, V4 e V1 per creare il secondo triangolo; V4, V5 e V1 per creare il terzo triangolo; E così via.</span><span class="sxs-lookup"><span data-stu-id="2da59-106">The system uses vertices v2, v3, and v1 to draw the first triangle; v3, v4, and v1 to draw the second triangle; v4, v5, and v1 to draw the third triangle; and so on.</span></span> <span data-ttu-id="2da59-107">Quando è abilitata l'ombreggiatura piatta, il sistema ombreggia il triangolo con il colore del primo vertice.</span><span class="sxs-lookup"><span data-stu-id="2da59-107">When flat shading is enabled, the system shades the triangle with the color from its first vertex.</span></span>

<span data-ttu-id="2da59-108">Nella figura seguente viene illustrata una ventola del triangolo sottoposta a rendering.</span><span class="sxs-lookup"><span data-stu-id="2da59-108">The following illustration depicts a rendered triangle fan.</span></span>

![illustrazione di una ventola del triangolo sottoposta a rendering](images/tfan2.gif)

<span data-ttu-id="2da59-110">Il codice seguente illustra come creare vertici per questa ventola del triangolo.</span><span class="sxs-lookup"><span data-stu-id="2da59-110">The following code shows how to create vertices for this triangle fan.</span></span>


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    { 0.0, 0.0, 0.0},
    {-5.0, 5.0, 0.0},
    {-3.0,  7.0, 0.0},
    { 0.0, 10.0, 0.0},
    { 3.0,  7.0, 0.0},
    { 5.0,  5.0, 0.0},
};
```



<span data-ttu-id="2da59-111">L'esempio di codice seguente illustra come eseguire il rendering di questa ventola del triangolo in Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="2da59-111">The code example below shows how to render this triangle fan in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



<span data-ttu-id="2da59-112">Le ventole del triangolo non sono supportate in Direct3D 10 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2da59-112">Triangle fans are not supported in Direct3D 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2da59-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2da59-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2da59-114">Primitives</span><span class="sxs-lookup"><span data-stu-id="2da59-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
