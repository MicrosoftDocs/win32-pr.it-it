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
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a><span data-ttu-id="980b9-103">Come aggiungere effetti di disegno client a un layout di testo</span><span class="sxs-lookup"><span data-stu-id="980b9-103">How to Add Client Drawing Effects to a Text Layout</span></span>

<span data-ttu-id="980b9-104">Fornisce una breve esercitazione sull'aggiunta di effetti di disegno dei client a un'applicazione [DirectWrite](direct-write-portal.md) che Visualizza il testo usando l'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e un renderer di testo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="980b9-104">Provides a short tutorial on adding client drawing effects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface and a custom text renderer.</span></span>

<span data-ttu-id="980b9-105">Il prodotto finale di questa esercitazione è un'applicazione che Visualizza il testo con intervalli di testo con un effetto di disegno colore diverso per ogni, come illustrato nello screenshot seguente.</span><span class="sxs-lookup"><span data-stu-id="980b9-105">The end product of this tutorial is an application that displays text that has ranges of text with a different color drawing effect on each, as shown in the following screen shot.</span></span>

![Screenshot di "esempio di effetto di disegno client!"](images/drawingeffects.png)

> [!Note]  
> <span data-ttu-id="980b9-108">Questa esercitazione è destinata a essere un esempio semplificato della creazione di effetti di disegno client personalizzati, non di un esempio di un metodo semplice per il disegno del testo dei colori.</span><span class="sxs-lookup"><span data-stu-id="980b9-108">This tutorial is meant to be a simplified example of how to create custom client drawing effects, not an example of a simple method for drawing color text.</span></span> <span data-ttu-id="980b9-109">Per ulteriori informazioni, vedere la pagina di riferimento [**IDWriteTextLayout:: SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) .</span><span class="sxs-lookup"><span data-stu-id="980b9-109">See the [**IDWriteTextLayout::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) reference page for more information.</span></span>

 

