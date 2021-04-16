---
title: Visualizzare una bitmap fornita dall'app nell'immagine composita
description: Visualizzazione di un Application-Supplied bitmap nell'immagine composita
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ecd8ac931d0a0bb83eafba09d8ca7dc8263f0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520577"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a>Visualizzare una bitmap fornita dall'app nell'immagine composita

Le applicazioni possono usare la modalità di combinazione di VMR per visualizzare i loghi del canale con Blend alfa, un'interfaccia utente o annunci parzialmente o completamente all'interno del rettangolo video. Poiché la fusione viene eseguita nell'hardware dal processore di grafica, è possibile avere un effetto minimo sulle prestazioni di riproduzione del flusso video e non ci sono elementi di sfarfallio rilevabili o di strappi. Le applicazioni possono modificare l'immagine visualizzata con la frequenza desiderata. Si noti che le modifiche si riflettono solo sullo schermo quando il grafico del filtro DirectShow è nello stato in esecuzione.

VMR usa il componente Mixer per sovrapporre la bitmap nell'immagine composita. Con VMR-7, l'applicazione deve forzare il VMR a caricare il mixer, anche se è presente un solo flusso video. Questa operazione non è necessaria con VMR-9 perché carica il mixer per impostazione predefinita.

Per fondere un'immagine bitmap statica con il flusso video, l'applicazione crea il VMR e lo aggiunge al grafo, quindi chiama [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). Il valore passato a questa funzione identifica il numero di pin di input che deve essere creato da VMR. Le applicazioni possono specificare qualsiasi valore compreso tra 1 e \_ i flussi di mixer massimo. \_ se si specifica un valore 1, il valore è valido se l'applicazione prevede solo la visualizzazione di un singolo flusso video. Anche se VMR-7 ha un singolo pin di input per impostazione predefinita, questo metodo deve essere chiamato per forzare il caricamento del componente mixer. (VMR-9 carica il mixer e configura quattro pin per impostazione predefinita).

Per impostare la bitmap, utilizzare l'interfaccia [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) sull'interfaccia VMR-7 o [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) su VMR-9.

La bitmap può essere specificata da un handle per un contesto di dispositivo GDI (hDC) o da un'interfaccia di superficie DirectDraw. Se l'applicazione desidera che l'immagine contenga informazioni Alpha incorporate (anche note come per pixel alfa), deve inserire i dati dell'immagine in un'interfaccia di superficie DirectDraw. Questo perché non è attualmente possibile inserire informazioni alfa per pixel con un contesto di dispositivo GDI. La superficie DirectDraw deve essere RGB32 o ARGB32 e deve essere preferibilmente una superficie di memoria di sistema. Non è necessario che le dimensioni della superficie siano una potenza di 2.

VMR consente alle applicazioni di specificare il percorso e un valore di trasparenza generale per l'immagine. Il codice seguente illustra come passare i dati dell'immagine fino al VMR per la fusione successiva:


```C++
HRESULT BlendApplicationImage( 
  HWND hwndApp,
  IVMRWindowlessControl* pWc,
  HBITMAP hbm
)
{
    LONG cx, cy;
    HRESULT hr;
    hr = pWc->GetNativeVideoSize(&cx, &cy, NULL, NULL);
    if (FAILED(hr))
        return hr;
    
    HDC hdc = GetDC(hwndApp);
    if (hdc == NULL)
    {
        return E_FAIL;
    }
    
    HDC hdcBmp = CreateCompatibleDC(hdc);
    ReleaseDC(hwndApp, hdc);
    
    if (hdcBmp == NULL)
    {
        return E_FAIL;
    }
    
    BITMAP bm;
    if (0 == GetObject(hbm, sizeof(bm), &bm))
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    HBITMAP hbmOld = (HBITMAP)SelectObject(hdcBmp, hbm);
    if (hbmOld == 0)
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    VMRALPHABITMAP bmpInfo;
    ZeroMemory(&bmpInfo, sizeof(bmpInfo) );
    bmpInfo.dwFlags = VMRBITMAP_HDC;
    bmpInfo.hdc = hdcBmp;
    
    // Show the entire bitmap in the top-left corner of the video image.
    SetRect(&bmpInfo.rSrc, 0, 0, bm.bmWidth, bm.bmHeight);
    bmpInfo.rDest.left = 0.f;
    bmpInfo.rDest.top = 0.f;
    bmpInfo.rDest.right = (float)bm.bmWidth / (float)cx;
    bmpInfo.rDest.bottom = (float)bm.bmHeight / (float)cy;
    
    // Set the transparency value (1.0 is opaque, 0.0 is transparent).
    bmpInfo.fAlpha = 0.2f;
    
    IVMRMixerBitmap* pBmp;
    hr = pWc->QueryInterface(IID_IVMRMixerBitmap, (LPVOID *)&pBmp);
    if (SUCCEEDED(hr)) 
    {
        pBmp->SetAlphaBitmap(&bmpInfo);
        pBmp->Release();
    }
    
    DeleteObject(SelectObject(hdcBmp, hbmOld));
    DeleteDC(hdcBmp);
    return hr;
}
```



I concetti illustrati in questo argomento sono illustrati nell'applicazione di esempio [VMRPlayer](vmrplayer-sample.md) .

**Creazione di animazioni semplici con l'immagine bitmap**

Per creare un semplice logo bitmap animato, inserire tutti i "frame" della bitmap in un'unica immagine, come illustrato nella figura seguente.

![VMR image Strip](images/vmr-image-strip.png)

Quando si imposta la bitmap inizialmente usando [**IVMRMixerBitmap:: SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), se la bitmap si trova in un HDC, impostare il campo **RSrc** della struttura **VMRALPHABITMAP** per specificare le dimensioni dell'intera bitmap all'interno di HDC. I membri **superiore** e **sinistro** della struttura vengono impostati su 0 e i membri **destro** e **inferiore** sono la larghezza e l'altezza della bitmap. Se la bitmap si trova in una superficie DirectDraw, le dimensioni della superficie sono note, pertanto non è necessario specificare rSrc in questo metodo.

Quando si chiama [**IVMRMixerBitmap:: UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), usare il membro **rsrc** per le bitmap HDC e DirectDraw, per specificare il frame o il rettangolo specifico all'interno dell'immagine che si vuole visualizzare e impostare il flag **VMRBITMAP \_ SRCRECT** nel membro **dwFlags** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità di combinazione VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



