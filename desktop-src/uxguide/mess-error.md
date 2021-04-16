---
title: Messaggi di errore (nozioni di base sulla progettazione)
description: Un messaggio di errore avvisa gli utenti di un problema che si è già verificato.
ms.assetid: b02110e9-985d-4448-9c95-eb958b0059b1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0a8ee17093618dc8a192cfad8ce962f7ed04fc76
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104566410"
---
# <a name="error-messages-design-basics"></a>Messaggi di errore (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Un messaggio di errore avvisa gli utenti di un problema che si è già verificato. Al contrario, un messaggio di avviso avvisa gli utenti di una condizione che potrebbe causare un problema in futuro. I messaggi di errore possono essere presentati usando le finestre di dialogo modali, i messaggi sul posto, le notifiche o le mongolfiere.

![screenshot del messaggio di errore: non è possibile rinominare](images/mess-error-image1.png)

Messaggio di errore modale tipico.

I messaggi di errore effettivi indicano agli utenti che si è verificato un problema, ne spiegano il motivo e forniscono una soluzione in modo che gli utenti possano risolvere il problema. Gli utenti devono eseguire un'azione o modificarne il comportamento come risultato di un messaggio di errore.

I messaggi di errore utili e ben scritti sono fondamentali per un'esperienza utente di qualità. I messaggi di errore scritti in modo non corretto comportano una bassa soddisfazione del prodotto e sono una causa principale di costi di supporto tecnico evitabili. I messaggi di errore non necessari interrompono il flusso degli utenti.

**Nota:** Le linee guida relative alle [finestre di dialogo](win-dialog-box.md), [i messaggi di avviso](mess-warn.md), le [conferme](mess-confirm.md), le [icone standard](vis-std-icons.md), le [notifiche](mess-notif.md)e il [layout](vis-layout.md) vengono presentati in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendi in considerazione queste domande:

- **L'interfaccia utente presenta un problema che si è già verificato?** In caso contrario, il messaggio non è un errore. Se l'utente viene avvisato di una condizione che potrebbe causare un problema in futuro, utilizzare un messaggio di avviso.
- **Il problema può essere impedito senza causare confusione?** In caso affermativo, evitare il problema. Utilizzare, ad esempio, i controlli vincolati a valori validi anziché utilizzare controlli non vincolati che potrebbero richiedere messaggi di errore. Inoltre, disabilitare i controlli quando si fa clic su genera un errore, purché sia ovvio perché il controllo è disabilitato.
- **Il problema può essere corretto automaticamente?** In tal caso, gestire il problema ed escludere il messaggio di errore.
- **È probabile che gli utenti eseguano un'azione o modifichino il proprio comportamento come risultato del messaggio?** In caso contrario, la condizione non giustifica l'interruzione dell'utente, quindi è preferibile eliminarlo.
- **Il problema è rilevante quando gli utenti utilizzano attivamente altri programmi?** In tal caso, provare a visualizzare il problema usando un' [icona dell'area di notifica](winenv-notification.md).
- **Il problema non è correlato all'attività dell'utente corrente, non richiede un'azione immediata da parte dell'utente e può essere ignorato liberamente dagli utenti?** In caso affermativo, usare invece una [notifica di errore di azione](mess-notif.md) .
- **Il problema riguarda lo stato di un'attività in background all'interno di una finestra primaria?** In tal caso, provare a visualizzare il problema usando le [barre di stato](ctrl-status-bars.md).
- **Gli utenti di destinazione primari sono professionisti IT?** In tal caso, prendere in considerazione l'uso di un meccanismo alternativo di feedback, ad esempio voci di [file di log](glossary.md) o avvisi di posta elettronica I professionisti IT preferiscono fortemente i file di log per le informazioni non critiche.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

**Caratteristiche dei messaggi di errore insufficienti**

Non dovrebbe sorprendere che ci siano molti messaggi di errore fastidiosi, non consentiti e scritti in modo non corretto. Poiché i messaggi di errore vengono spesso presentati con le finestre di dialogo modali, interrompono l'attività corrente dell'utente e la richiesta di conferma prima di consentire all'utente di continuare.

Parte del problema consiste nel fatto che esistono molti modi per farlo male. Prendere in considerazione questi esempi dalla hall del messaggio di errore:

**Messaggi di errore non necessari**

**Non corretto:**

