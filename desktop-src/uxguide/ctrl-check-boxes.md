---
title: Caselle
description: Con una casella di controllo, gli utenti possono scegliere tra due scelte chiaramente opposte.
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 29666991d0a0659f7ff3a95f12953504b70c6dc782049ac8d93d70df73afa5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118040689"
---
# <a name="check-boxes"></a>Caselle

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con una casella di controllo, gli utenti possono scegliere tra due scelte chiaramente opposte. L'etichetta della casella di controllo indica lo stato selezionato, mentre il significato dello stato deselezionato deve essere l'opposto non ambiguo dello stato selezionato. Di conseguenza, le caselle di controllo devono essere usate solo per attivare o disattivare un'opzione **o per selezionare o deselezionare un elemento.**

![Screenshot di una delle quattro caselle di controllo selezionate ](images/ctrl-check-boxes-image1.png)

Gruppo tipico di caselle di controllo.

> [!Note]  
> Le linee guida [relative al layout](vis-layout.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **La casella di controllo consente di attivare o disattivare un'opzione o di selezionare o deselezionare un elemento?** Se non è così, usa un altro controllo.
-   **Gli stati selezionati e deselezionati sono opposti chiari e non ambigui?** In caso contrario, usare [i pulsanti di opzione](ctrl-radio-buttons.md) o un elenco a [discesa](/windows/desktop/uxguide/ctrl-drop) in modo da poter etichettare gli stati in modo indipendente.
-   **Se usato in un gruppo, il gruppo comprende scelte indipendenti, tra cui gli utenti possono scegliere zero o più?** In caso contrario, prendere in considerazione i controlli per le scelte dipendenti, ad esempio i pulsanti di opzione e [le visualizzazioni albero delle caselle di controllo.](ctrl-tree-views.md)
-   **Se usato in un gruppo, il gruppo comprende scelte dipendenti, tra cui gli utenti devono sceglierne una o più?** In tal caso, usare un gruppo di caselle di controllo e gestire l'errore quando nessuna delle opzioni è selezionata.
-   **Il numero di opzioni in un gruppo è minore o minore di 10?** Poiché lo spazio sullo schermo usato è proporzionale al numero di opzioni, mantenere il numero di caselle di controllo al massimo 10. Per più di 10 opzioni, usare un elenco [di caselle di controllo](ctrl-list-boxes.md).
-   **Un pulsante di opzione è una scelta migliore?** Se le caselle di controllo sono adatte solo per attivare o disattivare un'opzione, i pulsanti di opzione possono essere usati per opzioni completamente diverse. Se entrambe le soluzioni sono possibili:
    -   Usare i pulsanti di opzione se il significato della casella di controllo deselezionata non è del tutto ovvio.

        **Non corretto:**

        ![Screenshot di una casella di controllo con etichetta orizzontale ](images/ctrl-check-boxes-image2.png)

        In questo esempio la scelta opposta da Orizzontale non è chiara, quindi la casella di controllo non è una scelta ottimale.

        **Corretto:**

        ![Screenshot di due pulsanti di opzione ](images/ctrl-check-boxes-image3.png)

        In questo esempio le scelte non sono opposte, quindi i pulsanti di opzione sono la scelta migliore.

    -   Usare i pulsanti di opzione nelle pagine della procedura guidata per deselezionare le alternative, anche se una casella di controllo è altrimenti accettabile.
    -   Usare i pulsanti di opzione se lo spazio sullo schermo è sufficiente e le opzioni sono sufficientemente importanti da essere un buon uso di tale spazio sullo schermo. In caso contrario, utilizzare una casella di controllo o un elenco a discesa.

        **Non corretto:**

        ![screenshot dei pulsanti Mostra e Non mostra rapporto ](images/ctrl-check-boxes-image4.png)

        In questo esempio le opzioni non sono abbastanza importanti da usare i pulsanti di opzione.

        **Corretto:**

        ![Screenshot della casella di controllo con non visualizzare il messaggio ](images/ctrl-check-boxes-image5.png)

        In questo esempio, una casella di controllo è un uso efficiente dello spazio sullo schermo per questa opzione della periferica.

-   Utilizzare una casella di controllo se nella finestra sono presenti altre caselle di controllo.
-   **L'opzione presenta un'opzione di programma anziché dati?** I valori dell'opzione non devono essere basati sul contesto o su altri dati. Per i dati, usare un elenco di caselle di controllo [o un elenco a selezione multipla](ctrl-list-boxes.md).

## <a name="usage-patterns"></a>Modelli di utilizzo

Le caselle di controllo hanno diversi modelli di utilizzo:



|    Utilizzo                                                                          |         Esempio                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Una scelta individuale** Una singola casella di controllo viene usata per selezionare una singola scelta. <br/>                                                                                                             | ![Screenshot di una casella di controllo con promemoria etichetta ](images/ctrl-check-boxes-image6.png)<br/> Per una singola scelta viene utilizzata una singola casella di controllo.<br/>                                                                                                                                                                                                                                                                                                                        |
| **Scelte indipendenti (zero o più)** Un gruppo di caselle di controllo viene usato per selezionare da un set di zero o più scelte.<br/>                                                                              | A differenza dei controlli a selezione singola, ad esempio [i pulsanti di](ctrl-radio-buttons.md)opzione , gli utenti possono selezionare qualsiasi combinazione di opzioni in un gruppo di caselle di controllo.<br/> ![Screenshot di due delle tre caselle di controllo selezionate ](images/ctrl-check-boxes-image7.png)<br/> Un gruppo di caselle di controllo viene utilizzato per le scelte indipendenti.<br/>                                                                                                                                                  |
| **Scelte dipendenti (una o più)** È anche possibile utilizzare un gruppo di caselle di controllo per eseguire una selezione da un set di una o più opzioni.<br/>                                                                         | **potrebbe essere necessario rappresentare una selezione di una o più scelte dipendenti.** Poiché microsoft?windows non ha un controllo che supporta direttamente questo tipo di input, la soluzione migliore consiste nell'usare un gruppo di caselle di controllo e gestire l'errore quando non è selezionata nessuna delle opzioni.<br/> ![Screenshot di una delle due caselle di controllo selezionate ](images/ctrl-check-boxes-image8.png)<br/> Viene utilizzato un gruppo di caselle di controllo in cui è necessario selezionare almeno un protocollo.<br/> |
| **Scelta mista** Oltre agli stati selezionati e deselezionati, le caselle di controllo hanno anche uno stato misto per la selezione multipla per indicare che l'opzione è impostata per alcuni, ma non per tutti gli oggetti.<br/> | ![Screenshot di una casella di controllo di sola lettura blu a tinta unita ](images/ctrl-check-boxes-image9.png)<br/> Casella di controllo con stato misto.<br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Raggruppare le caselle di controllo correlate**. Combinare le opzioni correlate e separare le opzioni non correlate in gruppi di 10 o meno, usando più gruppi, se necessario.

    ![Screenshot delle caselle di controllo correlate e non correlate ](images/ctrl-check-boxes-image10.png)

    Esempio di gruppi di opzioni correlate e indipendenti.

-   **Riconsiderare l'uso delle caselle di** gruppo per organizzare gruppi di caselle di controllo, questo spesso comporta un superfluo disordine dello schermo.
-   **Elencare le caselle di** controllo in un ordine logico, ad esempio raggruppando le opzioni altamente correlate o inserendo prima le opzioni più comuni o seguendo un'altra progressione naturale. L'ordinamento alfabetico non è consigliato perché dipende dalla lingua e pertanto non è localizzabile.
-   **Allineare le caselle di controllo verticalmente, non orizzontalmente.** L'allineamento orizzontale è più difficile da leggere.

    **Corretto:**

    ![Screenshot delle caselle di controllo allineate verticalmente ](images/ctrl-check-boxes-image11.png)

    In questo esempio le caselle di controllo sono allineate correttamente.

    **Non corretto:**

    ![Screenshot delle caselle di controllo allineate orizzontalmente ](images/ctrl-check-boxes-image12.png)

    In questo esempio l'allineamento orizzontale è più difficile da leggere.

-   **Non usare lo stato misto per rappresentare un terzo stato.** Lo stato misto viene usato per indicare che un'opzione è impostata per alcuni, ma non per tutti, oggetti figlio. Gli utenti non devono essere in grado di impostare direttamente uno stato misto, ma lo stato misto è una reflection degli oggetti figlio. Lo stato misto non viene usato come terzo stato per un singolo elemento. Per rappresentare un terzo stato, usare invece i pulsanti di opzione o un elenco a discesa.

    **Non corretto:**

    ![Screenshot della casella di controllo solid blue theme service ](images/ctrl-check-boxes-image13.png)

    In questo esempio lo stato misto dovrebbe indicare che il servizio Tema non è installato.

    **Corretto:**

    ![Screenshot dell'elenco a discesa con tre opzioni ](images/ctrl-check-boxes-image14.png)

    In questo esempio gli utenti possono scegliere da un elenco di tre opzioni chiare.

-   **Facendo clic su una casella di controllo con stato misto è possibile scorrere tutti gli stati selezionati, tutti deselezionati e gli stati misti originali.** Per quanto possibile, è importante essere in grado di ripristinare lo stato misto originale perché le impostazioni potrebbero essere complesse o sconosciute all'utente. In caso contrario, l'unico modo per ripristinare lo stato misto in tutta sicurezza sarebbe annullare l'attività e ricominciare.
-   **Non usare le caselle di controllo come indicatore di stato**. Usare invece un [controllo indicatore di](progress-bars.md) stato.

    **Non corretto:**

    ![Screenshot di quattro caselle di controllo che mostrano lo stato di avanzamento ](images/ctrl-check-boxes-image15.png)

    In questo esempio le caselle di controllo vengono usate in modo non corretto come indicatore di stato.

    **Corretto:**

    ![Screenshot di un indicatore di stato parzialmente pieno ](images/ctrl-check-boxes-image16.png)

    Esempio di un indicatore di stato tipico.

-   **Mostra le caselle di controllo disabilitate usando lo stato di selezione corretto.** Anche se gli utenti non possono modificarle, le caselle di controllo disabilitate comunicano le informazioni in modo che siano coerenti con i risultati.

    **Non corretto:**

    ![Screenshot di una delle due caselle di controllo in grigio ](images/ctrl-check-boxes-image17.png)

    In questo esempio l'opzione "Leggi sempre questa sezione ad alta voce" deve essere deselezionata perché la sezione non viene letta quando l'opzione è disabilitata.

-   **Non usare la selezione di una casella di controllo per**:
    -   Eseguire comandi.
    -   Visualizzare altre finestre, ad esempio una finestra di dialogo per raccogliere più input.
    -   Visualizza in modo dinamico altri controlli correlati al controllo selezionato (le utilità per la lettura dello schermo non sono in grado di rilevare tali eventi).

### <a name="dont-show-this-item-again"></a>Non visualizzare questo <item> di nuovo

-   **È consigliabile usare l'opzione Non visualizzare più questa opzione per consentire agli utenti di eliminare una finestra di dialogo ricorrente solo se non esiste <item> un'alternativa migliore.** Provare a determinare in anticipo se gli utenti necessitano effettivamente del dialogo; In caso contrario, visualizzare sempre il dialogo e, in caso contrario, eliminarlo.

Per altre linee guida ed esempi, vedere [Finestre di dialogo.](win-dialog-box.md)

### <a name="subordinate-controls"></a>Controlli subordinati

-   Posizionare i controlli subordinati a destra o sotto (rientrati, scaricati con l'etichetta della casella di controllo) la casella di controllo e la relativa etichetta. Terminare l'etichetta della casella di controllo con due punti.

    ![Screenshot della casella di testo sotto l'etichetta della casella di controllo ](images/ctrl-check-boxes-image18.png)

    In questo esempio la casella di controllo e il relativo controllo subordinato condividono l'etichetta della casella di controllo e la relativa chiave di accesso.

-   **Lasciare abilitate le caselle di testo modificabili dipendenti e gli elenchi a discesa se condividono l'etichetta della casella di controllo.** Quando gli utenti digitano o incollano qualsiasi elemento nella casella, selezionare automaticamente l'opzione corrispondente. Questa operazione semplifica l'interazione.

    ![Screenshot delle caselle di testo dell'intestazione e del piè di pagina ](images/ctrl-check-boxes-image19.png)

    In questo esempio, l'immissione di un'intestazione o di un piè di pagina seleziona automaticamente l'opzione .

-   Se si annidare caselle di controllo con pulsanti di opzione o altre caselle di controllo, disabilitare questi controlli subordinati fino a quando non viene selezionata **l'opzione di alto livello**. In questo modo si evita confusione sul significato dei controlli subordinati.
-   Rendere contigui i controlli subordinati a una casella di controllo con la casella di controllo nell'ordine di tabulazione.
-   **Se la selezione di un'opzione implica la selezione di caselle di controllo subordinate, selezionarle in modo esplicito per rendere chiara la relazione.**

    **Non corretto:**

    ![screenshot: pulsante selezionato, caselle di controllo deselezionate ](images/ctrl-check-boxes-image20.png)

    In questo esempio le caselle di controllo subordinate non sono selezionate.

    **Corretto:**

    ![screenshot: pulsante selezionato, caselle di controllo selezionate ](images/ctrl-check-boxes-image21.png)

    In questo esempio le caselle di controllo subordinate sono selezionate, rendendo deselezionata la relazione con l'opzione selezionata.

-   **Usare le caselle di controllo dipendenti se le alternative aggiungono complessità non necessaria.** Anche se le caselle di controllo devono essere opzioni indipendenti, a volte alternative come i pulsanti di opzione aggiungono complessità non necessaria.

    **Corretto:**

    ![Screenshot di pulsanti e caselle di controllo confusi ](images/ctrl-check-boxes-image22.png)

    In questo esempio l'uso dei pulsanti di opzione è accurato, ma crea complessità non necessaria.

    **Migliore:**

    ![Screenshot solo delle caselle di controllo ](images/ctrl-check-boxes-image23.png)

    In questo esempio, l'uso delle caselle di controllo è più semplice e consente agli utenti di concentrarsi sulla selezione delle opzioni desiderate anziché sulla relazione complessa.

    **Importante: applicare queste linee guida solo in circostanze estremamente rare,** quando la visualizzazione delle dipendenze aggiunge una complessità significativa senza maggiore chiarezza. Nell'esempio precedente è improbabile che gli utenti tentino di scegliere sia l'apice che l'indice e, in caso contrario, sarebbe facile comprendere che si trattasse di opzioni esclusive.

### <a name="default-values"></a>Valori predefiniti

-   Se una casella di controllo è per un'opzione utente, impostare lo stato più sicuro (per evitare la perdita di dati o l'accesso al sistema), lo stato più sicuro e privato **per impostazione predefinita.** Se la sicurezza e la sicurezza non sono fattori, selezionare il valore più probabile o conveniente.

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

![figura del ridimensionamento e della spaziatura delle caselle di controllo suggerite ](images/ctrl-check-boxes-image24.png)

Dimensioni e spaziatura consigliate per le caselle di controllo.

## <a name="labels"></a>Etichette

**Etichette delle caselle di controllo**

-   Assegnare un'etichetta a ogni casella di controllo.
-   Assegnare una chiave [di accesso univoca](glossary.md) a ogni etichetta. Per le linee guida, vedere [Tastiera.](inter-keyboard.md)
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Scrivere l'etichetta come frase o frase imperativa e non usare punteggiatura finale.
    -   **Eccezione:** Se un'etichetta di casella di controllo etichetta anche un controllo subordinato che la segue, terminare l'etichetta con due punti.
-   Scrivere l'etichetta in modo che descriva lo stato selezionato della casella di controllo.
-   Per un gruppo di caselle di controllo, usare la formulazione parallela e provare a mantenere la lunghezza circa la stessa per tutte le etichette.
-   Per un gruppo di caselle di controllo, concentrare il testo dell'etichetta sulle differenze tra le opzioni. Se tutte le opzioni hanno lo stesso testo introduttivo, spostare il testo nell'etichetta del gruppo.
-   Usare la formulazione positiva. Non formulare un'etichetta in modo che la selezione di una casella di controllo non comporta l'esecuzione di un'azione.

    -   **Eccezione: non visualizzare più le <item> caselle** di controllo.

    **Non corretto:**

    ![Screenshot dell'etichetta negativa 'turn off'](images/ctrl-check-boxes-image25.png)

    In questo esempio l'opzione non usa la formulazione positiva.

-   Descrivere solo l'opzione con l'etichetta. Tenere brevi le etichette in modo che sia facile fare riferimento a esse nei messaggi e nella documentazione. Se l'opzione richiede un'ulteriore spiegazione, fornire la spiegazione in un controllo di testo [statico](./glossary.md) usando frasi complete e terminando la punteggiatura.

    > [!Note]
    >
    > L'aggiunta di una spiegazione a una casella di controllo in un gruppo non significa che sia necessario fornire spiegazioni per tutte le caselle di controllo nel gruppo. Se possibile, fornire le informazioni rilevanti nell'etichetta e usare le spiegazioni solo quando necessario. Non limitarsi a rievalutare l'etichetta per la coerenza.

     

    ![Screenshot della casella di controllo, dell'etichetta e della descrizione ](images/ctrl-check-boxes-image26.png)

    In questo esempio, sotto l'etichetta di una casella di controllo è presente altro testo esplicativo.

-   Se un'opzione è fortemente consigliata, è consigliabile aggiungere "(scelta consigliata)" all'etichetta. Assicurarsi di aggiungere all'etichetta del controllo, non le note supplementari.
-   Se è necessario usare etichette su più righe, allineare la parte superiore dell'etichetta alla casella di controllo.
-   Non usare un controllo subordinato, i valori in esso contenuti o l'etichetta di unità per creare una frase o una frase. Tale progettazione non è localizzabile perché la struttura delle frasi varia in base alla lingua.

    **Non corretto:**

    ![Screenshot dell'etichetta della casella di controllo con la casella di testo al suo interno ](images/ctrl-check-boxes-image27.png)

    In questo esempio la casella di testo viene inserita erroneamente all'interno dell'etichetta della casella di controllo.

**Etichette di gruppo delle caselle di controllo**

-   Usare l'etichetta del gruppo per spiegare lo scopo del gruppo, non come effettuare la selezione. Si supponga che gli utenti sappiano come usare le caselle di controllo. Ad esempio, non pronunciare "Selezionare una delle opzioni seguenti".
-   Terminare ogni etichetta con due punti.
-   Non assegnare una chiave di accesso all'etichetta. Questa operazione non è necessaria e rende più difficile l'assegnazione delle altre chiavi di accesso.
-   Per una selezione di una o più scelte dipendenti, spiegare il requisito sull'etichetta.

    **Corretto:**

    ![Screenshot dell'etichetta per due controlli: protocolli ](images/ctrl-check-boxes-image28.png)

    In questo esempio, gli utenti potrebbero pensare di poter effettuare una sola selezione.

    **Migliore:**

    ![Screenshot dell'etichetta: i protocolli selezionano uno o più ](images/ctrl-check-boxes-image29.png)

    In questo esempio è chiaro che gli utenti possono effettuare più selezioni.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento a caselle di controllo:

-   Usare il testo esatto dell'etichetta, inclusa la combinazione di maiuscole e minuscole, ma non includere il carattere di sottolineatura o i due punti della chiave di accesso. Includere la casella di controllo della parola.
-   Fare riferimento a una casella di controllo come casella di controllo, non come opzione, casella di controllo o semplicemente casella, perché la sola casella è ambigua per i localizzatori.
-   Per descrivere l'interazione dell'utente, usare select e clear.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

    Esempio: selezionare la **casella di controllo** Sottolineatura.

