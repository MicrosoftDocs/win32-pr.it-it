---
title: Pulsanti di comando
description: Con un pulsante di comando, gli utenti avviano un'azione immediata.
ms.assetid: 0e2ff31a-657b-4e4c-afee-2a6bd742f46c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 97b452964066ce061a71a74f547305ba7d9d5794
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524585"
---
# <a name="command-buttons"></a>Pulsanti di comando

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con un pulsante di comando, gli utenti avviano un'azione immediata.

![Screenshot del pulsante di comando OK ](images/ctrl-command-buttons-image1.png)

Pulsante di comando tipico.

Il pulsante di comando predefinito viene richiamato quando gli utenti premono INVIO. Viene assegnato dallo sviluppatore, ma qualsiasi pulsante di comando diventa l'impostazione predefinita quando gli utenti lo visualizzano.

> [!Note]  
> Le linee guida [correlate al layout](vis-layout.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Il pulsante di comando viene usato per avviare un'azione immediata?** Se non è così, usa un altro controllo.
-   **Un collegamento potrebbe essere una scelta migliore?** Usare un collegamento se:
    -   L'azione consente di passare a un'altra pagina, finestra o argomento della Guida. **Eccezione:** per la navigazione della procedura guidata vengono utilizzati i pulsanti di comando Indietro e Avanti.
    -   Il comando è incorporato in un corpo di testo.
    -   Il comando è secondario per natura. Ciò significa che non è correlato allo scopo principale della finestra. In questo caso, sarebbe appropriato un pulsante di comando leggero o un collegamento.
    -   Il comando fa parte di un menu o di un gruppo di collegamenti correlati.
    -   L'etichetta è lunga, costituita da cinque o più parole, offrendo un aspetto scomodo a un pulsante di comando.
-   **Una combinazione di pulsanti di opzione e pulsanti di comando generici sarebbe una scelta migliore?** Spesso i pulsanti di opzione vengono usati insieme ai pulsanti di comando generici (OK, Annulla) al posto di un set di pulsanti di comando specifici quando si verifica uno dei seguenti:
    -   Sono disponibili cinque o più azioni possibili.
    -   Gli utenti devono visualizzare informazioni aggiuntive prima di prendere una decisione.
    -   Gli utenti devono interagire con le scelte (ad esempio per visualizzare informazioni aggiuntive) prima di prendere una decisione.
    -   Gli utenti visualizzano le opzioni come opzioni anziché come comandi diversi.

        **Corretto:** ![ Screenshot della finestra di dialogo, dei pulsanti di opzione e del testo ](images/ctrl-command-buttons-image2.png)

        In questo esempio i pulsanti di opzione vengono combinati con i pulsanti OK e Annulla per fornire informazioni aggiuntive sulle opzioni.

        **Non corretto:** ![ Screenshot del messaggio con i pulsanti di comando ](images/ctrl-command-buttons-image3.png)

        In questo esempio, i pulsanti di comando da soli rendono difficile agli utenti prendere una decisione informata.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

**Uso dei puntini di sospensione**

Anche se i pulsanti di comando vengono usati per azioni immediate, potrebbero essere necessarie altre informazioni per eseguire l'azione. **Indicare un comando che richiede informazioni aggiuntive (inclusa** la conferma) aggiungendo i puntini di sospensione alla fine dell'etichetta del pulsante .

![Screenshot del pulsante di comando stampa con puntini di sospensione ](images/ctrl-command-buttons-image4.png)

In questo esempio, print... visualizza una finestra di dialogo Stampa per raccogliere altre informazioni.

![Screenshot del pulsante di comando print, senza puntini di sospensione ](images/ctrl-command-buttons-image5.png)

Al contrario, in questo esempio il comando Stampa stampa una singola copia di un documento nella stampante predefinita senza ulteriori interazioni con l'utente.

**L'uso corretto dei puntini** di sospensione è importante per indicare che gli utenti possono effettuare altre scelte prima di eseguire l'azione o anche annullare completamente l'azione . Il segnale visivo offerto da un puntoni di sospensione consente agli utenti di esplorare il software senza timori.

**Questo non significa che è necessario** usare i puntini di sospensione ogni volta che un'azione visualizza un'altra finestra solo quando sono necessarie informazioni aggiuntive per eseguire l'azione. Di conseguenza, qualsiasi pulsante di comando il cui **verbo implicito è "mostra un'altra finestra"** non accetta i puntini di sospensione , ad esempio con i comandi Informazioni su, Avanzate, Guida (o qualsiasi altro comando che collega a un argomento della Guida), Opzioni, Proprietà o Impostazioni.

In genere, i puntini di sospensione vengono usati nelle interfacce utente per indicare l'incompletezza. I comandi che mostrano altre finestre non sono incompleti e devono visualizzare un'altra finestra e non sono necessarie informazioni aggiuntive per eseguire l'azione. Questo approccio elimina l'ingombro dello schermo in situazioni in cui i puntini di sospensione hanno poco valore.

**Nota:** Quando si determina se un pulsante di comando necessita di puntini di sospensione, non usare la necessità di elevare i [privilegi](winenv-uac.md) come fattore. L'elevazione dei privilegi non è necessaria per eseguire un comando (piuttosto che per l'autorizzazione) e la necessità di elevare è indicata con lo schermo di sicurezza.

