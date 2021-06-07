---
title: Notifiche (nozioni di base sulla progettazione)
description: Una notifica informa gli utenti degli eventi non correlati all'attività dell'utente corrente, visualizzando brevemente un fumetto da un'icona nell'area di notifica.
ms.assetid: dcac2fb7-e503-4ea3-a2c5-e3cb660c040a
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: be783ac6aac25e818d4ddf3612c726e55efa5fa5
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524515"
---
# <a name="notifications-design-basics"></a>Notifiche (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Una notifica informa gli utenti degli eventi non correlati all'attività dell'utente corrente, visualizzando brevemente un fumetto da un'icona nell'area di notifica. La notifica può essere il risultato di un'azione dell'utente o di un evento di sistema significativo o potrebbe offrire informazioni potenzialmente utili da Microsoft Windows o da un'applicazione.

Le informazioni contenute in una notifica sono **utili e rilevanti, ma non sono mai critiche.** Di conseguenza, le notifiche non richiedono un intervento immediato da parte dell'utente e gli utenti possono ignorarle liberamente.

![Screenshot del balloon con "nuovi aggiornamenti" nel titolo ](images/mess-notif-image1.png)

Una notifica tipica.

In Windows Vista e versioni successive le notifiche vengono visualizzate per una durata fissa di 9 secondi. Le notifiche non vengono visualizzate immediatamente quando gli utenti sono inattivi o gli screen saver sono in esecuzione. Windows accoda automaticamente le notifiche durante questi orari e visualizza le notifiche in coda quando l'utente riprende la normale attività. Di conseguenza, non è necessario eseguire operazioni per gestire queste circostanze speciali.

**Sviluppatori:** È possibile determinare quando l'utente è attivo usando l'API SHQueryUserNotificationState.

