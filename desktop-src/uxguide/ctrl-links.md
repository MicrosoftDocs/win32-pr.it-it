---
title: Collegamenti
description: Con un collegamento, gli utenti possono passare a un'altra pagina, a una finestra o a un argomento della Guida; visualizzare una definizione; avviare un comando; in alternativa, scegliere un'opzione.
ms.assetid: a23748e4-b2dd-4b9f-9a7c-ff6533922c8c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 521f96146de535210d79814b375499ea34399179
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104565536"
---
# <a name="links"></a>Collegamenti

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con un *collegamento*, gli utenti possono passare a un'altra pagina, a una finestra o a un argomento della Guida; visualizzare una definizione; avviare un comando; in alternativa, scegliere un'opzione. Un collegamento è un testo o un elemento grafico che indica che è possibile fare clic su di esso, in genere visualizzando utilizzando i colori del [sistema di collegamento](vis-color.md)visitati o non visitati. Tradizionalmente, i collegamenti sono sottolineati, ma questo approccio è spesso superfluo e non è più adatto per ridurre il disordine visivo.

Quando si passa il mouse su un collegamento, il testo del collegamento viene visualizzato come sottolineato (se non era già presente) e la forma del puntatore passa a una [mano](inter-mouse.md).

Un collegamento di testo è il controllo selezionabile con il peso più chiaro e viene spesso utilizzato per ridurre la complessità visiva di una progettazione.

> [!Note]  
> Le linee guida correlate ai collegamenti e al [layout](vis-layout.md) del [comando](ctrl-command-links.md) sono presentate in articoli distinti.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **È il collegamento utilizzato per passare a un'altra pagina, a una finestra o a un argomento della Guida; visualizzare una definizione; avviare un comando; oppure scegliere un'opzione?** Se non è così, usa un altro controllo.
-   **Un pulsante di comando è la scelta migliore?** Usare un [pulsante di comando](ctrl-command-buttons.md) se:
    -   Il controllo avvia un'azione immediata, inclusa la visualizzazione di una finestra, e tale comando è correlato allo scopo principale della finestra.
    -   Viene visualizzata una finestra per raccogliere l'input o le scelte, anche se per un comando secondario.
    -   L'etichetta è breve, composta da quattro o meno parole, evitando così l'aspetto imbarazzante dei pulsanti lunghi.
    -   Il comando non è inline.
    -   Il controllo viene visualizzato all'interno di un gruppo di altri pulsanti di comando correlati.
    -   L'azione è distruttiva o irreversibile. Poiché gli utenti associano i collegamenti con la navigazione (e la possibilità di eseguire il backup), i collegamenti non sono appropriati per i comandi con conseguenze significative.
    -   Analogamente, in una [procedura guidata](win-wizards.md) o un [flusso di attività](glossary.md), il comando rappresenta l'impegno. In tali finestre, i pulsanti di comando suggeriscono un impegno mentre i collegamenti suggeriscono lo spostamento al passaggio successivo.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

**Creazione di collegamenti riconoscibili**

I collegamenti non dispongono di [convenienza](glossary.md), il che significa che **le proprietà visive non suggeriscono come vengono usate** e sono comprese solo tramite esperienza. I collegamenti senza una sottolineatura e i colori del sistema di collegamento vengono visualizzati come testo normale; l'unico modo per verificare il comportamento è dalla presentazione, dal contesto o dal posizionamento del puntatore su di essi.

Sorprendentemente, questa mancanza di convenienza è spesso una motivazione per l'uso dei collegamenti perché appaiono così leggeri, riducendo così la complessità visiva di una progettazione. I collegamenti eliminano il frame visivamente intenso usato dai [pulsanti di comando](ctrl-command-buttons.md) e dal bordo usati da altri controlli. Ad esempio, anche se è possibile usare i pulsanti di comando per rendere evidenti i comandi primari, è possibile scegliere i collegamenti per i comandi secondari per deaccentuarli.

Il problema è quindi tenere traccia di un numero sufficiente di indizi visivi, in modo che gli utenti possano riconoscere i collegamenti. Le linee guida fondamentali sono **gli utenti che devono essere in grado di riconoscere i collegamenti solo tramite l'ispezione visiva, non devono passare il puntatore su un oggetto o fare clic su di esso per determinare se si tratta di un collegamento**.

