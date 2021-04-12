---
title: Disegno con Direct2D
description: Dopo aver creato le risorse grafiche, si è pronti per il progetto.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f8f3cf82d3ce6f485a7c54700c32c9eb65d054
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472899"
---
# <a name="drawing-with-direct2d"></a><span data-ttu-id="d47f4-103">Disegno con Direct2D</span><span class="sxs-lookup"><span data-stu-id="d47f4-103">Drawing with Direct2D</span></span>

<span data-ttu-id="d47f4-104">Dopo aver creato le risorse grafiche, si è pronti per il progetto.</span><span class="sxs-lookup"><span data-stu-id="d47f4-104">After you create your graphics resources, you are ready to draw.</span></span>

## <a name="drawing-an-ellipse"></a><span data-ttu-id="d47f4-105">Disegno di un'ellisse</span><span class="sxs-lookup"><span data-stu-id="d47f4-105">Drawing an Ellipse</span></span>

<span data-ttu-id="d47f4-106">Il programma [Circle](your-first-direct2d-program.md) esegue una logica di disegno molto semplice:</span><span class="sxs-lookup"><span data-stu-id="d47f4-106">The [Circle](your-first-direct2d-program.md) program performs very simple drawing logic:</span></span>

1.  <span data-ttu-id="d47f4-107">Riempire lo sfondo con un colore a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="d47f4-107">Fill the background with a solid color.</span></span>
2.  <span data-ttu-id="d47f4-108">Viene disegnato un cerchio pieno.</span><span class="sxs-lookup"><span data-stu-id="d47f4-108">Draw a filled circle.</span></span>

![screenshot del programma Circle.](images/graphics08.png)

