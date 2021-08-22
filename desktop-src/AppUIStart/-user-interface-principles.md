---
title: Interfaccia utente principi
description: Questo argomento illustra come implementare l'interfaccia utente intuitiva e i principi di progettazione dell'esperienza utente in Windows applicazioni.
ms.assetid: 603bc184-3eec-4281-8caa-993834da3131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57781ab2cb0a2d9574288000f65805c981afa391d49263bd21e23eeed432416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021494"
---
# <a name="user-interface-principles"></a>Interfaccia utente principi

Questo argomento illustra come implementare l'interfaccia utente intuitiva e i principi di progettazione dell'esperienza utente in Windows applicazioni.

-   [Introduzione](#introduction)
-   [Principi di base dell'interfaccia utente corretta](#the-basic-principles-of-proper-ui)
    -   [Spaziatura e posizionamento](#spacing-and-positioning)
    -   [Dimensioni](#size)
    -   [Raggruppamento](#grouping)
    -   [Intuitività](#intuitiveness)
-   [20 Suggerimenti per un'esperienza utente migliore e funzionale](#20-tips-for-a-better-functional-user-experience)
    -   [Usare gli standard](#use-standards)
    -   [Attirare l'attenzione sui pulsanti importanti](#draw-attention-to-important-buttons)
    -   [Semplificare il riconoscimento con le icone](#simplify-recognition-with-icons)
    -   [Semplificare il riconoscimento con le intestazioni](#simplify-recognition-with-headers)
    -   [Usare finestre di messaggio personalizzate](#use-custom-message-boxes)
    -   [Includi comandi alternativi](#include-alternate-commands)
    -   [Come gestire le azioni critiche](#how-to-handle-critical-actions)
    -   [Pulsanti di opzione o caselle combinate?](#radiobuttons-or-comboboxes)
    -   [Non interrompere mai l'utente.](#never-disrupt-the-user)
    -   [Specificare lo stato di avanzamento](#provide-progress-status)
    -   [Semplificare i passaggi complessi con le procedure guidate](#simplify-complex-steps-with-wizards)
    -   [Ottenere il tono del testo a destra](#get-the-tone-of-your-text-right)
    -   [A volte un controllo ListView è migliore](#sometimes-a-listview-is-better)
    -   [Semplificare la navigazione con i controlli di navigazione e le barre laterali](#simplify-navigation-with-breadcrumb-controls-and-sidebars)
    -   [Usare pretty graphics](#use-pretty-graphics)
    -   [Fornire moduli ridimensionabili quando possibile](#provide-resizable-forms-when-possible)
    -   [Fornire altre funzionalità con barre laterali/riquadri attività](#provide-more-functionality-with-sidebarstask-panes)
    -   [Scegliere una notifica](#give-a-notification-choice)
    -   [Specificare le descrizioni comando.](#provide-tooltips)
    -   [Non dimenticare le piccole cose](#do-not-forget-the-little-things)
-   [Conclusione](#conclusion)

## <a name="introduction"></a>Introduzione

Gli sviluppatori spesso non riescono a prendere in considerazione la prospettiva dell'utente finale. Gli sviluppatori lavorano sodo per far funzionare l'applicazione: i clienti si aspettano semplicemente che funzioni e la loro percezione dei centri software in base a questo requisito. Ciò vale soprattutto se si sviluppa software per la vendita al dettaglio o un elemento che verrà usato da persone non tecniche. Gli sviluppatori devono essere consapevoli delle esigenze dell'utente finale durante l'intero processo di progettazione del software.

Un'applicazione software deve essere il più semplice possibile da esplorare e usare. Con la quantità di software in fase di creazione, circa 4 applicazioni software su 10 hanno un'interfaccia utente davvero eccezionale che l'utente finale vuole realmente usare.

Viene creata una grande quantità di software per uso interno per le aziende. Indipendentemente dal fatto che sia sviluppata all'interno o sotto la cura di un consulente, spesso viene investito un minimo di tempo, lavoro o denaro per creare un'interfaccia utente migliore. Il ruolo di "finestra di progettazione" è raro nel ciclo di sviluppo, soprattutto nel mondo delle Windows applicazioni.

Esistono alcune regole di base da seguire per avere un'interfaccia utente molto più gradevole e funzionante per l'applicazione. Non richiede troppo tempo o denaro da parte dell'utente e aggiunge un buon ritorno sugli investimenti.

Prima di procedere, è necessario distinguere l'interfaccia utente dall'esperienza utente, almeno per l'ambito di questo articolo. L'interfaccia utente, o interfaccia utente, si riferisce agli oggetti visivi e ai controlli dell'applicazione, mentre l'esperienza utente, o esperienza utente, comprende sia l'interfaccia utente che il comportamento dell'applicazione correlata all'interfaccia utente, nonché la "emozione" che l'utente ottiene dall'app. Non si tratta solo di progettare un'interfaccia utente dall'aspetto eccezionale, ma anche di assicurarsi che funzioni bene.

In questa sezione verranno illustrati 20 punti di progettazione dell'esperienza utente che è possibile integrare facilmente nella fase di progettazione dell'applicazione. Il risultato sarà un'applicazione più completa con funzionalità più intuitive, ovvero un'esperienza utente umana. Come tutti sanno, la Windows di applicazioni vista dovrà avere un aspetto e un comportamento diversi. Questo argomento consente di prepararsi per le applicazioni future, offrendo agli utenti correnti un'assaggio del futuro.

Le sezioni seguenti illustrano le nozioni di base della progettazione corretta dell'interfaccia utente.

## <a name="the-basic-principles-of-proper-ui"></a>Principi di base dell'interfaccia utente corretta

Un'esperienza utente professionale dipende da questi quattro fattori:

-   Spaziatura e posizionamento
-   Dimensione
-   Raggruppamento
-   Intuitività

Con le versioni Microsoft Visual Studio precedenti alla 8.0, la spaziatura e il ridimensionamento erano nonoptimali. Una griglia 4x4 o 8x8 non sempre funziona. Con l'inclusione delle guide di allineamento, il processo è stato notevolmente semplificato. L'allineamento di un'etichetta a una casella di testo o, ancora peggiore, l'allineamento di più etichette con le caselle di testo corrispondenti era estremamente difficile nelle versioni precedenti di Visual Studio. Le guide di allineamento hanno notevolmente semplificato questo processo.

Le sezioni seguenti descrivono quattro degli aspetti più importanti della progettazione dell'esperienza utente professionale.

### <a name="spacing-and-positioning"></a>Spaziatura e posizionamento

La spaziatura tra due controlli è importante. Lo screenshot seguente illustra un  modulo di immissione di informazioni utente non progettato in modo scadente: le prime due caselle di testo sono troppo vicine, l'elenco al loro interno è troppo lontano e nel modulo è presente una grande quantità di spazio inutilizzato.

![screenshot di un modulo progettato in modo non scadente.](images/humanux-01.png)

Nello screenshot seguente è possibile visualizzare una finestra di dialogo dall'aspetto professionale con spaziatura appropriata e controlli di dimensioni appropriate. Si tratta dello stesso formato dello screenshot precedente, ma è stato modificato per usare la spaziatura consigliata dalle guide di allineamento. È sempre consigliabile allineare un'etichetta alla linea di base del testo della casella di testo o di un altro controllo accanto, anziché al bordo inferiore effettivo del controllo. Le guide di allineamento hanno un colore diverso quando viene raggiunto tale allineamento, in genere solo pochi pixel sopra il bordo inferiore.

![screenshot di un modulo più ben progettato.](images/humanux-02.png)

Anche se non esistono regole esatte per la spaziatura, le guide di allineamento forniscono linee guida estremamente utili per una spaziatura appropriata. Altri strumenti che consentono di mantenere la spaziatura appropriata sono i controlli Layout nel gruppo Della casella degli strumenti Contenitori. TableLayoutPanel è anche molto utile per la creazione di finestre di dialogo di stile modulo di immissione.

### <a name="size"></a>Dimensione

Le stesse considerazioni si applicano alle dimensioni. Quando si trascina un pulsante dalla casella degli strumenti nel form, l'altezza e la larghezza sono ideali. La larghezza massima consigliata (a parte eventuali motivi estremamente importanti) è il doppio della larghezza originale.

Se si osserva la **finestra** Esegui nel  menu **Start** o la finestra di dialogo Proprietà di qualsiasi Windows Explorer, le dimensioni del pulsante sono "a destra". Se si dispone di una funzione molto importante che l'utente finale deve notare senza errori, esistono altri metodi rispetto all'uso di un pulsante di grandi dimensioni o di colori non standard (più avanti).

Nell'immagine seguente sono visualizzati tre pulsanti. Il primo pulsante è la dimensione consigliata ed è la dimensione creata per impostazione predefinita quando viene trascinato (o si fa doppio clic) dalla casella degli strumenti. In alcuni casi, per il testo aggiuntivo è necessario ingrandire il pulsante. Il secondo pulsante mostra dimensioni grandi ma accettabili. Non creerebbe confusione per la disposizione di altri controlli. Il terzo pulsante, tuttavia, è una dimensione completamente inaccettabile. È anche possibile vedere che distorce leggermente le bitmap del tema Windows per disegnare controlli con tema. Sarà anche difficile allineare gli altri controlli in modo intuitivo.

![immagine di tre pulsanti, che aumentano le dimensioni da sinistra a destra.](images/humanux-03.png)

### <a name="grouping"></a>Raggruppamento

In genere, un'applicazione contiene molti controlli. Il raggruppamento intuitivo e appropriato consente di semplificare l'uso di tutti questi controlli. Il raggruppamento basato su funzioni o categorizzato viene eseguito in modo ottimale dai controlli Tab. Ad esempio, "Account", "Report", "Dipendenti" e "Progetti" sono candidati ideali per le schede in una tipica applicazione aziendale. Il raggruppamento di pari livello, ovvero i controlli che contribuiscono allo stesso risultato finale, viene eseguito in modo ottimale dai controlli Group. Non è consigliabile usare i pannelli con bordi per questo raggruppamento. I controlli di gruppo risparmiano il peso aggiuntivo di un controllo etichetta, soprattutto se i controlli secondari sono autoesplicativi.

I controlli Group all'interno dei controlli Group non sono consigliati a meno che non ne siano presenti più di 2 o 3 all'interno di un controllo Group di grandi dimensioni.

### <a name="intuitiveness"></a>Intuitività

Questo è l'aspetto più importante di un'esperienza utente ottimale. L'esperienza utente intuitiva non richiede spiegazioni. L'utente sa solo cosa fanno i controlli.

Un argomento importante della progettazione intuitiva è la codifica a colori. Un buon esempio viene presentato in Windows XP, che presenta nuovi pulsanti quadratici per  funzioni quali la navigazione in applicazioni con colori, le finestre di dialogo Disconi e Spegni **computer** e altre ancora.

La colorazione di questi controlli è stata determinata in base alla gravità del risultato del push del pulsante. La navigazione è verde, in modo molto simile a un semaforo "Go". L'arresto, che comporta una potenziale perdita di lavoro, è di colore rosso come un segno di avviso. I pulsanti semi-critici, ad esempio Discosto o Iberna, sono gialli. I pulsanti neutri che non hanno effetti critici sui processi di lavoro dell'utente, ad esempio la Guida, sono di colore blu. Quando si crea un'interfaccia utente con interfaccia personalizzata, è necessario tenere presenti questi aspetti del colore.

Un ottimo esempio di riconoscimento del contenuto in base ai colori è Microsoft Office OneNote. Le schede dell'applicazione possono essere impostate su colori diversi, pur rimanendo essenzialmente simile a una parte appropriata della progettazione Windows stile XP.

Un altro aspetto importante è il testo nelle applicazioni. Di recente sono stati fatti diversi tentativi per semplificare il linguaggio usato per le istruzioni scritte Windows software. L'uso del testo all'interno del software verrà illustrato più avanti, ma si notino i dettagli piccoli ma importanti seguenti.

MSN Messenger aveva una casella di controllo nella finestra **di dialogo Opzioni** contrassegnata come "Condividi funzionalità webcam". Gli sviluppatori e le persone tecnologiche sanno cosa significa, ma un utente non esperto potrebbe pensare di poter consentire anche a un altro utente all'altra estremità della chat di usare la web cam. In una versione recente è stato modificato in "My Webcam: Allow others to see that I have a webcam" (Webcam: Consenti ad altri di vedere che ho una webcam). Questo è ideale per i destinatari che potrebbero non avere conoscenze tecniche e che vengono usati per un linguaggio semplice.

Anche se un linguaggio più semplice semplifica la comprensione, c'è anche un ulteriore vantaggio. Gli studi scientifici mostrano che la nostra mente funziona più facilmente con un linguaggio più semplice quando si cerca di comprendere qualcosa di nuovo. Spesso il cervello elabora parole come "it", "for", "that" e altre parole comuni in modo così veloce e senza problemi che viene allocata una maggiore "larghezza di banda" per comprendere le parole che si distinguono, ad esempio "Webcam" o "Altri", nell'esempio precedente.

I titoli delle caselle di messaggio, le didascalie di GroupBox e altri blocchi di testo di questo tipo semplificano la trasmissione della funzione di un gruppo di controlli all'utente finale con poche parole.

Anche l'intuitività deriva dalla familiarità. Ad esempio, la posizione  dei pulsanti **OK** e Annulla è così uniforme e ben posizionata nella nostra mente che se una finestra di dialogo  contiene questi pulsanti in una sequenza inversa (**Annulla**, quindi **OK**, invece di **OK**, quindi Annulla **),** potresti semplicemente premere Annulla. Dopo aver utilizzato uno standard specifico per eseguire operazioni, Windows ad esempio applicazioni basate su più di un anno, si sviluppano abitudini. La conformità agli standard di settore (anche se non è stato specificato) semplifica l'uso del software.

In una delle prime Windows di anteprima di Vista, i  pulsanti Riduci a **icona,** Ingrandisci e Chiudi di qualsiasi finestra sono diventati diversi.  Nelle versioni precedenti di Windows (in particolare quando si usa un singolo monitor), si sviluppa l'consuetudine di spostare il cursore nell'angolo superiore destro dello schermo e di fare clic. Ciò ha sempre comportato la chiusura della finestra. In questa particolare build di Windows Vista, c'erano circa 8 pixel di spazio tra il pulsante Chiudi e il bordo più a destra della finestra. Lo spazio aggiuntivo lo rendeva interessante (ed era probabilmente necessario per l'animazione con l'alone di raffreddamento del pulsante) ma si stava distondendo perché non consentiva agli utenti di chiudere le finestre aperte con la facilità. Ricondizionare la propria mente può essere difficile. Fortunatamente, nella build seguente questo problema è stato risolto. A questo punto, c'è ancora spazio tra il bordo della finestra e il pulsante chiudi, ma facendo clic su tale spazio viene chiusa anche la finestra.

Un fattore molto importante della progettazione intuitiva è la quantità di "larghezza di banda fisica", ovvero la quantità di tempo che potrebbe essere necessario per comprendere qualcosa, che usa. Minore è l'utilizzo della "larghezza di banda", migliore sarà l'esperienza utente.

Si tratta di piccole cose che contribuiscono all'"esperienza" di utilizzo di un'applicazione software. Gli esempi seguenti offrono suggerimenti su come migliorare le applicazioni con suggerimenti e consigli reali.

## <a name="20-tips-for-a-better-functional-user-experience"></a>20 Suggerimenti per un'esperienza utente migliore e funzionale

L'obiettivo di un'esperienza utente migliore è avere un'interfaccia utente più semplice, più semplice e funzionale che abbia anche un aspetto ottimale. Questi suggerimenti consentono di modellare l'interfaccia utente in modo che sia più efficace.

### <a name="use-standards"></a>Usare gli standard

Gli standard stabiliti di qualsiasi ambiente software, a livello di sistema operativo, di marchio o di applicazione, sono molto importanti. Oltre alla personalizzazione, gli standard fungono da schema proverbiale nella mente dell'utente. Quando l'utente impiega lunghi periodi di tempo a lavorare con un'applicazione software, aumenta automaticamente la produttività a causa della crescente familiarità.

Prima di discutere degli standard, si esaminino esattamente questi standard. Gli standard includono tutti gli elementi del layout dei controlli in modo particolare nelle finestre di dialogo, ad esempio i pulsanti **OK** e **Annulla,** la forma dell'interfaccia utente, gli angoli arrotondati della parte superiore della finestra come nelle finestre di dialogo di Windows XP, gli stili delle icone, gli stili di qualsiasi altra grafica, il comportamento interattivo dell'applicazione e così via.

Se l'applicazione rientra in una rete specifica, potrebbe essere più utile seguire un set diverso di standard. Ad esempio, se l'applicazione supporta, un'applicazione o un componente aggiuntivo per, Office OneNote 2003, è opportuno seguire gli stili dell'interfaccia utente e gli standard di interattività di Office e OneNote in particolare. Ciò include l'uso Office barre dei comandi in stile standard anziché le barre degli strumenti standard e altri elementi di questo tipo, sia visivi che comportamentali. Se l'applicazione deve far parte della Microsoft Visual Studio .NET, si dispone di un set separato di standard. Di fatto, per tali applicazioni di supporto o componenti aggiuntivi, aziende come Microsoft rilasciano linee guida scritte. Si noti anche che a volte i concetti di grafica e progettazione sono proprietà intellettuale protette. Controllare sempre la documentazione appropriata per assicurarsi di avere la licenza per creare tali progettazioni.

Un terzo esempio di standard è l'ambiente Tablet PC. Questi standard superano i limiti tra le linee guida del sistema operativo e le linee guida per le applicazioni. La [documentazione di Tablet PC SDK](/previous-versions/ms840465(v=msdn.10)) contiene alcune informazioni molto utili nell'argomento "Pianificazione dell'applicazione". A differenza delle linee guida diOffice 2003 o Visual Studio, queste indicazioni di progettazione influiscono direttamente sul modo in cui l'utente interagirà con l'applicazione e sul comportamento che dovrebbe comportarsi a sua volta. Ad esempio, se sono presenti finestre di ancoraggio nell'applicazione, la documentazione consiglia di assicurarsi che sia in grado di rilevare quando viene modificato l'orientamento dello schermo e che le finestre di ancoraggio si riorganizzino correttamente con un orientamento verticale o orizzontale in base alle esigenze. Anche se non si sta progettando un'applicazione specifica per tablet, è consigliabile vedere queste linee guida.

Con l'aumento dei client intelligenti, le applicazioni stanno ora superando i limiti tra diversi hardware: PC normali, PC tablet, dispositivi mobili o ultra mobili, PC Media Center e così via. Ogni situazione richiede un set diverso (o aggiuntivo) di standard da seguire.

Quando le applicazioni condividono gli standard a livello di sistema operativo o di applicazione, gli utenti sono più a proprio a casa con il software, semplificando l'apprendimento e l'uso. Si tratta di un aumento diretto della produttività. Gli utenti vogliono essere in grado di diventare produttivi con nuovo software il più rapidamente possibile.

### <a name="draw-attention-to-important-buttons"></a>Attirare l'attenzione sui pulsanti importanti

A volte è necessario indirizzare l'utente ai pulsanti più importanti anche quando sono presenti quattro o cinque altri pulsanti intorno a esso. Se si provano le dimensioni, il colore o il tipo di carattere, si interromperebbero gli standard, che non sono consigliati. A tale scopo, è invece possibile usare un paio di semplici consigli.

Il primo è convertire gli altri pulsanti non critici in LinkLabels, come illustrato nell'immagine seguente. In questo modo, l'utente sa che questi collegamenti eseguiranno un'attività, ma la loro attenzione verrà prima sul pulsante che risalta, senza interrompere le linee guida di progettazione standard.

![Immagine di tre pulsanti convertiti in etichette di collegamento.](images/humanux-04.png)

Il secondo è inserire il pulsante critico per primo in linea, a sinistra per i layout orizzontali, come illustrato nell'immagine seguente, o in alto per i layout verticali. Si noti che questo può cambiare a seconda delle impostazioni cultura dell'utente di destinazione. È possibile ottenere risultati migliori se si posiziona il pulsante in questione all'estrema destra se l'applicazione è una lingua scritta da destra a sinistra.

![Immagine di tre pulsanti in cui il pulsante critico si trova all'estrema sinistra in un layout orizzontale.](images/humanux-05.png)

L'opzione consigliata è impostare per ricevere lo stato attivo per impostazione predefinita. Ad esempio, in una finestra di dialogo di conferma dell'eliminazione, l'opzione **No** deve essere evidenziata, in quanto impedisce all'utente di eliminare accidentalmente qualcosa.

### <a name="simplify-recognition-with-icons"></a>Semplificare il riconoscimento con le icone

Le icone, in particolare le icone di Windows XP e Office 2003 e le bitmap della barra degli strumenti, consentono di velocizzare la conoscenza dell'interfaccia utente e dell'attività che l'utente deve eseguire.

Ad esempio, quando viene visualizzata l'icona del punto esclamativo più spesso visualizzata nella finestra di messaggio, si diventa immediatamente consapevoli del livello di rischio associato ai controlli accanto a tale icona. Analogamente, quando l'applicazione inserisce molti controlli, indipendentemente dalla corretta disposta, può essere distogliato trovare il set di controlli che si sta cercando.

In Windows XP Service Pack 2 viene aggiunta una  scheda aggiornata all'applet del pannello di controllo Proprietà di sistema denominata "Aggiornamenti automatici". Sono disponibili quattro opzioni: scaricare automaticamente gli aggiornamenti, scaricare gli aggiornamenti, ma consentire all'utente di decidere quando installarli, inviare una notifica all'utente se gli aggiornamenti sono disponibili ma non avviare il download e disabilitare completamente gli aggiornamenti automatici.

Un nuovo utente del PC potrebbe non essere a conoscenza di questi aggiornamenti e potrebbe non conoscere l'opzione migliore da scegliere. Microsoft ha quindi inserito un'icona di schermatura verde con un segno di spunta grande accanto all'opzione più consigliata che indica un'opzione "sicura" e un'icona di schermatura rossa con una "x" grande accanto a quella potenzialmente dannosa per l'utente. Ciò è molto utile in situazioni critiche, soprattutto quando l'utente non ha tempo per leggere troppo testo.

Nella stessa applet **Proprietà di** sistema ogni scheda ha più caselle di gruppo con controlli diversi per attività diverse. Accanto a ogni gruppo viene posizionato un elemento grafico relativo che indica facilmente l'attività del gruppo di controlli. Questo tipo di codice grafico è simile alla codifica a colori nei file fisici o nei parcheggio. Questo vale anche per lo stesso principio di avere almeno alcuni oggetti visivi in un articolo di rivista, mantenendo l'interesse del lettore.

Anche la scelta dell'icona a destra è importante. Microsoft offre molti elementi grafici standard come parte di Visual Studio 2005. Si tratta della scelta migliore. Se si creano icone personalizzate, è consigliabile seguire gli standard a livello di sistema operativo [](#use-standards) o di applicazione per questi elementi grafici, come indicato nella sezione Usare gli standard precedente.

La [Windows linee guida per l'interazione con l'esperienza utente](/windows/apps/desktop/) contiene una guida molto utile per la creazione Windows icone di [stile.](https://msdn.microsoft.com/library/aa511280.aspx)

### <a name="simplify-recognition-with-headers"></a>Semplificare il riconoscimento con le intestazioni

Le intestazioni sono il modo perfetto per spiegare l'intero dialogo in una singola frase (e, facoltativamente, un elemento grafico). In alcuni casi, le intestazioni possono anche essere utili per gestire la navigazione e i comandi al loro interno. Le intestazioni funzionano in modo più efficace rispetto alle normali etichette di descrizione perché sono la prima cosa che un utente vede quando viene visualizzata la finestra di dialogo.

Le Windows di installazione guidata sono probabilmente le intestazioni più comuni: una semplice icona all'estrema destra; un'etichetta del titolo che descrive la finestra di dialogo (ad esempio, Selezionare la cartella di installazione); e un'intestazione secondaria che descrive lo scopo della finestra di dialogo, ad esempio Selezionare la cartella in cui verranno installati i file software.

Si supponiamo di avere una tipica applicazione aziendale con una sezione account. Seguendo il paradigma di progettazione basato su Windows Vista, è possibile fornire informazioni cruciali e comandi correlati nell'intestazione (o nel piè di pagina, se lo scenario lo richiede) stesso. L'utente ha aperto il file dell'account per "Big Company" e l'intestazione sarà simile a quella illustrata nello screenshot seguente.

![Screenshot di una finestra di dialogo che contiene un piè di pagina dettagliato.](images/humanux-06.png)

Lo screenshot seguente mostra un esempio di intestazione dettagliata in una finestra di dialogo.

![Screenshot di una finestra di dialogo che contiene un'intestazione dettagliata.](images/humanux-07.png)

Analogamente, è possibile evitare di dover aggiungere Windows riquadri attività in stile XP, soprattutto quando sono disponibili pochi comandi, che sprecano molto spazio verticale, spostando questi comandi nell'intestazione .

Quando si progettano le intestazioni, è necessario tenere presenti alcuni aspetti:

-   Assicurarsi che il colore di sfondo sia diverso dal colore di sfondo della finestra di dialogo. Più spesso, un'intestazione bianca su un controllo standard Windows il colore intrinseco del viso del controllo. Tuttavia, se vuoi assicurarti che nessun tema speciale o colori personalizzati confonda l'intestazione, disegna un **LinearGradient** usando **Color.FromKnownColor** con i colori **ControlLight** e **ControlDark.**
-   Se possibile, mantenere l'altezza dell'intestazione inferiore a 150 pixel. In genere l'altezza è 100 o 120. Come regola generale, assicurarsi che sia inferiore a 1/4 dell'altezza dell'intero modulo.
-   Se vuoi aggiungere la modifica sul posto per le informazioni mostrate nell'intestazione precedente, sostituisci dinamicamente LinkLabel con una casella di testo e scambiala di nuovo al termine della modifica.
-   Se si ha un'etichetta del titolo con un tipo di carattere di dimensioni più grandi di 10 pt, usare Arial o Arial Medium. MS Sans Serif avrà un aspetto troppo irregolare e non professionale. La raccomandazione è disponibile nella documentazione Windows xp design guidelines (Linee guida per la progettazione di XP). Per le applicazioni che Windows Vista, usare Segoe UI tipo di carattere predefinito del sistema.

### <a name="use-custom-message-boxes"></a>Usare finestre di messaggio personalizzate

Le opzioni disponibili nella finestra di Windows standard sono molto limitate. Quando è necessario porre all'utente una domanda a cui non è possibile rispondere con un semplice sì/no o OK/annulla, diventa complicato.

Windows applicazioni stanno diventando più semplici da usare a causa dell'elevato volume di utenti non tecnici. In alcuni casi può essere molto più semplice fornire ai pulsanti testi più facili e anche alcuni controlli aggiuntivi, ad esempio LinkLabels, per semplificare l'esecuzione dell'attività.

Microsoft .NET Framework semplifica l'implementazione di finestre di dialogo personalizzate. Assegnando solo un paio di proprietà nel modulo della finestra di dialogo personalizzata o con una singola riga di codice, il modulo può funzionare esattamente come una finestra di messaggio standard. In un evento button-click impostare la proprietà **DialogResult** della finestra di dialogo su **DialogResult.Ok** o **DialogResult.Cancel.** Usare il **metodo ShowDialog( \[ OwnerForm \] )** dal form padre. Questo metodo restituisce il **valore DialogResult.**

È possibile usare tutti i **membri DialogResult.** Queste stesse opzioni vengono usate dal metodo **MessageBox.Show** standard.

In alternativa, puoi semplicemente impostare la proprietà **AcceptButton** della finestra di dialogo **su btnOK** e la **proprietà CancelButton** su **btnCancel.** I tasti **INVIO** e ESC verranno mappati **automaticamente** ai rispettivi eventi Click dei pulsanti **btnOK** e **btnCancel.**

Ecco alcuni suggerimenti per creare finestre di dialogo personalizzate:

-   Per argomenti complessi, fornire collegamenti alla Guida locale o online con linkLabel che indica "Altre informazioni" sotto l'etichetta di testo appropriata.
-   Invece dei pulsanti Sì No Annulla, usare testi che specificano chiaramente il risultato del clic sul pulsante, ad esempio "Salva file ed esci", "Esci senza salvare" e /  /  "Non uscire". Tuttavia, se possibile, attenersi ai pulsanti standard  / **Sì No**, **OK** / **Annulla** e a tali pulsanti standard. La familiarità garantisce una produttività elevata.
-   Mantenere uno spazio del margine di 50 pixel a sinistra (o a destra a seconda delle impostazioni cultura di destinazione) e aggiungere un'icona che rappresenta lo scenario per la finestra di dialogo. Se si tratta di una finestra di dialogo informazioni, è possibile usare l'icona "i" usata dalle finestre di messaggio standard. Se si tratta di una finestra di dialogo di sicurezza, è possibile usare un'icona a forma di lucchetto o un'icona a forma di chiave. Visual Studio 2005 viene fornito con alcune immagini di alta qualità.
-   Assicurarsi sempre di fornire una navigazione da tastiera appropriata per questi pulsanti, ovvero gli utenti usano i tasti di scelta rapida per le finestre di messaggio (ad esempio, O per Ok, Y per Sì, C per Annulla e così via) molto di frequente. Se il dialogo personalizzato non li usasse, l'uso sarebbe sicuramente fastidioso.

### <a name="include-alternate-commands"></a>Includi comandi alternativi

Due fattori importanti determinano la necessità di metodi di input alternativi: frustrazione e laziness. La frustrazione è un evento che si verifica troppo spesso per gli utenti di computer. Quando si è frustranti, si vuole che l'attività sia eseguita rapidamente. Un clic aggiuntivo o un'attesa aggiuntiva di pochi secondi crea un problema a una persona sotto stress: si sa com'è, tutti sono stati presenti. La pigrizia spesso consente di completare l'attività solo con la tastiera o il mouse, indipendentemente dal momento in cui si sta usando. A parte questi due fattori, tuttavia, la presenza di metodi di input alternativi semplifica l'esecuzione delle attività da parte dell'utente.

Ad esempio, se si dispone di una casella di riepilogo con due pulsanti, "Aggiungi" e "Rimuovi", è necessario aggiungere un menu di scelta rapida per la casella di riepilogo con comandi di menu analoghi a tali pulsanti. In questo modo l'utente ha la possibilità di scegliere il metodo più adatto. Gli utenti non esperti, come illustrato Windows Vista User Experience Guidelines (Linee guida sull'esperienza utente di Windows Vista), usano spesso i menu di scelta rapida e si aspettano che si trovino ovunque si trovino con il pulsante destro del mouse.

Analogamente, si usano controlli visivi per l'input di testo o numerico. Ad esempio, i dispositivi di scorrimento vengono usati per specificare numeri interi e i controlli Calendar vengono usati per l'input di data. In alcuni casi può essere più comodo immettere semplicemente digitando . Spesso può fare la differenza per l'utente se si aggiunge un controllo Numeric Up-Down collegato a un dispositivo di scorrimento o si usa un controllo DateTimePicker anziché il controllo Calendar.

### <a name="how-to-handle-critical-actions"></a>Come gestire le azioni critiche

Quando si esegue una funzione critica e irreversibile, è in genere consigliabile visualizzare una finestra di messaggio per confermare l'azione. Si esamini ora questa impostazione. Nello screenshot seguente è possibile visualizzare una finestra di messaggio personalizzata simile, ma con un ulteriore vantaggio, ovvero un timer visualizzato visivamente con l'aiuto di un indicatore di stato.

![screenshot di una finestra di dialogo di azione critica.](images/humanux-08.png)

È possibile usare alcune varianti specifiche dello scenario. Se l'azione da eseguire è molto critica (dall'overload di una centrale elettrica all'eliminazione permanente di file), l'azione predefinita dopo il timeout del timer deve essere annullata. La finestra di dialogo non deve uscire, ma l'etichetta di testo cambia per mostrare che l'azione è stata annullata. L'utente può scegliere di confermare il comando o l'annullamento.

Assicurarsi sempre che i pulsanti che eseguono operazioni critiche siano chiaramente contrassegnati. Usare sempre testo non crittografato che descriva accuratamente l'azione. Se l'azione è l'eliminazione di file, non scrivere "Rimuovi file dal repository"; scrivere "Delete Files from Repository" (Elimina file dal repository). Quando si lavora con gli elenchi di file, se un comando di menu Elimina elimina i file selezionati dal disco rigido stesso (anziché essere rimossi solo dall'elenco di file), è necessario sottolineare correttamente la natura critica di questa operazione e sottolineare in modo esplicito che l'azione eliminerà definitivamente i file.

Una volta qualcuno ha detto: "You are as good as your worst work". Lo stesso vale per le applicazioni software. Una singola esperienza negativa con l'app può dare un'impressione negativa all'utente. Per assicurarsi che ciò non accada, è possibile assicurarsi che, in caso di arresto anomalo dell'applicazione, l'applicazione si arresti normalmente. Se è possibile aggiungere il ripristino dei dati o consentire all'utente di provare a salvare una copia di questi dati, può essere un grande vantaggio. L'utente deve ricevere una notifica corretta in caso di arresto anomalo dell'applicazione. Un JIT-Debugger o un dialogo di errore critico non è una buona cosa. Anche se parlare di come gestire gli arresti anomali va oltre l'ambito di questo articolo, è consigliabile che un dialogo semplice che si insodssi con l'utente e ne informi la situazione (e possibilmente con un collegamento a altre informazioni su come eseguire il ripristino da questo arresto anomalo) sia molto utile per l'utente.

Se si vuole fare un ulteriore passo avanti, è possibile fare ciò che fa una delle applicazioni di progettazione grafica preferite. Se si arresta in modo anomalo, verrà visualizzata una finestra di dialogo di ripristino che consente di salvare una copia separata del file su cui si sta lavorando e quindi di fornire una finestra di dialogo di feedback in cui è possibile immettere le informazioni sull'arresto anomalo (informazioni personali facoltative, naturalmente) e inviarle agli autori.

### <a name="radiobuttons-or-comboboxes"></a>Pulsanti di opzione o caselle combinate?

A prima vista, il metodo per effettuare una selezione uno-a-molti non sembra così difficile o importante. In alcuni casi può essere, soprattutto se lo scenario è un'applicazione usata per il lavoro a tempo.

Di seguito viene illustrato un esempio reale. Microsoft ha rilasciato di recente una versione di anteprima di un'applicazione grafica, Expression Graphics Designer (in precedenza denominata "Acrilico"). Ho avuto circa 20 oggetti grafici a cui ho dovuto assegnare una determinata proprietà separatamente in questa applicazione. Si tratta di un processo ineffiato. A tale scopo, è stato necessario selezionare l'oggetto, fare clic sul pulsante per visualizzare la finestra delle impostazioni e impostare le opzioni. In una di queste opzioni è stato necessario selezionare due opzioni da un controllo ComboBox, come si può vedere nello screenshot seguente.

![Screenshot della finestra di dialogo texture per la finestra di progettazione grafica delle espressioni.](images/humanux-09.png)

Quando devi selezionare il secondo elemento (su un solo 2 elementi) nell'elenco a discesa ComboBox, può essere davvero difficile. Ciò che in genere non ci si rende conto è il tempo necessario per la visualizzazione dell'elenco a discesa. Può sprecare molto tempo e può essere frustrante. Questo problema può essere risolto facilmente inserendo un controllo GroupBox con due pulsanti di opzione, soprattutto quando lo spazio disponibile è così grande. Si sono verificati problemi simili in applicazioni come CorelDRAW, Microsoft Access e altre.

Oltre a sprecare tempo a causa dell'animazione a discesa, si spreca anche la "larghezza di banda psichiche". Con due pulsanti di opzione "sempre visibili", la nostra mente conosce in modo subliminale la posizione in cui il cursore deve fare clic. Con comboBox verrà elaborato solo dopo che l'elenco è stato disegnato. Anche se può sembrare troppo poco importante, in realtà è molto importante.

A volte è meglio usare i pulsanti di opzione, soprattutto se sono disponibili 4 opzioni o meno.

### <a name="never-disrupt-the-user"></a>Non interrompere mai l'utente.

A meno di mettere una mitragliatrice alla testa, questa è la cosa più distruttiva che uno sviluppatore può fare agli utenti. Quando l'applicazione, inutilmente o in altro modo, interrompe l'utente mentre sta lavorando a un'altra applicazione con una finestra di messaggio o un flash della barra delle applicazioni, si ottengono punti negativi dall'utente.

I flash della barra delle applicazioni possono essere utili, naturalmente, ma devono essere chiamati solo quando il processo dell'applicazione richiede l'input dell'utente per continuare o se si ha qualcosa di fondamentale da trasmettere all'utente. Se l'utente ha mantenuto la barra delle applicazioni in Nascondi automaticamente, un pulsante della barra delle applicazioni lampeggiante può impedirlo di accedere alla barra di stato o ad altri controlli a basso ancoraggio perché la barra delle applicazioni si nasconderebbe di nuovo finché l'utente non ha fatto clic sul pulsante lampeggiante.

![Screenshot di una finestra di tipo avviso popup.](images/humanux-10.png)

Le finestre "Toast" (vedere la figura 10), rese famosi dai client di messaggistica immediata come MSN Messenger, sono un'ottima soluzione per informare l'utente di qualcosa senza disturbare o interrompere il flusso di lavoro. C'è un ottimo articolo ( https://docs.microsoft.com/archive/msdn-magazine/2005/september/sprinkle-some-pizzazz-on-your-plain-vanilla-windows-forms-apps) di Bill Toast sulla creazione di finestre toast. È buona policy (e modi) non disturbare gli avvisi popup di altre applicazioni. L'ostruzione di tali finestre può essere fastidiosa e improduttiva. Una soluzione consiste nell'usare il mutex ToastSemaphore (/library/WinMessenger/winmessenger/overview/toast.asp) fornito dal sistema operativo per evitare conflitti di tipo avviso popup.

A volte potrebbe essere necessario visualizzare più elementi tramite l'avviso popup. Non è consigliabile visualizzare 3 o più avvisi popup. Al contrario, è meglio eseguire il ciclo tra ognuno selezionando/dissolvendo un avviso popup dopo l'altro. Microsoft Outlook una soluzione simile quando invia una notifica all'utente di messaggi di posta elettronica in arrivo.

### <a name="provide-progress-status"></a>Fornire lo stato di avanzamento

Spesso sono presenti attività che richiedono all'utente di attendere. Naturalmente, questa è una delle cose che l'utente non può fare. Ma la cosa peggiore è quando sono in attesa senza sapere cosa accade. In alcuni casi l'applicazione potrebbe dover connettersi a un servizio Web o a un computer remoto o forse sta elaborando grandi blocchi di dati, indipendentemente dal motivo per cui l'utente deve essere a conoscenza o almeno vagamente consapevole di ciò che accade sotto il cofano. Esistono diversi metodi per eseguire questa operazione, in base alla situazione.

Se ci si connette a un oggetto lontano, ad esempio un servizio Web o un elemento inserito in una rete o in un server Internet, è consigliabile visualizzare una semplice finestra di dialogo di stato (vedere l'immagine seguente) o un indicatore di stato ospitato nella barra di stato. Un'etichetta che accompagna deve descrivere lo stato corrente del processo. Ad esempio, se ci si connette a un servizio Web per elaborare alcuni dati, pronunciare semplicemente "Connessione al servizio Web... " o "Attendere, elaborare... " Se questo processo è sincrono, è consigliabile disabilitare tutti i controlli a cui l'utente può accedere fino al completamento del processo oppure visualizzare semplicemente lo stato di avanzamento come finestra di dialogo modale.

![Screenshot di una finestra di dialogo dell'indicatore di stato.](images/humanux-11.png)

Se si usa un indicatore di stato e il tempo di elaborazione è sconosciuto o se non si ha un valore massimo, è consigliabile impostare l'indicatore di stato stile sulla modalità selezione.

Un altro metodo che sta diventando popolare è una finestra "avviso popup" fissa che visualizza lo stato di avanzamento. Microsoft AntiSpyware downloader/updater o gli avvisi popup di analisi tramite posta elettronica di Norton AntiVirus sono esempi di questo tipo. Naturalmente, questa opzione deve essere usata solo per i processi asincroni. In caso contrario, l'utente potrebbe essere sconcertato. Queste finestre sono più usate per l'elaborazione in background, ad esempio il download di un aggiornamento o l'esecuzione di un'attività pianificata, e non devono mai essere impostate su "Always on top".

### <a name="simplify-complex-steps-with-wizards"></a>Semplificare i passaggi complessi con le procedure guidate

È possibile presupporre che, di fronte a una grande gamma di controlli in un singolo form, un utente tipico verrà confuso senza fine. In alcuni casi, nessuna quantità di raggruppamento, ridimensionamento o spaziatura può essere utile quando si hanno molti controlli importanti.

Una procedura guidata è la soluzione migliore per questi scenari. È possibile dividere i controlli per attività o categorie in base alle specifiche condizioni e posizionarli in passaggi separati. In questo modo l'utente può rimanere concentrato e non essere insoddziato dall'attività. È possibile fornire una Guida specifica per un passaggio o un'attività con un pulsante ? Le linee guida per la creazione guidata sono presenti in MSDN Library.

Le procedure guidate sono anche un buon modo per configurare la configurazione iniziale dell'applicazione. Molte applicazioni usano questa procedura guidata per configurare la configurazione personalizzata subito dopo il completamento dell'installazione o al primo utilizzo. Una procedura guidata iniziale di questo tipo deve essere resa facoltativa, se possibile. Se l'utente annulla in qualsiasi momento, le impostazioni non specificata passano ai valori predefiniti. Se è possibile rendere la procedura guidata un po' grafica (vedere la sezione Usare [Pretty Graphics),](#use-pretty-graphics) l'attività di configurazione risulta molto più semplice.

### <a name="get-the-tone-of-your-text-right"></a>Ottenere il tono del testo a destra

Nella sezione [Windows di interazione dell'esperienza](/windows/apps/desktop/)utente è stato fatto un punto molto importante su "Tono di testo". Si tratta dell'impressione e del senso del testo nell'applicazione. Può trattarsi di qualsiasi elemento, da una semplice descrizione comando a un controllo etichetta istruzione.

In precedenza è stata illustrata la modifica del testo nell'opzione Webcam in MSN Messenger. Questo è detto tono di testo appropriato. Quando si gestiscono utenti non tecnici o principianti, l'invio del messaggio assume un aspetto diverso.

Se si scrive "Percorso di destinazione" sopra una casella di testo in un'applicazione autoestraendo, un utente tecnico può facilmente sapere che si immette qualcosa come "C: \\ Temp \\ MyPath". Un utente non esperto (si pensi a "Mom") può facilmente essere sconcertato e dovrebbe fare riferimento al manuale, chiamare il supporto tecnico o, in caso contrario, rinunciare. Un'alternativa valida consiste nel specificare le operazioni che l'utente deve eseguire: "Selezionare la cartella in cui si desidera inserire questi file". È anche possibile rinominare "Sfoglia... " accanto a tale casella di testo per selezionare "Seleziona cartella" "

Fornendo una descrizione chiara di ciò che si vuole che l'utente faccia, si ridurre anche la necessità di file della Guida o almeno di ridurre i dettagli da includere nei file della Guida.

Un suggerimento molto valido dalle linee guida per l'interazione [Windows'esperienza utente si](/windows/apps/desktop/) applica a qualsiasi software. Indica che il writer deve mantenere il testo conversazionale. Le linee guida definiscono questa impostazione come "Evitare parole che non si direbbe a un altro utente di persona".

Alcuni suggerimenti per la scrittura di testo:

-   Evitare di parlare dell'utente in terza persona. Pronunciare "You" anziché "The user".
-   Quando possibile, usare con giudizio "My name:" o "My E-Mail address:" anziché "Name:" o "E-Mail:"
-   Quando si danno più opzioni, scrivere il testo dal punto di vista dell'utente. Ad esempio, se sono disponibili due pulsanti di opzione sotto un'etichetta, ad esempio "Selezionare l'autorizzazione per Nome utente in questa rete" sopra due pulsanti di opzione, ad esempio "Consenti" e "Nega", sostituire il testo di RadioButton con \[ \] "I want to allow Username" e \[ \] "I want to disallow \[ \] Username".
-   Sottolinea il testo solo se viene usato per i collegamenti. Confonde l'utente se il testo sottolineato non è un collegamento.
-   Prestare attenzione alle informazioni importanti con un'etichetta in grassetto, ma usarle con attenzione. Troppo testo in grassetto crea confusione e riduce l'impatto complessivo del modulo.
-   Quando si scrive il testo per una casella di controllo, assicurarsi che sia facile sapere cosa accade quando viene selezionata e quando viene deselezionata o deselezionata. L'opzione consigliata è scrivere il testo direttamente come risultato della selezione della casella di controllo. Ad esempio, scrivere "Inviami informazioni utili dai partner" anziché "Non inviare informazioni utili dai partner". Anche se posso immaginare molte persone di marketing che discutono di questo particolare esempio, sono certo che tu sappia cosa voglio dire.
-   Se si dispone di un controllo simile a un pulsante (in genere un controllo RadioButton con un aspetto pulsante di comando) che controlla Abilitato/Disabilitato, assicurarsi di etichettarlo correttamente. Se il processo è abilitato, scrivere "Enabled" anziché "Enable" o "Disable". Se si scrive Abilitato, viene visualizzato lo stato corrente. Se si fa clic sul pulsante (abilitato) e il pulsante indica "Abilita", può generare confusione e problemi. "Abilita" potrebbe richiedere all'utente di fare clic su di esso in modo che il processo non sia attivo.

### <a name="sometimes-a-listview-is-better"></a>A volte un controllo ListView è migliore

Spesso si usa DataGrid o ListBox o anche ComboBox per le attività di selezione, ma con Windows XP e versioni successive di Windows, l'uso di listView può offrire opzioni più grandi.

Punti finali del controllo ListView:

-   Accelera il riconoscimento degli elementi con icone e bitmap.
-   Visualizza informazioni aggiuntive con le visualizzazioni Dettagli o Riquadro.
-   Con Visual Studio 2005, è anche possibile avere gruppi per la categorizzazione aggiuntiva. I gruppi si estendono su tutte le viste e sono flessibili. I gruppi possono essere usati anche per appiattire una visualizzazione gerarchia,ad esempio TreeView, in cui sono presenti più nodi figlio rispetto ai nodi padre. Un buon esempio è la finestra di dialogo Connessioni di rete in Windows XP, quando viene visualizzata con "Mostra in gruppi" e la visualizzazione impostata su Dettagli.
-   Per personalizzare un controllo ListView, disegnarlo manualmente impostando la **proprietà OwnerDraw** e usando gli eventi **DrawItem** **e DrawSubItem.**
-   Supporta la modifica rapida sul posto degli elementi listView.
-   Supporta facilmente il riordinamento manuale.
-   Consente agli utenti di selezionare la visualizzazione (icone grandi, icone piccole, elenco e così via) con cui sono più a loro agio.

### <a name="simplify-navigation-with-breadcrumb-controls-and-sidebars"></a>Semplificare la navigazione con controlli breadcrumb e barre laterali

La "navigazione secondaria" è la chiave per un'interfaccia utente complessa. A volte non è possibile evitare di avere un'interfaccia utente complessa. La cosa migliore da fare in una situazione di questo tipo è rendere l'esperienza il più semplice possibile per l'utente. Una barra laterale costituita da etichette di collegamento o un controllo TreeView per lo spostamento basato sulla gerarchia suggerisce uno spostamento a livello di pari livello per l'attività della finestra di dialogo corrente. Rende molto semplice per l'utente passare da un passaggio all'altro del processo sapendo dove si trova.

Se si passa a una navigazione basata su gerarchia con TreeViews o altri elementi di spostamento analogamente complessi, una buona utilità per l'utente è un controllo breadcrumb. Sebbene Visual Studio non sia ancora disponibile con un controllo incorporato, vedere Creazione di un controllo [breadcrumb](/archive/msdn-magazine/2005/july/advanced-basics-creating-a-breadcrumb-control) per informazioni sulla creazione di un controllo personalizzato. Un controllo di navigazione semplifica l'individuazione della posizione corrente in relazione alla gerarchia.

È possibile eseguire facilmente il merge della navigazione nell'intestazione se il form ne ha uno. Vedere la sezione precedente sulle [intestazioni](#simplify-recognition-with-headers).

### <a name="use-pretty-graphics"></a>Usare pretty graphics

Tutti gli utenti si disdezzano delle applicazioni con una grafica interessante, almeno la maggior parte. Anche se un'interfaccia utente con una grafica ben strutturata non è una scelta logica per tutte le applicazioni, è utile per dare un'impressione e può essere difficile lavorare. Naturalmente, la grafica non deve ostacolare la produttività, ma se usata correttamente può aumentarla.

Non è necessario che siano presenti molte immagini, né richiedono necessariamente molto lavoro. Una schermata iniziale o un'intestazione progettata professionalmente (come quella di cui si è parlato in precedenza) esegue il trick. Se il budget lo consente, è possibile usare grafica ben progettata per barre degli strumenti, procedure guidate e altro ancora. Rendono l'app un aspetto piuttosto semplice e anche più professionale. Si tratta di un effetto sottile, ma un aspetto professionale trasmette fiducia e stabilità. Se si è un'azienda relativamente piccola che crea applicazioni per la vendita al dettaglio, questo è un aspetto fondamentale da considerare.

È sempre importante usare grafica progettata professionalmente. La grafica senza diritti è facilmente disponibile e conveniente. È anche possibile assumere un progettista. Tuttavia, se la grafica non è forte, non provare a farlo da soli. Se non è possibile acquisire o usare grafica progettata professionalmente, è meglio non usarle affatto.

Per la grafica di piccole dimensioni, è sempre possibile scegliere le icone e le bitmap disponibili con Visual Studio 2005. La grafica fornita con le versioni precedenti non è consigliata.

### <a name="provide-resizable-forms-when-possible"></a>Fornire moduli ridimensionabili quando possibile

Le finestre ridimensionabili sono simili alle finestre indipendenti dalla risoluzione. Le finestre indipendenti dalla risoluzione hanno lo stesso aspetto indipendentemente dal fatto che si usino schermate 96DPI o 300DPI. Indipendentemente dal fatto che l'interfaccia utente dell'applicazione sia indipendente dalla risoluzione, è più utile se è ridimensionabile. Naturalmente, questo non si applica a molti scenari, ma è una buona regola per utilizzo generico.

Se la finestra gestisce elenchi di qualsiasi tipo, in particolare ListView, questo diventa ancora più importante. Il ridimensionamento consente all'utente di esaminare più dati contemporaneamente.

Ad esempio, si ha un'applicazione in cui l'utente deve selezionare un'immagine da una raccolta di grandi dimensioni. La finestra di dialogo aperta consente di selezionare una visualizzazione anteprima, ma la finestra di dialogo ha dimensioni fisse e l'elenco di anteprime mostra solo 4 anteprime alla volta. Se la raccolta include centinaia di immagini, lo scorrimento e l'aspetto, un'attività ripetitiva, possono essere piuttosto noiosi e ridurre l'efficienza. Se la finestra di dialogo è ridimensionabile, l'utente può renderla grande quanto è comoda o almeno grande quanto lo schermo consentirebbe ed essere in grado di completare rapidamente l'attività. Se l'elenco ha uno scorrimento orizzontale, ad esempio un controllo ListView o DataGrid dettagliato, è ancora più faticoso. Le finestre ridimensionabili sono molto utili in una situazione di questo tipo.

### <a name="provide-more-functionality-with-sidebarstask-panes"></a>Fornire altre funzionalità con barre laterali/riquadri attività

Analogamente alle intestazioni di cui si è parlato in precedenza, le barre laterali e i riquadri attività sono un modo straordinario per fornire funzionalità aggiuntive e comandi di utilità. Ad esempio, i riquadri attività Office Word 2003 sono molto pratici, accessibili e non intrusivi. Funzionano anche in modo asincrono durante la connessione alle risorse online, offrendo all'utente la possibilità di eseguire più attività.

La creazione di un riquadro attività o di una barra laterale è semplice quanto la creazione di un pannello di ancoraggio, con la possibilità di inserire un elemento grafico a forma di slick nella parte superiore per fungere da barra del titolo. È anche possibile usare un controllo Etichetta colorato. Le opportunità per i riquadri attività sono molte.

Se si dispone di funzionalità aggiuntive e si vuole fornirla in modo non intrusivo all'utente, non c'è alcuna posizione come il riquadro attività. È anche possibile rendere i riquadri attività "Nascondi automaticamente" o comprimersi come le finestre Visual Studio strumenti.

### <a name="give-a-notification-choice"></a>Scegliere una notifica

In precedenza è stato illustrato come creare una finestra di messaggio personalizzata. Se una finestra di messaggio nell'applicazione verrà visualizzata spesso all'utente, può essere utile aggiungere una casella di controllo che l'utente può selezionare per disabilitare la finestra di dialogo in futuro. Questa opzione è particolarmente utile per i messaggi più ovvi.

Un esempio familiare è la finestra di Visual Studio trova. Quando si cerca o si sostituisce testo, Visual Studio viene visualizzata una finestra di messaggio che indica i risultati. Ma è anche possibile disabilitare la finestra di messaggio. Può essere davvero fastidioso premere INVIO o fare clic su OK ogni volta che si cerca.

Un altro aspetto interessante Visual Studio è che, anche se la finestra di dialogo è disabilitata, visualizza comunque i risultati di tale operazione nella barra di stato.

### <a name="provide-tooltips"></a>Specificare le descrizioni comando.

In alcuni casi le descrizioni comando possono risparmiare molto tempo. Pulsanti, caselle di controllo e altri controlli possono essere ambigui e l'utente potrebbe non essere sicuro di cosa fare. Le descrizioni comando offrono la forma migliore della Guida sensibile al contesto in una sola riga. L'utente può decidere rapidamente cosa fare senza cercare nulla nel file della Guida o aprire un'altra finestra.

Gli utenti spesso ignorano questo problema nelle proprie applicazioni. Fare in modo che punti ad aggiungere descrizioni comando a tutti i controlli ambigui o a TUTTI i controlli, se possibile. Non ripetere il testo di un'etichetta o del testo del controllo associato, ma fornire informazioni aggiuntive su tale controllo. Il testo deve spiegare la funzione del controllo in poche parole.

### <a name="do-not-forget-the-little-things"></a>Non dimenticare le piccole cose

Le piccole cose possono infastidire l'utente, ma ignorarle può influire sull'impressione che si crea. Una volta ho usato un'applicazione effettuata da una persona importante nel settore del software che aveva borderStyle del modulo impostato su Sizeable, ma i controlli sul lato destro del form non erano ancorati. Per questo, l'applicazione creata da un settore pesante aveva un aspetto non professionale.

Questi tipi di "piccole cose" sono alla base dell'impressione complessiva. L'interfaccia utente e l'esperienza utente dell'applicazione sono gli elementi su cui gli utenti giudiranno l'applicazione, almeno all'inizio. Se vengono visualizzati bug ovvi nell'interfaccia utente, è possibile che percepiranno l'applicazione come meno potente ed efficace.

## <a name="conclusion"></a>Conclusione

È stata trattata solo una piccola parte dell'esperienza utente umana. Quando l'esperienza utente diventa più semplice, efficace, divertente e più semplice da usare, l'attività di creazione di tale esperienza utente diventa molto più complessa. Tuttavia, con una certa previsione e una buona pianificazione, è possibile creare un'esperienza utente ottimale.

Il modo migliore per creare un'esperienza utente perfetta è eseguire test di usabilità destinati soprattutto all'interfaccia utente, sia con un gruppo di test speciale che con l'utente stesso. Maggiore è il tempo necessario per testare l'esperienza utente prima di rilasciare l'applicazione, meglio è. Questa operazione consente di risparmiare molti problemi in un secondo momento.

 

 