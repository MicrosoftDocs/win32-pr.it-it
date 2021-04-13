---
title: Caselle di riepilogo
description: Con una casella di riepilogo, gli utenti possono selezionare da un set di valori presentati in un elenco sempre visibile.
ms.assetid: 620e9ff9-b367-446b-9e97-9c9d6d14f4bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 3db0bbb07ed6cea18b7d8fb29fd4e329840590d5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351111"
---
# <a name="list-boxes"></a>Caselle di riepilogo

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con una casella di riepilogo, gli utenti possono selezionare da un set di valori presentati in un elenco sempre visibile. Con una casella di riepilogo a selezione singola, gli utenti selezionano un elemento da un elenco di valori che si escludono a vicenda. Con una casella di riepilogo a selezione multipla, gli utenti selezionano zero o più elementi da un elenco di valori.

![screenshot della casella di riepilogo a selezione singola ](images/ctrl-list-boxes-image1.png)

Casella di riepilogo tipica a selezione singola.

> [!Note]  
> Le linee guida correlate alle [visualizzazioni](ctrl-list-views.md) [layout](vis-layout.md) e elenco sono presentate in articoli distinti.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **L'elenco presenta i dati, anziché le opzioni di programma?** In entrambi i casi, una casella di riepilogo è una scelta appropriata indipendentemente dal numero di elementi. Al contrario, i [pulsanti di opzione](ctrl-radio-buttons.md) o le caselle di [controllo](ctrl-check-boxes.md) sono idonei solo per un numero ridotto di opzioni di programma.
-   **Gli utenti devono modificare le visualizzazioni, il raggruppamento, l'ordinamento in base alle colonne o modificare la larghezza e l'ordine delle colonne?** In caso affermativo, usare invece una [visualizzazione elenco](ctrl-list-views.md) .
-   **Il controllo deve essere un'origine di trascinamento o una destinazione di rilascio?** In caso affermativo, usare invece una visualizzazione elenco.
-   **Gli elementi dell'elenco devono essere copiati o incollati dagli Appunti?** In caso affermativo, usare invece una visualizzazione elenco.

**Elenchi a selezione singola**

-   **Il controllo viene usato per scegliere un'opzione da un elenco di valori che si escludono a vicenda?** Se non è così, usa un altro controllo. Per scegliere più opzioni, utilizzare un elenco di selezione multipla standard, un elenco di caselle di controllo, un generatore di elenchi o un elenco di aggiunta/rimozione.
-   **Esiste un'opzione predefinita consigliata per la maggior parte degli utenti nella maggior parte dei casi?** L'opzione selezionata è molto più importante che vedere le alternative? In tal caso, prendere in considerazione l'uso di un [elenco a discesa](/windows/desktop/uxguide/ctrl-drop) se non si vuole incoraggiare gli utenti a apportare modifiche nascondendo le alternative.

![cattura di schermata del pulsante predefinito di qualità superiore ](images/ctrl-list-boxes-image2.png)

In questo esempio, la qualità del colore più elevata è la scelta migliore per la maggior parte degli utenti, quindi un elenco a discesa rappresenta una scelta ottimale per minimizzare le alternative.

-   **L'elenco richiede un'interazione costante?** In tal caso, utilizzare un elenco a selezione singola per semplificare l'interazione.