<span data-ttu-id="d47f4-110">Poiché la destinazione di rendering è una finestra (in contrapposizione a una bitmap o ad altra superficie Offscreen), il disegno viene eseguito in risposta ai messaggi di disegno [**WM \_**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="d47f4-110">Because the render target is a window (as opposed to a bitmap or other offscreen surface), drawing is done in response to [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) messages.</span></span> <span data-ttu-id="d47f4-111">Il codice seguente illustra la procedura della finestra per il programma Circle.</span><span class="sxs-lookup"><span data-stu-id="d47f4-111">The following code shows the window procedure for the Circle program.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_PAINT:
            OnPaint();
            return 0;

         // Other messages not shown...
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```

<span data-ttu-id="d47f4-112">Ecco il codice che disegna il cerchio.</span><span class="sxs-lookup"><span data-stu-id="d47f4-112">Here is the code that draws the circle.</span></span>

```C++
void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="d47f4-113">L'interfaccia [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) viene utilizzata per tutte le operazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="d47f4-113">The [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface is used for all drawing operations.</span></span> <span data-ttu-id="d47f4-114">Il metodo del programma `OnPaint` esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d47f4-114">The program's `OnPaint` method does the following:</span></span>

1.  <span data-ttu-id="d47f4-115">Il metodo [**ID2D1RenderTarget:: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) segnala l'inizio del disegno.</span><span class="sxs-lookup"><span data-stu-id="d47f4-115">The [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method signals the start of drawing.</span></span>
2.  <span data-ttu-id="d47f4-116">Il metodo [**ID2D1RenderTarget:: Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) riempie l'intera destinazione di rendering con un colore a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="d47f4-116">The [**ID2D1RenderTarget::Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) method fills the entire render target with a solid color.</span></span> <span data-ttu-id="d47f4-117">Il colore viene specificato come una struttura [**d2d1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) .</span><span class="sxs-lookup"><span data-stu-id="d47f4-117">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) structure.</span></span> <span data-ttu-id="d47f4-118">È possibile usare la classe [**D2D1:: ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) per inizializzare la struttura.</span><span class="sxs-lookup"><span data-stu-id="d47f4-118">You can use the [**D2D1::ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) class to initialize the structure.</span></span> <span data-ttu-id="d47f4-119">Per ulteriori informazioni, vedere [utilizzo del colore in Direct2D](using-color-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="d47f4-119">For more information, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>
3.  <span data-ttu-id="d47f4-120">Il metodo [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) disegna un'ellisse piena, usando il pennello specificato per il riempimento.</span><span class="sxs-lookup"><span data-stu-id="d47f4-120">The [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws a filled ellipse, using the specified brush for the fill.</span></span> <span data-ttu-id="d47f4-121">Un'ellisse è specificata da un punto centrale e dai raggi x e y.</span><span class="sxs-lookup"><span data-stu-id="d47f4-121">An ellipse is specified by a center point and the x- and y-radii.</span></span> <span data-ttu-id="d47f4-122">Se i raggi x e y sono uguali, il risultato è un cerchio.</span><span class="sxs-lookup"><span data-stu-id="d47f4-122">If the x- and y-radii are the same, the result is a circle.</span></span>
4.  <span data-ttu-id="d47f4-123">Il metodo [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) segnala il completamento del disegno per questo frame.</span><span class="sxs-lookup"><span data-stu-id="d47f4-123">The [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method signals the completion of drawing for this frame.</span></span> <span data-ttu-id="d47f4-124">Tutte le operazioni di disegno devono essere inserite tra le chiamate a [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e **EndDraw**.</span><span class="sxs-lookup"><span data-stu-id="d47f4-124">All drawing operations must be placed between calls to [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw**.</span></span>

<span data-ttu-id="d47f4-125">I metodi [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)e [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) hanno tutti un tipo restituito **void** .</span><span class="sxs-lookup"><span data-stu-id="d47f4-125">The [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear), and [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) methods all have a **void** return type.</span></span> <span data-ttu-id="d47f4-126">Se si verifica un errore durante l'esecuzione di uno di questi metodi, l'errore viene segnalato tramite il valore restituito del metodo [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="d47f4-126">If an error occurs during the execution of any of these methods, the error is signaled through the return value of the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="d47f4-127">Il `CreateGraphicsResources` metodo viene illustrato nell'argomento [creazione di risorse Direct2D](render-targets--devices--and-resources.md).</span><span class="sxs-lookup"><span data-stu-id="d47f4-127">The `CreateGraphicsResources` method is shown in the topic [Creating Direct2D Resources](render-targets--devices--and-resources.md).</span></span> <span data-ttu-id="d47f4-128">Questo metodo crea la destinazione di rendering e il pennello a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="d47f4-128">This method creates the render target and the solid-color brush.</span></span>

<span data-ttu-id="d47f4-129">Il dispositivo potrebbe memorizzare nel buffer i comandi di disegno e rinviarne l'esecuzione fino a quando non viene chiamato [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="d47f4-129">The device might buffer the drawing commands and defer executing them until [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) is called.</span></span> <span data-ttu-id="d47f4-130">È possibile forzare il dispositivo a eseguire tutti i comandi di disegno in sospeso chiamando [**ID2D1RenderTarget:: Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span><span class="sxs-lookup"><span data-stu-id="d47f4-130">You can force the device to execute any pending drawing commands by calling [**ID2D1RenderTarget::Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span> <span data-ttu-id="d47f4-131">Lo scaricamento può tuttavia ridurre le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="d47f4-131">Flushing can reduce performance, however.</span></span>

## <a name="handling-device-loss"></a><span data-ttu-id="d47f4-132">Gestione della perdita di dispositivi</span><span class="sxs-lookup"><span data-stu-id="d47f4-132">Handling Device Loss</span></span>

<span data-ttu-id="d47f4-133">Mentre il programma è in esecuzione, il dispositivo grafico in uso potrebbe non essere più disponibile.</span><span class="sxs-lookup"><span data-stu-id="d47f4-133">While your program is running, the graphics device that you are using might become unavailable.</span></span> <span data-ttu-id="d47f4-134">Ad esempio, il dispositivo può andare perduto se viene modificata la risoluzione dello schermo o se l'utente rimuove la scheda di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d47f4-134">For example, the device can be lost if the display resolution changes, or if the user removes the display adapter.</span></span> <span data-ttu-id="d47f4-135">Se il dispositivo viene perso, anche la destinazione di rendering diventa non valida, insieme alle risorse dipendenti dal dispositivo associate al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d47f4-135">If the device is lost, the render target also becomes invalid, along with any device-dependent resources that were associated with the device.</span></span> <span data-ttu-id="d47f4-136">Direct2D segnala un dispositivo perso restituendo il codice di errore **D2DERR \_ ricrea \_ destinazione** dal metodo [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="d47f4-136">Direct2D signals a lost device by returning the error code **D2DERR\_RECREATE\_TARGET** from the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="d47f4-137">Se viene visualizzato questo codice di errore, è necessario ricreare la destinazione di rendering e tutte le risorse dipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d47f4-137">If you receive this error code, you must re-create the render target and all device-dependent resources.</span></span>

<span data-ttu-id="d47f4-138">Per eliminare una risorsa, è sufficiente rilasciare l'interfaccia per tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="d47f4-138">To discard a resource, simply release the interface for that resource.</span></span>


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



<span data-ttu-id="d47f4-139">La creazione di una risorsa può essere un'operazione costosa, quindi non ricreare le risorse per ogni messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="d47f4-139">Creating a resource can be an expensive operation, so do not recreate your resources for every [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="d47f4-140">Creare una risorsa una sola volta e memorizzare nella cache il puntatore alla risorsa fino a quando la risorsa non diventa non valida a causa della perdita del dispositivo o fino a quando la risorsa non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="d47f4-140">Create a resource once, and cache the resource pointer until the resource becomes invalid due to device loss, or until you no longer need that resource.</span></span>

## <a name="the-direct2d-render-loop"></a><span data-ttu-id="d47f4-141">Ciclo di rendering Direct2D</span><span class="sxs-lookup"><span data-stu-id="d47f4-141">The Direct2D Render Loop</span></span>

<span data-ttu-id="d47f4-142">Indipendentemente da quanto disegnato, il programma deve eseguire un ciclo simile a quello riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d47f4-142">Regardless of what you draw, your program should perform a loop similar to following.</span></span>

1.  <span data-ttu-id="d47f4-143">Creare risorse indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d47f4-143">Create device-independent resources.</span></span>
2.  <span data-ttu-id="d47f4-144">Esegue il rendering della scena.</span><span class="sxs-lookup"><span data-stu-id="d47f4-144">Render the scene.</span></span>
    1.  <span data-ttu-id="d47f4-145">Controllare se esiste una destinazione di rendering valida.</span><span class="sxs-lookup"><span data-stu-id="d47f4-145">Check if a valid render target exists.</span></span> <span data-ttu-id="d47f4-146">In caso contrario, creare la destinazione di rendering e le risorse dipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d47f4-146">If not, create the render target and the device-dependent resources.</span></span>
    2.  <span data-ttu-id="d47f4-147">Chiamare [**ID2D1RenderTarget:: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).</span><span class="sxs-lookup"><span data-stu-id="d47f4-147">Call [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).</span></span>
    3.  <span data-ttu-id="d47f4-148">Eseguire i comandi di disegno.</span><span class="sxs-lookup"><span data-stu-id="d47f4-148">Issue drawing commands.</span></span>
    4.  <span data-ttu-id="d47f4-149">Chiamare [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="d47f4-149">Call [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>
    5.  <span data-ttu-id="d47f4-150">Se [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) restituisce **la \_ \_ destinazione D2DERR ricreate**, eliminare la destinazione di rendering e le risorse dipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d47f4-150">If [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) returns **D2DERR\_RECREATE\_TARGET**, discard the render target and device-dependent resources.</span></span>
3.  <span data-ttu-id="d47f4-151">Ripetere il passaggio 2 ogni volta che è necessario aggiornare o ricreare la scena.</span><span class="sxs-lookup"><span data-stu-id="d47f4-151">Repeat step 2 whenever you need to update or redraw the scene.</span></span>

<span data-ttu-id="d47f4-152">Se la destinazione di rendering è una finestra, il passaggio 2 si verifica ogni volta che la finestra riceve un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="d47f4-152">If the render target is a window, step 2 occurs whenever the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="d47f4-153">Il ciclo riportato di seguito gestisce la perdita del dispositivo ignorando le risorse dipendenti dal dispositivo e creando di nuovo tali risorse all'inizio del ciclo successivo (passaggio 2a).</span><span class="sxs-lookup"><span data-stu-id="d47f4-153">The loop shown here handles device loss by discarding the device-dependent resources and re-creating them at the start of the next loop (step 2a).</span></span>

## <a name="next"></a><span data-ttu-id="d47f4-154">Prossima</span><span class="sxs-lookup"><span data-stu-id="d47f4-154">Next</span></span>

[<span data-ttu-id="d47f4-155">DPI e Device-Independent pixel</span><span class="sxs-lookup"><span data-stu-id="d47f4-155">DPI and Device-Independent Pixels</span></span>](dpi-and-device-independent-pixels.md)

 

 