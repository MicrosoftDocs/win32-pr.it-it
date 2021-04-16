---
title: Indicatori di stato
description: Con un indicatore di stato, gli utenti possono seguire lo stato di avanzamento di un'operazione di lunga durata. Un indicatore di stato può mostrare una percentuale approssimativa di completamento (determinata) o indicare che un'operazione è in corso (indeterminata).
ms.assetid: 067961fa-2fb1-4cd1-99a4-cbe2244c3913
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: db8aca7300b309fb6929106cf97329956b7accb0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104565331"
---
# <a name="progress-bars"></a>Indicatori di stato

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con un indicatore di stato, gli utenti possono seguire lo stato di avanzamento di un'operazione di lunga durata. Un indicatore di stato può mostrare una percentuale approssimativa di completamento (determinata) o indicare che un'operazione è in corso (indeterminata).

Gli studi di usabilità hanno dimostrato che gli utenti sono consapevoli dei tempi di risposta di oltre un secondo. Di conseguenza, è necessario prendere in considerazione le operazioni che richiedono due secondi o più per completare la lunghezza e la necessità di un tipo di feedback sullo stato di avanzamento.

![Screenshot di un indicatore di stato tipico ](images/progress-bars-image1.png)

Indicatore di stato tipico.

> [!Note]  
> Le linee guida correlate al [layout](vis-layout.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **L'operazione viene completata in circa cinque secondi o meno?** In caso affermativo, usare invece un [indicatore di attività](inter-mouse.md) , perché la visualizzazione di una barra di stato per una durata di questo tipo potrebbe essere distrazione. Se l'operazione richiede in genere almeno cinque secondi, ma a volte richiede più, iniziare con un puntatore occupato e convertirlo in un indicatore di stato dopo cinque secondi.
-   **Indicatore di stato indeterminato utilizzato per attendere il completamento di un'attività da parte dell'utente.** In caso affermativo, non usare un indicatore di stato. Gli indicatori di stato sono per lo stato di avanzamento del computer, non lo stato utente.
-   **Un indicatore di stato indeterminato è associato a un'animazione?** In caso affermativo, usare invece solo l'animazione. L'indicatore di stato indeterminato è effettivamente un'animazione generica e non aggiunge alcun valore all'animazione.
-   **L'operazione è molto lunga (più di due minuti) in background per cui gli utenti sono più interessati al completamento dello stato di avanzamento?** In caso affermativo, usare invece una [notifica](mess-notif.md) . In questo caso, gli utenti eseguono altre attività nel frattempo e non eseguono il monitoraggio dello stato di avanzamento. L'uso di una notifica consente agli utenti di eseguire altre attività senza alcuna distorsione. Esempi di operazioni di questo tipo sono: stampa, backup, analisi del sistema e trasferimenti di dati in blocco o conversioni.
-   **Al termine dell'operazione, gli utenti saranno in grado di riprodurre i risultati?** In caso affermativo, usare invece un dispositivo di scorrimento. Esempi di tali operazioni includono la registrazione e la riproduzione audio e video.

    ![screenshot del lettore multimediale e del dispositivo di scorrimento ](images/progress-bars-image2.png)

    In questo esempio viene usato un dispositivo di scorrimento per indicare lo stato di avanzamento durante la riproduzione del suono. Questa operazione consente agli utenti di riprodurre i risultati in un secondo momento.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Durante un'operazione di lunga durata, gli utenti devono avere un'idea generale dell'operazione eseguita. Devono inoltre essere in grado di tenere presente quanto segue:

-   È stata avviata un'operazione di lunga durata.
-   Lo stato di avanzamento viene effettuato e l'operazione verrà completata (e pertanto non è bloccata).
-   Percentuale approssimativa dell'operazione completata (e pertanto la percentuale rimanente).
-   Se l'operazione deve essere annullata se non vale la pena continuare ad attendere.
-   Se devono continuare ad attendere o eseguire altre operazioni durante il completamento dell'operazione.

**Utilizzare gli indicatori di stato determinati per le operazioni che richiedono un periodo di tempo limitato,** anche se non è possibile prevedere accuratamente tale periodo di tempo. Gli indicatori di stato indeterminati mostrano che lo stato di avanzamento viene effettuato, ma non forniscono altre informazioni. Non scegliere un indicatore di stato indeterminato in base solo alla possibile mancanza di precisione.

Si supponga, ad esempio, che un'operazione richieda cinque passaggi e che ognuno di questi passaggi richieda un periodo di tempo limitato, ma la quantità di tempo per ogni passaggio può variare significativamente. In questo caso, usare un indicatore di stato determinato e mostrare lo stato di avanzamento quando ogni passaggio viene completato in modo proporzionale alla quantità di tempo che ogni passaggio richiede in genere. Usare un indicatore di stato indeterminato solo se un indicatore di stato determinato provocherebbe la conclusione non corretta dell'operazione da parte degli utenti.

**Se si esegue una sola operazione...**

Assicurarsi di fornire il feedback sullo stato di avanzamento per le operazioni di lunga durata e che le informazioni sopra indicate siano chiaramente comunicate. Utilizzare le barre di stato determinate laddove possibile.

## <a name="usage-patterns"></a>Modelli di utilizzo

Gli indicatori di stato hanno diversi modelli di utilizzo:

### <a name="determinate-progress-bars"></a>Indicatori di stato determinati



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Indicatori di stato determinati modale</strong><br/> Indicare lo stato di avanzamento di un'operazione compilando da sinistra a destra e riempiendo completamente al termine dell'operazione. <br/></td>
<td>Poiché questo feedback è <a href="glossary.md">modale</a>, gli utenti non possono eseguire altre attività nella finestra (o nel relativo elemento padre se visualizzate in una finestra di dialogo modale) finché l'operazione non è stata completata. <br/> <img src="images/progress-bars-image3.png" alt="Screen shot of progress bar in modal window " /><br/> In questo esempio, l'indicatore di stato fornisce commenti e suggerimenti durante la configurazione. <br/></td>
</tr>
<tr class="even">
<td><strong>Indicatori di stato determinati in modalità modale con pulsante Annulla o arresta</strong><br/> Consentire agli utenti di interrompere l'operazione, probabilmente perché l'operazione sta richiedendo troppo tempo o se non vale la pena aspettare.<br/></td>
<td><img src="images/progress-bars-image4.png" alt="Screen shot of progress bar with Stop button " /><br/> In questo esempio, gli utenti possono fare clic su Interrompi per arrestare l'operazione e lasciare l'ambiente nello stato corrente.<br/></td>
</tr>
<tr class="odd">
<td><strong>Indicatori di stato determinati in modalità modale con pulsante Annulla o Interrompi e animazione</strong><br/> Consentire agli utenti di arrestare l'operazione e includere un'animazione per consentire agli utenti di visualizzare l'effetto di un'operazione.<br/></td>
<td><img src="images/progress-bars-image5.png" alt="Screen shot of progress bar with animation " /><br/> In questo esempio, gli utenti possono fare clic su Interrompi per arrestare l'operazione e lasciare l'ambiente nello stato corrente.<br/></td>
</tr>
<tr class="even">
<td><strong>Barre di stato doppie determinate modale</strong><br/> Indicare lo stato di avanzamento di un'operazione in più passaggi mostrando lo stato di avanzamento del passaggio corrente nel primo indicatore di stato e lo stato di avanzamento generale nella seconda barra.<br/></td>
<td>Poiché il primo indicatore di stato fornisce poche informazioni aggiuntive e può risultare piuttosto distrazione, questo modello non è consigliato. Al contrario, tutti i passaggi dell'operazione condividono una parte dello stato di avanzamento e un singolo indicatore di stato passa al completamento una volta. <br/> <img src="images/progress-bars-image6.png" alt="Screen shot of current and overall progress bars " /><br/> In questo esempio, il primo indicatore di stato Mostra lo stato di avanzamento del passaggio corrente e il secondo indicatore di stato Mostra lo stato di avanzamento generale.<br/>
<blockquote>
[!Note]<br />
Questo modello non è in genere necessario e deve essere evitato.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Indicatori di stato determinati non modale</strong><br/> Indicare lo stato di avanzamento di un'operazione compilando da sinistra a destra e riempiendo completamente al termine dell'operazione.<br/></td>
<td>Diversamente dagli indicatori di stato modale, gli utenti possono eseguire altre attività mentre è in corso l'operazione. Questi indicatori di stato possono essere visualizzati nel contesto o in una barra di stato. <br/> <img src="images/progress-bars-image7.png" alt="Screen shot of progress bar on status bar " /><br/> In questo esempio Windows Internet ExplorerWindows Internet Explorer visualizza lo stato di avanzamento per il caricamento di una pagina Web sulla barra di stato. Gli utenti possono eseguire altre attività durante il caricamento della pagina.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="indeterminate-progress-bars"></a>Indicatori di stato indeterminati



|                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Indicatori di stato indeterminato modale**<br/> indica che è in corso un'operazione visualizzando un'animazione che scorre continuamente sulla barra da sinistra a destra. <br/>   | Utilizzato solo per le operazioni di cui non è possibile determinare lo stato di avanzamento generale, pertanto non esiste alcuna nozione di completezza. è preferibile specificare indicatori di stato determinati perché indicano la percentuale approssimativa dell'operazione completata e consentono agli utenti di determinare se è opportuno continuare l'operazione. sono anche meno distracting visivamente. <br/> ![screenshot dell'indicatore di stato modale e indeterminato](images/progress-bars-image8.png)<br/> In questo esempio Windows Update utilizza un indicatore di stato indeterminato modale per indicare lo stato di avanzamento durante la ricerca degli aggiornamenti.<br/> |
| **Indicatori di stato indeterminati non modale**<br/> indica che è in corso un'operazione visualizzando un'animazione che scorre continuamente sulla barra da sinistra a destra.<br/> | Diversamente dagli indicatori di stato modale, gli utenti possono eseguire altre attività mentre è in corso l'elaborazione. questi indicatori di stato possono essere visualizzati nel contesto o in una barra di stato. <br/> ![screenshot della barra di avanzamento sottile nella finestra di Outlook ](images/progress-bars-image9.png)<br/> In questo esempio Microsoft Outlook usa un indicatore di stato indeterminato non modale durante il riempimento delle proprietà del contatto. Gli utenti possono continuare a usare la finestra delle proprietà mentre questo lavoro è in corso.<br/>                                                                                                                    |



 

### <a name="meters"></a>Metri



|                                                                                          |                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Metri**<br/> indicare una percentuale che non è correlata allo stato di avanzamento. <br/> | Questo modello non è un indicatore di stato, ma viene implementato usando il controllo indicatore di stato. i contatori hanno un aspetto distinto per distinguerli dalle barre di stato reali. <br/> ![screenshot del contatore che mostra lo spazio disponibile su disco ](images/progress-bars-image10.png)<br/> In questo esempio il contatore mostra la percentuale di spazio su disco utilizzato.<br/> |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Fornire un feedback sullo stato di avanzamento quando si esegue un'operazione di lunga durata.** Gli utenti non devono mai indovinare se lo stato di avanzamento viene eseguito.
-   **Indica chiaramente lo stato di avanzamento effettivo.** L'indicatore di stato deve avanzare in caso di avanzamento. Se l'intervallo di tempo previsto per il completamento è elevato, provare a usare una scala non lineare per indicare lo stato di avanzamento per più tempo. Non si vuole che gli utenti concludano il blocco del programma quando non lo è.
-   **Indica chiaramente la mancanza di stato.** Se non viene eseguito alcun avanzamento, l'indicatore di stato non deve avanzare. Non si vuole che gli utenti attendano indefinitamente un'operazione che non verrà mai completata.
-   **Fornire dettagli utili sullo stato di avanzamento.** Fornire informazioni aggiuntive sullo stato di avanzamento, ma solo se gli utenti possono eseguire un'operazione. Verificare che il testo venga visualizzato abbastanza a lungo da consentire agli utenti di leggerlo.

    ![screenshot dell'indicatore di stato che mostra la velocità di trasferimento ](images/progress-bars-image11.png)

    In questo esempio, gli utenti possono visualizzare la velocità di trasferimento. La velocità di trasferimento ridotta suggerisce la necessità di usare una connessione di rete con larghezza di banda elevata.

-   **Non fornire dettagli superflui.** In genere gli utenti non sono interessati ai dettagli dell'operazione eseguita. Ad esempio, gli utenti di un programma di installazione non sono interessati al file specifico copiato o ai componenti di sistema in corso di registrazione, perché non hanno aspettative su questi dettagli. In genere, un indicatore di stato con l'etichetta fornita da solo fornisce informazioni sufficienti, quindi fornire informazioni aggiuntive sullo stato di avanzamento solo se gli utenti possono eseguire un'operazione. Fornire dettagli che gli utenti non sono interessati a rende l'esperienza utente eccessivamente complicata e tecnica. Se sono necessarie informazioni più dettagliate per il debug, non visualizzarle nelle build di rilascio.

    **Corretto:**

    ![screenshot dello stato dell'installazione ](images/progress-bars-image12.png)

    In questo esempio, l'indicatore di stato con etichetta è sufficiente.

    **Corretto:**

    ![screenshot dell'indicatore di stato che mostra la velocità di trasferimento ](images/progress-bars-image11.png)

    In questo esempio Esplora risorse copia i file selezionati dall'utente, quindi la visualizzazione dei nomi di file da copiare è significativa.

    **Non corretto:**

    ![screenshot dello stato di avanzamento della registrazione ](images/progress-bars-image13.png)

    In questo esempio un programma di installazione fornisce dettagli che non sono significativi per l'utente.

-   **Fornire animazioni utili.** Se questa operazione è stata eseguita correttamente, le animazioni migliorano l'esperienza utente aiutando gli utenti a visualizzare l'operazione. Le animazioni valide hanno un effetto maggiore rispetto al testo. Ad esempio, l'indicatore di stato per il comando di eliminazione di Outlook Visualizza il cestino per la destinazione se è possibile ripristinare i file, ma non il cestino se i file non possono essere recuperati.

    ![screenshot dello stato di avanzamento dell'eliminazione ](images/progress-bars-image14.png)

    In questo esempio, la mancanza di un cestino rafforza il fatto che i file vengano eliminati definitivamente. Queste informazioni aggiuntive non verranno comunicate in modo efficace usando solo testo.

-   **Non usare animazioni non necessarie.** Le animazioni possono essere fuorvianti perché in genere vengono eseguite in un thread separato dall'attività effettiva e pertanto possono suggerire lo stato di avanzamento anche se l'operazione è stata bloccata. Inoltre, se l'operazione è più lenta del previsto, gli utenti talvolta presuppongono che l'animazione faccia parte del motivo. Di conseguenza, utilizzare le animazioni solo quando è presente una giustificazione chiara; non usarli per provare a intrattenere gli utenti.
-   **Posizionare le animazioni centrate sull'indicatore di stato.** Inserire l'animazione sopra le etichette dell'indicatore di stato, se disponibile. Se è presente un pulsante Annulla o Interrompi a destra dell'indicatore di stato, includere il pulsante quando si determina il centro.
-   **Riprodurre un effetto acustico al termine di un'operazione solo se è molto lungo (più di due minuti), poco frequente e importante.** Se l'utente è probabilmente in grado di uscire da un'operazione importante durante l'elaborazione, un effetto acustico consente di ripristinare l'attenzione dell'utente. L'uso di un effetto acustico al completamento in altre circostanze costituisce un fastidio fastidioso.
-   **Non rubare lo stato attivo per l'input per visualizzare un aggiornamento o un completamento dello stato.** Gli utenti spesso passano ad altri programmi in attesa e non vogliono essere interrotti. Le attività in background devono rimanere in background.
-   **Non preoccuparti del supporto tecnico.** Poiché il feedback fornito dagli indicatori di stato non è necessariamente accurato ed è flottante, le barre di stato non sono un meccanismo valido per fornire informazioni per il supporto tecnico. Di conseguenza, se l'operazione può avere esito negativo (come nel caso di un programma di installazione), non fornire informazioni aggiuntive sullo stato di avanzamento utili solo per il supporto tecnico. Fornire invece un meccanismo alternativo, ad esempio un file di log, per registrare le informazioni di supporto tecnico.

    **Non corretto:**

    ![screenshot dell'indicatore di stato che mostra il nome del server ](images/progress-bars-image15.png)

    In questo esempio, l'indicatore di stato Mostra i dettagli destinati al supporto tecnico.

-   **Non inserire la percentuale di completamento o qualsiasi altro testo su un indicatore di stato.** Tale testo non è accessibile e non è compatibile con l'uso dei temi.

    **Non corretto:**

    ![screenshot dell'indicatore di stato con testo sulla barra ](images/progress-bars-image16.png)

    In questo esempio, il testo in percentuale nell'indicatore di stato non è accessibile.

-   **Non combinare un indicatore di stato con un puntatore occupato.** Usare uno o l'altro, ma non entrambi contemporaneamente.
-   **Non usare barre di stato verticali.** Gli indicatori di stato orizzontali hanno un mapping più naturale e un flusso migliore.

### <a name="determinate-progress-bars"></a>Indicatori di stato determinati

-   **Utilizzare gli indicatori di stato determinati per le operazioni che richiedono un periodo di tempo limitato,** anche se non è possibile prevedere accuratamente tale periodo di tempo. Gli indicatori di stato indeterminati mostrano che lo stato di avanzamento viene effettuato, ma non forniscono altre informazioni. Non scegliere un indicatore di stato indeterminato in base solo alla possibile mancanza di precisione.
-   **Indica chiaramente la fase di avanzamento.** L'indicatore di stato deve essere in grado di indicare se l'operazione si trova all'inizio, al centro o alla fine di un'operazione. Ad esempio, gli indicatori di stato che rientrano immediatamente nel completamento del 99%, quindi rimaneno da molto tempo sono particolarmente informativi e fastidiosi. In questi casi, l'indicatore di stato deve essere impostato inizialmente su un massimo del 33% per indicare che l'operazione è ancora nella fase iniziale.
-   **Indica chiaramente il completamento.** Non lasciare che un indicatore di stato vada al 100%, a meno che l'operazione non sia stata completata.
-   **Fornire una stima del tempo rimanente se è possibile eseguire questa operazione in modo accurato.** Le stime del tempo rimanenti accurate sono utili, ma le stime che si trovano fuori dal contrassegno o rimbalzano in modo significativo non sono utili. Prima di poter assegnare stime accurate, potrebbe essere necessario eseguire alcune operazioni di elaborazione. In tal caso, non visualizzare stime potenzialmente non accurate durante questo periodo iniziale.
-   **Non riavviare lo stato di avanzamento.** Un indicatore di stato perde il suo valore se viene riavviato (forse perché un passaggio nell'operazione viene completato) perché gli utenti non hanno modo di sapere quando l'operazione verrà completata. Al contrario, tutti i passaggi dell'operazione condividono una parte dello stato di avanzamento e l'indicatore di stato passa al completamento una volta.

    **Non corretto:**

    ![screenshot dell'indicatore di stato riavviato ](images/progress-bars-image17.png)

    In questo esempio, l'operazione è stata spostata nel passaggio di copia dei file e Reimposta l'indicatore di stato per il passaggio. Ora gli utenti non hanno idea della quantità di avanzamento o del tempo rimanente.

-   **Non eseguire il backup dello stato di avanzamento.** Come per il riavvio, un indicatore di stato perde il relativo valore se viene eseguito il backup. Aumentare sempre la progressione monotona. Tuttavia, è possibile avere una stima rimanente del tempo che aumenta (così come diminuisce) perché la velocità di avanzamento può variare.

### <a name="indeterminate-progress-bars"></a>Indicatori di stato indeterminati

-   **Utilizzare le barre di stato Indeterminate solo per le operazioni di cui non è possibile determinare lo stato generale.** Utilizzare gli indicatori di stato indeterminati per le operazioni che richiedono un periodo di tempo illimitato o che accedono a un numero sconosciuto di oggetti. Usare i timeout per assegnare i limiti alle operazioni basate sul tempo.
-   **Eseguire la conversione in un indicatore di stato determinato quando è possibile determinare lo stato di avanzamento generale.** Se, ad esempio, sono necessari più di due secondi per determinare il numero di oggetti, è possibile utilizzare una barra di avanzamento indeterminata mentre gli oggetti vengono conteggiati, quindi convertirli in un indicatore di stato determinato.
-   **Non combinare le barre di avanzamento indeterminate con percentuali di completamento o stime rimanenti del tempo.** Se è possibile fornire queste informazioni, utilizzare invece un indicatore di stato determinato.
-   **Non combinare barre di stato Indeterminate con animazioni.** Un indicatore di stato indeterminato è in realtà un'animazione generica ed è quindi consigliabile usare uno o l'altro, ma mai entrambi.

    **Corretto:**

    ![screenshot dello stato di avanzamento del rilevamento del server ](images/progress-bars-image18.png)

    In questo esempio viene usata solo un'animazione per indicare che un'operazione è in corso.

### <a name="modeless-progress-bars"></a>Indicatori di stato non modale

-   **Se gli utenti possono produrre qualcosa di produttivo mentre è in corso l'operazione, fornire commenti e suggerimenti non modale.** Potrebbe essere necessario disabilitare un subset di funzionalità che richiede il completamento dell'operazione.
-   **Se la finestra dispone di una barra degli indirizzi, visualizzare lo stato non modale nella barra degli indirizzi.**

    ![screenshot dell'indicatore di stato come parte della barra degli indirizzi ](images/progress-bars-image19.png)

    In questo esempio lo stato non modale viene visualizzato nella barra degli indirizzi.

-   In caso contrario, **se la finestra dispone di una barra di stato, visualizzare lo stato non modale sulla barra di stato.** Inserire un testo corrispondente a sinistra nella barra di stato.

    ![screenshot dell'indicatore di stato come parte della barra di stato ](images/progress-bars-image7.png)

    In questo esempio lo stato non modale viene visualizzato nella barra di stato.

### <a name="modal-progress-bars"></a>Indicatori di stato modale

-   **Posizionare le barre di avanzamento modale nelle finestre di stato o nelle** [finestre](win-dialog-box.md)di stato.
-   **Fornire un pulsante di comando per arrestare l'operazione se il completamento richiede più di alcuni secondi oppure non è possibile completare mai il tentativo.** Etichetta il pulsante Annulla se l'annullamento restituisce l'ambiente allo stato precedente (lasciando nessun effetto collaterale); in caso contrario, etichetta il pulsante Interrompi per indicare che l'operazione parzialmente completata è intatta. È possibile modificare l'etichetta del pulsante da Annulla per arrestarsi al centro dell'operazione se a un certo punto non è possibile ripristinare lo stato precedente dell'ambiente. Allineare al centro il pulsante di comando con l'indicatore di stato anziché allineare i vertici.

    **Corretto:**

    ![screenshot dello stato di avanzamento dell'attesa della rete ](images/progress-bars-image20.png)

    In questo esempio, l'arresto della connessione di rete non ha alcun effetto collaterale, pertanto viene usato Cancel.

    **Corretto:**

    ![screenshot dell'indicatore di stato che mostra il tempo di copia rimasto ](images/progress-bars-image21.png)

    In questo esempio, l'arresto della copia lascia tutti i file copiati, quindi il pulsante di comando viene contrassegnato come stop.

    **Non corretto:**

    ![screenshot della barra di stato della ricerca e del pulsante Arresta ](images/progress-bars-image22.png)

    In questo esempio, l'arresto della ricerca non lascia alcun effetto collaterale, quindi il pulsante di comando deve essere etichettato Annulla.

### <a name="time-remaining"></a>Tempo rimanente

Per gli indicatori di stato determinati:

-   **Usare i formati di ora seguenti.** Iniziare con il primo dei formati seguenti, in cui l'unità di tempo più grande non è zero e quindi passare al formato successivo quando l'unità di tempo più grande diventa zero.

    **Per gli indicatori di stato:**

    **Se le informazioni correlate vengono visualizzate nel formato due punti:**

    Tempo rimanente: h ore, m minuti

    Tempo rimanente: m minuti, s secondi

    Tempo rimanente: s secondi

    **Se lo spazio sullo schermo è Premium:**

    ore h, m minuti rimanenti

    m min, s sec rimanenti

    secondi rimanenti

    **In caso contrario**

    ore h, m minuti rimanenti

    m minuti, s secondi rimanenti

    secondi rimanenti

    **Per le barre del titolo:**

    HH: mm rimanenti

    mm: SS rimanenti

    0: SS rimanenti

    Questo formato compatto Mostra prima le informazioni più importanti, in modo che non vengano troncate sulla barra delle applicazioni.

-   **Rendere accurate le stime, ma non dare una precisione falsa.** Se l'unità più grande è di ore, concedere minuti (se significativo) ma non secondi.

    **Non corretto:**

    hh ore, mm minuti, ss secondi

-   **Tenere aggiornata la stima.** Aggiornare le stime rimanenti almeno ogni 5 secondi.
-   **Concentrarsi sul tempo rimanente, in** quanto si tratta delle informazioni che gli utenti si occupano maggiormente. Fornire tempo totale trascorso solo quando sono presenti scenari in cui è utile il tempo trascorso, ad esempio quando è probabile che l'attività venga ripetuta. Se il tempo rimanente stimato è associato a un indicatore di stato, non è presente un testo con percentuale di completamento perché tali informazioni vengono trasmesse dall'indicatore di stato.
-   **Essere grammaticamente corretti.** Usare unità singolari quando il numero è uno.

    **Non corretto:**

    1 minuto, 1 secondo

-   **Usare le maiuscole/minuscole come nelle frasi comuni.**

### <a name="progress-bar-colors"></a>Colori dell'indicatore di stato

-   **Utilizzare le barre di stato rosse o gialle solo per indicare lo stato di avanzamento, non i risultati finali di un'attività.** Un indicatore di stato rosso o giallo indica che gli utenti devono eseguire un'azione per completare l'attività. Se la condizione non è reversibile, lasciare l'indicatore di stato verde e visualizzare un messaggio di errore.
-   **Trasformare l'indicatore di stato in rosso quando è presente una condizione reversibile dall'utente che impedisce l'esecuzione di ulteriori progressi.** Visualizzare un messaggio per spiegare il problema e consigliare una soluzione.
-   **Impostare l'indicatore di stato come giallo per indicare che l'utente ha sospeso l'attività o che è presente una condizione che impedisce lo stato di** avanzamento, ma lo stato di avanzamento è ancora in corso (ad esempio, con una connettività di rete insufficiente). Se l'utente è stato sospeso, modificare l'etichetta del pulsante Sospendi per riprendere. Se lo stato di avanzamento è ostacolato, visualizzare un messaggio per spiegare il problema e consigliare una soluzione.

### <a name="meters"></a>Metri

-   **Utilizzare le barre di stato solo per lo stato di avanzamento.** Usare i contatori per indicare le percentuali non correlate allo stato di avanzamento.

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![diagramma che mostra il ridimensionamento e la spaziatura della barra di avanzamento ](images/progress-bars-image23.png)

Dimensionamento e spaziatura consigliati per gli indicatori di stato.

-   Usare sempre l'altezza consigliata dell'indicatore di stato.
    -   **Eccezione:** È possibile utilizzare un'altezza diversa se la finestra padre non supporta l'altezza consigliata.
-   Utilizzare la larghezza minima se si desidera rendere l'indicatore di stato non intrusivo.
-   Non usare larghezze più lunghe del valore massimo consigliato. L'indicatore di stato non deve occupare lo spazio disponibile.
-   Centrare l'indicatore di stato orizzontalmente se la finestra è molto più ampia della larghezza massima consigliata.

## <a name="labels"></a>Etichette

### <a name="progress-bar-labels"></a>Etichette indicatore di stato

-   **Utilizzare un'etichetta concisa con un controllo testo statico per indicare l'operazione eseguita.** Avviare l'etichetta con un verbo (ad esempio, copiando) e terminare con i puntini di sospensione. Questa etichetta può variare in modo dinamico se l'operazione ha più passaggi o sta elaborando più oggetti.
-   Non assegnare una [chiave di accesso](glossary.md) univoca perché il controllo non è interattivo.
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Se l'operazione non è stata avviata direttamente dall'utente, è possibile includere un'etichetta aggiuntiva per fornire il contesto e chiedere scusa per l'interruzione. Inizia questa etichetta aggiuntiva con la frase. Attendi. Questa etichetta non deve cambiare durante l'operazione.

    ![screenshot dell'indicatore di stato con etichetta ](images/progress-bars-image24.png)

    In questo esempio, all'utente viene chiesto di attendere che l'utente non abbia avviato direttamente l'operazione.

-   Posizionare l'etichetta sopra l'indicatore di stato e allineare l'etichetta al bordo sinistro dell'indicatore di stato.

### <a name="progress-bar-details"></a>Dettagli indicatore di stato

-   Specificare i dettagli nel testo statico, che precede i dati con un'etichetta che termina con i due punti. Specificare le unità (secondi, kilobyte e così via) dopo il testo dei dettagli.

    **Corretto:**

    ![screenshot dell'indicatore di stato che mostra la velocità di trasferimento ](images/progress-bars-image11.png)

    In questo esempio, i dettagli sono etichettati correttamente.

    **Non corretto:**

    ![screenshot dell'indicatore di stato senza etichetta corretta ](images/progress-bars-image25.png)

    In questo esempio i dettagli non sono contrassegnati, quindi è necessario che gli utenti ne determinino il significato.

-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Posizionare i dettagli sotto l'indicatore di stato e allineare l'etichetta al bordo sinistro dell'indicatore di stato.
-   Non assegnare la percentuale completa o rimanente perché tali informazioni vengono trasmesse dall'indicatore di stato.

### <a name="cancel-button"></a>Scegliere il pulsante Annulla.

-   Etichetta il pulsante Annulla se l'annullamento restituisce l'ambiente allo stato precedente (lasciando nessun effetto collaterale); in caso contrario, etichettare il pulsante Interrompi per indicare che lascia intatta l'operazione parzialmente completata.
-   È possibile modificare l'etichetta del pulsante da Annulla per arrestarsi al centro dell'operazione se a un certo punto non è possibile ripristinare lo stato precedente dell'ambiente.

### <a name="progress-dialog-box-titles"></a>Titoli della finestra di dialogo stato

-   Se la barra di stato viene visualizzata in una finestra di dialogo modale, il titolo della finestra di dialogo deve essere il nome del programma o il nome dell'operazione. Non usare quello che dovrebbe essere l'etichetta dell'indicatore di stato per il titolo della finestra di dialogo.

    **Corretto:**

    ![screenshot del titolo dell'indicatore di stato con nome attività ](images/progress-bars-image26.png)

    In questo esempio, il nome dell'attività viene usato per il titolo della finestra di dialogo.

    **Non corretto:**

    ![screenshot del titolo della finestra di dialogo ridondante ](images/progress-bars-image27.png)

    In questo esempio, il testo del titolo della finestra di dialogo è una ripubblicazione dell'etichetta dell'indicatore di stato. In alternativa, è necessario usare il nome del programma.

-   Se l'indicatore di stato viene visualizzato in una finestra di dialogo non modale, ottimizzare il titolo per la visualizzazione sulla barra delle applicazioni, inserendo prima di tutto le informazioni di distinzione. Esempio: "66% completato".

 

