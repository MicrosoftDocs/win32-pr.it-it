---
description: Molte tecniche di rendering e generazione di contenuto richiedono una mappa univoca non sovrapposta di un segnale 2D, ad esempio una trama, su una rete mesh.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Uso di UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b335dd6ea94a3db0c0760b0d07a0b8df3fe4c7c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104234407"
---
# <a name="using-uvatlas-direct3d-9"></a>Uso di UVAtlas (Direct3D 9)

Molte tecniche di rendering e generazione di contenuto richiedono una mappa univoca non sovrapposta di un segnale 2D, ad esempio una trama, su una rete mesh. Tali tecniche includono:

-   Mapping normale/spostamento
-   Texture-simulazioni PRT di spazio e mappe chiare
-   Disegno della superficie
-   Illuminazione dello spazio di trama

La generazione manuale di un mapping UV univoco è spesso noiosa e dispendiosa in termini di tempo. Ciò è particolarmente vero quando la geometria di input è complessa ed efficiente/a bassa distorsione. si desidera utilizzare lo spazio. La figura seguente mostra una mesh di esempio e il relativo Atlante di trama corrispondente.

![Mostra una mesh di esempio e il relativo Atlante di trama corrispondente.](images/uvatlas1.jpg)

Questo esempio mostra una mesh (a sinistra) e la mappa normale dello spazio UV corrispondente (sulla destra). Si noti che l'Atlante di trama contiene diversi gruppi o cluster di dati; ogni cluster è denominato grafico e nell'esempio precedente, Visualizza contiene i dati normali per una parte della mesh.

Le API UVAtlas di D3DX generano automaticamente un Atlante di trama ottimale non sovrapposto. Le API forniscono parametri di input che consentono di:

-   Ridurre al minimo l'estensione della trama, la distorsione e il sottocampionamento.
-   Massimizza la densità di compressione dello spazio di trama per un uso efficiente della memoria.
-   Fornire un campionamento uniforme sulla rete, riducendo al minimo le discontinuità nella frequenza di campionamento.

## <a name="how-uvatlas-works"></a>Funzionamento di UVAtlas

