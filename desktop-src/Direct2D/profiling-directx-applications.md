---
title: Profilatura di app DirectX
description: Illustra come misurare alcune delle misurazioni temporizzazione delle prestazioni più importanti per un'app DirectX usando gli strumenti XPerf e GPUView forniti come parte dell'Windows Performance Toolkit.
ms.assetid: 4B2F7273-C9B0-4DD3-B559-6220CDE62129
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c923f2917dbb8695bcd624f4d998043e7218cf2f976b19b24ab4cff2bc65f398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665429"
---
# <a name="profiling-directx-apps"></a>Profilatura di app DirectX

Questo articolo illustra come misurare alcune delle misurazioni temporizzazione delle prestazioni più importanti per un'app [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) usando gli strumenti **XPerf** e **GPUView** forniti come parte dell'Windows Performance Toolkit. Questa non è una guida completa per comprendere gli strumenti, ma piuttosto la loro applicabilità specifica per l'analisi delle prestazioni delle app DirectX. Sebbene la maggior parte delle tecniche descritte in questo documento sia pertinente per tutte le app DirectX, è più rilevante per le app che usano catene di scambio e non per le applicazioni DirectX create su XAML che usano SIS/VSIS e animazioni XAML. Vengono ora analizzate le misurazioni chiave del tempo delle prestazioni, viene illustrato come acquisire e installare gli strumenti, acquisire tracce di misurazione delle prestazioni e quindi analizzarle per comprendere i colli di bottiglia delle app.

## <a name="about-the-tools"></a>Informazioni sugli strumenti

### <a name="xperf"></a>**XPerf**

**XPerf** è un set di strumenti di analisi delle prestazioni basato su Event Tracing for Windows (ETW) progettato per misurare e analizzare le prestazioni dettagliate del sistema e delle app e l'utilizzo delle risorse. A partire Windows 8 questo strumento da riga di comando ha un'interfaccia utente grafica e viene chiamato Windows Performance Recorder (WPR) e Windows analizzatore prestazioni (WPA). Per altre informazioni su questi strumenti, vedere la pagina Web [Windows Performance Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)) (WPT): Windows Performance [Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)).

Un ETW raccoglie gli eventi del kernel richiesti e li salva in un file denominato file di log di traccia eventi (ETL). Questi eventi del kernel forniscono informazioni dettagliate sulle caratteristiche di un'app e di sistema durante l'esecuzione dell'app. I dati vengono raccolti abilitando l'acquisizione della traccia, eseguendo lo scenario di app desiderato che richiede l'analisi, arrestando l'acquisizione che salva i dati in un file ETL. È quindi possibile analizzare il file nello stesso computer o in un computer diverso usando lo strumento da riga di comando **xperf.exe** o lo strumento di analisi della traccia **visivaxperfview.exe**.

### <a name="gpuview"></a>GPUView

**GPUView è** uno strumento di sviluppo per determinare le prestazioni dell'unità di elaborazione grafica (GPU) e della CPU. Esamina le prestazioni per quanto riguarda l'elaborazione del buffer DMA (Direct Memory Access) e tutte le altre elaborazioni video nell'hardware video.

Per [le app DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) che si basano molto sulla GPU, **GPUView** è uno strumento potente per comprendere la relazione tra il lavoro svolto sulla CPU e la GPU. Per altre informazioni su **GPUView,** vedere [Uso di GPUView.](/windows-hardware/drivers/display/using-gpuview)

Analogamente a **XPerf,** per prima cosa viene eseguita una traccia ETW avviando il servizio di traccia, esercitando lo scenario che richiede l'analisi per l'app in esame, arrestando il servizio e salvando le informazioni in un file ETL. **GPUView** presenta i dati presenti nel file ETL in formato grafico.

Dopo aver installato lo strumento **GPUView,** è consigliabile leggere l'argomento "Visualizzazione principale di **GPUView"** nel menu "Guida di **GPUView".** Contiene informazioni utili su come interpretare l'interfaccia utente **GPUView.**

