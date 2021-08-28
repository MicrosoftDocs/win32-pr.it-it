---
title: Messaggi di errore (nozioni di base sulla progettazione)
description: Un messaggio di errore avvisa gli utenti di un problema che si è già verificato.
ms.assetid: b02110e9-985d-4448-9c95-eb958b0059b1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 50e9d945baf736329d38334a94ede6158621167c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984104"
---
# <a name="error-messages-design-basics"></a>Messaggi di errore (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Un messaggio di errore avvisa gli utenti di un problema che si è già verificato. Al contrario, un messaggio di avviso avvisa gli utenti di una condizione che potrebbe causare un problema in futuro. I messaggi di errore possono essere visualizzati usando finestre di dialogo modali, messaggi sul posto, notifiche o balloon.

![Screenshot del messaggio di errore: Non è possibile rinominare](images/mess-error-image1.png)

Messaggio di errore modale tipico.

I messaggi di errore effettivi informano gli utenti che si è verificato un problema, spiegano perché si è verificato e forniscono una soluzione per consentire agli utenti di risolvere il problema. Gli utenti devono eseguire un'azione o modificarne il comportamento come risultato di un messaggio di errore.

I messaggi di errore ben scritti e utili sono fondamentali per un'esperienza utente di qualità. I messaggi di errore scritti in modo non soddisfacente comportano una bassa soddisfazione del prodotto e sono una causa principale di costi di supporto tecnico evitabili. I messaggi di errore non necessari interrompno il flusso degli utenti.

**Nota:** Le linee guida relative a [](mess-confirm.md) [finestre di dialogo,](win-dialog-box.md)messaggi di [avviso,](mess-warn.md) [conferme, icone standard,](vis-std-icons.md) [notifiche](mess-notif.md)e [layout](vis-layout.md) vengono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, prendi in considerazione queste domande:

- **L'interfaccia utente sta presentando un problema che si è già verificato?** In caso contrario, il messaggio non è un errore. Se l'utente viene avvisato di una condizione che potrebbe causare un problema in futuro, usare un messaggio di avviso.
- **Il problema può essere evitato senza causare confusione?** In tal caso, evitare il problema. Ad esempio, usare controlli vincolati a valori validi anziché controlli non vincolati che possono richiedere messaggi di errore. Inoltre, disabilitare i controlli quando si fa clic restituirebbe un errore, purché sia evidente il motivo per cui il controllo è disabilitato.
- **Il problema può essere corretto automaticamente?** In tal caso, gestire il problema ed eliminare il messaggio di errore.
- **Gli utenti probabilmente eseguiranno un'azione o modificheranno il comportamento come risultato del messaggio?** In caso contrario, la condizione non giustifica l'interruzione dell'utente, quindi è meglio eliminare l'errore.
- **Il problema è rilevante quando gli utenti usano attivamente altri programmi?** In tal caso, provare a visualizzare il problema usando [un'icona dell'area di notifica](winenv-notification.md).
- **Il problema non è correlato all'attività dell'utente corrente, non richiede un intervento immediato da parte dell'utente e gli utenti possono ignorarlo liberamente?** In tal caso, usare invece una [notifica di errore dell'azione.](mess-notif.md)
- **Il problema è correlato allo stato di un'attività in background all'interno di una finestra primaria?** In tal caso, provare a visualizzare il problema usando una barra [di stato](ctrl-status-bars.md).
- **I principali utenti di destinazione sono i professionisti IT?** In tal caso, è consigliabile usare un meccanismo di feedback alternativo, ad esempio voci [di file](glossary.md) di log o avvisi di posta elettronica. I professionisti IT preferiscono fortemente i file di log per le informazioni non critiche.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

**Caratteristiche dei messaggi di errore non visualizzati**

Non deve essere sorprendente che ci siano molti messaggi di errore insoddvoli, inutili e scritti in modo eroso. Inoltre, poiché i messaggi di errore vengono spesso presentati usando finestre di dialogo modali, interrompe l'attività corrente dell'utente e la richiesta di conferma prima di consentire all'utente di continuare.

Parte del problema è che esistono così tanti modi per farlo in modo errato. Si considerino questi esempi della Sala dei messaggi di errore di Eva:

**Messaggi di errore non necessari**

**Non corretto:**

![Screenshot del messaggio di errore: applicazione non riuscita ](images/mess-error-image2.png)

Questo esempio di Windows XP potrebbe essere il messaggio di errore peggiore di sempre. Indica che non è stato possibile avviare un programma perché Windows è in corso l'arresto. Non c'è nulla che l'utente possa fare in questo caso o addirittura vuole farlo (l'utente ha scelto di arrestare Windows, dopo tutto). E visualizzando questo messaggio di errore, Windows si impedisce l'arresto.

**Il problema:** Il problema è il messaggio di errore. Oltre a ignorare il messaggio di errore, non c'è nulla da fare per gli utenti.

**Causa principale:** Segnalazione di tutti i casi di errore, indipendentemente dagli obiettivi o dal punto di vista degli utenti.

**Alternativa consigliata:** Non segnalare errori che gli utenti non sono a loro abili.

**Messaggi di errore "Operazione riuscita"**

**Non corretto:**

![Screenshot del messaggio di errore: errore di rimozione ](images/mess-error-image3.png)

Questo messaggio di errore è stato visualizzato quando l'utente ha scelto di non Windows immediatamente dopo la rimozione del programma. La rimozione del programma è riuscita dal punto di vista dell'utente.

**Il problema:** Non si verificano errori dal punto di vista dell'utente. Oltre a ignorare il messaggio di errore, non c'è nulla da fare per gli utenti.

**Causa principale:** L'attività è stata completata correttamente dal punto di vista dell'utente, ma non dal punto di vista del programma di disinstallazione.

**Alternativa consigliata:** Non segnalare errori per condizioni considerate accettabili dagli utenti.

**Messaggi di errore completamente inutili**

**Non corretto:**

![Screenshot del messaggio di errore: errore sconosciuto ](images/mess-error-image4.png)

Gli utenti apprendono che si è verificato un errore, ma non hanno idea di quale sia stato l'errore o cosa fare. E no, non va bene.

**Il problema:** Il messaggio di errore non indica un problema specifico e gli utenti non possono fare nulla.

**Causa principale:** Molto probabilmente, la gestione degli errori del programma è scarsa.

**Alternativa consigliata:** Progettare una buona gestione degli errori nel programma.

**Messaggi di errore incomprensibili**

**Non corretto:**

![Screenshot del messaggio di errore: Backup non completato ](images/mess-error-image5.png)

In questo esempio, l'affermazione del problema è chiara, ma la spiegazione supplementare è assolutamente sconcertante.

**Il problema:** La dichiarazione o la soluzione del problema non è comprensibile.

**Causa principale:** Spiegazione del problema dal punto di vista del codice anziché dell'utente.

**Alternativa consigliata:** Scrivere testo del messaggio di errore facilmente comprensibile per gli utenti di destinazione. Fornire soluzioni che gli utenti possono effettivamente eseguire. Per progettare l'esperienza dei messaggi di errore del programma, i programmatori non devono comporre messaggi di errore sul posto.

