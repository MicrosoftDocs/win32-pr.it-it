---
title: Glossario di Direct3D 12
description: Questi termini sono specifici di Direct3D 12.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a84b4b2e5a993b33b4c322b91682c8f9b5499bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548879"
---
# <a name="direct3d-12-glossary"></a><span data-ttu-id="86621-103">Glossario di Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="86621-103">Direct3D 12 glossary</span></span>

<span data-ttu-id="86621-104">Questi termini sono specifici di Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="86621-104">These terms are distinctive of Direct3D 12.</span></span>

<dl> <dt>

<span data-ttu-id="86621-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**associazione**</span><span class="sxs-lookup"><span data-stu-id="86621-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="86621-106">Processo di connessione della memoria alla pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="86621-106">The process of attaching memory to the graphics pipeline.</span></span> <span data-ttu-id="86621-107">L'associazione di risorse, ad esempio, implica l'associazione di una risorsa, ad esempio una trama alla pipeline, da usare per il rendering di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="86621-107">Resource binding, for example, involves the binding of a resource such as a texture to the pipeline, for use in rendering an object.</span></span>

</dd> <dt>

<span data-ttu-id="86621-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**buffer**</span><span class="sxs-lookup"><span data-stu-id="86621-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**buffer**</span></span>
</dt> <dd>

<span data-ttu-id="86621-109">Tipo di risorsa D3D che è sinonimo di un'allocazione di memoria contigua.</span><span class="sxs-lookup"><span data-stu-id="86621-109">A type of D3D resource that is synonymous with a contiguous memory allocation.</span></span>

</dd> <dt>

<span data-ttu-id="86621-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**Bundle**</span><span class="sxs-lookup"><span data-stu-id="86621-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**bundle**</span></span>
</dt> <dd>

<span data-ttu-id="86621-111">Un buffer dei comandi che l'unità di elaborazione grafica (GPU) può eseguire solo direttamente tramite un *elenco di comandi diretto*.</span><span class="sxs-lookup"><span data-stu-id="86621-111">A command buffer that the graphics processing unit (GPU) can execute only directly via a *direct command list*.</span></span> <span data-ttu-id="86621-112">Un bundle eredita lo stato della GPU (ad eccezione dell' *oggetto stato della pipeline* attualmente impostato e della topologia primitiva).</span><span class="sxs-lookup"><span data-stu-id="86621-112">A bundle inherits all GPU state (except for the currently set *pipeline state object* and primitive topology).</span></span>

</dd> <dt>

<span data-ttu-id="86621-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**allocatore di comandi**</span><span class="sxs-lookup"><span data-stu-id="86621-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**command allocator**</span></span>
</dt> <dd>

<span data-ttu-id="86621-114">Allocazioni di memoria sottostanti in cui sono archiviati i comandi della GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-114">The underlying memory allocations in which GPU commands are stored.</span></span> <span data-ttu-id="86621-115">L'oggetto allocatore di comandi si applica sia agli *elenchi di comandi diretti* che ai *bundle*.</span><span class="sxs-lookup"><span data-stu-id="86621-115">The command allocator object applies to both *direct command lists* and *bundles*.</span></span>

</dd> <dt>

<span data-ttu-id="86621-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**Elenco comandi**</span><span class="sxs-lookup"><span data-stu-id="86621-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**command list**</span></span>
</dt> <dd>

<span data-ttu-id="86621-117">Un elenco di comandi corrisponde a un set di comandi eseguiti dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-117">A command list corresponds to a set of commands which the GPU executes.</span></span> <span data-ttu-id="86621-118">Questi includono comandi come per impostare lo stato, il progetto, la cancellazione e la copia.</span><span class="sxs-lookup"><span data-stu-id="86621-118">These include commands such as to set state, draw, clear, and copy.</span></span> <span data-ttu-id="86621-119">L'interfaccia dell'elenco di comandi D3D12 è significativamente diversa dall'interfaccia dell'elenco di comandi di D3D11.</span><span class="sxs-lookup"><span data-stu-id="86621-119">The D3D12 command list interface is significantly different than the D3D11 command list interface.</span></span> <span data-ttu-id="86621-120">L'interfaccia dell'elenco di comandi D3D12 contiene API simili alle API per il rendering del contesto del dispositivo D3D11.</span><span class="sxs-lookup"><span data-stu-id="86621-120">The D3D12 command list interface contains APIs similar to the D3D11 device context rendering APIs.</span></span>

<span data-ttu-id="86621-121">Un elenco di comandi di D3D12 non esegue il mapping delle risorse o annullare, modifica i mapping dei riquadri, ridimensiona i pool di sezioni, ottiene i dati della query e non invia mai in modo implicito comandi alla GPU per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="86621-121">A D3D12 command list does not map or unmap resources, change tile mappings, resize tile pools, get query data, nor does it ever implicitly submit commands to the GPU for execution.</span></span>