**Se si fa una sola cosa...** Usare un'etichetta concisa, specifica e auto-esplicativa che descriva chiaramente l'azione eseguita dal pulsante di comando e usare i puntini di sospensione quando appropriato.

## <a name="usage-patterns"></a>Modelli di utilizzo

I pulsanti di comando hanno diversi modelli di utilizzo:



|     Utilizzo                                                                                                                                                                    |    Esempio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pulsanti di comando standard** È possibile usare pulsanti di comando standard per avviare un'azione immediata.<br/>                                                           | ![Screenshot del pulsante di comando standard (grigio) ](images/ctrl-command-buttons-image6.png)<br/> Pulsante di comando standard.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Pulsanti di comando predefiniti** Il pulsante di comando predefinito in una finestra indica il pulsante di comando che verrà attivato quando gli utenti premeranno INVIO.<br/>       | ![Screenshot del pulsante di comando predefinito (blu) ](images/ctrl-command-buttons-image7.png)<br/> Pulsante di comando predefinito.<br/> Qualsiasi pulsante di comando diventa l'impostazione predefinita quando gli utenti lo visualizzano. Se lo stato attivo per l'input è su un controllo che non è un pulsante di comando, il pulsante di comando con l'attributo del pulsante predefinito diventa l'impostazione predefinita. Un solo pulsante di comando in una finestra può essere l'impostazione predefinita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Pulsanti di comando leggeri** Un pulsante di comando leggero è simile a un pulsante di comando standard, ad eccezione del fatto che la cornice del pulsante viene visualizzata solo al passaggio del mouse. <br/> | ![Screenshot di uno dei due pulsanti di stampa selezionati ](images/ctrl-command-buttons-image8.png)<br/> In questo esempio il comando ha un aspetto molto leggero (simile [a](ctrl-links.md)un collegamento ) fino a quando l'utente non passa il puntatore del mouse sul comando, a quel punto viene disegnato con una cornice del pulsante.<br/> È possibile usare pulsanti di comando leggeri in situazioni in cui si usa un pulsante di comando standard, ma si vuole evitare di visualizzare sempre la cornice del pulsante. I pulsanti di comando leggeri sono ideali per i comandi da sottodimensionare e l'uso di un collegamento non sarebbe appropriato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Pulsanti di menu** Usare un pulsante di menu quando è necessario un menu per un piccolo set di comandi correlati.<br/>                                                                 | ![Screenshot del pulsante di menu Formato e dei relativi comandi ](images/ctrl-command-buttons-image9.png)<br/> Pulsante di menu con un piccolo set di comandi correlati.<br/> Usare un pulsante di menu quando una barra dei menu non è desiderabile, ad esempio in una finestra di dialogo, in una barra degli strumenti o in un'altra finestra che non dispone di una barra dei menu. Un singolo triangolo verso il basso indica che facendo clic sul pulsante verrà visualizzato un menu a discesa.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Pulsanti di divisione** Usare un pulsante di divisione per consolidare un set di varianti di un comando, soprattutto quando uno dei comandi viene usato per la maggior parte del tempo.<br/>          | ![Screenshot del pulsante di divisione aperto senza comandi ](images/ctrl-command-buttons-image10.png)<br/> pulsante di divisione compresso.<br/> come un pulsante di menu, un singolo triangolo verso il basso indica che facendo clic sulla parte più a destra del pulsante verrà visualizzato un menu a discesa.<br/> ![Screenshot del pulsante di divisione aperto con i comandi ](images/ctrl-command-buttons-image11.png)<br/> pulsante di divisione a discesa.<br/> In questo esempio viene usato un pulsante di divisione per consolidare sei varianti del comando open. Il normale comando open viene usato nella maggior parte dei casi, quindi in genere gli utenti non devono visualizzare gli altri comandi. L'uso di un pulsante di divisione consente di risparmiare una quantità significativa di spazio sullo schermo, offrendo al tempo stesso scelte avanzate.<br/> A differenza di un pulsante di menu, facendo clic sulla parte sinistra del pulsante viene eseguita direttamente l'azione sull'etichetta. I pulsanti di divisione sono efficaci in situazioni in cui è probabile che l'azione successiva con uno strumento specifico sia la stessa dell'ultima azione. In questo caso, l'etichetta viene modificata nell'ultima azione, come con un selettore colori:<br/> ![Screenshot del pulsante di divisione riempimento senza comandi ](images/ctrl-command-buttons-image12.png)<br/> In questo esempio l'etichetta viene modificata nell'ultima azione.<br/> |
| **Pulsanti Sfoglia** Usare un pulsante Sfoglia per visualizzare una finestra di dialogo che consente agli utenti di selezionare un valore valido.<br/>                                                           | Le finestre di dialogo avviate da un pulsante Sfoglia consentono agli utenti di selezionare file, cartelle, computer, utenti, colori e così via. vengono in genere combinati con un controllo senza vincoli, ad esempio una casella di testo. sono in genere etichettati come browse, other o more e hanno sempre i puntini di sospensione per indicare che sono necessarie altre informazioni. <br/> ![Screenshot della casella di testo con il pulsante Sfoglia ](images/ctrl-command-buttons-image13.png)<br/> una casella di testo con un pulsante Sfoglia.<br/> per le finestre con molti pulsanti di esplorazione, è possibile usare una versione breve:<br/> ![Screenshot del pulsante sfoglia breve con puntini di sospensione ](images/ctrl-command-buttons-image14.png)<br/> Breve pulsante Sfoglia.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Pulsanti di divulgazione progressiva** Usare un pulsante di divulgazione progressiva per visualizzare o nascondere le opzioni usate raramente.<br/>                                            | Nascondere le opzioni usate raramente fino a quando non sono necessarie è detto divulgazione progressiva. Le doppie virgolette vengono usate per indicare la divulgazione progressiva e puntano nella direzione in cui avrà luogo il revealing o il nascondimento: <br/> ![Screenshot del pulsante con "more" e le frecce a destra ](images/ctrl-command-buttons-image15.png)<br/> Dopo aver fatto clic sul pulsante, l'etichetta cambia per indicare che il clic successivo avrà l'effetto opposto:<br/> ![Screenshot del pulsante con le frecce "less" e "left" ](images/ctrl-command-buttons-image16.png)<br/> Per altre informazioni ed esempi, vedere [Controlli di divulgazione progressiva.](ctrl-progressive-disclosure-controls.md) <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Pulsanti direzionali** Usare un pulsante direzionale per indicare la direzione in cui verrà eseguita un'azione.<br/>                                               | In questo caso, viene usata una singola parentesi uncinata anziché una doppia freccia di controllo: <br/> ![Screenshot dei pulsanti freccia destra e sinistra ](images/ctrl-command-buttons-image17.png)<br/> Un pulsante direzionale indica la direzione dell'azione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Visualizzare un puntatore occupato se il risultato della selezione di un pulsante di comando non è istantaneo.** Senza commenti e suggerimenti, gli utenti potrebbero presupporre che il clic non sia stato fatto e fare di nuovo clic.
-   Se lo stesso pulsante di comando viene visualizzato in più di una finestra, provare a usare lo stesso testo dell'etichetta e la stessa chiave di accesso e, quando possibile, individuarlo approssimativamente nella stessa posizione **in ogni finestra.**
-   **Per i pulsanti di comando con etichette di testo, usare la larghezza minima del pulsante e l'altezza standard del pulsante di comando.** Per altre informazioni, vedere [Dimensioni e spaziatura consigliate.](#recommended-sizing-and-spacing)
-   Per ogni **finestra, i pulsanti di comando hanno la stessa larghezza.** Se non è pratico, limitare a due il numero di larghezze diverse per i pulsanti di comando con etichette di testo.
-   Quando un altro controllo interagisce con un pulsante di comando, ad esempio una casella di testo con un pulsante Sfoglia, indica la relazione posizionando il pulsante di comando in una **delle tre posizioni seguenti:**
    -   A destra di e allineati in alto con l'altro controllo.
    -   Sotto e allineati a sinistra con l'altro controllo.
    -   Allineato verticalmente al centro tra i controlli che interoperano , ad esempio i pulsanti Aggiungi e Rimuovi tra due caselle di riepilogo interoperativi.
