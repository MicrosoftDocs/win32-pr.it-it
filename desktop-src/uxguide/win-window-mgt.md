---
title: Gestione finestre
description: In questo articolo viene illustrata la posizione predefinita delle finestre quando visualizzate inizialmente sullo schermo, il relativo ordine di sovrapposizione rispetto ad altre finestre (z order), le dimensioni iniziali e il modo in cui la visualizzazione influiscono sullo stato attivo per l'input.
ms.assetid: d81bd71c-6d8f-45a9-82cb-bdb9b8bcbb11
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dc194741713a139f643ad84b829294577d020d94
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103968828"
---
# <a name="window-management"></a>Gestione finestre

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

In questo articolo viene illustrata la posizione predefinita delle finestre quando visualizzate inizialmente sullo schermo, il relativo ordine di sovrapposizione rispetto ad altre finestre ([z order](glossary.md)), le dimensioni iniziali e il modo in cui la visualizzazione influiscono sullo stato attivo per l'input.

Per le linee guida seguenti:

-   Una finestra di primo livello non dispone di una finestra proprietaria e viene visualizzata sulla barra delle applicazioni. Esempi: finestre dell'applicazione. In Windows Vista e versioni successive, anche le finestre di dialogo senza finestre proprietarie e finestre delle proprietà vengono considerate di primo livello.
-   Una finestra di proprietà ha una finestra proprietaria e non viene visualizzata sulla barra delle applicazioni. Esempi: finestre di dialogo modali, finestre di dialogo non modali.
-   Una finestra avviata dall'utente viene visualizzata come il risultato diretto di un'azione dell'utente. In caso contrario, viene avviato dal programma se avviato da un programma o avviato dal sistema se avviato da Microsoft Windows. Ad esempio, una finestra di dialogo Opzioni viene avviata dall'utente, ma un promemoria della riunione viene avviato dal programma.
-   Una finestra contestuale è una finestra avviata dall'utente che ha una relazione forte con l'oggetto da cui è stata avviata. Ad esempio, le finestre visualizzate in base ai menu di scelta rapida o alle icone dell'area di notifica sono contestuali, ma le finestre visualizzate dalle barre dei menu non lo sono.
-   Il monitoraggio attivo è il monitoraggio in cui è in esecuzione il programma attivo.
-   Il monitoraggio predefinito è quello con il menu Start, la barra delle applicazioni e l'area di notifica.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Gestione finestre è una delle attività utente più importanti. Prima di Windows Vista, a Windows venivano spesso assegnate dimensioni predefinite minime e venivano posizionate al centro dello schermo. Questo approccio funziona bene per i monitoraggi singoli precedenti a bassa risoluzione, ma non per l'hardware video moderno.

Windows è progettato per supportare l'hardware video moderno, che spesso viene eseguito a risoluzioni significativamente superiori rispetto alla risoluzione minima supportata dello schermo e può disporre di più monitoraggi. In questo modo:

-   Consente agli utenti di trarre vantaggio completamente dall'hardware avanzato.
-   Richiede meno impegno da parte degli utenti per spostare il mouse tra più distanze.
-   Rende la posizione della finestra più prevedibile e quindi più facile da trovare.

### <a name="the-minimum-supported-screen-resolution"></a>Risoluzione minima dello schermo supportata

La [risoluzione minima effettiva dello schermo](glossary.md) supportata da Windows è 800x600 pixel. Ciò significa che le finestre a dimensione fissa dovrebbero essere visualizzate completamente con la risoluzione minima (riservando spazio per la barra delle applicazioni), ma le finestre ridimensionabili possono essere ottimizzate per una risoluzione efficace di 1024x768 pixel, purché siano funzionali con la risoluzione minima.

Sebbene attualmente le risoluzioni dello schermo fisico più comuni per i PC Windows siano 1024x768 pixel o superiore, la destinazione di 800x600 pixel consente a Windows di:

-   Funziona bene con tutti i componenti hardware moderni, inclusi i computer notebook di piccole dimensioni.
-   Supportano le impostazioni dpi (punti per pollice) elevate.
-   Supporto di tipi di carattere più grandi per l'accessibilità.
-   Supportare l'hardware utilizzato su base globale.

La scelta della risoluzione minima da supportare richiede un giusto equilibrio. La definizione di una risoluzione più elevata comporta un'esperienza non ottimale per una percentuale significativa di hardware moderno, mentre la definizione di una risoluzione più bassa impedisce ai progettisti di sfruttare al meglio lo spazio disponibile sullo schermo.

Se si ritiene che gli utenti di destinazione stiano utilizzando risoluzioni significativamente più elevate rispetto al valore minimo di Windows, è possibile progettare il programma per sfruttare appieno lo spazio dello schermo aggiuntivo utilizzando finestre ridimensionabili con scalabilità.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Supporta la risoluzione minima di Windows per 800x600 pixel.** Per le interfacce utente critiche (UI) che devono funzionare in modalità provvisoria, supportare una risoluzione efficace di 640x480 pixel. Assicurarsi di tenere conto dello spazio usato dalla barra delle applicazioni riservando 48 [pixel relativi](glossary.md) per le finestre visualizzate con la barra delle applicazioni.
-   **Ottimizzare il layout delle finestre ridimensionabili per una risoluzione efficace di 1024x768 pixel.** Ridimensionare automaticamente le finestre per risoluzioni dello schermo inferiori in modo ancora funzionante.
-   **Assicurarsi di testare le finestre con 96 dpi (100%) a 800x600 pixel, 120 dpi (125%) a 1024x768 pixel e 144 dpi (150%) a 1200x900 pixel.** Verificare la presenza di problemi di layout, ad esempio il ritaglio di controlli, testo e finestre, nonché l'estensione delle icone e delle bitmap.
-   **Per i programmi con scenari di utilizzo tocco e dispositivi mobili, ottimizzarli per 120 dpi.** Le schermate ad alta risoluzione sono attualmente prevalentemente nei PC portatili e a tocco.
-   Le finestre ridimensionabili **non devono più visualizzare il glifo di ridimensionamento** nell'angolo inferiore destro, perché:
    -   Tutti i lati e i bordi di una finestra sono ridimensionabili, non solo l'angolo inferiore destro.
    -   Il glifo richiede la visualizzazione di una barra di stato, ma molte finestre ridimensionabili non forniscono barre di stato.
    -   I bordi ridimensionabili della finestra e i puntatori di ridimensionamento sono più efficaci quando si comunica che una finestra è ridimensionabile rispetto al glifo di ridimensionamento.

### <a name="title-bar-controls"></a>Controlli barra del titolo

Usare i controlli della barra del titolo come indicato di seguito:

-   **Vicino.** Tutte le finestre primarie e secondarie con una cornice di finestra standard devono avere un pulsante Chiudi sulla barra del titolo. Quando si fa clic su Chiudi si annulla o chiude la finestra.

![screenshot della finestra di dialogo senza pulsante Chiudi ](images/win-window-mgt-image1.png)

In questo esempio, nella finestra di dialogo non è presente un pulsante Chiudi nella barra del titolo.

-   **Minimizzare.** Tutte le finestre primarie e le finestre secondarie non modali con esecuzione prolungata, ad esempio le finestre di dialogo di stato, devono avere un pulsante Riduci a icona. Fare clic su Riduci a icona per ridurre la finestra al pulsante della barra delle applicazioni. Di conseguenza, le finestre che possono essere ridotte a icona richiedono un'icona della barra del titolo.
-   **Ingrandimento/ripristino.** Tutte le finestre ridimensionabili devono avere un pulsante di ingrandimento/ripristino. Fare clic su Ingrandisci per visualizzare la finestra con le dimensioni massime, che per la maggior parte delle finestre è a schermo intero; Quando si fa clic su Ripristina giù, la finestra viene visualizzata nelle dimensioni precedenti. Tuttavia, alcune finestre non traggono vantaggio dall'utilizzo di un schermo intero, pertanto queste finestre dovrebbero ottimizzare le dimensioni più utili.