<span data-ttu-id="86621-122">A differenza dei contesti posticipati di D3D11, gli elenchi di comandi D3D12 supportano solo due livelli di riferimento indiretto.</span><span class="sxs-lookup"><span data-stu-id="86621-122">Unlike D3D11 deferred contexts, D3D12 command lists only support two levels of indirection.</span></span> <span data-ttu-id="86621-123">Un *elenco di comandi diretto* corrisponde a un buffer dei comandi che può essere eseguito dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-123">A *direct command list* corresponds to a command buffer which the GPU can execute.</span></span> <span data-ttu-id="86621-124">Un *bundle* può essere eseguito solo direttamente tramite un elenco di comandi diretto.</span><span class="sxs-lookup"><span data-stu-id="86621-124">A *bundle* can be executed only directly via a direct command list.</span></span>

<span data-ttu-id="86621-125">Un elenco di comandi diretto non eredita alcuno stato GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-125">A direct command list does not inherit any GPU state.</span></span> <span data-ttu-id="86621-126">Un bundle eredita lo stato della GPU (ad eccezione dell'oggetto stato della pipeline attualmente impostato e della topologia primitiva).</span><span class="sxs-lookup"><span data-stu-id="86621-126">A bundle inherits all GPU state (except for the currently set pipeline state object and primitive topology).</span></span>

<span data-ttu-id="86621-127">La memoria per un elenco di comandi viene impostata dall' *allocatore di comandi*.</span><span class="sxs-lookup"><span data-stu-id="86621-127">Memory for a command list is set by the *command allocator*.</span></span> <span data-ttu-id="86621-128">Lo scopo degli elenchi di comandi è che possono essere inviati a una GPU come una singola richiesta di rendering.</span><span class="sxs-lookup"><span data-stu-id="86621-128">The purpose of command lists is that they can be submitted to a GPU as a single rendering request.</span></span>

</dd> <dt>

<span data-ttu-id="86621-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**coda comandi**</span><span class="sxs-lookup"><span data-stu-id="86621-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**command queue**</span></span>
</dt> <dd>

<span data-ttu-id="86621-130">Coda degli *elenchi di comandi* eseguiti dalla GPU in successione.</span><span class="sxs-lookup"><span data-stu-id="86621-130">A queue of *command lists* that the GPU executes in succession.</span></span> <span data-ttu-id="86621-131">Le applicazioni devono inviare in modo esplicito *elenchi di comandi* a una coda di comandi per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="86621-131">Applications must explicitly submit *command lists* to a command queue for execution.</span></span> <span data-ttu-id="86621-132">Sono in genere disponibili tre code di comando: grafica 3D, calcolo e copia, corrispondenti alla pipeline grafica 3D, al motore di calcolo e a uno o più motori di copia nella GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-132">Typically there are three command queues: 3D graphics, compute and copy, corresponding to the 3D graphics pipeline, the compute engine, and one or more copy engines, on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="86621-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**rasterizzazione conservativa**</span><span class="sxs-lookup"><span data-stu-id="86621-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**conservative rasterization**</span></span>
</dt> <dd>

<span data-ttu-id="86621-134">La rasterizzazione conservativa è una modalità di funzionamento per la fase di rasterizzazione della pipeline grafica Direct3D.</span><span class="sxs-lookup"><span data-stu-id="86621-134">Conservative rasterization is a mode of operation for the rasterizer stage of the Direct3D graphics pipeline.</span></span> <span data-ttu-id="86621-135">Consente di disabilitare la rasterizzazione basata su campione standard e di rasterizzare invece un pixel coperto da qualsiasi quantità da una primitiva.</span><span class="sxs-lookup"><span data-stu-id="86621-135">It disables the standard sample-based rasterization, and will instead rasterize a pixel that is covered by any amount by a primitive.</span></span> <span data-ttu-id="86621-136">Una differenza importante è che, sebbene qualsiasi copertura produca un pixel rasterizzato, il code coverage non può essere caratterizzato dall'hardware, quindi il code coverage viene sempre visualizzato come binario per un pixel shader, ovvero completamente coperto o non coperto.</span><span class="sxs-lookup"><span data-stu-id="86621-136">One important distinction is that, while any coverage at all produces a rasterized pixel, that coverage cannot be characterized by the hardware, so coverage always appears binary to a pixel shader: either fully covered or not covered.</span></span> <span data-ttu-id="86621-137">Viene lasciata al codice pixel shader per determinare in modo analitico il coverage effettivo.</span><span class="sxs-lookup"><span data-stu-id="86621-137">It is left to the pixel shader code to analytically determine the actual coverage.</span></span>

