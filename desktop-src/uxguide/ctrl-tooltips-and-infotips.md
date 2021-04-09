---
title: Descrizioni comandi e infotip
description: Una descrizione comando è una piccola finestra popup che etichetta il controllo senza etichetta a cui fa riferimento, ad esempio i controlli della barra degli strumenti senza etichetta o i pulsanti di comando.
ms.assetid: 80979281-eefb-485a-b42f-7f9e05665357
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ddccf694b51bf8357dd779bd70146bebf4f14345
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103885914"
---
# <a name="tooltips-and-infotips"></a>Descrizioni comandi e infotip

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Una descrizione comando è una piccola finestra popup che etichetta il controllo senza etichetta a cui fa riferimento, ad esempio i controlli della barra degli strumenti senza etichetta o i pulsanti di comando.

![Screenshot che mostra il pulsante stampa con la descrizione comando "Print (CTRL + P)" visualizzata.](images/ctrl-tooltips-and-infotips-image1.png)

Una descrizione comando tipica per un pulsante della barra degli strumenti.

Poiché le descrizioni comandi sono risultate così utili, esiste un controllo correlato denominato infotip, che fornisce un testo più descrittivo rispetto a quanto possibile con le descrizioni comandi.

Un infotip è una piccola finestra popup che descrive in modo conciso l'oggetto a cui si fa riferimento, ad esempio le descrizioni dei controlli della barra degli strumenti, le icone, le immagini, i collegamenti, gli oggetti di Esplora risorse, le voci del menu Start e i pulsanti della barra delle applicazioni. Infotip sono una forma di [controlli di divulgazione progressivi](ctrl-progressive-disclosure-controls.md), eliminando sempre la necessità di avere un testo descrittivo sullo schermo.

![cattura di schermata del pulsante Condividi con infotip ](images/ctrl-tooltips-and-infotips-image2.png)

Infotip tipico.

Ai fini di questo articolo, le descrizioni comandi e infotip vengono definite collettivamente come suggerimenti.

I suggerimenti consentono agli utenti di comprendere oggetti sconosciuti o non noti che non sono descritti direttamente nell'interfaccia utente (UI). Vengono visualizzati automaticamente quando gli utenti posizionano il puntatore del mouse su un oggetto e vengono rimossi quando gli utenti fanno clic sul controllo o spostano il mouse o quando si verifica il timeout del suggerimento.

**Sviluppatori:** Nessun controllo infotip. infotip vengono implementati con il controllo ToolTip. La distinzione è nell'utilizzo, non nell'implementazione.

> [!Note]  
> Le linee guida relative a [palloncini](ctrl-balloons.md), [barre degli strumenti](cmd-toolbars.md)e [Guida](winenv-help.md) vengono presentate in articoli distinti.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Le informazioni vengono visualizzate in base al passaggio del puntatore?** Se non è così, usa un altro controllo. Visualizza i suggerimenti solo in quanto il risultato dell'interazione utente non li visualizza mai autonomamente. Al contrario, i [palloni](ctrl-balloons.md) possono essere visualizzati in modo autonomo (come avviene con le notifiche), quindi hanno una coda che identifica la loro origine.
-   **Un controllo ha un'etichetta di testo?** Se non ne ha una, usa una descrizione comando per fornire l'etichetta. Si noti che la maggior parte dei controlli deve essere etichettata e pertanto non dispone di descrizioni comandi. I controlli della barra degli strumenti e i pulsanti di comando con etichette grafiche devono contenere descrizioni comandi.
-   **Un oggetto può trarre vantaggio da una descrizione supplementare o da ulteriori informazioni?** In caso affermativo, usare un infotip. Tuttavia, il testo deve essere supplementare, non essenziale per le attività primarie. Se è essenziale, inseriscilo direttamente nell'interfaccia utente, in modo che gli utenti non debbano trovarlo o andare alla ricerca di informazioni.
-   **Le informazioni aggiuntive sono un errore, un avviso o uno stato?** In tal caso, utilizzare un altro elemento dell'interfaccia utente, ad esempio un fumetto, un [messaggio di errore](mess-error.md)o una [barra di stato](ctrl-status-bars.md). L'icona dell'area di notifica infotip è un'eccezione perché può essere usata per visualizzare le informazioni sullo stato.
-   **Gli utenti devono interagire con la descrizione comando?** In tal caso, usare un altro controllo, ad esempio un fumetto. Gli utenti non possono interagire con le descrizioni comandi perché spostando il mouse spariscono.
-   **Gli utenti devono stampare le informazioni supplementari?** In tal caso, usare un altro controllo, ad esempio un campo di commento statico. Tuttavia, è anche possibile usare infotip per fornire un accesso più diretto a queste informazioni.

    ![screenshot del fumetto di commento ](images/ctrl-tooltips-and-infotips-image3.png)

    In questo esempio, un campo di commento statico in Microsoft Word consente agli utenti di stampare commenti.

