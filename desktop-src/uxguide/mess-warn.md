---
title: Messaggi di avviso
description: Un messaggio di avviso è una finestra di dialogo modale, un messaggio sul posto, una notifica o un fumetto che avvisa l'utente di una condizione che potrebbe causare un problema in futuro.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d704890b2471e205b933e2995950716c269488e8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351086"
---
# <a name="warning-messages"></a>Messaggi di avviso

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Un messaggio di avviso è una finestra di dialogo modale, un messaggio sul posto, una notifica o un fumetto che avvisa l'utente di una condizione che potrebbe causare un problema in futuro.

![Screenshot di un messaggio di avviso tipico](images/mess-warn-image1.png)

Un messaggio di avviso modale tipico.

La caratteristica fondamentale degli avvisi è che coinvolgono il rischio di perdita di uno o più dei seguenti elementi:

-   Una risorsa preziosa, ad esempio dati finanziari o altri dati importanti.
-   Accesso al sistema o integrità.
-   Privacy o controllo sulle informazioni riservate.
-   Tempo utente (un importo significativo, ad esempio 30 secondi o più).

Al contrario, una conferma è una finestra di dialogo modale che chiede se l'utente desidera procedere con un'azione. Alcuni tipi di avvisi vengono presentati come conferme e, in tal caso, vengono applicate anche le linee guida di conferma.

**Nota:** Le linee guida relative alle [finestre di dialogo](win-dialog-box.md), le [conferme](mess-confirm.md), [i messaggi di errore](mess-error.md)[icone standard](vis-std-icons.md), le [notifiche](mess-notif.md)e il [layout](vis-layout.md) vengono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendi in considerazione queste domande:

-   **L'utente viene avvisato di una condizione che potrebbe causare un problema in futuro?** In caso contrario, il messaggio non è un avviso.
-   **L'interfaccia utente presenta un errore o un problema che si è già verificato?** In caso affermativo, usare invece un messaggio di errore.
-   **È probabile che gli utenti eseguano un'azione o modifichino il proprio comportamento come risultato del messaggio?** In caso contrario, la condizione non giustifica l'interruzione dell'utente, quindi è preferibile eliminarlo.
-   **La condizione è il risultato diretto di un'azione iniziata dall'utente?** In caso contrario, prendere in considerazione l'uso di [notifiche di eventi non critiche](mess-notif.md).
-   **La condizione è una condizione speciale in un controllo?** In caso affermativo, usare invece un [fumetto](ctrl-balloons.md) .
-   **Per le conferme, l'utente sta per eseguire un'azione rischiosa?** In tal caso, è opportuno un avviso se l'azione ha conseguenze significative o non può essere facilmente annullata.
-   **Per altri tipi di avvisi, è necessario che l'utente agisca ora o nel futuro immediato?** Non visualizzare avvisi se gli utenti possono continuare a lavorare in modo produttivo senza problemi immediati. Posticipare l'avviso fino a quando la condizione non è più immediata e pertinente.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="avoid-overwarning"></a>Evitare l'overwarning

I programmi Microsoft Windows sono sovrainformati. Il normale programma Windows presenta avvisi apparentemente ovunque, in cui si verificano elementi che hanno un significato ridotto. In alcuni programmi, quasi tutte le domande vengono presentate come un avviso. L'overwarning fa in modo che l'uso di un programma risulti un'attività pericolosa e si riducono da problemi realmente significativi.

**Non corretto:**

![Screenshot di un messaggio di avviso non necessario ](images/mess-warn-image2.png)

Overwarning rende il programma più pericoloso e sembra che sia stato progettato dagli avvocati.

Il mero potenziale per la perdita di dati o un problema futuro da solo non è sufficiente per chiamare un avviso. Inoltre, tutti i risultati indesiderati devono essere imprevisti o non intenzionali e non sono facilmente corretti. In caso contrario, quasi tutti gli errori utente potrebbero essere interpretati per comportare la perdita di dati o un potenziale problema di qualche tipo e meritare un avviso.

