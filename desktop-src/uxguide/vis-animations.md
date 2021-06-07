---
title: Animazioni e transizioni
description: L'uso strategico di animazioni e transizioni può rendere il programma più facile da comprendere, essere più semplice, più naturale e di qualità superiore ed essere più coinvolgente.
ms.assetid: 9e0e9604-f051-47e4-bcd0-59fbfd38b9c1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 546c1d0a59808b54f4ffa12fc7cd034554521ca3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444762"
---
# <a name="animations-and-transitions"></a>Animazioni e transizioni

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

L'uso strategico di animazioni e transizioni può rendere il programma più facile da comprendere, essere più semplice, più naturale e di qualità superiore ed essere più coinvolgente. Tuttavia, l'uso gratuito di animazioni e transizioni può rendere il programma distratto e persino fastidioso.

Le animazioni danno l'aspetto del movimento o del cambiamento nel tempo. Usare l'animazione per fornire commenti e suggerimenti, visualizzare in anteprima l'effetto di un'azione, mostrare la relazione tra oggetti, attirare l'attenzione sul cambiamento o spiegare visivamente un'attività.

![figura del tastierino numerico con un tasto evidenziato ](images/vis-animations-image1.png)

Microsoft Windows usa un'animazione flash di sfondo per fornire un feedback che indica che l'oggetto è stato selezionato.

Le transizioni sono animazioni usate per mantenere gli utenti orientati durante le modifiche dello stato dell'interfaccia utente e le modifiche degli oggetti e per rendere tali modifiche uniformi invece che jarring. Le transizioni buone sono naturali, spesso dando l'idea che gli utenti interagiscano con oggetti reali.

![Screenshot che mostra tre dimensioni di mal tempo.](images/vis-animations-image2.png)

I desktop di Windows usano transizioni uniformi tra i rispettivi stati concisi e dettagliati.

In genere, le animazioni e le transizioni migliori vengono usate per comunicare agli utenti in modo non verbale e per rendere le modifiche di stato più naturali e meno evidenti. Al contrario, i meno efficaci sono gratuito perché non comunicano nulla o non richiamano l'attenzione non necessaria. Le animazioni sono più usate come forma secondaria di comunicazione. Devono comunicare informazioni utili ma non critiche e, per essere accessibili, gli utenti devono essere in grado di determinare informazioni equivalenti tramite altri mezzi.

**Nota:** Le linee guida relative [alla personalizzazione del software,](exper-branding.md) [all'audio](vis-sound.md)e [all'accessibilità](inter-accessibility.md) sono presentate in articoli separati.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, considerare le domande seguenti.

### <a name="animations"></a>Animazioni

Si applicano le condizioni seguenti?

-   L'animazione comunica visivamente qualcosa di utile, ad esempio fornire feedback, mostrare relazioni, cause ed effetti o attirare l'attenzione su modifiche importanti.
-   La visualizzazione dell'animazione non è essenziale. Le informazioni equivalenti possono essere ottenute in un altro modo. Gli utenti potrebbero non trarre vantaggio dall'animazione se:
    -   Le animazioni sono state disattivate.
    -   La loro attenzione è altrove.
    -   Sono ipovedenti.
    -   L'animazione viene nascosta da un'altra finestra.
    -   L'animazione non viene riprodotta a causa di prestazioni del sistema insufficienti.
-   L'animazione non influisce sulla produttività dell'utente. Una delle due versioni seguenti:
    -   Si verifica rapidamente (200 millisecondi o meno).
    -   Non interferisce con l'interazione o può essere interrotta.
    -   L'utente deve comunque attendere.
-   L'animazione non influisce sul flusso dell'utente.
    -   È al centro dell'attenzione dell'utente o richiama l'attenzione su un elemento al di fuori del centro dell'attenzione che è importante o utile per completare un'attività.
    -   È facilmente ignorabile, non distogliere o distrarre.
    -   Non diventa faticoso. Gli utenti lo trovano comunque appropriato e divertente anche dopo la visualizzazione ripetuta.

In tal caso, è consigliabile usare un'animazione.

### <a name="transitions"></a>Transizioni

Lo stato di un oggetto o di una scena cambia e si applicano tutte le condizioni precedenti per l'uso delle animazioni e di una delle condizioni seguenti?

-   La modifica dello stato è concettualmente disorientante, confusa o altrimenti difficile da comprendere.
-   La modifica dello stato è visivamente in jarring, manca di continuità o uniformità o lampeggia; o viene visualizzato innaturale, non inpolato o di qualità scadente, soprattutto se riguarda un'area di grandi dimensioni dello schermo.
-   L'uso di una transizione renderebbe la modifica dello stato più veloce.
-   La modifica dello stato è un'attenzione particolare da parte dell'utente.

In tal caso, è consigliabile usare una transizione.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Le animazioni e le transizioni sono un modo efficace per comunicare visivamente le informazioni che altrimenti richiederebbero una spiegazione del testo o potrebbero essere perse dagli utenti.

**Non corretto:**

![Screenshot della finestra di dialogo con il messaggio ](images/vis-animations-image3.png)

**Corretto:**

