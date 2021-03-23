---
title: Creazione di un componente Direct3D 12 di base
description: In questo argomento viene descritto il flusso di chiamate per creare un componente Direct3D 12 di base.
ms.assetid: A0FB108B-15C1-42AD-9277-D5CB63FA8329
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: d0c7ead9ce67ee23a0668304a006d6cd67fb3d67
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "104758861"
---
# <a name="creating-a-basic-direct3d-12-component"></a><span data-ttu-id="58284-103">Creazione di un componente Direct3D 12 di base</span><span class="sxs-lookup"><span data-stu-id="58284-103">Creating a basic Direct3D 12 component</span></span>

> [!NOTE]
> <span data-ttu-id="58284-104">Vedere il repository [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) per gli esempi di grafica DirectX 12 che illustrano come creare applicazioni con utilizzo intensivo di grafica per Windows 10.</span><span class="sxs-lookup"><span data-stu-id="58284-104">See the [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) repo for DirectX 12 Graphics samples that demonstrate how to build graphics-intensive applications for Windows 10.</span></span>

<span data-ttu-id="58284-105">In questo argomento viene descritto il flusso di chiamate per creare un componente Direct3D 12 di base.</span><span class="sxs-lookup"><span data-stu-id="58284-105">This topic describes the call flow to create a basic Direct3D 12 component.</span></span>