**Nota:** Le linee guida relative [all'area di](winenv-notification.md)notifica, [alla](winenv-taskbar.md)barra delle applicazioni e ai [balloon sono](ctrl-balloons.md) presentate in articoli separati.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, prendi in considerazione queste domande:

-   **Le informazioni sono il risultato diretto immediato dell'interazione degli utenti con l'applicazione?** In tal caso, visualizzare queste informazioni sincrone direttamente all'interno dell'applicazione usando invece una finestra di dialogo [,](win-dialog-box.md)una finestra di [messaggio,](glossary.md)un [balloon](ctrl-balloons.md)o l'interfaccia [utente](glossary.md) sul posto. Le notifiche sono solo per informazioni asincrone.

![Screenshot dell'avviso di sicurezza di Windows ](images/mess-notif-image2.png)

In questo esempio la finestra di dialogo Eccezioni di Windows Firewall viene visualizzata come risultato diretto dell'interazione dell'utente. Una notifica non è appropriata in questo caso.

-   **Le informazioni sono rilevanti solo quando gli utenti usano attivamente l'applicazione?** In tal caso, visualizzare le informazioni nella barra di stato dell'applicazione o [in](ctrl-status-bars.md) un'altra area di stato.

![Screenshot della barra di stato di Outlook ](images/mess-notif-image3.png)

In questo esempio Outlook visualizza la connessione e lo stato di sincronizzazione sulla barra di stato.

-   **Le informazioni cambiano rapidamente, in modo continuo e in tempo reale?** Ad esempio, lo stato di avanzamento dell'elaborazione, le quotazioni azionarie e i punteggi sport. In tal caso, non usare le notifiche perché non sono adatte per le informazioni che cambiano rapidamente.
-   **Le informazioni sono utili e pertinenti? È probabile che gli utenti cambino il proprio comportamento o evitino inconvenienti a causa della ricezione delle informazioni?** In caso contrario, non visualizzare le informazioni o inserire le informazioni in una finestra di stato o in un file di log.
-   **Le informazioni sono critiche? È necessaria un'azione immediata?** In tal caso, visualizzare le informazioni usando un'interfaccia che richiede attenzione e non può essere facilmente ignorata, ad esempio una finestra di dialogo modale o una finestra di messaggio. Se il programma non è attivo, puoi attirare [l'attenzione](winenv-taskbar.md) sulle informazioni critiche facendo lampeggiare tre volte il pulsante della barra delle applicazioni del programma e lasciandolo evidenziato fino a quando il programma non è attivo.
-   **I principali utenti di destinazione sono i professionisti IT?** In tal caso, usare un meccanismo di feedback alternativo, ad esempio [voci di file](glossary.md) di log o messaggi di posta elettronica. I professionisti IT preferiscono fortemente i file di log per le informazioni non critiche. Inoltre, i server vengono spesso gestiti in remoto e in genere vengono eseguiti senza alcun utente connesso, rendendo inefficaci le notifiche.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Le notifiche efficaci che promuovono una buona esperienza utente sono:

-   **Asincrona.** L'evento non è un risultato diretto immediato dell'interazione corrente degli utenti con Microsoft Windows o con l'applicazione.
-   **Utile.** Esiste una ragionevole probabilità che gli utenti eseereranno un'attività o modificheranno il proprio comportamento come risultato della notifica.
-   **rilevante.** La notifica visualizza informazioni utili che gli utenti sono importanti e che non conoscono già.
-   **Non critico.** Le notifiche non sono modali e non richiedono l'interazione dell'utente, quindi gli utenti possono ignorarle liberamente.
-   **Eseguibili.** Per le notifiche che suggeriscono di eseguire un'azione, tale azione viene avviata facendo clic sulla notifica. Tuttavia, l'azione può sempre essere posticipata.
-   **Presentato in modo appropriato.** La presentazione della notifica (durata, frequenza, testo, icona e interattività) corrisponde alle circostanze.
-   **Non è fastidioso.** C'è una linea fine tra le comunicazioni che informano gli utenti di un evento e la loro esecuzione.

Sfortunatamente, sono presenti troppe notifiche inappropriati, inappropriati, inutili e irrilevanti. Prendere in considerazione queste notifiche dalla Hall of Disartie di Windows XP:

![screenshot della notifica "presentazione di windows xp" ](images/mess-notif-image4.png)

![Screenshot della notifica "Icone inutilizzate" ](images/mess-notif-image5.png)

![Screenshot della notifica di aggiunta di .NET Passport ](images/mess-notif-image6.png)

In questi esempi, Windows XP tenta di assistere gli utenti nella configurazione iniziale. Tuttavia, queste notifiche vengono visualizzate troppo spesso e ben dopo essere state utili, quindi sono poco più di annunci di funzionalità non richieste.

## <a name="user-flow-must-be-maintained"></a>È necessario mantenere il flusso utente

**Idealmente, gli utenti immersi nel proprio lavoro non visualizzano affatto le notifiche. Al contrario, vedranno le notifiche solo quando il flusso è già interrotto.**

In Flow: The Satisfactiony of Optimal Experience, Mihaly Csikszentmihalyi afferma che gli utenti entrano in uno stato di flusso quando sono completamente soddisfatti dell'attività durante la quale perdono il senso del tempo e sono soddisfatti.

**Le notifiche efficaci consentono agli utenti di mantenere il flusso presentando informazioni utili e rilevanti che possono essere facilmente ignorate.** Le notifiche vengono presentate in modo periferico e a bassa chiave e non richiedono l'interazione.

Non presupporre che, se le notifiche sono [non modanti,](glossary.md) non possono essere un'interruzione fastidiosa. Le notifiche non richiedono l'attenzione degli utenti, ma lo richiedono sicuramente. È possibile interrompere il flusso degli utenti nel modo seguente:

-   Visualizzazione di notifiche non importanti per gli utenti.
-   Visualizzazione troppo frequente di una notifica.
-   Uso di più notifiche quando è sufficiente una singola notifica.
-   Uso dell'audio durante la visualizzazione di una notifica.

In Windows 7 gli utenti hanno il controllo finale sulle notifiche. **Se gli utenti trovano che le notifiche di un programma sono troppo fastidiose, possono scegliere di eliminare tutte le notifiche da tale programma.** Assicurarsi che gli utenti non esercitino questa operazione al programma presentando informazioni utili e rilevanti e seguendo queste linee guida.

## <a name="notifications-must-be-ignorable"></a>Le notifiche devono essere ignorabili

**Le notifiche non richiedono un intervento immediato da parte dell'utente e gli utenti possono ignorarle liberamente.**

Gli sviluppatori e i progettisti spesso vogliono presentare le notifiche in un modo che gli utenti non possono ignorare. Questo obiettivo interrompe completamente il vantaggio principale delle notifiche perché interrompe il flusso degli utenti. Se gli utenti sono distratti dalle notifiche o sono obbligati a leggerle, la progettazione delle notifiche non è riuscita.

**Se si ritiene che gli utenti ignorino le notifiche, tenere presente quanto segue:**

-   Se si usano correttamente le notifiche e non è necessario un intervento immediato da parte dell'utente, fare in modo che gli utenti sceglino di ignorarle per impostazione predefinita. Non modificare questa impostazione.
-   Se l'evento richiede un'azione immediata da parte dell'utente, usare un'interfaccia utente alternativa che gli utenti non possono ignorare. Vedere Questa è l'interfaccia utente giusta? per le alternative.

## <a name="use-progressive-escalation-where-applicable"></a>Usare l'escalation progressiva dove applicabile

Se viene usata una notifica per un evento che gli utenti possono ignorare in un primo momento, ma che alla fine deve essere affrontata, è consigliabile usare un'interfaccia utente alternativa quando la situazione diventa critica. Questa tecnica è nota come escalation progressiva.

Ad esempio, il sistema di risparmio energia di Windows indica inizialmente una batteria in esaurimento modificando semplicemente l'icona dell'area di notifica.

![Screenshot di sei icone che mostrano lo stato della batteria ](images/mess-notif-image7.png)

In questi esempi, il risparmio energia di Windows usa l'icona dell'area di notifica per notificare agli utenti l'interruzione progressiva dell'alimentazione a batteria.

Quando l'alimentazione della batteria si riduce, Windows avvisa gli utenti dell'interruzione dell'alimentazione a batteria tramite una notifica.

![Screenshot della notifica di alimentazione a batteria in esaurimento](images/mess-notif-image8.png)

In questo esempio, il risparmio energia di Windows usa una notifica per indicare agli utenti che l'alimentazione a batteria è debole.

Questa notifica viene visualizzata mentre gli utenti hanno ancora diverse opzioni. Gli utenti possono collegarsi, modificare le opzioni di risparmio energia, eseguire il wrapping del lavoro e arrestare il computer oppure ignorare la notifica e continuare a funzionare. Con l'esaurimento della batteria, il testo e l'icona della notifica riflettono l'urgenza aggiuntiva. Tuttavia, quando l'alimentazione a batteria diventa così bassa che gli utenti devono agire immediatamente, Il risparmio energia di Windows invia una notifica agli utenti usando una [finestra di](glossary.md) messaggio modale.

![Screenshot dell'avviso relativo all'alimentazione a batteria in esaurimento](images/mess-notif-image9.png)

In questo esempio, il risparmio energia di Windows usa una finestra di messaggio modale per notificare agli utenti l'alimentazione a batteria in condizioni critiche.

**Se si eservino solo tre operazioni...**

1.  Usare le notifiche solo se è effettivamente necessario. Quando si visualizza una notifica, si potrebbero interrompere gli utenti o addirittura disturbarli. Assicurarsi che l'interruzione sia giustificata.
2.  Usare le notifiche per eventi non critici o situazioni che non richiedono un'azione immediata dell'utente. Per eventi critici o situazioni che richiedono un'azione immediata dell'utente, usare un'interfaccia utente alternativa, ad esempio una finestra di dialogo modale.
3.  Se si usano le notifiche, è possibile renderla un'esperienza utente ottimale. Non provare a forzare gli utenti a visualizzare le notifiche. Se gli utenti sono così immersi nel lavoro che non vedono le notifiche, la progettazione è buona.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le notifiche hanno diversi modelli di utilizzo:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Azione riuscita</strong><br/> Notifica agli utenti quando un'azione asincrona avviata dall'utente viene completata correttamente. <br/></td>
<td><strong>Corretto:</strong><br/> <img src="images/mess-notif-image10.png" alt="Screen shot of balloon showing successful updates " /><br/> In questo esempio, Windows Update gli utenti quando il computer è stato aggiornato correttamente.<br/> <strong>Non corretto:</strong><br/> <img src="images/mess-notif-image11.png" alt="Screen shot of balloon showing file check complete " /><br/> In questo esempio Microsoft Outlook invia una notifica agli utenti al termine di un controllo del file di dati. Cosa dovrebbero fare gli utenti ora? E perché avvisare gli utenti del completamento corretto?<br/> <strong>Mostra quando:</strong> Al completamento di un'attività asincrona. Notificare agli utenti le azioni riuscite solo se è probabile che siano in attesa del completamento o dopo errori recenti.<br/> <strong>Mostra come:</strong> Usare l'opzione in tempo reale in modo che queste notifiche non siano in coda quando gli utenti eseguono un'applicazione a schermo intero o non usano attivamente il computer.<br/> <strong>Mostra la frequenza con cui:</strong> una volta.<br/> <strong>Fattore di infastidimento:</strong> Basso se l'esito positivo non è previsto a causa di errori recenti, l'esito positivo è dopo un errore critico o altamente insolito, quindi l'utente necessita di commenti e suggerimenti aggiuntivi o l'utente è in attesa del completamento. alto in caso di insod..<br/> <strong>Alternative:</strong> Inviare commenti e suggerimenti su richiesta visualizzando un'icona (o modificando un'icona esistente) nell'area di notifica durante l'esecuzione dell'operazione; rimuovere l'icona (o ripristinare l'icona precedente) al termine &quot; &quot; dell'operazione. <br/></td>
</tr>
<tr class="even">
<td><strong>Errore dell'azione</strong><br/> Notifica agli utenti quando un'azione asincrona avviata dall'utente ha esito negativo. <br/></td>
<td><strong>Corretto:</strong><br/> <img src="images/mess-notif-image12.png" alt="Screen shot of notification of failure to install " /><br/> In questo esempio, l'attivazione di Windows notifica agli utenti l'errore.<br/> <strong>Non corretto:</strong><br/> <img src="images/mess-notif-image13.png" alt="Screen shot of notification of failure to update " /><br/> In questo esempio, Microsoft Outlook ha usato per notificare agli utenti un errore di cui è improbabile che si occupino.<br/> <strong>Mostra quando:</strong> In caso di errore di un'attività asincrona.<br/> <strong>Mostra la frequenza con cui:</strong> una volta.<br/> <strong>Fattore di infastidimento:</strong> Basso se utile e pertinente; alto se il problema si risolve immediatamente o gli utenti in caso contrario non si preoccupano.<br/> <strong>Alternative:</strong> Utilizzare una finestra di dialogo modale se gli utenti devono risolvere immediatamente l'errore. <br/></td>
</tr>
<tr class="odd">
<td><strong>Evento di sistema non critico</strong><br/> Notifica agli utenti eventi di sistema significativi o stato che possono essere ignorati in modo sicuro, almeno temporaneamente. <br/></td>
<td><img src="images/mess-notif-image8.png" alt="Screen shot of notification of low battery power " /><br/> In questo esempio, Windows avvisa gli utenti dell'alimentazione a batteria insufficiente, ma c'è ancora molto tempo prima di intervenire.<br/> <strong>Mostra quando:</strong> Quando si verifica un evento e l'utente è attivo o una condizione continua a esistere. Se si verifica un problema, rimuovere le notifiche attualmente visualizzate immediatamente dopo la risoluzione del problema. Come per le notifiche di azione, notificare agli utenti gli eventi di sistema riusciti solo se è probabile che gli utenti siano in attesa dell'evento o dopo errori recenti.<br/> <strong>Mostra la frequenza con cui:</strong> Una volta quando si verifica l'evento per la prima volta. Se questo è il risultato di un problema che gli utenti devono risolvere, visualizzarlo di nuovo una volta al giorno.<br/> <strong>Fattore di infastidimento:</strong> Basso, purché la notifica non sia visualizzata troppo spesso.<br/> <strong>Alternative:</strong> Se gli utenti devono risolvere un problema, usare l'escalation progressiva visualizzando infine una finestra di dialogo modale quando la risoluzione diventa obbligatoria. <br/></td>
</tr>
<tr class="even">
<td><strong>Attività utente facoltativa</strong><br/> Notifica agli utenti le attività asincrone che devono eseguire. Facoltativa o obbligatoria, l'attività può essere posticipata in modo sicuro. <br/></td>
<td><img src="images/mess-notif-image14.png" alt="Screen shot of notification of available updates " /><br/> In questo esempio, Windows Update notifica agli utenti di un nuovo aggiornamento della sicurezza.<br/> <strong>Mostra quando:</strong> Quando viene determinata la necessità di eseguire un'attività e l'utente è attivo.<br/> <strong>Mostra la frequenza con cui:</strong> Una volta al giorno per un massimo di tre volte.<br/> <strong>Fattore di infastidimento:</strong> Basso, purché gli utenti considerino importante l'attività e la notifica non viene visualizzata troppo spesso.<br/> <strong>Alternative:</strong> Se gli utenti devono eseguire l'attività, usare l'escalation progressiva visualizzando infine una finestra di dialogo modale quando l'attività diventa obbligatoria. <br/></td>
</tr>
<tr class="odd">
<td><strong>Fyi</strong><br/> Notifica agli utenti informazioni potenzialmente utili e rilevanti. È possibile notificare agli utenti informazioni di rilevanza marginale se sono facoltative e gli utenti acconsentino esplicitamente. <br/></td>
<td><strong>Corretto:</strong><br/> <img src="images/mess-notif-image15.png" alt="Screen shot of notification of new e-mail message " /><br/> In questo esempio, agli utenti viene inviata una notifica quando viene ricevuto un nuovo messaggio di posta elettronica.<br/> <strong>Corretto:</strong><br/> <img src="images/mess-notif-image16.png" alt="Screen shot of notification of contact signed in " /><br/> In questo esempio gli utenti ricevono una notifica quando i contatti vengono online e scelgono di ricevere queste informazioni facoltative.<br/> <strong>Non corretto:</strong><br/> <img src="images/mess-notif-image17.png" alt="Screen shot of notification for faster performance " /><br/> In questo esempio le informazioni sono utili solo se l'utente ha già installato porte USB ad alta velocità. In caso contrario, è probabile che l'utente non esererà un'operazione diversa come risultato.<br/> <strong>Mostra quando:</strong> Quando si verifica l'evento di attivazione.<br/> <strong>Mostra come:</strong> Usare l'opzione in tempo reale in modo che queste notifiche non siano in coda quando gli utenti eseguono un'applicazione a schermo intero o non usano attivamente il computer.<br/> <strong>Mostra la frequenza con cui:</strong> una volta.<br/> <strong>Fattore di infastidimento:</strong> Medio-alto, a seconda della percezione dell'utilità e della pertinenza degli utenti. Non consigliato se è presente una bassa probabilità di interesse dell'utente.<br/> <strong>Alternative:</strong> Non inviare notifiche agli utenti. <br/></td>
</tr>
<tr class="even">
<td><strong>Annuncio di funzionalità</strong><br/> Notifica agli utenti le funzionalità del sistema o dell'applicazione appena installate, non utilizzate.<br/></td>
<td><strong>Non usare le notifiche per gli annunci di funzionalità.</strong> Usare invece un altro modo per rendere individuabile la funzionalità, ad esempio: <br/>
<ul>
<li>Progettare la funzionalità in modo che sia più facile da individuare nei contesti in cui è necessaria.</li>
<li>Non fare nulla di speciale e consentire agli utenti di scoprire la funzionalità da soli.</li>
</ul>
<strong>Non corretto:</strong><br/> <img src="images/mess-notif-image4.png" alt="Screen shot of notification of new features " /><br/> Non usare le notifiche per gli annunci di funzionalità.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Selezionare il modello di notifica in base al relativo utilizzo.** Per una descrizione di ogni modello di utilizzo, vedere la tabella precedente.
-   **Non usare notifiche durante l'esperienza iniziale di Windows.** Per migliorare la prima esperienza, Windows 7 elimina tutte le notifiche visualizzate durante le prime ore di utilizzo. Progettare il programma presupponendo che gli utenti non vedano tali notifiche.

### <a name="what-to-notify"></a>Cosa inviare una notifica

-   **Non notificare operazioni riuscite, ad eccezione delle circostanze seguenti:**
    -   **Sicurezza.** Gli utenti considerano le operazioni di sicurezza di massima importanza, quindi notificare agli utenti le operazioni di sicurezza riuscite.
    -   **Errore recente.** Gli utenti non accettano operazioni riuscite per scontate se hanno avuto esito negativo immediatamente prima, quindi notificare agli utenti l'esito positivo quando l'operazione ha avuto esito negativo di recente.
    -   **Evitare disagi.** Se si segnalano operazioni riuscite, è possibile evitare l'incoerenza degli utenti. Di conseguenza, inviare una notifica agli utenti quando un'operazione viene eseguita in modo imprevisto, ad esempio quando un'operazione è lunga o viene completata prima o dopo il previsto.
-   **In altre circostanze, non inviare commenti e suggerimenti per il successo o inviare commenti e suggerimenti "su richiesta".** Si supponga che gli utenti prendano per scontate le operazioni riuscite. È possibile inviare commenti e suggerimenti su richiesta visualizzando un'icona (o modificando un'icona esistente) nell'area di notifica durante l'esecuzione dell'operazione e rimuovendo l'icona (o ripristinando l'icona precedente) al termine dell'operazione.
-   Per il modello FYI, non inviare una notifica se gli utenti possono continuare a lavorare normalmente o se è improbabile che esercitino operazioni diverse in seguito **alla notifica.**

    **Non corretto:**

    ![Screenshot della notifica per migliorare le prestazioni ](images/mess-notif-image17.png)

    In questo esempio le informazioni sono utili solo se l'utente ha già installato le porte. In caso contrario, è probabile che l'utente non esersi in alcun modo diverso come risultato.

    -   Eccezione: è possibile notificare agli utenti informazioni di dubbia rilevanza se sono facoltative e gli **utenti acconsentino esplicitamente.**

        **Corretto:**

        ![Screenshot della notifica del contatto connesso ](images/mess-notif-image16.png)

        In questo esempio, gli utenti ricevono una notifica quando i contatti tornano online e scelgono di ricevere queste informazioni facoltative.

-   Per gli eventi di sistema non critici e i modelli FYI, **usare le notifiche complete per un singolo evento.** Non presenta più file parziali.

    **Non corretto:**

    ![Screenshot delle notifiche "Trovato nuovo hardware" ](images/mess-notif-image18.png)

    Questi esempi mostrano solo quattro delle otto notifiche visualizzate da Windows XP quando un utente collega una tastiera USB specifica, ognuna delle quali presenta in modo incrementale altre informazioni.

    **Corretto:**

    ![Screenshot delle notifiche sullo stato dell'installazione ](images/mess-notif-image19.png)

    In questo esempio, il collegamento di una tastiera USB comporta due notifiche complete.

### <a name="when-to-notify"></a>Quando inviare una notifica

-   **Visualizzare una notifica in base al relativo schema progettuale:**



| Modello              | Quando inviare una notifica          |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azione riuscita<br/>            | Al completamento di un'attività asincrona. Notificare agli utenti le azioni riuscite solo se è probabile che siano in attesa del completamento o dopo errori recenti.<br/>                                             |
| Azione non riuscita<br/>            | In caso di errore di un'attività asincrona.<br/>                                                                                                                                                                   |
| Evento di sistema non critico<br/> | Quando si verifica un evento e l'utente è attivo o la condizione continua a esistere. Se si verifica un problema, rimuovere immediatamente la notifica attualmente visualizzata dopo aver risolto il problema.<br/> |
| Attività utente facoltativa<br/>        | Quando viene determinata la necessità di eseguire un'attività e l'utente è attivo.<br/>                                                                                                                                   |
| Fyi<br/>                       | Quando si verifica l'evento di attivazione.<br/>                                                                                                                                                                       |



 

-   Per il modello di errore dell'azione, se il problema potrebbe correggersi entro pochi **secondi, ritardare** la notifica di errore per un periodo di tempo appropriato. Se il problema si corregge, non segnalare nulla. Notificare solo dopo che è passato un tempo sufficiente per segnalare che l'errore è evidente. Se si segnala troppo presto, molto probabilmente gli utenti non noteranno il problema segnalato, ma noteranno la notifica non necessaria.

**Non corretto:**

![Screenshot di nessuna notifica di connessione di rete ](images/mess-notif-image20.png)

Quando immediatamente seguito da:

![Screenshot della notifica di connessione riuscita ](images/mess-notif-image21.png)

In questo esempio, in Windows Vista la notifica di nessuna connettività wireless è prematura perché viene spesso seguita immediatamente da una notifica di una buona connettività.

-   Per l'azione riuscita e  i modelli FYI, usare l'opzione in tempo reale in modo che le notifiche non datate non siano accodati quando gli utenti eseguono un'applicazione a schermo intero o non usano attivamente il computer.
-   Per il modello di eventi di sistema non critico, non creare il rischio di tempeste di notifica sfalsando gli eventi associati a eventi noti, ad esempio **l'accesso utente.** Associare invece l'evento a un periodo di tempo successivo all'evento. Ad esempio, è possibile ricordare agli utenti di registrare il prodotto cinque minuti dopo l'accesso dell'utente.

### <a name="how-long-to-notify"></a>Per quanto tempo inviare una notifica

In Windows Vista e versioni successive le notifiche vengono visualizzate per una durata fissa di 9 secondi.

### <a name="how-often-to-notify"></a>Frequenza di notifica

-   **Il numero di volte in cui visualizzare una notifica è basato sul relativo schema progettuale:**



| Modello           | Frequenza di notifica  |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Azione riuscita<br/>            | Singola occorrenza.<br/>                                                                                                            |
| Azione non riuscita<br/>            | Singola occorrenza.<br/>                                                                                                            |
| Evento di sistema non critico<br/> | Una volta quando si verifica l'evento per la prima volta. Se ciò è il risultato di un problema che gli utenti devono risolvere, visualizzarlo di nuovo una volta al giorno.<br/> |
| Attività utente facoltativa<br/>        | Una volta al giorno per un massimo di tre volte.<br/>                                                                         |
| Fyi<br/>                       | Singola occorrenza.<br/>                                                                                                            |



 

-   **Per le attività utente facoltative, non tentare di eseguire l'invio degli utenti visualizzando costantemente le notifiche.** Se l'attività è necessaria, visualizzare immediatamente una finestra di dialogo modale anziché usare le notifiche.

### <a name="notification-escalation"></a>Escalation delle notifiche

-   **Non presupporre che gli utenti vedano le notifiche.** Gli utenti non li visualizzano quando:
    -   Sono immersi nel proprio lavoro.
    -   Non prestano attenzione.
    -   Sono lontano dal computer.
    -   Eseguono un'applicazione a schermo intero.
    -   L'amministratore ha disattivato tutte le notifiche per il computer.
-   **Se gli utenti devono eseguire un'azione, usare l'escalation progressiva** per visualizzare un'interfaccia utente alternativa che gli utenti non possono ignorare.

### <a name="interaction"></a>Interazione

-   **Rendere le notifiche selezionabili quando:**
    -   **Gli utenti devono eseguire un'azione.** Facendo clic sulla notifica verrà visualizzata una finestra in cui gli utenti possono eseguire l'azione. Questo approccio è preferibile per l'errore dell'azione e per i modelli di progettazione facoltativi delle attività utente.
    -   **Gli utenti potrebbero voler visualizzare altre informazioni.** Facendo clic sulla notifica verrà visualizzata una finestra in cui gli utenti possono visualizzare informazioni aggiuntive.
-   **Visualizza sempre una finestra quando gli utenti fa clic per eseguire un'azione.** Non fare clic su Esegui un'azione direttamente.
-   **Se si fa clic per visualizzare altre informazioni, vengono sempre visualizzate altre informazioni.** Non riformizza semplicemente le informazioni già presenti nella notifica.

### <a name="icons"></a>Icone

-   **Per il modello di errore azione, usare l'icona di errore standard.**
-   **Per i modelli di eventi di sistema non critici, usare l'icona di avviso standard.**
-   **Per altri modelli, usare icone che** mostrano gli oggetti correlati all'oggetto o suggeriscono l'oggetto , ad esempio uno schermo per la sicurezza o una batteria per l'alimentazione.
-   **Usare le icone in base alla personalizzazione dell'applicazione o dell'azienda se gli utenti di destinazione le riconosceranno e non esiste un'alternativa migliore.**
-   Per l'escalation progressiva, prendere in considerazione l'uso di icone con un aspetto progressivamente più **enfatico quando la situazione diventa più urgente.**
-   **Non usare l'icona delle informazioni standard.** Che le notifiche siano informazioni senza dire.
-   **È consigliabile usare icone grandi (32x32 pixel) quando:**
    -   Gli utenti comprenderanno rapidamente l'icona anziché il testo.
    -   Le icone grandi comunicano il significato in modo più chiaro ed efficace rispetto alle icone standard da 16x16 pixel.
    -   L'icona usa [l'oggetto in stile Aero.](vis-icons.md)

![screenshot della notifica "messaggi importanti" ](images/mess-notif-image22.png)

In questo esempio gli utenti possono comprendere rapidamente la natura della notifica con un'occhiata all'icona grande.

### <a name="notification-queuing"></a>Accodamento notifiche

**Nota:** Le notifiche vengono accodate ogni volta che non possono essere visualizzate immediatamente, ad esempio quando viene visualizzata un'altra notifica, l'utente esegue un'applicazione a schermo intero o l'utente non usa attivamente il computer. Le notifiche in tempo reale rimangono nella coda solo per 60 secondi.

-   **Per i modelli di azione riuscita e FYI,** usare l'opzione in tempo reale in modo che la notifica non sia accodata per molto tempo. Queste notifiche hanno valore solo quando possono essere visualizzate immediatamente.
-   **Rimuovere le notifiche in coda quando non sono più rilevanti.**
-   **Sviluppatori:** A tale scopo, impostare il flag NIF \_ INFO in uFlags e impostare szInfo su una stringa vuota. Questa operazione non ha alcun problema se la notifica non è più in coda.

### <a name="system-integration"></a>Integrazione del sistema

-   Se l'applicazione non ha sempre un'icona [nell'area](winenv-notification.md) di notifica quando è in esecuzione, visualizzare temporaneamente un'icona durante l'attività asincrona o l'evento che ha causato **la notifica.**

## <a name="text"></a>Testo

### <a name="title-text"></a>Testo titolo

-   **Usare il testo del titolo che riepiloga brevemente le informazioni più importanti necessarie per comunicare agli utenti in una lingua chiara, semplice, concisa e specifica.** Gli utenti devono essere in grado di comprendere lo scopo delle informazioni di notifica in modo rapido e con il minimo sforzo.
-   **Usare frammenti di testo o frasi complete senza terminare la punteggiatura.**
-   **Usare le maiuscole/minuscole come nelle frasi comuni.**
-   **Usare non più di 48 caratteri (in inglese) per supportare la localizzazione.** Il titolo ha una lunghezza massima di 63 caratteri, ma è necessario consentire l'espansione del 30% quando viene tradotto il testo in lingua inglese.

### <a name="body-text"></a>Testo del corpo

-   **Usare il testo del corpo che fornisce una descrizione (senza ripetere le informazioni nel titolo) e, facoltativamente, che fornisce dettagli specifici sulla notifica e consente inoltre agli utenti di sapere quale azione è disponibile.**
-   **Usare frasi complete con punteggiatura finale.**
-   **Usare le maiuscole/minuscole come nelle frasi comuni.**
-   **Usare non più di 200 caratteri (in inglese) per supportare la localizzazione.** Il testo del corpo ha una lunghezza massima di 255 caratteri, ma è necessario consentire l'espansione del 30% quando viene tradotto il testo in lingua inglese.
-   **Includere informazioni essenziali nel testo del corpo, ad esempio nomi di oggetti specifici.** Esempi: nomi utente, nomi di file o URL. Gli utenti non devono aprire un'altra finestra per trovare tali informazioni.
-   **Inserire le virgolette doppie per i nomi degli oggetti.**
    -   **Eccezione:** Non usare le virgolette quando:
        -   Il nome dell'oggetto usa [sempre l'uso di maiuscole e minuscole](glossary.md)in stile titolo, ad esempio con i nomi utente.
        -   Il nome dell'oggetto è offset con due punti (ad esempio: Nome stampante: Stampante).
        -   Il nome dell'oggetto può essere determinato facilmente dal contesto.
-   **Se è necessario troncare i nomi degli oggetti a una dimensione massima fissa per supportare la localizzazione, usare i puntini di sospensione per indicare il troncamento.**

    ![Screenshot del messaggio contenente il nome abbreviato ](images/mess-notif-image23.png)

    In questo esempio il nome di un oggetto viene troncato usando i puntini di sospensione.

-   **Usare la formulazione seguente se la notifica è fattibile:**
    -   Se gli utenti possono fare clic sulla notifica per eseguire un'azione:

        < breve descrizione delle informazioni essenziali>

        <optional details>

        Fare clic su <do something> .

        ![Screenshot del messaggio: "Fare clic per visualizzare lo stato di avanzamento" ](images/mess-notif-image24.png)

        In questo esempio gli utenti possono fare clic per eseguire un'azione.

    -   Se gli utenti possono fare clic sulla notifica per visualizzare altre informazioni:

        < breve descrizione delle informazioni essenziali>

        <optional details>

        Fare clic per altre informazioni.

        ![Screenshot del messaggio: fare clic per altre informazioni ](images/mess-notif-image25.png)

        In questo esempio gli utenti possono fare clic su per altre informazioni.

-   **Non dire che l'utente deve eseguire un'azione in una notifica.** Le notifiche sono relative a informazioni non critiche che gli utenti possono ignorare liberamente. Se gli utenti devono effettivamente eseguire un'azione, non usare le notifiche.
-   **Se gli utenti devono eseguire un'azione, chiarire l'importanza.**
-   Per i modelli di evento di sistema non critici e di errore dell'azione, **descrivere i problemi in linguaggio normale.**

    **Non corretto:**

    ![Screenshot di un messaggio lungo e complesso ](images/mess-notif-image26.png)

    In questo esempio il problema viene descritto usando un linguaggio troppo tecnico, ma non specifico.

    **Corretto:**

    ![screenshot del messaggio chiaro e conciso ](images/mess-notif-image27.png)

    In questo esempio il problema è descritto in linguaggio normale.

-   **Descrivere l'evento in modo rilevante per gli utenti di destinazione.** Una notifica è pertinente se esiste una ragionevole probabilità che gli utenti eserneranno un'attività o modificheranno il comportamento come risultato della notifica. Spesso è possibile eseguire questa operazione descrivendo le notifiche in termini di obiettivi dell'utente anziché problemi tecnologici.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle notifiche:

-   Usare il testo esatto del titolo, inclusa la relativa maiuscola.
-   Fare riferimento al componente come una notifica, non come un balloon o un avviso.
-   Per descrivere l'interazione dell'utente, usare click.
-   Quando possibile, formattare il testo del titolo usando il testo in grassetto. In caso contrario, inserire il titolo tra virgolette solo se necessario per evitare confusione.

Esempio: quando viene visualizzata **la notifica Aggiornamenti critici pronti per l'installazione,** fare clic sulla notifica per avviare il processo.

Quando si fa riferimento all'area di notifica:

-   Fare riferimento all'area di notifica come area di notifica, non come area di notifica.

 

