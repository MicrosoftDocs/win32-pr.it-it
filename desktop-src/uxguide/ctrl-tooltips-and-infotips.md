---
title: Descrizioni comando e descrizioni comandi
description: Una descrizione comando è una piccola finestra popup che etichetta il controllo senza etichetta a cui punta, ad esempio i controlli della barra degli strumenti senza etichetta o i pulsanti di comando.
ms.assetid: 80979281-eefb-485a-b42f-7f9e05665357
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8911c5a008d2de6cec2bd564fd786a23c670d633
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524535"
---
# <a name="tooltips-and-infotips"></a>Descrizioni comando e descrizioni comandi

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Una descrizione comando è una piccola finestra popup che etichetta il controllo senza etichetta a cui punta, ad esempio i controlli della barra degli strumenti senza etichetta o i pulsanti di comando.

![Screenshot che mostra il pulsante di stampa con la descrizione comando "Stampa (CTRL+P)" visualizzata.](images/ctrl-tooltips-and-infotips-image1.png)

Descrizione comando tipica per un pulsante della barra degli strumenti.

Poiché le descrizioni comando sono state rivelate così utili, esiste un controllo correlato denominato descrizioni comandi, che fornisce un testo più descrittivo di quello possibile con le descrizioni comando.

Una descrizione comando è una piccola finestra popup che descrive in modo conciso l'oggetto a cui punta, ad esempio descrizioni di controlli della barra degli strumenti, icone, grafica, collegamenti, oggetti Esplora risorse, elementi menu Start e pulsanti della barra delle applicazioni. Le descrizioni comandi sono una forma [di](ctrl-progressive-disclosure-controls.md)controlli di divulgazione progressiva, eliminando la necessità di avere sempre un testo descrittivo sullo schermo.

![Screenshot del pulsante Condividi con la descrizione comandi ](images/ctrl-tooltips-and-infotips-image2.png)

Una tipica descrizione comandi.

Ai fini di questo articolo, le descrizioni comando e le descrizioni comandi sono denominate collettivamente suggerimenti.

I suggerimenti consentono agli utenti di comprendere gli oggetti sconosciuti o non noti che non sono descritti direttamente nell'interfaccia utente. Vengono visualizzate automaticamente quando gli utenti passano il puntatore del mouse su un oggetto e vengono rimosse quando gli utenti fanno clic sul controllo o spostano il mouse o quando si verifica il timeout della mancia.

**Sviluppatori:** Non è disponibile alcun controllo della descrizione comandi. Le descrizioni comandi vengono implementate con il controllo della descrizione comando. La distinzione è nell'utilizzo, non nell'implementazione.

> [!Note]  
> Le linee guida relative [a balloon,](ctrl-balloons.md) [barre degli strumenti](cmd-toolbars.md)e [Guida](winenv-help.md) sono presentate in articoli separati.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Le informazioni vengono visualizzate in base al passaggio del puntatore?** Se non è così, usa un altro controllo. Visualizzare i suggerimenti solo come risultato dell'interazione dell'utente. Al contrario, [i balloon possono](ctrl-balloons.md) essere visualizzati in modo proprio (come con le notifiche), in modo da avere una coda che identifica l'origine.
-   **Un controllo ha un'etichetta di testo?** Se non ne ha una, usa una descrizione comando per fornire l'etichetta. Si noti che la maggior parte dei controlli deve essere etichettata e pertanto non deve contenere descrizioni comando. I controlli della barra degli strumenti e i pulsanti di comando con etichette grafiche devono contenere descrizioni comando.
-   **Un oggetto trae vantaggio da una descrizione supplementare o da altre informazioni?** In tal caso, usare una descrizione comandi. Tuttavia, il testo deve essere supplementare, non essenziale per le attività principali. Se è essenziale, inseriscilo direttamente nell'interfaccia utente, in modo che gli utenti non debbano trovarlo o andare alla ricerca di informazioni.
-   **Le informazioni supplementari sono un errore, un avviso o uno stato?** In tal caso, usare un altro elemento dell'interfaccia utente, ad esempio un fumetto, [un messaggio di errore](mess-error.md)o una barra di [stato.](ctrl-status-bars.md) Le descrizioni comandi dell'icona dell'area di notifica sono un'eccezione perché possono essere usate per visualizzare informazioni sullo stato.
-   **Gli utenti devono interagire con la descrizione comando?** In tal caso, usare un altro controllo, ad esempio un balloon. Gli utenti non possono interagire con le descrizioni comandi perché spostando il mouse spariscono.
-   **Gli utenti devono stampare le informazioni supplementari?** In tal caso, usare un altro controllo, ad esempio un campo di commento statico. Tuttavia, è anche possibile usare le descrizioni comandi per fornire un accesso più diretto a queste informazioni.

    ![Screenshot del balloon dei commenti ](images/ctrl-tooltips-and-infotips-image3.png)

    In questo esempio, un campo di commento statico in Microsoft Word consente agli utenti di stampare commenti.

