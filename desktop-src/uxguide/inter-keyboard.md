---
title: Tastiera
description: La tastiera è il dispositivo di input primario usato per l'input di testo in Microsoft Windows. Per l'accessibilità e l'efficienza, la maggior parte delle azioni può essere eseguita anche usando la tastiera.
ms.assetid: 27185c98-1233-4e26-a156-0ff080fd4db3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 4339dfd8d4d31d0d8859dcedd07fc287426b04c0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104562154"
---
# <a name="keyboard"></a>Tastiera

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

La tastiera è il dispositivo di input primario usato per l'input di testo in Microsoft Windows. Per l'accessibilità e l'efficienza, la maggior parte delle azioni può essere eseguita anche usando la tastiera.

Le tastiere possono anche fare riferimento alle tastiere virtuali, sullo schermo e ai pad di scrittura usati dai computer senza una tastiera fisica, ad esempio computer basati su tablet.

![screenshot della tastiera su schermo ](images/inter-keyboard-image1.png)

Tastiera su schermo di Windows Tablet e Touch Technology.

![screenshot del riquadro di scrittura del Tablet Windows ](images/inter-keyboard-image2.png)

Riquadro di scrittura della tecnologia Tablet e touch di Windows.

Sono disponibili sei tipi di chiavi di base:

-   Un tasto carattere Invia un carattere letterale alla finestra con lo stato attivo per l'input.
-   Un tasto di modifica combinato con un'altra chiave modifica il significato della chiave associata, ad esempio CTRL, ALT, MAIUSC e il tasto logo Windows.
-   I tasti di navigazione sono le frecce direzionali, più Home, fine, PGSU e PGGIÙ.
-   I tasti di modifica sono INSERT, backspace ed Delete.
-   I tasti funzione sono da F1 a F12.
-   Le chiavi di sistema inseriscono il sistema in modalità o eseguono un'attività di sistema, ad esempio Stamp, BLOC MAIUSC e BLOC NUM.

Le chiavi di accesso sono chiavi o combinazioni di chiavi usate per l'accessibilità per interagire con tutti i controlli o le voci di menu tramite la tastiera. I tasti di scelta rapida sono chiavi o combinazioni di chiavi usate dagli utenti avanzati per eseguire i comandi usati di frequente per migliorare l'efficienza. Windows indica le chiavi di accesso, sottostrutturando l'assegnazione della chiave di accesso.

![screenshot delle chiavi di accesso e dei tasti di scelta rapida ](images/inter-keyboard-image3.png)

Questo esempio mostra sia le chiavi di accesso che i tasti di scelta rapida.

Per eliminare la confusione visiva, Windows nasconde le sottolineature delle chiavi di accesso per impostazione predefinita e le Visualizza solo quando viene premuto il tasto ALT. Per garantire la coerenza con Windows, le immagini nella Guida di UX vengono visualizzate anche con le sottolineature delle chiavi di accesso nascoste, a meno che le linee guida non includano chiavi di accesso.

Per migliorare la conoscenza delle assegnazioni delle chiavi di accesso nel programma durante il processo di sviluppo, è possibile visualizzarle in qualsiasi momento. Nel pannello di controllo passare al centro di accesso facilitato e fare clic su **Rendi più semplice l'uso della tastiera**; Selezionare quindi la casella di controllo **sottolineatura tasti di scelta rapida e chiavi di accesso** .

**Nota:** Le linee guida correlate all' [accessibilità](inter-accessibility.md) sono presentate in un articolo separato.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="elements-of-keyboard-navigation"></a>Elementi di navigazione da tastiera

Gli utenti interagiscono con una finestra usando la tastiera passando a controlli, effettuando selezioni ed eseguendo comandi. Per eseguire questa operazione, gli elementi seguenti interagiscono.

![screenshot della finestra di dialogo Modifica colori ](images/inter-keyboard-image4.png)

Per illustrare gli elementi della navigazione da tastiera nell'elenco seguente, si farà riferimento a questa finestra di dialogo.

-   **Stato attivo per l'input.** Il controllo con lo stato attivo di input riceve la maggior parte degli input da tastiera. Lo stato attivo per l'input è indicato da un rettangolo tratteggiato denominato rettangolo di attivazione. Viene inviato un input da tastiera a controlli che non hanno lo stato attivo per l'input, come spiegato più avanti.

    ![screenshot della prima riga nella finestra di dialogo Modifica colori ](images/inter-keyboard-image5.png)

    Il primo controllo colori di base ha lo stato attivo per l'input, come indicato con un rettangolo tratteggiato.

-   **Tasto TAB e tabulazioni.** Il tasto TAB è il meccanismo principale per spostarsi all'interno di una finestra. Il tasto TAB consente di visitare solo i controlli con una tabulazione. Tutti i controlli interattivi dovrebbero avere delle tabulazioni (a meno che non siano in un gruppo), a differenza dei controlli non interattivi, come le etichette.
-   **Ordine di tabulazione.** Tutti i controlli con tabulazioni vengono visualizzati in ordine di tabulazione. Premendo TAB lo stato attivo viene spostato al controllo successivo nell'ordine di tabulazione, mentre se si preme MAIUSC + TAB lo stato attivo viene spostato sul controllo precedente.
-   **Gruppi di controlli.** Un set di controlli correlati può essere creato in un gruppo a cui viene assegnata una singola tabulazione. I gruppi di controlli vengono usati per i set di controlli che si comportano come un singolo controllo, ad esempio i pulsanti di opzione. Possono essere usati anche quando i controlli sono troppi per poter navigare in modo efficiente solo con il tasto TAB.

    ![screenshot dei gruppi di colori di base e personalizzati ](images/inter-keyboard-image6.png)

    I colori di base e i colori personalizzati sono gruppi di controllo, che assegnano a questa finestra di dialogo cinque tabulazioni. Ci sono così tanti controlli che la navigazione sarebbe inefficiente senza usare i gruppi di controllo.

