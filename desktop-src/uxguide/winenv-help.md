---
title: Help
description: Usare la guida come meccanismo secondario per aiutare gli utenti a completare e comprendere meglio le attività \ 8212; il meccanismo principale è l'interfaccia utente. Applicare queste linee guida per rendere il contenuto realmente utile e facile da trovare.
ms.assetid: 82ce076e-062b-4793-a1c0-ed96c0f2b284
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 907494e9a97ccaf51e4eba463c34e49854b14a81
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104552996"
---
# <a name="help"></a>Help

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Usare la guida come meccanismo secondario per aiutare gli utenti a completare e comprendere meglio le attività. il meccanismo principale è l'interfaccia utente. Applicare queste linee guida per rendere il contenuto realmente utile e facile da trovare.

Un sistema di guida è costituito da vari tipi di contenuto progettati per assistere gli utenti quando non sono in grado di completare un'attività, di comprendere un concetto in modo più dettagliato o di richiedere dettagli più tecnici rispetto a quelli disponibili nell'interfaccia utente.

In questo articolo si fa riferimento alla guida come secondaria dell'interfaccia utente. L'interfaccia utente è primaria perché gli utenti tentano innanzitutto di risolvere i problemi. Consultano il sistema di guida solo se non riescono a eseguire l'attività con l'interfaccia utente.

![screenshot della pagina Guida e supporto tecnico di Windows ](images/winenv-help-image1.png)

Il home page guida e supporto tecnico di Windows, disponibile dal menu Start.

**Nota:** Le linee guida correlate allo [stile e al tono](text-style-tone.md) sono presentate in un articolo separato.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendi in considerazione queste domande:

-   **Quanto sono motivati gli utenti di destinazione?** Più sono motivati a individuare le funzionalità del programma e a diventare utenti intermedi o anche avanzati, più saranno disponibili per la ricerca di risposte alle proprie domande da parte degli argomenti della guida.
-   **Si sta usando la guida per correggere un'interfaccia utente non valida?** Maggiore è l'interfaccia utente, minore sarà il numero di utenti che cercheranno assistenza aggiuntiva. Se il programma ha un'interfaccia utente primaria molto chiara e utile, ad esempio messaggi di errore di gergo, procedure guidate ben scritte e finestre di dialogo non ambigue, potrebbe non essere necessario un sistema di guida secondario.
-   **Il programma è relativamente semplice?** In tal caso, è consigliabile incorporare tutto il contenuto di assistenza necessario nelle superfici primarie dell'interfaccia utente. È più probabile che gli utenti richiedano ulteriore assistenza nei programmi che eseguono attività complesse.
-   **L'applicazione è destinata a sviluppatori, professionisti IT o altri esperti software?** Questi utenti tendono a prevedere la Guida di riferimento per le convenzioni del linguaggio di programmazione e la Guida concettuale approfondita per la padronanza delle funzionalità.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Se si decide di includere la guida nel programma, integrarla nel progetto generale. L'interfaccia della guida deve essere semplice, efficiente e pertinente; deve consentire agli utenti di ottenere facilmente assistenza e quindi tornare alla propria attività. È possibile considerare il sistema di guida in termini di tempo per gli utenti: ridurre al minimo le problematiche, anticipando la posizione in cui si verificheranno problemi nel programma, risolvendo tali problemi incorporando assistenza fondamentale nell'interfaccia utente e creando punti di ingresso chiari e coerenti nella guida più dettagliata.

Windows Assistance è stato progettato in base a questi principi. Di seguito sono riportate alcune delle modifiche di progettazione all'esperienza utente della Guida di Windows:

