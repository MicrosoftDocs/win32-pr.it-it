---
title: Livello di funzionalità di Direct3D 12 Core 1.0
description: Il livello di funzionalità di base 1,0 è un subset del set completo di funzionalità di Direct3D 12.
ms.topic: article
ms.date: 11/05/2019
ms.openlocfilehash: 42d13b71c516e55ecce378cf9cb415c45e520ba9
ms.sourcegitcommit: bba068130240d16de8a3f3468b7cd72b2cd760f6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/03/2020
ms.locfileid: "106299548"
---
# <a name="the-direct3d-12-core-10-feature-level"></a><span data-ttu-id="309b6-103">Livello di funzionalità di Direct3D 12 Core 1.0</span><span class="sxs-lookup"><span data-stu-id="309b6-103">The Direct3D 12 Core 1.0 Feature Level</span></span>

<span data-ttu-id="309b6-104">Il livello di funzionalità di base 1,0 è un subset del set completo di funzionalità di Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="309b6-104">The Core 1.0 Feature Level is a subset of the full Direct3D 12 feature set.</span></span> <span data-ttu-id="309b6-105">Il livello di funzionalità di base 1,0 può essere esposto da una categoria di dispositivi noti come *dispositivi di sola elaborazione*.</span><span class="sxs-lookup"><span data-stu-id="309b6-105">Core 1.0 Feature Level can be exposed by a category of devices known as *compute-only devices*.</span></span> <span data-ttu-id="309b6-106">Il modello di driver globale per i dispositivi solo calcolo è Microsoft Compute Driver Model (MCDM).</span><span class="sxs-lookup"><span data-stu-id="309b6-106">The overall driver model for compute-only devices is the Microsoft Compute Driver Model (MCDM).</span></span> <span data-ttu-id="309b6-107">MCDM è un peer con scalabilità orizzontale del modello di driver di dispositivo Windows (WDDM), che ha un ambito più ampio.</span><span class="sxs-lookup"><span data-stu-id="309b6-107">MCDM is a scaled-down peer of the Windows Device Driver Model (WDDM), which has a larger scope.</span></span>

<span data-ttu-id="309b6-108">Un dispositivo che supporta *solo* le funzionalità all'interno di un livello di funzionalità di base è noto come *dispositivo principale*.</span><span class="sxs-lookup"><span data-stu-id="309b6-108">A device that supports *only* the features within a Core Feature Level is known as a *Core device*.</span></span>

> [!NOTE]
> <span data-ttu-id="309b6-109">Il dispositivo di *solo calcolo*, il dispositivo *MCDM*, il dispositivo *principale a livello di funzionalità* e il *dispositivo principale* significano tutti la stessa cosa.</span><span class="sxs-lookup"><span data-stu-id="309b6-109">*Compute-only device*, *MCDM device*, *Core Feature Level device*, and *Core device* all mean the same thing.</span></span> <span data-ttu-id="309b6-110">Per semplicità, è preferibile usare il *dispositivo principale* .</span><span class="sxs-lookup"><span data-stu-id="309b6-110">We'll prefer *Core device* for simplicity.</span></span>

## <a name="creating-a-core-device"></a><span data-ttu-id="309b6-111">Creazione di un dispositivo principale</span><span class="sxs-lookup"><span data-stu-id="309b6-111">Creating a Core device</span></span>

<span data-ttu-id="309b6-112">In generale, per creare un dispositivo Direct3D 12, chiamare la funzione [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) e specificare un livello di funzionalità minimo.</span><span class="sxs-lookup"><span data-stu-id="309b6-112">In general, to create a Direct3D 12 device, you call the [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) function, and specify a minimum feature level.</span></span>

<span data-ttu-id="309b6-113">Se si specifica un livello di funzionalità da 9 a 12, il dispositivo restituito è un dispositivo ricco di funzionalità, ad esempio una GPU tradizionale (che supporta un superset della funzionalità di un dispositivo principale).</span><span class="sxs-lookup"><span data-stu-id="309b6-113">If you specify a feature level of 9 through 12, then the device that's returned is a feature-rich device, such as a traditional GPU (which supports a superset of the functionality of a Core device).</span></span> <span data-ttu-id="309b6-114">Un dispositivo Core non viene mai restituito per tale intervallo di livelli di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="309b6-114">A Core device is never returned for that range of feature levels.</span></span>

