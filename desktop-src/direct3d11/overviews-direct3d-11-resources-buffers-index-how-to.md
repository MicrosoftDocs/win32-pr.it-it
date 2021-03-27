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
# <a name="how-to-create-an-index-buffer"></a>Procedura: creare un buffer di indice

I [buffer di indice](overviews-direct3d-11-resources-buffers-intro.md) contengono dati di indice. In questo argomento viene illustrato come inizializzare un [buffer di indice](overviews-direct3d-11-resources-buffers-intro.md) in preparazione per il rendering.

**Per inizializzare un buffer di indice**

1.  Creare un buffer che contiene le informazioni sugli indici.
2.  Creare una descrizione del buffer compilando una struttura [**d3d11 \_ buffer \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) . Passare il \_ \_ flag buffer index d3d11 binding \_ al membro **BindFlags** e passare la dimensione del buffer in byte al membro **ByteWidth** .
3.  Creare una descrizione dei dati della sottorisorsa compilando una struttura di [**\_ \_ dati della sottorisorsa d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) . Il membro **pSysMem** deve puntare direttamente ai dati dell'indice creati nel passaggio 1.
4.  Chiamare [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) passando la struttura [**\_ \_ Desc del buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , la [**struttura \_ \_ dei dati della sottorisorsa d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e l'indirizzo di un puntatore all'interfaccia [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) da inizializzare.

Nell'esempio di codice riportato di seguito viene illustrato come creare un buffer di indice. Questo esempio presuppone che


```
g_pd3dDevice
```



è un oggetto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) valido e


```
g_pd3dContext
```



è un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) valido.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




