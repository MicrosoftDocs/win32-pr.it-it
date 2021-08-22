---
title: Come aggiungere effetti di disegno client a un layout di testo
description: Viene fornita una breve esercitazione sull'aggiunta di effetti di disegno client a un'applicazione DirectWrite che visualizza testo usando l'interfaccia IDWriteTextLayout e un renderer di testo personalizzato.
ms.assetid: b66ff814-2113-48b0-8913-3d30a5d20077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bae98813d8f8aa8fc8a7df0a1a53d11a0329c93abb22a7f60d60754b8edc91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071711"
---
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a>Come aggiungere effetti di disegno client a un layout di testo

Viene fornita una breve esercitazione sull'aggiunta di effetti di disegno client a un'applicazione [DirectWrite](direct-write-portal.md) che visualizza testo usando l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e un renderer di testo personalizzato.

Il prodotto finale di questa esercitazione è un'applicazione che visualizza testo con intervalli di testo con un effetto di disegno di colore diverso su ognuno, come illustrato nello screenshot seguente.

![Screenshot di "esempio di effetto di disegno client!" in colori diversi](images/drawingeffects.png)

> [!Note]  
> Questa esercitazione ha lo scopo di essere un esempio semplificato di come creare effetti di disegno client personalizzati, non un esempio di metodo semplice per disegnare testo a colori. Per altre informazioni, vedere la pagina di riferimento [**IDWriteTextLayout::SetDrawingEffect.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect)

 

Questa esercitazione contiene le parti seguenti:

