---
title: Palloncini
description: Un balloon è una piccola finestra popup che informa gli utenti di un problema non critico o di una condizione speciale in un controllo.
ms.assetid: 67092831-e573-4ad6-b1fc-baa1836031cb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 792974ebaaa946a3e1a4f05d52c8fd9ac32fc87a
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524555"
---
# <a name="balloons"></a>Palloncini

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Un balloon è una piccola finestra popup che informa gli utenti di un problema non critico o di una condizione speciale in un controllo.

![Screenshot che mostra un fumetto che indica che BLOC MAIUSC è on.](images/ctrl-balloons-image1.png)

Un balloon tipico.

I balloon hanno un'icona, un titolo e il testo del corpo, tutti facoltativi. A differenza delle descrizioni comando e delle descrizioni comandi, i balloon hanno anche una coda che ne identifica l'origine. In genere l'origine è un controllo , se sì, viene definito controllo [proprietario](glossary.md).

Anche se i balloon segnalano agli utenti problemi non critici, non impediscono problemi anche se il controllo del proprietario potrebbe. Eventuali problemi non gestiti devono essere gestiti dall'interfaccia utente del proprietario quando gli utenti tentano di eseguire il commit all'azione.

I balloon vengono in genere usati con caselle di testo o controlli che usano caselle di testo per modificare i valori, ad esempio caselle combinate, visualizzazioni elenco e visualizzazioni albero. Altri tipi di controlli sono sufficientemente vincolati e non necessitano dei balloon di feedback aggiuntivi. Inoltre, se si verifica un problema con altri tipi di controlli, spesso comporta incoerenze tra più controlli in una situazione in cui i balloon non sono adatti. Solo i controlli di immissione di testo sono sia senza vincoli che un'origine comune di [errori a punto singolo.](glossary.md)

Una notifica è un tipo specifico di fumetto visualizzato da un'icona [dell'area di](winenv-notification.md) notifica.

**Nota:** Le linee guida [relative a notifiche,](mess-notif.md) [descrizioni](ctrl-tooltips-and-infotips.md)comando e suggerimenti e messaggi [di](mess-error.md) errore sono presentate in articoli separati.

**È il controllo giusto?**

Per decidere, prendi in considerazione queste domande:

-   **Le informazioni descrivono un problema o una condizione speciale?** Se non è così, usa un altro controllo. Non usare i balloon per visualizzare informazioni supplementari per un controllo. È [consigliabile usare testo](glossary.md)statico,[suggerimenti,](glossary.md) [divulgazione progressiva](glossary.md)o prompt.
-   **Il problema o la condizione speciale può essere rilevata immediatamente** all'input o quando il controllo proprietario perde lo stato attivo per l'input? In caso contrario, usare un messaggio di errore visualizzato in una finestra [di dialogo attività o](glossary.md) in una finestra di [messaggio](glossary.md).
-   **Per i problemi, il problema è critico?** In tal caso, usare un messaggio di errore visualizzato in una finestra di dialogo attività o in una finestra di messaggio. Tali messaggi di errore richiedono l'interazione (adatta per gli errori critici), mentre i balloon non lo richiedono.
-   **Per condizioni speciali, la condizione è valida ma probabilmente non intenzionale?** In tal caso, i balloon sono appropriati. Per condizioni non valide, è meglio prevenirle in primo luogo. Per le condizioni probabili, non è necessario eseguire alcuna operazione.
-   **Il problema o la condizione speciale può essere espressa in modo conciso?** Se non è così, usa un altro controllo. I balloon non possono avere spiegazioni dettagliate o fornire informazioni supplementari.
-   **Le informazioni descrivono il controllo su cui è attualmente in corso il passaggio del mouse?** In tal caso, usare invece un suggerimento, a meno che gli utenti non necessitino di interagire con il messaggio.
-   **Le informazioni sono correlate all'attività corrente dell'utente?** In caso contrario, è consigliabile usare [una notifica o](mess-notif.md) una finestra di [dialogo.](win-dialog-box.md) È probabile che gli utenti tralasciano i balloon al di fuori dell'attività corrente e, per impostazione predefinita, il timeout dei balloon dopo 10 secondi.
-   **Le informazioni provengono da una singola origine specifica?** Se un problema o una condizione ha più origini o nessuna origine specifica, [usare invece un messaggio](glossary.md) sul posto o una finestra di dialogo.

