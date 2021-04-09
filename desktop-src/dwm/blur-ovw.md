---
title: Panoramica di DWM Blur behind
description: Uno degli effetti di Gestione finestre desktop della firma (DWM) è un'area non client trasparente e sfocata. Le API DWM consentono alle applicazioni di applicare questi effetti all'area client delle finestre di primo livello.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Gestione finestre desktop (DWM), effetto Blur-behind
- DWM (Gestione finestre desktop), effetto Blur-behind
- effetto Blur-behind
- effetto translucido
- effetto cristallo trasparente
- Gestione finestre desktop (DWM), effetto translucido
- DWM (Gestione finestre desktop), effetto translucido
- Gestione finestre desktop (DWM), effetto cristallo trasparente
- DWM (Gestione finestre desktop), effetto cristallo trasparente
- Gestione finestre desktop (DWM), estensione della cornice della finestra all'area client
- DWM (Gestione finestre desktop), estensione della cornice della finestra all'area client
- estensione della cornice della finestra all'area client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf7378cfcaff93aa9a54ce399890ec1bfd8cc1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047259"
---
# <a name="dwm-blur-behind-overview"></a>Panoramica di DWM Blur behind

Uno degli effetti di Gestione finestre desktop della firma (DWM) è un'area non client trasparente e sfocata. Le API DWM consentono alle applicazioni di applicare questi effetti all'area client delle finestre di primo livello.

> [!Note]  
> Windows Vista Home Basic Edition non supporta l'effetto cristallo trasparente. Le aree che in genere eseguono il rendering con effetto cristallo trasparente sulle altre edizioni di Windows vengono visualizzate come opache.
> A partire da Windows 8, la chiamata a questa funzione non comporta un effetto sfocatura, a causa di una modifica dello stile nel modo in cui viene eseguito il rendering di Windows.


 

In questo argomento vengono illustrati i seguenti scenari di sfocatura dei client abilitati da DWM.

-   [Aggiunta della sfocatura a un'area specifica dell'area client](#adding-blur-to-a-specific-region-of-the-client-area)
-   [Estensione della cornice della finestra nell'area client](#extending-the-window-frame-into-the-client-area)
-   [Argomenti correlati](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a>Aggiunta della sfocatura a un'area specifica dell'area client

Un'applicazione può applicare l'effetto sfocatura dietro l'intera area client della finestra o a una specifica area secondaria. In questo modo, le applicazioni possono aggiungere barre di ricerca e percorso con stile separate visivamente dal resto dell'applicazione.

L'API usata in questo scenario è la funzione [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) , che usa la [**sfocatura di DWM dietro le costanti**](dwm-bb-constants.md) e la struttura [**\_ BLURBEHIND di DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) .

La funzione di esempio seguente, `EnableBlurBehind` , illustra come applicare l'effetto Blur-behind all'intera finestra.


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



Si noti che il **valore null** è specificato nel parametro *hRgnBlur* . Ciò indica a DWM di applicare la sfocatura dietro l'intera finestra.

Nell'immagine seguente viene illustrato l'effetto Blur-behind applicato all'intera finestra.

![effetto Blur-behind applicato a una finestra](images/dwm-blurbehindwindow.png)

Per applicare la sfocatura dietro un'area secondaria, applicare un handle di area valido (HRGN) al membro **hRgnBlur** della struttura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) e aggiungere il flag **DWM \_ BB \_ BLURREGION** al membro **dwFlags** .

Quando si applica l'effetto Blur-behind a un'area secondaria della finestra, viene usato il canale alfa della finestra per l'area non sfocata. Ciò può causare una trasparenza imprevista nell'area non sfocata di una finestra. Pertanto, prestare attenzione quando si applica un effetto di sfocatura a un'area secondaria.

## <a name="extending-the-window-frame-into-the-client-area"></a>Estensione della cornice della finestra nell'area client

Un'applicazione può estendere la sfocatura della cornice della finestra nell'area client. Questa operazione è utile quando si applica l'effetto di sfocatura dietro una finestra con una barra degli strumenti ancorata o si separano visivamente i controlli dal resto di un'applicazione. Questa funzionalità è esposta dalla funzione [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .

Per abilitare la sfocatura usando [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), usare la struttura dei [**margini**](/windows/win32/api/uxtheme/ns-uxtheme-margins) per indicare la quantità di estensione nell'area client. La funzione di esempio seguente, `ExtendIntoClientBottom` , imposta l'estensione della sfocatura nella parte inferiore del frame non client nell'area client.


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



Nell'immagine seguente viene illustrato l'effetto Blur-behind esteso nella parte inferiore dell'area client.

![immagine che mostra l'effetto Blur-behind esteso nella parte inferiore di un'area client](images/dwm-extendedbottom.png)

Disponibile anche tramite il metodo [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) è l'effetto "foglio di vetro", in cui l'effetto di sfocatura viene applicato all'intera superficie della finestra senza bordo visibile della finestra. Nell'esempio seguente viene illustrato questo effetto in cui viene eseguito il rendering dell'area client senza un bordo della finestra.


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



Nell'immagine seguente viene illustrata la sfocatura nello stile della finestra "foglio di vetro".

![immagine che illustra l'effetto Blur-behind nello stile della finestra "foglio di vetro"](images/dwm-sheetofglass.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari di Gestione finestre desktop](dwm-overview.md)
</dt> <dt>

[Abilitare e controllare la composizione DWM](composition-ovw.md)
</dt> <dt>

[Considerazioni sulle prestazioni e procedure consigliate](bestpractices-ovw.md)
</dt> </dl>

 

 