<span data-ttu-id="86621-138">La rasterizzazione conservativa può essere utile per risolvere problemi di questo tipo, ad esempio collisioni e rilevamento di colpi, contenitori e abbattimento dell'occlusione, in cui il colore di un pixel è più determinato e i casi limite possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="86621-138">Conservative rasterization can help with such problems as collision and hit detection, binning, and occlusion culling, where the color of a pixel is more certain and edge cases can be eliminated.</span></span> <span data-ttu-id="86621-139">Vedere [rasterizzazione conservativa](conservative-rasterization.md).</span><span class="sxs-lookup"><span data-stu-id="86621-139">See [Conservative Rasterization](conservative-rasterization.md).</span></span>

</dd> <dt>

<span data-ttu-id="86621-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Constant Buffer View (CBV)**</span><span class="sxs-lookup"><span data-stu-id="86621-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Constant Buffer View (CBV)**</span></span>
</dt> <dd>

<span data-ttu-id="86621-141">I buffer costanti contengono dati costanti dello shader, ad esempio una visualizzazione della fotocamera, matrici di proiezione e matrici internazionali.</span><span class="sxs-lookup"><span data-stu-id="86621-141">Constant buffers contain shader constant data, such as a camera view, projection matrices, and world matrices.</span></span> <span data-ttu-id="86621-142">Una "visualizzazione buffer costante" è la visualizzazione specifica del formato del buffer, come illustrato dalla pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="86621-142">A "constant buffer view" is the format-specific view of the buffer as seen by the graphics pipeline.</span></span>

</dd> <dt>

<span data-ttu-id="86621-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**heap predefinito**</span><span class="sxs-lookup"><span data-stu-id="86621-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**default heap**</span></span>
</dt> <dd>

<span data-ttu-id="86621-144">Heap in modalità utente che è incentrato sul supporto di tipi di risorse GPU persistenti, incluse le risorse scritte da GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-144">A user-mode heap that is focused on supporting persistent GPU resource types, including GPU-written resources.</span></span>

</dd> <dt>

<span data-ttu-id="86621-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**descrittore**</span><span class="sxs-lookup"><span data-stu-id="86621-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="86621-146">I descrittori sono l'unità primaria di binding per una singola risorsa in D3D12.</span><span class="sxs-lookup"><span data-stu-id="86621-146">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span> <span data-ttu-id="86621-147">Un descrittore è un blocco di dati relativamente piccolo che descrive completamente un oggetto alla GPU, in un formato specifico della GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-147">A descriptor is a relatively small block of data that fully describes an object to the GPU, in a GPU specific format.</span></span> <span data-ttu-id="86621-148">Esistono molti tipi diversi di descrittori: le viste delle risorse dello shader (SRVs), le viste di accesso non ordinate (UAV), le viste del buffer costante (CBVs) e i Samplers sono alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="86621-148">There are many different types of descriptors: Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers are a few examples.</span></span>

</dd> <dt>

<span data-ttu-id="86621-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**heap descrittore**</span><span class="sxs-lookup"><span data-stu-id="86621-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**descriptor heap**</span></span>
</dt> <dd>

<span data-ttu-id="86621-150">Un heap del descrittore è una raccolta di allocazioni contigue di descrittori, un'allocazione per ogni descrittore.</span><span class="sxs-lookup"><span data-stu-id="86621-150">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span> <span data-ttu-id="86621-151">Il punto principale di un heap del descrittore consiste nell'includere la maggior parte dell'allocazione di memoria necessaria per archiviare le specifiche del descrittore dei tipi di oggetto a cui gli shader fanno riferimento per il maggior numero possibile di una finestra di rendering (idealmente un intero frame di rendering o più).</span><span class="sxs-lookup"><span data-stu-id="86621-151">The primary point of a descriptor heap is to encompass the bulk of memory allocation required for storing the descriptor specifications of object types that shaders reference for as large of a window of rendering as possible (ideally an entire frame of rendering or more).</span></span>

</dd> <dt>

<span data-ttu-id="86621-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**tabella descrittori**</span><span class="sxs-lookup"><span data-stu-id="86621-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**descriptor table**</span></span>
</dt> <dd>

<span data-ttu-id="86621-153">Una tabella descrittore è logicamente una matrice di descrittori.</span><span class="sxs-lookup"><span data-stu-id="86621-153">A descriptor table is logically an array of descriptors.</span></span> <span data-ttu-id="86621-154">Ogni tabella dei descrittori archivia i descrittori di uno o più tipi, tra cui SRVs, UAVe, CBVs e Samplers.</span><span class="sxs-lookup"><span data-stu-id="86621-154">Each descriptor table stores descriptors of one or more types, including SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="86621-155">Una tabella dei descrittori non è un'allocazione di memoria, ma è semplicemente un offset e una lunghezza in un heap descrittore.</span><span class="sxs-lookup"><span data-stu-id="86621-155">A descriptor table is not an allocation of memory, it is simply an offset and length into a descriptor heap.</span></span>

</dd> <dt>

<span data-ttu-id="86621-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**Elenco comandi diretti**</span><span class="sxs-lookup"><span data-stu-id="86621-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**direct command list**</span></span>
</dt> <dd>

