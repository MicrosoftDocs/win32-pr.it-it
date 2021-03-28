---
title: Come creare un vertex buffer
description: In questo argomento viene illustrato come inizializzare un buffer di vertex statico, ovvero un buffer vertex che non cambia.
ms.assetid: 584a39d1-7629-429a-b451-64b1432cb48f
keywords:
- buffer vertex, creazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e0b3d9d8f731b01e7c919105c21c8d150f864a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330791"
---
# <a name="how-to-create-a-vertex-buffer"></a><span data-ttu-id="ae3b1-104">Procedura: creare un vertex buffer</span><span class="sxs-lookup"><span data-stu-id="ae3b1-104">How to: Create a Vertex Buffer</span></span>

<span data-ttu-id="ae3b1-105">I [buffer vertex](overviews-direct3d-11-resources-buffers-intro.md) contengono i dati per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-105">[Vertex buffers](overviews-direct3d-11-resources-buffers-intro.md) contain per vertex data.</span></span> <span data-ttu-id="ae3b1-106">In questo argomento viene illustrato come inizializzare un [buffer di vertex](overviews-direct3d-11-resources-buffers-intro.md)statico, ovvero un buffer vertex che non cambia.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-106">This topic shows how to initialize a static [vertex buffer](overviews-direct3d-11-resources-buffers-intro.md), that is, a vertex buffer that does not change.</span></span> <span data-ttu-id="ae3b1-107">Per informazioni sull'inizializzazione di un buffer non statico, vedere la sezione [osservazioni](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="ae3b1-107">For help initializing a non-static buffer, see the [remarks](#remarks) section.</span></span>

<span data-ttu-id="ae3b1-108">**Per inizializzare un buffer vertex statico**</span><span class="sxs-lookup"><span data-stu-id="ae3b1-108">**To initialize a static vertex buffer**</span></span>

