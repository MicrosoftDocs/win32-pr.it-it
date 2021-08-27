---
title: Messaggi di avviso
description: Un messaggio di avviso è una finestra di dialogo modale, un messaggio sul posto, una notifica o un balloon che avvisa l'utente di una condizione che potrebbe causare un problema in futuro.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 944c99b546df5fd313ee5bd656db58fafe991d01
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470288"
---
# <a name="warning-messages"></a>Messaggi di avviso

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Un messaggio di avviso è una finestra di dialogo modale, un messaggio sul posto, una notifica o un balloon che avvisa l'utente di una condizione che potrebbe causare un problema in futuro.

![screenshot di un messaggio di avviso tipico](images/mess-warn-image1.png)

Messaggio di avviso modale tipico.

La caratteristica fondamentale degli avvisi è che comportano il rischio di perdere uno o più degli elementi seguenti:

-   Un asset prezioso, ad esempio dati finanziari o di altro tipo importanti.
-   Accesso o integrità del sistema.
-   Privacy o controllo sulle informazioni riservate.
-   Tempo dell'utente (una quantità significativa, ad esempio 30 secondi o più).

Al contrario, una conferma è una finestra di dialogo modale che chiede se l'utente vuole procedere con un'azione. Alcuni tipi di avvisi vengono presentati come conferme e, in tal caso, si applicano anche le linee guida per la conferma.

**Nota:** Le linee guida relative [a finestre di dialogo,](win-dialog-box.md) [conferme,](mess-confirm.md)messaggi di errore icone [](mess-error.md)[standard,](vis-std-icons.md) [notifiche](mess-notif.md)e [layout](vis-layout.md) vengono presentate in articoli separati.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, prendi in considerazione queste domande:

-   **L'utente viene avvisato di una condizione che potrebbe causare un problema in futuro?** In caso contrario, il messaggio non è un avviso.
-   **L'interfaccia utente presenta un errore o un problema che si è già verificato?** In tal caso, usare invece un messaggio di errore.
-   **Gli utenti probabilmente eseguiranno un'azione o modificheranno il comportamento come risultato del messaggio?** In caso contrario, la condizione non giustifica l'interruzione dell'utente, quindi è meglio eliminare l'avviso.
-   **La condizione è il risultato diretto di un'azione avviata dall'utente?** In caso contrario, è consigliabile usare [una notifica degli eventi non critica.](mess-notif.md)
-   **La condizione è una condizione speciale in un controllo?** In tal caso, usare invece [un balloon.](ctrl-balloons.md)
-   **Per le conferme, l'utente sta per eseguire un'azione rischiosa?** In tal caso, è appropriato un avviso se l'azione ha conseguenze significative o non può essere facilmente annullata.
-   **Per altri tipi di avvisi, l'utente deve agire ora o nell'immediato futuro?** Non visualizzare avvisi se gli utenti possono continuare a lavorare in modo produttivo senza problemi immediati. Posticipare l'avviso finché la condizione non è più immediata e pertinente.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="avoid-overwarning"></a>Evitare l'overwarning

Microsoft ha un'overwarn in microsoft Windows programmi. Il programma Windows presenta avvisi apparentemente ovunque, con avvisi relativi a elementi poco significativi. In alcuni programmi quasi tutte le domande vengono presentate come un avviso. L'overwarning fa in modo che l'uso di un programma sia un'attività rischiosa e sminuziona i problemi realmente significativi.

**Non corretto:**

![screenshot di un messaggio di avviso non necessario ](images/mess-warn-image2.png)

L'overwarning rende il programma pericoloso e sembra che sia stato progettato da persone.

Il semplice rischio di perdita di dati o un problema futuro da solo non è sufficiente per chiamare un avviso. Inoltre, eventuali risultati indesiderati dovrebbero essere imprevisti o imprevisti e non essere facilmente corretti. In caso contrario, è possibile che qualsiasi errore dell'utente possa comportare la perdita di dati o un potenziale problema di qualche tipo e causare un avviso.

