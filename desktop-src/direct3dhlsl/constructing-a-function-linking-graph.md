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
# <a name="constructing-a-function-linking-graph-and-linking-it-to-compiled-code"></a>Creazione di un grafico di collegamento di funzioni e collegamento al codice compilato

Qui viene illustrato come creare grafici di collegamento a funzioni (FLGs) per gli shader e come collegare gli shader a una libreria shader per produrre BLOB dello shader che possono essere usati dal runtime Direct3D.

**Obiettivo:** Per costruire un grafo di collegamento di funzione e collegarlo al codice compilato.

## <a name="prerequisites"></a>Prerequisiti

Partiamo dal presupposto che tu abbia familiarità con C++. Devi inoltre avere un'esperienza di base dei concetti di programmazione di grafica.

Si presuppone anche che sia stata illustrata la creazione del [pacchetto di una libreria shader](pachaging-a-shader-library.md).

**Tempo necessario per il completamento:** 30 minuti.

## <a name="instructions"></a>Istruzioni

### <a name="1-construct-a-function-linking-graph-for-the-vertex-shader"></a>1. costruire un grafo di collegamento di funzione per il vertex shader.

Chiamare la funzione [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) per creare un [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)(Function-linking-Graph) per rappresentare il vertex shader.

Usare una matrice di [**strutture \_ \_ Desc del parametro d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) per definire i parametri di input per il vertex shader. La [fase input-assembler](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) inserisce i parametri di input per il vertex shader. Il layout dei parametri di input del vertex shader corrisponde al layout del vertex shader nel codice compilato. Dopo aver definito i parametri di input, chiamare il metodo [**ID3D11FunctionLinkingGraph:: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) per definire il nodo di input ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) per il vertex shader.


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



Chiamare il metodo [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) per creare un nodo per la funzione vertex shader principale ed effettuare chiamate a [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) per passare i valori dal nodo di input al nodo per la funzione vertex shader principale.


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



Usare una matrice di [**strutture \_ \_ Desc del parametro d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) per definire i parametri di output per il vertex shader. Il vertex shader inserisce i parametri di output nel pixel shader. Il layout dei parametri di output del vertex shader corrisponde al layout del pixel shader nel codice compilato. Dopo aver definito i parametri di output, chiamare il metodo [**ID3D11FunctionLinkingGraph:: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) per definire il nodo di output ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) per il vertex shader.


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



Effettuare chiamate a [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) per passare i valori dal nodo per la funzione vertex shader principale al nodo di output.


```C++
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 0, vertexShaderOutputNode.Get(), 2), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 1, vertexShaderOutputNode.Get(), 0), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 2, vertexShaderOutputNode.Get(), 1), 
                vertexShaderGraph.Get());
```



Chiamare il metodo [**ID3D11FunctionLinkingGraph:: CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) per finalizzare il grafo del vertex shader.


```C++
            // Finalize the vertex shader graph.
            ComPtr<ID3D11ModuleInstance> vertexShaderGraphInstance;
            LinkingThrowIfFailed(vertexShaderGraph->CreateModuleInstance(&vertexShaderGraphInstance, nullptr), vertexShaderGraph.Get());
```



### <a name="2-link-the-vertex-shader"></a>2. Collegare il vertex shader

Chiamare la funzione [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) per creare un linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) che è possibile usare per collegare l'istanza della libreria shader creata nel [pacchetto di una libreria shader](pachaging-a-shader-library.md) con l'istanza del grafico vertex shader creato nel passaggio precedente. Chiamare il metodo [**ID3D11Linker:: UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) per specificare la libreria dello shader da usare per il collegamento. Chiamare il metodo [**ID3D11Linker:: link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) per collegare la libreria dello shader al grafico vertex shader e produrre un puntatore all'interfaccia [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) che è possibile usare per accedere al codice del vertex shader compilato. È quindi possibile passare il codice vertex shader compilato al metodo [**ID3D11Device:: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) per creare l'oggetto vertex shader e il metodo [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) per creare l'oggetto di layout di input.


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



