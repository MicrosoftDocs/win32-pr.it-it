---
title: Collegamenti
description: Con un collegamento, gli utenti possono passare a un'altra pagina, finestra o argomento della Guida. visualizzare una definizione; avviare un comando; o scegliere un'opzione.
ms.assetid: a23748e4-b2dd-4b9f-9a7c-ff6533922c8c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 161313008612d04b5009942f82f662888d1ffd35
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524256"
---
# <a name="links"></a>Collegamenti

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con un *collegamento*, gli utenti possono passare a un'altra pagina, finestra o argomento della Guida. visualizzare una definizione; avviare un comando; o scegliere un'opzione. Un collegamento è un testo o un elemento grafico che indica che è possibile fare clic su di esso, in genere visualizzando i colori del sistema dei collegamenti visitati o [non supervisionati.](vis-color.md) Tradizionalmente, anche i collegamenti sono sottolineati, ma questo approccio è spesso superfluo e non favorisce la riduzione del disordine visivo.

Quando gli utenti passano il puntatore del mouse su un collegamento, il testo del collegamento viene visualizzato come sottolineato (se non lo era già) e la forma del puntatore assume la forma di una [mano.](inter-mouse.md)

Un collegamento di testo è il controllo selezionabile con il peso più leggero e viene spesso usato per ridurre la complessità visiva di una progettazione.

> [!Note]  
> Le linee guida relative [ai collegamenti ai comandi](ctrl-command-links.md) e al [layout](vis-layout.md) sono presentate in articoli separati.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Collegamento usato per passare a un'altra pagina, finestra o argomento della Guida. visualizzare una definizione; avviare un comando; o scegliere un'opzione?** Se non è così, usa un altro controllo.
-   **Un pulsante di comando è una scelta migliore?** Usare un [pulsante di comando](ctrl-command-buttons.md) se:
    -   Il controllo avvia un'azione immediata, inclusa la visualizzazione di una finestra, e tale comando è correlato allo scopo principale della finestra.
    -   Viene visualizzata una finestra per raccogliere input o effettuare scelte, anche se per un comando secondario.
    -   L'etichetta è breve, costituita da quattro o meno parole, evitando così l'aspetto scomodo dei pulsanti lunghi.
    -   Il comando non è inline.
    -   Il controllo viene visualizzato all'interno di un gruppo di altri pulsanti di comando correlati.
    -   L'azione è distruttiva o irreversibile. Poiché gli utenti associano i collegamenti alla navigazione (e la possibilità di eseguire il back-out), i collegamenti non sono appropriati per i comandi con conseguenze significative.
    -   Analogamente, in una procedura [guidata o](win-wizards.md) in un flusso [di attività,](glossary.md)il comando rappresenta l'impegno. In tali finestre i pulsanti di comando suggeriscono impegno, mentre i collegamenti suggeriscono di passare al passaggio successivo.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

**Rendere i collegamenti riconoscibili**

I collegamenti non [dispongono di affordance,](glossary.md)il che significa che **le relative proprietà** visive non suggeriscono come vengono usati e sono compresi solo tramite esperienza. I collegamenti senza sottolineatura e i colori di sistema dei collegamenti vengono visualizzati come testo normale. l'unico modo per verificarne il comportamento è dalla presentazione, dal contesto o posizionando il puntatore su di essi.

Sorprendentemente, questa mancanza di convenienza è spesso una motivazione per l'uso dei collegamenti perché appaiono così leggeri, riducendo così la complessità visiva di una progettazione. I collegamenti eliminano la cornice visivamente pesante usata dai [pulsanti di comando](ctrl-command-buttons.md) e dai bordi usati da altri controlli. Ad esempio, anche se è possibile usare i pulsanti di comando per rendere ovvi i comandi principali, è possibile scegliere i collegamenti per i comandi secondari per de-enfatizzarli.

La sfida consiste quindi nel mantenere un numero sufficiente di indizi visivi in modo che gli utenti possano riconoscere i collegamenti. La linea guida fondamentale è che gli utenti devono essere in grado di riconoscere i collegamenti solo tramite ispezione visiva e non devono passare il puntatore del mouse su un oggetto o fare clic su di esso per determinare se si tratta di **un collegamento**.

