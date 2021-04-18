---
title: Elenco di controllo UX per applicazioni desktop
description: Ecco una raccolta di alcune delle principali linee guida disponibili nella Guida all'esperienza utente. È possibile usarlo come elenco di controllo per assicurarsi che l'interfaccia utente del programma ottenga questi elementi importanti a destra.
ms.assetid: 4705a807-5949-4957-8ea6-70871beaf8e0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d1006b7ad9de30941b6ceb4cc7282ec578450840
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/25/2021
ms.locfileid: "106333990"
---
# <a name="ux-checklist-for-desktop-applications"></a>Elenco di controllo UX per applicazioni desktop

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Ecco una raccolta di alcune delle principali linee guida disponibili nella Guida all'esperienza utente. È possibile usarlo come elenco di controllo per assicurarsi che l'interfaccia utente del programma ottenga questi elementi importanti a destra.

## <a name="windows"></a>Windows

-   **Supporta la risoluzione minima di Windows per 800x600 pixel.** Per le interfacce utente critiche (UI) che devono funzionare in modalità provvisoria, supportare una [risoluzione efficace](glossary.md) di 640x480 pixel. Assicurarsi di tenere conto dello spazio usato dalla barra delle applicazioni riservando 48 [pixel relativi](glossary.md) per le finestre visualizzate con la barra delle applicazioni.
-   **Ottimizzare il layout delle finestre ridimensionabili per una risoluzione efficace di 1024x768 pixel.** Ridimensionare automaticamente le finestre per risoluzioni dello schermo inferiori in modo ancora funzionante.
-   **Assicurarsi di testare le finestre in modalità 96 punti per pollice (dpi) (a 800x600 pixel), 120 dpi (a 1024x768 pixel) e 144 dpi (a 1200x900 pixel).** Verificare la presenza di problemi di layout, ad esempio il ritaglio di controlli, testo e finestre, nonché l'estensione delle icone e delle bitmap.
-   **Per i programmi con scenari di utilizzo tocco e dispositivi mobili, ottimizzarli per 120 dpi.** Le schermate ad alta risoluzione sono attualmente prevalentemente nei PC portatili e a tocco.
-   **Se una finestra è una finestra di proprietà, visualizzarla inizialmente "centrata" nella parte superiore della finestra proprietaria.** Mai sotto. Per la visualizzazione successiva, provare a visualizzarla nell'ultima posizione, relativa alla finestra proprietaria, se questa operazione è probabilmente più pratica.
-   **Se una finestra è contestuale, visualizzarla sempre accanto all'oggetto da cui è stata avviata.** Tuttavia, posizionarlo fuori dalla modalità (preferibilmente offset verso il basso e verso destra) in modo che l'oggetto non sia coperto dalla finestra.

## <a name="layout"></a>Layout

-   **Ridimensionare i controlli e i riquadri in una finestra in modo che corrispondano al contenuto tipico.** Evitare il testo troncato e i relativi ellissi associati. Gli utenti non devono mai interagire con una finestra per visualizzare il contenuto tipico, ovvero riservare il ridimensionamento e lo scorrimento per contenuto insolitamente grande. Controllare in modo specifico:
    -   **Dimensioni del controllo.** Ridimensionare i controlli sul contenuto tipico, rendendoli più ampi, più alti o più righe, se necessario. Ridimensionare i controlli per eliminare o ridurre lo scorrimento in finestre con una quantità di spazio disponibile. Inoltre, non dovrebbero mai essere presenti etichette troncate o testo troncato all'interno di finestre con una quantità di spazio disponibile. Tuttavia, per semplificare la lettura del testo, provare a limitare le larghezze di riga a 65 caratteri.
    -   **Larghezza delle colonne.** Verificare che le colonne della visualizzazione elenco includano il dimensionamento predefinito, minimo e massimo appropriato. Scegliere le visualizzazioni elenco le larghezze delle colonne predefinite che non comportano il troncamento del testo, soprattutto se è disponibile spazio nella visualizzazione elenco.
    -   **Bilanciamento del layout.** Il layout di una finestra deve essere approssimativamente bilanciato. Se il layout è molto elevato, provare a rendere più ampi i controlli e a trasferire alcuni controlli più a destra.
    -   **Ridimensionamento layout.** Quando una finestra è ridimensionabile e i dati vengono troncati, assicurarsi che le dimensioni delle finestre maggiori mostrino più dati. Quando i dati vengono troncati, gli utenti si aspettano di ridimensionare le finestre per visualizzare altre informazioni.
-   **Impostare una dimensione minima della finestra se è presente una dimensione al di sotto della quale il contenuto non è più utilizzabile.** Per i controlli ridimensionabili, impostare dimensioni minime degli elementi ridimensionabili sulle dimensioni funzionali più piccole, ad esempio la larghezza minima delle colonne funzionali nelle visualizzazioni elenco.

## <a name="text"></a>Testo

