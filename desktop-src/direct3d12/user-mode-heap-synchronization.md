---
title: Sincronizzazione multimotore
description: Questo argomento illustra la sincronizzazione dell'accesso a più motori indipendenti disponibili nella maggior parte delle GPU moderne.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d60704e411a1ba45dd4902ad9101a416391743dd
ms.sourcegitcommit: 622d149edf775af5a9633c2d12ccfddf7000b8fd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2020
ms.locfileid: "104548777"
---
# <a name="multi-engine-synchronization"></a><span data-ttu-id="c8014-103">Sincronizzazione multimotore</span><span class="sxs-lookup"><span data-stu-id="c8014-103">Multi-engine synchronization</span></span>

<span data-ttu-id="c8014-104">La maggior parte delle GPU moderne contiene più motori indipendenti che offrono funzionalità specializzate.</span><span class="sxs-lookup"><span data-stu-id="c8014-104">Most modern GPUs contain multiple independent engines that provide specialized functionality.</span></span> <span data-ttu-id="c8014-105">Molti hanno uno o più motori di copia dedicati e un motore di calcolo, in genere distinti dal motore 3D.</span><span class="sxs-lookup"><span data-stu-id="c8014-105">Many have one or more dedicated copy engines, and a compute engine, usually distinct from the 3D engine.</span></span> <span data-ttu-id="c8014-106">Ognuno di questi motori può eseguire comandi in parallelo tra loro.</span><span class="sxs-lookup"><span data-stu-id="c8014-106">Each of these engines can execute commands in parallel with each other.</span></span> <span data-ttu-id="c8014-107">Direct3D 12 offre un accesso con granularità fine ai motori 3D, di calcolo e di copia, usando code ed elenchi di comandi.</span><span class="sxs-lookup"><span data-stu-id="c8014-107">Direct3D 12 provides fine-grained access to the 3D, compute, and copy engines, using queues and command lists.</span></span>

## <a name="gpu-engines"></a><span data-ttu-id="c8014-108">Motori GPU</span><span class="sxs-lookup"><span data-stu-id="c8014-108">GPU engines</span></span>

<span data-ttu-id="c8014-109">Il diagramma seguente mostra i thread della CPU del titolo, ciascuno dei quali popola una o più code di copia, calcolo e 3D.</span><span class="sxs-lookup"><span data-stu-id="c8014-109">The following diagram shows a title's CPU threads, each populating one or more of the copy, compute, and 3D queues.</span></span> <span data-ttu-id="c8014-110">La coda 3D può gestire tutti e tre i motori GPU; la coda di calcolo può guidare i motori di calcolo e di copia; e la coda di copia semplicemente il motore di copia.</span><span class="sxs-lookup"><span data-stu-id="c8014-110">The 3D queue can drive all three GPU engines; the compute queue can drive the compute and copy engines; and the copy queue simply the copy engine.</span></span>

<span data-ttu-id="c8014-111">Poiché i diversi thread popolano le code, non è possibile fornire una semplice garanzia dell'ordine di esecuzione, quindi la necessità di meccanismi di sincronizzazione &mdash; quando il titolo li richiede.</span><span class="sxs-lookup"><span data-stu-id="c8014-111">As the different threads populate the queues, there can be no simple guarantee of the order of execution, hence the need for synchronization mechanisms&mdash;when the title requires them.</span></span>

![quattro thread che inviano comandi a tre code](images/gpu-engines.png)

<span data-ttu-id="c8014-113">Nell'immagine seguente viene illustrato il modo in cui un titolo può pianificare il lavoro tra più motori GPU, inclusa la sincronizzazione tra i motori quando necessario: Mostra i carichi di lavoro per motore con dipendenze tra i motori.</span><span class="sxs-lookup"><span data-stu-id="c8014-113">The following image illustrate how a title might schedule work across multiple GPU engines, including inter-engine synchronization where necessary: it shows the per-engine workloads with inter-engine dependencies.</span></span> <span data-ttu-id="c8014-114">In questo esempio il motore di copia copia prima di tutto la geometria necessaria per il rendering.</span><span class="sxs-lookup"><span data-stu-id="c8014-114">In this example, the copy engine first copies some geometry necessary for rendering.</span></span> <span data-ttu-id="c8014-115">Il motore 3D attende il completamento di queste copie ed esegue il rendering di un pre-pass sulla geometria.</span><span class="sxs-lookup"><span data-stu-id="c8014-115">The 3D engine waits for these copies to complete, and renders a pre-pass over the geometry.</span></span> <span data-ttu-id="c8014-116">Questa operazione viene quindi utilizzata dal motore di calcolo.</span><span class="sxs-lookup"><span data-stu-id="c8014-116">This is then consumed by the compute engine.</span></span> <span data-ttu-id="c8014-117">I risultati dell' [**invio**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)del motore di calcolo, insieme a diverse operazioni di copia di trama nel motore di copia, vengono usati dal motore 3D per la chiamata di [**progetto**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) finale.</span><span class="sxs-lookup"><span data-stu-id="c8014-117">The results of the compute engine [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch), along with several texture copy operations on the copy engine, are consumed by the 3D engine for the final [**Draw**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) call.</span></span>

![copia, grafica e motori di calcolo che comunicano](images/gpu-sync.png)

<span data-ttu-id="c8014-119">Lo pseudo-codice seguente illustra come un titolo può inviare un carico di lavoro di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="c8014-119">The following pseudo-code illustrates how a title might submit such a workload.</span></span>

``` syntax
// Get per-engine contexts. Note that multiple queues may be exposed
// per engine, however that design is not reflected here.
copyEngine = device->GetCopyEngineContext();
renderEngine = device->GetRenderEngineContext();
computeEngine = device->GetComputeEngineContext();
copyEngine->CopyResource(geometry, ...); // copy geometry
copyEngine->Signal(copyFence, 101);
copyEngine->CopyResource(tex1, ...); // copy textures
copyEngine->CopyResource(tex2, ...); // copy more textures
copyEngine->CopyResource(tex3, ...); // copy more textures
copyEngine->CopyResource(tex4, ...); // copy more textures
copyEngine->Signal(copyFence, 102);
renderEngine->Wait(copyFence, 101); // geometry copied
renderEngine->Draw(); // pre-pass using geometry only into rt1
renderEngine->Signal(renderFence, 201);
computeEngine->Wait(renderFence, 201); // prepass completed
computeEngine->Dispatch(); // lighting calculations on pre-pass (using rt1 as SRV)
computeEngine->Signal(computeFence, 301);
renderEngine->Wait(computeFence, 301); // lighting calculated into buf1
renderEngine->Wait(copyFence, 102); // textures copied
renderEngine->Draw(); // final render using buf1 as SRV, and tex[1-4] SRVs
```

