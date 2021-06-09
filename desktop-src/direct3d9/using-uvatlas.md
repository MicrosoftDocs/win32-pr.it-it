---
description: Molte tecniche di rendering e generazione di contenuto richiedono una mappa univoca e non sovrapposta di un segnale 2D (ad esempio una trama) in una mesh.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Uso di UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8faeaa0a416f6f062c81c4101ff47d5222ca75d
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826329"
---
# <a name="using-uvatlas-direct3d-9"></a>Uso di UVAtlas (Direct3D 9)

> [!NOTE]
> UVAtlas è stato originariamente fornito nella libreria di utilità D3DX9, ora deprecata. La versione più recente è disponibile in [UV Atlas Command-Line Tool (uvatlas.exe).](https://github.com/Microsoft/UVAtlas)

Molte tecniche di rendering e generazione di contenuto richiedono una mappa univoca e non sovrapposta di un segnale 2D (ad esempio una trama) in una mesh. Tali tecniche includono:

-   Mapping normale/spostamento
-   Simulazioni PRT dello spazio delle trame e mappe di luce
-   Disegno di superficie
-   Illuminazione dello spazio trame

La generazione manuale di un mapping UV univoco è spesso dispendiosa in termini di tempo e noiosa; Ciò vale soprattutto quando la geometria di input è complessa ed è necessario un utilizzo efficiente/a bassa distorsione dello spazio della trama. La figura seguente mostra una mesh di esempio e l'at atlas di trama corrispondente.

![Mostra una mesh di esempio e l'at atlas di trama corrispondente.](images/uvatlas1.jpg)

Questo esempio mostra una mesh (a sinistra) e la mappa normale dello spazio UV corrispondente (a destra). Si noti che l'atlas delle trame contiene diversi gruppi o cluster di dati. Ogni cluster è denominato grafico e nell'esempio precedente, displays contiene i dati normali per una parte della mesh.

Le API UVAtlas D3DX generano automaticamente un at atlas ottimale non sovrapposto alle trame. Le API forniscono parametri di input che consentono di:

-   Ridurre al minimo l'estensione, la distorsione e il sottocampionamento della trama.
-   Ottimizzare la densità di creazione di un pacchetto dello spazio tra le trame per un uso efficiente della memoria.
-   Fornire un campionamento uniforme nella rete, riducendo al minimo le discontinuità nella frequenza di campionamento.

## <a name="how-uvatlas-works"></a>Funzionamento di UVAtlas

Le API UVAtlas (vedere Funzioni [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generano un at aterno di trama partizionando una superficie in grafici e impacchettondo i grafici in un aterno di trama. Usare [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) e [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) per eseguire questi passaggi separatamente. oppure usare [**D3DXUVAtlasCrea per**](d3dxuvatlascreate.md) partizionare, parametrizzare e creare un pacchetto in una singola chiamata.

-   [Partizionamento e parametrizzazione di una mesh](#partitioning-and-parameterizing-a-mesh)
-   [Uso di tensori delle metriche integrati per controllare la parametrizzazione](#using-integrated-metric-tensors-to-control-parameterization)
-   [Uso dei dati di adizia per le crease specificate dall'utente](#using-adjacency-data-for-user-specified-creases)
-   [Creazione di un pacchetto di grafici in un Atlas](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a>Partizionamento e parametrizzazione di una mesh

In primo luogo, la mesh viene partizionata in grafici, quindi ogni grafico viene parametrizzato nel proprio \[ spazio UV 0,1. \] Un cilindro può essere parametrizzato da un grafico; Una sfera, d'altra parte, richiederà due grafici, come illustrato nella figura seguente.

![illustrazione di una sfera partizionata in due grafici](images/uvatlas3.jpg)

Una mesh che può essere parametrizzata con un singolo grafico viene classificata come "omeomorfica in un disco", vale a dire che è possibile distribuire un disco all'infinito flessibile e all'infinito e coprire perfettamente la geometria. Questa estensione, detta omomorfismo, è una funzione bidirezionale; ciò significa che è possibile passare da una parametrizzazione all'altra senza perdere informazioni.

Pochissime mesh reali possono essere parametrizzate in due dimensioni senza separare la mesh in cluster o grafici. La figura seguente mostra un'altra mesh di esempio e l'at atlas di trama corrispondente.

![Mostra una mesh di esempio con forme diverse e l'at atlas di trama corrispondente.](images/uvatlas2.jpg)

Esistono due parametri che determinano il numero di grafici creati:

-   Numero massimo di grafici consentiti per l'at atlas
-   Quantità massima di estensione consentita per ogni grafico

La quantità di estensione determinerà il numero di grafici generati e la qualità complessiva del campionamento. L'estensione va da 0,0 (senza estensione) a 1,0 (qualsiasi quantità di estensione). D3DXUVAtlasCreate e D3DXUVAtlasPartition restituiscono l'estensione massima generata dall'algoritmo. La figura seguente mostra un'altra mesh di esempio e l'at atlas di trama corrispondente.

![illustrazione di una mesh di esempio e del relativo at atlas di trama corrispondente](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a>Uso di tensori delle metriche integrati per controllare la parametrizzazione

La priorità dello spazio della trama può essere specificata in base al triangolo. I tensori delle metriche integrati possono essere forniti per controllare il modo in cui i triangoli vengono allungati nell'at atlas dello spazio trame risultante. Gli IMT possono essere specificati direttamente o calcolati in base a un segnale di input usando le funzioni di calcolo D3DX IMT. Un tensore delle metriche integrato (o IMT) è una matrice simmetrica 2x2 che descrive come viene allungato un triangolo nell'ateroso. Ogni IMT è definito da 3 float e li chiama (a,b,c). Possono essere disposti in una matrice simmetrica 2x2 simile alla seguente:


```
a b
b c
```



L'IMT può quindi essere usato per trovare la distanza tra due vettori. Dati due vettori v1 e v2, dove :


```
vector v1
vector v2 = v1 + (s,t)
```



La distanza tra v1 e v2 può essere calcolata come:


```
sqrt((s, t) * M * (s, t)^T)
```



In altre parole, il vettore (s,t) potrebbe essere la grandezza dell'estensione in una direzione arbitraria nello spazio u-v. In questo caso, il vettore s è una direzione dal primo al secondo vertice e t è il prodotto incrociato della normale e di . Ad esempio:


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



Gli IMT possono essere specificati direttamente o calcolati in base a un segnale di input usando le funzioni di calcolo D3DX IMT: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal e grafica D3DXComputeIMTFromTexture. \_

Specificare direttamente i dati IMT se si vuole controllare la modalità di allocazione dello spazio trame ai singoli triangoli. In questo modo, allocare più area nell'at atlas ad aree importanti di una mesh, ad esempio il viso o il logo del logo di un logo del logo del logo di un personaggio o le aree di una scena vicino al percorso a piedi di un giocatore. Specificando gli IMT che sono multipli della matrice di identità, i triangoli risultanti verranno ridimensionati in modo uniforme nello spazio della trama.

Ad esempio, data una mappa normale ad alta risoluzione, è possibile calcolare IMT per fornire più spazio di trama alle aree di segnale di frequenza più elevata nella mappa normale. I triangoli "flat" (mappati alle aree costanti della mappa normale originale) riceveranno meno spazio trame. I triangoli che contengono una grande quantità di dettagli normali della mappa riceveranno un'area di trama maggiore nel risultato finale. È quindi possibile ricampionare la mappa normale in una trama più piccola, ma mantenere i dettagli, oppure è possibile ricalcolare la mappa normale con il mapping UV ottimale.

### <a name="using-adjacency-data-for-user-specified-creases"></a>Uso dei dati di adizia per le crease specificate dall'utente

Le informazioni sull'adicenza definite dall'utente possono essere fornite alla funzione di partizionamento per descrivere le creazioni predefinite nella mesh e quindi definire un limite del grafico tra i visi adiacenti. Si tratta di un modo semplice per il chiamante di specificare il proprio partizionamento del grafico come input nell'algoritmo, che perfeziona ulteriormente i grafici per portare l'estensione al di sotto del massimo consentito.

### <a name="example"></a>Esempio

Questo esempio illustra come è possibile usare le API UVAtlas e DirectX Viewer (Dxviewer.exe) per trovare e correggere le discontinuità nel modello che possono influire notevolmente sulle dimensioni dell'at atlas della trama. È possibile ottenere Dxviewer.exe e ottenere informazioni su di esso da DirectX SDK. Dxviewer.exe è stato rimosso da DirectX SDK dopo la versione di agosto 2009, quindi per ottenerlo è necessario almeno l'SDK di DirectX di agosto 2009. Per informazioni su DirectX SDK, vedere [Dove si trova DirectX SDK?](../directx-sdk--august-2009-.md).

Si supponga di aver iniziato con un modello nel software preferito per la generazione di contenuti(in questo esempio viene utilizzato un modello di testa dwarf creato in Maya). Esportare il modello con trama in un file con estensione x e creare un at atlas di trama con D3DXUVAtlasCreate. L'at atlas risultante per le trame sarà simile all'illustrazione seguente.

![illustrazione di un at atlas per un modello nano](images/uvatlas5.jpg)

L'atlas ha 22 grafici e un'estensione massima di 0,994.

Osservare ora il modello con trame per vedere quanto l'ateroso della trama è mappato alla geometria. A tale scopo, caricare il modello nello strumento visualizzatore:

-   Aprire lo strumento visualizzatore da Utilità DirectX.
-   Caricare il file con estensione x facendo clic sul pulsante Apri.
-   Per abilitare l'opzione di visualizzazione crease, fare clic sul pulsante visualizza e selezionare Creases from popup (Crea da popup).

La figura seguente mostra cosa dovrebbe essere visualizzato nello strumento visualizzatore.

![illustrazione di una mesh con trama nello strumento visualizzatore](images/uvatlas6c.jpg)

Ogni linea è una crease che è un bordo adiacente tra due grafici nell'at atlas della trama. Il numero di grafici generati dall'algoritmo è causato da lievi differenze, probabilmente a causa di discontinuità nelle normali. Queste piccole differenze possono essere ridotte mediante la welding dei dati, ad esempio forzando dati quasi uguali. Per weld the normals and the skinweights:To weld the normals and the skinweights:To weld the normals and the skinweights:

-   Eseguire lo strumento DirectX Ops (dxops.exe) con la riga di comando seguente nella mesh (sostituendo "modelName.x" con il nome del modello):
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

In questo modo vengono confrontati i valori normali e i pesi della interfaccia e, dove il valore è minore di 2,01, i dati vengono resi uguali. Le illustrazioni seguenti mostrano un primo sguardo per vedere le scrissi prima dellalding (a sinistra) e le scrissi dopo lalding (a destra):

![illustrazione delle creazioni prima dellalding](images/uvatlas6a.jpg)![illustrazione delle creazioni dopo lalding](images/uvatlas6b.jpg)

Figura 7: Rimozione di creases mediante la welding

In questo esempio la welding ha rimosso 86 vertici dalla mesh di input. Con un minor numero di sfasamenti nella mesh, è possibile rigenerare l'at atlas, come illustrato nella figura seguente.

![illustrazione del nuovo atlas con le crease rimosse](images/uvatlas8.jpg)

L'atlas ha solo 7 grafici e un'estensione massima di circa 0,0776. Il nuovo at atlas ora si inserisce in una trama più piccola (circa il 30% in questo esempio).

### <a name="packing-charts-into-an-atlas"></a>Creazione di un pacchetto di grafici in un Atlas

Dopo che una mesh è stata partizionata in grafici con parametri singoli, i grafici devono essere suddivisi in modo efficiente in un'unica mappa di trama. Questa operazione viene eseguita come secondo passaggio di D3DXUVAtlasCreate o può essere richiamata in modo esplicito chiamando D3DXUVAtlasPack.

I grafici impacchettati sono separati da una larghezza di margine specificata dall'utente. La larghezza della barra è la quantità di separazione tra i grafici e consente l'interpolazione bilineare e il mapping mip per evitare il rendering degli artefatti ai limiti del grafico. D3DX offre un'interfaccia per il riempimento automatico di questi canali. Per altre informazioni, vedere [**ID3DXTextureGutterHelper.**](id3dxtexturegutterhelper.md)

## <a name="integrating-uvatlas-into-your-pipeline"></a>Integrazione di UVAtlas nella pipeline

Oltre a essere richiamate dall'artista prima della trama, queste funzioni possono essere integrate in una pipeline grafica automatizzata. Ad esempio, una chiamata UVAtlas può essere eseguita automaticamente dopo l'aggiornamento di un asset, prima di eseguire una simulazione PRT o un normale passaggio di mapping. In questo modo si evita la necessità di ripristinare manualmente il mapping UV di un oggetto se la topologia della mesh è stata modificata.

Vedere uv [Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) per un esempio di utilizzo delle funzioni UVAtlas.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati](advanced-topics.md)
</dt> </dl>

 

 
