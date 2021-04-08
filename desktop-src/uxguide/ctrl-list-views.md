---
title: Visualizzazione elenco
description: Con una visualizzazione elenco, gli utenti possono visualizzare e interagire con una raccolta di oggetti dati, usando una selezione singola o più selezioni.
ms.assetid: 62a7bfc8-96a9-450d-9db9-ec9dab6687b7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c3c823b23c03f29ac6b80e10df79eac36653f2e4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761284"
---
# <a name="list-views"></a>Visualizzazione elenco

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con una visualizzazione elenco, gli utenti possono visualizzare e interagire con una raccolta di oggetti dati, usando una selezione singola o più selezioni.

![screenshot della visualizzazione elenco con le intestazioni di colonna ](images/ctrl-list-views-image1.png)

Visualizzazione elenco tipica.

Le visualizzazioni elenco hanno una maggiore flessibilità e funzionalità rispetto alle caselle di riepilogo. Diversamente dalle caselle di riepilogo, supportano la modifica delle visualizzazioni, il raggruppamento, più colonne con intestazioni, l'ordinamento in base alle colonne, la modifica della larghezza e dell'ordine delle colonne, l'origine di un trascinamento o l'obiettivo di rilascio e la copia dei dati da e verso gli Appunti.

> [!Note]  
> Le linee guida relative al [layout](vis-layout.md) e alle [caselle di riepilogo](ctrl-list-boxes.md) vengono presentate in articoli distinti.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Una visualizzazione elenco è più di una semplice casella di riepilogo funzionale e flessibile: la funzionalità aggiuntiva comporta un utilizzo diverso. Nella tabella seguente viene illustrato il confronto.



|                             |                                           |                                                                                                                                               |
|-----------------------------|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
|                             | **Caselle di riepilogo**<br/>                 | **Visualizzazioni elenco**<br/>                                                                                                                     |
| **Tipo di dati**<br/>    | Opzioni per i dati e il programma.<br/> | Solo dati.<br/>                                                                                                                         |
| **Contents**<br/>     | Solo etichette.<br/>                   | Etichette e dati ausiliari, possibilmente in più colonne.<br/>                                                                           |
| **Interazione**<br/>  | Utilizzato per effettuare selezioni.<br/>    | Può essere utilizzato per effettuare selezioni, ma spesso per la visualizzazione e l'interazione con i dati. Può essere un'origine di trascinamento o una destinazione di rilascio.<br/> |
| **Presentazione**<br/> | Fissa.<br/>                         | Gli utenti possono modificare le visualizzazioni, il raggruppamento, l'ordinamento in base alle colonne e modificare la larghezza e l'ordine delle colonne.<br/>                                                |



 

Per decidere se si tratta del controllo corretto, prendere in considerazione le domande seguenti:

-   **L'elenco presenta i dati, anziché le opzioni di programma?** In caso contrario, prendere in considerazione l'uso di una casella di riepilogo.
-   **Gli utenti devono modificare le visualizzazioni, il raggruppamento, l'ordinamento in base alle colonne o modificare la larghezza e l'ordine delle colonne?** In caso contrario, utilizzare una casella di riepilogo.
-   **Il controllo deve essere un'origine di trascinamento o una destinazione di rilascio?** In tal caso, utilizzare una visualizzazione elenco.
-   **Gli elementi dell'elenco devono essere copiati o incollati dagli Appunti?** In tal caso, utilizzare una visualizzazione elenco.

### <a name="check-box-list-views"></a>Visualizzazioni elenco caselle di controllo

-   **Il controllo viene utilizzato per scegliere zero o più elementi da un elenco di dati?** Per scegliere un elemento, usare invece la selezione singola.
-   **La selezione multipla è essenziale per l'attività o comunemente utilizzata?** In tal caso, usare una visualizzazione elenco di caselle di controllo per rendere più ovvie le selezioni, soprattutto se gli utenti di destinazione non sono avanzati. In caso contrario, utilizzare una visualizzazione elenco a selezione multipla standard se le caselle di controllo prelevano troppe attenzioni per la selezione multipla o comportano un disordine dello schermo troppo grande.
-   **La stabilità della selezione multipla è importante?** In tal caso, utilizzare un elenco di caselle di [controllo](ctrl-list-boxes.md), un generatore di elenchi o un elenco di aggiunta/rimozione, perché fare clic su modifica un solo elemento alla volta. Con un elenco di selezione multipla standard, è molto semplice cancellare tutte le selezioni anche per errore.

