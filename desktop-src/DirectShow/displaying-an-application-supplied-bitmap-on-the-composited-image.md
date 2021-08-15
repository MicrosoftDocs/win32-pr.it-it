---
title: Visualizzare una bitmap fornita dall'app nell'immagine composita
description: Visualizzazione di una Application-Supplied bitmap nell'immagine composita
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90768cc9ba9ed3a7f53336c63b0112f297e1844ba9638799e8badf28588775eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653518"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a>Visualizzare una bitmap fornita dall'app nell'immagine composita

Le applicazioni possono usare la modalità di combinazione della macchina virtuale per visualizzare i logo del canale con combinazione alfa, un'interfaccia utente o annunci parzialmente o completamente all'interno del rettangolo video. Poiché la fusione viene eseguita nell'hardware dal processore grafico, l'impatto sulle prestazioni di riproduzione del flusso video è minimo e non sono presenti elementi di sfarfallio o di rimozione rilevabili. Le applicazioni possono modificare l'immagine visualizzata con la frequenza richiesta. Si noti che le modifiche vengono riflesse sullo schermo solo quando il grafico DirectShow filtro è in esecuzione.

La macchina virtuale usa il componente mixer per sovrapporre la bitmap all'immagine composita. Con VMR-7, l'applicazione deve forzare il caricamento del mixer, anche se è presente un solo flusso video. Questa operazione non è necessaria con vmr-9 perché carica il mixer per impostazione predefinita.

Per unire un'immagine bitmap statica al flusso video, l'applicazione crea la macchina virtuale e la aggiunge al grafo e quindi chiama [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams). Il valore passato a questa funzione identifica il numero di pin di input che la macchina virtuale deve creare. Le applicazioni possono specificare qualsiasi valore compreso tra 1 e MAX MIXER STREAMS. Se l'applicazione intende visualizzare un solo flusso video, specificare un valore \_ \_ pari a 1. Anche se vmr-7 ha un singolo pin di input per impostazione predefinita, questo metodo deve essere chiamato per forzare il caricamento del componente mixer. VmR-9 carica il mixer e configura quattro pin per impostazione predefinita.

Per impostare la bitmap, usare [**l'interfaccia IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) in VMR-7 o [**l'interfaccia IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) nella VMR-9.

La bitmap può essere specificata da un handle per un contesto di dispositivo GDI (hDC) o da un'interfaccia Surface DirectDraw. Se l'applicazione vuole che l'immagine contenga informazioni alfa incorporate (note anche come alfa per pixel), deve inserire i dati dell'immagine in un'interfaccia Surface DirectDraw. Ciò è dovuto al fatto che attualmente non è possibile inserire informazioni alfa per pixel con un contesto di dispositivo GDI. La superficie DirectDraw deve essere RGB32 o ARGB32 e deve essere preferibilmente una superficie di memoria di sistema. Non è necessario che le dimensioni della superficie siano una potenza di 2.

La macchina virtuale consente alle applicazioni di specificare la posizione e un valore di trasparenza complessivo per l'immagine. Il codice seguente illustra come passare i dati immagine alla macchina virtuale per la fusione successiva:


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



I concetti illustrati in questo argomento sono illustrati nell'applicazione di esempio [VMRPlayer Sample.](vmrplayer-sample.md)

**Creazione di animazioni semplici con l'immagine bitmap**

Per creare un logo bitmap animato semplice, inserire tutti i "fotogrammi" della bitmap in una singola immagine, come illustrato nella figura seguente.

![Strip di immagini vmr](images/vmr-image-strip.png)

Quando si imposta inizialmente la bitmap usando [**IVMRMixerBitmap::SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), se la bitmap si trova in hdc, impostare il campo **rSrc** della struttura **VMRALPHABITMAP** per specificare le dimensioni dell'intera bitmap all'interno di HDC. I **membri** superiore **e** sinistro della struttura sono  impostati  su 0 e i membri destro e inferiore sono la larghezza e l'altezza della bitmap. Se la bitmap si trova in una superficie DirectDraw, le dimensioni della superficie sono note, quindi non è necessario specificare rSrc in questo metodo.

Quando si chiama [**IVMRMixerBitmap::UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), usare il membro **rSrc** per le bitmap HDC e DirectDraw, specificare il frame o il rettangolo specifico all'interno dell'immagine che si vuole visualizzare e impostare il flag **VMRBITMAP \_ SRCRECT** nel membro **dwFlags.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità di combinazione vmr](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



