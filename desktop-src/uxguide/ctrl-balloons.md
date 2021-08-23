---
title: Palloncini
description: Un fumetto è una piccola finestra popup che informa gli utenti di un problema non critico o di una condizione speciale in un controllo.
ms.assetid: 67092831-e573-4ad6-b1fc-baa1836031cb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ea95eee6e745dc85dbe7cd354df0906b5df4a7870198fc662effd326c6fbaae9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119818697"
---
# <a name="balloons"></a>Palloncini

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Un fumetto è una piccola finestra popup che informa gli utenti di un problema non critico o di una condizione speciale in un controllo.

![Screenshot che mostra un fumetto che indica che BLOC MAIUSC è on.](images/ctrl-balloons-image1.png)

Un palloncino tipico.

I fumetto hanno un'icona, un titolo e il corpo del testo, tutti facoltativi. A differenza delle descrizioni comando e delle descrizioni comando, i palloncino hanno anche una coda che identifica l'origine. In genere l'origine è un controllo , in caso contrario, definito [controllo proprietario](glossary.md).

Sebbene i palloncino informino gli utenti di problemi non critici, non impediscono problemi anche se il controllo proprietario potrebbe. Eventuali problemi non gestiti devono essere gestiti dall'interfaccia utente del proprietario quando gli utenti tentano di eseguire il commit dell'azione.

I numeri di riferimento vengono in genere usati con caselle di testo o controlli che usano caselle di testo per modificare i valori, ad esempio caselle combinate, visualizzazioni elenco e visualizzazioni albero. Altri tipi di controlli sono sufficientemente vincolati e non necessitano dei pallonci di feedback aggiuntivi. Inoltre, se si verifica un problema con altri tipi di controlli, spesso comporta l'incoerenza tra più controlli in una situazione per cui i palloncini non sono adatti. Solo i controlli di immissione di testo sono sia senza vincoli che un'origine comune di [errori a punto singolo.](glossary.md)

Una notifica è un tipo specifico di fumetto visualizzato da un'icona [dell'area di](winenv-notification.md) notifica.

**Nota:** Le linee guida [relative a notifiche,](mess-notif.md) [descrizioni comando](ctrl-tooltips-and-infotips.md)e suggerimenti e messaggi [di errore](mess-error.md) vengono presentate in articoli separati.

**È il controllo giusto?**

Per decidere, prendi in considerazione queste domande:

-   **Le informazioni descrivono un problema o una condizione speciale?** Se non è così, usa un altro controllo. Non usare i fumetto per visualizzare informazioni supplementari per un controllo. è [consigliabile usare testo](glossary.md)statico,[infotip,](glossary.md) [divulgazione](glossary.md)progressiva o richieste.
-   **Il problema o la condizione speciale può essere rilevata immediatamente** all'input o quando il controllo proprietario perde lo stato attivo per l'input? In caso contrario, usare un messaggio di errore visualizzato in una finestra [di dialogo attività](glossary.md) o in una finestra di [messaggio](glossary.md).
-   **Per i problemi, il problema è critico?** In tal caso, usare un messaggio di errore visualizzato in una finestra di dialogo o in una finestra di messaggio dell'attività. Questi messaggi di errore richiedono l'interazione (adatta per gli errori critici), mentre i palloncini non lo sono.
-   **Per condizioni speciali, la condizione è valida ma probabilmente non intenzionale?** In tal caso, i palloncino sono appropriati. Per le condizioni non valide, è meglio evitarle in primo luogo. Per le condizioni probabili, non è necessario eseguire alcuna operazione.
-   **Il problema o la condizione speciale può essere espressa concisamente?** Se non è così, usa un altro controllo. I fumetto non possono avere spiegazioni dettagliate o fornire informazioni supplementari.
-   **Le informazioni descrivono il controllo su cui è attualmente in corso il passaggio del mouse?** In caso contrario, usare un suggerimento, a meno che gli utenti non possano dover interagire con il messaggio.
-   **Le informazioni sono correlate all'attività corrente dell'utente?** In caso contrario, è consigliabile usare una [notifica o](mess-notif.md) una finestra [di dialogo.](win-dialog-box.md) È probabile che gli utenti trascurino i palloncini al di fuori dell'attività corrente e, per impostazione predefinita, i palloncino si timeout dopo 10 secondi.
-   **Le informazioni provengono da una singola origine specifica?** Se un problema o una condizione ha più origini o nessuna origine specifica, usare invece un [messaggio](glossary.md) sul posto o una finestra di dialogo.

