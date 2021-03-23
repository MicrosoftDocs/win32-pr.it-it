---
title: Convalida basata su GPU e livello di debug Direct3D 12
description: Questo argomento descrive come usare al meglio il livello di debug Direct3D 12. La convalida basata su GPU (GBV) consente scenari di convalida nella sequenza temporale GPU che non sono possibili durante le chiamate API sulla CPU.
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 3160df3faf994df2abf9cf878088e84564bb5fe1
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548875"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a><span data-ttu-id="b19df-104">Convalida basata su GPU e livello di debug Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b19df-104">GPU-based validation and the Direct3D 12 Debug Layer</span></span>

<span data-ttu-id="b19df-105">Questo argomento descrive come usare al meglio il livello di debug Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="b19df-105">This topic describes how to make best use of the Direct3D 12 Debug Layer.</span></span> <span data-ttu-id="b19df-106">La convalida basata su GPU (GBV) consente scenari di convalida nella sequenza temporale GPU che non sono possibili durante le chiamate API sulla CPU.</span><span class="sxs-lookup"><span data-stu-id="b19df-106">GPU-based validation (GBV) enables validation scenarios on the GPU timeline that are not possible during API calls on the CPU.</span></span> <span data-ttu-id="b19df-107">GBV è disponibile a partire da strumenti di grafica per l'aggiornamento dell'anniversario di Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b19df-107">GBV is available starting with the Graphics Tools for Windows 10 Anniversary Update.</span></span>

## <a name="purpose-of-gpu-based-validation"></a><span data-ttu-id="b19df-108">Scopo della convalida basata su GPU</span><span class="sxs-lookup"><span data-stu-id="b19df-108">Purpose of GPU-based validation</span></span>

<span data-ttu-id="b19df-109">La convalida basata su GPU consente di identificare gli errori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b19df-109">GPU-based validation helps to identify the following errors:</span></span>

- <span data-ttu-id="b19df-110">Utilizzo di descrittori non inizializzati o incompatibili in uno shader.</span><span class="sxs-lookup"><span data-stu-id="b19df-110">Use of uninitialized or incompatible descriptors in a shader.</span></span>
- <span data-ttu-id="b19df-111">Uso di descrittori che fanno riferimento a risorse eliminate in uno shader.</span><span class="sxs-lookup"><span data-stu-id="b19df-111">Use of descriptors referencing deleted Resources in a shader.</span></span>
- <span data-ttu-id="b19df-112">Convalida degli Stati delle risorse promossi e del decadimento dello stato delle risorse.</span><span class="sxs-lookup"><span data-stu-id="b19df-112">Validation of promoted resource states and resource state decay.</span></span>
- <span data-ttu-id="b19df-113">Indicizzazione oltre la fine dell'heap del descrittore in uno shader.</span><span class="sxs-lookup"><span data-stu-id="b19df-113">Indexing beyond the end of the descriptor heap in a shader.</span></span>
- <span data-ttu-id="b19df-114">Gli accessi allo shader di risorse in stato incompatibile.</span><span class="sxs-lookup"><span data-stu-id="b19df-114">Shader accesses of resources in incompatible state.</span></span>
- <span data-ttu-id="b19df-115">Utilizzo di campioni non inizializzati o incompatibili in uno shader.</span><span class="sxs-lookup"><span data-stu-id="b19df-115">Use of uninitialized or incompatible Samplers in a shader.</span></span>

