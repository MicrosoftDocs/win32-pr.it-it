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
# <a name="how-to-add-inline-objects-to-a-text-layout"></a><span data-ttu-id="8ff59-103">Come aggiungere oggetti inline a un layout di testo</span><span class="sxs-lookup"><span data-stu-id="8ff59-103">How to Add Inline Objects to a Text Layout</span></span>

<span data-ttu-id="8ff59-104">Fornisce una breve esercitazione sull'aggiunta di oggetti inline a un'applicazione [DirectWrite](direct-write-portal.md) che Visualizza il testo usando l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="8ff59-104">Provides a short tutorial on adding inline objects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="8ff59-105">Il prodotto finale di questa esercitazione è un'applicazione che Visualizza il testo con un'immagine inline incorporata, come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="8ff59-105">The end product of this tutorial is an application that displays text with an inline image embedded in it, as shown in the following screen shot.</span></span>

![Screenshot di "esempio di oggetto inline" con un'immagine incorporata](images/inlineobject.png)

<span data-ttu-id="8ff59-107">Questa esercitazione contiene le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ff59-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="8ff59-108">Passaggio 1: creare un layout di testo.</span><span class="sxs-lookup"><span data-stu-id="8ff59-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="8ff59-109">Passaggio 2: definire una classe derivata dall'interfaccia IDWriteInlineObject.</span><span class="sxs-lookup"><span data-stu-id="8ff59-109">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [<span data-ttu-id="8ff59-110">Passaggio 3: implementare la classe di oggetti inline.</span><span class="sxs-lookup"><span data-stu-id="8ff59-110">Step 3: Implement the Inline Object Class.</span></span>](#step-3-implement-the-inline-object-class)
    -   [<span data-ttu-id="8ff59-111">Costruttore.</span><span class="sxs-lookup"><span data-stu-id="8ff59-111">The Constructor.</span></span>](#the-constructor)
    -   [<span data-ttu-id="8ff59-112">Metodo di estrazione.</span><span class="sxs-lookup"><span data-stu-id="8ff59-112">The Draw Method.</span></span>](#the-draw-method)
    -   [<span data-ttu-id="8ff59-113">Metodo GetMetrics.</span><span class="sxs-lookup"><span data-stu-id="8ff59-113">The GetMetrics Method.</span></span>](#the-getmetrics-method)
    -   [<span data-ttu-id="8ff59-114">Metodo GetOverhangMetrics.</span><span class="sxs-lookup"><span data-stu-id="8ff59-114">The GetOverhangMetrics Method.</span></span>](#the-getoverhangmetrics-method)
    -   [<span data-ttu-id="8ff59-115">Metodo GetBreakConditions.</span><span class="sxs-lookup"><span data-stu-id="8ff59-115">The GetBreakConditions Method.</span></span>](#the-getbreakconditions-method)
-   [<span data-ttu-id="8ff59-116">Passaggio 4: creare un'istanza della classe InlineImage e aggiungerla al layout di testo.</span><span class="sxs-lookup"><span data-stu-id="8ff59-116">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="8ff59-117">Passaggio 1: creare un layout di testo.</span><span class="sxs-lookup"><span data-stu-id="8ff59-117">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="8ff59-118">Per iniziare, sarà necessaria un'applicazione con un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="8ff59-118">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="8ff59-119">Se è già presente un'applicazione che visualizza testo con un layout di testo, andare al passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="8ff59-119">If you already have an application that displays text with a text layout, skip to Step 2.</span></span>

<span data-ttu-id="8ff59-120">Per aggiungere un layout di testo è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ff59-120">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="8ff59-121">Dichiarare un puntatore a un'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) come membro della classe.</span><span class="sxs-lookup"><span data-stu-id="8ff59-121">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="8ff59-122">Alla fine del metodo CreateDeviceIndependentResources, creare un oggetto interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiamando il metodo [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="8ff59-122">At the end of the CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
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

    

3.  <span data-ttu-id="8ff59-123">Quindi, è necessario modificare la chiamata al metodo [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) in [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="8ff59-123">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), as shown in the following code.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a><span data-ttu-id="8ff59-124">Passaggio 2: definire una classe derivata dall'interfaccia IDWriteInlineObject.</span><span class="sxs-lookup"><span data-stu-id="8ff59-124">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>

<span data-ttu-id="8ff59-125">Il supporto per gli oggetti inline in [DirectWrite](direct-write-portal.md) viene fornito dall'interfaccia [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) .</span><span class="sxs-lookup"><span data-stu-id="8ff59-125">Support for inline objects in [DirectWrite](direct-write-portal.md) is provided by the [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) interface.</span></span> <span data-ttu-id="8ff59-126">Per usare gli oggetti inline, è necessario implementare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="8ff59-126">To use inline objects, you must implement this interface.</span></span> <span data-ttu-id="8ff59-127">Gestisce il disegno dell'oggetto inline, oltre a fornire metriche e altre informazioni al renderer.</span><span class="sxs-lookup"><span data-stu-id="8ff59-127">It handles the drawing of the inline object, as well as providing metrics and other information to the renderer.</span></span>

<span data-ttu-id="8ff59-128">Creare un nuovo file di intestazione e dichiarare un'interfaccia denominata InlineImage, derivata da [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).</span><span class="sxs-lookup"><span data-stu-id="8ff59-128">Create a new header file and declare an interface called InlineImage, derived from [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).</span></span>

<span data-ttu-id="8ff59-129">Oltre a QueryInterface, AddRef e Release ereditate da IUnknown, questa classe deve disporre dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ff59-129">In addition to QueryInterface, AddRef, and Release inherited from IUnknown, this class must have the following methods:</span></span>

-   [<span data-ttu-id="8ff59-130">**Disegna**</span><span class="sxs-lookup"><span data-stu-id="8ff59-130">**Draw**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [<span data-ttu-id="8ff59-131">**GetMetrics**</span><span class="sxs-lookup"><span data-stu-id="8ff59-131">**GetMetrics**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [<span data-ttu-id="8ff59-132">**GetOverhangMetrics**</span><span class="sxs-lookup"><span data-stu-id="8ff59-132">**GetOverhangMetrics**</span></span>](idwriteinlineobject-getoverhangmetrics.md)
-   [<span data-ttu-id="8ff59-133">**GetBreakConditions**</span><span class="sxs-lookup"><span data-stu-id="8ff59-133">**GetBreakConditions**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a><span data-ttu-id="8ff59-134">Passaggio 3: implementare la classe di oggetti inline.</span><span class="sxs-lookup"><span data-stu-id="8ff59-134">Step 3: Implement the Inline Object Class.</span></span>

<span data-ttu-id="8ff59-135">Creare un nuovo file C++, denominato InlineImage. cpp, per l'implementazione della classe.</span><span class="sxs-lookup"><span data-stu-id="8ff59-135">Create a new C++ file, named InlineImage.cpp, for the class implementation.</span></span> <span data-ttu-id="8ff59-136">Oltre al metodo LoadBitmapFromFile e ai metodi ereditati dall'interfaccia IUnknown, la classe InlineImage è costituita dai metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8ff59-136">In addition to the LoadBitmapFromFile method and the methods inherited from the IUnknown interface, the InlineImage class is made up of the following methods.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="8ff59-137">Costruttore.</span><span class="sxs-lookup"><span data-stu-id="8ff59-137">The Constructor.</span></span>


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



<span data-ttu-id="8ff59-138">Il primo argomento del costruttore è il ID2D1RenderTarget in cui verrà eseguito il rendering dell'immagine inline.</span><span class="sxs-lookup"><span data-stu-id="8ff59-138">The first argument of the constructor is the ID2D1RenderTarget that the inline image will be rendered to.</span></span> <span data-ttu-id="8ff59-139">Questa operazione viene archiviata per essere usata in un secondo momento durante il disegno.</span><span class="sxs-lookup"><span data-stu-id="8ff59-139">This is stored for use later when drawing.</span></span>

<span data-ttu-id="8ff59-140">La destinazione di rendering, IWICImagingFactory, e l'URI del nome file vengono tutti passati al metodo LoadBitmapFromFile che carica la bitmap e archivia le dimensioni bitmap (larghezza e altezza) nella \_ variabile membro Rect.</span><span class="sxs-lookup"><span data-stu-id="8ff59-140">The render target, IWICImagingFactory, and the filename uri are all passed to the LoadBitmapFromFile method that loads the bitmap and stores the bitmap size (width and height) in the rect\_ member variable.</span></span>

### <a name="the-draw-method"></a><span data-ttu-id="8ff59-141">Metodo di estrazione.</span><span class="sxs-lookup"><span data-stu-id="8ff59-141">The Draw Method.</span></span>

<span data-ttu-id="8ff59-142">Il metodo di [**disegno**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) è un callback chiamato dall'oggetto [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) quando è necessario disegnare l'oggetto inline.</span><span class="sxs-lookup"><span data-stu-id="8ff59-142">The [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) method is a callback that is called by the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) object when the inline object needs to be drawn.</span></span> <span data-ttu-id="8ff59-143">Il layout del testo non chiama direttamente questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8ff59-143">The text layout does not call this method directly.</span></span>


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



<span data-ttu-id="8ff59-144">In questo caso, la creazione della bitmap viene eseguita usando il metodo [**ID2D1RenderTarget::D rawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) ; Tuttavia, è possibile usare qualsiasi metodo per il disegno.</span><span class="sxs-lookup"><span data-stu-id="8ff59-144">In this case, drawing the bitmap is done by using the [**ID2D1RenderTarget::DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) method; however, any method for drawing can be used.</span></span>

### <a name="the-getmetrics-method"></a><span data-ttu-id="8ff59-145">Metodo GetMetrics.</span><span class="sxs-lookup"><span data-stu-id="8ff59-145">The GetMetrics Method.</span></span>


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



<span data-ttu-id="8ff59-146">Per il metodo [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) , archiviare la larghezza, l'altezza e la linea di base in una struttura di [**\_ \_ \_ metrica dell'oggetto inline DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) .</span><span class="sxs-lookup"><span data-stu-id="8ff59-146">For the [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) method, store the width, height and baseline in an [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) structure.</span></span> <span data-ttu-id="8ff59-147">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiama questa funzione di callback per ottenere la misura dell'oggetto inline.</span><span class="sxs-lookup"><span data-stu-id="8ff59-147">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the measurement of the inline object.</span></span>

### <a name="the-getoverhangmetrics-method"></a><span data-ttu-id="8ff59-148">Metodo GetOverhangMetrics.</span><span class="sxs-lookup"><span data-stu-id="8ff59-148">The GetOverhangMetrics Method.</span></span>


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



<span data-ttu-id="8ff59-149">In questo caso, non è necessario alcun sbalzo, quindi il metodo [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) restituisce tutti gli zeri.</span><span class="sxs-lookup"><span data-stu-id="8ff59-149">In this case, no overhang is necessary, so the [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) method returns all zeros.</span></span>

### <a name="the-getbreakconditions-method"></a><span data-ttu-id="8ff59-150">Metodo GetBreakConditions.</span><span class="sxs-lookup"><span data-stu-id="8ff59-150">The GetBreakConditions Method.</span></span>


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



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a><span data-ttu-id="8ff59-151">Passaggio 4: creare un'istanza della classe InlineImage e aggiungerla al layout di testo.</span><span class="sxs-lookup"><span data-stu-id="8ff59-151">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>

<span data-ttu-id="8ff59-152">Infine, nel metodo CreateDeviceDependentResources, creare un'istanza della classe InlineImage e aggiungerla al layout di testo.</span><span class="sxs-lookup"><span data-stu-id="8ff59-152">Finally, in the CreateDeviceDependentResources method, create an instance of the InlineImage class and add it to the text layout.</span></span> <span data-ttu-id="8ff59-153">Poiché include un riferimento a [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), che è una risorsa dipendente dal dispositivo e il [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) viene creato usando la destinazione di rendering, il InlineImage è anche dipendente dal dispositivo e deve essere ricreato se la destinazione di rendering viene ricreata.</span><span class="sxs-lookup"><span data-stu-id="8ff59-153">Because it holds a reference to the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), which is a device dependent resource, and the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is created by using the render target, the InlineImage is also device dependent and must be recreated if the render target is recreated.</span></span>


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



<span data-ttu-id="8ff59-154">Il metodo [**IDWriteTextLayout:: SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) accetta una struttura di intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="8ff59-154">The [**IDWriteTextLayout::SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) method takes a text range structure.</span></span> <span data-ttu-id="8ff59-155">L'oggetto si applica all'intervallo specificato e qualsiasi testo nell'intervallo verrà eliminato.</span><span class="sxs-lookup"><span data-stu-id="8ff59-155">The object applies to the range specified here, and any text in the range will be suppressed.</span></span> <span data-ttu-id="8ff59-156">Se la lunghezza dell'intervallo di testo è 0, l'oggetto non verrà disegnato.</span><span class="sxs-lookup"><span data-stu-id="8ff59-156">If the length of the text range is 0, the object will not be drawn.</span></span>

<span data-ttu-id="8ff59-157">In questo esempio è presente un asterisco ( \* ) come segnaposto nella posizione in cui verrà visualizzata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="8ff59-157">In this example, there is an asterisk (\*) as a place holder in the position where the image will be displayed.</span></span>


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



<span data-ttu-id="8ff59-158">Poiché la classe InlineImage dipende da [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), è necessario rilasciarla quando si rilascia la destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="8ff59-158">Since the InlineImage class is dependent on the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), you must release it when you release the render target.</span></span>


```C++
SafeRelease(&pInlineImage_);
```



 

 