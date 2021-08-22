---
title: Come progettare l'esperienza utente per le applicazioni desktop
description: Un'ottima applicazione desktop è potente e, allo stesso tempo, semplice. Grazie alla selezione e alla presentazione delle funzionalità accuratamente bilanciate, è possibile ottenere potenza e semplicità.
ms.assetid: 0039a3ee-95bc-457f-a1a8-6a036ce22fd2
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a9c191a92ccf6147d37deca191a861220c4a925035bf39c92e7e7d062fa14184
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119221733"
---
# <a name="how-to-design-a-great-user-experience-for-desktop-applications"></a>Come progettare un'esperienza utente ottimale per le applicazioni desktop

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Un'ottima applicazione desktop è potente e, allo stesso tempo, semplice. Grazie alla selezione e alla presentazione delle funzionalità accuratamente bilanciate, è possibile ottenere potenza e semplicità.

**Potente:**

![Screenshot della finestra di dialogo ortografia e grammatica ](images/powerful-simple-image1.png)

**Potente e semplice:**

![Screenshot dell'elenco delle possibili revisioni ortografiche ](images/powerful-simple-image2.png)

L'applicazione Windows basata su applicazioni è potente e semplice. Naturalmente si vuole che l'applicazione sia potente e naturalmente si vuole che sia semplice, ma è possibile ottenere entrambi i risultati? C'è una tensione naturale tra questi obiettivi, ma tale tensione non è inconciliabile. È possibile ottenere sia potenza che semplicità tramite la selezione e la presentazione di funzionalità con un'attenzione bilanciata.

## <a name="what-makes-an-application-powerful"></a>Che cosa rende potente un'applicazione?

Che cosa significa realmente "alimentazione" in termini di software? Un'applicazione può essere considerata potente se è piena di funzionalità, con un'enorme gamma di funzionalità nel tentativo di essere tutto per tutti gli utenti. È improbabile che una progettazione di questo tipo abbia esito positivo perché è improbabile che un set di funzionalità non mirate soddisfi le esigenze di chiunque. Questo non è il tipo di alimentazione che si sta verificando.

Un'applicazione è potente quando ha la giusta combinazione di queste caratteristiche:

-   **Abilitazione.** L'applicazione soddisfa le esigenze degli utenti di destinazione, consentendo loro di eseguire attività altrimenti non eseguite e raggiungere gli obiettivi in modo efficace.
-   **Efficiente** L'applicazione consente agli utenti di eseguire attività con un livello di produttività e scalabilità che prima non era possibile.
-   **Versatile.** L'applicazione consente agli utenti di eseguire un'ampia gamma di attività in modo efficace in diverse circostanze.
-   **Diretto.** L'applicazione sembra aiutare direttamente gli utenti a raggiungere i propri obiettivi, invece di insoddire o richiedere passaggi non necessari. Funzionalità come i tasti di scelta rapida, l'accesso tramite tastiera e le macro migliorano il senso di diretta.
-   **Flessibile.** L'applicazione consente agli utenti di controllare con granularità fine il proprio lavoro.
-   **Integrato.** L'applicazione è ben integrata con Microsoft Windows, consentendo di condividere dati con altre applicazioni.
-   **Avanzata** L'applicazione ha caratteristiche straordinarie, innovative e all'avanguardia che non si trovano nelle soluzioni concorrenti.

Alcune di queste caratteristiche dipendono dalla percezione dell'utente e sono relative alle funzionalità correnti degli utenti. Ciò che viene considerato potente può cambiare nel tempo, quindi la funzionalità di ricerca avanzata di oggi potrebbe essere comune domani.

Tutte queste caratteristiche possono essere combinate nella definizione di potenza:

**Un'applicazione è potente quando consente agli utenti di destinazione di realizzare in modo efficiente il loro potenziale completo.**

Di conseguenza, la misura finale della potenza è la produttività, non il numero di funzionalità.

Utenti diversi hanno bisogno di aiuto per ottenere il massimo potenziale in modi diversi. Ciò che consente ad alcuni utenti potrebbe danneggiare la versatilità, la directità e il controllo per altri utenti. Il software ben progettato deve bilanciare queste caratteristiche in modo appropriato. Ad esempio, un sistema di desktop publishing progettato per i non esperti potrebbe usare procedure guidate per illustrare agli utenti attività complesse. Queste procedure guidate consentono agli utenti di destinazione di eseguire attività che altrimenti non sarebbero in grado di eseguire. Al contrario, un sistema di desktop publishing per i professionisti potrebbe concentrarsi su directness, efficienza e controllo completo. Per gli utenti di un'applicazione di questo tipo, le procedure guidate possono essere limitanti e frustranti.

**Se si fa una sola cosa...**

Comprendere gli obiettivi degli utenti di destinazione e creare un set di funzionalità che consenta loro di raggiungere tali obiettivi in modo produttivo.

## <a name="what-makes-a-user-experience-simple"></a>Che cosa rende semplice un'esperienza utente?

La semplicità viene definita come segue:

**La semplicità è la riduzione o l'eliminazione di un attributo di una progettazione di cui gli utenti di destinazione sono a conoscenza e considerano non non essenziali.**

In pratica, la semplicità si ottiene selezionando il set di funzionalità giusto e presentando le funzionalità nel modo giusto. In questo modo si riduce l'inesienziale, reale e percepito.

La semplicità dipende dalla percezione degli utenti. Considerare in che modo l'effetto di una trasmissione automatica dipende dal punto di vista dell'utente:

-   Per il driver tipico (l'utente di destinazione), una trasmissione automatica elimina la necessità di un cambio manuale e di una frizione, rendendo un'auto molto più facile da guidare. Un cambio manuale e una frizione non sono essenziali per il compito di guida, quindi vengono rimossi per ottenere semplicità.
-   Per un pilota professionista, avere il controllo diretto sulla trasmissione è essenziale per essere competitivi. Una trasmissione automatica influisce negativamente sulle prestazioni dell'auto, quindi non viene considerata come semplice.
-   Per un meccanico, una trasmissione automatica è un meccanismo più complesso e quindi non è più facile da ripristinare o gestire rispetto a una trasmissione manuale. A differenza del meccanismo, l'utente di destinazione non è inconsapevole di questa complessità interna.

Sebbene utenti diversi considerino la trasmissione automatica in modo diverso, la trasmissione ha esito positivo perché elimina la necessità di conoscenze, competenze e impegno non irrealiscibili da parte degli utenti di destinazione. Per il driver tipico, la trasmissione automatica è un'ottima funzionalità perché funziona solo.

### <a name="simplicity-vs-ease-of-use"></a>Semplicità e semplicità d'uso

La semplicità, se applicata correttamente, comporta una facilità d'uso. La semplicità e la facilità d'uso non sono tuttavia gli stessi concetti. La facilità d'uso si ottiene quando gli utenti possono eseguire correttamente un'attività da soli senza difficoltà o confusione entro un periodo di tempo appropriato. Esistono molti modi per ottenere la facilità d'uso e la semplicità, ovvero la riduzione dell'non essenziali, è solo uno di questi.

Tutti gli utenti, indipendentemente dal livello di sofisticato, vogliono eseguire il proprio lavoro con una quantità minima di lavoro non necessario. Tutti gli utenti, anche gli utenti avanzati, sono principalmente motivati a eseguire il proprio lavoro, non a conoscere i computer o l'applicazione.

La semplicità è il modo più efficace per ottenere la facilità d'uso e la semplicità d'uso è uguale all'uso. Le funzionalità complesse e difficili da usare non vengono usate. Al contrario, i design semplici ed eleganti che eseguono bene la loro funzione sono un piacere da usare. Richiamano una risposta positiva ed emozionale.

Si consideri, ad esempio, il supporto della rete wireless in Microsoft Windows XP. Microsoft potrebbe aver aggiunto una procedura guidata per illustrare agli utenti il processo di configurazione. Questo approccio avrebbe comportato una facilità d'uso ma non una semplicità, perché sarebbe stata aggiunta una funzionalità non non di tipo non formale (la procedura guidata). Microsoft ha invece progettato la rete wireless per la configurazione automatica. Gli utenti in definitiva non si preoccupano dei dettagli di configurazione, purché funzionino in modo affidabile e sicuro. Questa combinazione di potenza e semplicità nella tecnologia di rete wireless ha portato alla sua popolarità e alla rapida adozione.

**Se si fa una sola cosa...**

Avviare il processo di progettazione con le progettazioni più semplici che fanno bene il processo.

Se non si è soddisfatti della progettazione corrente, iniziare rimuovendo tutti gli elementi non nonenti. Si scoprirà che ciò che rimane è in genere piuttosto buono.

## <a name="obtaining-simplicity-while-maintaining-power"></a>Ottenere semplicità mantenendo l'alimentazione

### <a name="design-principles"></a>Principi di progettazione

Per ottenere semplicità, progettare sempre per il probabile, non il possibile.

Possibile

Le decisioni di progettazione basate su ciò che è possibile comportano interfacce utente complesse come l'editor del Registro di sistema, in cui la progettazione presuppone che tutte le azioni siano ugualmente possibili e di conseguenza richiedono pari impegno. Poiché tutto è possibile, gli obiettivi degli utenti non vengono considerati nelle decisioni di progettazione.

Probabile

Decisioni di progettazione basate sul probabile vantaggio di soluzioni semplificate, basate su obiettivi e attività, in cui gli scenari probabili ricevono lo stato attivo e richiedono un impegno minimo per l'esecuzione.

Principio di progettazione della semplicità

**Per ottenere semplicità, concentrarsi su ciò che è probabile; ridurre, nascondere o rimuovere ciò che è improbabile; ed eliminare ciò che è impossibile.**

Ciò che gli utenti fanno è molto più rilevante per la progettazione rispetto a quello che potrebbero fare.

### <a name="design-techniques"></a>Tecniche di progettazione

Per ottenere semplicità mantenendo l'alimentazione, scegliere il  **set** di funzionalità giusto, individuare le funzionalità nelle posizioni giuste e ridurre il lavoro **necessario** per usarle. Questa sezione offre alcune tecniche comuni per raggiungere questi obiettivi.

Scelta del set di funzionalità giusto

"La perfezione si ottiene, non quando non c'è altro da aggiungere,

ma quando non c'è più nulla da portare via." — Antoine de Saint-Exupery

Le tecniche di progettazione seguenti offrono agli utenti le funzionalità necessarie, ottenendo al tempo stesso la semplicità tramite la riduzione o la rimozione effettiva:

-   **Determinare le funzionalità necessarie agli utenti.** Comprendere le esigenze degli utenti tramite l'obiettivo, lo scenario e l'analisi delle attività. Determinare un set di funzionalità che realizzano questi obiettivi.
-   **Rimuovere gli elementi non necessari.** Rimuovere gli elementi che probabilmente non verranno usati o che hanno alternative preferibili.
-   **Rimuovere la ridondanza non necessaria.** Esistono diversi modi efficaci per eseguire un'attività. Per ottenere semplicità, prendere la decisione più difficile e scegliere quella migliore per gli utenti di destinazione invece di fornirli tutti e fare della scelta un'opzione.
-   **Renderlo "just work" automaticamente.** L'elemento è necessario, ma qualsiasi interazione dell'utente per farlo funzionare non è perché esiste un comportamento o una configurazione predefinita accettabile. Per ottenere semplicità, farlo funzionare automaticamente e nasconderlo completamente all'utente o ridurne in modo significativo l'esposizione.

Struttura della presentazione

"La possibilità di semplificare significa eliminare gli elementi non necessari

in modo che il necessario possa parlare." — Hans Hofmann

Usare le tecniche di progettazione seguenti per mantenere la potenza, ottenendo al tempo stesso la semplicità attraverso la percezione di riduzione o rimozione:

-   **Combinare gli elementi da combinare.** Mettere insieme le funzionalità essenziali che supportano un'attività in modo che un'attività possa essere eseguita in un'unica posizione. I passaggi dell'attività devono avere un flusso unificato e semplificato. Suddividere le attività complesse in un set di passaggi semplici e chiari, in modo che "una" posizione possa essere costituita da diverse superfici dell'interfaccia utente, ad esempio una procedura guidata.
-   **Separare gli elementi da separare.** Non tutto può essere presentato in un'unica posizione, quindi avere sempre limiti chiari e ben scelti. Rendere centrali e ovvie le funzionalità che supportano gli scenari principali e nascondere le funzionalità facoltative o renderle periferiche. Separare le singole attività e fornire collegamenti alle attività correlate. Ad esempio, le attività correlate alla modifica delle foto devono essere chiaramente separate dalle attività correlate alla gestione delle raccolte di foto, ma devono essere facilmente accessibili l'una dall'altra.
-   **Eliminare ciò che può essere eliminato.** Eseguire una stampa della progettazione ed evidenziare gli elementi usati per eseguire le attività più importanti. Evidenziare anche le singole parole nel testo dell'interfaccia utente che comunicano informazioni utili. Esaminare ora ciò che non è evidenziato e provare a rimuoverlo dalla progettazione. Se si rimuove l'elemento, si verifica qualcosa di negativo? In caso contrario, rimuoverlo.
-   La coerenza, la configurabilità e la generalizzazione sono spesso qualità desiderabili, ma possono causare inutili complessità. Esaminare la progettazione per le attività erre nella coerenza (ad esempio con testo ridondante), generalizzazione (ad esempio con un numero qualsiasi di fusi orari quando ne sono sufficienti due) e configurabilità (ad esempio opzioni che gli utenti non sono in grado di modificare) ed eliminare ciò che può essere eliminato.
-   **Inserire gli elementi nella posizione giusta.** All'interno di una finestra, la posizione di un elemento deve seguire la relativa utilità. I controlli, le istruzioni e le spiegazioni essenziali devono essere tutti nel contesto in ordine logico. Se sono necessarie altre opzioni, esporle nel contesto facendo clic su una freccia di controllo o un meccanismo simile; Se sono necessarie altre informazioni, visualizzare un suggerimento al passaggio del mouse. Inserire attività, opzioni e informazioni della Guida meno importanti all'esterno del flusso principale in una finestra o in una pagina separata. La tecnica di visualizzazione di dettagli aggiuntivi in base alle esigenze è detta divulgazione progressiva.
-   **Usare combinazioni significative di alto livello.** Spesso è più semplice e scalabile selezionare e modificare gruppi di elementi correlati rispetto ai singoli elementi. Esempi di combinazioni di alto livello includono cartelle, temi, stili e gruppi di utenti. Queste combinazioni spesso vengono mappate a un obiettivo o a un'intenzione dell'utente che non è evidente dai singoli elementi. Ad esempio, l'intenzione alla base della combinazione Contrasto elevato colore nero è molto più evidente di quella di uno sfondo di una finestra nera.
-   **Selezionare i controlli a destra.** Gli elementi di progettazione sono racchiusi tra i controlli utilizzati per rappresentarli, quindi la selezione del controllo giusto è fondamentale per una presentazione efficiente. Ad esempio, la casella di selezione del tipo di carattere usata Microsoft Word mostra sia un'anteprima del tipo di carattere che i tipi di carattere usati più di recente. Analogamente, il modo in cui Word mostra potenziali errori di ortografia e grammatica è molto più semplice rispetto all'alternativa della finestra di dialogo, come illustrato all'inizio di questo articolo.

Riduzione dell'impegno

"Le cose semplici dovrebbero essere semplici.

Le cose complesse dovrebbero essere possibili." - Alan Kay

Le tecniche di progettazione seguenti comportano un impegno ridotto per gli utenti:

-   **Rendere le attività individuabili e visibili.** Tutte le attività, ma soprattutto le attività frequenti, devono essere facilmente individuabili all'interno dell'interfaccia utente. I passaggi necessari per eseguire le attività devono essere visibili e non devono basarsi sulla memorizzazione.
-   **Presentare attività nel dominio dell'utente.** Il software complesso richiede agli utenti di eseguire il mapping dei problemi alla tecnologia. Il software semplice esegue tale mapping presentando ciò che è naturale. Ad esempio, una funzionalità di riduzione degli occhi rossi viene mappata direttamente allo spazio problematico e non richiede agli utenti di pensare in termini di dettagli come tonalità e sfumature.
-   **Inserire le informazioni di dominio nel programma.** Agli utenti non deve essere richiesto di accedere a informazioni esterne per usare correttamente l'applicazione. Le conoscenze del dominio possono variare da dati complessi e algoritmi a semplici chiarimenti sul tipo di input valido.
-   **Usare testo comprensibile agli utenti.** Il testo ben creato è fondamentale per una comunicazione efficace con gli utenti. Usare concetti e termini familiari per gli utenti. Spiegare in modo completo ciò che viene richiesto in un linguaggio normale in modo che gli utenti possano prendere decisioni intelligenti e informate.
-   **Usare impostazioni predefinite sicure, sicure e probabili.** Se un'impostazione ha un valore che si applica alla maggior parte degli utenti nella maggior parte dei casi e tale impostazione è sicura e sicura, usarla come valore predefinito. Fare in modo che gli utenti specificano i valori solo quando necessario.
-   **Usare i vincoli.** Se esistono molti modi per eseguire un'attività, ma solo alcuni sono corretti, vincolare l'attività ai modi corretti. Agli utenti non deve essere consentito commettere errori facilmente evitabili.

### <a name="simplicity-does-not-mean-simplistic"></a>La semplicità non significa semplicistica

"Tutto deve essere reso il più semplice possibile,

ma non più semplice." -Albert Alberto

La semplicità è fondamentale per un'esperienza utente efficace e desiderabile, ma è sempre possibile andare troppo oltre. L'essenzialità della semplicità è la riduzione o l'eliminazione dell'nonesential. La rimozione dell'essenziale produce semplicemente una progettazione scadente. Se la "semplificazione" comporta che gli utenti diventino frustrati, confusi, non confermati o non in grado di completare correttamente le attività, è stato rimosso troppo.

### <a name="simplicity-does-mean-more-effort-for-you"></a>La semplicità significa più impegno per l'utente

"Ho creato questa lettera solo più a lungo perché ho

non è il momento di renderlo più breve." - Blaise Pascal

Ottenere semplicità mantenendo al tempo stesso l'alimentazione spesso richiede una complessità interna significativa. In genere è più facile progettare software che espone tutto il plumbing tecnologico piuttosto che progettarne uno che lo nasconde. Quest'ultimo richiede una conoscenza eccellente degli utenti di destinazione e dei relativi obiettivi. La rimozione di una funzionalità richiede disciplina, così come decidere di non aggiungere quella funzionalità interessante che non è pratica. La semplicità richiede scelte di progettazione difficili anziché rendere tutto configurabile. Il software complesso spesso deriva da un'errata concepizione degli utenti: che valorizzato le funzionalità inutilizzate o funzionalità troppo complesse che non possono comprendere.

## <a name="powerful-and-simple"></a>Potente e semplice

Power è tutto ciò che riguarda l'abilitazione degli utenti e la loro produttività. La semplicità riguarda la rimozione delle funzionalità non essenziali e la presentazione nel modo giusto. Comprendendo gli utenti di destinazione e ottenendo il giusto equilibrio tra funzionalità e presentazione, è possibile progettare applicazioni basate Windows che eseguino entrambe le operazioni.

 

 