<span data-ttu-id="c8014-120">Lo pseudo-codice seguente illustra la sincronizzazione tra i motori di copia e 3D per ottenere l'allocazione di memoria simile a heap tramite un buffer circolare.</span><span class="sxs-lookup"><span data-stu-id="c8014-120">The following pseudo-code illustrates synchronization between the copy and 3D engines to accomplish heap-like memory allocation via a ring buffer.</span></span> <span data-ttu-id="c8014-121">I titoli hanno la flessibilità di scegliere il giusto equilibrio tra l'ottimizzazione del parallelismo (tramite un buffer di grandi dimensioni) e la riduzione dell'utilizzo della memoria e della latenza (tramite un buffer di piccole dimensioni).</span><span class="sxs-lookup"><span data-stu-id="c8014-121">Titles have the flexibility to choose the right balance between maximizing parallelism (via a large buffer) and reducing memory consumption and latency (via a small buffer).</span></span>

``` syntax
device->CreateBuffer(&ringCB);
for(int i=1;i++){
  if(i > length) copyEngine->Wait(fence1, i - length);
  copyEngine->Map(ringCB, value%length, WRITE, pData); // copy new data
  copyEngine->Signal(fence2, i);
  renderEngine->Wait(fence2, i);
  renderEngine->Draw(); // draw using copied data
  renderEngine->Signal(fence1, i);
}

// example for length = 3:
// copyEngine->Map();
// copyEngine->Signal(fence2, 1); // fence2 = 1  
// copyEngine->Map();
// copyEngine->Signal(fence2, 2); // fence2 = 2
// copyEngine->Map();
// copyEngine->Signal(fence2, 3); // fence2 = 3
// copy engine has exhausted the ring buffer, so must wait for render to consume it
// copyEngine->Wait(fence1, 1); // fence1 == 0, wait
// renderEngine->Wait(fence2, 1); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 1); // fence1 = 1, copy engine now unblocked
// renderEngine->Wait(fence2, 2); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 2); // fence1 = 2
// renderEngine->Wait(fence2, 3); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 3); // fence1 = 3
// now render engine is starved, and so must wait for the copy engine
// renderEngine->Wait(fence2, 4); // fence2 == 3, wait
```

## <a name="multi-engine-scenarios"></a><span data-ttu-id="c8014-122">Scenari multimotore</span><span class="sxs-lookup"><span data-stu-id="c8014-122">Multi-engine scenarios</span></span>

<span data-ttu-id="c8014-123">Direct3D 12 consente di evitare l'esecuzione accidentale di inefficienze dovute a ritardi di sincronizzazione imprevisti.</span><span class="sxs-lookup"><span data-stu-id="c8014-123">Direct3D 12 allows you to avoid accidentally running into inefficiencies caused by unexpected synchronization delays.</span></span> <span data-ttu-id="c8014-124">Consente inoltre di introdurre la sincronizzazione a un livello superiore in cui è possibile determinare la sincronizzazione necessaria con maggiore precisione.</span><span class="sxs-lookup"><span data-stu-id="c8014-124">It also allows you to introduce synchronization at a higher level where the required synchronization can be determined with greater certainty.</span></span> <span data-ttu-id="c8014-125">Un secondo problema per cui gli indirizzi multimotore è quello di rendere più complesse le operazioni più complesse, incluse le transizioni tra 3D e video che erano tradizionalmente costose a causa della sincronizzazione tra più contesti kernel.</span><span class="sxs-lookup"><span data-stu-id="c8014-125">A second issue that multi-engine addresses is to make expensive operations more explicit, which includes transitions between 3D and video that were traditionally costly because of synchronization between multiple kernel contexts.</span></span>

<span data-ttu-id="c8014-126">In particolare, è possibile risolvere gli scenari seguenti con Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="c8014-126">In particular, the following scenarios can be addressed with Direct3D 12.</span></span>

