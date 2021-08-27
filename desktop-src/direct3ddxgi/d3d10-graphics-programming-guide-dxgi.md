---
description: In questo argomento sono contenute le sezioni seguenti.
ms.assetid: 0522ccbf-e754-470a-8199-004fcbaa927d
title: Panoramica di DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 604787a1b3f747b9d33cc04e249128aede7b7a3e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626137"
---
# <a name="dxgi-overview"></a>Panoramica di DXGI

Microsoft DirectX Graphic Infrastructure (DXGI) riconosce che alcune parti della grafica si evolvono più lentamente di altre. L'obiettivo principale di DXGI è gestire attività di basso livello che possono essere indipendenti dal runtime di grafica DirectX. DXGI fornisce un framework comune per i componenti grafici futuri; Il primo componente che sfrutta DXGI è Microsoft Direct3D 10.

Nelle versioni precedenti di Direct3D, nel runtime Direct3D sono state incluse attività di basso livello come l'enumerazione dei dispositivi hardware, la presentazione di fotogrammi sottoposti a rendering in un output, il controllo della gamma e la gestione di una transizione a schermo intero. Queste attività sono ora implementate in DXGI.

Lo scopo di DXGI è comunicare con il driver in modalità kernel e con l'hardware di sistema, come illustrato nel diagramma seguente.

![diagramma della comunicazione tra applicazioni, dxgi e driver e hardware](images/dxgi-dll.png)

Un'applicazione può accedere direttamente a DXGI o chiamare le API Direct3D in D3D11 \_ 1.h, D3D11.h, D3D10 1.h o D3D10.h, che gestisce automaticamente le comunicazioni con \_ DXGI. È possibile usare DXGI direttamente se l'applicazione deve enumerare i dispositivi o controllare la modalità di presentazione dei dati a un output.

In questo argomento sono contenute le sezioni seguenti.

