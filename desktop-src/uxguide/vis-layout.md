---
title: Layout
description: Il layout è il ridimensionamento, la spaziatura e la posizione del contenuto all'interno di una finestra o di una pagina.
ms.assetid: 39cd896f-d3cc-4768-a20c-a7f598da7136
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2bd705346f979a44cc2a8c7917f81b9e918ce5277893b5a377ab1ede4b945bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119817083"
---
# <a name="layout"></a>Layout

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Il layout è il ridimensionamento, la spaziatura e la posizione del contenuto all'interno di una finestra o di una pagina. Un layout efficace è fondamentale per aiutare gli utenti a trovare rapidamente ciò che cercano, oltre a rendere l'aspetto visivamente accattivante. Un layout efficace può fare la differenza tra le progettazioni immediatamente comprensibili dagli utenti e quelle che lasciano gli utenti perplessi e sopraffatti.

**Nota:** Le linee guida relative [alla gestione delle](win-window-mgt.md) finestre sono presentate in un articolo separato. Il ridimensionamento e la spaziatura dei controlli specifici consigliati sono presentati nei rispettivi articoli sulle linee guida.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="visual-hierarchy"></a>Gerarchia visiva

Una finestra o una pagina ha una gerarchia visiva chiara quando il relativo aspetto indica la relazione e la priorità dei relativi elementi. Senza una gerarchia visiva, gli utenti devono capire queste relazioni e le priorità stesse.

La gerarchia visiva si ottiene combinando sapientemente gli attributi seguenti:

-   **Concentrarsi.** Il layout indica dove gli utenti devono cercare per primi.
-   **Flow.** L'occhio scorre uniformemente e naturalmente da un percorso chiaro attraverso la superficie, trovando gli elementi dell'interfaccia utente nell'ordine appropriato per l'uso.
-   **Raggruppamento.** Gli elementi dell'interfaccia utente correlati logicamente hanno una relazione visiva chiara. Gli elementi correlati vengono raggruppati tra loro. Gli elementi non correlati sono separati.
-   **Enfasi.** Gli elementi dell'interfaccia utente vengono evidenziati in base alla relativa importanza.
-   **Allineamento.** Gli elementi dell'interfaccia utente hanno una posizione coordinata, quindi sono facili da analizzare e appaiono in ordine.

Inoltre, il layout effettivo ha questi attributi:

-   **Indipendenza del dispositivo.** Il layout viene visualizzato come previsto indipendentemente dal tipo di carattere o dalle dimensioni, punti per pollice (dpi), schermo o adattatore grafico.
-   **Facile da analizzare.** Gli utenti possono trovare il contenuto che stanno cercando a colpo d'occhio.
-   **Efficienza.** Gli elementi dell'interfaccia utente di grandi dimensioni devono essere di grandi dimensioni e gli elementi di piccole dimensioni funzionano in modo molto piccolo.
-   **Ridimensionabilità.** Se utile, una finestra è ridimensionabile e il relativo layout del contenuto è efficace indipendentemente dalla superficie grande o piccola.
-   **Equilibrio.** Il contenuto viene distribuito uniformemente sulla superficie.
-   **Semplicità visiva.** La percezione che un layout non sia più complesso del necessario. Gli utenti non si sentono sovraccaricati dall'aspetto del layout.
-   **Coerenza.** Finestre o pagine simili usano un layout simile, in modo che gli utenti si sentano sempre orientati.

Anche se il ridimensionamento, la spaziatura e il posizionamento sono concetti semplici, la sfida con il layout consiste nel ottenere la giusta combinazione di questi attributi.

In Windows, il layout viene comunicato usando metriche indipendenti dal dispositivo, ad esempio unità di dialogo (DKU) e pixel relativi.

### <a name="a-design-model-for-reading"></a>Un modello di progettazione per la lettura

**Gli utenti scelgono ciò che leggono in base all'aspetto e all'organizzazione del contenuto.** Per creare un layout efficace, è necessario comprendere quali utenti tendono a leggere e perché.

È possibile prendere decisioni di layout usando questo modello di progettazione per la lettura:

-   Le persone leggono da sinistra a destra, dall'alto verso il basso (nelle culture occidentali).
-   Esistono due modalità di lettura: lettura immersiva e scansione. L'obiettivo della lettura immersiva è la comprensione.

    ![Figura della freccia rossa nel modello di lettura a zigzag ](images/vis-layout-image1.png)

    Questo diagramma modella la lettura immersiva.

    Al contrario, l'obiettivo della scansione è individuare gli elementi. Il percorso di analisi complessivo è simile al seguente:

    ![Figura della freccia rossa in un modello di lettura diagonale ](images/vis-layout-image2.png)

    Questo diagramma modella l'analisi.

    ![figura della freccia rossa in un motivo verso il basso e un arco ](images/vis-layout-image3.png)

    Se il testo è in esecuzione lungo il bordo sinistro di una pagina, gli utenti analizzano prima il bordo sinistro.

-   Quando si usa il software, gli utenti non sono immersi nell'interfaccia utente stessa, ma nel proprio lavoro. Di conseguenza, gli utenti in genere non leggono il testo dell'interfaccia utente che analizzano. Legge quindi i bit di testo in modo completo solo quando ritiene di doversi servono.
-   Gli utenti tendono a ignorare i riquadri di spostamento sul lato sinistro o destro di una pagina. Gli utenti riconoscono di essere presenti, ma guardano i riquadri di spostamento solo quando vogliono spostarsi.
-   Gli utenti tendono a ignorare blocchi di testo non formattato di grandi dimensioni senza leggerli.

    ![Figura di testo con frecce che mostrano il testo di scansione ](images/vis-layout-image4.png)

    Gli utenti tendono a ignorare blocchi di testo e riquadri di spostamento di grandi dimensioni durante l'analisi.

-   Tutti gli elementi sono uguali, gli utenti guardano prima nell'angolo superiore sinistro di una finestra, analizzano la pagina e terminano l'analisi nell'angolo inferiore destro. Tendono a ignorare l'angolo inferiore sinistro.

    ![figura della pagina e freccia da sinistra a basso a destra ](images/vis-layout-image5.png)

    Tutti gli elementi uguali, gli utenti leggeranno questi numeri nell'ordine seguente: 1, 2, 4 e 3.

-   Tuttavia, nell'interfaccia utente interattiva non tutti gli elementi sono uguali, quindi elementi dell'interfaccia utente diversi ricevono diversi livelli di attenzione. Gli utenti tendono a esaminare i controlli interattivi, in particolare i controlli in alto a sinistra e al centro della finestra e il testo in primo piano.

![Figura dello schermo con testo acuto e sfocato ](images/vis-layout-image6.png)

Gli utenti si concentrano sui principali controlli interattivi e sull'istruzione principale di primo piano e guardano altre cose solo quando necessario.

-   Gli utenti tendono a leggere le etichette di controllo interattive, in particolare quelle che sembrano rilevanti per completare l'attività a portata di mano. Al contrario, gli utenti tendono a leggere testo statico solo quando ne hanno bisogno.
-   Gli elementi che appaiono diversi attirano l'attenzione. Il testo in grassetto e il testo di grandi dimensioni si distingue dal testo normale. Gli elementi dell'interfaccia utente con colore o su uno sfondo colorato si distinguono. Gli elementi con icone si distinguono dagli elementi senza icone.
-   Gli utenti non scorrono a meno che non ne abbia un motivo. Se il contenuto [sopra la visualizzazione](glossary.md) non fornisce un motivo per scorrere, non lo sarà.
-   Dopo aver deciso cosa fare, gli utenti interrompino immediatamente la scansione e lo eserciteranno.
-   Poiché gli utenti interrompino l'analisi quando si pensa di aver completato l'operazione, tendono a ignorare qualsiasi elemento oltre a quello che sembra essere il punto di completamento.

