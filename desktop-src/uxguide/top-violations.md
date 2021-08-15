---
title: Elenco di controllo dell'esperienza utente per le applicazioni desktop
description: Ecco una raccolta di alcune importanti linee guida nella Guida all'esperienza utente. È possibile usarlo come elenco di controllo per assicurarsi che l'interfaccia utente del programma osevi questi elementi importanti.
ms.assetid: 4705a807-5949-4957-8ea6-70871beaf8e0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 712b31a7a5166e41e590470aea48f60a1f159850da3ea6917b36ece9ada80fa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119332471"
---
# <a name="ux-checklist-for-desktop-applications"></a>Elenco di controllo dell'esperienza utente per le applicazioni desktop

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Ecco una raccolta di alcune importanti linee guida nella Guida all'esperienza utente. È possibile usarlo come elenco di controllo per assicurarsi che l'interfaccia utente del programma osevi questi elementi importanti.

## <a name="windows"></a>Windows

-   **Supportare la risoluzione Windows effettiva di 800 x 600 pixel.** Per le interfacce utente critiche che devono funzionare in modalità [](glossary.md) provvisoria, supportare una risoluzione effettiva di 640x480 pixel. Assicurarsi di usare lo spazio usato dalla barra delle applicazioni [](glossary.md) riservando 48 pixel verticali relativi per le finestre visualizzate con la barra delle applicazioni.
-   **Ottimizzare i layout delle finestre ridimensionabili per una risoluzione effettiva di 1024 x 768 pixel.** Ridimensionare automaticamente queste finestre per le risoluzioni dello schermo inferiori in modo che sia ancora funzionante.
-   **Assicurarsi di testare le finestre in modalità 96 punti per pollice (dpi) (a 800 x 600 pixel), 120 dpi (a 1024 x 768 pixel) e 144 dpi (a 1200 x 900 pixel).** Verificare la presenza di problemi di layout, ad esempio il ritaglio di controlli, testo e finestre e l'estensione di icone e bitmap.
-   **Per i programmi con scenari di uso touch e mobile, ottimizzare per 120 dpi.** Gli schermi ad alta risoluzione sono attualmente prevalenti nei PC touch e per dispositivi mobili.
-   **Se una finestra è una finestra di proprietà, inizialmente la visualizza "centrata" nella parte superiore della finestra proprietaria.** Mai sotto. Per la visualizzazione successiva, è consigliabile visualizzarla nell'ultima posizione (rispetto alla finestra del proprietario) se questa operazione è più comoda.
-   **Se una finestra è contestuale, visualizzarla sempre accanto all'oggetto da cui è stata avviata.** Tuttavia, posizionarlo fuori strada (preferibilmente offset verso il basso e a destra) in modo che l'oggetto non sia coperto dalla finestra.

## <a name="layout"></a>Layout

-   **Ridimensionare i controlli e i riquadri all'interno di una finestra in modo che corrispondano al contenuto tipico.** Evitare il testo troncato e i puntini di sospensione associati. Gli utenti non devono mai interagire con una finestra per visualizzare il contenuto tipico, riservando il ridimensionamento e lo scorrimento per contenuti insolitamente grandi. Controllare in particolare:
    -   **Dimensioni dei controlli.** Ridimensionare i controlli in base al contenuto tipico, rendendo i controlli più ampi, più alti o multilinea, se necessario. Controlli delle dimensioni per eliminare o ridurre lo scorrimento nelle finestre con molto spazio disponibile. Inoltre, non dovrebbero mai essere presenti etichette troncate o testo troncato all'interno di finestre con molto spazio disponibile. Tuttavia, per semplificare la lettura del testo, è consigliabile limitare la larghezza delle righe a 65 caratteri.
    -   **Larghezze delle colonne.** Assicurarsi che le dimensioni predefinite, minime e massime delle colonne della visualizzazione elenco siano adatte. Scegliere le visualizzazioni elenco larghezze predefinite delle colonne che non comportano il troncamento del testo, soprattutto se è disponibile spazio all'interno della visualizzazione elenco.
    -   **Bilanciamento del layout.** Il layout di una finestra dovrebbe essere approssimativamente bilanciato. Se il layout sembra molto pesante a sinistra, è consigliabile rendere i controlli più ampi e spostare alcuni controlli più a destra.
    -   **Ridimensionamento del layout.** Quando una finestra è ridimensionabile e i dati vengono troncati, assicurarsi che le dimensioni della finestra più grandi mostrino più dati. Quando i dati vengono troncati, gli utenti prevedono che le finestre di ridimensionamento mostrino altre informazioni.
-   **Impostare una dimensione minima della finestra se è presente una dimensione inferiore alla quale il contenuto non è più utilizzabile.** Per i controlli ridimensionabili, impostare le dimensioni minime degli elementi ridimensionabili sulle dimensioni funzionali più piccole, ad esempio la larghezza minima delle colonne funzionali nelle visualizzazioni elenco.

## <a name="text"></a>Testo

