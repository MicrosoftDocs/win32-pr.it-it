---
title: Tecniche comuni per migliorare le mappe di profondità delle ombreggiature
description: In questo articolo tecnico viene fornita una panoramica di alcuni algoritmi comuni di mapping di ombreggiatura e di artefatti comuni e vengono illustrate diverse tecniche, che possono essere usate per aumentare la qualità delle mappe Shadow standard.
ms.assetid: bf994838-a261-0379-9301-eb9b250d216c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b25507d7f6b8608d4dacf5fab620bc8a3294c7
ms.sourcegitcommit: 218b1ff779402c3ebe1786679e1aa80a5c0d6c95
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730711"
---
# <a name="common-techniques-to-improve-shadow-depth-maps"></a>Tecniche comuni per migliorare le mappe di profondità delle ombreggiature

Le mappe Shadow, introdotte per la prima volta nel 1978, rappresentano una tecnica comune per l'aggiunta di ombre ai giochi. Tre decenni dopo, nonostante gli anticipi sull'hardware e sul software, gli artefatti ombreggiatura, ovvero i bordi luccicanti, l'aliasing prospettico e altri problemi di precisione, vengono mantenuti.

In questo articolo tecnico viene fornita una panoramica di alcuni algoritmi comuni di mapping di ombreggiatura e di artefatti comuni e vengono illustrate diverse tecniche, che possono essere usate per aumentare la qualità delle mappe Shadow standard. L'aggiunta di mappe shadow di base a un titolo è in genere semplice, ma la comprensione delle sfumature degli artefatti shadow può essere complessa. Questo articolo tecnico è stato scritto per lo sviluppatore di grafica intermedio che ha implementato le ombre, ma non comprende completamente il motivo per cui vengono visualizzati elementi specifici e non è certo come risolverli.

La selezione delle tecniche corrette per attenuare elementi specifici non è semplice. Quando vengono risolti gli svantaggi della mappa Shadow, la differenza nella qualità può essere impressionante (Figura 1). Una corretta implementazione di queste tecniche migliora drasticamente le ombre standard. Le tecniche descritte in questo articolo sono implementate nell'esempio CascadedShadowMaps11 in DirectX SDK.

**Figura 1. Ombre con elementi gravi (a sinistra) e ombre dopo l'implementazione delle tecniche descritte in questo articolo (Right)**

