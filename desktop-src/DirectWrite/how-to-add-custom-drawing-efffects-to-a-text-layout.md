---
title: Come aggiungere effetti di disegno client a un layout di testo
description: Fornisce una breve esercitazione sull'aggiunta di effetti di disegno dei client a un'applicazione DirectWrite che Visualizza il testo usando l'interfaccia IDWriteTextLayout e un renderer di testo personalizzato.
ms.assetid: b66ff814-2113-48b0-8913-3d30a5d20077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338dc1a720bde80c1daf2b4baf7c7a4bad6d2cff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046999"
---
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a>Come aggiungere effetti di disegno client a un layout di testo

Fornisce una breve esercitazione sull'aggiunta di effetti di disegno dei client a un'applicazione [DirectWrite](direct-write-portal.md) che Visualizza il testo usando l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e un renderer di testo personalizzato.

Il prodotto finale di questa esercitazione è un'applicazione che Visualizza il testo con intervalli di testo con un effetto di disegno colore diverso per ogni, come illustrato nello screenshot seguente.

![Screenshot di "esempio di effetto di disegno client!" in colori diversi](images/drawingeffects.png)

> [!Note]  
> Questa esercitazione è destinata a essere un esempio semplificato della creazione di effetti di disegno client personalizzati, non di un esempio di un metodo semplice per il disegno del testo dei colori. Per ulteriori informazioni, vedere la pagina di riferimento [**IDWriteTextLayout:: SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) .

 

Questa esercitazione contiene le parti seguenti:

