---
title: Conferme
description: Una conferma è una finestra di dialogo modale che chiede se l'utente vuole procedere con un'azione.
ms.assetid: 086302cd-c8a1-479c-87be-580945e5d3e6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: cbfe45319051e79bcbcf57486c99f12e38ab6658
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474447"
---
# <a name="confirmations"></a>Conferme

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Una conferma è una finestra di dialogo modale che chiede se l'utente vuole procedere con un'azione.

![Screenshot che mostra un Blocco note 'vuoi salvare le modifiche?' dell'applicazione di condivisione.](images/mess-confirm-image1.png)

Una conferma tipica.

Le conferme hanno queste caratteristiche essenziali:

-   Vengono visualizzati come risultato diretto di un'azione avviata dall'utente.
-   Verificano che l'utente voglia procedere con l'azione.
-   Sono costituiti da una domanda semplice e da due o più risposte.

Le conferme sono particolarmente utili quando l'azione richiede all'utente di effettuare una scelta pertinente e distinta che non può essere eseguita in un secondo momento. Questa scelta comporta spesso un elemento di rischio che non è ovvio per l'utente, ma il rischio non è essenziale per le conferme. Questi elementi sono necessari per giustificare l'interruzione della risposta a un dialogo modale.

Al contrario, [i messaggi di](mess-warn.md) avviso presentano una condizione che potrebbe causare un problema in futuro. La loro caratteristica fondamentale è che comportano il rischio:

-   Comportano una potenziale perdita di uno o più degli elementi seguenti:
    -   Un asset prezioso, ad esempio perdita di dati o perdita finanziaria.
    -   Accesso o integrità del sistema.
    -   Privacy o controllo sulle informazioni riservate.
    -   Tempo dell'utente (una quantità significativa, ad esempio 30 secondi o più).
-   Hanno conseguenze impreviste o impreviste.
-   Richiedono ora una gestione corretta perché gli errori non possono essere risolti facilmente e possono anche essere irreversibili.

Se una conferma comporta rischi, può essere considerata anche un avviso. Di conseguenza, si applicano anche le linee guida per i messaggi di avviso.

**Nota:** Le linee guida relative [a finestre di](win-dialog-box.md)dialogo, messaggi [di](mess-error.md)errore, [layout](vis-layout.md)e messaggi [di](mess-warn.md) avviso vengono presentate in articoli separati.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, prendi in considerazione queste domande:

-   **All'utente viene posta una domanda per procedere con un'azione con due o più risposte?** In caso contrario, il messaggio non è una conferma.
-   **L'interfaccia utente presenta un errore o un problema che si è verificato?** In caso contrario, usare un [messaggio di](mess-error.md) errore.
-   **Procedere con l'azione richiede all'utente di effettuare una scelta che non dispone di un'impostazione predefinita appropriata?** In tal caso, potrebbe essere appropriata una conferma.
-   **Esiste una progettazione alternativa che elimina la necessità di conferma?** La necessità di una conferma a volte indica un difetto di progettazione. Spesso esiste un'alternativa di progettazione migliore che non richiede una conferma.
-   **L'utente sta per eseguire un'azione rischiosa?** In tal caso, una conferma è appropriata se l'azione ha conseguenze significative o non può essere facilmente annullata.
-   **L'utente sta per abbandonare un'attività?** In tal caso, non confermare. Si supponga che gli utenti comprendono le conseguenze del non completamento di un'attività.
-   **L'azione ha conseguenze di cui gli utenti potrebbero non essere a conoscenza?** In tal caso, potrebbe essere appropriata una conferma.
-   **Dato il contesto corrente, è probabile che gli utenti eseereranno un'azione in errore?** In tal caso, potrebbe essere appropriata una conferma.
-   **Gli utenti eseguono spesso l'azione?** In tal caso, prendere in considerazione una progettazione alternativa. Le conferme frequenti sono fastidiose e hanno poco valore perché gli utenti imparano a rispondere senza pensare.
-   **L'azione ha implicazioni per la sicurezza?** In tal caso, potrebbe essere necessaria una conferma anche se i test precedenti indicano il contrario.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="unnecessary-confirmations-are-annoying"></a>Le conferme non necessarie sono fastidiose

La prima Windows conferma mai creata è stata così:

![Screenshot di 'sei sicuro?' Conferma ](images/mess-confirm-image2.png)

Conferma fastidiosa originale.

Si è trattata di un inizio molto negativo. Se si vuole che gli utenti odino il programma, basta spargere conferme come questa in tutto. Per comprendere il motivo, considerare il punto di vista dell'utente. L'utente ha appena chiesto di eseguire un'azione in base alla definizione di una conferma, quindi, a meno che qualcosa non sia stato in qualche modo fatto clic o premuto accidentalmente, naturalmente l'utente vuole procedere.

Non solo le conferme non necessarie sono fastidiose, ma non sono efficaci per proteggere l'utente dagli errori. Gli utenti individuano rapidamente quando un programma ha conferme non necessarie e la risposta naturale è ignorarle il più rapidamente possibile, spesso senza leggere. Di conseguenza, tali conferme non fanno altro che aggiungere un passaggio aggiuntivo a queste attività.

Non usare le conferme solo perché è possibile che gli utenti commettono un errore. **Le conferme sono invece più efficaci se usate per confermare azioni con conseguenze significative o impreviste.** Le buone conferme non confermano mai l'ovvio; devono comunicare qualcosa che gli utenti devono essere a conoscenza di un buon motivo per non continuare. E vengono usati solo quando sono effettivamente necessari da un'azione, ad esempio per chiedere agli utenti di salvare le modifiche solo quando sono presenti modifiche che vale la pena salvare. Questa operazione richiede l'attenzione dell'utente solo quando è effettivamente garantito.

Per altri tipi di conferme, esiste spesso un'alternativa di progettazione migliore rispetto a forzare gli utenti a rispondere a una domanda.

### <a name="consider-the-design-alternatives"></a>Considerare le alternative di progettazione

Ecco alcune alternative di progettazione che eliminano la necessità di conferme di routine:

-   **Evitare errori.** Progettare attività in modo che gli errori significativi siano difficili da eseguire accidentalmente. Ad esempio, separare fisicamente i comandi distruttivi da altri comandi e richiedere il completamento di più azioni.
-   **Fornire l'annullamento.** Consente di ripristinare le azioni. Ad esempio, l'eliminazione di un file in Microsoft Windows in genere non richiede una conferma perché i file eliminati possono essere recuperati dal Cestino. Si noti che se un'azione è molto semplice da eseguire, potrebbe essere sufficiente ripetere l'azione solo per gli utenti.
-   **Inviare commenti e suggerimenti.** Rendere ovvi i risultati indesiderati. Fornire l'annullamento da solo non è sufficiente se gli utenti non si rendono conto quando commettono un errore. Ad esempio, l'effetto della manipolazione diretta ,ad esempio un'operazione di trascinamento della selezione, deve essere sempre ovvio.
-   **Presupporre il risultato probabile, ma semplificare la modifica.** Se non si è certi di cosa vogliono gli utenti, ma esiste una scelta probabile, sicura e sicura, presupporre questa scelta, chiarire cosa è successo e semplificare la modifica usando un menu di scelta rapida. Ad esempio, Microsoft Word presuppone che gli utenti vogliano scrivere correttamente le parole. Se riconosce una parola con errori di ortografia e conosce l'ortografia probabilmente corretta, Word esegue automaticamente la correzione, ma consente agli utenti di ripristinare.
-   **Eliminare completamente la scelta.** Se la scelta non è importante, agli utenti non interessa. È meglio [semplificare](/previous-versions//dn742474(v=vs.85)) il programma ed eliminare la scelta.

### <a name="make-confirmations-require-thought"></a>Le conferme richiedono un'idea

Per ottenere un valore per una conferma, gli utenti devono comprendere il motivo per cui non procedere. A volte il motivo è ovvio, come quando gli utenti chiudono un documento con modifiche che non sono state salvate:

![Screenshot che mostra un Paint 'Vuoi salvare le modifiche?' .](images/mess-confirm-image3.png)

In questo esempio il motivo della conferma è ovvio.

In altre situazioni, il motivo potrebbe non essere così ovvio.

Quando si scelgono le etichette [](win-dialog-box.md) dei pulsanti di commit per le finestre di dialogo, le linee guida generali sono la scelta di etichette che sono risposte specifiche all'istruzione principale. Ciò comporta un processo decisionale efficiente perché gli utenti devono leggere una quantità minima di testo per procedere. Tuttavia, questo obiettivo di efficienza può essere controproducente per le conferme. Prendere in considerazione questo esempio:

**Non corretto:**

![Screenshot di conferma con il pulsante di disinstallazione ](images/mess-confirm-image4.png)

In questo esempio, la risposta corretta richiede un'idea.

Se si presenta questa conferma immediatamente dopo che l'utente ha dato il comando Disinstalla, è probabile che la risposta dell'utente sia "Naturalmente si vuole disinstallare!" L'utente farà clic su Disinstalla senza dare una seconda idea.

Per le conferme, non è necessario che gli utenti prendono decisioni rapide ed emotive. Per invitare gli utenti a pensare alla loro risposta, è necessario fornire un piccolo ostacolo alla velocità del processo decisionale. Quando è pratico, è in genere meglio eseguire questa operazione tramite la formulazione attentamente dei pulsanti di commit. Ad esempio, è possibile usare un linguaggio aggiuntivo per indicare che esiste un motivo per non continuare.

**Migliore:**

![Screenshot del pulsante "Disinstalla comunque" ](images/mess-confirm-image5.png)

In questo esempio viene aggiunto "anyway" all'etichetta del pulsante commit per indicare che la conferma indica un motivo per non continuare.

Se questo approccio non è pratico, è possibile usare i pulsanti di commit Sì/No.

**Anche meglio:**

![Screenshot di conferma con pulsanti Sì/No ](images/mess-confirm-image6.png)

In questo esempio, l'uso dei pulsanti di commit Sì/No impone agli utenti di leggere almeno l'istruzione principale.

### <a name="provide-all-the-information"></a>Fornire tutte le informazioni

Se si desidera porre una domanda, è necessario fornire informazioni sufficienti per consentire agli utenti di rispondere a tale domanda in modo intelligente. Si consideri la finestra di dialogo Conferma sostituzione file Windows XP:

![Screenshot della finestra di dialogo "Conferma sostituzione file" ](images/mess-confirm-image7.png)

Finestra Windows finestra di dialogo Conferma sostituzione file di XP.

Questa conferma fornisce tutte le informazioni necessarie agli utenti per rispondere alla domanda? Prima di rispondere, considerare gli scenari utente più comuni:

-   Copiare (o spostare) l'altro file, sostituendo quello esistente.
-   Mantenere il file esistente, senza copiare o spostare l'altro file.
-   Mantenere o copiare il file più recente (scenario principale).
-   Mantenere il file esistente o copiare l'altro file, a seconda di criteri quali il contenuto e le dimensioni del file.
-   Mantenere il file esistente e copiare l'altro file con un nome diverso.
-   Annullare l'operazione in caso di errore o imprevisto.

Gli utenti possono ottenere lo scenario 1 facendo clic su Sì e scenario 2 facendo clic su No. Possono ottenere lo scenario 3 confrontando le date del file e facendo clic sul pulsante appropriato, ma si noti quanto si pensa di determinare il file più recente e quindi determinare il pulsante appropriato, in particolare per quello che è probabile che sia lo scenario più comune.

Anche gli scenari 4, 5 e 6 sono sorprendentemente difficili. Le dimensioni dei file vengono arrotondate, quindi, ad esempio, non è possibile determinare se questi file hanno le stesse dimensioni o anche se sono lo stesso file. Le icone sono relative all'applicazione usata per aprire il file, quindi gli utenti devono aprire i file per esaminare e confrontare il contenuto. Avere anteprime del contenuto del file sarebbe molto più utile per rispondere alla domanda.

La conferma copia file da Windows Vista offre un processo molto migliore per gestire questi scenari fornendo altre informazioni e aggiungendo l'opzione per mantenere entrambi i file:

![Screenshot della finestra di dialogo "Copia file" ](images/mess-confirm-image8.png)

Conferma Windows file di copia di Vista.

### <a name="provide-specific-useful-information"></a>Fornire informazioni specifiche e utili

Se si desidera porre una domanda, assicurarsi che gli utenti comprendano la domanda e le implicazioni delle risposte alternative. Si consideri questa Windows Internet Explorer di sicurezza:

![Screenshot di conferma con una domanda vaga ](images/mess-confirm-image9.png)

Una vaga conferma di sicurezza.

Questa conferma pone una domanda a cui gli utenti non possono rispondere in modo intelligente. L'utente ha richiesto Windows Internet Explorer visualizzare una pagina e questo messaggio la sconsiglia in modo implicito tramite la formulazione del testo ed evidenziando No come scelta predefinita.

Il problema di sicurezza specifico che la pagina pone non è sufficientemente spiegato, quindi il rischio di continuare non è chiaro. Quali informazioni nella conferma causerebbero all'utente di fare clic su No? A causa della vaghezza del messaggio, è probabile che la conferma non scoraggi gli utenti di continuare, ma farà in modo che si senta in disod di farlo.

Perché questa conferma sia utile, deve fornire informazioni più specifiche che potrebbero far decidere all'utente di non procedere. In generale, per ogni risposta in una conferma, prendere in considerazione gli scenari che la richiedono e assicurarsi che siano disponibili informazioni sufficienti per consentire agli utenti di sceglierla. Offrire scelte, non dilemmi.

### <a name="how-to-determine-if-a-confirmation-is-necessary"></a>Come determinare se è necessaria una conferma

L'analisi degli scenari e la probabilità di scegliere ogni risposta suggerisce un modo sistematico per determinare se è necessaria una conferma. Se è probabile che gli utenti selezionano tutte le risposte, la conferma è necessaria e utile. Tuttavia, se è probabile una sola risposta (ad esempio il 98% del tempo), la conferma è chiaramente superflua e deve essere rimossa. Si noti che le conferme relative a problemi di sicurezza, legali e di sicurezza sono possibili eccezioni.

![Screenshot di 'Vuoi modificare le impostazioni?' ](images/mess-confirm-image10.png)

Questa conferma è necessaria? Gli utenti selezioneranno mai No? È possibile ma molto improbabile. Questa conferma deve essere rimossa.

**Se si eservino solo tre operazioni...**

1. Assicurarsi che la conferma sia effettivamente necessaria. Ci dovrebbe essere un motivo legittimo e chiaro per non procedere e una possibilità che a volte gli utenti non lo siano.

2. Se il motivo della conferma non è immediatamente ovvio, scegliere pulsanti di commit che incoraggino gli utenti a pensare alla risposta. In genere, questa operazione viene eseguita formulazione della conferma come una domanda sì o no e fornendo risposte completamente autosplicative o Sì/No.

3. Prendere in considerazione tutti gli scenari e fornire le informazioni necessarie per rispondere alla domanda in modo intelligente.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le conferme hanno diversi modelli di utilizzo:



|   Utilizzo                                                                                                                                                                    |    Esempio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Conferme di routine**<br/> verificare che l'utente voglia procedere con un'azione di routine a basso rischio. <br/>                                              | Queste conferme sono in genere formulate "sei sicuro...?" e spesso hanno una casella di controllo Non visualizzare più questo messaggio per ridurre al minimo i fastidi. <br/> ![Screenshot di "Spostare la cartella nel Cestino?". ](images/mess-confirm-image11.png)<br/> ![Screenshot di 'Don't show message again' (Non visualizzare più il messaggio) ](images/mess-confirm-image12.png)<br/> Esempi di conferme di routine.<br/> **Nota:** Questo modello non è in genere necessario e deve essere evitato.<br/>                                                                                                                                                                                                                                                                                        |
| **Conferme di azioni rischiose**<br/> verificare che l'utente voglia procedere con un'azione che presenta un rischio e non può essere facilmente annullata. <br/>            | Poiché hanno rischi, queste conferme hanno in genere un'icona di avviso. <br/> ![Screenshot che mostra un esempio di conferma della formattazione del volume.](images/mess-confirm-image13.png)<br/> ![Screenshot che mostra un esempio di conferma dell'eliminazione permanente.](images/mess-confirm-image14.png)<br/> Esempi di conferme di azioni rischiose.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Conferme impreviste delle conseguenze**<br/> verificare che l'utente voglia procedere con un'azione con conseguenze impreviste o impreviste. <br/> | Oltre a porre una domanda, queste conferme indicano le conseguenze impreviste. poiché hanno conseguenze impreviste, queste conferme hanno in genere un'icona di avviso. <br/> ![Screenshot di "Chiudi tutte le schede?". Conferma ](images/mess-confirm-image15.png)<br/> ![Screenshot di "Annullare l'installazione?". Conferma ](images/mess-confirm-image16.png)<br/> esempi di conferme impreviste delle conseguenze.<br/> Tuttavia, questo modello richiede che le conseguenze siano realmente impreviste. <br/> **Errato:**<br/> ![Screenshot di 'spegni key logger?' Conferma ](images/mess-confirm-image17.png)<br/> Le conseguenze sono da intendersi in questo caso, quindi si tratta di una conferma di routine.<br/> |
| **Precisazioni**<br/> chiarire come l'utente vuole procedere con un'azione con conseguenze potenzialmente ambigue o impreviste. <br/>             | Le operazioni di trascinamento della selezione possono comportare chiarimenti se l'effetto dell'operazione può essere interpretato erroneamente. <br/> ![screenshot di 'change only this occurrence?'](images/mess-confirm-image18.png)<br/> ![Screenshot di "Salva sempre all'uscita?". Conferma ](images/mess-confirm-image19.png)<br/> Esempi di chiarimenti.<br/> **Nota:** Questo modello deve essere evitato perché è consigliabile progettare azioni senza conseguenze ambigue e presupporre il risultato desiderato più probabile. <br/>                                                                                                                                                                                                                                     |
| **Conferme di sicurezza**<br/> verificare che l'utente voglia procedere con un'azione con conseguenze per la sicurezza. <br/>                                   | ![screenshot di "do you want to run this software?". ](images/mess-confirm-image20.png)<br/> ![Screenshot di "memorizza password?". Conferma ](images/mess-confirm-image21.png)<br/> Esempi di conferme di sicurezza.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Conferme di motivazioniulterior**<br/> fornire informazioni su un'azione, ma presentarla come conferma. <br/>                                       | Anche se queste finestre di dialogo vengono presentate come conferme, il loro obiettivo reale è la formazione degli utenti o l'annuncio di funzionalità. <br/> ![screenshot della barra degli strumenti desiderata sulla barra delle applicazioni? ](images/mess-confirm-image22.png)<br/> Esempio di conferma della motivazione più esecutore.<br/> **Nota:** Questo modello non è consigliato perché in genere esiste un'alternativa migliore e più diretta. Ad esempio, [le animazioni sono](vis-animations.md) un modo migliore per mostrare la relazione tra causa ed effetto. <br/>                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Usare le conferme "Salva modifiche" solo in caso di modifiche significative.** Non confermare le modifiche che non sono state apportate direttamente dall'utente, ad esempio la riformattazione automatica dei documenti.

**Non corretto:**

![Screenshot che mostra un Microsoft Office Outlook 'vuoi salvare le modifiche?' dell'applicazione di condivisione.](images/mess-confirm-image23.png)

Questo esempio non è corretto se usato per un messaggio di posta elettronica o un documento vuoto che non è stato modificato dall'utente.

### <a name="icons"></a>Icone

-   Le conferme non usano le icone della barra del titolo.
-   **L'icona dell'area del contenuto per una conferma si basa sul relativo schema progettuale:**



    | Modello                                                | Icona                                                                                                                                             |
    |--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
    | Conferme di routine <br/>                | Nessuna icona. <br/>                                                                                                                         |
    | Conferme di azioni rischiose <br/>           | Icona di avviso. <br/>                                                                                                                    |
    | Conferme di conseguenza impreviste <br/> | Usare un'icona di avviso in caso di rischio, l'icona della funzionalità, se disponibile; in caso contrario, nessuna icona. <br/>                                          |
    | Precisazioni <br/>                       | Se la conferma riguarda un documento, usare l'anteprima del documento. In caso contrario, usare l'icona della funzionalità, se disponibile, o nessuna icona. <br/> |
    | Conferme di sicurezza <br/>               | Icona di avviso. <br/>                                                                                                                    |
    | Conferme di motivazioniulterior <br/>        | Nessuna icona. <br/>                                                                                                                         |



 

-   **Non usare icone di avviso per domande di routine.** In questo modo si contrasta con il tono [incoraggiante Windows](text-style-tone.md) e fa in modo che l'uso del programma sia un'attività rischiosa. Si supponga che gli utenti comprendono le conseguenze dell'annullamento di un'attività prima del completamento.

**Non corretto:**

![Screenshot di "si vuole terminare l'esercitazione?". ](images/mess-confirm-image24.png)

In questo esempio viene usata un'icona di avviso per porre una domanda di routine.

### <a name="commit-buttons"></a>Pulsanti di commit

-   **Usare risposte specifiche all'istruzione principale se il motivo della conferma è ovvio o può essere reso auto-esplicativo.**

![Screenshot di "Si vogliono salvare le modifiche?". ](images/mess-confirm-image25.png)

In questo esempio il motivo della conferma è ovvio, quindi salva e non salva correttamente.

-   **In caso contrario, usare i pulsanti Sì e No per le risposte di conferma.** In questo modo, gli utenti danno una certa idea alla conferma prima di rispondere. Non usare mai OK e Annulla per le conferme.

**Corretto:**

![Screenshot di "vuoi disinstallare i file di supporto?". ](images/mess-confirm-image26.png)

In questo esempio, l'uso dei pulsanti di commit Sì/No impone agli utenti di leggere almeno l'istruzione principale.

**Non corretto:**

![Screenshot di "Annullare la prenotazione?". ](images/mess-confirm-image27.png)

In questo esempio l'uso di OK/Cancel crea confusione.

-   **Per chiudere un programma o riavviare Windows, usare risposte specifiche all'istruzione principale.** Per evitare incomprensioni, non usare Chiudi o Sì/No a questo scopo.

**Corretto:**

![Screenshot del pulsante Riavvia windows ora](images/mess-confirm-image28.png)

**Non corretto:**

![Screenshot del pulsante Sì](images/mess-confirm-image29.png)

Nell'esempio non corretto viene usato Sì per riavviare Windows.

### <a name="command-links"></a>Collegamenti di comando

-   **Per il modello di chiarimenti, è consigliabile usare i collegamenti ai comandi per rendere chiare le alternative.**

**Accettabile:**

![screenshot di "modificare una o tutte le occorrenze?". ](images/mess-confirm-image30.png)

**Migliore:**

![screenshot della stessa domanda con i collegamenti di comando ](images/mess-confirm-image31.png)

Nell'esempio migliore, i collegamenti ai comandi rendono chiare le alternative.

-   **Presentare prima i collegamenti ai comandi usati più di frequente.** L'ordine risultante deve seguire approssimativamente la probabilità di utilizzo, ma avere anche un flusso logico.
-   Se un collegamento al comando richiede un'ulteriore spiegazione, **fornire una spiegazione supplementare.** Le spiegazioni supplementari descrivono il motivo per cui gli utenti possono scegliere l'opzione o cosa accade se si sceglie l'opzione.

Per altre linee guida ed esempi, vedere [Collegamenti ai comandi.](ctrl-command-links.md)

### <a name="default-values"></a>Valori predefiniti

-   **La risposta predefinita per una conferma si basa sul relativo schema progettuale:**



    | Modello                                                 | Risposta predefinita                                                                                |
    |--------------------------------------------------|---------------------------------------------------------------------------------|
    | Conferme di routine <br/>                | Procedere. <br/>                                                            |
    | Conferme di azioni rischiose <br/>           | Non procedere (o la scelta sicura). <br/>                                 |
    | Conferme di conseguenza impreviste <br/> | Se le conseguenze sono significative, non procedere. In caso contrario, procedere. <br/> |
    | Precisazioni <br/>                       | Risposta più probabile. <br/>                                           |
    | Conferme di sicurezza <br/>               | Non procedere. <br/>                                                      |
    | Conferme delle motivazioniulterior <br/>        | Procedere. <br/>                                                            |



 

### <a name="dont-show-this-message-again"></a>Non visualizzare più questo messaggio

-   **Usare questa opzione solo per i modelli di conferma delle routine e delle motivazioni.** Per gli altri modelli, se le informazioni sono necessarie, devono essere sempre visualizzate.
-   **Non specificare questa opzione per giustificare la visualizzazione di una conferma non necessaria.** È sufficiente eliminare la conferma.

**Non corretto:**

![Screenshot di "ignora questi promemoria?". ](images/mess-confirm-image32.png)

**Ancora non corretto:**

![Screenshot di 'Don't show message again' (Non visualizzare più il messaggio)](images/mess-confirm-image33.png)

In questi esempi l'aggiunta di un'opzione Non visualizzare più questo messaggio non consente di correggere una conferma non necessaria.

Per altre linee guida, vedere [Finestre di dialogo](win-dialog-box.md).

### <a name="bulk-operations"></a>Operazioni bulk

-   Per le conferme che si applicano alle operazioni bulk, fornire un'opzione per applicare la conferma all'intera operazione.

![Screenshot di 'Eseguire questa operazione per tutti gli elementi?' Casella di controllo ](images/mess-confirm-image34.png)

In questo esempio è disponibile un'opzione per le operazioni bulk.

-   Eliminare o posticipare le conferme in un'operazione in blocco.

**Non corretto:**

![Screenshot della finestra di dialogo "conferma eliminazione file" ](images/mess-confirm-image35.png)

In questo esempio, Windows Explorer in Windows XP conferma ogni file di sola lettura durante uno spostamento bulk di file. È meglio semplicemente copiare i file di sola lettura senza chiedere o posticipare la gestione di questi file e presentare la conferma alla fine dell'attività.

### <a name="progressive-disclosure&quot;></a>Rivelazione progressiva

-   **Se è necessario includere informazioni avanzate in un messaggio di conferma, rivelarlo usando pulsanti di divulgazione progressiva (ad esempio, &quot;Mostra dettagli").** In questo modo si semplifica la conferma per l'utilizzo tipico. Non nascondere le informazioni necessarie perché gli utenti potrebbero non trovarle.
-   **Non usare "Mostra dettagli" a meno che non siano presenti dettagli più dettagliati.** Non è sufficiente ripristinare le informazioni esistenti in un formato diverso.

Per le linee guida sull'etichettatura, vedere [Divulgazione progressiva](ctrl-progressive-disclosure-controls.md).

### <a name="user-account-control"></a>Controllo dell'account utente

-   **Non usare l'interfaccia utente di elevazione del controllo dell'account utente come sostituzione di una conferma.** Se un'azione richiede una conferma, usare una finestra di dialogo separata. Durante [l'interfaccia utente di](winenv-uac.md)elevazione dei privilegi, gli utenti devono concentrarsi sul fatto che l'attività sia stata avviata e se il programma sia attendibile.
-   **Visualizzare la conferma prima dell'interfaccia utente di elevazione dei privilegi.** Questa operazione elimina le elevazioni non necessarie.

## <a name="text"></a>Testo

### <a name="general"></a>Generale

-   **Rimuovere il testo ridondante.** Cercare testo ridondante in titoli, istruzioni principali, istruzioni supplementari, aree di contenuto, collegamenti ai comandi e pulsanti di commit. In genere, lasciare il testo completo nelle istruzioni e nei controlli interattivi e rimuovere la ridondanza dalle altre posizioni.
-   **Non usare "warning" o "caution" nel testo.** Se gli utenti devono procedere con cautela, indicare questa opzione usando invece un'icona di avviso.

**Non corretto:**

![Screenshot di conferma della formattazione del volume ](images/mess-confirm-image36.png)

In questo esempio il termine "avviso" non è necessario.

### <a name="titles"></a>Titoli

-   **Usare il titolo per identificare il comando o la funzionalità da cui proveniva la conferma. Eccezioni:**
    -   Se viene visualizzata una conferma da molti comandi diversi, è consigliabile usare il nome del programma.
    -   Se tale titolo sarebbe ridondante o confuso con l'istruzione principale, usare invece il nome del programma.

Tuttavia, se la conferma deriva da un'attività a esecuzione lunga e può essere visualizzata anche dopo l'avvio dell'attività, usare sempre il comando o la funzionalità per identificare chiaramente il contesto.

-   **Non usare il titolo per spiegare cosa fare nella finestra di** dialogo che è lo scopo dell'istruzione principale.
-   Se aggiunge chiarezza, iniziare il titolo con la parola Confirm.
-   **Per le conferme di azioni rischiose, è possibile aggiungere il nome dell'oggetto interessato per una maggiore enfasi.**

![Screenshot del titolo della finestra di dialogo 'format f drive' ](images/mess-confirm-image13.png)

In questo esempio l'unità da formattare è inclusa nel titolo.

-   Usare [l'uso di maiuscole e minuscole](glossary.md)in stile titolo senza terminare la punteggiatura.

### <a name="main-instructions"></a>Istruzioni principali

-   **L'istruzione principale per una conferma è basata sul modello di progettazione:**



    | Modello                                                 | Istruzione main                                                                                                                                                                                                                                                                                                                                                                                                          |
    |--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Conferme impreviste delle conseguenze <br/> | stato della conseguenza non intenzionale.<br/> **exception:** se una domanda che chiede se l'utente vuole procedere implica chiaramente la conseguenza non intenzionale, porre la domanda. <br/> ![Screenshot di "Chiudi tutte le schede?". Conferma ](images/mess-confirm-image15.png)<br/> In questo esempio, chiedere all'utente di procedere sufficientemente comunica le conseguenze dell'azione.<br/> |
    | Tutti gli altri <br/>                           | Porre una singola domanda per determinare se l'utente vuole procedere. <br/>                                                                                                                                                                                                                                                                                                                              |



 

-   **Usare concisa una sola frase completa.** Rimuovere l'istruzione principale fino alle informazioni essenziali. Se è necessario spiegare altro, usare un'istruzione supplementare.
-   **Essere specifici se sono presenti oggetti coinvolti, assegnare i relativi nomi completi.**
-   **Usare formulazioni positive.** La formulazione positiva è più facile da comprendere per gli utenti.

**Corretto:**

Si vuole abilitare la condivisione di file e stampanti?

**Non corretto:**

Disabilitare la condivisione di file e stampanti?

Tuttavia, la formulazione deve corrispondere al comando associato, anche se il comando è con frase negativa; quindi, ad esempio, usare disable per confermare un comando Disable.

-   Anche se non esistono regole rigorose per la formulazione, queste frasi di conferma comuni **hanno la connotazione indicata:**



    | Frase                                                            | Connotazione                                                            |
    |-------------------------------------------------------------|-------------------------------------------------------------|
    | Si è certi di voler \[ eseguire un'azione? \] <br/> | Conferma del risultato diretto di una richiesta utente. <br/> |
    | Si vuole eseguire \[ \] un'azione? <br/>           | Conferma di un effetto collaterale di una richiesta utente. <br/>     |
    | Si vuole selezionare \[ un \] risultato? <br/>          | Serve un chiarimento. <br/>                           |
    | \[Eseguire un'azione \] ? <br/>                          | Nessuna connotazione. <br/>                                 |



 

-   Per le conferme di azioni rischiose, usare il termine in modo permanente per indicare che un'azione non può essere annullata.

![Screenshot di conferma dell'eliminazione permanente ](images/mess-confirm-image37.png)

In questo esempio , "permanently" indica che l'azione non può essere annullata.

-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)

### <a name="supplemental-instructions"></a>Istruzioni supplementari

-   **L'istruzione supplementare per una conferma si basa sul modello di progettazione:**

    
| | | <strong>Modello</strong><br /> | <strong>Istruzione supplementare</strong><br /> | | Conferme impreviste delle conseguenze <br /> | Porre una singola domanda per determinare se l'utente vuole procedere. <br /> | | Tutti gli altri <br /> | Spiegare eventuali motivi non ovvi per cui l'utente potrebbe non voler procedere. Questi motivi includono: <br /><ul><li>Potenziale perdita di uno o più degli elementi seguenti:    <ul><li>Asset prezioso, ad esempio perdita di dati o perdita finanziaria.</li><li>Accesso o integrità del sistema.</li><li>Privacy o controllo sulle informazioni riservate.</li></ul></li><li>Azioni irreversibili.</li></ul> | 


    

     

-   **Non ripetere l'istruzione principale con una formulazione leggermente diversa.** In alternativa, omettere l'istruzione supplementare se non sono presenti altri elementi da aggiungere.
-   Per conferme di conseguenza impreviste, è consigliabile usare comunque il termine per indicare **concisamente** che esiste un motivo per non continuare nel caso in cui l'utente trascura l'istruzione principale. Per altre informazioni, vedere Concetti di progettazione.
-   Usare frasi complete, lettere maiuscole in stile frase e punteggiatura finale.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle conferme:

-   Fare riferimento a una conferma in base al titolo se il titolo è specifico della conferma, ovvero non del nome del programma. In caso contrario, fare riferimento a esso tramite l'istruzione principale.
-   Se necessario, è possibile fare riferimento a una finestra di dialogo di conferma come messaggio.
-   Usare il testo esatto, inclusa la relativa maiuscola.
-   Quando possibile, formattare il testo in grassetto. In caso contrario, inserire il testo tra virgolette solo se necessario per evitare confusione.

Esempio: nel messaggio **Copia file** fare clic sul file più recente.

