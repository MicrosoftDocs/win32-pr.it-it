---
title: Come creare un buffer costante
description: In questo argomento viene illustrato come inizializzare un buffer costante in preparazione per il rendering.
ms.assetid: 78694ac2-e850-402d-8c99-6afb0bd5d660
keywords:
- buffer costante, creazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1abb6718ad223ff389aa0b7ebf10ad1ec8bacd71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729562"
---
# <a name="how-to-create-a-constant-buffer"></a><span data-ttu-id="18856-104">Procedura: creare un buffer costante</span><span class="sxs-lookup"><span data-stu-id="18856-104">How to: Create a Constant Buffer</span></span>

<span data-ttu-id="18856-105">I [buffer costanti](overviews-direct3d-11-resources-buffers-intro.md) contengono dati costanti dello shader.</span><span class="sxs-lookup"><span data-stu-id="18856-105">[Constant buffers](overviews-direct3d-11-resources-buffers-intro.md) contain shader constant data.</span></span> <span data-ttu-id="18856-106">In questo argomento viene illustrato come inizializzare un [buffer costante](overviews-direct3d-11-resources-buffers-intro.md) in preparazione per il rendering.</span><span class="sxs-lookup"><span data-stu-id="18856-106">This topic shows how to initialize a [constant buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="18856-107">**Per inizializzare un buffer costante**</span><span class="sxs-lookup"><span data-stu-id="18856-107">**To initialize a constant buffer**</span></span>

1.  <span data-ttu-id="18856-108">Definire una struttura che descrive i dati costanti del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="18856-108">Define a structure that describes the vertex shader constant data.</span></span>
2.  <span data-ttu-id="18856-109">Allocare memoria per la struttura definita nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="18856-109">Allocate memory for the structure that you defined in step one.</span></span> <span data-ttu-id="18856-110">Riempire questo buffer con i dati costanti del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="18856-110">Fill this buffer with vertex shader constant data.</span></span> <span data-ttu-id="18856-111">È possibile usare **malloc** o **New** per allocare la memoria oppure è possibile allocare memoria per la struttura dallo stack.</span><span class="sxs-lookup"><span data-stu-id="18856-111">You can use **malloc** or **new** to allocate the memory, or you can allocate memory for the structure from the stack.</span></span>
3.  <span data-ttu-id="18856-112">Creare una descrizione del buffer compilando una struttura [**d3d11 \_ buffer \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="18856-112">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="18856-113">Passare il \_ flag del \_ buffer costante di binding d3d11 \_ al membro **BindFlags** e passare le dimensioni della struttura di descrizione del buffer costante in byte al membro **ByteWidth** .</span><span class="sxs-lookup"><span data-stu-id="18856-113">Pass the D3D11\_BIND\_CONSTANT\_BUFFER flag to the **BindFlags** member and pass the size of the constant buffer description structure in bytes to the **ByteWidth** member.</span></span>

    > [!Note]  
    > <span data-ttu-id="18856-114">\_ \_ \_ Non è possibile combinare il flag del buffer costante di binding d3d11 con altri flag.</span><span class="sxs-lookup"><span data-stu-id="18856-114">The D3D11\_BIND\_CONSTANT\_BUFFER flag cannot be combined with any other flags.</span></span>

     

4.  <span data-ttu-id="18856-115">Creare una descrizione dei dati della sottorisorsa compilando una struttura di [**\_ \_ dati della sottorisorsa d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) .</span><span class="sxs-lookup"><span data-stu-id="18856-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="18856-116">Il membro **pSysMem** della struttura **dei \_ \_ dati della sottorisorsa d3d11** deve puntare direttamente ai dati costanti del vertex shader creati nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="18856-116">The **pSysMem** member of the **D3D11\_SUBRESOURCE\_DATA** structure must point directly to the vertex shader constant data that you created in step two.</span></span>
5.  <span data-ttu-id="18856-117">Chiamare [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) passando la struttura [**\_ \_ Desc del buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , la [**struttura \_ \_ dei dati della sottorisorsa d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e l'indirizzo di un puntatore all'interfaccia [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) da inizializzare.</span><span class="sxs-lookup"><span data-stu-id="18856-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="18856-118">Questi esempi di codice illustrano come creare un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="18856-118">These code examples demonstrate how to create a constant buffer.</span></span>

<span data-ttu-id="18856-119">Questo esempio si basa sul presupposto che **g \_ pd3dDevice** sia un oggetto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) valido e che **g \_ pd3dContext** sia un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) valido.</span><span class="sxs-lookup"><span data-stu-id="18856-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that **g\_pd3dContext** is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


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



<span data-ttu-id="18856-120">In questo esempio viene illustrata la definizione cbuffer HLSL associata.</span><span class="sxs-lookup"><span data-stu-id="18856-120">This example shows the associated HLSL cbuffer definition.</span></span>

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
> <span data-ttu-id="18856-121">Assicurarsi di associare il layout della \_ memoria del buffer costante di Visual Studio \_ in C++ con il layout HLSL.</span><span class="sxs-lookup"><span data-stu-id="18856-121">Make sure to match the VS\_CONSTANT\_BUFFER memory layout in C++ with the HLSL layout.</span></span> <span data-ttu-id="18856-122">Per informazioni sul modo in cui HLSL gestisce il layout in memoria, vedere [regole di compressione per variabili costanti](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span><span class="sxs-lookup"><span data-stu-id="18856-122">For info about how HLSL handles layout in memory, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="18856-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18856-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18856-124">Buffer</span><span class="sxs-lookup"><span data-stu-id="18856-124">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="18856-125">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="18856-125">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 