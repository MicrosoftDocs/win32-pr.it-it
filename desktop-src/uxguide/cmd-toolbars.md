---
title: Barre degli strumenti
description: Le barre degli strumenti rappresentano un modo per raggruppare i comandi per un accesso efficiente.
ms.assetid: 8f36307c-54fc-493d-a2ff-57db29e3508d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: bb32c84f6090bc25b985b8445fb351a478c24c2b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104568539"
---
# <a name="toolbars"></a>Barre degli strumenti

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Le barre degli strumenti rappresentano un modo per raggruppare i comandi per un accesso efficiente.

![Screenshot di due barre degli strumenti con elementi con etichetta ](images/cmd-toolbars-image1.png)

Alcune barre degli strumenti tipiche.

**Utilizzare le barre degli strumenti oltre al o al posto delle barre dei menu.** Le barre degli strumenti possono essere più efficienti delle barre dei menu perché sono dirette (sempre visualizzate anziché visualizzate al clic del mouse), immediate (anziché richiedere input aggiuntivi) e contengono i comandi usati più di frequente (anziché un elenco completo). Diversamente dalle barre dei menu, le barre degli strumenti non devono necessariamente essere complete o autoesplicative solo in modo rapido, pratico ed efficiente.

Alcune barre degli strumenti sono personalizzabili, consentendo agli utenti di aggiungere o rimuovere barre degli strumenti, modificarne le dimensioni e la posizione e persino modificarne il contenuto. Alcuni tipi di barre degli strumenti possono essere disancorati, ottenendo una finestra della tavolozza. Per altre informazioni sulle varietà della barra degli strumenti, vedere [modelli di utilizzo](#usage-patterns) in questo articolo.

> [!Note]  
> Le linee guida relative a [menu](cmd-menus.md), [pulsanti di comando](ctrl-command-buttons.md)e [Icone](vis-icons.md) sono presentate in articoli distinti.

 

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendi in considerazione queste domande:

-   **La finestra è una finestra primaria?** Le barre degli strumenti funzionano correttamente per le finestre primarie, ma sono in genere sovraccaricate per le finestre secondarie. Per le finestre secondarie, usare i [pulsanti di comando](ctrl-command-buttons.md), i [pulsanti di menu](ctrl-command-buttons.md)e i [collegamenti](ctrl-command-links.md) .
-   **Sono presenti un numero ridotto di comandi usati di frequente?** Le barre degli strumenti non possono gestire il numero di comandi delle barre dei menu, quindi funzionano meglio per accedere in modo efficiente a un numero ridotto di comandi usati di frequente.
-   **La maggior parte dei comandi è immediata?** Ovvero sono principalmente comandi che non richiedono input aggiuntivo? Per una maggiore efficienza, le barre degli strumenti devono avere un'idea diretta e immediata. In caso contrario, le barre dei menu sono più adatte per i comandi che richiedono input aggiuntivo.
-   **La maggior parte dei comandi può essere presentata direttamente?** Ovvero, gli utenti interagiscono con loro usando un solo clic? Mentre alcuni comandi possono essere presentati usando i pulsanti di menu, presentando la maggior parte dei comandi in questo modo, si riduce l'efficienza della barra degli strumenti, rendendo una barra dei menu una scelta migliore.
-   **I comandi sono ben rappresentati dalle icone?** I pulsanti della barra degli strumenti sono in genere rappresentati da icone anziché da etichette di testo (sebbene alcuni pulsanti della barra degli strumenti usino entrambi), mentre i comandi di menu sono rappresentati dal testo. Se le icone del comando non sono di qualità elevata e non sono esplicative, una barra dei menu può essere la scelta migliore.

Se il programma dispone di una barra degli strumenti senza una barra dei menu e la maggior parte dei comandi è accessibile indirettamente tramite pulsanti di menu e pulsanti di menu [combinato](ctrl-command-buttons.md), questa barra degli strumenti è essenzialmente una barra dei menu. Applicare il modello di [menu della barra degli strumenti](cmd-menus.md) nelle linee guida dei menu.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Una barra dei menu valida è un catalogo completo di tutti i comandi di primo livello disponibili, mentre una barra degli strumenti valida consente un accesso rapido e pratico ai comandi usati di frequente. Una barra degli strumenti non tenta di eseguire il training degli utenti. Una volta che gli utenti apprenderanno come accedere a un comando su una barra degli strumenti, continuano raramente ad accedere al comando dalla barra dei menu. Per questi motivi, non è necessario che la barra dei menu di un programma e la relativa barra degli strumenti corrispondano direttamente.

### <a name="toolbars-vs-menu-bars"></a>Barre degli strumenti e barre dei menu

Tradizionalmente, le barre degli strumenti sono diverse dalle barre dei menu nei modi seguenti:

-   **Frequenza.** Le barre degli strumenti presentano solo i comandi usati più di frequente, mentre le barre dei menu catalogano tutti i comandi di primo livello disponibili all'interno di un programma.
-   **Immediatezza.** Quando si fa clic su un comando della barra degli strumenti, viene applicato immediatamente un comando di menu, che potrebbe richiedere input aggiuntivo. Ad esempio, un comando stampa in una barra dei menu Visualizza prima di tutto la finestra di dialogo Stampa, mentre un pulsante della barra degli strumenti stampa stampa immediatamente una singola copia di un documento sulla stampante predefinita.

    ![screenshot del pulsante della stampante della barra degli strumenti selezionato ](images/cmd-toolbars-image2.png)

    In questo esempio, facendo clic sul pulsante della barra degli strumenti stampa viene immediatamente stampata una singola copia di un documento sulla stampante predefinita.

-   **Immediatezza.** I comandi della barra degli strumenti vengono richiamati con un solo clic, mentre i comandi della barra dei menu richiedono lo spostamento nel menu.
-   **Numero e densità.** Lo spazio dello schermo richiesto da una barra degli strumenti è proporzionale al numero di comandi e tale spazio viene sempre usato, anche se i comandi non lo sono. Di conseguenza, le barre degli strumenti devono utilizzare lo spazio in modo efficiente. Al contrario, i comandi della barra dei menu sono normalmente nascosti dalla visualizzazione e la struttura gerarchica consente un numero qualsiasi di comandi.
-   **Dimensioni e presentazione.** Per comprimere molti comandi in uno spazio ridotto, le barre degli strumenti utilizzano in genere comandi basati su icone (con etichette basate su descrizioni comandi), mentre le barre dei menu utilizzano comandi basati su testo (con icone facoltative). Anche se i pulsanti della barra degli strumenti possono avere etichette di testo standard, questi utilizzano molto più spazio.

    ![screenshot della barra degli strumenti con etichetta trasmissione/ricezione ](images/cmd-toolbars-image3.png)

    I pulsanti della barra degli strumenti con etichetta accettano almeno tre volte lo stesso spazio di quelli senza etichetta.

-   **Spiegazione automatica.** Per le barre degli strumenti ben progettate è necessario avere icone per la maggior parte intuitive perché gli utenti non riescono a trovare i comandi in modo efficiente solo usando le descrizioni comandi Tuttavia, le barre degli strumenti continuano a funzionare correttamente se alcuni comandi usati meno di frequente non sono di chiara interpretazione.

    ![screenshot della barra degli strumenti con icone note ](images/cmd-toolbars-image4.png)

    In questo esempio, le icone utilizzate più di frequente sono di chiara interpretazione.

-   **Riconoscibile e distinguibili.** Per i comandi usati di frequente, gli utenti ricordano gli attributi dei pulsanti della barra degli strumenti come posizione, forma e colore. Con le barre degli strumenti ben progettate, gli utenti possono trovare rapidamente i comandi anche se non ricordano il simbolo esatto dell'icona. Al contrario, gli utenti ricordano i percorsi dei comandi della barra dei menu usati di frequente, ma si basano sulle etichette dei comandi per effettuare le selezioni.

    ![screenshot della finestra di dialogo Opzioni dello strumento di cattura ](images/cmd-toolbars-image5.png)

    Per i comandi della barra degli strumenti, la posizione distinta, la forma e il colore contribuiscono a rendere le icone riconoscibili e distinguibili.

    ![screenshot della barra dei menu con comando file selezionato ](images/cmd-toolbars-image6.png)

    Per i comandi della barra dei menu, gli utenti dipendono infine dalle etichette.

### <a name="efficiency"></a>Efficienza

Date le relative caratteristiche, le barre degli strumenti devono essere progettate principalmente per migliorare l'efficienza. Una barra degli strumenti poco efficiente non ha alcun significato.

**Se si esegue una sola operazione...**

Assicurarsi che le barre degli strumenti siano progettate principalmente per migliorare l'efficienza. Attiva le barre degli strumenti sui comandi utilizzati di frequente, immediate, dirette e riconoscibili rapidamente.

### <a name="hiding-menu-bars"></a>Nascondere le barre dei menu

In genere, le barre degli strumenti funzionano perfettamente insieme alle barre dei menu: le barre degli strumenti valide forniscono efficienza e le barre dei menu ottimali forniscono la completezza. **La presenza di barre dei menu e barre degli strumenti consente a ognuno di concentrarsi sui propri punti di forza senza compromessi.**

Sorprendentemente, questo modello si interrompe con semplici programmi. Per i programmi con pochi comandi, la presenza di una barra dei menu e una barra degli strumenti non ha senso perché la barra dei menu è una versione ridondante e inefficiente della barra degli strumenti.

Per eliminare questa ridondanza, molti programmi semplici in Windows Vista si concentrano sull'invio di comandi esclusivamente tramite la barra degli strumenti e sulla barra dei menu per impostazione predefinita. Tali programmi includono Esplora risorse, Windows Internet Explorer, Windows Media Player e raccolta foto di Windows.

Non si tratta di modifiche minime. Rimuovendo la barra dei menu si modifica in modo sostanziale la natura delle barre degli strumenti perché tali barre degli strumenti devono essere complete e modificare nei modi seguenti:

-   **Frequenza.** La rimozione della barra dei menu significa che tutti i comandi non disponibili direttamente da una finestra o dai relativi menu di scelta rapida devono essere accessibili dalla barra degli strumenti, indipendentemente dalla relativa frequenza d'uso.
-   **Immediatezza.** Rimuovendo la barra dei menu, la barra degli strumenti è l'unico punto di accesso visibile per i comandi, che richiede che la barra degli strumenti abbia le versioni completamente funzionali. Se, ad esempio, non è presente alcuna barra dei menu, un comando stampa su una barra degli strumenti deve visualizzare la finestra di dialogo Stampa anziché immediatamente stampa. (Anche se l'uso di un pulsante combinato è un ottimo compromesso in questo caso. Per il pulsante di suddivisione standard stampa, vedere [menu standard e pulsanti di menu combinato](#standard-menu-and-split-buttons) .

    ![screenshot della barra degli strumenti e delle opzioni del comando stampa ](images/cmd-toolbars-image7.png)

    In questo esempio, il pulsante della barra degli strumenti di stampa in raccolta foto di Windows include un comando stampa che consente di visualizzare la finestra di dialogo Stampa.

-   **Immediatezza.** Per risparmiare spazio ed evitare confusione, i comandi usati meno di frequente possono essere spostati in pulsanti di menu, rendendoli meno diretti.

Le barre degli strumenti utilizzate per integrare una barra dei menu sono progettate in modo diverso rispetto alle barre degli strumenti progettate per l'utilizzo con una barra dei menu rimossa o nascosta. Poiché non è possibile presupporre che gli utenti visualizzino una barra dei menu nascosta per eseguire un singolo comando, nascondere una barra dei menu deve essere considerata come la rimozione completa quando si prendono decisioni di progettazione. Se per impostazione predefinita si nasconde la barra dei menu, non presupporre che gli utenti penseranno di visualizzare la barra dei menu per trovare un comando o anche scoprire come visualizzarlo.

La progettazione di una barra degli strumenti per lavorare senza una barra dei menu spesso implica alcuni compromessi. Tuttavia, per migliorare l'efficienza, non compromettere eccessivamente. Se la barra dei menu viene nascosta in una barra degli strumenti non efficiente, non nascondere la barra dei menu.

### <a name="keyboard-accessibility"></a>Accessibilità tramite tastiera

Dalla tastiera, l'accesso alle barre degli strumenti è piuttosto diverso dall'accesso alle barre dei menu. Le barre dei menu ricevono lo stato attivo per l'input quando gli utenti preme il tasto ALT e perdono lo stato attivo per l'input con il tasto ESC. Quando una barra dei menu ha lo stato attivo per l'input, viene spostata indipendentemente dal resto della finestra, gestendo tutti i tasti di direzione, Home, fine e tabulazione. Al contrario, le barre degli strumenti ricevono lo stato attivo per l'input quando gli utenti preme il tasto TAB per l'intero contenuto della finestra. Poiché le barre degli strumenti sono le ultime in base all'ordine di tabulazione, possono richiedere un notevole sforzo per l'attivazione in una pagina occupata, a meno che gli utenti non sappiano di usare MAIUSC + TAB per spostarsi all'indietro.

L'accessibilità presenta un dilemma: Sebbene le barre degli strumenti siano più semplici per gli utenti del mouse, sono meno accessibili per gli utenti della tastiera. Questo non è un problema se è presente una barra dei menu e una barra degli strumenti, ma è se la barra dei menu viene rimossa o nascosta.

Per motivi di accessibilità, è preferibile mantenere la barra dei menu anziché rimuoverla completamente a favore di una barra degli strumenti. Se è necessario scegliere tra rimuovere la barra dei menu e nasconderla semplicemente, è preferibile nasconderla.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le barre degli strumenti hanno diversi modelli di utilizzo:



|                                                                                                                      |                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barre degli strumenti primarie**<br/> barra degli strumenti progettata per funzionare senza una barra dei menu, nascosta o rimossa. <br/> | le barre degli strumenti primarie devono bilanciare la necessità di efficienza con la completezza, quindi funzionano meglio per i programmi semplici. <br/> ![screenshot della barra degli strumenti di Esplora risorse ](images/cmd-toolbars-image8.png)<br/> Barra degli strumenti principale di Esplora risorse.<br/>                                                                        |
| **Barre degli strumenti supplementari**<br/> barra degli strumenti progettata per funzionare con una barra dei menu. <br/>                         | le barre degli strumenti aggiuntive possono concentrarsi sull'efficienza senza compromessi. <br/> ![Screenshot di una barra dei menu su una barra degli strumenti ](images/cmd-toolbars-image9.png)<br/> Una barra degli strumenti supplementare di Windows Movie Maker.<br/>                                                                                                                  |
| **Menu della barra degli strumenti**<br/> barra dei menu implementata come barra degli strumenti. <br/>                                        | i menu della barra degli strumenti sono barre degli strumenti costituite principalmente da comandi nei [pulsanti di menu](ctrl-command-buttons.md) e pulsanti di menu combinato, con solo pochi comandi diretti, se presenti. <br/> ![screenshot della barra dei menu con icone e comandi ](images/cmd-toolbars-image10.png)<br/> Menu della barra degli strumenti nella raccolta foto di Windows.<br/> |
| **Barre degli strumenti personalizzabili**<br/> barra degli strumenti che può essere personalizzata dagli utenti. <br/>                          | le barre degli strumenti personalizzabili consentono agli utenti di aggiungere o rimuovere barre degli strumenti, modificarne le dimensioni e la posizione e persino modificarne il contenuto. <br/> ![Screenshot di una barra degli strumenti con dozzine di icone ](images/cmd-toolbars-image11.png)<br/> Barra degli strumenti personalizzabile da Microsoft Visual Studio.<br/>                                             |
| **Finestre tavolozza**<br/> una finestra di dialogo non modale che presenta una matrice di comandi. <br/>                 | le finestre della tavolozza sono barre degli strumenti non ancorate. <br/> ![screenshot della finestra di dialogo colori ](images/cmd-toolbars-image12.png)<br/> ![Screenshot di una finestra di dialogo dei tipi di carattere ](images/cmd-toolbars-image13.png)<br/> Finestre della tavolozza da disegno Windows.<br/>                                                                             |



 

Gli stili della barra degli strumenti sono i seguenti:



|                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Icone senza etichetta**<br/> una o più righe di piccoli pulsanti icona senza etichetta. <br/>                                           | usare questo stile se sono presenti troppi pulsanti per l'etichetta o il programma viene usato di frequente. con questo stile, i programmi con funzionalità complesse possono avere più righe e, pertanto, questo è l'unico stile che deve essere personalizzabile. con questo stile, alcuni pulsanti di comando possono essere etichettati se usati di frequente. <br/> ![screenshot della barra degli strumenti con icone piccole e non etichettate ](images/cmd-toolbars-image14.png)<br/> Barra degli strumenti icone senza etichetta da WordPad.<br/> |
| **Icone grandi senza etichetta**<br/> una singola riga di pulsanti delle icone senza etichetta grandi. <br/>                                         | utilizzare questo stile per semplici utilità che includono icone facilmente riconoscibili e che vengono in genere eseguite in finestre di piccole dimensioni. <br/> ![screenshot della barra degli strumenti con icone grandi e non etichettate ](images/cmd-toolbars-image15.png)<br/> ![screenshot della barra degli strumenti con icone grandi ](images/cmd-toolbars-image16.png)<br/> Barre degli strumenti icone senza etichetta grandi da Windows Live Messenger e lo strumento di cattura di Windows.<br/>                                                                       |
| **Icone con etichetta**<br/> una singola riga di icone con etichetta piccola. <br/>                                                          | utilizzare questo stile se sono presenti pochi comandi oppure il programma non viene utilizzato di frequente. Questo stile ha sempre una sola riga. <br/> ![screenshot della barra degli strumenti con icone con etichetta ](images/cmd-toolbars-image8.png)<br/> Barra degli strumenti icone con etichetta da Esplora risorse.<br/>                                                                                                                                                                                                               |
| **Barre degli strumenti parziali**<br/> riga parziale di icone piccole utilizzata per risparmiare spazio quando non è necessaria una barra degli strumenti completa. <br/>       | utilizzare questo stile per Windows con pulsanti di spostamento, una casella di ricerca o schede per eliminare il peso superfluo nella parte superiore della finestra. <br/> ![screenshot della barra dei menu, della barra degli strumenti e della barra Preferiti ](images/cmd-toolbars-image17.png)<br/> Le barre degli strumenti parziali possono essere combinate con pulsanti di spostamento, una casella di ricerca o tabulazioni.<br/>                                                                                                                                                  |
| **Barre degli strumenti parziali di grandi dimensioni**<br/> riga parziale di icone grandi utilizzata per risparmiare spazio quando non è necessaria una barra degli strumenti completa. <br/> | utilizzare questo stile per semplici utilità con pulsanti di spostamento o una casella di ricerca per eliminare il peso superfluo nella parte superiore della finestra. <br/> ![Screenshot di una barra degli strumenti parziale di grandi dimensioni ](images/cmd-toolbars-image18.png)<br/> Barra degli strumenti parziale di grandi dimensioni di Windows Defender.<br/>                                                                                                                                                                                         |



 

Infine, i controlli della barra degli strumenti hanno diversi modelli di utilizzo:



|                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pulsanti dell'icona di comando**<br/> Quando si fa clic su un pulsante di comando, viene avviata un'azione immediata. <br/>                                                                                                 | ![screenshot della barra degli strumenti delle icone con etichetta ](images/cmd-toolbars-image19.png)<br/> Esempi di pulsanti di comando icona da fax e scanner di Windows.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Pulsanti icona modalità**<br/> Quando si fa clic su un pulsante della modalità, viene attivata la modalità selezionata. <br/>                                                                                                            | ![Screenshot di una barra degli strumenti verticale ](images/cmd-toolbars-image20.png)<br/> Esempi di pulsanti della modalità di Paint di Windows.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Pulsanti delle icone delle proprietà**<br/> lo stato di un pulsante della proprietà riflette lo stato degli oggetti attualmente selezionati. facendo clic sul pulsante viene applicata la modifica agli oggetti selezionati. <br/> | ![screenshot delle icone di formattazione e del testo selezionato ](images/cmd-toolbars-image21.png)<br/> Esempi di pulsanti delle proprietà di Microsoft Word.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Pulsanti delle icone con etichette**<br/> un pulsante di comando o una proprietà con un'etichetta con un'icona e un'etichetta di testo. <br/>                                                                               | questi pulsanti vengono usati per i pulsanti della barra degli strumenti usati di frequente, la cui icona non è sufficientemente intuitiva. vengono inoltre utilizzate nelle barre degli strumenti con pochi pulsanti che possono avere un'etichetta di testo. <br/> ![Screenshot che mostra la barra degli strumenti con le icone contrassegnate per i pulsanti usati più di frequente. ](images/cmd-toolbars-image22.png)<br/> Barra degli strumenti con i pulsanti usati più di frequente con etichetta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Pulsanti di menu**<br/> un pulsante di comando utilizzato per presentare un piccolo set di comandi correlati. <br/>                                                                                                | un singolo triangolo verso il basso indica che facendo clic sul pulsante viene visualizzato un menu. <br/> ![screenshot della barra degli strumenti e dell'elenco dei comandi a discesa ](images/cmd-toolbars-image23.png)<br/> Pulsante di menu con un piccolo set di comandi correlati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Pulsanti di divisione**<br/> un pulsante di comando usato per consolidare le variazioni di un comando, soprattutto quando uno dei comandi viene usato nella maggior parte dei casi. <br/>                                     | ![cattura di schermata del pulsante Dividi stampa ](images/cmd-toolbars-image24.png)<br/> pulsante di suddivisione nello stato normale.<br/> Analogamente a un pulsante di menu, un singolo triangolo verso il basso indica che facendo clic sulla parte più a destra del pulsante viene visualizzato un menu. <br/> ![screenshot dei comandi dei pulsanti Split Print ](images/cmd-toolbars-image25.png)<br/> pulsante di suddivisione a discesa.<br/> in questo esempio viene usato un pulsante combinato per consolidare tutti i comandi correlati alla stampa. il comando di stampa immediata viene usato nella maggior parte dei casi, quindi gli utenti in genere non devono visualizzare gli altri comandi. <br/> a differenza di un pulsante di menu, facendo clic sulla parte sinistra del pulsante viene eseguita direttamente l'azione sull'etichetta. i pulsanti di suddivisione sono efficaci nelle situazioni in cui il comando successivo è probabilmente uguale all'ultimo comando. in questo caso, l'etichetta viene modificata nell'ultimo comando, come con una selezione colori:<br/> ![screenshot dell'icona del cucchiaio che versa il disegno ](images/cmd-toolbars-image26.png)<br/> In questo esempio, l'etichetta viene modificata nell'ultimo comando.<br/> |
| **Elenchi a discesa**<br/> elenco a discesa (modificabile o di sola lettura) utilizzato per visualizzare o modificare una proprietà. <br/>                                                                                   | ![screenshot dell'elenco a discesa dei tipi di carattere ](images/cmd-toolbars-image27.png)<br/> In questo esempio gli elenchi a discesa vengono utilizzati per visualizzare e impostare gli attributi del tipo di carattere.<br/> Un elenco a discesa in una barra degli strumenti riflette lo stato dell'oggetto attualmente selezionato, se disponibile. La modifica dell'elenco modifica lo stato dell'oggetto selezionato. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="guidelines"></a>Indicazioni

### <a name="presentation"></a>Presentazione

-   **Scegliere uno stile appropriato per la barra degli strumenti in base al numero di comandi e al relativo utilizzo.** Per istruzioni su come scegliere, vedere la tabella precedente dello stile della barra degli strumenti. Evitare di utilizzare una configurazione della barra degli strumenti che occupa troppo spazio dall'area di lavoro del programma.
-   **Posizionare le barre degli strumenti appena sopra l'area del contenuto,** sotto la barra dei menu e la barra degli indirizzi, se presente.
-   **Se lo spazio è Premium, risparmiare spazio per:**

    -   Omissione delle etichette di icone note e dei comandi utilizzati meno di frequente.
    -   Utilizzando solo una barra degli strumenti parziale anziché l'intera larghezza della finestra.
    -   Consolidamento dei comandi correlati con un pulsante di menu o un pulsante di menu combinato.
    -   Utilizzo di una freccia di [espansione overflow](glossary.md) per rivelare i comandi utilizzati meno di frequente.
    -   Visualizzazione di comandi solo quando si applicano al contesto corrente.

    ![screenshot delle icone comuni della barra degli strumenti senza etichetta ](images/cmd-toolbars-image28.png)

    La barra degli strumenti di Windows Internet Explorer consente di risparmiare spazio omettendo le etichette delle icone note, utilizzando una barra degli strumenti parziale e utilizzando una freccia di espansione per i comandi utilizzati meno di frequente.

-   **Per il modello della barra degli strumenti icone senza etichetta, utilizzare una configurazione predefinita con non più di due righe di barre degli strumenti.** Se possono essere utili più di due righe, rendere le barre degli strumenti personalizzabili. A partire da più di due righe è possibile sovraccaricare gli utenti e occupare troppo spazio dall'area di lavoro del programma.

    **Non corretto:**

    ![cattura di schermata della barra dei menu e di tre righe di barre degli strumenti ](images/cmd-toolbars-image29.png)

    Una configurazione predefinita con più di due righe di barre degli strumenti comporta un disordine visivo troppo elevato.

-   **Disabilitare i singoli pulsanti della barra degli strumenti che non si applicano al contesto corrente,** anziché rimuoverli. In questo modo, il contenuto della barra degli strumenti diventa stabile e più facile da trovare.
-   **Disabilitare i singoli pulsanti della barra degli strumenti se facendo clic su di essi verrebbe generato direttamente un errore.** Questa operazione è necessaria per mantenere un aspetto diretto.
-   **Per il modello della barra degli strumenti icone senza etichetta, rimuovere intere barre degli strumenti se non si applicano al contesto corrente.** Visualizzarli solo nelle modalità applicabili.

    ![screenshot della barra degli strumenti debug ](images/cmd-toolbars-image30.png)

    In questo esempio, la barra degli strumenti debug viene visualizzata solo quando il programma è in esecuzione.

-   **Visualizzare i pulsanti della barra degli strumenti allineati.** L'icona della guida, se presente, è allineata a destra.

    ![screenshot della barra degli strumenti, icona della guida allineata a destra ](images/cmd-toolbars-image31.png)

    Tutti i pulsanti della barra degli strumenti sono allineati a sinistra tranne per la guida

    **Eccezione:** Le barre degli strumenti di Windows 7 sono allineate ai comandi specifici del programma, ma allinea a destra i comandi standard e noti, ad esempio opzioni, Visualizza e guida.

-   **Non modificare dinamicamente le etichette del pulsante della barra degli strumenti.** Questa operazione è confusa e imprevista. Tuttavia, è possibile modificare l'icona per riflettere lo stato corrente.

    ![screenshot dell'icona del cucchiaio che versa il disegno ](images/cmd-toolbars-image26.png)

    In questo esempio, l'icona viene modificata per indicare il comando predefinito.

### <a name="controls-and-commands"></a>Controlli e comandi

-   **Preferisce i comandi usati più di frequente.**
    -   **Per le barre degli strumenti primarie, fornire comandi completi.** Le barre degli strumenti primarie non devono necessariamente essere complete come le barre dei menu, ma devono fornire tutti i comandi che non sono facilmente individuabili altrove. Le barre degli strumenti primarie non devono avere comandi per:
        -   Comandi direttamente sull'interfaccia utente.
        -   Comandi in genere accessibili tramite i menu di scelta rapida.
        -   Comandi standard e noti, ad esempio taglia, copia e incolla.
    -   **Per le barre degli strumenti aggiuntive, fornire i comandi utilizzati più di frequente.** I comandi della barra dei menu sono un superset dei comandi della barra degli strumenti, pertanto non è necessario specificare tutti gli elementi. Concentrati sull'accesso rapido e pratico ai comandi e ignora il resto.
-   **Preferisci controlli diretti.** Usare i pulsanti della barra degli strumenti nell'ordine di preferenza seguente:
    -   **Pulsante icona.** Diretta e impiega spazio minimo.
    -   **Pulsante icona con etichetta.** Diretta, ma occupa più spazio.
    -   **Pulsante di divisione.** Direct per il comando più comune, ma gestisce le variazioni dei comandi.
    -   **Pulsante di menu.** Indirect, ma presenta molti comandi.
-   **Preferisci comandi immediati.** Per i comandi che possono essere immediati o avere input aggiuntivi per la flessibilità:
    -   Per le barre degli strumenti primarie, usare le versioni flessibili dei comandi, ad esempio Print....
    -   Per le barre degli strumenti aggiuntive, utilizzare le versioni immediate della barra degli strumenti, ad esempio Print, e utilizzare versioni flessibili nella barra dei menu (ad esempio Print...).
-   **Fornire etichette per i comandi usati di frequente,** soprattutto se le icone non sono icone note.

    **Accettabile:**

    ![screenshot della barra degli strumenti senza icone con etichetta ](images/cmd-toolbars-image32.png)

    **Migliore:**

    ![screenshot della barra degli strumenti con alcune icone con etichetta ](images/cmd-toolbars-image33.png)

    La barra degli strumenti di fax e digitalizzazione di Windows presenta pochi comandi, quindi la versione migliore è l'etichetta più importante.

-   Non inserire i comandi nei menu della barra degli strumenti che si trovano anche direttamente sulla barra degli strumenti.

    **Non corretto:**

    ![screenshot del comando stampa sulla barra degli strumenti e sul menu ](images/cmd-toolbars-image34.png)

    In questo esempio, Print è direttamente sulla barra degli strumenti, quindi non è necessario che sia nel menu.

### <a name="organization-and-order"></a>Organizzazione e ordine

-   **Organizzare i comandi all'interno di una barra degli strumenti in gruppi correlati.**
-   **Inserire prima i gruppi usati più di frequente. All'interno di un gruppo, inserire i comandi nell'ordine logico.** Nel complesso, i comandi devono avere un flusso logico per facilitarne l'individuazione, mentre i comandi usati più di frequente vengono visualizzati per primi. Questa operazione è più efficiente, soprattutto se si verifica un overflow.
-   **Usare i divisori di gruppo solo se i comandi tra gruppi sono debolmente accoppiati.** Questa operazione rende i raggruppamenti evidenti e i comandi più facili da trovare.

    ![Screenshot che mostra una barra degli strumenti con icone ben organizzate usando i divisori di gruppo.](images/cmd-toolbars-image35.png)

    ![screenshot della barra degli strumenti con icone ben organizzate ](images/cmd-toolbars-image36.png)

    Esempi di barre degli strumenti raggruppate di Windows Mail.

-   **Evitare di inserire comandi distruttivi accanto ai comandi usati di frequente.** Usare Order o GROUPING per ottenere la separazione. Inoltre, è consigliabile non inserire comandi distruttivi sulla barra degli strumenti, ma solo nella barra dei menu o nei menu di scelta rapida.

    **Accettabile:**

    ![screenshot dei pulsanti di stampa e di eliminazione adiacenti ](images/cmd-toolbars-image37.png)

    **Migliore:**

    ![screenshot dei pulsanti di stampa e eliminazione separati ](images/cmd-toolbars-image38.png)

    Nell'esempio migliore, il comando Delete è fisicamente separato dalla stampa.

-   **Utilizzare la freccia di espansione overflow per indicare che non è possibile visualizzare tutti i comandi.** Usare però overflow solo se non è disponibile spazio sufficiente per visualizzare tutti i comandi.

    **Non corretto:**

    ![screenshot della barra Preferiti e dei comandi nascosti ](images/cmd-toolbars-image39.png)

    La freccia di espansione overflow indica che non tutti i comandi vengono visualizzati, ma più di essi potrebbero avere un layout migliore.

-   **Verificare che i comandi usati più di frequente siano accessibili direttamente dalla barra degli strumenti (ovvero, non in overflow) in dimensioni di finestra ridotte.** Se necessario, riordinare i comandi, spostare i comandi utilizzati meno di frequente in pulsanti di menu o pulsanti di menu combinato oppure rimuoverli completamente dalla barra degli strumenti. Se il problema persiste, riconsiderare la scelta dello stile della barra degli strumenti.

### <a name="hiding-menu-bars"></a>Nascondere le barre dei menu

In genere, le barre degli strumenti funzionano perfettamente insieme alle barre dei menu perché entrambe consentono di concentrarsi sui propri punti di forza senza compromessi.

-   Per impostazione predefinita, nascondere la barra dei menu se la progettazione della barra degli strumenti rende ridondante la barra dei menu.
-   Nascondere la barra dei menu anziché rimuoverla completamente, perché le barre dei menu sono più accessibili per gli utenti della tastiera.
-   Per ripristinare la barra dei menu, specificare un'opzione per il segno di spunta della barra dei menu nella categoria Visualizza (per le barre degli strumenti primarie) o strumenti (per le barre degli strumenti secondarie). Per ulteriori informazioni, vedere [menu standard e pulsanti di menu combinato](#standard-menu-and-split-buttons).
-   Visualizzare la barra dei menu quando gli utenti preme il tasto ALT e impostare lo stato attivo per l'input sulla prima categoria di menu.

### <a name="interaction"></a>Interazione

-   Al passaggio del mouse, visualizzare la [convenienza](glossary.md) del pulsante per indicare che l'icona è selezionabile. Dopo il timeout della descrizione comando, visualizzare la descrizione comando o infotip.

    ![Screenshot di un infotip che descrive un pulsante ](images/cmd-toolbars-image40.png)

    In questo esempio vengono illustrati i vari Stati di visualizzazione.

-   A sinistra con un solo clic:
    -   Per i pulsanti di comando, interagire con il controllo come di consueto.
    -   Per i pulsanti Mode, visualizzare il controllo in modo da riflettere la modalità attualmente selezionata. Se la modalità influiscono sul comportamento dell'interazione del mouse, modificare anche il puntatore.

        ![cattura di schermata di un puntatore simile a un bucket di disegno ](images/cmd-toolbars-image41.png)

        In questo esempio, il puntatore viene modificato per mostrare la modalità di interazione del mouse.

    -   Per i pulsanti delle proprietà e gli elenchi a discesa, visualizzare il controllo in modo da riflettere lo stato degli oggetti attualmente selezionati. In interazione aggiornare lo stato del controllo e applicare la modifica agli oggetti selezionati. Se non è selezionata alcuna opzione, non eseguire alcuna operazione.

-   Fare doppio clic con il pulsante destro del mouse ed eseguire la stessa azione di un singolo clic a sinistra.
    -   **Eccezione:** In rare occasioni, è possibile usare un comando della barra degli strumenti in modo più efficiente. In questi casi, utilizzare il doppio clic per impostare la modalità.

        ![Screenshot di infotip che mostra le funzioni del pulsante ](images/cmd-toolbars-image42.png)

        In questo esempio, facendo doppio clic sul comando Format Paint, viene attivata una modalità in cui tutti i clic successivi applicano il formato. Gli utenti possono lasciare la modalità facendo clic con il pulsante sinistro del mouse.

-   Fare clic con il pulsante destro del mouse:
    -   Per le barre degli strumenti personalizzabili, visualizzare il menu di scelta rapida per la personalizzazione della barra degli strumenti. Visualizzare il menu facendo clic con il pulsante destro del mouse sulla freccia giù, non sul pulsante del mouse.
    -   Per le altre barre degli strumenti, non eseguire alcuna operazione.

### <a name="icons"></a>Icone

-   **Fornire icone per tutti i controlli della barra degli strumenti tranne gli elenchi a discesa.**

    ![screenshot dell'elenco a discesa delle dimensioni dei tipi di carattere ](images/cmd-toolbars-image43.png)

    Gli elenchi a discesa non necessitano di icone, ma di tutti gli altri controlli della barra degli strumenti.

    **Eccezione:** Le barre degli strumenti di tipo Windows 7 usano le icone solo per i comandi le cui icone sono note; in caso contrario, utilizzano etichette di testo senza icone. Questa operazione consente di migliorare la chiarezza delle etichette, ma richiede più spazio.

-   **Verificare che le icone della barra degli strumenti siano chiaramente visibili rispetto al colore di sfondo della barra degli strumenti.** Valutare sempre le icone della barra degli strumenti nel contesto e in modalità a contrasto elevato.
-   **Scegliere le progettazioni di icone che comunicano chiaramente il proprio scopo, specialmente per i comandi usati più di frequente.** Le barre degli strumenti ben progettate necessitano di icone autoesplicative perché gli utenti non riescono a trovare i comandi in modo efficiente usando le descrizioni comandi. Tuttavia, le barre degli strumenti continuano a funzionare correttamente se le icone per alcuni comandi usati meno di frequente non sono esplicative.
-   **Scegliere le icone riconoscibili e distinguibili, specialmente per i comandi usati più di frequente.** Assicurarsi che le icone abbiano forme e colori distinti. Questa operazione consente agli utenti di trovare rapidamente i comandi anche se non ricordano il simbolo dell'icona.
-   **Assicurarsi che le icone della barra degli strumenti siano conformi alle linee guida dell'icona di tipo Aero.**

Per ulteriori informazioni ed esempi, vedere [Icone](vis-icons.md).

### <a name="standard-menu-and-split-buttons"></a>Menu standard e pulsanti di menu combinato

Se si utilizzano pulsanti di menu e pulsanti di menu combinato in una barra degli strumenti, provare a utilizzare le seguenti strutture di menu standard e i relativi comandi quando possibile. Diversamente dalle barre dei menu, i comandi della barra degli strumenti non accettano chiavi di accesso.

**Barre degli strumenti primarie**

Questi comandi rispecchiano i comandi presenti nelle barre dei menu standard, pertanto devono essere usati solo per le barre degli strumenti primarie. Questo elenco Mostra le etichette dei pulsanti (e digitare) con l'ordine e i separatori, i tasti di scelta rapida e le ellisse. **Si noti che il comando per visualizzare e nascondere la barra dei menu si trova nel menu Visualizza.**

<dl> File <dl> NewCtrl + N  
Apri... CTRL + O  
Chiudere <separator>  
SaveCtrl + S  
Salva con nome... <separator>  
Invia a <separator>  
Stampa... CTRL + P  
Anteprima di stampa  
Imposta pagina <separator>  
ExitAlt + F4 (collegamento di solito non fornito)
</dl> </dd> Edit(menu button) <dl> UndoCtrl + Z  
RedoCtrl + Y <separator>  
CutCtrl + X  
CopyCtrl + C  
PasteCtrl + V <separator>  
Seleziona allCtrl + A <separator>  
DeleteDel (collegamento generalmente non specificato)  
Rinomina... <separator>  
Trova... CTRL + F  
Find nextF3 (comando in genere non specificato)  
Sostituisci... CTRL + H  
Vai a... CTRL + G
</dl> </dd> <dd>Print (pulsante di suddivisione) <dl> Stampa... CTRL + P  
Anteprima di stampa <separator>  
Impostazioni di pagina
</dl> </dd> Visualizza (pulsante di menu) <dl> Barra dei menu (controlla se visibile)  
Riquadro dei dettagli (verificare se visibile)  
Riquadro di anteprima (controlla se visibile)  
Barra di stato (controlla se visibile) <separator>  
Zoom  
Zoom indietro + +  
Zoom indietro (CTRL +-) <separator>  
Dimensioni testo (impostazione selezionata con Bullet) <dl> Più  
Maggiore  
Medio  
Più piccoli  
Più piccolo
</dl> </dd> <separator> ScreenF11 completo  
RefreshF5
</dl> </dd> Tools(menu button) <dl> ... <separator>  
Opzioni
</dl>> </dd> Help(split button, use the Help icon) <dl> <program name> helpF1 <separator>  
Su <program name>  
</dl> </dd> </dl>

**Barre degli strumenti supplementari**

Questi comandi completano le barre dei menu standard. Questo elenco Mostra le etichette dei pulsanti (e digitare) con l'ordine e i separatori, i tasti di scelta rapida e le ellisse. **Si noti che il comando per visualizzare e nascondere la barra dei menu si trova nel menu strumenti.**

I nomi delle categorie aggiuntive della barra degli strumenti sono diversi dai nomi delle categorie di menu standard, perché devono essere più inclusi. Ad esempio, viene usata la categoria Organize anziché Edit perché contiene comandi che non sono correlati alla modifica. **Per mantenere la coerenza tra le barre dei menu e le barre degli strumenti, utilizzare i nomi delle categorie di menu standard se questa operazione non è fuorviante.**

**Non corretto:**

![screenshot delle stesse opzioni per i diversi comandi ](images/cmd-toolbars-image44.png)

In questo esempio, la barra degli strumenti deve usare modifica anziché organizza per coerenza perché contiene i comandi di menu modifica standard.

### <a name="palette-windows"></a>Finestre tavolozza

-   **Le finestre della tavolozza utilizzano barre del titolo più brevi per ridurre al minimo lo spazio dello schermo.** Posizionare un pulsante Chiudi sulla barra del titolo.
-   **Impostare il testo della barra del titolo sul comando che ha visualizzato la finestra della tavolozza.**
-   **Usare l'uso di maiuscole in stile frase senza la punteggiatura finale.**
-   **Consente di specificare un menu di scelta rapida per i comandi di gestione della finestra.** Visualizza questo menu di scelta rapida quando gli utenti fanno clic con il pulsante destro del mouse sulla barra del titolo.

    ![screenshot della casella degli strumenti con menu di scelta rapida ](images/cmd-toolbars-image45.png)

    In questo esempio, gli utenti possono fare clic con il pulsante destro del mouse sulla barra del titolo per visualizzare il menu di scelta rapida.

-   **Quando possibile e utile, rendere ridimensionabili le finestre della tavolozza.** Indica che la finestra è ridimensionabile, usando i puntatori di ridimensionamento quando si trova sulla cornice della finestra.
-   **Quando una finestra della tavolozza viene visualizzata nuovamente, visualizzarla utilizzando lo stesso stato dell'ultimo accesso.** Alla chiusura, salvare le dimensioni e la posizione della finestra. Quando si esegue la rivisualizzazione, ripristinare le dimensioni e la posizione della finestra salvata. Si consiglia inoltre di rendere persistenti questi attributi tra le istanze del programma in base ai singoli utenti.

### <a name="customization"></a>Personalizzazione

-   **Fornire la personalizzazione per le barre degli strumenti costituite da due o più righe.** Solo lo stile delle icone senza etichetta necessita di personalizzazione. Per le barre degli strumenti semplici con pochi comandi non è necessaria la personalizzazione.
-   **Fornire una configurazione predefinita corretta.** Gli utenti non devono personalizzare le barre degli strumenti per gli scenari comuni. Non dipendere dagli utenti che personalizzano la loro modalità di configurazione iniziale non valida. Si supponga che la maggior parte degli utenti non Personalizza le barre degli strumenti.
-   **Fornire un menu di scelta rapida con i comandi seguenti:**
    -   Elenco di caselle di controllo per visualizzare le barre degli strumenti disponibili
    -   Blocca/Sblocca barre degli strumenti
    -   Personalizza...
-   Per **impostazione predefinita, bloccare le barre degli strumenti personalizzabili** per evitare modifiche accidentali.
-   **Per il comando Personalizza, visualizzare una finestra di dialogo Opzioni** che consente di scegliere le barre degli strumenti da visualizzare e i comandi su ogni barra degli strumenti.

    ![screenshot della finestra di dialogo Personalizza e delle opzioni ](images/cmd-toolbars-image46.png)

    In questo esempio, Visual Studio fornisce una finestra di dialogo Opzioni per personalizzare le barre degli strumenti.

-   Fornire un comando reset per tornare alla configurazione originale della barra degli strumenti nella finestra di dialogo Opzioni di personalizzazione.
-   **Fornire la possibilità di personalizzare le barre degli strumenti tramite il trascinamento della selezione nei modi seguenti:**

    -   Imposta ordine e posizioni della barra degli strumenti.
    -   Impostare le lunghezze della barra degli strumenti, visualizzando le barre degli strumenti troppo piccole per visualizzare il contenuto con una freccia di espansione.
    -   Se supportato, disancorare le barre degli strumenti per diventare finestre della tavolozza e viceversa.

    Quando viene visualizzata la finestra di dialogo Personalizza opzioni:

    -   Imposta il contenuto della barra degli strumenti.
    -   Imposta l'ordine del contenuto della barra degli strumenti.

    Questa operazione consente agli utenti di apportare modifiche in modo più diretto ed efficiente.

-   **Salvare tutte le personalizzazioni della barra degli strumenti,** in base ai singoli utenti.

### <a name="using-ellipses"></a>Uso di ellissi

Mentre i comandi della barra degli strumenti vengono usati per le azioni immediate, a volte sono necessarie altre informazioni per eseguire l'azione. Usare i puntini di sospensione per indicare che un comando richiede ulteriori informazioni prima che possa essere applicato. Posizionare i puntini di sospensione alla fine della descrizione comando e dell'etichetta, se presente.

![screenshot del testo della descrizione comando stampa con puntini di sospensione ](images/cmd-toolbars-image47.png)

In questo esempio, Print... consente di visualizzare una finestra di dialogo Stampa per raccogliere ulteriori informazioni.

Se un comando non può essere applicato immediatamente, tuttavia, non è necessario alcun ellisse. Quindi, ad esempio, le impostazioni di condivisione non hanno i puntini di sospensione anche se sono necessarie informazioni aggiuntive, perché il comando non può essere applicato immediatamente.

![screenshot della barra degli strumenti, del comando e della descrizione comando ](images/cmd-toolbars-image48.png)

Il comando impostazioni di condivisione non ha i puntini di sospensione perché non può essere applicato immediatamente.

Poiché le barre degli strumenti vengono visualizzate costantemente e lo spazio è a un livello Premium, i puntini di sospensione **devono essere usati raramente**.

> [!Note]  
> Per i menu visualizzati da una barra degli strumenti, applicare le [linee guida per le ellissi del menu](cmd-menus.md).

 

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![screenshot delle barre degli strumenti con informazioni sulla spaziatura ](images/cmd-toolbars-image49.png)

Dimensionamento e spaziatura consigliati per le barre degli strumenti standard.

## <a name="labels"></a>Etichette

### <a name="general"></a>Generale

-   **Usare le maiuscole/minuscole come nelle frasi comuni.**
    -   **Eccezione:** Per le applicazioni legacy, è possibile usare l'uso di maiuscole in stile titolo, se necessario, per evitare di combinare stili di maiuscole.

### <a name="unlabeled-icon-buttons"></a>Pulsanti icona senza etichetta

-   **Usare una descrizione comando per etichettare il comando.** Per il testo della descrizione comando, usare l'etichetta se il pulsante è stato etichettato, ma includere il tasto di scelta rapida se ne esiste uno.

    ![screenshot della barra degli strumenti, dell'icona della stampante e della descrizione comando ](images/cmd-toolbars-image50.png)

    Esempio di descrizione comando di un pulsante icona.

### <a name="labeled-icon-buttons"></a>Pulsanti delle icone con etichette

-   **Utilizzare un'etichetta concisa.** Se possibile, utilizzare una sola parola, ovvero il valore massimo di quattro parole.
-   **Posizionare l'etichetta a destra dell'icona.**
-   **Usare un infotip per descrivere il comando.** Poiché i pulsanti vengono etichettati, l'uso di una descrizione comando anziché di un infotip sarebbe ridondante.

    ![screenshot del pulsante con etichetta con infotip ](images/cmd-toolbars-image51.png)

    Esempio di pulsante icona con etichetta infotip.

### <a name="drop-down-lists"></a>Elenchi a discesa

-   **Se l'elenco contiene sempre un valore, utilizzare il valore corrente come etichetta.**

    ![screenshot della barra degli strumenti con opzioni carattere ](images/cmd-toolbars-image52.png)

    In questo esempio, il nome del tipo di carattere attualmente selezionato funge da etichetta.

-   Se un elenco a discesa modificabile non ha un valore, usare una [richiesta](glossary.md).

    ![screenshot delle rubriche di ricerca dell'etichetta elenco ](images/cmd-toolbars-image53.png)

    In questo esempio viene usato un prompt per l'etichetta dell'elenco a discesa.

### <a name="menu-buttons-and-split-buttons"></a>Pulsanti di menu e pulsanti di menu combinato

-   **Preferisce i nomi dei pulsanti di menu basati su verbi.** Tuttavia, omettere il verbo se è creare, visualizzare, visualizzare o gestire. Ad esempio, **gli strumenti** e i pulsanti del menu **pagina** non dispongono di verbi.
-   **Usare una singola parola specifica che descrive in modo chiaro e accurato il contenuto del menu.** Sebbene i nomi non debbano essere così generali che descrivano tutti gli elementi del menu, dovrebbero essere prevedibili, in modo che gli utenti non siano sorpresi da ciò che trovano nel menu.
-   **Sebbene non sia obbligatorio, fornire le descrizioni infotip se sono utili.**

### <a name="menu-items"></a>Voci di menu

-   **Usare nomi di voci di menu che iniziano con un verbo, un sostantivo o una frase nominale.**
-   **Preferisce i nomi di menu basati su verbi.** Tuttavia, omettere il verbo se è creare, visualizzare, visualizzare o gestire. I comandi seguenti, ad esempio, non usano i verbi:
    -   Informazioni
    -   Avanzato
    -   Schermo intero
    -   Nuova
    -   Opzioni
    -   Proprietà
-   **Usare verbi specifici.** Evitare verbi generici e non helper, ad esempio la modifica e la gestione.
-   **Utilizzare sostantivi singoli per i comandi che si applicano a un singolo oggetto;** in caso contrario, utilizzare Sostantivi plurali.
-   **Per le coppie di comandi complementari, scegliere nomi chiaramente complementari.** Esempi: Add, Remove; Mostra, Nascondi; Insert, DELETE.
-   **Scegliere i nomi delle voci di menu in base agli obiettivi e alle attività dell'utente, non alla tecnologia.**
-   Utilizzare i seguenti nomi di voci di menu per lo scopo indicato:
    -   **Opzioni:** Per visualizzare le opzioni del programma.
    -   **Personalizza:** Per visualizzare le opzioni di programma specifiche relative alla configurazione dell'interfaccia utente meccanica.
    -   **Personalizza:** Per visualizzare un riepilogo delle impostazioni di [personalizzazione](glossary.md) di uso comune.
    -   **Preferenze:** Non usare. Usare invece le opzioni.
    -   **Proprietà:** Per visualizzare la finestra delle proprietà di un oggetto.
    -   **Impostazioni:** Non usare come etichetta di menu. Usare invece le opzioni.
-   **Le voci di menu che visualizzano i sottomenu non hanno mai i puntini di sospensione nell'etichetta.** La freccia del sottomenu indica che è necessaria un'altra selezione.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle barre degli strumenti:

-   Se è presente una sola barra degli strumenti, farvi riferimento come barra degli strumenti.
-   Se sono presenti più barre degli strumenti, fare riferimento a esse in base al nome, seguite dalla barra degli strumenti di Word. Per impostazione predefinita, fare riferimento alla barra degli strumenti principale e contiene i pulsanti per le attività di base, ad esempio l'apertura e la stampa di un file, come barra degli strumenti standard.
-   La barra degli strumenti è un'unica parola non maiuscola. Al contrario, la barra dei menu è due parole.
-   Fare riferimento ai pulsanti della barra degli strumenti in base alle etichette della descrizione comando. Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere i puntini di sospensione.
-   Fare riferimento ai pulsanti di menu della barra degli strumenti in base alle etichette e al menu di Word. Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola.
-   Vedere i controlli della barra degli strumenti in genere come pulsanti della barra degli strumenti.
-   Per descrivere l'interazione dell'utente, utilizzare fare clic per i pulsanti della barra degli strumenti e gli elenchi a discesa di sola lettura e immettere per gli elenchi a discesa modificabili. Non usare choose, SELECT o pick.
-   Non usare i pulsanti a cascata, a discesa, a discesa o a comparsa per descrivere i pulsanti di menu, tranne che nella documentazione di programmazione.
-   Vedere gli elementi non disponibili come non disponibili, non come grigio, disabilitato o inattivo. Usare Disabled nella documentazione di programmazione.
-   Quando possibile, formattare le etichette usando il testo in grassetto. In caso contrario, inserire le etichette tra virgolette solo se necessario per evitare confusione.

Esempi:

-   Dal menu **pagina** sulla barra degli strumenti fare clic su **Invia pagina tramite posta elettronica**.
-   Nella casella **caratteri** della barra degli strumenti immettere "Segoe UI".
-   Sulla barra degli strumenti **formattazione** scegliere **Mostra**, quindi fare clic su **Commenti**.

 

