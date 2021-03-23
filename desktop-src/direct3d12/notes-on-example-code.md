---
title: Codice di esempio nel riferimento D3D12
description: Viene illustrato l'uso del codice di esempio nella documentazione di Direct3D 12.
ms.assetid: C2323482-D06D-43B7-9BDE-BFB9A6A6B70D
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d65dd8db64dd829a7a318717e44a64ea189c7a3
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548789"
---
# <a name="example-code-in-the-d3d12-reference"></a>Codice di esempio nel riferimento D3D12

Viene illustrato l'uso del codice di esempio nella documentazione di Direct3D 12.

-   [Codice frammento di esempio](#example-snippet-code)
-   [Argomenti correlati](#related-topics)

## <a name="example-snippet-code"></a>Codice frammento di esempio

Il codice di esempio illustrato nella Guida di riferimento a Direct3D 12 non è compilabile o codice di esecuzione. si tratta semplicemente di un frammento di codice che fornisce un esempio di come viene chiamata l'API. Alcuni esempi elencano le variabili globali e i membri di classe usati dalle chiamate, ad esempio:

Oggetti pipeline globali.


```C++
D3D12_VIEWPORT m_viewport;
D3D12_RECT m_scissorRect;
ComPtr<IDXGISwapChain3> m_swapChain;
ComPtr<ID3D12Device> m_device;
ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
ComPtr<ID3D12CommandAllocator> m_commandAllocator;
ComPtr<ID3D12CommandQueue> m_commandQueue;
ComPtr<ID3D12RootSignature> m_rootSignature;
ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
ComPtr<ID3D12PipelineState> m_pipelineState;
ComPtr<ID3D12GraphicsCommandList> m_commandList;
UINT m_rtvDescriptorSize;
```



Popolamento degli elenchi di comandi.


```C++
// Command list allocators can only be reset when the associated 
// command lists have finished execution on the GPU; apps should use 
// fences to determine GPU execution progress.
ThrowIfFailed(m_commandAllocator->Reset());

// However, when ExecuteCommandList() is called on a particular command 
// list, that command list can then be reset at any time and must be before 
// re-recording.
ThrowIfFailed(m_commandList->Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

// Set necessary state.
m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());
m_commandList->RSSetViewports(1, &m_viewport);
m_commandList->RSSetScissorRects(1, &m_scissorRect);

// Indicate that the back buffer will be used as a render target.
auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET);
m_commandList->ResourceBarrier(1, &barrier);

CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

// Record commands.
const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
m_commandList->DrawInstanced(3, 1, 0, 0);

// Indicate that the back buffer will now be used to present.
m_commandList->ResourceBarrier(1, &barrier);
barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT);
ThrowIfFailed(m_commandList->Close());
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un componente Direct3D 12 di base](creating-a-basic-direct3d-12-component.md)
</dt> <dt>

[Guida di riferimento a Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Procedure dettagliate per il codice D3D12](d3d12-code-walk-throughs.md)
</dt> <dt>

[Esempi di lavoro](working-samples.md)
</dt> </dl>

 

 




