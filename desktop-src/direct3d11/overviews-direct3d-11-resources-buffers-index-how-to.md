---
title: Come creare un buffer di indice
description: In questo argomento viene illustrato come inizializzare un buffer di indice in preparazione per il rendering.
ms.assetid: 4b33d32a-27fd-4652-87ac-3b7268881f89
keywords:
- buffer di indice, creazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c4c99639748876a5f5fd84e546aaf299885c76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221748"
---
# <a name="how-to-create-an-index-buffer"></a><span data-ttu-id="4ca44-104">Procedura: creare un buffer di indice</span><span class="sxs-lookup"><span data-stu-id="4ca44-104">How to: Create an Index Buffer</span></span>

<span data-ttu-id="4ca44-105">I [buffer di indice](overviews-direct3d-11-resources-buffers-intro.md) contengono dati di indice.</span><span class="sxs-lookup"><span data-stu-id="4ca44-105">[Index buffers](overviews-direct3d-11-resources-buffers-intro.md) contain index data.</span></span> <span data-ttu-id="4ca44-106">In questo argomento viene illustrato come inizializzare un [buffer di indice](overviews-direct3d-11-resources-buffers-intro.md) in preparazione per il rendering.</span><span class="sxs-lookup"><span data-stu-id="4ca44-106">This topic shows how to initialize an [index buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="4ca44-107">**Per inizializzare un buffer di indice**</span><span class="sxs-lookup"><span data-stu-id="4ca44-107">**To initialize an index buffer**</span></span>

1.  <span data-ttu-id="4ca44-108">Creare un buffer che contiene le informazioni sugli indici.</span><span class="sxs-lookup"><span data-stu-id="4ca44-108">Create a buffer that contains your index information.</span></span>
2.  <span data-ttu-id="4ca44-109">Creare una descrizione del buffer compilando una struttura [**d3d11 \_ buffer \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="4ca44-109">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="4ca44-110">Passare il \_ \_ flag buffer index d3d11 binding \_ al membro **BindFlags** e passare la dimensione del buffer in byte al membro **ByteWidth** .</span><span class="sxs-lookup"><span data-stu-id="4ca44-110">Pass the D3D11\_BIND\_INDEX\_BUFFER flag to the **BindFlags** member and pass the size of the buffer in bytes to the **ByteWidth** member.</span></span>
3.  <span data-ttu-id="4ca44-111">Creare una descrizione dei dati della sottorisorsa compilando una struttura di [**\_ \_ dati della sottorisorsa d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) .</span><span class="sxs-lookup"><span data-stu-id="4ca44-111">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="4ca44-112">Il membro **pSysMem** deve puntare direttamente ai dati dell'indice creati nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="4ca44-112">The **pSysMem** member should point directly to the index data created in step one.</span></span>
4.  <span data-ttu-id="4ca44-113">Chiamare [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) passando la struttura [**\_ \_ Desc del buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , la [**struttura \_ \_ dei dati della sottorisorsa d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e l'indirizzo di un puntatore all'interfaccia [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) da inizializzare.</span><span class="sxs-lookup"><span data-stu-id="4ca44-113">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="4ca44-114">Nell'esempio di codice riportato di seguito viene illustrato come creare un buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="4ca44-114">The following code example demonstrates how to create an index buffer.</span></span> <span data-ttu-id="4ca44-115">Questo esempio presuppone che</span><span class="sxs-lookup"><span data-stu-id="4ca44-115">This example assumes that</span></span>


```
g_pd3dDevice
```



<span data-ttu-id="4ca44-116">è un oggetto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) valido e</span><span class="sxs-lookup"><span data-stu-id="4ca44-116">is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that</span></span>


```
g_pd3dContext
```



<span data-ttu-id="4ca44-117">è un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) valido.</span><span class="sxs-lookup"><span data-stu-id="4ca44-117">is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


```
ID3D11Buffer *g_pIndexBuffer = NULL;

// Create indices.
unsigned int indices[] = { 0, 1, 2 };

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage           = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
bufferDesc.BindFlags       = D3D11_BIND_INDEX_BUFFER;
bufferDesc.CPUAccessFlags  = 0;
bufferDesc.MiscFlags       = 0;

// Define the resource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = indices;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer with the device.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
if( FAILED( hr ) )
    return hr;

// Set the buffer.
g_pd3dContext->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
    
```



## <a name="related-topics"></a><span data-ttu-id="4ca44-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ca44-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ca44-119">Buffer</span><span class="sxs-lookup"><span data-stu-id="4ca44-119">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="4ca44-120">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="4ca44-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