<span data-ttu-id="b19df-116">GBV funziona creando shader con patch con la convalida aggiunta direttamente allo shader.</span><span class="sxs-lookup"><span data-stu-id="b19df-116">GBV works by creating patched shaders that have validation added directly to the shader.</span></span> <span data-ttu-id="b19df-117">Gli shader con patch controllano gli argomenti radice e le risorse a cui si accede durante l'esecuzione dello shader e segnalano gli errori a un buffer del log.</span><span class="sxs-lookup"><span data-stu-id="b19df-117">The patched shaders inspect root arguments and resources accessed during shader execution and report errors to a log buffer.</span></span> <span data-ttu-id="b19df-118">GBV inserisce anche operazioni aggiuntive e invia chiamate agli elenchi di comandi dell'applicazione per convalidare e tenere traccia delle modifiche apportate allo stato delle risorse imposte dall'elenco dei comandi nella sequenza temporale GPU.</span><span class="sxs-lookup"><span data-stu-id="b19df-118">GBV also injects extra operations and Dispatch calls into the application command lists to validate and track changes to resource state imposed by the command list on the GPU-timeline.</span></span>

<span data-ttu-id="b19df-119">Poiché GBV richiede la possibilità di eseguire shader, gli elenchi di comandi di copia vengono emulati da un elenco di comandi di calcolo.</span><span class="sxs-lookup"><span data-stu-id="b19df-119">Because GBV requires the ability to execute shaders, COPY command lists are emulated by a COMPUTE command list.</span></span> <span data-ttu-id="b19df-120">Questo può potenzialmente modificare il modo in cui l'hardware esegue le copie anche se il risultato finale non deve essere modificato.</span><span class="sxs-lookup"><span data-stu-id="b19df-120">This may potentially change how hardware performs copies though the end result should not be changed.</span></span> <span data-ttu-id="b19df-121">L'applicazione continuerà a percepire gli elenchi di comandi di copia e il livello di debug li convaliderà come tali.</span><span class="sxs-lookup"><span data-stu-id="b19df-121">The application will still perceive these are COPY command lists and the debug layer will validate them as such.</span></span>

## <a name="turning-on-gpu-based-validation"></a><span data-ttu-id="b19df-122">Attivazione della convalida basata su GPU</span><span class="sxs-lookup"><span data-stu-id="b19df-122">Turning on GPU-based validation</span></span>

<span data-ttu-id="b19df-123">GBV può essere forzata usando il pannello di controllo DirectX (DXCPL) forzando il livello di debug Direct3D 12 e forzando la convalida basata su GPU (nuova scheda nel pannello di controllo).</span><span class="sxs-lookup"><span data-stu-id="b19df-123">GBV can be forced on using the DirectX Control Panel (DXCPL) by forcing on the Direct3D 12 Debug Layer and additionally forcing on GPU-based validation (new tab in the control panel).</span></span> <span data-ttu-id="b19df-124">Una volta abilitata, GBV rimarrà abilitato fino al rilascio del dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="b19df-124">Once enabled, GBV will remain enabled until the Direct3D 12 device is released.</span></span> <span data-ttu-id="b19df-125">In alternativa, è possibile abilitare GBV a livello di codice prima di creare il dispositivo Direct3D 12:</span><span class="sxs-lookup"><span data-stu-id="b19df-125">Alternatively, GBV can be enabled programmatically prior to creating the Direct3D 12 Device:</span></span>

```cpp
void EnableShaderBasedValidation()
{
    CComPtr<ID3D12Debug> spDebugController0;
    CComPtr<ID3D12Debug1> spDebugController1;
    VERIFY(D3D12GetDebugInterface(IID_PPV_ARGS(&spDebugController0)));
    VERIFY(spDebugController0->QueryInterface(IID_PPV_ARGS(&spDebugController1)));
    spDebugController1->SetEnableGPUBasedValidation(true);
}
```

## <a name="recommended-usage"></a><span data-ttu-id="b19df-126">Uso consigliato</span><span class="sxs-lookup"><span data-stu-id="b19df-126">Recommended usage</span></span>