<span data-ttu-id="86621-157">Buffer dei comandi che può essere eseguito dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-157">A command buffer that the GPU can execute.</span></span> <span data-ttu-id="86621-158">Un elenco di comandi diretto non eredita alcuno stato della GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-158">A direct command list doesn't inherit any GPU state.</span></span>

</dd> <dt>

<span data-ttu-id="86621-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**limite**</span><span class="sxs-lookup"><span data-stu-id="86621-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**fence**</span></span>
</dt> <dd>

<span data-ttu-id="86621-160">Meccanismo per sincronizzare la GPU e la CPU.</span><span class="sxs-lookup"><span data-stu-id="86621-160">A mechanism to synchronize the GPU and CPU.</span></span> <span data-ttu-id="86621-161">Sia la GPU che la CPU possono essere istruite ad attendere una recinzione, in attesa che l'altro processore si aggiorni.</span><span class="sxs-lookup"><span data-stu-id="86621-161">Both the GPU and CPU can be instructed to wait at a fence, waiting in effect for the other processor to catch up.</span></span> <span data-ttu-id="86621-162">Vedere [sincronizzazione multimotore](./user-mode-heap-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="86621-162">See [Multi-engine synchronization](./user-mode-heap-synchronization.md).</span></span>

</dd> <dt>

<span data-ttu-id="86621-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**rischio, rilevamento dei rischi**</span><span class="sxs-lookup"><span data-stu-id="86621-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**hazard, hazard tracking**</span></span>
</dt> <dd>

<span data-ttu-id="86621-164">Un rischio si verifica quando una risorsa è stata usata per uno scopo e l'app intende riutilizzarla per un altro scopo.</span><span class="sxs-lookup"><span data-stu-id="86621-164">A hazard occurs when a resource has been used for one purpose, and the app intends to reuse it for another purpose.</span></span> <span data-ttu-id="86621-165">Per usare di nuovo la risorsa, le cache intermedie dovranno essere scaricate o invalidate, i requisiti di compressione dovranno essere coerenti con il secondo utilizzo e la risorsa deve essere nello stato richiesto per evitare la lettura della risorsa dopo che è stata scritta e invalidata per lo scopo designato.</span><span class="sxs-lookup"><span data-stu-id="86621-165">In order to use the resource again, intermediate caches will need to be flushed or invalidated, compression requirements will need to be consistent with the second use, and the resource should be in the required state to avoid reading the resource after it has been written to and invalidated for the intended purpose.</span></span>

<span data-ttu-id="86621-166">Il processo di gestione delle risorse e di evitare questi problemi di sincronizzazione è noto come rilevamento dei rischi.</span><span class="sxs-lookup"><span data-stu-id="86621-166">The process of maintaining resources and avoiding these sync issues is known as hazard tracking.</span></span> <span data-ttu-id="86621-167">Se non si verifica alcun rischio da parte del driver, l'app è responsabile di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="86621-167">If there is no hazard tracking by the driver, then the app is responsible for this.</span></span> <span data-ttu-id="86621-168">Nella maggior parte delle versioni precedenti di DirectX, il rilevamento dei rischi è stato gestito dal driver.</span><span class="sxs-lookup"><span data-stu-id="86621-168">In most earlier versions of DirectX, hazard tracking was handled by the driver.</span></span> <span data-ttu-id="86621-169">Per migliorare le prestazioni, i metodi senza rilevamento dei rischi sono disponibili in DirectX 12.</span><span class="sxs-lookup"><span data-stu-id="86621-169">To improve performance, methods without hazard tracking are available in DirectX 12.</span></span>

</dd> <dt>

<span data-ttu-id="86621-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**High-Level Shader Language (HLSL)**</span><span class="sxs-lookup"><span data-stu-id="86621-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**High-Level Shader Language (HLSL)**</span></span>
</dt> <dd>

<span data-ttu-id="86621-171">Linguaggio del computer, simile ma distinto in molti modi da C, usato per scrivere il codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="86621-171">A computer language, similar but distinct in many ways from C, that is used to write shader code.</span></span> <span data-ttu-id="86621-172">Gli shader vertex, pixel, Geometry, COMPUTE, Domain e Hull vengono scritti con HLSL.</span><span class="sxs-lookup"><span data-stu-id="86621-172">Vertex, pixel, geometry, compute, domain, and hull shaders are all written using HLSL.</span></span> <span data-ttu-id="86621-173">Un compilatore converte l'origine HLSL in un formato binario per l'utilizzo della GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-173">A compiler converts the HLSL source into a binary format for the GPU to consume.</span></span>

</dd> <dt>

<span data-ttu-id="86621-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multimotore**</span><span class="sxs-lookup"><span data-stu-id="86621-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**</span></span>
</dt> <dd>

