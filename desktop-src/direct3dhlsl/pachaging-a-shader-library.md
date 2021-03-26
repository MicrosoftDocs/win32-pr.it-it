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
# <a name="packaging-a-shader-library"></a>Creazione del pacchetto di una libreria shader

Qui viene illustrato come compilare il codice dello shader, caricare il codice compilato in una libreria shader e associare le risorse da slot di origine a slot di destinazione.

**Obiettivo:** Per creare un pacchetto di una libreria shader da utilizzare per il collegamento dello shader.

## <a name="prerequisites"></a>Prerequisiti

Partiamo dal presupposto che tu abbia familiarità con C++. Devi inoltre avere un'esperienza di base dei concetti di programmazione di grafica.

**Tempo necessario per il completamento:** 30 minuti.

## <a name="instructions"></a>Istruzioni

### <a name="1-compiling-your-shader-code"></a>1. compilazione del codice dello shader

Compilare il codice dello shader con una delle funzioni di compilazione. Questo frammento di codice, ad esempio, USA [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).

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

La stringa di origine contiene il codice HLSL ASCII non compilato.

### <a name="2-load-the-compiled-code-into-a-shader-library"></a>2. caricare il codice compilato in una libreria shader.

Chiamare la funzione [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) per caricare il codice compilato ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) in un modulo ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) che rappresenta una libreria shader.


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a>3. associare le risorse dagli slot di origine agli slot di destinazione.

Chiamare il metodo [**ID3D11Module:: CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) per creare un'istanza ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) della libreria, in modo da poter quindi definire le associazioni di risorse per l'istanza.

Chiamare i metodi Bind di [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) per associare le risorse necessarie dagli slot di origine agli slot di destinazione. Le risorse possono essere trame, buffer, Sampler, buffer costanti o UAV. In genere, si utilizzeranno gli stessi slot della libreria di origine.


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



Questo codice HLSL Mostra che la libreria di origine usa gli stessi slot (T0, S0, B0, B1 e B2) come gli slot usati nei metodi BIND precedenti di [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).

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

## <a name="summary-and-next-steps"></a>Riepilogo e passaggi successivi

Il codice dello shader è stato compilato, è stato caricato il codice compilato in una libreria dello shader e le risorse sono state delimitate da slot di origine a slot di destinazione.

A questo punto si costruiscono i grafici a collegamento di funzioni (FLGs) per gli shader, li si collega al codice compilato e si producono BLOB dello shader che possono essere usati dal runtime Direct3D.

[Creazione di un grafico di collegamento di funzioni e collegamento al codice compilato](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del collegamento shader](using-shader-linking.md)
</dt> </dl>

 

 