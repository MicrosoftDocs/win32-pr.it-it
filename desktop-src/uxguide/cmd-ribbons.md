---
title: Barre multifunzione
description: Le barre multifunzione sono il modo moderno per aiutare gli utenti a trovare, comprendere e usare i comandi in modo efficiente e diretto, con un numero minimo di clic, con una minore necessità di ricorrere a tentativi ed errori e senza dover fare riferimento alla guida.
ms.assetid: 8a4699da-9840-4622-9e94-d6d5c4e7708c
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2327a633f02c9d56116367405803c4da56ad5b19
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351026"
---
# <a name="ribbons"></a>Barre multifunzione

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Le barre multifunzione sono il modo moderno per aiutare gli utenti a trovare, comprendere e usare i comandi in modo efficiente e diretto con un numero minimo di clic, con una minore necessità di ricorrere a tentativi ed errori e senza dover fare riferimento alla guida.

Una barra multifunzione è una barra dei comandi che organizza le funzionalità di un programma in una serie di schede nella parte superiore di una finestra. L'uso di una barra multifunzione aumenta l'individuabilità delle funzionalità e delle funzioni, consente un apprendimento più rapido del programma nel suo complesso e rende gli utenti più esperti a controllare la propria esperienza con il programma. Una barra multifunzione può sostituire la barra dei menu e le barre degli strumenti tradizionali.

![Screenshot di una barra multifunzione ](images/cmd-ribbons-image1.png)

Una barra multifunzione tipica.

Le schede della barra multifunzione sono costituite da gruppi, ovvero un set con etichetta di comandi strettamente correlati. Oltre a schede e gruppi, le barre multifunzione sono costituite da:

- Pulsante dell'applicazione, che presenta un menu di comandi che comportano l'operazione in o con un documento o un'area di lavoro, ad esempio i comandi correlati ai file.
- Barra di accesso rapido, una piccola barra degli strumenti personalizzabile che Visualizza i comandi utilizzati di frequente.
- Le schede principali sono le schede che vengono sempre visualizzate.
- Le schede contestuali, che vengono visualizzate solo quando viene selezionato un particolare tipo di oggetto. Le schede che vengono sempre visualizzate sono denominate schede principali.
- Un set di schede è una raccolta di schede contestuali per un singolo tipo di oggetto. Poiché gli oggetti possono avere più tipi (ad esempio, un'intestazione in una tabella che dispone di un'immagine è costituita da tre tipi), è possibile che vengano visualizzati più set di schede contestuali alla volta.
- Le schede modali, ovvero le schede principali visualizzate con una particolare modalità temporanea, ad esempio anteprima di stampa.
- Raccolte, ovvero elenchi di comandi o opzioni presentate graficamente. Una raccolta basata sui risultati illustra l'effetto dei comandi o delle opzioni anziché dei comandi stessi. Una raccolta della barra multifunzione viene visualizzata in una barra multifunzione anziché in una finestra popup.
- Descrizioni comando avanzate, che illustrano in modo conciso i comandi associati e forniscono i tasti di scelta rapida. Possono inoltre includere elementi grafici e riferimenti alla guida. Le descrizioni comando migliorate riducono la necessità di guida.
- I pulsanti di avvio della finestra di dialogo, ovvero i pulsanti nella parte inferiore di alcuni gruppi che aprono le finestre di dialogo contenenti le funzionalità correlate al gruppo.

Le barre multifunzione sono state introdotte originariamente con Microsoft Office 2007. Per informazioni sui motivi per cui Office deve usare le barre multifunzione e i molti problemi che usano una barra multifunzione, vedere [la storia della barra](/archive/blogs/jensenh/the-story-of-the-ribbon)multifunzione.

> [!Note]  
> Le linee guida relative a [menu](cmd-menus.md), [barre degli strumenti](cmd-toolbars.md), [pulsanti di comando](ctrl-command-buttons.md)e [Icone](vis-icons.md) sono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere di usare una barra multifunzione, prendere in considerazione le domande seguenti:

### <a name="program-type"></a>Tipo di programma

- **Quale tipo di programma si sta progettando?** Il tipo di programma è un indicatore appropriato della correttezza di una barra multifunzione. Le barre multifunzione sono ideali per la creazione e la creazione di documenti, nonché per i visualizzatori e i browser dei documenti. Le barre multifunzione potrebbero funzionare per altri tipi di programmi, ma altre forme di presentazione dei comandi potrebbero essere più appropriate. In genere, i programmi leggeri devono avere una presentazione semplice del comando.

### <a name="discoverability-and-learning-issues"></a>Problemi di individuabilità e apprendimento

- **Gli utenti non riescono a trovare i comandi? Gli utenti richiedono funzionalità già presenti nel programma?** In tal caso, l'utilizzo di una barra multifunzione renderà i comandi più semplici da trovare con etichette e raggruppamento di comandi correlati. L'uso di una barra multifunzione è anche più efficace delle barre dei menu e delle barre degli strumenti per la crescita futura
- **Gli utenti non riescono a comprendere i comandi del programma? Spesso ricorrono a "versione di valutazione ed errore" per selezionare il comando corretto o determinare il funzionamento dei comandi?** In tal caso, l'utilizzo di una barra multifunzione con comandi orientati ai risultati basati su raccolte e anteprime in tempo reale rende i comandi più facili da comprendere.

### <a name="command-characteristics"></a>Caratteristiche del comando

- **I comandi sono presentati in diverse posizioni? Se il programma esiste già, i comandi vengono visualizzati nelle barre dei menu, nelle barre degli strumenti, nei riquadri attività e all'interno dell'area di lavoro?** In tal caso, l'utilizzo di una barra multifunzione consentirà di unificare i comandi in un'unica posizione, rendendoli più facili da trovare.
- **I comandi si applicano all'intera finestra o solo a riquadri specifici?** Le barre multifunzione funzionano meglio per i comandi che si applicano all'intera finestra o a oggetti specifici. I comandi sul posto funzionano meglio per i singoli riquadri della finestra.
- **La maggior parte dei comandi può essere presentata direttamente? Ovvero, gli utenti possono interagire con loro usando un solo clic? Se si accede ai comandi di uso comune da menu e finestre di dialogo, è possibile effettuarne il refactoring in modo che siano diretti?** Mentre alcuni comandi possono essere presentati usando menu e finestre di dialogo, presentando la maggior parte dei comandi in questo modo, è possibile rendere una barra dei menu una scelta migliore.

### <a name="command-scale"></a>Scala comandi

- **È presente un numero ridotto di comandi? I comandi usati più di frequente possono essere presentati facilmente su una singola barra degli strumenti semplice?** L'uso di una barra multifunzione è utile se l'aggiunta di schede di base e contestuali produce una semplice scheda Home che può essere usata da sola per eseguire le attività più comuni. In caso contrario, il vantaggio derivante dall'utilizzo di una barra multifunzione potrebbe non giustificare il peso aggiuntivo per un numero ridotto di comandi.
- **Esiste un numero elevato di comandi? Usare una barra multifunzione richiede più di sette schede core? Gli utenti dovranno continuamente modificare le schede per eseguire attività comuni?** In tal caso, usando le barre degli strumenti (che non richiedono la modifica delle schede) e le [finestre della tavolozza](cmd-toolbars.md) (che potrebbero richiedere la modifica delle schede, ma possono essere aperte diverse volte), potrebbe essere una scelta più efficiente.
- **Gli utenti tendono a usare un numero ridotto di comandi la maggior parte del tempo?** In tal caso, è possibile utilizzare una barra multifunzione inserendo tali comandi nella scheda Home. Le schede che cambiano continuamente rendono una barra multifunzione troppo inefficiente.
- **Il programma può trarre vantaggio dal fatto che l'area di contenuto del programma è il più grande possibile?** In tal caso, l'utilizzo di una barra dei menu e di una singola barra degli strumenti è più efficiente rispetto a una barra multifunzione. Tuttavia, se il programma richiede tre o più righe di barre degli strumenti o utilizza i riquadri attività, l'utilizzo di una barra multifunzione è più efficiente dello spazio.
- **Gli utenti tendono a lavorare in un'area specifica all'interno di una finestra di grandi dimensioni del programma per lunghi periodi di tempo?** In tal caso, trarrebbero vantaggio dalla vicinanza di mini-barre degli strumenti, finestre della tavolozza e comandi diretti. Rendere il round trip dall'area di lavoro alla barra multifunzione sarebbe troppo inefficiente.
- **Per migliorare l'efficienza e la flessibilità, gli utenti devono apportare modifiche significative al contenuto, alla posizione o alle dimensioni della presentazione del comando?** In tal caso, è preferibile scegliere le finestre degli strumenti e delle tavolozze personalizzabili ed estendibili. Si noti che alcuni tipi di barre degli strumenti possono essere disancorati per diventare finestre della tavolozza e le finestre della tavolozza possono essere spostate, ridimensionate e personalizzate.

Infine, si consideri questa domanda fondamentale: **è il miglioramento di individuabilità, facilità di apprendimento, efficienza e produttività, vale a dire il costo dello spazio aggiuntivo e la necessità di schede per organizzare i comandi?** In tal caso, l'utilizzo di una barra multifunzione è un'ottima scelta. Se non si è certi, provare a eseguire il test di usabilità di una progettazione basata sulla barra multifunzione e a confrontarla con la migliore alternativa.

Le barre multifunzione sono una forma nuova e accattivante della presentazione dei comandi e un ottimo modo per modernizzare un programma. Tuttavia, non è la scelta ideale per ogni programma.

**Non corretto:**

![Screenshot di una barra multifunzione con una calcolatrice ](images/cmd-ribbons-image2.png)

Non eseguire questa operazione.

## <a name="seven-most-important-things"></a>Sette elementi più importanti

1. Scegliere una soluzione di comando adatta per il tipo di programma. L'uso di una barra multifunzione deve rendere un programma più semplice, più efficiente e più semplice da usare mai l'opposto. Se l'uso di una barra multifunzione non è appropriato, è consigliabile usare invece comandi avanzati.  
2. Non sottovalutare la necessità di creare una barra multifunzione efficace. Non aspettatevi una semplice porta delle barre dei menu e delle barre degli strumenti esistenti. E non è necessario che l'uso di una barra multifunzione renda automaticamente il programma migliore. Essere disposti a eseguire il commit del tempo e del lavoro richiesto per una riprogettazione dei comandi è un fattore importante nella decisione di usare una barra multifunzione.  
3. Rendere individuabili i comandi. Scegliere una struttura a schede con un mapping chiaro, ovvio e univoco tra i comandi e le schede con etichetta descrittivo in cui risiedono. Gli utenti devono essere in grado di determinare in modo rapido e sicuro quale scheda dispone del comando cercato e raramente di scegliere la scheda errata.  
4. Rendere i comandi autoesplicativi. Gli utenti devono comprendere l'effetto di un comando dell'etichetta, dell'icona, della descrizione comando e dell'anteprima. Non dovrebbero sperimentare o leggere un argomento della Guida per vedere come funziona un comando.  
5. Usare i comandi in modo efficiente:
    - Gli utenti devono dedicare la maggior parte del tempo alla scheda Home.
    - Gli utenti devono raramente modificare le schede durante le attività comuni.
    - Quando la finestra è ingrandita e gli utenti si trovano nella scheda corretta, i comandi usati più di frequente hanno la massima enfasi visiva e gli utenti possono richiamarli con un solo clic. Gli utenti possono eseguire tutti gli altri comandi nella scheda con al massimo quattro clic.
    - Gli utenti non devono aprire finestre di dialogo per fornire comandi e modificare gli attributi nelle attività comuni.
