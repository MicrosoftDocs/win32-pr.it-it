---
title: Creazione di un grafico di collegamento di funzioni e collegamento al codice compilato
description: Qui viene illustrato come creare grafici di collegamento a funzioni (FLGs) per gli shader e come collegare gli shader a una libreria shader per produrre BLOB dello shader che possono essere usati dal runtime Direct3D.
ms.assetid: 82C3109E-8571-49D2-A8BF-298E30E1281B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c037e7ea111d11d24df173ffba7e56c8f486af82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872790"
---
# <a name="constructing-a-function-linking-graph-and-linking-it-to-compiled-code"></a><span data-ttu-id="c6099-103">Creazione di un grafico di collegamento di funzioni e collegamento al codice compilato</span><span class="sxs-lookup"><span data-stu-id="c6099-103">Constructing a function-linking-graph and linking it to compiled code</span></span>

<span data-ttu-id="c6099-104">Qui viene illustrato come creare grafici di collegamento a funzioni (FLGs) per gli shader e come collegare gli shader a una libreria shader per produrre BLOB dello shader che possono essere usati dal runtime Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c6099-104">Here we show you how to construct function-linking-graphs (FLGs) for shaders and how to link those shaders with a shader library to produce shader blobs that the Direct3D runtime can use.</span></span>

<span data-ttu-id="c6099-105">**Obiettivo:** Per costruire un grafo di collegamento di funzione e collegarlo al codice compilato.</span><span class="sxs-lookup"><span data-stu-id="c6099-105">**Objective:** To construct a function-linking-graph and link it to compiled code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c6099-106">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="c6099-106">Prerequisites</span></span>

<span data-ttu-id="c6099-107">Partiamo dal presupposto che tu abbia familiarità con C++.</span><span class="sxs-lookup"><span data-stu-id="c6099-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="c6099-108">Devi inoltre avere un'esperienza di base dei concetti di programmazione di grafica.</span><span class="sxs-lookup"><span data-stu-id="c6099-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="c6099-109">Si presuppone anche che sia stata illustrata la creazione del [pacchetto di una libreria shader](pachaging-a-shader-library.md).</span><span class="sxs-lookup"><span data-stu-id="c6099-109">We also assume that you went through [Packaging a shader library](pachaging-a-shader-library.md).</span></span>

<span data-ttu-id="c6099-110">**Tempo necessario per il completamento:** 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="c6099-110">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="c6099-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c6099-111">Instructions</span></span>

### <a name="1-construct-a-function-linking-graph-for-the-vertex-shader"></a><span data-ttu-id="c6099-112">1. costruire un grafo di collegamento di funzione per il vertex shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-112">1. Construct a function-linking-graph for the vertex shader.</span></span>

<span data-ttu-id="c6099-113">Chiamare la funzione [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) per creare un [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)(Function-linking-Graph) per rappresentare il vertex shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-113">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the vertex shader.</span></span>

<span data-ttu-id="c6099-114">Usare una matrice di [**strutture \_ \_ Desc del parametro d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) per definire i parametri di input per il vertex shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-114">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the vertex shader.</span></span> <span data-ttu-id="c6099-115">La [fase input-assembler](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) inserisce i parametri di input per il vertex shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-115">The [Input-Assembler Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) feeds the input parameters to the vertex shader.</span></span> <span data-ttu-id="c6099-116">Il layout dei parametri di input del vertex shader corrisponde al layout del vertex shader nel codice compilato.</span><span class="sxs-lookup"><span data-stu-id="c6099-116">The layout of the vertex shader’s input parameters matches the layout of the vertex shader in the compiled code.</span></span> <span data-ttu-id="c6099-117">Dopo aver definito i parametri di input, chiamare il metodo [**ID3D11FunctionLinkingGraph:: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) per definire il nodo di input ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) per il vertex shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-117">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


