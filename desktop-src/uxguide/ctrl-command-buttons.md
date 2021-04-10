---
title: Pulsanti di comando
description: Con un pulsante di comando, gli utenti avviano un'azione immediata.
ms.assetid: 0e2ff31a-657b-4e4c-afee-2a6bd742f46c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 32c8c16cef275e1fefe44e579105515d3e61c497
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761296"
---
# <a name="command-buttons"></a>Pulsanti di comando

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con un pulsante di comando, gli utenti avviano un'azione immediata.

![screenshot del pulsante di comando OK ](images/ctrl-command-buttons-image1.png)

Un pulsante di comando tipico.

Il pulsante di comando predefinito viene richiamato quando gli utenti preme il tasto INVIO. Viene assegnato dallo sviluppatore, ma qualsiasi pulsante di comando diventa il valore predefinito quando viene selezionata la scheda utenti.

> [!Note]  
> Le linee guida correlate al [layout](vis-layout.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Il pulsante di comando utilizzato per avviare un'azione immediata?** Se non è così, usa un altro controllo.
-   **Un collegamento è la scelta migliore?** Usare un collegamento se:
    -   L'azione consiste nel passare a un'altra pagina, a una finestra o a un argomento della guida. **Eccezione**: lo spostamento della procedura guidata usa i pulsanti di comando indietro e avanti.
    -   Il comando è incorporato in un corpo di testo.
    -   Il comando è di natura secondaria. Ciò significa che non è correlato allo scopo principale della finestra. In questo caso, è opportuno utilizzare un pulsante di comando o un collegamento leggero.
    -   Il comando fa parte di un menu o di un gruppo di collegamenti correlati.
    -   Il valore dell'etichetta è lungo, composto da cinque o più parole, in modo da assegnare un aspetto imbarazzato a un pulsante di comando.
-   **Una combinazione di pulsanti di opzione e pulsanti di comando generici è la scelta migliore?** Spesso i pulsanti di opzione vengono usati insieme ai pulsanti di comando generici (OK, Annulla) al posto di un set di pulsanti di comando specifici quando si verifica una delle condizioni seguenti:
    -   Sono disponibili cinque o più azioni possibili.
    -   Gli utenti devono visualizzare informazioni aggiuntive prima di prendere una decisione.
    -   Gli utenti devono interagire con le scelte, ad esempio per visualizzare informazioni aggiuntive, prima di prendere una decisione.
    -   Gli utenti visualizzano le scelte come opzioni anziché comandi diversi.

        **Corretto:** ![ screenshot della finestra di dialogo, pulsanti di opzione e testo ](images/ctrl-command-buttons-image2.png)

        In questo esempio, i pulsanti di opzione sono combinati con i pulsanti OK e Annulla per fornire informazioni aggiuntive sulle opzioni.

        Non **corretto:** ![ screenshot del messaggio con i pulsanti di comando](images/ctrl-command-buttons-image3.png)

        In questo esempio, i pulsanti di comando da soli rendono difficile per gli utenti prendere una decisione informata.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

**Uso di ellissi**

Mentre i pulsanti di comando vengono utilizzati per le azioni immediate, per eseguire l'azione potrebbero essere necessarie ulteriori informazioni. **Indicare un comando che richiede informazioni aggiuntive (inclusa la conferma) aggiungendo i puntini di sospensione alla fine dell'etichetta del pulsante**.

![cattura di schermata del pulsante di comando stampa con ellissi ](images/ctrl-command-buttons-image4.png)

In questo esempio, Print... consente di visualizzare una finestra di dialogo Stampa per raccogliere ulteriori informazioni.

![screenshot del pulsante di comando stampa, nessun ellisse ](images/ctrl-command-buttons-image5.png)

Al contrario, in questo esempio il comando Print stampa una singola copia di un documento sulla stampante predefinita senza ulteriori interazioni da parte dell'utente.

L' **uso corretto dei puntini di sospensione è importante per indicare che gli utenti possono effettuare altre scelte prima di eseguire l'azione o persino annullare completamente l'azione**. Il segnale visivo offerto dai puntini di sospensione consente agli utenti di esplorare il software senza timore.

**Questo non significa che è necessario usare i puntini di sospensione ogni volta che un'azione Visualizza un'altra finestra** solo quando sono necessarie altre informazioni per eseguire l'azione. Di conseguenza, **qualsiasi pulsante di comando il cui verbo implicito deve essere "Mostra un'altra finestra" non accetta i puntini** di sospensione, ad esempio con i comandi about, Advanced, Help (o qualsiasi altro comando collegato a un argomento della guida), opzioni, proprietà o impostazioni.

In genere, i puntini di sospensione vengono usati nelle interfacce utente per indicare l'incompletezza. I comandi che mostrano altre finestre non sono incompleti devono visualizzare un'altra finestra e altre informazioni non sono necessarie per eseguire l'azione. Questo approccio elimina il disordine dello schermo nelle situazioni in cui le ellissi hanno un valore minimo.

**Nota:** Per determinare se un pulsante di comando necessita di puntini di sospensione, non usare la necessità di [elevare i privilegi](winenv-uac.md) come fattore. L'elevazione non è necessaria per eseguire un comando (piuttosto, è per l'autorizzazione) e la necessità di elevare è indicata con lo scudo di sicurezza.