**Risposta errata:** ![ Screenshot di un balloon: accesso non riuscito](images/ctrl-balloons-image2.png)

In questo esempio, il problema potrebbe essere relativo al nome utente o alla password, ma la segnalazione del problema con un balloon suggerisce visivamente che solo la password è il problema. Di conseguenza, il feedback dell'immissione di un nome utente errato è fuorviante.

I balloon sono un'alternativa alle descrizioni comandi, alle finestre di dialogo e ai messaggi sul posto. A differenza delle descrizioni comando e delle descrizioni comandi:

-   I balloon possono essere visualizzati indipendentemente dalla posizione corrente del puntatore, quindi hanno una coda che ne indica l'origine.
-   I fumetto hanno un titolo, il testo del corpo e un'icona.
-   I balloon possono essere interattivi, mentre non è possibile fare clic su un suggerimento.

A differenza delle finestre di dialogo modali:

-   I balloon non rubano lo stato attivo per l'input né richiedono l'interazione.
-   I balloon identificano una singola origine specifica. Le finestre di dialogo modali possono avere più origini o nessuna origine specifica.

A differenza dei messaggi sul posto:

-   I balloon sono più evidenti.
-   I balloon non richiedono lo spazio disponibile sullo schermo o il layout dinamico necessario per visualizzare i messaggi sul posto.
-   I balloon si rimuovono automaticamente dopo un timeout.

**Modelli di utilizzo**

I balloon hanno questi modelli di utilizzo:



|   Utilizzo                                                                                                                                                            |    Esempio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Problema di input** Un problema di input utente non critico proveniente da un singolo controllo proprietario, in genere una casella di testo. <br/>                                               | L'uso di balloon per i messaggi di errore non sottrae lo stato attivo per l'input, ma è ancora molto evidente se il controllo proprietario ha lo stato attivo per l'input. per correggere il problema, potrebbe essere necessario modificare o immettere nuovamente l'input. tuttavia, se il controllo proprietario ignora l'input non corretto, l'utente potrebbe non essere necessario apportare alcuna modifica. Poiché il problema non è critico, non è necessaria [alcuna icona](vis-std-icons.md) di errore. <br/> ![Screenshot che mostra un fumetto che indica un carattere non corretto.](images/ctrl-balloons-image3.png)<br/> Balloon usato per segnalare un problema di input utente non critico.<br/>                                                                                                  |
| **Condizione speciale** Il controllo proprietario si trova in uno stato che influisce sull'input. Questo stato è probabilmente imprevisto e l'utente potrebbe non rendersi conto che l'input è interessato. <br/> | usare i balloon per evitare frustrazioni avvisando gli utenti di condizioni speciali non appena si verificano (ad esempio, superando le dimensioni massime di input o impostando il blocco dei limiti per errore). È importante fornire commenti e suggerimenti senza sottrarre lo stato attivo all'input o forzare l'interazione perché queste condizioni potrebbero essere intenzionali. Questi balloon sono particolarmente importanti per le caselle password e pin, in cui gli utenti stanno lavorando con un feedback minimo. Questi balloon hanno [un'icona di avviso](vis-std-icons.md). <br/> ![Screenshot che mostra i fumetto che indicano che BLOC MAIUSC è on e viene immesso un carattere non corretto.](images/ctrl-balloons-image4.png)<br/> Balloon utilizzato per segnalare una condizione speciale.<br/> |



 

**Linee guida**

**Quando visualizzare**

