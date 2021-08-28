---
title: Visualizzazioni elenco
description: Con una visualizzazione elenco, gli utenti possono visualizzare e interagire con una raccolta di oggetti dati, usando una selezione singola o più selezioni.
ms.assetid: 62a7bfc8-96a9-450d-9db9-ec9dab6687b7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8b8a1ce068b03ddf2a7aba40a0044f79914102d3
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983064"
---
# <a name="list-views"></a>Visualizzazioni elenco

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con una visualizzazione elenco, gli utenti possono visualizzare e interagire con una raccolta di oggetti dati, usando una selezione singola o più selezioni.

![Screenshot della visualizzazione elenco con intestazioni di colonna ](images/ctrl-list-views-image1.png)

Visualizzazione elenco tipica.

Le visualizzazioni elenco offrono maggiore flessibilità e funzionalità rispetto alle caselle di riepilogo. A differenza delle caselle di riepilogo, supportano la modifica di visualizzazioni, raggruppamenti, più colonne con intestazioni, ordinamento in base alle colonne, modifica della larghezza e dell'ordine delle colonne, origine di trascinamento o destinazione di rilascio e copia dei dati da e verso gli Appunti.

> [!Note]  
> Le linee guida relative [al layout e](vis-layout.md) alle [caselle di riepilogo](ctrl-list-boxes.md) sono presentate in articoli separati.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Una visualizzazione elenco non è solo una casella di riepilogo più flessibile e funzionale: le funzionalità aggiuntive comportano un utilizzo diverso. Nella tabella seguente viene illustrato il confronto.



|   Utilizzo                          | Caselle di riepilogo                 | Visualizzazioni elenco               |
|-----------------------------|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **Tipo di dati**<br/>    | Opzioni per dati e programmi.<br/> | Solo dati.<br/>                                                                                                                         |
| **Contents**<br/>     | Solo etichette.<br/>                   | Etichette e dati ausiliari, possibilmente in più colonne.<br/>                                                                           |
| **Interazione**<br/>  | Usato per effettuare selezioni.<br/>    | Può essere usato per effettuare selezioni, ma spesso usato per la visualizzazione e l'interazione con i dati. Può essere un'origine di trascinamento o un obiettivo di rilascio.<br/> |
| **Presentazione**<br/> | Fisso.<br/>                         | Gli utenti possono modificare le visualizzazioni, raggruppare, ordinare in base alle colonne e modificare la larghezza e l'ordine delle colonne.<br/>                                                |



 

Per decidere se questo è il controllo giusto, considerare queste domande:

-   **L'elenco presenta i dati anziché le opzioni del programma?** In caso contrario, è consigliabile usare una casella di riepilogo.
-   **Gli utenti devono modificare le visualizzazioni, raggruppare, ordinare in base alle colonne o modificare la larghezza e l'ordine delle colonne?** In caso contrario, usare invece una casella di riepilogo.
-   **Il controllo deve essere un'origine di trascinamento o un obiettivo di rilascio?** In tal caso, usare una visualizzazione elenco.
-   **Gli elementi dell'elenco devono essere copiati o incollati dagli Appunti?** In tal caso, usare una visualizzazione elenco.

### <a name="check-box-list-views"></a>Visualizzazioni elenco delle caselle di controllo

-   **Il controllo viene usato per scegliere zero o più elementi da un elenco di dati?** Per scegliere un elemento, usare invece la selezione singola.
-   **La selezione multipla è essenziale per l'attività o viene comunemente usata?** In tal caso, usare una visualizzazione elenco di caselle di controllo per rendere più ovvie le selezioni, soprattutto se gli utenti di destinazione non sono avanzati. In caso contrario, usare una visualizzazione elenco a selezione multipla standard se le caselle di controllo distondono troppo attenzione a più selezioni o causano troppo confusione sullo schermo.
-   **La stabilità della selezione multipla è importante?** In tal caso, usare un elenco di caselle [di](ctrl-list-boxes.md)controllo, un generatore di elenchi o un elenco di aggiunta/rimozione perché facendo clic su viene modificato un solo elemento alla volta. Con un elenco di selezione multipla standard, è molto facile cancellare tutte le selezioni anche per errore.

