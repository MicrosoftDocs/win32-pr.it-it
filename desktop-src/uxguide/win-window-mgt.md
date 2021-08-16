---
title: Gestione finestre
description: Questo articolo illustra il posizionamento predefinito delle finestre quando vengono visualizzate inizialmente sullo schermo, l'ordine di sovrapposizione rispetto ad altre finestre (ordine Z), le dimensioni iniziali e il modo in cui lo schermo influisce sullo stato attivo per l'input.
ms.assetid: d81bd71c-6d8f-45a9-82cb-bdb9b8bcbb11
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b8dc2858b0e3cc3b2a451210a61315c610afc727ac42156d5c4fc5c112135807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118212164"
---
# <a name="window-management"></a>Gestione finestre

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Questo articolo illustra il posizionamento predefinito delle finestre quando vengono visualizzate inizialmente sullo schermo, l'ordine di sovrapposizione rispetto ad altre finestre ([ordine Z](glossary.md)), le dimensioni iniziali e il modo in cui lo schermo influisce sullo stato attivo per l'input.

Per le linee guida seguenti:

-   Una finestra di primo livello non ha alcuna finestra proprietaria e viene visualizzata sulla barra delle applicazioni. Esempi: finestre dell'applicazione. In Windows Vista e versioni successive, anche le finestre di dialogo senza finestre proprietarie e finestre delle proprietà vengono considerate di primo livello.
-   Una finestra di proprietà ha una finestra proprietaria e non viene visualizzata sulla barra delle applicazioni. Esempi: finestre di dialogo modali, finestre di dialogo non modali.
-   Una finestra avviata dall'utente viene visualizzata come risultato diretto dell'azione di un utente. In caso contrario, viene avviato dal programma se avviato da un programma o dal sistema se avviato da Microsoft Windows . Ad esempio, una finestra di dialogo Opzioni viene avviata dall'utente, ma viene avviato un promemoria della riunione.
-   Una finestra contestuale è una finestra avviata dall'utente che ha una relazione forte con l'oggetto da cui è stata avviata. Ad esempio, le finestre visualizzate dai menu di scelta rapida o dalle icone dell'area di notifica sono contestuali, ma non le finestre visualizzate dalle barre dei menu.
-   Il monitoraggio attivo è il monitoraggio in cui è in esecuzione il programma attivo.
-   Il monitoraggio predefinito è quello con il menu Start, la barra delle applicazioni e l'area di notifica.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

La gestione delle finestre è una delle attività più fondamentali degli utenti. Prima Windows Vista, alle finestre venivano spesso date piccole dimensioni predefinite e posizionate al centro dello schermo. Questo approccio funziona bene per i monitor singoli e a bassa risoluzione meno recenti, ma non per l'hardware video moderno.

Windows è progettato per supportare hardware video moderno, che spesso viene eseguito a risoluzioni significativamente superiori alla risoluzione minima dello schermo supportata e può avere più monitor. In questo modo:

-   Consente agli utenti di trarre vantaggio completamente dall'hardware avanzato.
-   Richiede meno impegno da parte degli utenti per spostare il mouse su distanze maggiori.
-   Rende il posizionamento della finestra più prevedibile e quindi più facile da trovare.

### <a name="the-minimum-supported-screen-resolution"></a>Risoluzione minima dello schermo supportata

La risoluzione [minima effettiva dello](glossary.md) schermo supportata da Windows è di 800x600 pixel. Ciò significa che le finestre di dimensioni fisse devono essere visualizzate completamente alla risoluzione minima (riservando spazio per la barra delle applicazioni), ma le finestre ridimensionabili possono essere ottimizzate per una risoluzione effettiva di 1024x768 pixel, purché funzionino alla risoluzione minima.

Anche se attualmente le risoluzioni dello schermo fisiche più comuni per i PC Windows sono 1024 x 768 pixel o superiori, la destinazione di 800x600 pixel consente di Windows:

