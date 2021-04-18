---
description: 'Tutte le risorse usate dalla pipeline Direct3D derivano da due tipi di risorse di base: buffer e trame. Un buffer è una raccolta di dati non elaborati (elementi); una trama è una raccolta di Texel (elementi della trama).'
ms.assetid: c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69
title: Tipi di risorse (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec6ec9b57a2e504c137d424b19c61f2353d685e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567250"
---
# <a name="resource-types-direct3d-10"></a>Tipi di risorse (Direct3D 10)

Tutte le risorse usate dalla pipeline Direct3D derivano da due tipi di risorse di base: [buffer](#buffer-resources) e [trame](#texture-resources). Un buffer è una raccolta di dati non elaborati (elementi); una trama è una raccolta di Texel (elementi della trama).

-   [Risorse buffer](#buffer-resources)
    -   [Tipi di buffer](#buffer-types)
-   [Risorse di trama](#texture-resources)
    -   [Tipi di trama](#texture-types)
    -   [Sottorisorse](#subresources)
    -   [Confronto tra forte e tipizzazione debole](#strong-vs-weak-typing)
-   [Argomenti correlati](#related-topics)

Esistono due modi per specificare completamente il layout (o footprint di memoria) di una risorsa:



| Elemento                                                                                                 | Descrizione                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="Typed"></span><span id="typed"></span><span id="TYPED"></span>Tipizzato<br/>             | Specificare completamente il tipo quando viene creata la risorsa.<br/>               |
| <span id="Typeless"></span><span id="typeless"></span><span id="TYPELESS"></span>Doverle<br/> | Specificare completamente il tipo quando la risorsa è associata alla pipeline.<br/> |



 

## <a name="buffer-resources"></a>Risorse buffer

Una risorsa buffer è una raccolta di dati completamente tipizzati; internamente, un buffer contiene elementi. Un elemento è costituito da 1 a 4 componenti. Esempi di tipi di dati degli elementi includono: un valore di dati compresso, ad esempio R8G8B8A8, un singolo Integer a 8 bit a 4 32 bit. Questi tipi di dati vengono usati per archiviare i dati, ad esempio un vettore di posizione, un vettore normale, una coordinata di trama in un buffer di vertice, un indice in un buffer di indice o uno stato del dispositivo.

Un buffer viene creato come una risorsa non strutturata. Poiché non è strutturato, un buffer non può contenere alcun livello di mipmap, non viene filtrato durante la lettura e non può essere multicampionato.

### <a name="buffer-types"></a>Tipi di buffer

-   [Buffer vertex](#vertex-buffer)
-   [Buffer indice](#index-buffer)
-   [Buffer costante](#constant-buffer)

### <a name="vertex-buffer"></a>Buffer vertex

Un buffer è una raccolta di elementi. un buffer di vertici contiene dati per vertice. L'esempio più semplice è un vertex buffer che contiene un tipo di dati, ad esempio i dati di posizione. Può essere visualizzato come illustrato nella figura seguente.

![illustrazione di un buffer di vertice che contiene i dati relativi alla posizione](images/d3d10-resources-single-element-vb2.png)

Più spesso, un buffer di vertici contiene tutti i dati necessari per specificare in modo completo i vertici 3D. Un esempio può essere un buffer vertex che contiene le coordinate di trama, normali e di posizione per vertice. Questi dati sono in genere organizzati come set di elementi per vertice, come illustrato nella figura seguente.

![illustrazione di un buffer vertex che contiene i dati relativi alla posizione, al normale e alla trama](images/d3d10-vertex-buffer-element.png)

Questo buffer vertici contiene dati per vertice per otto vertici; ogni vertice archivia tre elementi (posizione, normale e coordinate di trama). La posizione e la normale vengono in genere specificate usando float a 3 32 bit (DXGI \_ Format \_ R32G32B32 \_ float) e le coordinate di trama usando float a 2 32 bit (DXGI \_ Format \_ R32G32 \_ float).

Per accedere ai dati da un buffer vertex, è necessario individuare il vertice a cui accedere e gli altri parametri del buffer:

-   Offset: numero di byte dall'inizio del buffer ai dati per il primo vertice. L'offset viene fornito a [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers).
-   BaseVertexLocation: numero di byte dall'offset al primo vertice usato dalla chiamata di progetto appropriata (vedere [metodi di estrazione](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).

Prima di creare un buffer vertex, è necessario definirne il layout creando un [**oggetto di layout di input**](/windows/win32/api/d3d10/nn-d3d10-id3d10inputlayout). Questa operazione viene eseguita chiamando [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout). Una volta creato l'oggetto di layout di input, associarlo alla fase input-assembler chiamando [**IASetInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetinputlayout).

Per creare un buffer vertex, chiamare [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer).

### <a name="index-buffer"></a>Buffer indice

Un buffer di indice contiene un set sequenziale di indici a 16 bit o a 32 bit; ogni indice viene usato per identificare un vertice in un buffer del vertice. L'uso di un buffer di indice con uno o più buffer di Vertex per fornire dati alla fase IA è denominato indicizzazione. Un buffer di indice può essere visualizzato come illustrato nella figura seguente.

![illustrazione di un buffer di indice](images/d3d10-index-buffer.png)

Gli indici sequenziali archiviati in un buffer di indice si trovano con i parametri seguenti:

-   Offset: numero di byte dall'inizio del buffer al primo indice. L'offset viene fornito a [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer).
-   StartIndexLocation: numero di byte dall'offset al primo vertice usato dalla chiamata di progetto appropriata (vedere [metodi di estrazione](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).
-   IndexCount: numero di indici di cui eseguire il rendering.

Per creare un buffer di indice, chiamare [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer).

Un buffer di indice può unire più [strisce a linee o](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) a un triangolo separandoli con un indice con strip-Cut. Un indice con strip-cut consente di disegnare più strisce a linee o a triangolo con una singola chiamata di disegno. Un indice con strip-Cut è semplicemente il valore massimo possibile per l'indice (0xFFFF per un indice a 16 bit, 0xFFFFFFFF per un indice a 32 bit). L'indice Strip-Cut Reimposta l'ordine di avvolgimento nelle primitive indicizzate e può essere usato per rimuovere la necessità di triangoli degenerati che altrimenti potrebbero essere necessari per mantenere un ordine di avvolgimento appropriato in una striscia di triangolo. Nell'illustrazione seguente viene illustrato un esempio di un indice con strip-Cut.

![illustrazione di un indice con strip-Cut](images/d3d10-ia-strips-cut-value.png)

### <a name="constant-buffer"></a>Buffer costante

In Direct3D 10 è stato introdotto un nuovo buffer per la fornitura di costanti shader denominate buffer costante dello shader o semplicemente un buffer costante. Concettualmente, l'aspetto è analogo a quello di un vertex buffer a elemento singolo, come illustrato nella figura seguente.

![illustrazione di un buffer di costante shader](images/d3d10-shader-resource-buffer.png)

Ogni elemento archivia una costante componente da 1 a 4, determinata dal formato dei dati archiviati.

I buffer costanti consentono di ridurre la larghezza di banda necessaria per aggiornare le costanti dello shader consentendo il raggruppamento e il commit delle costanti dello shader, anziché eseguire chiamate singole per eseguire il commit di ogni costante separatamente.

Per creare un buffer di costante shader, chiamare [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) e specificare il flag di binding constant-buffer bind D3D10 \_ binding \_ Constant \_ buffer (vedere [**D3D10 \_ Bind \_ flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)).

Per associare un buffer di costante shader alla pipeline, chiamare uno dei metodi seguenti: [**GSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers), [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers)o [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers).

Si noti che quando si usa l'interfaccia [**ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) , il processo di creazione, associazione e invio di un buffer costante viene gestito dall'istanza dell' **interfaccia ID3D10Effect** . In tal caso, è solo nescesary ottenere la variabile dall'effetto con uno dei metodi GetVariable, ad esempio [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) , e aggiornare la variabile con uno dei metodi sevariable, ad esempio [**sematrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix). Per un esempio di utilizzo dell' **interfaccia ID3D10Effect** per la gestione di un buffer costante, vedere l' [esercitazione 07](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).

Uno shader continua a leggere le variabili in un buffer costante direttamente in base al nome della variabile, nello stesso modo in cui vengono lette le variabili che non fanno parte di un buffer costante.

Ogni fase dello shader consente fino a 15 buffer di costanti shader. ogni buffer può ospitare fino a 4096 costanti.

Usare un buffer costante per archiviare i risultati della fase di output del flusso.

Vedere [costanti shader (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-constants.md) per un esempio di dichiarazione di un buffer costante in uno shader.

## <a name="texture-resources"></a>Risorse di trama

Una risorsa di trama è una raccolta strutturata di dati progettati per archiviare Texel. A differenza dei buffer, le trame possono essere filtrate in base ai Sampler di trama Man mano che vengono lette dalle unità dello shader. Il tipo di trama influisca sul modo in cui la trama viene filtrata. Un Texel rappresenta l'unità più piccola di una trama che può essere letta o scritta dalla pipeline. Ogni Texel contiene da 1 a 4 componenti, disposti in uno dei formati DXGI (vedere [**il \_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).

Le trame vengono create come una risorsa strutturata in modo che le relative dimensioni siano note. Tuttavia, ogni trama può essere tipizzata o digitare meno in fase di creazione delle risorse, purché il tipo venga specificato completamente utilizzando una visualizzazione quando la trama è associata alla pipeline.

-   [Tipi di trama](#texture-types)
-   [Sottorisorse](#subresources)
-   [Confronto tra forte e tipizzazione debole](#strong-vs-weak-typing)

### <a name="texture-types"></a>Tipi di trama

Sono disponibili diversi tipi di trame: 1D, 2D, 3D, ciascuna delle quali può essere creata con o senza mipmap. Direct3D 10 supporta anche matrici di trame e trame multicampionate.

-   [Trama 1D](#1d-texture)
-   [Matrice di trama 1D](#1d-texture-array)
-   [Trama 2D e matrice di trama 2D](#2d-texture-and-2d-texture-array)
-   [Trama 3D](#3d-texture)

### <a name="1d-texture"></a>Trama 1D

Una trama 1D nella sua forma più semplice contiene dati di trama che possono essere risolti con una singola coordinata di trama; può essere visualizzato come matrice di Texel, come illustrato nella figura seguente.

![illustrazione di una trama 1D](images/d3d10-1d-texture.png)

Ogni Texel contiene diversi componenti colore a seconda del formato dei dati archiviati. Aggiungendo maggiore complessità, è possibile creare una trama 1D con livelli mipmap, come illustrato nella figura seguente.

![illustrazione di una trama 1D con livelli mipmap](images/d3d10-resource-texture1d.png)

Un livello mipmap è una trama che è una potenza di due dimensioni inferiori al livello superiore. Il livello superiore contiene il maggior numero di dettagli, ogni livello successivo è minore; per un mipmap 1D, il livello più piccolo contiene un Texel. I livelli diversi sono identificati da un indice denominato LOD (livello di dettaglio); è possibile usare il valore di LOD per accedere a una trama più piccola quando si esegue il rendering della geometria che non si avvicina alla fotocamera.

### <a name="1d-texture-array"></a>Matrice di trama 1D

Direct3D 10 include anche una nuova struttura di dati per una matrice di trame. Una matrice di trame 1D sembra concettualmente simile alla figura seguente.

![illustrazione di una matrice di trama 1D](images/d3d10-resource-texture1darray.png)

Questa matrice di trame contiene tre trame. Ognuna delle tre trame ha una larghezza di trama pari a 5, ovvero il numero di elementi nel primo livello. Ogni trama contiene anche un mipmap a 3 livelli.

Tutte le matrici di trama in Direct3D sono una matrice omogenea di trame; Ciò significa che ogni trama in una matrice di trame deve avere lo stesso formato e la stessa dimensione dei dati (inclusa la larghezza della trama e il numero di livelli di mipmap). È possibile creare matrici di trama di dimensioni diverse, purché tutte le trame in ogni matrice corrispondano alle dimensioni.

### <a name="2d-texture-and-2d-texture-array"></a>Trama 2D e matrice di trama 2D

Una risorsa Texture2D contiene una griglia 2D di Texel. Ogni Texel è indirizzabile da un vettore u, v. Poiché si tratta di una risorsa di trama, può contenere livelli mipmap e sottorisorse. Una risorsa di trama 2D completamente popolata ha un aspetto simile a quello illustrato nella figura seguente.

![illustrazione di una risorsa di trama 2D](images/d3d10-resource-texture2d.png)

Questa risorsa trama contiene una singola trama 3x5 con tre livelli di mipmap.

Una risorsa Texture2DArray è una matrice omogenea di trame 2D. ovvero ogni trama presenta lo stesso formato di dati e le stesse dimensioni (inclusi i livelli mipmap). Presenta un layout simile a quello della matrice di trama 1D, tranne per il fatto che le trame contengono dati 2D e pertanto sono simili all'illustrazione seguente.

![illustrazione di una matrice di risorse di trama 2D](images/d3d10-resource-texture2darray.png)

Questa matrice di trame contiene tre trame; ogni trama è 3x5 con due livelli di mipmap.

### <a name="using-a-texture2darray-as-a-texture-cube"></a>Uso di un Texture2DArray come cubo di trama

Un cubo di trama è una matrice di trame 2D che contiene 6 trame, una per ogni faccia del cubo. Un cubo di trama completamente popolato ha un aspetto simile a quello illustrato nella figura seguente.

![illustrazione di una matrice di risorse di trama 2D che rappresentano un cubo di trama](images/d3d10-resource-texturecube.png)

Una matrice di trame 2D che contiene 6 trame può essere letta dall'interno degli shader con le funzioni intrinseche della mappa del cubo, dopo che sono state associate alla pipeline con una visualizzazione di trama del cubo. I cubi di trama sono indirizzati dallo shader con un vettore 3D che punta al centro del cubo di trama.

### <a name="3d-texture"></a>Trama 3D

Una risorsa Texture3D (nota anche come trama del volume) contiene un volume 3D di Texel. Poiché si tratta di una risorsa di trama, può contenere livelli mipmap. Una [**trama 3D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) completamente popolata ha un aspetto simile a quello illustrato nella figura seguente.

![illustrazione di una risorsa di trama 3D](images/d3d10-resource-texture3d.png)

Quando una sezione mipmap trama 3D viene associata come output della destinazione di rendering (con una visualizzazione di destinazione del rendering), la trama 3D si comporta in modo identico a una matrice di trama 2D con n sezioni. La sezione di rendering specifica viene scelta dalla fase geometry-shader, dichiarando un componente scalare dei dati di output come \_ valore di sistema RENDERTARGETARRAYINDEX SV.

Non esiste alcun concetto di matrice di trama 3D; una sottorisorsa di trama 3D è quindi un singolo livello di mipmap.

### <a name="subresources"></a>Sottorisorse

L'API Direct3D 10 fa riferimento a intere risorse o subset di risorse. Per specificare una parte delle risorse, Direct3D ha coniato il termine sottorisorse che indica un subset di una risorsa.

Un buffer è definito come una singola risorsa. Le trame sono leggermente più complesse perché sono presenti diversi tipi di trama (1D, 2D e così via), alcuni dei quali supportano i livelli mipmap e/o le matrici di trama. A partire dal caso più semplice, una trama 1D viene definita come una singola risorsa, come illustrato nella figura seguente.

![illustrazione di una trama 1D](images/d3d10-1d-texture.png)

Ciò significa che la matrice di Texel che compongono una trama 1D è contenuta in una singola risorsa.

Se si espande una trama 1D con tre livelli di mipmap, è possibile visualizzarla in questo modo.

![illustrazione di una trama 1D con livelli mipmap](images/d3d10-resource-texture1d.png)

Si può pensare a questo come una singola trama costituita da tre sottotrame. Ogni sottotrama viene conteggiata come una sottorisorsa, quindi questa trama 1D contiene 3 sottorisorse. Una sottotrama (o una sottorisorsa) può essere indicizzata usando il livello di dettaglio (LOD) per una singola trama. Quando si usa una matrice di trame, l'accesso a una determinata sottotrama richiede sia l'oggetto LOD che la trama particolare. In alternativa, l'API combina queste due informazioni in un singolo indice di sottorisorsa in base zero, come illustrato di seguito.

![illustrazione di un indice di sottorisorsa in base zero](images/d3d10-resource-texture1darray-sub-indexing.png)

### <a name="selecting-subresources"></a>Selezione delle sottorisorse

Alcune API accedono a un'intera risorsa, ad esempio [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), altre accedono a una parte di una risorsa, ad esempio [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource) o [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion). Le API che accedono a una parte di una risorsa in genere usano una descrizione della vista, ad esempio [**D3D10 \_ TEX2D \_ array \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv), per specificare le sottorisorse a cui accedere.

Queste figure illustrano i termini usati da una descrizione della vista durante l'accesso a una matrice di trame.

### <a name="array-slice"></a>Sezione matrice

Data una matrice di trame, ogni trama con mipmap, una sezione di matrice (rappresentata dal rettangolo bianco) include una trama e tutte le relative sottotrame, come illustrato nella figura seguente.

![illustrazione di una giunzione di matrici](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>Sezione MIP

Una sezione MIP, rappresentata dal rettangolo bianco, include un livello mipmap per ogni trama in una matrice, come illustrato nella figura seguente.

![illustrazione di una giunzione MIP](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>Selezione di una singola sottorisorsa

È possibile usare questi due tipi di sezioni per scegliere una singola sottorisorsa, come illustrato nella figura seguente.

![illustrazione della scelta di una sottorisorsa usando una sezione della matrice e una giunzione MIP](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>Selezione di più sottorisorse

In alternativa, è possibile usare questi due tipi di sezioni con il numero di livelli di mipmap e/o il numero di trame per scegliere più sottorisorse.

![illustrazione della scelta di più sottorisorse](images/d3d10-resource-subresources-2.png)

Indipendentemente dal tipo di trama usato, con o senza mipmap, con o senza una matrice di trama, è possibile usare la funzione di supporto [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource)per calcolare l'indice di una determinata sottorisorsa.

### <a name="strong-vs-weak-typing"></a>Confronto tra forte e tipizzazione debole

La creazione di una risorsa completamente tipizzata limita la risorsa al formato con cui è stato creato. Ciò consente al runtime di ottimizzare l'accesso, soprattutto se la risorsa viene creata con flag che indicano che non è possibile eseguirne il [mapping](d3d10-graphics-programming-guide-resources-mapping.md) tramite l'applicazione. Le risorse create con un tipo specifico non possono essere riinterpretate mediante il meccanismo di visualizzazione.

In una risorsa di tipo less, il tipo di dati è sconosciuto quando la risorsa viene creata per la prima volta. L'applicazione deve scegliere tra i formati di tipo less disponibili (vedere [**DXGI \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)). È necessario specificare le dimensioni della memoria da allocare e se il runtime dovrà generare le sottotrame in un mipmap. Tuttavia, il formato dei dati esatto (indipendentemente dal fatto che la memoria venga interpretata come numeri interi, valori a virgola mobile, interi senza segno e così via) non viene determinato fino a quando la risorsa non viene associata alla pipeline con una vista. Poiché il formato di trama rimane flessibile finché la trama non è associata alla pipeline, la risorsa viene definita archiviazione debolmente tipizzata. L'archiviazione debolmente tipizzata ha il vantaggio di poter essere riutilizzata o riinterpretata (in un altro formato), purché il bit del nuovo formato corrisponda al numero di bit del formato precedente.

Una singola risorsa può essere associata a più fasi della pipeline, purché ognuna disponga di una visualizzazione univoca, che qualifica completamente i formati in ogni posizione. Ad esempio, una risorsa creata con formato DXGI \_ formato \_ R32G32B32A32 senza \_ tipo può essere usata come \_ formato DXGI \_ R32G32B32A32 \_ float e un \_ formato DXGI \_ R32G32B32A32 uint in \_ posizioni diverse della pipeline simultaneamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
