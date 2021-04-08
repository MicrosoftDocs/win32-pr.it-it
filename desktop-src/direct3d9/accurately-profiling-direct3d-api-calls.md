---
description: Quando si dispone di un'applicazione Microsoft Direct3D funzionale e si desidera migliorare le prestazioni, in genere si usa uno strumento di profilatura fuori programma o una tecnica di misurazione personalizzata per misurare il tempo necessario per eseguire una o più chiamate di Application Programming Interface (API). Se questa operazione è stata eseguita ma si ricevono risultati temporali che variano da una sequenza di rendering a quella successiva o si eseguono ipotesi che non mantengono i risultati effettivi dell'esperimento, le informazioni seguenti possono essere utili per comprendere il motivo.
ms.assetid: f969be42-d541-4e8d-aec4-eb9508bcc7cf
title: Profilatura precisa delle chiamate API Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdb6d60fcc1b3ace4112dbf7028d91e2c9c8b345
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748738"
---
# <a name="accurately-profiling-direct3d-api-calls-direct3d-9"></a>Profilatura precisa delle chiamate API Direct3D (Direct3D 9)

-   [Il profiling accurato di Direct3D è difficile](#accurately-profiling-direct3d-is-difficult)
-   [Come profilare accuratamente una sequenza di rendering Direct3D](#how-to-accurately-profile-a-direct3d-render-sequence)
-   [Profilatura delle modifiche dello stato Direct3D](#profiling-direct3d-state-changes)
-   [Summary](#summary)
-   [Appendice](#appendix)

Quando si dispone di un'applicazione Microsoft Direct3D funzionale e si desidera migliorare le prestazioni, in genere si usa uno strumento di profilatura fuori programma o una tecnica di misurazione personalizzata per misurare il tempo necessario per eseguire una o più chiamate di Application Programming Interface (API). Se questa operazione è stata eseguita ma si ricevono risultati temporali che variano da una sequenza di rendering a quella successiva o si eseguono ipotesi che non mantengono i risultati effettivi dell'esperimento, le informazioni seguenti possono essere utili per comprendere il motivo.

Le informazioni fornite in questo articolo si basano sul presupposto che l'utente abbia familiarità e abbia esperienza con quanto segue:

-   Programmazione C/C++
-   Programmazione dell'API Direct3D
-   Misurazione della temporizzazione delle API
-   Scheda video e driver software
-   Possibili risultati inspiegabili della precedente esperienza di profilatura

## <a name="accurately-profiling-direct3d-is-difficult"></a>Il profiling accurato di Direct3D è difficile

Un profiler segnala la quantità di tempo impiegato in ogni chiamata API. Questa operazione consente di migliorare le prestazioni individuando e ottimizzando le aree sensibili. Esistono diversi tipi di Profiler e tecniche di profilatura.

-   Un profiler di campionamento si trova in una fase di inattività, riattivando a intervalli specifici di esempio (o per registrare) le funzioni in esecuzione. Restituisce la percentuale di tempo trascorso in ogni chiamata. In genere, un profiler di campionamento non è molto invasivo per l'applicazione e ha un impatto minimo sul sovraccarico per l'applicazione.
-   Un profiler di strumentazione misura il tempo effettivo necessario per la restituzione di una chiamata. Richiede la compilazione di delimitatori di avvio e di arresto in un'applicazione. Un profiler di strumentazione è relativamente più invasive per un'applicazione rispetto a un profiler di campionamento.
-   È anche possibile usare una tecnica di profilatura personalizzata con un timer a prestazioni elevate. Questa operazione produce risultati molto simili a quelli di un profiler di strumentazione.

Il tipo di Profiler o la tecnica di profilatura utilizzata fa solo parte della richiesta di generazione di misurazioni accurate.

La profilatura offre risposte che consentono di ottenere un budget per le prestazioni. Si supponga, ad esempio, che un'API chiami la media di 1000 cicli di clock da eseguire. È possibile dichiarare alcune conclusioni sulle prestazioni, come le seguenti:

-   Una CPU a 2 GHz, che dedica il 50% del rendering del tempo, è limitata alla chiamata a questa API 1 milione volte al secondo.
-   Per ottenere 30 fotogrammi al secondo, non è possibile chiamare l'API più di 33.000 volte per frame.
-   È possibile eseguire il rendering solo di 3.3 K oggetti per fotogramma (presupponendo 10 di queste chiamate API per la sequenza di rendering di ogni oggetto).

In altre parole, se si dispone di tempo sufficiente per ogni chiamata API, è possibile rispondere a una domanda di budget, ad esempio il numero di primitive di cui è possibile eseguire il rendering in modo interattivo. Tuttavia, i numeri non elaborati restituiti da un profiler di strumentazione non rispondono in modo accurato alle domande di budget. Ciò è dovuto al fatto che la pipeline grafica presenta problemi di progettazione complessi, ad esempio il numero di componenti che devono funzionare, il numero di processori che controllano il flusso di lavoro tra i componenti e le strategie di ottimizzazione implementate in fase di esecuzione e in un driver progettato per rendere la pipeline più efficiente.

### <a name="each-api-call-goes-through-several-components"></a>Ogni chiamata API passa attraverso diversi componenti

Ogni chiamata viene elaborata da diversi componenti dal punto di forza dell'applicazione alla scheda video. Si consideri, ad esempio, la sequenza di rendering seguente che contiene due chiamate per il disegno di un singolo triangolo:


```
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
```



Il diagramma concettuale seguente mostra i diversi componenti attraverso i quali le chiamate devono essere superate.

![diagramma dei componenti grafici che passano dalle chiamate API](images/microbenchmarkinstructionflow2.png)

L'applicazione richiama Direct3D che controlla la scena, gestisce le interazioni dell'utente e determina il modo in cui viene eseguito il rendering. Tutte queste operazioni vengono specificate nella sequenza di rendering, che viene inviata al runtime tramite chiamate API Direct3D. La sequenza di rendering è virtualmente indipendente dall'hardware, ovvero le chiamate API sono indipendenti dall'hardware, ma un'applicazione è in grado di conoscere le funzionalità supportate da una scheda video.

Il runtime converte queste chiamate in un formato indipendente dal dispositivo. Il runtime gestisce tutte le comunicazioni tra l'applicazione e il driver, in modo che un'applicazione venga eseguita su più componenti hardware compatibili (a seconda delle funzionalità necessarie). Quando si misura una chiamata di funzione, un profiler di strumentazione misura il tempo trascorso in una funzione e il tempo necessario per la restituzione della funzione. Una limitazione di un profiler di strumentazione è che potrebbe non includere il tempo impiegato da un driver per inviare il lavoro risultante alla scheda video e il tempo necessario alla scheda video per elaborare il lavoro. In altre parole, un profiler di strumentazione fuori piano non riesce a attribuire tutto il lavoro associato a ogni chiamata di funzione.

Il driver software utilizza informazioni specifiche dell'hardware sulla scheda video per convertire i comandi indipendenti dal dispositivo in una sequenza di comandi di schede video. I driver possono anche ottimizzare la sequenza di comandi inviati alla scheda video, in modo che il rendering sulla scheda video venga eseguito in modo efficiente. Queste ottimizzazioni possono causare problemi di profilatura perché la quantità di lavoro eseguita non corrisponde a quanto sembra (potrebbe essere necessario comprendere le ottimizzazioni da tenere in considerazione). Il driver restituisce in genere il controllo al runtime prima che la scheda video abbia terminato l'elaborazione di tutti i comandi.

La scheda video esegue la maggior parte del rendering combinando i dati dai buffer dei vertici e degli indici, le trame, le informazioni sullo stato di rendering e i comandi grafici. Quando la scheda video termina il rendering, il lavoro creato dalla sequenza di rendering è completo.

Ogni chiamata all'API Direct3D deve essere elaborata da ogni componente (il runtime, il driver e la scheda video) per eseguire il rendering di qualsiasi elemento.

### <a name="there-is-more-than-one-processor-controlling-the-components"></a>È presente più di un processore che controlla i componenti

La relazione tra questi componenti è ancora più complessa, poiché l'applicazione, il runtime e il driver sono controllati da un processore e la scheda video è controllata da un processore separato. Il diagramma seguente mostra due tipi di processori: un'unità di elaborazione centrale (CPU) e una GPU (Graphics Processing Unit).

![diagramma di una CPU e di una GPU e dei relativi componenti](images/microbenchmarkprocessors.png)

I sistemi PC hanno almeno una CPU e una GPU, ma possono avere più di uno dei due o entrambi. Le CPU si trovano sulla scheda madre e le GPU si trovano sulla scheda madre o sulla scheda video. La velocità della CPU è determinata da un chip di clock sulla scheda madre e la velocità della GPU è determinata da un chip di clock separato. Il clock della CPU controlla la velocità del lavoro eseguito dall'applicazione, dal runtime e dal driver. L'applicazione invia il lavoro alla GPU tramite il runtime e il driver.

La CPU e la GPU vengono in genere eseguite a velocità diverse, indipendenti l'una dall'altra. La GPU può rispondere al lavoro non appena il lavoro è disponibile (presupponendo che la GPU abbia terminato l'elaborazione del lavoro precedente). Il lavoro della GPU viene eseguito in parallelo con il lavoro della CPU evidenziato dalla linea curva nella figura precedente. Un profiler in genere misura le prestazioni della CPU, non della GPU. Ciò rende difficoltosa la profilatura, perché le misurazioni eseguite da un profiler di strumentazione includono il tempo della CPU, ma potrebbero non includere il tempo della GPU.

Lo scopo della GPU è quello di non caricare l'elaborazione dalla CPU a un processore appositamente progettato per il lavoro della grafica. Sulle schede video moderne la GPU sostituisce gran parte del lavoro di trasformazione e illuminazione nella pipeline dalla CPU alla GPU. Questo riduce notevolmente il carico di lavoro della CPU, lasciando più cicli di CPU disponibili per altre elaborazioni. Per ottimizzare un'applicazione grafica per le prestazioni ottimali, è necessario misurare le prestazioni della CPU e della GPU e bilanciare il lavoro tra i due tipi di processori.

In questo documento non vengono trattati gli argomenti relativi alla misurazione delle prestazioni della GPU o al bilanciamento del lavoro tra la CPU e la GPU. Per comprendere meglio le prestazioni di una GPU (o una scheda video specifica), visitare il sito Web del fornitore per cercare ulteriori informazioni sulle prestazioni della GPU. Al contrario, questo documento è incentrato sul lavoro svolto dal runtime e dal driver riducendo il lavoro della GPU a una quantità trascurabile. Questo è in parte basato sull'esperienza che le applicazioni che hanno riscontrato problemi di prestazioni sono in genere limitate alla CPU.

### <a name="runtime-and-driver-optimizations-can-mask-api-measurements"></a>Le ottimizzazioni di runtime e driver possono mascherare le misurazioni API

Nel runtime è incorporata un'ottimizzazione delle prestazioni che può sovraccaricare la misurazione di una singola chiamata. Ecco uno scenario di esempio che illustra questo problema. Si consideri la seguente sequenza di rendering:


```
  BeginScene();
    ...
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
    ...
  EndScene();
  Present();
```



Esempio 1: sequenza di rendering semplice

Esaminando i risultati per le due chiamate nella sequenza di rendering, un profiler di strumentazione può restituire risultati simili ai seguenti:


```
Number of cycles for SetTexture       : 100
Number of cycles for DrawPrimitive    : 950,500
```



Il profiler restituisce il numero di cicli della CPU necessari per elaborare il lavoro associato a ogni chiamata. tenere presente che la GPU non è inclusa in questi numeri perché la GPU non ha ancora iniziato a usare questi comandi. Poiché [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) richiedeva quasi un milione di cicli per l'elaborazione, è possibile concludere che non è molto efficiente. Tuttavia, si noterà presto il motivo per cui questa conclusione non è corretta e come è possibile generare risultati che possono essere utilizzati per il budget.

### <a name="measuring-state-changes-requires-careful-render-sequences"></a>La misurazione delle modifiche di stato richiede un'attenta sequenza di rendering

Tutte le chiamate diverse da [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)o [**Clear**](/windows/desktop/api) (ad esempio, [**setrame**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), [**SetVertexDeclaration**](/windows/desktop/api)e [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) producono una modifica dello stato. Ogni modifica di stato imposta lo stato della pipeline che controlla il modo in cui verrà eseguito il rendering.

Le ottimizzazioni in fase di esecuzione e/o il driver sono progettate per velocizzare il rendering riducendo la quantità di lavoro necessario. Di seguito sono riportate alcune ottimizzazioni di modifica dello stato che potrebbero inquinare le medie del profilo:

-   Un driver (o il Runtime) può salvare una modifica di stato come stato locale. Poiché il driver potrebbe funzionare in un algoritmo "Lazy" (posticipando il lavoro fino a quando non è assolutamente necessario), il lavoro associato ad alcune modifiche di stato potrebbe essere ritardato.
-   Il runtime (o un driver) può rimuovere le modifiche dello stato ottimizzando. Un esempio potrebbe essere quello di rimuovere una modifica di stato ridondante che disabilita l'illuminazione perché l'illuminazione è stata precedentemente disabilitata.

Non esiste un modo infallibile per esaminare una sequenza di rendering e concludere quali modifiche di stato consentiranno di impostare un bit dirty e rinviare il lavoro oppure verranno semplicemente rimosse dall'ottimizzazione. Anche se è possibile identificare le modifiche dello stato ottimizzate nel runtime o nel driver odierno, è probabile che il runtime o il driver di domani venga aggiornato. Non si conosce neanche facilmente lo stato precedente, quindi è difficile identificare le modifiche di stato ridondanti. L'unico modo per verificare il costo di una modifica di stato consiste nel misurare la sequenza di rendering che include le modifiche dello stato.

Come si può notare, le complicazioni provocate dalla presenza di più processori, comandi elaborati da più di un componente e ottimizzazioni incorporate nei componenti rendono difficile la stima della profilatura. Nella sezione successiva verranno affrontate le eventuali problemi di profilatura. Verranno visualizzate le sequenze di rendering Direct3D di esempio, con le tecniche di misurazione associate. Con queste informazioni, sarà possibile generare misurazioni accurate e ripetibili sulle singole chiamate.

## <a name="how-to-accurately-profile-a-direct3d-render-sequence"></a>Come profilare accuratamente una sequenza di rendering Direct3D

Ora che sono state evidenziate alcune delle problemi di profilatura, in questa sezione verranno illustrate le tecniche che consentono di generare misure di profilo che possono essere utilizzate per il budget. Le misurazioni di profilatura accurate e ripetibili sono possibili se si conosce la relazione tra i componenti controllati dalla CPU e come evitare le ottimizzazioni delle prestazioni implementate dal runtime e dal driver.

Per iniziare, è necessario essere in grado di misurare accuratamente il tempo di esecuzione di una singola chiamata API.

### <a name="pick-an-accurate-measurement-tool-like-queryperformancecounter"></a>Selezionare uno strumento di misurazione accurato come QueryPerformanceCounter

Il sistema operativo Microsoft Windows include un timer ad alta risoluzione che può essere usato per misurare i tempi di risoluzione elevata. Il valore corrente di uno di questi timer può essere restituito usando [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Dopo aver richiamato **QueryPerformanceCounter** per restituire i valori di inizio e di arresto, la differenza tra i due valori può essere convertita nel tempo effettivo trascorso (in secondi) usando **QueryPerformanceCounter**.

I vantaggi dell'uso di [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) sono che sono disponibili in Windows ed è facile da usare. È sufficiente racchiudere le chiamate con una chiamata **QueryPerformanceCounter** e salvare i valori di inizio e di fine. Pertanto, in questo documento viene illustrato come utilizzare **QueryPerformanceCounter** per profilare i tempi di esecuzione, in modo analogo al modo in cui un profiler di strumentazione lo misura. Di seguito è riportato un esempio che illustra come incorporare **QueryPerformanceCounter** nel codice sorgente:


```
  BeginScene();
    ...
    // Start profiling
    LARGE_INTEGER start, stop, freq;
    QueryPerformanceCounter(&start);

    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1); 

    QueryPerformanceCounter(&stop);
    stop.QuadPart -= start.QuadPart;
    QueryPerformanceFrequency(&freq);
    // Stop profiling
    ...
  EndScene();
  Present();
```



Esempio 2: implementazione della profilatura personalizzata con QPC

Start e stop sono due numeri interi di grandi dimensioni che conterranno i valori di inizio e di arresto restituiti dal timer a prestazioni elevate. Si noti che QueryPerformanceCounter (&Start) viene chiamato immediatamente [**prima di**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) QueryPerformanceCounter (&stop) viene chiamato subito dopo [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). Dopo aver ricevuto il valore di arresto, viene chiamato QueryPerformanceFrequency per restituire freq, che corrisponde alla frequenza del timer ad alta risoluzione. In questo esempio ipotetico si supponga di ottenere i risultati seguenti per Start, stop e FREQ:



| Variabile locale | Numero di cicli |
|----------------|-----------------|
| start          | 1792998845094   |
| stop           | 1792998845102   |
| freq           | 3579545         |



 

È possibile convertire questi valori nel numero di cicli necessari per eseguire le chiamate API, come indicato di seguito:


```
# ticks = (stop - start) = 1792998845102 - 1792998845094 = 8 ticks

# cycles = CPU speed * number of ticks / QPF
# 4568   = 2 GHz      * 8              / 3,579,545
```



In altre parole, sono necessari circa 4568 cicli di clock per elaborare la [**trama**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) in questo computer da 2 GHz. È possibile convertire questi valori nel tempo effettivo richiesto per eseguire tutte le chiamate come segue:


```
(stop - start)/ freq = elapsed time
8 ticks / 3,579,545 = 2.2E-6 seconds or between 2 and 3 microseconds.
```



L'uso di QueryPerformanceCounter richiede l'aggiunta di misure di avvio e interruzione alla sequenza di rendering e l'uso di QueryPerformanceFrequency per convertire la differenza (numero di cicli) nel numero di cicli della CPU o nel tempo effettivo. Identificare la tecnica di misurazione è un inizio efficace per lo sviluppo di un'implementazione di profilatura personalizzata. Tuttavia, prima di iniziare a eseguire le misurazioni, è necessario capire come gestire la scheda video.

### <a name="focus-on-cpu-measurements"></a>Concentrarsi sulle misurazioni della CPU

Come indicato in precedenza, la CPU e la GPU funzionano in parallelo per elaborare il lavoro generato dalle chiamate API. Un'applicazione reale richiede la profilatura di entrambi i tipi di processori per verificare se l'applicazione è limitata a livello di CPU o GPU. Poiché le prestazioni della GPU sono specifiche del fornitore, è molto difficile produrre i risultati in questo documento che coprono la varietà di schede video disponibili.

Al contrario, questo documento è incentrato solo sulla profilatura del lavoro eseguito dalla CPU utilizzando una tecnica personalizzata per misurare il funzionamento del runtime e del driver. Il lavoro della GPU verrà ridotto a un importo non significativo, in modo che i risultati della CPU risultino più visibili. Un vantaggio di questo approccio è che questa tecnica restituisce i risultati nell'appendice che dovrebbe essere in grado di correlare con le misurazioni. Per ridurre il lavoro richiesto dalla scheda video a un livello non significativo, è sufficiente ridurre il lavoro di rendering al minor numero possibile. Questa operazione può essere eseguita limitando le chiamate di disegnare per eseguire il rendering di un singolo triangolo e può essere ulteriormente vincolato in modo che ogni triangolo contenga solo un pixel.

L'unità di misura utilizzata in questo documento per misurare il lavoro della CPU sarà il numero di cicli di clock della CPU anziché il tempo effettivo. I cicli di clock della CPU hanno il vantaggio di essere più portabili (per applicazioni limitate alla CPU) rispetto al tempo trascorso effettivo tra computer con velocità di CPU diverse. Questa operazione può essere facilmente convertita in un momento effettivo se lo si desidera.

In questo documento non vengono trattati gli argomenti relativi al bilanciamento del carico di lavoro tra la CPU e la GPU. Tenere presente che l'obiettivo di questo documento non è misurare le prestazioni complessive di un'applicazione, ma per illustrare come misurare accuratamente il tempo impiegato dal runtime e dal driver per elaborare le chiamate API. Con queste misurazioni accurate, è possibile eseguire l'attività di budget della CPU per comprendere determinati scenari di prestazioni.

### <a name="controlling-runtime-and-driver-optimizations"></a>Controllo delle ottimizzazioni di runtime e driver

Con una tecnica di misurazione identificata e una strategia per ridurre il lavoro della GPU, il passaggio successivo consiste nel comprendere le ottimizzazioni del runtime e dei driver che vengono eseguite durante la profilatura.

Il lavoro della CPU può essere suddiviso in tre bucket: il lavoro dell'applicazione, il funzionamento del runtime e il funzionamento del driver. Ignorare il lavoro dell'applicazione perché è sotto il controllo del programmatore. Dal punto di vista dell'applicazione, il runtime e il driver sono come le caselle nere, perché l'applicazione non ha alcun controllo sugli elementi implementati. La chiave consiste nel comprendere le tecniche di ottimizzazione che possono essere implementate nel runtime e nel driver. Se non si conoscono queste ottimizzazioni, è molto facile passare alla conclusione sbagliata sulla quantità di lavoro eseguita dalla CPU in base alle misurazioni del profilo. In particolare, esistono due argomenti correlati a un elemento denominato buffer dei comandi e le operazioni che possono essere eseguite per offuscare la profilatura. tra cui:

-   Ottimizzazione del runtime con il buffer dei comandi. Il buffer dei comandi è un'ottimizzazione del runtime che riduce l'effetto di una transizione in modalità. Per controllare l'intervallo di transizione della modalità, vedere [controllo del buffer dei comandi](#controlling-the-command-buffer).
-   Negazione degli effetti temporali del buffer dei comandi. Il tempo trascorso di una transizione in modalità può avere un notevole effetto sulle misurazioni di profiling. La strategia consiste nel [rendere la sequenza di rendering grande rispetto alla transizione della modalità](#make-the-render-sequence-large-compared-to-the-mode-transition).

### <a name="controlling-the-command-buffer"></a>Controllo del buffer dei comandi

Quando un'applicazione esegue una chiamata API, il runtime converte la chiamata API in un formato indipendente dal dispositivo (che verrà chiamato da un comando) e lo archivia nel buffer dei comandi. Il buffer dei comandi viene aggiunto al diagramma seguente.

![diagramma dei componenti della CPU, incluso un buffer dei comandi](images/microbenchmarkcommandbuffer2.png)

Ogni volta che l'applicazione esegue un'altra chiamata API, il runtime ripete questa sequenza e aggiunge un altro comando al buffer dei comandi. A un certo punto, il runtime svuota il buffer (inviando i comandi al driver). In Windows XP, lo svuotamento del buffer dei comandi provoca una transizione in modalità come il sistema operativo passa dal runtime (in esecuzione in modalità utente) al driver (in esecuzione in modalità kernel), come illustrato nel diagramma seguente.

-   modalità utente: la modalità del processore senza privilegi che esegue il codice dell'applicazione. Le applicazioni in modalità utente non possono accedere ai dati di sistema tranne che tramite i servizi di sistema.
-   modalità kernel: la modalità di elaborazione con privilegi in cui viene eseguito il codice Executive basato su Windows. Un driver o un thread in esecuzione in modalità kernel può accedere a tutta la memoria di sistema, l'accesso diretto all'hardware e le istruzioni della CPU per l'esecuzione di operazioni di I/O con l'hardware.

![diagramma delle transizioni tra la modalità utente e la modalità kernel](images/microbenchmarkcommandbuffer3.png)

La transizione si verifica ogni volta che la CPU passa dall'utente alla modalità kernel (e viceversa) e il numero di cicli richiesti è grande rispetto a una singola chiamata API. Se il runtime ha inviato ogni chiamata API al driver quando è stato richiamato, ogni chiamata API comporterebbe il costo di una transizione in modalità.

Il buffer dei comandi è invece un'ottimizzazione del Runtime progettata per ridurre il costo effettivo della transizione in modalità. Il buffer dei comandi Accoda molti comandi driver in preparazione per una singola transizione in modalità. Quando il runtime aggiunge un comando al buffer dei comandi, il controllo viene restituito all'applicazione. Un profiler non è in grado di sapere che i comandi del driver non sono stati ancora inviati al driver. Di conseguenza, i numeri restituiti da un profiler di strumentazione fuori piano sono fuorvianti, perché misura il lavoro di runtime ma non il driver associato.

### <a name="profile-results-without-a-mode-transition"></a>Risultati del profilo senza una transizione in modalità

Utilizzando la sequenza di rendering dell'esempio 2, di seguito sono riportate alcune misurazioni di intervallo tipiche che illustrano la grandezza di una transizione in modalità. Supponendo che le chiamate a [**Setrame**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) non causino una transizione in modalità, un profiler instrumentato non ripiano può restituire risultati simili ai seguenti:


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
```



Ognuno di questi numeri è la quantità di tempo impiegato dal runtime per aggiungere queste chiamate al buffer dei comandi. Poiché non è presente alcuna transizione in modalità, il driver non ha ancora eseguito alcun lavoro. I risultati del profiler sono accurati, ma non misurano tutte le operazioni che la sequenza di rendering provocherà alla fine della CPU.

### <a name="profile-results-with-a-mode-transition"></a>Risultati del profilo con una transizione in modalità

A questo punto, osservare cosa accade per lo stesso esempio quando si verifica una transizione in modalità. Questa volta, si [**supponga che**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) causi una transizione in modalità. Ancora una volta, un profiler instrumentato fuori piano può restituire risultati simili ai seguenti:


```
Number of cycles for SetTexture           : 98 
Number of cycles for DrawPrimitive        : 946,900
```



Il tempo misurato per la [**detrama**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) è lo stesso, tuttavia, il notevole aumento della quantità di tempo impiegato in [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) è dovuto alla transizione della modalità. Ecco cosa accade:

1.  Si supponga che il buffer dei comandi disponga di spazio per un comando prima dell'avvio della sequenza di rendering.
2.  La [**trama**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) viene convertita in un formato indipendente dal dispositivo e aggiunta al buffer dei comandi. In questo scenario, questa chiamata riempie il buffer dei comandi.
3.  Il runtime tenta di aggiungere [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) al buffer dei comandi, ma non può perché è pieno. Al contrario, il runtime svuota il buffer dei comandi. Questa operazione causa la transizione in modalità kernel. Si supponga che la transizione riprenda circa 5000 cicli. Questo tempo contribuisce al tempo dedicato a **DrawPrimitive**.
4.  Il driver elabora quindi il lavoro associato a tutti i comandi che sono stati svuotati dal buffer dei comandi. Si supponga che l'ora del driver per elaborare i comandi che hanno quasi riempito il buffer dei comandi sia pari a circa 935.000 cicli. Si supponga che il funzionamento del driver associato a [**Setrame**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) sia pari a circa 2750 cicli. Questo tempo contribuisce al tempo dedicato a [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).
5.  Quando il driver termina il lavoro, la transizione in modalità utente restituisce il controllo al runtime. Il buffer dei comandi è ora vuoto. Si supponga che la transizione riprenda circa 5000 cicli.
6.  La sequenza di rendering termina convertendo [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) e aggiungendolo al buffer dei comandi. Si supponga che questa operazione contenga circa 900 cicli. Questo tempo contribuisce al tempo dedicato a **DrawPrimitive**.

Riepilogando i risultati, viene visualizzato quanto segue:


```
DrawPrimitive = kernel-transition + driver work    + user-transition + runtime work
DrawPrimitive = 5000              + 935,000 + 2750 + 5000            + 900
DrawPrimitive = 947,950  
```



Analogamente alla misurazione per [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) senza la transizione della modalità (900 cicli), la misurazione per **DrawPrimitive** con la transizione della modalità (947.950 cicli) è precisa ma inutile in termini di budget per il lavoro della CPU. Il risultato contiene il corretto funzionamento del runtime, il driver funziona per la funzione di [**detrama**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), il driver funziona per tutti i comandi che precedono la **trama** e due transizioni in modalità. Tuttavia, la misurazione manca il funzionamento del driver **DrawPrimitive** .

Una transizione in modalità potrebbe verificarsi in risposta a qualsiasi chiamata. Dipende da ciò che in precedenza era presente nel buffer dei comandi. È necessario controllare la transizione della modalità per comprendere la quantità di lavoro della CPU (Runtime e driver) associata a ogni chiamata. A tale scopo, è necessario un meccanismo per controllare il buffer dei comandi e l'intervallo di transizione della modalità.

### <a name="the-query-mechanism"></a>Meccanismo di query

Il meccanismo di query di Microsoft Direct3D 9 è stato progettato per consentire al runtime di eseguire query sulla GPU per lo stato di avanzamento e restituire determinati dati dalla GPU. Durante la profilatura, se il lavoro della GPU è ridotto al minimo, in modo da avere un effetto trascurabile sulle prestazioni, è possibile restituire lo stato dalla GPU per misurare il lavoro del driver. Dopo tutto, il lavoro del driver è completo quando la GPU ha visto i comandi del driver. Inoltre, il meccanismo di query può essere persuaso a controllare due caratteristiche del buffer dei comandi importanti per la profilatura: quando il buffer dei comandi viene svuotato e la quantità di lavoro nel buffer.

Di seguito è illustrata la stessa sequenza di rendering con il meccanismo di query:


```
// 1. Create an event query from the current device
IDirect3DQuery9* pEvent;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEvent);

// 2. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 3. Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

// 4. Start profiling
LARGE_INTEGER start, stop;
QueryPerformanceCounter(&start);

// 5. Invoke the API calls to be profiled.
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);

// 6. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 7. Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
    
// 8. End profiling
QueryPerformanceCounter(&stop);
```



Esempio 3: utilizzo di una query per controllare il buffer dei comandi

Ecco una spiegazione più dettagliata di ognuna di queste righe di codice:

1.  Creare una query di eventi creando un oggetto query con \_ evento D3DQUERYTYPE.
2.  Aggiungere un marcatore dell'evento di query al buffer dei comandi chiamando [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)([**D3DISSUE \_ end**](d3dissue-end.md)). Questo marcatore indica al driver di rilevare quando la GPU termina l'esecuzione di qualsiasi comando preceduto dal marcatore.
3.  La prima chiamata svuota il buffer dei comandi perché la chiamata di [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) con lo [**\_ svuotamento D3DGETDATA**](d3dgetdata-flush.md) forza il svuotamento del buffer dei comandi. Ogni chiamata successiva sta controllando la GPU per vedere quando viene completata l'elaborazione di tutte le operazioni del buffer dei comandi. Questo ciclo non restituisce S \_ OK fino a quando la GPU non è inattiva.
4.  Campionare l'ora di inizio.
5.  Richiamare le chiamate API profilate.
6.  Aggiungere un secondo marcatore dell'evento di query al buffer dei comandi. Questo marcatore verrà usato per tenere traccia del completamento delle chiamate.
7.  La prima chiamata svuota il buffer dei comandi perché la chiamata di [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) con lo [**\_ svuotamento D3DGETDATA**](d3dgetdata-flush.md) forza il svuotamento del buffer dei comandi. Quando la GPU completa l'elaborazione di tutte le operazioni del buffer dei comandi, **GetData** restituisce S \_ OK e il ciclo viene terminato perché la GPU è inattiva.
8.  Campionare l'ora di arresto.

Di seguito sono riportati i risultati misurati con QueryPerformanceCounter e QueryPerformanceFrequency:



| Variabile locale | Numero di cicli |
|----------------|-----------------|
| start          | 1792998845060   |
| stop           | 1792998845090   |
| freq           | 3579545         |



 

Conversione di cicli in cicli di nuovo (in un computer a 2 GHz):


```
# ticks  = (stop - start) = 1792998845090 - 1792998845060 = 30 ticks
# cycles = CPU speed * number of ticks / QPF
# 16,450 = 2 GHz      * 30             / 3,579,545
```



Di seguito è illustrata la suddivisione del numero di cicli per chiamata:


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
Number of cycles for Issue                : 200
Number of cycles for GetData              : 16,450
```



Il meccanismo di query ci ha consentito di controllare il runtime e il lavoro dei driver misurati. Per comprendere ognuno di questi numeri, ecco cosa accade in risposta a ogni chiamata API, insieme ai tempi stimati:

1.  La prima chiamata svuota il buffer dei comandi chiamando [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) con [**D3DGETDATA \_ Flush**](d3dgetdata-flush.md). Quando la GPU completa l'elaborazione di tutte le operazioni del buffer dei comandi, **GetData** restituisce S \_ OK e il ciclo viene terminato perché la GPU è inattiva.
2.  La sequenza di rendering inizia con la conversione di [**texture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) in un formato indipendente dal dispositivo e l'aggiunta al buffer dei comandi. Si supponga che questa operazione contenga circa 100 cicli.
3.  [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) viene convertito e aggiunto al buffer dei comandi. Si supponga che questa operazione contenga circa 900 cicli.
4.  Il [**problema**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) aggiunge un marcatore di query al buffer dei comandi. Si supponga che questa operazione contenga circa 200 cicli.
5.  [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) causa il svuotamento del buffer dei comandi che impone la transizione in modalità kernel. Si supponga che questa operazione contenga circa 5000 cicli.
6.  Il driver elabora quindi il lavoro associato a tutte e quattro le chiamate. Si supponga che il tempo del driver per elaborare la [**trama**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) sia pari a circa 2964 cicli, [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) è di circa 3600 cicli, il [**problema**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) è circa 200 cicli. Il tempo totale dei driver per tutti e quattro i comandi è quindi pari a circa 6450 cicli.
    > [!Note]  
    > Il driver richiede anche un po' di tempo per visualizzare lo stato della GPU. Poiché il lavoro della GPU è semplice, la GPU dovrebbe essere già stata eseguita. [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) restituirà S \_ OK in base alla probabilità che la GPU sia stata completata.

     

7.  Quando il driver termina il lavoro, la transizione in modalità utente restituisce il controllo al runtime. Il buffer dei comandi è ora vuoto. Si supponga che questa operazione contenga circa 5000 cicli.

I numeri per [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) includono:


```
GetData = kernel-transition + driver work + user-transition
GetData = 5000              + 6450        + 5000           
GetData = 16,450  

driver work = SetTexture + DrawPrimitive + Issue = 
driver work = 2964       + 3600          + 200   = 6450 cycles 
```



Il meccanismo di query utilizzato in combinazione con QueryPerformanceCounter misura tutto il lavoro della CPU. Questa operazione viene eseguita con una combinazione di marcatori di query e confronto dello stato delle query. I marcatori di query di avvio e arresto aggiunti al buffer dei comandi vengono usati per controllare la quantità di lavoro presente nel buffer. Attendendo che venga restituito il codice restituito corretto, la misurazione iniziale viene eseguita subito prima dell'avvio di una sequenza di rendering pulita e la misurazione dell'arresto viene eseguita subito dopo il completamento del lavoro associato al contenuto del buffer dei comandi. Questo consente di acquisire efficacemente il lavoro della CPU eseguito dal runtime e dal driver.

Ora che si conosce il buffer dei comandi e l'effetto che può avere sulla profilatura, è necessario sapere che esistono alcune altre condizioni che possono causare il svuotamento del buffer dei comandi da parte del runtime. È necessario tenerli sotto controllo nelle sequenze di rendering. Alcune di queste condizioni sono in risposta alle chiamate API, altre sono in risposta alle modifiche delle risorse nel Runtime. Una delle condizioni seguenti determinerà una transizione in modalità:

-   Quando uno dei metodi di blocco ([**Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)) viene chiamato su un vertex buffer, un buffer di indice o una trama (in determinate condizioni con determinati flag).
-   Quando viene creato un dispositivo o un vertex buffer, un buffer di indice o una trama.
-   Quando un dispositivo o un vertex buffer, un buffer di indice o una trama viene eliminato definitivamente dall'ultima versione.
-   Quando viene chiamato [**ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) .
-   Quando [**present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) viene chiamato.
-   Quando il buffer dei comandi si riempie.
-   Quando [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) viene chiamato con lo \_ scaricamento di D3DGETDATA.

Prestare attenzione a controllare queste condizioni nelle sequenze di rendering. Ogni volta che viene aggiunta una transizione in modalità, 10.000 cicli di lavoro dei driver verranno aggiunti alle misurazioni della profilatura. Il buffer dei comandi non è inoltre dimensionato in modo statico. Il runtime può modificare le dimensioni del buffer in risposta alla quantità di lavoro generata dall'applicazione. Si tratta ancora di un'altra ottimizzazione che dipende da una sequenza di rendering.

Prestare attenzione a controllare le transizioni della modalità durante la profilatura. Il meccanismo di query offre un metodo efficace per svuotare il buffer dei comandi, in modo da poter controllare i tempi della transizione della modalità e la quantità di lavoro contenuto nel buffer. Tuttavia, anche questa tecnica può essere migliorata riducendo il tempo di transizione della modalità per renderlo non significativo rispetto al risultato misurato.

### <a name="make-the-render-sequence-large-compared-to-the-mode-transition"></a>Rendere la sequenza di rendering grande rispetto alla transizione della modalità

Nell'esempio precedente, l'opzione della modalità kernel e l'opzione della modalità utente utilizzano circa 10.000 cicli che non hanno nulla a che fare con il lavoro di runtime e driver. Poiché la transizione della modalità è incorporata nel sistema operativo, non è possibile ridurla a zero. Per rendere la transizione della modalità non significativa, è necessario modificare la sequenza di rendering in modo che il driver e il lavoro di runtime siano un ordine di grandezza maggiore rispetto a quello delle opzioni di modalità. È possibile provare a eseguire una sottrazione per rimuovere le transizioni, ma il costo di una sequenza di rendering notevolmente maggiore è più affidabile.

La strategia per ridurre la transizione della modalità fino a quando non diventa irrilevante consiste nell'aggiungere un ciclo alla sequenza di rendering. È ad esempio possibile esaminare i risultati della profilatura se viene aggiunto un ciclo che ripete la sequenza di rendering 1500 volte:


```
// Initialize the array with two textures, same size, same format
IDirect3DTexture* texArray[2];

CreateQuery(D3DQUERYTYPE_EVENT, pEvent);
pEvent->Issue(D3DISSUE_END);
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

LARGE_INTEGER start, stop;
// Now start counting because the video card is ready
QueryPerformanceCounter(&start);

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  SetTexture(taxArray[i%2]);
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

pEvent->Issue(D3DISSUE_END);

while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
QueryPerformanceCounter(&stop);
```



Esempio 4: aggiungere un ciclo alla sequenza di rendering

Di seguito sono riportati i risultati misurati con QueryPerformanceCounter e QueryPerformanceFrequency:



| Variabile locale | Numero di TIC |
|----------------|----------------|
| start          | 1792998845000  |
| stop           | 1792998847084  |
| freq           | 3579545        |



 

L'uso di QueryPerformanceCounter misura 2.840 ora. La conversione di cicli in cicli è uguale a quella già visualizzata:


```
# ticks  = (stop - start) = 1792998847084 - 1792998845000 = 2840 ticks
# cycles    = machine speed * number of ticks / QPF
# 6,900,000 = 2 GHz          * 2840           / 3,579,545
```



In altre parole, sono necessari circa 6,9 milioni cicli in questo computer a 2 GHz per elaborare le chiamate 1500 nel ciclo di rendering. Dei cicli 6,9 milioni, la quantità di tempo nelle transizioni della modalità è approssimativamente di 10.000, quindi i risultati del profilo sono quasi interamente misurabili al lavoro associato a [**Setrame**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).

Si noti che l'esempio di codice richiede una matrice di due trame. Per evitare un'ottimizzazione del runtime che rimuoverebbe la [**texture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) se imposta lo stesso puntatore di trama ogni volta che viene chiamato, è sufficiente usare una matrice di due trame. In questo modo, ogni volta attraverso il ciclo, viene modificato il puntatore di trama e viene eseguito il lavoro completo associato a **Setrame** . Assicurarsi che entrambe le trame abbiano le stesse dimensioni e il formato, in modo che nessun altro stato cambierà quando viene eseguita la trama.

Ora è disponibile una tecnica per la profilatura di Direct3D. Si basa sul contatore delle prestazioni elevate (QueryPerformanceCounter) per registrare il numero di cicli che richiede la CPU per elaborare il lavoro. Il lavoro viene controllato attentamente in modo da essere il runtime e il lavoro dei driver associati alle chiamate API usando il meccanismo di query. Una query fornisce due metodi di controllo: innanzitutto per svuotare il buffer dei comandi prima dell'avvio della sequenza di rendering e, in secondo luogo, per restituire al termine del lavoro della GPU.

Finora, in questo documento è stato illustrato come profilare una sequenza di rendering. Ogni sequenza di rendering è stata abbastanza semplice e contiene una singola chiamata [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) e una chiamata di [**setrama**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) . Questa operazione è stata eseguita per concentrarsi sul buffer dei comandi e sull'uso del meccanismo di query per controllarlo. Di seguito è riportato un breve riepilogo di come profilare una sequenza di rendering arbitraria:

-   Usare un contatore delle prestazioni elevato come QueryPerformanceCounter per misurare il tempo necessario per elaborare ogni chiamata API. Usare QueryPerformanceFrequency e la frequenza di clock della CPU per convertirla nel numero di cicli della CPU per ogni chiamata API.
-   Ridurre al minimo la quantità di lavoro della GPU eseguendo il rendering degli elenchi di triangolo, in cui ogni triangolo contiene un pixel.
-   Utilizzare il meccanismo di query per svuotare il buffer dei comandi prima della sequenza di rendering. Ciò garantisce che la profilatura catturerà la quantità corretta di lavoro di runtime e driver associata alla sequenza di rendering.
-   Controllare la quantità di lavoro aggiunto al buffer dei comandi con marcatori degli eventi di query. Questa stessa query rileva quando la GPU termina il lavoro. Poiché il lavoro della GPU è semplice, questo è praticamente equivalente alla misurazione del completamento del lavoro del driver.

Tutte queste tecniche vengono utilizzate per profilare le modifiche di stato. Supponendo di aver letto e compreso come controllare il buffer dei comandi e avere completato le misurazioni di base in [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), è possibile aggiungere modifiche di stato alle sequenze di rendering. Quando si aggiungono modifiche di stato a una sequenza di rendering, si verificano alcuni problemi di profilatura aggiuntivi. Se si intende aggiungere modifiche di stato alle sequenze di rendering, assicurarsi di continuare con la sezione successiva.

## <a name="profiling-direct3d-state-changes"></a>Profilatura delle modifiche dello stato Direct3D

Direct3D usa molti Stati di rendering per controllare quasi tutti gli aspetti della pipeline. Le API che provocano modifiche di stato includono qualsiasi funzione o metodo diverso dalle \* chiamate primitive di estrazione.

Le modifiche di stato sono complesse perché potrebbe non essere possibile visualizzare il costo di una modifica di stato senza rendering. Si tratta di un risultato dell'algoritmo Lazy utilizzato dal driver e dalla GPU per rinviare il lavoro fino a quando non è assolutamente necessario eseguire questa operazione. In generale, attenersi alla procedura seguente per misurare una singola modifica dello stato:

1.  Profilare prima [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .
2.  Aggiungere una modifica di stato alla sequenza di rendering e profilare la nuova sequenza.
3.  Sottrarre la differenza tra le due sequenze per ottenere il costo della modifica dello stato.

Naturalmente, tutto ciò che si è appreso sull'uso del meccanismo di query e l'inserimento della sequenza di rendering in un ciclo per negare il costo della transizione della modalità si applica ancora.

### <a name="profiling-a-simple-state-change"></a>Profilatura di una semplice modifica dello stato

A partire da una sequenza di rendering che contiene [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), di seguito è illustrata la sequenza di codice per misurare il costo di aggiunta di una [**trama**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture):


```
// Get the start counter value as shown in Example 4 

// Initialize a texture array as shown in Example 4
IDirect3DTexture* texArray[2];

// Render sequence loop 
for(int i = 0; i < 1500; i++)
{
  SetTexture(0, texArray[i%2];
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

// Get the stop counter value as shown in Example 4 
```



Esempio 5: misurazione di una chiamata API di modifica dello stato

Si noti che il ciclo contiene due chiamate, [**Setrame**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). La sequenza di rendering esegue il ciclo di 1500 volte e genera risultati simili ai seguenti:



| Variabile locale | Numero di TIC |
|----------------|----------------|
| start          | 1792998860000  |
| stop           | 1792998870260  |
| freq           | 3579545        |



 

La conversione di cicli in cicli di nuovo produce:


```
# ticks  = (stop - start) = 1792998870260 - 1792998860000 = 10,260 ticks
# cycles    = machine speed * number of ticks / QPF
5,775,000   = 2 GHz          * 10,260         / 3,579,545
```



La divisione per il numero di iterazioni nel ciclo produce:


```
5,775,000 cycles / 1500 iterations = 3850 cycles for one iteration
```



Ogni iterazione del ciclo contiene una modifica di stato e una chiamata di progetto. La sottrazione del risultato della sequenza di rendering [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) lascia:


```
3850 - 1100 = 2750 cycles for SetTexture
```



Il numero medio di cicli per aggiungere la [**texture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) a questa sequenza di rendering. Questa stessa tecnica può essere applicata ad altre modifiche di stato.

Perché la [**texture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) è una modifica di stato semplice? Poiché lo stato impostato è vincolato in modo che la pipeline abbia la stessa quantità di lavoro ogni volta che lo stato viene modificato. La limitazione di entrambe le trame allo stesso formato e alle stesse dimensioni garantisce la stessa quantità di lavoro per ogni chiamata di **setrama** .

### <a name="profiling-a-state-change-that-needs-to-be-toggled"></a>Profilatura di una modifica di stato che deve essere attivata/disabilitata

Sono presenti altre modifiche di stato che provocano la modifica della quantità di lavoro eseguita dalla pipeline grafica per ogni iterazione del ciclo di rendering. Se, ad esempio, il test z è abilitato, ogni colore pixel aggiorna una destinazione di rendering solo dopo che il valore z del nuovo pixel viene testato rispetto al valore z del pixel esistente. Se il test z è disabilitato, questo test per pixel non viene eseguito e l'output viene scritto molto più velocemente. L'abilitazione o la disabilitazione dello stato dei test z modifica in modo significativo la quantità di lavoro eseguita (dalla CPU e dalla GPU) durante il rendering.

[**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) richiede un particolare stato di rendering e un valore di stato per abilitare o disabilitare il test z. Il valore di stato specifico viene valutato in fase di esecuzione per determinare la quantità di lavoro necessaria. È difficile misurare questa modifica dello stato in un ciclo di rendering e precondizionare comunque lo stato della pipeline in modo che cambi. L'unica soluzione consiste nell'impostare la modifica dello stato durante la sequenza di rendering.

Ad esempio, la tecnica di profilatura deve essere ripetuta due volte come segue:

1.  Per iniziare, profilare la sequenza di rendering [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) . Chiamare questa linea di base.
2.  Profilare una seconda sequenza di rendering che consente di disabilitare la modifica dello stato. Il ciclo della sequenza di rendering contiene:
    -   Una modifica dello stato per impostare lo stato in una condizione "false".
    -   [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) proprio come la sequenza originale.
    -   Una modifica dello stato per impostare lo stato in una condizione "true".
    -   Secondo [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) per forzare la realizzazione della seconda modifica dello stato.
3.  Trovare la differenza tra le due sequenze di rendering. Questa operazione viene eseguita da:
    -   Moltiplicare la sequenza di [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) di base per 2 perché sono presenti due chiamate **DrawPrimitive** nella nuova sequenza.
    -   Sottrae il risultato della nuova sequenza dalla sequenza originale.
    -   Dividere il risultato per 2 per ottenere il costo medio della modifica dello stato "false" e "true".

Con la tecnica di ciclo usata nella sequenza di rendering, è necessario misurare il costo della modifica dello stato della pipeline passando lo stato da "true" a una condizione "false" e viceversa per ogni iterazione nella sequenza di rendering. Il significato di "true" e "false" qui non è un valore letterale. Ciò significa semplicemente che lo stato deve essere impostato in condizioni opposte. In questo modo verranno misurate entrambe le modifiche dello stato durante la profilatura. Naturalmente, tutto ciò che si è appreso sull'uso del meccanismo di query e l'inserimento della sequenza di rendering in un ciclo per negare il costo della transizione della modalità si applica ancora.

Ecco ad esempio la sequenza di codice per misurare il costo di attivazione o disattivazione del test z:


```
// Get the start counter value as shown in Example 4 

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the "false" condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Set the pipeline state to the "true" condition
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}

// Get the stop counter value as shown in Example 4 
```



Esempio 5: misurazione di una modifica dello stato di attivazione

Il ciclo commuta lo stato eseguendo due chiamate [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) . La prima chiamata di **SetRenderState** Disabilita il test z e il secondo **SetRenderState** Abilita il test z. Ogni **SetRenderState** è seguito da [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , in modo che il lavoro associato alla modifica dello stato venga elaborato dal driver anziché impostare solo un bit dirty nel driver.

Questi numeri sono ragionevoli per questa sequenza di rendering:



| Variabile locale | Numero di cicli |
|----------------|-----------------|
| start          | 1792998845000   |
| stop           | 1792998861740   |
| freq           | 3579545         |



 

La conversione di cicli in cicli di nuovo produce:


```
# ticks  = (stop - start) = 1792998861740 - 1792998845000 = 15,120 ticks
# cycles    = machine speed * number of ticks / QPF
 9,300,000  = 2 GHz          * 16,740         / 3,579,545
```



La divisione per il numero di iterazioni nel ciclo produce:


```
9,300,000 cycles / 1500 iterations = 6200 cycles for one iteration
```



Ogni iterazione del ciclo contiene due modifiche di stato e due chiamate di progetto. La sottrazione delle chiamate di estrazione (presupponendo 1100 cicli) lascia:


```
6200 - 1100 - 1100 = 4000 cycles for both state changes
```



Il numero medio di cicli per entrambe le modifiche di stato, quindi il tempo medio per ogni modifica dello stato è:


```
4000 / 2  = 2000 cycles for each state change
```



Pertanto, il numero medio di cicli per abilitare o disabilitare il test z è 2000 cicli. Vale la pena notare che QueryPerformanceCounter sta misurando la metà del tempo e la disabilitazione della z per la metà del tempo. Questa tecnica misura effettivamente la media di entrambe le modifiche di stato. In altre parole, si sta misurando il tempo necessario per abilitare o disabilitare uno stato. Utilizzando questa tecnica, non è possibile sapere se le ore di abilitazione e disabilitazione sono equivalenti poiché è stata misurata la media di entrambe. Tuttavia, si tratta di un numero ragionevole da usare quando si imposta un budget per uno stato di attivazione/disattivazione come un'applicazione che causa questa modifica dello stato solo attivando questo stato.

Ora è possibile applicare queste tecniche e profilare tutte le modifiche dello stato desiderate, giusto? Risposta errata. È comunque necessario prestare particolare attenzione alle ottimizzazioni progettate per ridurre la quantità di lavoro che deve essere eseguita. Quando si progettano le sequenze di rendering, è necessario tenere presenti due tipi di ottimizzazioni.

### <a name="watch-out-for-state-change-optimizations"></a>Guarda le ottimizzazioni di modifica dello stato

Nella sezione precedente viene illustrato come profilare entrambi i tipi di modifiche di stato, ovvero una semplice modifica dello stato vincolata a generare la stessa quantità di lavoro per ogni iterazione e una modifica dello stato di attivazione e modifica che modifica in modo significativo la quantità di lavoro eseguita. Cosa accade se si accetta la sequenza di rendering precedente e si aggiunge un'altra modifica allo stato? Ad esempio, in questo esempio viene accettata la sequenza di rendering z>-Enable e viene aggiunto un confronto z-Func:


```
// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZFUNC, D3DCMP_NEVER);

  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZFUNC, D3DCMP_ALWAYS);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}
```



Lo stato z-Func imposta il livello di confronto durante la scrittura nel buffer z (tra il valore z di un pixel corrente e il valore z di un pixel nel buffer di profondità). D3DCMP \_ non disattiva mai il confronto di test z mentre D3DCMP \_ imposta sempre il confronto in modo che avvenga ogni volta che viene eseguito il test z.

La profilatura di una di queste modifiche di stato in una sequenza di rendering con [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) genera risultati simili ai seguenti:



| Modifica dello stato singolo | Numero medio di cicli |
|---------------------|--------------------------|
| \_Solo ZENABLE D3DRS | 2000                     |



 

oppure



| Modifica dello stato singolo | Numero medio di cicli |
|---------------------|--------------------------|
| \_Solo ZFUNC D3DRS   | 600                      |



 

Tuttavia, se si esegue il profiling \_ di D3DRS ZENABLE e D3DRS \_ ZFUNC nella stessa sequenza di rendering, è possibile visualizzare risultati simili ai seguenti:



| Entrambe le modifiche di stato            | Numero medio di cicli |
|-------------------------------|--------------------------|
| D3DRS \_ ZENABLE + D3DRS \_ ZFUNC | 2000                     |



 

È possibile prevedere che il risultato sia la somma dei cicli 2000 e 600 (o 2600) perché il driver esegue tutte le operazioni associate all'impostazione di entrambi gli Stati di rendering. La media è invece di 2000 cicli.

Questo risultato riflette un'ottimizzazione della modifica dello stato implementata nel runtime, nel driver o nella GPU. In questo caso, il driver potrebbe vedere il primo [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e impostare uno stato dirty che posticipa il lavoro fino a un momento successivo. Quando il driver rileva il secondo **SetRenderState**, lo stesso stato dirty potrebbe essere impostato in modo ridondante e lo stesso lavoro verrà posticipato ancora una volta. Quando viene chiamato [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , il lavoro associato allo stato dirty viene infine elaborato. Il driver esegue il lavoro una volta, il che significa che le prime due modifiche di stato vengono effettivamente consolidate dal driver. Analogamente, le modifiche apportate al terzo e al quarto stato vengono consolidate dal driver in una singola modifica dello stato quando viene chiamato il secondo **DrawPrimitive** . Il risultato finale è che il driver e la GPU elaborano una singola modifica dello stato per ogni chiamata di progetto.

Si tratta di un valido esempio di ottimizzazione di driver dipendente dalla sequenza. Il driver è stato posticipato due volte impostando uno stato dirty, quindi il lavoro viene eseguito una volta per cancellare lo stato modificato. Questo è un buon esempio del tipo di miglioramento dell'efficienza che può avere luogo quando il lavoro viene posticipato fino a quando non è assolutamente necessario.

Come è possibile stabilire quali modifiche di stato impostano uno stato dirty internamente e quindi posticipare il lavoro fino a un momento successivo? Solo eseguendo il test delle sequenze di rendering (o parlando con writer di driver). I driver vengono aggiornati e migliorati periodicamente, in modo che l'elenco di ottimizzazioni non sia statico. Esiste un solo modo per conoscere perfettamente il costo di una modifica di stato in una determinata sequenza di rendering, in un determinato set di hardware; e in questo modo viene misurato.

### <a name="watch-out-for-drawprimitive-optimizations"></a>Guarda le ottimizzazioni DrawPrimitive

Oltre alle ottimizzazioni di modifica dello stato, il runtime tenterà di ottimizzare il numero di chiamate di progetto che devono essere elaborate dal driver. Si considerino, ad esempio, le chiamate di estrazione back:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 3); // Draw 3 primitives, vertices 0 - 8
DrawPrimitive(D3DPT_TRIANGLELIST, 9, 4); // Draw 4 primitives, vertices 9 - 20
```



Esempio 5a: due chiamate di progetto

Questa sequenza contiene due chiamate di richiamo, che il runtime consoliderà in una singola chiamata equivalente a:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 7); // Draw 7 primitives, vertices 0 - 20
```



Esempio 5b: una singola chiamata di estrazione concatenata

Il runtime concatenerà entrambe le chiamate di progetto in una singola chiamata, riducendo al contempo il lavoro del driver del 50% perché il driver deve ora elaborare una sola chiamata di progetto.

In generale, il runtime concatenerà due o più chiamate [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) back-to-back quando:

1.  Il tipo primitivo è un elenco di triangoli (triangolare D3DPT \_ ).
2.  Ogni chiamata successiva di [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) deve fare riferimento a vertici consecutivi all'interno del buffer dei vertici.

Analogamente, le condizioni corrette per la concatenazione di due o più chiamate [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) back-to-back sono:

1.  Il tipo primitivo è un elenco di triangoli (triangolare D3DPT \_ ).
2.  Ogni chiamata successiva di [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) deve fare riferimento sequenziale agli indici consecutivi all'interno del buffer dell'indice.
3.  Ogni chiamata [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) successiva deve usare lo stesso valore per BaseVertexIndex.

Per evitare la concatenazione durante la profilatura, modificare la sequenza di rendering in modo che il tipo primitivo non sia un elenco di triangolo oppure modificare la sequenza di rendering in modo che non siano presenti chiamate di traccia di tipo back-to-back che usino vertici consecutivi (o indici). In particolare, il runtime concatenerà anche le chiamate di progetto che soddisfano entrambe le condizioni seguenti:

-   Quando la chiamata precedente è [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), se la chiamata di richiamo successiva:
    -   Usa un elenco di triangolo e
    -   Specifica il StartVertex = precedente StartVertex + precedente PrimitiveCount \* 3
-   Quando si usa [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive), se la chiamata di richiamo successiva:
    -   Usa un elenco di triangolo e
    -   Specifica il startIndex = precedente StartIndex + PrimitiveCount precedente \* 3 e
    -   Specifica il BaseVertexIndex = BaseVertexIndex precedente

Di seguito è riportato un esempio più delicato di concatenazione delle chiamate di traccia che è facile da ignorare durante la profilatura. Si supponga che la sequenza di rendering abbia un aspetto simile al seguente:


```
  for(int i = 0; i < 1500; i++)
  {
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Esempio 5C: una modifica di stato e una chiamata di un progetto

Il ciclo scorre i triangoli 1500, impostando una trama e disegnando ogni triangolo. Questo ciclo di rendering richiede circa 2750 cicli per la [**ditrama**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e 1100 cicli per [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , come illustrato nelle sezioni precedenti. È possibile prevedere in modo intuitivo che lo spostando di una **struttura** all'esterno del ciclo di rendering debba ridurre la quantità di lavoro eseguita dal driver di 1500 \* cicli 2750, ovvero la quantità di lavoro associato alla chiamata di **setrame** 1500 volte. Il frammento di codice avrà un aspetto simile al seguente:


```
  SetTexture(...); // Set the state outside the loop
  for(int i = 0; i < 1500; i++)
  {
//    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Esempio 5D: esempio 5C con la modifica dello stato al di fuori del ciclo

Lo stato di un'operazione di ridimensionamento [**all'esterno del**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) ciclo di rendering comporta una riduzione della quantità di lavoro associato a un oggetto **setexture** poiché viene chiamato una volta anziché 1500 volte. Un effetto secondario meno ovvio è che il lavoro per [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) è ridotto anche da 1500 chiamate a 1 chiamata, perché tutte le condizioni per la concatenazione delle chiamate di progetto sono soddisfatte. Quando la sequenza di rendering viene elaborata, il runtime elabora le chiamate 1500 in una singola chiamata al driver. Spostando questa riga di codice, la quantità di lavoro dei driver è stata ridotta in modo significativo:


```
total work done = runtime + driver work

Example 5c: with SetTexture in the loop:
runtime work = 1500 SetTextures + 1500 DrawPrimitives 
driver  work = 1500 SetTextures + 1500 DrawPrimitives 

Example 5d: with SetTexture outside of the loop:
runtime work = 1 SetTexture + 1 DrawPrimitive + 1499 Concatenated DrawPrimitives 
driver  work = 1 SetTexture + 1 DrawPrimitive 
```



Questi risultati sono completamente corretti, ma sono molto fuorvianti nel contesto della domanda originale. L'ottimizzazione della chiamata di richiamo ha causato una riduzione significativa della quantità di lavoro del driver. Si tratta di un problema comune quando si esegue la profilatura personalizzata. Quando si eliminano le chiamate da una sequenza di rendering, prestare attenzione per evitare la concatenazione di chiamate di richiamo. In realtà, questo scenario è un esempio potente della quantità di miglioramento delle prestazioni del driver possibile da questa ottimizzazione del runtime.

A questo punto si è in grado di misurare le modifiche allo stato. Per iniziare, eseguire la profilatura di [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). Aggiungere quindi ogni modifica di stato aggiuntiva alla sequenza (in alcuni casi l'aggiunta di una chiamata e in altri casi l'aggiunta di due chiamate) e la misurazione della differenza tra le due sequenze. È possibile convertire i risultati in cicli o cicli o ora. Analogamente alla misurazione delle sequenze di rendering con QueryPerformanceCounter, la misurazione delle singole modifiche di stato si basa sul meccanismo di query per controllare il buffer dei comandi e l'inserimento delle modifiche allo stato in un ciclo per ridurre al minimo l'effetto delle transizioni in modalità. Questa tecnica consente di misurare il costo di attivazione e disattivazione di uno stato, poiché il profiler restituisce la media di abilitazione e disabilitazione dello stato.

Grazie a questa funzionalità, è possibile iniziare a generare sequenze di rendering arbitrarie e misurare accuratamente le operazioni di runtime e driver associate. I numeri possono quindi essere usati per rispondere a domande relative al budget, ad esempio "quante più chiamate" possono essere apportate nella sequenza di rendering, mantenendo al tempo stesso una frequenza di fotogrammi ragionevole, presumendo scenari limitati dalla CPU.

## <a name="summary"></a>Riepilogo

Questo documento illustra come controllare il buffer dei comandi in modo che le singole chiamate possano essere profilate accuratamente. I numeri di profilatura possono essere generati in cicli, cicli o tempo assoluto. Rappresentano la quantità di operazioni di runtime e driver associate a ogni chiamata API.

Iniziare con la profilatura di una \* chiamata primitiva di traccia in una sequenza di rendering. Ricordare di:

1.  Usare QueryPerformanceCounter per misurare il numero di cicli per ogni chiamata API. Usare QueryPerformanceFrequency per convertire i risultati in cicli o ora se si desidera.
2.  Utilizzare il meccanismo di query per svuotare il buffer dei comandi prima di avviare.
3.  Includere la sequenza di rendering in un ciclo per ridurre al minimo l'effetto della transizione in modalità.
4.  Usare il meccanismo di query per misurare il completamento del lavoro della GPU.
5.  Osservare la concatenazione in fase di esecuzione che avrà un notevole effetto sulla quantità di lavoro svolto.

In questo modo vengono fornite le prestazioni di base per [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) che possono essere usate per compilare da. Per profilare una modifica di stato, seguire questi suggerimenti aggiuntivi:

1.  Aggiungere la modifica di stato a un profilo di sequenza di rendering noto la nuova sequenza. Poiché il test viene eseguito in un ciclo, è necessario impostare lo stato due volte in valori opposti, come Enable e Disable per instance.
2.  Confrontare la differenza nei tempi di ciclo tra le due sequenze.
3.  Per le modifiche di stato che cambiano significativamente la pipeline (ad esempio, la [**trama**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)), sottrarre la differenza tra le due sequenze per ottenere l'ora per la modifica dello stato.
4.  Per le modifiche di stato che modificano in modo significativo la pipeline (e pertanto richiedono gli Stati di alternanza come [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)), sottrarre la differenza tra le sequenze di rendering e dividere per 2. Verrà generato il numero medio di cicli per ogni modifica dello stato.

Tuttavia, prestare attenzione alle ottimizzazioni che causano risultati imprevisti durante la profilatura. Le ottimizzazioni di modifica dello stato possono impostare stati Dirty che causano il rinvio del lavoro. Questo può causare risultati del profilo che non sono intuitivi come previsto. Le chiamate di estrazione concatenate ridurranno notevolmente le attività dei driver che possono causare conclusioni fuorvianti. Le sequenze di rendering pianificate con attenzione vengono usate per impedire che le concatenazioni di modifiche di stato e di chiamata vengano eseguite. Il trucco consiste nel impedire che le ottimizzazioni avvengano durante la profilatura, in modo che i numeri generati siano numeri di budget ragionevoli.

> [!Note]  
> La duplicazione di questa strategia di profilatura in un'applicazione senza il meccanismo di query è più difficile. Prima di Direct3D 9, l'unico modo prevedibile per svuotare il buffer dei comandi consiste nel bloccare una superficie attiva, ad esempio una destinazione di rendering, per attendere fino a quando la GPU non è inattiva. Questo è dovuto al fatto che il blocco di una superficie impone al runtime di svuotare il buffer dei comandi nel caso in cui siano presenti comandi di rendering nel buffer che dovrebbero aggiornare la superficie prima che venga bloccata, oltre ad attendere il completamento della GPU. Questa tecnica è funzionale, sebbene sia più intrusiva l'uso del meccanismo di query introdotto in Direct3D 9.

 

## <a name="appendix"></a>Appendice

I numeri in questa tabella sono un intervallo di approssimazioni per la quantità di operazioni di runtime e driver associate a ognuna di queste modifiche di stato. Le approssimazioni sono basate sulle misure effettive effettuate sui driver usando le tecniche illustrate nel documento. Questi numeri sono stati generati utilizzando il runtime Direct3D 9 e sono dipendenti dal driver.

Le tecniche descritte in questo documento sono progettate per misurare il funzionamento del driver e del runtime. In generale, non è pratico fornire risultati che corrispondano alle prestazioni della CPU e della GPU in ogni applicazione, perché ciò richiede una matrice completa di sequenze di rendering. Inoltre, è particolarmente difficile eseguire il benchmark delle prestazioni della GPU perché dipende in modo elevato dall'impostazione dello stato nella pipeline prima della sequenza di rendering. Ad esempio, l'abilitazione della fusione alfa non influisce sulla quantità di lavoro della CPU necessaria, ma può avere un notevole impatto sulla quantità di lavoro svolto dalla GPU. Pertanto, le tecniche di questo documento vincolano il lavoro della GPU alla quantità minima possibile limitando la quantità di dati di cui è necessario eseguire il rendering. Ciò significa che i numeri nella tabella corrisponderanno maggiormente ai risultati ottenuti dalle applicazioni con limitazione della CPU, anziché da un'applicazione limitata dalla GPU.

Si consiglia di usare le tecniche presentate per coprire gli scenari e le configurazioni più importanti per l'utente. I valori nella tabella possono essere utilizzati per il confronto con i numeri generati. Poiché ogni driver varia, l'unico modo per generare i numeri effettivi è quello di generare i risultati della profilatura usando gli scenari.



| Chiamata API                             | Numero medio di cicli |
|--------------------------------------|--------------------------|
| SetVertexDeclaration                 | 6500-11250             |
| SetFVF                               | 6400-11200             |
| SetVertexShader                      | 3000-12100             |
| SetPixelShader                       | 6300-7000              |
| SPECULARENABLE                       | 1900-11200             |
| SetRenderTarget                      | 6000-6250              |
| SetPixelShaderConstant (1 costante)  | 1500-9000              |
| NORMALIZENORMALS                     | 2200-8100              |
| Alleggeribile                          | 1300-9000              |
| SetStreamSource                      | 3700-5800              |
| ILLUMINAZIONE                             | 1700-7500              |
| DIFFUSEMATERIALSOURCE                | 900-8300               |
| AMBIENTMATERIALSOURCE                | 900-8200               |
| COLORVERTEX                          | 800-7800               |
| Chiaro                             | 2200-5100              |
| SetTransform                         | 3200-3750              |
| SetIndices                           | 900-5600               |
| AMBIENTE                              | 1150-4800              |
| SetTexture                           | 2500-3100              |
| SPECULARMATERIALSOURCE               | 900-4600               |
| EMISSIVEMATERIALSOURCE               | 900-4500               |
| Materiali                          | 1000-3700              |
| ZENABLE                              | 700-3900               |
| WRAP0                                | 1600-2700              |
| MINFILTER                            | 1700-2500              |
| MAGFILTER                            | 1700-2400              |
| SetVertexShaderConstant (1 costante) | 1000-2700              |
| COLOROP                              | 1500-2100              |
| COLORARG2                            | 1300-2000              |
| COLORARG1                            | 1300-1980              |
| CULLMODE                             | 500-2570               |
| RITAGLIO                             | 500-2550               |
| DrawIndexedPrimitive                 | 1200-1400              |
| ADDRESSV                             | 1090-1500              |
| ADDRESSU                             | 1070-1500              |
| DrawPrimitive                        | 1050-1150              |
| SRGBTEXTURE                          | 150-1500               |
| STENCILMASK                          | 570-700                |
| STENCILZFAIL                         | 500-800                |
| STENCILREF                           | 550-700                |
| ALPHABLENDENABLE                     | 550-700                |
| STENCILFUNC                          | 560-680                |
| STENCILWRITEMASK                     | 520-700                |
| STENCILFAIL                          | 500-750                |
| ZFUNC                                | 510-700                |
| ZWRITEENABLE                         | 520-680                |
| STENCILENABLE                        | 540-650                |
| STENCILPASS                          | 560-630                |
| SRCBLEND                             | 500-685                |
| StencilMODE a due \_ lati \_              | 450-590                |
| ALPHATESTENABLE                      | 470-525                |
| ALPHAREF                             | 460-530                |
| ALPHAFUNC                            | 450-540                |
| DESTBLEND                            | 475-510                |
| COLORWRITEENABLE                     | 465-515                |
| CCW \_ STENCILFAIL                     | 340-560                |
| CCW \_ STENCILPASS                     | 340-545                |
| CCW \_ STENCILZFAIL                    | 330-495                |
| SCISSORTESTENABLE                    | 375-440                |
| CCW \_ STENCILFUNC                     | 250-480                |
| SetScissorRect                       | 150-340                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati](advanced-topics.md)
</dt> </dl>

 

 
