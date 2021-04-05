---
title: Principi dell'interfaccia utente
description: In questo argomento viene illustrato come implementare i principi di progettazione intuitiva dell'interfaccia utente e dell'esperienza utente in un'applicazione Windows.
ms.assetid: 603bc184-3eec-4281-8caa-993834da3131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98383f9379248570ef8b254c647ab8348d703696
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047116"
---
# <a name="user-interface-principles"></a>Principi dell'interfaccia utente

In questo argomento viene illustrato come implementare i principi di progettazione intuitiva dell'interfaccia utente e dell'esperienza utente in un'applicazione Windows.

-   [Introduzione](#introduction)
-   [Principi di base dell'interfaccia utente corretta](#the-basic-principles-of-proper-ui)
    -   [Spaziatura e posizionamento](#spacing-and-positioning)
    -   [Dimensioni](#size)
    -   [Raggruppamento](#grouping)
    -   [Intuitività](#intuitiveness)
-   [20 suggerimenti per una migliore esperienza utente funzionale](#20-tips-for-a-better-functional-user-experience)
    -   [USA standard](#use-standards)
    -   [Attirare l'attenzione sui pulsanti importanti](#draw-attention-to-important-buttons)
    -   [Semplificare il riconoscimento con le icone](#simplify-recognition-with-icons)
    -   [Semplificare il riconoscimento con le intestazioni](#simplify-recognition-with-headers)
    -   [Usare le finestre di messaggio personalizzate](#use-custom-message-boxes)
    -   [Includi comandi alternativi](#include-alternate-commands)
    -   [Come gestire le azioni critiche](#how-to-handle-critical-actions)
    -   [Pulsanti o ComboBox?](#radiobuttons-or-comboboxes)
    -   [Non Interrompi mai l'utente.](#never-disrupt-the-user)
    -   [Fornire lo stato di avanzamento](#provide-progress-status)
    -   [Semplificare i passaggi complessi con le procedure guidate](#simplify-complex-steps-with-wizards)
    -   [Ottenere il tono del testo a destra](#get-the-tone-of-your-text-right)
    -   [A volte un controllo ListView è migliore](#sometimes-a-listview-is-better)
    -   [Semplificare la navigazione con controlli di navigazione e barre laterali](#simplify-navigation-with-breadcrumb-controls-and-sidebars)
    -   [Usa grafica piuttosto semplice](#use-pretty-graphics)
    -   [Fornire moduli ridimensionabili quando possibile](#provide-resizable-forms-when-possible)
    -   [Offrire più funzionalità con i riquadri Sidebar/attività](#provide-more-functionality-with-sidebarstask-panes)
    -   [Concedi una scelta di notifica](#give-a-notification-choice)
    -   [Fornire descrizioni comandi.](#provide-tooltips)
    -   [Non dimenticare le piccole cose](#do-not-forget-the-little-things)
-   [Conclusione](#conclusion)

## <a name="introduction"></a>Introduzione

Gli sviluppatori spesso non riescono a prendere in considerazione il punto di vista dell'utente finale. Gli sviluppatori lavorano duramente per far funzionare l'applicazione, ovvero i clienti si aspettano di lavorare e la loro percezione del software si basa su questo requisito. Ciò vale soprattutto se si sviluppa software per la vendita al dettaglio o un elemento che verrà usato da persone non tecniche. Gli sviluppatori devono essere a conoscenza delle esigenze dell'utente finale nell'intero processo di progettazione del software.

Un'applicazione software deve essere facile da esplorare e usare come possibile. Con la quantità di software da creare, un numero stimato di 4 applicazioni software dispone di un'interfaccia utente molto straordinaria che l'utente finale ama effettivamente e che è immediatamente comodo utilizzando.

Per le aziende viene creata una grande quantità di software per uso interno. Che siano sviluppate internamente o sotto la cura di un consulente, spesso un minimo di tempo, fatica o denaro viene investito nella creazione di un'interfaccia utente migliore. Il ruolo "designer" è raro nel ciclo di sviluppo, soprattutto nel mondo delle applicazioni Windows.

Ci sono alcune regole di base da seguire per avere un'interfaccia utente più gradevole e funzionante per l'applicazione. Non richiede una quantità eccessiva di tempo o denaro da parte dell'utente e aggiunge un valido ritorno sugli investimenti.

Prima di procedere, possiamo distinguere tra l'interfaccia utente e l'esperienza utente, almeno per quanto riguarda l'ambito di questo articolo. L'interfaccia utente (UI) si riferisce agli oggetti visivi e ai controlli dell'applicazione, mentre l'esperienza utente, o UX, include sia l'interfaccia utente che il comportamento dell'applicazione correlata all'interfaccia utente, oltre alla "sensazione" che l'utente ottiene dall'app. Non si tratta solo di progettare un'interfaccia utente molto interessante, ma anche di assicurarsi che funzioni benissimo.

In questo articolo verranno discussi 20 punti di progettazione di UX che è possibile integrare facilmente nella fase di progettazione dell'applicazione. Il risultato è costituito da applicazioni più avanzate con funzionalità più intuitive, una "UX umana". Poiché tutti sanno che la generazione di applicazioni Windows Vista dovrà avere un aspetto e un comportamento diverso. Questo argomento consente di prepararsi per le applicazioni future, offrendo al contempo agli utenti correnti un buon gusto del futuro.

Le sezioni seguenti illustrano le nozioni di base della progettazione corretta dell'interfaccia utente.

## <a name="the-basic-principles-of-proper-ui"></a>Principi di base dell'interfaccia utente corretta

Un UX professionale che sta cercando dipende da questi quattro fattori:

-   Spaziatura e posizionamento
-   Dimensione
-   Raggruppamento
-   Intuitività

Con le versioni di Microsoft Visual Studio precedenti alla 8,0, la spaziatura e il ridimensionamento non erano ottimali. Una griglia 4x4 o 8x8 Virtual non è sempre funzionante. Con l'inclusione delle guide di allineamento, il processo è stato semplificato. L'allineamento di un'etichetta a una casella di testo o ancora peggio, l'allineamento di più etichette con le caselle di testo corrispondenti è estremamente difficile nelle versioni precedenti di Visual Studio. Le guide di allineamento hanno semplificato significativamente questo processo.

Le sezioni seguenti descrivono quattro degli aspetti più importanti della progettazione di UX professionali.

### <a name="spacing-and-positioning"></a>Spaziatura e posizionamento

La spaziatura tra due controlli è importante. Lo screenshot seguente illustra un modulo di immissione di **informazioni utente** non corretto: le prime due caselle di testo sono troppo chiuse, l'elenco sottostante è troppo lontano ed è presente una grande quantità di spazio inutilizzato nel form.

![Screenshot di un modulo progettato in modo non corretto.](images/humanux-01.png)

Nello screenshot seguente è possibile visualizzare una finestra di dialogo più professionale con la spaziatura corretta e i controlli con dimensioni appropriate. Si tratta dello stesso formato dello screenshot precedente, ma è stato modificato per utilizzare la spaziatura consigliata dalle guide di allineamento. È sempre consigliabile allineare un'etichetta con la linea di base del testo della casella di testo o di un altro controllo accanto, anziché il bordo inferiore effettivo del controllo. Le guide di allineamento diventano un colore diverso quando viene raggiunto l'allineamento, in genere solo pochi pixel sopra il bordo inferiore.

![Screenshot di un modulo più ben progettato.](images/humanux-02.png)

Sebbene non esistano regole esatte per la spaziatura, le guide di allineamento forniscono linee guida estremamente utili per la spaziatura corretta. Altri strumenti che consentono di gestire la spaziatura corretta sono i controlli di layout nel gruppo della casella degli strumenti contenitori. TableLayoutPanel è inoltre molto utile per la creazione di finestre di dialogo di stile del form di immissione.

### <a name="size"></a>Dimensione

Le stesse considerazioni si applicano alle dimensioni. Quando si trascina un pulsante dalla casella degli strumenti nel form, l'altezza e la larghezza sono perfette. La larghezza massima consigliata (a esclusione di eventuali motivi gravi) consiste nel raddoppiare la larghezza originale.

Se si osserva la finestra **Esegui** nel menu **Start** o la finestra di dialogo delle **Proprietà** di qualsiasi oggetto di Esplora risorse, le dimensioni dei pulsanti sono "Just Right". Se si dispone di una funzione molto importante che l'utente finale deve notare senza esito negativo, sono disponibili altri metodi rispetto all'uso di un pulsante grande o di colori non standard vistosi (altre informazioni in seguito).

Nell'immagine seguente è possibile visualizzare tre pulsanti. Il primo pulsante è la dimensione più consigliata e corrisponde alla dimensione creata per impostazione predefinita quando viene trascinato (o fatto doppio clic) dalla casella degli strumenti. A volte il testo aggiuntivo richiede che il pulsante sia più grande. Il secondo pulsante Mostra una dimensione grande ma accettabile. Non creerebbe un disordine per la definizione di altri controlli. Il terzo pulsante, tuttavia, è una dimensione completamente inaccettabile. Si noterà che le bitmap del tema utilizzate da Windows per creare controlli con temi possono anche essere leggermente distorte. Inoltre, sarà difficile allineare gli altri controlli in modo intuitivo.

![immagine di tre pulsanti, che aumentano di dimensione da sinistra a destra.](images/humanux-03.png)

### <a name="grouping"></a>Raggruppamento

In genere, un'applicazione contiene molti controlli. Solo in base a un raggruppamento intuitivo, è possibile rendere più semplice l'uso di tutti questi controlli. Il raggruppamento in base alla funzione o in categorie viene eseguito in modo ottimale per i controlli struttura a schede. Ad esempio,' Accounts,'' Reports,'' Employees,' and ' Projects ' sarebbero candidati perfetti per le schede in una tipica applicazione aziendale. Raggruppamento di pari livello: i controlli che contribuiscono allo stesso risultato finale vengono eseguiti meglio da controlli gruppo. Non è consigliabile usare pannelli con bordi per tale raggruppamento. I controlli gruppo salvano il peso aggiuntivo di un controllo etichetta, soprattutto se i controlli secondari sono autoesplicativi.

I controlli gruppo all'interno dei controlli gruppo non sono consigliati a meno che non siano presenti più di 2 o 3 di essi all'interno di un controllo gruppo di grandi dimensioni.

### <a name="intuitiveness"></a>Intuitività

Questo è l'aspetto più importante di un'esperienza utente eccezionale. Un UX intuitivo riduce la necessità di spiegazioni. L'utente conosce semplicemente i controlli.

Un argomento importante nella progettazione intuitiva è la codifica a colori. Un valido esempio viene presentato in Windows XP che presenta nuovi pulsanti di tipo soft-Square per funzioni quali la navigazione nelle applicazioni con tema, le finestre di dialogo **Disconnetti** e **Disattiva computer** e altre ancora.

La colorazione di questi controlli è stata determinata in base alla gravità del risultato del push di tale pulsante. La navigazione è verde, molto simile a un semaforo "go". L'arresto, che comporterebbe una potenziale perdita di lavoro, è colorato in rosso come un segno di avviso. I pulsanti semi-critici, come la disconnessione o l'ibernazione, sono gialli. I pulsanti neutri che non hanno alcun effetto critico sui processi di lavoro dell'utente, ad esempio la guida, sono un blu Soft. Quando si crea un'interfaccia utente con skin, questi aspetti di colore devono essere tenuti in considerazione.

Un esempio molto valido di riconoscimento del contenuto per colore è Microsoft Office OneNote. Le schede dell'applicazione possono essere impostate su colori diversi pur continuando a sembrare essenzialmente una parte appropriata della progettazione complessiva di Windows XP.

Un altro aspetto importante è il testo nelle applicazioni. Di recente sono stati apportati diversi sforzi per semplificare la lingua utilizzata per le istruzioni scritte nel software Windows. L'utilizzo del testo all'interno del software verrà illustrato più avanti, ma si noti quanto segue.

MSN Messenger aveva una casella di controllo nella finestra di dialogo **Opzioni** contrassegnata come "condividere le funzionalità di webcam". Gli sviluppatori e gli addetti alla tecnologia possono sapere cosa significa, ma un utente con il novizio potrebbe pensare che è possibile consentire a un altro utente all'altra estremità della chat di usare anche la Web Cam. In una versione recente è stato modificato in "My Webcam: Consenti ad altri utenti di vedere che ho una webcam". Questo è perfetto per i destinatari che potrebbero non avere conoscenze tecniche e vengono usati per il linguaggio semplice.

Sebbene il linguaggio più semplice ne semplifica la comprensione, c'è anche un ulteriore vantaggio. Gli studi scientifici mostrano che la nostra idea è più semplice con un linguaggio più semplice quando si prova a comprendere qualcosa di nuovo. Spesso, il cervello elabora parole come ' it,'' per,'',' e altre parole comuni così rapidamente e con facilità, che viene allocata una maggiore larghezza di banda per comprendere le parole che si distinguono, come ' Webcam ' o ' others ', nell'esempio precedente.

I titoli di MessageBox, le didascalie e altri blocchi di testo semplificano la trasmissione della funzione di un gruppo di controlli all'utente finale con solo poche parole.

L'intuitività è nata anche da una certa familiarità. Ad esempio, la posizione dei pulsanti **OK** e **Annulla** è così uniforme e ben posizionata nel pensiero che se una finestra di dialogo include questi pulsanti in una sequenza inversa (**Annulla**, quindi **OK**, anziché **OK**, quindi **Annulla**), è possibile che venga invece raggiunto l' **annullamento** . Dopo aver usato un particolare standard per eseguire le operazioni, ad esempio le applicazioni basate su Windows, per più di un anno, le abitudini si sviluppano. Gli standard di settore seguenti, ma non stati, possono essere più facili da usare.

In una delle prime build di anteprima di Windows Vista, i pulsanti **Riduci a icona**, **Ingrandisci** e **Chiudi** di qualsiasi finestra sono diventati diversi. Nelle versioni precedenti di Windows, soprattutto quando si utilizza un singolo monitor, si sviluppa un'abitudine nello scorrere il cursore nell'angolo superiore destro dello schermo e fare clic su. Questa operazione ha sempre causato la chiusura della finestra. Ora, in questa particolare build di Windows Vista, c'era circa 8 pixel di spazio tra il pulsante Chiudi e il bordo destro della finestra. Lo spazio aggiuntivo ha reso l'aspetto interessante (ed era probabilmente necessario per l'animazione a freddo bagliore del pulsante), ma era irritante perché non consentiva agli utenti di chiudere le finestre aperte con facilità. Il ricondizionamento della mente può essere difficile. Fortunatamente, nella compilazione seguente questo problema è stato risolto. A questo punto, rimane spazio tra il bordo della finestra e il pulsante Chiudi, ma facendo clic su tale spazio viene anche chiusa la finestra.

Un fattore molto importante della progettazione intuitiva è la quantità di "bandwidth'mentale", ovvero l'intervallo di tempo in cui può essere utile comprendere qualcosa, che usa. Minore è l'utilizzo della larghezza di banda, migliore sarà l'esperienza utente.

Si tratta di piccoli elementi che contribuiscono alla "esperienza" dell'uso di un'applicazione software. Gli esempi seguenti forniscono suggerimenti per migliorare le applicazioni con suggerimenti e consigli reali.

## <a name="20-tips-for-a-better-functional-user-experience"></a>20 suggerimenti per una migliore esperienza utente funzionale

L'obiettivo di un'esperienza utente migliore consiste nel disporre di un'interfaccia utente più semplice, semplice e funzionale che risulti anche corretta. Questi suggerimenti consentono di definire l'interfaccia utente in modo più efficace.

### <a name="use-standards"></a>USA standard

Gli standard stabiliti di qualsiasi ambiente software, sia a livello di sistema operativo, a livello di marchio o di applicazione, sono molto importanti. Oltre alla personalizzazione, gli standard agiscono come uno schema proverbiale nell'idea dell'utente. Quando l'utente dedica lunghi periodi di tempo a lavorare con un'applicazione software, aumenterà automaticamente la produttività a causa della crescente familiarità.

Prima di discutere gli standard, è necessario discutere esattamente di questi standard. Gli standard includono tutti gli elementi del layout dei controlli in un particolare modo nelle finestre di dialogo, ad esempio i pulsanti **OK** e **Annulla** , la forma dell'interfaccia utente, ovvero gli angoli arrotondati della parte superiore della finestra come nelle finestre di dialogo di Windows XP, gli stili delle icone, gli stili di qualsiasi altra grafica, il comportamento interattivo dell'applicazione e simili.

Se l'applicazione rientra in una nicchia specifica, potrebbe essere più adatta a seguire un diverso set di standard. Ad esempio, se l'applicazione supporta, un'applicazione o un componente aggiuntivo per, Office OneNote 2003, è consigliabile seguire gli stili dell'interfaccia utente e degli standard di interattività di Office, in particolare OneNote. Questo include l'uso delle barre dei comandi di tipo Office anziché delle barre degli strumenti standard e di altri elementi, sia visivi che comportamentali. Se l'applicazione fa parte della categoria Microsoft Visual Studio .NET, si avrà un set separato di standard. In realtà, per le applicazioni di supporto o di questo componente aggiuntivo, le aziende come Microsoft rilasciano linee guida scritte. Si noti anche che a volte i concetti grafici e di progettazione sono proprietà intellettuali protette. Controllare sempre la documentazione appropriata per assicurarsi di disporre della licenza per la creazione di tali progetti.

Un terzo esempio di standard è costituito dall'ambiente Tablet PC. Questi standard superano i limiti tra le linee guida del sistema operativo e le linee guida dell'applicazione. La [documentazione di Tablet PC SDK](/previous-versions/ms840465(v=msdn.10)) contiene alcune informazioni molto utili nell'argomento "pianificazione dell'applicazione". Diversamente dalle linee guida theOffice 2003 o Visual Studio, queste indicazioni sulla progettazione influiscono direttamente sulla modalità di interazione dell'utente con l'applicazione e su come dovrebbe comportarsi a sua volta. Se, ad esempio, nell'applicazione sono presenti finestre ancorate, la documentazione consiglia di assicurarsi che sia in grado di rilevare quando l'orientamento dello schermo viene modificato e che le finestre di ancoraggio vengano riorganizzate correttamente con orientamento verticale o orizzontale in base alle esigenze. Anche se non si sta progettando l'applicazione in modo che sia specifica per i tablet, è consigliabile seguire queste linee guida.

Con la crescita dei client intelligenti, le applicazioni stanno ora attraversando i limiti tra un hardware diverso, ovvero PC normali, Tablet PC, dispositivi mobili o ultra mobile, PC di Media Center e così via. Ogni situazione richiede un set di standard diverso (o aggiuntivo) da seguire.

Quando le applicazioni condividono gli standard a livello di sistema operativo o di applicazione, gli utenti si sentono più a casa con il software, semplificando così l'apprendimento e l'utilizzo. Questo risultato è un aumento diretto della produttività. Gli utenti vogliono essere in grado di diventare produttivi con il nuovo software nel minor tempo possibile.

### <a name="draw-attention-to-important-buttons"></a>Attirare l'attenzione sui pulsanti importanti

A volte è necessario indirizzare l'utente ai pulsanti più importanti anche quando si trovano quattro o cinque altri pulsanti. Se si prova a usare le dimensioni, il colore o il tipo di carattere, si interrompono gli standard, operazione sconsigliata. Per eseguire questa operazione, è invece possibile usare un paio di semplici trucchi.

Il primo consiste nel convertire gli altri pulsanti non critici in LinkLabels, come illustrato nella figura seguente. In questo modo, l'utente sa che questi collegamenti eseguiranno un'attività, ma la loro attenzione passerà prima al pulsante che si distingue, senza compromettere le linee guida di progettazione standard.

![immagine di tre pulsanti convertiti in linklabels.](images/humanux-04.png)

Il secondo consiste nell'inserire il pulsante critico prima nella riga, a sinistra per i layout orizzontali, come illustrato nell'immagine seguente, o in cima per i layout verticali. Si noti che questo può variare a seconda delle impostazioni cultura dell'utente di destinazione. Se si posiziona il pulsante in questione all'estrema destra, se l'applicazione è qualsiasi linguaggio scritto da destra a sinistra.

![immagine di tre pulsanti in cui il pulsante critico è più a sinistra in un layout orizzontale.](images/humanux-05.png)

L'opzione consigliata consiste nell'impostare per la ricezione dello stato attivo per impostazione predefinita. Ad esempio, in una finestra di dialogo di conferma dell'eliminazione, l'opzione **No** deve essere evidenziata, perché ciò impedisce all'utente di eliminare accidentalmente qualcosa.

### <a name="simplify-recognition-with-icons"></a>Semplificare il riconoscimento con le icone

Le icone, in particolare le icone di Windows XP e Office 2003 e le bitmap della barra degli strumenti, consentono di velocizzare la conoscenza dell'interfaccia utente e dell'attività che l'utente deve eseguire.

Ad esempio, quando si visualizza l'icona esclamativa più spesso visualizzata nella finestra di messaggio, si diventa immediatamente a conoscenza del livello di rischio associato ai controlli accanto a tale icona. Analogamente, quando l'applicazione mette a disposizione una grande quantità di controlli, indipendentemente dal modo in cui è stata eseguita correttamente, può essere difficile trovare il set di controlli che si sta cercando.

In Windows XP Service Pack 2 viene aggiunta una scheda aggiornata all'applet del pannello di controllo delle **proprietà del sistema** denominata "aggiornamenti automatici". Sono disponibili quattro opzioni: scaricare automaticamente gli aggiornamenti, scaricare gli aggiornamenti, ma consentire all'utente di decidere quando installarli, inviare una notifica all'utente se gli aggiornamenti sono disponibili, ma non avviare il download e disabilitare completamente gli aggiornamenti automatici.

Un nuovo utente del computer potrebbe non essere a conoscenza degli aggiornamenti e potrebbe non essere in grado di individuare l'opzione più adatta. Quindi, Microsoft ha inserito un'icona a scudo verde con un segno di spunta grande accanto al più consigliato, che indica un'opzione "sicura" e un'icona a scudo rossa con una grande "x" accanto a quella che sarebbe potenzialmente dannosa per l'utente. Questa operazione è molto utile in situazioni critiche, soprattutto quando l'utente non ha tempo per leggere troppo testo.

Nella stessa applet delle **proprietà di sistema** , ogni scheda dispone di più GroupBox con diversi controlli per diverse attività. Una rappresentazione grafica relativa viene posizionata accanto a ogni gruppo che può indicare facilmente l'attività del gruppo di controllo. Questo tipo di codice grafico è simile alla codifica a colori in file fisici o parcheggi. Questa operazione funziona anche sullo stesso principio della presenza di almeno alcuni oggetti visivi in un articolo della rivista, ma mantiene l'interesse del lettore.

È importante anche scegliere l'icona a destra. Microsoft fornisce molti elementi grafici standard come parte di Visual Studio 2005. Si tratta della scelta migliore. Se si creano icone personalizzate, è consigliabile seguire gli standard a livello di sistema operativo o di applicazione per questi elementi grafici, come indicato nella sezione [usare gli standard](#use-standards) sopra.

Le [linee guida](/windows/apps/desktop/) per l'interazione con l'esperienza utente di Windows contengono una guida molto utile per la creazione di [Icone](https://msdn.microsoft.com/library/aa511280.aspx)di stile Windows.

### <a name="simplify-recognition-with-headers"></a>Semplificare il riconoscimento con le intestazioni

Le intestazioni rappresentano il modo perfetto per spiegare l'intera finestra di dialogo in una singola frase e, facoltativamente, un elemento grafico. In alcuni casi, le intestazioni possono anche aiutare a supportare anche lo spostamento e i comandi all'interno di essi. Le intestazioni funzionano in modo più efficace rispetto alle normali etichette di descrizione, perché sono la prima cosa che un utente vede quando viene visualizzata la finestra di dialogo.

Le procedure guidate di Windows Installer sono forse le intestazioni più diffuse: un'icona semplice all'estrema destra; etichetta del titolo che descrive la finestra di dialogo, ad esempio selezionare la cartella di installazione. e un'intestazione secondaria che descriva lo scopo della finestra di dialogo (ad esempio, selezionare la cartella in cui verranno installati i file software).

Supponiamo di avere una tipica applicazione aziendale con una sezione accounts. Seguendo il paradigma di progettazione di Windows Vista, è possibile fornire informazioni cruciali e i comandi correlati nell'intestazione (o nel piè di pagina, se lo scenario lo chiama). L'utente ha aperto il file dell'account per "Big Company" e l'intestazione avrà un aspetto simile a quello illustrato nella schermata seguente.

![Screenshot di una finestra di dialogo che contiene un piè di pagina dettagliato.](images/humanux-06.png)

Lo screenshot seguente mostra un esempio di intestazione dettagliata in una finestra di dialogo.

![Screenshot di una finestra di dialogo contenente un'intestazione dettagliata.](images/humanux-07.png)

Analogamente, è possibile evitare di dover aggiungere riquadri attività in stile Windows XP, specialmente quando si dispone di pochi comandi, che potrebbero sprecare molto spazio verticale, spostando questi comandi nell'intestazione.

Quando si progettano le intestazioni, è necessario tenere presente quanto segue:

-   Verificare che il colore di sfondo sia diverso dal colore di sfondo della finestra di dialogo. Spesso, un'intestazione bianca su un colore della faccia del controllo intrinseco Windows standard eseguirà questa operazione. Tuttavia, se si desidera assicurarsi che nessun tema speciale o colori personalizzati inserisca un problema nell'intestazione, creare un **LinearGradient** utilizzando il **colore. FromKnownColor** con i colori **ControlLight** e **ControlDark**.
-   Se possibile, lasciare l'altezza dell'intestazione inferiore a 150 pixel. In genere viene eseguita un'altezza di 100 o 120. Come regola generale, verificare che sia minore di 1/4 dell'altezza dell'intero form.
-   Se si desidera aggiungere la modifica sul posto per le informazioni mostrate nell'intestazione precedente, sostituire in modo dinamico l'oggetto LinkLabel con una casella di testo e scambiarle nuovamente al termine della modifica.
-   Se si dispone di un'etichetta del titolo con un tipo di carattere superiore a 10 PT, utilizzare Arial o Franklin Gothic Medium. MS Sans Serif sarà troppo irregolare e non professionale. Franklin Gothic media è la raccomandazione nella documentazione delle linee guida di progettazione di Windows XP. Per le applicazioni destinate a Windows Vista, utilizzare il tipo di carattere Segoe UI che rappresenta il tipo di carattere predefinito del sistema.

### <a name="use-custom-message-boxes"></a>Usare le finestre di messaggio personalizzate

Le opzioni disponibili nella finestra di messaggio standard di Windows sono molto limitate. Quando è necessario chiedere all'utente una domanda a cui non è possibile rispondere con una semplice sì/no o OK/Annulla, diventa complicata.

Le applicazioni Windows ora diventano più semplici da utilizzare a causa del volume elevato di utenti non tecnici. In alcuni casi può essere molto più semplice fornire pulsanti con testi più amichevoli e anche alcuni controlli aggiuntivi, ad esempio LinkLabel, per semplificare l'esecuzione dell'attività.

Il Framework Microsoft .NET facilita l'implementazione di finestre di dialogo personalizzate. Semplicemente assegnando un paio di proprietà nel form personalizzato della finestra di dialogo o con una singola riga di codice, il form può funzionare esattamente come una finestra di messaggio standard. In un evento clic sul pulsante, impostare la proprietà **DialogResult** della finestra di dialogo su **DialogResult. OK** o **DialogResult. Cancel**. Usare il metodo **ShowDialog ( \[ OwnerForm \] )** dal form padre. Questo metodo di metodo restituisce il valore **DialogResult** .

È possibile utilizzare tutti i membri **DialogResult** . Queste stesse opzioni sono utilizzate dal metodo **MessageBox. Show** standard.

In alternativa, è possibile impostare semplicemente la proprietà **AcceptButton** della finestra di dialogo su **btnOK** e la proprietà **CancelButton** su **btnCancel**. Questa operazione eseguirà automaticamente il mapping dei tasti **Enter** e **ESC** ai pulsanti **btnOK** e **btnCancel** per i rispettivi eventi click.

Ecco alcuni suggerimenti per rendere disponibili le finestre di dialogo personalizzate:

-   Per argomenti complicati, fornire collegamenti alla guida locale o online con un oggetto LinkLabel che informa "ulteriori informazioni" nell'etichetta di testo appropriata.
-   Anziché  /  / i pulsanti **Annulla** , usare i testi che indicano chiaramente il risultato della selezione del pulsante, ad esempio "Salva file e Chiudi", "Esci senza salvare" e "non uscire". Tuttavia, attenersi allo standard **Yes** / **No**, **OK** / **Cancel** e tali pulsanti standard, laddove possibile. Una certa familiarità garantisce una produttività elevata.
-   Mantieni lo spazio dei margini di 50 pixel sul lato sinistro (o sul lato destro a seconda delle impostazioni cultura di destinazione) e Aggiungi un'icona che rappresenta lo scenario per la finestra di dialogo. Se si tratta di una finestra di dialogo informativa, è possibile utilizzare l'icona "i" utilizzata dalle finestre di messaggio standard. Se si tratta di una finestra di dialogo di sicurezza, è possibile usare un'icona di blocco o un'icona a chiave. Visual Studio 2005 viene fornito con una grafica di alta qualità.
-   Assicurarsi sempre di fornire una corretta navigazione da tastiera per questi pulsanti: gli utenti usano i tasti di scelta rapida per le finestre di messaggio (ad esempio, O per OK, Y per Sì, C per annullamento e così via). Si tratta di un fastidio se la finestra di dialogo personalizzata non le utilizza.

### <a name="include-alternate-commands"></a>Includi comandi alternativi

Due fattori importanti stabiliscono la necessità di metodi di input alternativi, frustrazione e pigrizia. La frustrazione è una cosa che si verifica troppo spesso per gli utenti di computer. Quando si è frustrati, si desidera che l'attività venga eseguita rapidamente. Un altro clic o un'attesa aggiuntiva di pochi secondi fa davvero infuriare una persona sottoposta a stress, che è già presente. La pigrizia spesso invita a completare l'attività con solo la tastiera o il mouse, a seconda del momento in cui si usa. Tuttavia, oltre a questi due fattori, l'utilizzo di metodi di input alternativi consente di semplificare l'operazione.

Ad esempio, se si dispone di una casella di riepilogo con due pulsanti, ovvero "Aggiungi" e "Rimuovi", su entrambi i lati, è necessario aggiungere un menu di scelta rapida per tale casella di riepilogo con i comandi di menu analoghi a tali pulsanti. Ciò consente all'utente di scegliere il metodo più adatto. Gli utenti principianti, come lo stato delle linee guida sull'esperienza utente di Windows Vista, utilizzano i menu di scelta rapida e prevedono che si trovino in qualsiasi punto.

Analogamente, vengono usati controlli visivi per l'input di testo o numerici. I dispositivi di scorrimento, ad esempio, vengono usati per specificare numeri interi e i controlli calendario vengono usati per l'input di data. In alcuni casi può essere più semplice immettere solo digitando. Spesso può creare una differenza per l'utente se si aggiunge un controllo Up-Down numerico collegato a un dispositivo di scorrimento oppure si usa un oggetto DateTimePicker anziché il controllo Calendar.

### <a name="how-to-handle-critical-actions"></a>Come gestire le azioni critiche

Quando si esegue una funzione critica e irreversibile, in genere è consigliabile creare una finestra di messaggio popup per confermare l'azione. Diamo un'intacca. Nella schermata seguente è possibile visualizzare una finestra di messaggio personalizzata simile, ma con un vantaggio aggiunto, un timer visualizzato visivamente con l'ausilio di un indicatore di stato.

![screenshot della finestra di dialogo di un'azione critica.](images/humanux-08.png)

Esistono alcune varianti specifiche dello scenario che è possibile usare. Se l'azione da intraprendere è molto critica (a partire dal sovraccarico di un impianto nucleare per l'eliminazione permanente dei file), l'azione predefinita dopo l'esaurimento del timer deve essere Annulla. La finestra di dialogo non deve essere eliminata, ma l'etichetta di testo viene modificata per indicare che l'azione è stata annullata. L'utente può scegliere di confermare il comando o l'annullamento.

Assicurarsi sempre che i pulsanti che eseguono operazioni critiche siano contrassegnati in modo chiaro: usare sempre testo non crittografato che descrive accuratamente l'azione. Se l'azione è l'eliminazione dei file, non scrivere "Rimuovi file dal repository"; scrivere "Elimina file dal repository". Quando si lavora con gli elenchi di file, se un comando di menu Delete Elimina i file selezionati dal disco rigido stesso (in contrapposizione alla rimozione solo dall'elenco dei file), è necessario sottolineare in modo appropriato la natura critica di questo e sottolineare in modo esplicito che l'azione eliminerà definitivamente i file.

Una volta detto, l'utente è molto utile come il lavoro peggiore. Lo stesso vale per le applicazioni software. Una singola esperienza negativa con l'app può comportare una grande impressione negativa sull'utente. Per assicurarsi che non si verifichi questo problema, è possibile fare in modo che, in caso di arresto anomalo dell'applicazione, si verifichi un arresto normale. Se è possibile aggiungere il ripristino dei dati o consentire all'utente di provare a salvare una copia di tali dati, può essere un grande vantaggio. L'utente deve ricevere una notifica corretta in caso di arresto anomalo dell'applicazione. Un JIT-Debugger o una finestra di dialogo di errore critica non è un aspetto positivo. Quando si parla di come gestire gli arresti anomali esula dall'ambito di questo articolo, si consiglia di fare in modo che una semplice finestra di dialogo che chiede all'utente di rivolgersi alla situazione (e possibilmente con un collegamento ad altre informazioni su come risolvere questo arresto anomalo) risulti molto utile per l'utente.

Se si desidera eseguire un'ulteriore operazione, è possibile eseguire una delle applicazioni di progettazione grafica preferite. In caso di arresto anomalo, verrà visualizzata una finestra di dialogo di ripristino che consente di salvare una copia separata del file su cui si sta lavorando e quindi di visualizzare una finestra di dialogo di feedback in cui è possibile immettere le informazioni sull'arresto anomalo (informazioni personali facoltative, ovviamente) e inviarle agli autori.

### <a name="radiobuttons-or-comboboxes"></a>Pulsanti o ComboBox?

A prima vista, il metodo per eseguire una selezione uno-a-molti non sembra così difficile o importante. In alcuni casi può essere, soprattutto se lo scenario è un'applicazione usata per il lavoro dipendente dal tempo.

Diamo uno sguardo a un esempio di vita reale. Microsoft ha recentemente rilasciato una versione di anteprima di un'applicazione grafica, Expression graphics designer (denominata in precedenza "acrilico"). Avevo circa 20 oggetti grafici a cui ho dovuto assegnare separatamente una determinata proprietà in questa applicazione. Si tratta di un processo tetro. A tale scopo, ho dovuto selezionare l'oggetto, fare clic sul pulsante per attivare la finestra impostazioni e impostare le opzioni. In una di queste opzioni è stato necessario selezionare due opzioni da una casella combinata, come si può notare nello screenshot seguente.

![screenshot della finestra di dialogo di trama Fringe per la finestra di progettazione grafica delle espressioni.](images/humanux-09.png)

Quando è necessario scorrere l'elenco ComboBox e selezionare il secondo elemento (solo 2 elementi), è possibile che si stia effettivamente irritando. Ciò che non è in genere possibile realizzare è il tempo necessario per visualizzare l'elenco a discesa. E può essere molto frustrante. Questo problema può essere risolto facilmente inserendo un oggetto GroupBox con due radiopulsanti, soprattutto quando è disponibile molto spazio. Sono stati riscontrati problemi simili nelle applicazioni, ad esempio CorelDRAW, Microsoft Access e altri.

Oltre a sprecare tempo a causa dell'animazione a discesa, viene sprecata anche la "larghezza di banda mentale". Con due radiopulsanti "sempre visibili", è opportuno che la posizione del cursore venga rilevata in modo subliminale. Con la casella combinata verrà elaborata solo dopo che l'elenco è stato disegnato. Sebbene possa sembrare troppo poco importante, in realtà è molto importante.

A volte è preferibile usare i radiopulsanti, soprattutto se si dispone di 4 scelte o meno.

### <a name="never-disrupt-the-user"></a>Non Interrompi mai l'utente.

A breve, si tratta dell'elemento più distruttivo che uno sviluppatore può eseguire per gli utenti. Quando l'applicazione, inutilmente o altrimenti, interrompe l'utente mentre lavora su un'altra applicazione con una finestra di messaggio o una barra delle applicazioni Flash, si ottengono punti negativi dall'utente.

I flash della barra delle applicazioni possono essere utili, ovviamente, ma devono essere richiamati solo quando il processo dell'applicazione richiede l'input dell'utente per continuare o se si dispone di un elemento critico da inviare all'utente. Se l'utente ha mantenuto la barra delle applicazioni in caso di Nascondi automaticamente, un pulsante della barra delle applicazioni lampeggiante può impedire all'utente di accedere alla barra di stato o ad altri controlli di basso livello, perché la barra delle applicazioni si trova sopra di essa e non viene nascosta di nuovo fino a quando l'utente non fa clic sul pulsante lampeggiante.

![Screenshot di una finestra popup.](images/humanux-10.png)

Le finestre "toast" (vedere la figura 10), rese famose da client di messaggistica immediata come MSN Messenger, rappresentano un'ottima soluzione per informare l'utente di qualcosa senza irritare o interferire con il proprio flusso di lavoro. È disponibile un articolo straordinario ( https://docs.microsoft.com/archive/msdn-magazine/2005/september/sprinkle-some-pizzazz-on-your-plain-vanilla-windows-forms-apps) di Bill Wagner per la creazione di finestre popup. È opportuno che i criteri e le modalità di non disturbino i toast di altre applicazioni. L'ostruzione di tali finestre può risultare fastidiosa e non produttiva. Una soluzione consiste nell'usare il mutex ToastSemaphore (/library/WinMessenger/winmessenger/overview/toast.asp) fornito dal sistema operativo per evitare collisioni di tipo avviso popup.

In alcuni casi potrebbe essere necessario visualizzare più elementi tramite il popup. Il prelevamento di tre o più popup non sarebbe davvero consigliabile. In ogni caso, è consigliabile eseguire il proseguimento di un popup dopo l'altro. Microsoft Outlook implementa una soluzione simile quando invia una notifica all'utente dei messaggi di posta elettronica in arrivo.

### <a name="provide-progress-status"></a>Fornire lo stato di avanzamento

Spesso sono presenti attività che richiedono l'intervento dell'utente. Naturalmente, questo è uno degli elementi che l'utente odia semplicemente. Ma peggiori è quando sono in attesa senza sapere cosa accade. Talvolta è possibile che l'applicazione debba connettersi a un servizio Web o a un computer remoto o che stia elaborando blocchi di dati di grandi dimensioni, a prescindere dal motivo, l'utente deve essere informato o almeno vagamente, cosa accade dietro le quinte. Esistono diversi metodi per eseguire questa operazione, in base alla situazione.

Se ci si connette ad alcuni oggetti lontani come un servizio Web o un elemento inserito in una rete o in un server Internet, è consigliabile visualizzare una finestra di dialogo di stato semplice (vedere l'immagine seguente) o un indicatore di stato ospitato nella barra di stato. Un'etichetta associata dovrebbe descrivere lo stato corrente del processo. Se ad esempio ci si connette a un servizio Web per elaborare alcuni dati, è sufficiente indicare "connessione al servizio Web... "o" attendere, elaborazione... "Se questo processo è sincrono, è consigliabile disabilitare tutti i controlli a cui l'utente può accedere fino a quando il processo non è stato completato o semplicemente visualizzare lo stato di avanzamento come finestra di dialogo modale.

![Screenshot di una finestra di dialogo Indicatore di stato.](images/humanux-11.png)

È consigliabile impostare lo stile dell'indicatore di stato sulla modalità marquee se si utilizza un indicatore di stato e il tempo di elaborazione è sconosciuto o se non si dispone di un valore massimo.

Un altro metodo che sta diventando popolare è una finestra ' toast ' fissa che visualizza lo stato di avanzamento. I popup di Microsoft AntiSpyware Downloader/Updater o di Norton AntiVirus per la posta elettronica sono ottimi esempi. Naturalmente, questa operazione deve essere usata solo per i processi asincroni. In caso contrario, l'utente potrebbe non essere più concordato. Tali finestre sono particolarmente utilizzate per l'elaborazione in background, ad esempio il download di un aggiornamento o l'esecuzione di un'attività pianificata, e non devono mai essere impostate su "always on top".

### <a name="simplify-complex-steps-with-wizards"></a>Semplificare i passaggi complessi con le procedure guidate

È possibile presupporre che, se affrontato con una pletora di controlli in un singolo form, un utente tipico verrà confuso senza alcuna fine. In alcuni casi, la quantità di raggruppamento, ridimensionamento o spaziatura può risultare utile quando si dispone di molti controlli importanti.

Una procedura guidata è la cosa migliore per questi scenari. È possibile dividere i controlli per attività o categorie come applicabile e inserirli in passaggi distinti. Questo può aiutare gli utenti a rimanere concentrati e non essere scoraggiati dall'attività. Con un pulsante? è possibile specificare una guida specifica per i passaggi o le attività. È possibile trovare le linee guida per la creazione della procedura guidata in MSDN Library.

Le procedure guidate rappresentano anche un modo efficace per configurare la configurazione iniziale dell'applicazione. Molte applicazioni usano una procedura guidata per configurare la configurazione personalizzata subito dopo il completamento dell'installazione o al primo utilizzo. Una procedura guidata iniziale deve anche essere resa facoltativa, se possibile, se l'utente annulla in qualsiasi momento, le impostazioni non specificate passano ai valori predefiniti. Se è possibile fare in modo che la procedura guidata sia un po' grafica (vedere la sezione [usare una grafica piuttosto](#use-pretty-graphics) interessante), l'attività di configurazione risulta molto più semplice.

### <a name="get-the-tone-of-your-text-right"></a>Ottenere il tono del testo a destra

Nelle linee guida per l'interazione con l' [esperienza utente di Windows](/windows/apps/desktop/)è stato apportato un punto molto importante su "testo tono". Si tratta dell'impressione e della sensazione fornita dal testo nell'applicazione. Può trattarsi di qualsiasi elemento di una semplice descrizione comando a un controllo etichetta di istruzione.

In precedenza è stata illustrata la modifica del testo nell'opzione webcam in MSN Messenger. Questo metodo è denominato tono di testo appropriato. Quando si gestiscono utenti non tecnici o principianti, il messaggio viene preso da un altro aspetto.

Se si scrive "percorso di destinazione" sopra una casella di testo in un'applicazione autoestraente, un utente tecnico può facilmente essere a conoscenza di immettere un valore simile a "C: \\ temp \\ percorso". Un utente con novizio (pensa a "mom") può essere facilmente confuso e dovrebbe fare riferimento al manuale, chiamare il supporto tecnico, o peggiori, rinunciare. Una valida alternativa consiste nel specificare le operazioni che l'utente deve eseguire: "selezionare la cartella in cui si desidera inserire i file". È anche possibile rinominare il "Sfoglia... "pulsante che si trova accanto a tale casella di testo per" selezionare la cartella... "

Se si fornisce una descrizione chiara di ciò che si desidera che l'utente esegua la riduzione della necessità di file della guida, o meno i dettagli che è necessario includere nei file della guida.

Un suggerimento molto valido dalle linee guida per l'interazione con l' [esperienza utente di Windows](/windows/apps/desktop/) si applica a tutti i software. Indica che il writer deve tenere il testo colloquiale. Le linee guida definiscono questo come, "evitare le parole che non si vuole dire a un altro utente".

Alcuni suggerimenti per la scrittura di testo:

-   Evitare di parlare dell'utente nella terza persona. Pronunciare "utente" invece di "utente".
-   Laddove possibile, utilizzare con cautela il nome "My Name:" o "My email address:" invece di "Name:" o "email:"
-   Quando si assegnano più opzioni, scrivere il testo dal punto di vista dell'utente. Se, ad esempio, si dispone di due radiopulsanti sotto un'etichetta, ad esempio "Seleziona autorizzazione per \[ nome utente \] in questa rete" sopra due radiopulsanti, ad esempio "Consenti" e "Nega", sostituire il testo di RadioButton con "Voglio consentire il \[ nome utente \] " e "Desidero impedire il \[ nome utente" \] .
-   Sottolineare il testo solo se viene usato per i collegamenti. Confonde l'utente se il testo sottolineato non è un collegamento.
-   Attirare l'attenzione su informazioni importanti con un'etichetta in grassetto, ma usarla attentamente. Il testo in grassetto è molto confuso e riduce l'effetto complessivo del modulo.
-   Quando si scrive il testo per una casella di controllo, assicurarsi che sia facile sapere cosa accadrà quando viene selezionato e quando viene deselezionato o deselezionato. L'opzione consigliata consiste nel scrivere il testo direttamente come risultato della selezione della casella di controllo. Ad esempio, scrivi "Inviami informazioni utili dai tuoi partner" invece di "non inviare informazioni utili dai tuoi partner". Sebbene sia possibile immaginare che molti addetti al marketing discutono su questo particolare esempio, sono certo di sapere cosa intendo.
-   Se è presente un controllo simile a un pulsante (in genere un RadioButton con un aspetto del pulsante di comando) che controlla abilitato/disabilitato, assicurarsi di etichettarlo correttamente. Se il processo è abilitato, scrivere "Enabled" invece di "Enable" o "Disable". Se la scrittura è abilitata, viene visualizzato lo stato corrente. Se si fa clic sul pulsante (abilitato) e il pulsante indica "Enable", può essere confuso e problematico. "Enable" potrebbe richiedere all'utente di fare clic su di esso pensando che il processo non sia attivo.

### <a name="sometimes-a-listview-is-better"></a>A volte un controllo ListView è migliore

Spesso si passa a DataGrid o ListBox o anche a ComboBox per le attività di selezione, ma con Windows XP e versioni successive di Windows, l'uso di un controllo ListView può offrire opzioni più grandi.

Punti fine del controllo ListView:

-   Accelera il riconoscimento degli elementi con icone e bitmap.
-   Visualizza informazioni aggiuntive con i dettagli o le visualizzazioni affiancate.
-   Con Visual Studio 2005, è anche possibile avere gruppi per la categorizzazione aggiuntiva. I gruppi si estendono in tutte le visualizzazioni e sono flessibili. I gruppi possono essere usati anche per appiattire una visualizzazione gerarchica, ad esempio un oggetto TreeView, in cui sono presenti più nodi figlio rispetto ai nodi padre. Un esempio valido è la finestra di dialogo connessioni di rete in Windows XP, se visualizzata con "Mostra in gruppi" e la vista è impostata su dettagli.
-   Per personalizzare un controllo ListView, dipingerlo manualmente impostando la proprietà **OwnerDraw** e utilizzando gli eventi **DrawItem** e **DrawSubItem** .
-   Supporta la modifica sul posto rapida degli elementi ListView.
-   Supporta facilmente il riordino manuale.
-   Consente agli utenti di selezionare la visualizzazione (icone grandi, icone piccole, elenchi e così via) più agevoli.

### <a name="simplify-navigation-with-breadcrumb-controls-and-sidebars"></a>Semplificare la navigazione con controlli di navigazione e barre laterali

"Navigazione secondaria" è la chiave per un'interfaccia utente complessa. In alcuni casi non è possibile sfuggire a una complessa interfaccia utente. La cosa migliore da fare in una situazione di questo tipo consiste nel rendere l'esperienza più semplice possibile per l'utente. Una barra laterale costituita da etichette di collegamento o da un TreeView per la navigazione basata su gerarchia suggerisce un'esplorazione del livello di pari livello per l'attività della finestra di dialogo corrente. In questo modo, è molto semplice per l'utente passare tra i passaggi del processo e sapere dove si trova.

Se si utilizza un'esplorazione basata su gerarchia con TreeView o un'altra navigazione complessa, un'utilità efficace per l'utente è un controllo di navigazione. Anche se Visual Studio non è ancora fornito con un controllo incorporato, vedere [creazione di un controllo di navigazione](/archive/msdn-magazine/2005/july/advanced-basics-creating-a-breadcrumb-control) per informazioni su come crearne uno. Un controllo di navigazione semplifica la ricerca della posizione corrente rispetto alla gerarchia.

L'esplorazione del percorso di navigazione può essere facilmente unita all'intestazione se presente nel form. Vedere la sezione precedente sulle [intestazioni](#simplify-recognition-with-headers).

### <a name="use-pretty-graphics"></a>Usa grafica piuttosto semplice

Tutti amano le applicazioni con grafica interessante, almeno la maggior parte. Anche se un'interfaccia utente con una grafica piuttosto semplice non è una scelta logica per tutte le applicazioni, è utile per creare un'ottima impressione e può essere il piacere di lavorare. Naturalmente, la grafica non dovrebbe ostacolare la produttività, ma se utilizzata correttamente può aumentare.

Non è necessario che siano presenti molti elementi grafici, né necessariamente richiedono molto lavoro. Una schermata iniziale progettata professionalmente o un'intestazione, ad esempio quella che abbiamo menzionato in precedenza, è il trucco. Se il budget lo consente, è possibile usare grafica ben progettata per le barre degli strumenti, le procedure guidate e altro ancora. L'aspetto dell'app è piuttosto semplice e professionale. Si tratta di un effetto sottile, ma un aspetto professionale esprime fiducia e stabilità. Se si è una società relativamente piccola che crea applicazioni per la vendita al dettaglio, questo è un aspetto fondamentale da considerare.

Fai sempre un punto per usare graficamente progettata professionalmente. Le immagini prive di diritti d'autore sono facilmente disponibili e convenienti. È anche possibile assumere una finestra di progettazione. Ma se la grafica non è la forte, non provare a usarla. Se non è possibile acquisire o utilizzare graficamente progettate professionalmente, è preferibile non utilizzarle affatto.

Per la grafica di piccole dimensioni è sempre possibile passare alle icone e alle bitmap fornite con Visual Studio 2005. Non è consigliabile usare la grafica fornita con le versioni precedenti.

### <a name="provide-resizable-forms-when-possible"></a>Fornire moduli ridimensionabili quando possibile

Le finestre ridimensionabili sono piuttosto simili alle finestre indipendenti dalla risoluzione. Le finestre indipendenti dalla risoluzione hanno lo stesso aspetto se si usano le schermate 96DPI o 300DPI. Se l'interfaccia utente dell'applicazione è indipendente dalla risoluzione, sarà migliore se è ridimensionabile. Naturalmente, questa situazione non si applica a molti scenari, ma è una valida regola per scopi generali.

Se la finestra gestisce gli elenchi di qualsiasi ordinamento, in particolare i ListView, questo diventa ancora più importante. Il ridimensionamento consente all'utente di esaminare più dati nello stesso momento.

Ad esempio, si dispone di un'applicazione in cui l'utente deve selezionare un'immagine da una raccolta di grandi dimensioni. La finestra di dialogo Apri consente di selezionare una visualizzazione di anteprima, ma la finestra di dialogo è a dimensione fissa e l'elenco di anteprime Mostra solo 4 anteprime alla volta. Se la raccolta ha un centinaio di immagini, lo scorrimento e la ricerca, un'attività ripetitiva, può essere piuttosto noiosa e una riduzione dell'efficienza. Se la finestra di dialogo è ridimensionabile, l'utente può renderla più grande di quanto sia comoda o almeno uguale a quella consentita dallo schermo ed essere in grado di completare rapidamente l'attività. Se l'elenco ha lo scorrimento orizzontale, ad esempio un controllo ListView o DataGrid dettagliato, è ancora più noioso. Le finestre ridimensionabili sono molto utili in una situazione di questo tipo.

### <a name="provide-more-functionality-with-sidebarstask-panes"></a>Offrire più funzionalità con i riquadri Sidebar/attività

Come le intestazioni di cui si parlava in precedenza, le barre laterali e i riquadri attività sono un ottimo modo per fornire ulteriori funzionalità e comandi di utilità. I riquadri attività in Office Word 2003, ad esempio, sono molto pratici, accessibili e non intrusivi. Funzionano anche in modo asincrono quando ci si connette a risorse online, offrendo all'utente la possibilità di eseguire attività diverse.

La creazione di un riquadro attività o di un'intestazione laterale è semplice come la creazione di un pannello ancorato, con la possibilità di inserire un grafico slick nella parte superiore per fungere da barra del titolo. È anche possibile usare un controllo Label colorato. Le opportunità per i riquadri attività sono molte.

Se si dispone di funzionalità aggiuntive e si desidera fornirle in modo non intrusivo per l'utente, non esiste alcun posto come il riquadro attività. È anche possibile creare riquadri attività "Nascondi automaticamente" o comprimere come le finestre degli strumenti di Visual Studio.

### <a name="give-a-notification-choice"></a>Concedi una scelta di notifica

In precedenza abbiamo visto come creare una finestra di messaggio personalizzata. Se una finestra di messaggio nell'applicazione verrà visualizzata spesso all'utente, può essere opportuno aggiungere una casella di controllo che l'utente può selezionare per disabilitare la finestra di dialogo in futuro. Questa opzione è particolarmente utile per i messaggi più evidenti.

Un esempio familiare è la finestra di dialogo di ricerca di Visual Studio. Quando si cerca o si sostituisce il testo, Visual Studio Visualizza una finestra di messaggio che informa i risultati. Tuttavia, viene anche offerta la possibilità di disabilitare tale finestra di messaggio. Può essere davvero fastidioso se è necessario premere INVIO oppure fare clic su OK ogni volta che si esegue la ricerca.

Un altro aspetto interessante di Visual Studio è che anche se la finestra di dialogo è disabilitata, Visualizza comunque i risultati dell'operazione nella barra di stato.

### <a name="provide-tooltips"></a>Fornire descrizioni comandi.

Talvolta le descrizioni comandi consentono di risparmiare molto tempo. I pulsanti, le caselle di controllo e altri controlli possono essere ambigui e l'utente potrebbe non essere sicuro di cosa fare. Le descrizioni comandi forniscono la forma migliore di guida sensibile al contesto in una sola riga. L'utente può decidere rapidamente cosa fare senza cercare nulla nel file della guida o aprire un'altra finestra.

Spesso gli utenti ignorano questa funzionalità nelle proprie applicazioni. Creare un punto per aggiungere descrizioni comandi a tutti i controlli ambigui oppure a tutti i controlli, se possibile. Non ripetere il testo di un'etichetta associata o del testo del controllo, ma fornire informazioni aggiuntive su tale controllo. Il testo deve spiegare la funzione del controllo in poche parole.

### <a name="do-not-forget-the-little-things"></a>Non dimenticare le piccole cose

Le piccole cose possono compromettere l'utente, ma ignorarle possono avere un effetto sull'impressione che si apportano. Una volta ho usato un'applicazione fatta da una persona importante nel settore del software che ha impostato la proprietà BorderStyle del modulo su un valore notevole, ma i controlli sul lato destro del form non erano ancorati. Per questo motivo, l'applicazione creata da un settore pesante ha avuto un aspetto non professionale.

Questi tipi di "piccoli elementi" sono il nucleo dell'impressione complessiva. L'interfaccia utente e l'esperienza utente dell'applicazione sono i cui utenti giudicherà l'applicazione, almeno alla prima. Se si verificano bug evidenti nell'interfaccia utente, è possibile che l'applicazione sia meno potente ed efficace.

## <a name="conclusion"></a>Conclusione

Si è trattato solo di una piccola parte dell'esperienza utente umana. Poiché l'esperienza utente diventa più semplice, efficace, divertente e più intuitiva, l'attività di creazione dell'esperienza utente diventa molto più complessa. Tuttavia, con alcune previsioni e una buona pianificazione, è possibile creare un'esperienza utente eccezionale.

Il modo migliore per creare un'esperienza utente perfetta consiste nell'eseguire test di usabilità destinati in particolare all'interfaccia utente, sia che si tratti di un gruppo di test speciale o autonomo. Maggiore è la quantità di tempo impiegato per testare l'esperienza utente prima di rilasciare l'applicazione. In seguito verrà risparmiato molto tempo.

 

 