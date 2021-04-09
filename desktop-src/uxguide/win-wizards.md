---
title: Procedure guidate
description: Nonostante questo meraviglioso nome bizzarro, le procedure guidate non sono davvero una forma speciale di interfaccia utente e hanno solo una particolare gamma di utilità.
ms.assetid: 122d6e65-92f0-4e8a-92f7-ecd7e90665c8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6455c38228606932e9144c744dd217d0a7fa67e8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103885906"
---
# <a name="wizards"></a>Procedure guidate

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Nonostante questo meraviglioso nome bizzarro, le procedure guidate non sono davvero una forma speciale di interfaccia utente e hanno solo una particolare gamma di utilità.

Le procedure guidate vengono utilizzate per eseguire attività in più passaggi.

![Screenshot che mostra la procedura guidata "Aggiungi stampante" con "quale tipo di stampante si vuole installare?" prompt.](images/win-wizards-image1.png)

![Screenshot che mostra la procedura guidata "Aggiungi stampante" durante la ricerca delle stampanti disponibili.](images/win-wizards-image2.png)

![screenshot dell'aggiunta guidata stampante ](images/win-wizards-image3.png)

Più passaggi di una procedura guidata vengono presentati come sequenza di pagine.

Nelle procedure guidate sono in genere inclusi i tipi di pagine seguenti:

-   Le pagine scelte vengono utilizzate per raccogliere informazioni e consentire agli utenti di scegliere.
-   La pagina commit viene utilizzata per eseguire un'azione che non può essere annullata facendo clic su indietro o Annulla.
-   La pagina stato consente di visualizzare lo stato di avanzamento di un'operazione di lunga durata.

La progettazione guidata moderna pone una soluzione Premium in termini di efficienza, rendendo la pagina di avanzamento facoltativa per operazioni più brevi e spesso distribuendo la pagina [iniziale di benvenuto](glossary.md) e la [pagina di congratulazioni](glossary.md) all'inizio e alla fine.

Tutte le pagine della procedura guidata includono i componenti seguenti:

-   Una barra del titolo per identificare il nome della procedura guidata, con un pulsante indietro nell'angolo superiore sinistro e un pulsante Chiudi con pulsanti facoltativi di riduzione/ingrandimento e ripristino. Si noti che la barra del titolo include anche un'icona per identificarla sulla barra delle applicazioni.
-   Un'istruzione principale per spiegare l'obiettivo dell'utente con la pagina.
-   Area di contenuto con testo facoltativo e possibilmente altri controlli.
-   Un'area di comando con almeno un pulsante di commit per eseguire il commit nell'attività o procedere al passaggio successivo.

Anche se una procedura guidata prevede più passaggi, questi passaggi devono essere tutti aggiunti a una singola attività, dal punto di vista dell'utente. Si tratta del principio di progettazione della procedura guidata fondamentale di "una procedura guidata, un'unica attività".

Pertanto, in questo articolo, un'attività è la funzione di base di una procedura guidata (ad esempio, l'attività di un'installazione guidata prevede l'installazione di un programma). Le sottoattività sono aspetti dell'attività più grande (ad esempio, una sottoattività di un'installazione guidata potrebbe essere la configurazione del programma da installare). Infine, ogni pagina della procedura guidata viene considerata un passaggio in una determinata attività o attività (ad esempio, potrebbero essere necessari due o tre passaggi per la configurazione del programma).

**Nota:** Le linee guida relative a [installazione](exper-setup.md), [finestre di dialogo](win-dialog-box.md)e [barre di stato](progress-bars.md) sono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Una procedura guidata può essere usata per qualsiasi attività che richiede più passaggi di input. Tuttavia, le procedure guidate valide hanno requisiti aggiuntivi:

-   **La procedura guidata esegue una singola attività atomica?** Non usare interazioni che non sono singole attività (un intero programma non deve mai essere una procedura guidata, a meno che non esegua una sola attività). Non usare le procedure guidate per combinare attività indipendenti o passaggi in gran parte non correlati.
-   **È possibile ridurre il numero di domande necessarie? Sono presenti valori predefiniti accettabili che funzionano correttamente per la maggior parte dei casi o che possono essere modificati in base alle esigenze in un secondo momento? Di conseguenza, è possibile ridurre il numero di pagine?** In tal caso, provare a semplificare l'attività in modo da poterla presentare in una singola pagina, ad esempio una finestra di dialogo, oppure eliminare la necessità di input completamente (consentendo l'esecuzione diretta dell'attività).
-   **È necessario fornire le domande necessarie in modo sequenziale? Esistono diverse domande probabili, ma facoltative?** In tal caso, prendere in considerazione una finestra di dialogo o una finestra di dialogo a schede.

    **Corretto:**

    ![screenshot della finestra di dialogo Opzioni di stampa ](images/win-wizards-image4.png)

    La finestra di dialogo Opzioni di stampa di Microsoft PowerPoint contiene numerose opzioni di input utente, pertanto è possibile presentarle in una procedura guidata. Tuttavia, non è necessario fornirli in modo sequenziale, quindi una finestra di dialogo è la scelta migliore.

Le procedure guidate sono una forma relativamente pesante dell'interfaccia utente. Se è disponibile una soluzione adatta, più leggera, usare!

## <a name="design-concepts&quot;></a>Concetti relativi alla progettazione

### <a name=&quot;overuse-of-wizards&quot;></a>Utilizzo eccessivo di procedure guidate

In passato, le procedure guidate differivano dall'interfaccia utente ordinaria in quanto sono state progettate per aiutare gli utenti a eseguire attività particolarmente complesse, con passaggi che risiedono in posizioni diverse, e spesso hanno incorporato funzionalità di intelligence per aiutare gli utenti a riuscire. Attualmente, tutte le interfacce utente devono essere progettate per semplificare il più possibile le attività, pertanto non è necessaria un'interfaccia utente speciale a questo scopo.

