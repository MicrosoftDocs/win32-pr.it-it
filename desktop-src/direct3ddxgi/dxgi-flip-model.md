---
description: Windows 8 il supporto per il modello di presentazione flip e le statistiche presenti associate in DXGI 1.2.
ms.assetid: E132DAF5-80B7-4C52-A760-3779CC140CE7
title: Modello di inversione DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b4b4cf8f792a23d4d32e5cb4b4273594745283cb803a638ea3d0cf4c45977f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289462"
---
# <a name="dxgi-flip-model"></a>Modello di inversione DXGI

Windows 8 il supporto per il modello di presentazione flip e le statistiche presenti associate in DXGI 1.2. Windows 8 del modello di presentazione flip DXGI è simile Windows presentazione della modalità flip [Direct3D 9EX di 7.](../direct3darticles/direct3d-9ex-improvements.md) Le app di presentazione basate su frequenza di fotogrammi o video, ad esempio i giochi, possono trarre maggior vantaggio usando il modello di presentazione flip. Le app che usano il modello di presentazione flip DXGI riducono il carico delle risorse di sistema e aumentano le prestazioni. Le app possono anche usare miglioramenti delle statistiche presenti con il modello di presentazione flip per controllare meglio la frequenza di presentazione fornendo meccanismi di feedback e correzione in tempo reale.

