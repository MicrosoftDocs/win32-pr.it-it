---
title: Come creare un buffer costante
description: In questo argomento viene illustrato come inizializzare un buffer costante in preparazione per il rendering.
ms.assetid: 78694ac2-e850-402d-8c99-6afb0bd5d660
keywords:
- buffer costante, creazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2359698c4dfc72bfe3c3c9747e29ddfa5f6aecd2aaa32b99d75fbe38e956ac4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912822"
---
# <a name="how-to-create-a-constant-buffer"></a>Procedura: Creare un buffer costante

[I buffer costanti contengono](overviews-direct3d-11-resources-buffers-intro.md) dati costanti dello shader. In questo argomento viene illustrato come inizializzare un [buffer costante](overviews-direct3d-11-resources-buffers-intro.md) in preparazione per il rendering.

**Per inizializzare un buffer costante**

1.  Definire una struttura che descrive i dati costanti del vertex shader.
2.  Allocare memoria per la struttura definita nel passaggio 1. Riempire questo buffer con dati costanti del vertex shader. È possibile usare **malloc** o **new** per allocare la memoria oppure è possibile allocare memoria per la struttura dallo stack.
3.  Creare una descrizione del buffer compilando una [**struttura D3D11 \_ BUFFER \_ DESC.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Passare il flag D3D11 BIND CONSTANT BUFFER al membro \_ \_ \_ **BindFlags** e passare le dimensioni della struttura di descrizione costante del buffer in byte al **membro ByteWidth.**

    > [!Note]  
    > Il flag D3D11 \_ BIND CONSTANT BUFFER non può essere combinato con altri \_ \_ flag.

     

4.  Creare una descrizione dei dati della sottorisorsa compilando una [**struttura D3D11 \_ SUBRESOURCE \_ DATA.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Il **membro pSysMem** della struttura **\_ SUBRESOURCE \_ DATA D3D11** deve puntare direttamente ai dati costanti del vertex shader creati nel passaggio 2.
5.  Chiamare [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) durante il passaggio della struttura [**D3D11 \_ BUFFER \_ DESC,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) della struttura [**\_ SUBRESOURCE \_ DATA D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e dell'indirizzo di un puntatore all'interfaccia [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) da inizializzare.

Questi esempi di codice illustrano come creare un buffer costante.

Questo esempio presuppone che **g \_ pd3dDevice** sia un oggetto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) valido e **che g \_ pd3dContext** sia un oggetto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) valido.


```C++
ID3D11Buffer*   g_pConstantBuffer11 = NULL;

// Define the constant data used to communicate with shaders.
struct VS_CONSTANT_BUFFER
{
    XMFLOAT4X4 mWorldViewProj;                              
    XMFLOAT4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                                            
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
} VS_CONSTANT_BUFFER;

// Supply the vertex shader constant data.
VS_CONSTANT_BUFFER VsConstData;
VsConstData.mWorldViewProj = {...};
VsConstData.vSomeVectorThatMayBeNeededByASpecificShader = XMFLOAT4(1,2,3,4);
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader = 3.0f;
VsConstData.fTime = 1.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader2 = 2.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader3 = 4.0f;

// Fill in a buffer description.
D3D11_BUFFER_DESC cbDesc;
cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
cbDesc.Usage = D3D11_USAGE_DYNAMIC;
cbDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;
cbDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
cbDesc.MiscFlags = 0;
cbDesc.StructureByteStride = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = &VsConstData;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer.
hr = g_pd3dDevice->CreateBuffer( &cbDesc, &InitData, 
                                 &g_pConstantBuffer11 );

if( FAILED( hr ) )
   return hr;

// Set the buffer.
g_pd3dContext->VSSetConstantBuffers( 0, 1, &g_pConstantBuffer11 );
    
```



Questo esempio illustra la definizione di cbuffer HLSL associata.

``` syntax
cbuffer VS_CONSTANT_BUFFER : register(b0)
{
    matrix mWorldViewProj;
    float4  vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};
```

> [!Note]  
> Assicurarsi di associare il layout di memoria DI VS \_ CONSTANT \_ BUFFER in C++ con il layout HLSL. Per informazioni sul modo in cui HLSL gestisce il layout in memoria, vedere [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 