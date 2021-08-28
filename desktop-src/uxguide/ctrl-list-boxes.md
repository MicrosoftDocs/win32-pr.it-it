---
title: Caselle di riepilogo
description: Con una casella di riepilogo, gli utenti possono selezionare da un set di valori presentati in un elenco sempre visibile.
ms.assetid: 620e9ff9-b367-446b-9e97-9c9d6d14f4bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0f1fe5a0c804e1c0b5b2636b4c7747caa9fb1049
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986904"
---
# <a name="list-boxes"></a>Caselle di riepilogo

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con una casella di riepilogo, gli utenti possono selezionare da un set di valori presentati in un elenco sempre visibile. Con una casella di riepilogo a selezione singola, gli utenti selezionano un elemento da un elenco di valori che si escludono a vicenda. Con una casella di riepilogo a selezione multipla, gli utenti selezionano zero o più elementi da un elenco di valori.

![Screenshot della casella di riepilogo a selezione singola ](images/ctrl-list-boxes-image1.png)

Casella di riepilogo a selezione singola tipica.

> [!Note]  
> Le linee guida relative [alle visualizzazioni](vis-layout.md) [layout ed](ctrl-list-views.md) elenco sono presentate in articoli separati.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **L'elenco presenta i dati anziché le opzioni del programma?** In entrambi i modi, una casella di riepilogo è una scelta appropriata indipendentemente dal numero di elementi. Al contrario, i [pulsanti di opzione](ctrl-radio-buttons.md) o le [caselle di](ctrl-check-boxes.md) controllo sono adatti solo per un numero ridotto di opzioni di programma.
-   **Gli utenti devono modificare le visualizzazioni, raggruppare, ordinare in base alle colonne o modificare la larghezza e l'ordine delle colonne?** In tal caso, usare [invece una visualizzazione](ctrl-list-views.md) elenco.
-   **Il controllo deve essere un'origine di trascinamento o un obiettivo di rilascio?** In tal caso, usare invece una visualizzazione elenco.
-   **Gli elementi dell'elenco devono essere copiati o incollati dagli Appunti?** In tal caso, usare invece una visualizzazione elenco.

**Elenchi a selezione singola**

-   **Il controllo viene usato per scegliere un'opzione da un elenco di valori che si escludono a vicenda?** Se non è così, usa un altro controllo. Per scegliere più opzioni, usare invece un elenco a selezione multipla standard, un elenco di caselle di controllo, un generatore di elenchi o un elenco di aggiunta/rimozione.
-   **Esiste un'opzione predefinita consigliata per la maggior parte degli utenti nella maggior parte delle situazioni?** L'opzione selezionata è molto più importante rispetto alle alternative? In tal caso, è consigliabile usare un elenco [a](/windows/desktop/uxguide/ctrl-drop) discesa se non si vuole incoraggiare gli utenti a apportare modifiche nascondendo le alternative.

![Schermata con la massima qualità come pulsante predefinito ](images/ctrl-list-boxes-image2.png)

In questo esempio, la qualità del colore più elevata è la scelta migliore per la maggior parte degli utenti, quindi un elenco a discesa è una buona scelta per eseguire il downplay delle alternative.

-   **L'elenco richiede un'interazione costante?** In tal caso, usare un elenco a selezione singola per semplificare l'interazione.

