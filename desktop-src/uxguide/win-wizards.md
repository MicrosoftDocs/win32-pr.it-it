---
title: Procedure guidate
description: Nonostante questo nome straordinario e conciso, le procedure guidate non sono in realtà una forma speciale di interfaccia utente e hanno solo una particolare gamma di utilità.
ms.assetid: 122d6e65-92f0-4e8a-92f7-ecd7e90665c8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 31a9a0b4ed0c114dbdeadce7fe894bdd7da9cc099960f6ce2291e073ffdf3ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119029061"
---
# <a name="wizards"></a>Procedure guidate

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Nonostante questo nome straordinario e conciso, le procedure guidate non sono in realtà una forma speciale di interfaccia utente e hanno solo una particolare gamma di utilità.

Le procedure guidate vengono usate per eseguire attività in più passaggi.

![Screenshot che mostra la procedura guidata "Aggiungi stampante" con "Quale tipo di stampante si vuole installare?". Prompt dei comandi.](images/win-wizards-image1.png)

![Screenshot che mostra la procedura guidata "Aggiungi stampante" durante la ricerca delle stampanti disponibili.](images/win-wizards-image2.png)

![Screenshot dell'Aggiunta guidata stampante ](images/win-wizards-image3.png)

Più passaggi di una procedura guidata vengono presentati come una sequenza di pagine.

Le procedure guidate includono in genere i tipi di pagine seguenti:

-   Le pagine di scelta vengono usate per raccogliere informazioni e consentire agli utenti di effettuare scelte.
-   La pagina Commit consente di eseguire un'azione che non può essere annullata facendo clic su Indietro o Annulla.
-   La pagina Stato viene usata per visualizzare lo stato di avanzamento di un'operazione di lunga durata.

La progettazione moderna della procedura guidata consente di migliorare l'efficienza, rendendo facoltativa [](glossary.md) la [](glossary.md) pagina Stato per operazioni più brevi e spesso con la tradizionale pagina di benvenuto e la pagina di benvenuto all'inizio e alla fine.

Tutte le pagine della procedura guidata hanno questi componenti:

-   Barra del titolo per identificare il nome della procedura guidata, con un pulsante Indietro nell'angolo superiore sinistro e un pulsante Chiudi con i pulsanti facoltativi Riduci a icona/Ingrandisci e Ripristina. Si noti che la barra del titolo include anche un'icona per identificarla sulla barra delle applicazioni.
-   Istruzione principale per spiegare l'obiettivo dell'utente con la pagina.
-   Area di contenuto con testo facoltativo ed eventualmente altri controlli.
-   Un'area di comando con almeno un pulsante di commit per eseguire il commit nell'attività o procedere al passaggio successivo.

Anche se una procedura guidata include più passaggi, tutti questi passaggi devono essere aggiunti a una singola attività, dal punto di vista dell'utente. Questo è il principio di progettazione della procedura guidata fondamentale di "una procedura guidata, una sola attività".

In questo articolo, quindi, un'attività è la funzione di base di una procedura guidata (ad esempio, l'attività di un'installazione guidata è l'installazione di un programma). Le sotto-attività sono aspetti dell'attività più grande(ad esempio, un'attività secondaria di un'installazione guidata potrebbe essere la configurazione del programma da installare). Infine, ogni pagina della procedura guidata viene considerata un passaggio in una determinata sotto-attività o attività (ad esempio, potrebbero essere necessari due o tre passaggi per la configurazione del programma).