Se il collegamento USA i [colori del sistema di collegamento](vis-color.md) e almeno uno dei seguenti indizi visivi, gli utenti possono riconoscere un collegamento solo tramite l'ispezione visiva:

-   Testo sottolineato.
-   Grafico o punto elenco, ad esempio con il [testo con il modello di collegamento all'icona](#usage-patterns) .
-   Selezione host all'interno di un percorso, un'opzione o un percorso di comando standard, ad esempio l' [area del contenuto](glossary.md) di una finestra o in una barra di navigazione, una barra dei menu, una barra degli strumenti o un piè di pagina.

Gli utenti possono anche riconoscere un collegamento mediante l'ispezione visiva con i seguenti indizi visivi, ma questi indizi non sono sufficienti da soli:

-   Testo che suggerisce di fare clic, ad esempio un comando che inizia con un verbo imperativo come mostra, stampa, copia o Elimina.
-   Posizionamento all'interno di un blocco di testo normale.

Naturalmente, gli utenti possono sempre determinare un collegamento tramite l'interazione con il puntatore del mouse o facendo clic su di esso. Se l'individuazione di un collegamento non è necessaria per le attività significative, è possibile delineare tali collegamenti.

![screenshot delle etichette grigio sullo sfondo nero ](images/ctrl-links-image1.png)

In questo esempio, contattaci, condizioni per l'utilizzo, marchi e informativa sulla privacy sono collegamenti. Sono delineati intenzionalmente perché non sono necessari per le attività importanti. Gli unici indizi che sono collegamenti sono che hanno un puntatore del mouse al passaggio del mouse e sono posizionati in un'area di navigazione standard nella parte inferiore della finestra.

**Creazione di collegamenti specifici, pertinenti e prevedibili**

Il testo del collegamento indicherà il risultato della selezione del collegamento.

I collegamenti specifici sono più interessanti per gli utenti rispetto ai collegamenti generali. utilizzare quindi le etichette dei collegamenti **che forniscono informazioni descrittive specifiche sul risultato della selezione del collegamento**. Tuttavia, assicurarsi che il testo del collegamento non sia così specifico che è fuorviante e che sconsiglia l'uso corretto.

È più probabile che i collegamenti concisi siano letti rispetto ai collegamenti dettagliati. **Eliminare il testo e i dettagli superflui.** Le etichette di collegamento non devono essere complete.

Per valutare il testo del collegamento:

-   Verificare che il testo del collegamento rispecchi gli scenari supportati dal collegamento.
-   Verificare che i risultati del collegamento siano prevedibili. I risultati non devono essere sorpresi dagli utenti.

**Se si eseguono solo due operazioni...**

1. Rendere individuabili i collegamenti solo tramite controllo visivo. Gli utenti non devono interagire con il programma per trovare i collegamenti.

2. Usare i collegamenti che forniscono informazioni descrittive specifiche sul risultato della selezione del collegamento, usando la quantità di testo necessaria. Gli utenti devono essere in grado di prevedere accuratamente il risultato di un collegamento dal testo del collegamento e da [infotip](ctrl-tooltips-and-infotips.md)facoltativi.

## <a name="usage-patterns"></a>Modelli di utilizzo

I collegamenti includono diversi modelli funzionali:



|                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Collegamenti di navigazione**<br/> Un collegamento usato per passare a un'altra pagina o a un'altra finestra. <br/>                                                      | Facendo clic sul collegamento si passa a un'altra pagina, come in una finestra del browser o in una procedura guidata. in alternativa, viene visualizzata una nuova finestra. A differenza dei collegamenti alle attività, la navigazione non avvia un'attività ma passa semplicemente a un'altra posizione o procede con un'attività già in corso. La navigazione implica la sicurezza perché l'utente può sempre tornare indietro.<br/> Titoli di notizie<br/> In questo esempio, facendo clic sul collegamento si passa alla pagina dei titoli delle notizie.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Collegamenti alle attività**<br/> Collegamento utilizzato per avviare un nuovo comando. <br/>                                                                        | Facendo clic sul collegamento viene eseguito immediatamente un comando oppure viene visualizzata una finestra di dialogo o una pagina per raccogliere più input. A differenza dei collegamenti di navigazione, i collegamenti alle attività avviano una nuova attività anziché continuare con un'attività esistente. Le attività non implicano che safetyusers non possa ripristinare lo stato precedente con un comando back. I collegamenti alle attività sono così chiamati per evitare confusione con i [collegamenti ai comandi](ctrl-command-links.md). <br/> Accedi<br/> In questo esempio, facendo clic sul collegamento viene avviato un comando di accesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Collegamenti alla guida**<br/> Collegamento di testo utilizzato per visualizzare un argomento della guida. <br/>                                                                     | Facendo clic sul collegamento viene visualizzato un articolo della Guida in una finestra separata.<br/> Che cos'è una password complessa?<br/> In questo esempio, facendo clic sul collegamento viene visualizzata una finestra della guida con l'argomento specificato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Collegamenti alla definizione**<br/> un collegamento di testo usato per visualizzare una definizione in un infotip quando l'utente fa clic su o passa il puntatore del mouse sul collegamento. <br/> | Questo modello è utile per definire i termini che potrebbero non essere noti agli utenti senza aggiungere disordine dello schermo.<br/> ![Screenshot di infotip visualizzato dal passaggio del mouse ](images/ctrl-links-image2.png)<br/> In questo esempio viene visualizzata la definizione infotip. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Collegamenti a menu**<br/> set di collegamenti alle attività usato per creare un menu. <br/>                                                                    | Poiché il contesto del menu indica un set di collegamenti, il testo non è in genere sottolineato (eccetto al passaggio del mouse) e potrebbe non usare i colori del sistema di collegamento.<br/> ![Screenshot di un set di collegamenti ](images/ctrl-links-image3.png)<br/> In questo esempio, un set di collegamenti crea un menu.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Collegamenti alle opzioni**<br/> opzione selezionata o segnaposto, in cui fare clic sul collegamento richiama un comando per modificare tale opzione.<br/>       | a differenza dei collegamenti di testo normali, il collegamento modifica il testo in modo che corrisponda all'opzione attualmente selezionata e viene sempre disegnato usando il colore del collegamento non visitato. <br/> ![Screenshot di una regola nella procedura guidata delle regole di Outlook ](images/ctrl-links-image4.png)<br/> Nell'esempio a sinistra viene visualizzata una regola della procedura guidata delle regole di Microsoft Outlook con le opzioni segnaposto. Quando gli utenti fanno clic sui collegamenti e selezionano alcune opzioni, nell'esempio a destra viene aggiornato il testo del collegamento per visualizzare i risultati.<br/> l'uso di collegamenti di opzione è particolarmente adatto se le opzioni hanno un formato variabile. <br/> ![Screenshot di una regola modificata nella creazione guidata delle regole ](images/ctrl-links-image5.png)<br/> L'esempio a destra mostra che le regole di Outlook hanno un formato variabile. <br/> ![screenshot della modalità di modifica del testo nell'elenco a discesa ](images/ctrl-links-image6.png)<br/> Nell'esempio a sinistra viene visualizzato un collegamento all'opzione. Se selezionato, diventa un elenco a discesa, come illustrato a destra.<br/> |



 

I collegamenti includono inoltre diversi modelli di presentazione:



|                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Collegamenti testo normale**<br/> sono costituiti solo da testo. <br/>                                      | Questa presentazione è la più flessibile perché può essere usata ovunque, incluso [inline](glossary.md).<br/> ![screenshot del testo del collegamento blu ](images/ctrl-links-image7.png)<br/> In questo esempio, il colore del testo identifica chiaramente un collegamento inline.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Testo con collegamenti a icone**<br/> testo con un'icona precedente che indica la relativa funzione.<br/> | Poiché il grafico fornisce un'indicazione visiva aggiuntiva di un collegamento, è più facile da riconoscere come collegamento rispetto a un collegamento di testo normale non sottolineato. Questo modello USA in genere un'icona con 16x16 pixel.<br/> ![screenshot dell'elenco di quattro collegamenti con icone ](images/ctrl-links-image8.png)<br/> in questo esempio, le icone forniscono un'ulteriore indicazione visiva di un collegamento.<br/> ![screenshot del comando Play con un piccolo triangolo ](images/ctrl-links-image9.png)<br/> In questo esempio, il simbolo di riproduzione triangolare standard indica che questo testo è un comando.<br/>                                                                                                                                     |
| **Collegamenti solo grafica**<br/> sono costituiti solo da un grafico.<br/>                               | Data la mancanza di un collegamento di testo, non è disponibile alcun colore di collegamento o sottolineatura per indicare il collegamento. questi collegamenti dipendono dalla progettazione grafica per suggerire il clic o dal testo all'interno dell'immagine che suggerisce un'azione quando gli utenti fanno clic. i collegamenti grafici solo a volte presentano un effetto del mouse per indicare il collegamento. Questo approccio consente, ma non è individuabile da solo ispezione visiva.<br/> ![screenshot dell'icona con collegamento-Seleziona puntatore del mouse ](images/ctrl-links-image10.png)<br/> In questo esempio il collegamento non è individuabile dall'ispezione visiva da solo.<br/> **A causa dei potenziali problemi di riconoscimento e localizzazione, i collegamenti solo grafici non sono consigliati come unico modo per eseguire un'attività.** <br/> |



 