-   **Tasti di direzione** I tasti di direzione spostano lo stato attivo per l'input tra i controlli all'interno di un gruppo. Premendo il tasto freccia destra si sposta lo stato attivo di input al controllo successivo nell'ordine di tabulazione, mentre la pressione della freccia sinistra sposta lo stato attivo sul controllo precedente. Anche Home, end, up e Down hanno il comportamento previsto all'interno di un gruppo. Gli utenti non possono spostarsi da un gruppo di controllo usando i tasti di direzione.
-   **Pulsanti predefiniti.** Windows con i pulsanti di comando e i collegamenti di comando hanno un singolo pulsante predefinito indicato da un bordo evidenziato, ovvero il pulsante che si fa clic quando si preme il tasto INVIO. Per impostazione predefinita, viene assegnato un singolo pulsante di comando o collegamento al comando predefinito. Il pulsante predefinito si sposta tuttavia quando l'utente esegue la tabulazione su un altro pulsante di comando o collegamento al comando. Di conseguenza, qualsiasi pulsante di comando o collegamento al comando con lo stato attivo per l'input è sempre il pulsante predefinito.

    ![screenshot dei pulsanti OK e Annulla ](images/inter-keyboard-image7.png)

    Il pulsante OK corrisponde in genere al pulsante predefinito, come indicato dal bordo evidenziato. Tuttavia, se l'utente dovesse premere TAB sul pulsante Annulla, diventa il pulsante predefinito e viene attivato con il tasto INVIO.