## <a name="installing-the-tools"></a>Installazione degli strumenti

Sia **XPerf** che **GPUView** sono inclusi nella Windows Performance Toolkit (WPT).

**XPerf** viene fornito come parte di Windows Software Development Kit (SDK) per Windows. [Scaricare Windows SDK](https://dev.windows.com/downloads).

**GPUView** è disponibile in Windows Assessment and Deployment Kit (Windows ADK). [Scaricare il Windows ADK](/windows-hardware/get-started/adk-install).

Dopo l'installazione, è necessario aggiungere le directory che contengono **XPerf** e **GPUView** alla variabile di sistema "Path".

Fare clic pulsante Start e digitare "Variabili di sistema". Verrà visualizzata Finestra Proprietà sistema. Fare clic su "Modifica le variabili di ambiente di sistema". Selezionare "Variabili di ambiente" nella finestra di dialogo "Proprietà di sistema". La variabile "Path" si trova in "Variabili di sistema". Aggiungere la directory contenente **xperf.exe** **eGPUView.exe** al percorso. Questi file eseguibili si trovano nella directory "Windows Performance Toolkit" all'interno di "Windows Kit". Il percorso predefinito è: **C: \\ Programmi (x86) \\ Windows \\ Kits 10 \\** Windows Prestazioni Toolkit .

## <a name="performance-time-measurements"></a>Misurazioni del tempo delle prestazioni

La maggior parte delle app prevede di funzionare senza problemi e di rispondere all'input dell'utente. Tuttavia, a seconda dello scenario desiderato, un aspetto delle prestazioni potrebbe essere più importante di un altro. Ad esempio, per un'app di lettura notizie in esecuzione in un tablet PC con tocco, l'aspetto più importante è visualizzare un singolo articolo alla volta e scorrere lo stesso articolo o un articolo diverso. In questo scenario non è necessaria la possibilità di eseguire il rendering di tutto il contenuto di ogni frame. Tuttavia, la possibilità di scorrere l'articolo senza problemi su un movimento tocco è estremamente importante.

In un'altra istanza, un gioco o un'app per il rendering video che usa molti difetti di animazione se i fotogrammi vengono eliminati. In questo caso, la possibilità di presentare contenuto sullo schermo senza interuption dall'input dell'utente è estremamente importante.

Per comprendere quale parte dell'app è problematica, il primo passaggio consiste nel decidere gli scenari più importanti. Una volta compresi gli aspetti principali dell'app e come verranno esercitati, la ricerca di problemi con gli strumenti diventa più semplice.

Di seguito sono riportati alcuni dei dati più comuni relativi al tempo delle prestazioni:

### <a name="startup-time"></a>Fase di avvio

Tempo misurato dall'avvio del processo alla prima presentazione che viene visualizzata sullo schermo. Questa misurazione è più utile quando il sistema è caldo, ovvero la misurazione viene eseguita dopo l'avvio dell'app alcune volte.

### <a name="cpu-time-per-frame"></a>Tempo CPU per frame

Tempo per cui la CPU elabora attivamente il carico di lavoro dell'app per un frame. Se l'app viene eseguita senza problemi, tutta l'elaborazione necessaria per un frame viene eseguita entro un intervallo di sincronizzazione v. Con la frequenza di aggiornamento del monitoraggio di 60 Hz, si tratta di 16 ms per frame. Se il tempo/frame della CPU è maggiore di 16 ms, potrebbero essere necessarie ottimizzazioni della CPU per produrre un'esperienza di app senza problemi.

### <a name="gpu-time-per-frame"></a>Tempo GPU per fotogramma

Tempo per cui la GPU elabora attivamente il carico di lavoro dell'app per un frame. Un'app è associata a GPU quando il tempo impiegato per elaborare un frame di dati è superiore a 16 ms.

La possibilità di comprendere se un'app è associata a CPU o GPU restringe la parte problematica del codice.

## <a name="taking-performance-time-measurement-trace"></a>Analisi della misurazione del tempo delle prestazioni

Per eseguire una traccia, seguire questa procedura:

1.  Aprire una finestra di comando come amministratore.
2.  Chiudere l'app se è già in esecuzione.
3.  Passare alla directory *gpuview* all'interno della cartella Windows Performance Toolkit.
4.  Digitare "log.cmd" per avviare la traccia eventi. Questa opzione registra gli eventi più interessanti. Altre opzioni disponibili registrano un ambito diverso degli eventi. Ad esempio, la modalità di log dettagliata o 'v' acquisisce tutti gli eventi che **GPUView** è in grado di riconoscere.
5.  Avviare l'esempio ed eseguire l'esempio in modo da coprire il percorso delle prestazioni che è necessario analizzare.
6.  Tornare alle finestre dei comandi e digitare di nuovo "log.cmd" per arrestare la registrazione.
7.  Verrà restituito un file denominato "merged.etl" nella *cartella gpuview.* È possibile salvare il file in un'altra posizione ed analizzarlo nello stesso computer o in un altro computer. Per visualizzare i dettagli dell'acquisizione dello stack, salvare il file di simboli (con estensione pdb) associato all'app.

## <a name="measurements"></a>Misurazioni


> [!Note]  
> Le misurazioni per il campione di realizzazione della geometria vengono prese in un computer Quad Core con una scheda grafica DirectX11 integrata. Le misurazioni variano a seconda della configurazione del computer.

 

Questa sezione illustra come misurare il tempo di avvio, la CPU e le misurazioni del tempo GPU per fotogramma. È possibile acquisire una traccia delle prestazioni per lo stesso esempio nel computer e visualizzare le differenze nelle diverse misurazioni.

Per analizzare la traccia in **GPUView,** aprire il file "merged.elt" **usando** GPUView.exe.

### <a name="startup-time"></a>Fase di avvio

Il tempo di avvio viene misurato in base al tempo totale trascorso dall'avvio dell'app fino alla prima visualizzazione del contenuto sullo schermo.

La misurazione del tempo di avvio è ottimale seguendo i passaggi elencati nella sezione precedente con queste variazioni:

-   Se si prendono le misurazioni di avvio la prima volta che si avvia l'app, si chiama avvio a freddo. Questo può variare dalle misurazioni prese dopo l'avvio dell'app più volte in un breve periodo di tempo. Questa operazione è denominata avvio a caldo. A seconda del numero di risorse create da un'app all'avvio, può esserci una grande differenza tra i due tempi di avvio. A seconda degli obiettivi dell'app, potrebbe essere preferibile misurare uno o l'altro.
-   Quando si registrano le informazioni sulle prestazioni, terminare l'app non appena viene visualizzato il primo frame sullo schermo.

### <a name="calculating-start-up-time-using-gpuview"></a>Calcolo del tempo di avvio tramite **GPUView**

1.  In **GPUView** scorrere verso il basso fino al processo pertinente, in questo caso GeometryRealization.exe.

    ![Screenshot che mostra un esempio di processi in GPUView.](images/profile1.png)

2.  La coda della CPU di contesto rappresenta il carico di lavoro grafico accodato all'hardware, ma non viene necessariamente elaborato dall'hardware. Quando il file di traccia viene aperto, vengono visualizzati tutti gli eventi registrati tra il momento in cui è stata eseguita la traccia. Per calcolare il tempo di avvio, selezionare l'area di interesse, ingrandire la parte iniziale della prima coda CPU di contesto (questa è quella che mostra l'attività) usando CTRL+Z. Altre informazioni sui **controlli GPUView** sono disponibili nella sezione "Riepilogo dei controlli **GPUView"** della Guida di **GPUView.** La figura seguente mostra solo il GeometryRealization.exe processo ingrandito fino alla prima parte della coda della CPU di contesto. Il colore della coda CPU di contesto è indicato dal rettangolo proprio sotto la coda e gli stessi pacchetti di dati a colori nella coda mostrano il lavoro GPU in coda sull'hardware. Il pacchetto del modello di tratteggio nella coda di contesto mostra il pacchetto corrente, il che significa che l'app vuole che l'hardware presenti il contenuto sullo schermo.

    ![Screenshot che mostra esempi di "Context C P U Queue".](images/profile2.png)

