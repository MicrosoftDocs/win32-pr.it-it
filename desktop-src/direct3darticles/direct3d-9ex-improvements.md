---
title: Miglioramenti di Direct3D 9Ex
description: Questo argomento descrive Windows supporto aggiunto di 7 per la modalità flip present e le statistiche presenti associate in Direct3D 9Ex e Gestione finestre desktop.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3221b805f07408b27e19a00a42ca0c4733ea725bd32a51b5b3e340b48d2070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796993"
---
# <a name="direct3d-9ex-improvements"></a>Miglioramenti di Direct3D 9Ex

Questo argomento descrive Windows supporto aggiunto di 7 per la modalità flip present e le statistiche presenti associate in Direct3D 9Ex e Gestione finestre desktop. Le applicazioni di destinazione includono applicazioni di presentazione basate su frequenza di fotogrammi o video. Le applicazioni che usano Direct3D 9Ex Flip Mode Present riducono il carico delle risorse di sistema quando È abilitato DWM. Present statistics enhancements associated with Flip Mode Present consente alle applicazioni Direct3D 9Ex di controllare meglio la frequenza di presentazione fornendo feedback e meccanismi di correzione in tempo reale. Sono incluse spiegazioni dettagliate e puntatori alle risorse di esempio.

In questo argomento sono contenute le sezioni seguenti.

