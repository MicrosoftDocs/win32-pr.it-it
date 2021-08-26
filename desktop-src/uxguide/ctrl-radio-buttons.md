---
title: Pulsanti
description: Con un pulsante di opzione, gli utenti possono scegliere tra un set di opzioni correlate che si escludono a vicenda.
ms.assetid: f9af0a8a-d4a1-464c-a967-bab88ae0726b
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: cbe870e1c1900de29dda515fd2142b951886929af46e69b4fea3fc6644e6f8fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934520"
---
# <a name="radio-buttons"></a>Pulsanti

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con un pulsante di opzione, gli utenti possono scegliere tra un set di opzioni correlate che si escludono a vicenda. Gli utenti possono scegliere una sola opzione. I pulsanti di opzione vengono chiamati perché funzionano come i set di impostazioni del canale sulle radio.

![Screenshot di tre pulsanti di opzione ](images/radio-buttons-image1.png)

Gruppo tipico di pulsanti di opzione.

Un gruppo di pulsanti di opzione si comporta come un singolo controllo. Solo la scelta selezionata è accessibile tramite tab, ma gli utenti possono scorrere il gruppo usando i tasti di direzione.

> [!Note]  
> Le linee guida relative [al layout](vis-layout.md) e alla [navigazione tramite](inter-keyboard.md) tastiera sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Il controllo viene usato per scegliere un'opzione da un set di scelte che si escludono a vicenda?** Se non è così, usa un altro controllo. Per scegliere più opzioni, usare [](ctrl-list-boxes.md) [invece le caselle](ctrl-check-boxes.md)di controllo , un elenco a selezione multipla o un elenco di caselle di controllo.
-   **Il numero di opzioni è compreso tra due e sette?** Poiché lo spazio dello schermo usato è proporzionale al numero di opzioni, mantenere il numero di opzioni in un gruppo compreso tra due e sette. Per otto o più opzioni, usare un elenco a [discesa](/windows/desktop/uxguide/ctrl-drop) o [un elenco a selezione singola.](ctrl-list-boxes.md)
-   **Una casella di controllo è una scelta migliore?** Se sono disponibili solo due opzioni, è possibile usare una singola [casella di controllo.](ctrl-check-boxes.md) Tuttavia, le caselle di controllo sono adatte solo per attivare o disattivare una singola opzione, mentre i pulsanti di opzione possono essere usati per alternative completamente diverse. Se entrambe le soluzioni sono possibili:
    -   Usare i pulsanti di opzione se il significato della casella di controllo deselezionata non è del tutto ovvio.

        **Non corretto:**

        ![Screenshot della casella di controllo orizzontale ](images/radio-buttons-image2.png)

        **Corretto:**

        ![Screenshot dei pulsanti di opzione orizzontale/verticale ](images/radio-buttons-image3.png)

        Nell'esempio corretto, le scelte non sono opposte, quindi i pulsanti di opzione sono la scelta migliore.

    -   Usare i pulsanti di opzione nelle pagine della procedura guidata per cancellare le alternative, anche se una casella di controllo è altrimenti accettabile.
    -   Usare i pulsanti di opzione se lo spazio dello schermo è sufficiente e le opzioni sono sufficientemente importanti da essere un buon uso di tale spazio. In caso contrario, usare una casella di controllo o un elenco a discesa.

        **Non corretto:**

        ![Screenshot di show/don't show radio buttons (Mostra/Non visualizzare pulsanti di opzione) ](images/radio-buttons-image4.png)

        In questo esempio le opzioni non sono sufficientemente importanti da usare i pulsanti di opzione.

        **Corretto:**

        ![Screenshot della casella di controllo Non visualizzare questo messaggio ](images/radio-buttons-image5.png)

        In questo esempio, una casella di controllo è un uso efficiente dello spazio sullo schermo per questa opzione periferica.

    -   Usare una casella di controllo se nella pagina sono presenti altre caselle di controllo.

-   **Un elenco a discesa è una scelta migliore?** Se l'opzione predefinita è consigliata per la maggior parte degli utenti nella maggior parte dei casi, i pulsanti di opzione potrebbero attirare più attenzione rispetto alle opzioni necessarie.
    -   È consigliabile usare un elenco a discesa se non si vuole attirare l'attenzione delle opzioni o non si vuole invitare gli utenti a apportare modifiche. Un elenco a discesa si concentra sulla selezione corrente, mentre i pulsanti di opzione evidenziano tutte le opzioni in modo uniforme.

        ![Screenshot con la massima qualità come pulsante predefinito ](images/radio-buttons-image6.png)

        In questo esempio, un elenco a discesa si concentra sulla selezione corrente e sconsiglia agli utenti di apportare modifiche.

    -   Si consideri un elenco a discesa se nella pagina sono presenti altri elenchi a discesa.

-   **Un set di pulsanti di comando, collegamenti di comando o un pulsante di divisione è una scelta migliore?** Se i pulsanti di opzione vengono usati solo per influire sulla modalità di esecuzione di un comando, è spesso meglio presentare le variazioni del comando. In questo modo, gli utenti possono scegliere il comando giusto con una singola interazione.
-   **Le opzioni presentano opzioni di programma anziché dati?** I valori delle opzioni non devono essere basati sul contesto o su altri dati. Per i dati, usare un elenco a discesa o un elenco a selezione singola.
-   Se il controllo viene usato in una pagina della procedura guidata o in un pannello di controllo, il controllo è una risposta all'istruzione principale e gli utenti possono modificare **la scelta in un secondo momento?** In tal caso, è consigliabile usare i collegamenti di comando anziché i pulsanti di opzione per rendere più efficiente l'interazione.
-   **I valori sono non numerici?** Per i dati numerici, usare [caselle](ctrl-text-boxes.md)di testo, [elenchi a discesa](/windows/desktop/uxguide/ctrl-drop)o dispositivi di [scorrimento](ctrl-sliders.md).

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Elencare le opzioni in** un ordine logico, ad esempio con maggiore probabilità di essere selezionate al minimo, operazione più semplice alla più complessa o meno rischiosa per la maggior parte. L'ordinamento alfabetico non è consigliato perché dipende dalla lingua e pertanto non è localizzabile.
-   **Se nessuna delle opzioni è una scelta valida,** aggiungere un'altra opzione per riflettere questa scelta, ad esempio Nessuna o Non applicabile.
-   **Preferisce allineare i pulsanti di opzione verticalmente anziché orizzontalmente.** L'allineamento orizzontale è più difficile da leggere e localizzare.

    **Corretto:**

    ![Screenshot dell'allineamento verticale dei pulsanti di opzione ](images/radio-buttons-image7.png)

    In questo esempio i pulsanti di opzione sono allineati verticalmente.

    **Non corretto:**

    ![Screenshot dell'allineamento orizzontale dei pulsanti di opzione ](images/radio-buttons-image8.png)

    In questo esempio l'allineamento orizzontale è più difficile da leggere.

-   **Riconsiderare l'uso delle caselle di** gruppo per organizzare gruppi di pulsanti di opzione. Ciò spesso comporta un disordine dello schermo non necessario.
-   **Non usare le etichette dei pulsanti di opzione come etichette della casella di gruppo.**
-   **Non usare la selezione di un pulsante di opzione per:**
    -   Eseguire comandi.
    -   Visualizzare altre finestre, ad esempio una finestra di dialogo per raccogliere più input.
    -   Mostra o nasconde dinamicamente altri controlli correlati al controllo selezionato (le utilità per la lettura dello schermo non possono rilevare tali eventi). È tuttavia possibile modificare il testo in modo dinamico in base alla selezione.

### <a name="subordinate-controls"></a>Controlli subordinati

-   Posizionare i controlli subordinati a destra o sotto (rientrati, scaricati con l'etichetta del pulsante di opzione) il pulsante di opzione e la relativa etichetta. Terminare l'etichetta del pulsante di opzione con due punti.

    ![Screenshot del controllo a destra dell'etichetta ](images/radio-buttons-image9.png)

    In questo esempio il pulsante di opzione e il relativo controllo subordinato condividono l'etichetta del pulsante di opzione e il relativo tasto di scelta. In questo caso, i tasti di direzione spostano lo stato attivo dal pulsante di opzione alla relativa casella di testo subordinata.

-   **Lasciare abilitate le caselle di testo modificabili dipendenti e gli elenchi a discesa se condividono l'etichetta del pulsante di opzione.** Quando gli utenti digitano o incollano qualsiasi elemento nella casella, selezionare automaticamente l'opzione corrispondente. Questa operazione semplifica l'interazione.

    ![Screenshot della finestra di dialogo Intervallo di pagine con casella di testo ](images/radio-buttons-image10.png)

    In questo esempio l'immissione di un numero di pagina seleziona automaticamente Pagine.

-   **Evitare di annidare i pulsanti di opzione con altri pulsanti di opzione o caselle di controllo.** Se possibile, mantenere tutte le opzioni allo stesso livello.

    **Corretto:**

    ![Screenshot dei pulsanti di opzione allineati a sinistra ](images/radio-buttons-image11.png)

    In questo esempio le opzioni sono allo stesso livello.

    **Non corretto:**

    ![Screenshot dei pulsanti di opzione annidati ](images/radio-buttons-image12.png)

    In questo esempio, l'uso di opzioni annidate aggiunge complessità non necessaria.

-   Se si annidare i pulsanti di opzione con altri pulsanti di opzione o caselle di controllo, disabilitare questi controlli subordinati fino a quando non viene selezionata **l'opzione di alto livello.** In questo modo si evita confusione sul significato dei controlli subordinati.

### <a name="default-values"></a>Valori predefiniti

-   Poiché un gruppo di pulsanti di opzione rappresenta un set di scelte che si escludono a vicenda, per impostazione predefinita è sempre selezionato **un pulsante di opzione. Selezionare l'opzione più sicura (per evitare la perdita di dati o** l'accesso al sistema) e l'opzione più sicura e privata. Se sicurezza e sicurezza non sono fattori, selezionare l'opzione più probabile o comoda.
-   **Eccezioni:** Non avere una selezione predefinita se:
    -   **Non esiste un'opzione predefinita accettabile per motivi di sicurezza, di sicurezza o legali e pertanto l'utente deve effettuare una scelta esplicita.** Se l'utente non effettua una selezione, visualizzare un messaggio di errore per forzarne una.
    -   **L'interfaccia utente deve riflettere lo stato corrente e l'opzione non è stata ancora impostata.** Un valore predefinito implica erroneamente che l'utente non deve effettuare una selezione.
    -   **L'obiettivo è raccogliere dati non imparziali.** I valori predefiniti distorsionerebbe la raccolta dei dati.
    -   **Il gruppo di pulsanti di opzione** rappresenta una proprietà in uno stato misto, che si verifica quando si visualizza una proprietà per più oggetti che non hanno la stessa impostazione. In questo caso, non visualizzare un messaggio di errore perché ogni oggetto ha uno stato valido.
-   **Impostare la prima opzione come opzione predefinita,** perché gli utenti lo prevedono spesso, a meno che l'ordine non sia logico. A tale scopo, potrebbe essere necessario modificare le etichette delle opzioni.

    **Non corretto:**

    ![Screenshot dell'ultimo pulsante di opzione come opzione predefinita ](images/radio-buttons-image13.png)

    In questo esempio l'opzione predefinita non è la prima opzione.

    **Corretto:**

    ![Screenshot del primo pulsante di opzione come predefinito ](images/radio-buttons-image14.png)

    In questo esempio, le etichette di opzione vengono riformulate per rendere la prima opzione l'opzione predefinita.

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

![Screenshot del ridimensionamento e della spaziatura dei pulsanti di opzione ](images/radio-buttons-image15.png)

Dimensioni e spaziatura consigliate per i pulsanti di opzione.

## <a name="labels"></a>Etichette

### <a name="radio-button-labels"></a>Etichette dei pulsanti di opzione

-   Etichettare ogni pulsante di opzione.

<!-- -->

-   Assegnare una chiave [di accesso univoca](glossary.md) a ogni etichetta. Per le linee guida, vedere [Tastiera.](inter-keyboard.md)
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Scrivere l'etichetta come frase, non come frase, e non usare la punteggiatura finale.
    -   **Eccezione:** Se un'etichetta di pulsante di opzione etichetta anche un controllo subordinato che lo segue, terminare l'etichetta con due punti.
-   Usare la formulazione parallela e provare a mantenere la lunghezza circa uguale per tutte le etichette.
-   Concentrare il testo dell'etichetta sulle differenze tra le opzioni. Se tutte le opzioni hanno lo stesso testo introduttivo, spostare il testo nell'etichetta del gruppo.
-   Usare la formulazione positiva. Ad esempio, usare do invece di do e print anziché do not print.
-   Descrivere solo l'opzione con l'etichetta. Tenere brevi le etichette in modo che sia facile fare riferimento a esse nei messaggi e nella documentazione. Se l'opzione richiede un'ulteriore spiegazione, fornire la spiegazione in un controllo di testo [statico](glossary.md) usando frasi complete e terminando la punteggiatura.

    ![Screenshot dei pulsanti di opzione con testo esplicativo](images/radio-buttons-image16.png)

    In questo esempio le opzioni vengono spiegate usando controlli di testo statico separati.

    > [!Note]  
    > L'aggiunta di una spiegazione a un pulsante di opzione non significa che è necessario fornire spiegazioni per tutti i pulsanti di opzione. Se possibile, fornire le informazioni rilevanti nell'etichetta e usare le spiegazioni solo quando necessario. Non limitarsi a rievalutare l'etichetta per garantire la coerenza.

     

-   **Se un'opzione è fortemente consigliata, aggiungere "(consigliato)" all'etichetta.** Assicurarsi di aggiungere all'etichetta del controllo, non le note supplementari.
-   **Se un'opzione è destinata solo agli utenti avanzati, aggiungere "(advanced)" all'etichetta.** Assicurarsi di aggiungere all'etichetta del controllo, non le note supplementari.
-   Se è necessario usare etichette su più righe, allineare la parte superiore dell'etichetta al pulsante di opzione.
-   Non usare un controllo subordinato, i valori in esso contenuti o l'etichetta di unità per creare una frase o una frase. Tale progettazione non è localizzabile perché la struttura delle frasi varia in base alla lingua.

### <a name="radio-button-group-labels"></a>Etichette dei gruppi di pulsanti di opzione

-   Usare l'etichetta del gruppo per spiegare lo scopo del gruppo, non come effettuare la selezione. Si supponga che gli utenti sappiano come usare i pulsanti di opzione. Ad esempio, non pronunciare "Selezionare una delle opzioni seguenti".
-   Tutti i gruppi di pulsanti di opzione necessitano di etichette. Scrivere l'etichetta come parola o frase, non come frase, terminando con due punti usando testo statico o una casella di gruppo.

    **Eccezione:** Omettere l'etichetta se si tratta semplicemente di una riemissione dell'istruzione principale di una finestra [di dialogo.](glossary.md) In questo caso, l'istruzione principale accetta i due punti (a meno che non si tratta di una domanda) e la chiave di accesso (se presente).

    **Accettabile:**

    ![Screenshot dell'etichetta del gruppo di pulsanti di opzione ridondante ](images/radio-buttons-image17.png)

    In questo esempio, l'etichetta del gruppo di pulsanti di opzione è solo una ridescrizione dell'istruzione principale.

    **Migliore:**

    ![Screenshot solo dell'istruzione principale del pulsante di opzione ](images/radio-buttons-image18.png)

    In questo esempio l'etichetta ridondante viene rimossa, quindi l'istruzione principale accetta i due punti.

-   Non assegnare una chiave di accesso all'etichetta. Questa operazione non è necessaria e rende più difficile l'assegnazione delle altre chiavi di accesso.
    -   **Eccezione:** Se non tutti i controlli possono avere chiavi di accesso univoche, è possibile assegnare una chiave di accesso all'etichetta anziché ai singoli controlli. Per altre informazioni, vedere [Tastiera.](inter-keyboard.md)

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai pulsanti di opzione:

-   Usare il testo esatto dell'etichetta, inclusa la combinazione di maiuscole e minuscole, ma non includere il carattere di sottolineatura del tasto di scelta o i due punti.
-   Nella programmazione e in altri documenti tecnici, fare riferimento ai pulsanti di opzione come pulsanti di opzione. Ovunque usino i pulsanti di opzione, in particolare nella documentazione dell'utente.
-   Per descrivere l'interazione dell'utente, usare click.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempio: fare clic **su Pagina corrente** e quindi su **OK.**

 

 