Le API UVAtlas (vedere [funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generano un Atlante di trama partizionando una superficie nei grafici e imballando i grafici in un Atlante di trama. Usare [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) e [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) per eseguire questi passaggi separatamente. in alternativa, usare [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) per partizionare, parametrizzare e comprimere in un'unica chiamata.

-   [Partizionamento e parametrizzazione di una mesh](#partitioning-and-parameterizing-a-mesh)
-   [Uso di tensori metrici integrati per controllare la parametrizzazione](#using-integrated-metric-tensors-to-control-parameterization)
-   [Utilizzo di dati adiacenza per le pieghe specificate dall'utente](#using-adjacency-data-for-user-specified-creases)
-   [Compressione dei grafici in un Atlante](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a>Partizionamento e parametrizzazione di una mesh

In primo luogo, la mesh viene partizionata in grafici, quindi ogni grafico viene sottoposto a parametrizzazione in un proprio \[ \] spazio UV di 0, 1. Un cilindro può essere parametrizzato da un grafico; una sfera è invece necessaria per due grafici, come illustrato nella figura seguente.

![illustrazione di una sfera partizionata in due grafici](images/uvatlas3.jpg)

Una mesh che può essere parametrizzata con un singolo grafico è classificata come "omeomorfo su un disco", vale a dire che è possibile distribuire un disco infinitamente flessibile e infinitamente estensibile sul grafico e coprire la geometria perfettamente. Questa estensione, denominata omeomorfismo, è una funzione bidirezionale. Ciò significa che è possibile passare da una parametrizzazione all'altra senza perdere le informazioni.

Pochissime mesh reali possono essere parametrizzate in due dimensioni senza separare la mesh in cluster o grafici. La figura seguente mostra un altro mesh di esempio e il relativo Atlante di trama corrispondente.

![Mostra un esempio di mesh con forme diverse e il relativo Atlante di trama corrispondente.](images/uvatlas2.jpg)

Sono disponibili due parametri che determinano il numero di grafici creati:

-   Numero massimo di grafici consentiti per l'Atlante
-   Quantità massima di estensione consentita per ogni grafico

La quantità di estensione determinerà il numero di grafici generati e la qualità complessiva del campionamento. L'estensione varia da 0,0 (nessun tratto) a 1,0 (qualsiasi quantità di estensione). D3DXUVAtlasCreate e D3DXUVAtlasPartition restituiscono l'estensione massima generata dall'algoritmo. La figura seguente mostra un altro mesh di esempio e il relativo Atlante di trama corrispondente.

![illustrazione di una mesh di esempio e dell'Atlante di trama corrispondente](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a>Uso di tensori metrici integrati per controllare la parametrizzazione

La definizione delle priorità dello spazio di trama può essere specificata in base ai singoli triangoli. È possibile fornire i tensori di metrica integrati per controllare il modo in cui i triangoli vengono estesi nell'Atlante di spazio di trama risultante. Gli IMT possono essere specificati direttamente o calcolati in base a un segnale di input usando le funzioni di calcolo di D3DX IMT. Un tensore di metrica integrato (o IMT) è una matrice 2x2 simmetrica che descrive il modo in cui un triangolo viene esteso nell'Atlante. Ogni IMT è definito da 3 float, chiamati (a, b, c). Possono essere disposte in una matrice simmetrica 2x2 come la seguente:


```
a b
b c
```



È quindi possibile usare IMT per trovare la distanza tra due vettori. Dati due vettori v1 e V2, dove:


```
vector v1
vector v2 = v1 + (s,t)
```



La distanza tra V1 e V2 può essere calcolata come segue:


```
sqrt((s, t) * M * (s, t)^T)
```



In altre parole, il vettore (s, t) potrebbe essere la grandezza dell'estensione in una direzione arbitraria nello spazio u-v. In questo caso, il vettore s corrisponde a una direzione dal primo al secondo vertice e t è il prodotto incrociato di Normal e s. Ad esempio:


```
(1,1) * (1,1) = (2,2)
        (1,1)
IMT(1,1,1) scales by 2
```




```
(1,-1) * (1,1) = (0,0)
         (1,1)
IMT(2,0,2) scales by 2 with no shearing
```



Gli IMT possono essere specificati direttamente o calcolati in base a un segnale di input usando le funzioni di calcolo di D3DX IMT: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal e D3DXComputeIMTFromTexture \_ Graphics.

Specificare direttamente i dati di IMT se si vuole controllare il modo in cui lo spazio di trama viene allocato ai singoli triangoli. In questo modo, allocare più area nell'Atlante a aree importanti di una mesh (ad esempio, il volto di un carattere o il logo toracico o le aree di una scena vicino a walking-path). Specificando gli IMT che sono multipli della matrice di identità, i triangoli risultanti verranno ridimensionati in modo uniforme nello spazio di trama.

Ad esempio, data una mappa normale ad alta risoluzione, è possibile calcolare IMT per fornire più spazio di trama a aree con un segnale di frequenza superiore nella mappa normale. I triangoli "flat", che sono mappati a aree costanti della mappa normale originale, riceveranno uno spazio di trama minore. I triangoli che contengono una grande quantità di dettagli della mappa normale riceveranno più area di trama nel risultato finale. È quindi possibile ricampionare la mappa normale in una trama più piccola, ma mantenere i dettagli, oppure è possibile ricalcolare la mappa normale con il mapping UV più ottimale.

### <a name="using-adjacency-data-for-user-specified-creases"></a>Utilizzo di dati adiacenza per le pieghe specificate dall'utente

Le informazioni adiacenza definite dall'utente possono essere fornite alla funzione di partizionamento per descrivere le pieghe predefinite nella rete e quindi definire un limite del grafico tra i visi adiacenti. Si tratta di un modo semplice per consentire al chiamante di specificare il proprio partizionamento del grafico come input nell'algoritmo, che consente di perfezionare ulteriormente i grafici in modo da portare l'estensione al di sotto del valore massimo consentito.

### <a name="example"></a>Esempio

Questo esempio illustra come usare le API UVAtlas e il Visualizzatore DirectX (Dxviewer.exe) per individuare e correggere le discontinuità nel modello che può influire in modo significativo sulle dimensioni dell'Atlante della trama. È possibile ottenere Dxviewer.exe e ottenere informazioni su di esso da DirectX SDK. Dxviewer.exe è stata rimossa da DirectX SDK dopo la versione agosto 2009, quindi per ottenerla è necessario almeno l'SDK di DirectX 2009 di agosto. Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).

Si supponga di iniziare con un modello nel software di generazione del contenuto preferito (in questo esempio viene usato un modello Head Nano creato in Maya). Esportare il modello con trama in un file con estensione x e creare un Atlante di trama con D3DXUVAtlasCreate. L'Atlante di trama risultante avrà un aspetto simile a quello illustrato nella figura seguente.

![illustrazione di un atlante per un modello nano](images/uvatlas5.jpg)

L'Atlante è costituito da 22 grafici e da un tratto massimo di 0,994.

A questo punto, esaminare il modello con trama per vedere il modo in cui viene eseguito il mapping tra l'Atlante della trama e la geometria. A tale scopo, caricare il modello nello strumento Visualizzatore:

-   Aprire lo strumento Visualizzatore da DirectX Utilities.
-   Caricare il file con estensione x facendo clic sul pulsante Apri.
-   Per abilitare l'opzione di visualizzazione delle pieghe, fare clic sul pulsante Visualizza e selezionare le pieghe dal popup.

Nell'illustrazione seguente vengono mostrati gli elementi che dovrebbero essere visualizzati nello strumento Visualizzatore.

![illustrazione di una mesh con trama nello strumento Visualizzatore](images/uvatlas6c.jpg)

Ogni riga è una piega che rappresenta un bordo adiacente tra due grafici nell'Atlante della trama. Il numero di grafici generati dall'algoritmo è causato da lievi differenze, probabilmente a causa di discontinuità nei normali. Queste piccole differenze possono essere ridotte mediante i dati di saldatura, ovvero forzando i dati che sono quasi uguali. Per saldare i normali e il skinweights:

-   Eseguire lo strumento DirectX Ops (dxops.exe) con la riga di comando seguente sulla mesh (sostituendo ' modelname. x ' con il nome del modello):
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

Ciò consente di confrontare i valori normali e skinweights e la posizione in cui si differenziano per un valore inferiore a 2,01, i dati vengono resi uguali. Le illustrazioni seguenti mostrano un primo sguardo per visualizzare le pieghe prima della saldatura (a sinistra) e le pieghe dopo la saldatura (a destra):

![illustrazione delle pieghe prima della saldatura](images/uvatlas6a.jpg)![illustrazione delle pieghe dopo la saldatura](images/uvatlas6b.jpg)

Figura 7: rimozione di pieghe mediante saldatura

In questo esempio, la saldatura ha rimosso 86 vertici dalla mesh di input. Con un minor numero di pieghe nella rete, è possibile rigenerare l'Atlante, come illustrato nella figura seguente.

![illustrazione del nuovo Atlante con le pieghe rimosse](images/uvatlas8.jpg)

L'Atlante dispone solo di 7 grafici e un'estensione massima di circa 0,0776. Il nuovo Atlante si inserisce ora in una trama più piccola (circa il 30% di dimensioni inferiori in questo esempio).

### <a name="packing-charts-into-an-atlas"></a>Compressione dei grafici in un Atlante

Una volta partizionata una mesh in grafici con parametri singoli, i grafici devono essere compressi in modo efficiente in un'unica mappa di trama. Questa operazione viene eseguita come secondo passaggio di D3DXUVAtlasCreate o può essere richiamata in modo esplicito chiamando D3DXUVAtlasPack.

I grafici compressi sono separati da una larghezza di gronda specificata dall'utente. La larghezza della barra di navigazione è la quantità di separazione tra i grafici e consente l'interpolazione bilineare e il mapping MIP per evitare il rendering degli artefatti ai limiti del grafico. D3DX fornisce un'interfaccia per la compilazione automatica di queste grondaie. per ulteriori informazioni, vedere [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .

## <a name="integrating-uvatlas-into-your-pipeline"></a>Integrazione di UVAtlas nella pipeline

Oltre a essere richiamati dall'artista prima del disegno della trama, queste funzioni possono essere integrate in una pipeline grafica automatizzata. Ad esempio, una chiamata UVAtlas può essere eseguita automaticamente dopo l'aggiornamento di un asset, prima di eseguire una simulazione PRT o il normale passaggio di mapping. In questo modo si evita di dover eseguire manualmente il ripristino manuale del mapping UV di un oggetto se la topologia della mesh è stata modificata.

Vedere lo [strumento di Command-Line UV Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx) , ad esempio utilizzo delle funzioni UVAtlas.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati](advanced-topics.md)
</dt> </dl>

 

 