<span data-ttu-id="309b6-115">D'altra parte, se si specifica un livello di funzionalità di base (ad esempio [**D3D_FEATURE_LEVEL::D 3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), il dispositivo restituito potrebbe essere ricco di funzionalità o potrebbe essere un dispositivo principale.</span><span class="sxs-lookup"><span data-stu-id="309b6-115">On the other hand, if you specify a Core feature level (for example, [**D3D_FEATURE_LEVEL::D3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), then the device that's returned could be feature-rich, or it could be a Core device.</span></span>

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

<span data-ttu-id="309b6-116">Se si specifica un `_CORE` livello di funzionalità, il livello di runtime/debug convalida che le funzionalità usate dall'applicazione sono consentite da tale `_CORE` livello di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="309b6-116">If you specify a `_CORE` feature level, then the runtime/debug layer validates that the features your application uses are allowed by that `_CORE` feature level.</span></span> <span data-ttu-id="309b6-117">Tale set di funzionalità viene definito più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="309b6-117">That set of features is defined later in this topic.</span></span>

## <a name="shader-model-for-core-devices"></a><span data-ttu-id="309b6-118">Modello shader per dispositivi Core</span><span class="sxs-lookup"><span data-stu-id="309b6-118">Shader model for Core devices</span></span>

<span data-ttu-id="309b6-119">Un dispositivo Core supporta il modello di shader 5.0 +.</span><span class="sxs-lookup"><span data-stu-id="309b6-119">A Core device supports Shader Model 5.0+.</span></span>

<span data-ttu-id="309b6-120">Il runtime esegue la conversione dei modelli di shader non DXIL 5. x in 6,0 DXIL.</span><span class="sxs-lookup"><span data-stu-id="309b6-120">The runtime performs conversion of 5.x non DXIL shader models to 6.0 DXIL.</span></span> <span data-ttu-id="309b6-121">Il driver deve pertanto supportare solo 6. x.</span><span class="sxs-lookup"><span data-stu-id="309b6-121">So the driver need only support 6.x.</span></span>

## <a name="resource-management-model-for-core-devices"></a><span data-ttu-id="309b6-122">Modello di gestione delle risorse per i dispositivi Core</span><span class="sxs-lookup"><span data-stu-id="309b6-122">Resource management model for Core devices</span></span>

- <span data-ttu-id="309b6-123">Dimensioni delle risorse supportate: solo buffer non elaborati e strutturati (nessun buffer tipizzato, texture1d/2D e così via)</span><span class="sxs-lookup"><span data-stu-id="309b6-123">Supported resource dimensions: raw and structured buffers only (no typed buffers, texture1d/2D, etc.)</span></span>
- <span data-ttu-id="309b6-124">Nessun supporto per risorse riservate (affiancate)</span><span class="sxs-lookup"><span data-stu-id="309b6-124">No support for reserved (tiled) resources</span></span>
- <span data-ttu-id="309b6-125">Nessun supporto per gli heap personalizzati</span><span class="sxs-lookup"><span data-stu-id="309b6-125">No support for custom heaps</span></span>
- <span data-ttu-id="309b6-126">Nessun supporto per uno di questi flag heap:</span><span class="sxs-lookup"><span data-stu-id="309b6-126">No support for any of these heap flags:</span></span>
  - <span data-ttu-id="309b6-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span><span class="sxs-lookup"><span data-stu-id="309b6-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span></span>
  - <span data-ttu-id="309b6-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span><span class="sxs-lookup"><span data-stu-id="309b6-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span></span>
  - <span data-ttu-id="309b6-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span><span class="sxs-lookup"><span data-stu-id="309b6-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span></span>
  - <span data-ttu-id="309b6-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (Nota gli atomici shader sono necessari, questo flag è per un'altra funzionalità, atomici Cross Adapter)</span><span class="sxs-lookup"><span data-stu-id="309b6-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (note shader atomics are required, this flag is for another feature, cross adapter atomics)</span></span>

## <a name="resource-binding-model-for-core-devices"></a><span data-ttu-id="309b6-131">Modello di associazione delle risorse per i dispositivi Core</span><span class="sxs-lookup"><span data-stu-id="309b6-131">Resource binding model for Core devices</span></span>

