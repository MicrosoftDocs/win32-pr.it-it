---
title: Icone (nozioni di base sulla progettazione)
description: Le icone sono rappresentazioni pittoriche di oggetti, importanti non solo per motivi estetici come parte dell'identità visiva di un programma, ma anche per motivi utilitaristici come sintassi abbreviata per la trasmissione di un significato che gli utenti percepiscono quasi istantaneamente.
ms.assetid: 6f88cb32-ecfe-4e6e-a41b-31891cf510cf
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 9dc0994aa4e7aa07709a8051f9b13b72142bcb7b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104556031"
---
# <a name="icons-design-basics"></a>Icone (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Le icone sono rappresentazioni pittoriche di oggetti, importanti non solo per motivi estetici come parte dell'identità visiva di un programma, ma anche per motivi utilitaristici come sintassi abbreviata per la trasmissione di un significato che gli utenti percepiscono quasi istantaneamente. Windows Vista introduce un nuovo stile di iconografia che offre un livello di dettaglio e sofisticazione più elevato per Windows.

**Nota:** Le linee guida correlate alle [icone standard](vis-std-icons.md) vengono presentate in un articolo separato.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Aero è il nome dell'esperienza utente di Windows Vista, che rappresenta sia i valori incorporati nella progettazione delle estetiche, sia la visione sottostante all'interfaccia utente (UI). Aero sta per: autentico, energico, riflettente e aperto. Aero mira a definire un progetto che sia professionale che bello. L'estetica Aero crea un'esperienza di qualità elevata ed elegante che facilita la produttività degli utenti e persino una risposta emotiva.

Le icone di Windows Vista sono diverse dalle icone di tipo Windows XP nei modi seguenti:

-   Lo stile è più realistico rispetto a quello esemplificativo, ma non abbastanza realistico. Le icone sono immagini simboliche che dovrebbero avere un aspetto migliore rispetto a quella fotorealistica.
-   Le icone hanno una dimensione massima di 256x256 pixel, in modo da renderle appropriate per le visualizzazioni a DPI elevato (punti per pollice). Queste icone ad alta risoluzione consentono una qualità visiva elevata nelle visualizzazioni elenco con icone grandi.
-   Laddove le icone di documento fisse e pratiche siano sostituite dalle anteprime del contenuto, semplificando l'identificazione e la ricerca dei documenti.
-   Le icone della barra degli strumenti hanno un minor numero di dettagli e nessuna prospettiva, da ottimizzare per dimensioni ridotte e caratteristiche visive.

Icone ben progettate:

-   Migliorare la comunicazione visiva del programma.
-   Impatto generale sugli utenti sulla progettazione visiva del programma e sull'apprezzamento per la sua idoneità.
-   Migliorare l'usabilità semplificando l'identificazione, l'apprendimento e la ricerca di programmi, oggetti e azioni.

Le immagini seguenti illustrano il modo in cui lo stile Aero dell'iconografia in Windows Vista è diverso da quello utilizzato in Windows XP.

![immagini delle icone del blocco e della chiave](images/vis-icons-image1.png)

Le icone di Windows Vista (il blocco e la chiave a sinistra) sono autentiche, croccanti e dettagliate. Ne viene eseguito il rendering anziché disegnata, ma non sono completamente fotorealistici.

![immagini delle icone del notebook Globe e spirale](images/vis-icons-image2.png)

Le icone di Windows Vista (le due a sinistra) sono professionali e bellissime, con particolare attenzione ai dettagli che migliorano la qualità della produzione di icone.

![immagini di notebook, blocco, monitoraggio e carta](images/vis-icons-image3.png)

Queste icone di Windows Vista mostrano il bilanciamento ottico e l'accuratezza percepita nella prospettiva e nei dettagli. In questo modo è possibile che l'aspetto sia grande o piccolo, chiuso o da una distanza. Questo stile di iconografia funziona inoltre per schermi ad alta risoluzione.

![immagine di un'icona del router wireless](images/vis-icons-image4.png)![immagine di un foglio di carta icona](images/vis-icons-image5.png)![immagine di un'icona a destra grande, verde](images/vis-icons-image6.png)

In questi esempi vengono illustrati diversi tipi di icone, tra cui un oggetto tridimensionale in prospettiva, un'icona con il front-end (Flat) e un'icona della barra degli strumenti.