> [!Note]  
> A volte un controllo simile a una visualizzazione elenco viene implementato utilizzando una casella di riepilogo e viceversa. In questi casi, applicare le linee guida in base all'utilizzo, non all'implementazione.

 

## <a name="usage-patterns"></a>Modelli di utilizzo

Tutte le visualizzazioni supportano la selezione singola, in cui gli utenti possono selezionare un solo elemento alla volta e selezione multipla, in cui gli utenti possono selezionare un numero qualsiasi di elementi, tra cui nessuno. Le visualizzazioni elenco supportano la [modalità di selezione estesa](glossary.md), in cui è possibile estendere la selezione mediante trascinamento o con MAIUSC + clic o CTRL + clic per selezionare rispettivamente i gruppi di valori contigui o non adiacenti. Diversamente dalle caselle di riepilogo, non supportano la [modalità di selezione multipla](glossary.md), in cui fare clic su un elemento per spostare lo stato di selezione indipendentemente dai tasti MAIUSC e CTRL.

### <a name="standard-list-view"></a>Visualizzazione elenco standard

Il controllo visualizzazione elenco supporta cinque visualizzazioni standard:



|                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tile**<br/> ogni elemento viene visualizzato come icona Media, con un'etichetta e i dettagli facoltativi a destra. <br/>                                                                                                                         | ![screenshot delle anteprime con titoli e dettagli ](images/ctrl-list-views-image2.png)<br/> La visualizzazione affiancata Mostra icone medie con etichette e dettagli facoltativi a destra.<br/>                                                                                                                                                                |
| **Icona grande**<br/> ogni elemento viene visualizzato come icona molto grande, grande o media con un'etichetta sotto di essa.<br/>                                                                                                                      | ![screenshot della visualizzazione elenco di anteprime di grandi dimensioni ](images/ctrl-list-views-image3.png)<br/> Visualizzazione icone grandi Mostra ogni elemento come icona grande con un'etichetta sotto di essa.<br/>                                                                                                                                                                              |
| **Icona piccola**<br/> ogni elemento viene visualizzato come icona piccola con un'etichetta a destra.<br/>                                                                                                                                           | ![screenshot della visualizzazione elenco piccole anteprime ](images/ctrl-list-views-image4.png)<br/> Una piccola visualizzazione icone Mostra ogni elemento come piccola icona con la relativa etichetta a destra.<br/>                                                                                                                                                                        |
| **Elenco**<br/> ogni elemento viene visualizzato come icona piccola con un'etichetta a destra.<br/>                                                                                                                                                 | in modalità elenco questa vista Ordina gli elementi nelle colonne e usa una barra di scorrimento orizzontale. al contrario, le modalità di visualizzazione icone ordinano gli elementi nelle righe e usano una barra di scorrimento verticale. <br/> ![screenshot della visualizzazione elenco in modalità elenco ](images/ctrl-list-views-image5.png)<br/> In modalità elenco ogni elemento viene visualizzato come icona piccola con la relativa etichetta a destra.<br/> |
| **Dettagli**<br/> ogni elemento viene visualizzato come una riga in formato tabulare. la colonna più a sinistra contiene l'icona e l'etichetta facoltativa dell'elemento e le colonne successive contengono informazioni aggiuntive, ad esempio le proprietà degli elementi.<br/> | Inoltre, le colonne possono essere aggiunte o rimosse e riordinate e ridimensionate. le righe possono essere raggruppate, ordinate per colonna. <br/> ![screenshot della visualizzazione elenco in modalità dettagli ](images/ctrl-list-views-image6.png)<br/> Visualizzazione dettagli Mostra ogni elemento come riga in un formato di tabella.<br/>                                                              |



 