![figura dell'animazione che comunica visivamente ](images/vis-animations-image4.png)

L'uso di un'animazione comunica le stesse informazioni, ma in modo naturale e non intrusivo. Quale si preferisce visualizzare un migliaio di volte?

**Le animazioni e le transizioni non devono richiedere attenzione per avere esito positivo.** In realtà, vengono spesso usati per evitare di attirare l'attenzione su meccanismi di programma di cui gli utenti non devono essere a conoscenza. Molte animazioni con successo sono così naturali che gli utenti non ne sono nemmeno a conoscenza; piuttosto che gli utenti noteranno solo la loro assenza. La frequenza di occorrenza aumenta la necessità di leggerezza, quindi è possibile risparmiare effetti che richiedono attenzione per gli eventi poco frequenti che realmente richiedono l'attenzione.

![Screenshot di tutti i programmi che cambiano in freccia indietro ](images/vis-animations-image5.png)

Transizione menu Start che evita di attirare l'attenzione.

Oltre a semplificare la comprensione e l'aspetto del programma, animazioni e transizioni ben progettate sono un ottimo modo per aggiungere personalità, carattere e **stile al programma.** Possono rendere l'esperienza utente più coinvolgente e coinvolgente offrendo un'esperienza naturale e reale.

![Figura che mostra l'effetto del passaggio del mouse sul colore del pulsante ](images/vis-animations-image6.png)

Windows 7 evidenzia i pulsanti della barra delle applicazioni al passaggio del mouse in base alla posizione corrente del mouse e al colore dell'icona del programma. Questo approccio è visivamente interessante, ma sottile, trasmettendo una personalità accattivante.

**Tuttavia, le animazioni e le transizioni sono più efficaci e ben accette quando hanno uno scopo chiaro.** Devono essere usati per migliorare l'usabilità, l'uniformità e il flusso e la percezione della qualità, senza danneggiare significativamente le prestazioni.

Anche se alcuni tipi di animazioni vengono usati per attirare l'attenzione dell'utente, assicurarsi che l'attenzione sia ben disdegnata e disdegnata di interrompere il modo di pensare dell'utente. L'occhio umano è sensibile al movimento, in particolare al movimento periferico. Può essere difficile per gli utenti concentrarsi quando è presente un pulsante della barra delle applicazioni lampeggiante o un'icona dell'area di notifica rotante. **Evitare di usare animazioni per interrompere o distrarre gli utenti o attirare l'attenzione su elementi che non giustificano l'attenzione dell'utente.**

**Non corretto:**

![figura del pulsante della barra delle applicazioni evidenziato senza motivo ](images/vis-animations-image7.png)

I programmi non devono far lampeggiare il pulsante della barra delle applicazioni a meno che gli utenti non debbano eseguire immediatamente un'operazione importante. In questo caso, l'unica operazione che l'utente deve eseguire è attivare il programma.

**Usare animazioni e transizioni perché il programma ne ha bisogno, non solo perché è possibile.** Per l'accessibilità, non usare l'animazione come unico modo per trasmettere informazioni essenziali. Assicurarsi che gli utenti possano ottenere informazioni equivalenti in modo diverso.

### <a name="attributes-of-good-animations-and-transitions"></a>Attributi di animazioni e transizioni di qualità

Le animazioni e le transizioni di qualità hanno il giusto equilibrio tra questi attributi:

-   **Sono chiaramente di scopo.** Le animazioni sono utili perché devono essere, sia per comunicare informazioni, per fare in modo che un'interazione sia reale o per attirare l'attenzione su qualcosa di importante. E le animazioni con finalità sono accurate; Se un'animazione mostra che è in corso un'attività, è perché l'attività è in realtà in corso.

**Non corretto:**

![Screenshot dell'icona della batteria e dell'etichetta con carico completo ](images/vis-animations-image8.png)

In questo esempio, l'animazione mostra che viene caricata una batteria completamente carica.

-   **Aspetto uniforme e continuo.** Le animazioni buone rimuovono senza problemi le schele tra le modifiche dello stato della scena o dell'elemento mostrando le relazioni e fornendo un'idea del luogo e del contesto. La continuità consente agli utenti di comprendere come si sono trovati e come tornare a dove sono arrivati.

![Screenshot di tre anteprime della finestra della barra delle applicazioni ](images/vis-animations-image9.png)

L'anteprima della finestra della barra delle applicazioni di Windows 7 si trasforma per garantire la continuità quando l'utente passa da un programma a un altro.

-   **Sono realistici.** Le animazioni di qualità simulano le proprietà fisiche e il comportamento reali di un oggetto. Ciò consente agli utenti di prevedere e comprendere i risultati delle interazioni. Non è necessario modellare esattamente il mondo reale, ma se si usano animazioni realistiche, è necessario mantenerle coerenti con il mondo reale. Gli utenti non devono mai essere confusi o confusi dai risultati, in particolare con le animazioni usate per la manipolazione diretta.

![Figura del pulsante della barra delle applicazioni trascinato nella nuova posizione ](images/vis-animations-image10.png)

In questo esempio l'animazione "move out of the way" usata dalla barra delle applicazioni di Windows 7 è più realistica di un punto di inserimento statico.

-   **Sono autentici.** Anche gli oggetti che non si trovano nel mondo reale possono apparire naturali in base al comportamento reale di un oggetto diverso, ma correlato. Questa metafora funziona solo se la relazione comunica chiaramente lo scopo e il comportamento previsto.

![Screenshot dell'effetto in rilievo dietro la finestra spostata ](images/vis-animations-image11.png)

In questo esempio l'animazione "squeegee" della finestra usata da Windows 7 è autentica perché è coerente con il comportamento delle finestre di cristallo nel mondo reale.

-   **Usare il mapping naturale.** I mapping naturali sono fisici o culturali. Un mapping naturale basato sulla cultura, ad esempio, potrebbe iniziare dal fatto che nelle culture occidentali le persone leggono da sinistra a destra. Di conseguenza, per esprimere una sequenza temporale di oggetti, l'oggetto intermedio è corrente, gli oggetti a sinistra sono del passato e gli oggetti a destra sono in futuro. Lo spostamento da sinistra a destra è indicato in futuro nel tempo.

![Screenshot dell'indicatore di stato del lettore multimediale ](images/vis-animations-image12.png)

In questo esempio il controllo Windows Media Player ha un mapping naturale perché la riproduzione sposta la posizione da sinistra a destra.

-   **Avere personalità.** Le animazioni ben scelte sono ottimi modi per aggiungere personalità, carattere e stile al programma. Possono rendere l'esperienza utente più coinvolgente e coinvolgente. Mentre il tipo di animazione determina ciò che comunica, il modo specifico in cui viene eseguita l'animazione mostra la personalità del programma. Le animazioni buone proiettano la personalità giusta per il programma, se grave o capriccioso o in un punto qualsiasi.

![Screenshot dell'interfaccia zune progettata in modo creative ](images/vis-animations-image13.png)

In questo esempio, l'uso del testo animato e della prospettiva dinamica di Zune consente di modellarne la personalità.

-   **Aspetto reattivo.** Le animazioni buone non danneggiano la produttività dell'utente bloccando gli utenti da altre interazioni o forzando gli utenti a guardare. Non importa quanto siano naturali e coinvolgenti le animazioni del programma, nessuno vuole attenderle esclusivamente. Anche le animazioni buone sembrano reattive senza essere in jarring grazie a un avvio rapido con un pianerottolo soft. Anche le animazioni reattive traggono vantaggio dalla comunicazione rapida dello scopo. Gli utenti non devono guardare un'animazione per molto tempo solo per capire cosa sta facendo o quando è stata eseguita. Per la manipolazione diretta, le animazioni reattive sono essenziali per mantenere un'esperienza reale diretta e coinvolgente. Per essere diretti, i punti di contatto di un oggetto devono rimanere sotto il puntatore senza problemi durante la manipolazione. Qualsiasi ritardo, risposta insoddetta o perdita di contatto elimina la percezione di manipolazione diretta.

![figura del dito che tocca un touch screen ](images/vis-animations-image14.png)

In questo esempio, la transizione di panoramica del tocco è reattiva mantenendo il punto di contatto sotto il dito dell'utente durante la manipolazione.

-   **Attirare il giusto livello di attenzione.** Le animazioni buone sono in genere sottili e richiamano solo l'attenzione necessaria per soddisfare il loro scopo. Di conseguenza, non sono distratti, fastidiosi, e troppo complessi, troppo lunghi o ripetitivi. Non diventano noiosi dopo le ripetute visualizzazione.

![Screenshot dell'evidenziazione della dissolvenziazione nei nomi di file ](images/vis-animations-image15.png)

In questo esempio, Ricerca di Windows richiama temporaneamente l'attenzione sulla corrispondenza delle parole di ricerca e quindi sfumare.

-   **Aspetto speciale solo se davvero speciale.** La frequenza aumenta la necessità di una sottigliezza, quindi le interazioni comuni necessitano di animazioni semplici che comunicano un'idea semplice in modo semplice. Riservare animazioni speciali e complesse per esperienze speciali e poco frequenti.

![Screenshot di quattro cerchi che diventano logo di Windows ](images/vis-animations-image16.png)

In questo esempio, Windows usa un'animazione che riceve attenzione all'avvio per rendere l'esperienza speciale, ma tale animazione sarebbe inappropriata altrove.

Si saprà che è stato raggiunto il giusto equilibrio quando l'esperienza complessiva sarebbe danneggiata se uno di questi attributi fosse stato rimosso.

### <a name="creating-an-animation-vocabulary"></a>Creazione di un vocabolario di animazione

Le animazioni efficaci riguardano una comunicazione visiva efficace e la coerenza è fondamentale per la loro efficacia. Se si usa una transizione specifica, ad esempio il push di una scena da destra a quella successiva, questa dovrebbe essere l'unica transizione usata a tale scopo e tale transizione non deve essere usata per altri scopi. L'assegnazione di significati diversi alla stessa animazione ne danneggia la capacità di comunicare. Assegnando animazioni e transizioni specifiche a significati specifici, si crea un vocabolario di animazione.

Questo problema si applica alle animazioni e alle transizioni che hanno significato, non a quelle generiche a cui gli utenti probabilmente non assegnano un significato o a quelle il cui scopo non è evidente. Ad esempio, le animazioni come le dissolvenze e gli effetti speciali come le dissolvenze non hanno un significato particolare, quindi possono essere usate liberamente.

Un buon vocabolario assegna animazioni che modellano il comportamento fisico reale di un oggetto. Se è necessario assegnare un'animazione a un oggetto o a un'azione che non ha una controparte reale, scegliere un'animazione che mostra il comportamento dell'oggetto se fosse reale.

![Screenshot di come il passaggio del mouse rende bagliore il logo di Windows ](images/vis-animations-image17.png)

Anche se menu Start non è un oggetto reale, l'effetto al passaggio del mouse si illumina come potrebbe essere un oggetto reale quando viene attivato.

Ogni animazione in un vocabolario deve essere chiaramente distinta. Le animazioni devono avere comportamenti simili solo se le azioni associate sono correlate in modo analogo. Ad esempio, le transizioni di spostamento suggeriscono la navigazione, quindi è possibile usare transizioni di spostamento da direzioni diverse per indicare tipi diversi di navigazione.

Si saprà che le animazioni e le transizioni non comunicano bene quando gli utenti trovano i risultati confusi, sorprendenti o imprevisti. In genere, è consigliabile ottenere un singolo scopo anziché più scopi non così bene.

Idealmente, il vocabolario dell'animazione deve essere completo in tutte le aree del programma che ne hanno bisogno. Se solo alcune interazioni hanno animazioni naturali, questo richiama l'attenzione su quelle che non lo sono.

Per altre informazioni sul vocabolario delle animazioni di Windows, vedere la sezione [Modelli di](#usage-patterns) utilizzo di questo articolo.

### <a name="designing-the-right-personality"></a>Progettare la personalità giusta

Mentre il tipo di animazione determina ciò che comunica, il modo specifico in cui viene eseguita l'animazione parla alla personalità del programma e ne rinforza il marchio.

La personalità del programma deve riflettere la natura delle attività e la personalità degli utenti, quindi non è una scelta arbitraria. Una personalità ben progettata dovrebbe invece essere autentica; non provare mai a forzarlo. La personalità deve stabilire una connessione emozionale con l'utente. Alcuni fattori da considerare:

-   **Attività:** Grave o divertente; facoltativo o obbligatorio.
-   **Conseguenze:** Grave o minorenne.
-   **Costo:** Gratuito o acquistato; se acquistati, a prezzi moderati o costosi.
-   **Stato attivo dell'utente:** Gruppo relativamente ristretto di utenti di destinazione o destinatari generali.
-   **Ambiente utente:** Professionale, casuale o domestico.
-   **Età utente:** Più giovane o più vecchio.
-   **Frequenza di utilizzo:** Frequente o poco frequente.

La combinazione di questi fattori consente di determinare una personalità appropriata per il programma. Ecco alcune combinazioni adatte per i tipi comuni di programmi:

**Applicazioni di produttività**

Naturalmente, le applicazioni di produttività devono concentrarsi sulla produttività. Sebbene alcune esperienze speciali possano distinguersi, la maggior parte delle altre animazioni deve avere queste caratteristiche:

-   Small
-   Naturale, realistico
-   Sottile, sottomesso
-   Veloce ed efficiente
-   Relaxed

**Utilità**

Le utilità vengono in genere usate brevemente, quindi l'uso dell'animazione può essere più aggressivo:

-   Realistico, illustrativo, auto-esplicativo
-   Safe
-   Coinvolgente

**Intrattenimento, giochi**

Poiché l'obiettivo di questi programmi è coinvolgere e soddisfare gli utenti, le animazioni e le transizioni possono essere molto più aggressive grazie alle caratteristiche seguenti:

-   Large (possibilmente diventando parte integrante dell'esperienza)
-   Artificiale, irresismo
-   Di impatto, vibrante
-   Emotivo, giocoso, capriccioso
-   Energico

Stabilire una connessione emozionale è così importante per i programmi di intrattenimento che è accettabile modificare alcune regole se si fa in modo che gli utenti si innamorino del programma. Ad esempio, è accettabile se un'animazione o una transizione diventa noiosa dopo la centesima volta se la maggior parte degli utenti è improbabile che usi il programma che spesso.

In genere, le animazioni e le transizioni piccole, naturali, sottodue, efficienti ma meno efficaci sono la soluzione più sicura. Le transizioni con queste caratteristiche in genere accettano il percorso più breve dall'inizio alla fine, iniziano rapidamente, terminano in modo graduale e non si verificano problemi di overshoot. Inoltre, le transizioni ben progettate sono progettate per funzionare correttamente nell'intera gamma di distanze in cui verranno usate.

### <a name="animation-performance"></a>Prestazioni dell'animazione

Quando si progettano animazioni, assicurarsi che non influiscano sulla capacità degli utenti di usare il programma in modo efficiente. In genere, rendere le animazioni sufficientemente lente per soddisfare lo scopo, ma abbastanza velocemente da non interferire con la velocità di risposta, richiedere troppo attenzione o diventare noiosa.

**Non corretto:**

![figura della pagina che ruota da destra a sinistra ](images/vis-animations-image18.png)

Anche se questa animazione di trasformazione della pagina ha un aspetto coinvolgente e reale, consente di aumentare la produttività degli utenti richiedendo più tempo per ruotare le pagine.

Brevi transizioni (200 millisecondi o meno) sono un caso speciale (soprattutto quando spesso lavorano fuori da un ritardo) perché gli utenti saranno consapevoli di doverli attendere un secondo. Gli utenti sono disposti ad attendere tali animazioni se:

-   L'attesa percepita è estremamente breve (200 millisecondi o meno).
-   La transizione rende l'interazione più uniforme e naturale.
-   La transizione rende l'interazione più reattiva.
-   Qualsiasi ritardo consente all'utente di controllare l'interazione.

![figura dei pulsanti della barra delle applicazioni trascinati in una nuova posizione ](images/vis-animations-image19.png)

Gli utenti accetteranno un breve ritardo per l'animazione di riordinamento del pulsante della barra delle applicazioni perché è molto breve e rende l'interazione più naturale.

Esistono tre modi in cui le animazioni possono influire negativamente sulle prestazioni: velocità, velocità di risposta e percezione.

Per la velocità, alcune animazioni sono elementi visivi per le attività che richiedono un uso intensivo della CPU, quindi l'ultima cosa da fare è rallentare queste attività con animazioni a elevato utilizzo di CPU. Le animazioni con utilizzo elevato di CPU (animazioni "heavy") tendono a:

-   Coinvolgere molti elementi che si spostano in modo indipendente.
-   Riprodurre per una lunga durata o distanza.
-   Implica una grande quantità di spazio sullo schermo.
-   Sono a elevato utilizzo matematico.

Animazioni con un impatto minore sulle prestazioni:

-   Coinvolgere un singolo oggetto.
-   Riprodurre per una breve durata o distanza.
-   Coinvolgere una piccola quantità di spazio sullo schermo.
-   Non sono matematicamente intensive.

Per garantire prestazioni ottimali, è consigliabile usare animazioni intensive solo per le attività che non richiedono un utilizzo intensivo della CPU, mentre le animazioni leggere possono essere usate ovunque.

Per la velocità di risposta, la maggior parte delle animazioni e delle transizioni deve essere progettata in modo che gli utenti possano interagire durante l'esecuzione dell'animazione. A meno che un'animazione non sia parte di un processo, renderla indipendente dall'interazione principale dell'utente e consentire agli utenti di interromperla.

Un'animazione potrebbe non influire negativamente sulle prestazioni di un'attività in realtà, ma gli utenti potrebbero avere la percezione che lo sia. Ad esempio, non usare un'animazione che sembra pesante per un'attività lenta e a elevato utilizzo di CPU anche se non danneggia le prestazioni, perché gli utenti potrebbero concludere che l'animazione è il motivo per cui l'attività è lenta. **Se un elemento sembra lento, sarà lento, quindi è meglio usare animazioni semplici, leggere e veloci.** L'uso di animazioni con inizio snappy per attività a elevato utilizzo di CPU è utile.

**Rischioso:**

![Screenshot della finestra di dialogo copia con l'indicatore di stato ](images/vis-animations-image20.png)

Anche se l'animazione nella finestra di dialogo di copia file di Windows non danneggia le prestazioni di copia dei file, rischia di fare in modo che gli utenti lo pensino.

**Rischioso anche:**

![Screenshot dello stato di avanzamento visualizzato nella barra degli indirizzi ](images/vis-animations-image21.png)

In questo esempio, l'animazione dello stato di avanzamento dell'aspetto lento nella barra Esplora risorse degli indirizzi rende alcune attività estremamente lente.

Le animazioni e le transizioni non hanno alcun valore se la qualità è così scarsa da rendere l'esperienza meno uniforme e meno coinvolgente. Per mantenerne la qualità, le animazioni devono essere progettate in modo da ridurre le prestazioni normalmente quando non sono disponibili risorse di sistema sufficienti. Le animazioni possono peggiorare con variazioni che richiedono meno risorse (ad esempio lunghezze più brevi o frequenze dei fotogrammi inferiori) o addirittura non in esecuzione. Indipendentemente dalle risorse disponibili, assicurarsi che le animazioni siano di alta qualità e siano simili alle animazioni anziché ai bug software.

Infine, se gli utenti ritengono che le animazioni e le transizioni del programma distoglino dalla produttività, è probabile che alcuni utenti vogliano disattivarle. Per supportare questa funzionalità, rispetta l'opzione **Disattiva tutte le animazioni non necessarie** presenti in Windows Centro accessibilità.

### <a name="attracting-the-right-level-of-attention"></a>Attirare il giusto livello di attenzione

Anche se solo alcuni tipi di animazioni e transizioni sono progettati specificamente per attirare l'attenzione dell'utente, devono essere progettati per attirare il livello di attenzione giusto per soddisfare bene lo scopo. Quali sono i diversi modi per attirare l'attenzione e come si sceglie quello giusto?

**Effetti di animazione**

Diversi effetti di animazione attraggono livelli di attenzione diversi. L'elenco seguente riepiloga i metodi più comuni, a partire da quello più attento:

-   **Flashing rapido.** Richiede attenzione immediata. Può interrompere la concentrazione degli utenti indipendentemente dal punto in cui si verifica il flashing.
-   **Lampeggiamento moderato.** Uguale, ma richiede meno attenzione con una frequenza inferiore.
-   **Rimbalzare.** Evidente nella visione periferica e per natura relativamente impegnativa. È probabile che gli utenti se ne accortino, ma possono continuare a concentrarsi altrove solo se la durata è breve.
-   **Movimento.** Evidente nella visione periferica, ma non impegnativa. Tuttavia, i movimenti complessi o 3D attraggono più attenzione dei movimenti semplici o 2D. È probabile che gli utenti se ne accorano, ma possono continuare a concentrarsi altrove.
-   **Pulsazione moderata.** Evidente ma senza distrazioni nella visione periferica. Gli utenti possono continuare a concentrarsi altrove. Può pulsarsi di luminosità, colori e dimensioni.
-   **Pulsazione lenta/alone.** Evidente ma sottile. Attrae più attenzione rispetto a un effetto statico, ma gli utenti potrebbero non notare l'animazione a meno che non lo cerchino già.
-   **Dissolvenza.** Ancora meno evidente. Attrae più attenzione rispetto a un effetto statico, ma gli utenti potrebbero non notare l'animazione a meno che non lo cerchino già.
-   **Evidenziazione/gleam statica.** Evidente se gli utenti scelgono di guardare, ma non richiedono attenzione se si trova altrove.
-   **Ambiente/naturale.** Intenzionalmente non è evidente con un aspetto naturale e reale.

Per determinare l'approccio giusto per il programma o la funzionalità, considerare in che modo questi fattori sono correlati agli scenari della funzionalità.

Si supponga, ad esempio, di progettare un programma di messaggistica istantanea e che qualcuno abbia appena inviato un messaggio all'utente. Questo scenario richiede l'attenzione dell'utente, dovrebbe essere evidente ovunque e in genere l'utente vorrà rispondere rapidamente. Questo scenario suggerisce che un'animazione flashing moderata sarebbe una scelta ottimale. Si supponga invece di voler informare gli utenti che un processo di stampa è stato completato. Gli utenti devono essere in grado di continuare a concentrarsi e a lavorare in modo produttivo altrove ed è accettabile se gli utenti non lo notano. Questo scenario suggerisce che una pulsazione da moderata a lenta o incandescente sarebbe una scelta ottimale.

**Duration**

La durata appropriata per un'animazione che riceve attenzione dipende dallo scenario e dal tipo specifico di animazione usato. Maggiore è l'attenzione richiesta da un effetto di animazione, più breve sarà la durata. Mentre gli effetti molto piccoli che richiedono una piccola attenzione (ad esempio pulsazione lenta) possono essere riprodotti all'infinito, gli effetti che richiedono attenzione devono essere riprodotti solo da 1 a 3 secondi. Qualsiasi elemento più lungo rischia di rendere l'animazione travolgente e fastidiosa.

![Screenshot del pulsante della barra delle applicazioni evidenziato ](images/vis-animations-image22.png)

In Windows 7 la barra delle applicazioni lampeggia solo per un secondo. Non sarebbe più noioso.

**Decadimento dell'effetto**

È consigliabile progettare animazioni che consentono di ricevere attenzione in base al presupposto che, se gli utenti non rispondono immediatamente, è perché sono occupati a eseguire altre attività e non vogliono essere interrotti. L'obiettivo dovrebbe quindi essere quello di attirare l'attenzione senza richiederla.

Per ottenere il giusto equilibrio tra attirare l'attenzione senza richiederla, decadimento dell'intensità di un effetto nel tempo. Ad esempio, per attirare l'attenzione, è possibile rendere l'effetto inizialmente forte, ma quindi rallentare rapidamente l'effetto. In questo modo, la potenza interessante è determinata principalmente dall'effetto iniziale, ma l'impressione complessiva dell'utente è determinata principalmente dalla sua fine.

![Screenshot che illustra una frequenza flash ridotta ](images/vis-animations-image23.png)

In Windows 7 l'effetto flash della barra delle applicazioni rallenta alla fine.

### <a name="what-about-powerpoint"></a>Che ne è di PowerPoint?

Le transizioni di Microsoft PowerPoint spesso violano intenzionalmente queste linee guida perché sono progettate per attirare l'attenzione sulle transizioni di scorrimento e richiedere agli utenti di attenderle. Inoltre, non hanno alcun significato particolare, quindi non comunicano nulla oltre il fatto che una diapositiva sta cambiando.

Le transizioni di tipo PowerPoint, se usate correttamente, hanno gli scopi seguenti:

-   Le presentazioni lunghe vengono suddivise in blocchi più piccoli forzando la sospensione del presentatore.
-   Richiamano l'attenzione del pubblico verso i cambiamenti nella presentazione, consentendo alle persone di concentrarsi di nuovo se si sono chiesti.
-   Assegnano un ritmo alla presentazione in modo che non si senta monotona o opprimente.
-   Il loro stile riflette la personalità del presentatore o del materiale.

Anche se questi sono obiettivi importanti per una presentazione, tali transizioni richiamano l'attenzione non necessaria nell'interfaccia utente della maggior parte dei tipi di programmi e diventano rapidamente noiosi.

**In basso:** Non usare transizioni di tipo PowerPoint come modello per il programma.

**Se si eservino solo sei operazioni...**

1.  Usa animazioni e transizioni per rendere il programma più facile da comprendere e risultare più semplice e coinvolgente. Devono avere uno scopo chiaro. Non usare animazioni solo perché è possibile o per attirare l'attenzione non necessaria sul programma.
2.  Definire un vocabolario di animazione e usarlo in modo coerente in tutto il programma. Usare il vocabolario dell'animazione di Windows 7 quando appropriato.
3.  Usare le caratteristiche delle animazioni per dare personalità al programma e rafforzare il proprio marchio.
4.  Rendere la maggior parte delle animazioni semplice, breve e sottile. Tenere presente che le animazioni non devono richiedere attenzione per avere esito positivo. Se un'animazione è appropriata e naturale, gli utenti noteranno solo la sua assenza.
5.  Rendere le animazioni veloci e reattive e renderle più leggere. Indipendentemente da quanto siano coinvolgenti le animazioni, nessuno vorrà aspettarle. Progettare animazioni più pesanti per ottenere una riduzione delle prestazioni.
6.  Progettare a lungo termine. Se un'animazione è fastidiosa, distrazione o noiosa, riprogettarla o rimuoverla.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le animazioni hanno diversi modelli di utilizzo:



|   Utilizzo                                                                                                               |   Descrizione                                     |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Feedback al passaggio del mouse**<br/> per mostrare dove si trova il punto di interazione. <br/>                                | Indica che il punto di interazione è attivo. Il passaggio del mouse può essere visualizzato anche tramite un effetto statico.<br/> vocabolario windows: visualizza l'effetto al passaggio del mouse (rettangolo di delimitazione, evidenziazione, ingrandimento) con effetto di dissolvenza in entrata/uscita per uniformità. <br/> ![Screenshot di una delle sei cover degli album evidenziate ](images/vis-animations-image24.png)<br/> Nel lettore multimediale digitale Zune, l'album copre l'evidenziazione e aggiunge i controlli di riproduzione al passaggio del mouse.<br/>                                                                                                                                                                                                                 |
| **Fare clic su Commenti e suggerimenti**<br/> per mostrare che un oggetto selezionabile è reattivo e ha ricevuto un clic. <br/>    | Indica che è stato fatto clic su un oggetto .<br/> vocabolario windows: sfondo dell'oggetto flash in caso di evento click-down. per visualizzare il contatto tocco, usare un effetto ondulato. <br/> ![foto del dito sul touchscreen che mostra le increspature ](images/vis-animations-image25.png)<br/> Il tocco visualizza un'animazione ondulata in modo che l'utente sappia che l'interazione è stata riconosciuta.<br/>                                                                                                                                                                                                                                                                                                         |
| **Feedback sulla selezione**<br/> per mostrare che un oggetto è selezionato. <br/>                                | Indica che è selezionato un oggetto . La selezione può essere visualizzata anche tramite un effetto statico.<br/> vocabolario windows: disegnare un rettangolo di selezione con un effetto di dissolvenza in entrata/uscita per uniformità. <br/> ![figura di una cover dell'album selezionata e quindi selezionata ](images/vis-animations-image26.png)<br/> In Zune l'album copre il lampeggiamento quando si fa clic e quindi ottiene un rettangolo di selezione alla selezione.<br/>                                                                                                                                                                                                                                                                      |
| **Feedback sullo stato di avanzamento**<br/> per mostrare che è in corso l'esecuzione di un'attività. <br/>                             | Il feedback sullo stato di avanzamento indica che un'attività è in corso, in genere con indicatori di attività, indicatori di stato o animazioni che illustrano l'attività. Determinate informazioni sullo stato di avanzamento indicano approssimativamente la quantità di attività eseguita e la quantità che rimane, mentre lo stato di avanzamento indeterminato indica solo che l'attività è in corso.<br/> vocabolario windows: indicatori di attività rotanti, indicatori di stato, sfondi di stato, animazioni di illustrazioni. <br/> ![Screenshot della finestra di dialogo con il testo "accesso" ](images/vis-animations-image27.png)<br/> In questo esempio, Windows Live Messenger visualizza un feedback sullo stato di avanzamento indeterminato durante l'accesso.<br/> |
| **Attrattore**<br/> per mostrare che qualcosa richiede l'attenzione dell'utente. <br/>                          | Attirare il livello di attenzione giusto quando vengono creati oggetti significativi o è necessaria attenzione (spesso a causa di modifiche) o si verificano eventi importanti o urgenti. vedere [l'interesse per il livello di attenzione per](#attracting-the-right-level-of-attention) le tecniche di progettazione.<br/> vocabolario windows: lampeggiamento, spostamento, pulsazione, incandescente, bagliore. <br/> ![Screenshot che illustra l'animazione della barra degli strumenti ](images/vis-animations-image28.png)<br/> La barra degli strumenti di Windows Live viene animata al primo aspetto per renderla evidente dove si trova.<br/>                                                                                                                                 |
| **Relazione**<br/> per mostrare la relazione tra oggetti o la causalità negli effetti. <br/>        | Mostrare le relazioni, soprattutto quando la relazione potrebbe non essere compresa o prevista, in modo che non distragga o confonda.<br/> vocabolario windows: modifica, trasporto, modifica fisica, ad esempio capovolgimento, crescita da un'origine punto, riduzione a una destinazione punto. <br/> ![Screenshot della finestra di dialogo di calibrazione colori](images/vis-animations-image29.png)<br/> In questo esempio, l'animazione mostra la relazione tra l'impostazione gamma e il relativo effetto sullo schermo.<br/>                                                                                                                                                    |
| **Illustrazione/Anteprima**<br/> per spiegare visivamente un concetto, un'attività o l'effetto di un comando. <br/> | Animazione o video che illustra un concetto o il funzionamento visivo di un elemento, per integrare o sostituire una spiegazione testuale. In questo modo gli utenti possono eseguire attività o scegliere i comandi in modo efficiente e sicuro. <br/> ![Screenshot della penna che corregge l'errore di ortografia ](images/vis-animations-image30.png)<br/> In questo esempio i comandi "show me" del Pannello di input di Tablet PC usano illustrazioni per illustrare come correggere, eliminare, dividere e unire.<br/>                                                                                                                                                                                                        |



 

Le transizioni hanno diversi modelli di utilizzo:



|      Utilizzo                                                                                                                                                                                                      |    Descrizione                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dimensioni dell'oggetto/riduzione/visualizzazione**<br/> per modificare le dimensioni o lo stato di un oggetto senza problemi. <br/>                                                                                                         | L'oggetto cambia tra gli stati, possibilmente durante lo spostamento. la transizione mantiene gli utenti orientati durante le modifiche.<br/> vocabolario windows: morph, change size, object slitte in o out. <br/> ![Screenshot di tre dimensioni di tempo in mal tempo ](images/vis-animations-image31.png)<br/> In questo esempio Weather Weather Weather Si trasforma dal relativo stato conciso per visualizzare la relativa finestra di dialogo Opzioni.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Visualizzazione/nascondi/modifica del contenuto**<br/> per mostrare, nascondere o modificare il contenuto senza problemi, in genere per la divulgazione progressiva. <br/>                                                                       | Le forme interne della finestra vengono rimodellate per visualizzare contenuto più, meno o diverso. la transizione mantiene gli utenti orientati durante le modifiche.<br/> vocabolario windows: il riquadro scorre in o fuori. Le finestre a comparsa vengono dissolvenza in entrata e in uscita. dissolvenza o roll-in di contenuti diversi. <br/> ![Screenshot di tre dimensioni della calcolatrice ](images/vis-animations-image32.png)<br/> Il Calcolatrice Windows ha una transizione uniforme tra le modalità di visualizzazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Visualizzazione/visualizzazione del controllo o dell'affordance**<br/> per mostrare o nascondere in modo uniforme i controlli o i relativi affordance al passaggio del mouse o al passaggio del mouse per semplificare l'aspetto visivo normale. <br/>                | Visualizza i controlli quando gli utenti passano il puntatore del mouse su un'area dei comandi o visualizzano gli affordance quando gli utenti passano il puntatore del mouse su un controllo. Il passaggio del mouse su queste aree indica che l'utente intende interagire. Gli affordance possono nascondersi se il puntatore diventa stazionario. <br/> ![Screenshot dei controlli in dissolvenza prima del passaggio del mouse ](images/vis-animations-image33.png)<br/> In questo esempio, i controlli Windows Media Player dissolvenza al passaggio del mouse quando sono in modalità schermo intero.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Transizioni di scena**<br/> per rendere la transizione di una scena uniforme e trasparente per evitare l'attenzione. <br/>                                                                                   | Le modifiche improvvie della scena possono essere stridenti, in particolare per le aree dello schermo di grandi dimensioni, quindi usare le transizioni della scena per creare uniformità e continuità e fornire contesto. Le transizioni di scena sono progettate per essere una chiave naturale e bassa, per evitare di richiamare l'attenzione sul processo di transizione stesso.<br/> vocabolario windows: dissolvenza in entrata/uscita; dissolvenza incrociata; scorrimento in/sinistra, out/right, up, down; push e coperture. <br/> ![Screenshot di una foto che sbiade in un'altra ](images/vis-animations-image34.png)<br/> In questo esempio, lo sfondo del desktop di Windows si dissolve tra le immagini in modo da rendere la transizione uniforme e controllata.<br/>                                                                                                                                                                                                                                                                                                                               |
| **Transizioni di scena speciali**<br/> per attirare l'attenzione su una modifica della scena per renderla speciale o riorientare l'attenzione dell'utente. <br/>                                                               | Anche se la maggior parte delle transizioni di scena non deve richiamare l'attenzione sul processo di transizione, alcune sono progettate per interrompere il flusso e attirare l'attenzione per sottolineare che sta per verificarsi qualcosa di diverso. per attirare l'attenzione, le transizioni speciali della scena sono progettate per essere innaturali e avere un impatto visivo elevato. <br/> ![Screenshot della diapositiva di transizione che cattura l'attenzione ](images/vis-animations-image35.png)<br/> In questo esempio, PowerPoint usa transizioni per attirare l'attenzione per attirare il pubblico nella modifica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Manipolazioni dirette**<br/> per mostrare l'effetto delle manipolazioni dirette (ad esempio spostamento, scorrimento/panoramica, rotazione e zoom). <br/>                                                                   | La transizione mostra l'effetto della manipolazione in tempo reale. l'effetto dovrebbe essere uniforme, continuo e coerente con il mondo reale. Lo spostamento e la rotazione potrebbero non essere continui in alcune posizioni per indicare restrizioni o scelte probabilmente preferite. Lo zoom rende il contenuto più grande o più piccolo, modificando eventualmente il livello di dettaglio di conseguenza. <br/> ![Screenshot di tre dimensioni di lente di ingrandimento ](images/vis-animations-image36.png)<br/> In questo esempio Lente di ingrandimento esegue lo zoom uniforme tra i livelli.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Modifiche dirette non corrette**<br/> per indicare che è stata tentata una manipolazione diretta ,ad esempio spostamento, scorrimento/panoramica, ma non è stato possibile eseguire questa operazione. <br/>                                           | La transizione mostra la manipolazione tentata, ma ripristina lo stato originale. spesso l'effetto sembra che la manipolazione non possa essere eseguita a causa di alcune restrizioni fisiche reali. queste animazioni vengono usate al posto dei messaggi di errore basati su testo, che interromperebbero l'aspetto reale della manipolazione.<br/> vocabolario windows: bounce <br/> ![Figura dell'animazione che comunica visivamente ](images/vis-animations-image4.png)<br/> In questo esempio il documento viene restituito per mostrare che l'utente ha raggiunto la fine.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Ordinare, filtrare, riordinare le transizioni**<br/> per indicare che la presentazione o il contenuto di una raccolta di elementi è stato modificato. <br/>                                                            | La transizione mostra (o per modifiche complesse, suggerisce) l'effetto della modifica. <br/> ![Screenshot di righe fotocamere con tre fotocamere rimosse ](images/vis-animations-image37.png)<br/> ![screenshot simile con diverse fotocamere rimosse ](images/vis-animations-image38.png)<br/> ![screenshot simile con altre fotocamere rimosse ](images/vis-animations-image39.png)<br/> In questo esempio la ricerca visiva Bing usa una transizione di filtro.<br/> ![Screenshot della copertina dell'album che ne modifica l'aspetto ](images/vis-animations-image40.png)<br/> In questo esempio, Windows Media Center usa una transizione di riordino come esperienza speciale durante la riproduzione di un brano.<br/>                                                                                                                                                                                                                                                                                   |
| **Transizioni delle prestazioni**<br/> per fare in modo che un'azione venga eseguita più rapidamente. <br/>                                                                                                              | Anche se qualsiasi transizione può rendere un'azione più rapida, lo scopo principale di queste transizioni è migliorare la percezione delle prestazioni e della velocità di risposta. una buona tecnica consiste nel mostrare l'attività eseguita in passaggi intenzionali. al contrario, il ritardo dell'azione, il rendering dei risultati in modo casuale o l'uso di un indicatore di attività saranno lenti.<br/> vocabolario windows: eseguire azioni in fasi, con transizioni fluide tra le fasi. <br/> ![Screenshot dell'aggiunta jump list destinazioni ](images/vis-animations-image41.png)<br/> In questo esempio, una barra delle Jump List visualizza immediatamente gli elementi standard e quindi scorre verso l'altro per visualizzare le destinazioni quando l'elenco è pronto. In questo modo viene nascosto il tempo necessario per compilare l'elenco. Al contrario, il ritardo della visualizzazione iniziale non risponde e la visualizzazione di un elenco incompleto o un feedback sullo stato di avanzamento si sentirebbe molto più lenta.<br/> |
| **Esperienze speciali**<br/> per coinvolgere e dilettare gli [](glossary.md) utenti durante esperienze speciali poco frequenti che sono importanti per il programma e hanno la massima attenzione dell'utente. <br/>    | Anche se qualsiasi transizione può essere un'esperienza speciale, queste transizioni sono meglio riservate alle esperienze poco frequenti realmente speciali per il programma. Le transizioni personalizzate vengono usate per offrire un aspetto speciale. la personalizzazione e la personalità sono spesso elementi di progettazione importanti. A differenza di altri modelli, le esperienze speciali possono richiedere attenzione, essere pesanti e richiedere agli utenti di attendere un momento. Di conseguenza, queste transizioni si consumano rapidamente se sovrautilizzate perché l'esperienza non è più speciale. <br/> ![Screenshot del logo di Windows che cambia in nuova schermata ](images/vis-animations-image42.png)<br/> In questo esempio Windows Media Center visualizza un'animazione durante il caricamento per coinvolgere immediatamente gli utenti.<br/>                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Indicazioni

### <a name="effective-communication"></a>Comunicazione efficace

-   **Definire e usare un vocabolario** di animazione per assicurarsi che le animazioni e le transizioni abbia un significato coerente e usarlo in modo coerente in tutto il programma. La maggior parte dei vocabolari deve includere voci per l'aspetto e la scomparsa di scene e oggetti, la navigazione, l'interazione di base (passaggio del mouse, selezione, clic), la manipolazione e l'interazione degli oggetti (spostamento, eliminazione, ridimensionamento, scorrimento, panoramica, zoom, rotazione, filtro) e attirare l'attenzione. Un significato coerente è fondamentale per una comunicazione efficace.
-   **Quando pratico, usare il vocabolario di animazione di Windows.** Anche se il programma può avere un pubblico diverso e esigenze diverse, spesso i vantaggi della coerenza e della familiarità superano i vantaggi dell'essere diversi. Se il vocabolario del programma deve essere diverso, usare gli stessi tipi di animazione di base di Windows, ma fornire loro la personalità giusta per il programma.
-   **Non assegnare significati specifici ad animazioni e transizioni generiche in un vocabolario di animazione.** Le transizioni generiche, come le dissolvenze e gli effetti speciali come le dissolvenze, non hanno un significato particolare (oltre che appaiono o scompaiono), quindi possono essere usate liberamente.

    **Non corretto:**

    ![Screenshot di una finestra di dialogo che si dissolve in un'altra ](images/vis-animations-image43.png)

    In questo esempio, una dissolvenza incrociata viene usata erroneamente per passare all'elemento successivo. Poiché le dissolvenze incrociate non hanno un significato particolare, questa transizione non fornisce il contesto.

-   **Rendere chiaramente distinte le voci del vocabolario.** Le azioni correlate possono avere effetti simili (ad esempio, lo zoom avanti e indietro deve avere transizioni inverse), ma le azioni non correlate devono avere effetti chiaramente distinti (ad esempio, lo zoom non deve mai essere confuso con la rotazione).
-   **Mantenere realistici e coerenti gli effetti reali.** Se si usano animazioni e transizioni realistiche, mantenere l'esperienza coerente con il mondo reale. Gli utenti non devono mai essere confusi, confusi o fuorsi dai risultati. Per coerenza, non combinare metafore.
-   **Assegnare animazioni inverse ad azioni inverse.** Questa operazione soddisfa le aspettative degli utenti e semplifica il vocabolario. Ad esempio, se un riquadro viene visualizzato scorrendo, rimuoverlo scorrendo non con altri effetti.
-   **Rendere comprensibili le animazioni.** Gli utenti devono essere in grado di comprendere rapidamente lo scopo di un'animazione. È possibile rendere un'animazione troppo piccola, troppo breve (meno di 50 millisecondi) o così sottile che gli utenti non sono in grado di comprendere lo scopo. In questi casi, riprogettare per rendere chiaro il significato o rimuovere.

    **Non corretto:**

    ![Screenshot dell'animazione durante l'eliminazione della finestra di dialogo ](images/vis-animations-image44.png)

    In questo esempio l'effetto è così piccolo e sottile che pochi utenti possono comprenderne lo scopo. È meglio riprogettare o rimuovere.

### <a name="patterns"></a>Modelli

**Commenti e suggerimenti al passaggio del mouse**

-   **Per apparire reattivo, cercare di riprodurre l'animazione entro 50 millisecondi dall'immissione o dalla fine dello stato del passaggio del mouse.**
-   **Per apparire rapidamente, impostare la durata delle animazioni al passaggio del mouse su un valore inferiore a 50 millisecondi.**
-   **Usare un effetto dissolvenza in entrata/uscita dal passaggio del mouse.** In questo modo, gli effetti del passaggio del mouse sono chiaramente distinti dal feedback su clic e selezione.

**Fare clic su Commenti e suggerimenti**

-   **Per apparire reattivo, cercare di riprodurre l'animazione entro 50 millisecondi dall'evento click down.** Gli eventi click-up non necessitano di commenti e suggerimenti.
-   **Per apparire rapidamente, impostare la durata delle animazioni clic su meno di 50 millisecondi.**
-   **Usare un effetto flash o lampeggiamento in background.** In questo modo, gli effetti del clic sono chiaramente distinti dal feedback al passaggio del mouse e dalla selezione. Poiché per fare clic è necessario passare il puntatore del mouse, è possibile aggiungere commenti e suggerimenti al passaggio del mouse.

**Feedback sulla selezione**

-   **Per apparire reattivo, cercare di riprodurre l'animazione entro 50 millisecondi dalla selezione o dalla deselezione.**
-   **Per apparire rapidamente, impostare la durata delle animazioni di selezione su un valore inferiore a 50 millisecondi.**
-   **Usa un effetto rettangolo di selezione con dissolvenza in entrata/uscita.** In questo modo la selezione è chiaramente distinta dal passaggio del mouse e dal feedback del clic.

**Feedback sullo stato di avanzamento**

-   **Usare un indicatore di attività quando non è possibile eseguire un'azione entro un secondo.** Questa operazione indica che il comando è stato ricevuto.
-   **Usare un indicatore di stato quando un'attività può richiedere più di cinque secondi.** Per altre linee guida, vedere [ProgressBars](progress-bars.md).
-   **Usare animazioni di feedback sullo stato di avanzamento che consentono agli utenti di visualizzare l'effetto delle attività a esecuzione lunga.** Evitare animazioni di feedback sullo stato di avanzamento non necessarie se un'animazione non comunica nulla di utile, usare invece un indicatore di stato.
-   **Avere stati di completamento e di errore chiaramente identificabili.** Gli utenti devono essere in grado di determinare rapidamente questi stati finali.
-   **Interrompere la visualizzazione dello stato di avanzamento quando l'attività sottostante non è in corso.** Gli utenti devono essere in grado di determinare se lo stato di avanzamento non viene effettuato e reagire di conseguenza.

**Attrattori**

-   **Usare gli attrattori con un'attenzione.** A meno che le informazioni non siano urgenti, critiche o che potrebbero influire sul comportamento immediato dell'utente, è in genere meglio modificare lo stato in modo nonspicuo e consentire agli utenti di individuare la modifica da soli. [Risolvere le distrazioni, non l'individuabilità.](/windows/desktop/uxguide/how-to-design-desktop-ux)

    ![Screenshot delle icone di stato wireless ](images/vis-animations-image45.png)

    In questo esempio, l'icona dell'area di notifica della rete wireless usa un'animazione per i problemi critici, ma consente agli utenti di individuare i segnali deboli da soli.

-   **Scegliere un'animazione che disegna il livello di attenzione giusto.** Le animazioni di attrattore devono attirare solo l'attenzione su se stesse per soddisfare il proprio scopo, ma non di più. Se l'utente deve agire immediatamente, scegliere un effetto che richiede attenzione indipendentemente dalla posizione in cui l'utente sta cercando. Per altre situazioni, vedere la sezione [Attrarre](#attracting-the-right-level-of-attention) il livello di attenzione giusto per ottenere la giusta combinazione di attenzione, personalizzazione ed urgenza.

    **Non corretto:**

    ![screenshot dell'assistente per l'ufficio paperclip ](images/vis-animations-image46.png)

    Gli Microsoft Office hanno attratto l'attenzione non necessaria su se stessi.

-   **Se l'utente non risponde, non ripetere l'animazione o usare animazioni continue.** Si supponga invece che l'utente abbia scelto di non agire ora, ma che possa agire in un secondo momento. Le animazioni continue rendono difficile per gli utenti concentrarsi su qualsiasi altro elemento.

**Animazioni delle relazioni**

-   **Usare animazioni di relazione per mostrare da dove provenivano gli oggetti o da dove sono passati.**
-   **Le animazioni di relazione devono iniziare o terminare con l'oggetto selezionato.** Non mostrare le relazioni tra gli oggetti con cui l'utente attualmente non interagisce. Se gli utenti notano affatto, ciò che noteranno è la distrazione.

**Illustrazioni/anteprime**

-   **Usare le anteprime per mostrare l'effetto di un comando senza che gli utenti lo devono eseguire prima.** Usando le anteprime utili, è possibile migliorare l'efficienza e la facilità di apprendimento del programma e ridurre la necessità di tentativi ed errori.
-   **Usare illustrazioni e anteprime con un'interpretazione chiara.** Hanno poco valore se confondono.
-   **Riprodurre una sola illustrazione alla volta per** evitare di travolgere gli utenti. Se sono possibili più illustrazioni simultanee, usare il passaggio del mouse o un pulsante di riproduzione per consentire agli utenti di indicare il proprio interesse.
-   **Riprodurre automaticamente un'illustrazione se è lo scopo principale della finestra o della pagina.** In caso contrario, se è facoltativo, consentire agli utenti di riprodurlo quando sono pronti.
-   **Riprodurre animazioni alla velocità** ottimale: non sono così veloci da comprendere, ma non sono così lente da guardare.

**Aumentare/ridurre l'oggetto**

-   **Non ritagliare il contenuto durante un ridimensionamento.** Espandere i contenitori prima di aggiungere contenuto. Rimuovere il contenuto prima di ridurre i contenitori.

    **Non corretto:**

    ![Screenshot della calcolatrice troncata ](images/vis-animations-image47.png)

    In questo esempio il contenuto viene ritagliato durante un ridimensionamento.

**Visualizzazione/nascondi/modifica del contenuto**

-   **Visualizzare informazioni importanti in modo statico.** Gli utenti non devono accedere a informazioni importanti attraverso la divulgazione progressiva.

**Visualizzazione/visualizzazione del controllo o dell'affordance**

-   **Visualizza controlli importanti quando l'utente posiziona il puntatore del mouse in un punto qualsiasi all'interno della finestra o del riquadro o, se a schermo intero, durante lo spostamento del mouse.** Gli utenti non devono cercare questi controlli, quindi assicurarsi che l'individuazione sia certa.

    ![Figura che mostra come il passaggio del mouse visualizza i controlli ](images/vis-animations-image48.png)

    In questo esempio, Windows Media Center visualizza i controlli ogni volta che il puntatore si trova sopra la finestra.

-   **Visualizzare i controlli secondari o gli affordance dei controlli quando l'utente posiziona il puntatore sopra o vicino ai comandi.** Per semplificare l'individuazione, rendere la posizione ovvia e la destinazione di grandi dimensioni.

    ![Screenshot del puntatore che rivela il comando secondario ](images/vis-animations-image49.png)

    In questo esempio, Windows Live Messenger visualizza un comando secondario quando il puntatore si trova vicino all'angolo superiore destro.

**Transizioni della scena**

-   **Rendere coerenti le transizioni fisiche della scena con il mapping naturale.** Le persone leggono da sinistra a destra nelle culture occidentali e i diagrammi gerarchici scorrono dall'alto verso il basso. Di conseguenza, il futuro nel tempo è indicato dal movimento da sinistra a destra. Le transizioni della scena fisica seguenti hanno un mapping naturale:



    | Transizione                          | Significato                                     |
    |---------------------------|--------------------------------------|
    | Da sinistra<br/>      | Tornare al flusso di attività<br/>    |
    | Da destra<br/>     | Procedere nel flusso di attività<br/> |
    | Dall'alto<br/>       | Spostare verso l'alto la gerarchia delle attività<br/>    |
    | Dal basso<br/>    | Spostare verso il basso la gerarchia delle attività<br/>  |



 

-   **Se il programma riproduce audio, le transizioni della scena di progettazione e le transizioni audio insieme.** Ad esempio, se una scena si dissolve gradualmente, anche qualsiasi suono dovrebbe dissolversi gradualmente. Non creare transizioni visive senza problemi grazie a transizioni sonore improvvate. Per altre linee guida, vedere [Audio.](vis-sound.md)

**Manipolazioni dirette**

-   **Quando si usano movimenti fisici nell'interazione (ad esempio, il movimento), progettare l'animazione in modo che si senta come una risposta naturale al movimento.** Collegare la causa dell'interazione all'effetto di transizione. Assegnare all'animazione caratteristiche fisiche reali, ad esempio accelerazione, decelerazione, accelerazione, tolleranza, peso, rimbalzo e rotazione.
-   **Per mantenere un aspetto diretto, mantenere i punti di contatto di un oggetto sotto il puntatore senza problemi durante l'interazione.** Qualsiasi ritardo, risposta concisa o perdita di contatto elimina la percezione della manipolazione diretta. Gli oggetti non devono mai scomparire durante la manipolazione.

**Ordinare, filtrare o riordinare le transizioni**

-   **Per le modifiche semplici, mostrare l'intera transizione.** Gli utenti potranno seguire facilmente l'intera transizione. Le modifiche semplici riguardano al meno quattro elementi.
-   **Per modifiche complesse, evidenziare la fine del movimento mentre rallenta e lasciare che l'occhio riempia il resto.** In questo modo il movimento è molto più reattivo e ordinato.

**Transizioni delle prestazioni**

-   **È consigliabile eseguire transizioni lente in due o tre fasi per renderle più veloci e immediatamente interattive.** Usare l'ordine di composizione seguente quando appropriato:
    -   Frame esterno
    -   Sfondo
    -   Contenuto iniziale (usando una rappresentazione temporanea, se necessario)
    -   Controlli principali (in modo che gli utenti possano interagire immediatamente)
    -   Controlli secondari ed eventuali elementi rimanenti dell'interfaccia utente
    -   Contenuto finale (se è stata usata una rappresentazione temporanea) Usare transizioni come dissolvenze e diapositive per rendere la composizione uniforme, ordinata e perfezionata.

![screenshot della mappa con foto satellitari e griglia ](images/vis-animations-image50.png)

Quando si scorre la visualizzazione "Occhio d'occhio", le mappe bing visualizzano uno sfondo temporaneo della griglia. In questo modo gli utenti possono continuare a scorrere immediatamente, ben prima che venga eseguito il rendering del contenuto finale.

**Animazioni con esperienza speciale**

-   **Riconsiderare le schermate iniziali animate (nonché le schermate iniziali statiche).** Spesso le schermate iniziali richiamano semplicemente l'attenzione sul tempo necessario per il caricamento di un programma e si usurano rapidamente. Anche se le schermate iniziali sono accettabili se vengono visualizzate solo quando l'interazione dell'utente non è possibile, ogni volta che è possibile un'alternativa migliore consiste nel progettare il programma in modo che gli utenti possano interagire con esso immediatamente, anche mentre è ancora in fase di caricamento.
-   **Specificare un comando Ignora introduzione se una schermata iniziale animata richiede più di tre secondi.** Se si fa clic in un punto qualsiasi della schermata iniziale, la si chiude. In alternativa, usare una versione breve dell'animazione dopo un periodo iniziale.

### <a name="performance"></a>Prestazioni

-   **Non fare in modo che gli utenti attendano le animazioni e le transizioni del programma.** Usare brevi animazioni e transizioni (inferiori a 200 millisecondi) quando possibile. Usare animazioni più veloci (100 millisecondi) per operazioni più frequenti. Progettare animazioni più lunghe (più di un secondo in genere il feedback sullo stato di avanzamento, l'illustrazione e i modelli di esperienza speciale) in modo che gli utenti possano continuare a lavorare mentre sono in esecuzione.
-   **Progettare animazioni a esecuzione lunga per rendere chiaro agli utenti che possono interagire durante l'esecuzione dell'animazione.** Gli utenti non tenterà di continuare a lavorare se gli indizi visivi indicano che non possono continuare a lavorare.

    ![Screenshot di un indicatore di stato in una barra di stato ](images/vis-animations-image51.png)

    In questo esempio di Windows Internet Explorer, l'indicatore di stato basso nella barra di stato suggerisce che gli utenti non devono attendere il completamento prima di poter interagire.

-   **Usare animazioni leggere per attività a elevato utilizzo di CPU.** In questo modo, l'attività offre tutta la potenza di elaborazione. Inoltre, gli utenti non percepiranno che l'animazione leggera è il motivo per cui l'attività richiede un utilizzo elevato della CPU.
-   **Non visualizzare un indicatore di attività durante un'animazione o una transizione.** Questa operazione elimina l'effetto. Progettare animazioni e transizioni in modo che possano iniziare immediatamente.
-   **Progettare animazioni in modo che si degradino normalmente ogni volta che le risorse di sistema non sono sufficienti.** Le animazioni possono peggiorare con variazioni che richiedono meno risorse (ad esempio lunghezze più brevi o frequenze dei fotogrammi inferiori) o addirittura non in esecuzione. Indipendentemente dalle risorse disponibili, assicurarsi che le animazioni siano di alta qualità e siano simili alle animazioni anziché ai bug software.

    **Non corretto:**

    ![Screenshot della cornice del programma in dissolvenza sul desktop ](images/vis-animations-image52.png)

    In questo esempio viene usata la transizione di ripristino della finestra anche se non sono disponibili risorse di sistema sufficienti per riprodurla in modo adeguato. Di conseguenza, il frame bloccato sembra essere un bug. Se le risorse non sono disponibili, è meglio semplicemente visualizzare la finestra senza una transizione.

### <a name="animation-characteristics"></a>Caratteristiche dell'animazione

Le animazioni e le transizioni ben progettate in genere hanno queste caratteristiche:

-   **Breve durata.** La maggior parte delle animazioni deve essere compresa tra 100 e 300 millisecondi, preferibilmente 1/6 secondo (167 millisecondi) o 1/4 secondo (250 millisecondi). Le esperienze speciali e il feedback sullo stato di avanzamento possono essere più lunghi. Usare tempi di animazione più veloci per operazioni più frequenti. In genere, il completamento delle animazioni più lunghe richiede più tempo, richiede più tempo per comprenderlo e può essere lento.
-   **Reattività.** Le animazioni devono iniziare entro 50 millisecondi dall'evento di avvio o dall'azione dell'utente. Gli orari di inizio più lunghi non rispondono.
-   **Accelerazione/decelerazione.** Per sembrare naturale, la maggior parte degli effetti di animazione deve accelerare all'avvio e decelerare all'arresto. Per avere un aspetto reattivo, progettare animazioni in modo che inizino rapidamente. Per apparire controllate, progettare le animazioni in modo che alla fine si presentino degli attesi soft. Anche se si applica agli effetti di movimento, si applica anche a qualsiasi effetto che suggerisce il movimento, ad esempio zoom e persino dissolvenze.

    ![figura di un grafico che mostra una velocità ridotta nel tempo ](images/vis-animations-image53.png)

    La maggior parte delle animazioni deve avere inizi rapidi e terminazioni soft per avere un aspetto reattivo ma controllato.

-   **Movimento.** Le animazioni che usano il movimento in particolare devono accelerare e decelerare, quindi non usare il movimento lineare a meno che la durata dell'animazione non sia molto breve. I movimenti devono prendere il percorso shorts dall'inizio alla fine, senza overshooting. Il percorso di movimento completo non è sempre obbligatorio. Quando appropriato, evidenziare la fine del movimento mentre rallenta e lasciare che l'occhio riempia il resto. In questo modo il movimento è molto più reattivo e ordinato. Quando si anima il movimento di più oggetti contemporaneamente, assegnare loro percorsi leggermente diversi con intervalli leggermente diversi per essere più naturali.
-   **Frequenza dei fotogrammi.** La maggior parte delle animazioni deve usare una frequenza dei fotogrammi di 20 fotogrammi al secondo. Se l'animazione è per un'esperienza speciale o è correlata allo scopo principale del programma, prendere in considerazione l'uso di una frequenza superiore di 24 30 fotogrammi al secondo per migliorare la smussità e il contrario.
-   **Scala.** Progettare animazioni in modo che funzionino correttamente nell'intera gamma di utilizzo previsto. Ad esempio, le transizioni di pagina devono essere progettate per funzionare per tutte le dimensioni di pagina.
-   **Personalità.** Progettare animazioni in modo che si senta naturali, sottodubite ed efficienti anziché artificiali, whimsical o lente.

### <a name="animated-text"></a>Testo animato

-   Anche se è possibile visualizzare il testo usando una transizione, **non animare continuamente il testo.** Il testo animato è spesso distratto e più difficile da leggere rispetto al testo statico. **Eccezioni:**
    -   È possibile animare il testo in situazioni in cui viene tradizionalmente animato e fornire un'alternativa accessibile.
    -   È possibile animare il testo se lo scopo del testo è principalmente decorativo.

![Screenshot dell'interfaccia zune progettata in modo creative ](images/vis-animations-image13.png)

In questo esempio Zune anima il testo, ma lo scopo è principalmente decorativo. Non si verifica alcun problema se gli utenti non leggono attentamente il testo.

### <a name="reducing-power-consumption"></a>Riduzione del consumo di energia

-   **Progettare le animazioni per ridurre il consumo di energia.** Se progettate correttamente, le animazioni non devono aumentare significativamente il consumo di energia. Per ridurre il consumo di energia:
    -   **Interrompere l'animazione quando la visualizzazione è disattivata.** Lo schermo potrebbe essere spento per risparmiare energia.
    -   **Non usare animazioni a esecuzione lunga non avviate dall'utente.** Le animazioni che usano timer periodici ad alta risoluzione riducono l'efficienza del risparmio energia del processore. Assicurarsi inoltre di disabilitare eventuali timer periodici ad alta risoluzione al termine delle animazioni.
    -   **Sospendi tutte le animazioni quando il sistema diventa inattivo.** Il periodo di inattività dell'utente che diventa inattivo è determinato Opzioni risparmio energia in Pannello di controllo.

### <a name="accessibility"></a>Accessibilità

-   **Non usare l'animazione come unico modo per trasmettere informazioni essenziali.** Le animazioni devono comunicare informazioni utili ma non critiche, perché non sono accessibili agli utenti con problemi visivi.
-   **Assicurarsi che le informazioni equivalenti siano disponibili in altri mezzi,** ad esempio:

    -   **Tramite ispezione.** Gli utenti possono determinare informazioni equivalenti esaminando lo schermo o gli oggetti coinvolti nell'animazione.
    -   **Con una semplice interazione.** Gli utenti possono determinare informazioni equivalenti passando il puntatore del mouse, facendo clic o facendo doppio clic.

    ![Screenshot di bing home page con aree sensibili ](images/vis-animations-image54.png)

    L'home page Bing ha un'animazione iniziale che rivela diversi punti critici. Gli utenti possono anche visualizzare gli hot spot spostando il cursore vicino a essi.

    Si noti che "informazioni equivalenti" non significano informazioni identiche. Le informazioni potrebbero essere in un formato diverso o richiedere una deduzione semplice.

-   **Se appropriato, impostare lo stato attivo per l'input sull'oggetto modificato durante una transizione.** Questa operazione consente alle tecnologie di assistive di rilevare la posizione in cui è stata apportata la modifica. Tuttavia, non modificare lo stato attivo dell'input quando l'utente usa la tastiera.
-   **Non usare animazioni o transizioni che flash o ridimensionano rapidamente gli oggetti.** Il flashing e le rapide modifiche dello schermo possono causare problemi per le persone con problemi di attacco e altri disordini di carattere cario.
-   **Consentire agli utenti di disattivare le animazioni e le transizioni del programma.** Per supportare questa funzionalità, rispettare l'opzione Disattiva tutte le animazioni non necessarie nella Centro accessibilità in Windows.

    **Sviluppatori:** È possibile determinare se le animazioni sono abilitate usando l'API SystemParametersInfo.

-   **Progettare attività presupponendo che gli utenti spegnino le animazioni del programma.** Assicurarsi che questa operazione non interrompa in modo significativo il flusso di attività.

Per altre linee guida sull'accessibilità, vedere [Accessibilità](inter-accessibility.md).

## <a name="documentation"></a>Documentazione

-   Evitare di fare riferimento alle animazioni quando possibile. Fare invece riferimento all'oggetto animato e, se necessario, al tipo di animazione.
-   Non fare riferimento alle transizioni, ad eccezione della documentazione tecnica. Fare invece riferimento all'oggetto nello stato finale o iniziale.
-   Se l'utente avvia in modo esplicito un'animazione, usare il verbo play; in caso contrario, usare il verbo use per la documentazione tecnica.

Esempi:

-   Si saprà che un elemento richiede attenzione quando la relativa icona inizia a rimbalzare.
-   Prima di tutto, selezionare le foto che si desidera stampare (si noti che le foto vengono ingrandite al momento della selezione).
-   Usare una transizione con dissolvenza incrociata per modificare facilmente lo stato di un oggetto.