## <a name="guidelines"></a>Indicazioni

### <a name="perspective"></a>Prospettiva

-   **Le icone in Windows Vista sono tridimensionali e sono mostrate in prospettiva come oggetti solidi o oggetti bidimensionali visualizzati direttamente.** Usare icone piatte per i file e per gli oggetti effettivamente Flat, ad esempio documenti o fogli di carta.

    ![immagini del computer 3D e della carta Flat, 2D ](images/vis-icons-image7.png)

    Icone tipiche 3D e Flat.

-   **Gli oggetti tridimensionali sono rappresentati nella prospettiva come oggetti solidi, visti da una visualizzazione a bassa Birds-Eye con due punti di dissolvenza.**

    ![immagine del notebook con linee che mostrano la prospettiva](images/vis-icons-image8.png)

    In questo esempio vengono illustrati punti di vista e di dissolvenza tipici delle icone 3D.

-   **Nelle dimensioni più piccole, la stessa icona può variare da una prospettiva a una diretta.** Alla dimensione di 16x16 pixel e di dimensioni inferiori, eseguire il rendering delle icone direttamente (front-end). Per le icone più grandi, usare Perspective.

    -   **Eccezione:** Le icone della barra degli strumenti sono sempre in primo piano, anche in dimensioni maggiori.

    ![immagine di un computer 3D di grandi dimensioni e di un piccolo computer 2D ](images/vis-icons-image9.png)

    Questo esempio mostra in che modo la stessa icona viene gestita in modo diverso, a seconda delle dimensioni.

### <a name="light-source"></a>Sorgente di luce

-   **La sorgente di luce per gli oggetti all'interno della griglia prospettiva è sopra, leggermente davanti a e leggermente a sinistra dell'oggetto.**
-   **La sorgente di luce esegue il cast delle ombreggiature leggermente verso il lato anteriore e destro della base dell'oggetto.**
-   **Tutti i raggi luminosi sono paralleli e colpiscono l'oggetto lungo lo stesso angolo (ad esempio il sole).** L'obiettivo è avere un aspetto di illuminazione uniforme in tutte le icone e gli effetti Spotlight. I raggi luminosi paralleli producono ombre che hanno tutti la stessa lunghezza e densità, offrendo un'ulteriore Unity tra più icone.

### <a name="shadows"></a>Ombreggiature

**Generale**

-   **Utilizzare le ombreggiature per sollevare oggetti visivamente dallo sfondo e per fare in modo che gli oggetti 3D vengano visualizzati a terra, piuttosto che a una virgola mobile.**
-   **Usare un intervallo di opacità pari al 30-50% per le ombreggiature.** A volte è necessario usare un livello di ombreggiatura diverso, a seconda della forma o del colore di un'icona.
-   **Feather o abbreviare l'ombreggiatura, se necessario, per evitare che venga ritagliata in base alle dimensioni della casella di icone.**
-   **Non usare le ombreggiature nelle icone a 24x24 o dimensioni inferiori.**

    ![immagini di icone 3D con ombre ](images/vis-icons-image10.png)

    Icone tipiche ombreggiatura.

**Icone Flat**

-   **Le icone flat vengono in genere usate per le icone di file e gli oggetti reali Flat,** ad esempio un documento o un foglio di carta.
-   **L'illuminazione dell'icona piatta deriva dall'angolo superiore sinistro a 130 gradi.**
-   **Le icone più piccole, ad esempio 16x16 e 32x32, sono semplificate per migliorare la leggibilità.** Tuttavia, se contengono una reflection all'interno dell'icona (spesso semplificata), possono avere un'ombreggiatura stretta. Gli intervalli di ombreggiatura sono in opacità del 30-50%.
-   **Gli effetti dei livelli possono essere usati per le icone Flat, ma devono essere confrontati con altre icone piane.** Le ombreggiature per gli oggetti variano in parte, in base all'aspetto migliore ed è più coerente all'interno del set di dimensioni e con le altre icone di Windows Vista. In alcuni casi, potrebbe anche essere necessario modificare le ombre. Ciò si verifica soprattutto quando gli oggetti sono disposti su altri.
-   **Per ottenere il risultato desiderato, è possibile utilizzare un intervallo di colori sottile.** Ombreggiatura gli oggetti della guida si trovano nello spazio. Il colore influisca sul peso percepito dell'ombreggiatura e può falsare l'immagine se è troppo pesante.

