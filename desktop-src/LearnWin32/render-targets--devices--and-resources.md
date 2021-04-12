---
title: Destinazioni di rendering, dispositivi e risorse
description: Destinazioni di rendering, dispositivi e risorse
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeddd84e12c52e0fd0ae82dab8b5e8741a2e0891
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337199"
---
# <a name="render-targets-devices-and-resources"></a><span data-ttu-id="f1d5e-103">Destinazioni di rendering, dispositivi e risorse</span><span class="sxs-lookup"><span data-stu-id="f1d5e-103">Render Targets, Devices, and Resources</span></span>

<span data-ttu-id="f1d5e-104">Una *destinazione di rendering* è semplicemente la posizione in cui verrà disegnato il programma.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-104">A *render target* is simply the location where your program will draw.</span></span> <span data-ttu-id="f1d5e-105">In genere, la destinazione di rendering è una finestra (in particolare, l'area client della finestra).</span><span class="sxs-lookup"><span data-stu-id="f1d5e-105">Typically, the render target is a window (specifically, the client area of the window).</span></span> <span data-ttu-id="f1d5e-106">Potrebbe anche essere una bitmap in memoria che non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-106">It could also be a bitmap in memory that is not displayed.</span></span> <span data-ttu-id="f1d5e-107">Una destinazione di rendering è rappresentata dall'interfaccia [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="f1d5e-107">A render target is represented by the [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span>

<span data-ttu-id="f1d5e-108">Un *dispositivo* è un'astrazione che rappresenta qualsiasi cosa disegna effettivamente i pixel.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-108">A *device* is an abstraction that represents whatever actually draws the pixels.</span></span> <span data-ttu-id="f1d5e-109">Un dispositivo hardware usa la GPU per ottenere prestazioni più veloci, mentre un dispositivo software usa la CPU.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-109">A hardware device uses the GPU for faster performance, whereas a software device uses the CPU.</span></span> <span data-ttu-id="f1d5e-110">L'applicazione non crea il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-110">The application does not create the device.</span></span> <span data-ttu-id="f1d5e-111">Al contrario, il dispositivo viene creato in modo implicito quando l'applicazione crea la destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-111">Instead, the device is created implicitly when the application creates the render target.</span></span> <span data-ttu-id="f1d5e-112">Ogni destinazione di rendering è associata a un particolare dispositivo, hardware o software.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-112">Each render target is associated with a particular device, either hardware or software.</span></span>

![diagramma che mostra la relazione tra una destinazione di rendering e un dispositivo.](images/graphics09.png)

<span data-ttu-id="f1d5e-114">Una *risorsa* è un oggetto utilizzato dal programma per il disegno.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-114">A *resource* is an object that the program uses for drawing.</span></span> <span data-ttu-id="f1d5e-115">Di seguito sono riportati alcuni esempi di risorse definite in Direct2D:</span><span class="sxs-lookup"><span data-stu-id="f1d5e-115">Here are some examples of resources that are defined in Direct2D:</span></span>

-   <span data-ttu-id="f1d5e-116">**Pennello**.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-116">**Brush**.</span></span> <span data-ttu-id="f1d5e-117">Controlla il modo in cui vengono disegnate le linee e le aree.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-117">Controls how lines and regions are painted.</span></span> <span data-ttu-id="f1d5e-118">I tipi di pennelli includono pennelli a tinta unita e pennelli sfumatura.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-118">Brush types include solid-color brushes and gradient brushes.</span></span>
-   <span data-ttu-id="f1d5e-119">**Stile tratto**.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-119">**Stroke style**.</span></span> <span data-ttu-id="f1d5e-120">Controlla l'aspetto di una riga, ad esempio tratteggiata o a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-120">Controls the appearance of a line—for example, dashed or solid.</span></span>
-   <span data-ttu-id="f1d5e-121">**Geometria**.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-121">**Geometry**.</span></span> <span data-ttu-id="f1d5e-122">Rappresenta una raccolta di linee e curve.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-122">Represents a collection of lines and curves.</span></span>
-   <span data-ttu-id="f1d5e-123">**Mesh**.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-123">**Mesh**.</span></span> <span data-ttu-id="f1d5e-124">Forma composta da triangoli.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-124">A shape formed out of triangles.</span></span> <span data-ttu-id="f1d5e-125">I dati mesh possono essere utilizzati direttamente dalla GPU, a differenza dei dati geometry, che devono essere convertiti prima del rendering.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-125">Mesh data can be consumed directly by the GPU, unlike geometry data, which must be converted before rendering.</span></span>