> [!Note]  
> Talvolta un controllo simile a una visualizzazione elenco viene implementato usando una casella di riepilogo e viceversa. In questi casi, applicare le linee guida in base all'utilizzo, non all'implementazione.

 

## <a name="usage-patterns"></a>Modelli di utilizzo

Tutte le visualizzazioni supportano la selezione singola, in cui gli utenti possono selezionare un solo elemento alla volta e la selezione multipla, in cui gli utenti possono selezionare un numero qualsiasi di elementi, incluso nessuno. Le [visualizzazioni](glossary.md)elenco supportano la modalità di selezione estesa, in cui la selezione può essere estesa trascinando o premendo MAIUSC+clic o CTRL+clic per selezionare rispettivamente gruppi di valori contigui o non adiacenti. A differenza delle caselle di riepilogo, non supportano la modalità di selezione [multipla,](glossary.md)in cui facendo clic su un elemento viene attivato o disattivato lo stato di selezione indipendentemente dai tasti MAIUSC e CTRL.

### <a name="standard-list-view"></a>Visualizzazione elenco standard

Il controllo visualizzazione elenco supporta cinque visualizzazioni standard:



|    Utilizzo    |   Esempio        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tile**<br/> ogni elemento viene visualizzato come icona media, con un'etichetta e dettagli facoltativi a destra. <br/>                                                                                                                         | ![Screenshot delle anteprime con titoli e dettagli ](images/ctrl-list-views-image2.png)<br/> La visualizzazione affiancata mostra icone medie con etichette e dettagli facoltativi a destra.<br/>                                                                                                                                                                |
| **Icona grande**<br/> ogni elemento viene visualizzato come icona molto grande, grande o media con un'etichetta sotto di esso.<br/>                                                                                                                      | ![Screenshot della visualizzazione elenco di anteprime di grandi dimensioni ](images/ctrl-list-views-image3.png)<br/> La visualizzazione Icona grande mostra ogni elemento come icona grande con un'etichetta sotto di esso.<br/>                                                                                                                                                                              |
| **Icona piccola**<br/> ogni elemento viene visualizzato come icona piccola con un'etichetta a destra.<br/>                                                                                                                                           | ![Screenshot della visualizzazione elenco di anteprime di piccole dimensioni ](images/ctrl-list-views-image4.png)<br/> La visualizzazione Icona piccola mostra ogni elemento come icona piccola con l'etichetta a destra.<br/>                                                                                                                                                                        |
| **Elenco**<br/> ogni elemento viene visualizzato come icona piccola con un'etichetta a destra.<br/>                                                                                                                                                 | in modalità elenco, questa visualizzazione ordina gli elementi nelle colonne e usa una barra di scorrimento orizzontale. al contrario, le modalità di visualizzazione icona ordinano gli elementi in righe e usano una barra di scorrimento verticale. <br/> ![Screenshot della visualizzazione elenco in modalità elenco ](images/ctrl-list-views-image5.png)<br/> La modalità elenco mostra ogni elemento come icona piccola con la relativa etichetta a destra.<br/> |
| **Dettagli**<br/> ogni elemento viene visualizzato come riga in formato tabulare. la colonna più a sinistra contiene sia l'icona facoltativa che l'etichetta dell'elemento e le colonne successive contengono informazioni aggiuntive, ad esempio le proprietà dell'elemento.<br/> | Inoltre, le colonne possono essere aggiunte o rimosse e riordinate e ridimensionate. Le righe possono essere raggruppate, ordinate per colonna. <br/> ![Screenshot della visualizzazione elenco in modalità dettagli ](images/ctrl-list-views-image6.png)<br/> La visualizzazione Dettagli mostra ogni elemento come riga in formato tabella.<br/>                                                              |



 

### <a name="list-view-variations"></a>Varianti della visualizzazione elenco