Tuttavia, la convinzione è che le procedure guidate sono un'interfaccia utente speciale, in gran parte perché sono denominate &quot;procedure guidate&quot; (molto più creative che, ad esempio, &quot;dialoghi&quot; e &quot;finestre delle proprietà"). Al contrario, è preferibile prendere in considerazione le attività in più passaggi e non attirare particolare attenzione a questo fatto.

Prima di creare una procedura guidata, valutare se gli utenti devono effettivamente essere interrotti dal flusso principale del programma. Potrebbe esserci una soluzione più leggera, inline e contestuale, che alla fine si risulterà più utile ed efficiente per gli utenti. Ad esempio, una funzionalità progettata in modo non corretto in un programma non garantisce una procedura guidata per spiegarla e semplificarla. garantisce la riprogettazione della funzionalità stessa. Una procedura guidata non può essere usata come Band-Aid per risolvere un problema più semplice con il programma.

### <a name="wizards-do-have-appropriate-functions"></a>Le procedure guidate dispongono di funzioni appropriate

Le procedure guidate sono una delle chiavi per semplificare l'esperienza utente. Consentono di eseguire un'operazione complessa, ad esempio la configurazione di un programma, e di suddividerla in una serie di semplici passaggi. In ogni punto del processo è possibile fornire una spiegazione degli elementi necessari e visualizzare i controlli che consentono all'utente di effettuare le selezioni e immettere il testo.

Alcuni tipi di attività in più passaggi si prestano al form della procedura guidata. In Windows, ad esempio, diverse procedure guidate coinvolgono funzioni di connettività (Internet o rete aziendale o dispositivi periferici quali stampanti e fax).

![cattura di schermata della connessione guidata ](images/win-wizards-image5.png)

La connessione a una rete è un'attività tipica di Windows appropriata per una procedura guidata.

Qui la funzione della procedura guidata consiste nel mediare tra un elemento noto e stabile (il sistema operativo predefinito) e un elemento sconosciuto e variabile (accordi di connettività con una società telefonica o un provider di servizi Internet). La complessità degli ecosistemi di elaborazione è sufficientemente significativa, ora che è effettivamente utile utilizzare le procedure guidate per ridurre tale complessità.

Altri tipi di attività che funzionano correttamente come le procedure guidate di Windows includono funzionalità di fascia alta, come il riconoscimento vocale e della grafia, e esperienze multimediali avanzate, ad esempio la configurazione di opzioni per la creazione e la pubblicazione di filmati. È possibile distribuire le procedure guidate anche per attività più semplici, ad esempio per la risoluzione dei problemi. In breve, se è probabile che utenti diversi desiderino sperimentare il programma in modi molto diversi, questo può indicare la necessità di una procedura guidata e la relativa capacità per più punti di input utente.

Per il programma, è opportuno un po' di tempo di progettazione in anticipo per determinare il funzionamento della procedura guidata e se tale funzione effettivamente aumenta fino al livello di distribuzione di una procedura guidata.

### <a name="wizard-length"></a>Lunghezza procedura guidata

Le domande di progettazione si verificano naturalmente intorno al numero e all'organizzazione delle pagine e delle opzioni. Ad esempio:

-   È disponibile un numero ottimale di pagine per una procedura guidata? O almeno un intervallo auspicabile?
-   La procedura guidata dovrebbe essere concisa e semplificata, in modo che gli utenti possano completarla nel minor tempo possibile?
-   Dovrebbero essere presenti più pagine che richiedono un minor numero di scelte? O un minor numero di pagine con maggiore complessità? Quale progettazione è considerata più utilizzabile?
-   È possibile progettare esperienze guidate più velocemente applicando le convenzioni dell'interfaccia utente, ad esempio le pagine a schede?

Microsoft ha utilizzato per consigliare che le procedure guidate di tre pagine o meno siano progettate come semplici procedure guidate e quelle di quattro o più pagine utilizzano una progettazione avanzata della procedura guidata (vedere le linee guida sull' [esperienza utente di Windows](/previous-versions/ms997609(v=msdn.10)) da 1999). Tuttavia, gli attuali standard di progettazione della procedura guidata preferiscono quello che rappresentava una delle differenze principali tra i moduli semplici e avanzati (l'utilizzo delle pagine di benvenuto e di congratulazioni), quindi queste categorie ora non sono adeguate e il numero di pagine che determinano la scelta della progettazione sembra arbitrario.

La procedura guidata deve essere di lunghezza o breve quanto richiesto dall'attività; non esiste alcuna linea fissa per la lunghezza. Una procedura guidata a una pagina dovrebbe essere effettivamente visualizzata come una finestra di dialogo, pertanto due pagine sono probabilmente la forma più condensata possibile per una procedura guidata.

**Corretto:**

![screenshot della finestra di dialogo Crea disco ](images/win-wizards-image6.png)

Questa attività dispone di poche opzioni che la presentano come procedura guidata. Una finestra di dialogo è il formato appropriato per questa interfaccia utente.

All'altra estremità dello spettro, se si dispone di una procedura guidata che include più punti decisionali e rami e spesso gli utenti perdono la traccia del percorso di navigazione, è stato superato un limite pratico e si dovrebbe ridurre la durata della procedura guidata. In alternativa, potrebbe essere possibile suddividere la procedura guidata in diverse attività distinte.

Quando si determina la lunghezza più appropriata per la procedura guidata, prestare particolare attenzione agli utenti di destinazione. I programmi per gli utenti finali, ad esempio gli utenti privati e i lavoratori di ufficio, tendono a utilizzare le procedure guidate per nascondere la complessità. le procedure guidate sono le più brevi possibile, con la progettazione semplice e semplice della pagina e le impostazioni predefinite preselezionate per il maggior numero possibile di opzioni. Al contrario, le procedure guidate per i server o i programmi destinati ai professionisti IT tendono a essere più lunghi e complessi. Questo gruppo di utenti di destinazione ha una tolleranza più elevata per prendere decisioni relative alla configurazione e può infatti diventare sospetto se è nascosta una quantità eccessiva di complessità.