![ombre con elementi gravi (a sinistra) e ombre dopo l'implementazione delle tecniche descritte in questo articolo (Right)](images/shadows-before-and-after.jpg)

## <a name="shadow-depth-maps-review"></a>Revisione mappe profondità ombreggiatura

L'algoritmo di mappa profondità ombreggiatura è un algoritmo a due passaggi. Il primo passaggio genera una mappa di profondità nello spazio chiaro. Nel secondo passaggio, questa mappa viene utilizzata per confrontare la profondità di ogni pixel nello spazio chiaro rispetto alla profondità corrispondente nella mappa della profondità dello spazio chiaro.

**Figura 2. Parti principali di una scena Shadow**

![parti principali di una scena Shadow](images/key-parts-of-shadow-scene.jpg)

### <a name="pass-1"></a>Passaggio 1

La scena è illustrata nella figura 2. Nel primo passaggio (Figura 3), la geometria viene sottoposta a rendering in un buffer di profondità dal punto di vista della luce. In particolare, il vertex shader trasforma la geometria nello spazio di visualizzazione chiaro.

Il risultato finale di questo primo passaggio è un buffer di profondità contenente le informazioni di profondità della scena dal punto di vista della luce. Questo ora può essere usato nel passaggio 2 per determinare quali pixel sono bloccati dalla luce.

**Figura 3. Primo passaggio del mapping ombreggiato di base**

![primo passaggio del mapping ombreggiato di base](images/first-pass-of-basic-hadow-mapping.png)

### <a name="pass-2"></a>Passaggio 2

Nel secondo passaggio (Figura 4), il vertex shader trasforma due volte ogni vertice. Ogni vertice viene trasformato nello spazio di visualizzazione della fotocamera e passato al pixel shader come posizione. Ogni vertice viene anche trasformato dalla matrice di visualizzazione-proiezione-trama della luce e passato al pixel shader come coordinata di trama. La matrice View-Projection-texture è la stessa matrice usata per eseguire il rendering della scena nel passaggio 1 con una trasformazione aggiuntiva. Si tratta di una trasformazione che consente di ridimensionare e traslare i punti dallo spazio di visualizzazione (da-1 a 1 in X e Y) allo spazio della trama (da 0 a 1 in X e da 1 a 0 in Y).

Il pixel shader riceve la posizione interpolata e le coordinate della trama interpolata. Tutti gli elementi necessari per eseguire il test di profondità sono ora in questa coordinata di trama. È ora possibile eseguire il test di profondità indicizzando il buffer di profondità dal primo passaggio con le coordinate della trama X e Y e confrontando il valore di profondità risultante con la coordinata Z-texture.

**Figura 4. Secondo passaggio del mapping ombreggiato di base**

![secondo passaggio del mapping ombreggiato di base](images/second-pass-of-basic-shadow-mapping.png)

## <a name="shadow-map-artifacts"></a>Artefatti mappa Shadow

L'algoritmo di mappa profondità ombreggiatura è l'algoritmo di shadowing in tempo reale usato più di frequente, ma produce ancora diversi artefatti che richiedono la mitigazione. I tipi di artefatti che possono verificarsi sono riepilogati successivamente.

### <a name="perspective-aliasing"></a>Aliasing prospettiva

L'aliasing della prospettiva, un artefatto comune, è illustrato nella figura 5. Si verifica quando il mapping dei pixel nello spazio di visualizzazione ai Texel nella mappa shadow non è un rapporto uno-a-uno. Il motivo è che i pixel vicini al piano vicino sono più vicini e richiedono una risoluzione più elevata della mappa Shadow.

Nella figura 6 è illustrata una mappa Shadow e una vista tronco. In prossimità dell'occhio, i pixel sono più vicini e molti pixel sono mappati agli stessi Texel di ombreggiatura. I pixel del piano lontano sono distribuiti, riducendo così l'aliasing della prospettiva.

**Figura 5. Aliasing ad alta prospettiva (a sinistra) rispetto all'aliasing a bassa prospettiva (Right)**

![aliasing ad alta prospettiva (a sinistra) rispetto all'aliasing a bassa prospettiva (Right)](images/high-perspective-aliasing-vs-low-perspective-aliasing.jpg)

Per l'immagine a sinistra, l'aliasing della prospettiva è più elevato; un numero eccessivo di pixel dello spazio oculare è mappato agli stessi Texel della mappa Shadow. Nell'immagine a destra, l'aliasing della prospettiva è basso perché è presente un mapping 1:1 tra i pixel di spazio occhio e i Texel Mappa Shadow.

**Figura 6. Visualizza tronco con mappa Shadow**

![Visualizza tronco con mappa Shadow](images/view-frustum-with-shadow-map.jpg)

I pixel leggeri nel piano lontano rappresentano l'aliasing a bassa prospettiva e i pixel scuri nel piano vicino rappresentano gli alias ad alta prospettiva.

Anche la risoluzione della mappa shadow può essere troppo elevata. Anche se una risoluzione più elevata è meno evidente, può tuttavia comportare piccoli oggetti, come i cavi telefonici, e non il cast delle ombreggiature. Inoltre, la presenza di una risoluzione troppo elevata può causare gravi problemi di prestazioni a causa dei modelli di accesso alla trama.

Le mappe Shadow (PSMs) e le mappe Shadow della prospettiva dello spazio (LSPSMs) presentano un tentativo di indirizzare l'aliasing prospettico inclinando la matrice di proiezione della luce per collocare più Texel vicino all'occhio dove sono necessari. Sfortunatamente, nessuna tecnica è in grado di risolvere l'aliasing della prospettiva. La parametrizzazione della trasformazione necessaria per eseguire il mapping tra i pixel dello spazio degli occhi e i Texel nella mappa shadow non può essere associata da un'asimmetria lineare. È necessaria una parametrizzazione logaritmica. PSMs ha messo a punto una quantità eccessiva di dettagli, causando ombre distanti per essere di bassa qualità o addirittura scomparire. LSPSMs offrono un lavoro migliore per trovare un terreno intermedio tra l'aumento della risoluzione in prossimità dell'occhio e l'uscita di un numero sufficiente di dettagli per gli oggetti lontani. Entrambe le tecniche degenerano le ombreggiature ortogonali in alcune configurazioni di scena. Questa degenerazione può essere neutralizzata mediante il rendering di una mappa Shadow separata per ogni faccia della vista tronco, anche se si tratta di un'operazione costosa. Anche le mappe Shadow della prospettiva logaritmica (LogPSMs) eseguono il rendering di una mappa separata per faccia della vista tronco. Questa tecnica usa la rasterizzazione non lineare per collocare più Texel in prossimità dell'occhio. L'hardware della classe D3D10 e D3D11 non supporta la rasterizzazione non lineare. Per ulteriori informazioni su queste tecniche e sugli algoritmi, vedere la sezione riferimenti.

Le mappe Shadow a cascata (CSM) sono la tecnica più diffusa per la gestione degli alias delle prospettive. Sebbene CSM possa essere combinato con PSMs e LSPSMs, non è necessario. L'uso di CSM per correggere gli errori di aliasing della prospettiva viene trattato nell'articolo complementare [mappe Shadow a cascata](/windows/desktop/DxTechArts/cascaded-shadow-maps).

### <a name="projective-aliasing"></a>Aliasing proiettivo

L'aliasing proiettivo è più difficile da mostrare rispetto all'alias della prospettiva. Le ombreggiature rivelate evidenziate nella figura 7 illustrano gli errori di aliasing proiettivi. L'aliasing proiettivo si verifica quando il mapping tra Texel nello spazio della fotocamera e i Texel nello spazio chiaro non è un rapporto uno-a-uno. Questo è dovuto all'orientamento della geometria rispetto alla fotocamera chiaro. L'aliasing proiettivo si verifica quando il piano tangente della geometria diventa parallelo ai raggi luminosi.

**Figura 7. Aliasing ad alta proiezione e con aliasing basso-proiettivo**

![aliasing ad alta proiezione e con aliasing basso-proiettivo](images/high-projective-aliasing-vs-low%20projective-aliasing.jpg)

Anche le tecniche usate per attenuare gli errori di aliasing delle prospettive attenuano l'aliasing proiettivo. L'aliasing proiettivo si verifica quando la superficie normale è ortogonale alla luce; Queste superfici dovrebbero ricevere una minore luminosità in base alle equazioni di illuminazione diffuse.

### <a name="shadow-acne-and-erroneous-self-shadowing"></a>Shadow acne e Self-Shadowing errata

Shadow acne (Figura 8), un termine sinonimo di shadowing automatico errato, si verifica quando la mappa Shadow Quantizza la profondità su un intero Texel. Quando lo shader confronta una profondità effettiva rispetto a questo valore, è probabile che venga ombreggiata in modo automatico perché deve essere ombreggiata.

Un altro motivo per l'acne ombra è che il Texel nello spazio chiaro è così vicino alla profondità del Texel corrispondente nella mappa di profondità. gli errori di precisione causano un errore errato del test di profondità. Uno dei motivi di questa differenza consiste nel fatto che la mappa Depth è stata calcolata dall'hardware di rasterizzazione a funzione fissa, mentre la profondità confrontata è stata calcolata dallo shader. L'aliasing proiettivo può anche causare Shadow acne.

**Figura 8. Artefatto Shadow acne**

![artefatto Shadow acne](images/shadow-acne-artifact.jpg)

Come illustrato nell'immagine a sinistra, alcuni pixel non hanno superato il test di profondità e hanno creato artefatti e modelli moiré. Per ridurre il ridimensionamento automatico errato, i limiti sul piano vicino e il piano lontano per la visualizzazione dello spazio chiaro tronco devono essere calcolati nel modo più rigoroso possibile. La distorsione della profondità basata sulla scala di inclinazione e altri tipi di distorsione sono altre soluzioni usate per mitigare l'acne Shadow.

### <a name="peter-panning"></a>Peter panning

Il termine *Peter panning* deriva il nome da un carattere del libro figlio la cui ombra è stata scollegata e che può volare. Questo artefatto fa sì che gli oggetti con ombreggiature mancanti risultino scollegati da e in float sopra l'area (Figura 9).

**Figura 9. Artefatto di Peter panning**

![artefatto di Peter panning](images/peter-panning-artifact.jpg)

Nell'immagine a sinistra, l'ombreggiatura viene scollegata dall'oggetto, creando un effetto a virgola mobile.

Una tecnica per la rimozione della superficie acne è l'aggiunta di un valore alla posizione dei pixel nello spazio chiaro; Questa operazione viene denominata aggiunta di un offset di profondità. Peter panning restituisce quando l'offset di profondità utilizzato è troppo grande. In questo caso, l'offset di profondità causa il passaggio errato del test di profondità. Come Shadow acne, Peter panning viene aggravato quando la precisione nel buffer di profondità non è sufficiente. Il calcolo di piani stretti vicini e di piani lontani consente anche di evitare la Panoramica di Peter.

## <a name="techniques-to-improve-shadow-maps"></a>Tecniche per migliorare le mappe Shadow

L'aggiunta di ombre a un titolo è un processo. Il primo passaggio consiste nel far funzionare le mappe shadow di base. Il secondo consiste nel garantire che tutti i calcoli di base vengano eseguiti in modo ottimale: frusta adatta al più possibile, i piani near/lontano si adattano strettamente, viene usata la distorsione con scalabilità verticale e così via. Una volta abilitate le ombreggiature di base e osservate quanto più possibile, lo sviluppatore ha un'idea più precisa degli algoritmi necessari per ottenere le ombre per una fedeltà sufficiente. In questa sezione vengono forniti suggerimenti di base che potrebbero essere necessari per ottenere le mappe shadow di base che esaminano meglio le proprie esigenze.

### <a name="slope-scale-depth-bias"></a>Distorsione profondità Slope-Scale

Come indicato in precedenza, l'ombreggiatura automatica può causare l'acne Shadow. L'aggiunta di una distorsione troppo lunga può comportare la Panoramica di Peter. Inoltre, i poligoni con pendii ridotti (relativi alla luce) soffrono più dell'aliasing proiettivo rispetto ai poligoni con pendii superficiali (in relazione alla luce). Per questo motivo, ogni valore della mappa di profondità potrebbe richiedere un offset diverso a seconda della pendenza del poligono rispetto alla luce.

L'hardware Direct3D 10 ha la possibilità di inclinare un poligono in base alla relativa pendenza rispetto alla direzione di visualizzazione. Questo ha l'effetto di applicare una polarizzazione di grandi dimensioni a un poligono che viene visualizzato Edge-on alla direzione della luce, ma non applica alcuna distorsione a un poligono che risponda direttamente alla luce. Nella figura 10 viene illustrato il modo in cui due pixel adiacenti possono alternarsi tra le ombreggiature e le ombreggiature durante i test sulla stessa inclinazione non distorta.

**Figura 10. Profondità ridimensionata inclinata-distorsione rispetto a profondità non distorta**

![profondità ridimensionata inclinata-distorsione rispetto a profondità non distorta](images/slope-scaled-depth-bias-compared-to-unbiased-depth.png)

### <a name="calculating-a-tight-projection"></a>Calcolo di una proiezione stretta

L'adattamento della proiezione della luce alla visualizzazione tronco aumenta la copertura della mappa Shadow. Nella figura 11 viene illustrato che utilizzando una proiezione arbitraria o adattando la proiezione ai limiti della scena, si ottiene un alias di prospettiva più elevato.

**Figura 11. Tronco ombreggiatura arbitraria e tronco Shadow adatta alla scena**

![tronco ombreggiatura arbitraria e tronco Shadow adatta alla scena](images/arbitrary-shadow-frustum-and-shadow-frustum-fit-to-scene.jpg)

La visualizzazione è dal punto di vista della luce. Il trapezio rappresenta la tronco della fotocamera della visualizzazione. La griglia disegnata sull'immagine rappresenta il mapping ombreggiatura. L'immagine a destra mostra che la stessa mappa Shadow della risoluzione crea una maggiore copertura Texel quando è più aderente alla scena.

Nella figura 12 vengono illustrati frustums che si adattano correttamente. Per calcolare la proiezione, gli otto punti che compongono la vista tronco vengono trasformati in uno spazio chiaro. Vengono quindi trovati i valori minimo e massimo in X e Y. Questi valori costituiscono i limiti di una proiezione ortogonale.

**Figura 12. Proiezione Shadow adatta per la visualizzazione tronco**

![proiezione Shadow adatta per la visualizzazione tronco](images/shadow-projection-fit-to-view-frustum.jpg)

È anche possibile ritagliare tronco alla scena AABB per ottenere un limite più restrittivo. Questa operazione non è consigliata in tutti i casi perché può modificare la dimensione della proiezione della fotocamera chiara dal fotogramma al frame. Molte tecniche, ad esempio quelle descritte nella sezione che spostano la luce Texel-Sized incrementi, forniscono risultati migliori quando le dimensioni della proiezione della luce rimangono costanti in ogni frame.

### <a name="calculating-the-near-plane-and-far-plane"></a>Calcolo del piano vicino e del piano lontano

Il piano vicino e il piano lontano sono i componenti finali necessari per calcolare la matrice di proiezione. Maggiore è la combinazione dei piani, più precisa è il valore del buffer di profondità.

Il buffer di profondità può essere a 16 bit, a 24 bit o a 32 bit, con valori compresi tra 0 e 1. In genere, i buffer di profondità sono punti fissi, con i valori vicini al piano vicino raggruppati più accuratamente rispetto ai valori vicini al piano lontano. Il grado di precisione disponibile per il buffer di profondità è determinato dal rapporto tra il piano vicino e il piano lontano. L'utilizzo del più stretto possibile piano Near/lontani potrebbe consentire l'utilizzo di un buffer di profondità a 16 bit. Un buffer di profondità A 16 bit può ridurre l'utilizzo della memoria aumentando la velocità di elaborazione.

### <a name="aabb-based-near-plane-and-far-plane"></a>AABB-Based piano vicino e piano lontano

Un modo semplice e ingenuo per calcolare il piano vicino e il piano lontano consiste nel trasformare il volume di delimitazione della scena nello spazio chiaro. Il valore più piccolo della coordinata Z è il piano vicino e il valore della coordinata Z più grande è il piano lontano. Per molte configurazioni della scena e della luce, questo approccio è sufficiente. Il caso peggiore, tuttavia, può causare una perdita significativa di precisione nel buffer di profondità; Nella figura 13 viene illustrato uno scenario di questo tipo. Qui l'intervallo del piano vicino al piano lontano è quattro volte più grande del necessario.

La visualizzazione tronco nella figura 13 è stata scelta intenzionalmente come piccola. Una piccola visualizzazione tronco viene visualizzata in una scena molto grande costituita da pilastri che si estendono dalla fotocamera di visualizzazione. L'uso della scena AABB per i piani near e lontani non è ottimale. L'algoritmo CSM descritto nell'articolo tecnico sulle [mappe Shadow a cascata](/windows/desktop/DxTechArts/cascaded-shadow-maps) deve calcolare i piani near e lontano per frustums di dimensioni molto ridotte.

**Figura 13. Piani vicini e lontani basati sulla scena AABB**

![piani vicini e lontani basati sulla scena AABB](images/near-far-%20planes-based-on-scene-aabb.jpg)

### <a name="frustum-based-near-plane-and-far-plane"></a>Frustum-Based piano vicino e piano lontano

Un'altra tecnica per il calcolo dei piani vicini e lontani consiste nel trasformare il tronco in uno spazio chiaro e usare rispettivamente i valori minimo e massimo in Z come piani vicini e lontani. La figura 14 illustra i due problemi con questo approccio. In primo luogo, il calcolo è troppo conservatore, come illustrato quando il tronco si estende oltre la geometria della scena. In secondo luogo, il piano vicino potrebbe essere troppo stretto, causando la ritaglio dei cast Shadow.

**Figura 14. Piani vicini e lontani basati esclusivamente sulla vista tronco**

![piani vicini e lontani basati esclusivamente sulla vista tronco](images/near-far-planes-based-solely-on-view-frustum.jpg)

### <a name="light-frustum-intersected-with-scene-to-calculate-near-and-far-planes"></a>Tronco chiaro intersecato con la scena per calcolare piani vicini e lontani

Il modo corretto per calcolare i piani vicini e lontani è illustrato nella figura 15. Quattro dei piani della luce ortogonale tronco sono stati calcolati utilizzando il valore minimo e massimo delle coordinate X e Y della vista tronco nello spazio chiaro. Gli ultimi due aerei della visualizzazione ortogonale tronco sono i piani near e lontani. Per trovare questi piani, i limiti della scena vengono ritagliati rispetto ai quattro piani tronco di luce noti. I valori Z più piccoli e più grandi dal limite appena ritagliato rappresentano rispettivamente il piano vicino e il piano lontano.

Il codice che esegue questa operazione si trova nell'esempio CascadedShadowMaps11. Gli otto punti che costituiscono i AABB del mondo vengono trasformati in uno spazio chiaro. La trasformazione dei punti nello spazio chiaro semplifica i test di ritaglio. I quattro piani noti della tronco Light possono ora essere rappresentati come righe. Le scene che delimitatino il volume nello spazio chiaro possono essere rappresentate da sei quadrilateri. Questi 6 quadrilateri possono quindi essere trasformati in 12 triangoli per il ritaglio basato su triangolo. I triangoli vengono ritagliati rispetto ai piani noti della vista tronco (si tratta di linee orizzontali e verticali in X e Y nello spazio chiaro). Quando un punto di intersezione viene trovato in X e Y, il triangolo 3D viene troncato in corrispondenza di quel punto. I valori Z minimo e massimo di tutti i triangoli ritagliati sono il piano vicino e il piano lontano. Nell'esempio CascadedShadowMaps11 viene illustrato come eseguire questo ritaglio nella funzione **ComputeNearAndFar** .

Sono disponibili altre due tecniche che è possibile usare per calcolare i piani più vicini e lontani. Queste tecniche non vengono visualizzate nell'esempio CascadedShadowMaps.

-   Anche i piani più stretti vicini e lontani possono essere calcolati intersecando una gerarchia di una scena o singoli oggetti in una scena con la luce tronco. Si tratta di un calcolo più complesso. Sebbene non sia illustrato nell'esempio CascadedShadowMaps11, potrebbe trattarsi di una tecnica valida per alcuni riquadri.
-   Il piano lontano può essere calcolato prendendo il minimo:

    -   Profondità maggiore della visualizzazione tronco nello spazio chiaro.
    -   Profondità massima dell'intersezione tra la visualizzazione tronco e la scena AABB.

Questo approccio può essere problematico quando viene usato con le mappe Shadow a cascata in cui è possibile indicizzare al di fuori di una vista tronco. In questo caso, potrebbe mancare la geometria della mappa Shadow.

**Figura 15. Piani vicini e lontani basati sull'intersezione dei quattro piani calcolati della tronco leggera e della geometria di delimitazione della scena**

![piani vicini e lontani basati sull'intersezione dei quattro piani calcolati della tronco leggera e della geometria di delimitazione della scena](images/near-far-plane-based-on-intersection-of-four.jpg)

### <a name="moving-the-light-in-texel-sized-increments"></a>Incremento della luce in incrementi di Texel-Sized

Un artefatto comune nelle mappe Shadow è l'effetto bordo luccicante. Quando la fotocamera viene spostata, i pixel lungo i bordi dell'ombreggiatura sono illuminati e scuriti. Questa operazione non può essere visualizzata in immagini ancora, ma è molto evidente e distrae in tempo reale. Nella figura 16 viene evidenziato il problema e nella figura 17 viene illustrato il modo in cui dovrebbero apparire i bordi Shadow.

Si verifica l'errore del bordo luccicante perché la matrice di proiezione chiara viene ricalcolata ogni volta che la fotocamera viene spostata. Ciò consente di creare differenze minime nelle mappe Shadow generate. Tutti i fattori seguenti possono influenzare la matrice creata per l'associazione della scena.

-   Dimensioni della vista tronco
-   Orientamento della visualizzazione tronco
-   Posizione della luce
-   Posizione della fotocamera

Ogni volta che la matrice cambia, i bordi delle ombreggiature potrebbero cambiare.

**Figura 16. Bordi ombreggiatura luccicanti**

![bordi ombreggiatura luccicanti](images/shimmering-shadow-edges.jpg)

I pixel lungo il bordo dell'ombreggiatura entrano e non rientrano nell'ombreggiatura quando la fotocamera viene spostata da sinistra a destra.

**Figura 17. Ombre senza bordi luccicanti**

![ombre senza bordi luccicanti](images/shadows-without-shimmering-edges.jpg)

I bordi dell'ombreggiatura rimangono costanti quando la fotocamera si sposta da sinistra a destra.

Per le luci direzionali, la soluzione a questo problema consiste nell'arrotondare il valore minimo o massimo in X e Y (che costituiscono i limiti di proiezione ortogonale) a incrementi di dimensioni in pixel. Questa operazione può essere eseguita con un'operazione di divisione, un'operazione Floor e una moltiplicazione.


```C++
        vLightCameraOrthographicMin /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMin = XMVectorFloor( vLightCameraOrthographicMin );
        vLightCameraOrthographicMin *= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax = XMVectorFloor( vLightCameraOrthographicMax );
        vLightCameraOrthographicMax *= vWorldUnitsPerTexel;
```



Il valore vWorldUnitsPerTexel viene calcolato accettando un limite della vista tronco e dividendo in base alle dimensioni del buffer.


```C++
        FLOAT fWorldUnitsPerTexel = fCascadeBound /
        (float)m_CopyOfCascadeConfig.m_iBufferSize;
        vWorldUnitsPerTexel = XMVectorSet( fWorldUnitsPerTexel, fWorldUnitsPerTexel,                            0.0f, 0.0f );
```



Il delimitatore delle dimensioni massime della vista tronco comporta una soluzione più flessibile per la proiezione ortogonale.

Quando si usa questa tecnica, è importante notare che la trama è maggiore di 1 pixel in larghezza e altezza. Questo consente di mantenere le coordinate Shadow dall'indicizzazione al di fuori della mappa Shadow.

### <a name="back-face-and-front-face"></a>Retro e faccia anteriore

È necessario eseguire il rendering delle mappe Shadow con l'abbattimento del back-face standard, un processo che ignora la rasterizzazione degli oggetti che il visualizzatore non può visualizzare e velocizza il rendering della scena. Un'altra opzione comune consiste nel eseguire il rendering delle mappe Shadow con l'abbattimento della facciata abilitata, il che significa che gli oggetti che si trovano nel visualizzatore vengono eliminati. L'argomento è che consente di eseguire l'ombreggiatura automatica perché la geometria che costituisce il retro degli oggetti è leggermente offset. Esistono due problemi con questa idea.

-   Qualsiasi oggetto con geometria front-end o back-face non corretta genera artefatti nella mappa Shadow. Tuttavia, se la geometria front-end o back-face non corretta provocherà altri problemi, è possibile che si presupponga che la geometria front-end e back-face venga eseguita correttamente. Potrebbe non essere pratico creare i visi indietro per la geometria basata su sprite, ad esempio il fogliame.
-   Peter panning e Gap Shadow vicino alla base di oggetti quali i muri hanno più probabilità di verificarsi perché la disparità della profondità ombreggiatura è troppo piccola.

### <a name="shadow-mapfriendly-geometry"></a>Mappa Shadow-geometria intuitiva

La creazione di geometria perfettamente funzionante nelle mappe shadow consente una maggiore flessibilità durante la lotta di artefatti come Peter panning e Shadow acne.

I bordi rigidi sono problematici per lo shadowing automatico. La disparità di profondità vicino alla punta del bordo è molto piccola. Anche un piccolo offset può causare la perdita delle ombre degli oggetti (Figura 18).

**Figura 18. I bordi affilati provocano la derivazione degli artefatti da una disparità bassa con offset**

![i bordi affilati provocano la derivazione degli artefatti da una disparità bassa con offset](images/sharp-edges-cause%20artifacts.jpg)

Gli oggetti narrow, ad esempio i muri, devono avere i backup anche se non sono mai visibili. In questo modo si aumenta la disparità della profondità.

È anche importante assicurarsi che la direzione della geometria sia corretta; ovvero all'esterno di un oggetto deve essere eseguito il back-end e l'interno di un oggetto deve essere di fronte. Si tratta di un aspetto importante per il rendering con l'abbattimento di back-face abilitato, nonché per contrastare gli effetti della distorsione della profondità.

## <a name="summary"></a>Riepilogo

Le tecniche descritte in questo articolo possono essere usate per aumentare la qualità delle mappe Shadow standard. Il passaggio successivo consiste nell'esaminare le tecniche che possono funzionare bene con le mappe Shadow standard. CSM sono consigliate come tecnica superiore per combattere l'aliasing della prospettiva. Per ammorbidire i bordi dell'ombreggiatura è possibile utilizzare le mappe shadow di varianza o filtro più vicino. Per ulteriori informazioni, vedere l'articolo tecnico sulle [mappe Shadow sovrapposte](/windows/desktop/DxTechArts/cascaded-shadow-maps) .

Donnelly, W. e Lauritzen, A. [varianza Maps](https://portal.acm.org/citation.cfm?doid=1111411.1111440). Simposio sulla grafica interattiva 3D, procedure del Simposio 2006 su grafica e giochi 3D interattivi. 2006, pp. 161 – 165.

Engel, Woflgang F. sezione 4. Mappe Shadow a cascata. ShaderX5, *Advanced rendering Techniques*, Wolfgang F. Engel, ed. Charles River Media, Boston, Massachusetts. 2006. pp. 197 – 206.

Stamminger, Marc e Drettakis, Giorgio. [Mappe Shadow della prospettiva](https://portal.acm.org/citation.cfm?id=566616). Conferenza internazionale sulla grafica dei computer e sulle tecniche interattive, *le procedure della 29 conferenza annuale sulla grafica del computer e le tecniche interattive*. 2002, pp 557 – 562.

Wimmer, M., Scherzer, D., e Purgathofer, W. [area chiara mappa Shadow Maps](https://www.cg.tuwien.ac.at/research/vr/lispsm/shadows_egsr2004_revised.pdf). EUROGRAPHICS Simposio sul rendering. 2004. Rivisto il 10 giugno 2005. [Technische Universität Wien](https://www.cg.tuwien.ac.at/research/vr/lispsm/).

 

 