- <span data-ttu-id="309b6-132">Supporto solo per il livello 1 dell'associazione di risorse</span><span class="sxs-lookup"><span data-stu-id="309b6-132">Support for resource binding tier 1 only</span></span>
- <span data-ttu-id="309b6-133">Eccezioni:</span><span class="sxs-lookup"><span data-stu-id="309b6-133">Exceptions:</span></span>
  - <span data-ttu-id="309b6-134">Nessun supporto per i sampler di trama</span><span class="sxs-lookup"><span data-stu-id="309b6-134">No support for texture samplers</span></span>
  - <span data-ttu-id="309b6-135">Supporto per 64 UAV, ad esempio il livello di funzionalità 11.1 + (anziché solo 8)</span><span class="sxs-lookup"><span data-stu-id="309b6-135">Support for 64 UAVs like Feature Level 11.1+ (as opposed to only 8)</span></span>
  - <span data-ttu-id="309b6-136">Le implementazioni non devono implementare il controllo dei limiti per gli accessi dello shader alle risorse tramite i descrittori, gli accessi fuori limite producono un comportamento non definito.</span><span class="sxs-lookup"><span data-stu-id="309b6-136">Implementations do not have to implement bounds checking on shader accesses to resources through descriptors, out of bounds accesses produce undefined behavior.</span></span>
    - <span data-ttu-id="309b6-137">Come sottoprodotto, il flag di intervallo descrittore D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS nelle firme radice non è supportato.</span><span class="sxs-lookup"><span data-stu-id="309b6-137">As a byproduct, the descriptor range flag D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS in root signatures is not supported.</span></span>
