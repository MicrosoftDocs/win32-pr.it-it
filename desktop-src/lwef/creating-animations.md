---
title: Creazione di animazioni
description: Creazione di animazioni
ms.assetid: 6d5c3c61-b3f2-4505-aa43-b6d001c444a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16c460908e7c782054a3f62ece87d01e7c9a817
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104551229"
---
# <a name="creating-animations"></a>Creazione di animazioni

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per iniziare a creare animazioni per il carattere, selezionare l'icona **animazioni** nell'albero. Verrà visualizzata la pagina delle **Proprietà** con le impostazioni predefinite per tutte le animazioni. È possibile modificare la dimensione del frame, la durata predefinita del frame e le impostazioni della tavolozza dei colori nella pagina delle **Proprietà** .

### <a name="setting-your-characters-frame-size"></a>Impostazione delle dimensioni del frame del carattere

L'altezza e la larghezza del fotogramma di animazione devono rimanere costanti per tutta la definizione del carattere, ovvero per tutte le animazioni di tale carattere. Sebbene sia possibile modificare le dimensioni del frame dall'impostazione predefinita (128 x 128 pixel), le immagini visualizzate nell'editor verranno ridimensionate in modo da adattarsi alle dimensioni di visualizzazione predefinite. Se si modifica l'impostazione predefinita del frame, è possibile visualizzare le dimensioni complete e non ridimensionate del frame scegliendo **Apri finestra cornice** dal menu **modifica** .

### <a name="setting-your-characters-palette"></a>Impostazione della tavolozza del carattere

Per impostazione predefinita, l'editor usa la prima immagine bitmap caricata per impostare la tavolozza dei colori predefinita del carattere, i colori che determinano come viene visualizzato il carattere e imposta il colore nella posizione della tavolozza di 11<sup>°</sup> come colore di trasparenza. Tuttavia, è possibile impostare la tavolozza e la trasparenza in modo esplicito nel gruppo **informazioni tavolozza** . In questo modo è possibile specificare un file di immagine da usare per la tavolozza. È possibile specificare uno dei file di immagine dell'animazione o qualsiasi file grafico. Il file della tavolozza specificato deve essere un file di colore a 8 bit (256). Al termine del caricamento, usare il pulsante **Modifica impostazione** per modificare il colore della trasparenza.

La tavolozza dei colori del carattere non deve modificare il mapping dei colori di sistema standard. L'editor riserva automaticamente la tavolozza dei colori del sistema quando si visualizzano le immagini. Inoltre, è necessario che tutte le immagini di animazione usino la stessa tavolozza dei colori e il colore della trasparenza. Questo è molto importante. In caso contrario, è possibile che venga visualizzato il mapping dei colori delle immagini quando vengono caricate nell'editor.

Sebbene sia possibile impostare la tavolozza dei colori per il carattere, nei sistemi Windows in cui le proprietà di visualizzazione sono impostate su una tavolozza dei colori a 8 bit (256), il colore del carattere sarà soggetto alla tavolozza di sistema corrente. Poiché le applicazioni possono modificare la tavolozza di sistema, il carattere potrebbe non essere visualizzato con le impostazioni del colore corrette. Sebbene non esistano modi per evitare questo problema, è possibile ridurre l'effetto limitando il numero di colori utilizzati e impostando la tavolozza del carattere in base alla tavolozza usata dall'applicazione che guida il carattere. Se, ad esempio, si sta sviluppando un carattere da utilizzare con le pagine Web, è possibile impostare la tavolozza dei caratteri utilizzando la tavolozza dei mezzitoni di Microsoft Internet Explorer. È possibile acquisire la tavolozza del browser facendo clic con il pulsante destro del mouse su un'immagine in una pagina Web e scegliendo il comando **Salva immagine come** e scegliendo **bitmap** nell'opzione **Salva con nome** e quindi facendo clic su **Salva**. Per ottimizzare i file di immagine dell'animazione in un file di tavolozza specifico, potrebbe essere necessario usare un prodotto come DeBabelizer di equilibrio.

### <a name="creating-a-new-animation"></a>Creazione di una nuova animazione