-   **Il contesto è tale che gli utenti potrebbero trovare i suggerimenti fastidiosi o fonte di distrazione?** In tal caso, è consigliabile usare un'altra soluzione, inclusa l'operazione non eseguire alcuna operazione. Se si usano suggerimenti in tali contesti, consentire agli utenti di disattivarli.

Se usati in modo appropriato, i suggerimenti migliorano la comunicazione con l'utente. **Non usare mai i suggerimenti come sostituzione per una buona progettazione.** Se un elemento grafico, un pulsante o un altro oggetto richiede che gli utenti continuino a controllare un suggerimento per comprenderlo, la progettazione è negativa. Correggere invece la progettazione.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

I suggerimenti sono un modo efficace per semplificare un'interfaccia utente. Forniscono agli utenti le informazioni necessarie quando ne hanno bisogno, con il minimo sforzo da parte degli utenti. I suggerimenti consentono di usare lo spazio sullo schermo in modo più efficace e di ridurre il disordine dello schermo. Tuttavia, le mance progettate in modo non efficace possono essere fastidiose, distrazioni, inutili, opprimenti o instradanti. I concetti di progettazione seguenti illustrano la differenza.

### <a name="discoverability"></a>Individuabilità

I suggerimenti vengono visualizzati automaticamente quando gli utenti passano il puntatore del mouse su un oggetto per un periodo di tempo. Questo meccanismo di ritardo di tempo rende i suggerimenti molto pratici, ma ne riduce anche l'individuabilità.

Nel corso del tempo, gli utenti apprendono che alcuni oggetti standard come i pulsanti della barra degli strumenti, i pulsanti grafici, gli elementi menu Start e le icone dell'area di notifica hanno suggerimenti, in modo da poter dare per scontata l'individuabilità.

L'individuazione dei suggerimenti in posizioni non standard richiede più tempo per gli utenti. Non esiste alcuna indicazione visiva, ad esempio un'area sensibile o una modifica del puntatore, che indica che un oggetto ha una mancia. Ancora peggiore, alcuni utenti spostano molto il mouse, soprattutto quando imparano a spostarsi nell'interfaccia utente. Gli utenti devono sapere che un oggetto ha una mancia, tramite esperienza passata o tramite sperimentazione.

È possibile migliorare l'individuabilità usando i suggerimenti in modo coerente, che a sua volta favorisce la prevedibilità. Se si forniscono suggerimenti per alcuni oggetti, è consigliabile fornirli per tutti gli oggetti simili per i quali è probabile che gli utenti desiderino informazioni supplementari. A volte questa operazione può risultare complessa, perché è necessario assicurarsi anche che i suggerimenti siano utili e non ovvi.

Se fornire suggerimenti individuabili e costantemente utili si rivela un problema, prendere in considerazione progettazioni alternative, ad esempio etichette di controllo auto-esplicativi o testo supplementare sul posto.

### <a name="appropriate-information"></a>Informazioni appropriate

Le informazioni appropriate per i suggerimenti hanno le caratteristiche seguenti:

-   **Conciso.** Le finestre popup usate dai suggerimenti sono ideali per frasi brevi e frammenti di frasi, nonché per testo formattato. Blocchi di testo grandi e non formattati sono difficili da leggere e opprimente.
-   **Disponibile.** Il testo del suggerimento deve essere informativo. Non dovrebbe essere ovvio o semplicemente ripetere ciò che è già presente sullo schermo.
-   **Supplementare.** Poiché il testo della mancia non è sempre visibile, devono essere informazioni supplementari che gli utenti non devono leggere. Le informazioni importanti devono essere comunicate usando etichette di controllo auto-esplicativo o testo supplementare sul posto.
-   **Statico.** Gli utenti non si aspettano che i suggerimenti cambino da un'istanza all'altra, quindi è improbabile che si notino modifiche nel contenuto dinamico, ad esempio le informazioni sullo stato. I suggerimenti per le icone dell'area di notifica sono un'eccezione importante: è più probabile che gli utenti rilevino modifiche nelle informazioni sui suggerimenti perché queste icone comunicano principalmente lo stato.

### <a name="appropriate-timeouts"></a>Timeout appropriati