<span data-ttu-id="86621-175">Istanze e tipi diversi di motori in una singola GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-175">The different instances and types of engines in a single GPU.</span></span> <span data-ttu-id="86621-176">I tipi di motori includono: graphics, COMPUTE e Copy.</span><span class="sxs-lookup"><span data-stu-id="86621-176">The types of engines include: graphics, compute, and copy.</span></span>

</dd> <dt>

<span data-ttu-id="86621-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**</span><span class="sxs-lookup"><span data-stu-id="86621-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**</span></span>
</dt> <dd>

<span data-ttu-id="86621-178">Una configurazione hardware in cui è presente più di una scheda grafica.</span><span class="sxs-lookup"><span data-stu-id="86621-178">A hardware configuration where there is more than one graphics adapter.</span></span> <span data-ttu-id="86621-179">Gli adapter separati sono talvolta denominati nodi.</span><span class="sxs-lookup"><span data-stu-id="86621-179">The separate adapters are sometimes referred to as nodes.</span></span> <span data-ttu-id="86621-180">La presenza di più GPU consente di eseguire l'operazione di sincronizzazione con la CPU e, tra loro, in modo molto più complesso rispetto a una singola GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-180">Having multiple GPUs can make the task of synchronizing them with the CPU, and each other, considerably more complex than with a single GPU.</span></span>

</dd> <dt>

<span data-ttu-id="86621-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Oggetto di stato della pipeline (PSO)**</span><span class="sxs-lookup"><span data-stu-id="86621-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Pipeline State object (PSO)**</span></span>
</dt> <dd>

<span data-ttu-id="86621-182">Parte significativa dello stato della GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-182">A significant portion of the state of the GPU.</span></span> <span data-ttu-id="86621-183">Questo stato include tutti gli shader attualmente impostati e alcuni oggetti di stato a funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="86621-183">This state includes all currently set shaders and certain fixed-function state objects.</span></span> <span data-ttu-id="86621-184">L'unico modo per modificare gli stati contenuti nell'oggetto pipeline consiste nel modificare l'oggetto pipeline attualmente associato.</span><span class="sxs-lookup"><span data-stu-id="86621-184">The only way to change states contained within the pipeline object is to change the currently bound pipeline object.</span></span>

</dd> <dt>

<span data-ttu-id="86621-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predicazione**</span><span class="sxs-lookup"><span data-stu-id="86621-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predication**</span></span>
</dt> <dd>

<span data-ttu-id="86621-186">Predicazione è una funzionalità che consente alla GPU anziché alla CPU di determinare di non creare, copiare o inviare un oggetto.</span><span class="sxs-lookup"><span data-stu-id="86621-186">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy or dispatch an object.</span></span> <span data-ttu-id="86621-187">Se, ad esempio, un rettangolo di delimitazione di un oggetto è completamente nascosto da un altro oggetto o una prospettiva ha ridotto l'oggetto a un valore inferiore a quello di un pixel, potrebbe non essere necessario tentare di creare l'oggetto nascosto.</span><span class="sxs-lookup"><span data-stu-id="86621-187">For example, if a bounding box of an object is totally occluded by another object or perspective has reduced the object to less than the size of a pixel, there may be no point in attempting to draw the hidden object at all.</span></span> <span data-ttu-id="86621-188">Vedere [predicazione](predication.md).</span><span class="sxs-lookup"><span data-stu-id="86621-188">See [Predication](predication.md).</span></span>

</dd> <dt>

<span data-ttu-id="86621-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Visualizzazione ordine rasterizzatore (ROV)**</span><span class="sxs-lookup"><span data-stu-id="86621-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Rasterizer Order View (ROV)**</span></span>
</dt> <dd>

<span data-ttu-id="86621-190">Le pipeline di grafica standard possono avere problemi a comporre correttamente più trame che contengono la trasparenza.</span><span class="sxs-lookup"><span data-stu-id="86621-190">Standard graphics pipelines may have trouble correctly compositing together multiple textures that contain transparency.</span></span> <span data-ttu-id="86621-191">Oggetti quali recinzioni di trasmissione, fumo, incendi, vegetazione e vetro colorato usano la trasparenza per ottenere l'effetto desiderato.</span><span class="sxs-lookup"><span data-stu-id="86621-191">Objects such as wire fences, smoke, fire, vegetation, and colored glass use transparency to get the desired effect.</span></span> <span data-ttu-id="86621-192">Si verificano problemi quando più trame che contengono la trasparenza sono allineate l'una all'altra (fumo davanti a una recinzione davanti a una costruzione di vetro che contiene la vegetazione, come esempio).</span><span class="sxs-lookup"><span data-stu-id="86621-192">Problems arise when multiple textures that contain transparency are in line with each other (smoke in front of a fence in front of a glass building containing vegetation, as an example).</span></span> <span data-ttu-id="86621-193">Le visualizzazioni ordinate del rasterizzatore (ROV) consentono agli algoritmi OIT (Order Independent Transparency) sottostanti di usare le funzionalità dell'hardware per tentare di risolvere correttamente l'ordine di trasparenza.</span><span class="sxs-lookup"><span data-stu-id="86621-193">Rasterizer ordered views (ROVs) enable the underlying Order Independent Transparency (OIT) algorithms to use features of the hardware to try to resolve the transparency order correctly.</span></span> <span data-ttu-id="86621-194">La trasparenza viene gestita dal pixel shader.</span><span class="sxs-lookup"><span data-stu-id="86621-194">Transparency is handled by the pixel shader.</span></span>