![screenshot dell'elenco di opzioni come testo normale ](images/ctrl-list-boxes-image3.png)

In questo esempio, gli utenti cambiano costantemente l'elemento selezionato nell'elenco elementi visualizzati per impostare i colori di primo piano e di sfondo. L'uso di un elenco a discesa in questo caso sarebbe molto noioso.

-   **L'impostazione sembra come una quantità relativa? Gli utenti possono trarre vantaggio da un feedback immediato** sull'effetto delle modifiche all'impostazione? In tal caso, prendere in considerazione l'uso di un [dispositivo di scorrimento](ctrl-sliders.md) .
-   **Esiste una significativa relazione gerarchica tra gli elementi dell'elenco?** In caso affermativo, usare invece un controllo di [visualizzazione albero](ctrl-tree-views.md) .
-   **Lo spazio dello schermo è Premium?** In caso affermativo, usare invece un elenco a discesa perché lo spazio dello schermo usato è fisso e indipendente dal numero di elementi dell'elenco.

**Elenchi di selezione multipla standard e caselle di controllo**

-   **La selezione multipla è essenziale per l'attività o comunemente utilizzata?** In tal caso, usare un elenco di caselle di controllo per rendere più semplice la selezione, soprattutto se gli utenti di destinazione non sono avanzati. Molti utenti non sono consapevoli che un elenco di selezione multipla standard supporta la selezione multipla. Utilizzare un elenco di selezione multipla standard se le caselle di controllo prelevano troppe attenzioni per la selezione multipla o comportano un disordine dello schermo.
-   **La stabilità della selezione multipla è importante?** In tal caso, utilizzare un elenco di caselle di controllo, un generatore di elenchi o un elenco di aggiunta/rimozione, perché fare clic su modifica un solo elemento alla volta. Con un elenco di selezione multipla standard, è molto semplice cancellare tutte le selezioni anche per errore.
-   **Il controllo viene utilizzato per scegliere zero o più elementi da un elenco di valori?** Se non è così, usa un altro controllo. Per scegliere un elemento, usare invece un elenco a selezione singola.

**Elenchi di anteprima**

-   **Le opzioni di selezione con le immagini sono più semplici rispetto a quelle del solo testo?** In caso affermativo, usare un elenco di anteprime.

**Elencare i compilatori e aggiungere/rimuovere elenchi**

-   **Il controllo viene utilizzato per scegliere zero o più elementi da un elenco di valori?** Se non è così, usa un altro controllo. Per scegliere un elemento, usare invece un elenco a selezione singola.
-   **L'ordine degli elementi selezionati è importante?** In tal caso, il generatore di elenchi e i modelli di elenco di aggiunta/rimozione supportano l'ordine, mentre gli altri modelli a selezione multipla non lo sono.
-   **È importante per gli utenti visualizzare un riepilogo di tutti gli elementi selezionati?** In tal caso, i modelli elenco generatore e Aggiungi/Rimuovi elenco visualizzano solo gli elementi selezionati, mentre gli altri modelli a selezione multipla non lo sono.
-   **Le possibili scelte non sono vincolate?** In caso affermativo, usare un elenco di aggiunta/rimozione in modo che gli utenti possano scegliere i valori attualmente non presenti nell'elenco.
-   **L'aggiunta di un valore all'elenco richiede una finestra di dialogo specializzata per la scelta degli oggetti?** In tal caso, utilizzare un elenco Aggiungi/Rimuovi e visualizzare la finestra di dialogo quando gli utenti fanno clic su Aggiungi.
-   **Lo spazio dello schermo è Premium?** In caso affermativo, usare invece un elenco Aggiungi/Rimuovi perché usa meno spazio sullo schermo, non sempre mostrando il set di opzioni.

Per le caselle di riepilogo, **il numero di elementi nell'elenco non rappresenta un fattore determinante per la scelta del controllo in** quanto si ridimensionano da migliaia di elementi fino a uno per gli elenchi a selezione singola (e nessuno per gli elenchi a selezione multipla). Poiché è possibile usare le caselle di riepilogo per i dati, il numero di elementi potrebbe non essere noto in anticipo.

**Nota:** A volte un controllo simile a una casella di riepilogo viene implementato usando una visualizzazione elenco e viceversa. In questi casi, applicare le linee guida in base all'utilizzo, non all'implementazione.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le caselle di riepilogo includono diversi modelli di utilizzo:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Elenchi a selezione singola</strong> Consente agli utenti di selezionare un elemento alla volta. <br/></td>
<td><img src="images/ctrl-list-boxes-image4.png" alt="Screen shot of list box with one item selected " /><br/> In questo esempio, gli utenti possono selezionare un solo elemento visualizzato.<br/></td>
</tr>
<tr class="even">
<td><strong>Elenchi a selezione multipla standard</strong> Consente agli utenti di selezionare un numero qualsiasi di elementi, incluso None.<br/></td>
<td>Gli elenchi a selezione multipla standard hanno esattamente lo stesso aspetto degli elenchi a selezione singola, quindi non c'è alcun indizio visivo che una casella di riepilogo supporti la selezione multipla. Poiché gli utenti devono individuare questa possibilità, questo modello di elenco è ideale per le attività in cui la selezione multipla non è essenziale e viene utilizzata raramente. <br/> Sono disponibili due diverse modalità di selezione multipla: <a href="glossary.md">multiple</a> ed <a href="glossary.md">Extended</a>. La <strong>modalità di selezione estesa</strong> è molto più comune, in cui la selezione può essere estesa trascinando o tenendo premuto MAIUSC + clic e CTRL + clic per selezionare i gruppi di valori contigui e non adiacenti, rispettivamente. Nella <strong>modalità a selezione multipla</strong>, facendo clic su qualsiasi elemento, il relativo stato di selezione viene disattivato indipendentemente dai tasti MAIUSC e CTRL. Dato questo comportamento insolito, la modalità di selezione multipla è deprecata ed è invece consigliabile usare elenchi di caselle di controllo.<br/> <img src="images/ctrl-list-boxes-image5.png" alt="Screen shot of list box with several items selected " /><br/> In questo esempio, gli utenti possono selezionare un numero qualsiasi di elementi usando la modalità di selezione multipla.<br/></td>
</tr>
<tr class="odd">
<td><strong>Elenchi</strong> di caselle di controllo Analogamente alle caselle di riepilogo standard a selezione multipla, gli elenchi di caselle di controllo consentono agli utenti di selezionare un numero qualsiasi di elementi, incluso None.<br/></td>
<td>A differenza degli elenchi di selezione multipla standard, le caselle di controllo indicano chiaramente che è possibile selezionare più selezioni. Usare questo modello di elenco per le attività in cui la selezione multipla è essenziale o usata di frequente. <br/> <img src="images/ctrl-list-boxes-image6.png" alt="Screen shot of Toolbars check-box list " /><br/> In questo esempio gli utenti selezionano in genere più di un elemento in modo da usare un elenco di caselle di controllo.<br/> In base a questa indicazione chiara di selezione multipla, si potrebbe presupporre che gli elenchi di caselle di controllo siano preferibili agli elenchi a selezione multipla standard. In pratica, per alcune attività è richiesta la selezione multipla o l'utilizzo intensivo. l'uso di un elenco di caselle di controllo in questi casi consente di attirare troppe attenzioni sulla selezione. Di conseguenza, gli <strong>elenchi a selezione multipla standard sono molto più comuni.</strong><br/></td>
</tr>
<tr class="even">
<td><strong>Elenchi di anteprima</strong> Può essere una selezione singola o multipla, ma Visualizza un'anteprima dell'effetto della selezione anziché solo del testo.<br/></td>
<td><img src="images/ctrl-list-boxes-image7.png" alt="Screen shot of Window Color options preview " /><br/> In questo esempio, un'anteprima di ogni opzione Mostra chiaramente l'effetto della scelta, che risulta più efficace rispetto all'uso del solo testo.<br/></td>
</tr>
<tr class="odd">
<td><strong>Elenca generatori</strong> Consente agli utenti di creare un elenco di scelte aggiungendo un elemento alla volta e impostando facoltativamente l'ordine dell'elenco.<br/></td>
<td>Un generatore di elenchi è costituito da due elenchi a selezione singola: l'elenco a sinistra è un set fisso di opzioni e l'elenco a destra è l'elenco da compilare. Tra gli elenchi sono presenti due pulsanti di comando: <br/>
<ul>
<li>Pulsante <strong>Aggiungi</strong> che sposta l'opzione attualmente selezionata nell'elenco compilato, inserito prima dell'elemento selezionato. (Fare doppio clic su un elemento di opzione ha lo stesso effetto).</li>
<li>Pulsante <strong>Rimuovi</strong> che rimuove l'elemento selezionato dall'elenco compilato e lo restituisce all'elenco di opzioni. (Facendo doppio clic su un elemento nell'elenco compilato si ha lo stesso effetto). L'elenco compilato può facoltativamente avere i comandi <strong>Sposta su</strong> e <strong>Sposta giù</strong> per ordinare gli elementi dell'elenco.</li>
</ul>
<img src="images/ctrl-list-boxes-image8.png" alt="Screen shot of Toolbar buttons list builder " /><br/> In questo esempio viene usato un generatore di elenchi per creare una barra degli strumenti selezionando gli elementi da un set di opzioni disponibili e impostando l'ordine.<br/></td>
</tr>
<tr class="even">
<td><strong>Aggiungi/Rimuovi elenchi</strong> Consente agli utenti di creare un elenco di scelte aggiungendo uno o più elementi alla volta e impostando facoltativamente l'ordine degli elenchi, ad esempio i generatori di elenchi.<br/></td>
<td>A differenza di un generatore di elenchi, fare clic su <strong>Aggiungi</strong> per visualizzare una finestra di dialogo che consente di selezionare gli elementi da aggiungere all'elenco. L'utilizzo di una finestra di dialogo separata consente una notevole flessibilità nella scelta degli elementi, è possibile utilizzare un selettore di oggetti specializzato o persino una finestra di dialogo comune. Rispetto al generatore di elenchi, questa variazione è più compatta ma richiede un po' più di impegno per l'aggiunta di elementi. <br/> <img src="images/ctrl-list-boxes-image9.png" alt="Screen shot of Menu contents list " /><br/> In questo esempio gli utenti possono aggiungere o rimuovere strumenti da un menu, nonché impostare l'ordine.<br/> Sebbene il generatore di elenchi e i modelli di elenco di aggiunta/rimozione siano significativamente più pesanti degli altri elenchi a selezione multipla, offrono due vantaggi esclusivi:<br/>
<ul>
<li>Gli utenti hanno il controllo sull'ordine degli elenchi, sia durante la compilazione dell'elenco che dopo.</li>
<li>Gli utenti possono esaminare un riepilogo degli elementi selezionati, il che può costituire un vantaggio significativo se il numero di scelte è elevato.</li>
</ul>
Gli svantaggi sono che richiedono molto più spazio sullo schermo e possono essere difficili da usare quando si crea un elenco di elementi di grandi dimensioni da zero. Di conseguenza, vengono usati meglio per creare elenchi brevi o modificare gli elenchi già esistenti.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Indicazioni

