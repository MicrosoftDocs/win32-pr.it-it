---
description: Non è necessario che le applicazioni usino il filtro trame.
ms.assetid: bba0e485-ac5a-4e43-9eb7-25cd0c90d316
title: Nearest-Point campionamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee8146ce8cfc2d5852cf3847233b431352d69b8bc1f0a52f41da5ac3c9a7c89d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119458761"
---
# <a name="nearest-point-sampling-direct3d-9"></a>Nearest-Point campionamento (Direct3D 9)

Non è necessario che le applicazioni usino il filtro trame. Direct3D può essere impostato in modo da calcolare l'indirizzo texel, che spesso non restituisce numeri interi, e copia il colore del texel con l'indirizzo intero più vicino. Questo processo è denominato campionamento del punto più vicino. Questo può essere un modo rapido ed efficiente per elaborare le trame se le dimensioni della trama sono simili alle dimensioni dell'immagine della primitiva sullo schermo. In caso contrario, la trama deve essere ingrandita o minificata. Il risultato può essere un'immagine a blocchi, con alias o sfocata.

L'applicazione C++ può selezionare il campionamento del punto più vicino chiamando il [**metodo IDirect3DDevice9::SetSamplerState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) Impostare il valore del primo parametro sul numero di indice intero (0-7) della trama per cui si sta selezionando un metodo di filtro trame. Passare D3DSAMP \_ MAGFILTER, D3DSAMP MINFILTER o D3DSAMP MIPFILTER per il secondo parametro per impostare il filtro \_ \_ di ingrandimento, minificazione o mipmapping. Passare D3DTEXF \_ POINT nel terzo parametro.

È consigliabile usare con attenzione il campionamento del punto più vicino, perché talvolta può causare artefatti grafici quando la trama viene campionata al limite tra due texel. Questo limite è la posizione lungo la trama (u o v) in cui il texel campionato passa da un texel a quello successivo. Quando si usa il campionamento a punti, il sistema sceglie un campione di texel o l'altro e il risultato può cambiare improvvisamente da un texel al texel successivo quando il limite viene incrociato. Questo effetto può essere visualizzato come artefatti grafici indesiderati nella trama visualizzata. Quando si usa il filtro lineare, il texel risultante viene calcolato dai texel adiacenti e si unisce uniformemente tra di essi quando l'indice della trama si sposta attraverso il limite.

Questo effetto può essere visualizzato quando si esegue il mapping di una trama molto piccola su un poligono molto grande: un'operazione spesso chiamata ingrandimento. Ad esempio, quando si usa una trama simile a una scacchiera, il campionamento del punto più vicino comporta una scacchiera più grande che mostra bordi distinti. Al contrario, il filtro trame lineare determina un'immagine in cui i colori della scacchiera variano uniformemente nel poligono.

Nella maggior parte dei casi, le applicazioni ricevono i risultati migliori evitando, laddove possibile, il campione del punto più vicino. La maggior parte dell'hardware è attualmente ottimizzata per il filtro lineare, quindi l'applicazione non deve subire prestazioni ridotte. Se l'effetto desiderato richiede assolutamente l'uso del campionamento del punto più vicino, ad esempio quando si usano trame per visualizzare caratteri di testo leggibili, l'applicazione deve essere estremamente attenta a evitare il campionamento ai limiti del texel, che potrebbe causare effetti indesiderati. La figura seguente mostra l'aspetto di questi elementi.

![Illustrazione di una casella a sei sezioni con linee orizzontali non contigue nei due quadrati in alto a destra](images/ptrtfct.png)

Si noti che i due quadrati in alto a destra del gruppo appaiono diversi rispetto ai rispettivi vicini, con offset diagonali che li attraversano. Per evitare artefatti grafici come questi, è necessario avere familiarità con le regole di campionamento trame Direct3D per il filtro del punto più vicino. Direct3D esegue il mapping di una coordinata di trama a virgola mobile compresa tra \[ 0,0, 1,0 (da 0,0 a 1,0 inclusi) a un valore di spazio intero texel compreso tra \] \[ - 0,5, n - 0,5 , dove n è il numero di texel in una determinata dimensione \] nella trama. L'indice di trama risultante viene arrotondato all'intero più vicino. Questo mapping può introdurre imprecisioni di campionamento ai limiti del texel.

Per un esempio semplice, si immagini un'applicazione che esegue il rendering dei poligoni con la modalità di indirizzamento della trama WRAP D3DTADDRESS. \_ Usando il mapping utilizzato da Direct3D, l'indice di trama u viene mappato come illustrato nel diagramma seguente per una trama con una larghezza di 4 texel.

![diagramma delle coordinate di trama 0.0 e 1.0 al limite tra i texel](images/ptsmpprb.png)

Si noti che le coordinate della trama, 0,0 e 1,0 per questa illustrazione, sono esattamente al limite tra i texel. Usando il metodo con cui Direct3D esegue il mapping dei valori, le coordinate della trama sono da \[ - 0,5, 4 a 0,5 , dove 4 è la larghezza \] della trama. In questo caso, il texel campionato è il texel 0 per un indice di trama di 1,0. Tuttavia, se la coordinata della trama è leggermente inferiore a 1,0, il texel campionato sarà il texel n anziché il texel 0.

L'implicazione di questo è che l'ingrandimento di una trama di piccole dimensioni usando coordinate di trama esattamente 0,0 e 1,0 con il filtro del punto più vicino su un triangolo allineato allo spazio dello schermo determina i pixel per cui la mappa trama viene campionata al limite tra texel. Eventuali imprecisioni nel calcolo delle coordinate della trama, per quanto piccole, comportano artefatti lungo le aree dell'immagine sottoposta a rendering che corrispondono ai bordi texel della mappa trama.

L'esecuzione di questo mapping di coordinate di trama a virgola mobile a texel interi con precisione perfetta è difficile, dispendiosa dal punto di vista del calcolo e in genere non è necessaria. La maggior parte delle implementazioni hardware usa un approccio iterativo per il calcolo delle coordinate della trama in ogni posizione di pixel all'interno di un triangolo. Gli approcci iterativi tendono a nascondere queste imprecisioni perché gli errori vengono accumulati in modo uniforme durante l'iterazione.

Il rasterizzatore di riferimento Direct3D usa un approccio di valutazione diretta per il calcolo degli indici di trama in ogni posizione dei pixel. La valutazione diretta differisce dall'approccio iterativo in quanto qualsiasi imprecisione nell'operazione presenta una distribuzione degli errori più casuale. Il risultato è che gli errori di campionamento che si verificano ai limiti possono essere più evidenti perché il rasterizzatore di riferimento non esegue questa operazione con una precisione perfetta.

L'approccio migliore consiste nell'usare il filtro del punto più vicino solo quando necessario. Quando è necessario usarlo, è consigliabile compensare leggermente le coordinate della trama dalle posizioni limite per evitare artefatti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtro trame](texture-filtering.md)
</dt> </dl>

 

 