**Nota:** Le linee guida relative [all'installazione,](exper-setup.md) [alle finestre di](win-dialog-box.md)dialogo e agli barre [di](progress-bars.md) stato sono presentate in articoli separati.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Una procedura guidata può essere usata per qualsiasi attività che richiede più passaggi di input. Tuttavia, le procedure guidate efficaci hanno requisiti aggiuntivi:

-   **La procedura guidata esegue una singola attività atomica?** Non usare interazioni che non sono singole attività (un intero programma non deve mai essere una procedura guidata a meno che non esegua una singola attività). Non usare procedure guidate per combinare attività indipendenti o passaggi in gran parte non correlati.
-   **È possibile ridurre il numero di domande necessarie? Esistono impostazioni predefinite accettabili che funzionano bene per la maggior parte dei casi o possono essere modificate in base alle esigenze in un secondo momento? Di conseguenza, è possibile ridurre il numero di pagine?** In tal caso, provare a semplificare l'attività in modo che possa essere presentata in una singola pagina (ad esempio una finestra di dialogo) o eliminare completamente la necessità di input (consentendo l'esecuzione diretta dell'attività).
-   **Le domande necessarie devono essere fornite in sequenza? Esistono diverse domande probabili, ma facoltative?** In tal caso, prendere in considerazione una finestra di dialogo o una finestra di dialogo a schede.

    **Corretto:**

    ![Screenshot della finestra di dialogo opzioni di stampa ](images/win-wizards-image4.png)

    La finestra di PowerPoint opzioni di stampa di Microsoft PowerPoint contiene molte opzioni di input utente, pertanto è possibile presentarle in una procedura guidata. Tuttavia, non è necessario fornirli in sequenza, quindi una finestra di dialogo è una scelta migliore.

Le procedure guidate sono una forma relativamente pesante di interfaccia utente. Se è disponibile una soluzione adatta e più leggera, è possibile usarla.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="overuse-of-wizards"></a>Uso eccessivo delle procedure guidate

In genere, le procedure guidate differivano dall'interfaccia utente normale perché erano progettate per aiutare gli utenti a eseguire attività particolarmente complesse (con passaggi che si trovano in posizioni diverse) e spesso avevano un'intelligenza incorporata per consentire agli utenti di avere successo. Attualmente, tutta l'interfaccia utente deve essere progettata per semplificare il più possibile le attività, quindi non è necessaria un'interfaccia utente speciale solo a questo scopo.

Tuttavia, la persistenza persiste nel fatto che le procedure guidate sono un'interfaccia utente speciale, in gran parte perché sono definite "procedure guidate" (molto più creative rispetto, ad esempio, alle "finestre di dialogo" e alle "finestre delle proprietà"). È invece consigliabile considerarle attività in più passaggi e non attirare particolare attenzione a tale fatto.

Prima di creare una procedura guidata, valutare se gli utenti devono effettivamente essere interrotti dal flusso principale del programma. Potrebbe essere disponibile una soluzione contestuale più leggera, inline, che in definitiva sarà più utile ed efficiente per gli utenti. Ad esempio, una funzionalità progettata in modo erto in un programma non richiede una procedura guidata per spiegarla e semplificarla; garantisce la riprogettazione della funzionalità stessa. Una procedura guidata non deve essere usata come supporto a banda per risolvere un problema più semplice con il programma.

### <a name="wizards-do-have-appropriate-functions"></a>Le procedure guidate hanno funzioni appropriate

Le procedure guidate sono una delle chiavi per semplificare l'esperienza utente. Consentono di eseguire un'operazione complessa, ad esempio la configurazione di un programma, e di suddividerla in una serie di semplici passaggi. In ogni punto del processo è possibile fornire una spiegazione degli elementi necessari e visualizzare i controlli che consentono all'utente di effettuare selezioni e immettere testo.

Alcuni tipi di attività in più passaggi si prestano al modulo della procedura guidata. Ad esempio, in Windows, diverse procedure guidate prevedono funzioni di connettività (a Internet o alla rete aziendale o a periferiche come stampanti e fax).

![Screenshot della connessione guidata ](images/win-wizards-image5.png)

La connessione a una rete è un'attività tipica in Windows appropriata per una procedura guidata.

In questo caso la funzione della procedura guidata è di mediare tra qualcosa di noto e stabile (il sistema operativo predefinito) e qualcosa di sconosciuto e variabile (disposizioni di connettività con una società telefonica o un provider di servizi Internet). La complessità degli ecosistemi di elaborazione è sufficientemente significativa ora che è davvero utile usare procedure guidate per ridurre tale complessità.

Altri tipi di attività che funzionano così come le procedure guidate di Windows includono funzionalità di fascia alta (ad esempio il riconoscimento vocale e della grafia) e esperienze multimediali avanzate (ad esempio la configurazione di opzioni per la creazione e la pubblicazione di film). Le procedure guidate possono essere distribuite anche per attività in più passaggi di base, ad esempio la risoluzione dei problemi. In breve, se è probabile che utenti diversi vogliano sperimentare il programma in modi molto diversi, ciò può indicare la necessità di una procedura guidata e della relativa capacità per più punti di input utente.

Per il programma, è opportuno un po' di tempo di progettazione in anticipo per determinare quale funzione viene utilizzata dalla procedura guidata e se tale funzione aumenta effettivamente fino al livello di distribuzione di una procedura guidata.

### <a name="wizard-length"></a>Lunghezza procedura guidata

Le domande di progettazione sorgono naturalmente in base al numero e all'organizzazione di pagine e opzioni. Esempio:

-   Esiste un numero ottimale di pagine per una procedura guidata? O almeno un intervallo auspicabile?
-   La procedura guidata deve essere concisa e semplificata, in modo che gli utenti possano completarla il più rapidamente possibile?
-   Devono essere presenti più pagine che richiedono meno scelte? O meno pagine con maggiore complessità? Quale progettazione è considerata più utilizzabile?
-   È possibile progettare esperienze di procedura guidata più veloci applicando convenzioni dell'interfaccia utente, ad esempio le pagine a schede?

Microsoft consigliava che le procedure guidate di tre o meno pagine siano progettate come semplici procedure guidate e quelle di quattro o più pagine usano una progettazione avanzata della procedura guidata (vedere le linee guida sull'esperienza utente di [Windows](/previous-versions/ms997609(v=msdn.10)) del 1999). Gli standard di progettazione delle procedure guidate correnti, tuttavia, sono una delle differenze principali tra i moduli semplici e avanzati (l'uso delle pagine Di benvenuto e Congratulazioni), quindi queste categorie ora sembrano insufficienti e il numero di pagine che determinano la scelta della progettazione sembra arbitrario.

La procedura guidata deve essere lunga o breve come richiesto dall'attività. non sono presenti linee guida fisse per la lunghezza. Una procedura guidata di una pagina deve essere effettivamente presentata come finestra di dialogo, quindi due pagine sono probabilmente la forma più condensata possibile per una procedura guidata.

**Corretto:**

![Screenshot della finestra di dialogo crea disco ](images/win-wizards-image6.png)

Questa attività ha così poche opzioni che presentarla come procedura guidata sarebbe uno spreco. Una finestra di dialogo è il modulo appropriato per questa interfaccia utente.

All'altra estremità dello spettro, se si dispone di una procedura guidata che include più punti decisionali e rami e causa spesso la perdita di traccia del percorso di navigazione da parte degli utenti, è stato superato un limite pratico e si dovrebbe ridurre la lunghezza della procedura guidata. In alternativa, è possibile suddividere la procedura guidata in diverse attività distinte.

Quando si determina la lunghezza più appropriata per la procedura guidata, prestare particolare attenzione agli utenti di destinazione. I programmi per gli utenti finali, ad esempio gli utenti privati e gli impiegati, tendono a usare procedure guidate per nascondere la complessità; Le procedure guidate sono il più brevi possibile, con una progettazione semplice e pulita della pagina e valori predefiniti pre-selezionati per il maggior numero possibile di opzioni. Al contrario, le procedure guidate server o i programmi destinati ai professionisti IT tendono a essere più lunghi e complessi. Questo gruppo di utenti di destinazione ha una tolleranza molto più elevata per prendere decisioni di configurazione e può diventare sospetto se è nascosta una complessità troppo elevata.

Se una procedura guidata per natura semplifica un'attività complessa, è consigliabile eseguire questa operazione in modo relativamente minimo per un pubblico tecnicamente sofisticato e relativamente aggressivo per una base utenti inesatta.

**Corretto:**

![Screenshot della procedura guidata lingue di visualizzazione ](images/win-wizards-image7.png)

Questa pagina della procedura guidata è ben progettata per gli utenti finali perché riduce un soggetto potenzialmente complesso a una semplice scelta binaria logica: installazione o disinstallazione.

**Corretto:**

![Screenshot che mostra la pagina "Selezione funzionalità" SQL Server'installazione guidata.](images/win-wizards-image8.png)

Nell'installazione guidata di Microsoft SQL Server 2008, la progettazione delle pagine è più attiva e le numerose scelte richiedono più attenzione, ma i destinatari sono gli amministratori di database che si aspettano un controllo stretto della selezione delle funzionalità.

Infine, prestare attenzione alla frequenza con cui potrebbe essere eseguita l'attività specifica. Un'attività poco frequente può distribuire una procedura guidata più lunga, mentre le attività frequenti dovrebbero sicuramente favorire la brevità.

### <a name="branching"></a>Diramazione

Per procedure guidate più lunghe, potrebbe essere necessario creare rami del flusso di attività in cui la sequenza di pagine può differire in base all'input dell'utente fornito "upstream". La diramazione è intrinsecamente dislocata per gli utenti, quindi è necessario progettare l'esperienza utente per comunicare la stabilità. È consigliabile non più di due punti decisionali che causeranno la diramazione nell'intera procedura guidata e non più di un ramo annidato all'interno di un singolo ramo.

Per linee guida sulla creazione di un'esperienza utente stabile all'interno di una creazione guidata di rami, vedere [Branching](#branching) nella sezione Linee guida di questo articolo.

### <a name="providing-a-navigation-guide"></a>Fornire una guida di navigazione

Le guide di spostamento possono essere utili quando sono presenti molti passaggi nell'attività e gli utenti potrebbero perdere il proprio posto nella sequenza o semplicemente voler sapere quanto tempo sarà necessario per il completamento.

Le guide di spostamento vengono spesso visualizzate come elenco di pagine o sezioni della procedura guidata, con un aspetto simile a un sommario, in una colonna o in un riquadro sul lato sinistro di ogni pagina. Anche se l'elenco persiste in tutta la procedura guidata (lo stesso elenco di pagine viene visualizzato in ogni pagina), esistono alcuni mezzi visivi per indicare dove l'utente si trova attualmente nella sequenza (ad esempio, usando il grassetto per distinguere la pagina o la sezione attiva).

Le guide di navigazione possono essere sequenziali o non sequenziali. Il tipo sequenziale presenta le pagine precedenti insieme alle pagine future note. È possibile presentare il futuro in termini di passaggi anziché di pagine se i passaggi sono noti e le pagine dipendono. È quindi possibile popolare le pagine in modo dinamico non appena diventano note. Poiché la sequenza di navigazione è fissa, la guida di navigazione non è interattiva.

Le guide di navigazione non sequenziali sono interattive, quindi gli utenti possono rivedere direttamente le pagine visualizzate in precedenza. Possono anche ignorare la sequenza di navigazione per le pagine progettate per essere facoltative. Le pagine facoltative devono avere valori predefiniti accettabili nella maggior parte dei casi. Con questo tipo di guida:

-   Le pagine visualizzate in precedenza possono sempre essere visualizzate direttamente.
-   Le pagine future potrebbero non essere visualizzate se hanno prerequisiti.
-   Le pagine che possono essere visitate devono essere visibilmente distinte da quelle che non possono essere (ad esempio usando collegamenti attivi o disabilitati), insieme alle pagine obbligatorie o facoltative.

Gli utenti possono confondersi sul significato della pulsante Indietro in questo scenario. Se si fa clic su Indietro, si viene alla pagina o alla sezione precedente nella guida di spostamento o all'ultima pagina o sezione visualizzata? Poiché Windows procedure guidate posizionano ora il pulsante Indietro nell'angolo superiore sinistro delle pagine della procedura guidata, anziché nell'angolo inferiore destro con gli altri pulsanti di commit, gli utenti possono pensare alla funzionalità Indietro come avviene sul Web. La soluzione migliore consiste quindi nell'assegnare al pulsante Indietro il significato della navigazione Web (facendo clic su Indietro si dovrebbe visualizzare l'ultima pagina o sezione) e usare la guida di navigazione della procedura guidata per lo spostamento sequenziale.

### <a name="page-integrity"></a>Integrità della pagina

La progettazione guidata implica non solo decisioni relative all'intero flusso di attività, ad esempio come gestire la navigazione e l'esperienza di creazione di rami, ma anche quelle relative alle singole pagine che costituiscono la procedura guidata. **Il principio più importante per la progettazione di buone pagine della procedura guidata è quello dell'integrità: il contenuto di una pagina deve appartenere insieme.**

Le pagine della procedura guidata sono notevolmente più utilizzabili se ognuna si blocca concettualmente, trattando solo un aspetto dell'attività complessiva. [L'istruzione principale](glossary.md) è il mezzo principale per ottenere questo risultato. Identificare chiaramente l'obiettivo o lo scopo della pagina per gli utenti. [Istruzioni supplementari](glossary.md)e tutti i controlli nella pagina, tutti riguardano direttamente l'istruzione principale. Anche se le pagine della procedura guidata devono presentare agli utenti opzioni per le quali è necessaria una certa attenzione, questo sforzo non sembra funzionare perché è strettamente incentrato sull'integrità della pagina stessa.

Sfortunatamente, i progettisti di procedure guidate spesso confondeno il rapido clic del pulsante Avanti degli utenti come prova dell'usabilità, della semplicità e dell'integrità delle pagine. L'esperienza finale della procedura guidata non è Avanti, Avanti, Avanti, Fine. Anche se tale esperienza suggerisce che le impostazioni predefinite sono state scelte in modo ottimale, suggerisce anche che la procedura guidata non era realmente necessaria perché tutte le scelte sono facoltative.

In termini di oggetti visivi e testo, questi elementi sono essenziali. Non è necessario aggregare più sotto-attività in una singola pagina (la "procedura guidata burrito") o ricorrere alle schede per presentare requisiti di input complessi. Una singola pagina deve coprire una singola sotto-attività dell'attività complessiva della procedura guidata.

**Non corretto:**

![Screenshot dell'installazione guidata di SQL Server ](images/win-wizards-image9.png)

Con tre schede di input utente piuttosto denso necessario, questa pagina della procedura guidata sta tentando di ottenere un risultato troppo grande.

Nella maggior parte dei casi, mantenere le dimensioni di ogni pagina in tutta la procedura guidata per favorire un aspetto coerente. Sebbene Windows procedure guidate consentano pagine ridimensionabili in modo che le dimensioni di una pagina corrispondano alla quantità di contenuto, solo pochi usano questa opzione.

Infine, mantenere gli elementi strutturali di ogni pagina della procedura guidata tramite la sequenza. Ad esempio, non spostare l'pulsante Indietro dall'angolo superiore sinistro verso il basso nell'area dei pulsanti di commit per una o due pagine. Questo livello di coerenza del layout consente agli utenti di essere stabili all'interno della procedura guidata. Si pensi a questo come una linea di base per l'integrità visiva di una pagina.

### <a name="finding-the-right-level-of-communication"></a>Individuazione del livello di comunicazione giusto

Gli utenti hanno una tolleranza bassa per la lettura di grandi blocchi di testo sullo schermo e anche meno all'interno di una superficie dell'interfaccia utente il cui scopo rapido è quello di spostarsi in modo rapido attraverso un'attività.

Le procedure guidate hanno la tendenza a comunicare in modo over. Occupano molto spazio sullo schermo, il che sembra incoraggiare un'unità a riempire lo spazio. È come una variante di Legge di Parkinson: il testo dell'interfaccia utente si espanderà per riempire lo spazio disponibile.

Un responsabile in questo eccesso è la ridondanza. A causa dei modelli usati nella progettazione iniziale della procedura guidata, la stessa lingua potrebbe essere visualizzata in più posizioni in una pagina, ad esempio nella barra del titolo, nelle intestazioni, nel corpo del testo, nelle etichette dei controlli e così via.

Vale la pena assumere un editor professionista per eliminare il testo della procedura guidata senza errori. Eliminare le domande e le opzioni non necessarie nelle singole pagine ed eliminare intere pagine dalla procedura guidata nel suo complesso (ad esempio, le pagine di benvenuto e di congratulazioni tradizionali). Arrivare direttamente al punto della pagina con un'istruzione principale scritta in modo conciso, usando il linguaggio che il pubblico di destinazione usa per descrivere l'attività, non il gergo della tecnologia o della funzionalità che l'utente o il team usa internamente. Questo approccio incentrato sull'utente è fondamentale per migliorare la comunicazione delle procedure guidate del programma.

Prestare particolare attenzione al tono della procedura guidata: a volte le impressioni più durevoli del programma sono il risultato non di ciò che si dice, ma di come si dice. Nelle procedure guidate, gli utenti hanno familiarità con un tono descrittivo e conversazionale, con l'uso del pronome di seconda persona ("tu") quando il programma richiede input. Per altre linee guida, vedere [Stile e tono.](text-style-tone.md)

La riduzione del numero di parole nella pagina della procedura guidata è in genere encomiabile, ma prestare attenzione a non andare troppo lontano. Se l'attività è importante e garantisce una procedura guidata, gli utenti apprezzano la presenza di informazioni sufficienti per effettuare scelte oculatiche. L'esempio seguente illustra come è possibile condensare il testo della procedura guidata senza sacrificare il significato.

**Prima:**

![Screenshot della procedura guidata cleartype, bozza ](images/win-wizards-image10.png)

**Dopo:**

![Screenshot della procedura guidata cleartype, modificata ](images/win-wizards-image11.png)

La versione modificata di questa pagina della procedura guidata fornisce un'istruzione principale orientata alle attività, rimuove il paragrafo esplicativo non necessario sotto l'istruzione principale e modifica l'etichetta della casella di controllo per chiarire lo scopo della casella di controllo.

**Se si eservino solo tre operazioni...**

1. Eseguire il mapping dell'attività che si sta tentando di eseguire con l'interfaccia utente appropriata per eseguire il processo. Non è sufficiente impostare come impostazione predefinita una procedura guidata quando si pensa di dover raccogliere molto input dagli utenti.

2. Considerare attentamente la lunghezza e la struttura della procedura guidata; preferire procedure guidate brevi e non diramazione per mantenere l'esperienza il più semplice possibile, in modo che gli utenti possano tornare alla propria attività principale o all'interesse per il programma.

3. Verificare l'integrità di ogni pagina della procedura guidata: il contenuto di una pagina deve chiaramente appartenere insieme.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Considerare prima di tutto alternative leggere, ad esempio finestre di dialogo, riquadri attività o singole pagine.** Non è necessario usare le procedure guidate. È possibile fornire informazioni e assistenza utili in qualsiasi interfaccia utente.
-   **Usare le procedure guidate per le attività in più passaggi.** Usare finestre di dialogo a più pagine per attività a passaggio singolo con commenti e suggerimenti. Per altre linee guida, vedere [Finestre di dialogo](win-dialog-box.md).

    **Corretto:**

    ![Screenshot della finestra di dialogo diagnostica ](images/win-wizards-image12.png)

    ![Screenshot del feedback della finestra di dialogo di diagnostica ](images/win-wizards-image13.png)

    In questo esempio, Windows diagnostica di rete è costituito da pagine di stato e risultati. Poiché l'attività è solo un singolo passaggio, non richiede i pulsanti di spostamento necessari agli utenti in una procedura guidata. Viene presentato in modo efficace come finestra di dialogo a più pagine.

### <a name="window-size"></a>Dimensioni finestra

-   **Scegliere le dimensioni della finestra in grado di visualizzare tutte le pagine della procedura guidata senza scorrimento verticale o orizzontale.** Anche se i controlli nella pagina possono richiedere lo scorrimento, le pagine della procedura guidata non devono.
-   **Ridimensionare le finestre sufficientemente grandi da eseguire le attività in modo semplice.** Il layout di pagina non deve essere troppo piccolo o richiedere agli utenti di scorrere o ridimensionare in modo eccessivo.
-   **Ma non rendere le finestre eccessivamente grandi.** Le finestre più grandi rendono l'attività più complessa e richiedono uno spostamento aggiuntivo per l'interazione.
-   **Usare finestre ridimensionabili per una procedura guidata che può trarre vantaggio da più spazio sullo schermo, ma non lo richiede.** Assegnare una dimensione minima appropriata. Le finestre ridimensionabili sono utili quando le pagine richiedono l'interazione con contenuto ridimensionabile, ad esempio visualizzazioni elenco di grandi dimensioni.

    **Corretto:**

    ![Screenshot della configurazione di Visual Studio, elenco parziale ](images/win-wizards-image14.png)

    **Migliore:**

    ![Screenshot della configurazione di Visual Studio, elenco completo ](images/win-wizards-image15.png)

    In questo esempio il ridimensionamento della finestra consente agli utenti di visualizzare l'elenco completo.

-   **Prendere in considerazione l'uso di procedure guidate con dimensioni dinamica le cui dimensioni della pagina cambiano in base alle esigenze per il contenuto.** Questa operazione consente a una procedura guidata di supportare i layout di pagina con un'ampia gamma di contenuto.
-   **Preferire il ridimensionamento statico rispetto a dinamico se gli utenti possono percepire le modifiche come una mancanza di stabilità nell'esperienza della procedura guidata.** La stabilità visiva spesso è un'alternativa alla sistemazione del contenuto. La maggior parte delle procedure guidate deve adottare dimensioni di finestra statiche standard, con ridimensionamento dinamico riservato per casi speciali.

### <a name="wizard-length"></a>Lunghezza procedura guidata

-   **Rendere la procedura guidata più concisa e semplificata possibile.** Eliminare le opzioni e le domande non necessarie e usare impostazioni predefinite intelligenti per ridurre il numero di pagine necessarie per l'input dell'utente.
    -   **Eccezione:** I professionisti IT e altri utenti tecnici hanno una tolleranza più elevata per procedure guidate più lunghe e requisiti di input dettagliati.
-   **Impostare la procedura guidata su un minimo di due pagine.** Una procedura guidata di una pagina deve essere riprogettata come finestra di dialogo.
-   **Non ridurre il numero di pagine della procedura guidata semplicemente aumentando la complessità di ogni pagina.** Ad esempio, una pagina della procedura guidata che include tre schede che richiedono l'input dell'utente deve essere riprogettata come tre pagine separate.
-   **Non aumentare il numero di pagine della procedura guidata rendendo ogni pagina così semplice che gli utenti fanno clic senza disatto su Avanti per l'intera sequenza.** Si tratta di un comune difetto di progettazione della procedura guidata. Se una pagina della procedura guidata non richiede almeno un certo grado di riflessione, probabilmente non deve essere nella procedura guidata.

### <a name="branching"></a>Diramazione

-   **Preferire la progettazione guidata senza rami rispetto alla creazione di rami.** Le procedure guidate senza diramazione tendono a essere più semplici, brevi e facili da esplorare. Le procedure guidate per la creazione di rami rendono più difficile per gli utenti determinare il numero di passaggi nell'attività e la posizione in cui si trova nella sequenza.
-   **Se è necessario creare un ramo, aiutare gli utenti a orientarsi usando una delle tecniche seguenti:**
    -   **Enumerare le pagine.** Una tecnica comune consiste nell'indicare la posizione dell'utente nella sequenza in ogni pagina, ad esempio con la frase Passaggio X di Y. Assicurarsi che l'endpoint (Y) sia stabile. Se cambia valore, ciò compromette l'attendibilità degli utenti.
    -   **Includere la nozione di passaggi secondari** ,ad esempio passaggio 2a di 6.
    -   **Rendere i passaggi indipendenti dalle pagine, in cui ogni passaggio può includere più pagine.** Ad esempio, un servizio di viaggi potrebbe impiegare un'organizzazione guidata basata su convenzioni di e-commerce ben stabilite per il settore.

        **Corretto:**

        ![Screenshot dell'organizzazione della procedura guidata basata su passaggi ](images/win-wizards-image16.png)

        Le etichette logiche possono fornire un orientamento adeguato per gli utenti di una creazione guidata di rami.

    -   **Considerare i passaggi facoltativi come persistenti nella sequenza di enumerazione.** Ad esempio, se un ramo sta semplicemente ignorando alcuni passaggi facoltativi, è sufficiente ignorare anche i passaggi nei commenti e suggerimenti, anziché rinumerare. Pertanto, se un utente effettua una scelta a pagina 2 che rende le pagine 3 e 4 facoltative, visualizzare i passaggi 1, 2, 5 e 6 di 6. Non rinumerare i passaggi 5 e 6.
    -   **Se la procedura guidata usa un singolo ramo e il ramo si verifica all'inizio dell'attività, avviare la sequenza in quel punto e quindi usare semplicemente l'approccio di non diramazione.** Ciò significa che, a partire dal punto del ramo, lo stato di avanzamento in sequenza fino alla fine del ramo.

-   **Se è necessario creare un ramo, limitare il numero di rami a uno o due all'interno di una singola procedura guidata.** Non includere mai più di un ramo all'interno di un ramo (un ramo "annidato").

### <a name="commit-buttons"></a>Pulsanti di commit

-   **Quando gli utenti emettono** un'attività, usare un pulsante di commit che rappresenta una risposta specifica all'istruzione principale, ad esempio Stampa, Connessione o Avvia. Non usare etichette generiche come Next (che non implica impegno) o Finish (che non è specifico) per il commit di un'attività. Le etichette su questi pulsanti di commit dovrebbero avere senso da soli. Avviare sempre le etichette dei pulsanti di commit con un verbo. **Eccezioni:**
    -   Usare Fine quando le risposte specifiche sono ancora generiche, ad esempio Salva, Seleziona, Scegli o Ottieni.
    -   Usare Fine per modificare un'impostazione specifica o una raccolta di impostazioni.
-   **Una singola procedura guidata può avere più punti di commit, ma è preferibile un singolo punto.**
-   **Se necessario, è possibile rinominare o nascondere i pulsanti di commit in una pagina.** Questa flessibilità è uno dei vantaggi della nuova progettazione guidata Windows che non era disponibile nelle procedure guidate precedenti. Si noti che nascondere un pulsante di commit è diverso dalla disabilitazione.
-   **Evitare di disabilitare un pulsante di commit positivo.** In caso contrario, gli utenti devono dedurre perché i pulsanti di commit sono disabilitati. È meglio lasciare abilitati i pulsanti di commit e fornire un messaggio di errore utile ogni volta che si verifica un problema. La disabilitazione del pulsante è accettabile solo se il motivo è ovvio e non ambiguo.
-   **Non confondere i pulsanti di navigazione (Avanti e Indietro) con i pulsanti di commit.** Avanti significa andare avanti nella procedura guidata senza impegno; Tornare dovrebbe essere sempre disponibile nella pagina successiva e fare clic su Indietro per annullare l'effetto dell'ultimo pulsante Avanti. Se ciò non è possibile, gli utenti stanno prendendo un impegno e questo viene indicato tramite un'etichetta specifica sul pulsante commit. Per altre linee guida sui pulsanti Avanti e Indietro, vedere [Navigazione.](#providing-a-navigation-guide)

### <a name="cancel-buttons"></a>Pulsanti Annulla

-   **Non chiedere agli utenti di confermare se intendono effettivamente annullare.** Questa operazione può essere fastidiosa. **Eccezioni:**
    -   L'azione ha conseguenze significative e, se non è corretta, non è facilmente risolvibile.
    -   L'azione può comportare una perdita significativa del tempo o dell'impegno dell'utente.
    -   L'azione è chiaramente incoerente con altre azioni.
-   **Consentire agli utenti di riavviare le procedure guidate nel caso in cui siano state annullate per errore.**
-   **Non disabilitare il pulsante Annulla. Eccezioni:**
    -   Se l'annullamento è dannoso, ciò potrebbe verificarsi quando si esegue un'attività nelle procedure guidate indipendenti.
    -   Se l'annullamento è impossibile, ciò potrebbe verificarsi quando la procedura guidata non ha il controllo su tutti i passaggi.

### <a name="close-buttons"></a>Pulsanti di chiusura

-   **Usare Chiudi per le Follow-Up e Di completamento.** Non usare Annulla, perché la chiusura della finestra non abbandonerà le modifiche o le azioni eseguite a questo punto. Non usare Done, perché non è un verbo imperativo.
-   **Dopo l'esecuzione dell'attività, Cancel dovrebbe diventare Close (per le procedure guidate indipendenti).** L'effetto di Close è semplicemente chiudere la finestra.

### <a name="other-controls"></a>Altri controlli

-   **Usare i collegamenti ai comandi solo per le scelte, non per gli impegni.** I pulsanti di commit specifici indicano un impegno molto migliore rispetto ai collegamenti di comando in una procedura guidata.
-   **Quando si usano collegamenti di comando, nascondere il pulsante Avanti, ma lasciare il pulsante Annulla.**

### <a name="using-pages-vs-dialog-boxes-or-inline-ui"></a>Uso delle pagine (rispetto alle finestre di dialogo o all'interfaccia utente inline)

-   **In generale, preferire le pagine alle finestre di dialogo.** Gli utenti prevedono che le procedure guidate siano basate su pagina.
-   **Usare le finestre di dialogo per completare le pagine, ad** esempio con i selettori di oggetti e i browser.
-   **Usare le finestre di dialogo per fornire messaggi di errore che si applicano all'intera pagina e risultare dalla selezione di un pulsante di commit.**
-   **Usare la presentazione inline per comportamenti dinamici semplici, ad** esempio la divulgazione progressiva e l'interfaccia utente contestuale.
-   **Usare la presentazione inline per i messaggi di errore che si applicano a controlli specifici.**

### <a name="wizard-pages"></a>Pagine della procedura guidata

-   **Concentrarsi sul processo decisionale efficiente.** Ridurre il numero di pagine per concentrarsi sulle informazioni di base. Consolidare le pagine correlate e portare le pagine facoltative fuori dal flusso principale. Fare clic su Avanti completamente tramite la procedura guidata può sembrare una buona esperienza all'inizio, ma se gli utenti non devono mai modificare le impostazioni predefinite, è probabile che le pagine non siano necessarie.
-   **Progettare ogni pagina in modo che abbia un unico scopo e coerenza visiva.** Per altre informazioni, vedere [Integrità delle pagine](#page-integrity).
-   **Non usare le pagine di benvenuto: rendere la prima pagina funzionante quando possibile.** Usare una pagina Attività iniziali facoltativa solo quando:

    -   La procedura guidata include i prerequisiti necessari per completare correttamente la procedura guidata.
    -   Gli utenti potrebbero non comprendere lo scopo della procedura guidata in base alla prima pagina Scelta e non c'è spazio per ulteriori spiegazioni.
    -   L'istruzione principale per Attività iniziali pagine è "Prima di iniziare:".

    **Non corretto:**

    ![Screenshot della pagina iniziale dell'installazione di mappoint ](images/win-wizards-image17.png)

-   Le procedure guidate moderne optano per le prime pagine funzionali. Qui non è possibile fare altro che fare clic su Avanti. Perché forzare gli utenti a pagare questa imposta sui token per il tempo prezioso?
-   **Nelle pagine in cui agli utenti viene richiesto di effettuare scelte, ottimizzare per i casi più probabili.** Questi tipi di pagine devono presentare scelte effettive, non solo istruzioni.
    -   Se non si usa una pagina Attività iniziali, spiegare lo scopo della procedura guidata nella parte superiore della prima pagina di scelte.
-   **Usare le pagine Commit per chiarire quando gli utenti emettono il commit nell'attività.** In genere la pagina Commit è l'ultima pagina di scelte e il pulsante Avanti viene rietichettato per indicare l'attività di cui viene eseguito il commit.
    -   Non usare pagine di riepilogo che riepilogano semplicemente le selezioni precedenti dell'utente, a meno che l'attività non sia rischiosa (che comporta sicurezza o perdita di tempo o denaro) o che gli utenti non necessitino di rivedere le selezioni.
-   **Usare le pagine Stato per visualizzare lo stato di un'operazione di lunga durata.** Al termine, la pagina di stato deve passare automaticamente al passaggio successivo. Deve rimanere nella pagina di stato solo se si verifica un problema che l'utente deve visualizzare. Fare clic su Torna a una pagina di stato non dovrebbe avere alcun effetto collaterale.
    -   **Usare un singolo indicatore di stato determinato.** Seguire le linee [guida dell'indicatore di stato determinate,](progress-bars.md)tra cui:
        -   Indicare chiaramente il completamento. Non lasciare che un indicatore di stato passi al 100% a meno che l'operazione non sia stata completata.
        -   Non riavviare lo stato di avanzamento. Un indicatore di stato perde il valore se viene riavviato (ad esempio perché viene completato un passaggio dell'operazione) perché gli utenti non hanno modo di sapere quando l'operazione verrà completata. In alternativa, tutti i passaggi nell'operazione condividono una parte dello stato di avanzamento e fare in modo che l'indicatore di stato passi al completamento una sola volta.
    -   **Fornire una descrizione concisa del passaggio corrente sopra l'indicatore di stato.** Per operazioni rapide, tale testo non è necessario. l'indicatore di stato da solo è sufficiente. Per le operazioni che richiedono un minuto o più, il testo può essere utile.
        -   Usare frammenti di frase, che in genere iniziano con un verbo e terminano con i puntini di sospensione. Esempi: copia di file, installazione dei componenti necessari.
        -   Posizionare il testo sopra la barra, non sotto.
        -   **Non corretto:**
        -   ![Screenshot dell'indicatore di stato con il testo sotto ](images/win-wizards-image18.png)
        -   In questo esempio il testo esplicativo dovrebbe essere visualizzato sopra l'indicatore di stato.
        -   Evitare di ingombrare la pagina di stato con dettagli non necessari. Questa pagina non è per il supporto tecnico. è per gli utenti.
        -   **Non corretto:**
        -   ![Screenshot dell'indicatore di stato con troppi dettagli ](images/win-wizards-image19.png)
        -   In questo esempio, i dettagli tecnici, ad esempio i GUID, sono inutili per gli utenti.
-   **Non usare pagine di congratulazioni che non esere terminare la procedura guidata.** Se i risultati della procedura guidata sono chiaramente evidenti per gli utenti, è sufficiente chiudere la procedura guidata nel pulsante di commit finale.
    -   Usare Follow-Up pagine quando è probabile che gli utenti eseguano attività correlate come follow-up. Evitare attività di follow-up familiari, ad esempio "Inviare un messaggio di posta elettronica".
    -   Usare le pagine di completamento solo quando i risultati non sono visibili e non esiste un modo migliore per fornire commenti e suggerimenti per il completamento dell'attività.
    -   Le procedure guidate con pagine Progress devono usare una pagina Completamento o Follow-Up per indicare il completamento dell'attività. Per le attività con esecuzione lunga, chiudere la procedura guidata nella pagina Commit e usare le notifiche per inviare commenti e suggerimenti.
-   **Usare le pagine di riepilogo solo se l'input è complesso e gli utenti devono esaminare, se l'attività comporta rischi significativi (ad esempio una transizione finanziaria) o se la procedura guidata esegue un'azione in base all'input dell'utente che non è ovvio (per creare una relazione di trust attraverso la trasparenza).** Spesso le pagine di riepilogo non soddisfano questa barra di pertinenza e possono essere omesse.
-   **Usare le pagine di errore se la procedura guidata non può essere completata a causa di un problema da cui non è possibile eseguire il ripristino.** In questa pagina viene illustrato il problema in un linguaggio chiaro, senza il linguaggio tecnico che gli utenti non capiranno. Fornire anche procedure pratiche che gli utenti possono eseguire per risolvere il problema. Per altre linee guida, vedere [Messaggi di errore](mess-error.md).
    -   **Eccezione:** Se la procedura guidata viene completata con un problema secondario da cui è possibile eseguire il ripristino, presentare il problema come attività aggiuntiva anziché come errore. Usare un linguaggio positivo, orientato al successo, incoraggiante, non termini come errore, errore o problema. Non usare un'icona di errore.

### <a name="navigation"></a>Spostamento

-   **Usare Avanti solo quando si avanza alla pagina successiva senza impegno.** L'avanzamento alla pagina successiva viene considerato un impegno quando il relativo effetto non può essere annullato facendo clic su Indietro o Annulla.
-   **Usare Indietro solo per correggere gli errori.** Oltre a correggere gli errori, gli utenti non devono fare clic su Indietro per eseguire lo stato di un'attività.
-   **Mantenere le selezioni utente tramite la navigazione.** Ad esempio, se l'utente apporta modifiche, fa clic su Indietro e quindi su Avanti, tali modifiche devono essere mantenute. Gli utenti non si aspettano di immettere nuovamente le modifiche a meno che non scelsino esplicitamente di cancellarle.
-   **Non disabilitare il pulsante Indietro a meno che la ripetizione dei passaggi non sia dannosa.**
-   **Consentire agli utenti di esplorare o rivedere le scelte negli scenari di navigazione seguenti:**
    -   L'utente fornisce input, fa clic sul pulsante Commit, fa clic su Indietro per rivedere le modifiche precedenti, non modifica nulla e quindi fa di nuovo clic sul pulsante commit. In genere, questo dovrebbe essere possibile e il secondo commit dovrebbe passare semplicemente alla pagina successiva (perché l'attività è già stata eseguita).
    -   L'utente fornisce input, fa clic sul pulsante Commit, fa clic su Indietro per rivedere le modifiche precedenti, modifica qualcosa e quindi fa di nuovo clic sul pulsante Commit. In genere, questo dovrebbe essere possibile e il secondo commit deve ripetere l'attività con l'input modificato (sostituendo o annullando l'effetto del primo).

### <a name="help"></a>Help

-   **Progettare pagine della procedura guidata per fornire informazioni sufficienti in modo che non sia necessario fare riferimento alla documentazione nella Guida del programma.** Una procedura guidata sta già allontanando gli utenti dall'interazione diretta desiderata con il programma; la richiesta agli utenti di cercare la Guida esterna li rimuove ulteriormente da questo stato. La Guida deve essere l'eccezione, non la regola.
-   **Se è necessario fornire un punto di accesso alla Guida, usare un collegamento nella parte inferiore sinistra dell'area del contenuto della pagina (sopra l'area dei comandi).** Questo collegamento deve essere breve e in genere formulato sotto forma di domanda a cui gli utenti probabilmente vogliono rispondere.
-   **Corretto:**
-   ![Screenshot della pagina della procedura guidata con collegamento alla Guida ](images/win-wizards-image5.png)
-   Questo collegamento alla Guida è appropriato perché le informazioni di base di base come questa ingombrerebbe troppo la pagina della procedura guidata.

## <a name="text"></a>Testo

### <a name="general"></a>Generale

-   Usare l'utente e per fare riferimento all'utente e al computer, al documento, alle impostazioni e così via. Non usare la prima persona (I, my) per fare riferimento al computer o alla procedura guidata. Tuttavia, è accettabile usare la prima persona nelle opzioni selezionate dall'utente. **Casella di controllo Esempio:Solo uso.**
-   Ogni pagina della procedura guidata deve avere [un'istruzione principale](glossary.md).

### <a name="titles"></a>Titoli

-   Inserire il nome della procedura guidata nella barra del titolo. Usare [l'uso di maiuscole e minuscole in stile titolo.](glossary.md)
-   I titoli non devono includere la punteggiatura, ad eccezione di quelli con punti interrogativi.
-   Non includere la parola Creazione guidata nei titoli della procedura guidata. Ad esempio, usare Connessione a una rete anziché alla rete Installazione guidata.

### <a name="buttons"></a>Pulsanti

-   Non includere testo nel pulsante Indietro. Usare invece il glifo a forma di freccia, senza etichetta.
-   Includere il testo nel pulsante Avanti. Non usare glifi (ad esempio > o >>) oltre alla parola Avanti.
-   Usare etichette specifiche del pulsante di commit che hanno senso da soli e che sono una risposta all'istruzione principale. Idealmente gli utenti non devono leggere altro per comprendere l'etichetta. È molto più probabile che gli utenti leggono le etichette dei pulsanti di comando rispetto al testo statico.
-   Se possibile, non usare la parola Fine per l'etichetta del pulsante commit, perché in genere è disponibile un pulsante di commit migliore e più specifico:
    -   Se facendo clic sul pulsante viene eseguito il commit nell'attività (in modo che l'attività non sia già stata eseguita), usare un'etichetta specifica che inizia con un verbo che rappresenta una risposta all'istruzione principale (ad esempio Print, Connessione, Start).
    -   Se l'attività è già stata eseguita all'interno della procedura guidata, usare invece Chiudi.

        **Eccezioni:**

        -   È possibile usare Fine quando l'etichetta specifica è ancora generica, ad esempio Salva, Seleziona, Scegli o Ottieni.
        -   È possibile usare Fine quando l'attività comporta la modifica di un'impostazione o di una raccolta di impostazioni.

-   Avviare le etichette dei pulsanti di commit con un verbo. Le eccezioni sono OK, Sì e No.
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Non usare punteggiatura finale.

## <a name="documentation"></a>Documentazione

-   Anche se Windows procedure guidate non hanno più la parola Procedura guidata nel titolo, è accettabile fare riferimento alle procedure guidate come procedure guidate nella documentazione. Questo riferimento deve essere in minuscolo.
-   **Corretto:**
-   Se si configura una rete per la prima volta, è possibile ottenere assistenza usando la procedura guidata Connessione **a una** rete.
-   Alcune procedure guidate legacy di versioni precedenti di Windows potrebbero includere la procedura guidata nel titolo. Quando si fa riferimento a una di queste procedure guidate, è accettabile usare la procedura guidata X per evitare di pronunciare \[ \] la procedura guidata \[ \] X.
-   Fare riferimento a una singola schermata all'interno di una procedura guidata come pagina.

 

 