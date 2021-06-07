---
title: Help
description: Usare la Guida come meccanismo secondario per consentire agli utenti di completare e comprendere meglio le attività \ 8212; il meccanismo principale è l'interfaccia utente stessa. Applicare queste linee guida per rendere il contenuto davvero utile e facile da trovare.
ms.assetid: 82ce076e-062b-4793-a1c0-ed96c0f2b284
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f9b1260128eb253a2d501a810923ae809c5f8187
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443246"
---
# <a name="help"></a>Help

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Usare la Guida come meccanismo secondario per consentire agli utenti di completare e comprendere meglio le attività che il meccanismo principale è l'interfaccia utente stessa. Applicare queste linee guida per rendere il contenuto davvero utile e facile da trovare.

Un sistema della Guida è costituito da vari tipi di contenuto progettati per assistere gli utenti quando non sono in grado di completare un'attività, vogliono comprendere un concetto in modo più dettagliato o hanno bisogno di dettagli più tecnici di quelli disponibili nell'interfaccia utente.

In questo articolo si fa riferimento alla Guida come secondaria all'interfaccia utente. L'interfaccia utente è primaria perché è qui che gli utenti tentano prima di risolvere i problemi. Consultano il sistema della Guida solo se non possono eseguire l'attività con l'interfaccia utente.

![Screenshot della pagina Guida e supporto tecnico di Windows ](images/winenv-help-image1.png)

Guida e supporto tecnico home page Windows, disponibile nell'menu Start.

**Nota:** Le linee guida [relative allo stile e al tono](text-style-tone.md) sono presentate in un articolo separato.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, prendi in considerazione queste domande:

-   **Quanto sono motivati gli utenti di destinazione?** Più sono altamente motivati a individuare le funzionalità del programma e a diventare utenti intermedi o persino avanzati, più saranno disposti a ricercare le risposte alle proprie domande consultando gli argomenti della Guida.
-   **Si sta usando la Guida per correggere un'interfaccia utente non erta?** Maggiore è la qualità dell'interfaccia utente, minore sarà la ricerca di assistenza aggiuntiva da parte degli utenti. Se il programma ha un'interfaccia utente primaria molto chiara e utile (ad esempio messaggi di errore senza gergo, procedure guidate ben scritte e finestre di dialogo non ambigue), potrebbe non essere necessario un sistema di Guida secondario.
-   **Il programma è relativamente semplice?** In tal caso, è consigliabile incorporare tutto il contenuto di assistenza necessario nelle superfici principali dell'interfaccia utente. È più probabile che gli utenti cerchino assistenza aggiuntiva nei programmi che eseguono attività complesse.
-   **L'applicazione è destinata a sviluppatori, professionisti IT o altri esperti di software?** Questi utenti tendono ad aspettarsi la Guida di riferimento per le convenzioni del linguaggio di programmazione e una Guida concettuale approfondita per la conoscenza delle funzionalità.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Se si decide di includere la Guida nel programma, integrarla nella progettazione complessiva. L'interfaccia della Guida deve essere semplice, efficiente e pertinente. dovrebbe consentire agli utenti di ottenere facilmente assistenza e quindi tornare all'attività. Si pensi al sistema della Guida in termini di tempo degli utenti: ridurre al minimo l'interruzione anticipando prima dove si verificano problemi nel programma, quindi risolvendo questi problemi incorporando l'assistenza fondamentale direttamente nell'interfaccia utente e creando punti di ingresso chiari e coerenti nella Guida più dettagliata.

L'assistenza di Windows è stata progettata in base a questi principi. Ecco alcune delle modifiche di progettazione apportate all'esperienza utente della Guida di Windows:

