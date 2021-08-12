---
title: Leggere i dati tramite un buffer
description: Per leggere i dati dalla GPU,ad esempio per acquisire uno screenshot, si usa un heap di readback.
ms.assetid: 2F515B2C-3317-4AA8-81E1-7762ED895F77
ms.localizationpriority: high
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: 56babd93ddd0f06ee331b19db4a4d8ba2dc5ecb314ec3d828e3e3f7c4f4f9a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300874"
---
# <a name="read-back-data-via-a-buffer"></a>Leggere i dati tramite un buffer

Per leggere i dati dalla GPU,ad esempio per acquisire uno screenshot, si usa un heap di readback. Questa tecnica è correlata al [caricamento dei dati di trama tramite un buffer](upload-and-readback-of-texture-data.md), con alcune differenze.

- Per leggere i dati, si crea un heap con D3D12_HEAP_TYPE **impostato** su [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type), **anziché su D3D12_HEAP_TYPE_UPLOAD**.
- La risorsa nell'heap read-back deve essere sempre un **D3D12_RESOURCE_DIMENSION_BUFFER**.
- Si usa un limite per rilevare quando la GPU completa l'elaborazione di un frame (al termine della scrittura dei dati nel buffer di output). Questo è importante, perché il [**metodo ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) non esegue la sincronizzazione con la GPU (al contrario, l'equivalente direct3D 11 esegue la *sincronizzazione).* Le chiamate mappa  Direct3D 12 si comportano come se si chiamava l'equivalente Direct3D 11 con il flag NO_OVERWRITE.
- Quando i dati sono pronti (inclusa qualsiasi barriera di risorse necessaria), chiamare [**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) per rendere i dati di readback visibili alla CPU.

## <a name="code-example"></a>Esempio di codice

L'esempio di codice seguente illustra la struttura generale del processo di lettura dei dati dalla GPU alla CPU tramite un buffer.

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

Per un'implementazione completa di una routine screenshot che legge la trama di destinazione di rendering e la scrive su disco come file, vedere DirectX Tool Kit per [ScreenGrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp)di *DX12.*

## <a name="related-topics"></a>Argomenti correlati

* [Sottoallocazione all'interno di un buffer](large-buffers.md)