**Se si esegue una sola operazione...** Utilizzare un'etichetta concisa, specifica e intuitiva che descrive chiaramente l'azione eseguita dal pulsante di comando e utilizza i puntini di sospensione quando appropriato.

## <a name="usage-patterns"></a>Modelli di utilizzo

I pulsanti di comando hanno diversi modelli di utilizzo:



|                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pulsanti di comando standard** È possibile usare i pulsanti di comando standard per avviare un'azione immediata.<br/>                                                           | ![screenshot del pulsante di comando standard (grigio) ](images/ctrl-command-buttons-image6.png)<br/> Un pulsante di comando standard.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Pulsanti di comando predefiniti** Il pulsante di comando predefinito in una finestra indica il pulsante di comando che verrà attivato quando gli utenti preme il tasto INVIO.<br/>       | ![screenshot del pulsante di comando predefinito (blu) ](images/ctrl-command-buttons-image7.png)<br/> Pulsante di comando predefinito.<br/> Qualsiasi pulsante di comando diventa il valore predefinito quando viene selezionata la scheda utenti. Se lo stato attivo per l'input si trova su un controllo che non è un pulsante di comando, il pulsante di comando con l'attributo del pulsante predefinito diventa il valore predefinito. Per impostazione predefinita, è possibile avere un solo pulsante di comando in una finestra.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Pulsanti di comando semplici** Un pulsante di comando Lightweight è simile a un pulsante di comando standard, ad eccezione del fatto che il relativo frame Button viene visualizzato solo al passaggio del mouse. <br/> | ![Screenshot di uno dei due pulsanti di stampa selezionati ](images/ctrl-command-buttons-image8.png)<br/> In questo esempio, il comando ha un aspetto molto leggero, simile a un [collegamento](ctrl-links.md), fino a quando l'utente passa il mouse sul comando, a quel punto viene disegnato con un frame di pulsanti.<br/> È possibile utilizzare i pulsanti di comando Lightweight in situazioni in cui si utilizza un pulsante di comando standard, ma si desidera evitare di visualizzare sempre il frame del pulsante. I pulsanti di comando Lightweight sono ideali per i comandi che si desidera sottoporre a sottolineatura e l'utilizzo di un collegamento non sarebbe appropriato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Pulsanti di menu** Utilizzare un pulsante di menu quando è necessario un menu per un piccolo set di comandi correlati.<br/>                                                                 | ![screenshot del pulsante di menu formato e dei relativi comandi ](images/ctrl-command-buttons-image9.png)<br/> Pulsante di menu con un piccolo set di comandi correlati.<br/> Utilizzare un pulsante di menu quando una barra dei menu non è desiderata, ad esempio in una finestra di dialogo, in una barra degli strumenti o in un'altra finestra che non dispone di una barra dei menu. Un singolo triangolo verso il basso indica che facendo clic sul pulsante viene visualizzato un menu a discesa.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Pulsanti di divisione** Usare un pulsante di suddivisione per consolidare un set di varianti di un comando, soprattutto quando uno dei comandi viene usato nella maggior parte dei casi.<br/>          | ![cattura di schermata del pulsante Apri split senza comandi ](images/ctrl-command-buttons-image10.png)<br/> pulsante di suddivisione compresso.<br/> Analogamente a un pulsante di menu, un singolo triangolo verso il basso indica che facendo clic sulla parte più a destra del pulsante viene visualizzato il menu a discesa.<br/> ![cattura di schermata del pulsante Apri split con i comandi ](images/ctrl-command-buttons-image11.png)<br/> pulsante di suddivisione a discesa.<br/> in questo esempio viene usato un pulsante combinato per consolidare sei varianti del comando Apri. il normale comando di apertura viene usato nella maggior parte dei casi, quindi gli utenti in genere non devono visualizzare gli altri comandi. l'utilizzo di un pulsante di selezione consente di risparmiare una notevole quantità di spazio sullo schermo, offrendo al tempo stesso opzioni avanzate.<br/> a differenza di un pulsante di menu, facendo clic sulla parte sinistra del pulsante viene eseguita direttamente l'azione sull'etichetta. i pulsanti di suddivisione sono efficaci nelle situazioni in cui l'azione successiva con uno strumento specifico è probabilmente uguale all'ultima azione. in questo caso, l'etichetta viene modificata nell'ultima azione, come con una selezione colori:<br/> ![cattura di schermata del pulsante Dividi riempimento senza comandi ](images/ctrl-command-buttons-image12.png)<br/> In questo esempio, l'etichetta viene modificata nell'ultima azione.<br/> |
| **Pulsanti Sfoglia** Utilizzare un pulsante Sfoglia per visualizzare una finestra di dialogo che consente agli utenti di selezionare un valore valido.<br/>                                                           | le finestre di dialogo avviate da un pulsante Sfoglia consentono agli utenti di selezionare file, cartelle, computer, utenti, colori e così via. vengono in genere combinati con un controllo non vincolato, ad esempio una casella di testo. vengono in genere contrassegnati come browse, other o more e presentano sempre i puntini di sospensione per indicare che sono necessarie altre informazioni. <br/> ![screenshot della casella di testo con il pulsante Sfoglia ](images/ctrl-command-buttons-image13.png)<br/> casella di testo con un pulsante Sfoglia.<br/> per Windows con molti pulsanti Sfoglia, è possibile usare una versione breve:<br/> ![cattura di schermata del pulsante Sfoglia breve con ellissi ](images/ctrl-command-buttons-image14.png)<br/> Pulsante di ricerca breve.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Pulsanti di divulgazione progressiva** Usare un pulsante di divulgazione progressiva per mostrare o nascondere le opzioni usate raramente.<br/>                                            | nascondere le opzioni usate raramente finché non sono necessarie viene chiamato divulgazione progressiva. le virgolette doppie vengono usate per indicare la divulgazione progressiva e indicano la direzione in cui verrà eseguita la divulgazione o l'occultamento: <br/> ![screenshot del pulsante con ' more ' e frecce a destra ](images/ctrl-command-buttons-image15.png)<br/> Dopo aver fatto clic sul pulsante, l'etichetta cambia per indicare che il clic successivo avrà l'effetto opposto:<br/> ![cattura di schermata del pulsante con ' less ' e frecce sinistre ](images/ctrl-command-buttons-image16.png)<br/> Per ulteriori informazioni ed esempi, vedere [controlli di divulgazione progressivi](ctrl-progressive-disclosure-controls.md). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Pulsanti direzionali** Utilizzare un pulsante direzionale per indicare la direzione in cui verrà eseguita un'azione.<br/>                                               | in questo caso viene usata una parentesi uncinata singola anziché una doppia freccia di espansione: <br/> ![screenshot dei pulsanti freccia a destra e a sinistra ](images/ctrl-command-buttons-image17.png)<br/> Un pulsante direzionale indica la direzione di azione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Visualizza un puntatore occupato se il risultato della selezione di un pulsante di comando non è istantaneo.** Senza commenti, gli utenti potrebbero presupporre che il clic non sia stato fatto, quindi fare clic di nuovo su.
-   Se lo stesso pulsante di comando viene visualizzato in più di una finestra, **provare a usare lo stesso testo dell'etichetta e la stessa chiave di accesso e individuarlo approssimativamente nella stessa posizione in ogni finestra quando è pratica.**
-   **Per i pulsanti di comando con etichette di testo, usare la larghezza minima del pulsante e l'altezza del pulsante di comando standard.** Per altre informazioni, vedere [ridimensionamento e spaziatura consigliati](#recommended-sizing-and-spacing).
-   Per ogni finestra, **i pulsanti di comando hanno la stessa larghezza**. Se non è pratico, limitare il numero di larghezze diverse per i pulsanti di comando con etichette di testo a due.
-   Quando un altro controllo interagisce con un pulsante di comando, ad esempio una casella di testo con un pulsante Sfoglia, **indica la relazione posizionando il pulsante di comando in una delle tre posizioni seguenti:**
    -   A destra di e allineato in alto con l'altro controllo.
    -   Sotto e allineato a sinistra con l'altro controllo.
    -   Centrato verticalmente tra i controlli che interagiscono (ad esempio aggiungere e rimuovere i pulsanti tra due caselle di riepilogo interoperative).