-   Punti di ingresso più individuabili alla Guida dall'interfaccia utente primaria (in particolare nuovi collegamenti alla Guida da superfici dell'interfaccia utente, ad esempio finestre di dialogo, messaggi di errore e procedure guidate). I collegamenti alla Guida consentono di accedere direttamente all'argomento pertinente nella Guida.
-   L'icona del pulsante Guida è disponibile nell'angolo superiore destro della maggior parte delle pagine dell Pannello di controllo hub e delle cartelle della shell.
-   Gli utenti possono scegliere di ottenere il contenuto della Guida più aggiornato da Guida online e supporto tecnico di Windows quando sono online.
-   Gli argomenti della Guida sono ora basati sulle attività anziché sulle funzionalità, in modo che gli utenti possano eseguire le proprie attività in modo rapido ed efficiente.
-   Gli argomenti della Guida sono ora in gran parte basati su scenari utente principali noti.
-   Gli argomenti della Guida hanno un tono [più](text-style-tone.md)rilassato e informale, usando il linguaggio reale.
-   Gli argomenti della Guida sono progettati per un'analisi efficace, in quanto gli utenti leggono raramente il contenuto parola per parola.

### <a name="an-analogy-for-help"></a>Analogia per la Guida

Per esaminare in modo più approfondito la progettazione del sistema della Guida, prendere in considerazione un'analogia con la vita quotidiana. Si è persi in una città sconosciuta. Come si deve procedere? Molti reagiranno in questo modo:

-   Orientarsi; cercare punti di riferimento, simboli stradali (nomi e puntatori ai luoghi).
-   Cercare le mappe.
-   Infine, come ultima risorsa, chiedere indicazioni stradali o chiamare un amico.

La progettazione dell'"interfaccia" della città influisce sulla necessità di assistenza. Strade ben etichettate, indicazioni esplicite (puntatori ad ospedali, aeroporti, aeroporti e uffici postali) e luoghi di interesse chiari come caratteristiche geografiche o edifici importanti consentono di trovare la strada.

Si chiede aiuto come ultima risorsa. È un'indicazione che l'"interfaccia" della città ha avuto esito negativo perché non è stata progettata correttamente e confonde. È più probabile che si chieda aiuto in una posizione con un'etichetta specifica che suggerisce utilità. Ad esempio, è più probabile che si chieda aiuto in un luogo con etichetta "Indicazioni stradali" o "Informazioni" rispetto a un luogo generale come il Municipio, anche se chiunque al Municipio potrebbe fornire indicazioni stradali.

Quando si chiede aiuto, è probabile che si sia frustrati e si voglia semplicemente raggiungere la destinazione desiderata. Probabilmente non si è in vena di dedicare del tempo a visitare la città o a conoscere la sua storia. Inoltre, la motivazione dipende dall'importanza dell'attività. Se si sta tentando di trovare la camera d'hotel, si farà tutto il necessario. Tuttavia, se l'obiettivo è quello di trovare un luogo di importanza minore, molto probabilmente ci si arrendo solo dopo un impegno modesto.

Tutti questi aspetti della ricerca nello spazio reale corrispondono al modo in cui gli utenti in genere si trovano nello spazio virtuale del programma. La ricerca di aiuto oltre l'interfaccia utente primaria è per sua natura disorientante; fare del proprio meglio per mitigare tale esperienza grazie all'interfaccia utente ben progettata e ai "segnali stradali" intelligenti per indirizzare gli utenti alle risposte necessarie.

### <a name="designing-ui-so-that-help-is-unnecessary"></a>Progettazione dell'interfaccia utente in modo che la Guida non sia necessaria

Provare innanzitutto a rendere superflua la Guida, effettuando le operazioni seguenti:

-   Semplifica l'individuazione e l'esecuzione di attività comuni.
-   Fornire istruzioni [principali chiare.](text-ui.md)
-   Fornire etichette di controllo chiare e concise orientate agli obiettivi e alle attività.
-   Fornire istruzioni e spiegazioni supplementari, se necessario.
-   Anticipare i problemi evitabili usando controlli vincolati a scelte valide, fornendo valori predefiniti appropriati, gestendo tutti i formati di input ed evitando errori.
-   Scrittura di messaggi di errore che forniscono una soluzione o un'azione chiara da intraprendere per l'utente.
-   Evitare di confondere le progettazioni dell'interfaccia utente, ad esempio le attività con un flusso scadente o l'uso di controlli disabilitati senza alcun motivo apparente.
-   Uso di writer ed editor all'inizio del ciclo di sviluppo per creare testo dell'interfaccia utente di alta qualità e [coerente](text-ui.md) in tutto il programma.

