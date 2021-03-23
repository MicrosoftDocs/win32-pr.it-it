---
title: Simulazione della gravità del corpo a più motori
description: L'esempio D3D12nBodyGravity illustra come eseguire il lavoro di calcolo in modo asincrono.
ms.assetid: B20C5575-0616-43F7-9AC9-5F802E5597B5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60782519de6f655882717c4ea657668129a6ce3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548805"
---
# <a name="multi-engine-n-body-gravity-simulation"></a><span data-ttu-id="e7a2e-103">Simulazione della gravità del corpo a più motori</span><span class="sxs-lookup"><span data-stu-id="e7a2e-103">Multi-engine n-body gravity simulation</span></span>

<span data-ttu-id="e7a2e-104">L'esempio **D3D12nBodyGravity** illustra come eseguire il lavoro di calcolo in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-104">The **D3D12nBodyGravity** sample demonstrates how to do compute work asynchronously.</span></span> <span data-ttu-id="e7a2e-105">L'esempio avvia un numero di thread ciascuno con una coda di comandi di calcolo e pianifica il lavoro di calcolo sulla GPU che esegue una simulazione di gravità n corpo.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-105">The sample spins up a number of threads each with a compute command queue and schedules compute work on the GPU that performs an n-body gravity simulation.</span></span> <span data-ttu-id="e7a2e-106">Ogni thread opera su due buffer pieni di dati sulla posizione e sulla velocità.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-106">Each thread operates on two buffers full of position and velocity data.</span></span> <span data-ttu-id="e7a2e-107">Con ogni iterazione, compute shader legge i dati della posizione e della velocità correnti da un buffer e scrive l'iterazione successiva nell'altro buffer.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-107">With each iteration, the compute shader reads the current position and velocity data from one buffer and writes the next iteration into the other buffer.</span></span> <span data-ttu-id="e7a2e-108">Al termine dell'iterazione, compute shader scambia quale buffer è il SRV per la lettura dei dati di posizione/velocità e che è il UAV per la scrittura di aggiornamenti della posizione/velocità modificando lo stato della risorsa in ogni buffer.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-108">When the iteration completes, the compute shader swaps which buffer is the SRV for reading position/velocity data and which is the UAV for writing position/velocity updates by changing the resource state on each buffer.</span></span>

