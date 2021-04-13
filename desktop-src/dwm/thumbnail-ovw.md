---
title: Panoramica dell'anteprima di DWM
description: Gestione finestre desktop (DWM) consente la visualizzazione delle rappresentazioni di anteprime delle finestre dell'applicazione.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Gestione finestre desktop (DWM), anteprime
- DWM (Gestione finestre desktop), anteprime
- Gestione finestre desktop (DWM), relazioni di anteprima
- DWM (Gestione finestre desktop), relazioni di anteprima
- anteprime in miniatura
- relazioni di anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3e0f1e6875e447a18ff5e63d703460ff909b25
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104559704"
---
# <a name="dwm-thumbnail-overview"></a><span data-ttu-id="2d76b-109">Panoramica dell'anteprima di DWM</span><span class="sxs-lookup"><span data-stu-id="2d76b-109">DWM Thumbnail Overview</span></span>

<span data-ttu-id="2d76b-110">Gestione finestre desktop (DWM) consente la visualizzazione delle rappresentazioni di anteprime delle finestre dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d76b-110">Desktop Window Manager (DWM) enables the display of thumbnail representations of application windows.</span></span> <span data-ttu-id="2d76b-111">Queste non sono snapshot statiche di una finestra, ma sono invece dinamiche, connessioni costanti tra una finestra di origine di anteprima e un percorso in una finestra di destinazione che riceve il rendering dell'anteprima in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="2d76b-111">These are not static snapshots of a window, but are instead dynamic, constant connections between a thumbnail source window and a location on a destination window that receives the live thumbnail rendering.</span></span> <span data-ttu-id="2d76b-112">In questo modo è possibile visualizzare rapidamente le applicazioni in esecuzione passando il puntatore del mouse sull'applicazione sulla barra delle applicazioni o utilizzando il movimento ALT + TAB per visualizzare e passare rapidamente a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d76b-112">This allows a quick view of running applications by hovering over the application on the taskbar or using the ALT-TAB key gesture to see and quickly switch to an application.</span></span>

<span data-ttu-id="2d76b-113">Nell'immagine seguente viene illustrata l'anteprima di Windows Vista Live visualizzata quando si passa il mouse sull'applicazione sulla barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2d76b-113">The following image illustrates the Windows Vista live thumbnail seen when you hover over the application on the taskbar.</span></span>

![Screenshot che mostra l'anteprima D W M visualizzata quando si passa il puntatore del mouse su un'app nella barra delle applicazioni.](images/dwm-livethumbnail.png)

<span data-ttu-id="2d76b-115">Nell'immagine seguente viene illustrata la versione di Windows Vista (ALT + TAB) abilitata da DWM.</span><span class="sxs-lookup"><span data-stu-id="2d76b-115">The following image illustrates the Windows Vista Flip (ALT-TAB) enabled by DWM.</span></span>

![screenshot della pagina ALT-TAB abilitata per DWM](images/dwm-flip.png)

> [!Note]  
> <span data-ttu-id="2d76b-117">Le anteprime di DWM non consentono agli sviluppatori di creare applicazioni come la funzionalità Windows Vista Flip3D (WINKEY-TAB).</span><span class="sxs-lookup"><span data-stu-id="2d76b-117">DWM thumbnails do not enable developers to create applications like the Windows Vista Flip3D (WINKEY-TAB) feature.</span></span> <span data-ttu-id="2d76b-118">Il rendering delle anteprime viene eseguito direttamente nella finestra di destinazione in 2D.</span><span class="sxs-lookup"><span data-stu-id="2d76b-118">Thumbnails are rendered directly to the destination window in 2-D.</span></span>

 

## <a name="dwm-thumbnail-relationships"></a><span data-ttu-id="2d76b-119">Relazioni di anteprima di DWM</span><span class="sxs-lookup"><span data-stu-id="2d76b-119">DWM Thumbnail Relationships</span></span>

<span data-ttu-id="2d76b-120">Per visualizzare le anteprime nell'applicazione, è innanzitutto necessario stabilire una relazione tra una finestra di origine e una finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2d76b-120">To display thumbnails in your application, you must first establish a relationship between a source window and a destination window.</span></span> <span data-ttu-id="2d76b-121">Questa operazione viene eseguita chiamando la funzione [**funzionalità DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="2d76b-121">This is done by calling the [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) function.</span></span>

<span data-ttu-id="2d76b-122">[**Funzionalità DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) non esegue il rendering di un'anteprima nella finestra di destinazione, ma crea semplicemente la relazione e fornisce l'handle di anteprima.</span><span class="sxs-lookup"><span data-stu-id="2d76b-122">[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) does not render a thumbnail on the destination window but merely creates the relationship and provides the thumbnail handle.</span></span> <span data-ttu-id="2d76b-123">L'anteprima viene sottoposta a rendering dopo che sono state impostate le [**proprietà di \_ Anteprima \_ di DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) e la funzione [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) è stata chiamata.</span><span class="sxs-lookup"><span data-stu-id="2d76b-123">The thumbnail is rendered after the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) have been set and the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function has been called.</span></span> <span data-ttu-id="2d76b-124">Le chiamate successive a **DwmUpdateThumbnailProperties** aggiornano l'anteprima con un nuovo set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="2d76b-124">Subsequent calls to **DwmUpdateThumbnailProperties** update the thumbnail with a new set of properties.</span></span> <span data-ttu-id="2d76b-125">DWM fornisce anche la funzione helper [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) per ottenere le dimensioni della finestra di origine dall'anteprima.</span><span class="sxs-lookup"><span data-stu-id="2d76b-125">The DWM also provides the helper function [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) to obtain the size of the source window from the thumbnail.</span></span>

<span data-ttu-id="2d76b-126">Per terminare una relazione di anteprima, chiamare la funzione [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="2d76b-126">To end a thumbnail relationship, call the [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) function.</span></span>

<span data-ttu-id="2d76b-127">Nell'esempio seguente viene illustrato come creare un releationship con il desktop di Windows e visualizzarlo in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d76b-127">The following example demonstrates how to create a releationship with the Windows desktop and display it in an application.</span></span>


```
HRESULT hr = S_OK;
HTHUMBNAIL thumbnail = NULL;

// Register the thumbnail
hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
if (SUCCEEDED(hr))
{
    // Specify the destination rectangle size
    RECT dest = {0,50,100,150};

    // Set the thumbnail properties for use
    DWM_THUMBNAIL_PROPERTIES dskThumbProps;
    dskThumbProps.dwFlags = DWM_TNP_SOURCECLIENTAREAONLY | DWM_TNP_VISIBLE | DWM_TNP_OPACITY | DWM_TNP_RECTDESTINATION;
    dskThumbProps.fSourceClientAreaOnly = FALSE; 
    dskThumbProps.fVisible = TRUE;
    dskThumbProps.opacity = (255 * 70)/100;
    dskThumbProps.rcDestination = dest;

    // Display the thumbnail
    hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
    if (SUCCEEDED(hr))
    {
        // ...
    }
}
return hr;
```



## <a name="related-topics"></a><span data-ttu-id="2d76b-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d76b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d76b-129">Cenni preliminari di Gestione finestre desktop</span><span class="sxs-lookup"><span data-stu-id="2d76b-129">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> <dt>

[<span data-ttu-id="2d76b-130">Abilitare e controllare la composizione DWM</span><span class="sxs-lookup"><span data-stu-id="2d76b-130">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="2d76b-131">Considerazioni sulle prestazioni e procedure consigliate</span><span class="sxs-lookup"><span data-stu-id="2d76b-131">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 




