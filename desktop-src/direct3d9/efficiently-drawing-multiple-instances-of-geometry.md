---
description: Data una scena che contiene molti oggetti che usano la stessa geometria, è possibile creare molte istanze di tale geometria con diversi orientamenti, dimensioni, colori e così via con prestazioni notevolmente migliori riducendo la quantità di dati che è necessario fornire al renderer.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Creazione efficiente di più istanze di Geometry (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9981dff913b704fca5e6b211b57e3647fddd28c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876201"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a>Creazione efficiente di più istanze di Geometry (Direct3D 9)

Data una scena che contiene molti oggetti che usano la stessa geometria, è possibile creare molte istanze di tale geometria con diversi orientamenti, dimensioni, colori e così via con prestazioni notevolmente migliori riducendo la quantità di dati che è necessario fornire al renderer.

Questa operazione può essere eseguita tramite l'utilizzo di due tecniche: la prima per il disegno della geometria indicizzata e la seconda per la geometria non indicizzata. Entrambe le tecniche usano due buffer vertex: uno per fornire i dati geometrici e uno per fornire i dati dell'istanza per oggetto. I dati dell'istanza possono essere un'ampia gamma di informazioni, ad esempio una trasformazione, i dati dei colori o i dati di illuminazione, ovvero qualsiasi elemento che è possibile descrivere in una dichiarazione di vertice. Il disegno di molte istanze di Geometry con queste tecniche può ridurre notevolmente la quantità di dati inviati al renderer.

-   [Disegno della geometria indicizzata](#drawing-indexed-geometry)
    -   [Confronto delle prestazioni della geometria indicizzata](#indexed-geometry-performance-comparison)
-   [Disegno di una geometria non indicizzata](#drawing-non-indexed-geometry)
    -   [Confronto tra le prestazioni della geometria non indicizzata](#non-indexed-geometry-performance-comparison)
-   [Argomenti correlati](#related-topics)

## <a name="drawing-indexed-geometry"></a>Disegno della geometria indicizzata

Il buffer vertex contiene dati per vertice definiti da una dichiarazione di vertice. Si supponga che una parte di ogni vertice includa dati di geometria e che parte di ogni vertice includa dati di istanza per oggetto, come illustrato nel diagramma seguente.

![diagramma di un buffer vertex per la geometria indicizzata](images/drawingmultipleinstances.png)

Questa tecnica richiede un dispositivo che supporta il \_ modello di vertex shader da 3 0. Questa tecnica funziona con qualsiasi shader programmabile ma non con la pipeline della funzione fissa.

Per i buffer dei vertici sopra indicati, di seguito sono riportate le dichiarazioni di buffer dei vertici corrispondenti:


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



Queste dichiarazioni definiscono due buffer vertici. La prima dichiarazione (per il flusso 0, indicata dagli zeri nella colonna 1) definisce i dati geometrici che sono costituiti dai dati di coordinate di posizione, normale, tangente, binormale e trama.

La seconda dichiarazione (per il flusso 1, indicata da quelli nella colonna 1) definisce i dati dell'istanza per oggetto. Ogni istanza è definita da numeri a virgola mobile a 4 4 componenti e da un colore a quattro componenti. I primi quattro valori possono essere usati per inizializzare una matrice 4x4, il che significa che questi dati saranno dimensionati in modo univoco, posizionati e ruotano ogni istanza della geometria. I primi quattro componenti usano una semantica delle coordinate di trama che, in questo caso, significa "questo è un numero generale di quattro componenti". Quando si usano dati arbitrari in una dichiarazione di vertice, usare una semantica delle coordinate di trama per contrassegnarla. L'ultimo elemento del flusso viene usato per i dati di colore. Questo può essere applicato nel vertex shader per assegnare a ogni istanza un colore univoco.

Prima di eseguire il rendering, è necessario chiamare [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) per associare i flussi del buffer dei vertici al dispositivo. Di seguito è riportato un esempio che associa entrambi i buffer dei vertici:


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) utilizza [D3DSTREAMSOURCE \_ INDEXEDDATA](other-direct3d-constants.md) per identificare i dati della geometria indicizzata. In questo caso, il flusso 0 contiene i dati indicizzati che descrivono la geometria dell'oggetto. Questo valore viene combinato logicamente con il numero di istanze della geometria da creare.

Si noti che D3DSTREAMSOURCE \_ INDEXEDDATA e il numero di istanze da creare devono sempre essere impostati nel flusso zero.

Nella seconda chiamata, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) utilizza [D3DSTREAMSOURCE \_ INSTANCEDATA](other-direct3d-constants.md) per identificare il flusso contenente i dati dell'istanza. Questo valore viene combinato logicamente con 1 poiché ogni vertice contiene un set di dati dell'istanza.

Le ultime due chiamate a [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) associano i puntatori del buffer del vertice al dispositivo.

Al termine del rendering dei dati dell'istanza, assicurarsi di reimpostare la frequenza del flusso dei vertici sullo stato predefinito, che non utilizza le istanze. Poiché in questo esempio sono stati usati due flussi, impostare entrambi i flussi, come illustrato di seguito:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a>Confronto delle prestazioni della geometria indicizzata

Sebbene non sia possibile creare una singola conclusione su quanto questa tecnica può ridurre il tempo di rendering in ogni applicazione, considerare la differenza nella quantità di dati trasmessi nel runtime e il numero di modifiche di stato che verranno ridotte se si usa la tecnica di creazione di istanze. Questa sequenza di rendering sfrutta i vantaggi della creazione di più istanze della stessa geometria:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



Si noti che il ciclo di rendering viene chiamato una volta, che i dati di geometria vengono trasmessi una sola volta e n istanze viene trasmesso una volta. Questa successiva sequenza di rendering è identica alla funzionalità, ma non sfrutta le istanze:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



Si noti che l'intero ciclo di rendering viene sottoposta a incapsulamento da un secondo ciclo per disegnare ogni oggetto. I dati geometrici vengono ora trasmessi nel renderer n volte (anziché una volta) e gli Stati della pipeline possono anche essere impostati in ridondanza per ogni oggetto disegnato. Questa sequenza di rendering è molto probabile che risulti notevolmente più lenta. Si noti inoltre che i parametri di [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) non sono stati modificati tra i due cicli di rendering.

## <a name="drawing-non-indexed-geometry"></a>Disegno di una geometria non indicizzata

Nel [disegno della geometria indicizzata](#drawing-indexed-geometry), i buffer dei vertici sono stati configurati per disegnare più istanze della geometria indicizzata con maggiore efficienza. È anche possibile usare [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) per creare una geometria non indicizzata. Questa operazione richiede un layout di vertex buffer diverso e presenta vincoli diversi. Per creare una geometria non indicizzata, preparare i buffer del vertice come illustrato nel diagramma seguente.

![diagramma di un buffer vertex per la geometria non indicizzata](images/olderstyleinstancing.png)

Questa tecnica non è supportata dall'accelerazione hardware su qualsiasi dispositivo. È supportato solo dall'elaborazione dei vertici software e funziona solo con gli shader [vs \_ 3 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) .

Poiché questa tecnica funziona con la geometria non indicizzata, non esiste alcun buffer di indice. Come illustrato nel diagramma, il buffer dei vertici che contiene la geometria contiene n copie dei dati geometrici. Per ogni istanza disegnata, i dati di geometria vengono letti dal primo buffer dei vertici e i dati dell'istanza vengono letti dal secondo buffer del vertice.

Di seguito sono riportate le dichiarazioni di buffer vertex corrispondenti:


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



Queste dichiarazioni sono identiche alle dichiarazioni effettuate nell'esempio di geometria indicizzata. Ancora una volta, la prima dichiarazione (per il flusso 0) definisce i dati geometrici e la seconda dichiarazione (per il flusso 1) definisce i dati dell'istanza per oggetto. Quando si crea il primo buffer vertex, assicurarsi di caricarlo con il numero di istanze dei dati geometrici che verranno disegnati.

Prima del rendering, è necessario configurare il divisore che indica al runtime come dividere il primo buffer del vertice in n istanze. Impostare quindi il divisore usando [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) come segue:


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



La prima chiamata a [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) indica che il flusso 0 contiene n istanze di vertici m. [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) associa quindi il flusso 0 al buffer del vertice di geometria.

Nella seconda chiamata, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifica il flusso 1 come origine dei dati dell'istanza. Il secondo parametro è il numero di vertici in ogni oggetto (m). Tenere presente che il flusso di dati dell'istanza deve essere sempre dichiarato come secondo flusso. [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) quindi associa il flusso 1 al buffer vertex che contiene i dati dell'istanza.

Al termine del rendering dei dati dell'istanza, assicurarsi di reimpostare la frequenza del flusso dei vertici sullo stato predefinito. Poiché in questo esempio sono stati usati due flussi, impostare entrambi i flussi, come illustrato di seguito:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a>Confronto tra le prestazioni della geometria non indicizzata

Il vantaggio principale di questo stile di istanza è che può essere utilizzato su una geometria non indicizzata. Sebbene non sia possibile creare una singola conclusione su quanto questa tecnica può ridurre il tempo di rendering in ogni applicazione, considerare la differenza nella quantità di dati trasmessi nel runtime e il numero di modifiche di stato che verranno ridotte per la sequenza di rendering seguente:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



Si noti che il ciclo di rendering viene chiamato una volta. Il flusso dei dati di geometria viene eseguito una sola volta, anche se sono presenti n istanze della geometria da trasmettere. Il flusso dei dati dal buffer del vertice dell'istanza viene eseguito una sola volta. Questa successiva sequenza di rendering è identica alla funzionalità, ma non sfrutta le istanze:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



Senza istanze, il ciclo di rendering deve essere sottoposta a incapsulamento da un secondo ciclo per disegnare ogni oggetto. Eliminando il secondo ciclo di rendering, è necessario prevedere prestazioni migliori a causa di un minor numero di modifiche allo stato di rendering chiamate all'interno del ciclo.

Nel complesso, è ragionevole aspettarsi che la tecnica indicizzata ([disegno della geometria indicizzata](#drawing-indexed-geometry)) risulti migliore rispetto alla tecnica non indicizzata ([disegno di una geometria non indicizzata](#drawing-non-indexed-geometry)) perché la tecnica indicizzata trasmette solo una copia dei dati geometrici. Si noti che i parametri di [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) non sono stati modificati per nessuna delle sequenze di rendering.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati](advanced-topics.md)
</dt> <dt>

[Esempio di istanze](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)
</dt> </dl>

 

 
