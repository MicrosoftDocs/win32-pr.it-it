---
title: Elenchi a discesa caselle combinate
description: Con un elenco a discesa o una casella combinata, gli utenti fanno una scelta tra un elenco di valori che si escludono a vicenda.
ms.assetid: dbe88cf1-7946-4343-bc16-ce12be7ce205
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 646fb569cf3a7861d68d0eb885107ba12978c101
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104234451"
---
# <a name="drop-down-lists--combo-boxes"></a>Elenchi a discesa & caselle combinate

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con un elenco a discesa o una casella combinata, gli utenti fanno una scelta tra un elenco di valori che si escludono a vicenda. Gli utenti possono scegliere solo una delle opzioni. Con un elenco a discesa standard, gli utenti sono limitati alle scelte nell'elenco, ma con una casella combinata è possibile immettere una scelta non presente nell'elenco.

![cattura di schermata della casella combinata ora promemoria ](images/ctrl-drop-image1.png)

Casella combinata tipica.

I termini seguenti sono importanti da comprendere durante la lettura di questo articolo:

-   Una casella di riepilogo standard è una casella contenente un elenco di più elementi, con più elementi visibili.
-   Un elenco a discesa è un elenco in cui l'elemento selezionato è sempre visibile e gli altri sono visibili su richiesta facendo clic su un pulsante a discesa.
-   Una casella combinata è una combinazione di una casella di riepilogo standard o un elenco a discesa e una [casella di testo](ctrl-text-boxes.md)modificabile, consentendo così agli utenti di immettere un valore non incluso nell'elenco.
    -   Un elenco a discesa modificabile è una combinazione di un elenco a discesa e una casella di testo modificabile.
    -   Una casella di riepilogo modificabile è una combinazione di una casella di riepilogo standard e una casella di testo modificabile.