-   Funziona bene con tutto l'hardware moderno, inclusi i PC notebook di piccole dimensioni.
-   Supporto delle impostazioni dpi (punti per pollice) elevate.
-   Supporto di tipi di carattere più grandi per l'accessibilità.
-   Supportare l'hardware usato a livello globale.

La scelta della risoluzione minima da supportare richiede il giusto equilibrio. La destinazione di una risoluzione più elevata comporta un'esperienza non ottimale per una percentuale significativa di hardware moderno, mentre la destinazione di una risoluzione inferiore impedirebbe ai progettisti di sfruttare al meglio lo spazio disponibile sullo schermo.

Se si ritiene che gli utenti di destinazione utilizzino risoluzioni significativamente più elevate rispetto al minimo Windows, è possibile progettare il programma in modo da sfruttare al meglio lo spazio aggiuntivo dello schermo usando finestre ridimensionabili con scalabilità elevata.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Supportare la risoluzione Windows effettiva di 800x600 pixel.** Per le interfacce utente critiche che devono funzionare in modalità provvisoria, supportare una risoluzione effettiva di 640x480 pixel. Assicurarsi di usare lo spazio usato dalla barra delle applicazioni [](glossary.md) riservando 48 pixel verticali relativi per le finestre visualizzate con la barra delle applicazioni.
-   **Ottimizzare i layout delle finestre ridimensionabili per una risoluzione effettiva di 1024x768 pixel.** Ridimensionare automaticamente queste finestre per le risoluzioni dello schermo inferiori in modo che sia ancora funzionante.
-   **Assicurarsi di testare le finestre in 96 dpi (100%) a 800 x 600 pixel, 120 dpi (125%) a 1024 x 768 pixel e 144 dpi (150%) a 1200x900 pixel.** Verificare la presenza di problemi di layout, ad esempio il ritaglio di controlli, testo e finestre e l'estensione di icone e bitmap.
-   **Per i programmi con scenari di uso touch e mobile, ottimizzare per 120 dpi.** Gli schermi ad alta risoluzione sono attualmente prevalenti nei PC touch e per dispositivi mobili.
-   **Le finestre ridimensionabili non devono più visualizzare il glifo** di ridimensionamento nell'angolo inferiore destro, perché:
    -   Tutti i lati e i bordi di una finestra sono ridimensionabili, non solo l'angolo inferiore destro.
    -   Il glifo richiede la visualizzazione di una barra di stato, ma molte finestre ridimensionabili non forniscono barre di stato.
    -   I bordi della finestra ridimensionabile e i puntatori di ridimensionamento sono più efficaci nel comunicare che una finestra è ridimensionabile rispetto al glifo di ridimensionamento.

### <a name="title-bar-controls"></a>Controlli della barra del titolo

Usare i controlli della barra del titolo come indicato di seguito:

-   **Vicino.** Tutte le finestre primarie e secondarie con una cornice di finestra standard devono avere un pulsante Chiudi sulla barra del titolo. Fare clic su Chiudi ha l'effetto di annullare o chiudere la finestra.

![Screenshot della finestra di dialogo senza pulsante chiudi ](images/win-window-mgt-image1.png)

In questo esempio la finestra di dialogo non ha un pulsante Chiudi nella barra del titolo.

-   **Minimizzare.** Tutte le finestre primarie e le finestre secondarie non modali a esecuzione lunga,ad esempio le finestre di dialogo di stato, devono avere un pulsante Riduci a icona. Se si fa clic su Riduci a icona, la finestra viene ridotta al pulsante della barra delle applicazioni. Di conseguenza, le finestre che possono essere ridotte a icona richiedono un'icona della barra del titolo.
-   **Ingrandisci/Ripristina in basso.** Tutte le finestre ridimensionabili devono avere un pulsante Ingrandisci/Ripristina in basso. Facendo clic su Ingrandisci viene visualizzata la finestra con le dimensioni più grandi, che per la maggior parte delle finestre è a schermo intero; mentre facendo clic su Ripristina in basso viene visualizzata la finestra con le dimensioni precedenti. Tuttavia, alcune finestre non traggono vantaggio dall'uso di uno schermo intero, quindi queste finestre dovrebbero ingrandire fino alle dimensioni utili più grandi.