-   Se più pulsanti di comando interagisce con lo stesso controllo, sovrapporrli verticalmente a destra di e allineati in alto con l'altro controllo oppure posizionarli orizzontalmente allineati a sinistra sotto **il controllo.**
-   Quando i pulsanti di comando sono subordinati ad altri controlli, usare la posizione precedente e disabilitare il pulsante di comando subordinato fino a quando non **viene selezionato il controllo superiore.**
-   **Non usare pulsanti di comando narrow, short** o tall con etichette di testo perché tendono a sembrare poco professionale. Provare a usare le larghezze e altezze predefinite.

**Risposta corretta:** ![ Screenshot del pulsante OK con dimensioni predefinite ](images/ctrl-command-buttons-image18.png)

In questo esempio la dimensione del pulsante è standard e ha un aspetto professionale.

**Risposta errata:** ![ Screenshot del pulsante OK breve ](images/ctrl-command-buttons-image19.png)

In questo esempio il pulsante è troppo piccolo.

**Risposta errata:** ![ Screenshot del pulsante OK quadrato di grandi dimensioni ](images/ctrl-command-buttons-image20.png)

In questo esempio, il pulsante ha troppo spazio intorno all'etichetta.

-   **Evitare di combinare etichette di testo e grafica sui pulsanti di comando.** La combinazione di testo e grafica aggiunge in genere confusione visiva non necessaria e non migliora la comprensione dell'utente. Prendere in considerazione la combinazione di testo e grafica solo quando la grafica facilita la comprensione, ad esempio quando è un simbolo standard per il comando o consente agli utenti di visualizzare i risultati del comando. In caso contrario, preferire il testo, ma usare testo o grafica.

