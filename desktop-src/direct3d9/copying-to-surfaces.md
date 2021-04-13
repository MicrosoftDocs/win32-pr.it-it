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
# <a name="copying-to-surfaces-direct3d-9"></a>Copia in superfici (Direct3D 9)

Quando si usa [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface), passare un rettangolo sulla superficie di origine o usare **null** per specificare l'intera superficie. Si passa anche un punto nell'area di destinazione in cui viene copiata la posizione superiore sinistra del rettangolo nell'immagine di origine. Questo metodo non supporta il ritaglio. L'operazione avrà esito negativo a meno che il rettangolo di origine e il rettangolo di destinazione corrispondente non siano completamente contenuti all'interno delle aree di origine e di destinazione rispettivamente. Questo metodo non supporta la fusione alfa, le chiavi di colore o la conversione del formato. Si noti che le superfici di destinazione e di origine devono essere diverse.

Per altre restrizioni relative all'uso di UpdateSurface, vedere [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).

I metodi seguenti sono disponibili anche in C++/C per la copia di immagini in una superficie Direct3D.

-   [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md)
-   [**D3DXLoadSurfaceFromFileInMemory**](d3dxloadsurfacefromfileinmemory.md)
-   [**D3DXLoadSurfaceFromMemory**](d3dxloadsurfacefrommemory.md)
-   [**D3DXLoadSurfaceFromResource**](d3dxloadsurfacefromresource.md)
-   [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)
-   [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a>Esempio di UpdateSurface

Nell'esempio seguente vengono copiati due rettangoli dalla superficie di origine a una superficie di destinazione. Il primo rettangolo viene copiato da (0, 0, 50, 50) nella superficie di origine nello stesso percorso dell'area di destinazione e il secondo rettangolo viene copiato da (50, 50, 100, 100) nella superficie di origine a (150, 150, 200, 200) nell'area di destinazione.


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9:: StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