![screenshot della finestra di dialogo con l'ombreggiatura selezionata ](images/vis-icons-image11.png)![screenshot dell'icona della carta con ombreggiatura stretta ](images/vis-icons-image12.png)

L'opzione ombreggiatura nella finestra di dialogo stile livello e un'ombreggiatura tipica per un'icona piatta.

**Intervalli di ombreggiatura di base icona piatta**



| Caratteristica                              | Range                                                         |
|-------------------------------|----------------------------------------------------------|
| Colore<br/>              | Black<br/>                                         |
| Modalità Blend<br/>         | Moltiplicazione<br/>                                      |
| Opacità<br/>            | 22-50%, a seconda del colore dell'elemento<br/> |
| Angle<br/>              | 120-130 (utilizzare la luce globale)<br/>                    |
| Distanza<br/>           | 3 per 256x256, a partire da 1 per 32x32<br/>    |
| Spread<br/>             | 0<br/>                                             |
| Dimensione<br/>               | 7 per 256x256, che va giù a 2 per 32x32<br/>    |



 

**Icone tridimensionali**

-   Creare ombre per le icone 3D in base alla distinzione tra maiuscole e minuscole, con un impegno per adattarsi a una gamma di distanza di cast e di feathering a completamente trasparente. Creare le immagini di dimensioni leggermente inferiori rispetto alle dimensioni complessive dell'icona per consentire lo spazio per un'ombreggiatura (per le dimensioni che ne richiedono uno). Assicurarsi che l'ombreggiatura non si concluda bruscamente al bordo dell'icona.

![Illustrazione della creazione di ombre in Photoshop](images/vis_icons_image13.jpeg)

![Illustrazione di quattro oggetti con ombreggiature variabili](images/vis_icons_image14.jpeg)

In questi esempi vengono illustrate le varianti create in base alla forma e alla posizione dell'oggetto stesso. È talvolta necessario che l'ombreggiatura sia in piuma o abbreviata per evitare che venga ritagliata in base alle dimensioni della casella di icone.

### <a name="color-and-saturation"></a>Colore e saturazione

-   **I colori sono in genere meno saturi rispetto a Windows XP.**
-   **Usare le sfumature per creare un'immagine più realistica.**
-   **Sebbene non esistano tavolozze dei colori specifiche per le icone standard, tenere presente che è necessario che funzionino insieme in molti contesti e temi.** Preferire il set standard di colori; Non ricolorare le icone standard, ad esempio le icone di avviso, perché in questo modo si interrompe la capacità degli utenti di interpretare il significato. Per altre linee guida, vedere [color](vis-color.md).
-   **I file icona richiedono anche versioni a 8 bit e a 4 bit** per supportare l'impostazione predefinita in un desktop remoto. Questi file possono essere creati tramite un processo batch, ma devono essere rivisti, in quanto alcuni richiederanno il ritocco per una migliore leggibilità.

    ![screenshot della finestra di dialogo di selezione colori ](images/vis-icons-image15.png)

    Non esiste alcuna restrizione rigida per la tavolozza dei colori. Viene evitata solo la saturazione completa (in alto a destra).

-   Livelli di bit: progettazione ICO per 32 bit (incluso Alpha) + 8 bit + 4 bit (dipendono automaticamente da un solo pixel poke). È necessario includere solo una copia a 32 bit dell'immagine 256x256 pixel e solo l'immagine 256x256 pixel deve essere compressa per ridurre le dimensioni del file. Diversi strumenti per le icone offrono la compressione per Windows Vista.
-   Livelli di bit: barre degli strumenti a 24 bit + Alpha (maschera a 1 bit), a 8 bit e a 4 bit.
-   Barre degli strumenti o file AVI: usare Magenta (R255 G0 B255) come colore di trasparenza dello sfondo.

### <a name="size-requirements"></a>Requisiti di dimensione

**Generale**

