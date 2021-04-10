---
title: Palloncini
description: Un fumetto è una piccola finestra popup che informa gli utenti di un problema non critico o di una condizione speciale in un controllo.
ms.assetid: 67092831-e573-4ad6-b1fc-baa1836031cb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 348167594db2f7895e185d8d7761832ec5c0c1cb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351061"
---
# <a name="balloons"></a>Palloncini

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Un fumetto è una piccola finestra popup che informa gli utenti di un problema non critico o di una condizione speciale in un controllo.

![Screenshot che mostra un fumetto che indica che BLOC MAIUSC è on.](images/ctrl-balloons-image1.png)

Un fumetto tipico.

Gli aerostati hanno un'icona, un titolo e un testo del corpo, tutti facoltativi. Diversamente dalle descrizioni comandi e infotip, i palloncini hanno anche una coda che identifica la loro origine. In genere, l'origine è un controllo, in caso affermativo, viene definito [controllo proprietario](glossary.md).

Mentre gli aerostati informano gli utenti di problemi non critici, non impediscono problemi anche se il controllo proprietario potrebbe. Eventuali problemi non gestiti devono essere gestiti dall'interfaccia utente del proprietario quando gli utenti tentano di eseguire il commit dell'azione.

Gli aerostati vengono in genere usati con caselle di testo o controlli che usano caselle di testo per modificare i valori, ad esempio caselle combinate, visualizzazioni elenco e visualizzazioni ad albero. Altri tipi di controlli sono sufficientemente limitati e non è necessario che si offrano le altre bolle di feedback. Inoltre, se si verifica un problema con altri tipi di controlli, spesso l'incoerenza tra più controlli rappresenta una situazione in cui i palloni non sono appropriati. Solo i controlli di immissione di testo sono non vincolati e un'origine comune di [errori a singolo punto](glossary.md).

Una notifica è un tipo specifico di fumetto visualizzato da un'icona dell' [area di notifica](winenv-notification.md) .

**Nota:** Le linee guida relative a [notifiche](mess-notif.md), [descrizioni comandi e infotip](ctrl-tooltips-and-infotips.md)e [messaggi di errore](mess-error.md) vengono presentate in articoli distinti.

**È il controllo giusto?**

Per decidere, prendi in considerazione queste domande:

-   **Le informazioni descrivono un problema o una condizione speciale?** Se non è così, usa un altro controllo. Non usare gli aerostati per visualizzare informazioni aggiuntive per un controllo; prendere in considerazione l'uso di [testo statico](glossary.md),[infotip](glossary.md), [divulgazione progressiva](glossary.md)o richieste.
-   **È possibile rilevare immediatamente il problema o la condizione speciale** in caso di input o quando il controllo proprietario perde lo stato attivo per l'input? In caso contrario, utilizzare un messaggio di errore visualizzato in una [finestra di dialogo attività](glossary.md) o in una [finestra di messaggio](glossary.md).
-   **Per i problemi, il problema è critico?** In tal caso, utilizzare un messaggio di errore visualizzato in una finestra di dialogo attività o in una finestra di messaggio. Tali messaggi di errore richiedono l'interazione (idonea per gli errori critici), mentre i fumetti non lo sono.
-   **Per condizioni speciali, la condizione valida è probabilmente non intenzionale?** In tal caso, i palloni sono appropriati. Per le condizioni non valide, è preferibile impedirle nella prima posizione. Per le condizioni previste probabilmente, non è necessario eseguire alcuna operazione.
-   **Il problema o la condizione speciale può essere espressa in modo conciso?** Se non è così, usa un altro controllo. Gli aerostati non possono avere spiegazioni dettagliate o fornire informazioni aggiuntive.
-   **Le informazioni descrivono il controllo di cui è attualmente in corso il passaggio del mouse?** In caso affermativo, usare invece un suggerimento, a meno che non sia necessario che gli utenti interagiscano con il messaggio.
-   **Le informazioni sono correlate all'attività corrente dell'utente?** In caso contrario, prendere in considerazione l'uso di una [notifica](mess-notif.md) o di una [finestra di dialogo](win-dialog-box.md) . È probabile che gli utenti ignorino i palloni al di fuori dell'attività corrente e, per impostazione predefinita, il timeout dei palloncini dopo 10 secondi.
-   **Le informazioni provengono da un'unica origine specifica?** Se un problema o una condizione ha più origini o nessuna origine specifica, usare invece un [messaggio sul posto](glossary.md) o una finestra di dialogo.

