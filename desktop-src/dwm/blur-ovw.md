---
title: Panoramica della sfocatura DWM
description: Uno degli effetti di Gestione finestre desktop (DWM) è un'area non client traslucida e sfocata. Le API DWM consentono alle applicazioni di applicare questi effetti all'area client delle finestre di primo livello.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Gestione finestre desktop (DWM), effetto blur-behind
- DWM (Gestione finestre desktop), effetto blur-behind
- Effetto blur-behind
- effetto traslucido
- effetto vetri trasparenti
- Gestione finestre desktop (DWM), effetto traslucido
- DWM (Gestione finestre desktop), effetto traslucido
- Gestione finestre desktop (DWM), effetto trasparente
- Effetto DWM (Gestione finestre desktop), trasparente
- Gestione finestre desktop (DWM), estensione della cornice della finestra nell'area client
- DWM (Gestione finestre desktop), estensione della cornice della finestra nell'area client
- estensione della cornice della finestra nell'area client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb7b357719ea3aa5a4853a933350ee2dda417842777354e2bbf1711e1cbeff1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456086"
---
# <a name="dwm-blur-behind-overview"></a>Panoramica della sfocatura DWM

Uno degli effetti di Gestione finestre desktop (DWM) è un'area non client traslucida e sfocata. Le API DWM consentono alle applicazioni di applicare questi effetti all'area client delle finestre di primo livello.

> [!Note]  
> Windows Vista Home Basic Edition non supporta l'effetto trasparente. Le aree di cui in genere viene eseguito il rendering con l'effetto trasparente in Windows edizioni vengono visualizzate come opache.
> A partire Windows 8, la chiamata a questa funzione non comporta l'effetto sfocatura, a causa di una modifica dello stile nel modo in cui viene eseguito il rendering delle finestre.


 

In questo argomento vengono illustrati gli scenari di sfocatura client seguenti abilitati da DWM.

-   [Aggiunta della sfocatura a un'area specifica dell'area client](#adding-blur-to-a-specific-region-of-the-client-area)
-   [Estensione della cornice della finestra nell'area client](#extending-the-window-frame-into-the-client-area)
-   [Argomenti correlati](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a>Aggiunta della sfocatura a un'area specifica dell'area client

Un'applicazione può applicare l'effetto sfocatura dietro l'intera area client della finestra o a una sottoarea specifica. In questo modo le applicazioni possono aggiungere barre di ricerca e percorso con stile che sono visivamente separate dal resto dell'applicazione.

L'API usata in questo scenario è la funzione [**DwmEnableBlurBehindWindow,**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) che usa la sfocatura [**DWM dietro**](dwm-bb-constants.md) le costanti e la struttura [**DWM \_ BLURBEHIND.**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)

La funzione di esempio seguente, `EnableBlurBehind` , illustra come applicare l'effetto sfocatura all'intera finestra.


```
HRESULT EnableBlurBehind(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Create and populate the blur-behind structure.
    DWM_BLURBEHIND bb = {0};

    // Specify blur-behind and blur region.
    bb.dwFlags = DWM_BB_ENABLE;
    bb.fEnable = true;
    bb.hRgnBlur = NULL;

    // Enable blur-behind.
    hr = DwmEnableBlurBehindWindow(hwnd, &bb);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



Si noti **che NULL** è specificato nel *parametro hRgnBlur.* Questo indica al DWM di applicare la sfocatura dietro l'intera finestra.

L'immagine seguente illustra l'effetto sfocatura applicato all'intera finestra.

![effetto sfocatura applicato a una finestra](images/dwm-blurbehindwindow.png)

Per applicare la sfocatura dietro una sottoarea, applicare un handle di area valido (HRGN) al membro **hRgnBlur** della struttura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) e aggiungere il flag **DWM \_ BB \_ BLURREGION** al membro **dwFlags.**

Quando si applica l'effetto sfocatura a una sottoarea della finestra, viene usato il canale alfa della finestra per l'area non ancorata. Ciò può causare una trasparenza imprevista nell'area non ancorata di una finestra. Prestare quindi attenzione quando si applica un effetto sfocatura a una sottoarea.

## <a name="extending-the-window-frame-into-the-client-area"></a>Estensione della cornice della finestra nell'area client

Un'applicazione può estendere la sfocatura della cornice della finestra nell'area client. Ciò è utile quando si applica l'effetto sfocatura dietro una finestra con una barra degli strumenti ancorata o si separano visivamente i controlli dal resto di un'applicazione. Questa funzionalità è esposta dalla [**funzione DwmExtendFrameIntoClientArea.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea)

Per abilitare la sfocatura [**tramite DwmExtendFrameIntoClientArea,**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea)usare la struttura [**MARGINS**](/windows/win32/api/uxtheme/ns-uxtheme-margins) per indicare la quantità di estensione nell'area client. La funzione di esempio seguente, , attiva o disattiva l'estensione sfocatura nella parte inferiore del `ExtendIntoClientBottom` frame non client nell'area client.


```
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Set the margins, extending the bottom margin.
    MARGINS margins = {0,0,0,25};

    // Extend the frame on the bottom of the client area.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



L'immagine seguente illustra l'effetto sfocatura esteso nella parte inferiore dell'area client.

![Immagine che mostra l'effetto sfocatura esteso nella parte inferiore di un'area client](images/dwm-extendedbottom.png)

Disponibile anche tramite il metodo [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) è l'effetto "foglio di cristallo", in cui l'effetto sfocatura viene applicato all'intera superficie della finestra senza un bordo visibile della finestra. L'esempio seguente illustra questo effetto in cui viene eseguito il rendering dell'area client senza un bordo della finestra.


```
HRESULT ExtendIntoClientAll(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
    // Negative margins create the "sheet of glass" effect, where the client 
    // area is rendered as a solid surface without a window border.
    MARGINS margins = {-1};

    // Extend the frame across the whole window.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



L'immagine seguente illustra la sfocatura nello stile della finestra "foglio di vetro".

![immagine che illustra l'effetto sfocatura nello stile della finestra "foglio di vetro"](images/dwm-sheetofglass.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari di Gestione finestre desktop](dwm-overview.md)
</dt> <dt>

[Abilitare e controllare la composizione DWM](composition-ovw.md)
</dt> <dt>

[Considerazioni sulle prestazioni e procedure consigliate](bestpractices-ovw.md)
</dt> </dl>

 

 