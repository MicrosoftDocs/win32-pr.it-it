---
title: Pulsanti di opzione
description: Con un pulsante di opzione, gli utenti possono scegliere tra un set di opzioni correlate che si escludono a vicenda.
ms.assetid: f9af0a8a-d4a1-464c-a967-bab88ae0726b
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 00495695753506702015431c889e74d5a7effe9a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104234450"
---
# <a name="radio-buttons"></a>Pulsanti di opzione

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con un pulsante di opzione, gli utenti possono scegliere tra un set di opzioni correlate che si escludono a vicenda. Gli utenti possono scegliere solo una delle opzioni. I pulsanti di opzione sono chiamati perché funzionano come i set di impostazioni del canale sulle radio.

![Screenshot di tre pulsanti di opzione ](images/radio-buttons-image1.png)

Gruppo tipico di pulsanti di opzione.

Un gruppo di pulsanti di opzione si comporta come un unico controllo. Solo la scelta selezionata è accessibile utilizzando il tasto TAB, ma gli utenti possono scorrere il gruppo utilizzando i tasti di direzione.

> [!Note]  
> Le linee guida relative al [layout](vis-layout.md) e alla [navigazione da tastiera](inter-keyboard.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Il controllo viene usato per scegliere un'opzione da un set di scelte che si escludono a vicenda?** Se non è così, usa un altro controllo. Per scegliere più opzioni, usare invece le [caselle di controllo](ctrl-check-boxes.md), un [elenco a selezione multipla](ctrl-list-boxes.md) o un elenco di caselle di controllo.
-   **Il numero di opzioni tra due e sette?** Poiché lo spazio dello schermo utilizzato è proporzionale al numero di opzioni, è possibile utilizzare il numero di opzioni in un gruppo compreso tra due e sette. Per otto o più opzioni, usare un [elenco a discesa](/windows/desktop/uxguide/ctrl-drop) o un [elenco a selezione singola](ctrl-list-boxes.md).
-   **Una casella di controllo è una scelta migliore?** Se sono disponibili solo due opzioni, è possibile utilizzare invece una sola [casella di controllo](ctrl-check-boxes.md) . Tuttavia, le caselle di controllo sono adatte solo per attivare o disattivare una singola opzione, mentre i pulsanti di opzione possono essere usati per alternative completamente diverse. Se entrambe le soluzioni sono possibili:
    -   Usare i pulsanti di opzione se il significato della casella di controllo deselezionata non è completamente ovvio.

        **Non corretto:**

        ![cattura di schermata della casella di controllo orizzontale ](images/radio-buttons-image2.png)

        **Corretto:**

        ![screenshot dei pulsanti di opzione orizzontale/verticale ](images/radio-buttons-image3.png)

        Nell'esempio corretto, le scelte non sono opposte, quindi i pulsanti di opzione sono la scelta migliore.

    -   Utilizzare pulsanti di opzione nelle pagine della procedura guidata per cancellare le alternative, anche se una casella di controllo è altrimenti accettabile.
    -   Usare i pulsanti di opzione se lo spazio dello schermo è sufficiente e le opzioni sono sufficientemente importanti per essere un buon utilizzo dello spazio dello schermo. In caso contrario, utilizzare un elenco a discesa o una casella di controllo.

        **Non corretto:**

        ![screenshot dei pulsanti di opzione Mostra/non visualizzare ](images/radio-buttons-image4.png)

        In questo esempio, le opzioni non sono sufficientemente importanti da usare i pulsanti di opzione.

        **Corretto:**

        ![screenshot della casella di controllo non visualizzare questo messaggio ](images/radio-buttons-image5.png)

        In questo esempio, una casella di controllo è un uso efficiente dello spazio dello schermo per questa opzione della periferica.

    -   Se nella pagina sono presenti altre caselle di controllo, utilizzare una casella di controllo.

-   **Un elenco a discesa è la scelta migliore?** Se l'opzione predefinita è consigliata per la maggior parte degli utenti nella maggior parte dei casi, i pulsanti di opzione possono attirare una maggiore attenzione sulle opzioni del necessario.
    -   Prendere in considerazione l'uso di un elenco a discesa se non si vuole attirare l'attenzione sulle opzioni o non si vuole incoraggiare gli utenti a apportare modifiche. Un elenco a discesa è incentrato sulla selezione corrente, mentre i pulsanti di opzione enfatizzano equamente tutte le opzioni.

        ![cattura di schermata del pulsante predefinito di qualità superiore ](images/radio-buttons-image6.png)

        In questo esempio, un elenco a discesa è incentrato sulla selezione corrente e sconsiglia agli utenti di apportare modifiche.

    -   Se nella pagina sono presenti altri elenchi a discesa, prendere in considerazione un elenco a discesa.

-   **Un set di pulsanti di comando, collegamenti ai comandi o un pulsante di suddivisione è la scelta migliore?** Se i pulsanti di opzione vengono usati solo per influire sulla modalità di esecuzione di un comando, è spesso preferibile presentare le varianti del comando. In questo modo gli utenti possono scegliere il comando giusto con una singola interazione.
-   **Sono disponibili opzioni di programma, anziché dati?** I valori delle opzioni non devono essere basati sul contesto o su altri dati. Per i dati, utilizzare un elenco a discesa o un elenco a selezione singola.
-   Se il controllo viene utilizzato in una pagina della procedura guidata o in un pannello di controllo, **è il controllo di una risposta all'istruzione principale e gli utenti possono modificare la scelta in un secondo momento?** In tal caso, prendere in considerazione l'uso dei collegamenti ai comandi anziché dei pulsanti di opzione per rendere più efficiente l'interazione.
-   **I valori non sono numerici?** Per i dati numerici, usare [caselle di testo](ctrl-text-boxes.md), [elenchi a discesa](/windows/desktop/uxguide/ctrl-drop)o dispositivi di [scorrimento](ctrl-sliders.md).

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Elencare le opzioni in un ordine logico,** ad esempio con la maggiore probabilità di essere selezionate come meno, più semplice operazione per la maggior parte dei casi più complessi o meno rischiosi. L'ordinamento alfabetico non è consigliato perché dipende dal linguaggio e pertanto non è localizzabile.
-   **Se nessuna delle opzioni è una scelta valida, aggiungere un'altra opzione per riflettere la scelta,** ad esempio None o non applicabile.
-   **Preferisce allineare verticalmente i pulsanti di opzione anziché orizzontalmente.** L'allineamento orizzontale è più difficile da leggere e localizzare.

    **Corretto:**

    ![screenshot dell'allineamento verticale dei pulsanti di opzione ](images/radio-buttons-image7.png)

    In questo esempio, i pulsanti di opzione sono allineati verticalmente.

    **Non corretto:**

    ![cattura di schermata dell'allineamento del pulsante di opzione orizzontale ](images/radio-buttons-image8.png)

    In questo esempio, l'allineamento orizzontale è più difficile da leggere.

-   **Riprendere in considerazione l'uso di caselle di gruppo per organizzare i gruppi di pulsanti di opzione**. questa operazione spesso comporta un disordine dello schermo superfluo.
-   **Non usare etichette di pulsanti di opzione come etichette della casella di gruppo.**
-   **Non usare la selezione di un pulsante di opzione per:**
    -   Eseguire comandi.
    -   Visualizzare altre finestre, ad esempio una finestra di dialogo per raccogliere più input.
    -   Consente di visualizzare o nascondere in modo dinamico altri controlli correlati al controllo selezionato (le utilità per la lettura dello schermo non possono rilevare tali eventi). Tuttavia, è possibile modificare il testo in modo dinamico in base alla selezione.

### <a name="subordinate-controls"></a>Controlli subordinati

-   Posizionare i controlli subordinati a destra di o sotto (con rientri, scaricare con l'etichetta del pulsante di opzione) il pulsante di opzione e la relativa etichetta. Terminare l'etichetta del pulsante di opzione con i due punti.

    ![screenshot del controllo a destra dell'etichetta ](images/radio-buttons-image9.png)

    In questo esempio il pulsante di opzione e il relativo controllo subordinato condividono l'etichetta del pulsante di opzione e la relativa chiave di accesso. In questo caso, i tasti di direzione spostano lo stato attivo dal pulsante di opzione alla relativa casella di testo subordinata.

-   **Lasciare abilitati gli elenchi a discesa e le caselle di testo modificabili dipendenti se condividono l'etichetta del pulsante di opzione.** Quando gli utenti digitano o incollano qualsiasi elemento nella casella, selezionare l'opzione corrispondente automaticamente. Questa operazione semplifica l'interazione.

    ![screenshot della finestra di dialogo intervallo pagine con casella di testo ](images/radio-buttons-image10.png)

    In questo esempio, l'immissione di un numero di pagina Seleziona automaticamente le pagine.

-   **Evitare l'annidamento di pulsanti di opzione con altri pulsanti di opzione o caselle di controllo.** Se possibile, Mantieni tutte le opzioni allo stesso livello.

    **Corretto:**

    ![screenshot dei pulsanti di opzione allineati a sinistra ](images/radio-buttons-image11.png)

    In questo esempio, le opzioni sono allo stesso livello.

    **Non corretto:**

    ![screenshot dei pulsanti di opzione annidati ](images/radio-buttons-image12.png)

    In questo esempio, l'uso di opzioni annidate aggiunge complessità superflua.

-   Se si annidano pulsanti di opzione con altri pulsanti di opzione o caselle di controllo, **disabilitare questi controlli subordinati fino a quando non si seleziona l'opzione di alto livello.** In questo modo si evita confusione sul significato dei controlli subordinati.

### <a name="default-values"></a>Valori predefiniti

-   Poiché un gruppo di pulsanti di opzione rappresenta un set di scelte che si escludono a vicenda, **è sempre selezionato un pulsante di opzione per impostazione predefinita. Selezionare il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e l'opzione più sicura e privata.** Se la sicurezza e la sicurezza non sono fattori, selezionare l'opzione più probabile o pratica.
-   **Eccezioni:** Non avere una selezione predefinita se:
    -   **Non esiste un'opzione predefinita accettabile per motivi di sicurezza, sicurezza o legali e pertanto l'utente deve effettuare una scelta esplicita.** Se l'utente non effettua una selezione, Visualizza un messaggio di errore per forzarne uno.
    -   **L'interfaccia utente (UI) deve riflettere lo stato corrente e l'opzione non è ancora stata impostata.** Un valore predefinito non implica erroneamente che l'utente non debba effettuare una selezione.
    -   **L'obiettivo è raccogliere dati non distorta.** I valori predefiniti comporterebbero la raccolta dei dati.
    -   **Il gruppo di pulsanti di opzione rappresenta una proprietà in uno stato misto**, che si verifica quando si visualizza una proprietà per più oggetti che non hanno la stessa impostazione. Non visualizzare un messaggio di errore in questo caso poiché ogni oggetto ha uno stato valido.
-   **Imposta la prima opzione come predefinita**, perché gli utenti si aspettano spesso, a meno che tale ordine non sia logico. A tale scopo, potrebbe essere necessario modificare le etichette delle opzioni.

    **Non corretto:**

    ![cattura di schermata dell'ultimo pulsante di opzione come impostazione predefinita ](images/radio-buttons-image13.png)

    In questo esempio, l'opzione predefinita non è la prima opzione.

    **Corretto:**

    ![screenshot del primo pulsante di opzione come predefinito ](images/radio-buttons-image14.png)

    In questo esempio, le etichette delle opzioni vengono riformulate per rendere la prima opzione l'opzione predefinita.

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![screenshot del ridimensionamento e della spaziatura dei pulsanti di opzione ](images/radio-buttons-image15.png)

Dimensionamento e spaziatura consigliati per i pulsanti di opzione.

## <a name="labels"></a>Etichette

### <a name="radio-button-labels"></a>Etichette pulsanti di opzione

-   Etichetta tutti i pulsanti di opzione.

<!-- -->

-   Assegnare una [chiave di accesso](glossary.md) univoca a ogni etichetta. Per le linee guida, vedere [tastiera](inter-keyboard.md).
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Scrivere l'etichetta come frase, non come frase e non usare segni di punteggiatura finale.
    -   **Eccezione:** Se un'etichetta del pulsante di opzione contrassegna anche un controllo subordinato che lo segue, terminare l'etichetta con i due punti.
-   Usare il formulazione parallela e provare a rimanere la stessa lunghezza per tutte le etichette.
-   Concentrare il testo dell'etichetta sulle differenze tra le opzioni. Se tutte le opzioni hanno lo stesso testo introduttivo, spostare il testo nell'etichetta del gruppo.
-   Usare la formulazione positiva. Ad esempio, utilizzare do anziché do not e Print anziché do not Print.
-   Descrivere solo l'opzione con l'etichetta. Mantieni le etichette brevi, quindi è facile farvi riferimento nei messaggi e nella documentazione. Se l'opzione richiede una spiegazione ulteriore, fornire la spiegazione in un controllo [testo statico](glossary.md) usando le frasi complete e la punteggiatura finale.

    ![screenshot dei pulsanti di opzione con testo esplicativo](images/radio-buttons-image16.png)

    In questo esempio, le opzioni vengono descritte utilizzando controlli di testo statici distinti.

    > [!Note]  
    > L'aggiunta di una spiegazione a un solo pulsante di opzione non significa che è necessario fornire spiegazioni per tutti i pulsanti di opzione. Fornire le informazioni rilevanti nell'etichetta, se possibile, e utilizzare le spiegazioni solo quando necessario. Non semplicemente riassegnare l'etichetta per la coerenza.

     

-   **Se un'opzione è fortemente consigliata, aggiungere "(scelta consigliata)" all'etichetta.** Assicurarsi di aggiungere all'etichetta del controllo e non alle note aggiuntive.
-   **Se un'opzione è destinata solo agli utenti avanzati, aggiungere "(Advanced)" all'etichetta.** Assicurarsi di aggiungere all'etichetta del controllo e non alle note aggiuntive.
-   Se è necessario utilizzare etichette a più righe, allineare la parte superiore dell'etichetta al pulsante di opzione.
-   Non usare un controllo subordinato, i valori in esso contenuti o l'etichetta unità per creare una frase o una frase. Una progettazione di questo tipo non è localizzabile perché la struttura della frase varia in base alla lingua.

### <a name="radio-button-group-labels"></a>Etichette del gruppo di pulsanti di opzione

-   Utilizzare l'etichetta del gruppo per spiegare lo scopo del gruppo, non come effettuare la selezione. Si supponga che gli utenti sappiano come usare i pulsanti di opzione. Ad esempio, non pronunciare "selezionare una delle opzioni seguenti".
-   Tutti i gruppi di pulsanti di opzione necessitano di etichette. Scrivere l'etichetta come una parola o una frase, non come una frase, terminando con un segno di due punti usando un testo statico o una casella di gruppo.

    **Eccezione:** Omettere l'etichetta se si tratta semplicemente di una ripubblicazione dell' [istruzione principale](glossary.md)di una finestra di dialogo. In questo caso, l'istruzione principale accetta i due punti (a meno che non si tratti di una domanda) e una chiave di accesso (se presente).

    **Accettabile:**

    ![cattura di schermata dell'etichetta del gruppo di pulsanti di opzione ridondante ](images/radio-buttons-image17.png)

    In questo esempio, l'etichetta del gruppo di pulsanti di opzione è semplicemente una ripubblicazione dell'istruzione principale.

    **Migliore:**

    ![cattura di schermata del pulsante di opzione solo istruzione principale ](images/radio-buttons-image18.png)

    In questo esempio, l'etichetta ridondante viene rimossa, quindi l'istruzione principale accetta i due punti.

-   Non assegnare una chiave di accesso all'etichetta. Questa operazione non è necessaria e rende più difficile l'assegnazione delle altre chiavi di accesso.
    -   **Eccezione:** Se non tutti i controlli possono avere chiavi di accesso univoche, è possibile assegnare una chiave di accesso all'etichetta anziché ai singoli controlli. Per ulteriori informazioni, vedere [tastiera](inter-keyboard.md).

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai pulsanti di opzione:

-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere il carattere di sottolineatura della chiave di accesso o i due punti.
-   In programmazione e altri documenti tecnici, fare riferimento ai pulsanti di opzione come pulsanti di opzione. In tutti gli altri casi utilizzare i pulsanti di opzione, in particolare nella documentazione dell'utente.
-   Per descrivere l'interazione dell'utente, utilizzare fare clic su.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempio: fare clic su **pagina corrente**, quindi fare clic su **OK**.

 

 