---
title: Creazione di animazioni
description: Creazione di animazioni
ms.assetid: 6d5c3c61-b3f2-4505-aa43-b6d001c444a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed5955e57af405451def3208902678d3d6a0ffb9857cc719bfe100dbbd2447f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752329"
---
# <a name="creating-animations"></a>Creazione di animazioni

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per iniziare a creare animazioni per il tuo carattere, seleziona **l'icona Animazioni** nell'albero. Verrà visualizzata la **pagina Proprietà** con le impostazioni predefinite per tutte le animazioni. È possibile modificare le dimensioni del frame, la durata predefinita del frame e le impostazioni della tavolozza dei colori nella **pagina** Proprietà.

### <a name="setting-your-characters-frame-size"></a>Impostazione delle dimensioni del frame del carattere

L'altezza e la larghezza dei fotogrammi dell'animazione devono rimanere costanti per tutta la definizione del carattere, ovvero per tutte le animazioni del carattere. Anche se è possibile modificare le dimensioni del frame rispetto all'impostazione predefinita (128 x 128 pixel), le immagini visualizzate nell'editor verranno ridimensionate in base alle dimensioni di visualizzazione predefinite. Se si modifica l'impostazione predefinita del frame, è possibile visualizzare le  dimensioni complete e non ridimensionate del frame scegliendo Apri finestra cornice **dal** menu Modifica.

### <a name="setting-your-characters-palette"></a>Impostazione della tavolozza del carattere

Per impostazione predefinita, l'editor usa la prima immagine bitmap caricata per impostare la tavolozza dei colori predefinita del<sup></sup> carattere, i colori che determinano la modalità di visualizzazione del carattere e imposta il colore nell'undicesimo punto della tavolozza come colore di trasparenza. Tuttavia, è possibile impostare la tavolozza e la trasparenza in modo esplicito nel **gruppo Informazioni tavolozza** . In questo modo è possibile specificare un file di immagine da utilizzare per la tavolozza. È possibile specificare uno dei file di immagine di animazione o qualsiasi file grafico. Il file della tavolozza specificato deve essere un file di colori a 8 bit (256). Dopo il caricamento, usare il pulsante **Cambia impostazione** per modificare il colore della trasparenza.

La tavolozza dei colori del carattere non deve modificare il mapping dei colori di sistema standard. L'editor riserva automaticamente la tavolozza dei colori del sistema durante la visualizzazione delle immagini. Inoltre, tutte le immagini di animazione devono usare la stessa tavolozza dei colori e lo stesso colore di trasparenza. Questo è molto importante. In caso contrario, è possibile che venga visualizzato un nuovo mapping dei colori delle immagini quando vengono caricate nell'editor.

Sebbene sia possibile impostare la tavolozza dei colori per il carattere, nei sistemi Windows in cui le proprietà di visualizzazione sono impostate su una tavolozza dei colori a 8 bit (256), il colore del carattere sarà soggetto alla tavolozza di sistema corrente. Poiché le applicazioni possono modificare la tavolozza di sistema, è possibile che il carattere non venga visualizzato con le impostazioni di colore corrette. Anche se non è possibile evitare questo problema, è possibile ridurre l'effetto limitando il numero di colori usati e impostando la tavolozza del carattere in base alla tavolozza usata dall'applicazione che guida il carattere. Ad esempio, se si sviluppa un carattere da usare con le pagine Web, è possibile impostare la tavolozza del carattere usando la tavolozza a metà Internet Explorer di Microsoft Internet Explorer. È possibile acquisire la tavolozza del browser facendo clic con il pulsante destro del mouse  su un'immagine in una pagina Web, scegliendo il comando **Salva** immagine con nome e scegliendo **Bitmap** nell'opzione Salva con nome e quindi facendo clic su **Salva**. Per ottimizzare i file di immagine dell'animazione in un file di tavolozza specifico, è possibile usare un prodotto come Equilibizer DeBabelizer.

### <a name="creating-a-new-animation"></a>Creazione di una nuova animazione

Dopo aver determinato le impostazioni di animazione globali, è possibile iniziare a creare animazioni. Per creare una nuova animazione, scegliere **Nuova animazione** dal menu **Modifica** o dal **pulsante Nuova** animazione sulla barra degli strumenti. Verrà aggiunta una nuova icona di animazione nell'albero sotto l'icona **Animazioni** e alla nuova icona verrà assegnato un nome predefinito. È possibile rinominare l'animazione digitando nel **campo Nome animazione.** Si noti che i nomi delle animazioni all'interno di una definizione di carattere devono essere univoci. Evitare inoltre di usare caratteri nel nome che non sono caratteri validi per i nomi di file.