-   [<span data-ttu-id="e7a2e-109">Creare le firme radice</span><span class="sxs-lookup"><span data-stu-id="e7a2e-109">Create the root signatures</span></span>](#create-the-root-signatures)
-   [<span data-ttu-id="e7a2e-110">Creare i buffer SRV e UAV</span><span class="sxs-lookup"><span data-stu-id="e7a2e-110">Create the SRV and UAV buffers</span></span>](#create-the-srv-and-uav-buffers)
-   [<span data-ttu-id="e7a2e-111">Creare i buffer CBV e vertex</span><span class="sxs-lookup"><span data-stu-id="e7a2e-111">Create the CBV and vertex buffers</span></span>](#create-the-cbv-and-vertex-buffers)
-   [<span data-ttu-id="e7a2e-112">Sincronizzare i thread di rendering e di calcolo</span><span class="sxs-lookup"><span data-stu-id="e7a2e-112">Synchronize the rendering and compute threads</span></span>](#synchronize-the-rendering-and-compute-threads)
-   [<span data-ttu-id="e7a2e-113">Eseguire l'esempio</span><span class="sxs-lookup"><span data-stu-id="e7a2e-113">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="e7a2e-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7a2e-114">Related topics</span></span>](#related-topics)

## <a name="create-the-root-signatures"></a><span data-ttu-id="e7a2e-115">Creare le firme radice</span><span class="sxs-lookup"><span data-stu-id="e7a2e-115">Create the root signatures</span></span>

<span data-ttu-id="e7a2e-116">Si inizia creando sia una grafica che una firma radice di calcolo nel metodo **LoadAssets** .</span><span class="sxs-lookup"><span data-stu-id="e7a2e-116">We start out by creating both a graphics and a compute root signature, in the **LoadAssets** method.</span></span> <span data-ttu-id="e7a2e-117">Entrambe le firme radice hanno una visualizzazione buffer costante radice (CBV) e una tabella dei descrittori di visualizzazione risorse shader (SRV).</span><span class="sxs-lookup"><span data-stu-id="e7a2e-117">Both root signatures have a root constant buffer view (CBV) and a shader resource view (SRV) descriptor table.</span></span> <span data-ttu-id="e7a2e-118">La firma radice di calcolo dispone anche di una tabella dei descrittori UAV (unordered Access View).</span><span class="sxs-lookup"><span data-stu-id="e7a2e-118">The compute root signature also has an unordered access view (UAV) descriptor table.</span></span>

``` syntax
 // Create the root signatures.
       {
              CD3DX12_DESCRIPTOR_RANGE ranges[2];
              ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1, 0);
              ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_UAV, 1, 0);

              CD3DX12_ROOT_PARAMETER rootParameters[RootParametersCount];
              rootParameters[RootParameterCB].InitAsConstantBufferView(0, 0, D3D12_SHADER_VISIBILITY_ALL);
              rootParameters[RootParameterSRV].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_VERTEX);
              rootParameters[RootParameterUAV].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_ALL);

              // The rendering pipeline does not need the UAV parameter.
              CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
              rootSignatureDesc.Init(_countof(rootParameters) - 1, rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

              ComPtr<ID3DBlob> signature;
              ComPtr<ID3DBlob> error;
              ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

              // Create compute signature. Must change visibility for the SRV.
              rootParameters[RootParameterSRV].ShaderVisibility = D3D12_SHADER_VISIBILITY_ALL;

              CD3DX12_ROOT_SIGNATURE_DESC computeRootSignatureDesc(_countof(rootParameters), rootParameters, 0, nullptr);
              ThrowIfFailed(D3D12SerializeRootSignature(&computeRootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));

              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_computeRootSignature)));
       }
```



| <span data-ttu-id="e7a2e-119">Flusso di chiamate</span><span class="sxs-lookup"><span data-stu-id="e7a2e-119">Call flow</span></span>                                                             | <span data-ttu-id="e7a2e-120">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7a2e-120">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="e7a2e-121">**\_Intervallo descrittore CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-121">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="e7a2e-122">**\_Tipo di \_ intervallo descrittore D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-122">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="e7a2e-123">**\_Parametro radice \_ CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-123">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="e7a2e-124">**\_Visibilità shader D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-124">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="e7a2e-125">**\_Descrizione della \_ firma \_ radice CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-125">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="e7a2e-126">**\_Flag di \_ firma \_ radice D3D12**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-126">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="e7a2e-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7a2e-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="e7a2e-128">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-128">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="e7a2e-129">**\_Versione della \_ firma \_ radice D3D**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-129">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="e7a2e-130">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-130">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [<span data-ttu-id="e7a2e-131">**\_Descrizione della \_ firma \_ radice CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-131">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) |                                                                       |
| [<span data-ttu-id="e7a2e-132">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-132">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="e7a2e-133">**\_Versione della \_ firma \_ radice D3D**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-133">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="e7a2e-134">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-134">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-srv-and-uav-buffers"></a><span data-ttu-id="e7a2e-135">Creare i buffer SRV e UAV</span><span class="sxs-lookup"><span data-stu-id="e7a2e-135">Create the SRV and UAV buffers</span></span>

<span data-ttu-id="e7a2e-136">I buffer SRV e UAV sono costituiti da una matrice di dati di posizione e velocità.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-136">The SRV and UAV buffers consist of an array of position and velocity data.</span></span>

``` syntax
 // Position and velocity data for the particles in the system.
       // Two buffers full of Particle data are utilized in this sample.
       // The compute thread alternates writing to each of them.
       // The render thread renders using the buffer that is not currently
       // in use by the compute shader.
       struct Particle
       {
              XMFLOAT4 position;
              XMFLOAT4 velocity;
       };
```



| <span data-ttu-id="e7a2e-137">Flusso di chiamate</span><span class="sxs-lookup"><span data-stu-id="e7a2e-137">Call flow</span></span>                       | <span data-ttu-id="e7a2e-138">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7a2e-138">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="e7a2e-139">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-139">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

## <a name="create-the-cbv-and-vertex-buffers"></a><span data-ttu-id="e7a2e-140">Creare i buffer CBV e vertex</span><span class="sxs-lookup"><span data-stu-id="e7a2e-140">Create the CBV and vertex buffers</span></span>

<span data-ttu-id="e7a2e-141">Per la pipeline grafica, CBV è uno **struct** che contiene due matrici usate dal geometry shader.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-141">For the graphics pipeline, the CBV is a **struct** containing two matrices used by the geometry shader.</span></span> <span data-ttu-id="e7a2e-142">Geometry shader acquisisce la posizione di ogni particella nel sistema e genera un quad per rappresentarlo usando queste matrici.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-142">The geometry shader takes the position of each particle in the system and generates a quad to represent it using these matrices.</span></span>

``` syntax
 struct ConstantBufferGS
       {
              XMMATRIX worldViewProjection;
              XMMATRIX inverseView;

              // Constant buffers are 256-byte aligned in GPU memory. Padding is added
              // for convenience when computing the struct's size.
              float padding[32];
       };
```



| <span data-ttu-id="e7a2e-143">Flusso di chiamate</span><span class="sxs-lookup"><span data-stu-id="e7a2e-143">Call flow</span></span>                       | <span data-ttu-id="e7a2e-144">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7a2e-144">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="e7a2e-145">**XMMATRIX**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-145">**XMMATRIX**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) |            |



 

<span data-ttu-id="e7a2e-146">Di conseguenza, il buffer dei vertici utilizzato dal vertex shader in realtà non contiene alcun dato posizionale.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-146">As a result, the vertex buffer used by the vertex shader actually does not contain any positional data.</span></span>

``` syntax
 // "Vertex" definition for particles. Triangle vertices are generated 
       // by the geometry shader. Color data will be assigned to those 
       // vertices via this struct.
       struct ParticleVertex
       {
              XMFLOAT4 color;
       };
```



| <span data-ttu-id="e7a2e-147">Flusso di chiamate</span><span class="sxs-lookup"><span data-stu-id="e7a2e-147">Call flow</span></span>                       | <span data-ttu-id="e7a2e-148">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7a2e-148">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="e7a2e-149">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-149">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

<span data-ttu-id="e7a2e-150">Per la pipeline di calcolo, CBV è uno **struct** che contiene alcune costanti usate dalla simulazione di gravità del corpo n nel compute shader.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-150">For the compute pipeline, the CBV is a **struct** containing some constants used by the n-body gravity simulation in the compute shader.</span></span>

``` syntax
 struct ConstantBufferCS
       {
              UINT param[4];
              float paramf[4];
       };
```

## <a name="synchronize-the-rendering-and-compute-threads"></a><span data-ttu-id="e7a2e-151">Sincronizzare i thread di rendering e di calcolo</span><span class="sxs-lookup"><span data-stu-id="e7a2e-151">Synchronize the rendering and compute threads</span></span>

<span data-ttu-id="e7a2e-152">Una volta inizializzati tutti i buffer, verranno avviati il rendering e il lavoro di calcolo.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-152">After the buffers are all initialized, the rendering and compute work will begin.</span></span> <span data-ttu-id="e7a2e-153">Il thread di calcolo cambierà lo stato dei due buffer di posizione/velocità tra SRV e UAV durante l'iterazione della simulazione e il thread di rendering deve assicurarsi che pianifica il lavoro sulla pipeline grafica che opera sul SRV.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-153">The compute thread will be changing the state of the two position/velocity buffers back and forth between SRV and UAV as it iterates on the simulation, and the rendering thread needs to ensure that it schedules work on the graphics pipeline that operates on the SRV.</span></span> <span data-ttu-id="e7a2e-154">Le recinzioni vengono usate per sincronizzare l'accesso ai due buffer.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-154">Fences are used to synchronize access to the two buffers.</span></span>

<span data-ttu-id="e7a2e-155">Nel thread di rendering:</span><span class="sxs-lookup"><span data-stu-id="e7a2e-155">On the Render thread:</span></span>

``` syntax
// Render the scene.
void D3D12nBodyGravity::OnRender()
{
       // Let the compute thread know that a new frame is being rendered.
       for (int n = 0; n < ThreadCount; n++)
       {
              InterlockedExchange(&m_renderContextFenceValues[n], m_renderContextFenceValue);
       }

       // Compute work must be completed before the frame can render or else the SRV 
       // will be in the wrong state.
       for (UINT n = 0; n < ThreadCount; n++)
       {
              UINT64 threadFenceValue = InterlockedGetValue(&m_threadFenceValues[n]);
              if (m_threadFences[n]->GetCompletedValue() < threadFenceValue)
              {
                     // Instruct the rendering command queue to wait for the current 
                     // compute work to complete.
                     ThrowIfFailed(m_commandQueue->Wait(m_threadFences[n].Get(), threadFenceValue));
              }
       }

       // Record all the commands we need to render the scene into the command list.
       PopulateCommandList();

       // Execute the command list.
       ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
       m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

       // Present the frame.
       ThrowIfFailed(m_swapChain->Present(0, 0));

       MoveToNextFrame();
}
```



| <span data-ttu-id="e7a2e-156">Flusso di chiamate</span><span class="sxs-lookup"><span data-stu-id="e7a2e-156">Call flow</span></span>                                                              | <span data-ttu-id="e7a2e-157">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7a2e-157">Parameters</span></span> |
|------------------------------------------------------------------------|------------|
| [<span data-ttu-id="e7a2e-158">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-158">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                  |            |
| [<span data-ttu-id="e7a2e-159">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-159">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)           |            |
| [<span data-ttu-id="e7a2e-160">**GetCompletedValue**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-160">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)             |            |
| [<span data-ttu-id="e7a2e-161">**Attesa**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-161">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                |            |
| [<span data-ttu-id="e7a2e-162">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-162">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [<span data-ttu-id="e7a2e-163">**Oggetti executecommandlist**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-163">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [<span data-ttu-id="e7a2e-164">**IDXGISwapChain1::Present1**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-164">**IDXGISwapChain1::Present1**</span></span>](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

<span data-ttu-id="e7a2e-165">Per semplificare l'esempio, il thread di calcolo attende che la GPU completi ogni iterazione prima di pianificare altre attività di calcolo.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-165">To simplify the sample a bit, the compute thread waits for the GPU to complete each iteration before scheduling any more compute work.</span></span> <span data-ttu-id="e7a2e-166">In pratica, è probabile che le applicazioni mantengano la coda di calcolo completa per ottenere le massime prestazioni dalla GPU.</span><span class="sxs-lookup"><span data-stu-id="e7a2e-166">In practice, applications will likely want to keep the compute queue full to achieve maximum performance from the GPU.</span></span>

<span data-ttu-id="e7a2e-167">Nel thread di calcolo:</span><span class="sxs-lookup"><span data-stu-id="e7a2e-167">On the Compute thread:</span></span>

``` syntax
DWORD D3D12nBodyGravity::AsyncComputeThreadProc(int threadIndex)
{
       ID3D12CommandQueue* pCommandQueue = m_computeCommandQueue[threadIndex].Get();
       ID3D12CommandAllocator* pCommandAllocator = m_computeAllocator[threadIndex].Get();
       ID3D12GraphicsCommandList* pCommandList = m_computeCommandList[threadIndex].Get();
       ID3D12Fence* pFence = m_threadFences[threadIndex].Get();

       while (0 == InterlockedGetValue(&m_terminating))
       {
              // Run the particle simulation.
              Simulate(threadIndex);

              // Close and execute the command list.
              ThrowIfFailed(pCommandList->Close());
              ID3D12CommandList* ppCommandLists[] = { pCommandList };

              pCommandQueue->ExecuteCommandLists(1, ppCommandLists);

              // Wait for the compute shader to complete the simulation.
              UINT64 threadFenceValue = InterlockedIncrement(&m_threadFenceValues[threadIndex]);
              ThrowIfFailed(pCommandQueue->Signal(pFence, threadFenceValue));
              ThrowIfFailed(pFence->SetEventOnCompletion(threadFenceValue, m_threadFenceEvents[threadIndex]));
              WaitForSingleObject(m_threadFenceEvents[threadIndex], INFINITE);

              // Wait for the render thread to be done with the SRV so that
              // the next frame in the simulation can run.
              UINT64 renderContextFenceValue = InterlockedGetValue(&m_renderContextFenceValues[threadIndex]);
              if (m_renderContextFence->GetCompletedValue() < renderContextFenceValue)
              {
                     ThrowIfFailed(pCommandQueue->Wait(m_renderContextFence.Get(), renderContextFenceValue));
                     InterlockedExchange(&m_renderContextFenceValues[threadIndex], 0);
              }

              // Swap the indices to the SRV and UAV.
              m_srvIndex[threadIndex] = 1 - m_srvIndex[threadIndex];

              // Prepare for the next frame.
              ThrowIfFailed(pCommandAllocator->Reset());
              ThrowIfFailed(pCommandList->Reset(pCommandAllocator, m_computeState.Get()));
       }

       return 0;
}
```



| <span data-ttu-id="e7a2e-168">Flusso di chiamate</span><span class="sxs-lookup"><span data-stu-id="e7a2e-168">Call flow</span></span>                                                                   | <span data-ttu-id="e7a2e-169">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7a2e-169">Parameters</span></span> |
|-----------------------------------------------------------------------------|------------|
| [<span data-ttu-id="e7a2e-170">**ID3D12CommandQueue**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-170">**ID3D12CommandQueue**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)                            |            |
| [<span data-ttu-id="e7a2e-171">**ID3D12CommandAllocator**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-171">**ID3D12CommandAllocator**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)                    |            |
| [<span data-ttu-id="e7a2e-172">**ID3D12GraphicsCommandList**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-172">**ID3D12GraphicsCommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)              |            |
| [<span data-ttu-id="e7a2e-173">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-173">**ID3D12Fence**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)                                          |            |
| [<span data-ttu-id="e7a2e-174">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-174">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="e7a2e-175">**Chiudi**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-175">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)                            |            |
| [<span data-ttu-id="e7a2e-176">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-176">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                              |            |
| [<span data-ttu-id="e7a2e-177">**Oggetti executecommandlist**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-177">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)       |            |
| [<span data-ttu-id="e7a2e-178">**InterlockedIncrement**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-178">**InterlockedIncrement**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedincrement)                     |            |
| [<span data-ttu-id="e7a2e-179">**Segnale**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-179">**Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                                 |            |
| [<span data-ttu-id="e7a2e-180">**SetEventOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-180">**SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)            |            |
| [<span data-ttu-id="e7a2e-181">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-181">**WaitForSingleObject**</span></span>](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)                         |            |
| [<span data-ttu-id="e7a2e-182">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-182">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="e7a2e-183">**GetCompletedValue**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-183">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)                  |            |
| [<span data-ttu-id="e7a2e-184">**Attesa**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-184">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                     |            |
| [<span data-ttu-id="e7a2e-185">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-185">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                       |            |
| [<span data-ttu-id="e7a2e-186">**ID3D12CommandAllocator:: Reset**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-186">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)       |            |
| [<span data-ttu-id="e7a2e-187">**ID3D12GraphicsCommandList:: Reset**</span><span class="sxs-lookup"><span data-stu-id="e7a2e-187">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) |            |



 

## <a name="run-the-sample"></a><span data-ttu-id="e7a2e-188">Eseguire l'esempio</span><span class="sxs-lookup"><span data-stu-id="e7a2e-188">Run the sample</span></span>

![screenshot della simulazione della gravità del corpo n finale](images/nbodygravity.png)

## <a name="related-topics"></a><span data-ttu-id="e7a2e-190">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7a2e-190">Related topics</span></span>

[<span data-ttu-id="e7a2e-191">Procedure dettagliate per il codice D3D12</span><span class="sxs-lookup"><span data-stu-id="e7a2e-191">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)

[<span data-ttu-id="e7a2e-192">Sincronizzazione multimotore</span><span class="sxs-lookup"><span data-stu-id="e7a2e-192">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)