3.  Il tempo di avvio è il momento in cui l'app viene avviata per la prima volta (in questo caso il modulo del punto di ingresso del thread dell'interfaccia utente SHCORE.dll) fino al momento in cui il contesto viene visualizzato per la prima volta (contrassegnato da un pacchetto tratteggiato). La figura qui evidenzia l'area di interesse.

    > [!Note]  
    > Le informazioni presenti effettive sono rappresentate nella coda di capovolgimento e quindi il tempo necessario viene esteso fino al completamento effettivo del pacchetto corrente nella coda di capovolgimento.

     

    La barra di stato completa non è visibile nella figura seguente che mostra anche il tempo trascorso tra le parti evidenziate. Questo è il momento di avvio dell'app. In questo caso per il computer indicato in precedenza, si è scoperto che si tratta di circa 240 ms.

    ![Screenshot che mostra le aree di interesse relative al tempo di avvio nella "coda di contesto C P U".](images/profile3.png)

### <a name="cpu-and-gpu-time-per-frame"></a>Tempo CPU e GPU per fotogramma

Quando si misura il tempo della CPU, è necessario valutare alcuni aspetti. Cercare le aree nella traccia in cui è stato esercitato lo scenario da analizzare. Ad esempio, nell'esempio di realizzazione della geometria uno degli scenari analizzati è la transizione tra il rendering delle primitive 2048 e 8192, tutte non realizzati (come in, la geometria non viene suddivisa a tessella per ogni fotogramma). La traccia mostra chiaramente la differenza nell'attività cpu e GPU prima e dopo la transizione nel numero di primitive.

