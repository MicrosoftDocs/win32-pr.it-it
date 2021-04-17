---
title: Caselle di testo
description: Con una casella di testo, gli utenti possono visualizzare, immettere o modificare un valore di testo o numerico.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2b5257e9772465f26815abb0f6ecbe0ff357ba4b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104530433"
---
# <a name="text-boxes"></a>Caselle di testo

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con una casella di testo, gli utenti possono visualizzare, immettere o modificare un valore di testo o numerico.

![Screenshot di una casella di testo e di un'etichetta tipici ](images/ctrl-text-boxes-image1.png)

Casella di testo tipica.

> [!Note]  
> Le linee guida relative a [layout](vis-layout.md), [tipi di carattere](vis-fonts.md)e [palloni](ctrl-balloons.md) vengono presentate in articoli distinti.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **È utile enumerare tutti i valori validi in modo efficiente?** In tal caso, prendere in considerazione un [elenco a selezione singola](ctrl-list-boxes.md), una [visualizzazione elenco](ctrl-list-views.md), un elenco [a discesa](/windows/desktop/uxguide/ctrl-drop), un elenco a discesa modificabile o un [dispositivo di scorrimento](ctrl-sliders.md) .
-   **I dati validi sono completamente non vincolati? O sono i dati validi vincolati solo in base al formato (lunghezza vincolata o tipi di carattere)?** In tal caso, utilizzare una casella di testo.
-   **Il valore rappresenta un tipo di dati che dispone di un controllo comune specifico?** Gli esempi includono data, ora o indirizzo IPv4 o IPv6. In tal caso, utilizzare il controllo appropriato, ad esempio un controllo data anziché una casella di testo.
-   Se i dati sono numerici:
    -   **Gli utenti percepiscono l'impostazione come una quantità relativa?** Se sì, usa un dispositivo di scorrimento.
    -   **L'utente trarrebbe vantaggio da un riscontro immediato sull'effetto delle modifiche dell'impostazione?** In tal caso, utilizzare un dispositivo di scorrimento, possibilmente insieme a una casella di testo. Ad esempio, gli utenti possono scegliere facilmente un colore usando un dispositivo di scorrimento perché possono visualizzare immediatamente l'effetto delle modifiche ai valori di tonalità, saturazione o luminosità.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Mentre le caselle di testo hanno il vantaggio di essere molto flessibili, hanno lo svantaggio di avere limitazioni minime. Gli unici vincoli in una casella di testo modificabile sono:

-   Facoltativamente, è possibile impostare il numero massimo di caratteri.
-   Facoltativamente, è possibile limitare l'input solo ai caratteri numerici (0 9).
-   Se si usa un [controllo di selezione](ctrl-spin-controls.md), è possibile limitare le opzioni di controllo di selezione ai valori validi.

Oltre alla lunghezza e alla presenza facoltativa di un controllo di selezione, le caselle di testo non hanno indizi visivi che suggeriscono i valori validi o il formato. Ciò significa basarsi sulle etichette per fornire queste informazioni agli utenti. Se gli utenti immettono testo non valido, è necessario gestire l'errore con un messaggio di errore.

Come regola generale, **è consigliabile usare il controllo più vincolato possibile**. Usare controlli non vincolati come le caselle di testo come ultima risorsa. Ciò detto, quando si considerano i vincoli, tenere presente le esigenze degli utenti globali. Ad esempio, un controllo vincolato a Stati Uniti CAP non è globalizzato, ma una casella di testo non vincolata che accetta qualsiasi formato di codice postale è.

## <a name="usage-patterns"></a>Modelli di utilizzo

Una casella di testo è un controllo flessibile con diversi usi possibili.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Input di dati</strong><br/> Casella di testo a riga singola non vincolata utilizzata per inserire o modificare stringhe brevi.<br/></td>
<td><img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br/> Casella di testo A riga singola non vincolata.<br/></td>
</tr>
<tr class="even">
<td><strong>Input di dati formattato</strong><br/> Set di caselle di testo a dimensione fissa breve e a dimensione fissa utilizzate per immettere dati con un formato specifico. <br/></td>
<td><img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br/> Casella di testo utilizzata per l'input di dati formattato.<br/>
<blockquote>
[!Note]<br />
La funzionalità di <a href="glossary.md">uscita automatica</a> sposta automaticamente lo stato attivo di input da una casella di testo a quella successiva. Uno svantaggio di questo approccio è che i dati non possono essere copiati o incollati come singola unità.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Input di dati assistito</strong><br/> Casella di testo a riga singola non vincolata utilizzata per immettere o modificare le stringhe, insieme a un pulsante di comando che consente agli utenti di selezionare valori validi.<br/></td>
<td><img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br/> In questo esempio, il comando Browse consente agli utenti di selezionare valori validi.<br/></td>
</tr>
<tr class="even">
<td><strong>Input testuale</strong><br/> Casella di testo a più righe, non vincolata utilizzata per inserire o modificare stringhe lunghe. <br/></td>
<td><img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br/> Casella di testo A più righe, non vincolata.<br/></td>
</tr>
<tr class="odd">
<td><strong>Input numerico</strong><br/> Casella di testo a riga singola solo numerica utilizzata per inserire o modificare numeri, con un controllo di <a href="ctrl-spin-controls.md">selezione</a> facoltativo per facilitare l'input basato sul mouse. <br/></td>
<td><img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br/> Casella di testo utilizzata per l'input numerico.<br/> La combinazione di una casella di testo e del controllo di selezione associato è detta <a href="ctrl-spin-controls.md">casella di selezione</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>Input di password e PIN</strong><br/> Casella di testo a riga singola non vincolata utilizzata per immettere le password e i pin in modo sicuro.<br/></td>
<td><img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br/> Casella di testo utilizzata per immettere le password.<br/></td>
</tr>
<tr class="odd">
<td><strong>Output dei dati</strong><br/> Una casella di testo a riga singola, di sola lettura, sempre visualizzata senza bordo, utilizzata per visualizzare le stringhe brevi. <br/></td>
<td>A differenza del testo statico, è possibile scorrere i dati visualizzati utilizzando una casella di testo (utile se i dati sono più larghi del controllo), selezionati e copiati.<br/> <img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br/> Casella di testo di sola lettura a riga singola utilizzata per visualizzare i dati.<br/></td>
</tr>
<tr class="even">
<td><strong>Output testuale</strong><br/> Casella di testo di sola lettura a più righe utilizzata per visualizzare stringhe lunghe. <br/></td>
<td><img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br/> Casella di testo di sola lettura utilizzata per visualizzare i dati.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Quando si disabilita una casella di testo, disabilitare anche le etichette associate, le etichette di istruzione, i controlli di selezione e i pulsanti di comando.**
-   **Usare il completamento automatico per consentire agli utenti di immettere dati che potrebbero essere usati ripetutamente**. Gli esempi includono nomi utente, indirizzi e nomi di file. Tuttavia, non usare il completamento automatico per caselle di testo che possono contenere informazioni riservate, ad esempio password, pin, numeri di carta di credito o informazioni mediche.
-   **Non fare in modo che gli utenti scorrano inutilmente.** Se si prevede che i dati siano più grandi della casella di testo ed è possibile fare in modo che la casella di testo sia più grande senza danneggiare il layout, ridimensionare la casella per eliminare la necessità di scorrimento.

    **Non corretto:**

    ![screenshot della casella di testo nome computer ](images/ctrl-text-boxes-image10.png)

    In questo esempio la casella di testo deve essere resa più lunga per gestire i dati.

-   Barre di scorrimento:
    -   **Non inserire barre di scorrimento orizzontali nelle caselle di testo a più righe.** Usare invece lo scorrimento verticale e il ritorno a capo riga.
    -   **Non inserire barre di scorrimento sulle caselle di testo a riga singola.**
-   **Per l'input numerico, è possibile usare un controllo di selezione.** Per l'input testuale, usare invece un elenco a discesa o un elenco a discesa modificabile.
-   **Non usare la funzionalità di uscita automatica, ad eccezione dell'input di dati formattato.** Lo spostamento automatico dello stato attivo può sorprendere gli utenti.

### <a name="editable-text-boxes"></a>Caselle di testo modificabili

-   **Quando possibile, limitare la lunghezza del testo di input.** Se, ad esempio, l'input valido è un numero compreso tra 0 e 999, utilizzare una casella di testo numerica limitata a tre caratteri. Tutte le parti di caselle di testo che utilizzano input di dati formattati devono avere una lunghezza fissa breve.
-   **Essere flessibili con i formati di dati.** Se è probabile che gli utenti immettano testo usando un'ampia gamma di formati, provare a gestire tutti i più comuni. È ad esempio possibile immettere molti nomi, numeri e identificatori con spazi e punteggiatura facoltativi e le maiuscole spesso non sono importanti.
-   Se non è possibile gestire i formati probabili, richiedere un formato specifico usando input di dati formattati o indicare i formati validi nell'etichetta.

    **Accettabile:**

    ![Screenshot di una casella di testo per l'input numerico ](images/ctrl-text-boxes-image11.png)

    In questo esempio, una casella di testo richiede l'input in un formato specifico.

    **Migliore:**

    ![screenshot della casella di testo di input dei dati formattati ](images/ctrl-text-boxes-image12.png)

    In questo esempio, il modello di input dei dati formattato viene usato per richiedere un formato specifico.

    **Consigliate**

    ![Screenshot di una casella di testo non vincolata ](images/ctrl-text-boxes-image13.png)

    In questo esempio, una casella di testo gestisce tutti i formati probabili.

-   Considerare la flessibilità del formato quando si sceglie la lunghezza massima di input. Un numero di carta di credito valido, ad esempio, può utilizzare fino a 19 caratteri, quindi limitare la lunghezza a un valore più breve potrebbe rendere difficile l'immissione di numeri utilizzando i formati più lunghi.
-   **Non usare il modello di input dei dati formattato se gli utenti hanno più probabilità di incollare dati lunghi e complessi.** Riservare invece il modello di input dei dati formattato per le situazioni in cui è più probabile che gli utenti digitano i dati.

    ![Screenshot di una casella di testo con etichetta: indirizzo IPv6 ](images/ctrl-text-boxes-image14.png)

    In questo esempio, il modello di input dei dati formattato non viene usato, in modo che gli utenti possano incollare gli indirizzi IPv6.

-   **Se è più probabile che gli utenti immettano nuovamente l'intero valore, selezionare tutto il testo sullo stato attivo per l'input.** Se è più probabile che gli utenti modifichino, posizionare il punto di inserimento alla fine del testo.

    ![screenshot della casella di testo della password ](images/ctrl-text-boxes-image15.png)

    In questo esempio, è più probabile che gli utenti sostituiscano di Edit, quindi l'intero valore viene selezionato sullo stato attivo per l'input.

    ![Screenshot di una casella di testo per l'immissione di parole chiave ](images/ctrl-text-boxes-image16.png)

    In questo esempio, è più probabile che gli utenti aggiungano parole chiave che sostituiscono il testo, quindi il punto di inserimento si trova alla fine del testo.

-   **Usare sempre una casella di testo a più righe se i caratteri di nuova riga sono input validi.**
-   **Quando la casella di testo è per un file o un percorso, fornire sempre un pulsante Sfoglia.**

### <a name="numeric-text-boxes"></a>Caselle di testo numerici

-   **Scegliere l'unità più pratica ed etichettare le unità.** Si supponga, ad esempio, di usare millilitri anziché litri (o viceversa), percentuali anziché valori diretti (o viceversa) e così via.

    **Corretto:**

    ![screenshot della casella di testo con litri come unità ](images/ctrl-text-boxes-image17.png)

    In questo esempio, l'unità viene etichettata, ma è necessario che gli utenti immettano numeri decimali.

    **Migliore:**

    ![screenshot della casella di testo con millilitri come unità ](images/ctrl-text-boxes-image18.png)

    In questo esempio, la casella di testo usa un'unità più pratica.

-   **Utilizzare un controllo di selezione ogni volta che è utile.** Tuttavia, a volte i controlli di selezione non sono pratici, ad esempio quando gli utenti devono immettere molti numeri elevati. Usare i controlli di selezione nei casi seguenti:
    -   È probabile che l'input sia un numero ridotto, in genere inferiore a 100.
    -   È probabile che gli utenti apporteranno una piccola modifica a un numero esistente.
    -   È più probabile che gli utenti utilizzino il mouse anziché la tastiera.
-   **Allinea a destra il testo numerico ogni volta che:**

    -   È presente più di una casella di testo numerica.
    -   Le caselle di testo sono allineate verticalmente.
    -   È probabile che gli utenti aggiungano o confrontino i valori.

    **Corretto:**

    ![screenshot delle caselle di testo spese (Hotel e così via) ](images/ctrl-text-boxes-image19.png)

    In questo esempio il testo numerico è allineato a destra per facilitare il confronto dei valori.

    **Non corretto:**

    ![screenshot delle caselle di testo per i valori RGB ](images/ctrl-text-boxes-image20.png)

    In questo esempio il testo numerico è allineato in modo non corretto.

-   **Allinea sempre a destra i valori monetari.**
-   **Non assegnare significati speciali a valori numerici specifici**, anche se questi significati speciali vengono usati internamente dall'applicazione. Usare invece caselle di controllo o pulsanti di opzione per una selezione esplicita dell'utente.

    **Non corretto:**

    ![screenshot dell'etichetta: usare-1 per disabilitare la memorizzazione nella cache ](images/ctrl-text-boxes-image21.png)

    In questo esempio, il valore-1 ha un significato speciale.

    **Corretto:**

    ![screenshot dell'etichetta della casella di controllo: Caching ](images/ctrl-text-boxes-image22.png)

    In questo esempio, una casella di controllo rende esplicita l'opzione.

### <a name="password-and-pin-input"></a>Input di password e PIN

-   **Usare sempre il controllo comune password anziché crearne di personalizzati.** Le password e i pin richiedono un trattamento speciale per essere gestiti in modo sicuro.

Per altre linee guida ed esempi, vedere [Balloons](ctrl-balloons.md).

### <a name="textual-output"></a>Output testuale

-   **Si consiglia di usare il colore di sistema in background bianco per il testo di sola lettura su larga linea e su più righe.** Uno sfondo bianco rende il testo più semplice da leggere. Molti testi su uno sfondo grigio sconsigliano la lettura.

Per ulteriori informazioni sui colori di sfondo, vedere [tipi di carattere](vis-fonts.md).

### <a name="data-output"></a>Output dei dati

-   **Non usare un bordo per le caselle di testo a riga singola e di sola lettura.** Il bordo è un indizio visivo che il testo è modificabile.
-   **Non disabilitare le caselle di testo di sola lettura a riga singola.** In questo modo si impedisce agli utenti di selezionare e copiare il testo negli Appunti. Impedisce inoltre agli utenti di scorrere i dati se superano le dimensioni dei relativi limiti.
-   **Non impostare una tabulazione su una sola riga di testo di sola lettura, a meno che non sia probabile che l'utente debba scorrere o copiare il testo.**

## <a name="input-validation-and-error-handling"></a>Convalida degli input e gestione degli errori

Poiché le caselle di testo non sono in genere vincolate ad accettare solo un input valido, potrebbe essere necessario convalidare l'input e gestire eventuali problemi. Convalidare i vari tipi di problemi di input come segue:

-   Se l'utente immette un carattere non valido, ignorare il carattere e visualizzare un fumetto di un [problema di input](ctrl-balloons.md) che illustra i caratteri validi.

    ![screenshot della casella di testo del codice Product Key](images/ctrl-text-boxes-image23.png)

    In questo esempio un fumetto segnala un carattere di input non corretto.

-   Se i dati di input hanno un valore o un formato non valido, visualizzare un fumetto di problema di input quando la casella di testo perde lo stato attivo per l'input.
-   Se i dati di input non sono coerenti con altri controlli della finestra, fornire un messaggio di errore quando l'intero input è completo, ad esempio quando gli utenti fanno clic su OK per una finestra di dialogo modale.

**Non cancellare i dati di input non validi a meno che gli utenti non siano in grado di correggere facilmente gli errori.** Questa operazione consente agli utenti di correggere gli errori senza ricominciare. Ad esempio, è consigliabile cancellare le password e i pin non corretti perché gli utenti non possono correggerli facilmente.

Per altre linee guida ed esempi, vedere [messaggi di errore](mess-error.md) e [palloncini](ctrl-balloons.md).

## <a name="prompts"></a>Prompt

Un messaggio di richiesta è un'etichetta o un'istruzione breve posizionata all'interno di una casella di testo come valore predefinito. A differenza del testo statico, i messaggi di richiesta scompaiono dallo schermo una volta che gli utenti digitano qualcosa nella casella di testo o ottengono lo stato attivo per l'input.

![screenshot della casella di testo della richiesta con etichetta: ricerca ](images/ctrl-text-boxes-image24.png)

Un prompt tipico.

Usare un prompt nei casi seguenti:

-   Lo spazio dello schermo è a un livello superiore che l'uso di un'etichetta o di un'istruzione è indesiderato, ad esempio su una barra degli strumenti.
-   Il prompt è principalmente per identificare lo scopo della casella di testo in modo compatto. Non devono essere informazioni cruciali che l'utente deve visualizzare durante l'uso della casella di testo.

Non usare i prompt solo per indicare agli utenti di digitare qualcosa o fare clic sui pulsanti. Ad esempio, non scrivere testo della richiesta di conferma immettere un nome file e quindi fare clic su Invia.

Quando si usano i prompt:

-   Creare il testo della richiesta in grigio corsivo e il testo di input effettivo in nero normale. Il testo della richiesta non deve essere confuso con il testo reale.
-   Conserva il testo della richiesta conciso. È possibile utilizzare frammenti anziché frasi complete.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Non usare la punteggiatura finale o i puntini di sospensione.
-   Il testo della richiesta non deve essere modificabile e dovrebbe scomparire quando gli utenti fanno clic nella casella di testo o nella scheda.
    -   **Eccezione:** Se la casella di testo ha lo stato attivo per l'input predefinito, il prompt viene visualizzato e scompare una volta che l'utente inizia a digitare.
-   Il testo della richiesta viene ripristinato se la casella di testo è ancora vuota quando perde lo stato attivo per l'input.

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![Figura di caselle di testo a riga singola e a due righe ](images/ctrl-text-boxes-image25.png)

Ridimensionamento e spaziatura consigliati per le caselle di testo.

La larghezza di una casella di testo è un indizio visivo delle dimensioni di input previste. Quando si ridimensionano le caselle di testo:

-   **Scegliere una larghezza appropriata per i dati più lunghi validi.** Nella maggior parte dei casi, gli utenti non dovrebbero dover scorrere la stringa più probabile che entreranno o visualizzano.
-   **Includere un ulteriore 30%** (fino al 200% per un testo più breve) per qualsiasi testo (ma non per i numeri) che verrà localizzato.
-   **Se l'input previsto non ha dimensioni particolari, scegliere una larghezza coerente con le altre caselle di testo o i controlli della finestra.**
-   **Ridimensiona le caselle di testo su più righe per visualizzare un numero integrale di righe di testo.**

## <a name="labels"></a>Etichette

### <a name="text-box-labels"></a>Etichette casella di testo

-   Tutte le caselle di testo necessitano di etichette. Scrivere l'etichetta come una parola o una frase, non come una frase, terminando con i due punti e usando il [testo statico](glossary.md).

    **Eccezioni**

    -   Caselle di testo con prompt in cui lo spazio è disponibile a un livello Premium.
    -   Per l'assegnazione di etichette, un gruppo di caselle di testo utilizzate per l' **input di dati formattati** deve essere considerato come una singola casella di testo.
    -   Se una casella di testo è subordinata a un pulsante di opzione o a una casella di controllo e viene introdotta dall'etichetta che termina con i due punti, non inserire un'etichetta aggiuntiva nella casella di testo.
    -   **Omettere le etichette dei controlli che riportano l'istruzione principale.** In questo caso, l'istruzione principale accetta i due punti, a meno che non si tratti di una domanda, e la chiave di accesso.

        **Accettabile:**

        ![screenshot della casella di testo con etichetta ripetitiva](images/ctrl-text-boxes-image26.png)

        In questo esempio, l'etichetta della casella di testo è semplicemente una ripubblicazione dell'istruzione principale.

        **Migliore:**

        ![screenshot della casella di testo con solo istruzione principale ](images/ctrl-text-boxes-image27.png)

        In questo esempio, l'etichetta ridondante viene rimossa, quindi l'istruzione principale accetta i due punti e la chiave di accesso.

-   Assegnare una chiave di accesso univoca. Per le linee guida per l'assegnazione delle chiavi di accesso, vedere [tastiera](inter-keyboard.md).
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Posizionare l'etichetta a sinistra o sopra la casella di testo e allineare l'etichetta al bordo sinistro della casella di testo. Se l'etichetta è a sinistra, allineare verticalmente il testo dell'etichetta con il testo della casella di testo.

    **Corretto:**

    ![screenshot dell'etichetta allineata a sinistra sopra la casella di testo ](images/ctrl-text-boxes-image28.png)

    ![screenshot dell'etichetta allineata al testo a sinistra della casella di testo ](images/ctrl-text-boxes-image29.png)

    In questi esempi, l'etichetta nella parte superiore si allinea al bordo sinistro della casella di testo e l'etichetta a sinistra viene allineata al testo nella casella di testo.

    **Non corretto:**

    ![screenshot dell'etichetta allineata al testo sopra la casella di testo ](images/ctrl-text-boxes-image30.png)

    ![screenshot dell'etichetta allineata in alto a sinistra della casella di testo ](images/ctrl-text-boxes-image31.png)

    In questi esempi non corretti, l'etichetta nella parte superiore viene allineata al testo nella casella di testo e l'etichetta a sinistra viene allineata alla parte superiore della casella di testo.

-   È possibile specificare unità (ad esempio, secondi o connessioni) tra parentesi dopo l'etichetta.
-   Se una casella di testo accetta un numero massimo di caratteri arbitrariamente ridotto, è possibile indicare l'input massimo nell'etichetta. La larghezza della casella di testo suggerisce anche le dimensioni massime.

    ![screenshot della casella di testo password ](images/ctrl-text-boxes-image32.png)

    In questo esempio, l'etichetta indica il numero massimo di caratteri.

-   Non fare in modo che il contenuto della casella di testo (o etichetta unità) faccia parte di una frase, perché non è localizzabile.
-   Se è possibile usare la casella di testo per immettere diversi elementi, deselezionare la modalità di separazione degli elementi nell'etichetta.

    ![screenshot dei nomi separati dall'etichetta con punto e virgola ](images/ctrl-text-boxes-image33.png)

    In questo esempio, il separatore di elementi viene specificato nell'etichetta.

-   Per linee guida su come indicare l'input richiesto, vedere input obbligatorio nelle [finestre di dialogo](win-dialog-box.md).

### <a name="instruction-labels"></a>Etichette di istruzioni

-   Se è necessario aggiungere testo di istruzioni su una casella di testo, aggiungerla sopra l'etichetta. Utilizzare frasi complete con la punteggiatura finale.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Informazioni aggiuntive utili ma non necessarie devono essere mantenute brevi. Inserire queste informazioni tra parentesi tra l'etichetta e i due punti o senza parentesi sotto la casella di testo.

    ![screenshot delle informazioni aggiunte sotto la casella di testo ](images/ctrl-text-boxes-image34.png)

    In questo esempio, le informazioni aggiuntive vengono posizionate sotto la casella di testo.

### <a name="prompt-labels"></a>Etichette dei messaggi di richiesta

-   Conserva il testo della richiesta conciso. È possibile utilizzare frammenti anziché frasi complete.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Non usare la punteggiatura finale o i puntini di sospensione.
-   Se il prompt indica agli utenti di immettere informazioni che verranno eseguite da un pulsante accanto alla casella di testo, è sufficiente posizionare il pulsante accanto alla casella di testo. Non usare il prompt per indirizzare gli utenti a fare clic sul pulsante (ad esempio, non scrivere il testo della richiesta, trascinare un file e quindi fare clic su Invia).

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle caselle di testo:

-   Usare il tipo per fare riferimento a interazioni utente che richiedono la digitazione o incolla; in caso contrario, utilizzare invio se gli utenti possono inserire informazioni nella casella di testo utilizzando altri metodi, ad esempio selezionando il valore da un elenco o utilizzando un pulsante Sfoglia.
-   Usare SELECT per fare riferimento a una voce in una casella di testo di sola lettura.
-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, e includere la parola box. Non includere il carattere di sottolineatura della chiave di accesso o i due punti. Non fare riferimento a una casella di testo come una casella di testo o un campo.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

    Esempio: digitare la password nella casella **password** e quindi fare clic su **OK**.

-   Se la casella di testo richiede un formato specifico, documentare solo il formato accettabile usato più di frequente. Consentire agli utenti di individuare altri formati in modo autonomo. Si desidera essere flessibili con i formati di dati, ma questa operazione non dovrebbe produrre una documentazione complessa.

    **Corretto:**

    Immettere il numero di serie della parte usando il formato 1234-56-7890.

    **Non corretto:**

    Immettere il numero di serie della parte usando uno dei formati seguenti:

    1234567890

    1234-56-7890

    1234 56 7890