-   **Prestare particolare attenzione alle icone con visibilità elevata,** ad esempio icone principali dell'applicazione, icone di file che possono essere visualizzate in Esplora risorse e icone visualizzate nel menu Start o sul desktop.
    -   **Icone dell'applicazione e elementi del pannello di controllo:** Il set completo include 16x16, 32x32, 48x48 e 256x256. il codice è scalabile tra 32 e 256. Il formato del file ico è obbligatorio. Per la modalità classica, il set completo è 16x16, 24x24, 32x32, 48x48 e 64x64.
    -   **Opzioni dell'icona dell'elemento elenco:** Usare anteprime o icone di file del tipo di file (ad esempio, doc); set completo.
    -   **Icone della barra degli strumenti:** 16x16, 24x24, 32x32. Si noti che le icone della barra degli strumenti sono sempre piatte, non 3D, anche alla dimensione 32x32.
    -   **Icone della finestra di dialogo e della procedura guidata:** 32x32 e 48x48.
    -   **Sovrapposizioni:** Codice shell principale (ad esempio, un collegamento) 10x10 (per 16x16), 16x16 (per 32x32), 24x24 (per 48x48), 128x128 (per 256x256). Si noti che alcuni di questi sono leggermente più piccoli ma sono vicini a queste dimensioni, a seconda della forma e del bilanciamento ottico.
    -   **Area avvio veloce:** Le icone si ridurranno da 48x48 nelle sovrapposizioni dinamiche con ALT + TAB, ma per una versione più nitida aggiungere un file 40x40 al file con estensione ico.
    -   **Icone a fumetti:** 32x32 e 40x40.
    -   **Dimensioni aggiuntive:** Questi possono essere usati come risorse per creare altri file, ad esempio annotazioni, strisce della barra degli strumenti, sovrapposizioni, DPI alti e casi speciali: 128x128, 96x96, 64x64, 40x40, 24x24, 22x22, 14x14, 10x10 e 8x8 Virtual. È possibile usare. ico,. png,. bmp o altri formati di file, a seconda del codice in tale area.

**Per valori DPI alti**

-   Windows Vista è destinato a 96 dpi e 120 dpi.

Le tabelle seguenti illustrano esempi di proporzioni di scalabilità applicate a due dimensioni delle icone comuni. Si noti che non tutte le dimensioni devono essere incluse nel file con estensione ico. Il codice aumenterà le dimensioni di quelle più grandi.



| dpi                   | Dimensioni icona                         | Fattore di scala                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 16x16<br/>         | 1,0 (100%)<br/>       |
| 120<br/>     | 20x20<br/>         | 1,25 (125%)<br/>      |
| 144<br/>     | 24x24<br/>         | 1,5 (150%)<br/>       |
| 192<br/>     | 32x32<br/>         | 2,0 (200%)<br/>       |



 



| dpi                   | Dimensioni icona                         | Fattore di scala                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 32x32<br/>         | 1,0 (100%)<br/>       |
| 120<br/>     | 40x40<br/>         | 1,25 (125%)<br/>      |
| 144<br/>     | 48x48<br/>         | 1,5 (150%)<br/>       |
| 192<br/>     | 64x64<br/>         | 2,0 (200%)<br/>       |



 

**Dimensioni file ICO (standard)**

![Diagramma che mostra le diverse icone del router di dimensioni standard.](images/vis-icons-image16.png)

**dimensioni dei file ICO (casi speciali)**

![illustrazione delle icone del router di dimensioni diverse ](images/vis-icons-image17.png)

**Annotazioni e sovrapposizioni**

-   Le annotazioni vanno nell'angolo inferiore destro dell'icona e devono riempire il 25% dell'area icona.
    -   **Eccezione:** le icone 16x16 accettano le annotazioni 10x10.
-   Non usare più di un'annotazione su un'icona.
-   Le sovrimpressioni vengono inserite nell'angolo inferiore sinistro dell'icona e il 25% dell'area icona.
    -   **Eccezione:** le icone 16x16 accettano sovrimpressioni 10x10.

### <a name="level-of-detail"></a>Livello di dettaglio