Gli utenti non devono andare altrove per capire come usare l'interfaccia utente. Aggiungere informazioni essenziali direttamente nell'interfaccia utente principale, invece di forzare gli utenti dal contesto immediato e nel riquadro Guida. Se le informazioni importanti sono presenti solo in un argomento della Guida, è probabile che gli utenti non le vedano. Per informazioni facoltative e più dettagliate, usare i collegamenti della Guida dall'interfaccia utente principale all'argomento della Guida pertinente per assistenza supplementare.

### <a name="considering-user-motivation"></a>Considerare la motivazione dell'utente

Per la maggior parte degli utenti, velocità ed efficienza sono tra le virtù fondamentali dei buoni programmi. Gli utenti vogliono eseguire il proprio lavoro. In genere, non sono interessati a conoscere il programma e la tecnologia per proprio conto; la loro attenzione si estende solo nella misura in cui il programma serve i propri interessi e risolve i problemi a portata di mano.

Progettare il sistema della Guida in base alle motivazioni degli utenti. Si consideri, ad esempio, un utente che si è insediato in un chiosco multimediale in un locale. Se non riesce a capire come eseguire rapidamente l'attività, è probabile che si sia arresa e se ne andrà. È improbabile che passi del tempo usando la Guida. In alternativa, un utente altamente motivato ha una tolleranza più elevata per il tempo dedicato alla ricerca di risposte nel sistema della Guida. Un utente aziendale che deve bilanciare i libri, ad esempio, è probabilmente disposto a consultare il contenuto della Guida per ottenere il massimo da questa nuova applicazione di contabilità.

### <a name="writing-content-for-scanning"></a>Scrittura di contenuto per l'analisi

Scrivere argomenti della Guida sapendo che verranno analizzati per ottenere informazioni specifiche, non leggere parola per parola. Scrivere concisamente, arrivare rapidamente al punto e fornire informazioni su cui gli utenti possono agire.

-   Scrivere argomenti relativi alle procedure usando passaggi numerati in un formato coerente in modo che gli utenti riconoscano di ricevere assistenza procedurale.
-   Scrivere argomenti di riferimento con facilità di analisi, usando tabelle, ad esempio, per presentare le opzioni dell'interfaccia utente o la sintassi del linguaggio.
-   Scrivere argomenti concettuali organizzati logicamente in base ai sottotitoli, in modo che l'utente possa ignorare intere sezioni di minore interesse.

In tutto il contenuto della Guida è più semplice analizzare gli elenchi puntati rispetto ai blocchi di paragrafo standard di testo. usare gli elenchi puntati in modo giudizioso, tuttavia, non come stampella per materiale nonorganizzato.

### <a name="creating-content-that-matters"></a>Creazione di contenuto importante

Dato che nessun sistema di Guida può prevedere ogni domanda che ogni utente potrebbe avere, concentrarsi sulla maggior parte del contenuto per rispondere alle domande principali negli scenari principali per gli utenti di destinazione. Ad esempio, una ricerca efficace e come stabilire la connettività di rete (tra le altre attività) possono essere argomenti molto ricercati. Concentrarsi anche sulle attività all'interno degli scenari utente principali, anziché documentare una funzionalità o una tecnologia in modo esaustivo per proprio conto.

**Suggerimento:** Il supporto tecnico è una buona fonte per il contenuto della Guida. Gli help desk spesso tengono traccia delle domande frequenti su particolari programmi o attività che gli utenti tentano (e non riescono) a eseguire.

Non è necessario fornire assistenza per ogni funzionalità dell'interfaccia utente. **Spesso, la Guida non è utile quando si prova a creare la Guida per tutti gli elementi.** Se l'interfaccia utente è ben progettata, la maggior parte di questi argomenti della Guida non sarà molto utile; si rietieni semplicemente l'ovvio.