Dopo aver determinato le impostazioni di animazione globale, è possibile iniziare la creazione di animazioni. Per creare una nuova animazione, scegliere **nuova animazione** dal menu **modifica** o dal pulsante **nuova animazione** sulla barra degli strumenti. Viene aggiunta una nuova icona di animazione nell'albero sotto l'icona **animazioni** e viene assegnata alla nuova icona un nome predefinito. È possibile rinominare l'animazione digitando nel campo **nome animazione** . Si noti che i nomi di animazione all'interno di una definizione di caratteri devono essere univoci. Inoltre, evitare di usare caratteri non validi per i nomi di file nel nome.

### <a name="adding-frames"></a>Aggiunta di frame

Ogni animazione è costituita da frame. Per creare un nuovo frame per l'animazione, scegliere **nuovo frame** dal menu **modifica** o dalla barra degli strumenti. Viene aggiunta una nuova icona del frame all'albero sotto l'icona di animazione e vengono visualizzate tre pagine a schede. Nella pagina **generale** sono inclusi i controlli che consentono di caricare e modificare un'immagine per il frame. Include anche un'area di visualizzazione per l'aspetto del frame.

![Screenshot che mostra il riquadro immagine con il nome file, il percorso e la posizione.](images/f2charflame.gif)

Un frame può contenere una o più immagini. Per definire un'immagine per un frame, fare clic sul pulsante **Aggiungi file di immagine** appena sopra la casella di riepilogo **Immagini** . Viene visualizzata la finestra di dialogo **Seleziona file di immagine** , che consente di selezionare un file di immagine bitmap.

![Screenshot che mostra un file di immagine selezionato in Esplora file.](images/f3chardialbox.gif)

Selezionare il file che si desidera caricare, scegliere **Apri**. l'immagine verrà visualizzata nella visualizzazione frame della pagina **generale** . L'editor accetta immagini archiviate come formato bitmap di Windows a 1 bit (monocromatico), a 4 bit o a 8 bit o come formato GIF.

È possibile usare i quattro pulsanti freccia sotto l'immagine nella casella **posizione** per modificare l'aspetto dell'immagine all'interno del frame. Se l'immagine è più grande delle dimensioni del frame, verrà visualizzata solo la parte dell'immagine visualizzata all'interno del frame. Se si aumentano le dimensioni del frame, l'immagine può essere ridimensionata per adattarsi all'area di visualizzazione dell'editor.

È anche possibile visualizzare un frame scegliendo **Apri finestra cornice** dal menu **modifica** . Viene visualizzato il frame corrente in una finestra separata senza ridimensionare le immagini caricate nel frame. Le dimensioni iniziali della finestra sono basate sulle impostazioni di altezza e larghezza del fotogramma. È possibile ridimensionarlo più piccolo, ma non più grande. La finestra cornice riflette le modifiche apportate usando i controlli nell'editor e consente anche di visualizzare il frame durante la visualizzazione delle altre pagine delle proprietà.

![Screenshot che mostra il riquadro posizione.](images/f4charposctrl.gif)

È possibile comporre un frame da più immagini. Ogni volta che si seleziona il pulsante **Aggiungi immagine** e si sceglie un'altra immagine, l'immagine viene aggiunta all'elenco e all'area di visualizzazione dell'immagine. È anche possibile aggiungere più immagini selezionando più di un file. Premere MAIUSC o CTRL mentre si fa clic nella finestra di dialogo **Seleziona file di immagine** , quindi scegliere **Apri**. I pulsanti **Sposta su** e **Sposta giù** sopra la casella di riepilogo **Immagini** spostano un'immagine selezionata nell'ordine di visualizzazione (ordine z) per il frame. È anche possibile spostare le immagini trascinandoli all'interno dell'elenco. Se si seleziona un'immagine nell'elenco e si fa clic sul pulsante **Elimina** , viene rimossa un'immagine. Per modificare un'immagine caricata in un altro file di immagine, è possibile fare clic sul nome del file per modificarlo direttamente o utilizzare il pulsante **...** (puntini di sospensione) per visualizzare la finestra di dialogo **Seleziona file di immagine** e selezionare un altro file.

![Screenshot che mostra il pulsante con i puntini di sospensione.](images/f5charell.gif)

È possibile utilizzare la casella di testo **durata** per impostare la durata del frame. ovvero per quanto tempo verrà visualizzato il frame. Se un frame non ha un'immagine e una durata pari a zero, il frame non verrà visualizzato quando viene riprodotta l'animazione.

