---
title: Miglioramenti di Direct3D 9Ex
description: In questo argomento viene descritto il supporto aggiunto di Windows 7 per la modalità Flip presente e le statistiche presenti associate in Direct3D 9Ex e Gestione finestre desktop.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42eef10b6caaa959cb750f073c97a0f665384463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399482"
---
# <a name="direct3d-9ex-improvements"></a>Miglioramenti di Direct3D 9Ex

In questo argomento viene descritto il supporto aggiunto di Windows 7 per la modalità Flip presente e le statistiche presenti associate in Direct3D 9Ex e Gestione finestre desktop. Le applicazioni di destinazione includono video o applicazioni di presentazione basate sulla frequenza dei fotogrammi. Le applicazioni che usano la modalità Flip 9Ex Direct3D presentano una riduzione del carico delle risorse di sistema quando DWM è abilitato. I miglioramenti attuali delle statistiche associati alla modalità Flip consentono alle applicazioni Direct3D 9Ex di controllare meglio la frequenza di presentazione fornendo i meccanismi di correzione e feedback in tempo reale. Sono incluse spiegazioni dettagliate e puntatori alle risorse di esempio.

In questo argomento sono contenute le sezioni seguenti.

-   [Miglioramenti di Direct3D 9Ex per Windows 7](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [Presentazione della modalità Flip 9EX Direct3D](#direct3d-9ex-flip-mode-presentation)
-   [Modello di programmazione e API](#programming-model-and-apis)
    -   [Come acconsentire esplicitamente al modello di Flip 9Ex Direct3D](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [Linee guida di progettazione per Direct3D 9Ex flip model Applications](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [Sincronizzazione dei frame delle applicazioni di modelli 9Ex Flip Direct3D](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [Sincronizzazione dei frame per le applicazioni con finestra quando DWM è disattivato](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [Procedura dettagliata di un esempio Direct3D 9Ex flip model e present Statistics](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [Riepilogo dei consigli di programmazione per la sincronizzazione dei frame](#summary-of-programming-recommendations-for-frame-synchronization)
-   [Conclusione dei miglioramenti di Direct3D 9Ex](#conclusion-about-direct3d-9ex-improvements)
-   [Chiamata all'azione](#call-to-action)
-   [Argomenti correlati](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a>Miglioramenti di Direct3D 9Ex per Windows 7

La presentazione della modalità Flip di Direct3D 9Ex è una modalità migliorata per presentare immagini in Direct3D 9Ex che consente di passare in modo efficiente le immagini sottoposte a rendering a Windows 7 Gestione finestre desktop (DWM) per la composizione. A partire da Windows Vista, DWM compone l'intero desktop. Quando DWM è abilitato, le applicazioni in modalità finestra presentano il proprio contenuto sul desktop usando un metodo denominato modalità BLT presente in DWM (o modello BLT). Con il modello BLT, DWM mantiene una copia della superficie di rendering di Direct3D 9Ex per la composizione del desktop. Quando l'applicazione viene aggiornata, il nuovo contenuto viene copiato nell'area di DWM tramite un BLT. Per le applicazioni che contengono contenuto Direct3D e GDI, i dati GDI vengono anche copiati nella superficie di DWM.

Disponibile in Windows 7, la modalità Flip presente in DWM (o Capovolgi modello) è un nuovo metodo di presentazione che consente essenzialmente di passare handle di superfici dell'applicazione tra applicazioni in modalità finestra e DWM. Oltre al salvataggio delle risorse, il modello Flip supporta statistiche attuali avanzate.

Le statistiche attuali sono informazioni sugli intervalli di frame che possono essere usate dalle applicazioni per sincronizzare flussi video e audio e per eseguire il ripristino da problemi di riproduzione video. Le informazioni relative alla temporizzazione dei frame nelle statistiche attuali consentono alle applicazioni di regolare la frequenza di presentazione dei fotogrammi video per una presentazione più uniforme. In Windows Vista, in cui DWM gestisce una copia corrispondente della superficie del frame per la composizione del desktop, le applicazioni possono utilizzare le statistiche presenti disponibili in DWM. Questo metodo per ottenere le statistiche attuali sarà ancora disponibile in Windows 7 per le applicazioni esistenti.

In Windows 7, le applicazioni basate su Direct3D 9Ex che adottano il modello Flip devono usare le API D3D9Ex per ottenere le statistiche attuali. Quando DWM è abilitato, la modalità a finestra e le applicazioni Direct3D 9Ex in modalità esclusiva a schermo intero possono prevedere le stesse informazioni sulle statistiche presenti quando si usa Capovolgi modello. Direct3D 9Ex flip model present Statistics consente alle applicazioni di eseguire query per le statistiche presenti in tempo reale, anziché dopo che il frame è stato visualizzato sullo schermo; le stesse informazioni sulle statistiche sono disponibili per le applicazioni abilitate per la Flip-Model in modalità finestra come applicazioni a schermo intero. un flag aggiunto nelle API D3D9Ex consente alle applicazioni flip model di eliminare in modo efficace i frame tardivi in fase di presentazione.

Il modello Direct3D 9Ex Flip deve essere usato dalle nuove applicazioni di presentazione basate su video o frequenza dei fotogrammi destinate a Windows 7. A causa della sincronizzazione tra DWM e il runtime 9Ex Direct3D, le applicazioni che utilizzano il modello Flip devono specificare tra 2 e 4 buffer per garantire una presentazione uniforme. Le applicazioni che usano le informazioni statistiche attuali trarranno vantaggio dall'uso dei miglioramenti delle statistiche presenti in flip model Enabled.

## <a name="direct3d-9ex-flip-mode-presentation"></a>Presentazione della modalità Flip 9EX Direct3D

I miglioramenti delle prestazioni della modalità Flip 9Ex di Direct3D sono significativi nel sistema quando DWM è acceso e quando l'applicazione è in modalità finestra, anziché in modalità esclusiva a schermo intero. Nella tabella e nell'illustrazione seguenti viene illustrato un confronto semplificato degli utilizzi della larghezza di banda della memoria e delle letture e scritture di sistema delle applicazioni con finestra che scelgono Capovolgi modello rispetto al modello BLT utilizzo predefinito.



| Modalità BLT presente in DWM                                                                                                 | Modalità D3D9Ex Flip presente in DWM                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1. l'applicazione aggiorna il frame (scrittura)<br/>                                                                 | 1. l'applicazione aggiorna il frame (scrittura)<br/>                     |
| 2. il runtime Direct3D copia il contenuto della superficie in una superficie di reindirizzamento DWM (lettura, scrittura)<br/>                       | 2. il runtime Direct3D passa l'area dell'applicazione a DWM<br/>        |
| 3. una volta completata la copia della superficie condivisa, DWM esegue il rendering dell'area dell'applicazione sullo schermo (lettura, scrittura)<br/> | 3. DWM esegue il rendering dell'area dell'applicazione sullo schermo (lettura, scrittura)<br/> |



 

![illustrazione di un confronto tra il modello BLT e il modello Flip](images/blt-flip-mode-present.png)

La modalità Flip consente di ridurre l'utilizzo della memoria di sistema riducendo il numero di letture e scritture da parte del runtime Direct3D per la composizione del frame finestra di DWM. In questo modo si riduce il consumo di energia del sistema e l'utilizzo complessivo della memoria.

Le applicazioni possono sfruttare i vantaggi di Direct3D 9Ex Flip mode presenta i miglioramenti delle statistiche quando DWM è acceso, indipendentemente dal fatto che l'applicazione sia in modalità finestra o in modalità esclusiva a schermo intero.

## <a name="programming-model-and-apis"></a>Modello di programmazione e API

Le nuove applicazioni per la misurazione della frequenza dei fotogrammi e dei video che usano le API Direct3D 9Ex in Windows 7 possono sfruttare i vantaggi della memoria e del risparmio energetico e della presentazione migliorata offerta dalla modalità Flip presente durante l'esecuzione in Windows 7. Quando è in esecuzione in versioni precedenti di Windows, il runtime di Direct3D usa per impostazione predefinita l'applicazione in modalità BLT.

La modalità Flip prevede che l'applicazione possa sfruttare i vantaggi dei meccanismi di correzione e feedback delle statistiche presenti in tempo reale quando DWM è acceso. Tuttavia, le applicazioni che usano la modalità Flip presentano le limitazioni quando usano il rendering dell'API GDI simultaneo.

È possibile modificare le applicazioni esistenti per sfruttare i vantaggi della modalità Flip presente, con gli stessi vantaggi e avvertenze delle applicazioni appena sviluppate.

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a>Come acconsentire esplicitamente al modello di Flip 9Ex Direct3D

Le applicazioni Direct3D 9Ex destinate a Windows 7 possono optare per il modello Flip creando la catena di scambio con il valore di enumerazione [**\_ FLIPEX D3DSWAPEFFECT**](/windows/desktop/direct3d9/d3dswapeffect) . Per acconsentire esplicitamente al modello Flip, le applicazioni specificano la struttura dei [**\_ parametri D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) , quindi passano un puntatore a questa struttura quando chiamano l'API [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) . In questa sezione viene descritto in che modo le applicazioni destinate a Windows 7 utilizzano **IDirect3D9Ex:: CreateDeviceEx** per acconsentire esplicitamente al modello flip. Per ulteriori informazioni sull'API **IDirect3D9Ex:: CreateDeviceEx** , vedere **IDirect3D9Ex:: CreateDeviceEx su MSDN**.

Per praticità, la sintassi [**dei \_ parametri D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) e [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) viene ripetuta qui.

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

Quando si modificano le applicazioni Direct3D 9Ex per Windows 7 per acconsentire al modello Flip, è necessario considerare gli elementi seguenti sui membri specificati [**dei \_ parametri D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters):

<dl> <dt>

**BackBufferCount**
</dt> <dd>

(Solo Windows 7)

Quando **SwapEffect** è impostato sul nuovo tipo di \_ effetto catena di scambio D3DSWAPEFFECT FLIPEX, il numero di buffer nascosto deve essere uguale o maggiore di 2, per evitare una riduzione delle prestazioni dell'applicazione come conseguenza dell'attesa del rilascio di DWM da parte del buffer presente precedente.

Quando l'applicazione usa anche le statistiche presenti associate a D3DSWAPEFFECT \_ FLIPEX, è consigliabile impostare il numero di buffer indietro su da 2 a 4.

L'utilizzo \_ di D3DSWAPEFFECT FLIPEX in Windows Vista o nelle versioni precedenti del sistema operativo restituirà FAIL da [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).

</dd> <dt>

**SwapEffect**
</dt> <dd>

(Solo Windows 7)

Il nuovo \_ tipo di effetto catena di scambio FLIPEX di D3DSWAPEFFECT designa quando un'applicazione sta adottando la modalità di capovolgimento presente in DWM. Consente all'applicazione un utilizzo più efficiente della memoria e della potenza e consente inoltre all'applicazione di sfruttare le statistiche presenti a schermo intero in modalità finestra. Il comportamento dell'applicazione a schermo intero non è interessato. Se Windowed è impostato su **true** e **SwapEffect** è impostato su D3DSWAPEFFECT \_ FLIPEX, il runtime crea un ulteriore buffer aggiuntivo e ruota a seconda di quale handle appartiene al buffer che diventa il buffer anteriore al momento della presentazione.

</dd> <dt>

**Flag**
</dt> <dd>

(Solo Windows 7)

Non è possibile impostare il flag [ \_ \_ backBuffer bloccabile D3DPRESENTFLAG](/windows/desktop/direct3d9/d3dpresentflag) se **SwapEffect** è impostato sul nuovo tipo di effetto catena di scambio [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) .

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a>Linee guida di progettazione per Direct3D 9Ex flip model Applications

Usare le linee guida riportate nelle sezioni riportate di seguito per progettare le applicazioni Direct3D 9Ex flip model.

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a>Utilizzare la modalità Flip presente in un HWND separato dalla modalità BLT presente

Le applicazioni devono utilizzare la modalità Flip 9Ex di Direct3D presente in un HWND che non è anche di destinazione di altre API, inclusa la modalità BLT che presenta 9Ex Direct3D, altre versioni di Direct3D o GDI. La modalità Flip presente può essere usata per presentare le finestre figlio; in altre condizioni, le applicazioni possono utilizzare Capovolgi modello quando non è misto al modello BLT nello stesso HWND, come illustrato nelle illustrazioni seguenti.

![illustrazione della finestra padre Direct3D e di una finestra figlio GDI, ciascuna con il proprio HWND](images/parent-d3d.png)

![illustrazione della finestra padre GDI e di una finestra figlio Direct3D, ciascuna con il proprio HWND](images/parent-gdi.png)

Poiché il modello BLT mantiene una copia aggiuntiva della superficie, è possibile aggiungere GDI e altri contenuti Direct3D allo stesso HWND tramite aggiornamenti a fasi da Direct3D e GDI. Utilizzando il modello Flip, solo il contenuto Direct3D 9Ex nelle catene di scambio [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) passate a DWM sarà visibile. Tutti gli altri aggiornamenti del contenuto Direct3D o GDI del modello BLT verranno ignorati, come illustrato nelle illustrazioni seguenti.

![illustrazione del testo GDI che potrebbe non essere visualizzato se si utilizza il modello Flip e il contenuto Direct3D e GDI si trovano nello stesso HWND](images/d3d-gdi-same-hwnd.png)

![illustrazione del contenuto Direct3D e GDI in cui DWM è abilitato e l'applicazione è in modalità finestra](images/d3d-gdinotext-same-hwnd.png)

Per questo motivo, è necessario abilitare il modello Flip per i buffer della catena di scambio, in cui il modello di 9Ex Flip solo per il rendering dell'intero HWND.

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a>Non usare Capovolgi modello con ScrollWindow o ScrollWindowEx di GDI

Alcune applicazioni Direct3D 9Ex utilizzano le funzioni ScrollWindow o ScrollWindowEx di GDI per aggiornare il contenuto della finestra quando viene attivato un evento Scroll utente. ScrollWindow e ScrollWindowEx eseguono BLTs del contenuto della finestra sullo schermo durante lo scorrimento di una finestra. Queste funzioni richiedono anche aggiornamenti del modello BLT per il contenuto GDI e 9Ex di Direct3D. Nelle applicazioni in cui viene utilizzata una delle due funzioni non verrà necessariamente visualizzato lo scorrimento del contenuto della finestra visibile sullo schermo quando l'applicazione è in modalità finestra e DWM è abilitato. Si consiglia di non utilizzare le API ScrollWindow e ScrollWindowEx di GDI nelle applicazioni e di ricreare il contenuto sullo schermo in risposta allo scorrimento.

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a>Usare una \_ catena di scambio FLIPEX di D3DSWAPEFFECT per HWND

Le applicazioni che usano Capovolgi modello non devono usare più catene di scambio del modello Flip destinate allo stesso HWND.

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a>Sincronizzazione dei frame delle applicazioni di modelli 9Ex Flip Direct3D

Le statistiche attuali sono informazioni sulla tempistica dei frame utilizzate dalle applicazioni multimediali per sincronizzare flussi video e audio e per eseguire il ripristino da problemi di riproduzione video. Per abilitare la disponibilità delle statistiche, l'applicazione Direct3D 9Ex deve garantire che il parametro *BehaviorFlags* passato dall'applicazione a [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contenga il flag di comportamento del dispositivo [D3DCREATE \_ enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).

Per praticità, la sintassi di [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) è ripetuta qui.

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

Il modello Direct3D 9Ex flip aggiunge il flag di presentazione di [D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) che impone il comportamento del flag di presentazione [ \_ \_ immediato dell'intervallo D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) . L'applicazione Direct3D 9Ex specifica questi flag di presentazione nel parametro *dwFlags* che l'applicazione passa a [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), come illustrato di seguito.

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

Quando si modifica l'applicazione Direct3D 9Ex per Windows 7, è necessario considerare le seguenti informazioni sui flag di presentazione di [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) specificati:

<dl> <dt>

[\_DONOTFLIP D3DPRESENT](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

Questo flag è disponibile solo in modalità schermo intero o

(Solo Windows 7)

Quando l'applicazione imposta il membro **SwapEffect** dei [**\_ parametri D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) su [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in una chiamata a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).

</dd> <dt>

[\_FORCEIMMEDIATE D3DPRESENT](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

(Solo Windows 7)

Questo flag può essere specificato solo se l'applicazione imposta il membro **SwapEffect** dei [**\_ parametri D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) su [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in una chiamata a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex). L'applicazione può utilizzare questo flag per aggiornare immediatamente una superficie con diversi frame in un secondo momento nella coda del presente DWM, ignorando essenzialmente i frame intermedi.

Le applicazioni abilitate per FlipEx con finestra possono usare questo flag per aggiornare immediatamente una superficie con un frame che si trova in un secondo momento nella coda del presente DWM, ignorando i frame intermedi. Questa operazione è particolarmente utile per le applicazioni multimediali che desiderano rimuovere i frame rilevati in ritardo e presentare i frame successivi al momento della composizione. [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) restituisce un errore di parametro non valido se il flag non è specificato correttamente.

</dd> </dl>

Per ottenere le informazioni sulle statistiche presenti, l'applicazione ottiene la struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) chiamando l'API [**IDirect3DSwapChain9Ex:: GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) .

La struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) contiene statistiche sulle chiamate [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) . Il dispositivo deve essere creato tramite una chiamata [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) con il flag [di \_ Abilitazione di \_ PRESENTSTATS D3DCREATE](/windows/desktop/direct3d9/d3dcreate) . In caso contrario, i dati restituiti da [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) non sono definiti. Una catena di swap 9Ex Direct3D abilitata per il modello fornisce informazioni sulle statistiche presenti nelle modalità finestra e a schermo intero.

Per le catene di scambio Direct3D 9Ex abilitate per il modello BLT in modalità finestra, tutti i valori della struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) saranno zeri.

Per FlipEx present Statistics, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) restituisce \_ D3DERR \_ le statistiche presenti \_ nelle situazioni seguenti:

-   Prima chiamata a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ever, che indica l'inizio di una sequenza
-   Transizione di DWM da on a off
-   Modifica della modalità: in modalità finestra a o da schermo intero o a schermo intero a transizioni a schermo intero

Per praticità, la sintassi di [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) viene ripetuta qui.

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

Il metodo [**IDirect3DSwapChain9Ex:: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) restituisce l'ultimo PresentCount, ovvero l'ID attuale dell'ultima chiamata a present riuscita effettuata da un dispositivo di visualizzazione associato alla catena di scambio. Questo ID presenta il valore del membro **PresentCount** della struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) . Per le catene di scambio Direct3D 9Ex abilitate per il modello, in modalità finestra, tutti i valori della struttura **D3DPRESENTSTATS** saranno zeri.

Per praticità, la sintassi di [**IDirect3DSwapChain9Ex:: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) è ripetuta qui.

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

Quando si modifica l'applicazione Direct3D 9Ex per Windows 7, è necessario considerare le informazioni seguenti sulla struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) :

-   Il valore di PresentCount restituito da [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) non viene aggiornato quando una chiamata [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT \_ DONOTWAIT specificato nel parametro *dwFlags* restituisce un errore.
-   Quando [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) viene chiamato con D3DPRESENT \_ DONOTFLIP, una chiamata [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ha esito positivo ma non restituisce una struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) aggiornata quando l'applicazione è in modalità finestra.
-   **PresentRefreshCount** rispetto a **SyncRefreshCount** in [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):
    -   **PresentRefreshCount** è uguale a **SyncRefreshCount** quando l'applicazione presenta ogni vsync.
    -   **SyncRefreshCount** viene ottenuto nell'intervallo vsync quando è stato inviato il presente, **SyncQPCTime** è approssimativamente il tempo associato all'intervallo vsync.

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a>Sincronizzazione dei frame per le applicazioni con finestra quando DWM è disattivato

Quando DWM è disattivato, le applicazioni finestra vengono visualizzate direttamente nella schermata di monitoraggio senza passare attraverso una catena di scorrimento. In Windows Vista non è disponibile alcun supporto per ottenere informazioni sulle statistiche dei frame per le applicazioni con finestra quando DWM è disattivato. Per mantenere un'API in cui le applicazioni non devono essere compatibili con DWM, Windows 7 restituirà le informazioni sulle statistiche dei frame per le applicazioni con finestra quando DWM è disattivato. Le statistiche dei frame restituite quando DWM è disattivato sono solo stime.

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a>Walk-Through di un esempio Direct3D 9Ex flip model e present Statistics

**Per acconsentire esplicitamente all'esempio FlipEx Presentation for Direct3D 9Ex**

1.  Verificare che l'applicazione di esempio sia in esecuzione in Windows 7 o versione successiva del sistema operativo.
2.  Impostare il membro **SwapEffect** dei [**\_ parametri D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) su [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in una chiamata a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



**Per acconsentire esplicitamente all'esempio FlipEx Associated present Statistics for Direct3D 9Ex**

-   Impostare [D3DCREATE \_ enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) nel parametro *BehaviorFlags* di [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



**Per evitare, rilevare e ripristinare le anomalie**

1.  Chiamate di coda presenti: il numero consigliato di backBuffer è compreso tra 2 e 4.
2.  L'esempio Direct3D 9Ex aggiunge un backBuffer implicito. la lunghezza effettiva della coda attuale è il conteggio delle sottobuffer + 1.
3.  Creare una struttura di coda presente nell'helper per archiviare tutti gli ID presenti (PresentCount) e i PresentRefreshCount associati, calcolati/previsti.
4.  Per rilevare l'occorrenza glitch:

    -   Chiamare [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).
    -   Ottenere l'ID attuale (PresentCount) e il numero di VSync in cui viene visualizzato il frame (PresentRefreshCount) del fotogramma con le statistiche attuali ottenute.
    -   Recuperare il PresentRefreshCount previsto (TargetRefresh nel codice di esempio) associato all'ID presente.
    -   Se il valore di PresentRefreshCount effettivo è successivo al previsto, si è verificato un problema.

5.  Per risolvere il problema:

    -   Calcolare il numero di frame da ignorare ( \_ variabile g iImmediates nel codice di esempio).
    -   Presentare i frame ignorati con intervallo D3DPRESENT \_ FORCEIMMEDIATE.

**Considerazioni per il rilevamento e il ripristino di problemi**

1.  Il recupero glitch accetta N ( \_ variabile iQueueDelay nel codice di esempio) numero di chiamate presenti in cui N (g \_ iQueueDelay) è uguale \_ a g iImmediates più la lunghezza della coda corrente, ovvero:

    -   I frame ignorati con l'intervallo presente D3DPRESENT \_ FORCEIMMEDIATE, più
    -   Present in coda che devono essere elaborati

2.  Impostare un limite per la lunghezza del glitch ( \_ limite di recupero glitch \_ nell'esempio). Se l'applicazione di esempio non è in grado di eseguire il ripristino da un problema troppo lungo (ad esempio, 1 secondo o 60 vsyncs su 60Hz monitor), passare all'animazione intermittente e reimpostare la coda Helper presente.


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



**Scenario di esempio**

-   Nell'illustrazione seguente viene mostrata un'applicazione con conteggio del buffer di 4. La lunghezza effettiva della coda attuale è pertanto 5.

    ![illustrazione di un frame sottoposto a rendering applicas e della coda presente](images/sample-scenario.png)

    Il frame A è destinato a andare sullo schermo sul numero di intervalli di sincronizzazione 1 ma è stato rilevato che è stato visualizzato sul numero di intervalli di sincronizzazione pari a 4. Si è quindi verificato un problema. I 3 frame successivi vengono presentati con l'intervallo di D3DPRESENT \_ \_ FORCEIMMEDIATE. Il glitch dovrebbe richiedere un totale di 8 chiamate presenti prima del ripristino. il frame successivo verrà visualizzato in base al numero di intervalli di sincronizzazione di destinazione.

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a>Riepilogo dei consigli di programmazione per la sincronizzazione dei frame

-   Creare un elenco di backup di tutti gli ID LastPresentCount (ottenuti tramite [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) e i PresentRefreshCount stimati associati di tutti i presentamenti inviati.
    > [!Note]  
    > Quando l'applicazione chiama [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT \_ DONOTFLIP, la chiamata [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ha esito positivo ma non restituisce una struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) aggiornata quando l'applicazione è in modalità finestra.

     

-   Chiamare [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) per ottenere il PresentRefreshCount effettivo associato a ogni ID presente dei frame visualizzati, per assicurarsi che l'applicazione gestisca gli errori restituiti dalla chiamata.
-   Se il valore di PresentRefreshCount effettivo è successivo al valore di PresentRefreshCount stimato, viene rilevato un problema. Compensare inviando frame in ritardo ' presenti con D3DPRESENT \_ FORCEIMMEDIATE.
-   Quando un frame viene presentato in ritardo nella coda corrente, tutti i frame successivi in coda saranno presentati in ritardo. D3DPRESENT \_ FORCEIMMEDIATE correggerà solo il frame successivo che verrà visualizzato dopo tutti i frame in coda. Pertanto, il conteggio della coda o del buffer non deve essere troppo lungo, quindi è possibile che si verifichino problemi di frame minori. Il numero di backBuffer ottimale è da 2 a 4.
-   Se il valore di PresentRefreshCount stimato è successivo al valore effettivo di PresentRefreshCount, potrebbe essersi verificata la limitazione di DWM. Sono possibili le soluzioni seguenti:

    -   riduzione della lunghezza della coda presente
    -   riduzione dei requisiti di memoria della GPU con qualsiasi altro mezzo, oltre a ridurre la lunghezza della coda presente (ovvero, diminuire la qualità, rimuovere gli effetti e così via)
    -   specifica di [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) per impedire la limitazione di DWM in generale

-   Verificare le prestazioni delle funzionalità di visualizzazione delle applicazioni e delle statistiche dei frame negli scenari seguenti:

    -   con DWM acceso e disattivato
    -   modalità esclusive e con finestra a schermo intero
    -   hardware con funzionalità più bassa

-   Quando le applicazioni non possono eseguire il ripristino da un numero elevato di frame glitch con D3DPRESENT \_ FORCEIMMEDIATE presenti, possono eseguire potenzialmente le operazioni seguenti:

    -   ridurre l'utilizzo della CPU e della GPU eseguendo il rendering con minor carico di lavoro.
    -   nel caso di decodifica video, decodifica più velocemente riducendo la qualità e, pertanto, l'utilizzo della CPU e della GPU.

## <a name="conclusion-about-direct3d-9ex-improvements"></a>Conclusione dei miglioramenti di Direct3D 9Ex

In Windows 7, le applicazioni che visualizzano la frequenza dei fotogrammi video o misuratore durante la presentazione possono scegliere di capovolgere il modello. I miglioramenti attuali delle statistiche associati a flip model Direct3D 9Ex possono trarre vantaggio dalle applicazioni che sincronizzano la presentazione per frequenza dei fotogrammi, con feedback in tempo reale per il rilevamento e il recupero di problemi. Gli sviluppatori che adottano il modello Direct3D 9Ex Flip devono considerare come destinazione un HWND separato dal contenuto GDI e dalla sincronizzazione della frequenza dei fotogrammi. Vedere i dettagli in questo argomento e la documentazione MSDN. Per ulteriori informazioni, vedere la pagina relativa [al centro per sviluppatori DirectX su MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).

## <a name="call-to-action"></a>Invito all'azione ##

Quando si creano applicazioni che tentano di sincronizzare la frequenza dei fotogrammi di presentazione o il ripristino da anomalie di visualizzazione, si consiglia di usare Direct3D 9Ex flip model e le statistiche presenti in Windows 7.

## <a name="related-topics"></a>Argomenti correlati

[Centro per sviluppatori DirectX su MSDN](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> </dl>