-   **Quando possibile, utilizzare termini ordinari e colloquiali.** Concentrarsi sugli obiettivi utente, non sulla tecnologia. Questa operazione è particolarmente efficace se si spiega un concetto tecnico o un'azione complessa. Si supponga di dover esaminare la spalla dell'utente e spiegare come eseguire l'attività.
-   **Sii gentile, supportato e incoraggiante.** L'utente non deve mai essere condiscendente, accusato o intimidito.
-   **Rimuovere il testo ridondante.** Cercare il testo ridondante nei titoli delle finestre, le istruzioni principali, le istruzioni aggiuntive, le aree di contenuto, i collegamenti ai comandi e i pulsanti di commit. In genere, lasciare il testo completo nelle istruzioni principali e i controlli interattivi e rimuovere qualsiasi ridondanza dalle altre posizioni.
-   **Usare la capitalizzazione in stile titolo per i titoli e la maiuscola in stile frase per tutti gli altri elementi dell'interfaccia utente.** Questa operazione è più appropriata per il tono di Windows.
    -   **Eccezione:** Per le applicazioni legacy, è possibile usare la capitalizzazione in stile titolo per i pulsanti di comando, i menu e le intestazioni di colonna, se necessario, per evitare di combinare gli stili di maiuscole e minuscole.
-   **Per i nomi delle funzionalità e delle tecnologie, è opportuno tenere in maiuscolo.** In genere, solo i componenti principali devono essere in lettere maiuscole (usando la maiuscola in stile titolo).
-   **Per i nomi delle funzionalità e delle tecnologie, è necessario essere coerenti.** Se il nome viene visualizzato più di una volta in una schermata dell'interfaccia utente, deve sempre apparire allo stesso modo. Analogamente, in tutte le schermate dell'interfaccia utente del programma, il nome deve essere presentato in modo coerente.
-   **Non capitalizzare i nomi degli elementi generici dell'interfaccia utente,** ad esempio barra degli strumenti, menu, barra di scorrimento, pulsante e icona.
    -   **Eccezioni:** Barra degli indirizzi, barra collegamenti, barra multifunzione.
-   **Non usare lettere maiuscole per i tasti di scelta rapida.** Seguire invece le maiuscole usate dalle tastiere standard o minuscole se la chiave non è etichettata sulla tastiera.
-   **I puntini di sospensione indicano l'incompletezza.** Usare i puntini di sospensione nel testo dell'interfaccia utente come segue:
    -   **Comandi.** Indica che per un comando sono necessarie informazioni aggiuntive. Non usare i puntini di sospensione ogni volta che un'azione Visualizza un'altra finestra, solo quando sono necessarie informazioni aggiuntive. I comandi il cui verbo implicito viene visualizzato in un'altra finestra non accettano i puntini di sospensione, ad esempio avanzate, guida, opzioni, proprietà o impostazioni.
    -   **Dati.** Indica che il testo è troncato.
    -   **Etichette.** Indica che è in corso un'attività (ad esempio, "ricerca in corso...").

**Suggerimento:** Il testo troncato in una finestra o in una pagina con spazio inutilizzato indica un layout insufficiente o una dimensione della finestra predefinita troppo piccola. Cercare i layout e le dimensioni predefinite della finestra che eliminano o riducono la quantità di testo troncato. Per altre informazioni, vedere [Layout](vis-layout.md).

-   **Non usare il testo blu che non è un collegamento, perché gli utenti possono supporre che si tratta di un collegamento.** Usare il testo in grassetto o una sfumatura di grigio, in cui altrimenti si userebbe un testo colorato.
-   **Per attirare l'attenzione sul testo, gli utenti devono leggere in grassetto.**
-   **Utilizzare l'istruzione principale per spiegare in modo conciso le operazioni che gli utenti devono eseguire in una determinata finestra o pagina.** Le ottime istruzioni principali comunicano l'obiettivo dell'utente piuttosto che concentrarsi solo sulla modifica dell'interfaccia utente.
-   **Esprimere l'istruzione principale sotto forma di direzione imperativa o domanda specifica.**
-   **Non posizionare i punti alla fine delle etichette dei controlli o delle istruzioni principali.**
-   **Usare uno spazio tra le frasi.** Non due.

## <a name="controls"></a>Controlli