-   [Passaggio 1: creare un layout di testo](#step-1-create-a-text-layout)
-   [Passaggio 2: implementare una classe di effetto di disegno personalizzata](#step-2-implement-a-custom-drawing-effect-class)
-   [Passaggio 3: implementare una classe renderer di testo personalizzato](#step-3-implement-a-custom-text-renderer-class)
    -   [Costruttore](#the-constructor)
    -   [Metodo DrawGlyphRun](#the-drawglyphrun-method)
    -   [Distruttore](#the-destructor)
-   [Passaggio 4: creare il renderer di testo](#step-4-create-the-text-renderer)
-   [Passaggio 5: creare un'istanza degli oggetti effetto disegno colori](#step-5-instantiate-the-color-drawing-effect-objects)
-   [Passaggio 6: impostare l'effetto di disegno per intervalli di testo specifici](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [Passaggio 7: creare il layout del testo usando il renderer personalizzato](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [Passaggio 8: eseguire la pulizia](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a>Passaggio 1: creare un layout di testo

Per iniziare, sarà necessaria un'applicazione con un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Se è già presente un'applicazione che visualizza testo con un layout di testo o si usa il codice di esempio DrawingEffect personalizzato, andare al passaggio 2.

Per aggiungere un layout di testo è necessario eseguire le operazioni seguenti:

1.  Dichiarare un puntatore a un'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) come membro della classe.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  Alla fine del metodo **CreateDeviceIndependentResources** , creare un oggetto interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiamando il metodo [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

3.  Infine, ricordarsi di rilasciare il layout del testo nel distruttore.
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a>Passaggio 2: implementare una classe di effetto di disegno personalizzata

Oltre ai metodi ereditati da IUnknown, un'interfaccia dell'effetto di disegno client personalizzata non ha alcun requisito per quanto riguarda gli elementi che devono implementare. In questo caso, la classe **ColorDrawingEffect** include semplicemente un [**valore \_ \_ F di colore d2d1**](../direct2d/d2d1-color-f.md) e dichiara i metodi per ottenere e impostare questo valore, nonché un costruttore che può impostare inizialmente il colore.

Dopo l'applicazione di un effetto di disegno client a un intervallo di testo in un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , l'effetto di disegno viene passato al metodo [**IDWriteTextRenderer::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) di qualsiasi operazione di glifo di cui eseguire il rendering. I metodi dell'effetto di disegno sono quindi disponibili per il renderer di testo.

Un effetto di disegno del client può essere complesso quanto si vuole, portando più informazioni rispetto a questo esempio, oltre a fornire metodi per modificare i glifi, creare oggetti da usare per il disegno e così via.

## <a name="step-3-implement-a-custom-text-renderer-class"></a>Passaggio 3: implementare una classe renderer di testo personalizzato

Per sfruttare i vantaggi di un effetto di disegno client, è necessario implementare un renderer di testo personalizzato. Questo renderer di testo applicherà l'effetto di disegno passato tramite il metodo [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) all'esecuzione del glifo che si sta disegnando.

### <a name="the-constructor"></a>Costruttore

Il costruttore per il renderer di testo personalizzato archivia l'oggetto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) che verrà utilizzato per creare oggetti [Direct2D](../direct2d/direct2d-portal.md) e la destinazione di rendering Direct2D su cui verrà disegnato il testo.


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
}
```



### <a name="the-drawglyphrun-method"></a>Metodo DrawGlyphRun

Un'esecuzione di glifo è un set di glifi che condividono lo stesso formato, incluso l'effetto di disegno del client. Il metodo [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) prende in considerazione il rendering del testo per un'esecuzione del glifo specificata.

Per prima cosa, creare un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)e quindi recuperare la struttura di esecuzione del glifo usando [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline). Trasformare quindi l'origine della geometria usando il metodo [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory:: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) , come illustrato nel codice seguente.


```C++
HRESULT hr = S_OK;

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

// Close the geometry sink
if (SUCCEEDED(hr))
{
    hr = pSink->Close();
}

// Initialize a matrix to translate the origin of the glyph run.
D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
    1.0f, 0.0f,
    0.0f, 1.0f,
    baselineOriginX, baselineOriginY
    );

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



Dichiarare quindi un oggetto pennello a tinta unita [Direct2D](../direct2d/direct2d-portal.md) .


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



Se il parametro *clientDrawingEffect* non è null, eseguire una query sull'oggetto per l'interfaccia **ColorDrawingEffect** . Questa operazione funzionerà perché la classe verrà impostata come effetto di disegno del client sugli intervalli di testo dell'oggetto layout di testo.

Una volta ottenuto un puntatore all'interfaccia **ColorDrawingEffect** , è possibile recuperare il valore di [**d2d1 \_ Color \_ F**](../direct2d/d2d1-color-f.md) che archivia usando il metodo **GetColor** . Usare quindi il **\_ colore \_ F di d2d1** per creare un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) in tale colore.

Se il parametro *clientDrawingEffect* è **null**, è sufficiente creare un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)nero.


```C++
// If there is a drawing effect create a color brush using it, otherwise create a black brush.
if (clientDrawingEffect != NULL)
{
    // Go from IUnknown to ColorDrawingEffect.
    ColorDrawingEffect *colorDrawingEffect;

    clientDrawingEffect->QueryInterface(__uuidof(ColorDrawingEffect), reinterpret_cast<void**>(&colorDrawingEffect));

    // Get the color from the ColorDrawingEffect object.
    D2D1_COLOR_F color;

    colorDrawingEffect->GetColor(&color);

    // Create the brush using the color pecified by our ColorDrawingEffect object.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            color,
            &pBrush);
    }

    SafeRelease(&colorDrawingEffect);
}
else
{
    // Create a black brush.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            D2D1::ColorF(
            D2D1::ColorF::Black
            ),
            &pBrush);
    }
}
```



Infine, disegnare la geometria del contorno e riempirla usando il pennello a tinta unita appena creato.


```C++
if (SUCCEEDED(hr))
{
    // Draw the outline of the glyph run
    pRT_->DrawGeometry(
        pTransformedGeometry,
        pBrush
        );

    // Fill in the glyph run
    pRT_->FillGeometry(
        pTransformedGeometry,
        pBrush
        );
}
```



### <a name="the-destructor"></a>Distruttore

Non dimenticare di rilasciare la factory [Direct2D](../direct2d/direct2d-portal.md) e la destinazione di rendering nel distruttore.


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a>Passaggio 4: creare il renderer di testo

Nelle risorse **CreateDeviceDependent** creare l'oggetto renderer di testo personalizzato. È dipendente dal dispositivo perché usa **ID2D1RenderTarget**, che è a sua volta dipendente dal dispositivo.


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a>Passaggio 5: creare un'istanza degli oggetti effetto disegno colori

Crea un'istanza degli oggetti **ColorDrawingEffect** in rosso, verde e blu.


```C++
// Instantiate some custom color drawing effects.
redDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Red
        )
    );

blueDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Blue
        )
    );

greenDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Green
        )
    );
```



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a>Passaggio 6: impostare l'effetto di disegno per intervalli di testo specifici

Impostare l'effetto di disegno per intervalli di testo specifici usando il metodo [**IDWriteTextLayou:: SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) e uno struct dell' [**\_ \_ intervallo di testo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) .


```C++
// Set the drawing effects.

// Red.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {0,
                                   14};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(redDrawingEffect_, textRange);
    }
}

// Blue.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {14,
                                   7};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(blueDrawingEffect_, textRange);
    }
}

// Green.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {21,
                                   8};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(greenDrawingEffect_, textRange);
    }
}
```



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a>Passaggio 7: creare il layout del testo usando il renderer personalizzato

È necessario chiamare il metodo [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) anziché i metodi [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) o [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) .


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a>Passaggio 8: eseguire la pulizia

Nel distruttore DemoApp rilasciare il renderer di testo personalizzato.


```C++
SafeRelease(&pTextRenderer_);
```



Successivamente, aggiungere il codice per rilasciare le classi dell'effetto di disegno del client.


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 