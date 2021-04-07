---
description: Un elenco di punti è una raccolta di vertici di cui viene eseguito il rendering come punti isolati. L'applicazione può usarle nelle scene 3D per i campi Star o linee tratteggiate sulla superficie di un poligono.
ms.assetid: 82866b07-5043-433f-974a-0a301d4b5491
title: Elenchi di punti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57086a445209d9e60173910e07166a6149e0b8d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746778"
---
# <a name="point-lists"></a><span data-ttu-id="253c9-104">Elenchi di punti</span><span class="sxs-lookup"><span data-stu-id="253c9-104">Point Lists</span></span>

<span data-ttu-id="253c9-105">Un elenco di punti è una raccolta di vertici di cui viene eseguito il rendering come punti isolati.</span><span class="sxs-lookup"><span data-stu-id="253c9-105">A point list is a collection of vertices that are rendered as isolated points.</span></span> <span data-ttu-id="253c9-106">L'applicazione può usarle nelle scene 3D per i campi Star o linee tratteggiate sulla superficie di un poligono.</span><span class="sxs-lookup"><span data-stu-id="253c9-106">Your application can use them in 3D scenes for star fields, or dotted lines on the surface of a polygon.</span></span>

<span data-ttu-id="253c9-107">Nella figura seguente viene illustrato un elenco di punti di cui è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="253c9-107">The following illustration depicts a rendered point list.</span></span>

![illustrazione di un elenco di punti](images/pointlst.png)

<span data-ttu-id="253c9-109">L'applicazione può applicare materiali e trame a un elenco di punti.</span><span class="sxs-lookup"><span data-stu-id="253c9-109">Your application can apply materials and textures to a point list.</span></span> <span data-ttu-id="253c9-110">I colori del materiale o della trama vengono visualizzati solo in corrispondenza dei punti disegnati e non tra i punti.</span><span class="sxs-lookup"><span data-stu-id="253c9-110">The colors in the material or texture appear only at the points drawn, and not anywhere between the points.</span></span>

<span data-ttu-id="253c9-111">Nel codice seguente viene illustrato come creare vertici per questo elenco di punti.</span><span class="sxs-lookup"><span data-stu-id="253c9-111">The following code shows how to create vertices for this point list.</span></span>


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



<span data-ttu-id="253c9-112">L'esempio di codice seguente illustra come eseguire il rendering di questo elenco di punti in Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="253c9-112">The code example below shows how to render this point list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_POINTLIST, 0, 6 );
```



## <a name="related-topics"></a><span data-ttu-id="253c9-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="253c9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="253c9-114">Primitives</span><span class="sxs-lookup"><span data-stu-id="253c9-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
