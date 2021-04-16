---
title: Profilatura di app DirectX
description: Viene illustrato come misurare alcune delle misurazioni più importanti del tempo di prestazioni per un'app DirectX usando gli strumenti XPerf e GPUView forniti come parte di Windows Performance Toolkit.
ms.assetid: 4B2F7273-C9B0-4DD3-B559-6220CDE62129
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0280389d4f8f2161e5e07f8906df7ea0484ad458
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104565626"
---
# <a name="profiling-directx-apps"></a>Profilatura di app DirectX

Viene illustrato come misurare alcune delle misurazioni più importanti del tempo di prestazioni per un'app [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) usando gli strumenti **Xperf** e **GPUView** forniti come parte di Windows Performance Toolkit. Non si tratta di una guida completa per comprendere gli strumenti, piuttosto che per l'analisi delle prestazioni delle app DirectX. Sebbene la maggior parte delle tecniche descritte in questo articolo sia pertinente per tutte le app DirectX, è più rilevante per le app che usano catene di scambio e non per le applicazioni DirectX basate su XAML che usano SIS/VSI e le animazioni XAML. Verranno illustrate le misurazioni del tempo di prestazioni chiave, come acquisire e installare gli strumenti e le tracce di misurazione delle prestazioni e analizzarle per comprendere i colli di bottiglia delle app.

## <a name="about-the-tools"></a>Informazioni sugli strumenti

### <a name="xperf"></a>**XPerf**

**Xperf** è un set di strumenti di analisi delle prestazioni basati su Event Tracing for Windows (ETW) progettati per la misurazione e l'analisi delle prestazioni e dell'utilizzo delle risorse di sistema e delle app dettagliate. A partire da Windows 8, questo strumento da riga di comando ha un'interfaccia utente grafica e viene chiamato Windows Performance Recorder (WPR) e Windows Performance Analyzer (WPA). Altre informazioni su questi strumenti sono disponibili nella pagina Web per [Windows Performance Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)) (WPT): [Windows Performance Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh162945(v=win.10)).

Un ETW raccoglie gli eventi del kernel richiesti e li salva in un file denominato file ETL (Event Trace Log). Questi eventi del kernel forniscono informazioni dettagliate su un'app e sulle caratteristiche di sistema durante l'esecuzione dell'app. I dati vengono raccolti abilitando l'acquisizione della traccia, eseguendo lo scenario di app desiderato che richiede l'analisi, arrestando l'acquisizione che salva i dati in un file ETL. È quindi possibile analizzare il file nello stesso computer o in un computer diverso usando lo strumento da riga di comando **xperf.exe** o lo strumento di analisi della traccia visiva **xperfview.exe**.

### <a name="gpuview"></a>GPUView

**GPUView** è uno strumento di sviluppo per determinare le prestazioni della GPU (Graphics Processing Unit) e della CPU. Esamina le prestazioni per quanto riguarda l'elaborazione del buffer DMA (Direct Memory Access) e tutte le altre elaborazioni video sull'hardware video.

Per le app [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) basate molto sulla GPU, **GPUView** è uno strumento potente per comprendere la relazione tra il lavoro svolto sulla CPU e GPU. Per altre informazioni su **GPUView**, vedere [uso di GPUView](/windows-hardware/drivers/display/using-gpuview).

Analogamente a **Xperf**, una traccia ETW viene innanzitutto eseguita avviando il servizio di traccia, esercitando lo scenario che richiede l'analisi per l'app in considerazione, arrestando il servizio e salvando le informazioni in un file ETL. **GPUView** presenta i dati presenti nel file ETL in formato grafico.

Dopo aver installato lo strumento **GPUView** , è consigliabile leggere l'argomento "visualizzazione principale di **GPUView**" nel menu "Guida **GPUView** ". Contiene informazioni utili su come interpretare l'interfaccia utente di **GPUView** .