**Messaggi di errore overcommunicate**

**Non corretto:**

![Screenshot del messaggio estremamente dettagliato ](images/mess-error-image6.png)

In questo esempio il messaggio di errore tenta apparentemente di spiegare ogni passaggio di risoluzione dei problemi.

**Il problema:** Troppe informazioni.

**Causa principale:** Fornire troppi dettagli o tentare di spiegare un processo di risoluzione dei problemi complesso all'interno di un messaggio di errore.

**Alternativa consigliata:** Evitare dettagli non necessari. Evitare anche di risolvere i problemi. Se è necessario uno strumento di risoluzione dei problemi, concentrarsi sulle soluzioni più probabili e spiegare il resto collegando all'argomento appropriato nella Guida.

**Messaggi di errore inutilmente ergasi**

**Non corretto:**

![Screenshot del messaggio: Impossibile trovare l'oggetto ](images/mess-error-image7.png)

L'impossibilità del programma di trovare un oggetto sembra irreversibile. Supponendo che sia catastrofico, perché la risposta è corretta?

**Il problema:** Il tono del programma è inutilmente rigido o notevole.

**Causa principale:** Il problema è dovuto a un bug che dal punto di vista del programma risulta irreversico.

**Alternativa consigliata:** Scegliere con attenzione la lingua in base al punto di vista dell'utente.

**Messaggi di errore che incolpano gli utenti**

**Non corretto:**

![Screenshot del messaggio: carattere non valido ](images/mess-error-image8.png)

Perché fare in modo che gli utenti si senta un criminale?

**Il problema:** Il messaggio di errore viene formulato in modo da insoddire l'utente di aver generato un errore.

**Causa principale:** Formulazione senza distinzione che si concentra sul comportamento dell'utente anziché sul problema.

**Alternativa consigliata:** Concentrarsi sul problema, non sull'azione dell'utente che ha causato il problema, usando la voce passiva in base alle esigenze.

**Messaggi di errore non semplici**

**Non corretto:**

![Screenshot del messaggio: errore nella segnalazione errori ](images/mess-error-image9.png)

In questo esempio l'affermazione del problema è piuttosto ironia e non vengono fornite soluzioni.

**Il problema:** Istruzioni di messaggi di errore non semplici o non sequitor.

**Causa principale:** Creazione di messaggi di errore senza prestare attenzione al contesto.

**Alternativa consigliata:** Creare e rivedere i messaggi di errore da un writer. Quando si esaminano gli errori, considerare il contesto e lo stato d'mente dell'utente.

**Messaggi di errore del programmatore**

**Non corretto:**

![Screenshot del messaggio: indirizzo di violazione di accesso ](images/mess-error-image10.png)

In questo esempio, il messaggio di errore indica che è presente un bug nel programma. Questo messaggio di errore ha significato solo per il programmatore.

**Il problema:** I messaggi destinati ad aiutare gli sviluppatori del programma a trovare i bug vengono lasciati nella versione di rilascio del programma. Questi messaggi di errore non hanno significato o valore per gli utenti.

**Causa principale:** Programmatori che usano l'interfaccia utente normale per inviare messaggi a se stessi.

**Alternativa consigliata:** Gli sviluppatori devono compilare in modo condizionale tutti questi messaggi in modo che siano rimossi automaticamente dalla versione di rilascio di un prodotto. Non perdere tempo a cercare di rendere comprensibili errori come questo per gli utenti, perché il loro unico pubblico sono i programmatori.

**Messaggi di errore presentati in modo non erre**

**Non corretto:**

![Screenshot del messaggio: errore imprevisto ](images/mess-error-image11.png)

Questo esempio presenta molti errori di presentazione comuni.

**Il problema:** Recupero di tutti i dettagli non corretto nella presentazione del messaggio di errore.

**Causa principale:** Non conoscendo e applicando le linee guida per i messaggi di errore. Non si usano writer ed editor per creare ed esaminare i messaggi di errore.

La natura della gestione degli errori è tale che molti di questi errori sono molto facili da commettere. È preoccupante rendersi conto che la maggior parte dei messaggi di errore potrebbe essere candidata per la Hall of Shame.

**Caratteristiche dei messaggi di errore buoni**

A differenza degli esempi non buoni precedenti, i messaggi di errore sono:

- **Un problema.** Indica che si è verificato un problema.
- **Una causa.** Spiega perché si è verificato il problema.
- **Una soluzione.** Fornisce una soluzione che consente agli utenti di risolvere il problema.

Inoltre, i messaggi di errore sono presentati nel modo seguente:

- **Rilevante.** Il messaggio presenta un problema che interessa agli utenti.
- **Eseguibili.** Gli utenti devono eseguire un'azione o modificarne il comportamento come risultato del messaggio.
- **Centrata dall'utente.** Il messaggio descrive il problema in termini di azioni o obiettivi dell'utente di destinazione, non in termini di ciò che il codice non è soddisfatto.
- **Breve.** Il messaggio è il più breve possibile, ma non più breve.
- **Chiaro.** Il messaggio usa un linguaggio normale in modo che gli utenti di destinazione possano comprendere facilmente il problema e la soluzione.
- **Specifico.** Il messaggio descrive il problema usando un linguaggio specifico, fornendo nomi, posizioni e valori specifici degli oggetti coinvolti.
- **Cortese.** Gli utenti non devono essere incolpati o incolpati.
- **Raro.** Viene visualizzato raramente. I messaggi di errore visualizzati di frequente sono un segno di progettazione non erta.

Progettando l'esperienza di gestione degli errori in modo che abbia queste caratteristiche, è possibile mantenere i messaggi di errore del programma fuori dalla sala dei messaggi di errore di tutti i tipi.

**Evitare messaggi di errore non necessari**

Spesso il messaggio di errore migliore non è alcun messaggio di errore. Molti errori possono essere evitati con una progettazione migliore e spesso esistono alternative migliori ai messaggi di errore. In genere è meglio evitare un errore che segnalarne uno.

I messaggi di errore più ovvi da evitare sono quelli che non sono utilizzabili. Se gli utenti potrebbero ignorare il messaggio senza eseguire o modificare alcun elemento, omettere il messaggio di errore.

Alcuni messaggi di errore possono essere eliminati perché non sono problemi dal punto di vista dell'utente. Si supponga, ad esempio, che l'utente abbia tentato di eliminare un file già in corso di eliminazione. Anche se potrebbe trattarsi di un caso imprevisto dal punto di vista del codice, gli utenti non considerano questo errore perché si ottiene il risultato desiderato.

**Non corretto:**

![Screenshot del messaggio: Impossibile eliminare il file ](images/mess-error-image12.png)

Questo messaggio di errore deve essere eliminato perché l'azione ha avuto esito positivo dal punto di vista dell'utente.

Si supponga, ad esempio, che l'utente annulli in modo esplicito un'attività. Per il punto di vista dell'utente, la condizione seguente non è un errore.

**Non corretto:**

![Screenshot del messaggio: Impossibile completare il backup ](images/mess-error-image13.png)

Questo messaggio di errore deve essere eliminato anche perché l'azione ha avuto esito positivo dal punto di vista dell'utente.

A volte i messaggi di errore possono essere eliminati concentrandosi sugli obiettivi degli utenti anziché sulla tecnologia. In questo modo, riconsiderare che cos'è effettivamente un errore. Il problema è relativo agli obiettivi dell'utente o alla capacità del programma di soddisfarli? Se l'azione dell'utente ha senso nel mondo reale, dovrebbe avere senso anche nel software.

Si supponga, ad esempio, che all'interno di un programma di e-commerce un utente tenti di trovare un prodotto usando la ricerca, ma la query di ricerca letterale non ha corrispondenze e il prodotto desiderato non è disponibile. Tecnicamente, si tratta di un errore, ma invece di fornire un messaggio di errore, il programma potrebbe:

- Continuare a cercare i prodotti che corrispondono maggiormente alla query.
- Se la ricerca presenta errori evidenti, consigliare automaticamente una query corretta.
- Gestire automaticamente problemi comuni, ad esempio errori di ortografia, ortografie alternative e mancata corrispondenza di pluralizzazione e casi di verbi.
- Indicare quando il prodotto sarà disponibile in magazzino.

Finché la richiesta dell'utente è ragionevole, un programma di e-commerce ben progettato dovrebbe restituire risultati ragionevoli non errori.

Un altro ottimo modo per evitare i messaggi di errore è innanzitutto evitare problemi. È possibile impedire gli errori tramite:

- **Uso di controlli vincolati.** Usare controlli vincolati a valori validi. Controlli come elenchi, dispositivi di scorrimento, caselle di controllo, pulsanti di opzione e selettori di data e ora sono vincolati a valori validi, mentre le caselle di testo spesso non sono e possono richiedere messaggi di errore. È tuttavia possibile vincolare le caselle di testo in modo che accettino solo determinati caratteri e accettino un numero massimo di caratteri.
- **Uso di interazioni vincolate.** Per le operazioni di trascinamento, consentire agli utenti di rilasciare solo su destinazioni valide.
- **Uso di controlli disabilitati e voci di menu.** Disabilitare i controlli e le voci di menu quando gli utenti possono dedurre facilmente il motivo per cui il controllo o la voce di menu è disabilitata.
- **Fornire valori predefiniti validi.** Gli utenti hanno meno probabilità di errori di input se possono accettare i valori predefiniti. Anche se gli utenti decidono di modificare il valore, il valore predefinito consente agli utenti di conoscere il formato di input previsto.
- **Fare in modo che le cose funzionino.** Gli utenti hanno meno probabilità di commettere errori se le attività non sono necessarie o vengono eseguite automaticamente per loro. Oppure, se gli utenti commettono piccoli errori ma la loro intenzione è chiara, il problema viene risolto automaticamente. Ad esempio, è possibile correggere automaticamente i problemi di formattazione secondari.

**Fornire i messaggi di errore necessari**

A volte è effettivamente necessario fornire un messaggio di errore. Gli utenti commettono errori, le reti e i dispositivi smettono di funzionare, gli oggetti non possono essere trovati o modificati, le attività non possono essere completate e i programmi hanno bug. Idealmente, questi problemi si verificano meno spesso, ad esempio, è possibile progettare il software per evitare molti tipi di errori dell'utente, ma non è realistico evitare tutti questi problemi. Quando si verifica uno di questi problemi, un messaggio di errore utile consente agli utenti di tornare rapidamente in piedi.

Una credenza comune è che i messaggi di errore siano l'esperienza utente peggiore e devono essere evitati a tutti i costi, ma è più accurato dire che la confusione degli utenti è l'esperienza peggiore e deve essere evitata a tutti i costi. A volte questo costo è un messaggio di errore utile.

Si considerino i controlli disabilitati. Nella maggior parte dei casi, è ovvio perché un controllo è disabilitato, quindi la disabilitazione del controllo è un ottimo modo per evitare un messaggio di errore. Tuttavia, cosa succede se il motivo per cui un controllo è disabilitato non è ovvio? L'utente non può procedere e non sono presenti commenti per determinare il problema. Ora l'utente è bloccato e deve dedurre il problema o ottenere supporto tecnico. In questi casi, è molto meglio lasciare il controllo abilitato e fornire invece un messaggio di errore utile.

**Non corretto:**

![Screenshot del messaggio: dove salvare il backup? ](images/mess-error-image14.png)

Perché il pulsante Avanti è disabilitato qui? È meglio lasciarlo abilitato ed evitare confusione dell'utente, fornendo un messaggio di errore utile.

Se non si è certi di dover inviare un messaggio di errore, iniziare componendo il messaggio di errore che potrebbe essere visualizzato. Se gli utenti possono eseguire un'azione o modificarne il comportamento di conseguenza, specificare il messaggio di errore. Al contrario, se è probabile che gli utenti eseguino la chiusura del messaggio senza eseguire o modificare alcun elemento, omettere il messaggio di errore.

**Progettazione per una buona gestione degli errori**

Anche se la creazione di un testo di messaggio di errore di qualità può essere complessa, a volte è impossibile senza un buon supporto per la gestione degli errori dal programma. Si consideri questo messaggio di errore:

**Non corretto:**

![Screenshot del messaggio: errore sconosciuto ](images/mess-error-image15.png)

È probabile che il problema sia davvero sconosciuto perché manca il supporto per la gestione degli errori del programma.

Anche se è possibile che si tratta di un messaggio di errore scritto in modo non valido, è più probabile che rifletta la mancanza di una buona gestione degli errori da parte del codice sottostante, ma non sono note informazioni specifiche sul problema.

Per creare messaggi di errore specifici, utilizzabili e centrati sull'utente, il codice di gestione degli errori del programma deve fornire informazioni specifiche sugli errori di alto livello:

- A ogni problema deve essere assegnato un codice di errore univoco.
- Se un problema presenta diverse cause, il programma deve determinare la causa specifica quando possibile.
- Se il problema presenta parametri, è necessario mantenere i parametri.
- I problemi di basso livello devono essere gestiti a un livello sufficientemente elevato in modo che il messaggio di errore possa essere visualizzato dal punto di vista dell'utente.

I buoni messaggi di errore non sono solo un problema dell'interfaccia utente, ma un problema di progettazione software. Un'esperienza di messaggio di errore ottimale non è qualcosa che può essere intasato in un secondo momento.

**Risoluzione dei problemi (e come evitarla)**

La risoluzione dei problemi si verifica quando un problema con diverse cause viene segnalato con un singolo messaggio di errore.

**Non corretto:**

![diagramma di un messaggio che indica tre cause ](images/mess-error-image16.png)

**Corretto:**

![diagramma di tre messaggi che indicano una causa ciascuno](images/mess-error-image17.png)

Risoluzione dei problemi quando vengono segnalati diversi problemi con un singolo messaggio di errore.

Nell'esempio seguente non è stato possibile spostare un elemento perché è già stato spostato o eliminato oppure l'accesso è stato negato. Se il programma è in grado di determinare facilmente la causa, perché mettere il carico di lavoro sull'utente per determinare la causa specifica?

**Non corretto:**

![Screenshot del messaggio che indica due cause ](images/mess-error-image18.png)

Bene, qual è? A questo punto l'utente deve risolvere i problemi.

Il programma può determinare se l'accesso è stato negato, quindi questo problema deve essere segnalato con un messaggio di errore specifico.

**Corretto:**

![Screenshot del messaggio che indica una causa ](images/mess-error-image19.png)

Con una causa specifica, non è necessaria alcuna risoluzione dei problemi.

Usare messaggi con più cause solo quando non è possibile determinare la causa specifica. In questo esempio, sarebbe difficile per il programma determinare se l'elemento è stato spostato o eliminato. In questo caso potrebbe essere usato un singolo messaggio di errore con più cause. Tuttavia, è improbabile che gli utenti si occupino se, ad esempio, non sono riusciti a spostare un file eliminato. Per queste cause, il messaggio di errore non è nemmeno necessario.

**Gestione degli errori sconosciuti**

In alcuni casi, non si conoscerà il problema, la causa o la soluzione. Se non è consigliabile eliminare l'errore, è consigliabile evitare la mancanza di informazioni piuttosto che presentare problemi, cause o soluzioni che potrebbero non essere giuste.

Ad esempio, se il programma presenta un'eccezione non gestita, è appropriato il messaggio di errore seguente:

![Screenshot del messaggio: si è verificato un errore sconosciuto ](images/mess-error-image20.png)

Se non è possibile eliminare un errore sconosciuto, è meglio essere in anticipo sulla mancanza di informazioni.

D'altra parte, fornire informazioni specifiche e utilizzabili se è probabile che siano utili nella maggior parte dei casi.

![Screenshot che mostra un messaggio Office Communicator 'server non disponibile'. ](images/mess-error-image21.png)

Questo messaggio di errore è adatto per un errore sconosciuto se il problema è in genere la connettività di rete.

**Determinare il tipo di messaggio appropriato**

Alcuni problemi possono essere presentati come un errore, un avviso o informazioni, a seconda dell'enfasi e della formulazione. Si supponga, ad esempio, che una pagina Web non possa caricare un controllo ActiveX basato sulla configurazione Windows Internet Explorer corrente:

- **Errore.** "Questa pagina non può caricare un controllo ActiveX non firmato." (Formulato come un problema esistente.
- **Avviso.** "Questa pagina potrebbe non comportarsi come previsto perché Windows Internet Explorer non è configurato per caricare i controlli ActiveX firmati." o "Consenti a questa pagina di installare un controllo ActiveX non firmato? Questa operazione da origini non attendibili può danneggiare il computer." Entrambe formulate come condizioni che possono causare problemi futuri.
- **Informazioni.** "Sono stati configurati Windows Internet Explorer per bloccare i controlli ActiveX non firmati." (Formulato come affermazione di fatto).

**Per determinare il tipo di messaggio appropriato, concentrarsi sull'aspetto più importante del problema che gli utenti devono conoscere o su cui intervenire.** In genere, se un problema impedisce all'utente di procedere, è necessario presentarlo come errore. se l'utente può procedere, presentarlo come avviso. Creare [l'istruzione principale](text-ui.md) o altro testo corrispondente in base a tale stato attivo, quindi scegliere un'icona[(standard](vis-std-icons.md) o altro) che corrisponde al testo. Il testo dell'istruzione principale e le icone devono sempre corrispondere.

**Presentazione del messaggio di errore**

La maggior parte dei messaggi di errore nei programmi Windows vengono visualizzati usando finestre di dialogo modali (come la maggior parte degli esempi in questo articolo), ma sono disponibili altre opzioni:

- Sul posto
- Palloncini
- Notifiche
- Icone dell'area di notifica
- Barre di stato
- File di log (per gli errori destinati ai professionisti IT)

L'inserimento di messaggi di errore nelle finestre di dialogo modali ha il vantaggio di chiedere l'attenzione e il riconoscimento immediati dell'utente. Tuttavia, questo è anche il principale svantaggio se tale attenzione non è necessaria.

![Screenshot del messaggio: arrestare l'operazione ](images/mess-error-image22.png)

È davvero necessario interrompere gli utenti in modo che possano fare clic sul pulsante Chiudi? In caso contrario, prendere in considerazione alternative all'uso di una finestra di dialogo modale.

Le finestre di dialogo modali sono un'ottima scelta quando l'utente deve riconoscere il problema immediatamente prima di continuare, ma spesso è una scelta non ottimale. In genere, è consigliabile usare la presentazione con il peso più leggero che fa bene il lavoro.

**Evitare l'overcommunicating**

In genere, [gli utenti non leggono, analizzano](vis-layout.md). Più testo è presente, più difficile è l'analisi del testo e più è probabile che gli utenti non leggono il testo. Di conseguenza, è importante ridurre il testo alle informazioni di base e usare la diffusione progressiva e i collegamenti alla Guida quando necessario per fornire informazioni aggiuntive.

Esistono molti esempi estremi, ma ne esamini uno più tipico. L'esempio seguente include la maggior parte degli attributi di un messaggio di errore, ma il testo non è conciso e richiede motivazione per la lettura.

**Non corretto:**

![Screenshot del messaggio dettagliato ](images/mess-error-image23.png)

Questo esempio è un buon messaggio di errore, ma overcommunicates.

Che cosa dice tutto questo testo? Qualcosa di analogo a quanto segue:

**Corretto:**

![Screenshot del messaggio: registratore cd non rilevato ](images/mess-error-image24.png)

Questo messaggio di errore contiene essenzialmente le stesse informazioni, ma è molto più conciso.

Usando la Guida per fornire i dettagli, questo messaggio di errore ha uno stile a piramide [invertito](text-ui.md) di presentazione.

Per altre linee guida ed esempi sull'overcommunicating, vedere Interfaccia utente [Text](text-ui.md).

**Se si eservino solo otto operazioni**

1. Progettare il programma per la gestione degli errori.
2. Non fornire messaggi di errore non necessari.
3. Evitare confusione dell'utente fornendo i messaggi di errore necessari.
4. Assicurarsi che il messaggio di errore dia un problema, una causa e una soluzione.
5. Assicurarsi che il messaggio di errore sia pertinente, fattibile, breve, chiaro, specifico, cortese e raro.
6. Progettare i messaggi di errore dal punto di vista dell'utente, non dal punto di vista del programma.
7. Evitare di coinvolgere l'utente nella risoluzione dei problemi usare un messaggio di errore diverso per ogni causa rilevabile.
8. Usare il metodo di presentazione del peso più leggero che consente di eseguire il processo in modo appropriato.

**Modelli di utilizzo**

I messaggi di errore hanno diversi modelli di utilizzo:


| Etichetta | Valore |
|--------|-------|
| <strong>Problemi di sistema</strong><br /> Il sistema operativo, il dispositivo hardware, la rete o il programma non è riuscito o non è nello stato necessario per eseguire un'attività. <br /> | Molti problemi di sistema possono essere risolti dall'utente: <br /><ul><li>I problemi del dispositivo possono essere risolti attivando il dispositivo, riconnettendo il dispositivo e inserendo supporti.</li><li>I problemi di rete possono essere risolti controllando la connessione di rete fisica ed eseguendo <strong>Diagnostica e ripristino della rete.</strong></li><li>I problemi del programma possono essere risolti modificando le opzioni del programma o riavviando il programma.</li></ul><img src="images/mess-error-image25.png" alt="Screen shot of message: Can't find a camera " /><br /> In questo esempio il programma non trova una fotocamera per eseguire un'attività utente.<br /><img src="images/mess-error-image26.png" alt="Screen shot of message Network discovery off " /><br /> In questo esempio deve essere attivata una funzionalità necessaria per eseguire un'attività.<br /> | 
| <strong>Problemi relativi ai file</strong><br /> Un file o una cartella necessaria per un'attività avviata dall'utente non è stato trovato, è già in uso o non ha il formato previsto. <br /> | <img src="images/mess-error-image27.png" alt="Screen shot of message: Can't delete file " /><br /> In questo esempio non è possibile eliminare il file o la cartella perché non è stato trovato.<br /><img src="images/mess-error-image28.png" alt="Screen shot of message: Can't play this file " /><br /> In questo esempio il programma non supporta il formato di file specificato.<br /> | 
| <strong>Problemi di sicurezza</strong><br /> L'utente non dispone dell'autorizzazione per accedere a una risorsa o di privilegi sufficienti per eseguire un'attività avviata dall'utente. <br /> | <img src="images/mess-error-image29.png" alt="Screen shot of message: You don't have permission " /><br /> In questo esempio l'utente non dispone dell'autorizzazione per accedere a una risorsa.<br /><img src="images/mess-error-image30.png" alt="Screen shot of message: You don't have privilege " /><br /> In questo esempio l'utente non ha il privilegio di eseguire un'attività.<br /> | 
| <strong>Problemi relativi alle attività</strong><br /> Si è verificato un problema specifico durante l'esecuzione di un'attività avviata dall'utente(diverso da un sistema, un file non trovato, un formato di file o un problema di sicurezza). <br /> | <img src="images/mess-error-image31.png" alt="Screen shot of message: Data can't be pasted " /><br /> In questo esempio i dati degli Appunti non possono essere incollati in Paint.<br /><img src="images/mess-error-image32.png" alt="Screen shot of message: Upgrade can't be installed " /><br /> In questo esempio l'utente non può installare un aggiornamento software.<br /> | 
| <strong>Problemi di input dell'utente</strong><br /> L'utente ha immesso un valore non corretto o incoerente con un altro input utente. <br /> | <img src="images/mess-error-image33.png" alt="Screen shot of message: Incorrect time value " /><br /> In questo esempio l'utente ha immesso un valore di ora non corretto.<br /><img src="images/mess-error-image34.png" alt="Screen shot of message: Incorrect input format " /><br /> In questo esempio l'input dell'utente non è nel formato corretto.<br /> | 


## <a name="guidelines"></a>Indicazioni

### <a name="presentation"></a>Presentazione

- **Usare le finestre di dialogo delle attività quando appropriato** per ottenere un aspetto e un layout coerenti. I dialoghe attività Windows Vista o versioni successive, quindi non sono adatti per le versioni precedenti di Windows. Se è necessario usare una finestra di messaggio, separare l'istruzione principale dall'istruzione supplementare con due interruzioni di riga.

### <a name="user-input-errors"></a>Errori di input dell'utente

- **Quando possibile, impedire o ridurre gli errori di input dell'utente tramite:**
  - Uso di controlli vincolati a valori validi.
  - Se si disabilitano i controlli e le voci di menu quando si fa clic, si verifica un errore, purché sia evidente il motivo per cui il controllo o la voce di menu è disabilitata.
  - Fornire valori predefiniti validi.

**Non corretto:**

![Screenshot della casella di testo con l'etichetta del volume del parlante ](images/mess-error-image35.png)

In questo esempio viene usata una casella di testo senza vincoli per l'input vincolato. Usare invece un dispositivo di scorrimento.

- **Usare la gestione degli errori non modali (errori sul posto o fumetto) per i problemi di input contestuale dell'utente.**
- **Usare i palloncino per** i problemi di input utente non critici rilevati in una casella di testo o immediatamente dopo che una casella di testo perde lo stato attivo. [I fumetto](https://msdn.microsoft.com/library/windows/desktop/aa511451.aspx) non richiedono lo spazio disponibile sullo schermo o il layout dinamico necessario per visualizzare i messaggi sul posto. Consente di visualizzare un solo fumetto alla volta. Poiché il problema non è critico, non è necessaria alcuna icona di errore. I palloncino vengono visualizzati quando si fa clic, quando il problema viene risolto o dopo un timeout.

![Screenshot del messaggio: carattere non corretto ](images/mess-error-image36.png)

In questo esempio, un fumetto indica un problema di input mentre è ancora nel controllo .

- Usare gli errori sul posto per il rilevamento degli errori **ritardati,** in genere gli errori rilevati facendo clic su un pulsante di commit. Non usare errori [sul posto per](glossary.md) le impostazioni di cui viene eseguito immediatamente il commit. Possono essere presenti più errori sul posto contemporaneamente. Usare testo normale e un'icona di errore di 16x16 pixel, posizionandoli direttamente accanto al problema, quando possibile. Gli errori sul posto non vengono visualizzati a meno che l'utente non eserciti il commit e non vengano trovati altri errori.

![Screenshot del messaggio: indirizzo di posta elettronica non corretto ](images/mess-error-image37.png)

In questo esempio viene usato un errore sul posto per un errore rilevato facendo clic sul pulsante commit.

- Usare la gestione degli errori modale (finestre di dialogo attività o finestre di messaggio) per tutti gli altri **problemi,** inclusi gli errori che coinvolgono più controlli o sono errori non contestuali o non di input trovati facendo clic su un pulsante di commit.
- **Quando viene segnalato un problema di input dell'utente, impostare lo stato attivo per l'input sul primo controllo con i dati non corretti.** Scorrere il controllo nella visualizzazione, se necessario. Se il controllo è una casella di testo, selezionare l'intero contenuto. Dovrebbe essere sempre ovvio a cosa fa riferimento il messaggio di errore.
- **Non cancellare l'input non corretto.** Lasciare invece in modo che l'utente possa visualizzare e correggere il problema senza ricominciare.
  - **Eccezione:** Deselezionare le caselle di testo password e PIN non corrette perché gli utenti non possono correggere l'input mascherato in modo efficace.

### <a name="troubleshooting"></a>Risoluzione dei problemi

- **Evitare di creare problemi di risoluzione dei problemi.** Non affidarsi a un singolo messaggio di errore per segnalare un problema con diverse cause rilevabili.
- **Usare un messaggio di errore diverso (in genere un'istruzione supplementare diversa) per ogni causa rilevabile.** Ad esempio, se un file non può essere aperto per diversi motivi, fornire un'istruzione supplementare separata per ogni motivo.
- **Usare un messaggio con più cause solo quando non è possibile determinare la causa specifica.** In questo caso, presentare le soluzioni in ordine di probabilità di risolvere il problema. In questo modo, gli utenti possono risolvere il problema in modo più efficiente.

### <a name="icons"></a>Icone

- **Le finestre di dialogo modali dei messaggi di errore non hanno icone della barra del titolo.** Le icone della barra del titolo vengono usate come distinzione visiva tra le finestre primarie e le finestre secondarie.
- **Usare un'icona di errore.** Eccezioni:
  - Se l'errore è un problema di input dell'utente visualizzato tramite una finestra di dialogo modale o un fumetto, non usare un'icona. Questa operazione è in contrasto con il tono incoraggiante Windows. Tuttavia, i messaggi di errore sul posto devono usare una piccola icona di errore (16x16 pixel) per identificarli chiaramente come messaggi di errore.

     ![Screenshot del messaggio in formato postale non corretto](images/mess-error-image38.png)

     ![Screenshot del nome computer del messaggio troppo lungo](images/mess-error-image39.png)

     In questi esempi, i problemi di input dell'utente non necessitano di icone di errore.

     ![Screenshot del formato errato del numero di telefono del messaggio](images/mess-error-image40.png)

     In questo esempio, un messaggio di errore sul posto richiede una piccola icona di errore per identificarlo chiaramente come messaggio di errore.

- Se il problema si verifica per una funzionalità con un'icona (e non un problema di input dell'utente), è possibile usare l'icona della funzionalità con una sovrapposizione degli errori. In questo caso, usare anche il nome della funzionalità come oggetto dell'errore.

    ![Screen shot message media player can't play file (Impossibile riprodurre il file) ](images/mess-error-image41.png)

    In questo esempio l'icona della funzionalità ha una sovrapposizione di errori e la funzionalità è l'oggetto dell'errore.

- **Non usare icone di avviso per gli errori.** Questa operazione viene spesso eseguita per rendere la presentazione meno grave. Gli errori non sono avvisi.

    **Non corretto:**

    ![Screenshot del cambio rapido del messaggio non abilitato ](images/mess-error-image42.png)

    In questo esempio, un'icona di avviso viene usata erroneamente per rendere l'errore meno grave.

Per altre linee guida ed esempi, vedere [Icone standard.](vis-std-icons.md)

### <a name="progressive-disclosure"></a>Rivelazione progressiva

- **Usare un pulsante Mostra/Nascondi informazioni di divulgazione progressiva dei dettagli per nascondere informazioni avanzate o dettagliate in un messaggio di errore.** In questo modo il messaggio di errore viene semplificato per l'utilizzo tipico. Non nascondere le informazioni necessarie, perché gli utenti potrebbero non trovarle.

![Screenshot del messaggio: ActiveSync non può accedere ](images/mess-error-image43.png)

In questo esempio, il pulsante di divulgazione progressiva consente agli utenti di eseguire il drill-down in modo più dettagliato, se lo vogliono, o semplificare l'interfaccia utente in caso contrario.

- **Non usare Mostra/Nascondi dettagli a meno che non siano presenti dettagli più dettagliati.** Non è sufficiente ripristinare le informazioni esistenti in un formato più dettagliato.
- **Non usare Mostra/Nascondi dettagli per visualizzare le informazioni della Guida.** Usare invece i collegamenti della Guida.

Per le linee guida sull'etichettatura, vedere [Controlli di diffusione progressiva](ctrl-progressive-disclosure-controls.md).

**Non visualizzare più questo messaggio**

- **Se un messaggio di errore richiede questa opzione, riconsiderare l'errore e la relativa frequenza.** Se ha tutte le caratteristiche di un buon errore (pertinente, utilizzabile e poco comune), non dovrebbe avere senso per gli utenti di sopprimerlo.

Per altre linee guida, vedere [Finestre di dialogo](win-dialog-box.md).

### <a name="default-values"></a>Valori predefiniti

- **Selezionare la risposta più sicura, meno distruttiva o più sicura come predefinita.** Se la sicurezza non è un fattore importante, selezionare il comando più probabile o pratico.

### <a name="help"></a>Help

- **Progettare i messaggi di errore per evitare la necessità di aiuto.** In genere gli utenti non devono leggere testo esterno per comprendere e risolvere il problema, a meno che la soluzione non richieda diversi passaggi.
- **Assicurarsi che il contenuto della Guida sia pertinente e utile.** Non deve essere una riepilogazione dettagliata del messaggio di errore, ma deve contenere informazioni utili oltre l'ambito del messaggio di errore, ad esempio modi per evitare il problema in futuro. Non fornire un collegamento alla Guida solo perché è possibile.
- **Usare collegamenti della Guida specifici, concisi e pertinenti per accedere al contenuto della Guida.** Non usare pulsanti di comando o divulgazione progressiva a questo scopo.
- **Per i messaggi di errore che non è possibile rendere specifici e utilizzabili, valutare la possibilità di fornire collegamenti al contenuto della Guida online.** In questo modo, è possibile fornire agli utenti informazioni aggiuntive che è possibile aggiornare dopo il rilascio del programma.

Per altre linee guida, vedere [la Guida](winenv-help.md).

### <a name="error-codes"></a>Codici di errore

- **Per i messaggi di errore che non è possibile rendere specifici e utilizzabili o che traggono vantaggio dalla Guida, prendere in considerazione anche l'invio di codici di errore.** Gli utenti usano spesso questi codici di errore per cercare informazioni aggiuntive in Internet.
- **Fornire sempre una descrizione testuale del problema e della soluzione.** Non dipendere solo dal codice di errore a questo scopo.

**Non corretto:**

![Screenshot del messaggio: Impossibile aprire il file ](images/mess-error-image44.png)

In questo esempio viene usato un codice di errore come sostituzione del testo di una soluzione.

- **Assegnare un codice di errore univoco per ogni causa diversa.** In questo modo si evita la risoluzione dei problemi.
- **Scegliere i codici di errore facilmente ricercabili in Internet.** Se si usano codici a 32 bit, usare una rappresentazione esadecimale con uno "0x" iniziale e caratteri maiuscoli.

**Corretto:**

1234

0xC0001234

**Non corretto:**

-1

-67113524

- **Usare Mostra/Nascondi dettagli per visualizzare i codici di errore.** Frase come codice di errore: <error code> .

![Screenshot del messaggio: programma non inizializzato ](images/mess-error-image45.png)

In questo esempio viene usato un codice di errore per integrare un messaggio di errore che può trarre vantaggio da altre informazioni.

### <a name="sound"></a>Suoni

- **Non accompagnare i messaggi di errore con un effetto sonoro o un segnale acustico.** Questa operazione è inasserente e non necessaria.
  - **Eccezione:** Riprodurre l'effetto audio Arresto critico se il problema è critico per il funzionamento del computer e l'utente deve intervenire immediatamente per evitare conseguenze gravi.

## <a name="text"></a>Testo

**Generale**

- **Rimuovere il testo ridondante.** Cercarlo in titoli, istruzioni principali, istruzioni supplementari, collegamenti ai comandi e pulsanti di commit. In genere, lasciare il testo completo nelle istruzioni e nei controlli interattivi e rimuovere la ridondanza dalle altre posizioni.
- **Usare spiegazioni centrate sull'utente.** Descrivere il problema in termini di azioni o obiettivi dell'utente, non in termini di ciò che il software non è soddisfatto. Usare il linguaggio che gli utenti di destinazione comprendono e usano. Evitare il gergo tecnico.

**Non corretto:**

![Screenshot del messaggio: input-synchronous call ](images/mess-error-image46.png)

**Corretto:**

![Screenshot del messaggio: occupato a ricevere una chiamata ](images/mess-error-image47.png)

In questi esempi, la versione corretta parla la lingua dell'utente, mentre la versione non corretta è troppo tecnica.

- **Non usare le parole seguenti:**
  - Errore, errore (usare invece il problema)
  - Non riuscito (non è possibile usare in alternativa)
  - Non valido, non valido, non valido (usare invece non corretto)
  - Abort, kill, terminate (usare stop)
  - Irreversibile, irreversibile (usare invece grave)

Questi termini non sono necessari e contrariamente al tono incoraggiante Windows. Se [usata correttamente,](vis-std-icons.md)l'icona di errore comunica sufficientemente che si è verificato un problema.

**Non corretto:**

![Screenshot del messaggio: errore irreversibile. ](images/mess-error-image48.png)

**Corretto:**

![Screenshot del messaggio: Il backup deve essere chiuso contemporaneamente ](images/mess-error-image49.png)

Nell'esempio errato, i termini "irreversici" e "errore" non sono necessari.

- Non usare formulazioni che incolpano l'utente o implicano un errore dell'utente. Evitare di usare l'utente e nella formulazione. Anche se la voce attiva è generalmente preferita, usare la voce passiva quando l'utente è il soggetto e potrebbe essere incolpata per l'errore se è stata usata la voce attiva.

**Non corretto:**

![screenshot del messaggio immesso come accesso non corretto ](images/mess-error-image50.png)

**Corretto:**

![Screenshot del messaggio: password non corretta ](images/mess-error-image51.png)

L'esempio non corretto incolpa l'utente usando la voce attiva.

- **Essere specifici.** Evitare formulazioni erre, ad esempio errori di sintassi e operazioni non valida. Specificare nomi, posizioni e valori specifici degli oggetti coinvolti.

**Non corretto:**

File non trovato.

Disco pieno.

Valore non compreso nell'intervallo.

Il carattere non è valido.

Dispositivo non disponibile.

Questi problemi sarebbero molto più semplici da risolvere con nomi, posizioni e valori specifici.

- **Non fornire possibili problemi, cause o soluzioni improbabili nel tentativo di essere specifici.** Non fornire un problema, una causa o una soluzione a meno che non sia probabilmente la scelta giusta. Ad esempio, è meglio dire Che si è verificato un errore sconosciuto rispetto a un elemento che probabilmente non è accurato.
- **Evitare la parola "per favore",** tranne nelle situazioni in cui all'utente viene richiesto di eseguire un'operazione poco pratico (ad esempio in attesa) o il software è responsabile della situazione.

**Corretto:**

Attendere che Windows copia i file nel computer.

- **Usare la parola "sorry"** solo nei messaggi di errore che causano gravi problemi per l'utente, ad esempio la perdita di dati o l'impossibilità di usare il computer. Non ci si deve chiedere se il problema si è verificato durante il normale funzionamento del programma( ad esempio, se l'utente deve attendere che sia trovata una connessione di rete).

**Corretto:**

Il servizio Backup di Fabrikam ha rilevato un problema irreversibile ed è stato arrestato per proteggere i file nel computer.

- **Fare riferimento ai prodotti usando i nomi brevi.** Non usare nomi di prodotti completi o simboli di marchio. Non includere il nome della società a meno che gli utenti non assortino il nome della società al prodotto. Non includere i numeri di versione del programma.

**Non corretto:**

![Screenshot che mostra un Microsoft Office Outlook messaggio "Non è possibile aprire questo elemento". ](images/mess-error-image52.png)

**Corretto:**

![Screenshot del messaggio: Non è possibile aprire questo elemento ](images/mess-error-image53.png)

Nell'esempio non corretto vengono usati i nomi completi dei prodotti e i simboli dei marchi.

- **Usare le virgolette doppie per i nomi degli oggetti.** In questo modo il testo risulta più facile da analizzare ed evita le istruzioni potenzialmente imbarazzanti.
  - **Eccezione:** I percorsi di file completi, gli URL e i nomi di dominio non devono essere racchiusi tra virgolette doppie.

**Corretto:**

![Screenshot del messaggio: "la mia casa" non è disponibile ](images/mess-error-image54.png)

In questo esempio, il messaggio di errore potrebbe generare confusione se il nome dell'oggetto non fosse racchiuso tra virgolette.

- **Evitare di iniziare frasi con nomi di oggetto.** Questa operazione è spesso difficile da analizzare.
- **Non usare punti esclamativi o parole con tutte lettere maiuscole.** I punti esclamativi e le lettere maiuscole fanno in modo che l'utente si diffondono.

Per altre linee guida ed esempi, vedere [Stile e tono.](text-style-tone.md)

**Titoli**

- **Usare il titolo per identificare il comando o la funzionalità da cui ha avuto origine l'errore.** Eccezioni:
  - Se un errore viene visualizzato da molti comandi diversi, prendere in considerazione l'uso del nome del programma.
  - Se il titolo sarebbe ridondante o confondere con l'istruzione principale, usare invece il nome del programma.
- **Non usare il titolo per spiegare o riepilogare il problema** che è lo scopo dell'istruzione principale.

**Non corretto:**

![Screenshot che mostra il messaggio "Non è possibile rinominare una nuova cartella". ](images/mess-error-image55.png)

In questo esempio il titolo viene usato in modo non corretto per spiegare il problema.

- Usare l'iniziale maiuscola in stile titolo, senza terminare la punteggiatura.

**Istruzioni principali**

- **Usare l'istruzione principale per descrivere il problema in un linguaggio chiaro, semplice e specifico.**
- **Usare concisa una sola frase completa.** Si può trovare l'istruzione principale fino alle informazioni essenziali. È possibile lasciare implicito l'oggetto se si tratta del programma o dell'utente. Includere il motivo del problema se è possibile farlo in modo conciso. Se è necessario spiegare altro, usare un'istruzione supplementare.

**Non corretto:**

![Screenshot del messaggio: Non è possibile installare l'aggiornamento ](images/mess-error-image56.png)

In questo esempio, l'intero messaggio di errore viene inserito nell'istruzione principale, rendendo difficile la lettura.

- **Se sono presenti oggetti coinvolti, specificarne i nomi.**
- **Evitare di inserire percorsi di file completi e URL nell'istruzione principale.** Usare invece un nome breve, ad esempio il nome del file, e inserire il nome completo (ad esempio il percorso del file) nell'istruzione supplementare. Tuttavia, è possibile inserire un singolo url o percorso di file completo nell'istruzione principale se il messaggio di errore non richiede un'istruzione supplementare.

![Screenshot del messaggio: non è possibile eliminare il file fabrikam ](images/mess-error-image57.png)

In questo esempio solo il nome del file si trova nell'istruzione principale. Il percorso completo si trova nell'istruzione supplementare.

- **Non fornire il percorso completo del file e l'URL se è ovvio dal contesto.**

![Screenshot del messaggio: Non è possibile rinominare una nuova cartella ](images/mess-error-image58.png)

In questo esempio l'utente rinomina un file da Windows Explorer. In questo caso, il percorso completo del file non è necessario perché è ovvio dal contesto.

- Usare il tempo presente quando possibile.
- Usare le maiuscole/minuscole come nelle frasi comuni.
- Non includere i periodi finali se l'istruzione è un'istruzione . Se l'istruzione è una domanda, includere un punto interrogativo finale.

**Modelli di istruzioni principali**

Anche se non esistono regole rigide per la formulazione, provare a usare i modelli di istruzioni principali seguenti quando possibile:

- [nome soggetto facoltativo] non può [eseguire un'azione]
- [nome soggetto facoltativo] non può [eseguire l'azione] perché [motivo]
- [nome soggetto facoltativo] non può [eseguire l'azione] su "[nome oggetto]"
- [nome soggetto facoltativo] non può [eseguire l'azione] su "[nome oggetto]" perché [motivo]
- [risorsa] non è sufficiente per [eseguire un'azione]
- [Nome soggetto] non ha un [nome oggetto] obbligatorio per [scopo]
- [Dispositivo o impostazione] è disattivato in modo che [risultati indesiderati]
- [Dispositivo o impostazione] non è [disponibile \| trovato \| attivato \| abilitato]
- "[nome oggetto]" non è attualmente disponibile
- Il nome utente o la password non è corretta
- Non si dispone dell'autorizzazione per accedere a "[nome oggetto]"
- Non si ha il privilegio di [eseguire un'azione]
- [nome programma] ha riscontrato un problema grave e deve chiudersi immediatamente

Naturalmente, apportare le modifiche necessarie perché l'istruzione principale sia grammaticalmente corretta e conforme alle linee guida per le istruzioni principali.

**Istruzioni supplementari**

- Usare l'istruzione supplementare per:
  - Fornire dettagli aggiuntivi sul problema.
  - Spiegare la causa del problema.
  - Elencare i passaggi che l'utente può eseguire per risolvere il problema.
  - Fornire misure per evitare che il problema si ripeta.
- **Quando possibile, proporre una soluzione pratica e utile in modo che gli utenti possano risolvere il problema.** Assicurarsi tuttavia che la soluzione proposta risolva il problema. Non sprecare il tempo degli utenti suggerendo soluzioni possibili, ma improbabili.

**Non corretto:**

![Screenshot del messaggio: memoria insufficiente ](images/mess-error-image59.png)

In questo esempio, sebbene il problema e la soluzione consigliata siano possibili, è molto improbabile.

- **Se il problema è un valore non corretto immesso dall'utente, usare l'istruzione supplementare per spiegare i valori corretti.** Gli utenti non devono determinare queste informazioni da un'altra origine.
- **Non fornire una soluzione se può essere dedotta in modo semplice dall'istruzione del problema.**

![Screenshot del messaggio: valore di ora non corretto ](images/mess-error-image33.png)

In questo esempio non è necessaria alcuna istruzione supplementare. la soluzione può essere dedotta in modo semplice dall'istruzione del problema.

- **Se la soluzione include più passaggi, presentare i passaggi nell'ordine in cui devono essere completati.** Evitare tuttavia soluzioni in più passaggi perché gli utenti hanno difficoltà a ricordare più di due o tre semplici passaggi. Se sono necessari altri passaggi, fare riferimento all'argomento della Guida appropriato.
- **Mantenere le istruzioni supplementari concise.** Fornire solo ciò che gli utenti devono sapere. Omettere i dettagli non necessari. Puntare a un massimo di tre frasi di lunghezza moderata.
- **Per evitare errori mentre gli utenti eseguono istruzioni, inserire i risultati prima dell'azione.**

**Corretto:**

Per riavviare Windows, fare clic su OK.

**Non corretto:**

Fare clic su OK per riavviare Windows.

Nell'esempio non corretto, è più probabile che gli utenti clicno su OK per errore.

- **Non è consigliabile contattare un amministratore, a meno che questa operazione non sia una delle soluzioni più probabili al problema.** Riservare soluzioni di questo tipo per problemi che possono essere risolti solo da un amministratore.

**Non corretto:**

![Screenshot del messaggio: Server non disponibile ](images/mess-error-image60.png)

In questo esempio, molto probabilmente il problema è relativo alla connessione di rete dell'utente, quindi non vale la pena contattare un amministratore.

- **Non è consigliabile contattare il supporto tecnico.** L'opzione per contattare il supporto tecnico per risolvere un problema è sempre disponibile e non deve essere promossa tramite messaggi di errore. Concentrarsi invece sulla scrittura di messaggi di errore utili in modo che gli utenti possano risolvere i problemi senza contattare il supporto tecnico.

**Non corretto:**

![Screenshot che mostra il messaggio "Non è possibile aprire questo elemento". ](images/mess-error-image61.png)

In questo esempio, il messaggio di errore consiglia erroneamente di contattare il supporto tecnico.

- Usare frasi complete, lettere maiuscole in stile frase e punteggiatura finale.

**Pulsanti di commit**

- Se il messaggio di errore fornisce pulsanti di comando o collegamenti di comando che risolvono il problema, seguire le rispettive linee guida in [Finestre di dialogo](win-dialog-box.md).
- Se il programma deve terminare in seguito all'errore, specificare un pulsante Esci dal programma. Per evitare confusione, non usare Chiudi a questo scopo.
- In caso contrario, specificare un pulsante Chiudi. Non usare OK per i messaggi di errore, perché questa formulazione implica che i problemi sono ok.
  - **Eccezione:** Usare OK se il meccanismo di segnalazione degli errori ha etichette fisse (come con l'API MessageBox).

## <a name="documentation"></a>Documentazione

Quando si fa riferimento agli errori:

- Fare riferimento agli errori in base all'istruzione principale. Se l'istruzione principale è lunga o dettagliata, riepilogarla.
- Se necessario, è possibile fare riferimento a una finestra di dialogo di messaggio di errore come messaggio. Fare riferimento a come messaggio di errore solo nella programmazione e in altre documentazione tecnica.
- Quando possibile, formattare il testo usando il grassetto. In caso contrario, inserire il testo tra virgolette solo se necessario per evitare confusione.

**Esempio:** Se viene visualizzato il messaggio Non è presente alcun **disco CD** nel messaggio dell'unità, inserire un nuovo disco CD nell'unità e riprovare.
