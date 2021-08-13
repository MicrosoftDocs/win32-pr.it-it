---
title: Cenni preliminari sull'interoperabilità
description: Riepiloga le diverse tecnologie che è possibile usare con Direct2D.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Interoperabilità Direct2D,GDI
- Direct2D,GDI+interoperazione
- Direct2D, interoperabilità
- Direct2D,DirectWrite interoperazione
- interoperabilità, Direct2D
- interoperabilità, Direct3D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilità, Graphics Device Interface (GDI)
- interoperabilità, GDI+
- DirectWrite interoperabilità
- interoperabilità, DirectWrite
- Windows Imaging Component (WIC)
- WIC (Windows Imaging Component)
- interoperabilità, Windows Imaging Component (WIC)
- Interoperabilità Direct2D,WIC
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 35567b461815d28a5fc00b2cc4049f5c81b61c6e8030f477e93efbc8a5d580e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119385326"
---
# <a name="interoperability-overview"></a>Cenni preliminari sull'interoperabilità

Una delle funzionalità principali di Direct2D è l'abilitazione dell'interoperabilità tra Direct2D e altre piattaforme di rendering in modo che gli sviluppatori possano usare i punti di forza specifici di ogni piattaforma senza essere costretti a compromettere scegliendo una piattaforma per tutte le esigenze. Questo argomento riepiloga le diverse piattaforme con cui Direct2D è interoperabile. Include le sezioni seguenti:

-   [Interoperabilità con GDI](#gdi-interoperability)
-   [GDI+ Interoperabilità](#gdi-interoperability)
-   [Interoperabilità Direct3D](#direct3d-interoperability)
-   [DirectWrite Interoperabilità](#directwrite-interoperability)
-   [Windows Interoperabilità del componente di creazione dell'immagine (WIC)](#windows-imaging-component-wic-interoperability)
-   [Argomenti correlati](#related-topics)

Il diagramma seguente riepiloga le diverse piattaforme con cui Direct2D è interoperabile ed elenca alcuni metodi e interfacce che forniscono interoperabilità.

![Diagramma delle piattaforme con cui direct2d interagisce, tra cui direct3d 10.1, directwrite, wic, gdi+ e gdi](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a>Interoperabilità con GDI

Direct2D consente l'interoperabilità bidirestica con GDI. È possibile usare [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) per scrivere contenuto Direct2D in un contesto di dispositivo [GDI](/windows/desktop/gdi/device-contexts) oppure [**usare ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) per ottenere una rappresentazione DC di una destinazione di rendering.

Per altre informazioni ed esempi, vedere Cenni [preliminari sull'interoperabilità di Direct2D e GDI.](direct2d-and-gdi-interoperation-overview.md)

## <a name="gdi-interoperability"></a>GDI+ Interoperabilità

È possibile usare GDI+ direct2D nello stesso modo di GDI. È possibile usare [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) per scrivere contenuto Direct2D nello stesso controller di dominio del GDI+ contenuto. Questo approccio consente di iniziare ad aggiungere contenuto Direct2D alle applicazioni di cui viene eseguito principalmente il rendering usando GDI+.

È anche possibile usare [**un ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) per fornire l'accesso a un controller di dominio GDI che scrive tramite Direct2D e quindi usare il [**metodo FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) per creare un oggetto. Questo approccio è utile per le applicazioni che eseguono principalmente il rendering con Direct2D, ma hanno un modello di estendibilità o altro contenuto legacy che richiede la possibilità di eseguire il rendering con GDI+.

## <a name="direct3d-interoperability"></a>Interoperabilità Direct3D

Direct2D può usare una destinazione di rendering della superficie DXGI (creata dal [**metodo CreateDxgiSurfaceRender)**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) per scrivere in [idXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface). Questa azione consente di aggiungere sfondi e interfacce 2D a scene 3D e usare contenuto Direct2D come trama per un modello 3D. Direct2D può anche prendere un [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) e usare il [**metodo CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) per creare una rappresentazione bitmap.

Per altre informazioni ed esempi, vedere La panoramica [dell'interoperabilità direct2D e Direct3D](direct2d-and-direct3d-interoperation-overview.md).

## <a name="directwrite-interoperability"></a>DirectWrite Interoperabilità

Direct2D è strettamente integrato con DirectWrite. Direct2D semplifica il rendering del contenuto DirectWrite fornendo i metodi [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)e [**DrawGlyphRun.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

## <a name="windows-imaging-component-wic-interoperability"></a>Windows Interoperabilità del componente di creazione dell'immagine (WIC)

Direct2D fornisce i [**metodi CreateBitmapFromWicBitmap,**](id2d1rendertarget-createbitmapfromwicbitmap.md) [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)e [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) per la modifica delle bitmap WIC.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'interoperabilità di Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[Panoramica sull'interoperabilità tra Direct2D e Direct3D](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 