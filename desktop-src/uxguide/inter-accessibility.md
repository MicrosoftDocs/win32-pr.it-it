---
title: Accessibilità (nozioni di base sulla progettazione)
description: La progettazione di software per l'accessibilità significa garantire che i programmi e le funzionalità siano facilmente disponibili per la più ampia gamma di utenti, inclusi quelli che hanno disabilità e problemi.
ms.assetid: df6947ec-6a1d-4645-ae3e-863839c32588
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 559d4c18e59c63a428aca1086e57f2ba4e62ae6f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104571750"
---
# <a name="accessibility-design-basics"></a>Accessibilità (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

La progettazione di software per l'accessibilità significa garantire che i programmi e le funzionalità siano facilmente disponibili per la più ampia gamma di utenti, inclusi quelli che hanno disabilità e problemi.

Il numero di utenti che possono aiutare le funzionalità di accessibilità può sorprendere. nel Stati Uniti, ad esempio, i sondaggi hanno dimostrato che più della metà di tutti gli utenti del computer riscontrano difficoltà o problemi correlati all'accessibilità e che probabilmente trarranno vantaggio dall'uso della tecnologia accessibile. Inoltre, l'avvicinamento della progettazione del software con la flessibilità e l'inclusione che rappresentano le caratteristiche di accessibilità spesso comporta una migliore usabilità e soddisfazione dei clienti.

![screenshot della finestra di dialogo ' facilità di accesso al centro ' ](images/inter-accessibility-image1.png)

Il Centro accesso facilitato, disponibile dal pannello di controllo, fornisce una posizione centralizzata in cui gli utenti possono scegliere e personalizzare le funzionalità di accessibilità desiderate.

**Nota:** Le linee guida relative alla [tastiera](inter-keyboard.md), al [mouse](inter-mouse.md), al [colore](vis-color.md)e al [suono](vis-sound.md) sono presentate in articoli distinti.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Molti fattori fisici, percettivi e cognitivi entrano in gioco quando gli utenti interagiscono con hardware e software del computer. Prima di prendere in considerazione i modi per rendere le funzionalità del programma più accessibili, è utile sapere quali sono i tipi di disabilità e le difficoltà esistenti e alcune delle tecnologie assistive che questi utenti possono usare durante l'interazione con i computer.

### <a name="types-of-impairments"></a>Tipi di problemi

Nella tabella seguente vengono descritte le disabilità utente comuni e i problemi e vengono elencate alcune delle soluzioni più importanti utilizzate per rendere più accessibili i computer.



|                               |                                                                                                                                                                                                         |                                                                                                                                                                                       |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Danno**<br/>     | **Descrizione**<br/>                                                                                                                                                                              | **Soluzioni**<br/>                                                                                                                                                              |
| Visual<br/>             | Intervalli da lieve (che influiscono sul 17% degli utenti) a gravi (che influiscono sul 9% degli utenti).<br/>                                                                                                   | Ingrandimento, colori e contrasto personalizzabili; Utilità Braille; utilità per la lettura dello schermo.<br/>                                                                                       |
| Udito<br/>            | Intervalli da lieve (che influiscono sul 18% degli utenti) a gravi (che influiscono sul 2% degli utenti).<br/>                                                                                                   | Ridondanza delle informazioni: suono utilizzato solo come supplemento al testo o alla comunicazione visiva.<br/>                                                                                     |
| Difficoltà movimento<br/>          | Intervalli da lieve (che influiscono sul 19% degli utenti) a gravi (che influiscono sul 5% degli utenti). Questo problema spesso implica difficoltà nell'esecuzione di determinate competenze motorie con la tastiera o il mouse.<br/> | Ridondanza del metodo di input: funzionalità del programma accessibili dagli equivalenti del mouse o della tastiera.<br/>                                                                                       |
| Analisi cognitiva<br/>          | Include problemi di memoria e differenze percettive. Influiscono sul 16% degli utenti.<br/>                                                                                                         | Interfaccia utente a personalizzazione elevata; uso della [divulgazione progressiva](ctrl-progressive-disclosure-controls.md) per nascondere la complessità. uso di icone e altri supporti visivi.<br/> |
| Requisizione<br/>            | Include sensibilità visiva per lo spostamento e il lampeggio.<br/>                                                                                                                                        | Approccio conservativo per modulare le interfacce, ad esempio l'uso delle animazioni; evitare lo sfarfallio dello schermo nell'intervallo compreso tra 2 hertz (Hz) e 55 Hz.<br/>                        |
| Sintesi vocale o lingua<br/> | Include la dislessità e le difficoltà di comunicazione orale.<br/>                                                                                                                                       | Controllo ortografico e grammatica-controllo delle utilità; riconoscimento vocale e tecnologia sintesi vocale.<br/>                                                                                 |



 