```C++
            ComPtr<ID3D11FunctionLinkingGraph> vertexShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &vertexShaderGraph));

            // Define the main input node which will be fed by the Input Assembler pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderInputParameters[] =
            {
                {"inputPos",  "POSITION0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputTex",  "TEXCOORD0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderInputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetInputSignature(vertexShaderInputParameters, ARRAYSIZE(vertexShaderInputParameters), 
                &vertexShaderInputNode), vertexShaderGraph.Get());
```



<span data-ttu-id="c6099-118">Chiamare il metodo [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) per creare un nodo per la funzione vertex shader principale ed effettuare chiamate a [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) per passare i valori dal nodo di input al nodo per la funzione vertex shader principale.</span><span class="sxs-lookup"><span data-stu-id="c6099-118">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main vertex shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main vertex shader function.</span></span>


```C++
            // Create a node for the main VertexFunction call using the output of the helper functions.
            ComPtr<ID3D11LinkingNode> vertexFunctionCallNode;
            LinkingThrowIfFailed(vertexShaderGraph->CallFunction("", shaderLibrary.Get(), "VertexFunction", &vertexFunctionCallNode), 
                vertexShaderGraph.Get());

            // Define the graph edges from the input node and helper function nodes.
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForPos.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 0), vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexShaderInputNode.Get(), 1, vertexFunctionCallNode.Get(), 1), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForNorm.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 2), vertexShaderGraph.Get());
```



<span data-ttu-id="c6099-119">Usare una matrice di [**strutture \_ \_ Desc del parametro d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) per definire i parametri di output per il vertex shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-119">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the vertex shader.</span></span> <span data-ttu-id="c6099-120">Il vertex shader inserisce i parametri di output nel pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-120">The vertex shader feeds its output parameters to the pixel shader.</span></span> <span data-ttu-id="c6099-121">Il layout dei parametri di output del vertex shader corrisponde al layout del pixel shader nel codice compilato.</span><span class="sxs-lookup"><span data-stu-id="c6099-121">The layout of the vertex shader’s output parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="c6099-122">Dopo aver definito i parametri di output, chiamare il metodo [**ID3D11FunctionLinkingGraph:: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) per definire il nodo di output ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) per il vertex shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-122">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


```C++
            // Define the main output node which will feed the Pixel Shader pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderOutputParameters[] =
            {
                {"outputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderOutputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetOutputSignature(vertexShaderOutputParameters, ARRAYSIZE(vertexShaderOutputParameters), 
                &vertexShaderOutputNode), vertexShaderGraph.Get());
```



<span data-ttu-id="c6099-123">Effettuare chiamate a [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) per passare i valori dal nodo per la funzione vertex shader principale al nodo di output.</span><span class="sxs-lookup"><span data-stu-id="c6099-123">Make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the node for the main vertex shader function to the output node.</span></span>


```C++
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 0, vertexShaderOutputNode.Get(), 2), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 1, vertexShaderOutputNode.Get(), 0), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 2, vertexShaderOutputNode.Get(), 1), 
                vertexShaderGraph.Get());
```



<span data-ttu-id="c6099-124">Chiamare il metodo [**ID3D11FunctionLinkingGraph:: CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) per finalizzare il grafo del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-124">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the vertex shader graph.</span></span>


```C++
            // Finalize the vertex shader graph.
            ComPtr<ID3D11ModuleInstance> vertexShaderGraphInstance;
            LinkingThrowIfFailed(vertexShaderGraph->CreateModuleInstance(&vertexShaderGraphInstance, nullptr), vertexShaderGraph.Get());
```



### <a name="2-link-the-vertex-shader"></a><span data-ttu-id="c6099-125">2. Collegare il vertex shader</span><span class="sxs-lookup"><span data-stu-id="c6099-125">2. Link the vertex shader</span></span>