<span data-ttu-id="86621-195">Le visualizzazioni ordinate del rasterizzatore (ROV) consentono pixel shader codice di contrassegnare Unordered Access View (UAV) binding con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV.</span><span class="sxs-lookup"><span data-stu-id="86621-195">Rasterizer Ordered Views (ROVs) allow pixel shader code to mark Unordered Access View (UAV) bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span>

</dd> <dt>

<span data-ttu-id="86621-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**heap readback**</span><span class="sxs-lookup"><span data-stu-id="86621-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**readback heap**</span></span>
</dt> <dd>

<span data-ttu-id="86621-197">Heap in modalità utente focalizzato sul trasferimento dei dati dalla GPU alla CPU.</span><span class="sxs-lookup"><span data-stu-id="86621-197">A user-mode heap that is focused on data transfer from the GPU back to the CPU.</span></span>

</dd> <dt>

<span data-ttu-id="86621-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**risorse**</span><span class="sxs-lookup"><span data-stu-id="86621-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**resource**</span></span>
</dt> <dd>

<span data-ttu-id="86621-199">Entità che fornisce i dati alla pipeline e definisce gli elementi di cui viene eseguito il rendering durante la scena.</span><span class="sxs-lookup"><span data-stu-id="86621-199">An entity that provides data to the pipeline and defines what is rendered during your scene.</span></span> <span data-ttu-id="86621-200">Le risorse possono essere caricate dal supporto del gioco o create dinamicamente in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="86621-200">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="86621-201">In genere, le risorse includono i dati di trama, i dati dei vertici e gli shader.</span><span class="sxs-lookup"><span data-stu-id="86621-201">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="86621-202">La maggior parte delle applicazioni Direct3D crea ed Elimina in modo estensivo le risorse per tutta la loro durata.</span><span class="sxs-lookup"><span data-stu-id="86621-202">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span>

</dd> <dt>

<span data-ttu-id="86621-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**barriera delle risorse**</span><span class="sxs-lookup"><span data-stu-id="86621-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**resource barrier**</span></span>
</dt> <dd>

<span data-ttu-id="86621-204">Una barriera delle risorse notifica al driver che la sincronizzazione di più accessi a una singola risorsa potrebbe essere obbligatoria, ad esempio la lettura e la scrittura nella stessa trama.</span><span class="sxs-lookup"><span data-stu-id="86621-204">A resource barrier notifies the driver that synchronization of multiple accesses to a single resource may be required, for example, reading and writing to the same texture.</span></span>

</dd> <dt>

<span data-ttu-id="86621-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**associazione di risorse**</span><span class="sxs-lookup"><span data-stu-id="86621-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**resource binding**</span></span>
</dt> <dd>

<span data-ttu-id="86621-206">L'associazione di risorse è il processo di collegamento delle risorse (trame, buffer dei vertici, buffer di indice e così via) alla pipeline grafica, consentendo agli shader della pipeline di elaborare la risorsa corretta.</span><span class="sxs-lookup"><span data-stu-id="86621-206">Resource binding is the process of linking resources (textures, vertex buffers, index buffers, and so on), to the graphics pipeline, enabling the shaders of the pipeline to process the correct resource.</span></span>

</dd> <dt>

<span data-ttu-id="86621-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**heap delle risorse**</span><span class="sxs-lookup"><span data-stu-id="86621-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**resource heaps**</span></span>
</dt> <dd>

<span data-ttu-id="86621-208">Heap risorse è un termine generico per gli heap che sono buffer di memoria accantonati per mantenere le risorse non appena vengono trasferiti da e verso la GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-208">Resource heaps is a generic term for the heaps that are memory buffers set aside to hold resources as they are transferred to and from the GPU.</span></span> <span data-ttu-id="86621-209">Un trasferimento alla GPU richiede un heap di caricamento, dalla GPU alla CPU richiede un heap readback e un heap permanente per la GPU per la manutenzione di più frame di rendering viene definito heap predefinito.</span><span class="sxs-lookup"><span data-stu-id="86621-209">A transfer to the GPU requires an Upload Heap, from the GPU to the CPU requires a Readback Heap, and a persistent heap for the GPU to maintain over multiple rendering frames is called a Default Heap.</span></span>

</dd> <dt>

<span data-ttu-id="86621-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**firma radice**</span><span class="sxs-lookup"><span data-stu-id="86621-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**root signature**</span></span>
</dt> <dd>