-   **Il contesto in modo che gli utenti possano trovare i suggerimenti fastidiosi o distrae?** In tal caso, prendere in considerazione l'uso di un'altra soluzione, tra cui non eseguire alcuna operazione. Se si usano suggerimenti in questi contesti, consentire agli utenti di disattivarli.

Se utilizzate in modo appropriato, i suggerimenti migliorano la comunicazione con l'utente. **Non usare mai suggerimenti come sostituzioni per una progettazione corretta.** Se un elemento grafico, un pulsante o un altro oggetto richiede agli utenti di controllare un suggerimento per comprenderlo, la progettazione non è valida. Correggere invece la progettazione.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

I suggerimenti sono un potente strumento per semplificare un'interfaccia utente. Forniscono agli utenti le informazioni necessarie quando necessario, con un impegno minimo da parte dell'utente. I suggerimenti consentono di usare lo spazio dello schermo in modo più efficace e di ridurre il disordine dello schermo. Tuttavia, i suggerimenti progettati in modo non corretto possono essere fastidiosi, distrazioni, non aiutanti, travolgenti o nel loro modo. I concetti di progettazione seguenti hanno lo scopo di illustrare la differenza.

### <a name="discoverability"></a>Individuabilità

I suggerimenti vengono visualizzati automaticamente quando gli utenti posizionano il puntatore del mouse su un oggetto per un determinato periodo di tempo. Questo meccanismo di ritardo rende più convenienti i suggerimenti, ma riduce anche la loro individuabilità.

Nel corso del tempo, gli utenti apprendono che alcuni oggetti standard, come pulsanti della barra degli strumenti, pulsanti grafici, voci del menu Start e icone dell'area di notifica, presentano suggerimenti, quindi è possibile ottenere la loro individuabilità per l'autorizzazione.

Gli utenti sono più lunghi per individuare i suggerimenti nelle posizioni non standard. Non esiste alcun indizio visivo, ad esempio una modifica sensibile o un puntatore, che indica che un oggetto ha un suggerimento. Peggio ancora, alcuni utenti spostano il mouse intorno a molti, specialmente quando stanno imparando a navigare nell'interfaccia utente. Gli utenti devono tenere presente che un oggetto ha un suggerimento, tramite esperienza passata o sperimentazione.

È possibile migliorare l'individuabilità usando suggerimenti coerenti, che a sua volta favorisce la prevedibilità. Se si forniscono suggerimenti per alcuni oggetti, è necessario fornirli per tutti gli oggetti simili per cui è probabile che gli utenti desiderino informazioni aggiuntive. In alcuni casi può essere difficile, perché è necessario assicurarsi anche che i suggerimenti siano utili e non evidenti.

Se la fornitura di suggerimenti individuabili, sempre utili dimostra un problema, prendere in considerazione progettazioni alternative, ad esempio etichette di controllo autoesplicative o testo supplementare sul posto.

### <a name="appropriate-information"></a>Informazioni appropriate

Le informazioni appropriate per i suggerimenti hanno le caratteristiche seguenti:

-   **Conciso.** Le finestre popup usate da suggerimenti sono perfette per brevi frasi e frammenti di frasi, nonché per testo formattato. I blocchi di testo di grandi dimensioni e non formattati sono difficili da leggere e sopraffare.
-   **Utile.** Il testo del suggerimento deve essere informativo. Non dovrebbe essere ovvio o semplicemente ripetere gli elementi già presenti sullo schermo.
-   **Supplementare.** Poiché il testo del suggerimento non è sempre visibile, deve essere costituito da informazioni supplementari che non devono essere lette dagli utenti. Le informazioni importanti devono essere comunicate usando etichette di controllo autoesplicative o testo aggiuntivo sul posto.
-   **Statico.** Gli utenti non aspettano che i suggerimenti vengano modificati da un'istanza alla successiva, quindi è improbabile che si verifichino modifiche nel contenuto dinamico, ad esempio le informazioni sullo stato. I suggerimenti per le icone dell'area di notifica rappresentano un'eccezione notevole: è più probabile che gli utenti rilevino le modifiche nelle informazioni sulle mance, perché comunicano principalmente lo stato.

