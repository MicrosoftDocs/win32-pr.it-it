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
# <a name="hardware-overlay-support"></a>Supporto per overlay hardware

Una sovrapposizione hardware è un'area dedicata di memoria video che può essere sovrapposta all'area primaria. Non viene eseguita alcuna copia quando viene visualizzata la sovrimpressione. L'operazione di sovrapposizione viene eseguita in hardware, senza modificare i dati nell'area primaria.

L'uso di sovrimpressioni hardware per la riproduzione video è stato comune nelle versioni precedenti di Windows, perché le sovrapposizioni sono efficienti per contenuti video con una frequenza elevata di fotogrammi. A partire da Windows 7, Direct3D 9 supporta le sovrapposizioni hardware. Questo supporto è concepito principalmente per la riproduzione di video e presenta alcune differenze rispetto alle API DirectDraw precedenti:

-   Non è possibile compattare, eseguire il mirroring o deinterlacciare la sovrimpressione.
-   Le chiavi di colore di origine e la fusione alfa non sono supportate.
-   Le sovrapposizioni possono essere allungate se l'hardware sovrapposto lo supporta. In caso contrario, l'estensione non è supportata. In pratica, non tutti i driver grafici supportano l'estensione.
-   Ogni dispositivo supporta al massimo una sovrimpressione.
-   La sovrapposizione viene eseguita utilizzando una chiave di colore di destinazione, ma il runtime Direct3D seleziona automaticamente il colore e disegna il rettangolo di destinazione. Direct3D rileva automaticamente la posizione della finestra e aggiorna la posizione di sovrapposizione ogni volta che viene chiamato **PresentEx** .

### <a name="creating-a-hardware-overlay-surface"></a>Creazione di una superficie di sovrapposizione hardware

Per eseguire una query per il supporto della sovrimpressione, chiamare **IDirect3D9:: GetDeviceCaps**. Se il driver supporta la sovrimpressione hardware, il flag **D3DCAPS \_ overlay** viene impostato in **D3DCAPS9. Membro Caps** .

Per determinare se un formato di sovrimpressione specifico è supportato per una determinata modalità di visualizzazione, chiamare [**IDirect3D9ExOverlayExtension:: CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).

Per creare la sovrimpressione, chiamare **IDirect3D9Ex:: CreateDeviceEx** e specificare l'effetto di swap **\_ overlay D3DSWAPEFFECT** . Il buffer nascosto può usare un formato non RGB se l'hardware lo supporta.

Le superfici sovrapposte presentano le limitazioni seguenti:

-   L'applicazione non può creare più di una catena di scambio overlay.
-   La sovrimpressione deve essere utilizzata in modalità finestra. Non può essere usato in modalità a schermo intero.
-   L'effetto di swap overlay deve essere utilizzato con l'interfaccia **IDirect3DDevice9Ex** . Non è supportata per **IDirect3DDevice9**.
-   Non è possibile usare il campionamento multiplo.
-   I flag **D3DPRESENT \_ DONOTFLIP** e **D3DPRESENT \_ FLIPRESTART** non sono supportati.
-   Le statistiche di presentazione non sono disponibili per la superficie della sovrimpressione.

Se l'hardware non supporta l'estensione, si consiglia di creare una catena di scambio fino alla modalità di visualizzazione, in modo che la finestra possa essere ridimensionata in qualsiasi dimensione. La ricreazione della catena di scambio non è un modo ottimale per gestire il ridimensionamento della finestra, perché può causare gravi artefatti di rendering. Inoltre, a causa del modo in cui la GPU gestisce la memoria sovrapposta, la ricreazione della catena di scambio può causare l'esaurimento della memoria video da parte di un'applicazione.

### <a name="new-d3dpresent_parameters-flags"></a>Nuovi \_ flag dei parametri D3DPRESENT

I flag **di \_ parametri D3DPRESENT** seguenti sono definiti per la creazione di sovrimpressioni.



| Flag                                      | Descrizione                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENTFLAG \_ overlay \_ LIMITEDRGB**   | L'intervallo RGB è 16 – 235. Il valore predefinito è 0 – 255. <br/> Richiede la **funzionalità \_ LIMITEDRANGERGB di D3DOVERLAYCAPS** .<br/>                                                 |
| **D3DPRESENTFLAG \_ overlay \_ YCbCr \_ BT709** | I colori YUV usano la definizione BT. 709. Il valore predefinito è BT. 601. <br/> Richiede la **funzionalità \_ \_ BT709 YCbCr di D3DOVERLAYCAPS** .<br/>                                      |
| **D3DPRESENTFLAG \_ overlay \_ YCbCr \_ xvYCC** | Restituire i dati usando Extended YCbCr (xvYCC).<br/> Richiede la funzionalità **D3DOVERLAYCAPS \_ YCbCr \_ BT601 \_ xvYCC** o D3DOVERLAYCAPS YCbCr BT709 xvYCC. **\_ \_ \_**<br/> |



 

### <a name="using-hardware-overlays"></a>Uso di sovrimpressioni hardware

Per visualizzare la superficie della sovrimpressione, l'applicazione chiama **IDirect3DDevice9Ex::P resentex**. Il runtime Direct3D disegna automaticamente la chiave di colore di destinazione.

Per le sovrapposizioni vengono definiti i flag **PresentEx** seguenti.



| Flag                              | Descrizione                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_UPDATECOLORKEY D3DPRESENT**    | Impostare questo flag se la composizione di Gestione finestre desktop (DWM) è disabilitata. Questo flag fa in modo che Direct3D ridisegni la chiave di colore.<br/> Se DWM è abilitato, questo flag non è necessario perché Direct3D disegna la chiave di colore una volta sulla superficie utilizzata da DWM per il reindirizzamento.<br/> |
| **\_HIDEOVERLAY D3DPRESENT**       | Nasconde la sovrimpressione.                                                                                                                                                                                                                                                                    |
| **\_UPDATEOVERLAYONLY D3DPRESENT** | Aggiorna la sovrimpressione senza modificare il contenuto.<br/> Questo flag è utile se la finestra si sposta mentre il video è sospeso.<br/>                                                                                                                                           |



 

Un'applicazione deve essere preparata a gestire i casi seguenti:

-   Se un'altra applicazione usa la sovrimpressione, **PresentEx** restituisce **D3DERR \_ NOTAVAILABLE**.
-   Se la finestra viene spostata in un altro monitor, l'applicazione deve ricreare la catena di scambio. In caso contrario, se l'applicazione chiama **PresentEx** per visualizzare la sovrimpressione su un altro monitor, **PresentEx** restituisce **D3DERR \_ INVALIDDEVICE**.
-   Se la modalità di visualizzazione viene modificata, Direct3D tenta di ripristinare la sovrimpressione. Se la nuova modalità non supporta la sovrimpressione, **PresentEx** restituisce **D3DERR \_ UNSUPPORTEDOVERLAY**.

### <a name="example-code"></a>Codice di esempio

Nell'esempio seguente viene illustrato come creare una superficie sovrapposta.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API video Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 




