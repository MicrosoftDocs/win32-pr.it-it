---
title: Testo dell'interfaccia utente
description: Il testo dell'interfaccia utente viene visualizzato nelle superfici dell'interfaccia utente.
ms.assetid: db42fe22-9baf-453a-9b89-9bbb251b0b6f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 1c1a60ba0bfef33dcf1e72c5ba19b11c4a5f38a2
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104566243"
---
# <a name="user-interface-text"></a>Testo dell'interfaccia utente

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Il testo dell'interfaccia utente viene visualizzato nelle superfici dell'interfaccia utente. Questo testo include le etichette di controllo e il testo statico:

-   Le etichette di controllo identificano i controlli e vengono posizionati direttamente o accanto ai controlli.
-   Il testo statico, che viene chiamato perché non fa parte di un controllo interattivo, fornisce agli utenti istruzioni dettagliate o spiegazioni che consentono di prendere decisioni informate.

**Nota:** Le linee guida correlate a [stile e tono](text-style-tone.md), i [tipi di carattere](vis-fonts.md)e le etichette di [controllo Como](controls.md) sono presentate in articoli distinti.

## <a name="usage-patterns"></a>Modelli di utilizzo

Il testo dell'interfaccia utente presenta diversi modelli di utilizzo:



|                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Testo per la barra del titolo**<br/> usare il testo della barra del titolo per identificare una finestra o l'origine di una finestra di dialogo. <br/>                                                                            | ![screenshot della barra del titolo delle opzioni della cartella](images/text-ui-image1.png)<br/> In questo esempio, il testo della barra del titolo identifica una finestra.<br/>                                                                                                                                                                                                                                                                                                             |
| **Istruzioni principali**<br/> utilizzare l'istruzione principale prominente per spiegare in modo conciso le operazioni da eseguire nella finestra o nella pagina. <br/>                                                      | L'istruzione deve essere un'istruzione, una direzione imperativa o una domanda specifica. le ottime istruzioni principali comunicano l'obiettivo dell'utente piuttosto che concentrarsi solo sulla modifica dell'interfaccia utente. <br/> ![screenshot della domanda: si desidera la guida più recente? ](images/text-ui-image2.png)<br/> In questo esempio, il testo dell'istruzione principale inserisce direttamente l'utente in questione in termini di vantaggio o interesse dell'utente.<br/>             |
| **Istruzioni supplementari**<br/> Quando necessario, utilizzare un'istruzione supplementare per presentare informazioni aggiuntive utili per la comprensione o l'utilizzo della finestra o della pagina. <br/> | È possibile fornire informazioni più dettagliate, fornire contesto e definire la terminologia. le istruzioni aggiuntive elaborano l'istruzione principale senza limitarsi a ripetere la definizione. <br/> ![screenshot del testo al cambio dell'account amministratore ](images/text-ui-image3.png)<br/> In questo esempio, le istruzioni aggiuntive forniscono due possibili corsi di azione da eseguire in risposta alle informazioni presentate nell'istruzione principale.<br/> |
| **Etichette di controllo**<br/> etichette direttamente o accanto ai controlli. <br/>                                                                                                           | ![screenshot delle opzioni di clock del desktop ](images/text-ui-image4.png)<br/> In questo esempio le etichette di controllo identificano le impostazioni dell'orologio desktop che gli utenti possono selezionare o modificare.<br/>                                                                                                                                                                                                                                                                       |
| **Spiegazioni aggiuntive**<br/> elaborazione delle etichette dei controlli, in genere per i collegamenti ai comandi, i pulsanti di opzione e le caselle di controllo. <br/>                                    | ![Screenshot che mostra una finestra di dialogo Impostazioni di sicurezza.](images/text-ui-image5.png)<br/> In questo esempio, le spiegazioni aggiuntive chiariscono le scelte.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Gli sviluppatori di software spesso pensano al testo come relegato alla documentazione del prodotto e al supporto tecnico. "Prima scriviamo il codice, quindi assumiamo qualcuno che ci consentirà di spiegare cosa abbiamo sviluppato". In realtà, il testo importante viene scritto prima del processo, in quanto l'interfaccia utente è concepita e codificata. Questo testo è, dopo tutto, più frequente e da più persone che probabilmente qualsiasi altro tipo di scrittura tecnica.

**Un testo comprensibile è essenziale per l'interfaccia utente efficace.** I writer e gli editor professionali dovrebbero collaborare con gli sviluppatori di software sul testo dell'interfaccia utente come parte integrante del processo di progettazione. Fare in modo che funzionino sul testo in anticipo perché i problemi del testo spesso rivelano problemi di progettazione Se il team ha problemi a spiegare una progettazione, molto spesso è la progettazione, non la spiegazione, che necessita di miglioramento.

### <a name="a-design-model-for-ui-text"></a>Modello di progettazione per il testo dell'interfaccia utente

Quando si pensa al testo dell'interfaccia utente e alla relativa posizione nelle superfici dell'interfaccia utente, prendere in considerazione i fatti seguenti:

-   Durante la lettura immersiva e mirata, le persone leggono in un ordine da sinistra a destra, dall'alto verso il basso (nelle impostazioni cultura occidentali).
-   Quando si usa il software, gli utenti non sono immersi nell'interfaccia utente, ma nel lavoro. Di conseguenza, gli utenti non leggono il testo dell'interfaccia utente che li analizzano.
-   Quando si esegue l'analisi di una finestra, è possibile che gli utenti stiano leggendo il testo quando si filtrano in realtà. Spesso non comprendono effettivamente il testo dell'interfaccia utente, a meno che non ritengano la necessità.
-   All'interno di una finestra, diversi elementi dell'interfaccia utente ricevono diversi livelli di attenzione. Gli utenti tendono a leggere innanzitutto le etichette di controllo, in particolare quelle che risultano rilevanti per il completamento dell'attività. Al contrario, gli utenti tendono a leggere testo statico solo quando ne pensano che debbano.