### <a name="appropriate-timeouts"></a>Timeout appropriati

La visualizzazione e la rimozione di suggerimenti appropriati sono fondamentali per consentire agli utenti di mantenere il controllo dell'ambiente dell'interfaccia utente. I suggerimenti hanno tre valori di timeout:

-   **Iniziale.** L'ora in cui il puntatore deve rimanere fermo affinché venga visualizzata la mancia. L'ora predefinita è 0,5 secondi.
-   **Reshow.** L'ora in cui il puntatore deve rimanere fermo perché il puntatore passa da una destinazione a un'altra. L'ora predefinita è 0,1 secondi.
-   **Rimozione.** Ora dopo la quale il suggerimento viene rimosso automaticamente. L'ora predefinita è 5 secondi.

La presenza di un valore iniziale troppo breve e di una rivisualizzazione dei valori comporta un'esperienza fastidioso e problematica, poiché viene spesso visualizzata inavvertitamente, mentre i suggerimenti non rispondono o non vengono individuati troppo a lungo. Il tempo di rimozione predefinito funziona correttamente per il testo della Mancia breve, come usato nelle descrizioni comandi. Il testo di infotip è più lungo, quindi sono necessari tempi di visualizzazione più lunghi.

### <a name="appropriate-placement"></a>Selezione host appropriata

I suggerimenti devono essere posizionati accanto all'oggetto spostato, in genere in corrispondenza della parte finale o della testa del puntatore, se possibile. Tuttavia, non dovrebbero mai essere posizionati in modo da interferire con le operazioni svolte dall'utente nascondendo l'oggetto di interesse. Per evitare questo problema potrebbe essere necessario spostare il suggerimento dall'indicatore di misura, ma adiacente all'oggetto. Non si tratta di un problema purché la relazione tra l'oggetto e il relativo suggerimento sia chiara. Assicurarsi che gli utenti non sposti il puntatore solo per fare in modo che i suggerimenti del programma vadano via.

### <a name="accessibility"></a>Accessibilità

I suggerimenti hanno un effetto insolito sull'accessibilità. Mentre vengono normalmente attivati passando il puntatore del mouse su un oggetto, i suggerimenti vengono gestiti dalle [utilità per la lettura dello schermo](inter-accessibility.md) per i controlli con accesso alla tastiera. Se utilizzate in modo appropriato per informazioni concise, utili, statiche e aggiuntive, i suggerimenti possono migliorare l'accessibilità complessiva. Infatti, il modello di suggerimento del testo alternativo è il modo migliore per rendere accessibile la grafica. Tuttavia, quando vengono usati in modo non appropriato, danneggiano l'accessibilità rendendo più difficile l'ottenimento di informazioni importanti o dinamiche.

Fornire più di un modo per accedere a un controllo se il controllo richiede un suggerimento che non dispone dell'accesso da tastiera.

![cattura di schermata del pulsante stampa con descrizione comando ](images/ctrl-tooltips-and-infotips-image4.png)

In questo esempio, gli utenti possono stampare usando il pulsante della barra degli strumenti (che non è accessibile dalla tastiera) o il tasto di scelta rapida da tastiera comando stampa.

**Se si esegue una sola operazione...**

Progetta suggerimenti individuabili che visualizzano informazioni aggiuntive concise, utili, statiche e aggiuntive nella posizione appropriata al momento opportuno.

## <a name="usage-patterns"></a>Modelli di utilizzo

I suggerimenti includono diversi modelli di utilizzo:



|                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Descrizioni comandi**<br/> Visualizza l'etichetta di un controllo o di un glifo senza etichetta. <br/>                                         | Poiché questi suggerimenti vengono usati come etichette, il testo segue le linee guida per le etichette per il controllo sottostante. <br/> ![screenshot del pulsante Esporta elenco con descrizione comando ](images/ctrl-tooltips-and-infotips-image5.png)<br/> in questo esempio la descrizione comando fornisce l'etichetta del comando.<br/> ![cattura di schermata del pulsante Chiudi con la descrizione comando ](images/ctrl-tooltips-and-infotips-image6.png)![screenshot del pulsante Riproduci con descrizione comando ](images/ctrl-tooltips-and-infotips-image7.png)<br/> in questi esempi, le descrizioni comando etichettano i pulsanti grafici.<br/> ![screenshot del glifo del menu Mostra con descrizione comando ](images/ctrl-tooltips-and-infotips-image8.png)<br/> In questo esempio la descrizione comando contrassegna un glifo.<br/> |
| **Infotip**<br/> fornire una descrizione o una spiegazione aggiuntiva di un oggetto o di un controllo. <br/>                  | Usare infotip per descrivere o spiegare gli oggetti e i controlli, ad esempio i controlli della [barra degli strumenti](cmd-toolbars.md) , le [Icone](vis-icons.md) , incluse le sovrapposizioni di icone, i [collegamenti](ctrl-links.md), le [schede](ctrl-tabs.md), i [controlli di divulgazione progressiva](ctrl-progressive-disclosure-controls.md)e i controlli personalizzati. <br/> ![screenshot del pulsante di posta elettronica con infotip ](images/ctrl-tooltips-and-infotips-image9.png)<br/> ![cattura di schermata del pulsante Burn con infotip ](images/ctrl-tooltips-and-infotips-image10.png)<br/> In questi esempi, infotip forniscono informazioni aggiuntive sui controlli e sugli oggetti.<br/>                                                                                        |
| **Infotip testo alternativo**<br/> descrivere un elemento grafico per l'accessibilità. <br/>                                              | Questo modello è destinato principalmente agli utenti che hanno una qualche forma di problemi di visione e potrebbero usare un'operazione di lettura dello schermo. <br/> ![screenshot del pulsante Start di Windows con infotip ](images/ctrl-tooltips-and-infotips-image11.png)<br/> In questo esempio, infotip descrive la grafica del menu Start.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Anteprima**<br/> Visualizza un'immagine di dimensioni ridotte di un elemento. <br/>                                                         | Le anteprime offrono una rappresentazione grafica facilmente riconoscibile di una finestra o di un documento. <br/> ![screenshot dell'anteprima delle categorie del pannello di controllo ](images/ctrl-tooltips-and-infotips-image12.png)<br/> in questo esempio, la barra delle applicazioni di Windows fornisce suggerimenti per l'anteprima per gli elementi.<br/> ![screenshot dell'anteprima della foto e dei relativi dati ](images/ctrl-tooltips-and-infotips-image13.png)<br/> In questo esempio, raccolta foto di Windows offre suggerimenti per l'anteprima per gli elementi.<br/>                                                                                                                                                                                                                      |
| **Dettagli infotip**<br/> Visualizza informazioni dettagliate su un oggetto. <br/>                                        | Infotip rappresentano un modo efficace per visualizzare informazioni dettagliate su un oggetto o per fornire dati. <br/> ![screenshot della infotip della foto che mostra il tipo di file ](images/ctrl-tooltips-and-infotips-image14.png)![screenshot del grafo con i valori dettagliati infotip ](images/ctrl-tooltips-and-infotips-image15.png)<br/> In questi esempi, infotip forniscono informazioni dettagliate su un oggetto o sui dati.<br/>                                                                                                                                                                                                                                                                                                      |
| **Menu Start infotip**<br/> descrivere un elemento nel menu Start. <br/>                                              | Il menu Start è costituito da nomi di programma e destinazioni di Windows importanti, ad esempio documenti, immagini e pannello di controllo. questi suggerimenti descrivono le voci del menu Start, in genere fornendo una breve descrizione del programma o della destinazione e delle attività primarie che gli utenti possono eseguire. Queste descrizioni sono indicizzate anche dalla casella di ricerca del menu Start, per aiutare gli utenti a trovare i programmi necessari. <br/> ![screenshot del centro di benvenuto infotip ](images/ctrl-tooltips-and-infotips-image16.png)<br/> In questo esempio, infotip descrive le operazioni che gli utenti possono eseguire con un programma nel menu Start.<br/>                                                                                    |
| **Pannello di controllo infotip**<br/> descrivere una categoria o un'attività del pannello di controllo. <br/>                                    | Questi suggerimenti forniscono informazioni aggiuntive per aiutare gli utenti a scegliere la categoria e l'elemento del pannello di controllo corretti. <br/> ![screenshot della categoria degli account utente con infotip ](images/ctrl-tooltips-and-infotips-image17.png)<br/> In questo esempio, infotip descrive la categoria del pannello di controllo degli account utente.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| **Nome completo infotip**<br/> visualizzare il nome completo di un elemento quando il nome viene troncato o non è completamente visibile. <br/> | Questi suggerimenti consentono di visualizzare gli elementi in uno spazio più compatto, riducendo al tempo stesso la necessità di scorrimento orizzontale. Questo è particolarmente importante quando la lunghezza del contenuto è sconosciuta perché è dinamica. Diversamente dagli altri criteri, quando vengono usati negli elenchi e negli alberi, questi suggerimenti vengono visualizzati direttamente sull'oggetto di origine. <br/> ![screenshot del gruppo di pulsanti di opzione-title infotip ](images/ctrl-tooltips-and-infotips-image18.png)<br/> In questo esempio viene usato un infotip per visualizzare il nome dell'elemento completo al passaggio del mouse.<br/>                                                                                                                                                                                     |
| **Stato infotip**<br/> visualizzare le informazioni sullo stato per le icone dell'area di notifica. <br/>                              | In genere, i suggerimenti devono essere statici perché gli utenti non si aspettano di passare da un'istanza a quella successiva. le **Icone dell'area di notifica rappresentano un'eccezione** perché queste icone comunicano lo stato e non è disponibile altro spazio sullo schermo per il testo dello stato. <br/> ![Screenshot di "Messenger non firmato" infotip ](images/ctrl-tooltips-and-infotips-image19.png)<br/> ![Screenshot di "Messenger signed in" infotip ](images/ctrl-tooltips-and-infotips-image20.png)<br/> In questi esempi, infotip fornisce informazioni sullo stato per le icone dell'area di notifica.<br/>                                                                                                                                  |



 

