---
title: Eseguire la lettura dei dati tramite un buffer
description: Per leggere i dati dalla GPU, ad esempio per acquisire una schermata, è possibile usare un heap readback.
ms.assetid: 2F515B2C-3317-4AA8-81E1-7762ED895F77
ms.localizationpriority: high
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: 752d97d517a48a38adabc7c8fe51d11d47c1d8d3
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548861"
---
# <a name="read-back-data-via-a-buffer"></a><span data-ttu-id="cafe2-103">Eseguire la lettura dei dati tramite un buffer</span><span class="sxs-lookup"><span data-stu-id="cafe2-103">Read back data via a buffer</span></span>

<span data-ttu-id="cafe2-104">Per leggere i dati dalla GPU, ad esempio per acquisire una schermata, è possibile usare un heap readback.</span><span class="sxs-lookup"><span data-stu-id="cafe2-104">To read back data from the GPU (for example, to capture a screen shot), you use a readback heap.</span></span> <span data-ttu-id="cafe2-105">Questa tecnica è correlata al [caricamento di dati di trama tramite un buffer](upload-and-readback-of-texture-data.md), con alcune differenze.</span><span class="sxs-lookup"><span data-stu-id="cafe2-105">This technique is related to [Uploading texture data via a buffer](upload-and-readback-of-texture-data.md), with a few differences.</span></span>

- <span data-ttu-id="cafe2-106">Per eseguire la lettura dei dati, creare un heap con la **D3D12_HEAP_TYPE** impostata su [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type), anziché **D3D12_HEAP_TYPE_UPLOAD**.</span><span class="sxs-lookup"><span data-stu-id="cafe2-106">To read back data, you create a heap with the **D3D12_HEAP_TYPE** set to [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type), instead of **D3D12_HEAP_TYPE_UPLOAD**.</span></span>
- <span data-ttu-id="cafe2-107">La risorsa nell'heap read-back deve essere sempre un **D3D12_RESOURCE_DIMENSION_BUFFER**.</span><span class="sxs-lookup"><span data-stu-id="cafe2-107">The resource on the read-back heap must always be a **D3D12_RESOURCE_DIMENSION_BUFFER**.</span></span>
- <span data-ttu-id="cafe2-108">Si usa una recinzione per rilevare quando la GPU completa l'elaborazione di un frame (al termine della scrittura dei dati nel buffer di output).</span><span class="sxs-lookup"><span data-stu-id="cafe2-108">You use a fence to detect when the GPU completes processing a frame (when it is done writing data into your output buffer).</span></span> <span data-ttu-id="cafe2-109">Questo è importante perché il metodo [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) non viene sincronizzato con la GPU (viceversa, l'equivalente Direct3D 11 *non esegue* la sincronizzazione).</span><span class="sxs-lookup"><span data-stu-id="cafe2-109">This is important, because the [**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) method doesn't synchronize with the GPU (conversely, the Direct3D 11 equivalent *does* synchronize).</span></span> <span data-ttu-id="cafe2-110">Direct3D 12 le chiamate di **mapping** si comportano come se fosse stato chiamato l'equivalente Direct3D 11 con il flag NO_OVERWRITE.</span><span class="sxs-lookup"><span data-stu-id="cafe2-110">Direct3D 12 **Map** calls behave as if you called the Direct3D 11 equivalent with the NO_OVERWRITE flag.</span></span>
- <span data-ttu-id="cafe2-111">Dopo che i dati sono pronti (inclusa la barriera di risorse necessaria), chiamare [**ID3D12Resource:: Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) per rendere visibili i dati READBACK alla CPU.</span><span class="sxs-lookup"><span data-stu-id="cafe2-111">After the data is ready (including any necessary resource barrier), call [**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) to make the readback data visible to the CPU.</span></span>

## <a name="code-example"></a><span data-ttu-id="cafe2-112">Esempio di codice</span><span class="sxs-lookup"><span data-stu-id="cafe2-112">Code example</span></span>

<span data-ttu-id="cafe2-113">Nell'esempio di codice seguente viene illustrato il profilo generale del processo di lettura dei dati dalla GPU alla CPU tramite un buffer.</span><span class="sxs-lookup"><span data-stu-id="cafe2-113">The code example below shows the general outline of the process of reading back data from the GPU to the CPU via a buffer.</span></span>

```cppwinrt

// The output buffer (created below) is on a default heap, so only the GPU can access it.

D3D12_HEAP_PROPERTIES defaultHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT) };
D3D12_RESOURCE_DESC outputBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize, D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS) };
winrt::com_ptr<::ID3D12Resource> outputBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &defaultHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &outputBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(outputBuffer),
    outputBuffer.put_void()));

// The readback buffer (created below) is on a readback heap, so that the CPU can access it.

D3D12_HEAP_PROPERTIES readbackHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_READBACK) };
D3D12_RESOURCE_DESC readbackBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize) };
winrt::com_ptr<::ID3D12Resource> readbackBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &readbackHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &readbackBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(readbackBuffer),
    readbackBuffer.put_void()));

{
    D3D12_RESOURCE_BARRIER outputBufferResourceBarrier
    {
        CD3DX12_RESOURCE_BARRIER::Transition(
            outputBuffer.get(),
            D3D12_RESOURCE_STATE_COPY_DEST,
            D3D12_RESOURCE_STATE_COPY_SOURCE)
    };
    commandList->ResourceBarrier(1, &outputBufferResourceBarrier);
}

commandList->CopyResource(readbackBuffer.get(), outputBuffer.get());

// Code goes here to close, execute (and optionally reset) the command list, and also
// to use a fence to wait for the command queue.

// The code below assumes that the GPU wrote FLOATs to the buffer.

D3D12_RANGE readbackBufferRange{ 0, outputBufferSize };
FLOAT * pReadbackBufferData{};
winrt::check_hresult(
    readbackBuffer->Map
    (
        0,
        &readbackBufferRange,
        reinterpret_cast<void**>(&pReadbackBufferData)
    )
);

// Code goes here to access the data via pReadbackBufferData.

D3D12_RANGE emptyRange{ 0, 0 };
readbackBuffer->Unmap
(
    0,
    &emptyRange
);
```

<span data-ttu-id="cafe2-114">Per un'implementazione completa di una routine screenshot che legge la trama della destinazione di rendering e la scrive su disco come file, vedere *DirectX Tool Kit per* [Screengrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp)di DX12.</span><span class="sxs-lookup"><span data-stu-id="cafe2-114">For a full implementation of a screenshot routine that reads the render target texture, and writes it to disk as a file, see *DirectX Tool Kit for DX12*'s [ScreenGrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cafe2-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cafe2-115">Related topics</span></span>

* [<span data-ttu-id="cafe2-116">Sottoallocazione all'interno di un buffer</span><span class="sxs-lookup"><span data-stu-id="cafe2-116">Suballocation within a buffer</span></span>](large-buffers.md)