<span data-ttu-id="b19df-127">In genere, è consigliabile eseguire il codice con il livello di debug abilitato per la maggior parte del tempo.</span><span class="sxs-lookup"><span data-stu-id="b19df-127">Generally, you should run your code with the debug layer enabled most of the time.</span></span> <span data-ttu-id="b19df-128">Tuttavia, GBV può rallentare molto l'attività.</span><span class="sxs-lookup"><span data-stu-id="b19df-128">However, GBV can slow things down a lot.</span></span> <span data-ttu-id="b19df-129">Gli sviluppatori possono prendere in considerazione l'abilitazione di GBV con set di dati più piccoli (ad esempio, demo del motore o piccoli livelli di gioco con meno impostazioni e risorse di PSO) o durante l'introduzione anticipata dell'applicazione per ridurre i problemi di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b19df-129">Developers may consider enabling GBV with smaller data sets (for example, engine demos or small game levels with fewer PSO’s and resources) or during early application bring-up to reduce performance problems.</span></span> <span data-ttu-id="b19df-130">Con contenuto di dimensioni maggiori, è consigliabile attivare GBV in uno o due computer di test in un test notturno superato.</span><span class="sxs-lookup"><span data-stu-id="b19df-130">With larger content consider turning on GBV on one or two test machines in a nightly test pass.</span></span>

## <a name="debug-output"></a><span data-ttu-id="b19df-131">Output di debug</span><span class="sxs-lookup"><span data-stu-id="b19df-131">Debug output</span></span>

<span data-ttu-id="b19df-132">GBV produce l'output di debug dopo che una chiamata a [**oggetti executecommandlist**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) completa l'esecuzione sulla GPU.</span><span class="sxs-lookup"><span data-stu-id="b19df-132">GBV produces debug output after a call to [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) completes execution on the GPU.</span></span> <span data-ttu-id="b19df-133">Poiché si trova nella sequenza temporale GPU, l'output di debug può essere asincrono con altre convalide della sequenza temporale della CPU.</span><span class="sxs-lookup"><span data-stu-id="b19df-133">Since this is on the GPU-timeline the debug output may be asynchronous with other CPU-timeline validation.</span></span> <span data-ttu-id="b19df-134">Gli sviluppatori di applicazioni possono voler inserire il proprio Wait-after-Execute per sincronizzare l'output di debug.</span><span class="sxs-lookup"><span data-stu-id="b19df-134">Application developers may want to inject their own wait-after-execute to synchronize debug output.</span></span>

<span data-ttu-id="b19df-135">L'output di GBV identifica la posizione in cui si è verificato un errore in uno shader, insieme al conteggio e alle identità correnti degli oggetti correlati, ad esempio elenco dei comandi, coda, PSO e così via.</span><span class="sxs-lookup"><span data-stu-id="b19df-135">GBV output identifies where in a shader an error occurred, along with the current draw/dispatch count and identities of related objects (e.g. command list, queue, PSO, etc).</span></span>

## <a name="example-debug-message"></a><span data-ttu-id="b19df-136">Messaggio di debug di esempio</span><span class="sxs-lookup"><span data-stu-id="b19df-136">Example debug message</span></span>

<span data-ttu-id="b19df-137">Il messaggio di errore seguente indica che è stato eseguito l'accesso a una risorsa denominata "buffer del colore principale" in uno shader come risorsa dello shader, ma che era nello stato di accesso non ordinato quando lo shader è stato eseguito nella GPU.</span><span class="sxs-lookup"><span data-stu-id="b19df-137">The following error message indicates that a resource named “Main Color Buffer” was accessed in a shader as a shader resource but was in the unordered access state when the shader ran on the GPU.</span></span> <span data-ttu-id="b19df-138">Vengono fornite anche informazioni aggiuntive, ad esempio la posizione nell'origine dello shader, il nome dell'elenco di comandi e il conteggio di disegni (indice di estrazione) e i nomi degli oggetti dell'interfaccia D3D correlati.</span><span class="sxs-lookup"><span data-stu-id="b19df-138">Additional information, such as the location in the shader source, the name of the command list and the Draw count (Draw Index), and the names of related D3D interface objects are also provided.</span></span>

