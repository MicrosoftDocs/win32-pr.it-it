---
description: In questo argomento sono contenute le sezioni seguenti.
ms.assetid: 0522ccbf-e754-470a-8199-004fcbaa927d
title: Panoramica di DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 324a5be26aade17385a6ab0b7d347015497a2a3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481085"
---
# <a name="dxgi-overview"></a>Panoramica di DXGI

Microsoft DirectX Graphics Infrastructure (DXGI) riconosce che alcune parti della grafica si evolvono più lentamente di altre. L'obiettivo principale di DXGI è quello di gestire attività di basso livello che possono essere indipendenti dal runtime di grafica DirectX. DXGI fornisce un Framework comune per i componenti grafici futuri. il primo componente che sfrutta i vantaggi di DXGI è Microsoft Direct3D 10.

Nelle versioni precedenti di Direct3D, le attività di basso livello, ad esempio l'enumerazione dei dispositivi hardware, la presentazione di frame di cui è stato eseguito il rendering in un output, il controllo di gamma e la gestione di una transizione a schermo intero erano incluse nel runtime Direct3D. Queste attività sono ora implementate in DXGI.

Lo scopo di DXGI è comunicare con il driver in modalità kernel e l'hardware di sistema, come illustrato nel diagramma seguente.

![diagramma della comunicazione tra applicazioni, DXGI, driver e hardware](images/dxgi-dll.png)

Un'applicazione può accedere direttamente a DXGI o chiamare le API Direct3D in D3D11 \_ 1. h, d3d11. h, D3D10 \_ 1. h o d3d10. h, che gestisce le comunicazioni con dxgi. Si consiglia di usare direttamente DXGI se l'applicazione deve enumerare i dispositivi o controllare la modalità di presentazione dei dati a un output.

In questo argomento sono contenute le sezioni seguenti.