Per un modello di progettazione generale, non presupporre che gli utenti leggano attentamente il testo in un ordine da sinistra a destra, dall'alto verso il basso. Piuttosto, si supponga che gli utenti inizino analizzando rapidamente l'intera finestra e quindi leggano il testo dell'interfaccia utente approssimativamente nell'ordine seguente:

-   Controlli interattivi al centro
-   [Pulsanti commit](glossary.md)
-   Controlli interattivi trovati altrove
-   Istruzione principale
-   Spiegazioni aggiuntive
-   Titolo della finestra
-   Altro testo statico nel corpo principale
-   Note a piè di pagina

Si supponga inoltre che, una volta che gli utenti hanno deciso come procedere, interrompono immediatamente la lettura e l'esecuzione.

### <a name="eliminate-redundancy"></a>Elimina ridondanza

Il testo ridondante non solo occupa uno spazio dello schermo valido, ma indebolisce l'efficacia delle idee o delle azioni importanti che si sta tentando di trasferire. Si tratta anche di uno spreco del tempo del lettore e molto altro in un contesto in cui l'analisi è la norma. **Windows si impegna a spiegare quali utenti devono eseguire una sola volta e in modo conciso.**

Esaminare ogni finestra ed eliminare parole e istruzioni duplicate, sia all'interno che tra i controlli. Non è possibile evitare che un testo importante venga esplicito laddove necessario, ma non è ridondante e non spiega l'ovvio.

### <a name="avoid-over-communication"></a>Evitare la sovracomunicazione

Anche se il testo non è ridondante, può essere semplicemente troppo elaborato per spiegare ogni dettaglio. **Una quantità eccessiva di testo scoraggia la lettura degli occhi tende a ignorarla in modo ironico, causando una minore comunicazione anziché altro ancora.** Nel testo dell'interfaccia utente, comunicare concisamente le informazioni essenziali. Se sono necessarie altre informazioni per alcuni utenti o per alcuni scenari, fornire un collegamento a un [contenuto della Guida](winenv-help.md)più dettagliato o forse a una voce di glossario per chiarire un periodo di validità.

**Non corretto:**

![screenshot della finestra di dialogo con 6 paragrafi](images/text-ui-image6.png)

In questo esempio c'è troppo testo da analizzare facilmente. Sebbene non sia previsto dalla finestra di progettazione, c'è molto testo che gli utenti più probabilmente faranno clic su Avanti senza alcuna lettura.

Per evitare il testo che sconsiglia la lettura, creare il testo per eseguire ogni conteggio delle parole. Ciò che non viene aggiunto sottrae, quindi utilizzare un testo semplice e conciso.

### <a name="use-the-inverted-pyramid"></a>Usare la piramide invertita

La scrittura accademica USA in genere uno stile strutturale "piramide" che definisce una base di fact, lavora con tali fact e si basa su una conclusione che costituisce una struttura a piramide. Al contrario, i giornalisti utilizzano uno stile "piramide invertita" che inizia con la conclusione dell'"asporto" fondamentale che i lettori devono avere. Viene quindi compilato progressivamente più dettagliatamente che i lettori potrebbero essere interessati ad analizzare. Il vantaggio di questo stile è il fatto che si trova fin dall'ora e consente ai lettori di arrestare la lettura in qualsiasi momento, ma anche di comprendere le informazioni essenziali.

È necessario applicare la struttura della piramide invertita al testo dell'interfaccia utente. È possibile passare direttamente alle informazioni essenziali, consentire agli utenti di interrompere la lettura in qualsiasi momento, e usare un collegamento alla guida per presentare il resto della piramide.

![screenshot del messaggio al programma Windows join ](images/text-ui-image7.png)

In questo esempio, le informazioni essenziali si trovano nella query del testo dell'istruzione principale, altre informazioni utili sono incluse nelle istruzioni aggiuntive e i dettagli sono disponibili facendo clic su un collegamento della guida.

**Se si eseguono solo cinque operazioni...**

1.  Lavorare sul testo in anticipo perché i problemi del testo rivelano spesso problemi di progettazione.
2.  Progettare il testo per l'analisi.
3.  Eliminare il testo ridondante.
4.  Usare un testo di facile comprensione; non comunicare eccessivamente.
5.  Quando necessario, fornire collegamenti al contenuto della Guida per ottenere informazioni più dettagliate.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Rimuovere il testo ridondante.** Cercare il testo ridondante nei titoli delle finestre, le istruzioni principali, le istruzioni aggiuntive, le aree di contenuto, i collegamenti ai comandi e i pulsanti di commit. In genere, lasciare il testo completo nelle istruzioni principali e i controlli interattivi e rimuovere qualsiasi ridondanza dalle altre posizioni.
-   **Evitare grandi blocchi di testo dell'interfaccia utente.** Di seguito sono riportate alcune modalità:
    -   Suddivisione in blocchi del testo in frasi e paragrafi più brevi.
    -   Quando necessario, fornire [collegamenti alla guida](winenv-help.md) a informazioni utili, ma non essenziali.