### <a name="list-view-variations"></a>Variazioni visualizzazione elenco



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Selezione colonne</strong><br/> Le visualizzazioni elenco presentano talvolta un numero così elevato di colonne, che non è pratico per visualizzarle tutte. In questo caso, l'approccio migliore consiste nel visualizzare le colonne più utili per impostazione predefinita e consentire agli utenti di aggiungere o rimuovere le colonne in base alle esigenze. <br/></td>
<td><img src="images/ctrl-list-views-image7.png" alt="Screen shot of list view with Column Chooser menu " /><br/> Facendo clic con il pulsante destro del mouse sull'intestazione di colonna viene visualizzato un menu di scelta rapida che consente di aggiungere o rimuovere colonne.<br/> <img src="images/ctrl-list-views-image8.png" alt="Screen shot of Choose Details dialog box " /><br/> Se si fa clic su altro nel menu di scelta rapida dell'intestazione di colonna, viene visualizzata la finestra di dialogo Scegli colonne, che consente agli utenti di aggiungere o rimuovere colonne e di riordinarle.<br/></td>
</tr>
<tr class="even">
<td><strong>Visualizzazione elenco casella di controllo</strong><br/> Consente agli utenti di selezionare più elementi.<br/></td>
<td>Le visualizzazioni elenco a selezione multipla hanno esattamente lo stesso aspetto delle visualizzazioni elenco a selezione singola, quindi non esiste alcun indizio visivo che supportino selezioni multiple. È possibile utilizzare una visualizzazione elenco di caselle di controllo per indicare chiaramente che è possibile selezionare più selezioni. Di conseguenza, questo modello deve essere usato per le attività in cui la selezione multipla è essenziale o usata di frequente.<br/> <img src="images/ctrl-list-views-image9.png" alt="Screen shot of dialog box with several check boxes " /><br/> In questo esempio, una piccola visualizzazione icone usa le caselle di controllo perché la selezione multipla è essenziale per l'attività.<br/></td>
</tr>
<tr class="odd">
<td><strong>Elencare le visualizzazioni con i gruppi</strong><br/> Organizzare i dati in gruppi.<br/></td>
<td>Sebbene le visualizzazioni dettagli supportino spesso l'ordinamento dei dati in base a qualsiasi colonna, le visualizzazioni elenco consentono agli utenti di organizzare gli elementi in gruppi. Alcuni dei vantaggi del raggruppamento sono i seguenti:<br/>
<ul>
<li>Gruppi funziona in tutte le visualizzazioni (eccetto List), quindi, ad esempio, gli utenti possono raggruppare una visualizzazione icone molto grandi degli album per artista.</li>
<li>I gruppi possono essere raccolte di alto livello, che sono spesso più significative del raggruppamento direttamente dai dati. Ad esempio, Esplora risorse raggruppa le date in oggi, ieri, ultima settimana, prima di quest'anno e molto tempo fa.</li>
</ul>
<img src="images/ctrl-list-views-image10.png" alt="Screen shot of list view with several data groups " /><br/> In questo esempio, il centro accoglienza Windows Mostra gli elementi raggruppati in una visualizzazione elenco.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Indicazioni

### <a name="presentation"></a>Presentazione

-   **Ordina gli elementi dell'elenco in un ordine logico.** Ordina i nomi in ordine alfabetico, numeri in ordine numerico e date in ordine cronologico.
-   **Se necessario, consentire agli utenti di modificare l'ordinamento.** L'ordinamento utente è importante se l'elenco contiene molti elementi o se sono presenti scenari in cui gli elementi vengono trovati più efficacemente utilizzando un ordinamento diverso da quello predefinito.
-   **Usare l'attributo always show Selection** in modo che gli utenti possano determinare prontamente l'elemento selezionato, anche quando il controllo non ha lo stato attivo.
-   **Evitare di presentare visualizzazioni elenco vuote.** Se gli utenti creano un elenco, inizializzare l'elenco con le istruzioni o gli elementi di esempio che potrebbero essere necessari per gli utenti.

    ![screenshot della finestra di dialogo di ricerca con istruzioni ](images/ctrl-list-views-image11.png)

    In questo esempio, nella visualizzazione elenco di ricerca vengono presentate inizialmente le istruzioni.