-   Punti di ingresso più individuabili per facilitare l'interfaccia utente primaria (in particolare i nuovi collegamenti alla guida dalle superfici dell'interfaccia utente, ad esempio le finestre di dialogo, i messaggi di errore e le procedure guidate). I collegamenti alla guida consentono di passare direttamente all'argomento pertinente nella Guida di.
-   L'icona di un pulsante? è disponibile nell'angolo superiore destro della maggior parte delle pagine dell'hub del pannello di controllo e nelle cartelle della shell.
-   Gli utenti possono scegliere di ottenere il contenuto della guida più aggiornato dalla guida e dal supporto tecnico di Windows in linea.
-   Gli argomenti della guida sono ora basati sulle attività piuttosto che sulle funzionalità, in modo che gli utenti possano eseguire le proprie attività in modo rapido ed efficiente.
-   Gli argomenti della guida si basano principalmente sugli scenari noti degli utenti principali.
-   Gli argomenti della guida hanno un [tono](text-style-tone.md)più rilassato e informale, usando il linguaggio del mondo reale.
-   Gli argomenti della guida sono progettati per un'analisi efficace, perché gli utenti leggono raramente il contenuto di Word per Word.

### <a name="an-analogy-for-help"></a>Analogie per la guida

Per una maggiore profondità sulla progettazione del sistema di guida, prendere in considerazione un'analogia rispetto alla vita quotidiana. Si è perso in una città non nota. Come si deve procedere? Molti reagiranno come segue:

-   Orientarsi; cercare i punti di riferimento, i simboli via (nomi e puntatori alle posizioni).
-   Cercare maps.
-   Infine, come ultima risorsa, richiedere indicazioni o chiamare un amico.

La progettazione della "interfaccia" della città influiscono sulla necessità di assistenza. Le strade ben etichettate, le direzioni esplicite (puntatori agli ospedali, gli aeroporti, i musei e l'ufficio postale) e i punti di riferimento più evidenti, ad esempio le funzionalità geografiche prominenti, consentono di trovare il modo desiderato.

È possibile richiedere assistenza come ultima risorsa. Si tratta di un'indicazione che l'"interfaccia" della città ha avuto esito negativo grazie alla scarsa progettazione e confusione. È più probabile che si chieda assistenza in una posizione con un'etichetta specifica che suggerisce l'utilità. Ad esempio, è più probabile che si chieda assistenza in un posto con etichetta "Directions" o "Information" rispetto a un posto generale come City Hall anche se tutti gli utenti di City Hall potrebbero fornire indicazioni.

Quando si richiede assistenza, è probabile che l'utente sia frustrato e voglia semplicemente raggiungere la destinazione desiderata. Probabilmente non si è in vena di dedicare molto tempo alla visita della città o all'apprendimento della relativa cronologia. Inoltre, la motivazione dipende dall'importanza dell'attività. Se si sta provando a trovare la chat room, sarà necessario eseguire tutte le operazioni necessarie. Tuttavia, se l'obiettivo è quello di trovare un posto di importanza minore, molto probabilmente si cederà solo dopo un modesto sforzo.

Tutti questi aspetti della ricerca di un modo nello spazio reale corrispondono a come gli utenti in genere si trovano nello spazio virtuale del programma. La ricerca di una guida oltre l'interfaccia utente primaria è per sua natura disorientata; è possibile mitigare questa esperienza grazie a un'interfaccia utente ben progettata e a "strade" intelligenti per indirizzare gli utenti alle risposte necessarie.

### <a name="designing-ui-so-that-help-is-unnecessary"></a>Progettazione dell'interfaccia utente in modo che la guida non sia necessaria

Provare a rendere superflua la Guida in primo luogo, per:

-   Semplificare l'individuazione e l'esecuzione di attività comuni.
-   Fornire [istruzioni principali](text-ui.md)chiare.
-   Fornire etichette di controllo chiare e concise che siano orientate a obiettivi e attività.
-   Fornire istruzioni e spiegazioni aggiuntive laddove necessario.
-   Prevedere problemi evitabili utilizzando i controlli vincolati a scelte valide, fornendo valori predefiniti appropriati, gestendo tutti i formati di input ed evitando errori.
-   Scrittura di messaggi di errore che forniscono una soluzione o un'azione chiara che l'utente deve eseguire.
-   Evitare la confusione delle progettazioni dell'interfaccia utente, ad esempio le attività con un flusso scarso o l'uso di controlli disabilitati per nessun motivo apparente.
-   Collaborando con Writer e editor all'inizio del ciclo di sviluppo per creare [testo dell'interfaccia utente](text-ui.md) coerente e di alta qualità in tutto il programma.