<span data-ttu-id="c6099-126">Chiamare la funzione [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) per creare un linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) che è possibile usare per collegare l'istanza della libreria shader creata nel [pacchetto di una libreria shader](pachaging-a-shader-library.md) con l'istanza del grafico vertex shader creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="c6099-126">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the vertex shader graph that you created in the preceding step.</span></span> <span data-ttu-id="c6099-127">Chiamare il metodo [**ID3D11Linker:: UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) per specificare la libreria dello shader da usare per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="c6099-127">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="c6099-128">Chiamare il metodo [**ID3D11Linker:: link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) per collegare la libreria dello shader al grafico vertex shader e produrre un puntatore all'interfaccia [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) che è possibile usare per accedere al codice del vertex shader compilato.</span><span class="sxs-lookup"><span data-stu-id="c6099-128">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the vertex shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled vertex shader code.</span></span> <span data-ttu-id="c6099-129">È quindi possibile passare il codice vertex shader compilato al metodo [**ID3D11Device:: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) per creare l'oggetto vertex shader e il metodo [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) per creare l'oggetto di layout di input.</span><span class="sxs-lookup"><span data-stu-id="c6099-129">You can then pass this compiled vertex shader code to the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method to create the vertex shader object and to the [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) method to create the input-layout object.</span></span>


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the vertex shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(vertexShaderGraphInstance.Get(), "main", ("vs" + m_shaderModelSuffix).c_str(), 0, &vertexShaderBlob, 
                &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11VertexShader> vertexShader;
    DX::ThrowIfFailed(
        device->CreateVertexShader(
            vertexShaderBlob->GetBufferPointer(),
            vertexShaderBlob->GetBufferSize(),
            nullptr,
            &vertexShader
            )
        );
    context->VSSetShader(vertexShader.Get(), nullptr, 0);
    D3D11_INPUT_ELEMENT_DESC inputLayoutDesc[] =
    {
        { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0,  D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT,    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "NORMAL",   0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, D3D11_INPUT_PER_VERTEX_DATA, 0 }
    };
    ComPtr<ID3D11InputLayout> inputLayout;
    DX::ThrowIfFailed(device->CreateInputLayout(inputLayoutDesc, ARRAYSIZE(inputLayoutDesc), vertexShaderBlob->GetBufferPointer(), vertexShaderBlob->GetBufferSize(), &inputLayout));
    context->IASetInputLayout(inputLayout.Get());
```



### <a name="3-construct-a-function-linking-graph-for-the-pixel-shader"></a><span data-ttu-id="c6099-130">3. creare un grafico di collegamento a funzioni per la pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-130">3. Construct a function-linking-graph for the pixel shader.</span></span>

<span data-ttu-id="c6099-131">Chiamare la funzione [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) per creare un [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)(Function-linking-Graph) per rappresentare il pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-131">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the pixel shader.</span></span>

<span data-ttu-id="c6099-132">Usare una matrice di [**strutture \_ \_ Desc del parametro d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) per definire i parametri di input per la pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-132">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the pixel shader.</span></span> <span data-ttu-id="c6099-133">La fase vertex shader inserisce i parametri di input per la pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-133">The vertex shader stage feeds the input parameters to the pixel shader.</span></span> <span data-ttu-id="c6099-134">Il layout dei parametri di input del pixel shader corrisponde al layout della pixel shader nel codice compilato.</span><span class="sxs-lookup"><span data-stu-id="c6099-134">The layout of the pixel shader’s input parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="c6099-135">Dopo aver definito i parametri di input, chiamare il metodo [**ID3D11FunctionLinkingGraph:: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) per definire il nodo di input ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) per la pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-135">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader.</span></span>


```C++
            ComPtr<ID3D11FunctionLinkingGraph> pixelShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &pixelShaderGraph));

            // Define the main input node which will be fed by the vertex shader pipeline stage.
            static const D3D11_PARAMETER_DESC pixelShaderInputParameters[] =
            {
                {"inputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderInputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetInputSignature(pixelShaderInputParameters, ARRAYSIZE(pixelShaderInputParameters), 
                &pixelShaderInputNode), pixelShaderGraph.Get());