-   **Se gli utenti possono modificare le visualizzazioni, raggruppare, ordinare in base alle colonne oppure modificare le colonne e le relative larghezze e ordine, rendere effettive le impostazioni in modo che divengano effettive alla successiva visualizzazione dell'elenco.** Renderli mantenuti in base a una visualizzazione per elenco, per ogni utente.

### <a name="interaction"></a>Interazione

-   **Utilizzare un solo clic per selezionare l'elemento dell'elenco a cui l'utente sta puntando. Eccezione:** per il modello di elenco dei collegamenti ai comandi, fare clic con il pulsante destro del mouse su Seleziona l'elemento e chiude la finestra o passa alla pagina successiva.
-   **Si consiglia di fornire un comportamento di doppio clic.** Il doppio clic dovrebbe avere lo stesso effetto della selezione di un elemento e dell'esecuzione del comando predefinito.
-   **Rendere ridondante il comportamento di doppio clic.** Deve essere sempre presente un pulsante di comando o un comando del menu di scelta rapida con lo stesso effetto.
-   Se un elemento dell'elenco richiede una spiegazione ulteriore, **fornire la spiegazione in un** [infotip](ctrl-tooltips-and-infotips.md). Usare le frasi complete e la punteggiatura finale.

    ![screenshot della visualizzazione elenco con tastiera infotip ](images/ctrl-list-views-image12.png)

    In questo esempio viene usato un infotip per fornire ulteriori informazioni.