<span data-ttu-id="f1d5e-126">Anche le destinazioni di rendering sono considerate un tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-126">Render targets are also considered a type of resource.</span></span>

<span data-ttu-id="f1d5e-127">Alcune risorse traggono vantaggio dall'accelerazione hardware.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-127">Some resources benefit from hardware acceleration.</span></span> <span data-ttu-id="f1d5e-128">Una risorsa di questo tipo è sempre associata a un particolare dispositivo, ovvero hardware (GPU) o software (CPU).</span><span class="sxs-lookup"><span data-stu-id="f1d5e-128">A resource of this type is always associated with a particular device, either hardware (GPU) or software (CPU).</span></span> <span data-ttu-id="f1d5e-129">Questo tipo di risorsa viene definito *dipendente dal dispositivo*.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-129">This type of resource is called *device-dependent*.</span></span> <span data-ttu-id="f1d5e-130">I pennelli e le mesh sono esempi di risorse dipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-130">Brushes and meshes are examples of device-dependent resources.</span></span> <span data-ttu-id="f1d5e-131">Se il dispositivo diventa non disponibile, è necessario ricreare la risorsa per un nuovo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-131">If the device becomes unavailable, the resource must be re-created for a new device.</span></span>

<span data-ttu-id="f1d5e-132">Le altre risorse vengono mantenute nella memoria della CPU, indipendentemente dal dispositivo usato.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-132">Other resources are kept in CPU memory, regardless of what device is used.</span></span> <span data-ttu-id="f1d5e-133">Queste risorse sono *indipendenti dal dispositivo*, perché non sono associate a un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-133">These resources are *device-independent*, because they are not associated with a particular device.</span></span> <span data-ttu-id="f1d5e-134">Non è necessario ricreare risorse indipendenti dal dispositivo quando il dispositivo viene modificato.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-134">It is not necessary to re-create device-independent resources when the device changes.</span></span> <span data-ttu-id="f1d5e-135">Gli stili e le geometrie del tratto sono risorse indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-135">Stroke styles and geometries are device-independent resources.</span></span>

<span data-ttu-id="f1d5e-136">La documentazione MSDN relativa a ogni risorsa indica se la risorsa è dipendente dal dispositivo o indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-136">The MSDN documentation for each resource states whether the resource is device-dependent or device-independent.</span></span> <span data-ttu-id="f1d5e-137">Ogni tipo di risorsa è rappresentato da un'interfaccia che deriva da [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource).</span><span class="sxs-lookup"><span data-stu-id="f1d5e-137">Every resource type is represented by an interface that derives from [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource).</span></span> <span data-ttu-id="f1d5e-138">I pennelli, ad esempio, sono rappresentati dall'interfaccia [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) .</span><span class="sxs-lookup"><span data-stu-id="f1d5e-138">For example, brushes are represented by the [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) interface.</span></span>

## <a name="the-direct2d-factory-object"></a><span data-ttu-id="f1d5e-139">Oggetto factory Direct2D</span><span class="sxs-lookup"><span data-stu-id="f1d5e-139">The Direct2D Factory Object</span></span>

