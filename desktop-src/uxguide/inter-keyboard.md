---
title: Tastiera
description: La tastiera è il dispositivo di input principale usato per l'input di testo in Microsoft Windows. Per accessibilità ed efficienza, la maggior parte delle azioni può essere eseguita anche tramite la tastiera.
ms.assetid: 27185c98-1233-4e26-a156-0ff080fd4db3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c1554ca1a9769b562f154498cd0871bc1b813067
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524296"
---
# <a name="keyboard"></a>Tastiera

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

La tastiera è il dispositivo di input principale usato per l'input di testo in Microsoft Windows. Per accessibilità ed efficienza, la maggior parte delle azioni può essere eseguita anche tramite la tastiera.

Le tastiere possono anche fare riferimento a tastiere virtuali su schermo e a pad di scrittura usati da computer senza tastiera fisica, ad esempio computer basati su tablet.

![Screenshot della tastiera su schermo ](images/inter-keyboard-image1.png)

Tastiera su schermo della tecnologia tablet e tocco di Windows.

![Screenshot del blocco di scrittura del tablet Windows ](images/inter-keyboard-image2.png)

Il pannello di scrittura per tablet e tecnologia touch di Windows.

Esistono sei tipi di chiavi di base:

-   Un tasto carattere invia un carattere letterale alla finestra con lo stato attivo per l'input.
-   Un tasto di modifica combinato con un altro tasto modifica il significato del tasto associato, ad esempio CTRL, ALT, MAIUSC e il tasto logo Windows.
-   I tasti di spostamento sono le frecce direzionali, oltre a Home, Fine, PGGI IN SU e PGGI GIÙ.
-   I tasti di modifica sono Insert, Backspace e Delete.
-   I tasti funzione sono da F1 a F12.
-   I tasti di sistema impostano il sistema in una modalità o eseguono un'attività di sistema, ad esempio Stampa schermo, BLOC MAIUSC e BLOC NUM.

I tasti di scelta sono tasti o combinazioni di tasti usati per l'accessibilità per interagire con tutti i controlli o le voci di menu usando la tastiera. I tasti di scelta rapida sono tasti o combinazioni di tasti usati dagli utenti avanzati per eseguire i comandi usati di frequente per migliorare l'efficienza. Windows indica i tasti di scelta sottolineando l'assegnazione della chiave di accesso.

![Screenshot dei tasti di scelta e dei tasti di scelta rapida ](images/inter-keyboard-image3.png)

Questo esempio mostra sia i tasti di scelta che i tasti di scelta rapida.

Per evitare confusione visiva, Windows nasconde le sottolineature dei tasti di scelta per impostazione predefinita e le visualizza solo quando si preme ALT. Per mantenere la coerenza con Windows, le immagini nella Guida all'esperienza utente vengono visualizzate anche con le sottolineature dei tasti di scelta nascoste, a meno che le linee guida non prescindono da tasti di scelta.

