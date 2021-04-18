---
description: Viene descritto come utilizzare le sovrapposizioni hardware in Direct3D 9.
ms.assetid: fa9d5bf5-4c0f-471a-b639-d329b0cd89a4
title: Supporto per overlay hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcae33cdf55de59bdcd074829d52b4c1c43ea5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308767"
---
# <a name="hardware-overlay-support"></a><span data-ttu-id="26617-103">Supporto per overlay hardware</span><span class="sxs-lookup"><span data-stu-id="26617-103">Hardware Overlay Support</span></span>

<span data-ttu-id="26617-104">Una sovrapposizione hardware è un'area dedicata di memoria video che può essere sovrapposta all'area primaria.</span><span class="sxs-lookup"><span data-stu-id="26617-104">A hardware overlay is a dedicated area of video memory that can be overlayed on the primary surface.</span></span> <span data-ttu-id="26617-105">Non viene eseguita alcuna copia quando viene visualizzata la sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="26617-105">No copy is performed when the overlay is displayed.</span></span> <span data-ttu-id="26617-106">L'operazione di sovrapposizione viene eseguita in hardware, senza modificare i dati nell'area primaria.</span><span class="sxs-lookup"><span data-stu-id="26617-106">The overlay operation is performed in hardware, without modifying the data in the primary surface.</span></span>

<span data-ttu-id="26617-107">L'uso di sovrimpressioni hardware per la riproduzione video è stato comune nelle versioni precedenti di Windows, perché le sovrapposizioni sono efficienti per contenuti video con una frequenza elevata di fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="26617-107">The use of hardware overlays for video playback was common in earlier versions of Windows, because overlays are efficient for video content with a high frame rate.</span></span> <span data-ttu-id="26617-108">A partire da Windows 7, Direct3D 9 supporta le sovrapposizioni hardware.</span><span class="sxs-lookup"><span data-stu-id="26617-108">Starting in Windows 7, Direct3D 9 supports hardware overlays.</span></span> <span data-ttu-id="26617-109">Questo supporto è concepito principalmente per la riproduzione di video e presenta alcune differenze rispetto alle API DirectDraw precedenti:</span><span class="sxs-lookup"><span data-stu-id="26617-109">This support is intended primarily for video playback, and differs in some respects from earlier DirectDraw APIs:</span></span>

-   <span data-ttu-id="26617-110">Non è possibile compattare, eseguire il mirroring o deinterlacciare la sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="26617-110">The overlay cannot be shrunk, mirrored, or deinterlaced.</span></span>
-   <span data-ttu-id="26617-111">Le chiavi di colore di origine e la fusione alfa non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="26617-111">Source color keys and alpha blending are not supported.</span></span>
-   <span data-ttu-id="26617-112">Le sovrapposizioni possono essere allungate se l'hardware sovrapposto lo supporta.</span><span class="sxs-lookup"><span data-stu-id="26617-112">Overlays can be stretched if the overlay hardware supports it.</span></span> <span data-ttu-id="26617-113">In caso contrario, l'estensione non è supportata.</span><span class="sxs-lookup"><span data-stu-id="26617-113">Otherwise, stretching is not supported.</span></span> <span data-ttu-id="26617-114">In pratica, non tutti i driver grafici supportano l'estensione.</span><span class="sxs-lookup"><span data-stu-id="26617-114">In practice, not all graphics drivers support stretching.</span></span>
-   <span data-ttu-id="26617-115">Ogni dispositivo supporta al massimo una sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="26617-115">Each device supports at most one overlay.</span></span>
-   <span data-ttu-id="26617-116">La sovrapposizione viene eseguita utilizzando una chiave di colore di destinazione, ma il runtime Direct3D seleziona automaticamente il colore e disegna il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="26617-116">Overlay is performed using a destination color key, but the Direct3D runtime automatically selects the color and draws the destination rectangle.</span></span> <span data-ttu-id="26617-117">Direct3D rileva automaticamente la posizione della finestra e aggiorna la posizione di sovrapposizione ogni volta che viene chiamato **PresentEx** .</span><span class="sxs-lookup"><span data-stu-id="26617-117">Direct3D automatically tracks the position of the window and updates the overlay position whenever the **PresentEx** is called.</span></span>

