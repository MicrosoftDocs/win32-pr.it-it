---
title: Descrizioni comando e descrizioni comandi
description: Una descrizione comando è una piccola finestra popup che etichetta il controllo senza etichetta a cui punta, ad esempio i controlli della barra degli strumenti senza etichetta o i pulsanti di comando.
ms.assetid: 80979281-eefb-485a-b42f-7f9e05665357
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 4df7950529b2ac78c9d9bbf51c8996f17bcd985898a286f8d58e05db3b94d27e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041137"
---
# <a name="tooltips-and-infotips"></a>Descrizioni comando e descrizioni comandi

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Una descrizione comando è una piccola finestra popup che etichetta il controllo senza etichetta a cui punta, ad esempio i controlli della barra degli strumenti senza etichetta o i pulsanti di comando.

![Screenshot che mostra il pulsante di stampa con la descrizione comando "Stampa (CTRL+P)" visualizzata.](images/ctrl-tooltips-and-infotips-image1.png)

Descrizione comando tipica per un pulsante della barra degli strumenti.

Poiché le descrizioni comando si sono rivelate così utili, esiste un controllo correlato denominato infotip, che fornisce un testo più descrittivo di quanto sia possibile con le descrizioni comando.

Una descrizione comando è una piccola finestra popup che descrive in modo conciso l'oggetto a cui punta, ad esempio descrizioni di controlli della barra degli strumenti, icone, grafica, collegamenti, oggetti Windows Explorer, elementi menu Start e pulsanti della barra delle applicazioni. Le descrizioni comandi sono una forma di controlli di [divulgazione](ctrl-progressive-disclosure-controls.md)progressiva, eliminando la necessità di avere sempre un testo descrittivo sullo schermo.

![Screenshot del pulsante Condividi con la descrizione comando ](images/ctrl-tooltips-and-infotips-image2.png)

Un infotip tipico.

Ai fini di questo articolo, le descrizioni comando e le descrizioni comando vengono definite collettivamente suggerimenti.

Suggerimenti aiutare gli utenti a comprendere oggetti sconosciuti o sconosciuti che non sono descritti direttamente nell'interfaccia utente. Vengono visualizzate automaticamente quando gli utenti passano il puntatore del mouse su un oggetto e vengono rimosse quando gli utenti fanno clic sul controllo o spostano il mouse o quando si verifica il timeout della mancia.

**Sviluppatori:** Non è disponibile alcun controllo infotip; Le infotip vengono implementate con il controllo descrizione comando. La distinzione è nell'utilizzo, non nell'implementazione.

> [!Note]  
> Le linee guida relative [ai fumetto,](ctrl-balloons.md) [alle barre degli](cmd-toolbars.md)strumenti e alla [Guida](winenv-help.md) sono presentate in articoli separati.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Le informazioni vengono visualizzate in base al passaggio del puntatore del mouse?** Se non è così, usa un altro controllo. I suggerimenti visualizzati solo come risultato dell'interazione dell'utente non li visualizzano mai da soli. Al contrario, [i palloncino](ctrl-balloons.md) possono essere visualizzati da soli (come con le notifiche), quindi hanno una coda che identifica l'origine.
-   **Un controllo ha un'etichetta di testo?** Se non ne ha una, usa una descrizione comando per fornire l'etichetta. Si noti che la maggior parte dei controlli deve essere etichettata e pertanto non contiene descrizioni comando. I controlli barra degli strumenti e i pulsanti di comando con etichette grafiche devono avere descrizioni comando.
-   **Un oggetto può trarre vantaggio da una descrizione supplementare o da altre informazioni?** In tal caso, usare un infotip. Tuttavia, il testo deve essere supplementare, non essenziale per le attività primarie. Se è essenziale, inseriscilo direttamente nell'interfaccia utente, in modo che gli utenti non debbano trovarlo o andare alla ricerca di informazioni.
-   **Le informazioni supplementari sono un errore, un avviso o uno stato?** In tal caso, usare un altro elemento dell'interfaccia utente, ad esempio un fumetto, un [messaggio di errore](mess-error.md)o una barra di [stato.](ctrl-status-bars.md) I suggerimenti per le icone dell'area di notifica sono un'eccezione perché possono essere usati per visualizzare informazioni sullo stato.
-   **Gli utenti devono interagire con la descrizione comando?** In tal caso, usare un altro controllo, ad esempio un fumetto. Gli utenti non possono interagire con le descrizioni comandi perché spostando il mouse spariscono.
-   **Gli utenti devono stampare le informazioni supplementari?** In tal caso, usare un altro controllo, ad esempio un campo di commento statico. Tuttavia, è anche possibile usare infotip per fornire un accesso più diretto a queste informazioni.

    ![Screenshot del fumetto dei commenti ](images/ctrl-tooltips-and-infotips-image3.png)

    In questo esempio, un campo di commento statico in Microsoft Word consente agli utenti di stampare commenti.

