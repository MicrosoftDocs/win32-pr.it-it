---
title: Capovolgi modello, rettangoli Dirty, aree a scorrimento
description: DXGI 1,2 supporta una nuova catena di scambio Flip-Model, rettangoli Dirty e aree a scorrimento. Vengono illustrati i vantaggi derivanti dall'utilizzo della nuova catena di scambio flip-model e dall'ottimizzazione della presentazione specificando rettangoli Dirty e aree a scorrimento.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3abbb784de82f5bf647a4b66503497edcd4f89
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "104568728"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a><span data-ttu-id="9cbc5-104">Capovolgi modello, rettangoli Dirty, aree a scorrimento</span><span class="sxs-lookup"><span data-stu-id="9cbc5-104">Flip model, dirty rectangles, scrolled areas</span></span>

<span data-ttu-id="9cbc5-105">DXGI 1,2 supporta una nuova catena di scambio Flip-Model, rettangoli Dirty e aree a scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-105">DXGI 1.2 supports a new flip-model swap chain, dirty rectangles, and scrolled areas.</span></span> <span data-ttu-id="9cbc5-106">Vengono illustrati i vantaggi derivanti dall'utilizzo della nuova catena di scambio flip-model e dall'ottimizzazione della presentazione specificando rettangoli Dirty e aree a scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-106">We explain the benefits of using the new flip-model swap chain and of optimizing presentation by specifying dirty rectangles and scrolled areas.</span></span>

## <a name="dxgi-flip-model-presentation"></a><span data-ttu-id="9cbc5-107">Presentazione del modello DXGI Flip</span><span class="sxs-lookup"><span data-stu-id="9cbc5-107">DXGI flip-model presentation</span></span>

<span data-ttu-id="9cbc5-108">DXGI 1,2 aggiunge il supporto per il modello Flip Presentation per le API Direct3D 10 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-108">DXGI 1.2 adds support for the flip presentation model for Direct3D 10 and later APIs.</span></span> <span data-ttu-id="9cbc5-109">In Windows 7, Direct3D 9EX ha adottato per la prima volta la [presentazione del modello Flip](../direct3darticles/direct3d-9ex-improvements.md) per evitare la copia inutilmente del buffer della catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-109">In Windows 7, Direct3D 9EX first adopted [flip-model presentation](../direct3darticles/direct3d-9ex-improvements.md) to avoid unnecessarily copying the swap-chain buffer.</span></span> <span data-ttu-id="9cbc5-110">Utilizzando Capovolgi modello, i buffer indietro vengono capovolti tra il runtime e Gestione finestre desktop (DWM), quindi DWM si compone sempre direttamente dal buffer nascosto anziché copiare il contenuto del buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-110">By using flip model, back buffers are flipped between the runtime and Desktop Window Manager (DWM), so DWM always composes directly from the back buffer instead of copying the back buffer content.</span></span>