-   [<span data-ttu-id="58284-106">Flusso di codice per un'app semplice</span><span class="sxs-lookup"><span data-stu-id="58284-106">Code flow for a simple app</span></span>](#code-flow-for-a-simple-app)
    -   [<span data-ttu-id="58284-107">Inizializzare</span><span class="sxs-lookup"><span data-stu-id="58284-107">Initialize</span></span>](#initialize)
    -   [<span data-ttu-id="58284-108">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="58284-108">Update</span></span>](#update)
    -   [<span data-ttu-id="58284-109">Rendering</span><span class="sxs-lookup"><span data-stu-id="58284-109">Render</span></span>](#render)
    -   [<span data-ttu-id="58284-110">Eliminare</span><span class="sxs-lookup"><span data-stu-id="58284-110">Destroy</span></span>](#destroy)
-   [<span data-ttu-id="58284-111">Esempio di codice per un'app semplice</span><span class="sxs-lookup"><span data-stu-id="58284-111">Code example for a simple app</span></span>](#code-example-for-a-simple-app)
    -   [<span data-ttu-id="58284-112">Classe D3D12HelloTriangle</span><span class="sxs-lookup"><span data-stu-id="58284-112">class D3D12HelloTriangle</span></span>](#class-d3d12hellotriangle)
    -   [<span data-ttu-id="58284-113">OnInit ()</span><span class="sxs-lookup"><span data-stu-id="58284-113">OnInit()</span></span>](#oninit)
    -   [<span data-ttu-id="58284-114">LoadPipeline()</span><span class="sxs-lookup"><span data-stu-id="58284-114">LoadPipeline()</span></span>](#loadpipeline)
    -   [<span data-ttu-id="58284-115">LoadAssets()</span><span class="sxs-lookup"><span data-stu-id="58284-115">LoadAssets()</span></span>](#loadassets)
    -   [<span data-ttu-id="58284-116">OnUpdate ()</span><span class="sxs-lookup"><span data-stu-id="58284-116">OnUpdate()</span></span>](#onupdate)
    -   [<span data-ttu-id="58284-117">OnRender ()</span><span class="sxs-lookup"><span data-stu-id="58284-117">OnRender()</span></span>](#onrender)
    -   [<span data-ttu-id="58284-118">PopulateCommandList()</span><span class="sxs-lookup"><span data-stu-id="58284-118">PopulateCommandList()</span></span>](#populatecommandlist)
    -   [<span data-ttu-id="58284-119">WaitForPreviousFrame()</span><span class="sxs-lookup"><span data-stu-id="58284-119">WaitForPreviousFrame()</span></span>](#waitforpreviousframe)
    -   [<span data-ttu-id="58284-120">OnDestroy ()</span><span class="sxs-lookup"><span data-stu-id="58284-120">OnDestroy()</span></span>](#ondestroy)
-   [<span data-ttu-id="58284-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58284-121">Related topics</span></span>](#related-topics)

## <a name="code-flow-for-a-simple-app"></a><span data-ttu-id="58284-122">Flusso di codice per un'app semplice</span><span class="sxs-lookup"><span data-stu-id="58284-122">Code flow for a simple app</span></span>

<span data-ttu-id="58284-123">Il ciclo più esterno di un programma D3D 12 segue un processo grafico molto standard:</span><span class="sxs-lookup"><span data-stu-id="58284-123">The outermost loop of a D3D 12 program follows a very standard graphics process:</span></span>

> [!TIP]
> <span data-ttu-id="58284-124">Le nuove funzionalità di Direct3D 12 sono seguite da una nota.</span><span class="sxs-lookup"><span data-stu-id="58284-124">Features new to Direct3D 12 are followed by a note.</span></span>

-   [<span data-ttu-id="58284-125">Inizializzare</span><span class="sxs-lookup"><span data-stu-id="58284-125">Initialize</span></span>](#initialize)
-   <span data-ttu-id="58284-126">**Ripetere**</span><span class="sxs-lookup"><span data-stu-id="58284-126">**Repeat**</span></span>
    -   [<span data-ttu-id="58284-127">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="58284-127">Update</span></span>](#update)
    -   [<span data-ttu-id="58284-128">Rendering</span><span class="sxs-lookup"><span data-stu-id="58284-128">Render</span></span>](#render)
-   [<span data-ttu-id="58284-129">Eliminare</span><span class="sxs-lookup"><span data-stu-id="58284-129">Destroy</span></span>](#destroy)

### <a name="initialize"></a><span data-ttu-id="58284-130">Inizializzare</span><span class="sxs-lookup"><span data-stu-id="58284-130">Initialize</span></span>

<span data-ttu-id="58284-131">L'inizializzazione prevede innanzitutto la configurazione delle variabili e delle classi globali, mentre una funzione Initialize deve preparare la pipeline e gli asset.</span><span class="sxs-lookup"><span data-stu-id="58284-131">Initialization involves first setting up the global variables and classes, and an initialize function must prepare the pipeline and assets.</span></span>

-   <span data-ttu-id="58284-132">Inizializzare la pipeline.</span><span class="sxs-lookup"><span data-stu-id="58284-132">Initialize the pipeline.</span></span>
    -   <span data-ttu-id="58284-133">Abilitare il livello debug.</span><span class="sxs-lookup"><span data-stu-id="58284-133">Enable the debug layer.</span></span>
    -   <span data-ttu-id="58284-134">Creare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="58284-134">Create the device.</span></span>
    -   <span data-ttu-id="58284-135">Creare la coda dei comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-135">Create the command queue.</span></span>
    -   <span data-ttu-id="58284-136">Creare la catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="58284-136">Create the swap chain.</span></span>
    -   <span data-ttu-id="58284-137">Creare un heap del descrittore RTV (render target View).</span><span class="sxs-lookup"><span data-stu-id="58284-137">Create a render target view (RTV) descriptor heap.</span></span>
        > [!Note]  
        > <span data-ttu-id="58284-138">Un [heap del descrittore](descriptor-heaps.md) può essere considerato come una matrice di [descrittori](descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="58284-138">A [descriptor heap](descriptor-heaps.md) can be thought of as an array of [descriptors](descriptors.md).</span></span> <span data-ttu-id="58284-139">Dove ogni descrittore descrive completamente un oggetto alla GPU.</span><span class="sxs-lookup"><span data-stu-id="58284-139">Where each descriptor fully describes an object to the GPU.</span></span>

    -   <span data-ttu-id="58284-140">Creare risorse frame (visualizzazione della destinazione di rendering per ogni frame).</span><span class="sxs-lookup"><span data-stu-id="58284-140">Create frame resources (a render target view for each frame).</span></span>
    -   <span data-ttu-id="58284-141">Creare un allocatore di comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-141">Create a command allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="58284-142">Un allocatore di comandi gestisce l'archiviazione sottostante per gli [elenchi di comandi e i bundle](recording-command-lists-and-bundles.md).</span><span class="sxs-lookup"><span data-stu-id="58284-142">A command allocator manages the underlying storage for [command lists and bundles](recording-command-lists-and-bundles.md).</span></span>
         
-   <span data-ttu-id="58284-143">Inizializzare gli asset.</span><span class="sxs-lookup"><span data-stu-id="58284-143">Initialize the assets.</span></span>
    -   <span data-ttu-id="58284-144">Crea una firma radice vuota.</span><span class="sxs-lookup"><span data-stu-id="58284-144">Create an empty root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="58284-145">Una [firma radice](root-signatures.md) grafica definisce quali risorse sono associate alla pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="58284-145">A graphics [root signature](root-signatures.md) defines what resources are bound to the graphics pipeline.</span></span>

    -   <span data-ttu-id="58284-146">Compilare gli shader.</span><span class="sxs-lookup"><span data-stu-id="58284-146">Compile the shaders.</span></span>
    -   <span data-ttu-id="58284-147">Creare il layout di input vertice.</span><span class="sxs-lookup"><span data-stu-id="58284-147">Create the vertex input layout.</span></span>
    -   <span data-ttu-id="58284-148">Creare una descrizione dell' [oggetto stato della pipeline](managing-graphics-pipeline-state-in-direct3d-12.md) , quindi creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="58284-148">Create a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) description, then create the object.</span></span>
        > [!Note]  
        > <span data-ttu-id="58284-149">Un oggetto di stato della pipeline gestisce lo stato di tutti gli shader attualmente impostati, nonché alcuni oggetti di stato della funzione fissa, ad esempio l' *assembler di input*, *Tesselator*, *rasterizzatore* e *Unione di output*.</span><span class="sxs-lookup"><span data-stu-id="58284-149">A pipeline state object maintains the state of all currently set shaders as well as certain fixed function state objects (such as the *input assembler*, *tesselator*, *rasterizer* and *output merger*).</span></span>

    -   <span data-ttu-id="58284-150">Creare l'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-150">Create the command list.</span></span>
    -   <span data-ttu-id="58284-151">Chiudere l'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-151">Close the command list.</span></span>
    -   <span data-ttu-id="58284-152">Creare e caricare i buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="58284-152">Create and load the vertex buffers.</span></span>
    -   <span data-ttu-id="58284-153">Creare le visualizzazioni del buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="58284-153">Create the vertex buffer views.</span></span>
    -   <span data-ttu-id="58284-154">Creare una recinzione.</span><span class="sxs-lookup"><span data-stu-id="58284-154">Create a fence.</span></span>
        > [!Note]  
        > <span data-ttu-id="58284-155">Viene usata una recinzione per sincronizzare la CPU con la GPU (vedere [sincronizzazione multimotore](./user-mode-heap-synchronization.md)).</span><span class="sxs-lookup"><span data-stu-id="58284-155">A fence is used to synchronize the CPU with the GPU (see [Multi-engine synchronization](./user-mode-heap-synchronization.md)).</span></span>

    -   <span data-ttu-id="58284-156">Creare un handle di evento.</span><span class="sxs-lookup"><span data-stu-id="58284-156">Create an event handle.</span></span>
    -   <span data-ttu-id="58284-157">Attendere il completamento della GPU.</span><span class="sxs-lookup"><span data-stu-id="58284-157">Wait for the GPU to finish.</span></span>
        > [!Note]  
        > <span data-ttu-id="58284-158">Controllare la barriera.</span><span class="sxs-lookup"><span data-stu-id="58284-158">Check on the fence!</span></span>

<span data-ttu-id="58284-159">Vedere la [classe D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [LoadPipeline](#loadpipeline) e [LoadAssets](#loadassets).</span><span class="sxs-lookup"><span data-stu-id="58284-159">Refer to [class D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [LoadPipeline](#loadpipeline) and [LoadAssets](#loadassets).</span></span>

### <a name="update"></a><span data-ttu-id="58284-160">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="58284-160">Update</span></span>

<span data-ttu-id="58284-161">Aggiornare tutti gli elementi che devono essere modificati dall'ultimo frame.</span><span class="sxs-lookup"><span data-stu-id="58284-161">Update everything that should change since the last frame.</span></span>

-   <span data-ttu-id="58284-162">Modificare la costante, il vertice, i buffer di indice e tutti gli altri elementi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="58284-162">Modify the constant, vertex, index buffers, and everything else, as necessary.</span></span>

<span data-ttu-id="58284-163">Vedere [OnUpdate](#onupdate).</span><span class="sxs-lookup"><span data-stu-id="58284-163">Refer to [OnUpdate](#onupdate).</span></span>

### <a name="render"></a><span data-ttu-id="58284-164">Rendering</span><span class="sxs-lookup"><span data-stu-id="58284-164">Render</span></span>

<span data-ttu-id="58284-165">Creare il nuovo mondo.</span><span class="sxs-lookup"><span data-stu-id="58284-165">Draw the new world.</span></span>

-   <span data-ttu-id="58284-166">Popolare l'elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-166">Populate the command list.</span></span>
    -   <span data-ttu-id="58284-167">Reimpostare l'allocatore dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-167">Reset the command list allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="58284-168">Riutilizzare la memoria associata all'allocatore di comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-168">Re-use the memory that is associated with the command allocator.</span></span>

         

    -   <span data-ttu-id="58284-169">Reimpostare l'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-169">Reset the command list.</span></span>
    -   <span data-ttu-id="58284-170">Imposta la firma radice grafica.</span><span class="sxs-lookup"><span data-stu-id="58284-170">Set the graphics root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="58284-171">Imposta la firma radice grafica da usare per l'elenco di comandi corrente.</span><span class="sxs-lookup"><span data-stu-id="58284-171">Sets the graphics root signature to use for the current command list.</span></span>

         

    -   <span data-ttu-id="58284-172">Impostare il viewport e i rettangoli a forbice.</span><span class="sxs-lookup"><span data-stu-id="58284-172">Set the viewport and scissor rectangles.</span></span>
    -   <span data-ttu-id="58284-173">Impostare una barriera delle risorse, che indica che il buffer nascosto deve essere usato come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="58284-173">Set a resource barrier, indicating the back buffer is to be used as a render target.</span></span>
        > [!Note]  
        > <span data-ttu-id="58284-174">Le barriere delle risorse vengono usate per gestire le transizioni delle risorse.</span><span class="sxs-lookup"><span data-stu-id="58284-174">Resource barriers are used to manage resource transitions.</span></span>

         

    -   <span data-ttu-id="58284-175">Registrare i comandi nell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-175">Record commands into the command list.</span></span>
    -   <span data-ttu-id="58284-176">Indica che il buffer nascosto verrà usato per presentare dopo l'esecuzione dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-176">Indicate the back buffer will be used to present after the command list has executed.</span></span>
        > [!Note]  
        > <span data-ttu-id="58284-177">Un'altra chiamata per impostare una barriera delle risorse.</span><span class="sxs-lookup"><span data-stu-id="58284-177">Another call to set a resource barrier.</span></span>

         

    -   <span data-ttu-id="58284-178">Chiudere l'elenco dei comandi per eseguire ulteriori registrazioni.</span><span class="sxs-lookup"><span data-stu-id="58284-178">Close the command list to further recording.</span></span>
-   <span data-ttu-id="58284-179">Eseguire l'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-179">Execute the command list.</span></span>
-   <span data-ttu-id="58284-180">Presentare il frame.</span><span class="sxs-lookup"><span data-stu-id="58284-180">Present the frame.</span></span>
-   <span data-ttu-id="58284-181">Attendere il completamento della GPU.</span><span class="sxs-lookup"><span data-stu-id="58284-181">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="58284-182">Continua ad aggiornare e controllare la recinzione.</span><span class="sxs-lookup"><span data-stu-id="58284-182">Keep updating and checking the fence.</span></span>

<span data-ttu-id="58284-183">Vedere [OnRender](#onrender).</span><span class="sxs-lookup"><span data-stu-id="58284-183">Refer to [OnRender](#onrender).</span></span>

### <a name="destroy"></a><span data-ttu-id="58284-184">Destroy</span><span class="sxs-lookup"><span data-stu-id="58284-184">Destroy</span></span>

<span data-ttu-id="58284-185">Chiudere l'app in modo semplice.</span><span class="sxs-lookup"><span data-stu-id="58284-185">Cleanly close down the app.</span></span>

-   <span data-ttu-id="58284-186">Attendere il completamento della GPU.</span><span class="sxs-lookup"><span data-stu-id="58284-186">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="58284-187">Controllo finale sul perimetro.</span><span class="sxs-lookup"><span data-stu-id="58284-187">Final check on the fence.</span></span>

-   <span data-ttu-id="58284-188">Chiudere l'handle dell'evento.</span><span class="sxs-lookup"><span data-stu-id="58284-188">Close the event handle.</span></span>

<span data-ttu-id="58284-189">Vedere [OnDestroy](#ondestroy).</span><span class="sxs-lookup"><span data-stu-id="58284-189">Refer to [OnDestroy](#ondestroy).</span></span>

## <a name="code-example-for-a-simple-app"></a><span data-ttu-id="58284-190">Esempio di codice per un'app semplice</span><span class="sxs-lookup"><span data-stu-id="58284-190">Code example for a simple app</span></span>

<span data-ttu-id="58284-191">Il codice seguente espande il flusso del codice sopra riportato per includere il codice richiesto per un esempio di base.</span><span class="sxs-lookup"><span data-stu-id="58284-191">The following expands the code flow above to include the code required for a basic sample.</span></span>

### <a name="class-d3d12hellotriangle"></a><span data-ttu-id="58284-192">Classe D3D12HelloTriangle</span><span class="sxs-lookup"><span data-stu-id="58284-192">class D3D12HelloTriangle</span></span>

<span data-ttu-id="58284-193">Definire prima di tutto la classe in un file di intestazione, inclusi un viewport, un rettangolo a forbice e un buffer vertex usando le strutture:</span><span class="sxs-lookup"><span data-stu-id="58284-193">First define the class in a header file, including a viewport, scissor rectangle and vertex buffer using the structures:</span></span>

-   [<span data-ttu-id="58284-194">**\_Viewport D3D12**</span><span class="sxs-lookup"><span data-stu-id="58284-194">**D3D12\_VIEWPORT**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)
-   [<span data-ttu-id="58284-195">**D3D12 \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="58284-195">**D3D12\_RECT**</span></span>](d3d12-rect.md)
-   [<span data-ttu-id="58284-196">**\_ \_ Visualizzazione buffer vertex \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="58284-196">**D3D12\_VERTEX\_BUFFER\_VIEW**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)

```cpp
#include "DXSample.h"

using namespace DirectX;
using namespace Microsoft::WRL;

class D3D12HelloTriangle : public DXSample
{
public:
    D3D12HelloTriangle(UINT width, UINT height, std::wstring name);

    virtual void OnInit();
    virtual void OnUpdate();
    virtual void OnRender();
    virtual void OnDestroy();

private:
    static const UINT FrameCount = 2;

    struct Vertex
    {
        XMFLOAT3 position;
        XMFLOAT4 color;
    };

    // Pipeline objects.
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

    // App resources.
    ComPtr<ID3D12Resource> m_vertexBuffer;
    D3D12_VERTEX_BUFFER_VIEW m_vertexBufferView;

    // Synchronization objects.
    UINT m_frameIndex;
    HANDLE m_fenceEvent;
    ComPtr<ID3D12Fence> m_fence;
    UINT64 m_fenceValue;

    void LoadPipeline();
    void LoadAssets();
    void PopulateCommandList();
    void WaitForPreviousFrame();
};
```

### <a name="oninit"></a><span data-ttu-id="58284-197">OnInit ()</span><span class="sxs-lookup"><span data-stu-id="58284-197">OnInit()</span></span>

<span data-ttu-id="58284-198">Nel file di origine principale dei progetti avviare l'inizializzazione degli oggetti:</span><span class="sxs-lookup"><span data-stu-id="58284-198">In the projects main source file, start initializing the objects:</span></span>

```cpp
void D3D12HelloTriangle::OnInit()
{
    LoadPipeline();
    LoadAssets();
}
```

### <a name="loadpipeline"></a><span data-ttu-id="58284-199">LoadPipeline()</span><span class="sxs-lookup"><span data-stu-id="58284-199">LoadPipeline()</span></span>

<span data-ttu-id="58284-200">Il codice seguente crea le nozioni di base per una pipeline grafica.</span><span class="sxs-lookup"><span data-stu-id="58284-200">The following code creates the basics for a graphics pipeline.</span></span> <span data-ttu-id="58284-201">Il processo di creazione di dispositivi e catene di scambio è molto simile a Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="58284-201">The process of creating devices and swap chains is very similar to Direct3D 11.</span></span>

-   <span data-ttu-id="58284-202">Abilitare il livello di debug, con le chiamate a:</span><span class="sxs-lookup"><span data-stu-id="58284-202">Enable the debug layer, with calls to:</span></span><dl>

[<span data-ttu-id="58284-203">**D3D12GetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="58284-203">**D3D12GetDebugInterface**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12getdebuginterface)  
    [<span data-ttu-id="58284-204">**ID3D12Debug::EnableDebugLayer**</span><span class="sxs-lookup"><span data-stu-id="58284-204">**ID3D12Debug::EnableDebugLayer**</span></span>](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)  
    </dl>
-   <span data-ttu-id="58284-205">Creare il dispositivo:</span><span class="sxs-lookup"><span data-stu-id="58284-205">Create the device:</span></span><dl>

[<span data-ttu-id="58284-206">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="58284-206">**CreateDXGIFactory1**</span></span>](/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1)  
    [<span data-ttu-id="58284-207">**D3D12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="58284-207">**D3D12CreateDevice**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)  
    </dl>
-   <span data-ttu-id="58284-208">Compilare una descrizione della coda di comandi, quindi creare la coda dei comandi:</span><span class="sxs-lookup"><span data-stu-id="58284-208">Fill out a command queue description, then create the command queue:</span></span><dl>

[<span data-ttu-id="58284-209">**\_ \_ Descrizione coda comandi \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="58284-209">**D3D12\_COMMAND\_QUEUE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)  
    [<span data-ttu-id="58284-210">**ID3D12Device::CreateCommandQueue**</span><span class="sxs-lookup"><span data-stu-id="58284-210">**ID3D12Device::CreateCommandQueue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)  
    </dl>
-   <span data-ttu-id="58284-211">Compilare una descrizione presentazione catena, quindi creare la catena di scambio:</span><span class="sxs-lookup"><span data-stu-id="58284-211">Fill out a swapchain description, then create the swap chain:</span></span> <dl>

[<span data-ttu-id="58284-212">**\_ \_ desc catena di scambio DXGI \_**</span><span class="sxs-lookup"><span data-stu-id="58284-212">**DXGI\_SWAP\_CHAIN\_DESC**</span></span>](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)  
    [<span data-ttu-id="58284-213">**IDXGIFactory::CreateSwapChain**</span><span class="sxs-lookup"><span data-stu-id="58284-213">**IDXGIFactory::CreateSwapChain**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgifactory-createswapchain)  
    [<span data-ttu-id="58284-214">**IDXGISwapChain3::GetCurrentBackBufferIndex**</span><span class="sxs-lookup"><span data-stu-id="58284-214">**IDXGISwapChain3::GetCurrentBackBufferIndex**</span></span>](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)  
    </dl>
-   <span data-ttu-id="58284-215">Compilare una descrizione dell'heap.</span><span class="sxs-lookup"><span data-stu-id="58284-215">Fill out a heap description.</span></span> <span data-ttu-id="58284-216">creare quindi un heap del descrittore:</span><span class="sxs-lookup"><span data-stu-id="58284-216">then create a descriptor heap:</span></span> <dl>

[<span data-ttu-id="58284-217">**D3D12 \_ \_ Descrizione heap descrittore \_**</span><span class="sxs-lookup"><span data-stu-id="58284-217">**D3D12\_DESCRIPTOR\_HEAP\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)  
    [<span data-ttu-id="58284-218">**ID3D12Device::CreateDescriptorHeap**</span><span class="sxs-lookup"><span data-stu-id="58284-218">**ID3D12Device::CreateDescriptorHeap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)  
    [<span data-ttu-id="58284-219">**ID3D12Device::GetDescriptorHandleIncrementSize**</span><span class="sxs-lookup"><span data-stu-id="58284-219">**ID3D12Device::GetDescriptorHandleIncrementSize**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)  
    </dl>
-   <span data-ttu-id="58284-220">Creare la visualizzazione della destinazione di rendering:</span><span class="sxs-lookup"><span data-stu-id="58284-220">Create the render target view:</span></span> <dl>

[<span data-ttu-id="58284-221">**\_ \_ Handle descrittore CPU CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="58284-221">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE**</span></span>](cd3dx12-cpu-descriptor-handle.md)  
    [<span data-ttu-id="58284-222">**GetCPUDescriptorHandleForHeapStart**</span><span class="sxs-lookup"><span data-stu-id="58284-222">**GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="58284-223">**IDXGISwapChain:: GetBuffer**</span><span class="sxs-lookup"><span data-stu-id="58284-223">**IDXGISwapChain::GetBuffer**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)  
    [<span data-ttu-id="58284-224">**ID3D12Device::CreateRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="58284-224">**ID3D12Device::CreateRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)  
    </dl>
-   <span data-ttu-id="58284-225">Creare il comando allocator: [**ID3D12Device:: CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).</span><span class="sxs-lookup"><span data-stu-id="58284-225">Create the command allocator: [**ID3D12Device::CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).</span></span>

<span data-ttu-id="58284-226">Nei passaggi successivi gli elenchi di comandi vengono ottenuti dall'allocatore di comandi e inviati alla coda dei comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-226">In later steps, command lists are obtained from the command allocator and submitted to the command queue.</span></span>

<span data-ttu-id="58284-227">Caricare le dipendenze della pipeline di rendering (si noti che la creazione di un dispositivo WARP software è interamente facoltativa).</span><span class="sxs-lookup"><span data-stu-id="58284-227">Load the rendering pipeline dependencies (note that the creation of a software WARP device is entirely optional).</span></span>


```cpp
void D3D12HelloTriangle::LoadPipeline()
{
#if defined(_DEBUG)
    // Enable the D3D12 debug layer.
    {
        
        ComPtr<ID3D12Debug> debugController;
        if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&debugController))))
        {
            debugController->EnableDebugLayer();
        }
    }
#endif

    ComPtr<IDXGIFactory4> factory;
    ThrowIfFailed(CreateDXGIFactory1(IID_PPV_ARGS(&factory)));

    if (m_useWarpDevice)
    {
        ComPtr<IDXGIAdapter> warpAdapter;
        ThrowIfFailed(factory->EnumWarpAdapter(IID_PPV_ARGS(&warpAdapter)));

        ThrowIfFailed(D3D12CreateDevice(
            warpAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }
    else
    {
        ComPtr<IDXGIAdapter1> hardwareAdapter;
        GetHardwareAdapter(factory.Get(), &hardwareAdapter);

        ThrowIfFailed(D3D12CreateDevice(
            hardwareAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }

    // Describe and create the command queue.
    D3D12_COMMAND_QUEUE_DESC queueDesc = {};
    queueDesc.Flags = D3D12_COMMAND_QUEUE_FLAG_NONE;
    queueDesc.Type = D3D12_COMMAND_LIST_TYPE_DIRECT;

    ThrowIfFailed(m_device->CreateCommandQueue(&queueDesc, IID_PPV_ARGS(&m_commandQueue)));

    // Describe and create the swap chain.
    DXGI_SWAP_CHAIN_DESC swapChainDesc = {};
    swapChainDesc.BufferCount = FrameCount;
    swapChainDesc.BufferDesc.Width = m_width;
    swapChainDesc.BufferDesc.Height = m_height;
    swapChainDesc.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
    swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
    swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_DISCARD;
    swapChainDesc.OutputWindow = Win32Application::GetHwnd();
    swapChainDesc.SampleDesc.Count = 1;
    swapChainDesc.Windowed = TRUE;

    ComPtr<IDXGISwapChain> swapChain;
    ThrowIfFailed(factory->CreateSwapChain(
        m_commandQueue.Get(),        // Swap chain needs the queue so that it can force a flush on it.
        &swapChainDesc,
        &swapChain
        ));

    ThrowIfFailed(swapChain.As(&m_swapChain));

    // This sample does not support fullscreen transitions.
    ThrowIfFailed(factory->MakeWindowAssociation(Win32Application::GetHwnd(), DXGI_MWA_NO_ALT_ENTER));

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();

    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
            rtvHandle.Offset(1, m_rtvDescriptorSize);
        }
    }

    ThrowIfFailed(m_device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocator)));
}
```



### <a name="loadassets"></a><span data-ttu-id="58284-228">LoadAssets()</span><span class="sxs-lookup"><span data-stu-id="58284-228">LoadAssets()</span></span>

<span data-ttu-id="58284-229">Il caricamento e la preparazione degli asset è un processo lungo.</span><span class="sxs-lookup"><span data-stu-id="58284-229">Loading and preparing assets is a lengthy process.</span></span> <span data-ttu-id="58284-230">Molte di queste fasi sono simili a D3D 11, anche se alcune sono nuove per D3D 12.</span><span class="sxs-lookup"><span data-stu-id="58284-230">Many of these stages are similar to D3D 11, though some are new to D3D 12.</span></span>

<span data-ttu-id="58284-231">In Direct3D 12 lo stato della pipeline richiesto è associato a un elenco di comandi tramite un [oggetto di stato della pipeline](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO).</span><span class="sxs-lookup"><span data-stu-id="58284-231">In Direct3D 12, required pipeline state is attached to a command list via a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO).</span></span> <span data-ttu-id="58284-232">Questo esempio illustra come creare un oggetto PSO.</span><span class="sxs-lookup"><span data-stu-id="58284-232">This example shows how to create a PSO.</span></span> <span data-ttu-id="58284-233">È possibile archiviare l'oggetto PSO come variabile membro e riutilizzarlo il numero di volte necessario.</span><span class="sxs-lookup"><span data-stu-id="58284-233">You can store the PSO as a member variable and reuse it as many times as needed.</span></span>

<span data-ttu-id="58284-234">Un heap descrittore definisce le visualizzazioni e come accedere alle risorse, ad esempio una visualizzazione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="58284-234">A descriptor heap defines the views and how to access resources (for example, a render target view).</span></span>

<span data-ttu-id="58284-235">Con l'elenco dei comandi allocator e PSO, è possibile creare l'elenco di comandi effettivo, che verrà eseguito in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="58284-235">With the command list allocator and PSO, you can create the actual command list, which will be executed at a later time.</span></span>

<span data-ttu-id="58284-236">Le API e i processi seguenti vengono chiamati in successione.</span><span class="sxs-lookup"><span data-stu-id="58284-236">The following APIs and processes are called in succession.</span></span>

-   <span data-ttu-id="58284-237">Creare una firma radice vuota, usando la struttura Helper disponibile:</span><span class="sxs-lookup"><span data-stu-id="58284-237">Create an empty root signature, using the available helper structure:</span></span> <dl>

[<span data-ttu-id="58284-238">**\_Descrizione della \_ firma \_ radice CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="58284-238">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md)  
    [<span data-ttu-id="58284-239">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="58284-239">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)  
    [<span data-ttu-id="58284-240">**ID3D12Device::CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="58284-240">**ID3D12Device::CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)  
    </dl>
-   <span data-ttu-id="58284-241">Caricare e compilare gli shader: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).</span><span class="sxs-lookup"><span data-stu-id="58284-241">Load and compile the shaders: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).</span></span>
-   <span data-ttu-id="58284-242">Creare il layout di input del vertice: [**\_ elemento di input D3D12 \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="58284-242">Create the vertex input layout: [**D3D12\_INPUT\_ELEMENT\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).</span></span>
-   <span data-ttu-id="58284-243">Compilare una descrizione dello stato della pipeline, usando le strutture di supporto disponibili, quindi creare lo stato della pipeline grafica:</span><span class="sxs-lookup"><span data-stu-id="58284-243">Fill out a pipeline state description, using the helper structures available, then create the graphics pipeline state:</span></span> <dl>

[<span data-ttu-id="58284-244">**\_ \_ \_ Descrizione dello stato della pipeline grafica D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="58284-244">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)  
    [<span data-ttu-id="58284-245">**CD3DX12 \_ rasterizzatore \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="58284-245">**CD3DX12\_RASTERIZER\_DESC**</span></span>](cd3dx12-rasterizer-desc.md)  
    [<span data-ttu-id="58284-246">**CD3DX12 \_ Blend \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="58284-246">**CD3DX12\_BLEND\_DESC**</span></span>](cd3dx12-blend-desc.md)  
    [<span data-ttu-id="58284-247">**ID3D12Device::CreateGraphicsPipelineState**</span><span class="sxs-lookup"><span data-stu-id="58284-247">**ID3D12Device::CreateGraphicsPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)  
    </dl>
-   <span data-ttu-id="58284-248">Creare, quindi chiudere, un elenco di comandi:</span><span class="sxs-lookup"><span data-stu-id="58284-248">Create, then close, a command list:</span></span> <dl>

[<span data-ttu-id="58284-249">**ID3D12Device::CreateCommandList**</span><span class="sxs-lookup"><span data-stu-id="58284-249">**ID3D12Device::CreateCommandList**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)  
    [<span data-ttu-id="58284-250">**ID3D12GraphicsCommandList:: Close**</span><span class="sxs-lookup"><span data-stu-id="58284-250">**ID3D12GraphicsCommandList::Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)  
    </dl>
-   <span data-ttu-id="58284-251">Creare il buffer vertex: [**ID3D12Device:: CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="58284-251">Create the vertex buffer: [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>
-   <span data-ttu-id="58284-252">Copiare i dati dei vertici nel buffer dei vertici:</span><span class="sxs-lookup"><span data-stu-id="58284-252">Copy the vertex data to the vertex buffer:</span></span><dl>

[<span data-ttu-id="58284-253">**ID3D12Resource:: Map**</span><span class="sxs-lookup"><span data-stu-id="58284-253">**ID3D12Resource::Map**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)  
    [<span data-ttu-id="58284-254">**ID3D12Resource:: annullare**</span><span class="sxs-lookup"><span data-stu-id="58284-254">**ID3D12Resource::Unmap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-unmap)  
    </dl>
-   <span data-ttu-id="58284-255">Inizializzare la visualizzazione del buffer dei vertici: [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).</span><span class="sxs-lookup"><span data-stu-id="58284-255">Initialize the vertex buffer view: [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).</span></span>
-   <span data-ttu-id="58284-256">Creare e inizializzare la recinzione: [**ID3D12Device:: CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).</span><span class="sxs-lookup"><span data-stu-id="58284-256">Create and initialize the fence: [**ID3D12Device::CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).</span></span>
-   <span data-ttu-id="58284-257">Creare un handle di evento da usare con la sincronizzazione dei frame.</span><span class="sxs-lookup"><span data-stu-id="58284-257">Create an event handle for use with frame synchronization.</span></span>
-   <span data-ttu-id="58284-258">Attendere il completamento della GPU.</span><span class="sxs-lookup"><span data-stu-id="58284-258">Wait for the GPU to finish.</span></span>


```cpp
void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr<ID3DBlob> vertexShader;
        ComPtr<ID3DBlob> pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast<UINT8*>(vertexShader->GetBufferPointer()), vertexShader->GetBufferSize() };
        psoDesc.PS = { reinterpret_cast<UINT8*>(pixelShader->GetBufferPointer()), pixelShader->GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList->Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_UPLOAD);
        auto desc = CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize);
        ThrowIfFailed(m_device->CreateCommittedResource(
            &heapProps,
            D3D12_HEAP_FLAG_NONE,
            &desc,
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer->Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device->CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
```



### <a name="onupdate"></a><span data-ttu-id="58284-259">OnUpdate ()</span><span class="sxs-lookup"><span data-stu-id="58284-259">OnUpdate()</span></span>

<span data-ttu-id="58284-260">Per un semplice esempio, non viene aggiornato alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="58284-260">For a simple example, nothing is updated.</span></span>


```cpp
void D3D12HelloTriangle::OnUpdate()

{
}
```



### <a name="onrender"></a><span data-ttu-id="58284-261">OnRender ()</span><span class="sxs-lookup"><span data-stu-id="58284-261">OnRender()</span></span>

<span data-ttu-id="58284-262">Durante la configurazione, la variabile membro **m \_ Commanding** è stata usata per registrare ed eseguire tutti i comandi di configurazione.</span><span class="sxs-lookup"><span data-stu-id="58284-262">During set up, the member variable **m\_commandList** was used to record and execute all of the set up commands.</span></span> <span data-ttu-id="58284-263">È ora possibile riutilizzare il membro nel ciclo di rendering principale.</span><span class="sxs-lookup"><span data-stu-id="58284-263">You can now reuse that member in the main render loop.</span></span>

<span data-ttu-id="58284-264">Il rendering prevede una chiamata per popolare l'elenco di comandi, quindi l'elenco dei comandi può essere eseguito e il buffer successivo nella catena di scambio presenta:</span><span class="sxs-lookup"><span data-stu-id="58284-264">Rendering involves a call to populate the command list, then the command list can be executed and the next buffer in the swap chain presented:</span></span>

-   <span data-ttu-id="58284-265">Popolare l'elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-265">Populate the command list.</span></span>
-   <span data-ttu-id="58284-266">Eseguire l'elenco di comandi: [**ID3D12CommandQueue:: oggetti executecommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span><span class="sxs-lookup"><span data-stu-id="58284-266">Execute the command list: [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>
-   <span data-ttu-id="58284-267">[**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) il frame.</span><span class="sxs-lookup"><span data-stu-id="58284-267">[**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) the frame.</span></span>
-   <span data-ttu-id="58284-268">Attendere la fine della GPU.</span><span class="sxs-lookup"><span data-stu-id="58284-268">Wait on the GPU to finish.</span></span>


```cpp
void D3D12HelloTriangle::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(1, 0));

    WaitForPreviousFrame();
}
```



### <a name="populatecommandlist"></a><span data-ttu-id="58284-269">PopulateCommandList()</span><span class="sxs-lookup"><span data-stu-id="58284-269">PopulateCommandList()</span></span>

<span data-ttu-id="58284-270">È necessario reimpostare l'allocatore dell'elenco di comandi e l'elenco dei comandi prima di poterlo riutilizzare.</span><span class="sxs-lookup"><span data-stu-id="58284-270">You must reset the command list allocator and the command list itself before you can reuse them.</span></span> <span data-ttu-id="58284-271">Negli scenari più avanzati può essere utile reimpostare l'allocatore ogni più frame.</span><span class="sxs-lookup"><span data-stu-id="58284-271">In more advanced scenarios it might make sense to reset the allocator every several frames.</span></span> <span data-ttu-id="58284-272">La memoria è associata all'allocatore che non può essere rilasciata immediatamente dopo l'esecuzione di un elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-272">Memory is associated with the allocator that can't be released immediately after executing a command list.</span></span> <span data-ttu-id="58284-273">Questo esempio illustra come reimpostare l'allocatore dopo ogni frame.</span><span class="sxs-lookup"><span data-stu-id="58284-273">This example shows how to reset the allocator after every frame.</span></span>

<span data-ttu-id="58284-274">A questo punto, riutilizzare l'elenco dei comandi per il frame corrente.</span><span class="sxs-lookup"><span data-stu-id="58284-274">Now, reuse the command list for the current frame.</span></span> <span data-ttu-id="58284-275">Riassegnare il viewport all'elenco dei comandi (che deve essere eseguito ogni volta che viene reimpostato un elenco di comandi e prima che venga eseguito l'elenco dei comandi), indicare che la risorsa verrà utilizzata come destinazione di rendering, registrare i comandi e indicare che la destinazione di rendering verrà utilizzata per presentare al termine dell'esecuzione dell'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="58284-275">Reattach the viewport to the command list (which must be done whenever a command list is reset, and before the command list is executed), indicate that the resource will be in use as a render target, record commands, and then indicate that the render target will be used to present when the command list is done executing.</span></span>

<span data-ttu-id="58284-276">Il popolamento degli elenchi di comandi chiama a sua volta i metodi e i processi seguenti:</span><span class="sxs-lookup"><span data-stu-id="58284-276">Populating command lists calls the following methods and processes in turn:</span></span>

-   <span data-ttu-id="58284-277">Reimpostare l'allocatore di comandi e l'elenco dei comandi:</span><span class="sxs-lookup"><span data-stu-id="58284-277">Reset the command allocator, and command list:</span></span> <dl>

[<span data-ttu-id="58284-278">**ID3D12CommandAllocator:: Reset**</span><span class="sxs-lookup"><span data-stu-id="58284-278">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)  
    [<span data-ttu-id="58284-279">**ID3D12GraphicsCommandList:: Reset**</span><span class="sxs-lookup"><span data-stu-id="58284-279">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)  
    </dl>
-   <span data-ttu-id="58284-280">Impostare i rettangoli di firma radice, viewport e forbici:</span><span class="sxs-lookup"><span data-stu-id="58284-280">Set the root signature, viewport and scissors rectangles:</span></span> <dl>

[<span data-ttu-id="58284-281">**ID3D12GraphicsCommandList::SetGraphicsRootSignature**</span><span class="sxs-lookup"><span data-stu-id="58284-281">**ID3D12GraphicsCommandList::SetGraphicsRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature)  
    [<span data-ttu-id="58284-282">**ID3D12GraphicsCommandList::RSSetViewports**</span><span class="sxs-lookup"><span data-stu-id="58284-282">**ID3D12GraphicsCommandList::RSSetViewports**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)  
    [<span data-ttu-id="58284-283">**ID3D12GraphicsCommandList::RSSetScissorRects**</span><span class="sxs-lookup"><span data-stu-id="58284-283">**ID3D12GraphicsCommandList::RSSetScissorRects**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)  
    </dl>
-   <span data-ttu-id="58284-284">Indica che il buffer nascosto deve essere utilizzato come destinazione di rendering:</span><span class="sxs-lookup"><span data-stu-id="58284-284">Indicate that the back buffer is to be used as a render target:</span></span> <dl>

[<span data-ttu-id="58284-285">**ID3D12GraphicsCommandList::ResourceBarrier**</span><span class="sxs-lookup"><span data-stu-id="58284-285">**ID3D12GraphicsCommandList::ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)  
    [<span data-ttu-id="58284-286">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span><span class="sxs-lookup"><span data-stu-id="58284-286">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="58284-287">**ID3D12GraphicsCommandList::OMSetRenderTargets**</span><span class="sxs-lookup"><span data-stu-id="58284-287">**ID3D12GraphicsCommandList::OMSetRenderTargets**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)  
    </dl>
-   <span data-ttu-id="58284-288">Registrare i comandi:</span><span class="sxs-lookup"><span data-stu-id="58284-288">Record the commands:</span></span><dl>

[<span data-ttu-id="58284-289">**ID3D12GraphicsCommandList::ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="58284-289">**ID3D12GraphicsCommandList::ClearRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)  
    [<span data-ttu-id="58284-290">**ID3D12GraphicsCommandList::IASetPrimitiveTopology**</span><span class="sxs-lookup"><span data-stu-id="58284-290">**ID3D12GraphicsCommandList::IASetPrimitiveTopology**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)  
    [<span data-ttu-id="58284-291">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="58284-291">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)  
    [<span data-ttu-id="58284-292">**ID3D12GraphicsCommandList::D rawInstanced**</span><span class="sxs-lookup"><span data-stu-id="58284-292">**ID3D12GraphicsCommandList::DrawInstanced**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)  
    </dl>
-   <span data-ttu-id="58284-293">Indica che il buffer nascosto verrà ora usato per presentare: [**ID3D12GraphicsCommandList:: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="58284-293">Indicate the back buffer will now be used to present: [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>
-   <span data-ttu-id="58284-294">Chiudere l'elenco dei comandi: [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).</span><span class="sxs-lookup"><span data-stu-id="58284-294">Close the command list: [**ID3D12GraphicsCommandList::Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).</span></span>


```cpp
void D3D12HelloTriangle::PopulateCommandList()
{
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
    barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT);
    m_commandList->ResourceBarrier(1, &barrier);

    ThrowIfFailed(m_commandList->Close());
}
```



### <a name="waitforpreviousframe"></a><span data-ttu-id="58284-295">WaitForPreviousFrame()</span><span class="sxs-lookup"><span data-stu-id="58284-295">WaitForPreviousFrame()</span></span>

<span data-ttu-id="58284-296">Il codice seguente illustra un uso più semplificato delle recinzioni.</span><span class="sxs-lookup"><span data-stu-id="58284-296">The following code shows an over-simplified use of fences.</span></span>

> [!Note]  
> <span data-ttu-id="58284-297">In attesa del completamento di un frame è troppo inefficiente per la maggior parte delle app.</span><span class="sxs-lookup"><span data-stu-id="58284-297">Waiting for a frame to complete is too inefficient for most apps.</span></span>

 

<span data-ttu-id="58284-298">Le API e i processi seguenti vengono chiamati nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="58284-298">The following APIs and processes are called in order:</span></span>

-   [<span data-ttu-id="58284-299">**ID3D12CommandQueue:: Signal**</span><span class="sxs-lookup"><span data-stu-id="58284-299">**ID3D12CommandQueue::Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
-   [<span data-ttu-id="58284-300">**ID3D12Fence::GetCompletedValue**</span><span class="sxs-lookup"><span data-stu-id="58284-300">**ID3D12Fence::GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)
-   [<span data-ttu-id="58284-301">**ID3D12Fence::SetEventOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="58284-301">**ID3D12Fence::SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)
-   <span data-ttu-id="58284-302">Attendere l'evento.</span><span class="sxs-lookup"><span data-stu-id="58284-302">Wait for the event.</span></span>
-   <span data-ttu-id="58284-303">Aggiornare l'indice del frame: [**IDXGISwapChain3:: GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).</span><span class="sxs-lookup"><span data-stu-id="58284-303">Update the frame index: [**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).</span></span>


```cpp
void D3D12HelloTriangle::WaitForPreviousFrame()
{
    // WAITING FOR THE FRAME TO COMPLETE BEFORE CONTINUING IS NOT BEST PRACTICE.
    // This is code implemented as such for simplicity. More advanced samples 
    // illustrate how to use fences for efficient resource usage.

    // Signal and increment the fence value.
    const UINT64 fence = m_fenceValue;
    ThrowIfFailed(m_commandQueue->Signal(m_fence.Get(), fence));
    m_fenceValue++;

    // Wait until the previous frame is finished.
    if (m_fence->GetCompletedValue() < fence)
    {
        ThrowIfFailed(m_fence->SetEventOnCompletion(fence, m_fenceEvent));
        WaitForSingleObject(m_fenceEvent, INFINITE);
    }

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();
}
```



### <a name="ondestroy"></a><span data-ttu-id="58284-304">OnDestroy ()</span><span class="sxs-lookup"><span data-stu-id="58284-304">OnDestroy()</span></span>

<span data-ttu-id="58284-305">Chiudere l'app in modo semplice.</span><span class="sxs-lookup"><span data-stu-id="58284-305">Cleanly close down the app.</span></span>

-   <span data-ttu-id="58284-306">Attendere il completamento della GPU.</span><span class="sxs-lookup"><span data-stu-id="58284-306">Wait for the GPU to finish.</span></span>
-   <span data-ttu-id="58284-307">Chiudere l'evento.</span><span class="sxs-lookup"><span data-stu-id="58284-307">Close the event.</span></span>


```cpp
void D3D12HelloTriangle::OnDestroy()
{

    // Wait for the GPU to be done with all resources.
    WaitForPreviousFrame();

    CloseHandle(m_fenceEvent);
}
```



## <a name="related-topics"></a><span data-ttu-id="58284-308">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58284-308">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58284-309">Informazioni su Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="58284-309">Understanding Direct3D 12</span></span>](directx-12-getting-started.md)
</dt> <dt>

[<span data-ttu-id="58284-310">Esempi di lavoro</span><span class="sxs-lookup"><span data-stu-id="58284-310">Working Samples</span></span>](working-samples.md)
</dt> </dl>

 

 