<span data-ttu-id="86621-211">Le firme radice definiscono tutte le risorse che devono essere associate alle pipeline di calcolo o di grafica.</span><span class="sxs-lookup"><span data-stu-id="86621-211">Root signatures define all the resources that are to be bound to the graphics, or compute, pipelines.</span></span> <span data-ttu-id="86621-212">Una firma radice viene configurata tramite l'app e collega gli elenchi di comandi alle risorse richieste dagli shader in genere, sono presenti una grafica e una firma radice di calcolo per ogni app.</span><span class="sxs-lookup"><span data-stu-id="86621-212">A root signature is configured by the app and links command lists to the resources that the shaders require Typically, there is one graphics and one compute root signature per app.</span></span>

</dd> <dt>

<span data-ttu-id="86621-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**campionatore**</span><span class="sxs-lookup"><span data-stu-id="86621-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**sampler**</span></span>
</dt> <dd>

<span data-ttu-id="86621-214">Un campionatore è un codice che legge da una trama.</span><span class="sxs-lookup"><span data-stu-id="86621-214">A sampler is code that reads from a texture.</span></span>

</dd> <dt>

<span data-ttu-id="86621-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Shader Resource View (SRV)**</span><span class="sxs-lookup"><span data-stu-id="86621-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Shader Resource View (SRV)**</span></span>
</dt> <dd>

<span data-ttu-id="86621-216">Modo specifico del formato per esaminare i dati in una risorsa shader, ad esempio una trama.</span><span class="sxs-lookup"><span data-stu-id="86621-216">A format-specific way to look at the data in a shader resource, such as a texture.</span></span>

</dd> <dt>

<span data-ttu-id="86621-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**heap statico**</span><span class="sxs-lookup"><span data-stu-id="86621-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**static heap**</span></span>
</dt> <dd>

<span data-ttu-id="86621-218">Heap in modalità utente incentrato su più risorse di sola lettura GPU che in genere vengono utilizzate contemporaneamente e non vengono modificate di frequente.</span><span class="sxs-lookup"><span data-stu-id="86621-218">A user-mode heap that is focused on multiple GPU-read-only resources that are typically used at the same time and are not changed frequently.</span></span>

</dd> <dt>

<span data-ttu-id="86621-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**Scambia catena**</span><span class="sxs-lookup"><span data-stu-id="86621-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="86621-220">Le catene di scambio controllano la rotazione del buffer indietro, formando la base dell'animazione grafica.</span><span class="sxs-lookup"><span data-stu-id="86621-220">Swap chains control the back buffer rotation, forming the basis of graphics animation.</span></span> <span data-ttu-id="86621-221">Le catene di scambio vengono gestite dal set di API di basso livello DXGI (vedere [Panoramica di DXGI](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).</span><span class="sxs-lookup"><span data-stu-id="86621-221">Swap chains are handled by the low level API set DXGI (see [DXGI Overview](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).</span></span>

</dd> <dt>

<span data-ttu-id="86621-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**</span><span class="sxs-lookup"><span data-stu-id="86621-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**</span></span>
</dt> <dd>

<span data-ttu-id="86621-223">Una tecnica per l'individuazione dei dati multidimensionali in memoria, in modo che i dati di dimensionalità vicina tendano a disporre di indirizzi vicini.</span><span class="sxs-lookup"><span data-stu-id="86621-223">A technique of locating multidimensional data in memory such that data of nearby dimensionality tends to have nearby addresses.</span></span> <span data-ttu-id="86621-224">In particolare, tutti i dati di una riga non si trovano in modo contiguo prima dei dati della riga successiva.</span><span class="sxs-lookup"><span data-stu-id="86621-224">In particular, all the data for one row is not located contiguously before the data for the next row.</span></span> <span data-ttu-id="86621-225">Un "swizzle con parametri" descrive un modo standardizzato per descrivere i modelli di Swizzle.</span><span class="sxs-lookup"><span data-stu-id="86621-225">A "Parameterized Swizzle" describes a standardized way to describe swizzle patterns.</span></span>

</dd> <dt>

<span data-ttu-id="86621-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**trama**</span><span class="sxs-lookup"><span data-stu-id="86621-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**texture**</span></span>
</dt> <dd>

<span data-ttu-id="86621-227">Tipo di risorsa D3D che è multidimensionale e ha un layout di memoria ottimizzato per l'accesso multidimensionale dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-227">A type of D3D resource that is multi-dimensional and has a memory layout that is optimized for multi-dimensional access from the GPU.</span></span> <span data-ttu-id="86621-228">Le trame contengono spesso l'immagine non elaborata necessaria per il rendering su una superficie, prima che l'illuminazione e la fusione avvengano, ma possono contenere altre forme di dati, ad esempio sfumature di colore e colori di riferimento.</span><span class="sxs-lookup"><span data-stu-id="86621-228">Textures often contain the raw image required to render onto a surface, before lighting and blending takes place, but can contain other forms of data such as color gradients and reference colors.</span></span> <span data-ttu-id="86621-229">Direct3D 12 supporta una, due e tre trame dimensionali.</span><span class="sxs-lookup"><span data-stu-id="86621-229">Direct3D 12 supports one, two, and three dimensional textures.</span></span>