### <a name="adding-frames"></a>Aggiunta di frame

Ogni animazione è costituita da fotogrammi. Per creare un nuovo frame per l'animazione, scegliere **Nuovo frame** dal menu **Modifica o** dalla barra degli strumenti. Verrà aggiunta una nuova icona cornice all'albero sotto l'icona dell'animazione e verranno visualizzate tre pagine a schede. La **pagina** Generale include controlli che consentono di caricare e modificare un'immagine per il frame. Include anche un'area di visualizzazione per l'aspetto della cornice.

![Screenshot che mostra il riquadro Immagine con il nome file, il percorso e la posizione.](images/f2charflame.gif)

Un frame può contenere una o più immagini. Per definire un'immagine per un frame, fare clic **sul pulsante Aggiungi file di** immagine appena sopra la casella **di** riepilogo Immagini. Verrà **visualizzata la finestra di dialogo** Seleziona file di immagine che consente di selezionare un file di immagine bitmap.

![Screenshot che mostra un file di immagine selezionato in Esplora file.](images/f3chardialbox.gif)

Selezionare il file da caricare, scegliere **Apri** per visualizzare l'immagine nel frame visualizzato nella **pagina** Generale. L'editor accetta le immagini archiviate in formato bitmap a 1 bit (monocromatico), a 4 o a 8 bit Windows bitmap o come formato GIF.

È possibile usare i quattro pulsanti freccia sotto l'immagine nella casella **Posizione** per modificare l'aspetto dell'immagine all'interno della cornice. Se le dimensioni dell'immagine sono superiori a quelle del frame, verrà visualizzata solo la parte dell'immagine visualizzata all'interno del frame. Se si aumentano le dimensioni del frame, l'immagine può essere ridimensionata per adattarsi all'area di visualizzazione dell'editor.

È anche possibile visualizzare un frame scegliendo **Apri finestra cornice** dal menu Modifica.  Il frame corrente viene visualizzato in una finestra separata senza ridimensionare le immagini caricate nel frame. Le dimensioni iniziali di questa finestra si basano sulle impostazioni di altezza e larghezza del frame. È possibile ridimensionarlo più piccolo, ma non più grande. La finestra cornice riflette le modifiche apportate usando i controlli nell'editor e consente anche di visualizzare il frame durante la visualizzazione delle altre pagine delle proprietà.

![Screenshot che mostra il riquadro Posizione.](images/f4charposctrl.gif)

È possibile comporre un frame da più immagini. Ogni volta che si seleziona il **pulsante Aggiungi immagine** e si sceglie un'altra immagine, l'immagine viene aggiunta all'elenco e all'area di visualizzazione dell'immagine. È anche possibile aggiungere più immagini selezionando più di un file. Premere MAIUSC o CTRL mentre si fa clic nella **finestra di dialogo** Seleziona file di immagine e quindi scegliere **Apri.** I **pulsanti Sposta su** e Sposta **giù** sopra la **casella** di riepilogo Immagini spostano un'immagine selezionata nell'ordine di visualizzazione (ordine Z) per il frame. È anche possibile spostare le immagini trascinandole all'interno dell'elenco. Se si seleziona un'immagine nell'elenco e si fa clic **sul pulsante** Elimina, viene rimossa un'immagine. Per modificare un'immagine caricata in un altro file di immagine, è possibile fare clic sul nome file  per modificarla direttamente oppure usare il pulsante **...** (puntini di sospensione) per visualizzare la finestra di dialogo Seleziona file di immagine e selezionare un file diverso.

![Screenshot che mostra il pulsante con i puntini di sospensione.](images/f5charell.gif)

È possibile usare la **casella di** testo Durata per impostare la durata del frame. che indica per quanto tempo verrà visualizzato il frame. Se un frame non ha un'immagine e una durata pari a zero, non verrà visualizzato durante la riproduzione dell'animazione.