La visualizzazione automatica e la rimozione appropriate dei suggerimenti sono fondamentali per l'obiettivo degli utenti di mantenere il controllo dell'ambiente dell'interfaccia utente. I suggerimenti hanno tre valori di timeout:

-   **Iniziale.** Tempo in cui l'indicatore di misura deve rimanere zionario per visualizzare la mancia. L'ora predefinita è 0,5 secondi.
-   **Mostra.** Tempo in cui l'indicatore di misura deve rimanere stazionare quando il puntatore si sposta da una destinazione a un'altra. L'ora predefinita è 0,1 secondi.
-   **Rimozione.** Ora dopo la quale la mancia viene rimossa automaticamente. Il tempo predefinito è 5 secondi.

La presenza di valori iniziali e di descrizione troppo brevi comporta un'esperienza disaffezionata e disaffezionata perché spesso vengono visualizzati inavvertitamente, mentre troppo a lungo i suggerimenti non rispondono o non vengono individuati. Il tempo di rimozione predefinito funziona bene per il testo breve della mancia, come usato nelle descrizioni comando. Le descrizioni comandi hanno testo più lungo, quindi necessitano di tempi di visualizzazione più lunghi.

### <a name="appropriate-placement"></a>Posizionamento appropriato

Le descrizioni comandi devono essere posizionate accanto all'oggetto al passaggio del mouse, in genere alla coda o alla testa del puntatore, se possibile. Tuttavia, non devono mai essere posizionati in modo da interferire con ciò che l'utente sta facendo oscurando l'oggetto di interesse. Per evitare questo problema potrebbe essere necessario spostare la mancia dal puntatore, ma adiacente all'oggetto . Non si tratta di un problema, purché la relazione tra l'oggetto e la relativa descrizione sia chiara. Assicurarsi che gli utenti non spostino il puntatore solo per ottenere i suggerimenti per il programma.

### <a name="accessibility"></a>Accessibilità

I suggerimenti hanno un effetto insolito sull'accessibilità. Anche se vengono in genere attivati passando il puntatore [](inter-accessibility.md) del mouse su un oggetto, i suggerimenti vengono gestiti dalle utilità per la lettura dello schermo per i controlli con accesso tramite tastiera. Se usati in modo appropriato per informazioni concise, utili, statiche e supplementari, i suggerimenti possono migliorare l'accessibilità complessiva. In realtà, il modello di suggerimento del testo alternativo è il modo preferito per rendere accessibile la grafica. Tuttavia, se usati in modo non appropriato, danneggiano l'accessibilità rendendo più difficile ottenere informazioni importanti o dinamiche.

Fornire più di un modo per accedere a un controllo se tale controllo richiede un suggerimento che non ha accesso tramite tastiera.

![Screenshot del pulsante di stampa con la descrizione comando ](images/ctrl-tooltips-and-infotips-image4.png)

In questo esempio, gli utenti possono stampare usando il pulsante della barra degli strumenti (che non è accessibile da tastiera) o il tasto di scelta rapida del comando Stampa.

**Se si fa una sola cosa...**

Progettare suggerimenti individuabili che visualizzano informazioni concise, utili, statiche e supplementari nella posizione appropriata al momento appropriato.

## <a name="usage-patterns"></a>Modelli di utilizzo

I suggerimenti hanno diversi modelli di utilizzo:



|    Utilizzo                                                                                                                             |    Esempio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Descrizioni comandi**<br/> consente di visualizzare l'etichetta di un controllo o di un glifo senza etichetta. <br/>                                         | Poiché questi suggerimenti fungono da etichette, il testo segue le linee guida per le etichette per il controllo sottostante. <br/> ![Screenshot del pulsante esporta elenco con la descrizione comando ](images/ctrl-tooltips-and-infotips-image5.png)<br/> In questo esempio la descrizione comando fornisce l'etichetta del comando.<br/> ![Screenshot del pulsante chiudi con la descrizione comando ](images/ctrl-tooltips-and-infotips-image6.png)![Screenshot del pulsante di riproduzione con la descrizione comando ](images/ctrl-tooltips-and-infotips-image7.png)<br/> In questi esempi, le descrizioni comando etichettano i pulsanti grafici.<br/> ![Screenshot del glifo del menu show con la descrizione comando ](images/ctrl-tooltips-and-infotips-image8.png)<br/> In questo esempio la descrizione comando etichetta un glifo.<br/> |
| **Suggerimenti per le informazioni**<br/> fornire una descrizione supplementare o una spiegazione di un oggetto o di un controllo. <br/>                  | Usare le descrizioni comandi per descrivere [](cmd-toolbars.md) o spiegare oggetti e controlli, ad esempio controlli della barra degli [strumenti,](vis-icons.md) icone (incluse sovrapposizioni di [icone),](ctrl-links.md) [collegamenti,](ctrl-tabs.md) [schede,](ctrl-progressive-disclosure-controls.md)controlli di divulgazione progressiva e controlli personalizzati. <br/> ![Screenshot del pulsante di posta elettronica con suggerimento ](images/ctrl-tooltips-and-infotips-image9.png)<br/> ![Screenshot del pulsante di masterizzazione con la descrizione comando ](images/ctrl-tooltips-and-infotips-image10.png)<br/> In questi esempi, le infotip forniscono informazioni supplementari su controlli e oggetti.<br/>                                                                                        |
| **Suggerimenti per il testo alternativo**<br/> descrivere un elemento grafico per l'accessibilità. <br/>                                              | Questo modello è destinato principalmente agli utenti che hanno una qualche forma di comprovazione della visione e possono usare un'utilità per la lettura dello schermo. <br/> ![Screenshot del pulsante Start di Windows con il suggerimento ](images/ctrl-tooltips-and-infotips-image11.png)<br/> In questo esempio, la descrizione comando descrive la menu Start grafica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Anteprima**<br/> consente di visualizzare una piccola immagine di un elemento. <br/>                                                         | Le anteprime offrono una rappresentazione grafica facilmente riconoscibile di una finestra o di un documento. <br/> ![Screenshot dell'anteprima delle categorie del pannello di controllo ](images/ctrl-tooltips-and-infotips-image12.png)<br/> In questo esempio, la barra delle applicazioni di Windows offre suggerimenti di anteprima per gli elementi.<br/> ![Screenshot dell'anteprima della foto e dei relativi dati ](images/ctrl-tooltips-and-infotips-image13.png)<br/> In questo esempio Windows Raccolta foto suggerimenti sulle anteprime per gli elementi.<br/>                                                                                                                                                                                                                      |
| **Suggerimenti dettagliati**<br/> visualizza informazioni dettagliate su un oggetto. <br/>                                        | I suggerimenti sono un modo efficace per visualizzare informazioni dettagliate su un oggetto o per fornire dati. <br/> ![Screenshot della descrizione comando della foto che mostra il tipo di file ](images/ctrl-tooltips-and-infotips-image14.png)![Screenshot del grafico con valori di dettaglio delle descrizioni comandi ](images/ctrl-tooltips-and-infotips-image15.png)<br/> In questi esempi, le descrizioni comandi forniscono informazioni dettagliate su un oggetto o dati.<br/>                                                                                                                                                                                                                                                                                                      |
| **Suggerimenti per il menu Start**<br/> descrivere una voce nel menu Start. <br/>                                              | Il menu Start è costituito da nomi di programmi e importanti destinazioni di windows, ad esempio documenti, immagini e pannello di controllo. questi suggerimenti descrivono le voci del menu Start, in genere fornendo una breve descrizione del programma o della destinazione, nonché le attività principali che gli utenti possono eseguire con esso. Queste descrizioni vengono indicizzate anche dalla casella di ricerca del menu Start, consentendo agli utenti di trovare i programmi necessari. <br/> ![Screenshot della descrizione comando del Centro di benvenuto ](images/ctrl-tooltips-and-infotips-image16.png)<br/> In questo esempio, la descrizione comando descrive le attività che gli utenti possono eseguire con un programma nel menu Start.<br/>                                                                                    |
| **Pannello di controllo infotip**<br/> descrivere una categoria o un'attività del pannello di controllo. <br/>                                    | Questi suggerimenti forniscono informazioni supplementari per consentire agli utenti di scegliere la categoria e l'elemento del pannello di controllo giusto. <br/> ![Screenshot della categoria di account utente con infotip ](images/ctrl-tooltips-and-infotips-image17.png)<br/> In questo esempio, la descrizione comando descrive la categoria account Pannello di controllo utente.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| **Suggerimenti per il nome completo**<br/> visualizza il nome completo di un elemento quando il nome viene troncato o non completamente visibile. <br/> | Questi suggerimenti consentono di visualizzare gli elementi in uno spazio più compatto, riducendo al tempo stesso la necessità di scorrimento orizzontale. ciò è particolarmente importante quando la lunghezza del contenuto è sconosciuta perché è dinamica. A differenza degli altri modelli, quando vengono usati in elenchi e alberi, questi suggerimenti vengono visualizzati direttamente sull'oggetto di origine. <br/> ![Screenshot della descrizione comando del titolo del gruppo di pulsanti di opzione ](images/ctrl-tooltips-and-infotips-image18.png)<br/> In questo esempio viene usata una descrizione comando per visualizzare il nome completo dell'elemento al passaggio del mouse.<br/>                                                                                                                                                                                     |
| **Suggerimenti per lo stato**<br/> visualizzare le informazioni sullo stato per le icone dell'area di notifica. <br/>                              | In genere, i suggerimenti devono essere statici perché gli utenti non si aspettano che cambino da un'istanza all'altra. **Le icone dell'area di notifica sono un'eccezione** perché comunicano lo stato e non è disponibile altro spazio sullo schermo per il testo dello stato. <br/> ![Screenshot della descrizione comando "Messenger non connesso" ](images/ctrl-tooltips-and-infotips-image19.png)<br/> ![Screenshot della descrizione comando "Messenger connesso" ](images/ctrl-tooltips-and-infotips-image20.png)<br/> In questi esempi, i suggerimenti info forniscono informazioni sullo stato per le icone dell'area di notifica.<br/>                                                                                                                                  |



 

