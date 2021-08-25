---
title: Icone (nozioni di base sulla progettazione)
description: Le icone sono rappresentazioni tipiche di oggetti, importanti non solo per motivi estetici come parte dell'identità visiva di un programma, ma anche per motivi utilitari come abbreviazione per trasmettere un significato che gli utenti percepiranno quasi istantaneamente.
ms.assetid: 6f88cb32-ecfe-4e6e-a41b-31891cf510cf
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ad788338adc81bd9bc796412eebf4bef87ceca2b7a3855e024702a3e1bb23e49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841858"
---
# <a name="icons-design-basics"></a>Icone (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Le icone sono rappresentazioni tipiche di oggetti, importanti non solo per motivi estetici come parte dell'identità visiva di un programma, ma anche per motivi utilitari come abbreviazione per trasmettere un significato che gli utenti percepiranno quasi istantaneamente. Windows Vista introduce un nuovo stile di iconografia che offre un livello superiore di dettaglio e sofisticato per Windows.

**Nota:** Le linee guida relative [alle icone standard](vis-std-icons.md) sono presentate in un articolo separato.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Aero è il nome per l'esperienza utente di Windows Vista, che rappresenta sia i valori racchiusi nella progettazione dell'aspetto estetico, sia la visione dietro l'interfaccia utente. Aero è l'acronimo di: authentic, energetic, reflective e open. L'obiettivo di Aero è definire un design sia professionale che di bell'aspetto. L'aspetto estetico di Aero crea un'esperienza di alta qualità ed elegante che facilita la produttività degli utenti e determina anche una risposta emozionale.

Windows Le icone di Vista Windows icone in stile XP nei modi seguenti:

-   Lo stile è più realistico che illustrativo, ma non abbastanza fotorealistico. Le icone sono immagini simboliche che dovrebbero avere un aspetto migliore rispetto a quelle fotorealistiche.
-   Le icone hanno dimensioni massime di 256 x 256 pixel, rendendole idonee per i display ad alta risoluzione (punti per pollice). Queste icone ad alta risoluzione consentono una qualità visiva elevata nelle visualizzazioni elenco con icone grandi.
-   Laddove possibile, le icone fisse dei documenti vengono sostituite da anteprime del contenuto, semplificando l'identificazione e la ricerca dei documenti.
-   Le icone della barra degli strumenti hanno meno dettagli e nessuna prospettiva, per ottimizzare dimensioni più piccole e distintività visiva.

Icone ben progettate:

-   Migliorare la comunicazione visiva del programma.
-   Influiscono fortemente sull'impressione complessiva degli utenti sulla progettazione visiva del programma e sulla stima per la sua idoneità e fine.
-   Migliorare l'usabilità semplificando l'identificazione, l'apprendimento e la ricerca di programmi, oggetti e azioni.

Le immagini seguenti illustrano ciò che rende lo stile Aero dell'iconografia in Windows Vista diverso da quello usato in Windows XP.

![immagini di icone di blocco e chiave](images/vis-icons-image1.png)

Le Windows di Vista (il blocco e la chiave a sinistra) sono autentiche, nitide e dettagliate. Vengono sottoposti a rendering anziché disegnati, ma non sono completamente fotorealistici.

![immagini delle icone dei notebook globo e della mappa a forma di globo](images/vis-icons-image2.png)

Le Windows Di Vista (le due a sinistra) sono professionali e belle, con attenzione ai dettagli che migliorano la qualità di produzione delle icone.

![immagini di notebook, blocchi, monitor e carta](images/vis-icons-image3.png)

Queste icone Windows Vista mostrano l'equilibrio ottico e l'accuratezza percepita in prospettiva e nei dettagli. In questo modo possono avere un aspetto grande o piccolo, da vicino o da lontano. Inoltre, questo stile di iconografia funziona per schermi ad alta risoluzione.