È anche possibile specificare un file di effetto audio da riprodurre quando viene visualizzato il frame. Se si prevede di caricare il carattere da un server Web, è possibile comprimere il file degli effetti acustici per ridurre al minimo il tempo di caricamento. È quindi possibile specificare il file audio compresso nell'editor dei caratteri di Agent. Inoltre, evitare di utilizzare un effetto acustico con una durata superiore alla durata dell'animazione, evitando in particolare un effetto acustico che esegue cicli, perché i servizi animazione agente Microsoft non inviano un evento di animazione completo fino al completamento del suono. Evitare inoltre di specificare un effetto acustico per qualsiasi animazione assegnata agli Stati di **ascolto** o **udito** , perché questo interferisce con l'input vocale. Infine, sebbene sia possibile includere più di un effetto audio in un'animazione, evitare di posizionarli in modo che si sovrappongano, perché ciò può influire sulla tempistica dell'animazione. Tenere inoltre presente che gli effetti acustici possono essere riprodotti a frequenze diverse in base all'hardware dell'utente.

Per aggiungere frame all'animazione, scegliere nuovamente il comando **nuovo frame** e seguire la stessa procedura. In alternativa, è anche possibile caricare più immagini e generare automaticamente nuovi frame. Per usare questa funzionalità, scegliere **nuovi frame dalle immagini** dal menu **modifica** . I frame verranno creati in ordine alfabetico in base ai nomi dei file di immagine. Al termine della definizione di tutti i frame per l'animazione, è possibile scegliere nuovamente il comando **nuova animazione** per iniziare una nuova animazione.

Esistono altri modi per aggiungere frame alle animazioni e spostare i frame all'interno o tra le animazioni. È possibile selezionare un altro frame dalla stessa animazione o da un'altra, quindi scegliere **taglia** o **copia**, quindi selezionare l'animazione o un frame nell'animazione e scegliere **Incolla**. È anche possibile trascinare un frame da un'animazione a un'altra. Se si trascina in un'animazione, l'azione sposta il frame. Se si trascina in un'altra animazione, il frame viene copiato. Il trascinamento di un frame precedente nella stessa animazione inserisce il frame prima del frame in cui si trascina. Il trascinamento su un frame seguente lo posiziona dopo il frame in cui si trascina. Se si trascina un frame usando il pulsante destro del mouse, il rilascio del pulsante Visualizza un menu a comparsa con le scelte di trasferimento.

