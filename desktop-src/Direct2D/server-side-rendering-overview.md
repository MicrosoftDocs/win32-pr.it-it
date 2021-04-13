---
title: Uso di Direct2D per il rendering di Server-Side
description: Viene descritto l'utilizzo di Direct2D per il rendering lato server.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, rendering lato server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35c9df619ee43d11c90c171598c87b6e447dd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399146"
---
# <a name="using-direct2d-for-server-side-rendering"></a><span data-ttu-id="5be03-104">Uso di Direct2D per il rendering di Server-Side</span><span class="sxs-lookup"><span data-stu-id="5be03-104">Using Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="5be03-105">Direct2D è particolarmente adatto per applicazioni grafiche che richiedono il rendering lato server in Windows Server.</span><span class="sxs-lookup"><span data-stu-id="5be03-105">Direct2D is well-suited for graphics applications that require server-side rendering on Windows Server.</span></span> <span data-ttu-id="5be03-106">Questa panoramica descrive le nozioni di base sull'uso di Direct2D per il rendering lato server.</span><span class="sxs-lookup"><span data-stu-id="5be03-106">This overview describes the basics of using Direct2D for server-side rendering.</span></span> <span data-ttu-id="5be03-107">Contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5be03-107">It contains the following sections:</span></span>

-   [<span data-ttu-id="5be03-108">Requisiti per il rendering di Server-Side</span><span class="sxs-lookup"><span data-stu-id="5be03-108">Requirements for Server-Side Rendering</span></span>](#requirements-for-server-side-rendering)
-   [<span data-ttu-id="5be03-109">Opzioni per le API disponibili</span><span class="sxs-lookup"><span data-stu-id="5be03-109">Options for Available APIs</span></span>](#options-for-available-apis)
    -   [<span data-ttu-id="5be03-110">GDI</span><span class="sxs-lookup"><span data-stu-id="5be03-110">GDI</span></span>](#gdi)
    -   [<span data-ttu-id="5be03-111">GDI+</span><span class="sxs-lookup"><span data-stu-id="5be03-111">GDI+</span></span>](#gdi)
    -   [<span data-ttu-id="5be03-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="5be03-112">Direct2D</span></span>](#using-direct2d-for-server-side-rendering)
-   [<span data-ttu-id="5be03-113">Come usare Direct2D per il rendering di Server-Side</span><span class="sxs-lookup"><span data-stu-id="5be03-113">How to Use Direct2D for Server-Side Rendering</span></span>](#how-to-use-direct2d-for-server-side-rendering)
    -   [<span data-ttu-id="5be03-114">Rendering del software</span><span class="sxs-lookup"><span data-stu-id="5be03-114">Software Rendering</span></span>](#software-rendering)
    -   [<span data-ttu-id="5be03-115">Multithreading</span><span class="sxs-lookup"><span data-stu-id="5be03-115">Multithreading</span></span>](#multithreading)
    -   [<span data-ttu-id="5be03-116">Generazione di un file bitmap</span><span class="sxs-lookup"><span data-stu-id="5be03-116">Generating a Bitmap File</span></span>](#generating-a-bitmap-file)
-   [<span data-ttu-id="5be03-117">Conclusione</span><span class="sxs-lookup"><span data-stu-id="5be03-117">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="5be03-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5be03-118">Related topics</span></span>](#related-topics)

## <a name="requirements-for-server-side-rendering"></a><span data-ttu-id="5be03-119">Requisiti per il rendering di Server-Side</span><span class="sxs-lookup"><span data-stu-id="5be03-119">Requirements for Server-Side Rendering</span></span>

<span data-ttu-id="5be03-120">Di seguito è riportato uno scenario tipico per un server del grafico: il rendering di grafici e grafici viene eseguito in un server e recapitato come bitmap in risposta alle richieste Web.</span><span class="sxs-lookup"><span data-stu-id="5be03-120">The following is a typical scenario for a chart server: charts and graphics are rendered on a server and delivered as bitmaps in response to Web requests.</span></span> <span data-ttu-id="5be03-121">Il server potrebbe essere dotato di una scheda grafica di fascia bassa o nessuna scheda grafica.</span><span class="sxs-lookup"><span data-stu-id="5be03-121">The server might be equipped with a low-end graphics card or no graphics card at all.</span></span>

<span data-ttu-id="5be03-122">Questo scenario rivela tre requisiti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5be03-122">This scenario reveals three application requirements.</span></span> <span data-ttu-id="5be03-123">In primo luogo, l'applicazione deve gestire più richieste simultanee in modo efficiente, soprattutto nei server multicore.</span><span class="sxs-lookup"><span data-stu-id="5be03-123">First, the application must handle multiple concurrent requests efficiently, especially on multicore servers.</span></span> <span data-ttu-id="5be03-124">In secondo luogo, l'applicazione deve utilizzare il rendering del software quando viene eseguito su server con una scheda grafica di fascia bassa o senza scheda grafica.</span><span class="sxs-lookup"><span data-stu-id="5be03-124">Second, the application must use software rendering when running on servers with a low-end graphics card or no graphics card.</span></span> <span data-ttu-id="5be03-125">Infine, l'applicazione deve essere eseguita come servizio nella sessione 0 in modo che non richieda l'accesso di un utente.</span><span class="sxs-lookup"><span data-stu-id="5be03-125">Finally, the application must run as a service in Session 0 so that it does not require a user to be logged in.</span></span> <span data-ttu-id="5be03-126">Per ulteriori informazioni sulla sessione 0, vedere [Impact of Session 0 isolation on Services and Drivers in Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).</span><span class="sxs-lookup"><span data-stu-id="5be03-126">For more information about Session 0, see [Impact of Session 0 Isolation on Services and Drivers in Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).</span></span>

## <a name="options-for-available-apis"></a><span data-ttu-id="5be03-127">Opzioni per le API disponibili</span><span class="sxs-lookup"><span data-stu-id="5be03-127">Options for Available APIs</span></span>

<span data-ttu-id="5be03-128">Sono disponibili tre opzioni per il rendering lato server: GDI, GDI+ e Direct2D.</span><span class="sxs-lookup"><span data-stu-id="5be03-128">There are three options for server-side rendering: GDI, GDI+ and Direct2D.</span></span> <span data-ttu-id="5be03-129">Come GDI e GDI+, Direct2D è un'API di rendering 2D nativa che offre alle applicazioni un maggiore controllo sull'uso dei dispositivi grafici.</span><span class="sxs-lookup"><span data-stu-id="5be03-129">Like GDI and GDI+, Direct2D is a native 2D rendering API that gives applications more control over the use of graphics devices.</span></span> <span data-ttu-id="5be03-130">Inoltre, Direct2D supporta in modo univoco una factory a thread singolo e con multithreading.</span><span class="sxs-lookup"><span data-stu-id="5be03-130">In addition, Direct2D uniquely supports a single-threaded and a multithreaded factory.</span></span> <span data-ttu-id="5be03-131">Le sezioni seguenti confrontano ogni API in termini di qualità del disegno e rendering sul lato server multithreading.</span><span class="sxs-lookup"><span data-stu-id="5be03-131">The following sections compare each API in terms of drawing qualities and multithreaded server-side rendering.</span></span>

### <a name="gdi"></a><span data-ttu-id="5be03-132">GDI</span><span class="sxs-lookup"><span data-stu-id="5be03-132">GDI</span></span>

<span data-ttu-id="5be03-133">A differenza di Direct2D e GDI+, GDI non supporta le funzionalità di disegno di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="5be03-133">Unlike Direct2D and GDI+, GDI does not support high-quality drawing features.</span></span> <span data-ttu-id="5be03-134">Ad esempio, GDI non supporta l'anti-aliasing per la creazione di linee smussate e ha solo un supporto limitato per la trasparenza.</span><span class="sxs-lookup"><span data-stu-id="5be03-134">For instance, GDI does not support antialiasing for creating smooth lines and has only limited support for transparency.</span></span> <span data-ttu-id="5be03-135">In base ai risultati dei test delle prestazioni della grafica in Windows 7 e Windows Server 2008 R2, Direct2D viene ridimensionato in modo più efficiente rispetto a GDI, nonostante la riprogettazione dei blocchi in GDI.</span><span class="sxs-lookup"><span data-stu-id="5be03-135">Based on the graphics performance test results on Windows 7 and Windows Server 2008 R2, Direct2D scales more efficiently than GDI, despite the redesign of locks in GDI.</span></span> <span data-ttu-id="5be03-136">Per ulteriori informazioni su questi risultati dei test, vedere la pagina relativa alla [progettazione delle prestazioni grafiche di Windows 7](/archive/blogs/e7/engineering-windows-7-graphics-performance).</span><span class="sxs-lookup"><span data-stu-id="5be03-136">For more information about these test results, see [Engineering Windows 7 Graphics Performance](/archive/blogs/e7/engineering-windows-7-graphics-performance).</span></span>

<span data-ttu-id="5be03-137">Inoltre, le applicazioni che utilizzano GDI sono limitate a 10240 handle GDI per processo e 65536 handle GDI per sessione.</span><span class="sxs-lookup"><span data-stu-id="5be03-137">In addition, applications using GDI are limited to 10240 GDI handles per process and 65536 GDI handles per session.</span></span> <span data-ttu-id="5be03-138">Il motivo è che Windows internamente utilizza una parola a 16 bit per archiviare l'indice degli handle per ogni sessione.</span><span class="sxs-lookup"><span data-stu-id="5be03-138">The reason is that internally Windows uses a 16-bit WORD to store the index of handles for each session.</span></span>

### <a name="gdi"></a><span data-ttu-id="5be03-139">GDI+</span><span class="sxs-lookup"><span data-stu-id="5be03-139">GDI+</span></span>

<span data-ttu-id="5be03-140">Sebbene GDI+ supporti l'anti-aliasing e la fusione alfa per il disegno di alta qualità, il problema principale con GDI+ per gli scenari server è che non supporta l'esecuzione nella sessione 0.</span><span class="sxs-lookup"><span data-stu-id="5be03-140">While GDI+ supports antialiasing and alpha blending for high-quality drawing, the main problem with GDI+ for server-scenarios is that it does not support running in Session 0.</span></span> <span data-ttu-id="5be03-141">Poiché la sessione 0 supporta solo funzionalità non interattive, le funzioni che interagiscono direttamente o indirettamente con i dispositivi di visualizzazione riceveranno degli errori.</span><span class="sxs-lookup"><span data-stu-id="5be03-141">Since Session 0 only supports non-interactive functionality, functions that directly or indirectly interact with display devices will therefore receive errors.</span></span> <span data-ttu-id="5be03-142">Esempi specifici di funzioni includono non solo quelli che gestiscono i dispositivi di visualizzazione, ma anche quelli che gestiscono indirettamente i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5be03-142">Specific examples of functions include not only those dealing with display devices, but also those indirectly dealing with device drivers.</span></span>

<span data-ttu-id="5be03-143">Analogamente a GDI, GDI+ è limitato dal meccanismo di blocco.</span><span class="sxs-lookup"><span data-stu-id="5be03-143">Similar to GDI, GDI+ is limited by its locking mechanism.</span></span> <span data-ttu-id="5be03-144">I meccanismi di blocco in GDI+ sono gli stessi in Windows 7 e Windows Server 2008 R2 come nelle versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="5be03-144">The locking mechanisms in GDI+ are the same in Windows 7 and Windows Server 2008 R2 as in previous versions.</span></span>

### <a name="direct2d"></a><span data-ttu-id="5be03-145">Direct2D</span><span class="sxs-lookup"><span data-stu-id="5be03-145">Direct2D</span></span>

<span data-ttu-id="5be03-146">Direct2D è un'API grafica 2D, con accelerazione immediata e in modalità immediata, che offre prestazioni elevate e rendering di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="5be03-146">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering.</span></span> <span data-ttu-id="5be03-147">Offre una factory a thread singolo e una factory a thread multipli e il ridimensionamento lineare del rendering del software con granularità dei corsi.</span><span class="sxs-lookup"><span data-stu-id="5be03-147">It offers a single-threaded and a multithreaded factory and the linear scaling of course-grained software rendering.</span></span>

<span data-ttu-id="5be03-148">A tale scopo, Direct2D definisce un'interfaccia Factory radice.</span><span class="sxs-lookup"><span data-stu-id="5be03-148">To do this, Direct2D defines a root factory interface.</span></span> <span data-ttu-id="5be03-149">Come regola, un oggetto creato in una factory può essere usato solo con altri oggetti creati dalla stessa factory.</span><span class="sxs-lookup"><span data-stu-id="5be03-149">As a rule, an object created on a factory can only be used with other objects created from the same factory.</span></span> <span data-ttu-id="5be03-150">Il chiamante può richiedere una factory a thread singolo o con multithreading al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="5be03-150">The caller can request either a single-threaded or a multithreaded factory when it is created.</span></span> <span data-ttu-id="5be03-151">Se viene richiesta una factory a thread singolo, non viene eseguito alcun blocco dei thread.</span><span class="sxs-lookup"><span data-stu-id="5be03-151">If a single-threaded factory is requested, then no locking of threads is performed.</span></span> <span data-ttu-id="5be03-152">Se il chiamante richiede una factory multithreading, viene acquisito un blocco di thread a livello di Factory ogni volta che viene effettuata una chiamata a Direct2D.</span><span class="sxs-lookup"><span data-stu-id="5be03-152">If the caller requests a multithreaded factory, then, a factory-wide thread lock is acquired whenever a call is made into Direct2D.</span></span>

<span data-ttu-id="5be03-153">Inoltre, il blocco dei thread in Direct2D è più granulare rispetto a GDI e GDI+, in modo che l'incremento del numero di thread abbia un effetto minimo sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5be03-153">In addition, the locking of threads in Direct2D is more granular than in GDI and GDI+, so that the increase of the number of threads has minimal impact on the performance.</span></span>

## <a name="how-to-use-direct2d-for-server-side-rendering"></a><span data-ttu-id="5be03-154">Come usare Direct2D per il rendering di Server-Side</span><span class="sxs-lookup"><span data-stu-id="5be03-154">How to Use Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="5be03-155">Le sezioni seguenti descrivono come usare il rendering del software, come usare in modo ottimale una factory a thread singolo e con multithreading e come creare e salvare un disegno complesso in un file.</span><span class="sxs-lookup"><span data-stu-id="5be03-155">The following sections describe how to use software rendering, how to optimally use a single-threaded and a multithreaded factory, and how to draw and save a complex drawing to a file.</span></span>

### <a name="software-rendering"></a><span data-ttu-id="5be03-156">Rendering del software</span><span class="sxs-lookup"><span data-stu-id="5be03-156">Software Rendering</span></span>

<span data-ttu-id="5be03-157">Le applicazioni lato server usano il rendering del software creando la destinazione di rendering [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , con il tipo di destinazione di rendering impostato su d2d1 \_ Render \_ target type \_ \_ software o d2d1 \_ Render \_ target \_ Type \_ default.</span><span class="sxs-lookup"><span data-stu-id="5be03-157">Server-side applications use software rendering by creating [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target, with the render target type set to either D2D1\_RENDER\_TARGET\_TYPE\_SOFTWARE or D2D1\_RENDER\_TARGET\_TYPE\_DEFAULT.</span></span> <span data-ttu-id="5be03-158">Per ulteriori informazioni sulle destinazioni di rendering [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , vedere il metodo [**ID2D1Factory:: CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) . Per ulteriori informazioni sui tipi di destinazione di rendering, [**vedere \_ \_ \_ tipo di destinazione di rendering d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).</span><span class="sxs-lookup"><span data-stu-id="5be03-158">For more information about [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render targets, see the [**ID2D1Factory::CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) method; for more information about the render target types, see [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).</span></span>

### <a name="multithreading"></a><span data-ttu-id="5be03-159">Multithreading</span><span class="sxs-lookup"><span data-stu-id="5be03-159">Multithreading</span></span>

<span data-ttu-id="5be03-160">Sapere come creare e condividere le fabbriche e le destinazioni di rendering tra i thread può influire significativamente sulle prestazioni di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5be03-160">Knowing how to create and share factories and render targets across threads can significantly impact the performance of an application.</span></span> <span data-ttu-id="5be03-161">Nelle tre figure seguenti sono illustrati tre approcci diversi.</span><span class="sxs-lookup"><span data-stu-id="5be03-161">The following three figures show three varied approaches.</span></span> <span data-ttu-id="5be03-162">L'approccio ottimale è illustrato nella figura 3.</span><span class="sxs-lookup"><span data-stu-id="5be03-162">The optimal approach is shown in figure 3.</span></span>

![diagramma multithreading Direct2D con una singola destinazione di rendering.](images/server-side-rendering-1.png)

<span data-ttu-id="5be03-164">Nella figura 1, i diversi thread condividono la stessa factory e la stessa destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="5be03-164">In figure 1, different threads share the same factory and the same render target.</span></span> <span data-ttu-id="5be03-165">Questo approccio può causare risultati imprevedibili nei casi in cui più thread cambiano simultaneamente lo stato della destinazione di rendering condivisa, ad esempio impostando contemporaneamente la matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="5be03-165">This approach can lead to unpredictable results in cases when multiple threads simultaneously change the state of the shared render target, such as simultaneously setting the transformation matrix.</span></span> <span data-ttu-id="5be03-166">Poiché il blocco interno in Direct2D non sincronizza una risorsa condivisa, ad esempio le destinazioni di rendering, questo approccio può causare il fallimento della chiamata [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) nel thread 1, perché nel thread 2 la chiamata **BeginDraw** sta già usando la destinazione di rendering condivisa.</span><span class="sxs-lookup"><span data-stu-id="5be03-166">As the internal locking in Direct2D does not synchronize a shared resource such as render targets, this approach can cause the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) call to fail in thread 1, because in thread 2, the **BeginDraw** call is already using the shared render target.</span></span>

![diagramma multithreading Direct2D con più destinazioni di rendering.](images/server-side-rendering-2.png)

<span data-ttu-id="5be03-168">Per evitare i risultati imprevedibili rilevati nella figura 1, la figura 2 Mostra una factory multithreading con ogni thread con una propria destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="5be03-168">To avoid the unpredictable results encountered in figure 1, figure 2 shows a multithreaded factory with each thread having its own render target.</span></span> <span data-ttu-id="5be03-169">Questo approccio funziona, ma funziona in modo efficace come applicazione a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="5be03-169">This approach works but it effectively functions as a single-threaded application.</span></span> <span data-ttu-id="5be03-170">Il motivo è che il blocco a livello di Factory si applica solo al livello di operazione di disegno e tutte le chiamate di disegno nella stessa factory di conseguenza vengono serializzate.</span><span class="sxs-lookup"><span data-stu-id="5be03-170">The reason is that the factory-wide lock applies only to the drawing-operation level and all the drawing calls in the same factory consequently are serialized.</span></span> <span data-ttu-id="5be03-171">Di conseguenza, il thread 1 viene bloccato durante il tentativo di immissione di una chiamata di disegno, mentre il thread 2 sta per eseguire un'altra chiamata di disegno.</span><span class="sxs-lookup"><span data-stu-id="5be03-171">As a result, thread 1 becomes blocked when trying to enter a drawing call, while thread 2 is in the middle of executing another drawing call.</span></span>

![diagramma multithreading Direct2D con più Factory e più destinazioni di rendering.](images/server-side-rendering-3.png)

<span data-ttu-id="5be03-173">Nella figura 3 viene illustrato l'approccio ottimale, in cui vengono utilizzate una factory a thread singolo e una destinazione di rendering a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="5be03-173">Figure 3 shows the optimal approach, where a single-threaded factory and a single-threaded render target are used.</span></span> <span data-ttu-id="5be03-174">Poiché non viene eseguito alcun blocco quando si usa una factory a thread singolo, le operazioni di disegno in ogni thread possono essere eseguite simultaneamente per ottenere prestazioni ottimali.</span><span class="sxs-lookup"><span data-stu-id="5be03-174">Since no locking is performed when using a single-threaded factory, drawing operations in each thread can run concurrently to achieve optimal performance.</span></span>

### <a name="generating-a-bitmap-file"></a><span data-ttu-id="5be03-175">Generazione di un file bitmap</span><span class="sxs-lookup"><span data-stu-id="5be03-175">Generating a Bitmap File</span></span>

<span data-ttu-id="5be03-176">Per generare un file bitmap utilizzando il rendering del software, utilizzare una destinazione di rendering [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="5be03-176">To generate a bitmap file using software rendering, use an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="5be03-177">Usare un [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) per scrivere la bitmap in un file.</span><span class="sxs-lookup"><span data-stu-id="5be03-177">Use an [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) to write the bitmap to a file.</span></span> <span data-ttu-id="5be03-178">Usare [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) per codificare la bitmap in un formato di immagine specificato.</span><span class="sxs-lookup"><span data-stu-id="5be03-178">Use [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap into a specified image format.</span></span> <span data-ttu-id="5be03-179">Nell'esempio di codice seguente viene illustrato come creare e salvare l'immagine seguente in un file.</span><span class="sxs-lookup"><span data-stu-id="5be03-179">The following code example shows how to draw and save the following image to a file.</span></span>

![esempio di immagine di output.](images/saveasimagefile-sample.png)

<span data-ttu-id="5be03-181">Questo esempio di codice crea prima un [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) e una destinazione di rendering [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="5be03-181">This code example first creates an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) and an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="5be03-182">Viene quindi eseguito il rendering di un disegno con un testo, una geometria del percorso che rappresenta un vetro dell'ora e un vetro dell'ora trasformato in una bitmap WIC.</span><span class="sxs-lookup"><span data-stu-id="5be03-182">It then renders a drawing with some text, a path geometry representing an hour glass, and a transformed hour glass into a WIC bitmap.</span></span> <span data-ttu-id="5be03-183">USA quindi [IWICStream:: InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) per salvare la bitmap in un file.</span><span class="sxs-lookup"><span data-stu-id="5be03-183">It then uses [IWICStream::InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) to save the bitmap to a file.</span></span> <span data-ttu-id="5be03-184">Se l'applicazione deve salvare la bitmap in memoria, usare invece [IWICStream:: InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="5be03-184">If your application needs to save the bitmap in memory, use [IWICStream::InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) instead.</span></span> <span data-ttu-id="5be03-185">Infine, USA [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) per codificare la bitmap.</span><span class="sxs-lookup"><span data-stu-id="5be03-185">Finally, it uses [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap.</span></span>


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a><span data-ttu-id="5be03-186">Conclusione</span><span class="sxs-lookup"><span data-stu-id="5be03-186">Conclusion</span></span>

<span data-ttu-id="5be03-187">Come illustrato nell'esempio precedente, l'uso di Direct2D per il rendering lato server è semplice e diretto.</span><span class="sxs-lookup"><span data-stu-id="5be03-187">As seen from the above, using Direct2D for server-side rendering is simple and straightforward.</span></span> <span data-ttu-id="5be03-188">Fornisce inoltre un rendering di elevata qualità e altamente eseguibili che può essere eseguito in ambienti con privilegi limitati del server.</span><span class="sxs-lookup"><span data-stu-id="5be03-188">In addition, it provides high quality and highly parallelizable rendering that can run in low-privilege environments of the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5be03-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5be03-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5be03-190">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="5be03-190">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 