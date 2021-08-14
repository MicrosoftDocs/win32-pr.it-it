---
title: Elenchi a discesa Caselle combinate
description: Con un elenco a discesa o una casella combinata, gli utenti possono scegliere tra un elenco di valori che si escludono a vicenda.
ms.assetid: dbe88cf1-7946-4343-bc16-ce12be7ce205
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e74589da084a9f4c9f950336b3093452988052b57aba42e6a7a8f449f24a254f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966275"
---
# <a name="drop-down-lists--combo-boxes"></a>Elenchi a discesa & caselle combinate

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con un elenco a discesa o una casella combinata, gli utenti possono scegliere tra un elenco di valori che si escludono a vicenda. Gli utenti possono scegliere una sola opzione. Con un elenco a discesa standard, gli utenti sono limitati alle scelte nell'elenco, ma con una casella combinata possono immettere una scelta non presente nell'elenco.

![Screenshot della casella combinata dell'ora del promemoria ](images/ctrl-drop-image1.png)

Casella combinata tipica.

I termini seguenti sono importanti da comprendere durante la lettura di questo articolo:

-   Una casella di riepilogo standard è una casella contenente un elenco di più elementi, con più elementi visibili.
-   Un elenco a discesa è un elenco in cui l'elemento selezionato è sempre visibile e gli altri sono visibili su richiesta facendo clic su un pulsante a discesa.
-   Una casella combinata è una combinazione di una casella di [](ctrl-text-boxes.md)riepilogo standard o di un elenco a discesa e di una casella di testo modificabile, consentendo così agli utenti di immettere un valore non presente nell'elenco.
    -   Un elenco a discesa modificabile è una combinazione di un elenco a discesa e di una casella di testo modificabile.
    -   Una casella di riepilogo modificabile è una combinazione di una casella di riepilogo standard e di una casella di testo modificabile.

> [!Note]  
> Le linee guida [correlate al layout](vis-layout.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Il controllo viene usato per scegliere un'opzione da un elenco di valori che si escludono a vicenda?** Se non è così, usa un altro controllo. Per scegliere più opzioni, usare invece un elenco a selezione multipla [standard,](ctrl-list-boxes.md)un elenco di caselle di controllo, un generatore di elenchi o un elenco di aggiunta/rimozione.
-   **I comandi delle opzioni sono?** In caso contrario, usare un [pulsante di menu](ctrl-command-buttons.md) o un pulsante di divisione. Usare elenchi a discesa e caselle combinate per oggetti (sostantivi) o attributi (aggettivi), ma non comandi (verbi).
-   **L'elenco presenta dati anziché opzioni di programma?** In entrambi i modi, un elenco a discesa o una casella combinata è una scelta appropriata. Al contrario, [i pulsanti di opzione](ctrl-radio-buttons.md) sono adatti solo per un numero ridotto di opzioni del programma.

**Elenchi a discesa**

-   **Esiste un'opzione predefinita consigliata per la maggior parte degli utenti nella maggior parte dei casi?** L'opzione selezionata è molto più importante rispetto alla visualizzazione delle alternative? È consigliabile usare un elenco a discesa se non si vuole invitare gli utenti a apportare modifiche nascondendo le alternative. In caso contrario, si considerino i pulsanti di opzione, un elenco a selezione singola o una casella di riepilogo modificabile, che offrono maggiore enfasi sulle scelte alternative.

    ![Screenshot con la massima qualità come pulsante predefinito ](images/ctrl-drop-image2.png)

    In questo esempio, la qualità del colore più elevata è la scelta migliore per la maggior parte degli utenti, quindi un elenco a discesa è una buona scelta per eseguire il downplay delle alternative.

-   **Si vuole attirare l'attenzione sull'opzione ?** In tal caso, si considerino i pulsanti di opzione, un elenco a selezione singola o una casella di riepilogo modificabile, che tendono a attirare maggiore attenzione occupando più spazio sullo schermo. Poiché gli elenchi a discesa sono compatti, sono una buona scelta per le opzioni da sottodimensionare.
-   **Lo spazio dello schermo è premium?** In tal caso, usare un elenco a discesa perché lo spazio dello schermo usato è fisso e indipendente dal numero di scelte.
-   **Nella finestra sono presenti altri elenchi a discesa?** In tal caso, è consigliabile usare un elenco a discesa per garantire la coerenza.

**Elenchi a discesa modificabili**

Oltre ai principi appena forniti per gli elenchi a discesa, si applicano anche gli elementi seguenti:

-   **Le scelte possibili sono vincolate?** In caso contrario, usare un normale elenco a discesa. Le caselle combinate sono per input non vincolato, in cui gli utenti potrebbero dover immettere un valore non presente nell'elenco. Poiché l'input non è vincolato, se gli utenti immettono testo non valido, è necessario gestire l'errore con un messaggio di errore.
-   **È possibile enumerare in anticipo le scelte più probabili?** In caso contrario, usare una casella di testo.
-   **L'elenco a discesa viene usato per elencare l'input utente precedente?** A meno che gli utenti non necessitino di esaminare l'elenco completo dell'input precedente, usare invece una casella di testo con l'opzione di completamento automatico.

    ![Screenshot della finestra di dialogo Esegui con elenco a discesa ](images/ctrl-drop-image3.png)

    In questo esempio, gli utenti potrebbero dover rivedere l'input precedente, quindi un elenco a discesa modificabile è una buona scelta.

    ![Screenshot di Outlook da riga a riga e completamento automatico ](images/ctrl-drop-image4.png)

    In questo esempio, una casella di testo con completamento automatico è una buona scelta.

-   **Gli utenti avranno bisogno di assistenza per la selezione dei valori validi?** In tal caso, usare una casella di testo con [un pulsante Sfoglia.](ctrl-command-buttons.md)

    ![Screenshot di Outlook da riga a riga e pulsante Sfoglia ](images/ctrl-drop-image5.png)

    In questo esempio gli utenti possono fare clic su "A" per consentire loro di selezionare valori validi.

-   **È importante invitare gli utenti a rivedere le scelte alternative o invitare le modifiche?** In tal caso, è consigliabile usare una casella di riepilogo modificabile. Con un elenco a discesa modificabile, gli utenti non saranno a conoscenza delle alternative fino a quando l'elenco non viene eliminato.
-   **Gli utenti devono individuare rapidamente un elemento in un elenco di grandi dimensioni?** (solo Win32) In tal caso, usare una casella combinata perché gli utenti possono selezionare un elemento digitandone il nome completo. Al contrario, l'elenco a discesa Win32 seleziona gli elementi in base solo all'ultimo carattere digitato(quindi digitare "Jun" in un elenco di mesi corrisponderebbe a novembre, non a giugno). In questo caso, usare una casella combinata anche se le scelte possibili sono vincolate.

**Caselle di riepilogo modificabili**

-   **Le scelte possibili sono vincolate?** In caso contrario, usare un elenco a selezione singola o un elenco a discesa normale. Le caselle combinate sono per l'input senza vincoli, in cui gli utenti potrebbero dover immettere un valore non presente nell'elenco. Poiché l'input non è vincolato, se gli utenti immettono testo non valido, è necessario gestire l'errore con un messaggio di errore.
-   **È possibile enumerare in anticipo le scelte più probabili?** In caso contrario, usare una casella di testo.
-   **È importante invitare gli utenti a rivedere le scelte alternative o invitare le modifiche?** In caso contrario, prendere in considerazione un elenco a discesa modificabile.
-   **Si vuole attirare l'attenzione sull'opzione ?** In caso contrario, prendere in considerazione un elenco a discesa modificabile. Poiché gli elenchi a discesa sono compatti, sono una buona scelta per le opzioni da sottodimensionare.
-   **Lo spazio dello schermo è premium?** In tal caso, usare un elenco a discesa modificabile perché lo spazio sullo schermo usato è fisso e indipendente dal numero di scelte.

Per gli elenchi a discesa, il numero di elementi **nell'elenco** non è un fattore importante nella scelta del controllo perché vengono ridimensionati da migliaia di elementi fino a uno. Gli elenchi a discesa modificabili vengono ridimensionati da migliaia di elementi a nessuno, perché gli utenti possono immettere un valore non presente nell'elenco. Poiché gli elenchi a discesa possono essere usati per i dati, il numero di elementi potrebbe non essere noto in anticipo e potrebbe non essere garantito. **Includere sempre almeno tre elementi nelle caselle di riepilogo modificabili per giustificare lo spazio aggiuntivo dello schermo.**

## <a name="usage-patterns"></a>Modelli di utilizzo

Gli elenchi a discesa e le caselle combinate hanno diversi modelli di utilizzo:



|   Utilizzo     |    Esempio   |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nell'elenco** a discesa viene visualizzato un elenco a discesa standard, con un set fisso di valori predeterminati. <br/>                                 | quando viene chiuso, è visibile solo l'elemento selezionato. Quando gli utenti fa clic sul pulsante a discesa, tutte le opzioni diventano visibili. per modificare il valore, gli utenti aprono l'elenco e fare clic su un altro valore.<br/> ![Screenshot dell'elenco a discesa, opzioni nascoste ](images/ctrl-drop-image6.png)<br/> In questo esempio l'elenco è nello stato normale.<br/> ![screenshot dell'elenco a discesa, opzioni visualizzate ](images/ctrl-drop-image7.png)<br/> In questo esempio l'elenco è stato eliminato.<br/> |
| **Elenco a discesa Anteprima un** elenco a discesa che visualizza in anteprima i risultati della selezione per consentire agli utenti di scegliere.<br/>             | ![Screenshot delle opzioni di colore e testo ](images/ctrl-drop-image8.png)<br/> In questi esempi gli elenchi a discesa visualizzano in anteprima i risultati della selezione.<br/>                                                                                                                                                                                                                                                                                                                                           |
| **Elenco a discesa modificabile** una casella combinata a discesa, che consente agli utenti di immettere un valore non presente nell'elenco a discesa.<br/> | ![aa511458.dropdownlists27(en-us,msdn.10).png](images/ctrl-drop-image9.png)![Screenshot della casella combinata dimensione carattere modificabile ](images/ctrl-drop-image10.png)<br/> Esempi di un elenco a discesa modificabile in modalità di modifica ed elenco a discesa.<br/> Usare questo controllo quando si vuole offrire la flessibilità di una casella di testo, ma si vuole aiutare gli utenti fornendo un comodo elenco di possibili scelte.<br/>                                                                                                   |
| **Le caselle di riepilogo** modificabili consentono agli utenti di immettere un valore non presente nell'elenco sempre visibile. <br/> | ![Screenshot dell'elenco a discesa delle opzioni del tipo di carattere ](images/ctrl-drop-image11.png)<br/> In questi esempi vengono sempre visualizzate le caselle di riepilogo modificabili.<br/> Questo controllo è una scelta migliore rispetto all'elenco a discesa modificabile quando è importante invitare gli utenti a rivedere le scelte alternative o invitare le modifiche.<br/>                                                                                                                                                                      |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Non usare la modifica di un elenco a** discesa o di una casella combinata in :
    -   Eseguire comandi.
    -   Visualizzare altre finestre, ad esempio una finestra di dialogo per raccogliere più input.
    -   Visualizzare dinamicamente altri controlli correlati al controllo selezionato ( le[utilità per la](inter-accessibility.md) lettura dello schermo non possono rilevare tali eventi).