### <a name="presentation"></a>Presentazione

-   **Ordinare gli elementi dell'elenco in un ordine logico,** ad esempio raggruppando le opzioni correlate, inserendo prima gli elementi utilizzati più di frequente o utilizzando l'ordine alfabetico. Ordina i nomi in ordine alfabetico, numeri in ordine numerico e date in ordine cronologico. Gli elenchi con 12 o più elementi devono essere ordinati in ordine alfabetico per semplificare la ricerca degli elementi.

**Corretto:** ![ screenshot dell'allineamento (a sinistra, al centro, a destra) ](images/ctrl-list-boxes-image10.png)

In questo esempio gli elementi della casella di riepilogo vengono ordinati in base alla relazione spaziale.

Non **corretto:** ![ screenshot dell'elenco disorganizzato](images/ctrl-list-boxes-image11.png)

In questo esempio sono presenti molti elementi elenco che devono essere ordinati in ordine alfabetico.

**Corretto:** ![ screenshot dell'elenco in ordine alfabetico ](images/ctrl-list-boxes-image12.png)

In questo esempio, gli elementi dell'elenco sono più facili da trovare perché sono ordinati in ordine alfabetico. Tuttavia, l'elemento "tutti i prodotti Windows" si trova all'inizio dell'elenco, indipendentemente dal relativo ordinamento.

-   **Posizionare le opzioni che rappresentano tutti o nessuno all'inizio dell'elenco**, indipendentemente dall'ordinamento degli elementi rimanenti.
-   **Racchiudere le metaopzioni tra parentesi.**

![screenshot dell'elenco a discesa con nessuna selezione ](images/ctrl-list-boxes-image13.png)

In questo esempio "(nessuno)" è una meta-opzione perché non è un valore valido per la scelta, ma indica che l'opzione stessa non è in uso.

-   **Gli elementi dell'elenco non sono vuoti. usare invece le opzioni meta.** Gli utenti non sono in grado di interpretare gli elementi vuoti, mentre il significato di meta-options è esplicito.

Non **corretto:** ![ screenshot dell'elenco a discesa con vuoto selezionato](images/ctrl-list-boxes-image14.png)

In questo esempio, il significato dell'elemento vuoto non è chiaro.

**Corretto:** ![ screenshot dell'elenco a discesa con nessuna selezione ](images/ctrl-list-boxes-image13.png)

In questo esempio viene invece usata la meta-opzione "(None)".

### <a name="interaction"></a>Interazione

-   **Si consiglia di fornire un comportamento di doppio clic.** Il doppio clic dovrebbe avere lo stesso effetto della selezione di un elemento e dell'esecuzione del comando predefinito.
-   **Rendere ridondante il comportamento di doppio clic.** Deve essere sempre presente un pulsante di comando o un comando del menu di scelta rapida con lo stesso effetto.
-   **Se gli utenti non possono eseguire alcuna operazione con gli elementi selezionati, non consentire la selezione.**

**Corretto:** ![ cattura di schermata dell'elenco delle modifiche della procedura guidata completata ](images/ctrl-list-boxes-image15.png)

In questa casella di riepilogo viene visualizzato un elenco di sola lettura delle modifiche. non è necessario selezionare.

-   **Quando si disabilita una casella di riepilogo, disabilitare anche le etichette e i pulsanti di comando associati.**
-   **Non usare la modifica dell'elemento selezionato in una casella di riepilogo per:**
    -   Eseguire comandi.
    -   Visualizzare altre finestre, ad esempio una finestra di dialogo per raccogliere più input.
    -   Consente di visualizzare in modo dinamico altri controlli correlati al controllo selezionato (le utilità per la lettura dello schermo non possono rilevare tali eventi). **Eccezione:** È possibile modificare dinamicamente il testo statico utilizzato per descrivere l'elemento selezionato.

**Accettabile:** ![ cattura di schermata dei dettagli dell'elemento elenco selezionato ](images/ctrl-list-boxes-image16.png)

In questo esempio, la modifica dell'elemento selezionato cambia la descrizione.

-   **Evitare lo scorrimento orizzontale.** Gli elenchi a più colonne si basano sullo scorrimento orizzontale, che in genere è più difficile da usare rispetto allo scorrimento verticale. Gli elenchi a più colonne che richiedono lo scorrimento orizzontale possono essere usati quando sono presenti molti elementi ordinati in ordine alfabetico e uno spazio su schermo sufficiente per un controllo esteso.

**Accettabile:** ![ screenshot dell'elenco di cartelle in Esplora risorse ](images/ctrl-list-boxes-image17.png)

In questo esempio vengono usate più colonne che richiedono lo scorrimento orizzontale perché sono presenti molti elementi e una grande quantità di spazio sullo schermo disponibile per un controllo esteso.

### <a name="multiple-selection-lists"></a>Elenchi a selezione multipla

-   Si **consiglia di visualizzare il numero di elementi selezionati al di sotto dell'elenco,** soprattutto se gli utenti hanno la possibilità di selezionare più elementi. Queste informazioni non solo forniscono utili commenti, ma indica chiaramente che la casella di riepilogo supporta la selezione multipla.

![screenshot della casella di riepilogo con quattro elementi selezionati ](images/ctrl-list-boxes-image5.png)

In questo esempio, il numero di elementi selezionati viene visualizzato sotto l'elenco.

-   È possibile fornire altre metriche di selezione che potrebbero essere più significative, ad esempio le risorse necessarie per le selezioni.

![screenshot dell'elenco di caselle di controllo delle funzionalità di Windows ](images/ctrl-list-boxes-image18.png)

In questo esempio, lo spazio su disco necessario per installare i componenti è più significativo rispetto al numero di elementi selezionati.

-   Se sono presenti potenzialmente molti elementi elenco e la selezione o la cancellazione di tutti gli elementi è probabile, aggiungere tutti i pulsanti di comando Seleziona tutto e cancella tutti.
-   Per gli elenchi di selezione multipla standard, non usare la modalità di selezione multipla perché questa modalità di selezione è stata deprecata. Per un comportamento equivalente, usare invece un elenco di caselle di controllo.

### <a name="default-values"></a>Valori predefiniti

-   **Selezionare il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e l'opzione più sicura per impostazione predefinita.** Se la sicurezza e la sicurezza non sono fattori, selezionare l'opzione più probabile o pratica.

**Eccezione:** Non selezionare elementi se il controllo rappresenta una proprietà in uno [stato misto](glossary.md), che si verifica quando si visualizza una proprietà per più oggetti che non hanno la stessa impostazione.

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![screenshot del ridimensionamento e della spaziatura della casella di riepilogo ](images/ctrl-list-boxes-image19.png)

Ridimensionamento e spaziatura consigliati per le caselle di riepilogo.

-   **Scegliere una larghezza della casella di riepilogo appropriata per i dati più lunghi validi.** Non è possibile scorrere orizzontalmente le caselle di riepilogo standard, in modo che gli utenti possano visualizzare solo ciò che è visibile nel controllo.
-   **Includere un ulteriore 30%** (fino al 200% per un testo più breve) per qualsiasi testo (ma non per i numeri) che verrà localizzato.
-   **Scegliere l'altezza di una casella di riepilogo che visualizza un numero integrale di elementi.** Evitare di troncare verticalmente gli elementi.
-   **Scegliere l'altezza di una casella di riepilogo che elimini lo scorrimento verticale non necessario.** Le caselle di riepilogo dovrebbero visualizzare tra 3 e 20 elementi senza dover scorrere. Se si elimina la barra di scorrimento verticale, provare a creare una casella di riepilogo leggermente più a lungo. Gli elenchi con un numero potenzialmente elevato di elementi devono visualizzare almeno cinque elementi per facilitare lo scorrimento mostrando più elementi alla volta e rendendo la barra di scorrimento più semplice da posizionare.
-   **Se gli utenti traggono vantaggio da una maggiore quantità di casella di riepilogo, rendere ridimensionabili la casella di riepilogo e la finestra padre.** Questa operazione consente agli utenti di modificare le dimensioni della casella di riepilogo in base alle esigenze. Tuttavia, le caselle di riepilogo ridimensionabili non devono visualizzare meno di tre elementi.

## <a name="labels"></a>Etichette

**Etichette di controllo**

-   Tutte le caselle di riepilogo necessitano di etichette. Scrivere l'etichetta come una parola o una frase, non come una frase; usare i due punti alla fine dell'etichetta.

**Eccezione:** Omettere l'etichetta se si tratta semplicemente di una ripubblicazione dell' [istruzione principale](glossary.md)di una finestra di dialogo. In questo caso, l'istruzione principale accetta i due punti, a meno che non si tratti di una domanda, e la chiave di accesso.

**Accettabile:** ![ screenshot dell'elenco con etichetta ridondante ](images/ctrl-list-boxes-image20.png)

In questo esempio, l'etichetta della casella di riepilogo ridichiara semplicemente l'istruzione principale.

**Migliore:** ![ screenshot dell'elenco di senza etichetta ridondante ](images/ctrl-list-boxes-image21.png)

In questo esempio, l'etichetta ridondante viene rimossa, quindi l'istruzione principale accetta i due punti e la chiave di accesso.

-   Se una casella di riepilogo è subordinata a un pulsante di opzione o a una casella di controllo e viene introdotta dall'etichetta del controllo che termina con i due punti, non inserire un'etichetta aggiuntiva nel controllo casella di riepilogo.

![Screenshot di Button ed elenco con la stessa etichetta ](images/ctrl-list-boxes-image22.png)

In questo esempio, la casella di riepilogo è subordinata a un pulsante di opzione e condivide l'etichetta.

-   Assegnare una [chiave di accesso](glossary.md)univoca. Per le linee guida, vedere [tastiera](inter-keyboard.md).
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Posizionare l'etichetta a sinistra o sopra il controllo e allineare l'etichetta al bordo sinistro del controllo.
    -   Se l'etichetta è a sinistra, allineare verticalmente il testo dell'etichetta con la prima riga di testo nel controllo.

**Corretto:** ![ screenshot dell'elenco con etichetta allineata a sinistra sopra ](images/ctrl-list-boxes-image23.png)![ la schermata dell'elenco con etichetta allineata al testo a sinistra ](images/ctrl-list-boxes-image24.png)

In questi esempi, l'etichetta nella parte superiore è allineata al bordo sinistro della casella di riepilogo e l'etichetta a sinistra viene allineata al testo nella casella di riepilogo.

Non **corretto:** ![ cattura di schermata dell'elenco con etichetta allineata al testo sopra l'immagine ](images/ctrl-list-boxes-image25.png)![ dell'elenco con l'etichetta allineata in alto a sinistra](images/ctrl-list-boxes-image26.png)

In questi esempi non corretti, l'etichetta nella parte superiore viene allineata al testo nella casella di riepilogo e l'etichetta a sinistra viene allineata alla parte superiore della casella di riepilogo.

-   Per le caselle di riepilogo a selezione multipla, usare un'etichetta che indichi chiaramente che è possibile selezionare più selezioni. Le etichette dell'elenco di caselle di controllo possono essere meno esplicite.

**Corretto:** ![ screenshot dell'elenco con selezionare una o più etichette ](images/ctrl-list-boxes-image27.png)

In questo esempio, l'etichetta indica chiaramente che è possibile selezionare più selezioni.

Non **corretto:** ![ screenshot della casella di riepilogo con etichetta componenti aggiuntivi](images/ctrl-list-boxes-image28.png)

In questo esempio, l'etichetta non fornisce informazioni evidenti sulla selezione multipla.

**Migliore:** ![ screenshot dell'elenco di caselle di controllo con etichetta componenti aggiuntivi ](images/ctrl-list-boxes-image29.png)

In questo esempio, le caselle di controllo indicano chiaramente che è possibile selezionare più selezioni, quindi l'etichetta non deve essere esplicita.

-   È possibile specificare unità (secondi, connessioni e così via) tra parentesi dopo l'etichetta.

**Testo opzione**

-   Assegnare un nome univoco a ogni opzione.
-   Usare l'uso di [maiuscole in stile frase](glossary.md), a meno che un elemento non sia un sostantivo appropriato.
-   Scrivere l'etichetta come una parola o una frase, non come una frase, e non usare la punteggiatura finale.
-   Usare il formulazione parallela e provare a rimanere la stessa lunghezza per tutte le opzioni.

**Testo informativo e supplementare**

-   Se è necessario aggiungere testo di istruzioni su una casella di riepilogo, aggiungerla sopra l'etichetta. Utilizzare frasi complete con la punteggiatura finale.
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Informazioni aggiuntive utili ma non necessarie devono essere mantenute brevi. Inserire questo testo tra parentesi tra l'etichetta e i due punti o senza parentesi sotto il controllo.

![screenshot dell'elenco di caselle di controllo e del testo descrittivo ](images/ctrl-list-boxes-image30.png)

In questo esempio, il testo supplementare viene inserito sotto l'elenco.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle caselle di riepilogo:

-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere il carattere di sottolineatura della chiave di accesso o i due punti. Includere l'elenco di parole. Non fare riferimento a una casella di riepilogo come casella di riepilogo o campo.
-   Per gli elementi dell'elenco, usare il testo esatto dell'elemento, inclusa la relativa maiuscola.
-   In programmazione e altri documenti tecnici, fare riferimento alle caselle di riepilogo come caselle di riepilogo. Ovunque, usare l'elenco.
-   Per descrivere l'interazione dell'utente, usare SELECT.
-   Quando possibile, formattare l'etichetta ed elencare gli elementi usando il testo in grassetto. In caso contrario, inserire l'etichetta e gli elementi tra virgolette solo se necessario per evitare confusione.

Esempio: nell'elenco **Vai all'** elenco selezionare un **segnalibro**.

