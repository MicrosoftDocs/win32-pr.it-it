---
title: Livello di funzionalità di Direct3D 12 Core 1.0
description: Il livello di funzionalità Core 1.0 è un subset del set completo di funzionalità Direct3D 12.
ms.topic: article
ms.date: 11/05/2019
ms.openlocfilehash: 93eab39509074114bf2032cfb1cdea3e4e767dae9786241a34f970ca5cd51703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530721"
---
# <a name="the-direct3d-12-core-10-feature-level"></a>Livello di funzionalità di Direct3D 12 Core 1.0

Il livello di funzionalità Core 1.0 è un subset del set completo di funzionalità Direct3D 12. Il livello di funzionalità Core 1.0 può essere esposto da una categoria di dispositivi noti come *dispositivi solo di calcolo.* Il modello di driver complessivo per i dispositivi di solo calcolo è microsoft Compute Driver Model (MCDM). MCDM è un peer con scalabilità orizzontale del Windows Device Driver Model (WDDM), che ha un ambito più ampio.

Un dispositivo che supporta solo *le* funzionalità all'interno di un livello di funzionalità core è noto come *dispositivo core.*

> [!NOTE]
> *Il dispositivo solo calcolo,* *il dispositivo MCDM,* *il dispositivo a livello* di funzionalità principale e il dispositivo *Core* hanno tutti lo stesso significato. Per semplicità, è preferibile usare il dispositivo *Core.*

## <a name="creating-a-core-device"></a>Creazione di un dispositivo Core

In generale, per creare un dispositivo Direct3D 12, chiamare la [**funzione D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) e specificare un livello di funzionalità minimo.

Se si specifica un livello di funzionalità da 9 a 12, il dispositivo restituito è un dispositivo ricco di funzionalità, ad esempio una GPU tradizionale (che supporta un superset delle funzionalità di un dispositivo Core). Un dispositivo Core non viene mai restituito per tale intervallo di livelli di funzionalità.

D'altra parte, se si specifica un livello di funzionalità Core (ad [**esempio, D3D_FEATURE_LEVEL::D 3D_FEATURE_LEVEL_1_0_CORE),**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)il dispositivo restituito potrebbe essere ricco di funzionalità o potrebbe essere un dispositivo Core.

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

Se si specifica un livello di funzionalità, il livello di runtime/debug verifica che le funzionalità utilizzate dall'applicazione siano `_CORE` consentite da tale `_CORE` livello di funzionalità. Questo set di funzionalità è definito più avanti in questo argomento.

## <a name="shader-model-for-core-devices"></a>Modello shader per dispositivi Core

Un dispositivo Core supporta Shader Model 5.0+.

Il runtime esegue la conversione di modelli shader non DXIL da 5.x a 6.0 DXIL. Il driver deve quindi supportare solo la versione 6.x.

## <a name="resource-management-model-for-core-devices"></a>Modello di gestione delle risorse per i dispositivi Core

