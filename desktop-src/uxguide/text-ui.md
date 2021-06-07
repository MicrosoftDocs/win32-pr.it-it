---
title: Interfaccia utente testo
description: Informazioni sul testo dell'interfaccia utente visualizzato nelle superfici dell'interfaccia utente.
ms.assetid: db42fe22-9baf-453a-9b89-9bbb251b0b6f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a0ab5025407d5149d1747fbd083fed7df345e3f3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444742"
---
# <a name="user-interface-text"></a>Interfaccia utente testo

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Il testo dell'interfaccia utente viene visualizzato nelle superfici dell'interfaccia utente. Questo testo include le etichette dei controlli e il testo statico:

-   Le etichette dei controlli identificano i controlli e vengono posizionate direttamente su o accanto ai controlli.
-   Il testo statico, chiamato così perché non fa parte di un controllo interattivo, fornisce agli utenti istruzioni o spiegazioni dettagliate in modo che possano prendere decisioni informate.

**Nota:** Le linee guida relative [allo stile e al tono,](text-style-tone.md) [ai](vis-fonts.md)tipi di carattere e alle etichette dei controlli [comon](controls.md) sono presentate in articoli separati.

## <a name="usage-patterns"></a>Modelli di utilizzo

Il testo dell'interfaccia utente ha diversi modelli di utilizzo:



|   Utilizzo                                                                                                                                                                                          |    Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Testo per la barra del titolo**<br/> Usare il testo della barra del titolo per identificare una finestra o l'origine di una finestra di dialogo. <br/>                                                                            | ![Screenshot della barra del titolo delle opzioni della cartella](images/text-ui-image1.png)<br/> In questo esempio il testo della barra del titolo identifica una finestra.<br/>                                                                                                                                                                                                                                                                                                             |
| **Istruzioni principali**<br/> Usare l'istruzione principale principale per spiegare concisamente cosa fare nella finestra o nella pagina. <br/>                                                      | L'istruzione deve essere un'istruzione specifica, una direzione imperativa o una domanda. le istruzioni principali di buona qualità comunicano l'obiettivo dell'utente anziché concentrarsi solo sulla manipolazione dell'interfaccia utente. <br/> ![Screenshot della domanda: si vuole visualizzare la Guida più recente? ](images/text-ui-image2.png)<br/> In questo esempio, il testo dell'istruzione principale coinvolge direttamente l'utente con una domanda in termini di vantaggio o interesse dell'utente.<br/>             |
| **Istruzioni supplementari**<br/> Quando necessario, usare un'istruzione supplementare per presentare informazioni aggiuntive utili per comprendere o usare la finestra o la pagina. <br/> | È possibile fornire informazioni più dettagliate, fornire il contesto e definire la terminologia. istruzioni supplementari elaborate sull'istruzione principale senza semplicemente ri wording. <br/> ![Screenshot del testo quando si passa all'account amministratore ](images/text-ui-image3.png)<br/> In questo esempio le istruzioni supplementari forniscono due possibili corsi di azione da intraprendere in risposta alle informazioni presentate nell'istruzione principale.<br/> |
| **Etichette di controllo**<br/> etichette direttamente su o accanto ai controlli. <br/>                                                                                                           | ![Screenshot delle opzioni dell'orologio del desktop ](images/text-ui-image4.png)<br/> In questo esempio, le etichette dei controlli identificano le impostazioni dell'orologio del desktop che gli utenti possono selezionare o modificare.<br/>                                                                                                                                                                                                                                                                       |
| **Spiegazioni supplementari**<br/> un'elaborazione delle etichette dei controlli (in genere per i collegamenti ai comandi, i pulsanti di opzione e le caselle di controllo). <br/>                                    | ![Screenshot che mostra una finestra di dialogo delle impostazioni di sicurezza.](images/text-ui-image5.png)<br/> In questo esempio le spiegazioni supplementari chiariscono le scelte.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Gli sviluppatori di software spesso pensano al testo come alla documentazione del prodotto e al supporto tecnico. "Prima di tutto si scriverà il codice e quindi si assumerà qualcuno per spiegare ciò che è stato sviluppato". In realtà, tuttavia, il testo importante viene scritto in una parte precedente del processo, perché l'interfaccia utente viene concepita e codificata. Questo testo è, dopo tutto, visto più frequentemente e da più persone rispetto a qualsiasi altro tipo di scrittura tecnica.

**Il testo comprensibile è fondamentale per un'interfaccia utente efficace.** Gli editor e gli autori professionisti devono collaborare con gli sviluppatori software al testo dell'interfaccia utente come parte integrante del processo di progettazione. Fare in modo che il testo funzioni in anticipo perché i problemi di testo spesso rivelano problemi di progettazione. Se il team ha problemi a spiegare una progettazione, spesso è la progettazione, non la spiegazione, a migliorare.

### <a name="a-design-model-for-ui-text"></a>Modello di progettazione per il testo dell'interfaccia utente

Quando si pensa al testo dell'interfaccia utente e al relativo posizionamento sulle superfici dell'interfaccia utente, considerare questi fatti:

-   Durante la lettura incentrata e immersiva, le persone leggono in ordine da sinistra a destra e dall'alto verso il basso (nelle culture occidentali).
-   Quando si usa il software, gli utenti non sono immersi nell'interfaccia utente stessa, ma nel proprio lavoro. Di conseguenza, gli utenti non leggono il testo dell'interfaccia utente che analizzano.
-   Quando si esegue la scansione di una finestra, gli utenti potrebbero sembrare che leggono il testo quando in realtà lo filtrano. Spesso non comprendono realmente il testo dell'interfaccia utente a meno che non percepiranno la necessità di .
-   All'interno di una finestra, diversi elementi dell'interfaccia utente ricevono diversi livelli di attenzione. Gli utenti tendono a leggere prima le etichette di controllo, in particolare quelle che sembrano rilevanti per il completamento dell'attività in corso. Al contrario, gli utenti tendono a leggere il testo statico solo quando ne hanno l'esigenza.

Per un modello di progettazione generale, non presupporre che gli utenti leggono attentamente il testo in ordine dall'alto verso destra e dall'alto verso il basso. Si supponga invece che gli utenti inizino a analizzare rapidamente l'intera finestra e quindi leggono il testo dell'interfaccia utente approssimativamente nell'ordine seguente:

-   Controlli interattivi al centro
-   Pulsanti [di commit](glossary.md)
-   Controlli interattivi trovati altrove
-   Istruzione main
-   Spiegazioni supplementari
-   Titolo della finestra
-   Altro testo statico nel corpo principale
-   Note a piè di pagina

È anche necessario presupporre che, una volta che gli utenti hanno deciso cosa fare, smetteranno immediatamente di leggere ed eseguire questa operazione.

### <a name="eliminate-redundancy"></a>Eliminare la ridondanza

Il testo ridondante non solo richiede spazio prezioso sullo schermo, ma ne attenua l'efficacia delle idee o delle azioni importanti che si sta tentando di trasmettere. È anche uno spreco di tempo per il lettore, a maggior parte in un contesto in cui l'analisi è la norma. **Windows si impegna a spiegare ciò che gli utenti devono fare una volta bene e concisamente.**

Esaminare ogni finestra ed eliminare parole e istruzioni duplicate, sia all'interno che tra i controlli. Non evitare che il testo importante sia esplicito laddove necessario, ma non essere ridondante e non spiegare l'ovvio.

### <a name="avoid-over-communication"></a>Evitare l'over communication

Anche se il testo non è ridondante, può essere semplicemente troppo semplice per spiegare ogni dettaglio. **Una quantità troppo grande di testo sconsiglia la lettura dell'occhio tende a ignorarlo in modo ironico, con una conseguente minore comunicazione anziché un maggior numero di messaggi.** Nel testo dell'interfaccia utente comunicare concisamente le informazioni essenziali. Se sono necessarie altre informazioni per alcuni utenti o alcuni [](winenv-help.md)scenari, fornire un collegamento a contenuto della Guida più dettagliato o, ad esempio, a una voce di glossario per chiarire un termine.

**Non corretto:**

![Screenshot della finestra di dialogo con 6 paragrafi](images/text-ui-image6.png)

In questo esempio è presente una quantità di testo troppo grande da analizzare facilmente. Anche se non è previsto dalla finestra di progettazione, molto probabilmente gli utenti potranno fare clic su Avanti senza leggere nulla.

Per evitare testo che sconsiglia la lettura, creare il testo in modo che ogni parola sia conteggiato. Ciò che non aggiunge sottrazioni, quindi usare testo semplice e conciso.

### <a name="use-the-inverted-pyramid"></a>Usare la piramide invertita

La scrittura accademica usa in genere uno stile strutturale "piramide" che basa una base di fatti, opera con tali fatti e si basa su una conclusione che forma una struttura simile a una piramide. Al contrario, i lettori usano uno stile di "piramide invertita" che inizia con la conclusione del "takeaway" fondamentale che i lettori devono avere. Vengono quindi compilati progressivamente più dettagli a cui i lettori potrebbero essere interessati solo per l'analisi. Il vantaggio di questo stile è che si arriva direttamente al punto e consente ai lettori di interrompere la lettura in qualsiasi momento scelto e di comprendere comunque le informazioni essenziali.

È consigliabile applicare la struttura a piramide invertita al testo dell'interfaccia utente. È possibile arrivare direttamente al punto con le informazioni essenziali, consentire agli utenti di smettere di leggere in qualsiasi momento e usare un collegamento alla Guida per presentare il resto della piramide.

![screenshot del messaggio quando si partecipa a un programma Windows ](images/text-ui-image7.png)

In questo esempio le informazioni essenziali sono contenute nella query del testo dell'istruzione principale, altre informazioni utili sono disponibili nelle istruzioni supplementari e i dettagli sono disponibili facendo clic su un collegamento alla Guida.

**Se si eservino solo cinque operazioni...**

1.  Lavorare in anticipo sul testo perché i problemi di testo spesso rivelano problemi di progettazione.
2.  Progettare il testo per l'analisi.
3.  Eliminare il testo ridondante.
4.  Usare testo di facile comprensione; non comunicano in modo over.
5.  Se necessario, fornire collegamenti al contenuto della Guida per informazioni più dettagliate.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Rimuovere il testo ridondante.** Cercare testo ridondante nei titoli delle finestre, nelle istruzioni principali, nelle istruzioni supplementari, nelle aree di contenuto, nei collegamenti ai comandi e nei pulsanti di commit. In genere, lasciare il testo completo nelle istruzioni principali e nei controlli interattivi e rimuovere la ridondanza dalle altre posizioni.
-   **Evitare blocchi di testo dell'interfaccia utente di grandi dimensioni.** I modi per eseguire questa operazione includono:
    -   Suddivisione del testo in frasi e paragrafi più brevi.
    -   Se necessario, fornire [collegamenti alla Guida](winenv-help.md) a informazioni utili, ma non essenziali.
-   **Scegliere i nomi e le etichette degli oggetti che comunicano chiaramente e differenziano le informazioni sull'oggetto.** Gli utenti non devono capire cosa significa realmente l'oggetto o in che modo differisce da altri oggetti.

    Non corretto:

    ![Screenshot dell'elenco di monitor senza nome](images/text-ui-image8.png)

    Migliore:

    ![Screenshot dell'elenco di adattatori di rete specifici](images/text-ui-image9.png)

    Nell'esempio non corretto, i nomi degli oggetti non sono affatto differenziati; l'esempio migliore mostra la differenziazione forte in base al nome del prodotto.

-   **Per assicurarsi che gli utenti leggono testo specifico correlato a un'azione, posizionarlo in un controllo interattivo.**
    -   **Accettabile:**
    -   ![Screenshot dell'avviso di formattazione tramite il pulsante OK ](images/text-ui-image10.png)
    -   In questo esempio è possibile che gli utenti non leggono il testo che spiega cosa stanno confermando.
    -   **Migliore:**
    -   ![Screenshot dell'avviso di formattazione e del pulsante Formatta ](images/text-ui-image11.png)
    -   In questo esempio è possibile assicurarsi che almeno gli utenti comprendano che stanno per formattare un disco.
-   **Usare uno spazio tra le frasi.** Non due.

### <a name="text-fonts-sizes-and-colors"></a>Tipi di carattere, dimensioni e colori del testo

-   **Usare il testo blu solo per i collegamenti e le istruzioni principali.**
-   **Usare il testo verde solo per gli URL nei risultati della ricerca.**

I tipi di carattere e i colori seguenti sono predefiniti per Windows.



| Modello                                                                                     | Simbolo del tema                            | Tipo di carattere, Colore                                                           |
|--------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![prima colonna: testo della barra del titolo ](images/text-ui-image12.png)<br/>              | CaptionFont<br/>      | 9 pt. nero \# (000000) Segoe UI<br/>                 |
| ![prima colonna: istruzioni principali ](images/text-ui-image13.png)<br/>           | MainInstruction<br/>  | 12 pt. blu \# (003399) Segoe UI<br/>                 |
| ![prima colonna: istruzioni secondarie ](images/text-ui-image14.png)<br/>      | Istruzione<br/>      | 9 pt. nero \# (000000) Segoe UI<br/>                 |
| ![prima colonna: testo normale ](images/text-ui-image15.png)<br/>                 | BodyText<br/>         | 9 pt. nero \# (000000) Segoe UI<br/>                 |
| ![prima colonna: testo evidenziato ](images/text-ui-image16.png)<br/>             | BodyText<br/>         | 9 pt. nero \# (000000) Segoe UI, grassetto o corsivo<br/> |
| ![prima colonna: testo modificabile ](images/text-ui-image17.png)<br/>               | BodyText<br/>         | 9 pt. nero \# (000000) Segoe UI, in una casella<br/>       |
| ![prima colonna: testo disabilitato ](images/text-ui-image18.png)<br/>               | Disabled<br/>         | 9 pt. grigio scuro \# (323232) Segoe UI<br/>             |
| ![prima colonna: collegamento ](images/text-ui-image19.png)<br/>                        | HyperLinkText<br/>    | 9 pt. blu \# (0066CC) Segoe UI<br/>                  |
| ![prima colonna: collegamenti (passaggio del mouse) ](images/text-ui-image20.png)<br/>               | Accesso frequente<br/>              | 9 pt. blu chiaro \# (3399FF) Segoe UI<br/>            |
| ![prima colonna: intestazione di gruppo ](images/text-ui-image21.png)<br/>                |  <br/>                | 11 pt. blu \# (003399) Segoe UI<br/>                 |
| ![prima colonna: nome file (nella visualizzazione contenuto) ](images/text-ui-image22.png)<br/> |  <br/>                | 11 pt. nero \# (000000) Segoe UI<br/>                |
| ![prima colonna: testo del documento ](images/text-ui-image23.png)<br/>               | (nessuna)<br/>           | 9 pt. nero \# (000000) Calibri<br/>                  |
| ![prima colonna: intestazioni di documento ](images/text-ui-image24.png)<br/>           | (nessuna)<br/>           | 17 pt. nero \# (000000) Calibri<br/>                 |



 

Per altre informazioni ed esempi, vedere [Tipi di carattere](vis-fonts.md) e [colore](vis-color.md).

### <a name="other-text-characteristics"></a>Altre caratteristiche del testo

**Grassetto**

-   **Usare il grassetto con parsimonio per attirare l'attenzione sul testo che gli utenti devono leggere.** Ad esempio, gli utenti che esercitino la scansione di un elenco di opzioni dei pulsanti di opzione possono apprezzare la visualizzazione delle etichette in grassetto, per distinguersi dal testo che aggiunge informazioni supplementari su ogni opzione. Tenere presente che l'uso di troppo grassetto ne consente una minore influenza.
-   **Con i dati etichettati, usare il grassetto per evidenziare qualsiasi cosa sia più importante per i dati nel suo complesso.**
    -   Per i dati per lo più generici (in cui i dati hanno poco significato senza etichette, come con numeri o date), usare etichette in grassetto e dati semplici in modo che gli utenti possano analizzare e comprendere più facilmente i tipi di dati.
    -   Per i dati per lo più auto-esplicativi, usare etichette semplici e dati in grassetto in modo che gli utenti possano concentrarsi sui dati stessi.
    -   In alternativa, è possibile usare il testo grigio scuro per de-evidenziare le informazioni meno importanti invece di usare il grassetto per evidenziare le informazioni più importanti.

        ![Screenshot della visualizzazione dell'anteprima di Esplora risorse ](images/text-ui-image25.png)

        In questo esempio, invece di enfatizzare i dati usando il grassetto, le etichette vengono de-sottolineate usando il grigio scuro.

-   **Non tutti i tipi di carattere supportano il grassetto, quindi non deve mai essere fondamentale comprendere il testo.**

**Corsivo**

-   Usare per fare riferimento letteralmente al testo. Non usare le virgolette a questo scopo.

    **Corretto:**

    I termini documento e file vengono spesso usati in modo intercambiabile.

-   Usare per [le richieste](glossary.md) nelle [caselle di testo](ctrl-text-boxes.md) e negli elenchi a discesa [modificabili.](/windows/desktop/uxguide/ctrl-drop)

    ![Screenshot della casella di testo di ricerca ](images/text-ui-image26.png)

    In questo esempio il prompt nella casella Di ricerca viene formattato come testo in corsivo.

-   Usare con parsimonio per evidenziare parole specifiche per facilitare la comprensione.
-   **Non tutti i tipi di carattere supportano il corsivo, quindi non deve mai essere fondamentale comprendere il testo.**

**Corsivo grassetto**

-   Non usare nel testo dell'interfaccia utente.

**Sottolineato**

-   Non usare, ad eccezione dei collegamenti.
-   Non usare per l'enfasi. Usare invece il corsivo.

### <a name="punctuation&quot;></a>Punteggiatura

**Periodi**

-   **Non posizionare alla fine delle etichette di controllo, delle istruzioni principali o dei collegamenti della Guida.**
-   Posizionare alla fine di istruzioni supplementari, spiegazioni supplementari o qualsiasi altro testo statico che forma una frase completa.

**punti interrogativi**

-   **Posizionare alla fine di tutte le domande.** A differenza dei punti, i punti interrogativi vengono usati per tutti i tipi di testo.

**Punti esclamativi**

-   Nelle applicazioni aziendali, evitare.
    -   **Eccezioni:** I punti esclamativi vengono talvolta usati nel contesto di completamento del download (&quot;Done!") e per richiamare l'attenzione sul contenuto Web ("Nuovo!").

**Virgole**

-   In un elenco di tre o più elementi inserire sempre una virgola dopo l'ultimo elemento dell'elenco.

**Due punti**

-   **Usare i due punti alla fine delle etichette di controllo esterne.** Ciò è particolarmente importante per l'accessibilità perché alcune tecnologie di assistive ricercano i due punti per identificare le etichette di controllo.
-   Usare i due punti per introdurre un elenco di elementi.

**Ellissi**

-   **I puntini di sospensione significano incompletezza.** Usare i puntini di sospensione nel testo dell'interfaccia utente come segue:
    -   **Comandi:** Indicare che un comando richiede informazioni aggiuntive. Non usare i puntini di sospensione ogni volta che un'azione visualizza un'altra finestra solo quando sono necessarie informazioni aggiuntive. Per altre informazioni, vedere [Pulsanti di comando](ctrl-command-buttons.md).
    -   **Dati:** Indicare che il testo viene troncato.
    -   **Etichette:** Indicare che un'attività è in corso, ad esempio "Ricerca in corso".

        **Suggerimento:** Il testo troncato in una finestra o in una pagina con spazio inutilizzato indica un layout insufficiente o dimensioni della finestra predefinite troppo piccole. Cercare layout e dimensioni predefinite delle finestre che eliminano o riducono la quantità di testo troncato. Per altre informazioni, vedere [Layout](vis-layout.md).

-   **Non rendere interattivi i puntini di sospensione.** Per visualizzare il testo troncato, consentire agli utenti di ridimensionare il controllo per visualizzare più testo o usare invece un controllo di [diffusione](ctrl-progressive-disclosure-controls.md) progressiva.

**Virgolette e apostrofi**

-   Per fare riferimento letteralmente al testo, usare la formattazione corsiva anziché le virgolette.
-   Inserire i titoli delle finestre e le etichette di controllo tra virgolette solo se necessario per evitare confusione e non è possibile formattare in grassetto.
-   Per le virgolette, preferire le virgolette doppie (" "); evitare virgolette singole.

    **Corretto:**

    Si è certi di voler eliminare la "cartella cat di Sparky"?

    **Non corretto:**

    Si è certi di voler eliminare la cartella cat di Sparky?

### <a name="capitalization"></a>Uso delle maiuscole

-   **Usare l'uso delle maiuscole in stile titolo per i titoli, l'uso di maiuscole e minuscole in stile frase per tutti gli altri elementi dell'interfaccia utente.** Questa operazione è più appropriata per il tono [di Windows.](text-style-tone.md)

    -   **Eccezione:** Per le applicazioni legacy, è possibile usare l'uso di maiuscole e minuscole per i pulsanti di comando, i menu e le intestazioni di colonna, se necessario, per evitare di combinare gli stili di combinazione di maiuscole e minuscole.

        ![Screenshot della finestra delle proprietà generica ](images/text-ui-image27.png)

    Questo esempio generico illustra l'utilizzo corretto di maiuscole e minuscole per le finestre delle proprietà.

    ![Screenshot della finestra di dialogo generica ](images/text-ui-image28.png)

    Questo esempio generico mostra l'utilizzo corretto di maiuscole e minuscole e la punteggiatura per i dialoghe.

-   **Per i nomi di funzionalità e tecnologie, è necessario essere conservativi per l'applicazione di maiuscole e minuscole.** In genere, solo i componenti principali devono essere in maiuscolo (usando l'uso di maiuscole e minuscole in stile titolo).

    **Corretto:**

    Analysis Services, cubi, dimensioni

    Analysis Services è un componente principale dell'SQL Server, pertanto è appropriata l'utilizzo di maiuscole e minuscole in stile titolo. I cubi e le dimensioni sono elementi comuni del software di analisi del database, pertanto non è necessario capitalizzarli.

-   **Per i nomi delle funzionalità e delle tecnologie, è necessario essere coerenti nell'in maiuscolo.** Se il nome viene visualizzato più di una volta in una schermata dell'interfaccia utente, dovrebbe sempre apparire nello stesso modo. Analogamente, in tutte le schermate dell'interfaccia utente del programma, il nome deve essere presentato in modo coerente.
-   Non convertire in maiuscolo i nomi degli elementi dell'interfaccia utente generici, ad esempio barra degli strumenti, menu, barra di scorrimento, pulsante e icona.
    -   **Eccezioni:** Barra degli indirizzi, barra dei collegamenti.
-   Non usare tutte le lettere maiuscole per i tasti della tastiera. Seguire invece le lettere maiuscole usate dalle tastiere standard o lettere minuscole se il tasto non è etichettato sulla tastiera.

    **Corretto:**

    BARRA SPAZIATRICE, TAB, INVIO, PTTA SU, CTRL+ALT+CANC

    **Non corretto:**

    BARRA SPAZIATRICE, TAB, INVIO, PG SU, CTRL+ALT+CANC

-   **Non usare tutte le lettere maiuscole per l'enfasi.** Gli studi hanno dimostrato che questo è difficile da leggere e gli utenti tendono a considerarlo come "urlo". Per gli avvisi, usare un'icona di avviso e una spiegazione chiara della situazione. Non è necessario aggiungere, ad esempio, il termine WARNING in tutte le lettere maiuscole.

Per altre informazioni, vedere la sezione "Testo" o "Etichette" nelle linee guida specifiche del componente dell'interfaccia utente.

### <a name="dates-and-times"></a>Date e ore

-   **Non codificare a livello di codice il formato di date e ore.** Rispettare la scelta dell'utente di impostazioni locali e opzioni di personalizzazione per i formati di data e ora. L'utente le seleziona nell'elemento del pannello di controllo Area e lingua.

    ![Screenshot del formato della data: lunedì 06 luglio 2009](images/text-ui-image29.png)![Screenshot del formato data: 06 luglio 2009](images/text-ui-image30.png)

    In questi esempi di Microsoft Outlook entrambi i formati per la data lunga sono corretti. Riflettono le diverse scelte effettuate dagli utenti nell'elemento del pannello di controllo Area e lingua.

-   **Usare il formato di data lunga per scenari che traggono vantaggio dalla presenza di informazioni aggiuntive.** Usare il formato di data breve per i contesti che non hanno spazio sufficiente per il formato lungo. Mentre gli utenti scelgono le informazioni da includere nei formati lunghi e brevi, i progettisti scelgono il formato da visualizzare nei programmi in base allo scenario e al contesto.

    ![Screenshot del formato con date di inizio e scadenza](images/text-ui-image31.png)

    In questo esempio, il formato di data lunga consente agli utenti di organizzare attività e scadenze.

### <a name="globalization-and-localization"></a>Globalizzazione e localizzazione

La globalizzazione significa creare documenti o prodotti utilizzabili in qualsiasi paese, area geografica o cultura. Localizzazione significa adattare documenti o prodotti per l'uso in impostazioni locali diverse dal paese o dall'area geografica di origine. Prendere in considerazione la globalizzazione e la localizzazione durante la scrittura di testo dell'interfaccia utente. Il programma può essere tradotto in altre lingue e usato in impostazioni cultura molto diverse dalle proprie.

-   Per i controlli con contenuto variabile, ad esempio visualizzazioni elenco e visualizzazioni albero, scegliere una **larghezza appropriata per i dati validi più lunghi.**
-   Includere spazio sufficiente nella superficie dell'interfaccia utente per un ulteriore **30%** (fino al 200% per il testo più breve) per qualsiasi testo (ma non numeri) che verrà localizzato. La traduzione da una lingua a un'altra spesso modifica la lunghezza della riga del testo.
-   Non comporre stringhe da sottostringhe in fase di esecuzione. Usare invece frasi complete in modo da non creare ambiguità per il traduttore.
-   **Non usare un controllo subordinato, i valori in esso contenuti o l'etichetta di unità per creare una frase o una frase.** Tale progettazione non è localizzabile perché la struttura delle frasi varia in base alla lingua.

    **Non corretto:**

    ![Screenshot della casella di testo all'interno di un'etichetta di casella di controllo ](images/text-ui-image32.png)

    **Corretto:**

    ![Screenshot della casella di testo dopo l'etichetta di una casella di controllo ](images/text-ui-image33.png)

    Nell'esempio non corretto la casella di testo viene inserita all'interno dell'etichetta della casella di controllo.

-   Non rendere solo parte di una frase un collegamento, perché quando viene tradotto, il testo potrebbe non rimanere insieme. Il testo del collegamento deve quindi formare una frase completa da sola.
    -   **Eccezione:** I collegamenti di glossario possono essere inseriti inline come parte di una frase.

Per altre informazioni, vedere [go global developer center.](https://msdn.microsoft.com/goglobal/)

### <a name="title-bar-text"></a>Testo per la barra del titolo

-   Scegliere il testo della barra del titolo in base al tipo di finestra:
    -   **Finestre del programma incentrato sui documenti di primo livello:** Usare un formato "nome programma nome documento". I nomi dei documenti vengono visualizzati per primi per dare un aspetto incentrato sul documento.
    -   **Finestre di programma di primo livello non incentrate sui documenti:** Visualizzare solo il nome del programma.
    -   **Finestre di dialogo:** Consente di visualizzare il comando, la funzionalità o il programma da cui è stata visualizzata la finestra di dialogo. Non usare il titolo per spiegare lo scopo della finestra di dialogo che è lo scopo delle istruzioni principali. Per altre linee guida, vedere [Finestre di dialogo.](win-dialog-box.md)
    -   **Procedure guidate:** Visualizzare il nome della procedura guidata. Si noti che la parola "wizard" non deve essere inclusa nei nomi delle procedure guidate. Per altre linee guida, vedere [Procedure guidate.](win-wizards.md)
-   **Per le finestre dei programmi di primo livello, se la didascalia e l'icona della barra del titolo vengono visualizzate in primo piano nella parte superiore della finestra, è possibile nascondere la didascalia e l'icona della barra del titolo per evitare ridondanza.** Tuttavia, è comunque necessario impostare internamente un titolo appropriato per l'uso da parte di Windows.
-   **Per le finestre di dialogo, non includere le parole "dialog" o "progress" nei titoli.** Questi concetti sono impliciti e lasciare queste parole disattivate semplifica la scansione dei titoli per gli utenti.

### <a name="main-instructions"></a>Istruzioni principali

-   **Usare l'istruzione principale per spiegare in modo conciso le attività che gli utenti devono eseguire in una determinata finestra o pagina.** Le istruzioni principali di buona qualità comunicano l'obiettivo dell'utente anziché concentrarsi solo sulla manipolazione dell'interfaccia utente.
-   **Esprimere l'istruzione principale sotto forma di una direzione imperativa o di una domanda specifica.**

    **Non corretto:**

    ![Screenshot del nome del programma come istruzione principale ](images/text-ui-image34.png)

    In questo esempio l'istruzione main indica semplicemente il nome del programma. non invita in modo esplicito un corso di azione che l'utente deve eseguire.

    **Eccezioni:** I messaggi di errore, i messaggi di avviso e le conferme possono usare strutture di frase diverse nelle istruzioni principali.

-   **Usare verbi specifici quando possibile.** Verbi specifici (ad esempio: connessione, salvataggio, installazione) sono più significativi per gli utenti rispetto a quelli generici (ad esempio: configurare, gestire, impostare).
    -   Per le pagine del pannello di controllo e le pagine della procedura guidata, se non è possibile usare un verbo specifico, è preferibile omettere completamente il verbo.

        **Accettabile:**

        Immettere le impostazioni locali, l'area geografica e la lingua

        **Migliore:**

        Impostazioni locali, area geografica e lingua

    -   Per le finestre di dialogo, ad esempio messaggi di errore e avvisi, non omettere il verbo.

-   Non è obbligatorio usare il testo dell'istruzione principale se aggiungerlo sarebbe ridondante o ovvio solo dal contesto dell'interfaccia utente.

    ![Screenshot della finestra di dialogo Salva con nome ](images/text-ui-image35.png)

    In questo esempio il contesto dell'interfaccia utente è già molto chiaro. non è necessario aggiungere il testo dell'istruzione principale.

-   **Usare concisa una sola frase completa.** Si può trovare l'istruzione principale fino alle informazioni essenziali. Se è necessario spiegare altro, è consigliabile usare un'istruzione supplementare.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   **Non includere i periodi finali se l'istruzione è un'istruzione .** Se l'istruzione è una domanda, includere un punto interrogativo finale.
-   **Per i dialoghe di stato, usare** una frase gergo che spiega brevemente l'operazione in corso, terminando con i puntini di sospensione. Esempio: "Stampa delle immagini..."
-   **Suggerimento:** È possibile valutare un'istruzione principale immaginare ciò che si dice a un amico quando si spiega cosa fare con la finestra o la pagina. Se rispondere con l'istruzione principale sarebbe innaturale, poco utile o difficile, rielaborare l'istruzione.

Per altre informazioni, vedere la sezione "Istruzione principale" nelle linee guida specifiche per i componenti dell'interfaccia utente.

### <a name="supplemental-instructions"></a>Istruzioni supplementari

-   Quando necessario, **usare un'istruzione supplementare per presentare informazioni** aggiuntive utili per comprendere o usare la finestra o la pagina, ad esempio:
    -   Fornire il contesto per spiegare il motivo per cui la finestra viene visualizzata se è avviata dal programma o dal sistema.
    -   Informazioni idonee che consentono agli utenti di decidere come agire sull'istruzione principale.
    -   Definizione di terminologia importante.
-   **Non usare un'istruzione supplementare se non è necessaria.** Se è possibile farlo in modo conciso, è preferibile comunicare tutto con l'istruzione principale.
-   **Non ripetere l'istruzione principale con una formulazione leggermente diversa.** In alternativa, omettere l'istruzione supplementare se non è più necessario aggiungere.
-   Usare frasi complete e lettere maiuscole in stile frase.

### <a name="control-labels"></a>Etichette di controllo

-   **Etichettare ogni controllo o gruppo di controlli. Eccezioni:**
    -   Le caselle di testo e gli elenchi a discesa possono essere etichettati tramite prompt.
    -   I controlli di divulgazione progressiva sono in genere senza etichetta.
    -   **I controlli subordinati usano l'etichetta del controllo associato.** I controlli di selezione sono sempre controlli subordinati.
    -   **Omettere le etichette di controllo che rievalore l'istruzione principale.** In questo caso, l'istruzione principale accetta la chiave di accesso.

        **Accettabile:**

        ![Screenshot della casella di testo con istruzioni ed etichetta ](images/text-ui-image36.png)

        In questo esempio, l'etichetta della casella di testo è solo una riezione dell'istruzione principale.

        **Migliore:**

        ![Screenshot della casella di testo con solo istruzioni ](images/text-ui-image37.png)

        In questo esempio l'etichetta ridondante viene rimossa, quindi l'istruzione principale accetta la chiave di accesso.

-   Posizionamento delle etichette:
    -   I fumetto, le caselle di controllo, i pulsanti di comando, le caselle di gruppo, i collegamenti, le schede e i suggerimenti vengono etichettati direttamente dal controllo stesso.
    -   Gli elenchi a discesa, le caselle di riepilogo, le visualizzazioni elenco, gli indicatori di stato, i dispositivi di scorrimento, le caselle di testo e le visualizzazioni albero sono etichettati sopra, scaricati a sinistra o a sinistra.
    -   I controlli di divulgazione progressiva sono in genere senza etichetta. I pulsanti freccia di controllo sono etichettati a destra.
-   **Assegnare una chiave di accesso univoca per ogni controllo interattivo,** ad eccezione dei collegamenti. Per altre informazioni, vedere [Tastiera.](inter-keyboard.md)
-   **Tenere brevi le etichette.** Si noti, tuttavia, che l'aggiunta di una o due parole a un'etichetta può contribuire alla chiarezza e talvolta elimina la necessità di spiegazioni supplementari.
-   **Preferire etichette specifiche a quelle generiche.** Idealmente, gli utenti non devono leggere altro per comprendere l'etichetta.

    **Non corretto:**

    ![Screenshot del pulsante di comando OK ](images/text-ui-image38.png)

    **Corretto:**

    ![Screenshot del pulsante di comando Pubblica ](images/text-ui-image39.png)

    Nell'esempio corretto viene usata un'etichetta specifica per il pulsante di commit.

-   **Per gli elenchi di etichette,** ad esempio i pulsanti di opzione, usare la formulazione parallela e provare a mantenere la lunghezza per tutte le etichette.
-   **Per gli elenchi di etichette, concentrare il testo dell'etichetta sulle differenze tra le opzioni.** Se tutte le opzioni hanno lo stesso testo introduttivo, spostare il testo nell'etichetta del gruppo.

    **Non corretto:**

    ![Screenshot delle etichette con le prime frasi duplicate](images/text-ui-image40.png)

    **Corretto:**

    ![Screenshot della prima frase spostata nell'etichetta di gruppo](images/text-ui-image41.png)

    L'esempio corretto sposta la formulazione introduttiva identica all'etichetta, in modo che le due opzioni siano differenziate in modo più pulito.

-   **In generale, preferire la formulazione positiva.** Ad esempio, usare do invece di do not e notify invece di non notificare.
    -   **Eccezione:** L'etichetta della casella di controllo "Non visualizzare più questo messaggio" è ampiamente usata.
-   **Omettere verbi di istruzione che si applicano a tutti i controlli del tipo specificato.** È invece possibile concentrare le etichette sugli elementi univoci dei controlli. Ad esempio, non è necessario che gli utenti devono digitare in un controllo casella di testo o che gli utenti devono fare clic su un collegamento.

    **Non corretto:**

    ![Screenshot dell'etichetta: 'type your name' ](images/text-ui-image42.png)

    **Corretto:**

    ![Screenshot dell'etichetta: 'your name' ](images/text-ui-image43.png)

    Negli esempi non corretti, le etichette dei controlli hanno verbi di istruzione che si applicano a tutti i controlli del tipo.

-   In alcuni casi, possono essere utili le annotazioni tra parentesi seguenti per controllare le etichette:
    -   **Se un'opzione è facoltativa, è consigliabile aggiungere "(facoltativo)" all'etichetta.**
    -   **Se un'opzione è fortemente consigliata, aggiungere "(scelta consigliata)" all'etichetta.** In questo modo, l'impostazione è facoltativa, ma deve essere comunque impostata.
    -   **Se un'opzione è destinata solo agli utenti avanzati, è consigliabile aggiungere "(advanced)" all'etichetta.**
-   È possibile specificare unità (secondi, connessioni e così via) tra parentesi dopo l'etichetta.

    ![Screenshot dell'etichetta: dimensioni iniziali (mb) ](images/text-ui-image44.png)

    Questo esempio mostra che l'unità di misura è megabyte (MB).

Per altre informazioni, vedere la sezione "Testo" o "Etichette" nelle linee guida specifiche per i componenti dell'interfaccia utente.

### <a name="supplemental-explanations"></a>Spiegazioni supplementari

-   **Usare spiegazioni supplementari quando i controlli richiedono più informazioni di quelle che possono essere trasmesse dalla relativa etichetta.** Tuttavia, non usare una spiegazione supplementare se non è necessario, se è possibile farlo concisamente, comunicare tutto con l'etichetta del controllo. In genere, le spiegazioni supplementari vengono usate con i collegamenti di comando, i pulsanti di opzione e le caselle di controllo.
-   Quando necessario, **usare il grassetto nelle etichette del controllo per semplificare** l'analisi del testo in caso di spiegazioni supplementari.

    ![Screenshot della finestra di dialogo impostazioni di sicurezza ](images/text-ui-image45.png)

    In questo esempio le etichette dei pulsanti di opzione sono in grassetto per facilitarne l'analisi.

-   **L'aggiunta di una spiegazione supplementare a un controllo in un gruppo non significa che sia necessario fornire spiegazioni per tutti gli altri controlli nel gruppo.** Fornire le informazioni rilevanti nell'etichetta se è possibile e usare le spiegazioni solo quando necessario. Non avere spiegazioni supplementari che si limitano a rielimentare l'etichetta per la coerenza.

    ![Screenshot di tre pulsanti di opzione ](images/text-ui-image46.png)

    In questo esempio due controlli nel gruppo includono spiegazioni supplementari, ma il terzo no.

-   Se una spiegazione supplementare segue un collegamento di comando, scrivere il testo supplementare in seconda persona.

    **Esempio:** Collegamento comando: Creare le impostazioni di rete wireless e salvare in unità flash USB

    Spiegazione supplementare: verranno create impostazioni che è possibile trasferire al router con un'unità flash USB. Eseguire questa operazione solo se si dispone di un router wireless che supporta la configurazione dell'unità flash USB.

-   Usare frasi complete e la punteggiatura finale.

### <a name="commit-button-labels"></a>Etichette dei pulsanti di commit

La tabella seguente illustra le etichette dei pulsanti di commit più comuni e il relativo utilizzo.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Etichetta del pulsante</strong><br/></td>
<td><strong>Significato</strong><br/></td>
<td><strong>Quando usarla</strong><br/></td>
<td><strong>Chiave di accesso</strong><br/></td>
</tr>
<tr class="even">
<td><strong>OK</strong><br/></td>
<td><ul>
<li>Nelle finestre di dialogo: applicare le modifiche o eseguire il commit all'attività e chiudere la finestra.</li>
<li>Nelle finestre delle proprietà del proprietario: applicare le modifiche in sospeso (apportate dopo l'apertura della finestra o l'ultima applicazione) e chiudere la finestra.</li>
<li>Nelle finestre delle proprietà di proprietà: mantenere le modifiche, chiudere la finestra e applicare le modifiche quando vengono applicate le modifiche della finestra proprietaria.</li>
</ul></td>
<td><ul>
<li>Usare con finestre non specifiche delle attività, ad esempio le finestre delle proprietà.</li>
<li>Per le finestre usate per eseguire un'attività specifica, usare invece un'etichetta specifica che inizia con un verbo (ad esempio: Stampa).</li>
<li>Per le finestre in cui gli utenti non possono apportare modifiche, usare Chiudi.</li>
</ul></td>
<td>Immettere<br/></td>
</tr>
<tr class="odd">
<td><strong>Sì/No</strong><br/></td>
<td>Sì è la risposta affermativa a una domanda sì o no, mentre No è la risposta negativa.<br/></td>
<td><ul>
<li>Usare i pulsanti Sì e No solo per rispondere a domande sì o no. Non usare mai OK e Annulla per domande sì o no.</li>
<li>Preferisci risposte specifiche rispetto ai pulsanti Sì e No. Anche se non c'è niente di sbagliato nell'uso di Sì e No, risposte specifiche possono essere comprese più rapidamente, determinando un processo decisionale efficiente.</li>
<li>È tuttavia consigliabile usare le risposte Sì e No se la formulazione di risposte specifiche risulta lunga o difficile.</li>
<li>Non usare i pulsanti Sì e No se il significato della risposta No non è chiaro. In tal caso, usare risposte specifiche.</li>
<li>Sì e No devono essere sempre usati come coppia.</li>
</ul></td>
<td>Y e N<br/></td>
</tr>
<tr class="even">
<td><strong>Annulla</strong><br/></td>
<td><ul>
<li>Nelle finestre di dialogo: annullare tutte le modifiche o le operazioni in corso, ripristinare lo stato precedente (senza alcun effetto collaterale evidente) e chiudere la finestra.</li>
<li>Nelle finestre delle proprietà: rimuovere tutte le modifiche in sospeso (apportate dopo l'apertura della finestra o l'ultima applicazione) e chiudere la finestra.</li>
<li>Negli elementi del Pannello di controllo: rimuovere tutte le modifiche o il lavoro in corso, ripristinare lo stato precedente e tornare alla pagina dell'hub da cui è stata avviata l'attività. Se non è presente una pagina hub di questo tipo, chiudere invece la finestra dell'elemento del Pannello di controllo.</li>
</ul></td>
<td><ul>
<li>Usare quando tutte le modifiche o le azioni in sospeso possono essere rimosse ed eventuali effetti collaterali possono essere annullati.</li>
<li>Per le modifiche che non possono essere rimosse, usare Chiudi. Per le azioni in corso che possono essere arrestate, usare Arresta. Se inizialmente le modifiche o le azioni possono essere rimosse, è possibile usare Annulla inizialmente e quindi passare a Chiudi o Arresta quando non può essere annullata.</li>
</ul></td>
<td>ESC<br/></td>
</tr>
<tr class="odd">
<td><strong>Close</strong><br/></td>
<td>Chiudere la finestra. Eventuali modifiche o effetti collaterali non vengono eliminati.<br/></td>
<td><ul>
<li>Usare quando le modifiche o gli effetti collaterali non possono essere eliminati. Usare Chiudi invece di Annulla per le finestre primarie.</li>
<li>Usare per le finestre in cui gli utenti non possono apportare modifiche.</li>
</ul></td>
<td>Alt+F4, Ctrl+F4<br/></td>
</tr>
<tr class="even">
<td><strong>Stop</strong><br/></td>
<td>Arrestare un'attività attualmente in esecuzione e chiudere la finestra. Eventuali lavori in corso o effetti collaterali non vengono eliminati.<br/></td>
<td><ul>
<li>Usare quando il lavoro in corso e gli effetti collaterali non possono o non verranno eliminati, in genere con animazioni o barre di stato.</li>
</ul></td>
<td>ESC<br/></td>
</tr>
<tr class="odd">
<td><strong>Applica</strong><br/></td>
<td>Nelle finestre delle proprietà del proprietario: applicare le modifiche in sospeso apportate dopo l'apertura della finestra o l'ultima applicazione, ma lasciare aperta la finestra. In questo modo gli utenti possono valutare le modifiche prima di chiudere la finestra delle proprietà. Nelle finestre delle proprietà di proprietà: non usare .<br/></td>
<td><ul>
<li>Usare solo nelle finestre delle proprietà.</li>
<li>Specificare un pulsante Applica solo se nella finestra delle proprietà sono presenti impostazioni (almeno una) con effetti che gli utenti possono valutare in modo significativo. In genere, i pulsanti Applica vengono usati quando le impostazioni apportano modifiche visibili. Gli utenti devono essere in grado di applicare una modifica, valutarne la modifica e apportare altre modifiche in base a tale valutazione. In caso contrario, rimuovere il pulsante Applica anziché disabilitarlo.</li>
</ul></td>
<td>Una<br/></td>
</tr>
<tr class="even">
<td><strong>Avanti</strong><br/></td>
<td>Nelle procedure guidate e nelle attività in più passaggi: passare al passaggio successivo senza eseguire il commit dell'attività.<br/></td>
<td><ul>
<li>Usare solo nelle procedure guidate e nelle attività in più passaggi per passare al passaggio successivo senza impegno.</li>
<li>L'effetto di un pulsante Avanti può sempre essere annullato facendo clic su Indietro.</li>
</ul></td>
<td>N<br/></td>
</tr>
<tr class="odd">
<td><strong>Fine</strong><br/></td>
<td>Nelle procedure guidate e nelle attività in più passaggi: chiudere la finestra. Se l'attività non è ancora stata eseguita, eseguire l'attività. Se tale attività è già stata eseguita, le modifiche o gli effetti collaterali non vengono eliminati.<br/></td>
<td><ul>
<li>Usare solo nelle procedure guidate e nelle attività in più passaggi. Tuttavia, l'uso di Finish è sconsigliato perché in genere è disponibile un pulsante di commit migliore e più specifico:
<ul>
<li>Se facendo clic sul pulsante viene eseguito il commit nell'attività (in modo che l'attività non sia già stata eseguita), usare un'etichetta specifica che inizia con un verbo (ad esempio Print, Connect, Start) che rappresenta una risposta all'istruzione principale.</li>
<li>Se l'attività è già stata eseguita all'interno della procedura guidata, usare invece Chiudi.</li>
</ul></li>
<li>Tuttavia, è possibile usare Fine quando:
<ul>
<li>L'etichetta specifica è ancora generica, ad esempio Salva, Seleziona, Scegli o Ottieni.</li>
<li>L'attività comporta la modifica di un'impostazione o di una raccolta di impostazioni.</li>
</ul></li>
</ul></td>
<td>Immettere<br/></td>
</tr>
<tr class="even">
<td><strong>Completato</strong><br/></td>
<td>Non applicabile.<br/></td>
<td><ul>
<li>Non usare. Eseguito come comando non è grammaticalmente corretto.</li>
</ul></td>
<td>Non applicabile.<br/></td>
</tr>
</tbody>
</table>



 