Non **corretto:** ![ Screenshot di un fumetto: accesso non riuscito](images/ctrl-balloons-image2.png)

In questo esempio, il problema potrebbe essere con il nome utente o la password, ma la segnalazione del problema con un fumetto suggerisce visivamente che solo la password è il problema. Di conseguenza, il feedback dell'immissione di un nome utente errato è fuorviante.

Gli aerostati rappresentano un'alternativa a infotip, finestre di dialogo e messaggi sul posto. Diversamente dalle descrizioni comando e infotip:

-   Gli aerostati possono essere visualizzati indipendentemente dalla posizione corrente del puntatore, quindi hanno una coda che ne indica l'origine.
-   Gli aerostati hanno un titolo, un testo del corpo e un'icona.
-   Gli aerostati possono essere interattivi, mentre è Impossibile fare clic su un suggerimento.

Diversamente dalle finestre di dialogo modali:

-   Gli aerostati non rubano lo stato attivo per l'input o richiedono interazione.
-   Gli aerostati identificano una singola origine specifica. Le finestre di dialogo modali possono avere più origini o nessuna origine specifica.

A differenza dei messaggi sul posto:

-   Gli aerostati sono più evidenti.
-   Le mongolfiere non richiedono lo spazio disponibile sullo schermo o il layout dinamico necessario per visualizzare i messaggi sul posto.
-   I palloni vengono rimossi automaticamente dopo un timeout.

**Modelli di utilizzo**

I modelli di utilizzo dei palloncini sono i seguenti:



|                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Problema di input** Un problema di input utente non critico proveniente da un singolo controllo proprietario, in genere una casella di testo. <br/>                                               | l'uso di palloni per i messaggi di errore non ruba lo stato attivo per l'input, ma è ancora molto evidente se il controllo proprietario ha lo stato attivo per l'input per risolvere il problema, è possibile che l'utente debba modificare o immettere nuovamente l'input. Tuttavia, se il controllo proprietario ignora un input errato, è possibile che l'utente non debba apportare alcuna modifica. Poiché il problema non è critico, non è necessaria alcuna [icona di errore](vis-std-icons.md) . <br/> ![Screenshot che mostra un fumetto che indica un carattere non corretto.](images/ctrl-balloons-image3.png)<br/> Un fumetto usato per segnalare un problema di input utente non critico.<br/>                                                                                                  |
| **Condizione speciale** Il controllo proprietario si trova in uno stato che influiscono sull'input. È probabile che questo stato non sia intenzionale e che l'utente non possa realizzare l'input interessato. <br/> | usare i palloni per evitare la frustrazione avvisando gli utenti di condizioni speciali non appena si verificano (ad esempio, superando le dimensioni massime di input o impostando BLOC MAIUSC per errore). è importante fornire tali commenti senza sottrarre lo stato attivo per l'input o forzare l'interazione perché queste condizioni potrebbero essere intenzionali. questi palloncini sono particolarmente importanti per le caselle password e pin, in cui gli utenti lavorano altrimenti con un feedback minimo. questi palloncini hanno un' [icona di avviso](vis-std-icons.md). <br/> ![Screenshot che Mostra gli aerostati che indicano che BLOC MAIUSC è attivato e viene immesso un carattere non corretto.](images/ctrl-balloons-image4.png)<br/> Fumetto utilizzato per segnalare una condizione speciale.<br/> |



 

**Linee guida**

**Quando visualizzare**

-   **Visualizza il fumetto non appena viene rilevato il problema o la condizione speciale, anche se ripetutamente, senza ritardi evidenti.**
    -   Per i problemi relativi ai singoli caratteri o alle dimensioni massime di input, visualizzare immediatamente il fumetto in input.
    -   Per i problemi che coinvolgono il valore di input (inclusa la richiesta di un valore non vuoto), visualizzare il fumetto quando il controllo proprietario perde lo stato attivo per l'input. In caso contrario, la visualizzazione di palloncini mentre gli utenti entrano in un input potenzialmente valido può essere distrazione e fastidioso.