-   **Quando è possibile, usare termini comuni e conversazionali.** Concentrarsi sugli obiettivi dell'utente, non sulla tecnologia. Ciò è particolarmente efficace se si illustra un concetto o un'azione tecnica complessa. Imagine'utente e spiega come eseguire l'attività.
-   **Essere educati, di supporto e incoraggianti.** L'utente non deve mai essere incolpato, incolpato o intimidato.
-   **Rimuovere il testo ridondante.** Cercare testo ridondante nei titoli delle finestre, nelle istruzioni principali, nelle istruzioni supplementari, nelle aree di contenuto, nei collegamenti ai comandi e nei pulsanti di commit. In genere, lasciare il testo completo nelle istruzioni principali e nei controlli interattivi e rimuovere la ridondanza dalle altre posizioni.
-   **Usare l'uso di maiuscole e minuscole in stile titolo per i titoli e l'uso di maiuscole e minuscole in stile frase per tutti gli altri elementi dell'interfaccia utente.** In questo modo è più appropriato per il Windows tono.
    -   **Eccezione:** Per le applicazioni legacy, è possibile usare l'uso di maiuscole e minuscole per i pulsanti di comando, i menu e le intestazioni di colonna, se necessario, per evitare di combinare gli stili di combinazione di maiuscole e minuscole.
-   **Per i nomi delle funzionalità e delle tecnologie, è necessario essere conservativi nell'applicazione di maiuscole e minuscole.** In genere, solo i componenti principali devono essere in maiuscolo (usando l'uso di maiuscole e minuscole in stile titolo).
-   **Per i nomi delle funzionalità e delle tecnologie, è necessario essere coerenti nell'in maiuscolo.** Se il nome viene visualizzato più di una volta in una schermata dell'interfaccia utente, dovrebbe sempre apparire nello stesso modo. Analogamente, in tutte le schermate dell'interfaccia utente del programma, il nome deve essere presentato in modo coerente.
-   **Non convertire in maiuscolo i nomi degli elementi dell'interfaccia utente generici,** ad esempio barra degli strumenti, menu, barra di scorrimento, pulsante e icona.
    -   **Eccezioni:** Barra degli indirizzi, barra dei collegamenti, barra multifunzione.
-   **Non usare tutte le lettere maiuscole per i tasti della tastiera.** Seguire invece le maiuscole usate dalle tastiere standard o lettere minuscole se il tasto non è etichettato sulla tastiera.
-   **I puntini di sospensione significano incompletezza.** Usare i puntini di sospensione nel testo dell'interfaccia utente come segue:
    -   **Comandi.** Indicare che un comando richiede informazioni aggiuntive. Non usare i puntini di sospensione ogni volta che un'azione visualizza un'altra finestra, solo quando sono necessarie informazioni aggiuntive. I comandi il cui verbo implicito è mostrare un'altra finestra non accettano puntini di sospensione, ad esempio Avanzate, Guida, Opzioni, Proprietà o Impostazioni.
    -   **Dati.** Indicare che il testo viene troncato.
    -   **Etichette.** Indicare che un'attività è in corso, ad esempio "Ricerca in corso".

**Suggerimento:** Il testo troncato in una finestra o in una pagina con spazio inutilizzato indica un layout insufficiente o dimensioni della finestra predefinite troppo piccole. Cercare layout e dimensioni predefinite delle finestre che eliminano o riducono la quantità di testo troncato. Per altre informazioni, vedere [Layout](vis-layout.md).

-   **Non usare testo blu che non sia un collegamento, perché gli utenti possono presupporre che si tratta di un collegamento.** Usare il grassetto o una sfumatura di grigio in caso contrario si userebbe testo colorato.
-   **Usare il grassetto con parsimonio per attirare l'attenzione sul testo che gli utenti devono leggere.**
-   **Usare l'istruzione principale per spiegare in modo conciso le attività che gli utenti devono eseguire in una determinata finestra o pagina.** Le buone istruzioni principali comunicano l'obiettivo dell'utente anziché concentrarsi solo sulla modifica dell'interfaccia utente.
-   **Esprimere l'istruzione principale sotto forma di una direzione imperativa o di una domanda specifica.**
-   **Non inserire punti alla fine delle etichette di controllo o delle istruzioni principali.**
-   **Usare uno spazio tra le frasi.** Non due.

## <a name="controls"></a>Controlli

