---
title: Come progettare UX per applicazioni desktop
description: Una grande applicazione desktop è potente e, allo stesso tempo, semplice. Grazie alla selezione e alla presentazione delle funzionalità con particolare equilibrio, è possibile ottenere sia la potenza che la semplicità.
ms.assetid: 0039a3ee-95bc-457f-a1a8-6a036ce22fd2
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 74433514f61b37ba1c9941c8134767be5458ebc8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351066"
---
# <a name="how-to-design-a-great-user-experience-for-desktop-applications"></a>Come progettare un'esperienza utente ottimale per le applicazioni desktop

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Una grande applicazione desktop è potente e, allo stesso tempo, semplice. Grazie alla selezione e alla presentazione delle funzionalità con particolare equilibrio, è possibile ottenere sia la potenza che la semplicità.

**Potente**

![screenshot della finestra di dialogo ortografia e grammatica ](images/powerful-simple-image1.png)

**Potente e semplice:**

![screenshot dell'elenco di possibili revisioni ortografiche ](images/powerful-simple-image2.png)

L'applicazione ideale basata su Windows è potente e semplice. Naturalmente si desidera che l'applicazione sia potente e naturalmente si desidera che sia semplice, ma è possibile ottenere entrambi i risultati? Si verifica una tensione naturale tra questi obiettivi, ma la tensione è molto più inconciliabile. Puoi ottenere la potenza e la semplicità grazie alla selezione e alla presentazione di funzionalità con particolare equilibrio.

## <a name="what-makes-an-application-powerful"></a>Che cosa rende un'applicazione potente?

Che cosa significa "potenza" in termini di software? Un'applicazione potrebbe essere considerata potente se è piena di funzionalità, con una vasta gamma di funzionalità nel tentativo di essere tutti gli utenti. Una progettazione di questo tipo non ha probabilmente esito positivo perché un set di funzionalità senza destinazione è improbabile che soddisfi le esigenze di chiunque. Questo non è il tipo di potenza che si sta dopo.

Un'applicazione è potente quando presenta la combinazione corretta di queste caratteristiche:

-   **Consentendo.** L'applicazione soddisfa le esigenze degli utenti di destinazione, consentendo loro di eseguire attività che altrimenti non avrebbero potuto eseguire e raggiungere in modo efficiente gli obiettivi.
-   **Efficiente** L'applicazione consente agli utenti di eseguire attività con un livello di produttività e scalabilità che non era possibile prima.
-   **Versatile.** L'applicazione consente agli utenti di eseguire in modo efficace un'ampia gamma di attività in diverse circostanze.
-   **Diretto.** L'applicazione è in grado di aiutare gli utenti a raggiungere i propri obiettivi, anziché raggiungere il metodo o richiedere passaggi superflui. Funzionalità quali i collegamenti, l'accesso alla tastiera e le macro migliorano il senso di indirizzamento.
-   **Flessibile.** L'applicazione consente agli utenti di controllare il proprio lavoro in modo completo e accurato.
-   **Integrato.** L'applicazione è perfettamente integrata con Microsoft Windows, consentendo la condivisione di dati con altre applicazioni.
-   **Avanzata** L'applicazione presenta funzionalità eccezionali, innovative e all'avanguardia, che non sono disponibili nelle soluzioni in competizione.

Alcune di queste caratteristiche dipendono dalla percezione dell'utente e sono relative alle funzionalità correnti degli utenti. Gli elementi considerati potenti possono cambiare nel tempo, quindi la funzionalità di ricerca avanzata di oggi potrebbe essere un'operazione comune domani.

Tutte queste caratteristiche possono essere combinate nella definizione di Power:

**Un'applicazione è potente quando consente agli utenti di destinazione di realizzare in modo efficiente il loro pieno potenziale.**

Quindi, la misura finale della potenza è la produttività, non il numero di funzionalità.

Diversi utenti hanno bisogno di aiuto per ottenere il massimo potenziale in modi diversi. Ciò che consente ad alcuni utenti potrebbe danneggiare la versatilità, la direzione e il controllo per altri utenti. Il software ben progettato deve bilanciare queste caratteristiche in modo appropriato. Ad esempio, un sistema di pubblicazione desktop progettato per gli utenti non professionisti può utilizzare le procedure guidate per esaminare gli utenti attraverso attività complesse. Tali procedure guidate consentono agli utenti di destinazione di eseguire attività che altrimenti non sarebbero in grado di eseguire. Al contrario, un sistema di pubblicazione desktop per i professionisti può concentrarsi su indirizzamento, efficienza e controllo completo. Per gli utenti di tale applicazione, le procedure guidate potrebbero essere limitate e frustranti.

**Se si esegue una sola operazione...**

Comprendere gli obiettivi degli utenti di destinazione e creare un set di funzionalità che consenta loro di realizzare questi obiettivi in modo produttivo.

## <a name="what-makes-a-user-experience-simple"></a>Che cosa rende semplice l'esperienza utente?

Si definisce la semplicità come segue:

**La semplicità è la riduzione o l'eliminazione di un attributo di una progettazione che gli utenti di destinazione sono consapevoli e considerano non essenziali.**

In pratica, la semplicità viene eseguita selezionando il set di funzionalità corretto e presentando le funzionalità nel modo giusto. In questo modo si riduce il tempo necessario, sia reale che percepito.

La semplicità dipende dalla percezione degli utenti. Prendere in considerazione il modo in cui l'effetto di una trasmissione automatica dipende dal punto di vista di un utente:

-   Per il driver tipico (utente di destinazione), una trasmissione automatica Elimina la necessità di un cambio di ingranaggio manuale e di una frizione, rendendo un'auto molto più semplice da guidare. Un cambio e una frizione manuali non sono essenziali per l'attività di guida, quindi vengono rimossi per ottenere la semplicità.
-   Per un driver di Race Car professionale, il controllo diretto sulla trasmissione è essenziale per la competitività. Una trasmissione automatica influisce negativamente sulle prestazioni dell'auto, quindi non viene considerata come la semplicità.
-   Per un meccanico, una trasmissione automatica è un meccanismo più complesso e pertanto non è più facile da ripristinare o gestire rispetto a una trasmissione manuale. A differenza del meccanico, l'utente di destinazione non è a conoscenza di questa complessità interna.

Anche se diversi utenti considerano la trasmissione automatica in modo diverso, l'operazione ha esito positivo perché elimina la necessità di conoscenze, competenze e sforzi non essenziali da parte degli utenti di destinazione. Per il driver tipico, la trasmissione automatica è un'ottima funzionalità perché funziona semplicemente.

### <a name="simplicity-vs-ease-of-use"></a>Semplicità e semplicità d'uso

La semplicità, se applicata correttamente, comporta semplicità d'uso. Ma la semplicità e la facilità d'uso non sono gli stessi concetti. La facilità d'uso si verifica quando gli utenti possono eseguire correttamente un'attività autonomamente senza difficoltà o confusione entro un intervallo di tempo appropriato. Sono disponibili diversi modi per ottenere la semplicità d'uso e la semplicità, ovvero la riduzione del non essenziale, è solo uno di essi.

Tutti gli utenti, indipendentemente dalla sofisticazione, vogliono svolgere il proprio lavoro con una quantità minima di lavoro superfluo. Tutti gli utenti, anche quelli avanzati, sono principalmente motivati a svolgere il proprio lavoro, non per conoscere i computer o l'applicazione.

La semplicità è il modo più efficace per ottenere la semplicità d'uso e la facilità d'uso equivale a usare. Le funzionalità complesse e difficili da usare non vengono usate. Al contrario, i progetti semplici e eleganti che eseguono la loro funzione sono una gioia da usare. Richiamano una risposta positiva e emotiva.

Si consideri, ad esempio, il supporto delle reti wireless in Microsoft Windows XP. Microsoft potrebbe avere aggiunto una procedura guidata per esaminare gli utenti durante il processo di configurazione. Questo approccio avrebbe causato la semplicità d'uso, ma non la semplicità, perché sarebbe stata aggiunta una funzionalità non essenziale (procedura guidata). Microsoft ha progettato invece reti wireless per configurarsi automaticamente. Infine, gli utenti non sono interessati ai dettagli della configurazione, a condizione che funzionino in modo affidabile e sicuro. Questa combinazione di potenza e semplicità nella tecnologia di rete wireless ha comportato la popolarità e l'adozione rapida.

**Se si esegue una sola operazione...**

Avviare il processo di progettazione con le progettazioni più semplici che fanno bene il lavoro.

Se non si è soddisfatti della progettazione corrente, iniziare rimuovendo tutti gli elementi non essenziali. Si noterà che il resto è in genere piuttosto positivo.

## <a name="obtaining-simplicity-while-maintaining-power"></a>Ottenere semplicità mantenendo la potenza

### <a name="design-principles"></a>Principi di progettazione

Per ottenere la semplicità, progettare sempre per il probabile, non il possibile.

Il possibile

Decisioni di progettazione basate sulle possibili cause di interfacce utente complesse, ad esempio l'editor del registro di sistema, in cui la progettazione presuppone che tutte le azioni siano ugualmente possibili e, di conseguenza, richiedono un uguale sforzo. Poiché ciò è possibile, gli obiettivi utente non vengono considerati nelle decisioni di progettazione.

Il probabile

Decisioni di progettazione basate sul probabile lead a soluzioni semplificate, basate su obiettivi e attività, in cui gli scenari probabili ricevono lo stato attivo e richiedono un impegno minimo per l'esecuzione.

Principio di progettazione della semplicità

**Per ottenere semplicità, concentrarsi sulle probabilità ridurre, nascondere o rimuovere ciò che è improbabile; ed eliminano ciò che è impossibile.**

Ciò che gli utenti faranno è molto più rilevante per la progettazione rispetto a quello che potrebbero fare.

### <a name="design-techniques"></a>Tecniche di progettazione

Per ottenere semplicità mantenendo la potenza, scegliere il **set corretto di funzionalità**, individuare le funzionalità **nei punti giusti** e **ridurre il lavoro** necessario per usarle. In questa sezione vengono fornite alcune tecniche comuni per raggiungere questi obiettivi.

Scelta del set di funzionalità corretto

"Si raggiunge la perfezione, non quando non c'è altro da aggiungere.

Tuttavia, quando non c'è nulla da togliere ". -Antoine de Saint-Exupery

Le tecniche di progettazione seguenti forniscono agli utenti le funzionalità necessarie per ottenere la semplicità grazie alla riduzione effettiva o alla rimozione:

-   **Determinare le funzionalità necessarie agli utenti.** Informazioni sulle esigenze degli utenti tramite l'analisi di obiettivi, scenari e attività. Determinare un set di funzionalità che realizza questi obiettivi.
-   **Rimuovere gli elementi superflui.** Rimuovere gli elementi che non possono essere usati o che preferiscono alternative.
-   **Rimuovere la ridondanza superflua.** Per eseguire un'attività possono essere disponibili diversi modi efficaci. Per ottenere la semplicità, prendere la decisione più complessa e scegliere quella migliore per gli utenti di destinazione invece di fornirli tutti e scegliere un'opzione.
-   **Fare in modo che funzioni automaticamente.** L'elemento è necessario, ma qualsiasi interazione utente per ottenerne il funzionamento non è perché esiste un comportamento o una configurazione predefinita accettabile. Per ottenere la semplicità, è possibile farlo funzionare automaticamente e nasconderlo completamente dall'utente o ridurne significativamente l'esposizione.

Semplificazione della presentazione

"La possibilità di semplificare il metodo per eliminare il superfluo

in modo che il necessario possa pronunciare ". -Hans Hofmann

Usare le tecniche di progettazione seguenti per mantenere la potenza, ottenendo la semplicità grazie alla percezione della riduzione o della rimozione:

-   **Combinare gli elementi da combinare.** Inserire le funzionalità essenziali che supportano un'attività insieme in modo che un'attività possa essere eseguita in un'unica posizione. I passaggi dell'attività devono avere un flusso unificato e semplificato. Suddividere le attività complesse in un set di passaggi semplici e chiari, in modo che la posizione "One" sia costituita da diverse aree dell'interfaccia utente, ad esempio una procedura guidata.
-   **Separare gli elementi che devono essere separati.** Non tutti gli elementi possono essere presentati in un'unica posizione, quindi i limiti sono sempre chiari e ben scelti. Creare funzionalità che supportano gli scenari principali centrali e ovvie e nascondere le funzionalità facoltative o renderle periferiche. Separare le singole attività e fornire collegamenti alle attività correlate. Ad esempio, le attività correlate alla manipolazione delle foto dovrebbero essere chiaramente separate dalle attività correlate alla gestione di raccolte di foto, ma devono essere facilmente accessibili tra loro.
-   **Eliminare gli elementi che possono essere eliminati.** Eseguire una stampa della progettazione ed evidenziare gli elementi utilizzati per eseguire le attività più importanti. Anche evidenziare le singole parole nel testo dell'interfaccia utente che comunicano informazioni utili. A questo punto, esaminare gli elementi che non vengono evidenziati e provare a rimuoverli dalla progettazione. Se si rimuove l'elemento, si verificherebbe un errore? In caso contrario, Rimuovi!
-   La coerenza, la configurabilità e la generalizzazione sono spesso caratteristiche auspicabili, ma possono causare complessità superflue. Esaminare la progettazione per ottenere la coerenza tra le attività, ad esempio con testo ridondante, generalizzazione, ad esempio la presenza di un numero qualsiasi di fusi orari quando è sufficiente, e la configurabilità (ad esempio, le opzioni che gli utenti non possono modificare) ed eliminare gli elementi che possono essere eliminati.
-   **Inserire gli elementi nella posizione corretta.** All'interno di una finestra, la posizione di un elemento deve seguire l'utilità. I controlli, le istruzioni e le spiegazioni essenziali dovrebbero essere tutti nel contesto nell'ordine logico. Se sono necessarie più opzioni, esporle nel contesto facendo clic su una freccia di espansione o un meccanismo simile; Se sono necessarie ulteriori informazioni, visualizzare un infotip al passaggio del mouse. Inserire attività, opzioni e informazioni della guida meno importanti all'esterno del flusso principale in una finestra o in una pagina separata. La tecnica di visualizzazione dei dettagli aggiuntivi in base alle esigenze è detta divulgazione progressiva.
-   **Usare combinazioni significative di alto livello.** Spesso è più semplice e più scalabile selezionare e modificare gruppi di elementi correlati rispetto a singoli elementi. Esempi di combinazioni di alto livello includono cartelle, temi, stili e gruppi di utenti. Tali combinazioni spesso vengono mappate a un obiettivo utente o a un'intenzione che non è evidente dai singoli elementi. Ad esempio, l'intenzione alla base della Contrasto elevato combinazione di colori nero è molto più evidente rispetto a quella di uno sfondo della finestra nera.
-   **Selezionare i controlli corretti.** Gli elementi di progettazione sono incorporati dai controlli usati per rappresentarli, quindi la selezione del controllo appropriato è fondamentale per una presentazione efficiente. Ad esempio, la casella di selezione dei tipi di carattere utilizzata da Microsoft Word Mostra sia un'anteprima del tipo di carattere che i tipi di carattere usati più di recente. Analogamente, il modo in cui Word Mostra i potenziali errori di ortografia e grammatica sul posto è molto più semplice rispetto all'alternativa della finestra di dialogo, come illustrato all'inizio di questo articolo.

Riduzione del lavoro richiesto

"Le cose semplici dovrebbero essere semplici.

Dovrebbero essere possibili aspetti complessi. " -Alan Kay

Le tecniche di progettazione seguenti comportano una riduzione dello sforzo per gli utenti:

-   **Rendere le attività individuabili e visibili.** Tutte le attività, ma soprattutto quelle frequenti, dovrebbero essere facilmente individuabili all'interno dell'interfaccia utente. I passaggi necessari per eseguire le attività devono essere visibili e non devono essere basati sulla memorizzazione.
-   **Presentare attività nel dominio dell'utente.** Il software complesso richiede agli utenti di mappare i problemi alla tecnologia. Il software semplice esegue tale mapping presentando le caratteristiche naturali. Una funzionalità di riduzione degli occhi rossi, ad esempio, è mappata direttamente allo spazio del problema e non richiede che gli utenti pensino in termini di dettagli quali tonalità e sfumature.
-   **Inserire le informazioni di dominio nel programma.** Non è necessario che gli utenti accedano alle informazioni esterne per usare correttamente l'applicazione. La Knowledge base del dominio può variare da dati complessi e algoritmi per chiarire semplicemente il tipo di input valido.
-   **Usare il testo che gli utenti comprendono.** Un testo ben creato è essenziale per la comunicazione efficace con gli utenti. Usare concetti e termini noti agli utenti. Spiega in modo completo cosa viene richiesto in linguaggio semplice, in modo che gli utenti possano prendere decisioni intelligenti e informate.
-   **Usare impostazioni predefinite sicure e sicure.** Se un'impostazione ha un valore che si applica alla maggior parte degli utenti nella maggior parte dei casi e tale impostazione è sicura e sicura, usarla come valore predefinito. Consentire agli utenti di specificare i valori solo quando necessario.
-   **Usare i vincoli.** Se sono disponibili molti modi per eseguire un'attività, ma solo alcuni sono corretti, vincolare l'attività ai modi corretti. Gli utenti non devono essere autorizzati a creare errori prontamente evitabili.

### <a name="simplicity-does-not-mean-simplistic"></a>Semplicità non significa semplicistico

"Tutto dovrebbe essere il più semplice possibile,

ma non più semplice ". -Albert Einstein

Si ritiene che la semplicità sia fondamentale per un'esperienza utente efficace e auspicabile, ma è sempre possibile prendere una valida cosa troppo a lungo. L'essenza della semplicità è la riduzione o l'eliminazione di elementi non essenziali. La rimozione dell'elemento essenziale produce semplicemente un progetto di scarsa qualità. Se la "semplificazione" consente agli utenti di diventare frustrate, confuse, non sicure o non riescono a completare correttamente le attività, è stata rimossa una quantità eccessiva di dati.

### <a name="simplicity-does-mean-more-effort-for-you"></a>La semplicità comporta più sforzi

"Ho fatto questa lettera più a lungo perché ho

non è il momento di renderlo più breve ". -Blaise Pascal

Ottenere semplicità mantenendo la potenza è spesso necessaria una notevole complessità interna. In genere, è più facile progettare software che espone tutto il plumbing della tecnologia rispetto alla progettazione che la nasconde. quest'ultimo richiede una conoscenza ottimale degli utenti di destinazione e dei rispettivi obiettivi. La rimozione di una funzionalità richiede la disciplina, così come si decide di non aggiungere la funzionalità interessante che in realtà non è praticabile. Per semplicità è necessario effettuare scelte di progettazione complesse anziché rendere configurabili tutti gli elementi. Il software complesso spesso deriva da un malinteso sugli utenti, ovvero il fatto che le funzionalità non utilizzate o le funzionalità eccessivamente complesse non sono in grado di comprendere.

## <a name="powerful-and-simple"></a>Potente e semplice

La potenza è l'abilitazione degli utenti e la loro produttività. Il modo più semplice è quello di rimuovere le funzionalità non essenziali e presentando il modo giusto. Grazie alla comprensione degli utenti di destinazione e al raggiungimento del giusto equilibrio tra funzionalità e presentazione, è possibile progettare applicazioni basate su Windows che eseguono entrambe le operazioni.

 

 