<span data-ttu-id="f1d5e-140">Il primo passaggio quando si utilizza Direct2D consiste nel creare un'istanza dell'oggetto factory Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-140">The first step when using Direct2D is to create an instance of the Direct2D factory object.</span></span> <span data-ttu-id="f1d5e-141">Nella programmazione di computer, una *Factory* è un oggetto che crea altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-141">In computer programming, a *factory* is an object that creates other objects.</span></span> <span data-ttu-id="f1d5e-142">La factory Direct2D crea i tipi di oggetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1d5e-142">The Direct2D factory creates the following types of objects:</span></span>

-   <span data-ttu-id="f1d5e-143">Destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-143">Render targets.</span></span>
-   <span data-ttu-id="f1d5e-144">Risorse indipendenti dal dispositivo, ad esempio stili di tratto e geometrie.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-144">Device-independent resources, such as stroke styles and geometries.</span></span>

<span data-ttu-id="f1d5e-145">Le risorse dipendenti dal dispositivo, ad esempio pennelli e bitmap, vengono create dall'oggetto di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-145">Device-dependent resources, such as brushes and bitmaps, are created by the render target object.</span></span>

![diagramma che mostra la factory Direct2D.](images/graphics10.png)

<span data-ttu-id="f1d5e-147">Per creare l'oggetto factory Direct2D, chiamare la funzione [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .</span><span class="sxs-lookup"><span data-stu-id="f1d5e-147">To create the Direct2D factory object, call the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



<span data-ttu-id="f1d5e-148">Il primo parametro è un flag che specifica le opzioni di creazione.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-148">The first parameter is a flag that specifies creation options.</span></span> <span data-ttu-id="f1d5e-149">Il flag a **\_ \_ \_ \_ thread singolo di tipo Factory d2d1** significa che non si chiamerà Direct2D da più thread.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-149">The **D2D1\_FACTORY\_TYPE\_SINGLE\_THREADED** flag means that you will not call Direct2D from multiple threads.</span></span> <span data-ttu-id="f1d5e-150">Per supportare le chiamate da più thread, specificare **d2d1 \_ Factory di \_ tipo \_ multithread \_**.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-150">To support calls from multiple threads, specify **D2D1\_FACTORY\_TYPE\_MULTI\_THREADED**.</span></span> <span data-ttu-id="f1d5e-151">Se il programma usa un solo thread per chiamare Direct2D, l'opzione a thread singolo è più efficiente.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-151">If your program uses a single thread to call into Direct2D, the single-threaded option is more efficient.</span></span>

<span data-ttu-id="f1d5e-152">Il secondo parametro della funzione [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) riceve un puntatore all'interfaccia [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) .</span><span class="sxs-lookup"><span data-stu-id="f1d5e-152">The second parameter to the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function receives a pointer to the [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) interface.</span></span>

<span data-ttu-id="f1d5e-153">È necessario creare l'oggetto factory Direct2D prima del primo messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="f1d5e-153">You should create the Direct2D factory object before the first [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="f1d5e-154">Il gestore di messaggi [**WM \_ create**](/windows/desktop/winmsg/wm-create) è una posizione ideale per creare la Factory:</span><span class="sxs-lookup"><span data-stu-id="f1d5e-154">The [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message handler is a good place to create the factory:</span></span>


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a><span data-ttu-id="f1d5e-155">Creazione di risorse Direct2D</span><span class="sxs-lookup"><span data-stu-id="f1d5e-155">Creating Direct2D Resources</span></span>

<span data-ttu-id="f1d5e-156">Il programma Circle usa le risorse dipendenti dal dispositivo seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1d5e-156">The Circle program uses the following device-dependent resources:</span></span>

-   <span data-ttu-id="f1d5e-157">Destinazione di rendering associata alla finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-157">A render target that is associated with the application window.</span></span>
-   <span data-ttu-id="f1d5e-158">Pennello a tinta unita per disegnare il cerchio.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-158">A solid-color brush to paint the circle.</span></span>