-   le dimensioni 16x16 di molte di queste icone sono ancora ampiamente utilizzate e pertanto importanti.
-   I dettagli in un'icona di questa dimensione devono indicare chiaramente il punto chiave dell'icona.
-   Poiché un'icona è più piccola, la trasparenza e alcuni dettagli speciali trovati in dimensioni maggiori dovrebbero essere sacrificati per semplificare e ottenere il punto.
-   Gli attributi e i colori devono essere esagerati e usati per evidenziare i moduli chiave.

    ![illustrazione di uno o due dispositivi di piccole dimensioni ](images/vis-icons-image18.png)

    In 16x16, l'icona del dispositivo audio portatile potrebbe essere facilmente confusa per un telefono cellulare, in modo che la parte dell'orecchio sia un dettaglio visivo chiave da visualizzare.

-   Semplicemente la scalabilità verso il basso rispetto alle dimensioni di 256x256 non funziona.
-   Tutte le dimensioni richiedono il livello di dettaglio pertinente; minore è l'icona più è necessario per esagerare i dettagli di definizione.

    ![illustrazione dei telefoni cellulari con dettagli chiari ](images/vis-icons-image19.png)

    ![illustrazione dei telefoni cellulari con dettagli sfocatura ](images/vis-icons-image20.png)

### <a name="icon-development"></a>Sviluppo di icone

**Progettazione e produzione di icone**

-   **Assumere un graphic designer esperto.** Per la grafica, le immagini e le icone eccezionali funzionano con gli esperti. Si consiglia di sperimentare le illustrazioni usando i programmi Vector Art o 3D.
-   Pianificare l'esecuzione di **serie di iterazioni,** da sketch iniziali del concetto, a simulazioni nel contesto, fino alla revisione finale della produzione e al completamento delle icone nel prodotto funzionante.
-   **La creazione di icone in anticipo può essere costosa.** Raccogliere tutti i dettagli e i requisiti esistenti, ad esempio: il set completo di icone necessarie; funzione principale e significato per ciascuna; famiglie o cluster nel set che si desidera siano evidenti; requisiti del marchio; i nomi di file esatti; formati di immagine usati nel codice. e requisiti di dimensione. Assicurarsi prima di tutto che sia possibile sfruttare al massimo il tempo con la finestra di progettazione.
-   **Tenere presente che la finestra di progettazione potrebbe non avere familiarità con il prodotto, quindi fornire le informazioni funzionali, le schermate e le sezioni specifiche, a seconda delle esigenze.**
-   **Pianificare le verifiche geopolitiche e legali nel modo appropriato.**
-   **Eseguire il mapping di un intervallo di tempo e disporre di comunicazione normale.**

**Da sketch di concept a End-Product**

![illustrazione dello sviluppo di schizzi di telefoni cellulari ](images/vis-icons-image21.png)

-   Creare sketch concettuali.
-   Provare il concetto con dimensioni diverse.
-   Se necessario, eseguire il rendering in 3D.
-   Testare le dimensioni su colori di sfondo diversi.
-   Valutare le icone nel contesto dell'interfaccia utente reale.
-   Genera il file. ico finale o altri formati di risorse grafiche.

**Strumenti**

-   **Matita e carta:** Idee concettuali iniziali, elencate e delineate.
-   **massimo 3D Studio:** Eseguire il rendering degli oggetti 3D nella prospettiva.
-   **Adobe Photoshop:** Eseguire lo sketch e l'iterazione, simulare il contesto e finalizzare i dettagli.
-   **Adobe Illustrator/Macromedia FreeHand:** Eseguire lo sketch e l'iterazione, finalizzare i dettagli.
-   **Gamani GIF Movie Gear:** Produce il file con estensione ICO (con compressione se necessario).
-   **Workshop sull'icona Assiis:** Produce il file con estensione ICO (con compressione se necessario).
-   Microsoft Visual Studio non supporta le icone di Windows Vista (non è disponibile alcun supporto per il canale alfa o più di 256 colori).

**Produzione**

> [!TIP]
> Attenersi alla procedura seguente per creare un singolo file con estensione ico contenente più dimensioni di immagine e profondità dei colori.

**Passaggio 1: concettualizzazione**

