---
description: Uso della modalità senza finestra
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Uso della modalità senza finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5189fb52932a328493baec9a79ccd6598a9a0659c198ee3ce3d4d157574a63c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119271251"
---
# <a name="using-windowless-mode"></a>Uso della modalità senza finestra

Sia il filtro del renderer di combinazione video [7](video-mixing-renderer-filter-7.md) (VMR-7) che il filtro del renderer di combinazione video [9](video-mixing-renderer-filter-9.md) (VMR-9) supportano la modalità senza *finestra,* che rappresenta un miglioramento significativo rispetto all'interfaccia [**IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow) Questo argomento descrive le differenze tra la modalità senza finestra e la modalità finestra e come usare la modalità senza finestra.

Per mantenere la compatibilità con le versioni precedenti delle applicazioni esistenti, per impostazione predefinita la vmr è in modalità finestra. In modalità finestra il renderer crea la propria finestra per visualizzare il video. In genere l'applicazione imposta la finestra video come figlio della finestra dell'applicazione. L'esistenza di una finestra video separata causa tuttavia alcuni problemi:

-   L'aspetto più importante è che potrebbero verificarsi deadlock se i messaggi della finestra vengono inviati tra thread.
-   Filter Graph Manager deve inoltrare determinati messaggi della finestra, ad esempio WM \_ PAINT, al renderer video. L'applicazione deve usare l'implementazione di [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (e non del renderer video) di Filter Graph Manager, in modo che filter Graph Manager mantenga lo stato interno corretto.
-   Per ricevere gli eventi del mouse o della tastiera dalla finestra video, l'applicazione deve impostare uno svuotamento dei *messaggi,* facendo in modo che la finestra video inoltra questi messaggi all'applicazione.
-   Per evitare problemi di ritaglio, la finestra video deve avere gli stili di finestra destra.

La modalità senza finestra evita questi problemi facendo in modo che la macchina virtuale venga disegnata direttamente nell'area client della finestra dell'applicazione, usando DirectDraw per ritagliare il rettangolo video. La modalità senza finestra riduce significativamente la probabilità di deadlock. Inoltre, l'applicazione non deve impostare la finestra proprietaria o gli stili della finestra. Infatti, quando la macchina virtuale è in modalità senza finestra, non espone nemmeno [**l'interfaccia IVideoWindow,**](/windows/desktop/api/Control/nn-control-ivideowindow) che non è più necessaria.

Per usare la modalità senza finestra, è necessario configurare in modo esplicito la macchina virtuale. Tuttavia, si scoprirà che è più flessibile e più facile da usare rispetto alla modalità finestra.

Il filtro VMR-7 e il filtro VMR-9 espongono interfacce diverse, ma i passaggi sono equivalenti per ognuna.

## <a name="configure-the-vmr-for-windowless-mode"></a>Configurare la macchina virtuale per la modalità senza finestra

Per eseguire l'override del comportamento predefinito della macchina virtuale, configurare la macchina virtuale prima di compilare il grafico dei filtri:

**VMR-7**

