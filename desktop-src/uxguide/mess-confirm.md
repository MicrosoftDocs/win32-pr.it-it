---
title: Conferme
description: Una conferma è una finestra di dialogo modale che chiede se l'utente desidera procedere con un'azione.
ms.assetid: 086302cd-c8a1-479c-87be-580945e5d3e6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b979987daa4cf2c40308a0cda9c23b08b73f4795
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104565685"
---
# <a name="confirmations"></a>Conferme

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Una conferma è una finestra di dialogo modale che chiede se l'utente desidera procedere con un'azione.

![Screenshot che mostra un blocco note ' salvare le modifiche?' dell'applicazione di condivisione.](images/mess-confirm-image1.png)

Una conferma tipica.

Le conferme hanno queste caratteristiche essenziali:

-   Vengono visualizzati come il risultato diretto di un'azione iniziata dall'utente.
-   Verificano che l'utente voglia procedere con l'azione.
-   Sono costituiti da una semplice domanda e da due o più risposte.

Le conferme sono particolarmente utili quando l'azione richiede all'utente di effettuare una scelta pertinente e distinta che non può essere eseguita in un secondo momento. Questa scelta spesso implica alcuni elementi di rischio non evidenti per l'utente, ma il rischio non è essenziale per le conferme. Questi elementi sono necessari per giustificare l'interruzione della risposta a una finestra di dialogo modale.

Al contrario, [i messaggi di avviso](mess-warn.md) presentano una condizione che potrebbe causare un problema in futuro. La caratteristica fondamentale è che coinvolgono i rischi:

-   Che comportano una perdita potenziale di uno o più degli elementi seguenti:
    -   Una risorsa preziosa, ad esempio la perdita di dati o la perdita finanziaria.
    -   Accesso al sistema o integrità.
    -   Privacy o controllo sulle informazioni riservate.
    -   Tempo utente (un importo significativo, ad esempio 30 secondi o più).
-   Hanno conseguenze impreviste o impreviste.
-   Richiedono una corretta gestione perché gli errori non possono essere risolti facilmente e possono anche essere irreversibili.

Se una conferma comporta un rischio, può essere considerata anche un avviso. Di conseguenza, vengono applicate anche le linee guida per i messaggi di avviso.

**Nota:** Le linee guida relative alle [finestre di dialogo](win-dialog-box.md), ai [messaggi di errore](mess-error.md), al [layout](vis-layout.md)e ai [messaggi di avviso](mess-warn.md) vengono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendi in considerazione queste domande:

-   **Viene chiesto all'utente di procedere con un'azione con due o più risposte?** In caso contrario, il messaggio non è una conferma.
-   **L'interfaccia utente presenta un errore o un problema che si è verificato?** In caso affermativo, usare invece un [messaggio di errore](mess-error.md) .
-   **Continuando con l'azione è necessario che l'utente possa scegliere che non abbia un valore predefinito appropriato?** In tal caso, è possibile che sia necessaria una conferma.
-   **Esiste una progettazione alternativa che elimina la necessità della conferma?** La necessità di una conferma talvolta indica un difetto di progettazione. Spesso è disponibile un'alternativa di progettazione migliore che non richiede una conferma.
-   **L'utente sta per eseguire un'azione rischiosa?** In tal caso, una conferma è appropriata se l'azione ha conseguenze significative o non può essere annullata facilmente.
-   **L'utente sta per abbandonare un'attività?** In caso affermativo, non confermare. Si supponga che gli utenti capiscano le conseguenze del mancato completamento di un'attività.
-   **L'azione è soggetta a conseguenze che gli utenti potrebbero non essere in grado di riconoscere?** In tal caso, è possibile che sia necessaria una conferma.
-   **Dato il contesto corrente, è probabile che gli utenti eseguano un'azione in errore?** In tal caso, è possibile che sia necessaria una conferma.
-   **Gli utenti eseguono l'azione di frequente?** In tal caso, prendere in considerazione una progettazione alternativa. Le conferme frequenti sono fastidiose e hanno un valore minimo perché gli utenti imparano a rispondere senza pensare.
-   **L'azione ha implicazioni relative alla sicurezza?** In tal caso, potrebbe essere necessaria una conferma anche se i test precedenti indicano in altro modo.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="unnecessary-confirmations-are-annoying"></a>Le conferme non necessarie sono fastidiose

La prima conferma di Windows creata indubbiamente è simile alla seguente:

![la cattura di schermata di "Sei sicuro?" Conferma ](images/mess-confirm-image2.png)

La conferma originale fastidiosa.

Si tratta di un avvio molto negativo. Se si vuole che gli utenti odi il programma, è sufficiente spruzzare conferme di questo tipo in tutto. Per comprendere il motivo, prendere in considerazione il punto di vista dell'utente. L'utente ha appena richiesto di eseguire un'azione mediante la definizione di una conferma, a meno che non sia stato selezionato o premuto accidentalmente, ovviamente l'utente vuole continuare.

Non solo le conferme non solo necessarie sono fastidiose, ma non sono valide per proteggere l'utente dagli errori. Gli utenti scoprono rapidamente quando un programma non dispone di conferme inutili e la loro risposta naturale consiste nel chiuderli il più rapidamente possibile, spesso senza leggerli. Di conseguenza, tali conferme sono molto più che aggiungere un passaggio aggiuntivo a queste attività.

Non usare le conferme solo perché è possibile che gli utenti facciano un errore. **Al contrario, le conferme sono più efficaci quando vengono usate per confermare le azioni con conseguenze significative o impreviste.** Le convalide non sono mai state evidenti. devono comunicare che gli utenti devono essere a conoscenza di un buon motivo per non continuare. E vengono usati solo quando sono effettivamente necessari per un'azione, ad esempio chiedere agli utenti di salvare le modifiche solo quando sono presenti modifiche da salvare. Questa operazione richiede l'attenzione dell'utente solo quando è effettivamente garantita.

Per altri tipi di conferme, spesso è disponibile un'alternativa di progettazione migliore rispetto alla forzatura degli utenti a rispondere a una domanda.

### <a name="consider-the-design-alternatives"></a>Prendere in considerazione le alternative di progettazione

Di seguito sono riportate alcune alternative di progettazione che eliminano la necessità di conferme di routine:

-   **Impedisci errori.** Progettare le attività in modo che gli errori significativi siano difficili da eseguire accidentalmente. Ad esempio, separare fisicamente comandi distruttivi da altri comandi e richiedere il completamento di più azioni.
-   **Fornire l'annullamento.** Fornire la possibilità di ripristinare le azioni. L'eliminazione di un file in Microsoft Windows, ad esempio, in genere non richiede una conferma perché i file eliminati possono essere ripristinati dal Cestino. Si noti che se un'azione è molto semplice da eseguire, è sufficiente che gli utenti eseguano il rollforward dell'azione.
-   **Inviare commenti e suggerimenti.** Rendere evidenti i risultati indesiderati. La mancata disponibilità di Undo alone non è sufficiente se gli utenti non si rendono conto quando si commette un errore. Ad esempio, l'effetto della manipolazione diretta (ad esempio un'operazione di trascinamento della selezione) dovrebbe essere sempre ovvio.
-   **Si supponga il risultato probabile, ma è possibile modificarlo facilmente.** Se non si è certi di quali utenti desiderano, ma esiste una scelta sicura, sicura e sicura, si supponga che sia possibile scegliere di chiarire cosa è successo e semplificarne la modifica utilizzando un menu di scelta rapida. Ad esempio, in Microsoft Word si presuppone che gli utenti desiderino scrivere correttamente le parole. Se riconosce una parola digitata in modo errato e conosce l'ortografia corretta, la correzione viene eseguita automaticamente da Word, ma consente agli utenti di ripristinare.
-   **Eliminare completamente la scelta.** Se la scelta non è importante, gli utenti non sono interessati. Migliore per [semplificare](/previous-versions//dn742474(v=vs.85)) il programma ed eliminare la scelta.

### <a name="make-confirmations-require-thought"></a>Richieste di conferma richieste

Per una conferma per avere valore, gli utenti devono comprendere il motivo per non continuare. In alcuni casi il motivo è ovvio, ad esempio quando gli utenti chiudono un documento con modifiche che non sono state salvate:

![Screenshot che mostra un disegno che si desidera salvare le modifiche? il messaggio "Hello World!".](images/mess-confirm-image3.png)

In questo esempio, il motivo della conferma è evidente.

In altre situazioni, il motivo potrebbe non essere così ovvio.

Quando si scelgono le etichette dei pulsanti di commit per le finestre di dialogo, le [linee guida generali](win-dialog-box.md) sono scegliere le etichette che sono risposte specifiche all'istruzione principale. Questo comporta un processo decisionale efficiente perché gli utenti devono leggere una quantità minima di testo per continuare. Tuttavia, questo obiettivo di efficienza può essere controproducente per le conferme. Prendere in considerazione questo esempio:

**Non corretto:**

![cattura di schermata della conferma con il pulsante Disinstalla ](images/mess-confirm-image4.png)

In questo esempio, la risposta corretta richiede il pensiero.

Se si presenta questa conferma immediatamente dopo che l'utente ha assegnato il comando di disinstallazione, è probabile che la risposta dell'utente sia "naturalmente voglio disinstallare". L'utente fa clic su Disinstalla senza darlo una seconda considerazione.

Per le conferme, non si vuole che gli utenti stiano prendendo decisioni emotive. Per incoraggiare gli utenti a pensare alla propria risposta, è necessario fornire un piccolo aumento della velocità della decisione. Quando è pratico, è in genere preferibile eseguire questa operazione con una formulazione accurata dei pulsanti di commit. Ad esempio, è possibile usare la lingua aggiuntiva per indicare che esiste un motivo per non continuare.

**Migliore:**

![screenshot del pulsante ' Disinstalla comunque ' ](images/mess-confirm-image5.png)

In questo esempio, "Anyway" viene aggiunto all'etichetta del pulsante commit per indicare che la conferma indica che non è possibile continuare.

Se questo approccio non è pratico, è possibile usare i pulsanti Sì/no commit.

**Migliore anche:**

![cattura di schermata della conferma con i pulsanti Sì/No ](images/mess-confirm-image6.png)

In questo esempio, l'uso dei pulsanti Sì/no commit impone agli utenti di leggere almeno l'istruzione principale.

### <a name="provide-all-the-information"></a>Fornire tutte le informazioni

Se si prevede di porre una domanda, è necessario fornire informazioni sufficienti per consentire agli utenti di rispondere in modo intelligente a tale domanda. Si consideri la finestra di dialogo Conferma sostituzione file da Windows XP:

![screenshot della finestra di dialogo ' Conferma sostituzione file ' ](images/mess-confirm-image7.png)

Finestra di dialogo Conferma sostituzione file di Windows XP.

Questa conferma fornisce tutte le informazioni che potrebbero essere necessarie agli utenti per rispondere alla domanda? Prima di rispondere, considerare gli scenari utente più comuni:

-   Copiare o spostare l'altro file, sostituendo quello esistente.
-   Conserva il file esistente, senza copiare o trasferire l'altro file.
-   Conserva o copia il file più recente (scenario principale).
-   Conserva il file esistente o copia l'altro file, a seconda dei criteri, ad esempio il contenuto e le dimensioni dei file.
-   Conserva il file esistente e copia l'altro file con un nome diverso.
-   Annullare l'operazione se si è verificato un errore o un valore imprevisto.

Gli utenti possono ottenere lo scenario 1 facendo clic su Sì e sullo scenario 2 facendo clic su No. Possono ottenere lo scenario 3 confrontando le date dei file e facendo clic sul pulsante appropriato, ma si noti quanto è necessario per determinare il file più recente e quindi determinare il pulsante appropriato in particolare per quello che probabilmente sarà lo scenario più comune.

Anche gli scenari 4, 5 e 6 sono sorprendentemente difficili. Le dimensioni dei file vengono arrotondate, quindi, ad esempio, è Impossibile determinare se questi file hanno le stesse dimensioni o anche se sono lo stesso file. Le icone si riferiscono all'applicazione utilizzata per aprire il file, in modo che gli utenti debbano aprire i file per controllare e confrontare il contenuto. La presenza di anteprime del contenuto dei file sarebbe molto più utile per rispondere alla domanda.

La conferma della copia del file da Windows Vista offre un lavoro molto migliore per la gestione di questi scenari, fornendo ulteriori informazioni e aggiungendo l'opzione per la conservazione di entrambi i file:

![screenshot della finestra di dialogo ' copia file ' ](images/mess-confirm-image8.png)

Conferma del file di copia di Windows Vista.

### <a name="provide-specific-useful-information"></a>Fornire informazioni utili specifiche

Se si intende porre una domanda, assicurarsi che gli utenti capiscano la domanda e le implicazioni delle risposte alternative. Prendere in considerazione questa conferma di sicurezza di Windows Internet Explorer:

![screenshot della conferma con una domanda vaga ](images/mess-confirm-image9.png)

Una conferma di sicurezza vaga.

Questa conferma pone una domanda a cui gli utenti non possono rispondere in modo intelligente. L'utente ha richiesto la visualizzazione di una pagina da parte di Windows Internet Explorer e questo messaggio ne consiglia il testo in modo implicito tramite la formulazione del testo e evidenziando No come scelta predefinita.

Il problema di sicurezza specifico che la pagina pone non è sufficientemente illustrato, quindi il rischio di continuare non è chiaro. Quali informazioni nella conferma potrebbero far sì che l'utente non abbia mai fatto clic su No? A causa della vaghezza del messaggio, la conferma non è probabile che gli utenti continuino, ma li farà sentire male.

Affinché questa conferma risulti utile, è necessario fornire altre informazioni specifiche che potrebbero comportare la scelta di non continuare da parte dell'utente. In generale, per ogni risposta in una conferma, prendere in considerazione gli scenari che lo richiedono e assicurarsi che siano disponibili informazioni sufficienti per consentire agli utenti di sceglierlo. Fornire scelte, non dilemmi.

### <a name="how-to-determine-if-a-confirmation-is-necessary"></a>Come determinare se è necessaria una conferma

Il pensiero degli scenari e la possibilità di scegliere ogni risposta suggerisce un metodo sistematico per determinare se è necessaria una conferma. Se gli utenti hanno la possibilità di selezionare tutte le risposte, la conferma è necessaria e utile. Tuttavia, se è probabile che sia presente una sola risposta (ad indicare il 98% del tempo), la conferma è chiaramente inutile e deve essere rimossa. Si noti che le conferme correlate ai problemi di sicurezza, legali e di sicurezza sono possibili eccezioni.

![Screenshot di "modificare le impostazioni?" ](images/mess-confirm-image10.png)

Questa conferma è necessaria? Gli utenti selezionano No? È possibile ma molto improbabile. Questa conferma deve essere rimossa.

**Se si eseguono solo tre operazioni...**

1. Assicurarsi che la conferma sia effettivamente necessaria. Dovrebbe esserci un motivo legittimo e chiaro per non continuare e la possibilità che a volte gli utenti non lo siano.

2. Se il motivo della conferma non è immediatamente ovvio, scegliere i pulsanti Esegui commit che incoraggiano gli utenti a pensare alla risposta. In genere, questa operazione viene eseguita tramite la formulazione della conferma come una domanda sì o no e fornisce una risposta completamente automatica o Sì/No.

3. Prendere in considerazione tutti gli scenari e fornire le informazioni necessarie per rispondere in modo intelligente alla domanda.

## <a name="usage-patterns"></a>Modelli di utilizzo

Per le conferme sono disponibili diversi modelli di utilizzo:



|                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Conferme di routine**<br/> Verificare che l'utente voglia procedere con un'azione di routine a basso rischio. <br/>                                              | Queste conferme vengono in genere formulate "si è certi...?" e spesso hanno una casella di controllo non visualizzare più questo messaggio per ridurre al minimo la loro fastidiosa. <br/> ![screenshot della "Sposta cartella nel Cestino" ](images/mess-confirm-image11.png)<br/> ![Screenshot di ' non visualizzare più il messaggio ' ](images/mess-confirm-image12.png)<br/> Esempi di conferme di routine.<br/> **Nota:** Questo modello non è in genere necessario e deve essere evitato.<br/>                                                                                                                                                                                                                                                                                        |
| **Conferme di azione rischiosa**<br/> confermare che l'utente desidera procedere con un'azione che presenta un certo rischio e non può essere annullata facilmente. <br/>            | Poiché presentano rischi, le conferme di solito presentano un'icona di avviso. <br/> ![Screenshot che mostra un esempio di conferma della formattazione del volume.](images/mess-confirm-image13.png)<br/> ![Screenshot che mostra un esempio di conferma dell'eliminazione permanente.](images/mess-confirm-image14.png)<br/> Esempi di conferme di azioni rischiose.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Conferme di conseguenza non intenzionali**<br/> Verificare che l'utente voglia procedere con un'azione con conseguenze impreviste o impreviste. <br/> | Oltre a porre una domanda, le conferme indicano le conseguenze impreviste. poiché presentano conseguenze impreviste, le conferme di solito presentano un'icona di avviso. <br/> ![Screenshot di "Chiudi tutte le schede?" conferma ](images/mess-confirm-image15.png)<br/> ![Screenshot di "Annulla installazione?" conferma ](images/mess-confirm-image16.png)<br/> esempi di conferme di conseguenza impreviste.<br/> Tuttavia, questo modello richiede che le conseguenze siano effettivamente indesiderate. <br/> **errata**<br/> ![Screenshot di "Disattiva il logger del tasto?" conferma ](images/mess-confirm-image17.png)<br/> Le conseguenze sono riportate qui, pertanto si tratta di una conferma di routine.<br/> |
| **Precisazioni**<br/> chiarire il modo in cui l'utente desidera procedere con un'azione con conseguenze potenzialmente ambigue o impreviste. <br/>             | Le operazioni di trascinamento della selezione possono generare chiarimenti se l'effetto dell'operazione può essere interpretato erroneamente. <br/> ![Screenshot di "modifica solo questa occorrenza?"](images/mess-confirm-image18.png)<br/> ![Screenshot di "Salva sempre all'uscita?" conferma ](images/mess-confirm-image19.png)<br/> Esempi di chiarimenti.<br/> **Nota:** Questo modello deve essere evitato perché è preferibile progettare azioni senza conseguenze ambigue e presupporre il risultato più probabile. <br/>                                                                                                                                                                                                                                     |
| **Conferme di sicurezza**<br/> Verificare che l'utente voglia procedere con un'azione con conseguenze per la sicurezza. <br/>                                   | ![Screenshot di "eseguire questo software?" ](images/mess-confirm-image20.png)<br/> ![Screenshot di "Memorizza password?" Conferma ](images/mess-confirm-image21.png)<br/> Esempi di conferme di sicurezza.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Conferme per più motivi**<br/> fornire informazioni su un'azione, ma presentarla come conferma. <br/>                                       | Sebbene queste finestre di dialogo vengano presentate come conferme, il loro obiettivo reale è la formazione degli utenti o l'annuncio delle funzionalità. <br/> ![screenshot della barra degli strumenti della barra delle applicazioni ](images/mess-confirm-image22.png)<br/> Esempio di conferma di un ulteriore motivo.<br/> **Nota:** Questo modello non è consigliato perché esiste in genere un'alternativa migliore e più diretta. Ad esempio, le [animazioni](vis-animations.md) rappresentano un modo migliore per mostrare la relazione tra la ragione e l'effetto. <br/>                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Utilizzare le conferme "Salva modifiche" solo quando sono presenti modifiche significative.** Non confermare le modifiche non apportate direttamente dall'utente, ad esempio la riformattazione automatica dei documenti.

