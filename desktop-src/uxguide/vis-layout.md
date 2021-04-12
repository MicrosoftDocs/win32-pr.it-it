---
title: Layout
description: Il layout è il ridimensionamento, la spaziatura e il posizionamento del contenuto all'interno di una finestra o di una pagina.
ms.assetid: 39cd896f-d3cc-4768-a20c-a7f598da7136
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f6b33375cbb679cc7c7efdeb12e5cd30be6280c5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104234449"
---
# <a name="layout"></a>Layout

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Il layout è il ridimensionamento, la spaziatura e il posizionamento del contenuto all'interno di una finestra o di una pagina. Un layout efficace è essenziale per aiutare gli utenti a trovare ciò che cercano rapidamente, oltre a rendere l'aspetto visivamente accattivante. Un layout efficace può fare la differenza tra le progettazioni che gli utenti comprendono immediatamente e quelle che lasciano gli utenti a stupirsi e sopraffare.

**Nota:** Le linee guida correlate alla [gestione delle finestre](win-window-mgt.md) sono presentate in un articolo separato. Il dimensionamento e la spaziatura dei controlli specifici sono presentati nei rispettivi articoli delle linee guida.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="visual-hierarchy"></a>Gerarchia visiva

Una finestra o una pagina dispone di una gerarchia visiva chiara quando l'aspetto indica la relazione e la priorità dei relativi elementi. Senza una gerarchia visiva, gli utenti devono individuare tali relazioni e priorità.

La gerarchia visiva viene eseguita combinando con sapientemente gli attributi seguenti:

-   **Lo stato attivo.** Il layout indica il punto in cui gli utenti devono eseguire prima la ricerca.
-   **Flusso.** L'occhio scorre senza problemi e naturalmente da un tracciato chiaro attraverso la superficie, individuando gli elementi dell'interfaccia utente nell'ordine appropriato per l'utilizzo.
-   **Raggruppamento.** Gli elementi dell'interfaccia utente correlati logicamente hanno una relazione visiva chiara. Gli elementi correlati sono raggruppati. gli elementi non correlati sono separati.
-   **Enfasi.** Gli elementi dell'interfaccia utente vengono evidenziati in base alla relativa importanza relativa.
-   **Allineamento.** Gli elementi dell'interfaccia utente hanno un posizionamento coordinato, quindi sono facili da analizzare e apparire ordinati.

Inoltre, il layout effettivo presenta questi attributi:

-   **Indipendenza del dispositivo.** Il layout viene visualizzato come previsto, indipendentemente dal carattere tipografico o dalle dimensioni, da punti per pollice (dpi), da visualizzazione o da adattatore grafico.
-   **Facile da analizzare.** Gli utenti possono trovare il contenuto che cerca a colpo d'occhio.
-   **Efficienza.** Gli elementi dell'interfaccia utente di grandi dimensioni devono essere di grandi dimensioni e gli elementi piccoli sono molto piccoli.
-   **Resizability.** Se utile, una finestra è ridimensionabile e il layout del contenuto è efficace indipendentemente dalla dimensione o dalla dimensione della superficie.
-   **Bilanciare.** Il contenuto viene distribuito uniformemente in tutta la superficie.
-   **Semplicità visiva.** La percezione che un layout non sia più complicato del necessario. Gli utenti non si sentono sopraffatti dall'aspetto del layout.
-   **Coerenza.** Finestre o pagine simili utilizzano un layout simile, in modo che gli utenti si trovino sempre orientati.

Sebbene il ridimensionamento, la spaziatura e la selezione host siano concetti semplici, la sfida con il layout consiste nel raggiungere il giusto miscuglio di questi attributi.

In Windows il layout viene comunicato usando le metriche indipendenti dal dispositivo, ad esempio le unità di dialogo (DLU) e i pixel relativi.

### <a name="a-design-model-for-reading"></a>Modello di progettazione per la lettura

**Gli utenti scelgono gli elementi letti dall'aspetto e dall'organizzazione del contenuto.** Per creare un layout efficace, è necessario comprendere quali utenti tendono a leggere e perché.

È possibile prendere decisioni di layout utilizzando questo modello di progettazione per la lettura:

-   Le persone leggono in un ordine da sinistra a destra, dall'alto verso il basso (nelle impostazioni cultura occidentali).
-   Sono disponibili due modalità di lettura: lettura e analisi immersive. L'obiettivo della lettura immersiva è la comprensione.

    ![Figura della freccia rossa nel modello di lettura zigzag ](images/vis-layout-image1.png)

    Questo diagramma modella la lettura immersiva.

    Al contrario, l'obiettivo dell'analisi è individuare gli elementi. Il percorso di analisi generale è simile al seguente:

    ![Figura della freccia rossa nel modello di lettura diagonale ](images/vis-layout-image2.png)

    Questo diagramma modella l'analisi.

    ![Figura della freccia rossa in un motivo di inattività e di arco ](images/vis-layout-image3.png)

    Se è presente un testo in esecuzione lungo il bordo sinistro di una pagina, gli utenti analizzano prima il bordo sinistro.

-   Quando si usa il software, gli utenti non sono immersi nell'interfaccia utente, ma nel lavoro. Di conseguenza, gli utenti in genere non leggono il testo dell'interfaccia utente che li analizzano. Leggono quindi i bit di testo in modo completo solo quando si ritengono necessari.
-   Gli utenti tendono a ignorare i riquadri di navigazione sul lato sinistro o destro di una pagina. Gli utenti riconoscono che sono presenti, ma esaminano i riquadri di spostamento solo quando vogliono spostarsi.
-   Gli utenti tendono a ignorare i grandi blocchi di testo non formattato senza leggerli affatto.

    ![Figura del testo con frecce che mostrano il testo di analisi ](images/vis-layout-image4.png)

    Gli utenti tendono a ignorare i grandi blocchi di testo e i riquadri di spostamento durante l'analisi.

-   Tutti gli elementi sono uguali, gli utenti esaminano prima di tutto l'angolo superiore sinistro di una finestra, eseguono l'analisi nella pagina e terminano l'analisi nell'angolo inferiore destro. Tendono a ignorare l'angolo in basso a sinistra.

    ![Figura di pagina e in alto a sinistra nella freccia in basso a destra ](images/vis-layout-image5.png)

    Tutti gli elementi sono uguali. i numeri vengono letti nell'ordine seguente: 1, 2, 4 e 3.

-   Tuttavia, nell'interfaccia utente interattiva, non tutti gli elementi sono uguali, in modo che gli elementi dell'interfaccia utente diversi ricevano diversi livelli di attenzione. Gli utenti tendono a esaminare i controlli interattivi in particolare i controlli in alto a sinistra e al centro della finestra e il primo testo prominente.

![Figura della schermata con testo nitido e sfocato ](images/vis-layout-image6.png)

Gli utenti si concentrano sui principali controlli interattivi e sull'informativa principale principale ed esaminano altri aspetti solo quando sono necessari.

-   Gli utenti tendono a leggere le etichette di controllo interattive, in particolare quelle che risultano rilevanti per il completamento dell'attività. Al contrario, gli utenti tendono a leggere testo statico solo quando ne pensano che debbano.
-   Gli elementi che appaiono diversi attirano l'attenzione. Il testo in grassetto e il testo di grandi dimensioni si differenziano dal testo normale. Gli elementi dell'interfaccia utente con colore o sfondo colorato si distinguono. Gli elementi con icone si distinguono da elementi senza icone.
-   Gli utenti non scorrono a meno che non dispongano di un motivo per. Se il contenuto [sopra la](glossary.md) sezione non fornisce un motivo per scorrere, non verrà eseguito.
-   Una volta che gli utenti hanno deciso cosa fare, interrompono immediatamente l'analisi e lo eseguono.
-   Poiché gli utenti interrompono l'analisi quando ritengono che vengano eseguiti, tendono a ignorare qualsiasi elemento oltre quello che sembra essere il punto di completamento.