![Screenshot delle opzioni della tastiera ](images/vis-layout-image7.png)

Gli utenti interrompino l'analisi quando si pensa di aver finito.

Naturalmente, ci saranno eccezioni a questo modello generale. I dispositivi di tracciamento oculare indicano che il comportamento degli utenti reali è piuttosto irregolare. L'obiettivo di questo modello è aiutare a prendere decisioni e compromessi efficaci, non a modellare in modo accurato il comportamento dell'utente. Tuttavia, dopo aver letto questo elenco, si spera di aver riconosciuto anche molti dei propri modelli di lettura.

### <a name="designing-for-scanning"></a>Progettazione per l'analisi

**Gli utenti non leggono e analizzano, quindi è consigliabile progettare le superfici dell'interfaccia utente per l'analisi.** Non presupporre che gli utenti leggono il testo come scritto in un ordine da sinistra a destra e dall'alto verso il basso, ma piuttosto che guardino gli elementi dell'interfaccia utente che attraggono la loro attenzione.

Per progettare per l'analisi:

-   Si supponga che gli utenti inizino eseguendo rapidamente la scansione dell'intera finestra e quindi leggendo gli elementi dell'interfaccia utente nell'ordine seguente:
    -   Controlli interattivi al centro
    -   Pulsanti di commit
    -   Controlli interattivi trovati altrove
    -   Istruzione main
    -   Spiegazioni supplementari
    -   Testo visualizzato con un'icona di avviso
    -   Titolo della finestra
    -   Altro testo statico nel corpo principale
    -   Note a piè di pagina
-   Posizionare gli elementi dell'interfaccia utente che avviano un'attività nell'angolo superiore sinistro o in alto al centro.
-   Posizionare gli elementi dell'interfaccia utente che completano un'attività nell'angolo inferiore destro.
-   Quando possibile, inserire testo fondamentale nei controlli interattivi anziché nel testo statico.
-   Evitare di inserire informazioni cruciali nell'angolo inferiore sinistro o nella parte inferiore di un controllo o di una pagina a scorrimento lungo.
-   Non presentare grandi blocchi di testo. Eliminare il testo non necessario. Usare lo [stile di presentazione della piramide](text-ui.md) invertita.
-   Se si fa qualcosa per attirare l'attenzione degli utenti, assicurarsi che l'attenzione sia garantita.

Quando possibile, usare questo modello invece di farlo; ma in alcuni casi sarà necessario evidenziare o de-evidenziare determinati elementi dell'interfaccia utente.

Per evidenziare gli elementi principali dell'interfaccia utente:

-   Inserire gli elementi primari dell'interfaccia utente nel [percorso di analisi](glossary.md).
-   Inserire qualsiasi interfaccia utente per avviare un'attività nell'angolo superiore sinistro o in alto al centro.
-   Inserire i pulsanti di commit nell'angolo inferiore destro.
-   Posizionare al centro l'interfaccia utente primaria rimanente.
-   Usare controlli che attraggono l'attenzione, ad esempio pulsanti di comando, collegamenti di comando e icone.
-   Usare testo di primo piano, tra cui testo di grandi dimensioni e testo in grassetto.
-   Inserire testo che gli utenti devono leggere nei controlli interattivi, con icone o [su banner](vis-graphic.md).
-   Usare testo scuro su uno sfondo chiaro.
-   Racchiudere gli elementi con spazio libero.
-   Non è necessaria alcuna interazione, ad esempio il puntamento o il passaggio del mouse, per visualizzare l'elemento che si sta enfatizzando.

    ![Screenshot delle opzioni di attivazione di Windows ](images/vis-layout-image8.png)

    Questo esempio illustra molti modi per evidenziare gli elementi primari dell'interfaccia utente.

Per de-evidenziare gli elementi secondari dell'interfaccia utente:

-   Inserire gli elementi secondari dell'interfaccia utente all'esterno del percorso di analisi.
-   Inserire tutto ciò che gli utenti in genere non devono visualizzare nell'angolo inferiore sinistro o nella parte inferiore della finestra.
-   Usare i controlli che non attraggono l'attenzione, ad esempio i collegamenti alle attività anziché i pulsanti di comando.
-   Usare testo normale o grigio.
-   Usare testo chiaro su uno sfondo scuro. Il testo bianco su sfondo grigio scuro o blu funziona correttamente.
-   Racchiudere gli elementi con spazio minimo.
-   Valutare la possibilità di [usare la diffusione progressiva](ctrl-progressive-disclosure-controls.md) per nascondere gli elementi secondari dell'interfaccia utente.

    ![Screenshot di elementi di interfaccia di grandi e piccoli dimensioni ](images/vis-layout-image9.png)

    Questo esempio illustra molti modi per de-evidenziare gli elementi secondari dell'interfaccia utente.

### <a name="using-screen-space-effectively"></a>Uso efficace dello spazio sullo schermo

L'uso efficace dello spazio dello schermo richiede il bilanciamento di diversi fattori: l'uso di una quantità di spazio insufficiente e di una finestra risulta pesante e disaffettuata e persino difficile da usare in base alla legge di [Fitts.](inter-mouse.md)

**Non corretto:**

![Screenshot che mostra una quantità troppo grande di spazio vuoto ](images/vis-layout-image10.png)

In questo esempio la finestra è troppo grande per il contenuto.

D'altra parte, usare troppo poco spazio e una finestra sembra complicata, fastidiosa e intimidatoria e difficile da usare se richiede lo scorrimento e altre manipolazioni da usare.

**Non corretto:**

![Screenshot con troppi controlli ](images/vis-layout-image11.png)

In questo esempio la finestra è troppo piccola per il contenuto.

Anche se l'interfaccia utente critica deve rientrare nella risoluzione effettiva minima [supportata,](glossary.md)non presupporre che l'uso efficace dello spazio sullo schermo significhi che le finestre devono essere il più piccole possibili. **Il layout efficace rispetta lo spazio aperto e non tenta di eseguire il cram di tutto nello spazio più piccolo possibile.** Gli schermi moderni hanno uno spazio dello schermo significativo ed è opportuno usarlo in modo efficace quando è possibile. Di conseguenza, err sul lato dell'uso di troppo spazio sullo schermo anziché troppo poco. In questo modo le finestre sono più leggere e più raggiungibili.

Si sa che un layout usa in modo efficace lo spazio dello schermo quando:

-   Windows, i riquadri delle finestre e i controlli non devono essere ridimensionati per essere utilizzabili. Se la prima cosa che fanno gli utenti è ridimensionare una finestra, un riquadro o un controllo, le dimensioni non sono erre.
-   I dati non vengono troncati. La maggior parte dei dati nelle visualizzazioni elenco e nelle visualizzazioni albero non ha puntini di sospensione e i dati in altri controlli non vengono ritagliati a meno che la lunghezza dei dati non sia insolitamente grande. I dati che devono essere letti per eseguire un'attività non devono essere troncati.
-   Le finestre e i controlli vengono ridimensionati in modo appropriato per eliminare lo scorrimento non necessario. Esistono poche barre di scorrimento orizzontali e nessuna barra di scorrimento verticale non necessaria.
-   I controlli usano principalmente le dimensioni standard. Cercare di ridurre il numero di dimensioni dei controlli, ad esempio usando solo una o due larghezze dei pulsanti di comando su una superficie.
-   La superficie dell'interfaccia utente è bilanciata. Non sono presenti aree dello schermo non utilizzate di grandi dimensioni.

Scegliere dimensioni della finestra sufficientemente grandi da soddisfare le proprie finalità. Se la finestra è ridimensionabile, questo obiettivo si applica alle dimensioni predefinite. Una combinazione di dati troncati o barre di scorrimento e molto spazio disponibile sullo schermo è un chiaro segno di **layout inefficace.**

