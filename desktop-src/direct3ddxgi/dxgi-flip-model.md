---
description: In Windows 8 è stato aggiunto il supporto per il modello Flip Presentation e le statistiche presenti associate in DXGI 1,2.
ms.assetid: E132DAF5-80B7-4C52-A760-3779CC140CE7
title: Modello DXGI Flip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ee82febd13a3b57a06d93fd01eb8d230d6b78a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876633"
---
# <a name="dxgi-flip-model"></a>Modello DXGI Flip

In Windows 8 è stato aggiunto il supporto per il modello Flip Presentation e le statistiche presenti associate in DXGI 1,2. Il modello DXGI Flip Presentation di Windows 8 è simile alla presentazione di Windows 7 [Direct3D 9Ex Flip Mode](../direct3darticles/direct3d-9ex-improvements.md). Le app di presentazione basate sulla frequenza dei video o dei frame, ad esempio i giochi, possono trarre vantaggio dalla maggior parte usando il modello Flip Presentation. Le app che usano il modello DXGI Flip Presentation riducono il carico delle risorse di sistema e aumentano le prestazioni. Le app possono anche usare i miglioramenti attuali delle statistiche con il modello Flip Presentation per controllare meglio la frequenza di presentazione fornendo i meccanismi di correzione e feedback in tempo reale.