![screenshot delle opzioni della tastiera ](images/vis-layout-image7.png)

Gli utenti interrompono l'analisi quando ritengono che siano state eseguite.

Naturalmente, vi saranno eccezioni a questo modello generale. I dispositivi di rilevamento degli occhi indicano che il comportamento degli utenti reali è piuttosto irregolare. Lo scopo di questo modello è aiutare a prendere decisioni e compromessi efficaci, non a modellare il comportamento degli utenti in modo accurato. Tuttavia, come hai letto questo elenco, speriamo che tu abbia riconosciuto anche molti dei tuoi modelli di lettura.

### <a name="designing-for-scanning"></a>Progettazione per l'analisi

**Gli utenti non leggono, analizzano quindi è necessario progettare superfici dell'interfaccia utente per l'analisi.** Non presupporre che gli utenti leggano il testo come scritto in un ordine da sinistra a destra e dall'alto verso il basso, ma piuttosto che esaminano gli elementi dell'interfaccia utente che attraggono la loro attenzione.

Per progettare per l'analisi:

-   Si supponga che gli utenti inizino analizzando rapidamente l'intera finestra, quindi leggendo gli elementi dell'interfaccia utente approssimativamente nell'ordine seguente:
    -   Controlli interattivi al centro
    -   Pulsanti commit
    -   Controlli interattivi trovati altrove
    -   Istruzione principale
    -   Spiegazioni aggiuntive
    -   Testo visualizzato con un'icona di avviso
    -   Titolo della finestra
    -   Altro testo statico nel corpo principale
    -   Note a piè di pagina
-   Posizionare gli elementi dell'interfaccia utente che avviano un'attività nell'angolo superiore sinistro o nel centro superiore.
-   Posizionare gli elementi dell'interfaccia utente che completano un'attività nell'angolo inferiore destro.
-   Laddove possibile, inserire testo cruciale sui controlli interattivi anziché sul testo statico.
-   Evitare di inserire informazioni cruciali nell'angolo inferiore sinistro o nella parte inferiore di una pagina o di un controllo scorrevole lungo.
-   Non presentare grandi blocchi di testo. Eliminare il testo non necessario. Utilizzare lo stile di presentazione della [piramide invertita](text-ui.md) .
-   Per attirare l'attenzione degli utenti, assicurarsi che sia garantita l'attenzione.

Quando possibile, usare questo modello anziché combatterlo; in alcuni casi, tuttavia, sarà necessario enfatizzare o deaccentuare particolari elementi dell'interfaccia utente.

Per evidenziare gli elementi primari dell'interfaccia utente:

-   Inserire gli elementi primari dell'interfaccia utente nel [percorso di analisi](glossary.md).
-   Inserire un'interfaccia utente per avviare un'attività nell'angolo superiore sinistro o nel centro superiore.
-   Inserire i pulsanti commit nell'angolo in basso a destra.
-   Inserire l'interfaccia utente primaria rimanente al centro.
-   Usare i controlli che attirano l'attenzione, ad esempio pulsanti di comando, collegamenti di comando e icone.
-   Utilizzare testo prominente, inclusi testo di grandi dimensioni e testo in grassetto.
-   Gli utenti con testo Put devono leggere i controlli interattivi o con icone o [banner](vis-graphic.md).
-   Usare testo scuro su uno sfondo chiaro.
-   Racchiudere gli elementi con spazio generoso.
-   Non richiedere alcuna interazione, ad esempio puntando o posizionando il puntatore del mouse, per visualizzare l'elemento sottolineato.

    ![screenshot delle opzioni di attivazione di Windows ](images/vis-layout-image8.png)

    Questo esempio illustra molti modi per evidenziare gli elementi primari dell'interfaccia utente.

Per deaccentuare gli elementi secondari dell'interfaccia utente:

-   Inserire gli elementi dell'interfaccia utente secondaria all'esterno del percorso di analisi.
-   Inserire in genere gli utenti non devono essere visualizzati nell'angolo in basso a sinistra o in basso nella finestra.
-   Usare i controlli che non attraggono l'attenzione, ad esempio i collegamenti alle attività invece dei pulsanti di comando.
-   Utilizzare testo normale o grigio.
-   Usare il testo chiaro sullo sfondo scuro. Il testo bianco su uno sfondo grigio scuro o blu funziona correttamente.
-   Racchiudere gli elementi con spazio minimo.
-   Provare a usare la [divulgazione progressiva](ctrl-progressive-disclosure-controls.md) per nascondere gli elementi dell'interfaccia utente secondaria.

    ![Screenshot di elementi di interfaccia grandi e piccoli ](images/vis-layout-image9.png)

    Questo esempio illustra molti modi per delineare gli elementi dell'interfaccia utente secondaria.

### <a name="using-screen-space-effectively"></a>Utilizzo efficace dello spazio dello schermo

L'uso dello spazio dello schermo richiede di bilanciare diversi fattori: usare una quantità eccessiva di spazio e una finestra si presenta in modo intensivo e dispendioso e persino difficile da usare in base alla [legge Fitts](inter-mouse.md).

**Non corretto:**

![screenshot che mostra una quantità eccessiva di spazio vuoto ](images/vis-layout-image10.png)

In questo esempio, la finestra è troppo grande per il relativo contenuto.

D'altra parte, usare uno spazio troppo piccolo e una finestra si trova in difficoltà, scomodo e intimidatorio, ed è difficile da usare se è necessario lo scorrimento e altre modifiche da usare.

**Non corretto:**

![screenshot con troppi controlli ](images/vis-layout-image11.png)

In questo esempio, la finestra è troppo piccola per il contenuto.

Mentre l'interfaccia utente critica deve adattarsi alla [risoluzione effettiva](glossary.md)minima supportata, non presupporre che l'uso di uno spazio dello schermo significa che Windows dovrebbe essere il più piccolo possibile. **Il layout efficace è relativo allo spazio aperto e non tenta di stipare tutto nello spazio più piccolo possibile.** Gli schermi moderni hanno uno spazio dello schermo significativo ed è opportuno usare questo spazio in modo efficace quando possibile. Di conseguenza, err sul lato dell'utilizzo di una quantità eccessiva di spazio sullo schermo anziché troppo piccola. In questo modo, le finestre si sentono più chiare e più accessibili.

Si sa che un layout sta usando lo spazio dello schermo in modo efficace nei casi seguenti:

-   Windows, i riquadri della finestra e i controlli non devono essere ridimensionati per poter essere usati. Se la prima operazione eseguita dagli utenti è il ridimensionamento di una finestra, di un riquadro o di un controllo, le dimensioni non sono corrette.
-   I dati non vengono troncati. La maggior parte dei dati nelle visualizzazioni elenco e nelle visualizzazioni ad albero non contiene ellissi e i dati in altri controlli non vengono ritagliati, a meno che la lunghezza dei dati non sia insolitamente grande. I dati che devono essere letti per eseguire un'attività non devono essere troncati.
-   Le finestre e i controlli vengono ridimensionati in modo appropriato per eliminare lo scorrimento non necessario. Sono presenti poche barre di scorrimento orizzontali e nessuna barra di scorrimento verticale non necessaria.
-   I controlli utilizzano per lo più le dimensioni standard. Si tenta di ridurre il numero di dimensioni del controllo, ad esempio usando solo una o due larghezze dei pulsanti di comando in una superficie.
-   La superficie dell'interfaccia utente è bilanciata. Non sono presenti aree dello schermo inutilizzate di grandi dimensioni.

Scegliere le dimensioni della finestra sufficientemente grandi da soddisfare le proprie esigenze. Se la finestra è ridimensionabile, questo obiettivo si applica alle dimensioni predefinite. **Una combinazione di dati troncati o barre di scorrimento e una grande quantità di spazio disponibile sullo schermo è un segno chiaro del layout inefficace.**