1.  Creare la gestione Graph filtro.
2.  Creare vmr-7 e aggiungerlo al grafico dei filtri.
3.  Chiamare [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) in VMR-7 con il flag **VMRMode \_ senza** finestra.
4.  Eseguire una query su VMR-7 per [**l'interfaccia IVMRWindowlessControl.**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol)
5.  Chiamare [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) in VMR-7. Specificare un handle per la finestra in cui deve essere visualizzato il video.

**VMR-9**

1.  Creare la gestione Graph filtro.
2.  Creare vmr-9 e aggiungerlo al grafico dei filtri.
3.  Chiamare [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) in VMR-9 con il flag **VMR9Mode \_ senza** finestra.
4.  Eseguire una query su VMR-9 per [**l'interfaccia IVMRWindowlessControl9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9)
5.  Chiamare [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) in VMR-9. Specificare un handle per la finestra in cui deve essere visualizzato il video.

Compilare ora il resto del grafico di filtro chiamando [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o altri metodi di compilazione del grafo. Il filtro Graph Manager usa automaticamente l'istanza della macchina virtuale aggiunta al grafico. Per informazioni dettagliate sul motivo per cui ciò si verifica, [vedere Intelligent Connessione](intelligent-connect.md).

Il codice seguente illustra una funzione helper che crea VMR-7, la aggiunge al grafo e configura la modalità senza finestra.


```C++
HRESULT InitWindowlessVMR( 
    HWND hwndApp,                  // Window to hold the video. 
    IGraphBuilder* pGraph,         // Pointer to the Filter Graph Manager. 
    IVMRWindowlessControl** ppWc   // Receives a pointer to the VMR.
    ) 
{ 
    if (!pGraph || !ppWc) 
    {
        return E_POINTER;
    }
    IBaseFilter* pVmr = NULL; 
    IVMRWindowlessControl* pWc = NULL; 
    // Create the VMR. 
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL, 
        CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr); 
    if (FAILED(hr))
    {
        return hr;
    }
    
    // Add the VMR to the filter graph.
    hr = pGraph->AddFilter(pVmr, L"Video Mixing Renderer"); 
    if (FAILED(hr)) 
    {
        pVmr->Release();
        return hr;
    }
    // Set the rendering mode.  
    IVMRFilterConfig* pConfig; 
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig); 
    if (SUCCEEDED(hr)) 
    { 
        hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
        pConfig->Release(); 
    }
    if (SUCCEEDED(hr))
    {
        // Set the window. 
        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if( SUCCEEDED(hr)) 
        { 
            hr = pWc->SetVideoClippingWindow(hwndApp); 
            if (SUCCEEDED(hr))
            {
                *ppWc = pWc; // Return this as an AddRef'd pointer. 
            }
            else
            {
                // An error occurred, so release the interface.
                pWc->Release();
            }
        } 
    } 
    pVmr->Release(); 
    return hr; 
} 
```



Questa funzione presuppone che sia visualizzato un solo flusso video e non si combina una bitmap statica sul video. Per informazioni dettagliate, vedere [Modalità senza finestra di VMR.](vmr-windowless-mode.md) Chiamare questa funzione nel modo seguente:


```C++
IVMRWindowlessControl *pWc = NULL;
hr = InitWindowlessVMR(hwnd, pGraph, &g_pWc);
if (SUCCEEDED(hr))
{
    // Build the graph. For example:
    pGraph->RenderFile(wszMyFileName, 0);
    // Release the VMR interface when you are done.
    pWc->Release();
}
```



## <a name="position-the-video"></a>Posizionare il video

Dopo aver configurato il vmr, il passaggio successivo consiste nell'impostare la posizione del video. Esistono due rettangoli da considerare, il *rettangolo di* origine e il rettangolo *di* destinazione. Il rettangolo di origine definisce la parte del video da visualizzare. Il rettangolo di destinazione specifica l'area nell'area client della finestra che conterrà il video. La macchina virtuale ritaglia l'immagine video nel rettangolo di origine e estende l'immagine ritagliata per adattarla al rettangolo di destinazione.

**VMR-7**

1.  Chiamare il [**metodo IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) per specificare entrambi i rettangoli.
2.  Il rettangolo di origine deve essere uguale o inferiore alle dimensioni del video nativo. È possibile usare il [**metodo IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) per ottenere le dimensioni del video nativo.

**VMR-9**

1.  Chiamare il [**metodo IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) per specificare entrambi i rettangoli.
2.  Il rettangolo di origine deve essere uguale o inferiore alle dimensioni del video nativo. È possibile usare il [**metodo IVMRWindowlessControl9::GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) per ottenere le dimensioni del video nativo.

Ad esempio, il codice seguente imposta i rettangoli di origine e di destinazione per VMR-7. Imposta il rettangolo di origine uguale all'intera immagine video e il rettangolo di destinazione uguale all'intera area client della finestra:


```C++
// Find the native video size.
long lWidth, lHeight; 
HRESULT hr = g_pWc->GetNativeVideoSize(&lWidth, &lHeight, NULL, NULL); 
if (SUCCEEDED(hr))
{
    RECT rcSrc, rcDest; 
    // Set the source rectangle.
    SetRect(&rcSrc, 0, 0, lWidth, lHeight); 
    
    // Get the window client area.
    GetClientRect(hwnd, &rcDest); 
    // Set the destination rectangle.
    SetRect(&rcDest, 0, 0, rcDest.right, rcDest.bottom); 
    
    // Set the video position.
    hr = g_pWc->SetVideoPosition(&rcSrc, &rcDest); 
}
```



Se si vuole che il video occupi una parte più piccola dell'area client, modificare il *parametro rcDest.* Se si vuole ritagliare l'immagine video, modificare il *parametro rcSrc.*

## <a name="handle-window-messages"></a>Gestire i messaggi della finestra

Poiché il vmr non ha una finestra propria, deve ricevere una notifica se deve ridisegnare o ridimensionare il video. Rispondere ai messaggi della finestra seguenti chiamando i metodi VMR elencati.

**VMR-7**

1.  [**WM \_ DISEGNARE**](../gdi/wm-paint.md). Chiamare [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo). Questo metodo fa sì che VMR-7 ridisegni il fotogramma video più recente.
2.  [**WM \_ DISPLAYCHANGE:**](../gdi/wm-displaychange.md)chiama [**IVMRWindowlessControl::D isplayModeChanged.**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged) Questo metodo notifica a VMR-7 che il video deve essere visualizzato con una nuova risoluzione o profondità del colore.
3.  [**WM \_ SIZE**](../winmsg/wm-size.md) o [**WM \_ WINDOWPOSCHANGED:**](../winmsg/wm-windowposchanged.md)ricalcola la posizione del video e chiama [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) per aggiornare la posizione, se necessario.

**VMR-9**

1.  [**WM \_ DISEGNARE**](../gdi/wm-paint.md). Chiamare [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo). Questo metodo fa sì che VMR-9 ridisegni il fotogramma video più recente.
2.  [**WM \_ DISPLAYCHANGE:**](../gdi/wm-displaychange.md)chiama [**IVMRWindowlessControl9::D isplayModeChanged.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged) Questo metodo notifica a VMR-9 che il video deve essere visualizzato con una nuova risoluzione o profondità del colore.
3.  [**WM \_ SIZE**](../winmsg/wm-size.md) o [**WM \_ WINDOWPOSCHANGED:**](../winmsg/wm-windowposchanged.md)ricalcola la posizione del video e chiama [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) per aggiornare la posizione, se necessario.

> [!Note]  
> Il gestore predefinito per il [**messaggio WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) invia un [**messaggio WM \_ SIZE.**](../winmsg/wm-size.md) Tuttavia, se l'applicazione intercetta WM WINDOWPOSCHANGED e non la passa a [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)devi chiamare **SetVideoPosition** nel gestore **WM \_ WINDOWPOSCHANGED,** oltre al gestore **WM \_ SIZE.** **\_**

 

L'esempio seguente mostra un [**gestore di messaggi WM \_ PAINT.**](../gdi/wm-paint.md) Disegna un'area definita dal rettangolo client meno il rettangolo video. Non disegnare sul rettangolo video, perché la macchina virtuale disegna su di esso, causando sfarfallio. Per lo stesso motivo, non impostare un pennello di sfondo nella classe della finestra.


```C++
void OnPaint(HWND hwnd) 
{ 
    PAINTSTRUCT ps; 
    HDC         hdc; 
    RECT        rcClient; 
    GetClientRect(hwnd, &rcClient); 
    hdc = BeginPaint(hwnd, &ps); 
    if (g_pWc != NULL) 
    { 
        // Find the region where the application can paint by subtracting 
        // the video destination rectangle from the client area.
        // (Assume that g_rcDest was calculated previously.)
        HRGN rgnClient = CreateRectRgnIndirect(&rcClient); 
        HRGN rgnVideo  = CreateRectRgnIndirect(&g_rcDest);  
        CombineRgn(rgnClient, rgnClient, rgnVideo, RGN_DIFF);  
        
        // Paint on window.
        HBRUSH hbr = GetSysColorBrush(COLOR_BTNFACE); 
        FillRgn(hdc, rgnClient, hbr); 

        // Clean up.
        DeleteObject(hbr); 
        DeleteObject(rgnClient); 
        DeleteObject(rgnVideo); 

        // Request the VMR to paint the video.
        HRESULT hr = g_pWc->RepaintVideo(hwnd, hdc);  
    } 
    else  // There is no video, so paint the whole client area. 
    { 
        FillRect(hdc, &rc2, (HBRUSH)(COLOR_BTNFACE + 1)); 
    } 
    EndPaint(hwnd, &ps); 
} 
```



Anche se è necessario rispondere ai [**messaggi WM \_ PAINT,**](../gdi/wm-paint.md) non è necessario eseguire alcuna operazione tra i **messaggi WM \_ PAINT** per aggiornare il video. Come illustrato in questo esempio, la modalità senza finestra consente di considerare l'immagine video semplicemente come un'area di disegno automatica nella finestra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del renderer di combinazione di video](using-the-video-mixing-renderer.md)
</dt> <dt>

[Video Rendering](video-rendering.md)
</dt> </dl>

 

 