-   **Visualizzare il balloon non appena viene rilevato il problema o una condizione speciale, anche se ripetutamente, senza alcun ritardo evidente.**
    -   Per i problemi relativi a singoli caratteri o alle dimensioni massime di input, visualizzare il balloon immediatamente all'input.
    -   Per i problemi relativi al valore di input(inclusa la richiesta di un valore non vuoto), visualizzare il balloon quando il controllo proprietario perde lo stato attivo per l'input. In caso contrario, la visualizzazione di balloon mentre gli utenti immettono input potenzialmente validi può essere fonte di distrazione e di distrazione.
-   **Visualizzare un solo fumetto alla volta.** La visualizzazione di più balloon può essere esente. Se un singolo evento comporta più problemi, presenta tutti i problemi contemporaneamente o segnala solo il problema più importante.

**Risposta errata:** ![ Screenshot di due balloon che puntano a una casella](images/ctrl-balloons-image5.png)

In questo esempio due problemi vengono presentati in modo errato contemporaneamente.

**Per quanto tempo visualizzare**

-   **Rimuovere un balloon quando:**
    -   Il problema viene risolto o viene rimossa una condizione speciale.
    -   L'utente immette dati validi (per problemi di input).
    -   Timeout del balloon. Per impostazione predefinita, i balloon vengono rimuovono se stessi dopo 10 secondi, anche se gli utenti possono modificare questa impostazione modificando il parametro di sistema SPI \_ MESSAGEDURATION.
-   **Rimuovere il timeout se gli utenti non possono continuare fino a quando il problema non viene risolto. Sviluppatori:** in Win32 è possibile impostare l'ora di visualizzazione con il messaggio \_ TTM SETDELAYTIME.

**Come visualizzare**

-   **Visualizzare i balloon sotto il controllo proprietario.** In questo modo gli utenti possono visualizzare il contesto, inclusi il controllo proprietario e la relativa etichetta. Microsoft Windows regola automaticamente le posizioni del fumetto in modo che siano completamente visualizzate sullo schermo. Il comportamento predefinito è la visualizzazione di un fumetto sopra il relativo controllo proprietario, come avviene con le notifiche.

**Risposta corretta:** ![ screenshot di un fumetto visualizzato sotto il relativo controllo](images/ctrl-balloons-image6.png)

**Risposta errata:** ![ screenshot di un fumetto visualizzato sopra il relativo controllo](images/ctrl-balloons-image7.png)

Nell'esempio non corretto, il balloon viene visualizzato in modo non corretto sopra il relativo controllo proprietario.

**Caselle di testo per password e PIN**

-   **Usare un fumetto per indicare che BLOC MAIUSC è su**, usando il testo nell'esempio seguente:

![Screenshot di un fumetto che indica che il blocco con estremità è on](images/ctrl-balloons-image8.png)

In questo esempio, un fumetto indica che BLOC MAIUSC è selezionato in una casella di testo PIN.

-   **Usare un balloon per indicare quando gli utenti tentano di superare le dimensioni massime di input.** Il raggiungimento delle dimensioni massime di input è molto meno ovvio nelle caselle di testo per password e PIN rispetto alle normali caselle di testo.

![Screenshot di un fumetto che indica i limiti del codice pin](images/ctrl-balloons-image9.png)

In questo esempio, un balloon indica che l'utente sta tentando di superare le dimensioni massime di input.

-   **Usare un fumetto per indicare quando gli utenti immettere caratteri non corretti.** Tuttavia, è meglio non avere tali restrizioni perché riducono la sicurezza della password o del PIN. Per impedire la divulgazione di informazioni, il balloon deve menzionare solo i fatti documentati relativi a password o PIN validi.

![Screenshot di un balloon che indica un input non corretto](images/ctrl-balloons-image10.png)

In questo esempio, un fumetto indica che il PIN richiede numeri.

**Altre caselle di testo**

-   **È consigliabile usare un fumetto per indicare quando gli utenti tentano di superare le dimensioni massime di input per le caselle di testo brevi critiche destinate agli utenti non esperti.** Ad esempio, i nomi utente e i nomi degli account. Le caselle di testo esigono un segnale acustico quando gli utenti tentano di superare l'input massimo, ma gli utenti non esperti potrebbero non comprendere il significato del segnale acustico.