È anche possibile specificare un file di effetto sonoro da riprodurre quando viene visualizzato il fotogramma. Se si prevede di caricare il carattere da un server Web, è possibile comprimere il file dell'effetto sonoro per ridurre al minimo il tempo di caricamento. È quindi possibile specificare il file audio compresso nell'Editor caratteri dell'agente. Evitare inoltre di usare un effetto sonoro con una durata superiore alla durata dell'animazione ed evitare in particolare un effetto sonoro che scorre a ciclo continuo, perché i servizi di animazione di Microsoft Agent non inviano un evento di completamento dell'animazione fino al completamento dell'audio. Evitare anche di specificare un effetto sonoro  per qualsiasi animazione assegnata agli stati Ascolto o **Ascolto,** perché ciò interferisce con l'input vocale. Infine, anche se è possibile includere più di un effetto sonoro in un'animazione, evitare di posizionarli in modo che si sovrappongano, perché ciò può influire sulla durata dell'animazione. Tenere inoltre presente che gli effetti sonori possono essere riprodotti a velocità diverse in base all'hardware dell'utente.

Per aggiungere fotogrammi all'animazione, scegliere di nuovo il **comando Nuovo** frame e seguire la stessa procedura. È anche possibile caricare più immagini e generare automaticamente nuovi fotogrammi. Per usare questa funzionalità, scegliere **Nuovi fotogrammi da immagini** dal menu Modifica.  I frame verranno creati in ordine alfabetico in base ai nomi file dell'immagine. Dopo aver definito tutti i fotogrammi per l'animazione, è possibile scegliere di nuovo il **comando Nuova** animazione per iniziare una nuova animazione.

Esistono altri modi per aggiungere fotogrammi alle animazioni e spostare i fotogrammi all'interno o tra le animazioni. È possibile selezionare un altro fotogramma (dalla  stessa animazione o da un'altra) e scegliere Taglia o **Copia,** quindi selezionare l'animazione o un frame in tale animazione e scegliere **Incolla.** È anche possibile trascinare un frame da un'animazione a un'altra. Se si trascina all'interno di un'animazione, l'azione sposta il frame. Se si trascina in un'altra animazione, il frame viene copiato. Il trascinamento su un frame precedente nella stessa animazione inserisce il frame prima del frame in cui si trascina. Il trascinamento su un frame seguente lo posiziona dopo il frame in cui si trascina. Se si trascina un frame usando il pulsante destro del mouse, il rilascio del pulsante visualizza un menu a comparsa con le scelte di trasferimento.