Per migliorare la consapevolezza delle assegnazioni delle chiavi di accesso nel programma durante il processo di sviluppo, è possibile visualizzarle in qualsiasi momento. In Pannello di controllo, passare al Centro accessibilità e fare clic su Make the keyboard easier to use ( Semplifica l'uso **della tastiera).** selezionare quindi la casella **di controllo Sottolinea tasti di scelta rapida** e tasti di scelta.

**Nota:** Le linee guida relative [all'accessibilità](inter-accessibility.md) sono presentate in un articolo separato.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="elements-of-keyboard-navigation"></a>Elementi dello spostamento tramite tastiera

Gli utenti interagiscono con una finestra usando la tastiera passando ai controlli, effettuando selezioni ed eseguendo comandi. Gli elementi seguenti funzionano insieme per eseguire questa operazione.

![Screenshot della finestra di dialogo Modifica colori ](images/inter-keyboard-image4.png)

Per illustrare gli elementi della navigazione da tastiera nell'elenco seguente, si fa riferimento a questa finestra di dialogo.

-   **Stato attivo per l'input.** Il controllo con lo stato attivo per l'input riceve la maggior parte dell'input da tastiera. Lo stato attivo per l'input è indicato da un rettangolo punteggiato denominato rettangolo di attivazione. Alcuni input da tastiera vengono inviati ai controlli che non hanno lo stato attivo per l'input, come illustrato più avanti.

    ![Screenshot della prima riga nella finestra di dialogo Modifica colori ](images/inter-keyboard-image5.png)

    Il primo controllo Colori di base ha lo stato attivo per l'input, come indicato da un rettangolo punteggiato.

-   **Tasto TAB e tabulazioni.** Il tasto TAB è il meccanismo principale per spostarsi all'interno di una finestra. Il tasto TAB visita solo i controlli con una tabulazione. Tutti i controlli interattivi dovrebbero avere delle tabulazioni (a meno che non siano in un gruppo), a differenza dei controlli non interattivi, come le etichette.
-   **Ordine di tabulazione.** Tutti i controlli con tabulazioni vengono visitati in ordine di tabulazione. Premendo TAB, lo stato attivo per l'input viene spostato sul controllo successivo in ordine di tabulazione, mentre premendo MAIUSC+TAB lo stato attivo per l'input viene spostato sul controllo precedente.
-   **Gruppi di controllo.** È possibile creare un set di controlli correlati in un gruppo e assegnare una singola tabulazione. I gruppi di controlli vengono usati per i set di controlli che si comportano come un singolo controllo, ad esempio i pulsanti di opzione. Possono essere usati anche quando i controlli sono troppi per poter navigare in modo efficiente solo con il tasto TAB.

    ![Screenshot dei gruppi di colori di base e personalizzati ](images/inter-keyboard-image6.png)

    I colori di base e i colori personalizzati sono gruppi di controlli, offrendo a questa finestra di dialogo cinque tabulazioni. Esistono così tanti controlli che la navigazione sarebbe inefficiente senza usare gruppi di controlli.

-   **Tasti di direzione** I tasti di direzione spostano lo stato attivo per l'input tra i controlli all'interno di un gruppo. Premendo il tasto freccia DESTRA, lo stato attivo per l'input viene spostato sul controllo successivo in ordine di tabulazione, mentre premendo la freccia sinistra lo stato attivo per l'input viene spostato sul controllo precedente. Anche Home, End, Up e Down hanno il comportamento previsto all'interno di un gruppo. Gli utenti non possono uscire da un gruppo di controlli usando i tasti di direzione.
-   **Pulsanti predefiniti.** Le finestre con pulsanti di comando e collegamenti di comando hanno un singolo pulsante predefinito indicato da un bordo evidenziato, ovvero il pulsante su cui si fa clic quando si preme INVIO. Per impostazione predefinita, è assegnato un solo pulsante di comando o collegamento di comando predefinito. Tuttavia, il pulsante predefinito si sposta quando l'utente passa a un altro pulsante di comando o a un altro collegamento di comando. Di conseguenza, anche qualsiasi pulsante di comando o collegamento di comando con lo stato attivo per l'input è sempre il pulsante predefinito.

    ![Screenshot dei pulsanti OK e Cancel ](images/inter-keyboard-image7.png)

    Il pulsante OK è in genere il pulsante predefinito, come indicato dal bordo evidenziato. Tuttavia, se l'utente deve premere TAB per il pulsante Annulla, diventa il pulsante predefinito e viene attivato con il tasto INVIO.

-   **Barra spaziatrice, INVIO ed ESC.** La barra spaziatrice attiva il controllo con lo stato attivo per l'input, mentre il tasto INVIO attiva il pulsante predefinito. Se si preme ESC, la finestra viene annullata o chiusa.
-   **Chiavi di accesso.** I tasti di scelta vengono usati per interagire direttamente con i controlli anziché spostarsi con TAB. Vengono combinati con il tasto ALT e indicati con una lettera sottolineata nell'etichetta.
-   **Etichette delle chiavi di accesso.** Mentre alcuni controlli contengono etichette proprie, ad esempio pulsanti di comando, caselle di controllo e pulsanti di opzione, altri controlli hanno etichette esterne, ad esempio caselle di riepilogo e visualizzazioni albero. Per le etichette esterne, il tasto di scelta viene assegnato all'etichetta e, se richiamato, passa al controllo successivo in ordine di tabulazione. Ai pulsanti con etichetta OK, Annulla e Chiudi non vengono assegnati tasti di scelta perché vengono richiamati con INVIO ed ESC.

    ![Screenshot delle etichette con "b" e "d" sottolineati ](images/inter-keyboard-image8.png)

    Premendo ALT+B si passa al colore di base selezionato, premendo ALT+D si fa clic sul pulsante Definisci colori personalizzati, INVIO richiama il pulsante OK e ESC richiama Annulla.

-   **Comportamento della chiave di accesso.** Quando un tasto di scelta viene richiamato e assegnato in modo univoco, viene fatto clic sul controllo associato. Se l'assegnazione non è univoca, al controllo associato viene assegnato lo stato attivo per l'input. Se l'utente ha di nuovo immesso lo stesso tasto di scelta, al controllo successivo in ordine di tabulazione con la stessa assegnazione viene assegnato lo stato attivo per l'input.

Anche se questo meccanismo è piuttosto complicato, è anche piuttosto intuitivo. Gli utenti prelevano la maggior parte di questi dettagli immediatamente, anche se pochi possono spiegare esattamente come funzionano.

### <a name="keyboard-support-for-accessibility-and-advanced-users"></a>Supporto della tastiera per l'accessibilità e gli utenti avanzati

**In Windows la progettazione per la tastiera si riduce a fornire una navigazione da tastiera ben progettata, i tasti di scelta per l'accessibilità e i tasti di scelta rapida per gli utenti avanzati.**

Per garantire che la funzionalità del programma sia facilmente disponibile per la più ampia gamma di utenti, inclusi quelli con disabilità e problemi, tutti gli elementi dell'interfaccia utente interattiva devono essere accessibili tramite tastiera. In genere, ciò significa che gli elementi dell'interfaccia utente usati più di frequente sono accessibili usando un singolo tasto di scelta o una combinazione di tasti, mentre gli elementi usati meno di frequente possono richiedere un'ulteriore navigazione tramite tasto tab o tasto di direzione. Per questi utenti, la completezza è più importante della coerenza.

Per garantire che le funzionalità del programma siano efficienti per gli utenti esperti, gli elementi dell'interfaccia utente di uso comune devono avere anche tasti di scelta rapida per l'accesso diretto tramite tastiera. Gli utenti esperti spesso preferiscono usare la tastiera, perché i comandi basati sulla tastiera possono essere immessi più rapidamente e senza dover togliere le mani dalla tastiera. Per questi utenti, efficienza e coerenza sono indispensabili. La completezza è importante solo per i comandi usati più di frequente.

Esistono piccole distinzioni quando si progetta l'accesso tramite tastiera per questi due gruppi, motivo per cui Windows offre due meccanismi indipendenti di accesso diretto alla tastiera. Usando in modo efficace sia l'accesso che i tasti di scelta rapida, è possibile offrire ai programmi un accesso da tastiera efficiente, coerente e completo che offre vantaggi a tutti.

### <a name="access-keys"></a>Chiavi di accesso

I tasti di scelta presentano le caratteristiche seguenti:

-   Usano il tasto ALT e un tasto alfanumerico.
-   Servono principalmente per l'accessibilità.
-   Vengono assegnati a tutti i menu e alla maggior parte dei controlli delle finestre di dialogo.
-   Non è previsto che vengano memorizzati e quindi vengono documentati direttamente nell'interfaccia utente sottolineando il carattere corrispondente dell'etichetta del controllo.
-   Hanno effetto solo nella finestra corrente e passano alla voce di menu o al controllo corrispondente.
-   Non è sempre possibile assegnarli in modo coerente, ma lo si dovrebbe fare per i comandi più usati, soprattutto i pulsanti di conferma.
-   Vengono localizzati.

Poiché le chiavi di accesso non sono progettate per essere memorizzate, vengono assegnate a un carattere che si trova **all'inizio dell'etichetta** per facilitarle l'individuazione, anche se è presente una parola chiave che viene visualizzata più avanti nell'etichetta.

**Corretto:**

![Schermata del primo carattere nell'etichetta sottolineata ](images/inter-keyboard-image9.png)

**Non corretto:**

![screenshot del ventiuno carattere sottolineato ](images/inter-keyboard-image10.png)

Nell'esempio corretto il tasto di scelta viene assegnato a un carattere all'inizio dell'etichetta.

### <a name="shortcut-keys"></a>Combinazioni di tasti

Al contrario, i tasti di scelta rapida hanno le caratteristiche seguenti:

-   Usano soprattutto le sequenze di tasti funzione e CTRL. Le combinazioni di tasti dei sistemi Windows usano anche ALT+tasti non alfanumerici e il tasto WINDOWS.
-   Servono soprattutto a garantire efficienza agli utenti avanzati.
-   Vengono assegnati solo ai comandi usati più comunemente.
-   È previsto che vengano memorizzati e vengono documentati solo nei menu, nelle descrizioni comandi e nella Guida.
-   Hanno effetto in tutto il programma, ma non hanno effetto se non vengono applicati.
-   Devono essere assegnati in modo coerente perché vengono memorizzati e non sono documentati direttamente.
-   Non vengono localizzati.

Poiché i tasti di scelta rapida devono essere memorizzati, i tasti di scelta rapida usati più di frequente usano idealmente lettere del primo o più facile da ricordare **all'interno** delle parole chiave del comando, ad esempio CTRL+C per Copia e CTRL+Q per la richiesta.

Significati incoerenti per i tasti di scelta rapida noti sono frustranti e causano errori.

**Non corretto:**

![Screenshot del pulsante Avanti con la sottolineatura "w" ](images/inter-keyboard-image11.png)

In questo esempio CTRL+F è il tasto di scelta rapida standard per Trova, quindi l'assegnazione a Avanti è frustrante e erta. CTRL+W sarebbe una scelta migliore e facile da ricordare.

Infine, poiché sono destinati a essere memorizzati, i tasti di scelta rapida specifici dell'applicazione hanno senso solo per i programmi e le funzionalità eseguiti con una frequenza sufficiente per consentire agli utenti **motivati di memorizzare.** I programmi e le funzionalità usati raramente non necessitano di tasti di scelta rapida. Ad esempio, i programmi di installazione e la maggior parte delle procedure guidate non necessitano di assegnazioni di tasti di scelta rapida speciali né di comandi usati raramente in un'applicazione per la produttività.

### <a name="assigning-access-keys-in-dialog-boxes"></a>Assegnazione di chiavi di accesso nelle finestre di dialogo

Quando possibile, assegnare chiavi di accesso univoche a tutti i controlli interattivi, ad eccezione di quelli a cui in genere non sono assegnate chiavi di accesso. Tuttavia, in inglese sono presenti solo 26 caratteri. Alcuni caratteri potrebbero non essere presenti in nessuna delle etichette e potrebbero non essere presenti caratteri distintivi in tutte le etichette, riducendo ulteriormente questo numero. È inoltre consigliabile pianificare alcuni caratteri non assegnati per facilitare la localizzazione. Di conseguenza, è possibile assegnare solo circa 20 chiavi di accesso univoche in una singola finestra di dialogo.

Se è presente una finestra di dialogo con più di 20 controlli interattivi, non assegnare chiavi di accesso ad alcuni controlli o, in rare situazioni, assegnare chiavi di accesso duplicate.

![Screenshot della finestra di dialogo tipo di carattere ](images/inter-keyboard-image12.png)

Quando sono presenti molti controlli interattivi, non tutti necessitano di una chiave di accesso assegnata.

Usare la procedura generale seguente per assegnare le chiavi di accesso:

-   In primo luogo, assegnare i tasti di scelta ai [pulsanti di commit e](glossary.md) ai collegamenti di comando. Usare la tabella delle assegnazioni di chiavi di accesso standard quando viene applicata. In caso contrario, usare la prima lettera della prima parola.
-   Ignorare i controlli a cui non sono assegnate chiavi di accesso.
-   Assegnare chiavi di accesso univoche ai controlli rimanenti (a partire da quello usato più di frequente):
    -   Se possibile, assegnare la chiave di accesso in base alla tabella delle assegnazioni standard delle chiavi di accesso.
    -   In caso contrario:
        -   Indica la preferenza per i caratteri visualizzati all'inizio dell'etichetta, idealmente il primo carattere della prima o della seconda parola.
        -   Preferisce una consonante distintiva o una vocale, ad esempio "x" in "Exit".
        -   Preferisce caratteri con larghezze ampie, ad esempio w, m e lettere maiuscole.
        -   Evitare di usare caratteri che rendono difficile la sottolineatura, ad esempio lettere larghe di un pixel, lettere con discendenti e lettere accanto a una lettera con un discendente.
-   Se non tutti i controlli possono avere chiavi di accesso univoche (iniziare con il meno frequentemente usato):
    -   Se sono presenti gruppi di controlli correlati, ad esempio:
        -   Un singolo set di pulsanti di opzione
        -   Un set di caselle di controllo correlate
        -   Set di controlli correlati all'interno di una casella di gruppo

Assegnare i tasti di scelta alle etichette di gruppo anziché ai singoli controlli. In genere, si farebbe il contrario. In questo modo, assicurarsi che sia definito un gruppo di controlli per questi controlli.

-   Se ancora non tutti i controlli possono avere chiavi di accesso univoche:
    -   È possibile assegnare chiavi di accesso non univoche se:
        -   In caso contrario, sarebbe troppo difficile spostarsi tra i controlli.
        -   Le chiavi di accesso non univoche non sono in conflitto con le chiavi di accesso dei controlli di uso comune.
    -   In caso contrario, è possibile accedere ai controlli rimanenti usando la navigazione tramite TAB e i tasti di direzione.

![Screenshot di gruppi con chiavi di accesso diverse ](images/inter-keyboard-image13.png)

In questo esempio sono presenti controlli ripetitivi, quindi i tasti di scelta vengono assegnati ai gruppi di pulsanti di opzione.

### <a name="preventing-accidental-commands"></a>Prevenzione di comandi accidentali

Se una finestra visualizzata fuori contesto (non avviata dall'utente) sottrai lo stato attivo per l'input, è probabile che questa finestra riceva l'input destinato a un'altra finestra. Inoltre, i tasti di scelta hanno effetto quando vengono premuti senza premere ALT se nella finestra di dialogo non sono presenti controlli che accettano input di testo, ad esempio caselle di testo ed elenchi. Nell'esempio seguente, quindi, premendo "r" viene attivato il pulsante Riavvia ora.

Ovviamente, tale input può avere conseguenze impreviste significative.

**Non corretto:**

![screenshot del pulsante Riavvia ora, 'r' sottolineato ](images/inter-keyboard-image14.png)

In questo esempio, la digitazione di testo con spazio, "r" o INVIO riavvia accidentalmente Windows.

Naturalmente, la soluzione migliore a questo problema è non sottrarre lo stato attivo all'input. Al contrario, eseguire il flash del pulsante della barra delle applicazioni [del](winenv-taskbar.md) programma o visualizzare una notifica per ottenere l'attenzione dell'utente.

Tuttavia, se è necessario visualizzare una finestra di questo tipo, l'approccio migliore consiste nell'non assegnare un pulsante predefinito o i tasti di scelta e assegnare lo stato attivo per l'input iniziale a un controllo diverso da un pulsante di commit.

**Corretto:**

![screenshot del pulsante di riavvio, 'r' non sottolineato ](images/inter-keyboard-image15.png)

In questo esempio il riavvio accidentale di Windows è molto più difficile.

**Se si eservino solo sei operazioni...**

1.  Progettare una buona navigazione tramite tastiera, con un ordine di tabulazione appropriato e gruppi di controlli appropriati, lo stato attivo per l'input iniziale e i pulsanti predefiniti.
2.  Assegnare i tasti di scelta a tutti i menu e alla maggior parte dei controlli.
3.  Assegnare i tasti di scelta a un carattere visualizzato all'inizio dell'etichetta, per facilitarle l'individuazione.
4.  Assegnare i tasti di scelta rapida ai comandi usati più di frequente.
5.  Provare ad assegnare i tasti di scelta rapida al primo o più facile da ricordare all'interno di parole chiave.
6.  Assegnare un significato coerente ai tasti di scelta rapida noti.

## <a name="guidelines"></a>Indicazioni

### <a name="interaction"></a>Interazione

-   **Non usare MAIUSC per modificare i comandi nei menu o nelle finestre di dialogo.** Questa operazione non è rilevabile e imprevista.

    **Non corretto:**

    ![Screenshot della finestra di dialogo conferma sostituzione cartella ](images/inter-keyboard-image16.png)

    In questo esempio di Windows XP, tenendo premuto MAIUSC si sostituisce Sì a Tutti con No a Tutti.

-   **Non disabilitare un controllo con lo stato attivo per l'input. Questa operazione potrebbe impedire alla finestra di ricevere l'input da tastiera.** Al contrario, prima di disabilitare un controllo con lo stato attivo per l'input, spostare lo stato attivo per l'input su un altro controllo.
-   **Se una finestra viene visualizzata all'insito nel contesto e potenzialmente sorprendente, potrebbe essere necessario evitare conseguenze impreviste significative:**
    -   Non assegnare un pulsante predefinito.
    -   Non assegnare chiavi di accesso.
    -   Assegnare lo stato attivo per l'input iniziale a un controllo diverso da un pulsante di commit.

### <a name="keyboard-navigation"></a>Spostamento tramite tastiera

-   **Visualizzare sempre l'indicatore dello stato attivo di input. Eccezione:** è possibile eliminare temporaneamente l'indicatore dello stato attivo di input se:
    -   L'indicatore dello stato attivo per l'input distrae visivamente (come con una visualizzazione elenco di grandi dimensioni non nella visualizzazione Dettagli).
    -   L'utilizzo del tasto INVIO è probabilmente preceduto da altri input da tastiera, ad esempio ALT o i tasti di direzione.
    -   L'indicatore dello stato attivo per l'input viene visualizzato su qualsiasi input da tastiera.
-   **Assegnare lo stato attivo per l'input** iniziale al controllo con cui è più probabile che gli utenti interagiscano per primi, che spesso è il primo controllo interattivo. Se il primo controllo interattivo non è una scelta ottimale, è consigliabile modificare il layout della finestra.
-   **Assegnare tabulazioni a tutti i controlli interattivi, incluse le caselle di modifica di sola lettura. Eccezioni:**
    -   Gruppi di controlli correlati che si comportano come un singolo controllo, ad esempio pulsanti di opzione. Tali gruppi hanno una singola tabulazione.
    -   Contenere correttamente i gruppi in modo che i tasti di direzione esercitino il ciclo avanti e indietro all'interno del gruppo e rimangano all'interno del gruppo.
-   **L'ordine di tabulazione deve seguire l'ordine di lettura, che in genere scorre da sinistra a destra, dall'alto verso il basso.** Prendere in considerazione la possibilità di creare eccezioni per i controlli di uso comune inserendoli in precedenza nell'ordine di tabulazione. Tab deve scorrere tutte le tabulazioni in entrambe le direzioni senza arrestarsi.
-   **All'interno di una tabulazione, l'ordine dei tasti di** direzione deve scorrere da sinistra a destra, dall'alto verso il basso, senza eccezioni. I tasti di direzione devono scorrere tutti gli elementi in entrambe le direzioni senza arrestarsi.
-   **Presentare i pulsanti di commit nell'ordine seguente:**
    -   OK/ \[ Eseguire \] l'operazione /Sì
    -   \[Non eseguire questa operazione \] /No
    -   Annulla
    -   Applica (se presente)

dove \[ Do it e \] \[ Don't do it \] sono risposte specifiche all'istruzione main.

-   **Selezionare il pulsante di comando o il collegamento di comando più sicuro (per evitare la perdita di dati o l'accesso al sistema) e il pulsante di comando o il collegamento di comando più sicuro come impostazione predefinita.** Se la sicurezza e la sicurezza non sono fattori, selezionare la risposta più probabile o conveniente.
-   **La navigazione tramite tastiera non deve modificare i valori del controllo né causare un messaggio di errore.** Non richiedere mai agli utenti di modificare il valore iniziale di un controllo durante lo spostamento. Inizializzare invece i controlli che convalidano all'uscita con valori validi e convalidare il valore di un controllo solo quando è stato modificato.

### <a name="access-keys"></a>Chiavi di accesso

-   **Quando possibile, assegnare le chiavi di accesso per i comandi di uso comune in base alla tabella seguente.** Anche se le assegnazioni coerenti dei tasti di scelta non sono sempre possibili, sono sicuramente preferibili soprattutto per i comandi usati di frequente.

    |  Chiave di accesso         | Comando                             |
    |---------------------------|-------------------------------------------|
    | Una<br/>              | Informazioni<br/>                          |
    | Una<br/>              | Sempre in primo piano<br/>                  |
    | Una<br/>              | Applica<br/>                          |
    | B<br/>              | Indietro<br/>                           |
    | B<br/>              | Bold<br/>                           |
    | B o r<br/>         | Esplora<br/>                         |
    | C<br/>              | Chiudi<br/>                          |
    | C<br/>              | Copia<br/>                           |
    | C<br/>              | Copiare qui<br/>                      |
    | s<br/>              | Crea collegamento<br/>                |
    | s<br/>              | Creare un collegamento qui<br/>           |
    | t<br/>              | Taglia<br/>                            |
    | D<br/>              | Delete<br/>                         |
    | D<br/>              | Non visualizzare più questo \[ \] elemento<br/> |
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
    | t<br/>              | argomenti della Guida<br/>                    |
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
    | P<br/>              | Stampare qui<br/>                     |
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
-   **Preferire una consonante distintiva o una vocale,** ad esempio "x" in "Exit".
-   **Evitare di usare caratteri che rendono difficile la sottolineatura,** ad esempio (dal più problematico al meno problematico):
    -   Caratteri di larghezza di un solo pixel, ad esempio i e l.
    -   Caratteri con discendenti, ad esempio g, j, p, q e y.
    -   Caratteri accanto a una lettera con un discendente.
-   Quando si assegnano chiavi di accesso nelle pagine della procedura guidata, ricordarsi di riservare "B" per Indietro e "N" per Avanti.
-   Quando si assegnano chiavi di accesso nelle pagine delle proprietà, ricordarsi di riservare "A" per Applica, se usato.

### <a name="menu-access-keys"></a>Tasti di scelta dei menu

-   **Assegnare i tasti di scelta a tutte le voci di menu.** Nessuna eccezione.
-   **Per le voci di menu dinamico,ad esempio i file usati di recente, assegnare numericamente i tasti di scelta.**

    ![Screenshot delle voci di menu con tasti di scelta numerici ](images/inter-keyboard-image17.png)

    In questo esempio, il programma Paint in Windows assegna tasti di scelta numerici ai file usati di recente.

-   **Assegnare chiavi di accesso univoche all'interno di un livello di menu.** È possibile riutilizzare le chiavi di accesso a livelli di menu diversi.
-   **Semplificare l'individuazione delle chiavi di accesso:**
    -   Per le voci di menu usate più di frequente, scegliere i caratteri all'inizio della prima o della seconda parola dell'etichetta, preferibilmente il primo carattere.
    -   Per le voci di menu usate meno di frequente, scegliere lettere consonanti distintive o vocali nell'etichetta.

### <a name="dialog-box-access-keys"></a>Tasti di scelta della finestra di dialogo

-   **Quando possibile, assegnare chiavi di accesso univoche a tutti i controlli interattivi o alle relative etichette.** [Le caselle di testo di sola](ctrl-text-boxes.md) lettura sono controlli interattivi(perché gli utenti possono scorrerle e copiare testo), quindi traggono vantaggio dai tasti di scelta. **Non assegnare chiavi di accesso a:**
    -   **Pulsanti OK, Annulla e Chiudi.** I tasti invio e ESC vengono usati per le chiavi di accesso. Tuttavia, assegnare sempre un tasto di scelta a un controllo che indica OK o Annulla, ma con un'etichetta diversa.

        ![Screenshot della finestra di dialogo con pulsanti Sì e No ](images/inter-keyboard-image18.png)

        In questo esempio, al pulsante commit positivo è assegnata una chiave di accesso.

    -   **Raggruppare le etichette.** In genere, ai singoli controlli all'interno di un gruppo vengono assegnati tasti di scelta, quindi l'etichetta del gruppo non ne richiede uno. Tuttavia, assegnare una chiave di accesso all'etichetta del gruppo e non i singoli controlli in caso di mancanza di chiavi di accesso.
    -   **Pulsanti della Guida generica a** cui si accede con F1.
    -   **Collegare le etichette.** Spesso sono presenti troppi collegamenti per assegnare chiavi di accesso univoche e i caratteri di sottolineatura dei collegamenti nascondono i caratteri di sottolineatura dei tasti di scelta. Fare in modo che gli utenti accedono ai collegamenti con il tasto TAB.
    -   **Nomi delle schede.** Le schede vengono spostate in ciclo usando CTRL+TAB e CTRL+MAIUSC+TAB.
    -   **Pulsanti Sfoglia con etichetta "...".** Non è possibile assegnare chiavi di accesso in modo univoco.
    -   **Controlli senza etichetta, ad** esempio controlli di selezione, pulsanti di comando grafici e controlli di divulgazione progressiva senza etichetta.
    -   **Testo statico non etichettato o etichette per i controlli non interattivi,** ad esempio gli barre di stato.

-   **Assegnare prima le chiavi di accesso del pulsante di commit per assicurarsi che siano assegnate le assegnazioni di chiave standard.** Se non è presente un'assegnazione di chiave standard, usare la prima lettera della prima parola. Ad esempio, il tasto di scelta per i pulsanti Sì e No commit deve essere sempre "Y" e "N", indipendentemente dagli altri controlli nella finestra di dialogo.
-   **Per i pulsanti di commit negativi (diversi da Annulla) formulati come "Non fare", assegnare la chiave di accesso a "n" in "Non fare".** Se non viene formulata come "Non usare", usare l'assegnazione della chiave di accesso standard o assegnare la prima lettera della prima parola. In questo modo, tutti i valori Don'ts e No hanno una chiave di accesso coerente.
-   **Per semplificare** la ricerca dei tasti di scelta, assegnare i tasti di scelta a un carattere visualizzato all'inizio dell'etichetta, idealmente il primo carattere, anche se è presente una parola chiave che viene visualizzata più avanti nell'etichetta.
-   **Assegnare al massimo 20** chiavi di accesso, in modo da avere alcuni caratteri non assegnati per facilitare la localizzazione.
-   **Se sono presenti troppi controlli interattivi per assegnare chiavi di accesso univoche, è possibile assegnare chiavi di accesso non univoche** se:
    -   In caso contrario, sarebbe troppo difficile spostarsi tra i controlli.
    -   Le chiavi di accesso non univoche non sono in conflitto con le chiavi di accesso dei controlli di uso comune.
-   **Non usare le barre dei menu nelle finestre di dialogo.** In questo caso è difficile assegnare chiavi di accesso univoche, perché i controlli della finestra di dialogo e le voci di menu condividono gli stessi caratteri.

### <a name="shortcut-keys"></a>Combinazioni di tasti

-   **Assegnare i tasti di scelta rapida ai comandi usati più di frequente.** I programmi e le funzionalità usati raramente non necessitano di tasti di scelta rapida perché gli utenti possono usare i tasti di scelta.
-   **Non creare un tasto di scelta rapida come unico modo per eseguire un'attività.** Gli utenti devono anche essere in grado di usare il mouse o la tastiera con TAB, freccia e tasti di scelta.
-   **Non assegnare significati diversi a tasti di scelta rapida noti.** Poiché sono memorizzati, significati incoerenti per le scelte rapide note sono frustranti e erre.
-   **Non provare ad assegnare tasti di scelta rapida del programma a livello di sistema.** I tasti di scelta rapida del programma avranno effetto solo quando il programma ha lo stato attivo per l'input.
-   **Documentare tutti i tasti di scelta rapida.** Collegamenti ai documenti in voci della barra dei menu, descrizioni comando della barra degli strumenti e un singolo articolo della Guida che documenta tutti i tasti di scelta rapida usati. In questo modo gli utenti possono apprendere le assegnazioni dei tasti di scelta rapida che non devono essere segreti.

    -   **Eccezione:** Non visualizzare le assegnazioni dei tasti di scelta rapida all'interno dei menu di scelta rapida. I menu di scelta rapida non visualizzano le assegnazioni dei tasti di scelta rapida perché sono ottimizzati per l'efficienza.

    ![Screenshot della descrizione comando per il tasto di scelta rapida in grassetto ](images/inter-keyboard-image19.png)

    Il tasto di scelta rapida è documentato nella descrizione comando.

-   **Se il programma assegna molti tasti di scelta rapida, è possibile personalizzare le assegnazioni.** In questo modo gli utenti possono riassegnare i tasti di scelta rapida in conflitto ed eseguire la migrazione da altri prodotti. La maggior parte dei programmi non assegna tasti di scelta rapida sufficienti per questa funzionalità.

### <a name="choosing-shortcut-keys"></a>Scelta dei tasti di scelta rapida

-   **Per i tasti di scelta rapida noti, usare le assegnazioni standard.**
-   **Per le assegnazioni di tasti non standard, usare i tasti di scelta rapida consigliati seguenti per i comandi usati più di frequente.** Questi tasti di scelta rapida sono consigliati perché non sono in conflitto con i tasti di scelta rapida noti e sono facili da premere.
    -   CTRL+G, J, K, L M, Q, R o T
    -   CTRL+qualsiasi numero
    -   F7, F8, F9 o F12
    -   MAIUSC+F2, F3, F4, F5, F7, F8, F9, F11 o F12
    -   ALT+qualsiasi tasto funzione ad eccezione di F4
-   **Usare i tasti di scelta rapida consigliati seguenti per i comandi usati meno di frequente.** Questi tasti di scelta rapida non hanno conflitti, ma sono più difficili da premere spesso richiedendo due mani.
    -   CTRL+qualsiasi tasto funzione ad eccezione di F4 e F6
    -   CTRL+MAIUSC+qualsiasi lettera o numero
-   **È facile ricordare i tasti di scelta rapida usati di frequente:**
    -   Usare lettere anziché numeri o chiavi di funzione.
    -   Provare a usare una lettera che si trova nella prima parola o nel carattere più facile da ricordare all'interno delle parole chiave del comando.
-   **Usare i tasti funzione per i comandi che hanno un** effetto su scala ridotta, ad esempio i comandi che si applicano all'oggetto selezionato. Ad esempio, F2 rinomina l'elemento selezionato.
-   **Usare le combinazioni di tasti CTRL per i** comandi che hanno un effetto su larga scala, ad esempio i comandi che si applicano a un intero documento. Ad esempio, CTRL+S salva il documento corrente.
-   **Usare le combinazioni di tasti MAIUSC per i comandi che estendono o integrano le azioni del tasto di scelta rapida standard.** Ad esempio, il tasto di scelta rapida ALT+TAB scorre le finestre primarie aperte, mentre ALT+MAIUSC+TAB scorre in ordine inverso. Analogamente, F1 visualizza la Guida, mentre MAIUSC+F1 visualizza la Guida sensibile al contesto.
-   **Quando si usano i tasti di direzione per spostare o ridimensionare un elemento, usare CTRL+tasti di direzione per un controllo più granulare.**

### <a name="choosing-shortcut-keys-what-not-to-do"></a>Scelta dei tasti di scelta rapida (cosa non fare)

-   **Non distinguere tra le posizioni delle chiavi.** Ad esempio, Windows è in grado di distinguere tra MAIUSC a sinistra e a destra, ALT, CTRL, [logo windows](glossary.md)e tasti [applicazione,](glossary.md)nonché i tasti del tastierino numerico. L'assegnazione di un comportamento a una sola posizione chiave è confusa e imprevista.
-   **Non usare il tasto di modifica del logo Windows per i tasti di scelta rapida del programma.** Il tasto logo Windows è riservato per l'uso in Windows. Anche se una combinazione di tasti logo Windows non viene attualmente usata da Windows, potrebbe essere in futuro.
-   **Non usare il tasto applicazione come modificatore del tasto di scelta rapida.** Usare invece CTRL, ALT e MAIUSC.
-   **Non usare i tasti di scelta rapida usati da Windows per i tasti di scelta rapida del programma.** Questa operazione sarà in conflitto con i tasti di scelta rapida di sistema di Windows quando il programma ha lo stato attivo per l'input.
-   **Non usare combinazioni di tasti alt+alfanumerico per i tasti di scelta rapida.** Tali tasti di scelta rapida possono essere in conflitto con i tasti di scelta.
-   **Non usare i caratteri seguenti per i tasti di scelta rapida:** @ $ {} \[ \] \\  ~  \| ^ ' < >. Questi caratteri richiedono combinazioni di tasti diverse tra le lingue o sono specifici delle impostazioni locali.
-   **Evitare combinazioni** di tasti complesse, ad esempio tre o più tasti insieme (ad esempio CTRL+ALT+BARRA SPAZIATRICE) o tasti distanti dalla tastiera (ad esempio: CTRL+F5). Usare semplici tasti di scelta rapida per i comandi usati di frequente.
-   **Non usare combinazioni CTRL+ALT,** perché Windows interpreta questa combinazione in alcune versioni del linguaggio come tasto ALTGR, che genera caratteri alfanumerici.

### <a name="keyboard-and-mouse-combinations"></a>Combinazioni di tastiera e mouse

-   Per i collegamenti, usare MAIUSC+clic per spostarsi in una nuova finestra e CTRL+clic per spostarsi usando una nuova scheda. Questo approccio è coerente con Windows Internet Explorer .

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alla tastiera:

-   Usare la tastiera su schermo per fare riferimento a una rappresentazione della tastiera sullo schermo che l'utente tocca ai caratteri di input.
-   Assegnare le combinazioni di tasti a partire dal tasto di modifica. Presentare i tasti di modifica nell'ordine seguente: logo windows, applicazione, CTRL, ALT, MAIUSC. Se viene usato il modificatore Numpad, inseriscilo subito prima del tasto modificato.
-   Non usare tutte le lettere maiuscole per i tasti della tastiera. Seguire invece le maiuscole usate dalle tastiere standard o minuscole se il tasto non è etichettato sulla tastiera.
    -   Per le combinazioni di tasti alfabetiche, usare una lettera maiuscola.
    -   Impostare pggi su, pggi in giù, schermata di stampa e blocco di scorrimento.
    -   Eseguire l'ortografia con il segno più, il segno meno, il trattino, il punto e la virgola.
    -   Per i tasti di direzione, usare freccia SINISTRA, freccia DESTRA, freccia SU e freccia GIÙ. Non usare etichette grafiche per i tasti di direzione.
    -   Usare il tasto logo Windows e il tasto applicazione per fare riferimento alle chiavi etichettate con icone. Non usare etichette grafiche per queste chiavi.

**Corretto:**

barra spaziatrice, TAB, INVIO, P SU, CTRL+ALT+CANC, ALT+W, CTRL+segno più

**Non corretto:**

BARRA SPAZIATRICE, TAB, INVIO, PG SU, CTRL+ALT+CANC, ALT+W, CTRL++

-   Indicare le combinazioni di tasti con un segno più, senza spazi.

**Corretto:**

CTRL+A, MAIUSC+F5

**Non corretto:**

CTRL+A, MAIUSC+F5

-   Per visualizzare una combinazione di tasti che include la punteggiatura che richiede l'uso del tasto MAIUSC, ad esempio il punto interrogativo, aggiungere MAIUSC alla combinazione e assegnare il nome o il simbolo del tasto spostato. L'uso del nome della chiave non fuorviata, ad esempio 4 anziché $, potrebbe generare confusione per gli utenti o addirittura errato. ad esempio? i caratteri e /non sono sempre spostati su ogni tastiera.

**Corretto:**

CTRL+MAIUSC+?, CTRL+MAIUSC+, \* CTRL+MAIUSC+virgola

**Non corretto:**

CTRL+MAIUSC+/, CTRL+?, CTRL+MAIUSC+8, CTRL+\*

-   Prima di tutto, usare la chiave e con il nome della chiave, se necessario per maggiore chiarezza, ad esempio il tasto F1. In tutti i riferimenti successivi, fare riferimento alla chiave solo in base al nome, ad esempio premere F1.
-   Fare riferimento in particolare ai tasti di scelta e ai tasti di scelta rapida nella programmazione e in altri documenti tecnici. Non usare tasti di scelta rapida, tasti di scelta rapida o tasti di scelta rapida. Ovunque si usino tasti di scelta rapida, in particolare nella documentazione dell'utente.

Quando si fa riferimento all'interazione:

-   Quando si preme e si rilascia immediatamente un tasto, viene avviata un'azione all'interno del programma o ci si sposta all'interno di un documento o di un'interfaccia utente.
-   Usare il tipo, non immettere, per indirizzare gli utenti alla digitazione di testo.
-   Usare in situazioni in cui la pressione potrebbe generare confusione, ad esempio quando si fa riferimento a un tipo di tasto, ad esempio i tasti di direzione o i tasti funzione. In questi casi, premere potrebbe far pensare agli utenti di dover premere tutti i tasti contemporaneamente.
-   Tenere premuto quando si tiene premuto un tasto, ad esempio un tasto di modifica.
-   Non usare press come sinonimo del clic.

Esempi:

-   Digitare il nome e quindi premere INVIO.
-   Premere CTRL+F e quindi digitare il testo da cercare.
-   Per salvare il file, premere Y.
-   Per spostare il punto di inserimento, usare i tasti di direzione.

 

