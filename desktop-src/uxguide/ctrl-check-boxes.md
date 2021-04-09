---
title: Caselle di controllo
description: Con una casella di controllo, gli utenti decidono tra due scelte chiaramente opposte.
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7a175893b2dfab2999ce37e3f00395d881f03973
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103968822"
---
# <a name="check-boxes"></a>Caselle di controllo

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con una casella di controllo, gli utenti decidono tra due scelte chiaramente opposte. L'etichetta della casella di controllo indica lo stato selezionato, mentre il significato dello stato cancellato deve essere l'opposto non ambiguo dello stato selezionato. Di conseguenza, le **caselle di controllo devono essere usate solo per attivare o disattivare un'opzione o per selezionare o deselezionare un elemento.**

![Screenshot di una delle quattro caselle di controllo selezionate ](images/ctrl-check-boxes-image1.png)

Gruppo tipico di caselle di controllo.

> [!Note]  
> Le linee guida correlate al [layout](vis-layout.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Casella di controllo utilizzata per attivare o disattivare un'opzione oppure per selezionare o deselezionare un elemento.** Se non è così, usa un altro controllo.
-   **Gli stati selezionati e deselezionati sono cancellati e non ambigui?** In caso contrario, utilizzare [pulsanti di opzione](ctrl-radio-buttons.md) o un elenco a [discesa](/windows/desktop/uxguide/ctrl-drop) in modo che sia possibile etichettare gli stati in modo indipendente.
-   **Quando viene usato in un gruppo, il gruppo comprende scelte indipendenti, da cui gli utenti possono scegliere zero o più?** In caso contrario, prendere in considerazione i controlli per le scelte dipendenti, ad esempio pulsanti di opzione e [visualizzazioni ad albero](ctrl-tree-views.md)delle caselle di controllo.
-   **Se usato in un gruppo, il gruppo comprende scelte dipendenti, da cui gli utenti devono scegliere una o più opzioni?** In tal caso, utilizzare un gruppo di caselle di controllo e gestire l'errore quando nessuna delle opzioni è selezionata.
-   **Il numero di opzioni in un gruppo è inferiore a 10?** Poiché lo spazio dello schermo utilizzato è proporzionale al numero di opzioni, è necessario limitare il numero di caselle di controllo a un massimo di 10. Per più di 10 opzioni, usare un [elenco](ctrl-list-boxes.md)di caselle di controllo.
-   **Un pulsante di opzione potrebbe essere la scelta migliore?** Se le caselle di controllo sono appropriate solo per attivare o disattivare un'opzione, è possibile usare i pulsanti di opzione per le opzioni completamente diverse. Se entrambe le soluzioni sono possibili:
    -   Usare i pulsanti di opzione se il significato della casella di controllo deselezionata non è completamente ovvio.

        **Non corretto:**

        ![Screenshot di una casella di controllo con etichetta landscape ](images/ctrl-check-boxes-image2.png)

        In questo esempio, la scelta opposta da Landscape non è chiara, quindi la casella di controllo non è una scelta ottimale.

        **Corretto:**

        ![Screenshot di due pulsanti di opzione ](images/ctrl-check-boxes-image3.png)

        In questo esempio, le scelte non sono opposte, quindi i pulsanti di opzione sono la scelta migliore.

    -   Utilizzare pulsanti di opzione nelle pagine della procedura guidata per cancellare le alternative, anche se una casella di controllo è altrimenti accettabile.
    -   Usare i pulsanti di opzione se lo spazio dello schermo è sufficiente e le opzioni sono sufficientemente importanti per essere un buon utilizzo dello spazio dello schermo. In caso contrario, utilizzare una casella di controllo o un elenco a discesa.

        **Non corretto:**

        ![screenshot dei pulsanti Mostra e non Mostra rapporto ](images/ctrl-check-boxes-image4.png)

        In questo esempio, le opzioni non sono sufficientemente importanti da usare i pulsanti di opzione.

        **Corretto:**

        ![screenshot della casella di controllo con il messaggio non visualizzare ](images/ctrl-check-boxes-image5.png)

        In questo esempio, una casella di controllo è un uso efficiente dello spazio dello schermo per questa opzione della periferica.

-   Se sono presenti altre caselle di controllo nella finestra, utilizzare una casella di controllo.
-   **L'opzione presenta un'opzione di programma, anziché dati?** I valori dell'opzione non devono essere basati sul contesto o su altri dati. Per i dati, utilizzare un elenco di caselle di controllo o un [elenco di selezione multipla](ctrl-list-boxes.md).

## <a name="usage-patterns"></a>Modelli di utilizzo

Le caselle di controllo includono diversi modelli di utilizzo:



|                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Una singola scelta** Viene utilizzata una singola casella di controllo per selezionare una singola scelta. <br/>                                                                                                             | ![Screenshot di una casella di controllo con l'etichetta promemoria ](images/ctrl-check-boxes-image6.png)<br/> Viene utilizzata una sola casella di controllo per una singola scelta.<br/>                                                                                                                                                                                                                                                                                                                        |
| **Scelte indipendenti (zero o più)** Un gruppo di caselle di controllo viene utilizzato per effettuare una selezione da un set di zero o più opzioni.<br/>                                                                              | a differenza dei controlli a selezione singola, ad esempio [pulsanti di opzione](ctrl-radio-buttons.md), gli utenti possono selezionare qualsiasi combinazione di opzioni in un gruppo di caselle di controllo.<br/> ![Screenshot di due di tre caselle di controllo selezionate ](images/ctrl-check-boxes-image7.png)<br/> Un gruppo di caselle di controllo viene utilizzato per le scelte indipendenti.<br/>                                                                                                                                                  |
| **Scelte dipendenti (uno o più)** Un gruppo di caselle di controllo può essere utilizzato anche per effettuare una selezione da un set di una o più opzioni.<br/>                                                                         | **potrebbe essere necessario rappresentare una selezione di una o più scelte dipendenti**. Poiché Microsoft? Windows non dispone di un controllo che supporta direttamente questo tipo di input, la soluzione migliore consiste nell'usare un gruppo di caselle di controllo e gestire l'errore quando nessuna delle opzioni è selezionata.<br/> ![Screenshot di una delle due caselle di controllo selezionate ](images/ctrl-check-boxes-image8.png)<br/> Viene utilizzato un gruppo di caselle di controllo in cui è necessario selezionare almeno un protocollo.<br/> |
| **Scelta mista** Oltre agli stati selezionati e deselezionati, le caselle di controllo hanno anche uno stato misto per la selezione multipla per indicare che l'opzione è impostata per alcuni, ma non per tutti gli oggetti.<br/> | ![Screenshot di una casella di controllo di sola lettura a tinta unita blu ](images/ctrl-check-boxes-image9.png)<br/> Casella di controllo con stato misto.<br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Caselle di controllo relative ai gruppi**. Combinare le opzioni correlate e separare le opzioni non correlate in gruppi di 10 o meno, usando più gruppi, se necessario.

    ![Screenshot di caselle di controllo correlate e non correlate ](images/ctrl-check-boxes-image10.png)

    Esempio di gruppi di opzioni indipendenti correlate.

-   **Riprendere in considerazione l'utilizzo di caselle di gruppo per organizzare gruppi di caselle di controllo** , questo spesso comporta un disordine dello schermo superfluo.
-   **Elenca le caselle di controllo in un ordine logico**, ad esempio raggruppando le opzioni altamente correlate o inserendo prima le opzioni più comuni o seguendo un'altra progressione naturale. L'ordinamento alfabetico non è consigliato perché dipende dal linguaggio e pertanto non è localizzabile.
-   **Allinea le caselle di controllo verticalmente, non orizzontalmente**. L'allineamento orizzontale è più difficile da leggere.

    **Corretto:**

    ![screenshot delle caselle di controllo allineate verticalmente ](images/ctrl-check-boxes-image11.png)

    In questo esempio le caselle di controllo sono allineate correttamente.

    **Non corretto:**

    ![screenshot delle caselle di controllo allineate orizzontalmente ](images/ctrl-check-boxes-image12.png)

    In questo esempio, l'allineamento orizzontale è più difficile da leggere.

-   **Non usare lo stato misto per rappresentare un terzo stato.** Lo stato misto viene usato per indicare che un'opzione è impostata per alcuni, ma non per tutti gli oggetti figlio. Gli utenti non devono essere in grado di impostare uno stato misto direttamente piuttosto che lo stato misto è un riflesso degli oggetti figlio. Lo stato misto non viene usato come terzo stato per un singolo elemento. Per rappresentare un terzo stato, usare invece pulsanti di opzione o un elenco a discesa.

    **Non corretto:**

    ![screenshot della casella di controllo del servizio a tema blu continuo ](images/ctrl-check-boxes-image13.png)

    In questo esempio lo stato misto dovrebbe indicare che il servizio del tema non è installato.

    **Corretto:**

    ![screenshot dell'elenco a discesa con tre opzioni ](images/ctrl-check-boxes-image14.png)

    In questo esempio, gli utenti possono scegliere da un elenco di tre opzioni chiare.

-   **Facendo clic sulla casella di controllo con stato misto, verranno esaminati tutti gli stati selezionati, tutti cancellati e quelli misti originali.** Per quanto riguarda il perdono, è importante essere in grado di ripristinare lo stato misto originale, perché le impostazioni potrebbero essere complesse o sconosciute all'utente. In caso contrario, l'unico modo per ripristinare lo stato misto con confidenza è quello di annullare l'attività e ricominciare.
-   **Non usare le caselle di controllo come indicatore di stato**. Usare invece un controllo [indicatore di stato](progress-bars.md) .

    **Non corretto:**

    ![Screenshot di quattro caselle di controllo che mostrano lo stato di avanzamento ](images/ctrl-check-boxes-image15.png)

    In questo esempio le caselle di controllo vengono usate in modo errato come indicatore di stato.

    **Corretto:**

    ![Screenshot di un indicatore di stato riempito parzialmente ](images/ctrl-check-boxes-image16.png)

    Esempio di un indicatore di stato tipico.

-   **Mostra le caselle di controllo disabilitate con lo stato di selezione corretto.** Anche se gli utenti non possono modificarli, le caselle di controllo disabilitate forniscono informazioni in modo che siano coerenti con i risultati.

    **Non corretto:**

    ![Screenshot di una delle due caselle di controllo in grigio ](images/ctrl-check-boxes-image17.png)

    In questo esempio, l'opzione "leggi sempre questa sezione a voce alta" deve essere cancellata perché la sezione non viene letta quando l'opzione è disabilitata.

-   **Non usare la selezione di una casella di controllo per**:
    -   Eseguire comandi.
    -   Visualizzare altre finestre, ad esempio una finestra di dialogo per raccogliere più input.
    -   Consente di visualizzare in modo dinamico altri controlli correlati al controllo selezionato (le utilità per la lettura dello schermo non possono rilevare tali eventi).

### <a name="dont-show-this-item-again"></a>Non visualizzare <item> nuovo

-   **Provare a usare un'opzione non visualizzare <item> più questo messaggio per consentire agli utenti di disattivare una finestra di dialogo ricorrente solo se non è disponibile un'alternativa migliore.** Provare a determinare in anticipo se gli utenti necessitano effettivamente della finestra di dialogo; in caso affermativo, visualizzare sempre la finestra di dialogo e, in caso contrario, eliminare la finestra di dialogo.

Per altre linee guida ed esempi, vedere [finestre di dialogo](win-dialog-box.md).

### <a name="subordinate-controls"></a>Controlli subordinati

-   Posizionare i controlli subordinati a destra di o sotto (rientrato, svuotare con l'etichetta della casella di controllo) la casella di controllo e la relativa etichetta. Terminare l'etichetta della casella di controllo con i due punti.

    ![screenshot della casella di testo sotto l'etichetta della casella di controllo ](images/ctrl-check-boxes-image18.png)

    In questo esempio, la casella di controllo e il relativo controllo subordinato condividono l'etichetta della casella di controllo e la relativa chiave di accesso.

-   **Lasciare le caselle di testo modificabili dipendenti e gli elenchi a discesa abilitati se condividono l'etichetta della casella di controllo.** Quando gli utenti digitano o incollano qualsiasi elemento nella casella, selezionare l'opzione corrispondente automaticamente. Questa operazione semplifica l'interazione.

    ![screenshot delle caselle di testo dell'intestazione e del piè di pagina ](images/ctrl-check-boxes-image19.png)

    In questo esempio, l'immissione di un'intestazione o di un piè di pagina Seleziona automaticamente l'opzione.

-   Se si annidano le caselle di controllo con pulsanti di opzione o altre caselle di controllo, **disabilitare questi controlli subordinati fino a quando non si seleziona l'opzione di alto livello**. In questo modo si evita confusione sul significato dei controlli subordinati.
-   Rendere i controlli subordinati a una casella di controllo contigui con la casella di controllo nell'ordine di tabulazione.
-   **Se la selezione di un'opzione implica la selezione delle caselle di controllo subordinate, selezionare in modo esplicito le caselle di controllo per rendere la relazione chiara.**

    **Non corretto:**

    ![Screenshot: pulsante selezionato, caselle di controllo deselezionate ](images/ctrl-check-boxes-image20.png)

    In questo esempio le caselle di controllo subordinate non sono selezionate.

    **Corretto:**

    ![Screenshot: pulsante selezionato, caselle di controllo selezionate ](images/ctrl-check-boxes-image21.png)

    In questo esempio vengono selezionate le caselle di controllo subordinate, in modo da rendere chiara la relazione con l'opzione selezionata.

-   **Utilizzare le caselle di controllo dipendenti se le alternative aggiungono complessità superflua**. Mentre le caselle di controllo devono essere opzioni indipendenti, a volte alternative come i pulsanti di opzione aggiungono complessità superflua.

    **Corretto:**

    ![Screenshot di pulsanti e caselle di controllo confusi ](images/ctrl-check-boxes-image22.png)

    In questo esempio, l'uso dei pulsanti di opzione è accurato, ma crea una complessità non necessaria.

    **Migliore:**

    ![screenshot delle caselle di controllo ](images/ctrl-check-boxes-image23.png)

    In questo esempio, l'utilizzo di caselle di controllo è più semplice e consente agli utenti di concentrarsi sulla selezione delle opzioni desiderate invece che sulla relazione complessa.

    **Importante: applicare questa linea guida solo in circostanze estremamente rare**, quando la visualizzazione delle dipendenze aggiunge una complessità significativa senza aggiungere chiarezza. Nell'esempio precedente, è improbabile che gli utenti tenti di scegliere sia superscript che pedice e, in caso affermativo, sarebbe facile capire che si trattava di opzioni esclusive.

### <a name="default-values"></a>Valori predefiniti

-   Se una casella di controllo è relativa a un'opzione utente, **impostare il livello di sicurezza (per evitare la perdita di dati o l'accesso al sistema), per impostazione predefinita lo stato più sicuro e privato.** Se la sicurezza e la sicurezza non sono fattori, selezionare il valore più probabile o pratico.

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![Figura di ridimensionamento e spaziatura di caselle di controllo suggerite ](images/ctrl-check-boxes-image24.png)

Ridimensionamento e spaziatura consigliati per le caselle di controllo.

## <a name="labels"></a>Etichette

**Etichette casella di controllo**

-   Etichetta ogni casella di controllo.
-   Assegnare una [chiave di accesso](glossary.md) univoca a ogni etichetta. Per le linee guida, vedere [tastiera](inter-keyboard.md).
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Scrivere l'etichetta come frase o frase imperativa e non usare la punteggiatura finale.
    -   **Eccezione:** Se un'etichetta della casella di controllo contrassegna anche un controllo subordinato che lo segue, terminare l'etichetta con i due punti.
-   Scrivere l'etichetta in modo che descriva lo stato selezionato della casella di controllo.
-   Per un gruppo di caselle di controllo, utilizzare la formulazione parallela e provare a rimanere la lunghezza dello stesso per tutte le etichette.
-   Per un gruppo di caselle di controllo, concentrare il testo dell'etichetta sulle differenze tra le opzioni. Se tutte le opzioni hanno lo stesso testo introduttivo, spostare il testo nell'etichetta del gruppo.
-   Usare la formulazione positiva. Non formulare un'etichetta in modo che la selezione di una casella di controllo significhi di non eseguire un'azione.

    -   **Eccezione: non visualizzare <item> più queste** caselle di controllo.

    **Non corretto:**

    ![screenshot dell'etichetta negativa ' Disattiva '](images/ctrl-check-boxes-image25.png)

    In questo esempio, l'opzione non usa la formulazione positiva.

-   Descrivere solo l'opzione con l'etichetta. Mantieni le etichette brevi, quindi è facile farvi riferimento nei messaggi e nella documentazione. Se l'opzione richiede una spiegazione ulteriore, fornire la spiegazione in un controllo [testo statico](./glossary.md) usando le frasi complete e la punteggiatura finale.

    > [!Note]
    >
    > L'aggiunta di una spiegazione a una casella di controllo in un gruppo non significa che è necessario fornire spiegazioni per tutte le caselle di controllo del gruppo. Fornire le informazioni rilevanti nell'etichetta, se possibile, e utilizzare le spiegazioni solo quando necessario. Non semplicemente riassegnare l'etichetta per la coerenza.

     

    ![Screenshot di CheckBox, Label e Description ](images/ctrl-check-boxes-image26.png)

    In questo esempio, un'etichetta della casella di controllo contiene un testo esplicativo aggiuntivo sotto di esso.

-   Se un'opzione è fortemente consigliata, provare ad aggiungere "(scelta consigliata)" all'etichetta. Assicurarsi di aggiungere all'etichetta del controllo e non alle note aggiuntive.
-   Se è necessario utilizzare etichette a più righe, allineare la parte superiore dell'etichetta alla casella di controllo.
-   Non usare un controllo subordinato, i valori in esso contenuti o l'etichetta unità per creare una frase o una frase. Una progettazione di questo tipo non è localizzabile perché la struttura della frase varia in base alla lingua.

    **Non corretto:**

    ![screenshot dell'etichetta della casella di controllo con la casella di testo ](images/ctrl-check-boxes-image27.png)

    In questo esempio la casella di testo non viene inserita correttamente nell'etichetta della casella di controllo.

**Etichette del gruppo di caselle di controllo**

-   Utilizzare l'etichetta del gruppo per spiegare lo scopo del gruppo, non come effettuare la selezione. Si supponga che gli utenti sappiano come usare le caselle di controllo. Ad esempio, non pronunciare "selezionare una delle opzioni seguenti".
-   Terminare ogni etichetta con i due punti.
-   Non assegnare una chiave di accesso all'etichetta. Questa operazione non è necessaria e rende più difficile l'assegnazione delle altre chiavi di accesso.
-   Per una selezione di una o più scelte dipendenti, spiegare il requisito relativo all'etichetta.

    **Corretto:**

    ![screenshot dell'etichetta per due controlli: protocolli ](images/ctrl-check-boxes-image28.png)

    In questo esempio, gli utenti potrebbero pensare di poter creare solo una selezione.

    **Migliore:**

    ![screenshot dell'etichetta: i protocolli selezionano uno o più ](images/ctrl-check-boxes-image29.png)

    In questo esempio, è chiaro che gli utenti possono creare più di una selezione.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle caselle di controllo:

-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere il carattere di sottolineatura della chiave di accesso o i due punti. Includere la parola casella di controllo.
-   Fare riferimento a una casella di controllo come casella di controllo, non opzione, casella di controllo o solo casella, perché box alone è ambiguo per i localizzatori.
-   Per descrivere l'interazione dell'utente, usare SELECT e Clear.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

    Esempio: selezionare la casella di controllo **Underline** .