-   [Passaggio 1: Creare un layout di testo](#step-1-create-a-text-layout)
-   [Passaggio 2: Implementare una classe dell'effetto di disegno personalizzato](#step-2-implement-a-custom-drawing-effect-class)
-   [Passaggio 3: Implementare una classe renderer di testo personalizzato](#step-3-implement-a-custom-text-renderer-class)
    -   [Costruttore](#the-constructor)
    -   [Metodo DrawGlyphRun](#the-drawglyphrun-method)
    -   [Distruttore](#the-destructor)
-   [Passaggio 4: Creare il renderer di testo](#step-4-create-the-text-renderer)
-   [Passaggio 5: Creare un'istanza degli oggetti Effetto disegno colori](#step-5-instantiate-the-color-drawing-effect-objects)
-   [Passaggio 6: Impostare l'effetto di disegno per intervalli di testo specifici](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [Passaggio 7: Disegnare il layout del testo usando il renderer personalizzato](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [Passaggio 8: Pulire](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a>Passaggio 1: Creare un layout di testo

Per iniziare, è necessaria un'applicazione con un [**oggetto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) Se si ha già un'applicazione che visualizza testo con un layout di testo o si usa il codice di esempio DrawingEffect personalizzato, andare al passaggio 2.

Per aggiungere un layout di testo, è necessario eseguire le operazioni seguenti:

1.  Dichiarare un puntatore a [**un'interfaccia IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) come membro della classe .
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  Alla fine del metodo **CreateDeviceIndependentResources** creare un oggetto interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiamando il [**metodo CreateTextLayout.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)
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

    

3.  Infine, ricordarsi di rilasciare il layout di testo nel distruttore.
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a>Passaggio 2: Implementare una classe dell'effetto di disegno personalizzato

A parte i metodi ereditati da IUnknown, un'interfaccia dell'effetto di disegno client personalizzata non ha requisiti in base a ciò che deve implementare. In questo caso, la classe **ColorDrawingEffect** contiene semplicemente un valore [**D2D1 \_ COLOR \_ F**](../direct2d/d2d1-color-f.md) e dichiara i metodi per ottenere e impostare questo valore, nonché un costruttore che può impostare inizialmente il colore.

Dopo l'applicazione di un effetto di disegno client a un intervallo di testo in un oggetto [**IDWriteTextLayout,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) l'effetto di disegno viene passato al metodo [**IDWriteTextRenderer::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) di qualsiasi esecuzione del glifo di cui eseguire il rendering. I metodi dell'effetto di disegno sono quindi disponibili per il renderer di testo.

Un effetto di disegno client può essere complesso quanto si vuole, con più informazioni rispetto a questo esempio, oltre a fornire metodi per modificare i glifi, creare oggetti da usare per il disegno e così via.

## <a name="step-3-implement-a-custom-text-renderer-class"></a>Passaggio 3: Implementare una classe renderer di testo personalizzato

Per sfruttare i vantaggi di un effetto di disegno client, è necessario implementare un renderer di testo personalizzato. Questo renderer di testo applierà l'effetto di disegno passato dal metodo [**IDWriteTextLayout::D raw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) all'esecuzione del glifo da disegnare.

### <a name="the-constructor"></a>Costruttore

Il costruttore per il renderer di testo personalizzato archivia l'oggetto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) che verrà usato per creare oggetti [Direct2D](../direct2d/direct2d-portal.md) e la destinazione di rendering Direct2D su cui verrà disegnato il testo.


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

Un'esecuzione di glifi è un set di glifi che condividono lo stesso formato, incluso l'effetto di disegno del client. Il [**metodo DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) si occupa del rendering del testo per un'esecuzione del glifo specificata.

Creare prima di tutto [**id2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)e quindi recuperare la struttura di esecuzione del glifo usando [**IDWriteFontFace::GetGlyphRunOutline.**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) Trasformare quindi l'origine della geometria usando il metodo [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory::CreateTransformedGeometry,**](../direct2d/id2d1factory-createtransformedgeometry.md) come illustrato nel codice seguente.


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



Dichiarare quindi un oggetto pennello a tinta [unita Direct2D.](../direct2d/direct2d-portal.md)


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



Se il *parametro clientDrawingEffect* non è NULL, eseguire una query sull'oggetto per **l'interfaccia ColorDrawingEffect.** Questa operazione funzionerà perché questa classe verrà impostata come effetto di disegno del client sugli intervalli di testo dell'oggetto layout di testo.

Dopo aver creato un puntatore all'interfaccia **ColorDrawingEffect,** è possibile recuperare il valore [**COLOR \_ \_ F D2D1**](../direct2d/d2d1-color-f.md) archiviato usando il **metodo GetColor.** Usare quindi **D2D1 \_ COLOR \_ F** per creare un [**oggetto ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) in tale colore.

Se il *parametro clientDrawingEffect* è **NULL,** è sufficiente creare un [**oggetto ID2D1SolidColorBrush nero.**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)


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



## <a name="step-4-create-the-text-renderer"></a>Passaggio 4: Creare il renderer di testo

Nelle risorse **CreateDeviceDependent** creare l'oggetto renderer di testo personalizzato. Dipende dal dispositivo perché usa **ID2D1RenderTarget,** che è a sua stessa dipendente dal dispositivo.


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a>Passaggio 5: Creare un'istanza degli oggetti Effetto disegno colori

Creare **un'istanza degli oggetti ColorDrawingEffect** in rosso, verde e blu.


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



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a>Passaggio 6: Impostare l'effetto di disegno per intervalli di testo specifici

Impostare l'effetto di disegno per intervalli di testo specifici usando il metodo [**IDWriteTextLayou::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) e uno struct [**DWRITE \_ TEXT \_ RANGE.**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range)


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



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a>Passaggio 7: Disegnare il layout del testo usando il renderer personalizzato

È necessario chiamare il [**metodo IDWriteTextLayout::D raw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) anziché i metodi [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) o [**ID2D1RenderTarget::D rawTextLayout.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a>Passaggio 8: Pulire

Nel distruttore DemoApp rilasciare il renderer di testo personalizzato.


```C++
SafeRelease(&pTextRenderer_);
```



Successivamente, aggiungere il codice per rilasciare le classi dell'effetto di disegno client.


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 