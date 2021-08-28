---
description: Data una scena che contiene molti oggetti che usano la stessa geometria, è possibile disegnare molte istanze di tale geometria con orientamenti, dimensioni, colori e così via diversi, con prestazioni notevolmente migliori riducendo la quantità di dati da fornire al renderer.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Disegno efficiente di più istanze di geometria (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70586142b58076e5010083f61aeff360aa245a298e5d010fb487aed8b5843ec8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122371"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a>Disegno efficiente di più istanze di geometria (Direct3D 9)

Data una scena che contiene molti oggetti che usano la stessa geometria, è possibile disegnare molte istanze di tale geometria con orientamenti, dimensioni, colori e così via diversi, con prestazioni notevolmente migliori riducendo la quantità di dati da fornire al renderer.

Questa operazione può essere eseguita tramite l'uso di due tecniche: la prima per disegnare la geometria indicizzata e la seconda per la geometria non indicizzata. Entrambe le tecniche usano due buffer dei vertici: uno per fornire i dati geometrici e uno per fornire i dati dell'istanza per oggetto. I dati dell'istanza possono essere un'ampia gamma di informazioni, ad esempio una trasformazione, dati di colore o dati di illuminazione, fondamentalmente tutto ciò che è possibile descrivere in una dichiarazione di vertice. Il disegno di molte istanze di geometria con queste tecniche può ridurre notevolmente la quantità di dati inviati al renderer.

-   [Disegno di geometria indicizzata](#drawing-indexed-geometry)
    -   [Confronto delle prestazioni delle geometrie indicizzate](#indexed-geometry-performance-comparison)
-   [Disegno di geometria non indicizzata](#drawing-non-indexed-geometry)
    -   [Confronto delle prestazioni delle geometrie non indicizzate](#non-indexed-geometry-performance-comparison)
-   [Argomenti correlati](#related-topics)

## <a name="drawing-indexed-geometry"></a>Disegno di geometria indicizzata

Il buffer dei vertici contiene dati per vertice definiti da una dichiarazione di vertice. Si supponga che una parte di ogni vertice contenga dati geometrici e che parte di ogni vertice contenga dati di istanza per oggetto, come illustrato nel diagramma seguente.

![diagramma di un vertex buffer per la geometria indicizzata](images/drawingmultipleinstances.png)

Questa tecnica richiede un dispositivo che supporti il modello \_ di vertex shader a 3 0. Questa tecnica funziona con qualsiasi shader programmabile, ma non con la pipeline di funzioni fisse.

Per i buffer dei vertici illustrati in precedenza, di seguito sono riportate le dichiarazioni del buffer dei vertici corrispondenti:


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



Queste dichiarazioni definiscono due buffer dei vertici. La prima dichiarazione (per il flusso 0, indicato dagli zeri nella colonna 1) definisce i dati geometrici costituiti dai dati relativi a posizione, normale, tangente, binormale e coordinata della trama.

La seconda dichiarazione (per il flusso 1, indicata da quelle nella colonna 1) definisce i dati dell'istanza per oggetto. Ogni istanza è definita da quattro numeri a virgola mobile a quattro componenti e da un colore a quattro componenti. I primi quattro valori possono essere usati per inizializzare una matrice 4x4, il che significa che questi dati verranno ridimensionati, posizionati e ruotati in modo univoco per ogni istanza della geometria. I primi quattro componenti usano una semantica delle coordinate di trama che, in questo caso, significa "si tratta di un numero generale a quattro componenti". Quando si usano dati arbitrari in una dichiarazione di vertice, usare una semantica delle coordinate di trama per contrassegnarla. L'ultimo elemento del flusso viene usato per i dati di colore. Questo può essere applicato nel vertex shader per assegnare a ogni istanza un colore univoco.

Prima del rendering, è necessario chiamare [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) per associare i flussi del buffer dei vertici al dispositivo. Di seguito è riportato un esempio che associa entrambi i buffer dei vertici:


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



[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) usa [D3DSTREAMSOURCE \_ INDEXEDDATA](other-direct3d-constants.md) per identificare i dati geometrici indicizzati. In questo caso, il flusso 0 contiene i dati indicizzati che descrivono la geometria dell'oggetto. Questo valore viene combinato logicamente con il numero di istanze della geometria da disegnare.

Si noti che D3DSTREAMSOURCE INDEXEDDATA e il numero di istanze da disegnare devono \_ sempre essere impostati nel flusso zero.

Nella seconda chiamata [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) usa [D3DSTREAMSOURCE \_ INSTANCEDATA](other-direct3d-constants.md) per identificare il flusso contenente i dati dell'istanza. Questo valore viene combinato logicamente con 1 perché ogni vertice contiene un set di dati dell'istanza.

Le ultime due chiamate a [**SetStreamSource associano**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) i puntatori del buffer dei vertici al dispositivo.

Al termine del rendering dei dati dell'istanza, assicurarsi di ripristinare lo stato predefinito della frequenza del flusso dei vertici, che non usa la creazione di istanze. Poiché in questo esempio sono stati usati due flussi, impostare entrambi i flussi come illustrato di seguito:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a>Confronto delle prestazioni delle geometrie indicizzate

Anche se non è possibile trarre una singola conclusione su quanto questa tecnica potrebbe ridurre il tempo di rendering in ogni applicazione, considerare la differenza nella quantità di dati trasmessi nel runtime e il numero di modifiche dello stato che verranno ridotte se si usa la tecnica di creazione di istanze. Questa sequenza di rendering sfrutta il disegno di più istanze della stessa geometria:


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



Si noti che il ciclo di rendering viene chiamato una volta, i dati geometry vengono trasmessi una sola volta e n istanze vengono trasmesse una sola volta. La sequenza di rendering successiva ha funzionalità identiche, ma non sfrutta le istanze:


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



Si noti che l'intero ciclo di rendering viene incapsulato da un secondo ciclo per disegnare ogni oggetto. Ora i dati geometry vengono trasmessi nel renderer n volte (anziché una volta) e gli stati della pipeline possono anche essere impostati in modo ridondante per ogni oggetto disegnato. È molto probabile che questa sequenza di rendering sia notevolmente più lenta. Si noti anche che i parametri per [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) non sono cambiati tra i due cicli di rendering.

## <a name="drawing-non-indexed-geometry"></a>Disegno di geometria non indicizzata

In [Drawing Indexed Geometry](#drawing-indexed-geometry)i buffer dei vertici sono stati configurati per disegnare più istanze di geometria indicizzata con maggiore efficienza. È anche possibile usare [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) per disegnare geometria non indicizzata. Questa operazione richiede un layout diverso per il buffer dei vertici e ha vincoli diversi. Per disegnare una geometria non indicizzata, preparare i buffer dei vertici come nel diagramma seguente.

![diagramma di un buffer dei vertici per la geometria non indicizzata](images/olderstyleinstancing.png)

Questa tecnica non è supportata dall'accelerazione hardware in alcun dispositivo. È supportato solo dall'elaborazione dei vertici software e funzionerà solo con [ \_ 3 \_ shader rispetto a 3 0.](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md)

Poiché questa tecnica funziona con la geometria non indicizzata, non è index buffer. Come illustrato nel diagramma, il buffer dei vertici che contiene la geometria contiene n copie dei dati geometrici. Per ogni istanza disegnata, i dati geometrici vengono letti dal primo buffer dei vertici e i dati dell'istanza vengono letti dal secondo buffer dei vertici.

Ecco le dichiarazioni di vertex buffer corrispondenti:


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



Queste dichiarazioni sono identiche alle dichiarazioni effettuate nell'esempio di geometria indicizzata. Ancora una volta, la prima dichiarazione (per il flusso 0) definisce i dati geometry e la seconda dichiarazione (per il flusso 1) definisce i dati dell'istanza per oggetto. Quando si crea il primo buffer dei vertici, assicurarsi di caricarlo con il numero di istanze dei dati geometrici da disegnare.

Prima del rendering, è necessario configurare il divisore che indica al runtime come dividere il primo buffer dei vertici in n istanze. Impostare quindi il divisore usando [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) nel modo seguente:


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



La prima chiamata a [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) indica che il flusso 0 contiene n istanze di m vertici. [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) associa quindi il flusso 0 al buffer dei vertici geometrici.

Nella seconda chiamata [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifica il flusso 1 come origine dei dati dell'istanza. Il secondo parametro è il numero di vertici in ogni oggetto (m). Tenere presente che il flusso di dati dell'istanza deve essere sempre dichiarato come secondo flusso. [**SetStreamSource associa**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) quindi il flusso 1 al buffer dei vertici che contiene i dati dell'istanza.

Al termine del rendering dei dati dell'istanza, assicurarsi di ripristinare lo stato predefinito della frequenza del flusso dei vertici. Poiché in questo esempio sono stati usati due flussi, impostare entrambi i flussi come illustrato di seguito:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a>Confronto delle prestazioni delle geometrie non indicizzate

Il vantaggio principale di questo stile di creazione di istanze è che può essere usato su geometrie non indicizzate. Anche se non è possibile trarre una singola conclusione su quanto questa tecnica potrebbe ridurre il tempo di rendering in ogni applicazione, considerare la differenza nella quantità di dati trasmessi in fase di esecuzione e il numero di modifiche di stato che verranno ridotte per la sequenza di rendering seguente:


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



Si noti che il ciclo di rendering viene chiamato una sola volta. I dati geometry vengono trasmessi una sola volta anche se sono presenti n istanze della geometria trasmesse. I dati del buffer dei vertici dell'istanza vengono trasmessi una sola volta. La sequenza di rendering successiva ha funzionalità identiche, ma non sfrutta le istanze:


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



Senza istanze, il ciclo di rendering deve essere racchiuso in un secondo ciclo per disegnare ogni oggetto. Eliminando il secondo ciclo di rendering, si dovrebbero prevedere prestazioni migliori a causa di un minor numero di modifiche dello stato di rendering chiamate all'interno del ciclo.

In generale, è ragionevole aspettarsi che la tecnica indicizzata ([Drawing Indexed Geometry](#drawing-indexed-geometry)) funzioni meglio della tecnica non indicizzata ([Drawing Non-Indexed Geometry](#drawing-non-indexed-geometry)) perché la tecnica indicizzata esegue il flusso di una sola copia dei dati geometry. Si noti che i parametri [**per DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) non sono stati modificati per nessuna delle sequenze di rendering.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati](advanced-topics.md)
</dt> <dt>

[Esempio di istanze](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)
</dt> </dl>

 

 
