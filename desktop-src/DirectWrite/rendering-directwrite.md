---
title: Rendering DirectWrite
description: Rendering DirectWrite
ms.assetid: e8099fac-b5d7-4fb1-b06d-a6e85da0d1dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa640b8963c427b9eaf1d17fd3e4691115a3965d477c5076deb1f5eb05a569db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070591"
---
# <a name="rendering-directwrite"></a>Rendering DirectWrite

## <a name="rendering-options"></a>Opzioni di rendering

Il rendering del testo con formattazione descritta solo da un oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) può essere eseguito con [Direct2D,](../direct2d/direct2d-portal.md)tuttavia sono disponibili altre opzioni per il rendering di un [**oggetto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

È possibile eseguire il rendering della stringa descritta da un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando i metodi seguenti.

## <a name="1-render-using-direct2d"></a>1. Eseguire il rendering con Direct2D

Per eseguire il rendering di un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando Direct2D, usare il metodo [**ID2D1RenderTarget::D rawTextLayout,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) come illustrato nel codice seguente.


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



Per un'analisi più approfondita del disegno di un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) con [Direct2D,](../direct2d/direct2d-portal.md)vedere Attività iniziali [con DirectWrite](getting-started-with-directwrite.md).

## <a name="2-render-using-a-custom-text-renderer"></a>2. Eseguire il rendering usando un renderer di testo personalizzato.

Il rendering viene eseguito con un renderer personalizzato usando il metodo [**IDWriteTextLayout::D raw,**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) che accetta un'interfaccia di callback derivata da [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) come argomento, come illustrato nel codice seguente.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



Il [**metodo IDWriteTextLayout::D raw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) chiama i metodi del callback del renderer personalizzato fornito. I [**metodi DrawGlyphRun,**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) [**DrawUnderline,**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)e [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) eseguono le funzioni di disegno.

[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) dichiara i metodi per disegnare un'esecuzione di glifi, sottolineatura, barratura e oggetti inline. È l'applicazione a implementare questi metodi. La creazione di un renderer di testo personalizzato consente all'applicazione di applicare effetti aggiuntivi durante il rendering del testo, ad esempio un riempimento o un contorno personalizzato. Un renderer di testo personalizzato di esempio è incluso [nell'DirectWrite Hello World esempio](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="3-render-cleartype-to-a-gdi-surface"></a>3. Eseguire il rendering di ClearType su una superficie GDI.

Il rendering su una superficie GDI è in realtà un esempio di uso di un renderer di testo personalizzato. Tuttavia, parte del lavoro viene eseguito per l'utente sotto forma di [**interfaccia IDWriteBitmapRenderTarget.**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)

Per creare questa interfaccia, usare il [**metodo IDWriteGdiInterop::CreateBitmapRenderTarget.**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)

Il [**metodo DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) del renderer di testo personalizzato chiama il metodo [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) per disegnare i glifi. Il rendering degli oggetti sottolineato, barrato e inline deve essere eseguito dal renderer personalizzato.

[**L'interfaccia IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) esegue il rendering in un contesto di dispositivo (DC) in memoria. Per ottenere un handle per questo controller di dominio, usare il [**metodo IDWriteBitmapRenderTarget::GetMemoryDC.**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc)


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



Dopo aver eseguito il disegno, il controller di dominio di memoria dell'oggetto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) deve essere copiato nella superficie GDI di destinazione.

> [!Note]  
> È anche possibile trasferire la bitmap in un altro tipo di superficie, ad esempio una GDI+ superficie.

 


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



> [!Note]  
> L'app ha la responsabilità di eseguire il rendering di tutti gli elementi alla fine della finestra. Sono inclusi testo e grafica. Questa operazione ha una penalizzazione delle prestazioni. Inoltre, il rendering in un controller di dominio di memoria non è accelerato dall'hardware GDI.

 

Per una panoramica più dettagliata dell'interoperabilità con GDI, vedere [Interoperabilità con GDI.](interoperating-with-gdi.md)

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a>4. Eseguire il rendering del testo in scala di grigi in modo trasparente su una superficie GDI. (Windows 8 e versioni successive)

A partire da Windows 8, è possibile eseguire il rendering del testo in scala di grigi in modo trasparente su una superficie GDI per ottenere prestazioni migliori. A tale scopo, è necessario:

1.  Cancellare il controller di dominio di memoria in trasparente.
2.  Eseguire il rendering del testo nell'HDC di memoria usando l'antialiasing in scala di grigi (MODALITÀ \_ DWRITE TEXT \_ ANTIALIAS \_ \_ GRAYSCALE).
3.  Usare la [**funzione AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) per eseguire il rendering della memoria HDC in modo trasparente sopra l'HDC di destinazione finale.
4.  Ripetere il numero di volte necessario (ad esempio, una volta per ogni esecuzione del glifo) e tra un'altra grafica può essere eseguito il rendering direttamente nell'HDC di destinazione finale senza essere sovrascritto dalla funzione [**AlphaBlend.**](/windows/win32/api/wingdi/nf-wingdi-alphablend)


```C++
pRT_->SetTextAntialiasMode(DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE);

pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

BLENDFUNCTION blendFunction = { 0 };  
blendFunction.BlendOp = AC_SRC_OVER;  
blendFunction.SourceConstantAlpha = 255;  
blendFunction.AlphaFormat = AC_SRC_ALPHA;

AlphaBlend(  
        hdc,  
        0, 0,  
        width, height,  
        pRT_->GetMemoryDC(),  
        0, 0,  
        width, height,  
        blendFunction  
        );

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Eseguire il rendering con Direct2D](rendering-by-using-direct2d.md)
</dt> <dt>

[Eseguire il rendering usando un renderer di testo personalizzato](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[Eseguire il rendering su una superficie GDI](render-to-a-gdi-surface.md)
</dt> <dt>

[Interoperabilità con GDI](interoperating-with-gdi.md)
</dt> </dl>

 

 