Se esiste più di un modo per eseguire un'attività, nella maggior parte dei casi è sufficiente documentare il modo più comune usato dagli utenti meno esperti. Le eccezioni includono considerazioni sull'accessibilità (che documenta gli equivalenti della tastiera delle azioni del mouse, ad esempio) e considerazioni sulla piattaforma ,ad esempio per il fattore di forma del tablet o per gli ambienti server in cui la riga di comando può sostituire l'interfaccia utente grafica.

Tenere presente che gli utenti spesso non pensano ai problemi che si verificano esattamente con gli stessi termini che si verificano. Ad esempio, gli utenti possono trovare strano pensare a se stessi come a un "account". Assicurarsi di progettare la funzionalità di ricerca e indicizzazione, quindi, in modo da verificare le probabili variazioni di terminologia e sinonimi.

Tra l'interfaccia utente principale e il sistema della Guida, tuttavia, i termini devono essere molto simili se non identici. Gli utenti possono essere confusi quando la lingua del sistema della Guida non è strettamente correlata a ciò che vedono sullo schermo.

### <a name="writing-compelling-help-link-text"></a>Scrittura di testo accattivante del collegamento alla Guida

Quando si collega a un argomento della Guida dall'interfaccia utente principale, assicurarsi di scrivere testo accattivante per il collegamento alla Guida. Un linguaggio chiaro e specifico ispira fiducia. Gli utenti tendono a ritiene che i collegamenti generici della Guida (un pulsante con la parola "Guida" o "Altre informazioni") non condurranno alle informazioni giuste senza un investimento significativo di tempo.

**Se si eservino solo cinque operazioni...**

1.  Progettare l'interfaccia utente in modo che gli utenti non necessitino della Guida.
2.  Rendere la Guida utile concentrando il contenuto sulle domande principali negli scenari principali per gli utenti di destinazione.
3.  Presentare il contenuto della Guida in modo che sia facile da analizzare.
4.  Comprendere che non è necessario fornire assistenza per ogni funzionalità nell'interfaccia utente.
5.  Rendere i punti di ingresso della Guida individuabili e accattivanti.

## <a name="usage-patterns"></a>Modelli di utilizzo

Diversi tipi di contenuto hanno scopi diversi.



|    Tipo di contenuto                                                                                                        |   Esempio                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guida procedurale**<br/> illustra i passaggi per l'esecuzione di un'attività. <br/>                       | La Guida procedurale deve concentrarsi sulle informazioni "come" anziché su "cosa" o "perché". <br/> ![Screenshot della pagina della Guida "Elimina file temporanei" ](images/winenv-help-image2.png)<br/> In questo esempio, l'argomento della Guida descrive come usare una funzionalità dell'utilità Pulizia disco, illustrando i passaggi da seguire in sequenza.<br/>                                              |
| **Guida concettuale**<br/> fornisce informazioni di base, panoramiche sulle funzionalità o processi. <br/> | La Guida concettuale deve fornire informazioni "cosa" o "perché" oltre a quella necessaria per completare un'attività. <br/> ![Screenshot della pagina della Guida "Desktop (panoramica)" ](images/winenv-help-image3.png)<br/> In questo esempio, l'argomento della Guida definisce che cos'è il desktop e fornisce dettagli aggiuntivi su ciò che contiene e sul motivo per cui gli utenti interagiscono con esso.<br/>           |
| **Guida di riferimento**<br/> funge da libro di riferimento online. <br/>                                | È possibile usare la Guida di riferimento per documentare un linguaggio di programmazione o interfacce di programmazione. <br/> ![Screenshot della pagina della Guida "Convenzioni di notazione" ](images/winenv-help-image4.png)<br/> In questo esempio l'argomento della Guida elenca le convenzioni tipografiche in uso per questa lingua o applicazione specifica, fornendo le informazioni in una tabella di facile analisi.<br/> |



 

## <a name="guidelines"></a>Indicazioni

### <a name="entry-points"></a>Punti di ingresso