## <a name="guidelines"></a>Indicazioni

### <a name="timeouts"></a>Timeout

-   **Usare i timeout predefiniti iniziali e di rivisualizzazione. Eccezione**
    -   Le anteprime che non sono ridondanti e visualizzate sul lato dell'oggetto associato possono essere visualizzate immediatamente (senza ritardi). Tuttavia, usare il timeout iniziale predefinito per le anteprime ridondanti, ad esempio una grande mancia per un piccolo oggetto grafico, o anteprime che coprono l'oggetto associato.
-   **Per le descrizioni comandi, utilizzare il timeout di rimozione del suggerimento predefinito di cinque secondi.**
-   **Per infotip, disattivare il timeout di rimozione del suggerimento. Sviluppatori:** poiché non è tecnicamente possibile disattivare il timeout di rimozione, impostarlo sul valore più grande.
-   Per l'accessibilità, se è necessario impostare i valori di timeout su un valore diverso da quello massimo, renderli multipli dei \_ parametri di sistema SPI GETMOUSEHOVERTIME e SPI \_ GETMESSAGEDURATION anziché usare orari fissi. Questa operazione consente di adattare i timeout alla velocità dell'utente.

### <a name="placement"></a>Selezione host

-   **Evitare di coprire l'oggetto con cui l'utente sta per visualizzare o interagire.** Posizionare sempre il suggerimento sul lato dell'oggetto, anche se è necessaria la separazione tra il puntatore e il suggerimento. Una separazione non è un problema, purché la relazione tra l'oggetto e il relativo suggerimento sia chiara.

    -   **Eccezione:** Descrizioni comandi con nome completo utilizzati negli elenchi e negli alberi.

    **Non corretto:**

    ![screenshot della casella di ricerca infotip obscuring ](images/ctrl-tooltips-and-infotips-image21.png)

    **Corretto:**

    ![Screenshot di infotip posizionata sotto la casella di ricerca ](images/ctrl-tooltips-and-infotips-image22.png)

    Nell'esempio corretto, il infotip viene disposto dalla casella di ricerca, anche se è necessario spazio tra il punto di inserimento e il punto di inserimento.

    **Non corretto:**

    ![Screenshot di infotip che oscura il testo modificato ](images/ctrl-tooltips-and-infotips-image23.png)

    **Corretto:**

    ![Screenshot di infotip posizionata sopra il testo modificato ](images/ctrl-tooltips-and-infotips-image24.png)

    Nell'esempio corretto, il testo sottostante è molto più utile del suggerimento, quindi la infotip viene posizionata correttamente.