<span data-ttu-id="980b9-110">Questa esercitazione contiene le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="980b9-110">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="980b9-111">Passaggio 1: creare un layout di testo</span><span class="sxs-lookup"><span data-stu-id="980b9-111">Step 1: Create a Text Layout</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="980b9-112">Passaggio 2: implementare una classe di effetto di disegno personalizzata</span><span class="sxs-lookup"><span data-stu-id="980b9-112">Step 2: Implement a Custom Drawing Effect Class</span></span>](#step-2-implement-a-custom-drawing-effect-class)
-   [<span data-ttu-id="980b9-113">Passaggio 3: implementare una classe renderer di testo personalizzato</span><span class="sxs-lookup"><span data-stu-id="980b9-113">Step 3: Implement a Custom Text Renderer Class</span></span>](#step-3-implement-a-custom-text-renderer-class)
    -   [<span data-ttu-id="980b9-114">Costruttore</span><span class="sxs-lookup"><span data-stu-id="980b9-114">The Constructor</span></span>](#the-constructor)
    -   [<span data-ttu-id="980b9-115">Metodo DrawGlyphRun</span><span class="sxs-lookup"><span data-stu-id="980b9-115">The DrawGlyphRun Method</span></span>](#the-drawglyphrun-method)
    -   [<span data-ttu-id="980b9-116">Distruttore</span><span class="sxs-lookup"><span data-stu-id="980b9-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="980b9-117">Passaggio 4: creare il renderer di testo</span><span class="sxs-lookup"><span data-stu-id="980b9-117">Step 4: Create the Text Renderer</span></span>](#step-4-create-the-text-renderer)
-   [<span data-ttu-id="980b9-118">Passaggio 5: creare un'istanza degli oggetti effetto disegno colori</span><span class="sxs-lookup"><span data-stu-id="980b9-118">Step 5: Instantiate the Color Drawing Effect Objects</span></span>](#step-5-instantiate-the-color-drawing-effect-objects)
-   [<span data-ttu-id="980b9-119">Passaggio 6: impostare l'effetto di disegno per intervalli di testo specifici</span><span class="sxs-lookup"><span data-stu-id="980b9-119">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [<span data-ttu-id="980b9-120">Passaggio 7: creare il layout del testo usando il renderer personalizzato</span><span class="sxs-lookup"><span data-stu-id="980b9-120">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [<span data-ttu-id="980b9-121">Passaggio 8: eseguire la pulizia</span><span class="sxs-lookup"><span data-stu-id="980b9-121">Step 8: Clean up</span></span>](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="980b9-122">Passaggio 1: creare un layout di testo</span><span class="sxs-lookup"><span data-stu-id="980b9-122">Step 1: Create a Text Layout</span></span>

<span data-ttu-id="980b9-123">Per iniziare, sarà necessaria un'applicazione con un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="980b9-123">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="980b9-124">Se è già presente un'applicazione che visualizza testo con un layout di testo o si usa il codice di esempio DrawingEffect personalizzato, andare al passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="980b9-124">If you already have an application that displays text with a text layout, or you are using the Custom DrawingEffect Example Code, skip to Step 2.</span></span>

<span data-ttu-id="980b9-125">Per aggiungere un layout di testo è necessario eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="980b9-125">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="980b9-126">Dichiarare un puntatore a un'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) come membro della classe.</span><span class="sxs-lookup"><span data-stu-id="980b9-126">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="980b9-127">Alla fine del metodo **CreateDeviceIndependentResources** , creare un oggetto interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chiamando il metodo [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="980b9-127">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
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

    

3.  <span data-ttu-id="980b9-128">Infine, ricordarsi di rilasciare il layout del testo nel distruttore.</span><span class="sxs-lookup"><span data-stu-id="980b9-128">Finally, remember to release the text layout in the destructor.</span></span>
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a><span data-ttu-id="980b9-129">Passaggio 2: implementare una classe di effetto di disegno personalizzata</span><span class="sxs-lookup"><span data-stu-id="980b9-129">Step 2: Implement a Custom Drawing Effect Class</span></span>

<span data-ttu-id="980b9-130">Oltre ai metodi ereditati da IUnknown, un'interfaccia dell'effetto di disegno client personalizzata non ha alcun requisito per quanto riguarda gli elementi che devono implementare.</span><span class="sxs-lookup"><span data-stu-id="980b9-130">Other than the methods inherited from IUnknown, a custom client drawing effect interface has no requirements as to what it must implement.</span></span> <span data-ttu-id="980b9-131">In questo caso, la classe **ColorDrawingEffect** include semplicemente un [**valore \_ \_ F di colore d2d1**](../direct2d/d2d1-color-f.md) e dichiara i metodi per ottenere e impostare questo valore, nonché un costruttore che può impostare inizialmente il colore.</span><span class="sxs-lookup"><span data-stu-id="980b9-131">In this case, the **ColorDrawingEffect** class simply holds a [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value and declares methods to get and set this value, as well as a constructor that can set the color initially.</span></span>

<span data-ttu-id="980b9-132">Dopo l'applicazione di un effetto di disegno client a un intervallo di testo in un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , l'effetto di disegno viene passato al metodo [**IDWriteTextRenderer::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) di qualsiasi operazione di glifo di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="980b9-132">After a client drawing effect is applied to a text range in a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, the drawing effect is passed to the [**IDWriteTextRenderer::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of any glyph run that is to be rendered.</span></span> <span data-ttu-id="980b9-133">I metodi dell'effetto di disegno sono quindi disponibili per il renderer di testo.</span><span class="sxs-lookup"><span data-stu-id="980b9-133">The methods of the drawing effect are then available to the text renderer.</span></span>

<span data-ttu-id="980b9-134">Un effetto di disegno del client può essere complesso quanto si vuole, portando più informazioni rispetto a questo esempio, oltre a fornire metodi per modificare i glifi, creare oggetti da usare per il disegno e così via.</span><span class="sxs-lookup"><span data-stu-id="980b9-134">A client drawing effect can be as complex as you want to make it, carrying more information than in this example, as well as providing methods to alter glyphs, create objects to be used for drawing, and so on.</span></span>

## <a name="step-3-implement-a-custom-text-renderer-class"></a><span data-ttu-id="980b9-135">Passaggio 3: implementare una classe renderer di testo personalizzato</span><span class="sxs-lookup"><span data-stu-id="980b9-135">Step 3: Implement a Custom Text Renderer Class</span></span>

<span data-ttu-id="980b9-136">Per sfruttare i vantaggi di un effetto di disegno client, è necessario implementare un renderer di testo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="980b9-136">In order to take advantage of a client drawing effect, you must implement a custom text renderer.</span></span> <span data-ttu-id="980b9-137">Questo renderer di testo applicherà l'effetto di disegno passato tramite il metodo [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) all'esecuzione del glifo che si sta disegnando.</span><span class="sxs-lookup"><span data-stu-id="980b9-137">This text renderer will apply the drawing effect passed to it by the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method to the glyph run being drawn.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="980b9-138">Costruttore</span><span class="sxs-lookup"><span data-stu-id="980b9-138">The Constructor</span></span>

<span data-ttu-id="980b9-139">Il costruttore per il renderer di testo personalizzato archivia l'oggetto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) che verrà utilizzato per creare oggetti [Direct2D](../direct2d/direct2d-portal.md) e la destinazione di rendering Direct2D su cui verrà disegnato il testo.</span><span class="sxs-lookup"><span data-stu-id="980b9-139">The constructor for the custom text renderer stores the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create [Direct2D](../direct2d/direct2d-portal.md) objects, and the Direct2D render target that the text will be drawn on to.</span></span>


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



### <a name="the-drawglyphrun-method"></a><span data-ttu-id="980b9-140">Metodo DrawGlyphRun</span><span class="sxs-lookup"><span data-stu-id="980b9-140">The DrawGlyphRun Method</span></span>

<span data-ttu-id="980b9-141">Un'esecuzione di glifo è un set di glifi che condividono lo stesso formato, incluso l'effetto di disegno del client.</span><span class="sxs-lookup"><span data-stu-id="980b9-141">A glyph run is a set of glyphs that share the same format, including the client drawing effect.</span></span> <span data-ttu-id="980b9-142">Il metodo [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) prende in considerazione il rendering del testo per un'esecuzione del glifo specificata.</span><span class="sxs-lookup"><span data-stu-id="980b9-142">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method takes care of the text rendering for a specified glyph run.</span></span>

<span data-ttu-id="980b9-143">Per prima cosa, creare un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e un [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)e quindi recuperare la struttura di esecuzione del glifo usando [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline).</span><span class="sxs-lookup"><span data-stu-id="980b9-143">First, create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink), and then retrieve the glyph run outline by using [**IDWriteFontFace::GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline).</span></span> <span data-ttu-id="980b9-144">Trasformare quindi l'origine della geometria usando il metodo [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory:: CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="980b9-144">Then transform the origin of the geometry by using the [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method, as shown in the following code.</span></span>


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



<span data-ttu-id="980b9-145">Dichiarare quindi un oggetto pennello a tinta unita [Direct2D](../direct2d/direct2d-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="980b9-145">Next, declare a [Direct2D](../direct2d/direct2d-portal.md) solid brush object.</span></span>


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



<span data-ttu-id="980b9-146">Se il parametro *clientDrawingEffect* non è null, eseguire una query sull'oggetto per l'interfaccia **ColorDrawingEffect** .</span><span class="sxs-lookup"><span data-stu-id="980b9-146">If the *clientDrawingEffect* parameter is not NULL, query the object for the **ColorDrawingEffect** interface.</span></span> <span data-ttu-id="980b9-147">Questa operazione funzionerà perché la classe verrà impostata come effetto di disegno del client sugli intervalli di testo dell'oggetto layout di testo.</span><span class="sxs-lookup"><span data-stu-id="980b9-147">This will work because you will set this class as the client drawing effect on text ranges of the text layout object.</span></span>

<span data-ttu-id="980b9-148">Una volta ottenuto un puntatore all'interfaccia **ColorDrawingEffect** , è possibile recuperare il valore di [**d2d1 \_ Color \_ F**](../direct2d/d2d1-color-f.md) che archivia usando il metodo **GetColor** .</span><span class="sxs-lookup"><span data-stu-id="980b9-148">Once you have a pointer to the **ColorDrawingEffect** interface, you can retrieve the [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value that it stores using the **GetColor** method.</span></span> <span data-ttu-id="980b9-149">Usare quindi il **\_ colore \_ F di d2d1** per creare un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) in tale colore.</span><span class="sxs-lookup"><span data-stu-id="980b9-149">Then, use the **D2D1\_COLOR\_F** to create a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) in that color.</span></span>

<span data-ttu-id="980b9-150">Se il parametro *clientDrawingEffect* è **null**, è sufficiente creare un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)nero.</span><span class="sxs-lookup"><span data-stu-id="980b9-150">If the *clientDrawingEffect* parameter is **NULL**, then just create a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


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



<span data-ttu-id="980b9-151">Infine, disegnare la geometria del contorno e riempirla usando il pennello a tinta unita appena creato.</span><span class="sxs-lookup"><span data-stu-id="980b9-151">Finally, draw the outline geometry and fill it using the solid color brush that you just created.</span></span>


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



### <a name="the-destructor"></a><span data-ttu-id="980b9-152">Distruttore</span><span class="sxs-lookup"><span data-stu-id="980b9-152">The Destructor</span></span>

<span data-ttu-id="980b9-153">Non dimenticare di rilasciare la factory [Direct2D](../direct2d/direct2d-portal.md) e la destinazione di rendering nel distruttore.</span><span class="sxs-lookup"><span data-stu-id="980b9-153">Don't forget to release the [Direct2D](../direct2d/direct2d-portal.md) factory and render target in the destructor.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a><span data-ttu-id="980b9-154">Passaggio 4: creare il renderer di testo</span><span class="sxs-lookup"><span data-stu-id="980b9-154">Step 4: Create the Text Renderer</span></span>

<span data-ttu-id="980b9-155">Nelle risorse **CreateDeviceDependent** creare l'oggetto renderer di testo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="980b9-155">In the **CreateDeviceDependent** resources, create the custom text renderer object.</span></span> <span data-ttu-id="980b9-156">È dipendente dal dispositivo perché usa **ID2D1RenderTarget**, che è a sua volta dipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="980b9-156">It is device dependent because it uses the **ID2D1RenderTarget**, which is itself device dependent.</span></span>


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a><span data-ttu-id="980b9-157">Passaggio 5: creare un'istanza degli oggetti effetto disegno colori</span><span class="sxs-lookup"><span data-stu-id="980b9-157">Step 5: Instantiate the Color Drawing Effect Objects</span></span>

<span data-ttu-id="980b9-158">Crea un'istanza degli oggetti **ColorDrawingEffect** in rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="980b9-158">Instantiate **ColorDrawingEffect** objects in red, green, and blue.</span></span>


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



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a><span data-ttu-id="980b9-159">Passaggio 6: impostare l'effetto di disegno per intervalli di testo specifici</span><span class="sxs-lookup"><span data-stu-id="980b9-159">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>

<span data-ttu-id="980b9-160">Impostare l'effetto di disegno per intervalli di testo specifici usando il metodo [**IDWriteTextLayou:: SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) e uno struct dell' [**\_ \_ intervallo di testo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) .</span><span class="sxs-lookup"><span data-stu-id="980b9-160">Set the drawing effect for specific ranges of text by using the [**IDWriteTextLayou::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) method and a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) struct.</span></span>


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



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a><span data-ttu-id="980b9-161">Passaggio 7: creare il layout del testo usando il renderer personalizzato</span><span class="sxs-lookup"><span data-stu-id="980b9-161">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>

<span data-ttu-id="980b9-162">È necessario chiamare il metodo [**IDWriteTextLayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) anziché i metodi [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) o [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) .</span><span class="sxs-lookup"><span data-stu-id="980b9-162">You must call the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method rather than the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) or [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) methods.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a><span data-ttu-id="980b9-163">Passaggio 8: eseguire la pulizia</span><span class="sxs-lookup"><span data-stu-id="980b9-163">Step 8: Clean up</span></span>

<span data-ttu-id="980b9-164">Nel distruttore DemoApp rilasciare il renderer di testo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="980b9-164">In the DemoApp destructor, release the custom text renderer.</span></span>


```C++
SafeRelease(&pTextRenderer_);
```



<span data-ttu-id="980b9-165">Successivamente, aggiungere il codice per rilasciare le classi dell'effetto di disegno del client.</span><span class="sxs-lookup"><span data-stu-id="980b9-165">After that, add code to release the client drawing effect classes.</span></span>


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 