<span data-ttu-id="9cbc5-111">Le API DXGI 1,2 includono un'interfaccia a catena di scambio DXGI modificata, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1).</span><span class="sxs-lookup"><span data-stu-id="9cbc5-111">DXGI 1.2 APIs include a revised DXGI swap-chain interface, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="9cbc5-112">È possibile usare più metodi di interfaccia [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) per creare l'oggetto **IDXGISwapChain1** appropriato da usare con un handle [**HWND**](../winprog/windows-data-types.md) , un oggetto [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) , [DirectComposition](../directcomp/directcomposition-portal.md)o il Framework [**Windows. UI. XAML**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="9cbc5-112">You can use multiple [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) interface methods to create the appropriate **IDXGISwapChain1** object to use with an [**HWND**](../winprog/windows-data-types.md) handle, a [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) object, [DirectComposition](../directcomp/directcomposition-portal.md), or the [**Windows.UI.Xaml**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) framework.</span></span>

<span data-ttu-id="9cbc5-113">È possibile selezionare il modello Flip Presentation specificando il valore di enumerazione [**\_ \_ \_ \_ sequenziale DXGI swap effect Flip**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) nel membro **SwapEffect** della struttura [**DXGI \_ \_ Chain swap \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) e impostando il membro **BufferCount** di **DXGI \_ swap \_ Chain \_ DESC1** su un minimo di 2.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-113">You select the flip presentation model by specifying the [**DXGI\_SWAP\_EFFECT\_FLIP\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) enumeration value in the **SwapEffect** member of the [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) structure and by setting the **BufferCount** member of **DXGI\_SWAP\_CHAIN\_DESC1** to a minimum of 2.</span></span> <span data-ttu-id="9cbc5-114">Per ulteriori informazioni sull'utilizzo del modello DXGI Flip, vedere [DXGI flip model](dxgi-flip-model.md).</span><span class="sxs-lookup"><span data-stu-id="9cbc5-114">For more info about how to use DXGI flip model, see [DXGI flip model](dxgi-flip-model.md).</span></span> <span data-ttu-id="9cbc5-115">Grazie alla presentazione più semplice del modello di presentazione e ad altre nuove funzionalità, è consigliabile usare il modello Flip Presentation per tutte le nuove app scritte con le API Direct3D 10 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-115">Because of the flip presentation model's smoother presentation and other new functionality, we recommend that you use flip presentation model for all new apps that you write with Direct3D 10 and later APIs.</span></span>

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a><span data-ttu-id="9cbc5-116">Uso di rettangoli Dirty e del rettangolo di scorrimento nella presentazione della catena di scambio</span><span class="sxs-lookup"><span data-stu-id="9cbc5-116">Using dirty rectangles and the scroll rectangle in swap chain presentation</span></span>

<span data-ttu-id="9cbc5-117">Utilizzando rettangoli Dirty e il rettangolo di scorrimento nella presentazione della catena di scambio, è possibile risparmiare sull'utilizzo della larghezza di banda della memoria e sull'utilizzo correlato della potenza del sistema, perché la quantità di dati pixel che il sistema operativo deve creare il successivo frame presentato è ridotta se non è necessario che il sistema operativo disegni l'intero frame.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-117">By using dirty rectangles and the scroll rectangle in swap chain presentation, you save on the usage of memory bandwidth and the related usage of system power because the amount of pixel data that the operating system needs to draw the next presented frame is reduced if the operating system doesn't need to draw the entire frame.</span></span> <span data-ttu-id="9cbc5-118">Per le app che vengono spesso visualizzate tramite Connessione Desktop remoto e altre tecnologie di accesso remoto, i risparmi sono particolarmente evidenti nella qualità di visualizzazione, in quanto tali tecnologie utilizzano rettangoli Dirty e metadati di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-118">For apps that are often displayed via Remote Desktop Connection and other remote-accessing technologies, the savings are particularly noticeable in the display quality because these technologies use dirty rectangles and scroll metadata.</span></span>

<span data-ttu-id="9cbc5-119">È possibile usare Scroll solo con le catene di scambio DXGI eseguite nel modello Flip Presentation.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-119">You can use scroll only with DXGI swap chains that run in flip presentation model.</span></span> <span data-ttu-id="9cbc5-120">È possibile usare rettangoli Dirty con le catene di scambio DXGI che vengono eseguite sia nel modello flip che nel modello BitBlt (impostato con l' [**\_ effetto di scambio DXGI \_ \_ sequenziale**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span><span class="sxs-lookup"><span data-stu-id="9cbc5-120">You can use dirty rectangles with DXGI swap chains that run in both flip model and bitblt model (set with [**DXGI\_SWAP\_EFFECT\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span></span>

<span data-ttu-id="9cbc5-121">In questo scenario viene illustrata la funzionalità di utilizzo di rettangoli e scorrimenti Dirty.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-121">In this scenario and illustration we show the functionality of using dirty rectangles and scroll.</span></span> <span data-ttu-id="9cbc5-122">Qui, un'app scorrevole contiene testo e animazione di video.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-122">Here, a scrollable app contains text and animating video.</span></span> <span data-ttu-id="9cbc5-123">L'app usa rettangoli Dirty per aggiornare semplicemente il video di animazione e la nuova riga per la finestra, anziché aggiornare l'intera finestra.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-123">The app uses dirty rectangles to just update the animating video and new line for the window, instead of updating the entire window.</span></span> <span data-ttu-id="9cbc5-124">Il rettangolo di scorrimento consente al sistema operativo di copiare e tradurre il contenuto precedentemente sottoposto a rendering sul nuovo frame e di eseguire il rendering solo della nuova riga sul nuovo frame.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-124">The scroll rectangle allows the operating system to copy and translate the previously rendered content on the new frame and to render only the new line on the new frame.</span></span>

<span data-ttu-id="9cbc5-125">L'app esegue la presentazione chiamando il metodo [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) .</span><span class="sxs-lookup"><span data-stu-id="9cbc5-125">The app performs presentation by calling the [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) method.</span></span> <span data-ttu-id="9cbc5-126">In questa chiamata, l'app passa un puntatore a una struttura di [**\_ \_ parametri presente DXGI**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) che include rettangoli Dirty e il numero di rettangoli Dirty, oppure il rettangolo di scorrimento e l'offset di scorrimento associato oppure i rettangoli Dirty e il rettangolo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-126">In this call, the app passes a pointer to a [**DXGI\_PRESENT\_PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) structure that includes dirty rectangles and the number of dirty rectangles, or the scroll rectangle and the associated scroll offset, or both dirty rectangles and the scroll rectangle.</span></span> <span data-ttu-id="9cbc5-127">L'app passa 2 rettangoli Dirty e il rettangolo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-127">Our app passes 2 dirty rectangles and the scroll rectangle.</span></span> <span data-ttu-id="9cbc5-128">Il rettangolo di scorrimento è l'area del fotogramma precedente che il sistema operativo deve copiare nel frame corrente prima di eseguire il rendering del frame corrente.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-128">The scroll rectangle is the area of the previous frame that the operating system needs to copy to the current frame before it renders the current frame.</span></span> <span data-ttu-id="9cbc5-129">L'app specifica il video di animazione e la nuova riga come rettangoli Dirty e il sistema operativo li esegue il rendering nel frame corrente.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-129">The app specifies the animating video and new line as dirty rectangles, and the operating system renders them on the current frame.</span></span>

![illustrazione dei rettangoli scroll e Dirty sovrapposti](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

<span data-ttu-id="9cbc5-131">Il rettangolo tratteggiato Mostra il rettangolo di scorrimento nel frame corrente.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-131">The dashed rectangle shows the scroll rectangle in the current frame.</span></span> <span data-ttu-id="9cbc5-132">Il rettangolo di scorrimento viene specificato dal membro **pScrollRect** di [**DXGI \_ \_ parametri presenti**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters).</span><span class="sxs-lookup"><span data-stu-id="9cbc5-132">The scroll rectangle is specified by the **pScrollRect** member of [**DXGI\_PRESENT\_PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters).</span></span> <span data-ttu-id="9cbc5-133">La freccia Mostra l'offset di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-133">The arrow shows the scroll offset.</span></span> <span data-ttu-id="9cbc5-134">L'offset di scorrimento viene specificato dal membro **pScrollOffset** di **DXGI \_ \_ parametri presenti**.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-134">The scroll offset is specified by the **pScrollOffset** member of **DXGI\_PRESENT\_PARAMETERS**.</span></span> <span data-ttu-id="9cbc5-135">I rettangoli riempiti mostrano i rettangoli Dirty che l'app ha aggiornato con nuovo contenuto.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-135">Filled rectangles show dirty rectangles that the app updated with new content.</span></span> <span data-ttu-id="9cbc5-136">I rettangoli riempiti sono specificati dai membri **DirtyRectsCount** e **pDirtyRects** di **DXGI \_ present \_ Parameters**.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-136">The filled rectangles are specified by the **DirtyRectsCount** and **pDirtyRects** members of **DXGI\_PRESENT\_PARAMETERS**.</span></span>

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a><span data-ttu-id="9cbc5-137">Esempio 2: catena di scambio Flip del buffer con rettangoli Dirty e rettangolo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="9cbc5-137">Sample 2-buffer flip-model swap chain with dirty rectangles and scroll rectangle</span></span>

<span data-ttu-id="9cbc5-138">L'illustrazione e la sequenza successive mostrano un esempio di un'operazione di presentazione del modello DXGI flip che usa rettangoli Dirty e un rettangolo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-138">The next illustration and sequence shows an example of a DXGI flip-model presentation operation that uses dirty rectangles and a scroll rectangle.</span></span> <span data-ttu-id="9cbc5-139">In questo esempio viene usato il numero minimo di buffer per la presentazione del modello Flip, ovvero un numero di buffer di due, un buffer anteriore che contiene il contenuto di visualizzazione dell'app e un buffer nascosto che contiene il frame corrente di cui l'app vuole eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-139">In this example we use the minimum number of buffers for flip-model presentation, which is a buffer count of two, one front buffer that contains the app display content and one back buffer that contains the current frame that the app wants to render.</span></span>

1.  <span data-ttu-id="9cbc5-140">Come illustrato nel buffer anteriore all'inizio del frame, l'app scorrevole Mostra inizialmente un frame con testo e animazione di video.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-140">As shown in the front buffer at the beginning of the frame, the scrollable app initially shows a frame with some text and animating video.</span></span>
2.  <span data-ttu-id="9cbc5-141">Per eseguire il rendering del frame successivo, l'app esegue il rendering sul buffer nascosto dei rettangoli Dirty che aggiornano il video di animazione e la nuova riga per la finestra.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-141">To render the next frame, the app renders onto the back buffer the dirty rectangles that update the animating video and the new line for the window.</span></span>
3.  <span data-ttu-id="9cbc5-142">Quando l'app chiama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), specifica i rettangoli Dirty e il rettangolo di scorrimento e l'offset.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-142">When the app calls [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), it specifies the dirty rectangles and the scroll rectangle and offset.</span></span> <span data-ttu-id="9cbc5-143">Il runtime copia successivamente il rettangolo di scorrimento dal fotogramma precedente meno i rettangoli Dirty aggiornati sul buffer nascosto corrente.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-143">The runtime next copies the scroll rectangle from the previous frame minus the updated dirty rectangles onto the current back buffer.</span></span>
4.  <span data-ttu-id="9cbc5-144">Il runtime scambia infine i buffer anteriore e posteriore.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-144">The runtime finally swaps the front and back buffers.</span></span>

![esempio di catena di scambio flip-model con rettangoli scroll e Dirty](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a><span data-ttu-id="9cbc5-146">Rilevamento di rettangoli Dirty e rettangoli di scorrimento tra più frame</span><span class="sxs-lookup"><span data-stu-id="9cbc5-146">Tracking dirty rectangles and scroll rectangles across multiple frames</span></span>

<span data-ttu-id="9cbc5-147">Quando si usano rettangoli Dirty nell'app, è necessario tenere traccia dei rettangoli Dirty per supportare il rendering incrementale.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-147">When you use dirty rectangles in your app, you must track the dirty rectangles to support incremental rendering.</span></span> <span data-ttu-id="9cbc5-148">Quando l'app chiama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) con rettangoli Dirty, è necessario assicurarsi che ogni pixel all'interno dei rettangoli Dirty sia aggiornato.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-148">When your app calls [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) with dirty rectangles, you must ensure that every pixel within the dirty rectangles is up to date.</span></span> <span data-ttu-id="9cbc5-149">Se non si esegue completamente il rendering dell'intera area del rettangolo modificato o se non si è in grado di individuare determinate aree sporche, è necessario copiare alcuni dati dal buffer nascosto precedente completamente coerente al buffer nascosto corrente, prima di iniziare il rendering.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-149">If you aren't completely re-rendering the whole area of the dirty rectangle or if you can’t know for certain the areas that are dirtied, you must copy some data from the previous fully coherent back buffer to the current, stale back buffer before you start rendering.</span></span>

<span data-ttu-id="9cbc5-150">Il runtime copia solo le differenze tra le aree aggiornate del frame precedente e le aree aggiornate del frame corrente nel buffer nascosto corrente.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-150">The runtime copies only the differences between updated areas of the previous frame and updated areas of the current frame onto the current back buffer.</span></span> <span data-ttu-id="9cbc5-151">Se queste aree si intersecano, il runtime copia solo la differenza tra di esse.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-151">If these areas intersect, the runtime copies only the difference between them.</span></span> <span data-ttu-id="9cbc5-152">Come si può notare nel diagramma e nella sequenza seguenti, è necessario copiare l'intersezione tra il rettangolo Dirty dal frame 1 e il rettangolo Dirty dal frame 2 al rettangolo modificato del frame 2.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-152">As you can see in the following diagram and sequence, you must copy the intersection between the dirty rectangle from frame 1 and the dirty rectangle from frame 2 into frame 2’s dirty rectangle.</span></span>

1.  <span data-ttu-id="9cbc5-153">Presentare un rettangolo modificato nel frame 1.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-153">Present dirty rectangle in frame 1.</span></span>
2.  <span data-ttu-id="9cbc5-154">Copia intersezione tra il rettangolo Dirty dal frame 1 e il rettangolo Dirty dal frame 2 al rettangolo modificato del frame 2.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-154">Copy intersection between the dirty rectangle from frame 1 and the dirty rectangle from frame 2 into frame 2’s dirty rectangle.</span></span>
3.  <span data-ttu-id="9cbc5-155">Presentare un rettangolo modificato nel frame 2.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-155">Present dirty rectangle in frame 2.</span></span>

![rilevamento dei rettangoli scroll e Dirty tra più frame](images/track-dirty-rects-scroll-rects.png)

<span data-ttu-id="9cbc5-157">Per generalizzare, per una catena di scambio con N buffer, l'area che il runtime copia dall'ultimo frame al frame corrente sul presente frame corrente è:</span><span class="sxs-lookup"><span data-stu-id="9cbc5-157">To generalize, for a swap chain with N buffers, the area that the runtime copies from the last frame to the current frame on the current frame’s present is:</span></span>

![equazione per calcolare l'area copiata dal runtime](images/runtime-copy-equation.png)

<span data-ttu-id="9cbc5-159">dove buffer indica l'indice del buffer in una catena di scambio, a partire dall'indice del buffer corrente a zero.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-159">where buffer indicates the buffer index in a swap chain, starting with current buffer index at zero.</span></span>

<span data-ttu-id="9cbc5-160">È possibile tenere traccia di tutte le intersezioni tra il frame precedente e i rettangoli Dirty del frame corrente mantenendo una copia dei rettangoli Dirty del fotogramma precedente oppure eseguendo nuovamente il rendering dei rettangoli Dirty del nuovo frame con il contenuto appropriato del frame precedente.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-160">You can keep track of any intersections between the previous frame and the current frame’s dirty rectangles by keeping a copy of the previous frame’s dirty rectangles or by re-rendering the new frame’s dirty rectangles with the appropriate content from the previous frame.</span></span>

<span data-ttu-id="9cbc5-161">Analogamente, nei casi in cui la catena di scambio dispone di più di 2 buffer indietro, è necessario assicurarsi che le aree sovrapposte tra i rettangoli Dirty del buffer corrente e i rettangoli Dirty di tutti i frame precedenti vengano copiati o nuovamente sottoposti a rendering.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-161">Similarly, in the cases where the swap chain has more than 2 back buffers, you must ensure that overlapping areas between the current buffer’s dirty rectangles and the dirty rectangles of all previous frame’s are copied or re-rendered.</span></span>

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a><span data-ttu-id="9cbc5-162">Rilevamento di una singola intersezione tra due rettangoli Dirty</span><span class="sxs-lookup"><span data-stu-id="9cbc5-162">Tracking a single intersection between 2 dirty rectangles</span></span>

<span data-ttu-id="9cbc5-163">Nel caso più semplice, quando si aggiorna un singolo rettangolo modificato per fotogramma, è possibile che i rettangoli Dirty tra due frame si intersecano.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-163">In the simplest case, when you update a single dirty rectangle per frame, the dirty rectangles across two frames might intersect.</span></span> <span data-ttu-id="9cbc5-164">Per determinare se il rettangolo modificato del frame precedente e il rettangolo modificato del frame corrente si sovrappongono, è necessario verificare se il rettangolo modificato del fotogramma precedente si interseca con il rettangolo modificato del frame corrente.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-164">To find out whether the dirty rectangle of the previous frame and the dirty rectangle of the current frame overlap, you need to verify whether the dirty rectangle of the previous frame intersects with the dirty rectangle of the current frame.</span></span> <span data-ttu-id="9cbc5-165">È possibile chiamare la funzione GDI [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) per determinare se due strutture [**Rect**](/previous-versions//dd162897(v=vs.85)) che rappresentano i due rettangoli Dirty si intersecano.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-165">You can call the GDI [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) function to determine whether two [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that represent the two dirty rectangles intersect.</span></span>

<span data-ttu-id="9cbc5-166">In questo frammento di codice, una chiamata a [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) restituisce l'intersezione di due rettangoli Dirty in un altro oggetto [**Rect**](/previous-versions//dd162897(v=vs.85)) denominato dirtyRectCopy.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-166">In this code snippet, a call to [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) returns the intersection of two dirty rectangles in another [**RECT**](/previous-versions//dd162897(v=vs.85)) called dirtyRectCopy.</span></span> <span data-ttu-id="9cbc5-167">Dopo che il frammento di codice ha determinato che i due rettangoli Dirty si intersecano, chiama il metodo [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) per copiare l'area di intersezione nel frame corrente.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-167">After the code snippet determines that the two dirty rectangles intersect, it calls the [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) method to copy the region of intersection into the current frame.</span></span>

```
RECT dirtyRectPrev, dirtyRectCurrent, dirtyRectCopy;
 
if (IntersectRect( &dirtyRectCopy, &dirtyRectPrev, &dirtyRectCurrent ))
{
       D3D11_BOX intersectBox;
       intersectBox.left    = dirtyRectCopy.left;
       intersectBox.top     = dirtyRectCopy.top;
       intersectBox.front   = 0;
       intersectBox.right   = dirtyRectCopy.right;
       intersectBox.bottom  = dirtyRectCopy.bottom;
       intersectBox.back    = 1;
 
       d3dContext->CopySubresourceRegion1(pBackbuffer,
                                    0,
                                    0,
                                    0,
                                    0,
                                    pPrevBackbuffer,
                                    0,
                                    &intersectBox,
                                    0
                                    );
}

// Render additional content to the current pBackbuffer and call Present1.
```

<span data-ttu-id="9cbc5-168">Se si usa questo frammento di codice nell'applicazione, l'app sarà pronta per chiamare [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) per aggiornare il frame corrente con il rettangolo modificato corrente.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-168">If you use this code snippet in your application, the app will then be ready to call [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) to update the current frame with the current dirty rectangle.</span></span>

### <a name="tracking-intersections-between-n-dirty-rectangles"></a><span data-ttu-id="9cbc5-169">Rilevamento di intersezioni tra N rettangoli Dirty</span><span class="sxs-lookup"><span data-stu-id="9cbc5-169">Tracking intersections between N dirty rectangles</span></span>

<span data-ttu-id="9cbc5-170">Se si specificano più rettangoli Dirty, che possono includere un rettangolo modificato per la riga di scorrimento appena rivelata, per fotogramma, è necessario verificare e tenere traccia di eventuali sovrapposizioni che potrebbero verificarsi tra tutti i rettangoli Dirty del frame precedente e tutti i rettangoli modificati del frame corrente.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-170">If you specify multiple dirty rectangles, which can include a dirty rectangle for the newly revealed scroll line, per frame, you need to verify and track any overlaps that might occur between all the dirty rectangles of the previous frame and all the dirty rectangles of the current frame.</span></span> <span data-ttu-id="9cbc5-171">Per calcolare le intersezioni tra i rettangoli Dirty del fotogramma precedente e i rettangoli Dirty del frame corrente, è possibile raggruppare i rettangoli Dirty in aree.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-171">To calculate the intersections between the dirty rectangles of the previous frame and the dirty rectangles of the current frame, you can group the dirty rectangles into regions.</span></span>

<span data-ttu-id="9cbc5-172">In questo frammento di codice viene chiamata la funzione GDI [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) per convertire ogni rettangolo modificato in un'area rettangolare, quindi viene chiamata la funzione GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) per combinare tutte le aree rettangolari Dirty in un gruppo.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-172">In this code snippet, we call the GDI [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) function to convert each dirty rectangle into a rectangular region and then we call the GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) function to combine all the dirty rectangular regions into a group.</span></span>

```
HRGN hDirtyRgnPrev, hDirtyRgnCurrent, hRectRgn; // Handles to regions 
// Save all the dirty rectangles from the previous frame.
 
RECT dirtyRect[N]; // N is the number of dirty rectangles in current frame, which includes newly scrolled area.
 
int iReturn;
SetRectRgn(hDirtyRgnCurrent, 
       dirtyRect[0].left, 
       dirtyRect[0].top, 
       dirtyRect[0].right, 
       dirtyRect[0].bottom 
       );

for (int i = 1; i<N; i++)
{
   SetRectRgn(hRectRgn, 
          dirtyRect[0].left, 
          dirtyRect[0].top, 
          dirtyRect[0].right, 
          dirtyRect[0].bottom 
          );

   iReturn = CombineRgn(hDirtyRgnCurrent,
                        hDirtyRgnCurrent,
                        hRectRgn,
                        RGN_OR
                        );
   // Handle the error that CombineRgn returns for iReturn.
}
```

<span data-ttu-id="9cbc5-173">È ora possibile usare la funzione GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) per determinare l'intersezione tra l'area dirty del frame precedente e l'area dirty del frame corrente.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-173">You can now use the GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) function to determine the intersection between the dirty region of the previous frame and the dirty region of the current frame.</span></span> <span data-ttu-id="9cbc5-174">Una volta ottenuta l'area di intersezione, chiamare la funzione GDI [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) per ottenere ogni singolo rettangolo dall'area intersecante, quindi chiamare il metodo [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) per copiare ogni rettangolo intersecante nel buffer nascosto corrente.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-174">After you obtain the intersecting region, call the GDI [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) function to obtain each individual rectangle from the intersecting region and then call the [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) method to copy each intersecting rectangle into the current back buffer.</span></span> <span data-ttu-id="9cbc5-175">Il frammento di codice successivo Mostra come usare queste funzioni GDI e Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-175">The next code snippet shows how to use these GDI and Direct3D functions.</span></span>

```
HRGN hIntersectRgn;
bool bRegionsIntersect;
iReturn = CombineRgn(hIntersectRgn, hDirtyRgnCurrent, hDirtyRgnPrev, RGN_AND);
if (iReturn == ERROR)
{
       // Handle error.
}
else if(iReturn == NULLREGION)
{
       bRegionsIntersect = false;
}
else
{
       bRegionsIntersect = true;
}
 
if (bRegionsIntersect)
{
       int rgnDataSize = GetRegionData(hIntersectRgn, 0, NULL);
       if (rgnDataSize)
       {
              char pMem[] = new char[size];
              RGNDATA* pRgnData = reinterpret_cast<RGNDATA*>(pMem);
              iReturn = GetRegionData(hIntersectRgn, rgnDataSize, pRgnData);
              // Handle iReturn failure.
 
              for (int rectcount = 0; rectcount < pRgnData->rdh.nCount; ++r)
              {
                     const RECT* pIntersectRect = reinterpret_cast<RECT*>(pRgnData->Buffer) +                                            
                                                  rectcount;                
                     D3D11_BOX intersectBox;
                     intersectBox.left    = pIntersectRect->left;
                     intersectBox.top     = pIntersectRect->top;
                     intersectBox.front   = 0;
                     intersectBox.right   = pIntersectRect->right;
                     intersectBox.bottom  = pIntersectRect->bottom;
                     intersectBox.back    = 1;
 
                     d3dContext->CopySubresourceRegion1(pBackbuffer,
                                                      0,
                                                      0,
                                                      0,
                                                      0,
                                                      pPrevBackbuffer,
                                                      0,
                                                      &intersectBox,
                                                      0
                                                      );
              }

              delete [] pMem;
       }
}
```

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a><span data-ttu-id="9cbc5-176">Catena di scambio del modello BitBlt con rettangoli Dirty</span><span class="sxs-lookup"><span data-stu-id="9cbc5-176">Bitblt model swap chain with dirty rectangles</span></span>

<span data-ttu-id="9cbc5-177">È possibile usare rettangoli Dirty con le catene di scambio DXGI eseguite nel modello BitBlt (impostate con l' [**\_ effetto di scambio DXGI \_ \_ sequenziale**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span><span class="sxs-lookup"><span data-stu-id="9cbc5-177">You can use dirty rectangles with DXGI swap chains that run in bitblt model (set with [**DXGI\_SWAP\_EFFECT\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span></span> <span data-ttu-id="9cbc5-178">Le catene di scambio del modello BitBlt che usano più di un buffer devono anche tenere traccia dei rettangoli sporchi sovrapposti tra i frame nello stesso modo descritto in [rilevamento di rettangoli Dirty e rettangoli di scorrimento tra più frame per le](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) catene di scambio del modello flip.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-178">Bitblt model swap chains that use more than one buffer must also track overlapping dirty rectangles across frames in the same way as described in [Tracking dirty rectangles and scroll rectangles across multiple frames](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) for flip model swap chains.</span></span> <span data-ttu-id="9cbc5-179">Le catene di scambio del modello BitBlt con un solo buffer non devono rilevare rettangoli sporchi sovrapposti perché l'intero buffer viene ridisegnato ogni frame.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-179">Bitblt model swap chains with just one buffer need not track overlapping dirty rectangles because the entire buffer is redrawn every frame.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cbc5-180">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9cbc5-180">Related topics</span></span>

[<span data-ttu-id="9cbc5-181">Miglioramenti di DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="9cbc5-181">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
