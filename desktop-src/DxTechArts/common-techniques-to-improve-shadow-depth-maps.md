---
title: Tecniche comuni per migliorare le mappe di profondità delle ombreggiature
description: Questo articolo tecnico offre una panoramica di alcuni algoritmi comuni della mappa di profondità delle ombreggiatura e degli artefatti comuni e illustra diverse tecniche, che vanno dalle difficoltà di base a intermedie, che possono essere usate per aumentare la qualità delle mappe shadow standard.
ms.assetid: bf994838-a261-0379-9301-eb9b250d216c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafff1b537830ae0ee681ed32932cca2b6274a4d9da3e0471ef498e0bef2d483
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102471"
---
# <a name="common-techniques-to-improve-shadow-depth-maps"></a>Tecniche comuni per migliorare le mappe di profondità delle ombreggiature

Le mappe delle ombreggiature, introdotte per la prima volta nel 1978, sono una tecnica comune per aggiungere ombreggiature ai giochi. Tre decenni dopo, nonostante i progressi nell'hardware e nel software, gli artefatti di shadowing, ovvero i bordi con sing, l'aliasing prospettica e altri problemi di precisione, persistono.

Questo articolo tecnico offre una panoramica di alcuni algoritmi comuni della mappa di profondità delle ombreggiatura e degli artefatti comuni e illustra diverse tecniche, che vanno dalle difficoltà di base a intermedie, che possono essere usate per aumentare la qualità delle mappe shadow standard. L'aggiunta di mappe ombreggiatura di base a un titolo è in genere semplice, ma comprendere le sfumature degli artefatti ombreggiati può risultare difficile. Questo articolo tecnico è stato scritto per lo sviluppatore di grafica intermedio che ha implementato le ombreggiature, ma non comprende completamente il motivo per cui vengono visualizzati elementi specifici e non sa come aggirarli.

La selezione delle tecniche corrette per mitigare elementi specifici non è un'attività semplice. Quando si affrontano i difetti della mappa delle ombreggiatura, la differenza di qualità può essere notevole (Figura 1). L'implementazione corretta di queste tecniche migliora drasticamente le ombreggiature standard. Le tecniche illustrate in questo articolo sono implementate nell'esempio CascadedShadowMaps11 in DirectX SDK.

**Figura 1. Ombreggiature con artefatti gravi (a sinistra) e ombreggiature dopo l'implementazione delle tecniche descritte in questo articolo (a destra)**