-   [Miglioramenti di Direct3D 9Ex per Windows 7](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [Presentazione della modalità flip Direct3D 9EX](#direct3d-9ex-flip-mode-presentation)
-   [Modello di programmazione e API](#programming-model-and-apis)
    -   [Come acconsentire esplicitamente al modello Flip Direct3D 9Ex](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [Linee guida di progettazione per applicazioni Direct3D 9Ex Flip Model](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [Sincronizzazione dei frame delle applicazioni Direct3D 9Ex Flip Model](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [Sincronizzazione dei frame per le applicazioni con finestra quando DWM è disattivato](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [Presentazione di un modello flip Direct3D 9Ex e di un esempio di statistiche di presentazione](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [Riepilogo delle funzionalità di Consigli per la sincronizzazione dei frame](#summary-of-programming-recommendations-for-frame-synchronization)
-   [Conclusioni sui miglioramenti di Direct3D 9Ex](#conclusion-about-direct3d-9ex-improvements)
-   [Invito all'azione](#call-to-action)
-   [Argomenti correlati](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a>Miglioramenti di Direct3D 9Ex per Windows 7

Presentazione in modalità flip di Direct3D 9Ex è una modalità migliorata di presentazione delle immagini in Direct3D 9Ex che consente di eseguire in modo efficiente il rendering delle immagini Windows Windows 7 Gestione finestre desktop (DWM) per la composizione. A partire Windows Vista, DWM compone l'intero desktop. Quando DWM è abilitato, le applicazioni in modalità finestra presentano il proprio contenuto sul desktop usando un metodo denominato Modalità Blt presente in DWM (o modello Blt). Con il modello Blt, DWM mantiene una copia della superficie di rendering Direct3D 9Ex per la composizione desktop. Quando l'applicazione viene aggiornata, il nuovo contenuto viene copiato nella superficie DWM tramite blt. Per le applicazioni che contengono contenuto Direct3D e GDI, i dati GDI vengono copiati anche sulla superficie DWM.

Disponibile in Windows 7, la modalità flip presente in DWM (o Flip Model) è un nuovo metodo di presentazione che consente essenzialmente il passaggio di handle delle superfici dell'applicazione tra applicazioni in modalità finestra e DWM. Oltre a salvare le risorse, Flip Model supporta statistiche attuali migliorate.

Le statistiche presenti sono informazioni di temporizzazione dei fotogrammi che le applicazioni possono usare per sincronizzare i flussi video e audio e recuperare da problemi di riproduzione video. Le informazioni sulla temporizzazione dei fotogrammi nelle statistiche attuali consentono alle applicazioni di regolare la frequenza di presentazione dei fotogrammi video per una presentazione più uniforme. In Windows Vista, in cui DWM gestisce una copia corrispondente della superficie cornice per la composizione desktop, le applicazioni possono usare le statistiche presenti fornite da DWM. Questo metodo per ottenere le statistiche attuali sarà ancora disponibile in Windows 7 per le applicazioni esistenti.

In Windows 7, le applicazioni basate su Direct3D 9Ex che adottano Flip Model devono usare le API D3D9Ex per ottenere le statistiche presenti. Quando DWM è abilitato, le applicazioni Direct3D 9Ex in modalità esclusiva a schermo intero e in modalità finestra possono prevedere le stesse informazioni statistiche presenti quando si usa Flip Model. Direct3D 9Ex Flip Model presenta statistiche che consentono alle applicazioni di eseguire query per le statistiche presenti in tempo reale, anziché dopo che il frame è stato visualizzato sullo schermo; le stesse informazioni statistiche presenti sono disponibili per le applicazioni abilitate in modalità Flip-Model come applicazioni a schermo intero; Un flag aggiunto nelle API D3D9Ex consente alle applicazioni Flip Model di eliminare in modo efficace i fotogrammi in ritardo in fase di presentazione.

Direct3D 9Ex Flip Model deve essere usato dalle nuove applicazioni di presentazione basate su frequenza fotogrammi o video che hanno come destinazione Windows 7. A causa della sincronizzazione tra DWM e il runtime Direct3D 9Ex, le applicazioni che usano Flip Model devono specificare da 2 a 4 backbuffer per garantire una presentazione uniforme. Le applicazioni che usano le informazioni sulle statistiche presenti trarranno vantaggio dall'uso dei miglioramenti apportati alle statistiche di Flip Model abilitati.

## <a name="direct3d-9ex-flip-mode-presentation"></a>Presentazione della modalità flip Direct3D 9EX

I miglioramenti delle prestazioni di Direct3D 9Ex Flip Mode Present sono significativi nel sistema quando DWM è attiva e quando l'applicazione è in modalità a finestre, anziché in modalità esclusiva a schermo intero. La tabella e l'illustrazione seguenti illustrano un confronto semplificato degli utilizzi della larghezza di banda della memoria e delle operazioni di lettura e scrittura di sistema delle applicazioni con finestra che scelgono Flip Model (Capovolgi modello) rispetto al modello Blt di utilizzo predefinito.



| Modalità Blt presente in DWM                                                                                                 | Modalità flip D3D9Ex presente in DWM                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1. L'applicazione aggiorna il frame (scrittura)<br/>                                                                 | 1. L'applicazione aggiorna il frame (scrittura)<br/>                     |
| 2. Il runtime Direct3D copia il contenuto della superficie in una superficie di reindirizzamento DWM (Lettura, Scrittura)<br/>                       | 2. Il runtime Direct3D passa la superficie dell'applicazione a DWM<br/>        |
| 3. Al termine della copia della superficie condivisa, DWM esegue il rendering della superficie dell'applicazione sullo schermo (lettura, scrittura)<br/> | 3. DWM esegue il rendering della superficie dell'applicazione sullo schermo (lettura, scrittura)<br/> |



 

![illustrazione di un confronto tra il modello blt e il modello flip](images/blt-flip-mode-present.png)

La modalità Flip Present riduce l'utilizzo della memoria di sistema riducendo il numero di operazioni di lettura e scrittura da parte del runtime Direct3D per la composizione di frame con finestra da parte di DWM. In questo modo si riduce il consumo di energia del sistema e l'utilizzo complessivo della memoria.

Le applicazioni possono sfruttare i vantaggi della modalità flip Direct3D 9Ex presentano miglioramenti delle statistiche quando DWM è attiva, indipendentemente dal fatto che l'applicazione sia in modalità finestra o in modalità esclusiva a schermo intero.

## <a name="programming-model-and-apis"></a>Modello di programmazione e API

Le nuove applicazioni video o frame rate-gauging che usano API Direct3D 9Ex in Windows 7 possono sfruttare i vantaggi della memoria e del risparmio di energia e della presentazione migliorata offerta dalla modalità flip presente quando è in esecuzione Windows 7. Quando è in esecuzione nelle versioni Windows precedenti, il runtime Direct3D predefinito dell'applicazione è Blt Mode Present.)

La modalità Flip Present comporta che l'applicazione possa sfruttare i meccanismi di feedback e correzione delle statistiche presenti in tempo reale quando DWM è attivata. Tuttavia, le applicazioni che usano la modalità Flip Present devono essere consapevoli delle limitazioni quando usano il rendering simultaneo dell'API GDI.

È possibile modificare le applicazioni esistenti per sfruttare la modalità Flip Present, con gli stessi vantaggi e avvertenze delle applicazioni appena sviluppate.

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a>Come acconsentire esplicitamente al modello Flip Direct3D 9Ex

Le applicazioni Direct3D 9Ex che hanno come destinazione Windows 7 possono acconsentire esplicitamente al modello flip creando la catena di scambio con il valore di enumerazione [**D3DSWAPEFFECT \_ FLIPEX.**](/windows/desktop/direct3d9/d3dswapeffect) Per acconsentire esplicitamente al modello Flip, le applicazioni specificano la struttura [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) e quindi passano un puntatore a questa struttura quando chiamano l'API [**IDirect3D9Ex::CreateDeviceEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) Questa sezione descrive in che modo le applicazioni Windows 7 usano **IDirect3D9Ex::CreateDeviceEx** per acconsentire esplicitamente al modello Flip. Per altre informazioni sull'API **IDirect3D9Ex::CreateDeviceEx,** vedere **IDirect3D9Ex::CreateDeviceEx su MSDN.**

Per praticità, la sintassi [**di D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) e [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) viene ripetuta qui.

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

Quando si modificano le applicazioni Direct3D 9Ex per Windows 7 per acconsentire esplicitamente al modello flip, è necessario considerare gli elementi seguenti relativi ai membri specificati di [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters):

<dl> <dt>

**BackBufferCount**
</dt> <dd>

(solo Windows 7)

Quando **SwapEffect** è impostato sul nuovo tipo di effetto della catena di scambio FLIPEX D3DSWAPEFFECT, il conteggio del buffer nascosto deve essere uguale o maggiore di 2, per evitare una perdita di prestazioni dell'applicazione in seguito all'attesa del buffer Present precedente rilasciato da \_ DWM.

Quando l'applicazione usa anche le statistiche presenti associate a D3DSWAPEFFECT FLIPEX, è consigliabile impostare il numero di buffer nascosto \_ su 2 a 4.

L'uso di D3DSWAPEFFECT FLIPEX Windows Vista o versioni precedenti del sistema operativo restituirà un errore \_ [**da CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).

</dd> <dt>

**SwapEffect**
</dt> <dd>

(solo Windows 7)

Il nuovo tipo di effetto della catena di scambio FLIPEX D3DSWAPEFFECT definisce quando un'applicazione adotta la modalità flip \_ presente in DWM. Consente all'applicazione un utilizzo più efficiente della memoria e della potenza e consente anche all'applicazione di sfruttare le statistiche presenti a schermo intero in modalità finestra. Il comportamento dell'applicazione a schermo intero non è interessato. Se Windowed è impostato su **TRUE** e **SwapEffect** è impostato su D3DSWAPEFFECT FLIPEX, il runtime crea un buffer nascosto aggiuntivo e ruota qualsiasi handle appartenga al buffer che diventa il front buffer in fase di \_ presentazione.

</dd> <dt>

**Flag**
</dt> <dd>

(solo Windows 7)

Non è possibile impostare il flag [ \_ \_ BACKBUFFER D3DPRESENTFLAG LOCKABLE](/windows/desktop/direct3d9/d3dpresentflag) se **SwapEffect** è impostato sul nuovo tipo di effetto della catena di scambio [**\_ FLIPEX D3DSWAPEFFECT.**](/windows/desktop/direct3d9/d3dswapeffect)

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a>Linee guida di progettazione per applicazioni Direct3D 9Ex Flip Model

Usare le linee guida nelle sezioni seguenti per progettare le applicazioni Direct3D 9Ex Flip Model.

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a>Usare la modalità flip presente in un HWND separato dalla modalità Blt presente

Le applicazioni devono usare Direct3D 9Ex Flip Mode Presente in un HWND che non è destinato anche ad altre API, tra cui Blt Mode Present Direct3D 9Ex, altre versioni di Direct3D o GDI. La modalità Flip Present può essere usata per presentare le finestre figlio. vale a dire, le applicazioni possono usare Flip Model quando non è misto con il modello Blt nello stesso HWND, come illustrato nelle illustrazioni seguenti.

![Illustrazione della finestra padre direct3d e di una finestra figlio gdi, ognuna con hwnd](images/parent-d3d.png)

![Illustrazione della finestra padre gdi e di una finestra figlio direct3d, ognuna con hwnd](images/parent-gdi.png)

Poiché il modello Blt mantiene una copia aggiuntiva della superficie, GDI e altri contenuti Direct3D possono essere aggiunti allo stesso HWND tramite aggiornamenti a frammento da Direct3D e GDI. Usando il modello Flip, sarà visibile solo il contenuto Direct3D 9Ex nelle catene di scambio [**\_ FLIPEX D3DSWAPEFFECT**](/windows/desktop/direct3d9/d3dswapeffect) passate a DWM. Tutti gli altri aggiornamenti del contenuto Direct3D o GDI del modello Blt verranno ignorati, come illustrato nelle illustrazioni seguenti.

![illustrazione del testo gdi che potrebbe non essere visualizzato se si usa il modello flip e il contenuto direct3d e gdi si trova nello stesso hwnd](images/d3d-gdi-same-hwnd.png)

![Illustrazione del contenuto direct3d e gdi in cui dwm è abilitato e l'applicazione è in modalità a finestre](images/d3d-gdinotext-same-hwnd.png)

Pertanto, è necessario che l'opzione Flip Model (Capovolgi modello) sia abilitata per le superfici dei buffer della catena di scambio in cui il solo modello flip Direct3D 9Ex esegue il rendering sull'intero HWND.

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a>Non usare il modello Flip con ScrollWindow o ScrollWindowEx di GDI

Alcune applicazioni Direct3D 9Ex usano le funzioni ScrollWindow o ScrollWindowEx di GDI per aggiornare il contenuto della finestra quando viene attivato un evento di scorrimento utente. ScrollWindow e ScrollWindowEx eseguono blt del contenuto della finestra sullo schermo durante lo scorrimento di una finestra. Queste funzioni richiedono anche aggiornamenti del modello Blt per il contenuto GDI e Direct3D 9Ex. Le applicazioni che usano una delle due funzioni non visualizzano necessariamente il contenuto visibile della finestra scorrendo sullo schermo quando l'applicazione è in modalità a finestre e DWM è abilitato. È consigliabile non usare le API ScrollWindow e ScrollWindowEx di GDI nelle applicazioni e ridisegnarne il contenuto sullo schermo in risposta a uno scorrimento.

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a>Usare una catena di scambio FLIPEX D3DSWAPEFFECT \_ per HWND

Le applicazioni che usano Flip Model non devono usare più catene di scambio Flip Model che hanno come destinazione lo stesso HWND.

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a>Sincronizzazione dei frame delle applicazioni Direct3D 9Ex Flip Model

Le statistiche presenti sono informazioni sulla temporizzazione dei fotogrammi usate dalle applicazioni multimediali per sincronizzare i flussi video e audio e recuperare da problemi di riproduzione video. Per abilitare la disponibilità delle statistiche, l'applicazione Direct3D 9Ex deve assicurarsi che il parametro *BehaviorFlags* passato dall'applicazione a [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contenga il flag di comportamento del dispositivo [D3DCREATE \_ ENABLE \_ PRESENTSTATS.](/windows/desktop/direct3d9/d3dcreate)

Per praticità, la sintassi [**di IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) viene ripetuta qui.

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

Direct3D 9Ex Flip Model aggiunge il flag di presentazione [D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) che applica il comportamento del flag di presentazione [D3DPRESENT \_ INTERVAL \_ IMMEDIATE.](/windows/desktop/direct3d9/d3dpresent) L'applicazione Direct3D 9Ex specifica questi flag di presentazione nel parametro *dwFlags* che l'applicazione passa a [**IDirect3DDevice9Ex::P resentEx,**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)come illustrato di seguito.

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

Quando si modifica l'applicazione Direct3D 9Ex per Windows 7, è necessario considerare le informazioni seguenti sui flag di presentazione [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) specificati:

<dl> <dt>

[D3DPRESENT \_ DONOTFLIP](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

Questo flag è disponibile solo in modalità schermo intero o

(solo Windows 7)

quando l'applicazione imposta il **membro SwapEffect** di [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) su [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in una chiamata a [**CreateDeviceEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)

</dd> <dt>

[D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

(solo Windows 7)

Questo flag può essere specificato solo se l'applicazione imposta il membro **SwapEffect** di [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) su [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in una chiamata a [**CreateDeviceEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) L'applicazione può usare questo flag per aggiornare immediatamente una superficie con diversi frame in un secondo momento nella coda DWM presente, ignorando essenzialmente i fotogrammi intermedi.

Le applicazioni abilitate per FlipEx finestra possono usare questo flag per aggiornare immediatamente una superficie con un frame che si trova in un secondo momento nella coda DWM presente, ignorando i fotogrammi intermedi. Ciò è particolarmente utile per le applicazioni multimediali che vogliono eliminare i fotogrammi che sono stati rilevati come in ritardo e presentano i fotogrammi successivi in fase di composizione. [**IDirect3DDevice9Ex::P resentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) restituisce un errore di parametro non valido se questo flag viene specificato in modo non corretto.

</dd> </dl>

Per ottenere informazioni sulle statistiche presenti, l'applicazione ottiene la struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) chiamando l'API [**IDirect3DSwapChain9Ex::GetPresentStatistics.**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))

La [**struttura D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) contiene statistiche sulle chiamate [**IDirect3DDevice9Ex::P resentEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) Il dispositivo deve essere creato usando una chiamata [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) con il flag [D3DCREATE \_ ENABLE \_ PRESENTSTATS.](/windows/desktop/direct3d9/d3dcreate) In caso contrario, i dati [**restituiti da GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) non sono definiti. Una catena di scambio Direct3D 9Ex abilitata per Flip-Model fornisce informazioni statistiche sia in modalità finestra che a schermo intero.

Per le catene di scambio Direct3D 9Ex abilitate per Blt-Model in modalità finestra, tutti i valori della struttura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) saranno zeri.

Per FlipEx presenta le statistiche, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) restituisce D3DERR \_ PRESENT STATISTICS \_ \_ DISJOINT nelle situazioni seguenti:

-   Prima chiamata a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) in assoluto, che indica l'inizio di una sequenza
-   Transizione DWM da on a off
-   Modifica della modalità: dalla modalità finestra a o da schermo intero o schermo intero a transizioni a schermo intero

Per praticità, la sintassi [**di GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) viene ripetuta qui.

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

Il [**metodo IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) restituisce l'ultimo PresentCount, cio' l'ID presente dell'ultima chiamata present riuscita eseguita da un dispositivo di visualizzazione associato alla catena di scambio. Questo ID presente è il valore **del membro PresentCount** della [**struttura D3DPRESENTSTATS.**](/windows/desktop/direct3d9/d3dpresentstats) Per le catene di scambio Direct3D 9Ex abilitate per Blt-Model, in modalità finestra, tutti i valori della struttura **D3DPRESENTSTATS** saranno zeri.

Per praticità, la sintassi [**di IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) viene ripetuta qui.

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

Quando si modifica l'applicazione Direct3D 9Ex per Windows 7, è necessario considerare le informazioni seguenti sulla [**struttura D3DPRESENTSTATS:**](/windows/desktop/direct3d9/d3dpresentstats)

-   Il valore PresentCount restituito da [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) non viene aggiornato quando una chiamata [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT DONOTWAIT specificato nel \_ parametro *dwFlags* restituisce un errore.
-   Quando [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) viene chiamato con D3DPRESENT \_ DONOTFLIP, una [**chiamata GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ha esito positivo, ma non restituisce una struttura [**D3DPRESENTSTATS aggiornata**](/windows/desktop/direct3d9/d3dpresentstats) quando l'applicazione è in modalità finestra.
-   **PresentRefreshCount** e **SyncRefreshCount** in [**D3DPRESENTSTATS:**](/windows/desktop/direct3d9/d3dpresentstats)
    -   **PresentRefreshCount è** uguale a **SyncRefreshCount** quando l'applicazione viene presentata in ogni vsync.
    -   **SyncRefreshCount** viene ottenuto nell'intervallo vsync quando è stato inviato il valore presente, **Mentre SyncQPCTime** corrisponde approssimativamente all'ora associata all'intervallo di vsync.

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a>Sincronizzazione dei frame per le applicazioni finestra quando DWM è disattivato

Quando DWM è disattivato, le applicazioni finestra vengono visualizzate direttamente sullo schermo del monitor senza passare attraverso una catena di capovolgimento. In Windows Vista non è disponibile alcun supporto per ottenere informazioni sulle statistiche dei frame per le applicazioni finestra quando DWM è disattivato. Per mantenere un'API in cui le applicazioni non devono essere in grado di riconoscere DWM, Windows 7 restituirà informazioni statistiche sui frame per le applicazioni finestra quando DWM è disattivato. Le statistiche dei frame restituite quando DWM è disattivato sono solo stime.

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a>Walk-Through di un modello flip Direct3D 9Ex e present statistics sample

**Per acconsentire esplicitamente alla presentazione FlipEx per l'esempio Direct3D 9Ex**

1.  Verificare che l'applicazione di esempio sia in esecuzione Windows versione 7 o successiva del sistema operativo.
2.  Impostare il **membro SwapEffect** di [**D3DPRESENT \_ PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) su [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in una chiamata a [**CreateDeviceEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)


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



**Per acconsentire esplicitamente anche all'esempio Present Statistics for Direct3D 9Ex associato a FlipEx**

-   Impostare [D3DCREATE \_ ENABLE \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) nel *parametro BehaviorFlags* di [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).


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



**Per evitare problemi, rilevare e recuperare da problemi**

1.  Chiamate presenti nella coda: il numero di backbuffer consigliato è da 2 a 4.
2.  L'esempio Direct3D 9Ex aggiunge un backbuffer implicito, la lunghezza effettiva della coda Present è backbuffer count + 1.
3.  Creare la struttura della coda Present dell'helper per archiviare tutti gli ID presente (PresentCount) inviati correttamente e presentRefreshCount associati, calcolati o previsti.
4.  Per rilevare l'occorrenza di problemi:

    -   Chiamare [**GetPresentStatistics.**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))
    -   Ottenere l'ID presente (PresentCount) e il conteggio vsync in cui viene visualizzato il frame (PresentRefreshCount) del frame di cui vengono ottenute le statistiche presenti.
    -   Recuperare l'oggetto PresentRefreshCount previsto (TargetRefresh nel codice di esempio) associato all'ID presente.
    -   Se presentRefreshCount effettivo è successivo al previsto, si è verificato un problema.

5.  Per eseguire il ripristino da un problema:

    -   Calcolare il numero di fotogrammi da ignorare (g \_ iImmediates variabile nel codice di esempio).
    -   Presentare i fotogrammi ignorati con l'intervallo D3DPRESENT \_ FORCEIMMEDIATE.

**Considerazioni sul rilevamento e il ripristino degli errori**

1.  Il recupero con glitch accetta N (g variabile iQueueDelay nel codice di esempio) numero di chiamate Present in cui \_ N (g iQueueDelay) è uguale a \_ g iImmediates più lunghezza della coda \_ Present, ovvero:

    -   Ignorare i fotogrammi con intervallo corrente D3DPRESENT \_ FORCEIMMEDIATE, più
    -   Presenta in coda che devono essere elaborati

2.  Impostare un limite per la lunghezza degli glitch (GLITCH \_ RECOVERY \_ LIMIT nell'esempio). Se l'applicazione di esempio non è in grado di eseguire il ripristino da un problema troppo lungo (ad esempio, 1 secondo o 60 vsync su un monitor a 60 Hz), passare all'animazione intermittente e reimpostare la coda helper Presente.


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

-   La figura seguente mostra un'applicazione con un numero di backbuffer di 4. La lunghezza effettiva della coda present è quindi 5.

    ![illustrazione di un'applicazione di frame sottoposti a rendering e di una coda presente](images/sample-scenario.png)

    Il frame A è destinato a essere visualizzato sullo schermo nel conteggio dell'intervallo di sincronizzazione di 1, ma è stato rilevato che è stato visualizzato con un numero di intervalli di sincronizzazione di 4. Di conseguenza, si è verificato un problema. I 3 fotogrammi successivi vengono presentati con D3DPRESENT \_ INTERVAL \_ FORCEIMMEDIATE. Il problema dovrebbe richiedere un totale di 8 chiamate presenti prima del ripristino. Il frame successivo verrà visualizzato in base al numero di intervalli di sincronizzazione di destinazione.

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a>Riepilogo delle attività di programmazione Consigli la sincronizzazione dei frame

-   Crea un elenco di backup di tutti gli ID LastPresentCount (ottenuti tramite [**GetLastPresentCount)**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)e di PresentRefreshCount stimati associati di tutti i present inviati.
    > [!Note]  
    > Quando l'applicazione chiama [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT \_ DONOTFLIP, la [**chiamata GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ha esito positivo, ma non restituisce una struttura [**D3DPRESENTSTATS aggiornata**](/windows/desktop/direct3d9/d3dpresentstats) quando l'applicazione è in modalità finestra.

     

-   Chiamare [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) per ottenere il presentRefreshCount effettivo associato a ogni ID presente dei fotogrammi visualizzati, per assicurarsi che l'applicazione gestisca i risultati dell'errore restituiti dalla chiamata.
-   Se il valore effettivo di PresentRefreshCount è successivo al valore stimato di PresentRefreshCount, viene rilevato un problema. Compensare inviando present dei fotogrammi in ritardo con D3DPRESENT \_ FORCEIMMEDIATE.
-   Quando un frame viene presentato in ritardo nella coda present, tutti i fotogrammi in coda successivi verranno presentati in ritardo. D3DPRESENT \_ FORCEIMMEDIATE correggerà solo il frame successivo da presentare dopo tutti i frame in coda. Pertanto, il numero di code o backbuffer presenti non deve essere troppo lungo, quindi ci sono meno problemi di frame da recuperare. Il numero di backbuffer ottimale è da 2 a 4.
-   Se il valore stimato di PresentRefreshCount è successivo a quello effettivo di PresentRefreshCount, è possibile che si sia verificata la limitazione DWM. Sono possibili le soluzioni seguenti:

    -   riduzione della lunghezza attuale della coda
    -   riduzione dei requisiti di memoria GPU con qualsiasi altro mezzo, oltre a ridurre la lunghezza della coda attuale (ovvero, riducendo la qualità, rimuovendo gli effetti e così via)
    -   specifica di [**DwmEnableMMCSS per**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) impedire la limitazione DWM in generale

-   Verificare la funzionalità di visualizzazione dell'applicazione e le prestazioni delle statistiche dei frame negli scenari seguenti:

    -   con DWM on e off
    -   modalità esclusiva e finestra a schermo intero
    -   hardware con funzionalità inferiori

-   Quando le applicazioni non possono eseguire il ripristino da un numero elevato di frame con anomalie con D3DPRESENT FORCEIMMEDIATE Presente, possono potenzialmente eseguire \_ le operazioni seguenti:

    -   ridurre l'utilizzo di CPU e GPU grazie al rendering con un carico di lavoro inferiore.
    -   Nel caso della decodifica video, decodificare più velocemente riducendo la qualità e, di conseguenza, l'utilizzo di CPU e GPU.

## <a name="conclusion-about-direct3d-9ex-improvements"></a>Conclusioni sui miglioramenti di Direct3D 9Ex

In Windows 7, le applicazioni che visualizzano la frequenza dei fotogrammi del misuratore o del video durante la presentazione possono acconsentire esplicitamente al modello di capovolgimento. I miglioramenti attuali delle statistiche associati a Flip Model Direct3D 9Ex possono trarre vantaggio dalle applicazioni che sincronizzano la presentazione per frequenza dei fotogrammi, con feedback in tempo reale per il rilevamento e il ripristino di anomalie. Gli sviluppatori che adottano direct3D 9Ex Flip Model devono prendere in considerazione la selezione di un HWND separato dal contenuto GDI e dalla sincronizzazione della frequenza dei fotogrammi. Vedere i dettagli in questo argomento e la documentazione MSDN. Per altre informazioni, vedere [Il Centro per sviluppatori DirectX su MSDN.](/previous-versions/windows/apps/hh452744(v=win.10))

## <a name="call-to-action"></a>Invito all'azione ##

Si consiglia di usare Direct3D 9Ex Flip Model e le statistiche presenti in Windows 7 quando si creano applicazioni che tentano di sincronizzare la frequenza dei fotogrammi di presentazione o di recuperare da problemi di visualizzazione.

## <a name="related-topics"></a>Argomenti correlati

[Centro per sviluppatori DirectX su MSDN](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> </dl>