### <a name="creating-a-hardware-overlay-surface"></a><span data-ttu-id="26617-118">Creazione di una superficie di sovrapposizione hardware</span><span class="sxs-lookup"><span data-stu-id="26617-118">Creating a Hardware Overlay Surface</span></span>

<span data-ttu-id="26617-119">Per eseguire una query per il supporto della sovrimpressione, chiamare **IDirect3D9:: GetDeviceCaps**.</span><span class="sxs-lookup"><span data-stu-id="26617-119">To query for overlay support, call **IDirect3D9::GetDeviceCaps**.</span></span> <span data-ttu-id="26617-120">Se il driver supporta la sovrimpressione hardware, il flag **D3DCAPS \_ overlay** viene impostato in **D3DCAPS9. Membro Caps** .</span><span class="sxs-lookup"><span data-stu-id="26617-120">If the driver supports hardware overlay, the **D3DCAPS\_OVERLAY** flag is set in the **D3DCAPS9.Caps** member.</span></span>

<span data-ttu-id="26617-121">Per determinare se un formato di sovrimpressione specifico è supportato per una determinata modalità di visualizzazione, chiamare [**IDirect3D9ExOverlayExtension:: CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).</span><span class="sxs-lookup"><span data-stu-id="26617-121">To find out whether a specific overlay format is supported for a given display mode, call [**IDirect3D9ExOverlayExtension::CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).</span></span>

<span data-ttu-id="26617-122">Per creare la sovrimpressione, chiamare **IDirect3D9Ex:: CreateDeviceEx** e specificare l'effetto di swap **\_ overlay D3DSWAPEFFECT** .</span><span class="sxs-lookup"><span data-stu-id="26617-122">To create the overlay, call **IDirect3D9Ex::CreateDeviceEx** and specify the **D3DSWAPEFFECT\_OVERLAY** swap effect.</span></span> <span data-ttu-id="26617-123">Il buffer nascosto può usare un formato non RGB se l'hardware lo supporta.</span><span class="sxs-lookup"><span data-stu-id="26617-123">The back buffer can use a non-RGB format if the hardware supports it.</span></span>

<span data-ttu-id="26617-124">Le superfici sovrapposte presentano le limitazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="26617-124">Overlay surfaces have the following limitations:</span></span>

-   <span data-ttu-id="26617-125">L'applicazione non può creare più di una catena di scambio overlay.</span><span class="sxs-lookup"><span data-stu-id="26617-125">The application cannot create more than one overlay swap chain.</span></span>
-   <span data-ttu-id="26617-126">La sovrimpressione deve essere utilizzata in modalità finestra.</span><span class="sxs-lookup"><span data-stu-id="26617-126">The overlay must be used in windowed mode.</span></span> <span data-ttu-id="26617-127">Non può essere usato in modalità a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="26617-127">It cannot be used in fullscreen mode.</span></span>
-   <span data-ttu-id="26617-128">L'effetto di swap overlay deve essere utilizzato con l'interfaccia **IDirect3DDevice9Ex** .</span><span class="sxs-lookup"><span data-stu-id="26617-128">The overlay swap effect must be used with the **IDirect3DDevice9Ex** interface.</span></span> <span data-ttu-id="26617-129">Non è supportata per **IDirect3DDevice9**.</span><span class="sxs-lookup"><span data-stu-id="26617-129">It is not supported for **IDirect3DDevice9**.</span></span>
-   <span data-ttu-id="26617-130">Non è possibile usare il campionamento multiplo.</span><span class="sxs-lookup"><span data-stu-id="26617-130">Multisampling cannot be used.</span></span>
-   <span data-ttu-id="26617-131">I flag **D3DPRESENT \_ DONOTFLIP** e **D3DPRESENT \_ FLIPRESTART** non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="26617-131">The **D3DPRESENT\_DONOTFLIP** and **D3DPRESENT\_FLIPRESTART** flags are not supported.</span></span>
-   <span data-ttu-id="26617-132">Le statistiche di presentazione non sono disponibili per la superficie della sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="26617-132">Presentation statistics are not available for the overlay surface.</span></span>

