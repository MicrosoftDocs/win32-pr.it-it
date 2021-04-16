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
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a><span data-ttu-id="7bec8-103">Visualizzare una bitmap fornita dall'app nell'immagine composita</span><span class="sxs-lookup"><span data-stu-id="7bec8-103">Display an app-supplied bitmap on the composited image</span></span>

<span data-ttu-id="7bec8-104">Le applicazioni possono usare la modalità di combinazione di VMR per visualizzare i loghi del canale con Blend alfa, un'interfaccia utente o annunci parzialmente o completamente all'interno del rettangolo video.</span><span class="sxs-lookup"><span data-stu-id="7bec8-104">Applications can use the VMR's mixing mode to display alpha-blended channel logos, a user interface, or advertisements either partially or completely within the video rectangle.</span></span> <span data-ttu-id="7bec8-105">Poiché la fusione viene eseguita nell'hardware dal processore di grafica, è possibile avere un effetto minimo sulle prestazioni di riproduzione del flusso video e non ci sono elementi di sfarfallio rilevabili o di strappi.</span><span class="sxs-lookup"><span data-stu-id="7bec8-105">Because the blending is performed in hardware by the graphics processor, there is minimal impact to the playback performance of the Video Stream, and there are no detectable flicker or tearing artifacts.</span></span> <span data-ttu-id="7bec8-106">Le applicazioni possono modificare l'immagine visualizzata con la frequenza desiderata.</span><span class="sxs-lookup"><span data-stu-id="7bec8-106">Applications can change the image displayed as frequently as they wish.</span></span> <span data-ttu-id="7bec8-107">Si noti che le modifiche si riflettono solo sullo schermo quando il grafico del filtro DirectShow è nello stato in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7bec8-107">It should be noted that changes are only reflected on the screen when the DirectShow filter graph is in the running state.</span></span>

<span data-ttu-id="7bec8-108">VMR usa il componente Mixer per sovrapporre la bitmap nell'immagine composita.</span><span class="sxs-lookup"><span data-stu-id="7bec8-108">The VMR uses its mixer component to overlay the bitmap onto the composited image.</span></span> <span data-ttu-id="7bec8-109">Con VMR-7, l'applicazione deve forzare il VMR a caricare il mixer, anche se è presente un solo flusso video.</span><span class="sxs-lookup"><span data-stu-id="7bec8-109">With the VMR-7, the application must force the VMR to load its mixer, even if there is only a single video stream.</span></span> <span data-ttu-id="7bec8-110">Questa operazione non è necessaria con VMR-9 perché carica il mixer per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7bec8-110">This is not necessary with the VMR-9 since it loads its mixer by default.</span></span>

