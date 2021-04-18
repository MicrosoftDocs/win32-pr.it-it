---
title: Notifiche (nozioni di base sulla progettazione)
description: Una notifica informa gli utenti degli eventi che non sono correlati all'attività dell'utente corrente, visualizzando brevemente un fumetto da un'icona nell'area di notifica.
ms.assetid: dcac2fb7-e503-4ea3-a2c5-e3cb660c040a
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5de312b33a970245d2f6f410e55a891c286d9aa7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104565204"
---
# <a name="notifications-design-basics"></a>Notifiche (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Una notifica informa gli utenti degli eventi che non sono correlati all'attività dell'utente corrente, visualizzando brevemente un fumetto da un'icona nell'area di notifica. La notifica potrebbe essere dovuta a un'azione dell'utente o a un evento di sistema significativo oppure potrebbe offrire informazioni potenzialmente utili da Microsoft Windows o da un'applicazione.

Le informazioni contenute in una notifica sono **utili e rilevanti, ma mai critiche.** Di conseguenza, le notifiche non richiedono azioni immediate da parte dell'utente e gli utenti possono ignorarle liberamente.

![screenshot del fumetto con ' nuovi aggiornamenti ' nel titolo ](images/mess-notif-image1.png)

Una notifica tipica.

In Windows Vista e versioni successive, le notifiche vengono visualizzate per una durata fissa di 9 secondi. Le notifiche non vengono visualizzate immediatamente quando gli utenti sono inattivi o gli screen saver sono in esecuzione. Windows accoda automaticamente le notifiche durante questi periodi e visualizza le notifiche in coda quando l'utente riprende le attività regolari. Di conseguenza, non è necessario eseguire alcuna operazione per gestire queste circostanze particolari.

**Sviluppatori:** È possibile determinare quando l'utente è attivo tramite l'API SHQueryUserNotificationState.

**Nota:** Le linee guida relative all' [area di notifica](winenv-notification.md), alla [barra delle applicazioni](winenv-taskbar.md)e ai [palloncini](ctrl-balloons.md) vengono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendi in considerazione queste domande:

-   **Le informazioni sono il risultato immediato e diretto dell'interazione degli utenti con l'applicazione?** In tal caso, visualizzare le informazioni sincrone direttamente all'interno dell'applicazione usando una finestra di [dialogo](win-dialog-box.md), una [finestra di messaggio](glossary.md), un [fumetto](ctrl-balloons.md)o un'interfaccia utente [sul posto](glossary.md) . Le notifiche sono solo per informazioni asincrone.

