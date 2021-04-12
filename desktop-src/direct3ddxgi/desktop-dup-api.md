---
description: Windows 8 Disabilita i driver mirror standard di Windows 2000 Display Driver Model (XDDM) e offre invece l'API per la duplicazione dei desktop.
ms.assetid: 523FBFAD-5D78-4EE3-A3B7-8FD5BA39DC46
title: API di duplicazione desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad27f545318254404beb6372344d8dd0cdfdf604
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481077"
---
# <a name="desktop-duplication-api"></a><span data-ttu-id="8ce00-103">API di duplicazione desktop</span><span class="sxs-lookup"><span data-stu-id="8ce00-103">Desktop Duplication API</span></span>

<span data-ttu-id="8ce00-104">Windows 8 Disabilita i driver mirror standard di Windows 2000 Display Driver Model (XDDM) e offre invece l'API per la duplicazione dei desktop.</span><span class="sxs-lookup"><span data-stu-id="8ce00-104">Windows 8 disables standard Windows 2000 Display Driver Model (XDDM) mirror drivers and offers the desktop duplication API instead.</span></span> <span data-ttu-id="8ce00-105">L'API di duplicazione desktop fornisce accesso remoto a un'immagine desktop per scenari di collaborazione.</span><span class="sxs-lookup"><span data-stu-id="8ce00-105">The desktop duplication API provides remote access to a desktop image for collaboration scenarios.</span></span> <span data-ttu-id="8ce00-106">Le app possono usare l'API di duplicazione desktop per accedere agli aggiornamenti frame per fotogramma sul desktop.</span><span class="sxs-lookup"><span data-stu-id="8ce00-106">Apps can use the desktop duplication API to access frame-by-frame updates to the desktop.</span></span> <span data-ttu-id="8ce00-107">Poiché le app ricevono aggiornamenti per l'immagine desktop in una superficie DXGI, le app possono sfruttare tutte le potenzialità della GPU per elaborare gli aggiornamenti delle immagini.</span><span class="sxs-lookup"><span data-stu-id="8ce00-107">Because apps receive updates to the desktop image in a DXGI surface, the apps can use the full power of the GPU to process the image updates.</span></span>