Per altre linee guida su come aiutare gli utenti a risolvere questi problemi, vedere [risoluzione di particolari problemi](#addressing-particular-impairments) più avanti in questo articolo.

### <a name="types-of-assistive-technologies-and-accessibility-features"></a>Tipi di tecnologie per l'accesso facilitato e funzionalità di accessibilità

**Utilità per la lettura dello schermo**

Una lettura schermo consente agli utenti con disabilità visive o problemi di spostarsi in un'interfaccia utente tramite la trasformazione di oggetti visivi in audio. Pertanto, il testo dell'interfaccia utente, i controlli, i menu, le barre degli strumenti, la grafica e altri elementi della schermata vengono pronunciati dalla voce computerizzata dell'lettore dello schermo. Per creare un programma ottimizzato per la tecnologia di Assistive Reader per la lettura dello schermo, è necessario pianificare l'identificazione di ogni elemento dell'interfaccia utente.

Ogni elemento dell'interfaccia utente con cui l'utente può interagire deve essere accessibile dalla tastiera, nonché essere esposto tramite un Application Programming Interface di accessibilità (API). È consigliabile usare automazione interfaccia utente, il nuovo Framework di accessibilità per tutte le versioni di Microsoft Windows che supportano Windows Presentation Foundation (WPF). Automazione interfaccia utente consente l'accesso a livello di codice alla maggior parte degli elementi sul desktop, consentendo a prodotti di Assistive Technology, quali utilità per la lettura dello schermo, di fornire informazioni sull'interfaccia utente agli utenti e di manipolare l'interfaccia utente per mezzo di input standard, ad esempio parlando piuttosto che o oltre a manipolare il mouse o la tastiera. Per altre informazioni, vedere [Panoramica di automazione interfaccia utente](/dotnet/framework/ui-automation/ui-automation-overview).

Tenere presente che anche se le utilità per la lettura dello schermo sono una tecnologia per l'accessibilità molto importante, esistono anche altri. Per ulteriori informazioni sull'ampia gamma di tecnologie disponibili, vedere [tipi di prodotti Assistive Technology](https://www.microsoft.com/enable/at/types.aspx).

**Riconoscimento vocale**

Il riconoscimento vocale è una funzionalità di accessibilità di Windows che consente agli utenti di interagire con i propri computer tramite voce, riducendo la necessità di interazione del motore con il mouse o la tastiera. Gli utenti possono definire documenti e messaggi di posta elettronica, usare comandi vocali per avviare e passare da un programma all'altra, controllare il sistema operativo e persino compilare moduli sul Web.

**Lente di ingrandimento**

Il fattore di ingrandimento consente agli utenti con ipovisione di ampliare gli elementi sullo schermo da 2 a 16 volte l'originale. Gli utenti possono impostare questa funzionalità in modo da tenere traccia del mouse (per visualizzare una versione ingrandita di ciò che il mouse punta), la tastiera (per visualizzare l'area in cui si sposta il puntatore durante la tabulazione) o la modifica del testo (per vedere cosa stanno digitando).

**Impostazioni visive e combinazioni colori**

Oltre a rendere più ampio lo schermo, gli utenti con problemi visivi possono trarre vantaggio dalle impostazioni di sistema, ad esempio la [modalità a contrasto elevato](glossary.md) o la possibilità di personalizzare le combinazioni di colori di sfondo e di primo piano.

**Assistente vocale**

Assistente vocale è un lettore di schermi con scalabilità orizzontale in Windows che consente agli utenti di ascoltare il testo sullo schermo e gli elementi dell'interfaccia utente letti ad alta voce, anche inclusi alcuni eventi, inclusi i messaggi di errore, che si verificano spontaneamente. L'utente può udire i menu dell'Assistente vocale senza uscire dalla finestra attiva.

![screenshot della finestra di dialogo ' Microsoft Assistente vocale ' ](images/inter-accessibility-image2.png)

Gli utenti possono personalizzare l'ambito di utilizzo dell'Assistente vocale Microsoft.

**Tastiera su schermo**

Per gli utenti che hanno difficoltà con le tastiere fisiche ed è necessario usare un dispositivo di input alternativo, ad esempio un commuti, le tastiere sullo schermo sono una necessità. Gli utenti possono selezionare le chiavi usando il mouse o un altro dispositivo di puntamento, un piccolo gruppo di chiavi o solo una chiave, a seconda di come si configura la tastiera sullo schermo.

**Controllo puntatore**

Con le chiavi del mouse abilitate, gli utenti che preferiscono la tastiera possono usare i tasti di direzione sul tastierino numerico per spostare il puntatore del mouse.

Per un elenco completo delle funzionalità di accessibilità, vedere [accessibilità in Windows Vista](https://www.microsoft.com/enable/products/windowsvista/default.aspx) sul sito Web Microsoft.

### <a name="keyboard-based-navigation"></a>Navigazione basata su tastiera

Il tasto TAB, i tasti di direzione, la barra spaziatrice e il tasto invio sono importanti per la navigazione basata sulla tastiera. Premendo TAB, i cicli di [input vengono attivati](glossary.md) tramite i diversi gruppi di controllo e la pressione dei tasti di direzione si sposta in un controllo o tra i controlli all'interno di un gruppo. Premere barra spaziatrice equivale a fare clic sul controllo con lo stato attivo per l'input, mentre premere INVIO equivale a fare clic sul pulsante di comando predefinito o sul collegamento al comando, indipendentemente dallo stato attivo per l'input.

![screenshot della finestra di dialogo ' Svuota cestino ' ](images/inter-accessibility-image3.png)

In questo esempio, gli utenti possono premere TAB fino a quando l'opzione desiderata non ha lo stato attivo per l'input, quindi premere INVIO per aprire l'oggetto.

### <a name="access-keys"></a>Chiavi di accesso

Le chiavi di accesso consentono agli utenti di scegliere le opzioni e avviare i comandi direttamente senza dover prima passare al controllo. Le chiavi di accesso sono indicate dalla sottostrutturazione di uno dei caratteri nell'etichetta di ogni controllo. Gli utenti attivano quindi l'opzione o il comando premendo il tasto ALT insieme al carattere sottolineato. Chiavi di accesso senza distinzione tra maiuscole e minuscole.

![screenshot del menu file e delle chiavi di accesso ](images/inter-accessibility-image4.png)

In questo esempio, premendo ALT + O viene attivato il comando Apri.

La scelta delle chiavi di accesso logiche per i controlli in genere non pone alcuna difficoltà; maggiore è il numero di controlli in una finestra, tuttavia, maggiore sarà la possibilità di esaurire le scelte delle chiavi di accesso. In questo caso, assegnare le chiavi di accesso ai gruppi di controllo anziché a ogni singolo utente.

![screenshot dei gruppi di controllo e delle chiavi di accesso ](images/inter-accessibility-image5.png)

In questo esempio, le chiavi di accesso vengono assegnate ai gruppi di controllo, anziché ai singoli controlli.

Le chiavi di accesso vengono spesso confuse con i tasti di scelta rapida, ma i tasti di scelta rapida vengono assegnati diversamente dalle chiavi di accesso e hanno obiettivi diversi. Ad esempio, i tasti di scelta rapida utilizzano le sequenze di tasti CTRL e Function e sono destinati principalmente a utenti avanzati anziché per l'accessibilità.

Per ulteriori informazioni, vedere [tastiera](inter-keyboard.md).

### <a name="designing-for-accessibility-three-fundamental-practices"></a>Progettazione per l'accessibilità: tre procedure fondamentali

I programmi accessibili consentono a tutti gli utenti in qualche modo, perché gli obiettivi di accessibilità e usabilità si sovrappongono. Ad esempio, le funzionalità progettate per rendere più efficienti gli utenti avanzati possono anche trarre vantaggio dagli utenti che preferiscono utilizzare la tastiera a causa di problemi di destrezza.

Tre procedure fondamentali sono utili per la progettazione accessibile: consentire un certo livello di flessibilità nell'interfaccia utente, rispettare le esigenze degli utenti e le preferenze svolgono un ruolo fondamentale nelle decisioni di progettazione e forniscono l'accesso a livello di codice all'interfaccia utente.

**Fornire interfaccia utente flessibile**

La progettazione accessibile è, almeno in parte, per fornire scelte agli utenti. Una matrice di scelte frustrante e vertiginosa, ma un numero limitato di scelte che prevedono le esigenze degli utenti in modo intelligente. "Non piace navigare con il mouse? Qui è possibile eseguire le stesse operazioni usando solo la tastiera. Non come le tastiere fisiche? Ecco un esempio virtuale che è possibile usare a schermo ".

Ad esempio, fornire flessibilità per:

-   Fornire equivalenti selezionabili dall'utente per gli elementi non di testo (ad esempio, il testo alternativo per la grafica e le didascalie per l'audio).

    ![cattura di schermata del pulsante di accesso](images/inter-accessibility-image6.png)

    ![screenshot del testo alternativo per il pulsante di accesso](images/inter-accessibility-image7.png)

    Gli utenti che hanno scelto di non eseguire il rendering della grafica dovrebbero invece visualizzare il testo alternativo, descrivendo il funzionamento del controllo e come interagire con esso.

-   Fornire alternative al colore, ad esempio la differenziazione delle icone o l'uso di suoni.

    ![screenshot delle icone con sfumature di grigio (scala di grigi) ](images/inter-accessibility-image8.png)

    In questo esempio, le icone standard sono facilmente distinguibili in base alle rispettive progettazioni.

-   Assicurando l'accesso tramite tastiera, ad esempio una tabulazione per ogni controllo interattivo, in modo che gli utenti possano eseguire le stesse operazioni nel programma con il mouse o la tastiera.
-   Verificare che il programma offra opzioni di contrasto dei colori valide per gli utenti. Windows offre un'opzione a contrasto elevato, ma è effettivamente progettata per essere una soluzione per la forte compromissione degli oggetti visivi. Altre opzioni di contrasto migliorano gli utenti con una lieve difficoltà, ad esempio ipovisione e daltonica.
-   Verificare che gli utenti dispongano di un modo per regolare le dimensioni del testo nell'interfaccia utente del programma (ad esempio, tramite un controllo dispositivo di scorrimento o una casella di riepilogo a discesa per le dimensioni del carattere). Se possibile, supporta la modalità dpi (punti per pollice).
-   Assicurandosi che il programma sia multimodale, ovvero se la modalità principale del programma è inaccessibile per alcuni, questi utenti hanno una soluzione per aggirare il problema. Ad esempio, quando viene visualizzata l'animazione, le informazioni devono essere riprodotte in almeno una modalità di presentazione non animata con l'opzione dell'utente.

Le interfacce multimodali e la navigazione flessibile offrono essenzialmente all'utente l'architettura della ridondanza delle informazioni. La ridondanza a volte presenta connotazioni negative; nel testo dell'interfaccia utente, ad esempio, si consiglia di rimuovere la ridondanza per semplificare l'esperienza di lettura. Tuttavia, nel contesto dell'accessibilità, la ridondanza denota meccanismi ed esperienze positivi e non affidabili.

**Rispetto degli utenti**

Rispetto come generale, il principio guida è fondamentale per la progettazione di programmi accessibili. Anche per quanto riguarda un esercizio intellettuale, si supponga di voler incontrare il programma come un utente disabilitato. Si consiglia di testare le schermate dell'interfaccia utente in modalità a contrasto elevato e con diverse risoluzioni, per garantire che l'esperienza sia ottimale per gli utenti con problemi visivi. Testare l'accessibilità della tastiera selezionando la casella di controllo **sottolineare i tasti di scelta e le chiavi di accesso** nell'elemento del pannello di controllo accesso facilitato (in modo che le chiavi di accesso siano sempre visibili). È anche possibile superare i rigorosi test impiegando gli sviluppatori e i progettisti che hanno un'idoneità naturale per Empathizing con altri utenti per iniziare.

È inoltre necessario dimostrare quanto segue:

-   Utilizzando le impostazioni a livello di sistema (ad esempio, il colore di sistema) anziché le impostazioni cablatura per il programma specifico. Non solo i parametri selezionati dagli utenti per interagire con i programmi, ma anche le funzionalità di accessibilità incorporate nel sistema operativo che l'utente desidera in effetti indipendentemente dal programma in uso. Per ulteriori informazioni, vedere [informazioni sulle funzionalità di accessibilità di Windows](/previous-versions//ms695605(v=vs.85)).
-   Preferisce controlli comuni ai controlli personalizzati, perché i controlli comuni hanno già implementato le API di accessibilità di Windows.
-   Documentare tutte le opzioni e le funzionalità di accessibilità, ad esempio tutti i tasti di scelta rapida. Gli utenti con problemi sono molto motivati a individuare le funzionalità di accessibilità e spesso prevedono la raccolta di informazioni complete nella Guida di.
-   Creazione di documentazione accessibile in formati accessibili. La documentazione stessa deve quindi rispettare le stesse regole di accessibilità dell'interfaccia utente primaria, inclusa la possibilità di ingrandire le dimensioni del carattere, l'uso del testo alternativo per la grafica e l'architettura delle informazioni ridondanti, ad esempio l'uso della codifica a colori solo come supplemento al testo.

Nei prodotti software, il rispetto degli utenti può manifestarsi nell'usabilità e nella ricerca di mercato, in servizi di supporto e documentazione efficaci e naturalmente nelle decisioni di progettazione. Ad esempio, pensando di nuovo in termini di progettazione per gli utenti avanzati: si sta inserendo la nuova funzionalità all'avanguardia in perché si vuole o perché si è certi che gli utenti avanzati lo hanno chiesto? Il secondo caso indica che il processo decisionale di progettazione è ben informato dal valore di respect.

**Fornire l'accesso a livello di codice**

Fornire l'accesso a livello di codice all'interfaccia utente è essenziale, in modo che le tecnologie per l'accesso facilitato (quali utilità per la lettura dello schermo, dispositivi di input alternativi e programmi di riconoscimento vocale) interpretino correttamente lo schermo per gli Creando una "mappa" di ogni schermata dell'interfaccia utente nel programma, è possibile renderla disponibile agli utenti delle tecnologie per l'accesso facilitato.

Eseguire questa operazione in base a quanto segue:

-   Abilitazione dell'accesso programmatico a tutti gli elementi e il testo dell'interfaccia utente, ad esempio usando l'interfaccia COM di Active Accessibility, [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)).
-   Immissione di nomi (o titoli) e descrizioni su oggetti dell'interfaccia utente, frame e pagine, ad esempio utilizzando la proprietà nome [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
-   Assicurandosi che gli eventi programmatici vengano attivati da tutte le attività dell'interfaccia utente, ad esempio eventi di attivazione per tutte le attività dell'interfaccia utente che coinvolgono lo spostamento dello stato

**Se si eseguono solo quattro operazioni...**

1.  Assicurarsi che ogni utente possa sfruttare tutte le potenzialità del programma.
2.  È possibile considerare l'accessibilità come un'opportunità per la risoluzione di problemi creativi e un altro mezzo per aumentare la soddisfazione complessiva degli utenti.
3.  Rispettare le impostazioni di sistema.
4.  Usare i controlli comuni laddove possibile.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Non compromettere o disabilitare le funzionalità attivate del sistema operativo o di altri prodotti identificati come funzionalità di accessibilità.** È possibile identificare queste funzionalità facendo riferimento alla documentazione del sistema operativo o del prodotto in questione.
-   **Non forzare gli utenti a interagire con il programma come finestra superiore sullo schermo.** Se una funzione o una finestra è richiesta in modo continuo per consentire agli utenti di eseguire un'attività, tale finestra rimarrà sempre visibile, se l'utente sceglie, indipendentemente dalla relativa posizione rispetto ad altre finestre. Ad esempio, se l'utente dispone di una tastiera sullo schermo mobile che si trova in tutte le altre finestre, in modo che sia visibile in qualsiasi momento, il programma non dovrebbe mai nasconderlo in base alla posizione obbligatoria nella parte superiore del [z order](glossary.md).
-   **Usare i colori di sistema, i tipi di carattere e i controlli comuni laddove possibile.** In questo modo si riduce significativamente il numero di problemi di accessibilità riscontrati dagli utenti.

### <a name="addressing-particular-impairments"></a>Risoluzione di particolari problemi

**Visual**

-   **Non fare mai affidamento su un solo colore per fornire significato.** Usare il colore solo come mezzo per rinforzare il significato fornito da testo, progettazione, posizione o suono.

    ![screenshot dell'icona e della descrizione comando di Red Communicator ](images/inter-accessibility-image9.png)

    Il metodo principale di comunicazione in questo esempio è il testo conciso della descrizione comando. L'uso dei colori facilita la comunicazione del significato, ma è secondario.

-   **Usare infotip di testo alternativo (alt) per descrivere la grafica.**
-   **Non usare testo in grafica.** È possibile che gli utenti con problemi visivi siano disattivati (ad esempio, in una Web browser) o semplicemente non possano visualizzare o cercare il testo inserito nella grafica.
-   **Verificare che le finestre di dialogo e le finestre abbiano nomi significativi,** in modo che un utente che sta sentendo invece di visualizzare lo schermo (ad esempio, usando un'analisi dello schermo) ottenga le informazioni contestuali appropriate.
-   **Rispettare le impostazioni dell'utente per la visualizzazione visiva** ottenendo sempre caratteri tipografici, dimensioni e colori, le dimensioni degli elementi di visualizzazione di Windows e le impostazioni di configurazione del sistema dal tema e dalle API GetSystemMetrics.
-   Il **testo del fumetto è conciso** , in modo da semplificare la lettura e ridurre al minimo le rotture per le utilità per la lettura dello schermo.

    ![screenshot del fumetto che indica i limiti del codice PIN ](images/inter-accessibility-image10.png)

    Sebbene gli aerostati possano usare un testo del corpo aggiuntivo se necessario, questo esempio mostra che talvolta il testo del titolo da solo raggiunge lo stesso obiettivo in modo più economico e accessibile.

**Udito**

-   **Non fare mai affidamento su un solo suono per fornire significato.** Usare il suono solo come mezzo per rinforzare il significato fornito da testo, progettazione, posizione o colore.
-   **Consentire agli utenti di controllare il volume dell'output audio.** Per questo scopo, usare il mixer di volume di Windows. Per ulteriori informazioni, vedere [suono](vis-sound.md).
-   Specificare come **destinazione il suono del programma in un intervallo compreso tra 500 Hz e 3000 Hz** oppure facilmente modificabile dall'utente in tale intervallo. I suoni in questo intervallo sono probabilmente rilevabili dagli utenti con problemi di udito.

**Difficoltà movimento**

-   **Rendere i valori di timeout dell'interfaccia utente relativi a GetDoubleClickTime () anziché usare gli orari assoluti.** Questa operazione consente di adattare i timeout alla velocità dell'utente.
-   **Assegnare le chiavi di accesso a tutte le voci di menu** in modo che gli utenti che preferiscono utilizzare la tastiera abbiano la stessa capacità di esplorare il programma come utenti che lavorano con il mouse.
-   **Non fare doppio clic e trascinare l'unico modo per eseguire un'azione.** Questi possono essere movimenti difficili per alcuni utenti.
-   **Non rimuovere le barre dei menu dal programma.** Le barre dei menu sono più semplici delle barre degli strumenti per l'accesso degli utenti della tastiera. Se non si vuole che la barra dei menu sia visibile per impostazione predefinita, nasconderla.
-   **Rendere la guida accessibile dalla tastiera fornendo tabulazioni per i pulsanti e i collegamenti della guida.**
-   **Per migliorare la conoscenza delle assegnazioni delle chiavi di accesso nel programma, è possibile visualizzarle in qualsiasi momento.** Nel pannello di controllo passare al centro di accesso facilitato e fare clic su **Rendi più semplice l'uso della tastiera**; Selezionare quindi la casella di controllo **sottolineatura tasti di scelta rapida e chiavi di accesso** .

**Analisi cognitiva**

-   **Usare la divulgazione progressiva** per nascondere la complessità.

    ![screenshot dei pulsanti di divisione con triangoli inferiori ](images/inter-accessibility-image11.png)

    In questi esempi, le opzioni disponibili nel pulsante di comando sono nascoste per impostazione predefinita e gli utenti possono scegliere di visualizzare le opzioni sfruttando i controlli di divulgazione progressiva.

-   **Usare icone, barre degli strumenti e altri supporti visivi** per ridurre il carico cognitivo della lettura del testo.
-   Quando possibile, **fornire funzionalità di completamento automatico nelle caselle di testo e negli elenchi a discesa modificabili, in** modo che gli utenti non debbano digitare l'intero nome di comandi, nomi file o scelte simili da un set limitato di opzioni. In questo modo si riduce il carico cognitivo per tutti gli utenti e si riduce la quantità di tipi di utenti per i quali l'ortografia o la digitazione è difficile, lenta o dolorosa.
-   **Vengono illustrati i concetti difficili della guida, incluse le esercitazioni e le animazioni.** Si noti che le animazioni possono essere difficili da usare per gli utenti con compromissione del grippaggio e pertanto devono essere usate solo quando necessario.

**Requisizione**

-   **Non usare il testo lampeggiante o lampeggiante, gli oggetti o altri elementi con una frequenza flash o Blink nell'intervallo compreso tra 2-55 Hz.**
-   **Limitare l'uso di animazioni.** Alcuni utenti sono particolarmente sensibili allo spostamento dello schermo, soprattutto nella periferia del rispettivo campo visivo. Se si usa l'animazione per attirare l'attenzione su un elemento, assicurarsi che l'attenzione venga rifornita e che l'utente sia in grado di interrompere l'operazione.

**Sintesi vocale o lingua**

-   **Organizzare e scrivere testo chiaro, conciso e facilmente comprensibile.** I test di usabilità mostrano che lo svolgimento delle informazioni chiave alla fine di una frase migliora la comprensione. Per altre linee guida, vedere [stile e tono](text-style-tone.md).

**Non corretto:**

Si tratta di tre cifre successive?

Fare clic su OK per iniziare.

**Corretto:**

La terza cifra è la seguente?

Per iniziare, fare clic su OK.

### <a name="access-keys"></a>Chiavi di accesso

-   **Preferisce caratteri con larghezze ampie,** ad esempio w, m e lettere maiuscole.
-   **Preferisce una consonante distinta o una vocale,** ad esempio "x" in "Exit".
-   **Evitare l'uso di caratteri che rendono difficile la visualizzazione della sottolineatura,** ad esempio (dal più problematico al meno problematico):
    -   Caratteri con una sola larghezza di pixel, ad esempio i e l.
    -   Caratteri con discendenti, ad esempio g, j, p, q e y.
    -   Caratteri accanto a una lettera con un discendente.

### <a name="menu-access-keys"></a>Chiavi di accesso ai menu

-   **Assegnare chiavi di accesso a tutte le voci di menu.** Nessuna eccezione.
-   **Per le voci di menu dinamiche, ad esempio i file usati di recente, assegnare chiavi di accesso numericamente.**

    ![screenshot del menu Apri con i file usati di recente ](images/inter-accessibility-image12.png)

    In questo esempio, il programma di disegno in Windows assegna chiavi di accesso numeriche ai file usati di recente.

-   **Assegnare chiavi di accesso univoche all'interno di un livello di menu.** È possibile riutilizzare le chiavi di accesso in diversi livelli di menu.
-   **Semplifica la ricerca delle chiavi di accesso:**
    -   Per le voci di menu utilizzate più di frequente, scegliere caratteri all'inizio della prima o della seconda parola dell'etichetta, preferibilmente il primo carattere.
    -   Per le voci di menu utilizzate meno di frequente, scegliere lettere che rappresentano una consonante distinta o una vocale nell'etichetta.

### <a name="dialog-box-access-keys"></a>Chiavi di accesso della finestra di dialogo

-   **Laddove possibile, assegnare chiavi di accesso univoche a tutti i controlli interattivi o alle relative etichette.** Le [caselle di testo](ctrl-text-boxes.md) di sola lettura sono controlli interattivi (poiché gli utenti possono scorrerli e copiare testo), quindi traggono vantaggio dalle chiavi di accesso. **Non assegnare chiavi di accesso a:**
    -   **Pulsanti OK, Annulla e Chiudi.** Per le chiavi di accesso vengono usati Enter e ESC. Tuttavia, assegnare sempre una chiave di accesso a un controllo che significa OK o Annulla, ma con un'etichetta diversa.

        ![screenshot dei controlli con chiavi di accesso assegnate ](images/inter-accessibility-image13.png)

        In questo esempio il pulsante di commit positivo ha una chiave di accesso assegnata.

-   **Etichette del gruppo.** In genere, i singoli controlli all'interno di un gruppo vengono assegnati alle chiavi di accesso, quindi l'etichetta del gruppo non ne ha bisogno. Tuttavia, assegnare una chiave di accesso all'etichetta del gruppo e non ai singoli controlli in caso di carenza di chiavi di accesso.
-   **Pulsanti della Guida generici,** a cui è possibile accedere con F1.
-   **Etichette di collegamento.** Spesso sono presenti troppi collegamenti per assegnare chiavi di accesso univoche e i caratteri di sottolineatura dei collegamenti nascondono i caratteri di sottolineatura della chiave di accesso. Chiedere agli utenti di accedere ai collegamenti con il tasto TAB.
-   **Nomi delle schede.** Le tabulazioni vengono ciclate con CTRL + TAB e CTRL + MAIUSC + TAB.
-   **Pulsanti Sfoglia con etichetta "...".** Non è possibile assegnare chiavi di accesso in modo univoco.
-   **Controlli senza etichetta,** ad esempio controlli di selezione, pulsanti di comando grafici e controlli di divulgazione progressivi senza etichetta.
-   **Testo statico senza etichetta o etichette per i controlli che non sono interattivi,** ad esempio le barre di stato.
-   **Assegnare prima di tutto i pulsanti di accesso per assicurarsi che abbiano le assegnazioni di chiavi standard.** Se non è disponibile un'assegnazione di chiave standard, usare la prima lettera della prima parola. La chiave di accesso per i pulsanti Sì e no commit, ad esempio, deve essere sempre "Y" e "N", indipendentemente dagli altri controlli della finestra di dialogo.
-   **Per i pulsanti di commit negativi (diversi da Cancel) formulati come "non", assegnare la chiave di accesso a "n" in "No".** Se non viene formulata come "non", usare l'assegnazione della chiave di accesso standard o assegnare la prima lettera della prima parola. In questo modo, tutti i non sono disponibili e non hanno una chiave di accesso coerente.
-   **Per semplificare la ricerca delle chiavi di accesso, assegnare le chiavi di accesso a un carattere che viene visualizzato all'inizio dell'etichetta,** idealmente il primo carattere, anche se è presente una parola chiave che viene visualizzata più avanti nell'etichetta.

Per altre linee guida ed esempi, vedere [tastiera](inter-keyboard.md).

## <a name="text"></a>Testo

-   **Usare i due punti alla fine delle etichette del controllo esterno.** Alcune tecnologie per l'accesso facilitano la ricerca dei due punti per identificare le etichette dei controlli.
-   **Posizionare le etichette in modo coerente rispetto agli elementi per i quali viene applicata un'etichetta.** In questo modo, la tecnologia per l'accessibilità associa correttamente le etichette ai controlli corrispondenti e consente agli utenti di ingrandimenti dello schermo di individuare il punto in cui cercare un'etichetta o un controllo.

    ![screenshot delle etichette posizionate in modo coerente ](images/inter-accessibility-image14.png)

    In questo esempio, le etichette per ogni elenco a discesa vengono posizionate in modo coerente e utilizzano i due punti.

-   **Limitare il testo Alt a un massimo di 150 caratteri.** Descrivere l'azione per attivare il controllo (ad esempio, fare clic su, fare clic con il pulsante destro del mouse e così via) e quindi descrivere la funzione del controllo.

    **Accettabile:**

    Pulsante.

    Colline blu.

    **Migliore:**

    Fare clic per accedere al proprio account.

    Foto di colline distanti che mostrano il modo in cui i colori passano alla distanza.

-   **Non usare il testo per creare linee, caselle o altri simboli grafici.** I caratteri usati in questo modo possono confondere gli utenti delle utilità per la lettura dello schermo. Ad esempio, una casella disegnata con la lettera "X" intorno a un'area di testo viene letta dal software di lettura dello schermo come "X x x x x" sulla prima riga, seguita da "X" e dal contenuto e "X".

## <a name="documentation"></a>Documentazione

-   Documentare tutte le opzioni e le funzionalità di accessibilità, ad esempio tutti i tasti di scelta rapida.
-   Crea la documentazione accessibile in formati accessibili. La documentazione stessa deve quindi rispettare le stesse regole di accessibilità dell'interfaccia utente primaria.
-   Fare riferimento alle chiavi di accesso, non ai tasti di scelta rapida (che hanno un significato e un uso diversi), chiavi mnemonico o acceleratori.
-   In generale, fare riferimento a una persona con un tipo di disabilità, non a un utente disabilitato. Considerare prima di tutto la persona, non l'etichetta.



|                                                               |                                                                                  |
|---------------------------------------------------------------|----------------------------------------------------------------------------------|
| **Usa questi termini**<br/>                                | **Invece di**<br/>                                                        |
| Con destrezza limitata, con disabilità del movimento<br/>     | Storpio, zoppo<br/>                                                        |
| Senza disabilità<br/>                               | Normale, con corpo possibile, integro<br/>                                          |
| Con una sola mano, chi digita con una mano<br/>          | A mano singola <br/>                                                        |
| Utenti con particolari esigenze<br/>                           | Persone disabilitate, disabilitate, persone con handicap, handicappati<br/> |
| Disabilità cognitive, disabilità di sviluppo<br/> |                                                                                  |



 