### <a name="characteristics-of-good-warnings"></a>Caratteristiche degli avvisi di qualità

Avvisi di qualità:

-   **Coinvolgere il rischio.** Gli avvisi di qualità avvisano gli utenti di qualcosa di significativo.

**Non corretto:**

![screenshot di 'do you want to exit?' warning ](images/mess-warn-image3.png)

E allora? Questa conferma presuppone che gli utenti spesso escono dai programmi per errore.

-   **Avere rilevanza immediata.** Non solo gli utenti devono fare attenzione, ma ora devono fare attenzione. Gli utenti in genere non sono interessati ai problemi che potrebbero avere in un secondo momento, purché possano lavorare ora.

**Non corretto:**

![screenshot dell'avviso di batteria in esaurimento in tre ore ](images/mess-warn-image4.png)

In questo caso, è meglio solo avvisare l'utente in tre ore.

-   **Portare all'azione.** Come risultato dell'avviso, gli utenti devono eseguire o essere a conoscenza di un'operazione. Potrebbe essere necessario eseguire un'azione ora o in un certo momento nell'immediato futuro. Probabilmente eseguiranno un'attività in modo diverso di conseguenza. La conseguenza dell'ignorare l'avviso dovrebbe essere chiara. Gli avvisi senza azioni fanno solo in modo che gli utenti si senta paranoico.

**Non corretto:**

![Screenshot dell'avviso "Live Messenger è in esecuzione" ](images/mess-warn-image5.png)

Perché questa notifica è un avviso? Cosa dovrebbero fare gli utenti (oltre alla preoccupazione)?

-   **Non sono ovvi.** Non visualizzare un avviso che indica la conseguenza ovvia di un'azione. Si supponga, ad esempio, che gli utenti comprendono le conseguenze del non completamento di un'attività.

**Non corretto:**

![Screenshot della procedura guidata che si vuole chiudere? Avviso ](images/mess-warn-image6.png)

L'annullamento di una procedura guidata incompleta significa che l'attività non viene completata... chi ha conosciuto?

-   **Si verificano raramente.** Gli avvisi costanti diventano rapidamente inefficaci e fastidiosi. Gli utenti spesso si concentrano più sull'eliminazione dell'avviso che sulla risoluzione del problema.

**Non corretto:**

![Screenshot dell'avviso di aggiornamento delle firme antivirus ](images/mess-warn-image7.png)

È più probabile che gli utenti si concentrino sull'eliminazione dell'avviso rispetto alla risoluzione del problema sottostante.

Un messaggio che non ha queste caratteristiche potrebbe comunque essere un messaggio positivo, ma non un avviso.

### <a name="determine-the-appropriate-message-type"></a>Determinare il tipo di messaggio appropriato

Alcuni problemi possono essere presentati come un errore, un avviso o informazioni, a seconda dell'enfasi e della formulazione. Si supponga, ad esempio, che una pagina Web non possa caricare un controllo ActiveX non firmato in base alla configurazione Windows Internet Explorer corrente:

-   **Errore.** "Questa pagina non è in grado di caricare un ActiveX non firmato." Si è formulato come un problema esistente.
-   **Avviso.** "Questa pagina potrebbe non comportarsi come previsto perché Windows Internet Explorer non è configurato per caricare controlli ActiveX non firmati." o "Consenti a questa pagina di installare un controllo di ActiveX non firmato? Questa operazione da origini non attendibili può danneggiare il computer." Entrambe formulate come condizioni che possono causare problemi futuri.
-   **Informazioni.** "You have configured Windows Internet Explorer to block unsigned ActiveX controls". (formulata come dichiarazione di fatto).

**Per determinare il tipo di messaggio appropriato, concentrarsi sull'aspetto più importante del problema che gli utenti devono conoscere o su cui intervenire.** In genere, se un problema impedisce all'utente di procedere, è necessario presentarlo come errore. se l'utente può procedere, presentarlo come avviso. Creare [l'istruzione principale](text-ui.md) o altro testo corrispondente in base a tale stato attivo, quindi scegliere un'icona[(standard](vis-std-icons.md) o altro) corrispondente al testo. Il testo dell'istruzione principale e le icone devono sempre corrispondere.

### <a name="be-specific"></a>Essere specifici

Gli avvisi sono più interessanti quando le informazioni seguenti sono specifiche e chiare:

-   Origine dell'avviso.
-   Condizione specifica e potenziale problema.
-   Che cosa deve fare l'utente al riguardo.
-   Cosa accade se l'utente non fa nulla.

**Non corretto:**

![Screenshot di un avviso vago di rischio significativo ](images/mess-warn-image8.png)

In questo esempio, qual è il potenziale problema? Cosa dovrebbe fare l'utente, oltre a non usare il proiettore in rete? Senza informazioni più specifiche, tutto ciò che l'utente può fare è provare a procedere.

**Corretto:**

![Screenshot di avviso relativo a problemi e conseguenze ](images/mess-warn-image9.png)

In questo esempio il problema e le conseguenze sono chiari.

A volte esiste un potenziale problema legittimo che è importante informare gli utenti, ma la soluzione e le conseguenze non sono note con certezza. Anziché fornire un avviso vago, essere specifici fornendo le informazioni più probabili o l'esempio più comune.

**Corretto:**

![Screenshot dell'avviso di errore di rete e delle soluzioni ](images/mess-warn-image10.png)

In questo esempio l'avviso viene reso specifico fornendo la soluzione più probabile.

Tuttavia, in questi casi, usare una formulazione che indica che esistono altre possibilità. In caso contrario, gli utenti potrebbero essere in errore.

**Non corretto:**

![Screenshot dell'avviso di scollegamento del cavo di rete ](images/mess-warn-image11.png)

**Corretto:**

![Screenshot del cavo potrebbe essere unplugged warning ](images/mess-warn-image12.png)

Nell'esempio non corretto, gli utenti saranno confusi se il cavo è chiaramente collegato.

**Se si eservino solo due operazioni...**

1. Non sopravavare. Limitare gli avvisi alle condizioni che comportano rischi e sono immediatamente rilevanti, utilizzabili, non ovvie e poco frequenti. In caso contrario, rimuovere o riformizza il messaggio.

2. Fornire informazioni specifiche e utili.

## <a name="usage-patterns"></a>Modelli di utilizzo

Gli avvisi hanno diversi modelli di utilizzo:




| | | <strong>Consapevolezza</strong><br /> Rendere l'utente a conoscenza di una condizione o di un potenziale problema, ma l'utente potrebbe non avere a che fare ora. <br /> | <img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br /><img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br /><img src="images/mess-warn-image15.png" alt="Screen shot of 'caps-lock-is-on' warning " /><br /><img src="images/mess-warn-image16.png" alt="Screen shot of 'TPM-not-found' warning " /><br /> Esempi di avvisi di sensibilizzazione.<br /> Gli avvisi di sensibilizzazione hanno la presentazione seguente: <br /><ul><li><strong>Istruzione principale:</strong> Descrivere la condizione o il potenziale problema.</li><li><strong>Istruzioni supplementari:</strong> Spiegare l'implicazione e il motivo per cui è importante.</li><li><strong>Pulsanti commit:</strong> Vicino.</li></ul> | | <strong>Prevenzione degli errori</strong><br /> Rendere gli utenti consapevoli delle informazioni che potrebbero impedire un problema, soprattutto quando si effettuano scelte. <br /> | Gli avvisi di prevenzione degli errori vengono presentati meglio usando un'icona di avviso sul posto e un testo esplicativo. <br /><img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br /><img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br /> Esempi di avvisi di prevenzione degli errori.<br /> | | <strong>Problema imminente</strong><br /> L'utente deve eseguire ora un'operazione per evitare un problema imminente. <br /> | <img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br /> Esempio di avviso di problema imminente.<br /> Gli avvisi di problema imminenti hanno la presentazione seguente: <br /><ul><li><strong>Istruzione principale:</strong> Descrivere l'operazione che l'utente deve eseguire ora.</li><li><strong>Istruzioni supplementari:</strong> Spiegare la condizione e il motivo per cui è importante.</li><li><strong>Pulsanti commit:</strong> Un pulsante di comando o un collegamento di comando per ogni opzione oppure OK se l'azione si verifica all'esterno della finestra di dialogo.</li></ul> | | <strong>Conferma dell'azione rischiosa</strong><br /> Verificare che l'utente voglia procedere con un'azione che presenta un rischio e non può essere facilmente annullata. <br /> | <img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br /> Esempio di conferma dell'azione rischiosa.<br /> Le conferme di azioni rischiose hanno la presentazione seguente: <br /><ul><li><strong>Istruzione principale:</strong> Porre una domanda per determinare se l'utente vuole procedere.</li><li><strong>Istruzioni supplementari:</strong> Spiegare i motivi non ovvi per cui l'utente potrebbe non voler procedere.</li><li><strong>Pulsanti commit:</strong> Sì, No.</li></ul>Per linee guida su questo modello, vedere <a href="mess-confirm.md">Conferme</a>. <br /> | 




 

## <a name="guidelines"></a>Indicazioni

### <a name="presentation"></a>Presentazione

-   **Scegliere l'interfaccia utente della presentazione in base al tipo di informazioni:**



| Interfaccia utente  | Utilizzo ottimale per |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Finestre di dialogo modali<br/> | Avvisi critici (incluse le conferme) a cui gli utenti devono rispondere ora.<br/>                                                 |
| Sul posto<br/>           | Informazioni che potrebbero impedire un problema, soprattutto quando gli utenti effettuano scelte.<br/>                                         |
| Banner<br/>            | Informazioni che potrebbero impedire un problema, soprattutto quando sono correlate al completamento di un'attività.<br/>                                     |
| Notifiche<br/>      | Eventi significativi o stato che possono essere ignorati in modo sicuro, almeno temporaneamente.<br/>                                              |
| Palloncini<br/>           | Un controllo si trova in uno stato che influisce sull'input. Questo stato è probabilmente imprevisto e l'utente potrebbe non rendersi conto che l'input è interessato.<br/> |



 

-   **Per le finestre di dialogo modali:**
    -   **Usare le finestre di dialogo delle attività quando appropriato per ottenere un aspetto e un layout coerenti.** I dialoghe attività Windows Vista o versioni successive, quindi non sono adatti per le versioni precedenti di Windows.
    -   **Visualizzare un solo messaggio di avviso per ogni condizione.** Ad esempio, visualizzare un singolo avviso che spiega completamente una condizione anziché descriverla un dettaglio alla volta per ogni messaggio. La visualizzazione di una sequenza di finestre di dialogo di avviso per una singola condizione è fonte di confusione e fastidiosa.
    -   **Non visualizzare un avviso più di una volta per ogni condizione.** Gli avvisi costanti diventano rapidamente inefficaci e fastidiosi. Gli utenti spesso si concentrano più sull'eliminazione dell'avviso che sulla risoluzione del problema. Se è necessario avvisare ripetutamente per una singola condizione, usare [l'escalation progressiva.](mess-notif.md)
-   **Non accompagnare gli avvisi con un effetto sonoro o un segnale acustico.** Questa operazione è inevasa e superflua.
    -   **Eccezione:** Se l'utente deve rispondere immediatamente, è possibile usare un effetto sonoro.

### <a name="icons"></a>Icone

-   Non posizionare un'icona di avviso nella barra del titolo di una finestra di dialogo.
-   **Usare un'icona di avviso.** Eccezioni:
    -   Se l'avviso è relativo a una funzionalità con un'icona, è possibile usare l'icona della funzionalità con una sovrapposizione di avviso.

        **Corretto:**

        ![Screenshot dell'icona di blocco con sovrimpressione dell'icona di avviso ](images/mess-warn-image21.png)

        In questo esempio l'icona della funzionalità ha una sovrapposizione di avviso.

-   Per le finestre di dialogo modali con una nota a piè di pagina di avviso, inserire l'icona di avviso nella nota a piè di pagina anziché nell'area del contenuto.

    **Corretto:**

    ![Screenshot dell'icona di avviso nella nota a piè di pagina della finestra di dialogo ](images/mess-warn-image22.png)

    In questo esempio la nota a piè di pagina ha l'icona di avviso.

Per altre linee guida ed esempi, vedere [Icone standard.](vis-std-icons.md)

### <a name="dont-show-this-message-again"></a>Non visualizzare più questo messaggio

-   **Se questa opzione è richiesta da una finestra di dialogo di avviso, riconsiderare l'avviso e la relativa frequenza.** Se ha tutte le caratteristiche di un avviso positivo (comporta rischi ed è immediatamente pertinente, fattibile, non ovvio e poco comune), non dovrebbe avere senso per gli utenti sopprimerlo.

Per altre linee guida, vedere [Finestre di dialogo](win-dialog-box.md).

### <a name="progressive-disclosure"></a>Rivelazione progressiva

-   **Se è necessario includere informazioni avanzate in un messaggio di avviso, rivelarlo** usando pulsanti di divulgazione progressiva (ad esempio, "Mostra dettagli"). In questo modo, l'avviso viene semplificato per l'utilizzo tipico. Non nascondere le informazioni necessarie perché gli utenti potrebbero non trovarle.
-   **Non usare "Mostra dettagli" a meno che non siano presenti dettagli più dettagliati.** Non è sufficiente ripristinare le informazioni esistenti in un formato diverso.

Per le linee guida sull'etichettatura, vedere [Divulgazione progressiva](ctrl-progressive-disclosure-controls.md).

### <a name="default-values"></a>Valori predefiniti

-   **Selezionare la risposta più sicura, meno distruttiva o più sicura come predefinita.**

## <a name="text"></a>Testo

### <a name="general"></a>Generale

-   **Rimuovere il testo ridondante.** Cercarlo in titoli, istruzioni principali, istruzioni supplementari, aree di contenuto, collegamenti di comando e pulsanti di commit. In genere, lasciare il testo completo nelle istruzioni e nei controlli interattivi e rimuovere la ridondanza dalle altre posizioni.
-   **Non usare i termini "avviso" o "attenzione" nel testo.** Se [usata correttamente,](vis-std-icons.md)l'icona di avviso comunica sufficientemente che gli utenti devono procedere con cautela.

**Non corretto:**

![Screenshot dell'uso non necessario dell'avviso nel testo ](images/mess-warn-image23.png)

In questo esempio il termine "avviso" non è necessario.

### <a name="titles"></a>Titoli

-   **Usare il titolo per identificare il comando o la funzionalità da cui è stato generato l'avviso.** Eccezioni:
    -   Se un avviso viene visualizzato da molti comandi diversi, è consigliabile usare il nome del programma.
    -   Se tale titolo sarebbe ridondante o confuso con l'istruzione principale, usare invece il nome del programma.

**Non corretto:**

![Screenshot del titolo della finestra di dialogo avviso di sicurezza ](images/mess-warn-image24.png)

In questo esempio, "Avviso di sicurezza" non identifica il comando o la funzionalità da cui proveniva l'avviso.

-   **Non usare il titolo per spiegare cosa fare nella finestra di** dialogo che è lo scopo dell'istruzione principale.
-   Usare [l'uso di maiuscole e minuscole](glossary.md)in stile titolo senza terminare la punteggiatura.

### <a name="main-instructions"></a>Istruzioni principali

-   L'istruzione principale per un avviso si basa sul relativo modello di progettazione:



| Modello                        | Istruzione main                                               |
|--------------------------------------|----------------------------------------------------------------------|
| Riconoscimento<br/>                 | Descrivere la condizione o il potenziale problema.<br/>              |
| Problema imminente<br/>          | Descrivere l'operazione che l'utente deve eseguire ora.<br/>                   |
| Conferma dell'azione rischiosa<br/> | Porre una domanda per determinare se l'utente vuole procedere.<br/> |



 

-   ![Screenshot di una notifica con batteria in esaurimento ](images/mess-warn-image25.png)
-   In questo esempio, la notifica di batteria in esaurimento è un avviso di riconoscimento, quindi l'istruzione principale descrive la condizione.
-   ![Screenshot dell'avviso immediato della batteria di modifica ](images/mess-warn-image1.png)
-   In questo esempio la finestra di dialogo batteria in esaurimento è un problema imminente, quindi l'istruzione principale descrive le attività che l'utente deve eseguire ora.
-   **Usare concisa una sola frase completa.** Rimuovere l'istruzione principale fino alle informazioni essenziali. Se è necessario spiegare altro, usare un'istruzione supplementare.
-   **Usare parole come "now" e "immediately" se l'utente deve agire immediatamente.** Non usare queste parole se non c'è urgenza.
-   **Essere specifici se sono presenti oggetti coinvolti, assegnare i relativi nomi completi.**
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)

### <a name="supplemental-instructions"></a>Istruzioni supplementari

-   L'istruzione supplementare per un avviso si basa sul relativo modello di progettazione:



| Modello            | Istruzione supplementare                                            |
|--------------------------------------|------------------------------------------------------------------------------------|
| Riconoscimento<br/>                 | Spiegare l'implicazione e il motivo per cui è importante.<br/>                        |
| Problema imminente<br/>          | Spiegare la condizione e il motivo per cui è importante.<br/>                          |
| Conferma dell'azione rischiosa<br/> | Spiegare i motivi non ovvi per cui l'utente potrebbe non voler procedere.<br/> |



 

-   **Non ripetere l'istruzione principale con una formulazione leggermente diversa.** Omettere invece l'istruzione supplementare se non sono presenti altre istruzioni da aggiungere.
-   Usare frasi complete, lettere maiuscole in stile frase e punteggiatura finale.

### <a name="commit-buttons"></a>Pulsanti di commit

-   Per le finestre di dialogo di avviso, i pulsanti di commit si basano sul relativo modello di progettazione:



| Modello               | Pulsanti di commit        |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Riconoscimento<br/>                 | Quasi. Non usare OK perché suggerisce che i potenziali problemi sono ok.<br/>                              |
| Problema imminente<br/>          | Un pulsante di comando o un collegamento di comando per ogni opzione oppure OK se l'azione si verifica all'esterno della finestra di dialogo.<br/> |
| Conferma dell'azione rischiosa<br/> | Sì, No.<br/>                                                                                             |



 

-   **Non corretto:**
-   ![Screenshot della finestra di dialogo di avviso con il pulsante OK ](images/mess-warn-image26.png)
-   I problemi non sono ok, quindi usare Close.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento agli avvisi:

-   Se l'avviso pone una domanda, fare riferimento a un avviso in base alla domanda; In caso contrario, usare l'istruzione main. Se la domanda o l'istruzione principale è lunga o dettagliata, riepilogarla.
-   Se necessario, è possibile fare riferimento a una finestra di dialogo di avviso come messaggio.
-   Quando possibile, formattare il testo usando il grassetto. In caso contrario, inserire il testo tra virgolette solo se necessario per evitare confusione.

Esempio: nel messaggio Vuoi visualizzare gli **elementi non sicuri?** fai clic su Sì.

 