- <span data-ttu-id="309b6-138">I descrittori UAV/CBV possono essere creati solo per le risorse dagli heap predefiniti (pertanto nessun heap di caricamento/readback).</span><span class="sxs-lookup"><span data-stu-id="309b6-138">UAV/CBV descriptors can only be made on resources from default heaps (so no upload/readback heaps).</span></span> <span data-ttu-id="309b6-139">In questo modo, l'applicazione eseguirà copie per ottenere i dati attraverso la GPU< >CPU.</span><span class="sxs-lookup"><span data-stu-id="309b6-139">This forces your application to do copies to get data across CPU<->GPU.</span></span>
- <span data-ttu-id="309b6-140">Nonostante sia il livello di funzionalità di binding più basso, esistono ancora alcune funzionalità necessarie anche in questo livello che vale la pena chiamare:</span><span class="sxs-lookup"><span data-stu-id="309b6-140">Despite being the lowest binding capability tier, there are still some features required even in this tier worth calling out:</span></span>
  - <span data-ttu-id="309b6-141">Gli heap dei descrittori possono essere aggiornati dopo la registrazione degli elenchi di comandi (vedere D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE nella specifica dell'associazione di risorse)</span><span class="sxs-lookup"><span data-stu-id="309b6-141">Descriptor heaps can be updated after command lists are recorded (see D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE in the resource binding spec)</span></span>
  - <span data-ttu-id="309b6-142">I descrittori radice sono fondamentalmente puntatori GPUVA</span><span class="sxs-lookup"><span data-stu-id="309b6-142">Root descriptors are basically GPUVA pointers</span></span>
    - <span data-ttu-id="309b6-143">Anche se non è disponibile alcun supporto per MMU/VA, il buffer VAs usato nei descrittori radice può essere emulato dalle implementazioni tramite l'applicazione di patch all'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="309b6-143">Even though there is no MMU / VA support, buffer VAs that are used in root descriptors can be emulated by implementations by doing address patching.</span></span>

### <a name="structured-buffer-restrictions"></a><span data-ttu-id="309b6-144">Restrizioni del buffer strutturato</span><span class="sxs-lookup"><span data-stu-id="309b6-144">Structured buffer restrictions</span></span>

<span data-ttu-id="309b6-145">I buffer strutturati devono avere un indirizzo di base a 4 byte allineato e lo stride deve essere 2 o un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="309b6-145">Structured buffers must have a base address that is 4 byte aligned, and stride must be 2 or a multiple of 4.</span></span> <span data-ttu-id="309b6-146">Il caso per uno stride di 2 è per le app con dati a 16 bit, in particolare se non è disponibile alcun supporto per i buffer tipizzati in D3D_FEATURE_LEVEL_1_0_CORE.</span><span class="sxs-lookup"><span data-stu-id="309b6-146">The case for a stride of 2 is for apps with 16 bit data, particularly given there is no support for typed buffers in D3D_FEATURE_LEVEL_1_0_CORE.</span></span>

<span data-ttu-id="309b6-147">Lo stride specificato nei descrittori deve corrispondere allo stride specificato in HLSL.</span><span class="sxs-lookup"><span data-stu-id="309b6-147">Stride specified in descriptors must match the stride specified in HLSL.</span></span>  

## <a name="command-queue-support-for-core-devices"></a><span data-ttu-id="309b6-148">Supporto della coda dei comandi per i dispositivi principali</span><span class="sxs-lookup"><span data-stu-id="309b6-148">Command queue support for Core devices</span></span>

<span data-ttu-id="309b6-149">Calcola e copia solo le code (nessuna coda 3D, video e così via).</span><span class="sxs-lookup"><span data-stu-id="309b6-149">Compute and copy queues only (no 3D, video, etc. queues).</span></span>

## <a name="shader-support-for-core-devices"></a><span data-ttu-id="309b6-150">Supporto dello shader per i dispositivi principali</span><span class="sxs-lookup"><span data-stu-id="309b6-150">Shader support for Core devices</span></span>

<span data-ttu-id="309b6-151">Solo compute shader, nessun shader grafico (Vertex, pixel shader e così via) né eventuali funzionalità correlate, ad esempio le destinazioni di rendering, le catene di scambio e l'assembler di input.</span><span class="sxs-lookup"><span data-stu-id="309b6-151">Compute shaders only, no graphics shaders (Vertex, Pixel Shaders, etc.) nor any related functionality such as render targets, swap chains, input assembler.</span></span>

### <a name="arithmetic-precision"></a><span data-ttu-id="309b6-152">Precisione aritmetica</span><span class="sxs-lookup"><span data-stu-id="309b6-152">Arithmetic precision</span></span>

<span data-ttu-id="309b6-153">I dispositivi Core non devono supportare le denormazioni per le operazioni a virgola mobile a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="309b6-153">Core devices do not have to support denorms for 16 bit floating point operations.</span></span>

## <a name="supported-apis-for-core-devices"></a><span data-ttu-id="309b6-154">API supportate per i dispositivi Core</span><span class="sxs-lookup"><span data-stu-id="309b6-154">Supported APIs for Core devices</span></span>

<span data-ttu-id="309b6-155">L'elenco seguente rappresenta il subset supportato della Application Programming Interface completa (le API *non* supportate nel livello di funzionalità di core 1,0 *non* sono elencate).</span><span class="sxs-lookup"><span data-stu-id="309b6-155">The list below represents the supported subset of the full application programming interface (APIs that are *not* supported in Core 1.0 Feature Level are *not* listed).</span></span>

### <a name="id3d12device-methods"></a><span data-ttu-id="309b6-156">Metodi ID3D12Device</span><span class="sxs-lookup"><span data-stu-id="309b6-156">ID3D12Device methods</span></span>

* [<span data-ttu-id="309b6-157">ID3D12Device::CheckFeatureSupport</span><span class="sxs-lookup"><span data-stu-id="309b6-157">ID3D12Device::CheckFeatureSupport</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [<span data-ttu-id="309b6-158">ID3D12Device::CopyDescriptors</span><span class="sxs-lookup"><span data-stu-id="309b6-158">ID3D12Device::CopyDescriptors</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [<span data-ttu-id="309b6-159">ID3D12Device::CopyDescriptorsSimple</span><span class="sxs-lookup"><span data-stu-id="309b6-159">ID3D12Device::CopyDescriptorsSimple</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [<span data-ttu-id="309b6-160">ID3D12Device::CreateCommandAllocator</span><span class="sxs-lookup"><span data-stu-id="309b6-160">ID3D12Device::CreateCommandAllocator</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [<span data-ttu-id="309b6-161">ID3D12Device::CreateCommandList</span><span class="sxs-lookup"><span data-stu-id="309b6-161">ID3D12Device::CreateCommandList</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [<span data-ttu-id="309b6-162">ID3D12Device::CreateCommandQueue</span><span class="sxs-lookup"><span data-stu-id="309b6-162">ID3D12Device::CreateCommandQueue</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [<span data-ttu-id="309b6-163">ID3D12Device::CreateCommandSignature</span><span class="sxs-lookup"><span data-stu-id="309b6-163">ID3D12Device::CreateCommandSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [<span data-ttu-id="309b6-164">ID3D12Device::CreateCommittedResource</span><span class="sxs-lookup"><span data-stu-id="309b6-164">ID3D12Device::CreateCommittedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [<span data-ttu-id="309b6-165">ID3D12Device::CreateComputePipelineState</span><span class="sxs-lookup"><span data-stu-id="309b6-165">ID3D12Device::CreateComputePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [<span data-ttu-id="309b6-166">ID3D12Device::CreateConstantBufferView</span><span class="sxs-lookup"><span data-stu-id="309b6-166">ID3D12Device::CreateConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [<span data-ttu-id="309b6-167">ID3D12Device::CreateDescriptorHeap</span><span class="sxs-lookup"><span data-stu-id="309b6-167">ID3D12Device::CreateDescriptorHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [<span data-ttu-id="309b6-168">ID3D12Device::CreateFence</span><span class="sxs-lookup"><span data-stu-id="309b6-168">ID3D12Device::CreateFence</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [<span data-ttu-id="309b6-169">ID3D12Device:: Createheap ha provocato</span><span class="sxs-lookup"><span data-stu-id="309b6-169">ID3D12Device::CreateHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [<span data-ttu-id="309b6-170">ID3D12Device::CreatePlacedResource</span><span class="sxs-lookup"><span data-stu-id="309b6-170">ID3D12Device::CreatePlacedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [<span data-ttu-id="309b6-171">ID3D12Device::CreateQueryHeap</span><span class="sxs-lookup"><span data-stu-id="309b6-171">ID3D12Device::CreateQueryHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [<span data-ttu-id="309b6-172">ID3D12Device::CreateRootSignature</span><span class="sxs-lookup"><span data-stu-id="309b6-172">ID3D12Device::CreateRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [<span data-ttu-id="309b6-173">ID3D12Device::CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="309b6-173">ID3D12Device::CreateShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [<span data-ttu-id="309b6-174">ID3D12Device::CreateSharedHandle</span><span class="sxs-lookup"><span data-stu-id="309b6-174">ID3D12Device::CreateSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [<span data-ttu-id="309b6-175">ID3D12Device::CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="309b6-175">ID3D12Device::CreateUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [<span data-ttu-id="309b6-176">ID3D12Device:: Rimuovi</span><span class="sxs-lookup"><span data-stu-id="309b6-176">ID3D12Device::Evict</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [<span data-ttu-id="309b6-177">ID3D12Device::GetAdapterLuid</span><span class="sxs-lookup"><span data-stu-id="309b6-177">ID3D12Device::GetAdapterLuid</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [<span data-ttu-id="309b6-178">ID3D12Device:: GetCopyableFootprints</span><span class="sxs-lookup"><span data-stu-id="309b6-178">ID3D12Device::GetCopyableFootprints</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [<span data-ttu-id="309b6-179">ID3D12Device::GetCustomHeapProperties</span><span class="sxs-lookup"><span data-stu-id="309b6-179">ID3D12Device::GetCustomHeapProperties</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [<span data-ttu-id="309b6-180">ID3D12Device::GetDescriptorHandleIncrementSize</span><span class="sxs-lookup"><span data-stu-id="309b6-180">ID3D12Device::GetDescriptorHandleIncrementSize</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [<span data-ttu-id="309b6-181">ID3D12Device::GetDeviceRemovedReason</span><span class="sxs-lookup"><span data-stu-id="309b6-181">ID3D12Device::GetDeviceRemovedReason</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [<span data-ttu-id="309b6-182">ID3D12Device:: GetNodeCount</span><span class="sxs-lookup"><span data-stu-id="309b6-182">ID3D12Device::GetNodeCount</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [<span data-ttu-id="309b6-183">ID3D12Device::GetResourceAllocationInfo</span><span class="sxs-lookup"><span data-stu-id="309b6-183">ID3D12Device::GetResourceAllocationInfo</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [<span data-ttu-id="309b6-184">ID3D12Device::MakeResident</span><span class="sxs-lookup"><span data-stu-id="309b6-184">ID3D12Device::MakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [<span data-ttu-id="309b6-185">ID3D12Device::OpenSharedHandle</span><span class="sxs-lookup"><span data-stu-id="309b6-185">ID3D12Device::OpenSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [<span data-ttu-id="309b6-186">ID3D12Device::OpenSharedHandleByName</span><span class="sxs-lookup"><span data-stu-id="309b6-186">ID3D12Device::OpenSharedHandleByName</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [<span data-ttu-id="309b6-187">ID3D12Device::SetStablePowerState</span><span class="sxs-lookup"><span data-stu-id="309b6-187">ID3D12Device::SetStablePowerState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a><span data-ttu-id="309b6-188">Metodi ID3D12Device1</span><span class="sxs-lookup"><span data-stu-id="309b6-188">ID3D12Device1 methods</span></span>

* [<span data-ttu-id="309b6-189">ID3D12Device1::CreatePipelineLibrary</span><span class="sxs-lookup"><span data-stu-id="309b6-189">ID3D12Device1::CreatePipelineLibrary</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [<span data-ttu-id="309b6-190">ID3D12Device1::SetEventOnMultipleFenceCompletion</span><span class="sxs-lookup"><span data-stu-id="309b6-190">ID3D12Device1::SetEventOnMultipleFenceCompletion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [<span data-ttu-id="309b6-191">ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority</span><span class="sxs-lookup"><span data-stu-id="309b6-191">ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a><span data-ttu-id="309b6-192">Metodi ID3D12Device2</span><span class="sxs-lookup"><span data-stu-id="309b6-192">ID3D12Device2 methods</span></span>

* [<span data-ttu-id="309b6-193">ID3D12Device2::CreatePipelineState</span><span class="sxs-lookup"><span data-stu-id="309b6-193">ID3D12Device2::CreatePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a><span data-ttu-id="309b6-194">Metodi ID3D12Device3</span><span class="sxs-lookup"><span data-stu-id="309b6-194">ID3D12Device3 methods</span></span>

* [<span data-ttu-id="309b6-195">ID3D12Device3::OpenExistingHeapFromAddress</span><span class="sxs-lookup"><span data-stu-id="309b6-195">ID3D12Device3::OpenExistingHeapFromAddress</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* <span data-ttu-id="309b6-196">[ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span><span class="sxs-lookup"><span data-stu-id="309b6-196">[ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span></span>
* [<span data-ttu-id="309b6-197">ID3D12Device3::EnqueueMakeResident</span><span class="sxs-lookup"><span data-stu-id="309b6-197">ID3D12Device3::EnqueueMakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a><span data-ttu-id="309b6-198">Metodi ID3D12Device4</span><span class="sxs-lookup"><span data-stu-id="309b6-198">ID3D12Device4 methods</span></span>

* [<span data-ttu-id="309b6-199">ID3D12Device4::GetResourceAllocationInfo1</span><span class="sxs-lookup"><span data-stu-id="309b6-199">ID3D12Device4::GetResourceAllocationInfo1</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a><span data-ttu-id="309b6-200">Metodi ID3D12Device5</span><span class="sxs-lookup"><span data-stu-id="309b6-200">ID3D12Device5 methods</span></span>

* [<span data-ttu-id="309b6-201">ID3D12Device5::CreateMetaCommand</span><span class="sxs-lookup"><span data-stu-id="309b6-201">ID3D12Device5::CreateMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [<span data-ttu-id="309b6-202">ID3D12Device5::CreateStateObject</span><span class="sxs-lookup"><span data-stu-id="309b6-202">ID3D12Device5::CreateStateObject</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [<span data-ttu-id="309b6-203">ID3D12Device5::EnumerateMetaCommandParameters</span><span class="sxs-lookup"><span data-stu-id="309b6-203">ID3D12Device5::EnumerateMetaCommandParameters</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [<span data-ttu-id="309b6-204">ID3D12Device5::EnumerateMetaCommands</span><span class="sxs-lookup"><span data-stu-id="309b6-204">ID3D12Device5::EnumerateMetaCommands</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [<span data-ttu-id="309b6-205">ID3D12Device5::RemoveDevice</span><span class="sxs-lookup"><span data-stu-id="309b6-205">ID3D12Device5::RemoveDevice</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a><span data-ttu-id="309b6-206">Metodi ID3D12CommandQueue</span><span class="sxs-lookup"><span data-stu-id="309b6-206">ID3D12CommandQueue methods</span></span>

* [<span data-ttu-id="309b6-207">ID3D12CommandQueue::BeginEvent</span><span class="sxs-lookup"><span data-stu-id="309b6-207">ID3D12CommandQueue::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [<span data-ttu-id="309b6-208">ID3D12CommandQueue:: chiamata endEvent</span><span class="sxs-lookup"><span data-stu-id="309b6-208">ID3D12CommandQueue::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [<span data-ttu-id="309b6-209">ID3D12CommandQueue:: oggetti executecommandlist</span><span class="sxs-lookup"><span data-stu-id="309b6-209">ID3D12CommandQueue::ExecuteCommandLists</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [<span data-ttu-id="309b6-210">ID3D12CommandQueue::GetClockCalibration</span><span class="sxs-lookup"><span data-stu-id="309b6-210">ID3D12CommandQueue::GetClockCalibration</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [<span data-ttu-id="309b6-211">ID3D12CommandQueue:: getdesc</span><span class="sxs-lookup"><span data-stu-id="309b6-211">ID3D12CommandQueue::GetDesc</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [<span data-ttu-id="309b6-212">ID3D12CommandQueue::GetTimestampFrequency</span><span class="sxs-lookup"><span data-stu-id="309b6-212">ID3D12CommandQueue::GetTimestampFrequency</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [<span data-ttu-id="309b6-213">ID3D12CommandQueue:: semarker</span><span class="sxs-lookup"><span data-stu-id="309b6-213">ID3D12CommandQueue::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [<span data-ttu-id="309b6-214">ID3D12CommandQueue:: Signal</span><span class="sxs-lookup"><span data-stu-id="309b6-214">ID3D12CommandQueue::Signal</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [<span data-ttu-id="309b6-215">ID3D12CommandQueue:: wait</span><span class="sxs-lookup"><span data-stu-id="309b6-215">ID3D12CommandQueue::Wait</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a><span data-ttu-id="309b6-216">Metodi ID3D12CommandList</span><span class="sxs-lookup"><span data-stu-id="309b6-216">ID3D12CommandList methods</span></span>

* [<span data-ttu-id="309b6-217">ID3D12CommandList:: GetType</span><span class="sxs-lookup"><span data-stu-id="309b6-217">ID3D12CommandList::GetType</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a><span data-ttu-id="309b6-218">Metodi ID3D12GraphicsCommandList</span><span class="sxs-lookup"><span data-stu-id="309b6-218">ID3D12GraphicsCommandList methods</span></span>

* [<span data-ttu-id="309b6-219">ID3D12GraphicsCommandList::BeginEvent</span><span class="sxs-lookup"><span data-stu-id="309b6-219">ID3D12GraphicsCommandList::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [<span data-ttu-id="309b6-220">ID3D12GraphicsCommandList:: BeginQuery</span><span class="sxs-lookup"><span data-stu-id="309b6-220">ID3D12GraphicsCommandList::BeginQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [<span data-ttu-id="309b6-221">ID3D12GraphicsCommandList::ClearState</span><span class="sxs-lookup"><span data-stu-id="309b6-221">ID3D12GraphicsCommandList::ClearState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [<span data-ttu-id="309b6-222">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="309b6-222">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [<span data-ttu-id="309b6-223">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="309b6-223">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [<span data-ttu-id="309b6-224">ID3D12GraphicsCommandList:: Close</span><span class="sxs-lookup"><span data-stu-id="309b6-224">ID3D12GraphicsCommandList::Close</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [<span data-ttu-id="309b6-225">ID3D12GraphicsCommandList::CopyBufferRegion</span><span class="sxs-lookup"><span data-stu-id="309b6-225">ID3D12GraphicsCommandList::CopyBufferRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [<span data-ttu-id="309b6-226">ID3D12GraphicsCommandList::CopyResource</span><span class="sxs-lookup"><span data-stu-id="309b6-226">ID3D12GraphicsCommandList::CopyResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [<span data-ttu-id="309b6-227">ID3D12GraphicsCommandList::CopyTextureRegion</span><span class="sxs-lookup"><span data-stu-id="309b6-227">ID3D12GraphicsCommandList::CopyTextureRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [<span data-ttu-id="309b6-228">ID3D12GraphicsCommandList::D patch</span><span class="sxs-lookup"><span data-stu-id="309b6-228">ID3D12GraphicsCommandList::Dispatch</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [<span data-ttu-id="309b6-229">ID3D12GraphicsCommandList:: chiamata endEvent</span><span class="sxs-lookup"><span data-stu-id="309b6-229">ID3D12GraphicsCommandList::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [<span data-ttu-id="309b6-230">ID3D12GraphicsCommandList::EndQuery</span><span class="sxs-lookup"><span data-stu-id="309b6-230">ID3D12GraphicsCommandList::EndQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [<span data-ttu-id="309b6-231">ID3D12GraphicsCommandList:: Reset</span><span class="sxs-lookup"><span data-stu-id="309b6-231">ID3D12GraphicsCommandList::Reset</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [<span data-ttu-id="309b6-232">ID3D12GraphicsCommandList::ResolveQueryData</span><span class="sxs-lookup"><span data-stu-id="309b6-232">ID3D12GraphicsCommandList::ResolveQueryData</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [<span data-ttu-id="309b6-233">ID3D12GraphicsCommandList::ResourceBarrier</span><span class="sxs-lookup"><span data-stu-id="309b6-233">ID3D12GraphicsCommandList::ResourceBarrier</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [<span data-ttu-id="309b6-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span><span class="sxs-lookup"><span data-stu-id="309b6-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [<span data-ttu-id="309b6-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span><span class="sxs-lookup"><span data-stu-id="309b6-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [<span data-ttu-id="309b6-236">ID3D12GraphicsCommandList::SetComputeRootConstantBufferView</span><span class="sxs-lookup"><span data-stu-id="309b6-236">ID3D12GraphicsCommandList::SetComputeRootConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [<span data-ttu-id="309b6-237">ID3D12GraphicsCommandList::SetComputeRootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="309b6-237">ID3D12GraphicsCommandList::SetComputeRootDescriptorTable</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [<span data-ttu-id="309b6-238">ID3D12GraphicsCommandList::SetComputeRootShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="309b6-238">ID3D12GraphicsCommandList::SetComputeRootShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [<span data-ttu-id="309b6-239">ID3D12GraphicsCommandList::SetComputeRootSignature</span><span class="sxs-lookup"><span data-stu-id="309b6-239">ID3D12GraphicsCommandList::SetComputeRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [<span data-ttu-id="309b6-240">ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="309b6-240">ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [<span data-ttu-id="309b6-241">ID3D12GraphicsCommandList::SetDescriptorHeaps</span><span class="sxs-lookup"><span data-stu-id="309b6-241">ID3D12GraphicsCommandList::SetDescriptorHeaps</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [<span data-ttu-id="309b6-242">ID3D12GraphicsCommandList:: semarker</span><span class="sxs-lookup"><span data-stu-id="309b6-242">ID3D12GraphicsCommandList::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [<span data-ttu-id="309b6-243">ID3D12GraphicsCommandList::SetPipelineState</span><span class="sxs-lookup"><span data-stu-id="309b6-243">ID3D12GraphicsCommandList::SetPipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [<span data-ttu-id="309b6-244">ID3D12GraphicsCommandList::SetPredication</span><span class="sxs-lookup"><span data-stu-id="309b6-244">ID3D12GraphicsCommandList::SetPredication</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a><span data-ttu-id="309b6-245">Metodi ID3D12GraphicsCommandList1</span><span class="sxs-lookup"><span data-stu-id="309b6-245">ID3D12GraphicsCommandList1 methods</span></span>

* [<span data-ttu-id="309b6-246">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT</span><span class="sxs-lookup"><span data-stu-id="309b6-246">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [<span data-ttu-id="309b6-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span><span class="sxs-lookup"><span data-stu-id="309b6-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a><span data-ttu-id="309b6-248">Metodi ID3D12GraphicsCommandList2</span><span class="sxs-lookup"><span data-stu-id="309b6-248">ID3D12GraphicsCommandList2 methods</span></span>

* [<span data-ttu-id="309b6-249">ID3D12GraphicsCommandList2::WriteBufferImmediate</span><span class="sxs-lookup"><span data-stu-id="309b6-249">ID3D12GraphicsCommandList2::WriteBufferImmediate</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a><span data-ttu-id="309b6-250">Metodi ID3D12GraphicsCommandList4</span><span class="sxs-lookup"><span data-stu-id="309b6-250">ID3D12GraphicsCommandList4 methods</span></span>

* [<span data-ttu-id="309b6-251">ID3D12GraphicsCommandList4::ExecuteMetaCommand</span><span class="sxs-lookup"><span data-stu-id="309b6-251">ID3D12GraphicsCommandList4::ExecuteMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [<span data-ttu-id="309b6-252">ID3D12GraphicsCommandList4::InitializeMetaCommand</span><span class="sxs-lookup"><span data-stu-id="309b6-252">ID3D12GraphicsCommandList4::InitializeMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)