6. Consentire agli utenti di scegliere i comandi e le opzioni in modo sicuro e ridurre al minimo la necessità di tentativi ed errori. Usare i comandi orientati ai risultati ogni volta che è appropriato, spesso sotto forma di raccolte e anteprime in tempo reale.  
7. Assicurarsi che la barra multifunzione venga ridimensionata correttamente dalle dimensioni massime della finestra fino al più piccolo.  

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="adapting-a-ribbon-in-an-existing-program"></a>Adattamento di una barra multifunzione in un programma esistente

Sebbene sia possibile eseguire il refactoring di una barra dei menu tradizionale e della progettazione di una barra degli strumenti di un programma esistente a un formato della barra multifunzione. Le barre multifunzione presentano il maggior valore quando vengono usate per presentare comandi immediatamente orientati ai risultati, spesso sotto forma di raccolte e anteprime in tempo reale. I comandi orientati ai risultati semplificano la comprensione e la produttività degli utenti. Invece di effettuare il refactoring dei comandi esistenti, è preferibile riprogettare completamente il modo in cui vengono eseguiti i comandi nel programma.

Non sottovalutare la necessità di creare una barra multifunzione efficace. E non è necessario che l'uso di una barra multifunzione renda automaticamente il programma migliore. La creazione di una barra multifunzione efficace richiede molto tempo e fatica. Essere disposti a eseguire il commit del tempo e del lavoro richiesto per la riprogettazione di un comando di questo tipo è un fattore importante nella decisione di usare una barra multifunzione.

### <a name="the-nature-of-ribbons"></a>La natura delle barre multifunzione

Rispetto alle barre dei menu e alle barre degli strumenti tradizionali, le barre multifunzione presentano le caratteristiche seguenti:

- **Interfaccia utente singola per tutti i comandi.** Le barre dei menu sono complete e facili da imparare, le barre degli strumenti sono efficienti e dirette, ma perché non usare più spazio sullo schermo per creare un'interfaccia utente di comandi singola che li esegue? Con una sola interfaccia utente, le barre multifunzione non richiedono che gli utenti scoprano l'interfaccia utente che ha il comando che sta cercando.
- **Visibile e autoesplicativo.** I comandi della barra dei menu sono autoesplicativi tramite le relative etichette, ma sono nascosti nella maggior parte dei casi. Per risparmiare spazio sullo schermo, i pulsanti della barra degli strumenti sono rappresentati principalmente da icone anziché etichette (sebbene alcuni pulsanti della barra degli strumenti usino entrambi) e dipendano dalle descrizioni comandi quando l'icona non è di chiara comprensione. Tuttavia, gli utenti in genere conoscono le icone solo per i comandi usati più di frequente.
- Presentando la maggior parte dei comandi con icone etichettate, i comandi della barra multifunzione sono visibili e autoesplicativi e usano le descrizioni comandi solo per fornire informazioni aggiuntive. Non è necessario andare altrove (ad esempio la guida) per comprendere un comando.
- **Raggruppamento con etichetta.** Mentre le categorie di menu sono etichettate, i gruppi in un menu a discesa non sono e sono indicati solo con un separatore senza etichetta. I gruppi nelle barre degli strumenti sono indicati anche con separatori senza etichetta.
- Organizzando i comandi in gruppi con etichetta, le barre multifunzione semplificano la ricerca dei comandi e ne determinano lo scopo.
- **Modale ma non gerarchico.** Ridimensiona le barre dei menu creando una gerarchia di comandi. I menu con molti elementi possono usare uno o più livelli di sottomenu per fornire più comandi.
- I comandi della barra multifunzione richiedono più spazio rispetto ai comandi della barra degli strumenti, quindi usano le schede per ridimensionare Questo utilizzo delle schede rende le barre multifunzione modali, richiedendo agli utenti di modificare le modalità occasionalmente per trovare i comandi. Tuttavia, all'interno di una scheda la maggior parte dei comandi è diretta o usa un solo pulsante di menu combinato o un pulsante di menu, non una gerarchia.
- **Diretta e immediata.** Un comando è diretto se richiamato con un solo clic, ovvero senza spostarsi tra i menu, e immediato se viene applicato immediatamente (ovvero senza finestre di dialogo per raccogliere input aggiuntivi). I comandi della barra dei menu sono sempre indiretti e spesso non immediati. Analogamente alle barre degli strumenti, la maggior parte dei comandi della barra multifunzione sono progettati per essere diretti e immediati, con i comandi usati più di frequente con un solo clic e senza la necessità di una finestra di dialogo per raccogliere input aggiuntivi.
- **Spazioso.** Le barre dei menu e le barre degli strumenti sono progettate principalmente per garantire una maggiore efficienza dello spazio. Per fornire i propri vantaggi, le barre multifunzione possono utilizzare più spazio verticale, ovvero approssimativamente l'equivalente di una barra dei menu più tre righe di barre degli strumenti. Poiché pochi programmi includono tre o più righe di barre degli strumenti, le barre multifunzione utilizzano in genere più spazio rispetto alle interfacce utente tradizionali per i comandi.
- **Dispone di un pulsante applicazione e di una barra di accesso rapido.** Una barra multifunzione viene sempre visualizzata con un pulsante applicazione e una barra di accesso rapido. Questa operazione consente agli utenti di accedere ai comandi di uso frequente e correlati ai file senza modificare le schede e promuove la coerenza tra i programmi.
- **Personalizzazione minima.** Mentre le barre dei menu hanno una presentazione fissa, molte barre degli strumenti sono piuttosto personalizzabili, consentendo agli utenti di impostare posizioni, dimensioni e contenuti. Una barra multifunzione non è personalizzabile, ma la barra di accesso rapido fornisce una personalizzazione limitata.
- **Maggiore accessibilità da tastiera.** Le barre dei menu hanno un'eccellente accessibilità da tastiera perché premendo il tasto ALT viene direttamente visualizzato lo stato attivo di input della barra dei menu Tuttavia, non esiste un meccanismo di questo tipo per le barre degli strumenti perché condividono la navigazione tramite tastiera con il contenuto della finestra. Di conseguenza, gli utenti devono passare alla barra degli strumenti usando il tasto TAB (a cui viene assegnato l'ultimo Tab), quindi passare a un comando specifico usando i tasti di direzione.

Al contrario, le barre multifunzione forniscono una maggiore accessibilità da tastiera tramite [suggerimenti](glossary.md)per i tasti, in genere con un processo in tre passaggi:

- Premere ALT per attivare la modalità suggerimento.
- Premere un carattere per scegliere una scheda, il pulsante dell'applicazione o un comando nella barra di accesso rapido.
- In una scheda premere una o due lettere per scegliere un comando.

    Questo approccio è molto visivo. È anche più flessibile, consentendo una migliore scalabilità e un numero maggiore di assegnazioni di chiavi di accesso.

    Non confondere le chiavi di accesso con i tasti di scelta rapida. Sebbene sia le chiavi di accesso che i tasti di scelta rapida forniscano l'accesso tramite tastiera all'interfaccia utente, hanno scopi e linee guida diversi. Per ulteriori informazioni, vedere [tastiera](inter-keyboard.md).

### <a name="the-nature-of-rich-commands"></a>La natura dei comandi avanzati

I comandi avanzati fanno riferimento alla presentazione e all'interazione dei comandi usati dalle barre multifunzione, senza necessariamente usare un contenitore della barra multifunzione. I comandi avanzati presentano queste caratteristiche:

- **Etichette.** A tutti i comandi vengono assegnate etichette autoesplicative, con eccezioni solo quando le icone sono estremamente note e lo spazio è a un livello Premium.

    **Corretto:**

    ![screenshot della barra multifunzione per la formattazione dei caratteri ](images/cmd-ribbons-image3.png)

    Questi comandi sono molto noti, quindi non necessitano di etichette.

    **Non corretto:**

    ![Screenshot di una barra multifunzione con icone usate raramente ](images/cmd-ribbons-image4.png)

    Queste icone non intelligibili richiedono etichette per i comandi avanzati.