-   **Per le raccolte di elementi, evitare di coprire l'oggetto successivo che è probabile che l'utente possa visualizzare o interagire con.** Per gli elementi disposti orizzontalmente, evitare di posizionare i suggerimenti a destra; per gli elementi disposti verticalmente, evitare di inserire i suggerimenti seguenti.

    **Non corretto:**

    ![screenshot dell'elenco di elementi recenti di infotip obscuring ](images/ctrl-tooltips-and-infotips-image25.png)

    **Corretto:**

    ![Screenshot di infotip accanto all'elenco degli elementi recenti ](images/ctrl-tooltips-and-infotips-image26.png)

    Nell'esempio errato, il suggerimento riguarda l'oggetto che l'utente con maggiore probabilità interagirà con Next.

-   **Per i suggerimenti potenzialmente dispersivi (spesso grandi), assicurarsi che le informazioni siano utili per la maggior parte degli utenti.** In caso contrario, rendere i suggerimenti distrattivi facoltativi o addirittura eliminarli. In caso contrario, la maggior parte degli utenti dovrà spostare il puntatore dall'oggetto di destinazione per eliminare il suggerimento.

### <a name="tooltips"></a>Descrizioni comando

-   **Usare le descrizioni comandi per fornire etichette per i controlli senza etichetta.** I controlli che in genere dispongono di descrizioni comandi sono [pulsanti della barra degli strumenti](cmd-toolbars.md), pulsanti grafici e [controlli di divulgazione progressiva](ctrl-progressive-disclosure-controls.md). I controlli con i prompt vengono considerati etichettati, ad esempio [caselle di testo](ctrl-text-boxes.md) e [caselle combinate](/windows/desktop/uxguide/ctrl-drop). Tutti gli altri controlli devono avere etichette esplicite.
-   Usare frammenti di frase senza punteggiatura finale.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
    -   **Eccezione:** Questa guida è una novità di Windows Vista. Per le applicazioni legacy, è possibile usare l'uso di maiuscole in stile titolo, se necessario, per evitare di combinare stili di maiuscole.
-   Aggiungere i [puntini](ctrl-command-buttons.md) di sospensione se l'etichetta è per un comando che richiede informazioni aggiuntive.
-   Come per le etichette normali, le **descrizioni comando mantengono brevi** in genere cinque parole o meno, ma preferiscono etichette specifiche rispetto a quelle vaghe.

    **Accettabile:**

    ![screenshot della descrizione comando di stampa ](images/ctrl-tooltips-and-infotips-image27.png)

    **Migliore:**

    ![screenshot della descrizione comando ' stampa su stampante predefinità ](images/ctrl-tooltips-and-infotips-image28.png)

    **Consigliate**

    ![screenshot della descrizione comando ' stampa (Document Writer)' ](images/ctrl-tooltips-and-infotips-image29.png)

    **Non corretto:**

    ![screenshot della descrizione comando dettagliata ](images/ctrl-tooltips-and-infotips-image30.png)

    In questi esempi, l'esempio migliore è conciso e specifico, mentre l'esempio errato è inutilmente dettagliato.

-   **Le descrizioni comandi possono inoltre fornire maggiori dettagli per i pulsanti della barra degli strumenti con etichetta se questa operazione è utile.** Non solo ripetere o fornire una riformulazione di parole in cui si trova già nell'etichetta.

    **Corretto:**

    ![screenshot della descrizione comando ' Cerca tutto Outlook ' ](images/ctrl-tooltips-and-infotips-image31.png)

    In questo esempio, la descrizione comando illustra il risultato della ricerca.

    **Non corretto:**

    ![screenshot dell'etichetta del pulsante ripetuto della descrizione comando ](images/ctrl-tooltips-and-infotips-image32.png)

    In questo esempio la descrizione comando ripete semplicemente ciò che è già presente nell'etichetta.

-   **Non è necessario assegnare descrizioni comandi con etichetta semplicemente per motivi di coerenza.**

    ![screenshot dei pulsanti con etichetta e senza etichetta ](images/ctrl-tooltips-and-infotips-image33.png)

    In questo esempio, i pulsanti della barra degli strumenti senza etichetta hanno descrizioni comandi, ma non quelli con etichetta.

-   Quando appropriato, **rendere più utili le descrizioni comando fornendo i tasti di scelta rapida e i valori predefiniti.** Inserire queste informazioni aggiuntive tra parentesi. In questo modo, le descrizioni comandi risultano utili per i controlli con etichetta anche quando altrimenti ripeteranno semplicemente l'etichetta. Non considerare questo testo aggiuntivo quando si valuta la concisità di una descrizione comando.

    ![screenshot della descrizione comando ' stampa (Document Writer)' ](images/ctrl-tooltips-and-infotips-image29.png)

    In questo esempio, in Word vengono visualizzati i valori predefiniti e i tasti di scelta rapida nelle descrizioni comandi della barra degli strumenti.

### <a name="infotips"></a>Infotip

-   **Per infotip in posizioni non standard, prediligere la coerenza rispetto all'utilità per migliorare l'individuabilità.** Fornire suggerimenti per tutti gli oggetti per cui è probabile che gli utenti desiderino informazioni aggiuntive, anche se alcune infotip potrebbero essere ovvie. In questo modo si evita che gli utenti attendano un infotip che non verrà mai fatto.
    -   **Eccezione:** Se solo pochi oggetti hanno infotip utili, non usare infotip. Usare invece etichette di controllo con spiegazione automatica o testo aggiuntivo sul posto.
-   Utilizzare frasi complete con la punteggiatura finale.
    -   **Eccezione:** Icona dell'area di notifica [infotip](winenv-notification.md) non usare la punteggiatura finale.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Usare il tempo presente e non futuro.
-   Usare costruzioni grammaticali parallele. Il parallelismo richiede che le parole e le frasi con la stessa funzione abbiano lo stesso formato.
    -   **Eccezione:** Per il modello infotip completo, il testo infotip corrisponde esattamente alla formulazione, alle maiuscole e alla punteggiatura del controllo sottostante.
-   **Evitare infotip di grandi dimensioni.** Infotip di grandi dimensioni sono difficili da leggere e difficili da posizionare senza interferire con l'oggetto sottostante.
-   **Formattare infotip per semplificare la lettura e l'analisi dei contenuti.** Un blocco di testo non formattato può essere difficile da leggere.

    **Non corretto:**

    ![screenshot della descrizione comando run-on lunga, non strutturata ](images/ctrl-tooltips-and-infotips-image34.png)

    **Corretto:**

    ![screenshot della stessa descrizione comando con una riga per ogni elemento ](images/ctrl-tooltips-and-infotips-image35.png)

    Nell'esempio corretto, il testo formattato è molto più semplice da leggere e analizzare.

-   Al primo utilizzo all'interno di un infotip, digitare i nomi degli acronimi, seguiti dall'acronimo tra parentesi. Esempio: "Dynamic Host Configuration Protocol (DHCP)".

### <a name="start-menu-infotips"></a>Menu Start infotip

-   Usare il menu Start infotip per **descrivere l'elemento in modo conciso ed elencare le attività primarie che gli utenti possono eseguire con l'elemento.**
-   **Essere utile.** Concentrarsi sulle operazioni che gli utenti possono eseguire. Non solo ripetere il nome dell'elemento o usarlo nella descrizione.
-   **Essere specifici.** Evitare verbi generici e frasi catch-all come e altre attività. Se le informazioni sono importanti, elencarle in modo specifico; in caso contrario, si supponga che gli utenti capiscano che non tutti gli elementi sono elencati nella infotip.
-   **Essere concisi.** Usare meno di 25 parole. Lettura più lunga di infotip sconsigliata.
-   **Iniziare con un verbo imperativo e presente,** ad esempio creare, modificare, mostrare e inviare. Preferisce verbi specifici su verbi generici, ad esempio gestione e apertura, che si applicano effettivamente alla maggior parte delle voci di menu Start. Vai direttamente al punto.

    **Non corretto:**

    ![screenshot della descrizione comando: apre la cartella Music ](images/ctrl-tooltips-and-infotips-image36.png)

    **Migliore:**

    ![screenshot della descrizione comando: archiviare e riprodurre musica ](images/ctrl-tooltips-and-infotips-image37.png)

    Nell'esempio errato, infotip inizia con un verbo generico. L'esempio migliore è quello con i verbi specifici, ma continua a usare il formulazione "e l'altro" superfluo alla fine del suggerimento.

-   **Non usare un linguaggio che suoni come il marketing.**

    **Non corretto:**

    ![screenshot del punto di partenza "One-Stop" infotip ](images/ctrl-tooltips-and-infotips-image38.png)

    In questo esempio, il infotip suona come marketing.

-   Poiché questi infotip sono indicizzati per la casella di ricerca del menu Start, **descrivono le attività importanti del programma usando i termini per i quali è più probabile che gli utenti cerchino. Si consiglia di usare parole chiave e sinonimi comuni.**

    **Non corretto:**

    ![screenshot della descrizione comando: creare DVD ](images/ctrl-tooltips-and-infotips-image39.png)

    **Corretto:**

    ![screenshot della descrizione comando: creare (masterizzare) CDS, DVD ](images/ctrl-tooltips-and-infotips-image40.png)

    Nell'esempio corretto, infotip presenta sinonimi comuni.

-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   **Sviluppatori:** Il menu Start infotip text deriva dal campo Comment dell'elemento.

### <a name="quick-launch-tooltips"></a>Descrizioni comandi di avvio veloce

-   **Usare una descrizione comando con il formato seguente:** Launch (nome completo del programma)
-   Non usare punteggiatura finale.
-   Non usare testo aggiuntivo per descrivere il programma o il relativo funzionamento. Poiché gli utenti scelgono i programmi visualizzati nella barra di avvio veloce, ne conoscono già lo scopo.

### <a name="control-panel-infotips"></a>Pannello di controllo infotip

-   Usare il pannello di controllo infotip per **descrivere brevemente le attività del pannello di controllo e l'hardware e il software configurati.**
-   **I nomi e le icone del pannello di controllo devono contenere infotip.** Le singole attività non dispongono di descrizioni comandi.
-   **Essere utile.** Concentrarsi sulle operazioni che gli utenti possono eseguire. Non ripetere semplicemente il nome dell'elemento del pannello di controllo o anche usarlo nella descrizione.
-   **Essere specifici.** Evitare verbi generici e frasi catch-all come e altri componenti hardware. Se le informazioni sono importanti, elencarle in modo specifico; in caso contrario, si supponga che gli utenti capiscano che non tutti gli elementi sono elencati nella infotip.

    **Non corretto:**

    ![screenshot della descrizione comando: configura il mouse ](images/ctrl-tooltips-and-infotips-image41.png)

    **Corretto:**

    ![screenshot della descrizione comando dettagliata per le impostazioni del mouse ](images/ctrl-tooltips-and-infotips-image42.png)

    Nell'esempio corretto, i tipi di hardware configurati sono elencati in modo specifico.

-   **Essere concisi.** Usare meno di 25 parole. Lettura più lunga di infotip sconsigliata.
-   **Inizia con un verbo imperativo presente.**

    **Corretto:**

    Configurare le impostazioni di connessione e visualizzazione Internet.

    Modificare le impostazioni per la visione, l'udito e la mobilità.

-   **Vai direttamente al punto.** Non usare il linguaggio applicabile a qualsiasi pannello di controllo, ad esempio "usare per visualizzare e configurare le impostazioni per l'aspetto e la funzionalità del..." o "fornisce opzioni da..."
-   Non usare un linguaggio che suoni come il marketing.

    **Non corretto:**

    Il punto di partenza unico per tutte le esigenze di configurazione dei dischi.

-   Poiché questi infotip sono indicizzati per la casella di ricerca del pannello di controllo, **descrivere gli elementi usando i termini per i quali è più probabile che gli utenti cerchino.** Considerare l'uso di sinonimi comuni per le attività e gli oggetti più diffusi.

    ![screenshot della descrizione comando con attività del controller di gioco ](images/ctrl-tooltips-and-infotips-image43.png)

    In questo esempio, l'elemento viene descritto usando i termini per i quali è più probabile che gli utenti cerchino.

-   Se è probabile che un elemento del pannello di controllo sia confuso con altri, spiegare come è diverso nella infotip.

    **Non corretto:**

    ![Screenshot di infotip privo di dettagli specifici ](images/ctrl-tooltips-and-infotips-image44.png)

    In questo esempio, entrambi gli elementi del pannello di controllo configurano il suono, ma infotip non chiarisce la differenza.

    **Corretto:**

    ![Screenshot di infotip con dettagli specifici ](images/ctrl-tooltips-and-infotips-image45.png)

    In questo esempio, la differenza tra i due elementi è più evidente a causa del suggerimento.

### <a name="icons"></a>Icone

Diversamente dalle versioni precedenti di Windows, Windows Vista consente ai suggerimenti di avere icone.

-   Per le descrizioni comandi, non usare le icone.
-   Per infotip, usare le icone solo se facilitano il riconoscimento o la comprensione o forniscono il contesto. La maggior parte dei infotip non deve avere icone.

    ![screenshot del volume infotip con icona a cuffia ](images/ctrl-tooltips-and-infotips-image46.png)

    In questo esempio, infotip dispone di un'icona che consente di associare l'icona al suo significato.

-   L'icona deve usare il [tipo Aero](vis-icons.md) e avere un aspetto non intrusivo.

Per le linee guida e gli esempi dell'icona generale, vedere [Icone](vis-icons.md).

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai suggerimenti:

-   In programmazione e in altra documentazione tecnica, fare riferimento al tipo di suggerimento (descrizione comando o infotip). Ovunque, è sufficiente chiamare un suggerimento.
-   Le varianti seguenti non sono corrette: descrizione comando, descrizione comando e descrizione comando.
-   Per descrivere l'interazione dell'utente, usare il puntatore del mouse.