## <a name="guidelines"></a>Indicazioni

### <a name="timeouts"></a>Timeout

-   **Usare i timeout iniziali e di ricomasci predefiniti. Eccezione:**
    -   Le anteprime non ridondanti e visualizzate sul lato dell'oggetto associato possono essere visualizzate immediatamente (senza alcun ritardo). Tuttavia, usare il timeout iniziale predefinito per le anteprime ridondanti (ad esempio una descrizione di anteprima di grandi dimensioni per un oggetto grafico di piccole dimensioni) o le anteprime che coprono l'oggetto associato.
-   **Per le descrizioni comando, usare il timeout predefinito di rimozione della mancia di cinque secondi.**
-   **Per i suggerimenti, disattivare il timeout di rimozione della mancia. Sviluppatori:** poiché tecnicamente non è possibile disattivare il timeout di rimozione, impostarlo sul valore più grande.
-   Per l'accessibilità, se è necessario impostare i valori di timeout su un valore diverso dal valore massimo, impostarli come multipli dei parametri di sistema SPI \_ GETMOUSEHOVERTIME e SPI GETMESSAGEDURATION anziché usare orari \_ fissi. In questo modo i timeout vengono adattati alla velocità dell'utente.

### <a name="placement"></a>Selezione host

-   **Evitare di coprire l'oggetto con cui l'utente sta per visualizzare o interagire.** Posizionare sempre la punta sul lato dell'oggetto, anche se ciò richiede la separazione tra il puntatore e la mancia. Una separazione non è un problema, purché la relazione tra l'oggetto e la relativa mancia sia chiara.

    -   **Eccezione:** Descrizioni comando con nome completo usate in elenchi e alberi.

    **Non corretto:**

    ![Screenshot della casella di ricerca di infotip obscuring ](images/ctrl-tooltips-and-infotips-image21.png)

    **Corretto:**

    ![Screenshot della descrizione comando posizionata sotto la casella di ricerca ](images/ctrl-tooltips-and-infotips-image22.png)

    Nell'esempio corretto, il suggerimento viene posizionato lontano dalla casella di ricerca, anche se ciò richiede spazio tra l'infotip e il caret.

    **Non corretto:**

    ![Screenshot della descrizione comando che oscura il testo modificato ](images/ctrl-tooltips-and-infotips-image23.png)

    **Corretto:**

    ![Screenshot della descrizione comando posizionata sopra il testo modificato ](images/ctrl-tooltips-and-infotips-image24.png)

    Nell'esempio corretto, il testo sottostante è molto più utile della mancia, quindi la descrizione comando viene posizionata ben fuori strada.

