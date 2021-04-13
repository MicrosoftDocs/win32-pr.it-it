---
title: Rendering in una superficie GDI
description: Rendering in una superficie GDI
ms.assetid: a6096ff5-1e6e-4edb-b455-ea5d205072ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff292feb2250a4dd81abeb62d8ee48ebfb4488b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399640"
---
# <a name="render-to-a-gdi-surface"></a>Rendering in una superficie GDI

In alcuni casi, potrebbe essere necessario poter visualizzare il testo [DirectWrite](direct-write-portal.md) su una superficie GDI. L'interfaccia [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) incapsula una bitmap e un contesto di dispositivo su cui eseguire il rendering del testo. Per creare un **IDWriteBitmapRenderTarget** , usare il metodo [**IDWriteGdiInterop:: CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) , come illustrato nel codice seguente.


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



Per eseguire il rendering con un [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget), è necessario implementare un'interfaccia di callback del renderer di testo personalizzata derivata dall'interfaccia [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) . È necessario implementare metodi per disegnare un'esecuzione del glifo, una sottolineatura, una barratura, oggetti inline e così via. Per un elenco completo dei metodi, vedere la pagina di riferimento di [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) . Non tutti i metodi devono essere implementati, possono solo restituire **e \_ NOTIMPL** e il disegno continuerà.

È quindi possibile creare il testo usando il metodo [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) e passando l'interfaccia di callback implementata come parametro. Il metodo **IDWriteTextLayout::D RAW** chiama i metodi del callback del renderer personalizzato fornito. I metodi [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)e [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) eseguono le funzioni di disegno.

Nell'implementazione di [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)chiamare il metodo [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) per creare i glifi. Il rendering degli oggetti Underline, barrato e inline deve essere eseguito dal renderer personalizzato.

[**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) ha un parametro di uscita Rect facoltativo che contiene i limiti dell'area in cui è stato disegnato il testo. È possibile usare queste informazioni per impostare il rettangolo di delimitazione per il contesto di dispositivo con la funzione [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) fornita da GDI. Il codice seguente è un'implementazione di esempio del metodo [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) di un renderer personalizzato.


```C++
STDMETHODIMP GdiTextRenderer::DrawGlyphRun(
    __maybenull void* clientDrawingContext,
    FLOAT baselineOriginX,
    FLOAT baselineOriginY,
    DWRITE_MEASURING_MODE measuringMode,
    __in DWRITE_GLYPH_RUN const* glyphRun,
    __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
    IUnknown* clientDrawingEffect
    )
{
    HRESULT hr = S_OK;

    // Pass on the drawing call to the render target to do the real work.
    RECT dirtyRect = {0};

    hr = pRenderTarget_->DrawGlyphRun(
        baselineOriginX,
        baselineOriginY,
        measuringMode,
        glyphRun,
        pRenderingParams_,
        RGB(0,200,255),
        &dirtyRect
        );
    

    return hr;
}
```



L'interfaccia [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) esegue il rendering in un contesto di dispositivo (DC) in memoria. Si ottiene un handle per il controller di dominio usando il metodo [**IDWriteBitmapRenderTarget:: GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) . Non appena il disegno è stato eseguito, il controller di dominio della memoria dell'oggetto **IDWriteBitmapRenderTarget** deve essere copiato nella superficie GDI di destinazione.

È possibile recuperare il rettangolo di delimitazione utilizzando la funzione [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) , quindi utilizzare il rettangolo di delimitazione con la funzione [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) per copiare il testo [DirectWrite](direct-write-portal.md) sottoposto a rendering dal controller di dominio della memoria alla superficie GDI, come illustrato nel codice seguente.


```C++
// Transfer from DWrite's rendering target to the window.
BitBlt(
    hdc,
    0, 0,
    size.cx, size.cy,
    memoryHdc,
    0, 0, 
    SRCCOPY | NOMIRRORBITMAP
    );
```



 

 