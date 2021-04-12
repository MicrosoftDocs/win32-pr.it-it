---
description: Non è necessario che le applicazioni utilizzino il filtro della trama.
ms.assetid: bba0e485-ac5a-4e43-9eb7-25cd0c90d316
title: Campionamento Nearest-Point (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11cf98ee917b124b35f3c30ff263365ec3c46e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401193"
---
# <a name="nearest-point-sampling-direct3d-9"></a>Campionamento Nearest-Point (Direct3D 9)

Non è necessario che le applicazioni utilizzino il filtro della trama. Direct3D può essere impostato in modo da calcolare l'indirizzo di Texel, che spesso non restituisce Integer, e copia il colore del Texel con l'indirizzo integer più vicino. Questo processo è denominato campionamento del punto più vicino. Questo può essere un modo rapido ed efficiente per elaborare le trame se la dimensione della trama è simile alla dimensione dell'immagine della primitiva sullo schermo. In caso contrario, la trama deve essere ingrandita o minimizzati. Il risultato può essere un'immagine chunked, con alias o sfocata.

L'applicazione C++ può selezionare il campionamento dei punti più vicini chiamando il metodo [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Impostare il valore del primo parametro sul numero di indice Integer (0-7) della trama per cui si seleziona un metodo di filtro della trama. Passare D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER o D3DSAMP \_ MIPFILTER per il secondo parametro per impostare il filtro di ingrandimento, minification o mapping MIP. Passare \_ il punto D3DTEXF nel terzo parametro.

È consigliabile usare attentamente il campionamento dei punti più vicini, perché talvolta può causare artefatti grafici quando la trama viene campionata al limite tra due Texel. Questo limite è la posizione lungo la trama (u o v) in cui il Texel campionato passa da un Texel a quello successivo. Quando si usa il campionamento dei punti, il sistema sceglie un Texel di esempio o l'altro e il risultato può cambiare bruscamente da un Texel al Texel successivo quando il limite viene attraversato. Questo effetto può essere visualizzato come elementi grafici indesiderati nella trama visualizzata. Quando si usa il filtro lineare, il Texel risultante viene calcolato da entrambi i Texel adiacenti e si fonde armoniosamente tra di essi quando l'indice di trama passa attraverso il limite.

Questo effetto si verifica quando si esegue il mapping di una trama molto piccola su un poligono di dimensioni molto grandi: un'operazione spesso denominata ingrandimento. Ad esempio, quando si usa una trama simile a una scacchiera, il campionamento del punto più vicino genera una scacchiera più grande che Mostra bordi distinti. Al contrario, il filtro di trama lineare produce un'immagine in cui i colori della scacchiera variano in modo uniforme nel poligono.

Nella maggior parte dei casi, le applicazioni ricevono i migliori risultati evitando laddove possibile il campione più vicino. La maggior parte dell'hardware oggi è ottimizzata per i filtri lineari, quindi l'applicazione non deve soffrire di prestazioni ridotte. Se l'effetto desiderato richiede assolutamente l'uso del campionamento dei punti più vicino, ad esempio quando si usano trame per visualizzare caratteri di testo leggibili, l'applicazione deve prestare molta attenzione a evitare il campionamento ai limiti di Texel, che potrebbero causare effetti indesiderati. Nella figura seguente sono illustrati gli elementi che possono essere simili.

![illustrazione di una casella a sei sezioni con linee orizzontali non continue nei due quadrati superiore destro](images/ptrtfct.png)

Si noti che i due quadrati nella parte superiore destra del gruppo appaiono diversi dagli elementi adiacenti, con offset diagonali in esecuzione. Per evitare artefatti grafici come questi, è necessario avere familiarità con le regole di campionamento di trama Direct3D per il filtro dei punti più vicino. Direct3D esegue il mapping di una coordinata di trama a virgola mobile compresa tra \[ 0,0, 1,0 \] (da 0,0 a 1,0, inclusi) a un valore dello spazio di Texel intero compreso tra \[ -0,5 e n-0,5 \] , dove n è il numero di Texel in una determinata dimensione sulla trama. L'indice di trama risultante viene arrotondato all'intero più vicino. Questo mapping può introdurre inesattezze di campionamento ai limiti di Texel.

Per un esempio semplice, si supponga che un'applicazione esegua il rendering dei poligoni con la \_ modalità di indirizzamento della trama D3DTADDRESS wrap. Usando il mapping usato da Direct3D, l'indice di trama u viene mappato come illustrato nel diagramma seguente per una trama con una larghezza di 4 Texel.

![diagramma delle coordinate di trama 0,0 e 1,0 al confine tra i Texel](images/ptsmpprb.png)

Si noti che le coordinate di trama 0,0 e 1,0 per questa illustrazione sono esattamente al confine tra i Texel. Utilizzando il metodo in base al quale Direct3D esegue il mapping dei valori, le coordinate di trama variano da \[ -0,5, 4-0,5 \] , dove 4 è la larghezza della trama. Per questo caso, il Texel campione è il Texel 0 per un indice di trama 1,0. Tuttavia, se la coordinata di trama era solo leggermente inferiore a 1,0, il Texel campione sarebbe il Texel n anziché il Texel 0.

L'implicazione è che l'ingrandimento di una trama di piccole dimensioni usando le coordinate di trama esattamente 0,0 e 1,0 con il filtro del punto più vicino in un triangolo allineato allo spazio dello schermo restituisce pixel per i quali viene campionata la mappa di trama al confine tra i Texel. Eventuali inesattezze nel calcolo di coordinate di trama, tuttavia di dimensioni ridotte, generano artefatti lungo le aree dell'immagine di cui è stato eseguito il rendering che corrispondono ai bordi Texel della mappa di trama.

L'esecuzione di questo mapping delle coordinate di trama a virgola mobile a Texel di tipo integer con accuratezza perfetta è un'operazione complessa, che richiede molto tempo e non è in genere necessaria. La maggior parte delle implementazioni hardware usa un approccio iterativo per calcolare le coordinate di trama in ogni posizione dei pixel all'interno di un triangolo. Gli approcci iterativi tendono a nascondere queste imprecisioni perché gli errori vengono accumulati uniformemente durante l'iterazione.

L'rasterizzazione dei riferimenti Direct3D usa un approccio di valutazione diretta per il calcolo degli indici di trama in ogni posizione dei pixel. La valutazione diretta differisce dall'approccio iterativo in quanto qualsiasi inesattezza nell'operazione presenta una distribuzione degli errori più casuale. Il risultato è che gli errori di campionamento che si verificano ai limiti possono essere più evidenti perché l'rasterizzazione dei riferimenti non esegue questa operazione con una precisione perfetta.

L'approccio migliore consiste nell'usare il filtro dei punti più vicini solo quando necessario. Quando è necessario usarlo, è consigliabile sfalsare leggermente le coordinate di trama dalle posizioni dei limiti per evitare gli artefatti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtraggio trama](texture-filtering.md)
</dt> </dl>

 

 