Gli utenti non devono andare altrove per capire come usare l'interfaccia utente. Aggiungere informazioni essenziali direttamente nell'interfaccia utente primaria, anziché forzare gli utenti al di fuori del contesto immediato e nel riquadro della guida. Se sono presenti informazioni importanti solo in un argomento della guida, è probabile che gli utenti non lo vedranno. Per informazioni facoltative e più esplicative, usare i collegamenti della guida dall'interfaccia utente primaria all'argomento della Guida pertinente per assistenza aggiuntiva.

### <a name="considering-user-motivation"></a>Considerazione della motivazione degli utenti

Per la maggior parte degli utenti, la velocità e l'efficienza sono tra le virtù principali dei programmi validi. Gli utenti desiderano svolgere il proprio lavoro. In genere, non sono interessati a conoscere il programma e la tecnologia per il proprio scopo; la loro pazienza si estende solo in quanto il programma si serve dei propri interessi e risolve i problemi a sua disposizione.

Progettare il sistema di supporto in modo che corrisponda alla motivazione degli utenti. Si consideri, ad esempio, un utente che ha eseguito una passeggiata a un chiosco in un museo. Se non riesce a capire come eseguire l'attività in modo rapido, è probabile che sia sufficiente abbandonarla e uscire. Non è improbabile dedicare tempo all'utilizzo della guida. In alternativa, un utente altamente motivato ha una tolleranza superiore per il tempo impiegato per la ricerca di risposte nel sistema della guida. Un utente aziendale che deve bilanciare i libri, ad esempio, è probabilmente disposto a consultare il contenuto della Guida per sfruttare al meglio la nuova applicazione contabile.

### <a name="writing-content-for-scanning"></a>Scrittura di contenuto per l'analisi

Scrivere gli argomenti della Guida sapendo che verranno analizzati per ottenere informazioni specifiche, non leggere Word-for-Word. Scrivere in modo conciso, raggiungere rapidamente il punto e fornire informazioni su cui gli utenti possono agire.

-   Scrivere gli argomenti "procedure" usando i passaggi numerati in un formato coerente, in modo che gli utenti riconoscano che ricevono assistenza procedurale.
-   Scrivere gli argomenti di riferimento con una semplice analisi, usando le tabelle, ad esempio, per presentare le opzioni dell'interfaccia utente o la sintassi del linguaggio.
-   Scrivere argomenti concettuali organizzati in modo logico in base a sottointestazioni, in modo che l'utente possa ignorare intere sezioni di minore interesse.

In tutto il contenuto della guida è più semplice analizzare elenchi puntati rispetto ai blocchi di testo di paragrafo standard. usare i Bullet list con cautela, ma non come una stampella per il materiale non organizzato.

### <a name="creating-content-that-matters"></a>Creazione di contenuti importanti

Dato che nessun sistema di guida può prevedere tutte le domande che ogni utente potrebbe avere, concentrare la maggior parte del contenuto sulla risposta alle domande principali negli scenari principali per gli utenti di destinazione. Ad esempio, la ricerca efficace e come stabilire la connettività di rete (tra le altre attività) può essere un argomento molto ricercato. Inoltre, è possibile concentrarsi sulle attività all'interno degli scenari utente principali, anziché documentare in maniera esauriente una funzionalità o una tecnologia.

**Suggerimento:** Il supporto tecnico è una fonte ideale per il contenuto della guida. I supporto tecnico spesso mantengono i record delle domande frequenti relative a specifici programmi o attività che gli utenti tentano di eseguire.

Non è necessario fornire supporto per tutte le funzionalità dell'interfaccia utente. **Molto spesso, la guida non aiuta i risultati del tentativo di creare una guida per tutti gli elementi.** Se l'interfaccia utente è progettata correttamente, la maggior parte di questi argomenti della guida non sarà molto utile. verranno riaffermati solo gli elementi evidenti.