-   Se più pulsanti di comando interagiscono con lo stesso controllo, **li impila verticalmente a destra di e allineato in alto con l'altro controllo oppure posizionarli orizzontalmente allineati a sinistra sotto il controllo.**
-   Quando i pulsanti di comando sono subordinati ad altri controlli, **usare la posizione precedente e disabilitare il pulsante di comando subordinato fino a quando non viene selezionato il controllo superiore.**
-   **Non usare pulsanti di comando narrow, short o Tall con etichette di testo** perché tendono a sembrare non professionali. Provare a usare le larghezze e le altezze predefinite.

**Corretto:** ![ screenshot del pulsante OK dimensioni predefinite ](images/ctrl-command-buttons-image18.png)

In questo esempio, le dimensioni del pulsante sono standard e sembrano professionali.

Non **corretto:** ![ cattura di schermata del pulsante OK breve](images/ctrl-command-buttons-image19.png)

In questo esempio il pulsante è troppo piccolo.

Non **corretto:** ![ screenshot del pulsante OK quadrato grande](images/ctrl-command-buttons-image20.png)

In questo esempio il pulsante presenta una quantità eccessiva di spazio intorno all'etichetta.

-   **Evitare di combinare etichette di testo e grafici sui pulsanti di comando.** La combinazione di testo e grafica in genere aggiunge confusione visiva superflua e non migliora la comprensione dell'utente. Si consiglia di combinare testo e grafica solo quando l'elemento grafico facilita la comprensione, ad esempio quando si tratta di un simbolo standard per il comando o consente agli utenti di visualizzare i risultati del comando. In caso contrario, preferire il testo, ma usare testo o grafica.

