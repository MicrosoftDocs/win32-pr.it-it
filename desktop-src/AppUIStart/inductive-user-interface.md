---
title: Interfaccia utente indotta
description: In questo argomento viene descritto il modello di interfaccia utente noto come IUI (inductal User Interface).
ms.assetid: d99dc30a-68e5-4b7a-8cbd-0ac77a90a354
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 632e16191b7103cbf6be9fe209ada78781d4a53c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220910"
---
# <a name="inductive-user-interface"></a>Interfaccia utente indotta

In questo argomento viene descritto il modello di interfaccia utente noto come IUI (inductal User Interface). Detto anche navigazione induttiva, il modello IUI suggerisce come rendere più semplici le applicazioni software suddividendo le funzionalità in schermate o pagine facili da spiegare e comprendere. Questo modello di IUI è evidente in diversi progetti Microsoft, ad esempio Microsoft Money 2000, i applet del pannello di controllo di Windows, varie schermate e finestre di dialogo in Microsoft Visual Studio 2010 e i pannelli attività Microsoft Office.

-   [Introduzione](#introduction)
-   [IUI in azione: risoluzione di un problema di progettazione comune](#iui-in-action-solving-a-common-design-problem)
    -   [Il problema: il software è difficile da usare](#the-problem-software-is-hard-to-use)
    -   [Interfaccia utente deduttiva](#deductive-user-interface)
    -   [Soluzione: interfaccia utente indotta](#a-solution-inductive-user-interface)
-   [Passaggi per la creazione di un'interfaccia utente indotta](#steps-for-creating-an-inductive-user-interface)
    -   [Passaggio uno: concentrare ogni pagina su un'unica attività](#step-one-focus-each-page-on-a-single-task)
    -   [Passaggio 2: stato dell'attività](#step-two-state-the-task)
    -   [Passaggio 3: rendere il contenuto della pagina adatto all'attività](#step-three-make-the-pages-contents-suit-the-task)
    -   [Passaggio 4: offrire collegamenti a attività secondarie](#step-four-offer-links-to-secondary-tasks)
-   [Linee guida aggiuntive](#additional-guidelines)
    -   [Usare modelli di schermo coerenti](#use-consistent-screen-templates)
    -   [Rendere evidente come eseguire l'attività con i controlli sullo schermo](#make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen)
    -   [Fornire un modo semplice per completare un'attività e avviarne una nuova](#provide-screens-for-starting-tasks)
    -   [Rendere ovvio il passaggio successivo per la navigazione](#make-the-next-navigational-step-obvious)
-   [Assistenza utenti](#user-assistance)
    -   [Assistenza primaria](#primary-assistance)
    -   [Assistenza secondaria](#secondary-assistance)
-   [Appendice: progettazione e test di Microsoft Money 2000](#appendix-designing-and-testing-microsoft-money-2000)
    -   [Progettazione e testing di Money 2000](#designing-and-testing-money-2000)
    -   [Test di usabilità](#usability-tests)
    -   [Confronto con siti Web](#comparison-with-web-sites)

## <a name="introduction"></a>Introduzione

IUI è un modello di interfaccia utente che suggerisce come rendere più semplici le applicazioni software suddividendo le funzionalità in schermate o pagine facili da spiegare e comprendere. Microsoft ha implementato questo modello in Money 2000, un'applicazione software commerciale di grandi dimensioni. I test informativi indicano che gli utenti possono eseguire le attività nel modo più rapido in questo modello come nelle interfacce tradizionali e possono trovarle più facilmente.

Molte applicazioni software commerciali includono interfacce utente in cui una schermata presenta un set di controlli, ma lascia all'utente di dedurre lo scopo della pagina e come usare i controlli per eseguire tale scopo.

I principi descritti in questo documento non richiedono o implicano particolari insiemi rigidi di progettazione, controlli o elementi visivi. Come le interfacce utente grafiche in generale, i principi di questo documento lasciano molto spazio per la flessibilità e la creatività nella progettazione.

I principi generali dell'interfaccia utente indotta sono illustrati con esempi tratti da Money 2000.

> [!IMPORTANT]
> Il concetto generale di IUI è nella sua immaginazione. I progettisti che usano queste tecniche sono apprendere e scoprire di più su di esso in quanto vengono usati per il software. Le informazioni contenute in questo documento si evolveranno nel tempo man mano che le ricerche e le conoscenze in quest'area aumentano. In questo argomento viene fornita un'introduzione a IUI, piuttosto che a una serie completa di linee guida.

 

## <a name="iui-in-action-solving-a-common-design-problem"></a>IUI in azione: risoluzione di un problema di progettazione comune

Questa sezione illustra un problema di progettazione comune con i prodotti software odierni e introduce IUI come tecnica per superare il problema.

### <a name="the-problem-software-is-hard-to-use"></a>Il problema: il software è difficile da usare

La maggior parte del software è troppo difficile da usare. Questa conclusione è ricavata da test di usabilità, evidenza aneddotica e esperienze personali dei progettisti software. Il concetto di IUI è stato creato conducendo ricerche, ipotizzando ipotesi che rendono difficile l'utilizzo del software corrente e quindi proponendo soluzioni. Le finestre di progettazione che usano IUI devono basarsi sulla soddisfazione del cliente per determinare il successo finale della progettazione.

I prodotti software più recenti sono difficili da usare per i motivi generali seguenti:

-   Gli utenti non sembrano costruire un modello mentale appropriato del prodotto.

    Per la progettazione dell'interfaccia per la maggior parte dei prodotti software correnti si presuppone che gli utenti conoscano un modello concettuale creato appositamente dalle finestre di progettazione. Sfortunatamente, la maggior parte degli utenti non sembra mai acquisire un modello mentale sufficientemente completo e accurato per guidare la navigazione. Questi utenti sono probabilmente molto occupati e sovraccaricati con le informazioni. Non hanno tempo, energia o desiderio di studiare un modello concettuale per il software.

-   Anche molti utenti a lungo termine non padroneggiano mai procedure comuni.

    I progettisti sanno che i nuovi utenti potrebbero avere problemi alla prima, ma si aspettano che questi problemi si dissolvano mentre gli utenti imparavano le attività comuni. I dati di usabilità indicano che questo problema non si verifica spesso. In uno studio, i ricercatori configurano apparecchiature automatizzate per la registrazione degli utenti a casa. Nei nastri è stato indicato che gli utenti che si concentrano sull'attività non devono necessariamente notare la procedura che seguono e non imparano dall'esperienza. Alla successiva esecuzione della stessa operazione, gli utenti potrebbero inciampare nello stesso modo.

-   Gli utenti devono lavorare duramente per individuare ogni funzionalità o schermata.

    La maggior parte dei prodotti software è progettata per i pochi utenti che ne comprendono il modello concettuale e le procedure comuni sono state padroneggiate. Per la maggior parte dei clienti, ogni funzionalità o procedura è un rompicapo frustrante e indesiderato. È possibile che gli utenti presuppongano che questi puzzle siano un costo inevitabile per l'utilizzo di computer, ma sarebbero sicuramente più contenti senza questo onere.

La soluzione migliore a questi problemi consiste nell'individuare una strategia generale per rendere le funzionalità dei prodotti software più evidenti e autoesplicative. Gli utenti devono essere in grado di trovare una funzionalità ogni volta che ne hanno bisogno e devono poter usare tale funzionalità ogni volta che vogliono usarla.

### <a name="deductive-user-interface"></a>Interfaccia utente deduttiva

La maggior parte degli elementi del software oggi richiede all'utente di studiarli e dedurre il comportamento, come illustrato nella schermata seguente.

![screenshot della finestra di dialogo Proprietà campione.](images/iuiguidelines01.png)

Gli utenti esperti del computer, inclusi i progettisti software, riconoscono rapidamente che questa finestra di dialogo consente loro di gestire un elenco di elementi. Sono consapevoli che i pulsanti sotto l'elenco possono aggiungere, rimuovere e fornire informazioni sugli elementi dell'elenco. Si noti tuttavia che nessuno di questi comportamenti è dichiarato in modo esplicito nella finestra di dialogo.

È ora possibile esaminare la finestra di dialogo dal punto di vista di un utente occasionale. Molti utenti, quando si trovano in questa finestra di dialogo, chiederanno "cosa devo fare?" Quando viene visualizzata la finestra di dialogo, l'utente deve arrestare e determinare le operazioni da eseguire successivamente. In primo luogo, l'utente deve dedurre il fatto che il rettangolo bianco di grandi dimensioni è una casella di riepilogo vuota da riempire con gli elementi. L'etichetta di testo di piccole dimensioni della casella, "Things", offre un suggerimento vago. Alcuni utenti tentano di digitare nella casella di riepilogo, perché sembra una casella di testo di modifica.

Successivamente, l'utente deve dedurre che i pulsanti sotto l'elenco influiscono sul contenuto. Alcuni pulsanti sono inizialmente disabilitati, che è un'altra potenziale fonte di confusione dell'utente. Per informazioni sul funzionamento della finestra di dialogo, l'utente deve provare a usare i controlli.

L'utente potrebbe anche porre altre domande: "quanti elementi è necessario inserire nell'elenco? È necessario immettere gli elementi in un ordine specifico? Perché questa finestra di dialogo è stata visualizzata in primo luogo? Che cosa serve? "

Gli utenti vengono distratti dai rispettivi obiettivi ogni volta che devono determinare lo scopo di una schermata e come usarlo. In definitiva rappresenta un costo nel tempo e la soddisfazione degli utenti. Ancora peggio, gli utenti pagano questo costo più volte durante l'uso dell'interfaccia ogni volta che usano una funzionalità.

Una schermata deve avere un titolo che ne spieghi chiaramente lo scopo. Quando le finestre di progettazione creano una schermata, è raramente necessario che lo scopo di esprimibile sia chiaramente. Al contrario, può essere semplicemente parte di un modello concettuale più ampio che l'utente deve dedurre.

Gli studi mostrano che molti utenti sono confusi anche dalle operazioni di base nel software. Hanno difficoltà a capire cosa può fare il prodotto, dove eseguire un'operazione e come eseguire tale operazione una volta individuata. Semplificare il software apportando modifiche fondamentali è un modo efficace per soddisfare al meglio i clienti esistenti e attrarre nuovi utenti.

### <a name="a-solution-inductive-user-interface"></a>Soluzione: interfaccia utente indotta

Come nuovo metodo di progettazione del software, l'obiettivo di IUI è ridurre la quantità di elementi estranei che è necessario eseguire per spostarsi tra le parti di un prodotto e utilizzarne le funzionalità. La parola induttiva deriva dal verbo indurre, il che significa condurre o spostarsi in base a influenza o persuasione.

IUI è un'estensione dell'interfaccia di tipo Web comune. Nell'ambiente Web le pagine devono essere semplici e basate su attività perché ogni informazione deve essere inviata a un server in una connessione relativamente lenta. Il server risponde quindi con il passaggio successivo e così via. Una progettazione Web efficace significa concentrarsi su una singola attività per pagina e fornire lo spostamento tra le pagine. Analogamente, la navigazione indotta inizia con la messa a fuoco dell'attività in ogni pagina in un'unica attività primaria.

Un'interfaccia indotta ben progettata consente agli utenti di rispondere a due domande fondamentali che devono affrontare quando esaminano una schermata:

-   Cosa devo fare ora?
-   Da dove è possibile passare da qui per eseguire l'attività successiva?

Il software progettato in base a questi principi risponde a queste domande iniziando da un presupposto fondamentale: una schermata con uno scopo esplicito, chiaramente dichiarato, è più facile da comprendere rispetto a una pagina senza tale scopo. Se la schermata è più facile da comprendere, sarà più semplice per l'utente sapere cosa fare e dove andare avanti.

Questo presupposto fondamentale può essere ampliato in una serie di quattro passaggi per la progettazione di software che usa IUI:

-   Concentrare ogni schermata su una singola attività.
-   Stato dell'attività.
-   Rendere il contenuto della schermata adatta all'attività.
-   Offrire collegamenti alle attività secondarie.

Sebbene in questo documento vengano descritti i principi generali di IUI, vengono illustrati anche questi principi in azione mostrando esempi di Money 2000 e altri software. È necessario considerare questi esempi come espressioni particolari di IUI, non un modello rigoroso per l'implementazione.

Oltre ai quattro passaggi elencati in precedenza, è possibile rafforzare l'interfaccia seguendo queste cinque linee guida:

-   Usare modelli di schermo coerenti.
-   Fornire schermate per l'avvio delle attività.
-   Rendere evidente come eseguire l'attività con i controlli sullo schermo.
-   Fornire un modo semplice per completare un'attività e avviarne una nuova.
-   Rendere ovvio il passaggio successivo per la navigazione.

### <a name="processes"></a>Processi

Molte attività richiedono agli utenti di spostarsi in una serie di schermate. Un utente che esegue un'attività potrebbe fare clic su un collegamento a un'attività secondaria che si allontana dalla sequenza di schermate che costituiscono l'attività principale. Quando l'utente completa l'attività secondaria, dovrebbe essere disponibile un modo semplice per restituire l'utente direttamente al punto di diramazione nell'attività originale. È probabile che gli utenti abbiano problemi con i controlli di navigazione convenzionali, ad esempio i pulsanti **indietro e indietro** **, per** tornare al punto in cui sono stati avviati.

Per fornire questa capacità, IUI definisce un concetto di spostamento chiamato processo, una schermata o una serie di schermate che eseguono un'attività. Un processo funziona come un tipo di subroutine per la navigazione. Gli utenti possono iniziare un processo, usare la serie di schermate e quindi, nell'ultima pagina, fare clic su un pulsante "fine" per tornare rapidamente alla pagina in cui ha iniziato il processo.

## <a name="steps-for-creating-an-inductive-user-interface"></a>Passaggi per la creazione di un'interfaccia utente indotta

Questa sezione descrive in dettaglio i quattro passaggi che è possibile usare per creare un IUI.

### <a name="step-one-focus-each-page-on-a-single-task"></a>Passaggio uno: concentrare ogni pagina su un'unica attività

Il primo passaggio nella progettazione di un IUI consiste nell'eseguire una funzionalità o un set di funzionalità e suddividerle in schermate separate. Ogni schermata deve essere concentrata su una singola attività, denominata attività principale della schermata.

Questa idea è semplice, ma alcune applicazioni lo seguono. La maggior parte delle applicazioni presenta una schermata da cui vengono eseguite tutte le funzionalità correlate. Questa progettazione richiede agli utenti di individuare (dedurre) le operazioni che possono essere eseguite e come farlo.

L'attività primaria può essere specifica o chiusa. Ad esempio, in un programma di finanza personale, un'attività specifica potrebbe essere "selezionare la fattura che si desidera pagare", mentre un'attività aperta potrebbe essere "esaminare le prestazioni degli investimenti".

L'attività primaria deve essere un elemento che ha senso per l'utente, anziché un riflesso di un dettaglio di implementazione o di un altro concetto astratto. L'attività deve essere qualcosa che gli utenti potrebbero pensare di fare, preferibilmente descritti in parole proprie.

### <a name="example"></a>Esempio

In questa sezione vengono confrontate due diverse versioni di Money. Gli esempi mostrano funzionalità molto simili che consentono agli utenti di visualizzare e gestire gli account finanziari.

Il modello IUI è stato sviluppato durante la creazione di Money 2000, un'applicazione per la gestione delle finanze personali. Money 2000 è l'ottavo rilascio principale del prodotto. Money 2000 è un programma Windows di grandi dimensioni con oltre 1 milione righe di codice.

Money 2000 è un'applicazione Web. Non si tratta di un sito Web, ma condivide molti attributi con i siti Web. L'interfaccia utente è costituita da pagine a schermo intero visualizzate in un frame condiviso, con strumenti per lo spostamento avanti e indietro di uno stack di navigazione. In questa base, Money 2000 aggiunge un set di nuove convenzioni dell'interfaccia utente che creano un'esperienza utente più strutturata.

Anche se IUI è stato usato per la prima volta nella progettazione di tipo Web di Money 2000, può essere usato anche con elementi di interfaccia tradizionali, ad esempio finestre e finestre di dialogo.

In Money 99, gli utenti hanno spesso eseguito una grande varietà di attività in una singola schermata. Ad esempio, lo screenshot seguente mostra l' **account manager** che ha presentato tutte le funzionalità relative agli account in Money 99 in un'unica schermata.

![screenshot della gestione account in Money 99.](images/iuiguidelines02.png)

Questa schermata consente di raggruppare un'attività comune, passando a un account, oltre a attività non frequenti come la creazione e l'eliminazione di account. Nessuna di queste attività specifiche è espressa direttamente nel titolo della schermata, ovvero **account manager**. Molti utenti possono trovare questa schermata come problematica come la finestra di dialogo di esempio nella figura 1. In entrambi i casi, l'utente deve dedurre lo scopo dello schermo e il modo in cui usarlo.

Money 2000, che segue IUI, offre un set pressoché identico di funzionalità relative agli account, ma le fornisce in due schermate separate. Lo screenshot seguente illustra il primo di queste schermate, che è incentrato interamente sull'acquisizione di un account da parte dell'utente.

![screenshot della schermata di selezione dell'account in Money 2000.](images/iuiguidelines03.png)

La schermata Money 2000 contiene approssimativamente lo stesso numero di elementi visivi della schermata precedente Money 99, ma la pagina è ora incentrata interamente sull'acquisizione dell'utente per la selezione di un account. Ad esempio, nella versione Money 99, un utente doveva fare due clic per aprire un account: uno per selezionarlo e un altro per selezionare l'operazione di apertura. Nella versione Money 2000, l'unico motivo per cui un utente fa clic su un account è aprirlo e quindi un solo clic può essere sufficiente. In questo modo, anche se il numero di schermate potrebbe aumentare, il numero di clic necessari per eseguire un'attività comune è spesso ridotto.

In alcuni casi, gli utenti vorranno aggiungere o rimuovere un account. Per eseguire questa attività in Money 2000, gli utenti passano a una seconda schermata, mostrata nella schermata seguente, che si concentra sulla configurazione degli account.

![screenshot della schermata di configurazione dell'account in Money 2000.](images/iuiguidelines04.png)

Lo scopo di ogni schermata è più chiaro nella versione IUI da Money 2000. Inoltre, ogni schermata ha più spazio da dedicare allo scopo di soddisfarne lo scopo. Ad esempio, il gestore di **account** Money 99 potrebbe dare spazio al pulsante **Delete account** , perché è stato usato raramente rispetto agli altri comandi sullo schermo. Al contrario, la schermata di configurazione dell'account in Money 2000 può presentare questo comando in maggiore evidenza, rendendola più individuabile e comprensibile.

### <a name="what-is-a-single-task"></a>Che cos'è una singola attività?

Come è possibile stabilire se una schermata è effettivamente focalizzata su una sola attività? Una schermata che supporta molte attività potrebbe essere spiegata come avente un solo scopo se tale scopo è sufficientemente astratto. Ecco una regola empirica: una schermata si concentra su un solo scopo se la finestra di progettazione è in grado di esprimere tale scopo con un titolo di schermo conciso, significativo e naturale.

I progettisti di Money 2000 consideravano la suddivisione di queste schermate (**Scegli un account da usare** e **Configura gli account in denaro**) in altre schermate. Tuttavia, poiché ogni schermata ha già un titolo conciso, significativo e naturale, le finestre di progettazione credevano che gli schermi fossero abbastanza mirati. Quando si progetta una schermata, se non è possibile considerare un titolo chiaro e semplice, è probabile che si stia tentando di eseguire troppe operazioni sullo schermo.

### <a name="step-two-state-the-task"></a>Passaggio 2: stato dell'attività

Ogni schermata deve essere denominata con un'istruzione concisa ed esplicita dell'attività primaria. Può trattarsi di un'istruzione diretta ("selezionare l'account che si vuole bilanciare") o di una domanda a cui l'utente deve rispondere ("quale account si desidera bilanciare?").

Si tratta di un altro principio semplice che spesso non viene praticato. Ad esempio, le versioni precedenti di Money hanno schermate con titoli come il **responsabile di servizi finanziari online** e l' **account Balance**. Gli utenti dovevano dedurre lo scopo e il comportamento di queste schermate dalla disposizione e dalle etichette dei controlli.

Il titolo della schermata o della pagina è molto importante. Indipendentemente dal fatto che il prodotto usi Windows, pagine Web, finestre di dialogo o un'altra progettazione, non è consentito eseguire lo scorrimento del titolo.

### <a name="usable-screens-have-clear-titles"></a>Schermate utilizzabili con titoli chiari

Le schermate che eseguono molte attività richiedono titoli astratti o complessi. Ad esempio, la schermata Money 99 mostrata nella figura 2 ha consentito all'utente di passare agli account e configurare gli account. Il titolo astratto "account manager" è stato assegnato a questa pagina nel tentativo di acquisire entrambi questi scopi. Sebbene gli utenti possano avere qualche idea sul significato di una pagina di gestione degli account, potrebbero non essere consapevoli che l'attività più comune per questa schermata è semplicemente la scelta di un account.

Alcune schermate o comandi hanno scopi astratti che non suggeriscono prontamente titoli chiari. Per queste schermate, i progettisti possono scegliere nomi deliberatamente vaghi, ad esempio "Impostazioni", come "QuickStep;" o gergo che mostra i dettagli di implementazione ("compattazione del database"). Questi tipi di nomi spesso sono fuorvianti o fuorvianti per gli utenti. Inoltre, tali nomi sono in genere sostantivi che non esprimono l'azione che l'utente desidera eseguire, che aggiunge alla confusione.

I titoli dello schermo e altri nomi spesso non vengono determinati fino alla fine del processo di progettazione. Le finestre di progettazione spesso chiedono ai writer di ottenere un nome adatto per una schermata dopo che è stato progettato e codificato. A questo punto, non è necessario ricorrere se non è possibile trovare un nome valido, quindi il team potrebbe dover definirne i nomi non chiari. La soluzione a questo difetto è che i progettisti considerino la chiarezza nelle funzioni e nei titoli dello schermo nelle prime fasi del processo di progettazione.

Le funzioni e i titoli dello schermo dovrebbero concentrarsi sulle attività più comuni eseguite dai clienti. I progettisti sono spesso tentati di fornire enormi quantità di funzionalità nel tentativo di soddisfare il maggior numero di clienti, insieme ai desideri del team di progettazione. Tuttavia, le funzionalità aggiuntive aggiungono sempre complessità e altri costi.

### <a name="screen-title-indicates-design-clarity"></a>Il titolo della schermata indica chiarezza della progettazione

Nel modello IUI, le finestre di progettazione scelgono i titoli delle schermate nelle prime fasi del processo di progettazione. Anziché selezionare un titolo per giustificare il funzionamento della schermata, il titolo viene usato per determinare se la schermata è sensata. Se non è possibile trovare un titolo appropriato, la funzionalità viene riprogettata. Se nessuna progettazione consente un titolo chiaro e conciso (ovvero se non esiste alcun modo per spiegare la funzionalità), i progettisti potrebbero abbandonare la funzionalità. Nelle schermate seguenti, confrontare la schermata di pagamento della fattura Money 99 sulla sinistra, che fornisce un'etichetta statica per la pagina ("pagamenti imminenti & depositi") e la schermata corrispondente di Money 2000 a destra, che ha un titolo esplicito ("fare clic sulla fattura che si vuole pagare"):

![screenshot che mostra un titolo statico in Money 99 e un titolo attivo in Money 2000.](images/iuiguidelines05.png)

Il titolo di una schermata, ovviamente solo una frase o una frase, è più facile da modificare rispetto a una progettazione o a un codice. Nonostante questo fatto, l'esperienza con IUI ha dimostrato che l'insistere su un titolo di schermo ben presto produce una progettazione migliore. I titoli devono essere scelti con l'input dei membri del team di formazione e di usabilità degli utenti, nonché dei progettisti di prodotti.

I membri del team possono a volte provare a posticipare questa decisione, supponendo che i clienti possano condividere le proprie conoscenze sullo scopo di una schermata. Quando viene richiesto di offrire un resoconto chiaro e conciso di questo scopo, tuttavia, vengono spesso rivelate le differenze di opinione. Risolvendo queste differenze e selezionando un titolo in anticipo, le discussioni di progettazione possono procedere in modo più semplice.

Una volta scelto un titolo, è consigliabile non considerarlo invariato. È probabile che le finestre di progettazione possano perfezionare i titoli dello schermo nel tempo, come per qualsiasi progetto. Tuttavia, il primo titolo scelto deve essere il più forte possibile in tale fase dello sviluppo.

### <a name="guidelines-for-choosing-screen-titles&quot;></a>Linee guida per la scelta dei titoli delle schermate

In questa sezione viene descritta una tecnica semplice per la scelta di titoli di schermo validi. Per usare questa tecnica, i progettisti immaginano un amico che chiede &quot;Qual è questa schermata?&quot; quindi, viene visualizzata una risposta chiara e utile che completa la frase &quot;Questa è la schermata in cui si trova?&quot;. Le parole che completano la frase diventano il titolo dello schermo.

Durante lo sviluppo di Money 2000, i writer della documentazione del team hanno creato le linee guida del titolo dello schermo per garantire la qualità e la coerenza. Ad esempio, queste linee guida suggerivano titoli che usavano verbi e venivano formulate come domande o istruzioni dirette. I progettisti evitavano nomi statici che consentivano una maggiore astrazione e potrebbero essere vaghi.

Per semplificare i titoli, i progettisti evitavano le frasi composte e tentavano di usare il linguaggio colloquiale, evitando termini e gergo. Se le finestre di progettazione non sono in grado di descrivere l'attività senza ricorrere a congiunzioni (&quot;e&quot;, &quot;o"), è probabile che lo schermo tenti di eseguire più di un'attività ed è meno probabile che l'utente possa comprendere immediatamente cosa fare.

Anche quando viene scelto attentamente un titolo, l'area del titolo potrebbe essere troppo piccola per spiegare adeguatamente un'attività complessa. Per ovviare a questo problema, è possibile includere un breve paragrafo descrittivo nella parte superiore dell'area di contenuto della schermata che elabora l'attività.

La tabella seguente contiene alcuni esempi di titoli di schermo in Money 99 e titoli per le stesse schermate o le schermate correlate in Money 2000.



| Titoli dello schermo in Money 99             | Nuovi titoli di schermata in Money 2000                         | Commento                                         |
|---------------------------------------|---------------------------------------------------------|-------------------------------------------------|
| **Gestione account**                   | **Selezionare un account** **configurare gli account**<br/> | Il titolo statico è stato modificato in titoli attivi.          |
| **Dettagli account**                   | **Modificare la configurazione dell'account**                                | Il titolo statico è stato modificato in attivo, titolo specifico. |
| **Calendario pagamenti**                  | **Pagare una fattura**                                          | Titolo vago reso descrittivo.                   |
| **Responsabile servizi finanziari online** |                                                         | Pagina non necessaria dopo la riprogettazione.                 |



 

### <a name="making-the-screen-title-prominent"></a>Rilievo del titolo della schermata

Una volta stabilito un titolo utile per la schermata, è importante assicurarsi che l'attenzione dell'utente sia disegnata su di essa. Alcuni studi hanno dimostrato che gli utenti leggono raramente testo istruttivo. Per ovviare a questo problema, i titoli delle schermate devono essere progettati in modo da essere importanti e accattivanti per attirare l'attenzione dell'utente. La progettazione visiva della schermata deve informare l'utente che il titolo è la cosa più importante da leggere.

### <a name="step-three-make-the-pages-contents-suit-the-task"></a>Passaggio 3: rendere il contenuto della pagina adatto all'attività

Quando si crea un software che segue le linee guida di IUI, il lavoro di progettazione più complesso comporta in genere la suddivisione delle funzionalità in schermate o pagine. Il passaggio successivo consiste nel determinare quali controlli verranno utilizzati in ogni schermata per completare l'attività principale. Questi controlli costituiscono il contenuto della pagina, in cui l'utente ottiene il lavoro eseguito. Il titolo e il contenuto dello schermo sono due metà di un dialogo tra il programma e l'utente. Il titolo pone la domanda del programma o fornisce un'istruzione e l'utente risponde attraverso l'interfaccia dello schermo.

Se il titolo della schermata è chiaro e semplice, la progettazione della schermata è in genere semplice. Ad esempio, una delle schermate di 2000 Money mostrate in precedenza è denominata "selezionare un account da usare". Dato questo titolo, lo schermo dovrebbe ovviamente contenere un semplice elenco di account da cui l'utente può scegliere. Un altro schermo Money 2000 ha il titolo "controllare gli elementi da includere nelle imposte". Naturalmente, questa schermata contiene un elenco di controllo di elementi.

Gli utenti dovrebbero essere in grado di capire facilmente come usare i controlli per ottenere l'attività principale della schermata. Quando agli utenti viene richiesto di selezionare un account e possono esaminare lo schermo per trovare un elenco di account, ne confermano la comprensione. In questo modo si aumenta la probabilità che gli utenti abbiano successo, aumentando così la loro confidenza nell'esecuzione di altre attività.

### <a name="screen-content-areas"></a>Aree del contenuto della schermata

La posizione e la forma esatte delle aree di contenuto della schermata dipendono dalla progettazione del software. In Money 2000, l'area del contenuto della schermata è tutto sotto il titolo dello schermo e a destra dell'elenco attività. Questa area può scorrere su schermi lunghi. Alcuni contenuti non essenziali potrebbero essere visualizzati anche nell'area stato sotto l'elenco attività.

I progettisti possono scegliere di elaborare l'attività principale della schermata in un paragrafo nella parte superiore dell'area del contenuto. Non è mai necessario che gli utenti leggano questo testo, ma possono risultare utili. Molti utenti possono ignorarlo e continuare a usare la schermata. A differenza del titolo, questa descrizione può scorrere se lo schermo è scorrevole. Per ulteriori informazioni, vedere [linee guida per la scelta dei titoli delle schermate](#guidelines-for-choosing-screen-titles).

Se le finestre di progettazione desiderano una pagina per visualizzare promemoria non essenziali, avvisi o altre informazioni sullo stato, possono essere visualizzate a sinistra dell'area del contenuto principale, sotto l'elenco attività sul lato sinistro dello schermo. Dal punto di vista funzionale, questa area di stato è un'area aggiuntiva per il contenuto dello schermo. Questa area non è sufficientemente rilevante per contenere controlli essenziali.

### <a name="provide-a-clear-exit-from-the-page"></a>Fornire un'uscita chiara dalla pagina

Dopo aver completato correttamente un'attività, l'utente deve affrontare un altro problema: quando e come uscire dalla schermata. Per le schermate la cui attività principale è la navigazione, l'esecuzione dell'attività consente di spostare l'utente nella schermata successiva. In altre schermate, potrebbe essere più difficile per l'utente capire come procedere. Ad esempio, in una schermata in cui viene richiesto all'utente di digitare le informazioni nei campi, l'utente potrebbe richiedere assistenza per capire quando e come procedere. In tali pagine, spesso è utile offrire un pulsante Clear **Next** o **done** in una posizione coerente.

Gli studi di usabilità hanno dimostrato che gli utenti preferiscono usare tali pulsanti anche quando i pulsanti di spostamento globali, ad esempio i pulsanti **indietro** o **Home** su una barra degli strumenti, sono disponibili. Spesso gli utenti si trovano a disagio sulle schermate senza alcuna uscita chiara, anche le schermate il cui unico scopo è fornire informazioni da leggere.

Per ulteriori informazioni su questo argomento, vedere [fornire un modo semplice per completare un'attività e avviarne uno nuovo](#provide-screens-for-starting-tasks) nella sezione linee guida aggiuntive.

### <a name="step-four-offer-links-to-secondary-tasks"></a>Passaggio 4: offrire collegamenti a attività secondarie

L'ultimo passaggio nella progettazione di una schermata consiste nel fornire collegamenti alle attività secondarie, ovvero funzionalità che non eseguono direttamente l'attività primaria, ma sono correlate allo schermo. Se, ad esempio, l'attività principale in una schermata consiste nel scrivere una lettera, le attività secondarie su tale schermata potrebbero essere la ricerca di un indirizzo di posta elettronica o la stampa di una busta.

Le attività secondarie potrebbero visualizzare le finestre di dialogo, modificare la presentazione visiva del contenuto della schermata o passare all'utente a una schermata diversa. Un'attività secondaria può eseguire indirettamente l'attività primaria o potrebbe reindirizzare gli utenti perduti al posto in cui si sta cercando.

Se una pagina è una conversazione tra il computer e l'utente, un'attività secondaria consente all'utente di ignorare la domanda del computer e chiedere al computer di eseguire un'altra operazione. Si supponga, ad esempio, che la finestra di dialogo: computer: "quale fattura si desidera pagare?" Utente: "in realtà, quello che voglio fare è trovare una fattura che ho pagato di nuovo".

Alcune schermate del prodotto non avranno attività secondarie, mentre altre ne avranno diverse. È consigliabile evitare di creare un lungo elenco di attività che probabilmente saranno difficili da eseguire per l'analisi da parte dell'utente. Se una schermata dispone di un elenco relativamente lungo di attività secondarie, è consigliabile posizionare prima le attività più comuni, raggruppate in una sezione separata o evidenziate in altro modo visivamente.

L'elenco non deve includere tutte le attività secondarie concepibili, purché sia ovvio il passaggio successivo per la navigazione. Anziché offrire molte attività secondarie, una schermata può fornire attività secondarie che accedono a pagine sussidiarie che elencano più attività.

### <a name="visual-design-of-secondary-tasks"></a>Progettazione visiva delle attività secondarie

Le attività secondarie devono essere elencate in una posizione subordinata sullo schermo, in cui sono accessibili, se necessario, ma non distraggono l'utente dall'attività primaria. L'inserimento di questo elenco in una posizione coerente in ogni schermata consente agli utenti di trovare rapidamente l'elenco quando necessario.

Se si visualizza l'elenco delle attività secondarie sul lato sinistro dello schermo, l'elenco non deve essere scorrevole, né deve mai scorrere con la pagina, come illustrato nella schermata seguente della **fattura di pagamento della fattura** da Money 2000.

![screenshot della schermata di fatturazione con pagamento in denaro 2000.](images/iuiguidelines07.png)

## <a name="additional-guidelines"></a>Linee guida aggiuntive

Questa sezione descrive cinque utili linee guida per la creazione di un IUI in base ai quattro passaggi descritti nella sezione precedente.

### <a name="use-consistent-screen-templates"></a>Usare modelli di schermo coerenti

Quando si progetta il software che segue il modello IUI, è necessario creare un modello da utilizzare come guida per ogni schermata. Il modello induttivo non impone l'uso di un modello particolare. Esistono diverse possibili varianti che possono soddisfare una progettazione indotta. Il prodotto potrebbe richiedere un solo modello per tutte le schermate oppure è possibile creare più modelli diversi per vari scopi.

Un modello valido consente a un nuovo utente di comprendere rapidamente il funzionamento delle schermate del prodotto. L'uso coerente del modello nelle schermate del prodotto fornisce un flusso di interfaccia utente efficace da schermo a schermo. Man mano che gli utenti imparano a prevedere che gli stessi elementi vengano visualizzati nello stesso luogo, possono analizzare e iniziare a usare ogni nuova schermata più rapidamente.

### <a name="provide-screens-for-starting-tasks"></a>Fornire schermate per l'avvio di attività

I prodotti progettati con IUI spesso usano schermate speciali progettate per avviare utenti su set di attività. Queste schermate vengono denominate pagine di attività perché consentono di organizzare gruppi correlati di attività comuni. Le pagine attività rappresentano un punto di partenza per gli utenti. In genere, una pagina di attività presenta collegamenti ad altre pagine in cui l'utente ottiene effettivamente il lavoro. Le pagine attività chiedono all'utente "che cosa si vuole fare ora?" e presentano un elenco di possibili risposte. Le pagine attività possono seguire un modello speciale per consentire agli utenti di riconoscerle.

Una pagina attività rende una pagina iniziale predefinita per un prodotto. Quando gli utenti avviano un'applicazione, in genere hanno un'idea dell'attività che desidera eseguire. In genere, il motivo per cui si avvia il prodotto è costituito da un numero ridotto di attività molto comuni. La pagina iniziale predefinita del prodotto riconosce questo aspetto rendendo ovvio come iniziare le attività comuni.

La **Home** page di Money 2000 è un esempio di pagina di attività. Per impostazione predefinita, gli utenti visualizzano questa schermata, in cui l'accesso a attività finanziarie comuni come il pagamento di una fattura e il bilanciamento di un account viene visualizzato quando avviano l'applicazione.

La schermata seguente mostra la **Home** page di Money 2000.

![screenshot del home page Money 2000. pagina attività in cui sono elencate alcune attività comuni e vengono forniti collegamenti a set di attività in altre pagine.](images/iuiguidelines08.png)

Poiché Money fornisce molte funzionalità finanziarie, solo le attività finanziarie più comuni si adattano alla **Home** page. Per tutte le altre attività, la **Home** page si collega a un set di pagine di attività secondarie denominato Financial Center. Ogni area principale del denaro fornisce un centro finanziario. Queste schermate presentano il livello successivo di attività, che funge da punto di partenza per tutte le funzionalità all'interno di ogni area.

Ad esempio, l'area tasse monetarie contiene le funzionalità relative alle **imposte** del prodotto. L'area **tasse** offre collegamenti a queste funzionalità in una pagina del **centro fiscale** , come illustrato nella schermata seguente.

![screenshot della pagina del centro fiscale 2000 Money. ](images/iuiguidelines09.png)

Una pagina di attività può anche essere molto più semplice se sono disponibili meno opzioni. Lo screenshot seguente mostra come è possibile usare una pagina di attività per la gestione degli account utente di Windows.

![Screenshot di una pagina di attività Money 2000 per la gestione degli account utente di Windows. ](images/iuiguidelines10.png)

### <a name="make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen"></a>Rendere evidente come eseguire l'attività con i controlli sullo schermo

Il modo migliore per seguire questa linea guida è scegliere un titolo dello schermo appropriato e limitare l'ambito delle attività primarie solo ai più comuni. Una volta ottenuto un titolo e una finalità chiare per la pagina, la scelta del set di controlli più appropriato sarà semplice.

### <a name="provide-an-easy-way-to-complete-a-task-and-start-a-new-one"></a>Fornire un modo semplice per completare un'attività e avviarne una nuova

L'ultimo ostacolo che un utente deve affrontare sullo schermo è capire quando e come uscire. L'utente in genere lascia lo schermo facendo clic su un collegamento o eseguendo un comando che passa a un'altra schermata. Questi collegamenti possono essere visualizzati nell'area del contenuto della schermata, nell'elenco attività o nelle barre degli strumenti di navigazione. Gli utenti possono anche lasciare una schermata chiudendo il file corrente o l'applicazione stessa.

L'attività in alcune schermate prevede la preparazione di un'operazione che l'utente deve confermare o annullare. Tali schermate in genere offrono un solo collegamento che esegue ed esegue il commit dell'operazione e un altro collegamento che Annulla. Se l'utente ignora queste opzioni e fa clic su un altro collegamento, il programma deve eseguire l'opzione meno distruttiva. Le schermate devono indicare che cosa accadrà se l'utente accetta questo percorso. È possibile formulare i collegamenti per renderli più evidenti. Un pulsante di commit denominato "Save Changes", ad esempio, implica che le modifiche apportate sullo schermo diverranno effettive solo dopo aver fatto clic sul pulsante.

Anche se gli utenti possono lasciare ogni volta che desiderano, potrebbe essere comunque disponibile un collegamento che suggerisce un'uscita ovvia dalla pagina. Lo stesso vale per le pagine che visualizzano semplicemente informazioni statiche. Per ulteriori informazioni su questo argomento, vedere la sezione [fornire un'uscita chiara dalla pagina](#provide-a-clear-exit-from-the-page).

### <a name="starting-and-completing-processes"></a>Avvio e completamento dei processi

Ai fini di questo articolo, i processi sono tecniche per la gestione delle attività che consentono all'utente di usare più di una schermata.

Si supponga che un utente faccia clic su un collegamento nel contenuto o nell'elenco di attività di una schermata e venga visualizzata in un'altra schermata. Questa pagina a sua volta potrebbe essere la prima di una serie di schermate che realizza un risultato complessivo. Alla fine di questa serie di schermate, l'utente desidera tornare alla schermata che precedeva il processo. Sono disponibili almeno due modi per tornare all'utente? fare clic ripetutamente sul pulsante indietro o tornare alla home page e spostarsi da questa posizione? nessuno di questi metodi è però ovvio o naturale. La maggior parte degli utenti si aspettano di trovare un pulsante nella schermata finale che li restituisce direttamente alla schermata originale.

Il modello IUI supporta questo scenario tramite il concetto di un processo, una schermata o una serie di schermate trattate come unità di navigazione. Gli utenti possono immettere il processo, lavorare attraverso le schermate e, nell'ultima schermata, trovare un pulsante che li restituisce alla posizione in cui sono stati avviati. In particolare, l'utente può avviare il processo da più posizioni nel prodotto. Gli utenti vengono sempre restituiti al posto in cui hanno iniziato a prescindere da dove si trovavano quando hanno iniziato il processo.

### <a name="process-name"></a>Nome del processo

A ogni processo deve essere assegnato un nome e il nome deve essere visualizzato in un punto qualsiasi della schermata del processo. Money 2000 utilizza questo approccio. Ogni schermata che fa parte di un processo generale include il nome del processo lungo la parte superiore. Questo nome di processo viene visualizzato in modo meno evidente rispetto al titolo univoco della schermata perché è meno importante. Il nome del processo ricorda agli utenti il processo che esegue e rafforza la nozione che tutte le schermate del processo fanno parte di una singola funzionalità. Ad esempio, l'area delle **imposte monetarie** include un processo di **stima dell'imposta** che si estende su più schermate. In ogni schermata di questo processo vengono visualizzati il nome del processo collettivo e il relativo titolo univoco dello schermo.

### <a name="implementation-of-processes"></a>Implementazione di processi

Lo stesso processo può essere avviato da diversi collegamenti su schermate diverse e gli utenti verranno sempre restituiti alla pagina iniziale corretta. Questo comportamento non può essere eseguito tramite un collegamento hardcoded nella schermata finale del processo, perché la destinazione del collegamento può variare. Al contrario, l'applicazione può implementare questo comportamento gestendo uno stack di processi attivi, indipendentemente dallo stack di navigazione normale utilizzato dai comandi **indietro** e **in** secondo piano. Quando l'utente avvia un processo, viene effettuato il push della schermata di avvio nello stack di processi. Quando l'utente fa clic sul pulsante **fine** nella schermata finale del processo, l'applicazione apre la schermata di avvio più recente dallo stack e restituisce l'utente a tale schermata.

Quando gli utenti si spostano fuori da una schermata di un processo, il processo rimane attivo nello stack di processi. Gli utenti possono completare il processo di backup sullo schermo in cui sono rimasti e continuare. Ciò consente agli utenti di eseguire una deviazione, eseguire il backup e quindi procedere con il processo. Per verificare il funzionamento di questo comportamento, avviare qualsiasi processo di shopping online nella World Wide Web, lasciare il sito, quindi fare clic sul pulsante **indietro** . Sarà in genere possibile scegliere il punto in cui si è interrotto.

### <a name="done-button"></a>Pulsante Fine

Per completare una schermata e passare alla schermata successiva del processo, le schermate possono visualizzare un pulsante nella parte inferiore della pagina. L'etichetta di questo pulsante è "Avanti", "completato" o qualcosa di simile. Se il pulsante Termina il processo e il processo può essere chiamato da più posizioni, la didascalia del pulsante **done** può includere il nome della posizione chiamante.

### <a name="navigation-bar"></a>Barra di navigazione

In qualsiasi schermata, gli utenti potrebbero decidere di aver terminato l'area corrente del prodotto e di voler iniziare un'altra operazione. È possibile che non si desideri completare in modo esplicito la schermata corrente prima di procedere a un'altra parte del prodotto. Una barra degli strumenti di navigazione può offrire all'utente un set di collegamenti per l'avvio di nuove attività. Come per gli altri elenchi di collegamenti alle attività, questi devono seguire il principio di rendere ovvio il passaggio successivo per la navigazione, descritto in dettaglio nella sezione seguente.

### <a name="make-the-next-navigational-step-obvious"></a>Rendere ovvio il passaggio successivo per la navigazione

Pochi programmi possono rendere disponibili tutte le funzionalità contemporaneamente. In genere, gli utenti devono spostarsi in un programma per trovare una funzionalità specifica. Gli utenti hanno più successo durante la navigazione se possono vedere facilmente come ottenere almeno un passaggio più vicino al risultato desiderato. Le schermate che usano IUI sono progettate tenendo presente questo principio.

Ad esempio, le pagine di attività non visualizzano necessariamente tutte le attività o destinazioni che l'utente potrebbe desiderare di ottenere da tale punto. Al contrario, le pagine attività forniscono un elenco delle attività sufficientemente complete in modo che gli utenti possano determinare facilmente il collegamento appropriato da fare clic, anche se vengono configurate solo in un'altra pagina di collegamenti. Le attività più frequenti dovrebbero essere più importanti e richiedere la minima quantità di navigazione. Le attività meno frequenti possono richiedere più passaggi.

Di seguito è riportato un esempio di Money 2000. Si supponga che gli utenti desiderino eseguire un'operazione solo occasionalmente, ad esempio il controllo dell'importo stimato del pagamento fiscale del reddito dell'anno successivo. Per prima cosa, gli utenti iniziano a cercare questa funzionalità nella Home page di Money 2000. Poiché la funzionalità non viene visualizzata nell'elenco delle attività comuni, è necessario eseguire la scansione dell'elenco di aree finanziarie. L'area delle **imposte** sembra promettente, quindi fa clic su di essa. La pagina del **centro fiscale** contiene un collegamento alla funzionalità di stima fiscale che sta cercando, quindi fare clic su di essa e completare l'attività. Applicando principi IUI, Money 2000 consente agli utenti di trovare in modo intuitivo ciò che cercano.

## <a name="user-assistance"></a>Assistenza utenti

Questa sezione descrive un set di linee guida consigliate per l'integrazione del testo di assistenza utente in un prodotto che usa IUI.

Per assistenza primaria si intende tutto il testo visibile sullo schermo, come illustrato nella schermata seguente. L'assistenza principale fornisce indizi testuali mirati alle attività, in modo che gli utenti possano facilmente comprendere tutte le informazioni presentate sullo schermo. Comprendono lo scopo della pagina e il modo in cui gli oggetti sono correlati tra loro per consentire l'esecuzione delle attività. Poiché il testo è direttamente sullo schermo, le informazioni che rispondono a domande di novizio come "cosa devo fare?" è facile da accedere e altamente visibile senza che l'utente debba eseguire alcuna azione.

![screenshot della schermata di configurazione dell'account Money 2000.](images/iuiguidelines11.png)

L'assistenza secondaria è costituita da tutto il testo non visibile sullo schermo e richiede l'intervento dell'utente per l'accesso, ad esempio il clic o il passaggio del mouse su un elemento dell'interfaccia utente. Questo contenuto non è essenziale per eseguire l'attività a disposizione, ma è ancora direttamente correlato.

### <a name="primary-assistance"></a>Assistenza primaria

L'assistenza primaria può includere alcuni o tutti i componenti seguenti:

-   Titolo della schermata

    Esempio: modificare l'immagine

    Il titolo della schermata è il primo e l'elemento più importante visualizzato sullo schermo. Lo scopo è quello di descrivere nella lingua dell'utente l'attività che può essere completata in questa pagina. Il titolo della schermata deve evitare di descrivere i dettagli del completamento dell'attività. Il testo nel titolo della schermata dovrebbe fare riferimento solo all'attività principale della schermata. Come regola empirica, più semplice e più breve è la descrizione dell'attività, più è probabile che l'attività venga definita. Per informazioni più dettagliate su questo argomento, vedere passaggio due: [stato dell'attività](#step-two-state-the-task).

-   Sottotitolo schermata

    Esempio: è anche possibile scaricare una nuova immagine da Internet.

    Anche con un'attenta attività, il titolo della schermata potrebbe non essere sufficiente per spiegare adeguatamente un'attività complessa. Il sottotitolo consente di elaborare lo scopo dello schermo. È possibile utilizzare un sottotitolo per chiarire lo scopo della pagina, fornire una descrizione dell'attività aggiuntiva o impostare le aspettative. Gli utenti che non leggono il sottotitolo dovrebbero essere in grado di utilizzare correttamente la pagina. Analogamente al titolo, il sottotitolo deve evitare di descrivere i dettagli per il completamento dell'attività.

-   Attività

    Esempio: modificare il screen saver

    Le attività possono essere presentate come collegamenti di testo o immagini grafiche che richiedono l'interazione dell'utente. I comandi presentati come collegamenti di testo devono essere basati su verbi e scritti come attività chiare e concise.

-   Etichette per i pulsanti di comando

    Esempio: create password

    Sono disponibili tre tipi di pulsanti di comando:

    -   Annulla
    -   Fine
    -   Commit

    I pulsanti Annulla e fine utilizzano semplicemente le etichette "Annulla" e "completato". I pulsanti commit devono usare etichette di testo attive anziché "OK". Ad esempio, usare "Crea password" invece di "OK".

-   Etichette per altri controlli

    Esempio: digitare la password

    Le etichette per controlli quali pulsanti di opzione, caselle di controllo e caselle di testo devono essere scritte in modo chiaro e conciso, in modo che gli utenti sappiano esattamente quali sono i controlli per, quali sono le informazioni da usare e quali informazioni devono essere fornite per completare l'attività.

-   Collegamenti "Related Tasks"

    Esempio: attività correlate-modificare un altro account

    I collegamenti "Related Tasks" sono punti di ingresso espliciti ad altre attività correlate alla funzionalità corrente. Devono essere scritti come collegamenti basati su attività.

-   Collegamenti "vedere anche"

    Esempio: vedere anche modificare il tema

    I collegamenti "vedere anche" sono attività secondarie. Questi sono correlati all'attività principale, ma l'utente esce dal contesto corrente. Questi devono essere visualizzati come collegamenti normali delle attività. Per ulteriori informazioni sulle attività secondarie, vedere la pagina relativa alla [progettazione visiva delle attività secondarie](#visual-design-of-secondary-tasks).

### <a name="secondary-assistance"></a>Assistenza secondaria

L'assistenza secondaria può includere alcuni o tutti i componenti seguenti:

-   Infotip

    È possibile usare un InfoTip per fornire all'utente informazioni aggiuntive su un collegamento a un'attività o un pulsante di comando. Ad esempio, un InfoTip su un collegamento all'attività potrebbe leggere ", Visualizza una pagina in cui è possibile selezionare un'immagine da usare con l'account." Il InfoTip viene visualizzato quando l'utente posiziona il puntatore del mouse sull'oggetto associato. È necessario creare infotip per tutti gli elementi dell'interfaccia utente che l'utente può fare clic.

-   Argomenti della Guida di "informazioni su"

    Esempio: informazioni su-download di un file

    I collegamenti "informazioni su" aprono gli argomenti della guida, ad esempio panoramiche sulle funzionalità, informazioni concettuali, informazioni di supporto e informazioni sulle procedure. Per ridurre il disordine, è necessario ridurre al minimo il numero di argomenti della Guida "informazioni su" disponibili sullo schermo.

## <a name="appendix-designing-and-testing-microsoft-money-2000"></a>Appendice: progettazione e test di Microsoft Money 2000

Questa sezione è stata adattata in base alle descrizioni della prima parte dei progettisti. Viene illustrato il modo in cui il team Money 2000 ha modificato il processo di progettazione e test per adattarsi al modello IUI.

### <a name="designing-and-testing-money-2000"></a>Progettazione e testing di Money 2000

La progettazione di Money 2000 usando il modello di navigazione induttivo ha portato il team a interrogare i progetti che erano stati nel prodotto per molto tempo. Poiché i principi del modello sono semplici, è facile adottare il modello nel processo di progettazione e mantenerlo. Alla fine, le finestre di progettazione ritengono che il modello abbia contribuito a migliorare le progettazioni che avrebbero potuto produrre senza di esso.

### <a name="clearer-titles-and-designs"></a>Progetti e titoli più chiari

I progettisti di Money 2000 hanno notato che spesso descrivono le funzionalità usando parole che non erano effettivamente visualizzate sullo schermo. Nel modello IUI le schermate dovrebbero spiegarsi autonomamente. Ad esempio, il team ha spiegato che la schermata relativa al **calendario di pagamento** è stata progettata per pagare le fatture. In Money 2000, questa schermata è denominata **pay fattura**. Tutti gli elementi non correlati a tale scopo sono stati spostati in schermate secondarie, ottenendo una progettazione più chiara.

Un altro esempio prevede una schermata denominata **responsabile servizi finanziari online**. Il team ha faticato a trovare una semplice spiegazione dello scopo di questa schermata. Quando non è stato possibile arrivare a un oggetto, questa schermata è stata rimossa e ne sono state distribuite le funzionalità tra pagine più definite in modo logico.

### <a name="helping-new-designers"></a>Supporto per nuove finestre di progettazione

Il team ha scoperto che è facile insegnare le tecniche di progettazione di IUI a nuovi progettisti software inesperti. Le tecniche hanno consentito ai progettisti a tutti i livelli di esperienza di valutare le proprie progettazioni usando i titoli delle schermate come test di chiarezza. Quando è forzato a inserire un titolo chiaro e conciso su uno schermo progettato in modo non corretto, i progettisti hanno riconosciuto rapidamente che nessun titolo era sufficiente per la pagina. Si è reso conto che il problema si è cercato di non dover scegliere parole per un titolo, bensì in una progettazione schermata difettosa. Con questa comprensione, potranno quindi riprogettare lo schermo per supportare un'interazione utente più chiara e, di conseguenza, un titolo più chiaro.

### <a name="including-writers"></a>Inclusione di writer

Con l'avanzamento della progettazione, il team si è reso conto che i writer e gli editor della documentazione dovrebbero essere necessari per creare i titoli delle schermate. I writer erano limitati alla possibilità di scegliere titoli efficaci nelle versioni precedenti perché erano interessati solo a una fase tardiva. Nelle schermate vengono in genere assegnati titoli di lavoro temporanei da designer o programmatori. Questi titoli venivano usati fino a tardi nel ciclo del prodotto quando venivano richiesti ai writer per ottenere i titoli finali dello schermo. A questo punto, era troppo tardi per rielaborare schermate progettate in modo non corretto.

Al contrario, il team Money 2000 ha partecipato ai writer nelle prime fasi del processo di progettazione. Ciò ha portato un prezioso input sui titoli dello schermo quando poteva ancora aiutare la progettazione. Se una schermata era troppo complessa per consentire un titolo chiaro, i writer potevano suggerire che la pagina venisse riprogettata.

Alla fine del progetto, i writer e i progettisti credevano che i titoli dello schermo fossero più chiari e più efficaci rispetto alle versioni precedenti. I writer ritenevano inoltre più semplice spiegare le nuove pagine, semplificando il processo di documentazione del prodotto. Tutti i membri del team ritenevano che interessassero tutte le discipline della fase di progettazione rendevano il prodotto migliore e più semplice da usare.

### <a name="usability-tests"></a>Test di usabilità

Durante lo sviluppo di Money 2000, il team ha condotto diversi test di usabilità per esaminare le differenze tra la struttura di spostamento precedente di Money 99 e le modifiche apportate in seguito all'applicazione del modello IUI.

### <a name="prototype-testing"></a>Test del prototipo

Nelle fasi iniziali del processo di sviluppo del prodotto, i progettisti hanno creato un prototipo per esplorare il modo in cui gli utenti reagiranno a IUI. Questa operazione è stata eseguita molto presto nel processo di sviluppo per consentire al tempo di affinare i principi del modello prima che i programmatori iniziassero a eseguire la revisione del prodotto stesso.

Il team ha creato un prototipo in Microsoft Visual Basic e HTML che simulava le attività finanziarie personali normalmente eseguite in denaro. Nel prototipo gli utenti potevano passare a più di 50 pagine che rappresentano le aree principali del prodotto. In queste aree, è possibile configurare account finanziari, pagare fatture, visualizzare report e collaborare con gli investimenti.

Undici partecipanti hanno eseguito lo stesso set di attività sia in Money 99 che nel prototipo IUI. Sono stati assegnati in modo casuale per utilizzare prima uno dei prodotti. Quattro partecipanti erano gli attuali utenti Money, quattro erano utenti correnti di un prodotto concorrente e tre non hanno mai usato un prodotto Finance personale prima.

Le preferenze generali indicano che i quattro utenti correnti di Money hanno preferito il prezzo 99 (la versione usata a casa) mentre gli altri sette utenti hanno preferito il nuovo prototipo alla versione corrente. Per tutte le altre misure, non esiste alcuna differenza tra gli utenti dei tre gruppi. In termini di prestazioni complessive, gli utenti si trovavano nell'area sbagliata del prodotto il doppio delle volte usando i costi 99 (2,82 volte per attività) come nel prototipo (1,45 volte per attività). Altre misure relative a dati e prestazioni, anche se non significative, sembrano favorire il prototipo. In base a questi dati e ad altri test, il team del prodotto Money ha deciso di incorporare i principi IUI in Money 2000.

### <a name="product-testing"></a>Test del prodotto

Una volta completata la maggior parte del codice per il prodotto, il team ha eseguito un altro studio sull'usabilità per esaminare l'implementazione finale di IUI. In questo test sono stati selezionati 10 partecipanti che non hanno mai usato un prodotto Finance personale prima di usare Money 99 o Money 2000. Tutti gli utenti hanno eseguito le stesse attività.

Gli utenti di Money 2000 hanno completato il 89% delle attività, mentre gli utenti di Money 99 sono riusciti a completare solo il 74% delle attività. Come per il prototipo, anche gli utenti sembrano essere più rapidi, ma non significativamente diversi, alla navigazione in denaro 2000 rispetto a Money 99. Inoltre, le misure generali di soddisfazione soggettiva per la navigazione tendono a essere più elevate per il denaro 2000 rispetto a quello per Money 99.

### <a name="controlled-testing"></a>Test controllati

Poiché Money 2000 è enorme e complesso, non è particolarmente adatto per condurre esperimenti controllati sugli effetti dell'applicazione di IUI. Al contrario, il team ha creato un ambiente più vincolato per il test.

Il test ha richiesto un'applicazione "Stock Market Viewer" che consentiva agli utenti di modificare la visualizzazione di un report sul mercato azionario visualizzato sullo schermo. Gli utenti potrebbero modificare le colonne di dati incluse nel report, l'ordine delle colonne del report, l'allineamento e il numero di posizioni decimali utilizzate. I progettisti volevano vedere in che modo un approccio IUI a questa attività verrebbe eseguito rispetto a un'interfaccia utente grafica convenzionale.

Lo screenshot seguente mostra l'interfaccia utente convenzionale usata nel test. Una singola finestra di dialogo esegue tutte le attività di personalizzazione del report. Molte applicazioni forniscono una finestra di dialogo simile per la selezione di un subset da un elenco di elementi. Nella finestra di dialogo sono contenuti due elenchi: nell'elenco a sinistra vengono visualizzate tutte le colonne del report disponibili, mentre a destra viene visualizzato il subset di colonne selezionate dall'utente per il report. Altri controlli modificano gli attributi di ordine e formattazione per le colonne del report selezionate nell'elenco a destra.

![Screenshot di una finestra di dialogo convenzionale.](images/iuiguidelines12.png)

Per la versione IUI di questa attività, il team ha creato un'applicazione Web. Ogni attività di personalizzazione è stata inserita in una pagina separata. Nell'applicazione è inclusa anche una pagina principale, mostrata nella schermata seguente, in cui viene chiesto agli utenti come desiderano personalizzare il report.

![Screenshot di una schermata di test di Iui.](images/iuiguidelines13.png)

Quando si fa clic sui collegamenti in questa pagina principale, l'utente viene aggiunto ad altre pagine per eseguire specifiche attività di personalizzazione. Ad esempio, lo screenshot seguente mostra la pagina utilizzata per selezionare le colonne del report.

![Screenshot di una schermata di test di Iui per la selezione delle colonne del report.](images/iuiguidelines14.png)

Nei test di entrambe le versioni, agli oggetti è stato richiesto di personalizzare i report da uno stato di avvio specifico (visualizzato sullo schermo) a uno stato obiettivo specificato (visualizzato in una carta stampata). Il computer tiene traccia della quantità di tempo e del numero di tentativi eseguiti per personalizzare il report. Il computer ha informato gli utenti quando il report è stato personalizzato correttamente.

Il test includeva 88 partecipanti. A ogni partecipante è stato richiesto di personalizzare un set di 11 report con una delle due versioni dell'applicazione. Inoltre, 72 di questi partecipanti hanno restituito una settimana dopo per personalizzare un altro set di 11 report che usano la stessa versione della prima sessione. Ogni soggetto è stato classificato come utente del computer novizio, principalmente utilizzando il computer per la posta elettronica, giocando a solitario e navigando il Web.

Non vi sono differenze significative tra gli utenti delle due versioni o qualsiasi altra variabile di interesse. Gli utenti hanno eseguito attività alla stessa velocità, hanno eseguito l'iterazione sull'attività lo stesso numero di volte e hanno avuto le stesse valutazioni generali di soddisfazione soggettiva per le due versioni. Questo test, quindi, non è riuscito a visualizzare le misure in cui IUI ha prodotto un miglioramento o una riduzione delle prestazioni o delle valutazioni soggettive.

Si potrebbe affermare che se l'utente deve spostarsi più per eseguire l'attività, la quantità di tempo per l'esecuzione dell'attività deve essere maggiore. Sebbene questo esperimento non suggerisca questo risultato, è importante notare che i tempi di prestazioni medi e le deviazioni standard associate per i due diversi approcci a questa attività erano quasi identici.

Ulteriori ricerche saranno necessarie per determinare se sono presenti miglioramenti misurabili dall'uso di IUI. Almeno, questo test non ha fornito alcuna evidenza che IUI danneggi le prestazioni o l'utilizzo del prodotto.

### <a name="comparison-with-web-sites"></a>Confronto con siti Web

Molti siti web ben progettati usano principi simili al modello IUI descritto in questo documento. Si tratta probabilmente di un effetto collaterale della modalità di funzionamento del Web. Poiché è difficile implementare interazioni complesse tra i controlli in una singola pagina Web, le finestre di progettazione spesso interrompono le attività in parti che coinvolgono più di un viaggio al server per ottenere una nuova pagina. Alcuni siti includono anche titoli di pagina che indicano chiaramente lo scopo della pagina.

I progettisti di applicazioni tradizionali hanno un set di strumenti più completo. Questo offre una maggiore flessibilità, ma offre anche maggiori opportunità per creare pagine complesse e confuse. Quando si creano interfacce utente indotte, le finestre di progettazione devono usare questa potenza a discrezione e ricordarsi di chiarezza e semplicità dei valori.

 

 