Gli utenti possono riconoscere un collegamento solo [](vis-color.md) tramite ispezione visiva se il collegamento usa i colori del sistema di collegamento e almeno uno degli indizi visivi seguenti:

-   Testo sottolineato.
-   Un elemento grafico o un punto elenco, ad esempio con il [testo con il modello di collegamento icona.](#usage-patterns)
-   Posizionamento all'interno di una posizione standard di navigazione, opzione o comando, ad esempio [l'area](glossary.md) del contenuto di una finestra o in una barra di spostamento, una barra dei menu, una barra degli strumenti o un piè di pagina.

Gli utenti possono anche riconoscere un collegamento tramite ispezione visiva con gli indizi visivi seguenti, ma questi indizi non sono sufficienti da soli:

-   Testo che suggerisce di fare clic, ad esempio un comando che inizia con un verbo imperativo come Show, Print, Copy o Delete.
-   Posizionamento all'interno di un blocco di testo normale.

Naturalmente, gli utenti possono sempre determinare un collegamento tramite l'interazione al passaggio del mouse o facendo clic. Se l'individuazione di un collegamento non è necessaria per attività significative, è possibile de-evidenziare tali collegamenti.

![Screenshot di etichette grigie su sfondo nero ](images/ctrl-links-image1.png)

In questo esempio, Contattaci, Condizioni per l'utilizzo, Marchi e Informativa sulla privacy sono collegamenti. Vengono intenzionalmente de-sottolineate perché non sono necessarie per attività importanti. Gli unici indizi che si tratta di collegamenti sono che hanno un puntatore del mouse al passaggio del mouse e sono posizionati in un'area di spostamento standard nella parte inferiore della finestra.

**Creazione di collegamenti specifici, pertinenti e prevedibili**

Il testo del collegamento dovrebbe indicare il risultato del clic sul collegamento.

I collegamenti specifici sono più interessanti per gli utenti rispetto ai collegamenti generali, quindi usare etichette di collegamento che forniscono informazioni descrittive specifiche sul risultato del clic **sul collegamento.** Assicurarsi tuttavia che il testo del collegamento non sia così specifico da essere fuorviante e sconsiglia l'uso corretto.

È più probabile che i collegamenti concisi siano letti rispetto ai collegamenti dettagliati. **Eliminare testo e dettagli non necessari.** Le etichette di collegamento non devono essere complete.

Per valutare il testo del collegamento:

-   Assicurarsi che il testo del collegamento rifletta gli scenari supportati dal collegamento.
-   Assicurarsi che i risultati del collegamento siano prevedibili. Gli utenti non devono essere sorprese dai risultati.

**Se si eservino solo due operazioni...**

1. Rendere i collegamenti individuabili solo tramite ispezione visiva. Gli utenti non devono interagire con il programma per trovare i collegamenti.

2. Usare collegamenti che forniscono informazioni descrittive specifiche sul risultato del clic sul collegamento, usando il testo necessario. Gli utenti devono essere in grado di stimare in modo accurato il risultato di un collegamento dal testo del collegamento e dalla descrizione [comando facoltativa.](ctrl-tooltips-and-infotips.md)

## <a name="usage-patterns"></a>Modelli di utilizzo

I collegamenti hanno diversi modelli funzionali:



|    Utilizzo                  |    Esempio   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Collegamenti di spostamento**<br/> Collegamento usato per passare a un'altra pagina o finestra. <br/>                                                      | Facendo clic sul collegamento si passa a un'altra pagina, come in una finestra del browser o in una procedura guidata. o visualizza una nuova finestra. A differenza dei collegamenti alle attività, la navigazione non avvia un'attività, ma semplicemente passa a un'altra posizione o procede con un'attività già in corso. La navigazione implica la sicurezza perché l'utente può sempre tornare indietro.<br/> Notizie<br/> In questo esempio, facendo clic sul collegamento si passa alla pagina Titoli delle notizie.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Collegamenti alle attività**<br/> Collegamento usato per avviare un nuovo comando. <br/>                                                                        | Facendo clic sul collegamento viene eseguito immediatamente un comando oppure viene visualizzata una finestra di dialogo o una pagina per raccogliere più input. A differenza dei collegamenti di navigazione, i collegamenti alle attività avviano una nuova attività invece di continuare con un'attività esistente. Le attività non implicano che gli utenti di sicurezza non possano ripristinare lo stato precedente con un comando Indietro. I collegamenti alle attività vengono chiamati così per evitare confusione con [i collegamenti di comando.](ctrl-command-links.md) <br/> Accedi<br/> In questo esempio, facendo clic sul collegamento viene avviato un comando di accesso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Collegamenti alla Guida**<br/> Collegamento di testo utilizzato per visualizzare un argomento della Guida. <br/>                                                                     | Facendo clic sul collegamento viene visualizzato un articolo della Guida in una finestra separata.<br/> Che cos'è una password complessa?<br/> In questo esempio, facendo clic sul collegamento viene visualizzata una finestra della Guida con l'argomento specificato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Collegamenti alle definizioni**<br/> un collegamento di testo usato per visualizzare una definizione in un suggerimento quando l'utente fa clic o passa il puntatore del mouse sul collegamento. <br/> | questo modello è utile per definire termini che potrebbero non essere noti agli utenti senza aggiungere confusione sullo schermo.<br/> ![Screenshot della descrizione comando visualizzata al passaggio del mouse ](images/ctrl-links-image2.png)<br/> In questo esempio viene visualizzata la definizione della descrizione comando. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Collegamenti di menu**<br/> un set di collegamenti di attività usati per creare un menu. <br/>                                                                    | Poiché il contesto del menu indica un set di collegamenti, il testo non viene in genere sottolineato (ad eccezione del passaggio del mouse) e potrebbe non usare i colori del sistema dei collegamenti.<br/> ![Screenshot di un set di collegamenti ](images/ctrl-links-image3.png)<br/> In questo esempio un set di collegamenti crea un menu.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Collegamenti alle opzioni**<br/> un'opzione selezionata o il relativo segnaposto, in cui facendo clic sul collegamento viene richiamato un comando per modificare tale opzione.<br/>       | A differenza dei collegamenti di testo normali, il testo del collegamento cambia in base all'opzione attualmente selezionata e viene sempre disegnato usando il colore del collegamento non supervisionato. <br/> ![Screenshot di una regola nella procedura guidata regole di Outlook ](images/ctrl-links-image4.png)<br/> L'esempio a sinistra mostra una regola della procedura guidata delle regole di Microsoft Outlook con opzioni segnaposto. Dopo che gli utenti hanno fatto clic sui collegamenti e selezionato alcune opzioni, l'esempio a destra aggiorna il testo del collegamento per visualizzare i risultati.<br/> L'uso di collegamenti di opzione è particolarmente adatto se le opzioni hanno un formato variabile. <br/> ![Screenshot di una regola modificata nella procedura guidata per le regole ](images/ctrl-links-image5.png)<br/> L'esempio a destra mostra che le regole di Outlook hanno un formato variabile. <br/> ![Screenshot della modalità di modifica del testo nell'elenco a discesa ](images/ctrl-links-image6.png)<br/> L'esempio a sinistra mostra un collegamento di opzione. Se selezionata, diventa un elenco a discesa, come illustrato a destra.<br/> |



 

I collegamenti hanno anche diversi modelli di presentazione:



|    Utilizzo                                 |    Esempio                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Collegamenti in testo normale**<br/> è costituito solo da testo. <br/>                                      | Questa presentazione è la più flessibile perché può essere usata ovunque, incluso [inline.](glossary.md)<br/> ![Screenshot del testo del collegamento blu ](images/ctrl-links-image7.png)<br/> In questo esempio il colore del testo identifica chiaramente un collegamento inline.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Testo con collegamenti icona**<br/> testo con un'icona precedente che ne indica la funzione.<br/> | Poiché l'elemento grafico fornisce un'indicazione visiva aggiuntiva di un collegamento, è più facile riconoscerlo come collegamento rispetto a un collegamento di testo normale non sottolineato. Questo modello usa in genere un'icona di 16x16 pixel.<br/> ![Screenshot dell'elenco di quattro collegamenti con icone ](images/ctrl-links-image8.png)<br/> In questo esempio le icone forniscono un'indicazione visiva aggiuntiva di un collegamento.<br/> ![Screenshot del comando play con triangolo piccolo ](images/ctrl-links-image9.png)<br/> In questo esempio il simbolo di riproduzione triangolare standard indica che questo testo è un comando.<br/>                                                                                                                                     |
| **Collegamenti solo grafica**<br/> è costituito solo da un elemento grafico.<br/>                               | Data la mancanza di un collegamento di testo, non è presente alcun colore o sottolineatura del collegamento per indicare il collegamento. Questi collegamenti dipendono dalla progettazione grafica per suggerire il clic o dal testo all'interno dell'elemento grafico che suggerisce un'azione quando gli utenti fa clic. I collegamenti solo grafici talvolta hanno un effetto di passaggio del mouse per indicare il collegamento. Questo approccio è utile, ma non è individuabile solo tramite l'ispezione visiva.<br/> ![Screenshot dell'icona con il puntatore del mouse di selezione collegamento ](images/ctrl-links-image10.png)<br/> In questo esempio il collegamento non è individuabile solo tramite l'ispezione visiva.<br/> **A causa dei potenziali problemi di riconoscimento e localizzazione, i collegamenti solo grafici non sono consigliati come unico modo per eseguire un'attività.** <br/> |



 

## <a name="guidelines"></a>Indicazioni

### <a name="interaction"></a>Interazione

-   **Visualizzare un puntatore occupato se il risultato della selezione di un collegamento non è istantaneo.** Senza commenti e suggerimenti, gli utenti potrebbero presupporre che il clic non sia stato fatto e fare di nuovo clic.

### <a name="color"></a>Color

-   **Usare il tema o i colori del sistema di collegamento per i collegamenti visitati e non visitati.** Il significato di questi colori è coerente in tutti i programmi. Se per qualsiasi motivo gli utenti non desiderano questi colori (ad esempio per motivi di accessibilità), possono modificarli.
-   **Per i collegamenti di navigazione, usare colori diversi per i collegamenti visitati e non visitati.** Mantenere la cronologia dei collegamenti visitati solo per la durata dell'istanza del programma. Il colore visitato è importante per indicare dove sono già stati gli utenti, impedendo loro di rivedere involontariamente le stesse pagine ripetutamente.
-   **Per altri tipi di collegamenti, non usare il colore dei collegamenti visitati.** L'identificazione dei comandi "visitati", ad esempio, non ha valore sufficiente.
-   **Non colorare il testo che non è un collegamento perché gli utenti potrebbero presupporre che si tratta di un collegamento.** Usare il grassetto o una sfumatura di grigio in cui altrimenti si userebbe testo colorato.
-   **Eccezione:** è possibile usare testo colorato se tutti i collegamenti sono sottolineati o posizionati all'interno di percorsi di spostamento o comandi standard.

    **Non corretto:**

    ![Screenshot del messaggio di combinazione per il risparmio di energia con testo blu ](images/ctrl-links-image11.png)

    In questo esempio il testo blu viene usato erroneamente per il testo che non è un collegamento.

-   **Usare colori di sfondo in contrasto con i colori dei collegamenti.** Il [colore di sistema della](vis-color.md) finestra è sempre una scelta ottimale.

    **Non corretto:**

    ![Screenshot del testo del collegamento blu sullo sfondo blu ](images/ctrl-links-image12.png)

    In questo esempio, il colore di sfondo offre un contrasto non elevato con il colore del collegamento.

### <a name="underlining"></a>Sottolineando

-   **Per i collegamenti necessari per eseguire un'attività principale, fornire indicazioni visive in modo che gli utenti possano riconoscere i collegamenti solo tramite ispezione visiva.** Questi indizi includono sottolineatura, grafica o punti elenco e posizioni standard dei collegamenti. Gli utenti non devono passare il puntatore del mouse su un oggetto o tentare di fare clic su di esso per determinare se si tratta di un collegamento. Usare il testo sottolineato se il collegamento non è ovvio dal contesto.
-   **Non sottolineare il testo che non è un collegamento perché gli utenti potrebbero presupporre che si tratta di un collegamento.** Usare il corsivo dove altrimenti si userebbe il testo sottolineato. Riservare la sottolineatura solo per i collegamenti.
-   **Durante la stampa, non stampare sottolineature o colori di collegamento.** I collegamenti stampati non hanno alcun valore e possono generare confusione.

### <a name="text-with-icon-links"></a>Testo con collegamenti icona

-   **Usare l'icona a forma di freccia solo per i collegamenti di comando.** I collegamenti normali non devono usare l'icona a forma di freccia a meno che non vengano usati come sostituzione dei [collegamenti di comando](ctrl-command-links.md) in Windows XP.
-   **Posizionare l'icona a sinistra del testo.** L'icona deve portare al testo visivamente.

**Corretto:**

![Screenshot dell'icona che precede il testo ](images/ctrl-links-image13.png)

**Non corretto:**

![Screenshot dell'icona che segue il testo ](images/ctrl-links-image14.png)

Nell'esempio non corretto, l'icona non porta nel testo.

-   **Fare in modo che il risultato della selezione dell'icona sia uguale al clic sul testo.** Altrimenti sarebbe imprevisto e confondere.

### <a name="graphics-only-links"></a>Collegamenti solo grafica

-   **Non usare collegamenti solo grafici.** Gli utenti hanno difficoltà a riconoscerli come collegamenti e qualsiasi testo all'interno dell'elemento grafico (usato per indicare l'azione quando si fa clic su di essi) crea un problema di localizzazione.

### <a name="navigation-links"></a>Collegamenti di spostamento

-   **Assicurarsi che i collegamenti di spostamento non richiedano impegno.** Gli utenti devono essere sempre in grado di tornare allo stato iniziale, usando Indietro per la navigazione sul posto o Annulla per chiudere una nuova finestra.
-   **Collegamento a contenuto specifico anziché a contenuto generale.** Ad esempio, è meglio collegarsi alla sezione pertinente di un documento anziché collegarsi all'inizio.
-   **Usare un collegamento solo se il materiale collegato è rilevante, utile e non ridondante.** L'uso dei collegamenti di navigazione non li usa solo perché è possibile.
-   **Se un collegamento passa a un sito esterno,** inserire l'URL nella descrizione comandi in modo che gli utenti possano determinare la destinazione del collegamento.
-   **Collegare solo la prima occorrenza del testo del collegamento.** I collegamenti ridondanti non sono necessari e possono rendere difficile la lettura del testo.

    **Corretto:**

    La cartella Immagini semplifica la condivisione delle immagini. È possibile usare le attività in Immagini per inviare le immagini tramite posta elettronica o pubblicarle in una posizione sicura e privata sul Web. È anche possibile stampare le immagini direttamente dalla cartella Immagini.

    **Non corretto:**

    La cartella Immagini semplifica la condivisione delle immagini. È possibile usare le attività in Immagini per inviare le immagini tramite posta elettronica o pubblicarle in una posizione sicura e privata sul Web. È anche possibile stampare le immagini direttamente dalla cartella Immagini.

    Nell'esempio corretto viene collegata solo la prima occorrenza del testo pertinente.

    **Eccezioni:**

    -   **Se un'istruzione ha un collegamento, inserire il collegamento nell'istruzione .**

        L'uso di password complesse è molto importante. Per altre informazioni, vedere Password complesse.

        In questo esempio il collegamento si trova nell'istruzione anziché nella prima occorrenza.

    -   **Collegarsi a occorrenze successive, se sono distorsi dalla prima.** Ad esempio, è possibile collegarsi in modo ridondante in sezioni diverse all'interno di un argomento della Guida.

### <a name="task-links"></a>Collegamenti alle attività

-   **Usare i collegamenti alle attività per i comandi non distruttivi o facilmente reversibili.** Poiché gli utenti associano i collegamenti alla navigazione (e la possibilità di tornare indietro), i collegamenti non sono appropriati per i comandi con conseguenze significative. I comandi che visualizzano una finestra di dialogo o una conferma sono una scelta ottimale.

    **Corretto:**

    Inizia

    Stop

    **Non corretto:**

    Elimina file

    Nell'esempio non corretto, il comando è distruttivo.

### <a name="menu-links"></a>Collegamenti di menu

-   **Raggruppare i collegamenti di attività e navigazione correlati nei menu.** Un menu di collegamenti correlati inseriti all'interno di un percorso di spostamento o di comando standard rende più semplice trovare e comprendere i collegamenti rispetto a quando vengono posizionati separatamente.
-   **Per i menu dipendenti dalla selezione, rimuovere i collegamenti di menu non applicabili.** Non disabilitarli. In questo modo si elimina la confusione e gli utenti non perderanno i collegamenti che richiedono la selezione.
-   **Per i menu indipendenti dalla selezione, disabilitare i collegamenti di menu non applicabili.** Non rimuoverli. In questo modo i menu sono più stabili e tali collegamenti sono più facili da trovare.

    ![Screenshot della finestra di dialogo con il comando di menu in grigio ](images/ctrl-links-image15.png)

    In questo esempio Windows Update viene eseguito un aggiornamento, quindi il comando Controlla aggiornamenti è disabilitato anziché rimosso.

### <a name="link-infotips"></a>Suggerimenti per i collegamenti

-   Se un collegamento richiede un'ulteriore spiegazione, fornire la spiegazione in una spiegazione supplementare in un controllo di testo separato o **in** una [descrizione](ctrl-tooltips-and-infotips.md)comando, ma non in entrambi. Usare frasi complete e la punteggiatura finale. Fornire entrambi non è necessario se il testo è lo stesso e confondere se il testo è diverso.

    ![Screenshot del collegamento con testo supplementare ](images/ctrl-links-image16.png)

    In questo esempio, una spiegazione supplementare fornisce altre informazioni sul collegamento.

    ![Screenshot del collegamento con la descrizione comando ](images/ctrl-links-image17.png)

    In questo esempio, una descrizione comando fornisce altre informazioni.

-   **Non fornire una descrizione comando che sia semplicemente una rietichezza del testo del collegamento.**

    **Non corretto:**

    ![Screenshot del collegamento con suggerimento ridondante ](images/ctrl-links-image18.png)

    In questo esempio la descrizione comandi rischia di insodziare gli utenti per la sua ripetitività.

## <a name="text"></a>Testo

-   Non assegnare una chiave [di accesso](glossary.md). È possibile accedere ai collegamenti usando il tasto TAB.
-   **Usare collegamenti che forniscono informazioni descrittive specifiche sul risultato del** clic sul collegamento , usando il testo necessario. Il testo del collegamento dovrebbe indicare il risultato del clic sul collegamento. **Gli utenti devono essere in grado di stimare accuratamente il risultato di un collegamento dal testo del collegamento e dalla descrizione comando facoltativa.**

    **Non corretto:**

    ![Screenshot di un collegamento di avviso relativo all'avviso di sicurezza ](images/ctrl-links-image19.png)

    In questo esempio, anche se il collegamento risulta importante, l'etichetta è troppo generale. È più probabile che gli utenti clicno su un collegamento più specifico.

-   Per i collegamenti inline:
    -   Mantenere le maiuscole e la punteggiatura del testo.
    -   Non includere la punteggiatura finale nel collegamento a meno che il testo non sia una domanda.
    -   Collegarsi alla parte più pertinente del testo e scegliere il testo del collegamento sufficientemente grande da essere facilmente selezionato.

        **Corretto:**

        Passare a un newsgroup.

        **Non corretto:**

        Passare a un newsgroup.

        In questi esempi, "Go" non è la parte più rilevante del testo e non è sufficientemente grande da fare un buon clic come destinazione, mentre il "newsgroup" lo è.

    -   **Evitare di inserire due collegamenti inline diversi uno accanto all'altro.** È probabile che gli utenti creino di essere un singolo collegamento.

        **Non corretto:**

        Per altre informazioni, vedere Linee guida per l'esperienza utente.

        In questo esempio, "UX" e "guidelines" sono due collegamenti diversi.

-   Per i collegamenti indipendenti (non inline):
    -   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
    -   Non usare la punteggiatura finale a meno che il collegamento non sia una domanda.
    -   Usare tutto il testo come collegamento.
-   Usare collegamenti chiaramente differenziati dagli altri collegamenti sullo schermo. Gli utenti devono essere in grado di stimare e distinguere accuratamente le destinazioni di collegamento.

    **Non corretto:**

    Trovare software antivirus

    Ottenere software antivirus

    **Corretto:**

    Come sapere se è installato un software antivirus

    Installare il software antivirus

    Nell'esempio non corretto, la distinzione tra i due collegamenti non è chiara.

-   Non aggiungere Fare clic o Fare clic qui al testo del collegamento. Non è necessario perché un collegamento implica il clic. Inoltre, Fare clic qui e qui da solo non fornisce informazioni sul collegamento quando viene letto da un'utilità per la lettura dello schermo.

    **Non corretto:**

    Fare clic qui per la descrizione.

    **Corretto:**

    Descrizione

    Negli esempi non corretti, "fare clic qui" non viene detto e non fornisce informazioni sul collegamento.

**Collegamenti di navigazione**

-   **Avviare il collegamento con un sostantivo e descrivere chiaramente dove verrà fatto clic sul collegamento.** Non usare punteggiatura finale. In alcuni casi potrebbe essere necessario avviare i collegamenti di navigazione con un verbo, ma non usare verbi che ritienino lo spostamento già implicito dal fatto di eseguire il collegamento, ad esempio Visualizza, Apri o Vai a.
-   **Presentare un collegamento di navigazione come URL se si passa a una pagina Web e si prevede che gli utenti di destinazione richiamino l'URL e lo dimentitino in un browser.** Se possibile, progettare tali URL in modo che siano brevi e facili da ricordare.
-   **Se il collegamento include un URL a un sito Web che inizia con "www", omettere il nome https:// protocollo e usare il testo in minuscolo.**

    **Non corretto:**

    https://www.microsoft.com

    `www.microsoft.com`

    **Corretto:**

    microsoft.com

    Negli esempi non corretti, le parole "https://" e "www" vanno senza dire.

**Collegamenti alle attività**

-   **Avviare il collegamento con un verbo imperativo e descrivere chiaramente l'attività eseguita dal collegamento.** Non usare punteggiatura finale.
-   **Terminare il collegamento con i puntini di sospensione se il comando necessita di informazioni aggiuntive (inclusa una conferma) per il corretto completamento.** Non usare i puntini di sospensione quando il completamento corretto dell'attività è visualizzare un'altra finestra solo quando sono necessarie informazioni aggiuntive per eseguire l'attività.

    Stampa...

    In questo esempio, il comando Stampa... Il collegamento al comando visualizza una finestra di dialogo Stampa per raccogliere altre informazioni.

    Stampa

    Al contrario, in questo esempio un collegamento al comando Stampa stampa una singola copia di un documento sulla stampante predefinita senza ulteriori interazioni con l'utente.

    È importante usare correttamente i puntini di sospensione per indicare che gli utenti possono effettuare altre scelte prima di eseguire l'attività o **annullare completamente l'attività.** Il segnale visivo offerto dai puntini di sospensione consente agli utenti di esplorare il software senza temere.

-   **Se necessario, terminare un collegamento di attività con "now" per distinguerlo da un collegamento di navigazione.**

    Scaricare i file

    Scarica i file ora

    In questo esempio "Download files" (Scarica file) passa a una pagina per il download dei file, mentre "Download files now" (Scarica file ora) esegue effettivamente il comando .

**Collegamenti alla Guida**

Per linee guida ed esempi, vedere [la Guida](winenv-help.md).

**Suggerimenti per i collegamenti**

-   Usare frasi complete e punteggiatura finale.

Per altre linee guida ed esempi, vedere [Descrizioni comando e suggerimenti.](ctrl-tooltips-and-infotips.md)

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai collegamenti:

-   Usare il testo esatto del collegamento, inclusa la relativa maiuscola, ma non includere i puntini di sospensione.
-   Per descrivere l'interazione dell'utente, usare click.
-   Quando possibile, formattare il testo del collegamento usando il testo in grassetto. In caso contrario, inserire il testo del collegamento tra virgolette solo se necessario per evitare confusione.

Esempio: per avviare l'analisi, fare clic **su Analizza un computer**.

 