| Etichetta | Valore |
|--------|-------|
| <strong>Selezione colonne</strong><br /> Le visualizzazioni elenco a volte hanno così tante colonne che non è pratico mostrarle tutte. In questo caso, l'approccio migliore consiste nel visualizzare le colonne più utili per impostazione predefinita e consentire agli utenti di aggiungere o rimuovere colonne in base alle esigenze. <br /> | <img src="images/ctrl-list-views-image7.png" alt="Screen shot of list view with Column Chooser menu " /><br /> Facendo clic con il pulsante destro del mouse sull'intestazione di colonna viene visualizzato un menu di scelta rapida che consente agli utenti di aggiungere o rimuovere colonne.<br /><img src="images/ctrl-list-views-image8.png" alt="Screen shot of Choose Details dialog box " /><br /> Se si fa clic su Altro nel menu di scelta rapida dell'intestazione di colonna, viene visualizzata la finestra di dialogo Scegli colonne che consente agli utenti di aggiungere o rimuovere colonne e di riordinarle.<br /> | 
| <strong>Visualizzazione elenco delle caselle di controllo</strong><br /> Consente agli utenti di selezionare più elementi.<br /> | Le visualizzazioni elenco a selezione multipla hanno esattamente lo stesso aspetto delle visualizzazioni elenco a selezione singola, quindi non esiste alcuna indicazione visiva che supportino la selezione multipla. Una visualizzazione elenco di caselle di controllo può essere usata per indicare chiaramente che è possibile effettuare più selezioni. Di conseguenza, questo modello deve essere usato per le attività in cui la selezione multipla è essenziale o comune.<br /><img src="images/ctrl-list-views-image9.png" alt="Screen shot of dialog box with several check boxes " /><br /> In questo esempio, in una visualizzazione Icona piccola vengono utilizzate caselle di controllo perché la selezione multipla è essenziale per l'attività.<br /> | 
| <strong>Visualizzazioni elenco con gruppi</strong><br /> Organizzare i dati in gruppi.<br /> | Anche se le visualizzazioni Dettagli spesso supportano l'ordinamento dei dati in base a una delle colonne, le visualizzazioni elenco consentono agli utenti di organizzare gli elementi in gruppi. Di seguito sono riportati alcuni vantaggi del raggruppamento:<br /><ul><li>I gruppi funzionano in tutte le visualizzazioni (ad eccezione dell'elenco), quindi, ad esempio, gli utenti possono raggruppare una visualizzazione icone di grandi dimensioni degli album in base all'artista.</li><li>I gruppi possono essere raccolte di alto livello, che spesso sono più significative del raggruppamento diretto dei dati. Ad esempio, Windows Explorer raggruppa le date in Today, Yesterday, Last week, Earlier this year e A long time ago.</li></ul><img src="images/ctrl-list-views-image10.png" alt="Screen shot of list view with several data groups " /><br /> In questo esempio, il Windows Centro attività iniziali mostra gli elementi raggruppati in una visualizzazione elenco.<br /> | 




 

## <a name="guidelines"></a>Indicazioni

### <a name="presentation"></a>Presentazione

-   **Ordinare gli elementi dell'elenco in un ordine logico.** Ordinare i nomi in ordine alfabetico, i numeri in ordine numerico e le date in ordine cronologico.
-   **Se appropriato, consentire agli utenti di modificare l'ordinamento.** L'ordinamento degli utenti è importante se l'elenco contiene molti elementi o se esistono scenari in cui gli elementi vengono trovati in modo più efficace usando un ordinamento diverso da quello predefinito.
-   **Usare l'attributo Mostra sempre selezione** in modo che gli utenti possano determinare rapidamente l'elemento selezionato, anche quando il controllo non ha lo stato attivo.
-   **Evitare di presentare visualizzazioni elenco vuote.** Se gli utenti creano un elenco, inizializzare l'elenco con istruzioni o elementi di esempio che potrebbero essere necessari agli utenti.

    ![Screenshot della finestra di dialogo di ricerca con le istruzioni ](images/ctrl-list-views-image11.png)

    In questo esempio la visualizzazione Elenco di ricerca presenta inizialmente le istruzioni.

-   **Se gli utenti possono modificare le visualizzazioni, raggruppare, ordinare in base alle colonne o modificare le colonne e la larghezza e l'ordine, rendere persistenti queste impostazioni in modo che siano effettive alla successiva visualizzazione elenco.** Renderli persistenti in base a una visualizzazione per elenco, per utente.

