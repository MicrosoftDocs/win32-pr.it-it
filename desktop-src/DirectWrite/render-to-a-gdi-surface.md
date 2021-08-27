---
title: Eseguire il rendering in una superficie GDI
description: Eseguire il rendering in una superficie GDI
ms.assetid: a6096ff5-1e6e-4edb-b455-ea5d205072ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20df241e379e9a133cb662ea141fa27c86a4bb486c8ffba311423cb9afd83fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048491"
---
# <a name="render-to-a-gdi-surface"></a>Eseguire il rendering in una superficie GDI

In alcuni casi, potrebbe essere necessario essere in grado di visualizzare [DirectWrite](direct-write-portal.md) testo su una superficie GDI. [**L'interfaccia IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) incapsula una bitmap e un contesto di dispositivo in cui eseguire il rendering del testo. Per creare un **OGGETTO IDWriteBitmapRenderTarget,** usare il metodo [**IDWriteGdiInterop::CreateBitmapRenderTarget,**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) come illustrato nel codice seguente.


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



Per eseguire il rendering con [**IDWriteBitmapRenderTarget,**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)è necessario implementare un'interfaccia di callback del renderer di testo personalizzata derivata [**dall'interfaccia IDWriteTextRenderer.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) È necessario implementare metodi per disegnare un'esecuzione, una sottolineatura, un barrato, oggetti inline e così via. Per un elenco completo dei metodi, vedere la pagina di riferimento [**IDWriteTextRenderer.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) Non tutti i metodi devono essere implementati, ma solo **restituire E \_ NOTIMPL** e il disegno continuerà.

È quindi possibile disegnare il testo usando il [**metodo IDWriteTextLayout::D raw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) e passando l'interfaccia di callback implementata come parametro. Il **metodo IDWriteTextLayout::D raw** chiama i metodi del callback del renderer personalizzato specificato. I [**metodi DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)e [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) eseguono le funzioni di disegno.

Nell'implementazione di [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)chiamare il metodo [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) per disegnare i glifi. Il rendering degli oggetti underline, strikethrough e inline deve essere eseguito dal renderer personalizzato.

[**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) ha un parametro RECT out facoltativo che contiene i limiti dell'area in cui è stato disegnato il testo. È possibile usare queste informazioni per impostare il rettangolo di delimitazione per il contesto di dispositivo con la [**funzione SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) fornita da GDI. Il codice seguente è un esempio di implementazione del [**metodo DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) di un renderer personalizzato.


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



Il [**rendering dell'interfaccia IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) viene eseguito in un contesto di dispositivo (DC) in memoria. Per ottenere un handle per questo controller di dominio, usare il [**metodo IDWriteBitmapRenderTarget::GetMemoryDC.**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) Non appena il disegno è stato eseguito, il controller di dominio di memoria dell'oggetto **IDWriteBitmapRenderTarget** deve essere copiato nella superficie GDI di destinazione.

È possibile recuperare il rettangolo di delimitazione usando la [**funzione GetBoundsRect,**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) quindi usare il rettangolo di delimitazione con la funzione [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) per copiare il testo DirectWrite di cui è stato eseguito il rendering dal controller di dominio di memoria alla superficie GDI, come illustrato nel codice seguente. [](direct-write-portal.md)


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



 

 