**Non corretto:** ![ Screenshot di un fumetto: accesso non riuscito](images/ctrl-balloons-image2.png)

In questo esempio il problema potrebbe essere relativo al nome utente o alla password, ma la segnalazione del problema con un fumetto suggerisce visivamente che solo la password è il problema. Di conseguenza, il feedback dell'immissione di un nome utente non corretto è fuorviante.

I fumetto sono un'alternativa a infotip, finestre di dialogo e messaggi sul posto. A differenza delle descrizioni comando e dei suggerimenti:

-   I palloncini possono essere visualizzati indipendentemente dalla posizione corrente del puntatore, quindi hanno una coda che ne indica l'origine.
-   I fumetto hanno un titolo, un corpo del testo e un'icona.
-   I palloncini possono essere interattivi, mentre è impossibile fare clic su una mancia.

A differenza delle finestre di dialogo modali:

-   I palloncini non rubano lo stato attivo per l'input o richiedono l'interazione.
-   I numeri di riferimento identificano una singola origine specifica. Le finestre di dialogo modali possono avere più origini o nessuna origine specifica.

A differenza dei messaggi sul posto:

-   I palloncini sono più evidenti.
-   I fumetto non richiedono lo spazio disponibile sullo schermo o il layout dinamico necessario per visualizzare i messaggi sul posto.
-   I palloncini si rimuovono automaticamente dopo un timeout.

**Modelli di utilizzo**

I palloncini hanno questi modelli di utilizzo:



|   Utilizzo                                                                                                                                                            |    Esempio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Problema di input** Un problema di input utente non critico proveniente da un singolo controllo proprietario, in genere una casella di testo. <br/>                                               | L'uso di fumetto per i messaggi di errore non ruba lo stato attivo per l'input, ma è ancora molto evidente se il controllo proprietario ha lo stato attivo per l'input. per correggere il problema, l'utente potrebbe essere necessario modificare o immettere nuovamente l'input. ma se il controllo proprietario ignora l'input non corretto, l'utente potrebbe non essere necessario apportare alcuna modifica. poiché il problema non è critico, non è necessaria [alcuna icona](vis-std-icons.md) di errore. <br/> ![Screenshot che mostra un fumetto che indica un carattere non corretto.](images/ctrl-balloons-image3.png)<br/> Un fumetto usato per segnalare un problema di input utente non critico.<br/>                                                                                                  |
| **Condizione speciale** Il controllo proprietario si trova in uno stato che influisce sull'input. Questo stato è probabilmente imprevisto e l'utente potrebbe non rendersi conto che l'input è interessato. <br/> | usare i palloncino per evitare frustrazione avvisando gli utenti di condizioni speciali non appena si verificano (ad esempio, il superamento delle dimensioni massime di input o l'impostazione dei limiti di blocco si bloccano per errore). è importante fornire un feedback di questo tipo senza sottrarre lo stato attivo all'input o forzare l'interazione perché queste condizioni potrebbero essere intenzionali. questi palloncino sono particolarmente importanti per le caselle di password e pin, in cui gli utenti altrimenti lavorano con commenti e suggerimenti minimi. questi fumetto hanno [un'icona di avviso](vis-std-icons.md). <br/> ![Screenshot che mostra i fumetto che indicano che BLOC MAIUSC è on e viene immesso un carattere non corretto.](images/ctrl-balloons-image4.png)<br/> Un fumetto usato per segnalare una condizione speciale.<br/> |



 

**Linee guida**

**Quando visualizzare**

-   **Visualizzare il fumetto non appena viene rilevato il problema o una condizione speciale, anche se ripetutamente, senza alcun ritardo evidente.**
    -   Per i problemi relativi a singoli caratteri o alle dimensioni massime di input, visualizzare il fumetto immediatamente all'input.
    -   Per i problemi relativi al valore di input (inclusa la richiesta di un valore non vuoto), visualizzare il fumetto quando il controllo proprietario perde lo stato attivo per l'input. In caso contrario, la visualizzazione di palloncini mentre gli utenti immettono input potenzialmente validi può essere distrazione e fastidiosa.
-   **Visualizzare un solo fumetto alla volta.** La visualizzazione di più palloncino può essere eccessivo. Se un singolo evento comporta più problemi, presentare tutti i problemi contemporaneamente o segnalare solo il problema più importante.

**Non corretto:** ![ Screenshot di due palloncini che puntano a una casella](images/ctrl-balloons-image5.png)

In questo esempio due problemi vengono presentati in modo errato contemporaneamente.

**Per quanto tempo visualizzare**

-   **Rimuovere un fumetto quando:**
    -   Il problema viene risolto o viene rimossa una condizione speciale.
    -   L'utente immette dati validi (per problemi di input).
    -   Timeout del fumetto. Per impostazione predefinita, i fumetto si rimuovono dopo 10 secondi, anche se gli utenti possono modificarlo modificando il parametro di sistema SPI \_ MESSAGEDURATION.
-   **Rimuovere il timeout se gli utenti non possono continuare fino a quando il problema non viene risolto. Sviluppatori:** in Win32 è possibile impostare l'ora di visualizzazione con il messaggio \_ TTM SETDELAYTIME.

**Come visualizzare**

-   **Visualizzare i fumetto sotto il controllo proprietario.** In questo modo gli utenti possono visualizzare il contesto, inclusi il controllo proprietario e la relativa etichetta. Microsoft Windows automaticamente le posizioni del fumetto in modo che siano completamente sullo schermo. Il comportamento predefinito è visualizzare un fumetto sopra il relativo controllo proprietario, come avviene con le notifiche.

**Corretto:** ![ Screenshot di un fumetto visualizzato sotto il relativo controllo](images/ctrl-balloons-image6.png)

**Risposta errata:** ![ screenshot di un fumetto visualizzato sopra il relativo controllo](images/ctrl-balloons-image7.png)

Nell'esempio non corretto, il balloon viene visualizzato in modo non corretto sopra il relativo controllo proprietario.

**Caselle di testo per password e PIN**

-   **Usare un fumetto per indicare che BLOC MAIUSC è su**, usando il testo nell'esempio seguente:

![Screenshot di un fumetto che indica che il blocco con estremità è on](images/ctrl-balloons-image8.png)

In questo esempio, un fumetto indica che BLOC MAIUSC è on in una casella di testo PIN.

-   **Usare un balloon per indicare quando gli utenti tentano di superare le dimensioni massime di input.** Il raggiungimento delle dimensioni massime di input è molto meno ovvio nelle caselle di testo per password e PIN rispetto alle normali caselle di testo.

![Screenshot di un fumetto che indica i limiti del codice pin](images/ctrl-balloons-image9.png)

In questo esempio, un balloon indica che l'utente sta tentando di superare le dimensioni massime di input.

-   **Usare un fumetto per indicare quando gli utenti immettere caratteri non corretti.** Tuttavia, è meglio non avere tali restrizioni perché riducono la sicurezza della password o del PIN. Per impedire la divulgazione di informazioni, il balloon deve menzionare solo i fatti documentati relativi a password o PIN validi.

![Screenshot di un fumetto che indica un input non corretto](images/ctrl-balloons-image10.png)

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
    | Problema di input | Nessuna icona. Non usare [un'icona di errore in](vis-std-icons.md) questo caso è coerente con le linee guida Windows [tono.](text-style-tone.md) |
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