1.  <span data-ttu-id="ae3b1-109">Definire una struttura che descrive un vertice.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-109">Define a structure that describes a vertex.</span></span> <span data-ttu-id="ae3b1-110">Se, ad esempio, i dati del vertice contengono dati di posizione e dati di colore, la struttura avrà un vettore che descrive la posizione e un'altra che descrive il colore.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-110">For example, if your vertex data contains position data and color data, your structure would have one vector that describes the position and another that describes the color.</span></span>
2.  <span data-ttu-id="ae3b1-111">Allocare memoria (usando malloc o New) per la struttura definita nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-111">Allocate memory (using malloc or new) for the structure that you defined in step one.</span></span> <span data-ttu-id="ae3b1-112">Riempire questo buffer con i dati del vertice effettivi che descrivono la geometria.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-112">Fill this buffer with the actual vertex data that describes your geometry.</span></span>
3.  <span data-ttu-id="ae3b1-113">Creare una descrizione del buffer compilando una struttura [**d3d11 \_ buffer \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="ae3b1-113">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="ae3b1-114">Passare il \_ flag del buffer di vertice di binding d3d11 \_ \_ al membro **BindFlags** e passare le dimensioni della struttura dal passaggio uno al membro **ByteWidth** .</span><span class="sxs-lookup"><span data-stu-id="ae3b1-114">Pass the D3D11\_BIND\_VERTEX\_BUFFER flag to the **BindFlags** member and pass the size of the structure from step one to the **ByteWidth** member.</span></span>
4.  <span data-ttu-id="ae3b1-115">Creare una descrizione dei dati della sottorisorsa compilando una struttura di [**\_ \_ dati della sottorisorsa d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) .</span><span class="sxs-lookup"><span data-stu-id="ae3b1-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="ae3b1-116">Il membro **pSysMem** della struttura [**dei \_ \_ dati della sottorisorsa d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) deve puntare direttamente ai dati delle risorse creati nel secondo passaggio.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-116">The **pSysMem** member of the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure should point directly to the resource data created in step two.</span></span>
5.  <span data-ttu-id="ae3b1-117">Chiamare [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) passando la struttura [**\_ \_ Desc del buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , la [**struttura \_ \_ dei dati della sottorisorsa d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e l'indirizzo di un puntatore all'interfaccia [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) da inizializzare.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="ae3b1-118">Nell'esempio di codice riportato di seguito viene illustrato come creare un buffer vertex.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-118">The following code example demonstrates how to create a vertex buffer.</span></span> <span data-ttu-id="ae3b1-119">Questo esempio si basa sul presupposto che **g \_ pd3dDevice** sia un oggetto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) valido.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object.</span></span>


```
ID3D11Buffer*      g_pVertexBuffer;

// Define the data-type that
// describes a vertex.
struct SimpleVertexCombined
{
    XMFLOAT3 Pos;  
    XMFLOAT3 Col;  
};

// Supply the actual vertex data.
SimpleVertexCombined verticesCombo[] =
{
    XMFLOAT3( 0.0f, 0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.0f, 0.5f ),
    XMFLOAT3( 0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.5f, 0.0f, 0.0f ),
    XMFLOAT3( -0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.5f, 0.0f ),
};

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage            = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
bufferDesc.BindFlags        = D3D11_BIND_VERTEX_BUFFER;
bufferDesc.CPUAccessFlags   = 0;
bufferDesc.MiscFlags        = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = verticesCombo;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the vertex buffer.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer );
    
```



## <a name="remarks"></a><span data-ttu-id="ae3b1-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae3b1-120">Remarks</span></span>

<span data-ttu-id="ae3b1-121">Ecco alcuni modi per inizializzare un buffer vertex che cambia nel tempo.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-121">Here are some ways to initialize a vertex buffer that changes over time.</span></span>

1.  <span data-ttu-id="ae3b1-122">Creare un secondo buffer con [**\_ \_ gestione temporanea dell'utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); compilare il secondo buffer usando [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**sul ID3D11DeviceContext:: annullare**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); usare [**sul ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) per copiare dal buffer di gestione temporanea al buffer predefinito.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-122">Create a 2nd buffer with [**D3D11\_USAGE\_STAGING**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); fill the second buffer using [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); use [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) to copy from the staging buffer to the default buffer.</span></span>
2.  <span data-ttu-id="ae3b1-123">Usare [**sul ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) per copiare i dati dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-123">Use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to copy data from memory.</span></span>
3.  <span data-ttu-id="ae3b1-124">Creare un buffer con [**la \_ \_ dinamica di utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)e riempirlo con [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**sul ID3D11DeviceContext:: annullare**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (usando i flag di eliminazione e nosovrascrive in modo appropriato).</span><span class="sxs-lookup"><span data-stu-id="ae3b1-124">Create a buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), and fill it with [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (using the Discard and NoOverwrite flags appropriately).</span></span>

<span data-ttu-id="ae3b1-125">\#1 e \# 2 sono utili per il contenuto che cambia meno di una volta per fotogramma.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-125">\#1 and \#2 are useful for content that changes less than once per frame.</span></span> <span data-ttu-id="ae3b1-126">In generale, le letture GPU saranno veloci e gli aggiornamenti della CPU saranno più lenti.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-126">In general, GPU reads will be fast and CPU updates will be slower.</span></span>

<span data-ttu-id="ae3b1-127">\#3 è utile per il contenuto che cambia più di una volta per fotogramma.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-127">\#3 is useful for content that changes more than once per frame.</span></span> <span data-ttu-id="ae3b1-128">In generale, le letture GPU saranno più lente, ma gli aggiornamenti della CPU saranno più veloci.</span><span class="sxs-lookup"><span data-stu-id="ae3b1-128">In general, GPU reads will be slower, but CPU updates will be faster.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae3b1-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ae3b1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae3b1-130">Buffer</span><span class="sxs-lookup"><span data-stu-id="ae3b1-130">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="ae3b1-131">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ae3b1-131">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




