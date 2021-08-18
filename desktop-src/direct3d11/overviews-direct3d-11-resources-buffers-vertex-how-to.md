---
title: Come creare un vertex buffer
description: In questo argomento viene illustrato come inizializzare un buffer dei vertici statico, ad esempio un buffer dei vertici che non cambia.
ms.assetid: 584a39d1-7629-429a-b451-64b1432cb48f
keywords:
- vertex buffer, creazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f919646dfd4e8f714b925606f342db586ff2b8f09690c58698b7dab2635159e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496901"
---
# <a name="how-to-create-a-vertex-buffer"></a>Procedura: Creare un vertex buffer

[I vertex buffer contengono](overviews-direct3d-11-resources-buffers-intro.md) dati per vertice. In questo argomento viene illustrato come inizializzare un [buffer dei vertici](overviews-direct3d-11-resources-buffers-intro.md)statico, ci esempio un buffer dei vertici che non cambia. Per informazioni sull'inizializzazione di un buffer non statico, vedere [la sezione osservazioni.](#remarks)

**Per inizializzare un vertex buffer statico**

1.  Definire una struttura che descrive un vertice. Ad esempio, se i dati dei vertici contengono dati sulla posizione e i dati di colore, la struttura avrebbe un vettore che descrive la posizione e un altro che descrive il colore.
2.  Allocare memoria (usando malloc o new) per la struttura definita nel passaggio 1. Riempire questo buffer con i dati dei vertici effettivi che descrivono la geometria.
3.  Creare una descrizione del buffer compilando una [**struttura D3D11 \_ BUFFER \_ DESC.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Passare il flag D3D11 BIND VERTEX BUFFER al membro BindFlags e passare le dimensioni della struttura dal passaggio \_ \_ \_ 1 al **membro ByteWidth.** 
4.  Creare una descrizione dei dati della sottorisorsa compilando una [**struttura D3D11 \_ SUBRESOURCE \_ DATA.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) Il **membro pSysMem** della struttura [**\_ SUBRESOURCE \_ DATA D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) deve puntare direttamente ai dati delle risorse creati nel passaggio 2.
5.  Chiamare [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) durante il passaggio della struttura [**D3D11 \_ BUFFER \_ DESC,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) della struttura [**\_ SUBRESOURCE \_ DATA D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e dell'indirizzo di un puntatore all'interfaccia [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) da inizializzare.

Nell'esempio di codice seguente viene illustrato come creare un vertex buffer. Questo esempio presuppone che **g \_ pd3dDevice** sia un oggetto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) valido.


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

Ecco alcuni modi per inizializzare un buffer dei vertici che cambia nel tempo.

1.  Creare un secondo buffer con [**D3D11 \_ USAGE \_ STAGING;**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)riempire il secondo buffer usando [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); usare [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) per copiare dal buffer di staging al buffer predefinito.
2.  Usare [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) per copiare i dati dalla memoria.
3.  Creare un buffer [**con D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)e riempirlo con [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (usando i flag Discard e NoOverwrite in modo appropriato).

\#1 e \# 2 sono utili per il contenuto che cambia meno di una volta per fotogramma. In generale, le operazioni di lettura della GPU saranno veloci e gli aggiornamenti della CPU saranno più lenti.

\#3 è utile per il contenuto che cambia più di una volta per fotogramma. In generale, le operazioni di lettura della GPU saranno più lente, ma gli aggiornamenti della CPU saranno più veloci.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