```cmd
D3D12 ERROR: Incompatible resource state: Resource: 0x0000016F61A6EA80:'Main Color Buffer', 
Subresource Index: [0], 
Descriptor heap index: [0], 
Binding Type In Descriptor: SRV, 
Resource State: D3D12_RESOURCE_STATE_UNORDERED_ACCESS(0x8), 
Shader Stage: PIXEL, 
Root Parameter Index: [0], 
Draw Index: [0], 
Shader Code: E:\FileShare\MiniEngine_GitHub_160128\MiniEngine_GitHub\Core\Shaders\SharpeningUpsamplePS.hlsl(37,2-59), 
Asm Instruction Range: [0x138-0x16b], 
Asm Operand Index: [3], 
Command List: 0x0000016F6F75F740:'CommandList', SRV/UAV/CBV Descriptor Heap: 0x0000016F6F76F280:'Unnamed ID3D12DescriptorHeap Object', 
Sampler Descriptor Heap: <not set>, 
Pipeline State: 0x0000016F572C89F0:'Unnamed ID3D12PipelineState Object',  
[ EXECUTION ERROR #942: GPU_BASED_VALIDATION_INCOMPATIBLE_RESOURCE_STATE]
```

## <a name="debug-layer-apis"></a><span data-ttu-id="b19df-139">API del livello di debug</span><span class="sxs-lookup"><span data-stu-id="b19df-139">Debug Layer APIs</span></span>

<span data-ttu-id="b19df-140">Per abilitare il livello di debug, chiamare [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).</span><span class="sxs-lookup"><span data-stu-id="b19df-140">To enable the debug layer, call [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).</span></span>

<span data-ttu-id="b19df-141">Per abilitare la convalida basata su GPU, chiamare [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)e fare riferimento ai metodi delle interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="b19df-141">To enable GPU-based validation, call [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation), and refer to the methods of the following interfaces:</span></span>

- [<span data-ttu-id="b19df-142">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="b19df-142">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [<span data-ttu-id="b19df-143">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="b19df-143">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [<span data-ttu-id="b19df-144">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="b19df-144">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

<span data-ttu-id="b19df-145">Vedere le enumerazioni e le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="b19df-145">Refer to the following enumerations and structures:</span></span>

- [<span data-ttu-id="b19df-146">**\_Tipo di \_ parametro dell'elenco di comandi di debug D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b19df-146">**D3D12\_DEBUG\_COMMAND\_LIST\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [<span data-ttu-id="b19df-147">**\_Tipo di \_ parametro del dispositivo di debug D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b19df-147">**D3D12\_DEBUG\_DEVICE\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [<span data-ttu-id="b19df-148">**D3D12 \_ \_ \_ \_ \_ \_ creare flag per lo stato della pipeline di convalida basata \_ sulla GPU**</span><span class="sxs-lookup"><span data-stu-id="b19df-148">**D3D12\_GPU\_BASED\_VALIDATION\_PIPELINE\_STATE\_CREATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [<span data-ttu-id="b19df-149">**\_ \_ \_ \_ \_ Modalità patch shader di convalida basata su \_ GPU D3D12**</span><span class="sxs-lookup"><span data-stu-id="b19df-149">**D3D12\_GPU\_BASED\_VALIDATION\_SHADER\_PATCH\_MODE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [<span data-ttu-id="b19df-150">**\_Impostazioni di \_ \_ \_ \_ convalida basate su GPU \_ per l'elenco dei \_ comandi di debug D3D12**</span><span class="sxs-lookup"><span data-stu-id="b19df-150">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [<span data-ttu-id="b19df-151">**\_Impostazioni di \_ \_ \_ convalida basate su \_ GPU \_ del dispositivo debug D3D12**</span><span class="sxs-lookup"><span data-stu-id="b19df-151">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a><span data-ttu-id="b19df-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b19df-152">Related topics</span></span>

* [<span data-ttu-id="b19df-153">Informazioni sul livello di debug Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b19df-153">Understanding the Direct3D 12 Debug Layer</span></span>](understanding-the-d3d12-debug-layer.md)