![screenshot dell'avviso di sicurezza di Windows ](images/mess-notif-image2.png)

In questo esempio la finestra di dialogo Windows Firewall eccezioni viene visualizzata come risultato diretto dell'interazione dell'utente. Una notifica non è appropriata.

-   **Le informazioni sono rilevanti solo quando gli utenti usano attivamente l'applicazione?** In tal caso, visualizzare le informazioni nella barra di [stato](ctrl-status-bars.md) dell'applicazione o in un'altra area di stato.

![screenshot della barra di stato di Outlook ](images/mess-notif-image3.png)

In questo esempio Outlook Visualizza la connessione e lo stato di sincronizzazione sulla barra di stato.

-   **Le informazioni cambiano rapidamente, continuamente e in tempo reale?** Gli esempi includono lo stato di avanzamento dell'elaborazione, le quote azionarie e i punteggi sportivi. In tal caso, non usare le notifiche perché non sono adatte alle informazioni che cambiano rapidamente.
-   **Le informazioni sono utili e pertinenti? È probabile che gli utenti modifichino il proprio comportamento o evitino inconvenienti come il risultato della ricezione delle informazioni?** In caso contrario, non visualizzare le informazioni o inserirle in una finestra di stato o in un file di log.
-   **Le informazioni sono critiche? È richiesta un'azione immediata?** In tal caso, visualizzare le informazioni utilizzando un'interfaccia che richiede attenzione e non può essere facilmente ignorata, ad esempio una finestra di dialogo modale o una finestra di messaggio. Se il programma non è attivo, è possibile attirare l'attenzione sulle informazioni critiche [lampeggiando il pulsante della barra delle applicazioni del programma](winenv-taskbar.md) tre volte e lasciandolo evidenziato finché il programma non è attivo.
-   **Gli utenti di destinazione primari sono professionisti IT?** In tal caso, utilizzare un meccanismo di feedback alternativo, ad esempio voci di [file di log](glossary.md) o messaggi di posta elettronica. I professionisti IT preferiscono fortemente i file di log per le informazioni non critiche. Inoltre, i server vengono spesso gestiti in remoto e in genere eseguiti senza che gli utenti accedano, rendendo le notifiche inefficaci.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Le notifiche valide che favoriscono un'esperienza utente ottimale sono:

-   **Asincrona.** L'evento non è un risultato immediato e diretto dell'interazione corrente degli utenti con Microsoft Windows o con l'applicazione.
-   **Utile.** Esiste una ragionevole probabilità che gli utenti eseguano un'attività o ne modifichino il comportamento come risultato della notifica.
-   **Rilevanti.** La notifica Visualizza informazioni utili a cui gli utenti sono interessati e che non conoscono già.
-   **Non critico.** Le notifiche non sono modali e non richiedono l'interazione dell'utente, in modo che gli utenti possano ignorarle liberamente.
-   **Utilità pratica.** Per le notifiche che suggeriscono l'esecuzione di un'azione, l'azione viene avviata facendo clic sulla notifica. Tuttavia, l'azione può essere sempre posticipata.
-   **Visualizzato in modo appropriato.** La presentazione della notifica (durata, frequenza, testo, icona e interattività) corrisponde alle relative circostanze.
-   **Non fastidioso.** Esiste una linea sottile che consente di informare delicatamente gli utenti di un evento e di infastidirli.

Sfortunatamente, sono presenti troppe notifiche fastidiose, non appropriate, inutili e irrilevanti. Prendere in considerazione queste notifiche da Windows XP Hall of Sham:

![screenshot della notifica di "Tour Windows XP" ](images/mess-notif-image4.png)

![screenshot della notifica ' icone inutilizzate ' ](images/mess-notif-image5.png)

![screenshot della notifica ' Aggiungi Passport .NET ' ](images/mess-notif-image6.png)

In questi esempi, Windows XP tenta di assistere gli utenti nella configurazione iniziale. Tuttavia, queste notifiche si presentano molto spesso e ben dopo che sono utili, quindi sono poco più che annunci di funzionalità non richieste.

## <a name="user-flow-must-be-maintained"></a>Il flusso utente deve essere mantenuto

**Idealmente, gli utenti immersi nel lavoro non vedranno alcuna notifica. Ma vedranno le notifiche solo quando il flusso è già danneggiato.**

In Flow: la psicologia dell'esperienza ottimale, Mihaly Csikszentmihalyi dice che gli utenti entrano in uno stato di flusso quando sono completamente assorbiti nell'attività durante le quali perdono il proprio senso di tempo e hanno sentimenti di grande soddisfazione.

**Le notifiche valide consentono agli utenti di gestire il proprio flusso presentando informazioni utili e rilevanti che possono essere facilmente ignorate.** Le notifiche vengono presentate in modalità a chiave ridotta e non richiedono interazioni.

Non presupporre che se le notifiche non sono [modali](glossary.md) , non possono essere un'interruzione fastidiosa. Le notifiche non richiedono l'attenzione degli utenti, ma certamente la richiedono. È possibile interrompere il flusso degli utenti:

-   Visualizzazione di notifiche a cui gli utenti non sono interessati.
-   Visualizzazione di una notifica troppo spesso.
-   Utilizzo di diverse notifiche quando è sufficiente una singola notifica.
-   Uso del suono quando si visualizza una notifica.

In Windows 7, gli utenti hanno il controllo massimo sulle notifiche. **Se gli utenti scoprono che le notifiche di un programma sono troppo noiose, possono scegliere di escludere tutte le notifiche dal programma.** Assicurarsi che gli utenti non eseguano questa operazione al programma presentando informazioni utili e rilevanti e seguendo queste linee guida.

## <a name="notifications-must-be-ignorable"></a>Le notifiche devono essere ignorabili

**Le notifiche non richiedono azioni immediate da parte dell'utente e gli utenti possono ignorarle liberamente.**

Gli sviluppatori e i progettisti spesso vogliono presentare le notifiche in modo che gli utenti non possano ignorare. Questo obiettivo è completamente subminato al principale vantaggio delle notifiche perché potrebbe interrompere il flusso degli utenti. Se gli utenti vengono distratti dalle notifiche o si ritiene che siano obbligati a leggerli, la progettazione delle notifiche non è riuscita.

**Se si è preoccupati che gli utenti ignorino le notifiche, tenere presente quanto segue:**

-   Se si usano correttamente le notifiche e non richiedono un'azione immediata da parte dell'utente, gli utenti scelgono di ignorarli è da progettazione. Non modificare questa operazione.
-   Se l'evento richiede un'azione immediata da parte dell'utente, utilizzare un'interfaccia utente (UI) alternativa che non può essere ignorata dagli utenti. Vedere si tratta dell'interfaccia utente corretta? per le alternative.

## <a name="use-progressive-escalation-where-applicable"></a>USA escalation progressiva laddove applicabile

Se viene usata una notifica per un evento che gli utenti possono ignorare in modo sicuro, ma che devono essere risolti in un momento qualsiasi, è consigliabile usare un'interfaccia utente alternativa quando la situazione diventa fondamentale. Questa tecnica è nota come escalation progressiva.

Ad esempio, il sistema di risparmio energia di Windows inizialmente indica una batteria insufficiente modificando semplicemente l'icona dell'area di notifica.

![Screenshot di sei icone che mostrano lo stato della batteria ](images/mess-notif-image7.png)

In questi esempi, il risparmio energia di Windows usa l'icona dell'area di notifica per informare gli utenti di una potenza di batteria progressivamente inferiore.

Con la riduzione della potenza della batteria, Windows avvisa gli utenti di una batteria debole con una notifica.

![screenshot della notifica dell'alimentazione a batteria insufficiente](images/mess-notif-image8.png)

In questo esempio, il risparmio energia di Windows usa una notifica per informare gli utenti che la loro alimentazione della batteria è debole.

Questa notifica viene visualizzata quando gli utenti hanno ancora diverse opzioni. Gli utenti possono collegarsi, modificare le opzioni di risparmio energia, eseguire il wrapping del lavoro e arrestare il computer oppure ignorare la notifica e continuare a lavorare. Quando l'alimentazione della batteria continua a esaurirsi, il testo e l'icona della notifica riflettono l'urgenza aggiuntiva. Tuttavia, quando l'alimentazione della batteria diventa talmente bassa da consentire agli utenti di agire immediatamente, il risparmio energia di Windows notifica agli utenti l'uso di una finestra di messaggio [modale](glossary.md) .

![cattura di schermata di un avviso gravemente basso a batteria](images/mess-notif-image9.png)

In questo esempio, il risparmio energia di Windows usa una finestra di messaggio modale per notificare agli utenti una potenza di batteria insufficiente.

**Se si eseguono solo tre operazioni...**

1.  Usare le notifiche solo se è effettivamente necessario. Quando si visualizza una notifica, si sta potenzialmente interrompendo gli utenti o addirittura fastidioso. Verificare che l'interruzione sia giustificata.
2.  Usare le notifiche per eventi o situazioni non critiche che non richiedono un'azione immediata dell'utente. Per gli eventi critici o le situazioni che richiedono un'azione immediata dell'utente, usare un'interfaccia utente alternativa, ad esempio una finestra di dialogo modale.
3.  Se si usano le notifiche, renderlo un'esperienza utente ottimale. Non provare a forzare gli utenti a visualizzare le notifiche. Se gli utenti sono immersi nel lavoro che non visualizzano le notifiche, la progettazione è corretta.

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
<td><strong>Corretto:</strong><br/> <img src="images/mess-notif-image10.png" alt="Screen shot of balloon showing successful updates " /><br/> In questo esempio Windows Update notifica agli utenti quando il computer è stato aggiornato correttamente.<br/> <strong>Non corretto:</strong><br/> <img src="images/mess-notif-image11.png" alt="Screen shot of balloon showing file check complete " /><br/> In questo esempio Microsoft Outlook invia una notifica agli utenti quando viene completato il controllo di un file di dati. Quali sono gli utenti che dovrebbero fare ora? E perché avvisare gli utenti in caso di completamento corretto?<br/> <strong>Mostra quando:</strong> Al completamento di un'attività asincrona. Notificare agli utenti le azioni riuscite solo se è probabile che siano in attesa del completamento o dopo errori recenti.<br/> <strong>Mostra come:</strong> Usare l'opzione in tempo reale in modo che queste notifiche non siano accodate quando gli utenti eseguono un'applicazione a schermo intero o non usano attivamente il computer.<br/> <strong>Mostra con quale frequenza:</strong> Una volta.<br/> <strong>Fattore di disturbo:</strong> Bassa se il successo non è previsto a causa di errori recenti, il successo si verifica dopo un errore critico o estremamente insolito, quindi l'utente necessita di un ulteriore feedback oppure l'utente è in attesa del completamento. alta in caso contrario.<br/> <strong>Alternative:</strong> Inviare commenti e suggerimenti &quot; su richiesta &quot; visualizzando un'icona (o modificando un'icona esistente) nell'area di notifica durante l'esecuzione dell'operazione. rimuovere l'icona (o ripristinare l'icona precedente) al termine dell'operazione. <br/></td>
</tr>
<tr class="even">
<td><strong>Errore azione</strong><br/> Notifica agli utenti la mancata riuscita di un'azione asincrona avviata dall'utente. <br/></td>
<td><strong>Corretto:</strong><br/> <img src="images/mess-notif-image12.png" alt="Screen shot of notification of failure to install " /><br/> In questo esempio, l'attivazione di Windows notifica agli utenti l'errore.<br/> <strong>Non corretto:</strong><br/> <img src="images/mess-notif-image13.png" alt="Screen shot of notification of failure to update " /><br/> In questo esempio Microsoft Outlook ha utilizzato per notificare agli utenti un errore che è improbabile che siano interessati.<br/> <strong>Mostra quando:</strong> In caso di errore di un'attività asincrona.<br/> <strong>Mostra con quale frequenza:</strong> Una volta.<br/> <strong>Fattore di disturbo:</strong> Bassa se utile e pertinente; alta se il problema si risolve immediatamente o se gli utenti non sono interessati.<br/> <strong>Alternative:</strong> Utilizzare una finestra di dialogo modale se gli utenti devono risolvere immediatamente l'errore. <br/></td>
</tr>
<tr class="odd">
<td><strong>Evento di sistema non critico</strong><br/> Notifica agli utenti uno stato o un evento di sistema significativo che può essere tranquillamente ignorato, almeno temporaneamente. <br/></td>
<td><img src="images/mess-notif-image8.png" alt="Screen shot of notification of low battery power " /><br/> In questo esempio, Windows avvisa gli utenti della bassa potenza della batteria, ma c'è ancora molto tempo prima di intervenire.<br/> <strong>Mostra quando:</strong> Quando si verifica un evento e l'utente è attivo oppure una condizione continua a esistere. Se risulta da un problema, rimuovere le notifiche attualmente visualizzate immediatamente dopo la risoluzione del problema. Come per le notifiche delle azioni, notificare agli utenti gli eventi di sistema riusciti solo se è probabile che gli utenti siano in attesa dell'evento o dopo errori recenti.<br/> <strong>Mostra con quale frequenza:</strong> Una volta quando l'evento si verifica per la prima volta. Se si verifica un problema che gli utenti devono risolvere, visualizzare una volta al giorno.<br/> <strong>Fattore di disturbo:</strong> Bassa, purché la notifica non venga visualizzata troppo spesso.<br/> <strong>Alternative:</strong> Se gli utenti devono risolvere un problema, usare l'escalation progressiva visualizzando una finestra di dialogo modale quando la risoluzione diventa obbligatoria. <br/></td>
</tr>
<tr class="even">
<td><strong>Attività utente facoltativa</strong><br/> Notifica agli utenti le attività asincrone che devono eseguire. Sia facoltativa che obbligatoria, l'attività può essere rimandata in modo sicuro. <br/></td>
<td><img src="images/mess-notif-image14.png" alt="Screen shot of notification of available updates " /><br/> In questo esempio Windows Update informa gli utenti di un nuovo aggiornamento della sicurezza.<br/> <strong>Mostra quando:</strong> Quando la necessità di eseguire un'attività è determinata e l'utente è attivo.<br/> <strong>Mostra con quale frequenza:</strong> Una volta al giorno per un massimo di tre volte.<br/> <strong>Fattore di disturbo:</strong> Bassa, purché gli utenti considerino l'attività importante e la notifica non venga visualizzata troppo spesso.<br/> <strong>Alternative:</strong> Se gli utenti devono infine eseguire l'attività, utilizzare l'escalation progressiva visualizzando una finestra di dialogo modale quando l'attività diventa obbligatoria. <br/></td>
</tr>
<tr class="odd">
<td><strong>FYI</strong><br/> Notifica agli utenti le informazioni rilevanti e potenzialmente utili. È possibile notificare agli utenti le informazioni sulla pertinenza marginale se è facoltativa e se gli utenti scelgono di partecipare. <br/></td>
<td><strong>Corretto:</strong><br/> <img src="images/mess-notif-image15.png" alt="Screen shot of notification of new e-mail message " /><br/> In questo esempio gli utenti ricevono una notifica quando viene ricevuto un nuovo messaggio di posta elettronica.<br/> <strong>Corretto:</strong><br/> <img src="images/mess-notif-image16.png" alt="Screen shot of notification of contact signed in " /><br/> In questo esempio gli utenti ricevono una notifica quando i contatti passano online e scelgono di ricevere queste informazioni facoltative.<br/> <strong>Non corretto:</strong><br/> <img src="images/mess-notif-image17.png" alt="Screen shot of notification for faster performance " /><br/> In questo esempio le informazioni sono utili solo se l'utente ha già installato porte USB ad alta velocità. In caso contrario, l'utente non potrà eseguire alcuna operazione diversa come il risultato.<br/> <strong>Mostra quando:</strong> Quando si verifica l'evento di attivazione.<br/> <strong>Mostra come:</strong> Usare l'opzione in tempo reale in modo che queste notifiche non siano accodate quando gli utenti eseguono un'applicazione a schermo intero o non usano attivamente il computer.<br/> <strong>Mostra con quale frequenza:</strong> Una volta.<br/> <strong>Fattore di disturbo:</strong> Da media ad alta, a seconda della percezione dell'utilità e della pertinenza degli utenti. Non consigliato se è presente una probabilità bassa di interesse dell'utente.<br/> <strong>Alternative:</strong> Non inviare notifiche agli utenti. <br/></td>
</tr>
<tr class="even">
<td><strong>Annuncio funzionalità</strong><br/> Notifica agli utenti le funzionalità del sistema o dell'applicazione appena installate e inutilizzate.<br/></td>
<td><strong>Non usare notifiche per gli annunci di funzionalità.</strong> Usare invece un altro modo per rendere individuabile la funzionalità, ad esempio: <br/>
<ul>
<li>Progettare la funzionalità per semplificare l'individuazione nei contesti in cui è necessario.</li>
<li>Non eseguire alcuna operazione speciale e consentire agli utenti di individuare la funzionalità autonomamente.</li>
</ul>
<strong>Non corretto:</strong><br/> <img src="images/mess-notif-image4.png" alt="Screen shot of notification of new features " /><br/> Non usare notifiche per gli annunci di funzionalità.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Selezionare il modello di notifica in base al relativo utilizzo.** Per una descrizione di ogni modello di utilizzo, vedere la tabella precedente.
-   **Non usare notifiche durante l'esperienza iniziale di Windows.** Per migliorare la prima esperienza, Windows 7 disattiva tutte le notifiche visualizzate durante le prime ore di utilizzo. Progettare il programma presumendo che gli utenti non visualizzino tali notifiche.

### <a name="what-to-notify"></a>Cosa notificare

-   **Non notificare le operazioni riuscite, tranne nei casi seguenti:**
    -   **Sicurezza.** Gli utenti considerano l'importanza più elevata per le operazioni di sicurezza, quindi notificare agli utenti le operazioni di protezione riuscite.
    -   **Errore recente.** Gli utenti non hanno eseguito correttamente le operazioni per la concessione se hanno avuto esito negativo immediatamente prima, quindi avvisare gli utenti del successo quando l'operazione ha avuto esito negativo.
    -   **Impedisci l'inconveniente.** Segnalare le operazioni riuscite quando si esegue questa operazione potrebbe evitare utenti scomodare. Di conseguenza, avvisare gli utenti quando un'operazione riuscita viene eseguita in modo imprevisto, ad esempio quando un'operazione è lunga o viene completata prima o dopo il previsto.
-   **In altre circostanze, non inviare commenti e suggerimenti per l'esito positivo o inviare commenti e suggerimenti "su richiesta".** Si supponga che gli utenti abbiano completato le operazioni per la concessione. È possibile inviare commenti e suggerimenti su richiesta visualizzando un'icona (o modificando un'icona esistente) nell'area di notifica durante l'esecuzione dell'operazione e rimuovendo l'icona (o ripristinando l'icona precedente) al termine dell'operazione.
-   Per il modello FYI, **non concedere una notifica se gli utenti possono continuare a lavorare normalmente o se è improbabile eseguire operazioni diverse come risultato della notifica.**

    **Non corretto:**

    ![screenshot della notifica per ottenere prestazioni più veloci ](images/mess-notif-image17.png)

    In questo esempio le informazioni sono utili solo se l'utente ha già installato le porte. In caso contrario, l'utente non potrà eseguire alcuna operazione diversa come il risultato.

    -   Eccezione: **è possibile notificare agli utenti le informazioni relative alla pertinenza dubbia se sono facoltative e gli utenti scelgono di partecipare.**

        **Corretto:**

        ![screenshot della notifica del contatto connesso ](images/mess-notif-image16.png)

        In questo esempio gli utenti ricevono una notifica quando i contatti passano online e scelgono di ricevere queste informazioni facoltative.

-   Per gli eventi di sistema non critici e i modelli FYI, **usare le notifiche complete per un singolo evento.** Non presentare più parti parziali.

    **Non corretto:**

    ![screenshot delle notifiche ' trovato nuovo hardware ' ](images/mess-notif-image18.png)

    In questi esempi vengono illustrate solo quattro delle otto notifiche visualizzate da Windows XP quando un utente connette una tastiera USB specifica, ciascuna delle quali presenta altre informazioni in modo incrementale.

    **Corretto:**

    ![screenshot delle notifiche dello stato di installazione ](images/mess-notif-image19.png)

    In questo esempio, il collegamento di una tastiera USB comporta due notifiche complete.

### <a name="when-to-notify"></a>Quando inviare una notifica

-   **Visualizza una notifica in base al modello di progettazione:**



|                                      |                                                                                                                                                                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modello**<br/>               | **Quando inviare una notifica**<br/>                                                                                                                                                                                      |
| Azione riuscita<br/>            | Al completamento di un'attività asincrona. Notificare agli utenti le azioni riuscite solo se è probabile che siano in attesa del completamento o dopo errori recenti.<br/>                                             |
| Errore azione<br/>            | In caso di errore di un'attività asincrona.<br/>                                                                                                                                                                   |
| Evento di sistema non critico<br/> | Quando si verifica un evento e l'utente è attivo o la condizione continua a esistere. Se si verifica un problema, rimuovere la notifica attualmente visualizzata immediatamente dopo la risoluzione del problema.<br/> |
| Attività utente facoltativa<br/>        | Quando la necessità di eseguire un'attività è determinata e l'utente è attivo.<br/>                                                                                                                                   |
| FYI<br/>                       | Quando si verifica l'evento di attivazione.<br/>                                                                                                                                                                       |



 

-   Per il modello di errore di azione, **se il problema potrebbe correggersi automaticamente entro pochi secondi, ritardare la notifica di errore per un periodo di tempo appropriato.** Se il problema si risolve, non segnalare alcun problema. Invia una notifica solo dopo che è trascorso un tempo sufficiente a indicare che l'errore è evidente. Se si segnalano troppo presto, la maggior parte degli utenti probabilmente non noterà il problema segnalato, ma si noterà che la notifica non è necessaria.

**Non corretto:**

![screenshot della notifica di nessuna connessione di rete ](images/mess-notif-image20.png)

Quando segue immediatamente:

![cattura di schermata della notifica di connessione riuscita ](images/mess-notif-image21.png)

In questo esempio, in Windows Vista la notifica di nessuna connettività wireless è prematura perché è spesso seguita immediatamente da una notifica di una corretta connettività.

-   Per l'azione riuscita e i modelli FYI, **usare l'opzione in tempo reale in modo che le notifiche non aggiornate non vengano accodate** quando gli utenti eseguono un'applicazione a schermo intero o non usano attivamente il computer.
-   Per il modello di eventi di sistema non critico, **non creare il rischio di Storm di notifica tramite lo scaglionamento degli eventi associati a eventi noti, ad esempio l'accesso dell'utente.** Al contrario, associare l'evento a un determinato periodo di tempo dopo l'evento. È ad esempio possibile ricordare agli utenti di registrare il prodotto cinque minuti dopo l'accesso dell'utente.

### <a name="how-long-to-notify"></a>Durata della notifica

In Windows Vista e versioni successive, le notifiche vengono visualizzate per una durata fissa di 9 secondi.

### <a name="how-often-to-notify"></a>Frequenza di notifica

-   **Il numero di volte in cui visualizzare una notifica si basa sul modello di progettazione:**



|                                      |                                                                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **Modello**<br/>               | **Frequenza di notifica**<br/>                                                                                          |
| Azione riuscita<br/>            | Singola occorrenza.<br/>                                                                                                            |
| Errore azione<br/>            | Singola occorrenza.<br/>                                                                                                            |
| Evento di sistema non critico<br/> | Una volta quando l'evento si verifica per la prima volta. Se si verifica un problema che gli utenti devono risolvere, visualizzare una volta al giorno.<br/> |
| Attività utente facoltativa<br/>        | Una volta al giorno per un massimo di tre volte.<br/>                                                                         |
| FYI<br/>                       | Singola occorrenza.<br/>                                                                                                            |



 

-   **Per le attività utente facoltative, non provare a tormentare gli utenti per l'invio visualizzando costantemente le notifiche.** Se l'attività è obbligatoria, visualizzare immediatamente una finestra di dialogo modale anziché utilizzare le notifiche.

### <a name="notification-escalation"></a>Escalation delle notifiche

-   **Non presupporre che gli utenti visualizzino le notifiche.** Gli utenti non possono visualizzarli quando:
    -   Sono immersi nel lavoro.
    -   Non prestano attenzione.
    -   Sono lontani dal computer.
    -   Eseguono un'applicazione a schermo intero.
    -   L'amministratore ha disattivato tutte le notifiche per il proprio computer.
-   **Se gli utenti devono eseguire un certo tipo di azione, usare l'escalation progressiva** per visualizzare un'interfaccia utente alternativa che gli utenti non possono ignorare.

### <a name="interaction"></a>Interazione

-   **Rendere le notifiche selezionabili quando:**
    -   **Gli utenti devono eseguire un'azione.** Fare clic sulla notifica per visualizzare una finestra in cui gli utenti possono eseguire l'azione. Questo approccio è preferibile per gli errori di azione e i modelli di progettazione di attività utente facoltative.
    -   **È possibile che gli utenti desiderino visualizzare altre informazioni.** Fare clic sulla notifica per visualizzare una finestra in cui gli utenti possono visualizzare informazioni aggiuntive.
-   **Visualizza sempre una finestra quando gli utenti fanno clic per eseguire un'azione.** Non fare clic su Esegui direttamente un'azione.
-   **Se si fa clic per visualizzare altre informazioni, è sempre necessario visualizzare altre informazioni.** Non limitarsi a riformulare le informazioni già presenti nella notifica.

### <a name="icons"></a>Icone

-   **Per il modello di errore dell'azione, usare l'icona di errore standard.**
-   **Per i modelli di eventi di sistema non critici, usare l'icona di avviso standard.**
-   **Per altri modelli, usare le icone che mostrano gli oggetti che riguardano o suggeriscono l'oggetto**, ad esempio uno scudo per la sicurezza o una batteria per l'alimentazione.
-   **Usare le icone in base all'applicazione o alle informazioni personalizzate distintive dell'azienda se gli utenti di destinazione le riconoscono e non esiste un'alternativa migliore.**
-   Per l'escalation progressiva, **provare a usare le icone con un aspetto progressivamente più enfatico, perché la situazione diventa più urgente.**
-   **Non usare l'icona informazioni standard.** Le notifiche sono informative.
-   **Si consiglia di usare icone grandi (32x32 pixel) quando:**
    -   Gli utenti possono comprendere rapidamente l'icona anziché il testo.
    -   Le icone grandi conferiscono il significato in modo più chiaro ed efficace rispetto alle icone di pixel 16x16 standard.
    -   L'icona usa il [tipo Aero](vis-icons.md).

![screenshot della notifica di ' messaggi importanti ' ](images/mess-notif-image22.png)

In questo esempio, gli utenti possono comprendere rapidamente la natura della notifica con un'occhiata all'icona grande.

### <a name="notification-queuing"></a>Accodamento notifiche

**Nota:** Le notifiche vengono accodate ogni volta che non possono essere visualizzate immediatamente, ad esempio quando viene visualizzata un'altra notifica, l'utente esegue un'applicazione a schermo intero oppure l'utente non usa attivamente il computer. Le notifiche in tempo reale rimangono nella coda solo per 60 secondi.

-   **Per l'azione riuscita e i modelli FYI, usare l'opzione in tempo reale** in modo che la notifica non venga accodata per lungo. Queste notifiche hanno valore solo quando possono essere visualizzate immediatamente.
-   **Rimuovere le notifiche in coda quando non sono più rilevanti.**
-   **Sviluppatori:** A tale scopo, è possibile impostare il \_ flag NSE info in uFlags e impostare szInfo su una stringa vuota. Se la notifica non è più presente nella coda, non vi sono problemi.

### <a name="system-integration"></a>Integrazione del sistema

-   Se l'applicazione non ha sempre un'icona nell' [area di notifica](winenv-notification.md) quando viene eseguita, **Visualizza un'icona temporaneamente durante l'attività o l'evento asincrono che ha causato la notifica.**

## <a name="text"></a>Testo

### <a name="title-text"></a>Testo titolo

-   **Usare il testo del titolo che riepiloga brevemente le informazioni più importanti che è necessario comunicare agli utenti in modo chiaro, semplice, conciso e specifico.** Gli utenti dovrebbero essere in grado di comprendere lo scopo delle informazioni di notifica rapidamente e con il minimo sforzo.
-   **Utilizzare frammenti di testo o frasi complete senza punteggiatura finale.**
-   **Usare le maiuscole/minuscole come nelle frasi comuni.**
-   **Per gestire la localizzazione, non usare più di 48 caratteri (in inglese).** Il titolo ha una lunghezza massima di 63 caratteri, ma è necessario consentire il 30% di espansione quando viene convertito il testo in lingua inglese.

### <a name="body-text"></a>Testo corpo

-   **Usare il testo del corpo che fornisce una descrizione (senza ripetere le informazioni nel titolo) e, facoltativamente, che fornisce dettagli specifici sulla notifica e consente inoltre agli utenti di sapere quale azione è disponibile.**
-   **Utilizzare frasi complete con la punteggiatura finale.**
-   **Usare le maiuscole/minuscole come nelle frasi comuni.**
-   **Per gestire la localizzazione, non usare più di 200 caratteri (in inglese).** Il testo del corpo ha una lunghezza massima di 255 caratteri, ma è necessario consentire il 30% di espansione quando viene convertito il testo in lingua inglese.
-   **Includere informazioni essenziali nel testo del corpo, ad esempio nomi di oggetti specifici.** Esempi: nomi utente, nomi file o URL. Gli utenti non devono aprire un'altra finestra per trovare tali informazioni.
-   **Racchiudere tra virgolette doppie i nomi degli oggetti.**
    -   **Eccezione:** Non usare le virgolette quando:
        -   Il nome dell'oggetto usa sempre le [lettere maiuscole in stile titolo](glossary.md), ad esempio con i nomi utente.
        -   Il nome dell'oggetto viene sfalsato con i due punti (ad esempio: nome della stampante: stampante).
        -   Il nome dell'oggetto può essere facilmente determinato dal contesto.
-   **Se è necessario troncare i nomi di oggetto a una dimensione massima fissa per supportare la localizzazione, utilizzare i puntini di sospensione per indicare un troncamento.**

    ![screenshot del messaggio contenente il nome abbreviato ](images/mess-notif-image23.png)

    In questo esempio, il nome di un oggetto viene troncato utilizzando i puntini di sospensione.

-   **Se la notifica è attiva, utilizzare la formulazione seguente:**
    -   Se gli utenti possono fare clic sulla notifica per eseguire un'azione:

        < breve descrizione delle informazioni essenziali>

        <optional details>

        Fare clic su <do something> .

        ![screenshot del messaggio:' fare clic per visualizzare lo stato di avanzamento ' ](images/mess-notif-image24.png)

        In questo esempio, gli utenti possono fare clic per eseguire un'azione.

    -   Se gli utenti possono fare clic sulla notifica per visualizzare altre informazioni:

        < breve descrizione delle informazioni essenziali>

        <optional details>

        Per ulteriori informazioni, fare clic su.

        ![screenshot del messaggio: fare clic per altre informazioni ](images/mess-notif-image25.png)

        In questo esempio, gli utenti possono fare clic per ulteriori informazioni.

-   **Non dire che l'utente "deve" eseguire un'azione in una notifica.** Le notifiche sono destinate a informazioni non critiche che possono essere ignorate liberamente dagli utenti. Se gli utenti devono effettivamente eseguire un'azione, non usare le notifiche.
-   **Se gli utenti devono eseguire un'azione, rendere chiara l'importanza.**
-   Per gli errori di azione e i modelli di eventi di sistema non critici, **descrivere i problemi in linguaggio normale.**

    **Non corretto:**

    ![Screenshot di messaggi lunghi e complessi ](images/mess-notif-image26.png)

    In questo esempio, il problema viene descritto utilizzando un linguaggio eccessivamente tecnico, ma non specifico.

    **Corretto:**

    ![screenshot del messaggio chiaro, conciso ](images/mess-notif-image27.png)

    In questo esempio il problema è descritto in linguaggio normale.

-   **Descrivere l'evento in modo rilevante per gli utenti di destinazione.** Una notifica è pertinente se c'è una ragionevole probabilità che gli utenti eseguano un'attività o ne modifichino il comportamento come risultato della notifica. Questa operazione può essere eseguita spesso con la descrizione delle notifiche in termini di obiettivi utente anziché di problemi tecnologici.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle notifiche:

-   Usare il testo del titolo esatto, inclusa la relativa maiuscola.
-   Fare riferimento al componente come notifica, non come fumetto o avviso.
-   Per descrivere l'interazione dell'utente, utilizzare fare clic su.
-   Quando possibile, formattare il testo del titolo utilizzando il testo in grassetto. In caso contrario, inserire il titolo racchiuso tra virgolette solo se necessario per evitare confusione.

Esempio: quando vengono visualizzati gli **aggiornamenti critici pronti per l'installazione** della notifica, fare clic sulla notifica per avviare il processo.

Quando si fa riferimento all'area di notifica:

-   Fare riferimento all'area di notifica come area di notifica, non alla barra di sistema.

 