Se una procedura guidata per natura semplifica un'attività complessa, è consigliabile eseguire questa operazione in modo relativamente minimo per un pubblico tecnicamente sofisticato e relativamente aggressiva per una base utente con novizio.

**Corretto:**

![screenshot della creazione guidata lingue di visualizzazione ](images/win-wizards-image7.png)

Questa pagina della procedura guidata è ben progettata per gli utenti finali, perché riduce un oggetto potenzialmente complesso a una semplice scelta binaria logica: installazione o disinstallazione.

**Corretto:**

![Screenshot che mostra la pagina "Selezione funzionalità" della procedura guidata "SQL Server installazione".](images/win-wizards-image8.png)

Nell'installazione guidata di Microsoft SQL Server 2008, la progettazione della pagina è più occupata e le varie scelte richiedono un maggior numero di volte, ma i destinatari sono amministratori di database che prevedono un controllo rigoroso della selezione delle funzioni.

Infine, prestare attenzione alla frequenza con cui la determinata attività potrebbe essere eseguita. Un'attività raramente può distribuire una procedura guidata più lunga, mentre le attività frequenti devono essere decisamente favorite dalla brevità.

### <a name="branching"></a>Diramazione

Per le procedure guidate più lunghe, potrebbe essere necessario creare rami del flusso attività in cui la sequenza di pagine può variare in base all'input dell'utente fornito "upstream". La diramazione viene intrinsecamente dislocata per gli utenti, pertanto è necessario progettare l'esperienza utente per garantire la stabilità. Si consiglia di non più di due punti decisionali che provocheranno la diramazione nell'intera procedura guidata e non più di un ramo annidato all'interno di un singolo Branch.

Per linee guida sulla creazione di un'esperienza utente stabile in una procedura guidata di diramazione, vedere [diramazione](#branching) nella sezione linee guida di questo articolo.

### <a name="providing-a-navigation-guide"></a>Fornire una guida alla navigazione

Le guide di spostamento possono essere utili in presenza di molti passaggi nell'attività e gli utenti possono perdere il proprio posto nella sequenza o semplicemente desiderano conoscere il tempo necessario per il completamento.

Le guide di navigazione sono spesso visualizzate come un elenco di pagine o sezioni della procedura guidata, in una colonna o in un riquadro a sinistra di ogni pagina. Sebbene l'elenco venga mantenuto in tutta la procedura guidata (lo stesso elenco di pagine viene visualizzato in ogni pagina), sono disponibili alcuni metodi visivi per indicare la posizione in cui l'utente è attualmente nella sequenza (ad esempio, utilizzando grassetto per distinguere la pagina o la sezione attiva).

Le guide di spostamento possono essere sequenziali o non sequenziali. Il tipo sequenziale presenta le pagine precedenti insieme alle pagine future note. È possibile presentare il futuro in termini di passaggi anziché di pagine se i passaggi sono noti e le pagine dipendono. È quindi possibile popolare le pagine in modo dinamico man mano che diventano note. Poiché la sequenza di navigazione è fissa, la Guida di navigazione non è interattiva.

Le guide di navigazione non sequenziali sono interattive, in modo che gli utenti possano rivedere direttamente le pagine visualizzate in precedenza. Possono anche saltare prima della sequenza di navigazione per le pagine progettate per essere facoltative. Le pagine facoltative devono avere valori predefiniti che sono accettabili nella maggior parte dei casi. Con questo tipo di guida:

-   Le pagine visualizzate in precedenza possono sempre essere visualizzate direttamente.
-   Le pagine future potrebbero non essere visualizzate se hanno prerequisiti.
-   Le pagine che è possibile visitare devono essere chiaramente distinte da quelle che non possono (ad esempio usando collegamenti attivi o disabilitati), insieme a pagine obbligatorie o facoltative.

In questo scenario gli utenti possono essere confusi sul significato del pulsante indietro. Se si fa clic su indietro, viene visualizzata la pagina o la sezione precedente nella Guida alla navigazione oppure è stata visualizzata l'ultima pagina o sezione? Poiché le creazioni guidate di Windows ora posizionano il pulsante indietro nell'angolo superiore sinistro delle pagine della procedura guidata, anziché nell'angolo in basso a destra con gli altri pulsanti di commit, gli utenti ritengono la funzionalità di back-down come nel Web. Quindi, la soluzione migliore consiste nel fare in modo che il pulsante indietro riporti lo spostamento Web, facendo clic su indietro per visualizzare l'ultima pagina o la sezione visualizzata, e utilizzare la Guida di spostamento della procedura guidata per la navigazione sequenziale.

### <a name="page-integrity"></a>Integrità della pagina

La progettazione della procedura guidata implica non solo le decisioni relative all'intero flusso di attività, ad esempio come gestire la navigazione e l'esperienza di diramazione, ma anche quelle riguardanti le singole pagine che costituiscono la procedura guidata. **Il principio più importante per la progettazione di pagine della procedura guidata corrette è quello di integrità: il contenuto di una pagina deve appartenere a un insieme.**

Le pagine della procedura guidata sono molto più utilizzabili se ciascuna di esse si blocca concettualmente, trattandosi di un solo aspetto dell'attività complessiva. L' [istruzione principale](glossary.md) è il modo principale per raggiungere questo obiettivo. Identificare chiaramente l'obiettivo o lo scopo della pagina agli utenti. Le [istruzioni aggiuntive](glossary.md)e tutti i controlli della pagina sono correlati direttamente all'istruzione principale. Sebbene le pagine della procedura guidata debbano presentare agli utenti le opzioni per le quali è necessario un po' di attenzione, questo lavoro non sembra funzionare perché è strettamente concentrato dall'integrità della pagina stessa.

