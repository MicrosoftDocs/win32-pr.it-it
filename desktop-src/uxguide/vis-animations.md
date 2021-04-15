---
title: Animazioni e transizioni
description: L'uso strategico di animazioni e transizioni può rendere il programma più semplice da comprendere, più uniforme, più naturale e di qualità superiore e più accattivante.
ms.assetid: 9e0e9604-f051-47e4-bcd0-59fbfd38b9c1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6d57c696bd78df9c9505bb85453456f10631a00d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104570197"
---
# <a name="animations-and-transitions"></a>Animazioni e transizioni

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

L'uso strategico di animazioni e transizioni può rendere il programma più semplice da comprendere, più uniforme, più naturale e di qualità superiore e più accattivante. Tuttavia, l'uso gratuito di animazioni e transizioni può rendere il programma distrazione e persino fastidioso.

Le animazioni forniscono l'aspetto del movimento o della modifica nel tempo. Usare l'animazione per inviare commenti e suggerimenti, visualizzare in anteprima l'effetto di un'azione, mostrare la relazione tra gli oggetti, attirare l'attenzione sulla modifica o spiegare visivamente un'attività.

![Figura del tastierino numerico con una chiave evidenziata ](images/vis-animations-image1.png)

Microsoft Windows utilizza un'animazione flash in background per fornire commenti e suggerimenti su cui è stato fatto clic sull'oggetto.

Le transizioni sono animazioni usate per consentire agli utenti di essere orientate durante le modifiche dello stato dell'interfaccia utente e le manipolazioni degli oggetti e rendere le modifiche più agevoli anziché stridente. Le transizioni valide hanno un aspetto naturale e spesso offrono l'illusione che gli utenti interagiscono con gli oggetti reali.

![Screenshot che mostra tre dimensioni dei gadget meteorologici.](images/vis-animations-image2.png)

I gadget desktop di Windows usano transizioni uniformi tra i rispettivi stati concisi e dettagli.

In genere, le animazioni e le transizioni migliori vengono usate per comunicare con gli utenti in modo non verbale e per rendere le modifiche dello stato più naturali e meno evidenti. Al contrario, la meno efficace è gratuita perché non comunicano nulla o non richiedono un'attenzione inutile. Le animazioni vengono usate in modo ottimale come forma secondaria di comunicazione. Devono comunicare informazioni utili ma non critiche e, per essere accessibili, gli utenti devono essere in grado di determinare informazioni equivalenti tramite altri mezzi.

**Nota:** Le linee guida relative a [personalizzazione del software](exper-branding.md), [audio](vis-sound.md)e [accessibilità](inter-accessibility.md) sono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendere in considerazione le domande seguenti.

### <a name="animations"></a>Animazioni

Si applicano le condizioni seguenti?

-   L'animazione comunica visivamente un elemento utile, ad esempio l'invio di commenti e suggerimenti, la visualizzazione di relazioni, le cause e gli effetti o l'attenzione a una modifica importante.
-   Vedere l'animazione non è essenziale. Le informazioni equivalenti possono essere ottenute in un altro modo. Gli utenti potrebbero non trarre vantaggio dall'animazione se:
    -   Le animazioni sono state disattivate.
    -   La loro attenzione è altrove.
    -   Sono disaccoppiati visivamente.
    -   L'animazione è nascosta da un'altra finestra.
    -   L'animazione non viene riprodotta a causa di prestazioni di sistema insufficienti.
-   L'animazione non influisce sulla produttività dell'utente. Una delle due versioni seguenti:
    -   Si verifica rapidamente (200 millisecondi o meno).
    -   Non interferisce con l'interazione o può essere interrotta.
    -   L'utente deve comunque attendere.
-   L'animazione non influisce sul flusso dell'utente.
    -   Si tratta di un centro di attenzione dell'utente o richiama l'attenzione di un elemento fuori dal centro dell'attenzione che è importante o utile per il completamento di un'attività.
    -   È facilmente ignorabile, non distrae o fastidioso.
    -   Non diventa noioso. Gli utenti ancora risultano appropriati e piacevoli anche dopo la visualizzazione ripetuta.

In tal caso, prendere in considerazione l'uso di un'animazione.

### <a name="transitions"></a>Transizioni

Si tratta di un oggetto o di una scena che modifica lo stato e si applicano tutte le condizioni indicate sopra per l'utilizzo delle animazioni, nonché di una delle condizioni seguenti?

-   Il cambiamento di stato è concettualmente disorientante, confuso o altrimenti difficile da comprendere.
-   La modifica dello stato è visivamente stridente, manca la continuità o la fluidità o lampeggia; o viene visualizzato non naturale, non lucidato o di scarsa qualità, soprattutto se riguarda un'area dello schermo grande.
-   L'uso di una transizione renderebbe più veloce la modifica dello stato.
-   Il cambiamento di stato è degno di particolare attenzione da parte dell'utente.

In tal caso, prendere in considerazione l'uso di una transizione.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Le animazioni e le transizioni sono un modo efficace per comunicare visivamente le informazioni che richiederebbero altrimenti il testo da spiegare o che potrebbero non essere più disponibili per gli utenti.

**Non corretto:**

![screenshot della finestra di dialogo con messaggio ](images/vis-animations-image3.png)

**Corretto:**

![Figura delle animazioni che comunicano visivamente ](images/vis-animations-image4.png)

L'uso di un'animazione comunica le stesse informazioni, ma in modo naturale e non intrusivo. Quali sarebbero le migliaia di volte?

**Le animazioni e le transizioni non devono richiedere attenzione per avere esito positivo.** Infatti, vengono spesso usati per evitare di attirare l'attenzione sui meccanismi dei programmi che gli utenti non devono essere a conoscenza. Molte animazioni di successo sono così naturali che gli utenti non ne sono consapevoli; piuttosto gli utenti ne noteranno solo la loro assenza. La frequenza di occorrenza aumenta la necessità di sottigliezza, quindi si risparmiano gli effetti che richiedono attenzione per eventi poco frequenti che meritano effettivamente l'attenzione.

![Screenshot di tutti i programmi che cambiano sulla freccia indietro ](images/vis-animations-image5.png)

Una transizione del menu Start che evita di attirare l'attenzione.

Oltre a rendere il programma più semplice da comprendere ed essere più agevole, le **animazioni e le transizioni ben progettate sono un ottimo modo per aggiungere personalità, carattere e stile al programma.** Possono rendere l'esperienza utente più coinvolgente e accattivante, offrendo un ambiente naturale e reale.

![figura che Mostra come il passaggio del mouse influisca sul colore del pulsante ](images/vis-animations-image6.png)

Windows 7 evidenzia i pulsanti della barra delle applicazioni al passaggio del mouse in base alla posizione corrente del mouse e al colore dell'icona del programma Questo approccio è visivamente interessante, ma sottile, che esprime una personalità umile.

**Tuttavia, le animazioni e le transizioni sono più efficaci e benvenuti quando svolgono uno scopo preciso.** Devono essere usati per migliorare l'usabilità, la fluidità e il flusso e la percezione della qualità, senza compromettere significativamente le prestazioni.

Mentre alcuni tipi di animazioni vengono usati per attirare l'attenzione dell'utente, assicurarsi che l'attenzione sia ben deservita e che l'utente interrompa il training del pensiero dell'utente. L'occhio umano è sensibile al movimento, soprattutto al movimento delle periferiche. Può essere difficile per gli utenti concentrarsi quando è presente un pulsante della barra delle applicazioni lampeggiante o un'icona dell'area di notifica rotante. **Evitare di usare le animazioni per interrompere o distrarre gli utenti o attirare l'attenzione su elementi che non garantiscono l'attenzione dell'utente.**

**Non corretto:**

![Figura del pulsante della barra delle applicazioni evidenziato per nessun motivo ](images/vis-animations-image7.png)

I programmi non devono ingrandire il pulsante della barra delle applicazioni, a meno che gli utenti non debbano immediatamente In questo caso, l'unica cosa che l'utente deve fare è attivare il programma.

**Usare animazioni e transizioni perché il programma ne ha bisogno, non solo perché è possibile.** Per l'accessibilità, non usare l'animazione come unico modo per fornire informazioni essenziali. Assicurarsi che gli utenti possano ottenere informazioni equivalenti in modo diverso.

### <a name="attributes-of-good-animations-and-transitions"></a>Attributi di ottime animazioni e transizioni

Le animazioni e le transizioni valide assestano il giusto equilibrio tra questi attributi:

-   **Sono chiaramente intenzionali.** Ci sono ottime animazioni perché devono essere, se comunicare le informazioni, far sentire un'interazione reale o attirare l'attenzione su qualcosa di interessante. E le animazioni con finalità sono accurate; Se un'animazione indica che un'attività è stata eseguita, è perché l'attività è stata effettivamente eseguita.

**Non corretto:**

