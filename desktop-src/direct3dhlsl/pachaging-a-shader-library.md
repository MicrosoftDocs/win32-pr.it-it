---
title: Creazione del pacchetto di una libreria shader
description: Qui viene illustrato come compilare il codice dello shader, caricare il codice compilato in una libreria shader e associare le risorse da slot di origine a slot di destinazione.
ms.assetid: ED2EB1DE-3C25-4633-BFA7-C535ABBBAD28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90124ca9753a390b924d5ba702e1986e32eee9e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993557"
---
# <a name="packaging-a-shader-library"></a><span data-ttu-id="8ad3e-103">Creazione del pacchetto di una libreria shader</span><span class="sxs-lookup"><span data-stu-id="8ad3e-103">Packaging a shader library</span></span>

<span data-ttu-id="8ad3e-104">Qui viene illustrato come compilare il codice dello shader, caricare il codice compilato in una libreria shader e associare le risorse da slot di origine a slot di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-104">Here we show you how to compile your shader code, load the compiled code into a shader library, and bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="8ad3e-105">**Obiettivo:** Per creare un pacchetto di una libreria shader da utilizzare per il collegamento dello shader.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-105">**Objective:** To package a shader library to use for shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8ad3e-106">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="8ad3e-106">Prerequisites</span></span>

<span data-ttu-id="8ad3e-107">Partiamo dal presupposto che tu abbia familiarità con C++.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="8ad3e-108">Devi inoltre avere un'esperienza di base dei concetti di programmazione di grafica.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="8ad3e-109">**Tempo necessario per il completamento:** 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-109">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="8ad3e-110">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="8ad3e-110">Instructions</span></span>

### <a name="1-compiling-your-shader-code"></a><span data-ttu-id="8ad3e-111">1. compilazione del codice dello shader</span><span class="sxs-lookup"><span data-stu-id="8ad3e-111">1. Compiling your shader code</span></span>

<span data-ttu-id="8ad3e-112">Compilare il codice dello shader con una delle funzioni di compilazione.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-112">Compile your shader code with one of the compile functions.</span></span> <span data-ttu-id="8ad3e-113">Questo frammento di codice, ad esempio, USA [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="8ad3e-113">For example, this code snippet uses [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).</span></span>

```cpp
    string source;
 
    ComPtr<ID3DBlob> codeBlob;
    ComPtr<ID3DBlob> errorBlob;
    HRESULT hr = D3DCompile(
        source.c_str(),
        source.size(),
        "ShaderModule",
        NULL,
        NULL,
        NULL,
        ("lib" + m_shaderModelSuffix).c_str(),
        D3DCOMPILE_OPTIMIZATION_LEVEL3,
        0,
        &codeBlob,
        &errorBlob
        );
```

<span data-ttu-id="8ad3e-114">La stringa di origine contiene il codice HLSL ASCII non compilato.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-114">The source string contains the uncompiled ASCII HLSL code.</span></span>

### <a name="2-load-the-compiled-code-into-a-shader-library"></a><span data-ttu-id="8ad3e-115">2. caricare il codice compilato in una libreria shader.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-115">2. Load the compiled code into a shader library.</span></span>

<span data-ttu-id="8ad3e-116">Chiamare la funzione [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) per caricare il codice compilato ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) in un modulo ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) che rappresenta una libreria shader.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-116">Call the [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) function to load the compiled code ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) into a module ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) that represents a shader library.</span></span>


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a><span data-ttu-id="8ad3e-117">3. associare le risorse dagli slot di origine agli slot di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-117">3. Bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="8ad3e-118">Chiamare il metodo [**ID3D11Module:: CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) per creare un'istanza ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) della libreria, in modo da poter quindi definire le associazioni di risorse per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-118">Call the [**ID3D11Module::CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) method to create an instance ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) of the library so you can then define resource bindings for the instance.</span></span>

<span data-ttu-id="8ad3e-119">Chiamare i metodi Bind di [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) per associare le risorse necessarie dagli slot di origine agli slot di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-119">Call the bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) to bind the resources you need from source slots to destination slots.</span></span> <span data-ttu-id="8ad3e-120">Le risorse possono essere trame, buffer, Sampler, buffer costanti o UAV.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-120">The resources can be textures, buffers, samplers, constant buffers, or UAVs.</span></span> <span data-ttu-id="8ad3e-121">In genere, si utilizzeranno gli stessi slot della libreria di origine.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-121">Typically, you will use the same slots as the source library.</span></span>


```C++
    // Create an instance of the library and define resource bindings for it.
    // In this sample we use the same slots as the source library however this is not required.
    ComPtr<ID3D11ModuleInstance> shaderLibraryInstance;
    DX::ThrowIfFailed(shaderLibrary->CreateInstance("", &shaderLibraryInstance));
    // HRESULTs for Bind methods are intentionally ignored as compiler optimizations may eliminate the source
    // bindings. In these cases, the Bind operation will fail, but the final shader will function normally.
    shaderLibraryInstance->BindResource(0, 0, 1);
    shaderLibraryInstance->BindSampler(0, 0, 1);
    shaderLibraryInstance->BindConstantBuffer(0, 0, 0);
    shaderLibraryInstance->BindConstantBuffer(1, 1, 0);
    shaderLibraryInstance->BindConstantBuffer(2, 2, 0);
```



<span data-ttu-id="8ad3e-122">Questo codice HLSL Mostra che la libreria di origine usa gli stessi slot (T0, S0, B0, B1 e B2) come gli slot usati nei metodi BIND precedenti di [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).</span><span class="sxs-lookup"><span data-stu-id="8ad3e-122">This HLSL code shows that the source library uses the same slots (t0, s0, b0, b1, and b2) as the slots used in the preceding bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).</span></span>

``` syntax
// This is the default code in the fixed header section.
Texture2D<float3> Texture : register(t0);
SamplerState Anisotropic : register(s0);
cbuffer CameraData : register(b0)
{
    float4x4 Model;
    float4x4 View;
    float4x4 Projection;
};
cbuffer TimeVariantSignals : register(b1)
{
    float SineWave;
    float SquareWave;
    float TriangleWave;
    float SawtoothWave;
};

// This code is not displayed, but is used as part of the linking process.
cbuffer HiddenBuffer : register(b2)
{
    float3 LightDirection;
};
```

## <a name="summary-and-next-steps"></a><span data-ttu-id="8ad3e-123">Riepilogo e passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="8ad3e-123">Summary and next steps</span></span>

<span data-ttu-id="8ad3e-124">Il codice dello shader è stato compilato, è stato caricato il codice compilato in una libreria dello shader e le risorse sono state delimitate da slot di origine a slot di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-124">We compiled shader code, loaded the compiled code into a shader library, and bound resources from source slots to destination slots.</span></span>

<span data-ttu-id="8ad3e-125">A questo punto si costruiscono i grafici a collegamento di funzioni (FLGs) per gli shader, li si collega al codice compilato e si producono BLOB dello shader che possono essere usati dal runtime Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8ad3e-125">Next we construct function-linking-graphs (FLGs) for shaders, link them to compiled code, and produce shader blobs that the Direct3D runtime can use.</span></span>

[<span data-ttu-id="8ad3e-126">Creazione di un grafico di collegamento di funzioni e collegamento al codice compilato</span><span class="sxs-lookup"><span data-stu-id="8ad3e-126">Constructing a function-linking-graph and linking it to compiled code</span></span>](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a><span data-ttu-id="8ad3e-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ad3e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ad3e-128">Uso del collegamento shader</span><span class="sxs-lookup"><span data-stu-id="8ad3e-128">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 