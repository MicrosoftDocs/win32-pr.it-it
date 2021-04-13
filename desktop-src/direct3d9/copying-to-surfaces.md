---
description: "Quando si usa IDirect3DDevice9:: UpdateSurface, passare un rettangolo sulla superficie di origine o usare NULL per specificare l'intera superficie."
ms.assetid: 2219d037-8480-4c36-b04e-0c23406a2e7e
title: Copia in superfici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163907aada5b2396a2a103d94af49d7ddd01d5ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483837"
---
# <a name="copying-to-surfaces-direct3d-9"></a><span data-ttu-id="f6d55-103">Copia in superfici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f6d55-103">Copying to Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="f6d55-104">Quando si usa [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), passare un rettangolo sulla superficie di origine o usare **null** per specificare l'intera superficie.</span><span class="sxs-lookup"><span data-stu-id="f6d55-104">When using [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), pass a rectangle on the source surface, or use **NULL** to specify the entire surface.</span></span> <span data-ttu-id="f6d55-105">Si passa anche un punto nell'area di destinazione in cui viene copiata la posizione superiore sinistra del rettangolo nell'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="f6d55-105">You also pass a point on the destination surface to which the upper left position of the rectangle on the source image is copied.</span></span> <span data-ttu-id="f6d55-106">Questo metodo non supporta il ritaglio.</span><span class="sxs-lookup"><span data-stu-id="f6d55-106">This method does not support clipping.</span></span> <span data-ttu-id="f6d55-107">L'operazione avrà esito negativo a meno che il rettangolo di origine e il rettangolo di destinazione corrispondente non siano completamente contenuti all'interno delle aree di origine e di destinazione rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="f6d55-107">The operation will fail unless the source rectangle and the corresponding destination rectangle are completely contained within the source and destination surfaces respectively.</span></span> <span data-ttu-id="f6d55-108">Questo metodo non supporta la fusione alfa, le chiavi di colore o la conversione del formato.</span><span class="sxs-lookup"><span data-stu-id="f6d55-108">This method does not support alpha blending, color keys, or format conversion.</span></span> <span data-ttu-id="f6d55-109">Si noti che le superfici di destinazione e di origine devono essere diverse.</span><span class="sxs-lookup"><span data-stu-id="f6d55-109">Note that the destination and source surfaces must be distinct.</span></span>

<span data-ttu-id="f6d55-110">Per altre restrizioni relative all'uso di UpdateSurface, vedere [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).</span><span class="sxs-lookup"><span data-stu-id="f6d55-110">For other restrictions when using UpdateSurface, see [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).</span></span>

<span data-ttu-id="f6d55-111">I metodi seguenti sono disponibili anche in C++/C per la copia di immagini in una superficie Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f6d55-111">The following methods are also available in C++/C for copying images to a Direct3D surface.</span></span>

-   [<span data-ttu-id="f6d55-112">**D3DXLoadSurfaceFromFile**</span><span class="sxs-lookup"><span data-stu-id="f6d55-112">**D3DXLoadSurfaceFromFile**</span></span>](d3dxloadsurfacefromfile.md)
-   [<span data-ttu-id="f6d55-113">**D3DXLoadSurfaceFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="f6d55-113">**D3DXLoadSurfaceFromFileInMemory**</span></span>](d3dxloadsurfacefromfileinmemory.md)
-   [<span data-ttu-id="f6d55-114">**D3DXLoadSurfaceFromMemory**</span><span class="sxs-lookup"><span data-stu-id="f6d55-114">**D3DXLoadSurfaceFromMemory**</span></span>](d3dxloadsurfacefrommemory.md)
-   [<span data-ttu-id="f6d55-115">**D3DXLoadSurfaceFromResource**</span><span class="sxs-lookup"><span data-stu-id="f6d55-115">**D3DXLoadSurfaceFromResource**</span></span>](d3dxloadsurfacefromresource.md)
-   [<span data-ttu-id="f6d55-116">**D3DXLoadSurfaceFromSurface**</span><span class="sxs-lookup"><span data-stu-id="f6d55-116">**D3DXLoadSurfaceFromSurface**</span></span>](d3dxloadsurfacefromsurface.md)
-   [<span data-ttu-id="f6d55-117">**IDirect3DDevice9:: UpdateSurface**</span><span class="sxs-lookup"><span data-stu-id="f6d55-117">**IDirect3DDevice9::UpdateSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a><span data-ttu-id="f6d55-118">Esempio di UpdateSurface</span><span class="sxs-lookup"><span data-stu-id="f6d55-118">UpdateSurface Example</span></span>

<span data-ttu-id="f6d55-119">Nell'esempio seguente vengono copiati due rettangoli dalla superficie di origine a una superficie di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f6d55-119">The following example copies two rectangles from the source surface to a destination surface.</span></span> <span data-ttu-id="f6d55-120">Il primo rettangolo viene copiato da (0, 0, 50, 50) nella superficie di origine nello stesso percorso dell'area di destinazione e il secondo rettangolo viene copiato da (50, 50, 100, 100) nella superficie di origine a (150, 150, 200, 200) nell'area di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f6d55-120">The first rectangle is copied from (0, 0, 50, 50) on the source surface to the same location on the destination surface, and the second rectangle is copied from (50, 50, 100, 100) on the source surface to (150, 150, 200, 200) on the destination surface.</span></span>


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a><span data-ttu-id="f6d55-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f6d55-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6d55-122">Superfici Direct3D</span><span class="sxs-lookup"><span data-stu-id="f6d55-122">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="f6d55-123">**IDirect3DDevice9:: StretchRect**</span><span class="sxs-lookup"><span data-stu-id="f6d55-123">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