-   **Il contesto è tale che gli utenti potrebbero trovare i suggerimenti fastidiosi o distratti?** In tal caso, è consigliabile usare un'altra soluzione, inclusa l'operazione non eseguire alcuna operazione. Se si usano suggerimenti in tali contesti, consentire agli utenti di disattivarli.

Se usati in modo appropriato, i suggerimenti migliorano la comunicazione con l'utente. **Non usare mai i suggerimenti come sostituto di una buona progettazione.** Se un elemento grafico, un pulsante o un altro oggetto richiede agli utenti di continuare a controllare un suggerimento per comprenderlo, la progettazione non è necessaria. Correggere invece la progettazione.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Suggerimenti un modo efficace per semplificare un'interfaccia utente. Forniscono informazioni necessarie agli utenti quando ne hanno bisogno, con il minimo sforzo da parte loro. Suggerimenti possibile usare lo spazio dello schermo in modo più efficace e ridurre il disordine dello schermo. Tuttavia, i suggerimenti progettati in modo non efficace possono essere fastidiosi, distratti, inutili, travolgenti o instradanti. I concetti di progettazione seguenti sono destinati a mostrare la differenza.

### <a name="discoverability"></a>Individuabilità

Suggerimenti automaticamente quando gli utenti passano il puntatore del mouse su un oggetto per un periodo di tempo. Questo meccanismo di ritardo temporale rende i suggerimenti molto utili, ma ne riduce anche l'individuabilità.

Nel corso del tempo, gli utenti apprendono che alcuni oggetti standard come i pulsanti della barra degli strumenti, i pulsanti grafici, gli elementi menu Start e le icone dell'area di notifica hanno suggerimenti, in modo da poter dare per scontata la loro individuabilità.

L'individuazione dei suggerimenti in posizioni non standard richiede più tempo per gli utenti. Non esiste alcun indizio visivo, ad esempio un'area sensibile o una modifica del puntatore, che indica che un oggetto ha una mancia. Ancora peggiore, alcuni utenti spostano molto il mouse, soprattutto quando stanno imparando a spostarsi nell'interfaccia utente. Gli utenti devono sapere che un oggetto ha una mancia, tramite esperienza passata o tramite sperimentazione.

È possibile migliorare l'individuabilità usando i suggerimenti in modo coerente, che a sua volta favorisce la prevedibilità. Se si forniscono suggerimenti per alcuni oggetti, è consigliabile specificarli per tutti gli oggetti simili per i quali è probabile che gli utenti desiderino informazioni supplementari. In alcuni casi può essere difficile, perché è necessario assicurarsi che i suggerimenti siano utili e non ovvi.

Se fornire suggerimenti individuabili e sempre utili si rivela un problema, prendere in considerazione progettazioni alternative, ad esempio etichette di controllo auto-esplicativi o testo supplementare sul posto.

### <a name="appropriate-information"></a>Informazioni appropriate

Le informazioni appropriate per i suggerimenti hanno le caratteristiche seguenti:

-   **Conciso.** Le finestre popup usate dai suggerimenti sono ideali per frasi brevi e frammenti di frasi, nonché per testo formattato. Blocchi di testo grandi e non formattati sono difficili da leggere e travolgenti.
-   **Disponibile.** Il testo della mancia deve essere informativo. Non dovrebbe essere ovvio o semplicemente ripetere ciò che è già sullo schermo.
-   **Supplementare.** Poiché il testo della mancia non è sempre visibile, devono essere informazioni supplementari che gli utenti non devono leggere. Le informazioni importanti devono essere comunicate usando etichette di controllo auto-esplicativo o testo supplementare sul posto.
-   **Statico.** Gli utenti non si aspettano che i suggerimenti cambino da un'istanza a quella successiva, quindi è improbabile che notino modifiche nel contenuto dinamico, ad esempio le informazioni sullo stato. I suggerimenti per le icone dell'area di notifica sono un'eccezione importante: è più probabile che gli utenti rilevino le modifiche nelle informazioni di suggerimento perché queste icone comunicano principalmente lo stato.

### <a name="appropriate-timeouts"></a>Timeout appropriati

La visualizzazione automatica appropriata e la rimozione dei suggerimenti sono fondamentali per l'obiettivo degli utenti di mantenere il controllo dell'ambiente dell'interfaccia utente. Suggerimenti tre valori di timeout:

-   **Iniziale.** Tempo in cui il puntatore deve rimanere fermo per visualizzare la mancia. L'ora predefinita è 0,5 secondi.
-   **Eseguire di nuovo la coma.** Tempo in cui il puntatore deve rimanere fermo quando il puntatore si sposta da una destinazione a un'altra. L'ora predefinita è 0,1 secondi.
-   **Rimozione.** Ora dopo la quale la mancia viene rimossa automaticamente. Il tempo predefinito è 5 secondi.

La presenza di valori iniziali e di sincronizzazione troppo brevi comporta un'esperienza fastidiosa e dirompente perché spesso vengono visualizzati inavvertitamente, mentre troppo a lungo comporta che i suggerimenti non rispettino o non vengano individuati. Il tempo di rimozione predefinito è utile per il testo breve della descrizione comando, come usato nelle descrizioni comando. Le descrizioni comandi hanno testo più lungo, quindi necessitano di tempi di visualizzazione più lunghi.

### <a name="appropriate-placement"></a>Posizionamento appropriato

Suggerimenti deve essere posizionato vicino all'oggetto su cui si passa il puntatore, in genere alla coda o alla testa del puntatore, se possibile. Tuttavia, non devono mai essere posizionati in modo da interferire con ciò che l'utente sta facendo, offuscando l'oggetto di interesse. Per evitare questo problema potrebbe essere necessario spostare la mancia dal puntatore, ma adiacente all'oggetto . Questo non è un problema, purché la relazione tra l'oggetto e la relativa mancia sia chiara. Assicurarsi che gli utenti non spostino il puntatore solo per ottenere i suggerimenti del programma da spostare.

### <a name="accessibility"></a>Accessibilità

Suggerimenti hanno un effetto insolito sull'accessibilità. Anche se in genere vengono attivati passando il puntatore [](inter-accessibility.md) del mouse su un oggetto, i suggerimenti vengono gestiti dalle utilità per la lettura dello schermo per i controlli con accesso tramite tastiera. Se usati in modo appropriato per informazioni concise, utili, statiche e supplementari, i suggerimenti possono migliorare l'accessibilità complessiva. In realtà, il modello di suggerimento per il testo alternativo è il modo migliore per rendere accessibile la grafica. Tuttavia, quando vengono usate in modo inappropriato, danneggiano l'accessibilità rendendo più difficile ottenere informazioni importanti o dinamiche.

Fornire più di un modo per accedere a un controllo se tale controllo richiede un suggerimento che non ha accesso tramite tastiera.

![Screenshot del pulsante di stampa con la descrizione comando ](images/ctrl-tooltips-and-infotips-image4.png)

In questo esempio gli utenti possono stampare usando il pulsante della barra degli strumenti (che non è accessibile da tastiera) o i tasti di scelta rapida del comando Stampa.

**Se si fa una sola cosa...**