Se è disponibile più di un modo per eseguire un'attività, nella maggior parte dei casi è possibile semplicemente documentare il modo più comune usato dagli utenti inesperti. Le eccezioni includono considerazioni sull'accessibilità (documentazione degli equivalenti di tastiera delle azioni del mouse, ad esempio) e considerazioni sulla piattaforma (documentazione per il fattore di forma del tablet, ad esempio, o per ambienti server in cui la riga di comando può sostituire l'interfaccia utente grafica).

Tenere presente che gli utenti spesso non pensano ai problemi riscontrati in modo identico alle stesse condizioni. Ad esempio, è possibile che gli utenti richiedano se stessi come "account". Assicurarsi di progettare le funzionalità di ricerca e indicizzazione, quindi per tenere conto di probabili varianti di terminologia e sinonimi.

Tra l'interfaccia utente principale e il sistema di guida, tuttavia, i termini dovrebbero essere molto simili se non identici. Gli utenti possono essere confusi quando il linguaggio del sistema di guida non è strettamente correlato a quanto visualizzato sullo schermo.

### <a name="writing-compelling-help-link-text"></a>Scrittura del testo del collegamento alla guida interessante

Quando si collega a un argomento della guida dall'interfaccia utente primaria, assicurarsi di scrivere un testo interessante del collegamento alla guida. Il linguaggio chiaro e specifico ispira la fiducia. Gli utenti tendono a credere che i collegamenti generici della guida (un pulsante con la parola "Help" o "Learn more") non consentiranno di ottenere le informazioni corrette senza un investimento significativo nel tempo.

**Se si eseguono solo cinque operazioni...**

1.  Progettare l'interfaccia utente in modo che gli utenti non necessitino di aiuto.
2.  Consente di rendere disponibile il supporto concentrando il contenuto sulle domande principali negli scenari principali per gli utenti di destinazione.
3.  Presentare il contenuto della Guida in modo che sia facile da analizzare.
4.  Tenere presente che non è necessario fornire supporto per tutte le funzionalità dell'interfaccia utente.
5.  Rendere i punti di ingresso della Guida individuabili e accattivanti.

## <a name="usage-patterns"></a>Modelli di utilizzo

Diversi tipi di contenuto servono a scopi diversi.



|                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guida procedurale**<br/> viene descritta la procedura per eseguire un'attività. <br/>                       | La guida procedurale dovrebbe concentrarsi sulle informazioni "how" invece che su "What" o "Why". <br/> ![screenshot della pagina della Guida relativa all'eliminazione dei file temporanei ](images/winenv-help-image2.png)<br/> In questo esempio, l'argomento della guida descrive come usare una funzionalità dell'utilità di pulitura del disco, che fornisce i passaggi da seguire in sequenza.<br/>                                              |
| **Guida concettuale**<br/> fornisce informazioni di base, panoramiche sulle funzionalità o processi. <br/> | La Guida concettuale deve fornire informazioni "cosa" o "perché" oltre a quelle necessarie per completare un'attività. <br/> ![screenshot della pagina della Guida relativa al desktop (panoramica) ](images/winenv-help-image3.png)<br/> In questo esempio, l'argomento della guida definisce le informazioni sul desktop e fornisce dettagli aggiuntivi sugli elementi che contiene e sul motivo per cui gli utenti interagiscono con esso.<br/>           |
| **Guida di riferimento**<br/> funge da libro di riferimento online. <br/>                                | È possibile utilizzare la Guida di riferimento per documentare un linguaggio di programmazione o interfacce di programmazione. <br/> ![screenshot della pagina della Guida "Notational Conventions" ](images/winenv-help-image4.png)<br/> In questo esempio, l'argomento della guida elenca le convenzioni tipografiche in uso per questa particolare lingua o applicazione, fornendo le informazioni in una tabella di facile analisi.<br/> |



 

## <a name="guidelines"></a>Indicazioni

### <a name="entry-points"></a>Punti di ingresso