-   [Confronto tra il modello flip DXGI e il modello BitBlt](#comparing-the-dxgi-flip-model-and-the-bitblt-model)
-   [Come usare il modello di inversione DXGI](#how-to-use-dxgi-flip-model)
-   [Sincronizzazione dei frame delle app modello flip DXGI](#frame-synchronization-of-dxgi-flip-model-apps)
-   [Evitare, rilevare e ripristinare da errori](#avoiding-detecting-and-recovering-from-glitches)
-   [Argomenti correlati](#related-topics)

## <a name="comparing-the-dxgi-flip-model-and-the-bitblt-model"></a>Confronto tra il modello flip DXGI e il modello BitBlt

Il runtime usa il trasferimento a blocchi di bit (bitblt) e i modelli di presentazione capovolgimento per presentare contenuto grafico sui monitor di visualizzazione. La differenza principale tra i modelli di presentazione bitblt e flip è il modo in cui il contenuto del buffer nascosto arriva al Windows 8 DWM per la composizione. Nel modello bitblt il contenuto del buffer nascosto viene copiato nella superficie di reindirizzamento in ogni chiamata a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). Nel modello flip tutti i buffer back vengono condivisi con il Gestione finestre desktop (DWM). Di conseguenza, DWM può comporre direttamente da tali buffer back senza operazioni di copia aggiuntive. In generale, il modello flip è più efficiente. Il modello flip offre anche altre funzionalità, ad esempio statistiche attuali migliorate.

Se si dispone di componenti legacy che usano Windows Graphics Device Interface (GDI) per scrivere direttamente in [**HWND,**](../winprog/windows-data-types.md) usare il modello bitblt.

I miglioramenti delle prestazioni del modello di inversione DXGI sono significativi quando l'app è in modalità a finestre. La sequenza in questa tabella e l'illustrazione confrontano gli utilizzi della larghezza di banda della memoria e le operazioni di lettura e scrittura di sistema delle app con finestre che scelgono il modello flip rispetto al modello bitblt.



| Passaggio | Modello BitBlt presente in DWM                                                                               | Modello flip DXGI presente in DWM                                   |
|------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 1.   | L'app aggiorna il frame (scrittura)<br/>                                                              | L'app aggiorna il frame (scrittura)<br/>                     |
| 2.   | Il runtime Direct3D copia il contenuto della superficie in una superficie di reindirizzamento DWM (Lettura, Scrittura)<br/>            | Il runtime Direct3D passa la superficie dell'app a DWM<br/>        |
| 3.   | Al termine della copia della superficie condivisa, DWM esegue il rendering della superficie dell'app sullo schermo (lettura, scrittura)<br/> | DWM esegue il rendering della superficie dell'app sullo schermo (lettura, scrittura)<br/> |



 

![illustrazione di un confronto tra il modello blt e il modello flip](images/blt-flip-mode-present.png)

Il modello flip riduce l'utilizzo della memoria di sistema riducendo il numero di operazioni di lettura e scrittura da parte del runtime Direct3D per la composizione dei frame con finestra da parte di DWM.

## <a name="how-to-use-dxgi-flip-model"></a>Come usare il modello di inversione DXGI

Le app Direct3D 11.1 che usano Windows 8 usano il modello flip creando la catena di scambio con il valore di enumerazione [**DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) impostato nel membro **SwapEffect** della struttura [**DXGI \_ SWAP CHAIN \_ \_ DESC1.**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) Quando si imposta **SwapEffect** su **DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL,** impostare anche questi membri di **DXGI \_ SWAP CHAIN \_ \_ DESC1** sui valori indicati:

-   **BufferCount** su un valore compreso tra 2 e 16 per evitare una perdita di prestazioni in seguito all'attesa in DWM di rilasciare il buffer di presentazione precedente.
-   **Format** to DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT, DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM o DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM
-   **Contare** il membro della struttura [**\_ \_ DESC DXGI SAMPLE**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc) specificato dal membro **SampleDesc** su uno e il membro **Quality** di **DXGI \_ SAMPLE \_ DESC** su zero perché l'antialiasing a più campioni (MSAA) non è supportato

Se si usa [**DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) Windows 7 o versioni precedenti del sistema operativo, la creazione del dispositivo non riesce. Quando si usa il modello flip, è possibile usare le statistiche di presentazione a schermo intero in modalità finestra. Il comportamento a schermo intero non è interessato. Se si passa **NULL** al parametro *pFullscreenDesc* [**di IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) per una catena di scambio con finestra e si imposta **SwapEffect** su **DXGI \_ SWAP EFFECT FLIP FLIP \_ \_ \_ SEQUENTIAL,** il runtime crea un buffer nascosto aggiuntivo e ruota qualsiasi handle appartenente al buffer che diventa il front buffer in fase di presentazione.

Quando si usa il modello flip, prendere in considerazione questi suggerimenti:

-   Usare una catena di scambio del modello flip per [**HWND**](../winprog/windows-data-types.md). Non impostare come destinazione più catene di scambio del modello flip allo stesso **HWND.**
-   Non usare la catena di scambio del modello flip con la funzione [**ScrollWindow**](/windows/win32/api/winuser/nf-winuser-scrollwindow) o [**ScrollWindowEx**](/windows/win32/api/winuser/nf-winuser-scrollwindowex) di GDI. Alcune app Direct3D usano le funzioni **ScrollWindow** e **ScrollWindowEx** di GDI per aggiornare il contenuto della finestra dopo che si verifica un evento di scorrimento utente. **ScrollWindow** e **ScrollWindowEx** eseguono bitblts del contenuto della finestra sullo schermo mentre l'utente scorre una finestra. Queste funzioni richiedono anche aggiornamenti del modello bitblt per il contenuto GDI e Direct3D. Le app che usano una delle due funzioni non visualizzano necessariamente il contenuto della finestra visibile scorrendo sullo schermo quando l'app è in modalità a finestre. È consigliabile non usare le funzioni **ScrollWindow** e **ScrollWindowEx** di GDI e ridisegnare invece il contenuto GDI e Direct3D sullo schermo in risposta a uno scorrimento.
-   Usare il modello flip in [**un HWND**](../winprog/windows-data-types.md) non destinato anche ad altre API, tra cui il modello di presentazione bitblt DXGI, altre versioni di Direct3D o GDI. Poiché il modello bitblt mantiene una copia aggiuntiva della superficie, è possibile aggiungere GDI e altri contenuti Direct3D allo stesso **HWND** tramite aggiornamenti a frammento da Direct3D e GDI. Quando si usa il modello flip, sono visibili solo il contenuto Direct3D nelle catene di scambio del modello flip passate dal runtime a DWM. Il runtime ignora tutti gli altri aggiornamenti del contenuto Direct3D o GDI del modello bitblt.

## <a name="frame-synchronization-of-dxgi-flip-model-apps"></a>Sincronizzazione dei frame delle app modello flip DXGI

Le statistiche presenti sono informazioni di temporizzazione dei fotogrammi usate dalle app multimediali per sincronizzare i flussi video e audio e recuperare da problemi di riproduzione video. Le app possono usare le informazioni di temporizzazione dei fotogrammi nelle statistiche presenti per regolare la velocità di presentazione dei fotogrammi video per una presentazione più uniforme. Per ottenere informazioni sulle statistiche presenti, chiamare il [**metodo IDXGISwapChain::GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) per ottenere la [**struttura DXGI \_ FRAME \_ STATISTICS.**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) **DXGI \_ FRAME \_ STATISTICS** contiene statistiche sulle [**chiamate IDXGISwapChain1::P resent1.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) Una catena di scambio di modelli di inversione fornisce informazioni statistiche presenti sia in modalità a finestra che a schermo intero. Per le catene di scambio di modelli bitblt in modalità finestra, tutti i valori **di DXGI \_ FRAME \_ STATISTICS** sono zeri.

Per le statistiche di presentazione del modello flip, [**IDXGISwapChain::GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) restituisce **DXGI \_ ERROR FRAME STATISTICS \_ \_ \_ DISJOINT** nelle situazioni seguenti:

-   Prima chiamata a [**GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics), che indica l'inizio di una sequenza
-   Modifica della modalità: dalla modalità finestra a o da schermo intero o da schermo intero a transizioni a schermo intero

I valori nei **membri PresentRefreshCount,** **SyncRefreshCount** e **SyncQPCTime** di [**DXGI \_ FRAME \_ STATISTICS**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) presentano le caratteristiche seguenti:

-   **PresentRefreshCount è** uguale a **SyncRefreshCount** quando l'app viene presentata in ogni vsync.
-   **SyncRefreshCount** viene ottenuto nell'intervallo vsync quando è stato inviato il presente, **SyncQPCTime** corrisponde approssimativamente all'ora associata all'intervallo vsync.

Il metodo [**IDXGISwapChain::GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount) restituisce l'ultimo conteggio presente, cioè l'ID corrente dell'ultima chiamata [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) eseguita da un dispositivo di visualizzazione associato alla catena di scambio. Questo ID corrente è il valore del **membro PresentCount** della struttura [**DXGI \_ FRAME \_ STATISTICS.**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) Per le catene di scambio di modelli bitblt, mentre in modalità finestra, tutti i valori **di DXGI \_ FRAME \_ STATISTICS** sono zeri.

## <a name="avoiding-detecting-and-recovering-from-glitches"></a>Evitare, rilevare e ripristinare da errori

Eseguire questi passaggi per evitare, rilevare e ripristinare gli errori nella presentazione dei frame:

1.  Chiamate [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) della coda( ovvero chiamare **IDXGISwapChain1::P resent1** più volte, che ne fa la raccolta in una coda).
2.  Creare una struttura della coda di presentazione per archiviare tutti gli [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)dell'ID presente (restituito da [**IDXGISwapChain::GetLastPresentCount)**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount)e i valori **PresentRefreshCount** associati, calcolati e previsti.
3.  Per rilevare un problema:

    -   Chiamare [**IDXGISwapChain::GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics).
    -   Per questo frame, ottenere l'ID presente (**PresentCount**) e il conteggio vsync in cui il sistema operativo ha presentato l'ultima immagine al monitoraggio (**PresentRefreshCount**).
    -   Recuperare **l'oggetto PresentRefreshCount** previsto associato all'ID corrente e archiviato in precedenza nella struttura della coda corrente.
    -   Se **l'oggetto PresentRefreshCount effettivo** è successivo al valore **previsto di PresentRefreshCount,** si è verificato un errore.

4.  Per eseguire il ripristino dal problema:

    -   Calcolare il numero di fotogrammi da ignorare per il ripristino dal problema. Ad esempio, se il passaggio 3 rivela che il conteggio vsync previsto (**PresentRefreshCount**) per un ID presente (**PresentCount**) è 5 e il conteggio vsync effettivo per l'ID corrente è 8, il numero di fotogrammi da ignorare per il ripristino dal problema è 3 fotogrammi.
    -   Passare 0 al parametro *SyncInterval* in questo numero di chiamate a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) per eliminare e ignorare questo numero di frame.

        > [!Note]  
        > Se il problema è costituito da un numero elevato di frame, chiamare [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) con il parametro *Flags* impostato su [**DXGI \_ PRESENT \_ RESTART**](dxgi-present.md) per eliminare e ignorare tutti i present in coda in sospeso.

         

Di seguito è riportato uno scenario di esempio di ripristino da problemi nella presentazione dei frame:

![Illustrazione di uno scenario di esempio di ripristino da problemi nella presentazione dei frame](images/frame-sync-glitch-recover.png)

Nello scenario di esempio si prevede che il frame A andrà sullo schermo con un conteggio vsync di 1. Ma si rileva effettivamente il numero di vsync che il frame A viene visualizzato sullo schermo come 4. Di conseguenza, si determina che si è verificato un problema. È quindi possibile eliminare 3 fotogrammi, in modo che sia possibile passare 0 al parametro *SyncInterval* in 3 chiamate a [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). Nello scenario di esempio precedente, per eseguire il ripristino dal problema di errore, è necessario un totale di 8 **chiamate IDXGISwapChain1::P resent1.** Il nono frame è quindi visibile in base al numero di vsync previsto.

Ecco una linea temporale di eventi di presentazione. Ogni linea verticale rappresenta un vsync. La direzione orizzontale è il tempo, che aumenta a destra. È possibile usare la figura per immaginare come possono verificarsi gli errori.

![illustrazione di una linea temporale di eventi di presentazionel](images/present-timeline.png)

La figura illustra questa sequenza:

1.  L'app si riattiva su vsync, esegue il rendering blu, chiama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)e quindi torna in sospensione.
2.  L'unità di elaborazione grafica (GPU) si riattiva dall'inattività, esegue il rendering in blu e quindi torna in sospensione.
3.  Il DWM si riattiva al successivo vsync, compone blu nel buffer nascosto, chiama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)e quindi torna in sospensione.
4.  L'app si riattiva, esegue il rendering verde, chiama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)e quindi torna in sospensione.
    > [!Note]  
    > L'app viene eseguita contemporaneamente mentre la GPU esegue la composizione di blu.

     

5.  Successivamente, la GPU viene visualizzato in verde per l'app.
6.  Infine, il convertitore da digitale ad analogico (DAC) mostra i risultati della composizione DWM sul monitor nella sincronizzazione vsync successiva.

Dalla linea temporale è possibile immaginare la latenza delle statistiche presenti e il modo in cui possono verificarsi gli errori. Ad esempio, per visualizzare un glitch DWM per il colore verde visualizzato sullo schermo, si supponga di ampliare la casella verde/rossa in modo che il lato destro della casella verde/rossa corrisponda al lato destro della casella viola/rossa. In questo scenario, l'applicazione livello dati mostra due fotogrammi di blu e quindi il frame verde. È possibile vedere che questo problema si è verificato leggendo le statistiche presenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramento della presentazione con il modello di capovolgimento, rettangoli dirty e aree di scorrimento](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