### <a name="window-size"></a>Dimensioni finestra

-   **Scegliere le dimensioni predefinite della finestra appropriate per il contenuto.** Se è possibile usare lo spazio in modo efficace, non è necessario usare dimensioni di finestra iniziali maggiori.
-   **Usare le finestre ridimensionabili ogni volta che è pratico per evitare barre di scorrimento e dati troncati.** Windows contenuto dinamico e gli elenchi traggono il massimo vantaggio dalle finestre ridimensionabili.
-   **Per i documenti di testo, prendere in** considerazione una lunghezza massima di riga di 65 caratteri per semplificare la lettura del testo. I caratteri includono lettere, punteggiatura e spazi.
-   Finestre di dimensioni fisse:
    -   **Deve essere completamente visibile e ridimensionato per adattarsi all'area di lavoro.**
-   Finestre ridimensionabili:
    -   **Può essere ottimizzato per risoluzioni più elevate, ma ridimensionato in base alle esigenze in fase di visualizzazione alla risoluzione effettiva dello schermo.**
    -   **Per le dimensioni delle finestre sempre più grandi, devono essere visualizzate progressivamente più informazioni.** Assicurarsi che almeno una parte della finestra o un controllo abbia contenuto ridimensionabile.
    -   **Evitare dimensioni ripristinate predefinite ingrandite o quasi ingrandite.** Scegliere invece una dimensione predefinita che in genere sia la più utile senza essere a schermo intero. Si supponga che gli utenti ingrandiranno la finestra invece di ridimensionarla per renderla a schermo intero.
    -   **Deve impostare una dimensione minima della finestra se è presente una dimensione inferiore alla quale il contenuto non è più utilizzabile.** Per i controlli ridimensionabili, impostare le dimensioni minime degli elementi ridimensionabili sulle dimensioni funzionali più piccole, ad esempio la larghezza minima delle colonne funzionali nelle visualizzazioni elenco.
    -   **Se si esegue questa operazione, è consigliabile modificare la presentazione per rendere il contenuto utilizzabile in dimensioni più piccole.**

![Screenshot dei pulsanti del lettore multimediale ](images/win-window-mgt-image2.png)

In questo esempio, Windows Media Player il formato quando la finestra diventa troppo piccola per il formato standard.

### <a name="window-location"></a>Posizione della finestra

-   **Per le linee guida seguenti, "centrare" significa distorsione del posizionamento verticale leggermente verso la parte superiore del monitor, anziché posizionarsi esattamente al centro.** Inserire il 45% dello spazio tra la parte superiore del monitor/proprietario e la finestra superiore e il 55% tra la parte inferiore del monitor/proprietario e la finestra inferiore. Eseguire questa operazione perché l'occhio è naturalmente distorto verso la parte superiore dello schermo.

    ![figura della finestra posizionata leggermente sopra il centro ](images/win-window-mgt-image3.png)

    "Centratura" significa distorsione del posizionamento verticale leggermente verso la parte superiore del monitor.

