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
# <a name="how-to-create-a-vertex-buffer"></a>Procedura: creare un vertex buffer

I [buffer vertex](overviews-direct3d-11-resources-buffers-intro.md) contengono i dati per ogni vertice. In questo argomento viene illustrato come inizializzare un [buffer di vertex](overviews-direct3d-11-resources-buffers-intro.md)statico, ovvero un buffer vertex che non cambia. Per informazioni sull'inizializzazione di un buffer non statico, vedere la sezione [osservazioni](#remarks) .

**Per inizializzare un buffer vertex statico**

1.  Definire una struttura che descrive un vertice. Se, ad esempio, i dati del vertice contengono dati di posizione e dati di colore, la struttura avrà un vettore che descrive la posizione e un'altra che descrive il colore.
2.  Allocare memoria (usando malloc o New) per la struttura definita nel passaggio 1. Riempire questo buffer con i dati del vertice effettivi che descrivono la geometria.
3.  Creare una descrizione del buffer compilando una struttura [**d3d11 \_ buffer \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) . Passare il \_ flag del buffer di vertice di binding d3d11 \_ \_ al membro **BindFlags** e passare le dimensioni della struttura dal passaggio uno al membro **ByteWidth** .
4.  Creare una descrizione dei dati della sottorisorsa compilando una struttura di [**\_ \_ dati della sottorisorsa d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) . Il membro **pSysMem** della struttura [**dei \_ \_ dati della sottorisorsa d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) deve puntare direttamente ai dati delle risorse creati nel secondo passaggio.
5.  Chiamare [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) passando la struttura [**\_ \_ Desc del buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , la [**struttura \_ \_ dei dati della sottorisorsa d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e l'indirizzo di un puntatore all'interfaccia [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) da inizializzare.

Nell'esempio di codice riportato di seguito viene illustrato come creare un buffer vertex. Questo esempio si basa sul presupposto che **g \_ pd3dDevice** sia un oggetto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) valido.


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



## <a name="remarks"></a>Commenti

Ecco alcuni modi per inizializzare un buffer vertex che cambia nel tempo.

1.  Creare un secondo buffer con [**\_ \_ gestione temporanea dell'utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); compilare il secondo buffer usando [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**sul ID3D11DeviceContext:: annullare**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); usare [**sul ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) per copiare dal buffer di gestione temporanea al buffer predefinito.
2.  Usare [**sul ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) per copiare i dati dalla memoria.
3.  Creare un buffer con [**la \_ \_ dinamica di utilizzo di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)e riempirlo con [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**sul ID3D11DeviceContext:: annullare**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (usando i flag di eliminazione e nosovrascrive in modo appropriato).

\#1 e \# 2 sono utili per il contenuto che cambia meno di una volta per fotogramma. In generale, le letture GPU saranno veloci e gli aggiornamenti della CPU saranno più lenti.

\#3 è utile per il contenuto che cambia più di una volta per fotogramma. In generale, le letture GPU saranno più lente, ma gli aggiornamenti della CPU saranno più veloci.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