<span data-ttu-id="f1d5e-159">Ognuna di queste risorse è rappresentata da un'interfaccia COM:</span><span class="sxs-lookup"><span data-stu-id="f1d5e-159">Each of these resources is represented by a COM interface:</span></span>

-   <span data-ttu-id="f1d5e-160">L'interfaccia [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) rappresenta la destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-160">The [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) interface represents the render target.</span></span>
-   <span data-ttu-id="f1d5e-161">L'interfaccia [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) rappresenta il pennello.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-161">The [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interface represents the brush.</span></span>

<span data-ttu-id="f1d5e-162">Il programma Circle archivia i puntatori a queste interfacce come variabili membro della `MainWindow` classe:</span><span class="sxs-lookup"><span data-stu-id="f1d5e-162">The Circle program stores pointers to these interfaces as member variables of the `MainWindow` class:</span></span>


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



<span data-ttu-id="f1d5e-163">Il codice seguente crea queste due risorse.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-163">The following code creates these two resources.</span></span>


```C++
HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}
```



<span data-ttu-id="f1d5e-164">Per creare una destinazione di rendering per una finestra, chiamare il metodo [**ID2D1Factory:: CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) nella factory Direct2D.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-164">To create a render target for a window, call the [**ID2D1Factory::CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method on the Direct2D factory.</span></span>

-   <span data-ttu-id="f1d5e-165">Il primo parametro specifica le opzioni comuni a qualsiasi tipo di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-165">The first parameter specifies options that are common to any type of render target.</span></span> <span data-ttu-id="f1d5e-166">In questo caso, vengono passate le opzioni predefinite chiamando la funzione helper [**D2D1:: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).</span><span class="sxs-lookup"><span data-stu-id="f1d5e-166">Here, we pass in default options by calling the helper function [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).</span></span>
-   <span data-ttu-id="f1d5e-167">Il secondo parametro specifica l'handle per la finestra più le dimensioni della destinazione di rendering, in pixel.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-167">The second parameter specifies the handle to the window plus the size of the render target, in pixels.</span></span>
-   <span data-ttu-id="f1d5e-168">Il terzo parametro riceve un puntatore [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="f1d5e-168">The third parameter receives an [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) pointer.</span></span>

<span data-ttu-id="f1d5e-169">Per creare il pennello a tinta unita, chiamare il metodo [**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) sulla destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-169">To create the solid-color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method on the render target.</span></span> <span data-ttu-id="f1d5e-170">Il colore viene specificato come valore [**\_ \_ F del colore d2d1**](/windows/desktop/Direct2D/d2d1-color-f) .</span><span class="sxs-lookup"><span data-stu-id="f1d5e-170">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) value.</span></span> <span data-ttu-id="f1d5e-171">Per ulteriori informazioni sui colori in Direct2D, vedere [utilizzo del colore in Direct2D](using-color-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="f1d5e-171">For more information about colors in Direct2D, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>

<span data-ttu-id="f1d5e-172">Si noti inoltre che se la destinazione di rendering esiste già, il `CreateGraphicsResources` metodo **restituisce \_ OK** senza eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-172">Also, notice that if the render target already exists, the `CreateGraphicsResources` method returns **S\_OK** without doing anything.</span></span> <span data-ttu-id="f1d5e-173">Il motivo di questa progettazione diventerà chiaro nell'argomento successivo.</span><span class="sxs-lookup"><span data-stu-id="f1d5e-173">The reason for this design will become clear in the next topic.</span></span>

## <a name="next"></a><span data-ttu-id="f1d5e-174">Prossima</span><span class="sxs-lookup"><span data-stu-id="f1d5e-174">Next</span></span>

[<span data-ttu-id="f1d5e-175">Disegno con Direct2D</span><span class="sxs-lookup"><span data-stu-id="f1d5e-175">Drawing with Direct2D</span></span>](drawing-with-direct2d.md)

 

 