> [!Note]  
> Le linee guida correlate al [layout](vis-layout.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Il controllo viene usato per scegliere un'opzione da un elenco di valori che si escludono a vicenda?** Se non è così, usa un altro controllo. Per scegliere più opzioni, utilizzare un [elenco di selezione multipla standard](ctrl-list-boxes.md), un elenco di caselle di controllo, un generatore di elenchi o un elenco di aggiunta/rimozione.
-   **Sono disponibili i comandi Options?** In caso affermativo, usare invece un [pulsante di menu](ctrl-command-buttons.md) o un pulsante di menu combinato. Usare elenchi a discesa e caselle combinate per gli oggetti (sostantivi) o gli attributi (aggettivi), ma non i comandi (verbi).
-   **L'elenco presenta i dati, anziché le opzioni di programma?** In entrambi i casi, un elenco a discesa o una casella combinata è una scelta appropriata. Al contrario, i [pulsanti di opzione](ctrl-radio-buttons.md) sono adatti solo per un numero ridotto di opzioni di programma.

**Elenchi a discesa**

-   **Esiste un'opzione predefinita consigliata per la maggior parte degli utenti nella maggior parte dei casi?** L'opzione selezionata è molto più importante che vedere le alternative? Prendere in considerazione l'uso di un elenco a discesa se non si vuole incoraggiare gli utenti a apportare modifiche nascondendo le alternative. In caso contrario, prendere in considerazione i pulsanti di opzione, un elenco a selezione singola o una casella di riepilogo modificabile, che offrono maggiore enfasi sulle scelte alternative.

    ![cattura di schermata del pulsante predefinito di qualità superiore ](images/ctrl-drop-image2.png)

    In questo esempio, la qualità del colore più elevata è la scelta migliore per la maggior parte degli utenti, quindi un elenco a discesa rappresenta una scelta ottimale per minimizzare le alternative.

-   **Si desidera attirare l'attenzione sull'opzione?** In tal caso, prendere in considerazione i pulsanti di opzione, un elenco a selezione singola o una casella di riepilogo modificabile, che tende a attirare più attenzione occupando più spazio sullo schermo. Poiché gli elenchi a discesa sono di dimensioni compatte, sono ottime scelte per le opzioni che si desidera sottoporre a sottolineatura.
-   **Lo spazio dello schermo è Premium?** In tal caso, utilizzare un elenco a discesa poiché lo spazio dello schermo utilizzato è fisso e indipendente dal numero di opzioni.
-   **Sono presenti altri elenchi a discesa nella finestra?** In tal caso, provare a usare un elenco a discesa per coerenza.

**Elenchi a discesa modificabili**

Oltre ai principi appena forniti per gli elenchi a discesa, si applicano anche gli elementi seguenti:

-   **Le scelte possibili sono limitate?** In tal caso, utilizzare invece un normale elenco a discesa. Le caselle combinate sono per l'input non vincolato, in cui gli utenti potrebbero dover immettere un valore che non è attualmente presente nell'elenco. Poiché l'input non è vincolato, se gli utenti immettono testo non valido è necessario gestire l'errore con un messaggio di errore.
-   **È possibile enumerare le scelte più probabili in anticipo**? In caso contrario, utilizzare una casella di testo.
-   **Si tratta dell'elenco a discesa usato per elencare l'input dell'utente precedente?** A meno che gli utenti non debbano rivedere l'elenco completo dell'input precedente, usare invece una casella di testo con l'opzione di completamento automatico.

    ![screenshot della finestra di dialogo Esegui con elenco a discesa ](images/ctrl-drop-image3.png)

    In questo esempio, è possibile che gli utenti debbano rivedere l'input precedente, quindi un elenco a discesa modificabile rappresenta una scelta ottimale.

    ![Screenshot di Outlook in linea e completamento automatico ](images/ctrl-drop-image4.png)

    In questo esempio, una casella di testo con completamento automatico è una scelta ottimale.

-   **Gli utenti dovranno ricevere assistenza per la selezione di valori validi?** In caso affermativo, usare invece una casella di testo con un [pulsante Sfoglia](ctrl-command-buttons.md) .

    ![Screenshot di Outlook in linea e pulsante Sfoglia ](images/ctrl-drop-image5.png)

    In questo esempio, gli utenti possono fare clic su "a" per consentire la selezione di valori validi.

-   **È importante incoraggiare gli utenti a esaminare le scelte alternative o invitare le modifiche?** In tal caso, prendere in considerazione l'uso di una casella di riepilogo modificabile. Con un elenco a discesa modificabile, gli utenti non saranno in grado di riconoscere le alternative fino a quando l'elenco non viene eliminato.
-   **Gli utenti devono individuare rapidamente un elemento in un elenco di grandi dimensioni?** (Solo Win32) In tal caso, utilizzare una casella combinata perché gli utenti possono selezionare un elemento digitando il nome completo. Al contrario, l'elenco a discesa Win32 seleziona gli elementi solo in base all'ultimo carattere digitato (digitando "Jun" in un elenco di mesi corrispondente a novembre, non a giugno). In questo caso, utilizzare una casella combinata anche se le possibili scelte sono vincolate.

**Caselle di riepilogo modificabili**

-   **Le scelte possibili sono limitate?** In tal caso, usare invece un elenco a selezione singola o un elenco a discesa normale. Le caselle combinate sono per l'input non vincolato, in cui gli utenti potrebbero dover immettere un valore che non è attualmente presente nell'elenco. Poiché l'input non è vincolato, se gli utenti immettono testo non valido è necessario gestire l'errore con un messaggio di errore.
-   **È possibile enumerare le scelte più probabili in anticipo?** In caso contrario, utilizzare una casella di testo.
-   **È importante incoraggiare gli utenti a esaminare le scelte alternative o invitare le modifiche?** In caso contrario, prendere in considerazione un elenco a discesa modificabile.
-   **Si desidera attirare l'attenzione sull'opzione?** In caso contrario, prendere in considerazione un elenco a discesa modificabile. Poiché gli elenchi a discesa sono di dimensioni compatte, sono ottime scelte per le opzioni che si desidera sottoporre a sottolineatura.
-   **Lo spazio dello schermo è Premium?** In tal caso, utilizzare un elenco a discesa modificabile perché lo spazio dello schermo utilizzato è fisso e indipendente dal numero di opzioni.

Per gli elenchi a discesa, **il numero di elementi nell'elenco non rappresenta un fattore determinante per la scelta del controllo in** quanto si ridimensionano da migliaia di elementi fino a uno. L'elenco a discesa modificabile elenca la scala da migliaia di elementi a nessuna, perché gli utenti possono immettere un valore non incluso nell'elenco. Poiché è possibile utilizzare gli elenchi a discesa per i dati, il numero di elementi potrebbe non essere noto in anticipo e probabilmente non può essere garantito. **Includere sempre almeno tre elementi nelle caselle di riepilogo modificabili per giustificare lo spazio aggiuntivo dello schermo.**

## <a name="usage-patterns"></a>Modelli di utilizzo

Gli elenchi a discesa e le caselle combinate presentano diversi modelli di utilizzo:



|                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Elenco** a discesa di un elenco a discesa standard con un set fisso di valori predeterminati. <br/>                                 | Quando la chiusura è chiusa, solo l'elemento selezionato è visibile. Quando gli utenti fanno clic sul pulsante a discesa, tutte le opzioni diventano visibili. per modificare il valore, gli utenti aprono l'elenco e fanno clic su un altro valore.<br/> ![screenshot dell'elenco a discesa, opzioni nascoste ](images/ctrl-drop-image6.png)<br/> in questo esempio, l'elenco è nello stato normale.<br/> ![screenshot dell'elenco a discesa, opzioni visualizzate ](images/ctrl-drop-image7.png)<br/> In questo esempio l'elenco è stato eliminato.<br/> |
| **Elenco a discesa Anteprima elenco** a discesa che consente di visualizzare in anteprima i risultati della selezione per consentire agli utenti di scegliere.<br/>             | ![screenshot delle opzioni relative al colore e al testo ](images/ctrl-drop-image8.png)<br/> In questi esempi, gli elenchi a discesa visualizzano in anteprima i risultati della selezione.<br/>                                                                                                                                                                                                                                                                                                                                           |
| **Elenco a discesa modificabile** casella combinata a discesa, che consente agli utenti di immettere un valore che non è presente nell'elenco a discesa.<br/> | ![aa511458. dropdownlists27 (en-US, MSDN. 10). png](images/ctrl-drop-image9.png)![screenshot della casella combinata delle dimensioni del tipo di carattere modificabile ](images/ctrl-drop-image10.png)<br/> Esempi di un elenco a discesa modificabile in modalità di modifica e di eliminazione.<br/> Utilizzare questo controllo quando si desidera fornire la flessibilità di una casella di testo, ma si desidera fornire un supporto per gli utenti, fornendo un elenco pratico di scelte possibili.<br/>                                                                                                   |
| **Caselle di riepilogo modificabili** una casella combinata regolare, che consente agli utenti di immettere un valore che non si trovi nell'elenco sempre visibile. <br/> | ![screenshot dell'elenco a discesa delle opzioni relative ai tipi di carattere ](images/ctrl-drop-image11.png)<br/> In questi esempi vengono sempre visualizzate le caselle di riepilogo modificabili.<br/> Questo controllo è una scelta migliore rispetto all'elenco a discesa modificabile quando è importante incoraggiare gli utenti a esaminare le scelte alternative o invitare le modifiche.<br/>                                                                                                                                                                      |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Non usare la modifica di un elenco a discesa o di una casella combinata per**:
    -   Eseguire comandi.
    -   Visualizzare altre finestre, ad esempio una finestra di dialogo per raccogliere più input.
    -   Consente di visualizzare in modo dinamico altri controlli correlati al controllo selezionato (le utilità per la[lettura dello schermo](inter-accessibility.md) non possono rilevare tali eventi).

### <a name="presentation"></a>Presentazione

-   **Ordinare gli elementi dell'elenco in base a un ordine logico**, ad esempio raggruppando insieme le opzioni altamente correlate, inserendo prima le opzioni più comuni o utilizzando l'ordine alfabetico. Ordina i nomi in ordine alfabetico, numeri in ordine numerico e date in ordine cronologico. Gli elenchi con 12 o più elementi devono essere ordinati in ordine alfabetico per semplificare la ricerca degli elementi.

    **Corretto:** ![ screenshot dell'elenco a discesa logico ](images/ctrl-drop-image12.png)

    In questo esempio, gli elementi dell'elenco sono ordinati in base alla relazione spaziale.

    Non **corretto:** ![ screenshot dell'elenco a discesa disorganizzato](images/ctrl-drop-image13.png)

    In questo esempio sono presenti molti elementi elenco che devono essere ordinati in ordine alfabetico.

    **Corretto:** ![ screenshot dell'elenco a discesa in ordine alfabetico ](images/ctrl-drop-image14.png)

    In questo esempio, gli elementi dell'elenco vengono ordinati in ordine alfabetico, ad eccezione dell'opzione che rappresenta tutti gli elementi.

-   **Posizionare le opzioni che rappresentano tutti o nessuno all'inizio dell'elenco, indipendentemente dall'ordinamento degli elementi rimanenti.**
-   **Racchiudere le metaopzioni tra parentesi.**

    ![Screenshot che mostra un elenco a discesa con "(nessuno)" selezionato.](images/ctrl-drop-image15.png)

    In questo esempio "(nessuno)" è una meta-opzione perché non è un valore valido per la scelta, ma descrive che l'opzione stessa non è in uso.

-   **Quando si disabilita un elenco a discesa o una casella combinata, disabilitare anche le etichette e i pulsanti di comando associati.**

### <a name="drop-down-lists"></a>Elenchi a discesa

-   Quando viene utilizzato un singolo elenco a discesa per modificare la visualizzazione di un controllo associato, **modificare la visualizzazione immediatamente alla selezione anziché richiedere un pulsante di comando separato.** Utilizzare un pulsante di comando separato solo se il rendering dell'elenco richiede una quantità di tempo significativa. Tuttavia, le intestazioni di elenco e i [pulsanti di menu](ctrl-command-buttons.md) sono i controlli preferiti a questo scopo.
-   **Gli elementi dell'elenco non sono vuoti** . **usare invece le opzioni meta**. Gli utenti non sono in grado di interpretare gli elementi vuoti, mentre il significato di meta-options è esplicito.

    **Corretto:** ![ screenshot dell'elenco a discesa con nessuna selezione ](images/ctrl-drop-image16.png)

    Non **corretto:** ![ screenshot dell'elenco a discesa con vuoto selezionato](images/ctrl-drop-image17.png)

    Nell'esempio errato, il significato dell'opzione blank non è chiaro.

### <a name="preview-drop-down-lists"></a>Elenchi a discesa Anteprima

-   **Usare le anteprime negli elementi dell'elenco quando è preferibile visualizzare con le immagini rispetto a quanto descritto usando solo testo.**

    ![screenshot dell'elenco a discesa dei tipi di carattere in anteprima ](images/ctrl-drop-image18.png)

    In questo esempio, l'anteprima spiega le opzioni molto meglio del testo da solo.

-   **Non usare icone non necessarie e non Helper nelle anteprime**.

    Non **corretto:** ![ screenshot dell'elenco a discesa delle etichette con icone](images/ctrl-drop-image19.png)

    In questo esempio le icone di anteprima non sono necessarie perché non comunicano alcuna informazione.

### <a name="combo-boxes"></a>Caselle combinate

-   **Quando possibile, limitare la lunghezza del testo di input.** Se, ad esempio, l'input valido è un numero compreso tra 0 e 999, utilizzare una casella combinata limitata a tre caratteri.
-   **Se sono disponibili molte opzioni possibili, concentrare il contenuto dell'elenco sulle opzioni più probabili**. Poiché gli utenti possono immettere valori non inclusi nell'elenco, le caselle combinate non devono necessariamente elencare tutte le scelte, bensì solo le scelte possibili o un campione rappresentativo.

    ![cattura di schermata dell'elenco a discesa delle dimensioni dei caratteri ](images/ctrl-drop-image10.png)

    In questo esempio, molte scelte valide non sono elencate, ad esempio 15, o tipi di carattere a metà dimensione, ad esempio 9,5.

### <a name="default-values"></a>Valori predefiniti

-   **Selezionare il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e l'opzione più sicura per impostazione predefinita.** Se la sicurezza e la sicurezza non sono fattori, selezionare l'opzione più probabile o pratica.
    -   **Eccezione:** Visualizza un valore predefinito vuoto se il controllo rappresenta una proprietà in uno [stato misto](glossary.md), che si verifica quando si visualizza una proprietà per più oggetti che non hanno la stessa impostazione.

## <a name="prompts"></a>Prompt

Un messaggio di richiesta è un'etichetta o un'istruzione breve posizionata all'interno di un elenco a discesa modificabile come valore predefinito. A differenza del testo statico, i messaggi di richiesta scompaiono dallo schermo una volta che gli utenti digitano un elemento nella casella combinata o ottiene lo stato attivo per l'input.

![Screenshot di una casella di ricerca ](images/ctrl-drop-image20.png)

Un prompt tipico.

Usare un prompt nei casi seguenti:

-   Lo spazio dello schermo è a un livello superiore che l'uso di un'etichetta o di un'istruzione è indesiderato, ad esempio su una barra degli strumenti.
-   Il prompt è principalmente per identificare lo scopo dell'elenco in modo compatto. Non deve trattarsi di informazioni cruciali che gli utenti devono visualizzare durante l'uso della casella combinata.

Non usare i prompt solo per indirizzare gli utenti alla selezione di un elemento dall'elenco o fare clic sui pulsanti. Ad esempio, richiede come selezionare un'opzione o immettere un nome file e quindi fare clic su Invia non è necessario.

Quando si usano i prompt:

-   Creare il testo della richiesta in grigio corsivo e in testo reale nel nero normale. Il testo della richiesta non deve essere confuso con il testo reale.
-   Conserva il testo della richiesta conciso. È possibile utilizzare frammenti anziché frasi complete.
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Non usare la punteggiatura finale o i puntini di sospensione.
-   Il testo della richiesta non deve essere modificabile e dovrebbe scomparire quando gli utenti fanno clic nella casella di testo o nella scheda.
    -   **Eccezione:** Il prompt viene visualizzato se la casella di testo ha lo stato attivo per l'input predefinito e scompare solo quando l'utente inizia a digitare.
-   Il testo della richiesta viene ripristinato se la casella di testo è ancora vuota quando perde lo stato attivo per l'input.

Non **corretto:** ![ Screenshot di sei elenchi a discesa modificabili](images/ctrl-drop-image21.png)

In questo esempio lo spazio dello schermo non è Premium; una volta compilato un elenco a discesa modificabile, è difficile per gli utenti ricordare per cosa si tratta; il testo della richiesta è modificabile e viene disegnato in modo analogo al testo reale.

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![screenshot dell'elenco a discesa e delle specifiche ](images/ctrl-drop-image22.png)

Dimensionamento e spaziatura consigliati per elenchi a discesa e caselle combinate.

-   **Scegliere una larghezza appropriata per i dati più lunghi validi.** Non è possibile scorrere orizzontalmente gli elenchi a discesa, in modo che gli utenti possano visualizzare solo ciò che è visibile nel controllo. Si noti tuttavia che è possibile abilitare la funzionalità di scorrimento automatico per le caselle combinate.
-   **Includere un ulteriore 30%** (fino al 200% per un testo più breve) per qualsiasi testo (ma non per i numeri) che verrà localizzato.
-   **Scegliere una lunghezza dell'elenco che elimini lo scorrimento verticale non necessario.** Poiché gli elenchi a discesa vengono visualizzati su richiesta, gli elenchi dovrebbero visualizzare fino a 30 elementi. Le caselle di riepilogo modificabili (quelle che non dispongono di un pulsante a discesa) dovrebbero visualizzare tra 3 e 12 elementi.

## <a name="labels"></a>Etichette

**Etichette di controllo**

-   Scrivere l'etichetta come una parola o una frase, non come una frase e terminarla con i due punti. **Eccezioni**
    -   Elenchi a discesa modificabili con richieste in cui lo spazio si trova a un livello Premium.
    -   Se un elenco a discesa o una casella combinata è subordinata a un pulsante di opzione o a una casella di controllo e viene introdotta dall'etichetta che termina con i due punti, non inserire un'etichetta aggiuntiva nel controllo.
-   Assegnare una [chiave di accesso](glossary.md) univoca per ogni etichetta. Per le linee guida, vedere [tastiera](inter-keyboard.md).
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Posizionare l'etichetta a sinistra o sopra il controllo e allineare l'etichetta al bordo sinistro del controllo. Se l'etichetta è a sinistra, allineare verticalmente il testo dell'etichetta con il testo del controllo.

    **Corretto:** ![ screenshot dell'allineamento dell'etichetta dell'elenco a discesa ](images/ctrl-drop-image23.png)

    In questo esempio, l'etichetta è allineata correttamente con il testo del controllo.

    Non **corretto:** ![ screenshot dell'elenco a discesa allineato in modo errato](images/ctrl-drop-image24.png)

    In questo esempio, l'etichetta è allineata in modo non corretto con il testo del controllo.

-   È possibile specificare unità (secondi, connessioni e così via) tra parentesi dopo l'etichetta.
-   Non fare in modo che il contenuto dell'elenco a discesa o della casella combinata (o della relativa etichetta Unity) faccia parte di una frase, perché non è localizzabile.

**Testo opzione**

-   Assegnare un nome univoco a ogni opzione.
-   Usare l'uso di [maiuscole in stile frase](glossary.md), a meno che un elemento non sia un sostantivo appropriato.
-   Scrivere l'etichetta come una parola o una frase, non come una frase, e non usare la punteggiatura finale.
-   Usare il formulazione parallela e provare a rimanere la stessa lunghezza per tutte le opzioni.

**Testo istruzioni**

-   Se è necessario aggiungere testo di istruzioni su un elenco a discesa o una casella combinata, aggiungerlo sopra l'etichetta. Utilizzare frasi complete con la punteggiatura finale.
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Informazioni aggiuntive utili ma non necessarie devono essere mantenute brevi. Inserire queste informazioni tra parentesi tra l'etichetta e i due punti o senza parentesi sotto il controllo.

    ![screenshot dell'elenco a discesa con dati aggiunti ](images/ctrl-drop-image25.png)

    Questo esempio Mostra informazioni aggiuntive posizionate sotto il controllo.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento agli elenchi a discesa:

-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere il carattere di sottolineatura della chiave di accesso o due punti; includere un elenco o una casella, a seconda del valore più chiaro.
-   Per le opzioni dell'elenco, usare il testo dell'opzione esatto, inclusa la relativa maiuscola.
-   In programmazione e altri documenti tecnici, fare riferimento agli elenchi a discesa come elenchi a discesa. Altrove, usare un elenco o una casella, a seconda del valore più chiaro.
-   Per descrivere l'interazione dell'utente, utilizzare fare clic su.
-   Quando possibile, formattare le opzioni di etichetta ed elenco usando il testo in grassetto. In caso contrario, inserire l'etichetta e le opzioni tra virgolette solo se necessario per evitare confusione.

Esempio: nell'elenco **dimensioni carattere** fare clic su **tipi di carattere di grandi** dimensioni.

Quando si fa riferimento alle caselle combinate:

-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere il carattere di sottolineatura della chiave di accesso o due punti; includere la parola box.
-   Per le opzioni dell'elenco, usare il testo dell'opzione exact, inclusa la relativa maiuscola.
-   In programmazione e altri documenti tecnici, fare riferimento alle caselle combinate come caselle combinate. Altrove, usare box.
-   Per descrivere l'interazione dell'utente, usare invio.
-   Quando possibile, formattare le opzioni di etichetta ed elenco usando il testo in grassetto. In caso contrario, inserire l'etichetta e le opzioni tra virgolette solo se necessario per evitare confusione.

Esempio: nella casella **carattere** immettere il tipo di carattere che si desidera utilizzare.

 