Vengono analizzati due scenari per calcolare il tempo di CPU e GPU per ogni fotogramma. Sono i seguenti.

-   Transizione dal rendering di primitive non irrealizzate 2048 a 8192 primitive non irrealizzate.
-   Transizione da primitive realizzate 8192 per il rendering a 8192 primitive non realizzate.

In entrambi i casi, è stato osservato che la frequenza dei fotogrammi è diminuita drasticamente. La misurazione del tempo di CPU e GPU, la relazione tra i due e alcuni altri modelli nella traccia può fornire informazioni utili sulle aree problematiche nell'app.

### <a name="calculating-cpu-and-gpu-time-when-2048-primitives-are-being-rendered-unrealized"></a>Calcolo del tempo di CPU e GPU quando viene eseguito il rendering non eseguito delle primitive 2048

1.  Aprire il file di traccia **usandoGPUView.exe**.
2.  Scorrere verso il basso fino GeometryRealization.exe processo.
3.  Selezionare un'area per il calcolo del tempo cpu e ingrandire l'area usando CTRL+Z.

    ![Screenshot che mostra un'area selezionata per il calcolo del tempo C P U nella 'Coda CPU contesto'.](images/profile4.png)

4.  Visualizzare le informazioni di sincronizzazione v tramite il togging tra F8. Mantenendo lo zoom avanti fino a quando non è facile vedere chiaramente un valore vsync dei dati. Le righe blu sono il punto in cui viene sincronizzata la v. In genere, si verificano una volta ogni 16 ms (60 fps), ma se DWM riscontra un problema di prestazioni, viene eseguito più lentamente in modo che si verifichino una volta ogni 32 ms (30 fps). Per avere un'idea del tempo, selezionare da una barra blu alla successiva e quindi esaminare il numero di ms segnalati nell'angolo inferiore destro della finestra **GPUView.**

    ![Screenshot che mostra un esempio di tempi di sincronizzazione v.](images/profile5.png)

5.  Per misurare il tempo di CPU per fotogramma, misurare il tempo impiegato da tutti i thread coinvolti nel rendering. Potrebbe essere utile restringere il thread che dovrebbe essere più pertinente dal punto di vista delle prestazioni. Ad esempio, nell'esempio di realizzazione della geometria, il contenuto sta animando e deve essere sottoposto a rendering sullo schermo ogni fotogramma rendendo il thread dell'interfaccia utente quello importante. Dopo aver determinato il thread da esaminare, misurare la lunghezza delle barre su questo thread. La media di alcuni di questi risultati genera tempo di CPU per frame. La figura seguente mostra il tempo impiegato nel thread dell'interfaccia utente. Mostra anche che questa volta si adatta bene tra due sincronizzazioni v consecutive, il che significa che sta toccando 60 FPS.

    ![Screenshot che mostra il tempo impiegato nel thread U I.](images/profile6.png)

    È anche possibile verificare esaminando la coda di capovolgimento per l'intervallo di tempo corrispondente che mostra che DWM è in grado di presentare ogni fotogramma.

    ![Screenshot che mostra un esempio di "Flip Queue".](images/profile7.png)

6.  Il tempo gpu può essere misurato nello stesso modo del tempo CPU. Ingrandire l'area pertinente come nel caso della misurazione del tempo cpu. Misurare la lunghezza delle barre nella coda hardware GPU con lo stesso colore della coda CPU del contesto. Purché le barre si adattino a sincronizzazioni v consecutive, l'app viene eseguita senza problemi a 60 FPS.

    ![Screenshot che mostra un esempio della "coda hardware GPU" che visualizza informazioni sull'esecuzione di un'app a 60 F P S.](images/profile8.png)

### <a name="calculating-cpu-and-gpu-time-when-8192-primitives-are-being-rendered-unrealized"></a>Calcolo del tempo di CPU e GPU quando viene eseguito il rendering non eseguito di 8192 primitive

1.  Se si seguono di nuovo gli stessi passaggi, la traccia mostra che tutto il lavoro della CPU per un frame non rientra tra una sincronizzazione v e la successiva. Ciò significa che l'app è associata alla CPU. Il thread dell'interfaccia utente sta saturando la CPU.

    ![Screenshot che mostra un esempio del thread dell'interfaccia utente che satura C P U.](images/profile9.png)

    Osservando la coda di capovolgimento, è anche chiaro che DWM non è in grado di presentare ogni fotogramma.

    ![Screenshot che mostra un esempio di D W M che non è in grado di presentare ogni frame.](images/profile10.png)

2.  Per analizzare dove viene impiegato il tempo, aprire la traccia in **XPerf**. Per analizzare il tempo di avvio in **XPerf,** trovare prima l'intervallo di tempo in **GPUView**. Posizionare il puntatore del mouse a sinistra dell'intervallo e a destra e prendere nota del tempo assoluto visualizzato nella parte inferiore della **finestra GPUView.** Aprire quindi lo stesso file con estensione etl in **XPerf** e scorrere verso il basso fino al grafico "Campionamento CPU per CPU", fare clic con il pulsante destro del mouse e selezionare "Seleziona intervallo..." Ciò consente di digitare l'intervallo di interesse individuato esaminando la traccia GPU.

    ![Screenshot che mostra il campionamento C P U by C P U in "Windows Performance Analysis".](images/profile11.png)

3.  Passare al menu Traccia e verificare che l'opzione "Carica simboli" sia selezionata. Passare anche a Trace -> Configure Symbol Paths (Configura percorsi simboli) e digitare il percorso del simbolo dell'app. Un file di simboli contiene informazioni di debug su un eseguibile compilato in un database separato (con estensione pdb). Questo file viene comunemente definito PDB. Altre informazioni sui file di simboli sono disponibili qui: [File di simboli](/windows/desktop/Debug/symbol-files). Questo file può trovarsi nella cartella "Debug" della directory dell'app.

4.  Per ottenere la suddivisione del tempo trascorso nell'app, fare clic con il pulsante destro del mouse sull'intervallo selezionato nel passaggio precedente e scegliere Tabella di riepilogo. Per ottenere una panoramica del tempo impiegato in ogni DLL, deselezionare "Stack" dal menu "Colonne". Si noti che la colonna "Count" mostra il numero di esempi all'interno della dll/funzione specificata. Poiché viene preso circa un campione per ms, questo numero può essere usato come ipotesi migliore per quanto tempo viene impiegato in ogni dll/funzione. Se si controlla "Stack" dal menu Colonne, si avrà il tempo inclusivo impiegato in ogni funzione nel grafico delle chiamate. Ciò consente di suddividere ulteriormente i punti problematici.

5.  Le informazioni di traccia dello stack per primitive non realizzati 2048 rivelano che il 30% del tempo della CPU viene impiegato nel processo di realizzazione della geometria. Di questo circa il 36% del tempo viene dedicato alla tessellazione e alla ghiottatura geometrica.

6.  Le informazioni di traccia dello stack per 8192 primitive non realizzati rivelano che circa il 60% del tempo cpu (4 core) viene impiegato nella realizzazione della geometria.

    ![Screenshot che mostra le informazioni sull'analisi dello stack per l'ora C P U.](images/profile12.png)

### <a name="calculating-cpu-time-when-8192-primitives-are-being-rendered-realized"></a>Calcolo del tempo di CPU quando viene eseguito il rendering di 8192 primitive

Dai profili è chiaro che l'app è associata alla CPU. Per ridurre il tempo impiegato dalla CPU, le geometrie possono essere create una sola volta e memorizzate nella cache. È possibile eseguire il rendering del contenuto memorizzato nella cache in ogni frame senza incorrere nel costo della sezione geometry per frame. Quando si esamina la traccia in **GPUView** per la parte realizzata dell'app, è chiaro che DWM è in grado di presentare ogni frame e che il tempo di CPU è drasticamente ridotto.

![Screenshot che mostra un esempio di traccia in GPUView che mostra che D W M è in grado di presentare ogni frame.](images/profile13.png)

La prima parte del grafico mostra 8192 primitive realizzate. Il tempo di CPU corrispondente per frame può essere compreso in due sincronizzazioni v consecutive. Nella parte successiva del grafico questo non è vero.

Se si **esamina XPerf,** la CPU è inattiva per il tempo più lungo, con solo circa il 25% del tempo cpu impiegato nell'app di realizzazione della geometria.

![Screenshot di gpuview.](images/profile14.png)

## <a name="summary"></a>Riepilogo

**GpUView** e **XPerf** e potenti strumenti per l'analisi delle prestazioni [delle app DirectX.](/previous-versions/windows/apps/jj262109(v=win.10)) Questo articolo è un elemento di base per l'uso di questi strumenti e la comprensione delle misurazioni delle prestazioni di base e delle caratteristiche dell'app. Oltre a comprendere l'uso degli strumenti, è prima di tutto importante comprendere l'app analizzata. Iniziare a trovare risposte a domande come cosa sta tentando di ottenere l'app? Quali thread del sistema sono più importanti? Quali compromessi si è disposti a realizzare? Quando si analizzano le tracce delle prestazioni, iniziare esaminando le posizioni problematiche ovvie. La CPU o la GPU dell'app è associata? L'app è in grado di presentare ogni frame? Gli strumenti insieme alla comprensione dell'app possono fornire informazioni molto utili per comprendere, trovare e risolvere infine i problemi di prestazioni.

 

 