</dd> <dt>

<span data-ttu-id="86621-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**piastrelle**</span><span class="sxs-lookup"><span data-stu-id="86621-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**tile**</span></span>
</dt> <dd>

<span data-ttu-id="86621-231">Una pagina di memoria video, simile a una pagina CPU/sistema di memoria.</span><span class="sxs-lookup"><span data-stu-id="86621-231">A page of video memory, similar to a CPU/System page of memory.</span></span> <span data-ttu-id="86621-232">La notazione dei riquadri consente di distinguere il sottosistema di memoria virtuale GPU dal sottosistema di memoria virtuale della CPU.</span><span class="sxs-lookup"><span data-stu-id="86621-232">The tile notation helps to distinguish the GPU virtual memory subsystem from the CPU virtual memory subsystem.</span></span> <span data-ttu-id="86621-233">Le GPU forniscono funzionalità di memoria virtuale analoghe alla memoria virtuale di sistema.</span><span class="sxs-lookup"><span data-stu-id="86621-233">GPUs provide similar virtual memory capabilities as system virtual memory.</span></span> <span data-ttu-id="86621-234">Alcune GPU hanno funzionalità di memoria virtuale condivise, che consentono la condivisione di alcune pagine del sottosistema di memoria virtuale con CPU e GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-234">Some GPUs have shared virtual memory capabilities, which allow for the sharing of some pages of the virtual memory subsystem with both the CPU and GPU.</span></span>

</dd> <dt>

<span data-ttu-id="86621-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**risorse affiancate**</span><span class="sxs-lookup"><span data-stu-id="86621-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="86621-236">Le risorse affiancate sono necessarie, in modo che meno memoria GPU venga sprecata per archiviare le aree di superficie che l'applicazione sa non sarà accessibile e l'hardware possa comprendere come filtrare tra i riquadri adiacenti.</span><span class="sxs-lookup"><span data-stu-id="86621-236">Tiled resources are needed so less GPU memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span> <span data-ttu-id="86621-237">Le risorse affiancate sono risorse logiche di grandi dimensioni, ma richiedono piccole quantità di memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="86621-237">Tiled resources are large logical resources, but requiring small amounts of physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="86621-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Unordered Access View (UAV)**</span><span class="sxs-lookup"><span data-stu-id="86621-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Unordered Access View (UAV)**</span></span>
</dt> <dd>

<span data-ttu-id="86621-239">Una visualizzazione di accesso non ordinato in una risorsa (che include buffer, trame e matrici di trame senza campionamento multiplo) consente l'accesso in lettura/scrittura non ordinato da più thread.</span><span class="sxs-lookup"><span data-stu-id="86621-239">An unordered access view into a resource (which includes buffers, textures, and texture arrays - without multi-sampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="86621-240">Questo significa che questo tipo di risorsa può essere letto/scritto simultaneamente da più thread senza generare conflitti di memoria.</span><span class="sxs-lookup"><span data-stu-id="86621-240">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span>

</dd> <dt>

<span data-ttu-id="86621-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**carica heap**</span><span class="sxs-lookup"><span data-stu-id="86621-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**upload heap**</span></span>
</dt> <dd>

<span data-ttu-id="86621-242">Heap in modalità utente incentrato sul trasferimento dei dati dalla CPU alla GPU.</span><span class="sxs-lookup"><span data-stu-id="86621-242">A user-mode heap that is focused on data transfer from the CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="86621-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**heap in modalità utente**</span><span class="sxs-lookup"><span data-stu-id="86621-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**user-mode heap**</span></span>
</dt> <dd>

<span data-ttu-id="86621-244">Raccolta di allocazioni di memoria grandi e contigue riciclate senza la consapevolezza di alcun componente kernel: i metodi di allocazione e distruzione non chiamano i metodi di allocazione e distruzione del kernel durante lo stato stazionario.</span><span class="sxs-lookup"><span data-stu-id="86621-244">A collection of large, contiguous memory allocations that are recycled without any kernel component's awareness: the allocation and destruction methods do not call kernel allocation and destruction methods during steady state.</span></span> <span data-ttu-id="86621-245">Gli heap upload, readback e default sono varianti degli heap in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="86621-245">Upload, Readback, and Default heaps are variants of user mode heaps.</span></span>

</dd> <dt>

<span data-ttu-id="86621-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**risorse affiancate al volume**</span><span class="sxs-lookup"><span data-stu-id="86621-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**volume tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="86621-247">[Risorse affiancate](/windows)tridimensionali.</span><span class="sxs-lookup"><span data-stu-id="86621-247">Three-dimensional [tiled resources](/windows).</span></span>

</dd> </dl>

 

 