Progettare suggerimenti individuabili che visualizzano informazioni concise, utili, statiche e supplementari nella posizione appropriata al momento appropriato.

## <a name="usage-patterns"></a>Modelli di utilizzo

Suggerimenti diversi modelli di utilizzo:



|    Utilizzo                                                                                                                             |    Esempio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Descrizioni comandi**<br/> consente di visualizzare l'etichetta di un controllo o di un glifo senza etichetta. <br/>                                         | Poiché questi suggerimenti fungono da etichette, il relativo testo segue le linee guida per le etichette per il controllo sottostante. <br/> ![Screenshot del pulsante esporta elenco con descrizione comando ](images/ctrl-tooltips-and-infotips-image5.png)<br/> In questo esempio, la descrizione comando fornisce l'etichetta del comando.<br/> ![Screenshot del pulsante chiudi con la descrizione comando ](images/ctrl-tooltips-and-infotips-image6.png)![Screenshot del pulsante di riproduzione con la descrizione comando ](images/ctrl-tooltips-and-infotips-image7.png)<br/> In questi esempi, le descrizioni comando etichettano i pulsanti grafici.<br/> ![Screenshot del glifo del menu Mostra con descrizione comando ](images/ctrl-tooltips-and-infotips-image8.png)<br/> In questo esempio la descrizione comando etichetta un glifo.<br/> |
| **Descrizioni comandi**<br/> fornire una descrizione supplementare o una spiegazione di un oggetto o di un controllo. <br/>                  | Usare le descrizioni comandi per descrivere [](cmd-toolbars.md) o spiegare oggetti e controlli come i controlli della barra degli [strumenti,](vis-icons.md) le icone (incluse le sovrimpressione delle [icone),](ctrl-links.md)i [collegamenti,](ctrl-tabs.md)le [schede,](ctrl-progressive-disclosure-controls.md)i controlli di divulgazione progressiva e i controlli personalizzati. <br/> ![Screenshot del pulsante di posta elettronica con la descrizione comandi ](images/ctrl-tooltips-and-infotips-image9.png)<br/> ![Screenshot del pulsante masterizzazione con la descrizione comandi ](images/ctrl-tooltips-and-infotips-image10.png)<br/> In questi esempi, le descrizioni comandi forniscono informazioni supplementari su controlli e oggetti.<br/>                                                                                        |
| **Suggerimenti per il testo alternativo**<br/> descrivere un elemento grafico per l'accessibilità. <br/>                                              | Questo modello è destinato principalmente agli utenti con problemi di vista e che potrebbero usare un'utilità per la lettura dello schermo. <br/> ![Screenshot del pulsante Start di Windows con la descrizione comandi ](images/ctrl-tooltips-and-infotips-image11.png)<br/> In questo esempio la descrizione comando descrive il menu Start grafico.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Anteprima**<br/> visualizza una piccola immagine di un elemento. <br/>                                                         | Le anteprime offrono una rappresentazione grafica facilmente riconoscibile di una finestra o di un documento. <br/> ![Screenshot dell'anteprima delle categorie del pannello di controllo ](images/ctrl-tooltips-and-infotips-image12.png)<br/> In questo esempio la barra delle applicazioni di Windows fornisce suggerimenti in anteprima per gli elementi.<br/> ![screenshot dell'anteprima della foto e dei relativi dati ](images/ctrl-tooltips-and-infotips-image13.png)<br/> In questo esempio, Windows Raccolta foto suggerimenti in anteprima per gli elementi.<br/>                                                                                                                                                                                                                      |
| **Descrizioni comandi dettagliate**<br/> visualizza informazioni dettagliate su un oggetto. <br/>                                        | Le descrizioni comandi sono un modo efficace per visualizzare informazioni dettagliate su un oggetto o per fornire dati. <br/> ![Screenshot della descrizione comandi della foto che mostra il tipo di file ](images/ctrl-tooltips-and-infotips-image14.png)![Screenshot del grafico con i valori di dettaglio della descrizione comando ](images/ctrl-tooltips-and-infotips-image15.png)<br/> In questi esempi, le descrizioni comandi forniscono informazioni dettagliate su un oggetto o dati.<br/>                                                                                                                                                                                                                                                                                                      |
| **Suggerimenti per il menu Start**<br/> descrivere una voce nel menu Start. <br/>                                              | Il menu Start è costituito da nomi di programma e destinazioni di finestre importanti, ad esempio documenti, immagini e pannello di controllo. Questi suggerimenti descrivono le voci del menu Start, in genere fornendo una breve descrizione del programma o della destinazione, nonché le attività principali che gli utenti possono eseguire con esso. Queste descrizioni vengono indicizzate anche dalla casella di ricerca del menu Start, per consentire agli utenti di trovare i programmi necessari. <br/> ![Screenshot della descrizione comandi dell'area di benvenuto ](images/ctrl-tooltips-and-infotips-image16.png)<br/> In questo esempio la descrizione comando descrive le attività che gli utenti possono eseguire con un programma nel menu Start.<br/>                                                                                    |
| **Pannello di controllo infotips**<br/> descrivere una categoria o un'attività del Pannello di controllo. <br/>                                    | Questi suggerimenti forniscono informazioni supplementari per aiutare gli utenti a scegliere la categoria e l'elemento del pannello di controllo più a destra. <br/> ![Screenshot della categoria degli account utente con la descrizione comando ](images/ctrl-tooltips-and-infotips-image17.png)<br/> In questo esempio la descrizione comando descrive la categoria account Pannello di controllo utente.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| **Descrizioni comandi per il nome completo**<br/> visualizza il nome completo di un elemento quando il nome viene troncato o non è completamente visibile. <br/> | Questi suggerimenti consentono di visualizzare gli elementi in uno spazio più compatto, riducendo al tempo stesso la necessità di scorrimento orizzontale. Ciò è particolarmente importante quando la lunghezza del contenuto è sconosciuta perché è dinamica. A differenza degli altri modelli, quando vengono usati in elenchi e alberi, questi suggerimenti vengono visualizzati direttamente sull'oggetto di origine. <br/> ![Screenshot della descrizione comandi del titolo del gruppo di pulsanti di opzione ](images/ctrl-tooltips-and-infotips-image18.png)<br/> In questo esempio viene usata una descrizione comandi per visualizzare il nome completo dell'elemento al passaggio del mouse.<br/>                                                                                                                                                                                     |
| **Suggerimenti sullo stato**<br/> visualizza informazioni sullo stato per le icone dell'area di notifica. <br/>                              | In genere, i suggerimenti devono essere statici perché gli utenti non si aspettano che cambino da un'istanza all'altra. **Le icone dell'area di notifica sono un'eccezione** perché comunicano lo stato e non è disponibile altro spazio sullo schermo per il testo dello stato. <br/> ![Screenshot della descrizione comando "Messenger non connesso" ](images/ctrl-tooltips-and-infotips-image19.png)<br/> ![Screenshot della descrizione comando "Messenger connesso" ](images/ctrl-tooltips-and-infotips-image20.png)<br/> In questi esempi, le descrizioni comandi forniscono informazioni sullo stato per le icone dell'area di notifica.<br/>                                                                                                                                  |



 

## <a name="guidelines"></a>Indicazioni

### <a name="timeouts"></a>Timeout

-   **Usare i timeout iniziali predefiniti e mostrali. Eccezione:**
    -   Le anteprime non ridondanti e visualizzate sul lato dell'oggetto associato possono essere visualizzate immediatamente (senza alcun ritardo). Tuttavia, usare il timeout iniziale predefinito per le anteprime ridondanti (ad esempio, un suggerimento di anteprima di grandi dimensioni per un oggetto grafico di piccole dimensioni) o le anteprime che coprono l'oggetto associato.
-   **Per le descrizioni comando, usare il timeout predefinito di rimozione della mancia di cinque secondi.**
-   **Per le descrizioni comandi, disattivare il timeout di rimozione della mancia. Sviluppatori:** poiché tecnicamente non è possibile disattivare il timeout di rimozione, impostarlo sul valore più grande.
-   Per l'accessibilità, se è necessario impostare i valori di timeout su un valore diverso dal valore massimo, impostarli come multipli dei parametri di sistema SPI \_ GETMOUSEHOVERTIME e SPI GETMESSAGEDURATION anziché usare orari \_ fissi. In questo modo i timeout vengono adattati alla velocità dell'utente.

### <a name="placement"></a>Selezione host

-   **Evitare di coprire l'oggetto che l'utente sta per visualizzare o con cui interagire.** Posizionare sempre la mancia sul lato dell'oggetto, anche se ciò richiede la separazione tra il puntatore e la mancia. Una separazione non è un problema, purché la relazione tra l'oggetto e la relativa mancia sia chiara.

    -   **Eccezione:** Descrizioni comando con nome completo usate in elenchi e alberi.

    **Non corretto:**

    ![Screenshot della casella di ricerca che offusse le descrizioni comandi ](images/ctrl-tooltips-and-infotips-image21.png)

    **Corretto:**

    ![Screenshot della descrizione comando posizionata sotto la casella di ricerca ](images/ctrl-tooltips-and-infotips-image22.png)

    Nell'esempio corretto, la descrizione comandi viene posizionata fuori dalla casella Di ricerca, anche se ciò richiede spazio tra di essa e il caret.

    **Non corretto:**

    ![Screenshot della descrizione comando che offuse il testo modificato ](images/ctrl-tooltips-and-infotips-image23.png)

    **Corretto:**

    ![Screenshot della descrizione comando posizionata sopra il testo modificato ](images/ctrl-tooltips-and-infotips-image24.png)

    Nell'esempio corretto, il testo sottostante è molto più utile del suggerimento, quindi la descrizione comando viene posizionata in modo corretto.

-   **Per le raccolte di elementi, evitare di coprire l'oggetto successivo che l'utente probabilmente visualizza o con cui interagisce.** Per gli elementi disposti orizzontalmente, evitare di posizionare le mance a destra; per gli elementi disposti verticalmente, evitare di inserire suggerimenti di seguito.

    **Non corretto:**

    ![Screenshot della descrizione comando che offuse l'elenco di elementi recenti ](images/ctrl-tooltips-and-infotips-image25.png)

    **Corretto:**

    ![Screenshot della descrizione comando accanto all'elenco di elementi recenti ](images/ctrl-tooltips-and-infotips-image26.png)

    Nell'esempio errato, il suggerimento copre l'oggetto con cui l'utente probabilmente interagirà successivamente.

-   **Per suggerimenti potenzialmente distranti (spesso di grandi dimensioni), assicurarsi che le informazioni siano utili per la maggior parte degli utenti.** In caso contrario, rendere facoltativi i suggerimenti di distrazione o addirittura eliminarli. In caso contrario, la maggior parte degli utenti dovrà spostare il puntatore dall'oggetto di destinazione per eliminare la mancia.

### <a name="tooltips"></a>Descrizioni comando

-   **Usare le descrizioni comando per fornire etichette per i controlli senza etichetta.** I controlli che in genere hanno descrizioni comando sono pulsanti [della barra degli](cmd-toolbars.md)strumenti, pulsanti grafici e controlli di [divulgazione progressiva.](ctrl-progressive-disclosure-controls.md) I controlli con prompt vengono considerati etichettati, ad esempio [caselle di testo](ctrl-text-boxes.md) e [caselle combinate.](/windows/desktop/uxguide/ctrl-drop) Tutti gli altri controlli devono avere etichette esplicite.
-   Usare frammenti di frase senza terminare la punteggiatura.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
    -   **Eccezione:** Questa linea guida è una novità per Windows Vista. Per le applicazioni legacy, è possibile usare la combinazione di maiuscole e minuscole in stile titolo, se necessario, per evitare di combinare gli stili di uso delle maiuscole.
-   Aggiungere i [puntini di sospensione se](ctrl-command-buttons.md) l'etichetta è per un comando che richiede informazioni aggiuntive.
-   Come per le etichette normali, **mantenere brevi descrizioni comando,** in genere cinque parole o meno, ma preferire etichette specifiche rispetto a quelle erre.

    **Accettabile:**

    ![Screenshot della descrizione comando di stampa ](images/ctrl-tooltips-and-infotips-image27.png)

    **Migliore:**

    ![Screenshot della descrizione comando "Stampa su stampante predefinita" ](images/ctrl-tooltips-and-infotips-image28.png)

    **Miglior:**

    ![Screenshot della descrizione comando "print (document writer)" ](images/ctrl-tooltips-and-infotips-image29.png)

    **Non corretto:**

    ![Screenshot della descrizione comando dettagliata ](images/ctrl-tooltips-and-infotips-image30.png)

    In questi esempi, l'esempio migliore è sia conciso che specifico, mentre l'esempio non corretto è inutilmente dettagliato.

-   **Le descrizioni comando possono anche fornire maggiori dettagli per i pulsanti della barra degli strumenti etichettati, se questa operazione è utile.** Non solo ripetere o fornire una rieificazione di ciò che è già presente nell'etichetta.

    **Corretto:**

    ![Screenshot della descrizione comando "Cerca in tutti i outlook" ](images/ctrl-tooltips-and-infotips-image31.png)

    In questo esempio la descrizione comando illustra le funzionalità della ricerca.

    **Non corretto:**

    ![Screenshot dell'etichetta del pulsante di ripetizione della descrizione comando ](images/ctrl-tooltips-and-infotips-image32.png)

    In questo esempio la descrizione comando ripete semplicemente ciò che è già presente nell'etichetta.

-   **Non è necessario assegnare descrizioni comando ai controlli etichettati semplicemente per motivi di coerenza.**

    ![Screenshot dei pulsanti etichettati e senza etichetta ](images/ctrl-tooltips-and-infotips-image33.png)

    In questo esempio i pulsanti della barra degli strumenti senza etichetta hanno descrizioni comando, ma quelli con etichetta no.

-   Quando appropriato, rendere **le descrizioni comando più utili fornendo tasti di scelta rapida e valori predefiniti.** Inserire queste informazioni aggiuntive tra parentesi. In questo modo le descrizioni comando sono utili per i controlli etichettati anche quando in caso contrario si ripete semplicemente l'etichetta. Non considerare questo testo aggiuntivo quando si valuta la concisità di una descrizione comando.

    ![Screenshot della descrizione comando "print (document writer)" ](images/ctrl-tooltips-and-infotips-image29.png)

    In questo esempio Word visualizza i valori predefiniti e i tasti di scelta rapida nelle descrizioni comando della barra degli strumenti.

### <a name="infotips"></a>Descrizioni comandi

-   **Per i suggerimenti in posizioni non standard, favorire la coerenza rispetto all'utilità per migliorare l'individuabilità.** Fornire suggerimenti per tutti gli oggetti per cui è probabile che gli utenti vogliano informazioni supplementari, anche se alcune descrizioni comandi potrebbero essere ovvie. In questo modo si evita che gli utenti attendano un suggerimento che non verrà mai visualizzato.
    -   **Eccezione:** Se solo alcuni oggetti hanno suggerimenti utili, non usare affatto le descrizioni comandi. Usare invece etichette di controllo auto-esplicativi o testo supplementare sul posto.
-   Usare frasi complete con punteggiatura finale.
    -   **Eccezione:** Le descrizioni [comandi dell'icona dell'area](winenv-notification.md) di notifica non usano la punteggiatura finale.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Usare il presente, non il futuro.
-   Usare le strutture grammaticali parallele. Il parallelismo richiede che le parole e le frasi che hanno la stessa funzione hanno la stessa forma.
    -   **Eccezione:** Per il modello di suggerimento per il nome completo, il testo della descrizione comandi corrisponde esattamente alla formulazione, all'utilizzo di maiuscole e minuscole e alla punteggiatura del controllo sottostante.
-   **Evitare suggerimenti di grandi dimensioni.** Le descrizioni comandi di grandi dimensioni sono difficili da leggere e difficili da posizionare senza interferire con l'oggetto sottostante.
-   **Formatta le descrizioni comandi per semplificare la lettura e l'analisi del contenuto.** Blocchi di testo non formattato di grandi dimensioni possono essere difficili da leggere.

    **Non corretto:**

    ![Screenshot della descrizione comando lunga, non strutturata e di esecuzione ](images/ctrl-tooltips-and-infotips-image34.png)

    **Corretto:**

    ![screenshot della stessa descrizione comando con una riga per elemento ](images/ctrl-tooltips-and-infotips-image35.png)

    Nell'esempio corretto, il testo formattato è molto più facile da leggere e analizzare.

-   Al primo utilizzo all'interno di una descrizione comando, inserire i nomi degli acronimi, seguiti dall'acronimo tra parentesi. Esempio: "Dynamic Host Configuration Protocol (DHCP)."

### <a name="start-menu-infotips"></a>Suggerimenti per il menu Start

-   Usare menu Start suggerimenti per descrivere l'elemento in modo conciso ed elencare le attività principali che gli utenti **possono eseguire con l'elemento.**
-   **Sii utile.** Concentrarsi sulle cose che gli utenti possono fare. Non è sufficiente ripetere il nome dell'elemento o persino usarlo nella descrizione.
-   **Essere specifici.** Evitare verbi generici e frasi catch-all come e altre attività. Se le informazioni sono importanti, elencare le informazioni in modo specifico. In caso contrario, si supponga che gli utenti comprendono che non tutti gli elementi sono elencati nelle descrizioni comandi.
-   **Essere concisi.** Usare un numero di parole non inferiore a 25. Suggerimenti più lunghi sconsigliano la lettura.
-   **Iniziare con un verbo imperativo presente,** ad esempio create, edit, show e send. Preferisce verbi specifici rispetto a verbi generici, ad esempio manage e open, che si applicano alla maggior parte menu Start elementi. Andare direttamente al punto.

    **Non corretto:**

    ![Screenshot della descrizione comando: apre la cartella musica ](images/ctrl-tooltips-and-infotips-image36.png)

    **Migliore:**

    ![Screenshot della descrizione comando: archiviare e riprodurre musica ](images/ctrl-tooltips-and-infotips-image37.png)

    Nell'esempio non corretto, la descrizione comando inizia con un verbo generico. L'esempio migliore arriva direttamente al punto con verbi specifici, ma continua a usare la formulazione non necessaria "e altre" alla fine della mancia.

-   **Non usare un linguaggio che sembra marketing.**

    **Non corretto:**

    ![Screenshot della descrizione comando "punto di partenza uni stop" ](images/ctrl-tooltips-and-infotips-image38.png)

    In questo esempio la descrizione comando sembra marketing.

-   Poiché queste descrizioni comandi sono indicizzate per la casella di ricerca menu Start, descrivere le attività importanti del programma usando i termini per cui gli utenti hanno più probabilità di **eseguire la ricerca. È consigliabile usare parole chiave e sinonimi comuni.**

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

-   Usare Pannello di controllo suggerimenti per **descrivere in modo conciso** le attività Pannello di controllo e l'hardware e il software configurati.
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

-   Se un Pannello di controllo elemento può essere confuso con altri, spiegare le relative diverse modalità di utilizzo nella descrizione comandi.

    **Non corretto:**

    ![Screenshot della descrizione comandi priva di dettagli specifici ](images/ctrl-tooltips-and-infotips-image44.png)

    In questo esempio entrambi gli Pannello di controllo configurano il suono, ma la descrizione comando non chiarisce la differenza.

    **Corretto:**

    ![Screenshot della descrizione comando con dettagli specifici ](images/ctrl-tooltips-and-infotips-image45.png)

    In questo esempio la differenza tra i due elementi è più evidente a causa della mancia.

### <a name="icons"></a>Icone

A differenza delle versioni precedenti Windows, Windows Vista consente ai suggerimenti di avere icone.

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