-   <span data-ttu-id="c8014-127">Lavoro GPU asincrono e con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="c8014-127">Asynchronous and low priority GPU work.</span></span> <span data-ttu-id="c8014-128">Ciò consente l'esecuzione simultanea di operazioni di GPU a priorità bassa e operazioni atomiche che consentono a un thread GPU di utilizzare i risultati di un altro thread non sincronizzato senza bloccarsi.</span><span class="sxs-lookup"><span data-stu-id="c8014-128">This enables concurrent execution of low priority GPU work and atomic operations that enable one GPU thread to consume the results of another unsynchronized thread without blocking.</span></span>
-   <span data-ttu-id="c8014-129">Lavoro di calcolo con priorità alta.</span><span class="sxs-lookup"><span data-stu-id="c8014-129">High priority compute work.</span></span> <span data-ttu-id="c8014-130">Con il calcolo in background è possibile interrompere il rendering 3D per eseguire una piccola quantità di lavoro di calcolo con priorità alta.</span><span class="sxs-lookup"><span data-stu-id="c8014-130">With background compute it is possible to interrupt 3D rendering to do a small amount of high priority compute work.</span></span> <span data-ttu-id="c8014-131">I risultati di questo lavoro possono essere ottenuti in anticipo per un'ulteriore elaborazione sulla CPU.</span><span class="sxs-lookup"><span data-stu-id="c8014-131">The results of this work can be obtained early for additional processing on the CPU.</span></span>
-   <span data-ttu-id="c8014-132">Lavoro di calcolo in background.</span><span class="sxs-lookup"><span data-stu-id="c8014-132">Background compute work.</span></span> <span data-ttu-id="c8014-133">Una coda separata con priorità bassa per i carichi di lavoro di calcolo consente a un'applicazione di usare cicli GPU di riserva per eseguire calcoli in background senza impatto negativo sulle attività di rendering (o altre) primarie.</span><span class="sxs-lookup"><span data-stu-id="c8014-133">A separate low priority queue for compute workloads allows an application to utilize spare GPU cycles to perform background computation without negative impact on the primary rendering (or other) tasks.</span></span> <span data-ttu-id="c8014-134">Le attività in background possono includere la decompressione di risorse o l'aggiornamento di simulazioni o strutture di accelerazione.</span><span class="sxs-lookup"><span data-stu-id="c8014-134">Background tasks may include decompression of resources or updating simulations or acceleration structures.</span></span> <span data-ttu-id="c8014-135">Le attività in background devono essere sincronizzate raramente sulla CPU (approssimativamente una volta per fotogramma) per evitare blocchi o rallentare il lavoro in primo piano.</span><span class="sxs-lookup"><span data-stu-id="c8014-135">Background tasks should be synchronized on the CPU infrequently (approximately once per frame) to avoid stalling or slowing foreground work.</span></span>
-   <span data-ttu-id="c8014-136">Streaming e caricamento dei dati.</span><span class="sxs-lookup"><span data-stu-id="c8014-136">Streaming and uploading data.</span></span> <span data-ttu-id="c8014-137">Una coda di copia separata sostituisce i concetti D3D11 dei dati iniziali e l'aggiornamento delle risorse.</span><span class="sxs-lookup"><span data-stu-id="c8014-137">A separate copy queue replaces the D3D11 concepts of initial data and updating resources.</span></span> <span data-ttu-id="c8014-138">Sebbene l'applicazione sia responsabile di ulteriori dettagli nel modello Direct3D 12, questa responsabilità viene fornita con energia.</span><span class="sxs-lookup"><span data-stu-id="c8014-138">Although the application is responsible for more details in the Direct3D 12 model, this responsibility comes with power.</span></span> <span data-ttu-id="c8014-139">L'applicazione può controllare la quantità di memoria di sistema dedicata al buffering dei dati di caricamento.</span><span class="sxs-lookup"><span data-stu-id="c8014-139">The application can control how much system memory is devoted to buffering upload data.</span></span> <span data-ttu-id="c8014-140">L'app può scegliere quando e in che modo eseguire la sincronizzazione (CPU e GPU, bloccando e non bloccando) ed è possibile tenere traccia dello stato di avanzamento e controllare la quantità di lavoro in coda.</span><span class="sxs-lookup"><span data-stu-id="c8014-140">The app can choose when and how (CPU vs GPU, blocking vs non-blocking) to synchronize, and can track progress and control the amount of queued work.</span></span>
-   <span data-ttu-id="c8014-141">Maggiore parallelismo.</span><span class="sxs-lookup"><span data-stu-id="c8014-141">Increased parallelism.</span></span> <span data-ttu-id="c8014-142">Le applicazioni possono usare code più profonde per i carichi di lavoro in background (ad esempio, decodifica video) quando hanno code separate per il lavoro in primo piano.</span><span class="sxs-lookup"><span data-stu-id="c8014-142">Applications can use deeper queues for background workloads (e.g. video decode) when they have separate queues for foreground work.</span></span>

<span data-ttu-id="c8014-143">In Direct3D 12 il concetto di coda dei comandi è la rappresentazione API di una sequenza di lavoro approssimativamente seriale inviata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c8014-143">In Direct3D 12 the concept of a command queue is the API representation of a roughly serial sequence of work submitted by the application.</span></span> <span data-ttu-id="c8014-144">Le barriere e altre tecniche consentono l'esecuzione di questo lavoro in una pipeline o non in ordine, ma l'applicazione Visualizza solo una sequenza temporale di completamento singola.</span><span class="sxs-lookup"><span data-stu-id="c8014-144">Barriers and other techniques allow this work to be executed in a pipeline or out of order, but the application only sees a single completion timeline.</span></span> <span data-ttu-id="c8014-145">Corrisponde al contesto immediato in D3D11.</span><span class="sxs-lookup"><span data-stu-id="c8014-145">This corresponds to the immediate context in D3D11.</span></span>

## <a name="synchronization-apis"></a><span data-ttu-id="c8014-146">API di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="c8014-146">Synchronization APIs</span></span>

### <a name="devices-and-queues"></a><span data-ttu-id="c8014-147">Dispositivi e code</span><span class="sxs-lookup"><span data-stu-id="c8014-147">Devices and queues</span></span>

<span data-ttu-id="c8014-148">Il dispositivo Direct3D 12 dispone di metodi per creare e recuperare le code dei comandi di tipi e priorità diversi.</span><span class="sxs-lookup"><span data-stu-id="c8014-148">The Direct3D 12 device has methods to create and retrieve command queues of different types and priorities.</span></span> <span data-ttu-id="c8014-149">La maggior parte delle applicazioni deve usare le code di comando predefinite perché consentono l'uso condiviso da parte di altri componenti.</span><span class="sxs-lookup"><span data-stu-id="c8014-149">Most applications should use the default command queues because these allow for shared usage by other components.</span></span> <span data-ttu-id="c8014-150">Le applicazioni con requisiti di concorrenza aggiuntivi possono creare code aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="c8014-150">Applications with additional concurrency requirements can create additional queues.</span></span> <span data-ttu-id="c8014-151">Le code vengono specificate dal tipo di elenco dei comandi utilizzato.</span><span class="sxs-lookup"><span data-stu-id="c8014-151">Queues are specified by the command list type that they consume.</span></span>

<span data-ttu-id="c8014-152">Vedere i seguenti metodi di creazione di [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).</span><span class="sxs-lookup"><span data-stu-id="c8014-152">Refer to the following creation methods of [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).</span></span>