![ombreggiature con elementi gravi (a sinistra) e ombreggiature dopo l'implementazione delle tecniche descritte in questo articolo (a destra)](images/shadows-before-and-after.jpg)

## <a name="shadow-depth-maps-review"></a>Revisione della profondità Mappe ombreggiatura

L'algoritmo di mapping della profondità dell'ombreggiatura è un algoritmo a due passi. Il primo passaggio genera una mappa di profondità nello spazio chiaro. Nel secondo passaggio questa mappa viene usata per confrontare la profondità di ogni pixel nello spazio chiaro con la profondità corrispondente nella mappa di profondità dello spazio chiaro.

**Figura 2. Parti chiave di una scena ombreggiata**

![parti chiave di una scena ombreggiata](images/key-parts-of-shadow-scene.jpg)

### <a name="pass-1"></a>Passaggio 1

La scena è illustrata nella figura 2. Nel primo passaggio (Figura 3) viene eseguito il rendering della geometria in un buffer di profondità dal punto di vista della luce. In particolare, il vertex shader trasforma la geometria in uno spazio di visualizzazione chiaro.

Il risultato finale di questo primo passaggio è un buffer di profondità contenente le informazioni sulla profondità della scena dal punto di vista della luce. Ora può essere usato nel passaggio 2 per determinare quali pixel sono occlusi dalla luce.

**Figura 3. Primo passaggio del mapping delle ombreggiatura di base**

![primo passaggio del mapping delle ombreggiatura di base](images/first-pass-of-basic-hadow-mapping.png)

### <a name="pass-2"></a>Passaggio 2

Nel secondo passaggio (Figura 4) il vertex shader trasforma ogni vertice due volte. Ogni vertice viene trasformato nello spazio di visualizzazione della fotocamera e passato al pixel shader come posizione. Ogni vertice viene trasformato anche dalla matrice view-projection-texture della luce e passato al pixel shader come coordinata della trama. La matrice di visualizzazione-proiezione-trama è la stessa matrice usata per eseguire il rendering della scena nel passaggio 1 con una trasformazione aggiuntiva. Si tratta di una trasformazione che ridimensiona e trasla i punti dallo spazio di visualizzazione (da -1 a 1 in X e Y) allo spazio della trama (da 0 a 1 in X e da 1 a 0 in Y).

Il pixel shader riceve la posizione interpolata e le coordinate della trama interpolata. Tutto il necessario per eseguire il test di profondità si trova ora in questa coordinata di trama. Il test di profondità può ora essere eseguito indicizzando il buffer di profondità dal primo passaggio con le coordinate di trama X e Y e confrontando il valore di profondità risultante con la coordinata della trama Z.

**Figura 4. Secondo passaggio del mapping delle ombreggiatura di base**

![secondo passaggio del mapping delle ombreggiatura di base](images/second-pass-of-basic-shadow-mapping.png)

## <a name="shadow-map-artifacts"></a>Shadow Map Artifacts

L'algoritmo di mapping della profondità dell'ombreggiatura è l'algoritmo di shadowing in tempo reale più diffuso, ma produce comunque diversi artefatti che richiedono la mitigazione. I tipi di artefatti che possono verificarsi sono riepilogati di seguito.

### <a name="perspective-aliasing"></a>Alias prospettiva

L'aliasing della prospettiva, un artefatto comune, è illustrato nella figura 5. Si verifica quando il mapping dei pixel nello spazio di visualizzazione ai texel nella mappa ombreggiatura non è un rapporto uno-a-uno. Ciò è dovuto al fatto che i pixel vicini al piano vicino sono più vicini e richiedono una risoluzione della mappa ombreggiatura più elevata.

La figura 6 mostra una mappa ombreggiatura e un frustum di visualizzazione. Vicino all'occhio, i pixel sono più vicini e molti pixel sono mappati agli stessi texel ombreggiati. I pixel del piano lontano vengono distribuiti, riducendo così l'aliasing prospettica.

**Figura 5. Alias con prospettiva elevata (a sinistra) e alias con prospettiva bassa (a destra)**

![aliasing con prospettiva elevata (a sinistra) e alias con prospettiva bassa (a destra)](images/high-perspective-aliasing-vs-low-perspective-aliasing.jpg)

Per l'immagine a sinistra, l'aliasing della prospettiva è superiore; troppi pixel dello spazio oculare vengono mappati agli stessi texel della mappa delle ombreggiatura. Nell'immagine a destra l'aliasing della prospettiva è basso perché esiste un mapping 1:1 tra i pixel dello spazio oculare e i texel della mappa delle ombreggiatura.

**Figura 6. Visualizzare il frustum con la mappa ombreggiatura**

![view frustum with shadow map](images/view-frustum-with-shadow-map.jpg)

I pixel chiari nel piano lontano rappresentano alias con prospettiva bassa e i pixel scuri nel piano vicino rappresentano alias con prospettiva elevata.

Anche la risoluzione della mappa delle ombreggiatura può essere troppo elevata. Sebbene una risoluzione più elevata sia meno evidente, può tuttavia comportare oggetti di piccole dimensioni, ad esempio cavi telefonici, che non proiettano ombreggiature. Inoltre, la presenza di una risoluzione troppo elevata può causare gravi problemi di prestazioni a causa dei modelli di accesso alla trama.

Le mappe di ombreggiatura prospettica (PSM) e le mappe di ombreggiatura prospettica dello spazio chiaro tentano di risolvere gli alias di prospettiva inclinando la matrice di proiezione della luce per posizionare più texel vicino all'occhio dove sono necessari. Sfortunatamente, nessuna delle due tecniche è in grado di risolvere l'aliasing della prospettiva. La parametrizzazione della trasformazione necessaria per mappare i pixel dello spazio oculare ai texel nella mappa ombreggiatura non può essere associata a un'a inclinazione lineare. È necessaria una parametrizzazione logaritmica. I psm mettono troppi dettagli vicino all'occhio, causando ombreggiature di scarsa qualità o addirittura scomparendo. Gli LSPSM fanno un lavoro migliore per trovare una soluzione intermedia tra l'aumento della risoluzione vicino all'occhio e l'uscita di dettagli sufficienti per gli oggetti lontano. Entrambe le tecniche degenere in ombreggiature ortografiche in alcune configurazioni di scena. Questa degenerezione può essere contrastata tramite il rendering di una mappa ombreggiatura separata per ogni viso del frustum di visualizzazione, anche se questo è costoso. Anche le mappe di ombreggiatura prospettica logaritmica (LogPSM) eseguono il rendering di una mappa separata per ogni viso del frustum di visualizzazione. Questa tecnica usa la rasterizzazione non lineare per posizionare più texel vicino all'occhio. L'hardware di classe D3D10 e D3D11 non supporta la rasterizzazione non lineare. Per altre informazioni su queste tecniche e algoritmi, vedere la sezione Riferimenti.

Le mappe di ombreggiatura a cascata sono la tecnica più diffusa per la gestione dell'aliasing prospettica. Anche se i CPM possono essere combinati con PSM e LSPSM, non è necessario. L'uso di CMS per correggere gli errori di aliasing prospettica è disponibile nell'articolo complementare [Cascaded Shadow Mappe](/windows/desktop/DxTechArts/cascaded-shadow-maps).

### <a name="projective-aliasing"></a>Aliasing proiettativo

L'aliasing proiettato è più difficile da visualizzare rispetto all'aliasing prospettica. Le ombreggiature distense evidenziate nella figura 7 illustrano gli errori di aliasing proiettati. L'aliasing proiettato si verifica quando il mapping tra texel nello spazio della fotocamera e texel nello spazio chiaro non è un rapporto uno-a-uno; ciò è dovuto all'orientamento della geometria rispetto alla fotocamera leggera. L'aliasing proiettato si verifica quando il piano tangente della geometria diventa parallelo ai raggi di luce.

**Figura 7. Alias ad alto rischio e alias a basso progetto**

![alias ad alto rischio e alias a basso progetto](images/high-projective-aliasing-vs-low%20projective-aliasing.jpg)

Le tecniche usate per ridurre gli errori di aliasing prospettica attenuano anche l'aliasing proiettativo. L'aliasing proiettato si verifica quando la normale della superficie è ortogonale alla luce; Queste superfici devono ricevere meno luce in base a equazioni di illuminazione diffuse.

### <a name="shadow-acne-and-erroneous-self-shadowing"></a>Shadow Shadow Erroneous Self-Shadowing

Shadow shadow shadow (Figura 8), termine sinonimo di ombreggiatura errata, si verifica quando la mappa delle ombreggiatura quantizza la profondità su un intero texel. Quando lo shader confronta una profondità effettiva con questo valore, è probabile che sia ombreggiato automaticamente quanto non ombreggiato.

Un altro motivo per l'ombreggiatura è che il texel nello spazio chiaro è così vicino alla profondità del texel corrispondente nella mappa di profondità che gli errori di precisione causano un errore del test di profondità. Uno dei motivi di questa differenza di precisione è che la mappa di profondità è stata calcolata dall'hardware di rasterizzazione a funzione fissa, mentre la profondità confrontata è stata calcolata dallo shader. L'aliasing proiettato può anche causare shadow shadow shadow.

**Figura 8. Artefatto shadow shadow**

![shadow shadow artifact](images/shadow-acne-artifact.jpg)

Come illustrato nell'immagine a sinistra, alcuni pixel non hanno superato il test di profondità e hanno creato artefatti speckled e modelli moiré. Per ridurre l'ombreggiatura errata, i limiti sul piano vicino e sul piano lontano per il frustum di visualizzazione dello spazio chiaro devono essere calcolati nel modo più stretto possibile. La distorsione della profondità basata sulla scala del inclinazione e altri tipi di distorsione sono altre soluzioni usate per attenuare l'ombreggiatura.

### <a name="peter-panning"></a>Peter Panning

Il termine *Peter Panning* deriva il nome da un carattere libro per bambini la cui ombreggiatura si è scollegata e chi può pilotare. Questo artefatto fa in modo che gli oggetti con ombreggiature mancanti vengano scollegati da e per fluttuare sopra la superficie (Figura 9).

**Figura 9. Artefatto Peter Panning**

![peter panning artifact](images/peter-panning-artifact.jpg)

Nell'immagine a sinistra l'ombreggiatura viene scollegata dall'oggetto , creando un effetto mobile.

Una tecnica per la rimozione della superficie è aggiungere un valore alla posizione dei pixel nello spazio chiaro; questa operazione è denominata aggiunta di un offset di profondità. Peter Panning risulta quando l'offset di profondità usato è troppo grande. In questo caso l'offset della profondità fa sì che il test di profondità passi erroneamente. Come per l'ombreggiatura, Peter Panning è peggiorato quando la precisione nel buffer di profondità non è sufficiente. Il calcolo di piani vicini e lontani consente anche di evitare Peter Panning.

## <a name="techniques-to-improve-shadow-maps"></a>Tecniche per migliorare l'Mappe

L'aggiunta di ombreggiature a un titolo è un processo. Il primo passaggio consiste nel far funzionare le mappe shadow di base. Il secondo è garantire che tutti i calcoli di base siano eserciti in modo ottimale: frusta fit as tightly as tight as possible, near/far planes fit tightly, slope-scaled bias is used e così via. Dopo aver abilitato le ombreggiature di base e avere un aspetto il più possibile valido, lo sviluppatore ha un'idea migliore degli algoritmi necessari per ottenere le ombreggiature a una fedeltà sufficiente. In questa sezione vengono forniti suggerimenti di base che potrebbero essere necessari per ottenere mappe shadow di base che esaminano al meglio.

### <a name="slope-scale-depth-bias"></a>Slope-Scale distorsione della profondità

Come accennato in precedenza, l'ombreggiatura self-shadowing può causare l'shadowing. L'aggiunta di una distorsione troppo grande può comportare l'aggiunta di Peter Panning. Inoltre, i poligoni con pendenza ripida (rispetto alla luce) hanno un aliasing più proiettativo rispetto ai poligoni con pendenza superficiale (rispetto alla luce). Per questo scopo, ogni valore della mappa di profondità potrebbe richiedere un offset diverso a seconda dell'inclinazione del poligono rispetto alla luce.

L'hardware Direct3D 10 ha la possibilità di distorsione di un poligono in base alla pendenza rispetto alla direzione di visualizzazione. Ciò ha l'effetto di applicare una distorsione di grandi dimensioni a un poligono che viene visualizzato nella direzione della luce, ma non applica alcuna distorsione a un poligono rivolto direttamente verso la luce. La figura 10 illustra come due pixel adiacenti possono alternarsi tra ombreggiatura e ombreggiatura durante il test sulla stessa pendenza imparziale.

**Figura 10. Distorsione della profondità in scala di pendenza rispetto alla profondità imparziale**

![distorsione della profondità in scala dell'inclinazione rispetto alla profondità imparziale](images/slope-scaled-depth-bias-compared-to-unbiased-depth.png)

### <a name="calculating-a-tight-projection"></a>Calcolo di una proiezione stretta

Adattando strettamente la proiezione della luce al frusto della vista, aumenta la copertura della mappa delle ombreggiatura. La figura 11 illustra che l'uso di una proiezione arbitraria o l'adattamento della proiezione ai limiti della scena comporta un aliasing prospettico più elevato.

**Figura 11. Frustum di ombreggiatura arbitraria e frustum di ombreggiatura adattati alla scena**

![frustum di ombreggiatura arbitraria e frustum di ombreggiatura adattati alla scena](images/arbitrary-shadow-frustum-and-shadow-frustum-fit-to-scene.jpg)

La vista è dal punto di vista della luce. Il trapezio rappresenta il frusto della fotocamera di visualizzazione. La griglia disegnata sull'immagine rappresenta la mappa ombreggiatura. L'immagine a destra mostra che la stessa mappa ombreggiatura con risoluzione crea una maggiore copertura texel quando è più adatta alla scena.

La figura 12 illustra i frustum adatti. Per calcolare la proiezione, gli otto punti che costituiscono il frustum della vista vengono trasformati in spazio chiaro. Vengono quindi trovati i valori minimo e massimo in X e Y. Questi valori costituiscono i limiti per una proiezione ortografica.

**Figura 12. Proiezione ombreggiatura adatta per visualizzare il frusto**

![proiezione ombreggiatura adatta per visualizzare frustum](images/shadow-projection-fit-to-view-frustum.jpg)

È anche possibile ritagliare il frusto alla scena AABB per ottenere un limite più stretto. Questa operazione non è consigliata in tutti i casi perché può cambiare le dimensioni della proiezione della fotocamera leggera da fotogramma a fotogramma. Molte tecniche, ad esempio quelle descritte nella sezione Spostamento della luce Texel-Sized incrementi, offrono risultati migliori quando le dimensioni della proiezione della luce rimangono costanti in ogni fotogramma.

### <a name="calculating-the-near-plane-and-far-plane"></a>Calcolo del piano vicino e del piano lontano

Il piano vicino e il piano lontano sono gli ultimi elementi necessari per calcolare la matrice di proiezione. Più vicini sono i piani, più precisi sono i valori nel buffer di profondità.

Il buffer di profondità può essere a 16 bit, a 24 o a 32 bit, con valori compresi tra 0 e 1. In genere, i buffer di profondità sono a punto fisso, con i valori vicini al piano vicino raggruppati più strettamente rispetto ai valori vicini al piano lontano. Il grado di precisione disponibile per il buffer di profondità è determinato dal rapporto tra il piano vicino e il piano lontano. L'uso del piano più stretto possibile vicino/lontano potrebbe consentire l'uso di un buffer di profondità a 16 bit. Un buffer di profondità a 16 bit potrebbe ridurre l'uso della memoria aumentando la velocità di elaborazione.

### <a name="aabb-based-near-plane-and-far-plane"></a>AABB-Based vicino al piano e al piano lontano

Un modo semplice e ingenuo per calcolare il piano vicino e il piano lontano è trasformare il volume di delimitazione della scena in spazio chiaro. Il valore più piccolo della coordinata Z è il piano vicino e il valore più grande della coordinata Z è il piano lontano. Per molte configurazioni della scena e della luce, questo approccio è sufficiente. Lo scenario peggiore, tuttavia, può comportare una perdita significativa di precisione nel buffer di profondità. La figura 13 illustra uno scenario di questo tipo. Qui l'intervallo del piano vicino al piano lontano è quattro volte più grande del necessario.

La visualizzazione frustum nella figura 13 è stata scelta appositamente come piccola. Un frusto di visualizzazione di piccole dimensioni viene visualizzato in una scena molto grande costituita da colonne che si estendono dalla fotocamera. L'uso della scena AABB per i piani vicino e lontano non è ottimale. L'algoritmo CSM descritto [nell'articolo](/windows/desktop/DxTechArts/cascaded-shadow-maps) tecnico Cascaded Shadow Mappe deve calcolare piani vicini e lontani per frustum molto piccoli.

**Figura 13. Piani vicini e lontani basati sulla scena AABB**

![piani vicini e lontani basati sulla scena aabb](images/near-far-%20planes-based-on-scene-aabb.jpg)

### <a name="frustum-based-near-plane-and-far-plane"></a>Frustum-Based vicino al piano e al piano lontano

Un'altra tecnica per calcolare i piani vicino e lontano consiste nel trasformare il frustum in spazio chiaro e usare i valori minimi e massimi in Z rispettivamente come piani vicini e lontani. La figura 14 illustra i due problemi relativi a questo approccio. In primo luogo, il calcolo è troppo conservativo, come illustrato quando il frustum si estende oltre la geometria della scena. In secondo momento, il piano vicino potrebbe essere troppo stretto, causando il ritaglio delle ombreggiatura.

**Figura 14. Piani vicini e lontani basati esclusivamente sul frustum di visualizzazione**

![piani vicini e lontani basati esclusivamente sul frustum di visualizzazione](images/near-far-planes-based-solely-on-view-frustum.jpg)

### <a name="light-frustum-intersected-with-scene-to-calculate-near-and-far-planes"></a>Frusto chiaro intersecato con la scena per calcolare i piani vicino e lontano

Il modo corretto per calcolare i piani vicino e lontano è illustrato nella figura 15. Quattro dei piani del frusto di luce ortografica sono stati calcolati usando il minimo e il massimo delle coordinate X e Y del frusto di visualizzazione nello spazio luce. Gli ultimi due piani del frustum della vista ortogonale sono i piani vicino e lontano. Per trovare questi piani, i limiti della scena vengono ritagliati rispetto ai quattro piani di frusto chiaro noti. I valori Z più piccoli e maggiori del limite appena ritagliato rappresentano rispettivamente il piano vicino e il piano lontano.

Il codice che esegue questa operazione si trova nell'esempio CascadedShadowMaps11. Gli otto punti che costituiscono l'AABB del mondo vengono trasformati in spazio chiaro. La trasformazione dei punti in spazio chiaro semplifica i test di ritaglio. I quattro piani noti del frusto chiaro possono ora essere rappresentati come linee. Il volume di delimitazione delle scene nello spazio chiaro può essere rappresentato come sei quadrilateri. Questi 6 quadrilateri possono quindi essere trasformati in 12 triangoli per il ritaglio basato su triangoli. I triangoli vengono ritagliati rispetto ai piani noti del frustum di visualizzazione (si tratta di linee orizzontali e verticali in X e Y nello spazio chiaro). Quando si trova un punto di intersezione in X e Y, il triangolo 3D viene ritagliato in quel punto. I valori Z minimo e massimo di tutti i triangoli ritagliati sono il piano vicino e il piano lontano. L'esempio CascadedShadowMaps11 illustra come eseguire questo ritaglio nella **funzione ComputeNearAndFar.**

Esistono altre due tecniche che possono essere usate per calcolare i piani più vicini e lontani possibili. Queste tecniche non sono illustrate nell'esempio CascadedShadowMaps.

-   I piani più vicini e lontani possono essere calcolati intersecando una gerarchia di una scena o di singoli oggetti in una scena rispetto al frusto chiaro. Questo sarebbe più complesso dal punto di vista del calcolo. Anche se non è illustrata nell'esempio CascadedShadowMaps11, questa potrebbe essere una tecnica valida per alcuni riquadri.
-   Il piano lontano può essere calcolato prendendo il minimo di:

    -   Profondità massima del frusto di visualizzazione nello spazio chiaro.
    -   Profondità massima dell'intersezione tra il frustum di visualizzazione e la scena AABB.

Questo approccio può essere problematico se usato con mappe ombreggiate a catena in cui è possibile indicizzare all'esterno di un frustum di vista. In questo caso, la mappa ombreggiatura potrebbe non essere presente nella geometria.

**Figura 15. Piani vicini e lontani basati sull'intersezione dei quattro piani calcolati del frusto chiaro e della geometria di delimitazione della scena**

![piani vicini e lontani basati sull'intersezione dei quattro piani calcolati del frusto chiaro e della geometria di delimitazione della scena](images/near-far-plane-based-on-intersection-of-four.jpg)

### <a name="moving-the-light-in-texel-sized-increments"></a>Spostamento della luce in Texel-Sized incrementi

Un artefatto comune nelle mappe di ombreggiatura è l'effetto del bordo shimmering. Quando la fotocamera si sposta, i pixel lungo i bordi delle ombreggiature si illuminano e si scurino. Questo non può essere visualizzato nelle immagini fisse, ma è molto evidente e distratto in tempo reale. La figura 16 evidenzia questo problema e la figura 17 illustra l'aspetto dei bordi delle ombreggiatura.

L'errore del bordo shimmering si verifica perché la matrice di proiezione della luce viene ricalcolata ogni volta che la fotocamera si sposta. Ciò crea piccole differenze nelle mappe ombreggiate generate. Tutti i fattori seguenti possono influenzare la matrice creata per delimitare la scena.

-   Dimensioni del frustum di visualizzazione
-   Orientamento del frustum di visualizzazione
-   Posizione della luce
-   Posizione della fotocamera

Ogni volta che questa matrice cambia, i bordi delle ombreggiature possono cambiare.

**Figura 16. Bordi ombreggiati sondanti**

![Ombreggiatura singing dei bordi](images/shimmering-shadow-edges.jpg)

I pixel lungo il bordo dell'ombreggiatura entrare e uscire dall'ombreggiatura quando la fotocamera si sposta da sinistra a destra.

**Figura 17. Ombreggiature senza bordi srsiglioati**

![ombreggiature senza bordi srsigliosi](images/shadows-without-shimmering-edges.jpg)

I bordi dell'ombreggiatura rimangono costanti quando la fotocamera si sposta da sinistra a destra.

Per le luci direzionali, la soluzione a questo problema consiste nell'arrotondare il valore minimo/massimo in X e Y (che costituiscono i limiti di proiezione ortografica) agli incrementi delle dimensioni in pixel. Questa operazione può essere eseguita con un'operazione di divisione, un'operazione floor e una moltiplicazione.


```C++
        vLightCameraOrthographicMin /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMin = XMVectorFloor( vLightCameraOrthographicMin );
        vLightCameraOrthographicMin *= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax = XMVectorFloor( vLightCameraOrthographicMax );
        vLightCameraOrthographicMax *= vWorldUnitsPerTexel;
```



Il valore vWorldUnitsPerTexel viene calcolato prendendo un limite del frustum di visualizzazione e dividendo per le dimensioni del buffer.


```C++
        FLOAT fWorldUnitsPerTexel = fCascadeBound /
        (float)m_CopyOfCascadeConfig.m_iBufferSize;
        vWorldUnitsPerTexel = XMVectorSet( fWorldUnitsPerTexel, fWorldUnitsPerTexel,                            0.0f, 0.0f );
```



Il delimitazione delle dimensioni massime del frustum di visualizzazione determina un adattamento più libero per la proiezione ortografica.

È importante notare che la trama ha una larghezza e un'altezza maggiori di 1 pixel quando si usa questa tecnica. In questo modo le coordinate dell'ombreggiatura non vengono indicizzate all'esterno della mappa ombreggiatura.

### <a name="back-face-and-front-face"></a>Back Face e Front Face

Il rendering delle mappe ombreggiate deve essere eseguito con l'culling standard dei back-face, un processo che ignora la rasterizzazione degli oggetti che il visualizzatore non può visualizzare e velocizza il rendering della scena. Un'altra opzione comune è eseguire il rendering delle mappe ombreggiate con il culling front-face abilitato, il che significa che gli oggetti rivolti verso il visualizzatore vengono eliminati. L'argomento per questo è che è utile con l'ombreggiatura autonoma, perché la geometria che rappresenta la parte posteriore degli oggetti è leggermente offset. Questa idea ha due problemi.

-   Qualsiasi oggetto con geometria front-face o back-face non corretta causa artefatti nella mappa ombreggiatura. Tuttavia, se la geometria frontale o posteriore non è corretta, possono verificarsi altri problemi, pertanto può essere sicuro presupporre che la geometria front-face e back-face venga eseguita correttamente. Potrebbe non essere pratico creare visi per la geometria basata su sprite, ad esempio la foglia.
-   Peter Panning e i vuoti di ombreggiatura vicino alla base di oggetti come le pareti hanno maggiori probabilità di verificarsi perché la disparità di profondità dell'ombreggiatura è troppo piccola.

### <a name="shadow-mapfriendly-geometry"></a>Mappa delle ombreggiatura- Geometria descrittiva

La creazione di una geometria che funziona bene nelle mappe ombreggiate offre maggiore flessibilità quando si contrasta con artefatti come Peter Panning e shadow shadow shadow.

I bordi rigidi sono problematici per l'ombreggiatura self-shadowing. La disparità di profondità vicino alla punta del bordo è molto piccola. Anche un offset ridotto può causare la perdita delle ombreggiature degli oggetti (figura 18).

**Figura 18. I bordi acuti causano artefatti che derivano dalla disparità a bassa profondità con offset**

![I bordi acuti causano artefatti che derivano da disparità a bassa profondità con offset](images/sharp-edges-cause%20artifacts.jpg)

Gli oggetti ristretti, ad esempio le pareti, devono avere le backs anche se non sono mai visibili. In questo modo si aumenterà la disparità di profondità.

È anche importante assicurarsi che la direzione della geometria sia corretta. ciò significa che l'esterno di un oggetto deve essere di nuovo rivolto verso l'esterno e l'interno di un oggetto deve essere rivolto verso l'esterno. Questo è importante per il rendering con il culling dei visi posteriore abilitato, nonché per contrastare gli effetti della distorsione della profondità.

## <a name="summary"></a>Riepilogo

Le tecniche descritte in questo articolo possono essere usate per aumentare la qualità delle mappe ombreggiate standard. Il passaggio successivo consiste nell'esaminare le tecniche che possono funzionare bene con le mappe ombreggiate standard. I CMM sono consigliati come tecnica superiore per contrastare l'aliasing della prospettiva. Per attenuare i bordi dell'ombreggiatura è possibile usare mappe di ombreggiatura con filtro o varianza più vicine. Per altre [informazioni, vedere](/windows/desktop/DxTechArts/cascaded-shadow-maps) l'articolo tecnico Mappe shadow a cascata.

Donnelly, W. e Lauritzen, A. [Variance Shadow Mappe](https://portal.acm.org/citation.cfm?doid=1111411.1111440). Symposium on Interactive 3D Graphics, Proceedings of the 2006 Symposium on Interactive 3D Graphics and Games (Simposio sulla grafica e i giochi 3D interattivi). 2006, pp. 161-165.

Ematerial, Woflgang F. Sezione 4. Shadow Mappe. ShaderX5, *Advanced Rendering Techniques*, Wolfgang F. E shader, Ed. Charles River Media, Boston, Portos. 2006. pp. 197-206.

Stamminger, Antonio e Drettakis, Antonio. [Ombreggiatura prospettiva Mappe](https://portal.acm.org/citation.cfm?id=566616). International Conference on Computer Graphics and Interactive Techniques, *Proceedings of the 29th Annual Conference on Computer Graphics and Interactive Techniques*. 2002, pp 557-562.

Wittico, M., Scherzer, D. e Purgathofer, W. [Light Space Perspective Shadow Mappe](https://www.cg.tuwien.ac.at/research/vr/lispsm/shadows_egsr2004_revised.pdf). Eurographics Symposium on Rendering (Simposio eurografico sul rendering). 2004. Rivisto il 10 giugno 2005. [Technische Cabaret Wien](https://www.cg.tuwien.ac.at/research/vr/lispsm/).

 

 