<span data-ttu-id="7bec8-111">Per fondere un'immagine bitmap statica con il flusso video, l'applicazione crea il VMR e lo aggiunge al grafo, quindi chiama [**IVMRFilterConfig:: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="7bec8-111">To blend a static bitmap image with the video stream, the application creates the VMR and adds it to the graph, and then calls [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="7bec8-112">Il valore passato a questa funzione identifica il numero di pin di input che deve essere creato da VMR.</span><span class="sxs-lookup"><span data-stu-id="7bec8-112">The value passed to this function identifies the number of input pins that the VMR should create.</span></span> <span data-ttu-id="7bec8-113">Le applicazioni possono specificare qualsiasi valore compreso tra 1 e \_ i flussi di mixer massimo. \_ se si specifica un valore 1, il valore è valido se l'applicazione prevede solo la visualizzazione di un singolo flusso video.</span><span class="sxs-lookup"><span data-stu-id="7bec8-113">Applications can specify any value between 1 and MAX\_MIXER\_STREAMS; specifying a value of 1 is valid if the application only intends to display a single video stream.</span></span> <span data-ttu-id="7bec8-114">Anche se VMR-7 ha un singolo pin di input per impostazione predefinita, questo metodo deve essere chiamato per forzare il caricamento del componente mixer.</span><span class="sxs-lookup"><span data-stu-id="7bec8-114">Even though the VMR-7 has a single input pin by default, this method must be called in order to force it to load its mixer component.</span></span> <span data-ttu-id="7bec8-115">(VMR-9 carica il mixer e configura quattro pin per impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="7bec8-115">(The VMR-9 loads its mixer and sets up four pins by default.)</span></span>

<span data-ttu-id="7bec8-116">Per impostare la bitmap, utilizzare l'interfaccia [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) sull'interfaccia VMR-7 o [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) su VMR-9.</span><span class="sxs-lookup"><span data-stu-id="7bec8-116">To set the bitmap, use the [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) interface on the VMR-7 or the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface on the VMR-9.</span></span>

<span data-ttu-id="7bec8-117">La bitmap può essere specificata da un handle per un contesto di dispositivo GDI (hDC) o da un'interfaccia di superficie DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="7bec8-117">The bitmap can be specified by either a handle to a GDI Device Context (hDC) or by a DirectDraw Surface interface.</span></span> <span data-ttu-id="7bec8-118">Se l'applicazione desidera che l'immagine contenga informazioni Alpha incorporate (anche note come per pixel alfa), deve inserire i dati dell'immagine in un'interfaccia di superficie DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="7bec8-118">If the application wants the image to contain embedded alpha information (also known as per pixel alpha) it must place the image data in a DirectDraw Surface interface.</span></span> <span data-ttu-id="7bec8-119">Questo perché non è attualmente possibile inserire informazioni alfa per pixel con un contesto di dispositivo GDI.</span><span class="sxs-lookup"><span data-stu-id="7bec8-119">This is because it is not currently possible to place per-pixel alpha information with a GDI Device Context.</span></span> <span data-ttu-id="7bec8-120">La superficie DirectDraw deve essere RGB32 o ARGB32 e deve essere preferibilmente una superficie di memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="7bec8-120">The DirectDraw surface must be either RGB32 or ARGB32, and should preferably be a system memory surface.</span></span> <span data-ttu-id="7bec8-121">Non è necessario che le dimensioni della superficie siano una potenza di 2.</span><span class="sxs-lookup"><span data-stu-id="7bec8-121">It is not necessary for the surface dimensions to be a power of 2.</span></span>

<span data-ttu-id="7bec8-122">VMR consente alle applicazioni di specificare il percorso e un valore di trasparenza generale per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="7bec8-122">The VMR allows applications to specify the location and an overall transparency value for the image.</span></span> <span data-ttu-id="7bec8-123">Il codice seguente illustra come passare i dati dell'immagine fino al VMR per la fusione successiva:</span><span class="sxs-lookup"><span data-stu-id="7bec8-123">The following code shows how to pass image data down to the VMR for subsequent blending:</span></span>


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



<span data-ttu-id="7bec8-124">I concetti illustrati in questo argomento sono illustrati nell'applicazione di esempio [VMRPlayer](vmrplayer-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="7bec8-124">The concepts discussed in this topic are demonstrated in the [VMRPlayer Sample](vmrplayer-sample.md) sample application.</span></span>

<span data-ttu-id="7bec8-125">**Creazione di animazioni semplici con l'immagine bitmap**</span><span class="sxs-lookup"><span data-stu-id="7bec8-125">**Creating Simple Animations with the Bitmap Image**</span></span>

<span data-ttu-id="7bec8-126">Per creare un semplice logo bitmap animato, inserire tutti i "frame" della bitmap in un'unica immagine, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="7bec8-126">To create a simple animated bitmap logo, put all of the bitmap "frames" into a single image, as shown in the following illustration.</span></span>

![VMR image Strip](images/vmr-image-strip.png)

<span data-ttu-id="7bec8-128">Quando si imposta la bitmap inizialmente usando [**IVMRMixerBitmap:: SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), se la bitmap si trova in un HDC, impostare il campo **RSrc** della struttura **VMRALPHABITMAP** per specificare le dimensioni dell'intera bitmap all'interno di HDC.</span><span class="sxs-lookup"><span data-stu-id="7bec8-128">When you set the bitmap initially using [**IVMRMixerBitmap::SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), if the bitmap is in an HDC, set the **rSrc** field of the **VMRALPHABITMAP** structure to specify the size of the entire bitmap within the HDC.</span></span> <span data-ttu-id="7bec8-129">I membri **superiore** e **sinistro** della struttura vengono impostati su 0 e i membri **destro** e **inferiore** sono la larghezza e l'altezza della bitmap.</span><span class="sxs-lookup"><span data-stu-id="7bec8-129">The **top** and **left** members of the structure are set to 0, and the **right** and **bottom** members are the width and height of the bitmap.</span></span> <span data-ttu-id="7bec8-130">Se la bitmap si trova in una superficie DirectDraw, le dimensioni della superficie sono note, pertanto non è necessario specificare rSrc in questo metodo.</span><span class="sxs-lookup"><span data-stu-id="7bec8-130">If the bitmap is in a DirectDraw surface, then the size of the surface is known, so there is no need to specify rSrc in this method.</span></span>

<span data-ttu-id="7bec8-131">Quando si chiama [**IVMRMixerBitmap:: UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), usare il membro **rsrc** per le bitmap HDC e DirectDraw, per specificare il frame o il rettangolo specifico all'interno dell'immagine che si vuole visualizzare e impostare il flag **VMRBITMAP \_ SRCRECT** nel membro **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="7bec8-131">When you call [**IVMRMixerBitmap::UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), use the **rSrc** member for both HDC and DirectDraw bitmaps, to specify the particular frame or rectangle within the image that you wish to display, and set the **VMRBITMAP\_SRCRECT** flag in the **dwFlags** member.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bec8-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7bec8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bec8-133">Uso della modalità di combinazione VMR</span><span class="sxs-lookup"><span data-stu-id="7bec8-133">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