### <a name="control-sizing"></a>Ridimensionamento dei controlli

In genere il primo passaggio per usare in modo efficace lo spazio dello schermo consiste nel determinare le dimensioni giuste per i vari elementi dell'interfaccia utente. Fare riferimento alla [tabella Ridimensionamento controllo](#recommended-sizing-and-spacing) e al ridimensionamento consigliato negli articoli specifici sulle linee guida per il controllo.

La legge di Fitts indica che più piccola è la destinazione, più tempo è necessario per acquisirla con il mouse. Inoltre, per i computer che usano Tecnologia Windows per Tablet PC, il "mouse" potrebbe essere effettivamente una penna o un dito dell'utente, pertanto è consigliabile prendere in considerazione dispositivi di input alternativi quando si determinano le dimensioni per i controlli di piccole dimensioni. **Una dimensione di controllo di 16x16 pixel relativi è una buona dimensione minima per qualsiasi dispositivo di input.** Al contrario, i pulsanti di controllo di selezione pixel relativi standard 15x9 sono troppo piccoli per essere usati in modo efficace dalle penna.

### <a name="spacing"></a>Spaziatura

Fornire spazio eccessivo (ma non eccessivo) rende il layout più comodo e più facile da analizzare. Lo spazio effettivo non è lo spazio inutilizzato, ma svolge un ruolo importante nel migliorare la capacità di analisi degli utenti e aggiunge anche un aspetto visivo della progettazione. Per le linee guida, vedere la [tabella Spaziatura](#recommended-sizing-and-spacing).

Per i computer Tecnologia Windows per Tablet PC, anche in questo caso il "mouse" potrebbe essere effettivamente una penna o un dito dell'utente. La destinazione è più difficile quando si usa una penna o un dito come dispositivo di puntamento e gli utenti toccano all'esterno della destinazione prevista. Quando i controlli interattivi vengono posizionati molto vicini ma non sono effettivamente toccati, gli utenti possono fare clic sullo spazio inattivo tra i controlli. Poiché fare clic su spazio inattivo non ha alcun risultato o feedback visivo, gli utenti sono spesso incerti su cosa sia successo. Se i controlli di piccole dimensioni sono troppo spaziati, l'utente deve toccare con precisione per evitare di toccare l'oggetto errato. **Per risolvere questi problemi, le aree di destinazione dei controlli interattivi devono toccare o avere almeno 3 DLU (5 pixel relativi) di spazio tra di essi.**

Si sa che un layout ha una spaziatura buona quando:

-   Nel complesso, la superficie dell'interfaccia utente si senta comoda e non si senta intrusa.
-   Lo spazio appare uniforme ed bilanciato.
-   Gli elementi correlati sono vicini e gli elementi non correlati sono relativamente distanti.
-   Non esiste spazio vuoto tra i controlli che devono essere uniti, ad esempio i pulsanti della barra degli strumenti.

### <a name="resizable-windows"></a>Finestre ridimensionabili

Anche le finestre ridimensionabili sono un fattore che consente di usare in modo efficace lo spazio dello schermo. Alcune finestre sono costituite da contenuto fisso e non traggono vantaggio dall'essere ridimensionabili, ma le finestre con contenuto ridimensionabile devono essere ridimensionabili. Naturalmente, il motivo per cui gli utenti ridimensionano una finestra è quello di assumere un'avanzata dello spazio aggiuntivo dello schermo, quindi il contenuto deve espandersi di conseguenza offrendo più spazio agli elementi dell'interfaccia utente che ne hanno bisogno. Windows con contenuto dinamico, documenti, immagini, elenchi e alberi traggono il massimo vantaggio dalle finestre ridimensionabili.

![Screenshot del controllo ridimensionato che riceve la barra di scorrimento ](images/vis-layout-image12.png)

In questo esempio il ridimensionamento della finestra ridimensiona il controllo visualizzazione elenco.

Detto questo, le finestre possono essere distese troppo larghe. Ad esempio, molte pagine del pannello di controllo diventano ingombrhe quando il contenuto è più ampio di 600 pixel relativi. In questo caso, è meglio non ridimensionare l'area del contenuto oltre questa larghezza massima o modificare l'origine del contenuto quando la finestra viene ridimensionata ingrandita. Mantenere invece una larghezza massima e un'origine fissa in alto a sinistra.

Il testo diventa difficile da leggere con l'aumentare della lunghezza della riga. Per i documenti di testo, prendere in considerazione una lunghezza massima di riga di 80 caratteri per semplificare la lettura del testo. I caratteri includono lettere, punteggiatura e spazi.

**Non corretto:**

![Screenshot della finestra di messaggio wide con testo lungo ](images/vis-layout-image13.png)

In questo esempio, la lunghezza lunga del testo rende difficile la lettura.

Infine, le finestre ridimensionabili devono anche usare in modo efficace lo spazio dello schermo quando vengono ridotte, rendendo più piccolo il contenuto ridimensionabile e rimuovendo lo spazio dagli elementi dell'interfaccia utente che possono funzionare in modo efficace senza di esso. A un certo punto, la finestra o i relativi elementi dell'interfaccia utente diventano troppo piccoli per essere utilizzabili, quindi è consigliabile assegnare loro una dimensione minima o rimuovere completamente alcuni elementi.

![Screenshot della finestra con barra multifunzione alta e intrusiva ](images/vis-layout-image14.png)

![Screenshot della finestra senza barra multifunzione ](images/vis-layout-image15.png)

In questo esempio, le dimensioni del riquadro sono minime.

Alcuni programmi traggono vantaggio dall'uso di una presentazione completamente diversa per rendere il contenuto utilizzabile a dimensioni più piccole.

![Screenshot dei pulsanti del lettore multimediale centrato ](images/vis-layout-image16.png)

In questo esempio, Windows Media Player modifica il formato quando la finestra diventa troppo piccola per il formato standard.

### <a name="focus"></a>Focus

Un layout ha lo stato attivo quando c'è un punto ovvio in cui guardare per primo. Lo stato attivo è importante per mostrare agli utenti dove iniziare a analizzare la finestra o la pagina. Senza una chiara messa a fuoco, l'occhio dell'utente si aggira senza mira. Il punto focale deve essere qualcosa di importante che gli utenti devono trovare e comprendere rapidamente e deve avere la massima enfasi visiva. L'angolo superiore sinistro è il punto focale naturale per la maggior parte delle finestre.

Deve essere presente un solo punto focale. Proprio come nella vita reale, l'occhio può concentrarsi su una sola cosa alla volta, gli utenti non possono concentrarsi su più posizioni contemporaneamente.

Per impostare un elemento dell'interfaccia utente come punto focale, è possibile assegnargli un'enfasi visiva:

-   Posizionarlo nella parte superiore sinistra o superiore centrale della superficie.
-   Uso di controlli interattivi importanti e facilmente comprensibili.
-   Uso di testo prominente, ad esempio un'istruzione principale.
-   Fornire ai controlli la selezione predefinita e lo stato attivo per l'input iniziale.
-   Posizionamento dei controlli su uno sfondo colorato diverso.

Provare Windows ricerca. Il punto focale per Windows ricerca deve essere la casella Cerca perché è il punto di partenza per l'attività. Tuttavia, si trova nell'angolo superiore destro per essere coerente con il posizionamento standard della casella di ricerca. La casella Di ricerca ha lo stato attivo per l'input, ma data la posizione nel percorso di analisi, l'indicazione da sola non è sufficiente.

Per risolvere questo problema, nella parte superiore centrale della finestra sono presenti istruzioni importanti per indirizzare gli utenti alla posizione corretta.

**Accettabile:**

![Screenshot della finestra di dialogo di ricerca con testo utile ](images/vis-layout-image17.png)

In questo esempio, un'istruzione importante nella parte superiore centrale della finestra indirizza gli utenti alla casella di ricerca.

Senza le istruzioni, la finestra non avrebbe un punto focale ovvio.

**Non corretto:**

![Screenshot della finestra di dialogo di ricerca senza testo ](images/vis-layout-image18.png)

Questo esempio non presenta alcun punto focale ovvio. Gli utenti non sanno dove cercare.

Se si assegna un'enfasi visiva agli elementi dell'interfaccia utente, assicurarsi che l'attenzione sia garantita. Nell'esempio precedente Windows Ricerca, il pulsante Tutti evidenziato si trova nell'angolo superiore sinistro e ha maggiore enfasi visiva, ma non è il punto focale previsto. Gli utenti potrebbero rimanere bloccati a guardare questo pulsante per capire come procedere.

**Non corretto:**

![Screenshot del pulsante Evidenziato tutto ](images/vis-layout-image19.png)

Senza l'istruzione principale come punto focale, il pulsante Tutti evidenziato è un punto focale non intenzionale.

### <a name="flow"></a>Flusso

Un layout ha un flusso quando gli utenti sono guidati in modo uniforme e naturale da un percorso chiaro attraverso la superficie, trovando gli elementi dell'interfaccia utente nell'ordine appropriato per l'uso. Dopo aver identificato il punto focale, gli utenti devono determinare come completare l'attività. La posizione degli elementi dell'interfaccia utente indica la relazione e deve rispecchiare i passaggi per eseguire l'attività. In genere, ciò significa che i passaggi dell'attività devono scorrere naturalmente in un ordine dall'alto verso destra e dall'alto verso il basso (nelle impostazioni cultura occidentali).

Si sa che un layout ha un flusso positivo quando:

-   La posizione degli elementi dell'interfaccia utente rispecchia i passaggi necessari agli utenti per eseguire l'attività.
-   Gli elementi dell'interfaccia utente che avviano un'attività sono nell'angolo superiore sinistro o in alto al centro.
-   Gli elementi dell'interfaccia utente che completano un'attività sono nell'angolo inferiore destro.
-   Gli elementi correlati dell'interfaccia utente sono insieme. gli elementi non correlati sono separati.
-   I passaggi necessari sono nel flusso principale.
-   I passaggi facoltativi sono al di fuori del flusso principale, possibilmente de-evidenziati usando un background appropriato o una divulgazione progressiva.
-   Gli elementi usati di frequente vengono visualizzati prima degli elementi usati raramente nel percorso di analisi.
-   Gli utenti sanno sempre cosa fare dopo. Non sono presenti salti o interruzioni impreviste nel flusso di attività.

**Non corretto:**

![Screenshot del layout della finestra di dialogo confusa ](images/vis-layout-image20.png)

In questo esempio gli utenti non sanno come procedere. Si verificano salti e interruzioni impreviste nel flusso di attività.

**Corretto:**

![Screenshot di una finestra di dialogo ben pianificata ](images/vis-layout-image21.png)

In questo esempio la presentazione degli elementi dell'interfaccia utente rispecchia i passaggi per eseguire l'attività.

### <a name="grouping"></a>Raggruppamento

Un layout ha un raggruppamento quando gli elementi dell'interfaccia utente correlati logicamente hanno una relazione visiva chiara. I gruppi sono importanti perché è più facile per gli utenti comprendere e concentrarsi su un gruppo di elementi correlati rispetto agli elementi singolarmente. I gruppi rendono un layout più semplice e più facile da analizzare.

È possibile visualizzare il raggruppamento nei modi seguenti (aumentando la pesantezza):

-   **Layout.** È possibile raggruppare i controlli correlati uno accanto all'altro e inserire ulteriore spaziatura tra i controlli non correlati.

    ![Figura di quattro icone che mostrano quattro gruppi di attività ](images/vis-layout-image22.png)

    In questo esempio viene usato solo il layout per mostrare le relazioni tra i controlli.

-   **Separatori.** Un separatore è una linea orizzontale o verticale che unifica un gruppo di controlli. I separatori offrono un aspetto più semplice e pulito. Tuttavia, a differenza delle caselle di gruppo, funzionano meglio quando si estendono su tutta la superficie.

    ![Screenshot di tre icone e tre separatori ](images/vis-layout-image23.png)

    In questo esempio i separatori etichettati vengono usati per mostrare le relazioni tra i controlli.

-   **Aggregatori.** Un aggregatore è un elemento grafico che crea una relazione visiva tra controlli strettamente correlati.

    ![Screenshot dei controlli all'interno di una linea ellittica ](images/vis-layout-image24.png)

    In questo esempio viene usato un aggregatore di limiti per evidenziare la relazione tra i controlli e renderli come un singolo controllo anziché otto.

-   **Caselle di gruppo.** Una casella di gruppo è una cornice rettangolare etichettata che circonda un set di controlli correlati.

    ![Screenshot delle caselle di controllo in un bordo rettangolare ](images/vis-layout-image25.png)

    In questo esempio, una casella di gruppo racchiude ed etichetta un set di controlli correlati.

-   **Sfondi.** È possibile usare gli sfondi per evidenziare o rimuovere l'enfasi di diversi tipi di contenuto.

    ![Screenshot del lato sinistro del pannello di controllo ](images/vis-layout-image26.png)

    In questo esempio il riquadro attività del Pannello di controllo viene usato per raggruppare le attività correlate e gli elementi del Pannello di controllo.

    Per evitare confusione visiva, il raggruppamento del peso più leggero che esegue il processo è la scelta migliore. Per altre informazioni, vedere [Caselle di gruppo,](ctrl-group-boxes.md) [schede,](ctrl-tabs.md) [separatori e sfondi.](vis-graphic.md)

Indipendentemente dal tipo di raggruppamento, è possibile usare il rientro per visualizzare la relazione dei controlli all'interno di un gruppo. I controlli che sono peer tra loro devono essere allineati a sinistra e i controlli dipendenti devono essere rientrati di 12 DLO o 18 pixel relativi.

![Screenshot di tre livelli di controlli rientrati ](images/vis-layout-image27.png)

I controlli dipendenti sono rientrati di 12 DLUS o 18 pixel relativi, che per impostazione predefinita è la distanza tra le caselle di controllo e i pulsanti di opzione dalle relative etichette.

Si sa che un layout ha un buon raggruppamento quando:

-   La finestra o le pagine hanno al massimo 7 gruppi.
-   Lo scopo di ogni gruppo è ovvio.
-   La relazione dei controlli all'interno di ogni gruppo è ovvia, in particolare la dipendenza del controllo.
-   Il raggruppamento semplifica il contenuto anziché renderlo più complesso.

### <a name="alignment"></a>Allineamento

L'allineamento è la posizione coordinata degli elementi dell'interfaccia utente. L'allineamento è importante perché semplifica l'analisi del contenuto e influisce sulla percezione della complessità visiva degli utenti.

Quando si determina l'allineamento, è necessario prendere in considerazione diversi obiettivi:

-   **Facilità di analisi orizzontale.** Gli utenti possono leggere orizzontalmente e trovare gli elementi correlati uno accanto all'altro, senza lacune difficili.
-   **Facilità di analisi verticale.** Gli utenti possono analizzare colonne di elementi correlati e trovare immediatamente ciò che cercano, con un minimo movimento orizzontale degli occhi.
-   **Complessità visiva minima.** Gli utenti percepiranno un layout visivamente complesso se ha linee griglia di allineamento verticale non necessarie.

### <a name="horizontal-alignment"></a>Allineamento orizzontale

**Allineamento a sinistra**

A causa dell'ordine di lettura da sinistra a destra, l'allineamento a sinistra funziona correttamente per la maggior parte del contenuto. L'allineamento a sinistra semplifica l'analisi verticale dei dati a colonne.

**Allineamento a destra**

L'allineamento a destra è la scelta migliore per i dati numerici, in [particolare le colonne di dati numerici.](ctrl-text-boxes.md) L'allineamento a destra funziona anche per [i pulsanti di commit](glossary.md) e i controlli allineati al bordo destro della finestra.

![Screenshot del pulsante con la freccia GIÙ della ricerca avanzata ](images/vis-layout-image28.png)

In questo esempio, il controllo di divulgazione progressiva ricerca avanzata è allineato a destra perché viene posizionato sul bordo destro della finestra.

**Allineamento al centro**

L'allineamento al centro è ideale per le situazioni in cui l'allineamento a sinistra o a destra non è appropriato o risulta non bilanciato.

![Screenshot dei controlli del lettore multimediale centrato ](images/vis-layout-image29.png)

In questo esempio il controllo lettore multimediale è centrato per ottenere un aspetto bilanciato.

Non centrare il contenuto della finestra solo per riempire lo spazio.

**Non corretto:**

![Screenshot di una finestra con troppo spazio vuoto ](images/vis-layout-image30.png)

In questo esempio il contenuto viene centrato in modo errato in una finestra ridimensionabile per riempire lo spazio.

### <a name="vertical-alignment"></a>Allineamento verticale

**Elementi all'inizio**

A causa dell'ordine di lettura dall'alto verso il basso, l'allineamento superiore funziona bene per la maggior parte del contenuto. L'allineamento superiore semplifica l'analisi orizzontale degli elementi dell'interfaccia utente.

**Linee di base del testo**

Quando si allineano verticalmente i controlli al testo, allineare le linee di base del testo per ottenere un flusso di lettura orizzontale uniforme.

**Corretto:**

![Screenshot del pulsante e del testo dell'etichetta allineati ](images/vis-layout-image31.png)

**Non corretto:**

![Screenshot del pulsante e del testo dell'etichetta non allineati ](images/vis-layout-image32.png)

Nell'esempio corretto, il controllo e la relativa etichetta sono allineati verticalmente in base alle linee di base del testo.

Si sa che un layout ha un buon allineamento quando:

-   È facile analizzare sia orizzontalmente che verticalmente.
-   Ha un aspetto visivo semplice.

### <a name="label-alignment"></a>Allineamento delle etichette

Le regole di allineamento generali si applicano alle etichette di controllo, ma si tratta di un problema comune che merita un'attenzione specifica. L'allineamento delle etichette ha gli obiettivi seguenti:

-   Facilità di analisi verticale per trovare il controllo giusto.
-   Facilità di analisi orizzontale per associare etichette ai relativi controlli.
-   Facilità di localizzazione, gestione delle etichette che differiscono per lunghezza tra lingue diverse.
-   Funziona bene con una combinazione di diverse lunghezze di etichetta.
-   Consente un uso efficiente dello spazio disponibile evitando il testo troncato.

L'obiettivo generale è ridurre la quantità di movimento oculare necessaria per trovare ciò che probabilmente gli utenti cercano, ma la natura dei controlli e ciò che gli utenti stanno cercando dipende dal contesto.

Esistono quattro stili comuni di posizionamento e allineamento delle etichette, ognuno con i relativi vantaggi:

-   Etichette giustificate a sinistra sopra i controlli
-   Etichette giustificate a sinistra a sinistra dei controlli
-   Etichette giustificate a sinistra a sinistra dei controlli, controlli instagliati a sinistra
-   Etichette giustificate a destra a sinistra dei controlli

**Etichette giustificate a sinistra sopra i controlli**

Questo stile è il più semplice da localizzare perché il layout non dipende dalla lunghezza delle etichette, ma richiede lo spazio più verticale.

![elenco con due colonne di etichette sopra i controlli ](images/vis-layout-image33.png)

Questo stile occupa lo spazio più verticale, ma è più semplice da localizzare. È una scelta migliore per l'etichettatura dei controlli principalmente interattivi.

È la soluzione più adatta quando:

-   I controlli etichettati sono interattivi (non solo testo).
-   L'interfaccia utente verrà localizzata. Questo stile offre spesso spazio per raddoppiare o addirittura triplicare la lunghezza dell'etichetta.
-   L'interfaccia utente usa una tecnologia di layout fisso, ad esempio Win32.
-   Sono disponibili dieci o meno controlli. Con più controlli, le etichette sono difficili da analizzare.
-   Lo spazio verticale è sufficiente per contenere le etichette.
-   Il layout deve essere in formato libero, non solo colonne.

**Etichette giustificate a sinistra a sinistra dei controlli**

Questo stile è il più semplice da analizzare in verticale e funziona anche quando le etichette differiscono notevolmente per lunghezza, ma è più difficile associare l'etichetta al relativo controllo. Questo stile può usare etichette su più righe, se necessario.

![elenco con quattro colonne di etichette a sinistra dei controlli ](images/vis-layout-image34.png)

Questo stile funziona correttamente. Tuttavia, sono presenti due colonne, ma visivamente sembra che siano presenti quattro colonne per rendere i dati più complessi.

È la soluzione più adatta quando:

-   È probabile che gli utenti eseereranno la scansione in verticale per trovare etichette specifiche.
-   È probabile che gli utenti leggono le etichette e i controlli in modo da sinistra a destra, dall'alto verso il basso.
-   Lo spazio orizzontale è sufficiente per contenere le etichette.
-   La lunghezza delle etichette varia in modo significativo.
-   Sono disponibili molti controlli, ad esempio con i form.
-   Sono presenti poche colonne. Visivamente le etichette e i controlli vengono visualizzati come due singole colonne.

**Etichette giustificate a sinistra a sinistra dei controlli, controlli instagliati a sinistra**

Questo stile semplifica l'analisi verticale delle etichette e delle etichette e dei controlli in orizzontale ed è molto efficiente in termini di spazio. ma è più difficile analizzare i controlli verticalmente. I controlli sono giustificati a destra per sfruttare al meglio lo spazio disponibile.

![elenco di due colonne di etichette con controlli non ancorati ](images/vis-layout-image35.png)

Questo stile è compatto e facile da leggere, ma è difficile analizzare i controlli verticalmente.

È la soluzione più adatta quando:

-   L'interfaccia utente usa una tecnologia di layout variabile (ad esempio Windows Presentation Foundation).
-   È probabile che gli utenti eseereranno la scansione in verticale per trovare etichette specifiche.
-   È probabile che gli utenti leggono le etichette e i controlli da sinistra a destra, dall'alto verso il basso.
-   Gli utenti probabilmente non analizzano i controlli verticalmente.
-   Il testo del controllo varia di lunghezza e potrebbe essere troncato se fosse stato usato un altro stile.
-   I controlli sono di sola lettura, ad esempio caselle di testo di sola lettura. Per gli altri controlli, questo allineamento avrà un aspetto sloppy. Tuttavia, i controlli possono diventare modificabili quando si fa clic.
-   Sono presenti molte colonne, ma alcuni controlli in una colonna.

**Etichette giustificate a destra a sinistra dei controlli**

Questo stile è il più semplice da leggere orizzontalmente per associare le etichette ai relativi controlli, ma è difficile analizzare le etichette verticalmente e non funziona correttamente quando labelsList con etichette e controlli rientrati differisce notevolmente per lunghezza.

![elenco con etichette e controlli rientrati ](images/vis-layout-image36.png)

Questo stile consente di analizzare facilmente i controlli verticalmente, ma rende difficile l'analisi verticale delle etichette.

L'uso ottimale è quando:

-   È probabile che gli utenti leggono le etichette e i controlli in modo da sinistra a destra, dall'alto verso il basso.
-   È probabile che gli utenti non esereranno la scansione in verticale per trovare etichette specifiche, probabilmente perché:
    -   Sono disponibili pochi controlli.
    -   Le etichette sono note.
    -   I controlli sono per lo più auto-esplicativi e raramente sono vuoti (possibilmente con valori predefiniti per evitare controlli vuoti).
-   Lo spazio orizzontale disponibile è sufficiente per contenere le etichette.
-   La lunghezza delle etichette non varia in modo significativo.
-   Sono presenti molte colonne. Visivamente le etichette e i controlli vengono visualizzati come una singola colonna.

Prima di adottare uno di questi stili, tuttavia, considerare altri due fattori:

-   Preferire uno stile che è possibile usare in modo coerente in tutto il programma.
-   Le etichette giustificate a sinistra sopra i controlli a sinistra dei controlli sono gli stili più comuni, pertanto è consigliabile scegliere tra loro.

### <a name="balance"></a>Balance

Una finestra o una pagina ha un bilanciamento quando il contenuto viene visualizzato uniformemente distribuito sulla superficie. Se la superficie fisicamente ha la stessa ponderazione che ha visivamente, un layout bilanciato non si distolerebbe su un lato.

Il problema di bilanciamento più comune è la presenza di una quantità di contenuto troppo grande sul lato sinistro di una finestra o di una pagina. È possibile creare un saldo nei modi seguenti:

-   Uso di margini maggiori sul lato sinistro rispetto a destra.
-   Posizionamento degli elementi dell'interfaccia utente usati per completare un'attività a destra.
-   Posizionare al centro gli elementi dell'interfaccia utente usati in tutta l'attività.
-   Estensione dei controlli ridimensionabili o su più righe.
-   Uso strategico dell'allineamento al centro.

![screenshot della stampante a sinistra e del testo a destra ](images/vis-layout-image37.png)

Questo layout di pagina della procedura guidata ben bilanciato mostra un margine sinistro maggiore rispetto a destra per migliorare il bilanciamento.

Se queste tecniche non hanno un equilibrio, provare a ridurre la larghezza della finestra o della pagina in modo che corrisponda meglio al relativo contenuto.

Per le superfici ridimensionabili, non centrare il contenuto solo per ottenere l'equilibrio. Mantenere invece un'origine fissa in alto a sinistra, definire una superficie di attacco massima e bilanciare il contenuto all'interno dello spazio usato.

### <a name="grids"></a>Griglie

Una griglia è un sistema di allineamento sottostante invisibile. Le griglie possono essere simmetriche, ma funzionano anche le griglie asimmetriche. Se usate da una singola finestra o pagina, le griglie consentono di organizzare il contenuto all'interno di una superficie. Quando vengono riutilizzate, le griglie creano un layout coerente tra le superfici.

Il numero di linee della griglia influisce sulla percezione della complessità visiva. Un layout con meno linee della griglia risulta più semplice di un layout con più linee griglia.

**Visivamente complesso:**

![Screenshot della finestra di dialogo ingombrata ](images/vis-layout-image38.png)

**Visivamente semplice:**

![Screenshot della finestra di dialogo organizzata ](images/vis-layout-image39.png)

Le linee griglia non necessarie creano complessità visiva.

Si sa che un layout usa le griglie in modo efficace quando:

-   Windows o le pagine con contenuto o funzione simili hanno un layout simile.
-   Gli elementi di progettazione ripetuti vengono visualizzati in posizioni simili nelle finestre e nelle pagine.
-   Non sono presenti linee griglia di allineamento orizzontale e verticale non necessarie.

### <a name="visual-simplicity"></a>Semplicità visiva

La semplicità visiva è la percezione che un layout non sia più complicato di quanto sia necessario.

Si sa che un layout ha una semplicità visiva quando:

-   Elimina i livelli non necessari del colore della finestra.
-   Presenta il contenuto usando al massimo sette gruppi facilmente identificabili.
-   Usa il raggruppamento leggero, ad esempio layout e separatori anziché caselle di gruppo.
-   Usa controlli leggeri, ad esempio collegamenti anziché pulsanti di comando per i comandi secondari, ed elenchi a discesa anziché elenchi per le scelte.
-   Riduce il numero di linee griglia di allineamento verticale e orizzontale.
-   Riduce il numero di dimensioni dei controlli, ad esempio usando una o due larghezze di uno o due pulsanti di comando su una superficie.
-   Usa la divulgazione progressiva per nascondere gli elementi dell'interfaccia utente fino a quando non sono necessari.
-   Usa spazio sufficiente in modo che la finestra o la pagina non si senta invasa.
-   Ridimensiona le finestre e i controlli in modo appropriato per eliminare lo scorrimento non necessario.
-   Usa un singolo tipo di carattere con un numero ridotto di dimensioni e colori del testo.

Come regola generale, se un elemento di layout può essere eliminato senza danneggiare l'efficacia dell'interfaccia utente, probabilmente dovrebbe farlo.

## <a name="guidelines"></a>Indicazioni

### <a name="screen-resolution-and-dpi"></a>Risoluzione dello schermo e dpi

-   **Supporta la risoluzione effettiva Windows minima di 800x600 pixel.** Per le ui critiche che devono funzionare in modalità sicura, supportare una risoluzione effettiva di 640x480 pixel. Assicurarsi di fare attenzione allo spazio usato dalla barra delle [](glossary.md) applicazioni riservando 48 pixel relativi verticali per le finestre visualizzate con la barra delle applicazioni.
-   **Ottimizzare i layout delle finestre ridimensionabili per una risoluzione effettiva di 1024x768 pixel.** Ridimensionare automaticamente queste finestre per le risoluzioni dello schermo inferiori in modo che sia ancora funzionante.
-   **Assicurarsi di testare le finestre in modalità 96 punti per pollice (dpi) (a 800x600 pixel), 120 dpi (a 1024 x 768 pixel) e 144 dpi (a 1200x900 pixel).** Verificare la presenza di problemi di layout, ad esempio il ritaglio di controlli, testo e finestre e l'estensione di icone e bitmap.
-   **Per i programmi con scenari di uso tocco e per dispositivi mobili, ottimizzare per 120 dpi.** Gli schermi con valori dpi alti sono attualmente prevalenti nei PC a tocco e per dispositivi mobili.

### <a name="window-size"></a>Dimensioni finestra

-   **Scegliere le dimensioni predefinite della finestra appropriate per il relativo contenuto.** Se è possibile usare lo spazio in modo efficace, non è necessario usare dimensioni di finestra iniziali maggiori.
-   **Usare proporzioni bilanciate tra altezza e larghezza.** È preferibile usare proporzioni tra 3:5 e 5:3, anche se è possibile usare proporzioni di 1:3 per le finestre di dialogo dei messaggi, ad esempio errori e avvisi.
-   **Usare finestre ridimensionabili quando possibile per evitare barre di scorrimento e dati troncati.** Windows con contenuto dinamico, documenti, immagini, elenchi e alberi traggono il massimo vantaggio dalle finestre ridimensionabili.
-   **Per i documenti di testo, prendere in** considerazione una lunghezza massima di riga di 80 caratteri per semplificare la lettura del testo. I caratteri includono lettere, punteggiatura e spazi.
-   Finestre a dimensione fissa:
    -   **Le finestre a dimensione fissa devono essere completamente visibili e ridimensionate per adattarsi all'area di lavoro.**
-   Finestre ridimensionabili:
    -   **Le finestre ridimensionabili possono essere ottimizzate per risoluzioni più elevate, ma ridimensionate in base alle esigenze in fase di visualizzazione fino alla risoluzione effettiva dello schermo.**
    -   **Le dimensioni delle finestre progressivamente più grandi devono mostrare informazioni sempre più dettagliate.** Assicurarsi che almeno una parte della finestra o un controllo abbia contenuto ridimensionabile.
    -   **Mantenere fissa l'origine superiore sinistra del contenuto quando la finestra viene ridimensionata.** Non spostare l'origine per bilanciare il contenuto quando cambiano le dimensioni della finestra.
    -   **Impostare le dimensioni massime del contenuto se il contenuto può essere troppo grande.** Se il contenuto diventa ingombrante, non ridimensionare l'area del contenuto oltre la larghezza massima o modificare l'origine del contenuto quando la finestra viene ridimensionata ingrandita. Mantenere invece una larghezza massima e un'origine fissa in alto a sinistra.
    -   **Impostare una dimensione minima della finestra se è presente una dimensione inferiore alla quale il contenuto non è più utilizzabile.** Per i controlli ridimensionabili, impostare le dimensioni minime degli elementi ridimensionabili sulle dimensioni funzionali più piccole, ad esempio la larghezza minima delle colonne funzionali nelle visualizzazioni elenco. Gli elementi facoltativi dell'interfaccia utente devono essere rimossi completamente.
    -   **Valutare la possibilità di modificare la presentazione per rendere il contenuto utilizzabile in dimensioni più piccole.**

        ![Screenshot dei controlli lettore multimediale ](images/vis-layout-image16.png)

        In questo esempio, Windows Media Player il formato quando la finestra diventa troppo piccola per il formato standard.

### <a name="control-size"></a>Dimensioni del controllo

-   **Impostare tutti i controlli interattivi almeno su 16 x 16 pixel relativi.** Questa operazione funziona bene per tutti i dispositivi di input, incluso Tecnologia Windows per Tablet PC.
-   **Ridimensiona i controlli per evitare dati troncati.** Non troncare i dati che devono essere letti per eseguire un'attività. Ridimensionare le colonne della visualizzazione elenco per evitare dati troncati.
-   **Ridimensionare i controlli per eliminare lo scorrimento non necessario.** Se si rende leggermente più grandi i controlli, questa operazione elimina una barra di scorrimento. Dovrebbero essere presenti poche barre di scorrimento verticali e nessuna barra di scorrimento orizzontale non necessaria.

    ![Screenshot dell'elenco ridimensionato per evitare una barra di scorrimento ](images/vis-layout-image40.png)

    In questo esempio l'elenco a discesa viene ridimensionato per eliminare la barra di scorrimento.

-   **Ridurre il numero di dimensioni di controllo su una superficie.** Preferire l'uso [delle dimensioni di controllo consigliate standard](#recommended-sizing-and-spacing) e, se necessario, usare alcuni controlli più grandi o più piccoli di dimensioni coerenti. Provare a usare una singola larghezza per le caselle di riepilogo e le visualizzazioni albero e non più di tre larghezze per i pulsanti di comando e gli elenchi a discesa. Tuttavia, la larghezza della casella di testo e della casella combinata dovrebbe suggerire la lunghezza dell'input più lungo o previsto.

    ![Screenshot della finestra di dialogo con elenchi e pulsanti ](images/vis-layout-image41.png)

    In questo esempio vengono usate in modo coerente una casella di riepilogo e le dimensioni del pulsante di comando.

-   **Per i controlli ridimensionati in base al testo, includere un ulteriore 30% (fino al 200% per il testo più breve) per qualsiasi testo che verrà localizzato.** Questa linea guida presuppone che il layout sia progettato usando testo in inglese. Si noti anche che questa linea guida si riferisce al testo localizzato, non ai numeri.
-   **Estendere i controlli di testo statici, le caselle di controllo e i pulsanti di opzione fino alla larghezza massima che verrà adattata al layout.** In questo modo si evita il troncamento dal testo a lunghezza variabile e dalla localizzazione.

    **Non corretto:**

    ![Screenshot del controllo di stato e del testo parziale ](images/vis-layout-image42.png)

    In questo esempio il testo del controllo viene troncato inutilmente.

### <a name="control-spacing"></a>Spaziatura dei controlli

-   **Se i controlli non vengono toccati, hanno almeno 3 DLU (5 pixel relativi) di spazio tra di essi.** In caso contrario, gli utenti possono fare clic sullo spazio inattivo tra i controlli. Poiché fare clic su spazio inattivo non ha alcun risultato o feedback visivo, gli utenti sono spesso incerti su cosa sia andato storto.

### <a name="placement"></a>Selezione host

-   **Disporre gli elementi dell'interfaccia utente all'interno di una superficie in modo che scorrono naturalmente in ordine da sinistra a destra, dall'alto verso il basso (nelle impostazioni cultura occidentali).** La posizione degli elementi dell'interfaccia utente comunica la relazione e deve rispecchiare i passaggi per eseguire l'attività.
-   **Posizionare gli elementi dell'interfaccia utente che avviano un'attività nell'angolo superiore sinistro o in alto al centro.** Assegnare all'elemento dell'interfaccia utente che gli utenti devono esaminare prima di tutto la massima enfasi visiva.
-   **Posizionare gli elementi dell'interfaccia utente che completano un'attività nell'angolo inferiore destro.**
-   **Inserire gli elementi correlati dell'interfaccia utente e separare gli elementi non correlati.**
-   **Inserire i passaggi necessari nel flusso principale.**
-   **Posizionare i passaggi facoltativi all'esterno** del flusso principale, possibilmente de-sottolineati usando uno sfondo appropriato o una diffusione progressiva.
-   **Posizionare gli elementi usati di frequente prima degli** elementi usati raramente nel percorso di analisi.

### <a name="focus"></a>Focus

-   **Scegliere un singolo elemento dell'interfaccia utente che gli utenti devono prima esaminare come punto focale.** Il punto focale deve essere qualcosa di importante che gli utenti devono trovare e comprendere rapidamente.
-   **Posizionare il punto focale nell'angolo superiore sinistro o in alto al centro.**
-   **Assegnare al punto focale la massima enfasi visiva,** ad esempio testo prominente, selezione predefinita o stato attivo di input iniziale.

### <a name="alignment"></a>Allineamento

-   In genere, usare l'allineamento a sinistra.
-   Usare l'allineamento a destra per i dati numerici, in particolare le colonne di dati numerici.
-   Usare l'allineamento a destra per i pulsanti di commit, nonché i controlli allineati al bordo destro della finestra.
-   Usare l'allineamento al centro quando l'allineamento a sinistra o a destra non è appropriato o risulta non bilanciato.
-   Quando si allineano verticalmente i controlli al testo, allineare le linee di base del testo per ottenere un flusso di lettura orizzontale uniforme.
-   Per l'allineamento delle etichette, vedere la [sezione Allineamento etichetta](#label-alignment) in Concetti di progettazione.

### <a name="accessibility"></a>Accessibilità

-   **Non usare il layout come unico mezzo per trasmettere informazioni importanti su un'interfaccia utente.** Gli utenti con problemi visivi potrebbero non essere in grado di interpretare questa presentazione. Ad esempio, assicurarsi che le etichette dei controlli comunichino la relazione con altri elementi.
-   **Non incorporare controlli subordinati all'interno delle etichette di controllo per creare una frase o una frase.** Queste associazioni si basano esclusivamente sul layout e non vengono gestite correttamente dalla navigazione tramite tastiera o dalle tecnologie di accessibilità assistive. Inoltre, questa tecnica non è localizzabile perché la struttura delle frasi varia in base alla lingua.

    **Non corretto:**

    ![Screenshot di una casella di testo al centro di una frase ](images/vis-layout-image43.png)

    In questo esempio la casella di testo viene inserita in modo non corretto all'interno dell'etichetta della casella di controllo.

    **Corretto:**

    ![Screenshot di una casella di testo alla fine di una frase ](images/vis-layout-image44.png)

    In questo caso, la casella di testo viene posizionata dopo l'etichetta della casella di controllo.

-   **Rendere accessibile il raggruppamento.** I gruppi definiti da riquadri finestra, caselle di gruppo, separatori, etichette di testo e aggregatori vengono gestiti automaticamente dagli strumenti di accessibilità. Tuttavia, i gruppi definiti solo dal posizionamento e dagli sfondi non lo sono e devono essere definiti a livello di codice per l'accessibilità.

Per altre linee guida, vedere [Accessibilità](inter-accessibility.md).

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

**Ridimensionamento dei controlli**

La tabella seguente elenca le dimensioni consigliate (larghezza x altezza o altezza se un singolo numero) per gli elementi comuni dell'interfaccia utente (per 9 pt. Segoe UI a 96 dpi). Le larghezze basate sull'elemento più lungo in inglese aggiungono il 30% per la localizzazione (fino al 200% per il testo più breve) per qualsiasi testo (ma non numeri) che verrà localizzato.



| Esempio | Control | Unità di dialogo | Pixel relativi |
|-------------------------------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| ![Screenshot delle caselle di controllo e delle relative etichette ](images/vis-layout-image45.png)<br/>       | Caselle di controllo<br/>     | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![Screenshot della casella combinata ](images/vis-layout-image46.png)<br/>                          | Caselle combinate<br/>     | larghezza dell'elemento più lungo + 30% x 14<br/>                                                       | larghezza dell'elemento più lungo + 30% x 23<br/>                                                                |
| ![Screenshot di un pulsante di comando ](images/vis-layout-image47.png)<br/>                   | Pulsanti di comando<br/> | 50 x 14<br/>                                                                                | 75 x 23<br/>                                                                                         |
| ![Screenshot di uno dei due collegamenti di comando selezionati ](images/vis-layout-image48.png)<br/>  | Collegamenti ai comandi<br/>   | 25 (una riga) o 35 (due righe)<br/>                                                        | 41 (una riga) o 58 (due righe)<br/>                                                                 |
| ![Screenshot di un elenco a discesa ](images/vis-layout-image49.png)<br/>                   | Elenchi a discesa<br/> | larghezza dei dati validi più lunghi + 30% x 14<br/>                                                 | larghezza dell'elemento più lungo + 30% x 23<br/>                                                                |
| ![Screenshot di una casella di riepilogo ](images/vis-layout-image50.png)<br/>                         | Caselle di riepilogo<br/>      | larghezza dell'elemento più lungo + 30% x un numero integrale di elementi (minimo 3 elementi)<br/>            |                                                                                                            |
| ![Screenshot di un elenco di file di immagine ](images/vis-layout-image51.png)<br/>            | Visualizzazioni elenco<br/>      | larghezze delle colonne che evitano i dati troncati x un numero integrale di elementi<br/>                 |                                                                                                            |
| ![Screenshot di un indicatore di stato ](images/vis-layout-image52.png)<br/>                     | Barre di stato<br/>   | 107 o 237 x 8<br/>                                                                         | 160 o 355 x 15<br/>                                                                                 |
| ![Screenshot dei pulsanti di opzione ](images/vis-layout-image53.png)<br/>                      | Pulsanti di opzione<br/>   | 10<br/>                                                                                     | 17<br/>                                                                                              |
| ![Screenshot del controllo dispositivo di scorrimento ](images/vis-layout-image54.png)<br/>                     | Dispositivi di scorrimento<br/>         | 15<br/>                                                                                     | 24<br/>                                                                                              |
| ![Screenshot del testo: 'select time zone' (Seleziona fuso orario) ](images/vis-layout-image55.png)<br/>           | Testo (statico)<br/>   | 8<br/>                                                                                      | 13<br/>                                                                                              |
| ![Screenshot della casella di testo vuota ](images/vis-layout-image56.png)<br/>                     | Caselle di testo<br/>      | larghezza dell'input più lungo o previsto + 30% x 14 (una riga) + 10 per ogni riga aggiuntiva<br/> | larghezza dei dati validi più lunghi + 30% x 23 pixel relativi (una riga) + 16 per ogni riga aggiuntiva<br/> |
| ![Screenshot delle cartelle annidate in Esplora risorse ](images/vis-layout-image57.png)<br/> | Visualizzazioni albero<br/>      | larghezza dell'elemento più lungo + 30% x un numero integrale di elementi (minimo 5 elementi)<br/>            |                                                                                                            |



 

**Spaziatura**

La tabella seguente elenca la spaziatura consigliata tra gli elementi comuni dell'interfaccia utente (per 9 pt. Segoe UI a 96 dpi).



|   &nbsp; | Elemento | Unità di dialogo | Pixel relativi |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![Immagine che mostra la spaziatura nei margini della finestra di dialogo ](images/vis_layout_image58.jpeg)<br/>        | Margini della finestra di dialogo<br/>                                                                         | 7 su tutti i lati<br/>                                                                 | 11 su tutti i lati<br/>                                                                |
| ![Immagine che mostra la spaziatura tra etichette e controlli ](images/vis_layout_image59.jpeg)<br/>  | Tra le etichette di testo e i controlli associati (ad esempio, caselle di testo e caselle di riepilogo)<br/> | 3<br/>                                                                              | 5<br/>                                                                              |
| ![Immagine che mostra la spaziatura tra i controlli correlati ](images/vis_layout_image60.jpeg)<br/>     | Tra controlli correlati<br/>                                                                   | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Immagine che mostra la spaziatura tra i controlli non correlati ](images/vis_layout_image61.jpeg)<br/>   | Tra controlli non correlati<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
| ![Immagine che mostra la spaziatura del primo controllo in un gruppo ](images/vis_layout_image62.jpeg)<br/>  | Primo controllo in una casella di gruppo<br/>                                                               | 11 verso il basso dalla parte superiore della casella di gruppo; allineare verticalmente al titolo della casella di gruppo<br/> | 16 verso il basso dalla parte superiore della casella di gruppo; allineare verticalmente al titolo della casella di gruppo<br/> |
| ![Aa511279.between-related(en-us,MSDN.10).jpg](images/vis_layout_image60.jpeg)<br/>         | Tra controlli in una casella di gruppo<br/>                                                            | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Immagine che mostra la spaziatura tra i pulsanti ](images/vis_layout_image63.jpeg)<br/>              | Tra pulsanti disposti orizzontalmente o verticalmente<br/>                                        | 4<br/>                                                                              | 7<br/>                                                                              |
| ![Immagine che mostra la spaziatura dell'ultimo controllo in un gruppo ](images/vis_layout_image64.jpeg)<br/>   | Ultimo controllo in una casella di gruppo<br/>                                                                | 7 sopra la parte inferiore della casella di gruppo<br/>                                            | 11 sopra la parte inferiore della casella di gruppo<br/>                                           |
| ![Immagine che mostra la spaziatura dal bordo sinistro della casella di gruppo ](images/vis_layout_image65.jpeg)<br/>  | Dal bordo sinistro di una casella di gruppo<br/>                                                          | 6<br/>                                                                              | 9<br/>                                                                              |
| ![Immagine che mostra la spaziatura dell'etichetta di testo accanto al controllo ](images/vis_layout_image66.jpeg)<br/> | Etichetta di testo accanto a un controllo<br/>                                                                | 3 verso il basso dalla parte superiore del controllo<br/>                                             | 5 verso il basso dalla parte superiore del controllo<br/>                                             |
| ![Immagine che mostra la spaziatura tra paragrafi di testo ](images/vis_layout_image67.jpeg)<br/>   | Tra paragrafi di testo<br/>                                                                 | 7<br/>                                                                              | 11<br/>                                                                             |
|                                                                                                   | Spazio minimo tra i controlli interattivi<br/>                                                | 3 o nessuno spazio<br/>                                                                  | 5 o nessun spazio<br/>                                                                  |
|                                                                                                   | Spazio minimo tra un controllo non interattivo e qualsiasi altro controllo<br/>                     | 2<br/>                                                                              | 3<br/>                                                                              |



 

 

