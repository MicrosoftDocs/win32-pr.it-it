---
description: Uso della modalità senza finestra
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: Uso della modalità senza finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393b112c6d340c3440521876da08111dd4bb0e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883093"
---
# <a name="using-windowless-mode"></a>Uso della modalità senza finestra

Sia il [filtro del renderer video mixing 7](video-mixing-renderer-filter-7.md) (VMR-7) che il [filtro del renderer video mixing 9](video-mixing-renderer-filter-9.md) (VMR-9) supportano la *modalità senza finestra*, che rappresenta un miglioramento significativo rispetto all'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . In questo argomento vengono descritte le differenze tra la modalità senza finestra e la modalità finestra e come utilizzare la modalità senza finestra.

Per mantenere la compatibilità con le applicazioni esistenti, il valore predefinito di VMR è la modalità con finestra. In modalità finestra, il renderer crea la propria finestra per visualizzare il video. In genere, l'applicazione imposta la finestra video come figlio della finestra dell'applicazione. L'esistenza di una finestra video separata comporta tuttavia alcuni problemi:

-   In particolare, è possibile che si verifichino deadlock se i messaggi della finestra vengono inviati tra i thread.
-   Il gestore del grafo del filtro deve trasmettere al renderer video alcuni messaggi della finestra, ad esempio WM \_ Paint. L'applicazione deve usare l'implementazione del gestore del grafo del filtro di [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (e non il renderer video), in modo che il gestore del grafico del filtro mantenga lo stato interno corretto.
-   Per ricevere gli eventi del mouse o della tastiera dalla finestra del video, l'applicazione deve impostare un *svuotamento del messaggio*, facendo sì che la finestra video inoltri tali messaggi all'applicazione.
-   Per evitare problemi di ritaglio, la finestra video deve avere gli stili della finestra corretti.

La modalità senza finestra consente di evitare questi problemi VMR direttamente sull'area client della finestra dell'applicazione, utilizzando DirectDraw per ritagliare il rettangolo del video. La modalità senza finestra riduce significativamente la probabilità di deadlock. Inoltre, l'applicazione non deve impostare la finestra proprietaria né gli stili della finestra. Infatti, quando il VMR è in modalità senza finestra, non espone anche l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) , che non è più necessaria.

Per usare la modalità senza finestra, è necessario configurare in modo esplicito VMR. Tuttavia, si noterà che è più flessibile e più semplice da usare rispetto alla modalità Window.

Il filtro VMR-7 e il filtro VMR-9 espongono interfacce diverse, ma i passaggi sono equivalenti per ciascuno di essi.

## <a name="configure-the-vmr-for-windowless-mode"></a>Configurare VMR per la modalità senza finestra

Per eseguire l'override del comportamento predefinito di VMR, configurare VMR prima di compilare il grafico del filtro:

**VMR-7**

1.  Creare il gestore del grafico dei filtri.
2.  Creare VMR-7 e aggiungerlo al grafico dei filtri.
3.  Chiamare [**IVMRFilterConfig:: SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) in VMR-7 con il flag **VMRMode senza \_ finestra** .
4.  Eseguire una query su VMR-7 per l'interfaccia [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .
5.  Chiamare [**IVMRWindowlessControl:: SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) in VMR-7. Specificare un handle per la finestra in cui deve essere visualizzato il video.

**VMR-9**

1.  Creare il gestore del grafico dei filtri.
2.  Creare VMR-9 e aggiungerlo al grafico del filtro.
3.  Chiamare [**IVMRFilterConfig9:: SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) in VMR-9 con il flag **VMR9Mode senza \_ finestra** .
4.  Eseguire una query su VMR-9 per l'interfaccia [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .
5.  Chiamare [**IVMRWindowlessControl9:: SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) in VMR-9. Specificare un handle per la finestra in cui deve essere visualizzato il video.

A questo punto, compilare il resto del grafo del filtro chiamando [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o altri metodi di creazione di grafici. Filter Graph Manager usa automaticamente l'istanza di VMR aggiunta al grafo. Per informazioni dettagliate sul motivo per cui si verifica questo problema, vedere la pagina relativa alla [connessione intelligente](intelligent-connect.md).

Il codice seguente illustra una funzione helper che crea VMR-7, la aggiunge al grafo e imposta la modalità senza finestra.


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



Questa funzione presuppone che venga visualizzato un solo flusso video e che non si mescoli una bitmap statica sul video. Per informazioni dettagliate, vedere [modalità senza finestra VMR](vmr-windowless-mode.md). Questa funzione verrà chiamata come segue:


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

Dopo aver configurato il VMR, il passaggio successivo consiste nell'impostare la posizione del video. È necessario considerare due rettangoli, il rettangolo di *origine* e il rettangolo di *destinazione* . Il rettangolo di origine definisce la parte del video da visualizzare. Il rettangolo di destinazione specifica l'area dell'area client della finestra che conterrà il video. VMR consente di ritagliare l'immagine del video nel rettangolo di origine e di allungare l'immagine ritagliata per adattarla al rettangolo di destinazione.

**VMR-7**

1.  Chiamare il metodo [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) per specificare entrambi i rettangoli.
2.  Il rettangolo di origine deve essere minore o uguale alla dimensione del video nativa; è possibile usare il metodo [**IVMRWindowlessControl:: GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) per ottenere la dimensione del video nativa.

**VMR-9**

1.  Chiamare il metodo [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) per specificare entrambi i rettangoli.
2.  Il rettangolo di origine deve essere minore o uguale alla dimensione del video nativa; è possibile usare il metodo [**IVMRWindowlessControl9:: GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) per ottenere la dimensione del video nativa.

Il codice seguente, ad esempio, imposta i rettangoli di origine e di destinazione per VMR-7. Imposta il rettangolo di origine uguale all'intera immagine video e il rettangolo di destinazione è uguale all'intera area client della finestra:


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



Se si vuole che il video occupi una parte più piccola dell'area client, modificare il parametro *rcDest* . Se si vuole ritagliare l'immagine video, modificare il parametro *rcSrc* .

## <a name="handle-window-messages"></a>Gestire i messaggi della finestra

Poiché VMR non dispone di una propria finestra, è necessario ricevere una notifica se è necessario ridisegnare o ridimensionare il video. Per rispondere ai messaggi della finestra seguenti, chiamare i metodi VMR elencati.

**VMR-7**

1.  [**WM \_ Disegna**](../gdi/wm-paint.md). Chiamare [**IVMRWindowlessControl:: RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo). Questo metodo fa in modo che VMR-7 ridisegni il frame video più recente.
2.  [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): chiama [**IVMRWindowlessControl::D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged). Questo metodo notifica a VMR-7 che il video deve essere visualizzato con una nuova risoluzione o profondità del colore.
3.  [**WM \_ SIZE**](../winmsg/wm-size.md) o [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): ricalcolare la posizione del video e chiamare [**IVMRWindowlessControl:: SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) per aggiornare la posizione, se necessario.

**VMR-9**

1.  [**WM \_ Disegna**](../gdi/wm-paint.md). Chiamare [**IVMRWindowlessControl9:: RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo). Questo metodo fa in modo che VMR-9 ridisegni il frame video più recente.
2.  [**WM \_ DISPLAYCHANGE**](../gdi/wm-displaychange.md): chiama [**IVMRWindowlessControl9::D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged). Questo metodo notifica a VMR-9 che il video deve essere visualizzato con una nuova risoluzione o profondità del colore.
3.  [**WM \_ SIZE**](../winmsg/wm-size.md) o [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): ricalcolare la posizione del video e chiamare [**IVMRWindowlessControl9:: SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) per aggiornare la posizione, se necessario.

> [!Note]  
> Il gestore predefinito per il messaggio [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) Invia un messaggio di [**\_ dimensioni WM**](../winmsg/wm-size.md) . Tuttavia, se l'applicazione intercetta **WM \_ WINDOWPOSCHANGED** e non la passa a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), è necessario chiamare **SetVideoPosition** nel gestore **WM \_ WINDOWPOSCHANGED** , oltre al gestore **\_ dimensioni WM** .

 

Nell'esempio seguente viene illustrato un gestore di messaggi di [**\_ disegno WM**](../gdi/wm-paint.md) . Disegna un'area definita dal rettangolo client meno il rettangolo del video. Non disegnare sul rettangolo video, perché il VMR ne eseguirà il disegno, causando lo sfarfallio. Per lo stesso motivo, non impostare un pennello per lo sfondo nella classe della finestra.


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



Sebbene sia necessario rispondere ai messaggi di [**\_ disegno WM**](../gdi/wm-paint.md) , non è necessario eseguire alcuna operazione tra i messaggi di **\_ disegno WM** per aggiornare il video. Come illustrato in questo esempio, la modalità senza finestra consente di gestire l'immagine video semplicemente come area di disegno automatico nella finestra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del renderer video mixing](using-the-video-mixing-renderer.md)
</dt> <dt>

[Rendering video](video-rendering.md)
</dt> </dl>

 

 