-   Usare i concetti stabiliti laddove possibile, per garantire la coerenza dei significati per l'icona e la relativa pertinenza ad altri usi.
-   Prendere in considerazione il modo in cui l'icona viene visualizzata nel contesto dell'interfaccia utente e come può funzionare come parte di un set di icone.
-   Se si modifica un'icona esistente, valutare se è possibile ridurre la complessità.
-   Considerare l'effetto culturale della grafica. Evitare di usare lettere, parole, mani o visi nelle icone. Se necessario, rappresenta le rappresentazioni di persone o utenti nel modo più generico possibile.
-   Se si combinano più oggetti in una singola immagine in un'icona, valutare il modo in cui l'immagine viene ridimensionata a dimensioni inferiori. Utilizzare non più di tre oggetti in un'icona (due sono preferiti). Per le dimensioni 16x16, è consigliabile rimuovere gli oggetti o semplificare l'immagine per migliorare il riconoscimento.
-   Non usare il flag di Windows nelle icone.

**Passaggio 2: illustrare**

-   Per illustrare le icone di stile di Windows Aero, usare uno strumento vettoriale, ad esempio Macromedia FreeHand o Adobe Illustrator. Utilizzare le caratteristiche della tavolozza e dello stile come descritto in precedenza in questo articolo.
-   Illustrare l'immagine usando FreeHand o Illustrator. Copiare e incollare le immagini vettoriali in Adobe Photoshop.
-   Creare e usare un livello di modello in Photoshop per assicurarsi che le operazioni vengano eseguite nelle aree quadrate delle dimensioni regolamentate.
-   Creare le immagini di dimensioni leggermente inferiori rispetto alle dimensioni complessive dell'icona per consentire lo spazio per un'ombreggiatura (per le dimensioni che ne richiedono uno).
-   Posizionare le immagini nella parte inferiore dei quadrati, in modo che tutte le icone di una directory siano posizionate in modo coerente. Evitare di tagliare le ombre.
-   Se si aggiunge un altro oggetto a un'immagine o a una serie, conservarlo in una posizione fissa e posizionare le immagini di dimensioni inferiori piane in una posizione fissa, ad esempio la parte inferiore sinistra o superiore destra, a seconda del caso.

**Passaggio 3: creare le immagini a 24 bit**