![screenshot dell'icona della batteria e dell'etichetta con ricarica completa ](images/vis-animations-image8.png)

In questo esempio, l'animazione indica che viene addebitata una batteria completamente carica.

-   **Aspetto uniforme e continuo.** Le animazioni efficaci rimuovono in modo semplice le giunzioni tra le modifiche dello stato della scena o dell'elemento visualizzando le relazioni e fornendo un'idea del luogo e del contesto. La continuità consente agli utenti di comprendere il modo in cui si trovano e come tornare al punto in cui provengono.

![cattura di schermata di tre anteprime delle finestre della barra delle applicazioni ](images/vis-animations-image9.png)

La finestra della barra delle applicazioni di Windows 7 Visualizza i morph per la continuità quando l'utente passa da un programma a un altro.

-   **Sono realistici.** Animazioni valide simulano le proprietà fisiche e il comportamento reali di un oggetto. Ciò consente agli utenti di stimare e comprendere i risultati delle interazioni. Non è necessario modellare esattamente il mondo reale, ma se si usano animazioni realistiche, è necessario mantenerle coerenti con il mondo reale. Gli utenti non devono mai essere sorpresi o confusi dai risultati, soprattutto con le animazioni usate per la manipolazione diretta.

![Figura del pulsante della barra delle applicazioni trascinato in una nuova posizione ](images/vis-animations-image10.png)

In questo esempio, l'animazione "sposta fuori dalla modalità" utilizzata dalla barra delle applicazioni di Windows 7 si rivelano più realistici rispetto a un punto di inserimento statico.

-   **Sono autentici.** Anche gli oggetti che non sono stati trovati nel mondo reale possono essere visualizzati in modo naturale, in base al comportamento reale di un oggetto diverso, ma correlato. Questa metafora funziona solo se la relazione comunica chiaramente lo scopo e il comportamento desiderati.