-   **Per le raccolte di elementi, evitare di coprire l'oggetto successivo con cui l'utente potrebbe visualizzare o interagire.** Per gli elementi disposti orizzontalmente, evitare di posizionare i suggerimenti a destra; per gli elementi disposti verticalmente, evitare di inserire suggerimenti di seguito.

    **Non corretto:**

    ![Screenshot della descrizione comando che oscura l'elenco di elementi recenti ](images/ctrl-tooltips-and-infotips-image25.png)

    **Corretto:**

    ![Screenshot della descrizione comando accanto all'elenco di elementi recenti ](images/ctrl-tooltips-and-infotips-image26.png)

    Nell'esempio non corretto, la mancia copre l'oggetto con cui l'utente probabilmente interagirà successivamente.

-   **Per suggerimenti potenzialmente distratti (spesso di grandi dimensioni), assicurarsi che le informazioni siano utili per la maggior parte degli utenti.** In caso contrario, rendere facoltativi i suggerimenti di distrazione o addirittura eliminarli. In caso contrario, la maggior parte degli utenti dovrà spostare il puntatore dall'oggetto di destinazione per eliminare la mancia.

### <a name="tooltips"></a>Descrizioni comando

-   **Usare le descrizioni comando per fornire etichette per i controlli senza etichetta.** I controlli che in genere dispongono di descrizioni comando sono pulsanti della [barra](cmd-toolbars.md)degli strumenti, pulsanti grafici e controlli [di divulgazione progressiva.](ctrl-progressive-disclosure-controls.md) I controlli con prompt vengono considerati etichettati, ad esempio caselle [di](ctrl-text-boxes.md) testo e [caselle combinate.](/windows/desktop/uxguide/ctrl-drop) Tutti gli altri controlli devono avere etichette esplicite.
-   Usare frammenti di frase senza terminare la punteggiatura.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
    -   **Eccezione:** Questa linea guida è una novità per Windows Vista. Per le applicazioni legacy, è possibile usare l'uso di maiuscole e minuscole in stile titolo, se necessario, per evitare di combinare gli stili di combinazione di maiuscole e minuscole.
-   Aggiungere i [puntini di sospensione se](ctrl-command-buttons.md) l'etichetta è per un comando che richiede informazioni aggiuntive.
-   Come per le etichette normali, **mantenere le descrizioni** comando brevi in genere con cinque parole o meno, ma preferire etichette specifiche rispetto a quelle vaghe.

    **Accettabile:**

    ![Screenshot della descrizione comando di stampa ](images/ctrl-tooltips-and-infotips-image27.png)

    **Migliore:**

    ![Screenshot della descrizione comando "Stampa nella stampante predefinita" ](images/ctrl-tooltips-and-infotips-image28.png)

    **Miglior:**

    ![Screenshot della descrizione comando 'print (document writer)' ](images/ctrl-tooltips-and-infotips-image29.png)

    **Non corretto:**

    ![Screenshot della descrizione comando dettagliata ](images/ctrl-tooltips-and-infotips-image30.png)

    In questi esempi, l'esempio migliore è sia conciso che specifico, mentre l'esempio non corretto è inutilmente dettagliato.

-   **Le descrizioni comando possono anche fornire maggiori dettagli per i pulsanti della barra degli strumenti etichettati se questa operazione è utile.** Non ripetere o dare una parola di conferma di ciò che è già presente nell'etichetta.

    **Corretto:**

    ![Screenshot della descrizione comando "Cerca in tutte le prospettive" ](images/ctrl-tooltips-and-infotips-image31.png)

    In questo esempio la descrizione comando illustra le funzionalità della ricerca.

    **Non corretto:**

    ![Screenshot dell'etichetta del pulsante di ripetizione della descrizione comando ](images/ctrl-tooltips-and-infotips-image32.png)

    In questo esempio, la descrizione comando ripete semplicemente ciò che è già presente nell'etichetta.

-   **Non è necessario fornire descrizioni comando dei controlli etichettati semplicemente per motivi di coerenza.**

    ![Screenshot dei pulsanti con etichetta e senza etichetta ](images/ctrl-tooltips-and-infotips-image33.png)

    In questo esempio i pulsanti della barra degli strumenti senza etichetta hanno descrizioni comando, ma non quelli con etichetta.

-   Se necessario, rendere **le descrizioni comando più utili fornendo tasti di scelta rapida e valori predefiniti.** Inserire queste informazioni aggiuntive tra parentesi. In questo modo, le descrizioni comando sono utili per i controlli con etichetta anche quando in caso contrario si ripete semplicemente l'etichetta. Non considerare questo testo aggiuntivo quando si valuta la concisità di una descrizione comando.

    ![Screenshot della descrizione comando 'print (document writer)' ](images/ctrl-tooltips-and-infotips-image29.png)

    In questo esempio Word visualizza i valori predefiniti e i tasti di scelta rapida nelle descrizioni comando della barra degli strumenti.

### <a name="infotips"></a>Suggerimenti per le informazioni

-   **Per i suggerimenti in posizioni non standard, favorire la coerenza rispetto all'utilità per migliorare l'individuabilità.** Fornire suggerimenti per tutti gli oggetti per i quali è probabile che gli utenti desiderino informazioni supplementari, anche se alcuni suggerimenti potrebbero essere ovvi. In questo modo si evita che gli utenti attendano un suggerimento che non verrà mai visualizzato.
    -   **Eccezione:** Se solo alcuni oggetti hanno suggerimenti utili, non usare affatto le infotip. Usare invece etichette di controllo auto-esplicativo o testo supplementare sul posto.
-   Usare frasi complete con punteggiatura finale.
    -   **Eccezione:** I suggerimenti per [le icone dell'area](winenv-notification.md) di notifica non usano la punteggiatura finale.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Usare il presente, non il futuro.
-   Usare le costruzione grammaticali parallele. Il parallelismo richiede che le parole e le frasi che hanno la stessa funzione hanno lo stesso formato.
    -   **Eccezione:** Per il modello di infotip del nome completo, il testo della descrizione comando corrisponde esattamente alla formulazione, all'utilizzo di maiuscole e minuscole e alla punteggiatura del controllo sottostante.
-   **Evitare infotip di grandi dimensioni.** Gli infotip di grandi dimensioni sono difficili da leggere e difficili da posizionare senza interferire con l'oggetto sottostante.
-   **Formatta i suggerimenti per semplificare la lettura e l'analisi del contenuto.** Blocchi di testo non formattato di grandi dimensioni possono essere difficili da leggere.

    **Non corretto:**

    ![Screenshot della descrizione comando lunga, non strutturata e di esecuzione ](images/ctrl-tooltips-and-infotips-image34.png)

    **Corretto:**

    ![Screenshot della stessa descrizione comando con una riga per ogni elemento ](images/ctrl-tooltips-and-infotips-image35.png)

    Nell'esempio corretto, il testo formattato è molto più facile da leggere e analizzare.

-   Al primo utilizzo all'interno di un infotip, inserire i nomi degli acronimi, seguiti dall'acronimo tra parentesi. Esempio: "Dynamic Host Configuration Protocol (DHCP)."

### <a name="start-menu-infotips"></a>Suggerimenti per il menu Start

-   Usare menu Start infotip per descrivere l'elemento in modo conciso ed elencare le attività principali che gli utenti **possono eseguire con l'elemento.**
-   **Sii utile.** Concentrarsi sulle operazione che gli utenti possono eseguire. Non è sufficiente ripetere il nome dell'elemento o usarlo nella descrizione.
-   **Essere specifici.** Evitare verbi generici e frasi catch-all come e altre attività. Se le informazioni sono importanti, elencare in modo specifico; In caso contrario, si supponga che gli utenti comprendono che non tutti gli elementi sono elencati nei suggerimenti.
-   **Essere concisi.** Usare un numero di parole inferiore a 25. Le infotip più lunghe sconsigliano la lettura.
-   **Iniziare con un verbo imperativo presente,** ad esempio creare, modificare, mostrare e inviare. Preferisce verbi specifici rispetto ai verbi generici, ad esempio manage e open, che si applicano alla maggior parte menu Start elementi. Arrivare direttamente al punto.

    **Non corretto:**

    ![Screenshot della descrizione comando: apre la cartella musica ](images/ctrl-tooltips-and-infotips-image36.png)

    **Migliore:**

    ![Screenshot della descrizione comando: archiviare e riprodurre musica ](images/ctrl-tooltips-and-infotips-image37.png)

    Nell'esempio non corretto il suggerimento inizia con un verbo generico. L'esempio migliore arriva direttamente al punto con verbi specifici, ma continua a usare la formulazione "e altre" non necessarie alla fine della mancia.

-   **Non usare un linguaggio simile al marketing.**

    **Non corretto:**

    ![Screenshot della descrizione comando "punto di partenza one-stop" ](images/ctrl-tooltips-and-infotips-image38.png)

    In questo esempio, l'infotip è simile al marketing.

-   Poiché questi suggerimenti sono indicizzati per la menu Start di ricerca, descrivere le attività importanti del programma usando termini per cui gli utenti hanno più probabilità di **eseguire la ricerca. Prendere in considerazione l'uso di parole chiave e sinonimi comuni.**

    **Non corretto:**

    ![Screenshot della descrizione comando: creare DVD ](images/ctrl-tooltips-and-infotips-image39.png)

    **Corretto:**

    ![screenshot della descrizione comando: creare (masterizzare) cds, dvd ](images/ctrl-tooltips-and-infotips-image40.png)

    Nell'esempio corretto, la descrizione comandi contiene sinonimi comuni.

-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   **Sviluppatori:** Il menu Start della descrizione comando proviene dal campo Commento dell'elemento.

### <a name="quick-launch-tooltips"></a>Avvio veloce descrizioni comando

-   **Usare una descrizione comando con il formato:** Launch (nome completo del programma)
-   Non usare punteggiatura finale.
-   Non usare testo aggiuntivo per descrivere il programma o le operazioni che esegue. Poiché gli utenti scelgono i programmi visualizzati nella barra Avvio veloce, conoscono già lo scopo.

### <a name="control-panel-infotips"></a>Pannello di controllo infotips

-   Usare Pannello di controllo suggerimenti per descrivere in modo conciso le attività Pannello di controllo e **l'hardware e il software configurati.**
-   **Pannello di controllo nomi e icone devono avere suggerimenti.** Le singole attività non hanno descrizioni comando.
-   **Sii utile.** Concentrarsi sulle cose che gli utenti possono fare. Non solo ripetere il nome Pannello di controllo elemento o anche usarlo nella descrizione.
-   **Essere specifici.** Evitare verbi generici e frasi catch-all come e altro hardware. Se le informazioni sono importanti, elencare le informazioni in modo specifico. In caso contrario, si supponga che gli utenti comprendono che non tutti gli elementi sono elencati nelle descrizioni comandi.

    **Non corretto:**

    ![Screenshot della descrizione comando: configura il mouse ](images/ctrl-tooltips-and-infotips-image41.png)

    **Corretto:**

    ![Screenshot della descrizione comando dettagliata per le impostazioni del mouse ](images/ctrl-tooltips-and-infotips-image42.png)

    Nell'esempio corretto, i tipi di hardware configurati sono elencati in modo specifico.

-   **Essere concisi.** Usare un numero di parole non inferiore a 25. Suggerimenti più lunghi sconsigliano la lettura.
-   **Iniziare con un verbo imperativo presente.**

    **Corretto:**

    Configurare le impostazioni di connessione e visualizzazione Internet.

    Modificare le impostazioni per la vista, l'udito e la mobilità.

-   **Andare direttamente al punto.** Non usare un linguaggio che si applica a qualsiasi Pannello di controllo, ad esempio "Usa per visualizzare e configurare le impostazioni per l'aspetto e la funzionalità di..." o "Fornisce le opzioni per..."
-   Non usare un linguaggio che sembra marketing.

    **Non corretto:**

    Il punto di partenza unico per tutte le esigenze di configurazione del disco.

-   Poiché queste descrizioni comandi sono indicizzate per la Pannello di controllo di ricerca, descrivere gli elementi usando termini per cui gli utenti hanno più probabilità **di eseguire la ricerca.** È consigliabile usare sinonimi comuni per le attività e gli oggetti più diffusi.

    ![Screenshot della descrizione comando con le attività del controller di gioco ](images/ctrl-tooltips-and-infotips-image43.png)

    In questo esempio, l'elemento viene descritto usando termini per i quali gli utenti hanno più probabilità di eseguire la ricerca.

-   Se un Pannello di controllo elemento può essere confuso con altri elementi, spiegarlo in che modo è diverso nella descrizione comandi.

    **Non corretto:**

    ![Screenshot della descrizione comandi priva di dettagli specifici ](images/ctrl-tooltips-and-infotips-image44.png)

    In questo esempio entrambi gli Pannello di controllo configurano l'audio, ma la descrizione comando non chiarisce la differenza.

    **Corretto:**

    ![Screenshot della descrizione comando con dettagli specifici ](images/ctrl-tooltips-and-infotips-image45.png)

    In questo esempio la differenza tra i due elementi è più evidente a causa della mancia.

### <a name="icons"></a>Icone

A differenza delle versioni precedenti di Windows, Windows Vista consente ai suggerimenti di avere icone.

-   Per le descrizioni comando, non usare le icone.
-   Per le descrizioni comandi, usare le icone solo se consentono il riconoscimento o la comprensione o forniscono il contesto. La maggior parte delle descrizioni comandi non deve avere icone.

    ![Screenshot della descrizione comando del volume con l'icona della cuffia ](images/ctrl-tooltips-and-infotips-image46.png)

    In questo esempio la descrizione comandi ha un'icona che consente di associare l'icona al relativo significato.

-   L'icona deve [usare lo stile Aero](vis-icons.md) e avere un aspetto discreto.

Per linee guida ed esempi generali sulle icone, vedere [Icone.](vis-icons.md)

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai suggerimenti:

-   Nella programmazione e in altri documenti tecnici, fare riferimento al tipo di suggerimento (descrizione comando o descrizione comando). Ovunque altrove, è sufficiente chiamarlo suggerimento.
-   Le varianti seguenti non sono corrette: descrizione comando, descrizione comando e descrizione comando.
-   Per descrivere l'interazione dell'utente, usare il passaggio del mouse.