**Corretto:** ![ screenshot del comando ruota con freccia curva ](images/ctrl-command-buttons-image21.png)

In questo esempio, l'icona a forma di freccia consente agli utenti di visualizzare i risultati del comando.

**Corretto:** ![ screenshot della barra degli indirizzi con icone e testo ](images/ctrl-command-buttons-image22.png)

In questo esempio i simboli standard vengono combinati con testo per facilitare la comprensione

Non **corretto:** ![ screenshot del pulsante con icona x e Annulla](images/ctrl-command-buttons-image23.png)

In questo esempio, il grafico Annulla non aggiunge nulla al testo.

-   **Non usare i pulsanti di comando per impostare lo stato**. Usare invece i pulsanti di opzione o le caselle di controllo. I pulsanti di comando sono solo per l'avvio di azioni.

### <a name="split-buttons"></a>Pulsanti di divisione

-   **Rendere il comando più probabile il comportamento predefinito**. Se è presente più di un comando probabile, sceglierne uno che non richiede informazioni aggiuntive.
-   **Se il comando più probabile è la selezione dell'ultimo utente, modificare l'etichetta del pulsante sull'ultima selezione.**
-   **Visualizzare il comando predefinito utilizzando il testo in grassetto nel menu**. In questo modo è più semplice per gli utenti trovare il comando predefinito, soprattutto quando il comando predefinito è dinamico o il pulsante di divisione utilizza un elemento grafico anziché un'etichetta di testo.

### <a name="default-values"></a>Valori predefiniti