### <a name="window-size"></a>Dimensioni finestra

-   **Scegliere le dimensioni predefinite della finestra appropriate per il relativo contenuto.** Se è possibile utilizzare lo spazio in modo efficiente, non è necessario utilizzare dimensioni della finestra iniziale maggiori.
-   **Usare le finestre ridimensionabili ogni volta che è possibile evitare le barre di scorrimento e i dati troncati.** Windows con contenuto dinamico ed elenchi sfrutta al meglio le finestre ridimensionabili.
-   **Per i documenti di testo, prendere in considerazione la lunghezza massima della riga di 65 caratteri** per facilitare la lettura del testo. I caratteri includono lettere, punteggiatura e spazi.
-   Finestre a dimensione fissa:
    -   **Deve essere completamente visibile e dimensionato per adattarsi all'area di lavoro.**
-   Finestre ridimensionabili:
    -   **Può essere ottimizzato per risoluzioni più elevate, ma ridimensionato in base alle necessità in fase di visualizzazione per la risoluzione effettiva dello schermo.**
    -   **Per le dimensioni della finestra progressivamente più grandi, è necessario che le informazioni vengano visualizzate gradualmente.** Assicurarsi che almeno una parte o un controllo della finestra includa contenuto ridimensionabile.
    -   **Evitare dimensioni ripristinate predefinite ingrandite o quasi ingrandite.** Scegliere invece una dimensione predefinita che in genere è la più utile senza essere a schermo intero. Si supponga che gli utenti ingrandiranno la finestra anziché ridimensionarla per renderla a schermo intero.
    -   **Impostare una dimensione minima della finestra se è presente una dimensione al di sotto della quale il contenuto non è più utilizzabile.** Per i controlli ridimensionabili, impostare dimensioni minime degli elementi ridimensionabili sulle dimensioni funzionali più piccole, ad esempio la larghezza minima delle colonne funzionali nelle visualizzazioni elenco.
    -   **Modificare la presentazione se questa operazione rende il contenuto utilizzabile a dimensioni inferiori.**

![screenshot dei pulsanti di Media Player ](images/win-window-mgt-image2.png)

In questo esempio, Windows Media Player modifica il formato quando la finestra diventa troppo piccola per il formato standard.

### <a name="window-location"></a>Posizione della finestra

-   **Per le linee guida seguenti, la "centratura" indica la distorsione della posizione verticale leggermente verso la parte superiore del monitor, anziché posizionarla esattamente al centro.** Inserire il 45% dello spazio tra la parte superiore del monitor/proprietario e la parte superiore della finestra e il 55% tra la parte inferiore del monitor/proprietario e la parte inferiore della finestra. Eseguire questa operazione perché l'occhio è naturalmente polarizzato verso la parte superiore dello schermo.

    ![Figura della finestra posizionata leggermente sopra il centro ](images/win-window-mgt-image3.png)

    "Centramento" indica la distorsione della posizione verticale leggermente verso la parte superiore del monitor.