-   <span data-ttu-id="c8014-153">[**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : crea una coda di comandi basata su informazioni in una struttura di [**\_ Descrizione della \_ coda \_ di comandi Direct3D 12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .</span><span class="sxs-lookup"><span data-stu-id="c8014-153">[**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : creates a command queue based on information in a [**Direct3D 12\_COMMAND\_QUEUE\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) structure.</span></span>
-   <span data-ttu-id="c8014-154">[**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : crea un elenco di comandi di tipo tipo [**\_ \_ elenco di \_ comandi Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span><span class="sxs-lookup"><span data-stu-id="c8014-154">[**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : creates a command list of type [**Direct3D 12\_COMMAND\_LIST\_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>
-   <span data-ttu-id="c8014-155">[**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : crea una recinzione, notando i flag nei [**\_ \_ flag di recinzione Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags).</span><span class="sxs-lookup"><span data-stu-id="c8014-155">[**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : creates a fence, noting the flags in [**Direct3D 12\_FENCE\_FLAGS**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags).</span></span> <span data-ttu-id="c8014-156">Le barriere vengono utilizzate per sincronizzare le code.</span><span class="sxs-lookup"><span data-stu-id="c8014-156">Fences are used to synchronize queues.</span></span>

<span data-ttu-id="c8014-157">Le code di tutti i tipi (3D, COMPUTE e Copy) condividono la stessa interfaccia e sono basate su tutti gli elenchi di comandi.</span><span class="sxs-lookup"><span data-stu-id="c8014-157">Queues of all types (3D, compute and copy) share the same interface and are all command-list based.</span></span>

<span data-ttu-id="c8014-158">Vedere i metodi seguenti per [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).</span><span class="sxs-lookup"><span data-stu-id="c8014-158">Refer to the following methods of [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue).</span></span>

-   <span data-ttu-id="c8014-159">[**Oggetti executecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : Invia una matrice di elenchi di comandi per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c8014-159">[**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) : submits an array of command lists for execution.</span></span> <span data-ttu-id="c8014-160">Ogni elenco di comandi definito da [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).</span><span class="sxs-lookup"><span data-stu-id="c8014-160">Each command list being defined by [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>
-   <span data-ttu-id="c8014-161">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : imposta un valore di recinzione quando la coda (in esecuzione sulla GPU) raggiunge un determinato punto.</span><span class="sxs-lookup"><span data-stu-id="c8014-161">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : sets a fence value when the queue (running on the GPU) reaches a certain point.</span></span>
-   <span data-ttu-id="c8014-162">[**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : la coda attende fino a quando il limite specificato non raggiunge il valore specificato.</span><span class="sxs-lookup"><span data-stu-id="c8014-162">[**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : the queue waits until the specified fence reaches the specified value.</span></span>

<span data-ttu-id="c8014-163">Si noti che i bundle non vengono utilizzati da alcuna coda e pertanto questo tipo non può essere utilizzato per creare una coda.</span><span class="sxs-lookup"><span data-stu-id="c8014-163">Note that bundles are not consumed by any queues and therefore this type cannot be used to create a queue.</span></span>

### <a name="fences"></a><span data-ttu-id="c8014-164">Barriere</span><span class="sxs-lookup"><span data-stu-id="c8014-164">Fences</span></span>

<span data-ttu-id="c8014-165">L'API multimotore fornisce API esplicite per creare e sincronizzare usando le schermate.</span><span class="sxs-lookup"><span data-stu-id="c8014-165">The multi-engine API provides explicit APIs to create and synchronize using fences.</span></span> <span data-ttu-id="c8014-166">Una recinzione è un costrutto di sincronizzazione controllato da un valore UINT64.</span><span class="sxs-lookup"><span data-stu-id="c8014-166">A fence is a synchronization construct controlled by a UINT64 value.</span></span> <span data-ttu-id="c8014-167">I valori di recinzione vengono impostati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c8014-167">Fence values are set by the application.</span></span> <span data-ttu-id="c8014-168">Un'operazione di segnalazione modifica il valore della recinzione e un blocco dell'operazione di attesa fino a quando il limite non raggiunge il valore richiesto o un valore superiore.</span><span class="sxs-lookup"><span data-stu-id="c8014-168">A signal operation modifies the fence value and a wait operation blocks until the fence has reached the requested value or greater.</span></span> <span data-ttu-id="c8014-169">Un evento può essere generato quando una recinzione raggiunge un determinato valore.</span><span class="sxs-lookup"><span data-stu-id="c8014-169">An event can be fired when a fence reaches a certain value.</span></span>

<span data-ttu-id="c8014-170">Vedere i metodi dell'interfaccia [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) .</span><span class="sxs-lookup"><span data-stu-id="c8014-170">Refer to the methods of the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface.</span></span>

-   <span data-ttu-id="c8014-171">[**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : restituisce il valore corrente della recinzione.</span><span class="sxs-lookup"><span data-stu-id="c8014-171">[**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : returns the current value of the fence.</span></span>
-   <span data-ttu-id="c8014-172">[**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : determina l'attivazione di un evento quando la barriera raggiunge un valore specificato.</span><span class="sxs-lookup"><span data-stu-id="c8014-172">[**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) : causes an event to fire when the fence reaches a given value.</span></span>
-   <span data-ttu-id="c8014-173">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : imposta la barriera sul valore specificato.</span><span class="sxs-lookup"><span data-stu-id="c8014-173">[**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : sets the fence to the given value.</span></span>

<span data-ttu-id="c8014-174">Le recinzioni consentono l'accesso alla CPU al valore di limite corrente e le attese e i segnali della CPU.</span><span class="sxs-lookup"><span data-stu-id="c8014-174">Fences allow CPU access to the current fence value, and CPU waits and signals.</span></span>

<span data-ttu-id="c8014-175">Il metodo [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) sull'interfaccia [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) aggiorna una recinzione dal lato CPU.</span><span class="sxs-lookup"><span data-stu-id="c8014-175">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) method on the [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) interface updates a fence from the CPU side.</span></span> <span data-ttu-id="c8014-176">Questo aggiornamento viene eseguito immediatamente.</span><span class="sxs-lookup"><span data-stu-id="c8014-176">This update occurs immediately.</span></span> <span data-ttu-id="c8014-177">Il metodo [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) su [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) aggiorna una recinzione dal lato GPU.</span><span class="sxs-lookup"><span data-stu-id="c8014-177">The [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) method on [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) updates a fence from the GPU side.</span></span> <span data-ttu-id="c8014-178">Questo aggiornamento si verifica dopo il completamento di tutte le altre operazioni nella coda dei comandi.</span><span class="sxs-lookup"><span data-stu-id="c8014-178">This update occurs after all other operations on the command queue have been completed.</span></span>

<span data-ttu-id="c8014-179">Tutti i nodi in una configurazione a più motori possono leggere e reagire a qualsiasi limite che raggiunga il valore corretto.</span><span class="sxs-lookup"><span data-stu-id="c8014-179">All nodes in a multi-engine setup can read and react to any fence reaching the right value.</span></span>

<span data-ttu-id="c8014-180">Le applicazioni impostano i propri valori di recinzione, un punto di partenza valido potrebbe aumentare una barriera una volta per ogni fotogramma.</span><span class="sxs-lookup"><span data-stu-id="c8014-180">Applications set their own fence values, a good starting point might be increasing a fence once per frame.</span></span>

<span data-ttu-id="c8014-181">Una recinzione *può* essere *riavvolta*.</span><span class="sxs-lookup"><span data-stu-id="c8014-181">A fence *may* be *rewound*.</span></span> <span data-ttu-id="c8014-182">Ciò significa che non è necessario incrementare solo il valore del limite.</span><span class="sxs-lookup"><span data-stu-id="c8014-182">This means that the fence value does not need to solely increment.</span></span> <span data-ttu-id="c8014-183">Se un'operazione di **segnalazione** viene accodata in due code di comando diverse o se due thread della CPU chiamano il **segnale** su un limite, è possibile che si verifichi una gara per determinare quale **segnale** viene completato per ultimo e quindi quale valore di limite è quello che resterà.</span><span class="sxs-lookup"><span data-stu-id="c8014-183">If a **Signal** operation is enqueued on two different command queues, or if two CPU threads are both calling **Signal** on a fence, there may be a race to determine which **Signal** completes last, and therefore which fence value is the one which will remain.</span></span> <span data-ttu-id="c8014-184">Se una recinzione viene riavvolta, eventuali nuove attese (incluse le richieste **SetEventOnCompletion** ) verranno confrontate con il nuovo valore di limite inferiore e pertanto potrebbero non essere soddisfatte, anche se il valore della recinzione era in precedenza sufficientemente elevato da soddisfarle.</span><span class="sxs-lookup"><span data-stu-id="c8014-184">If a fence is rewound, any new waits (including **SetEventOnCompletion** requests) will be compared against the new lower fence value, and therefore may not be satisfied, even if the fence value had previously been high enough to satisfy them.</span></span> <span data-ttu-id="c8014-185">Se si verifica una corsa, tra un valore che soddisferà un'attesa in attesa e un valore inferiore che non sarà, l'attesa *verrà* soddisfatta indipendentemente dal valore che rimane in seguito.</span><span class="sxs-lookup"><span data-stu-id="c8014-185">If a race does occur, between a value which will satisfy an outstanding wait, and a lower value which will not, the wait *will* be satisfied regardless of which value remains afterwards.</span></span>

<span data-ttu-id="c8014-186">Le API di recinzione forniscono funzionalità di sincronizzazione potenti, ma possono creare problemi di debug potenzialmente difficili.</span><span class="sxs-lookup"><span data-stu-id="c8014-186">The fence APIs provide powerful synchronization functionality but can create potentially difficult to debug issues.</span></span> <span data-ttu-id="c8014-187">È consigliabile usare ogni limite solo per indicare lo stato di avanzamento in una sequenza temporale per impedire le gare tra i SignalR.</span><span class="sxs-lookup"><span data-stu-id="c8014-187">It is recommended that each fence only be used to indicate progress on one timeline to prevent races between signalers.</span></span>

### <a name="copy-and-compute-command-lists"></a><span data-ttu-id="c8014-188">Elenchi di comandi di copia e calcolo</span><span class="sxs-lookup"><span data-stu-id="c8014-188">Copy and compute command lists</span></span>

<span data-ttu-id="c8014-189">Tutti e tre i tipi di elenco dei comandi usano l'interfaccia [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) , ma solo un subset dei metodi è supportato per le copie e le risorse di calcolo.</span><span class="sxs-lookup"><span data-stu-id="c8014-189">All three types of command list use the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface, however only a subset of the methods are supported for copy and compute.</span></span>

<span data-ttu-id="c8014-190">Gli elenchi di comandi di copia e calcolo possono usare i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c8014-190">Copy and compute command lists can use the following methods.</span></span>

-   [<span data-ttu-id="c8014-191">**Chiudi**</span><span class="sxs-lookup"><span data-stu-id="c8014-191">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [<span data-ttu-id="c8014-192">**CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="c8014-192">**CopyBufferRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="c8014-193">**CopyResource**</span><span class="sxs-lookup"><span data-stu-id="c8014-193">**CopyResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="c8014-194">**CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="c8014-194">**CopyTextureRegion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="c8014-195">**CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="c8014-195">**CopyTiles**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="c8014-196">**Reset**</span><span class="sxs-lookup"><span data-stu-id="c8014-196">**Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [<span data-ttu-id="c8014-197">**ResourceBarrier**</span><span class="sxs-lookup"><span data-stu-id="c8014-197">**ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

<span data-ttu-id="c8014-198">Gli elenchi di comandi Compute possono usare anche i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="c8014-198">Compute command lists can also use the following methods.</span></span>

-   [<span data-ttu-id="c8014-199">**ClearState**</span><span class="sxs-lookup"><span data-stu-id="c8014-199">**ClearState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [<span data-ttu-id="c8014-200">**ClearUnorderedAccessViewFloat**</span><span class="sxs-lookup"><span data-stu-id="c8014-200">**ClearUnorderedAccessViewFloat**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="c8014-201">**ClearUnorderedAccessViewUint**</span><span class="sxs-lookup"><span data-stu-id="c8014-201">**ClearUnorderedAccessViewUint**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="c8014-202">**DiscardResource**</span><span class="sxs-lookup"><span data-stu-id="c8014-202">**DiscardResource**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [<span data-ttu-id="c8014-203">**Dispatch**</span><span class="sxs-lookup"><span data-stu-id="c8014-203">**Dispatch**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="c8014-204">**ExecuteIndirect**</span><span class="sxs-lookup"><span data-stu-id="c8014-204">**ExecuteIndirect**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [<span data-ttu-id="c8014-205">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="c8014-205">**SetComputeRoot32BitConstant**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="c8014-206">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="c8014-206">**SetComputeRoot32BitConstants**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [<span data-ttu-id="c8014-207">**SetComputeRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="c8014-207">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="c8014-208">**SetComputeRootDescriptorTable**</span><span class="sxs-lookup"><span data-stu-id="c8014-208">**SetComputeRootDescriptorTable**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [<span data-ttu-id="c8014-209">**SetComputeRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="c8014-209">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="c8014-210">**SetComputeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="c8014-210">**SetComputeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [<span data-ttu-id="c8014-211">**SetComputeRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="c8014-211">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="c8014-212">**SetDescriptorHeaps**</span><span class="sxs-lookup"><span data-stu-id="c8014-212">**SetDescriptorHeaps**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [<span data-ttu-id="c8014-213">**SetPipelineState**</span><span class="sxs-lookup"><span data-stu-id="c8014-213">**SetPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [<span data-ttu-id="c8014-214">**SetPredication**</span><span class="sxs-lookup"><span data-stu-id="c8014-214">**SetPredication**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

<span data-ttu-id="c8014-215">Gli elenchi di comandi di calcolo devono impostare un oggetto PSO di calcolo quando si chiama [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).</span><span class="sxs-lookup"><span data-stu-id="c8014-215">Compute command lists must set a compute PSO when calling [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).</span></span>

<span data-ttu-id="c8014-216">I bundle non possono essere usati con le code o gli elenchi di comandi di calcolo o copia.</span><span class="sxs-lookup"><span data-stu-id="c8014-216">Bundles cannot be used with compute or copy command lists or queues.</span></span>

## <a name="pipelined-compute-and-graphics-example"></a><span data-ttu-id="c8014-217">Esempio di calcolo e di grafica in pipeline</span><span class="sxs-lookup"><span data-stu-id="c8014-217">Pipelined compute and graphics example</span></span>

<span data-ttu-id="c8014-218">Questo esempio Mostra come usare la sincronizzazione della recinzione per creare una pipeline di lavoro di calcolo in una coda (a cui fa riferimento `pComputeQueue` ) che viene utilizzata dalla grafica lavorare sulla coda `pGraphicsQueue` .</span><span class="sxs-lookup"><span data-stu-id="c8014-218">This example shows how fence synchronization can be used to create a pipeline of compute work on a queue (referenced by `pComputeQueue`) that's consumed by graphics work on queue `pGraphicsQueue`.</span></span> <span data-ttu-id="c8014-219">Il lavoro di calcolo e di grafica viene sottoposto a pipeline con la coda grafica che utilizza il risultato del lavoro di calcolo da diversi frame e viene utilizzato un evento CPU per limitare il lavoro totale in coda.</span><span class="sxs-lookup"><span data-stu-id="c8014-219">The compute and graphics work is pipelined with the graphics queue consuming the result of compute work from several frames back, and a CPU event is used to throttle the total work queued overall.</span></span>

```cpp
void PipelinedComputeGraphics()
{
    const UINT CpuLatency = 3;
    const UINT ComputeGraphicsLatency = 2;

    HANDLE handle = CreateEvent(nullptr, FALSE, FALSE, nullptr);

    UINT64 FrameNumber = 0;

    while (1)
    {
        if (FrameNumber > ComputeGraphicsLatency)
        {
            pComputeQueue->Wait(pGraphicsFence,
                FrameNumber - ComputeGraphicsLatency);
        }

        if (FrameNumber > CpuLatency)
        {
            pComputeFence->SetEventOnFenceCompletion(
                FrameNumber - CpuLatency,
                handle);
            WaitForSingleObject(handle, INFINITE);
        }

        ++FrameNumber;

        pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
        pComputeQueue->Signal(pComputeFence, FrameNumber);
        if (FrameNumber > ComputeGraphicsLatency)
        {
            UINT GraphicsFrameNumber = FrameNumber - ComputeGraphicsLatency;
            pGraphicsQueue->Wait(pComputeFence, GraphicsFrameNumber);
            pGraphicsQueue->ExecuteCommandLists(1, &pGraphicsCommandList);
            pGraphicsQueue->Signal(pGraphicsFence, GraphicsFrameNumber);
        }
    }
}
```

<span data-ttu-id="c8014-220">Per supportare questo pipelining, deve essere presente un buffer di `ComputeGraphicsLatency+1` copie diverse dei dati che passano dalla coda di calcolo alla coda grafica.</span><span class="sxs-lookup"><span data-stu-id="c8014-220">To support this pipelining, there must be a buffer of `ComputeGraphicsLatency+1` different copies of the data passing from the compute queue to the graphics queue.</span></span> <span data-ttu-id="c8014-221">Gli elenchi di comandi devono usare UAV e il riferimento indiretto per leggere e scrivere dalla "versione" appropriata dei dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="c8014-221">The command lists must use UAVs and indirection to read and write from the appropriate “version” of the data in the buffer.</span></span> <span data-ttu-id="c8014-222">La coda di calcolo deve attendere il completamento della lettura da parte della coda grafica dei dati per il frame N prima di poter scrivere il frame `N+ComputeGraphicsLatency` .</span><span class="sxs-lookup"><span data-stu-id="c8014-222">The compute queue must wait until the graphics queue has finished reading from the data for frame N before it can write frame `N+ComputeGraphicsLatency`.</span></span>

<span data-ttu-id="c8014-223">Si noti che la quantità di coda di calcolo elaborata in relazione alla CPU non dipende direttamente dalla quantità di buffering necessaria. Tuttavia, l'accodamento del lavoro della GPU oltre la quantità di spazio disponibile nel buffer è meno importante.</span><span class="sxs-lookup"><span data-stu-id="c8014-223">Note that the amount of compute queue worked relative to the CPU does not depend directly on the amount of buffering required, however, queuing GPU work beyond the amount of buffer space available is less valuable.</span></span>

<span data-ttu-id="c8014-224">Un meccanismo alternativo per evitare riferimenti indiretti consiste nel creare più elenchi di comandi corrispondenti a ognuna delle versioni "rinominate" dei dati.</span><span class="sxs-lookup"><span data-stu-id="c8014-224">An alternative mechanism to avoid indirection would be to create multiple command lists corresponding to each of the “renamed” versions of the data.</span></span> <span data-ttu-id="c8014-225">Nell'esempio seguente viene usata questa tecnica durante l'estensione dell'esempio precedente per consentire l'esecuzione più asincrona delle code di calcolo e di grafica.</span><span class="sxs-lookup"><span data-stu-id="c8014-225">The next example uses this technique while extending the previous example to allow the compute and graphics queues to run more asynchronously.</span></span>

## <a name="asynchronous-compute-and-graphics-example"></a><span data-ttu-id="c8014-226">Esempio di calcolo e di grafica asincrono</span><span class="sxs-lookup"><span data-stu-id="c8014-226">Asynchronous compute and graphics example</span></span>

<span data-ttu-id="c8014-227">Questo esempio seguente consente di eseguire il rendering asincrono della grafica dalla coda di calcolo.</span><span class="sxs-lookup"><span data-stu-id="c8014-227">This next example allows graphics to render asynchronously from the compute queue.</span></span> <span data-ttu-id="c8014-228">Tra le due fasi è ancora presente una quantità fissa di dati memorizzati nel buffer, ma ora il lavoro della grafica viene eseguito in modo indipendente e usa i risultati più aggiornati della fase di calcolo, come noto sulla CPU, quando il lavoro della grafica viene accodato.</span><span class="sxs-lookup"><span data-stu-id="c8014-228">There is still a fixed amount of buffered data between the two stages, however now graphics work proceeds independently and uses the most up-to-date result of the compute stage as known on the CPU when the graphics work is queued.</span></span> <span data-ttu-id="c8014-229">Questa operazione è utile se il lavoro di grafica è stato aggiornato da un'altra origine, ad esempio l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c8014-229">This would be useful if the graphics work was being updated by another source, for example user input.</span></span> <span data-ttu-id="c8014-230">È necessario che siano presenti più elenchi di comandi per consentire il `ComputeGraphicsLatency` funzionamento dei frame di grafica per volta e che la funzione `UpdateGraphicsCommandList` rappresenti l'aggiornamento dell'elenco dei comandi per includere i dati di input più recenti e la lettura dai dati di calcolo dal buffer appropriato.</span><span class="sxs-lookup"><span data-stu-id="c8014-230">There must be multiple command lists to allow the `ComputeGraphicsLatency` frames of graphics work to be in flight at a time, and the function `UpdateGraphicsCommandList` represents updating the command list to include the most recent input data and read from the compute data from the appropriate buffer.</span></span>

<span data-ttu-id="c8014-231">La coda di calcolo deve comunque attendere il completamento della coda grafica con i buffer di pipe, ma viene introdotta una terza recinzione ( `pGraphicsComputeFence` ) in modo che lo stato di avanzamento della grafica che legge il lavoro di calcolo e lo stato di avanzamento della grafica in generale possano essere rilevati.</span><span class="sxs-lookup"><span data-stu-id="c8014-231">The compute queue must still wait for the graphics queue to finish with the pipe buffers, but a third fence (`pGraphicsComputeFence`) is introduced so that the progress of graphics reading compute work versus graphics progress in general can be tracked.</span></span> <span data-ttu-id="c8014-232">Ciò riflette il fatto che ora i fotogrammi grafici consecutivi possono leggere dallo stesso risultato di calcolo o ignorare un risultato di calcolo.</span><span class="sxs-lookup"><span data-stu-id="c8014-232">This reflects the fact that now consecutive graphics frames could read from the same compute result or could skip a compute result.</span></span> <span data-ttu-id="c8014-233">Una progettazione più efficiente ma leggermente più complessa usa solo la barriera grafica singola e archivia un mapping ai frame di calcolo usati da ogni frame di grafica.</span><span class="sxs-lookup"><span data-stu-id="c8014-233">A more efficient but slightly more complicated design would use just the single graphics fence and store a mapping to the compute frames used by each graphics frame.</span></span>

```cpp
void AsyncPipelinedComputeGraphics()
{
    const UINT CpuLatency{ 3 };
    const UINT ComputeGraphicsLatency{ 2 };

    // The compute fence is at index 0; the graphics fence is at index 1.
    ID3D12Fence* rgpFences[]{ pComputeFence, pGraphicsFence };
    HANDLE handles[2];
    handles[0] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    handles[1] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    UINT FrameNumbers[]{ 0, 0 };

    ID3D12GraphicsCommandList* rgpGraphicsCommandLists[CpuLatency];
    CreateGraphicsCommandLists(ARRAYSIZE(rgpGraphicsCommandLists),
        rgpGraphicsCommandLists);

    // Graphics needs to wait for the first compute frame to complete; this is the
    // only wait that the graphics queue will perform.
    pGraphicsQueue->Wait(pComputeFence, 1);

    while (true)
    {
        for (auto i = 0; i < 2; ++i)
        {
            if (FrameNumbers[i] > CpuLatency)
            {
                rgpFences[i]->SetEventOnCompletion(
                    FrameNumbers[i] - CpuLatency,
                    handles[i]);
            }
            else
            {
                ::SetEvent(handles[i]);
            }
        }


        auto WaitResult = ::WaitForMultipleObjects(2, handles, FALSE, INFINITE);
        if (WaitResult > WAIT_OBJECT_0 + 1) continue;
        auto Stage = WaitResult - WAIT_OBJECT_0;
        ++FrameNumbers[Stage];

        switch (Stage)
        {
        case 0:
        {
            if (FrameNumbers[Stage] > ComputeGraphicsLatency)
            {
                pComputeQueue->Wait(pGraphicsComputeFence,
                    FrameNumbers[Stage] - ComputeGraphicsLatency);
            }
            pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
            pComputeQueue->Signal(pComputeFence, FrameNumbers[Stage]);
            break;
        }
        case 1:
        {
            // Recall that the GPU queue started with a wait for pComputeFence, 1
            UINT64 CompletedComputeFrames = min(1,
                pComputeFence->GetCompletedValue());
            UINT64 PipeBufferIndex =
                (CompletedComputeFrames - 1) % ComputeGraphicsLatency;
            UINT64 CommandListIndex = (FrameNumbers[Stage] - 1) % CpuLatency;
            // Update graphics command list based on CPU input and using the appropriate
            // buffer index for data produced by compute.
            UpdateGraphicsCommandList(PipeBufferIndex,
                rgpGraphicsCommandLists[CommandListIndex]);

            // Signal *before* new rendering to indicate what compute work
            // the graphics queue is DONE with
            pGraphicsQueue->Signal(pGraphicsComputeFence, CompletedComputeFrames - 1);
            pGraphicsQueue->ExecuteCommandLists(1,
                rgpGraphicsCommandLists + PipeBufferIndex);
            pGraphicsQueue->Signal(pGraphicsFence, FrameNumbers[Stage]);
            break;
        }
        }
    }
}
```

## <a name="multi-queue-resource-access"></a><span data-ttu-id="c8014-234">Accesso alle risorse in più code</span><span class="sxs-lookup"><span data-stu-id="c8014-234">Multi-queue resource access</span></span>

<span data-ttu-id="c8014-235">Per accedere a una risorsa in più di una coda, un'applicazione deve rispettare le regole seguenti.</span><span class="sxs-lookup"><span data-stu-id="c8014-235">To access a resource on more than one queue an application must adhere to the following rules.</span></span>

-   <span data-ttu-id="c8014-236">L'accesso alle risorse (vedere [**\_ \_ gli Stati delle risorse Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) è determinato dall'oggetto Queue della classe del tipo di coda not.</span><span class="sxs-lookup"><span data-stu-id="c8014-236">Resource access (refer to [**Direct3D 12\_RESOURCE\_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) is determined by queue type class not queue object.</span></span> <span data-ttu-id="c8014-237">Esistono due classi di tipo Queue: COMPUTE/3D Queue è una classe di tipo, Copy è una seconda classe di tipi.</span><span class="sxs-lookup"><span data-stu-id="c8014-237">There are two type classes of queue: Compute/3D queue is one type class, Copy is a second type class.</span></span> <span data-ttu-id="c8014-238">Pertanto, una risorsa che presenta una barriera allo \_ stato della risorsa non pixel shader in \_ \_ una coda 3D può essere usata in tale stato in qualsiasi coda 3D o di calcolo, in base ai requisiti di sincronizzazione che richiedono la serializzazione della maggior parte delle Scritture.</span><span class="sxs-lookup"><span data-stu-id="c8014-238">So a resource that has a barrier to the NON\_PIXEL\_SHADER\_RESOURCE state on one 3D queue can be used in that state on any 3D or Compute queue, subject to synchronization requirements which require most writes to be serialized.</span></span> <span data-ttu-id="c8014-239">Gli Stati delle risorse condivisi tra le due classi di tipi (origine di copia \_ e \_ destinazione di copia) sono considerati stati diversi per ogni classe di tipo.</span><span class="sxs-lookup"><span data-stu-id="c8014-239">The resource states that are shared between the two type classes (COPY\_SOURCE and COPY\_DEST) are considered different states for each type class.</span></span> <span data-ttu-id="c8014-240">In questo modo, se una risorsa esegue una transizione a copia \_ dest in una coda di copia, non è accessibile come destinazione della copia dalle code 3D o di calcolo e viceversa.</span><span class="sxs-lookup"><span data-stu-id="c8014-240">So that if a resource transitions to COPY\_DEST on a Copy queue it is not accessible as a copy destination from 3D or Compute queues and vice versa.</span></span>

    <span data-ttu-id="c8014-241">Da riepilogare.</span><span class="sxs-lookup"><span data-stu-id="c8014-241">To summarize.</span></span>

    -   <span data-ttu-id="c8014-242">Una coda "oggetto" è un'unica coda.</span><span class="sxs-lookup"><span data-stu-id="c8014-242">A queue "object" is any single queue.</span></span>
    -   <span data-ttu-id="c8014-243">Una coda "Type" è una delle tre seguenti: COMPUTE, 3D e Copy.</span><span class="sxs-lookup"><span data-stu-id="c8014-243">A queue "type" is any one of these three: Compute, 3D, and Copy.</span></span>
    -   <span data-ttu-id="c8014-244">Una coda "Type class" è una delle due seguenti: COMPUTE/3D e Copy.</span><span class="sxs-lookup"><span data-stu-id="c8014-244">A queue "type class" is any one of these two: Compute/3D and Copy.</span></span>

-   <span data-ttu-id="c8014-245">I flag di copia (COPY \_ dest e copy \_ source) usati come stati iniziali rappresentano gli Stati nella classe 3D/Compute Type.</span><span class="sxs-lookup"><span data-stu-id="c8014-245">The COPY flags (COPY\_DEST and COPY\_SOURCE) used as initial states represent states in the 3D/Compute type class.</span></span> <span data-ttu-id="c8014-246">Per usare una risorsa inizialmente in una coda di copia, deve iniziare nello stato comune.</span><span class="sxs-lookup"><span data-stu-id="c8014-246">To use a resource initially on a Copy queue it should start in the COMMON state.</span></span> <span data-ttu-id="c8014-247">Lo stato comune può essere usato per tutti gli utilizzi in una coda di copia usando le transizioni di stato implicite.</span><span class="sxs-lookup"><span data-stu-id="c8014-247">The COMMON state can be used for all usages on a Copy queue using the implicit state transitions.</span></span> 
-   <span data-ttu-id="c8014-248">Anche se lo stato della risorsa è condiviso tra tutte le code di calcolo e 3D, non è consentito scrivere contemporaneamente nella risorsa in code diverse.</span><span class="sxs-lookup"><span data-stu-id="c8014-248">Although resource state is shared across all Compute and 3D queues, it is not permitted to write to the resource simultaneously on different queues.</span></span> <span data-ttu-id="c8014-249">"Simultaneamente" indica che non è stata eseguita la sincronizzazione. l'esecuzione non sincronizzata non è possibile in alcuni componenti hardware.</span><span class="sxs-lookup"><span data-stu-id="c8014-249">"Simultaneously" here means unsynchronized, noting unsynchronized execution is not possible on some hardware.</span></span> <span data-ttu-id="c8014-250">Si applicano le regole seguenti.</span><span class="sxs-lookup"><span data-stu-id="c8014-250">The following rules apply.</span></span>

    -   <span data-ttu-id="c8014-251">Una sola coda può scrivere in una risorsa alla volta.</span><span class="sxs-lookup"><span data-stu-id="c8014-251">Only one queue can write to a resource at a time.</span></span>
    -   <span data-ttu-id="c8014-252">Più code possono leggere dalla risorsa, purché non leggano i byte modificati dal writer (la lettura dei byte scritti simultaneamente produce risultati non definiti).</span><span class="sxs-lookup"><span data-stu-id="c8014-252">Multiple queues can read from the resource as long as they don’t read the bytes being modified by the writer (reading bytes being simultaneously written produces undefined results).</span></span>
    -   <span data-ttu-id="c8014-253">È necessario utilizzare una recinzione per sincronizzare dopo la scrittura prima che un'altra coda possa leggere i byte scritti o effettuare qualsiasi accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="c8014-253">A fence must be used to synchronize after writing before another queue can read the written bytes or make any write access.</span></span>

-   <span data-ttu-id="c8014-254">I buffer indietro presentati devono trovarsi nello \_ stato comune della risorsa Direct3D 12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c8014-254">Back buffers being presented must be in the Direct3D 12\_RESOURCE\_STATE\_COMMON state.</span></span> 

## <a name="related-topics"></a><span data-ttu-id="c8014-255">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8014-255">Related topics</span></span>

[<span data-ttu-id="c8014-256">Guida per programmatori Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c8014-256">Direct3D 12 programming guide</span></span>](directx-12-programming-guide.md)

[<span data-ttu-id="c8014-257">Uso delle barriere delle risorse per sincronizzare gli Stati delle risorse in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c8014-257">Using resource barriers to synchronize resource states in Direct3D 12</span></span>](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[<span data-ttu-id="c8014-258">Gestione della memoria in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c8014-258">Memory management in Direct3D 12</span></span>](memory-management.md)