-   Includere un pulsante di comando predefinito in ogni finestra di dialogo. **Selezionare il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e il comando più sicuro è il valore predefinito**. Se la sicurezza e la sicurezza non sono fattori, selezionare il comando più probabile o pratico.
-   **Non eseguire un'azione distruttiva sul pulsante di comando predefinito** a meno che non esista un modo semplice per annullare il comando.

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![diagramma delle dimensioni dei pulsanti in pixel e dlu ](images/ctrl-command-buttons-image24.png)

Ridimensionamento e spaziatura consigliati per i pulsanti di comando.

## <a name="labels"></a>Etichette

-   Etichettare ogni pulsante di comando.
-   Se il pulsante ha solo un'etichetta grafica, assegnare la proprietà Name a un'etichetta di testo appropriata. Questo consente ai prodotti di Assistive Technology, ad esempio utilità per la lettura dello schermo, di fornire agli utenti informazioni alternative sul grafico.

    ![screenshot dei pulsanti su, giù e copia ](images/ctrl-command-buttons-image25.png)

    Questo esempio mostra i pulsanti grafici; internamente, questi pulsanti sono contrassegnati come precedente, successivo e copia.

-   Per i pulsanti di esplorazione brevi (con etichetta "..."), l'etichetta interna dovrebbe essere browse.
-   Assegnare una [chiave di accesso](glossary.md)univoca. Per le linee guida, vedere [tastiera](inter-keyboard.md).

    **Eccezioni**

    -   Non assegnare chiavi di accesso ai pulsanti OK e Annulla, perché immettere è la chiave di accesso per il pulsante predefinito (che corrisponde in genere al pulsante OK) ed ESC è il tasto di accesso per l'annullamento. In questo modo le altre chiavi di accesso risultano più semplici da assegnare.
    -   Non assegnare chiavi di accesso ai pulsanti di ricerca brevi (con etichetta "...") perché non possono essere assegnati in modo univoco.

-   Preferisci etichette specifiche rispetto a quelle generiche. Idealmente, gli utenti non devono leggere nient'altro per comprendere l'etichetta. È molto più probabile che gli utenti leggano le etichette dei pulsanti di comando rispetto al testo statico.

    -   **Eccezione:** Non rinominare il pulsante Annulla se il significato dell'annullamento non è ambiguo. Gli utenti non devono leggere tutti i pulsanti per determinare il pulsante che annulla un'azione. Tuttavia, rinominare Annulla se non è chiaro quale azione verrà annullata, ad esempio quando sono presenti diverse azioni in sospeso.

    **Accettabile:**

    ![Screenshot che mostra i pulsanti "OK" e "Annulla".](images/ctrl-command-buttons-image26.png)

    In questo esempio OK e Annulla sono etichette accettabili ma non specifiche.

    **Migliore:**

    ![screenshot dei pulsanti Masterizza CD e Annulla ](images/ctrl-command-buttons-image27.png)

    In questo esempio, Burn CD è più specifico di OK.

    **Non corretto:**

    ![screenshot dei pulsanti Masterizza CD e non Masterizza CD ](images/ctrl-command-buttons-image28.png)

    In questo esempio, è consigliabile usare Annulla anziché masterizzare CD.

-   Avviare le etichette con un verbo imperativo e descrivere chiaramente l'azione eseguita dal pulsante. Non usare punteggiatura finale.
    -   **Eccezione:** Le etichette standard seguenti sono accettabili senza verbi: avanzate, indietro, dettagli, avanti, minore, più, nuovo, successivo, no, OK, opzioni, precedente, proprietà, impostazioni e sì.