-   **Collegamento a specifici argomenti della guida pertinenti.** Non eseguire il collegamento al home page della guida, al sommario, a un elenco di risultati della ricerca o a una pagina che si limita solo a collegamenti ad altre pagine. Evitare il collegamento a pagine strutturate come un ampio elenco di domande frequenti, perché impone agli utenti di cercare quello che corrisponde al collegamento selezionato. Non eseguire il collegamento ad argomenti della Guida specifici che non sono rilevanti e utili per l'attività. Non collegare mai a pagine vuote.
-   **Non inserire collegamenti Guida in ogni finestra o pagina per motivi di coerenza.** Fornire un collegamento alla Guida in un'unica posizione non significa che è necessario fornirli ovunque.
-   **Usare i collegamenti della Guida per le finestre di dialogo, i messaggi di errore, le procedure guidate e le finestre delle proprietà.** Se il collegamento alla guida si applica a controlli specifici, posizionarlo sotto di essi, allineato a sinistra. Se il collegamento alla guida si applica all'intera finestra, posizionarlo nell'angolo inferiore sinistro dell'area di contenuto della finestra.

    ![screenshot della finestra delle proprietà con la casella di gruppo ](images/winenv-help-image5.png)

    In questo esempio il secondo collegamento alla guida si applica a un gruppo di controlli.

    ![screenshot della finestra delle proprietà e del collegamento alla guida ](images/winenv-help-image6.png)

    In questo esempio il collegamento alla guida si applica all'intera finestra.

-   **Usare i collegamenti della Guida anziché i riferimenti testuali generici per aiutare ogni volta che è tecnicamente possibile.**

    **Corretto:**

    Come è possibile correggere gli errori del disco?

    **Non corretto:**

    Per ulteriori informazioni sul ripristino degli errori del disco, vedere Guida e supporto tecnico.

