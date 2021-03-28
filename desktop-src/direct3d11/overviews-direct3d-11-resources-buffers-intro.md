---
title: Introduzione ai buffer in Direct3D 11
description: Una risorsa buffer è una raccolta di dati completamente tipizzati raggruppati in elementi.
ms.assetid: e33ca01e-f13c-4f91-b0db-2b2bc6b4fd8f
keywords:
- buffer costante, informazioni
- vertex buffer, informazioni
- buffer di indice, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241ade0721ae87b1371586bc901ee18f8975b53f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337895"
---
# <a name="introduction-to-buffers-in-direct3d-11"></a>Introduzione ai buffer in Direct3D 11

Una risorsa buffer è una raccolta di dati completamente tipizzati raggruppati in elementi. È possibile usare i buffer per archiviare un'ampia gamma di dati, inclusi i vettori di posizione, i vettori normali, le coordinate di trama in un buffer dei vertici, gli indici in un buffer di indice o lo stato del dispositivo. Un elemento buffer è costituito da 1 a 4 componenti. Gli elementi del buffer possono includere valori di dati compressi, ad esempio i valori della superficie R8G8B8A8, singoli interi a 8 bit o valori a virgola mobile a 4 32 bit.

Un buffer viene creato come una risorsa non strutturata. Poiché non è strutturato, un buffer non può contenere alcun livello di mipmap, non può essere filtrato durante la lettura e non può essere multicampionato.

## <a name="buffer-types"></a>Tipi di buffer

Di seguito sono riportati i tipi di risorse del buffer supportati da Direct3D 11. Tutti i tipi di buffer sono incapsulati dall'interfaccia [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) .

-   [Buffer vertex](#vertex-buffer)
-   [Buffer indice](#index-buffer)
-   [Buffer costante](#constant-buffer)

### <a name="vertex-buffer"></a>Buffer vertex

Un buffer di vertici contiene i dati dei vertici usati per definire la geometria. I dati dei vertici includono coordinate di posizione, dati di colore, dati di coordinate di trama, dati normali e così via.

L'esempio più semplice di un vertex buffer è quello che contiene solo i dati di posizione. Può essere visualizzato come illustrato nella figura seguente.

![illustrazione di un buffer di vertice che contiene i dati relativi alla posizione](images/d3d10-resources-single-element-vb2.png)

Più spesso, un buffer di vertici contiene tutti i dati necessari per specificare in modo completo i vertici 3D. Un esempio può essere un buffer vertex che contiene le coordinate di trama, normali e di posizione per vertice. Questi dati sono in genere organizzati come set di elementi per vertice, come illustrato nella figura seguente.

![illustrazione di un buffer vertex che contiene i dati relativi alla posizione, al normale e alla trama](images/d3d10-vertex-buffer-element.png)

Questo buffer vertex contiene dati per vertice. ogni vertice archivia tre elementi (posizione, normale e coordinate di trama). La posizione e la normale vengono in genere specificate usando float a 3 32 bit (DXGI \_ Format \_ R32G32B32 \_ float) e le coordinate di trama usando float a 2 32 bit (DXGI \_ Format \_ R32G32 \_ float).

Per accedere ai dati da un buffer vertex è necessario individuare il vertice a cui accedere, oltre ai seguenti parametri aggiuntivi del buffer:

-   Offset: numero di byte dall'inizio del buffer ai dati per il primo vertice. È possibile specificare l'offset usando il metodo [**sul ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) .
-   BaseVertexLocation: numero di byte dall'offset al primo vertice usato dalla chiamata di progetto appropriata.

Prima di creare un buffer vertex, è necessario definirne il layout creando un'interfaccia [**ID3D11InputLayout**](/windows/win32/api/d3d11/nn-d3d11-id3d11inputlayout) ; Questa operazione viene eseguita chiamando il metodo [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout) . Dopo la creazione dell'oggetto layout di input, è possibile associarlo alla fase input-assembler chiamando [**sul ID3D11DeviceContext:: IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).

Per creare un buffer vertex, chiamare [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).

### <a name="index-buffer"></a>Buffer indice

I buffer di indice contengono offset integer nei buffer dei vertici e vengono utilizzati per il rendering più efficiente delle primitive. Un buffer di indice contiene un set sequenziale di indici a 16 bit o a 32 bit; ogni indice viene usato per identificare un vertice in un buffer del vertice. Un buffer di indice può essere visualizzato come illustrato nella figura seguente.

![illustrazione di un buffer di indice](images/d3d10-index-buffer.png)

Gli indici sequenziali archiviati in un buffer di indice si trovano con i parametri seguenti:

-   Offset: numero di byte dall'indirizzo di base del buffer dell'indice. L'offset viene fornito al metodo [**sul ID3D11DeviceContext:: IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer) .
-   StartIndexLocation: specifica il primo elemento buffer index dall'indirizzo di base e l'offset specificato in [**IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer). Il percorso iniziale viene fornito al metodo [**sul ID3D11DeviceContext::D rawindexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) o [**sul ID3D11DeviceContext::D rawindexedinstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) e rappresenta il primo indice di cui eseguire il rendering.
-   IndexCount: numero di indici di cui eseguire il rendering. Il numero viene fornito al metodo [**DrawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)

Inizio del buffer di indice = indirizzo di base buffer di indice + offset (byte) + StartIndexLocation \* ElementSize (byte);

In questo calcolo, ElementSize è la dimensione di ogni elemento del buffer di indice, ovvero due o quattro byte.

Per creare un buffer di indice, chiamare [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).

### <a name="constant-buffer"></a>Buffer costante

Un buffer costante consente di fornire in modo efficiente i dati delle costanti dello shader alla pipeline. È possibile usare un buffer costante per archiviare i risultati della fase di output del flusso. Concettualmente, un buffer costante è simile a un buffer di vertice a elemento singolo, come illustrato nella figura seguente.

![illustrazione di un buffer di costante shader](images/d3d10-shader-resource-buffer.png)

Ogni elemento archivia una costante componente da 1 a 4, determinata dal formato dei dati archiviati. Per creare un buffer di costante dello shader, chiamare [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) e specificare il membro del **\_ \_ \_ buffer costante di binding d3d11** del tipo enumerato del [**\_ \_ flag di associazione d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .

Un buffer costante può utilizzare solo un singolo flag di binding (**d3d11 \_ binding \_ Constant \_ buffer**), che non può essere combinato con qualsiasi altro flag di binding. Per associare un buffer della costante dello shader alla pipeline, chiamare uno dei metodi seguenti: [**sul ID3D11DeviceContext:: GSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetconstantbuffers), [**sul ID3D11DeviceContext::P ssetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers)o [**sul ID3D11DeviceContext:: VSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers).

Per leggere un buffer di costante shader da uno shader, usare una funzione di caricamento HLSL (ad esempio, [**Load**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)). Ogni fase dello shader consente fino a 15 buffer di costanti shader. ogni buffer può ospitare fino a 4096 costanti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer](overviews-direct3d-11-resources-buffers.md)
</dt> </dl>

 

 