-   [Enumerazione degli adapter](#enumerating-adapters)
    -   [Nuove informazioni sull'enumerazione degli adapter per Windows 8](#new-info-about-enumerating-adapters-for-windows-8)
-   [Presentazione](#presentation)
    -   [Creare una catena di scambio](#create-a-swap-chain)
    -   [Cura e alimentazione della catena di scambio](#care-and-feeding-of-the-swap-chain)
    -   [Gestione del ridimensionamento della finestra](#handling-window-resizing)
    -   [Scelta dell'output e delle dimensioni di DXGI](#choosing-the-dxgi-output-and-size)
    -   [Debug in modalità Full-Screen](#debugging-in-full-screen-mode)
    -   [Eliminazione di una catena di scambio](#destroying-a-swap-chain)
    -   [Uso di un monitoraggio ruotato](#using-a-rotated-monitor)
    -   [Modalità di cambio](#switching-modes)
    -   [Suggerimento per le prestazioni a schermo intero](#full-screen-performance-tip)
    -   [Considerazioni su multithread](#multithread-considerations)
-   [Risposte DXGI da DLLMain](#dxgi-responses-from-dllmain)
-   [DXGI 1,1 modifiche](#dxgi-11-changes)
-   [DXGI 1,2 modifiche](#dxgi-12-changes)
-   [Argomenti correlati](#related-topics)

Per vedere quali formati sono supportati dall'hardware di Direct3D 11:

-   [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 12,1](hardware-support-for-direct3d-12-1-formats.md)
-   [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 12,0](hardware-support-for-direct3d-12-0-formats.md)
-   [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 11,1](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [Supporto del formato DXGI per l'hardware a livello di funzionalità Direct3D 11,0](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Supporto hardware per i formati 10Level9 Direct3D](/previous-versions//ff471324(v=vs.85))
-   [Supporto hardware per formati Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
-   [Supporto hardware per i formati Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="enumerating-adapters"></a>Enumerazione degli adapter

Un adapter è un'astrazione dell'hardware e della funzionalità software del computer. Nel computer sono in genere presenti molti adapter. Alcuni dispositivi sono implementati nell'hardware (ad esempio la scheda video) e altri sono implementati nel software, ad esempio l'unità di rasterizzazione dei riferimenti Direct3D. Gli adapter implementano la funzionalità utilizzata da un'applicazione grafica. Il diagramma seguente mostra un sistema con un singolo computer, due schede (schede video) e tre monitor di output.

![diagramma di un computer con due schede video e tre monitor](images/dxgi-terms.png)

Quando si enumerano questi componenti hardware, DXGI crea un'interfaccia [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) per ciascun output (o monitoraggio) e un'interfaccia [**IDXGIAdapter2**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgiadapter2) per ogni scheda video (anche se si tratta di una scheda video incorporata in una scheda madre). L'enumerazione viene eseguita utilizzando una chiamata di interfaccia [**IDXGIFactory**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) , [**IDXGIFactory:: EnumAdapters**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-enumadapters), per restituire un set di interfacce [**IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) che rappresentano l'hardware del video.

DXGI 1,1 ha aggiunto l'interfaccia [**IDXGIFactory1**](/windows/win32/api/DXGI/nn-dxgi-idxgifactory1) . [**IDXGIFactory1:: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) restituisce un set di interfacce [**IDXGIAdapter1**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter1) che rappresenta l'hardware del video.

Se si desidera selezionare funzionalità hardware video specifiche quando si utilizzano le API Direct3D, è consigliabile chiamare in modo iterativo la funzione [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) con ogni handle di adapter e il possibile [livello di funzionalità](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)dell'hardware. Questa funzione ha esito positivo se il livello di funzionalità è supportato dall'adapter specificato.

### <a name="new-info-about-enumerating-adapters-for-windows-8"></a>Nuove informazioni sull'enumerazione degli adapter per Windows 8

A partire da Windows 8, un adapter denominato "Microsoft Basic render driver" è sempre presente. Questa scheda ha un VendorId di **0x1414** e un DeviceID di **0x8c**. Questa scheda dispone anche del [**valore \_ \_ \_ software del flag dell'adattatore DXGI**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) impostato nel membro **Flags** della relativa struttura [**\_ \_ DESC2 dell'adapter DXGI**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_adapter_desc2) . Questo adapter è un dispositivo solo di rendering senza output di visualizzazione. DXGI non restituisce mai il [**\_ dispositivo DXGI Error \_ \_ rimosso**](dxgi-error.md) per questo adapter.

Se il driver di visualizzazione di un computer non funziona o è disabilitato, è possibile chevenga chiamato anche il "driver di rendering di base Microsoft". Tuttavia, per questo adapter sono presenti output e non è stato impostato il valore di DXGI per l' [**\_ adapter \_ \_**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) . Per impostazione predefinita, il sistema operativo e le app utilizzano questa scheda. Se è installato o abilitato un driver di visualizzazione, le app possono ricevere il [**\_ dispositivo di errore DXGI \_ \_ rimosso**](dxgi-error.md) per questa scheda e quindi rienumerare nuovamente gli adapter.

Quando la scheda di visualizzazione principale di un computer è "Microsoft Basic Display Adapter" (scheda[Warp](../direct3d11/overviews-direct3d-11-devices-create-warp.md) ), il computer dispone anche di un secondo adapter. Questa seconda scheda è il dispositivo solo di rendering senza output di visualizzazione e per il quale DXGI non restituisce mai il [**\_ dispositivo DXGI Error \_ \_ rimosso**](dxgi-error.md).

Se si vuole usare WARP per il rendering, il calcolo o altre attività a esecuzione prolungata, si consiglia di usare il dispositivo solo di rendering. È possibile ottenere un puntatore al dispositivo di sola rendering chiamando il metodo [**IDXGIFactory1:: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) . Si crea anche il dispositivo di sola rendering quando si specifica [**il \_ \_ tipo di \_ driver D3D**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_driver_type) nel parametro *DRIVERTYPE* di [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) perché il dispositivo Warp usa anche l'adattatore di distorsione di sola rendering.

## <a name="presentation"></a>Presentazione

Il processo dell'applicazione consiste nel eseguire il rendering dei frame e richiedere a DXGI di presentare tali frame all'output. Se l'applicazione dispone di due buffer disponibili, è possibile eseguire il rendering di un buffer e presentarne un altro. L'applicazione potrebbe richiedere più di due buffer a seconda del tempo necessario per eseguire il rendering di un frame o della frequenza dei fotogrammi desiderata per la presentazione. Il set di buffer creati è denominato catena di scambio, come illustrato di seguito.

![illustrazione di una catena di scambio](images/dxgi-swap-chain.png)

-   [Creare una catena di scambio](#create-a-swap-chain)
-   [Cura e alimentazione della catena di scambio](#care-and-feeding-of-the-swap-chain)
-   [Gestione del ridimensionamento della finestra](#handling-window-resizing)
-   [Scelta dell'output e delle dimensioni di DXGI](#choosing-the-dxgi-output-and-size)
-   [Debug in modalità Full-Screen](#debugging-in-full-screen-mode)
-   [Eliminazione di una catena di scambio](#destroying-a-swap-chain)
-   [Uso di un monitoraggio ruotato](#using-a-rotated-monitor)
-   [Modalità di cambio](#switching-modes)
-   [Suggerimento per le prestazioni a schermo intero](#full-screen-performance-tip)
-   [Considerazioni su multithread](#multithread-considerations)

Una catena di scambio ha un buffer anteriore e uno o più buffer back. Ogni applicazione crea la propria catena di scambio. Per massimizzare la velocità della presentazione dei dati a un output, viene quasi sempre creata una catena di scambio nella memoria di un sottosistema di visualizzazione, come illustrato nella figura seguente.

![illustrazione di un sottosistema di visualizzazione](images/dxgi-adapter.png)

Il sottosistema di visualizzazione (che è spesso una scheda video ma potrebbe essere implementato in una scheda madre) contiene una GPU, un convertitore da digitale a analogico (DAC) e memoria. La catena di scambio viene allocata in questa memoria per rendere la presentazione molto rapida. Il sottosistema di visualizzazione presenta i dati nel buffer anteriore all'output.

Una catena di scambio è configurata per essere tracciata in modalità a schermo intero o a finestra. in questo modo si elimina la necessità di sapere se un output è a finestra o a schermo intero. Una catena di scambio in modalità a schermo intero può ottimizzare le prestazioni cambiando la risoluzione dello schermo.

### <a name="create-a-swap-chain"></a>Creare la catena di scambio

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 10: Direct3D 10 è il primo componente grafico per l'uso di DXGI. DXGI presenta diversi comportamenti della catena di scambio.<br/>
<ul>
<li>In DXGI una catena di scambio è associata a una finestra al momento della creazione della catena di scambio. Questa modifica consente di migliorare le prestazioni e di risparmiare memoria. Le versioni precedenti di Direct3D consentivano alla catena di scambio di modificare la finestra a cui è associata la catena di scambio.</li>
<li>In DXGI una catena di scambio è associata a un dispositivo di rendering al momento della creazione. L'oggetto dispositivo che la funzione di creazione di un dispositivo Direct3D restituisce implementa l'interfaccia <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> . È possibile chiamare <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> per eseguire una query per l'interfaccia <a href="/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgidevice2"><strong>IDXGIDevice2</strong></a> corrispondente del dispositivo. Una modifica al dispositivo di rendering richiede la ricreazione della catena di scambio.</li>
<li><p>In DXGI, gli effetti di scambio disponibili sono DXGI_SWAP_EFFECT_DISCARD e DXGI_SWAP_EFFECT_SEQUENTIAL. A partire da Windows 8, è disponibile anche l'effetto di scambio DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL. Nella tabella seguente viene illustrato un mapping di Direct3D 9 a DXGI. </p>
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



 

I buffer di una catena di scambio vengono creati in una determinata dimensione e in un particolare formato. L'applicazione specifica questi valori (oppure è possibile ereditare le dimensioni dalla finestra di destinazione) all'avvio e può quindi modificarli eventualmente quando le dimensioni della finestra cambiano in risposta a eventi di input o programma dell'utente.

Dopo aver creato la catena di scambio, in genere si desidera eseguire il rendering delle immagini. Ecco un frammento di codice che configura un contesto Direct3D per il rendering in una catena di scambio. Questo codice estrae un buffer dalla catena di scambio, crea una visualizzazione della destinazione di rendering da tale buffer, quindi la imposta sul dispositivo:


```
ID3D11Resource * pBB;
ThrowFailure( pSwapChain->GetBuffer(0, __uuidof(pBB),    
  reinterpret_cast<void**>(&pBB)), "Couldn't get back buffer");
ID3D11RenderTargetView * pView;
ThrowFailure( pD3D11Device->CreateRenderTargetView(pBB, NULL, &pView), 
  "Couldn't create view" );
pD3D11DeviceContext->OMSetRenderTargets(1, &pView, 0);
        
```



Quando l'applicazione esegue il rendering di un frame in un buffer a catena di scambio, chiamare [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). L'applicazione può quindi eseguire il rendering dell'immagine successiva.

### <a name="care-and-feeding-of-the-swap-chain"></a>Cura e alimentazione della catena di scambio

Dopo aver eseguito il rendering dell'immagine, chiamare [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) e passare il rendering dell'immagine successiva. Questo è l'ambito della responsabilità dell'utente.

Se in precedenza è stato chiamato [**IDXGIFactory:: MakeWindowAssociation**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation), l'utente può premere la combinazione di tasti Alt-Enter e DXGI eseguirà la transizione dell'applicazione tra la modalità a schermo intero e a finestra. È consigliabile utilizzare **IDXGIFactory:: MakeWindowAssociation** , perché un meccanismo di controllo standard per l'utente è fortemente auspicabile.

Sebbene non sia necessario scrivere altro codice rispetto a quanto descritto, pochi semplici passaggi possono rendere l'applicazione più reattiva. La considerazione più importante è il ridimensionamento dei buffer della catena di scambio in risposta al ridimensionamento della finestra di output. Naturalmente, la migliore route dell'applicazione consiste nel rispondere alle dimensioni di WM \_ e chiamare [**IDXGISwapChain:: ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers), passando le dimensioni contenute nei parametri del messaggio. Questo comportamento rende ovviamente la risposta dell'applicazione all'utente quando trascina i bordi della finestra, ma è anche ciò che consente una transizione senza problemi a schermo intero. La finestra riceverà un \_ messaggio di dimensioni WM ogni volta che si verifica tale transizione e la chiamata a **IDXGISwapChain:: ResizeBuffers** è la possibilità della catena di scambio di riallocare l'archiviazione dei buffer per una presentazione ottimale. Questo è il motivo per cui l'applicazione è necessaria per rilasciare tutti i riferimenti presenti nei buffer esistenti prima di chiamare **IDXGISwapChain:: ResizeBuffers**.

Non è possibile chiamare [**IDXGISwapChain:: ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) in risposta al passare alla modalità a schermo intero (la maggior parte dei casi, in risposta a \_ dimensioni WM), può impedire l'ottimizzazione del capovolgimento, in cui DXGI può semplicemente scambiare il buffer visualizzato, anziché copiare i dati di un intero schermo.

[**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) indicherà se la finestra di output è completamente nascosto tramite **\_ lo stato \_ DXGI**. Quando si verifica questo problema, si consiglia di passare alla modalità standby (chiamando **IDXGISwapChain1::P resent1** con **DXGI \_ present \_ test**) poiché le risorse usate per eseguire il rendering del frame vengono sprecate. Se si usa DXGI, il **\_ \_ test presente** impedirà la presentazione di tutti i dati durante l'esecuzione del controllo dell'occlusione. Quando **IDXGISwapChain1::P resent1** restituisce S \_ OK, è necessario uscire dalla modalità standby. non usare il codice restituito per passare alla modalità standby. in questo modo, è possibile lasciare che la catena di scambio non possa rinunciare alla modalità a schermo intero.

Il runtime Direct3D 11,1, disponibile a partire da Windows 8, fornisce una catena di scambio Flip-Model, ovvero una catena di scambio con il valore [**\_ \_ \_ \_ sequenziale DXGI swap effect Flip**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) impostato nel membro **SwapEffect** di [**DXGI \_ swap \_ Chain \_ desc**](/windows/win32/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) o [**DXGI \_ swap \_ Chain \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)). Quando si visualizzano i frame in un output con una catena di scambio Flip-Model, DXGI Annulla il binding del buffer nascosto da tutte le posizioni dello stato della pipeline, ad esempio una destinazione di rendering dell'Unione di output, che scrivono nel buffer di back 0. Pertanto, si consiglia di chiamare [**sul ID3D11DeviceContext:: OMSetRenderTargets**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets) immediatamente prima di eseguire il rendering nel buffer nascosto. Ad esempio, non chiamare **OMSetRenderTargets** e quindi eseguire il lavoro compute shader che non termina il rendering nella risorsa. Per altre informazioni sulle catene di scambio flip-model e sui relativi vantaggi, vedere [DXGI flip model](dxgi-flip-model.md).

> [!NOTE]  
> In Direct3D 10 e Direct3D 11 non è necessario chiamare [**IDXGISwapChain:: GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer) per recuperare il buffer di back 0 dopo aver chiamato [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) perché per praticità le identità dei buffer indietro cambiano. Questa operazione non si verifica in Direct3D 12 e l'applicazione deve invece tenere traccia manualmente degli indici del buffer.

### <a name="handling-window-resizing"></a>Gestione del ridimensionamento della finestra

Per gestire il ridimensionamento delle finestre, è possibile usare il metodo [**IDXGISwapChain:: ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) . Prima di chiamare **ResizeBuffers**, è necessario rilasciare tutti i riferimenti in attesa ai buffer della catena di scambio. L'oggetto che in genere include un riferimento a un buffer della catena di scambio è una visualizzazione di destinazione di rendering.

Il codice di esempio seguente mostra come chiamare [**ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) dall'interno del gestore WindowProc per \_ i messaggi di dimensioni WM:


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



### <a name="choosing-the-dxgi-output-and-size"></a>Scelta dell'output e delle dimensioni di DXGI

Per impostazione predefinita, DXGI sceglie l'output che contiene la maggior parte dell'area client della finestra. Questa è l'unica opzione disponibile per DXGI quando viene visualizzata a schermo intero in risposta a ALT-INVIO. Se l'applicazione sceglie di passare alla modalità a schermo intero da solo, può chiamare [**IDXGISwapChain:: SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) e passare un [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) esplicito (o **null**, se l'applicazione è lieta di consentire a DXGI di decidere).

Per ridimensionare l'output a schermo intero o a finestra, si consiglia di chiamare [**IDXGISwapChain:: ResizeTarget**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget), poiché questo metodo ridimensiona anche la finestra di destinazione. Poiché la finestra di destinazione viene ridimensionata, il sistema operativo invia **le \_ dimensioni di WM** e il codice chiamerà naturalmente [**IDXGISwapChain:: ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) in risposta. Si tratta pertanto di uno spreco di sforzo per ridimensionare i buffer e successivamente ridimensionare la destinazione.

### <a name="debugging-in-full-screen-mode"></a>Debug in modalità schermo intero

Una catena di scambio DXGI abbandona la modalità schermo intero solo quando è strettamente necessario. Ciò significa che è possibile eseguire il debug di un'applicazione a schermo intero utilizzando più monitoraggi, purché la finestra di debug non si sovrappongano alla finestra di destinazione della catena di scambio. In alternativa, è possibile evitare completamente il cambio di modalità, non impostando il flag di opzione per la **modalità di scambio DXGI del \_ flag della \_ catena \_ \_ \_ \_ di scambio** .

Se il cambio di modalità è consentito, una catena di scambio abbandonerà la modalità a schermo intero ogni volta che la finestra di output è bloccato da un'altra finestra. Il controllo dell'occlusione viene eseguito durante [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)oppure da un thread separato il cui scopo è quello di controllare se l'applicazione non risponde e non chiama più **IDXGISwapChain1::P resent1**. Per disabilitare la possibilità che il thread separato provochi un'opzione, impostare la seguente chiave del registro di sistema su un valore diverso da zero.

**HKCU \\ software \\ Microsoft \\ DXGI \\ DisableFullscreenWatchdog**

### <a name="destroying-a-swap-chain"></a>Eliminazione di una catena di scambio

Non è possibile rilasciare una catena di scambio in modalità schermo intero perché questa operazione può creare una contesa di thread, che causerà la generazione di un'eccezione non continuabile da DXGI. Prima di rilasciare una catena di scambio, passare prima alla modalità finestra (usando [**IDXGISwapChain:: SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)( **false**, **null** )) e quindi chiamare [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

### <a name="using-a-rotated-monitor"></a>Uso di un monitoraggio ruotato

Non è necessario che un'applicazione si preoccupi dell'orientamento del monitoraggio, DXGI ruoterà un buffer a catena di scambio durante la presentazione, se necessario. Naturalmente, questa rotazione aggiuntiva può avere un effetto sulle prestazioni. Per ottenere prestazioni ottimali, si prenda in considerazione la rotazione nell'applicazione eseguendo le operazioni seguenti:

-   Usare il **\_ \_ flag Chain DXGI \_ swap \_ NONPREROTATED**. Questo notifica a DXGI che l'applicazione produrrà un'immagine ruotata, ad esempio modificando la matrice di proiezione. Un aspetto da notare è che questo flag è valido solo in modalità schermo intero.
-   Allocare ogni buffer della catena di scambio nelle dimensioni ruotate. Usare [**IDXGIOutput:: getdesc**](/windows/win32/api/DXGI/nf-dxgi-idxgioutput-getdesc) per ottenere questi valori, se necessario.

Eseguendo la rotazione nell'applicazione, DXGI eseguirà semplicemente una copia anziché una copia e una rotazione.

Il runtime Direct3D 11,1, disponibile a partire da Windows 8, fornisce una catena di scambio Flip-Model, ovvero una catena di scambio con il valore [**\_ \_ \_ \_ sequenziale DXGI swap effect Flip**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) impostato nel membro **SwapEffect** di [**DXGI \_ swap \_ Chain \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)). Per ottimizzare le ottimizzazioni della presentazione disponibili con una catena di scambio Flip-Model, è consigliabile fare in modo che le applicazioni orientino il contenuto in modo che corrisponda all'output specifico in cui si trova il contenuto quando il contenuto occupa completamente l'output. Per altre informazioni sulle catene di scambio flip-model e sui relativi vantaggi, vedere [DXGI flip model](dxgi-flip-model.md).

### <a name="switching-modes"></a>Modalità di cambio

La catena di scambio DXGI potrebbe modificare la modalità di visualizzazione di un output quando si esegue una transizione a schermo intero. Per abilitare la modifica della modalità di visualizzazione automatica, è necessario specificare l' **\_ \_ \_ \_ \_ \_ opzione di modalità Consenti flag catena di scambio DXGI** nella descrizione della catena di scambio. Se la modalità di visualizzazione cambia automaticamente, DXGI sceglierà la modalità più modesta (le dimensioni e la risoluzione non verranno modificate, ma la profondità del colore potrebbe essere). Il ridimensionamento dei buffer della catena di scambio non comporta l'attivazione di un commutatore di modalità. La catena di scambio crea una promessa implicita che se si sceglie un buffer nascosto che corrisponde esattamente a una modalità di visualizzazione supportata dall'output di destinazione, si passerà a tale modalità di visualizzazione quando si entra in modalità schermo intero su tale output. Di conseguenza, è possibile scegliere una modalità di visualizzazione scegliendo il formato e le dimensioni del buffer.

### <a name="full-screen-performance-tip"></a>Suggerimento per le prestazioni a schermo intero

Quando si chiama [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) su un'applicazione a schermo intero, la catena di scambio capovolge (in contrapposizione a Blits) il contenuto del buffer nascosto al buffer anteriore. A questo scopo, è necessario che la catena di scambio sia stata creata usando una modalità di visualizzazione enumerata (specificata in [**DXGI \_ swap \_ Chain \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)). Se non si riesce a enumerare le modalità di visualizzazione o si specifica erroneamente la modalità di visualizzazione nella descrizione, la catena di scambio può invece eseguire un trasferimento a blocchi di bit (BitBlt). Il BitBlt causa una copia di estensione aggiuntiva, oltre ad aumentare l'utilizzo della memoria video ed è difficile da rilevare. Per evitare questo problema, enumerare le modalità di visualizzazione e inizializzare correttamente la descrizione della catena di scambio prima di creare la catena di scambio. Questo garantisce prestazioni massime quando si esegue il capovolgimento in modalità schermo intero ed evita l'overhead aggiuntivo della memoria.

### <a name="multithread-considerations"></a>Considerazioni su multithread

Quando si usa DXGI in un'applicazione con più thread, è necessario prestare attenzione a evitare la creazione di un deadlock, in cui due thread diversi sono in attesa di essere completati. Questo problema può verificarsi in due situazioni.

-   Il thread di rendering non è il thread della pompa di messaggi.
-   Il thread che esegue un'API DXGI non è lo stesso thread che ha creato la finestra.

Quando si usano le catene di scambio a schermo intero, prestare attenzione a non avere mai un thread di message-pump in attesa sul thread di rendering. Ad esempio, la chiamata a [**IDXGISwapChain1::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) (dal thread di rendering) può provocare l'attesa del thread di rendering sul thread della pompa di messaggi. Quando si verifica una modifica della modalità, questo scenario è possibile se **Present1** chiama:: SetWindowPos () o:: SetWindowStyle () e uno di questi metodi chiama:: SendMessage (). In questo scenario, se il thread della pompa di messaggi presenta una sezione critica che lo sorveglia o se il thread di rendering è bloccato, i due thread risulteranno deadlock.

Per altre informazioni sull'uso di DXGI con più thread, vedere [multithreading e DXGI](../direct3d11/overviews-direct3d-11-render-multi-thread-intro.md).

## <a name="dxgi-responses-from-dllmain"></a>Risposte DXGI da DLLMain

Poiché una funzione [**DllMain**](../dlls/dllmain.md) non può garantire l'ordine in cui carica e Scarica le dll, è consigliabile che la funzione **DllMain** dell'app non chiami le funzioni o i metodi Direct3D o DXGI, incluse le funzioni o i metodi che creano o rilasciano oggetti. Se la funzione **DllMain** dell'app chiama un particolare componente, il componente potrebbe chiamare un'altra dll non presente nel sistema operativo, causando l'arresto anomalo del sistema operativo. Direct3D e DXGI possono caricare un set di dll, in genere un set di driver, che differisce da computer a computer. Pertanto, anche se l'app non si arresta in modo anomalo nei computer di sviluppo e di test quando la funzione **DllMain** chiama funzioni o metodi Direct3D o DXGI, è possibile che si verifichi un arresto anomalo quando viene eseguito in un altro computer.

Per evitare di creare un'app che potrebbe causare l'arresto anomalo del sistema operativo, DXGI fornisce le risposte seguenti nelle situazioni specificate:

-   Se la funzione [**DllMain**](../dlls/dllmain.md) dell'app rilascia l'ultimo riferimento a una factory DXGI, DXGI genera un'eccezione.
-   Se la funzione [**DllMain**](../dlls/dllmain.md) dell'app crea una factory DXGI, DXGI restituisce un codice di errore.

## <a name="dxgi-11-changes"></a>DXGI 1,1 modifiche

Sono state aggiunte le funzionalità seguenti in DXGI 1,1.

-   Supporto delle superfici condivise sincronizzate

    Le aree condivise sincronizzate per Direct3D 10,1 e Direct3D 11 consentono una condivisione efficace della superficie di lettura e scrittura tra più dispositivi Direct3D (la condivisione tra i dispositivi Direct3D 10 e Direct3D 11 è possibile). Vedere [**IDXGIKeyedMutex:: AcquireSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-acquiresync) e [**IDXGIKeyedMutex:: ReleaseSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-releasesync).

-   Supporto per colori elevati

    Supporta il formato \_ DXGI \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM.

-   [**IDXGIDevice1:: SetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) e [ **IDXGIDevice1:: GetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-getmaximumframelatency)
-   [**IDXGIFactory1:: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) enumera gli adapter locali senza i monitoraggi o gli output collegati, nonché gli adapter con gli output collegati. Il primo Adapter restituito sarà l'adapter locale in cui viene visualizzato il desktop primario.
-   Supporto del formato BGRA

    DXGI \_ Format \_ B8G8R8A8 \_ UNORM e DXGI \_ Format \_ B8G8R8A8 \_ UNORM \_ sRGB, vedere [**IDXGISurface1:: GetDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-getdc) e [**IDXGISurface1:: ReleaseDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-releasedc).

## <a name="dxgi-12-changes"></a>DXGI 1,2 modifiche

Sono state aggiunte le funzionalità seguenti in DXGI 1,2.

-   Catena di scambio stereo
-   [Inverti catena di scambio del modello](dxgi-flip-model.md)
-   Presentazione ottimizzata (scorrimento, rettangoli Dirty e rotazione)
-   Miglioramento delle risorse condivise e della sincronizzazione
-   [Duplicazione del desktop](desktop-dup-api.md)
-   Utilizzo ottimizzato della memoria video
-   Supporto per formati a 16 bit per pixel (BPP) ( \_ formato DXGI \_ B5G6R5 \_ UNORM, \_ formato DXGI B5G5R5A1 UNORM \_ \_ , \_ formato \_ DXGI \_ B4G4R4A4 UNORM)
-   API di debug

Per altre informazioni su DXGI 1,2, vedere [miglioramenti di DXGI 1,2](dxgi-1-2-improvements.md).

## <a name="related-topics"></a>Argomenti correlati

[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