### <a name="interaction"></a>Interazione

-   **Usare un solo clic per selezionare l'elemento dell'elenco a cui punta l'utente. Eccezione:** per il modello di elenco dei collegamenti di comando, fare clic con un solo clic per selezionare l'elemento e chiudere la finestra o passare alla pagina successiva.
-   **Valutare la possibilità di fornire il comportamento del doppio clic.** Il doppio clic dovrebbe avere lo stesso effetto della selezione di un elemento e dell'esecuzione del comando predefinito.
-   **Rendere ridondante il comportamento del doppio clic.** Deve essere sempre presente un pulsante di comando o un comando del menu di scelta rapida che ha lo stesso effetto.
-   Se un elemento dell'elenco richiede ulteriori spiegazioni, **fornire la spiegazione in un** [infotip](ctrl-tooltips-and-infotips.md). Usare frasi complete e punteggiatura finale.

    ![Screenshot della visualizzazione elenco con il suggerimento della tastiera ](images/ctrl-list-views-image12.png)

    In questo esempio viene usato un infotip per fornire altre informazioni.

-   **Fornire i menu di scelta rapida dei comandi pertinenti.** Tali comandi includono Taglia, Copia, Incolla, Rimuovi o Elimina, Rinomina e Proprietà.
-   **Se gli utenti possono modificare l'ordinamento e il raggruppamento, specificare i menu di scelta rapida Ordina per e Raggruppa per.** Il primo clic su un nome di colonna ordina o raggruppa l'elenco in ordine crescente per tale colonna, il secondo fa clic ordina o raggruppa in ordine decrescente. Usare l'ordine precedente (da un'altra colonna) come chiave secondaria.

    ![Screenshot della visualizzazione elenco con il menu "ordina per" ](images/ctrl-list-views-image13.png)

    In questo esempio il menu di scelta rapida Ordina per modifica l'ordinamento. Facendo clic su Name (Nome) viene ordinato in base al nome in ordine crescente. Facendo di nuovo clic su Nome, il nome viene ordinato in ordine decrescente.

-   **Rendere accessibile l'intestazione di colonna della visualizzazione elenco usando la tastiera.**
    -   **Sviluppatori:** A tale scopo, impostare lo stato attivo sul controllo intestazione di colonna. Questa funzionalità è una novità di Windows Vista.
-   **Quando si disabilita una visualizzazione elenco, disabilitare anche le etichette e i pulsanti di comando associati.**
-   **Evitare lo scorrimento orizzontale.** La modalità Elenco usa lo scorrimento orizzontale. Questa modalità è in genere la più compatta, ma lo scorrimento orizzontale è in genere più difficile da usare rispetto a quello verticale. È consigliabile usare la visualizzazione Icona piccola se la compattezza non è importante. Tuttavia, la modalità elenco è una scelta ottimale quando sono presenti molti elementi ordinati in ordine alfabetico e uno spazio sufficiente sullo schermo per un controllo wide.

    **Accettabile:**

    ![Screenshot di un controllo in modalità elenco ampio ](images/ctrl-list-views-image14.png)

    In questo esempio viene usata la modalità Elenco perché sono presenti molti elementi e molto spazio disponibile sullo schermo per un controllo wide.

### <a name="multiple-selection-lists"></a>Elenchi a selezione multipla