È anche possibile creare un'animazione copiando un'animazione esistente (selezionare l'animazione e scegliere **copia**) e selezionando l'icona **animazioni** o un'altra icona di animazione e scegliendo **Incolla**. L'editor crea automaticamente un nuovo nome per l'animazione, sebbene sia possibile modificarne il nome.

### <a name="branching"></a>Diramazione

Quando si crea un frame, è anche possibile definire il frame successivo. Per impostazione predefinita, il fotogramma successivo riprodotto nella sequenza di animazione è sempre il frame successivo nell'ordine z. Tuttavia, scegliendo la pagina **diramazione** , è possibile impostare la probabilità per un massimo di tre altri frame che possono essere riprodotti dal server. Immettere la percentuale di probabilità e il numero di frame di destinazione nei campi appropriati. È possibile specificare la diramazione anche per i frame che non dispongono di immagini e la cui durata è impostata su zero. In questo modo è possibile creare un ramo senza prima visualizzare un'immagine specifica.

![Screenshot che mostra la pagina "branching".](images/f6charbranch.gif)

È possibile usare la funzionalità di diramazione per creare animazioni che comporteranno un ciclo indefinito. Si noti tuttavia che quando viene riprodotta un'animazione di ciclo, altre animazioni nella coda del carattere non vengono riprodotte fino a quando un evento, ad esempio un utente che preme il tasto push-to-Talk o l'applicazione client che chiama il metodo [**Stop**](stop-method.md) , interrompe l'animazione di ciclo. Pertanto, valutare con attenzione il contesto in cui l'animazione verrà utilizzata prima di creare un'animazione di ciclo.

La pagina di diramazione consente inoltre di creare una diramazione di uscita. Un ramo di uscita è un ramo di un frame che verrà eseguito dall'animazione quando l'animazione viene arrestata e prima che venga riprodotta la successiva animazione. La definizione dei rami di uscita consente di spostarsi senza problemi durante la transizione da un'animazione a un'altra. La diramazione di uscita non deve creare un ciclo circolare, ma deve essere in grado di uscire dall'ultimo frame dell'animazione.

Tuttavia, non è necessario fornire un ramo di uscita per ogni frame. in caso contrario, l'animazione seguirà la normale diramazione del frame. Se il frame non ha un ramo esplicito, l'animazione viene automaticamente diramata al frame che lo segue. Se, ad esempio, si esegue il branching dal frame 3 al frame 1 e il frame 1 non contiene altre diramazioni (ramo normale o di uscita), il frame 1 diramato al frame 2. Se al frame 2 non è associata alcuna diramazione, l'animazione viene diramata di nuovo al frame 3 e si dispone di un ciclo circolare. Al contrario, è possibile eseguire il branching dal frame 3 al frame 1 e quindi impostare il ramo di uscita del frame 1 su qualsiasi frame che è dopo il frame 3 e normalmente procede all'ultimo frame dell'animazione.

In alcuni casi potrebbe essere necessario creare un frame finale esplicito di un'animazione che non viene riprodotta in modo visibile, ma fornisce una fine dell'animazione. È ad esempio necessario uscire dall'animazione, ma uscire dall'ultimo frame non è appropriato. È possibile eseguire questa operazione creando un frame di durata zero vuoto come ultimo frame dell'animazione. Ciò consente di riprodurre normalmente l'animazione nell'ultimo frame dell'animazione e di fornire un punto di uscita finale per la diramazione di uscita.

### <a name="previewing-an-animation"></a>Visualizzazione in anteprima di un'animazione

È possibile visualizzare in anteprima l'animazione nell'editor dei caratteri di Agent scegliendo il comando **Anteprima** dal menu **modifica** o il pulsante Anteprima sulla barra degli strumenti. Questa operazione riproduce l'animazione, inclusi i rami e gli effetti audio, a partire dal frame selezionato corrente. Viene reimpostato sul frame selezionato corrente al termine dell'animazione. Per riprodurre l'intera animazione, passare alla visualizzazione albero, selezionare l'icona o il primo frame dell'animazione e scegliere il comando **Anteprima** . L'editor anima i frame nella pagina **generale** . Per arrestare l'anteprima prima che termini, scegliere il comando **Arresta anteprima** . Il comando **Anteprima** cambia automaticamente in **Interrompi anteprima** mentre viene riprodotta l'anteprima.

È anche possibile visualizzare in anteprima la diramazione di uscita scegliendo il comando **Anteprima uscita diramazione** dal menu **modifica** o sulla barra degli strumenti. Consente di testare il modo in cui verrà visualizzata la diramazione di uscita da qualsiasi frame specifico.

### <a name="assigning-speaking-overlays"></a>Assegnazione di sovrimpressioni pronunciate

È possibile definire un carattere in modo che parli durante l'ultimo frame della relativa animazione. In questo frame scegliere la pagina **sovrimpressione** . Questa pagina consente di caricare e assegnare file di immagine mouth alle posizioni di bocca standard supportate da Microsoft Agent. Fare clic sul pulsante **Aggiungi immagine** e selezionare l'immagine dalla finestra di dialogo. È anche possibile selezionare più immagini e l'editor caricherà e assegnerà le immagini iniziando con la posizione della bocca selezionata. Fare clic sui pulsanti **Sposta su** e **Sposta giù** o trascinare una voce per modificare l'assegnazione di un'immagine nell'elenco. Per rimuovere un'immagine, fare clic sul pulsante **Elimina** . È anche possibile modificare il percorso di un file assegnato facendo clic sulla voce corrispondente nell'elenco e ridigitando il nome del file oppure scegliendo il pulsante con i **puntini** di sospensione per visualizzare la finestra di dialogo **Seleziona file di immagine** .

![Screenshot che mostra la pagina "sovrimpressioni" con un file selezionato.](images/f7charover.gif)

Gli overlay della bocca devono rientrare nel contorno del frame di base su cui verranno visualizzati. In caso contrario, verranno ritagliati nel frame di base.

Se si vuole che il carattere parli con la bocca al di fuori del frame di base, ad esempio, quando il carattere deve parlare lateralmente, creare prima di tutto il frame di base con la testa del carattere (o l'area che verrà spostata quando il carattere parla) come immagine superiore. Definire quindi le sovrapposizioni della bocca per sostituire l'immagine e impostare l'opzione **Replace base frame Top Image** . È anche possibile usare il pulsante **imposta tutto** per impostare questa opzione per tutte le sovrapposizioni della bocca nel frame.

### <a name="assigning-a-return-animation"></a>Assegnazione di un'animazione return

Per creare una transizione uniforme da un'animazione alla successiva, progettare le sequenze di animazione per iniziare e terminare con un'immagine neutra. Per ulteriori informazioni, vedere [**progettazione di caratteri per Microsoft Agent**](designing-characters-for-microsoft-agent.md). Tuttavia, ciò non significa che ogni animazione deve terminare in corrispondenza della posizione neutra. È possibile aggiungere un'animazione a un carattere mediante una sequenza di frame, fare in modo che parli durante l'ultimo frame e creare un'animazione separata e complementare che restituisce il carattere nella posizione neutra. Questa animazione complementare è detta animazione di ritorno.

È possibile definire un'animazione return creando un'animazione esplicita a questo scopo. È anche possibile creare un'animazione return usando la diramazione di uscita definita all'interno dell'animazione. Per assegnare un'animazione restituita, selezionare l'animazione nell'albero e selezionare l'animazione restituita creata o utilizzare la diramazione di uscita dall'elenco a discesa animazione restituita nella pagina proprietà.

La creazione e l'assegnazione di un'animazione restituita hanno un vantaggio aggiuntivo: quando il server riceve una richiesta di riproduzione di un'altra animazione, tenterà di riprodurre l'animazione restituita per l'ultima animazione riprodotta, se viene assegnata un'animazione di ritorno. In questo modo si garantisce una transizione senza problemi. Se un'animazione inizia e termina in corrispondenza della posizione neutra, non è necessario definire un'animazione restituita. Analogamente, se si intende gestire le transizioni da un'animazione a un'altra, potrebbe non essere necessario assegnare un'animazione return.

### <a name="assigning-animations-to-states"></a>Assegnazione di animazioni agli Stati

I servizi animazione agente Microsoft riproducono automaticamente le animazioni quando l'applicazione client host usa determinati metodi. Ad esempio, quando un'applicazione chiama i metodi [**MoveTo**](moveto-method.md) e [**GestureAt**](gestureat-method.md) , il server determina automaticamente la posizione in cui viene visualizzato il carattere e riproduce un'animazione appropriata. Analogamente, Microsoft Agent esegue automaticamente animazioni inattive quando l'utente non ha interagito con il carattere per alcuni secondi. Queste condizioni, quando il server riproduce automaticamente le animazioni per conto dell'applicazione, sono denominate *Stati*. Tuttavia, affinché il server sappia quale animazione riprodurre, è necessario assegnare animazioni a questi Stati.

Per assegnare un'animazione o animazioni a uno stato, creare l'animazione appropriata, espandere la voce stati nella visualizzazione albero della finestra dell'editor e selezionare l'icona stato. L'elenco delle animazioni create viene visualizzato in una casella di riepilogo sul lato destro della finestra. Controllare l'animazione che si vuole assegnare a questo stato. Si noti che è possibile assegnare più di un'animazione allo stesso stato. Ciò consente al server di selezionare in modo casuale animazioni diverse per lo stato. L'assegnazione di un'animazione a uno stato non impedisce l'esecuzione diretta di un'animazione.

È anche possibile assegnare un'animazione a uno stato selezionando la voce dell'animazione nell'albero. Nella casella **di riepilogo assegna a stato** della pagina **Proprietà** sono elencati gli Stati. Selezionare la casella di controllo dello stato a cui si sta assegnando l'animazione.

L'editor non supporta la creazione di stati aggiuntivi perché gli Stati si applicano solo alle situazioni in cui il server deve riprodurre automaticamente un'animazione per conto dell'applicazione client. Non vi sono quindi vantaggi nella definizione del proprio stato. Se necessario, è possibile riprodurre in modo esplicito qualsiasi animazione utilizzando il metodo [**Play**](play-method.md) .

### <a name="saving-your-character-definition"></a>Salvataggio della definizione dei caratteri

È possibile salvare il file di definizione del carattere scegliendo il comando **Salva** nel menu **file** o il pulsante per la **definizione dei caratteri Salva** sulla barra degli strumenti. Se si desidera salvare il file di definizione dei caratteri con un nuovo nome, scegliere il comando **Salva con** nome dal menu **file** . L'editor salva la definizione modificabile di un carattere come definizione del carattere dell'agente (. ACD). È anche possibile modificare questo formato di file di testo autodocumentato con la maggior parte degli editor di testo e delle applicazioni di elaborazione di Word.

### <a name="printing-your-character-definition"></a>Stampa della definizione dei caratteri

Per stampare la definizione del carattere, scegliere il comando **stampa** dal menu **file** o il pulsante **stampa** sulla barra degli strumenti. Per impostare le proprietà per l'output stampato, scegliere il comando **Imposta pagina** e scegliere le impostazioni prima di selezionare il comando **stampa** .

### <a name="building-a-character"></a>Compilazione di un carattere

Al termine della creazione delle animazioni, il carattere e le immagini devono essere compilati in un formato speciale usato da Microsoft Agent per caricare i dati. Per compilare un carattere, selezionare il comando Compila carattere dal menu **file** o dalla barra degli strumenti. Se nel file di definizione dei caratteri sono presenti modifiche non salvate, l'editor Salva il file di definizione prima di visualizzare la finestra di dialogo **carattere di compilazione** .

![Screenshot che mostra la finestra di "carattere di compilazione" con un file selezionato.](images/f8charbldg.gif)

L'editor dei caratteri dell'agente proporrà automaticamente un nome file in base al nome file della definizione del carattere. La finestra di dialogo carattere di compilazione include anche un elenco a discesa in cui è possibile scegliere se compilare il carattere come singolo file di archiviazione (. ACS) o come più file. Se si sceglie il secondo, l'editor compila un oggetto. File ACF che include i dati del carattere e un oggetto. File ACA per ogni animazione creata. Se si prevede di installare e accedere a un carattere archiviato nello stesso computer dell'applicazione client, in genere si sceglie il formato di file strutturato singolo. Questo formato consente l'installazione e l'accesso semplici ed efficienti al carattere. Tuttavia, se si accede al carattere da un server Web usando il protocollo HTTP, compilare il carattere usando. Formato di file ACF (singolo). Quest'ultima struttura di file consente a uno script di pagine Web di caricare singoli file di animazione, archiviando i dati nella cache dei file del browser dell'utente. Offre un accesso più efficiente sul Web, perché i dati di animazione possono essere scaricati in base alle esigenze, anziché richiedere all'utente di attendere il download dell'intero set di animazioni alla volta. Inoltre, poiché i dati del carattere vengono archiviati nella cache del browser, è possibile recuperare automaticamente lo spazio del file.

Sebbene sia anche possibile scaricare dati di tipo carattere (come un singolo file strutturato o più file) da un server Web e installarli altrove nel computer di un utente, tale metodo richiede le disposizioni di sicurezza per il download e l'installazione. Di conseguenza, l'API dell'agente Microsoft non include il supporto per l'installazione scaricabile di un carattere, ad eccezione della cache del browser. Tuttavia, è comunque possibile supportare questo scenario creando un controllo di installazione personalizzato e distribuendo tale scenario seguendo le convenzioni di sicurezza appropriate. Per ulteriori informazioni, vedere Microsoft Internet Client Software Development Kit.

L'opzione compress consente di specificare se i dati di tipo carattere vengono compressi. In genere, è consigliabile impostare questa opzione per compattare i dati di tipo carattere, anche se la compilazione di un carattere con i dati compressi richiede più tempo.

Quando si compila un carattere, le compilazioni successive saranno più veloci se si compila il carattere nello stesso percorso di directory. L'editor di caratteri verifica e copia automaticamente i file che non sono stati modificati e ricompila i dati che sono stati modificati.

Se l'Editor rileva eventuali errori nel file di caratteri durante la compilazione del carattere, scrive le informazioni in un file di log e visualizza una finestra di messaggio. È possibile scegliere di visualizzare il file di log o ignorarlo e leggerlo in un secondo momento con un editor di testo. Si noti tuttavia che l'editor sovrascriverà il file di log la volta successiva che si compila un file di caratteri.

### <a name="editing-an-existing-character"></a>Modifica di un carattere esistente

Per modificare un carattere esistente, scegliere **Apri** dal menu **file** e selezionare il file di definizione del carattere (. ACD) nella finestra di dialogo risultante e scegliere Apri. Il file viene caricato nell'editor. Si noti che non è possibile caricare file di caratteri compilati (. ACS,. ACF o. ACA) con l'editor.

Poiché il file di definizione del carattere (. ACD) è un file di testo. è anche possibile modificare la definizione di un carattere aprendo il file con un editor di testo o un programma di elaborazione testi. Tuttavia, quando si completano le modifiche, assicurarsi di salvare il file nel formato originale prima di caricarlo nell'editor di caratteri per la compilazione.

 

 