## <a name="installing-the-tools"></a>Installazione degli strumenti

Sia **Xperf** che **GPUView** sono inclusi in Windows Performance Toolkit (WPT).

**Xperf** viene fornito come parte di Windows Software Development Kit (SDK) per Windows. [Scaricare il Windows SDK](https://dev.windows.com/downloads).

**GPUView** è disponibile in Windows Assessment and Deployment Kit (Windows ADK). [Scaricare Windows ADK](/windows-hardware/get-started/adk-install).

Dopo l'installazione, è necessario aggiungere le directory che contengono **Xperf** e **GPUView** alla variabile di sistema "Path".

Fare clic sul pulsante Start e digitare "variabili di sistema". Si apre il Finestra Proprietà di sistema. Fare clic su "modifica le variabili di ambiente di sistema". Selezionare "variabili di ambiente" nella finestra di dialogo "proprietà di sistema". La variabile "Path" si trova in "variabili di sistema". Accodare la directory contenente **xperf.exe** e **GPUView.exe** al percorso. Questi file eseguibili si trovano nella directory "Windows Performance Toolkit" all'interno di "Windows Kit". Il percorso predefinito è: **C: \\ Program Files (x86) \\ Windows Kit \\ 10 \\ Windows Performance Toolkit**.

## <a name="performance-time-measurements"></a>Misurazioni del tempo di prestazioni

La maggior parte delle app si aspettano di essere eseguite senza problemi e rispondono all'input dell'utente. Tuttavia, a seconda dello scenario desiderato, un aspetto delle prestazioni potrebbe essere più importante di un altro. Ad esempio, per un'app lettore di notizie in esecuzione su un Tablet PC touch, l'aspetto più importante è quello di visualizzare un singolo articolo alla volta e di eseguire il panning, lo zoom e lo scorrimento dello stesso articolo o di un altro articolo. In questo scenario la possibilità di eseguire il rendering di tutto il contenuto di ogni frame non è necessaria. Tuttavia, la possibilità di scorrere l'articolo in modo semplice su un movimento tocco è estremamente importante.

In un'altra istanza, un gioco o un'app per il rendering video che usa numerose animazioni glitch se i frame vengono eliminati. In questo caso, la possibilità di presentare il contenuto sullo schermo senza interruzione dall'input dell'utente è estremamente importante.

Per comprendere quale parte dell'app è problematica, il primo passaggio consiste nel decidere gli scenari più importanti. Una volta che gli aspetti principali dell'app sono stati riconosciuti e il modo in cui verranno usati, la ricerca di problemi con gli strumenti risulta più semplice.

Di seguito sono riportate alcune delle metriche del tempo di prestazioni più comuni:

### <a name="startup-time"></a>Tempo di avvio

Tempo misurato dall'avvio del processo fino al primo intervento visualizzato sullo schermo. Questa misurazione è più utile quando il sistema è caldo, ovvero la misurazione viene eseguita dopo che l'app viene avviata alcune volte.

### <a name="cpu-time-per-frame"></a>Tempo CPU per fotogramma

Tempo per il quale la CPU elabora attivamente il carico di lavoro dell'app per un frame. Se l'app è in esecuzione senza problemi, tutte le operazioni di elaborazione necessarie per un frame avvengono all'interno di un intervallo di sincronizzazione v. Con la frequenza di aggiornamento del monitoraggio di 60Hz, si tratta di 16ms standard per frame. Se il tempo di CPU/frame è maggiore di 16ms standard, le ottimizzazioni della CPU potrebbero essere necessarie per produrre un'esperienza di app senza problemi.

### <a name="gpu-time-per-frame"></a>Tempo GPU per fotogramma

Tempo per cui GPU elabora attivamente il carico di lavoro dell'app per un frame. Un'app è associata alla GPU quando il tempo impiegato per elaborare i dati di un frame è maggiore di 16ms standard.

La possibilità di comprendere se un'app è associata alla CPU o alla GPU consente di limitare la parte problematica del codice.

## <a name="taking-performance-time-measurement-trace"></a>Esecuzione della traccia di misurazione del tempo di prestazioni

Eseguire questi passaggi per eseguire una traccia:

1.  Aprire una finestra di comando come amministratore.
2.  Chiudere l'app se è già in esecuzione.
3.  Passare alla directory *gpuview* all'interno della cartella Windows Performance Toolkit.
4.  Digitare "log. cmd" per avviare la traccia eventi. Questa opzione consente di registrare gli eventi più interessanti. Altre opzioni disponibili registrano un ambito diverso degli eventi. Per l'istanza "v" o la modalità log dettagliata acquisisce tutti gli eventi che il **GPUView** è in grado di riconoscere.
5.  Avviare l'esempio ed eseguire l'esempio in modo che copra il percorso di prestazioni che è necessario analizzare.
6.  Tornare alla finestra di comando e digitare di nuovo "log. cmd" per arrestare la registrazione.
7.  Viene restituito un file denominato "Merged. etl" nella cartella *gpuview* . È possibile salvare questo file in un altro percorso ed è possibile analizzarlo nello stesso computer o in un altro computer. Per visualizzare i dettagli di acquisizione dello stack, salvare il file di simboli (con estensione pdb) associato all'app.

## <a name="measurements"></a>Misurazioni


> [!Note]  
> Le misure per l'esempio di realizzazione della geometria vengono eseguite in un computer quad core con una scheda grafica DirectX11 integrata. Le misurazioni variano a seconda della configurazione del computer.

 

Questa sezione illustra come misurare i tempi di avvio, della CPU e della GPU per le misurazioni dei frame. È possibile acquisire una traccia delle prestazioni per lo stesso campione nel computer e visualizzare le differenze nelle varie misurazioni.

Per analizzare la traccia in **GPUView**, aprire il file "Merged. ELT" con **GPUView.exe**.

### <a name="startup-time"></a>Tempo di avvio

Il tempo di avvio viene misurato in base al tempo totale impiegato dall'avvio dell'app fino a quando il contenuto non viene visualizzato per la prima volta sullo schermo.

La misurazione del tempo di avvio viene eseguita in modo ottimale attenendosi alla procedura descritta nella sezione precedente con queste varianti:

-   Se la prima volta che si avvia l'app si esegue la misurazione dell'avvio, viene chiamata avvio a freddo. Questa operazione può variare rispetto alle misurazioni eseguite dopo l'avvio dell'app più volte in un periodo di tempo ridotto. Questa operazione viene definita avvio a caldo. A seconda del numero di risorse che un'app crea all'avvio, può esserci una grande differenza tra i due tempi di avvio. A seconda degli obiettivi dell'app, potrebbe essere utile misurare uno o l'altro.
-   Quando si registrano le informazioni sulle prestazioni, terminare l'app non appena il primo frame viene visualizzato sullo schermo.

### <a name="calculating-start-up-time-using-gpuview"></a>Calcolo del tempo di avvio con **GPUView**

1.  In **GPUView** scorrere fino al processo pertinente, in questo caso GeometryRealization.exe.

    ![Screenshot che mostra un esempio di processi in GPUView.](images/profile1.png)

2.  La coda CPU del contesto rappresenta il carico di lavoro grafico accodato all'hardware, ma non necessariamente elaborato dall'hardware. Quando si apre il file di traccia, vengono visualizzati tutti gli eventi registrati tra il momento in cui è stata eseguita la traccia. Per calcolare il tempo di avvio, selezionare l'area di interesse, ingrandire la parte iniziale della coda della CPU del primo contesto, ovvero quella che mostra l'attività, usando Ctrl + Z. Altre informazioni sui controlli **GPUView** sono reperibili nella sezione "Riepilogo dei controlli **GPUView** " del file della Guida di **GPUView** . La figura seguente mostra solo il processo di GeometryRealization.exe ingrandito alla prima parte della coda della CPU del contesto. Il colore della coda della CPU del contesto è indicato dal rettangolo immediatamente sotto la coda e lo stesso pacchetto di dati di colore nella coda Mostra il lavoro della GPU accodato nell'hardware. Il pacchetto del modello di tratteggio nella coda del contesto Mostra il pacchetto presente, che significa che l'app desidera che l'hardware presenti il contenuto sullo schermo.

    ![Screenshot che mostra esempi della "coda di contesto C P U".](images/profile2.png)

3.  Il tempo di avvio è il momento in cui l'app viene avviata per la prima volta (in questo caso il modulo del punto di ingresso del thread UI SHCORE.dll) fino al momento in cui viene visualizzato il contesto (contrassegnato da un pacchetto di tratteggio). Nella figura riportata di seguito viene evidenziata l'area di interesse.

    > [!Note]  
    > Le informazioni effettive presenti sono rappresentate nella coda di capovolgimento e, di conseguenza, il tempo di esecuzione viene esteso fino a quando il pacchetto corrente non viene effettivamente completato nella coda di scorrimento.

     

    La barra di stato completa non è visibile nella figura seguente, che mostra anche il tempo trascorso tra le parti evidenziate. Si tratta del tempo di avvio dell'app. In questo caso per il computer menzionato in precedenza, il risultato è che si trova intorno a 240ms.

    ![Screenshot che mostra le aree di interesse relative al tempo di avvio nella coda del contesto C P U.](images/profile3.png)

### <a name="cpu-and-gpu-time-per-frame"></a>Tempo CPU e GPU per fotogramma

Ci sono alcuni aspetti da considerare durante la misurazione del tempo di CPU. Individuare le aree della traccia in cui è stato esercitato lo scenario da analizzare. Ad esempio, nell'esempio di realizzazione Geometry uno degli scenari che è stato analizzato è la transizione tra il rendering di primitive 2048 e 8192, tutti non realizzati (come in, la geometria non è tassellati ogni frame). La traccia Mostra chiaramente la differenza nell'attività della CPU e della GPU prima e dopo la transizione nel numero di primitive.

Sono stati analizzati due scenari per calcolare il tempo di CPU e GPU per frame. Sono i seguenti.

-   Transizione dal rendering 2048 primitive non realizzate a 8192 primitive non reali.
-   Transizione dal rendering 8192 primitive realizzate a 8192 primitive non reali.

In entrambi i casi, si è notato che la frequenza dei fotogrammi è diminuita drasticamente. Misurazione del tempo di CPU e GPU, la relazione tra i due e altri modelli nella traccia può fornire informazioni utili sulle aree problematiche nell'app.

### <a name="calculating-cpu-and-gpu-time-when-2048-primitives-are-being-rendered-unrealized"></a>Calcolo del tempo di CPU e GPU quando viene eseguito il rendering di 2048 primitive non realizzati

1.  Aprire il file di traccia utilizzando **GPUView.exe**.
2.  Scorrere verso il basso fino al processo di GeometryRealization.exe.
3.  Selezionare un'area per calcolare il tempo della CPU e ingrandirla con CTRL + Z.

    ![Screenshot che mostra un'area selezionata per il calcolo del tempo di C P U nella "coda CPU del contesto".](images/profile4.png)

4.  Mostra le informazioni di sincronizzazione v attivando il tasto F8. Mantenendo lo zoom avanti fino a quando non è facile vedere chiaramente un valore vsync di dati. Le linee blu sono i tempi di sincronizzazione della v. In genere, questi si verificano ogni 16 ms (60 fps), ma se DWM rileva un problema di prestazioni, viene eseguito più lentamente in modo che si verifichino una volta ogni 32 ms (30 fps). Per ottenere un certo tempo, selezionare da una barra blu a quella successiva, quindi osservare il numero di MS riportato nell'angolo in basso a destra della finestra **GPUView** .

    ![Screenshot che mostra un esempio di tempi di sincronizzazione v.](images/profile5.png)

5.  Per misurare il tempo della CPU per fotogramma, misurare la durata del tempo impiegato da tutti i thread interessati dal rendering. Potrebbe essere utile limitare il thread che dovrebbe essere più pertinente dal punto di vista delle prestazioni. Ad esempio, nell'esempio di realizzazione Geometry, il contenuto viene animato ed è necessario eseguirne il rendering sullo schermo di ogni fotogramma che rende il thread UI quello importante. Una volta determinato il thread da esaminare, misurare la lunghezza delle barre in questo thread. La media di alcuni di questi prodotti produce tempo CPU per fotogramma. La figura seguente mostra il tempo impiegato sul thread dell'interfaccia utente. Indica inoltre che questo tempo si adatta perfettamente tra due sincronizzazioni v consecutive, il che significa che sta colpendo 60FPS.

    ![Screenshot che mostra il tempo impiegato nel thread di U I.](images/profile6.png)

    È anche possibile verificare esaminando la coda di scorrimento per l'intervallo di tempo corrispondente che mostra che DWM è in grado di presentare tutti i frame.

    ![Screenshot che mostra un esempio di "coda Flip".](images/profile7.png)

6.  Il tempo della GPU può essere misurato in modo analogo al tempo CPU. Ingrandire l'area pertinente come nel caso di misurazione del tempo di CPU. Misurare la lunghezza delle barre nella coda hardware della GPU con lo stesso colore del colore della coda della CPU del contesto. Fino a quando le barre si adattano all'interno di sincronizzazioni v consecutive, l'app viene eseguita senza problemi in 60FPS.

    ![Screenshot che mostra un esempio di "coda hardware GPU" che visualizza le informazioni che un'app è in esecuzione a 60 F P S.](images/profile8.png)

### <a name="calculating-cpu-and-gpu-time-when-8192-primitives-are-being-rendered-unrealized"></a>Calcolo del tempo di CPU e GPU quando viene eseguito il rendering di 8192 primitive non realizzati

1.  Se si seguono nuovamente gli stessi passaggi, la traccia Mostra che tutto il lavoro della CPU per un frame non rientra tra una sincronizzazione v e la successiva. Ciò significa che l'app è associata alla CPU. Il thread UI sta saturando la CPU.

    ![Screenshot che mostra un esempio del thread dell'interfaccia utente che satura la C P U.](images/profile9.png)

    Esaminando la coda Flip, è inoltre chiaro che DWM non è in grado di presentare tutti i frame.

    ![Screenshot che mostra un esempio di D W M non è in grado di presentare tutti i frame.](images/profile10.png)

2.  Per analizzare dove viene impiegato il tempo, aprire la traccia in **Xperf**. Per analizzare i tempi di avvio in **Xperf**, trovare prima di tutto l'intervallo di tempo in **GPUView**. Puntatore del mouse sulla sinistra dell'intervallo e sulla destra e prendere nota del tempo assoluto visualizzato nella parte inferiore della finestra di **GPUView** . Aprire quindi lo stesso file con estensione ETL in **Xperf** e scorrere verso il basso fino al grafico "CPU Sampling by CPU", fare clic con il pulsante destro del mouse e selezionare "Seleziona intervallo...". In questo modo è possibile digitare nell'intervallo di interesse individuato esaminando la traccia della GPU.

    ![Screenshot che mostra il campionamento C P U per C P U in "analisi prestazioni Windows".](images/profile11.png)

3.  Passare al menu Trace e verificare che "Load symbols" sia selezionato. Passare anche a Trace-> configurare i percorsi dei simboli e digitare il percorso del simbolo dell'app. Un file di simboli contiene informazioni di debug su un eseguibile compilato in un database separato (PDB). Questo file viene comunemente definito PDB. Altre informazioni sui file di simboli sono disponibili qui: [file di simboli](/windows/desktop/Debug/symbol-files). Questo file può trovarsi nella cartella "debug" della directory dell'app.

4.  Per ottenere la suddivisione del tempo impiegato nell'app, fare clic con il pulsante destro del mouse sull'intervallo selezionato nel passaggio precedente e scegliere tabella di riepilogo. Per ottenere una panoramica della quantità di tempo trascorso in ogni dll, deselezionare "stack" dal menu "colonne". Si noti che la colonna "count" indica il numero di campioni inclusi nella dll o nella funzione specificata. Poiché viene eseguita approssimativamente un campione per MS, questo numero può essere usato come ipotesi migliore per quanto tempo viene impiegato in ogni DLL o funzione. Se si seleziona il menu "stack" da colonne, viene fornito il tempo inclusivo trascorso in ogni funzione nel grafico delle chiamate. Ciò consentirà di suddividere ulteriormente i punti problematici.

5.  Le informazioni di analisi dello stack per 2048 primitive non realizzate rivelano che il 30% del tempo di CPU viene impiegato nel processo di realizzazione della geometria. Circa il 36% del tempo viene impiegato nello schema a mosaico geometrico e nel segno.

6.  Le informazioni di analisi dello stack per 8192 primitive non realizzate rivelano che circa il 60% del tempo di CPU (4 core) viene impiegato nella realizzazione della geometria.

    ![Screenshot che mostra le informazioni di analisi dello stack per il tempo C P U.](images/profile12.png)

### <a name="calculating-cpu-time-when-8192-primitives-are-being-rendered-realized"></a>Calcolo del tempo di CPU quando viene eseguito il rendering di 8192 primitive

È chiaro dai profili che l'app è associata alla CPU. Per ridurre il tempo impiegato dalla CPU, le geometrie possono essere create una sola volta e memorizzate nella cache. È possibile eseguire il rendering del contenuto memorizzato nella cache di ogni frame senza incorrere nel costo a mosaico della geometria per fotogramma. Quando si esamina la traccia in **GPUView** per la parte dell'app realizzata, è chiaro che DWM è in grado di presentare tutti i frame e il tempo della CPU è ridotto drasticamente.

![Screenshot che mostra un esempio di traccia in GPUView che mostra D W M è in grado di presentare tutti i frame.](images/profile13.png)

La prima parte del grafico mostra le primitive 8192 ottenute. Il tempo di CPU corrispondente per fotogramma può rientrare in due sincronizzazioni v consecutive. Nella parte successiva del grafico questo non è vero.

Quando si cerca in **Xperf**, la CPU è inattiva per il tempo più lungo con solo il 25% del tempo di CPU dedicato all'app per la realizzazione geometrica.

![schermata gpuview.](images/profile14.png)

## <a name="summary"></a>Riepilogo

Sia **GPUView** che **Xperf** e potenti strumenti per l'analisi delle prestazioni delle app [DirectX](/previous-versions/windows/apps/jj262109(v=win.10)) . Questo articolo è una nozioni di base per l'uso di questi strumenti e per le misure di base delle prestazioni e le caratteristiche delle app. Oltre a comprendere l'utilizzo degli strumenti, è prima di tutto importante comprendere l'app analizzata. Iniziare a trovare le risposte a domande come l'app che si sta tentando di realizzare. Quali thread del sistema sono più importanti? Quali sono i compromessi che è possibile fare? Quando si analizzano le tracce delle prestazioni, iniziare esaminando i punti problematici evidenti. La CPU dell'app o la GPU è associata? L'app è in grado di presentare tutti i frame? Gli strumenti con una conoscenza dell'app possono fornire informazioni molto utili per comprendere, individuare e risolvere i problemi relativi alle prestazioni.

 

 