-   [Enumerazione degli adattatori](#enumerating-adapters)
    -   [Nuove informazioni sull'enumerazione degli adapter per Windows 8](#new-info-about-enumerating-adapters-for-windows-8)
-   [Presentazione](#presentation)
    -   [Creare una catena di scambio](#create-a-swap-chain)
    -   [Cura e alimentazione della catena di scambio](#care-and-feeding-of-the-swap-chain)
    -   [Gestione del ridimensionamento della finestra](#handling-window-resizing)
    -   [Scelta dell'output e delle dimensioni DXGI](#choosing-the-dxgi-output-and-size)
    -   [Debug in modalità Full-Screen predefinita](#debugging-in-full-screen-mode)
    -   [Eliminazione di una catena di scambio](#destroying-a-swap-chain)
    -   [Uso di un monitoraggio ruotato](#using-a-rotated-monitor)
    -   [Cambio di modalità](#switching-modes)
    -   [Suggerimento sulle prestazioni a schermo intero](#full-screen-performance-tip)
    -   [Considerazioni sul multithreading](#multithread-considerations)
-   [Risposte DXGI da DLLMain](#dxgi-responses-from-dllmain)
-   [Modifiche di DXGI 1.1](#dxgi-11-changes)
-   [Modifiche di DXGI 1.2](#dxgi-12-changes)
-   [Argomenti correlati](#related-topics)

Per visualizzare i formati supportati dall'hardware Direct3D 11:

-   [Supporto del formato DXGI per l'hardware Direct3D Feature Level 12.1](hardware-support-for-direct3d-12-1-formats.md)
-   [Supporto del formato DXGI per l'hardware Direct3D Feature Level 12.0](hardware-support-for-direct3d-12-0-formats.md)
-   [Supporto del formato DXGI per l'hardware Direct3D Feature Level 11.1](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [Supporto del formato DXGI per l'hardware Direct3D Feature Level 11.0](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Supporto hardware per i formati Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
-   [Supporto hardware per i formati Direct3D 10.1](/previous-versions//cc627091(v=vs.85))
-   [Supporto hardware per i formati Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="enumerating-adapters"></a>Enumerazione degli adattatori

Un adattatore è un'astrazione dell'hardware e della funzionalità software del computer. In genere nel computer sono presenti molte schede. Alcuni dispositivi vengono implementati nell'hardware (come la scheda video) e altri nel software (come il rasterizzatore di riferimento Direct3D). Gli adattatori implementano le funzionalità usate da un'applicazione grafica. Il diagramma seguente illustra un sistema con un singolo computer, due schede (schede video) e tre monitor di output.

![Diagramma di un computer con due schede video e tre monitor](images/dxgi-terms.png)

Durante l'enumerazione di questi componenti hardware, DXGI crea un'interfaccia [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) per ogni output (o monitoraggio) e un'interfaccia [**IDXGIAdapter2**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgiadapter2) per ogni scheda video (anche se si tratta di una scheda video incorporata in una scheda madre). L'enumerazione viene eseguita usando una chiamata di interfaccia [**IDXGIFactory,**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) [**IDXGIFactory::EnumAdapters**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-enumadapters), per restituire un set di [**interfacce IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) che rappresentano l'hardware video.

DXGI 1.1 ha aggiunto [**l'interfaccia IDXGIFactory1.**](/windows/win32/api/DXGI/nn-dxgi-idxgifactory1) [**IDXGIFactory1::EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) restituisce un set di [**interfacce IDXGIAdapter1**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter1) che rappresenta l'hardware video.

Se si vogliono selezionare funzionalità hardware video specifiche quando si usano LE API Direct3D, è consigliabile chiamare in modo iterativo la funzione [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) con ogni handle di scheda e il possibile livello di funzionalità [hardware.](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) Questa funzione ha esito positivo se il livello di funzionalità è supportato dall'adapter specificato.

### <a name="new-info-about-enumerating-adapters-for-windows-8"></a>Nuove informazioni sull'enumerazione degli adapter per Windows 8

A partire Windows 8, è sempre presente un adattatore denominato "Microsoft Basic Render Driver". Questo adapter ha un VendorId di **0x1414** e un DeviceID di **0x8c**. Questa scheda ha anche il [**valore SOFTWARE DXGI \_ ADAPTER \_ \_ FLAG**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) impostato nel membro **Flags** della struttura [**DXGI \_ ADAPTER \_ DESC2.**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_adapter_desc2) Questo adattatore è un dispositivo di solo rendering senza output di visualizzazione. DXGI non restituisce mai [**DXGI \_ ERROR \_ DEVICE \_ REMOVED**](dxgi-error.md) per questa scheda.

Se il driver video di un computer non funziona o è disabilitato, l'adattatore primario **(NULL)** del computer potrebbe anche essere denominato "Driver di rendering Di base Microsoft". Ma questo adapter ha output e non ha il valore [**SOFTWARE DXGI \_ ADAPTER \_ FLAG \_**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) impostato. Il sistema operativo e le app usano questa scheda per impostazione predefinita. Se un driver video è installato o abilitato, le app possono ricevere [**DXGI \_ ERROR \_ DEVICE \_ REMOVED**](dxgi-error.md) per questa scheda e quindi devono enumerare nuovamente le schede.

Quando la scheda video principale di un computer è la "Scheda video Microsoft Basic"[(scheda WARP),](../direct3d11/overviews-direct3d-11-devices-create-warp.md) tale computer dispone anche di una seconda scheda. Questo secondo adattatore è il dispositivo di solo rendering senza output di visualizzazione e per il quale DXGI non restituisce mai [**DXGI \_ ERROR \_ DEVICE \_ REMOVED**](dxgi-error.md).

Se si vuole usare WARP per il rendering, il calcolo o altre attività a esecuzione lunga, è consigliabile usare il dispositivo solo rendering. È possibile ottenere un puntatore al dispositivo di solo rendering chiamando il [**metodo IDXGIFactory1::EnumAdapters1.**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) Il dispositivo di solo rendering viene creato anche quando si specifica [**D3D \_ DRIVER \_ TYPE \_ WARP**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_driver_type) nel parametro *DriverType* di [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) perché il dispositivo WARP usa anche l'adattatore WARP di solo rendering.

## <a name="presentation"></a>Presentazione

Il compito dell'applicazione è quello di eseguire il rendering dei fotogrammi e chiedere a DXGI di presentare tali fotogrammi nell'output. Se l'applicazione ha due buffer disponibili, può eseguire il rendering di un buffer durante la presentazione di un altro buffer. L'applicazione potrebbe richiedere più di due buffer a seconda del tempo necessario per eseguire il rendering di un frame o della frequenza di fotogrammi desiderata per la presentazione. Il set di buffer creati è detto catena di scambio, come illustrato di seguito.

![Illustrazione di una catena di scambio](images/dxgi-swap-chain.png)

-   [Creare una catena di scambio](#create-a-swap-chain)
-   [Cura e alimentazione della catena di scambio](#care-and-feeding-of-the-swap-chain)
-   [Gestione del ridimensionamento della finestra](#handling-window-resizing)
-   [Scelta dell'output e delle dimensioni DXGI](#choosing-the-dxgi-output-and-size)
-   [Debug in modalità Full-Screen predefinita](#debugging-in-full-screen-mode)
-   [Eliminazione di una catena di scambio](#destroying-a-swap-chain)
-   [Uso di un monitoraggio ruotato](#using-a-rotated-monitor)
-   [Cambio di modalità](#switching-modes)
-   [Suggerimento sulle prestazioni a schermo intero](#full-screen-performance-tip)
-   [Considerazioni sul multithreading](#multithread-considerations)

Una catena di scambio ha un front buffer e uno o più buffer back. Ogni applicazione crea una propria catena di scambio. Per ottimizzare la velocità di presentazione dei dati a un output, viene quasi sempre creata una catena di scambio nella memoria di un sottosistema di visualizzazione, come illustrato nella figura seguente.

![illustrazione di un sottosistema di visualizzazione](images/dxgi-adapter.png)

Il sottosistema di visualizzazione (che spesso è una scheda video ma può essere implementato in una scheda madre) contiene una GPU, un convertitore da digitale ad analogico (DAC) e memoria. La catena di scambio viene allocata all'interno di questa memoria per rendere la presentazione molto veloce. Il sottosistema di visualizzazione presenta i dati nel front buffer all'output.

Una catena di scambio è impostata per il disegno a schermo intero o in modalità finestra, eliminando la necessità di sapere se un output è a finestra o a schermo intero. Una catena di scambio in modalità schermo intero può ottimizzare le prestazioni passando alla risoluzione dello schermo.

### <a name="create-a-swap-chain"></a>Creare la catena di scambio

<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 10: Direct3D 10 è il primo componente grafico a usare DXGI. DXGI ha alcuni comportamenti diversi della catena di scambio.<br/>
<ul>
<li>In DXGI una catena di scambio è associata a una finestra quando viene creata la catena di scambio. Questa modifica migliora le prestazioni e consente di risparmiare memoria. Le versioni precedenti di Direct3D consentiva alla catena di scambio di modificare la finestra a cui è associata la catena di scambio.</li>
<li>In DXGI una catena di scambio è associata a un dispositivo di rendering al momento della creazione. L'oggetto dispositivo restituito da Direct3D create device functions implementa <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown"><strong>l'interfaccia IUnknown.</strong></a> È possibile chiamare <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> per eseguire una query per <a href="/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgidevice2"><strong>l'interfaccia IDXGIDevice2</strong></a> corrispondente del dispositivo. Una modifica al dispositivo di rendering richiede la ricreazione della catena di scambio.</li>
<li><p>In DXGI gli effetti di scambio disponibili sono DXGI_SWAP_EFFECT_DISCARD e DXGI_SWAP_EFFECT_SEQUENTIAL. A partire Windows 8 è disponibile DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL'effetto di scambio dei dati. La tabella seguente illustra il mapping tra l'effetto di scambio Direct3D 9 e DXGI definito. </p>
<table>
<thead>
<tr class="header">
<th>Effetto di scambio D3D9</th>
<th>Effetto di scambio DXGI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3DSWAPEFFECT_DISCARD</td>
<td>DXGI_SWAP_EFFECT_DISCARD</td>
</tr>
<tr class="even">
<td>D3DSWAPEFFECT_COPY</td>
<td>DXGI_SWAP_EFFECT_SEQUENTIAL con 1 buffer</td>
</tr>
<tr class="odd">
<td>D3DSWAPEFFECT_FLIP</td>
<td>DXGI_SWAP_EFFECT_SEQUENTIAL con 2 o più buffer</td>
</tr>
<tr class="even">
<td>D3DSWAPEFFECT_FLIPEX</td>
<td>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL con 2 o più buffer</td>
</tr>
</tbody>
</table>
<p></p>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



 

I buffer di una catena di scambio vengono creati a una dimensione specifica e in un particolare formato. L'applicazione specifica questi valori (oppure è possibile ereditare le dimensioni dalla finestra di destinazione) all'avvio e facoltativamente può modificarli quando le dimensioni della finestra cambiano in risposta agli eventi di input dell'utente o del programma.

Dopo aver creato la catena di scambio, è in genere necessario eseguirvi il rendering delle immagini. Ecco un frammento di codice che configura un contesto Direct3D per il rendering in una catena di scambio. Questo codice estrae un buffer dalla catena di scambio, crea una visualizzazione di destinazione di rendering da tale buffer e quindi lo imposta nel dispositivo:


```
ID3D11Resource * pBB;
ThrowFailure( pSwapChain->GetBuffer(0, __uuidof(pBB),    
  reinterpret_cast<void**>(&pBB)), "Couldn't get back buffer");
ID3D11RenderTargetView * pView;
ThrowFailure( pD3D11Device->CreateRenderTargetView(pBB, NULL, &pView), 
  "Couldn't create view" );
pD3D11DeviceContext->OMSetRenderTargets(1, &pView, 0);
        
```



Dopo che l'applicazione ha eseguito il rendering di un frame in un buffer della catena di scambio, chiamare [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). L'applicazione può quindi eseguire il rendering dell'immagine successiva.

### <a name="care-and-feeding-of-the-swap-chain"></a>Cura e alimentazione della catena di scambio

Dopo aver eseguito il rendering dell'immagine, chiamare [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) e passare a eseguire il rendering dell'immagine successiva. Questa è l'entità della responsabilità dell'utente.

Se in precedenza è stato chiamato [**IDXGIFactory::MakeWindowAssociation,**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation)l'utente può premere la combinazione di tasti Alt-Enter e DXGI esegue la transizione dell'applicazione tra la modalità finestra e la modalità schermo intero. **È consigliabile utilizzare IDXGIFactory::MakeWindowAssociation,** perché è fortemente desiderato un meccanismo di controllo standard per l'utente.

Anche se non è necessario scrivere altro codice di quello descritto, alcuni semplici passaggi possono rendere l'applicazione più reattiva. La considerazione più importante è il ridimensionamento dei buffer della catena di scambio in risposta al ridimensionamento della finestra di output. Naturalmente, la route migliore dell'applicazione è rispondere a WM SIZE e chiamare \_ [**IDXGISwapChain::ResizeBuffers,**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers)passando le dimensioni contenute nei parametri del messaggio. Questo comportamento ovviamente fa sì che l'applicazione risponda bene all'utente quando trascina i bordi della finestra, ma è anche esattamente ciò che consente una transizione uniforme a schermo intero. La finestra riceverà un messaggio WM SIZE ogni volta che si verifica una transizione di questo tipo e la chiamata a \_ **IDXGISwapChain::ResizeBuffers** è la possibilità della catena di scambio di riallocare lo spazio di archiviazione dei buffer per una presentazione ottimale. Questo è il motivo per cui l'applicazione deve rilasciare tutti i riferimenti presenti nei buffer esistenti prima di effettuare una **chiamata a IDXGISwapChain::ResizeBuffers**.

La mancata chiamata di [**IDXGISwapChain::ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) in risposta al passaggio alla modalità schermo intero (più naturalmente, in risposta a WM SIZE), può precludere l'ottimizzazione del capovolgimento, in cui DXGI può semplicemente scambiare quale buffer viene visualizzato, anziché copiare i dati di uno schermo \_ intero.

[**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) indica se la finestra di output è completamente occlusa tramite **STATO DXGI \_ \_ OCCLUDED.** In questo caso, è consigliabile attivare la modalità standby per l'applicazione (chiamando **IDXGISwapChain1::P resent1** con **DXGI \_ PRESENT \_ TEST)** perché le risorse usate per il rendering del frame vengono sprecate. **L'uso di DXGI \_ PRESENT \_ TEST** impedirà la presentazione di dati durante l'esecuzione del controllo dell'occlusione. Quando **IDXGISwapChain1::P resent1** restituisce S OK, è consigliabile uscire dalla modalità standby. Non usare il codice restituito per passare alla modalità standby, in quanto in questo modo la catena di scambio potrebbe non essere in grado di abbandonare la modalità schermo \_ intero.

Il runtime di Direct3D 11.1, disponibile a partire da Windows 8, fornisce una catena di scambio del modello flip, ovvero una catena di scambio con il valore [**\_ FLIP \_ \_ \_ SEQUENTIAL**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) DELL'EFFETTO SWAP DXGI impostato nel membro **SwapEffect** di [**DXGI \_ SWAP CHAIN \_ \_ DESC**](/windows/win32/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) o [**DXGI \_ SWAP CHAIN \_ \_ DESC1.**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) Quando si presentano frame a un output con una catena di scambio del modello di capovolgimento, DXGI disassocia il buffer nascosto da tutte le posizioni di stato della pipeline, ad esempio una destinazione di rendering unione output, che scrivono nel buffer nascosto 0. È quindi consigliabile chiamare [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets) immediatamente prima di eseguire il rendering nel buffer nascosto. Ad esempio, non chiamare **OMSetRenderTargets** e quindi eseguire operazioni di compute shader che non finisce per eseguire il rendering nella risorsa. Per altre informazioni sulle catene di scambio del modello di capovolgimento e sui relativi vantaggi, vedere [DXGI Flip Model (Modello di inversione DXGI).](dxgi-flip-model.md)

> [!NOTE]  
> In Direct3D 10 e Direct3D 11 non è necessario chiamare [**IDXGISwapChain::GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer) per recuperare il buffer nascosto 0 dopo aver chiamato [**IDXGISwapChain1::P resent1 perché**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) per praticità le identità dei buffer di back-buffer cambiano. Questo non avviene in Direct3D 12 e l'applicazione deve invece tenere traccia manualmente degli indici del buffer nascosto.

### <a name="handling-window-resizing"></a>Gestione del ridimensionamento delle finestre

È possibile usare il [**metodo IDXGISwapChain::ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) per gestire il ridimensionamento della finestra. Prima di chiamare **ResizeBuffers,** è necessario rilasciare tutti i riferimenti in sospeso ai buffer della catena di scambio. L'oggetto che in genere contiene un riferimento al buffer di una catena di scambio è una visualizzazione di destinazione di rendering.

Il codice di esempio seguente illustra come chiamare [**ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) dall'interno del gestore WindowProc per i messaggi \_ WM SIZE:


```
    case WM_SIZE:
        if (g_pSwapChain)
        {
            g_pd3dDeviceContext->OMSetRenderTargets(0, 0, 0);

            // Release all outstanding references to the swap chain's buffers.
            g_pRenderTargetView->Release();

            HRESULT hr;
            // Preserve the existing buffer count and format.
            // Automatically choose the width and height to match the client rect for HWNDs.
            hr = g_pSwapChain->ResizeBuffers(0, 0, 0, DXGI_FORMAT_UNKNOWN, 0);
                                            
            // Perform error handling here!

            // Get buffer and create a render-target-view.
            ID3D11Texture2D* pBuffer;
            hr = g_pSwapChain->GetBuffer(0, __uuidof( ID3D11Texture2D),
                                         (void**) &pBuffer );
            // Perform error handling here!

            hr = g_pd3dDevice->CreateRenderTargetView(pBuffer, NULL,
                                                     &g_pRenderTargetView);
            // Perform error handling here!
            pBuffer->Release();

            g_pd3dDeviceContext->OMSetRenderTargets(1, &g_pRenderTargetView, NULL );

            // Set up the viewport.
            D3D11_VIEWPORT vp;
            vp.Width = width;
            vp.Height = height;
            vp.MinDepth = 0.0f;
            vp.MaxDepth = 1.0f;
            vp.TopLeftX = 0;
            vp.TopLeftY = 0;
            g_pd3dDeviceContext->RSSetViewports( 1, &vp );
        }
        return 1;
```



### <a name="choosing-the-dxgi-output-and-size"></a>Scelta dell'output e delle dimensioni DXGI

Per impostazione predefinita, DXGI sceglie l'output che contiene la maggior parte dell'area client della finestra. Questa è l'unica opzione disponibile per DXGI quando passa a schermo intero in risposta a ALT+INVIO. Se l'applicazione sceglie di passare alla modalità schermo intero da sola, può chiamare [**IDXGISwapChain::SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) e passare un [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) esplicito (o **NULL,** se l'applicazione è contenta di consentire a DXGI di decidere).

Per ridimensionare l'output a schermo intero o in finestra, è consigliabile chiamare [**IDXGISwapChain::ResizeTarget,**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget)poiché questo metodo ridimensiona anche la finestra di destinazione. Poiché la finestra di destinazione viene ridimensionata, il sistema operativo invia **\_ WM SIZE** e il codice chiamerà naturalmente [**IDXGISwapChain::ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) in risposta. È quindi uno spreco di impegno ridimensionare i buffer e quindi ridimensionare successivamente la destinazione.

### <a name="debugging-in-full-screen-mode"></a>Debug in modalità schermo intero

Una catena di scambio DXGI cesa la modalità schermo intero solo quando assolutamente necessario. Ciò significa che è possibile eseguire il debug di un'applicazione a schermo intero usando più monitor, purché la finestra di debug non si sovrapponga alla finestra di destinazione della catena di scambio. In alternativa, è possibile impedire completamente il cambio di modalità non impostando il flag **DXGI \_ SWAP CHAIN FLAG ALLOW MODE \_ \_ \_ \_ \_ SWITCH.**

Se il cambio di modalità è consentito, una catena di scambio cederà la modalità schermo intero ogni volta che la finestra di output è occlusa da un'altra finestra. Il controllo dell'occlusione viene eseguito durante [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)o da un thread separato il cui scopo è controllare se l'applicazione non risponde (e non chiama **più IDXGISwapChain1::P resent1).** Per disabilitare la capacità del thread separato di causare un'opzione, impostare la chiave del Registro di sistema seguente su qualsiasi valore diverso da zero.

**HKCU \\ Software \\ Microsoft \\ DXGI \\ DisableFullscreenWatchdog**

### <a name="destroying-a-swap-chain"></a>Eliminazione di una catena di scambio

È possibile che non si rilasci una catena di scambio in modalità schermo intero perché in questo modo è possibile che si crei una contentione di thread (che causerà la generazione di un'eccezione non continuabile da parte di DXGI). Prima di rilasciare una catena di scambio, passare alla modalità finestra (usando [**IDXGISwapChain::SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)( **FALSE**, **NULL** )) e quindi chiamare [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

### <a name="using-a-rotated-monitor"></a>Uso di un monitor ruotato

Un'applicazione non deve preoccuparsi dell'orientamento del monitor. DXGI ruota un buffer della catena di scambio durante la presentazione, se necessario. Naturalmente, questa rotazione aggiuntiva può influire sulle prestazioni. Per ottenere prestazioni ottimali, eseguire le operazioni seguenti per eseguire la rotazione nell'applicazione:

-   Usare **DXGI \_ SWAP CHAIN FLAG \_ \_ \_ NONPREROTATED**. In questo modo si notifica a DXGI che l'applicazione produrrà un'immagine ruotata, ad esempio modificando la relativa matrice di proiezione. Un aspetto da notare è che questo flag è valido solo in modalità schermo intero.
-   Allocare ogni buffer della catena di scambio nelle dimensioni ruotate. Usare [**IDXGIOutput::GetDesc**](/windows/win32/api/DXGI/nf-dxgi-idxgioutput-getdesc) per ottenere questi valori, se necessario.

Eseguendo la rotazione nell'applicazione, DXGI eseguirà semplicemente una copia anziché una copia e una rotazione.

Il runtime di Direct3D 11.1, disponibile a partire da Windows 8, fornisce una catena di scambio del modello di capovolgimento, ovvero una catena di scambio con il valore [**\_ FLIP \_ \_ \_ SEQUENTIAL**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) DELL'EFFETTO SWAP DXGI impostato nel membro **SwapEffect** di [**DXGI \_ SWAP CHAIN \_ \_ DESC1.**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) Per ottimizzare le ottimizzazioni della presentazione disponibili con una catena di scambio del modello di capovolgimento, è consigliabile fare in modo che le applicazioni orientano il contenuto in modo che corrisponda all'output specifico in cui risiede il contenuto quando tale contenuto occupa completamente l'output. Per altre informazioni sulle catene di scambio del modello di capovolgimento e sui relativi vantaggi, vedere [DXGI Flip Model (Modello di inversione DXGI).](dxgi-flip-model.md)

### <a name="switching-modes"></a>Passaggio da una modalità all'altra

La catena di scambio DXGI potrebbe modificare la modalità di visualizzazione di un output quando si effettua una transizione a schermo intero. Per abilitare la modifica automatica della modalità di visualizzazione, è necessario specificare **DXGI \_ SWAP CHAIN FLAG ALLOW MODE \_ \_ \_ \_ \_ SWITCH** nella descrizione della catena di scambio. Se la modalità di visualizzazione cambia automaticamente, DXGI sceglierà la modalità più modesta (le dimensioni e la risoluzione non cambieranno, ma la profondità del colore potrebbe cambiare). Il ridimensionamento dei buffer della catena di scambio non causerà un cambio di modalità. La catena di scambio garantisce implicitamente che, se si sceglie un buffer nascosto che corrisponde esattamente a una modalità di visualizzazione supportata dall'output di destinazione, passa alla modalità di visualizzazione quando si passa alla modalità schermo intero nell'output. Di conseguenza, è possibile scegliere una modalità di visualizzazione scegliendo le dimensioni e il formato del buffer nascosto.

### <a name="full-screen-performance-tip"></a>Suggerimento per le prestazioni a schermo intero

Quando si chiama [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) in un'applicazione a schermo intero, la catena di scambio capovolge (anziché bliqui) il contenuto del buffer nascosto nel front buffer. A questo scopo è necessario che la catena di scambio sia stata creata usando una modalità di visualizzazione enumerata (specificata in [**DXGI \_ SWAP \_ CHAIN \_ DESC1).**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) Se non si riesce a enumerare le modalità di visualizzazione o si specifica erroneamente la modalità di visualizzazione nella descrizione, la catena di scambio potrebbe invece eseguire un trasferimento a blocchi di bit (bitblt). Il bitblt causa una copia di estensione aggiuntiva e un aumento dell'utilizzo della memoria video ed è difficile da rilevare. Per evitare questo problema, enumerare le modalità di visualizzazione e inizializzare correttamente la descrizione della catena di scambio prima di creare la catena di scambio. Ciò garantisce prestazioni massime quando si capovolge la modalità schermo intero ed evita il sovraccarico di memoria aggiuntivo.

### <a name="multithread-considerations"></a>Considerazioni sul multithreading

Quando si usa DXGI in un'applicazione con più thread, è necessario evitare di creare un deadlock, in cui due thread diversi sono in attesa l'uno sull'altro per il completamento. Questa situazione può verificarsi in due situazioni.

-   Il thread di rendering non è il thread message pump.
-   Il thread che esegue un'API DXGI non è lo stesso thread che ha creato la finestra.

Prestare attenzione a non avere mai il thread message pump in attesa sul thread di rendering quando si usano catene di scambio a schermo intero. Ad esempio, la chiamata [**a IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) (dal thread di rendering) può causare l'attesa del thread di rendering sul thread message-pump. Quando si verifica una modifica della modalità, questo scenario è possibile se **Present1** chiama ::SetWindowPos() o ::SetWindowStyle() e uno di questi metodi chiama ::SendMessage(). In questo scenario, se il thread message-pump ha una sezione critica che lo protegge o se il thread di rendering è bloccato, i due thread si bloccano.

Per altre informazioni sull'uso di DXGI con più thread, vedere [Multithreading e DXGI.](../direct3d11/overviews-direct3d-11-render-multi-thread-intro.md)

## <a name="dxgi-responses-from-dllmain"></a>Risposte DXGI da DLLMain

Poiché una funzione [**DllMain**](../dlls/dllmain.md) non può garantire l'ordine di caricamento e scaricamento delle DLL, è consigliabile che la funzione **DllMain** dell'app non chiami funzioni o metodi Direct3D o DXGI, incluse funzioni o metodi che creano o rilasciano oggetti. Se la funzione **DllMain** dell'app chiama un componente specifico, tale componente potrebbe chiamare un'altra DLL non presente nel sistema operativo, causando l'arresto anomalo del sistema operativo. Direct3D e DXGI potrebbero caricare un set di DLL, in genere un set di driver, che differisce da computer a computer. Pertanto, anche se l'app non si arresta in modo anomalo nei computer di sviluppo e test quando la relativa funzione **DllMain** chiama funzioni o metodi Direct3D o DXGI, potrebbe bloccarsi quando viene eseguita in un altro computer.

Per impedire la creazione di un'app che potrebbe causare l'arresto anomalo del sistema operativo, DXGI fornisce le risposte seguenti nelle situazioni specificate:

-   Se la funzione [**DllMain**](../dlls/dllmain.md) dell'app rilascia l'ultimo riferimento a una factory DXGI, DXGI genera un'eccezione.
-   Se la funzione [**DllMain**](../dlls/dllmain.md) dell'app crea una factory DXGI, DXGI restituisce un codice di errore.

## <a name="dxgi-11-changes"></a>Modifiche di DXGI 1.1

È stata aggiunta la funzionalità seguente in DXGI 1.1.

-   Supporto delle superfici condivise sincronizzate

    Le superfici condivise sincronizzate per Direct3D 10.1 e Direct3D 11 consentono una condivisione efficiente della superficie di lettura e scrittura tra più dispositivi Direct3D (è possibile condividere tra dispositivi Direct3D 10 e Direct3D 11). Vedere [**IDXGIKeyedMutex::AcquireSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-acquiresync) e [**IDXGIKeyedMutex::ReleaseSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-releasesync).

-   Supporto colori elevato

    Supporta il formato DXGI \_ FORMAT \_ R10G10B10 \_ XR \_ BIAS \_ A2 \_ UNORM.

-   [**IDXGIDevice1::SetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) e [ **IDXGIDevice1::GetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-getmaximumframelatency)
-   [**IDXGIFactory1::EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) enumera gli adattatori locali senza monitoraggi o output collegati, nonché gli adattatori con output collegati. Il primo adattatore restituito sarà l'adattatore locale in cui viene visualizzato il desktop primario.
-   Supporto del formato BGRA

    DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM e DXGI \_ FORMAT \_ B8G8R8A8A8 \_ UNORM \_ SRGB, vedere [**IDXGISurface1::GetDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-getdc) e [**IDXGISurface1::ReleaseDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-releasedc).

## <a name="dxgi-12-changes"></a>Modifiche di DXGI 1.2

È stata aggiunta la funzionalità seguente in DXGI 1.2.

-   Catena di scambio stereo
-   [Catena di scambio del modello flip](dxgi-flip-model.md)
-   Presentazione ottimizzata (scorrimento, rettangoli dirty e rotazione)
-   Miglioramento delle risorse condivise e della sincronizzazione
-   [Duplicazione del desktop](desktop-dup-api.md)
-   Uso ottimizzato della memoria video
-   Supporto per formati a 16 bit per pixel (bpp) (DXGI \_ \_ FORMAT B5G6R5 \_ UNORM, DXGI \_ FORMAT \_ B5G5R5A1 \_ UNORM, DXGI \_ FORMAT \_ B4G4R4A4 \_ UNORM)
-   Debug delle API

Per altre informazioni su DXGI 1.2, vedere [Miglioramenti di DXGI 1.2.](dxgi-1-2-improvements.md)

## <a name="related-topics"></a>Argomenti correlati

[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