- **Ridimensionamento.** Anziché il ridimensionamento uniforme, i comandi vengono dimensionati in relazione alla relativa frequenza di utilizzo e importanza. Oltre a rendere più facili da trovare e fare clic sui comandi usati più di frequente, è possibile renderli più [ritoccabili](https://msdn.microsoft.com/library/windows/desktop/cc872774.aspx).

    ![Screenshot di uno o tre pulsanti di grandi dimensioni ](images/cmd-ribbons-image5.png)

    In questo esempio il pulsante usato più di frequente è maggiore di quello degli altri.

- **Dimensionamento dinamico.** I controlli Rich Command si ridimensionano per sfruttare al meglio lo spazio disponibile, anziché usare una dimensione fissa e troncare o usare l'overflow quando le dimensioni sono troppo ridotte.

    ![screenshot della barra multifunzione ampia con pulsanti di uguale dimensione ](images/cmd-ribbons-image6.png)![screenshot della barra multifunzione di piccole dimensioni con pulsanti misti ](images/cmd-ribbons-image7.png)

    In questo esempio, i pulsanti di comando vengono ridimensionati per funzionare correttamente nello spazio disponibile.

- **Pulsanti di divisione.** I pulsanti di suddivisione sono un buon metodo per consolidare un set di varianti di un comando quando necessario, mantenendo al tempo stesso la direzione del comando usato più di frequente.

    ![screenshot del comando Salva con nome e delle relative opzioni ](images/cmd-ribbons-image8.png)

    In questo esempio, il comando Salva con nome utilizza un pulsante di menu combinato, in cui il pulsante principale esegue la variazione più comune e la parte di menu Visualizza un menu con varianti del comando.

- **Menu a discesa e raccolte avanzate.** I menu a discesa, gli elenchi a discesa e le raccolte hanno lo spazio necessario per comunicare e distinguere l'effetto delle scelte, spesso usando descrizioni di testo e grafica. Le categorie vengono usate per organizzare set di opzioni di grandi dimensioni.

    ![screenshot delle opzioni del menu a discesa con icone ](images/cmd-ribbons-image9.png)

    In questi esempi, facendo clic su un pulsante di menu viene visualizzato un elenco di opzioni che ne mostrano l'effetto.

- **Anteprime in tempo reale.** Quando l'utente passa il mouse su un'opzione di formattazione, il programma mostra i risultati con tale formattazione usando il contenuto effettivo.

    ![screenshot dei risultati delle scelte di formattazione ](images/cmd-ribbons-image10.png)

    Le anteprime in tempo reale mostrano i risultati dell'applicazione di un'opzione di formattazione al passaggio del mouse.

- **Descrizioni comando migliorate.** Questi spiegano brevemente i comandi associati e forniscono i tasti di scelta rapida. Possono anche includere elementi grafici e riferimenti alla guida (anche se eliminano in gran parte la necessità della Guida correlata ai comandi).

    ![screenshot della descrizione comando di grandi dimensioni con testo e grafica ](images/cmd-ribbons-image11.png)

    Descrizioni comando avanzate spiegano in modo conciso i comandi associati.

Sebbene le barre multifunzione potrebbero non essere adatte per tutti i programmi, tutti i programmi possono trarre vantaggio da comandi avanzati.

### <a name="ribbons-always-have-an-application-button-and-quick-access-toolbar"></a>Le barre multifunzione hanno sempre un pulsante applicazione e una barra di accesso rapido

Il pulsante applicazione e la barra di accesso rapido forniscono comandi utili in qualsiasi contesto, riducendo così la necessità di modificare le schede. Sebbene questi tre componenti siano logicamente indipendenti, una barra multifunzione deve avere sempre un pulsante applicazione e una barra di accesso rapido. Dato che i comandi possono andare sulla barra multifunzione o sul pulsante dell'applicazione, è possibile chiedersi dove posizionare i comandi. La scelta non è arbitraria.

Il pulsante applicazione viene usato per presentare un menu di comandi che comportano l'operazione o con un file, ad esempio i comandi che tradizionalmente passano al menu file per creare, aprire e salvare file, stampare e inviare e pubblicare documenti.

Al contrario, la barra multifunzione è per i comandi che influiscono sul contenuto della finestra. Gli esempi includono i comandi usati per leggere, modificare o usare il contenuto oppure modificare la visualizzazione.

Se si usa una barra multifunzione, è necessario usare anche un pulsante dell'applicazione anche se il programma non include documenti o file. In questi casi, usare il menu applicazione per presentare i comandi per la stampa, le opzioni di programma e l'uscita dal programma. Sebbene il pulsante dell'applicazione non sia necessario per tali programmi, l'utilizzo di questa funzionalità garantisce la coerenza tra i diversi programmi. Gli utenti non devono cercare i comandi Save e Undo o le opzioni del programma perché si trovano sempre nella stessa posizione.

La barra di accesso rapido è necessaria anche se la barra multifunzione usa solo una scheda. Anche in questo caso questi programmi non necessitano di una barra di accesso rapido (poiché tutti i comandi sono già presenti nella scheda singola), con una barra di accesso rapido personalizzabile che garantisce la coerenza tra i programmi. Ad esempio, se gli utenti hanno la possibilità di fare clic sul comando stampa, dovrebbero essere in grado di eseguire questa operazione in qualsiasi programma che usa una barra multifunzione.

### <a name="organization-and-discoverability"></a>Organizzazione e individuabilità

Fornendo schede e gruppi, le barre multifunzione consentono di organizzare i comandi per facilitare l'individuabilità. Il problema è che, se l'organizzazione viene eseguita in modo non corretto, può causare un notevole rischio di individuabilità. Dovrebbe esserci un mapping chiaro, ovvio ed univoco tra i comandi e le schede e i gruppi con etichetta descrittivo in cui risiedono.

Gli utenti formerà un modello mentale della barra multifunzione dopo averlo usato per un periodo di tempo. Se il modello mentale non ha senso per gli utenti, è inefficiente o non è corretto, comporterà confusione e frustrazione. **L'obiettivo più importante nella progettazione di una barra multifunzione consiste nel semplificare la ricerca dei comandi in modo rapido e sicuro. Se non si esegue questa operazione, la progettazione della barra multifunzione avrà esito negativo.** Il raggiungimento di questo obiettivo richiede un'attenta progettazione, un test utente e un'iterazione. Non presupporre che sia semplice.

Di seguito sono riportate alcune trappole comuni da evitare:

- **Evitare i nomi di schede e gruppi generici.** Una scheda o un nome di gruppo valido deve descrivere accuratamente il contenuto specifico, preferibilmente usando il linguaggio basato su attività e obiettivo. Evitare nomi di schede e gruppi generici, nonché nomi basati su tecnologia. Ad esempio, quasi tutti i comandi in un documento creazione e modifica di un programma potrebbero appartenere a schede con etichetta modifica, formato, strumenti, opzioni, avanzate e altro ancora. Si basano su etichette descrittive specifiche, non sulla memorizzazione.
- **Evitare i nomi di schede e gruppi eccessivamente specifici.** Anche se si vuole che i nomi di tabulazione e gruppo siano specifici, non dovrebbero essere così specifici che gli utenti siano sorpresi dal contenuto. Spesso gli utenti ricercano elementi che usano il processo di eliminazione, quindi impediscono la vista delle schede o dei gruppi, perché il nome è fuorviante.
- **Evitare più percorsi dello stesso comando, soprattutto se il percorso è imprevisto o se il comando richiede molti clic per richiamare.** Potrebbe sembrare una praticità trovare un comando tramite più percorsi. Tenere presente che, quando gli utenti trovano quello che cercano, si fermano alla ricerca. È troppo facile per gli utenti presumere che il primo percorso trovato sia l'unico percorso che rappresenta un problema grave se il percorso è inefficiente o imprevisto. Inoltre, la presenza di comandi duplicati rende più difficile per gli utenti trovare altri comandi per i quali sta eseguendo l'analisi.

![screenshot del comando percorso indiretto per i bordi ](images/cmd-ribbons-image12.png)

In questo esempio, è possibile modificare i bordi del paragrafo tramite il comando di bordi della pagina, anche se è presente un percorso più diretto nella scheda Home. Se gli utenti che cercano i bordi dei paragrafi hanno dovuto inciampare in questo percorso imprevisto, potrebbero facilmente supporre che si tratta dell'unico percorso.

- **Evitare la posizione arbitraria del comando.** Si supponga di disporre di una corretta progettazione di schede e gruppi, ma di scoprire che diversi comandi non rientrano. È probabile che la progettazione della scheda e del gruppo non sia una scelta ottimale e che sia necessario continuare a perfezionarla. Non risolvere questo problema inserendo i comandi in cui non appartengono. In tal caso, è probabile che gli utenti debbano controllare ogni scheda per trovarle, quindi dimenticare immediatamente dove si trovano.
- **Evitare la selezione host basata sul marketing.** Si supponga di disporre di una nuova versione del programma e che il team di marketing voglia realmente promuovere le nuove funzionalità. È possibile che si stia tentando di inserirli nella scheda Home, ma in questo caso si tratta di un errore costoso se l'individuabilità complessiva è danneggiata. Si prendano in considerazione le versioni future del prodotto e la frustrazione di un'organizzazione in costante evoluzione.

### <a name="tabs"></a>Schede

Il primo passaggio migliore consiste nel rivedere le [schede della barra multifunzione standard](#standard-ribbon-tabs). Se i comandi del programma si mappano naturalmente alle schede standard, basare l'organizzazione sulla scheda su questi standard. D'altra parte, se i comandi del programma non vengono mappati naturalmente, non provare a forzarlo. Determinare una struttura più naturale e assicurarsi di eseguire una grande quantità di test utente per assicurarsi di avere il giusto.

Per le schede non standard, considerare questi problemi:

- **Ogni nome di scheda deve descrivere il contenuto.** Scegliere nomi significativi specifici, ma non troppo specifici. Gli utenti non devono mai essere sorpresi dal contenuto.
- **Ogni nome di scheda deve rifletterne lo scopo.** Prendere in considerazione l'obiettivo o l'attività associata ai comandi.
- **Ogni nome di scheda deve essere chiaramente distinto da tutti gli altri nomi di scheda.**

La scheda Home è un'eccezione a queste considerazioni. Anche se non è necessario disporre di una scheda Home, la maggior parte dei programmi dovrebbe. La scheda Home è la prima scheda e contiene i comandi usati più di frequente. Se i comandi usati di frequente non rientrano nelle altre schede, la scheda Home è la posizione giusta.

Se non è possibile determinare un nome descrittivo della scheda significativo, probabilmente è perché la scheda non è ben progettata. Se l'organizzazione della barra multifunzione non funziona, riconsiderare la progettazione della scheda.

### <a name="groups"></a>Gruppi

Suddividendo i comandi in gruppi si strutturano i comandi in set correlati. L'etichetta del gruppo illustra lo scopo comune dei comandi.

Quando si determinano i gruppi e la relativa presentazione, è necessario prendere in considerazione diversi fattori:

- **Raggruppamento standard.** Sebbene esistano differenze significative nei comandi tra i vari programmi, sono disponibili [gruppi standard](#standard-ribbon-groups) comuni tra più programmi. La visualizzazione di questi comandi con gli stessi nomi e posizioni simili migliora notevolmente l'individuabilità.

| Risposta esatta.                                                                                      | Non corretto                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| ![screenshot dello zoom separato dal gruppo di modifica ](images/cmd-ribbons-image13.png)<br/>Il gruppo di comandi di modifica include tutti i comandi di modifica, ma non include il comando zoom.         | ![screenshot dello zoom incluso nel gruppo di modifica ](images/cmd-ribbons-image14.png)<br/>Il comando zoom non è un comando di modifica, ma si trova nel gruppo di modifica. |

- **Granularità.** Una struttura è buona, ma una struttura eccessiva rende più difficile trovare i comandi. Se i nomi dei gruppi sono generici, è possibile che non si disponga di granularità sufficiente. Se sono presenti gruppi con uno o due comandi ciascuno, è probabile che si disponga di una quantità eccessiva (anche se è accettabile disporre di una raccolta nella barra multifunzione senza altri comandi all'interno di un gruppo).

| Risposta esatta.                                                                                                 | Non corretto                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![screenshot dello zoom separato dal gruppo di modifica ](images/cmd-ribbons-image13.png)<br/> Il gruppo di comandi di modifica include tutti i comandi di modifica| ![screenshot del gruppo di modifica suddiviso in due gruppi ](images/cmd-ribbons-image15.png)<br/>Il gruppo di comandi di modifica è stato suddiviso in sezioni troppo granulari. Evitare i gruppi con uno o due comandi.|

- **Nomi.** I nomi di gruppo validi spiegano lo scopo dei comandi. Se i nomi dei gruppi non sono, riconsiderare il nome o il raggruppamento. Se non è possibile determinare un nome descrittivo significativo, è probabile che il gruppo non sia ben progettato.

| Risposta esatta.                                                                                                 | Non corretto                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![screenshot dei comandi divisi in quattro gruppi ](images/cmd-ribbons-image17.png) <br/> Utilizzare nomi di gruppi sufficientemente specifici per descrivere i comandi contenuti nel gruppo. | ![screenshot del gruppo di formato con diversi comandi ](images/cmd-ribbons-image16.png) <br/> Il nome del gruppo è troppo vago per essere utile. Un approccio migliore consiste nel riorganizzare questi comandi in gruppi più specifici. |

- **Ordine.** Le persone leggono in un ordine da sinistra a destra (nelle impostazioni cultura occidentali), pertanto si potrebbe pensare che i gruppi nell'estrema sinistra siano i più evidenti. Tuttavia, il nome della scheda evidenziato e il contenuto della finestra tendono a fungere da [punti focali](vis-layout.md), quindi i gruppi al centro della scheda in genere ricevono maggiore attenzione rispetto al gruppo più a sinistra. Inserire i gruppi usati più di frequente nelle posizioni più importanti e verificare che sia presente un flusso logico per i gruppi nella scheda.

![screenshot del gruppo Appunti all'estrema sinistra ](images/cmd-ribbons-image18.png)

In questo esempio, il tipo di carattere e i gruppi di paragrafi sono più evidenti del gruppo degli Appunti, perché sono gli elementi che l'occhio vede prima durante lo stato di trasferimento dal documento.

![screenshot del gruppo di rilevamento nella scheda Revisione ](images/cmd-ribbons-image19.png)

In questo esempio, il gruppo di rilevamento riceve la massima attenzione, in parte perché la scheda di revisione evidenziata funge da punto focale.

- **Uniformità.** Può essere difficile riconoscere i comandi quando la presentazione del comando ha lo stesso aspetto. L'uso di icone con forme e colori diversi, gruppi con formati variabili e comandi con dimensioni diverse rende più semplice per gli utenti riconoscere i gruppi di comandi. I comandi devono avere un dimensionamento uniforme solo quando la barra multifunzione viene ridotta alle dimensioni più piccole.

| Risposta esatta. | Non corretto |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![screenshot del gruppo con icone di dimensioni diverse ](images/cmd-ribbons-image20.png)<br/>Utilizzare un'ampia gamma di dimensioni delle icone per migliorare la riconoscibilità| ![screenshot del gruppo con icone con le stesse dimensioni ](images/cmd-ribbons-image21.png)<br/>Questi comandi hanno un aspetto troppo simile, perché hanno tutte le stesse dimensioni. |

### <a name="previews"></a>Anteprime

È possibile utilizzare vari tipi di anteprime per mostrare il risultato di un comando. Grazie alle anteprime utili, è possibile migliorare l'efficienza del programma e ridurre la necessità di un approccio di apprendimento per la valutazione e l'errore. Le anteprime in tempo reale invitano anche la sperimentazione e incoraggiare la creatività.

Ecco alcuni dei diversi tipi di anteprime che è possibile usare:

- **Icone e grafica statiche realistiche.** Immagini statiche che forniscono un'indicazione realistica dell'effetto di un comando. Questi possono essere usati in raccolte, menu a discesa e descrizioni comando migliorate.

![screenshot dell'elenco a discesa dei tipi di carattere ](images/cmd-ribbons-image22.png)

In questo esempio, nell'elenco a discesa tipo di carattere viene visualizzato il nome del tipo di carattere usando il tipo di carattere stesso.

![screenshot della raccolta di anteprime della filigrana ](images/cmd-ribbons-image23.png)

In questo esempio, le anteprime realistiche vengono usate per mostrare le diverse filigrane.

- **Icone dinamiche e grafica.** Icone e grafica modificate per riflettere lo stato corrente. Queste icone sono particolarmente utili per le raccolte, oltre ai pulsanti di suddivisione che modificano l'effetto predefinito in modo che corrispondano all'ultima azione.

![screenshot della raccolta di stili paragrafi ](images/cmd-ribbons-image24.png)

In questo esempio Microsoft Word modifica la raccolta di stili in modo da riflettere gli stili correnti.

![screenshot dei pulsanti di comando per la formattazione del testo ](images/cmd-ribbons-image25.png)

In questo esempio, Word modifica il colore di evidenziazione del testo e i comandi colore del carattere per indicare l'effetto corrente.

- **Anteprime in tempo reale.** Quando gli utenti passa il mouse su un'opzione di formattazione, l'anteprima in tempo reale Mostra i risultati con tale formattazione. Le anteprime attive consentono agli utenti di effettuare selezioni in modo più efficiente e sicuro in base al contesto effettivo dell'utente.

![screenshot del selettore colori del comando colore pagina ](images/cmd-ribbons-image26.png)

In questo esempio, il comando colore pagina esegue un'anteprima in tempo reale mostrando l'effetto delle opzioni di colore al passaggio del mouse.

Le anteprime in tempo reale sono una potente funzionalità che consente di migliorare la produttività degli utenti, ma anche le anteprime statiche semplici possono essere molto utili.

### <a name="scaling-the-ribbon"></a>Ridimensionamento della barra multifunzione

Il ridimensionamento di una barra degli strumenti è semplice: se una finestra è troppo stretta per visualizzare una barra degli strumenti, la barra degli strumenti consente di visualizzare le corrispondenze e rende accessibili tutti gli altri tramite un pulsante di overflow Un obiettivo dei comandi avanzati consiste nel sfruttare appieno lo spazio disponibile, quindi la scalabilità di una barra multifunzione richiede un maggior lavoro di progettazione. Non sono disponibili dimensioni predefinite della barra multifunzione, pertanto non è consigliabile progettare una barra multifunzione con una larghezza particolare. È necessario progettare layout con una vasta gamma di larghezze e tenere presente che uno di essi potrebbe essere quello che verrà visualizzato dalla maggior parte degli utenti. La scalabilità è una parte fondamentale della progettazione della barra multifunzione, non dell'ultimo passaggio. Quando si progetta una scheda, specificare i diversi layout per ogni gruppo (fino a tre), nonché le combinazioni che possono essere usate insieme. Nella barra multifunzione viene visualizzata la combinazione valida più grande che corrisponde alla dimensione della finestra corrente.

![screenshot dei comandi di formattazione nelle barre degli strumenti del menu di overflow ](images/cmd-ribbons-image27.png) scalabile con un pulsante di overflow.

![screenshot delle barre multifunzione con diverse larghezze ](images/cmd-ribbons-image28.png) non è presente alcuna dimensione predefinita della barra multifunzione. La dimensione più piccola è una singola icona di gruppo popup.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

- **Non combinare nastri con barre dei menu e barre degli strumenti all'interno di una finestra.** Le barre multifunzione devono essere usate al posto delle barre dei menu e delle barre degli strumenti. Tuttavia, una barra multifunzione può essere combinata con le finestre della tavolozza e gli elementi di navigazione, ad esempio i pulsanti indietro e indietro e una barra degli indirizzi.
- **Combinare sempre una barra multifunzione con un pulsante applicazione e una barra di accesso rapido.**
- **Selezionare la scheda più a sinistra (in genere Home) quando viene avviato un programma.** Non fare in modo che l'ultima scheda selezionata venga mantenute tra le istanze del programma.
- **Mostra la barra multifunzione nello stato normale (non ridotta a icona) quando un programma viene avviato per la prima volta.** Spesso gli utenti lasciano invariate le impostazioni predefinite, quindi la riduzione della barra multifunzione all'avvio del programma provocherà probabilmente la minore efficienza di tutti i comandi. Inoltre, la visualizzazione della barra multifunzione inizialmente ridotta a icona può essere disorientata.
- **Rendere permanente lo stato della barra multifunzione tra le istanze del programma.** Ad esempio, se un utente riduce a icona la barra multifunzione, dovrebbe essere visualizzata a icona al successivo avvio del programma. Ma anche in questo caso non rendere la scheda dell'ultima selezionata in modo permanente.

### <a name="using-tabs"></a>Utilizzo di schede

Generalmente, la presenza di un minor numero di schede è migliore, quindi rimuovere le schede che non consentono di raggiungere questi obiettivi.

- **Quando possibile, utilizzare schede standard.** L'utilizzo di schede standard migliora notevolmente l'individuabilità, soprattutto nei programmi. Vedere le [schede della barra multifunzione standard](#standard-ribbon-tabs) più avanti in questo articolo.
- **Etichettare la prima scheda iniziale, se appropriato.** La scheda Home deve contenere i comandi usati più di frequente. Se i comandi usati di frequente non rientrano nelle altre schede, la scheda Home è la posizione giusta.
- Aggiungere una nuova scheda se:
  - **I comandi sono strettamente correlati a attività specifiche e possono essere descritti accuratamente dall'etichetta della scheda.** L'aggiunta della scheda dovrebbe semplificare la ricerca dei comandi, non più difficile.
  - **I comandi non sono correlati principalmente alle attività di altre schede.** Per aggiungere la scheda non è necessario cambiare la scheda durante le attività comunemente eseguite.
  - **La scheda dispone di comandi sufficienti per giustificare la presenza di una posizione aggiuntiva.** Non sono disponibili schede con pochi comandi. **Eccezione:** Si consiglia di aggiungere una scheda con pochi comandi se sono strettamente correlati a un'attività specifica e l'aggiunta della scheda semplifica notevolmente una scheda Home eccessivamente complessa.
- **Per le schede rimanenti, inserire prima le schede utilizzate più di frequente, mantenendo un ordine logico tra le schede.**
- **Ottimizzare la progettazione della scheda in modo che gli utenti trovino i comandi in modo rapido e sicuro.** Tutte le altre considerazioni sono secondarie.
- **Non fornire una scheda della guida.** Fornire invece assistenza usando la guida a livello di programma e le descrizioni comandi avanzate.
- **Usare un massimo di sette schede principali.** Se sono presenti più di sette, diventa difficile determinare la scheda con un comando. Sebbene sette schede principali siano accettabili per le applicazioni con molti comandi, la maggior parte dei programmi dovrebbe puntare a un massimo di quattro schede.

### <a name="contextual-tabs"></a>Schede contestuali

- **Usare una scheda contestuale per visualizzare una raccolta di comandi rilevanti solo quando gli utenti selezionano un particolare tipo di oggetto.** Se sono presenti solo alcuni comandi usati di frequente, può risultare più semplice e più stabile usare una scheda normale e disabilitare semplicemente i comandi quando non sono applicabili.
- ![screenshot dei comandi taglia e copia in grigio ](images/cmd-ribbons-image29.png)<br>È preferibile disabilitare i comandi comuni, come taglia e copia, anziché usare una scheda contestuale.
- **Includere solo i comandi specifici di un determinato tipo di oggetto.** Non inserire i comandi solo in una scheda contestuale Se gli utenti potrebbero renderli necessari senza prima selezionare un oggetto.
- **Includere i comandi utilizzati di frequente quando si utilizza un particolare tipo di oggetto.** Inserire i comandi contestuali generali usati di frequente nei menu di scelta rapida e nelle mini-barre degli strumenti per evitare il cambio di tabulazione durante le attività comunemente eseguite. In alternativa, è consigliabile inserire in modo ridondante i comandi generali in una scheda contestuale, in modo da evitare un frequente cambio di scheda. Ma non esagerare, non provare a includere tutti i comandi che potrebbero essere necessari a un utente durante l'uso dell'oggetto.
- ![screenshot del comando bordi nella scheda Progettazione ](images/cmd-ribbons-image30.png)<br/>In questo esempio, il comando Borders è incluso nella scheda Progettazione per evitare un frequente cambio di tabulazione durante le attività comunemente eseguite. \
- **Scegliere un colore di scheda contestuale diverso dalle schede contestuali attualmente visualizzate.** Lo stesso set di schede può essere visualizzato in un secondo momento usando un colore diverso per ottenere questo risultato, ma provare a usare assegnazioni di colore coerenti tra le chiamate quando possibile.
- **Selezionando una scheda contestuale** è possibile agevolare l'individuabilità, migliorare la percezione della stabilità e ridurre la necessità di cambiare le schede. Selezionare una scheda contestuale automaticamente nei casi seguenti:
  - **L'utente inserisce un oggetto.** In questo caso, selezionare la prima scheda contestuale nel set.
  - **L'utente fa doppio clic su un oggetto.** In questo caso, selezionare la prima scheda contestuale nel set.
  - **L'utente ha selezionato una scheda contestuale, ha fatto clic sull'oggetto, quindi ha fatto clic immediatamente su un oggetto dello stesso tipo.** In questo caso, tornare alla scheda contestuale selezionata in precedenza.
- **Quando si rimuove una scheda contestuale che è la scheda attivo, rendere la scheda Home o la prima scheda attiva.** Questa operazione viene visualizzata come la più stabile.

### <a name="modal-tabs"></a>Schede modali

- **Usare una scheda modale per visualizzare una raccolta di comandi che si applicano a una particolare modalità temporanea e nessuna delle schede principali.** Se si applicano alcune schede principali, usare invece una scheda contestuale e disabilitare i comandi che non si applicano. Poiché le schede modali sono molto limitate, devono essere usate solo quando non esiste un'alternativa migliore.
- ![screenshot della scheda Anteprima di stampa ](images/cmd-ribbons-image31.png)<br/>L'anteprima di stampa è una scheda modale comunemente usata.
- **Per chiudere una scheda modale, inserire il <mode> comando close come ultimo comando nella scheda.** Usare l'icona Chiudi per semplificare la ricerca del comando. Assegnare la modalità nel comando per evitare confusione sugli elementi da chiudere.
- ![cattura di schermata del pulsante Chiudi anteprima stampa ](images/cmd-ribbons-image32.png)<br/>In questo esempio, l'etichettatura esplicita del comando Close con la modalità consente di rimuovere eventuali dubbi sugli elementi da chiudere.
- **Per chiudere una scheda modale, ridefinire anche il pulsante Chiudi sulla barra del titolo della finestra per chiudere la modalità anziché il programma.** Il test utente ha dimostrato che molti utenti si aspettano questo comportamento.

### <a name="standard-ribbon-tabs"></a>Schede standard della barra multifunzione

Quando è possibile, eseguire il mapping dei comandi del programma a queste schede standard, in base all'ordine di visualizzazione standard.

#### <a name="regular-tabs"></a>Schede normali

- **Casa.** Contiene i comandi utilizzati più di frequente. Se usato, è sempre la prima scheda.
- **Inserire.** Contiene i comandi per inserire contenuto e oggetti in un documento. Se usato, è sempre la seconda scheda.
- **Layout di pagina.** Contiene i comandi che influiscono sul layout della pagina, inclusi i temi, l'impostazione della pagina, gli sfondi della pagina, il rientro, la spaziatura e il posizionamento. Si noti che i gruppi di rientri e spaziatura possono trovarsi nella scheda Home invece se lo spazio disponibile è sufficiente. Se usato, è sempre la terza scheda.
- **Recensione.** Contiene i comandi per aggiungere commenti, rilevare le modifiche e confrontare le versioni.
- **Visualizzare.** Contiene i comandi che influiscono sulla visualizzazione del documento, incluse la modalità di visualizzazione, le opzioni Mostra/Nascondi, lo zoom, la gestione delle finestre e le macro i comandi tradizionalmente disponibili nella categoria menu di Windows. Se utilizzata, si tratta dell'ultima scheda normale, a meno che non venga visualizzata la scheda dello sviluppatore.
- **Sviluppatore.** Contiene i comandi utilizzati solo dagli sviluppatori. Se usato, è nascosto per impostazione predefinita e viene visualizzata l'ultima scheda normale.

Per la maggior parte dei programmi non sono necessarie le schede Review e Developer.

#### <a name="standard-contextual-tabs"></a>Schede contestuali standard

- **Formato.** Contiene i comandi correlati alla modifica del formato del tipo di oggetto selezionato. In genere si applica alla parte di un oggetto.
- **Design.** Contiene i comandi, spesso nelle raccolte, per applicare gli stili al tipo di oggetto selezionato. In genere si applica all'intero oggetto.
- **Layout.** Contiene i comandi per modificare la struttura di un oggetto complesso, ad esempio una tabella o un grafico.

Se si dispone di comandi contestuali correlati a formato, progettazione e layout, ma non sufficienti per più schede, è sufficiente specificare una scheda formato.

### <a name="standard-groups"></a>Gruppi standard

- **Quando si pratica, usare i gruppi standard.** La visualizzazione di comandi comuni con gli stessi nomi e posizioni simili migliora notevolmente l'individuabilità. Vedere i [gruppi della barra multifunzione standard](#standard-ribbon-groups) più avanti in questo articolo.
- **Aggiungere un nuovo gruppo** se:
  - **I comandi sono strettamente correlati e possono essere descritti accuratamente dall'etichetta del gruppo.** L'aggiunta del gruppo dovrebbe facilitare l'individuazione dei comandi, non più difficili.
  - **I relativi comandi hanno una relazione più debole con i comandi in altri gruppi.** Sebbene tutti i comandi di una scheda siano strettamente correlati, alcune relazioni tra i comandi sono più complesse di altre.
  - **Il gruppo dispone di comandi sufficienti per giustificare la presenza di una posizione aggiuntiva.** Scopo per i comandi 3-5 per la maggior parte dei gruppi. Evitare di avere gruppi con soli comandi 1-2, sebbene sia accettabile disporre di una raccolta nella barra multifunzione senza altri comandi all'interno di un gruppo. La presenza di molti gruppi con un unico comando suggerisce una struttura eccessiva o la mancanza di coesione dei comandi.
- **Non organizzare eccessivamente** aggiungendo gruppi in cui non sono necessari.
- **Provare a suddividere un gruppo** se:
  - ![screenshot del gruppo di comandi disorganizzato ](images/cmd-ribbons-image35.png)<br/>Il gruppo presenta molti comandi di dimensioni diverse e necessita di un'organizzazione.
  - ![Screenshot di due nomi di gruppi di paragrafi lunghi ](images/cmd-ribbons-image33.png)<br>Il gruppo dispone di comandi che traggono un notevole vantaggio dalla presenza di etichette aggiuntive.
- **Inserire i gruppi usati più di frequente nelle posizioni più importanti e verificare che sia presente un ordine logico per i gruppi nella scheda.**
- **Ottimizzare la progettazione del gruppo in modo che gli utenti trovino i comandi in modo rapido e sicuro.** Tutte le altre considerazioni sono secondarie.
- **Non ridimensionare i gruppi contenenti un singolo pulsante in un'icona di gruppo popup.** Quando si esegue il ridimensionamento, lasciarli come singolo pulsante.
- **Usare un massimo di sette gruppi.** Se sono presenti più di sette gruppi, diventa più difficile determinare quale gruppo dispone di un comando.

### <a name="standard-ribbon-groups"></a>Gruppi della barra multifunzione standard

Quando è possibile, eseguire il mapping dei comandi del programma a questi gruppi standard, che vengono forniti all'interno delle schede associate nell'ordine di visualizzazione standard.

#### <a name="main-tab"></a>Scheda principale

- Appunti
- Carattere
- Paragraph
- In fase di modifica

#### <a name="insert-tab"></a>Scheda Inserisci

- Tabelle
- Illustrazioni

#### <a name="page-layout-tab"></a>Scheda layout pagina

- Temi
- Impostazioni di pagina
- Disponi

#### <a name="review-tab"></a>Scheda Verifica

- Controllo ortografico
- Commenti

#### <a name="view-tab"></a>Scheda Visualizza

- Visualizzazioni documento
- Mostra/Nascondi
- Zoom
- Finestra

### <a name="commands"></a>Comandi

- ![screenshot del comando per i numeri di riga sulla barra multifunzione ](images/cmd-ribbons-image36.png)<br/>**Sfrutta i vantaggi dell'individuabilità e della scalabilità delle barre multifunzione esponendo tutti i comandi di uso comune.** Quando appropriato, spostare i comandi usati di frequente dalle finestre di dialogo alla barra multifunzione, in particolare quelli che risultano difficili da trovare. Idealmente, gli utenti devono essere in grado di eseguire attività comuni senza utilizzare finestre di dialogo.

- **Non usare la scalabilità delle barre multifunzione per giustificare l'aggiunta di complessità superflua.** Continuare a esercitare il vincolo non aggiungere comandi a una barra multifunzione solo perché è possibile. L'esperienza di comando complessiva è semplice. Di seguito sono riportati alcuni modi per semplificare la presentazione:
  - ![screenshot della barra degli strumenti mini e del menu di scelta rapida ](images/cmd-ribbons-image37.png)</br>**Usare i menu di scelta rapida e le mini barre degli strumenti per i comandi sul posto e contestuali.**
  - **Spostare o continuare a utilizzare i comandi utilizzati raramente nelle finestre di dialogo.** Usare i lanci della finestra di dialogo per accedere a questi comandi. È comunque possibile usare le finestre di dialogo con le barre multifunzione. È sufficiente provare a ridurre la necessità di utilizzarli durante le attività comuni.
  - **Elimina le funzionalità ridondanti e usate raramente.**

#### <a name="presentation"></a>Presentazione

- **Presentare ogni comando in una sola scheda. Evitare più percorsi per lo stesso comando, soprattutto se il comando richiede molti clic per richiamare.** Potrebbe sembrare una praticità trovare un comando tramite più percorsi. Tenere presente che, quando gli utenti trovano quello che cercano, si fermano alla ricerca. È troppo facile per gli utenti presumere che il primo percorso trovato sia l'unico percorso che rappresenta un problema grave se il percorso non è efficiente. **Eccezione:** Le schede contestuali possono duplicare alcuni comandi dalle schede Home e Inserisci se questa operazione impedisce la modifica delle schede per le attività contestuali comuni.
- **All'interno di un gruppo, inserire i comandi nell'ordine logico, assegnando la preferenza ai comandi usati più di frequente.** Nel complesso, i comandi devono avere un flusso logico per facilitarne l'individuazione, mentre i comandi usati più di frequente vengono visualizzati per primi. In genere, i comandi con icone pixel 32x32 vengono visualizzati prima dei comandi con icone 16x16 pixel per facilitare l'analisi tra i gruppi.
- **Evitare di inserire comandi distruttivi accanto ai comandi usati di frequente.** Un comando è considerato distruttivo se l'effetto è diffuso e non può essere facilmente annullato o l'effetto non è immediatamente percettibile.
- **Usare i separatori per indicare comandi fortemente correlati, ad esempio un set di opzioni che si escludono a vicenda.**
- ![screenshot dei gruppi di tipi di carattere e di paragrafo ](images/cmd-ribbons-image3.png)<br/> **Si consiglia di utilizzare gruppi di tipo barra degli strumenti per set di comandi noti e fortemente correlati che non necessitano di etichette.** In questo modo è possibile presentare molti comandi in uno spazio compatto senza influire sull'individuabilità e la facilità di apprendimento. Per essere così ben noti, questi comandi vengono spesso utilizzati, immediatamente riconosciuti e pertanto tendono a essere nella scheda Home.

- **Usare le icone pixel 32x32 per i comandi usati più di frequente e con etichetta importante.** Quando si ridimensiona un gruppo, fare in modo che questi comandi vengano convertiti in icone pixel 16x16.
- **Evitare la posizione arbitraria del comando.** Valutare con attenzione la struttura della scheda e del gruppo per assicurarsi che gli utenti non perdano tempo a controllare ogni scheda per trovare il comando desiderato.
- **Evitare la selezione host basata sul marketing.** Gli obiettivi di marketing per la promozione delle nuove funzionalità tendono a cambiare nel tempo. Si prendano in considerazione le versioni future del prodotto e la frustrazione di un'organizzazione in costante evoluzione.

#### <a name="interaction"></a>Interazione

- **Disabilitare i comandi che non si applicano al contesto corrente o che restituiscono direttamente un errore.** Se utile, usare la [Descrizione comando avanzata](glossary.md) per spiegare il motivo per cui il comando è disabilitato. Non nascondere tali comandi perché questa operazione può causare la modifica del layout della barra multifunzione, rendendo instabile la presentazione della barra multifunzione.
- **Non aggiornare le etichette del comando in modo dinamico.** Anche in questo caso, questa operazione potrebbe causare la modifica del layout di tabulazione, ottenendo un aspetto instabile. Al contrario, progettare i comandi in modo che funzionino con le etichette costanti.

    | Risposta esatta.                                                                                       | Non corretto                                                                 |
    |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | ![screenshot della nota di inserimento e della nota di eliminazione ](images/cmd-ribbons-image38.png)<br/> Disabilitare i comandi quando non sono disponibili | ![screenshot della nota di inserimento, nessuna nota di eliminazione ](images/cmd-ribbons-image39.png)<br/>Non nascondere i comandi, anche quando non sono disponibili |

- **Preferisci controlli diretti.** Un comando è diretto se richiamato con un solo clic, ovvero senza spostarsi tra i menu. Tuttavia, fatta eccezione per le raccolte nella barra multifunzione, i controlli diretti non supportano l'anteprima in tempo reale, quindi la necessità di un'anteprima in tempo reale è anche un fattore.
- **Usare l'anteprima in tempo reale** per indicare l'effetto delle opzioni quando un comando è incluso in un set correlato di opzioni di formattazione e l'anteprima in tempo reale è importante e pratica, soprattutto se è probabile che gli utenti scelgano l'opzione sbagliata.
  - Se il comando viene usato di frequente, usare una raccolta della barra multifunzione per la direzione.
  - Se il comando viene utilizzato raramente, utilizzare una raccolta a discesa.
- **Esporre i comandi diretti** usando i controlli seguenti nell'ordine di preferenza seguente
  - **Pulsanti di comando, caselle di controllo, pulsanti di opzione e raccolte sul posto.** Questi sono sempre diretti.
  - **Pulsanti di divisione.** Direct per il comando più comune, ma indiretto per le variazioni del comando.
  - **Pulsanti di menu.** Questi sono indiretti, ma presentano molti comandi facili da trovare.
  - **Caselle di testo (con controlli di selezione).** L'input di testo richiede in genere più sforzi rispetto agli altri tipi di controllo.
- ![screenshot della barra multifunzione con solo pulsanti di menu ](images/cmd-ribbons-image42.png)</br>Se la barra multifunzione è costituita principalmente da pulsanti di menu visualizzati a schermo intero, è possibile usare una barra dei menu.
- **Preferisci comandi immediati.** ![cattura di schermata del pulsante Dividi stampa e del relativo sottomenu ](images/cmd-ribbons-image43.png)<br/>Un comando è immediato se viene applicato immediatamente (ovvero senza finestre di dialogo per raccogliere input aggiuntivi). Se un comando può richiedere l'input, provare a usare un pulsante di menu combinato con il comando immediato nella parte del pulsante e i comandi che richiedono l'input nel sottomenu.

### <a name="galleries"></a>Raccolte

**Usare una [raccolta](glossary.md)** se:

- **È disponibile un set di opzioni ben definito e correlato, da cui gli utenti scelgono in genere.** Potrebbe essere presente un numero illimitato di varianti, ma le selezioni probabili dovrebbero essere contenute correttamente. Se le scelte non sono strettamente correlate, è consigliabile usare raccolte separate.
- **Le scelte vengono espresse in modo ottimale visivamente, ad esempio le funzionalità di formattazione.** L'uso delle anteprime rende più semplice sfogliare, comprendere e scegliere. Mentre le scelte possono essere etichettate, la selezione viene effettuata in modo visivo e le etichette di testo non devono essere necessarie per comprendere le scelte.
- **Le scelte indicano il risultato ottenuto immediatamente con un solo clic.** Non dovrebbe essere presente alcuna finestra di dialogo di completamento per chiarire ulteriormente l'intenzione dell'utente o una serie di passaggi per ottenere il risultato indicato. Se gli utenti desiderano modificare la scelta, è possibile farlo in seguito.

**Usare una raccolta della barra multifunzione** se:

- **Le scelte vengono usate di frequente.** Le scelte richiedono lo spazio e valgono lo spazio potenzialmente tratto da altri comandi.
- **Per un utilizzo tipico, non è necessario raggruppare o filtrare le scelte presentate.**
- **Le scelte possono essere visualizzate in modo efficace entro l'altezza di una barra multifunzione, ovvero 48 pixel.**

#### <a name="thumbnails-in-galleries"></a>Anteprime nelle raccolte

**Scegliere le dimensioni più piccole dell'anteprima della raccolta standard** che esegue correttamente il processo.

- Per le raccolte nella barra multifunzione, usare le anteprime di 16x16, 48x48 o 64x48 pixel.
- Per le raccolte a discesa, usare anteprime di 16x16, 32x32, 48x48, 64x48, 72x96, 96X72, 96x96 o 128x128 pixel.
- Tutti gli elementi della raccolta devono avere le stesse dimensioni di anteprima.

Per le raccolte nella barra multifunzione:

- **Visualizza almeno tre opzioni: Altre informazioni se c'è spazio.** Se lo spazio disponibile non è sufficiente per visualizzare almeno tre scelte nelle dimensioni tipiche della finestra, utilizzare invece una raccolta a discesa.
- **Espandere gallerie nella barra multifunzione per sfruttare i vantaggi dello spazio disponibile.** Utilizzare lo spazio aggiuntivo per visualizzare più elementi e semplificarne la scelta con un solo clic.

Per le raccolte a discesa:

- **Visualizza la raccolta da una casella combinata, un elenco a discesa, un pulsante di menu combinato o un pulsante di menu.**
- **Se l'utente fa clic sulla finestra principale per chiudere la raccolta a discesa, è sufficiente chiudere la raccolta senza selezionare o modificare il contenuto della finestra principale.**
- **Se una raccolta ha molte scelte e alcune scelte vengono usate raramente, semplificare la raccolta predefinita concentrandosi sulle scelte comunemente usate.** Per i comandi rimanenti, fornire un comando appropriato nella parte inferiore dell'elenco a discesa raccolta.
  - Se il comando Mostra un elenco di più varianti, denominarlo "more `singular feature name` options..."
  - Se il comando Visualizza una finestra di dialogo che consente agli utenti di creare le proprie opzioni personalizzate, denominarla "Custom `feature name` ..."
- **Organizzare le scelte in gruppi, in modo da rendere più efficiente l'esplorazione.**
- ![screenshot della raccolta di simboli e dei filtri ](images/cmd-ribbons-image44.png)<br/>**Se una raccolta include molti elementi, è consigliabile aggiungere un filtro per consentire agli utenti di trovare le scelte in modo più efficiente.** Per evitare confusione, visualizzare inizialmente la raccolta non filtrata. Tuttavia, la maggior parte delle raccolte non necessita di un filtro perché non dovrebbero avere così tante scelte e l'uso di gruppi dovrebbe essere sufficiente.

### <a name="command-previews"></a>Anteprime comandi

- **Usare anteprime per mostrare l'effetto di un comando senza che gli utenti debbano eseguirlo per primo.** Grazie alle anteprime utili, è possibile migliorare l'efficienza e la facilità di apprendimento del programma e ridurre la necessità di tentativi ed errori. Per i diversi tipi di anteprime dei comandi, vedere [anteprime](#previews) nella sezione concetti di progettazione di questo articolo.
- **Per le anteprime in tempo reale, assicurarsi che l'anteprima possa essere applicata e che lo stato corrente venga ripristinato entro 500 millisecondi.** In questo modo è necessario avere la possibilità di applicare le modifiche di formattazione rapidamente e in modo interrompibili. Gli utenti devono essere in grado di valutare le diverse opzioni rapidamente per visualizzare le anteprime in tempo reale per ottenere il massimo vantaggio.
- **Evitare di usare il testo nelle anteprime.** In caso contrario, sarà necessario localizzare le immagini di anteprima.

### <a name="icons"></a>Icone

- ![screenshot dell'elenco a discesa e delle caselle di controllo ](images/cmd-ribbons-image45.png)<br/>**Fornire icone per tutti i controlli della barra multifunzione eccetto gli elenchi a discesa, le caselle di controllo e i pulsanti di opzione.** Per la maggior parte dei comandi sono necessarie entrambe le icone 32x32 e 16x16 pixel. solo le icone 16x16 pixel vengono usate dalla barra di accesso rapido. Le raccolte in genere usano icone 16x16, 48x48 o 64x48 pixel.
- **Fornire icone univoche.** Non usare la stessa icona per comandi diversi.
- **Assicurarsi che le icone della barra multifunzione siano chiaramente visibili rispetto al colore di sfondo della barra multifunzione.** Valutare sempre le icone della barra multifunzione nel contesto e in modalità a contrasto elevato.
- **Scegliere le progettazioni di icone che comunicano chiaramente l'effetto,** specialmente per i comandi usati più di frequente. I nastri ben progettati hanno icone autoesplicative per aiutare gli utenti a trovare e comprendere i comandi in modo efficiente.
- **Scegliere le icone riconoscibili e distinguibili,** specialmente per i comandi usati più di frequente. Assicurarsi che le icone abbiano forme e colori distinti. Questa operazione consente agli utenti di trovare rapidamente i comandi, anche se non ricordano il simbolo dell'icona.

    | Risposta esatta.                                                                                                 | Non corretto                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![screenshot del contagocce blu e della matita gialla ](images/cmd-ribbons-image46.png)<br/>Utilizzare la forma e il colore per creare icone facili da distinguere. | ![screenshot del contagocce blu e della matita blu ](images/cmd-ribbons-image47.png)<br/> Le icone con lo stesso colore sono difficili da distinguere|

- ![screenshot del comando commenti nel contenitore popup ](images/cmd-ribbons-image48.png)<br/>**Prendere in considerazione la creazione di icone di gruppo popup posizionando l'icona 16x16 pixel del comando più evidente nel gruppo all'interno di un contenitore visuale 32x32 pixel.** Non è necessario creare icone diverse per i gruppi popup.
- ![screenshot dei pulsanti di comando per la formattazione del testo ](images/cmd-ribbons-image25.png)<br/>**Se utile, modificare l'icona per riflettere lo stato corrente.** Questa operazione è particolarmente utile per i pulsanti di suddivisione il cui effetto predefinito può cambiare.
- **Assicurarsi che le icone della barra multifunzione siano conformi alle linee guida dell'icona di tipo Aero.** Tuttavia, le icone della barra multifunzione vengono visualizzate direttamente anziché essere visualizzate nella prospettiva.

| Risposta esatta.                                                                                                 | Non corretto                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![screenshot delle icone del comando bidimensionale ](images/cmd-ribbons-image49.png)<br/> Usare icone bidimensionali.|![screenshot delle icone dei comandi tridimensionali ](images/cmd-ribbons-image50.png)<br/> Non usare icone tridimensionali. |
 
### <a name="enhanced-tooltips"></a>Descrizioni comando migliorate

- **Tutti i comandi della barra multifunzione devono avere descrizioni comandi avanzate** per assegnare il nome del comando, il tasto di scelta rapida, la descrizione e informazioni aggiuntive facoltative. Evitare le descrizioni comandi che ripubblicano semplicemente l'etichetta.

    **Non corretto:**

    ![screenshot della descrizione comando che ripete il nome del comando ](images/cmd-ribbons-image51.png)

    In questo esempio la descrizione comando riporta semplicemente l'etichetta del comando.

- **Quando si è pratici, descrivere completamente il comando utilizzando una descrizione concisa.** Collegamento alla guida solo se è effettivamente necessaria una spiegazione più approfondita.

    **Non corretto:**

    ![screenshot della descrizione comando per il comando barrato ](images/cmd-ribbons-image52.png)

    In questo esempio, il comando non necessita di aiuto.

- **Se utile, illustra l'effetto del comando usando un'anteprima.**

    ![screenshot della descrizione comando e del grafico per l'inserimento del grafico ](images/cmd-ribbons-image53.png)

    In questo esempio l'immagine della descrizione comando illustra l'effetto del comando.

Per le linee guida per l'assegnazione di etichette, vedere [Enhanced ToolTip labels](#enhanced-tooltips).

### <a name="access-keys-and-keytips"></a>Chiavi di accesso e suggerimenti

I suggerimenti tasto di ricerca sono il meccanismo usato per visualizzare le chiavi di accesso per i comandi visualizzati direttamente su una barra multifunzione.

Le chiavi di accesso per i comandi del menu a discesa sono indicate da un carattere sottolineato. Si differenziano dalle chiavi di accesso ai menu nei modi seguenti:

- È possibile usare due chiavi di accesso ai caratteri. Ad esempio, è possibile utilizzare FP per accedere al comando Format Painter.
- Le assegnazioni delle chiavi di accesso vengono visualizzate usando suggerimenti anziché sottolineature, quindi la larghezza e i derivati dei caratteri non rappresentano un fattore per la creazione di assegnazioni.

- **Assegnare chiavi di accesso a tutte le schede e i comandi della barra multifunzione.** L'unica eccezione possibile è per i comandi provenienti dai componenti aggiuntivi legacy.
- **Per il pulsante dell'applicazione e la barra di accesso rapido:**
  - Assegnare F al pulsante dell'applicazione. Questa assegnazione viene utilizzata a causa della somiglianza del pulsante dell'applicazione con il menu file tradizionale.
  - ![screenshot dei suggerimenti per i tasti di comando su una barra multifunzione ](images/cmd-ribbons-image54.png)<br/>Per la barra di accesso rapido e gli elenchi dei file usati di recente, assegnare numericamente le chiavi di accesso.
- ![screenshot che mostra i suggerimenti per le schede ](images/cmd-ribbons-image55.png)<br/>**Per le schede:**
  - Assegnare H a Home.
  - A partire dalle schede utilizzate più di frequente, assegnare la prima lettera dell'etichetta.
  - Per tutte le schede che non possono essere assegnate alla prima lettera, scegliere una consonante distinta o una vocale nell'etichetta.
  - Per i programmi utilizzati per supportare le barre dei menu, è opportuno mantenere la compatibilità con le chiavi di accesso per ottenere la massima praticità. Evitare di assegnare significati diversi alle chiavi di accesso dalle categorie di menu legacy. Se, ad esempio, la versione della barra dei menu legacy di un programma dispone di un menu modifica, tenta di utilizzare una chiave di accesso E per la scheda equivalente. Se non è presente una scheda equivalente, non assegnare una chiave di accesso E a qualsiasi scheda per evitare confusione.
- ![screenshot che mostra i suggerimenti per una barra multifunzione ](images/cmd-ribbons-image56.png)<br/>**Per i comandi della barra multifunzione, i menu e i sottomenu:**
  - Assegnare combinazioni di chiavi di accesso univoche all'interno di una scheda. È possibile riutilizzare le combinazioni di tasti di accesso all'interno di schede diverse.
  - Laddove possibile, assegnare le chiavi di accesso standard per i comandi di uso comune. Vedere la [tabella delle chiavi di accesso standard](inter-keyboard.md).
  - Per altri comandi:
    - Per i comandi usati più di frequente, scegliere lettere all'inizio della prima o della seconda parola dell'etichetta, preferibilmente la prima lettera.
    - Per i comandi utilizzati meno di frequente, scegliere lettere che rappresentano una consonante distinta o una vocale nell'etichetta, ad esempio "x" in "Exit".
    - Per i comandi e i lanci della finestra di dialogo utilizzati meno di frequente, è necessario utilizzare due lettere.
    - Per i menu e i sottomenu, utilizzare una singola lettera per ridurre il numero di sequenze di tasti necessarie per il comando completo.
    - Non usare chiavi di accesso che iniziano con J, Y o Z perché vengono usate per schede contestuali, suggerimenti per chiavi non assegnate e gruppi popup.
- ![screenshot dei suggerimenti tasti per i gruppi popup ](images/cmd-ribbons-image58.png)<br/>**Per i gruppi popup:**
  - Usare una chiave di accesso di due lettere che inizia con Z.
  - A partire dai gruppi usati più di frequente, assegnare la seconda lettera chiave di accesso alla prima lettera dell'etichetta.
  - Per tutti i gruppi rimanenti, scegliere una consonante distinta o una vocale nell'etichetta.

Per le linee guida sui tasti di scelta rapida, vedere [tastiera](inter-keyboard.md).

### <a name="application-buttons"></a>Pulsanti applicazione

- **Utilizzare un pulsante dell'applicazione per presentare un menu di comandi che comportano l'operazione in o con un file.** Gli esempi includono i comandi che tradizionalmente passano al menu file per creare, aprire e salvare file, stampare e inviare e pubblicare documenti.
- **Fornire sempre un pulsante applicazione quando si usa una barra multifunzione.** Se il programma non utilizza i file, utilizzare il pulsante applicazione per accedere alle opzioni di programma e al comando Esci. I pulsanti dell'applicazione visualizzano sempre un menu di comando che non sono mai semplicemente decorativi.
- **Usare i seguenti comandi del menu applicazione standard quando appropriato:**
  - Nuova  
  - Apri  
  - Salva  
  - Salva con nome...
  - Stampa...
  - Stampa veloce  
  - Anteprima di stampa  
  - Chiudi  
  - Opzioni  
  - Esci  
  
- **Riservare i comandi che appartengono al menu applicazione solo per tale menu.** Non inserirli in modo ridondante in una delle schede.
- Per ogni voce di menu specificare:
  - **Etichetta con il nome del comando.**
  - **Icona A 32x32 pixel.**
  - **Una breve descrizione.** Assicurarsi che la descrizione possa essere visualizzata utilizzando al massimo due righe di testo.
- ![screenshot della descrizione comando che documenta il tasto di scelta rapida ](images/cmd-ribbons-image59.png)<br/>**Utilizzare le descrizioni comandi per documentare i tasti di scelta rapida.** A differenza dei menu normali, i menu applicazione non documentano i tasti di scelta rapida usando le etichette.

### <a name="quick-access-toolbars"></a>Barre di accesso rapido

- **Utilizzare la barra di accesso rapido per fornire l'accesso ai comandi utilizzati di frequente.** I comandi possono essere dal pulsante dell'applicazione o dalla barra multifunzione.
- **Fornire sempre una barra di accesso rapido quando si usa una barra multifunzione.** Eseguire questa operazione anche se la barra multifunzione dispone di una sola scheda; Questo garantisce la coerenza tra i programmi.
- **Prepopolare la barra di accesso rapido con i comandi usati di frequente nel menu dell'applicazione.** Specificare Salva e Annulla se il programma li supporta e aprire e stampare se supportati e usati di frequente.
- **Per il menu di personalizzazione della barra di accesso rapido, fornire fino a 12 dei comandi immediati usati più di frequente.** I comandi immediati non richiedono input aggiuntivo prima che divengano effettivi e pertanto sono particolarmente adatti per la barra di accesso rapido. Sebbene possano essere presenti comandi immediati, preferire i comandi che non si trovano nella scheda Home, perché gli utenti hanno più probabilità di sceglierli.
- **Per personalizzare il menu della barra di accesso rapido, se è presente una coppia di comandi correlati, fornire entrambi gli elementi, indipendentemente dalla frequenza.** Le coppie comuni sono apertura/chiusura, indietro/in poi e annullamento/ripetizione.
- **Per la finestra di dialogo Personalizza barra di accesso rapido, fornire un modo per aggiungere qualsiasi comando.** Fornire un filtro dei comandi più diffusi che Visualizza i comandi usati più di frequente e selezionare questo filtro per impostazione predefinita.

### <a name="dialog-box-launchers"></a>Avviatori della finestra di dialogo

- ![screenshot della finestra di dialogo tipo di carattere e del gruppo di tipi di carattere ](images/cmd-ribbons-image60.png)<br/>**Consente di specificare un gruppo con un pulsante di avvio della finestra di dialogo se è presente una finestra di dialogo correlata con comandi e impostazioni usati raramente.** La finestra di dialogo deve contenere tutti i comandi del gruppo, oltre ad altri non un set di comandi completamente diverso o gli stessi comandi del gruppo.
- **Non usare un pulsante di avvio della finestra di dialogo per eseguire direttamente i comandi.** Un pulsante di avvio della finestra di dialogo deve visualizzare una finestra di dialogo.
- **Non usare un utilità di avvio della finestra di dialogo per accedere ai comandi e alle impostazioni usati di frequente.** Rispetto ai comandi direttamente sulla barra multifunzione, i comandi e le impostazioni della finestra di dialogo sono relativamente non individuabili.
- **Corrisponde al nome della finestra di dialogo con il nome del gruppo.** Non è necessario che sia una corrispondenza esatta, ma i nomi devono essere abbastanza simili in modo che gli utenti non sorprendano i risultati.

    **Non corretto:**

    ![screenshot della finestra di dialogo audio promemoria ](images/cmd-ribbons-image61.png)

    Mentre un promemoria è un'opzione di promemoria, l'uso dell'utilità di avvio della finestra di dialogo per impostare il suono del promemoria è imprevisto.

- **Consente di visualizzare solo i comandi e le impostazioni correlati al gruppo.** Se nella finestra di dialogo sono visualizzati altri elementi, gli utenti possono concludere che questo percorso di questi altri comandi e impostazioni è l'unico percorso.

    **Non corretto:**

    ![screenshot della finestra di dialogo tipo di carattere ](images/cmd-ribbons-image62.png)

    In questo esempio, nella finestra di dialogo tipo di carattere vengono visualizzate le impostazioni relative alla spaziatura dei caratteri, che non sono correlate alla scheda associata.

## <a name="labels&quot;></a>Etichette

### <a name=&quot;tab-labels&quot;></a>Etichette di tabulazione

- **Etichetta tutte le schede.**
- Quando possibile, **usare le schede standard della barra multifunzione**.
- **Preferisci etichette concise e singole parole.** Anche se le etichette a più parole sono accettabili, hanno più spazio e sono più difficili da localizzare.
- **Scegliere nomi di schede significativi che ne descrivano chiaramente e accuratamente il contenuto.** I nomi devono essere specifici, ma non troppo specifici. I nomi delle schede devono essere sufficientemente prevedibili, in modo che gli utenti non sorprendano il contenuto. Si noti che la scheda Home è denominata in modo generico perché viene usata per i comandi usati più di frequente.
- **Non** usare nomi di gruppo, ad esempio &quot;Basic&quot; e &quot;Advanced&quot;. Richiedono agli utenti di determinare se il comando cercato è di base o avanzato.
- **Scegliere i nomi delle schede che riflettono lo scopo.** Prendere in considerazione gli obiettivi o le attività associati alla scheda.
- **Scegliere nomi di schede chiaramente distinti rispetto a tutti gli altri nomi di schede.**
- **Usare i sostantivi o i verbi per le schede.** I nomi di tabulazione non richiedono il formulazione parallela, quindi scegliere l'etichetta migliore indipendentemente dal fatto che si tratti di un sostantivo o un verbo.
- **Non usare gerundi** (nomi che terminano con &quot;-ing"). Usare invece il verbo da cui viene derivato gerundio. (ad esempio, usare "Draw" invece di "Drawing").
- **Evitare i nomi di tabulazione con le stesse lettere iniziali, soprattutto le schede adiacenti.** Quando la barra multifunzione viene ridotta, i nomi delle schede avranno lo stesso testo troncato.
- **Preferisci nomi singolari.** Tuttavia, è possibile usare un nome pura se il nome singolare è imbarazzante.
- **Usare l'uso di maiuscole in stile titolo.**
- **Non usare punteggiatura finale.**

### <a name="contextual-tab-and-tab-set-labels"></a>Scheda contestuale e etichette del set di schede

- **Termina le etichette del set di schede contestuali con "Tools".** Questa operazione consente di identificare lo scopo delle schede contestuali.
- Usare l'uso di maiuscole in stile titolo.
- Non usare punteggiatura finale.

### <a name="group-labels"></a>Etichette di gruppo

- **Etichettare tutti i gruppi** , a meno che il gruppo non disponga di un solo comando e le etichette del gruppo e del comando siano le stesse.

- **Utilizzare la barra multifunzione standard groupsWhenever.**
- **Preferisci etichette concise e singole parole.** Anche se le etichette a più parole sono accettabili, hanno più spazio e sono più difficili da localizzare.
- **Scegliere nomi di gruppo significativi che ne descrivano chiaramente e accuratamente il contenuto.** I nomi devono essere specifici, non generici.
- **Scegliere i nomi dei gruppi che riflettono lo scopo.** Prendere in considerazione gli obiettivi o le attività associati ai comandi del gruppo.
- **Evitare di usare gerundi** (nomi che terminano con "-ing"). È possibile usare gerundi, tuttavia, se l'uso del verbo da cui deriva il gerundio potrebbe creare confusione. Ad esempio, usare "modifica" e "proofing" anziché "Edit" e "Proof".
- **Non usare nomi di gruppo identici ai nomi di tabulazione.** Se si usa il nome della scheda in cui si trova il gruppo, non sono disponibili informazioni e l'uso del nome di una scheda diversa è confuso.
- **Preferisci nomi singolari.** Tuttavia, è possibile usare un nome pura se il nome singolare è imbarazzante. 
- **Usare le maiuscole/minuscole come nelle frasi comuni.**
- **Non usare punteggiatura finale.**

### <a name="command-labels"></a>Etichette comando

- **Etichettare tutti i comandi.** La presenza di etichette di testo esplicite consente agli utenti di trovare e comprendere i comandi. **Eccezione:** È possibile senza etichettare un comando se la relativa icona è molto nota e lo spazio è a un livello Premium. Probabilmente, i comandi senza etichetta si troveranno nella scheda Home. In questo caso, assegnare la proprietà Name a un'etichetta di testo appropriata. Questo consente ai prodotti di Assistive Technology, ad esempio utilità per la lettura dello schermo, di fornire agli utenti informazioni alternative sul grafico.
- **Per i pulsanti di comando, usare un'etichetta concisa e intuitiva.** Se possibile, usare una sola parola; massimo quattro parole.
- **Per gli elenchi a discesa, se l'elenco contiene sempre un valore, usare il valore corrente come etichetta.**
- ![cattura di schermata del prompt della Rubrica di ricerca ](images/cmd-ribbons-image67.png)<br/>Se un [elenco a discesa modificabile](/windows/desktop/uxguide/ctrl-drop) non ha un valore, usare una [richiesta](glossary.md).
- **Gli elenchi a discesa che non sono di chiara interpretazione o usati raramente necessitano di un'etichetta esplicita.** Inserire i due punti alla fine dell'etichetta.
- ![Screenshot automatico dopo: \[ secondi \] ](images/cmd-ribbons-image69.png)<br. >per le **caselle di testo, usare un'etichetta esplicita.** Inserire i due punti alla fine dell'etichetta.
- **Usare le maiuscole/minuscole come nelle frasi comuni.** Questa operazione è più appropriata per il [tono](text-style-tone.md)di Windows.
- **Avviare l'etichetta con un verbo imperativo.** a meno che non corrisponda al nome della scheda o del gruppo o di un verbo comune come show, create, INSERT o format.
- **Non usare punteggiatura finale.**
- **Per conservare spazio, non inserire ellissi sulle etichette del comando della barra multifunzione.** Tuttavia, i puntini di sospensione vengono usati dai comandi nel pulsante dell'applicazione e nei menu a discesa.

### <a name="enhanced-tooltip-labels"></a>Etichette descrizioni comando avanzate

- **Usare il titolo per assegnare il nome del comando e il relativo tasto di scelta rapida, se applicabile.**
- **Per il titolo, non usare la punteggiatura finale.**
- **Inizia la descrizione con un verbo.** Usare la descrizione per aiutare gli utenti a determinare se una funzionalità specifica è quella che sta cercando. La descrizione deve essere formulata per completare la frase "Questa è la funzione corretta da usare se si vuole...".
- **Mantieni la descrizione breve.** Vai direttamente al punto. Il testo lungo sconsiglia la lettura.
-   ![cattura di schermata del pulsante di suddivisione incolla e di due descrizioni comandi ](images/cmd-ribbons-image70.png)<br/>**Per i pulsanti di menu combinato, utilizzare una descrizione comando diversa per spiegare il menu di menu combinato.**
- **Usare una descrizione supplementare facoltativa per spiegare come usare il controllo.** Questo testo può includere informazioni sullo stato del controllo (incluso il motivo per cui è disabilitato) se il controllo stesso non indica lo stato. Lasciare questo testo breve e utilizzare un argomento della Guida per ottenere spiegazioni più dettagliate.
- ![screenshot della descrizione comando con grafica e testo ](images/cmd-ribbons-image71.png)**per la descrizione e la descrizione supplementare, utilizzare frasi complete con la punteggiatura finale.**
- Usare le maiuscole/minuscole come nelle frasi comuni.

### <a name="application-button-labels"></a>Etichette del pulsante dell'applicazione

- [cattura di schermata dell'opzione di stampa rapida selezionata ](images/cmd-ribbons-image72.png)<br/>**Usare "Quick" per indicare una versione immediata di un comando.**

- **Utilizzare i puntini di sospensione per indicare che un comando richiede ulteriori informazioni.**
- **Usare le maiuscole/minuscole come nelle frasi comuni.**

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle barre multifunzione:

- Fare riferimento alla barra multifunzione e ai relativi componenti come barra multifunzione, tabulazioni, gruppi e controlli. Questi termini non sono in maiuscolo.
- Fare riferimento al pulsante Arrotonda come pulsante dell'applicazione e il menu che contiene come menu dell'applicazione.
- Fare riferimento alla barra degli strumenti come barra di accesso rapido.
- Vedere le schede per le etichette e la scheda Word. Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola.
- Fare riferimento ai comandi in base alle etichette. Per i nomi delle descrizioni comandi, fare riferimento ai comandi senza etichetta. Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere i puntini di sospensione. Non includere il pulsante o il comando di Word.
- Per descrivere l'interazione dell'utente, utilizzare fare clic per le schede e i controlli. Utilizzare invio per gli elenchi a discesa modificabili. Non usare choose, SELECT o pick.
- Vedere gli elementi non disponibili come non disponibili, non come grigio, disabilitato o inattivo. Nella documentazione di programmazione utilizzare disabilitato.
- Quando possibile, formattare le etichette usando il testo in grassetto. In caso contrario, inserire le etichette tra virgolette solo se necessario per evitare confusione.

Esempi:

- Nella scheda **Home** fare clic su **Incolla speciale**.
- Nella casella **tipo di carattere** della scheda **Home** immettere "Segoe UI".
- Nella scheda **Revisione** fare clic su **Mostra markup**, quindi fare clic su **revisori**.
- Nella scheda **formato** , in **Strumenti immagine**, fare clic su **Comprimi immagini**.