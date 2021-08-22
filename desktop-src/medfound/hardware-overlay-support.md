---
description: Descrive come usare le sovrimpressione hardware in Direct3D 9.
ms.assetid: fa9d5bf5-4c0f-471a-b639-d329b0cd89a4
title: Supporto della sovrapposizione hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f537c91bc217344206c0a23cf5ca8a14254a9c983e4ae550e96457bbb055e5d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600401"
---
# <a name="hardware-overlay-support"></a>Supporto della sovrapposizione hardware

Una sovrapposizione hardware è un'area dedicata di memoria video che può essere sovrapposta sulla superficie primaria. Non viene eseguita alcuna copia quando viene visualizzata la sovrimpressione. L'operazione di sovrapposizione viene eseguita nell'hardware, senza modificare i dati nella superficie primaria.

L'uso di sovrimpressione hardware per la riproduzione video era comune nelle versioni precedenti di Windows, perché le sovrimpressione sono efficienti per il contenuto video con una frequenza fotogrammi elevata. A partire da Windows 7, Direct3D 9 supporta le sovrapposizioni hardware. Questo supporto è destinato principalmente alla riproduzione video e differisce per alcuni aspetti dalle API DirectDraw precedenti:

-   La sovrimpressione non può essere ridotta, con mirroring o deinterlaced.
-   Le chiavi di colore di origine e la fusione alfa non sono supportate.
-   Le sovrimpressione possono essere allungate se l'hardware di sovrapposizione lo supporta. In caso contrario, l'estensione non è supportata. In pratica, non tutti i driver di grafica supportano l'estensione.
-   Ogni dispositivo supporta al massimo una sovrapposizione.
-   La sovrapposizione viene eseguita usando una chiave di colore di destinazione, ma il runtime Direct3D seleziona automaticamente il colore e disegna il rettangolo di destinazione. Direct3D tiene traccia automaticamente della posizione della finestra e aggiorna la posizione di sovrapposizione ogni volta che viene chiamato **PresentEx.**

### <a name="creating-a-hardware-overlay-surface"></a>Creazione di una superficie di sovrapposizione hardware

Per eseguire query sul supporto della sovrapposizione, **chiamare IDirect3D9::GetDeviceCaps**. Se il driver supporta la sovrapposizione hardware, il flag **OVERLAY \_ D3DCAPS** viene impostato in **D3DCAPS9. Membro Caps.**

Per determinare se un formato di sovrimpressione specifico è supportato per una determinata modalità di visualizzazione, chiamare [**IDirect3D9ExOverlayExtension::CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).

Per creare la sovrimpressione, chiamare **IDirect3D9Ex::CreateDeviceEx** e specificare l'effetto di scambio **OVERLAY D3DSWAPEFFECT. \_** Il buffer nascosto può usare un formato non RGB se supportato dall'hardware.

Le superfici sovrapposte presentano le limitazioni seguenti:

-   L'applicazione non può creare più di una catena di scambio di sovrimpressione.
-   La sovrimpressione deve essere usata in modalità a finestre. Non può essere usato in modalità schermo intero.
-   L'effetto di scambio della sovrimpressione deve essere usato con **l'interfaccia IDirect3DDevice9Ex.** Non è supportato per **IDirect3DDevice9.**
-   Non è possibile usare il multicampionamento.
-   I **flag D3DPRESENT \_ DONOTFLIP** e **D3DPRESENT \_ FLIPRESTART** non sono supportati.
-   Le statistiche di presentazione non sono disponibili per la superficie di sovrapposizione.

Se l'hardware non supporta l'estensione, è consigliabile creare una catena di scambio grande quanto la modalità di visualizzazione, in modo che la finestra possa essere ridimensionata in qualsiasi dimensione. La ricreazione della catena di scambio non è un modo ottimale per gestire il ridimensionamento della finestra, perché può causare artefatti di rendering gravi. Inoltre, a causa del modo in cui la GPU gestisce la memoria di sovrapposizione, la ricreazione della catena di scambio può causare l'estrazione della memoria video da parte di un'applicazione.

### <a name="new-d3dpresent_parameters-flags"></a>Nuovi flag D3DPRESENT \_ PARAMETERS

I flag **D3DPRESENT \_ PARAMETERS** seguenti sono definiti per la creazione di sovrimpressione.



| Flag                                      | Descrizione                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENTFLAG \_ OVERLAY \_ LIMITEDRGB**   | L'intervallo RGB è compreso tra 16 e 235. Il valore predefinito è 0-255. <br/> Richiede la **funzionalità D3DOVERLAYCAPS \_ LIMITEDRANGERGB.**<br/>                                                 |
| **D3DPRESENTFLAG \_ OVERLAY \_ YCbCr \_ BT709** | I colori YUV usano la definizione BT.709. Il valore predefinito è BT.601. <br/> Richiede la **funzionalità D3DOVERLAYCAPS \_ YCbCr \_ BT709.**<br/>                                      |
| **D3DPRESENTFLAG \_ OVERLAY \_ YCbCr \_ xvYCC** | Eseguire l'output dei dati usando YCbCr esteso (xvYCC).<br/> Richiede la funzionalità **D3DOVERLAYCAPS \_ YCbCr \_ BT601 \_ xvYCC** o **D3DOVERLAYCAPS \_ YCbCr \_ BT709 \_ xvYCC.**<br/> |



 

### <a name="using-hardware-overlays"></a>Uso di sovrimpressione hardware

Per visualizzare la superficie di sovrapposizione, l'applicazione chiama **IDirect3DDevice9Ex::P resentEx**. Il runtime Direct3D disegna automaticamente la chiave di colore di destinazione.

I flag **PresentEx** seguenti sono definiti per le sovrimpressione.



| Flag                              | Descrizione                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENT \_ UPDATECOLORKEY**    | Impostare questo flag se la Gestione finestre desktop (DWM) è disabilitata. Questo flag fa sì che Direct3D ridisegni la chiave di colore.<br/> Se DWM è abilitato, questo flag non è obbligatorio, perché Direct3D disegna la chiave di colore una volta sulla superficie utilizzata da DWM per il reindirizzamento.<br/> |
| **D3DPRESENT \_ HIDEOVERLAY**       | Nasconde la sovrimpressione.                                                                                                                                                                                                                                                                    |
| **D3DPRESENT \_ UPDATEOVERLAYONLY** | Aggiorna la sovrimpressione senza modificare il contenuto.<br/> Questo flag è utile se la finestra viene spostata mentre il video è in pausa.<br/>                                                                                                                                           |



 

Un'applicazione deve essere preparata per gestire i casi seguenti:

-   Se un'altra applicazione usa la sovrimpressione, **PresentEx** restituisce **D3DERR \_ NOTAVAILABLE**.
-   Se la finestra viene spostata in un altro monitoraggio, l'applicazione deve ricreare la catena di scambio. In caso contrario, se l'applicazione chiama **PresentEx** per visualizzare la sovrimpressione su un monitor diverso, **PresentEx** restituisce **D3DERR \_ INVALIDDEVICE**.
-   Se la modalità di visualizzazione cambia, Direct3D tenta di ripristinare la sovrimpressione. Se la nuova modalità non supporta la sovrapposizione, **PresentEx** restituisce **D3DERR \_ UNSUPPORTEDOVERLAY**.

### <a name="example-code"></a>Codice di esempio

L'esempio seguente illustra come creare una superficie di sovrapposizione.


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

[API Video Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 




