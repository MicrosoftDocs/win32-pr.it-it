---
title: Introduzione ai buffer in Direct3D 11
description: Una risorsa buffer è una raccolta di dati completamente tipiati raggruppati in elementi.
ms.assetid: e33ca01e-f13c-4f91-b0db-2b2bc6b4fd8f
keywords:
- constant buffer, cos'è
- vertex buffer, cos'è
- index buffer, che cos'è
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51f7b0dbd60264b77f9d9dc83f39cbb4325464079d537c3ee741a942d26a139
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752021"
---
# <a name="introduction-to-buffers-in-direct3d-11"></a>Introduzione ai buffer in Direct3D 11

Una risorsa buffer è una raccolta di dati completamente tipiati raggruppati in elementi. È possibile usare i buffer per archiviare un'ampia gamma di dati, tra cui vettori di posizione, vettori normali, coordinate di trama in un buffer dei vertici, indici in un index buffer o stato del dispositivo. Un elemento buffer è costituito da 1 a 4 componenti. Gli elementi buffer possono includere valori di dati di tipo pack (ad esempio valori della superficie R8G8B8A8), interi singoli a 8 bit o quattro valori a virgola mobile a 32 bit.

Un buffer viene creato come risorsa non strutturata. Poiché non è strutturato, un buffer non può contenere livelli mipmap, non può essere filtrato durante la lettura e non può essere multicampionato.

## <a name="buffer-types"></a>Tipi di buffer

Di seguito sono riportati i tipi di risorse buffer supportati da Direct3D 11. Tutti i tipi di buffer sono incapsulati [**dall'interfaccia ID3D11Buffer.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)

-   [Vertex Buffer](#vertex-buffer)
-   [Index Buffer](#index-buffer)
-   [Constant Buffer](#constant-buffer)

### <a name="vertex-buffer"></a>Vertex Buffer

Un buffer dei vertici contiene i dati dei vertici usati per definire la geometria. I dati dei vertici includono coordinate di posizione, dati di colore, dati delle coordinate di trama, dati normali e così via.

L'esempio più semplice di un vertex buffer è quello che contiene solo dati di posizione. Può essere visualizzato come illustrato nella figura seguente.

![illustrazione di un buffer dei vertici che contiene i dati di posizione](images/d3d10-resources-single-element-vb2.png)

Più spesso, un buffer dei vertici contiene tutti i dati necessari per specificare completamente i vertici 3D. Un esempio può essere un buffer dei vertici che contiene la posizione per vertice, le coordinate normali e di trama. Questi dati sono in genere organizzati come set di elementi per vertice, come illustrato nella figura seguente.

![illustrazione di un buffer dei vertici che contiene dati relativi a posizione, normale e trama](images/d3d10-vertex-buffer-element.png)

Questo buffer dei vertici contiene dati per vertice. ogni vertice archivia tre elementi (coordinate di posizione, normale e trama). La posizione e la normale vengono in genere specificate usando tre float a 32 bit (DXGI FORMAT R32G32B32 FLOAT) e le coordinate della trama usando due float a \_ \_ \_ 32 bit (DXGI \_ FORMAT \_ R32G32 \_ FLOAT).

Per accedere ai dati da un vertex buffer è necessario conoscere il vertice a cui accedere, oltre ai parametri del buffer aggiuntivi seguenti:

-   Offset: numero di byte dall'inizio del buffer ai dati per il primo vertice. È possibile specificare l'offset usando il [**metodo ID3D11DeviceContext::IASetVertexBuffers.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers)
-   BaseVertexLocation: numero di byte dall'offset al primo vertice usato dalla chiamata di disegno appropriata.

Prima di creare un vertex buffer, è necessario definirne il layout creando [**un'interfaccia ID3D11InputLayout.**](/windows/win32/api/d3d11/nn-d3d11-id3d11inputlayout) Questa operazione viene eseguita chiamando il [**metodo ID3D11Device::CreateInputLayout.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout) Dopo aver creato l'oggetto input-layout, è possibile associarlo alla fase input-assembler chiamando [**ID3D11DeviceContext::IASetInputLayout.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout)

Per creare un vertex buffer, chiamare [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).

### <a name="index-buffer"></a>Index Buffer

I buffer di indice contengono offset di interi nei buffer dei vertici e vengono usati per eseguire il rendering delle primitive in modo più efficiente. Un index buffer contiene un set sequenziale di indici a 16 o 32 bit; ogni indice viene usato per identificare un vertice in un vertex buffer. Un index buffer può essere visualizzato come nell'illustrazione seguente.

![illustrazione di un index buffer](images/d3d10-index-buffer.png)

Gli indici sequenziali archiviati in un index buffer si trovano con i parametri seguenti:

-   Offset: numero di byte dall'indirizzo di base del index buffer. L'offset viene fornito al [**metodo ID3D11DeviceContext::IASetIndexBuffer.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer)
-   StartIndexLocation: specifica il primo index buffer dall'indirizzo di base e l'offset fornito in [**IASetIndexBuffer.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer) Il percorso iniziale viene fornito al metodo [**ID3D11DeviceContext::D rawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) o [**ID3D11DeviceContext::D rawIndexedInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) e rappresenta il primo indice di cui eseguire il rendering.
-   IndexCount: numero di indici di cui eseguire il rendering. Il numero viene fornito al [**metodo DrawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)

Start of Index Buffer = Index Buffer Base Address + Offset (bytes) + StartIndexLocation \* ElementSize (bytes);

In questo calcolo ElementSize è la dimensione di ogni index buffer, ovvero due o quattro byte.

Per creare un index buffer, chiamare [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).

### <a name="constant-buffer"></a>Constant Buffer

Un buffer costante consente di fornire in modo efficiente i dati delle costanti shader alla pipeline. È possibile usare un buffer costante per archiviare i risultati della fase di output del flusso. Concettualmente, un buffer costante è simile a un vertex buffer a elemento singolo, come illustrato nella figura seguente.

![illustrazione di un buffer costante shader](images/d3d10-shader-resource-buffer.png)

Ogni elemento archivia una costante componente da 1 a 4, determinata dal formato dei dati archiviati. Per creare un buffer costante shader, chiamare [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) e specificare il membro **D3D11 \_ BIND \_ CONSTANT \_ BUFFER** del tipo [**enumerato D3D11 \_ BIND \_ FLAG.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)

Un buffer costante può usare un solo flag di associazione (**D3D11 \_ BIND \_ CONSTANT \_ BUFFER),** che non può essere combinato con altri flag di associazione. Per associare un buffer costante shader alla pipeline, chiamare uno dei metodi seguenti: [**ID3D11DeviceContext::GSSetConstantBuffers,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetconstantbuffers) [**ID3D11DeviceContext::P SSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers)o [**ID3D11DeviceContext::VSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers).

Per leggere un buffer costante shader da uno shader, usare una funzione di caricamento HLSL, ad esempio [**Load.**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load) Ogni fase dello shader consente fino a 15 buffer costanti shader; ogni buffer può contenere fino a 4096 costanti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer](overviews-direct3d-11-resources-buffers.md)
</dt> </dl>

 

 