-   **Visualizza solo un fumetto alla volta.** La visualizzazione di più palloncini può risultare eccessiva. Se un singolo evento comporta più problemi, presentare tutti i problemi contemporaneamente o segnalare solo il problema più importante.

Non **corretto:** ![ Screenshot di due palloncini che puntano a una casella](images/ctrl-balloons-image5.png)

In questo esempio, due problemi vengono presentati in modo errato nello stesso momento.

**Durata della visualizzazione**

-   **Rimuovere un fumetto quando:**
    -   Il problema è stato risolto o la condizione speciale è stata rimossa.
    -   L'utente immette dati validi (per i problemi di input).
    -   Timeout del fumetto. Per impostazione predefinita, i palloni vengono rimossi dopo 10 secondi, sebbene gli utenti possano modificare questa impostazione modificando il \_ parametro di sistema SPI MESSAGEDURATION.
-   **Rimuovere il timeout se gli utenti non possono continuare fino a quando il problema non viene risolto. Sviluppatori:** in Win32 è possibile impostare l'ora di visualizzazione con il \_ messaggio TTM SETDELAYTIME.

**Come visualizzare**

-   **Visualizza i palloni sotto il controllo proprietario.** Questa operazione consente agli utenti di visualizzare il contesto, inclusi il controllo proprietario e la relativa etichetta. Microsoft Windows regola automaticamente le posizioni del fumetto in modo che siano completamente sullo schermo. Il comportamento predefinito prevede la visualizzazione di un fumetto sopra il relativo controllo proprietario, come fatto con le notifiche.

**Corretto:** ![ Screenshot di un fumetto visualizzato sotto il relativo controllo](images/ctrl-balloons-image6.png)

Non **corretto:** ![ Screenshot di un fumetto visualizzato sopra il relativo controllo](images/ctrl-balloons-image7.png)

Nell'esempio errato, il fumetto viene visualizzato goffamente sopra il controllo del proprietario.

**Caselle di testo password e PIN**

-   **Usare un fumetto per indicare che BLOC MAIUSC è acceso**, usando il testo nell'esempio seguente:

![Screenshot di un fumetto che indica che BLOC MAIUSC è acceso](images/ctrl-balloons-image8.png)

In questo esempio un fumetto indica che BLOC MAIUSC si trova in una casella di testo PIN.

-   **Usare un fumetto per indicare quando gli utenti tentano di superare le dimensioni massime di input.** Il raggiungimento delle dimensioni massime di input è molto meno ovvio nelle caselle di testo password e PIN rispetto alle caselle di testo normali.

![Screenshot di un fumetto che indica i limiti del codice PIN](images/ctrl-balloons-image9.png)

In questo esempio, un fumetto indica che l'utente sta provando a superare le dimensioni massime di input.

-   **Usare un fumetto per indicare quando gli utenti immettevano caratteri non corretti.** Tuttavia, è preferibile non avere tali restrizioni perché riducono la sicurezza della password o del PIN. Per impedire la divulgazione di informazioni, il fumetto deve menzionare solo i fatti documentati relativi a password o pin validi.

![Screenshot di un fumetto che indica un input errato](images/ctrl-balloons-image10.png)

In questo esempio, un fumetto indica che il PIN richiede numeri.

**Altre caselle di testo**

-   **Si consiglia di usare un fumetto per indicare quando gli utenti tentano di superare le dimensioni massime di input per le caselle di testo critiche e brevi destinate agli utenti principianti.** Gli esempi includono i nomi utente e i nomi degli account. Le caselle di testo emette un segnale acustico quando gli utenti tentano di superare l'input massimo, ma gli utenti principianti potrebbero non comprendere il significato del segnale acustico.

![Screenshot di un fumetto che indica i limiti dei caratteri](images/ctrl-balloons-image11.png)