```



<span data-ttu-id="c6099-136">Chiamare il metodo [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) per creare un nodo per la funzione pixel shader principale ed effettuare chiamate a [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) per passare i valori dal nodo di input al nodo per la funzione pixel shader principale.</span><span class="sxs-lookup"><span data-stu-id="c6099-136">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main pixel shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main pixel shader function.</span></span>


```C++
            // Create a node for the main ColorFunction call and connect it to the pixel shader inputs.
            ComPtr<ID3D11LinkingNode> colorValueNode;
            LinkingThrowIfFailed(pixelShaderGraph->CallFunction("", shaderLibrary.Get(), "ColorFunction", &colorValueNode), 
                pixelShaderGraph.Get());

            // Define the graph edges from the input node.
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 0, colorValueNode.Get(), 0), 
                pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 1, colorValueNode.Get(), 1), 
                pixelShaderGraph.Get());
```



<span data-ttu-id="c6099-137">Usare una matrice di [**strutture \_ \_ Desc del parametro d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) per definire i parametri di output per la pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-137">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the pixel shader.</span></span> <span data-ttu-id="c6099-138">Il pixel shader inserisce i parametri di output nella [fase di Unione dell'output](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage).</span><span class="sxs-lookup"><span data-stu-id="c6099-138">The pixel shader feeds its output parameters to the [Output-Merger Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage).</span></span> <span data-ttu-id="c6099-139">Dopo aver definito i parametri di output, chiamare il metodo [**ID3D11FunctionLinkingGraph:: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) per definire il nodo di output ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) per la pixel shader ed effettuare chiamate a [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) per passare i valori da un nodo della funzione pixel shader al nodo di output.</span><span class="sxs-lookup"><span data-stu-id="c6099-139">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from a pixel shader function node to the output node.</span></span>


```C++
            // Define the main output node which will feed the Output Merger pipeline stage.
            D3D11_PARAMETER_DESC pixelShaderOutputParameters[] =
            {
                {"outputColor", "SV_TARGET", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderOutputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetOutputSignature(pixelShaderOutputParameters, ARRAYSIZE(pixelShaderOutputParameters), 
                &pixelShaderOutputNode), pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(fillAlphaCallNode.Get(), D3D_RETURN_PARAMETER_INDEX, pixelShaderOutputNode.Get(), 0), 
                pixelShaderGraph.Get());
```



<span data-ttu-id="c6099-140">Chiamare il metodo [**ID3D11FunctionLinkingGraph:: CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) per finalizzare la pixel shader Graph.</span><span class="sxs-lookup"><span data-stu-id="c6099-140">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the pixel shader graph.</span></span>


```C++
            // Finalize the pixel shader graph.
            ComPtr<ID3D11ModuleInstance> pixelShaderGraphInstance;
            LinkingThrowIfFailed(pixelShaderGraph->CreateModuleInstance(&pixelShaderGraphInstance, nullptr), pixelShaderGraph.Get());
```



### <a name="4-link-the-pixel-shader"></a><span data-ttu-id="c6099-141">4. Collegare il pixel shader</span><span class="sxs-lookup"><span data-stu-id="c6099-141">4. Link the pixel shader</span></span>

<span data-ttu-id="c6099-142">Chiamare la funzione [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) per creare un linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) che è possibile usare per collegare l'istanza della libreria shader creata nel [pacchetto di una libreria shader](pachaging-a-shader-library.md) con l'istanza del grafico pixel shader creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="c6099-142">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the pixel shader graph that you created in the preceding step.</span></span> <span data-ttu-id="c6099-143">Chiamare il metodo [**ID3D11Linker:: UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) per specificare la libreria dello shader da usare per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="c6099-143">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="c6099-144">Chiamare il metodo [**ID3D11Linker:: link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) per collegare la libreria dello shader al grafico pixel shader e per produrre un puntatore all'interfaccia [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) che è possibile usare per accedere al codice pixel shader compilato.</span><span class="sxs-lookup"><span data-stu-id="c6099-144">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the pixel shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled pixel shader code.</span></span> <span data-ttu-id="c6099-145">È quindi possibile passare questo codice pixel shader compilato al metodo [**ID3D11Device:: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) per creare l'oggetto pixel shader.</span><span class="sxs-lookup"><span data-stu-id="c6099-145">You can then pass this compiled pixel shader code to the [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) method to create the pixel shader object.</span></span>


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the pixel shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(pixelShaderGraphInstance.Get(), "main", ("ps" + m_shaderModelSuffix).c_str(), 0, &pixelShaderBlob, &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11PixelShader> pixelShader;
    DX::ThrowIfFailed(
        device->CreatePixelShader(
            pixelShaderBlob->GetBufferPointer(),
            pixelShaderBlob->GetBufferSize(),
            nullptr,
            &pixelShader
            )
        );
    context->PSSetShader(pixelShader.Get(), nullptr, 0);
```



## <a name="summary"></a><span data-ttu-id="c6099-146">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="c6099-146">Summary</span></span>

<span data-ttu-id="c6099-147">Sono stati usati i metodi [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) per costruire i grafici vertex e pixel shader e per specificare la struttura dello shader a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="c6099-147">We used the [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) methods to construct the vertex and pixel shader graphs and to specify the shader structure programmatically.</span></span>

<span data-ttu-id="c6099-148">Queste costruzioni di grafici sono costituite da sequenze di chiamate di funzione precompilate che passano i valori l'uno all'altro.</span><span class="sxs-lookup"><span data-stu-id="c6099-148">These graph constructions consist of sequences of precompiled function calls that pass values to each other.</span></span> <span data-ttu-id="c6099-149">I nodi FLG ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) rappresentano i nodi shader di input e output e le chiamate delle funzioni della libreria precompilata.</span><span class="sxs-lookup"><span data-stu-id="c6099-149">FLG nodes ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) represent input and output shader nodes and invocations of precompiled library functions.</span></span> <span data-ttu-id="c6099-150">L'ordine in cui si registrano i nodi della chiamata di funzione definisce la sequenza di chiamate.</span><span class="sxs-lookup"><span data-stu-id="c6099-150">The order in which you register the function-call nodes defines the sequence of invocations.</span></span> <span data-ttu-id="c6099-151">È necessario specificare prima il nodo di input ([**ID3D11FunctionLinkingGraph:: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) e il nodo di output per ultimo ([**ID3D11FunctionLinkingGraph:: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)).</span><span class="sxs-lookup"><span data-stu-id="c6099-151">You must specify the input node ([**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) first and the output node last ([**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)).</span></span> <span data-ttu-id="c6099-152">I bordi di FLG definiscono il modo in cui i valori vengono passati da un nodo a un altro.</span><span class="sxs-lookup"><span data-stu-id="c6099-152">FLG edges define how values are passed from one node to another.</span></span> <span data-ttu-id="c6099-153">I tipi di dati dei valori passati devono essere uguali. non esiste alcuna conversione implicita di tipi.</span><span class="sxs-lookup"><span data-stu-id="c6099-153">The data types of passed values must be the same; there is no implicit type conversion.</span></span> <span data-ttu-id="c6099-154">Le regole Shape e swizzling seguono il comportamento di HLSL.</span><span class="sxs-lookup"><span data-stu-id="c6099-154">Shape and swizzling rules follow the HLSL behavior.</span></span> <span data-ttu-id="c6099-155">I valori possono essere passati solo in futuro in questa sequenza.</span><span class="sxs-lookup"><span data-stu-id="c6099-155">Values can only be passed forward in this sequence.</span></span>

<span data-ttu-id="c6099-156">Sono stati inoltre usati i metodi [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) per collegare la libreria dello shader ai grafici dello shader e per produrre BLOB dello shader per il runtime Direct3D da usare.</span><span class="sxs-lookup"><span data-stu-id="c6099-156">We also used [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) methods to link the shader library with the shader graphs and to produce shader blobs for the Direct3D runtime to use.</span></span>

<span data-ttu-id="c6099-157">Congratulazioni!</span><span class="sxs-lookup"><span data-stu-id="c6099-157">Congratulations!</span></span> <span data-ttu-id="c6099-158">A questo punto è possibile usare il collegamento dello shader nelle proprie app.</span><span class="sxs-lookup"><span data-stu-id="c6099-158">You are now ready to use shader linking in your own apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6099-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6099-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6099-160">Uso del collegamento shader</span><span class="sxs-lookup"><span data-stu-id="c6099-160">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 