![Screenshot di un fumetto che indica i limiti dei caratteri](images/ctrl-balloons-image11.png)

In questo esempio, un balloon indica che l'utente ha tentato di superare le dimensioni massime di input.

**Interazione**

-   **Quando gli utenti fa clic su un fumetto, è sufficiente chiudere il fumetto senza visualizzare altre interfaccia utente o avere altri effetti collaterali.** A differenza delle notifiche, i balloon non devono avere pulsanti di chiusura.

**Icone**

-   Scegliere l'icona in base al modello di utilizzo:



    |  Modello |  Icona                                                                                                                                                       |
    ------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Problema di input | Nessuna icona. L'uso di [un'icona di errore](vis-std-icons.md) in questo caso è coerente con le linee guida [per il tono di Windows.](text-style-tone.md) |
    | Condizione speciale | Icona di avviso standard da 16x16 [pixel](vis-std-icons.md).                                                                                  |

**Accessibilità**

Se usati correttamente, i balloon migliorano l'accessibilità. Per l'accessibilità dei balloon:

-   Visualizzano solo i balloon correlati all'attività corrente dell'utente.
-   Mantenere conciso il testo del fumetto. In questo modo il testo del fumetto risulta più facile da leggere per gli utenti con problemi di vista e riduce al minimo l'interruzione durante la lettura da parte delle utilità per la lettura dello schermo.
-   Visualizzare nuovamente il balloon ogni volta che si verifica il problema o la condizione.

**Text**

**Testo titolo**

-   **Usare il testo del titolo che riepiloga brevemente il problema di input o una condizione speciale in una lingua chiara, semplice, concisa e specifica.** Gli utenti devono essere in grado di comprendere lo scopo del balloon rapidamente e con il minimo sforzo.
-   **Usare frammenti di testo o frasi complete senza terminare la punteggiatura.**
-   **Usare le maiuscole/minuscole come nelle frasi comuni.** Per altre informazioni, vedere [il glossario](./glossary.md).
-   **Usare non più di 48 caratteri (in inglese) per supportare la localizzazione.** Il titolo ha una lunghezza massima di 63 caratteri e deve essere in grado di espandersi di almeno il 30% per supportare la localizzazione.

**Testo del corpo**

-   **Usare la prima frase del testo del corpo per definire il problema o la condizione in modo chiaramente pertinente per l'utente.** Non ripetere le informazioni nel titolo. Omettere questo valore se non c'è altro da aggiungere.
-   **Usare la seconda frase per specificare cosa può fare l'utente per risolvere il problema o ripristinare lo stato.** In base alle linee guida [stile](./text-style-tone.md) e tono, non è necessario usare la parola Please in questa istruzione. Inserire due interruzioni di riga tra la prima e la seconda frase.

![Screenshot di un fumetto con titolo e testo del corpo](images/ctrl-balloons-image12.png)

Questo esempio illustra il layout standard del testo a fumetto.

-   **Spiegare come risolvere il problema o ripristinare** lo stato anche se questa spiegazione è ovvia, ma omettere la ridondanza tra l'istruzione del problema e la relativa risoluzione. **Eccezioni:**
    -   Omettere la risoluzione se non può essere espressa concisamente o senza ridondanza significativa.
    -   Omettere la risoluzione se l'utente non ha nulla da fare, ad esempio quando i caratteri non corretti vengono ignorati.
-   **Usare frasi complete con punteggiatura finale.**
-   **Usare le maiuscole/minuscole come nelle frasi comuni.**
-   **Usare non più di 200 caratteri (in inglese) per supportare la localizzazione.** Il testo del corpo ha una lunghezza massima di 255 caratteri e deve essere in grado di espandersi di almeno il 30% per supportare la localizzazione.

**Documentazione**

Quando si fa riferimento ai balloon:

-   Usare il testo esatto del titolo, inclusa la relativa maiuscola.
-   Fare riferimento al componente come un balloon, non come notifica o avviso.
-   Quando possibile, formattare il testo del titolo usando il testo in grassetto. In caso contrario, inserire il titolo tra virgolette solo se necessario per evitare confusione.

