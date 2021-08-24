---
title: Induttivi Interfaccia utente
description: Questo argomento descrive il modello di interfaccia utente noto come interfaccia utente induttiva (IUI).
ms.assetid: d99dc30a-68e5-4b7a-8cbd-0ac77a90a354
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a16282248e1942070f5dc3e1418016657de2e84f39e1f8473eaedcbc0eeccbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589429"
---
# <a name="inductive-user-interface"></a>Induttivi Interfaccia utente

Questo argomento descrive il modello di interfaccia utente noto come interfaccia utente induttiva (IUI). Detto anche navigazione induttiva, il modello IUI suggerisce come semplificare le applicazioni software suddividendo le funzionalità in schermate o pagine facili da spiegare e comprendere. Questo modello IUI è evidente in diversi progetti Microsoft, ad esempio Microsoft Money 2000, le applet del pannello di controllo di Windows, varie schermate e finestre di dialogo in Microsoft Visual Studio 2010 e i pannelli attività in Microsoft Office.

-   [Introduzione](#introduction)
-   [IUI in azione: Risoluzione di un problema di progettazione comune](#iui-in-action-solving-a-common-design-problem)
    -   [Il problema: il software è difficile da usare](#the-problem-software-is-hard-to-use)
    -   [Interfaccia utente deducibile](#deductive-user-interface)
    -   [Una soluzione: Interfaccia utente](#a-solution-inductive-user-interface)
-   [Passaggi per la creazione di un Interfaccia utente](#steps-for-creating-an-inductive-user-interface)
    -   [Passaggio 1: Concentrare ogni pagina su una singola attività](#step-one-focus-each-page-on-a-single-task)
    -   [Passaggio 2: Stato dell'attività](#step-two-state-the-task)
    -   [Passaggio 3: Adattare il contenuto della pagina all'attività](#step-three-make-the-pages-contents-suit-the-task)
    -   [Passaggio 4: Offrire collegamenti ad attività secondarie](#step-four-offer-links-to-secondary-tasks)
-   [Linee guida aggiuntive](#additional-guidelines)
    -   [Usare modelli di schermata coerenti](#use-consistent-screen-templates)
    -   [Rendere evidente come eseguire l'attività con i controlli sullo schermo](#make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen)
    -   [Fornire un modo semplice per completare un'attività e avviarne una nuova](#provide-screens-for-starting-tasks)
    -   [Rendere ovvio il passaggio di spostamento successivo](#make-the-next-navigational-step-obvious)
-   [Assistenza per l'utente](#user-assistance)
    -   [Assistenza principale](#primary-assistance)
    -   [Assistenza secondaria](#secondary-assistance)
-   [Appendice: Progettazione e test di Microsoft Money 2000](#appendix-designing-and-testing-microsoft-money-2000)
    -   [Progettazione e test di Money 2000](#designing-and-testing-money-2000)
    -   [Test di usabilità](#usability-tests)
    -   [Confronto con siti Web](#comparison-with-web-sites)

## <a name="introduction"></a>Introduzione

IUI è un modello di interfaccia utente che suggerisce come semplificare le applicazioni software suddividendo le funzionalità in schermate o pagine facili da spiegare e comprendere. Microsoft ha implementato questo modello in Money 2000, un'applicazione software commerciale di grandi dimensioni. I test informali suggeriscono che gli utenti possono eseguire attività con la rapidità di questo modello come nelle interfacce tradizionali e possono trovare le cose più facilmente.

Molte applicazioni software commerciali includono interfacce utente in cui una schermata presenta un set di controlli, ma lascia all'utente di dedurre lo scopo della pagina e come usare i controlli a tale scopo.

I principi descritti in questo documento non richiedono o implicano particolari set rigidi di progettazioni, controlli o elementi visivi. Come le interfacce utente grafiche in generale, i principi di questo documento lasciano molto spazio per la flessibilità e la creatività nella progettazione.

I principi generali dell'interfaccia utente induttiva sono illustrati con esempi tratti da Money 2000.

> [!IMPORTANT]
> Il concetto generale di IUI è infancy. I progettisti che usano queste tecniche apprendono e scoprono di più su di essa quando la usano per il software. Le informazioni contenute in questo documento evolveranno nel tempo con l'aumentare delle conoscenze e delle ricerche in quest'area. In questo argomento viene fornita un'introduzione all'interfaccia utente di , anziché a un set completo di linee guida.

 

## <a name="iui-in-action-solving-a-common-design-problem"></a>IUI in azione: Risoluzione di un problema di progettazione comune

Questa sezione illustra un problema di progettazione comune con i prodotti software attuali e introduce l'interfaccia utente grafica come tecnica per il superamento del problema.

### <a name="the-problem-software-is-hard-to-use"></a>Il problema: il software è difficile da usare

La maggior parte del software è troppo difficile da usare. Questa conclusione è tratta da test di usabilità, prove aneddotiche ed esperienze personali dei progettisti di software. Il concetto di IUI è stato creato effettuando ricerche, facendo ipotesi informate su ciò che rende il software corrente difficile da usare e quindi proponendo soluzioni. I progettisti che usano IUI devono basarsi sulla soddisfazione dei clienti per determinare il successo finale della progettazione.

La maggior parte dei prodotti software correnti è difficile da usare per i motivi generali seguenti:

-   Gli utenti non sembrano costruire un modello psichiale adeguato del prodotto.

    La progettazione dell'interfaccia per i prodotti software più attuali presuppone che gli utenti comprenderanno un modello concettuale creato con attenzione dagli sviluppatori. Sfortunatamente, la maggior parte degli utenti non sembra mai acquisire un modello psichiale sufficientemente accurato da guidare la navigazione. Questi utenti sono probabilmente molto occupati e sovraccarichi di informazioni. Non hanno tempo, energia o vogliano studiare un modello concettuale per il software.

-   Anche molti utenti di lunga data non sono mai esperti di procedure comuni.

    I progettisti sanno che i nuovi utenti potrebbero avere problemi all'inizio, ma si aspettano che questi problemi scompartino quando gli utenti apprendono attività comuni. I dati di usabilità indicano che questo spesso non si verifica. In uno studio, i ricercatori hanno configurato apparecchiature automatizzate per videotapeare gli utenti a casa. I nastri hanno dimostrato che gli utenti che si concentrano sull'attività a portata di mano non notano necessariamente la procedura che stanno seguendo e non apprendono dall'esperienza. La volta successiva che gli utenti eseguono la stessa operazione, è possibile che la attraversano esattamente nello stesso modo.

-   Gli utenti devono lavorare sodo per capire ogni funzionalità o schermata.

    La maggior parte dei prodotti software è progettata per (i pochi) utenti che ne comprendono il modello concettuale e hanno procedure comuni ben progettate. Per la maggior parte dei clienti, ogni funzionalità o procedura è frustrante e indesiderato. Gli utenti potrebbero presupporre che questi rompicapi siano un costo inevitabile per l'uso dei computer, ma senza questo carico di lavoro sarebbero sicuramente molto disaccoppiati.

La soluzione migliore a questi problemi consiste nell'individuare una strategia generale per rendere le funzionalità dei prodotti software più evidenti ed auto-esplicativi. Gli utenti devono essere in grado di trovare una funzionalità ogni volta che ne hanno bisogno e devono essere in grado di usarla ogni volta che vogliono usarla.

### <a name="deductive-user-interface"></a>Interfaccia utente deducibile

La maggior parte degli elementi nel software oggi richiede all'utente di studiare e dedurre il proprio comportamento, come illustrato nello screenshot seguente.

![Screenshot di una finestra di dialogo delle proprietà di esempio.](images/iuiguidelines01.png)

Gli utenti esperti di computer, inclusi i progettisti di software, riconoscono rapidamente che questa finestra di dialogo consente loro di gestire un elenco di elementi. Comprendono che i pulsanti sotto l'elenco possono aggiungere, rimuovere e fornire informazioni sugli elementi dell'elenco. Tuttavia, si noti che nessuno di questo comportamento viene dichiarato in modo esplicito nel dialogo stesso.

Osservare ora il dialogo dal punto di vista di un utente occasionale. Molti utenti, quando si trovano di fronte a questo dialogo, chiederanno: "Cosa devo fare con questo?" Quando viene visualizzata la finestra di dialogo, l'utente deve arrestarsi e capire come procedere. In primo luogo, l'utente deve dedurre il fatto che il grande rettangolo bianco è una casella di riepilogo vuota da riempire con elementi. L'etichetta di testo piccola della casella, "Things", offre un suggerimento vago. Alcuni utenti tentano di digitare nella casella di riepilogo, perché è simile a una casella di testo di modifica.

Successivamente, l'utente deve dedurre che i pulsanti sotto l'elenco influiscono sul relativo contenuto. Alcuni pulsanti sono inizialmente disabilitati, un'altra possibile causa di confusione dell'utente. L'utente deve sperimentare i controlli per apprendere il funzionamento del dialogo.

L'utente potrebbe anche porre altre domande: "Quanti elementi è necessario inserire nell'elenco? È consigliabile immettere gli elementi in un ordine specifico? Perché il dialogo è stato visualizzato in primo luogo? A cosa si può fare?"

Gli utenti sono distratti dai loro obiettivi ogni volta che devono capire lo scopo di una schermata e come usarlo. Ciò rappresenta in definitiva un costo nel tempo e nella soddisfazione degli utenti. Ancora peggiore, gli utenti pagano questo costo più e più volte mentre si distondono sull'interfaccia ogni volta che usano una funzionalità.

Una schermata deve avere un titolo che ne spiega chiaramente lo scopo. Quando i progettisti creano una schermata, raramente richiedono uno scopo chiaramente espressivo. Potrebbe invece fare semplicemente parte di un modello concettuale più ampio che l'utente deve dedurre.

Gli studi mostrano che molti utenti sono confusi anche dalle operazioni di base nel software. Hanno difficoltà a capire cosa può fare il prodotto per loro, dove andare per eseguire un'operazione e come eseguire tale operazione dopo che l'hanno trovata. Semplificare il software apportando modifiche fondamentali è un modo efficace per soddisfare in modo più completo i clienti esistenti e attirare nuovi utenti.

### <a name="a-solution-inductive-user-interface"></a>Una soluzione: Interfaccia utente

Come nuovo modo di progettare il software, l'obiettivo di IUI è ridurre la quantità di estranee che gli utenti devono fare per spostarsi correttamente tra le parti di un prodotto e usarne le funzionalità. La parola induttiva deriva dal verbo induce, ovvero guidare o spostarsi in base all'influenza o alla persuasione.

IUI è un'estensione dell'interfaccia web comune. Nell'ambiente Web le pagine devono essere semplici e basate su attività perché ogni informazione deve essere inviata a un server tramite una connessione relativamente lenta. Il server risponde quindi con il passaggio successivo e così via. Una buona progettazione Web significa concentrarsi su una singola attività per pagina e fornire la navigazione tra le pagine. Analogamente, la navigazione induttiva inizia concentrando l'attività su ogni pagina su una singola attività primaria.

Un'interfaccia induttiva ben progettata consente agli utenti di rispondere a due domande fondamentali che devono affrontare quando guardano uno schermo:

-   Cosa devo fare ora?
-   Dove posso andare da qui per eseguire l'attività successiva?

Il software progettato in base a questi principi risponde a queste domande partendo da una base fondamentale: una schermata con un singolo scopo esplicito, chiaramente dichiarato, è più facile da comprendere rispetto a una pagina senza tale scopo. Se la schermata è più facile da comprendere, sarà più facile per l'utente sapere cosa fare e dove procedere.

Questa base fondamentale può essere ampliata in una serie di quattro passaggi per la progettazione di software che usa IUI:

-   Concentrare ogni schermata su una singola attività.
-   Stato dell'attività.
-   Adattare il contenuto della schermata all'attività.
-   Offrire collegamenti ad attività secondarie.

Sebbene questo documento descriva i principi generali dell'interfaccia utente, illustra anche questi principi in azione mostrando esempi di Money 2000 e di altro software. È consigliabile pensare a questi esempi come a espressioni particolari di IUI, non a un modello rigoroso per l'implementazione.

Oltre ai quattro passaggi elencati in precedenza, è possibile rafforzare l'interfaccia seguendo queste cinque linee guida:

-   Usare modelli di schermata coerenti.
-   Specificare le schermate per l'avvio delle attività.
-   È evidente come eseguire l'attività con i controlli sullo schermo.
-   Fornire un modo semplice per completare un'attività e avviarne una nuova.
-   Rendere ovvio il passaggio di navigazione successivo.

### <a name="processes"></a>Processi

Molte attività richiedono agli utenti di spostarsi tra una serie di schermate. Un utente che esegue un'attività potrebbe fare clic su un collegamento a un'attività secondaria che si allontana dalla sequenza di schermate che costituiscono l'attività primaria. Quando l'utente completa l'attività secondaria, dovrebbe esserci un modo semplice per restituire l'utente direttamente al punto di diramazione nell'attività originale. È probabile che gli utenti non  siano  in grado di usare i controlli di navigazione convenzionali, ad esempio i pulsanti Indietro e Avanti, per tornare al punto in cui sono stati avviati.

Per offrire questa funzionalità, IUI definisce un concetto di navigazione denominato processo, schermata o serie di schermate che eseguono un'attività. Un processo funge da subroutine di navigazione. Gli utenti possono iniziare un processo, scorrere la serie di schermate e quindi nell'ultima pagina fare clic su un pulsante "Fine" per tornare rapidamente alla pagina in cui hanno iniziato il processo.

## <a name="steps-for-creating-an-inductive-user-interface"></a>Passaggi per la creazione di un Interfaccia utente

Questa sezione descrive in modo approfondito i quattro passaggi che è possibile usare per creare un'interfaccia utente IUI.

### <a name="step-one-focus-each-page-on-a-single-task"></a>Passaggio 1: Concentrare ogni pagina su una singola attività

Il primo passaggio nella progettazione di un'interfaccia utente grafica consiste nell'adottare una funzionalità o un set di funzionalità e suddividerla in schermate separate. Ogni schermata deve essere incentrata su una singola attività, denominata attività principale della schermata.

Questa idea sembra semplice, ma poche applicazioni la seguono. La maggior parte delle applicazioni presenta una schermata da cui vengono completate tutte le funzionalità correlate. Questa progettazione richiede agli utenti di determinare (dedurre) le attività che è possibile eseguire e come eseguire questa operazione.

L'attività principale può essere specifica o aperta. Ad esempio, in un programma finanza personale, un'attività specifica potrebbe essere "Selezionare la fattura da pagare", mentre un'attività aperta potrebbe essere "Esaminare le prestazioni degli investimenti".

L'attività principale deve essere qualcosa che ha senso per l'utente, anziché riflettere un dettaglio di implementazione o un altro concetto astratto. L'attività deve essere un'attività che gli utenti potrebbero pensare di eseguire, preferibilmente descritta con parole proprie.

### <a name="example"></a>Esempio

In questa sezione vengono confrontate due versioni diverse di Money. Gli esempi mostrano funzionalità molto simili che consentono agli utenti di visualizzare e gestire i conti finanziari.

Il modello IUI è stato sviluppato durante la creazione di Money 2000, un'applicazione per la gestione delle finanze personali. Money 2000 è l'ottava versione principale del prodotto. Money 2000 è un programma Windows con oltre un milione di righe di codice.

Money 2000 è un'applicazione di tipo Web. Non è un sito Web, ma condivide molti attributi con i siti Web. L'interfaccia utente è costituita da pagine a schermo intero visualizzate in un frame condiviso, con strumenti per spostarsi avanti e indietro in uno stack di navigazione. Su questa base, Money 2000 aggiunge un set di nuove convenzioni dell'interfaccia utente che creano un'esperienza utente più strutturata.

Sebbene IUI sia stato usato per la prima volta nella progettazione in stile Web di Money 2000, può essere usato anche con elementi di interfaccia tradizionali, ad esempio finestre e finestre di dialogo.

In Money 99, gli utenti spesso eseguiti un'ampia gamma di attività su un singolo schermo. Ad esempio, lo screenshot seguente mostra **l'Account Manager** che ha presentato tutte le funzionalità correlate all'account in Money 99 in un'unica schermata.

![Screenshot del account manager in denaro 99.](images/iuiguidelines02.png)

Questa schermata raggruppa un'attività comune, passando a un account, nonché attività poco frequenti come la creazione e l'eliminazione di account. Nessuna di queste attività specifiche è espressa direttamente nel titolo della schermata, **Account Manager**. Molti utenti possono trovare questa schermata complessa come la finestra di dialogo di esempio nella figura 1. In entrambi i casi, l'utente deve dedurre lo scopo dello schermo e come usarlo.

Money 2000, che segue LUI, offre un set quasi identico di funzionalità correlate all'account, ma le fornisce in due schermate separate. Lo screenshot seguente mostra la prima di queste schermate, incentrata interamente sul far scegliere un account all'utente.

![Screenshot della schermata di selezione dell'account in money 2000.](images/iuiguidelines03.png)

La schermata Money 2000 contiene approssimativamente lo stesso numero di elementi visivi della schermata Money 99 precedente, ma la pagina è incentrata interamente sul far selezionare un account all'utente. Ad esempio, nella versione Money 99 un utente ha dovuto fare due clic per aprire un account: uno per selezionarlo e un altro per selezionare l'operazione di apertura. Nella versione Money 2000 l'unico motivo per cui un utente fa clic su un account è aprirlo e quindi può essere sufficiente un solo clic. In questo modo, anche se il numero di schermate potrebbe aumentare, il numero di clic necessari per eseguire un'attività comune è spesso ridotto.

In alcuni casi, gli utenti desiderano aggiungere o rimuovere un account. Per eseguire questa attività in Money 2000, gli utenti passano a una seconda schermata (illustrata nello screenshot seguente) incentrata sulla configurazione degli account.

![screenshot della schermata di configurazione dell'account in denaro 2000.](images/iuiguidelines04.png)

Lo scopo di ogni schermata è più chiaro nella versione IUI di Money 2000. Inoltre, ogni schermata ha più spazio da dedicare all'adempimento del proprio scopo. Ad esempio, l'account **manager** di Money 99 potrebbe concedere molto poco spazio al pulsante Elimina **account,** perché è stato usato raramente rispetto agli altri comandi sullo schermo. Al contrario, la schermata di configurazione dell'account in Money 2000 può usare questo comando in modo più evidente, rendendolo più individuabile ed esplicativo.

### <a name="what-is-a-single-task"></a>Che cos'è una singola attività?

Come è possibile sapere se una schermata è incentrata su una sola attività? Una schermata che supporta molte attività può essere spiegata come avere un solo scopo se tale scopo è sufficientemente astratto. Ecco una regola generale: una schermata è incentrata su uno scopo se il progettista può esprimere tale scopo con un titolo conciso, significativo e dal suono naturale.

I progettisti di Money 2000 hanno preso in considerazione l'interruzione di queste schermate ( Scegliere un **account** da usare e Configurare gli account **in Money**) in più schermate. Tuttavia, poiché ogni schermata ha già un titolo conciso, significativo e dal suono naturale, i progettisti hanno ritenuto che le schermate fossero sufficientemente mirate. Quando si progetta una schermata, se non si riesce a pensare a un titolo chiaro e semplice, è probabile che si stia tentando di ottenere troppi risultati sullo schermo.

### <a name="step-two-state-the-task"></a>Passaggio 2: Stato dell'attività

Ogni schermata deve essere intitolata con un'istruzione concisa ed esplicita dell'attività principale. Può trattarsi di un'istruzione diretta ("Selezionare l'account da bilanciare") o di una domanda a cui l'utente deve rispondere ("Quale account si vuole bilanciare?").

Si tratta di un altro principio semplice che spesso non viene praticato. Ad esempio, le versioni precedenti di Money avevano schermate con titoli come **Online Financial Services Manager** e Balance **Account**. Gli utenti dovevano dedurre lo scopo e il comportamento di queste schermate dalla disposizione e dalle etichette dei controlli.

Il titolo della schermata o della pagina è molto importante. Indipendentemente dal fatto che il prodotto usi finestre, pagine di tipo Web, finestre di dialogo o un'altra progettazione, non è consentito scorrere il titolo.

### <a name="usable-screens-have-clear-titles"></a>Le schermate utilizzabili hanno titoli chiari

Le schermate che eseguono molte attività richiedono titoli astratti o complessi. Ad esempio, la schermata Money 99 illustrata nella figura 2 ha consentito all'utente di passare agli account e di configurare gli account. Il titolo astratto "Account Manager" è stato assegnato a questa pagina nel tentativo di acquisire entrambi questi scopi. Anche se gli utenti potrebbero avere idee su come potrebbe fare una pagina "Account Manager", è possibile che non si rendano conto che l'attività più comune per questa schermata era semplicemente la scelta di un account.

Alcune schermate o comandi hanno scopi astratti che non suggeriscono immediatamente titoli chiari. Per queste schermate, i progettisti possono scegliere nomi deliberatamente eruditi, ad esempio "Impostazioni;" parole d'ordine coniate, ad esempio "QuickStep;" o il gergo che rivela i dettagli di implementazione ("Compattazione del database"). Questi tipi di nomi spesso confondono o fuorvianti per gli utenti. Inoltre, questi nomi sono in genere sostantivi che non esprimono l'azione che l'utente vuole eseguire, con un'aggiunta di confusione.

I titoli delle schermate e altri nomi spesso non vengono determinati fino alla fine del processo di progettazione. I progettisti spesso chiedono agli autori di trovare un nome appropriato per una schermata dopo che è stata progettata e codificata. A questo punto, se non è possibile trovare un nome valido, il team potrebbe essere in grado di risolvere i nomi che non sono chiari. La soluzione a questo difetto è che i progettisti pensino alla chiarezza nelle funzioni dello schermo e nei titoli nelle prime fasi del processo di progettazione.

Le funzioni e i titoli dello schermo devono concentrarsi sulle attività più comuni eseguite dai clienti. I progettisti sono spesso tentati di fornire enormi quantità di funzionalità nel tentativo di soddisfare il maggior numero di clienti, insieme ai desideri del team di progettazione stesso. Tuttavia, le funzionalità aggiuntive aggiungono sempre complessità e altri costi.

### <a name="screen-title-indicates-design-clarity"></a>Il titolo della schermata indica chiarezza della progettazione

Nel modello IUI, i progettisti scelgono i titoli delle schermate nelle prime fasi del processo di progettazione. Invece di scegliere un titolo per giustificare il funzionamento dello schermo, il titolo viene usato per determinare se lo schermo ha senso. Se non viene trovato alcun titolo appropriato, la funzionalità viene riprogettata. Se nessuna progettazione consente un titolo chiaro e conciso, ovvero se non è possibile spiegare la funzionalità, le finestre di progettazione potrebbero abbandonare la funzionalità. Nelle schermate seguenti confrontare la schermata di pagamento della fattura Money 99 a sinistra, che fornisce un'etichetta statica per la pagina ("Upcoming Bills & Deposits") e la schermata corrispondente di Money 2000 a destra, con un titolo esplicito ("Fare clic sulla fattura da pagare"):

![Screenshot che mostra un titolo statico in money 99 e un titolo attivo in money 2000.](images/iuiguidelines05.png)

Un titolo della schermata, che è ovviamente solo una frase o una frase, è più facile da modificare rispetto a una progettazione o a un codice. Nonostante questo, l'esperienza con IUI ha dimostrato che l'insistenza su un titolo chiaro in anticipo produce progettazioni migliori. I titoli devono essere scelti con l'input dei membri del team di formazione e usabilità degli utenti e dei progettisti di prodotti.

I membri del team possono talvolta provare a posticipare questa decisione, presupponendo che i clienti convivono la comprensione dello scopo di una schermata. Quando si è costretti a offrire una dichiarazione chiara e concisa di questo scopo, tuttavia, vengono spesso rivelate differenze di opinione. Risolvendo queste differenze e selezionando un titolo in anticipo, le discussioni di progettazione possono procedere più agevolmente.

Dopo aver scelto un titolo, non è consigliabile considerarlo non modificabile. I progettisti probabilmente affineranno i titoli delle schermate nel corso del tempo, come per qualsiasi progettazione. Tuttavia, il primo titolo scelto deve essere il più forte possibile in quella fase di sviluppo.

### <a name="guidelines-for-choosing-screen-titles&quot;></a>Linee guida per la scelta dei titoli delle schermate

In questa sezione viene descritta una semplice tecnica per la scelta dei titoli delle schermate. Per usare questa tecnica, i progettisti immaginano un amico che chiede: &quot;A cosa sta cercando questa schermata?&quot; e quindi viene visualizzata una risposta chiara e utile che completa la frase &quot;This is the screen where you?&quot;. Le parole che completano la frase diventano il titolo della schermata.

Durante lo sviluppo di Money 2000, gli autori della documentazione del team hanno creato linee guida per il titolo dello schermo per garantire qualità e coerenza. Ad esempio, queste linee guida consigliavano titoli che usavano verbi e venivano formulati come domande o istruzioni dirette. Le finestre di progettazione hanno evitato nomi statici che hanno consentito un'astrazione maggiore e potrebbero essere vaghi.

Per semplificare i titoli, i progettisti evitavano frasi composte e cercavano di usare il linguaggio di conversazione, evitando termini e termini difficili. Se i progettisti non possono descrivere l'attività senza ricorrere a congiunzioni (&quot;e&quot;, &quot;o"), è probabile che lo schermo stia tentando di eseguire più attività ed è meno probabile che l'utente sia in grado di comprendere immediatamente cosa fare.

Anche quando un titolo viene scelto con attenzione, l'area del titolo potrebbe essere troppo piccola per spiegare adeguatamente un'attività complessa. Per risolvere questo problema, è possibile includere un breve paragrafo descrittivo nella parte superiore dell'area del contenuto della schermata che elabora l'attività.

La tabella seguente contiene alcuni esempi di titoli di schermate in Money 99 e titoli per le stesse schermate o correlate in Money 2000.



| Titoli delle schermate in Money 99             | Nuovi titoli delle schermate in Money 2000                         | Commento                                         |
|---------------------------------------|---------------------------------------------------------|-------------------------------------------------|
| **Gestione account**                   | **Selezionare un account** **Configurare gli account**<br/> | Titolo statico modificato in titoli attivi.          |
| **Dettagli account**                   | **Modificare la configurazione dell'account**                                | Titolo statico modificato in titolo attivo e specifico. |
| **Calendario dei pagamenti**                  | **Pagare una fattura**                                          | Titolo vago reso descrittivo.                   |
| **Online Financial Services Manager** |                                                         | Pagina non necessaria dopo la riprogettazione.                 |



 

### <a name="making-the-screen-title-prominent"></a>Fare in modo che il titolo della schermata sia in primo piano

Dopo aver sistemato un titolo dello schermo utile, è importante assicurarsi che l'attenzione dell'utente sia attirata su di esso. Alcuni studi hanno dimostrato che gli utenti leggono raramente il testo informativo. Per risolvere questo problema, i titoli delle schermate devono essere progettati per essere importanti e accattivanti per attirare l'attenzione dell'utente. La progettazione visiva dello schermo deve informare l'utente che il titolo è la cosa più importante da leggere.

### <a name="step-three-make-the-pages-contents-suit-the-task"></a>Passaggio 3: Adattare il contenuto della pagina all'attività

Quando si crea un software che segue le linee guida dell'interfaccia utente, il lavoro di progettazione più difficile comporta in genere l'interruzione delle funzionalità in schermate o pagine. Il passaggio successivo consiste nel determinare quali controlli verranno usati in ogni schermata per eseguire l'attività principale. Questi controlli costituiscono il contenuto della pagina, in cui l'utente lavora. Il titolo e il contenuto della schermata sono due metà di un dialogo tra il programma e l'utente. Il titolo pone la domanda del programma o fornisce un'istruzione e l'utente risponde tramite l'interfaccia dello schermo.

Se il titolo della schermata è chiaro e semplice, la progettazione dello schermo è in genere semplice. Ad esempio, una delle schermate di Money 2000 mostrate in precedenza è intitolata "Selezionare un account da usare". Dato questo titolo, la schermata deve ovviamente contenere un semplice elenco di account tra cui l'utente può scegliere. Un'altra schermata di Money 2000 ha il titolo "Controllare gli elementi da includere nelle imposte". Naturalmente, questa schermata contiene un elenco di controllo degli elementi.

Gli utenti devono essere in grado di capire facilmente come usare i controlli per ottenere l'attività principale dello schermo. Quando agli utenti viene detto di selezionare un account e possono cercare un elenco di account sullo schermo, confermano la comprensione dell'attività. Ciò aumenta la probabilità che gli utenti avranno esito positivo, con un aumento della fiducia nell'esecuzione di altre attività.

### <a name="screen-content-areas"></a>Aree del contenuto dello schermo

La posizione e la forma esatte delle aree di contenuto dello schermo dipendono dalla progettazione del software. In Money 2000 l'area del contenuto della schermata è tutto sotto il titolo della schermata e a destra dell'elenco attività. Questa area può scorrere su schermi lunghi. Alcuni contenuti non essenziali potrebbero essere visualizzati anche nell'area di stato sotto l'elenco attività.

I progettisti possono scegliere di elaborare l'attività principale della schermata in un paragrafo nella parte superiore dell'area del contenuto. Gli utenti non devono mai leggere questo testo, ma possono trovarlo utile. Molti utenti possono ignorarlo e usare comunque la schermata correttamente. A differenza del titolo, questa descrizione può scorrere via se la schermata è scorrevole. Per altre informazioni, vedere [Linee guida per la scelta dei titoli delle schermate.](#guidelines-for-choosing-screen-titles)

Se i progettisti vogliono che una pagina visualizza promemoria, avvisi o altre informazioni sullo stato non essenziali, può essere visualizzata a sinistra dell'area di contenuto principale, sotto l'elenco attività sul lato sinistro dello schermo. Dal punto di vista funzionale, questa area di stato è un'area aggiuntiva per il contenuto dello schermo. Questa area non è sufficientemente importante da contenere controlli essenziali.

### <a name="provide-a-clear-exit-from-the-page"></a>Specificare un'uscita chiara dalla pagina

Dopo aver completato correttamente un'attività, l'utente deve affrontare un altro problema: quando e come uscire dalla schermata. Per le schermate la cui attività principale è la navigazione, l'esecuzione dell'attività stessa sposta l'utente alla schermata successiva. In altre schermate può essere più difficile per l'utente sapere come procedere. Ad esempio, in una schermata che chiede all'utente di digitare informazioni nei campi, l'utente potrebbe avere bisogno di aiuto per capire quando e come andare avanti. In tali pagine è spesso utile offrire  un pulsante Avanti o **Fine** chiaro in una posizione coerente.

Gli studi sull'usabilità hanno dimostrato che gli utenti preferiscono  usare questi pulsanti anche quando sono disponibili pulsanti di spostamento globali, ad esempio i pulsanti Indietro o **Home** su una barra degli strumenti. Gli utenti spesso si trovano a disagio sugli schermi senza uscita chiara, anche le schermate il cui unico scopo è fornire informazioni da leggere.

Per altre informazioni su questo argomento, vedere Fornire un modo semplice per completare [un'attività](#provide-screens-for-starting-tasks) e avviarne una nuova nella sezione Linee guida aggiuntive.

### <a name="step-four-offer-links-to-secondary-tasks"></a>Passaggio 4: Offrire collegamenti ad attività secondarie

L'ultimo passaggio nella progettazione di una schermata consiste nel fornire collegamenti alle attività secondarie, ovvero funzionalità che non eseranno direttamente l'attività primaria, ma sono correlate alla schermata. Ad esempio, se l'attività principale in una schermata è scrivere una lettera, le attività secondarie in tale schermata potrebbero essere cercare un indirizzo postale o stampare una busta.

Le attività secondarie possono visualizzare finestre di dialogo, modificare la presentazione visiva del contenuto della schermata o passare all'utente in un'altra schermata. Un'attività secondaria potrebbe eseguire indirettamente l'attività primaria o reindirizzare gli utenti persi alla posizione che stanno cercando.

Se una pagina è una conversazione tra il computer e l'utente, un'attività secondaria consente all'utente di ignorare la domanda presente del computer e chiedere al computer di eseguire altre operazioni. Si supponga, ad esempio, che questa finestra di dialogo: Computer: "Quale fattura si vuole pagare?" Utente: "In realtà, quello che voglio fare è trovare una fattura che ho pagato un po' di tempo fa".

Alcune schermate del prodotto non avranno attività secondarie, mentre altre ne avranno diverse. È consigliabile evitare di creare un lungo elenco di attività che probabilmente saranno difficili da analizzare per l'utente. Se una schermata ha un elenco relativamente lungo di attività secondarie, le attività più comuni devono essere posizionate per prime, raggruppate in una sezione separata o evidenziate visivamente in altro modo.

L'elenco non deve includere tutte le attività secondarie concepibili, purché rendo evidente il passaggio di navigazione successivo. Anziché offrire molte attività secondarie, una schermata può fornire attività secondarie che consentono di passare alle pagine secondarie che elencano altre attività.

### <a name="visual-design-of-secondary-tasks"></a>Progettazione visiva delle attività secondarie

Le attività secondarie devono essere elencate in una posizione subordinata sullo schermo, dove sono accessibili se necessario, ma non distrarre l'utente dall'attività primaria. L'inserimento di questo elenco in una posizione coerente in ogni schermata consente agli utenti di trovare rapidamente l'elenco quando ne hanno bisogno.

Se si visualizza l'elenco delle attività secondarie sul lato sinistro della schermata, l'elenco stesso non deve essere scorrevole né deve scorrere con la pagina, come illustrato nell'immagine seguente della schermata **Bill Pay** di Money 2000.

![Screenshot della schermata di pagamento della fattura in denaro 2000.](images/iuiguidelines07.png)

## <a name="additional-guidelines"></a>Linee guida aggiuntive

Questa sezione descrive cinque linee guida utili per la creazione di un'interfaccia utente grafica in base ai quattro passaggi descritti nella sezione precedente.

### <a name="use-consistent-screen-templates"></a>Usare modelli di schermo coerenti

Quando si progetta un software che segue il modello IUI, è necessario creare un modello da usare come guida per ogni schermata. Il modello induttivo non impone l'uso di un modello specifico. Esistono molte possibili varianti che possono soddisfare una progettazione induttiva. Il prodotto potrebbe avere bisogno di un solo modello per tutte le schermate oppure è possibile creare diversi modelli per vari scopi.

Un buon modello consente a un nuovo utente di comprendere rapidamente il funzionamento degli schermi del prodotto. Un uso coerente del modello nelle schermate del prodotto offre un buon flusso dell'interfaccia utente da uno schermo all'altro. Quando gli utenti imparano a aspettarsi che gli stessi elementi vengano visualizzati nelle stesse posizioni, possono analizzare e iniziare a usare ogni nuova schermata più rapidamente.

### <a name="provide-screens-for-starting-tasks"></a>Fornire schermate per l'avvio delle attività

I prodotti progettati con IUI usano spesso schermate speciali progettate per avviare gli utenti su set di attività. Queste schermate sono denominate pagine di attività perché organizzano gruppi correlati di attività comuni. Le pagine attività forniscono un punto di partenza per gli utenti. Una pagina di attività presenta in genere collegamenti ad altre pagine in cui l'utente ottiene effettivamente il lavoro svolto. Le pagine attività chiedono all'utente "What do you want to do now?" (Cosa si vuole fare ora? e presentare un elenco di possibili risposte. Le pagine attività possono seguire un modello speciale per consentire agli utenti di riconoscerle.

Una pagina attività crea una buona pagina iniziale predefinita per un prodotto. Quando gli utenti avviano un'applicazione, in genere hanno un'idea dell'attività che vogliono eseguire. In genere, il motivo per cui si avvia il prodotto è una delle piccole attività molto comuni. La pagina iniziale predefinita del prodotto lo riconosce rendendo evidente come iniziare le attività comuni.

La home **page** di Money 2000 è un esempio di pagina attività. Per impostazione predefinita, gli utenti visualizzano questa schermata, in cui viene visualizzato l'accesso alle attività finanziarie comuni, ad esempio il pagamento di una fattura e il bilanciamento di un account, quando avviano l'applicazione.

Lo screenshot seguente mostra la home **page** di Money 2000.

![Screenshot della schermata money 2000 home page. una pagina attività che elenca alcune attività comuni e fornisce collegamenti a set di attività in altre pagine.](images/iuiguidelines08.png)

Poiché Money offre molte funzionalità finanziarie, solo le attività finanziarie più comuni rientrano nella **home** page. Per tutte le altre attività, la **home** page è collegata a un set affiliato di pagine di attività denominate centri finanziari. Ogni area principale di Money fornisce un centro finanziario. Queste schermate presentano il livello successivo di attività, che funge da punto di partenza per tutte le funzionalità all'interno di ogni area.

Ad esempio, l'area **Imposte sul** denaro contiene le funzionalità relative alle imposte del prodotto. **L'area Imposte** offre collegamenti a queste funzionalità in una **pagina tax center,** come illustrato nello screenshot seguente.

![Screenshot della pagina money 2000 tax center. ](images/iuiguidelines09.png)

Una pagina attività può anche essere molto più semplice se sono disponibili meno opzioni. La schermata seguente mostra come usare una pagina attività per la gestione Windows account utente.

![Screenshot di una pagina attività money 2000 per la gestione degli account utente di Windows. ](images/iuiguidelines10.png)

### <a name="make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen"></a>Rendere evidente come eseguire l'attività con i controlli sullo schermo

Il modo migliore per seguire questa linea guida è scegliere un titolo della schermata appropriato e limitare l'ambito delle attività primarie solo alle più comuni. Dopo aver raggiunto un titolo e uno scopo chiari per la pagina, scegliere il set di controlli giusto sarà semplice.

### <a name="provide-an-easy-way-to-complete-a-task-and-start-a-new-one"></a>Fornire un modo semplice per completare un'attività e avviarne una nuova

L'ultimo ostacolo che un utente deve affrontare su uno schermo è capire quando e come uscire. L'utente in genere lascia la schermata facendo clic su un collegamento o eseguendo un comando che consente di passare a un'altra schermata. Questi collegamenti possono essere visualizzati nell'area del contenuto della schermata, nell'elenco attività o sulle barre degli strumenti di spostamento. Gli utenti possono anche uscire da una schermata chiudendo il file corrente o l'applicazione stessa.

L'attività in alcune schermate è preparare un'operazione che l'utente deve confermare o annullare. Tali schermate in genere offrono un collegamento che esegue ed esegue il commit dell'operazione e un altro collegamento che annulla. Se l'utente ignora queste opzioni e fa clic su un altro collegamento, il programma deve eseguire l'opzione meno distruttiva. Le schermate indicano cosa accade se l'utente accetta questo percorso. È possibile formulare i collegamenti per renderlo più ovvio. Ad esempio, un pulsante di commit con etichetta "Salva modifiche" implica che le modifiche apportate sullo schermo non saranno effettive fino a quando non viene fatto clic su tale pulsante.

Anche se gli utenti possono uscire quando vogliono, è comunque possibile offrire un collegamento che suggerisce un'uscita ovvia dalla pagina. Lo stesso vale per le pagine che visualizzano semplicemente informazioni statiche. Per altre informazioni su questo argomento, vedere la sezione [Fornire un'uscita chiara dalla pagina](#provide-a-clear-exit-from-the-page).

### <a name="starting-and-completing-processes"></a>Avvio e completamento dei processi

Ai fini di questo articolo, i processi sono tecniche per gestire le attività che connettono l'utente a più schermate.

Si supponga che un utente fa clic su un collegamento nel contenuto o nell'elenco attività di una schermata e che sia visualizzato in un'altra schermata. Tale pagina a sua volta potrebbe essere la prima di una serie di schermate che ottiene un risultato complessivo. Alla fine di questa serie di schermate, l'utente vuole tornare alla schermata che ha preceduto il processo. Esistono almeno due modi in cui l'utente può tornare? facendo clic pulsante Indietro più volte o tornando al home page e passando da qui? ma nessuno di questi metodi è ovvio o naturale. La maggior parte degli utenti prevede di trovare un pulsante nella schermata finale che li restituisca direttamente alla schermata originale.

Il modello IUI supporta questo scenario tramite il concetto di processo, schermata o serie di schermate trattate come unità di navigazione. Gli utenti possono immettere il processo, scorrere le schermate e nell'ultima schermata trovare un pulsante che li restituisca nel punto in cui sono stati avviati. È importante notare che l'utente può avviare il processo da più posizioni nel prodotto. Gli utenti vengono sempre restituiti al punto in cui hanno iniziato, indipendentemente da dove si trovavano quando hanno iniziato il processo.

### <a name="process-name"></a>Nome del processo

A ogni processo deve essere assegnato un nome e il nome deve essere visualizzato in un punto qualsiasi di ogni schermata del processo. Money 2000 usa questo approccio. Ogni schermata che fa parte di un processo complessivo include il nome di tale processo nella parte superiore. Questo nome di processo viene visualizzato meno in primo piano rispetto al titolo univoco della schermata perché è meno importante. Il nome del processo ricorda agli utenti quale processo sta conducendo e rafforza la nozione che tutte le schermate del processo fanno parte di una singola funzionalità. Ad esempio, **l'area Imposte sul denaro** include un processo di **stima** delle imposte che si estende su più schermate. In ogni schermata di questo processo vengono visualizzati sia il nome del processo collettivo che il titolo univoco della schermata.

### <a name="implementation-of-processes"></a>Implementazione di processi

Lo stesso processo può essere avviato da vari collegamenti in schermate diverse e gli utenti verranno sempre restituiti alla pagina iniziale corretta. Questo comportamento non può essere ottenuto tramite un collegamento hard-coded nella schermata finale del processo, perché la destinazione del collegamento varierà. Al contrario, l'applicazione può implementare questo comportamento mantenendo uno stack di processi attivi, indipendentemente dallo stack di navigazione normale usato dai **comandi Indietro** **e** Avanti. Quando l'utente avvia un processo, viene inserito lo stack di processi nella schermata di avvio. Quando l'utente  fa clic sul pulsante Fine nella schermata finale del processo, l'applicazione apre la schermata di avvio più recente dallo stack e restituisce l'utente a tale schermata.

Quando gli utenti si allontanano da una schermata in un processo, il processo rimane attivo nello stack di processi. Gli utenti possono completare il processo di backup fino alla schermata in cui l'hanno lasciato e quindi continuare. In questo modo gli utenti possono effettuare una deviazione, eseguire il backup e quindi andare avanti con il processo. Per verificare il funzionamento di questo comportamento, avviare qualsiasi processo di acquisto online nel World Wide Web, lasciare il sito e quindi premere **il pulsante** Indietro. In genere sarà possibile riprendere da dove è stato lasciato.

### <a name="done-button"></a>Pulsante Fine

Per completare una schermata e passare alla schermata successiva nel processo, le schermate possono visualizzare un pulsante nella parte inferiore della pagina. L'etichetta di questo pulsante è "Avanti", "Fatto" o qualcosa di simile. Se il pulsante termina il processo e il processo  può essere chiamato da più posizioni, la didascalia del pulsante Fine può includere il nome della località chiamante.

### <a name="navigation-bar"></a>Barra di navigazione

In qualsiasi schermata, gli utenti potrebbero decidere di completare l'area corrente del prodotto e di voler avviare altro. Potrebbe non voler completare in modo esplicito la schermata corrente prima di passare a un'altra parte del prodotto. Una barra degli strumenti di spostamento può offrire all'utente un set di collegamenti per l'avvio di nuove attività. Come per altri elenchi di collegamenti alle attività, questi devono seguire il principio di rendere ovvio il passaggio di navigazione successivo, descritto in dettaglio nella sezione seguente.

### <a name="make-the-next-navigational-step-obvious"></a>Rendere ovvio il passaggio di navigazione successivo

Pochi programmi possono rendere tutte le funzionalità disponibili contemporaneamente. Gli utenti in genere devono spostarsi all'interno di un programma per trovare una particolare funzionalità. Gli utenti hanno più successo nella navigazione se possono facilmente vedere come ottenere almeno un passo più vicino al risultato desiderato. Le schermate che usano IUI sono progettate in base a questo principio.

Ad esempio, le pagine attività non visualizzano necessariamente ogni attività o destinazione immaginabile che l'utente potrebbe voler ottenere da quel punto. Al contrario, le pagine attività forniscono un elenco di attività sufficientemente complete in modo che gli utenti possano determinare facilmente il collegamento appropriato su cui fare clic, anche se le porta solo a un'altra pagina di collegamenti. Le attività più frequenti devono essere più importanti e richiedono la quantità minima di navigazione. Le attività meno frequenti possono richiedere più passaggi.

Ecco un esempio di Money 2000. Si supponga che gli utenti vogliano eseguire un'operazione solo occasionalmente, ad esempio controllare l'importo stimato del pagamento dell'imposta sul reddito dell'anno successivo. Gli utenti iniziano prima a cercare questa funzionalità nella home page di Money 2000. Poiché la funzionalità non viene visualizzata nell'elenco delle attività comuni, deve analizzare l'elenco delle aree finanziarie. **L'area Imposte sembra** promettente, quindi fanno clic su di essa. La **pagina Tax Center** contiene un collegamento alla funzionalità di stima delle imposte che sta cercando, quindi fa clic su di essa e completa l'attività. Applicando i principi IUI, Money 2000 consente agli utenti di trovare in modo intuitivo ciò che cercano.

## <a name="user-assistance"></a>Assistenza per l'utente

Questa sezione descrive un set di linee guida consigliate per l'integrazione del testo di assistenza utente in un prodotto che usa IUI.

L'assistenza principale si riferisce a tutto il testo visibile sullo schermo (come illustrato nella schermata seguente). L'assistenza primaria fornisce informazioni testuali incentrate sulle attività in modo che gli utenti possano facilmente comprendere tutte le informazioni presentate sullo schermo. Comprendono lo scopo della pagina e il modo in cui gli oggetti sono correlati tra loro per facilitare l'esecuzione di attività. Poiché il testo è direttamente sullo schermo, le informazioni che risponde a domande inesatta come "Cosa devo fare?" è facile da accedere e altamente visibile senza che l'utente deve eseguire alcuna azione.

![Screenshot della schermata di configurazione dell'account di Money 2000.](images/iuiguidelines11.png)

L'assistenza secondaria è costituita da tutto il testo non visibile sullo schermo e richiede un'interazione dell'utente per accedere, ad esempio facendo clic o passando il puntatore del mouse su un elemento dell'interfaccia utente. Questo contenuto non è essenziale per eseguire l'attività a portata di mano, ma è ancora correlato direttamente.

### <a name="primary-assistance"></a>Assistenza primaria

L'assistenza primaria può includere alcuni o tutti i componenti seguenti:

-   Titolo della schermata

    Esempio: Modificare l'immagine

    Il titolo della schermata è il primo e più importante elemento visualizzato sullo schermo. Lo scopo è descrivere nella lingua dell'utente l'attività che può essere completata in questa pagina. Il titolo della schermata deve evitare di descrivere i dettagli su come completare l'attività. Il testo nel titolo della schermata deve fare riferimento solo all'attività principale della schermata. Come regola generale, più semplice e più breve è la descrizione dell'attività, è probabile che l'attività sia meglio definita. Per informazioni più approfondite su questo argomento, vedere Passaggio 2: [Stato dell'attività](#step-two-state-the-task).

-   Sottotitolo dello schermo

    Esempio: è anche possibile scaricare una nuova immagine da Internet.

    Anche con un impegno attento, il titolo della schermata potrebbe non essere sufficiente per spiegare in modo adeguato un'attività complessa. Il sottotitolo consente di elaborare lo scopo dello schermo. È possibile usare un sottotitolo per chiarire lo scopo della pagina, fornire una descrizione aggiuntiva dell'attività o impostare le aspettative. Gli utenti che non leggono il sottotitolo devono essere in grado di usare correttamente la pagina. Proprio come il titolo, il sottotitolo deve evitare di descrivere i dettagli per il completamento dell'attività.

-   Attività

    Esempio: Modificare il screen saver

    Le attività possono essere presentate come collegamenti di testo o immagini grafiche che richiedono l'interazione dell'utente. I comandi presentati come collegamenti di testo devono essere basati su verbi e scritti come attività chiare e concise.

-   Etichette per i pulsanti di comando

    Esempio: Creare una password

    Esistono tre tipi di pulsanti di comando:

    -   Annulla
    -   Fine
    -   Commit

    I pulsanti Annulla e Fine usano semplicemente "Cancel" e "Done" come etichette. I pulsanti di commit devono usare etichette di testo attive anziché "OK". Ad esempio, usare "Crea password" anziché "OK".

-   Etichette per altri controlli

    Esempio: Digitare la password

    Le etichette per i controlli, ad esempio pulsanti di opzione, caselle di controllo e caselle di testo, devono essere scritte in modo chiaro e conciso in modo che gli utenti sappiano esattamente a cosa servono i controlli, quali usare e quali informazioni devono essere fornite per svolgere la propria attività.

-   Collegamenti "Attività correlate"

    Esempio: Attività correlate - Modificare un altro account

    I collegamenti "Attività correlate" sono punti di ingresso espliciti ad altre attività correlate alla funzionalità corrente. Devono essere scritti come collegamenti basati su attività.

-   Collegamenti "Vedere anche"

    Esempio: Vedere anche - Modificare il tema

    I collegamenti "Vedere anche" sono attività secondarie. Questi sono correlati all'attività primaria, ma esereranno l'utente dal contesto corrente. Dovrebbero essere visualizzati come normali collegamenti di attività. Per altre informazioni sulle attività secondarie, vedere [Progettazione visiva delle attività secondarie](#visual-design-of-secondary-tasks).

### <a name="secondary-assistance"></a>Assistenza secondaria

L'assistenza secondaria può includere alcuni o tutti i componenti seguenti:

-   Suggerimenti per le informazioni

    È possibile usare un suggerimento informazioni per fornire all'utente informazioni aggiuntive su un collegamento a un'attività o un pulsante di comando. Ad esempio, un suggerimento info su un collegamento all'attività potrebbe essere "Visualizza una pagina in cui è possibile selezionare un'immagine da usare con l'account". La descrizione comando viene visualizzata quando l'utente passa il mouse sull'oggetto associato. È necessario creare suggerimenti info per tutti gli elementi dell'interfaccia utente su cui l'utente può fare clic.

-   Argomenti della Guida "Informazioni su"

    Esempio: Informazioni su - Download di un file

    I collegamenti "Informazioni su" aprono argomenti della Guida, ad esempio panoramiche delle funzionalità, informazioni concettuali, informazioni di supporto e informazioni procedurali. Per ridurre il disordine, è consigliabile ridurre al minimo il numero di argomenti della Guida "Informazioni su" sullo schermo.

## <a name="appendix-designing-and-testing-microsoft-money-2000"></a>Appendice: Progettazione e test di Microsoft Money 2000

Questa sezione è stata adattata dalle descrizioni di prima mano dei progettisti. Viene illustrato come il team di Money 2000 ha modificato il processo di progettazione e test per adattarlo al modello IUI.

### <a name="designing-and-testing-money-2000"></a>Progettazione e test di Money 2000

La progettazione di Money 2000 con il modello di navigazione induttiva ha portato il team a mettere in discussione i progetti presenti nel prodotto da molto tempo. Poiché i principi del modello sono semplici, è stato facile adottare il modello nel processo di progettazione e rimanere con esso. Alla fine, i progettisti ritengono che il modello li abbia aiutati a creare progettazioni migliori di quelle che avrebbero potuto produrre senza di esso.

### <a name="clearer-titles-and-designs"></a>Titoli e progettazioni più chiari

I progettisti di Money 2000 hanno notato che spesso descrivono le funzionalità usando parole che non sono effettivamente visualizzate sullo schermo. Nel modello IUI le schermate devono spiegarsi. Ad esempio, il team ha spiegato che la schermata con etichetta **Calendario pagamenti** era destinata al pagamento delle fatture. In Money 2000 tale schermata è denominata **Pay Bills**. Tutti gli elementi che non sono correlati a tale scopo sono stati spostati in schermate sussidiarie, con conseguente progettazione più chiara.

Un altro esempio riguarda una schermata denominata **Online Financial Services Manager.** Il team ha faticato a trovare una semplice spiegazione dello scopo di questa schermata. Quando non sono stati in grado di arrivarne uno, questa schermata è stata rimossa e le funzionalità sono state distribuite tra pagine più definite in modo logico.

### <a name="helping-new-designers"></a>Aiutare i nuovi progettisti

Il team ha trovato facile insegnare tecniche di progettazione IUI a progettisti di software nuovi e inesperti. Le tecniche hanno consentito ai progettisti a tutti i livelli di esperienza di valutare le proprie progettazioni usando i titoli delle schermate come test di chiarezza. Quando sono costretti a inserire un titolo chiaro e conciso su uno schermo progettato in modo non sufficiente, i progettisti hanno rapidamente riconosciuto che nessun titolo era sufficiente per la pagina. Si sono resi conto che il problema non si verificava nella scelta delle parole per un titolo, ma in un design dello schermo difettoso. Con questa conoscenza, possono quindi riprogettare la schermata per supportare un'interazione più chiara con l'utente e, di conseguenza, un titolo più chiaro.

### <a name="including-writers"></a>Inclusione di writer

Con l'avanzamento della progettazione, il team si è reso conto che gli autori e gli editor della documentazione dovevano essere coinvolti nella creazione di titoli di schermata. Gli autori erano limitati nella possibilità di scegliere titoli di qualità nelle versioni precedenti perché erano coinvolti solo in una fase tardiva. I progettisti o i programmatori hanno in genere assegnato titoli di lavoro temporanei alle schermate. Questi titoli sono stati usati fino alla fine del ciclo del prodotto quando agli autori è stato chiesto di creare titoli di schermata finali. A questo punto, era troppo tardi per rielaborare schermate progettate in modo non scadente.

Al contrario, il team money 2000 ha coinvolto gli autori nelle prime fasi del processo di progettazione. Ciò ha portato importanti input sui titoli delle schermate quando poteva ancora essere utile per la progettazione. Se una schermata era troppo complessa per consentire un titolo chiaro, gli autori potrebbero suggerire la riprogettazione della pagina.

Alla fine del progetto, gli autori e i progettisti hanno ritenuto che i titoli delle schermate fossero più chiari e più potenti rispetto alle versioni precedenti. Gli autori hanno anche trovato più semplice spiegare le nuove pagine, semplificando così il processo di documentazione del prodotto. Tutti i membri del team hanno pensato che il coinvolgimento di tutte le discipline nella fase di progettazione rendesse il prodotto migliore e più facile da usare.

### <a name="usability-tests"></a>Test di usabilità

Durante lo sviluppo di Money 2000, il team ha eseguito diversi test di usabilità per esaminare le differenze tra la struttura di navigazione precedente di Money 99 e le modifiche apportate in seguito all'applicazione del modello IUI.

### <a name="prototype-testing"></a>Test del prototipo

Nelle prime fasi del processo di sviluppo del prodotto, i progettisti hanno creato un prototipo per esplorare il modo in cui gli utenti reagiscono all'interfaccia utente. Questo lavoro è stato eseguito molto presto nel processo di sviluppo per consentire il tempo necessario per perfezionare i principi del modello prima che i programmatori iniziano a migliorare il prodotto stesso.

Il team ha creato un prototipo in Microsoft Visual Basic e HTML che ha simulato finanza personale attività normalmente eseguite in Money. Nel prototipo gli utenti possono passare a più di 50 pagine che rappresentano le aree principali del prodotto. In queste aree è possibile configurare account finanziari, pagare fatture, visualizzare report e lavorare con gli investimenti.

Undicesimo partecipante ha eseguito lo stesso set di attività sia in Money 99 che nel prototipo IUI. Sono stati assegnati in modo casuale per usare prima uno dei prodotti. Quattro partecipanti erano gli utenti correnti di Money, quattro erano gli utenti correnti di un prodotto concorrente e tre non avevano mai usato un prodotto finanza personale prima d'ora.

Le preferenze generali indicavano che i quattro utenti correnti di Money preferivano Money 99 (la versione che usavano a casa), mentre i sette utenti rimanenti preferivano il nuovo prototipo alla versione corrente. Per tutte le altre misure, non esiste alcuna differenza tra gli utenti dei tre gruppi. In termini di prestazioni complessive, gli utenti si trovavano nell'area errata del prodotto il doppio delle volte usando Money 99 (2,82 volte per attività) come nel prototipo (1,45 volte per attività). Altri dati di preferenza e misure delle prestazioni, anche se non significativi, sembra predilivano il prototipo. In base a questi dati e ad altri test, il team del prodotto Money ha deciso di incorporare i principi IUI in Money 2000.

### <a name="product-testing"></a>Test del prodotto

Una volta completata la maggior parte del codice per il prodotto, il team ha eseguito un altro studio sull'usabilità per esaminare l'implementazione finale di IUI. In questo test sono stati selezionati 10 partecipanti che non hanno mai usato un prodotto finanza personale in precedenza per l'uso di Money 99 o Money 2000. Tutti gli utenti hanno eseguito le stesse attività.

Gli utenti di Money 2000 hanno completato correttamente l'89% delle attività, mentre gli utenti di Money 99 hanno completato correttamente solo il 74% delle attività. Come per il prototipo, anche gli utenti sono sembrati più veloci, ma non significativamente diversi, per la navigazione in Money 2000 rispetto a Money 99. Inoltre, le misure complessive di soddisfazione soggettiva per la navigazione tendevano anche a essere più elevate per Money 2000 che per Money 99.

### <a name="controlled-testing"></a>Test controllati

Poiché Money 2000 è enorme e complesso, non è particolarmente adatto per eseguire esperimenti controllati sugli effetti dell'applicazione dell'interfaccia utente grafica. Il team ha invece creato un ambiente più vincolato per il test.

Il test ha coinvolto un'applicazione "Stock Market Viewer" che ha consentito agli utenti di modificare la visualizzazione di un report del mercato azionario visualizzato sullo schermo. Gli utenti possono modificare le colonne di dati incluse nel report, l'ordine delle colonne del report, l'allineamento e il numero di posizioni decimali utilizzate. I progettisti desiderano vedere le prestazioni di un approccio IUI a questa attività rispetto a un'interfaccia utente grafica convenzionale.

Lo screenshot seguente mostra l'interfaccia utente convenzionale usata nel test. Una singola finestra di dialogo esegue tutte le attività di personalizzazione dei report. Molte applicazioni offrono una finestra di dialogo simile per la selezione di un subset da un elenco di elementi. La finestra di dialogo contiene due elenchi: nell'elenco a sinistra vengono visualizzate tutte le colonne del report disponibili e a destra viene visualizzato il subset di colonne selezionato dall'utente per il report. Controlli aggiuntivi modificano l'ordine e gli attributi di formattazione per le colonne del report selezionate nell'elenco a destra.

![Screenshot di una finestra di dialogo convenzionale.](images/iuiguidelines12.png)

Per la versione IUI di questa attività, il team ha creato un'applicazione di tipo Web. Ogni attività di personalizzazione è stata inserita in una pagina separata. L'applicazione include anche una pagina principale, illustrata nello screenshot seguente, che chiede agli utenti come personalizzare il report.

![screenshot di una schermata di test iui.](images/iuiguidelines13.png)

Facendo clic sui collegamenti in questa pagina principale, l'utente viene in grado di accedere ad altre pagine per eseguire attività di personalizzazione specifiche. Ad esempio, lo screenshot seguente mostra la pagina usata per selezionare le colonne del report.

![Screenshot di una schermata di test iui per la selezione delle colonne del report.](images/iuiguidelines14.png)

Nei test di entrambe le versioni, agli oggetti è stato richiesto di personalizzare i report da un determinato stato iniziale (visualizzato sullo schermo) a uno stato obiettivo specificato (visualizzato su un handout cartaceo). Il computer ha monitorato la quantità di tempo e il numero di tentativi effettuati per personalizzare il report. Il computer ha informato gli utenti quando hanno personalizzato correttamente il report.

Il test includeva 88 partecipanti. A ogni partecipante è stato richiesto di personalizzare un set di 11 report con una delle due versioni dell'applicazione. Inoltre, 72 di questi partecipanti sono tornati una settimana dopo per personalizzare un altro set di 11 report usando la stessa versione della prima sessione. Ogni oggetto è stato classificato come utente novizio del computer, principalmente usando il computer per la posta elettronica, riproducendo l'isolamento ed navigando sul Web.

Non vi sono differenze significative tra gli utenti delle due versioni o qualsiasi altra variabile di interesse. Gli utenti hanno eseguito attività alla stessa velocità, hanno eseguito l'iterazione sull'attività lo stesso numero di volte e hanno avuto le stesse classificazioni di soddisfazione soggettive complessive per le due versioni. Questo test, pertanto, non è riuscito a visualizzare le misure in cui l'interfaccia utente ha comportato un miglioramento o una riduzione delle prestazioni o delle classificazioni soggettive.

È possibile che, se l'utente deve spostarsi di più per eseguire l'attività, la quantità di tempo per eseguire l'attività deve essere maggiore. Anche se questo esperimento non suggerisce questo risultato, è importante notare che i tempi di prestazioni medio e le deviazioni standard associate per i due diversi approcci a questa attività erano quasi identici.

Saranno necessarie ulteriori ricerche per determinare se sono stati apportati miglioramenti misurabili dall'uso dell'IUI. Come minimo, questo test non ha fornito alcuna prova che l'IUI danneggerà le prestazioni o l'utilizzo del prodotto.

### <a name="comparison-with-web-sites"></a>Confronto con siti Web

Molti siti Web ben progettati usano principi simili al modello IUI descritto in questo documento. Si tratta probabilmente di un effetto collaterale del funzionamento del Web. Poiché è difficile implementare interazioni complesse tra i controlli in una singola pagina Web, i progettisti spesso suddivideno le attività in parti che comportano più di una corsa al server per ottenere una nuova pagina. Alcuni siti includono anche titoli di pagina che specificano chiaramente lo scopo della pagina.

I progettisti di applicazioni tradizionali hanno a disposizione un set di strumenti molto più ricco. Ciò offre maggiore flessibilità, ma offre anche più opportunità per creare pagine complesse e confusi. Quando si creano interfacce utente induttivi, i progettisti devono usare questa potenza con discrezione e ricordare di valore per chiarezza e semplicità.

 

 