-   **È consigliabile visualizzare il numero di elementi selezionati sotto l'elenco,** soprattutto se è probabile che gli utenti selezionano più elementi. Queste informazioni non solo inviano feedback utili, ma indicano anche chiaramente che la visualizzazione elenco supporta la selezione multipla.

    ![Screenshot dell'elenco di cinque anteprime selezionate ](images/ctrl-list-views-image15.png)

    In questo esempio il numero di elementi selezionati viene visualizzato sotto l'elenco.

-   In alternativa, anziché il numero di elementi selezionati, è possibile assegnare altre metriche di selezione che potrebbero essere più significative, ad esempio le risorse necessarie per le selezioni.

    ![Screenshot della finestra di dialogo che mostra lo spazio su disco ](images/ctrl-list-views-image16.png)

    In questo esempio, lo spazio su disco necessario per installare i componenti è più significativo del numero di componenti selezionati.

-   Per le visualizzazioni elenco di caselle di controllo, se potenzialmente sono presenti molti elementi e la selezione o la cancellazione di tutti gli elementi è probabile, aggiungere Seleziona tutto e Cancella tutti i pulsanti di comando.
-   **Usare le caselle di controllo dello stato misto per indicare la selezione parziale degli elementi in un contenitore.** Lo stato misto non viene usato come terzo stato per un singolo elemento.

### <a name="changing-views"></a>Modifica delle visualizzazioni

Se gli utenti possono modificare le visualizzazioni:

-   **Scegliere la visualizzazione più comoda per impostazione predefinita.** Tutte le modifiche apportate dagli utenti devono essere rese persistenti per ogni visualizzazione elenco, per utente.
-   **Modificare la visualizzazione usando un pulsante di divisione, un pulsante di menu o un elenco a discesa.** In caso di praticità, usare [un pulsante di divisione](ctrl-command-buttons.md) sulla barra degli strumenti e modificare l'etichetta del pulsante in modo che rifletta la visualizzazione corrente.

    ![Screenshot dell'elenco con il pulsante di divisione delle visualizzazioni ](images/ctrl-list-views-image17.png)

    In questo esempio viene usato un pulsante di divisione sulla barra degli strumenti per modificare le visualizzazioni.

-   **Specificare un menu di scelta rapida Visualizza.**

    ![Screenshot dell'elenco con il menu di scelta rapida "visualizza" ](images/ctrl-list-views-image18.png)

In questo esempio viene usato un menu di scelta rapida Visualizza per modificare le visualizzazioni.

### <a name="details-views"></a>Visualizzazioni dei dettagli

-   **È consigliabile usare la visualizzazione riquadri per migliorare la leggibilità.**

    **Accettabile:**

    ![Screenshot dell'elenco dei dettagli con colonne ristrette ](images/ctrl-list-views-image19.png)

    In questo esempio sono presenti troppi dati e la finestra, l'elenco e le colonne sono troppo piccole, rendendo gli elementi dell'elenco difficili da leggere.

    **Migliore:**

    ![Screenshot dell'elenco dei dettagli con i dati in gruppi ](images/ctrl-list-views-image20.png)

    In questo esempio la visualizzazione Riquadro visualizza i dati senza troncamento.

-   **Scegliere le larghezze di colonna predefinite appropriate per i dati più lunghi.** Le visualizzazioni elenco troncano automaticamente i dati lunghi con puntini di sospensione, pertanto la larghezza delle colonne è appropriata se per impostazione predefinita vengono visualizzati pochi puntini di sospensione. Anche se gli utenti possono ridimensionare le colonne, preferire altre soluzioni:

    -   Ridimensionare ogni larghezza di colonna per adattarla ai relativi dati.
    -   Ridimensionare la larghezza del controllo in modo che si adatti alle colonne più eventuali barre di scorrimento.
    -   Se necessario, usare lo scorrimento orizzontale.
    -   I dati sono stati troncati solo per gli elementi di dimensioni dispari o come ultima risorsa.

    Se i dati di dimensioni normali devono essere troncati per impostazione predefinita, rendere ridimensionabile la finestra e la visualizzazione elenco. Includere un ulteriore 30% (fino al 200% per il testo più breve) per qualsiasi testo (ma non numeri) che verrà localizzato.

    **Non corretto:**

    ![Screenshot delle colonne dell'elenco con dati troncati ](images/ctrl-list-views-image21.png)

    In questo esempio la maggior parte dei dati viene troncata. I molti puntini di sospensione indicano chiaramente che la larghezza del controllo e della colonna è troppo piccola per i dati.

    **Non corretto:**

    ![Screenshot dell'elenco a una colonna con dati troncati ](images/ctrl-list-views-image22.png)

    In questo esempio i dati vengono troncati senza motivo.

-   **Scegliere un ordine di colonna predefinito appropriato.** In genere, ordinare le colonne nel modo seguente:

    -   In primo luogo, il nome dell'elemento o i dati di identificazione.
    -   Successivamente, altri dati utili per differenziare gli elementi dell'elenco.
    -   Successivamente, i dati più utili (preferibilmente a lunghezza breve o fissa).
    -   Successivamente, dati meno utili (preferibilmente a lunghezza breve o fissa).
    -   Ultimi dati di lunghezza variabile.

    I dati di lunghezza variabile e lunga vengono inseriti nelle ultime colonne per ridurre la necessità di scorrimento orizzontale. All'interno di queste categorie, inserire le informazioni correlate insieme in una sequenza logica.

-   **Se appropriato, consentire agli utenti di aggiungere e rimuovere colonne, nonché modificare l'ordine.** Visualizzare le colonne più utili per impostazione predefinita. Questa operazione viene ottenuta con l'attributo Header Drag Drop.
-   Scegliere un allineamento appropriato per i dati. Usare le regole seguenti:
    -   Allineare a destra numeri, valute e ore.
    -   Testo allineato a sinistra, ID (anche se numerici) e date.
-   Per le intestazioni di colonna ordinabili, il primo clic su un'intestazione ordina l'elenco in ordine crescente per la colonna, il secondo fa clic **in ordine decrescente.** Usare l'ordinamento precedente (da un'altra colonna) come chiave di ordinamento secondaria.

    ![Screenshot dell'elenco dei dettagli con dati ordinati ](images/ctrl-list-views-image23.png)

    In questo esempio è stato fatto clic prima sulla colonna Nome e quindi sulla colonna Tipo. Di conseguenza, Type in ascending order è la chiave di ordinamento primaria e Name in ascending order is the secondary.

-   **Usare l'attributo Full Row Select** in modo che gli utenti possano determinare facilmente gli elementi selezionati in tutte le colonne.
-   **Non usare un'intestazione di colonna ordinabile a meno che non sia possibile ordinare i dati.**
-   **Non usare un'intestazione di colonna se è presente una sola colonna e non è necessario invertire l'ordinamento.** Usare invece un'etichetta per identificare i dati.

    **Non corretto:**

    ![Screenshot dell'elenco con etichetta nell'intestazione di colonna ](images/ctrl-list-views-image24.png)

    **Corretto:**

    ![Screenshot dell'elenco con etichetta sopra il controllo ](images/ctrl-list-views-image25.png)

    Nell'esempio corretto viene usata un'etichetta anziché un'intestazione di colonna.

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

![Screenshot del ridimensionamento e della spaziatura dell'elenco ](images/ctrl-list-views-image26.png)

Dimensioni e spaziatura consigliate per le visualizzazioni elenco.

-   **Scegliere un'altezza della visualizzazione elenco che visualizzi un numero integrale di elementi.** Evitare di troncare gli elementi verticalmente.
-   **Scegliere una dimensione di visualizzazione elenco che elimini lo scorrimento verticale e orizzontale non necessario in tutte le visualizzazioni supportate.** Le visualizzazioni elenco devono visualizzare da 3 a 20 elementi. È consigliabile rendere leggermente più grande una visualizzazione elenco in caso di eliminazione di una barra di scorrimento. Gli elenchi con potenzialmente molti elementi devono visualizzare almeno cinque elementi per facilitare lo scorrimento visualizzando più elementi alla volta e rendendo la barra di scorrimento più facile da posizionare.
-   **Se gli utenti traggono vantaggio dal rendere la visualizzazione elenco più grande, rendere ridimensionabile la visualizzazione elenco e la relativa finestra padre.** In questo modo, gli utenti possono modificare le dimensioni della visualizzazione elenco in base alle esigenze. Tuttavia, le visualizzazioni elenco ridimensionabili devono visualizzare non meno di tre elementi.

## <a name="labels"></a>Etichette

### <a name="control-labels"></a>Etichette di controllo

-   Tutte le visualizzazioni elenco necessitano di etichette. Scrivere l'etichetta come parola o frase, non come frase, terminando con due punti usando testo statico.
-   Assegnare una chiave [di accesso univoca](glossary.md) per ogni etichetta. Per le linee guida, vedere [Tastiera](inter-keyboard.md).
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Posizionare l'etichetta sopra il controllo e allineare l'etichetta al bordo sinistro del controllo.
-   Per le visualizzazioni elenco a selezione multipla, scrivere l'etichetta che indica chiaramente che è possibile selezionare più elementi. Le etichette della visualizzazione elenco di caselle di controllo possono essere meno esplicite.

    **Corretto:**

    ![Screenshot dell'etichetta: selezionare uno o più componenti aggiuntivi ](images/ctrl-list-views-image27.png)

    In questo esempio l'etichetta indica chiaramente che è possibile selezionare più elementi.

    **Non corretto:**

    ![Screenshot dell'etichetta: componenti aggiuntivi ](images/ctrl-list-views-image28.png)

    In questo esempio l'etichetta non fornisce informazioni sulla selezione multipla.

    **Accettabile:**

    ![Screenshot dell'etichetta dell'elenco di caselle di controllo: componenti aggiuntivi ](images/ctrl-list-views-image29.png)

    In questo esempio, le caselle di controllo indicano chiaramente che è possibile selezionare più elementi, quindi l'etichetta non deve essere esplicita.

-   È possibile specificare unità (secondi, connessioni e così via) tra parentesi dopo l'etichetta.

### <a name="heading-labels"></a>Etichette di intestazione

-   Mantenere brevi le etichette di intestazione (tre parole o meno).
-   Usare una singola frase sostantiva o sostantiva senza punteggiatura finale.
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Allineare l'intestazione allo stesso modo dei dati.

### <a name="group-labels"></a>Raggruppare le etichette

-   Usare le etichette di gruppo seguenti per le raccolte di alto livello:
    -   Nomi: usare la prima lettera di nome o gli intervalli di lettere.
    -   Dimensioni: Non specificato, 0 KB, 0-10 KB, 10-100 KB, 100 KB - 1 MB, 1-16 MB, 16-128 MB
    -   Dates: Today, Yesterday, Last week, Earlier this year, and A long time ago.
-   In caso contrario, le etichette di gruppo usano il testo esatto dei dati da raggruppare, incluse le lettere maiuscole e la punteggiatura.

### <a name="data-text"></a>Testo dei dati

-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)

### <a name="instructional-text"></a>Testo informativo

-   Se è necessario aggiungere testo informativo su una visualizzazione elenco, aggiungerlo sopra l'etichetta. Usare frasi complete con punteggiatura finale.
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Le informazioni aggiuntive utili ma non necessarie devono essere mantenute brevi. Inserire queste informazioni tra parentesi tra l'etichetta e i due punti o senza parentesi sotto il controllo.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle visualizzazioni elenco:

-   Usare il testo esatto dell'etichetta, incluse le lettere maiuscole, ma non includere il carattere di sottolineatura o i due punti della chiave di accesso e includere l'elenco di parole. Non fare riferimento a una casella di riepilogo come casella di riepilogo, visualizzazione elenco o campo.
-   Per elencare i dati, usare il testo esatto dei dati, inclusa l'uso di maiuscole e minuscole.
-   Fare riferimento alle visualizzazioni elenco come visualizzazioni elenco solo nella programmazione e in altre documentazione tecnica. In qualsiasi altro luogo usare list.
-   Per descrivere l'interazione dell'utente, usare select per i dati e fare clic per le intestazioni.
-   Quando possibile, formattare le opzioni di etichetta ed elenco usando il testo in grassetto. In caso contrario, inserire l'etichetta e le opzioni tra virgolette solo se necessario per evitare confusione.

Esempio: **nell'elenco Programmi e servizi** selezionare Condivisione file e **stampanti**.

Quando si fa riferimento alle caselle di controllo in una visualizzazione elenco:

-   Usare il testo esatto dell'etichetta, inclusa l'uso di maiuscole e minuscole, e includere la casella di controllo della parola. Non includere il carattere di sottolineatura della chiave di accesso.
-   Per descrivere l'interazione dell'utente, usare select e clear.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempio: selezionare la **casella di controllo** Sottolineatura.

 