<span data-ttu-id="26617-133">Se l'hardware non supporta l'estensione, si consiglia di creare una catena di scambio fino alla modalità di visualizzazione, in modo che la finestra possa essere ridimensionata in qualsiasi dimensione.</span><span class="sxs-lookup"><span data-stu-id="26617-133">If the hardware does not support stretching, it is recommended to create a swap chain as large as the display mode, so that the window can be resized to any dimensions.</span></span> <span data-ttu-id="26617-134">La ricreazione della catena di scambio non è un modo ottimale per gestire il ridimensionamento della finestra, perché può causare gravi artefatti di rendering.</span><span class="sxs-lookup"><span data-stu-id="26617-134">Recreating the swap chain is not an optimal way to handle resizing the window, because it can cause severe rendering artifacts.</span></span> <span data-ttu-id="26617-135">Inoltre, a causa del modo in cui la GPU gestisce la memoria sovrapposta, la ricreazione della catena di scambio può causare l'esaurimento della memoria video da parte di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="26617-135">Also, because of the way the GPU manages the overlay memory, recreating the swap chain can potentially cause an application to run out of video memory.</span></span>

### <a name="new-d3dpresent_parameters-flags"></a><span data-ttu-id="26617-136">Nuovi \_ flag dei parametri D3DPRESENT</span><span class="sxs-lookup"><span data-stu-id="26617-136">New D3DPRESENT\_PARAMETERS Flags</span></span>

<span data-ttu-id="26617-137">I flag **di \_ parametri D3DPRESENT** seguenti sono definiti per la creazione di sovrimpressioni.</span><span class="sxs-lookup"><span data-stu-id="26617-137">The following **D3DPRESENT\_PARAMETERS** flags are defined for creating overlays.</span></span>