In questo esempio, un fumetto indica che l'utente ha tentato di superare le dimensioni massime di input.

**Interazione**

-   **Quando gli utenti fanno clic su un fumetto, è sufficiente chiudere il fumetto senza visualizzare altre interfacce utente o avere altri effetti collaterali.** Diversamente dalle notifiche, gli aerostati non devono contenere pulsanti di chiusura.

**Icone**

-   Scegliere l'icona in base al modello di utilizzo:



    |  Modello |  Icona                                                                                                                                                       |
    ------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Problema di input | Nessuna icona. La mancata utilizzo di un' [icona di errore](vis-std-icons.md) è coerente con le linee guida per i [toni di Windows](text-style-tone.md) . |
    | Condizione speciale | [Icona di avviso](vis-std-icons.md)16x16 pixel standard.                                                                                  |

**Accessibilità**

Se usato correttamente, i palloncini migliorano l'accessibilità. Per l'accessibilità delle mongolfiere:

-   Consente di visualizzare solo gli aerostati correlati all'attività corrente dell'utente.
-   Rendere conciso il testo del fumetto. In questo modo il testo del fumetto risulta più semplice da leggere per gli utenti con ipovisione e riduce al minimo l'interruzione quando viene letta dalle utilità per la lettura dello schermo.
-   Rivisualizza il fumetto ogni volta che il problema o la condizione si ripete.

**Text**

**Testo titolo**

-   **Usare il testo del titolo che riepiloga brevemente il problema di input o la condizione speciale in un linguaggio chiaro, semplice, conciso e specifico.** Gli utenti dovrebbero essere in grado di comprendere lo scopo del fumetto rapidamente e con il minimo sforzo.
-   **Utilizzare frammenti di testo o frasi complete senza punteggiatura finale.**
-   **Usare le maiuscole/minuscole come nelle frasi comuni.** Per ulteriori informazioni, vedere il [Glossario](./glossary.md).
-   **Per gestire la localizzazione, non usare più di 48 caratteri (in inglese).** Il titolo ha una lunghezza massima di 63 caratteri e deve essere in grado di espandersi almeno del 30% per adattarsi alla localizzazione.

**Testo corpo**

-   **Usare la prima frase del testo del corpo per indicare il problema o la condizione in modo che sia chiaramente pertinente per l'utente.** Non ripetere le informazioni nel titolo. Omettere questo se non c'è altro da aggiungere.
-   **Utilizzare la seconda frase per indicare le operazioni che l'utente può eseguire per risolvere il problema o ripristinare lo stato.** In conformità alle linee guida per [stile e tono](./text-style-tone.md) , non è necessario usare la parola in questa istruzione. Inserire due interruzioni di riga tra la prima e la seconda frase.

![Screenshot di un fumetto con titolo e testo del corpo](images/ctrl-balloons-image12.png)

Questo esempio illustra il layout standard del testo del fumetto.

-   **Viene illustrato come risolvere il problema o ripristinare lo stato anche se la spiegazione è ovvia,** ma omettere la ridondanza tra l'istruzione problem e la relativa risoluzione. **Eccezioni**
    -   Omettere la risoluzione se non può essere espressa in breve o senza ridondanza significativa.
    -   Omettere la risoluzione se non è necessario eseguire alcuna operazione per l'utente, ad esempio quando vengono ignorati i caratteri non corretti.
-   **Utilizzare frasi complete con la punteggiatura finale.**
-   **Usare le maiuscole/minuscole come nelle frasi comuni.**
-   **Per gestire la localizzazione, non usare più di 200 caratteri (in inglese).** Il testo del corpo ha una lunghezza massima di 255 caratteri e deve essere in grado di espandersi almeno del 30% per adattarsi alla localizzazione.

**Documentazione**

Quando si fa riferimento a Balloons:

-   Usare il testo del titolo esatto, inclusa la relativa maiuscola.
-   Vedere il componente come un fumetto, non come notifica o avviso.
-   Quando possibile, formattare il testo del titolo utilizzando il testo in grassetto. In caso contrario, inserire il titolo racchiuso tra virgolette solo se necessario per evitare confusione.

