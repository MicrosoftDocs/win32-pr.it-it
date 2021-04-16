---
title: Come aggiungere oggetti inline a un layout di testo
description: Fornisce una breve esercitazione sull'aggiunta di oggetti inline a un'applicazione DirectWrite che Visualizza il testo usando l'interfaccia IDWriteTextLayout.
ms.assetid: 6aa9d17c-ee30-497f-9c73-ec2fa079222b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d9ef34e38ec9b84afd887e565e76efb9618b88
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104551486"
---
# <a name="how-to-add-inline-objects-to-a-text-layout"></a>Come aggiungere oggetti inline a un layout di testo

Fornisce una breve esercitazione sull'aggiunta di oggetti inline a un'applicazione [DirectWrite](direct-write-portal.md) che Visualizza il testo usando l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Il prodotto finale di questa esercitazione è un'applicazione che Visualizza il testo con un'immagine inline incorporata, come illustrato nella schermata seguente.

![Screenshot di "esempio di oggetto inline" con un'immagine incorporata](images/inlineobject.png)

Questa esercitazione contiene le parti seguenti:

-   [Passaggio 1: creare un layout di testo.](#step-1-create-a-text-layout)
-   [Passaggio 2: definire una classe derivata dall'interfaccia IDWriteInlineObject.](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [Passaggio 3: implementare la classe di oggetti inline.](#step-3-implement-the-inline-object-class)
    -   [Costruttore.](#the-constructor)
    -   [Metodo di estrazione.](#the-draw-method)
    -   [Metodo GetMetrics.](#the-getmetrics-method)
    -   [Metodo GetOverhangMetrics.](#the-getoverhangmetrics-method)
    -   [Metodo GetBreakConditions.](#the-getbreakconditions-method)
-   [Passaggio 4: creare un'istanza della classe InlineImage e aggiungerla al layout di testo.](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a>Passaggio 1: creare un layout di testo.

Per iniziare, sarà necessaria un'applicazione con un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . Se è già presente un'applicazione che visualizza testo con un layout di testo, andare al passaggio 2.

Per aggiungere un layout di testo è necessario eseguire le operazioni seguenti:

1.  Dichiarare un puntatore a un'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) come membro della classe.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  Alla fine del metodo CreateDeviceIndependentResources, creare un oggetto interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiamando il metodo [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .
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

    

3.  Quindi, è necessario modificare la chiamata al metodo [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) in [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), come illustrato nel codice seguente.
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a>Passaggio 2: definire una classe derivata dall'interfaccia IDWriteInlineObject.

Il supporto per gli oggetti inline in [DirectWrite](direct-write-portal.md) viene fornito dall'interfaccia [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) . Per usare gli oggetti inline, è necessario implementare questa interfaccia. Gestisce il disegno dell'oggetto inline, oltre a fornire metriche e altre informazioni al renderer.

Creare un nuovo file di intestazione e dichiarare un'interfaccia denominata InlineImage, derivata da [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).

Oltre a QueryInterface, AddRef e Release ereditate da IUnknown, questa classe deve disporre dei metodi seguenti:

-   [**Disegna**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md)
-   [**GetBreakConditions**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a>Passaggio 3: implementare la classe di oggetti inline.

Creare un nuovo file C++, denominato InlineImage. cpp, per l'implementazione della classe. Oltre al metodo LoadBitmapFromFile e ai metodi ereditati dall'interfaccia IUnknown, la classe InlineImage è costituita dai metodi seguenti.

### <a name="the-constructor"></a>Costruttore.


```C++
InlineImage::InlineImage(
    ID2D1RenderTarget *pRenderTarget, 
    IWICImagingFactory *pIWICFactory,
    PCWSTR uri
    )
{
    // Save the render target for later.
    pRT_ = pRenderTarget;

    pRT_->AddRef();

    // Load the bitmap from a file.
    LoadBitmapFromFile(
        pRenderTarget,
        pIWICFactory,
        uri,
        &pBitmap_
        );
}
```



Il primo argomento del costruttore è il ID2D1RenderTarget in cui verrà eseguito il rendering dell'immagine inline. Questa operazione viene archiviata per essere usata in un secondo momento durante il disegno.

La destinazione di rendering, IWICImagingFactory, e l'URI del nome file vengono tutti passati al metodo LoadBitmapFromFile che carica la bitmap e archivia le dimensioni bitmap (larghezza e altezza) nella \_ variabile membro Rect.

### <a name="the-draw-method"></a>Metodo di estrazione.

Il metodo di [**disegno**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) è un callback chiamato dall'oggetto [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) quando è necessario disegnare l'oggetto inline. Il layout del testo non chiama direttamente questo metodo.


```C++
HRESULT STDMETHODCALLTYPE InlineImage::Draw(
    __maybenull void* clientDrawingContext,
    IDWriteTextRenderer* renderer,
    FLOAT originX,
    FLOAT originY,
    BOOL isSideways,
    BOOL isRightToLeft,
    IUnknown* clientDrawingEffect
    )
{
    float height    = rect_.bottom - rect_.top;
    float width     = rect_.right  - rect_.left;
    D2D1_RECT_F destRect  = {originX, originY, originX + width, originY + height};

    pRT_->DrawBitmap(pBitmap_, destRect);

    return S_OK;
}
```



In questo caso, la creazione della bitmap viene eseguita usando il metodo [**ID2D1RenderTarget::D rawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) ; Tuttavia, è possibile usare qualsiasi metodo per il disegno.

### <a name="the-getmetrics-method"></a>Metodo GetMetrics.


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetMetrics(
    __out DWRITE_INLINE_OBJECT_METRICS* metrics
    )
{
    DWRITE_INLINE_OBJECT_METRICS inlineMetrics = {};
    inlineMetrics.width     = rect_.right  - rect_.left;
    inlineMetrics.height    = rect_.bottom - rect_.top;
    inlineMetrics.baseline  = baseline_;
    *metrics = inlineMetrics;
    return S_OK;
}
```



Per il metodo [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) , archiviare la larghezza, l'altezza e la linea di base in una struttura di [**\_ \_ \_ metrica dell'oggetto inline DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) . [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiama questa funzione di callback per ottenere la misura dell'oggetto inline.

### <a name="the-getoverhangmetrics-method"></a>Metodo GetOverhangMetrics.


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetOverhangMetrics(
    __out DWRITE_OVERHANG_METRICS* overhangs
    )
{
    overhangs->left      = 0;
    overhangs->top       = 0;
    overhangs->right     = 0;
    overhangs->bottom    = 0;
    return S_OK;
}
```



In questo caso, non è necessario alcun sbalzo, quindi il metodo [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) restituisce tutti gli zeri.

### <a name="the-getbreakconditions-method"></a>Metodo GetBreakConditions.


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetBreakConditions(
    __out DWRITE_BREAK_CONDITION* breakConditionBefore,
    __out DWRITE_BREAK_CONDITION* breakConditionAfter
    )
{
    *breakConditionBefore = DWRITE_BREAK_CONDITION_NEUTRAL;
    *breakConditionAfter  = DWRITE_BREAK_CONDITION_NEUTRAL;
    return S_OK;
}
```



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a>Passaggio 4: creare un'istanza della classe InlineImage e aggiungerla al layout di testo.

Infine, nel metodo CreateDeviceDependentResources, creare un'istanza della classe InlineImage e aggiungerla al layout di testo. Poiché include un riferimento a [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), che è una risorsa dipendente dal dispositivo e il [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) viene creato usando la destinazione di rendering, il InlineImage è anche dipendente dal dispositivo e deve essere ricreato se la destinazione di rendering viene ricreata.


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



Il metodo [**IDWriteTextLayout:: SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) accetta una struttura di intervallo di testo. L'oggetto si applica all'intervallo specificato e qualsiasi testo nell'intervallo verrà eliminato. Se la lunghezza dell'intervallo di testo è 0, l'oggetto non verrà disegnato.

In questo esempio è presente un asterisco ( \* ) come segnaposto nella posizione in cui verrà visualizzata l'immagine.


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



Poiché la classe InlineImage dipende da [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), è necessario rilasciarla quando si rilascia la destinazione di rendering.


```C++
SafeRelease(&pInlineImage_);
```



 

 