-   **Barra spaziatrice, invio e tasti ESC.** La barra spaziatrice attiva il controllo con lo stato attivo per l'input, mentre il tasto INVIO attiva il pulsante predefinito. Premendo ESC si annulla o si chiude la finestra.
-   **Chiavi di accesso.** Le chiavi di accesso vengono usate per interagire direttamente con i controlli anziché spostarsi con la scheda. Vengono combinati con il tasto ALT e indicati con una lettera sottolineata nell'etichetta.
-   **Etichette delle chiavi di accesso.** Mentre alcuni controlli contengono etichette proprie, ad esempio pulsanti di comando, caselle di controllo e pulsanti di opzione, altri controlli hanno etichette esterne, ad esempio caselle di riepilogo e visualizzazioni ad albero. Per le etichette esterne, la chiave di accesso viene assegnata all'etichetta e, se richiamata, passa al controllo successivo in ordine di tabulazione. Ai pulsanti con etichetta OK, Annulla e Chiudi non vengono assegnate chiavi di accesso perché vengono richiamati con Enter e ESC.

    ![screenshot delle etichette con ' b ' è d'sottolineato ](images/inter-keyboard-image8.png)

    Premendo ALT + B si passa al colore di base selezionato, premendo ALT + D viene fatto clic sul pulsante Definisci colori personalizzati, immettere richiama il pulsante OK e ESC richiama Annulla.

-   **Comportamento della chiave di accesso.** Quando viene richiamata una chiave di accesso che viene assegnata in modo univoco, viene fatto clic sul controllo associato. Se l'assegnazione non è univoca, al controllo associato viene assegnato lo stato attivo per l'input. Se l'utente digita di nuovo la stessa chiave di accesso, il controllo successivo nell'ordine di tabulazione con la stessa assegnazione riceve lo stato attivo per l'input.

Sebbene questo meccanismo sia piuttosto complesso, è anche abbastanza intuitivo. Gli utenti acquisiscono la maggior parte di questi dettagli immediatamente, anche se pochi possono spiegarne esattamente il funzionamento.

### <a name="keyboard-support-for-accessibility-and-advanced-users"></a>Supporto della tastiera per l'accessibilità e gli utenti avanzati

**In Windows, la progettazione per la tastiera si riduce per offrire una navigazione da tastiera ben progettata, chiavi di accesso per l'accessibilità e tasti di scelta rapida per utenti avanzati.**

Per assicurarsi che la funzionalità del programma sia facilmente disponibile per la più ampia gamma di utenti, inclusi quelli con disabilità e problemi, tutti gli elementi dell'interfaccia utente interattiva devono essere accessibili da tastiera. In genere, ciò significa che gli elementi dell'interfaccia utente usati più di frequente sono accessibili usando una singola combinazione di tasti o chiavi di accesso, mentre gli elementi usati meno di frequente possono richiedere l'esplorazione aggiuntiva della scheda o del tasto freccia. Per questi utenti, la completezza è più importante della coerenza.

Per assicurarsi che le funzionalità del programma siano efficienti per gli utenti esperti, gli elementi dell'interfaccia utente usati comunemente dovrebbero avere anche tasti di scelta rapida per l'accesso diretto alla tastiera. Gli utenti esperti spesso preferiscono usare la tastiera, perché i comandi basati sulla tastiera possono essere immessi più rapidamente e senza dover togliere le mani dalla tastiera. Per questi utenti, efficienza e coerenza sono indispensabili. La completezza è importante solo per i comandi usati più di frequente.

Quando si progetta l'accesso da tastiera per questi due gruppi, sono presenti differenze minime, motivo per cui Windows fornisce due meccanismi indipendenti di accesso diretto alla tastiera. Utilizzando i tasti di scelta rapida e di accesso, è possibile fornire ai programmi un accesso alla tastiera efficiente, coerente e completo che offre vantaggi a tutti.

### <a name="access-keys"></a>Chiavi di accesso

I tasti di scelta presentano le caratteristiche seguenti:

-   Usano il tasto ALT e un tasto alfanumerico.
-   Servono principalmente per l'accessibilità.
-   Vengono assegnati a tutti i menu e alla maggior parte dei controlli delle finestre di dialogo.
-   Non è previsto che vengano memorizzati e quindi vengono documentati direttamente nell'interfaccia utente sottolineando il carattere corrispondente dell'etichetta del controllo.
-   Hanno effetto solo nella finestra corrente e passano alla voce di menu o al controllo corrispondente.
-   Non è sempre possibile assegnarli in modo coerente, ma lo si dovrebbe fare per i comandi più usati, soprattutto i pulsanti di conferma.
-   Vengono localizzati.

**Poiché le chiavi di accesso non sono destinate a essere memorizzate, vengono assegnate a un carattere che si trova all'inizio dell'etichetta per** facilitarne la ricerca, anche se è presente una parola chiave che viene visualizzata più avanti nell'etichetta.

**Corretto:**

![cattura di schermata del primo carattere nell'etichetta sottolineata ](images/inter-keyboard-image9.png)

**Non corretto:**

![cattura di schermata del primo carattere sottolineato ](images/inter-keyboard-image10.png)

Nell'esempio corretto, la chiave di accesso viene assegnata a un carattere che si trova all'inizio dell'etichetta.

### <a name="shortcut-keys"></a>Combinazioni di tasti

Al contrario, i tasti di scelta rapida presentano le seguenti caratteristiche:

-   Usano soprattutto le sequenze di tasti funzione e CTRL. Le combinazioni di tasti dei sistemi Windows usano anche ALT+tasti non alfanumerici e il tasto WINDOWS.
-   Servono soprattutto a garantire efficienza agli utenti avanzati.
-   Vengono assegnati solo ai comandi usati più comunemente.
-   È previsto che vengano memorizzati e vengono documentati solo nei menu, nelle descrizioni comandi e nella Guida.
-   Hanno effetto in tutto il programma, ma non hanno effetto se non vengono applicati.
-   Devono essere assegnati in modo coerente perché vengono memorizzati e non sono documentati direttamente.
-   Non vengono localizzati.

**Poiché i tasti di scelta rapida sono destinati a essere memorizzati, i tasti di scelta rapida usati con maggiore frequenza idealmente usano le lettere del primo o dei caratteri più memorabili nelle parole chiave del comando,** ad esempio CTRL + C per la copia e CTRL + Q per la richiesta.

Il significato incoerente per i tasti di scelta rapida noti è frustrante e causare errori.

**Non corretto:**

![cattura di schermata del pulsante avanti con ' w ' sottolineato ](images/inter-keyboard-image11.png)

In questo esempio, CTRL + F è il tasto di scelta rapida standard per trova, quindi la relativa assegnazione a inoltr è frustrante e soggetta a errori. CTRL + W è una scelta migliore, memorabile.

Infine, dal momento che sono destinati a essere memorizzati, i **tasti di scelta rapida specifici dell'applicazione hanno senso solo per i programmi e le funzionalità che vengono eseguiti con frequenza sufficiente per consentire agli utenti motivati di memorizzare.** I programmi e le funzionalità usati raramente non necessitano di tasti di scelta rapida. Ad esempio, i programmi di installazione e la maggior parte delle procedure guidate non necessitano di particolari assegnazioni di tasti di scelta rapida, né i comandi usati di frequente in un'applicazione di produttività.

### <a name="assigning-access-keys-in-dialog-boxes"></a>Assegnazione delle chiavi di accesso nelle finestre di dialogo

Laddove possibile, assegnare chiavi di accesso univoche a tutti i controlli interattivi tranne quelli che in genere non sono assegnati alle chiavi di accesso. Tuttavia, in inglese sono disponibili solo 26 caratteri. Alcuni caratteri potrebbero non essere visualizzati in nessuna delle etichette e potrebbero non essere presenti caratteri distintivi in tutte le etichette, riducendo ulteriormente questo numero. Inoltre, è consigliabile pianificare la presenza di alcuni caratteri non assegnati per facilitare la localizzazione. Di conseguenza, è possibile assegnare solo circa 20 chiavi di accesso univoche in un'unica finestra di dialogo.

Se si dispone di una finestra di dialogo con più di 20 controlli interattivi, non assegnare chiavi di accesso ad alcuni controlli oppure, in rare situazioni, assegnare chiavi di accesso duplicate.

![screenshot della finestra di dialogo tipo di carattere ](images/inter-keyboard-image12.png)

Quando sono presenti molti controlli interattivi, non tutti necessitano di una chiave di accesso assegnata.

Utilizzare la seguente procedura generale per assegnare chiavi di accesso:

-   Assegnare innanzitutto le chiavi di accesso ai [pulsanti di commit](glossary.md) e ai collegamenti dei comandi. Usare la tabella assegnazioni di chiavi di accesso standard quando si applica; in caso contrario, usare la prima lettera della prima parola.
-   Ignorare i controlli a cui non sono assegnate chiavi di accesso.
-   Assegnare chiavi di accesso univoche ai controlli rimanenti (a partire dai più usati):
    -   Se possibile, assegnare la chiave di accesso in base alla tabella assegnazioni di chiavi di accesso standard.
    -   In caso contrario:
        -   Preferisce i caratteri che vengono visualizzati all'inizio dell'etichetta, idealmente il primo carattere della prima o della seconda parola.
        -   Preferisce una consonante distinta o una vocale, ad esempio "x" in "Exit".
        -   Preferisce i caratteri con larghezze larghe, come w, m e lettere maiuscole.
        -   Evitare l'uso di caratteri che rendono difficile la visualizzazione della sottolineatura, ad esempio lettere con una larghezza di un pixel, lettere con discendenti e lettere accanto a una lettera con un discendente.
-   Se non tutti i controlli possono avere chiavi di accesso univoche (iniziare con il meno frequente utilizzo):
    -   Se sono presenti gruppi di controlli correlati, ad esempio:
        -   Un singolo set di pulsanti di opzione
        -   Set di caselle di controllo correlate
        -   Set di controlli correlati in una casella di gruppo

Assegnare le chiavi di accesso per raggruppare le etichette invece dei singoli controlli. In genere si esegue l'operazione opposta. (In questo modo, assicurarsi che sia presente un gruppo di controlli definito per questi controlli).

-   Se ancora non tutti i controlli possono avere chiavi di accesso univoche:
    -   È possibile assegnare chiavi di accesso non univoche se:
        -   Altrimenti, i controlli sarebbero troppo difficili da esplorare.
        -   Le chiavi di accesso non univoche non sono in conflitto con le chiavi di accesso dei controlli di uso comune.
    -   In caso contrario, è possibile accedere ai controlli rimanenti utilizzando l'esplorazione dei tasti di direzione e di tabulazione.

![screenshot dei gruppi con chiavi di accesso diverse ](images/inter-keyboard-image13.png)

In questo esempio sono presenti controlli ripetuti, quindi le chiavi di accesso vengono assegnate ai gruppi di pulsanti di opzione.

### <a name="preventing-accidental-commands"></a>Prevenzione di comandi accidentali

Se una finestra visualizzata fuori contesto (non avviata dall'utente) sottrae lo stato attivo per l'input, è probabile che questa finestra riceva l'input destinato a un'altra finestra. Inoltre, le chiavi di accesso hanno effetto quando viene premuto senza premere ALT se la finestra di dialogo non contiene controlli che accettano input di testo (ad esempio caselle di testo ed elenchi). Quindi, nell'esempio seguente, premendo "r" viene attivato il pulsante Riavvia ora.

Chiaramente, tale input potrebbe avere conseguenze impreviste significative.

**Non corretto:**

![cattura di schermata del pulsante Riavvia ora,' r ' sottolineato ](images/inter-keyboard-image14.png)

In questo esempio, digitando il testo con lo spazio, "r" o immettendo il riavvio accidentale di Windows.

Naturalmente, la soluzione migliore per questo problema non è rubare lo stato attivo per l'input. In alternativa, lampeggiare il [pulsante della barra delle applicazioni](winenv-taskbar.md) del programma o visualizzare una notifica per ottenere l'attenzione dell'utente.

Tuttavia, se è necessario visualizzare tale finestra, l'approccio migliore consiste nel non assegnare un pulsante predefinito o chiavi di accesso e assegnare lo stato attivo per l'input iniziale a un controllo diverso da un pulsante di commit.

**Corretto:**

![cattura di schermata del pulsante Riavvia,' r ' non sottolineato ](images/inter-keyboard-image15.png)

In questo esempio, il riavvio accidentale di Windows è molto più difficile.

**Se si eseguono solo sei elementi...**

1.  Progettare una corretta navigazione da tastiera, con un ordine di tabulazione ragionevole e gruppi di controllo appropriati, lo stato attivo per l'input iniziale e i pulsanti predefiniti.
2.  Assegnare chiavi di accesso a tutti i menu e alla maggior parte dei controlli.
3.  Assegnare le chiavi di accesso a un carattere che viene visualizzato all'inizio dell'etichetta per facilitarne l'individuazione.
4.  Assegnare i tasti di scelta rapida ai comandi usati più di frequente.
5.  Provare ad assegnare i tasti di scelta rapida al primo o più caratteri memorabili all'interno delle parole chiave.
6.  Assegnare ai tasti di scelta rapida noti un significato coerente.

## <a name="guidelines"></a>Indicazioni

### <a name="interaction"></a>Interazione

-   **Non usare il tasto MAIUSC per modificare i comandi nei menu o nelle finestre di dialogo.** Questa operazione non è individuabile e imprevista.

    **Non corretto:**

    ![screenshot della finestra di dialogo Conferma sostituzione cartella ](images/inter-keyboard-image16.png)

    In questo esempio di Windows XP, tenendo premuto il tasto MAIUSC, viene sostituito sì con all.

-   **Non disabilitare un controllo con lo stato attivo per l'input. Questa operazione può impedire alla finestra di ricevere input da tastiera.** Al contrario, prima di disabilitare un controllo con lo stato attivo per l'input, spostare lo stato attivo di input in un altro controllo.
-   **Se una finestra viene visualizzata fuori contesto, potenzialmente sorprendente per gli utenti, potrebbe essere necessario prevenire conseguenze impreviste significative:**
    -   Non assegnare un pulsante predefinito.
    -   Non assegnare chiavi di accesso.
    -   Dare lo stato attivo per l'input iniziale a un controllo diverso da un pulsante di commit.

### <a name="keyboard-navigation"></a>Spostamento tramite tastiera

-   **Mostra sempre l'indicatore dello stato attivo per l'input. Eccezione:** è possibile disattivare temporaneamente l'indicatore dello stato attivo per l'input se:
    -   L'indicatore di stato attivo per l'input si distrae visivamente (come con una visualizzazione elenco di grandi dimensioni non in visualizzazione dettagli).
    -   L'utilizzo del tasto invio è probabilmente preceduto da un altro input da tastiera, ad esempio ALT o tasti di direzione.
    -   L'indicatore di stato attivo per l'input viene visualizzato su qualsiasi input da tastiera.
-   **Assegnare lo stato attivo per l'input iniziale al controllo che gli utenti con maggiore probabilità interagiranno prima,** che è spesso il primo controllo interattivo. Se il primo controllo interattivo non è una scelta ottimale, provare a modificare il layout della finestra.
-   **Assegna tabulazioni si arresta a tutti i controlli interattivi, incluse le caselle di modifica di sola lettura. Eccezioni**
    -   Gruppi di gruppi di controlli correlati che si comportano come un unico controllo, ad esempio i pulsanti di opzione. Tali gruppi hanno una singola tabulazione.
    -   Contenere correttamente i gruppi in modo che i tasti di direzione siano in avanti e indietro all'interno del gruppo e restino all'interno del gruppo.
-   **L'ordine di tabulazione deve seguire l'ordine di lettura, che in genere scorre da sinistra a destra, dall'alto verso il basso.** Provare a creare eccezioni per i controlli di uso comune inserendoli in precedenza nell'ordine di tabulazione. La scheda dovrebbe scorrere tutti i punti di tabulazione in entrambe le direzioni senza interruzioni.
-   **All'interno di una tabulazione, l'ordine del tasto di direzione deve essere propagato da sinistra a destra, dall'alto verso il basso,** senza eccezioni. I tasti di direzione devono scorrere tutti gli elementi in entrambe le direzioni senza interruzioni.
-   **Presentare i pulsanti commit nell'ordine seguente:**
    -   OK/ \[ \] /Yes
    -   \[Non \] /No
    -   Annulla
    -   Applica (se presente)

Quando si \[ esegue questa operazione \] , \[ non \] sono disponibili risposte specifiche all'istruzione principale.

-   **Selezionare il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e il pulsante di comando più sicuro o il collegamento di comando come predefinito.** Se la sicurezza e la sicurezza non sono fattori, selezionare la risposta più probabile o pratica.
-   **La navigazione tramite tastiera non deve modificare i valori del controllo o generare un messaggio di errore.** Non richiedere mai agli utenti di modificare il valore iniziale di un controllo durante la navigazione. Al contrario, inizializzare i controlli che convalidano all'uscita con valori validi e convalidare il valore di un controllo solo quando è stato modificato.

### <a name="access-keys"></a>Chiavi di accesso

-   **Quando possibile, assegnare le chiavi di accesso per i comandi usati di frequente in base alla tabella seguente.** Sebbene le assegnazioni di chiavi di accesso coerenti non siano sempre possibili, sono certamente preferite soprattutto per i comandi usati di frequente.

    |                           |                                           |
    |---------------------------|-------------------------------------------|
    | **Chiave di accesso**<br/> | **Comando**<br/>                    |
    | A<br/>              | Informazioni<br/>                          |
    | A<br/>              | Sempre in primo piano<br/>                  |
    | A<br/>              | Applica<br/>                          |
    | B<br/>              | Indietro<br/>                           |
    | B<br/>              | Grassetto<br/>                           |
    | B o r<br/>         | Esplora<br/>                         |
    | C<br/>              | Chiudi<br/>                          |
    | C<br/>              | Copia<br/>                           |
    | C<br/>              | Copia qui<br/>                      |
    | s<br/>              | Crea collegamento<br/>                |
    | s<br/>              | Crea collegamento qui<br/>           |
    | u<br/>              | Taglia<br/>                            |
    | D<br/>              | Delete<br/>                         |
    | D<br/>              | Non visualizzare \[ più questo elemento \]<br/> |
    | E<br/>              | Modifica<br/>                           |
    | x<br/>              | Esci<br/>                           |
    | E<br/>              | Esplora<br/>                        |
    | F<br/>              | Meno<br/>                          |
    | F<br/>              | File<br/>                           |
    | F<br/>              | Find<br/>                           |
    | n<br/>              | Trova successivo<br/>                      |
    | F<br/>              | Carattere<br/>                           |
    | F<br/>              | Inoltra<br/>                        |
    | H<br/>              | Help<br/>                           |
    | u<br/>              | argomenti della Guida<br/>                    |
    | H<br/>              | Nascondi<br/>                           |
    | I<br/>              | Insert<br/>                         |
    | o<br/>              | Inserisci oggetto<br/>                  |
    | I<br/>              | Corsivo<br/>                         |
    | L<br/>              | Collegamento qui<br/>                      |
    | x<br/>              | Ingrandisci<br/>                       |
    | n<br/>              | Riduci<br/>                       |
    | M<br/>              | Più informazioni<br/>                           |
    | M<br/>              | Sposta<br/>                           |
    | M<br/>              | Sposta qui<br/>                      |
    | N<br/>              | Nuova<br/>                            |
    | N<br/>              | Prossima<br/>                           |
    | N<br/>              | No<br/>                             |
    | O<br/>              | Apri<br/>                           |
    | w<br/>              | Apri con<br/>                      |
    | O<br/>              | Opzioni<br/>                        |
    | u<br/>              | Impostazioni di pagina<br/>                     |
    | P<br/>              | Incolla<br/>                          |
    | l<br/>              | Incolla collegamento<br/>                     |
    | s<br/>              | Incolla collegamento<br/>                 |
    | s<br/>              | Incolla speciale<br/>                  |
    | P<br/>              | Sospendi<br/>                          |
    | P<br/>              | Esegui<br/>                           |
    | P<br/>              | Stampa<br/>                          |
    | P<br/>              | Stampa qui<br/>                     |
    | r<br/>              | Proprietà<br/>                     |
    | R<br/>              | Ripeti<br/>                           |
    | R<br/>              | Repeat<br/>                         |
    | R<br/>              | Restore<br/>                        |
    | R<br/>              | Riprendi<br/>                         |
    | R<br/>              | Riprova<br/>                          |
    | R<br/>              | Esegui<br/>                            |
    | S<br/>              | Salva<br/>                           |
    | a<br/>              | Salva con nome<br/>                        |
    | a<br/>              | Seleziona tutto<br/>                     |
    | n<br/>              | Invia a<br/>                        |
    | S<br/>              | Mostra<br/>                           |
    | S<br/>              | Dimensione<br/>                           |
    | p<br/>              | Doppia visualizzazione<br/>                          |
    | S<br/>              | Interrompere<br/>                           |
    | T<br/>              | Strumenti<br/>                          |
    | U<br/>              | Sottolineato<br/>                      |
    | U<br/>              | Annulla<br/>                           |
    | V<br/>              | Visualizzazione<br/>                           |
    | W<br/>              | Finestra<br/>                         |
    | S<br/>              | Sì<br/>                            |

    

     

-   **Preferisce caratteri con larghezze ampie,** ad esempio w, m e lettere maiuscole.
-   **Preferisce una consonante distinta o una vocale,** ad esempio "x" in "Exit".
-   **Evitare l'uso di caratteri che rendono difficile la visualizzazione della sottolineatura,** ad esempio (dal più problematico al meno problematico):
    -   Caratteri con una sola larghezza di pixel, ad esempio i e l.
    -   Caratteri con discendenti, ad esempio g, j, p, q e y.
    -   Caratteri accanto a una lettera con un discendente.
-   Quando si assegnano le chiavi di accesso nelle pagine della procedura guidata, ricordarsi di riservare "B" per indietro e "N" per il successivo.
-   Quando si assegnano le chiavi di accesso nelle pagine delle proprietà, ricordarsi di riservare "A" per Apply, se usato.

### <a name="menu-access-keys"></a>Chiavi di accesso ai menu

-   **Assegnare chiavi di accesso a tutte le voci di menu.** Nessuna eccezione.
-   **Per le voci di menu dinamiche, ad esempio i file usati di recente, assegnare chiavi di accesso numericamente.**

    ![screenshot delle voci di menu con chiavi di accesso numeriche ](images/inter-keyboard-image17.png)

    In questo esempio, il programma di disegno in Windows assegna chiavi di accesso numeriche ai file usati di recente.

-   **Assegnare chiavi di accesso univoche all'interno di un livello di menu.** È possibile riutilizzare le chiavi di accesso in diversi livelli di menu.
-   **Semplifica la ricerca delle chiavi di accesso:**
    -   Per le voci di menu utilizzate più di frequente, scegliere caratteri all'inizio della prima o della seconda parola dell'etichetta, preferibilmente il primo carattere.
    -   Per le voci di menu utilizzate meno di frequente, scegliere lettere che rappresentano una consonante distinta o una vocale nell'etichetta.

### <a name="dialog-box-access-keys"></a>Chiavi di accesso della finestra di dialogo

-   **Laddove possibile, assegnare chiavi di accesso univoche a tutti i controlli interattivi o alle relative etichette.** Le [caselle di testo](ctrl-text-boxes.md) di sola lettura sono controlli interattivi (poiché gli utenti possono scorrerli e copiare testo), quindi traggono vantaggio dalle chiavi di accesso. **Non assegnare chiavi di accesso a:**
    -   **Pulsanti OK, Annulla e Chiudi.** Per le chiavi di accesso vengono usati Enter e ESC. Tuttavia, assegnare sempre una chiave di accesso a un controllo che significa OK o Annulla, ma con un'etichetta diversa.

        ![screenshot della finestra di dialogo con i pulsanti Sì e no ](images/inter-keyboard-image18.png)

        In questo esempio il pulsante di commit positivo ha una chiave di accesso assegnata.

    -   **Etichette del gruppo.** In genere, i singoli controlli all'interno di un gruppo vengono assegnati alle chiavi di accesso, quindi l'etichetta del gruppo non ne ha bisogno. Tuttavia, assegnare una chiave di accesso all'etichetta del gruppo e non ai singoli controlli in caso di carenza di chiavi di accesso.
    -   **Pulsanti della Guida generici,** a cui è possibile accedere con F1.
    -   **Etichette di collegamento.** Spesso sono presenti troppi collegamenti per assegnare chiavi di accesso univoche e i caratteri di sottolineatura dei collegamenti nascondono i caratteri di sottolineatura della chiave di accesso. Chiedere agli utenti di accedere ai collegamenti con il tasto TAB.
    -   **Nomi delle schede.** Le tabulazioni vengono ciclate con CTRL + TAB e CTRL + MAIUSC + TAB.
    -   **Pulsanti Sfoglia con etichetta "...".** Non è possibile assegnare chiavi di accesso in modo univoco.
    -   **Controlli senza etichetta,** ad esempio controlli di selezione, pulsanti di comando grafici e controlli di divulgazione progressivi senza etichetta.
    -   **Testo statico senza etichetta o etichette per i controlli che non sono interattivi,** ad esempio le barre di stato.

-   **Assegnare prima di tutto i pulsanti di accesso per assicurarsi che abbiano le assegnazioni di chiavi standard.** Se non è disponibile un'assegnazione di chiave standard, usare la prima lettera della prima parola. La chiave di accesso per i pulsanti Sì e no commit, ad esempio, deve essere sempre "Y" e "N", indipendentemente dagli altri controlli della finestra di dialogo.
-   **Per i pulsanti di commit negativi (diversi da Cancel) formulati come "non", assegnare la chiave di accesso a "n" in "No".** Se non viene formulata come "non", usare l'assegnazione della chiave di accesso standard o assegnare la prima lettera della prima parola. In questo modo, tutti i non sono disponibili e non hanno una chiave di accesso coerente.
-   **Per semplificare la ricerca delle chiavi di accesso, assegnare le chiavi di accesso a un carattere che viene visualizzato all'inizio dell'etichetta,** idealmente il primo carattere, anche se è presente una parola chiave che viene visualizzata più avanti nell'etichetta.
-   **Assegnare al massimo 20 chiavi di accesso,** quindi sono disponibili alcuni caratteri non assegnati per facilitare la localizzazione.
-   **Se sono presenti troppi controlli interattivi per assegnare chiavi di accesso univoche, è possibile assegnare chiavi di accesso non univoche** se:
    -   Altrimenti, i controlli sarebbero troppo difficili da esplorare.
    -   Le chiavi di accesso non univoche non sono in conflitto con le chiavi di accesso dei controlli di uso comune.
-   **Non usare le barre dei menu nelle finestre di dialogo.** In questo caso è difficile assegnare chiavi di accesso univoche, perché le voci di menu e i controlli della finestra di dialogo condividono gli stessi caratteri.

### <a name="shortcut-keys"></a>Combinazioni di tasti

-   **Assegnare i tasti di scelta rapida ai comandi usati più di frequente.** I programmi e le funzionalità usati raramente non necessitano di tasti di scelta rapida perché gli utenti possono usare le chiavi di accesso.
-   **Non creare un tasto di scelta rapida l'unico modo per eseguire un'attività.** Gli utenti devono inoltre essere in grado di utilizzare il mouse o la tastiera con la scheda, la freccia e le chiavi di accesso.
-   **Non assegnare significati diversi ai tasti di scelta rapida noti.** Poiché vengono memorizzati, i significati incoerenti per i collegamenti noti sono frustranti ed è soggetta a errori.
-   **Non tentare di assegnare i tasti di scelta rapida del programma a livello di sistema.** I tasti di scelta rapida del programma avranno effetto solo quando il programma ha lo stato attivo per l'input.
-   **Documentare tutti i tasti di scelta rapida.** Collegamenti ai documenti in elementi della barra dei menu, descrizioni comandi della barra degli strumenti e un singolo articolo della guida che documenta tutti i tasti di scelta rapida utilizzati. Questa operazione consente agli utenti di apprendere le assegnazioni dei tasti di scelta rapida che non devono essere un segreto.

    -   **Eccezione:** Non visualizzare le assegnazioni dei tasti di scelta rapida nei menu di scelta rapida. I menu di scelta rapida non visualizzano le assegnazioni dei tasti di scelta rapida perché questi menu sono ottimizzati per l'efficienza.

    ![screenshot della descrizione comando per il tasto di scelta rapida grassetto ](images/inter-keyboard-image19.png)

    Il tasto di scelta rapida è documentato nella descrizione comando.

-   **Se il programma assegna molti tasti di scelta rapida, fornire la possibilità di personalizzare le assegnazioni.** In questo modo gli utenti possono riassegnare i tasti di scelta rapida in conflitto ed eseguire la migrazione da altri prodotti. La maggior parte dei programmi non assegna abbastanza tasti di scelta rapida per richiedere questa funzionalità.

### <a name="choosing-shortcut-keys"></a>Scelta di tasti di scelta rapida

-   **Per i tasti di scelta rapida noti, usare le assegnazioni standard.**
-   **Per le assegnazioni di chiavi non standard, usare i tasti di scelta rapida consigliati seguenti per i comandi usati più di frequente.** Questi tasti di scelta rapida sono consigliati perché non sono in conflitto con i collegamenti noti e sono facili da premere.
    -   CTRL + G, J, K, L M, Q, R o T
    -   CTRL + qualsiasi numero
    -   F7, F8, F9 o F12
    -   MAIUSC + F2, F3, F4, F5, F7, F8, F9, F11 o F12
    -   Alt + qualsiasi tasto funzione eccetto F4
-   **Usare i tasti di scelta rapida consigliati seguenti per i comandi usati meno di frequente.** Questi tasti di scelta rapida non presentano conflitti, ma sono più difficili da premere spesso che richiedono due mani.
    -   CTRL + qualsiasi tasto funzione eccetto F4 e F6
    -   CTRL + MAIUSC + qualsiasi lettera o numero
-   **È facile ricordare i tasti di scelta rapida usati di frequente:**
    -   Usare lettere anziché numeri o tasti funzione.
    -   Provare a usare una lettera inclusa nella prima parola o nella maggior parte dei caratteri memorabili all'interno delle parole chiave del comando.
-   **Usare i tasti funzione per i comandi che hanno un effetto su scala ridotta,** ad esempio i comandi che si applicano all'oggetto selezionato. Ad esempio, F2 Rinomina l'elemento selezionato.
-   **Usare le combinazioni di tasti CTRL per i comandi che hanno un effetto su larga scala,** ad esempio i comandi che si applicano a un intero documento. Ad esempio, CTRL + S Salva il documento corrente.
-   **Usare le combinazioni di tasti MAIUSC per i comandi che estendono o completano le azioni del tasto di scelta rapida standard.** Ad esempio, il tasto di scelta rapida Alt + Tab scorre le finestre primarie aperte, mentre ALT + MAIUSC + TAB viene cicli nell'ordine inverso. Analogamente, F1 Visualizza la guida, mentre MAIUSC + F1 Visualizza la Guida sensibile al contesto.
-   **Quando si usano i tasti di direzione per spostare o ridimensionare un elemento, usare Ctrl + tasti di direzione per un controllo più granulare.**

### <a name="choosing-shortcut-keys-what-not-to-do"></a>Scelta di tasti di scelta rapida

-   **Non distinguere tra percorsi chiave.** Ad esempio, Windows può distinguere tra lo spostamento sinistro e destro, ALT, CTRL, il [logo Windows](glossary.md)e le [chiavi dell'applicazione](glossary.md), nonché le chiavi del tastierino numerico. L'assegnazione del comportamento a una sola posizione chiave è confusa e imprevista.
-   **Non usare il tasto di modifica logo Windows per i tasti di scelta rapida del programma.** Il tasto logo Windows è riservato per l'utilizzo di Windows. Anche se una combinazione di tasti logo Windows non è attualmente utilizzata da Windows, è possibile che sia in futuro.
-   **Non usare la chiave dell'applicazione come modificatore del tasto di scelta rapida.** Usare invece CTRL, ALT e MAIUSC.
-   **Non usare i tasti di scelta rapida usati da Windows per i tasti di scelta rapida del programma.** Questa operazione sarà in conflitto con i tasti di scelta rapida del sistema Windows quando il programma ha lo stato attivo per l'input.
-   **Non usare combinazioni di tasti ALT + alfanumerici per i tasti di scelta rapida.** Questi tasti di scelta rapida possono entrare in conflitto con le chiavi di accesso.
-   **Non usare i caratteri seguenti per i tasti di scelta rapida:** @ $ {} \[ \] \\  ~  \| ^'  < >. Questi caratteri richiedono combinazioni di chiavi diverse tra le lingue o sono specifiche delle impostazioni locali.
-   **Evitare combinazioni di chiavi complesse,** ad esempio tre o più chiavi, ad esempio CTRL + ALT + barra spaziatrice, o chiavi che sono distanti sulla tastiera, ad esempio CTRL + F5. Usare semplici tasti di scelta rapida per i comandi usati di frequente.
-   **Non usare combinazioni CTRL + ALT** perché Windows interpreta questa combinazione in alcune versioni del linguaggio come chiave AltGr, che genera caratteri alfanumerici.

### <a name="keyboard-and-mouse-combinations"></a>Combinazioni di tastiera e mouse

-   Per i collegamenti, usare Maiusc + clic per spostarsi usando una nuova finestra e CTRL + clic per spostarsi usando una nuova scheda. Questo approccio è coerente con Windows Internet Explorer.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alla tastiera:

-   Utilizzare la tastiera su schermo per fare riferimento a una rappresentazione della tastiera sullo schermo che l'utente tocca ai caratteri di input.
-   Assegnare le combinazioni di tasti iniziali con il tasto di modifica. Presentare i tasti di modifica nell'ordine seguente: logo Windows, applicazione, CTRL, ALT, MAIUSC. Se viene usato il modificatore del tastierino numerico, inserirlo immediatamente prima della chiave che modifica.
-   Non usare lettere maiuscole per i tasti di scelta rapida. Seguire invece le maiuscole usate dalle tastiere standard o minuscole se la chiave non è etichettata sulla tastiera.
    -   Per le combinazioni di tasti alfabetici, utilizzare una lettera maiuscola.
    -   Pagina di ortografia, PGGIÙ, schermo e blocco a scorrimento.
    -   Digitato segno più, segno meno, trattino, punto e virgola.
    -   Per i tasti di direzione, utilizzare freccia sinistra, freccia destra, freccia su e freccia giù. Non usare etichette grafiche per i tasti di direzione.
    -   Usare il tasto logo Windows e la chiave applicazione per fare riferimento alle chiavi etichettate con le icone. Non usare etichette grafiche per queste chiavi.

**Corretto:**

barra spaziatrice, TAB, invio, PGSU, CTRL + ALT + CANC, ALT + W, CTRL + segno più

**Non corretto:**

BARRA SPAZIAtrice, TAB, invio, PG su, CTRL + ALT + CANC, ALT + w, CTRL + +

-   Indica le combinazioni di tasti con un segno più, senza spazi.

**Corretto:**

CTRL + A, MAIUSC + F5

**Non corretto:**

CTRL + A, MAIUSC + F5

-   Per mostrare una combinazione di tasti che include la punteggiatura che richiede l'uso del tasto MAIUSC, ad esempio il punto interrogativo, aggiungere Shift alla combinazione e assegnare il nome o il simbolo della chiave spostata. L'utilizzo del nome della chiave non spostata, ad esempio 4 anziché $, potrebbe generare confusione per gli utenti o addirittura errato; ad esempio, il? i caratteri e/non sono sempre chiavi spostate su ogni tastiera.

**Corretto:**

CTRL + MAIUSC +?, CTRL + MAIUSC + \* , Ctrl + Maiusc + virgola

**Non corretto:**

CTRL + MAIUSC +/, CTRL +?, CTRL + MAIUSC + 8, CTRL +\*

-   Prima di tutto, usare la chiave e con il nome della chiave, se necessario, per maggiore chiarezza, ad esempio il tasto F1. Per tutti i riferimenti successivi, fare riferimento alla chiave solo in base al nome, ad esempio, premere F1.
-   Fare riferimento in modo specifico alle chiavi di accesso e ai tasti di scelta rapida nella programmazione e in altri documenti tecnici. Non usare tasti di scelta rapida, tasto di scelta o tasti di scelta rapida. In tutti gli altri casi, usare i tasti di scelta rapida, specialmente nella documentazione utente.

Quando si fa riferimento all'interazione:

-   Utilizzare premere, non decomprimere, colpire, colpire o digitare, quando si preme e si rilascia immediatamente una chiave avvia un'azione all'interno del programma o si sposta all'interno di un documento o di un'interfaccia utente.
-   Utilizzare tipo, non immettere, per indicare agli utenti di digitare il testo.
-   Utilizzare l'utilizzo in situazioni in cui la pressione di un tasto può causare confusione, ad esempio quando si fa riferimento a un tipo di chiave, ad esempio i tasti di direzione o i tasti funzione. In questi casi, è possibile che gli utenti richiedano di premere tutte le chiavi contemporaneamente.
-   Utilizzare la pressione tenendo premuto un tasto, ad esempio un tasto di modifica.
-   Non utilizzare premere come sinonimo di clic.

Esempi:

-   Digitare il nome e quindi premere INVIO.
-   Premere CTRL + F, quindi digitare il testo che si desidera cercare.
-   Per salvare il file, premere Y.
-   Per spostare il punto di inserimento, utilizzare i tasti di direzione.

 