-   **Se una finestra è contestuale, visualizzarla sempre accanto all'oggetto da cui è stata avviata.** Inserirlo in modo che l'oggetto di origine non sia coperto dalla finestra.

    -   Se viene visualizzato utilizzando il mouse, quando possibile posizionarlo in basso e a destra.

    ![Figura della finestra contestuale situata a destra dell'oggetto ](images/win-window-mgt-image4.png)

    Mostra le finestre contestuali accanto all'oggetto da cui è stato avviato.

    ![Figura della finestra dell'area di notifica ](images/win-window-mgt-image5.png)

    Le finestre avviate dalle icone dell'area di notifica vengono visualizzate accanto all'area di notifica.

-   Se viene visualizzato utilizzando una penna, quando possibile posizionarlo in modo che non venga trattato da parte dell'utente. Per gli utenti a destra, visualizzare a sinistra; in caso contrario, viene visualizzato a destra.

    ![Figura della finestra contestuale posizionata a sinistra dell'oggetto ](images/win-window-mgt-image6.png)

    Quando si usa una penna, Mostra anche le finestre contestuali in modo che non siano coperte dalla mano dell'utente.

-   **Sviluppatori:** È possibile distinguere tra gli eventi del mouse e gli eventi di penna usando l'API [GetMessageExtraInfo](../tablet/system-events-and-mouse-messages.md) . È possibile determinare la [manualità](/previous-versions/ms819495(v=msdn.10)) dell'utente usando l'API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ GETMENUDROPALIGNMENT.
-   **Posizionare i dialoghi sullo stato di avanzamento all'esterno dell'angolo inferiore destro del monitor attivo.**

    ![Figura dell'indicatore di stato nell'angolo inferiore destro ](images/win-window-mgt-image7.png)

    Posizionare le finestre di dialogo di stato nell'angolo inferiore destro.

-   **Se una finestra non è correlata al contesto o all'azione dell'utente corrente, posizionarla fuori dalla posizione corrente del puntatore.** Questa operazione impedisce l'interazione accidentale.
-   **Se una finestra è un'applicazione o un documento di primo livello, l'origine viene sempre propagata dall'angolo superiore sinistro del monitor.** Se creato dal programma attivo, utilizzare il monitoraggio attivo; in caso contrario, utilizzare il monitoraggio predefinito.

    ![Figura di tre propagazione di Windows dall'angolo in alto a sinistra ](images/win-window-mgt-image8.png)

    Propagazione delle finestre di primo livello dell'applicazione o del documento dall'angolo superiore sinistro del monitor.

-   **Se una finestra è un'utilità di primo livello, è sempre visualizzata come "centrata" nel monitoraggio.** Se creato dal programma attivo, utilizzare il monitoraggio attivo; in caso contrario, utilizzare il monitoraggio predefinito.

    ![Figura della finestra di utilità centrata nel monitoraggio ](images/win-window-mgt-image9.png)

    Finestre di utilità di primo livello al centro.

-   **Se una finestra è una finestra di proprietà, visualizzarla inizialmente "centrata" nella parte superiore della finestra proprietaria.** Per la visualizzazione successiva, provare a visualizzarla nell'ultima posizione, relativa alla finestra proprietaria, se questa operazione è probabilmente più pratica.

    ![Figura della finestra di proprietà centrata sulla finestra proprietaria ](images/win-window-mgt-image10.png)

    Centrare inizialmente le finestre di proprietà nella parte superiore della finestra proprietaria.

-   **Per le finestre di dialogo non modali, visualizzare sempre inizialmente nella parte superiore della finestra proprietaria per facilitarne l'individuazione.** Tuttavia, se l'utente attiva la finestra proprietaria, questa potrebbe nascondere la finestra di dialogo non modale.

    ![Figura della finestra di dialogo non modale sulla finestra proprietario ](images/win-window-mgt-image11.png)

    Visualizzare le finestre di dialogo non modali inizialmente nella parte superiore della finestra proprietaria per facilitarne l'individuazione.

-   **Se necessario, modificare la posizione iniziale in modo che l'intera finestra sia visibile all'interno del monitor di destinazione.** Se una finestra ridimensionabile è più grande del monitor di destinazione, ridurla per adattarla.

### <a name="window-order-z-order"></a>Ordine della finestra (z order)

-   **Posizionare sempre le finestre di proprietà nella parte superiore della finestra proprietaria.** Non inserire mai finestre di proprietà nelle finestre di proprietario, perché la maggior parte degli utenti probabilmente non le visualizzerà.
-   **Rispettare la selezione dei z order degli utenti. Quando gli utenti selezionano una finestra, solo le finestre associate a tale istanza del programma (la finestra più qualsiasi proprietario o finestra di proprietà) all'inizio del z order.** Non modificare l'ordine delle altre finestre, ad esempio le istanze indipendenti dello stesso programma.

### <a name="window-activation"></a>Attivazione finestra

-   **Rispettare la selezione dello stato della finestra degli utenti. Se è necessario prestare attenzione a una finestra esistente, lampeggiare il pulsante della barra delle applicazioni tre volte per attirare l'attenzione e lasciarla evidenziata, ma non eseguire altre operazioni.** Non ripristinare o attivare la finestra. Non usare alcun effetto acustico. In alternativa, consentire agli utenti di attivare la finestra quando sono pronti.
    -   **Eccezione:** Se la finestra non viene visualizzata sulla barra delle applicazioni, portarla nella parte superiore di tutte le altre finestre e lampeggiare la relativa barra del titolo.
-   **Il ripristino di una finestra primaria deve anche ripristinare tutte le finestre secondarie**, anche se le finestre secondarie hanno il proprio pulsante della barra delle applicazioni. Quando si esegue il ripristino, posizionare le finestre secondarie nella parte superiore della finestra principale.

### <a name="input-focus"></a>Stato attivo per l'input

-   **Le finestre visualizzate dalle azioni avviate dall'utente dovrebbero assumere lo stato attivo per l'input, ma solo se viene eseguito il rendering immediato della finestra** (entro 5 secondi). Una volta eseguito il rendering della finestra, può assumere lo stato attivo per l'input.
    -   Se una finestra viene visualizzata lentamente (più di 5 secondi), è probabile che gli utenti eseguano un'altra attività durante l'attesa. L'attenzione a questo punto costituisce un problema, soprattutto se eseguita più di una volta.
-   **Le finestre che non vengono visualizzate immediatamente o visualizzate da un'azione avviata dal sistema non devono assumere lo stato attivo per l'input.** Al contrario, visualizzare in primo piano senza lo stato attivo e consentire agli utenti di attivarli quando sono pronti.
    -   **Eccezione:** Gestione credenziali.

### <a name="persistence"></a>Persistenza

-   **Quando una finestra viene visualizzata nuovamente, provare a visualizzarla nello stesso stato dell'ultimo accesso.** Alla chiusura, salvare il monitoraggio usato, le dimensioni della finestra, la posizione e lo stato (ingrandito rispetto al ripristino). Quando si esegue la rivisualizzazione, ripristinare le dimensioni, la posizione e lo stato della finestra salvata utilizzando il monitor appropriato. Si consiglia inoltre di fare in modo che questi attributi vengano mantenuti tra le istanze del programma in base ai singoli utenti. **Eccezioni**
    -   Non salvare o rendere questi attributi mantenuti per Windows quando il loro utilizzo è tale che è molto più probabile che gli utenti debbano iniziare completamente.
    -   Per i programmi che possono essere usati nei computer Windows Tablet e Touch Technology, salvare due stati di Windows per le modalità orizzontale e verticale. Per ulteriori informazioni, vedere [progettazione per diverse dimensioni di visualizzazione](/previous-versions/windows/desktop/ms695587(v=vs.85)).
-   **Se la configurazione del monitoraggio corrente impedisce la visualizzazione di una finestra con l'ultimo stato:**
    -   Provare a visualizzare la finestra utilizzando l'ultimo monitoraggio.
    -   Se la finestra è più grande del monitoraggio, ridimensionare la finestra in modo necessario.
    -   Spostare la posizione verso l'angolo superiore sinistro per adattarla al monitoraggio in base alle esigenze.
    -   Se i passaggi precedenti non consentono di risolvere il problema, ripristinare le linee guida predefinite per la selezione host per la finestra. Se possibile, provare a ripristinare le dimensioni precedenti.

 

 