-   **Fornire menu di scelta rapida dei comandi pertinenti.** Tali comandi includono taglia, copia, incolla, Rimuovi o Elimina, Rinomina e proprietà.
-   **Se gli utenti possono modificare il tipo di ordinamento e il raggruppamento, fornire i menu di scelta rapida Ordina per e raggruppa per.** Il primo clic su un nome di colonna Ordina o raggruppa l'elenco in ordine crescente per la colonna, il secondo Ordina o raggruppa in ordine decrescente. Utilizzare l'ordine precedente (da un'altra colonna) come chiave secondaria.

    ![screenshot della visualizzazione elenco con il menu "Ordina per" ](images/ctrl-list-views-image13.png)

    In questo esempio, il menu di scelta rapida Ordina per modifica il tipo di ordinamento. Fare clic su nome una volta ordinata in base al nome in ordine crescente. Fare clic di nuovo su nome Ordina in base al nome in ordine decrescente.

-   **Rendere accessibile l'intestazione di colonna della visualizzazione elenco usando la tastiera.**
    -   **Sviluppatori:** È possibile eseguire questa operazione impostando lo stato attivo sul controllo intestazione di colonna. Questa funzionalità è una novità di Windows Vista.
-   **Quando si disabilita una visualizzazione elenco, disabilitare anche le etichette e i pulsanti di comando associati.**
-   **Evitare lo scorrimento orizzontale.** La modalità elenco Usa lo scorrimento orizzontale. Questa modalità è in genere la più compatta, ma lo scorrimento orizzontale è in genere più difficile da usare rispetto allo scorrimento verticale. Se la compattazione non è importante, è consigliabile usare invece la visualizzazione icona piccola. Tuttavia, la modalità elenco è una scelta ottimale quando sono presenti molti elementi ordinati in ordine alfabetico e spazio su schermo sufficiente per un controllo esteso.

    **Accettabile:**

    ![Screenshot di un ampio controllo in modalità elenco ](images/ctrl-list-views-image14.png)

    In questo esempio viene utilizzata la modalità elenco perché sono presenti molti elementi e una grande quantità di spazio disponibile sullo schermo per un controllo esteso.

### <a name="multiple-selection-lists"></a>Elenchi a selezione multipla

-   Si **consiglia di visualizzare il numero di elementi selezionati al di sotto dell'elenco**, soprattutto se gli utenti hanno la possibilità di selezionare più elementi. Queste informazioni non solo forniscono utili commenti, ma indicano chiaramente che la visualizzazione elenco supporta più selezioni.

    ![screenshot dell'elenco di cinque anteprime selezionate ](images/ctrl-list-views-image15.png)

    In questo esempio, il numero di elementi selezionati viene visualizzato sotto l'elenco.

-   In alternativa, anziché il numero di elementi selezionati, è possibile assegnare altre metriche di selezione che potrebbero essere più significative, ad esempio le risorse necessarie per le selezioni.

    ![screenshot della finestra di dialogo che mostra lo spazio su disco ](images/ctrl-list-views-image16.png)

    In questo esempio, lo spazio su disco necessario per installare i componenti è più significativo rispetto al numero di componenti selezionati.

-   Per le visualizzazioni elenco di caselle di controllo, se sono presenti potenzialmente molti elementi e la selezione o la cancellazione di tutti gli elementi è probabile, aggiungere tutti i pulsanti di comando Seleziona tutto e cancella tutti.
-   **Usare le caselle di controllo con stato misto per indicare la selezione parziale degli elementi in un contenitore.** Lo stato misto non viene utilizzato come terzo stato per un singolo elemento.

### <a name="changing-views"></a>Modifica delle visualizzazioni

Se gli utenti possono modificare le visualizzazioni:

-   **Per impostazione predefinita, scegliere la visualizzazione più pratica.** Tutte le modifiche apportate dagli utenti devono essere rese permanenti in base a una visualizzazione elenco per singolo utente.
-   **Modificare la visualizzazione utilizzando un pulsante di menu combinato, un pulsante di menu o un elenco a discesa.** Quando possibile, utilizzare un [pulsante di suddivisione](ctrl-command-buttons.md) sulla barra degli strumenti e modificare l'etichetta del pulsante in modo da riflettere la visualizzazione corrente.

    ![screenshot dell'elenco con pulsante Dividi ' views ' ](images/ctrl-list-views-image17.png)

    In questo esempio viene usato un pulsante di suddivisione sulla barra degli strumenti per modificare le visualizzazioni.

-   **Consente di visualizzare un menu di scelta rapida.**

    ![screenshot dell'elenco con il menu di scelta rapida ' Visualizza ' ](images/ctrl-list-views-image18.png)

In questo esempio, per modificare le visualizzazioni viene utilizzato un menu di scelta rapida di visualizzazione.

### <a name="details-views"></a>Visualizzazioni dettagli

-   **Provare a usare la visualizzazione riquadri per migliorare la leggibilità.**

    **Accettabile:**

    ![screenshot dell'elenco di dettagli con colonne strette ](images/ctrl-list-views-image19.png)

    In questo esempio è presente una quantità eccessiva di dati e la finestra, l'elenco e le colonne sono troppo piccole, rendendo gli elementi dell'elenco difficili da leggere.

    **Migliore:**

    ![screenshot dell'elenco dei dettagli con i dati in gruppi ](images/ctrl-list-views-image20.png)

    In questo esempio la visualizzazione affiancata Visualizza i dati senza troncamenti.

-   **Scegliere le larghezze delle colonne predefinite appropriate per i dati più lunghi.** Le visualizzazioni elenco troncano automaticamente i dati di lunghezza con ellissi, quindi le larghezze delle colonne sono appropriate se per impostazione predefinita vengono visualizzati pochi ellissi. Mentre gli utenti possono ridimensionare le colonne, preferire altre soluzioni:

    -   Ridimensionare la larghezza di ogni colonna in base ai dati.
    -   Ridimensionare la larghezza del controllo in modo da adattarla alle colonne più eventuali barre di scorrimento.
    -   Se necessario, usare lo scorrimento orizzontale.
    -   Hanno troncato i dati solo per gli elementi di dimensioni dispari o come ultima risorsa.

    Se per impostazione predefinita è necessario troncare i dati di dimensioni normali, rendere ridimensionabili la finestra e la visualizzazione elenco. Includere un ulteriore 30% (fino al 200% per un testo più breve) per qualsiasi testo (ma non per i numeri) che verrà localizzato.

    **Non corretto:**

    ![screenshot delle colonne dell'elenco con dati troncati ](images/ctrl-list-views-image21.png)

    In questo esempio, la maggior parte dei dati viene troncata. I numerosi puntini di sospensione indicano chiaramente che la larghezza del controllo e della colonna è troppo piccola per i dati.

    **Non corretto:**

    ![Screenshot di un elenco a colonna con dati troncati ](images/ctrl-list-views-image22.png)

    In questo esempio i dati vengono troncati senza motivo.

-   **Scegliere un ordine di colonna predefinito appropriato.** In genere, ordinare le colonne come segue:

    -   In primo luogo, il nome dell'elemento o i dati di identificazione.
    -   Successivamente, altri dati utili per distinguere gli elementi dell'elenco.
    -   Quindi, i dati più utili (preferibilmente brevi o a lunghezza fissa).
    -   Dati successivi, meno utili (preferibili a lunghezza breve o fissa).
    -   Dati Last, Long a lunghezza variabile.

    Long, variable length: i dati vengono inseriti nelle ultime colonne per ridurre la necessità di scorrimento orizzontale. All'interno di queste categorie, le informazioni correlate vengono inserite insieme in una sequenza logica.

-   **Quando appropriato, consentire agli utenti di aggiungere e rimuovere colonne, nonché modificare l'ordine.** Per impostazione predefinita, visualizzare le colonne più utili. Questa operazione viene eseguita con l'attributo Drag Drop dell'intestazione.
-   Scegliere un allineamento appropriato per i dati. Usare le regole seguenti:
    -   Allinea a destra numeri, valute e ore.
    -   Allinea a sinistra il testo, gli ID (anche se numerico) e le date.
-   Per le intestazioni di colonna ordinabili, **il primo clic su un'intestazione Ordina l'elenco in ordine crescente per la colonna, mentre il secondo clic Ordina in ordine decrescente.** Utilizzare il tipo di ordinamento precedente (da un'altra colonna) come chiave di ordinamento secondaria.

    ![screenshot dell'elenco dei dettagli con dati ordinati ](images/ctrl-list-views-image23.png)

    In questo esempio è stata prima fatto clic sulla colonna Name, quindi sulla colonna Type. Di conseguenza, il tipo in ordine crescente è la chiave di ordinamento primaria e il nome in ordine crescente è il database secondario.

-   **Usare l'attributo di selezione riga completa** in modo che gli utenti possano determinare prontamente gli elementi selezionati in tutte le colonne.
-   **Non usare un'intestazione di colonna ordinabile a meno che i dati non possano essere ordinati.**
-   **Non usare un'intestazione di colonna se è presente una sola colonna e non è necessario eseguire l'ordinamento inverso.** Usare invece un'etichetta per identificare i dati.

    **Non corretto:**

    ![screenshot dell'elenco con etichetta nell'intestazione di colonna ](images/ctrl-list-views-image24.png)

    **Corretto:**

    ![screenshot dell'elenco con etichetta sopra il controllo ](images/ctrl-list-views-image25.png)

    Nell'esempio corretto viene utilizzata un'etichetta al posto di un'intestazione di colonna.

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![screenshot del ridimensionamento e della spaziatura dell'elenco ](images/ctrl-list-views-image26.png)

Ridimensionamento e spaziatura consigliati per le visualizzazioni elenco.

-   **Scegliere un'altezza visualizzazione elenco che visualizzi un numero integrale di elementi.** Evitare di troncare verticalmente gli elementi.
-   **Scegliere una dimensione di visualizzazione elenco che elimini lo scorrimento orizzontale e verticale non necessario in tutte le visualizzazioni supportate.** Le visualizzazioni elenco devono essere visualizzate tra 3 e 20 elementi. Si consiglia di rendere una visualizzazione elenco leggermente più grande se si elimina una barra di scorrimento. Gli elenchi con un numero potenzialmente elevato di elementi devono visualizzare almeno cinque elementi per facilitare lo scorrimento mostrando più elementi alla volta e rendendo la barra di scorrimento più semplice da posizionare.
-   **Se gli utenti traggono vantaggio dalla visualizzazione elenco, rendere ridimensionabili la visualizzazione elenco e la finestra padre.** Questa operazione consente agli utenti di modificare le dimensioni della visualizzazione elenco in base alle esigenze. Tuttavia, le visualizzazioni elenco ridimensionabili non devono visualizzare meno di tre elementi.

## <a name="labels"></a>Etichette

### <a name="control-labels"></a>Etichette di controllo

-   Tutte le visualizzazioni elenco necessitano di etichette. Scrivere l'etichetta come una parola o una frase, non come una frase, terminando con i due punti usando il testo statico.
-   Assegnare una [chiave di accesso](glossary.md) univoca per ogni etichetta. Per le linee guida, vedere [tastiera](inter-keyboard.md).
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Posizionare l'etichetta sopra il controllo e allineare l'etichetta al bordo sinistro del controllo.
-   Per le visualizzazioni elenco a selezione multipla, scrivere l'etichetta che indica chiaramente che è possibile selezionare più selezioni. Le etichette di visualizzazione elenco caselle di controllo possono essere meno esplicite.

    **Corretto:**

    ![screenshot dell'etichetta: selezionare uno o più componenti aggiuntivi ](images/ctrl-list-views-image27.png)

    In questo esempio, l'etichetta indica chiaramente che è possibile selezionare più selezioni.

    **Non corretto:**

    ![screenshot dell'etichetta: Componenti aggiuntivi ](images/ctrl-list-views-image28.png)

    In questo esempio, l'etichetta non fornisce informazioni su selezione multipla.

    **Accettabile:**

    ![cattura di schermata dell'etichetta dell'elenco di caselle di controllo: Componenti aggiuntivi ](images/ctrl-list-views-image29.png)

    In questo esempio, le caselle di controllo indicano chiaramente che è possibile selezionare più selezioni, quindi l'etichetta non deve essere esplicita.

-   È possibile specificare unità (secondi, connessioni e così via) tra parentesi dopo l'etichetta.

### <a name="heading-labels"></a>Etichette di intestazione

-   Lasciare brevi le etichette delle intestazioni (tre parole o meno).
-   Usare un solo sostantivo o una frase nominale senza punteggiatura finale.
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Allineare l'intestazione allo stesso modo dei dati.

### <a name="group-labels"></a>Etichette di gruppo

-   Usare le etichette di gruppo seguenti per le raccolte di alto livello:
    -   Nomi: usare la prima lettera di intervalli di nome o lettera.
    -   Dimensioni: non specificato, 0 KB, 0-10 KB, 10-100 KB, 100 KB-1 MB, 1-16 MB, 16-128 MB
    -   Date: oggi, ieri, ultima settimana, prima di quest'anno e molto tempo fa.
-   In caso contrario, le etichette dei gruppi utilizzano il testo esatto dei dati raggruppati, incluse le maiuscole e la punteggiatura.

### <a name="data-text"></a>Testo dati

-   Usare l'uso [di maiuscole in stile frase](glossary.md).

### <a name="instructional-text"></a>Testo istruzioni

-   Se è necessario aggiungere testo di istruzioni su una visualizzazione elenco, aggiungerlo sopra l'etichetta. Utilizzare frasi complete con la punteggiatura finale.
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Informazioni aggiuntive utili ma non necessarie devono essere mantenute brevi. Inserire queste informazioni tra parentesi tra l'etichetta e i due punti o senza parentesi sotto il controllo.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento a visualizzazioni elenco:

-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere il carattere di sottolineatura della chiave di accesso o i due punti e includere l'elenco di parole. Non fare riferimento a una casella di riepilogo come casella di riepilogo, visualizzazione elenco o campo.
-   Per i dati dell'elenco, usare il testo esatto dei dati, inclusa la relativa maiuscola.
-   Vedere le visualizzazioni elenco come visualizzazioni elenco solo nella programmazione e in altre documentazioni tecniche. Elenco di utilizzo di tutti gli altri.
-   Per descrivere l'interazione dell'utente, usare SELECT per i dati e fare clic su per le intestazioni.
-   Quando possibile, formattare le opzioni di etichetta ed elenco usando il testo in grassetto. In caso contrario, inserire l'etichetta e le opzioni tra virgolette solo se necessario per evitare confusione.

Esempio: nell'elenco **programmi e servizi** selezionare **condivisione file e stampanti**.

Quando si fa riferimento alle caselle di controllo in una visualizzazione elenco:

-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, e includere la parola casella di controllo. Non includere il carattere di sottolineatura della chiave di accesso.
-   Per descrivere l'interazione dell'utente, usare SELECT e Clear.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempio: selezionare la casella di controllo **Underline** .

 