### <a name="presentation"></a>Presentazione

-   **Ordinare gli elementi dell'elenco in** ordine logico, ad esempio raggruppando le opzioni altamente correlate, inserendo prima le opzioni più comuni o usando l'ordine alfabetico. Ordinare i nomi in ordine alfabetico, i numeri in ordine numerico e le date in ordine cronologico. Gli elenchi con 12 o più elementi devono essere ordinati alfabeticamente per semplificare la ricerca degli elementi.

    **Corretto:** ![ Screenshot dell'elenco a discesa logico ](images/ctrl-drop-image12.png)

    In questo esempio, gli elementi dell'elenco vengono ordinati in base alla relazione spaziale.

    **Non corretto:** ![ Screenshot dell'elenco a discesa disorganizzato ](images/ctrl-drop-image13.png)

    In questo esempio sono presenti così tanti elementi dell'elenco che devono essere ordinati in ordine alfabetico.

    **Corretto:** ![ Screenshot dell'elenco a discesa in ordine alfabetico ](images/ctrl-drop-image14.png)

    In questo esempio gli elementi dell'elenco vengono ordinati in ordine alfabetico, ad eccezione dell'opzione che rappresenta tutti gli elementi.

-   **Posizionare le opzioni che rappresentano All o None all'inizio dell'elenco, indipendentemente dall'ordinamento degli elementi rimanenti.**
-   **Racchiudere le meta-opzioni tra parentesi.**

    ![Screenshot che mostra un elenco a discesa con l'opzione '(None)' selezionata.](images/ctrl-drop-image15.png)

    In questo esempio, "(None)" è una meta-opzione perché non è un valore valido per la scelta, ma descrive che l'opzione stessa non viene usata.

-   **Quando si disabilita un elenco a discesa o una casella combinata, disabilitare anche le etichette e i pulsanti di comando associati.**

### <a name="drop-down-lists"></a>Elenchi a discesa

-   Quando si usa un singolo elenco a discesa per modificare la visualizzazione di un controllo associato, modificare la visualizzazione immediatamente alla selezione anziché richiedere **un pulsante di comando separato.** Usare un pulsante di comando separato solo se il rendering dell'elenco richiede una quantità significativa di tempo. Tuttavia, le intestazioni di elenco [e i pulsanti di menu](ctrl-command-buttons.md) sono i controlli preferiti a questo scopo.
-   **Non sono presenti elementi elenco vuoti che** **usano le meta-opzioni.** Gli utenti non sanno interpretare gli elementi vuoti, mentre il significato delle meta-opzioni è esplicito.

    **Corretto:** ![ Screenshot dell'elenco a discesa con nessuno selezionato ](images/ctrl-drop-image16.png)

    **Non corretto:** ![ Screenshot dell'elenco a discesa con l'opzione vuota selezionata ](images/ctrl-drop-image17.png)

    Nell'esempio non corretto, il significato dell'opzione vuota non è chiaro.

### <a name="preview-drop-down-lists"></a>Elenchi a discesa di anteprima

-   **Usare le anteprime negli elementi dell'elenco quando è meglio mostrarlo con le immagini anziché descrivere l'uso del solo testo.**

    ![Screenshot dell'elenco a discesa dei tipi di carattere visualizzati in anteprima ](images/ctrl-drop-image18.png)

    In questo esempio, l'anteprima illustra le opzioni molto meglio del solo testo.

-   Non usare icone inutili e inutili nelle **anteprime.**

    **Non corretto:** ![ Screenshot dell'elenco a discesa di etichette con icone ](images/ctrl-drop-image19.png)

    In questo esempio le icone di anteprima non sono necessarie perché non comunicano alcuna informazione.

### <a name="combo-boxes"></a>Caselle combinate

-   **Limitare la lunghezza del testo di input quando è possibile.** Ad esempio, se l'input valido è un numero compreso tra 0 e 999, usare una casella combinata limitata a tre caratteri.
-   **Se sono disponibili molte opzioni possibili, concentrare il contenuto dell'elenco sulle opzioni più probabili.** Poiché gli utenti possono immettere valori non presenti nell'elenco, le caselle combinate non devono elencare tutte le scelte, solo le scelte possibili o un esempio rappresentativo.

    ![Screenshot dell'elenco a discesa delle dimensioni dei caratteri ](images/ctrl-drop-image10.png)

    In questo esempio non sono elencate molte opzioni valide, ad esempio 15 o tipi di carattere di mezza dimensione, ad esempio 9,5.

### <a name="default-values"></a>Valori predefiniti

-   **Selezionare l'opzione più sicura (per evitare la perdita di dati o l'accesso al sistema) e l'opzione più sicura per impostazione predefinita.** Se la sicurezza e la sicurezza non sono fattori, selezionare l'opzione più probabile o conveniente.
    -   **Eccezione:** Visualizzare un valore predefinito vuoto se il [](glossary.md)controllo rappresenta una proprietà in uno stato misto, che si verifica quando si visualizza una proprietà per più oggetti che non hanno la stessa impostazione.

## <a name="prompts"></a>Prompt

Un prompt è un'etichetta o un'istruzione breve inserita in un elenco a discesa modificabile come valore predefinito. A differenza del testo statico, i prompt scompaiono dalla schermata quando gli utenti digitano qualcosa nella casella combinata o quando ottiene lo stato attivo per l'input.

![Screenshot di una casella di ricerca ](images/ctrl-drop-image20.png)

Un prompt tipico.

Usare un prompt quando:

-   Lo spazio dello schermo è così premium che l'uso di un'etichetta o di un'istruzione è indesiderato, ad esempio su una barra degli strumenti.
-   La richiesta è principalmente per identificare lo scopo dell'elenco in modo compatto. Non devono essere informazioni cruciali che gli utenti devono visualizzare durante l'uso della casella combinata.

Non usare i prompt solo per indirizzare gli utenti a selezionare un elemento dall'elenco o a fare clic sui pulsanti. Ad esempio, le richieste come Selezionare un'opzione o Immettere un nome file e quindi fare clic su Invia non sono necessarie.

Quando si usano i prompt:

-   Disegnare il testo di richiesta in grigio corsivo e il testo reale in nero normale. Il testo della richiesta non deve essere confuso con il testo reale.
-   Mantenere il testo del prompt conciso. È possibile usare frammenti anziché frasi complete.
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Non usare la punteggiatura finale o i puntini di sospensione.
-   Il testo del prompt non deve essere modificabile e deve scomparire quando gli utenti fa clic o compaiono nella casella di testo.
    -   **Eccezione:** La richiesta viene visualizzata se la casella di testo ha lo stato attivo per l'input predefinito e scompare solo quando l'utente inizia a digitare.
-   Il testo del prompt viene ripristinato se la casella di testo è ancora vuota quando perde lo stato attivo per l'input.

**Non corretto:** ![ Screenshot di sei elenchi a discesa modificabili](images/ctrl-drop-image21.png)

In questo esempio lo spazio dello schermo non è premium. Dopo aver compilato un elenco a discesa modificabile, è difficile che gli utenti ricordino a cosa è necessario. e il testo di richiesta è modificabile e disegnato allo stesso modo del testo reale.

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

![Screenshot dell'elenco a discesa e delle specifiche ](images/ctrl-drop-image22.png)

Dimensioni e spaziatura consigliate per elenchi a discesa e caselle combinate.

-   **Scegliere una larghezza appropriata per i dati validi più lunghi.** Gli elenchi a discesa non possono essere scorrendo orizzontalmente, quindi gli utenti possono visualizzare solo ciò che è visibile nel controllo . Si noti, tuttavia, che le caselle combinate possono avere la funzionalità Di scorrimento automatico abilitata.
-   **Includere un ulteriore 30%** (fino al 200% per il testo più breve) per qualsiasi testo (ma non numeri) che verrà localizzato.
-   **Scegliere una lunghezza dell'elenco che elimini lo scorrimento verticale non necessario.** Poiché gli elenchi a discesa vengono visualizzati su richiesta, i relativi elenchi devono essere visualizzati fino a 30 elementi. Le caselle di riepilogo modificabili (quelle che non hanno un pulsante a discesa) devono essere visualizzate tra 3 e 12 elementi.

## <a name="labels"></a>Etichette

**Etichette di controllo**

-   Scrivere l'etichetta come parola o frase, non come frase e terminarla con due punti. **Eccezioni:**
    -   Elenchi a discesa modificabili con prompt che si trovano in un punto in cui lo spazio è premium.
    -   Se un elenco a discesa o una casella combinata è subordinata a un pulsante di opzione o a una casella di controllo e viene introdotta dalla relativa etichetta che termina con due punti, non inserire un'etichetta aggiuntiva nel controllo.
-   Assegnare una chiave [di accesso univoca](glossary.md) per ogni etichetta. Per le linee guida, vedere [Tastiera](inter-keyboard.md).
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Posizionare l'etichetta a sinistra o sopra il controllo e allineare l'etichetta al bordo sinistro del controllo. Se l'etichetta è a sinistra, allineare verticalmente il testo dell'etichetta al testo del controllo.

    **Corretto:** ![ Screenshot dell'allineamento dell'etichetta dell'elenco a discesa ](images/ctrl-drop-image23.png)

    In questo esempio l'etichetta è allineata correttamente al testo del controllo .

    **Non corretto:** ![ Screenshot dell'elenco a discesa allineato in modo non corretto ](images/ctrl-drop-image24.png)

    In questo esempio l'etichetta è allineata in modo non corretto al testo del controllo .

-   È possibile specificare unità (secondi, connessioni e così via) tra parentesi dopo l'etichetta.
-   Non rendere il contenuto dell'elenco a discesa o della casella combinata (o della relativa etichetta di unità) parte di una frase, perché non è localizzabile.

**Testo dell'opzione**

-   Assegnare un nome univoco a ogni opzione.
-   Usare [l'uso di maiuscole e minuscole](glossary.md)in stile frase, a meno che un elemento non sia un sostantivo appropriato.
-   Scrivere l'etichetta come parola o frase, non come frase e non usare la punteggiatura finale.
-   Usare la formulazione parallela e provare a mantenere la lunghezza circa la stessa per tutte le opzioni.

**Testo informativo**

-   Se è necessario aggiungere testo informativo su un elenco a discesa o una casella combinata, aggiungerlo sopra l'etichetta. Usare frasi complete con punteggiatura finale.
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Le informazioni aggiuntive utili ma non necessarie devono essere mantenute brevi. Inserire queste informazioni tra parentesi tra l'etichetta e i due punti o senza parentesi sotto il controllo.

    ![Screenshot dell'elenco a discesa con dati aggiunti ](images/ctrl-drop-image25.png)

    Questo esempio mostra informazioni aggiuntive inserite sotto il controllo .

## <a name="documentation"></a>Documentazione

Quando si fa riferimento agli elenchi a discesa:

-   Usare il testo esatto dell'etichetta, inclusa l'uso di maiuscole e minuscole, ma non includere il carattere di sottolineatura o i due punti della chiave di accesso. includere l'elenco o la casella, a seconda di quale sia più chiaro.
-   Per le opzioni dell'elenco, usare il testo esatto dell'opzione, inclusa l'uso di maiuscole e minuscole.
-   Nella programmazione e in altri documenti tecnici, fare riferimento agli elenchi a discesa come elenchi a discesa. In qualsiasi altro luogo, usare un elenco o una casella, a seconda di quale sia più chiaro.
-   Per descrivere l'interazione dell'utente, usare click.
-   Quando possibile, formattare le opzioni di etichetta ed elenco usando il testo in grassetto. In caso contrario, inserire l'etichetta e le opzioni tra virgolette solo se necessario per evitare confusione.

Esempio: **nell'elenco Dimensioni carattere fare** clic su Caratteri **grandi**.

Quando si fa riferimento a caselle combinate:

-   Usare il testo esatto dell'etichetta, inclusa l'uso di maiuscole e minuscole, ma non includere il carattere di sottolineatura o i due punti della chiave di accesso. includere la casella della parola.
-   Per le opzioni dell'elenco, usare il testo esatto dell'opzione, inclusa l'uso di maiuscole e minuscole.
-   Nella programmazione e in altre documentazione tecnica, fare riferimento alle caselle combinate come caselle combinate. In qualsiasi altro luogo, usare box.
-   Per descrivere l'interazione dell'utente, usare INVIO.
-   Quando possibile, formattare le opzioni di etichetta ed elenco usando il testo in grassetto. In caso contrario, inserire l'etichetta e le opzioni tra virgolette solo se necessario per evitare confusione.

Esempio: nella **casella Tipo** di carattere immettere il tipo di carattere da usare.

 

