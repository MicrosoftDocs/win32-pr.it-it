---
title: Cenni preliminari sull'interoperabilità
description: Riepiloga le diverse tecnologie che è possibile usare con Direct2D.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Direct2D, interoperatività GDI
- Direct2D, interoperatività GDI+
- Direct2D, interoperabilità
- Direct2D, interoperabilità DirectWrite
- interoperabilità, Direct2D
- interoperabilità, Direct3D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- interoperabilità, Graphics Device Interface (GDI)
- interoperabilità, GDI+
- Interoperabilità DirectWrite
- interoperabilità, DirectWrite
- Windows Imaging Component (WIC)
- WIC (componente Windows Imaging)
- interoperabilità, componente imaging Windows (WIC)
- Direct2D, interoperatività WIC
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6f56c570a837a541bac9467477d4f6009bda019e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399198"
---
# <a name="interoperability-overview"></a>Cenni preliminari sull'interoperabilità

Una delle funzionalità chiave di le convenzioni è l'abilitazione dell'interoperabilità tra Direct2D e altre piattaforme di rendering, in modo che gli sviluppatori possano usare i punti di forza specifici di ogni piattaforma senza essere costretti a compromettere la scelta di una piattaforma per tutte le esigenze. In questo argomento vengono riepilogate le diverse piattaforme con cui Direct2D è interoperativo. Include le sezioni seguenti:

-   [Interoperabilità GDI](#gdi-interoperability)
-   [Interoperabilità GDI+](#gdi-interoperability)
-   [Interoperabilità Direct3D](#direct3d-interoperability)
-   [Interoperabilità DirectWrite](#directwrite-interoperability)
-   [Interoperabilità di Windows Imaging Component (WIC)](#windows-imaging-component-wic-interoperability)
-   [Argomenti correlati](#related-topics)

Il diagramma seguente riepiloga le diverse piattaforme con cui Direct2D è interoperativo e elenca alcuni metodi e interfacce che forniscono l'interoperabilità.

![diagramma delle piattaforme con cui è interopera Direct2D, tra cui Direct3D 10,1, DirectWrite, WIC, GDI+ e GDI](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a>Interoperabilità GDI

Direct2D consente l'interoperabilità bidirezionale con GDI. È possibile utilizzare un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) per scrivere contenuto Direct2D in un [contesto di dispositivo](/windows/desktop/gdi/device-contexts) GDI (DC) oppure è possibile utilizzare [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) per ottenere una rappresentazione del controller di dominio di una destinazione di rendering.

Per ulteriori informazioni ed esempi, vedere [Cenni preliminari sull'interoperabilità Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md).

## <a name="gdi-interoperability"></a>Interoperabilità GDI+

È possibile utilizzare GDI+ con Direct2D in modo analogo a GDI. È possibile usare un [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) per scrivere contenuto Direct2D nello stesso controller di dominio del contenuto GDI+. Questo approccio consente di iniziare ad aggiungere contenuto Direct2D alle applicazioni che vengono principalmente sottoposte a rendering tramite GDI+.

È inoltre possibile utilizzare un [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) per fornire l'accesso a un controller di dominio GDI che scrive tramite Direct2D, quindi utilizzare il metodo [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) per creare un oggetto. Questo approccio è utile per le applicazioni che eseguono principalmente il rendering con Direct2D, ma hanno un modello di estendibilità o altri contenuti legacy che richiedono la possibilità di eseguire il rendering con GDI+.

## <a name="direct3d-interoperability"></a>Interoperabilità Direct3D

Direct2D può usare una destinazione di rendering della superficie DXGI (creata dal metodo [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ) per scrivere in un [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface). Questa azione consente di aggiungere sfondi e interfacce 2D a scene 3D e di usare il contenuto Direct2D come trama per un modello 3D. Direct2D può inoltre assumere un [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) e utilizzare il metodo [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) per creare una rappresentazione bitmap.

Per ulteriori informazioni ed esempi, vedere [Cenni preliminari sull'interoperabilità di Direct2D e Direct3D](direct2d-and-direct3d-interoperation-overview.md).

## <a name="directwrite-interoperability"></a>Interoperabilità DirectWrite

Direct2D è strettamente integrato con DirectWrite. Direct2D rende più semplice il rendering del contenuto DirectWrite fornendo i metodi [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)e [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) .

## <a name="windows-imaging-component-wic-interoperability"></a>Interoperabilità di Windows Imaging Component (WIC)

Direct2D fornisce i metodi [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)e [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) per la modifica delle bitmap di WIC.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'interoperabilità di Direct2D e GDI](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[Panoramica sull'interoperabilità tra Direct2D e Direct3D](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 