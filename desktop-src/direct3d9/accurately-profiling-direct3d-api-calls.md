---
description: Dopo aver creato un'applicazione Microsoft Direct3D funzionale e averne migliorato le prestazioni, in genere si usa uno strumento di profilatura pre-installato o una tecnica di misurazione personalizzata per misurare il tempo necessario per eseguire una o più chiamate API (Application Programming Interface). Se questa operazione è stata eseguita ma si stanno ottenendo risultati temporali che variano da una sequenza di rendering a quella successiva o si stanno formulando ipotesi che non supportano i risultati effettivi dell'esperimento, le informazioni seguenti possono essere utili per comprendere il motivo.
ms.assetid: f969be42-d541-4e8d-aec4-eb9508bcc7cf
title: Profilatura precisa delle chiamate API Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6457e47da58a3614270f89eefa1cfa33fbf30cf26544c1013d010696a68e4602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097493"
---
# <a name="accurately-profiling-direct3d-api-calls-direct3d-9"></a>Profilatura precisa delle chiamate API Direct3D (Direct3D 9)

-   [Profilatura accurata di Direct3D è difficile](#accurately-profiling-direct3d-is-difficult)
-   [Come profilare in modo accurato una sequenza di rendering Direct3D](#how-to-accurately-profile-a-direct3d-render-sequence)
-   [Profilatura delle modifiche dello stato Direct3D](#profiling-direct3d-state-changes)
-   [Summary](#summary)
-   [Appendice](#appendix)

Dopo aver creato un'applicazione Microsoft Direct3D funzionale e averne migliorato le prestazioni, in genere si usa uno strumento di profilatura pre-installato o una tecnica di misurazione personalizzata per misurare il tempo necessario per eseguire una o più chiamate API (Application Programming Interface). Se questa operazione è stata eseguita ma si stanno ottenendo risultati temporali che variano da una sequenza di rendering a quella successiva o si stanno formulando ipotesi che non supportano i risultati effettivi dell'esperimento, le informazioni seguenti possono essere utili per comprendere il motivo.

Le informazioni fornite in questo articolo si basano sul presupposto che si abbia una conoscenza e un'esperienza con gli elementi seguenti:

-   Programmazione C/C++
-   Programmazione dell'API Direct3D
-   Misurazione della temporizzazione dell'API
-   La scheda video e il relativo driver software
-   Possibili risultati inspiegabili dall'esperienza di profilatura precedente

## <a name="accurately-profiling-direct3d-is-difficult"></a>Profilatura accurata di Direct3D è difficile

Un profiler segnala la quantità di tempo impiegato in ogni chiamata API. Questa operazione viene eseguita per migliorare le prestazioni individuando e ottimizzare le aree sensibili. Esistono diversi tipi di profiler e tecniche di profilatura.

-   Un profiler di campionamento è inattivo per la maggior parte del tempo, a intervalli specifici per campionare (o registrare) le funzioni in esecuzione. Restituisce la percentuale di tempo impiegato in ogni chiamata. In genere, un profiler di campionamento non è molto invasivo per l'applicazione e ha un impatto minimo sull'overhead per l'applicazione.
-   Un profiler di strumentazione misura il tempo effettivo necessario per la restituzione di una chiamata. Richiede la compilazione di delimitatori di avvio e arresto in un'applicazione. Un profiler di strumentazione è relativamente più invasivo per un'applicazione rispetto a un profiler di campionamento.
-   È anche possibile usare una tecnica di profilatura personalizzata con un timer a prestazioni elevate. Ciò produce risultati molto simili a un profiler di strumentazione.

Il tipo di profiler o tecnica di profilatura usata fa solo parte della sfida di generare misurazioni accurate.

La profilatura offre risposte che consentono di bilanciare le prestazioni. Si supponga, ad esempio, di sapere che una chiamata API esegue una media di 1000 cicli di clock. È possibile asserire alcune conclusioni sulle prestazioni, ad esempio:

-   Una CPU a 2 GHz (che impiega il 50% del tempo di rendering) è limitata alla chiamata di questa API 1 milione di volte al secondo.
-   Per ottenere 30 fotogrammi al secondo, non è possibile chiamare questa API più di 33.000 volte per fotogramma.
-   È possibile eseguire il rendering solo di 3,3.000 oggetti per frame (presupponendo 10 di queste chiamate API per la sequenza di rendering di ogni oggetto).

In altre parole, se si ha tempo sufficiente per ogni chiamata API, è possibile rispondere a una domanda di budget, ad esempio il numero di primitive di cui è possibile eseguire il rendering in modo interattivo. Ma i numeri non elaborati restituiti da un profiler di strumentazione non risponderanno in modo accurato alle domande di budget. Ciò è dovuto al fatto che la pipeline grafica presenta problemi di progettazione complessi, ad esempio il numero di componenti che devono funzionare, il numero di processori che controllano il flusso di lavoro tra i componenti e le strategie di ottimizzazione implementate nel runtime e in un driver progettato per rendere la pipeline più efficiente.

### <a name="each-api-call-goes-through-several-components"></a>Ogni chiamata API passa attraverso diversi componenti

Ogni chiamata viene elaborata da diversi componenti durante il percorso dall'applicazione alla scheda video. Si consideri, ad esempio, la sequenza di rendering seguente contenente due chiamate per disegnare un singolo triangolo:


```
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
```



Il diagramma concettuale seguente illustra i diversi componenti attraverso i quali le chiamate devono passare.

![diagramma dei componenti grafici a cui passano le chiamate API](images/microbenchmarkinstructionflow2.png)

L'applicazione richiama Direct3D che controlla la scena, gestisce le interazioni dell'utente e determina come viene eseguito il rendering. Tutto questo lavoro viene specificato nella sequenza di rendering, che viene inviata al runtime tramite chiamate API Direct3D. La sequenza di rendering è praticamente indipendente dall'hardware, ovvero le chiamate API sono indipendenti dall'hardware, ma un'applicazione è a conoscenza delle funzionalità supportate da una scheda video.

Il runtime converte queste chiamate in un formato indipendente dal dispositivo. Il runtime gestisce tutte le comunicazioni tra l'applicazione e il driver, in modo che un'applicazione verrà eseguita su più componenti hardware compatibili (a seconda delle funzionalità necessarie). Quando si misura una chiamata di funzione, un profiler di strumentazione misura il tempo impiegato in una funzione e il tempo per la restituzione della funzione. Una limitazione di un profiler di strumentazione è che potrebbe non includere il tempo necessario a un driver per inviare il lavoro risultante alla scheda video né il tempo necessario alla scheda video per elaborare il lavoro. In altre parole, un profiler di strumentazione predefinito non riesce a attribuite tutto il lavoro associato a ogni chiamata di funzione.

Il driver software usa informazioni specifiche dell'hardware sulla scheda video per convertire i comandi indipendenti dal dispositivo in una sequenza di comandi della scheda video. I driver possono anche ottimizzare la sequenza di comandi inviati alla scheda video, in modo che il rendering sulla scheda video venga eseguito in modo efficiente. Queste ottimizzazioni possono causare problemi di profilatura perché la quantità di lavoro eseguita non è quella che sembra essere (potrebbe essere necessario comprendere le ottimizzazioni per conto di tali ottimizzazioni). Il driver restituisce in genere il controllo al runtime prima che la scheda video abbia terminato l'elaborazione di tutti i comandi.

La scheda video esegue la maggior parte del rendering combinando i dati del buffer del vertice e dell'indice, le trame, le informazioni sullo stato di rendering e i comandi grafici. Al termine del rendering della scheda video, il lavoro creato dalla sequenza di rendering è completo.

Ogni chiamata API Direct3D deve essere elaborata da ogni componente (runtime, driver e scheda video) per eseguire il rendering di qualsiasi elemento.

### <a name="there-is-more-than-one-processor-controlling-the-components"></a>Sono presenti più processori che controllano i componenti

La relazione tra questi componenti è ancora più complessa, perché l'applicazione, il runtime e il driver sono controllati da un processore e la scheda video è controllata da un processore separato. Il diagramma seguente illustra due tipi di processori: un'unità di elaborazione centrale (CPU) e un'unità di elaborazione grafica (GPU).

![diagramma di una CPU e di una gpu e dei relativi componenti](images/microbenchmarkprocessors.png)

I sistemi PC hanno almeno una CPU e una GPU, ma possono avere più di una o entrambe. Le CPU si trovano sulla scheda madre e le GPU si trovano nella scheda madre o nella scheda video. La velocità della CPU è determinata da un chip di clock sulla scheda madre e la velocità della GPU è determinata da un chip di clock separato. L'orologio della CPU controlla la velocità del lavoro eseguito dall'applicazione, dal runtime e dal driver. L'applicazione invia il lavoro alla GPU tramite il runtime e il driver.

La CPU e la GPU vengono in genere eseguite a velocità diverse, indipendentemente l'una dall'altra. La GPU può rispondere al lavoro non appena il lavoro è disponibile (presupponendo che la GPU abbia terminato l'elaborazione del lavoro precedente). Il lavoro della GPU viene eseguito in parallelo con il lavoro della CPU, come evidenziato dalla linea curva nella figura precedente. Un profiler misura in genere le prestazioni della CPU, non della GPU. Ciò rende difficile la profilatura, perché le misurazioni effettuate da un profiler di strumentazione includono il tempo di CPU, ma potrebbero non includere il tempo GPU.

Lo scopo della GPU è l'off-load dell'elaborazione dalla CPU a un processore appositamente progettato per il lavoro grafico. Nelle schede video moderne, la GPU sostituisce gran parte del lavoro di trasformazione e illuminazione nella pipeline dalla CPU alla GPU. In questo modo si riduce notevolmente il carico di lavoro della CPU, lasciando più cicli di CPU disponibili per altre elaborazioni. Per ottimizzare un'applicazione grafica per ottenere prestazioni ottimali, è necessario misurare le prestazioni della CPU e della GPU e bilanciare il lavoro tra i due tipi di processori.

Questo documento non tratta argomenti relativi alla misurazione delle prestazioni della GPU o al bilanciamento del lavoro tra CPU e GPU. Per comprendere meglio le prestazioni di una GPU (o di una scheda video specifica), visitare il sito Web del fornitore per altre informazioni sulle prestazioni della GPU. Questo documento è invece in particolare in particolare sul lavoro svolto dal runtime e dal driver riducendo il lavoro della GPU a una quantità trascurabile. In parte, ciò si basa sull'esperienza con cui le applicazioni che riscontrano problemi di prestazioni sono in genere limitate alla CPU.

### <a name="runtime-and-driver-optimizations-can-mask-api-measurements"></a>Le ottimizzazioni di runtime e driver possono mascherare le misurazioni dell'API

Il runtime include un'ottimizzazione delle prestazioni che può sovraccaricare la misurazione di una singola chiamata. Ecco uno scenario di esempio che illustra questo problema. Si consideri la sequenza di rendering seguente:


```
  BeginScene();
    ...
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
    ...
  EndScene();
  Present();
```



Esempio 1: Sequenza di rendering semplice

Esaminando i risultati delle due chiamate nella sequenza di rendering, un profiler di strumentazione potrebbe restituire risultati simili ai seguenti:


```
Number of cycles for SetTexture       : 100
Number of cycles for DrawPrimitive    : 950,500
```



Il profiler restituisce il numero di cicli della CPU necessari per elaborare il lavoro associato a ogni chiamata (tenere presente che la GPU non è inclusa in questi numeri perché la GPU non ha ancora iniziato a usare questi comandi). Poiché [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ha richiesto quasi un milione di cicli per l'elaborazione, è possibile concludere che non è molto efficiente. Tuttavia, si scoprirà presto perché questa conclusione non è corretta e come è possibile generare risultati che possono essere usati per l'impostazione del budget.

### <a name="measuring-state-changes-requires-careful-render-sequences"></a>La misurazione delle modifiche di stato richiede sequenze di rendering attente

Tutte le chiamate diverse da [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)o [**Clear**](/windows/desktop/api) (ad esempio [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), [**SetVertexDeclaration**](/windows/desktop/api)e [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) producono una modifica dello stato. Ogni modifica dello stato imposta lo stato della pipeline che controlla come verrà eseguito il rendering.

Le ottimizzazioni nel runtime e/o nel driver sono progettate per velocizzare il rendering riducendo la quantità di lavoro necessaria. Di seguito sono riportate alcune ottimizzazioni delle modifiche di stato che possono causare un problema di media dei profili:

-   Un driver (o il runtime) potrebbe salvare una modifica dello stato come stato locale. Poiché il driver può operare in un algoritmo "lazy" (posticipando il lavoro fino a quando non è assolutamente necessario), il lavoro associato ad alcune modifiche di stato potrebbe subire ritardi.
-   Il runtime (o un driver) può rimuovere le modifiche di stato ottimizzando . Un esempio potrebbe essere la rimozione di una modifica di stato ridondante che disabilita l'illuminazione perché l'illuminazione è stata disabilitata in precedenza.

Non esiste un modo infallibile per esaminare una sequenza di rendering e concludere quali modifiche dello stato impostano un dirty bit e rinviare il lavoro o vengono semplicemente rimosse dall'ottimizzazione. Anche se è possibile identificare le modifiche di stato ottimizzate nel runtime o nel driver attuale, è probabile che il runtime o il driver di domani sia aggiornato. Inoltre, non si sa immediatamente quale fosse lo stato precedente, quindi è difficile identificare le modifiche dello stato ridondante. L'unico modo per verificare il costo di una modifica dello stato è misurare la sequenza di rendering che include le modifiche dello stato.

Come si può vedere, le complicazioni causate dalla presenza di più processori, i comandi elaborati da più componenti e le ottimizzazioni integrate nei componenti rendono difficile prevedere la profilatura. Nella sezione successiva verranno affrontate ognuna di queste problematiche di profilatura. Verranno visualizzate sequenze di rendering Direct3D di esempio, con le tecniche di misurazione associate. Con queste informazioni, sarà possibile generare misurazioni accurate e ripetibili sulle singole chiamate.

## <a name="how-to-accurately-profile-a-direct3d-render-sequence"></a>Come profilare in modo accurato una sequenza di rendering Direct3D

Ora che sono state evidenziate alcune delle problematiche di profilatura, questa sezione illustra le tecniche che consentono di generare misurazioni del profilo che possono essere usate per l'impostazione del budget. Misurazioni accurate e ripetibili della profilatura sono possibili se si comprende la relazione tra i componenti controllati dalla CPU e si evitano ottimizzazioni delle prestazioni implementate dal runtime e dal driver.

Per iniziare, è necessario essere in grado di misurare in modo accurato il tempo di esecuzione di una singola chiamata API.

### <a name="pick-an-accurate-measurement-tool-like-queryperformancecounter"></a>Selezionare uno strumento di misurazione accurato come QueryPerformanceCounter

Il sistema Windows microsoft include un timer ad alta risoluzione che può essere usato per misurare i tempi trascorsi ad alta risoluzione. Il valore corrente di un timer di questo tipo può essere restituito [**usando QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Dopo aver **richiamato QueryPerformanceCounter** per restituire i valori di inizio e arresto, la differenza tra i due valori può essere convertita nel tempo trascorso effettivo (in secondi) usando **QueryPerformanceCounter**.

I vantaggi [**dell'uso di QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) sono che è disponibile in Windows ed è facile da usare. È sufficiente racchiudere le chiamate con **una chiamata QueryPerformanceCounter** e salvare i valori di avvio e arresto. Questo documento illustra quindi come usare **QueryPerformanceCounter** per profilare i tempi di esecuzione, in modo analogo al modo in cui verrebbe misurato da un profiler di strumentazione. Ecco un esempio che illustra come incorporare **QueryPerformanceCounter** nel codice sorgente:


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



Esempio 2: Implementazione della profilatura personalizzata con QPC

start e stop sono due numeri interi di grandi dimensioni che conteneranno i valori di avvio e arresto restituiti dal timer a prestazioni elevate. Si noti che QueryPerformanceCounter(&start) viene chiamato subito prima che [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e QueryPerformanceCounter(&stop) venga chiamato subito dopo [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). Dopo aver restituito il valore di arresto, viene chiamato QueryPerformanceFrequency per restituire freq, ovvero la frequenza del timer ad alta risoluzione. In questo ipotetico esempio si supponga di ottenere i risultati seguenti per start, stop e freq:



| Variabile locale | Numero di tick |
|----------------|-----------------|
| Avvio          | 1792998845094   |
| stop           | 1792998845102   |
| Freq           | 3579545         |



 

È possibile convertire questi valori nel numero di cicli necessari per eseguire le chiamate API come descritto di seguito:


```
# ticks = (stop - start) = 1792998845102 - 1792998845094 = 8 ticks

# cycles = CPU speed * number of ticks / QPF
# 4568   = 2 GHz      * 8              / 3,579,545
```



In altre parole, sono necessari circa 4568 cicli di clock per elaborare [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) in questo computer a 2 GHz. È possibile convertire questi valori nel tempo effettivo necessario per eseguire tutte le chiamate come queste:


```
(stop - start)/ freq = elapsed time
8 ticks / 3,579,545 = 2.2E-6 seconds or between 2 and 3 microseconds.
```



L'uso di QueryPerformanceCounter richiede l'aggiunta di misurazioni di avvio e arresto alla sequenza di rendering e l'uso di QueryPerformanceFrequency per convertire la differenza (numero di tick) nel numero di cicli cpu o nel tempo effettivo. L'identificazione della tecnica di misurazione è un buon inizio per lo sviluppo di un'implementazione di profilatura personalizzata. Ma prima di iniziare a eseguire le misurazioni, è necessario sapere come gestire la scheda video.

### <a name="focus-on-cpu-measurements"></a>Concentrarsi sulle misurazioni della CPU

Come indicato in precedenza, la CPU e la GPU funzionano in parallelo per elaborare il lavoro generato dalle chiamate API. Un'applicazione reale richiede la profilatura di entrambi i tipi di processori per determinare se l'applicazione è limitata alla CPU o a GPU. Poiché le prestazioni della GPU sono specifiche del fornitore, sarebbe molto difficile produrre risultati in questo documento che coprono l'ampia gamma di schede video disponibili.

Al contrario, questo documento si concentrerà solo sulla profilatura del lavoro eseguito dalla CPU usando una tecnica personalizzata per misurare il lavoro di runtime e driver. Il lavoro della GPU verrà ridotto a una quantità non significativa, in modo che i risultati della CPU siano più visibili. Uno dei vantaggi di questo approccio è che questa tecnica produce risultati nell'appendice che si dovrebbe essere in grado di correlare con le misurazioni. Per ridurre il lavoro richiesto dalla scheda video a un livello irrilevante, è sufficiente ridurre il lavoro di rendering alla quantità minima possibile. Questa operazione può essere eseguita limitando le chiamate di disegno per eseguire il rendering di un singolo triangolo e può essere ulteriormente vincolata in modo che ogni triangolo contenga un solo pixel.

L'unità di misura usata in questo documento per misurare il lavoro della CPU sarà il numero di cicli di clock della CPU anziché il tempo effettivo. I cicli di clock della CPU hanno il vantaggio di essere più portabili (per le applicazioni con limiti di CPU) rispetto al tempo trascorso effettivo tra computer con velocità di CPU diverse. Può essere facilmente convertito in tempo effettivo, se lo si desidera.

Questo documento non tratta argomenti relativi al bilanciamento del carico di lavoro tra la CPU e la GPU. Tenere presente che l'obiettivo di questo documento non è misurare le prestazioni complessive di un'applicazione, ma mostrare come misurare in modo accurato il tempo necessario al runtime e al driver per elaborare le chiamate API. Con queste misurazioni accurate, è possibile eseguire l'attività di impostazione del budget della CPU per comprendere determinati scenari di prestazioni.

### <a name="controlling-runtime-and-driver-optimizations"></a>Controllo delle ottimizzazioni di runtime e driver

Con una tecnica di misurazione identificata e una strategia per ridurre il lavoro della GPU, il passaggio successivo consiste nel comprendere le ottimizzazioni di runtime e driver che possono essere utilizzate durante la profilatura.

Il lavoro della CPU può essere suddiviso in tre bucket: il lavoro dell'applicazione, il lavoro di runtime e il lavoro del driver. Ignorare il lavoro dell'applicazione perché è sotto il controllo del programmatore. Dal punto di vista dell'applicazione, il runtime e il driver sono come caselle nere, perché l'applicazione non ha alcun controllo su ciò che viene implementato in esse. La chiave è comprendere le tecniche di ottimizzazione che possono essere implementate nel runtime e nel driver. Se non si comprendono queste ottimizzazioni, è molto facile passare alla conclusione errata sulla quantità di lavoro che la CPU sta eseguendo in base alle misurazioni del profilo. In particolare, sono disponibili due argomenti relativi a un elemento denominato buffer dei comandi e a cosa può fare per offuscare la profilatura. tra cui:

-   Ottimizzazione di runtime con il buffer dei comandi. Il buffer dei comandi è un'ottimizzazione di runtime che riduce l'impatto di una transizione di modalità. Per controllare l'intervallo della transizione di modalità, vedere [Controllo del buffer dei comandi](#controlling-the-command-buffer).
-   Negazione degli effetti di temporizzazione del buffer dei comandi. Il tempo trascorso di una transizione di modalità può avere un impatto significativo sulle misurazioni di profilatura. La strategia consiste nel rendere [la sequenza di rendering grande rispetto alla transizione di modalità](#make-the-render-sequence-large-compared-to-the-mode-transition).

### <a name="controlling-the-command-buffer"></a>Controllo del buffer dei comandi

Quando un'applicazione esegue una chiamata API, il runtime converte la chiamata API in un formato indipendente dal dispositivo (che verrà chiamato un comando) e la archivia nel buffer dei comandi. Il buffer dei comandi viene aggiunto al diagramma seguente.

![diagramma dei componenti cpu, incluso un buffer dei comandi](images/microbenchmarkcommandbuffer2.png)

Ogni volta che l'applicazione esegue un'altra chiamata API, il runtime ripete questa sequenza e aggiunge un altro comando al buffer dei comandi. A un certo punto, il runtime svuota il buffer (inviando i comandi al driver). In Windows XP, lo svuotamento del buffer dei comandi causa una transizione di modalità quando il sistema operativo passa dal runtime (in esecuzione in modalità utente) al driver (in esecuzione in modalità kernel), come illustrato nel diagramma seguente.

-   modalità utente: modalità processore senza privilegi che esegue il codice dell'applicazione. Le applicazioni in modalità utente non possono accedere ai dati di sistema se non tramite i servizi di sistema.
-   modalità kernel: modalità processore con privilegi in cui Windows codice executive basato su privilegi. Un driver o un thread in esecuzione in modalità kernel ha accesso a tutta la memoria di sistema, all'accesso diretto all'hardware e alle istruzioni della CPU per eseguire operazioni di I/O con l'hardware.

![Diagramma delle transizioni tra la modalità utente e la modalità kernel](images/microbenchmarkcommandbuffer3.png)

La transizione avviene ogni volta che la CPU passa dalla modalità utente alla modalità kernel (e viceversa) e il numero di cicli necessari è elevato rispetto a una singola chiamata API. Se il runtime ha inviato ogni chiamata API al driver quando è stato richiamato, ogni chiamata API comporta il costo di una transizione di modalità.

Il buffer dei comandi è invece un'ottimizzazione di runtime progettata per ridurre il costo effettivo della transizione di modalità. Il buffer dei comandi accoda molti comandi del driver in preparazione di una transizione in modalità singola. Quando il runtime aggiunge un comando al buffer dei comandi, il controllo viene restituito all'applicazione. Un profiler non è in grado di sapere che i comandi del driver probabilmente non sono stati ancora inviati al driver. Di conseguenza, i numeri restituiti da un profiler di strumentazione non disponibile sono fuorvianti perché misura il lavoro di runtime, ma non il lavoro del driver associato.

### <a name="profile-results-without-a-mode-transition"></a>Profilare i risultati senza una transizione di modalità

Usando la sequenza di rendering dell'esempio 2, ecco alcune misurazioni di temporizzazione tipiche che illustrano la grandezza di una transizione di modalità. Supponendo che [**le chiamate SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) non causano una transizione di modalità, un profiler di strumentazione non disponibile potrebbe restituire risultati simili ai seguenti:


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
```



Ognuno di questi numeri è la quantità di tempo necessario al runtime per aggiungere queste chiamate al buffer dei comandi. Poiché non è presente alcuna transizione di modalità, il driver non ha ancora eseguito alcuna operazione. I risultati del profiler sono accurati, ma non misurano tutto il lavoro che alla fine la sequenza di rendering causerà l'esecuzione della CPU.

### <a name="profile-results-with-a-mode-transition"></a>Profilare i risultati con una transizione di modalità

A questo punto, esaminare cosa accade per lo stesso esempio quando si verifica una transizione di modalità. Questa volta, si supponga che [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) [**e DrawPrimitive causeranno**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) una transizione di modalità. Ancora una volta, un profiler di strumentazione predefinito potrebbe restituire risultati simili ai seguenti:


```
Number of cycles for SetTexture           : 98 
Number of cycles for DrawPrimitive        : 946,900
```



Il tempo misurato per [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) è circa lo stesso, tuttavia, l'aumento significativo della quantità di tempo impiegato in [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) è dovuto alla transizione di modalità. Ecco cosa accade:

1.  Si supponga che il buffer dei comandi abbia spazio per un comando prima dell'avvio della sequenza di rendering.
2.  [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) viene convertito in un formato indipendente dal dispositivo e aggiunto al buffer dei comandi. In questo scenario, questa chiamata riempie il buffer dei comandi.
3.  Il runtime tenta di aggiungere [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) al buffer dei comandi, ma non può, perché è pieno. Il runtime svuota invece il buffer dei comandi. In questo modo viene attivata la transizione in modalità kernel. Si supponga che la transizione richiede circa 5000 cicli. Questo tempo contribuisce al tempo impiegato in **DrawPrimitive.**
4.  Il driver elabora quindi il lavoro associato a tutti i comandi svuotati dal buffer dei comandi. Si supponga che il tempo necessario al driver per elaborare i comandi che hanno quasi riempito il buffer dei comandi sia di circa 935.000 cicli. Si supponga che il lavoro del driver associato [**a SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) sia di circa 2750 cicli. Questo tempo contribuisce al tempo impiegato in [**DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
5.  Quando il driver termina il lavoro, la transizione in modalità utente restituisce il controllo al runtime. Il buffer dei comandi è ora vuoto. Si supponga che la transizione richiede circa 5000 cicli.
6.  La sequenza di rendering termina convertendo [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) e aggiungendola al buffer dei comandi. Si supponga che questa operazione richiede circa 900 cicli. Questo tempo contribuisce al tempo impiegato in **DrawPrimitive.**

Riepilogando i risultati, viene visualizzato:


```
DrawPrimitive = kernel-transition + driver work    + user-transition + runtime work
DrawPrimitive = 5000              + 935,000 + 2750 + 5000            + 900
DrawPrimitive = 947,950  
```



Proprio come la misurazione per [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) senza la transizione di modalità (900 cicli), la misura per **DrawPrimitive** con la transizione di modalità (947.950 cicli) è accurata ma inutile in termini di budget del lavoro della CPU. Il risultato contiene le operazioni di runtime corrette, il driver funziona per [**SetTexture,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)il driver funziona per tutti i comandi che precedono **SetTexture** e due transizioni di modalità. Tuttavia, nella misurazione manca il lavoro del driver **DrawPrimitive.**

Una transizione di modalità può verificarsi in risposta a qualsiasi chiamata. Dipende da ciò che era in precedenza nel buffer dei comandi. È necessario controllare la transizione di modalità per comprendere la quantità di lavoro della CPU (runtime e driver) associata a ogni chiamata. A tale scopo, è necessario un meccanismo per controllare il buffer dei comandi e la tempistica della transizione di modalità.

### <a name="the-query-mechanism"></a>Meccanismo di query

Il meccanismo di query in Microsoft Direct3D 9 è stato progettato per consentire al runtime di eseguire query sulla GPU per l'avanzamento e restituire determinati dati dalla GPU. Durante la profilatura, se il lavoro della GPU è ridotto al minimo in modo da avere un impatto trascurabile sulle prestazioni, è possibile restituire lo stato dalla GPU per facilitare la misurazione del lavoro del driver. Dopo tutto, il lavoro del driver è completo quando la GPU ha visto i comandi del driver. Inoltre, il meccanismo di query può essere coeso nel controllo di due caratteristiche del buffer dei comandi importanti per la profilatura: quando il buffer dei comandi si svuota e quanto lavoro si trova nel buffer.

Ecco la stessa sequenza di rendering usando il meccanismo di query:


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



Esempio 3: Uso di una query per controllare il buffer dei comandi

Ecco una spiegazione più dettagliata di ognuna di queste righe di codice:

1.  Creare una query di eventi creando un oggetto query con D3DQUERYTYPE \_ EVENT.
2.  Aggiungere un marcatore di evento di query al buffer dei comandi [**chiamando Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)([**D3DISSUE \_ END**](d3dissue-end.md)). Questo marcatore indica al driver di rilevare quando la GPU termina l'esecuzione di tutti i comandi che precedono il marcatore.
3.  La prima chiamata svuota il buffer dei comandi perché la chiamata a [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) [**con D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md) forza lo svuotamento del buffer dei comandi. Ogni chiamata successiva controlla la GPU per verificare quando termina l'elaborazione di tutto il lavoro del buffer dei comandi. Questo ciclo non restituisce S \_ OK finché la GPU non è inattiva.
4.  Campionare l'ora di inizio.
5.  Richiamare le chiamate API profilate.
6.  Aggiungere un secondo marcatore di evento di query al buffer dei comandi. Questo marcatore verrà usato per tenere traccia del completamento delle chiamate.
7.  La prima chiamata svuota il buffer dei comandi perché la chiamata a [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) [**con D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md) forza lo svuotamento del buffer dei comandi. Quando la GPU termina l'elaborazione di tutto il lavoro del buffer dei comandi, **GetData** restituisce S OK e il ciclo viene chiuso perché la \_ GPU è inattiva.
8.  Campionare l'ora di arresto.

Ecco i risultati misurati con QueryPerformanceCounter e QueryPerformanceFrequency:



| Variabile locale | Numero di tick |
|----------------|-----------------|
| Avvio          | 1792998845060   |
| stop           | 1792998845090   |
| Freq           | 3579545         |



 

Conversione dei tick in cicli (in un computer a 2 GHz):


```
# ticks  = (stop - start) = 1792998845090 - 1792998845060 = 30 ticks
# cycles = CPU speed * number of ticks / QPF
# 16,450 = 2 GHz      * 30             / 3,579,545
```



Ecco la suddivisione del numero di cicli per chiamata:


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
Number of cycles for Issue                : 200
Number of cycles for GetData              : 16,450
```



Il meccanismo di query ha consentito di controllare il runtime e il lavoro del driver misurato. Per comprendere ognuno di questi numeri, ecco cosa accade in risposta a ognuna delle chiamate API, insieme agli intervalli stimati:

1.  La prima chiamata svuota il buffer dei comandi chiamando [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) con [**D3DGETDATA \_ FLUSH.**](d3dgetdata-flush.md) Quando la GPU termina l'elaborazione di tutto il lavoro del buffer dei comandi, **GetData** restituisce S OK e il ciclo viene chiuso perché la \_ GPU è inattiva.
2.  La sequenza di rendering inizia convertendo [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) in un formato indipendente dal dispositivo e aggiungendolo al buffer dei comandi. Si supponga che questa operazione richiede circa 100 cicli.
3.  [**DrawPrimitive viene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) convertito e aggiunto al buffer dei comandi. Si supponga che questa operazione richiede circa 900 cicli.
4.  [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) aggiunge un marcatore di query al buffer dei comandi. Si supponga che questa operazione richiede circa 200 cicli.
5.  [**GetData fa**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) sì che il buffer dei comandi sia svuotato, forzando la transizione in modalità kernel. Si supponga che questa operazione richiede circa 5000 cicli.
6.  Il driver elabora quindi il lavoro associato a tutte e quattro le chiamate. Si supponga che il tempo del driver per elaborare [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) sia di circa 2964 cicli, [**che DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) sia di circa 3600 [**cicli,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) che il problema sia di circa 200 cicli. Il tempo totale del driver per tutti e quattro i comandi è quindi di circa 6450 cicli.
    > [!Note]  
    > Il driver richiede anche un po' di tempo per vedere qual è lo stato della GPU. Poiché il lavoro della GPU è semplice, la GPU deve essere già eseguita. [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) restituirà S \_ OK in base alla probabilità che la GPU sia terminata.

     

7.  Quando il driver termina il lavoro, la transizione in modalità utente restituisce il controllo al runtime. Il buffer dei comandi è ora vuoto. Si supponga che questa operazione richiede circa 5000 cicli.

I numeri per [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) includono:


```
GetData = kernel-transition + driver work + user-transition
GetData = 5000              + 6450        + 5000           
GetData = 16,450  

driver work = SetTexture + DrawPrimitive + Issue = 
driver work = 2964       + 3600          + 200   = 6450 cycles 
```



Il meccanismo di query usato in combinazione con QueryPerformanceCounter misura tutto il lavoro della CPU. Questa operazione viene eseguita con una combinazione di marcatori di query e confronti dello stato delle query. I marcatori di query di avvio e arresto aggiunti al buffer dei comandi vengono usati per controllare la quantità di lavoro nel buffer. Attendendo che venga restituito il codice restituito corretto, la misurazione di avvio viene effettuata subito prima dell'avvio di una sequenza di rendering pulita e la misurazione di arresto viene effettuata subito dopo che il driver ha completato le operazioni associate al contenuto del buffer dei comandi. Ciò consente di acquisire in modo efficace il lavoro della CPU eseguito dal runtime e dal driver.

Ora che si conoscono il buffer dei comandi e l'effetto che può avere sulla profilatura, è necessario sapere che esistono alcune altre condizioni che possono causare lo svuotamento del buffer dei comandi da parte del runtime. È necessario fare attenzione a questi elementi nelle sequenze di rendering. Alcune di queste condizioni sono in risposta alle chiamate API, altre sono in risposta alle modifiche delle risorse nel runtime. Una delle condizioni seguenti causerà una transizione di modalità:

-   Quando uno dei metodi di blocco ([**Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)) viene chiamato su un vertex buffer, index buffer o texture (in determinate condizioni con determinati flag).
-   Quando viene creato un dispositivo o un vertex buffer, index buffer o trama.
-   Quando un dispositivo o un vertex buffer, index buffer o trama viene eliminato dall'ultima versione.
-   Quando [**viene chiamato ValidateDevice.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice)
-   Quando [**viene chiamato Present.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
-   Quando il buffer dei comandi si riempie.
-   Quando [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) viene chiamato con D3DGETDATA \_ FLUSH.

Prestare attenzione a controllare queste condizioni nelle sequenze di rendering. Ogni volta che viene aggiunta una transizione di modalità, alle misurazioni di profilatura verranno aggiunti 10.000 cicli di lavoro del driver. Inoltre, il buffer dei comandi non viene ridimensionato in modo statico. Il runtime può modificare le dimensioni del buffer in risposta alla quantità di lavoro generata dall'applicazione. Si tratta di un'altra ottimizzazione che dipende da una sequenza di rendering.

Prestare quindi attenzione alle transizioni della modalità di controllo durante la profilatura. Il meccanismo di query offre un metodo affidabile per svuotare il buffer dei comandi in modo che sia possibile controllare l'intervallo di transizione della modalità e la quantità di lavoro contenuta nel buffer. Tuttavia, anche questa tecnica può essere migliorata riducendo il tempo di transizione della modalità per renderla irrilevante rispetto al risultato misurato.

### <a name="make-the-render-sequence-large-compared-to-the-mode-transition"></a>Rendere grande la sequenza di rendering rispetto alla transizione di modalità

Nell'esempio precedente, l'opzione in modalità kernel e l'opzione in modalità utente utilizzano circa 10.000 cicli che non hanno nulla a che fare con il lavoro di runtime e driver. Poiché la transizione di modalità è incorporata nel sistema operativo, non può essere ridotta a zero. Per rendere irrilevante la transizione di modalità, la sequenza di rendering deve essere regolata in modo che il driver e il runtime funzionino in modo da avere un ordine di grandezza maggiore rispetto ai commutatori di modalità. È possibile provare a eseguire una sottrazione per rimuovere le transizioni, ma l'ammortizzazione del costo su un costo della sequenza di rendering molto più elevato è più affidabile.

La strategia per ridurre la transizione di modalità fino a quando non diventa irrilevante consiste nell'aggiungere un ciclo alla sequenza di rendering. Ad esempio, esaminare i risultati della profilatura se viene aggiunto un ciclo che ripeterà la sequenza di rendering 1500 volte:


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



Esempio 4: Aggiungere un ciclo alla sequenza di rendering

Ecco i risultati misurati con QueryPerformanceCounter e QueryPerformanceFrequency:



| Variabile locale | Number of Tics |
|----------------|----------------|
| Avvio          | 1792998845000  |
| stop           | 1792998847084  |
| Freq           | 3579545        |



 

L'uso di QueryPerformanceCounter misura ora 2.840 tick. La conversione dei tick in cicli è identica a come è già stato illustrato:


```
# ticks  = (stop - start) = 1792998847084 - 1792998845000 = 2840 ticks
# cycles    = machine speed * number of ticks / QPF
# 6,900,000 = 2 GHz          * 2840           / 3,579,545
```



In altre parole, sono necessari circa 6,9 milioni di cicli in questo computer a 2 GHz per elaborare le chiamate a 1500 nel ciclo di rendering. Dei 6,9 milioni di cicli, la quantità di tempo nelle transizioni di modalità è di circa 10.000, quindi ora i risultati del profilo misurano quasi interamente il lavoro associato a [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) [**e DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)

Si noti che l'esempio di codice richiede una matrice di due trame. Per evitare un'ottimizzazione di runtime che rimuove [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) se imposta lo stesso puntatore di trama ogni volta che viene chiamato, è sufficiente usare una matrice di due trame. In questo modo, ogni volta che si scorre il ciclo, il puntatore della trama cambia e viene eseguito il lavoro completo associato a **SetTexture.** Assicurarsi che entrambe le trame siano delle stesse dimensioni e dello stesso formato, in modo che nessun altro stato cambi quando la trama lo fa.

È ora disponibile una tecnica per la profilatura di Direct3D. Si basa sul contatore delle prestazioni elevate (QueryPerformanceCounter) per registrare il numero di tick necessari alla CPU per elaborare il lavoro. Il lavoro viene controllato attentamente in modo da essere il runtime e il driver associati alle chiamate API usando il meccanismo di query. Una query fornisce due mezzi di controllo: prima di tutto per svuotare il buffer dei comandi prima dell'avvio della sequenza di rendering e in secondo luogo per restituire al termine del lavoro della GPU.

Finora questo documento ha illustrato come profilare una sequenza di rendering. Ogni sequenza di rendering è stata piuttosto semplice, contenente una [**singola chiamata DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) e una [**chiamata SetTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) Questa operazione è stata eseguita per concentrarsi sul buffer dei comandi e sull'uso del meccanismo di query per controllarlo. Ecco un breve riepilogo di come profilare una sequenza di rendering arbitraria:

-   Usare un contatore delle prestazioni elevate come QueryPerformanceCounter per misurare il tempo necessario per elaborare ogni chiamata API. Usare QueryPerformanceFrequency e la frequenza di clock della CPU per convertirlo nel numero di cicli della CPU per ogni chiamata API.
-   Ridurre al minimo la quantità di operazioni della GPU tramite il rendering degli elenchi di triangoli, in cui ogni triangolo contiene un pixel.
-   Usare il meccanismo di query per svuotare il buffer dei comandi prima della sequenza di rendering. Ciò garantisce che la profilatura acquisirà la quantità corretta di operazioni di runtime e driver associate alla sequenza di rendering.
-   Controllare la quantità di lavoro aggiunto al buffer dei comandi con marcatori di evento di query. Questa stessa query rileva quando la GPU termina il lavoro. Poiché il lavoro della GPU è semplice, è praticamente equivalente alla misurazione del completamento del lavoro del driver.

Tutte queste tecniche vengono usate per profilare le modifiche dello stato. Supponendo di aver letto e compreso come controllare il buffer dei comandi e di aver completato correttamente le misurazioni di base in [**DrawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)si è pronti ad aggiungere modifiche di stato alle sequenze di rendering. Quando si aggiungono modifiche di stato a una sequenza di rendering, esistono alcune problematiche di profilatura aggiuntive. Se si prevede di aggiungere modifiche di stato alle sequenze di rendering, assicurarsi di continuare con la sezione successiva.

## <a name="profiling-direct3d-state-changes"></a>Profilatura delle modifiche dello stato Direct3D

Direct3D usa molti stati di rendering per controllare quasi tutti gli aspetti della pipeline. Le API che causano modifiche di stato includono qualsiasi funzione o metodo diverso da draw \* primitive chiamate.

Le modifiche di stato sono difficili perché potrebbe non essere possibile visualizzare il costo di una modifica dello stato senza rendering. Questo è il risultato dell'algoritmo lazy che il driver e la GPU usano per rinviare il lavoro fino a quando non è assolutamente necessario. In generale, è consigliabile seguire questa procedura per misurare una singola modifica dello stato:

1.  Profilare [**prima DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
2.  Aggiungere una modifica dello stato alla sequenza di rendering e profilare la nuova sequenza.
3.  Sottrarre la differenza tra le due sequenze per ottenere il costo della modifica dello stato.

Naturalmente, tutto ciò che si è appreso sull'uso del meccanismo di query e sull'inserimento della sequenza di rendering in un ciclo per negare il costo della transizione di modalità è ancora valido.

### <a name="profiling-a-simple-state-change"></a>Profilatura di una semplice modifica dello stato

A partire da una sequenza di rendering che [**contiene DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), ecco la sequenza di codice per misurare il costo dell'aggiunta di [**SetTexture:**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)


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



Esempio 5: Misurazione di una chiamata API di modifica dello stato

Si noti che il ciclo contiene due chiamate, [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) [**e DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) La sequenza di rendering esegue il ciclo 1500 volte e genera risultati simili ai seguenti:



| Variabile locale | Number of Tics |
|----------------|----------------|
| Avvio          | 1792998860000  |
| stop           | 1792998870260  |
| Freq           | 3579545        |



 

La conversione dei tick in cicli produce ancora una volta:


```
# ticks  = (stop - start) = 1792998870260 - 1792998860000 = 10,260 ticks
# cycles    = machine speed * number of ticks / QPF
5,775,000   = 2 GHz          * 10,260         / 3,579,545
```



La divisione per il numero di iterazioni nel ciclo produce:


```
5,775,000 cycles / 1500 iterations = 3850 cycles for one iteration
```



Ogni iterazione del ciclo contiene una modifica dello stato e una chiamata di disegno. Sottraendo il risultato della sequenza di rendering [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) si lascia:


```
3850 - 1100 = 2750 cycles for SetTexture
```



Numero medio di cicli per aggiungere [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) a questa sequenza di rendering. Questa stessa tecnica può essere applicata ad altre modifiche di stato.

Perché [**SetTexture viene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) chiamato semplice modifica dello stato? Poiché lo stato impostato è vincolato in modo che la pipeline eserciti la stessa quantità di lavoro ogni volta che lo stato viene modificato. Vincolando entrambe le trame alla stessa dimensione e allo stesso formato si garantisce la stessa quantità di lavoro per ogni **chiamata a SetTexture.**

### <a name="profiling-a-state-change-that-needs-to-be-toggled"></a>Profilatura di una modifica dello stato che deve essere attivata/disattivata

Sono presenti altre modifiche dello stato che causano la modifica della quantità di lavoro eseguita dalla pipeline grafica per ogni iterazione del ciclo di rendering. Ad esempio, se il test z è abilitato, ogni colore di pixel aggiorna una destinazione di rendering solo dopo che il valore z del nuovo pixel è stato testato rispetto al valore z per il pixel esistente. Se il test z è disabilitato, questo test per pixel non viene eseguito e l'output viene scritto molto più velocemente. L'abilitazione o la disabilitazione dello stato z-test modifica notevolmente la quantità di lavoro svolto (dalla CPU e dalla GPU) durante il rendering.

[**SetRenderState richiede**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) uno stato di rendering specifico e un valore di stato per abilitare o disabilitare z-testing. Il valore di stato specifico viene valutato in fase di esecuzione per determinare la quantità di lavoro necessaria. È difficile misurare questa modifica dello stato in un ciclo di rendering e comunque precondizionare lo stato della pipeline in modo che cambi. L'unica soluzione consiste nell'attivare o disattivare la modifica dello stato durante la sequenza di rendering.

Ad esempio, la tecnica di profilatura deve essere ripetuta due volte come segue:

1.  Iniziare profilando la [**sequenza di rendering DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) Chiamare questa linea di base.
2.  Profilare una seconda sequenza di rendering che attiva o disattiva la modifica dello stato. Il ciclo della sequenza di rendering contiene:
    -   Modifica dello stato per impostare lo stato in una condizione "false".
    -   [**DrawPrimitive esattamente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) come la sequenza originale.
    -   Modifica dello stato per impostare lo stato in una condizione "true".
    -   Secondo [**DrawPrimitive per forzare**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) la seconda modifica dello stato da realizzare.
3.  Trovare la differenza tra le due sequenze di rendering. Questa operazione viene eseguita da:
    -   Moltiplicare la [**sequenza DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) di base per 2 perché nella nuova sequenza sono presenti due chiamate **DrawPrimitive.**
    -   Sottrarre il risultato della nuova sequenza dalla sequenza originale.
    -   Dividere il risultato per 2 per ottenere il costo medio della modifica di stato "false" e "true".

Con la tecnica di ciclo usata nella sequenza di rendering, il costo della modifica dello stato della pipeline deve essere misurato impostando lo stato da "true" a "false" e viceversa, per ogni iterazione nella sequenza di rendering. Il significato di "true" e "false" qui non sono valori letterali, questo significa semplicemente che lo stato deve essere impostato in condizioni opposte. In questo modo entrambe le modifiche di stato vengono misurate durante la profilatura. Naturalmente tutto ciò che si è appreso sull'uso del meccanismo di query e sull'inserimento della sequenza di rendering in un ciclo per negare il costo della transizione di modalità si applica ancora.

Ad esempio, di seguito è illustrata la sequenza di codice per la misurazione del costo del test z in modalità on o off:


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



Esempio 5: Misurazione di una modifica dello stato di toggling

Il ciclo attiva o disattiva lo stato eseguendo due [**chiamate SetRenderState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) La prima **chiamata SetRenderState** disabilita il test z e la seconda **setRenderState** abilita il test z. Ogni **SetRenderState** è seguito da [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) in modo che il lavoro associato alla modifica dello stato sia elaborato dal driver anziché solo impostando un dirty bit nel driver.

Questi numeri sono ragionevoli per questa sequenza di rendering:



| Variabile locale | Numero di tick |
|----------------|-----------------|
| Avvio          | 1792998845000   |
| stop           | 1792998861740   |
| Freq           | 3579545         |



 

La conversione dei tick in cicli produce di nuovo:


```
# ticks  = (stop - start) = 1792998861740 - 1792998845000 = 15,120 ticks
# cycles    = machine speed * number of ticks / QPF
 9,300,000  = 2 GHz          * 16,740         / 3,579,545
```



La divisione per il numero di iterazioni nel ciclo produce:


```
9,300,000 cycles / 1500 iterations = 6200 cycles for one iteration
```



Ogni iterazione del ciclo contiene due modifiche di stato e due chiamate di disegno. La sottrazione delle chiamate di disegno (presupponendo 1100 cicli) lascia:


```
6200 - 1100 - 1100 = 4000 cycles for both state changes
```



Questo è il numero medio di cicli per entrambe le modifiche di stato, quindi il tempo medio per ogni modifica di stato è:


```
4000 / 2  = 2000 cycles for each state change
```



Di conseguenza, il numero medio di cicli per abilitare o disabilitare il test z è 2000 cicli. Vale la pena notare che QueryPerformanceCounter misura l'abilitazione z metà del tempo e la disabilitazione z metà del tempo. Questa tecnica misura effettivamente la media di entrambe le modifiche di stato. In altre parole, si misura il tempo necessario per attivare o disattivare uno stato. Usando questa tecnica, non è possibile sapere se i tempi di abilitazione e disabilitazione sono equivalenti poiché è stata misurata la media di entrambi. Tuttavia, si tratta di un numero ragionevole da usare per il budget di uno stato di toggling come applicazione che causa questa modifica di stato può eseguire questa operazione solo tramite il togging di questo stato.

A questo punto è possibile applicare queste tecniche e profilare tutte le modifiche di stato desiderate, giusto? Risposta errata. È comunque necessario prestare attenzione alle ottimizzazioni progettate per ridurre la quantità di lavoro da eseguire. Quando si progettano le sequenze di rendering, è necessario tenere presenti due tipi di ottimizzazioni.

### <a name="watch-out-for-state-change-optimizations"></a>Attenzione alle ottimizzazioni delle modifiche di stato

La sezione precedente illustra come profilare entrambi i tipi di modifiche dello stato: una semplice modifica dello stato vincolata a generare la stessa quantità di lavoro per ogni iterazione e una modifica dello stato di toggling che modifica notevolmente la quantità di lavoro eseguito. Cosa accade se si accetta la sequenza di rendering precedente e si aggiunge un'altra modifica di stato? Ad esempio, questo esempio accetta la> di rendering z-enable e aggiunge un confronto z-func:


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



Lo stato z-func imposta il livello di confronto durante la scrittura nel buffer z (tra il valore z di un pixel corrente e il valore z di un pixel nel buffer di profondità). D3DCMP NON disattiva MAI il confronto dei test z mentre D3DCMP ALWAYS imposta il confronto in modo che avvenga ogni volta che viene \_ \_ eseguito il test z.

La profilatura di una di queste modifiche di stato in una sequenza di rendering [**con DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) genera risultati simili ai seguenti:



| Modifica dello stato singolo | Numero medio di cicli |
|---------------------|--------------------------|
| Solo D3DRS \_ ZENABLE | 2000                     |



 

oppure



| Modifica dello stato singolo | Numero medio di cicli |
|---------------------|--------------------------|
| Solo D3DRS \_ ZFUNC   | 600                      |



 

Tuttavia, se si profilano sia D3DRS ZENABLE che \_ D3DRS ZFUNC nella stessa sequenza di rendering, è possibile \_ visualizzare risultati simili ai seguenti:



| Entrambe le modifiche di stato            | Numero medio di cicli |
|-------------------------------|--------------------------|
| D3DRS \_ ZENABLE + D3DRS \_ ZFUNC | 2000                     |



 

È possibile prevedere che il risultato sia la somma dei cicli 2000 e 600 (o 2600) perché il driver esegue tutto il lavoro associato all'impostazione di entrambi gli stati di rendering. La media è invece di 2000 cicli.

Questo risultato riflette un'ottimizzazione della modifica dello stato implementata nel runtime, nel driver o nella GPU. In questo caso, il driver potrebbe visualizzare il primo [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e impostare uno stato dirty che posticiperebbe il lavoro fino a un secondo momento. Quando il driver visualizza il secondo **SetRenderState,** lo stesso stato dirty potrebbe essere impostato in modo ridondante e lo stesso lavoro verrebbe posticipato di nuovo. Quando [**viene chiamato DrawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) il lavoro associato allo stato dirty viene infine elaborato. Il driver esegue il lavoro una sola volta, il che significa che le prime due modifiche di stato vengono effettivamente consolidate dal driver. Analogamente, il terzo e il quarto stato vengono effettivamente consolidati dal driver in una singola modifica di stato quando viene chiamato il secondo **DrawPrimitive.** Il risultato finale è che il driver e la GPU elaborano una singola modifica dello stato per ogni chiamata di disegno.

Questo è un buon esempio di ottimizzazione del driver dipendente dalla sequenza. Il driver ha posticipato il lavoro due volte impostando uno stato dirty e quindi ha eseguito il lavoro una volta per cancellare lo stato dirty. Questo è un buon esempio del tipo di miglioramento dell'efficienza che può verificarsi quando il lavoro viene posticipato fino a quando non è assolutamente necessario.

Come è possibile sapere quali modifiche di stato impostano internamente uno stato dirty e quindi rimandare il lavoro fino a un secondo momento? Solo testando le sequenze di rendering (o parlando con i writer di driver). I driver vengono aggiornati e migliorati periodicamente in modo che l'elenco delle ottimizzazioni non sia statico. Esiste un solo modo per conoscere in modo assoluto i costi di una modifica dello stato in una determinata sequenza di rendering, in un determinato set di hardware. e cio' per misurarlo.

### <a name="watch-out-for-drawprimitive-optimizations"></a>Attenzione alle ottimizzazioni DrawPrimitive

Oltre alle ottimizzazioni delle modifiche dello stato, il runtime tenterà di ottimizzare il numero di chiamate di disegno che il driver deve elaborare. Si considerino, ad esempio, le chiamate di back-draw seguenti:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 3); // Draw 3 primitives, vertices 0 - 8
DrawPrimitive(D3DPT_TRIANGLELIST, 9, 4); // Draw 4 primitives, vertices 9 - 20
```



Esempio 5a: due chiamate di disegno

Questa sequenza contiene due chiamate di disegno, che il runtime consoliderà in una singola chiamata equivalente a:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 7); // Draw 7 primitives, vertices 0 - 20
```



Esempio 5b: una singola chiamata di disegno concatenata

Il runtime concatena entrambe queste chiamate di disegno specifiche in una singola chiamata, riducendo il lavoro del driver del 50%, perché il driver dovrà ora elaborare solo una chiamata di disegno.

In generale, il runtime concatena due o più chiamate [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) back-to-back quando:

1.  Il tipo primitivo è un elenco di triangoli (D3DPT \_ TRIANGLELIST).
2.  Ogni chiamata [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) successiva deve fare riferimento a vertici consecutivi all'interno del vertex buffer.

Analogamente, le condizioni giuste per concatenare due o più chiamate [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) back-to-back sono:

1.  Il tipo primitivo è un elenco di triangoli (D3DPT \_ TRIANGLELIST).
2.  Ogni chiamata [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) successiva deve fare riferimento sequenziale agli indici consecutivi all'interno del index buffer.
3.  Ogni chiamata [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) successiva deve usare lo stesso valore per BaseVertexIndex.

Per impedire la concatenazione durante la profilatura, modificare la sequenza di rendering in modo che il tipo primitivo non sia un elenco di triangoli o modificare la sequenza di rendering in modo che non siano presenti chiamate di disegno back-to-back che usano vertici consecutivi (o indici). In particolare, il runtime concatena anche le chiamate di disegno che soddisfano entrambe le condizioni seguenti:

-   Quando la chiamata precedente è [**DrawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)se la chiamata di disegno successiva:
    -   usa un elenco di triangoli, AND
    -   specifica StartVertex = StartVertex precedente + PrimitiveCount \* precedente 3
-   Quando si [**usa DrawIndexedPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)se la chiamata di disegno successiva:
    -   usa un elenco di triangoli, AND
    -   specifica StartIndex = StartIndex precedente + PrimitiveCount \* precedente 3, AND
    -   specifica BaseVertexIndex = baseVertexIndex precedente

Di seguito è riportato un esempio più sottile di concatenazione delle chiamate di disegno che è facile ignorare durante la profilatura. Si supponga che la sequenza di rendering sia simile alla seguente:


```
  for(int i = 0; i < 1500; i++)
  {
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Esempio 5c: una modifica dello stato e una chiamata di disegno

Il ciclo scorre 1500 triangoli, impostando una trama e disegnando ogni triangolo. Questo ciclo di rendering richiede circa 2750 cicli [**per SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e 1100 cicli per [**DrawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) come illustrato nelle sezioni precedenti. In modo intuitivo, lo spostamento di **SetTexture** all'esterno del ciclo di rendering dovrebbe ridurre la quantità di lavoro eseguita dal driver di 1500 2750 cicli, ovvero la quantità di lavoro associata alla chiamata a \* **SetTexture** 1500 volte. Il frammento di codice sarà simile al seguente:


```
  SetTexture(...); // Set the state outside the loop
  for(int i = 0; i < 1500; i++)
  {
//    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Esempio 5d: Esempio 5c con modifica dello stato all'esterno del ciclo

Lo [**spostamento di SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) all'esterno del ciclo di rendering riduce la quantità di lavoro associata a **SetTexture** perché viene chiamato una volta anziché 1500 volte. Un effetto secondario meno ovvio è che anche il lavoro per [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) è ridotto da 1500 chiamate a 1 chiamata perché vengono soddisfatte tutte le condizioni per la concatenazione delle chiamate di disegno. Quando la sequenza di rendering viene elaborata, il runtime eelaborare 1500 chiamate in una singola chiamata al driver. Spostando questa riga di codice, la quantità di lavoro del driver è stata ridotta notevolmente:


```
total work done = runtime + driver work

Example 5c: with SetTexture in the loop:
runtime work = 1500 SetTextures + 1500 DrawPrimitives 
driver  work = 1500 SetTextures + 1500 DrawPrimitives 

Example 5d: with SetTexture outside of the loop:
runtime work = 1 SetTexture + 1 DrawPrimitive + 1499 Concatenated DrawPrimitives 
driver  work = 1 SetTexture + 1 DrawPrimitive 
```



Questi risultati sono del tutto corretti, ma sono molto fuorvianti nel contesto della domanda originale. L'ottimizzazione delle chiamate di disegno ha ridotto notevolmente la quantità di lavoro del driver. Questo è un problema comune quando si esegue la profilatura personalizzata. Quando si eliminano chiamate da una sequenza di rendering, prestare attenzione a evitare la concatenazione delle chiamate di disegno. In realtà, questo scenario è un esempio efficace della quantità di miglioramento delle prestazioni del driver possibile da questa ottimizzazione di runtime.

A questo punto si sa come misurare le modifiche dello stato. Per iniziare, profilare [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). Aggiungere quindi ogni modifica di stato aggiuntiva alla sequenza (in alcuni casi aggiungendo una chiamata e in altri casi aggiungendo due chiamate) e misurare la differenza tra le due sequenze. È possibile convertire i risultati in tick, cicli o tempo. Analogamente alla misurazione delle sequenze di rendering con QueryPerformanceCounter, la misurazione delle singole modifiche dello stato si basa sul meccanismo di query per controllare il buffer dei comandi e sull'inserimento delle modifiche di stato in un ciclo per ridurre al minimo l'impatto delle transizioni di modalità. Questa tecnica misura il costo del toggling di uno stato, poiché il profiler restituisce la media di abilitazione e disabilitazione dello stato.

Con questa funzionalità, è possibile avviare la generazione di sequenze di rendering arbitrarie e misurare in modo accurato il lavoro di runtime e driver associato. I numeri possono quindi essere usati per rispondere a domande di budget come "quante altre di queste chiamate" possono essere effettuate nella sequenza di rendering mantenendo comunque una frequenza di fotogrammi ragionevole, presupponendo scenari con utilizzo limitato della CPU.

## <a name="summary"></a>Riepilogo

Questo documento illustra come controllare il buffer dei comandi in modo che le singole chiamate possano essere profilate in modo accurato. I numeri di profilatura possono essere generati in tick, cicli o tempo assoluto. Rappresentano la quantità di lavoro di runtime e driver associata a ogni chiamata API.

Iniziare profilando una chiamata draw \* primitive in una sequenza di rendering. Ricordare di:

1.  Usare QueryPerformanceCounter per misurare il numero di tick per ogni chiamata API. Usare QueryPerformanceFrequency per convertire i risultati in cicli o in tempo, se si desidera.
2.  Usare il meccanismo di query per svuotare il buffer dei comandi prima di iniziare.
3.  Includere la sequenza di rendering in un ciclo per ridurre al minimo l'impatto della transizione di modalità.
4.  Usare il meccanismo di query per misurare quando la GPU ha completato il proprio lavoro.
5.  Fare attenzione alla concatenazione di runtime che avrà un impatto significativo sulla quantità di lavoro svolto.

In questo modo è possibile ottenere prestazioni di base [**per DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) che possono essere usate per la compilazione. Per profilare una modifica dello stato, seguire questi suggerimenti aggiuntivi:

1.  Aggiungere la modifica dello stato a un profilo di sequenza di rendering noto per la nuova sequenza. Poiché il test viene eseguito in un ciclo, è necessario impostare lo stato due volte su valori opposti(ad esempio, abilitare e disabilitare).
2.  Confrontare la differenza nei tempi di ciclo tra le due sequenze.
3.  Per le modifiche di stato che modificano in modo significativo la pipeline (ad esempio [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)), sottrarre la differenza tra le due sequenze per ottenere il tempo per la modifica dello stato.
4.  Per le modifiche di stato che modificano in modo significativo la pipeline (e quindi richiedono stati di toggling come [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)), sottrarre la differenza tra le sequenze di rendering e dividere per 2. Verrà generato il numero medio di cicli per ogni modifica dello stato.

Prestare tuttavia attenzione alle ottimizzazioni che causano risultati imprevisti durante la profilatura. Le ottimizzazioni delle modifiche dello stato possono impostare gli stati dirty che causano il rinvio del lavoro. Ciò può causare risultati del profilo che non sono così intuitivi come previsto. Le chiamate di disegno concatenate ridurranno notevolmente il lavoro del driver e ciò può portare a conclusioni fuorvianti. Le sequenze di rendering pianificate con attenzione vengono usate per impedire la modifica dello stato e disegnare concatenazioni di chiamate. Il trucco è impedire che le ottimizzazioni si verifichino durante la profilatura in modo che i numeri generati siano numeri di budget ragionevoli.

> [!Note]  
> La duplicazione di questa strategia di profilatura in un'applicazione senza il meccanismo di query è più difficile. Prima di Direct3D 9 l'unico modo prevedibile per svuotare il buffer dei comandi è bloccare una superficie attiva (ad esempio una destinazione di rendering) per attendere che la GPU sia inattiva. Questo perché il blocco di una superficie forza il runtime a svuotare il buffer dei comandi nel caso in cui nel buffer siano presenti comandi di rendering che devono aggiornare la superficie prima che venga bloccata, oltre ad attendere il completamento della GPU. Questa tecnica è funzionale, anche se è più invadente che l'uso del meccanismo di query introdotto in Direct3D 9.

 

## <a name="appendix"></a>Appendice

I numeri in questa tabella sono un intervallo di approssimazioni per la quantità di lavoro di runtime e driver associata a ognuna di queste modifiche di stato. Le approssimazioni si basano sulle misurazioni effettive effettuate sui driver usando le tecniche illustrate nel documento. Questi numeri sono stati generati usando il runtime Direct3D 9 e dipendono dal driver.

Le tecniche illustrate in questo documento sono progettate per misurare il lavoro di runtime e driver. In generale, non è pratico fornire risultati che corrispondano alle prestazioni della CPU e della GPU in ogni applicazione, perché ciò richiederebbe una matrice esaustiva di sequenze di rendering. Inoltre, è particolarmente difficile eseguire il benchmark delle prestazioni della GPU perché dipende fortemente dalla configurazione dello stato nella pipeline prima della sequenza di rendering. Ad esempio, l'abilitazione della fusione alfa influisce poco sulla quantità di lavoro della CPU necessaria, ma può avere un impatto significativo sulla quantità di lavoro eseguito dalla GPU. Di conseguenza, le tecniche in questo documento vincolano il lavoro della GPU alla quantità minima possibile limitando la quantità di dati di cui è necessario eseguire il rendering. Ciò significa che i numeri nella tabella corrisponderanno maggiormente ai risultati ottenuti dalle applicazioni limitate dalla CPU (a differenza di un'applicazione limitata dalla GPU).

Si consiglia di usare le tecniche presentate per coprire gli scenari e le configurazioni più importanti. I valori nella tabella possono essere usati per confrontare con i numeri generati. Poiché ogni driver varia, l'unico modo per generare i numeri effettivi che verranno visualizzati è generare i risultati della profilatura usando gli scenari.



| Chiamata API                             | Numero medio di cicli |
|--------------------------------------|--------------------------|
| SetVertexDeclaration                 | 6500 - 11250             |
| SetFVF                               | 6400 - 11200             |
| SetVertexShader                      | 3000 - 12100             |
| SetPixelShader                       | 6300 - 7000              |
| SPECULARENABLE                       | 1900 - 11200             |
| SetRenderTarget                      | 6000 - 6250              |
| SetPixelShaderConstant (1 costante)  | 1500 - 9000              |
| NORMALIZENORMALS                     | 2200 - 8100              |
| LightEnable                          | 1300 - 9000              |
| SetStreamSource                      | 3700 - 5800              |
| Illuminazione                             | 1700 - 7500              |
| DIFFUSEMATERIALSOURCE                | 900 - 8300               |
| AMBIENTMATERIALSOURCE                | 900 - 8200               |
| COLORVERTEX                          | 800 - 7800               |
| SetLight                             | 2200 - 5100              |
| SetTransform                         | 3200 - 3750              |
| SetIndices                           | 900 - 5600               |
| Ambientale                              | 1150 - 4800              |
| SetTexture                           | 2500 - 3100              |
| SPECULARMATERIALSOURCE               | 900 - 4600               |
| EMISSIVEMATERIALSOURCE               | 900 - 4500               |
| SetMaterial                          | 1000 - 3700              |
| ZENABLE                              | 700 - 3900               |
| WRAP0                                | 1600 - 2700              |
| MINFILTER                            | 1700 - 2500              |
| MAGFILTER                            | 1700 - 2400              |
| SetVertexShaderConstant (1 costante) | 1000 - 2700              |
| COLOROP                              | 1500 - 2100              |
| COLORARG2                            | 1300 - 2000              |
| COLORARG1                            | 1300 - 1980              |
| CULLMODE                             | 500 - 2570               |
| Ritaglio                             | 500 - 2550               |
| DrawIndexedPrimitive                 | 1200 - 1400              |
| ADDRESSV                             | 1090 - 1500              |
| ADDRESSU                             | 1070 - 1500              |
| DrawPrimitive                        | 1050 - 1150              |
| SRGBTEXTURE                          | 150 - 1500               |
| STENCILMASK                          | 570 - 700                |
| STENCILZFAIL                         | 500 - 800                |
| STENCILREF                           | 550 - 700                |
| ALPHABLENDENABLE                     | 550 - 700                |
| STENCILFUNC                          | 560 - 680                |
| STENCILWRITEMASK                     | 520 - 700                |
| STENCILFAIL                          | 500 - 750                |
| ZFUNC                                | 510 - 700                |
| ZWRITEENABLE                         | 520 - 680                |
| STENCILENABLE                        | 540 - 650                |
| STENCILPASS                          | 560 - 630                |
| SRCBLEND                             | 500 - 685                |
| Two \_ Sided \_ StencilMODE              | 450 - 590                |
| ALPHATESTENABLE                      | 470 - 525                |
| ALPHAREF                             | 460 - 530                |
| ALPHAFUNC                            | 450 - 540                |
| DESTBLEND                            | 475 - 510                |
| COLORWRITEENABLE                     | 465 - 515                |
| CCW \_ STENCILFAIL                     | 340 - 560                |
| CCW \_ STENCILPASS                     | 340 - 545                |
| CCW \_ STENCILZFAIL                    | 330 - 495                |
| SCISSORTESTENABLE                    | 375 - 440                |
| CCW \_ STENCILFUNC                     | 250 - 480                |
| SetScissorRect                       | 150 - 340                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati](advanced-topics.md)
</dt> </dl>

 

 
