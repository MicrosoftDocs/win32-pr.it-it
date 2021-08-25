---
title: Attività iniziali con la Input-Assembler di lavoro
description: Per inizializzare la fase input-assembler (IA) sono necessari alcuni passaggi.
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513e7452eebf157a80d4239127bf1d04a014375f7bbaf06e4f5814199d7ba053
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858211"
---
# <a name="getting-started-with-the-input-assembler-stage"></a>Attività iniziali con la Input-Assembler di lavoro

Per inizializzare la fase input-assembler (IA) sono necessari alcuni passaggi. Ad esempio, è necessario creare risorse buffer con i dati dei vertici necessari per la pipeline, indicare alla fase IA dove si trova il buffer e quale tipo di dati contengono e specificare il tipo di primitive da assemblare dai dati.

In questo argomento vengono illustrati i passaggi di base necessari per configurare la fase IA, illustrata nella tabella seguente.



| Passaggio                                                                                    | Descrizione                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Creare buffer di input](#create-input-buffers)                                           | Creare e inizializzare i buffer di input con i dati dei vertici di input.                                           |
| [Creare l'oggetto Input-Layout](#create-the-input-layout-object)                       | Definire la modalità di streaming dei dati del vertex buffer nella fase IA usando un oggetto di layout di input. |
| [Associare oggetti alla Input-Assembler di lavoro](#bind-objects-to-the-input-assembler-stage) | Associare gli oggetti creati (buffer di input e oggetto di layout di input) alla fase IA.                 |
| [Specificare il tipo primitivo](#specify-the-primitive-type)                               | Identificare il modo in cui i vertici verranno assemblati in primitive.                                          |
| [Chiamare i metodi draw](#call-draw-methods)                                                 | Inviare i dati associati alla fase IA tramite la pipeline.                                             |



 

Dopo aver compreso questi passaggi, passare a [Using System-Generated Values](d3d10-graphics-programming-guide-input-assembler-stage-using.md).

## <a name="create-input-buffers"></a>Creare buffer di input

Esistono due tipi di buffer di input: [vertex buffer e](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) buffer di indice. I vertex buffer forniscono i dati dei vertici alla fase IA. I buffer di indice sono facoltativi. forniscono indici ai vertici dal vertex buffer. È possibile creare uno o più vertex buffer e, facoltativamente, un index buffer.

Dopo aver creato le risorse del buffer, è necessario creare un oggetto di layout di input per descrivere il layout dei dati nella fase IA e quindi associare le risorse del buffer alla fase IA. La creazione e l'associazione di buffer non è necessaria se gli shader non usano buffer. Per un esempio di vertice semplice e pixel shader che disegna un singolo triangolo, vedere Using [the Input-Assembler Stage without Buffers](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).

Per informazioni sulla creazione di un vertex buffer, vedere [Creare un vertex buffer](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating). Per informazioni sulla creazione di un index buffer, vedere Creare un buffer di indice.

## <a name="create-the-input-layout-object"></a>Creare l'oggetto Input-Layout

L'oggetto di layout di input incapsula lo stato di input della fase IA. Include una descrizione dei dati di input associati alla fase IA. I dati vengono trasmessi nella fase IA dalla memoria, da uno o più vertex buffer. La descrizione identifica i dati di input associati da uno o più vertex buffer e offre al runtime la possibilità di controllare i tipi di dati di input rispetto ai tipi di parametro di input shader. Questo controllo del tipo non solo verifica che i tipi siano compatibili, ma anche che ognuno degli elementi necessari per lo shader sia disponibile nelle risorse del buffer.

Un oggetto di layout di input viene creato da una matrice di descrizioni degli elementi di input e da un puntatore allo shader compilato (vedere [**ID3D11Device::CreateInputLayout).**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout) La matrice contiene uno o più elementi di input. Ogni elemento di input descrive un singolo elemento vertex-data da un singolo vertex buffer. L'intero set di descrizioni degli elementi di input descrive tutti gli elementi dei dati di vertice di tutti i vertex buffer che verranno associati alla fase di assemblaggio dell'input.

La descrizione del layout seguente descrive un singolo vertex buffer contenente tre elementi vertex-data:


```
D3D11_INPUT_ELEMENT_DESC layout[] =
{
    { L"POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT, 0, 12, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
};
```



Una descrizione dell'elemento di input descrive ogni elemento contenuto in un singolo vertice in un vertex buffer, tra cui dimensioni, tipo, posizione e scopo. Ogni riga identifica il tipo di dati usando la semantica, l'indice semantico e il formato dei dati. Una [semantica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) è una stringa di testo che identifica come verranno usati i dati. In questo esempio la prima riga identifica i dati di posizione a 3 componenti (*xyz*, ad esempio); la seconda riga identifica i dati di trama a 2 componenti (*UV,* ad esempio); e la terza riga identifica i dati normali.

In questo esempio di descrizione di un elemento di input, l'indice semantico (che è il secondo parametro) è impostato su zero per tutte e tre le righe. L'indice semantico consente di distinguere tra due righe che usano la stessa semantica. Poiché in questo esempio non sono presenti semantiche simili, l'indice semantico può essere impostato sul valore predefinito, zero.

Il terzo parametro è il *formato*. Il formato (vedere [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) specifica il numero di componenti per elemento e il tipo di dati, che definisce le dimensioni dei dati per ogni elemento. Il formato può essere digitato completamente al momento della creazione della risorsa oppure è possibile creare una risorsa usando **un formato DXGI \_**, che identifica il numero di componenti in un elemento, ma lascia il tipo di dati indefinito.

### <a name="input-slots"></a>Slot di input

I dati entrano nella fase IA tramite input denominati *slot di input,* come illustrato nella figura seguente. La fase IA ha *n* slot di input, progettati per ospitare fino a *n vertex* buffer che forniscono dati di input. Ogni vertex buffer deve essere assegnato a uno slot diverso. Queste informazioni vengono archiviate nella dichiarazione input-layout quando viene creato l'oggetto input-layout. È anche possibile specificare un offset dall'inizio di ogni buffer al primo elemento del buffer da leggere.

![Illustrazione degli slot di input per la fase ia](images/d3d10-ia-slots.png)

I due parametri successivi sono lo *slot di input e* l'offset di *input*. Quando si usano più buffer, è possibile associarli a uno o più slot di input. L'offset di input è il numero di byte tra l'inizio del buffer e l'inizio dei dati.

### <a name="reusing-input-layout-objects"></a>Riutilizzo Input-Layout oggetti

Ogni oggetto di layout di input viene creato in base a una firma shader; ciò consente all'API di convalidare gli elementi input-layout-object rispetto alla firma di input shader per assicurarsi che sia presente una corrispondenza esatta di tipi e semantica. È possibile creare un singolo oggetto di layout di input per molti shader, purché tutte le firme di input shader corrispondano esattamente.

## <a name="bind-objects-to-the-input-assembler-stage"></a>Associare oggetti alla Input-Assembler di lavoro

Dopo aver creato le risorse del vertex buffer e un oggetto di layout di input, è possibile associarle alla fase IA chiamando [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) e [**ID3D11DeviceContext::IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout). L'esempio seguente illustra l'associazione di un singolo vertex buffer e di un oggetto di layout di input alla fase IA:


```
UINT stride = sizeof( SimpleVertex );
UINT offset = 0;
g_pd3dDevice->IASetVertexBuffers( 
    0,                // the first input slot for binding
    1,                // the number of buffers in the array
    &g_pVertexBuffer, // the array of vertex buffers
    &stride,          // array of stride values, one for each buffer
    &offset );        // array of offset values, one for each buffer

// Set the input layout
g_pd3dDevice->IASetInputLayout( g_pVertexLayout );
```



L'associazione dell'oggetto di layout di input richiede solo un puntatore all'oggetto .

Nell'esempio precedente viene associato un singolo vertex buffer. Tuttavia, è possibile associare più vertex buffer tramite una singola chiamata a [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers)e il codice seguente illustra una chiamata di questo tipo per associare tre vertex buffer:


```
UINT strides[3];
strides[0] = sizeof(SimpleVertex1);
strides[1] = sizeof(SimpleVertex2);
strides[2] = sizeof(SimpleVertex3);
UINT offsets[3] = { 0, 0, 0 };
g_pd3dDevice->IASetVertexBuffers( 
    0,                 //first input slot for binding
    3,                 //number of buffers in the array
    &g_pVertexBuffers, //array of three vertex buffers
    &strides,          //array of stride values, one for each buffer
    &offsets );        //array of offset values, one for each buffer
```



Un index buffer associato alla fase IA chiamando [**ID3D11DeviceContext::IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).

## <a name="specify-the-primitive-type"></a>Specificare il tipo primitivo

Dopo aver associato i buffer di input, alla fase IA deve essere spiegato come assemblare i vertici in primitive. Questa operazione viene eseguita specificando il tipo [primitivo](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) chiamando [**ID3D11DeviceContext::IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); Il codice seguente chiama questa funzione per definire i dati come elenco di triangoli senza adienze:


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



Gli altri tipi primitivi sono elencati in [**TOPOLOGIA PRIMITIVA D3D \_ \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).

## <a name="call-draw-methods"></a>Chiamare i metodi draw

Dopo che le risorse di input sono state associate alla pipeline, un'applicazione chiama un metodo di disegno per eseguire il rendering delle primitive. Nella tabella seguente sono illustrati diversi metodi di disegno. alcuni usano buffer di indice, altri usano i dati dell'istanza e altri riutilizzano i dati dalla fase di streaming-output come input alla fase input-assembler.



| Metodi di disegno                                                                                  | Descrizione                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**ID3D11DeviceContext::D raw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | Disegnare primitive non indicizzate e senza istanze.                                                            |
| [**ID3D11DeviceContext::D rawInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | Disegnare primitive non indicizzate con istanze.                                                                |
| [**ID3D11DeviceContext::D rawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | Disegnare primitive indicizzate e senza istanze.                                                                |
| [**ID3D11DeviceContext::D rawIndexedInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | Disegnare primitive indicizzate con istanze.                                                                    |
| [**ID3D11DeviceContext::D rawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | Disegnare primitive non indicizzate e senza istanza dai dati di input provenienti dalla fase di streaming-output. |



 

Ogni metodo di disegno esegue il rendering di un singolo tipo di topologia. Durante il rendering, le primitive incomplete (quelle senza vertici sufficienti, senza indici, primitive parziali e così via) vengono rimosse automaticamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fase dell'assembler di input](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 