-   [Confronto tra il modello DXGI Flip e il modello BitBlt](#comparing-the-dxgi-flip-model-and-the-bitblt-model)
-   [Come usare DXGI flip model](#how-to-use-dxgi-flip-model)
-   [Sincronizzazione dei frame delle app DXGI flip model](#frame-synchronization-of-dxgi-flip-model-apps)
-   [Prevenzione, rilevamento e ripristino da problemi](#avoiding-detecting-and-recovering-from-glitches)
-   [Argomenti correlati](#related-topics)

## <a name="comparing-the-dxgi-flip-model-and-the-bitblt-model"></a>Confronto tra il modello DXGI Flip e il modello BitBlt

Il runtime usa i modelli di trasferimento a blocchi di bit (BitBlt) e flip Presentation per presentare contenuti grafici nei monitor di visualizzazione. La differenza principale tra i modelli BitBlt e flip Presentation è il modo in cui il contenuto del buffer di back-buffer arriva a Windows 8 DWM per la composizione. Nel modello BitBlt, il contenuto del buffer nascosto viene copiato nell'area di reindirizzamento a ogni chiamata a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). Nel modello flip tutti i buffer back sono condivisi con la Gestione finestre desktop (DWM). Di conseguenza, DWM può comporre direttamente da questi buffer di back senza altre operazioni di copia. In generale, il modello Flip è più efficiente. Il modello Flip fornisce anche altre funzionalità, ad esempio le statistiche attuali avanzate.

Se si dispone di componenti legacy che utilizzano Windows Graphics Device Interface (GDI) per scrivere direttamente in un [**HWND**](../winprog/windows-data-types.md) , utilizzare il modello BitBlt.

I miglioramenti delle prestazioni del modello DXGI flip sono significativi quando l'app è in modalità finestra. La sequenza in questa tabella e l'illustrazione confrontano gli utilizzi della larghezza di banda della memoria e le letture del sistema e le scritture delle app finestra che scelgono Capovolgi modello rispetto al modello BitBlt.



| Passaggio | Modello BitBlt presente in DWM                                                                               | Modello DXGI Flip presente in DWM                                   |
|------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 1.   | L'app Aggiorna il frame (scrittura)<br/>                                                              | L'app Aggiorna il frame (scrittura)<br/>                     |
| 2.   | Il runtime Direct3D copia il contenuto della superficie in una superficie di reindirizzamento di DWM (lettura, scrittura)<br/>            | Il runtime Direct3D passa l'area dell'app a DWM<br/>        |
| 3.   | Al termine della copia della superficie condivisa, DWM esegue il rendering dell'area dell'app sullo schermo (lettura, scrittura)<br/> | DWM esegue il rendering dell'area dell'app sullo schermo (lettura, scrittura)<br/> |



 

![illustrazione di un confronto tra il modello BLT e il modello Flip](images/blt-flip-mode-present.png)

Il modello Flip riduce l'utilizzo della memoria di sistema riducendo il numero di letture e scritture da parte del runtime Direct3D per la composizione del frame finestra di DWM.

## <a name="how-to-use-dxgi-flip-model"></a>Come usare DXGI flip model

Per le app Direct3D 11,1 destinate a Windows 8 viene usato Capovolgi modello creando la catena di scambio con il valore di enumerazione [**\_ \_ \_ \_ sequenziale di DXGI swap effect Flip**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) impostato nel membro **SwapEffect** della struttura [**DXGI della catena di \_ scambio \_ \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) . Quando si imposta **SwapEffect** su **DXGI \_ swap \_ Effect \_ Flip \_ sequenziale**, impostare anche questi membri **della \_ catena di scambio DXGI \_ \_ DESC1** sui valori indicati:

-   **BufferCount** a un valore compreso tra 2 e 16 per evitare una riduzione delle prestazioni in seguito all'attesa del rilascio del buffer di presentazione precedente in DWM.
-   **Format** to DXGI \_ Format \_ R16G16B16A16 \_ float, DXGI \_ Format \_ B8G8R8A8 \_ UNORM o DXGI \_ Format \_ \_ R8G8B8A8 UNORM
-   **Conteggio** del membro della [**struttura \_ \_ desc di esempio DXGI**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc) che il membro **SampleDesc** specifica a uno e il membro di **qualità** di **DXGI \_ Sample \_ desc** su zero perché non è supportato l'anti-aliasing di più campioni (MSAA)

Se si usa [**DXGI \_ swap \_ Effect \_ Flip \_ sequenziale**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) in Windows 7 o in un sistema operativo precedente, la creazione del dispositivo ha esito negativo. Quando si usa Capovolgi modello, è possibile usare le statistiche presenti a schermo intero in modalità finestra. Il comportamento a schermo intero non è interessato. Se si passa **null** al parametro *pFullscreenDesc* di [**IDXGIFactory2:: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) per una catena di scambio a finestra e si imposta **SwapEffect** su DXGI Inverti **effetto di \_ scambio \_ \_ \_ sequenziale**, il runtime crea un buffer indietro aggiuntivo e ruota a seconda di quale handle appartiene al buffer che diventa il buffer anteriore al momento della presentazione.

Quando si usa Capovolgi modello, prendere in considerazione i suggerimenti seguenti:

-   Usare una catena di scambio di tipo flip per [**HWND**](../winprog/windows-data-types.md). Non indirizzare più catene di scambio del modello Flip allo stesso **HWND**.
-   Non usare la catena di scambio flip model con la funzione [**ScrollWindow**](/windows/win32/api/winuser/nf-winuser-scrollwindow) o [**ScrollWindowEx**](/windows/win32/api/winuser/nf-winuser-scrollwindowex) di GDI. Alcune app Direct3D usano le funzioni **ScrollWindow** e **ScrollWindowEx** di GDI per aggiornare il contenuto della finestra dopo che si è verificato un evento di scorrimento utente. **ScrollWindow** e **ScrollWindowEx** eseguono BitBlts del contenuto della finestra sullo schermo quando l'utente scorre una finestra. Queste funzioni richiedono anche aggiornamenti del modello BitBlt per il contenuto GDI e Direct3D. Per le app che usano una delle due funzioni non verrà necessariamente visualizzato lo scorrimento del contenuto della finestra visibile sullo schermo quando l'app è in modalità finestra. Si consiglia di non utilizzare le funzioni **ScrollWindow** e **ScrollWindowEx** di GDI e di ricreare i contenuti GDI e Direct3D sullo schermo in risposta allo scorrimento.
-   Usare Capovolgi modello in un [**HWND**](../winprog/windows-data-types.md) non indirizzato anche ad altre API, tra cui il modello di presentazione DXGI BitBlt, altre versioni di Direct3D o GDI. Poiché il modello BitBlt gestisce una copia aggiuntiva dell'area, è possibile aggiungere GDI e altri contenuti Direct3D allo stesso **HWND** tramite aggiornamenti a fasi da Direct3D e GDI. Quando si usa il modello Flip, solo il contenuto Direct3D nelle catene di scambio flip model che il runtime passa a DWM è visibile. Il runtime ignora tutti gli altri aggiornamenti del contenuto Direct3D o GDI del modello BitBlt.

## <a name="frame-synchronization-of-dxgi-flip-model-apps"></a>Sincronizzazione dei frame delle app DXGI flip model

Le statistiche attuali sono informazioni sugli intervalli di frame usati dalle app multimediali per sincronizzare i flussi video e audio e per eseguire il ripristino da problemi di riproduzione video. Le app possono usare le informazioni relative alla temporizzazione dei frame nelle statistiche attuali per modificare la frequenza di presentazione dei fotogrammi video per una presentazione più uniforme. Per ottenere le informazioni sulle statistiche presenti, chiamare il metodo [**IDXGISwapChain:: GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) per ottenere la struttura delle [**\_ \_ statistiche di frame DXGI**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) . **DXGI \_ Le \_ statistiche dei frame** contengono statistiche sulle chiamate a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) . Una catena di scambio Flip Model fornisce le informazioni statistiche presenti nelle modalità finestra e a schermo intero. Per le catene di scambio del modello BitBlt in modalità finestra, tutti i valori delle **\_ \_ statistiche del frame di DXGI** sono pari a zero.

Per le statistiche di tipo flip model, [**IDXGISwapChain:: GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) restituisce **DXGI \_ Error \_ frame \_ Statistics \_ disgiunte** nelle situazioni seguenti:

-   Prima chiamata a [**GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics), che indica l'inizio di una sequenza
-   Modifica della modalità: in modalità finestra a o da schermo intero o a schermo intero a transizioni a schermo intero

I valori nei membri **PresentRefreshCount**, **SyncRefreshCount** e **SyncQPCTime** di [**DXGI \_ frame \_ Statistics**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) hanno le caratteristiche seguenti:

-   **PresentRefreshCount** è uguale a **SyncRefreshCount** quando l'app presenta ogni vsync.
-   **SyncRefreshCount** viene ottenuto nell'intervallo vsync quando è stato inviato il presente, **SyncQPCTime** è approssimativamente il tempo associato all'intervallo vsync.

Il metodo [**IDXGISwapChain:: GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount) restituisce l'ultimo conteggio presente, ovvero l'ID attuale dell'ultima chiamata di [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) eseguita da un dispositivo di visualizzazione associato alla catena di scambio. Questo ID attuale è il valore del membro **PresentCount** della struttura [**DXGI \_ frame \_ Statistics**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) . Per le catene di scambio del modello BitBlt, in modalità finestra, tutti i valori delle **\_ \_ statistiche del frame di DXGI** sono pari a zero.

## <a name="avoiding-detecting-and-recovering-from-glitches"></a>Prevenzione, rilevamento e ripristino da problemi

Eseguire questi passaggi per evitare, rilevare e ripristinare le anomalie nella presentazione del frame:

1.  Queue [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) chiama, ovvero Call **IDXGISwapChain1::P resent1** più volte, che ne determina la raccolta in una coda.
2.  Creare una struttura present-Queue per archiviare tutti i [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)present ID (restituito da [**IDXGISwapChain:: GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount)) e i valori associati, calcolati/previsti **PresentRefreshCount** .
3.  Per rilevare un problema:

    -   Chiamare [**IDXGISwapChain:: GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics).
    -   Per questo frame, ottenere l'ID attuale (**PresentCount**) e il numero di VSync in cui il sistema operativo ha presentato l'ultima immagine al monitor (**PresentRefreshCount**).
    -   Recuperare il **PresentRefreshCount** previsto associato all'ID presente e archiviato in precedenza nella struttura della coda corrente.
    -   Se il valore di **PresentRefreshCount** effettivo è successivo al valore previsto di **PresentRefreshCount**, si è verificato un problema.

4.  Per risolvere il problema:

    -   Calcolare il numero di frame da ignorare per il ripristino dal problema. Se, ad esempio, il passaggio 3 indica che il numero di vsync previsto (**PresentRefreshCount**) per un ID presente (**PresentCount**) è 5 e il conteggio vsync effettivo per l'ID attuale è 8, il numero di frame da ignorare per il recupero dal glitch è 3 fotogrammi.
    -   Passare 0 al parametro *SyncInterval* in questo numero di chiamate a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) per eliminare e ignorare questo numero di frame.

        > [!Note]  
        > Se il problema è costituito da un numero elevato di frame, chiamare [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) con il parametro *Flags* impostato su [**DXGI \_ present \_ Restart**](dxgi-present.md) per eliminare e ignorare tutti i rilasci in coda in attesa.

         

Di seguito è riportato uno scenario di esempio di ripristino da glitch nella presentazione frame:

![illustrazione di un esempio di scenario di ripristino da glitch nella presentazione di frame](images/frame-sync-glitch-recover.png)

Nello scenario di esempio si prevede che il frame a venga visualizzato sullo schermo in un numero di vsync pari a 1. Ma si rileva effettivamente il numero di vsync che frame A viene visualizzato sullo schermo come 4. Pertanto, si determina che si è verificato un problema. È quindi possibile rimuovere 3 frame, ovvero è possibile passare 0 al parametro *SyncInterval* in 3 chiamate a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). Nello scenario di esempio precedente, per risolvere il problema, è necessario un totale di 8 **IDXGISwapChain1::P resent1** chiamate. Il nono frame viene quindi visualizzato in base al numero di vsync previsto.

Ecco una riga temporale degli eventi di presentazione. Ogni linea verticale rappresenta un vsync. La direzione orizzontale è Time, che aumenta a destra. È possibile usare la figura per immaginare come possono verificarsi le anomalie.

![illustrazione di una linea temporale degli eventi di presentazione](images/present-timeline.png)

La figura illustra questa sequenza:

1.  L'app viene riattivata in vsync, esegue il rendering di Blue, chiama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)e quindi torna alla modalità sospensione.
2.  L'unità di elaborazione grafica (GPU) viene riattivata da inattiva, esegue il rendering in blu e quindi torna alla modalità sospensione.
3.  DWM si riattiva alla successiva vsync, compone il blu nel buffer nascosto, chiama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)e quindi torna alla modalità di sospensione.
4.  L'app viene riattivata, il rendering verde, chiama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)e quindi torna alla modalità sospensione.
    > [!Note]  
    > L'app viene eseguita contemporaneamente mentre la GPU esegue la composizione del blu.

     

5.  Il rendering della GPU viene quindi visualizzato in verde per l'app.
6.  Infine, il convertitore da digitale a analogico (DAC) Mostra i risultati della composizione di DWM sul monitor nella vsync successiva.

Dalla sequenza temporale è possibile immaginare la latenza delle statistiche presenti e il modo in cui possono verificarsi le anomalie. Ad esempio, per visualizzare un glitch di DWM per il colore verde visualizzato sullo schermo, si supponga di ampliare la casella verde/rosso in modo che il lato destro della casella verde/rossa corrisponda al lato destro della casella viola/rosso. In questo scenario, l'applicazione livello dati Mostra due fotogrammi di blu e quindi il frame verde. È possibile notare che questo problema si è verificato leggendo le statistiche presenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento della presentazione con il modello Flip, i rettangoli Dirty e le aree a scorrimento](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