## <a name="guidelines"></a>Indicazioni

### <a name="interaction"></a>Interazione

-   **Visualizza un puntatore occupato se il risultato della selezione di un collegamento non è istantaneo.** Senza commenti, gli utenti potrebbero presupporre che il clic non sia stato fatto, quindi fare clic di nuovo su.

### <a name="color"></a>Colore

-   **Usare i colori di sistema del tema o del collegamento per i collegamenti visitati e non visitati.** Il significato di questi colori è coerente in tutti i programmi. Se per qualsiasi motivo gli utenti non amano questi colori (ad esempio per motivi di accessibilità), possono modificarli autonomamente.
-   **Per i collegamenti di navigazione, usare colori diversi per i collegamenti visitati e non visitati.** Mantieni la cronologia dei collegamenti visitati solo per la durata dell'istanza del programma. Il colore visitato è importante per indicare la posizione in cui gli utenti sono già stati evitando di rivisitare le stesse pagine ripetutamente.
-   **Per altri tipi di collegamenti, non usare il colore dei collegamenti visitati.** Il valore non è sufficiente per identificare i comandi "visitati", ad esempio.
-   **Non colora il testo che non è un collegamento perché gli utenti possono presumere che sia un collegamento.** Usare il testo in grassetto o una sfumatura di grigio, in cui altrimenti si userebbe un testo colorato.
-   **Eccezione**: è possibile usare un testo colorato se tutti i collegamenti sono sottolineati o posizionati in percorsi di navigazione o di comando standard.

    **Non corretto:**

    ![screenshot del messaggio del piano di risparmio energia con testo blu ](images/ctrl-links-image11.png)

    In questo esempio il testo blu viene erroneamente usato per il testo che non è un collegamento.