-   **Collegamento ad argomenti specifici della Guida pertinenti.** Non collegarsi alla guida home page, al sommario, a un elenco di risultati della ricerca o a una pagina che si collega solo ad altre pagine. Evitare il collegamento a pagine strutturate come un ampio elenco di domande frequenti, perché impone agli utenti di cercare quella che corrisponde al collegamento su cui hanno fatto clic. Non collegare argomenti della Guida specifici che non sono rilevanti e utili per l'attività a portata di mano. Non collegarsi mai a pagine vuote.
-   **Non inserire collegamenti alla Guida in ogni finestra o pagina per motivi di coerenza.** Fornire un collegamento alla Guida in un'unica posizione non significa che è necessario fornirli ovunque.
-   **Usare i collegamenti della Guida per finestre di dialogo, messaggi di errore, procedure guidate e finestre delle proprietà.** Se il collegamento Guida si applica a controlli specifici, posizionarlo sotto di essi, allineato a sinistra. Se il collegamento Guida si applica all'intera finestra, posizionarlo nell'angolo inferiore sinistro dell'area del contenuto della finestra.

    ![Screenshot della finestra delle proprietà con la casella di gruppo ](images/winenv-help-image5.png)

    In questo esempio il secondo collegamento alla Guida si applica a un gruppo di controlli.

    ![Screenshot della finestra delle proprietà e del collegamento alla Guida ](images/winenv-help-image6.png)

    In questo esempio il collegamento Guida si applica all'intera finestra.

-   **Usare i collegamenti della Guida invece di riferimenti testuali generici alla Guida ogni volta che è possibile dal punto di vista tecnico.**

    **Corretto:**

    Come è possibile correggere gli errori del disco?

    **Non corretto:**

    Per altre informazioni sul ripristino degli errori del disco, vedere Guida e supporto tecnico.