![immagine dell'icona di un router wireless](images/vis-icons-image4.png)![immagine dell'icona di un foglio di carta](images/vis-icons-image5.png)![immagine di un'icona a forma di freccia destra verde grande](images/vis-icons-image6.png)

Questi esempi illustrano diversi tipi di icone, tra cui un oggetto tridimensionale in prospettiva, un'icona frontale (flat) e un'icona della barra degli strumenti.

## <a name="guidelines"></a>Indicazioni

### <a name="perspective"></a>Prospettiva

-   **Le icone in Windows Vista sono tridimensionali e visualizzate in prospettiva come oggetti solidi o oggetti bidimensionali visualizzati direttamente.** Usare icone flat per i file e per gli oggetti effettivamente flat, ad esempio documenti o fogli di carta.

    ![immagini di computer 3d e flat, carta 2d ](images/vis-icons-image7.png)

    Icone 3D e flat tipiche.

-   **Gli oggetti tridimensionali sono rappresentati in prospettiva come oggetti solidi, visti da una vista a punta bassa con due punti di scomparsa.**

    ![Immagine del notebook con linee che mostrano la prospettiva](images/vis-icons-image8.png)

    Questo esempio illustra i punti di prospettiva e di scomparsa tipici delle icone 3D.

-   **Nelle dimensioni più piccole, la stessa icona può cambiare da prospettiva a lineare.** Con dimensioni di 16x16 pixel e dimensioni inferiori, eseguire il rendering delle icone direttamente su (front-facing). Per le icone più grandi, usare la prospettiva.

    -   **Eccezione:** Le icone della barra degli strumenti sono sempre front-facing, anche in dimensioni maggiori.

    ![immagine di un computer 3D di grandi dimensioni e di un computer 2D di piccole dimensioni ](images/vis-icons-image9.png)

    Questo esempio mostra come la stessa icona viene trattata in modo diverso, a seconda delle dimensioni.

### <a name="light-source"></a>Sorgente di luce

-   **La sorgente di luce per gli oggetti all'interno della griglia prospettica è sopra, leggermente davanti e leggermente a sinistra dell'oggetto.**
-   **La sorgente di luce proietta ombreggiature leggermente nella parte posteriore e a destra della base dell'oggetto.**
-   **Tutti i raggi di luce sono paralleli e colpiscono l'oggetto lungo lo stesso angolo (come il sole).** L'obiettivo è avere un aspetto di illuminazione uniforme in tutte le icone e gli effetti spotlight. I raggi di luce paralleli producono ombreggiature che hanno tutte la stessa lunghezza e densità, offrendo un'ulteriore unità tra più icone.

### <a name="shadows"></a>Ombreggiature

**Generale**

-   **Usare le ombreggiature per elevare visivamente gli oggetti dallo sfondo e fare in modo che gli oggetti 3D vengano visualizzati a terra, anziché fluttuare in modo goffo nello spazio.**
-   **Usare un intervallo di opacità compreso tra 30 e 50% per le ombreggiature.** A volte è necessario usare un livello di ombreggiatura diverso, a seconda della forma o del colore di un'icona.
-   **Sfumatura o abbreviamento dell'ombreggiatura, se necessario, per evitare che venga ritagliata dalle dimensioni della casella dell'icona.**
-   **Non usare ombreggiature nelle icone con dimensioni 24x24 o inferiori.**

    ![immagini di icone 3D con ombreggiature ](images/vis-icons-image10.png)

    Ombreggiature tipiche dell'icona.

**Icone flat**

-   **Le icone flat vengono in genere usate per icone di file** e oggetti reali flat, ad esempio un documento o un foglio di carta.
-   **L'illuminazione a icona piana viene visualizzata in alto a sinistra a 130 gradi.**
-   **Le icone più piccole, ad esempio 16x16 e 32x32, sono semplificate per la leggibilità.** Tuttavia, se contengono una reflection all'interno dell'icona (spesso semplificata), possono avere un'ombreggiatura stretta. L'ombreggiatura ha intervalli di opacità dal 30 al 50%.
-   **Gli effetti livello possono essere usati per le icone flat, ma devono essere confrontati con altre icone flat.** Le ombreggiature per gli oggetti variano leggermente, a seconda di ciò che sembra migliore ed è più coerente all'interno del set di dimensioni e con le altre icone in Windows Vista. In alcuni casi può anche essere necessario modificare le ombreggiature. Ciò sarà particolarmente vero quando gli oggetti vengono disposti su altri oggetti.
-   **È possibile usare una gamma sottile di colori per ottenere il risultato desiderato.** Le ombreggiature aiutano gli oggetti a restare nello spazio. Il colore influisce sul peso percepito dell'ombreggiatura e può distorcere l'immagine se è troppo pesante.

![Screenshot della finestra di dialogo con ombreggiatura selezionata ](images/vis-icons-image11.png)![Screenshot dell'icona della carta con ombreggiatura stretta ](images/vis-icons-image12.png)

Opzione Ombreggiatura nella finestra di dialogo Stile livello e ombreggiatura tipica per un'icona piatta.

**Intervalli di ombreggiatura delle icone flat di base**



| Caratteristica                              | Intervallo                                                         |
|-------------------------------|----------------------------------------------------------|
| Color<br/>              | Nero<br/>                                         |
| Modalità di fusione<br/>         | Moltiplicazione<br/>                                      |
| Opacità<br/>            | 22-50%, a seconda del colore dell'elemento<br/> |
| Angle<br/>              | 120-130 (usare la luce globale)<br/>                    |
| Distanza<br/>           | 3 per 256x256, fino a 1 per 32x32<br/>    |
| Spread<br/>             | 0<br/>                                             |
| Dimensione<br/>               | 7 per 256x256, fino a 2 per 32x32<br/>    |



 

**Icone tridimensionali**

-   Creare ombreggiature per le icone 3D caso per caso, con uno sforzo per adattarsi a un intervallo di distanza di lancio e sfumature completamente trasparenti. Creare le immagini con dimensioni leggermente inferiori rispetto alle dimensioni complessive dell'icona per consentire lo spazio per un'ombreggiatura (per le dimensioni che ne richiederanno una). Assicurarsi che l'ombreggiatura non finisca improvvisamente sul bordo dell'icona.

![Illustrazione della creazione di ombreggiature in Photoshop](images/vis_icons_image13.jpeg)

![Illustrazione di quattro oggetti con ombreggiature variabili](images/vis_icons_image14.jpeg)

Questi esempi illustrano le variazioni create in base alla forma e alla posizione dell'oggetto stesso. L'ombreggiatura a volte deve essere sfumata o abbreviata per evitare che venga ritagliata dalle dimensioni della casella icona.

### <a name="color-and-saturation"></a>Colore e saturazione

-   **I colori sono in genere meno saturati rispetto Windows XP.**
-   **Usare le sfumature per creare un'immagine dall'aspetto più realistico.**
-   **Anche se non esiste una tavolozza dei colori specifica per le icone standard, tenere presente che devono funzionare bene insieme in molti contesti e temi.** Preferire il set standard di colori; non colorare nuovamente le icone standard, ad esempio le icone di avviso, perché ciò interrompe la capacità degli utenti di interpretare il significato. Per altre linee guida, vedere [Color](vis-color.md).
-   I file icona richiedono anche versioni del riquadro **a 8 e 4 bit per** supportare l'impostazione predefinita in un desktop remoto. Questi file possono essere creati tramite un processo batch, ma devono essere esaminati, in quanto alcuni richiedono un miglioramento della leggibilità.

    ![Screenshot della finestra di dialogo selezione colori ](images/vis-icons-image15.png)

    Non esiste alcuna restrizione della tavolozza dei colori. Viene evitata solo la saturazione completa (in alto a destra).

-   Livelli di bit: progettazione ICO per 32 bit (alfa incluso) + 8 bit + 4 bit (dithered down automaticamente pixel poke solo più critico). Deve essere inclusa solo una copia a 32 bit dell'immagine da 256 x 256 pixel e deve essere compressa solo l'immagine da 256 x 256 pixel per mantenere le dimensioni del file ridotte. Diversi strumenti icona offrono la compressione per Windows Vista.
-   Livelli di bit: barre degli strumenti a 24 bit + alfa (maschera a 1 bit), 8 bit e 4 bit.
-   Barre degli strumenti o file AVI: usare magenta (R255 G0 B255) come colore di trasparenza di sfondo.

### <a name="size-requirements"></a>Requisiti per le dimensioni

**Generale**

-   Prestare particolare attenzione alle icone a **visibilità elevata,** ad esempio le icone principali dell'applicazione, le icone dei file che possono essere visualizzate in esplora risorse Windows e le icone visualizzate nel menu Start o sul desktop.
    -   **Icone dell'applicazione ed Pannello di controllo elementi:** Il set completo include 16x16, 32x32, 48x48 e 256x256 (il codice è compreso tra 32 e 256). Il formato di file con estensione ico è obbligatorio. Per la modalità classica, il set completo è 16x16, 24x24, 32x32, 48x48 e 64x64.
    -   **Opzioni dell'icona dell'elemento elenco:** Usare anteprime o icone di file live del tipo di file (ad esempio, .doc); set completo.
    -   **Icone della barra degli strumenti:** 16x16, 24x24, 32x32. Si noti che le icone della barra degli strumenti sono sempre flat, non 3D, anche con dimensioni 32x32.
    -   **Icone della finestra di dialogo e della procedura guidata:** 32x32 e 48x48.
    -   **Sovrimpressione:** Codice della shell principale (ad esempio, un collegamento) 10x10 (per 16x16), 16x16 (per 32x32), 24x24 (per 48x48), 128x128 (per 256x256). Si noti che alcune sono leggermente più piccole, ma sono vicine a queste dimensioni, a seconda della forma e del bilanciamento ottico.
    -   **Avvio veloce'area:** Le icone verranno ridimensionate da 48x48 nelle sovrimpressione dinamiche ALT+TAB, ma per una versione più nitida aggiungere un file 40x40 al file con estensione ico.
    -   **Icone del fumetto:** 32x32 e 40x40.
    -   **Dimensioni aggiuntive:** Questi sono utili per avere a disposizione risorse per creare altri file (ad esempio annotazioni, barre degli strumenti, sovrapposizioni, dpi elevati e casi speciali): 128x128, 96x96, 64x64, 40x40, 24x24, 22x22, 14x14, 10x10 e 8x8. È possibile usare .ico, .png, .bmp o altri formati di file, a seconda del codice in quell'area.

**Per valori dpi elevati**

-   Windows Vista è destinato a 96 dpi e 120 dpi.

Le tabelle seguenti illustrano esempi di proporzioni di ridimensionamento applicate a due dimensioni comuni delle icone. Si noti che non tutte queste dimensioni devono essere incluse nel file con estensione ico. Il codice consente di ridimensionare quelli più grandi.



| dpi                   | Dimensioni icona                         | Fattore di scala                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 16x16<br/>         | 1.0 (100%)<br/>       |
| 120<br/>     | 20x20<br/>         | 1.25 (125%)<br/>      |
| 144<br/>     | 24x24<br/>         | 1.5 (150%)<br/>       |
| 192<br/>     | 32x32<br/>         | 2.0 (200%)<br/>       |



 



| dpi                   | Dimensioni icona                         | Fattore di scala                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 32x32<br/>         | 1.0 (100%)<br/>       |
| 120<br/>     | 40x40<br/>         | 1.25 (125%)<br/>      |
| 144<br/>     | 48x48<br/>         | 1.5 (150%)<br/>       |
| 192<br/>     | 64x64<br/>         | 2.0 (200%)<br/>       |



 

**Dimensioni dei file con estensione ico (standard)**

![Diagramma che mostra diverse icone del router di dimensioni standard.](images/vis-icons-image16.png)

**Dimensioni dei file con estensione ico (casi speciali)**

![Illustrazione di icone di router di dimensioni diverse ](images/vis-icons-image17.png)

**Annotazioni e sovrimpressione**

-   Le annotazioni vengono nell'angolo inferiore destro dell'icona e devono riempire il 25% dell'area dell'icona.
    -   **Eccezione:** le icone 16x16 accettano annotazioni 10x10.
-   Non usare più annotazioni su un'icona.
-   Le sovrimpressione si inseriscono nell'angolo inferiore sinistro dell'icona e devono riempire il 25% dell'area dell'icona.
    -   **Eccezione:** le icone 16x16 accettano sovrapposizioni 10x10.

### <a name="level-of-detail"></a>Livello di dettaglio

-   Le dimensioni 16x16 di molte di queste icone sono ancora ampiamente usate e quindi importanti.
-   I dettagli in un'icona di queste dimensioni devono mostrare chiaramente il punto chiave dell'icona.
-   Quando un'icona diventa più piccola, è consigliabile sacrificare la trasparenza e alcuni dettagli speciali presenti in dimensioni maggiori per semplificare e ottenere il punto.
-   Gli attributi e i colori devono essere esagerati e usati per evidenziare le forme chiave.

    ![Illustrazione di un dispositivo di grandi dimensioni e di due dispositivi di piccole dimensioni ](images/vis-icons-image18.png)

    A 16x16, l'icona per il dispositivo audio portatile potrebbe essere facilmente scambiata con un telefono cellulare, quindi l'orecchino è un dettaglio visivo chiave da visualizzare.

-   Il semplice ridimensionamento rispetto alle dimensioni 256x256 non funziona.
-   Tutte le dimensioni necessitano di un livello di dettaglio pertinente; più piccola è l'icona, più è necessario esagerare i dettagli di definizione.

    ![Illustrazione di telefoni cellulari con dettagli chiari ](images/vis-icons-image19.png)

    ![Illustrazione di telefoni cellulari con dettagli sfocati ](images/vis-icons-image20.png)

### <a name="icon-development"></a>Sviluppo di icone

**Progettazione e produzione di icone**

-   **Assumere un progettista grafico esperto.** Per una grafica, immagini e icone di grande qualità, è possibile collaborare con esperti. È consigliabile sperimentare le illustrazioni usando grafica vettoriale o programmi 3D.
-   **Pianificare una serie** di iterazioni, dagli sketch concettuali iniziali ai mock up nel contesto, alla revisione finale della produzione e all'adattamento e alla fine delle icone nel prodotto funzionante.
-   **La creazione di un'icona può essere costosa.** Raccogliere tutti i dettagli e i requisiti esistenti, ad esempio: il set completo di icone necessarie; la funzione main e il significato per ognuno; famiglie o cluster nel set che si desidera siano evidenti; requisiti del marchio; nomi di file esatti; formati di immagine usati nel codice; e requisiti di dimensioni. Assicurarsi di poter usare al meglio la finestra di progettazione.
-   **Tenere presente che la finestra di progettazione potrebbe non avere familiarità con il prodotto, quindi fornire informazioni funzionali, schermate e sezioni specifiche, in base alle esigenze.**
-   **Pianificare revisioni geopolitiche e legali in base alle esigenze.**
-   **Eseguire il mapping di un intervallo di tempo e comunicare regolarmente.**

**Dallo sketch concettuale al prodotto finale**

![illustrazione dello sviluppo di bozze di telefoni cellulari ](images/vis-icons-image21.png)

-   Creare bozze concettuali.
-   Provare il concetto in diverse dimensioni.
-   Eseguire il rendering in 3D, se necessario.
-   Testare le dimensioni in colori di sfondo diversi.
-   Valutare le icone nel contesto dell'interfaccia utente reale.
-   Produrre il file con estensione ico finale o altri formati di risorse grafiche.

**Strumenti**

-   **Matita e carta:** Concetti iniziali, elencati e delineati.
-   **3D Studio Max:** Eseguire il rendering di oggetti 3D in prospettiva.
-   **Adobe Adobe** Tracciare ed scorrere, mock-up nel contesto e finalizzare i dettagli.
-   **Adobe Illustrator/Macromedia Freehand:** Tracciare ed scorrere e finalizzare i dettagli.
-   **Gamani Gif Movie Gear:** Produrre un file con estensione ico (con compressione, se necessario).
-   **Axialis Icon Workshop:** Produrre un file con estensione ico (con compressione, se necessario).
-   Microsoft Visual Studio non supporta le icone Windows Vista (non è supportato il canale alfa o più di 256 colori).

**Produzione**

> [!TIP]
> Seguire questa procedura per creare un singolo file con estensione ico che contiene più dimensioni di immagine e profondità dei colori.

**Passaggio 1: Concettualizzare**

-   Usare concetti stabiliti laddove possibile, per garantire la coerenza dei significati per l'icona e la relativa pertinenza per altri usi.
-   Considerare come l'icona verrà visualizzata nel contesto dell'interfaccia utente e come potrebbe funzionare come parte di un set di icone.
-   Se si modifica un'icona esistente, valutare se è possibile ridurre la complessità.
-   Considerare l'impatto culturale della grafica. Evitare di usare lettere, parole, mani o visi nelle icone. Rappresentare le rappresentazioni di persone o utenti nel modo più generico possibile, se necessario.
-   Se si combinano più oggetti in una singola immagine in un'icona, valutare il modo in cui l'immagine verrà ridimensionata a dimensioni inferiori. Non usare più di tre oggetti in un'icona (due sono preferibili). Per le dimensioni 16x16, è consigliabile rimuovere oggetti o semplificare l'immagine per migliorare il riconoscimento.
-   Non usare il flag Windows nelle icone.

**Passaggio 2: Illustrare**

-   Per illustrare Windows icone in stile Aero, usa uno strumento vettoriale, ad esempio Macromedia Freehand o Adobe Illustrator. Usare la tavolozza e le caratteristiche di stile descritte in precedenza in questo articolo.
-   Illustrare l'immagine usando Freehand o Illustrator. Copiare e incollare le immagini vettoriali in Adobe Adobe.
-   Creare e usare un livello modello in Photoshop per assicurarsi che il lavoro sia eseguito all'interno di aree quadrate delle dimensioni regolamentate.
-   Creare le immagini con dimensioni leggermente inferiori rispetto alle dimensioni complessive richieste dall'icona per consentire lo spazio per un'ombreggiatura (per le dimensioni che ne richiedono una).
-   Posizionare le immagini nella parte inferiore dei quadrati, in modo che tutte le icone in una directory siano posizionate in modo coerente. Evitare di tagliare le ombreggiature.
-   Se si aggiunge un altro oggetto a un'immagine o a una serie, mantenere l'oggetto principale in una posizione fissa e posizionare le immagini di dimensioni più piccole in una posizione fissa, ad esempio in basso a sinistra o in alto a destra a seconda della distinzione tra maiuscole e minuscole.

**Passaggio 3: Creare le immagini a 24 bit**

-   Dopo aver incollato le dimensioni in Photoshop, verificare la leggibilità delle immagini, in particolare con dimensioni 16x16 e inferiori. Potrebbe essere necessario usare percentuali di colori per il pixel. Potrebbe essere necessaria anche la riduzione della trasparenza. È comune esagerare aspetti di dimensioni inferiori ed eliminare anche gli aspetti, per concentrarsi sul punto chiave.
-   Le icone a 8 bit verranno visualizzate in qualsiasi modalità colore inferiore a 32 bit e non avranno il canale alfa a 8 bit, quindi potrebbe essere necessario che i bordi siano o più puliti perché non è presente alcun anti-aliasing (i bordi potrebbero essere frastagliati e l'immagine potrebbe essere difficile da leggere).
-   In Photoshop duplicare il livello immagine a 24 bit e rinominare il livello in immagini a 4 bit. Indicizzare le immagini a 4 bit nella Windows a 16 colori.
-   Pulire le immagini usando solo i colori della tavolozza dei 16 colori. I contorni delle versioni più scura o più chiara dei colori dell'oggetto sono in genere preferibili al grigio o al nero.
-   Se si lavora su una bitmap, assicurarsi che il colore di sfondo non sia usato nell'immagine stessa, perché il colore che sarà il colore trasparente. Magenta (R255 G0 B255) viene spesso usato come colore di trasparenza dello sfondo.

**Passaggio 4: Creare le immagini a 8 bit e a 4 bit**

-   Ora che le immagini a 24 bit sono pronte per essere trasformate in icone a 32 bit, è necessario creare versioni a 8 bit.
-   Questo è il momento ideale per testare schermate contestuali. È straordinario ciò che può essere individuato visualizzando altre icone o una famiglia di icone nel contesto. Questo passaggio consente di risparmiare tempo e denaro. È molto meglio rilevare i problemi prima che i file passano nell'ambiente di produzione e siano consegnati.
-   Aggiungere l'ombreggiatura alle immagini in dimensioni che le richiedono.
-   Unire l'ombreggiatura e le immagini a 24 bit.
-   Creare un nuovo file Dir per ogni dimensione. Copiare e incollare l'immagine appropriata. Salvare ogni file come file .psd file.
-   Non unire il livello immagine con il livello di sfondo. È utile includere le dimensioni e la profondità del colore nel nome del file mentre si lavora, ma potrebbe essere necessario rinominare il file.

**Passaggio 5: Creare il file con estensione ico**

-   Scegliere l'applicazione che meglio soddisfa le esigenze e le competenze degli artista. Tenere presente che le icone da usare in un prodotto di spedizione devono essere create in uno strumento acquistato o concesso in licenza. Ciò significa che non è possibile usare le versioni di valutazione.
-   Entrambi i prodotti elencati di seguito sono stati usati dai progettisti che hanno prodotto icone per Windows Vista e ognuno offre la possibilità di esportare in Adobe Adobe Cs.
    -   Gamani Gif Movie Gear: Produce file con estensione ico
    -   Axialis Icon Workshop: Produce file con estensione ico
-   Visual Studio non supporta le icone Windows Vista (non è disponibile alcun supporto per il canale alfa o più di 256 colori), quindi non è consigliabile usarle.
-   I file di icona (formato ICO) devono contenere le versioni a 4 e 8 bit, nonché la versione a 24 bit + alfa.
-   Salvare i file come "icona Windows (.ico)" indipendentemente dal programma di creazione dell'icona che si sceglie di usare.
-   Alcuni asset iconografici possono essere in realtà strisce di bitmap, che richiedono anche un canale alfa (ad esempio, per le barre degli strumenti) o file .png salvati con trasparenza. Non tutti sono necessariamente in formato .ico. Verificare il formato supportato nel codice.

**Passaggio 6: Valutare**

-   Esaminare tutte le dimensioni.
-   Esaminare la famiglia per valutare la somiglianza della famiglia, l'equilibrio ottico e la distinzione.
-   Esaminare nel contesto per valutare i pesi relativi e la visibilità (assicurarsi che non ne sia dominata una).
-   Si considerino i casi che potrebbero non essere usati ora, ma che potrebbero essere nel prossimo futuro. È possibile annotare questa icona o avere una sovrimpressione?
-   Esaminare nel codice.

### <a name="icons-in-the-context-of-list-views-toolbars-and-tree-views"></a>Icone nel contesto di visualizzazioni elenco, barre degli strumenti e visualizzazioni albero

**Visualizzazioni elenco**

-   Per Windows Vista, usare le anteprime per i file che hanno contenuto visivamente distinto su scala ridotta, in modo che gli utenti possano riconoscere direttamente il file che stanno cercando. A tale scopo, Windows'interfaccia di programmazione dell'applicazione thumbnailing.

    ![Screenshot di Esplora risorse con le icone delle cartelle ](images/vis-icons-image22.png)

-   Le sovrimpressione dell'icona dell'applicazione (non mostrate qui) nelle anteprime consentono l'associazione con l'applicazione per il tipo di file, oltre a mostrare l'anteprima del file.

**Nota:** Per i file senza contenuto visivamente distinto, non usare anteprime. Usare invece icone di file simbolici tradizionali che mostrano la rappresentazione dell'oggetto e l'applicazione o il tipo associato.

**Barre degli strumenti**

-   Le icone visualizzate in una barra degli strumenti devono avere un equilibrio ottico per dimensioni, colore e complessità.
-   Testare le icone potenziali in una schermata contestuale per evitare dominanze o sbilanciamenti indesiderati.
-   Il test nelle schermate consente di evitare iterazioni costose nel codice.
-   Esaminare anche le icone nel codice. Il movimento e altri fattori possono influire sul successo di un'icona; in alcuni casi potrebbero essere necessarie altre iterazioni.

![Screenshot della barra degli strumenti con icone ed etichette piccole ](images/vis-icons-image23.png)

Nell'esempio precedente il bilanciamento ottico non è ancora stato raggiunto.

![Illustrazione di icone su sfondi diversi ](images/vis-icons-image24.png)

Provare le iterazioni nel contesto.

**Visualizzazioni albero**

-   Il bilanciamento ottico è necessario per mantenere la gerarchia in un controllo visualizzazione albero.
-   Di conseguenza, le icone usate in genere in questo contesto devono essere valutate in tale contesto. A volte una particolare icona 16x16 deve essere ridotta perché la sua forma ha una dominanza ottica rispetto ad altre.
-   La compensazione degli squilibri ottici è una parte importante della produzione di icone di qualità superiore.

![Figura di due set di cartelle nella visualizzazione albero ](images/vis-icons-image25.png)

 

