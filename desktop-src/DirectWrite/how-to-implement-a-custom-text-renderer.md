---
title: Eseguire il rendering usando un renderer di testo personalizzato
description: Un DirectWrite \ 160; il layout del testo può essere disegnato da un renderer di testo personalizzato derivato da IDWriteTextRenderer.
ms.assetid: a5b09733-24b2-408e-a1f9-cf7ad20c5c63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cda56fc5cc38a62e48a2f62066edfec2327e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399309"
---
# <a name="render-using-a-custom-text-renderer"></a>Eseguire il rendering usando un renderer di testo personalizzato

Un [](direct-write-portal.md) [**layout di testo**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) DirectWrite può essere disegnato da un renderer di testo personalizzato derivato da [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer). È necessario un renderer personalizzato per sfruttare le funzionalità avanzate di DirectWrite, ad esempio il rendering in una bitmap o in una superficie GDI, oggetti inline ed effetti di disegno dei client. In questa esercitazione vengono descritti i metodi di **IDWriteTextRenderer** e viene fornita un'implementazione di esempio che utilizza [Direct2D](../direct2d/direct2d-portal.md) per eseguire il rendering del testo con un riempimento bitmap.

Questa esercitazione contiene le parti seguenti:

-   [Costruttore](#the-constructor)
-   [DrawGlyphRun ()](#drawglyphrun)
-   [DrawUnderline () e DrawStrikethrough ()](#drawunderline-and-drawstrikethrough)
-   [Allineamento pixel, pixel per DIP e trasformazione](#pixel-snapping-pixels-per-dip-and-transform)
    -   [IsPixelSnappingDisabled()](#ispixelsnappingdisabled)
    -   [GetCurrentTransform()](#getcurrenttransform)
    -   [GetPixelsPerDip()](#getpixelsperdip)
-   [DrawInlineObject()](#drawinlineobject)
-   [Distruttore](#the-destructor)
-   [Uso del renderer di testo personalizzato](#using-the-custom-text-renderer)

Il renderer di testo personalizzato deve implementare i metodi ereditati da IUnknown oltre ai metodi elencati nella pagina di riferimento [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) e di seguito.

Per il codice sorgente completo per il renderer di testo personalizzato, vedere i file CustomTextRenderer. cpp e CustomTextRenderer. h dell' [esempio DirectWrite Hello World](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="the-constructor"></a>Costruttore

Il renderer di testo personalizzato richiede un costruttore. In questo esempio vengono utilizzati pennelli [Direct2D](../direct2d/direct2d-portal.md) a tinta unita e bitmap per eseguire il rendering del testo.

Per questo motivo, il costruttore accetta i parametri trovati nella tabella seguente con le descrizioni.



| Parametro       | Descrizione                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *pD2DFactory*   | Puntatore a un oggetto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) che verrà usato per creare le risorse Direct2D necessarie.                                                                                                        |
| *pRT*           | Puntatore all'oggetto [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) di cui verrà eseguito il rendering del testo. |
| *pOutlineBrush* | Puntatore a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) che verrà usato per disegnare il contorno del testo                                                                                                                     |
| *pFillBrush*    | Puntatore a [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) che verrà usato per riempire il testo.                                                                                                                                      |



 

Questi verranno archiviati dal costruttore, come illustrato nel codice seguente.


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT, 
    ID2D1SolidColorBrush* pOutlineBrush, 
    ID2D1BitmapBrush* pFillBrush
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT), 
pOutlineBrush_(pOutlineBrush), 
pFillBrush_(pFillBrush)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
    pOutlineBrush_->AddRef();
    pFillBrush_->AddRef();
}
```



## <a name="drawglyphrun"></a>DrawGlyphRun ()

Il metodo [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) è il metodo di callback principale del renderer di testo. Viene passata un'esecuzione di glifi da sottoposta a rendering, oltre a informazioni quali l'origine e la modalità di misurazione della linea di base. Passa inoltre un oggetto effetto di disegno client da applicare all'esecuzione del glifo. Per ulteriori informazioni, vedere l'argomento [How to Add client Drawing Effects to a text layout](how-to-add-custom-drawing-efffects-to-a-text-layout.md) .

Questa implementazione del renderer di testo esegue il rendering delle esecuzioni del glifo mediante la conversione in geometrie [Direct2D](rendering-by-using-direct2d.md) e quindi il disegno e il riempimento delle geometrie. Questa operazione è costituita dai passaggi seguenti.

1.  Creare un oggetto [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e quindi recuperare l'oggetto [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) usando il metodo [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .

    ```C++
    // Create the path geometry.
    ID2D1PathGeometry* pPathGeometry = NULL;
    hr = pD2DFactory_->CreatePathGeometry(
            &pPathGeometry
            );

    // Write to the path geometry using the geometry sink.
    ID2D1GeometrySink* pSink = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Open(
            &pSink
            );
    }
    ```

    

2.  L' [**\_ \_ esecuzione del glifo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) passata a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contiene un oggetto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) , denominato *fontFace*, che rappresenta il tipo di carattere per l'intera esecuzione del glifo. Inserire il contorno del glifo eseguito nel sink di geometria usando il metodo [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , come illustrato nel codice seguente.

    ```C++
    // Get the glyph run outline geometries back from DirectWrite and place them within the
    // geometry sink.
    if (SUCCEEDED(hr))
    {
        hr = glyphRun->fontFace->GetGlyphRunOutline(
            glyphRun->fontEmSize,
            glyphRun->glyphIndices,
            glyphRun->glyphAdvances,
            glyphRun->glyphOffsets,
            glyphRun->glyphCount,
            glyphRun->isSideways,
            glyphRun->bidiLevel%2,
            pSink
            );
    }
    ```

    

3.  Dopo aver compilato il sink di geometria, chiuderlo.

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  L'origine dell'esecuzione del glifo deve essere convertita in modo che venga sottoposta a rendering dall'origine di base corretta, come illustrato nel codice seguente.

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    *BaselineOriginX* e *baselineOriginY* vengono passati come parametri al metodo di callback [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .

5.  Creare la geometria trasformata usando il metodo [**ID2D1Factory:: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) e passando la geometria del percorso e la matrice di traslazione.

    ```C++
    // Create the transformed geometry
    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pPathGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

6.  Infine, disegnare la struttura della geometria trasformata e riempirla usando i metodi [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) e i pennelli [Direct2D](../direct2d/direct2d-portal.md) archiviati come variabili membro.

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

7.  Ora che è stata completata la creazione, non dimenticare di pulire gli oggetti creati in questo metodo.

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a>DrawUnderline () e DrawStrikethrough ()

[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) dispone anche di callback per disegnare la sottolineatura e la barratura. Questo esempio disegna un rettangolo semplice per una sottolineatura o una barratura, ma è possibile disegnare altre forme.

Il disegno di una sottolineatura tramite [Direct2D](../direct2d/direct2d-portal.md) è costituito dai passaggi seguenti.

1.  Per prima cosa, creare una struttura [**d2d1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) con le dimensioni e la forma della sottolineatura. La struttura di [**\_ sottolineatura DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) passata al metodo di callback [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) fornisce l'offset, la larghezza e lo spessore della sottolineatura.

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  Successivamente, creare un oggetto [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) usando il metodo [**ID2D1Factory:: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) e la struttura di [**d2d1 \_ Rect \_ F**](../direct2d/d2d1-rect-f.md) inizializzata.

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  Come per l'esecuzione del glifo, l'origine della geometria di sottolineatura deve essere convertita in base ai valori di origine della linea di base, usando il metodo [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) .

    ```C++
    // Initialize a matrix to translate the origin of the underline
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );

    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pRectangleGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

4.  Infine, disegnare la struttura della geometria trasformata e riempirla usando i metodi [**ID2D1RenderTarget::D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**ID2D1RenderTarget:: FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) e i pennelli [Direct2D](../direct2d/direct2d-portal.md) archiviati come variabili membro.

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

5.  Ora che è stata completata la creazione, non dimenticare di pulire gli oggetti creati in questo metodo.

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

Il processo di disegno di un barrato è lo stesso. Tuttavia, la barratura avrà un offset diverso e probabilmente una larghezza e uno spessore differenti.

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a>Allineamento pixel, pixel per DIP e trasformazione

### <a name="ispixelsnappingdisabled"></a>IsPixelSnappingDisabled()

Questo metodo viene chiamato per determinare se il blocco del pixel è disabilitato. Il valore predefinito consigliato è **false** ed è l'output di questo esempio.


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a>GetCurrentTransform()

In questo esempio viene eseguito il rendering in una destinazione di rendering Direct2D, quindi la trasformazione viene reindirizzata dalla destinazione di rendering utilizzando [**ID2D1RenderTarget:: GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a>GetPixelsPerDip()

Questo metodo viene chiamato per ottenere il numero di pixel per ogni DIP (device independent pixel).


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a>DrawInlineObject()

Un renderer di testo personalizzato dispone anche di un callback per disegnare oggetti inline. In questo esempio, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) restituisce E \_ NOTIMPL. Una spiegazione di come creare oggetti inline esula dall'ambito di questa esercitazione. Per ulteriori informazioni, vedere l'argomento [come aggiungere oggetti inline a un layout di testo](how-to-add-inline-objects-to-a-text-layout.md) .

## <a name="the-destructor"></a>Distruttore

È importante rilasciare tutti i puntatori usati dalla classe renderer del testo personalizzato.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a>Uso del renderer di testo personalizzato

Per eseguire il rendering con il renderer personalizzato, usare il metodo [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) , che accetta un'interfaccia di callback derivata da [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) come argomento, come illustrato nel codice seguente.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



Il metodo [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) chiama i metodi del callback del renderer personalizzato fornito. I metodi [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)e [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) descritti in precedenza eseguono le funzioni di disegno.

 

 