---
title: Barre di stato
description: Con un indicatore di stato, gli utenti possono seguire lo stato di avanzamento di un'operazione di lunga durata. Un indicatore di stato può mostrare una percentuale approssimativa di completamento (determinato) o indicare che un'operazione è in corso (indeterminata).
ms.assetid: 067961fa-2fb1-4cd1-99a4-cbe2244c3913
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b62240da0df0b284e8a5f7175131eaa9db18fc1743f9f8701019cc2efb390464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117853835"
---
# <a name="progress-bars"></a>Barre di stato

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con un indicatore di stato, gli utenti possono seguire lo stato di avanzamento di un'operazione di lunga durata. Un indicatore di stato può mostrare una percentuale approssimativa di completamento (determinato) o indicare che un'operazione è in corso (indeterminata).

Gli studi sull'usabilità hanno dimostrato che gli utenti sono a conoscenza dei tempi di risposta di oltre un secondo. Di conseguenza, è consigliabile considerare che le operazioni il cui completamento richiede almeno due secondi siano lunghe e che necessitano di un tipo di feedback sullo stato di avanzamento.

![Screenshot di un indicatore di stato tipico ](images/progress-bars-image1.png)

Un indicatore di stato tipico.

> [!Note]  
> Le linee guida [relative al layout](vis-layout.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **L'operazione verrà completata in circa cinque secondi o meno?** In tal caso, usare invece [un indicatore di](inter-mouse.md) attività, perché la visualizzazione di un indicatore di stato per una durata così breve potrebbe distrarre. Se l'operazione richiede in genere cinque secondi o meno, ma a volte ne richiede di più, iniziare con un puntatore occupato e convertirlo in un indicatore di stato dopo cinque secondi.
-   **Un indicatore di stato indeterminato viene usato per attendere il completamento di un'attività da parte dell'utente?** In tal caso, non usare un indicatore di stato. Gli barre di stato sono per lo stato del computer, non per l'utente.
-   **Un indicatore di stato indeterminato è combinato con un'animazione?** In caso contrario, usare solo l'animazione. L'indicatore di stato indeterminato è in effetti un'animazione generica e non aggiunge alcun valore all'animazione.
-   **L'operazione è un'attività in background molto lunga (più di due minuti) per cui gli utenti sono più interessati al completamento che allo stato di avanzamento?** In caso contrario, usare [una notifica.](mess-notif.md) In questo caso, gli utenti ese avanti nel frattempo e non monitorano lo stato di avanzamento. L'uso di una notifica consente agli utenti di eseguire altre attività senza interruzioni. Esempi di operazioni di questo tipo includono stampa, backup, analisi di sistema e trasferimenti o conversioni di dati in blocco.
-   **Al termine dell'operazione, gli utenti saranno in grado di riprodurre i risultati?** In tal caso, usare invece un dispositivo di scorrimento. Esempi di tali operazioni includono la registrazione e la riproduzione di video e audio.

    ![Screenshot del lettore multimediale e del dispositivo di scorrimento ](images/progress-bars-image2.png)

    In questo esempio viene usato un dispositivo di scorrimento per indicare lo stato di avanzamento durante la riproduzione del suono. In questo modo gli utenti possono riprodurre i risultati in un secondo momento.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Durante un'operazione di lunga durata, gli utenti necessitano di un'idea generale dell'operazione. Devono anche conoscere:

-   L'avvio di un'operazione di lunga durata.
-   Lo stato di avanzamento è in corso e l'operazione verrà completata (e pertanto non è stata bloccata).
-   Percentuale approssimativa dell'operazione completata (e pertanto la percentuale rimanente).
-   Se devono annullare l'operazione se non vale la pena continuare ad attendere.
-   Se devono continuare ad attendere o eseguire altre operazioni mentre l'operazione viene completata.

**Usare gli indicatore di stato determinati** per le operazioni che richiedono una quantità di tempo delimitata, anche se tale quantità di tempo non può essere stimata in modo accurato. Gli barre di stato indeterminati indicano lo stato di avanzamento in corso, ma non forniscono altre informazioni. Non scegliere un indicatore di stato indeterminato basato solo sulla possibile mancanza di accuratezza.

Si supponga, ad esempio, che un'operazione richieda cinque passaggi e che ognuno di questi passaggi richieda una quantità di tempo delimitata, ma la quantità di tempo per ogni passaggio può variare notevolmente. In questo caso, usare un indicatore di stato determinato e mostrare lo stato di avanzamento quando ogni passaggio viene completato proporzionalmente alla quantità di tempo generalmente necessario per ogni passaggio. Usare un indicatore di stato indeterminato solo se un indicatore di stato determinato fa sì che gli utenti concludono in modo errato che l'operazione è stata bloccata.

**Se si fa una sola cosa...**

Assicurarsi di fornire feedback sullo stato di avanzamento per le operazioni di lunga durata e che le informazioni sopra riportate siano chiaramente comunicate. Usare gli barre di stato determinati quando possibile.

## <a name="usage-patterns"></a>Modelli di utilizzo

Gli barre di stato hanno diversi modelli di utilizzo:

### <a name="determinate-progress-bars"></a>Indicatore di stato determinati



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Barre di stato determinate modali</strong><br/> Indicare lo stato di avanzamento di un'operazione compilando da sinistra a destra e completando l'operazione al termine dell'operazione. <br/></td>
<td>Poiché questo <a href="glossary.md"></a>feedback è modale, gli utenti non possono eseguire altre attività nella finestra (o l'elemento padre se visualizzato in una finestra di dialogo modale) fino al completamento dell'operazione. <br/> <img src="images/progress-bars-image3.png" alt="Screen shot of progress bar in modal window " /><br/> In questo esempio l'indicatore di stato fornisce feedback durante la configurazione. <br/></td>
</tr>
<tr class="even">
<td><strong>Barre di stato determinate modali con un pulsante Annulla o Arresta</strong><br/> Consentire agli utenti di interrompere l'operazione, ad esempio perché l'operazione sta prendendo troppo tempo o non vale la pena attendere.<br/></td>
<td><img src="images/progress-bars-image4.png" alt="Screen shot of progress bar with Stop button " /><br/> In questo esempio gli utenti possono fare clic su Arresta per arrestare l'operazione e lasciare l'ambiente nello stato corrente.<br/></td>
</tr>
<tr class="odd">
<td><strong>Barre di stato determinate modali con un pulsante Annulla o Arresta e un'animazione</strong><br/> Consentire agli utenti di interrompere l'operazione e includere un'animazione per consentire agli utenti di visualizzare l'effetto di un'operazione.<br/></td>
<td><img src="images/progress-bars-image5.png" alt="Screen shot of progress bar with animation " /><br/> In questo esempio gli utenti possono fare clic su Arresta per arrestare l'operazione e lasciare l'ambiente nello stato corrente.<br/></td>
</tr>
<tr class="even">
<td><strong>Barre di stato doppie determinate modali</strong><br/> Indicare lo stato di avanzamento di un'operazione in più passaggi visualizzando lo stato del passaggio corrente nel primo indicatore di stato e l'avanzamento complessivo nella seconda barra.<br/></td>
<td>Poiché il primo indicatore di stato fornisce poche informazioni aggiuntive e può essere piuttosto distratto, questo modello non è consigliato. Al contrario, fare in modo che tutti i passaggi dell'operazione condino una parte dello stato di avanzamento e che un singolo indicatore di stato passi al completamento una sola volta. <br/> <img src="images/progress-bars-image6.png" alt="Screen shot of current and overall progress bars " /><br/> In questo esempio, il primo indicatore di stato mostra lo stato di avanzamento del passaggio corrente e il secondo indicatore di stato mostra lo stato di avanzamento complessivo.<br/>
<blockquote>
[!Note]<br />
Questo modello non è in genere necessario e deve essere evitato.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Barre di stato determinate non modabili</strong><br/> Indicare lo stato di avanzamento di un'operazione compilando da sinistra a destra e completando l'operazione al termine dell'operazione.<br/></td>
<td>A differenza degli barre di stato modali, gli utenti possono eseguire altre attività mentre l'operazione è in corso. Questi barre di stato possono essere visualizzati nel contesto o in una barra di stato. <br/> <img src="images/progress-bars-image7.png" alt="Screen shot of progress bar on status bar " /><br/> In questo esempio, Windows Internet ExplorerWindows Internet Explorer visualizza lo stato di avanzamento per il caricamento di una pagina Web sulla barra di stato. Gli utenti possono eseguire altre attività durante il caricamento della pagina.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="indeterminate-progress-bars"></a>Barre di stato indeterminate



|   Tipo di indicatore di stato  | Descrizione             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Indicatore di stato indeterminato modale**<br/> indicano che un'operazione è in corso visualizzando un'animazione che scorre continuamente sulla barra da sinistra a destra. <br/>   | Usato solo per le operazioni il cui stato di avanzamento complessivo non può essere determinato, quindi non esiste alcuna nozione di completezza. È preferibile definire gli barre di stato perché indicano la percentuale approssimativa dell'operazione completata e consentono agli utenti di determinare se l'operazione vale la pena continuare ad attendere. sono anche meno distratti visivamente. <br/> ![Screenshot dell'indicatore di stato modale e indeterminato](images/progress-bars-image8.png)<br/> In questo esempio, Windows Update usa un indicatore di stato indeterminato modale per indicare lo stato di avanzamento durante la ricerca degli aggiornamenti.<br/> |
| **Barre di stato indeterminate non modabili**<br/> indicano che un'operazione è in corso visualizzando un'animazione che scorre continuamente sulla barra da sinistra a destra.<br/> | A differenza degli barre di stato modali, gli utenti possono eseguire altre attività mentre è in corso l'elaborazione. Questi barre di stato possono essere visualizzati nel contesto o in una barra di stato. <br/> ![Screenshot dell'indicatore di stato sottile nella finestra di Outlook ](images/progress-bars-image9.png)<br/> In questo esempio, Microsoft Outlook usa un indicatore di stato non modabile indeterminato durante la compilazione delle proprietà del contatto. Gli utenti possono continuare a usare la finestra delle proprietà mentre questa operazione è in corso.<br/>                                                                                                                    |



 

### <a name="meters"></a>Metri



|   Tipo                                                                                       |   Descrizione                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Metri**<br/> indicano una percentuale non correlata allo stato di avanzamento. <br/> | Questo modello non è un indicatore di stato, ma viene implementato usando il controllo indicatore di stato. I contatori hanno un aspetto distinto per distinguerli dagli indicatori di stato veri. <br/> ![Screenshot del contatore che mostra lo spazio libero su disco ](images/progress-bars-image10.png)<br/> In questo esempio il contatore mostra la percentuale di spazio su disco usato.<br/> |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Fornire feedback sullo stato di avanzamento quando si esegue un'operazione di lunga durata.** Gli utenti non devono mai indovinare se lo stato di avanzamento è in corso.
-   **Indicare chiaramente lo stato di avanzamento reale.** L'indicatore di stato deve avanzare se viene effettuato lo stato di avanzamento. Se l'intervallo di tempo di completamento previsto è elevato, è consigliabile usare una scala non lineare per indicare lo stato di avanzamento per i tempi più lunghi. Non si vuole che gli utenti concludono che il programma si è bloccato quando non lo è stato.
-   **Indicare chiaramente la mancanza di stato.** L'indicatore di stato non deve avanzare se non viene effettuato alcun avanzamento. Non si vuole che gli utenti attendano per un periodo illimitato un'operazione che non verrà mai completata.
-   **Fornire dettagli utili sullo stato di avanzamento.** Fornire informazioni aggiuntive sullo stato di avanzamento, ma solo se gli utenti possono eseguire un'operazione. Assicurarsi che il testo sia visualizzato per un periodo di tempo sufficiente per consentire agli utenti di leggerlo.

    ![Screenshot dell'indicatore di stato che mostra la velocità di trasferimento ](images/progress-bars-image11.png)

    In questo esempio, gli utenti possono visualizzare la velocità di trasferimento. La bassa velocità di trasferimento qui suggerisce la necessità di usare una connessione di rete a larghezza di banda elevata.

-   **Non specificare dettagli non necessari.** In genere gli utenti non si preoccupano dei dettagli dell'operazione in esecuzione. Ad esempio, gli utenti di un programma di installazione non si preoccupano del file specifico copiato o che i componenti di sistema vengono registrati perché non hanno aspettative su questi dettagli. In genere, un indicatore di stato ben etichettato da solo fornisce informazioni sufficienti, quindi fornire informazioni aggiuntive sullo stato solo se gli utenti possono eseguire un'operazione con esso. Fornire informazioni dettagliate che gli utenti non sono importanti rende l'esperienza utente e troppo complessa e tecnica. Se sono necessarie informazioni più dettagliate per il debug, non visualizzarle nelle build di rilascio.

    **Corretto:**

    ![Screenshot dello stato di avanzamento dell'installazione ](images/progress-bars-image12.png)

    In questo esempio, l'indicatore di stato con etichetta è tutto ciò che serve.

    **Corretto:**

    ![Screenshot dell'indicatore di stato che mostra la velocità di trasferimento ](images/progress-bars-image11.png)

    In questo esempio, Windows Explorer copia i file selezionati dall'utente, quindi la visualizzazione dei nomi file copiati è significativa.

    **Non corretto:**

    ![Screenshot dello stato di avanzamento della registrazione ](images/progress-bars-image13.png)

    In questo esempio, un programma di installazione fornisce dettagli che non sono importanti per l'utente.

-   **Fornire animazioni utili.** Se eseguite in modo ottimale, le animazioni migliorano l'esperienza utente consentendo agli utenti di visualizzare l'operazione. Le animazioni di qualità hanno un impatto maggiore rispetto al solo testo. Ad esempio, l'indicatore di stato per il comando Outlook Elimina visualizza il Cestino per la destinazione se i file possono essere ripristinati, ma non Cestino se i file non possono essere ripristinati.

    ![Screenshot dello stato di avanzamento dell'eliminazione ](images/progress-bars-image14.png)

    In questo esempio, la mancanza di un Cestino conferma che i file vengono eliminati definitivamente. Queste informazioni aggiuntive non verranno comunicate in modo efficace usando solo il testo.

-   **Non usare animazioni non necessarie.** Le animazioni possono essere fuorvianti perché in genere vengono eseguite in un thread separato dall'attività effettiva e pertanto possono suggerire lo stato di avanzamento anche se l'operazione è bloccata. Inoltre, se l'operazione è più lenta del previsto, gli utenti talvolta presuppongono che l'animazione sia parte del motivo. Di conseguenza, usare le animazioni solo quando esiste una giustificazione chiara; non usarli per provare a distogliere gli utenti.
-   **Posizionare le animazioni centrate sull'indicatore di stato.** Posizionare l'animazione sopra le etichette dell'indicatore di stato, se presenti. Se è presente un pulsante Annulla o Arresta a destra dell'indicatore di stato, includere il pulsante quando si determina il centro.
-   **Riprodurre un effetto sonoro al completamento di un'operazione solo se è molto lunga (più di due minuti), poco comune e importante.** Se l'utente probabilmente si allontana da un'operazione importante durante l'elaborazione, un effetto sonoro ripristina l'attenzione dell'utente. L'uso di un effetto sonoro al completamento in altre circostanze potrebbe distrarre l'attenzione.
-   **Non sottrarre lo stato attivo per l'input per mostrare un aggiornamento o un completamento dello stato di avanzamento.** Gli utenti spesso passano ad altri programmi in attesa e non vogliono essere interrotti. Le attività in background devono rimanere in background.
-   **Non è necessario preoccuparsi del supporto tecnico.** Poiché il feedback fornito dagli barre di stato non è necessariamente accurato ed è fuorciante, gli indicatore di stato non sono un buon meccanismo per fornire informazioni per il supporto tecnico. Di conseguenza, se l'operazione può non riuscire (come con un programma di installazione), non fornire informazioni aggiuntive sullo stato di avanzamento utili solo al supporto tecnico. Fornire invece un meccanismo alternativo, ad esempio un file di log, per registrare le informazioni di supporto tecnico.

    **Non corretto:**

    ![Screenshot dell'indicatore di stato che mostra il nome del server ](images/progress-bars-image15.png)

    In questo esempio l'indicatore di stato mostra i dettagli destinati al supporto tecnico.

-   **Non inserire la percentuale di completamento o qualsiasi altro testo in un indicatore di stato.** Questo testo non è accessibile e non è compatibile con l'uso dei temi.

    **Non corretto:**

    ![Screenshot dell'indicatore di stato con testo sulla barra ](images/progress-bars-image16.png)

    In questo esempio il testo percentuale sull'indicatore di stato non è accessibile.

-   **Non combinare un indicatore di stato con un puntatore occupato.** Usare uno o l'altro, ma non entrambi contemporaneamente.
-   **Non usare gli indicatore di stato verticali.** Gli barre di stato orizzontali hanno un mapping più naturale e un flusso migliore.

### <a name="determinate-progress-bars"></a>Indicatore di stato determinati

-   **Usare gli indicatore di stato determinati** per le operazioni che richiedono una quantità di tempo delimitata, anche se tale quantità di tempo non può essere stimata in modo accurato. Gli barre di stato indeterminati indicano lo stato di avanzamento in corso, ma non forniscono altre informazioni. Non scegliere un indicatore di stato indeterminato basato solo sulla possibile mancanza di accuratezza.
-   **Indicare chiaramente la fase di avanzamento.** L'indicatore di stato deve essere in grado di indicare se l'operazione si trova all'inizio, al centro o alla fine di un'operazione. Ad esempio, gli barre di stato che si affondono immediatamente fino al 99% del completamento, quindi rimangono in tale stato per molto tempo, sono particolarmente poco formattati e fastidiosi. In questi casi, l'indicatore di stato deve essere inizialmente impostato su un massimo del 33% per indicare che l'operazione è ancora nella fase iniziale.
-   **Indicare chiaramente il completamento.** Non lasciare che un indicatore di stato passi al 100% a meno che l'operazione non sia stata completata.
-   **Fornire una stima del tempo rimanente se è possibile farlo in modo accurato.** Le stime del tempo rimanente che sono accurate sono utili, ma non sono utili le stime che sono fuori dal segno o che si aggirano in modo significativo. Potrebbe essere necessario eseguire alcune operazioni di elaborazione prima di poter fornire stime accurate. In questo caso, non visualizzare stime potenzialmente imprecise durante questo periodo iniziale.
-   **Non riavviare lo stato di avanzamento.** Un indicatore di stato perde il valore se viene riavviato (ad esempio perché viene completato un passaggio dell'operazione) perché gli utenti non hanno modo di sapere quando l'operazione verrà completata. Al contrario, fare in modo che tutti i passaggi dell'operazione contitino una parte dello stato di avanzamento e che l'indicatore di stato passi al completamento una sola volta.

    **Non corretto:**

    ![Screenshot dell'indicatore di stato riavviato ](images/progress-bars-image17.png)

    In questo esempio l'operazione è passata al passaggio di copia dei file e reimposta l'indicatore di stato per tale passaggio. A questo punto gli utenti non hanno idea dello stato di avanzamento o del tempo che rimane.

-   **Non eseguire il backup dello stato di avanzamento.** Come con un riavvio, un indicatore di stato perde il valore se ne viene backup. Aumentare sempre lo stato di avanzamento in modo monotono. Tuttavia, è possibile avere una stima del tempo rimanente che aumenta (nonché diminuisce) perché la velocità di avanzamento può variare.

### <a name="indeterminate-progress-bars"></a>Barre di stato indeterminate

-   **Usare gli barre di stato indeterminati solo per le operazioni di cui non è possibile determinare lo stato di avanzamento complessivo.** Usare gli indicatore di stato indeterminati per le operazioni che richiedono un periodo di tempo illimitato o che accedono a un numero sconosciuto di oggetti. Usare i timeout per assegnare limiti alle operazioni basate sul tempo.
-   **Eseguire la conversione in un indicatore di stato determinato dopo aver determinato lo stato di avanzamento complessivo.** Ad esempio, se sono necessari più di due secondi per determinare il numero di oggetti, è possibile usare un indicatore di stato indeterminato mentre gli oggetti vengono conteggiati e quindi convertirli in un indicatore di stato determinato.
-   **Non combinare gli indicatore di stato indeterminati con le stime della percentuale di completamento o del tempo rimanente.** Se è possibile fornire queste informazioni, usare invece un indicatore di stato determinato.
-   **Non combinare barre di stato indeterminate con animazioni.** Un indicatore di stato indeterminato è in effetti un'animazione generica, pertanto è consigliabile usare una o l'altra, ma mai entrambe.

    **Corretto:**

    ![Screenshot dello stato di avanzamento nel rilevamento del server ](images/progress-bars-image18.png)

    In questo esempio viene usata solo un'animazione per mostrare che un'operazione è in corso.

### <a name="modeless-progress-bars"></a>Barre di stato non modabili

-   **Se gli utenti possono eseguire operazioni produttive mentre l'operazione è in corso, fornire commenti e suggerimenti non modabili.** Potrebbe essere necessario disabilitare un subset di funzionalità che richiede il completamento dell'operazione.
-   **Se la finestra ha una barra degli indirizzi, visualizzare lo stato di avanzamento non modato nella barra degli indirizzi.**

    ![Screenshot dell'indicatore di stato come parte della barra degli indirizzi ](images/progress-bars-image19.png)

    In questo esempio lo stato di avanzamento non modato viene visualizzato nella barra degli indirizzi.

-   In caso **contrario, se la finestra ha una barra di stato, visualizzare lo stato di avanzamento non modato nella barra di stato.** Posizionare il testo corrispondente a sinistra nella barra di stato.

    ![screenshot dell'indicatore di stato come parte della barra di stato ](images/progress-bars-image7.png)

    In questo esempio lo stato di avanzamento non modato viene visualizzato nella barra di stato.

### <a name="modal-progress-bars"></a>Barre di stato modali

-   **Posizionare gli barre di stato modali nelle pagine di stato o nelle finestre** di dialogo di [stato](win-dialog-box.md).
-   **Fornire un pulsante di comando per arrestare l'operazione se il completamento richiede più di pochi secondi o se può non essere mai completato.** Etichettare il pulsante Annulla se l'annullamento riporta l'ambiente allo stato precedente (senza effetti collaterali). In caso contrario, etichettare il pulsante Arresta per indicare che lascia intatta l'operazione parzialmente completata. È possibile modificare l'etichetta del pulsante da Annulla a Arresta al centro dell'operazione se a un certo punto non è possibile ripristinare lo stato precedente dell'ambiente. Centrare il pulsante di comando verticalmente con l'indicatore di stato invece di allinearne la parte superiore.

    **Corretto:**

    ![Screenshot dello stato di attesa della rete ](images/progress-bars-image20.png)

    In questo esempio l'interruzione della connessione di rete non ha alcun effetto collaterale, quindi viene usato Annulla.

    **Corretto:**

    ![Screenshot dell'indicatore di stato che mostra il tempo di copia a sinistra ](images/progress-bars-image21.png)

    In questo esempio, l'interruzione della copia lascia tutti i file copiati, quindi il pulsante di comando è contrassegnato con l'etichetta Arresta.

    **Non corretto:**

    ![Screenshot dell'indicatore di stato della ricerca e del pulsante arresta ](images/progress-bars-image22.png)

    In questo esempio l'interruzione della ricerca non ha alcun effetto collaterale, quindi il pulsante di comando deve essere contrassegnato con l'etichetta Annulla.

### <a name="time-remaining"></a>Tempo rimanente

Per gli barre di stato determinati:

-   **Usare i formati di ora seguenti.** Iniziare con il primo dei formati seguenti in cui l'unità di tempo più grande non è zero e quindi passare al formato successivo quando l'unità di tempo più grande diventa zero.

    **Per gli barre di stato:**

    **Se le informazioni correlate vengono visualizzate in formato due punti:**

    Tempo rimanente: ore h, m minuti

    Tempo rimanente: m minuti, s secondi

    Tempo rimanente: s secondi

    **Se lo spazio sullo schermo è premium:**

    h hrs, m min rimanenti

    m mins, s secs remaining

    s secondi rimanenti

    **In caso contrario:**

    ore h, m minuti rimanenti

    m minuti, s secondi rimanenti

    s secondi rimanenti

    **Per le barre del titolo:**

    hh:mm rimanente

    mm:ss remaining

    0:ss rimanenti

    Questo formato compatto mostra prima le informazioni più importanti in modo che non sia troncato sulla barra delle applicazioni.

-   **Fare in modo che le stime siano accurate, ma non fornire false precisione.** Se l'unità più grande è di ore, assegnare minuti (se significativi) ma non secondi.

    **Non corretto:**

    hh hours, mm minutes, ss seconds

-   **Mantenere aggiornata la stima.** Aggiornare le stime del tempo rimanente almeno ogni 5 secondi.
-   **Concentrarsi sul tempo rimanente** perché si tratta delle informazioni più importanti per gli utenti. Assegnare il tempo trascorso totale solo in alcuni scenari in cui il tempo trascorso è utile, ad esempio quando è probabile che l'attività sia ripetuta. Se la stima del tempo rimanente è associata a un indicatore di stato, non avere il testo completo della percentuale perché queste informazioni vengono trasmesse dall'indicatore di stato stesso.
-   **Essere grammaticalmente corretti.** Usare unità singolari quando il numero è uno.

    **Non corretto:**

    1 minuto, 1 secondo

-   **Usare le maiuscole/minuscole come nelle frasi comuni.**

### <a name="progress-bar-colors"></a>Colori dell'indicatore di stato

-   **Usare barre di stato rosse o gialle solo per indicare lo stato di avanzamento, non i risultati finali di un'attività.** Un indicatore di stato rosso o giallo indica che gli utenti devono eseguire un'azione per completare l'attività. Se la condizione non è recuperabile, lasciare verde l'indicatore di stato e visualizzare un messaggio di errore.
-   **Attivare l'indicatore di stato rosso quando è presente una condizione ripristinabile dall'utente che impedisce l'avanzamento.** Visualizzare un messaggio per spiegare il problema e consigliare una soluzione.
-   **Impostare** l'indicatore di stato in giallo per indicare che l'utente ha sospeso l'attività o che è presente una condizione che impedisce lo stato di avanzamento, ma lo stato di avanzamento è ancora in corso, ad esempio con una connettività di rete scadente. Se l'utente è stato sospeso, modificare l'etichetta del pulsante Sospendi in Riprendi. Se lo stato di avanzamento è ostacolato, visualizzare un messaggio per spiegare il problema e consigliare una soluzione.

### <a name="meters"></a>Metri

-   **Usare gli barre di stato solo per lo stato di avanzamento.** Usare i contatori per indicare le percentuali non correlate allo stato di avanzamento.

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

![Diagramma che mostra il ridimensionamento e la spaziatura dell'indicatore di stato ](images/progress-bars-image23.png)

Dimensioni e spaziatura consigliate per gli barre di stato.

-   Usare sempre l'altezza consigliata dell'indicatore di stato.
    -   **Eccezione:** È possibile usare un'altezza diversa se la finestra padre non supporta l'altezza consigliata.
-   Usare la larghezza minima se si vuole rendere non intrusivo l'indicatore di stato.
-   Non usare larghezze superiori al valore massimo consigliato. L'indicatore di stato non deve riempire lo spazio disponibile.
-   Centrare l'indicatore di stato orizzontalmente se la finestra è molto più ampia della larghezza massima consigliata.

## <a name="labels"></a>Etichette

### <a name="progress-bar-labels"></a>Etichette dell'indicatore di stato

-   **Usare un'etichetta concisa con un controllo di testo statico per indicare l'operazione eseguita.** Iniziare l'etichetta con un verbo (ad esempio, Copia) e terminare con i puntini di sospensione. Questa etichetta può cambiare in modo dinamico se l'operazione ha più passaggi o sta elaborando più oggetti.
-   Non assegnare una chiave [di accesso univoca](glossary.md) perché il controllo non è interattivo.
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Se l'operazione non è stata avviata direttamente dall'utente, è possibile includere un'etichetta aggiuntiva per fornire il contesto e chiedere di essere interrotta. Avviare questa etichetta aggiuntiva con la frase Please wait while (Attendere). Questa etichetta non deve cambiare durante l'operazione.

    ![Screenshot dell'indicatore di stato con etichetta ](images/progress-bars-image24.png)

    In questo esempio viene richiesto all'utente di attendere perché l'utente non ha avviato direttamente l'operazione.

-   Posizionare l'etichetta sopra l'indicatore di stato e allineare l'etichetta al bordo sinistro dell'indicatore di stato.

### <a name="progress-bar-details"></a>Dettagli dell'indicatore di stato

-   Specificare i dettagli nel testo statico, precedendo i dati con un'etichetta che termina con i due punti. Specificare le unità (secondi, kilobyte e così via) dopo il testo dei dettagli.

    **Corretto:**

    ![Screenshot dell'indicatore di stato che mostra la velocità di trasferimento ](images/progress-bars-image11.png)

    In questo esempio, i dettagli sono etichettati correttamente.

    **Non corretto:**

    ![Screenshot dell'indicatore di stato senza etichetta appropriata ](images/progress-bars-image25.png)

    In questo esempio, i dettagli non sono etichettati e quindi richiedono agli utenti di determinarne il significato.

-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Posizionare i dettagli sotto l'indicatore di stato e allineare l'etichetta al bordo sinistro dell'indicatore di stato.
-   Non assegnare la percentuale di completamento o di rimanente perché queste informazioni vengono comunicate dall'indicatore di stato stesso.

### <a name="cancel-button"></a>Scegliere il pulsante Annulla.

-   Etichettare il pulsante Annulla se l'annullamento riporta l'ambiente allo stato precedente (senza effetto collaterale); In caso contrario, etichettare il pulsante Arresta per indicare che l'operazione parzialmente completata rimane invariata.
-   È possibile modificare l'etichetta del pulsante da Annulla a Arresta nel mezzo dell'operazione se a un certo punto non è possibile ripristinare lo stato precedente dell'ambiente.

### <a name="progress-dialog-box-titles"></a>Titoli della finestra di dialogo Stato

-   Se l'indicatore di stato viene visualizzato in una finestra di dialogo modale, il titolo della finestra di dialogo deve essere il nome del programma o il nome dell'operazione. Non usare l'etichetta dell'indicatore di stato per il titolo della finestra di dialogo.

    **Corretto:**

    ![Screenshot del titolo dell'indicatore di stato con il nome dell'attività ](images/progress-bars-image26.png)

    In questo esempio il nome dell'attività viene usato per il titolo della finestra di dialogo.

    **Non corretto:**

    ![Screenshot del titolo della finestra di dialogo ridondante ](images/progress-bars-image27.png)

    In questo esempio, il testo del titolo della finestra di dialogo è una riezione dell'etichetta dell'indicatore di stato. In alternativa, è necessario usare il nome del programma.

-   Se l'indicatore di stato viene visualizzato in una finestra di dialogo non modali, ottimizzare il titolo per la visualizzazione sulla barra delle applicazioni posizionando concisamente le informazioni distintive per prime. Esempio: "66% completato".

 