-   **Generale**
    -   **Etichettare ogni controllo o gruppo di controlli. Eccezioni**
        -   Le caselle di testo e gli elenchi a discesa possono essere etichettati usando i prompt.
        -   I controlli subordinati usano l'etichetta del controllo associato. I controlli di selezione sono sempre controlli subordinati.
    -   **Per tutti i controlli selezionare il valore più sicuro (per evitare la perdita di dati o l'accesso al sistema), per impostazione predefinita.** Se la sicurezza e la sicurezza non sono fattori, selezionare il valore più probabile o pratico.
    -   **Preferisce i controlli vincolati.** Usare controlli vincolati come elenchi e dispositivi di scorrimento laddove possibile, anziché controlli non vincolati come caselle di testo, per ridurre la necessità di input di testo.
    -   **Riconsiderare i controlli disabilitati.** I controlli disabilitati possono essere difficili da usare perché gli utenti devono letteralmente dedurre il motivo per cui sono disabilitati. Disabilitare un controllo quando gli utenti si aspettano che venga applicato e possono facilmente dedurre il motivo per cui il controllo è disabilitato. Rimuovere il controllo quando non esiste alcun modo per consentire agli utenti di abilitarlo o non aspettarsi che venga applicato oppure lasciarlo abilitato, ma fornire un messaggio di errore quando viene usato in modo errato.
        -   **Suggerimento:** Se non si è certi che sia necessario disabilitare un controllo o fornire un messaggio di errore, iniziare componendo il messaggio di errore che è possibile fornire. Se il messaggio di errore contiene informazioni utili che gli utenti di destinazione non possono dedurre rapidamente, lasciare il controllo abilitato e fornire l'errore. In caso contrario, disabilitare il controllo.
-   **Pulsanti di comando**
    -   **Preferisci etichette specifiche rispetto a quelle generiche.** Idealmente, gli utenti non devono leggere nient'altro per comprendere l'etichetta. È molto più probabile che gli utenti leggano le etichette dei pulsanti di comando rispetto al testo statico.
        -   **Eccezione:** Non rinominare il pulsante Annulla se il significato dell'annullamento non è ambiguo. Gli utenti non devono leggere tutti i pulsanti per determinare il pulsante che annulla un'azione. Tuttavia, rinominare Annulla se non è chiaro quale azione verrà annullata, ad esempio quando sono presenti diverse azioni in sospeso.
    -   **Quando si pone una domanda, usare le etichette che corrispondono alla domanda.** Ad esempio, fornire risposte sì e no a una domanda sì o no.
    -   **Non usare pulsanti applica nelle finestre di dialogo che non sono finestre delle proprietà o elementi del pannello di controllo.** Il pulsante Applica significa applicare le modifiche in sospeso, ma lasciare aperta la finestra. Questa operazione consente agli utenti di valutare le modifiche prima di chiudere la finestra. Tuttavia, solo le finestre delle proprietà e gli elementi del pannello di controllo hanno questa necessità.
    -   Etichetta un pulsante Annulla se l'annullamento restituisce l'ambiente allo stato precedente (senza effetto collaterale); in caso contrario, etichettare la chiusura del pulsante (se l'operazione è stata completata) o arrestare (se l'operazione è in corso) per indicare che lascia intatto lo stato modificato corrente.
-   **Collegamenti ai comandi**
    -   **Presentare sempre i collegamenti ai comandi in un set di due o più.** Logicamente, non c'è motivo di porre una domanda con una sola risposta.
    -   **Consente di specificare un pulsante Annulla esplicito.** Non usare un collegamento di comando a questo scopo. Abbastanza spesso, gli utenti si rendono conto che non vogliono eseguire un'attività. L'uso di un collegamento al comando per annullare richiede agli utenti di leggere con attenzione tutti i collegamenti ai comandi per determinare quale mezzo annullare. La presenza di un pulsante Annulla esplicito consente agli utenti di annullare un'attività in modo efficiente.
    -   **Se l'inserimento di un pulsante Annulla esplicito lascia un solo collegamento di comando, specificare sia un collegamento di comando da annullare che un pulsante Annulla.** In questo modo è chiaro che gli utenti hanno una scelta. Frase il collegamento del comando in termini di differenze rispetto alla prima risposta, anziché semplicemente "Annulla" o una variante.
-   **Caselle di controllo "non visualizzare più questo messaggio \<item\> "**
    -   **Provare a usare un'opzione "non visualizzare \<item\> più questo messaggio" per consentire agli utenti di disattivare una finestra di dialogo ricorrente, solo se non è disponibile un'alternativa migliore.** È sempre meglio visualizzare la finestra di dialogo se gli utenti ne hanno effettivamente bisogno o semplicemente eliminarla.
    -   **Sostituire \<item\> con l'elemento specifico.** Ad esempio, non visualizzare più questo promemoria. Quando si fa riferimento a una finestra di dialogo in generale, usare non visualizzare più questo messaggio.
    -   **Indica chiaramente quando verrà usato l'input dell'utente per i valori predefiniti futuri** aggiungendo la frase seguente nell'opzione: le selezioni verranno usate per impostazione predefinita in futuro.
    -   **Non selezionare l'opzione per impostazione predefinita. Se la finestra di dialogo deve essere visualizzata una sola volta, eseguire questa operazione senza richiedere.** Non usare questa opzione come scusa per infastidire gli utenti: assicurarsi che il comportamento predefinito non sia fastidioso.
    -   **Se gli utenti selezionano l'opzione e fanno clic su Annulla, questa opzione ha effetto.** Questa impostazione è una meta-opzione, quindi non segue il comportamento di annullamento standard di senza effetto collaterale. Si noti che se gli utenti non vogliono visualizzare la finestra di dialogo in futuro, è molto probabile che vogliano annullarla.
-   **Collegamenti**
    -   **Non assegnare una chiave di** [accesso](glossary.md). Per accedere ai collegamenti, utilizzare il tasto TAB.
    -   **Non aggiungere "click" o "fare clic qui" al testo del collegamento.** Non è necessario perché un collegamento implica la selezione.
-   **Descrizioni comandi**
    -   **Usare le descrizioni comandi per fornire etichette per i controlli senza etichetta.** Non è necessario assegnare descrizioni comandi con etichetta semplicemente per motivi di coerenza.
    -   **Le descrizioni comandi possono inoltre fornire maggiori dettagli per i pulsanti della barra degli strumenti con etichetta se questa operazione è utile.** Non solo ripetere o fornire una riformulazione di parole in cui si trova già nell'etichetta.
    -   **Evitare di coprire l'oggetto con cui l'utente sta per visualizzare o interagire.** Posizionare sempre il suggerimento sul lato dell'oggetto, anche se è necessaria la separazione tra il puntatore e il suggerimento. Una separazione non è un problema, purché la relazione tra l'oggetto e il relativo suggerimento sia chiara.
        -   **Eccezione:** Descrizioni comandi con nome completo utilizzati negli elenchi e negli alberi.
    -   **Per le raccolte di elementi, evitare di coprire l'oggetto successivo che è probabile che l'utente possa visualizzare o interagire con.** Per gli elementi disposti orizzontalmente, evitare di posizionare i suggerimenti a destra; per gli elementi disposti verticalmente, evitare di inserire i suggerimenti seguenti.
-   **Rivelazione progressiva**
    -   **Usare pulsanti di divulgazione progressivi più o meno avanzati per nascondere le opzioni, i comandi e i dettagli usati o raramente usati dagli utenti in genere.** Non nascondono gli elementi usati comunemente, perché gli utenti potrebbero non trovarli. Tuttavia, verificare che sia presente un valore nascosto.
    -   Se la superficie Visualizza sempre alcune opzioni, comandi o dettagli, usare le coppie di etichette seguenti:
        -   **Opzioni più o meno.** Usare per le opzioni o una combinazione di opzioni, comandi e dettagli.
        -   **Comandi più o meno.** Usare solo per i comandi.
        -   **Dettagli più o meno.** Utilizzare solo per informazioni.
        -   **Più o meno \<object name\> .** Utilizzare per altri tipi di oggetto, ad esempio cartelle.
    -   In caso contrario:
        -   **Mostra/Nascondi opzioni.** Usare per le opzioni o una combinazione di opzioni, comandi e dettagli.
        -   **Mostra/Nascondi comandi.** Usare solo per i comandi.
        -   **Mostra/Nascondi dettagli.** Utilizzare solo per informazioni.
        -   **Mostra/Nascondi \<object name\> .** Utilizzare per altri tipi di oggetto, ad esempio cartelle.
-   **Indicatori di stato**
    -   **Utilizzare gli indicatori di stato determinati per le operazioni che richiedono un periodo di tempo limitato,** anche se non è possibile prevedere accuratamente tale periodo di tempo. Gli indicatori di stato indeterminati mostrano che lo stato di avanzamento viene effettuato, ma non forniscono altre informazioni. Non scegliere un indicatore di stato indeterminato in base solo alla possibile mancanza di precisione.
    -   **Fornire una stima del tempo rimanente se è possibile eseguire questa operazione in modo accurato.** Le stime del tempo rimanenti accurate sono utili, ma le stime che si trovano fuori dal contrassegno o rimbalzano in modo significativo non sono utili. Prima di poter assegnare stime accurate, potrebbe essere necessario eseguire alcune operazioni di elaborazione. In tal caso, non visualizzare stime potenzialmente non accurate durante questo periodo iniziale.
    -   **Non riavviare lo stato di avanzamento.** Un indicatore di stato perde il suo valore se viene riavviato (forse perché un passaggio nell'operazione viene completato) perché gli utenti non hanno modo di sapere quando l'operazione verrà completata. Al contrario, tutti i passaggi dell'operazione condividono una parte dello stato di avanzamento e l'indicatore di stato passa al completamento una volta.
    -   **Fornire dettagli utili sullo stato di avanzamento.** Fornire informazioni aggiuntive sullo stato di avanzamento, ma solo se gli utenti possono eseguire un'operazione. Verificare che il testo venga visualizzato abbastanza a lungo da consentire agli utenti di leggerlo.
    -   **Non combinare un indicatore di stato con un puntatore occupato.** Usare uno o l'altro, ma non entrambi contemporaneamente.
-   **Prompt**
    -   **Utilizzare un messaggio di richiesta quando lo spazio dello schermo è a un livello Premium che l'utilizzo di un'etichetta o di un'istruzione è indesiderato,** ad esempio su una barra degli strumenti
    -   **Il prompt viene principalmente utilizzato per identificare in modo compatto lo scopo della casella di testo o della casella combinata.** Non devono essere informazioni cruciali che l'utente deve visualizzare durante l'uso del controllo.
    -   **Il testo della richiesta non deve essere confuso con il testo reale.** Per eseguire questa operazione:
        -   Creare il testo della richiesta in grigio corsivo e il testo di input effettivo in nero romano.
        -   Il testo della richiesta non deve essere modificabile e dovrebbe scomparire quando gli utenti fanno clic nella casella di testo o nella scheda.
            -   **Eccezione:** Se la casella di testo ha lo stato attivo per l'input predefinito, il prompt viene visualizzato e scompare una volta che l'utente inizia a digitare.
    -   Non usare la punteggiatura finale o i puntini di sospensione.
-   **Notifications**
    -   **Usare le notifiche per gli eventi che non sono correlati all'attività dell'utente corrente, non richiedono un'azione immediata da parte dell'utente e gli utenti possono ignorarli liberamente.**
    -   **Non usare le notifiche:**
        -   **Usare le notifiche solo se necessario.** Quando si visualizza una notifica, si sta potenzialmente interrompendo gli utenti o addirittura fastidioso. Verificare che l'interruzione sia giustificata.
        -   **Usare le notifiche per eventi o situazioni non critiche che non richiedono un'azione immediata dell'utente.** Per gli eventi critici o le situazioni che richiedono un'azione immediata dell'utente, usare un elemento dell'interfaccia utente alternativo, ad esempio una finestra di dialogo modale.
        -   **Non usare notifiche per gli annunci di funzionalità.**

## <a name="keyboard"></a>Tastiera

-   **Assegnare lo stato attivo per l'input iniziale al controllo che gli utenti con maggiore probabilità interagiranno prima,** che è spesso il primo controllo interattivo. Se il primo controllo interattivo non è una scelta ottimale, provare a modificare il layout della finestra.
-   **Assegna tabulazioni si arresta a tutti i controlli interattivi, incluse le caselle di modifica di sola lettura. Eccezioni**
    -   Gruppi di gruppi di controlli correlati che si comportano come un unico controllo, ad esempio i pulsanti di opzione. Tali gruppi hanno una singola tabulazione.
    -   Contenere correttamente i gruppi in modo che i tasti di direzione siano in avanti e indietro all'interno del gruppo e restino all'interno del gruppo.
-   **L'ordine di tabulazione deve essere propagato da sinistra verso destra, dall'alto verso il basso.** In generale, l'ordine di tabulazione deve seguire l'ordine di lettura. Provare a creare eccezioni per i controlli di uso comune inserendoli in precedenza nell'ordine di tabulazione. La scheda dovrebbe scorrere tutti i punti di tabulazione in entrambe le direzioni senza interruzioni. All'interno di un gruppo, l'ordine di tabulazione deve essere in ordine sequenziale, senza eccezioni.
-   **All'interno di una tabulazione, l'ordine del tasto di direzione deve essere propagato da sinistra a destra, dall'alto verso il basso,** senza eccezioni. I tasti di direzione devono scorrere tutti gli elementi in entrambe le direzioni senza interruzioni.
-   **Presentare i pulsanti commit nell'ordine seguente:**
    -   OK/ \[ \] /Yes
    -   \[Non \] /No
    -   Annulla
    -   Applica (se presente)

Quando si \[ esegue questa operazione \] , \[ non \] sono disponibili risposte specifiche all'istruzione principale.

-   **Non confondere le chiavi di accesso con i tasti di scelta rapida.** Sebbene sia le chiavi di accesso che i tasti di scelta rapida forniscano l'accesso tramite tastiera all'interfaccia utente, hanno scopi e linee guida diversi.
-   **Laddove possibile, assegnare chiavi di accesso univoche a tutti i controlli interattivi o alle relative etichette.** Le [caselle di testo](ctrl-text-boxes.md) di sola lettura sono controlli interattivi (poiché gli utenti possono scorrerli e copiare testo), quindi traggono vantaggio dalle chiavi di accesso. **Non assegnare chiavi di accesso a:**
    -   Pulsanti OK, Annulla e Chiudi. Per le chiavi di accesso vengono usati Enter e ESC. Tuttavia, assegnare sempre una chiave di accesso a un controllo che significa OK o Annulla, ma con un'etichetta diversa.
-   **Assegnare i tasti di scelta rapida ai comandi usati più di frequente.** I programmi e le funzionalità usati raramente non necessitano di tasti di scelta rapida perché gli utenti possono usare le chiavi di accesso.
-   **Non creare un tasto di scelta rapida l'unico modo per eseguire un'attività.** Gli utenti devono inoltre essere in grado di utilizzare il mouse o la tastiera con la scheda, la freccia e le chiavi di accesso.
-   **Non assegnare significati diversi ai tasti di scelta rapida noti.** Poiché vengono memorizzati, i significati incoerenti per i collegamenti noti sono frustranti ed è soggetta a errori.
-   **Non tentare di assegnare i tasti di scelta rapida del programma a livello di sistema.** I tasti di scelta rapida del programma avranno effetto solo quando il programma ha lo stato attivo per l'input.

## <a name="mouse"></a>Mouse

-   **Non richiedere mai agli utenti di fare clic su un oggetto per determinare se è selezionabile.** Gli utenti devono essere in grado di determinare la possibilità di fare clic solo tramite controllo visivo.
    -   L'interfaccia utente primaria, ad esempio i pulsanti di commit, deve disporre di una convenienza di clic statica. Gli utenti non devono passare il mouse per individuare l'interfaccia utente primaria.
    -   L'interfaccia utente secondaria, ad esempio i comandi secondari o i controlli di divulgazione progressiva, può visualizzare la propria offerta di clic al passaggio del mouse.
    -   I collegamenti di testo devono suggerire staticamente il testo del collegamento e quindi visualizzare la loro offerta di clic (sottolineata o altra modifica della presentazione, con puntatore a mano) al passaggio del mouse.
    -   I collegamenti grafici visualizzano solo un puntatore a mano al passaggio del mouse.
-   **Usare il puntatore Hand (o "link Select") solo per i collegamenti di testo e grafica.** In caso contrario, gli utenti dovranno fare clic sugli oggetti per determinare se sono collegamenti.

## <a name="dialog-boxes"></a>Finestre di dialogo

-   **Per le finestre di dialogo modali è necessario interagire, quindi utilizzarle per gli elementi a cui gli utenti devono rispondere prima di continuare con l'attività.** Verificare che l'interruzione sia giustificata, ad esempio per attività critiche o non frequenti che richiedono il completamento. In caso contrario, prendere in considerazione alternative non modali.
-   **Le finestre di dialogo non modali non richiedono interazioni, quindi è possibile usarle quando gli utenti devono passare da una finestra di dialogo a una finestra proprietaria.** Sono particolarmente usati per attività frequenti, ripetitive o in corso. Tuttavia, le finestre Ribbon, le barre degli strumenti e le finestre della tavolozza sono spesso alternative migliori.

## <a name="property-sheets"></a>Finestre delle proprietà

-   **Verificare che le proprietà siano necessarie.** Non creare confusione nelle pagine delle proprietà con proprietà non necessarie solo per evitare di prendere decisioni di progettazione difficili.
-   **Presentare le proprietà in termini di obiettivi utente anziché della tecnologia.** Solo perché una proprietà configura una tecnologia specifica non significa che è necessario presentare la proprietà in termini di tale tecnologia.
    -   Se è necessario presentare le impostazioni in termini di tecnologia (forse perché gli utenti riconoscono il nome della tecnologia), includere una breve descrizione del vantaggio dell'utente.
-   **Usare etichette di tabulazioni specifiche e significative.** Evitare le etichette di schede generiche che possono essere applicate a qualsiasi scheda, ad esempio generale, avanzata o impostazioni.
-   **Evitare le pagine generali.** Non è necessario disporre di una pagina generale. Utilizzare una pagina generale solo se:
    -   Le proprietà si applicano a diverse attività e sono significative per la maggior parte degli utenti. Non inserire proprietà specializzate o avanzate in una pagina generale, ma è possibile renderle accessibili tramite un pulsante di comando nella pagina generale.
    -   Le proprietà non rientrano in una categoria più specifica. In caso affermativo, usare invece questo nome per la pagina.
-   **Evitare le pagine avanzate.** Usare una pagina avanzata solo se:
    -   Le proprietà si applicano alle attività non comuni e sono significative principalmente per gli utenti avanzati.
    -   Le proprietà non rientrano in una categoria più specifica. In caso affermativo, usare invece questo nome per la pagina.
-   **Non usare le schede se una finestra delle proprietà dispone di una sola scheda e non è estendibile.** Utilizzare una normale finestra di dialogo con OK, Annulla e un pulsante Applica facoltativo. Tuttavia, le finestre delle proprietà estendibili (che possono essere estese da terze parti) devono usare le schede.

## <a name="wizards"></a>Procedure guidate

-   **Considerare prima le alternative leggere, ad esempio le finestre di dialogo, i riquadri attività o le singole pagine.** Le procedure guidate sono un'interfaccia utente intensa, più adatta per l'attività in più passaggi e non frequenti. Non è necessario usare le procedure guidate: è possibile fornire informazioni utili e assistenza in qualsiasi interfaccia utente.
-   **Utilizzare avanti solo quando si avanza alla pagina successiva senza impegno.** Il passaggio alla pagina successiva viene considerato un impegno quando l'effetto non può essere annullato facendo clic su indietro o su Annulla.
-   **Utilizzare di nuovo solo per correggere gli errori.** Oltre a correggere gli errori, gli utenti non devono fare clic su indietro per avanzare in un'attività.
-   **Quando si esegue il commit di un utente in un'attività, utilizzare un pulsante commit che rappresenta una risposta specifica all'istruzione principale (ad esempio, stampa, Connetti o avvia).** Non usare etichette generiche come Next (che non implicano l'impegno) o Finish (che non è specifico) per il commit di un'attività. Le etichette di questi pulsanti di commit dovrebbero avere un significato autonomo. Avviare sempre le etichette dei pulsanti di commit con un verbo. **Eccezioni**
    -   Usare Finish quando le risposte specifiche sono ancora generiche, ad esempio Save, Select, choose o Get.
    -   Utilizzare fine per modificare un'impostazione specifica o una raccolta di impostazioni.
-   **Usare i collegamenti ai comandi solo per le scelte, non per gli impegni.** I pulsanti di commit specifici indicano un impegno molto migliore rispetto ai collegamenti ai comandi in una procedura guidata.
-   **Quando si usano i collegamenti ai comandi, nascondere il pulsante Avanti, ma lasciare il pulsante Annulla.**
-   **Utilizzare Close per le pagine Follow-Up e complete.** Non usare Annulla perché chiudendo la finestra non verranno abbandonate le modifiche o le azioni eseguite a questo punto. Non usare done perché non è un verbo imperativo.
-   **Non usare "Wizard" nei nomi delle procedure guidate.** Utilizzare, ad esempio, "Connetti a una rete" anziché "installazione guidata rete". Tuttavia, è accettabile fare riferimento alle procedure guidate come procedure guidate. Ad esempio: "Se si sta configurando una rete per la prima volta, è possibile ottenere assistenza usando la procedura guidata Connetti a una rete".
-   **Mantieni le selezioni degli utenti attraverso la navigazione.** Se, ad esempio, l'utente apporta modifiche, fa clic su indietro e quindi su Avanti, le modifiche devono essere mantenute. Non è necessario che gli utenti immettano di nuovo le modifiche, a meno che non vengano esplicitamente selezionate per cancellarle.

## <a name="wizard-pages"></a>Pagine della procedura guidata

-   **Concentrati su un processo decisionale efficiente.** Ridurre il numero di pagine per concentrarsi sui concetti di base. Consolidare le pagine correlate e prendere le pagine facoltative dal flusso principale. Se gli utenti fanno clic su avanti completamente, la procedura guidata potrebbe sembrare un'esperienza ottimale, ma se gli utenti non devono modificare le impostazioni predefinite, le pagine sono probabilmente non necessarie.
-   **Non usare le pagine di benvenuto. quando possibile, rendere la prima pagina funzionale.** Usare una pagina di Introduzione facoltativa solo nei casi seguenti:
    -   La procedura guidata include i prerequisiti necessari per completare correttamente la procedura guidata.
    -   Gli utenti potrebbero non comprendere lo scopo della procedura guidata in base alla pagina della prima scelta e non c'è spazio per altre spiegazioni.
    -   L'istruzione principale per Introduzione pagine è "prima di iniziare:".
-   **Nelle pagine in cui agli utenti viene richiesto di scegliere, ottimizzare per i casi più probabili.** Questi tipi di pagine devono presentare scelte effettive, non solo istruzioni.
    -   Se non si usa una pagina Introduzione, spiegare lo scopo della procedura guidata nella parte superiore della prima pagina di opzioni.
-   **Utilizzare le pagine di commit per cancellare il commit dell'attività da parte degli utenti.** In genere, la pagina commit è l'ultima pagina di scelte e il pulsante Avanti viene rietichettato per indicare l'attività di cui viene eseguito il commit.
    -   Non usare le pagine di riepilogo che riepilogano semplicemente le selezioni precedenti dell'utente, a meno che l'attività non sia rischiosa (che implica la sicurezza o la perdita di tempo o denaro) o se è possibile che gli utenti non siano in grado di comprenderne le selezioni ed è necessario esaminarli.
-   **Non usare le pagine di congratulazioni che non eseguono alcuna operazione ma terminano la procedura guidata.** Se i risultati della procedura guidata sono chiaramente evidenti per gli utenti, è sufficiente chiudere la procedura guidata sul pulsante finale commit.
    -   Utilizzare Follow-Up pagine quando sono presenti attività correlate che è probabile che gli utenti eseguano come completamento. Evitare attività di completamento familiari, ad esempio "inviare un messaggio di posta elettronica".
    -   Usare le pagine di completamento solo quando i risultati non sono visibili e non è disponibile un modo migliore per fornire commenti e suggerimenti per il completamento delle attività.
    -   Le procedure guidate che dispongono di pagine di stato devono utilizzare una pagina di completamento o Follow-Up pagina per indicare il completamento dell'attività. Per le attività a esecuzione prolungata, chiudere la procedura guidata nella pagina commit e utilizzare le notifiche per inviare commenti e suggerimenti.

## <a name="error-messages"></a>messaggi di errore

-   **Non fornire messaggi di errore quando gli utenti non sono in grado di eseguire un'azione o di modificarne il comportamento** come risultato del messaggio. Se non è disponibile alcun intervento da parte degli utenti o se il problema non è significativo, è possibile non visualizzare il messaggio di errore.
-   **Laddove possibile, proporre una soluzione in modo che gli utenti possano risolvere il problema.** Tuttavia, assicurarsi che la soluzione proposta sia in grado di risolvere il problema. Non sprecare tempo per gli utenti suggerendo soluzioni possibili, ma improbabili.
-   **Essere specifici.** Evitare una formulazione vaga, ad esempio errori di sintassi e operazione non valida. Specificare nomi, posizioni e valori specifici degli oggetti necessari.
-   **Non usare la formulazione per biasimare l'utente o implicare un errore dell'utente.** Evitare di usare l'utente e la formulazione. Mentre la voce attiva è in genere preferibile, usare la voce passiva quando l'utente è soggetto e potrebbe essere accusato dell'errore se è stata usata la voce attiva.
-   **Non usare OK per i messaggi di errore.** Gli utenti non visualizzano gli errori come se fossero OK. Se il messaggio di errore non ha un'azione diretta, usare invece Close.
-   **Non usare le parole seguenti:**
    -   Errore, errore (usare invece il problema)
    -   Non è stato possibile (usare in alternativa)
    -   Non valido, non valido, errato (usare invece errato o non valido)
    -   Abort, Kill, terminate (use stop)
    -   Irreversibile, fatale (usare invece gravi)

Questi termini non sono necessari e contrariamente al tono incoraggiante di Windows. Al contrario, un'icona di errore, [se utilizzata correttamente](vis-std-icons.md), comunica con sufficiente la presenza di un problema.

-   **Non accompagnare i messaggi di errore con effetti acustici.** Questa operazione è stonata e non necessaria.

## <a name="warning-messages"></a>Messaggi di avviso

-   **Gli avvisi descrivono una condizione che potrebbe causare un problema in futuro.** Gli avvisi non sono errori o domande, pertanto non è possibile formulare le domande di routine come avvisi.
-   **Non inviare messaggi di avviso quando gli utenti non sono in grado di eseguire un'azione o di modificarne il comportamento come risultato del messaggio.** Se non è disponibile alcun intervento da parte degli utenti o se la condizione non è significativa, non visualizzare il messaggio di avviso.

## <a name="confirmations"></a>Conferme

-   **Non usare conferme non necessarie.** USA conferme solo nei casi seguenti:
    -   Il motivo per cui non è possibile continuare e una ragionevole probabilità che talvolta gli utenti non saranno disponibili.
    -   L'azione ha conseguenze significative o non può essere facilmente annullata.
    -   L'azione ha conseguenze che gli utenti potrebbero non essere in grado di riconoscere.
    -   Per procedere con l'azione è necessario che gli utenti effettuino una scelta che non disponga di un valore predefinito appropriato.
    -   Dato il contesto corrente, è probabile che gli utenti abbiano eseguito un'azione in errore.
-   **Conferme di frase come domanda sì o no e fornire risposte sì o no.** A differenza di altri tipi di finestre di dialogo, le conferme sono progettate per impedire agli utenti di prendere decisioni rapide. Se gli utenti non considerano la risposta, una conferma non ha alcun valore.

## <a name="icons"></a>Icone

-   **Tutte le icone devono rispettare le linee guida per le icone di** [tipo Aero](vis-icons.md). Sostituire tutte le icone di tipo Windows XP.
-   **Scegliere icone standard in base al tipo di messaggio, non alla gravità del problema sottostante:**
    -   **Errore.** Errore o problema che si è verificato.
    -   **Avviso.** Condizione che potrebbe causare un problema in futuro.
    -   **Informazioni.** Informazioni utili.

Se un problema combina tipi di messaggi diversi, concentrarsi sull'aspetto più importante su cui gli utenti devono agire.

-   **Le icone devono sempre corrispondere all'istruzione principale o ad altro testo corrispondente.**
-   **Le icone di errore non sono necessarie per problemi di input utente non critici.** Tuttavia, le icone sono necessarie per gli errori sul posto, perché altrimenti tali commenti contestuali sarebbero troppo semplici da ignorare.
-   **Non usare icone di avviso per "ammorbidire" gli errori non critici.** Gli errori non sono avvisi; in alternativa, applicare le linee guida sull'icona di errore.
-   **Per le finestre di dialogo delle domande, usare le icone di avviso solo per le domande con conseguenze significative.** Non usare icone di avviso per domande di routine.

## <a name="help"></a>Help

-   **Collegamento a specifici argomenti della guida pertinenti.** Non eseguire il collegamento al home page della guida, al sommario, a un elenco di risultati della ricerca o a una pagina che si limita solo a collegamenti ad altre pagine. Evitare il collegamento a pagine strutturate come un ampio elenco di domande frequenti, perché impone agli utenti di cercare quello che corrisponde al collegamento selezionato. Non eseguire il collegamento ad argomenti della Guida specifici che non sono rilevanti e utili per l'attività. Non collegare mai a pagine vuote.
-   **Non inserire collegamenti Guida in ogni finestra o pagina per motivi di coerenza.** Fornire un collegamento alla Guida in un'unica posizione non significa che è necessario fornirli ovunque.
-   **Quando possibile, la frase guida consente di collegare il testo in termini di domanda principale fornita dal contenuto della guida.** Non usare la formulazione "ulteriori informazioni" o "ottenere assistenza per questo".
-   **Usare l'intero collegamento alla guida per il testo del collegamento,** non solo le parole chiave.
-   **Utilizzare frasi complete.**
-   **Non usare segni di punteggiatura o ellissi finali, ad eccezione dei punti interrogativi.**
-   **Se il contenuto della guida è online, renderlo chiaro nel testo del collegamento.** Questa operazione consente di rendere prevedibili i risultati dei collegamenti.