**Risposta corretta:** ![ Screenshot del comando rotate con freccia curva ](images/ctrl-command-buttons-image21.png)

In questo esempio la freccia consente agli utenti di visualizzare i risultati del comando.

**Risposta corretta:** ![ Screenshot della barra degli indirizzi con icone e testo ](images/ctrl-command-buttons-image22.png)

In questo esempio i simboli standard vengono combinati con il testo per facilitare la comprensione

**Risposta errata:** ![ Screenshot del pulsante con l'icona x e annullamento ](images/ctrl-command-buttons-image23.png)

In questo esempio, l'immagine di annullamento non aggiunge nulla al testo.

-   **Non usare i pulsanti di comando per impostare lo stato**. Usare invece pulsanti di opzione o caselle di controllo. I pulsanti di comando sono solo per l'avvio di azioni.

### <a name="split-buttons"></a>Pulsanti di menu suddivisi

-   **Impostare il comando più probabilmente come comportamento predefinito.** Se è presente più di un comando probabile, sceglierne uno che non richieda informazioni aggiuntive.
-   **Se il comando più probabile è l'ultima selezione dell'utente, modificare l'etichetta del pulsante sull'ultima selezione.**
-   **Visualizzare il comando predefinito usando il testo in grassetto nel menu**. In questo modo gli utenti possono trovare più facilmente il comando predefinito, soprattutto quando il comando predefinito è dinamico o il pulsante di menu suddiviso usa un elemento grafico anziché un'etichetta di testo.

### <a name="default-values"></a>Valori predefiniti

-   Includere un pulsante di comando predefinito in ogni finestra di dialogo. **Selezionare il comando più sicuro (per evitare la perdita di dati o** l'accesso al sistema) e il comando più sicuro come predefinito. Se la sicurezza e la sicurezza non sono fattori, selezionare il comando più probabile o pratico.
-   **Non eseguire un'azione distruttiva come pulsante di comando predefinito** a meno che non sia disponibile un modo semplice per annullare il comando.

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

![Diagramma delle dimensioni dei pulsanti in pixel e dlus ](images/ctrl-command-buttons-image24.png)

Dimensioni e spaziatura consigliate per i pulsanti di comando.

## <a name="labels"></a>Etichette

-   Assegnare un'etichetta a ogni pulsante di comando.
-   Se il pulsante ha solo un'etichetta grafica, assegnarne la proprietà Name a un'etichetta di testo appropriata. In questo modo assistive technology prodotti, ad esempio le utilità per la lettura dello schermo, per fornire agli utenti informazioni alternative sull'immagine.

    ![Screenshot dei pulsanti Su, Giù e Copia ](images/ctrl-command-buttons-image25.png)

    Questo esempio mostra i pulsanti grafici. internamente, questi pulsanti sono etichettati come Indietro, Avanti e Copia.

-   Per i pulsanti di esplorazione brevi (con etichetta "..."), l'etichetta interna deve essere Sfoglia.
-   Assegnare una chiave [di accesso univoca](glossary.md). Per le linee guida, vedere [Tastiera.](inter-keyboard.md)

    **Eccezioni:**

    -   Non assegnare i tasti di scelta ai pulsanti OK e Annulla, perché INVIO è il tasto di scelta per il pulsante predefinito (che in genere è il pulsante OK) e ESC è il tasto di scelta per Annulla. In questo modo le altre chiavi di accesso sono più facili da assegnare.
    -   Non assegnare tasti di scelta ai pulsanti di esplorazione brevi (con etichetta "..."), perché non possono essere assegnati in modo univoco.

-   Preferire etichette specifiche a quelle generiche. Idealmente, gli utenti non devono leggere altro per comprendere l'etichetta. È molto più probabile che gli utenti leggono le etichette dei pulsanti di comando rispetto al testo statico.

    -   **Eccezione:** Non rinominare il pulsante Annulla se il significato di annulla non è ambiguo. Gli utenti non devono leggere tutti i pulsanti per determinare quale pulsante annulla un'azione. Tuttavia, rinominare Annulla se non è chiaro quale azione viene annullata, ad esempio quando sono presenti diverse azioni in sospeso.

    **Accettabile:**

    ![Screenshot che mostra i pulsanti "OK" e "Annulla".](images/ctrl-command-buttons-image26.png)

    In questo esempio, OK e Annulla sono etichette accettabili ma non specifiche.

    **Migliore:**

    ![Screenshot dei pulsanti masterizza CD e Annulla ](images/ctrl-command-buttons-image27.png)

    In questo esempio La masterizzazione cd è più specifica di OK.

    **Non corretto:**

    ![screenshot dei pulsanti masterizzare cd e non masterizzare cd ](images/ctrl-command-buttons-image28.png)

    In questo esempio è consigliabile usare Cancel invece di Don't Burn CD (Non masterizzare CD).

-   Iniziare le etichette con un verbo imperativo e descrivere chiaramente l'azione eseguita dal pulsante. Non usare punteggiatura finale.
    -   **Eccezione:** Le etichette standard seguenti sono accettabili senza verbi: Advanced, Back, Details, Forward, Less, More, New, Next, No, OK, Options, Previous, Properties, Settings e Yes.
-   Sebbene siano preferibili le etichette brevi, usare un testo sufficiente per spiegare il comando. Usare un oggetto diretto (un sostantivo dopo il verbo) quando l'oggetto non è evidente dal contesto. Idealmente, gli utenti non devono leggere altro per comprendere l'etichetta.

    **Accettabile:**

    ![Screenshot del pulsante con aggiungi etichetta ](images/ctrl-command-buttons-image29.png)

    In questo esempio, un'etichetta breve è accettabile se il suo significato nel contesto è immediatamente evidente.

    **Meglio:** (se l'opzione Aggiungi non è deselezionata)

    ![Screenshot del pulsante con l'etichetta Aggiungi elementi ](images/ctrl-command-buttons-image30.png)

    In questo esempio, l'aggiunta di un sostantivo al verbo favorisce la comprensione degli utenti.

    **Migliore:** (se l'opzione Aggiungi o Aggiungi elementi non è deselezionata)

    ![Screenshot del pulsante con l'aggiunta di elementi selezionati ](images/ctrl-command-buttons-image31.png)

    In questo esempio l'etichetta è auto-esplicativa.

-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md) In questo modo è più appropriato per il tono di[Windows tono di](https://msdn.microsoft.com/library/windows/desktop/aa974175.aspx) [Windows](text-style-tone.md)e l'uso di frasi brevi per i pulsanti di comando.
    -   **Eccezione:** Per le applicazioni legacy, è possibile usare l'uso di maiuscole [e](glossary.md) minuscole in stile titolo, se necessario, per evitare di combinare gli stili di combinazione di maiuscole e minuscole.
-   Non usare ora nelle etichette dei pulsanti di comando perché l'immediatezza del comando può essere data per scontata.

    -   **Eccezione:** Se necessario, usare ora per distinguere i comandi che avviano un'attività dai comandi che eseguono immediatamente un'attività.

    ![Screenshot del pulsante con l'etichetta di download ](images/ctrl-command-buttons-image32.png)

    In questo esempio, facendo clic sul pulsante di comando si passa a una finestra o a una pagina che consente agli utenti di eseguire il download.

    ![Screenshot del pulsante con l'etichetta Scarica ora ](images/ctrl-command-buttons-image33.png)

    In questo esempio, facendo clic sul pulsante di comando viene eseguito il download.

    Un solo comando in un flusso di attività deve essere etichettato con now. Ad esempio, un **comando Scarica ora** non deve mai essere seguito da un altro comando Scarica **ora.**

-   Non usare più avanti nelle etichette dei pulsanti di comando se implica un'azione che non si verifica. Ad esempio, non usare Installa in un secondo momento (a differenza di Installa ora) a meno che il comando non venga installato in un secondo momento. Usare invece Non installare o Annulla.

    **Non corretto:**

    ![Screenshot del riavvio e riavvio in un secondo momento ](images/ctrl-command-buttons-image34.png)

    In questo esempio, Riavvia in seguito implica erroneamente che il comando viene riavviato automaticamente in un secondo momento.

-   Usare un pulsante Avanzate solo per le opzioni rilevanti per gli utenti esperti o che richiedono conoscenze avanzate dell'utente. Non usare un pulsante Avanzate per le funzionalità considerate tecnologicamente avanzate. Ad esempio, la funzionalità di graffatura di una stampante non è un'opzione avanzata, ma il sistema di gestione del colore lo è.

    **Non corretto:** (se le opzioni non sono effettivamente avanzate)

    ![Screenshot del pulsante con etichetta avanzata ](images/ctrl-command-buttons-image35.png)

    In questo esempio Advanced è fuorviante.

    **Corretto:**

    ![Screenshot del pulsante con altre opzioni etichetta ](images/ctrl-command-buttons-image36.png)

    In questo esempio l'etichetta è più specifica e accurata.

-   Per i pulsanti di comando che aprono altre finestre, scegliere un'etichetta che usi parte o tutto il testo della barra del titolo della finestra secondaria. Ad esempio, un pulsante di comando con etichetta Sfoglia potrebbe aprire una finestra di dialogo intitolato Sfoglia per cartella. L'uso della stessa terminologia in tutta l'attività consente di mantenere gli utenti orientati.
-   Quando si pone una domanda, usare etichette corrispondenti alla domanda. Non usare OK/Annulla per rispondere a domande sì/no.

    **Corretto:**

    ![Screenshot dei pulsanti Sì e No ](images/ctrl-command-buttons-image37.png)

    In questo esempio i pulsanti rispondono alla domanda.

    **Non corretto:**

    ![Screenshot dei pulsanti OK e Cancel ](images/ctrl-command-buttons-image38.png)

    In questo esempio i pulsanti non rispondono alla domanda.

-   Terminare l'etichetta con i puntini di sospensione se il comando richiede informazioni aggiuntive per l'esecuzione.

    -   **Eccezione:** Le etichette grafiche non accettano i puntini di sospensione.

    **Corretto:** (se viene visualizzata una finestra di dialogo Opzioni di stampa)

    ![Screenshot del pulsante di stampa con puntini di sospensione ](images/ctrl-command-buttons-image39.png)

    In questo esempio, dopo aver fatto clic sul pulsante, viene visualizzata la finestra di dialogo Opzioni di stampa e sono necessarie altre informazioni da parte dell'utente.

-   Non usare i puntini di sospensione quando il completamento dell'azione ha esito positivo è semplicemente visualizzare un'altra finestra. I comandi seguenti non accettano mai i puntini di sospensione: Informazioni su, Avanzate, Opzioni, Proprietà, Guida.

    **Non corretto:**

    ![Screenshot del pulsante opzioni con puntini di sospensione ](images/ctrl-command-buttons-image40.png)

    In questo esempio, dopo aver fatto clic sul pulsante, viene visualizzata la finestra di dialogo Opzioni, ma non sono necessarie altre informazioni dell'utente.

-   In caso di ambiguità (ad esempio, l'etichetta del comando non dispone di un verbo), decidere in base all'azione dell'utente più probabile. Se la semplice visualizzazione della finestra è un'azione comune, non usare i puntini di sospensione.

    **Corretto:**

    Altri colori...

    Informazioni sulla versione

    Nel primo esempio, gli utenti probabilmente sceglieranno un colore, quindi l'uso di un ellisse è corretto. Nel secondo esempio, gli utenti probabilmente visualizzano le informazioni sulla versione, rendendo i puntini di sospensione superflui.

-   Per i pulsanti di esplorazione, usare brevi pulsanti di esplorazione (etichettati "...") quando in una finestra sono presenti più di due pulsanti di esplorazione. Usare sempre la versione breve quando si vuole visualizzare un pulsante Sfoglia in una griglia.
-   Per i pulsanti direzionali, usare una singola parentesi uncinata e fare in modo che punti nella direzione in cui viene eseguita l'azione.

La tabella seguente illustra alcune etichette comuni dei pulsanti di comando e il relativo utilizzo.



| Etichetta del pulsante | Significato              | Chiave di accesso   |
|-----------------------------|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| **Back**<br/>         | Nelle procedure guidate e nei flussi di attività passare alla pagina precedente.<br/>                                               | 'B'<br/>              |
| **Sfoglia...**<br/>    | Visualizzare una finestra di dialogo per cercare un file o un oggetto.<br/>                                                | 'B' o 'r'<br/>       |
| **Opzioni**<br/>      | Consente di visualizzare le opzioni disponibili per gli utenti per la personalizzazione di un programma.<br/>                                 | 'O'<br/>              |
| **Sospendi**<br/>        | Nelle finestre di dialogo in corso sospendere l'attività.<br/>                                                       | 'P'<br/>              |
| **Personalizza**<br/>  | Personalizzare un'esperienza di base fondamentale per l'identificazione personale dell'utente con un programma.<br/> | 'P'<br/>              |
| **Preferenze**<br/>  | Non usare. In alternativa, usare Opzioni.<br/>                                                                   | Non applicabile.<br/>  |
| **Proprietà**<br/>   | Visualizzare gli attributi e le impostazioni per un oggetto.<br/>                                                | 'P' o prima 'r'<br/> |
| **Salva**<br/>         | Salvare un gruppo di impostazioni o salvare un file o un oggetto usando il nome corrente.<br/>                        | 'S'<br/>              |
| **Salva con nome...**<br/>   | Salvare un file o un oggetto usando un nome specificato.<br/>                                                     | Secondo 'a'<br/>       |
| **Impostazioni**<br/>     | Non usare. In alternativa, usare Opzioni.<br/>                                                                   | Non applicabile.<br/>  |
| **Risolvere i problemi**<br/> | Non usare. Usare invece un collegamento alla Guida specifico.<br/>                                                      | Non applicabile.<br/>  |



 

Per linee guida sulle etichette dei pulsanti di commit (OK, [Annulla,](text-ui.md)Sì/No, Chiudi, Arresta, Applica, Avanti, Fine, Fine), vedere Interfaccia utente Testo .

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai pulsanti di comando:

-   Usare il testo esatto dell'etichetta, inclusa la combinazione di maiuscole e minuscole, ma non includere il carattere di sottolineatura del tasto di scelta o i puntini di sospensione. Non includere il pulsante parola.
-   Per descrivere l'interazione dell'utente, usare click.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempio: fare **clic su Stampa** per stampare il documento.

 