-   **Usare i colori di sfondo che si differenziano dai colori dei collegamenti.** Il [colore di sistema della finestra](vis-color.md) è sempre una scelta ottimale.

    **Non corretto:**

    ![screenshot del testo del collegamento blu sullo sfondo blu ](images/ctrl-links-image12.png)

    In questo esempio, il colore di sfondo fornisce un contrasto scarso con il colore del collegamento.

### <a name="underlining"></a>Sottolineando

-   **Per i collegamenti necessari per eseguire un'attività primaria, fornire indizi visivi in modo che gli utenti possano riconoscere i collegamenti solo tramite controllo visivo.** Questi indizi includono la sottostruttura, i grafici o i punti elenco e le posizioni dei collegamenti standard. Gli utenti non devono passare il puntatore del mouse su un oggetto o provare a fare clic su di esso per determinare se si tratta di un collegamento. Usare il testo sottolineato se il collegamento non è ovvio dal contesto.
-   **Non sottolineare il testo che non è un collegamento perché gli utenti possono supporre che si tratta di un collegamento.** Usare i corsivo in cui si utilizzerebbe il testo sottolineato. Riservare la sottostruttura solo per i collegamenti.
-   **Quando si esegue la stampa, non stampare sottolineature o colori di collegamento.** I collegamenti stampati non hanno alcun valore e sono potenzialmente confusi.