- Dimensioni delle risorse supportate: solo buffer non elaborati e strutturati (senza buffer tipici, texture1d/2D e così via)
- Nessun supporto per le risorse riservate (affiancate)
- Nessun supporto per gli heap personalizzati
- Nessun supporto per uno di questi flag heap:
  - D3D12_HEAP_FLAG_HARDWARE_PROTECTED
  - D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH
  - D3D12_HEAP_FLAG_ALLOW_DISPLAY
  - D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (si noti che sono necessari atomici shader, questo flag è per un'altra funzionalità, atomiche tra adattatori)

## <a name="resource-binding-model-for-core-devices"></a>Modello di associazione di risorse per i dispositivi Core

- Supporto solo per il livello di binding delle risorse 1
- Eccezioni:
  - Nessun supporto per i campionatori di trame
  - Supporto per 64 UAV come Feature Level 11.1+ (anziché solo 8)
  - Le implementazioni non devono implementare il controllo dei limiti sugli accessi dello shader alle risorse tramite descrittori, gli accessi fuori dai limiti producono un comportamento non definito.
    - Come sottoprodotto, il flag dell'intervallo di D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS nelle firme radice non è supportato.
- I descrittori UAV/CBV possono essere emesse solo sulle risorse dagli heap predefiniti (quindi non sono disponibili heap di caricamento/readback). In questo modo l'applicazione deve eseguire copie per ottenere i dati< CPU >GPU.
- Nonostante sia il livello di funzionalità di associazione più basso, esistono ancora alcune funzionalità necessarie anche in questo livello, vale la pena notare:
  - Gli heap dei descrittori possono essere aggiornati dopo la registrazione degli elenchi di comandi (vedere D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE nella specifica di associazione di risorse)
  - I descrittori radice sono fondamentalmente puntatori GPUVA
    - Anche se non è disponibile alcun supporto MMU/VA, le macchine virtuali del buffer usate nei descrittori radice possono essere emulate dalle implementazioni eseguendo l'applicazione di patch degli indirizzi.

### <a name="structured-buffer-restrictions"></a>Restrizioni del buffer strutturato

I buffer strutturati devono avere un indirizzo di base allineato a 4 byte e stride deve essere 2 o un multiplo di 4. Il caso di uno stride di 2 è per le app con dati a 16 bit, in particolare dato che non è disponibile alcun supporto per i buffer tipi D3D_FEATURE_LEVEL_1_0_CORE.

Lo stride specificato nei descrittori deve corrispondere a quello specificato in HLSL.  

## <a name="command-queue-support-for-core-devices"></a>Supporto della coda di comandi per i dispositivi Core

Solo code di calcolo e copia (nessuna coda 3D, video e così via).

## <a name="shader-support-for-core-devices"></a>Supporto dello shader per i dispositivi Core

Solo shader di calcolo, nessun graphics shader (Vertex, Pixel Shader e così via) né funzionalità correlate, ad esempio destinazioni di rendering, catene di scambio, assembler di input.

### <a name="arithmetic-precision"></a>Precisione aritmetica

I dispositivi di base non devono supportare i denorm per le operazioni a virgola mobile a 16 bit.

## <a name="supported-apis-for-core-devices"></a>API supportate per i dispositivi Core

L'elenco seguente rappresenta il subset supportato dell'interfaccia di  programmazione completa delle applicazioni (le API non supportate nel livello di funzionalità Core 1.0 non *sono* elencate).

### <a name="id3d12device-methods"></a>Metodi id3D12Device

* [ID3D12Device::CheckFeatureSupport](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [ID3D12Device::CopyDescriptors](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [ID3D12Device::CopyDescriptorsSimple](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [ID3D12Device::CreateCommandAllocator](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [ID3D12Device::CreateCommandList](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [ID3D12Device::CreateCommandQueue](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [ID3D12Device::CreateCommandSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [ID3D12Device::CreateCommittedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [ID3D12Device::CreateComputePipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [ID3D12Device::CreateConstantBufferView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [ID3D12Device::CreateDescriptorHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [ID3D12Device::CreateFence](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [ID3D12Device::CreateHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [ID3D12Device::CreatePlacedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [ID3D12Device::CreateQueryHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [ID3D12Device::CreateRootSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [ID3D12Device::CreateShaderResourceView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [ID3D12Device::CreateSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [ID3D12Device::CreateUnorderedAccessView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [ID3D12Device::Evict](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [ID3D12Device::GetAdapterLuid](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [ID3D12Device::GetCopyableFootprints](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [ID3D12Device::GetCustomHeapProperties](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [ID3D12Device::GetDescriptorHandleIncrementSize](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [ID3D12Device::GetDeviceRemovedReason](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [ID3D12Device::GetNodeCount](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [ID3D12Device::GetResourceAllocationInfo](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [ID3D12Device::MakeResident](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [ID3D12Device::OpenSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [ID3D12Device::OpenSharedHandleByName](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [ID3D12Device::SetStablePowerState](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a>Metodi ID3D12Device1

* [ID3D12Device1::CreatePipelineLibrary](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [ID3D12Device1::SetEventOnMultipleFenceCompletion](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a>Metodi ID3D12Device2

* [ID3D12Device2::CreatePipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a>Metodi ID3D12Device3

* [ID3D12Device3::OpenExistingHeapFromAddress](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* [ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))
* [ID3D12Device3::EnqueueMakeResident](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a>Metodi ID3D12Device4

* [ID3D12Device4::GetResourceAllocationInfo1](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a>Metodi ID3D12Device5

* [ID3D12Device5::CreateMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [ID3D12Device5::CreateStateObject](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [ID3D12Device5::EnumerateMetaCommandParameters](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [ID3D12Device5::EnumerateMetaCommands](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [ID3D12Device5::RemoveDevice](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a>Metodi id3D12CommandQueue

* [ID3D12CommandQueue::BeginEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [ID3D12CommandQueue::EndEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [ID3D12CommandQueue::ExecuteCommandLists](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [ID3D12CommandQueue::GetClockCalibration](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [ID3D12CommandQueue::GetDesc](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [ID3D12CommandQueue::GetTimestampFrequency](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [ID3D12CommandQueue::SetMarker](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [ID3D12CommandQueue::Signal](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [ID3D12CommandQueue::Wait](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a>Metodi id3D12CommandList

* [ID3D12CommandList::GetType](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a>Metodi id3D12GraphicsCommandList

* [ID3D12GraphicsCommandList::BeginEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [ID3D12GraphicsCommandList::BeginQuery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [ID3D12GraphicsCommandList::ClearState](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [ID3D12GraphicsCommandList::Close](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [ID3D12GraphicsCommandList::CopyBufferRegion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [ID3D12GraphicsCommandList::CopyResource](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [ID3D12GraphicsCommandList::CopyTextureRegion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [ID3D12GraphicsCommandList::D ispatch](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [ID3D12GraphicsCommandList::EndEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [ID3D12GraphicsCommandList::EndQuery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [ID3D12GraphicsCommandList::Reset](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [ID3D12GraphicsCommandList::ResolveQueryData](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [ID3D12GraphicsCommandList::ResourceBarrier](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstant](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstants](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [ID3D12GraphicsCommandList::SetComputeRootConstantBufferView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [ID3D12GraphicsCommandList::SetComputeRootDescriptorTable](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [ID3D12GraphicsCommandList::SetComputeRootShaderResourceView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [ID3D12GraphicsCommandList::SetComputeRootSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [ID3D12GraphicsCommandList::SetDescriptorHeaps](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [ID3D12GraphicsCommandList::SetMarker](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [ID3D12GraphicsCommandList::SetPipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [ID3D12GraphicsCommandList::SetPredication](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a>Metodi ID3D12GraphicsCommandList1

* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a>Metodi id3D12GraphicsCommandList2

* [ID3D12GraphicsCommandList2::WriteBufferImmediate](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a>Metodi ID3D12GraphicsCommandList4

* [ID3D12GraphicsCommandList4::ExecuteMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [ID3D12GraphicsCommandList4::InitializeMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)