![screenshot del messaggio di errore: l'applicazione non è riuscita ](images/mess-error-image2.png)

Questo esempio di Windows XP potrebbe essere il messaggio di errore peggiore. Indica che non è stato possibile avviare un programma perché è in corso l'arresto di Windows. L'utente non è in grado di eseguire questa operazione o desidera eseguire questa operazione (l'utente ha scelto di chiudere Windows, dopo tutto). E visualizzando questo messaggio di errore, Windows impedisce l'arresto.

**Il problema:** Il messaggio di errore è il problema. A parte la mancata esecuzione del messaggio di errore, non è necessario che gli utenti eseguano alcuna operazione.

**Causa principale:** Segnalazione di tutti i casi di errore, indipendentemente dagli obiettivi o dal punto di vista degli utenti.

**Alternativa consigliata:** Non segnalare errori a cui gli utenti non sono interessati.

**Messaggi di errore di "operazione riuscita"**

**Non corretto:**

![screenshot del messaggio di errore: rimozione non riuscita ](images/mess-error-image3.png)

Questo messaggio di errore è risultato dall'utente che sceglie di non riavviare Windows immediatamente dopo la rimozione del programma. La rimozione del programma è stata completata dal punto di vista dell'utente.

**Il problema:** Non ci sono errori dal punto di vista dell'utente. A parte la mancata esecuzione del messaggio di errore, non è necessario che gli utenti eseguano alcuna operazione.

**Causa principale:** L'attività è stata completata correttamente dal punto di vista dell'utente, ma non è riuscita dal punto di vista del programma di disinstallazione.

**Alternativa consigliata:** Non segnalare errori per le condizioni che gli utenti considerano accettabili.

**Messaggi di errore completamente inutili**

**Non corretto:**

![screenshot del messaggio di errore: errore sconosciuto ](images/mess-error-image4.png)

Gli utenti apprenderanno che si è verificato un errore, ma non hanno idea di quale sia l'errore o cosa fare. E No, non è accettabile.

**Il problema:** Il messaggio di errore non fornisce un problema specifico e non è possibile eseguire alcuna operazione da parte degli utenti.

**Causa principale:** Probabilmente il programma ha una gestione degli errori insufficiente.

**Alternativa consigliata:** Progettare una gestione corretta degli errori nel programma.

**Messaggi di errore non comprensibili**

**Non corretto:**

![screenshot del messaggio di errore: backup non completato ](images/mess-error-image5.png)

In questo esempio, l'istruzione problem è chiara, ma la spiegazione supplementare è completamente sconcertante.

**Il problema:** La soluzione o l'istruzione del problema è incomprensibile.

**Causa principale:** Spiegazione del problema dal punto di vista del codice anziché dall'utente.

**Alternativa consigliata:** Scrivere il testo del messaggio di errore che gli utenti di destinazione possono facilmente comprendere. Fornire soluzioni che gli utenti possono effettivamente eseguire. Progettare l'esperienza del messaggio di errore del programma senza che i programmatori compongano messaggi di errore.

**Messaggi di errore che sovracomunicano**

**Non corretto:**

![screenshot del messaggio estremamente dettagliato ](images/mess-error-image6.png)

In questo esempio, il messaggio di errore tenta apparentemente di spiegare ogni passaggio di risoluzione dei problemi.

**Il problema:** Troppe informazioni.

**Causa principale:** Fornire troppi dettagli o provare a spiegare un processo complesso di risoluzione dei problemi in un messaggio di errore.

**Alternativa consigliata:** Evitare i dettagli superflui. Evitare inoltre la risoluzione dei problemi. Se è necessario uno strumento di risoluzione dei problemi, concentrarsi sulle soluzioni più probabili e spiegare il resto tramite il collegamento all'argomento appropriato nella Guida di.

**Messaggi di errore inutilmente rigidi**

**Non corretto:**

![screenshot del messaggio: Impossibile trovare l'oggetto ](images/mess-error-image7.png)

Il programma non è in grado di trovare un oggetto che difficilmente sembra catastrofico. E supponendo che sia catastrofico, perché la risposta è accettabile?

**Il problema:** Il tono del programma è inutilmente duro o drammatico.

**Causa principale:** Il problema è dovuto a un bug che risulta irreversibile dal punto di vista del programma.

**Alternativa consigliata:** Scegliere con attenzione la lingua in base al punto di vista dell'utente.

**Messaggi di errore che incolpano gli utenti**

**Non corretto:**

![screenshot del messaggio: carattere non valido ](images/mess-error-image8.png)

Perché gli utenti hanno l'aspetto di un criminale?

**Il problema:** Il messaggio di errore viene formulato in modo che accusi l'utente di eseguire un errore.

**Causa principale:** Formulazione insensitiva incentrata sul comportamento dell'utente anziché sul problema.

**Alternativa consigliata:** Concentrarsi sul problema, non sull'azione dell'utente che ha causato il problema, usando la voce passiva secondo necessità.

**Messaggi di errore sciocchi**

**Non corretto:**

![screenshot del messaggio: errore nella segnalazione errori ](images/mess-error-image9.png)

In questo esempio, l'istruzione problem è piuttosto ironica e non viene fornita alcuna soluzione.

**Il problema:** Istruzioni di messaggio di errore che sono stupidi o non Sequiter.

**Causa principale:** Creazione di messaggi di errore senza prestare attenzione al contesto.

**Alternativa consigliata:** Consente di creare e rivedere i messaggi di errore da un writer. Considerare il contesto e lo stato dell'utente quando si esaminano gli errori.

**Messaggi di errore del programmatore**

**Non corretto:**

![screenshot del messaggio: Indirizzo violazione di accesso ](images/mess-error-image10.png)

In questo esempio, il messaggio di errore indica che è presente un bug nel programma. Questo messaggio di errore ha un significato solo per il programmatore.

**Il problema:** I messaggi destinati a aiutare gli sviluppatori del programma a individuare i bug vengono lasciati nella versione di rilascio del programma. Questi messaggi di errore non hanno significato o valore per gli utenti.

**Causa principale:** Programmatori che usano l'interfaccia utente normale per creare messaggi a se stessi.

**Alternativa consigliata:** Gli sviluppatori devono compilare tutti questi messaggi in modo condizionale in modo che vengano rimossi automaticamente dalla versione di rilascio di un prodotto. Non sprecare tempo a provare a rendere gli errori di questo tipo comprensibili agli utenti, perché i soli destinatari sono i programmatori.

**Messaggi di errore presentati in modo non corretto**

**Non corretto:**

![screenshot del messaggio: errore imprevisto ](images/mess-error-image11.png)

Questo esempio presenta molti errori comuni di presentazione.

**Il problema:** Il recupero di tutti i dettagli nella presentazione del messaggio di errore non è corretto.

**Causa principale:** Non conosce e applica le linee guida per i messaggi di errore. Impossibile utilizzare writer ed editor per creare ed esaminare i messaggi di errore.

La natura della gestione degli errori è tale che molti di questi errori sono molto facili da realizzare. È preferibile tenere presente che la maggior parte dei messaggi di errore potrebbe essere un candidato per la Hall of Shame.

**Caratteristiche dei messaggi di errore validi**

A differenza dei precedenti esempi non validi, i messaggi di errore validi sono:

- **Un problema.** Indica che si è verificato un problema.
- **Una delle cause.** Spiega il motivo per cui si è verificato il problema.
- **Una soluzione.** Fornisce una soluzione che consente agli utenti di risolvere il problema.

Inoltre, i messaggi di errore validi vengono presentati in modo che:

- **Rilevanti.** Il messaggio presenta un problema a cui gli utenti interessano.
- **Utilità pratica.** Gli utenti devono eseguire un'azione o modificarne il comportamento come risultato del messaggio.
- **Centrato sull'utente.** Il messaggio descrive il problema in termini di azioni o obiettivi dell'utente di destinazione, non in termini di ciò che il codice non è soddisfatto.
- **Breve.** Il messaggio è il più breve possibile, ma non più breve.
- **Deselezionare.** Il messaggio usa il linguaggio normale in modo che gli utenti di destinazione possano comprendere facilmente il problema e la soluzione.
- **Specifico.** Il messaggio descrive il problema usando un linguaggio specifico, assegnando nomi specifici, posizioni e valori degli oggetti necessari.
- **Utile.** Gli utenti non devono essere incolpati o essere in uno stupido.
- **Rari.** Visualizzato raramente. I messaggi di errore visualizzati di frequente sono un segno di progettazione non valida.

Progettando l'esperienza di gestione degli errori in modo da avere queste caratteristiche, è possibile evitare che i messaggi di errore del programma vengano visualizzati nel messaggio di errore Hall of Sham.

**Evitare messaggi di errore non necessari**

Spesso il messaggio di errore migliore non è un messaggio di errore. Molti errori possono essere evitati con una progettazione migliore e spesso sono disponibili alternative migliori ai messaggi di errore. È in genere preferibile evitare un errore rispetto alla segnalazione di un errore.

I messaggi di errore più evidenti da evitare sono quelli che non possono essere praticati. Se gli utenti hanno la possibilità di ignorare il messaggio senza eseguire o modificare nulla, omettere il messaggio di errore.

Alcuni messaggi di errore possono essere eliminati perché non sono problemi dal punto di vista dell'utente. Si supponga, ad esempio, che l'utente abbia tentato di eliminare un file già in fase di eliminazione. Sebbene questo potrebbe essere un caso imprevisto dal punto di vista del codice, gli utenti non considerano questo errore perché viene ottenuto il risultato desiderato.

**Non corretto:**

![screenshot del messaggio: Impossibile eliminare il file ](images/mess-error-image12.png)

Questo messaggio di errore deve essere eliminato perché l'azione ha avuto esito positivo dal punto di vista dell'utente.

Per un altro esempio, si supponga che l'utente annulli esplicitamente un'attività. Per il punto di vista dell'utente, la condizione seguente non è un errore.

**Non corretto:**

![screenshot del messaggio: non è possibile completare il backup ](images/mess-error-image13.png)

Questo messaggio di errore deve essere eliminato anche perché l'azione è riuscita dal punto di vista dell'utente.

Talvolta è possibile eliminare i messaggi di errore concentrandosi sugli obiettivi degli utenti anziché sulla tecnologia. In questo modo, riconsiderare la realtà di un errore. Il problema con gli obiettivi dell'utente o con la capacità del programma di soddisfarli? Se l'azione dell'utente ha senso nel mondo reale, dovrebbe essere utile anche per il software.

Si supponga ad esempio che all'interno di un programma di e-commerce un utente tenti di trovare un prodotto utilizzando la ricerca, ma che la query di ricerca letterale non includa corrispondenze e che il prodotto desiderato non sia disponibile. Tecnicamente, si tratta di un errore, ma anziché fornire un messaggio di errore, il programma potrebbe:

- Continuare a cercare i prodotti che corrispondono maggiormente alla query.
- Se la ricerca ha errori evidenti, consiglia automaticamente una query con correzione.
- Gestisci automaticamente problemi comuni, ad esempio errori di ortografia, ortografie alternative e la pluralità e i casi di verbi non corrispondenti.
- Indica quando il prodotto sarà in magazzino.

Fino a quando la richiesta dell'utente è ragionevole, un programma di e-commerce ben progettato deve restituire risultati ragionevoli e non errori.

Un altro modo per evitare i messaggi di errore consiste nel prevenire i problemi in primo luogo. Per evitare errori, è possibile:

- **Uso di controlli vincolati.** Usare i controlli vincolati a valori validi. I controlli quali elenchi, dispositivi di scorrimento, caselle di controllo, pulsanti di opzione e selezionatori di data e ora sono limitati a valori validi, mentre le caselle di testo spesso non possono richiedere messaggi di errore. È tuttavia possibile vincolare caselle di testo in modo che accettino solo determinati caratteri e accettino un numero massimo di caratteri.
- **Uso di interazioni vincolate.** Per le operazioni di trascinamento, consentire agli utenti di eliminare solo le destinazioni valide.
- **Utilizzo di controlli disabilitati e voci di menu.** Disabilitare i controlli e le voci di menu quando gli utenti possono facilmente dedurre perché il controllo o la voce di menu è disabilitata.
- **Fornire valori predefiniti validi.** È meno probabile che gli utenti immettano gli errori di input se possono accettare i valori predefiniti. Anche se gli utenti decidono di modificare il valore, il valore predefinito consente agli utenti di verificare il formato di input previsto.
- **Operazioni.** È meno probabile che gli utenti commettano errori se le attività non sono necessarie o vengono eseguite automaticamente. In alternativa, se gli utenti comportano piccoli errori ma la loro intenzione è chiara, il problema viene risolto automaticamente. È ad esempio possibile correggere automaticamente i problemi di formattazione minori.

**Invio di messaggi di errore necessari**

In alcuni casi è effettivamente necessario fornire un messaggio di errore. Gli utenti commettono errori, reti e dispositivi smettono di funzionare, gli oggetti non possono essere trovati o modificati, non è possibile completare le attività e i programmi contengono bug. Idealmente, questi problemi si verificano meno spesso, ad esempio, è possibile progettare il software per evitare molti tipi di errori dell'utente, ma non è realistico prevenire tutti questi problemi. Quando si verifica uno di questi problemi, viene restituito un messaggio di errore utile per ottenere rapidamente gli utenti.

Una convinzione comune è che i messaggi di errore sono la peggior esperienza utente e dovrebbero essere evitati a tutti i costi, ma è più preciso dire che la confusione degli utenti è l'esperienza peggiore e dovrebbe essere evitata a tutti i costi. A volte il costo è un messaggio di errore utile.

Considerare i controlli disabilitati. Nella maggior parte dei casi, è ovvio perché un controllo è disabilitato, quindi la disabilitazione del controllo è un ottimo modo per evitare un messaggio di errore. Tuttavia, cosa accade se il motivo per cui un controllo è disabilitato non è ovvio? L'utente non può continuare e non è disponibile alcun feedback per determinare il problema. A questo punto l'utente è bloccato ed è necessario dedurre il problema o ottenere supporto tecnico. In questi casi, è preferibile lasciare il controllo abilitato e fornire invece un messaggio di errore utile.

**Non corretto:**

![screenshot del messaggio: dove salvare il backup? ](images/mess-error-image14.png)

Perché il pulsante Avanti è disabilitato qui? È preferibile lasciarlo abilitato ed evitare confusione da parte degli utenti fornendo un messaggio di errore utile.

Se non si è certi che sia necessario fornire un messaggio di errore, iniziare componendo il messaggio di errore che è possibile assegnare. Se è probabile che gli utenti eseguano un'azione o modifichino il comportamento di conseguenza, fornire il messaggio di errore. Al contrario, se gli utenti hanno la possibilità di ignorare il messaggio senza eseguire o modificare nulla, omettere il messaggio di errore.

**Progettazione per una gestione corretta degli errori**

Sebbene la creazione di un testo del messaggio di errore valido possa risultare complessa, in alcuni casi è impossibile senza il supporto per la gestione degli errori dal programma. Considerare questo messaggio di errore:

**Non corretto:**

![screenshot del messaggio: errore sconosciuto ](images/mess-error-image15.png)

È probabile che il problema sia effettivamente sconosciuto perché manca il supporto per la gestione degli errori del programma.

Sebbene sia possibile che questo sia un messaggio di errore scritto in modo non corretto, è più probabile che la mancanza di una gestione efficace degli errori da parte del codice sottostante non presenti informazioni specifiche sul problema.

Per creare messaggi di errore specifici, interoperabili e centrati sull'utente, il codice di gestione degli errori del programma deve fornire informazioni di errore specifiche, ad alto livello:

- A ogni problema deve essere assegnato un codice di errore univoco.
- Se un problema ha diverse cause, il programma deve determinare la causa specifica laddove possibile.
- Se il problema presenta parametri, i parametri devono essere conservati.
- I problemi di basso livello devono essere gestiti a un livello sufficientemente elevato, in modo che il messaggio di errore possa essere presentato dal punto di vista dell'utente.

I messaggi di errore validi non sono semplicemente un problema dell'interfaccia utente. si tratta di un problema di progettazione software. L'esperienza di un messaggio di errore non è un'operazione che può essere adattata in un secondo momento.

**Risoluzione dei problemi (e come evitarla)**

Risoluzione dei problemi relativi ai risultati quando viene segnalato un problema con diverse cause con un unico messaggio di errore.

**Non corretto:**

![diagramma di un messaggio che informa tre cause ](images/mess-error-image16.png)

**Corretto:**

![diagramma di tre messaggi che indica una delle cause](images/mess-error-image17.png)

Risoluzione dei problemi relativi ai risultati quando vengono segnalati diversi problemi con un singolo messaggio di errore.

Nell'esempio seguente non è stato possibile spostare un elemento perché è già stato spostato o eliminato oppure l'accesso è stato negato. Se il programma è in grado di determinare facilmente la causa, perché è necessario che l'utente determini la causa specifica?

**Non corretto:**

![screenshot del messaggio che indica due cause ](images/mess-error-image18.png)

Bene. A questo punto, l'utente deve risolvere i problemi.

Il programma può determinare se l'accesso è stato negato, quindi questo problema dovrebbe essere segnalato con un messaggio di errore specifico.

**Corretto:**

![screenshot del messaggio che indica una delle cause ](images/mess-error-image19.png)

Con una determinata ragione, non è richiesta alcuna risoluzione dei problemi.

Utilizzare i messaggi con più cause solo quando non è possibile determinare la causa specifica. In questo esempio, potrebbe essere difficile per il programma determinare se l'elemento è stato spostato o eliminato, quindi è possibile usare un singolo messaggio di errore con più cause. Tuttavia, è improbabile che gli utenti debbano occuparsi se, ad esempio, non hanno potuto spostare un file eliminato. Per queste cause, il messaggio di errore non è ancora necessario.

**Gestione degli errori sconosciuti**

In alcuni casi, non si conosce il problema, la causa o la soluzione. Se non è consigliabile rimuovere l'errore, è preferibile far fronte alla mancanza di informazioni rispetto a presentare problemi, cause o soluzioni che potrebbero non essere corrette.

Se, ad esempio, nel programma è presente un'eccezione non gestita, è consigliabile il seguente messaggio di errore:

![screenshot del messaggio: si è verificato un errore sconosciuto ](images/mess-error-image20.png)

Se non è possibile evitare un errore sconosciuto, è preferibile far fronte alla mancanza di informazioni.

D'altra parte, è possibile fornire informazioni specifiche e utilizzabili se è probabile che la maggior parte del tempo sia utile.

![Screenshot che mostra un messaggio di Office Communicator "server non disponibile". ](images/mess-error-image21.png)

Questo messaggio di errore è adatto a un errore sconosciuto se la connettività di rete è in genere il problema.

**Determinare il tipo di messaggio appropriato**

Alcuni problemi possono essere presentati come un errore, un avviso o informazioni, a seconda dell'enfasi e della formulazione. Si supponga, ad esempio, che una pagina Web non possa caricare un controllo ActiveX non firmato basato sulla configurazione corrente di Windows Internet Explorer:

- **Errore.** "Questa pagina non può caricare un controllo ActiveX senza segno". (Frase come problema esistente).
- **Avviso.** "Questa pagina potrebbe non comportarsi come previsto perché Windows Internet Explorer non è configurato per il caricamento di controlli ActiveX non firmati". oppure "Consenti a questa pagina di installare un controllo ActiveX senza segno? Questa operazione da origini non attendibili potrebbe danneggiare il computer ". (Entrambe espresse come condizioni che possono causare problemi futuri).
- **Informazioni.** "È stato configurato Windows Internet Explorer per bloccare i controlli ActiveX non firmati." (Enunciato come dichiarazione di fatto).

**Per determinare il tipo di messaggio appropriato, concentrarsi sull'aspetto più importante del problema che gli utenti devono sapere o su cui intervenire.** In genere, se un problema impedisce all'utente di procedere, è necessario presentarlo come errore; Se l'utente può continuare, presentarlo come avviso. Creare l' [istruzione principale](text-ui.md) o un altro testo corrispondente in base a tale stato attivo, quindi scegliere un'icona ([standard](vis-std-icons.md) o altro) che corrisponda al testo. Il testo dell'istruzione principale e le icone devono sempre corrispondere.

**Presentazione del messaggio di errore**

La maggior parte dei messaggi di errore nei programmi Windows viene presentata usando le finestre di dialogo modali (come la maggior parte degli esempi in questo articolo), ma sono disponibili altre opzioni:

- Sul posto
- Palloncini
- Notifiche
- Icone dell'area di notifica
- Barre di stato
- File di log (per gli errori destinati ai professionisti IT)

L'inserimento di messaggi di errore nelle finestre di dialogo modali ha il vantaggio di richiedere l'attenzione e il riconoscimento immediato dell'utente. Tuttavia, questo è anche il loro svantaggio principale se l'attenzione non è necessaria.

![screenshot del messaggio: arrestare l'operazione ](images/mess-error-image22.png)

È davvero necessario interrompere gli utenti in modo che possano fare clic sul pulsante Chiudi? In caso contrario, prendere in considerazione le alternative all'uso di una finestra di dialogo modale.

Le finestre di dialogo modali sono la scelta ideale quando l'utente deve riconoscere il problema immediatamente prima di continuare, ma in caso contrario è spesso una scelta scadente. In genere, è preferibile usare la presentazione con il peso più chiaro che esegue correttamente il processo.

**Evitare la sovracomunicazione**

In genere, [gli utenti non leggono, analizzano](vis-layout.md). Maggiore è il testo, più difficile è il testo da analizzare e più probabilmente gli utenti non leggono il testo. Di conseguenza, è importante ridurre il testo al relativo valore di base e utilizzare la divulgazione progressiva e i collegamenti della guida quando necessario per fornire informazioni aggiuntive.

Ci sono molti esempi estremi, ma ne esaminiamo uno più tipico. L'esempio seguente include la maggior parte degli attributi di un messaggio di errore valido, ma il testo non è conciso e richiede la lettura della motivazione.

**Non corretto:**

![screenshot del messaggio dettagliato ](images/mess-error-image23.png)

Questo esempio è un messaggio di errore valido, ma che si sta comunicando.

Qual è il testo effettivamente detto? Qualcosa di analogo a quanto segue:

**Corretto:**

![screenshot del messaggio: registratore CD non rilevato ](images/mess-error-image24.png)

Questo messaggio di errore presenta essenzialmente le stesse informazioni, ma è molto più conciso.

Utilizzando la guida per fornire i dettagli, questo messaggio di errore presenta uno [stile piramidale invertito](text-ui.md) della presentazione.

Per altre linee guida ed esempi sulla sovracomunicazione, vedere [testo dell'interfaccia utente](text-ui.md).

**Se si eseguono solo otto elementi**

1. Progettare il programma per la gestione degli errori.
2. Non fornire messaggi di errore superflui.
3. Evitare confusione utente fornendo i messaggi di errore necessari.
4. Verificare che il messaggio di errore fornisca un problema, la causa e la soluzione.
5. Verificare che il messaggio di errore sia pertinente, operativo, sintetico, chiaro, specifico, cortese e raro.
6. Progettare messaggi di errore dal punto di vista dell'utente, non dal punto di vista del programma.
7. Evitare di coinvolgere l'utente nella risoluzione dei problemi utilizzare un messaggio di errore diverso per ogni motivo rilevabile.
8. Usare il metodo di presentazione con il peso più chiaro che esegue correttamente il processo.

**Modelli di utilizzo**

I messaggi di errore presentano diversi modelli di utilizzo:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Problemi di sistema</strong><br/> Il sistema operativo, il dispositivo hardware, la rete o il programma non è stato completato o non è nello stato necessario per eseguire un'attività. <br/></td>
<td>Molti problemi di sistema possono essere risolti dall'utente: <br/>
<ul>
<li>È possibile risolvere i problemi del dispositivo attivando il dispositivo, riconnettendo il dispositivo e inserendo i supporti.</li>
<li>È possibile risolvere i problemi di rete controllando la connessione di rete fisica e eseguendo la <strong>diagnostica e il ripristino della rete</strong>.</li>
<li>È possibile risolvere i problemi del programma cambiando le opzioni del programma o riavviando il programma.</li>
</ul>
<img src="images/mess-error-image25.png" alt="Screen shot of message: Can&#39;t find a camera " /><br/> In questo esempio, il programma non riesce a trovare una fotocamera per eseguire un'attività utente.<br/> <img src="images/mess-error-image26.png" alt="Screen shot of message Network discovery off " /><br/> In questo esempio è necessario che sia attivata una funzionalità necessaria per eseguire un'attività.<br/></td>
</tr>
<tr class="even">
<td><strong>Problemi relativi ai file</strong><br/> Un file o una cartella necessaria per un'attività avviata dall'utente non è stato trovato, è già in uso o non ha il formato previsto. <br/></td>
<td><img src="images/mess-error-image27.png" alt="Screen shot of message: Can&#39;t delete file " /><br/> In questo esempio non è possibile eliminare il file o la cartella perché non è stata trovata.<br/> <img src="images/mess-error-image28.png" alt="Screen shot of message: Can&#39;t play this file " /><br/> In questo esempio il programma non supporta il formato di file specificato.<br/></td>
</tr>
<tr class="odd">
<td><strong>Problemi di sicurezza</strong><br/> L'utente non è autorizzato ad accedere a una risorsa o a privilegi sufficienti per eseguire un'attività avviata dall'utente. <br/></td>
<td><img src="images/mess-error-image29.png" alt="Screen shot of message: You don&#39;t have permission " /><br/> In questo esempio, l'utente non è autorizzato ad accedere a una risorsa.<br/> <img src="images/mess-error-image30.png" alt="Screen shot of message: You don&#39;t have privilege " /><br/> In questo esempio, l'utente non dispone dei privilegi necessari per eseguire un'attività.<br/></td>
</tr>
<tr class="even">
<td><strong>Problemi relativi alle attività</strong><br/> Si è verificato un problema specifico durante l'esecuzione di un'attività avviata dall'utente (ad eccezione di un sistema, un file non trovato, un formato di file o un problema di sicurezza). <br/></td>
<td><img src="images/mess-error-image31.png" alt="Screen shot of message: Data can&#39;t be pasted " /><br/> In questo esempio i dati degli Appunti non possono essere incollati in Paint.<br/> <img src="images/mess-error-image32.png" alt="Screen shot of message: Upgrade can&#39;t be installed " /><br/> In questo esempio, l'utente non può installare un aggiornamento software.<br/></td>
</tr>
<tr class="odd">
<td><strong>Problemi di input utente</strong><br/> L'utente ha immesso un valore non corretto o non coerente con altri input utente. <br/></td>
<td><img src="images/mess-error-image33.png" alt="Screen shot of message: Incorrect time value " /><br/> In questo esempio l'utente ha immesso un valore di ora non corretto.<br/> <img src="images/mess-error-image34.png" alt="Screen shot of message: Incorrect input format " /><br/> In questo esempio, l'input dell'utente non è nel formato corretto.<br/></td>
</tr>
</tbody>
</table>

## <a name="guidelines"></a>Indicazioni

### <a name="presentation"></a>Presentazione

- **Usare le finestre di dialogo delle attività quando appropriato** per ottenere un aspetto e un layout coerenti. Le finestre di dialogo delle attività richiedono Windows Vista o versioni successive, quindi non sono adatte per le versioni precedenti di Windows. Se è necessario utilizzare una finestra di messaggio, separare l'istruzione principale dall'istruzione supplementare con due interruzioni di riga.

### <a name="user-input-errors"></a>Errori di input utente

- **Laddove possibile, prevenire o ridurre gli errori di input dell'utente per:**
  - Utilizzo di controlli vincolati a valori validi.
  - La disabilitazione di controlli e voci di menu quando si fa clic genera un errore, purché sia ovvio perché il controllo o la voce di menu è disabilitata.
  - Fornire valori predefiniti validi.

**Non corretto:**

![screenshot della casella di testo con etichetta volume altoparlante ](images/mess-error-image35.png)

In questo esempio viene utilizzata una casella di testo non vincolata per l'input vincolato. Usare invece un dispositivo di scorrimento.

- **Usare la gestione degli errori non modale (errori sul posto o Balloon) per i problemi di input utente contestuali.**
- **Usare i palloni per i problemi di input utente singoli e non critici rilevati in una casella di testo o immediatamente dopo che una casella di testo perde lo stato attivo.** Le [mongolfiere](https://msdn.microsoft.com/library/windows/desktop/aa511451.aspx) non richiedono lo spazio disponibile sullo schermo o il layout dinamico necessario per visualizzare i messaggi sul posto. Visualizzare solo un singolo fumetto alla volta. Poiché il problema non è critico, non è necessaria alcuna icona di errore. Quando si fa clic su un pallone, quando il problema viene risolto o dopo un timeout.

![screenshot del messaggio: carattere non corretto ](images/mess-error-image36.png)

In questo esempio un fumetto indica un problema di input mentre è ancora nel controllo.

- **Usare errori sul posto per il rilevamento degli errori ritardati,** in genere errori trovati facendo clic su un pulsante di commit. Non usare [errori sul posto](glossary.md) per le impostazioni di cui viene immediatamente eseguito il commit. Possono essere presenti più errori sul posto alla volta. Usare il testo normale e un'icona di errore 16x16 pixel, inserendoli direttamente accanto al problema quando possibile. Gli errori sul posto non vengono rilevati a meno che l'utente non venga sottoposto a commit e non vengono rilevati altri errori.

![screenshot del messaggio: indirizzo di posta elettronica non corretto ](images/mess-error-image37.png)

In questo esempio viene usato un errore sul posto per un errore rilevato facendo clic sul pulsante commit.

- **Usare la gestione degli errori modale (finestre di dialogo delle attività o finestre di messaggio) per tutti gli altri problemi, inclusi gli** errori che coinvolgono più controlli o sono stati trovati errori non contestuale o non di input facendo clic su un pulsante di commit.
- **Quando viene segnalato un problema di input dell'utente, impostare lo stato attivo per l'input sul primo controllo con i dati non corretti.** Se necessario, scorrere il controllo nella visualizzazione. Se il controllo è una casella di testo, selezionare l'intero contenuto. Dovrebbe essere sempre evidente a cosa si riferisce il messaggio di errore.
- **Non cancellare l'input errato.** In alternativa, lasciarlo in modo che l'utente possa visualizzare e correggere il problema senza ricominciare.
  - **Eccezione:** Deselezionare le caselle di testo password non corrette e PIN perché gli utenti non possono correggere efficacemente l'input mascherato.

### <a name="troubleshooting"></a>Risoluzione dei problemi

- **Evitare di creare problemi di risoluzione dei problemi.** Non fare affidamento su un singolo messaggio di errore per segnalare un problema con diverse cause rilevabili.
- **Utilizzare un messaggio di errore diverso, in genere un'istruzione supplementare diversa, per ogni motivo rilevabile.** Se, ad esempio, non è possibile aprire un file per diversi motivi, fornire un'istruzione supplementare separata per ogni motivo.
- **Utilizzare un messaggio con più cause solo quando non è possibile determinare la causa specifica.** In questo caso, presentare le soluzioni in ordine di probabilità di risolvere il problema. Questa operazione consente agli utenti di risolvere il problema in modo più efficiente.

### <a name="icons"></a>Icone

- **Le finestre di dialogo del messaggio di errore modale non hanno icone della barra del titolo.** Le icone della barra del titolo vengono usate come distinzione visiva tra le finestre primarie e le finestre secondarie.
- **Utilizzare un'icona di errore.** Eccezioni:
  - Se l'errore è un problema di input dell'utente visualizzato con una finestra di dialogo modale o un fumetto, non usare un'icona. Questa operazione è un contatore al tono incoraggiante di Windows. Tuttavia, i messaggi di errore sul posto devono usare una piccola icona di errore (16x16 pixel) per identificarli chiaramente come messaggi di errore.

     ![screenshot del messaggio formato postale non corretto](images/mess-error-image38.png)

     ![screenshot del nome del computer del messaggio troppo lungo](images/mess-error-image39.png)

     In questi esempi, i problemi di input dell'utente non richiedono icone di errore.

     ![screenshot del formato del numero di telefono del messaggio errato](images/mess-error-image40.png)

     In questo esempio, un messaggio di errore sul posto richiede una piccola icona di errore per identificarlo chiaramente come un messaggio di errore.

- Se il problema riguarda una funzionalità con un'icona (e non un problema di input dell'utente), è possibile usare l'icona della funzionalità con una sovrapposizione degli errori. In tal caso, usare anche il nome della funzionalità come oggetto dell'errore.

    ![il lettore non può riprodurre il file con il messaggio screenshot ](images/mess-error-image41.png)

    In questo esempio, l'icona della funzionalità presenta una sovrapposizione degli errori e la funzionalità è l'oggetto dell'errore.

- **Non usare icone di avviso per gli errori.** Questa operazione viene eseguita spesso per rendere la presentazione meno grave. Gli errori non sono avvisi.

    **Non corretto:**

    ![screenshot della selezione rapida dei messaggi non abilitata ](images/mess-error-image42.png)

    In questo esempio, un'icona di avviso viene erroneamente usata per rendere l'errore meno grave.

Per altre linee guida ed esempi, vedere [icone standard](vis-std-icons.md).

### <a name="progressive-disclosure"></a>Rivelazione progressiva

- **Usare un pulsante Mostra/Nascondi dettagli di divulgazione progressiva per nascondere informazioni avanzate o dettagliate in un messaggio di errore.** In questo modo, il messaggio di errore viene semplificato per l'utilizzo tipico. Non nascondere le informazioni necessarie perché gli utenti potrebbero non trovarlo.

![screenshot del messaggio: Impossibile accedere a ActiveSync ](images/mess-error-image43.png)

In questo esempio, il pulsante di divulgazione progressiva consente agli utenti di eseguire il drill-down in modo più dettagliato se lo desiderano o di semplificare l'interfaccia utente in caso contrario.

- **Non usare i dettagli Mostra/Nascondi a meno che non ci siano altri dettagli.** Non solo riformulare le informazioni esistenti in un formato più dettagliato.
- **Non usare Mostra/Nascondi dettagli per visualizzare le informazioni della guida.** Usare invece i collegamenti della guida.

Per le linee guida per l'assegnazione di etichette, vedere [controlli di divulgazione progressiva](ctrl-progressive-disclosure-controls.md).

**Non visualizzare più questo messaggio**

- **Se per un messaggio di errore è necessaria questa opzione, riconsiderare l'errore e la relativa frequenza.** Se sono presenti tutte le caratteristiche di un buon errore (pertinente, praticabile e poco frequente), non dovrebbe essere opportuno eliminarlo.

Per altre linee guida, vedere [finestre di dialogo](win-dialog-box.md).

### <a name="default-values"></a>Valori predefiniti

- **Selezionare la risposta più sicura, meno distruttiva o più sicura come predefinita.** Se la sicurezza non è un fattore, selezionare il comando più probabile o pratico.

### <a name="help"></a>Help

- **Progettare messaggi di errore per evitare la necessità di aiuto.** Normalmente gli utenti non devono leggere il testo esterno per comprendere e risolvere il problema, a meno che la soluzione non richieda diversi passaggi.
- **Verificare che il contenuto della guida sia pertinente e utile.** Non dovrebbe essere una ripubblicazione dettagliata del messaggio di errore, ma deve contenere informazioni utili che esulano dall'ambito del messaggio di errore, ad esempio modi per evitare il problema in futuro. Non fornire un collegamento alla guida solo perché è possibile.
- **Utilizzare collegamenti specifici, concisi e pertinenti per accedere al contenuto della guida.** Non usare pulsanti di comando o divulgazione progressiva a questo scopo.
- **Per i messaggi di errore che non è possibile rendere specifici e interoperabili, è consigliabile fornire collegamenti al contenuto della guida online.** In questo modo, è possibile fornire agli utenti informazioni aggiuntive che è possibile aggiornare dopo il rilascio del programma.

Per ulteriori linee guida, vedere la [Guida](winenv-help.md)di.

### <a name="error-codes"></a>Codici di errore

- **Per i messaggi di errore che non è possibile rendere specifici e interoperabili o che traggono vantaggio dalla guida, è consigliabile fornire anche codici di errore.** Gli utenti spesso utilizzano questi codici di errore per cercare ulteriori informazioni in Internet.
- **Fornire sempre una descrizione di testo del problema e della soluzione.** Non dipendere solo dal codice di errore a questo scopo.

**Non corretto:**

![screenshot del messaggio: Impossibile aprire il file ](images/mess-error-image44.png)

In questo esempio, un codice di errore viene usato come sostituto di un testo della soluzione.

- **Assegnare un codice di errore univoco per ogni causa diversa.** In questo modo si evita la risoluzione dei problemi.
- **Scegliere i codici di errore che possono essere facilmente ricercati in Internet.** Se si utilizzano i codici a 32 bit, utilizzare una rappresentazione esadecimale con i caratteri "0x" iniziali e maiuscoli.

**Corretto:**

1234

0xC0001234

**Non corretto:**

-1

-67113524

- **Usare Mostra/Nascondi dettagli per visualizzare i codici di errore.** Frase come codice di errore: <error code> .

![screenshot del messaggio: il programma non è stato inizializzato ](images/mess-error-image45.png)

In questo esempio viene utilizzato un codice di errore per integrare un messaggio di errore che può trarre vantaggio da ulteriori informazioni.

### <a name="sound"></a>Suoni

- **Non accompagnare i messaggi di errore con un effetto acustico o un segnale acustico.** Questa operazione è stonata e non necessaria.
  - **Eccezione:** Se il problema è cruciale per il funzionamento del computer e l'utente deve intraprendere azioni immediate per evitare gravi conseguenze, riprodurre l'effetto critico di interruzione.

## <a name="text"></a>Testo

**Generale**

- **Rimuovere il testo ridondante.** Cercarla nei titoli, nelle istruzioni principali, nelle istruzioni aggiuntive, nei collegamenti di comando e nei pulsanti di commit. In genere, lasciare il testo completo nelle istruzioni e nei controlli interattivi e rimuovere qualsiasi ridondanza dalle altre posizioni.
- **Usare le spiegazioni incentrate sull'utente.** Descrivere il problema in termini di azioni utente o obiettivi, non in termini di ciò che il software non è soddisfatto. Usare la lingua che gli utenti di destinazione sono in grado di comprendere e usare. Evitare il gergo tecnico.

**Non corretto:**

![screenshot del messaggio: input-chiamata sincrona ](images/mess-error-image46.png)

**Corretto:**

![screenshot del messaggio: occupato a ricevere una chiamata ](images/mess-error-image47.png)

In questi esempi, la versione corretta indica la lingua dell'utente, mentre la versione non corretta è troppo tecnica.

- **Non usare le parole seguenti:**
  - Errore, errore (usare invece il problema)
  - Non è stato possibile (usare in alternativa)
  - Non valido, non valido, errato (usare invece errato)
  - Abort, Kill, terminate (use stop)
  - Irreversibile, fatale (usare invece gravi)

Questi termini non sono necessari e contrariamente al tono incoraggiante di Windows. Se [utilizzata correttamente](vis-std-icons.md), l'icona di errore comunica sufficientemente che si è verificato un problema.

**Non corretto:**

![screenshot del messaggio: errore irreversibile. ](images/mess-error-image48.png)

**Corretto:**

![screenshot del messaggio: il backup deve essere chiuso contemporaneamente ](images/mess-error-image49.png)

Nell'esempio errato, i termini "irreversibili" e "errore" non sono necessari.

- Non usare la formulazione per biasimare l'utente o implicare un errore dell'utente. Evitare di usare l'utente e la formulazione. Mentre la voce attiva è in genere preferibile, usare la voce passiva quando l'utente è soggetto e potrebbe essere accusato dell'errore se è stata usata la voce attiva.

**Non corretto:**

![screenshot del messaggio immesso accesso errato ](images/mess-error-image50.png)

**Corretto:**

![screenshot del messaggio: password non corretta ](images/mess-error-image51.png)

Nell'esempio errato l'utente viene accusato tramite la voce attiva.

- **Essere specifici.** Evitare una formulazione vaga, ad esempio errori di sintassi e operazione non valida. Specificare nomi, posizioni e valori specifici degli oggetti necessari.

**Non corretto:**

File non trovato.

Disco pieno.

Il valore non è compreso nell'intervallo.

Il carattere non è valido.

Il dispositivo non è disponibile.

Questi problemi sono molto più facili da risolvere con nomi, posizioni e valori specifici.

- **Non è possibile che si verifichino problemi, cause o soluzioni nel tentativo di essere specifici.** Non fornire un problema, una causa o una soluzione, a meno che non sia probabilmente corretta. Ad esempio, è preferibile dire che si è verificato un errore sconosciuto rispetto a un elemento che probabilmente non è accurato.
- **Evitare la parola "Please",** ad eccezione delle situazioni in cui all'utente viene richiesto di eseguire un'operazione scomoda, ad esempio l'attesa, oppure il software deve incolpare la situazione.

**Corretto:**

Attendere mentre Windows copia i file nel computer.

- **Usare la parola "Sorry" solo nei messaggi di errore che causano gravi problemi per l'utente** , ad esempio la perdita di dati o l'impossibilità di usare il computer. Non chiedere scusa se il problema si è verificato durante il normale funzionamento del programma (ad esempio, se l'utente deve attendere la ricerca di una connessione di rete).

**Corretto:**

Il backup di Fabrikam ha rilevato un problema irreversibile ed è stato arrestato per proteggere i file nel computer.

- **Fare riferimento ai prodotti usando i nomi brevi.** Non usare i nomi completi dei prodotti o i simboli dei marchi. Non includere il nome della società, a meno che gli utenti non associno il nome della società al prodotto. Non includere i numeri di versione del programma.

**Non corretto:**

![Screenshot che mostra un messaggio di Microsoft Office Outlook "Impossibile aprire questo elemento". ](images/mess-error-image52.png)

**Corretto:**

![screenshot del messaggio: Impossibile aprire l'elemento ](images/mess-error-image53.png)

Nell'esempio errato vengono usati i nomi completi dei prodotti e i simboli dei marchi.

- **Racchiudere tra virgolette doppie i nomi degli oggetti.** In questo modo il testo risulta più semplice da analizzare ed evitare istruzioni potenzialmente imbarazzanti.
  - **Eccezione:** Non è necessario che i percorsi di file, gli URL e i nomi di dominio completi siano racchiusi tra virgolette doppie.

**Corretto:**

![screenshot del messaggio:' My House ' non è disponibile ](images/mess-error-image54.png)

In questo esempio, il messaggio di errore potrebbe essere confuso se il nome dell'oggetto non era racchiuso tra virgolette.

- **Evitare di avviare frasi con i nomi degli oggetti.** Questa operazione è spesso difficile da analizzare.
- **Non usare punti esclamativi o parole con lettere maiuscole.** I punti esclamativi e le lettere maiuscole fanno sembrare che si stiano gridando all'utente.

Per altre linee guida ed esempi, vedere [stile e tono](text-style-tone.md).

**Titoli**

- **Utilizzare il titolo per identificare il comando o la funzionalità da cui ha avuto origine l'errore.** Eccezioni:
  - Se un errore viene visualizzato con molti comandi diversi, provare a usare il nome del programma.
  - Se il titolo è ridondante o confuso con l'istruzione principale, usare invece il nome del programma.
- **Non usare il titolo per spiegare o riepilogare il problema** che è lo scopo dell'istruzione principale.

**Non corretto:**

![Screenshot che mostra un messaggio "Impossibile rinominare la nuova cartella". ](images/mess-error-image55.png)

In questo esempio il titolo viene erroneamente usato per spiegare il problema.

- Usare l'uso di maiuscole in stile titolo senza la punteggiatura finale.

**Istruzioni principali**

- **Usare l'istruzione principale per descrivere il problema in un linguaggio chiaro, semplice e specifico.**
- **Usare concise solo una singola frase completa.** Riduci l'istruzione principale alle informazioni essenziali. Se si tratta del programma o dell'utente, è possibile lasciare l'oggetto implicito. Includere il motivo del problema se è possibile eseguire questa operazione in modo conciso. Se è necessario spiegare altro, utilizzare un'istruzione supplementare.

**Non corretto:**

![screenshot del messaggio: Impossibile installare l'aggiornamento ](images/mess-error-image56.png)

In questo esempio, l'intero messaggio di errore viene inserito nell'istruzione principale, rendendolo difficile da leggere.

- **Essere specifici se sono presenti oggetti interessati. assegnare loro i nomi.**
- **Evitare di inserire URL e percorsi di file completi nell'istruzione principale.** Usare invece un nome breve (ad esempio il nome del file) e inserire il nome completo, ad esempio il percorso del file, nell'istruzione supplementare. Tuttavia, se il messaggio di errore non necessita di un'istruzione supplementare, è possibile inserire un solo URL o percorso di file completo nell'istruzione principale.

![screenshot del messaggio: Impossibile eliminare il file Fabrikam ](images/mess-error-image57.png)

In questo esempio, solo il nome del file è nell'istruzione principale. Il percorso completo è nell'istruzione supplementare.

- **Non fornire il percorso completo del file e l'URL se è ovvio dal contesto.**

![screenshot del messaggio: Impossibile rinominare la nuova cartella ](images/mess-error-image58.png)

In questo esempio, l'utente rinomina un file da Esplora risorse. In questo caso, il percorso completo del file non è necessario perché è ovvio dal contesto.

- Quando possibile, utilizzare il tempo presente.
- Usare le maiuscole/minuscole come nelle frasi comuni.
- Non includere i periodi finali se l'istruzione è un'istruzione. Se l'istruzione è una domanda, includere un punto interrogativo finale.

**Modelli di istruzioni principali**

Sebbene non esistano regole rigide per la formulazione, provare a usare i modelli di istruzioni principali seguenti quando possibile:

- [nome soggetto facoltativo] non è possibile [eseguire l'azione]
- [nome soggetto facoltativo] non è possibile [eseguire l'azione] perché [motivo]
- [nome soggetto facoltativo] non è possibile [eseguire l'azione] in "[nome oggetto]"
- [nome soggetto facoltativo] non è possibile [eseguire l'azione] in "[nome oggetto]" perché [motivo]
- [Risorsa] insufficiente per [eseguire l'azione]
- [Nome soggetto] non ha un [nome oggetto] richiesto per [scopo]
- [Il dispositivo o l'impostazione] è disattivato in modo che [risultati indesiderati]
- [Dispositivo o impostazione] non è [ \| trovato \| abilitato attivato \| ]
- "[nome oggetto]" non è attualmente disponibile
- Il nome utente o la password non è corretta
- Non si è autorizzati ad accedere a "[nome oggetto]"
- Non si dispone dei privilegi necessari per [eseguire l'azione]
- [nome programma] ha riscontrato un problema grave ed è necessario chiuderlo immediatamente

Naturalmente, apportare modifiche in base alle necessità affinché le istruzioni principali siano corrette in modo grammaticale e siano conformi alle linee guida principali dell'istruzione.

**Istruzioni supplementari**

- Usare l'istruzione supplementare per:
  - Fornire ulteriori dettagli sul problema.
  - Spiegare la causa del problema.
  - Elenca i passaggi che l'utente può eseguire per risolvere il problema.
  - Fornire misure per impedire che si verifichi il problema.
- **Laddove possibile, proporre una soluzione pratica e utile per consentire agli utenti di risolvere il problema.** Tuttavia, assicurarsi che la soluzione proposta sia in grado di risolvere il problema. Non sprecare tempo per gli utenti suggerendo soluzioni possibili, ma improbabili.

**Non corretto:**

![screenshot del messaggio: memoria insufficiente ](images/mess-error-image59.png)

In questo esempio, sebbene il problema e la soluzione consigliata siano possibili, sono molto improbabili.

- **Se il problema è un valore non corretto immesso dall'utente, utilizzare l'istruzione supplementare per illustrare i valori corretti.** Gli utenti non devono necessariamente determinare queste informazioni da un'altra origine.
- **Non fornire una soluzione se può essere dedotta in maniera banale dall'istruzione del problema.**

![screenshot del messaggio: valore di ora non corretto ](images/mess-error-image33.png)

In questo esempio non è necessaria alcuna istruzione supplementare; la soluzione può essere dedotta dalla dichiarazione del problema.

- **Se la soluzione prevede più passaggi, presentare i passaggi nell'ordine in cui devono essere completati.** Tuttavia, evitare le soluzioni in più passaggi perché gli utenti hanno difficoltà a ricordare più di due o tre semplici passaggi. Se sono necessari più passaggi, fare riferimento all'argomento della Guida appropriato.
- **Mantieni concise le istruzioni aggiuntive.** Fornire solo le informazioni necessarie agli utenti. Omettere i dettagli superflui. Puntare per un massimo di tre frasi di lunghezza moderata.
- **Per evitare errori mentre gli utenti eseguono istruzioni, inserire i risultati prima dell'azione.**

**Corretto:**

Per riavviare Windows, fare clic su OK.

**Non corretto:**

Fare clic su OK per riavviare Windows.

Nell'esempio errato, è più probabile che gli utenti clicchino su OK per errore.

- **Non è consigliabile contattare un amministratore a meno che non si tratti di un problema tra le soluzioni più probabili.** Riservare tali soluzioni per i problemi che possono essere risolti solo da un amministratore.

**Non corretto:**

![screenshot del messaggio: server non disponibile ](images/mess-error-image60.png)

In questo esempio, è molto probabile che il problema sia dovuto alla connessione di rete dell'utente, pertanto non è opportuno contattare un amministratore.

- **Non è consigliabile contattare il supporto tecnico.** L'opzione per contattare il supporto tecnico per risolvere un problema è sempre disponibile e non deve essere promossa tramite messaggi di errore. Concentrarsi invece sulla scrittura di messaggi di errore utili, in modo che gli utenti possano risolvere i problemi senza contattare il supporto tecnico.

**Non corretto:**

![Screenshot che mostra un messaggio "Impossibile aprire questo elemento". ](images/mess-error-image61.png)

In questo esempio, il messaggio di errore consiglia erroneamente di contattare il supporto tecnico.

- Usare frasi complete, maiuscole e minuscole in stile frase e punteggiatura finale.

**Pulsanti di commit**

- Se il messaggio di errore fornisce i pulsanti di comando o i collegamenti ai comandi che consentono di risolvere il problema, seguire le rispettive linee guida nelle [finestre di dialogo](win-dialog-box.md).
- Se il programma deve terminare in seguito all'errore, fornire un pulsante Esci da programma. Per evitare confusione, non usare Close per questo scopo.
- In caso contrario, fornire un pulsante Chiudi. Non usare OK per i messaggi di errore, perché questa formulazione implica che i problemi sono OK.
  - **Eccezione:** Utilizzare OK se il meccanismo di segnalazione errori dispone di etichette fisse (come con l'API MessageBox).

## <a name="documentation"></a>Documentazione

Quando si fa riferimento a errori:

- Per istruzioni principali, vedere gli errori. Se l'istruzione principale è Long o detailed, riepilogarla.
- Se necessario, è possibile fare riferimento a una finestra di dialogo di messaggio di errore come messaggio. Vedere come messaggio di errore solo nella programmazione e in altri documenti tecnici.
- Quando possibile, formattare il testo usando grassetto. In caso contrario, inserire il testo tra virgolette solo se necessario per evitare confusione.

**Esempio:** Se si riceve un **disco CD nel messaggio dell'unità** , inserire un nuovo disco CD nell'unità e riprovare.