-   **Usare un pulsante? con l'icona della Guida per le pagine dell'hub degli elementi del pannello di controllo.** Posizionarlo nell'angolo superiore destro. Questi pulsanti non hanno un'etichetta, ma dispongono di una descrizione comando che legge la guida.

    ![screenshot dell'elemento del pannello di controllo con pulsante? ](images/winenv-help-image7.png)

    Elemento del pannello di controllo con un pulsante?.

-   **La Guida sensibile al contesto è facoltativa.** Gli utenti si sono abituati a trovare informazioni della Guida correlate al contesto immediato dell'interfaccia utente sullo schermo premendo il tasto F1, che è contrassegnato come guida sulle tastiere standard. È possibile includere la Guida sensibile al contesto se, ad esempio, gli studi di usabilità indicano che gli utenti si aspettano di trovarlo o che l'interfaccia utente del programma è sufficientemente complessa da trarre vantaggio dall'assistenza contestuale.
-   **I programmi con barre dei menu possono avere una categoria di menu della guida.** Per indicazioni sui menu della guida, vedere [menu](cmd-menus.md).

    ![screenshot della guida a cui si accede dalla barra dei menu ](images/winenv-help-image8.png)

    In questo esempio, l'accessorio Windows Paint presenta una categoria di menu della guida.

-   **Per l'accessibilità da tastiera, fornire tabulazioni per i pulsanti e i collegamenti della guida.**
-   Il pulsante della guida e il comportamento del collegamento devono essere i seguenti: viene aperto il riquadro della guida e viene visualizzato un argomento della guida dedicato. l'interfaccia utente che ha richiamato il riquadro della guida deve rimanere aperta per mantenere l'esperienza contestuale.
-   **Non usare gli stili dei punti di ingresso della Guida obsoleti seguenti: "ulteriori informazioni" o "ulteriori informazioni su..." collegamenti, pulsanti della Guida generici e pulsanti Guida sensibili al contesto sulla barra del titolo.** Sebbene siano stati usati in passato, gli studi sull'usabilità hanno determinato che gli utenti tendono a ignorarli. Usare invece i collegamenti ad argomenti della Guida specifici. Per le linee guida sulla scrittura di collegamenti guida validi, vedere [collegamenti alla guida](#text).

    **Non corretto:**

    ![screenshot della finestra di dialogo con un collegamento ' altre informazioni ' ](images/winenv-help-image9.png)

    Non usare "ulteriori informazioni" o "ulteriori informazioni su..." collegamenti.

    **Non corretto:**

    ![cattura di schermata del pulsante della guida accanto ai pulsanti di commit ](images/winenv-help-image10.png)

    Non usare pulsanti della Guida generici.

    **Non corretto:**

    ![screenshot dell'icona del punto interrogativo sulla barra del titolo ](images/winenv-help-image11.png)

    Non usare pulsanti Guida sensibili al contesto sulla barra del titolo.

### <a name="content"></a>Content

-   **Non creare contenuti evidenti.** Gli argomenti della guida che ripetono l'interfaccia utente primaria non aggiungono valore.
-   **Non creare contenuto su cui l'utente non può agire in qualche modo.**
    -   **Eccezione:** Alcuni contenuti concettuali forniscono importanti informazioni complementari senza necessariamente comportare l'intervento dell'utente.
-   **Evitare risoluzioni vaghe ai problemi.** Ad esempio, "contattare l'amministratore di sistema" o "reinstallare l'applicazione" tende a vanificare gli utenti.
    -   **Eccezione:** È consigliabile contattare l'amministratore di sistema se questa è l'unica soluzione pratica e gli amministratori di sistema si aspettano di essere contattati per il problema.
-   **Evitare contenuti che indirizzino scenari utente altamente improbabili.** Sviluppare il contenuto della guida principale per quanto previsto sarà l'utilizzo normale; prendere nota delle eccezioni importanti per l'utilizzo previsto, ma considerare questo contenuto come una priorità più bassa.
-   **Raccogliere commenti e suggerimenti degli utenti su come sono disponibili gli argomenti della guida.** Consente agli utenti di valutare singoli argomenti. Condurre [studi sull'usabilità](glossary.md) sulla documentazione per verificare i problemi che coinvolgono la qualità e l'individuabilità del contenuto.
    -   **Suggerimento:** Il feedback degli utenti è anche un ottimo modo per generare un contenuto più basato su attività, incentrato sulle operazioni effettivamente svolte dagli utenti con il programma, in contrapposizione al contenuto basato su funzionalità, che si concentra semplicemente su una descrizione della tecnologia.
-   **Fornire più modalità di accesso ai contenuti.** Un sommario, un indice e un meccanismo di [ricerca](ctrl-search-boxes.md) sono tre dei metodi più comuni per migliorare l'individuabilità.
-   **Se è disponibile più di un modo per eseguire un'attività, nella maggior parte dei casi è possibile semplicemente documentare il modo più comune usato dagli utenti inesperti.**

### <a name="icons"></a>Icone

-   Usare l'icona della guida solo per le finestre di esplorazione e le pagine dell'hub degli elementi del pannello di controllo. Non usare l'icona della guida con i collegamenti della guida.

**Corretto:**

![screenshot della finestra con icona del punto interrogativo ](images/winenv-help-image12.png)

In questo esempio, una finestra di Esplora risorse utilizza un'icona della Guida per fornire l'accesso alla guida.

**Non corretto:**

![screenshot della finestra con icona della guida nel pannello sinistro ](images/winenv-help-image13.png)

In questo esempio, l'icona della Guida in basso a sinistra viene utilizzata in modo non corretto con un collegamento alla guida.

## <a name="text"></a>Testo

**Collegamenti alla guida**

-   Fornire informazioni specifiche sul contenuto dell'argomento della guida, usando un testo conciso e molto pertinente, se necessario. Spesso gli utenti ignorano i collegamenti della Guida generici. Assicurarsi che i risultati del collegamento siano utenti stimabili non devono essere sorpresi dai risultati.

    -   **Eccezione:** È possibile usare "ulteriori informazioni" per integrare le istruzioni direttamente nell'interfaccia utente, soprattutto se la fornitura di informazioni specifiche nel collegamento alla guida comporta una ripetizione superflua o rende meno accattivante il collegamento.

    **Non corretto:**

    Una password complessa ha almeno sei lettere, numeri e simboli con lettere maiuscole. Che cos'è una password complessa?

    **Corretto:**

    Una password complessa ha almeno sei lettere, numeri e simboli con lettere maiuscole. Ulteriori informazioni

    Nell'esempio errato il collegamento alla guida è ripetitivo. Si pone una domanda a cui è effettivamente già stata fornita una risposta.

-   Laddove possibile, frasere il testo del collegamento alla Guida in termini di domanda principale fornita dal contenuto della guida. Non usare "ulteriori informazioni su", "ulteriori informazioni su" o "ottenere assistenza per questo".

    **Non corretto:**

    Altre informazioni sull'aggiunta di eccezioni

    **Corretto:**

    Quali sono i rischi per consentire le eccezioni?

    Ricerca per categorie aggiungere eccezioni?

    Negli esempi corretti, il collegamento viene formulato in base alla domanda principale fornita dall'argomento della guida.

-   Se le informazioni più rilevanti possono essere riepilogate concisamente, inserire il riepilogo direttamente nell'interfaccia utente anziché utilizzare un collegamento alla guida. Tuttavia, è possibile usare un collegamento alla guida per fornire informazioni aggiuntive.

    **Non corretto:**

    ![screenshot del collegamento a che cos'è una password complessa? ](images/winenv-help-image14.png)

    **Corretto:**

    ![screenshot del testo supplementare sulle password ](images/winenv-help-image15.png)

    **Migliore:**

    ![screenshot del testo con collegamento ad altre informazioni ](images/winenv-help-image16.png)

    Nell'esempio corretto le informazioni della guida vengono riepilogate concisamente, migliorando significativamente la probabilità che gli utenti lo leggano. Nell'esempio migliore viene fornito un collegamento alla guida per ulteriori informazioni su questo argomento complesso.

-   Frase Guida collegamenti per indicare chiaramente l'assistenza. I collegamenti della guida non devono mai essere letti come collegamenti di azione.
-   Usare l'intero collegamento alla guida per il testo del collegamento, non solo le parole chiave.

    **Corretto:**

    Quali sono i rischi per consentire le eccezioni?

    **Non corretto:**

    Quali sono i rischi per consentire le eccezioni?

    Nell'esempio corretto viene utilizzata l'intera frase del collegamento alla guida per il testo del collegamento.

    -   **Eccezione:** I collegamenti alla guida a siti Web esterni dovrebbero semplicemente utilizzare il nome del sito o della pagina come collegamento. Il testo che introduce il nome del sito non deve essere incluso nel collegamento.

-   I collegamenti alla guida non devono corrispondere esattamente alle intestazioni degli argomenti della guida, ma è necessario disporre di una connessione forte e ovvia tra i due. Progettare collegamenti e intestazioni in coppie per questo motivo.

    **Corretto:**

    Come è possibile migliorare le prestazioni di questa funzionalità? (testo del collegamento)

    Configurazione di questa funzionalità per ottenere prestazioni ottimali (intestazione dell'argomento)

    **Non corretto:**

    Come è possibile migliorare le prestazioni di questa funzionalità? (testo del collegamento)

    Panoramica completa di questa funzionalità (intestazione dell'argomento)

    Nell'esempio errato, l'intestazione dell'argomento della guida differisce sostanzialmente nell'ambito dal testo del collegamento della guida e potrebbe essere disorientata.

-   Se il contenuto della guida è online, renderlo chiaro nel testo del collegamento. Questa operazione consente di rendere prevedibili i risultati dei collegamenti.

    **Corretto:**

    Per ulteriori formati e strumenti, visitare il sito Web Microsoft.

    **Non corretto:**

    Dove è possibile trovare altri formati e strumenti?

-   Utilizzare frasi complete.
-   Non usare la punteggiatura finale, ad eccezione dei punti interrogativi.
-   Non usare ellissi per i collegamenti o i comandi della guida.

**Contenuto della Guida**

-   Formattare gli elementi dell'interfaccia utente usando Bold per facilitarne l'identificazione. Questa operazione è particolarmente utile per gli argomenti della guida procedurale, consentendo agli utenti di analizzare le procedure e visualizzare rapidamente gli elementi dell'interfaccia utente pertinenti.
-   Formattare le didascalie con corsivo. Questo vale per le tabelle, l'arte, le schermate e altri elementi grafici che traggono vantaggio dalla breve spiegazione testuale.
-   Per informazioni, vedere la guida. In genere, non usare la frase Guida in linea a meno che non si faccia riferimento al contenuto del sito Web.

 