-   [<span data-ttu-id="8ce00-108">Aggiornamento dei dati dell'immagine desktop</span><span class="sxs-lookup"><span data-stu-id="8ce00-108">Updating the desktop image data</span></span>](#updating-the-desktop-image-data)
-   [<span data-ttu-id="8ce00-109">Rotazione dell'immagine desktop</span><span class="sxs-lookup"><span data-stu-id="8ce00-109">Rotating the desktop image</span></span>](#rotating-the-desktop-image)
-   [<span data-ttu-id="8ce00-110">Aggiornamento del puntatore del desktop</span><span class="sxs-lookup"><span data-stu-id="8ce00-110">Updating the desktop pointer</span></span>](#updating-the-desktop-pointer)
-   [<span data-ttu-id="8ce00-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ce00-111">Related topics</span></span>](#related-topics)

## <a name="updating-the-desktop-image-data"></a><span data-ttu-id="8ce00-112">Aggiornamento dei dati dell'immagine desktop</span><span class="sxs-lookup"><span data-stu-id="8ce00-112">Updating the desktop image data</span></span>

<span data-ttu-id="8ce00-113">DXGI fornisce una superficie che contiene un'immagine desktop corrente tramite il nuovo metodo [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) .</span><span class="sxs-lookup"><span data-stu-id="8ce00-113">DXGI provides a surface that contains a current desktop image through the new [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) method.</span></span> <span data-ttu-id="8ce00-114">Il formato dell'immagine desktop è sempre [**DXGI \_ formato \_ B8G8R8A8 \_ UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , indipendentemente dalla modalità di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="8ce00-114">The format of the desktop image is always [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) no matter what the current display mode is.</span></span> <span data-ttu-id="8ce00-115">Insieme a questa superficie, questi metodi [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) restituiscono i tipi di informazioni indicati che consentono di determinare i pixel all'interno della superficie che è necessario elaborare:</span><span class="sxs-lookup"><span data-stu-id="8ce00-115">Along with this surface, these [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) methods return the indicated types of info that help you determine which pixels within the surface you need to process:</span></span>

-   <span data-ttu-id="8ce00-116">[**IDXGIOutputDuplication:: GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) restituisce aree dirty, ovvero rettangoli non sovrapposti che indicano le aree dell'immagine desktop aggiornate dal sistema operativo dopo l'elaborazione dell'immagine desktop precedente.</span><span class="sxs-lookup"><span data-stu-id="8ce00-116">[**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) returns dirty regions, which are non-overlapping rectangles that indicate the areas of the desktop image that the operating system updated since you processed the previous desktop image.</span></span>
-   <span data-ttu-id="8ce00-117">[**IDXGIOutputDuplication:: GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) restituisce le aree di spostamento, che sono rettangoli di pixel nell'immagine desktop che il sistema operativo ha spostato in un'altra posizione all'interno della stessa immagine.</span><span class="sxs-lookup"><span data-stu-id="8ce00-117">[**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) returns move regions, which are rectangles of pixels in the desktop image that the operating system moved to another location within the same image.</span></span> <span data-ttu-id="8ce00-118">Ogni area di spostamento è costituita da un rettangolo di destinazione e da un punto di origine.</span><span class="sxs-lookup"><span data-stu-id="8ce00-118">Each move region consists of a destination rectangle and a source point.</span></span> <span data-ttu-id="8ce00-119">Il punto di origine specifica il percorso da cui il sistema operativo ha copiato l'area e il rettangolo di destinazione specifica dove il sistema operativo ha spostato tale area.</span><span class="sxs-lookup"><span data-stu-id="8ce00-119">The source point specifies the location from where the operating system copied the region and the destination rectangle specifies to where the operating system moved that region.</span></span> <span data-ttu-id="8ce00-120">Le aree di spostamento sono sempre aree non estese, pertanto l'origine ha sempre le stesse dimensioni della destinazione.</span><span class="sxs-lookup"><span data-stu-id="8ce00-120">Move regions are always non-stretched regions so the source is always the same size as the destination.</span></span>

<span data-ttu-id="8ce00-121">Si supponga che l'immagine desktop sia stata trasmessa su una connessione lenta all'app client remota.</span><span class="sxs-lookup"><span data-stu-id="8ce00-121">Suppose the desktop image was transmitted over a slow connection to your remote client app.</span></span> <span data-ttu-id="8ce00-122">La quantità di dati inviati sulla connessione viene ridotta ricevendo solo i dati sul modo in cui l'app client deve spostare le aree di pixel anziché i dati effettivi sui pixel.</span><span class="sxs-lookup"><span data-stu-id="8ce00-122">The amount of data that is sent over the connection is reduced by receiving only data about how your client app must move regions of pixels rather than actual pixel data.</span></span> <span data-ttu-id="8ce00-123">Per elaborare lo spostamento, l'app client deve avere archiviato l'ultima immagine completa.</span><span class="sxs-lookup"><span data-stu-id="8ce00-123">To process the moves, your client app must have stored the complete last image.</span></span>

<span data-ttu-id="8ce00-124">Sebbene il sistema operativo accumuli aggiornamenti di immagini desktop non elaborati, lo spazio potrebbe esaurirsi per archiviare accuratamente le aree di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8ce00-124">While the operating system accumulates unprocessed desktop image updates, it might run out of space to accurately store the update regions.</span></span> <span data-ttu-id="8ce00-125">In questa situazione, il sistema operativo inizia ad accumulare gli aggiornamenti unendoli con le aree di aggiornamento esistenti per coprire tutti i nuovi aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="8ce00-125">In this situation, the operating system starts to accumulate the updates by coalescing them with existing update regions to cover all new updates.</span></span> <span data-ttu-id="8ce00-126">Di conseguenza, il sistema operativo copre i pixel che non sono ancora stati aggiornati in quel frame.</span><span class="sxs-lookup"><span data-stu-id="8ce00-126">As a result, the operating system covers pixels that it has not actually updated in that frame yet.</span></span> <span data-ttu-id="8ce00-127">Questa situazione, tuttavia, non genera problemi visivi nell'app client perché si riceve l'intera immagine desktop e non solo i pixel aggiornati.</span><span class="sxs-lookup"><span data-stu-id="8ce00-127">But this situation doesn’t produce visual issues on your client app because you receive the entire desktop image and not just the updated pixels.</span></span>

<span data-ttu-id="8ce00-128">Per ricostruire l'immagine desktop corretta, l'app client deve prima elaborare tutte le aree di spostamento e quindi elaborare tutte le aree dirty.</span><span class="sxs-lookup"><span data-stu-id="8ce00-128">To reconstruct the correct desktop image, your client app must first process all the move regions and then process all the dirty regions.</span></span> <span data-ttu-id="8ce00-129">Uno di questi elenchi di aree dirty e di spostamento può essere completamente vuoto.</span><span class="sxs-lookup"><span data-stu-id="8ce00-129">Either of these lists of dirty and move regions can be completely empty.</span></span> <span data-ttu-id="8ce00-130">Il codice di esempio dell' [esempio di duplicazione dei desktop](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) Mostra come elaborare le aree dirty e Move in un singolo frame:</span><span class="sxs-lookup"><span data-stu-id="8ce00-130">The example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to process both the dirty and move regions in a single frame:</span></span>


```C++
//
// Get next frame and write it into Data
//
HRESULT DUPLICATIONMANAGER::GetFrame(_Out_ FRAME_DATA* Data)
{
    HRESULT hr = S_OK;

    IDXGIResource* DesktopResource = NULL;
    DXGI_OUTDUPL_FRAME_INFO FrameInfo;

    //Get new frame
    hr = DeskDupl->AcquireNextFrame(500, &FrameInfo, &DesktopResource);
    if (FAILED(hr))
    {
        if ((hr != DXGI_ERROR_ACCESS_LOST) && (hr != DXGI_ERROR_WAIT_TIMEOUT))
        {
            DisplayErr(L"Failed to acquire next frame in DUPLICATIONMANAGER", L"Error", hr);
        }
        return hr;
    }

    // If still holding old frame, destroy it
    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    // QI for IDXGIResource
    hr = DesktopResource->QueryInterface(__uuidof(ID3D11Texture2D), reinterpret_cast<void **>(&AcquiredDesktopImage));
    DesktopResource->Release();
    DesktopResource = NULL;
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to QI for ID3D11Texture2D from acquired IDXGIResource in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    // Get metadata
    if (FrameInfo.TotalMetadataBufferSize)
    {
        // Old buffer too small
        if (FrameInfo.TotalMetadataBufferSize > MetaDataSize)
        {
            if (MetaDataBuffer)
            {
                delete [] MetaDataBuffer;
                MetaDataBuffer = NULL;
            }
            MetaDataBuffer = new (std::nothrow) BYTE[FrameInfo.TotalMetadataBufferSize];
            if (!MetaDataBuffer)
            {
                DisplayErr(L"Failed to allocate memory for metadata in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
                MetaDataSize = 0;
                Data->MoveCount = 0;
                Data->DirtyCount = 0;
                return E_OUTOFMEMORY;
            }
            MetaDataSize = FrameInfo.TotalMetadataBufferSize;
        }

        UINT BufSize = FrameInfo.TotalMetadataBufferSize;

        // Get move rectangles
        hr = DeskDupl->GetFrameMoveRects(BufSize, reinterpret_cast<DXGI_OUTDUPL_MOVE_RECT*>(MetaDataBuffer), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame move rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->MoveCount = BufSize / sizeof(DXGI_OUTDUPL_MOVE_RECT);

        BYTE* DirtyRects = MetaDataBuffer + BufSize;
        BufSize = FrameInfo.TotalMetadataBufferSize - BufSize;

        // Get dirty rectangles
        hr = DeskDupl->GetFrameDirtyRects(BufSize, reinterpret_cast<RECT*>(DirtyRects), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame dirty rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->DirtyCount = BufSize / sizeof(RECT);

        Data->MetaData = MetaDataBuffer;
    }

    Data->Frame = AcquiredDesktopImage;
    Data->FrameInfo = FrameInfo;

    return hr;
}

//
// Release frame
//
HRESULT DUPLICATIONMANAGER::DoneWithFrame()
{
    HRESULT hr = S_OK;

    hr = DeskDupl->ReleaseFrame();
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to release frame in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    return hr;
}
```



## <a name="rotating-the-desktop-image"></a><span data-ttu-id="8ce00-131">Rotazione dell'immagine desktop</span><span class="sxs-lookup"><span data-stu-id="8ce00-131">Rotating the desktop image</span></span>

<span data-ttu-id="8ce00-132">È necessario aggiungere codice esplicito all'app client di duplicazione desktop per supportare le modalità ruotate.</span><span class="sxs-lookup"><span data-stu-id="8ce00-132">You must add explicit code to your desktop duplication client app to support rotated modes.</span></span> <span data-ttu-id="8ce00-133">In una modalità ruotata la superficie ricevuta da [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) è sempre nell'orientamento non ruotato e l'immagine desktop viene ruotata all'interno della superficie.</span><span class="sxs-lookup"><span data-stu-id="8ce00-133">In a rotated mode, the surface that you receive from [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) is always in the un-rotated orientation, and the desktop image is rotated within the surface.</span></span> <span data-ttu-id="8ce00-134">Se, ad esempio, il desktop è impostato su 768x1024 a 90 gradi di rotazione, **AcquireNextFrame** restituisce una superficie 1024x768 con l'immagine del desktop ruotata al suo interno.</span><span class="sxs-lookup"><span data-stu-id="8ce00-134">For example, if the desktop is set to 768x1024 at 90 degrees rotation, **AcquireNextFrame** returns a 1024x768 surface with the desktop image rotated within it.</span></span> <span data-ttu-id="8ce00-135">Di seguito sono riportati alcuni esempi di rotazione.</span><span class="sxs-lookup"><span data-stu-id="8ce00-135">Here are some rotation examples.</span></span>



| <span data-ttu-id="8ce00-136">Modalità di visualizzazione impostata dal pannello di controllo di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="8ce00-136">Display mode set from display control panel</span></span> | <span data-ttu-id="8ce00-137">Modalità di visualizzazione restituita da GDI o DXGI</span><span class="sxs-lookup"><span data-stu-id="8ce00-137">Display mode returned by GDI or DXGI</span></span> | <span data-ttu-id="8ce00-138">Superficie restituita da [ **AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span><span class="sxs-lookup"><span data-stu-id="8ce00-138">Surface returned from [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span></span>                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce00-139">orizzontale 1024x768</span><span class="sxs-lookup"><span data-stu-id="8ce00-139">1024x768 landscape</span></span>                          | <span data-ttu-id="8ce00-140">rotazione di 1024x768 0 gradi</span><span class="sxs-lookup"><span data-stu-id="8ce00-140">1024x768 0 degree rotation</span></span>           | <span data-ttu-id="8ce00-141">\[nuova riga 1024x768\]</span><span class="sxs-lookup"><span data-stu-id="8ce00-141">1024x768\[newline\]</span></span> ![Desktop remoto non ruotato](images/dxgi-outdupl-0-rotate.png)<br/>            |
| <span data-ttu-id="8ce00-143">verticale 1024x768</span><span class="sxs-lookup"><span data-stu-id="8ce00-143">1024x768 portrait</span></span>                           | <span data-ttu-id="8ce00-144">rotazione 768x1024 90 Degree</span><span class="sxs-lookup"><span data-stu-id="8ce00-144">768x1024 90 degree rotation</span></span>          | <span data-ttu-id="8ce00-145">\[nuova riga 1024x768\]</span><span class="sxs-lookup"><span data-stu-id="8ce00-145">1024x768\[newline\]</span></span> ![Desktop remoto ruotato di 90 gradi](images/dxgi-outdupl-90-rotate.png)<br/>   |
| <span data-ttu-id="8ce00-147">orizzontale 1024x768 (capovolto)</span><span class="sxs-lookup"><span data-stu-id="8ce00-147">1024x768 landscape (flipped)</span></span>                | <span data-ttu-id="8ce00-148">rotazione di 180 gradi 1024x768</span><span class="sxs-lookup"><span data-stu-id="8ce00-148">1024x768 180 degree rotation</span></span>         | <span data-ttu-id="8ce00-149">\[nuova riga 1024x768\]</span><span class="sxs-lookup"><span data-stu-id="8ce00-149">1024x768\[newline\]</span></span> ![Desktop remoto ruotato di 180 gradi](images/dxgi-outdupl-180-rotate.png)<br/> |
| <span data-ttu-id="8ce00-151">verticale da 1024x768 (capovolto)</span><span class="sxs-lookup"><span data-stu-id="8ce00-151">1024x768 portrait (flipped)</span></span>                 | <span data-ttu-id="8ce00-152">rotazione 768x1024 270 degree</span><span class="sxs-lookup"><span data-stu-id="8ce00-152">768x1024 270 degree rotation</span></span>         | <span data-ttu-id="8ce00-153">\[nuova riga 1024x768\]</span><span class="sxs-lookup"><span data-stu-id="8ce00-153">1024x768\[newline\]</span></span> ![Desktop remoto ruotato di 270 gradi](images/dxgi-outdupl-270-rotate.png)<br/> |



 

<span data-ttu-id="8ce00-155">Il codice nell'app client di duplicazione desktop deve ruotare l'immagine desktop in modo appropriato prima di visualizzare l'immagine del desktop.</span><span class="sxs-lookup"><span data-stu-id="8ce00-155">The code in your desktop duplication client app must rotate the desktop image appropriately before you display the desktop image.</span></span>

> [!Note]  
> <span data-ttu-id="8ce00-156">Negli scenari con più monitor è possibile ruotare l'immagine del desktop per ogni monitoraggio in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="8ce00-156">In multi-monitor scenarios, you can rotate the desktop image for each monitor independently.</span></span>

 

## <a name="updating-the-desktop-pointer"></a><span data-ttu-id="8ce00-157">Aggiornamento del puntatore del desktop</span><span class="sxs-lookup"><span data-stu-id="8ce00-157">Updating the desktop pointer</span></span>

<span data-ttu-id="8ce00-158">È necessario usare l'API di duplicazione desktop per determinare se l'app client deve disegnare la forma puntatore del mouse sull'immagine desktop.</span><span class="sxs-lookup"><span data-stu-id="8ce00-158">You need to use the desktop duplication API to determine if your client app must draw the mouse pointer shape onto the desktop image.</span></span> <span data-ttu-id="8ce00-159">Il puntatore del mouse è già disegnato nell'immagine desktop fornita da [**IDXGIOutputDuplication:: AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) oppure il puntatore del mouse è separato dall'immagine desktop.</span><span class="sxs-lookup"><span data-stu-id="8ce00-159">Either the mouse pointer is already drawn onto the desktop image that [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) provides or the mouse pointer is separate from the desktop image.</span></span> <span data-ttu-id="8ce00-160">Se il puntatore del mouse viene disegnato sull'immagine desktop, i dati di posizione del puntatore segnalati da **AcquireNextFrame** (nel membro **PointerPosition** di [**DXGI \_ OUTDUPL \_ frame \_ info**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) a cui punta il parametro *pFrameInfo* ) indicano che un puntatore separato non è visibile.</span><span class="sxs-lookup"><span data-stu-id="8ce00-160">If the mouse pointer is drawn onto the desktop image, the pointer position data that is reported by **AcquireNextFrame** (in the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) that the *pFrameInfo* parameter points to) indicates that a separate pointer isn’t visible.</span></span> <span data-ttu-id="8ce00-161">Se la scheda grafica sovrappone il puntatore del mouse sulla parte superiore dell'immagine del desktop, **AcquireNextFrame** segnala che è visibile un puntatore separato.</span><span class="sxs-lookup"><span data-stu-id="8ce00-161">If the graphics adapter overlays the mouse pointer on top of the desktop image, **AcquireNextFrame** reports that a separate pointer is visible.</span></span> <span data-ttu-id="8ce00-162">Quindi, l'app client deve disegnare la forma puntatore del mouse sull'immagine desktop per rappresentare in modo accurato ciò che l'utente corrente vedrà sul monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="8ce00-162">So, your client app must draw the mouse pointer shape onto the desktop image to accurately represent what the current user will see on their monitor.</span></span>

<span data-ttu-id="8ce00-163">Per creare il puntatore del mouse sul desktop, usare il membro **PointerPosition** di [**DXGI \_ OUTDUPL \_ frame \_ info**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) dal parametro *pFrameInfo* di [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) per determinare la posizione in cui posizionare l'angolo superiore sinistro del puntatore del mouse sull'immagine desktop.</span><span class="sxs-lookup"><span data-stu-id="8ce00-163">To draw the desktop’s mouse pointer, use the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) from the *pFrameInfo* parameter of [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) to determine where to locate the top left hand corner of the mouse pointer on the desktop image.</span></span> <span data-ttu-id="8ce00-164">Quando si crea il primo frame, è necessario usare il metodo [**IDXGIOutputDuplication:: GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) per ottenere informazioni sulla forma del puntatore del mouse.</span><span class="sxs-lookup"><span data-stu-id="8ce00-164">When you draw the first frame, you must use the [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) method to obtain info about the shape of the mouse pointer.</span></span> <span data-ttu-id="8ce00-165">Ogni chiamata a **AcquireNextFrame** per ottenere il frame successivo fornisce anche la posizione corrente del puntatore per quel frame.</span><span class="sxs-lookup"><span data-stu-id="8ce00-165">Each call to **AcquireNextFrame** to get the next frame also provides the current pointer position for that frame.</span></span> <span data-ttu-id="8ce00-166">D'altra parte, è necessario usare nuovamente **GetFramePointerShape** solo se la forma viene modificata.</span><span class="sxs-lookup"><span data-stu-id="8ce00-166">On the other hand, you need to use **GetFramePointerShape** again only if the shape changes.</span></span> <span data-ttu-id="8ce00-167">Quindi, conserva una copia dell'ultima immagine puntatore e la usa per disegnare sul desktop, a meno che la forma del puntatore del mouse non venga modificata.</span><span class="sxs-lookup"><span data-stu-id="8ce00-167">So, keep a copy of the last pointer image and use it to draw on the desktop unless the shape of the mouse pointer changes.</span></span>

> [!Note]  
> <span data-ttu-id="8ce00-168">Insieme all'immagine della forma puntatore, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) fornisce le dimensioni della posizione sensibile.</span><span class="sxs-lookup"><span data-stu-id="8ce00-168">Together with the pointer shape image, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) provides the size of the hot spot location.</span></span> <span data-ttu-id="8ce00-169">L'area sensibile viene fornita solo a scopo informativo.</span><span class="sxs-lookup"><span data-stu-id="8ce00-169">The hot spot is given for informational purposes only.</span></span> <span data-ttu-id="8ce00-170">La posizione in cui creare l'immagine del puntatore è indipendente dall'area sensibile.</span><span class="sxs-lookup"><span data-stu-id="8ce00-170">The location of where to draw the pointer image is independent to the hotspot.</span></span>

 

<span data-ttu-id="8ce00-171">Questo esempio di codice dell' [esempio di duplicazione dei desktop](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) Mostra come ottenere la forma del puntatore del mouse:</span><span class="sxs-lookup"><span data-stu-id="8ce00-171">This example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to get the mouse pointer shape:</span></span>


```C++
//
// Retrieves mouse info and write it into PtrInfo
//
HRESULT DUPLICATIONMANAGER::GetMouse(_Out_ PTR_INFO* PtrInfo, _In_ DXGI_OUTDUPL_FRAME_INFO* FrameInfo, INT OffsetX, INT OffsetY)
{
    HRESULT hr = S_OK;

    // A non-zero mouse update timestamp indicates that there is a mouse position update and optionally a shape change
    if (FrameInfo->LastMouseUpdateTime.QuadPart == 0)
    {
        return hr;
    }

    bool UpdatePosition = true;

    // Make sure we don't update pointer position wrongly
    // If pointer is invisible, make sure we did not get an update from another output that the last time that said pointer
    // was visible, if so, don't set it to invisible or update.
    if (!FrameInfo->PointerPosition.Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber))
    {
        UpdatePosition = false;
    }

    // If two outputs both say they have a visible, only update if new update has newer timestamp
    if (FrameInfo->PointerPosition.Visible && PtrInfo->Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber) && (PtrInfo->LastTimeStamp.QuadPart > FrameInfo->LastMouseUpdateTime.QuadPart))
    {
        UpdatePosition = false;
    }

    // Update position
    if (UpdatePosition)
    {
        PtrInfo->Position.x = FrameInfo->PointerPosition.Position.x + OutputDesc.DesktopCoordinates.left - OffsetX;
        PtrInfo->Position.y = FrameInfo->PointerPosition.Position.y + OutputDesc.DesktopCoordinates.top - OffsetY;
        PtrInfo->WhoUpdatedPositionLast = OutputNumber;
        PtrInfo->LastTimeStamp = FrameInfo->LastMouseUpdateTime;
        PtrInfo->Visible = FrameInfo->PointerPosition.Visible != 0;
    }

    // No new shape
    if (FrameInfo->PointerShapeBufferSize == 0)
    {
        return hr;
    }

    // Old buffer too small
    if (FrameInfo->PointerShapeBufferSize > PtrInfo->BufferSize)
    {
        if (PtrInfo->PtrShapeBuffer)
        {
            delete [] PtrInfo->PtrShapeBuffer;
            PtrInfo->PtrShapeBuffer = NULL;
        }
        PtrInfo->PtrShapeBuffer = new (std::nothrow) BYTE[FrameInfo->PointerShapeBufferSize];
        if (!PtrInfo->PtrShapeBuffer)
        {
            DisplayErr(L"Failed to allocate memory for pointer shape in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
            PtrInfo->BufferSize = 0;
            return E_OUTOFMEMORY;
        }

        // Update buffer size
        PtrInfo->BufferSize = FrameInfo->PointerShapeBufferSize;
    }

    UINT BufferSizeRequired;
    // Get shape
    hr = DeskDupl->GetFramePointerShape(FrameInfo->PointerShapeBufferSize, reinterpret_cast<VOID*>(PtrInfo->PtrShapeBuffer), &BufferSizeRequired, &(PtrInfo->ShapeInfo));
    if (FAILED(hr))
    {
        if (hr != DXGI_ERROR_ACCESS_LOST)
        {
            DisplayErr(L"Failed to get frame pointer shape in DUPLICATIONMANAGER", L"Error", hr);
        }
        delete [] PtrInfo->PtrShapeBuffer;
        PtrInfo->PtrShapeBuffer = NULL;
        PtrInfo->BufferSize = 0;
        return hr;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="8ce00-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ce00-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ce00-173">Miglioramenti di DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="8ce00-173">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