| <span data-ttu-id="26617-138">Flag</span><span class="sxs-lookup"><span data-stu-id="26617-138">Flag</span></span>                                      | <span data-ttu-id="26617-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26617-139">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26617-140">**D3DPRESENTFLAG \_ overlay \_ LIMITEDRGB**</span><span class="sxs-lookup"><span data-stu-id="26617-140">**D3DPRESENTFLAG\_OVERLAY\_LIMITEDRGB**</span></span>   | <span data-ttu-id="26617-141">L'intervallo RGB è 16 – 235.</span><span class="sxs-lookup"><span data-stu-id="26617-141">The RGB range is 16–235.</span></span> <span data-ttu-id="26617-142">Il valore predefinito è 0 – 255.</span><span class="sxs-lookup"><span data-stu-id="26617-142">The default is 0–255.</span></span> <br/> <span data-ttu-id="26617-143">Richiede la **funzionalità \_ LIMITEDRANGERGB di D3DOVERLAYCAPS** .</span><span class="sxs-lookup"><span data-stu-id="26617-143">Requires the **D3DOVERLAYCAPS\_LIMITEDRANGERGB** capability.</span></span><br/>                                                 |
| <span data-ttu-id="26617-144">**D3DPRESENTFLAG \_ overlay \_ YCbCr \_ BT709**</span><span class="sxs-lookup"><span data-stu-id="26617-144">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_BT709**</span></span> | <span data-ttu-id="26617-145">I colori YUV usano la definizione BT. 709.</span><span class="sxs-lookup"><span data-stu-id="26617-145">YUV colors use the BT.709 definition.</span></span> <span data-ttu-id="26617-146">Il valore predefinito è BT. 601.</span><span class="sxs-lookup"><span data-stu-id="26617-146">The default is BT.601.</span></span> <br/> <span data-ttu-id="26617-147">Richiede la **funzionalità \_ \_ BT709 YCbCr di D3DOVERLAYCAPS** .</span><span class="sxs-lookup"><span data-stu-id="26617-147">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT709** capability.</span></span><br/>                                      |
| <span data-ttu-id="26617-148">**D3DPRESENTFLAG \_ overlay \_ YCbCr \_ xvYCC**</span><span class="sxs-lookup"><span data-stu-id="26617-148">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_xvYCC**</span></span> | <span data-ttu-id="26617-149">Restituire i dati usando Extended YCbCr (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="26617-149">Output the data by using extended YCbCr (xvYCC).</span></span><br/> <span data-ttu-id="26617-150">Richiede la funzionalità **D3DOVERLAYCAPS \_ YCbCr \_ BT601 \_ xvYCC** o D3DOVERLAYCAPS YCbCr BT709 xvYCC. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="26617-150">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT601\_xvYCC** or **D3DOVERLAYCAPS\_YCbCr\_BT709\_xvYCC** capability.</span></span><br/> |



 

### <a name="using-hardware-overlays"></a><span data-ttu-id="26617-151">Uso di sovrimpressioni hardware</span><span class="sxs-lookup"><span data-stu-id="26617-151">Using Hardware Overlays</span></span>

<span data-ttu-id="26617-152">Per visualizzare la superficie della sovrimpressione, l'applicazione chiama **IDirect3DDevice9Ex::P resentex**.</span><span class="sxs-lookup"><span data-stu-id="26617-152">To display the overlay surface, the application calls **IDirect3DDevice9Ex::PresentEx**.</span></span> <span data-ttu-id="26617-153">Il runtime Direct3D disegna automaticamente la chiave di colore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="26617-153">The Direct3D runtime automatically draws the destination color key.</span></span>

<span data-ttu-id="26617-154">Per le sovrapposizioni vengono definiti i flag **PresentEx** seguenti.</span><span class="sxs-lookup"><span data-stu-id="26617-154">The following **PresentEx** flags are defined for overlays.</span></span>



| <span data-ttu-id="26617-155">Flag</span><span class="sxs-lookup"><span data-stu-id="26617-155">Flag</span></span>                              | <span data-ttu-id="26617-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26617-156">Description</span></span>                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26617-157">**\_UPDATECOLORKEY D3DPRESENT**</span><span class="sxs-lookup"><span data-stu-id="26617-157">**D3DPRESENT\_UPDATECOLORKEY**</span></span>    | <span data-ttu-id="26617-158">Impostare questo flag se la composizione di Gestione finestre desktop (DWM) è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="26617-158">Set this flag if Desktop Window Manager (DWM) composition is disabled.</span></span> <span data-ttu-id="26617-159">Questo flag fa in modo che Direct3D ridisegni la chiave di colore.</span><span class="sxs-lookup"><span data-stu-id="26617-159">This flag causes Direct3D to redraw the color key.</span></span><br/> <span data-ttu-id="26617-160">Se DWM è abilitato, questo flag non è necessario perché Direct3D disegna la chiave di colore una volta sulla superficie utilizzata da DWM per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="26617-160">If DWM is enabled, this flag is not required, because Direct3D draws the color key once on the surface that DWM uses for redirection.</span></span><br/> |
| <span data-ttu-id="26617-161">**\_HIDEOVERLAY D3DPRESENT**</span><span class="sxs-lookup"><span data-stu-id="26617-161">**D3DPRESENT\_HIDEOVERLAY**</span></span>       | <span data-ttu-id="26617-162">Nasconde la sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="26617-162">Hides the overlay.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="26617-163">**\_UPDATEOVERLAYONLY D3DPRESENT**</span><span class="sxs-lookup"><span data-stu-id="26617-163">**D3DPRESENT\_UPDATEOVERLAYONLY**</span></span> | <span data-ttu-id="26617-164">Aggiorna la sovrimpressione senza modificare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="26617-164">Updates the overlay without changing the contents.</span></span><br/> <span data-ttu-id="26617-165">Questo flag è utile se la finestra si sposta mentre il video è sospeso.</span><span class="sxs-lookup"><span data-stu-id="26617-165">This flag is useful if the window moves while the video is paused.</span></span><br/>                                                                                                                                           |



 

<span data-ttu-id="26617-166">Un'applicazione deve essere preparata a gestire i casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="26617-166">An application should be prepared to handle the following cases:</span></span>

-   <span data-ttu-id="26617-167">Se un'altra applicazione usa la sovrimpressione, **PresentEx** restituisce **D3DERR \_ NOTAVAILABLE**.</span><span class="sxs-lookup"><span data-stu-id="26617-167">If another application is using the overlay, **PresentEx** returns **D3DERR\_NOTAVAILABLE**.</span></span>
-   <span data-ttu-id="26617-168">Se la finestra viene spostata in un altro monitor, l'applicazione deve ricreare la catena di scambio.</span><span class="sxs-lookup"><span data-stu-id="26617-168">If the window is moved to another monitor, the application must recreate the swap chain.</span></span> <span data-ttu-id="26617-169">In caso contrario, se l'applicazione chiama **PresentEx** per visualizzare la sovrimpressione su un altro monitor, **PresentEx** restituisce **D3DERR \_ INVALIDDEVICE**.</span><span class="sxs-lookup"><span data-stu-id="26617-169">Otherwise, if the application calls **PresentEx** to display the overlay on a different monitor, **PresentEx** returns **D3DERR\_INVALIDDEVICE**.</span></span>
-   <span data-ttu-id="26617-170">Se la modalità di visualizzazione viene modificata, Direct3D tenta di ripristinare la sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="26617-170">If the display mode changes, Direct3D attempts to restore the overlay.</span></span> <span data-ttu-id="26617-171">Se la nuova modalità non supporta la sovrimpressione, **PresentEx** restituisce **D3DERR \_ UNSUPPORTEDOVERLAY**.</span><span class="sxs-lookup"><span data-stu-id="26617-171">If the new mode does not support the overlay, **PresentEx** returns **D3DERR\_UNSUPPORTEDOVERLAY**.</span></span>

### <a name="example-code"></a><span data-ttu-id="26617-172">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="26617-172">Example Code</span></span>

<span data-ttu-id="26617-173">Nell'esempio seguente viene illustrato come creare una superficie sovrapposta.</span><span class="sxs-lookup"><span data-stu-id="26617-173">The following example shows how to create an overlay surface.</span></span>


```C++
const UINT VIDEO_WIDTH = 256;
const UINT VIDEO_HEIGHT = 256;

HRESULT CreateHWOverlay(
    HWND hwnd, 
    IDirect3D9Ex *pD3D, 
    IDirect3DDevice9Ex **ppDevice
    )
{
    *ppDevice = NULL;

    D3DCAPS9                caps;
    ZeroMemory(&caps, sizeof(caps));

    HRESULT hr = pD3D->GetDeviceCaps(
        D3DADAPTER_DEFAULT,
        D3DDEVTYPE_HAL,
        &caps
        );

    if (FAILED(hr))
    {
        return hr;
    }

    // Check if overlay is supported.
    if (!(caps.Caps & D3DCAPS_OVERLAY))
    {
        return D3DERR_UNSUPPORTEDOVERLAY;
    }

    D3DOVERLAYCAPS          overlayCaps = { 0 };

    IDirect3DDevice9Ex           *pDevice = NULL;
    IDirect3D9ExOverlayExtension *pOverlay = NULL;

    // Check specific overlay capabilities.
    hr = pD3D->QueryInterface(IID_PPV_ARGS(&pOverlay));

    if (SUCCEEDED(hr))
    {
        hr = pOverlay->CheckDeviceOverlayType(
            D3DADAPTER_DEFAULT,
            D3DDEVTYPE_HAL,
            VIDEO_WIDTH,
            VIDEO_HEIGHT,
            D3DFMT_X8R8G8B8,
            NULL,
            D3DDISPLAYROTATION_IDENTITY,
            &overlayCaps
            );
    }

    // Create the overlay.
    if (SUCCEEDED(hr))
    {

        DWORD flags =   D3DCREATE_FPU_PRESERVE | 
                        D3DCREATE_MULTITHREADED | 
                        D3DCREATE_SOFTWARE_VERTEXPROCESSING;

        
        D3DPRESENT_PARAMETERS   pp = { 0 };

        pp.BackBufferWidth = overlayCaps.MaxOverlayDisplayWidth;
        pp.BackBufferHeight = overlayCaps.MaxOverlayDisplayHeight;
        pp.BackBufferFormat = D3DFMT_X8R8G8B8;
        pp.SwapEffect = D3DSWAPEFFECT_OVERLAY;
        pp.hDeviceWindow = hwnd;
        pp.Windowed = TRUE;
        pp.Flags = D3DPRESENTFLAG_VIDEO;
        pp.FullScreen_RefreshRateInHz = D3DPRESENT_RATE_DEFAULT;
        pp.PresentationInterval       = D3DPRESENT_INTERVAL_ONE;

        hr = pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL,
            NULL, flags, &pp, NULL, &pDevice);
    }

    if (SUCCEEDED(hr))
    {
        (*ppDevice) = pDevice;
        (*ppDevice)->AddRef();
    }

    SafeRelease(&pD3D);
    SafeRelease(&pDevice);
    SafeRelease(&pOverlay);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="26617-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26617-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26617-175">API video Direct3D</span><span class="sxs-lookup"><span data-stu-id="26617-175">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 