### <a name="text-with-icon-links"></a>Testo con collegamenti a icone

-   **Usare l'icona freccia solo per i collegamenti ai comandi.** I collegamenti regolari non devono utilizzare l'icona a forma di freccia a meno che non vengano utilizzati come sostituti per i [collegamenti ai comandi](ctrl-command-links.md) in Windows XP.
-   **Posizionare l'icona a sinistra del testo.** L'icona deve condurre visivamente il testo.

**Corretto:**

![cattura di schermata dell'icona del testo precedente ](images/ctrl-links-image13.png)

**Non corretto:**

![screenshot dell'icona che segue il testo ](images/ctrl-links-image14.png)

Nell'esempio errato, l'icona non determina il testo.

-   **Fare clic sull'icona come risultato facendo clic sul testo.** Altrimenti sarebbe imprevisto e confuso.

### <a name="graphics-only-links"></a>Collegamenti solo grafica

-   **Non usare collegamenti solo grafica.** Gli utenti li riconoscono come collegamenti e il testo all'interno del grafico (usato per indicare l'azione quando si fa clic) crea un problema di localizzazione.

### <a name="navigation-links"></a>Collegamenti di navigazione

-   **Assicurarsi che i collegamenti di navigazione non richiedano un impegno.** Gli utenti devono essere sempre in grado di tornare allo stato iniziale, usando indietro per la navigazione inplace o Annulla per chiudere una nuova finestra.
-   **Collegamento a contenuto specifico anziché al contenuto generale.** Ad esempio, è preferibile collegarsi alla sezione pertinente di un documento rispetto al collegamento all'inizio.
-   **Utilizzare un collegamento solo se il materiale collegato è pertinente, utile e non ridondante.** Usare il vincolo nei collegamenti di navigazione non usarli solo perché è possibile.
-   **Se un collegamento passa a un sito esterno, inserire l'URL in infotip in** modo che gli utenti possano determinare la destinazione del collegamento.
-   **Collegare solo la prima occorrenza del testo del collegamento.** I collegamenti ridondanti non sono necessari e possono rendere il testo difficile da leggere.

    **Corretto:**

    La cartella Pictures semplifica la condivisione delle immagini. È possibile utilizzare le attività nelle immagini per inviare le immagini in un messaggio di posta elettronica o pubblicarle in una posizione sicura e privata sul Web. È anche possibile stampare le immagini direttamente dalla cartella immagini.

    **Non corretto:**

    La cartella Pictures semplifica la condivisione delle immagini. È possibile utilizzare le attività nelle immagini per inviare le immagini in un messaggio di posta elettronica o pubblicarle in una posizione sicura e privata sul Web. È anche possibile stampare le immagini direttamente dalla cartella immagini.

    Nell'esempio corretto, viene collegata solo la prima occorrenza del testo pertinente.

    **Eccezioni**

    -   **Se un'istruzione dispone di un collegamento, inserire il collegamento nell'istruzione.**

        L'utilizzo di password complesse è molto importante. Per altre informazioni, vedere Password complesse.

        In questo esempio il collegamento è nell'istruzione invece che nella prima occorrenza.

    -   **Collegamento a occorrenze successive se sono lontani dalla prima.** Ad esempio, è possibile collegarsi in maniera ridondante in sezioni diverse all'interno di un argomento della guida.

### <a name="task-links"></a>Collegamenti alle attività

-   **Usare i collegamenti alle attività per i comandi che non sono distruttivi o sono facilmente reversibili.** Poiché gli utenti associano i collegamenti con la navigazione (e la possibilità di eseguire il backup), i collegamenti non sono appropriati per i comandi con conseguenze significative. I comandi che visualizzano una finestra di dialogo o una conferma rappresentano una scelta ottimale.

    **Corretto:**

    Inizia

    Stop

    **Non corretto:**

    Elimina file

    Nell'esempio errato, il comando è distruttivo.

### <a name="menu-links"></a>Collegamenti a menu

-   **Raggruppare i collegamenti delle attività e di navigazione nei menu.** Un menu di collegamenti correlati posizionati all'interno di un percorso di navigazione o comando standard semplifica la ricerca e la comprensione dei collegamenti rispetto a quando vengono posizionati separatamente.
-   **Per i menu dipendenti dalla selezione, rimuovere i collegamenti di menu che non si applicano.** Non disabilitarli. Questa operazione elimina il disordine e gli utenti non perderanno i collegamenti che richiedono la selezione.
-   **Per i menu indipendenti dalla selezione, disabilitare i collegamenti al menu che non si applicano.** Non rimuoverli. In questo modo i menu risultano più stabili e tali collegamenti sono più facili da trovare.

    ![screenshot della finestra di dialogo con il comando di menu in grigio ](images/ctrl-links-image15.png)

    In questo esempio da Windows Update, viene eseguito un aggiornamento, quindi il comando Controlla aggiornamenti è disabilitato anziché rimosso.

### <a name="link-infotips"></a>Collega infotip

-   Se un collegamento richiede una spiegazione ulteriore, **fornire la spiegazione in una spiegazione aggiuntiva in un controllo testo separato o in un** [infotip](ctrl-tooltips-and-infotips.md), ma non in entrambi. Usare le frasi complete e la punteggiatura finale. Se il testo è lo stesso, non è necessario fornire entrambe le differenze se il testo è diverso.

    ![screenshot del collegamento con testo supplementare ](images/ctrl-links-image16.png)

    In questo esempio, una spiegazione supplementare fornisce ulteriori informazioni sul collegamento.

    ![screenshot del collegamento con infotip ](images/ctrl-links-image17.png)

    In questo esempio, un infotip fornisce ulteriori informazioni.

-   **Non fornire un infotip che è semplicemente una ripubblicazione del testo del collegamento.**

    **Non corretto:**

    ![screenshot del collegamento con infotip ridondante ](images/ctrl-links-image18.png)

    In questo esempio, il infotip rischia di infastidire gli utenti in base alla sua ripetibilità.

## <a name="text"></a>Testo

-   Non assegnare una [chiave di accesso](glossary.md). Per accedere ai collegamenti, utilizzare il tasto TAB.
-   **Usare i collegamenti che forniscono informazioni descrittive specifiche sul risultato della selezione del collegamento**, usando la quantità di testo necessaria. Il testo del collegamento indicherà il risultato della selezione del collegamento. **Gli utenti devono essere in grado di prevedere accuratamente il risultato di un collegamento dal testo del collegamento e da infotip facoltativi.**

    **Non corretto:**

    ![Screenshot di un collegamento avviso di avviso di sicurezza ](images/ctrl-links-image19.png)

    In questo esempio, anche se il collegamento risulta importante, l'etichetta è troppo generale. È più probabile che gli utenti clicchino su un collegamento più specifico.

-   Per i collegamenti inline:
    -   Mantenere le lettere maiuscole e punteggiatura del testo.
    -   Non includere la punteggiatura finale nel collegamento, a meno che il testo non sia una domanda.
    -   Collegamento alla parte più pertinente del testo e scegliere il testo del collegamento sufficientemente grande da fare clic.

        **Corretto:**

        Passare a un newsgroup.

        **Non corretto:**

        Passare a un newsgroup.

        In questi esempi, "go" non è la parte più pertinente del testo e non è sufficientemente grande da creare una buona destinazione di clic, mentre "newsgroup" è.

    -   **Evitare di inserire due collegamenti inline diversi l'uno accanto all'altro.** È probabile che gli utenti credano di essere un singolo collegamento.

        **Non corretto:**

        Per altre informazioni, vedere linee guida sull'UX.

        In questo esempio, "UX" e "linee guida" sono due collegamenti diversi.

-   Per i collegamenti indipendenti (non inline):
    -   Usare l'uso [di maiuscole in stile frase](glossary.md).
    -   Non usare la punteggiatura finale a meno che il collegamento non sia una domanda.
    -   Usare tutto il testo come collegamento.
-   Usare i collegamenti che si distinguono chiaramente dagli altri collegamenti sullo schermo. Gli utenti devono essere in grado di prevedere e distinguere accuratamente le destinazioni di collegamento.

    **Non corretto:**

    Trova il software antivirus

    Ottenere il software antivirus

    **Corretto:**

    Come verificare se il software antivirus è installato

    Installare il software antivirus

    Nell'esempio errato, la distinzione tra i due collegamenti non è chiara.

-   Non aggiungere clic o fare clic qui per il testo del collegamento. Non è necessario perché un collegamento implica la selezione. Inoltre, fare clic qui e non fornire informazioni sul collegamento durante la lettura da parte di un lettore di schermate.

    **Non corretto:**

    Fare clic qui per la descrizione.

    **Corretto:**

    Descrizione

    Negli esempi non corretti, "fare clic qui" viene eseguito senza indicare e non vengono fornite informazioni sul collegamento.

**Collegamenti di navigazione**

-   **Avviare il collegamento con un sostantivo e indicare chiaramente dove fare clic sul collegamento.** Non usare punteggiatura finale. In alcuni casi potrebbe essere necessario avviare collegamenti di navigazione con un verbo, ma non usare verbi che riiterano la navigazione che è già implicita nel fatto di collegamento, ad esempio View, Open o go to.
-   **Presentare un collegamento di navigazione come URL se passa a una pagina Web e si prevede che gli utenti di destinazione richiamino l'URL e lo digitano in un browser.** Se possibile, progettare tali URL in modo da essere brevi e facili da ricordare.
-   **Se il collegamento include un URL di un sito Web che inizia con "www", omettere il nome del protocollo https://e utilizzare testo minuscolo.**

    **Non corretto:**

    https://www.microsoft.com

    `www.microsoft.com`

    **Corretto:**

    microsoft.com

    Negli esempi non corretti, le parole "https://" e "www" vengono escluse.

**Collegamenti alle attività**

-   **Avviare il collegamento con un verbo imperativo e descrivere chiaramente l'attività eseguita dal collegamento.** Non usare punteggiatura finale.
-   **Terminare il collegamento con i puntini di sospensione se il comando richiede informazioni aggiuntive (inclusa una conferma) per il corretto completamento.** Non usare i puntini di sospensione quando il completamento dell'attività consiste nel visualizzare un'altra finestra solo quando sono necessarie altre informazioni per eseguire l'attività.

    Stampa...

    In questo esempio, Print... il collegamento al comando Visualizza una finestra di dialogo Stampa per raccogliere ulteriori informazioni.

    Stampa

    Al contrario, in questo esempio un collegamento al comando stampa stampa una singola copia di un documento nella stampante predefinita senza ulteriori interazioni da parte dell'utente.

    L' **uso corretto dei puntini di sospensione è importante per indicare che gli utenti possono effettuare altre scelte prima di eseguire l'attività oppure possono annullare completamente l'attività**. Il segnale visivo offerto dai puntini di sospensione consente agli utenti di esplorare il software senza timore.

-   **Se necessario, terminare un collegamento a un'attività con "Now" per distinguerlo da un collegamento di navigazione.**

    Scaricare i file

    Scarica file adesso

    In questo esempio, "Scarica file" passa a una pagina per il download di file, mentre "Scarica file ora" esegue effettivamente il comando.

**Collegamenti alla guida**

Per linee guida ed esempi, vedere la [Guida](winenv-help.md)di.

**Collega infotip**

-   Usare le frasi complete e la punteggiatura finale.

Per altre linee guida ed esempi, vedere [Tooltips and infotip](ctrl-tooltips-and-infotips.md).

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai collegamenti:

-   Usare il testo esatto del collegamento, inclusa la relativa maiuscola, ma non includere i puntini di sospensione.
-   Per descrivere l'interazione dell'utente, utilizzare fare clic su.
-   Quando possibile, formattare il testo del collegamento utilizzando il testo in grassetto. In caso contrario, inserire il testo del collegamento tra virgolette solo se necessario per evitare confusione.

Esempio: per avviare l'analisi, fare clic su **analizza un computer**.

 

