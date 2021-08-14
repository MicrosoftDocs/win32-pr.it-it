---
title: Accessibilità (nozioni di base sulla progettazione)
description: Progettare software per l'accessibilità significa garantire che i programmi e le funzionalità siano facilmente disponibili per la più ampia gamma di utenti, inclusi quelli con disabilità e disabilità.
ms.assetid: df6947ec-6a1d-4645-ae3e-863839c32588
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c38eb3993880d820a4e65fa25a1e910e9e842de823779aaf3ef24dab8635e60e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118212498"
---
# <a name="accessibility-design-basics"></a>Accessibilità (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Progettare software per l'accessibilità significa garantire che i programmi e le funzionalità siano facilmente disponibili per la più ampia gamma di utenti, inclusi quelli con disabilità e disabilità.

Il numero di utenti che le funzionalità di accessibilità possono essere utili può sorprendere; Ad esempio, nel Stati Uniti, i sondaggi hanno dimostrato che più della metà di tutti gli utenti di computer ha difficoltà o problemi correlati all'accessibilità e probabilmente trarrà vantaggio dall'uso di tecnologie accessibili. Inoltre, l'approccio alla progettazione software con la flessibilità e l'inclusività che sono i segni distintivi dell'accessibilità spesso comportano un miglioramento generale dell'usabilità e della soddisfazione dei clienti.

![Screenshot della finestra di dialogo "Centro accessibilità" ](images/inter-accessibility-image1.png)

Il Centro accessibilità, disponibile da Pannello di controllo, offre una posizione centrale in cui gli utenti possono scegliere e personalizzare le funzionalità di accessibilità desiderate.

**Nota:** Le linee guida relative [a tastiera,](inter-keyboard.md) [mouse,](inter-mouse.md) [colore](vis-color.md) [e suono](vis-sound.md) sono presentate in articoli separati.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Molti fattori fisici, percettivi e cognitivi interagiscono con l'hardware e il software del computer. Prima di considerare i modi per rendere più accessibili le funzionalità del programma, è utile conoscere i tipi di disabilità e disabilità esistenti e alcune delle tecnologie di assistive con cui questi utenti possono lavorare mentre interagiscono con i computer.

### <a name="types-of-impairments"></a>Tipi di problemi

La tabella seguente descrive le disabilità e le menomazioni degli utenti comuni ed elenca alcune delle soluzioni più importanti usate per rendere i computer più accessibili.



| Impedimento    | Descrizione   | Soluzioni  |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Visual<br/>             | Varia da lieve (che interessa il 17% degli utenti) a grave (che interessa il 9% degli utenti).<br/>                                                                                                   | Ingrandimento personalizzabile, colori e contrasto; Utilità braille; utilità per la lettura dello schermo.<br/>                                                                                       |
| Udito<br/>            | Varia da lieve (che interessa il 18% degli utenti) a grave (che interessa il 2% degli utenti).<br/>                                                                                                   | Ridondanza delle informazioni: suono usato solo come complemento alla comunicazione testuale o visiva.<br/>                                                                                     |
| Destrezza<br/>          | Varia da lieve (che interessa il 19% degli utenti) a grave (che interessa il 5% degli utenti). Questa comprosizione comporta spesso difficoltà nell'esecuzione di determinate competenze motorie con la tastiera o il mouse.<br/> | Ridondanza del metodo di input: funzionalità del programma accessibili da equivalenti del mouse o della tastiera.<br/>                                                                                       |
| Analisi cognitiva<br/>          | Include problemi di memoria e differenze percettivi. Influisce sul 16% degli utenti.<br/>                                                                                                         | Interfaccia utente altamente personalizzabile; uso della [divulgazione progressiva](ctrl-progressive-disclosure-controls.md) per nascondere la complessità; uso di icone e altri strumenti visivi.<br/> |
| Sequestro<br/>            | Include la sensibilità visiva al movimento e al lampeggiamento.<br/>                                                                                                                                        | Approccio conservativo alla modulazione delle interfacce, ad esempio l'uso di animazioni; evitando lo sfarfallio dello schermo nell'intervallo compreso tra 2 Hertz (Hz) e 55 Hz.<br/>                        |
| Voce o lingua<br/> | Include dislessia e difficoltà di comunicazione orale.<br/>                                                                                                                                       | Utilità per il controllo ortografico e grammaticale; riconoscimento vocale e tecnologia di sintesi vocale.<br/>                                                                                 |



 