![Screenshot dell'elenco di opzioni, ad esempio testo normale ](images/ctrl-list-boxes-image3.png)

In questo esempio gli utenti modificano costantemente l'elemento selezionato nell'elenco Elementi visualizzati per impostare i colori di primo piano e di sfondo. L'uso di un elenco a discesa in questo caso sarebbe molto noioso.

-   **L'impostazione sembra una quantità relativa? Gli utenti possono trarre vantaggio da commenti e suggerimenti immediati** sull'effetto delle modifiche delle impostazioni? In tal caso, è consigliabile usare invece [un dispositivo di](ctrl-sliders.md) scorrimento.
-   **Esiste una relazione gerarchica significativa tra gli elementi dell'elenco?** In tal caso, usare [invece un controllo di visualizzazione](ctrl-tree-views.md) albero.
-   **Lo spazio sullo schermo è premium?** In tal caso, usare invece un elenco a discesa perché lo spazio sullo schermo usato è fisso e indipendente dal numero di elementi dell'elenco.

**Elenchi standard a selezione multipla ed elenchi di caselle di controllo**

-   **La selezione multipla è essenziale per l'attività o viene comunemente usata?** In tal caso, usare un elenco di caselle di controllo per rendere più ovvie le selezioni, soprattutto se gli utenti di destinazione non sono avanzati. Molti utenti non si renderanno conto che un elenco a selezione multipla standard supporta la selezione multipla. Usare un elenco a selezione multipla standard se le caselle di controllo richiamano troppo attenzione a più selezioni o causano un'ingombro dello schermo.
-   **La stabilità della selezione multipla è importante?** In tal caso, usare un elenco di caselle di controllo, un generatore di elenchi o un elenco di aggiunta/rimozione perché facendo clic su viene modificato un solo elemento alla volta. Con un elenco di selezione multipla standard, è molto facile cancellare tutte le selezioni anche per errore.
-   **Il controllo viene usato per scegliere zero o più elementi da un elenco di valori?** Se non è così, usa un altro controllo. Per scegliere un elemento, usare invece un elenco a selezione singola.

**Elenchi di anteprima**

-   **Le opzioni sono più semplici da selezionare con le immagini rispetto al solo testo?** In tal caso, usare un elenco di anteprima.

**Generatori di elenchi ed elenchi di aggiunta/rimozione**

-   **Il controllo viene usato per scegliere zero o più elementi da un elenco di valori?** Se non è così, usa un altro controllo. Per scegliere un elemento, usare invece un elenco a selezione singola.
-   **L'ordine degli elementi selezionati è importante?** In tal caso, il generatore di elenchi e i modelli di elenco di aggiunta/rimozione supportano l'ordine, mentre gli altri criteri di selezione multipla non lo supportano.
-   **È importante che gli utenti vedano un riepilogo di tutti gli elementi selezionati?** In questo caso, il generatore di elenchi e i modelli di elenco di aggiunta/rimozione visualizzano solo gli elementi selezionati, mentre gli altri criteri di selezione multipla non lo visualizzano.
-   **Le scelte possibili sono senza vincoli?** In tal caso, usare un elenco di aggiunta/rimozione in modo che gli utenti possano scegliere i valori attualmente non presenti nell'elenco.
-   **L'aggiunta di un valore all'elenco richiede una finestra di dialogo specializzata per la scelta degli oggetti?** In tal caso, usare un elenco di aggiunta/rimozione e visualizzare la finestra di dialogo quando gli utenti fa clic su Aggiungi.
-   **Lo spazio sullo schermo è premium?** In tal caso, usare invece un elenco di aggiunta/rimozione perché usa meno spazio sullo schermo non visualizzando sempre il set di opzioni.

Per le caselle di riepilogo, il numero di elementi **nell'elenco** non è un fattore determinante nella scelta del controllo perché vengono ridimensionati da migliaia di elementi fino a uno per gli elenchi a selezione singola (e nessuno per gli elenchi a selezione multipla). Poiché le caselle di riepilogo possono essere utilizzate per i dati, il numero di elementi potrebbe non essere noto in anticipo.

**Nota:** In alcuni casi un controllo simile a una casella di riepilogo viene implementato usando una visualizzazione elenco e viceversa. In questi casi, applicare le linee guida in base all'utilizzo, non all'implementazione.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le caselle di riepilogo hanno diversi modelli di utilizzo:




| Etichetta | Valore |
|--------|-------|
| <strong>Elenchi a selezione singola</strong> Consente agli utenti di selezionare un elemento alla volta. <br /> | <img src="images/ctrl-list-boxes-image4.png" alt="Screen shot of list box with one item selected " /><br /> In questo esempio gli utenti possono selezionare un solo elemento visualizzato.<br /> | 
| <strong>Elenchi a selezione multipla standard</strong> Consente agli utenti di selezionare un numero qualsiasi di elementi, incluso nessuno.<br /> | Gli elenchi a selezione multipla standard hanno esattamente lo stesso aspetto degli elenchi a selezione singola, quindi non esiste alcuna indicazione visiva che una casella di riepilogo supporti la selezione multipla. Poiché gli utenti devono individuare questa possibilità, questo modello di elenco è ideale per le attività in cui la selezione multipla non è essenziale e viene usata raramente. <br /> Esistono due diverse modalità di selezione multipla: <a href="glossary.md">multiple</a> ed <a href="glossary.md">estese.</a> <strong>La modalità</strong> di selezione estesa è di gran lunga la più comune, in cui la selezione può essere estesa trascinando o premendo MAIUSC+clic e CTRL+clic per selezionare rispettivamente gruppi di valori contigui e non adiacenti. In modalità <strong>a selezione multipla, facendo</strong>clic su un elemento viene attivato o disattivato lo stato di selezione indipendentemente dai tasti MAIUSC e CTRL. Dato questo comportamento insolito, la modalità di selezione multipla è deprecata ed è consigliabile usare invece elenchi di caselle di controllo.<br /><img src="images/ctrl-list-boxes-image5.png" alt="Screen shot of list box with several items selected " /><br /> In questo esempio gli utenti possono selezionare un numero qualsiasi di elementi usando la modalità di selezione multipla.<br /> | 
| <strong>Elenchi di caselle di controllo</strong> Analogamente alle caselle di riepilogo a selezione multipla standard, gli elenchi di caselle di controllo consentono agli utenti di selezionare un numero qualsiasi di elementi, incluso nessuno.<br /> | A differenza degli elenchi di selezione multipla standard, le caselle di controllo indicano chiaramente che è possibile selezionare più elementi. Usare questo modello di elenco per le attività in cui la selezione multipla è essenziale o di uso comune. <br /><img src="images/ctrl-list-boxes-image6.png" alt="Screen shot of Toolbars check-box list " /><br /> In questo esempio gli utenti selezionano in genere più di un elemento, quindi viene usato un elenco di caselle di controllo.<br /> Data questa chiara indicazione di selezione multipla, si potrebbe presupporre che gli elenchi di caselle di controllo siano preferibili agli elenchi a selezione multipla standard. In pratica, alcune attività richiedono una selezione multipla o la usano molto spesso. L'utilizzo di un elenco di caselle di controllo in questi casi richiama un'attenzione troppo particolare alla selezione. Di conseguenza, <strong>gli elenchi a selezione multipla standard sono molto più comuni.</strong><br /> | 
| <strong>Elenchi di anteprima</strong> Può essere una o più selezioni, ma visualizzano un'anteprima dell'effetto della selezione anziché solo il testo.<br /> | <img src="images/ctrl-list-boxes-image7.png" alt="Screen shot of Window Color options preview " /><br /> In questo esempio, un'anteprima di ogni opzione mostra chiaramente l'effetto della scelta, che è più efficace rispetto all'uso del solo testo.<br /> | 
| <strong>Generatori di elenchi</strong> Consentire agli utenti di creare un elenco di scelte aggiungendo un elemento alla volta e, facoltativamente, impostando l'ordine dell'elenco.<br /> | Un generatore di elenchi è costituito da due elenchi a selezione singola: l'elenco a sinistra è un set fisso di opzioni e l'elenco a destra è l'elenco in fase di creazione. Sono disponibili due pulsanti di comando tra gli elenchi: <br /><ul><li>Pulsante <strong>Aggiungi</strong> che sposta l'opzione attualmente selezionata nell'elenco compilato, inserito prima dell'elemento selezionato. Fare doppio clic su un elemento opzione ha lo stesso effetto.</li><li>Pulsante <strong>Rimuovi</strong> che rimuove l'elemento selezionato dall'elenco compilato e lo restituisce all'elenco di opzioni. Fare doppio clic su un elemento nell'elenco compilato ha lo stesso effetto. L'elenco compilato può facoltativamente avere <strong>i comandi Sposta su</strong> e Sposta <strong>giù</strong> per ordinare gli elementi dell'elenco.</li></ul><img src="images/ctrl-list-boxes-image8.png" alt="Screen shot of Toolbar buttons list builder " /><br /> In questo esempio viene usato un generatore di elenchi per creare una barra degli strumenti selezionando gli elementi da un set di opzioni disponibili e impostando il relativo ordine.<br /> | 
| <strong>Aggiungere/rimuovere elenchi</strong> Consentire agli utenti di creare un elenco di scelte aggiungendo uno o più elementi alla volta e, facoltativamente, impostando l'ordine dell'elenco(ad esempio, i generatori di elenchi).<br /> | A differenza di un generatore di elenchi, facendo <strong>clic</strong> su Aggiungi viene visualizzata una finestra di dialogo per selezionare gli elementi da aggiungere all'elenco. L'uso di una finestra di dialogo separata offre una notevole flessibilità nella scelta degli elementi ed è possibile usare un selettore di oggetti specializzato o anche una finestra di dialogo comune. Rispetto al generatore di elenchi, questa variazione è più compatta, ma richiede un po' più di impegno per l'aggiunta di elementi. <br /><img src="images/ctrl-list-boxes-image9.png" alt="Screen shot of Menu contents list " /><br /> In questo esempio gli utenti possono aggiungere o rimuovere strumenti da un menu, nonché impostare l'ordine.<br /> Anche se i modelli di generatore di elenchi e di aggiunta/rimozione di elenchi sono notevolmente più pesanti rispetto agli altri elenchi a selezione multipla, offrono due vantaggi univoci:<br /><ul><li>Gli utenti hanno il controllo sull'ordine dell'elenco, sia durante la compilazione dell'elenco che dopo.</li><li>Gli utenti possono esaminare un riepilogo degli elementi selezionati, che può essere un vantaggio significativo se il numero di scelte è elevato.</li></ul>Gli svantaggi sono che richiedono molto più spazio sullo schermo e possono essere difficili da usare quando si crea un elenco di elementi di grandi dimensioni da zero. Di conseguenza, sono più usati per creare elenchi brevi o modificare elenchi già esistenti.<br /> | 




 

## <a name="guidelines"></a>Indicazioni

### <a name="presentation"></a>Presentazione

-   **Ordinare gli elementi dell'elenco in** ordine logico, ad esempio raggruppando le opzioni correlate, inserendo prima gli elementi usati più di frequente o usando l'ordine alfabetico. Ordinare i nomi in ordine alfabetico, i numeri in ordine numerico e le date in ordine cronologico. Gli elenchi con 12 o più elementi devono essere ordinati alfabeticamente per semplificare la ricerca degli elementi.

**Risposta corretta:** ![ Screenshot dell'allineamento (a sinistra, al centro, a destra) ](images/ctrl-list-boxes-image10.png)

In questo esempio gli elementi della casella di riepilogo vengono ordinati in base alla relazione spaziale.

**Risposta errata:** ![ Screenshot dell'elenco disorganizzato ](images/ctrl-list-boxes-image11.png)

In questo esempio sono presenti così tanti elementi dell'elenco che devono essere ordinati in ordine alfabetico.

**Risposta corretta:** ![ Screenshot dell'elenco in ordine alfabetico ](images/ctrl-list-boxes-image12.png)

In questo esempio, gli elementi dell'elenco sono più facili da trovare perché sono ordinati in ordine alfabetico. Tuttavia, l'elemento "All Windows products" si trova all'inizio dell'elenco, indipendentemente dal tipo di ordinamento.

-   **Posizionare le opzioni che rappresentano All o None all'inizio** dell'elenco, indipendentemente dall'ordinamento degli elementi rimanenti.
-   **Racchiudere le meta-opzioni tra parentesi.**

![Screenshot dell'elenco a discesa con nessuno selezionato ](images/ctrl-list-boxes-image13.png)

In questo esempio "(none)" è una meta-opzione perché non è un valore valido per la scelta, ma indica che l'opzione stessa non viene usata.

-   **Gli elementi elenco vuoti non usano invece le meta-opzioni.** Gli utenti non sanno come interpretare gli elementi vuoti, mentre il significato delle meta-opzioni è esplicito.

**Risposta errata:** ![ Screenshot dell'elenco a discesa con vuoto selezionato ](images/ctrl-list-boxes-image14.png)

In questo esempio il significato dell'elemento vuoto non è chiaro.

**Risposta corretta:** ![ Screenshot dell'elenco a discesa con nessuno selezionato ](images/ctrl-list-boxes-image13.png)

In questo esempio viene invece usata la meta-opzione "(none)".

### <a name="interaction"></a>Interazione

-   **Valutare la possibilità di fornire il comportamento del doppio clic.** Fare doppio clic dovrebbe avere lo stesso effetto della selezione di un elemento e dell'esecuzione del comando predefinito.
-   **Rendere ridondante il comportamento del doppio clic.** Deve essere sempre presente un pulsante di comando o un comando di menu di scelta rapida che ha lo stesso effetto.
-   **Se gli utenti non possono eseguire alcun'operazione con gli elementi selezionati, non consentire la selezione.**

**Risposta corretta:** ![ Screenshot dell'elenco delle modifiche della procedura guidata completate ](images/ctrl-list-boxes-image15.png)

In questa casella di riepilogo viene visualizzato un elenco di sola lettura delle modifiche. non è necessaria la selezione.

-   **Quando si disabilita una casella di riepilogo, disabilitare anche le etichette e i pulsanti di comando associati.**
-   **Non usare la modifica dell'elemento selezionato in una casella di riepilogo per:**
    -   Eseguire comandi.
    -   Visualizzare altre finestre, ad esempio una finestra di dialogo per raccogliere più input.
    -   Visualizza in modo dinamico altri controlli correlati al controllo selezionato (le utilità per la lettura dello schermo non sono in grado di rilevare tali eventi). **Eccezione:** È possibile modificare dinamicamente il testo statico usato per descrivere l'elemento selezionato.

**Accettabile:** ![ Screenshot dei dettagli dell'elemento dell'elenco selezionato ](images/ctrl-list-boxes-image16.png)

In questo esempio la modifica dell'elemento selezionato modifica la descrizione.

-   **Evitare lo scorrimento orizzontale.** Gli elenchi a più colonne si basano sullo scorrimento orizzontale, che in genere è più difficile da usare rispetto a quello verticale. Gli elenchi a più colonne che richiedono lo scorrimento orizzontale possono essere usati quando si dispone di molti elementi ordinati alfabeticamente e di spazio sullo schermo sufficiente per un controllo wide.

**Accettabile:** ![ Screenshot dell'elenco di cartelle in Esplora risorse ](images/ctrl-list-boxes-image17.png)

In questo esempio vengono usate più colonne che richiedono lo scorrimento orizzontale perché sono presenti molti elementi e molto spazio disponibile sullo schermo per un controllo wide.

### <a name="multiple-selection-lists"></a>Elenchi a selezione multipla

-   **È consigliabile visualizzare il numero di elementi selezionati sotto l'elenco,** soprattutto se è probabile che gli utenti selezionano più elementi. Queste informazioni non solo inviano commenti e suggerimenti utili, ma indicano anche chiaramente che la casella di riepilogo supporta la selezione multipla.

![Screenshot della casella di riepilogo con quattro elementi selezionati ](images/ctrl-list-boxes-image5.png)

In questo esempio il numero di elementi selezionati viene visualizzato sotto l'elenco.

-   È possibile fornire altre metriche di selezione che potrebbero essere più significative, ad esempio le risorse necessarie per le selezioni.

![Screenshot dell'elenco di caselle di controllo delle funzionalità di Windows ](images/ctrl-list-boxes-image18.png)

In questo esempio, lo spazio su disco necessario per installare i componenti è più significativo del numero di elementi selezionati.

-   Se potenzialmente sono presenti molti elementi dell'elenco e la selezione o la cancellazione di tutti gli elementi è probabile, aggiungere i pulsanti di comando Seleziona tutto e Cancella tutti.
-   Per gli elenchi a selezione multipla standard, non usare la modalità di selezione multipla perché questa modalità di selezione è stata deprecata. Per un comportamento equivalente, usare invece un elenco di caselle di controllo.

### <a name="default-values"></a>Valori predefiniti

-   **Selezionare l'opzione più sicura (per impedire la perdita di dati o l'accesso al sistema) e l'opzione più sicura per impostazione predefinita.** Se sicurezza e sicurezza non sono fattori, selezionare l'opzione più probabile o comoda.

**Eccezione:** Non selezionare elementi se il controllo rappresenta [](glossary.md)una proprietà in uno stato misto, cosa che si verifica quando si visualizza una proprietà per più oggetti che non hanno la stessa impostazione.

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

![Screenshot del ridimensionamento e della spaziatura della casella di riepilogo ](images/ctrl-list-boxes-image19.png)

Dimensioni e spaziatura consigliate per le caselle di riepilogo.

-   **Scegliere una larghezza della casella di riepilogo appropriata per i dati validi più lunghi.** Le caselle di riepilogo standard non possono essere scorrete orizzontalmente, quindi gli utenti possono visualizzare solo ciò che è visibile nel controllo.
-   **Includere un ulteriore 30%** (fino al 200% per il testo più breve) per qualsiasi testo (ma non numeri) che verrà localizzato.
-   **Scegliere un'altezza della casella di riepilogo che visualizza un numero integrale di elementi.** Evitare di troncare gli elementi verticalmente.
-   **Scegliere un'altezza della casella di riepilogo che elimini lo scorrimento verticale non necessario.** Le caselle di riepilogo devono essere visualizzate tra 3 e 20 elementi senza dover scorrere. È consigliabile rendere leggermente più lunga una casella di riepilogo se in questo modo si elimina la barra di scorrimento verticale. Gli elenchi con potenzialmente molti elementi devono visualizzare almeno cinque elementi per facilitare lo scorrimento visualizzando più elementi alla volta e rendendo la barra di scorrimento più facile da posizionare.
-   **Se gli utenti traggono vantaggio dall'estensione della casella di riepilogo, rendere ridimensionabile la casella di riepilogo e la finestra padre.** In questo modo gli utenti possono modificare le dimensioni della casella di riepilogo in base alle esigenze. Tuttavia, le caselle di riepilogo ridimensionabili devono visualizzare non meno di tre elementi.

## <a name="labels"></a>Etichette

**Etichette di controllo**

-   Tutte le caselle di riepilogo necessitano di etichette. Scrivere l'etichetta come parola o frase, non come frase. usare i due punti alla fine dell'etichetta.

**Eccezione:** Omettere l'etichetta se si tratta semplicemente di una riemissione dell'istruzione principale di una finestra [di dialogo.](glossary.md) In questo caso, l'istruzione principale accetta i due punti (a meno che non si tratta di una domanda) e la chiave di accesso.

**Accettabile:** ![ Screenshot dell'elenco con etichetta ridondante ](images/ctrl-list-boxes-image20.png)

In questo esempio, l'etichetta della casella di riepilogo rievaluta solo l'istruzione principale.

**Migliore:** ![ Screenshot dell'elenco di senza etichetta ridondante ](images/ctrl-list-boxes-image21.png)

In questo esempio l'etichetta ridondante viene rimossa, quindi l'istruzione principale accetta i due punti e la chiave di accesso.

-   Se una casella di riepilogo è subordinata a un pulsante di opzione o a una casella di controllo e viene introdotta dall'etichetta del controllo che termina con i due punti, non inserire un'etichetta aggiuntiva nel controllo casella di riepilogo.

![Screenshot del pulsante e dell'elenco con la stessa etichetta ](images/ctrl-list-boxes-image22.png)

In questo esempio la casella di riepilogo è subordinata a un pulsante di opzione e condivide la relativa etichetta.

-   Assegnare una chiave [di accesso univoca.](glossary.md) Per le linee guida, vedere [Tastiera](inter-keyboard.md).
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Posizionare l'etichetta a sinistra o sopra il controllo e allineare l'etichetta al bordo sinistro del controllo.
    -   Se l'etichetta è a sinistra, allineare verticalmente il testo dell'etichetta alla prima riga di testo nel controllo .

**Corretto:** ![ Screenshot dell'elenco con etichetta allineata a sinistra sopra la schermata dell'elenco con ](images/ctrl-list-boxes-image23.png)![ etichetta allineata al testo a sinistra ](images/ctrl-list-boxes-image24.png)

In questi esempi l'etichetta in alto è allineata al bordo sinistro della casella di riepilogo e l'etichetta a sinistra è allineata al testo nella casella di riepilogo.

**Non corretto:** ![ Screenshot dell'elenco con etichetta allineata al testo sopra la schermata dell'elenco con l'etichetta allineata in alto ](images/ctrl-list-boxes-image25.png)![ a sinistra ](images/ctrl-list-boxes-image26.png)

In questi esempi non corretti, l'etichetta in alto è allineata al testo nella casella di riepilogo e l'etichetta a sinistra viene allineata alla parte superiore della casella di riepilogo.

-   Per le caselle di riepilogo a selezione multipla, usare un'etichetta che indichi chiaramente che è possibile selezionare più elementi. Le etichette dell'elenco di caselle di controllo possono essere meno esplicite.

**Corretto:** ![ Screenshot dell'elenco con una o più etichette selezionate ](images/ctrl-list-boxes-image27.png)

In questo esempio l'etichetta indica chiaramente che è possibile selezionare più elementi.

**Non corretto:** ![ Screenshot della casella di riepilogo con l'etichetta dei componenti aggiuntivi ](images/ctrl-list-boxes-image28.png)

In questo esempio, l'etichetta non fornisce informazioni ovvie sulla selezione multipla.

**Migliore:** ![ Screenshot dell'elenco di caselle di controllo con l'etichetta dei componenti aggiuntivi ](images/ctrl-list-boxes-image29.png)

In questo esempio, le caselle di controllo indicano chiaramente che è possibile selezionare più elementi, quindi l'etichetta non deve essere esplicita.

-   È possibile specificare unità (secondi, connessioni e così via) tra parentesi dopo l'etichetta.

**Testo dell'opzione**

-   Assegnare un nome univoco a ogni opzione.
-   Usare [l'uso di maiuscole e minuscole](glossary.md)in stile frase, a meno che un elemento non sia un sostantivo appropriato.
-   Scrivere l'etichetta come parola o frase, non come frase e non usare la punteggiatura finale.
-   Usare la formulazione parallela e provare a mantenere la lunghezza circa la stessa per tutte le opzioni.

**Testo informativo e supplementare**

-   Se è necessario aggiungere testo informativo su una casella di riepilogo, aggiungerlo sopra l'etichetta. Usare frasi complete con punteggiatura finale.
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Le informazioni aggiuntive utili ma non necessarie devono essere mantenute brevi. Inserire il testo tra parentesi tra l'etichetta e i due punti o senza parentesi sotto il controllo.

![Screenshot dell'elenco di caselle di controllo e del testo descrittivo ](images/ctrl-list-boxes-image30.png)

In questo esempio il testo supplementare viene inserito sotto l'elenco.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle caselle di riepilogo:

-   Usare il testo esatto dell'etichetta, inclusa la combinazione di maiuscole e minuscole, ma non includere il carattere di sottolineatura o i due punti della chiave di accesso. Includere l'elenco di parole. Non fare riferimento a una casella di riepilogo come casella di riepilogo o campo.
-   Per gli elementi dell'elenco, usare il testo esatto dell'elemento, inclusa la relativa maiuscola.
-   Nella programmazione e in altri documenti tecnici, fare riferimento alle caselle di riepilogo come caselle di riepilogo. In qualsiasi altro luogo, usare list.
-   Per descrivere l'interazione dell'utente, usare select.
-   Quando possibile, formattare l'etichetta e gli elementi dell'elenco usando il testo in grassetto. In caso contrario, inserire l'etichetta e gli elementi tra virgolette solo se necessario per evitare confusione.

Esempio: **nell'elenco Vai a selezionare** **Segnalibro**.