-   Una volta incollate le dimensioni in Photoshop, controllare la leggibilità delle immagini, soprattutto in 16x16 e dimensioni inferiori. Potrebbe essere necessario disporre dei pixel con le percentuali di colori. Potrebbe essere necessaria anche la riduzione della trasparenza. È frequente esagerare gli aspetti a dimensioni inferiori ed eliminare anche gli aspetti, per concentrare l'attenzione sul punto chiave.
-   Le icone a 8 bit verranno visualizzate in qualsiasi modalità di colore inferiore a 32 bit e non avranno il canale alfa a 8 bit, quindi potrebbero dover avere i bordi o più puliti perché non esiste un anti-aliasing (i bordi possono essere irregolari e l'immagine potrebbe essere difficile da leggere).
-   In Photoshop duplicare il livello immagine a 24 bit e rinominare il livello in immagini a 4 bit. Indicizzare le immagini a 4 bit nella tavolozza dei colori di Windows 16.
-   Pulire le immagini usando solo i colori della tavolozza dei colori 16. I delineamenti eseguiti da versioni più scure o più chiare dei colori dell'oggetto sono in genere preferibili a grigio o nero.
-   Se si utilizza una bitmap, assicurarsi che il colore di sfondo non venga utilizzato nell'immagine stessa, perché tale colore sarà il colore trasparente. Magenta (R255 G0 B255) viene spesso usato come colore di trasparenza in background.

**Passaggio 4: creare le immagini a 8 bit e a 4 bit**

-   Ora che le immagini a 24 bit sono pronte per essere apportate nelle icone a 32 bit, è necessario creare versioni a 8 bit.
-   Questo è il momento ideale per testare le schermate contestuali. È sorprendente ciò che può essere individuato visualizzando altre icone o una famiglia di icone nel contesto. Questo passaggio consente di risparmiare tempo e denaro. È preferibile rilevare i problemi prima che i file vengano passati attraverso la produzione e non siano più disponibili.
-   Aggiungere l'ombreggiatura alle immagini in dimensioni che le richiedono.
-   Unire le immagini a ombreggiatura e a 24 bit insieme.
-   Creare un nuovo file di Photoshop per ogni dimensione. Copiare e incollare l'immagine appropriata. Salvare ogni file come file con estensione PSD.
-   Non unire il livello immagine con il livello di sfondo. È utile includere le dimensioni e la profondità dei colori nel nome file mentre si lavora, ma è possibile che il file debba essere rinominato.

**Passaggio 5: creare il file ICO**

-   Scegli l'applicazione che meglio soddisfa le esigenze e le competenze degli artisti. Tenere presente che le icone da usare in un prodotto di spedizione devono essere create in uno strumento acquistato o concesso in licenza. Ciò significa che non è possibile usare le versioni di valutazione.
-   Entrambi i prodotti elencati di seguito sono stati usati da progettisti che hanno prodotto icone per Windows Vista e ognuno offre la possibilità di esportare in Adobe Photoshop CS.
    -   Gamani GIF Movie Gear: produce il file ICO
    -   Workshop sull'icona assial: Produci file ICO
-   Visual Studio non supporta le icone di Windows Vista (non è disponibile alcun supporto per il canale alfa o più di 256 colori), quindi non è consigliabile usarlo.
-   I file icona (formato ICO) devono contenere le versioni a 4 e 8 bit, oltre a 24 bit + alpha.
-   Salvare i file come "icona di Windows (. ico)", indipendentemente dal programma di creazione dell'icona che si sceglie di usare.
-   Alcune risorse iconografiche possono essere effettivamente strisce bitmap, che richiedono anche un canale alfa, ad esempio per le barre degli strumenti, o file con estensione png salvati con la trasparenza. Non tutti sono necessariamente formati. ico; verificare il formato supportato nel codice.

**Passaggio 6: valutare**

-   Esaminare tutte le dimensioni.
-   Esaminare la famiglia per valutare la somiglianza, il bilanciamento ottico e la distinzione tra le famiglie.
-   Esaminare nel contesto per valutare i pesi e la visibilità relativi (assicurarsi che non sia dominata).
-   Si prendano in considerazione i casi che potrebbero non essere usati adesso, ma che potrebbero essere in futuro. È possibile che questa icona sia mai stata annotata o che sia presente una sovrapposizione?
-   Esaminare il codice.

### <a name="icons-in-the-context-of-list-views-toolbars-and-tree-views"></a>Icone nel contesto di visualizzazioni elenco, barre degli strumenti e visualizzazioni albero

**Visualizzazioni elenco**

-   Per Windows Vista, utilizzare anteprime per i file che contengono contenuto visivamente distinto su scala ridotta, in modo che gli utenti possano riconoscere direttamente il file cercato. (Usare l'anteprima di Windows Application Programming Interface per questo).

    ![Screenshot di Esplora risorse con icone di cartella ](images/vis-icons-image22.png)

-   Icona dell'applicazione sovrapposta (non mostrata qui) nelle anteprime guida l'associazione con l'applicazione per il tipo di file, oltre a visualizzare l'anteprima del file.

**Nota:** Per i file senza contenuto visivo distinto, non usare le anteprime. Usare invece icone di file simbolici tradizionali che mostrano la rappresentazione dell'oggetto e l'applicazione o il tipo associato.

**Barre degli strumenti**

-   Le icone visualizzate in una barra degli strumenti devono avere un bilanciamento ottico di dimensioni, colori e complessità.
-   Testare le icone potenziali in una schermata contestuale per evitare eventuali squilibri o sbilanciamenti indesiderati.
-   Il testing nelle schermate consente di evitare le iterazioni onerose nel codice.
-   Esaminare anche le icone nel codice. Il movimento e altri fattori possono influiscono sul successo di un'icona; in alcuni casi potrebbero essere necessarie altre iterazioni.

![screenshot della barra degli strumenti con icone ed etichette piccole ](images/vis-icons-image23.png)

Nell'esempio precedente, il saldo ottico non è ancora stato raggiunto.

![illustrazione delle icone in diversi background ](images/vis-icons-image24.png)

Provare le iterazioni nel contesto.

**Visualizzazioni albero**

-   Il bilanciamento ottico è necessario per mantenere la gerarchia in un controllo di visualizzazione albero.
-   Pertanto, le icone utilizzate in genere in questo contesto devono essere valutate in questa posizione. In alcuni casi, una particolare icona di 16x16 deve essere resa più piccola perché la sua forma ha una dominanza ottica rispetto ad altri.
-   La compensazione per gli squilibri ottici è una parte importante della creazione di icone di qualità superiore.

![Figura di due set di cartelle nella visualizzazione albero ](images/vis-icons-image25.png)

 