![screenshot dell'effetto generato dietro la finestra spostata ](images/vis-animations-image11.png)

In questo esempio, l'animazione della finestra "spatola" usata da Windows 7 si ritiene autentica perché è coerente con la modalità di funzionamento di Windows Glass nel mondo reale.

-   **Usare il mapping naturale.** I mapping naturali sono fisici o culturali. Un mapping naturale basato su impostazioni cultura, ad esempio, potrebbe iniziare dal fatto che nelle culture occidentali le persone leggono da sinistra a destra. Di conseguenza, per esprimere una sequenza temporale di oggetti, l'oggetto centrale è corrente, gli oggetti a sinistra sono passati e gli oggetti a destra sono in futuro. L'avanzamento nel tempo è indicato dal movimento da sinistra a destra.

![screenshot dell'indicatore di stato di Media Player ](images/vis-animations-image12.png)

In questo esempio, il controllo Windows Media Player dispone di un mapping naturale perché la riproduzione sposta la posizione da sinistra a destra.

-   **Hanno personalità.** Le animazioni ben scelte sono ottimi modi per aggiungere la personalità, il carattere e lo stile al programma. Possono rendere l'esperienza utente più coinvolgente e accattivante. Sebbene il tipo di animazione determini ciò che comunica, il modo specifico in cui viene eseguita l'animazione mostra la personalità del programma. Le animazioni valide proiettano la personalità giusta per il programma, se è grave o stravagante o in qualche parte.

![screenshot dell'interfaccia Zune progettata in modo creativo ](images/vis-animations-image13.png)

In questo esempio, l'uso del testo animato e della prospettiva dinamica di Zune consente di definire la propria personalità.

-   **Aspetto e sensibilità.** Le animazioni valide non danneggiano la produttività dell'utente bloccando gli utenti di altre interazioni o forzando gli utenti a guardare. Indipendentemente dalla natura e dal coinvolgimento delle animazioni del programma, nessuno vuole aspettarle in modo esclusivo. Anche le ottime animazioni sembrano reattive senza essere stonate grazie a un avvio rapido con un atterraggio soft. Le animazioni reattive possono inoltre trarre vantaggio dalla comunicazione immediata dei propri scopi. Gli utenti non devono guardare un'animazione per un lungo periodo di tempo solo per capire cosa sta facendo o quando viene eseguita. Per la manipolazione diretta, le animazioni reattive sono essenziali per mantenere un aspetto reale e coinvolgente del mondo reale. Per sentirsi direttamente, i punti di contatto di un oggetto devono rimanere sotto il puntatore senza problemi durante la manipolazione. Qualsiasi ritardo, risposta instabile o perdita di contatto elimina la percezione della manipolazione diretta.

![Figura del dito che tocca un touchscreen ](images/vis-animations-image14.png)

In questo esempio, la transizione di touch panning si riattiva mantenendo il punto di contatto sotto il dito dell'utente durante la manipolazione.

-   **Attrarre il livello di attenzione appropriato.** Le animazioni valide sono in genere minime e attirano solo l'attenzione necessaria per soddisfarne lo scopo. Di conseguenza, non si distrae, fastidioso, troppo complesso, troppo lungo o ripetitivo. Non diventano noiosi dopo le visualizzazioni ripetute.

![cattura di schermata dell'evidenziazione dissolvenza nei nomi file ](images/vis-animations-image15.png)

In questo esempio, Windows Search richiama temporaneamente l'attenzione sulle parole di ricerca corrispondenti, quindi si dissolve in basso.

-   **Aspetto speciale solo se davvero speciale.** La frequenza aumenta la necessità di sottigliezza, quindi le interazioni comuni necessitano di animazioni semplici che comunicano una semplice idea in modo semplice. Riservare animazioni speciali e complesse per esperienze speciali e non frequenti.

![Screenshot di quattro cerchi che diventano logo Windows ](images/vis-animations-image16.png)

In questo esempio, Windows usa un'animazione di acquisizione di attenzione all'avvio per rendere l'esperienza speciale, ma tale animazione non sarebbe appropriata altrove.

Se uno di questi attributi è stato rimosso, si saprà che è stato effettuato il giusto equilibrio.

### <a name="creating-an-animation-vocabulary"></a>Creazione di un vocabolario di animazione

Le ottime animazioni sono relative alla comunicazione visiva efficace e la coerenza è cruciale per la loro efficacia. Se si usa una transizione specifica, ad esempio il push di una scena in da destra per passare alla scena successiva, questa deve essere l'unica transizione usata a tale scopo e tale transizione non deve essere usata per altri scopi. L'assegnazione di significati diversi alla stessa animazione non può compromettere la comunicazione. Assegnando animazioni e transizioni specifiche a significati specifici, si crea un vocabolario di animazione.

Questo problema si applica alle animazioni e alle transizioni che hanno un significato, non a quelle generiche a cui gli utenti non possono assegnare significato o a quelle il cui scopo è non evidente. Ad esempio, animazioni come dissolvenze e effetti speciali come le dissolvenze non hanno un significato particolare, quindi possono essere utilizzate liberamente.

Un vocabolario valido assegna animazioni che modellano il comportamento fisico di un oggetto. Se è necessario assegnare un'animazione a un oggetto o a un'azione che non ha una controparte reale, scegliere un'animazione che Mostra come potrebbe comportarsi l'oggetto.

![screenshot del modo in cui hover rende l'alone del logo Windows ](images/vis-animations-image17.png)

Mentre il menu Start non è un oggetto reale, l'effetto del passaggio del mouse si accende come un oggetto reale, quando attivato.

Ogni animazione in un vocabolario deve essere chiaramente distinta. Le animazioni devono avere comportamenti simili solo se le azioni associate sono correlate in modo analogo. Ad esempio, le transizioni di spostamento suggeriscono la navigazione, quindi è possibile usare transizioni di spostamento da diverse direzioni per indicare tipi diversi di navigazione.

Si saprà che le animazioni e le transizioni non comunicano correttamente quando gli utenti trovano i risultati confusi, sorprendenti o imprevisti. In genere, è preferibile ottenere un solo scopo, oltre a diversi scopi.

Idealmente, il vocabolario di animazione deve essere completo in tutte le aree del programma in cui sono necessarie. Se solo alcune interazioni hanno animazioni naturali, questo attirerà l'attenzione su quelle che non lo sono.

Per ulteriori informazioni sul vocabolario di animazione di Windows, vedere la sezione [modelli di utilizzo](#usage-patterns) di questo articolo.

### <a name="designing-the-right-personality"></a>Progettazione della personalità corretta

Sebbene il tipo di animazione determini ciò che comunica, il modo specifico in cui viene eseguita l'animazione esprime la personalità del programma e ne rafforza il marchio.

La personalità del programma dovrebbe riflettere la natura delle attività e la personalità degli utenti, quindi non si tratta di una scelta arbitraria. Piuttosto, una personalità ben progettata dovrebbe essere autentica; non provare mai a forzarlo. La personalità deve creare una connessione emotiva all'utente. Alcuni fattori da considerare:

-   **Attività:** Grave o divertente; facoltativo o obbligatorio.
-   **Conseguenze:** Grave o minore.
-   **Costo:** Gratuito o acquistato; Se acquistato, prezzo moderato o costoso.
-   **Stato attivo dell'utente:** Gruppo relativamente limitato di utenti di destinazione o destinatari generali.
-   **Ambiente utente:** Professionale, occasionale o Home.
-   **Tempo utente:** Più giovane o meno recente.
-   **Frequenza di utilizzo:** Frequente o poco frequente.

La combinazione di questi fattori aiuta a determinare una personalità appropriata per il programma. Di seguito sono riportate alcune combinazioni appropriate per i tipi comuni di programmi:

**Applicazioni per la produttività**

Naturalmente, le applicazioni di produttività devono concentrarsi sulla produttività. Sebbene alcune esperienze speciali possano emergere, la maggior parte delle altre animazioni dovrebbe avere queste caratteristiche:

-   Piccola
-   Naturale, realistico
-   Sottile, sommesso
-   Veloce, efficiente
-   Relaxed

**Utilità**

Le utilità vengono in genere usate brevemente, quindi l'uso dell'animazione può essere più aggressivo:

-   Realistica, illustrativa, autonoma
-   Safe
-   Coinvolgente

**Intrattenimento, giochi**

Poiché l'obiettivo di questi programmi è coinvolgere e deliziare gli utenti, le animazioni e le transizioni possono essere molto più aggressive con queste caratteristiche:

-   Grande (probabilmente diventando parte integrante dell'esperienza)
-   Artificiale, surreale
-   Con conseguenze, vivaci
-   Emotiva, ludica, capricciosa
-   Energico

Creare una connessione emotiva è così importante per i programmi di intrattenimento che è accettabile ripiegare alcune regole, in modo da consentire agli utenti di amare il programma. Ad esempio, è accettabile se un'animazione o una transizione diventa noiosa dopo il centesimo tempo se la maggior parte degli utenti è improbabile che usi il programma spesso.

In generale, le animazioni e le transizioni di piccole dimensioni, naturali, sottolineate, efficienti, ma rilassate sono la scommessa più sicura. Le transizioni con queste caratteristiche in genere prendono il percorso più breve dall'inizio alla fine, avviano rapidamente, terminano senza interruzioni. Inoltre, le transizioni ben progettate sono progettate per funzionare correttamente nell'intera gamma di distanze in cui verranno usate.

### <a name="animation-performance"></a>Prestazioni animazione

Quando si progettano le animazioni, assicurarsi che non influiscano sulla capacità degli utenti di usare il programma in modo efficiente. In genere, è possibile rendere le animazioni sufficientemente lente per soddisfarne lo scopo, ma sufficientemente veloci da non interferire con la velocità di risposta, richiedere troppe attenzioni o diventare noiose.

**Non corretto:**

![Figura della pagina che gira da destra a sinistra ](images/vis-animations-image18.png)

Anche se questa pagina che gira l'animazione presenta un aspetto accattivante e realistico, riduce la produttività degli utenti richiedendo più tempo per trasformare le pagine.

Le brevi transizioni (200 millisecondi o meno) sono un caso speciale, specialmente quando si riferiscono a un ritardo, perché gli utenti saranno consapevoli di dover attendere una seconda divisione. Gli utenti sono disposti ad attendere queste animazioni se:

-   L'attesa percepita è estremamente breve (200 millisecondi o meno).
-   La transizione rende l'interazione più uniforme e naturale.
-   La transizione rende l'interazione più reattiva.
-   Qualsiasi ritardo consente di impedire all'utente di controllare l'interazione.

![Figura dei pulsanti della barra delle applicazioni trascinati in una nuova posizione ](images/vis-animations-image19.png)

Gli utenti accetteranno un breve ritardo per il pulsante della barra delle applicazioni per riordinare l'animazione perché è molto breve e rende l'interazione più naturale.

Esistono tre modi in cui le animazioni possono influire negativamente sulle prestazioni: velocità, velocità di risposta e percezione.

Per velocizzare, alcune animazioni sono faccette visive su attività con utilizzo intensivo della CPU, quindi l'ultima cosa da fare è rendere queste attività più lente con animazioni a elevato utilizzo di CPU. La maggior parte delle animazioni a elevato utilizzo di CPU (animazioni "pesanti") tende a:

-   Coinvolgere molti elementi in modo indipendente.
-   Riproduci per una durata o una distanza prolungata.
-   Coinvolgere una grande quantità di spazio sullo schermo.
-   Sono matematicamente complesse.

Animazioni con minore effetto sulle prestazioni:

-   Coinvolgere un singolo oggetto.
-   Riproduci per una durata o una distanza breve.
-   Implicano una piccola quantità di spazio sullo schermo.
-   Non sono matematicamente complesse.

Per garantire prestazioni ottimali, è consigliabile usare animazioni complesse solo per le attività che non richiedono un uso intensivo della CPU, mentre le animazioni leggere possono essere usate ovunque.

Per la velocità di risposta, la maggior parte delle animazioni e delle transizioni deve essere progettata in modo da consentire agli utenti di interagire mentre è in esecuzione l'animazione. A meno che un'animazione non faccia parte di un processo, renderla indipendente dall'interazione principale dell'utente e consentire agli utenti di interromperla.

Un'animazione potrebbe non influire negativamente sulle prestazioni di un'attività in realtà, ma gli utenti potrebbero avere la percezione che lo fa. Ad esempio, non usare un'animazione che risulti pesante per un'attività lenta e a elevato utilizzo di CPU anche se non danneggia le prestazioni, perché gli utenti potrebbero concludere che l'animazione è il motivo per cui l'attività è lenta. **Se un elemento sembra lento, sarà più lento, quindi è preferibile usare animazioni semplici, leggere e veloci.** L'uso delle animazioni con l'avvio a schiocco per le attività che richiedono un uso intensivo della CPU.

**Rischioso**

![screenshot della finestra di dialogo Copia con indicatore di stato ](images/vis-animations-image20.png)

Sebbene l'animazione nella finestra di dialogo Copia file di Windows non danneggi le prestazioni di copia dei file, viene eseguito il rischio che gli utenti ne pensino.

**Rischioso anche:**

![screenshot dello stato di avanzamento visualizzato nella barra degli indirizzi ](images/vis-animations-image21.png)

In questo esempio, l'animazione dello stato di avanzamento indesiderato nella barra degli indirizzi di Esplora risorse rende alcune attività molto lente.

Le animazioni e le transizioni non hanno alcun valore se la loro qualità è talmente ridotta che rendono l'esperienza meno semplice e meno accattivante. Per mantenerne la qualità, le animazioni devono essere progettate in modo da diminuire normalmente ogni volta che sono disponibili risorse di sistema sufficienti. Le animazioni possono peggiorare con varianti che richiedono un minor numero di risorse, ad esempio lunghezze più brevi o frequenze dei fotogrammi inferiori, o addirittura non in esecuzione. Indipendentemente dalle risorse disponibili, assicurarsi che le animazioni siano di qualità elevata e simili ad animazioni anziché bug software.

Infine, se gli utenti ritengono che le animazioni e le transizioni del programma si detraggono dalla loro produttività, è possibile che alcuni utenti vogliano disattivarli. Per supportare questa funzionalità, è necessario rispettare l'opzione per **disattivare tutte le animazioni non necessarie** presenti nel centro di accesso facilitato di Windows.

### <a name="attracting-the-right-level-of-attention"></a>Attrarre il livello di attenzione corretto

Mentre solo alcuni tipi di animazioni e transizioni sono appositamente progettati per attirare l'attenzione degli utenti, devono essere progettati per attirare il livello di attenzione appropriato per soddisfare le proprie esigenze. Quali sono i diversi modi per attirare l'attenzione e come scegliere quello più adatto?

**Effetti di animazione**

Diversi effetti di animazione attraggono diversi livelli di attenzione. Nell'elenco seguente vengono riepilogati i metodi più comuni, iniziando con la massima attenzione:

-   **Lampeggio rapido.** Richiede attenzione immediata. Può interrompere la concentrazione degli utenti, indipendentemente dal punto in cui si verifica il lampeggio.
-   **Intermittenza moderata.** Lo stesso, ma richiede meno attenzione con una frequenza inferiore.
-   **Rimbalzo.** Evidente nella visione periferica e relativamente impegnativo per natura. È probabile che gli utenti si notino, ma possono continuare a concentrarsi altrove solo se la durata è breve.
-   **Movimento.** Evidente in visione periferica, ma non impegnativo. Tuttavia, i movimenti complessi o tridimensionali attirano una maggiore attenzione rispetto ai movimenti semplici o 2D. È probabile che gli utenti si notino, ma possono continuare a concentrarsi altrove.
-   **Pulsazione moderata.** Evidente ma non distrazione nella visione periferica. Gli utenti possono continuare a concentrarsi altrove. Può avere luminosità, colori e dimensioni a impulsi.
-   **Impulsi lenti/incandescente.** Evidente ma impercettibile. Attrae maggiore attenzione rispetto a un effetto statico, ma gli utenti potrebbero non notare l'animazione a meno che non siano già in Cerca.
-   **Dissolvenza.** Anche meno evidente. Attrae maggiore attenzione rispetto a un effetto statico, ma gli utenti potrebbero non notare l'animazione a meno che non siano già in Cerca.
-   **Evidenziazione/bagliore statico.** Evidente se gli utenti scelgono di cercare, ma non richiedono attenzione se si trova altrove.
-   **Ambiente/naturale.** Espressamente non evidente grazie a un aspetto naturale e reale.

Per determinare l'approccio corretto per il programma o la funzionalità, valutare il modo in cui questi fattori sono correlati agli scenari della funzionalità.

Si supponga, ad esempio, di progettare un programma di messaggistica istantanea e che qualcuno abbia appena inviato un messaggio all'utente. Questo scenario richiede l'attenzione dell'utente, dovrebbe essere evidente ovunque e, in genere, l'utente vorrà rispondere rapidamente. Questo scenario suggerisce che un'animazione moderata lampeggiante sarebbe una scelta ottimale. Al contrario, si supponga di voler informare gli utenti che è stato completato un processo di stampa. Gli utenti devono essere in grado di continuare a concentrarsi e lavorare in modo produttivo altrove ed è accettabile se gli utenti non si accorgono. Questo scenario suggerisce che la scelta tra moderato e rallentamento o bagliore è una scelta ottimale.

**Duration**

La durata appropriata per un'animazione di recupero dipende dallo scenario e dal tipo specifico di animazione usato. Maggiore è l'attenzione di un effetto di animazione, minore sarà la durata. Sebbene gli effetti molto sottili che richiedono una certa attenzione, come la pulsazione lenta, possano essere riprodotti a tempo indeterminato, gli effetti impegnativi di attenzione devono essere riprodotti solo da 1 a 3 secondi. È più rischioso rendere l'animazione eccessiva e fastidiosa.

![screenshot del pulsante della barra delle applicazioni evidenziato ](images/vis-animations-image22.png)

In Windows 7 la barra delle applicazioni lampeggia per un secondo. È più fastidioso.

**Decadimento effetto**

Si consiglia di progettare animazioni con attenzione in base al presupposto che se gli utenti non rispondono immediatamente, perché sono occupati a eseguire un'altra operazione e non vogliono essere interrotti. Pertanto, l'obiettivo è quello di attirare l'attenzione senza richiedere l'intervento dell'utente.

Per ottenere il giusto equilibrio tra attirare l'attenzione senza richiederlo, decadire l'intensità di un effetto nel tempo. Per attirare l'attenzione, ad esempio, è possibile rendere l'effetto inizialmente forte, ma rallentare rapidamente l'effetto. In questo modo, la potenza allettante viene determinata principalmente dall'effetto iniziale, ma l'impressione complessiva dell'utente è determinata principalmente dal suo completamento.

![cattura di schermata che mostra la frequenza flash ridotta ](images/vis-animations-image23.png)

In Windows 7, l'effetto flash sulla barra delle applicazioni rallenta alla fine.

### <a name="what-about-powerpoint"></a>E per quanto riguarda PowerPoint?

Le transizioni di Microsoft PowerPoint spesso violano intenzionalmente queste linee guida perché sono progettate per attirare l'attenzione sulle transizioni delle diapositive e richiedere agli utenti di attenderle. Inoltre, non hanno un significato particolare, quindi non comunicano oltre il fatto che una diapositiva sta cambiando.

Le transizioni di tipo PowerPoint, quando vengono usate correttamente, hanno gli scopi seguenti:

-   Interrompono le presentazioni lunghe in blocchi più piccoli forzando la sospensione del Presenter.
-   Estraggono l'attenzione del pubblico verso le modifiche apportate alla presentazione, per aiutare gli utenti a concentrarsi sulle proprie opinioni.
-   Forniscono alla presentazione un ritmo in modo da non sembrare monotono o travolgente.
-   Il loro stile riflette la personalità del relatore o del materiale.

Sebbene si tratta di obiettivi importanti per una presentazione, le transizioni di questo tipo non possono attirare l'attenzione nell'interfaccia utente della maggior parte dei tipi di programmi e diventano faticosi rapidamente.

**Riga inferiore:** Non usare transizioni di tipo PowerPoint come modello per il programma.

**Se si eseguono solo sei elementi...**

1.  Usa le animazioni e le transizioni per semplificare la comprensione del programma, con una maggiore semplicità e più accattivante. Dovrebbero avere uno scopo preciso. Non usare le animazioni solo perché è possibile o per attirare un'attenzione non necessaria per il programma.
2.  Definire un vocabolario di animazione e usarlo in modo coerente in tutto il programma. Usare il vocabolario di animazione di Windows 7 quando appropriato.
3.  Usare le caratteristiche delle animazioni per fornire la personalità del programma e rafforzare il proprio marchio.
4.  Crea la maggior parte delle animazioni in modo semplice, conciso e sottile. Tenere presente che le animazioni non devono richiedere attenzione per avere esito positivo. Se un'animazione è appropriata e naturale, gli utenti ne noteranno solo l'assenza.
5.  Rendi le tue animazioni veloci e reattive e offrigli un aspetto leggero. Indipendentemente dalla modalità di coinvolgimento delle animazioni, nessuno desidera che sia in attesa. Progettare animazioni più pesanti per avere una riduzione del normale.
6.  Progettazione per la lunga esecuzione. Se un'animazione è noiosa, distrazione o noiosa, riprogettarla o rimuoverla.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le animazioni hanno diversi modelli di utilizzo:



|                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Feedback del passaggio del mouse**<br/> per indicare dove si trova il punto di interazione. <br/>                                | Indica che il punto di interazione è attivo. il passaggio del mouse può essere visualizzato anche tramite un effetto statico.<br/> vocabolario di Windows: visualizzazione dell'effetto del passaggio del mouse (rettangolo di delimitazione, evidenziazione, ingrandimento) con effetto di dissolvenza in uscita/dissolvenza. <br/> ![Screenshot di una delle sei copertine di un album evidenziato ](images/vis-animations-image24.png)<br/> In Zune Digital Media Player, l'album illustra come evidenziare e aggiungere i controlli di riproduzione al passaggio del mouse.<br/>                                                                                                                                                                                                                 |
| **Fare clic su feedback**<br/> per indicare che un oggetto selezionabile è reattivo e ha ricevuto un clic. <br/>    | Indica che è stato fatto clic su un oggetto.<br/> vocabolario di Windows: sfondo dell'oggetto Flash nell'evento Click-down. per visualizzare il contatto tocco, usare un effetto Ripple. <br/> ![Foto del dito sul touchscreen che mostra le Ripple ](images/vis-animations-image25.png)<br/> Touch Visualizza un'animazione Ripple in modo che l'utente sappia che l'interazione è stata riconosciuta.<br/>                                                                                                                                                                                                                                                                                                         |
| **Commenti sulla selezione**<br/> per indicare che un oggetto è selezionato. <br/>                                | Indica che un oggetto è selezionato. la selezione può essere visualizzata anche tramite un effetto statico.<br/> vocabolario di Windows: creare un rettangolo di selezione con effetto di dissolvenza in uscita/dissolvenza per la fluidità. <br/> ![Figura del coperchio di un album fatto clic e quindi selezionato ](images/vis-animations-image26.png)<br/> In Zune, l'album copre il lampeggiamento del clic e quindi ottiene un rettangolo di selezione alla selezione.<br/>                                                                                                                                                                                                                                                                      |
| **Feedback sullo stato di avanzamento**<br/> per mostrare che è in corso l'esecuzione di un'attività. <br/>                             | Il feedback sullo stato di avanzamento indica che un'attività è in corso, in genere con indicatori di attività, barre di stato o animazioni che illustrano l'attività. il feedback dello stato di avanzamento determinato Mostra approssimativamente la quantità di attività eseguita e la quantità rimanente, mentre lo stato di avanzamento indeterminato indica solo che l'attività è stata eseguita.<br/> vocabolario di Windows: indicatori di attività rotanti, barre di avanzamento, background di avanzamento, animazioni dell'illustrazione. <br/> ![screenshot della finestra di dialogo con testo di "accesso" ](images/vis-animations-image27.png)<br/> In questo esempio Windows Live Messenger Visualizza un feedback sullo stato di avanzamento indeterminato durante l'accesso.<br/> |
| **Attrattore**<br/> per mostrare che un elemento richiede l'attenzione dell'utente. <br/>                          | È possibile attirare il livello di attenzione corretto quando vengono creati oggetti significativi o richiedono attenzione (spesso a causa di modifiche) oppure si verificano eventi importanti o urgenti. vedere [attrarre il livello di attenzione corretto per le](#attracting-the-right-level-of-attention) tecniche di progettazione.<br/> vocabolario di Windows: lampeggiante, in continua evoluzione, pulsatura, bagliore, bagliore. <br/> ![screenshot che illustra l'animazione della barra degli strumenti ](images/vis-animations-image28.png)<br/> La barra degli strumenti di Windows Live viene animata al primo aspetto per renderla evidente.<br/>                                                                                                                                 |
| **Relationship**<br/> per mostrare la relazione tra gli oggetti o la causalità negli effetti. <br/>        | Mostra le relazioni, soprattutto quando la relazione potrebbe non essere riconosciuta o prevista, in modo che non sia distrazione o confusione.<br/> vocabolario di Windows: morphing, trasporto, cambiamento fisico, ad esempio il capovolgimento, la crescita da un'origine punto, la compattazione fino a un punto di destinazione. <br/> ![screenshot della finestra di dialogo Calibrazione colori](images/vis-animations-image29.png)<br/> In questo esempio, l'animazione mostra la relazione tra l'impostazione gamma e il relativo effetto sullo schermo.<br/>                                                                                                                                                    |
| **Illustrazione/anteprima**<br/> per spiegare visivamente un concetto, un'attività o l'effetto di un comando. <br/> | Un'animazione o un video che illustra un concetto o il modo in cui un elemento funziona visivamente, per integrare o sostituire una spiegazione testuale. Questa operazione consente agli utenti di eseguire attività o di scegliere i comandi in modo efficiente e sicuro. <br/> ![cattura di schermata dell'errore di ortografia correzione della penna ](images/vis-animations-image30.png)<br/> In questo esempio, i comandi "Mostra me" del pannello di input di Tablet PC utilizzano illustrazioni per mostrare come correggere, eliminare, dividere e unire.<br/>                                                                                                                                                                                                        |



 

Le transizioni hanno diversi modelli di utilizzo:



|                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aumento/riduzione/visualizzazione oggetto**<br/> per modificare la dimensione o lo stato di un oggetto in modo uniforme. <br/>                                                                                                         | Modifiche all'oggetto tra gli Stati, probabilmente durante lo stato di trasferimento. la transizione mantiene gli utenti orientati durante le modifiche.<br/> vocabolario di Windows: morph, Change Size, Object slides in o out. <br/> ![Screenshot di tre dimensioni dei gadget meteorologici ](images/vis-animations-image31.png)<br/> In questo esempio, il gadget meteorologico si trasforma dal proprio stato conciso per visualizzare la relativa finestra di dialogo Opzioni.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Mostra/Nascondi/Cambia contenuto**<br/> per mostrare, nascondere o modificare facilmente il contenuto, in genere per la divulgazione progressiva. <br/>                                                                       | Riforme interne della finestra per visualizzare contenuto più, minore o diverso. la transizione mantiene gli utenti orientati durante le modifiche.<br/> vocabolario di Windows: il riquadro scorre in o in uscita. dissolvenza in entrata e in uscita delle finestre a comparsa. il contenuto o il rollup del contenuto diverso. <br/> ![cattura di schermata di tre dimensioni del calcolatore ](images/vis-animations-image32.png)<br/> Il calcolatore di Windows presenta una transizione uniforme tra le modalità di visualizzazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Mostra/Nascondi controllo o convenienza**<br/> per visualizzare o nascondere in modo semplice i controlli o i relativi affordances al passaggio del mouse o del mouse per semplificare l'aspetto visivo normale. <br/>                | Visualizza i controlli quando gli utenti posizionano il puntatore del mouse su un'area di comando oppure visualizzano affordances quando gli utenti si spostano su un controllo. il passaggio del mouse su queste aree indica che l'utente intende interagire. affordances può nascondere se il puntatore diventa stazionario. <br/> ![screenshot dei controlli sbiaditi prima del passaggio del mouse ](images/vis-animations-image33.png)<br/> In questo esempio, i controlli di Windows Media Player passano al passaggio del mouse in modalità schermo intero.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Transizioni di scena**<br/> per rendere una transizione della scena uniforme e trasparente per evitare l'attenzione. <br/>                                                                                   | Le modifiche improvvise alla scena possono essere stridente, specialmente per le aree dello schermo di grandi dimensioni, quindi usare le transizioni di scena per creare uniformità e continuità e fornire il contesto. le transizioni di scena sono progettate come chiave naturale e bassa, per evitare di richiamare l'attenzione al processo di transizione.<br/> vocabolario di Windows: dissolvenza in entrata/in uscita; dissolvenza incrociata; scorrimento a sinistra, in uscita/a destra, in alto, in basso; push e coperture. <br/> ![Screenshot di una foto che si dissolve in un'altra ](images/vis-animations-image34.png)<br/> In questo esempio, lo sfondo del desktop di Windows è leggermente incrociato tra le immagini per fare in modo che la transizione risulti liscia e controllata.<br/>                                                                                                                                                                                                                                                                                                                               |
| **Transizioni di scena speciali**<br/> per attirare l'attenzione su una modifica della scena per renderla speciale o per concentrare l'attenzione dell'utente. <br/>                                                               | Sebbene la maggior parte delle transizioni di scena non chiami l'attenzione al processo di transizione, alcune sono progettate per suddividere il flusso e attirare l'attenzione in modo da evidenziare che sta per essere eseguita un'altra operazione. per attirare l'attenzione, le transizioni speciali della scena sono progettate per essere non naturali e hanno un impatto visivo elevato. <br/> ![screenshot della diapositiva di attenzione-cattura della transizione ](images/vis-animations-image35.png)<br/> In questo esempio PowerPoint usa le transizioni con attenzione per attirare i destinatari nella modifica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Manipolazione diretta**<br/> per mostrare l'effetto delle manipolazioni dirette (ad esempio, spostamento, scorrimento/panning, rotazione e zoom). <br/>                                                                   | La transizione Mostra l'effetto della manipolazione in tempo reale. l'effetto dovrebbe essere uniforme, continuo e coerente con il mondo reale. lo spostamento e la rotazione potrebbero non essere continui in alcune posizioni per indicare restrizioni o opzioni preferite. lo zoom rende il contenuto più grande o più piccolo, eventualmente modificando di conseguenza il livello di dettaglio. <br/> ![Screenshot di tre dimensioni di lente di ingrandimento ](images/vis-animations-image36.png)<br/> In questo esempio, la lente di ingrandimento viene ingrandita perfettamente tra i livelli.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Manipolazioni dirette non corrette**<br/> per indicare che è stata tentata una manipolazione diretta, ad esempio spostamento, scorrimento/Pan, ma che non è stato possibile eseguire. <br/>                                           | La transizione Mostra la manipolazione tentata, ma ritorna allo stato originale. spesso l'effetto sembra che la manipolazione non possa essere eseguita a causa di una restrizione fisica reale. Queste animazioni vengono usate al posto dei messaggi di errore basati su testo, che potrebbero compromettere l'aspetto reale della manipolazione.<br/> vocabolario di Windows: rimbalzo <br/> ![Figura delle animazioni che comunicano visivamente ](images/vis-animations-image4.png)<br/> In questo esempio il documento rimbalza per indicare che l'utente ha raggiunto la fine.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Ordina, filtra, riordina le transizioni**<br/> per indicare che la presentazione o il contenuto di una raccolta di elementi è stato modificato. <br/>                                                            | La transizione Mostra (o per le modifiche complesse, suggerisce) l'effetto della modifica. <br/> ![screenshot delle fotocamere riga con tre elementi rimossi ](images/vis-animations-image37.png)<br/> ![Screenshot simile con fotocamere diverse rimosse ](images/vis-animations-image38.png)<br/> ![Screenshot simile con altre fotocamere rimosse ](images/vis-animations-image39.png)<br/> in questo esempio, ricerca visiva Bing usa una transizione di filtro.<br/> ![screenshot del coperchio dell'album modificarne l'aspetto ](images/vis-animations-image40.png)<br/> In questo esempio Windows Media Center USA una transizione di riordino come esperienza speciale mentre un brano viene riprodotto.<br/>                                                                                                                                                                                                                                                                                   |
| **Transizioni di prestazioni**<br/> per far sembrare che un'azione avvenga più velocemente. <br/>                                                                                                              | Anche se qualsiasi transizione può comportare l'esecuzione di un'azione in modo più rapido, lo scopo principale di queste transizioni è quello di migliorare la percezione delle prestazioni e della velocità di risposta. una tecnica efficace consiste nel mostrare l'attività eseguita nei passaggi intenzionali. al contrario, ritardare l'azione, il rendering dei risultati in modo casuale o l'uso di un indicatore di attività avrà un aspetto lento.<br/> vocabolario di Windows: eseguire un'azione in fasi, con transizioni uniformi tra le fasi. <br/> ![screenshot della Jump List aggiunta di destinazioni ](images/vis-animations-image41.png)<br/> In questo esempio, un Jump List della barra delle applicazioni Visualizza immediatamente gli elementi standard e quindi scorre per visualizzare le destinazioni quando l'elenco è pronto. Questa operazione maschera il tempo necessario per compilare l'elenco. Al contrario, il ritardo della visualizzazione iniziale potrebbe non rispondere e la visualizzazione di un elenco incompleto o di un feedback sullo stato di avanzamento risulterebbe molto più lenta.<br/> |
| **Esperienze speciali**<br/> per coinvolgere e deliziare gli utenti durante le [esperienze](glossary.md) non frequenti e speciali che sono importanti per il programma e hanno l'attenzione completa dell'utente. <br/>    | Sebbene qualsiasi transizione abbia la possibilità di essere un'esperienza speciale, queste transizioni sono particolarmente riservate per esperienze poco frequenti che sono realmente speciali per il programma. le transizioni personalizzate vengono usate per dare un'idea particolare. la personalizzazione e la personalità sono spesso elementi di progettazione importanti. diversamente da altri modelli, le esperienze speciali possono richiedere attenzione, essere pesanti e richiedere agli utenti di attendere qualche minuto. di conseguenza, queste transizioni si esauriscono rapidamente se sovrautilizzate perché l'esperienza non è più speciale. <br/> ![screenshot del logo Windows che cambia in una nuova schermata ](images/vis-animations-image42.png)<br/> In questo esempio, Windows Media Center Visualizza un'animazione durante il caricamento per coinvolgere immediatamente gli utenti.<br/>                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Indicazioni

### <a name="effective-communication"></a>Comunicazione efficace

-   **Definire e usare un vocabolario di animazione** per assicurarsi che le animazioni e le transizioni abbiano un significato coerente e usarle in modo coerente in tutto il programma. La maggior parte dei vocabolari deve includere voci per la scena e l'aspetto dell'oggetto e la scomparsa, la navigazione, l'interazione di base (hovering, selezione, selezione), la manipolazione e l'interazione degli oggetti (spostamento, eliminazione, ridimensionamento, scorrimento, panning, zoom, rotazione, filtro) e attirare l'attenzione. Un significato coerente è essenziale per la comunicazione efficace.
-   **Quando si pratica, utilizzare il vocabolario di animazione di Windows.** Sebbene il programma possa avere un pubblico diverso e esigenze diverse, spesso i vantaggi della coerenza e della familiarità superano i vantaggi derivanti dall'uso diverso. Se il vocabolario del programma deve essere diverso, usare gli stessi tipi di animazione di base di Windows, ma assegnare loro la personalità giusta per il programma.
-   **Non assegnare significati specifici a animazioni e transizioni generiche in un vocabolario di animazione.** Le transizioni generiche come dissolvenze e effetti speciali come le dissolvenze non hanno un significato particolare (oltre a essere visualizzate o scompaiono), in modo che possano essere utilizzate liberamente.

    **Non corretto:**

    ![schermata di una finestra di dialogo che si dissolve in un'altra ](images/vis-animations-image43.png)

    In questo esempio, una dissolvenza incrociata viene erroneamente usata per passare all'elemento successivo. Poiché le dissolvenze incrociate non hanno un significato particolare, questa transizione non fornisce il contesto.

-   **Rendere le voci del vocabolario chiaramente distinte.** Le azioni correlate possono avere effetti simili (ad esempio, lo zoom avanti e lo zoom indietro dovrebbero avere transizioni inverse), ma le azioni non correlate dovrebbero avere effetti chiaramente distinti (ad esempio, lo zoom non deve mai essere confuso con la rotazione).
-   **Mantieni realistici e coerenti gli effetti reali.** Se usi animazioni e transizioni realistiche, Mantieni l'esperienza coerente con il mondo reale. Gli utenti non devono mai essere sorpresi, confusi o fuorviati dai risultati. Per coerenza, non combinare le metafore.
-   **Assegnare animazioni inverse alle azioni inverse.** Questa operazione soddisfa le aspettative degli utenti e semplifica il vocabolario. Se, ad esempio, un riquadro viene visualizzato scorrendo in, rimuoverlo facendo scorrere l'esterno con un altro effetto.
-   **Rendere comprensibili le animazioni.** Gli utenti dovrebbero essere in grado di comprendere rapidamente lo scopo di un'animazione. È possibile rendere un'animazione troppo piccola, troppo breve (meno di 50 millisecondi) o così sottile che gli utenti non siano in grado di comprenderne lo scopo. In questi casi, è possibile riprogettare per rendere chiaro il significato oppure rimuovere.

    **Non corretto:**

    ![cattura di schermata dell'animazione nella finestra di dialogo di eliminazione ](images/vis-animations-image44.png)

    In questo esempio, l'effetto è talmente piccolo e leggero che pochi utenti possono comprenderne lo scopo. Miglioramento della riprogettazione o della rimozione.

### <a name="patterns"></a>Modelli

**Feedback del passaggio del mouse**

-   **Per sembrare reattivo, provare a riprodurre l'animazione entro 50 millisecondi di immissione o uscita dallo stato del passaggio del mouse.**
-   **Per visualizzare rapidamente, rendere la durata delle animazioni del passaggio del mouse inferiore a 50 millisecondi.**
-   **Usare un effetto di dissolvenza in entrata/disattivazione del passaggio del mouse.** Questa operazione rende gli effetti del passaggio del mouse chiaramente distinti dal feedback di selezione e selezione.

**Fare clic su feedback**

-   **Per sembrare reattivo, provare a riprodurre l'animazione entro 50 millisecondi di evento Click down.** Fare clic su eventi non è necessario fare clic su feedback.
-   **Per visualizzare rapidamente, fare clic su animazioni con una durata inferiore a 50 millisecondi.**
-   **Usare un effetto flash o lampeggiamento in background.** Questa operazione rende gli effetti clic chiaramente distinti rispetto al passaggio del mouse e al feedback della selezione. Poiché fare clic su richiede il passaggio del mouse, fare clic su feedback una semplice aggiunta al feedback del passaggio del mouse.

**Commenti sulla selezione**

-   **Per sembrare reattivo, provare a riprodurre l'animazione entro 50 millisecondi di selezione o deselezione.**
-   **Per visualizzare rapidamente, fare in modo che la durata delle animazioni di selezione sia inferiore a 50 millisecondi.**
-   **Usare un effetto rettangolo di selezione dissolvenza in uscita/dissolvenza.** In questo modo, la selezione si distingue chiaramente dal passaggio del mouse e si fa clic su feedback

**Feedback sullo stato di avanzamento**

-   **Usare un indicatore di attività quando un'azione non può essere eseguita entro un secondo.** Questa operazione indica che il comando è stato ricevuto.
-   **Utilizzare un indicatore di stato quando un'attività impiega più di cinque secondi.** Per altre linee guida, vedere [indicatori di stato](progress-bars.md).
-   **Utilizzare animazioni di feedback sullo stato di avanzamento che consentono agli utenti di visualizzare l'effetto delle attività a esecuzione prolungata.** Evitare animazioni non necessarie per il feedback sullo stato di avanzamento se un'animazione non comunica niente di utile, usare invece un indicatore di stato.
-   **Hanno stati di completamento e di errore chiaramente identificabili.** Gli utenti devono essere in grado di determinare rapidamente questi stati finali.
-   **Interrompi la visualizzazione dello stato di avanzamento quando l'attività sottostante non sta procedendo.** Gli utenti devono essere in grado di determinare se lo stato di avanzamento non viene effettuato e reagire di conseguenza.

**Attrattori**

-   **Usare gli attraenti con il vincolo.** A meno che le informazioni non siano urgenti, critiche o altrimenti potrebbero influire sul comportamento immediato dell'utente, in genere è preferibile modificare lo stato in modo impercettibile e consentire agli utenti di individuare autonomamente la modifica. [Risolvere le distrazioni, non l'individuabilità](/windows/desktop/uxguide/how-to-design-desktop-ux).

    ![screenshot delle icone di stato wireless ](images/vis-animations-image45.png)

    In questo esempio, l'icona dell'area di notifica della rete wireless usa un'animazione per i problemi critici, ma consente agli utenti di individuare i segnali deboli autonomamente.

-   **Scegliere un'animazione che disegna il livello di attenzione corretto.** Le animazioni degli attrattori devono attirare l'attenzione a se stessi per soddisfare i propri scopi, ma non più. Se l'utente deve agire immediatamente, scegliere un effetto che richieda attenzione indipendentemente dalla posizione dell'utente. Per altre situazioni, vedere la sezione [attrarre il livello di attenzione corretto](#attracting-the-right-level-of-attention) per ottenere la corretta combinazione di attenzione, osservabilità e urgenza.

    **Non corretto:**

    ![screenshot della graffetta assistente di Office ](images/vis-animations-image46.png)

    Gli assistenti Microsoft Office hanno attirato un'attenzione non necessaria.

-   **Se l'utente non risponde, non ripetere l'animazione o usare animazioni continue.** Si supponga invece che l'utente abbia scelto di non agire ora, ma può agire in seguito. Le animazioni continue rendono difficile per gli utenti concentrarsi su qualsiasi altra operazione.

**Animazioni relazioni**

-   **Usare le animazioni delle relazioni per mostrare dove provengono gli oggetti o dove sono andati.**
-   **Le animazioni delle relazioni devono iniziare o terminare con l'oggetto selezionato.** Non visualizzare le relazioni tra gli oggetti a cui l'utente non sta interagendo. Se gli utenti notano, cosa si noterà è la distrazione.

**Illustrazioni/anteprime**

-   **Usare anteprime per mostrare l'effetto di un comando senza che gli utenti debbano eseguirlo per primo.** Grazie alle anteprime utili, è possibile migliorare l'efficienza e la facilità di apprendimento del programma e ridurre la necessità di tentativi ed errori.
-   **Utilizzare illustrazioni e anteprime con un'interpretazione chiara.** Hanno un valore minimo in caso di confusione.
-   **Riprodurre solo una illustrazione alla volta** per evitare di sovraccaricare gli utenti. Se sono possibili più illustrazioni simultanee, utilizzare il puntatore del mouse o un pulsante Riproduci per consentire agli utenti di indicare l'interesse.
-   **Riprodurre automaticamente un'illustrazione se è lo scopo principale della finestra o della pagina.** In caso contrario, se è facoltativo, consentire agli utenti di riprodurlo quando sono pronti.
-   **Riprodurre le animazioni alla velocità ottimale**: non così veloce sono difficili da comprendere, ma non così lente sono noiose da guardare.

**Aumento/riduzione oggetto**

-   **Non ritagliare il contenuto durante un ridimensionamento.** Espandere i contenitori prima di aggiungere il contenuto. Rimuovere il contenuto prima di ridurre i contenitori.

    **Non corretto:**

    ![screenshot del calcolatore troncato ](images/vis-animations-image47.png)

    In questo esempio, il contenuto viene ritagliato durante un ridimensionamento.

**Mostra/Nascondi/Cambia contenuto**

-   **Visualizzare informazioni importanti in modo statico.** Gli utenti non devono accedere a informazioni importanti attraverso la divulgazione progressiva.

**Mostra/Nascondi controllo o convenienza**

-   **Visualizza i controlli importanti quando l'utente posiziona il puntatore in un punto qualsiasi all'interno della finestra o del riquadro oppure, se a schermo intero, al passaggio del mouse.** Non è necessario che gli utenti cerchino questi controlli, quindi è opportuno renderne l'individuazione.

    ![figura che Mostra come il passaggio del mouse Visualizza i controlli ](images/vis-animations-image48.png)

    In questo esempio, Windows Media Center Visualizza i controlli quando il puntatore è posizionato sulla finestra.

-   **Consente di visualizzare i controlli secondari o i affordances di controllo quando l'utente posiziona il puntatore su o accanto ai comandi.** Per facilitarne l'individuazione, rendere la località ovvia e la destinazione di grandi dimensioni.

    ![screenshot del comando secondario che rivela il puntatore ](images/vis-animations-image49.png)

    In questo esempio, Windows Live Messenger Visualizza un comando secondario quando il puntatore si trova in prossimità dell'angolo superiore destro.

**Transizioni di scena**

-   **Rendere le transizioni della scena fisica coerenti con il mapping naturale.** Le persone leggono da sinistra a destra nelle impostazioni cultura occidentali e i diagrammi gerarchici scorrono dall'alto verso il basso. Di conseguenza, l'avanzamento nel tempo è indicato dallo spostamento da sinistra a destra. Le transizioni di scena fisiche seguenti hanno un mapping naturale:



    | Transizione                          | Significato                                     |
    |---------------------------|--------------------------------------|
    | Da sinistra<br/>      | Sposta indietro nel flusso attività<br/>    |
    | Da destra<br/>     | Sposta in avanti nel flusso attività<br/> |
    | Dall'alto<br/>       | Sposta su gerarchia attività<br/>    |
    | Dalla parte inferiore<br/>    | Sposta giù gerarchia attività<br/>  |



 

-   **Se il programma riproduce suoni, transizioni di scene di progettazione e transizioni audio insieme.** Se, ad esempio, una scena si dissolve gradualmente, qualsiasi suono dovrebbe dissolversi gradualmente. Non rovinare le transizioni visive senza problemi con transizioni audio improvvise. Per altre linee guida audio, vedere [audio](vis-sound.md).

**Manipolazione diretta**

-   **Quando si usano i movimenti fisici nell'interazione (ad esempio, il lancio), progettare l'animazione in modo da sembrare una risposta naturale al gesto.** Collegare la causare interazione con l'effetto di transizione. Fornire le caratteristiche fisiche di animazione reali, ad esempio accelerazione, decelerazione, Momentum, resistenza, peso, rimbalzo e rotazione.
-   **Per mantenere un'idea diretta, mantenere i punti di contatto di un oggetto sotto il puntatore in modo uniforme nell'intera interazione.** Qualsiasi ritardo, risposta instabile o perdita di contatto elimina la percezione della manipolazione diretta. Gli oggetti non devono mai scomparire durante la manipolazione.

**Ordinare, filtrare o riordinare le transizioni**

-   **Per le modifiche semplici, visualizzare l'intera transizione.** Gli utenti potranno seguire facilmente l'intera transizione. Le modifiche semplici coinvolgono quattro elementi o meno.
-   **Per le modifiche complesse, evidenziare la fine del movimento quando rallenta e lasciare l'occhio a riempire il resto.** In questo modo il movimento risulta molto più reattivo e ordinato.

**Transizioni di prestazioni**

-   **Provare a eseguire transizioni lente in due o tre fasi per renderle più veloci e immediatamente interattive.** Quando appropriato, utilizzare l'ordine di composizione seguente:
    -   Frame esterno
    -   Sfondo
    -   Contenuto iniziale (usando una rappresentazione temporanea, se necessario)
    -   Controlli primari (in modo che gli utenti possano interagire immediatamente)
    -   Controlli secondari e gli eventuali elementi dell'interfaccia utente rimanenti
    -   Contenuto finale (se è stata usata una rappresentazione temporanea) usare transizioni come dissolvenze e diapositive per far sembrare la composizione liscia, ordinata e raffinata.

![screenshot della mappa con la foto e la griglia satellite ](images/vis-animations-image50.png)

Quando si scorre la visualizzazione "Bird ' s Eye", Bing Maps Visualizza uno sfondo della griglia temporanea. In questo modo gli utenti possono continuare a scorrere immediatamente e prima del rendering del contenuto finale.

**Animazioni con esperienza speciale**

-   **Riprendere in considerazione le schermate iniziali animate (nonché le schermate iniziali statiche).** Spesso le schermate iniziali attirano l'attenzione sul tempo necessario per il caricamento di un programma e hanno una rapida introduzione. Mentre le schermate iniziali sono accettabili se vengono visualizzate solo quando l'interazione dell'utente non è possibile, ogni volta che si pratica un'alternativa migliore è progettare il programma in modo che gli utenti possano interagire immediatamente con esso, anche quando è ancora in fase di caricamento.
-   **Fornire un comando Ignora Introduzione Se una schermata iniziale animata richiede più di tre secondi.** Anche facendo clic in un punto qualsiasi della schermata iniziale verrà ignorata. In alternativa, usare una versione breve dell'animazione dopo un periodo iniziale.

### <a name="performance"></a>Prestazioni

-   **Non fare in modo che gli utenti attendano le animazioni e le transizioni del programma.** Usare brevi animazioni e transizioni (inferiori a 200 millisecondi) ogni volta che è pratica. Utilizzare animazioni più veloci (100 millisecondi) per operazioni più frequenti. Progettare animazioni più lunghe (più di un secondo in genere i suggerimenti sullo stato di avanzamento, l'illustrazione e i modelli di esperienza speciale) in modo che gli utenti possano continuare a lavorare mentre sono in esecuzione.
-   **Progettare animazioni con esecuzione prolungata per rendere chiaro agli utenti che possono interagire mentre l'animazione è in esecuzione.** Gli utenti non tenteranno di continuare a lavorare se gli indizi visivi suggeriscono che non possono.

    ![Screenshot di un indicatore di stato in una barra di stato ](images/vis-animations-image51.png)

    In questo esempio di Windows Internet Explorer, l'indicatore di stato della chiave inferiore nella barra di stato suggerisce che gli utenti non devono attendere il completamento prima di poter interagire.

-   **Utilizzare animazioni leggere per le attività con utilizzo intensivo della CPU.** In questo modo si ottiene l'intera potenza di elaborazione dell'attività. Inoltre, gli utenti non percepiscono che l'animazione leggera è il motivo per cui l'attività richiede un utilizzo intensivo della CPU.
-   **Non visualizzare un indicatore di attività durante un'animazione o una transizione.** Questa operazione elimina l'effetto. Progettare animazioni e transizioni in modo che possano iniziare subito.
-   **Progettare le animazioni in modo da peggiorare correttamente ogni volta che sono presenti risorse di sistema insufficienti.** Le animazioni possono peggiorare con varianti che richiedono un minor numero di risorse, ad esempio lunghezze più brevi o frequenze dei fotogrammi inferiori, o addirittura non in esecuzione. Indipendentemente dalle risorse disponibili, assicurarsi che le animazioni siano di qualità elevata e simili ad animazioni anziché bug software.

    **Non corretto:**

    ![screenshot del frame di programma sbiadito sul desktop ](images/vis-animations-image52.png)

    In questo esempio, la transizione della finestra di ripristino viene utilizzata anche se non sono disponibili risorse di sistema sufficienti per riprodurlo correttamente. Di conseguenza, il frame bloccato sembra essere un bug. Se le risorse non sono disponibili, è preferibile visualizzare semplicemente la finestra senza una transizione.

### <a name="animation-characteristics"></a>Caratteristiche di animazione

Le animazioni e le transizioni ben progettate presentano in genere queste caratteristiche:

-   **Breve durata.** La maggior parte delle animazioni deve avere una lunghezza compresa tra 100 e 300 millisecondi, preferibilmente 1/6 secondo (167 millisecondi) o 1/4 secondi (250 millisecondi). (Le esperienze speciali e il feedback sullo stato di avanzamento possono essere più lunghi). Usare tempi di animazione più veloci per operazioni più frequenti. In genere, le animazioni più lunghe importano più tempo per essere completate, importano più tempo per comprendere e rallentano.
-   **Reattività.** Le animazioni devono iniziare entro 50 millisecondi dall'azione di avvio o dall'azione dell'utente. Gli orari di inizio più lunghi non rispondono.
-   **Accelerazione/decelerazione.** Per un aspetto naturale, la maggior parte degli effetti di animazione deve accelerare all'avvio e decelerare quando si arresta. Per ottenere un aspetto reattivo, progettare animazioni con avvio rapido. Per visualizzare le animazioni controllate, progettare le animazioni in modo da avere una superficie morbida alla fine. Sebbene si applichi agli effetti di movimento, si applica anche a qualsiasi effetto che suggerisca lo spostamento, ad esempio le ingrandimenti e persino le dissolvenze.

    ![Figura di un grafico che mostra una velocità ridotta nel tempo ](images/vis-animations-image53.png)

    La maggior parte delle animazioni dovrebbe avere avvio rapido e terminazioni morbide per avere un aspetto reattivo, ma controllato.

-   **Movimento.** Le animazioni che ritraggono il movimento in particolare devono accelerare e decelerare, quindi non usare un movimento lineare, a meno che la durata dell'animazione non sia molto breve. I movimenti devono portare il percorso dei pantaloncini dall'inizio alla fine, senza overshooting. Il percorso di movimento completo non è sempre necessario. Quando appropriato, evidenziare la fine del movimento quando rallenta e lasciare l'occhio a riempire il resto. In questo modo il movimento risulta molto più reattivo e ordinato. Quando si anima il movimento di diversi oggetti simultaneamente, è possibile assegnare loro percorsi leggermente diversi con intervalli leggermente diversi per essere più naturali.
-   **Frequenza di fotogrammi.** La maggior parte delle animazioni deve usare una frequenza di fotogrammi di 20 fotogrammi al secondo. Se l'animazione è per un'esperienza speciale o è correlata allo scopo principale del programma, prendere in considerazione l'uso di una frequenza superiore di 24 30 fotogrammi al secondo per migliorare la fluidità e il realismo.
-   **Scala.** Progettare animazioni per lavorare correttamente nell'intera gamma di utilizzo previsto. Ad esempio, le transizioni di pagina devono essere progettate per funzionare per tutte le dimensioni di pagina.
-   **Personalità.** Progettare animazioni in modo da risultare naturale, sommesso ed efficiente anziché artificiale, capriccioso o lento.

### <a name="animated-text"></a>Testo animato

-   Sebbene sia possibile visualizzare il testo utilizzando una transizione, **non animare continuamente il testo.** Il testo animato è spesso distrattivo e più difficile da leggere rispetto al testo statico. **Eccezioni**
    -   È possibile aggiungere un'animazione al testo in situazioni in cui è tradizionalmente animata e fornire un'alternativa accessibile.
    -   È possibile aggiungere un'animazione al testo se lo scopo del testo è principalmente decorativo.

![screenshot dell'interfaccia Zune progettata in modo creativo ](images/vis-animations-image13.png)

In questo esempio, Zune anima il testo ma lo scopo è principalmente decorativo. Non esiste un problema se gli utenti non leggono attentamente il testo.

### <a name="reducing-power-consumption"></a>Riduzione del consumo di energia elettrica

-   **Progettare le animazioni per ridurre il consumo di energia.** Una volta progettato correttamente, le animazioni non devono aumentare significativamente il consumo di energia. Per ridurre il consumo di energia:
    -   **Interrompi l'animazione quando la visualizzazione è disattivata.** La visualizzazione può essere disattivata allo scopo di risparmiare energia.
    -   **Non usare animazioni con esecuzione prolungata che non vengono avviate dall'utente.** Le animazioni che usano timer periodici a risoluzione elevata riducono l'efficienza del risparmio energia del processore. Inoltre, assicurarsi di disabilitare eventuali timer periodici ad alta risoluzione quando le animazioni sono completate.
    -   **Sospendere tutte le animazioni quando il sistema diventa inattivo.** Il periodo di inattività dell'utente per diventare inattivo è determinato dalle opzioni di risparmio energia nel pannello di controllo.

### <a name="accessibility"></a>Accessibilità

-   **Non usare l'animazione come unico modo per trasferire informazioni essenziali.** Le animazioni devono comunicare informazioni utili ma non critiche, perché non sono accessibili agli utenti con problemi visivi.
-   **Verificare che le informazioni equivalenti siano disponibili in altri modi,** ad esempio:

    -   **Per verifica.** Gli utenti possono determinare le informazioni equivalenti osservando la schermata o gli oggetti interessati dall'animazione.
    -   **Mediante semplice interazione.** Gli utenti possono determinare le informazioni equivalenti spostando il puntatore del mouse, facendo clic o facendo doppio clic.

    ![screenshot del home page Bing con aree sensibili ](images/vis-animations-image54.png)

    Il home page Bing ha un'animazione iniziale che rivela diverse aree sensibili. Gli utenti possono anche visualizzare le aree sensibili spostando il cursore accanto a essi.

    Si noti che "informazioni equivalenti" non significano informazioni identiche. Le informazioni potrebbero essere in un formato diverso o richiedere una deduzione semplice.

-   **Quando appropriato, impostare lo stato attivo per l'input sull'oggetto modificato durante una transizione.** In questo modo, le tecnologie per l'accesso facilitano il rilevamento delle modifiche apportate. Non modificare lo stato attivo per l'input quando l'utente usa la tastiera.
-   **Non usare animazioni o transizioni che Flash o ridimensionano rapidamente gli oggetti.** Le modifiche apportate allo schermo lampeggiante e rapido possono causare problemi per gli utenti con problemi di convulsione e altri disturbi neurologici.
-   **Consente agli utenti di disattivare le animazioni e le transizioni del programma.** Per supportare questa funzionalità, rispettare l'opzione Disattiva tutte le animazioni non necessarie nel centro di accesso facilitato di Windows.

    **Sviluppatori:** È possibile determinare se le animazioni sono abilitate tramite l'API SystemParametersInfo.

-   **Attività di progettazione presupponendo che gli utenti trasformeranno le animazioni del programma.** Assicurarsi che questa operazione non interrompa significativamente il flusso dell'attività.

Per altre linee guida sull'accessibilità, vedere [accessibilità](inter-accessibility.md).

## <a name="documentation"></a>Documentazione

-   Evitare di fare riferimento alle animazioni quando possibile. Al contrario, fare riferimento all'oggetto che viene animato e, se necessario, il tipo di animazione.
-   Non fare riferimento alle transizioni, tranne che nella documentazione tecnica. Al contrario, fare riferimento all'oggetto nello stato finale o iniziale.
-   Se l'utente avvia in modo esplicito un'animazione, usare il verbo Play; in caso contrario, utilizzare il verbo utilizzare per la documentazione tecnica.

Esempi:

-   Si saprà che un elemento richiede attenzione quando l'icona inizia a rimbalzare.
-   Selezionare prima di tutto le foto che si desidera stampare (si noti che le foto sono ingrandite al momento della selezione).
-   Usare una transizione tra dissolvenza incrociata per modificare facilmente lo stato di un oggetto.