È anche possibile creare un'animazione copiando un'animazione esistente  (selezionare l'animazione e scegliere **Copia),** selezionare l'icona Animazioni o un'altra icona di animazione e scegliere **Incolla.** L'editor crea automaticamente un nuovo nome per l'animazione, anche se è possibile modificare il nome.

### <a name="branching"></a>Diramazione

Quando si crea un frame, è anche possibile definire quale fotogramma riprodurre successivamente. Per impostazione predefinita, il fotogramma successivo riprodotto nella sequenza di animazione è sempre il fotogramma successivo nell'ordine Z. Tuttavia, scegliendo la **pagina Diramazione,** è possibile impostare la probabilità per un massimo di tre altri fotogrammi che il server può riprodurre. Immettere la percentuale di probabilità e il numero di fotogramma di destinazione nei campi appropriati. È possibile specificare la diramazione anche per i fotogrammi che non hanno immagini e la cui durata è impostata su zero. In questo modo è possibile creare rami senza prima visualizzare una determinata immagine.

![Screenshot che mostra la pagina "Diramazione".](images/f6charbranch.gif)

È possibile usare la funzionalità di diramazione per creare animazioni che verranno ciclizzate per un periodo illimitato. Si noti tuttavia che quando viene riprodotta un'animazione a ciclo continuo, le altre animazioni nella coda del carattere non verranno riprodotte fino a quando un evento, ad esempio un utente che preme il tasto di pressione o l'applicazione client che chiama il metodo [**Stop,**](stop-method.md) interrompe l'animazione a ciclo continuo. Considerare quindi attentamente il contesto in cui verrà usata l'animazione prima di creare un'animazione a ciclo continuo.

La pagina di diramazione consente anche di creare la diramazione di uscita. Un ramo di uscita è un ramo di un frame che verrà utilizzato dall'animazione quando l'animazione viene arrestata e prima che venga riprodotta l'animazione successiva. La definizione dei rami di uscita consentirà di spostarsi senza problemi durante la transizione da un'animazione a un'altra. La diramazione di uscita non deve creare un ciclo circolare, ma alla fine deve essere in grado di uscire dall'ultimo fotogramma dell'animazione.

Non è necessario specificare un ramo di uscita per ogni fotogramma, tuttavia, in caso contrario, l'animazione seguirà la diramazione normale del frame. Se il frame non ha un ramo esplicito, l'animazione si dirama automaticamente al frame che lo segue. Ad esempio, se si dirama dal frame 3 al frame 1 e il frame 1 non ha altri rami (ramo normale o di uscita), il frame 1 si diramerà al frame 2. Se il frame 2 non ha diramazioni, l'animazione tornerà al frame 3 e si avrà un ciclo circolare. È invece possibile creare un ramo dal frame 3 al frame 1 e quindi impostare il ramo di uscita del frame 1 su qualsiasi frame successivo al frame 3 e in genere proceda all'ultimo fotogramma dell'animazione.

In alcuni casi può essere necessario creare un frame finale esplicito di un'animazione che non viene riprodotta in modo visibile, ma che fornisce una fine dell'animazione. Ad esempio, è necessario uscire dall'animazione, ma uscire dall'ultimo fotogramma non è appropriato. A tale scopo, è possibile creare un fotogramma di durata zero vuoto come ultimo fotogramma dell'animazione. In questo modo l'animazione può essere riprodotta normalmente attraverso l'ultimo fotogramma dell'animazione e consente anche di fornire un punto di uscita finale per la diramazione di uscita.

### <a name="previewing-an-animation"></a>Anteprima di un'animazione

È possibile visualizzare in anteprima l'animazione nell'Editor di caratteri dell'agente scegliendo il comando Anteprima dal **menu** Modifica o il pulsante Anteprima sulla barra degli strumenti.  Viene riprodotta l'animazione, inclusi eventuali rami ed effetti sonori, a partire dal frame selezionato corrente. Al termine dell'animazione, viene ripristinato il fotogramma selezionato corrente. Per riprodurre l'intera animazione, passare alla visualizzazione albero, selezionare l'icona dell'animazione o il primo fotogramma dell'animazione e scegliere **il comando Anteprima.** L'editor aggiunge un'animazione ai frame nella **pagina** Generale. Per arrestare l'anteprima prima della fine, scegliere il **comando Arresta** anteprima. Il **comando Anteprima** cambia automaticamente in **Arresta anteprima durante** la riproduzione dell'anteprima.

È anche possibile visualizzare in anteprima la diramazione di uscita scegliendo il comando Anteprima **Esci da** diramazione dal **menu** Modifica o sulla barra degli strumenti. consente di testare la modalità di visualizzazione della diramazione di uscita da qualsiasi frame specifico.

### <a name="assigning-speaking-overlays"></a>Assegnazione di sovrimpressione di pronuncia

È possibile definire un carattere in modo che pronuncia durante l'ultimo fotogramma dell'animazione. In questo frame scegliere la pagina **Sovrimpressione.** Questa pagina consente di caricare e assegnare i file di immagine della erta alle posizioni standard supportate da Microsoft Agent. Fare clic **sul pulsante Aggiungi** immagine e selezionare l'immagine nella finestra di dialogo. È anche possibile selezionare più immagini e l'editor carica e assegna le immagini a partire dalla posizione selezionata. Fare clic **sui pulsanti Sposta su** e Sposta **giù** oppure trascinare una voce per modificare l'assegnazione di un'immagine nell'elenco. Fare clic **sul pulsante** Elimina per rimuovere un'immagine. È anche possibile modificare il percorso di un file assegnato facendo clic sulla relativa voce  nell'elenco e quindi  digitare nuovamente il nome del file oppure scegliendo il pulsante con i puntini di sospensione per visualizzare la finestra di dialogo Seleziona file di immagine.

![Screenshot che mostra la pagina "Sovrimpressione" con un file selezionato.](images/f7charover.gif)

Le sovrimpressione della cornice devono rientrare nel contorno della cornice di base su cui verranno visualizzate. In caso contrario, verranno ritagliati nel frame di base.

Se si vuole fare in modo che il carattere parla con la sua testa al di fuori della cornice di base, ad esempio quando il carattere deve parlare lateralmente, creare prima la cornice di base con la testa del carattere (o l'area che si sposterà mentre il carattere parla) come immagine superiore. Definire quindi le sovrimpressione della sovrimpressione per sostituire l'immagine e impostare **l'opzione Replace Base Frame Top Image (Sostituisci** immagine principale fotogramma di base). È anche possibile usare il **pulsante Imposta tutto** per impostare questa opzione per tutte le sovrimpressione della cornice.

### <a name="assigning-a-return-animation"></a>Assegnazione di un'animazione return

Per creare una transizione uniforme da un'animazione a quella successiva, progettare le sequenze di animazione in modo che inizino e terminano con un'immagine neutra. Per altre informazioni, vedere [**Progettazione di caratteri per Microsoft Agent.**](designing-characters-for-microsoft-agent.md) Tuttavia, ciò non significa che ogni animazione deve terminare in corrispondenza della posizione neutra. È possibile aggiungere un'animazione a un carattere tramite una sequenza di fotogrammi, farlo parlare durante l'ultimo fotogramma e creare un'animazione complementare separata che restituisca il carattere alla posizione neutra. Questa animazione complementare è detta animazione Return.

È possibile definire un'animazione Return creando un'animazione esplicita a questo scopo. È anche possibile creare un'animazione Return usando la diramazione di uscita definita all'interno dell'animazione. Per assegnare un'animazione Return, selezionare l'animazione nell'albero e selezionare l'animazione Return creata o Use Exit Branching (Usa diramazione uscita) dall'elenco a discesa Return Animation (Restituisce animazione) nella pagina Proprietà.

La creazione e l'assegnazione di un'animazione Return hanno un ulteriore vantaggio: quando il server riceve una richiesta per riprodurre un'altra animazione, tenterà di riprodurre l'animazione Return per l'ultima animazione riprodotta, se viene assegnata un'animazione Return. In questo modo si garantisce una transizione senza problemi. Se un'animazione inizia e termina in corrispondenza della posizione neutra, non è necessario definire un'animazione Return. Analogamente, se si intende gestire manualmente le transizioni da un'animazione a un'altra, potrebbe non essere necessario assegnare un'animazione Return.

### <a name="assigning-animations-to-states"></a>Assegnazione di animazioni agli stati

I servizi di animazione di Microsoft Agent riproducino automaticamente le animazioni quando l'applicazione client di hosting usa determinati metodi. Ad esempio, quando un'applicazione chiama i [**metodi MoveTo**](moveto-method.md) e [**GestureAt,**](gestureat-method.md) il server determina automaticamente dove viene visualizzato il carattere e riproduce un'animazione appropriata. Analogamente, Microsoft Agent riproduce automaticamente animazioni inattive quando l'utente non ha interagito con il carattere per alcuni secondi. Queste condizioni, quando il server riproduce automaticamente animazioni per conto di un'applicazione, sono denominate *stati*. Tuttavia, perché il server sappia quale animazione riprodurre, è necessario assegnare animazioni a questi stati.

Per assegnare un'animazione o animazioni a uno stato, creare l'animazione appropriata, espandere la voce Stati nella visualizzazione albero della finestra dell'editor e selezionare l'icona Stato. L'elenco delle animazioni create viene visualizzato in una casella di riepilogo sul lato destro della finestra. Selezionare l'animazione da assegnare a questo stato. Si noti che è possibile assegnare più animazioni allo stesso stato. In questo modo il server può selezionare in modo casuale animazioni diverse per lo stato. L'assegnazione di un'animazione a uno stato non impedisce a un'animazione di riprodurre direttamente tale animazione.

È anche possibile assegnare un'animazione a uno stato selezionando la voce dell'animazione nell'albero. Nella **casella di riepilogo Assegna** a stato della **pagina** Proprietà sono elencati gli stati. Selezionare la casella di controllo dello stato a cui si sta assegnando l'animazione.

L'editor non supporta la creazione di stati aggiuntivi perché gli stati si applicano solo alle situazioni in cui il server deve riprodurre automaticamente un'animazione per conto dell'applicazione client. Pertanto, la definizione del proprio stato non ha alcun vantaggio. Se necessario, è possibile riprodurre qualsiasi animazione in modo esplicito usando il [**metodo Play.**](play-method.md)

### <a name="saving-your-character-definition"></a>Salvataggio della definizione del carattere

È possibile salvare il file di definizione del carattere scegliendo il **comando** Salva dal menu **File** o il **pulsante Salva** definizione carattere sulla barra degli strumenti. Se si vuole salvare il file di definizione dei caratteri con un nuovo nome, scegliere il **comando Salva** con nome dal menu **File.** L'editor salva la definizione modificabile di un carattere come definizione di carattere agente (. ACD). È anche possibile modificare questo formato di file di testo auto documentato con la maggior parte degli editor di testo e delle applicazioni di elaborazione di testo.

### <a name="printing-your-character-definition"></a>Stampa della definizione del carattere

Per stampare la definizione del carattere, scegliere **il comando Stampa** dal menu **File** o il **pulsante Stampa** sulla barra degli strumenti. Per impostare le proprietà per l'output stampato, scegliere il **comando Imposta** pagina e scegliere le impostazioni prima di selezionare il **comando** Stampa.

### <a name="building-a-character"></a>Compilazione di un carattere

Al termine della creazione delle animazioni, il carattere e le immagini devono essere compilati in un formato speciale utilizzato da Microsoft Agent per caricare questi dati. Per compilare un carattere, selezionare il comando Compila carattere dal menu **File** o dalla barra degli strumenti. Se sono presenti modifiche non salvate nel file di definizione dei caratteri, l'editor salva il file di definizione prima di visualizzare la **finestra di** dialogo Carattere di compilazione .

![Screenshot che mostra la finestra "Build Character" (Carattere di compilazione) con un file selezionato.](images/f8charbldg.gif)

L'editor di caratteri dell'agente proporrà automaticamente un nome file in base al nome del file di definizione del carattere. La finestra di dialogo Compila carattere include anche un elenco a discesa che consente di scegliere tra la compilazione del carattere come singolo file di archiviazione (. ACS) o come più file. Se si sceglie quest'ultimo, l'editor compila un oggetto . File ACF che include i dati del carattere e un oggetto . File ACA per ogni animazione creata. Se si prevede di installare e accedere a un carattere archiviato nello stesso computer dell'applicazione client, in genere si sceglie il singolo formato di file strutturato. Questo formato offre un'installazione semplice ed efficiente e l'accesso al carattere. Tuttavia, se si accede al carattere da un server Web usando il protocollo HTTP, compilare il carattere usando . Formato di file ACF (individuale). Quest'ultima struttura di file consente a uno script della pagina Web di caricare singoli file di animazione, archiviando i dati nella cache dei file del browser dell'utente. Offre un accesso più efficiente sul Web perché i dati di animazione possono essere scaricati in base alle esigenze anziché richiedere all'utente di attendere il download dell'intero set di animazioni contemporaneamente. Inoltre, poiché i dati del carattere vengono archiviati nella cache del browser, lo spazio file può essere recuperato automaticamente.

Sebbene sia anche possibile scaricare dati di tipo carattere (come un singolo file strutturato o più file) da un server Web e installarli altrove nel computer di un utente, questo metodo richiede provisioning di sicurezza per il download e l'installazione. Di conseguenza, l'API di Microsoft Agent non include il supporto per l'installazione scaricabile di un carattere, ad eccezione della cache del browser. Tuttavia, è comunque possibile supportare questo scenario creando un controllo di installazione personalizzato e distribuerlo seguendo le convenzioni di sicurezza appropriate. Per altre informazioni, vedere Microsoft Internet Client Software Development Kit.

L'opzione Comprimi consente di specificare se i dati di tipo carattere sono compressi. In genere, è necessario impostare questa opzione per compattare i dati di tipo carattere, anche se la compilazione di un carattere con i dati compattati richiede più tempo.

Dopo aver compilato un carattere, le compilazioni successive saranno più veloci se si compila il carattere nello stesso percorso di directory. L'editor di caratteri verifica e copia automaticamente i file che non sono stati modificati e ricompila tutti i dati modificati.

Se l'editor rileva eventuali errori nel file di caratteri durante la compilazione del carattere, scrive le informazioni in un file di log e visualizza una finestra di messaggio. È possibile scegliere di visualizzare il file di log o ignorarlo e leggerlo in un secondo momento con un editor di testo. Si noti tuttavia che l'editor sovrascriverà il file di log alla successiva compilazione di un file di caratteri.

### <a name="editing-an-existing-character"></a>Modifica di un carattere esistente

Per modificare un carattere esistente, scegliere **Apri** dal menu **File,** selezionare il file di definizione del carattere (. ACD) nella finestra di dialogo risultante e scegliere Apri. Il file verrà caricato nell'editor. Si noti che non è possibile caricare file di caratteri compilati (. Acs. ACF o . ACA) con l'editor.

Poiché il file di definizione del carattere (. ACD) è un file di testo, è anche possibile modificare la definizione di un carattere aprendo il file con un editor di testo o un programma di elaborazione di testo. Tuttavia, quando si completano le modifiche, assicurarsi di salvare il file nel formato originale prima di caricarlo nell'editor di caratteri per la compilazione.

 

 