-   **Generale**
    -   **Etichettare ogni controllo o gruppo di controlli. Eccezioni:**
        -   Le caselle di testo e gli elenchi a discesa possono essere etichettati usando i prompt.
        -   I controlli subordinati usano l'etichetta del controllo associato. I controlli di selezione sono sempre controlli subordinati.
    -   **Per tutti i controlli, selezionare il valore più sicuro (per evitare la perdita di dati o l'accesso al sistema), il valore più sicuro per impostazione predefinita.** Se la sicurezza e la sicurezza non sono fattori, selezionare il valore più probabile o conveniente.
    -   **Preferisce i controlli vincolati.** Usare controlli vincolati come elenchi e dispositivi di scorrimento quando possibile, anziché controlli non vincolati come caselle di testo, per ridurre la necessità di input di testo.
    -   **Riconsiderare i controlli disabilitati.** I controlli disabilitati possono essere difficili da usare perché gli utenti devono letteralmente dedurre perché sono disabilitati. Disabilitare un controllo quando gli utenti si aspettano che sia applicato e possono dedurre facilmente il motivo per cui il controllo è disabilitato. Rimuovere il controllo quando gli utenti non possono abilitarlo o non si aspettano che sia applicato o lasciarlo abilitato, ma fornire un messaggio di errore quando viene usato in modo non corretto.
        -   **Suggerimento:** Se non si è certi che sia necessario disabilitare un controllo o fornire un messaggio di errore, iniziare componendo il messaggio di errore che è possibile fornire. Se il messaggio di errore contiene informazioni utili che gli utenti di destinazione probabilmente non deducono rapidamente, lasciare il controllo abilitato e specificare l'errore. In caso contrario, disabilitare il controllo .
-   **Pulsanti di comando**
    -   **Preferire etichette specifiche a quelle generiche.** Idealmente, gli utenti non devono leggere altro per comprendere l'etichetta. È molto più probabile che gli utenti leggono le etichette dei pulsanti di comando rispetto al testo statico.
        -   **Eccezione:** Non rinominare il pulsante Annulla se il significato di annulla non è ambiguo. Gli utenti non devono leggere tutti i pulsanti per determinare quale pulsante annulla un'azione. Tuttavia, rinominare Annulla se non è chiaro quale azione viene annullata, ad esempio quando sono presenti diverse azioni in sospeso.
    -   **Quando si pone una domanda, usare etichette corrispondenti alla domanda.** Ad esempio, fornire risposte Sì e No a una domanda sì o no.
    -   **Non usare i pulsanti Applica nelle finestre di dialogo che non sono finestre delle proprietà o elementi del Pannello di controllo.** Il pulsante Applica significa applicare le modifiche in sospeso, ma lasciare aperta la finestra. In questo modo gli utenti possono valutare le modifiche prima di chiudere la finestra. Tuttavia, solo le finestre delle proprietà e gli elementi del Pannello di controllo hanno questa necessità.
    -   Etichettare un pulsante Annulla se l'annullamento riporta l'ambiente allo stato precedente (senza alcun effetto collaterale); In caso contrario, etichettare il pulsante Chiudi (se l'operazione è stata completata) o Arresta (se l'operazione è in corso) per indicare che lascia intatto lo stato modificato corrente.
-   **Collegamenti di comando**
    -   **Presentare sempre i collegamenti di comando in un set di due o più elementi.** Logicamente, non c'è alcun motivo per porre una domanda che abbia una sola risposta.
    -   **Specificare un pulsante Annulla esplicito.** Non usare un collegamento di comando a questo scopo. Spesso gli utenti si rendono conto di non voler eseguire un'attività. L'uso di un collegamento di comando per annullare richiederebbe agli utenti di leggere attentamente tutti i collegamenti di comando per determinare quale significa annullare. La presenza di un pulsante Annulla esplicito consente agli utenti di annullare un'attività in modo efficiente.
    -   **Se specificando un pulsante Annulla esplicito si lascia un singolo collegamento di comando, specificare sia un collegamento di comando da annullare che un pulsante Annulla.** In questo modo è chiaro che gli utenti hanno la possibilità di scegliere. Formulare questo collegamento di comando in termini di differenza rispetto alla prima risposta, anziché semplicemente "Cancel" o alcune variazioni.
-   **Caselle di controllo "Non visualizzare \<item\> più questo messaggio"**
    -   **È consigliabile usare un'opzione "Non visualizzare più questo messaggio" per consentire agli utenti di eliminare una finestra di dialogo ricorrente, solo se non esiste \<item\> un'alternativa migliore.** È sempre meglio visualizzare la finestra di dialogo se gli utenti ne hanno effettivamente bisogno o semplicemente eliminarla in caso contrario.
    -   **Sostituire \<item\> con l'elemento specifico.** Ad esempio, Non visualizzare più questo promemoria. Quando si fa riferimento a una finestra di dialogo in generale, usare Non visualizzare più questo messaggio.
    -   **Indicare chiaramente quando verrà usato l'input** dell'utente per i valori predefiniti futuri aggiungendo la frase seguente sotto l'opzione : Le selezioni verranno usate per impostazione predefinita in futuro.
    -   **Non selezionare l'opzione per impostazione predefinita. Se la finestra di dialogo deve essere effettivamente visualizzata una sola volta, eseguire questa operazione senza chiedere conferma.** Non usare questa opzione per infastidire gli utenti. Assicurarsi che il comportamento predefinito non sia fastidioso.
    -   **Se gli utenti selezionano l'opzione e fa clic su Annulla, questa opzione ha effetto.** Questa impostazione è una meta-opzione, quindi non segue il comportamento standard di annullamento di senza lasciare alcun effetto collaterale. Si noti che se gli utenti non vogliono visualizzare il dialogo in futuro, è probabile che vogliano annullarlo.
-   **Collegamenti**
    -   **Non assegnare una chiave** [di accesso](glossary.md). È possibile accedere ai collegamenti usando il tasto TAB.
    -   **Non aggiungere "Click" o "Click here" al testo del collegamento.** Non è necessario perché un collegamento implica il clic.
-   **Descrizioni comandi**
    -   **Usare le descrizioni comando per fornire etichette per i controlli senza etichetta.** Non è necessario assegnare descrizioni comando ai controlli etichettati semplicemente per motivi di coerenza.
    -   **Le descrizioni comando possono anche fornire maggiori dettagli per i pulsanti della barra degli strumenti etichettati, se questa operazione è utile.** Non solo ripetere o fornire una rieificazione di ciò che è già presente nell'etichetta.
    -   **Evitare di coprire l'oggetto che l'utente sta per visualizzare o con cui interagire.** Posizionare sempre la mancia sul lato dell'oggetto, anche se ciò richiede la separazione tra il puntatore e la mancia. Una separazione non è un problema, purché la relazione tra l'oggetto e la relativa mancia sia chiara.
        -   **Eccezione:** Descrizioni comando con nome completo usate in elenchi e alberi.
    -   **Per le raccolte di elementi, evitare di coprire l'oggetto successivo che l'utente probabilmente visualizza o con cui interagisce.** Per gli elementi disposti orizzontalmente, evitare di posizionare le mance a destra; per gli elementi disposti verticalmente, evitare di inserire suggerimenti di seguito.
-   **Rivelazione progressiva**
    -   **Usare i pulsanti More/Fewer progressive disclosure (Più/Meno di diffusione progressiva) per nascondere opzioni, comandi e dettagli avanzati o usati raramente che in genere non sono necessari agli utenti.** Non nascondere gli elementi di uso comune, perché gli utenti potrebbero non trovarli. Assicurarsi tuttavia che qualsiasi elemento nascosto abbia un valore.
    -   Se la superficie visualizza sempre alcune opzioni, comandi o dettagli, usare le coppie di etichette seguenti:
        -   **Più/Meno opzioni.** Usare per le opzioni o una combinazione di opzioni, comandi e dettagli.
        -   **Più/Meno comandi.** Usare solo per i comandi .
        -   **Più o meno dettagli.** Usare solo per le informazioni.
        -   **Più o meno \<object name\> .** Usare per altri tipi di oggetto, ad esempio le cartelle.
    -   In caso contrario:
        -   **Opzioni Mostra/Nascondi.** Usare per le opzioni o una combinazione di opzioni, comandi e dettagli.
        -   **Mostra/Nascondi comandi.** Usare solo per i comandi .
        -   **Mostra/Nascondi dettagli.** Usare solo per le informazioni.
        -   **Mostra/Nascondi \<object name\> .** Usare per altri tipi di oggetto, ad esempio le cartelle.
-   **Barre di stato**
    -   **Usare gli indicatore di stato determinati** per le operazioni che richiedono una quantità di tempo delimitata, anche se tale quantità di tempo non può essere stimata in modo accurato. Gli barre di stato indeterminati indicano lo stato di avanzamento in corso, ma non forniscono altre informazioni. Non scegliere un indicatore di stato indeterminato basato solo sulla possibile mancanza di accuratezza.
    -   **Fornire una stima del tempo rimanente se è possibile farlo in modo accurato.** Le stime del tempo rimanente che sono accurate sono utili, ma non sono utili le stime che sono fuori dal segno o che si aggirano in modo significativo. Potrebbe essere necessario eseguire alcune operazioni di elaborazione prima di poter fornire stime accurate. In questo caso, non visualizzare stime potenzialmente imprecise durante questo periodo iniziale.
    -   **Non riavviare lo stato di avanzamento.** Un indicatore di stato perde il valore se viene riavviato (ad esempio perché viene completato un passaggio dell'operazione) perché gli utenti non hanno modo di sapere quando l'operazione verrà completata. Al contrario, fare in modo che tutti i passaggi dell'operazione contitino una parte dello stato di avanzamento e che l'indicatore di stato passi al completamento una sola volta.
    -   **Fornire dettagli utili sullo stato di avanzamento.** Fornire informazioni aggiuntive sullo stato di avanzamento, ma solo se gli utenti possono eseguire un'operazione. Assicurarsi che il testo sia visualizzato per un periodo di tempo sufficiente per consentire agli utenti di leggerlo.
    -   **Non combinare un indicatore di stato con un puntatore occupato.** Usare uno o l'altro, ma non entrambi contemporaneamente.
-   **Prompt**
    -   **Usare un prompt quando lo spazio sullo schermo** è così elevato che l'uso di un'etichetta o di un'istruzione è indesiderato, ad esempio su una barra degli strumenti.
    -   **La richiesta è principalmente per identificare lo scopo della casella di testo o della casella combinata in modo compatto.** Non devono essere informazioni cruciali che l'utente deve visualizzare durante l'uso del controllo .
    -   **Il testo della richiesta non deve essere confuso con il testo reale.** Per eseguire questa operazione:
        -   Disegnare il testo di richiesta in grigio corsivo e il testo di input effettivo in nero.
        -   Il testo del prompt non deve essere modificabile e deve scomparire quando gli utenti fa clic o compaiono nella casella di testo.
            -   **Eccezione:** Se la casella di testo ha lo stato attivo per l'input predefinito, la richiesta viene visualizzata e scompare quando l'utente inizia a digitare.
    -   Non usare la punteggiatura finale o i puntini di sospensione.
-   **Notifications**
    -   **Usare le notifiche per gli eventi che non sono correlati all'attività utente corrente, non richiedono un'azione immediata dell'utente e gli utenti possono ignorare liberamente.**
    -   **Non utilizzare le notifiche in modo improprio:**
        -   **Usare le notifiche solo se necessario.** Quando si visualizza una notifica, si potrebbero interrompere gli utenti o addirittura disturbarli. Assicurarsi che l'interruzione sia giustificata.
        -   **Usare le notifiche per eventi non critici o situazioni che non richiedono un'azione immediata dell'utente.** Per eventi critici o situazioni che richiedono un'azione immediata dell'utente, usare un elemento alternativo dell'interfaccia utente, ad esempio una finestra di dialogo modale.
        -   **Non usare le notifiche per gli annunci di funzionalità.**

## <a name="keyboard"></a>Tastiera

-   **Assegnare lo stato attivo per l'input** iniziale al controllo con cui è più probabile che gli utenti interagiscano per primi, che spesso è il primo controllo interattivo. Se il primo controllo interattivo non è una scelta ottimale, è consigliabile modificare il layout della finestra.
-   **Assegnare tabulazioni a tutti i controlli interattivi, incluse le caselle di modifica di sola lettura. Eccezioni:**
    -   Raggruppare set di controlli correlati che si comportano come un singolo controllo, ad esempio i pulsanti di opzione. Tali gruppi hanno una singola tabulazione.
    -   Contenere correttamente i gruppi in modo che i tasti di direzione esercitino il ciclo avanti e indietro all'interno del gruppo e rimangano all'interno del gruppo.
-   **L'ordine di tabulazione deve scorrere da sinistra a destra, dall'alto verso il basso.** In genere, l'ordine di tabulazione deve seguire l'ordine di lettura. Prendere in considerazione la possibilità di creare eccezioni per i controlli di uso comune inserendoli in precedenza nell'ordine di tabulazione. Tab deve scorrere tutte le tabulazioni in entrambe le direzioni senza arrestarsi. All'interno di un gruppo, l'ordine di tabulazione deve essere in ordine sequenziale, senza eccezioni.
-   **All'interno di una tabulazione, l'ordine dei tasti di** direzione deve scorrere da sinistra a destra, dall'alto verso il basso, senza eccezioni. I tasti di direzione devono scorrere tutti gli elementi in entrambe le direzioni senza arrestarsi.
-   **Presentare i pulsanti di commit nell'ordine seguente:**
    -   OK/ \[ Eseguire \] l'operazione /Sì
    -   \[Non eseguire questa operazione \] /No
    -   Annulla
    -   Applica (se presente)

dove \[ Do it e \] \[ Don't do it \] sono risposte specifiche all'istruzione principale.

-   **Non confondere i tasti di scelta rapida con i tasti di scelta rapida.** I tasti di scelta rapida e i tasti di scelta rapida forniscono l'accesso tramite tastiera all'interfaccia utente, ma hanno scopi e linee guida diversi.
-   **Quando possibile, assegnare chiavi di accesso univoche a tutti i controlli interattivi o alle relative etichette.** [Le caselle di testo di sola](ctrl-text-boxes.md) lettura sono controlli interattivi (perché gli utenti possono scorrerle e copiare testo), quindi traggono vantaggio dai tasti di scelta. **Non assegnare chiavi di accesso a:**
    -   Pulsanti OK, Annulla e Chiudi. I tasti invio e ESC vengono usati per le chiavi di accesso. Tuttavia, assegnare sempre un tasto di scelta a un controllo che indica OK o Annulla, ma con un'etichetta diversa.
-   **Assegnare i tasti di scelta rapida ai comandi usati più di frequente.** I programmi e le funzionalità usati raramente non necessitano di tasti di scelta rapida perché gli utenti possono usare i tasti di scelta.
-   **Non creare un tasto di scelta rapida come unico modo per eseguire un'attività.** Gli utenti devono anche essere in grado di usare il mouse o la tastiera con tab, freccia e tasti di scelta.
-   **Non assegnare significati diversi a tasti di scelta rapida noti.** Poiché sono memorizzati, significati incoerenti per le scelte rapide note sono frustranti e erre.
-   **Non provare ad assegnare tasti di scelta rapida del programma a livello di sistema.** I tasti di scelta rapida del programma avranno effetto solo quando il programma ha lo stato attivo per l'input.

## <a name="mouse"></a>Mouse

-   **Non richiedere mai agli utenti di fare clic su un oggetto per determinare se è selezionabile.** Gli utenti devono essere in grado di determinare la possibilità di fare clic solo tramite l'ispezione visiva.
    -   L'interfaccia utente primaria, ad esempio i pulsanti di commit, deve avere un'opzione click affordance statica. Gli utenti non devono passare il mouse per individuare l'interfaccia utente primaria.
    -   L'interfaccia utente secondaria, ad esempio comandi secondari o controlli di divulgazione progressiva, può visualizzare il proprio clic al passaggio del mouse.
    -   I collegamenti di testo dovrebbero suggerire in modo statico il testo del collegamento e quindi visualizzare il relativo clic (sottolineatura o altra modifica della presentazione, con il puntatore a forma di mano) al passaggio del mouse.
    -   I collegamenti grafici visualizzano solo un puntatore a forma di mano al passaggio del mouse.
-   **Usare il puntatore a forma di mano (o "selezione collegamento") solo per i collegamenti di testo e di grafica.** In caso contrario, gli utenti devono fare clic sugli oggetti per determinare se sono collegamenti.

## <a name="dialog-boxes"></a>Finestre di dialogo

-   **Le finestre di dialogo modali richiedono l'interazione, quindi usarle per gli elementi a cui gli utenti devono rispondere prima di continuare con l'attività.** Assicurarsi che l'interruzione sia giustificata, ad esempio per attività critiche o poco frequenti che richiedono il completamento. In caso contrario, prendere in considerazione alternative non modali.
-   **Le finestre di dialogo non modali non richiedono l'interazione, quindi usarle quando gli utenti devono passare da una finestra di dialogo a una finestra di dialogo e dalla finestra proprietaria.** Sono più usati per attività frequenti, ripetitive o in corso. Tuttavia, le barre multifunzione, le barre degli strumenti e le finestre della tavolozza sono spesso alternative migliori.

## <a name="property-sheets"></a>Finestre delle proprietà

-   **Assicurarsi che le proprietà siano necessarie.** Non ingombrare le pagine delle proprietà con proprietà non necessarie solo per evitare decisioni di progettazione difficili.
-   **Presentare le proprietà in termini di obiettivi utente anziché di tecnologia.** Solo perché una proprietà configura una tecnologia specifica non significa che è necessario presentare la proprietà in termini di tale tecnologia.
    -   Se è necessario presentare le impostazioni in termini di tecnologia (ad esempio perché gli utenti riconoscono il nome della tecnologia), includere una breve descrizione del vantaggio utente.
-   **Usare etichette di tabulazione specifiche e significative.** Evitare etichette di tabulazione generiche che potrebbero essere applicate a qualsiasi scheda, ad esempio Generale, Avanzate o Impostazioni.
-   **Evitare le pagine Generali.** Non è necessario avere una pagina Generale. Usare una pagina Generale solo se:
    -   Le proprietà si applicano a diverse attività e sono significative per la maggior parte degli utenti. Non inserire proprietà specializzate o avanzate in una pagina Generale, ma è possibile renderle accessibili tramite un pulsante di comando nella pagina Generale.
    -   Le proprietà non rientrano in una categoria più specifica. In caso contrario, usare tale nome per la pagina.
-   **Evitare pagine avanzate.** Usare una pagina Avanzate solo se:
    -   Le proprietà si applicano ad attività non comuni e sono significative principalmente per gli utenti avanzati.
    -   Le proprietà non rientrano in una categoria più specifica. In caso contrario, usare tale nome per la pagina.
-   **Non usare le schede se una finestra delle proprietà ha una sola scheda e non è estendibile.** Usare una normale finestra di dialogo con OK, Annulla e un pulsante Applica facoltativo. Tuttavia, le finestre delle proprietà estensibili (che possono essere estese da terze parti) devono usare schede.

## <a name="wizards"></a>Procedure guidate

-   **Considerare prima di tutto alternative leggere, ad esempio finestre di dialogo, riquadri attività o singole pagine.** Le procedure guidate sono un'interfaccia utente pesante, usata meglio per attività in più passaggi e eseguite raramente. Non è necessario usare le procedure guidate. È possibile fornire informazioni e assistenza utili in qualsiasi interfaccia utente.
-   **Usare Avanti solo quando si avanza alla pagina successiva senza impegno.** L'avanzamento alla pagina successiva viene considerato un impegno quando il relativo effetto non può essere annullato facendo clic su Indietro o Annulla.
-   **Usare Indietro solo per correggere gli errori.** Oltre a correggere gli errori, gli utenti non devono fare clic su Indietro per eseguire lo stato di un'attività.
-   **Quando gli utenti emettono il commit in un'attività, usare un pulsante di commit che rappresenta una risposta specifica all'istruzione principale, ad esempio Stampa, Connessione o Avvia.** Non usare etichette generiche come Next (che non implica l'impegno) o Finish (che non è specifico) per il commit di un'attività. Le etichette su questi pulsanti di commit dovrebbero avere senso da soli. Avviare sempre le etichette dei pulsanti di commit con un verbo. **Eccezioni:**
    -   Usare Fine quando le risposte specifiche sono ancora generiche, ad esempio Salva, Seleziona, Scegli o Ottieni.
    -   Usare Fine per modificare un'impostazione specifica o una raccolta di impostazioni.
-   **Usare i collegamenti ai comandi solo per le scelte, non per gli impegni.** Pulsanti di commit specifici indicano un impegno molto migliore rispetto ai collegamenti di comando in una procedura guidata.
-   **Quando si usano i collegamenti di comando, nascondere il pulsante Avanti, ma lasciare il pulsante Annulla.**
-   **Usare Chiudi per le Follow-Up e completamento.** Non usare Annulla perché la chiusura della finestra non abbandonerà le modifiche o le azioni eseguite a questo punto. Non usare Done perché non è un verbo imperativo.
-   **Non usare la "procedura guidata" nei nomi delle procedure guidate.** Ad esempio, usare "Connessione a una rete" anziché "Rete Installazione guidata". È tuttavia accettabile fare riferimento alle procedure guidate come procedure guidate. Ad esempio: "Se si configura una rete per la prima volta, è possibile ottenere assistenza usando la procedura guidata Connessione a una rete".
-   **Mantenere le selezioni dell'utente tramite la navigazione.** Ad esempio, se l'utente apporta modifiche, fa clic su Indietro e quindi su Avanti, tali modifiche devono essere mantenute. Gli utenti non si aspettano di immettere di nuovo le modifiche a meno che non scelsino esplicitamente di cancellarle.

## <a name="wizard-pages"></a>Pagine della procedura guidata

-   **Concentrarsi sul processo decisionale efficiente.** Ridurre il numero di pagine per concentrarsi sulle informazioni di base. Consolidare le pagine correlate e prendere le pagine facoltative dal flusso principale. Fare in modo che gli utenti possano fare clic su Avanti completamente tramite la procedura guidata all'inizio può sembrare una buona esperienza, ma se gli utenti non devono mai modificare le impostazioni predefinite, le pagine probabilmente non sono necessarie.
-   **Non usare le pagine di benvenuto: rendere la prima pagina funzionante quando possibile.** Usare una pagina Attività iniziali facoltativa solo quando:
    -   La procedura guidata presenta i prerequisiti necessari per completare correttamente la procedura guidata.
    -   Gli utenti potrebbero non comprendere lo scopo della procedura guidata in base alla prima pagina Scelta e non c'è spazio per altre spiegazioni.
    -   L'istruzione principale per Attività iniziali pagine è "Prima di iniziare:".
-   **Nelle pagine in cui agli utenti viene richiesto di effettuare scelte, ottimizzare per i casi più probabili.** Questi tipi di pagine devono presentare scelte effettive, non solo istruzioni.
    -   Se non si usa una pagina Attività iniziali, spiegare lo scopo della procedura guidata nella parte superiore della prima pagina di scelte.
-   **Usare le pagine Commit per chiarire quando gli utenti emettono il commit dell'attività.** In genere la pagina Commit è l'ultima pagina di scelte e il pulsante Avanti viene rietichettato per indicare l'attività di cui viene eseguito il commit.
    -   Non usare pagine di riepilogo che riepilogano semplicemente le selezioni precedenti dell'utente, a meno che l'attività non sia rischiosa (che implica sicurezza o perdita di tempo o denaro) o non vi sia una buona probabilità che gli utenti non comprendano le selezioni e non necessitino di esaminarle.
-   **Non usare pagine di congratulazioni che non ese singole terminano la procedura guidata.** Se i risultati della procedura guidata sono chiaramente evidenti per gli utenti, è sufficiente chiudere la procedura guidata sul pulsante commit finale.
    -   Usare Follow-Up quando è probabile che gli utenti eseguano attività correlate come follow-up. Evitare attività di follow-up familiari, ad esempio "Inviare un messaggio di posta elettronica".
    -   Usare le pagine di completamento solo quando i risultati non sono visibili e non esiste un modo migliore per fornire commenti e suggerimenti per il completamento delle attività.
    -   Le procedure guidate con pagine Progress devono usare una pagina Completamento o Follow-Up per indicare il completamento dell'attività. Per le attività con esecuzione lunga, chiudere la procedura guidata nella pagina Commit e usare le notifiche per inviare commenti e suggerimenti.

## <a name="error-messages"></a>messaggi di errore

-   **Non inviare messaggi di errore quando è** probabile che gli utenti non esercitino un'azione o ne cambino il comportamento come risultato del messaggio. Se non è possibile eseguire alcuna azione da parte degli utenti o se il problema non è significativo, eliminare il messaggio di errore.
-   **Quando possibile, proporre una soluzione in modo che gli utenti possano risolvere il problema.** Tuttavia, assicurarsi che la soluzione proposta sia in grado di risolvere il problema. Non sprecare tempo per gli utenti suggerendo soluzioni possibili, ma improbabili.
-   **Essere specifici.** Evitare formulazioni erre, ad esempio errori di sintassi e operazioni non valida. Specificare nomi, posizioni e valori specifici degli oggetti coinvolti.
-   **Non usare formulazioni che incolpano l'utente o implicano un errore dell'utente.** Evitare di usare l'utente e nella formulazione. Anche se la voce attiva è generalmente preferita, usare la voce passiva quando l'utente è il soggetto e potrebbe essere incolpata per l'errore se è stata usata la voce attiva.
-   **Non usare OK per i messaggi di errore.** Gli utenti non visualizzano gli errori come OK. Se il messaggio di errore non ha alcuna azione diretta, usare close.
-   **Non usare le parole seguenti:**
    -   Errore, errore (usare invece un problema)
    -   Non riuscito a (non è possibile usare in alternativa)
    -   Non valido, non valido, non valido (usare invece un valore non corretto o non valido)
    -   Interrompere, terminare, terminare (usare invece stop)
    -   Irreversibile, irreversibile (usare invece grave)

Questi termini non sono necessari e contraddificano il tono di Windows. Al contrario, un'icona di errore, se [usata correttamente,](vis-std-icons.md)comunica sufficientemente che si è verificato un problema.

-   **Non accompagnare i messaggi di errore con effetti sonori.** Questa operazione è insoddura e non necessaria.

## <a name="warning-messages"></a>Messaggi di avviso

-   **Gli avvisi descrivono una condizione che potrebbe causare un problema in futuro.** Gli avvisi non sono errori o domande, quindi non formulare domande di routine come avvisi.
-   **Non inviare messaggi di avviso quando è probabile che gli utenti non esercitino un'azione o ne cambino il comportamento come risultato del messaggio.** Se gli utenti non possono eseguire alcuna azione o se la condizione non è significativa, eliminare il messaggio di avviso.

## <a name="confirmations"></a>Conferme

-   **Non usare conferme non necessarie.** Usare le conferme solo quando:
    -   C'è un motivo chiaro per non procedere e una ragionevole probabilità che a volte gli utenti non lo siano.
    -   L'azione ha conseguenze significative o non può essere facilmente annullata.
    -   L'azione ha conseguenze di cui gli utenti potrebbero non essere a conoscenza.
    -   Per procedere con l'azione, gli utenti devono effettuare una scelta che non ha un valore predefinito appropriato.
    -   Dato il contesto corrente, è probabile che gli utenti abbia eseguito un'azione in errore.
-   **Conferme di frasi come una domanda sì o no e forniscono risposte sì o no.** A differenza di altri tipi di finestre di dialogo, le conferme sono progettate per impedire agli utenti di prendere decisioni rapide. Se gli utenti non mettono in considerazione la risposta, una conferma non ha alcun valore.

## <a name="icons"></a>Icone

-   **Tutte le icone devono essere conformi alle linee** guida per le icone in stile [Aereo.](vis-icons.md) Sostituire tutte Windows icone in stile XP.
-   **Scegliere le icone standard in base al tipo di messaggio, non alla gravità del problema sottostante:**
    -   **Errore.** Errore o problema che si è verificato.
    -   **Avviso.** Condizione che potrebbe causare un problema in futuro.
    -   **Informazioni.** Informazioni utili.

Se un problema combina tipi di messaggio diversi, concentrarsi sull'aspetto più importante su cui gli utenti devono intervenire.

-   **Le icone devono sempre corrispondere all'istruzione principale o a un altro testo corrispondente.**
-   **Le icone di errore non sono necessarie per i problemi di input utente non critici.** Tuttavia, le icone sono necessarie per gli errori sul posto, perché in caso contrario tale feedback contestuale sarebbe troppo facile da tralasciare.
-   **Non usare icone di avviso per "attenuare" gli errori non critici.** Gli errori non sono avvisi. Applicare invece le linee guida per le icone di errore.
-   **Per le finestre di dialogo delle domande, usare le icone di avviso solo per le domande con conseguenze significative.** Non usare icone di avviso per le domande di routine.

## <a name="help"></a>Help

-   **Collegamento ad argomenti specifici della Guida pertinenti.** Non collegarsi alla guida home page, al sommario, a un elenco di risultati della ricerca o a una pagina che si collega solo ad altre pagine. Evitare il collegamento a pagine strutturate come un ampio elenco di domande frequenti, perché impone agli utenti di cercare quella corrispondente al collegamento su cui hanno fatto clic. Non collegare argomenti della Guida specifici che non sono rilevanti e utili per l'attività in fase di esecuzione. Non collegarsi mai a pagine vuote.
-   **Non inserire collegamenti alla Guida in ogni finestra o pagina per motivi di coerenza.** Fornire un collegamento alla Guida in un'unica posizione non significa che è necessario fornirli ovunque.
-   **Quando possibile, la guida alle frasi collega il testo in termini di domanda principale a cui risponde il contenuto della Guida.** Non usare la formulazione "Altre informazioni su" o "Ottenere assistenza per questo".
-   **Usare l'intero collegamento alla Guida per il testo del collegamento,** non solo le parole chiave.
-   **Usare frasi complete.**
-   **Non usare la punteggiatura finale o i puntini di sospensione, ad eccezione dei punti interrogativi.**
-   **Se il contenuto della Guida è online, renderlo chiaro nel testo del collegamento.** Questa operazione consente di rendere prevedibile il risultato dei collegamenti.