-   **Se una finestra è contestuale, visualizzarla sempre accanto all'oggetto da cui è stata avviata.** Posizionarlo in modo che l'oggetto di origine non sia coperto dalla finestra.

    -   Se viene visualizzato con il mouse, quando possibile posizionarlo verso il basso e verso destra.

    ![Figura della finestra contestuale posizionata a destra dell'oggetto ](images/win-window-mgt-image4.png)

    Mostra le finestre contestuali accanto all'oggetto da cui è stato avviato.

    ![figura della finestra dell'area di notifica ](images/win-window-mgt-image5.png)

    Windows le icone avviate dall'area di notifica vengono visualizzate accanto all'area di notifica.

-   Se viene visualizzato con una penna, quando possibile posizionarlo in modo da non essere coperto dalla mano dell'utente. Per gli utenti con la mano destra, visualizzare a sinistra; in caso contrario, viene visualizzato a destra.

    ![figura della finestra contestuale posizionata a sinistra dell'oggetto ](images/win-window-mgt-image6.png)

    Quando si usa una penna, visualizzare anche le finestre contestuali in modo che non siano coperte dalla mano dell'utente.

-   **Sviluppatori:** È possibile distinguere tra eventi del mouse ed eventi penna usando [l'API GetMessageExtraInfo.](../tablet/system-events-and-mouse-messages.md) È possibile determinare la mano [dell'utente usando](/previous-versions/ms819495(v=msdn.10)) l'API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ GETMENUDROPALIGNMENT.
-   **Posizionare le finestre di dialogo di stato nell'angolo inferiore destro del monitor attivo.**

    ![figura dell'indicatore di stato nell'angolo inferiore destro ](images/win-window-mgt-image7.png)

    Posizionare le finestre di dialogo di stato nell'angolo inferiore destro.

-   **Se una finestra non è correlata al contesto corrente o all'azione dell'utente, spostarla dalla posizione corrente del puntatore.** In questo modo si impedisce l'interazione accidentale.
-   **Se una finestra è un'applicazione o un documento di primo livello, propagarne sempre l'origine dall'angolo superiore sinistro del monitor.** Se creato dal programma attivo, usare il monitoraggio attivo. In caso contrario, usare il monitoraggio predefinito.

    ![figura di tre finestre a cascata dall'alto a sinistra ](images/win-window-mgt-image8.png)

    Sovrapporre le finestre dell'applicazione o del documento di primo livello all'angolo superiore sinistro del monitor.

-   **Se una finestra è un'utilità di primo livello, visualizzarla sempre al centro nel monitor.** Se creato dal programma attivo, usare il monitoraggio attivo. In caso contrario, usare il monitoraggio predefinito.

    ![figura della finestra dell'utilità centrata nel monitor ](images/win-window-mgt-image9.png)

    Centrare le finestre di utilità di primo livello.

-   **Se una finestra è una finestra di proprietà, inizialmente la visualizza "centrata" nella parte superiore della finestra proprietaria.** Per la visualizzazione successiva, è consigliabile visualizzarla nell'ultima posizione (relativa alla finestra del proprietario) se questa operazione è probabilmente più pratica.

    ![figura della finestra di proprietà centrata sulla finestra proprietaria ](images/win-window-mgt-image10.png)

    Centrare inizialmente le finestre di proprietà nella parte superiore della finestra proprietaria.

-   **Per le finestre di dialogo non modali, vengono sempre visualizzate inizialmente sopra la finestra del proprietario per facilitane l'individuazione.** Tuttavia, se l'utente attiva la finestra proprietaria, ciò potrebbe nascondere la finestra di dialogo non modali.

    ![figura della finestra di dialogo non modabile sulla finestra proprietaria ](images/win-window-mgt-image11.png)

    Visualizzare inizialmente le finestre di dialogo non modali nella parte superiore della finestra del proprietario per facilitane l'individuazione.

-   **Se necessario, modificare la posizione iniziale in modo che l'intera finestra sia visibile all'interno del monitor di destinazione.** Se una finestra ridimensionabile è più grande del monitor di destinazione, ridurla per adattarla.

### <a name="window-order-z-order"></a>Ordine delle finestre (ordine Z)

-   **Posizionare sempre le finestre di proprietà nella parte superiore della finestra proprietaria.** Non posizionare mai le finestre di proprietà sotto le finestre proprietarie, perché molto probabilmente gli utenti non le visualizzano.
-   **Rispettare la selezione dell'ordine Z degli utenti. Quando gli utenti selezionano una finestra, portare solo le finestre associate a tale istanza del programma (la finestra più eventuali finestre proprietarie o di proprietà) all'inizio dell'ordine Z.** Non modificare l'ordine di altre finestre, ad esempio istanze indipendenti dello stesso programma.

### <a name="window-activation"></a>Attivazione della finestra

-   **Rispettare la selezione dello stato della finestra degli utenti. Se una finestra esistente richiede attenzione, eseguire il flash del pulsante della barra delle applicazioni tre volte per attirare l'attenzione e lasciarla evidenziata, ma non eseguire altre attività.** Non ripristinare o attivare la finestra. Non usare effetti sonori. In alternativa, consentire agli utenti di attivare la finestra quando sono pronti.
    -   **Eccezione:** Se la finestra non viene visualizzata sulla barra delle applicazioni, portarla nella parte superiore di tutte le altre finestre e far lampeggiare la barra del titolo.
-   **Il ripristino di una finestra primaria dovrebbe ripristinare anche tutte le finestre secondarie,** anche se tali finestre secondarie hanno un proprio pulsante della barra delle applicazioni. Durante il ripristino, posizionare le finestre secondarie sopra la finestra primaria.

### <a name="input-focus"></a>Stato attivo per l'input

-   **Windows azioni avviate** dall'utente devono avere lo stato attivo per l'input, ma solo se il rendering della finestra viene eseguito immediatamente (entro 5 secondi). Una volta eseguito il rendering della finestra, può spostare lo stato attivo per l'input una sola volta.
    -   Se il rendering di una finestra è lento (più di 5 secondi), è probabile che gli utenti eseerino un'altra attività durante l'attesa. Concentrarsi a questo punto sarebbe un problema, soprattutto se eseguito più volte.
-   **Windows che non vengono immediatamente visualizzate o visualizzate da un'azione avviata dal sistema non devono avere lo stato attivo per l'input.** Al contrario, è possibile visualizzarli in alto senza lo stato attivo e consentire agli utenti di attivarli quando sono pronti.
    -   **Eccezione:** Gestione credenziali.

### <a name="persistence"></a>Persistenza

-   **Quando una finestra viene visualizzata nuovamente, è consigliabile visualizzarla nello stesso stato dell'ultimo accesso.** Quando si chiude, salvare il monitoraggio usato, le dimensioni della finestra, la posizione e lo stato (ingrandito o ripristinato). Quando si visualizza nuovamente, ripristinare le dimensioni, la posizione e lo stato della finestra salvati usando il monitoraggio appropriato. Valutare anche la possibilità di rendere questi attributi persistenti tra le istanze del programma per singolo utente. **Eccezioni:**
    -   Non salvare o rendere questi attributi persistenti per le finestre quando il loro utilizzo è tale che gli utenti hanno molto più probabilità di voler ricominciare completamente.
    -   Per i programmi che probabilmente verranno usati nei computer Tecnologia Windows per Tablet PC, salvare due stati di Windows per le modalità orizzontale e verticale. Per altre informazioni, vedere [Progettazione per dimensioni di visualizzazione variabili.](/previous-versions/windows/desktop/ms695587(v=vs.85))
-   **Se la configurazione del monitoraggio corrente impedisce la visualizzazione di una finestra con l'ultimo stato:**
    -   Provare a visualizzare la finestra usando l'ultimo monitor.
    -   Se la finestra è più grande del monitor, ridimensionarla in base alle esigenze.
    -   Spostare la posizione verso l'angolo superiore sinistro per adattarla al monitor in base alle esigenze.
    -   Se i passaggi precedenti non risolvono il problema, ripristinare le linee guida predefinite per il posizionamento delle finestre. Se possibile, provare a ripristinare le dimensioni precedenti.

 

 