Per altre linee guida su come aiutare gli utenti con questi problemi, vedere [Risolvere](#addressing-particular-impairments) particolari problemi più avanti in questo articolo.

### <a name="types-of-assistive-technologies-and-accessibility-features"></a>Tipi di tecnologie di assistive e funzionalità di accessibilità

**Utilità per la lettura dello schermo**

Un'utilità per la lettura dello schermo consente agli utenti con disabilità visive di spostarsi all'interno di un'interfaccia utente trasformando gli oggetti visivi in audio. Di conseguenza, il testo dell'interfaccia utente, i controlli, i menu, le barre degli strumenti, la grafica e altri elementi dello schermo vengono pronunciati dalla voce computerizzata dell'utilità per la lettura dello schermo. Per creare un programma ottimizzato per la lettura dello schermo assistive technology, è necessario pianificare il modo in cui l'utilità per la lettura dello schermo identificherà ogni elemento dell'interfaccia utente.

Ogni elemento dell'interfaccia utente con cui l'utente può interagire deve essere accessibile tramite tastiera e deve essere esposto tramite un'API (Accessibility Application Programming Interface). È consigliabile usare Automazione interfaccia utente, il nuovo framework di accessibilità per tutte le versioni di Microsoft Windows che supportano Windows Presentation Foundation (WPF). Automazione interfaccia utente fornisce l'accesso a livello di codice alla maggior parte degli elementi sul desktop, consentendo ai prodotti assistive technology, ad esempio le utilità per la lettura dello schermo, di fornire informazioni sull'interfaccia utente agli utenti e di modificare l'interfaccia utente con mezzi diversi dall'input standard (ad esempio, pronunciando anziché o oltre a manipolare il mouse o la tastiera). Per altre informazioni, vedere la Automazione interfaccia utente [panoramica di](/dotnet/framework/ui-automation/ui-automation-overview).

Tenere presente che anche se le utilità per la lettura dello schermo sono una assistive technology molto importante, ce ne sono anche altre. Per altre informazioni sulla gamma di tecnologie disponibili, vedere [Tipi di prodotti assistive technology](https://www.microsoft.com/enable/at/types.aspx).

**Riconoscimento vocale**

Il riconoscimento vocale è una funzionalità di accessibilità in Windows che consente agli utenti di interagire con i computer tramite voce, riducendo la necessità di interazione del motore con il mouse o la tastiera. Gli utenti possono dettare documenti e posta elettronica, usare i comandi vocali per avviare e passare da un programma all'altro, controllare il sistema operativo e persino compilare moduli sul Web.

**Lente di ingrandimento**

L'ingrandimento consente agli utenti con problemi di vista di ingrandire gli elementi sullo schermo da 2 a 16 volte l'originale. Gli utenti possono impostare questa funzionalità per tenere traccia del mouse (per visualizzare una versione ingrandita di ciò a cui punta il mouse), la tastiera (per visualizzare l'area in cui si sposta il puntatore durante la tabulazione) o la modifica del testo (per vedere cosa stanno digitando).

**Impostazioni visive e combinazioni di colori**

Oltre a rendere più grandi le dimensioni dello schermo, gli utenti con problemi visivi possono trarre vantaggio dalle impostazioni di sistema, ad esempio la modalità a [contrasto](glossary.md) elevato o la possibilità di personalizzare le combinazioni di colori di sfondo e primo piano.

**Assistente vocale**

Assistente vocale è un'utilità per la lettura dello schermo ridotta in Windows che consente agli utenti di ascoltare il testo sullo schermo e gli elementi dell'interfaccia utente letti ad alta voce, inclusi alcuni eventi (inclusi i messaggi di errore) che si verificano in modo spontaneo. L'utente può ascoltare i menu dell'Assistente vocale senza uscire dalla finestra attiva.

![Screenshot della finestra di dialogo "Assistente vocale Microsoft" ](images/inter-accessibility-image2.png)

Gli utenti possono personalizzare la misura in cui viene usato l'Assistente vocale Microsoft.

**Tastiera su schermo**

Per gli utenti che hanno difficoltà con le tastiere fisiche e devono usare un dispositivo di input alternativo, ad esempio un interruttore, le tastiere su schermo sono una necessità. Gli utenti possono selezionare i tasti usando il mouse o un altro dispositivo di puntamento, un piccolo gruppo di tasti o solo un tasto, a seconda della modalità di configurazione della tastiera su schermo.

**Controllo puntatore**

Con i tasti del mouse abilitati, gli utenti che preferiscono la tastiera possono usare i tasti di direzione sul tastierino numerico per spostare il puntatore del mouse.

Per un elenco completo delle funzionalità di accessibilità, vedere [Accessibilità in Windows Vista](https://www.microsoft.com/enable/products/windowsvista/default.aspx) nel sito Web Microsoft.

### <a name="keyboard-based-navigation"></a>Navigazione basata su tastiera

Il tasto TAB, i tasti di direzione, la barra spaziatrice e il tasto INVIO sono importanti per la navigazione basata su tastiera. Premendo TAB lo [stato attivo viene](glossary.md) spostato tra i diversi gruppi di controlli e i tasti di direzione si spostano all'interno di un controllo o tra i controlli all'interno di un gruppo. La pressione della barra spaziatrice è uguale a fare clic sul controllo con lo stato attivo per l'input, mentre premere INVIO è uguale a fare clic sul pulsante di comando o sul collegamento di comando predefinito, indipendentemente dallo stato attivo per l'input.

![Screenshot della finestra di dialogo "Cestino vuoto" ](images/inter-accessibility-image3.png)

In questo esempio gli utenti possono premere TAB finché l'opzione desiderata non ha lo stato attivo per l'input, quindi premere INVIO per aprire l'oggetto.

### <a name="access-keys"></a>Chiavi di accesso

I tasti di scelta consentono agli utenti di scegliere le opzioni e avviare i comandi direttamente senza dover prima passare al controllo. I tasti di scelta sono indicati sottolineando uno dei caratteri nell'etichetta di ogni controllo. Gli utenti attivano quindi l'opzione o il comando premendo ALT insieme al carattere sottolineato. Per le chiavi di accesso non viene fatto distinzione tra maiuscole e minuscole.

![Screenshot del menu file e dei tasti di scelta ](images/inter-accessibility-image4.png)

In questo esempio, premendo ALT+O viene attivato il comando Apri.

La scelta delle chiavi di accesso logiche per i controlli in genere non comporta alcuna difficoltà; Maggiore è il numero di controlli presenti in una finestra, tuttavia, maggiore è la possibilità che si esereranno le scelte della chiave di accesso. In questo caso, assegnare le chiavi di accesso ai gruppi di controllo anziché a ognuno di essi.

![Screenshot dei gruppi di controllo e dei tasti di scelta ](images/inter-accessibility-image5.png)

In questo esempio i tasti di scelta vengono assegnati ai gruppi di controllo, anziché ai singoli controlli.

I tasti di scelta sono spesso confusi con i tasti di scelta rapida, ma i tasti di scelta rapida vengono assegnati in modo diverso rispetto ai tasti di scelta e hanno obiettivi diversi. I tasti di scelta rapida, ad esempio, usano ctrl e sequenze di tasti funzione e sono destinati principalmente agli utenti avanzati anziché all'accessibilità.

Per altre informazioni, vedere [Tastiera](inter-keyboard.md).

### <a name="designing-for-accessibility-three-fundamental-practices"></a>Progettazione per l'accessibilità: tre procedure fondamentali

I programmi accessibili aiutano tutti gli utenti in qualche modo perché gli obiettivi di accessibilità e usabilità si sovrappongono. Ad esempio, le funzionalità progettate per rendere il più efficiente possibile gli utenti avanzati sono vantaggiose anche per gli utenti che preferiscono usare la tastiera a causa di problemi di destrezza.

Tre procedure fondamentali consentono di progettare in modo accessibile: consentire un certo grado di flessibilità nell'interfaccia utente, rispettare le esigenze e le preferenze degli utenti e svolgere un ruolo importante nelle decisioni di progettazione e fornire l'accesso a livello di codice all'interfaccia utente.

**Fornire un'interfaccia utente flessibile**

La progettazione accessibile riguarda, almeno in parte, la scelta degli utenti. Non una gamma frustrante e vertiginosa di scelte, ma un numero limitato di scelte che anticipano in modo intelligente le esigenze degli utenti. "Non ti piace navigare con il mouse? In questo caso, è possibile eseguire le stesse operazioni usando solo la tastiera. Le tastiere fisiche non sono simili? Ecco una virtuale che è possibile usare sullo schermo."

Ad esempio, fornire flessibilità tramite:

-   Fornire equivalenti selezionabili dall'utente per gli elementi non di testo, ad esempio testo alternativo per grafica e didascalie per l'audio.

    ![Screenshot del pulsante di accesso](images/inter-accessibility-image6.png)

    ![Screenshot del testo alternativo per il pulsante di accesso](images/inter-accessibility-image7.png)

    Gli utenti che hanno scelto di non eseguire il rendering della grafica dovrebbero invece visualizzare il testo alternativo, descrivendo le funzionalità del controllo e come interagire con esso.

-   Fornire alternative al colore,ad esempio la differenziazione delle icone o l'uso di suoni.

    ![Screenshot delle icone in sfumature di grigio (scala di grigi) ](images/inter-accessibility-image8.png)

    In questo esempio, le icone standard sono facilmente distinguibili in base alle progettazioni.

-   Garantire l'accesso tramite tastiera (ad esempio, una tabulazione per ogni controllo interattivo) in modo che gli utenti possano eseguire le stesse operazioni nel programma con il mouse o la tastiera.
-   Assicurarsi che il programma offre buone opzioni di contrasto dei colori per gli utenti. Windows offre un'opzione a contrasto elevato, ma è stata progettata per essere una soluzione per gravi problemi visivi. Altre opzioni di contrasto sono più adatta agli utenti con lievi problemi di vista e cecità dei colori.
-   Assicurarsi che gli utenti possono modificare le dimensioni del testo nell'interfaccia utente del programma, ad esempio tramite un controllo dispositivo di scorrimento o una casella a discesa per le dimensioni del carattere. Se possibile, supportare la modalità punti per pollice (dpi) elevata.
-   Assicurarsi che il programma sia multimodale, vale a dire che se la modalità principale del programma è inaccessibile per alcuni, questi utenti hanno un modo per risolvere il problema. Ad esempio, quando viene visualizzata l'animazione, le informazioni devono essere visualizzate in almeno una modalità di presentazione non animata, a scelta dell'utente.

Le interfacce multimodali e la navigazione flessibile offrono essenzialmente all'utente l'architettura della ridondanza delle informazioni. La ridondanza talvolta presenta connotazioni negative. nel testo dell'interfaccia utente, ad esempio, si consiglia di rimuovere la ridondanza per semplificare l'esperienza di lettura. Nel contesto dell'accessibilità, tuttavia, la ridondanza indica meccanismi ed esperienze positivi e non sicuri.

**Rispetto degli utenti**

Il rispetto come principio generale è fondamentale per la progettazione di programmi accessibili. Anche come esercizio intellettuale, immaginare come deve essere incontrare il programma come utente disabilitato. Prendere il tempo necessario per testare le schermate dell'interfaccia utente in modalità a contrasto elevato e a varie risoluzioni, per garantire che l'esperienza sia ottimale per gli utenti con problemi visivi. Testare l'accessibilità  tramite tastiera selezionando la casella di controllo Sottolinea tasti di scelta rapida e tasti di scelta nell'elemento Centro accessibilità Pannello di controllo (in modo che i tasti di scelta siano sempre visibili). È anche possibile andare oltre i test rigorosi assumendo sviluppatori e progettisti che hanno una naturale abilità di empatia con gli altri per iniziare.

È anche necessario dimostrare il rispetto tramite:

-   Uso delle impostazioni a livello di sistema (ad esempio, Colore di sistema) anziché delle impostazioni di hardwiring per il programma specifico. Rispettare non solo i parametri selezionati in modo specifico dagli utenti per l'interazione con i programmi, ma anche le funzionalità di accessibilità integrate nel sistema operativo che l'utente vuole in effetti, indipendentemente dal programma in uso. Per altre informazioni, vedere [Informazioni sulle Windows di accessibilità.](/previous-versions//ms695605(v=vs.85))
-   Preferendo i controlli comuni ai controlli personalizzati, perché i controlli comuni hanno già implementato le API Windows di accessibilità.
-   Documentazione di tutte le opzioni e le funzionalità di accessibilità (ad esempio, tutti i tasti di scelta rapida). Gli utenti con problemi sono altamente motivati a individuare le funzionalità di accessibilità e spesso prevedono la raccolta di informazioni complete nella Guida.
-   Creazione di documentazione accessibile in formati accessibili. Pertanto, la documentazione stessa deve rispettare le stesse regole di accessibilità dell'interfaccia utente principale, tra cui la possibilità di ingrandire le dimensioni del carattere, l'uso del testo alternativo per la grafica e l'architettura delle informazioni ridondante (ad esempio, l'uso della codifica a colori solo come supplemento al testo).

Nei prodotti software, il rispetto per gli utenti può manifestarsi nell'usabilità e nella ricerca di mercato, nei servizi di supporto e nella documentazione efficaci e, naturalmente, nelle decisioni di progettazione. Ad esempio, pensare di nuovo in termini di progettazione per gli utenti avanzati: si sta inserendo questa nuova funzionalità all'avanguardia perché lo si vuole o perché si sa che gli utenti avanzati l'hanno richiesta? Quest'ultimo caso indica che il processo decisionale di progettazione è ben informato dal valore del rispetto.

**Fornire l'accesso a livello di codice**

Fornire l'accesso a livello di codice all'interfaccia utente è essenziale in modo che le tecnologie di assistive (ad esempio utilità per la lettura dello schermo, dispositivi di input alternativi e programmi di riconoscimento vocale) interpretino correttamente lo schermo per gli utenti. Creando una "mappa" di ogni schermata dell'interfaccia utente nel programma, la si rende disponibile agli utenti delle tecnologie di assistive.

Per eseguire questa operazione, eseguire le seguenti operazione:

-   Abilitazione dell'accesso a livello di codice a tutti gli elementi dell'interfaccia utente e al testo, ad esempio usando l'interfaccia COM [**Active Accessibility, IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).
-   Inserimento di nomi (o titoli) e descrizioni in oggetti, frame e pagine dell'interfaccia utente, ad esempio usando la [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Name.
-   Assicurarsi che gli eventi a livello di codice siano attivati da tutte le attività dell'interfaccia utente, ad esempio gli eventi di stato attivo per tutte le attività dell'interfaccia utente che comportano lo spostamento dello stato attivo.

**Se si eservino solo quattro operazioni...**

1.  Assicurarsi che ogni utente possa sfruttare tutte le potenzialità del programma.
2.  L'accessibilità può essere un'opportunità per la risoluzione dei problemi creative e un altro modo per aumentare la soddisfazione complessiva degli utenti.
3.  Rispettare le impostazioni di sistema.
4.  Usare i controlli comuni quando possibile.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Non interrompere o disabilitare le funzionalità attivate del sistema operativo o di altri prodotti identificati come funzionalità di accessibilità.** È possibile identificare queste funzionalità facendo riferimento alla documentazione del sistema operativo o del prodotto in questione.
-   **Non forzare gli utenti a interagire con il programma come finestra superiore sullo schermo.** Se una funzione o una finestra è necessaria in modo continuo per consentire agli utenti di eseguire un'attività, tale finestra deve rimanere sempre visibile, se l'utente lo sceglie, indipendentemente dalla posizione relativa ad altre finestre. Ad esempio, se l'utente dispone di una tastiera mobile su schermo che si trova sopra tutte le altre finestre in modo che sia sempre visibile, il programma non deve mai nasconderla tramite il posizionamento obbligatorio nella parte superiore dell'ordine [Z.](glossary.md)
-   **Quando possibile, usare colori di sistema, tipi di carattere e controlli comuni.** In questo modo, si riduce significativamente il numero di problemi di accessibilità riscontrati dagli utenti.

### <a name="addressing-particular-impairments"></a>Affrontare particolari problemi

**Visual**

-   **Non fare mai affidamento solo sul colore per trasmettere il significato.** Usare il colore solo come mezzo per rafforzare il significato fornito da testo, progettazione, posizione o suono.

    ![Screenshot dell'icona del comunicatore rosso e della descrizione comando ](images/inter-accessibility-image9.png)

    Il metodo principale di comunicazione in questo esempio è il testo conciso della descrizione comando. L'uso del colore aiuta a comunicare il significato, ma è secondario.

-   **Usare suggerimenti alternativi per il testo (alt) per descrivere la grafica.**
-   **Non usare testo nella grafica.** Gli utenti con problemi visivi possono avere la grafica disattivata (ad esempio, in un Web browser) o semplicemente non visualizzare o cercare testo inserito nella grafica.
-   **Assicurarsi che le finestre di** dialogo e le finestre hanno nomi significativi, in modo che un utente che sta udindo anziché visualizzare lo schermo (ad esempio, usando un'utilità per la lettura dello schermo) osezioni le informazioni contestuali appropriate.
-   Rispettare le impostazioni **dell'utente** per la visualizzazione visiva ottenendo sempre caratteri tipografici, dimensioni e colori del tipo di carattere, dimensioni Windows dimensioni degli elementi di visualizzazione e impostazioni di configurazione del sistema dalle API Theme e GetSystemMetrics.
-   **Mantenere conciso il testo del fumetto** in modo che sia più facile da leggere e ridurre al minimo l'interruzione delle utilità per la lettura dello schermo.

    ![Screenshot del fumetto che indica i limiti del codice pin ](images/inter-accessibility-image10.png)

    Anche se i fumetto possono usare testo aggiuntivo del corpo se necessario, questo esempio mostra che talvolta solo il testo del titolo raggiunge lo stesso obiettivo in modo più economico e accessibile.

**Udito**

-   **Non affidarsi mai al suono da solo per trasmettere il significato.** Usare il suono solo come mezzo per rafforzare il significato fornito da testo, progettazione, posizione o colore.
-   **Consentire agli utenti di controllare il volume dell'output audio.** Usare il Windows volume Mixer a questo scopo. Per altre informazioni, vedere [Sound](vis-sound.md).
-   Impostare come destinazione il suono del programma in modo che si verifichi in un intervallo compreso tra **500 Hz e 3000 Hz** o sia facilmente regolabile dall'utente in tale intervallo. I suoni in questo intervallo sono molto probabilmente rilevabili da persone con problemi udibili.

**Destrezza**

-   **Impostare i valori di timeout dell'interfaccia utente rispetto a GetDoubleClickTime() anziché usare i tempi assoluti.** In questo modo i timeout vengono adattati alla velocità dell'utente.
-   **Assegnare i tasti** di scelta a tutte le voci di menu in modo che gli utenti che preferiscono usare la tastiera hanno la stessa possibilità di spostarsi nel programma degli utenti che lavorano con il mouse.
-   **Non fare doppio clic e trascinare l'unico modo per eseguire un'azione.** Questi possono essere movimenti difficili per alcuni utenti.
-   **Non rimuovere le barre dei menu dal programma.** Le barre dei menu sono più semplici rispetto alle barre degli strumenti a cui gli utenti possono accedere tramite tastiera. Se non si vuole che la barra dei menu sia visibile per impostazione predefinita, nasconderla.
-   **Rendere accessibile la Guida dalla tastiera fornendo tabulazioni per i pulsanti e i collegamenti della Guida.**
-   **Per migliorare la consapevolezza delle assegnazioni delle chiavi di accesso nel programma, è possibile visualizzarle in qualsiasi momento.** In Pannello di controllo passare alla Centro accessibilità e fare clic su Rendi la **tastiera più semplice da usare.** quindi selezionare la casella **di controllo Sottolinea tasti di scelta rapida e** tasti di scelta.

**Analisi cognitiva**

-   **Usare la diffusione progressiva** per nascondere la complessità.

    ![Screenshot dei pulsanti di divisione con triangoli verso il basso ](images/inter-accessibility-image11.png)

    In questi esempi le opzioni disponibili dal pulsante di comando sono nascoste per impostazione predefinita e gli utenti possono scegliere di visualizzare le opzioni sfruttando i controlli di divulgazione progressiva.

-   **Usare icone, barre degli strumenti e altri strumenti visivi per** ridurre il carico cognitivo di lettura del testo.
-   Quando possibile, fornire funzionalità di completamento automatico **nelle** caselle di testo e negli elenchi a discesa modificabili, in modo che gli utenti non devono digitare l'intero nome di comandi, nomi di file o scelte simili da un set limitato di opzioni. In questo modo si riduce il carico cognitivo per tutti gli utenti e si riduce la quantità di digitazione per gli utenti per i quali l'ortografia o la digitazione è difficile, lenta o complicata.
-   **Illustrare concetti complessi nella Guida includendo esercitazioni e animazioni.** Si noti che le animazioni possono essere difficili per gli utenti con problemi di disabilità e pertanto devono essere usate solo quando necessario.

**Sequestro**

-   **Non usare testo lampeggiante o lampeggiante, oggetti o altri elementi con una frequenza flash o lampeggiante compresa nell'intervallo compreso tra 2 e 55 Hz.**
-   **Limitare l'uso delle animazioni.** Alcuni utenti sono particolarmente sensibili al movimento dello schermo, soprattutto nella periferia del campo visivo. Se si usa l'animazione per attirare l'attenzione su un elemento, assicurarsi che l'attenzione sia disattenta e che l'utente interrompa l'utente.

**Voce o lingua**

-   **Organizzare e scrivere testo chiaro, conciso e facilmente comprensibile.** I test di usabilità mostrano che l'estensione delle informazioni chiave alla fine di una frase migliora la comprensione. Per altre linee guida, vedere [Stile e tono.](text-style-tone.md)

**Non corretto:**

Tre è la cifra successiva?

Fare clic su OK per iniziare.

**Corretto:**

La cifra successiva è tre?

Per iniziare, fare clic su OK.

### <a name="access-keys"></a>Chiavi di accesso

-   **Preferisce caratteri con larghezze ampie,** ad esempio w, m e lettere maiuscole.
-   **Preferisce una consonante distintiva o una vocale,** ad esempio "x" in "Exit".
-   **Evitare di usare caratteri che rendono difficile la sottolineatura,** ad esempio (dalla più problematica alla meno problematica):
    -   Caratteri che hanno una larghezza di un solo pixel, ad esempio i e l.
    -   Caratteri con discendenti, ad esempio g, j, p, q e y.
    -   Caratteri accanto a una lettera con un discendente.

### <a name="menu-access-keys"></a>Tasti di scelta dei menu

-   **Assegnare le chiavi di accesso a tutte le voci di menu.** Nessuna eccezione.
-   **Per le voci di menu dinamico, ad esempio i file usati di recente, assegnare numericamente le chiavi di accesso.**

    ![Screenshot del menu Apri con i file usati di recente ](images/inter-accessibility-image12.png)

    In questo esempio il programma Paint in Windows assegna chiavi di accesso numeriche ai file usati di recente.

-   **Assegnare chiavi di accesso univoche all'interno di un livello di menu.** È possibile riutilizzare le chiavi di accesso in diversi livelli di menu.
-   **Semplificare la ricerca delle chiavi di accesso:**
    -   Per le voci di menu usate più di frequente, scegliere i caratteri all'inizio della prima o della seconda parola dell'etichetta, preferibilmente il primo carattere.
    -   Per le voci di menu usate meno di frequente, scegliere lettere distintive consonanti o vocali nell'etichetta.

### <a name="dialog-box-access-keys"></a>Tasti di scelta della finestra di dialogo

-   **Quando possibile, assegnare chiavi di accesso univoche a tutti i controlli interattivi o alle relative etichette.** [Le caselle di testo di sola](ctrl-text-boxes.md) lettura sono controlli interattivi(perché gli utenti possono scorrerle e copiare il testo), quindi traggono vantaggio dai tasti di scelta. **Non assegnare chiavi di accesso a:**
    -   **PULSANTI OK, Annulla e Chiudi.** Per le chiavi di accesso vengono usati i tasti invio e ESC. Tuttavia, assegnare sempre un tasto di scelta a un controllo che indica OK o Annulla, ma ha un'etichetta diversa.

        ![Screenshot dei controlli con chiavi di accesso assegnate ](images/inter-accessibility-image13.png)

        In questo esempio, al pulsante commit positivo è assegnata una chiave di accesso.

-   **Raggruppare le etichette.** In genere, ai singoli controlli all'interno di un gruppo vengono assegnati tasti di scelta, quindi l'etichetta del gruppo non ne richiede uno. Tuttavia, assegnare una chiave di accesso all'etichetta del gruppo e non i singoli controlli in caso di mancanza di chiavi di accesso.
-   **Pulsanti della Guida generica a** cui si accede con F1.
-   **Collegare le etichette.** Spesso sono presenti troppi collegamenti per assegnare chiavi di accesso univoche e i caratteri di sottolineatura dei collegamenti nascondono i caratteri di sottolineatura dei tasti di scelta. Fare in modo che gli utenti accedono ai collegamenti con il tasto TAB.
-   **Nomi delle schede.** Le schede vengono spostate in ciclo usando CTRL+TAB e CTRL+MAIUSC+TAB.
-   **Pulsanti Sfoglia con etichetta "...".** Non è possibile assegnare chiavi di accesso in modo univoco.
-   **Controlli senza etichetta, ad** esempio controlli di selezione, pulsanti di comando grafici e controlli di divulgazione progressiva senza etichetta.
-   **Testo statico non etichettato o etichette per i controlli non interattivi,** ad esempio gli barre di stato.
-   **Assegnare prima le chiavi di accesso del pulsante di commit per assicurarsi che siano assegnate le assegnazioni di chiave standard.** Se non è presente un'assegnazione di chiave standard, usare la prima lettera della prima parola. Ad esempio, il tasto di scelta per i pulsanti Sì e No commit deve essere sempre "Y" e "N", indipendentemente dagli altri controlli nella finestra di dialogo.
-   **Per i pulsanti di commit negativi (diversi da Annulla) formulati come "Non fare", assegnare la chiave di accesso a "n" in "Non fare".** Se non viene formulata come "Non usare", usare l'assegnazione standard della chiave di accesso o assegnare la prima lettera della prima parola. In questo modo, tutti i valori Don'ts e No hanno una chiave di accesso coerente.
-   **Per semplificare** la ricerca dei tasti di scelta, assegnare i tasti di scelta a un carattere visualizzato all'inizio dell'etichetta, idealmente il primo carattere, anche se è presente una parola chiave che viene visualizzata più avanti nell'etichetta.

Per altre linee guida ed esempi, vedere [Tastiera.](inter-keyboard.md)

## <a name="text"></a>Testo

-   **Usare i due punti alla fine delle etichette di controllo esterne.** Alcune tecnologie di assistive technology ricercano i due punti per identificare le etichette dei controlli.
-   **Posizionare le etichette in modo coerente rispetto agli elementi che stanno etichettando.** Ciò consente assistive technology associare correttamente le etichette ai controlli corrispondenti e consente agli utenti degli ingranditori dello schermo di sapere dove cercare un'etichetta o un controllo.

    ![Screenshot delle etichette posizionate in modo coerente ](images/inter-accessibility-image14.png)

    In questo esempio le etichette per ogni elenco a discesa vengono posizionate in modo coerente e usano i due punti.

-   **Limitare il testo alternativo a un massimo di 150 caratteri.** Descrivere l'azione per attivare il controllo ( ad esempio, fare clic, fare clic con il pulsante destro del mouse e così via) e quindi descrivere la funzione del controllo.

    **Accettabile:**

    Pulsante.

    Blu blu.

    **Migliore:**

    Fare clic per accedere al proprio account.

    Foto di lontano che mostra la dissolvenza dei colori sulla distanza.

-   **Non usare il testo per disegnare linee, caselle o altri simboli grafici.** I caratteri usati in questo modo possono confondere gli utenti delle utilità per la lettura dello schermo. Ad esempio, una casella disegnata con la lettera "X" intorno a un'area di testo viene letta dal software di lettura dello schermo come "X X X X X X" sulla prima riga, seguita da "X" e dal contenuto e da "X".

## <a name="documentation"></a>Documentazione

-   Documentare tutte le opzioni e le funzionalità di accessibilità, ad esempio tutti i tasti di scelta rapida.
-   Creare documentazione accessibile in formati accessibili. Di conseguenza, la documentazione stessa deve rispettare le stesse regole di accessibilità dell'interfaccia utente principale.
-   Fare riferimento ai tasti di scelta, non ai tasti di scelta rapida (che hanno un significato e un uso diversi), ai tasti di scelta rapida o ai tasti di scelta rapida.
-   In generale, fare riferimento a una persona con un tipo di disabilità, non a una persona disabile. Si consideri prima di tutto la persona, non l'etichetta.



| Usare queste condizioni           | Anziché                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------|
| Ha una complessità limitata, ha disabilità del movimento<br/>     | Crippled, lame<br/>                                                        |
| Senza disabilità<br/>                               | Normale, con corpo in grado, integro<br/>                                          |
| Persone con una mano che digitano con una mano<br/>          | Con una sola mano <br/>                                                        |
| Persone con disabilità<br/>                           | Le persone disabilitate, disabilitate, le persone con i bambini, i bambini<br/> |
| Disabilità cognitive, disabilità di sviluppo<br/> |                                                                                  |



 