### <a name="3-construct-a-function-linking-graph-for-the-pixel-shader"></a>3. creare un grafico di collegamento a funzioni per la pixel shader.

Chiamare la funzione [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) per creare un [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)(Function-linking-Graph) per rappresentare il pixel shader.

Usare una matrice di [**strutture \_ \_ Desc del parametro d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) per definire i parametri di input per la pixel shader. La fase vertex shader inserisce i parametri di input per la pixel shader. Il layout dei parametri di input del pixel shader corrisponde al layout della pixel shader nel codice compilato. Dopo aver definito i parametri di input, chiamare il metodo [**ID3D11FunctionLinkingGraph:: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) per definire il nodo di input ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) per la pixel shader.


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



Chiamare il metodo [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) per creare un nodo per la funzione pixel shader principale ed effettuare chiamate a [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) per passare i valori dal nodo di input al nodo per la funzione pixel shader principale.


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



Usare una matrice di [**strutture \_ \_ Desc del parametro d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) per definire i parametri di output per la pixel shader. Il pixel shader inserisce i parametri di output nella [fase di Unione dell'output](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage). Dopo aver definito i parametri di output, chiamare il metodo [**ID3D11FunctionLinkingGraph:: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) per definire il nodo di output ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) per la pixel shader ed effettuare chiamate a [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) per passare i valori da un nodo della funzione pixel shader al nodo di output.


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



Chiamare il metodo [**ID3D11FunctionLinkingGraph:: CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) per finalizzare la pixel shader Graph.


```C++
            // Finalize the pixel shader graph.
            ComPtr<ID3D11ModuleInstance> pixelShaderGraphInstance;
            LinkingThrowIfFailed(pixelShaderGraph->CreateModuleInstance(&pixelShaderGraphInstance, nullptr), pixelShaderGraph.Get());
```



### <a name="4-link-the-pixel-shader"></a>4. Collegare il pixel shader

Chiamare la funzione [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) per creare un linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) che è possibile usare per collegare l'istanza della libreria shader creata nel [pacchetto di una libreria shader](pachaging-a-shader-library.md) con l'istanza del grafico pixel shader creato nel passaggio precedente. Chiamare il metodo [**ID3D11Linker:: UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) per specificare la libreria dello shader da usare per il collegamento. Chiamare il metodo [**ID3D11Linker:: link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) per collegare la libreria dello shader al grafico pixel shader e per produrre un puntatore all'interfaccia [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) che è possibile usare per accedere al codice pixel shader compilato. È quindi possibile passare questo codice pixel shader compilato al metodo [**ID3D11Device:: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) per creare l'oggetto pixel shader.


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



## <a name="summary"></a>Riepilogo

Sono stati usati i metodi [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) per costruire i grafici vertex e pixel shader e per specificare la struttura dello shader a livello di codice.

Queste costruzioni di grafici sono costituite da sequenze di chiamate di funzione precompilate che passano i valori l'uno all'altro. I nodi FLG ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) rappresentano i nodi shader di input e output e le chiamate delle funzioni della libreria precompilata. L'ordine in cui si registrano i nodi della chiamata di funzione definisce la sequenza di chiamate. È necessario specificare prima il nodo di input ([**ID3D11FunctionLinkingGraph:: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) e il nodo di output per ultimo ([**ID3D11FunctionLinkingGraph:: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)). I bordi di FLG definiscono il modo in cui i valori vengono passati da un nodo a un altro. I tipi di dati dei valori passati devono essere uguali. non esiste alcuna conversione implicita di tipi. Le regole Shape e swizzling seguono il comportamento di HLSL. I valori possono essere passati solo in futuro in questa sequenza.

Sono stati inoltre usati i metodi [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) per collegare la libreria dello shader ai grafici dello shader e per produrre BLOB dello shader per il runtime Direct3D da usare.

Congratulazioni! A questo punto è possibile usare il collegamento dello shader nelle proprie app.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del collegamento shader](using-shader-linking.md)
</dt> </dl>

 

 