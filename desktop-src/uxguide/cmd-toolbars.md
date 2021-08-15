---
title: Barre degli strumenti
description: Le barre degli strumenti consentono di raggruppare i comandi per un accesso efficiente.
ms.assetid: 8f36307c-54fc-493d-a2ff-57db29e3508d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8015e1dec17ad524645b474b21d42af9269ffbc8d24279c56612620f0e4bb615
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450033"
---
# <a name="toolbars"></a>Barre degli strumenti

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Le barre degli strumenti consentono di raggruppare i comandi per un accesso efficiente.

![Screenshot di due barre degli strumenti con elementi etichettati ](images/cmd-toolbars-image1.png)

Alcune barre degli strumenti tipiche.

**Usare le barre degli strumenti oltre o al posto delle barre dei menu.** Le barre degli strumenti possono essere più efficienti rispetto alle barre dei menu perché sono dirette (sempre visualizzate invece di essere visualizzate al clic del mouse), immediate (anziché richiedere input aggiuntivo) e contengono i comandi usati più di frequente (anziché un elenco completo). A differenza delle barre dei menu, le barre degli strumenti non devono essere complete o autosplicative, ma solo rapide, convenienti ed efficienti.

Alcune barre degli strumenti sono personalizzabili, consentendo agli utenti di aggiungere o rimuovere barre degli strumenti, modificarne le dimensioni e la posizione e persino modificarne il contenuto. Alcuni tipi di barre degli strumenti possono essere disinseriti, determinando una finestra del riquadro. Per altre informazioni sulle varietà di barre degli strumenti, vedere [Modelli di utilizzo](#usage-patterns) in questo articolo.

> [!Note]  
> Le linee guida relative [a menu,](cmd-menus.md) [pulsanti](ctrl-command-buttons.md)di comando e [icone](vis-icons.md) sono presentate in articoli separati.

 

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, prendi in considerazione queste domande:

-   **La finestra è una finestra primaria?** Le barre degli strumenti funzionano bene per le finestre primarie, ma in genere sono molto grandi per le finestre secondarie. Per le finestre secondarie, [usare i pulsanti di](ctrl-command-buttons.md)comando, i pulsanti di [menu](ctrl-command-buttons.md)e [i collegamenti.](ctrl-command-links.md)
-   **È presente un numero ridotto di comandi usati di frequente?** Le barre degli strumenti non possono gestire tutti i comandi delle barre dei menu, quindi funzionano meglio come un modo per accedere in modo efficiente a un numero ridotto di comandi usati di frequente.
-   **La maggior parte dei comandi è immediata?** In altre informazioni, si tratta principalmente di comandi che non richiedono input aggiuntivo? Per essere efficienti, le barre degli strumenti devono avere un aspetto diretto e immediato. In caso contrario, le barre dei menu sono più adatte per i comandi che richiedono input aggiuntivo.
-   **La maggior parte dei comandi può essere presentata direttamente?** In altri, gli utenti interagiscono con loro con un solo clic? Anche se alcuni comandi possono essere presentati usando i pulsanti di menu, la visualizzazione della maggior parte dei comandi in questo modo compromette l'efficienza della barra degli strumenti, rendendo una barra dei menu una scelta migliore.
-   **I comandi sono ben rappresentati dalle icone?** I pulsanti della barra degli strumenti sono in genere rappresentati da icone anziché etichette di testo (anche se alcuni pulsanti della barra degli strumenti usano entrambi), mentre i comandi di menu sono rappresentati dal relativo testo. Se le icone dei comandi non sono di alta qualità e non sono auto-esplicativi, una barra dei menu potrebbe essere una scelta migliore.

Se il programma dispone di una barra degli strumenti senza barra dei menu e la maggior parte dei comandi è accessibile indirettamente tramite pulsanti di menu e pulsanti di [divisione,](ctrl-command-buttons.md)questa barra degli strumenti è essenzialmente una barra dei menu. Applicare invece [il modello di menu della](cmd-menus.md) barra degli strumenti nelle linee guida menu.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Una buona barra dei menu è un catalogo completo di tutti i comandi di primo livello disponibili, mentre una buona barra degli strumenti offre un accesso rapido e pratico ai comandi usati di frequente. Una barra degli strumenti non tenta di eseguire il training degli utenti solo per renderli produttivi. Dopo aver appreso come accedere a un comando su una barra degli strumenti, gli utenti raramente continuano ad accedere al comando dalla barra dei menu. Per questi motivi, non è necessario che la barra dei menu di un programma e la relativa barra degli strumenti corrispondano direttamente.

### <a name="toolbars-vs-menu-bars"></a>Barre degli strumenti e barre dei menu

Tradizionalmente, le barre degli strumenti sono diverse dalle barre dei menu nei modi seguenti:

-   **Frequenza.** Le barre degli strumenti presentano solo i comandi usati più di frequente, mentre le barre dei menu catalogano tutti i comandi di primo livello disponibili all'interno di un programma.
-   **Immediatezza.** Facendo clic su un comando della barra degli strumenti viene eseguito immediatamente, mentre un comando di menu potrebbe richiedere un input aggiuntivo. Ad esempio, un comando Stampa in una barra dei menu visualizza prima la finestra di dialogo Stampa, mentre un pulsante della barra degli strumenti Stampa stampa immediatamente una singola copia di un documento nella stampante predefinita.

    ![Screenshot del pulsante della stampante della barra degli strumenti selezionato ](images/cmd-toolbars-image2.png)

    In questo esempio, facendo clic sul pulsante Della barra degli strumenti Stampa viene immediatamente stampata una singola copia di un documento nella stampante predefinita.

-   **Immediatezza.** I comandi della barra degli strumenti vengono richiamati con un solo clic, mentre i comandi della barra dei menu richiedono lo spostamento all'interno del menu.
-   **Numero e densità.** Lo spazio dello schermo richiesto da una barra degli strumenti è proporzionale al numero di comandi e lo spazio viene sempre usato, anche se non lo sono. Di conseguenza, le barre degli strumenti devono usare il proprio spazio in modo efficiente. Al contrario, i comandi della barra dei menu sono in genere nascosti alla visualizzazione e la relativa struttura gerarchica consente qualsiasi numero di comandi.
-   **Dimensioni e presentazione.** Per imballare molti comandi in uno spazio ridotto, le barre degli strumenti in genere usano comandi basati su icone (con etichette basate su descrizione comando), mentre le barre dei menu usano comandi basati su testo (con icone facoltative). Anche se i pulsanti della barra degli strumenti possono avere etichette di testo standard, questi usano molto più spazio.

    ![Screenshot della barra degli strumenti con etichetta di invio/ricezione ](images/cmd-toolbars-image3.png)

    I pulsanti della barra degli strumenti con etichetta hanno almeno tre volte più spazio di quelli senza etichetta.

-   **Auto-esplicativo.** Le barre degli strumenti ben progettate necessitano di icone per lo più autosplicative perché gli utenti non possono trovare i comandi in modo efficiente solo usando le descrizioni comando. Tuttavia, le barre degli strumenti funzionano ancora bene se alcuni comandi usati meno di frequente non sono auto-esplicativi.

    ![Screenshot della barra degli strumenti con icone familiari ](images/cmd-toolbars-image4.png)

    In questo esempio, le icone usate più di frequente sono auto-esplicativi.

-   **Riconoscibile e distinguibile.** Per i comandi usati di frequente, gli utenti ricordano gli attributi dei pulsanti della barra degli strumenti, ad esempio posizione, forma e colore. Con le barre degli strumenti ben progettate, gli utenti possono trovare rapidamente i comandi anche se non ricordano il simbolo esatto dell'icona. Al contrario, gli utenti ricordano le posizioni dei comandi della barra dei menu usate di frequente, ma si basano sulle etichette dei comandi per effettuare selezioni.

    ![Screenshot della finestra di dialogo delle opzioni dello strumento di cattura ](images/cmd-toolbars-image5.png)

    Per i comandi della barra degli strumenti, la posizione, la forma e il colore distintivi consentono di rendere le icone riconoscibili e distinguibili.

    ![Screenshot della barra dei menu con il comando file selezionato ](images/cmd-toolbars-image6.png)

    Per i comandi della barra dei menu, gli utenti dipendono in ultima analisi dalle etichette.

### <a name="efficiency"></a>Efficienza

Date le caratteristiche, le barre degli strumenti devono essere progettate principalmente per l'efficienza. Una barra degli strumenti inefficiente non ha alcun senso.

**Se si fa una sola cosa...**

Assicurarsi che le barre degli strumenti siano progettate principalmente per garantire l'efficienza. Concentrare le barre degli strumenti sui comandi usati di frequente, immediati, diretti e rapidamente riconoscibili.

### <a name="hiding-menu-bars"></a>Nascondere le barre dei menu

In genere, le barre degli strumenti funzionano in modo ottimale insieme alle barre dei menu: le barre degli strumenti sono efficienti e le barre dei menu sono complete. **La presenza di barre dei menu e barre degli strumenti consente a ognuna di concentrarsi sui punti di forza senza compromessi.**

Sorprendentemente, questo modello si suddivide in semplici programmi. Per i programmi con pochi comandi, avere sia una barra dei menu che una barra degli strumenti non ha senso perché la barra dei menu finisce per essere una versione ridondante e inefficiente della barra degli strumenti.

Per eliminare questa ridondanza, molti semplici programmi in Windows Vista si concentrano sulla necessità di fornire comandi esclusivamente tramite la barra degli strumenti e nascondere la barra dei menu per impostazione predefinita. Tali programmi includono Windows Explorer, Windows Internet Explorer, Windows Media Player e Windows Raccolta foto.

Questa non è una piccola modifica. La rimozione della barra dei menu modifica fondamentalmente la natura delle barre degli strumenti, perché tali barre degli strumenti devono essere complete e modificare nei modi seguenti:

-   **Frequenza.** La rimozione della barra dei menu significa che tutti i comandi non disponibili direttamente da una finestra o dai relativi menu di scelta rapida devono essere accessibili dalla barra degli strumenti, indipendentemente dalla frequenza d'uso.
-   **Immediatezza.** La rimozione della barra dei menu rende la barra degli strumenti l'unico punto di accesso visibile per i comandi, richiedendo che la barra degli strumenti abbia le versioni completamente funzionali. Ad esempio, se non è presente alcuna barra dei menu, un comando Stampa su una barra degli strumenti deve visualizzare la finestra di dialogo Stampa anziché stampare immediatamente. Anche se in questo caso l'uso di un pulsante di divisione è un compromesso eccellente. Vedere [Menu Standard e pulsanti di divisione](#standard-menu-and-split-buttons) per il pulsante di divisione Stampa standard.

    ![Screenshot della barra degli strumenti e delle opzioni del comando di stampa ](images/cmd-toolbars-image7.png)

    In questo esempio il pulsante della barra degli strumenti Stampa Windows Raccolta foto un comando Stampa che visualizza la finestra di dialogo Stampa .

-   **Immediatezza.** Per risparmiare spazio ed evitare confusione, i comandi usati meno di frequente possono essere spostati nei pulsanti di menu, rendendoli meno diretti.

Le barre degli strumenti usate per integrare una barra dei menu sono progettate in modo diverso rispetto alle barre degli strumenti progettate per l'uso con una barra dei menu rimossa o nascosta. Inoltre, poiché non è possibile presupporre che gli utenti visualizzano una barra dei menu nascosta per eseguire un singolo comando, nascondere una barra dei menu deve essere considerata come rimuoverla completamente quando si prendono decisioni di progettazione. Se si nasconde la barra dei menu per impostazione predefinita, non presupporre che gli utenti pensino a visualizzare la barra dei menu per trovare un comando o persino a capire come visualizzarla.

La progettazione di una barra degli strumenti per il funzionamento senza una barra dei menu spesso comporta alcune compromissione. Ma per efficienza, non compromettere troppo. Se nascondere la barra dei menu comporta una barra degli strumenti inefficiente, non nascondere la barra dei menu.

### <a name="keyboard-accessibility"></a>Accessibilità tramite tastiera

Dalla tastiera, l'accesso alle barre degli strumenti è piuttosto diverso dall'accesso alle barre dei menu. Le barre dei menu ricevono lo stato attivo quando gli utenti premono ALT e perdono lo stato attivo per l'input con il tasto ESC. Quando una barra dei menu ha lo stato attivo per l'input, viene spostata indipendentemente dal resto della finestra, gestendo tutti i tasti di direzione, Home, Fine e Tab. Al contrario, le barre degli strumenti ricevono lo stato attivo per l'input quando gli utenti preme TAB per l'intero contenuto della finestra. Poiché le barre degli strumenti sono l'ultima nell'ordine di tabulazione, l'attivazione potrebbe richiedere molto tempo in una pagina occupata(a meno che gli utenti non sappiano usare MAIUSC+TAB per spostarsi all'indietro).

L'accessibilità presenta un problema: sebbene le barre degli strumenti siano più facili per gli utenti del mouse, sono meno accessibili per gli utenti della tastiera. Questo non è un problema se sono presenti sia una barra dei menu che una barra degli strumenti, ma se la barra dei menu viene rimossa o nascosta.

Per motivi di accessibilità, è quindi preferibile mantenere la barra dei menu anziché rimuoverla completamente a favore di una barra degli strumenti. Se è necessario scegliere tra rimuovere la barra dei menu e nasconderla, è preferibile nasconderla.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le barre degli strumenti hanno diversi modelli di utilizzo:



|     Utilizzo                                                                                                                 |     Esempio                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barre degli strumenti principali**<br/> una barra degli strumenti progettata per funzionare senza una barra dei menu, nascosta o rimossa. <br/> | Le barre degli strumenti principali devono bilanciare la necessità di efficienza con la completezza, in modo che funzionino meglio per i programmi semplici. <br/> ![Screenshot della barra degli strumenti di Esplora risorse ](images/cmd-toolbars-image8.png)<br/> Barra degli strumenti principale da Windows Explorer.<br/>                                                                        |
| **Barre degli strumenti supplementari**<br/> una barra degli strumenti progettata per l'utilizzo con una barra dei menu. <br/>                         | Le barre degli strumenti supplementari possono concentrarsi sull'efficienza senza compromessi. <br/> ![Screenshot di una barra dei menu su una barra degli strumenti ](images/cmd-toolbars-image9.png)<br/> Barra degli strumenti supplementare da Windows Movie Maker.<br/>                                                                                                                  |
| **Menu della barra degli strumenti**<br/> una barra dei menu implementata come barra degli strumenti. <br/>                                        | I menu della barra degli strumenti sono barre degli strumenti costituite principalmente da comandi nei pulsanti di [menu](ctrl-command-buttons.md) e nei pulsanti di divisione, con solo alcuni comandi diretti, se presenti. <br/> ![Screenshot della barra dei menu con icone e comandi ](images/cmd-toolbars-image10.png)<br/> Menu della barra degli strumenti Windows Raccolta foto.<br/> |
| **Barre degli strumenti personalizzabili**<br/> una barra degli strumenti che può essere personalizzata dagli utenti. <br/>                          | Le barre degli strumenti personalizzabili consentono agli utenti di aggiungere o rimuovere barre degli strumenti, modificarne le dimensioni e la posizione e persino modificarne il contenuto. <br/> ![Screenshot di una barra degli strumenti con decine di icone ](images/cmd-toolbars-image11.png)<br/> Barra degli strumenti personalizzabile da Microsoft Visual Studio.<br/>                                             |
| **Finestre del riquadro**<br/> una finestra di dialogo non modabile che presenta una matrice di comandi. <br/>                 | Le finestre della tavolozza sono barre degli strumenti non ancorate. <br/> ![Screenshot di una finestra di dialogo colori ](images/cmd-toolbars-image12.png)<br/> ![Screenshot di una finestra di dialogo dei tipi di carattere ](images/cmd-toolbars-image13.png)<br/> Finestre della tavolozza Windows Paint.<br/>                                                                             |



 

Gli stili delle barre degli strumenti sono i seguenti:



|   Stile                                                                                                                                     | Esempio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Icone senza etichetta**<br/> una o più righe di piccoli pulsanti icona senza etichetta. <br/>                                           | usare questo stile se sono presenti troppi pulsanti da etichettare o se il programma viene usato di frequente. Con questo stile, i programmi con funzionalità complesse possono avere più righe e pertanto questo è l'unico stile che deve essere personalizzabile. Con questo stile, alcuni pulsanti di comando possono essere etichettati se vengono usati di frequente. <br/> ![Screenshot della barra degli strumenti con icone piccole e senza etichetta ](images/cmd-toolbars-image14.png)<br/> Barra degli strumenti delle icone senza etichetta da WordPad.<br/> |
| **Icone grandi senza etichetta**<br/> una singola riga di pulsanti di icone grandi senza etichetta. <br/>                                         | usare questo stile per utilità semplici che hanno icone facilmente riconoscibili e vengono in genere eseguite in finestre di piccole dimensioni. <br/> ![Screenshot della barra degli strumenti con icone grandi senza etichetta ](images/cmd-toolbars-image15.png)<br/> ![Screenshot della barra degli strumenti con icone grandi ](images/cmd-toolbars-image16.png)<br/> Barre degli strumenti di icone grandi senza etichetta Windows Live Messenger e dal Windows Strumento di cattura.<br/>                                                                       |
| **Icone con etichetta**<br/> una singola riga di piccole icone con etichetta. <br/>                                                          | usare questo stile se sono presenti pochi comandi o se il programma non viene usato di frequente. questo stile ha sempre una singola riga. <br/> ![Screenshot della barra degli strumenti con icone con etichetta ](images/cmd-toolbars-image8.png)<br/> Barra degli strumenti delle icone con etichetta Windows Explorer.<br/>                                                                                                                                                                                                               |
| **Barre degli strumenti parziali**<br/> una riga parziale di icone piccole usata per risparmiare spazio quando non è necessaria una barra degli strumenti completa. <br/>       | usare questo stile per le finestre con pulsanti di spostamento, una casella di ricerca o schede per eliminare il peso non necessario nella parte superiore della finestra. <br/> ![Screenshot della barra dei menu, della barra degli strumenti e della barra preferiti ](images/cmd-toolbars-image17.png)<br/> Le barre degli strumenti parziali possono essere combinate con pulsanti di spostamento, una casella di ricerca o schede.<br/>                                                                                                                                                  |
| **Barre degli strumenti parziali di grandi dimensioni**<br/> una riga parziale di icone grandi usata per risparmiare spazio quando non è necessaria una barra degli strumenti completa. <br/> | Usare questo stile per utilità semplici con pulsanti di spostamento o una casella di ricerca per eliminare il peso non necessario nella parte superiore della finestra. <br/> ![Screenshot di una barra degli strumenti parziale di grandi dimensioni ](images/cmd-toolbars-image18.png)<br/> Barra degli strumenti parziale di grandi dimensioni Windows Defender.<br/>                                                                                                                                                                                         |



 

Infine, i controlli barra degli strumenti hanno diversi modelli di utilizzo:



|     Utilizzo                                                                                                                 |     Esempio                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pulsanti dell'icona di comando**<br/> Facendo clic su un pulsante di comando viene avviata un'azione immediata. <br/>                                                                                                 | ![Screenshot di una barra degli strumenti con icone etichettate ](images/cmd-toolbars-image19.png)<br/> Esempi di pulsanti di comando icona Windows Fax e Scansione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Pulsanti icona modalità**<br/> Se si fa clic su un pulsante modalità, viene attivata la modalità selezionata. <br/>                                                                                                            | ![Screenshot di una barra degli strumenti verticale ](images/cmd-toolbars-image20.png)<br/> Esempi di pulsanti di modalità Windows Paint.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Pulsanti dell'icona delle proprietà**<br/> Lo stato di un pulsante di proprietà riflette lo stato degli oggetti attualmente selezionati, se presenti. Se si fa clic sul pulsante, la modifica viene applicata agli oggetti selezionati. <br/> | ![Screenshot delle icone di formattazione e del testo selezionato ](images/cmd-toolbars-image21.png)<br/> Esempi di pulsanti di proprietà Microsoft Word.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Pulsanti delle icone con etichette**<br/> un pulsante di comando o un pulsante di proprietà etichettato con un'icona e un'etichetta di testo. <br/>                                                                               | questi pulsanti vengono usati per i pulsanti della barra degli strumenti usati di frequente la cui icona non è sufficientemente auto-esplicativa. vengono usati anche nelle barre degli strumenti con così pochi pulsanti che ogni pulsante può avere un'etichetta di testo. <br/> ![Screenshot che mostra la barra degli strumenti con icone etichettate per i pulsanti usati più di frequente. ](images/cmd-toolbars-image22.png)<br/> Barra degli strumenti con i pulsanti usati più di frequente etichettati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Pulsanti di menu**<br/> un pulsante di comando usato per presentare un piccolo set di comandi correlati. <br/>                                                                                                | Un singolo triangolo che punta verso il basso indica che facendo clic sul pulsante viene visualizzato un menu. <br/> ![Screenshot della barra degli strumenti e dell'elenco a discesa dei comandi ](images/cmd-toolbars-image23.png)<br/> Pulsante di menu con un piccolo set di comandi correlati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Pulsanti di menu suddivisi**<br/> un pulsante di comando usato per consolidare le varianti di un comando, soprattutto quando uno dei comandi viene usato nella maggior parte dei casi. <br/>                                     | ![Screenshot del pulsante di divisione della stampa ](images/cmd-toolbars-image24.png)<br/> Pulsante di menu suddiviso nello stato normale.<br/> Come un pulsante di menu, un singolo triangolo che punta verso il basso indica che facendo clic sulla parte più a destra del pulsante viene visualizzato un menu. <br/> ![Screenshot dei comandi del pulsante di divisione della stampa ](images/cmd-toolbars-image25.png)<br/> pulsante di menu a discesa.<br/> In questo esempio viene usato un pulsante di menu suddiviso per consolidare tutti i comandi correlati alla stampa. Il comando di stampa immediato viene usato nella maggior parte dei casi, quindi gli utenti in genere non devono visualizzare gli altri comandi. <br/> A differenza di un pulsante di menu, facendo clic sulla parte sinistra del pulsante viene eseguita direttamente l'azione sull'etichetta. I pulsanti di divisione sono efficaci nelle situazioni in cui è probabile che il comando successivo sia uguale all'ultimo comando. In questo caso, l'etichetta viene modificata nell'ultimo comando, come con una selezione colori:<br/> ![screenshot dell'icona del bucket che colora ](images/cmd-toolbars-image26.png)<br/> In questo esempio l'etichetta viene modificata nell'ultimo comando.<br/> |
| **Elenchi a discesa**<br/> Elenco a discesa (modificabile o di sola lettura) usato per visualizzare o modificare una proprietà. <br/>                                                                                   | ![Screenshot dell'elenco a discesa dei tipi di carattere ](images/cmd-toolbars-image27.png)<br/> In questo esempio gli elenchi a discesa vengono usati per visualizzare e impostare gli attributi del tipo di carattere.<br/> Un elenco a discesa in una barra degli strumenti riflette lo stato dell'oggetto attualmente selezionato, se presente. La modifica dell'elenco modifica lo stato dell'oggetto selezionato. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="guidelines"></a>Indicazioni

### <a name="presentation"></a>Presentazione

-   **Scegliere uno stile appropriato per la barra degli strumenti in base al numero di comandi e al relativo utilizzo.** Per indicazioni su come scegliere, vedere la tabella di stile della barra degli strumenti precedente. Evitare di usare una configurazione della barra degli strumenti che richiede troppo spazio dall'area di lavoro del programma.
-   **Posizionare le barre degli strumenti appena sopra l'area del contenuto,** sotto la barra dei menu e la barra degli indirizzi, se presente.
-   **Se lo spazio è premium, risparmiare spazio in base a:**

    -   Omissione delle etichette delle icone note e dei comandi usati meno di frequente.
    -   Usando solo una barra degli strumenti parziale anziché l'intera larghezza della finestra.
    -   Consolidamento dei comandi correlati con un pulsante di menu o un pulsante di menu suddiviso.
    -   Uso di [una chevron di overflow](glossary.md) per rivelare i comandi usati meno di frequente.
    -   Visualizzazione dei comandi solo quando si applicano al contesto corrente.

    ![Screenshot delle icone comuni della barra degli strumenti non etichettate ](images/cmd-toolbars-image28.png)

    La Windows Internet Explorer barra degli strumenti consente di risparmiare spazio omettendo le etichette delle icone note, usando una barra degli strumenti parziale e usando una chevron di overflow per i comandi usati meno di frequente.

-   **Per il modello della barra degli strumenti icone senza etichetta, usare una configurazione predefinita con non più di due righe di barre degli strumenti.** Se potrebbero essere utili più di due righe, rendere personalizzabili le barre degli strumenti. Iniziare con più di due righe può sovraccaricare gli utenti e richiedere troppo spazio dall'area di lavoro del programma.

    **Non corretto:**

    ![Screenshot della barra dei menu e di tre righe di barre degli strumenti ](images/cmd-toolbars-image29.png)

    Una configurazione predefinita con più di due righe di barre degli strumenti comporta un numero troppo di confusione visiva.

-   **Disabilitare i singoli pulsanti della barra degli strumenti che** non si applicano al contesto corrente, invece di rimuoverli. In questo modo il contenuto della barra degli strumenti risulta stabile e più facile da trovare.
-   **Disabilitare i singoli pulsanti della barra degli strumenti se facendo clic su di essi si verifica direttamente un errore.** Questa operazione è necessaria per mantenere un'aspetto diretto.
-   **Per il modello della barra degli strumenti icone senza etichetta, rimuovere intere barre degli strumenti se non si applicano al contesto corrente.** Visualizzarli solo nelle modalità applicabili.

    ![Screenshot della barra degli strumenti di debug ](images/cmd-toolbars-image30.png)

    In questo esempio la barra degli strumenti Debug viene visualizzata solo quando il programma è in esecuzione.

-   **Visualizzare i pulsanti della barra degli strumenti allineati a sinistra.** L'icona della Guida, se presente, è allineata a destra.

    ![screenshot della barra degli strumenti, icona della Guida allineata a destra ](images/cmd-toolbars-image31.png)

    Tutti i pulsanti della barra degli strumenti sono allineati a sinistra, ad eccezione della Guida.

    **Eccezione: Windows** barre degli strumenti in stile 7 allineano a sinistra i comandi specifici del programma, ma allineano a destra i comandi standard noti, ad esempio Opzioni, Visualizza e Guida.

-   **Non modificare dinamicamente le etichette dei pulsanti della barra degli strumenti.** Questa operazione è confusa e imprevista. È tuttavia possibile modificare l'icona per riflettere lo stato corrente.

    ![screenshot dell'icona del bucket che colora ](images/cmd-toolbars-image26.png)

    In questo esempio l'icona viene modificata per indicare il comando predefinito.

### <a name="controls-and-commands"></a>Controlli e comandi

-   **Preferire i comandi usati più di frequente.**
    -   **Per le barre degli strumenti principali, fornire comandi completi.** Le barre degli strumenti principali non devono essere complete come le barre dei menu, ma devono fornire tutti i comandi che non sono facilmente individuabili altrove. Le barre degli strumenti principali non devono avere comandi per:
        -   Comandi direttamente nell'interfaccia utente.
        -   Comandi a cui si accede in genere tramite menu di scelta rapida.
        -   Comandi standard noti come Taglia, Copia e Incolla.
    -   **Per le barre degli strumenti supplementari, specificare i comandi usati più di frequente.** I comandi della barra dei menu sono un superset dei comandi della barra degli strumenti, quindi non è necessario fornire tutto. Concentrarsi sull'accesso rapido e pratico ai comandi e ignorare il resto.
-   **Preferisce i controlli diretti.** Usare i pulsanti della barra degli strumenti nell'ordine di preferenza seguente:
    -   **Pulsante icona.** Diretto e richiede spazio minimo.
    -   **Pulsante icona con etichetta.** Diretto, ma richiede più spazio.
    -   **Pulsante di menu suddiviso.** Diretto per il comando più comune, ma gestisce le varianti dei comandi.
    -   **Pulsante di menu.** Indiretto, ma presenta molti comandi.
-   **Preferisce comandi immediati.** Per i comandi che possono essere immediati o avere un input aggiuntivo per la flessibilità:
    -   Per le barre degli strumenti principali, usare le versioni flessibili dei comandi, ad esempio Stampa.
    -   Per le barre degli strumenti supplementari, usare le versioni immediate sulla barra degli strumenti (ad esempio Stampa) e usare versioni flessibili nella barra dei menu (ad esempio Stampa...).
-   **Fornire etichette per i comandi usati di frequente,** soprattutto se le icone non sono icone note.

    **Accettabile:**

    ![Screenshot della barra degli strumenti senza icone etichettate ](images/cmd-toolbars-image32.png)

    **Migliore:**

    ![Screenshot della barra degli strumenti con alcune icone etichettate ](images/cmd-toolbars-image33.png)

    La barra Windows Fax e Digitalizzazione include pochi comandi, quindi la versione migliore etichetta quelle più importanti.

-   Non inserire comandi nei menu della barra degli strumenti che sono anche direttamente sulla barra degli strumenti.

    **Non corretto:**

    ![Screenshot del comando di stampa sulla barra degli strumenti e sul menu ](images/cmd-toolbars-image34.png)

    In questo esempio Print è direttamente sulla barra degli strumenti, quindi non deve essere presente nel menu.

### <a name="organization-and-order"></a>Organizzazione e ordine

-   **Organizzare i comandi all'interno di una barra degli strumenti in gruppi correlati.**
-   **Posizionare prima i gruppi usati più di frequente. All'interno di un gruppo, inserire i comandi nell'ordine logico.** In generale, i comandi devono avere un flusso logico per semplificare l'individuazione, mantenendo al tempo stesso i comandi usati più di frequente per primi. Questa operazione è più efficiente, soprattutto in caso di overflow.
-   **Usare i divisori di gruppo solo se i comandi tra gruppi sono ad accoppiato debole.** In questo modo i raggruppamenti sono ovvi e i comandi sono più facili da trovare.

    ![Screenshot che mostra una barra degli strumenti con icone ben organizzate usando i divisori di gruppo.](images/cmd-toolbars-image35.png)

    ![Screenshot della barra degli strumenti con icone ben organizzate ](images/cmd-toolbars-image36.png)

    Esempi di barre degli strumenti raggruppate Windows Mail.

-   **Evitare di inserire comandi distruttivi accanto ai comandi usati di frequente.** Usare l'ordine o il raggruppamento per ottenere la separazione. È anche consigliabile non inserire comandi distruttivi nella barra degli strumenti, ma solo nella barra dei menu o nei menu di scelta rapida.

    **Accettabile:**

    ![Screenshot dei pulsanti di stampa ed eliminazione adiacenti ](images/cmd-toolbars-image37.png)

    **Migliore:**

    ![Screenshot dei pulsanti di stampa ed eliminazione separati ](images/cmd-toolbars-image38.png)

    Nell'esempio migliore, il comando Elimina è fisicamente separato da Stampa.

-   **Usare la chevron di overflow per indicare che non tutti i comandi possono essere visualizzati.** Ma usare l'overflow solo se non c'è spazio sufficiente per visualizzare tutti i comandi.

    **Non corretto:**

    ![Screenshot della barra Preferiti e dei comandi nascosti ](images/cmd-toolbars-image39.png)

    La descrizione dell'overflow indica che non tutti i comandi vengono visualizzati, ma più comandi potrebbero avere un layout migliore.

-   **Assicurarsi che i comandi usati più di frequente siano accessibili direttamente dalla barra degli strumenti, ovvero non in overflow, in finestre di piccole dimensioni.** Se necessario, riordinare i comandi, spostare i comandi usati meno di frequente nei pulsanti di menu o nei pulsanti di menu divisi o persino rimuoverli completamente dalla barra degli strumenti. Se il problema persiste, riconsiderare la scelta dello stile della barra degli strumenti.

### <a name="hiding-menu-bars"></a>Nascondere le barre dei menu

In genere, le barre degli strumenti funzionano bene insieme alle barre dei menu perché entrambe consentono a ognuna di concentrarsi sui punti di forza senza compromettere.

-   Nascondere la barra dei menu per impostazione predefinita se la progettazione della barra degli strumenti rende ridondante una barra dei menu.
-   Nascondere la barra dei menu invece di rimuoverla completamente, perché le barre dei menu sono più accessibili per gli utenti della tastiera.
-   Per ripristinare la barra dei menu, specificare un'opzione di segno di spunta barra dei menu nella categoria di menu Visualizza (per le barre degli strumenti principali) o Strumenti (per le barre degli strumenti secondarie). Per altre informazioni, vedere [Menu standard e pulsanti di menu suddivisi.](#standard-menu-and-split-buttons)
-   Visualizzare la barra dei menu quando gli utenti preme il tasto ALT e impostare lo stato attivo per l'input nella prima categoria di menu.

### <a name="interaction"></a>Interazione

-   Al passaggio del mouse, visualizzare [l'affordance del pulsante](glossary.md) per indicare che l'icona è selezionabile. Dopo il timeout della descrizione comando, visualizzare la descrizione comando o la descrizione comando.

    ![Screenshot di una descrizione comando che descrive un pulsante ](images/cmd-toolbars-image40.png)

    Questo esempio mostra i vari stati di visualizzazione.

-   Al clic singolo a sinistra:
    -   Per i pulsanti di comando, interagire con il controllo come di consueto.
    -   Per i pulsanti della modalità, visualizzare il controllo in modo da riflettere la modalità attualmente selezionata. Se la modalità influisce sul comportamento dell'interazione del mouse, modificare anche il puntatore.

        ![Screenshot del puntatore a forma di bucket di disegno ](images/cmd-toolbars-image41.png)

        In questo esempio il puntatore viene modificato per mostrare la modalità di interazione del mouse.

    -   Per i pulsanti di proprietà e gli elenchi a discesa, visualizzare il controllo per riflettere lo stato degli oggetti attualmente selezionati, se presenti. Durante l'interazione, aggiornare lo stato del controllo e applicare la modifica agli oggetti selezionati. Se non è selezionata alcuna opzione, non eseguire alcuna operazione.

-   Al doppio clic a sinistra, eseguire la stessa azione di un singolo clic a sinistra.
    -   **Eccezione:** In rari casi, un comando della barra degli strumenti può essere usato in modo più efficiente come modale. In questi casi, usare il doppio clic per attivare o disattivare la modalità.

        ![Screenshot della descrizione comando che mostra le funzioni del pulsante ](images/cmd-toolbars-image42.png)

        In questo esempio, facendo doppio clic sul comando Formatta , viene attivata una modalità in cui tutti i clic successivi applicano il formato. Gli utenti possono uscire dalla modalità facendo clic con il pulsante sinistro del mouse.

-   Al clic con il pulsante destro del mouse:
    -   Per le barre degli strumenti personalizzabili, visualizzare il menu di scelta rapida per la personalizzazione della barra degli strumenti. Visualizzare il menu quando si fa clic con il pulsante destro del mouse verso il basso, non verso l'alto.
    -   Per altre barre degli strumenti, non eseguire alcuna operazione.

### <a name="icons"></a>Icone

-   **Specificare le icone per tutti i controlli della barra degli strumenti, ad eccezione degli elenchi a discesa.**

    ![Screenshot dell'elenco a discesa delle dimensioni del carattere ](images/cmd-toolbars-image43.png)

    Gli elenchi a discesa non necessitano di icone, a differenza di tutti gli altri controlli della barra degli strumenti.

    **Eccezione: Windows** barre degli strumenti in stile 7 usano le icone solo per i comandi le cui icone sono note; In caso contrario, usano etichette di testo senza icone. Questa operazione migliora la chiarezza delle etichette, ma richiede più spazio.

-   **Assicurarsi che le icone della barra degli strumenti siano chiaramente visibili sul colore di sfondo della barra degli strumenti.** Valutare sempre le icone della barra degli strumenti nel contesto e in modalità a contrasto elevato.
-   **Scegliere progettazioni di icone che comunicano chiaramente lo scopo, in particolare per i comandi usati più di frequente.** Le barre degli strumenti ben progettate necessitano di icone che siano auto-esplicativi perché gli utenti non possono trovare i comandi in modo efficiente usando le descrizioni comando. Tuttavia, le barre degli strumenti continuano a funzionare correttamente se le icone per alcuni comandi usati meno di frequente non sono poco esplicativi.
-   **Scegliere icone riconoscibili e distinguibili, soprattutto per i comandi usati più di frequente.** Assicurarsi che le icone presentino forme e colori distintivi. In questo modo gli utenti possono trovare rapidamente i comandi anche se non ricordano il simbolo dell'icona.
-   **Assicurarsi che le icone della barra degli strumenti siano conformi alle linee guida per le icone in stile Aereo.**

Per altre informazioni ed esempi, vedere [Icone.](vis-icons.md)

### <a name="standard-menu-and-split-buttons"></a>Menu standard e pulsanti di menu suddivisi

Se si usano pulsanti di menu e pulsanti di menu divisi in una barra degli strumenti, provare a usare le strutture di menu standard seguenti e i relativi comandi pertinenti quando possibile. A differenza delle barre dei menu, i comandi della barra degli strumenti non accettano i tasti di scelta.

**Barre degli strumenti principali**

Questi comandi rispecchiano i comandi presenti nelle barre dei menu standard, quindi devono essere usati solo per le barre degli strumenti principali. Questo elenco mostra le etichette dei pulsanti (e il tipo) con l'ordine e i separatori, i tasti di scelta rapida e i puntini di sospensione. **Si noti che il comando per visualizzare e nascondere la barra dei menu è nel menu Visualizza.**

<dl> File <dl> NewCtrl+N  
Aperto... CTRL+O  
Chiudere <separator>  
SaveCtrl+S  
Salva con nome... <separator>  
Invia a <separator>  
Stampare... CTRL+P  
Anteprima di stampa  
Configurazione della pagina <separator>  
ExitAlt+F4(tasto di scelta rapida in genere non specificato)
</dl> </dd> Edit(menu button) <dl> UndoCtrl+Z  
RedoCtrl+Y <separator>  
CutCtrl+X  
CopyCtrl+C  
PasteCtrl+V <separator>  
Selezionare allCtrl+A <separator>  
DeleteDel(collegamento in genere non specificato)  
Rinominare... <separator>  
Trovare... CTRL+F  
Trova nextF3(comando in genere non specificato)  
Sostituire... CTRL+H  
Vai a... CTRL+G
</dl> </dd> <dd>Stampa (pulsante di menu suddiviso) <dl> Stampare... CTRL+P  
Anteprima di stampa <separator>  
Impostazioni di pagina
</dl> </dd> Visualizza (pulsante di menu) <dl> Barra dei menu (controllare se visibile)  
Riquadro dei dettagli (controllare se visibile)  
Riquadro di anteprima (controllare se visibile)  
Barra di stato (controllare se visibile) <separator>  
Zoom  
Zoom avantiCtrl++  
Zoom indietroCtrl+- <separator>  
Dimensioni del testo (l'impostazione selezionata include un punto elenco) <dl> Maggiori  
Maggiore  
Medio  
Piccoli  
Piccolo
</dl> </dd> <separator> Schermo interoF11  
RefreshF5
</dl> </dd> Tools(menu button) <dl> ... <separator>  
Opzioni
</dl>> </dd> Help(split button, use the Help icon) <dl> <program name> helpF1 <separator>  
Circa <program name>  
</dl> </dd> </dl>

**Barre degli strumenti supplementari**

Questi comandi integrano le barre dei menu standard. Questo elenco mostra le etichette dei pulsanti (e il tipo) con l'ordine e i separatori, i tasti di scelta rapida e i puntini di sospensione. **Si noti che il comando per visualizzare e nascondere la barra dei menu è nel menu Strumenti.**

I nomi delle categorie supplementari della barra degli strumenti differiscono dai nomi delle categorie di menu standard perché devono essere più comprendenti. Ad esempio, viene usata la categoria Organizza invece di Modifica perché contiene comandi non correlati alla modifica. **Per mantenere la coerenza tra barre dei menu e barre degli strumenti, usare i nomi delle categorie di menu standard se questa operazione non sarebbe fuorviante.**

**Non corretto:**

![Screenshot delle stesse opzioni per comandi diversi ](images/cmd-toolbars-image44.png)

In questo esempio la barra degli strumenti deve usare Modifica anziché Organizza per coerenza perché include i comandi di menu Standard Modifica.

### <a name="palette-windows"></a>Finestre della tavolozza

-   **Le finestre della tavolozza usano barre del titolo più brevi per ridurre al minimo lo spazio sullo schermo.** Inserire un pulsante Chiudi sulla barra del titolo.
-   **Impostare il testo della barra del titolo sul comando che ha visualizzato la finestra della tavolozza.**
-   **Usare l'iniziale maiuscola in stile frase senza terminare la punteggiatura.**
-   **Specificare un menu di scelta rapida per i comandi di gestione delle finestre.** Visualizzare questo menu di scelta rapida quando gli utenti fa clic con il pulsante destro del mouse sulla barra del titolo.

    ![Screenshot della casella degli strumenti con menu di scelta rapida ](images/cmd-toolbars-image45.png)

    In questo esempio gli utenti possono fare clic con il pulsante destro del mouse sulla barra del titolo per visualizzare il menu di scelta rapida.

-   **Quando possibile e utile, rendere ridimensionabili le finestre della tavolozza.** Indica che la finestra è ridimensionabile, usando i puntatori di ridimensionamento quando si trova sopra la cornice della finestra.
-   **Quando una finestra della tavolozza viene visualizzata nuovamente, visualizzarla con lo stesso stato dell'ultimo accesso.** Quando si chiude, salvare le dimensioni e la posizione della finestra. Quando si visualizza nuovamente, ripristinare le dimensioni e il percorso della finestra salvati. È anche consigliabile rendere questi attributi persistenti tra le istanze del programma per ogni utente.

### <a name="customization"></a>Personalizzazione

-   **Fornire la personalizzazione per le barre degli strumenti costituite da due o più righe.** Solo lo stile delle icone senza etichetta richiede la personalizzazione. Le barre degli strumenti semplici con pochi comandi non necessitano di personalizzazione.
-   **Fornire una configurazione predefinita valida.** Gli utenti non devono personalizzare le barre degli strumenti per scenari comuni. Non dipendere dalla personalizzazione da parte degli utenti di una configurazione iniziale non valida. Si supponga che la maggior parte degli utenti non personalizza le barre degli strumenti.
-   **Fornire un menu di scelta rapida con i comandi seguenti:**
    -   Elenco di caselle di controllo per visualizzare le barre degli strumenti disponibili
    -   Barre degli strumenti di blocco/sblocco
    -   Personalizza...
-   **Bloccare le barre degli strumenti personalizzabili per impostazione** predefinita, per impedire modifiche accidentali.
-   **Per il comando Personalizza, visualizzare una** finestra di dialogo di opzioni che consente di scegliere quali barre degli strumenti visualizzare e i comandi su ogni barra degli strumenti.

    ![Screenshot della finestra di dialogo di personalizzazione e delle opzioni ](images/cmd-toolbars-image46.png)

    In questo esempio, Visual Studio una finestra di dialogo di opzioni per personalizzare le barre degli strumenti.

-   Specificare un comando Reimposta per tornare alla configurazione originale della barra degli strumenti nella finestra di dialogo Personalizza opzioni.
-   **È possibile personalizzare le barre degli strumenti usando il trascinamento della selezione nei modi seguenti:**

    -   Impostare l'ordine e le posizioni della barra degli strumenti.
    -   Impostare le lunghezze delle barre degli strumenti, visualizzando tutte le barre degli strumenti troppo piccole per visualizzarne il contenuto con unavron di overflow.
    -   Se supportato, disinserire le barre degli strumenti in modo che diventino finestre della tavolozza e viceversa.

    Quando viene visualizzata la finestra di dialogo Personalizza opzioni:

    -   Impostare il contenuto della barra degli strumenti.
    -   Impostare l'ordine del contenuto della barra degli strumenti.

    In questo modo gli utenti possono apportare modifiche in modo più diretto ed efficiente.

-   **Salvare tutte le personalizzazioni della barra** degli strumenti in base all'utente.

### <a name="using-ellipses"></a>Uso dei puntini di sospensione

Mentre i comandi della barra degli strumenti vengono usati per azioni immediate, talvolta sono necessarie altre informazioni per eseguire l'azione. Usare i puntini di sospensione per indicare che un comando richiede altre informazioni prima che possa essere eseguito. Inserire i puntini di sospensione alla fine della descrizione comando e dell'etichetta, se presenti.

![Screenshot del testo della descrizione comando di stampa con i puntini di sospensione ](images/cmd-toolbars-image47.png)

In questo esempio, il comando Stampa... visualizza una finestra di dialogo Stampa per raccogliere altre informazioni.

Se un comando non può essere eseguito immediatamente, tuttavia, non sono necessari puntini di sospensione. Quindi, ad esempio, le impostazioni di condivisione non hanno puntini di sospensione anche se sono necessarie informazioni aggiuntive, perché il comando non può avere effetto immediato.

![Screenshot della barra degli strumenti, del comando e della descrizione comando ](images/cmd-toolbars-image48.png)

Il comando Impostazioni condivisione non ha i puntini di sospensione perché non può essere eseguito immediatamente.

Poiché le barre degli strumenti vengono visualizzate costantemente e lo spazio è premium, i puntini di sospensione devono **essere usati raramente.**

> [!Note]  
> Per i menu visualizzati da una barra degli strumenti, applicare le linee guida per i [puntini di sospensione dei menu.](cmd-menus.md)

 

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

![Screenshot delle barre degli strumenti con informazioni sulla spaziatura ](images/cmd-toolbars-image49.png)

Dimensioni e spaziatura consigliate per le barre degli strumenti standard.

## <a name="labels"></a>Etichette

### <a name="general"></a>Generale

-   **Usare le maiuscole/minuscole come nelle frasi comuni.**
    -   **Eccezione:** Per le applicazioni legacy, è possibile usare la combinazione di maiuscole e minuscole in stile titolo, se necessario, per evitare di combinare gli stili di uso delle maiuscole.

### <a name="unlabeled-icon-buttons"></a>Pulsanti icona senza etichetta

-   **Usare una descrizione comando per etichettare il comando.** Per il testo della descrizione comando, usare l'etichetta se il pulsante fosse etichettato, ma includere il tasto di scelta rapida, se presente.

    ![screenshot della barra degli strumenti, dell'icona della stampante e della descrizione comando ](images/cmd-toolbars-image50.png)

    Esempio di descrizione comando di un pulsante icona.

### <a name="labeled-icon-buttons"></a>Pulsanti delle icone con etichette

-   **Usare un'etichetta concisa.** Usare una singola parola, se possibile, al massimo quattro parole.
-   **Posizionare l'etichetta a destra dell'icona.**
-   **Usare un infotip per descrivere il comando.** Poiché i pulsanti sono etichettati, l'uso di una descrizione comando anziché di una descrizione comando sarebbe ridondante.

    ![Screenshot del pulsante con etichetta con suggerimento ](images/cmd-toolbars-image51.png)

    Un esempio di suggerimento per un pulsante icona con etichetta.

### <a name="drop-down-lists"></a>Elenchi a discesa

-   **Se l'elenco ha sempre un valore, usare il valore corrente come etichetta.**

    ![Screenshot della barra degli strumenti con le opzioni del tipo di carattere ](images/cmd-toolbars-image52.png)

    In questo esempio il nome del tipo di carattere attualmente selezionato funge da etichetta.

-   Se un elenco a discesa modificabile non ha un valore, usare un [prompt](glossary.md).

    ![Screenshot delle rubriche di ricerca di etichette di elenco ](images/cmd-toolbars-image53.png)

    In questo esempio viene usata una richiesta per l'etichetta dell'elenco a discesa.

### <a name="menu-buttons-and-split-buttons"></a>Pulsanti di menu e pulsanti di divisione

-   **Preferisce i nomi dei pulsanti di menu basati su verbi.** Tuttavia, omettere il verbo se è Create, Show, View o Manage. Ad esempio, **i pulsanti di** menu Strumenti e Pagina non hanno verbi. 
-   **Usare una singola parola specifica che descriva in modo chiaro e accurato il contenuto del menu.** Anche se i nomi non devono essere così generali da descrivere tutti gli elementi nel menu, devono essere sufficientemente prevedibili in modo che gli utenti non siano sorprese da ciò che trovano nel menu.
-   **Anche se non sono obbligatorie, fornire descrizioni infotip se sono utili.**

### <a name="menu-items"></a>Voci di menu

-   **Usare nomi di voci di menu che iniziano con una frase verbo, sostantivo o sostantivo.**
-   **Preferisce i nomi dei menu basati su verbi.** Tuttavia, omettere il verbo se è Create, Show, View o Manage. Ad esempio, i comandi seguenti non usano verbi:
    -   Informazioni
    -   Avanzato
    -   Schermo intero
    -   Nuovo
    -   Opzioni
    -   Proprietà
-   **Usare verbi specifici.** Evitare verbi generici e inutili, ad esempio Change e Manage.
-   **Usare sostantivi singolari per i comandi che si applicano a un singolo oggetto, altrimenti** usare sostantivi plurali.
-   **Per coppie di comandi complementari, scegliere nomi chiaramente complementari.** Esempi: Add, Remove; Mostra, Nascondi; Inserisci, Elimina.
-   **Scegliere i nomi delle voci di menu in base a obiettivi e attività dell'utente, non alla tecnologia.**
-   Usare i nomi delle voci di menu seguenti per lo scopo indicato:
    -   **Opzioni:** Per visualizzare le opzioni del programma.
    -   **Personalizza:** Per visualizzare le opzioni del programma correlate in modo specifico alla configurazione dell'interfaccia utente meccanica.
    -   **Personalizza:** Per visualizzare un riepilogo delle impostazioni di personalizzazione [di uso](glossary.md) comune.
    -   **Preferenze:** Non usare. In alternativa, usare Opzioni.
    -   **Proprietà:** Per visualizzare la finestra delle proprietà di un oggetto.
    -   **Impostazioni:** Non usare come etichetta di menu. In alternativa, usare Opzioni.
-   **Le voci di menu che visualizzano sottomenu non hanno mai puntini di sospensione sull'etichetta.** La freccia del sottomenu indica che è necessaria un'altra selezione.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle barre degli strumenti:

-   Se è presente una sola barra degli strumenti, fare riferimento a essa come barra degli strumenti.
-   Se sono presenti più barre degli strumenti, fare riferimento a esse in base al nome, seguito dalla barra degli strumenti delle parole. Fare riferimento alla barra degli strumenti principale che è aperta per impostazione predefinita e contiene pulsanti per attività di base, ad esempio l'apertura e la stampa di un file, come barra degli strumenti standard.
-   La barra degli strumenti è una singola parola non maiuscola. Al contrario, la barra dei menu è di due parole.
-   Fare riferimento ai pulsanti della barra degli strumenti in base alle etichette della descrizione comando. Usare il testo esatto dell'etichetta, inclusa l'uso di maiuscole e minuscole, ma non includere puntini di sospensione.
-   Fare riferimento ai pulsanti di menu della barra degli strumenti in base alle etichette e al menu delle parole. Usare il testo esatto dell'etichetta, inclusa l'uso di maiuscole e minuscole.
-   Fare riferimento ai controlli barra degli strumenti in genere come pulsanti della barra degli strumenti.
-   Per descrivere l'interazione dell'utente, usare fare clic per i pulsanti della barra degli strumenti e gli elenchi a discesa di sola lettura e immettere per gli elenchi a discesa modificabili. Non usare scegliere, selezionare o selezionare.
-   Non usare la propagazione, l'elenco a discesa, l'elenco a discesa o il popup per descrivere i pulsanti di menu, ad eccezione della documentazione di programmazione.
-   Fare riferimento agli elementi non disponibili come non disponibili, non in grigio, disabilitati o in grigio. Usare disabled nella documentazione di programmazione.
-   Quando possibile, formattare le etichette usando il testo in grassetto. In caso contrario, inserire le etichette tra virgolette solo se necessario per evitare confusione.

Esempi:

-   Scegliere **Invia** pagina tramite posta elettronica dal menu Pagina sulla barra **degli strumenti.**
-   Nella casella **Tipi di** carattere sulla barra degli strumenti immettere "Segoe UI".
-   Sulla barra **degli strumenti** Formattazione scegliere **Mostra** e quindi fare clic **su Commenti**.

 