Sfortunatamente, le finestre di progettazione della procedura guidata comunicano spesso il rapido clic del pulsante successivo come evidenza dell'usabilità, della semplicità e dell'integrità delle pagine. L'esperienza guidata Ultimate non è successiva, avanti, avanti, avanti, fine. Anche se questa esperienza suggerisce che i valori predefiniti sono stati scelti correttamente, suggerisce anche che la procedura guidata non era effettivamente necessaria perché tutte le opzioni sono facoltative.

In termini di oggetti visivi e testo, questo elemento viene ridotto a Bare Essentials. Resistere all'esigenza di aggregare più sottoattività in una singola pagina ("procedura guidata") o di ricorrere a schede per presentare requisiti di input complessi. Una singola pagina deve coprire una singola attività secondaria dell'attività complessiva della procedura guidata.

**Non corretto:**

![screenshot dell'installazione guidata di SQL Server ](images/win-wizards-image9.png)

Con tre schede di input utente abbastanza denso, questa pagina della procedura guidata sta provando a eseguire troppe operazioni.

Nella maggior parte dei casi, mantenere le dimensioni di ogni pagina in tutta la procedura guidata per favorire un aspetto coerente. Sebbene le creazioni guidate di Windows consentano pagine ridimensionabili, in modo che le dimensioni di una pagina corrispondano alla quantità di contenuto, solo alcune utilizzano questa opzione.

Infine, mantenere gli elementi strutturali di ogni pagina della procedura guidata attraverso la sequenza. Ad esempio, non spostare il pulsante indietro dall'angolo in alto a sinistra nell'area dei pulsanti di commit per una pagina o due. Questo livello di coerenza del layout consente agli utenti di essere stabili all'interno della procedura guidata. Si può pensare a questo come una linea di base per l'integrità visiva di una pagina.

### <a name="finding-the-right-level-of-communication"></a>Individuazione del livello di comunicazione corretto

Gli utenti hanno una bassa tolleranza per la lettura di grandi blocchi di testo sullo schermo e anche in meno, all'interno di una superficie dell'interfaccia utente il cui scopo esplicito è di spostarsi tempestivamente attraverso un'attività.

Le procedure guidate hanno una tendenza alla sovracomunicazione. Occupano molto spazio sullo schermo, che sembra incoraggiare un'unità a occupare lo spazio. È come una variazione della legge di Parkinson: il testo dell'interfaccia utente si espanderà per riempire lo spazio disponibile.

Un colpevole in questo eccesso è la ridondanza. A causa dei modelli utilizzati nella progettazione rapida della procedura guidata, è possibile che la stessa lingua venga visualizzata in più posizioni in una pagina, ad esempio nella barra del titolo, nelle intestazioni, nel testo del corpo, nelle etichette dei controlli e così via.

Vale la pena assumere un editor professionale per eliminare in modo spietato il testo della procedura guidata. Eliminare le domande e le opzioni non necessarie nelle singole pagine ed eliminare intere pagine dalla procedura guidata nel suo complesso (ad esempio, le pagine di benvenuto e di congratulazioni tradizionali). Passa direttamente al punto della pagina con un'istruzione principale scritta in modo conciso, usando la lingua che i destinatari usano per descrivere l'attività, non il gergo della tecnologia o della funzionalità utilizzata internamente dall'utente o dal team. Questo approccio incentrato sull'utente è fondamentale per migliorare la comunicazione delle procedure guidate del programma.

Prestare particolare attenzione al tono della procedura guidata: a volte le impressioni più durevoli del programma sono il risultato non di quello che si dice, ma come si dice! Nelle procedure guidate, gli utenti hanno familiarità con un tono descrittivo e colloquiale, con l'uso del pronome della seconda persona ("utente") quando il programma chiede l'input. Per altre linee guida, vedere [stile e tono](text-style-tone.md).

La riduzione del numero di parole nella pagina della procedura guidata è in genere lodevole, ma è necessario prestare attenzione a non andare troppo oltre. Se l'attività è importante e garantisce una procedura guidata, gli utenti apprezzeranno le informazioni necessarie per effettuare scelte sagge. Nell'esempio seguente viene illustrato come è possibile ridurre il testo della procedura guidata senza sacrificare il significato.

**Prima:**

![screenshot della procedura guidata ClearType, bozza ](images/win-wizards-image10.png)

**Dopo:**

![screenshot della procedura guidata ClearType, Revisione ](images/win-wizards-image11.png)

La versione modificata della pagina della procedura guidata fornisce un'istruzione principale orientata alle attività, rimuove il paragrafo esplicativo non necessario sotto l'istruzione principale e modifica l'etichetta della casella di controllo per chiarire lo scopo della casella di controllo.

**Se si eseguono solo tre operazioni...**

1. Eseguire il mapping dell'attività che si sta tentando di eseguire con l'interfaccia utente appropriata per eseguire il processo. non è sufficiente una procedura guidata per impostazione predefinita quando si ritiene che sia necessario raccogliere numerosi input dagli utenti.

2. Valutare con attenzione la lunghezza e la struttura della procedura guidata. preferisci procedure guidate brevi e non di branching per garantire l'esperienza più semplice possibile, in modo che gli utenti possano tornare alla propria attività principale o all'interesse del programma.

3. Verificare l'integrità di ogni pagina della procedura guidata: è necessario che il contenuto di una pagina appartenga chiaramente.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Considerare prima le alternative leggere, ad esempio le finestre di dialogo, i riquadri attività o le singole pagine.** Non è necessario usare le procedure guidate: è possibile fornire informazioni utili e assistenza in qualsiasi interfaccia utente.
-   **Utilizzare le procedure guidate per le attività in più passaggi.** Usare le finestre di dialogo a più pagine per le attività in un singolo passaggio con commenti e suggerimenti. Per altre linee guida, vedere [finestre di dialogo](win-dialog-box.md).

    **Corretto:**

    ![screenshot della finestra di dialogo Diagnostica ](images/win-wizards-image12.png)

    ![screenshot del feedback della finestra di dialogo di diagnostica ](images/win-wizards-image13.png)

    In questo esempio, la diagnostica di rete Windows è costituita dalle pagine stato e risultati. Poiché l'attività è un singolo passaggio, non richiede i pulsanti di spostamento necessari agli utenti in una procedura guidata. Viene presentata in modo efficace come finestra di dialogo a più pagine.

### <a name="window-size"></a>Dimensioni finestra

-   **Scegliere una dimensione della finestra in grado di visualizzare tutte le pagine della procedura guidata senza scorrimento pagina verticale o orizzontale.** Mentre i controlli della pagina potrebbero richiedere lo scorrimento, le pagine della procedura guidata non devono essere presenti.
-   **Dimensioni di Windows sufficientemente grandi da poter eseguire le proprie attività comodamente.** Il layout di pagina non deve essere ridotto o richiedere agli utenti di scorrere o ridimensionare in modo eccessivo.
-   **Ma non creare Windows eccessivamente grande.** Le finestre più grandi rendono l'attività più complessa e richiedono un movimento aggiuntivo per l'interazione.
-   **Usare le finestre ridimensionabili per una procedura guidata che può trarre vantaggio da più spazio sullo schermo, ma non lo richiede.** Assegnare dimensioni minime appropriate. Le finestre ridimensionabili sono utili quando le pagine richiedono l'interazione con contenuto ridimensionabile, ad esempio visualizzazioni elenco di grandi dimensioni.

    **Corretto:**

    ![screenshot del programma di installazione di Visual Studio, elenco parziale ](images/win-wizards-image14.png)

    **Migliore:**

    ![screenshot del programma di installazione di Visual Studio, elenco completo ](images/win-wizards-image15.png)

    In questo esempio, il ridimensionamento della finestra consente agli utenti di visualizzare l'elenco completo.

-   **Si consiglia di utilizzare procedure guidate di dimensioni dinamiche le cui dimensioni di pagina cambiano in base alle esigenze per il relativo contenuto.** Questa operazione consente a una procedura guidata di adattare i layout di pagina con un'ampia gamma di contenuti.
-   **Preferisci il ridimensionamento statico su dinamico se gli utenti possono percepire le modifiche come mancanza di stabilità nell'esperienza della procedura guidata.** La stabilità visiva spesso trionfa nell'alloggio del contenuto. La maggior parte delle procedure guidate deve adottare dimensioni di finestra statiche standard, con ridimensionamento dinamico riservato per casi speciali.

### <a name="wizard-length"></a>Lunghezza procedura guidata

-   **Rendere la procedura guidata più concisa e semplificata.** Elimina le opzioni e le domande non necessarie e usa le impostazioni predefinite intelligenti per ridurre il numero di pagine necessarie per l'input dell'utente.
    -   **Eccezione:** I professionisti IT e gli altri utenti tecnici hanno una maggiore tolleranza per le procedure guidate più lunghe e i requisiti di input dettagliati.
-   **Eseguire la procedura guidata per almeno due pagine.** In alternativa, è necessario riprogettare una procedura guidata a una pagina come finestra di dialogo.
-   **Non ridurre il numero di pagine della procedura guidata semplicemente aumentando la complessità di ogni pagina.** Ad esempio, una pagina della procedura guidata che include tre schede che richiedono l'input dell'utente deve essere riprogettata come tre pagine separate.
-   **Non aumentare il numero di pagine della procedura guidata rendendo ogni pagina talmente semplice che gli utenti fanno clic su avanti nell'intera sequenza.** Si tratta di un difetto comune di progettazione della procedura guidata. Se una pagina della procedura guidata non richiede almeno un certo grado di riflessione, probabilmente non deve necessariamente trovarsi nella procedura guidata.

### <a name="branching"></a>Diramazione

-   **Preferisci la progettazione guidata non di branching rispetto alla diramazione.** Le procedure guidate non di branching tendono a essere più semplici, più brevi e facili da esplorare. Le procedure guidate per la creazione di rami rendono più difficile per gli utenti determinare il numero di passaggi nell'attività e la posizione in cui si trovano nella sequenza.
-   **Se è necessario eseguire il branching, consentire agli utenti di orientarsi usando una delle tecniche seguenti:**
    -   **Enumerare le pagine.** Una tecnica comune è quella di indicare la posizione dell'utente nella sequenza in ogni pagina, ad esempio con il passaggio X di Y della frase. Assicurarsi che l'endpoint (Y) sia stabile. In caso di modifica del valore, questa operazione compromette la confidenza degli utenti.
    -   **Includere la nozione di passaggi secondari** , ad esempio il passaggio 2a di 6.
    -   **Eseguire le operazioni in modo indipendente dalle pagine, in cui ogni passaggio può coinvolgere diverse pagine.** Un servizio di viaggio, ad esempio, potrebbe impiegare l'organizzazione della procedura guidata in base a convenzioni di e-commerce ben stabilite per il settore.

        **Corretto:**

        ![screenshot dell'organizzazione guidata basata su passaggi ](images/win-wizards-image16.png)

        Le etichette logiche possono fornire un orientamento appropriato per gli utenti di una procedura guidata di creazione di rami.

    -   **Considera i passaggi facoltativi come permanenti nella sequenza di enumerazione.** Ad esempio, se un ramo Ignora solo alcuni passaggi facoltativi, è sufficiente ignorare i passaggi anche nei commenti e suggerimenti, anziché rinumerarli. Pertanto, se un utente effettua una scelta nella pagina 2 per rendere facoltative le pagine 3 e 4, visualizzare i passaggi 1, 2, 5 e 6 di 6. Non rinumerare i passaggi 5 e 6.
    -   **Se la procedura guidata usa un singolo Branch e il ramo si verifica all'inizio dell'attività, avviare la sequenza in quel momento e quindi usare semplicemente l'approccio senza diramazione.** Ovvero, a partire dal punto del ramo, avanza in sequenza fino alla fine del ramo.

-   **Se è necessario eseguire il branching, limitare il numero di rami a uno o due all'interno di un'unica procedura guidata.** Non includere mai più di un ramo in un ramo (un ramo "annidato").

### <a name="commit-buttons"></a>Pulsanti di commit

-   **Quando si esegue il commit di un utente in un'attività, utilizzare un pulsante commit che rappresenta una risposta specifica all'istruzione principale** (ad esempio, stampa, Connetti o avvia). Non usare etichette generiche come Next (che non implicano l'impegno) o Finish (che non è specifico) per il commit di un'attività. Le etichette di questi pulsanti di commit dovrebbero avere un significato autonomo. Avviare sempre le etichette dei pulsanti di commit con un verbo. **Eccezioni**
    -   Usare Finish quando le risposte specifiche sono ancora generiche, ad esempio Save, Select, choose o Get.
    -   Utilizzare fine per modificare un'impostazione specifica o una raccolta di impostazioni.
-   **Una singola procedura guidata può avere più punti di commit, ma è preferibile un singolo punto.**
-   **Se necessario, è possibile rinominare o nascondere i pulsanti di commit in una pagina.** Questa flessibilità è uno dei vantaggi della nuova progettazione guidata di Windows che non era disponibile nelle procedure guidate precedenti. Si noti che nascondere un pulsante commit è diverso dalla disabilitazione.
-   **Evitare di disabilitare un pulsante di commit positivo.** In caso contrario, gli utenti devono dedurre perché i pulsanti commit sono disabilitati. È preferibile lasciare abilitati i pulsanti di commit e fornire un messaggio di errore utile quando si verifica un problema. La disabilitazione del pulsante è accettabile solo se la causa è ovvia e non ambigua.
-   **Non confondere i pulsanti di navigazione (avanti e indietro) con i pulsanti di commit.** Quindi, procedere con l'avanzamento nella procedura guidata senza impegno; Tornare sempre disponibile nella pagina successiva e fare clic su indietro per annullare l'effetto dell'ultimo pulsante Avanti. Se ciò non è possibile, gli utenti stanno facendo un impegno e questo è indicato tramite un'etichetta specifica nel pulsante commit. Per altre linee guida sui pulsanti avanti e indietro, vedere [navigazione](#providing-a-navigation-guide).

### <a name="cancel-buttons"></a>Pulsanti Annulla

-   **Non invitare gli utenti a confermare se hanno effettivamente intenzione di annullare.** Questa operazione può risultare fastidiosa. **Eccezioni**
    -   L'azione ha conseguenze significative e, se non è corretta, non è facilmente risolvibile.
    -   L'azione può causare una perdita significativa del tempo o del lavoro dell'utente.
    -   L'azione è chiaramente incoerente con altre azioni.
-   **Consente agli utenti di riavviare le procedure guidate in caso di annullamento per errore.**
-   **Non disabilitare il pulsante Annulla. Eccezioni**
    -   Se l'annullamento è dannoso, è possibile che si tratti di un'attività in procedure guidate autosufficienti.
    -   Se l'annullamento è impossibile, questo potrebbe essere il caso in cui la procedura guidata non ha il controllo su tutti i passaggi.

### <a name="close-buttons"></a>Chiudi pulsanti

-   **Utilizzare Close per le pagine Follow-Up e complete.** Non usare Annulla perché la chiusura della finestra non abbandonerà le modifiche o le azioni eseguite a questo punto. Non usare done perché non è un verbo imperativo.
-   **Una volta eseguita l'attività, l'annullamento dovrebbe essere chiuso (per le procedure guidate indipendenti).** L'effetto di Close è semplicemente chiudere la finestra.

### <a name="other-controls"></a>Altri controlli

-   **Usare i collegamenti ai comandi solo per le scelte, non per gli impegni.** I pulsanti di commit specifici indicano un impegno molto migliore rispetto ai collegamenti ai comandi in una procedura guidata.
-   **Quando si usano i collegamenti ai comandi, nascondere il pulsante Avanti, ma lasciare il pulsante Annulla.**

### <a name="using-pages-vs-dialog-boxes-or-inline-ui"></a>Utilizzo di pagine (o finestre di dialogo o interfaccia utente inline)

-   **In generale, preferisce le pagine alle finestre di dialogo.** Gli utenti si aspettano che le procedure guidate siano basate su pagine.
-   **Usare le finestre di dialogo per facilitare il completamento delle pagine,** ad esempio con i selezionatori di oggetti e i browser.
-   **Usare le finestre di dialogo per fornire messaggi di errore che si applicano all'intera pagina e il risultato della selezione di un pulsante di commit.**
-   **Usare la presentazione inline per i comportamenti dinamici semplici,** ad esempio la divulgazione progressiva e l'interfaccia utente contestuale.
-   **Utilizzare la presentazione inline per i messaggi di errore che si applicano a controlli specifici.**

### <a name="wizard-pages"></a>Pagine della procedura guidata

-   **Concentrati su un processo decisionale efficiente.** Ridurre il numero di pagine per concentrarsi sui concetti di base. Consolidare le pagine correlate e prendere le pagine facoltative dal flusso principale. Se gli utenti fanno clic su avanti completamente, la procedura guidata potrebbe sembrare un'esperienza ottimale, ma se gli utenti non devono modificare le impostazioni predefinite, le pagine sono probabilmente non necessarie.
-   **Progettare ogni pagina in modo da avere un solo scopo e coerenza visiva.** Per ulteriori informazioni, vedere [integrità della pagina](#page-integrity).
-   **Non usare le pagine di benvenuto. quando possibile, rendere la prima pagina funzionale.** Usare una pagina di Introduzione facoltativa solo nei casi seguenti:

    -   La procedura guidata include i prerequisiti necessari per completare correttamente la procedura guidata.
    -   Gli utenti potrebbero non comprendere lo scopo della procedura guidata in base alla pagina della prima scelta e non c'è spazio per altre spiegazioni.
    -   L'istruzione principale per Introduzione pagine è "prima di iniziare:".

    **Non corretto:**

    ![screenshot della pagina iniziale dell'installazione di MapPoint ](images/win-wizards-image17.png)

-   Le procedure guidate moderne scelgono le prime pagine funzionali. Qui non è necessario eseguire alcuna operazione, ma fare clic su Avanti. Perché forzare gli utenti a pagare questa tassa sul token per il tempo prezioso?
-   **Nelle pagine in cui agli utenti viene richiesto di scegliere, ottimizzare per i casi più probabili.** Questi tipi di pagine devono presentare scelte effettive, non solo istruzioni.
    -   Se non si usa una pagina Introduzione, spiegare lo scopo della procedura guidata nella parte superiore della prima pagina di opzioni.
-   **Utilizzare le pagine di commit per cancellare il commit dell'attività da parte degli utenti.** In genere, la pagina commit è l'ultima pagina di scelte e il pulsante Avanti viene rietichettato per indicare l'attività di cui viene eseguito il commit.
    -   Non usare le pagine di riepilogo che riepilogano semplicemente le selezioni precedenti dell'utente, a meno che l'attività non sia rischiosa (che comporti la sicurezza o si verifichi una perdita di tempo o denaro) oppure è possibile che gli utenti debbano verificare le selezioni.
-   **Utilizzare le pagine di stato per visualizzare lo stato di un'operazione di lunga durata.** Al termine dell'operazione, la pagina di avanzamento dovrebbe passare automaticamente al passaggio successivo. Dovrebbe rimanere nella pagina di avanzamento solo se si verifica un problema che l'utente deve visualizzare. Quando si fa clic nuovamente su una pagina di stato, non dovrebbe esistere alcun effetto collaterale.
    -   **Utilizzare un singolo indicatore di stato determinato.** Seguire le [linee guida relative all'indicatore di stato](progress-bars.md), tra cui:
        -   Indica chiaramente il completamento. Non lasciare che un indicatore di stato vada al 100%, a meno che l'operazione non sia stata completata.
        -   Non riavviare lo stato di avanzamento. Un indicatore di stato perde il suo valore se viene riavviato (forse perché un passaggio nell'operazione viene completato) perché gli utenti non hanno modo di sapere quando l'operazione verrà completata. Al contrario, tutti i passaggi dell'operazione condividono una parte dello stato di avanzamento e l'indicatore di stato passa al completamento una volta.
    -   **Fornire una descrizione concisa del passaggio corrente sopra l'indicatore di stato.** Per operazioni rapide, il testo non è necessario; l'indicatore di stato da solo è sufficiente. Per le operazioni che richiedono un minuto o più, il testo può essere utile.
        -   Usare i frammenti di frase, in genere a partire da un verbo e terminando con i puntini di sospensione. Esempi: copia dei file in corso..., installazione dei componenti richiesti in corso...
        -   Posizionare il testo sopra la barra, non sotto.
        -   **Non corretto:**
        -   ![screenshot dell'indicatore di stato con il testo riportato di seguito ](images/win-wizards-image18.png)
        -   In questo esempio il testo esplicativo verrà visualizzato sopra l'indicatore di stato.
        -   Evitare di ingombrare la pagina di stato con dettagli superflui. Questa pagina non è per il supporto tecnico; per gli utenti.
        -   **Non corretto:**
        -   ![screenshot dell'indicatore di stato con troppi dettagli ](images/win-wizards-image19.png)
        -   In questo esempio, i dettagli tecnici, ad esempio i GUID, non sono significativi per gli utenti.
-   **Non usare le pagine di congratulazioni che non eseguono alcuna operazione ma terminano la procedura guidata.** Se i risultati della procedura guidata sono chiaramente evidenti per gli utenti, è sufficiente chiudere la procedura guidata sul pulsante finale commit.
    -   Utilizzare le pagine di Follow-Up quando sono presenti attività correlate che è probabile che gli utenti eseguano come completamento. Evitare attività di completamento familiari, ad esempio "inviare un messaggio di posta elettronica".
    -   Usare le pagine di completamento solo quando i risultati non sono visibili e non è disponibile un modo migliore per fornire commenti e suggerimenti per il completamento delle attività.
    -   Le procedure guidate che dispongono di pagine di stato devono utilizzare una pagina di completamento o Follow-Up pagina per indicare il completamento dell'attività. Per le attività a esecuzione prolungata, chiudere la procedura guidata nella pagina commit e utilizzare le notifiche per inviare commenti e suggerimenti.
-   **Utilizzare le pagine di riepilogo solo se l'input è complesso ed è necessario che gli utenti rivedano, se l'attività comporta un rischio significativo (ad esempio una transizione finanziaria) o se la procedura guidata eseguirà un'azione in base all'input dell'utente che non è ovvio (per creare l'attendibilità tramite la trasparenza).** Spesso le pagine di riepilogo non soddisfano questa barra di pertinenza e possono essere omesse.
-   **Utilizzare le pagine di errore se non è possibile completare la procedura guidata a causa di un problema da cui non è possibile eseguire il ripristino.** In questa pagina viene illustrato il problema della lingua chiara, senza che gli utenti del gergo tecnico non siano in conoscenza. Consente inoltre di eseguire i passaggi pratici che gli utenti possono eseguire per risolvere il problema. Per altre linee guida, vedere [messaggi di errore](mess-error.md).
    -   **Eccezione:** Se la procedura guidata viene completata con un problema minore dal quale è possibile il ripristino, presentare il problema come attività aggiuntiva anziché come errore. Usa un linguaggio positivo, orientato al successo, incoraggiante, non termini come errori, errori o problemi. Non usare un'icona di errore.

### <a name="navigation"></a>Spostamento

-   **Utilizzare avanti solo quando si avanza alla pagina successiva senza impegno.** Il passaggio alla pagina successiva viene considerato un impegno quando l'effetto non può essere annullato facendo clic su indietro o su Annulla.
-   **Utilizzare di nuovo solo per correggere gli errori.** Oltre a correggere gli errori, gli utenti non devono fare clic su indietro per avanzare in un'attività.
-   **Mantieni le selezioni degli utenti attraverso la navigazione.** Se, ad esempio, l'utente apporta modifiche, fa clic su indietro e quindi su Avanti, tali modifiche devono essere mantenute. Non è necessario che gli utenti immettano di nuovo le modifiche, a meno che non vengano esplicitamente selezionate per cancellarle.
-   **Non disabilitare il pulsante indietro, a meno che la ripetizione dei passaggi sia dannosa.**
-   **Consentire agli utenti di esplorare o rivedere le scelte negli scenari di navigazione seguenti:**
    -   L'utente assegna un input, fa clic sul pulsante commit, fa clic su indietro per rivedere le modifiche precedenti, non modifica nulla, quindi fa nuovamente clic sul pulsante commit. In genere, questa operazione dovrebbe essere possibile e il secondo commit dovrebbe passare alla pagina successiva (perché l'attività è già stata eseguita).
    -   L'utente assegna un input, fa clic sul pulsante commit, fa clic su indietro per rivedere le modifiche precedenti, modifica qualcosa, quindi fa nuovamente clic sul pulsante commit. In genere, questa operazione dovrebbe essere possibile e il secondo commit deve ripetere l'attività con l'input modificato (sostituendo o anportando l'effetto del primo).

### <a name="help"></a>Help

-   **Pagine della procedura guidata di progettazione per fornire informazioni sufficienti in modo che il riferimento alla documentazione nella guida del programma non sia necessario.** Una procedura guidata sta già prendendo gli utenti dall'interazione diretta desiderata con il programma; Se si richiede agli utenti di cercare la guida esterna, è possibile rimuoverli anche ulteriormente da questo stato. La guida deve essere l'eccezione, non la regola.
-   **Se è necessario fornire un punto di accesso per la guida, utilizzare un collegamento nella parte inferiore sinistra dell'area del contenuto della pagina (sopra l'area di comando).** Questo collegamento dovrebbe essere breve e, in genere, espresso sotto forma di una domanda a cui gli utenti hanno più probabilità di rispondere.
-   **Corretto:**
-   ![screenshot della pagina della procedura guidata con collegamento alla guida ](images/win-wizards-image5.png)
-   Questo collegamento alla guida è appropriato perché le informazioni di base di base come questa potrebbero complicare eccessivamente la pagina della procedura guidata.

## <a name="text"></a>Testo

### <a name="general"></a>Generale

-   Usare l'utente e il per fare riferimento all'utente e al computer, al documento, alle impostazioni e così via dell'utente. Non usare la prima persona (I, My) per fare riferimento al computer o alla procedura guidata. Tuttavia, è accettabile usare la prima persona nelle opzioni selezionate dall'utente. **Esempio:** casella di controllo Use only.
-   Ogni pagina della procedura guidata deve disporre di un' [istruzione principale](glossary.md).

### <a name="titles"></a>Titoli

-   Inserire il nome della procedura guidata nella barra del titolo. Usare l'uso [di maiuscole in stile titolo](glossary.md).
-   I titoli non devono includere la punteggiatura, ad eccezione di quelli con punti interrogativi.
-   Non includere la creazione guidata parola nei titoli della procedura guidata. Utilizzare ad esempio Connetti a una rete anziché installazione guidata rete.

### <a name="buttons"></a>Pulsanti

-   Non includere il testo sul pulsante indietro. Usare invece il glifo della freccia senza etichetta.
-   Includere il testo sul pulsante Avanti. Non usare i glifi, ad esempio > o >>, oltre alla parola successiva.
-   Usare etichette di pulsanti di commit specifiche che hanno un significato autonomo e sono una risposta all'istruzione principale. Idealmente, gli utenti non devono leggere nient'altro per comprendere l'etichetta. È molto più probabile che gli utenti leggano le etichette dei pulsanti di comando rispetto al testo statico.
-   Se possibile, non usare la parola Finish per l'etichetta del pulsante commit, perché in genere esiste un pulsante di commit migliore e più specifico:
    -   Se si fa clic sul pulsante commit dell'attività (in modo che l'attività non sia già stata eseguita), usare un'etichetta specifica che inizia con un verbo che rappresenta una risposta all'istruzione principale (esempi: Print, Connect, Start).
    -   Se l'attività è già stata eseguita all'interno della procedura guidata, utilizzare Close in alternativa.

        **Eccezioni**

        -   È possibile utilizzare Finish quando l'etichetta specifica è ancora generica, ad esempio Save, Select, choose o Get.
        -   È possibile utilizzare fine quando l'attività comporta la modifica di un'impostazione o di una raccolta di impostazioni.

-   Avviare le etichette dei pulsanti di commit con un verbo. Le eccezioni sono OK, sì e no.
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Non usare punteggiatura finale.

## <a name="documentation"></a>Documentazione

-   Sebbene la maggior parte delle procedure guidate di Windows non disponga più della procedura guidata di Word, è accettabile fare riferimento alle procedure guidate come procedure guidate nella documentazione. Questo riferimento deve essere minuscolo.
-   **Corretto:**
-   Se si sta configurando una rete per la prima volta, è possibile ottenere assistenza usando la procedura guidata **Connetti a una rete** .
-   Alcune procedure guidate legacy di versioni precedenti di Windows possono includere la procedura guidata nel titolo. Quando si fa riferimento a una di queste procedure guidate, è accettabile utilizzare la \[ \] procedura guidata x per evitare di ripetere la procedura guidata \[ x \] .
-   Fare riferimento a una singola schermata in una procedura guidata come pagina.

 

 