-   **Usare un pulsante ? con l'icona Guida per le pagine hub degli elementi del Pannello di controllo.** Posizionarlo nell'angolo superiore destro. Questi pulsanti non hanno un'etichetta, ma hanno una descrizione comando che legge la Guida.

    ![Screenshot dell'elemento del Pannello di controllo con il pulsante ? ](images/winenv-help-image7.png)

    Elemento del pannello di controllo con un pulsante ?

-   **F1 Help è facoltativo.** Gli utenti si sono abituati a trovare informazioni della Guida correlate al contesto immediato dell'interfaccia utente sullo schermo premendo F1, che è etichettato come Guida nelle tastiere standard. È possibile includere la Guida F1 se, ad esempio, gli studi sull'usabilità mostrano che gli utenti prevedono di trovarla o se l'interfaccia utente del programma è sufficientemente complessa da trarre vantaggio dall'assistenza contestuale.
-   **I programmi con barre dei menu possono avere una categoria di menu ?** Per le linee guida per i menu della Guida, [vedere Menu](cmd-menus.md).

    ![Screenshot della Guida a cui si accede dalla barra dei menu ](images/winenv-help-image8.png)

    In questo esempio l'accessorio Windows Paint ha una categoria di menu Guida.

-   **Per l'accessibilità tramite tastiera, specificare le tabulazioni per i pulsanti e i collegamenti della Guida.**
-   Il pulsante Guida e il comportamento del collegamento devono essere i seguenti: viene aperto il riquadro Guida e viene visualizzato un argomento della Guida dedicato. L'interfaccia utente che ha richiamato il riquadro Guida deve rimanere aperta per mantenere l'esperienza contestuale.
-   **Non usare i seguenti stili obsoleti del punto di ingresso della Guida: "Altre informazioni" o "Altre informazioni su..." collegamenti, pulsanti della Guida generici e pulsanti della Guida sensibile al contesto sulla barra del titolo.** Anche se sono stati usati in passato, gli studi sull'usabilità hanno determinato che gli utenti tendono a ignorarli. Usare invece i collegamenti ad argomenti specifici della Guida. Per le linee guida sulla scrittura di collegamenti alla Guida, vedere [Collegamenti alla Guida](#text).

    **Non corretto:**

    ![Screenshot della finestra di dialogo con un collegamento "Altre informazioni" ](images/winenv-help-image9.png)

    Non usare "Altre informazioni" o "Altre informazioni su..." Link.

    **Non corretto:**

    ![Screenshot del pulsante della Guida accanto ai pulsanti di commit ](images/winenv-help-image10.png)

    Non usare pulsanti della Guida generici.

    **Non corretto:**

    ![Screenshot dell'icona del punto interrogativo sulla barra del titolo ](images/winenv-help-image11.png)

    Non usare i pulsanti della Guida sensibile al contesto sulla barra del titolo.

### <a name="content"></a>Content

-   **Non creare contenuto ovvio.** Gli argomenti della Guida che ripetono ciò che si trova nell'interfaccia utente primaria non aggiungono valore.
-   **Non creare contenuto su cui l'utente non può agire in qualche modo.**
    -   **Eccezione:** Alcuni contenuti concettuali forniscono informazioni di base importanti senza necessariamente condurre all'azione dell'utente.
-   **Evitare soluzioni vaghe ai problemi.** Ad esempio, "contattare l'amministratore di sistema" o "reinstallare l'applicazione" tende a frustrare gli utenti.
    -   **Eccezione:** È consigliabile contattare l'amministratore di sistema se questa è l'unica soluzione pratica e gli amministratori di sistema prevedono di essere contattati per il problema.
-   **Evitare il contenuto che risolve scenari utente altamente improbabili.** Sviluppare il contenuto principale della Guida per quello che si prevede sarà l'utilizzo normale; Tenere presente le eccezioni importanti all'utilizzo previsto, ma considerare questo contenuto come una priorità più bassa.
-   **Raccogliere commenti e suggerimenti dagli utenti su quanto sono utili gli argomenti della Guida.** Consente agli utenti di valutare singoli argomenti. Eseguire [studi di usabilità](glossary.md) sulla documentazione per verificare i problemi relativi alla qualità e all'individuabilità del contenuto.
    -   **Suggerimento:** Il feedback degli utenti è anche un ottimo modo per generare più contenuto basato su attività, incentrato sulle operazioni effettivamente in corso con il programma, anziché sui contenuti basati sulle funzionalità, incentrati semplicemente su una descrizione della tecnologia.
-   **Fornire più modi per accedere al contenuto.** Un sommario, un indice e un meccanismo [di](ctrl-search-boxes.md) ricerca sono tre dei metodi più comuni per migliorare l'individuabilità.
-   **Se esiste più di un modo per eseguire un'attività, nella maggior parte dei casi è sufficiente documentare il modo più comune usato dagli utenti meno esperti.**

### <a name="icons"></a>Icone

-   Usare l'icona Guida solo per le finestre di Esplora risorse e le pagine hub degli elementi del Pannello di controllo. Non usare l'icona Guida con i collegamenti della Guida.

**Corretto:**

![Screenshot della finestra con l'icona del punto interrogativo ](images/winenv-help-image12.png)

In questo esempio, una finestra Esplora risorse usa un'icona della Guida per fornire l'accesso alla Guida.

**Non corretto:**

![Screenshot della finestra con l'icona della Guida nel pannello sinistro ](images/winenv-help-image13.png)

In questo esempio l'icona Guida in basso a sinistra viene usata in modo non corretto con un collegamento alla Guida.

## <a name="text"></a>Testo

**Collegamenti alla Guida**

-   Fornire informazioni specifiche sul contenuto dell'argomento della Guida, usando il testo pertinente e conciso necessario. Gli utenti spesso ignorano i collegamenti generici della Guida. Assicurarsi che i risultati del collegamento siano prevedibili. Gli utenti non devono essere sorprese dai risultati.

    -   **Eccezione:** È possibile usare "Altre informazioni" per integrare le istruzioni direttamente nell'interfaccia utente, soprattutto se fornire informazioni specifiche nel collegamento alla Guida comporta una ripetizione non necessaria o rende il collegamento meno interessante.

    **Non corretto:**

    Una password complessa include almeno sei lettere maiuscole e minuscole miste, numeri e simboli. Che cos'è una password complessa?

    **Corretto:**

    Una password complessa include almeno sei lettere maiuscole e minuscole miste, numeri e simboli. Altre informazioni

    Nell'esempio non corretto, il collegamento della Guida è ripetitivo. Pone una domanda a cui è già già stata data una risposta.

-   Quando possibile, il testo del collegamento alla Guida per frasi in termini di domanda principale risponde dal contenuto della Guida. Non usare la formulazione "Altre informazioni su", "Altre informazioni" o "Ottenere assistenza per questo".

    **Non corretto:**

    Altre informazioni sull'aggiunta di eccezioni

    **Corretto:**

    Quali sono i rischi di consentire le eccezioni?

    Ricerca per categorie aggiungere eccezioni?

    Negli esempi corretti, il collegamento viene formulato in termini di domanda principale a cui risponde l'argomento della Guida.

-   Se le informazioni più rilevanti possono essere riepilogate in modo sintetico, inserire il riepilogo direttamente nell'interfaccia utente anziché usare un collegamento alla Guida. Tuttavia, è possibile usare un collegamento alla Guida per fornire informazioni supplementari.

    **Non corretto:**

    ![Screenshot del collegamento a che cos'è una password complessa? ](images/winenv-help-image14.png)

    **Corretto:**

    ![Screenshot del testo supplementare sulle password ](images/winenv-help-image15.png)

    **Migliore:**

    ![Screenshot di testo con collegamento a altre informazioni ](images/winenv-help-image16.png)

    L'esempio corretto riepiloga le informazioni della Guida in modo sintetico, migliorando notevolmente la probabilità che gli utenti le le leggono. L'esempio migliore fornisce un collegamento alla Guida per altre informazioni su questo argomento complesso.

-   Collegamenti alla Guida per frasi per indicare chiaramente l'assistenza. I collegamenti della Guida non devono mai essere letti come collegamenti di azione.
-   Usare l'intero collegamento alla Guida per il testo del collegamento, non solo le parole chiave.

    **Corretto:**

    Quali sono i rischi di consentire le eccezioni?

    **Non corretto:**

    Quali sono i rischi di consentire le eccezioni?

    Nell'esempio corretto viene usata l'intera frase di collegamento della Guida per il testo del collegamento.

    -   **Eccezione:** I collegamenti della Guida a siti Web esterni devono usare semplicemente il nome del sito o della pagina come collegamento. Qualsiasi testo che introduce il nome del sito non deve essere incluso nel collegamento stesso.

-   I collegamenti della Guida non devono corrispondere esattamente alle intestazioni degli argomenti della Guida, ma tra i due deve essere presente una connessione forte e ovvia. Progettare collegamenti e intestazioni in coppie per questo motivo.

    **Corretto:**

    Come è possibile migliorare le prestazioni di questa funzionalità? (testo del collegamento)

    Configurazione di questa funzionalità per prestazioni ottimali (intestazione dell'argomento)

    **Non corretto:**

    Come è possibile migliorare le prestazioni di questa funzionalità? (testo del collegamento)

    Panoramica completa di questa funzionalità (intestazione dell'argomento)

    Nell'esempio non corretto, l'intestazione dell'argomento della Guida differisce sostanzialmente nell'ambito dal testo del collegamento alla Guida e potrebbe essere disorientante.

-   Se il contenuto della Guida è online, renderlo chiaro nel testo del collegamento. Questa operazione consente di rendere prevedibile il risultato dei collegamenti.

    **Corretto:**

    Per altri formati e strumenti, visitare il sito Web Microsoft.

    **Non corretto:**

    Dove è possibile trovare altri formati e strumenti?

-   Usare frasi complete.
-   Non usare la punteggiatura finale, ad eccezione dei punti interrogativi.
-   Non usare i puntini di sospensione per i collegamenti o i comandi della Guida.

**Contenuto della Guida**

-   Formattare gli elementi dell'interfaccia utente usando il grassetto per semplificare l'identificazione. Ciò è particolarmente utile per gli argomenti della Guida procedurali, consentendo agli utenti di analizzare le procedure e visualizzare rapidamente gli elementi dell'interfaccia utente pertinenti.
-   Formattare i sottotitoli usando il corsivo. Questo vale per tabelle, immagini, screenshot e altri elementi grafici che traggono vantaggio da brevi spiegazioni testuali.
-   Fare riferimento alla Guida semplicemente come Guida. In genere, non usare la frase Guida online a meno che non si fa di fatto riferimento al contenuto del sito Web.

 