### <a name="control-sizing"></a>Ridimensionamento del controllo

Il primo passaggio nell'uso dello spazio dello schermo è in genere quello di determinare le dimensioni corrette per i vari elementi dell'interfaccia utente. Vedere la [tabella di dimensionamento del controllo](#recommended-sizing-and-spacing) e il dimensionamento consigliato negli articoli specifici della linea guida del controllo.

Fitts ' Law indica che la destinazione più piccola è, maggiore è il tempo necessario per acquisirla con il mouse. Inoltre, per i computer che utilizzano la tecnologia Windows Tablet and touch, il "mouse" potrebbe essere effettivamente una penna o il dito dell'utente, pertanto è consigliabile prendere in considerazione i dispositivi di input alternativi per determinare le dimensioni per i controlli di piccole dimensioni. **Una dimensione del controllo dei pixel relativi di 16x16 è una dimensione minima corretta per qualsiasi dispositivo di input.** Al contrario, i pulsanti di controllo di selezione del pixel relativi di 15x9 standard sono troppo piccoli per essere usati in modo efficace dalle penne.

### <a name="spacing"></a>Spaziatura

La fornitura di spazio generoso (ma non eccessivo) rende il layout più comodo e più semplice da analizzare. Lo spazio effettivo non è uno spazio inutilizzato, ma svolge un ruolo importante nel miglioramento della capacità di analisi da parte degli utenti e aggiunge anche a un appeal visivo della progettazione. Per le linee guida, fare riferimento alla [tabella spaziatura](#recommended-sizing-and-spacing).

Per i computer che utilizzano la tecnologia Windows Tablet e touch, il "mouse" potrebbe essere effettivamente una penna o il dito dell'utente. Il targeting è più difficile quando si usa una penna o un dito come dispositivo di puntamento, in modo che gli utenti tocchino al di fuori della destinazione prevista. Quando i controlli interattivi vengono posizionati molto vicino ma non vengono effettivamente toccati, gli utenti possono fare clic sullo spazio inattivo tra i controlli. Poiché facendo clic su spazio inattivo non sono presenti risultati o commenti visivi, gli utenti spesso non sono sicuri di ciò che si è verificato. Se i controlli piccoli sono spaziati troppo attentamente, l'utente deve toccare con precisione per evitare di toccare l'oggetto errato. **Per risolvere questi problemi, le aree di destinazione dei controlli interattivi devono essere toccate o avere almeno 3 DLU (5 pixel relativi) di spazio tra di essi.**

Si sa che un layout presenta una spaziatura corretta nei casi seguenti:

-   In generale, l'area dell'interfaccia utente si sente a proprio agio e non ha un crampo.
-   Lo spazio viene visualizzato uniforme e bilanciato.
-   Gli elementi correlati sono vicini e gli elementi non correlati sono relativamente lontani.
-   Non esiste alcuno spazio inattivo tra i controlli che devono essere insieme, ad esempio i pulsanti della barra degli strumenti.

### <a name="resizable-windows"></a>Finestre ridimensionabili

Le finestre ridimensionabili sono anche un fattore essenziale per l'uso efficace dello spazio dello schermo. Alcune finestre sono costituite da contenuto fisso e non possono trarre vantaggio dal ridimensionamento, ma Windows con contenuto ridimensionabile dovrebbe essere ridimensionabile. Naturalmente, il motivo per cui gli utenti ridimensionano una finestra consiste nell'assumere lo spazio dello schermo aggiuntivo, in modo che il contenuto venga espanso di conseguenza assegnando più spazio agli elementi dell'interfaccia utente che lo richiedono. Windows con contenuto dinamico, documenti, immagini, elenchi e alberi è più vantaggioso dalle finestre ridimensionabili.

![screenshot del controllo ridimensionato recupero della barra di scorrimento ](images/vis-layout-image12.png)

In questo esempio, il ridimensionamento della finestra Ridimensiona il controllo di visualizzazione elenco.

Ciò premesso, Windows può essere esteso troppo a lungo. Molte pagine del pannello di controllo, ad esempio, diventano ingombranti quando il contenuto è più grande di 600 pixel relativi. In questo caso, è preferibile non ridimensionare l'area del contenuto oltre questa larghezza massima o modificare l'origine del contenuto quando la finestra viene ridimensionata in modo più grande. Al contrario, Mantieni una larghezza massima e un'origine superiore sinistra fissa.

Il testo diventa difficile da leggere man mano che aumenta la lunghezza della riga. Per i documenti di testo, prendere in considerazione la lunghezza massima della riga di 80 caratteri per facilitare la lettura del testo. I caratteri includono lettere, punteggiatura e spazi.

**Non corretto:**

![screenshot della finestra di messaggio estesa con testo lungo ](images/vis-layout-image13.png)

In questo esempio, la lunga lunghezza del testo rende difficile la lettura.

Infine, le finestre ridimensionabili devono anche usare lo spazio dello schermo in modo efficace quando sono rese più piccole, semplificando il contenuto ridimensionabile e rimuovendo lo spazio dagli elementi dell'interfaccia utente che possono funzionare in modo efficace senza di esso. A un certo punto, la finestra o i relativi elementi dell'interfaccia utente diventano troppo piccoli per essere utilizzabili, pertanto è necessario assegnare una dimensione minima oppure alcuni elementi devono essere rimossi completamente.

![screenshot della finestra con barra multifunzione alta e intrusiva ](images/vis-layout-image14.png)

![screenshot della finestra senza barra multifunzione ](images/vis-layout-image15.png)

In questo esempio il riquadro ha una dimensione minima.

Alcuni programmi traggono vantaggio dall'utilizzo di una presentazione completamente diversa per rendere il contenuto utilizzabile a dimensioni inferiori.

![screenshot dei pulsanti del lettore multimediale centrato ](images/vis-layout-image16.png)

In questo esempio, Windows Media Player modifica il formato quando la finestra diventa troppo piccola per il formato standard.

### <a name="focus"></a>Focus

Un layout ha lo stato attivo quando è presente una posizione ovvia da esaminare per prima. Lo stato attivo è importante per mostrare agli utenti dove iniziare a eseguire l'analisi della finestra o della pagina. Senza chiarire l'attenzione, l'occhio dell'utente si aggira senza alcuna necessità. Il punto focale dovrebbe essere qualcosa di importante che gli utenti debbano trovare e comprendere rapidamente e dovrebbero avere la massima enfasi visiva. L'angolo superiore sinistro è il punto focale naturale per la maggior parte delle finestre.

Deve essere presente un solo punto focale. Proprio come nel mondo reale, l'occhio può concentrarsi solo su una cosa alla volta, mentre gli utenti non possono concentrarsi su più posizioni contemporaneamente.

Per rendere un elemento dell'interfaccia utente il punto focale, è possibile dargli enfasi visiva:

-   Inserendolo nella parte superiore sinistra o in alto al centro della superficie.
-   Uso di controlli interattivi che sono importanti e facilmente comprensibili.
-   Utilizzando un testo prominente, ad esempio un'istruzione principale.
-   Assegnazione dei controlli alla selezione predefinita e allo stato attivo per l'input iniziale.
-   Posizionamento dei controlli in uno sfondo colorato diverso.

Si consideri Windows Search. Il punto focale per la ricerca di Windows deve essere la casella di ricerca perché è il punto di partenza per l'attività. Tuttavia, si trova nell'angolo in alto a destra per essere coerente con il posizionamento della casella di ricerca standard. La casella di ricerca ha lo stato attivo per l'input, ma in base alla relativa posizione nel percorso di analisi, questo solo indizio non è sufficiente.

Per risolvere questo problema, nella parte superiore centrale della finestra sono presenti istruzioni prominenti per indirizzare gli utenti alla posizione corretta.

**Accettabile:**

![screenshot della finestra di dialogo di ricerca con testo utile ](images/vis-layout-image17.png)

In questo esempio, un'istruzione prominente nella parte superiore centrale della finestra indirizza gli utenti alla casella di ricerca.

Senza le istruzioni, la finestra non avrà un punto focale evidente.

**Non corretto:**

![screenshot della finestra di dialogo di ricerca senza testo ](images/vis-layout-image18.png)

Questo esempio non ha un punto focale evidente. Gli utenti non sanno dove cercare.

Se si assegna un'enfasi visiva all'elemento dell'interfaccia utente, assicurarsi che l'attenzione sia garantita. Nell'esempio precedente di Windows Search errato, il pulsante evidenziato tutti si trova nell'angolo in alto a sinistra e presenta la maggiore enfasi visiva, ma non è il punto focale previsto. Gli utenti potrebbero rimanere bloccati guardando questo pulsante cercando di capire cosa fare.

**Non corretto:**

![cattura di schermata del pulsante tutti evidenziato ](images/vis-layout-image19.png)

Senza l'istruzione prominente come punto focale, il pulsante evidenziato All è un punto focale non intenzionale.

### <a name="flow"></a>Flusso

Un layout ha un flusso quando gli utenti vengono guidati in modo semplice e naturale da un tracciato chiaro attraverso la relativa superficie, individuando gli elementi dell'interfaccia utente nell'ordine appropriato per l'utilizzo. Dopo che gli utenti hanno identificato il punto focale, devono determinare come completare l'attività. La posizione degli elementi dell'interfaccia utente comunica la relazione ed è necessario eseguire il mirroring dei passaggi necessari per eseguire l'attività. In genere, ciò significa che i passaggi dell'attività devono essere propagati naturalmente in un ordine da sinistra a destra, dall'alto verso il basso (nelle impostazioni cultura occidentali).

Si sa che un layout ha un flusso valido nei casi seguenti:

-   La posizione degli elementi dell'interfaccia utente rispecchia i passaggi necessari agli utenti per eseguire l'attività.
-   Gli elementi dell'interfaccia utente che avviano un'attività si trovano nell'angolo superiore sinistro o nel centro superiore.
-   Gli elementi dell'interfaccia utente che completano un'attività si trovano nell'angolo inferiore destro.
-   Gli elementi dell'interfaccia utente correlati sono insieme; gli elementi non correlati sono separati.
-   I passaggi necessari sono nel flusso principale.
-   I passaggi facoltativi sono esterni al flusso principale, probabilmente deaccentuati usando uno sfondo adatto o una divulgazione progressiva.
-   Gli elementi utilizzati di frequente vengono visualizzati prima degli elementi utilizzati di frequente nel percorso di analisi.
-   Gli utenti conoscono sempre le operazioni da eseguire successivamente. Non ci sono salti o interruzioni impreviste nel flusso attività.

**Non corretto:**

![screenshot del layout della finestra di dialogo confusa ](images/vis-layout-image20.png)

In questo esempio, gli utenti non sanno cosa fare successivamente. Il flusso attività contiene salti e interruzioni impreviste.

**Corretto:**

![Screenshot di una finestra di dialogo ben pianificata ](images/vis-layout-image21.png)

In questo esempio, la presentazione degli elementi dell'interfaccia utente rispecchia i passaggi necessari per eseguire l'attività.

### <a name="grouping"></a>Raggruppamento

Un layout dispone di raggruppamento quando gli elementi dell'interfaccia utente correlati logicamente hanno una relazione visiva chiara. I gruppi sono importanti perché è più facile per gli utenti comprendere e concentrarsi su un gruppo di elementi correlati rispetto agli elementi singolarmente. I gruppi rendono un layout più semplice e più semplice da analizzare.

È possibile visualizzare il raggruppamento nei modi seguenti (in aumento della pesantezza):

-   **Layout.** È possibile raggruppare i controlli correlati uno accanto all'altro e inserire spazi aggiuntivi tra i controlli non correlati.

    ![Figura di quattro icone che mostrano quattro gruppi di attività ](images/vis-layout-image22.png)

    In questo esempio, viene usato solo il layout per visualizzare le relazioni di controllo.

-   **Separatori.** Un separatore è una linea orizzontale o verticale che unifica un gruppo di controlli. I separatori forniscono un aspetto più semplice e pulito. Tuttavia, a differenza delle caselle di gruppo, funzionano meglio quando si estendono sulla superficie intera.

    ![Screenshot di tre icone e tre separatori ](images/vis-layout-image23.png)

    In questo esempio, i separatori con etichetta vengono utilizzati per visualizzare le relazioni tra i controlli.

-   **Aggregatori.** Un aggregatore è un elemento grafico che crea una relazione visiva tra i controlli fortemente correlati.

    ![screenshot dei controlli all'interno di una linea ellittica ](images/vis-layout-image24.png)

    In questo esempio viene usato un aggregatore di limiti per evidenziare la relazione tra i controlli e fare in modo che sembri un singolo controllo anziché otto.

-   **Caselle di gruppo.** Una casella di gruppo è una cornice rettangolare con etichetta che racchiude un set di controlli correlati.

    ![Screenshot di caselle di controllo in un bordo rettangolare ](images/vis-layout-image25.png)

    In questo esempio, una casella di gruppo racchiude ed etichetta un set di controlli correlati.

-   **Sfondi.** È possibile usare gli sfondi per enfatizzare o deaccentuare tipi diversi di contenuto.

    ![screenshot del lato sinistro del pannello di controllo ](images/vis-layout-image26.png)

    In questo esempio, il riquadro attività del pannello di controllo viene utilizzato per raggruppare le attività correlate e gli elementi del pannello di controllo.

    Per evitare confusione visiva, il raggruppamento più chiaro che esegue il processo è la scelta migliore. Per altre informazioni, vedere [caselle di gruppo](ctrl-group-boxes.md), [tabulazioni](ctrl-tabs.md), [separatori e sfondi](vis-graphic.md).

Indipendentemente dallo stile di raggruppamento, è possibile usare il rientro per mostrare la relazione dei controlli all'interno di un gruppo. I controlli che sono peer tra loro devono essere allineati a sinistra e i controlli dipendenti vengono rientrati 12 dlu o 18 pixel relativi.

![Screenshot di tre livelli di controlli rientrati ](images/vis-layout-image27.png)

I controlli dipendenti vengono rientrati 12 dlu o 18 pixel relativi, che in base alla progettazione è la distanza tra le caselle di controllo e i pulsanti di opzione dalle etichette.

Si sa che un layout dispone di un raggruppamento valido nei casi seguenti:

-   La finestra o le pagine hanno al massimo 7 gruppi.
-   Lo scopo di ogni gruppo è ovvio.
-   La relazione dei controlli all'interno di ogni gruppo è ovvia, in particolare la dipendenza del controllo.
-   Il raggruppamento semplifica il contenuto anziché renderlo più complesso.

### <a name="alignment"></a>Allineamento

L'allineamento è il posizionamento coordinato degli elementi dell'interfaccia utente. L'allineamento è importante perché rende più semplice l'analisi dei contenuti e influiscono sulla percezione della complessità visiva degli utenti.

Esistono diversi obiettivi da considerare quando si determina l'allineamento:

-   **Facilità di analisi orizzontale.** Gli utenti possono leggere orizzontalmente e trovare elementi correlati uno accanto all'altro, senza gap imbarazzanti.
-   **Facilità di analisi verticale.** Gli utenti possono analizzare le colonne di elementi correlati e trovare immediatamente ciò che cercano, con un minimo movimento degli occhi orizzontali.
-   **Complessità visiva minima.** Gli utenti percepiscono un layout per essere visivamente complesso se presenta linee della griglia di allineamento verticale non necessarie.

### <a name="horizontal-alignment"></a>Allineamento orizzontale

**Allineamento a sinistra**

A causa dell'ordine di lettura da sinistra a destra, l'allineamento a sinistra funziona correttamente per la maggior parte del contenuto. L'allineamento a sinistra rende i dati a colonne facili da analizzare verticalmente.

**Allineamento a destra**

L'allineamento a destra è la scelta migliore per i dati numerici, in particolare per le [colonne di dati numerici](ctrl-text-boxes.md). L'allineamento a destra è adatto anche per i [pulsanti di commit](glossary.md) e per i controlli allineati al bordo destro della finestra.

![cattura di schermata del pulsante freccia giù della ricerca avanzata ](images/vis-layout-image28.png)

In questo esempio, il controllo di divulgazione progressivo ricerca avanzata è allineato a destra perché viene inserito sul bordo destro della finestra.

**Allineamento al centro**

Allineamento al centro è la scelta migliore per le situazioni in cui l'allineamento a sinistra o a destra non è appropriato o appare sbilanciato.

![screenshot dei controlli del lettore multimediale centrati ](images/vis-layout-image29.png)

In questo esempio, il controllo Media Player viene centrato per dare un aspetto bilanciato.

Non centrare il contenuto della finestra solo per riempire lo spazio.

**Non corretto:**

![Screenshot di una finestra con troppi spazi vuoti ](images/vis-layout-image30.png)

In questo esempio, il contenuto viene centrato in modo errato in una finestra ridimensionabile per riempire lo spazio.

### <a name="vertical-alignment"></a>Allineamento verticale

**Elementi superiori**

A causa dell'ordine di lettura dall'alto in basso, l'allineamento superiore funziona correttamente per la maggior parte del contenuto. L'allineamento superiore rende gli elementi dell'interfaccia utente facili da analizzare orizzontalmente.

**Linee di base testo**

Quando si allineano verticalmente i controlli con testo, allineare le linee di base del testo per fornire un flusso di lettura orizzontale uniforme.

**Corretto:**

![screenshot del testo del pulsante e dell'etichetta allineato ](images/vis-layout-image31.png)

**Non corretto:**

![screenshot del testo del pulsante e dell'etichetta non allineato ](images/vis-layout-image32.png)

Nell'esempio corretto, il controllo e la relativa etichetta sono allineati verticalmente in base alle linee di base del testo.

Si sa che un layout presenta un corretto allineamento nei casi seguenti:

-   È facile eseguire l'analisi sia orizzontalmente che verticalmente.
-   Ha un aspetto visivo semplice.

### <a name="label-alignment"></a>Allineamento etichette

Le regole di allineamento generali si applicano alle etichette di controllo, ma si tratta di un problema comune degno di particolare attenzione. Gli obiettivi dell'allineamento delle etichette sono i seguenti:

-   Facilità di analisi verticale per trovare il controllo corretto.
-   Facilità di analisi orizzontale per associare etichette ai relativi controlli.
-   Facilità di localizzazione, gestione delle etichette che variano di lunghezza tra le varie lingue.
-   Funziona bene con una combinazione di lunghezze diverse delle etichette.
-   Consente di utilizzare in modo efficiente lo spazio disponibile evitando il troncamento del testo.

L'obiettivo complessivo è quello di ridurre la quantità di movimento degli occhi necessario per individuare gli utenti che probabilmente cercano, ma la natura dei controlli e gli elementi che gli utenti cercano dipendono dal contesto.

Sono disponibili quattro stili comuni di posizionamento e allineamento delle etichette, ognuno con i vantaggi seguenti:

-   Etichette giustificate a sinistra sopra i controlli
-   Etichette giustificate a sinistra a sinistra dei controlli
-   Etichette giustificate a sinistra a sinistra dei controlli, controlli incomplete a sinistra
-   Etichette giustificate a destra a sinistra dei controlli

**Etichette giustificate a sinistra sopra i controlli**

Questo stile è il più semplice da localizzare perché il layout non dipende dalla lunghezza delle etichette, ma occupa lo spazio più verticale.

![elenco con due colonne di etichette sopra i controlli ](images/vis-layout-image33.png)

Questo stile occupa lo spazio più verticale, ma è più facile da localizzare. Si tratta di una scelta migliore per l'assegnazione di etichette principalmente ai controlli interattivi.

Migliore utilizzo nei casi seguenti:

-   I controlli etichettati sono interattivi (non solo testo).
-   L'interfaccia utente verrà localizzata. Questo stile spesso offre spazio per raddoppiare o persino triplicare la lunghezza dell'etichetta.
-   L'interfaccia utente usa una tecnologia di layout fisso (ad esempio Win32).
-   Sono presenti dieci o meno controlli. Con più controlli, le etichette sono difficili da analizzare.
-   Lo spazio verticale è sufficiente per contenere le etichette.
-   Il layout deve essere formato libero, non solo colonne.

**Etichette giustificate a sinistra a sinistra dei controlli**

Questo stile è il più semplice da analizzare verticalmente e funziona bene anche quando le etichette sono molto lunghe, ma è più difficile associare l'etichetta al relativo controllo. Se necessario, questo stile può utilizzare etichette a più righe.

![elenco con quattro colonne di etichette a sinistra dei controlli ](images/vis-layout-image34.png)

Questo stile funziona correttamente. Tuttavia, esistono due colonne, ma visivamente sembra che ci siano quattro che rendono i dati più complessi.

Migliore utilizzo nei casi seguenti:

-   È probabile che gli utenti analizzino verticalmente per trovare etichette specifiche.
-   Gli utenti non potranno leggere le etichette e i controlli in modo da sinistra a destra, dall'alto verso il basso.
-   Lo spazio orizzontale è sufficiente per contenere le etichette.
-   Le etichette variano notevolmente di lunghezza.
-   Sono disponibili molti controlli, ad esempio con i moduli.
-   Sono disponibili poche colonne. Visivamente le etichette e i controlli vengono visualizzati come due colonne singole.

**Etichette giustificate a sinistra a sinistra dei controlli, controlli incomplete a sinistra**

Questo stile rende più semplice l'analisi verticale delle etichette e le etichette e i controlli orizzontalmente ed è molto efficiente. Tuttavia è più difficile analizzare i controlli verticalmente. I controlli sono giustificati a destra per sfruttare al meglio lo spazio disponibile.

![elenco di due colonne di etichette con controlli incompleti ](images/vis-layout-image35.png)

Questo stile è compatto e facile da leggere, ma è difficile analizzare i controlli verticalmente.

Migliore utilizzo nei casi seguenti:

-   L'interfaccia utente usa una tecnologia di layout variabile, ad esempio Windows Presentation Foundation.
-   È probabile che gli utenti analizzino verticalmente per trovare etichette specifiche.
-   È probabile che gli utenti leggano le etichette e i controlli in modo da sinistra a destra, dall'alto verso il basso.
-   È probabile che gli utenti analizzino i controlli verticalmente.
-   Il testo del controllo varia di lunghezza ed è probabile che venga troncato se è stato usato un altro stile.
-   I controlli sono di sola lettura, ad esempio caselle di testo di sola lettura. Per gli altri controlli, questo allineamento sarà invariato. Tuttavia, i controlli possono essere modificati in un clic.
-   Sono presenti molte colonne, ma alcuni controlli in una colonna.

**Etichette giustificate a destra a sinistra dei controlli**

Questo stile è il più semplice da leggere orizzontalmente per associare le etichette ai relativi controlli, ma è difficile eseguire la scansione verticale delle etichette e non funziona correttamente quando l'etichetta con le etichette rientrate e i controlli differiscono molto di lunghezza.

![elenco con etichette e controlli rientrati ](images/vis-layout-image36.png)

Questo stile permette una semplice analisi verticale dei controlli, ma rende difficile l'analisi verticale delle etichette.

Migliore utilizzo nei casi seguenti:

-   È probabile che gli utenti leggano le etichette e i controlli in modo da sinistra a destra, dall'alto verso il basso.
-   È probabile che gli utenti non analizzino verticalmente per trovare etichette specifiche, probabilmente perché:
    -   Sono presenti pochi controlli.
    -   Le etichette sono note.
    -   I controlli sono per lo più evidenti e raramente sono vuoti (probabilmente con valori predefiniti per impedire i controlli vuoti).
-   Lo spazio orizzontale è sufficiente per contenere le etichette.
-   Le etichette non variano in modo significativo.
-   Sono presenti molte colonne. Visivamente le etichette e i controlli vengono visualizzati come una singola colonna.

Prima di adottare uno di questi stili, tuttavia, prendere in considerazione altri due fattori:

-   Preferisci uno stile che puoi usare in modo coerente in tutto il programma.
-   Le etichette giustificate a sinistra sopra i controlli a sinistra dei controlli sono gli stili più comuni, quindi è necessario assegnarle una preferenza.

### <a name="balance"></a>Balance

Una finestra o una pagina presenta un saldo quando il relativo contenuto viene distribuito uniformemente sulla superficie. Se la superficie ha fisicamente lo stesso peso di quanto si presenta visivamente, un layout bilanciato non viene sottoposta a Tip-Over su un lato.

Il problema di bilanciamento più comune è la presenza di un numero eccessivo di contenuti sul lato sinistro di una finestra o di una pagina. È possibile creare un saldo nei modi seguenti:

-   Utilizzando margini maggiori sul lato sinistro rispetto a quello a destra.
-   Posizionamento degli elementi dell'interfaccia utente utilizzati per completare un'attività a destra.
-   Posizionamento degli elementi dell'interfaccia utente utilizzati nell'intera attività al centro.
-   Allungamento di controlli ridimensionabili o a più righe.
-   Uso strategico dell'allineamento al centro.

![screenshot della stampante a sinistra e di testo a destra ](images/vis-layout-image37.png)

Il layout di pagina della procedura guidata ben bilanciato Mostra un margine superiore sinistro rispetto al diritto di migliorare il bilanciamento.

Se queste tecniche non raggiungono un equilibrio, provare a ridurre la larghezza della finestra o della pagina in modo che corrisponda meglio al contenuto.

Per le superfici ridimensionabili, non centrare il contenuto solo per ottenere un equilibrio. Mantenere invece un'origine fissa superiore sinistra, definire una superficie di attacco massima e bilanciare il contenuto nello spazio usato.

### <a name="grids"></a>Griglie

Una griglia è un sistema di allineamento sottostante invisibile. Le griglie possono essere simmetriche, ma le griglie asimmetriche funzionano altrettanto bene. Se utilizzata da una singola finestra o pagina, le griglie consentono di organizzare il contenuto all'interno di una superficie. Quando vengono riutilizzate, le griglie creano un layout coerente tra le superfici.

Il numero di linee della griglia influisce sulla percezione della complessità visiva. Un layout con un numero inferiore di linee della griglia risulta più semplice rispetto a un layout con più linee della griglia.

**Visivamente complessa:**

![screenshot della finestra di dialogo ingombrante ](images/vis-layout-image38.png)

**Visivamente semplice:**

![screenshot della finestra di dialogo organizzata ](images/vis-layout-image39.png)

Le linee griglia non necessarie creano complessità visiva.

Si sa che un layout usa le griglie in modo efficace nei casi seguenti:

-   Le finestre o le pagine con contenuto o funzione simili hanno un layout simile.
-   Gli elementi di progettazione ripetuti vengono visualizzati in posizioni simili tra le finestre e le pagine.
-   Non sono presenti linee della griglia di allineamento verticali e orizzontali superflue.

### <a name="visual-simplicity"></a>Semplicità visiva

La semplicità visiva è la percezione che un layout non è più complicato del necessario.

Si sa che un layout presenta una semplicità visiva:

-   Elimina i livelli non necessari della finestra Chrome.
-   Visualizza il contenuto usando al massimo sette gruppi facilmente identificabili.
-   Usa il raggruppamento leggero, ad esempio il layout e i separatori anziché le caselle di gruppo.
-   USA i controlli leggeri, ad esempio i collegamenti anziché i pulsanti di comando per i comandi secondari e gli elenchi a discesa anziché gli elenchi per le opzioni.
-   Riduce il numero di linee della griglia di allineamento verticale e orizzontale.
-   Riduce il numero di dimensioni del controllo, ad esempio, usando solo una o due larghezze dei pulsanti di comando in una superficie.
-   Usa la divulgazione progressiva per nascondere gli elementi dell'interfaccia utente fino a quando non sono necessari.
-   Usa spazio sufficiente, in modo che la finestra o la pagina non ritenga un crampo.
-   Ridimensiona le finestre e i controlli in modo appropriato per eliminare lo scorrimento non necessario.
-   Usa un solo tipo di carattere con un numero ridotto di dimensioni e colori di testo.

Come regola generale, se un elemento di layout può essere eliminato senza danneggiare l'efficacia dell'interfaccia utente, è probabile che sia.

## <a name="guidelines"></a>Indicazioni

### <a name="screen-resolution-and-dpi"></a>Risoluzione dello schermo e dpi

-   **Supporta la risoluzione minima di Windows per 800x600 pixel.** Per le interfacce utente critiche che devono funzionare in modalità provvisoria, supportare una risoluzione efficace di 640x480 pixel. Assicurarsi di tenere conto dello spazio usato dalla barra delle applicazioni riservando 48 [pixel relativi](glossary.md) per le finestre visualizzate con la barra delle applicazioni.
-   **Ottimizzare il layout delle finestre ridimensionabili per una risoluzione efficace di 1024x768 pixel.** Ridimensionare automaticamente le finestre per risoluzioni dello schermo inferiori in modo ancora funzionante.
-   **Assicurarsi di testare le finestre in modalità 96 punti per pollice (dpi) (a 800x600 pixel), 120 dpi (a 1024x768 pixel) e 144 dpi (a 1200x900 pixel).** Verificare la presenza di problemi di layout, ad esempio il ritaglio di controlli, testo e finestre, nonché l'estensione delle icone e delle bitmap.
-   **Per i programmi con scenari di utilizzo tocco e dispositivi mobili, ottimizzarli per 120 dpi.** Le schermate ad alta risoluzione sono attualmente prevalentemente nei PC portatili e a tocco.

### <a name="window-size"></a>Dimensioni finestra

-   **Scegliere le dimensioni predefinite della finestra appropriate per il relativo contenuto.** Se è possibile utilizzare lo spazio in modo efficiente, non è necessario utilizzare dimensioni della finestra iniziale maggiori.
-   **Utilizzare un'altezza bilanciata per proporzioni.** È preferibile una percentuale di proporzioni compresa tra 3:5 e 5:3, sebbene sia possibile utilizzare le proporzioni di 1:3 per le finestre di dialogo dei messaggi, ad esempio errori e avvisi.
-   **Usare le finestre ridimensionabili ogni volta che è possibile evitare le barre di scorrimento e i dati troncati.** Windows con contenuto dinamico, documenti, immagini, elenchi e alberi è più vantaggioso dalle finestre ridimensionabili.
-   **Per i documenti di testo, prendere in considerazione la lunghezza massima della riga di 80 caratteri** per facilitare la lettura del testo. I caratteri includono lettere, punteggiatura e spazi.
-   Finestre a dimensione fissa:
    -   **Le finestre a dimensione fissa devono essere completamente visibili e dimensionate per adattarsi all'area di lavoro.**
-   Finestre ridimensionabili:
    -   **Le finestre ridimensionabili possono essere ottimizzate per risoluzioni più elevate, ma ridimensionate in base alle esigenze in fase di visualizzazione per la risoluzione effettiva dello schermo.**
    -   **Le dimensioni delle finestre progressivamente più grandi devono visualizzare progressivamente ulteriori informazioni.** Assicurarsi che almeno una parte o un controllo della finestra includa contenuto ridimensionabile.
    -   **Mantiene l'origine superiore sinistra del contenuto fisso quando la finestra viene ridimensionata.** Non spostare l'origine per bilanciare il contenuto mentre le dimensioni della finestra cambiano.
    -   **Impostare una dimensione massima del contenuto se il contenuto può essere troppo esteso.** Se il contenuto diventa non ingombrante, non ridimensionare l'area del contenuto oltre la larghezza massima o modificare l'origine del contenuto quando la finestra viene ridimensionata in modo più grande. Al contrario, Mantieni una larghezza massima e un'origine superiore sinistra fissa.
    -   **Impostare una dimensione minima della finestra se è presente una dimensione al di sotto della quale il contenuto non è più utilizzabile.** Per i controlli ridimensionabili, impostare dimensioni minime degli elementi ridimensionabili sulle dimensioni funzionali più piccole, ad esempio la larghezza minima delle colonne funzionali nelle visualizzazioni elenco. Gli elementi facoltativi dell'interfaccia utente devono essere rimossi completamente.
    -   **Provare a modificare la presentazione per rendere il contenuto utilizzabile a dimensioni inferiori.**

        ![screenshot dei controlli Media Player ](images/vis-layout-image16.png)

        In questo esempio, Windows Media Player modifica il formato quando la finestra diventa troppo piccola per il formato standard.

### <a name="control-size"></a>Dimensioni del controllo

-   **Rendere tutti i controlli interattivi almeno relativi 16x16 pixel.** Questa operazione funziona bene per tutti i dispositivi di input, tra cui la tecnologia Windows Tablet e touch.
-   **Ridimensionare i controlli per evitare i dati troncati.** Non troncare i dati che devono essere letti per eseguire un'attività. Dimensioni colonne visualizzazione elenco per evitare i dati troncati.
-   **Ridimensionare i controlli per eliminare lo scorrimento non necessario.** Rendere i controlli leggermente più grandi se questa operazione elimina una barra di scorrimento. Devono essere presenti poche barre di scorrimento verticali e nessuna barra di scorrimento orizzontale non necessaria.

    ![screenshot delle dimensioni dell'elenco per evitare una barra di scorrimento ](images/vis-layout-image40.png)

    In questo esempio, l'elenco a discesa viene ridimensionato per eliminare la barra di scorrimento.

-   **Ridurre il numero di dimensioni del controllo in una superficie.** Preferisci usare le dimensioni dei controlli [standard consigliate](#recommended-sizing-and-spacing) e, quando necessario, usare un numero ridotto di controlli di dimensioni maggiori o minori. Provare a usare una sola larghezza per le caselle di riepilogo e le visualizzazioni albero e non più di tre larghezze per i pulsanti di comando e gli elenchi a discesa. Tuttavia, le larghezze della casella di testo e della casella combinata dovrebbero indicare la lunghezza dell'input più lungo o previsto.

    ![screenshot della finestra di dialogo con elenchi e pulsanti ](images/vis-layout-image41.png)

    In questo esempio, una casella di riepilogo e le dimensioni del pulsante di comando vengono usate in modo coerente.

-   **Per i controlli ridimensionati in base al testo, includere un ulteriore 30% (fino al 200% per un testo più breve) per qualsiasi testo che verrà localizzato.** Questa guida presuppone che il layout venga progettato con testo in lingua inglese. Si noti inoltre che questa linea guida si riferisce al testo localizzato, non ai numeri.
-   **Estendere i controlli di testo statici, le caselle di controllo e i pulsanti di opzione alla larghezza massima che rientrerà nel layout.** In questo modo si evita il troncamento dal testo a lunghezza variabile e dalla localizzazione.

    **Non corretto:**

    ![screenshot del controllo dello stato di avanzamento e del testo parziale ](images/vis-layout-image42.png)

    In questo esempio il testo del controllo non è necessariamente troncato.

### <a name="control-spacing"></a>Spaziatura del controllo

-   **Se i controlli non si toccano, avere almeno 3 DLU (5 pixel relativi) di spazio tra di essi.** In caso contrario, gli utenti possono fare clic sullo spazio inattivo tra i controlli. Poiché facendo clic su spazio inattivo non sono presenti risultati o commenti visivi, gli utenti spesso non sono sicuri di ciò che si è verificato.

### <a name="placement"></a>Selezione host

-   **Disporre gli elementi dell'interfaccia utente all'interno di una superficie per il flusso naturale in un ordine da sinistra a destra, dall'alto verso il basso (nelle impostazioni cultura occidentali).** La posizione degli elementi dell'interfaccia utente comunica la relazione ed è necessario eseguire il mirroring dei passaggi necessari per eseguire l'attività.
-   **Posizionare gli elementi dell'interfaccia utente che avviano un'attività nell'angolo superiore sinistro o nel centro superiore.** Fornire all'elemento dell'interfaccia utente che gli utenti dovrebbero esaminare prima l'enfasi visiva più grande.
-   **Posizionare gli elementi dell'interfaccia utente che completano un'attività nell'angolo inferiore destro.**
-   **Posizionare insieme gli elementi dell'interfaccia utente correlati e separare gli elementi non correlati.**
-   **Inserire i passaggi necessari nel flusso principale.**
-   **Inserire i passaggi facoltativi al di fuori del flusso principale,** probabilmente deaccentuati usando uno sfondo adatto o una divulgazione progressiva.
-   **Inserire gli elementi utilizzati di frequente prima degli elementi utilizzati** di frequente nel percorso di analisi.

### <a name="focus"></a>Focus

-   **Scegliere un singolo elemento dell'interfaccia utente che gli utenti devono prima esaminare per essere il punto focale.** Il punto focale dovrebbe essere qualcosa di importante che gli utenti debbano trovare e comprendere rapidamente.
-   **Posizionare il punto focale nell'angolo superiore sinistro o nel centro superiore.**
-   **Fornire al punto focale la massima enfasi visiva,** ad esempio testo prominente, selezione predefinita o lo stato attivo per l'input iniziale.

### <a name="alignment"></a>Allineamento

-   In genere, usare l'allineamento a sinistra.
-   Usare l'allineamento a destra per dati numerici, in particolare per le colonne di dati numerici.
-   Usare l'allineamento a destra per i pulsanti di commit, oltre ai controlli allineati con il bordo destro della finestra.
-   Usare allineamento al centro quando l'allineamento a sinistra o a destra non è appropriato o viene visualizzato sbilanciato.
-   Quando si allineano verticalmente i controlli con testo, allineare le linee di base del testo per fornire un flusso di lettura orizzontale uniforme.
-   Per l'allineamento delle etichette, vedere la sezione relativa all' [allineamento delle etichette](#label-alignment) nei concetti di progettazione.

### <a name="accessibility"></a>Accessibilità

-   **Non usare il layout come unico mezzo per fornire informazioni importanti su un'interfaccia utente.** Gli utenti con problemi visivi potrebbero non essere in grado di interpretare questa presentazione. Verificare, ad esempio, che le etichette dei controlli comunicano la relazione con altri elementi.
-   **Non incorporare controlli subordinati all'interno delle etichette di controllo per creare una frase o una frase.** Tali associazioni sono basate esclusivamente sul layout e non sono gestite correttamente dalla navigazione da tastiera o dalle tecnologie per l'accessibilità. Questa tecnica, inoltre, non è localizzabile perché la struttura della frase varia in base alla lingua.

    **Non corretto:**

    ![Screenshot di una casella di testo all'interno di una frase ](images/vis-layout-image43.png)

    In questo esempio la casella di testo non viene inserita correttamente nell'etichetta della casella di controllo.

    **Corretto:**

    ![Screenshot di una casella di testo alla fine di una frase ](images/vis-layout-image44.png)

    In questo caso, la casella di testo viene posizionata dopo l'etichetta della casella di controllo.

-   **Rendere accessibile il raggruppamento.** I gruppi definiti da riquadri della finestra, caselle di gruppo, separatori, etichette di testo e aggregatori vengono gestiti automaticamente dagli strumenti di accessibilità. Tuttavia, i gruppi definiti solo per posizione e sfondi non sono e devono essere definiti a livello di codice per l'accessibilità.

Per altre linee guida, vedere [accessibilità](inter-accessibility.md).

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

**Ridimensionamento del controllo**

La tabella seguente elenca le dimensioni consigliate (larghezza x altezza o altezza se un numero singolo) per gli elementi dell'interfaccia utente comuni (per 9 PT. Segoe UI a 96 dpi). Le larghezze in base all'elemento più lungo della lingua inglese aggiungono il 30% per la localizzazione (fino al 200% per un testo più breve) per qualsiasi testo (ma non per i numeri) che verrà localizzato.



|                                                                                                 |                            |                                                                                                   |                                                                                                            |
|-------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
|                                                                                                 | **Controllo**<br/>     | **Unità di dialogo**<br/>                                                                       | **Pixel relativi**<br/>                                                                             |
| ![screenshot delle caselle di controllo e delle relative etichette ](images/vis-layout-image45.png)<br/>       | Caselle di controllo<br/>     | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![screenshot della casella combinata ](images/vis-layout-image46.png)<br/>                          | Caselle combinate<br/>     | larghezza dell'elemento più lungo + 30% x 14<br/>                                                       | larghezza dell'elemento più lungo + 30% x 23<br/>                                                                |
| ![Screenshot di un pulsante di comando ](images/vis-layout-image47.png)<br/>                   | Pulsanti di comando<br/> | 50 x 14<br/>                                                                                | 75 x 23<br/>                                                                                         |
| ![Screenshot di uno dei due collegamenti ai comandi selezionati ](images/vis-layout-image48.png)<br/>  | Collegamenti ai comandi<br/>   | 25 (una riga) o 35 (due righe)<br/>                                                        | 41 (una riga) o 58 (due righe)<br/>                                                                 |
| ![Screenshot di un elenco a discesa ](images/vis-layout-image49.png)<br/>                   | Elenchi a discesa<br/> | larghezza dei dati più lunghi validi + 30% x 14<br/>                                                 | larghezza dell'elemento più lungo + 30% x 23<br/>                                                                |
| ![Screenshot di una casella di riepilogo ](images/vis-layout-image50.png)<br/>                         | Caselle di riepilogo<br/>      | larghezza dell'elemento più lungo + 30% x un numero integrale di elementi (minimo 3 elementi)<br/>            |                                                                                                            |
| ![Screenshot di un elenco di file di immagine ](images/vis-layout-image51.png)<br/>            | Visualizzazioni elenco<br/>      | larghezze delle colonne che evitano i dati troncati x un numero integrale di elementi<br/>                 |                                                                                                            |
| ![Screenshot di un indicatore di stato ](images/vis-layout-image52.png)<br/>                     | Indicatori di stato<br/>   | 107 o 237 x 8<br/>                                                                         | 160 o 355 x 15<br/>                                                                                 |
| ![screenshot dei pulsanti di opzione ](images/vis-layout-image53.png)<br/>                      | Pulsanti di opzione<br/>   | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![screenshot del controllo dispositivo di scorrimento ](images/vis-layout-image54.png)<br/>                     | Dispositivi di scorrimento<br/>         | 15<br/>                                                                                     | 24<br/>                                                                                              |
| ![screenshot del testo:' Select Time zone ' ](images/vis-layout-image55.png)<br/>           | Testo (statico)<br/>   | 8<br/>                                                                                      | 13<br/>                                                                                              |
| ![screenshot della casella di testo vuota ](images/vis-layout-image56.png)<br/>                     | Caselle di testo<br/>      | larghezza dell'input più lungo o previsto + 30% x 14 (una riga) + 10 per ogni riga aggiuntiva<br/> | larghezza dei dati più lunghi validi + 30% x 23 pixel relativi (una riga) + 16 per ogni riga aggiuntiva<br/> |
| ![screenshot delle cartelle nidificate in Esplora risorse ](images/vis-layout-image57.png)<br/> | Visualizzazioni albero<br/>      | larghezza dell'elemento più lungo + 30% x un numero integrale di elementi (minimo 5 elementi)<br/>            |                                                                                                            |



 

**Spaziatura**

La tabella seguente elenca la spaziatura consigliata tra gli elementi comuni dell'interfaccia utente (per 9 PT. Segoe UI a 96 dpi).



|                                                                                                   |                                                                                                       |                                                                                           |                                                                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
|                                                                                                   | **elemento**<br/>                                                                                | **Unità di dialogo**<br/>                                                               | **Pixel relativi**<br/>                                                            |
| ![Immagine che mostra la spaziatura nei margini della finestra di dialogo ](images/vis_layout_image58.jpeg)<br/>        | Margini della finestra di dialogo<br/>                                                                         | 7 su tutti i lati<br/>                                                                 | 11 su tutti i lati<br/>                                                                |
| ![Immagine che mostra la spaziatura tra le etichette e i controlli ](images/vis_layout_image59.jpeg)<br/>  | Tra le etichette di testo e i controlli associati (ad esempio, caselle di testo e caselle di riepilogo)<br/> | 3<br/>                                                                              | 5<br/>                                                                              |
| ![Immagine che mostra la spaziatura tra i controlli correlati ](images/vis_layout_image60.jpeg)<br/>     | Tra i controlli correlati<br/>                                                                   | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Immagine che mostra la spaziatura tra i controlli non correlati ](images/vis_layout_image61.jpeg)<br/>   | Tra controlli non correlati<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
| ![Immagine che mostra la spaziatura del primo controllo in un gruppo ](images/vis_layout_image62.jpeg)<br/>  | Primo controllo in una casella di gruppo<br/>                                                               | 11 giù dalla parte superiore della casella di gruppo; Allinea verticalmente al titolo della casella di gruppo<br/> | 16 nella parte superiore della casella di gruppo; Allinea verticalmente al titolo della casella di gruppo<br/> |
| ![Aa511279. between-related (en-US, MSDN. 10). jpg](images/vis_layout_image60.jpeg)<br/>         | Tra i controlli in una casella di gruppo<br/>                                                            | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Immagine che mostra la spaziatura tra i pulsanti ](images/vis_layout_image63.jpeg)<br/>              | Pulsanti disposti orizzontalmente o verticalmente<br/>                                        | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Immagine che mostra la spaziatura dell'ultimo controllo in un gruppo ](images/vis_layout_image64.jpeg)<br/>   | Ultimo controllo in una casella di gruppo<br/>                                                                | 7 superiore alla parte inferiore della casella di gruppo<br/>                                            | 11 sopra il fondo della casella di gruppo<br/>                                           |
| ![Immagine che mostra la spaziatura dal bordo sinistro della casella di gruppo ](images/vis_layout_image65.jpeg)<br/>  | Dal bordo sinistro di una casella di gruppo<br/>                                                          | 6<br/>                                                                              | 9<br/>                                                                              |
| ![Immagine che mostra la spaziatura dell'etichetta di testo accanto al controllo ](images/vis_layout_image66.jpeg)<br/> | Etichetta di testo accanto a un controllo<br/>                                                                | 3 giù dalla parte superiore del controllo<br/>                                             | 5 giù dalla parte superiore del controllo<br/>                                             |
| ![Immagine che mostra la spaziatura tra i paragrafi di testo ](images/vis_layout_image67.jpeg)<br/>   | Tra i paragrafi di testo<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
|                                                                                                   | Spazio minimo tra controlli interattivi<br/>                                                | 3 o nessuno spazio<br/>                                                                  | 5 o nessuno spazio<br/>                                                                  |
|                                                                                                   | Spazio minimo tra un controllo non interattivo e qualsiasi altro controllo<br/>                     | 2<br/>                                                                              | 3<br/>                                                                              |



 

 