-   Mentre le etichette brevi sono preferite, usare un testo sufficiente per spiegare il comando in modo sufficientemente appropriato. Usare un oggetto diretto (un sostantivo dopo il verbo) quando l'oggetto non è evidente dal contesto. Idealmente, gli utenti non devono leggere nient'altro per comprendere l'etichetta.

    **Accettabile:**

    ![screenshot del pulsante con Aggiungi etichetta ](images/ctrl-command-buttons-image29.png)

    In questo esempio, un'etichetta breve è accettabile se il relativo significato nel contesto è immediatamente evidente.

    **Migliore:** (se l'aggiunta non è chiara)

    ![screenshot del pulsante con l'etichetta Aggiungi elementi ](images/ctrl-command-buttons-image30.png)

    In questo esempio, l'aggiunta di un sostantivo al verbo aiuta la comprensione degli utenti.

    **Migliore:** (se l'aggiunta o l'aggiunta di elementi non è chiara)

    ![screenshot del pulsante con Aggiungi elementi selezionati ](images/ctrl-command-buttons-image31.png)

    In questo esempio, l'etichetta è di chiara interpretazione.

-   Usare l'uso [di maiuscole in stile frase](glossary.md). Questa operazione è più appropriata per il tono Windows [tono](text-style-tone.md)[Windows](https://msdn.microsoft.com/library/windows/desktop/aa974175.aspx) e l'uso di brevi frasi per i pulsanti di comando.
    -   **Eccezione:** Per le applicazioni legacy, è possibile usare l'uso di [maiuscole in stile titolo](glossary.md) , se necessario, per evitare di combinare stili di maiuscole.
-   Non usare ora nelle etichette dei pulsanti di comando perché l'immediatezza del comando può essere eseguita per la concessione.

    -   **Eccezione:** Quando necessario, utilizzare ora per distinguere i comandi che avviano un'attività da comandi che eseguono immediatamente un'attività.

    ![screenshot del pulsante con etichetta di download ](images/ctrl-command-buttons-image32.png)

    In questo esempio, facendo clic sul pulsante di comando si passa a una finestra o a una pagina che consente agli utenti di eseguire il download.

    ![screenshot del pulsante con l'etichetta Scarica ora ](images/ctrl-command-buttons-image33.png)

    In questo esempio, facendo clic sul pulsante di comando viene eseguito il download.

    A questo punto è necessario etichettare un solo comando in un flusso attività. Un comando **Scarica ora** , ad esempio, non deve mai essere seguito da un altro comando **Scarica ora** .

-   Non usare successivamente nelle etichette del pulsante di comando se implica un'azione che non si verificherà. Ad esempio, non usare install in un secondo momento (a differenza di Install Now), a meno che il comando non venga installato in un secondo momento. In alternativa, usare non installare o annullare.

    **Non corretto:**

    ![screenshot del riavvio ora e riavvio successivo ](images/ctrl-command-buttons-image34.png)

    In questo esempio, il riavvio in un secondo momento comporta che il comando venga riavviato automaticamente in un secondo momento.

-   Usare un pulsante avanzate solo per le opzioni rilevanti per gli utenti avanzati o per richiedere una conoscenza avanzata degli utenti. Non usare un pulsante avanzato per le funzionalità considerate avanzate tecnologicamente. Ad esempio, la funzionalità di graffatura di una stampante non è un'opzione avanzata, ma il suo sistema di gestione dei colori è.

    **Errato:** (se le opzioni non sono effettivamente avanzate)

    ![screenshot del pulsante con etichetta avanzata ](images/ctrl-command-buttons-image35.png)

    In questo esempio, Advanced è fuorviante.

    **Corretto:**

    ![screenshot del pulsante con altre etichette di opzioni ](images/ctrl-command-buttons-image36.png)

    In questo esempio, l'etichetta è più specifica e precisa.

-   Per i pulsanti di comando che aprono altre finestre, scegliere un'etichetta che usi parte o tutto il testo della barra del titolo della finestra secondaria. Ad esempio, un pulsante di comando con etichetta Sfoglia potrebbe aprire una finestra di dialogo con il titolo Sfoglia per cartella. L'uso della stessa terminologia per tutta l'attività consente di gestire gli utenti.
-   Quando si pone una domanda, usare le etichette che corrispondono alla domanda. Non usare OK/Annulla per rispondere alle domande sì/no.

    **Corretto:**

    ![screenshot dei pulsanti Sì e no ](images/ctrl-command-buttons-image37.png)

    In questo esempio, i pulsanti rispondono alla domanda.

    **Non corretto:**

    ![screenshot dei pulsanti OK e Annulla ](images/ctrl-command-buttons-image38.png)

    In questo esempio, i pulsanti non rispondono alla domanda.

-   Terminare l'etichetta con i puntini di sospensione se il comando richiede informazioni aggiuntive da eseguire.

    -   **Eccezione:** Le etichette grafiche non accettano i puntini di sospensione.

    **Corretto:** (se viene visualizzata una finestra di dialogo delle opzioni di stampa)

    ![cattura di schermata del pulsante stampa con ellissi ](images/ctrl-command-buttons-image39.png)

    In questo esempio, dopo aver fatto clic sul pulsante, viene visualizzata la finestra di dialogo Opzioni di stampa e sono necessarie altre informazioni da parte dell'utente.

-   Non usare i puntini di sospensione quando il completamento dell'azione è sufficiente per visualizzare un'altra finestra. I comandi seguenti non accettano mai i puntini di sospensione: informazioni su, avanzate, opzioni, proprietà, guida.

    **Non corretto:**

    ![cattura di schermata del pulsante Opzioni con ellissi ](images/ctrl-command-buttons-image40.png)

    In questo esempio, dopo aver fatto clic sul pulsante, viene visualizzata la finestra di dialogo Opzioni, ma non sono necessarie altre informazioni da parte dell'utente.

-   In caso di ambiguità (ad esempio, l'etichetta del comando non dispone di un verbo), decidere in base all'azione dell'utente più probabile. Se la semplice visualizzazione della finestra è un'azione comune, non usare i puntini di sospensione.

    **Corretto:**

    Altri colori...

    Informazioni sulla versione

    Nel primo esempio, gli utenti scelgono con maggiore probabilità un colore, quindi l'uso di un ellissi è corretto. Nel secondo esempio, gli utenti visualizzano con maggiore probabilità le informazioni sulla versione, rendendo inutili le ellissi.

-   Per i pulsanti Sfoglia, usare i pulsanti di esplorazione brevi (con etichetta "...") quando sono presenti più di due pulsanti di esplorazione in una finestra. Utilizzare sempre la versione abbreviata quando si desidera visualizzare un pulsante Sfoglia in una griglia.
-   Per i pulsanti direzionali, usare un'unica parentesi uncinata e fare in modo che punti nella direzione in cui si verifica l'azione.

La tabella seguente illustra alcune etichette comuni dei pulsanti di comando e il relativo utilizzo.



|                             |                                                                                                              |                             |
|-----------------------------|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| **Etichetta del pulsante**<br/> | **Significato**<br/>                                                                                       | **Chiave di accesso**<br/>   |
| **Back**<br/>         | In procedure guidate e flussi attività passare alla pagina precedente.<br/>                                               | 'B'<br/>              |
| **Sfoglia...**<br/>    | Consente di visualizzare una finestra di dialogo per la ricerca di un file o di un oggetto.<br/>                                                | ' B ' o ' r '<br/>       |
| **Opzioni**<br/>      | Consente di visualizzare le opzioni disponibili per gli utenti per la personalizzazione di un programma.<br/>                                 | 'O'<br/>              |
| **Sospendi**<br/>        | Le finestre di dialogo in corso sospendono l'attività.<br/>                                                       | P<br/>              |
| **Personalizza**<br/>  | Personalizzare un'esperienza di base essenziale per l'identificazione personale dell'utente con un programma.<br/> | P<br/>              |
| **Preferenze**<br/>  | Non usare. Usare invece le opzioni.<br/>                                                                   | Non applicabile.<br/>  |
| **Proprietà**<br/>   | Visualizza gli attributi e le impostazioni per un oggetto.<br/>                                                | ' P ' o primo ' r '<br/> |
| **Salva**<br/>         | Salvare un gruppo di impostazioni o salvare un file o un oggetto usando il nome corrente.<br/>                        | S<br/>              |
| **Salva con nome...**<br/>   | Salvare un file o un oggetto usando un nome specificato.<br/>                                                     | Secondo ' a'<br/>       |
| **Impostazioni**<br/>     | Non usare. Usare invece le opzioni.<br/>                                                                   | Non applicabile.<br/>  |
| **Risolvere i problemi**<br/> | Non usare. Usare invece uno specifico collegamento alla guida.<br/>                                                      | Non applicabile.<br/>  |



 

Per le linee guida sulle etichette dei pulsanti di commit (OK, Annulla, sì/no, Chiudi, arresta, applica, avanti, fine, operazione completata), vedere [testo dell'interfaccia utente](text-ui.md).

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai pulsanti di comando:

-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere la sottolineatura o i puntini di sospensione della chiave di accesso. Non includere il pulsante Word.
-   Per descrivere l'interazione dell'utente, utilizzare fare clic su.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempio: fare clic su **stampa** per stampare il documento.

 

