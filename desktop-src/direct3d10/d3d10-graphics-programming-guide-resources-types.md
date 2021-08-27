---
description: 'Tutte le risorse usate dalla pipeline Direct3D derivano da due tipi di risorse di base: buffer e trame. Un buffer è una raccolta di dati non elaborati (elementi); una trama è una raccolta di texel (elementi texture).'
ms.assetid: c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69
title: Tipi di risorse (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0f757eac93fac8c0ffd49641441fa4570824670dfcca9c3d271f954054548b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120105"
---
# <a name="resource-types-direct3d-10"></a>Tipi di risorse (Direct3D 10)

Tutte le risorse usate dalla pipeline Direct3D derivano da due tipi di risorse di base: [buffer](#buffer-resources) e [trame.](#texture-resources) Un buffer è una raccolta di dati non elaborati (elementi); una trama è una raccolta di texel (elementi texture).

-   [Risorse del buffer](#buffer-resources)
    -   [Tipi di buffer](#buffer-types)
-   [Risorse trama](#texture-resources)
    -   [Tipi di trama](#texture-types)
    -   [Sottorisorse](#subresources)
    -   [Tipizzazione forte e debole](#strong-vs-weak-typing)
-   [Argomenti correlati](#related-topics)

Esistono due modi per specificare completamente il layout (o footprint di memoria) di una risorsa:



| Elemento                                                                                                 | Descrizione                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="Typed"></span><span id="typed"></span><span id="TYPED"></span>Digitato<br/>             | Specificare completamente il tipo quando viene creata la risorsa.<br/>               |
| <span id="Typeless"></span><span id="typeless"></span><span id="TYPELESS"></span>Senza tipi<br/> | Specificare completamente il tipo quando la risorsa è associata alla pipeline.<br/> |



 

## <a name="buffer-resources"></a>Risorse del buffer

Una risorsa buffer è una raccolta di dati completamente tipiati. internamente, un buffer contiene elementi. Un elemento è costituito da 1 a 4 componenti. Esempi di tipi di dati degli elementi includono: un valore di dati pack (ad esempio R8G8B8A8), un singolo intero a 8 bit, quattro valori float a 32 bit. Questi tipi di dati vengono usati per archiviare dati, ad esempio un vettore di posizione, un vettore normale, una coordinata di trama in un vertex buffer, un indice in un index buffer o uno stato del dispositivo.

Un buffer viene creato come risorsa non strutturata. Poiché non è strutturato, un buffer non può contenere livelli mipmap, non viene filtrato durante la lettura e non può essere multicampionato.

### <a name="buffer-types"></a>Tipi di buffer

-   [Vertex Buffer](#vertex-buffer)
-   [Buffer indice](#index-buffer)
-   [Buffer costante](#constant-buffer)

### <a name="vertex-buffer"></a>Vertex Buffer

Un buffer è una raccolta di elementi. un buffer dei vertici contiene dati per vertice. L'esempio più semplice è un vertex buffer che contiene un tipo di dati, ad esempio i dati di posizione. Può essere visualizzato come illustrato nella figura seguente.

![Illustrazione di un vertex buffer che contiene i dati di posizione](images/d3d10-resources-single-element-vb2.png)

Più spesso, un vertex buffer contiene tutti i dati necessari per specificare completamente i vertici 3D. Un esempio di questo potrebbe essere un vertex buffer che contiene le coordinate di posizione per vertice, normale e trama. Questi dati sono in genere organizzati come set di elementi per vertice, come illustrato nella figura seguente.

![Illustrazione di un vertex buffer che contiene dati di posizione, normale e trama](images/d3d10-vertex-buffer-element.png)

Questo buffer dei vertici contiene dati per vertice per otto vertici. ogni vertice archivia tre elementi (coordinate di posizione, normale e trama). La posizione e la normale vengono in genere specificate usando tre float a 32 bit (DXGI FORMAT R32G32B32 FLOAT) e le coordinate della trama usando due float a \_ \_ \_ 32 bit (DXGI \_ FORMAT \_ R32G32 \_ FLOAT).

Per accedere ai dati da un vertex buffer, è necessario conoscere il vertice a cui accedere e gli altri parametri del buffer seguenti:

-   Offset: numero di byte dall'inizio del buffer ai dati per il primo vertice. L'offset viene fornito a [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers).
-   BaseVertexLocation: numero di byte dall'offset al primo vertice usato dalla chiamata di disegno appropriata (vedere [Metodi di disegno](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).

Prima di creare un vertex buffer, è necessario definirne il layout creando un [**oggetto di layout di input.**](/windows/win32/api/d3d10/nn-d3d10-id3d10inputlayout) Questa operazione viene eseguita chiamando [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout). Dopo aver creato l'oggetto di layout di input, associarlo alla fase dell'assembler di input chiamando [**IASetInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetinputlayout).

Per creare un vertex buffer, chiamare [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer).

### <a name="index-buffer"></a>Buffer indice

Un index buffer contiene un set sequenziale di indici a 16 o 32 bit. ogni indice viene usato per identificare un vertice in un vertex buffer. L'index buffer con uno o più vertex buffer per fornire dati alla fase IA è detto indicizzazione. Un index buffer può essere visualizzato come illustrato nella figura seguente.

![illustrazione di un index buffer](images/d3d10-index-buffer.png)

Gli indici sequenziali archiviati in un index buffer si trovano con i parametri seguenti:

-   Offset: numero di byte dall'inizio del buffer al primo indice. L'offset viene fornito a [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer).
-   StartIndexLocation: numero di byte dall'offset al primo vertice usato dalla chiamata di disegno appropriata (vedere [Metodi di disegno](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).
-   IndexCount: numero di indici di cui eseguire il rendering.

Per creare un index buffer, chiamare [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer).

Un index buffer può unire più [strisce](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) a linee o triangoli separando ognuna con un indice strip-cut. Un indice strip-cut consente di disegnare più strisce a linee o triangoli con una singola chiamata di disegno. Un indice strip-cut è semplicemente il valore massimo possibile per l'indice (0xffff per un indice a 16 bit, 0xffffffff per un indice a 32 bit). L'indice strip-cut reimposta l'ordine di avvolgimento nelle primitive indicizzate e può essere usato per rimuovere la necessità di triangoli degenerati che altrimenti potrebbero essere necessari per mantenere l'ordine di avvolgimento corretto in una striscia triangolare. Nella figura seguente viene illustrato un esempio di indice strip-cut.

![Illustrazione di un indice strip-cut](images/d3d10-ia-strips-cut-value.png)

### <a name="constant-buffer"></a>Buffer costante

Direct3D 10 ha introdotto un nuovo buffer per fornire costanti shader denominate buffer costanti shader o semplicemente un buffer costante. Concettualmente, è simile a un vertex buffer a elemento singolo, come illustrato nella figura seguente.

![Illustrazione di un buffer costante shader](images/d3d10-shader-resource-buffer.png)

Ogni elemento archivia una costante di componente da 1 a 4, determinata dal formato dei dati archiviati.

I buffer costanti riducono la larghezza di banda necessaria per aggiornare le costanti shader consentendo il raggruppamento e il commit delle costanti shader contemporaneamente anziché effettuare singole chiamate per eseguire il commit di ogni costante separatamente.

Per creare un buffer costante shader, chiamare [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) e specificare il flag di associazione del buffer costante D3D10 \_ BIND CONSTANT BUFFER \_ \_ (vedere [**D3D10 \_ BIND \_ FLAG).**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)

Per associare un buffer costante shader alla pipeline, chiamare uno dei metodi [**seguenti: GSSetConstantBuffers,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers) [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers)o [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers).

Si noti che quando si usa l'interfaccia [**ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) il processo di creazione, associazione e comitting di un buffer costante viene gestito dall'istanza dell'interfaccia **ID3D10Effect.** In tal caso, è necessario ottenere la variabile dall'effetto solo con uno dei metodi GetVariable, ad esempio [**GetVariableByName,**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) e aggiornare la variabile con uno dei metodi SetVariable, ad esempio [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix). Per un esempio di uso **dell'interfaccia ID3D10Effect** per gestire un buffer costante, vedere [l'esercitazione 07](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).

Uno shader continua a leggere le variabili in un buffer costante direttamente in base al nome della variabile nello stesso modo in cui vengono lette le variabili che non fanno parte di un buffer costante.

Ogni fase dello shader consente fino a 15 buffer costanti shader; ogni buffer può contenere fino a 4096 costanti.

Usare un buffer costante per archiviare i risultati della fase di output del flusso.

Vedere [Costanti shader (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-constants.md) per un esempio di dichiarazione di un buffer costante in uno shader.

## <a name="texture-resources"></a>Risorse trama

Una risorsa trama è una raccolta strutturata di dati progettata per archiviare texel. A differenza dei buffer, le trame possono essere filtrate in base ai campionatori di trama mentre vengono lette dalle unità shader. Il tipo di trama influisce sul modo in cui viene filtrata la trama. Un texel rappresenta l'unità più piccola di una trama che può essere letta o scritta dalla pipeline. Ogni texel contiene da 1 a 4 componenti, disposti in uno dei formati DXGI (vedere [**DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).

Le trame vengono create come risorsa strutturata in modo che le relative dimensioni siano note. Tuttavia, ogni trama può essere tipiata o meno al momento della creazione della risorsa, purché il tipo sia completamente specificato usando una vista quando la trama è associata alla pipeline.

-   [Tipi di trama](#texture-types)
-   [Sottorisorse](#subresources)
-   [Tipizzazione forte e debole](#strong-vs-weak-typing)

### <a name="texture-types"></a>Tipi di trama

Esistono diversi tipi di trame: 1D, 2D, 3D, ognuna delle quali può essere creata con o senza mipmap. Direct3D 10 supporta anche matrici di trame e trame multicampionato.

-   [Trama 1D](#1d-texture)
-   [Matrice di trame 1D](#1d-texture-array)
-   [Trama 2D e matrice di trame 2D](#2d-texture-and-2d-texture-array)
-   [Trama 3D](#3d-texture)

### <a name="1d-texture"></a>Trama 1D

Una trama 1D nella forma più semplice contiene dati di trama che possono essere indirizzati con una singola coordinata di trama; può essere visualizzato come matrice di texel, come illustrato nella figura seguente.

![illustrazione di una trama 1D](images/d3d10-1d-texture.png)

Ogni texel contiene una serie di componenti di colore a seconda del formato dei dati archiviati. Aggiungendo maggiore complessità, è possibile creare una trama 1D con livelli mipmap, come illustrato nella figura seguente.

![illustrazione di una trama 1d con livelli mipmap](images/d3d10-resource-texture1d.png)

Un livello mipmap è una trama che è una potenza di due più piccola del livello superiore. Il livello superiore contiene il maggior numero di dettagli, ogni livello successivo è più piccolo; Per una mipmap 1D, il livello più piccolo contiene un texel. I livelli diversi sono identificati da un indice denominato loD (livello di dettaglio); È possibile usare lo strumento LOD per accedere a una trama più piccola quando si esegue il rendering di una geometria non vicina alla fotocamera.

### <a name="1d-texture-array"></a>Matrice di trame 1D

Direct3D 10 include anche una nuova struttura di dati per una matrice di trame. Una matrice di trame 1D ha un aspetto concettuale simile all'illustrazione seguente.

![illustrazione di una matrice di trame 1d](images/d3d10-resource-texture1darray.png)

Questa matrice di trame contiene tre trame. Ognuna delle tre trame ha una larghezza di trama di 5 (ovvero il numero di elementi nel primo livello). Ogni trama contiene anche una mipmap di 3 livelli.

Tutte le matrici di trame in Direct3D sono una matrice omogenea di trame. Ciò significa che ogni trama in una matrice di trame deve avere lo stesso formato e le stesse dimensioni dei dati (inclusi la larghezza della trama e il numero di livelli di mipmap). È possibile creare matrici di trame di dimensioni diverse, purché tutte le trame in ogni matrice corrispondano alle dimensioni.

### <a name="2d-texture-and-2d-texture-array"></a>Trama 2D e matrice di trame 2D

Una risorsa Texture2D contiene una griglia 2D di texel. Ogni texel è indirizzabile da un vettore u, v. Poiché si tratta di una risorsa trama, può contenere livelli mipmap e sottorisorse. Una risorsa trama 2D completamente popolata è simile alla figura seguente.

![illustrazione di una risorsa trama 2D](images/d3d10-resource-texture2d.png)

Questa risorsa di trama contiene una singola trama 3x5 con tre livelli di mipmap.

Una risorsa Texture2DArray è una matrice omogenea di trame 2D. ovvero ogni trama ha lo stesso formato di dati e le stesse dimensioni (inclusi i livelli mipmap). Ha un layout simile a quello della matrice di trame 1D, ad eccezione del fatto che le trame ora contengono dati 2D e pertanto hanno un aspetto simile all'illustrazione seguente.

![illustrazione di una matrice di risorse di trama 2D](images/d3d10-resource-texture2darray.png)

Questa matrice di trame contiene tre trame. ogni trama è 3x5 con due livelli di mipmap.

### <a name="using-a-texture2darray-as-a-texture-cube"></a>Uso di Texture2DArray come cubo di trama

Un cubo di trama è una matrice di trame 2D che contiene 6 trame, una per ogni viso del cubo. Un cubo di trama completamente popolato è simile alla figura seguente.

![illustrazione di una matrice di risorse di trama 2D che rappresentano un cubo di trama](images/d3d10-resource-texturecube.png)

Una matrice di trame 2D che contiene 6 trame può essere letta dagli shader con le funzioni intrinseche della mappa cubo, dopo essere stata associata alla pipeline con una visualizzazione cubo-trama. I cubi di trama vengono indirizzati dallo shader con un vettore 3D che punta dal centro del cubo di trama.

### <a name="3d-texture"></a>Trama 3D

Una risorsa Texture3D (nota anche come trama del volume) contiene un volume 3D di texel. Poiché si tratta di una risorsa trama, può contenere livelli mipmap. Una trama [**3D completamente popolata è**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) simile alla figura seguente.

![illustrazione di una risorsa trama 3D](images/d3d10-resource-texture3d.png)

Quando una sezione mipmap di trama 3D viene associata come output di destinazione di rendering (con una visualizzazione di destinazione di rendering), la trama 3D si comporta in modo identico a una matrice di trame 2D con n sezioni. La sezione di rendering specifica viene scelta dalla fase geometry shader, dichiarando un componente scalare dei dati di output come valore di sistema \_ RenderTargetArrayIndex SV.

Non esiste alcun concetto di matrice di trame 3D. pertanto una sottorisorsa di trama 3D è un singolo livello di mipmap.

### <a name="subresources"></a>Sottorisorse

L'API Direct3D 10 fa riferimento a intere risorse o subset di risorse. Per specificare una parte delle risorse, Direct3D ha coniato il termine sottorisorse, ovvero un subset di una risorsa.

Un buffer è definito come una singola sottorisorsa. Le trame sono un po' più complesse perché esistono diversi tipi di trama (1D, 2D e così via), alcuni dei quali supportano i livelli mipmap e/o le matrici di trame. A partire dal caso più semplice, una trama 1D viene definita come una singola sottorisorsa, come illustrato nella figura seguente.

![illustrazione di una trama 1D](images/d3d10-1d-texture.png)

Ciò significa che la matrice di texel che costituiscono una trama 1D è contenuta in una singola sottorisorsa.

Se si espande una trama 1D con tre livelli di mipmap, è possibile visualizzarla in questo modo.

![illustrazione di una trama 1d con livelli mipmap](images/d3d10-resource-texture1d.png)

Si pensi a questa come a una singola trama che è costituito da tre sottotesti. Ogni sottotesto viene conteggiato come sottorisorsa, quindi questa trama 1D contiene 3 sottorisorse. Un sottotesto (o sottorisorsa) può essere indicizzato usando il livello di dettaglio (LOD) per una singola trama. Quando si usa una matrice di trame, l'accesso a un particolare sottotesto richiede sia il loD che la trama specifica. In alternativa, l'API combina queste due informazioni in un singolo indice di sottorisorsa in base zero, come illustrato di seguito.

![illustrazione di un indice di sottorisorsa in base zero](images/d3d10-resource-texture1darray-sub-indexing.png)

### <a name="selecting-subresources"></a>Selezione di sottorisorse

Alcune API accedono a un'intera risorsa (ad esempio [**CopyResource),**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource)altre a una parte di una risorsa (ad esempio [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource) o [**CopySubresourceRegion).**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) Le API che accedono a una parte di una risorsa usano in genere una descrizione della visualizzazione (ad esempio [**D3D10 \_ TEX2D \_ ARRAY \_ DSV)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)per specificare le sottorisorse a cui accedere.

Queste figure illustrano i termini usati da una descrizione della vista quando si accede a una matrice di trame.

### <a name="array-slice"></a>Sezione matrice

Data una matrice di trame, ogni trama con mipmap, una sezione di matrice (rappresentata dal rettangolo bianco) include una trama e tutti i relativi sottotesti, come illustrato nella figura seguente.

![illustrazione di una giunzione di matrice](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>Sezione Mip

Una sezione mip (rappresentata dal rettangolo bianco) include un livello mipmap per ogni trama in una matrice, come illustrato nella figura seguente.

![illustrazione di una giunzione mip](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>Selezione di una singola sottorisorsa

È possibile usare questi due tipi di sezioni per scegliere una singola sottorisorsa, come illustrato nella figura seguente.

![illustrazione della scelta di una sottorisorsa usando una sezione di matrice e una giunzione mip](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>Selezione di più sottorisorse

Oppure è possibile usare questi due tipi di sezioni con il numero di livelli di mipmap e/o il numero di trame, per scegliere più sottorisorse.

![illustrazione della scelta di più sottorisorse](images/d3d10-resource-subresources-2.png)

Indipendentemente dal tipo di trama in uso, con o senza mipmap, con o senza una matrice di trame, è possibile usare la funzione helper [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource)per calcolare l'indice di una determinata sottorisorsa.

### <a name="strong-vs-weak-typing"></a>Tipizzazione forte e tipizzazione debole

La creazione di una risorsa completamente tipiata limita la risorsa al formato con cui è stata creata. In questo modo il runtime può ottimizzare l'accesso, soprattutto se la risorsa viene creata con flag che indicano che non può essere [mappata](d3d10-graphics-programming-guide-resources-mapping.md) dall'applicazione. Le risorse create con un tipo specifico non possono essere reinterpretate usando il meccanismo di visualizzazione.

In una risorsa di tipo inferiore, il tipo di dati è sconosciuto quando la risorsa viene creata per la prima volta. L'applicazione deve scegliere tra i formati di tipo meno disponibili (vedere [**FORMATO DXGI). \_**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) È necessario specificare le dimensioni della memoria da allocare e se il runtime dovrà generare i sottotesti in un mipmap. Tuttavia, il formato esatto dei dati (se la memoria verrà interpretata come numeri interi, valori a virgola mobile, interi senza segno e così via) non viene determinato fino a quando la risorsa non viene associata alla pipeline con una visualizzazione. Poiché il formato della trama rimane flessibile fino a quando la trama non viene associata alla pipeline, la risorsa viene definita archiviazione con tipi di dati deboli. L'archiviazione con tipi di dati deboli ha il vantaggio di poter essere riutilizzata o reinterpretata (in un altro formato) purché il bit del componente del nuovo formato corrisponda al numero di bit del formato precedente.

Una singola risorsa può essere associata a più fasi della pipeline, purché ognuna abbia una visualizzazione univoca, che qualifica completamente i formati in ogni posizione. Ad esempio, una risorsa creata con il formato DXGI \_ FORMAT \_ R32G32B32A32 TYPELESS può essere usata come INTERFACCIA UTENTE \_ DXGI \_ FORMAT \_ R32G32B32A32 FLOAT e \_ DXGI \_ FORMAT \_ R32G32B32A32 \_ UINT in posizioni diverse della pipeline contemporaneamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
