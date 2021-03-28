---
title: Introduzione con la fase di Input-Assembler
description: Sono necessari alcuni passaggi per inizializzare la fase di input-assembler (IA).
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901b3facfef781e3f44acf75bee737f280dece55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399267"
---
# <a name="getting-started-with-the-input-assembler-stage"></a>Introduzione con la fase di Input-Assembler

Sono necessari alcuni passaggi per inizializzare la fase di input-assembler (IA). Ad esempio, è necessario creare risorse del buffer con i dati dei vertici necessari per la pipeline, indicare la fase IA in cui si trovano i buffer e il tipo di dati che contengono e specificare il tipo di primitive da assemblare dai dati.

In questo argomento vengono descritte le procedure di base necessarie per la configurazione della fase IA, illustrata nella tabella seguente.



| Passaggio                                                                                    | Descrizione                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Creare buffer di input](#create-input-buffers)                                           | Creare e inizializzare buffer di input con dati dei vertici di input.                                           |
| [Creare l'oggetto Input-Layout](#create-the-input-layout-object)                       | Definire il modo in cui i dati del buffer dei vertici verranno trasmessi nella fase IA usando un oggetto di layout di input. |
| [Associare oggetti alla fase Input-Assembler](#bind-objects-to-the-input-assembler-stage) | Associare gli oggetti creati (buffer di input e l'oggetto layout di input) alla fase IA.                 |
| [Specificare il tipo primitivo](#specify-the-primitive-type)                               | Identificare il modo in cui i vertici verranno assemblati in primitive.                                          |
| [Metodi di richiamo della chiamata](#call-draw-methods)                                                 | Inviare i dati associati alla fase IA tramite la pipeline.                                             |



 

Dopo aver compreso questi passaggi, passare a [utilizzando System-Generated valori](d3d10-graphics-programming-guide-input-assembler-stage-using.md).

## <a name="create-input-buffers"></a>Creare buffer di input

Sono disponibili due tipi di buffer di input: i buffer dei [vertici](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) e gli indici. I buffer vertex forniscono i dati dei vertici alla fase IA. I buffer di indice sono facoltativi. forniscono indici ai vertici dal buffer dei vertici. È possibile creare uno o più buffer vertex e, facoltativamente, un buffer di indice.

Dopo aver creato le risorse del buffer, è necessario creare un oggetto di layout di input per descrivere il layout dei dati alla fase IA, quindi è necessario associare le risorse del buffer alla fase IA. La creazione e l'associazione dei buffer non sono necessari se gli shader non usano i buffer. Per un esempio di un vertice semplice e pixel shader che disegna un singolo triangolo, vedere [uso della fase di Input-Assembler senza buffer](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).

Per informazioni sulla creazione di un buffer vertex, vedere [creare un buffer vertex](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating). Per informazioni sulla creazione di un buffer di indice, vedere creare un buffer di indice.

## <a name="create-the-input-layout-object"></a>Creare l'oggetto Input-Layout

L'oggetto di layout di input incapsula lo stato di input della fase IA. Include una descrizione dei dati di input associati alla fase IA. I dati vengono trasmessi alla fase IA dalla memoria, da uno o più buffer dei vertici. La descrizione identifica i dati di input associati da uno o più buffer vertex e consente al runtime di controllare i tipi di dati di input in base ai tipi di parametro di input dello shader. Questo controllo del tipo non solo verifica che i tipi siano compatibili, ma anche che ogni elemento richiesto dallo shader sia disponibile nelle risorse del buffer.

Viene creato un oggetto di layout di input da una matrice di descrizioni di elementi di input e un puntatore allo shader compilato (vedere [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)). La matrice contiene uno o più elementi di input. ogni elemento di input descrive un singolo elemento di dati vertex da un singolo buffer del vertice. L'intero set di descrizioni degli elementi di input descrive tutti gli elementi dei dati di vertice di tutti i vertex buffer che verranno associati alla fase di assemblaggio dell'input.

Nella descrizione del layout seguente viene descritto un singolo buffer del vertice che contiene tre elementi di dati dei vertici:


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



Una descrizione dell'elemento di input descrive ogni elemento contenuto da un singolo vertice in un buffer del vertice, incluse le dimensioni, il tipo, la posizione e lo scopo. Ogni riga identifica il tipo di dati utilizzando la semantica, l'indice semantico e il formato dati. Una [semantica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) è una stringa di testo che consente di identificare la modalità di utilizzo dei dati. In questo esempio, la prima riga identifica i dati di posizione a 3 componenti (ad esempio,*XYZ*); la seconda riga identifica i dati di trama a 2 componenti (ad esempio,*UV*); e la terza riga identifica i dati normali.

In questo esempio di descrizione di un elemento di input, l'indice semantico, ovvero il secondo parametro, viene impostato su zero per tutte e tre le righe. L'indice semantico consente di distinguere tra due righe che utilizzano la stessa semantica. Poiché in questo esempio non è presente alcuna semantica simile, l'indice semantico può essere impostato sul valore predefinito, pari a zero.

Il terzo parametro è il *formato*. Il formato (vedere [**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) specifica il numero di componenti per ogni elemento e il tipo di dati, che definisce le dimensioni dei dati per ogni elemento. Il formato può essere digitato completamente al momento della creazione della risorsa oppure è possibile creare una risorsa usando un **\_ formato DXGI**, che identifica il numero di componenti in un elemento, ma lascia il tipo di dati non definito.

### <a name="input-slots"></a>Slot di input

I dati entrano nella fase IA tramite input detti *slot di input*, come illustrato nella figura seguente. La fase IA ha *n* slot di input, progettati per ospitare fino a *n* buffer di vertici che forniscono dati di input. Ogni buffer dei vertici deve essere assegnato a uno slot diverso; Queste informazioni vengono archiviate nella dichiarazione di layout di input quando viene creato l'oggetto di layout di input. È anche possibile specificare un offset dall'inizio di ogni buffer al primo elemento nel buffer da leggere.

![illustrazione degli slot di input per la fase IA](images/d3d10-ia-slots.png)

I due parametri successivi sono lo *slot di input* e l' *offset di input*. Quando si usano più buffer, è possibile associarli a uno o più slot di input. L'offset di input è il numero di byte tra l'inizio del buffer e l'inizio dei dati.

### <a name="reusing-input-layout-objects"></a>Riutilizzo di oggetti Input-Layout

Ogni oggetto di layout di input viene creato in base a una firma dello shader. Ciò consente all'API di convalidare gli elementi input-layout-Object rispetto alla firma di input shader per assicurarsi che esista una corrispondenza esatta tra tipi e semantica. È possibile creare un singolo oggetto layout di input per molti shader, purché tutte le firme di input shader corrispondano esattamente.

## <a name="bind-objects-to-the-input-assembler-stage"></a>Associare oggetti alla fase Input-Assembler

Dopo aver creato le risorse del buffer dei vertici e un oggetto layout di input, è possibile associarle alla fase IA chiamando [**sul ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) e [**sul ID3D11DeviceContext:: IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout). Nell'esempio seguente viene illustrata l'associazione di un singolo vertex buffer e di un oggetto di layout di input alla fase IA:


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



Per l'associazione dell'oggetto di layout di input è necessario solo un puntatore all'oggetto.

Nell'esempio precedente viene associato un singolo buffer del vertice; Tuttavia, più buffer dei vertici possono essere associati da una singola chiamata a [**sul ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers)e il codice seguente mostra tale chiamata per associare tre buffer di vertici:


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



Un buffer di indice è associato alla fase IA chiamando [**sul ID3D11DeviceContext:: IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).

## <a name="specify-the-primitive-type"></a>Specificare il tipo primitivo

Una volta associati i buffer di input, è necessario che nella fase IA venga indicato come assemblare i vertici in primitive. Questa operazione viene eseguita specificando il [tipo primitivo](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) chiamando [**sul ID3D11DeviceContext:: IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); il codice seguente chiama questa funzione per definire i dati come un elenco di triangolo senza adiacenza:


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



I restanti tipi primitivi sono elencati nella [**\_ \_ topologia primitiva D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).

## <a name="call-draw-methods"></a>Metodi di richiamo della chiamata

Dopo aver associato le risorse di input alla pipeline, un'applicazione chiama un metodo di disegnare per eseguire il rendering delle primitive. Sono disponibili diversi metodi di estrazione, illustrati nella tabella seguente: Alcuni usano i buffer di indice, alcuni usano i dati dell'istanza e alcuni riutilizzano i dati dalla fase di output di streaming come input per la fase di input-assembler.



| Metodi di estrazione                                                                                  | Descrizione                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**Sul ID3D11DeviceContext::D RAW**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | Creare primitive non indicizzate non indicizzate.                                                            |
| [**Sul ID3D11DeviceContext::D rawInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | Creare primitive con istanze non indicizzate.                                                                |
| [**Sul ID3D11DeviceContext::D rawIndexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | Creare primitive indicizzate senza istanze.                                                                |
| [**Sul ID3D11DeviceContext::D rawIndexedInstanced**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | Creare primitive con indicizzazione e istanze.                                                                    |
| [**Sul ID3D11DeviceContext::D rawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | Tracciare primitive non indicizzate non indicizzate dai dati di input provenienti dalla fase di streaming-output. |



 

Ogni metodo di disegnare esegue il rendering di un singolo tipo di topologia. Durante il rendering, le primitive incomplete (quelle prive di vertici sufficienti, privi di indici, primitive parziali e così via) vengono ignorate automaticamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fase input-assembler](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 