### <a name="characteristics-of-good-warnings"></a>Caratteristiche degli avvisi validi

Avvisi positivi:

-   **Coinvolgere i rischi.** Avvisi validi avvisano gli utenti di qualcosa di significativo.

**Non corretto:**

![Screenshot di ' si desidera uscire?' warning ](images/mess-warn-image3.png)

E allora? Questa conferma presuppone che gli utenti riescano spesso i programmi per errore.

-   **Hanno una rilevanza immediata.** Non solo gli utenti devono occuparsi di questo. Gli utenti in genere non sono interessati ai problemi che potrebbero avere in un secondo momento, purché possano svolgere il proprio lavoro.

**Non corretto:**

![screenshot della batteria: avviso minimo di tre ore ](images/mess-warn-image4.png)

In questo caso, è preferibile solo avvisare l'utente in tre ore.

-   **Condurre l'azione.** È necessario che gli utenti eseguano o siano a conoscenza di come il risultato dell'avviso. Forse è necessario eseguire un'azione subito o in un secondo momento nel futuro immediato. Probabilmente eseguiranno un'attività in modo diverso. La conseguenza di ignorare l'avviso dovrebbe essere chiara. Gli avvisi senza azioni fanno solo sentire paranoici.

**Non corretto:**

![screenshot dell'avviso "Live Messenger is running" ](images/mess-warn-image5.png)

Perché si tratta di una notifica di avviso? Che cosa dovrebbero fare gli utenti (oltre a preoccuparsi)?

-   **Non sono evidenti.** Non visualizzare un avviso per indicare la conseguenza ovvia di un'azione. Si supponga, ad esempio, che gli utenti capiscano le conseguenze del mancato completamento di un'attività.

**Non corretto:**

![Screenshot di uscire dalla procedura guidata? avviso ](images/mess-warn-image6.png)

L'annullamento di una procedura guidata incompleta significa che l'attività non viene eseguita... Chi sa?

-   **Si verificano raramente.** Gli avvisi costanti diventano rapidamente inefficaci e fastidiosi. Gli utenti spesso diventano più mirati a eliminare l'avviso rispetto al problema.

**Non corretto:**

![screenshot dell'avviso ' Aggiorna firme virus ' ](images/mess-warn-image7.png)

È più probabile che gli utenti si concentrino su come eliminare l'avviso rispetto alla risoluzione del problema sottostante.

Un messaggio che non ha queste caratteristiche potrebbe essere ancora un messaggio valido, ma non un avviso valido.

### <a name="determine-the-appropriate-message-type"></a>Determinare il tipo di messaggio appropriato

Alcuni problemi possono essere presentati come un errore, un avviso o informazioni, a seconda dell'enfasi e della formulazione. Si supponga, ad esempio, che una pagina Web non possa caricare un controllo ActiveX non firmato basato sulla configurazione corrente di Windows Internet Explorer:

-   **Errore.** "Questa pagina non può caricare un controllo ActiveX senza segno". (Frase come problema esistente).
-   **Avviso.** "Questa pagina potrebbe non comportarsi come previsto perché Windows Internet Explorer non è configurato per il caricamento di controlli ActiveX non firmati". oppure "Consenti a questa pagina di installare un controllo ActiveX senza segno? Questa operazione da origini non attendibili potrebbe danneggiare il computer ". (Entrambe espresse come condizioni che possono causare problemi futuri).
-   **Informazioni.** "È stato configurato Windows Internet Explorer per bloccare i controlli ActiveX non firmati." (Enunciato come dichiarazione di fatto).

**Per determinare il tipo di messaggio appropriato, concentrarsi sull'aspetto più importante del problema che gli utenti devono sapere o su cui intervenire.** In genere, se un problema impedisce all'utente di procedere, è necessario presentarlo come errore; Se l'utente può continuare, presentarlo come avviso. Creare l' [istruzione principale](text-ui.md) o un altro testo corrispondente in base a tale stato attivo, quindi scegliere un'icona ([standard](vis-std-icons.md) o altro) che corrisponda al testo. Il testo dell'istruzione principale e le icone devono sempre corrispondere.

### <a name="be-specific"></a>Specifica

Gli avvisi sono più interessanti quando le informazioni seguenti sono specifiche e chiare:

-   Origine dell'avviso.
-   Condizione specifica e potenziale problema.
-   Operazioni che l'utente deve eseguire.
-   Cosa accade se l'utente non esegue alcuna operazione.

**Non corretto:**

![Screenshot di un avviso vago di rischio significativo ](images/mess-warn-image8.png)

In questo esempio, qual è il potenziale problema? Che cosa deve fare l'utente, oltre a non usare il proiettore sulla rete? Senza informazioni più specifiche, è possibile che l'utente non sia in grado di procedere.

**Corretto:**

![screenshot dell'avviso di problemi e conseguenze ](images/mess-warn-image9.png)

In questo esempio il problema e le conseguenze sono evidenti.

In alcuni casi è possibile che si verifichi un problema legittimo per informare gli utenti, ma la soluzione e le conseguenze non sono note. Anziché fornire un avviso vago, essere specifici fornendo le informazioni più probabili o l'esempio più comune.

**Corretto:**

![screenshot dell'avviso di errore di rete e delle soluzioni ](images/mess-warn-image10.png)

In questo esempio, l'avviso viene reso specifico fornendo la soluzione più probabile.

In questi casi, tuttavia, utilizzare la formulazione che indica che esistono altre possibilità. In caso contrario, gli utenti potrebbero essere fuorviati.

**Non corretto:**

![screenshot del cavo di rete-avviso scollegato ](images/mess-warn-image11.png)

**Corretto:**

![è possibile che lo screenshot del cavo sia scollegato dall'avviso ](images/mess-warn-image12.png)

Nell'esempio errato, gli utenti saranno confusi se il cavo è chiaramente collegato.

**Se si eseguono solo due operazioni...**

1. Non sovraavvisare. Limitare gli avvisi alle condizioni che coinvolgono il rischio e sono immediatamente rilevanti, interoperabili, non evidenti e poco frequenti. In caso contrario, rimuovere o riformulare il messaggio.

2. Fornire informazioni utili specifiche.

## <a name="usage-patterns"></a>Modelli di utilizzo

Gli avvisi hanno diversi modelli di utilizzo:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Informazioni</strong><br/> Informare l'utente di una condizione o di un potenziale problema, ma l'utente potrebbe non dover eseguire alcuna operazione. <br/></td>
<td><img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br/> <img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br/> <img src="images/mess-warn-image15.png" alt="Screen shot of &#39;caps-lock-is-on&#39; warning " /><br/> <img src="images/mess-warn-image16.png" alt="Screen shot of &#39;TPM-not-found&#39; warning " /><br/> Esempi di avvisi di consapevolezza.<br/> Gli avvisi di sensibilizzazione hanno la presentazione seguente: <br/>
<ul>
<li><strong>Istruzione principale:</strong> Descrizione della condizione o del potenziale problema.</li>
<li><strong>Istruzione supplementare:</strong> Illustrare le implicazioni e il motivo per cui è importante.</li>
<li><strong>Pulsanti di commit:</strong> Vicino.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Prevenzione degli errori</strong><br/> Informare gli utenti delle informazioni che potrebbero impedire un problema, soprattutto quando si effettuano scelte. <br/></td>
<td>Gli avvisi di prevenzione degli errori vengono presentati in modo ottimale usando un'icona di avviso sul posto e un testo esplicativo. <br/> <img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br/> <img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br/> Esempi di avvisi di prevenzione degli errori.<br/></td>
</tr>
<tr class="odd">
<td><strong>Problema imminente</strong><br/> L'utente deve ora eseguire un'operazione per evitare un problema imminente. <br/></td>
<td><img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br/> Un esempio di avviso imminente di un problema.<br/> Gli avvisi imminenti per i problemi hanno la seguente presentazione: <br/>
<ul>
<li><strong>Istruzione principale:</strong> Descrivere le operazioni che l'utente deve eseguire.</li>
<li><strong>Istruzione supplementare:</strong> Illustrare la condizione e il motivo per cui è importante.</li>
<li><strong>Pulsanti di commit:</strong> Un pulsante di comando o un collegamento al comando per ogni opzione oppure OK se l'azione si verifica all'esterno della finestra di dialogo.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Conferma dell'azione rischiosa</strong><br/> Confermare che l'utente desidera procedere con un'azione che presenta un certo rischio e non può essere annullata facilmente. <br/></td>
<td><img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br/> Esempio di conferma dell'azione rischiosa.<br/> Per le conferme di azione rischiosa sono disponibili le seguenti presentazioni: <br/>
<ul>
<li><strong>Istruzione principale:</strong> Porre una domanda per determinare se l'utente vuole continuare.</li>
<li><strong>Istruzione supplementare:</strong> Spiega tutti i motivi non evidenti per cui l'utente potrebbe non voler procedere.</li>
<li><strong>Pulsanti di commit:</strong> Sì, no.</li>
</ul>
Per le linee guida su questo modello, vedere <a href="mess-confirm.md">conferme</a>. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Indicazioni

### <a name="presentation"></a>Presentazione

-   **Scegliere l'interfaccia utente di presentazione in base al tipo di informazioni:**



|                               |                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Interfaccia utente**<br/> | **Migliore uso per**<br/>                                                                                                           |
| Finestre di dialogo modali<br/> | Avvisi critici (incluse le conferme) a cui gli utenti devono rispondere ora.<br/>                                                 |
| Sul posto<br/>           | Informazioni che potrebbero impedire un problema, specialmente quando gli utenti effettuano scelte.<br/>                                         |
| Banner<br/>            | Informazioni che potrebbero impedire un problema, soprattutto quando sono correlate al completamento di un'attività.<br/>                                     |
| Notifiche<br/>      | Eventi o stati significativi che possono essere tranquillamente ignorati, almeno temporaneamente.<br/>                                              |
| Palloncini<br/>           | Un controllo si trova in uno stato che influiscono sull'input. È probabile che questo stato non sia intenzionale e che l'utente non possa realizzare l'input interessato.<br/> |



 

-   **Per le finestre di dialogo modali:**
    -   **Usare le finestre di dialogo delle attività quando appropriato per ottenere un aspetto e un layout coerenti.** Le finestre di dialogo delle attività richiedono Windows Vista o versioni successive, quindi non sono adatte per le versioni precedenti di Windows.
    -   **Visualizza solo un messaggio di avviso per condizione.** Ad esempio, viene visualizzato un singolo avviso che spiega completamente una condizione invece di descriverlo un dettaglio alla volta per ogni messaggio. La visualizzazione di una sequenza di finestre di dialogo di avviso per una singola condizione è confusa e fastidiosa.
    -   **Non visualizzare più di una volta un avviso per condizione.** Gli avvisi costanti diventano rapidamente inefficaci e fastidiosi. Gli utenti spesso diventano più mirati a eliminare l'avviso rispetto al problema. Se è necessario avvisare ripetutamente per una singola condizione, usare l' [escalation progressiva](mess-notif.md).
-   **Non accompagnare avvisi con un effetto acustico o un segnale acustico.** Questa operazione è stonata e non necessaria.
    -   **Eccezione:** Se l'utente deve rispondere immediatamente, è possibile usare un effetto acustico.

### <a name="icons"></a>Icone

-   Non inserire un'icona di avviso nella barra del titolo di una finestra di dialogo.
-   **Usare un'icona di avviso.** Eccezioni:
    -   Se l'avviso è relativo a una funzionalità con un'icona, è possibile usare l'icona della funzionalità con una sovrimpressione di avviso.

        **Corretto:**

        ![screenshot dell'icona di blocco con sovrapposizione dell'icona di avviso ](images/mess-warn-image21.png)

        In questo esempio, l'icona della funzionalità presenta una sovrapposizione di avviso.

-   Per le finestre di dialogo modali con una nota di avviso, inserire l'icona di avviso nella nota a piè di pagina anziché nell'area del contenuto.

    **Corretto:**

    ![screenshot dell'icona di avviso nella nota a piè di pagina della finestra di dialogo ](images/mess-warn-image22.png)

    In questo esempio, la nota contiene l'icona di avviso.

Per altre linee guida ed esempi, vedere [icone standard](vis-std-icons.md).

### <a name="dont-show-this-message-again"></a>Non visualizzare più questo messaggio

-   **Se una finestra di dialogo di avviso richiede questa opzione, riconsiderare l'avviso e la relativa frequenza.** Se dispone di tutte le caratteristiche di un avviso valido (comporta il rischio ed è immediatamente pertinente, praticabile, non ovvia e poco frequente), non dovrebbe essere utile per gli utenti eliminarlo.

Per altre linee guida, vedere [finestre di dialogo](win-dialog-box.md).

### <a name="progressive-disclosure"></a>Rivelazione progressiva

-   **Se è necessario includere informazioni avanzate in un messaggio di avviso, visualizzarlo usando i pulsanti di divulgazione progressiva** (ad esempio, "Mostra dettagli"). In questo modo, l'avviso viene semplificato per l'utilizzo tipico. Non nascondere le informazioni necessarie perché gli utenti potrebbero non trovarlo.
-   **Non usare "Show Details", a meno che non vi siano effettivamente più dettagli.** Non solo riformulare le informazioni esistenti in un formato diverso.

Per le linee guida sulle etichette, vedere [divulgazione progressiva](ctrl-progressive-disclosure-controls.md).

### <a name="default-values"></a>Valori predefiniti

-   **Selezionare la risposta più sicura, meno distruttiva o più sicura come predefinita.**

## <a name="text"></a>Testo

### <a name="general"></a>Generale

-   **Rimuovere il testo ridondante.** Cercarla in titoli, istruzioni principali, istruzioni aggiuntive, aree di contenuto, collegamenti ai comandi e pulsanti di commit. In genere, lasciare il testo completo nelle istruzioni e nei controlli interattivi e rimuovere qualsiasi ridondanza dalle altre posizioni.
-   **Non usare i termini "avviso" o "attenzione" nel testo.** Se [usato correttamente](vis-std-icons.md), l'icona di avviso comunica sufficientemente che gli utenti devono procedere con cautela.

**Non corretto:**

![screenshot dell'utilizzo non necessario dell'avviso nel testo ](images/mess-warn-image23.png)

In questo esempio, il termine "avviso" non è necessario.

### <a name="titles"></a>Titoli

-   **Usare il titolo per identificare il comando o la funzionalità da cui proviene l'avviso.** Eccezioni:
    -   Se un avviso viene visualizzato con molti comandi diversi, provare a usare il nome del programma.
    -   Se il titolo è ridondante o confuso con l'istruzione principale, usare invece il nome del programma.

**Non corretto:**

![screenshot del titolo della finestra di dialogo avviso di sicurezza ](images/mess-warn-image24.png)

In questo esempio "avviso di sicurezza" non identifica il comando o la funzionalità da cui proviene l'avviso.

-   **Non usare il titolo per spiegare cosa fare nella finestra di dialogo** che è lo scopo dell'istruzione principale.
-   Usare l'uso [di maiuscole in stile titolo](glossary.md)senza la punteggiatura finale.

### <a name="main-instructions"></a>Istruzioni principali

-   L'istruzione principale di un avviso è basata sul modello di progettazione:



|                                      |                                                                      |
|--------------------------------------|----------------------------------------------------------------------|
| **Modello**<br/>               | **Istruzione principale**<br/>                                      |
| Riconoscimento<br/>                 | Descrizione della condizione o del potenziale problema.<br/>              |
| Problema imminente<br/>          | Descrivere le operazioni che l'utente deve eseguire.<br/>                   |
| Conferma dell'azione rischiosa<br/> | Porre una domanda per determinare se l'utente vuole continuare.<br/> |



 

-   ![Screenshot di una notifica con batteria insufficiente ](images/mess-warn-image25.png)
-   In questo esempio, la notifica della batteria insufficiente è un avviso di consapevolezza, quindi l'istruzione principale descrive la condizione.
-   ![screenshot della batteria di modifica immediatamente avviso ](images/mess-warn-image1.png)
-   In questo esempio, la finestra di dialogo batteria insufficiente è un problema imminente, quindi l'istruzione principale descrive le operazioni che l'utente deve eseguire.
-   **Usare concise solo una singola frase completa.** Rimuovere l'istruzione principale fino alle informazioni essenziali. Se è necessario spiegare altro, utilizzare un'istruzione supplementare.
-   **Usare parole come "Now" e "immediate" se l'utente deve agire immediatamente.** Non usare queste parole se non è prevista alcuna urgenza.
-   **Essere specifici se sono presenti oggetti interessati, assegnare i nomi completi.**
-   Usare l'uso [di maiuscole in stile frase](glossary.md).

### <a name="supplemental-instructions"></a>Istruzioni supplementari

-   L'istruzione supplementare per un avviso è basata sul modello di progettazione:



|                                      |                                                                                    |
|--------------------------------------|------------------------------------------------------------------------------------|
| **Modello**<br/>               | **Istruzione supplementare**<br/>                                            |
| Riconoscimento<br/>                 | Illustrare le implicazioni e il motivo per cui è importante.<br/>                        |
| Problema imminente<br/>          | Illustrare la condizione e il motivo per cui è importante.<br/>                          |
| Conferma dell'azione rischiosa<br/> | Spiega tutti i motivi non evidenti per cui l'utente potrebbe non voler procedere.<br/> |



 

-   **Non ripetere l'istruzione principale con una formulazione leggermente diversa.** Omettere invece l'istruzione supplementare se non è più necessario aggiungere.
-   Usare frasi complete, maiuscole e minuscole in stile frase e punteggiatura finale.

### <a name="commit-buttons"></a>Pulsanti di commit

-   Per le finestre di dialogo di avviso, i pulsanti commit sono basati sul modello di progettazione:



|                                      |                                                                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **Modello**<br/>               | **Pulsanti di commit**<br/>                                                                                   |
| Riconoscimento<br/>                 | Quasi. Non usare OK perché suggerisce che i potenziali problemi sono OK.<br/>                              |
| Problema imminente<br/>          | Un pulsante di comando o un collegamento al comando per ogni opzione oppure OK se l'azione si verifica all'esterno della finestra di dialogo.<br/> |
| Conferma dell'azione rischiosa<br/> | Sì, no.<br/>                                                                                             |



 

-   **Non corretto:**
-   ![screenshot della finestra di dialogo di avviso con pulsante OK ](images/mess-warn-image26.png)
-   I problemi non sono OK. usare invece Close.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento agli avvisi:

-   Se l'avviso pone una domanda, fare riferimento a un avviso in base alla domanda. in caso contrario, utilizzare l'istruzione principale. Se la domanda o l'istruzione principale è estesa o dettagliata, riepilogarla.
-   Se necessario, è possibile fare riferimento a una finestra di dialogo di avviso come messaggio.
-   Quando possibile, formattare il testo usando grassetto. In caso contrario, inserire il testo tra virgolette solo se necessario per evitare confusione.

Esempio: nel messaggio **visualizzare gli elementi non protetti?** fare clic su Sì.

 