**Non corretto:**

![Screenshot che mostra un Microsoft Office Outlook ' salvare le modifiche?' dell'applicazione di condivisione.](images/mess-confirm-image23.png)

Questo esempio non è corretto se usato per un messaggio di posta elettronica o un documento vuoto che non è stato modificato dall'utente.

### <a name="icons"></a>Icone

-   Le conferme non usano le icone della barra del titolo.
-   **L'icona dell'area di contenuto per una conferma si basa sul modello di progettazione:**



    | Modello                                                | Icona                                                                                                                                             |
    |--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
    | Conferme di routine <br/>                | Nessuna icona. <br/>                                                                                                                         |
    | Conferme di azione rischiosa <br/>           | Icona di avviso. <br/>                                                                                                                    |
    | Conferme di conseguenza non intenzionali <br/> | Utilizzare un'icona di avviso in caso di rischio, l'icona della funzionalità, se disponibile. in caso contrario, nessuna icona. <br/>                                          |
    | Precisazioni <br/>                       | Se la conferma prevede un documento, utilizzare l'anteprima del documento; in caso contrario, usare l'icona della funzionalità, se disponibile, o nessuna icona. <br/> |
    | Conferme di sicurezza <br/>               | Icona di avviso. <br/>                                                                                                                    |
    | Conferme per più motivi <br/>        | Nessuna icona. <br/>                                                                                                                         |



 

-   **Non usare icone di avviso per domande di routine.** Questa operazione viene eseguita in modo da contrastare il tono incoraggiante [di Windows](text-style-tone.md) e rende l'utilizzo del programma un'attività pericolosa. Si supponga che gli utenti capiscano le conseguenze dell'annullamento di un'attività prima del completamento.

**Non corretto:**

![Screenshot di "terminare l'esercitazione?" ](images/mess-confirm-image24.png)

In questo esempio viene usata un'icona di avviso per porre una domanda di routine.

### <a name="commit-buttons"></a>Pulsanti di commit

-   **Usare risposte specifiche all'istruzione principale se il motivo della conferma è ovvio o può essere reso autonomo.**

![Screenshot di "salvare le modifiche?" ](images/mess-confirm-image25.png)

In questo esempio, il motivo della conferma è ovvio, quindi salvare e non salvare il lavoro.

-   **In caso contrario, usare i pulsanti Sì e No per le risposte di conferma.** In questo modo gli utenti possono dare la conferma prima di rispondere. Non usare mai OK e Annulla per le conferme.

**Corretto:**

![Screenshot di "desidera disinstallare i file di supporto?" ](images/mess-confirm-image26.png)

In questo esempio, l'uso dei pulsanti Sì/no commit impone agli utenti di leggere almeno l'istruzione principale.

**Non corretto:**

![Screenshot di "Annulla prenotazione?" ](images/mess-confirm-image27.png)

In questo esempio, l'uso di OK/Annulla è confuso.

-   **Per chiudere un programma o riavviare Windows, usare risposte specifiche all'istruzione principale.** Per evitare fraintendimenti, non usare Close o yes/no a questo scopo.

**Corretto:**

![cattura di schermata del pulsante Riavvia Windows ora](images/mess-confirm-image28.png)

**Non corretto:**

![cattura di schermata del pulsante Sì](images/mess-confirm-image29.png)

Nell'esempio errato, sì viene usato per riavviare Windows.

### <a name="command-links"></a>Collegamenti ai comandi

-   **Per il modello chiarifications, prendere in considerazione l'uso dei collegamenti ai comandi per cancellare le alternative.**

**Accettabile:**

![Screenshot di ' modificare una o tutte le occorrenze?' ](images/mess-confirm-image30.png)

**Migliore:**

![screenshot della stessa domanda con i collegamenti ai comandi ](images/mess-confirm-image31.png)

Nell'esempio migliore, i collegamenti ai comandi rendono evidenti le alternative.

-   **Presentare prima i collegamenti ai comandi usati più di frequente.** L'ordine risultante dovrebbe approssimativamente rispettare la probabilità di utilizzo, ma anche un flusso logico.
-   Se un collegamento al comando richiede un'ulteriore spiegazione, **fornire una spiegazione aggiuntiva.** Le spiegazioni aggiuntive descrivono perché gli utenti possono scegliere l'opzione o cosa accade se si sceglie l'opzione.

Per altre linee guida ed esempi, vedere [collegamenti ai comandi](ctrl-command-links.md).

### <a name="default-values"></a>Valori predefiniti

-   **La risposta predefinita per una conferma si basa sul modello di progettazione:**



    | Modello                                                 | Risposta predefinita                                                                                |
    |--------------------------------------------------|---------------------------------------------------------------------------------|
    | Conferme di routine <br/>                | Procedere. <br/>                                                            |
    | Conferme di azione rischiosa <br/>           | Non procedere (o la scelta sicura). <br/>                                 |
    | Conferme di conseguenza non intenzionali <br/> | Se le conseguenze sono significative, non procedere; in caso contrario, continuare. <br/> |
    | Precisazioni <br/>                       | Risposta più probabile. <br/>                                           |
    | Conferme di sicurezza <br/>               | Non continuare. <br/>                                                      |
    | Conferme per più motivi <br/>        | Procedere. <br/>                                                            |



 

### <a name="dont-show-this-message-again"></a>Non visualizzare più questo messaggio

-   **Usare questa opzione solo per la routine e per altri motivi di conferma.** Per gli altri modelli, se le informazioni sono necessarie, deve sempre essere visualizzato.
-   **Non specificare questa opzione per giustificare la visualizzazione di una conferma non necessaria.** È sufficiente eliminare la conferma.

**Non corretto:**

![Screenshot di ' ignora questi promemoria?' ](images/mess-confirm-image32.png)

**Ancora errato:**

![Screenshot di ' non visualizzare più il messaggio '](images/mess-confirm-image33.png)

In questi esempi, l'aggiunta di un'opzione non visualizzare più questo messaggio non corregge una conferma non necessaria.

Per altre linee guida, vedere [finestre di dialogo](win-dialog-box.md).

### <a name="bulk-operations"></a>Operazioni bulk

-   Per le conferme che si applicano alle operazioni bulk, fornire un'opzione per applicare la conferma all'intera operazione.

![Screenshot di ' eseguire questa operazione per tutti gli elementi?' Casella di controllo ](images/mess-confirm-image34.png)

Questo esempio include un'opzione per le operazioni bulk.

-   Eliminare o posticipare le conferme in un'operazione bulk.

**Non corretto:**

![screenshot della finestra di dialogo ' conferma eliminazione file ' ](images/mess-confirm-image35.png)

In questo esempio Esplora risorse di Windows XP conferma ogni file di sola lettura durante lo spostamento di file in blocco. È preferibile copiare solo i file di sola lettura senza chiedere o posticipare la gestione di questi file e presentare la conferma alla fine dell'attività.

### <a name="progressive-disclosure&quot;></a>Rivelazione progressiva

-   **Se è necessario includere informazioni avanzate in un messaggio di conferma, rivelarlo utilizzando i pulsanti di divulgazione progressiva (ad esempio, &quot;Mostra dettagli").** Questa operazione semplifica la conferma dell'utilizzo tipico. Non nascondere le informazioni necessarie perché gli utenti potrebbero non trovarlo.
-   **Non usare "Show Details", a meno che non vi siano effettivamente più dettagli.** Non solo riformulare le informazioni esistenti in un formato diverso.

Per le linee guida sulle etichette, vedere [divulgazione progressiva](ctrl-progressive-disclosure-controls.md).

### <a name="user-account-control"></a>Controllo dell'account utente

-   **Non usare l'interfaccia utente di elevazione del controllo dell'account utente (UAC) come sostituto di una conferma.** Se per un'azione è necessaria una conferma, utilizzare una finestra di dialogo separata. Durante l' [interfaccia utente di elevazione](winenv-uac.md)dei privilegi, gli utenti devono concentrarsi sull'attività avviata e se il programma è attendibile.
-   **Visualizza la conferma prima dell'interfaccia utente di elevazione.** In questo modo si eliminano le elevazioni superflue.

## <a name="text"></a>Testo

### <a name="general"></a>Generale

-   **Rimuovere il testo ridondante.** Cercare il testo ridondante nei titoli, le istruzioni principali, le istruzioni aggiuntive, le aree di contenuto, i collegamenti ai comandi e i pulsanti di commit. In genere, lasciare il testo completo nelle istruzioni e nei controlli interattivi e rimuovere qualsiasi ridondanza dalle altre posizioni.
-   **Non usare "Warning" o "Warning" nel testo.** Se gli utenti devono procedere con cautela, indicare invece l'utilizzo di un'icona di avviso.

**Non corretto:**

![screenshot della conferma della formattazione del volume ](images/mess-confirm-image36.png)

In questo esempio, il termine "avviso" non è necessario.

### <a name="titles"></a>Titoli

-   **Usare il titolo per identificare il comando o la funzionalità da cui proviene la conferma. Eccezioni**
    -   Se una conferma viene visualizzata da molti comandi diversi, provare a usare invece il nome del programma.
    -   Se il titolo è ridondante o confuso con l'istruzione principale, usare invece il nome del programma.

Tuttavia, se la conferma viene eseguita da un'attività a esecuzione prolungata e può essere visualizzata correttamente dopo l'avvio dell'attività, utilizzare sempre il comando o la funzionalità per identificare chiaramente il contesto.

-   **Non usare il titolo per spiegare cosa fare nella finestra di dialogo** che è lo scopo dell'istruzione principale.
-   Se aggiunge chiarezza, avviare il titolo con la parola Confirm.
-   **Per le conferme di azione rischiosa, è possibile aggiungere il nome dell'oggetto necessario per l'enfasi aggiuntiva.**

![screenshot del titolo della finestra di dialogo ' formatta unità f ' ](images/mess-confirm-image13.png)

In questo esempio, l'unità da formattare viene inclusa nel titolo.

-   Usare l'uso [di maiuscole in stile titolo](glossary.md)senza la punteggiatura finale.

### <a name="main-instructions"></a>Istruzioni principali

-   **L'istruzione principale per una conferma si basa sul modello di progettazione:**



    | Modello                                                 | Istruzione principale                                                                                                                                                                                                                                                                                                                                                                                                          |
    |--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Conferme di conseguenza non intenzionali <br/> | dichiarare la conseguenza imprevista.<br/> **eccezione:** se una domanda che chiede se l'utente vuole continuare chiaramente implica la conseguenza imprevista, porre la domanda. <br/> ![Screenshot di "Chiudi tutte le schede?" conferma ](images/mess-confirm-image15.png)<br/> In questo esempio, chiedere all'utente di continuare a fornire le conseguenze dell'azione.<br/> |
    | Tutti gli altri <br/>                           | Porre una singola domanda per determinare se l'utente vuole continuare. <br/>                                                                                                                                                                                                                                                                                                                              |



 

-   **Usare concise solo una singola frase completa.** Rimuovere l'istruzione principale fino alle informazioni essenziali. Se è necessario spiegare altro, utilizzare un'istruzione supplementare.
-   **Essere specifici se sono presenti oggetti interessati, assegnare i nomi completi.**
-   **Usare la formulazione positiva.** La formulazione positiva è più semplice da comprendere per gli utenti.

**Corretto:**

Abilitare la condivisione di file e stampanti?

**Non corretto:**

Disabilitare la condivisione di file e stampanti?

Tuttavia, la formulazione deve corrispondere al comando associato, anche se il comando è con frase negativa. quindi, ad esempio, usare Disable per confermare un comando Disable.

-   Sebbene non esistano regole rigide per la formulazione, **queste frasi di conferma comuni hanno la connotazione indicata:**



    | Frase                                                            | Connotazione                                                            |
    |-------------------------------------------------------------|-------------------------------------------------------------|
    | \[Eseguire un'azione \] ? <br/> | Conferma del risultato diretto di una richiesta dell'utente. <br/> |
    | Si desidera \[ eseguire un'azione \] ? <br/>           | Conferma di un effetto collaterale di una richiesta dell'utente. <br/>     |
    | \[Selezionare un risultato \] ? <br/>          | È necessario un chiarimento. <br/>                           |
    | \[Eseguire un'azione \] ? <br/>                          | Nessuna connotazione. <br/>                                 |



 

-   Per le conferme di azione rischiosa, usare il termine in modo permanente per indicare che un'azione non può essere annullata.

![cattura di schermata della conferma dell'eliminazione permanente ](images/mess-confirm-image37.png)

In questo esempio "permanentemente" indica che l'azione non può essere annullata.

-   Usare l'uso [di maiuscole in stile frase](glossary.md).

### <a name="supplemental-instructions"></a>Istruzioni supplementari

-   **L'istruzione supplementare per una conferma si basa sul modello di progettazione:**

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><strong>Modello</strong><br/></td>
    <td><strong>Istruzione supplementare</strong><br/></td>
    </tr>
    <tr class="even">
    <td>Conferme di conseguenza non intenzionali <br/></td>
    <td>Porre una singola domanda per determinare se l'utente vuole continuare. <br/></td>
    </tr>
    <tr class="odd">
    <td>Tutti gli altri <br/></td>
    <td>Spiega tutti i motivi non evidenti per cui l'utente potrebbe non voler procedere. Questi motivi includono: <br/>
    <ul>
    <li>Potenziale perdita di uno o più degli elementi seguenti: <ul>
    <li>Una risorsa preziosa, ad esempio la perdita di dati o la perdita finanziaria.</li>
    <li>Accesso al sistema o integrità.</li>
    <li>Privacy o controllo sulle informazioni riservate.</li>
    </ul></li>
    <li>Azioni irreversibili.</li>
    </ul></td>
    </tr>
    </tbody>
    </table>

    

     

-   **Non ripetere l'istruzione principale con una formulazione leggermente diversa.** Omettere invece l'istruzione supplementare se non è più necessario aggiungere.
-   **Per le conferme di conseguenza impreviste, provare a usare il termine per indicare in modo conciso che esiste un motivo per non continuare** se l'utente ha trascurato l'istruzione principale. Per ulteriori informazioni, vedere Concetti di progettazione.
-   Usare frasi complete, maiuscole e minuscole in stile frase e punteggiatura finale.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento a conferme:

-   Se il titolo è specifico per la conferma, ovvero non il nome del programma, fare riferimento a una conferma in base al titolo. in caso contrario, fare riferimento alla relativa istruzione principale.
-   Se necessario, è possibile fare riferimento a una finestra di dialogo di conferma come messaggio.
-   Usare il testo esatto, inclusa la relativa maiuscola.
-   Quando possibile, formattare il testo usando grassetto. In caso contrario, inserire il testo tra virgolette solo se necessario per evitare confusione.

Esempio: nel messaggio **copia file** fare clic sul file più recente.