-   **Scegliere i nomi degli oggetti e le etichette che comunicano chiaramente e distinguere le operazioni svolte dall'oggetto.** Non è necessario che gli utenti riescano a capire cosa significa l'oggetto o come si differenzia da altri oggetti.

    Non corretto:

    ![screenshot dell'elenco di monitoraggi senza nome](images/text-ui-image8.png)

    Migliore:

    ![screenshot dell'elenco degli adattatori di rete specifici](images/text-ui-image9.png)

    Nell'esempio errato, i nomi degli oggetti non sono differenziati. Nell'esempio migliore viene illustrata la differenziazione avanzata in base al nome del prodotto.

-   **Per assicurarsi che gli utenti leggano un testo specifico correlato a un'azione, posizionarlo su un controllo interattivo.**
    -   **Accettabile:**
    -   ![screenshot dell'avviso di formattazione con il pulsante OK ](images/text-ui-image10.png)
    -   In questo esempio, è possibile che gli utenti non leggano il testo che spiega cosa ne confermano.
    -   **Migliore:**
    -   ![screenshot del pulsante Formatta avviso e formattazione ](images/text-ui-image11.png)
    -   In questo esempio, è possibile assicurarsi che almeno gli utenti capiscano che sta per formattare un disco.
-   **Usare uno spazio tra le frasi.** Non due.

### <a name="text-fonts-sizes-and-colors"></a>Tipi di carattere, dimensioni e colori del testo

-   **Usare solo testo blu per i collegamenti e le istruzioni principali.**
-   **Usare il testo verde solo per gli URL nei risultati della ricerca.**

I tipi di carattere e i colori seguenti sono valori predefiniti per Windows.



| Modello                                                                                     | Simbolo del tema                            | Tipo di carattere, colore                                                           |
|--------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![prima colonna: testo della barra del titolo ](images/text-ui-image12.png)<br/>              | CaptionFont<br/>      | 9 PT. nero ( \# 000000) Segoe UI<br/>                 |
| ![prima colonna: istruzioni principali ](images/text-ui-image13.png)<br/>           | MainInstruction<br/>  | 12 PT. blu ( \# 003399) Segoe UI<br/>                 |
| ![prima colonna: istruzioni secondarie ](images/text-ui-image14.png)<br/>      | Istruzione<br/>      | 9 PT. nero ( \# 000000) Segoe UI<br/>                 |
| ![prima colonna: testo normale ](images/text-ui-image15.png)<br/>                 | BodyText<br/>         | 9 PT. nero ( \# 000000) Segoe UI<br/>                 |
| ![prima colonna: testo enfatizzato ](images/text-ui-image16.png)<br/>             | BodyText<br/>         | 9 PT. Segoe UI nero ( \# 000000), grassetto o corsivo<br/> |
| ![prima colonna: testo modificabile ](images/text-ui-image17.png)<br/>               | BodyText<br/>         | 9 PT. Segoe UI nero ( \# 000000), in una casella<br/>       |
| ![prima colonna: testo disabilitato ](images/text-ui-image18.png)<br/>               | Disabled<br/>         | 9 PT. grigio scuro ( \# 323232) Segoe UI<br/>             |
| ![prima colonna: collegamento ](images/text-ui-image19.png)<br/>                        | HyperLinkText<br/>    | 9 PT. blu ( \# 0066CC) Segoe UI<br/>                  |
| ![prima colonna: collegamenti (hover) ](images/text-ui-image20.png)<br/>               | Accesso frequente<br/>              | 9 PT. blu chiaro ( \# 3399FF) Segoe UI<br/>            |
| ![prima colonna: intestazione di gruppo ](images/text-ui-image21.png)<br/>                |  <br/>                | 11 PT. blu ( \# 003399) Segoe UI<br/>                 |
| ![prima colonna: nome file (nella visualizzazione contenuto) ](images/text-ui-image22.png)<br/> |  <br/>                | 11 PT. nero ( \# 000000) Segoe UI<br/>                |
| ![prima colonna: testo del documento ](images/text-ui-image23.png)<br/>               | (nessuna)<br/>           | 9 PT. nero ( \# 000000) calibri<br/>                  |
| ![prima colonna: intestazioni di documento ](images/text-ui-image24.png)<br/>           | (nessuna)<br/>           | 17 PT. nero ( \# 000000) calibri<br/>                 |



 

Per ulteriori informazioni ed esempi, vedere [tipi di carattere](vis-fonts.md) e [colore](vis-color.md).

### <a name="other-text-characteristics"></a>Altre caratteristiche del testo

**Grassetto**

-   **Per attirare l'attenzione sul testo, gli utenti devono leggere in grassetto.** Ad esempio, gli utenti che analizzano un elenco di opzioni dei pulsanti di opzione possono apprezzare la visualizzazione delle etichette in grassetto, per distinguersi dal testo che aggiunge informazioni aggiuntive su ogni opzione. Tenere presente che l'utilizzo di una quantità eccessiva di grassetto ne riduce l'effetto.
-   **Con i dati con etichetta, utilizzare grassetto per evidenziare qualunque sia l'aspetto più importante per i dati nel suo complesso.**
    -   Per la maggior parte dei dati generici (in cui i dati hanno un significato minimo senza le etichette, come per i numeri o le date), usare etichette grassetto e dati semplici in modo che gli utenti possano analizzare e comprendere più facilmente i tipi di dati.
    -   Per la maggior parte dei dati con spiegazione automatica, usare etichette semplici e dati in grassetto in modo che gli utenti possano concentrarsi sui dati stessi.
    -   In alternativa, è possibile usare il testo grigio scuro per delineare le informazioni meno importanti anziché usare il grassetto per evidenziare le informazioni più importanti.

        ![screenshot della visualizzazione anteprima di Esplora risorse ](images/text-ui-image25.png)

        In questo esempio, anziché enfatizzare i dati usando Bold, le etichette vengono deaccentuate usando il grigio scuro.

-   **Non tutti i tipi di carattere supportano bold, quindi non dovrebbe mai essere fondamentale comprendere il testo.**

**Corsivo**

-   Utilizzare per fare riferimento letteralmente al testo. Non usare le virgolette per questo scopo.

    **Corretto:**

    I termini documento e file vengono spesso usati in modo interscambiabile.

-   Usare per le [richieste](glossary.md) nelle [caselle di testo](ctrl-text-boxes.md) e negli elenchi a [discesa modificabili](/windows/desktop/uxguide/ctrl-drop).

    ![screenshot della casella di testo di ricerca ](images/text-ui-image26.png)

    In questo esempio, il prompt nella casella di ricerca viene formattato come testo in corsivo.

-   Usare sporadicamente per evidenziare parole specifiche per facilitare la comprensione.
-   **Non tutti i tipi di carattere supportano il corsivo, quindi non dovrebbe mai essere fondamentale comprendere il testo.**

**Grassetto corsivo**

-   Non usare nel testo dell'interfaccia utente.

**Sottolineato**

-   Non usare, eccetto i collegamenti.
-   Non usare per l'enfasi. In alternativa, usare Italic.

### <a name="punctuation&quot;></a>Punteggiatura

**Periodi**

-   **Non inserire alla fine delle etichette dei controlli, delle istruzioni principali o dei collegamenti alla guida.**
-   Inserire alla fine di istruzioni aggiuntive, spiegazioni aggiuntive o qualsiasi altro testo statico che formi una frase completa.

**Punti interrogativi**

-   **Inserire alla fine di tutte le domande.** A differenza dei periodi, i punti interrogativi vengono usati per tutti i tipi di testo.

**Punti esclamativi**

-   In applicazioni aziendali evitare.
    -   **Eccezioni:** I punti esclamativi vengono talvolta usati nel contesto di completamento del download (&quot;Done!") e per richiamare l'attenzione sul contenuto Web ("New!").

**Virgole**

-   In un elenco di tre o più elementi, inserire sempre una virgola dopo l'elemento successivo all'ultimo nell'elenco.

**Due punti**

-   **Usare i due punti alla fine delle etichette del controllo esterno.** Questa operazione è particolarmente importante per l'accessibilità perché alcune tecnologie per l'accessibilità cercano i due punti per identificare le etichette dei controlli.
-   Usare i due punti per introdurre un elenco di elementi.

**Puntini**

-   **I puntini di sospensione indicano l'incompletezza.** Usare i puntini di sospensione nel testo dell'interfaccia utente come segue:
    -   **Comandi:** Indica che per un comando sono necessarie informazioni aggiuntive. Non usare i puntini di sospensione ogni volta che un'azione Visualizza un'altra finestra solo quando sono necessarie informazioni aggiuntive. Per ulteriori informazioni, vedere [pulsanti di comando](ctrl-command-buttons.md).
    -   **Dati:** Indica che il testo è troncato.
    -   **Etichette:** Indica che è in corso un'attività (ad esempio, "ricerca in corso...").

        **Suggerimento:** Il testo troncato in una finestra o in una pagina con spazio inutilizzato indica un layout insufficiente o una dimensione della finestra predefinita troppo piccola. Cercare i layout e le dimensioni predefinite della finestra che eliminano o riducono la quantità di testo troncato. Per altre informazioni, vedere [Layout](vis-layout.md).

-   **Non rendere interattive le ellisse.** Per visualizzare il testo troncato, consentire agli utenti di ridimensionare il controllo per visualizzare più testo o usare invece un [controllo di divulgazione progressiva](ctrl-progressive-disclosure-controls.md) .

**Virgolette e apostrofi**

-   Per fare riferimento al testo in modo letterale, utilizzare la formattazione corsivo anziché le virgolette.
-   Inserire i titoli delle finestre e le etichette di controllo tra virgolette solo se necessario per evitare confusione e non è possibile formattare con grassetto.
-   Per le virgolette, preferire le virgolette doppie (""); evitare virgolette singole.

    **Corretto:**

    Eliminare la "cartella Cat di Sparky"?

    **Non corretto:**

    Eliminare ' la cartella Cat di Sparky '?

### <a name="capitalization"></a>Uso delle maiuscole

-   **Usare l'uso di maiuscole in stile titolo per i titoli, le maiuscole in stile frase per tutti gli altri elementi dell'interfaccia utente.** Questa operazione è più appropriata per il [tono di Windows](text-style-tone.md).

    -   **Eccezione:** Per le applicazioni legacy, è possibile usare la capitalizzazione in stile titolo per i pulsanti di comando, i menu e le intestazioni di colonna, se necessario, per evitare di combinare gli stili di maiuscole e minuscole.

        ![screenshot della finestra delle proprietà generica ](images/text-ui-image27.png)

    Questo esempio generico Mostra la maiuscola e la punteggiatura corrette per le finestre delle proprietà.

    ![screenshot della finestra di dialogo generica ](images/text-ui-image28.png)

    Questo esempio generico Mostra la maiuscola e la punteggiatura corrette per le finestre di dialogo.

-   **Per i nomi delle funzionalità e delle tecnologie, è opportuno tenere in maiuscolo.** In genere, solo i componenti principali devono essere in lettere maiuscole (usando la maiuscola in stile titolo).

    **Corretto:**

    Analysis Services, cubi, dimensioni

    Analysis Services è un componente principale di SQL Server, quindi le maiuscole in stile titolo sono appropriate; i cubi e le dimensioni sono elementi comuni del software di analisi dei database, pertanto non è necessario capitalizzarli.

-   **Per i nomi delle funzionalità e delle tecnologie, è necessario essere coerenti.** Se il nome viene visualizzato più di una volta in una schermata dell'interfaccia utente, deve sempre apparire allo stesso modo. Analogamente, in tutte le schermate dell'interfaccia utente del programma, il nome deve essere presentato in modo coerente.
-   Non capitalizzare i nomi degli elementi generici dell'interfaccia utente, ad esempio barra degli strumenti, menu, barra di scorrimento, pulsante e icona.
    -   **Eccezioni:** Barra degli indirizzi, barra collegamenti.
-   Non usare lettere maiuscole per i tasti di scelta rapida. Seguire invece le maiuscole usate dalle tastiere standard o minuscole se la chiave non è etichettata sulla tastiera.

    **Corretto:**

    barra spaziatrice, TAB, invio, PGSU, CTRL + ALT + CANC

    **Non corretto:**

    BARRA SPAZIATRICE, TAB, INVIO, PG SU, CTRL + ALT + CANC

-   **Non usare tutte le lettere maiuscole per l'enfasi.** Gli studi hanno dimostrato che questo è difficile da leggere e gli utenti tendono a considerarlo come "Screaming". Per gli avvisi, usare un'icona di avviso e una spiegazione chiara della situazione. Non è necessario aggiungere, ad esempio, il termine avviso in lettere maiuscole.

Per ulteriori informazioni, vedere la sezione "testo" o "etichette" nelle linee guida specifiche dei componenti dell'interfaccia utente.

### <a name="dates-and-times"></a>Date e ore

-   **Non impostare come hardcoded il formato di date e ore.** Rispettare la scelta dell'utente per le impostazioni locali e le opzioni di personalizzazione per i formati di data e ora. L'utente li seleziona nell'elemento area e pannello di controllo della lingua.

    ![screenshot del formato data: lunedì, 6 luglio 2009](images/text-ui-image29.png)![screenshot del formato data: 06 luglio 2009](images/text-ui-image30.png)

    In questi esempi di Microsoft Outlook, entrambi i formati per la data estesa sono corretti. Riflettono diverse scelte effettuate dagli utenti nell'elemento Region e del pannello di controllo della lingua.

-   **Usare il formato di data estesa per gli scenari che possono trarre vantaggio dalla presenza di informazioni aggiuntive.** Usare il formato di data breve per i contesti che non dispongono di spazio sufficiente per il formato esteso. Mentre gli utenti scelgono le informazioni che desiderano includere nei formati lunghi e brevi, i progettisti scelgono il formato da visualizzare nei programmi in base allo scenario e al contesto.

    ![screenshot del formato con date di inizio e di scadenza](images/text-ui-image31.png)

    In questo esempio, il formato di data estesa consente agli utenti di organizzare le attività e le scadenze.

### <a name="globalization-and-localization"></a>Globalizzazione e localizzazione

La globalizzazione consente di creare documenti o prodotti utilizzabili in qualsiasi paese, area o cultura. La localizzazione consente di adattare i documenti o i prodotti per l'uso in impostazioni locali diverse da quelle del paese/regione di origine. Considerare la globalizzazione e la localizzazione durante la scrittura del testo dell'interfaccia utente. Il programma può essere convertito in altre lingue e usato in impostazioni cultura molto diverse da quelle personalizzate.

-   Per i controlli con contenuto variabile (ad esempio visualizzazioni elenco e visualizzazioni albero), **scegliere una larghezza appropriata per i dati più lunghi validi.**
-   **Includere spazio sufficiente nella superficie dell'interfaccia utente per un ulteriore 30%** (fino al 200% per un testo più breve) per qualsiasi testo (ma non per i numeri) che verrà localizzato. La conversione da una lingua a un'altra spesso modifica la lunghezza di riga del testo.
-   Non comporre stringhe da sottostringhe in fase di esecuzione. Usare invece frasi complete in modo che non esistano ambiguità per il traduttore.
-   **Non usare un controllo subordinato, i valori in esso contenuti o l'etichetta unità per creare una frase o una frase.** Una progettazione di questo tipo non è localizzabile perché la struttura della frase varia in base alla lingua.

    **Non corretto:**

    ![screenshot della casella di testo all'interno di un'etichetta della casella di controllo ](images/text-ui-image32.png)

    **Corretto:**

    ![screenshot della casella di testo dopo l'etichetta di una casella di controllo ](images/text-ui-image33.png)

    Nell'esempio errato, la casella di testo viene posizionata all'interno dell'etichetta della casella di controllo.

-   Non creare solo parte di una frase un collegamento perché, quando viene convertito, il testo potrebbe non rimanere insieme. Il testo del collegamento deve quindi formare una frase completa da sola.
    -   **Eccezione:** I collegamenti al glossario possono essere inseriti inline come parte di una frase.

Per ulteriori informazioni, vedere [go Global Developer Center](https://msdn.microsoft.com/goglobal/).

### <a name="title-bar-text"></a>Testo per la barra del titolo

-   Scegliere il testo della barra del titolo in base al tipo di finestra:
    -   **Finestre di programma di primo livello incentrate sui documenti:** Usare il formato "nome del programma nome documento". I nomi dei documenti vengono visualizzati per primi per fornire un'idea incentrata sui documenti.
    -   **Finestre di programma di primo livello che non sono incentrate sui documenti:** Visualizza solo il nome del programma.
    -   **Finestre di dialogo:** Consente di visualizzare il comando, la funzionalità o il programma da cui proviene la finestra di dialogo. Non usare il titolo per spiegare lo scopo della finestra di dialogo che è lo scopo delle istruzioni principali. Per altre linee guida, vedere [finestre di dialogo](win-dialog-box.md).
    -   **Procedure guidate:** Consente di visualizzare il nome della procedura guidata. Si noti che la parola "Wizard" non deve essere inclusa nei nomi delle procedure guidate. Per altre linee guida, vedere [procedure guidate](win-wizards.md).
-   **Per le finestre di programma di primo livello, se la didascalia e l'icona della barra del titolo vengono visualizzate in primo piano nella parte superiore della finestra, è possibile nascondere la didascalia e l'icona della barra del titolo per evitare la ridondanza.** Tuttavia, è comunque necessario impostare un titolo appropriato internamente per l'uso da Windows.
-   **Per le finestre di dialogo, non includere le parole "Dialog" o "Progress" nei titoli.** Questi concetti sono impliciti e l'uscita da queste parole rende i titoli più semplici da analizzare per gli utenti.

### <a name="main-instructions"></a>Istruzioni principali

-   **Utilizzare l'istruzione principale per spiegare in modo conciso le operazioni che gli utenti devono eseguire in una determinata finestra o pagina.** Le ottime istruzioni principali comunicano l'obiettivo dell'utente piuttosto che concentrarsi solo sulla modifica dell'interfaccia utente.
-   **Esprimere l'istruzione principale sotto forma di direzione imperativa o domanda specifica.**

    **Non corretto:**

    ![screenshot del nome del programma come istruzione principale ](images/text-ui-image34.png)

    In questo esempio, l'istruzione principale indica semplicemente il nome del programma; non invita esplicitamente una linea di azione che l'utente deve eseguire.

    **Eccezioni:** I messaggi di errore, i messaggi di avviso e le conferme possono utilizzare strutture di frasi diverse nelle istruzioni principali.

-   **Quando possibile, usare verbi specifici.** Verbi specifici (esempi: Connetti, Salva, installa) sono più significativi per gli utenti rispetto a quelli generici (esempi: configurazione, gestione, impostazione).
    -   Per le pagine del pannello di controllo e le pagine della procedura guidata, se non è possibile usare un verbo specifico, è preferibile omettere completamente il verbo.

        **Accettabile:**

        Immettere le impostazioni locali, l'area geografica e la lingua

        **Migliore:**

        Impostazioni locali, area geografica e lingua

    -   Per le finestre di dialogo, ad esempio messaggi di errore e avvisi, non omettere il verbo.

-   Non è necessario usare il testo dell'istruzione principale se l'aggiunta è solo ridondante o ovvia dal contesto dell'interfaccia utente.

    ![screenshot della finestra di dialogo Salva con nome ](images/text-ui-image35.png)

    In questo esempio, il contesto dell'interfaccia utente è già molto chiaro; non è necessario aggiungere il testo principale dell'istruzione.

-   **Usare concise solo una singola frase completa.** Riduci l'istruzione principale alle informazioni essenziali. Se è necessario spiegare altro, provare a usare un'istruzione supplementare.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   **Non includere i periodi finali se l'istruzione è un'istruzione.** Se l'istruzione è una domanda, includere un punto interrogativo finale.
-   **Per le finestre di dialogo dello stato di avanzamento, utilizzare una frase gerundio per spiegare brevemente l'operazione in corso,** terminando con i puntini di sospensione. Esempio: "stampa delle immagini in corso..."
-   **Suggerimento:** È possibile valutare un'istruzione principale immaginando ciò che si potrebbe dire a un amico quando si spiega cosa fare con la finestra o la pagina. Se la risposta con l'istruzione principale è non naturale, non utile o imbarazzante, rielaborare l'istruzione.

Per ulteriori informazioni, vedere la sezione "istruzione principale" nelle linee guida specifiche dei componenti dell'interfaccia utente.

### <a name="supplemental-instructions"></a>Istruzioni supplementari

-   Quando necessario, **utilizzare un'istruzione supplementare per presentare informazioni aggiuntive utili per la comprensione o l'utilizzo della finestra o della pagina,** ad esempio:
    -   Fornire il contesto per spiegare il motivo per cui la finestra viene visualizzata se si tratta di un programma o di un sistema avviato.
    -   Informazioni idonee che consentono agli utenti di decidere come agire sull'istruzione principale.
    -   Definizione di una terminologia importante.
-   **Non usare un'istruzione supplementare se non ne è necessario uno.** È preferibile comunicare tutti gli elementi con l'istruzione principale se è possibile eseguire questa operazione in modo conciso.
-   **Non ripetere l'istruzione principale con una formulazione leggermente diversa.** Omettere invece l'istruzione supplementare se non è necessario aggiungere altro.
-   Usare frasi complete e maiuscole/minuscole in stile frase.

### <a name="control-labels"></a>Etichette di controllo

-   **Etichettare ogni controllo o gruppo di controlli. Eccezioni**
    -   Le caselle di testo e gli elenchi a discesa possono essere etichettati usando i prompt.
    -   I controlli di divulgazione progressivi sono in genere senza etichetta.
    -   **I controlli subordinati usano l'etichetta del controllo associato.** I controlli di selezione sono sempre controlli subordinati.
    -   **Omettere le etichette dei controlli che riportano l'istruzione principale.** In questo caso, l'istruzione principale accetta il tasto di accesso.

        **Accettabile:**

        ![screenshot della casella di testo con l'istruzione e l'etichetta ](images/text-ui-image36.png)

        In questo esempio, l'etichetta della casella di testo è semplicemente una ripubblicazione dell'istruzione principale.

        **Migliore:**

        ![screenshot della casella di testo con solo istruzioni ](images/text-ui-image37.png)

        In questo esempio, l'etichetta ridondante viene rimossa, quindi l'istruzione principale accetta il tasto di accesso.

-   Posizione etichetta:
    -   Gli aerostati, le caselle di controllo, i pulsanti di comando, le caselle di gruppo, i collegamenti, le schede e i suggerimenti sono contrassegnati direttamente dal controllo stesso.
    -   Gli elenchi a discesa, le caselle di riepilogo, le visualizzazioni elenco, le barre di stato, i dispositivi di scorrimento, le caselle di testo e le visualizzazioni ad albero sono contrassegnati sopra, a sinistra o a sinistra.
    -   I controlli di divulgazione progressivi sono in genere senza etichetta. I pulsanti con la freccia di espansione sono contrassegnati a destra.
-   **Assegnare una chiave di accesso univoca per ogni controllo interattivo** tranne che per i collegamenti. Per ulteriori informazioni, vedere [tastiera](inter-keyboard.md).
-   **Mantieni brevi le etichette.** Si noti, tuttavia, che l'aggiunta di una parola o di due a un'etichetta può contribuire a semplificare e talvolta Elimina la necessità di spiegazioni aggiuntive.
-   **Preferisci etichette specifiche rispetto a quelle generiche.** Idealmente, gli utenti non devono leggere nient'altro per comprendere l'etichetta.

    **Non corretto:**

    ![screenshot del pulsante di comando OK ](images/text-ui-image38.png)

    **Corretto:**

    ![screenshot del pulsante di comando pubblica ](images/text-ui-image39.png)

    Nell'esempio corretto, per il pulsante commit viene utilizzata un'etichetta specifica.

-   **Per gli elenchi di etichette, ad esempio i pulsanti di opzione, utilizzare** la formulazione parallela e provare a rimanere la stessa lunghezza per tutte le etichette.
-   **Per gli elenchi di etichette, concentrare il testo dell'etichetta sulle differenze tra le opzioni.** Se tutte le opzioni hanno lo stesso testo introduttivo, spostare il testo nell'etichetta del gruppo.

    **Non corretto:**

    ![screenshot delle etichette con prime frasi duplicate](images/text-ui-image40.png)

    **Corretto:**

    ![cattura di schermata della prima frase spostata nell'etichetta del gruppo](images/text-ui-image41.png)

    Nell'esempio corretto viene spostata l'espressione introduttiva identica all'etichetta, quindi le due opzioni sono più pulite.

-   **In generale, è preferibile la formulazione positiva.** Ad esempio, utilizzare do anziché do not e notify anziché non inviare notifiche.
    -   **Eccezione:** L'etichetta della casella di controllo "non visualizzare più questo messaggio" è ampiamente usata.
-   **Omette i verbi di istruzione che si applicano a tutti i controlli del tipo specificato.** Concentrare invece le etichette sulle informazioni univoche sui controlli. Ad esempio, è possibile che gli utenti debbano digitare in un controllo casella di testo o che gli utenti debbano fare clic su un collegamento.

    **Non corretto:**

    ![screenshot dell'etichetta: "digitare il nome" ](images/text-ui-image42.png)

    **Corretto:**

    ![screenshot dell'etichetta:' Your Name ' ](images/text-ui-image43.png)

    Negli esempi non corretti, le etichette dei controlli dispongono di verbi di istruzioni che si applicano a tutti i controlli del relativo tipo.

-   In alcuni casi, le seguenti annotazioni di parentesi per controllare le etichette possono essere utili:
    -   **Se un'opzione è facoltativa, è consigliabile aggiungere "(facoltativo)" all'etichetta.**
    -   **Se un'opzione è fortemente consigliata, aggiungere "(scelta consigliata)" all'etichetta.** In questo modo l'impostazione è facoltativa, ma deve essere impostata comunque.
    -   **Se un'opzione è destinata solo agli utenti avanzati, è consigliabile aggiungere "(Advanced)" all'etichetta.**
-   È possibile specificare unità (secondi, connessioni e così via) tra parentesi dopo l'etichetta.

    ![screenshot dell'etichetta: dimensioni iniziali (MB) ](images/text-ui-image44.png)

    Questo esempio mostra che l'unità di misura è megabyte (MB).

Per ulteriori informazioni, vedere la sezione "testo" o "etichette" nelle linee guida specifiche dei componenti dell'interfaccia utente.

### <a name="supplemental-explanations"></a>Spiegazioni aggiuntive

-   **Usare spiegazioni aggiuntive quando i controlli richiedono più informazioni rispetto a quelle che possono essere fornite dall'etichetta.** Tuttavia, non usare una spiegazione aggiuntiva se non è necessario comunicare tutti gli elementi con l'etichetta del controllo se è possibile eseguire questa operazione in modo conciso. In genere, vengono usate spiegazioni aggiuntive con i collegamenti ai comandi, i pulsanti di opzione e le caselle di controllo.
-   Quando necessario, **utilizzare grassetto nelle etichette dei controlli per semplificare l'analisi del testo** quando sono presenti spiegazioni aggiuntive.

    ![screenshot della finestra di dialogo Impostazioni di sicurezza ](images/text-ui-image45.png)

    In questo esempio, le etichette dei pulsanti di opzione sono in grassetto per facilitarne l'analisi.

-   **L'aggiunta di una spiegazione aggiuntiva a un controllo in un gruppo non significa che è necessario fornire spiegazioni per tutti gli altri controlli nel gruppo.** Fornire le informazioni rilevanti nell'etichetta se è possibile e utilizzare le spiegazioni solo quando necessario. Non hanno spiegazioni aggiuntive che riportano semplicemente l'etichetta per la coerenza.

    ![Screenshot di tre pulsanti di opzione ](images/text-ui-image46.png)

    In questo esempio, due controlli nel gruppo includono spiegazioni aggiuntive, ma il terzo non lo è.

-   Se una spiegazione supplementare segue il collegamento di un comando, scrivere il testo supplementare nella seconda persona.

    **Esempio:** Collegamento di comando: crea impostazioni di rete wireless e Salva in unità flash USB

    Spiegazione supplementare: questa operazione creerà le impostazioni che è possibile trasferire al router con un'unità flash USB. Eseguire questa operazione solo se si dispone di un router wireless che supporta la configurazione dell'unità flash USB.

-   Usare le frasi complete e la punteggiatura finale.

### <a name="commit-button-labels"></a>Etichette di pulsanti di commit

Nella tabella seguente vengono illustrate le etichette dei pulsanti di commit più comuni e il relativo utilizzo.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Etichetta del pulsante</strong><br/></td>
<td><strong>Significato</strong><br/></td>
<td><strong>Quando usarla</strong><br/></td>
<td><strong>Chiave di accesso</strong><br/></td>
</tr>
<tr class="even">
<td><strong>OK</strong><br/></td>
<td><ul>
<li>Nelle finestre di dialogo: applicare le modifiche o eseguire il commit nell'attività e chiudere la finestra.</li>
<li>In finestre Proprietà proprietario: applica le modifiche in sospeso (effettuate dopo l'apertura della finestra o l'ultima applicazione) e chiude la finestra.</li>
<li>Nelle finestre delle proprietà di proprietà: Mantieni le modifiche, Chiudi la finestra e applica le modifiche quando vengono applicate le modifiche della finestra proprietaria.</li>
</ul></td>
<td><ul>
<li>Usare con Windows che non sono specifici dell'attività, ad esempio le finestre delle proprietà.</li>
<li>Per Windows utilizzato per eseguire un'attività specifica, utilizzare invece un'etichetta specifica che inizia con un verbo (ad esempio: Print).</li>
<li>Per Windows in cui gli utenti non possono apportare modifiche, usare Chiudi.</li>
</ul></td>
<td>Immettere<br/></td>
</tr>
<tr class="odd">
<td><strong>Sì/No</strong><br/></td>
<td>Sì è la risposta affermativa a una domanda sì o no, mentre no è la risposta negativa.<br/></td>
<td><ul>
<li>Usare i pulsanti Sì e no solo per rispondere alle domande sì o no. Non usare mai OK e Annulla per domande sì o no.</li>
<li>Preferisce risposte specifiche sui pulsanti Sì e no. Sebbene non esistano problemi con l'uso di sì e No, le risposte specifiche possono essere interpretate più rapidamente, ottenendo un processo decisionale efficace.</li>
<li>Tuttavia, si consiglia di usare Sì e nessuna risposta se il formulazione di risposte specifiche risulta troppo lungo o imbarazzante.</li>
<li>Non usare i pulsanti Sì e no se il significato di nessuna risposta non è chiaro. In caso affermativo, usare invece risposte specifiche.</li>
<li>Sì e no devono essere sempre usati come coppia.</li>
</ul></td>
<td>Y e N<br/></td>
</tr>
<tr class="even">
<td><strong>Annulla</strong><br/></td>
<td><ul>
<li>Nelle finestre di dialogo: rimuovere tutte le modifiche o il lavoro in corso, ripristinare lo stato precedente (lasciando nessun effetto collaterale evidente) e chiudere la finestra.</li>
<li>Nelle finestre delle proprietà: rimuovere tutte le modifiche in sospeso (effettuate dopo l'apertura della finestra o l'ultima applicazione) e chiudere la finestra.</li>
<li>In elementi del pannello di controllo: rimuovere tutte le modifiche o il lavoro in corso, ripristinare lo stato precedente e tornare alla pagina Hub da cui è stata avviata l'attività. Se non è presente alcuna pagina Hub, chiudere invece la finestra elemento del pannello di controllo.</li>
</ul></td>
<td><ul>
<li>Usare quando è possibile rimuovere tutte le modifiche o le azioni in sospeso e qualsiasi effetto collaterale può essere annullato.</li>
<li>Per le modifiche che non possono essere eliminate, utilizzare Close. Per le azioni in corso che possono essere arrestate, usare stop. Se inizialmente le modifiche o le azioni possono essere ignorate, è possibile usare Annulla inizialmente, quindi modificare per chiudere o arrestare una volta che non può essere annullato.</li>
</ul></td>
<td>ESC<br/></td>
</tr>
<tr class="odd">
<td><strong>Close</strong><br/></td>
<td>Chiudere la finestra. Eventuali modifiche o effetti collaterali non vengono eliminati.<br/></td>
<td><ul>
<li>Usare quando le modifiche o gli effetti collaterali non possono essere rimossi. Utilizzare Close anziché Cancel per le finestre primarie.</li>
<li>Usare per Windows in cui gli utenti non possono apportare modifiche.</li>
</ul></td>
<td>ALT + F4, CTRL + F4<br/></td>
</tr>
<tr class="even">
<td><strong>Stop</strong><br/></td>
<td>Arrestare un'attività attualmente in esecuzione e chiudere la finestra. Tutti i lavori in corso o gli effetti collaterali non vengono rimossi.<br/></td>
<td><ul>
<li>Usare quando il lavoro in corso e gli effetti collaterali non possono o non vengono rimossi, in genere con barre di avanzamento o animazioni.</li>
</ul></td>
<td>ESC<br/></td>
</tr>
<tr class="odd">
<td><strong>Applica</strong><br/></td>
<td>Nelle finestre delle proprietà del proprietario: applicare le modifiche in sospeso (effettuate dopo l'apertura della finestra o l'ultima applicazione), ma lasciare aperta la finestra. Questa operazione consente agli utenti di valutare le modifiche prima di chiudere la finestra delle proprietà. Nelle finestre delle proprietà di proprietà: non usare.<br/></td>
<td><ul>
<li>Utilizzare solo nelle finestre delle proprietà.</li>
<li>Fornire un pulsante applica solo se la finestra delle proprietà contiene impostazioni (almeno una) con effetti che gli utenti possono valutare in modo significativo. In genere, i pulsanti Applica vengono usati quando le impostazioni rendono visibili le modifiche. Gli utenti devono essere in grado di applicare una modifica, valutare la modifica e apportare ulteriori modifiche in base a tale valutazione. In caso contrario, rimuovere il pulsante Applica anziché disabilitarlo.</li>
</ul></td>
<td>A<br/></td>
</tr>
<tr class="even">
<td><strong>Avanti</strong><br/></td>
<td>Nelle procedure guidate e nelle attività in più passaggi: passare al passaggio successivo senza eseguire il commit dell'attività.<br/></td>
<td><ul>
<li>Utilizzare solo nelle procedure guidate e nelle attività in più passaggi per passare al passaggio successivo senza impegno.</li>
<li>L'effetto di un pulsante avanti può sempre essere annullato facendo clic su indietro.</li>
</ul></td>
<td>N<br/></td>
</tr>
<tr class="odd">
<td><strong>Fine</strong><br/></td>
<td>Nelle procedure guidate e nelle attività in più passaggi: chiudere la finestra. Se l'attività non è ancora stata eseguita, eseguire l'attività. Se l'attività è già stata eseguita, le modifiche o gli effetti collaterali non vengono rimossi.<br/></td>
<td><ul>
<li>Utilizzare solo nelle procedure guidate e nelle attività in più passaggi. Tuttavia, l'uso di Finish è sconsigliato perché è in genere disponibile un pulsante di commit migliore e più specifico:
<ul>
<li>Se si fa clic sul pulsante commit dell'attività (in modo che l'attività non sia già stata eseguita), usare un'etichetta specifica che inizia con un verbo (esempi: Print, Connect, Start) che rappresenta una risposta all'istruzione principale.</li>
<li>Se l'attività è già stata eseguita all'interno della procedura guidata, utilizzare Close in alternativa.</li>
</ul></li>
<li>Tuttavia, è possibile usare Finish quando:
<ul>
<li>L'etichetta specifica è ancora generica, ad esempio Save, Select, choose o Get.</li>
<li>L'attività comporta la modifica di un'impostazione o di una raccolta di impostazioni.</li>
</ul></li>
</ul></td>
<td>Immettere<br/></td>
</tr>
<tr class="even">
<td><strong>Completato</strong><br/></td>
<td>Non applicabile.<br/></td>
<td><ul>
<li>Non usare. L'operazione eseguita come comando è grammaticalmente errata.</li>
</ul></td>
<td>Non applicabile.<br/></td>
</tr>
</tbody>
</table>



 

