---
title: Abilitare e controllare la composizione DWM
description: Le API Gestione finestre desktop (DWM) forniscono diverse funzioni per l'impostazione e l'esecuzione di query per informazioni di base usate da DWM.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Gestione finestre desktop (DWM), composizione
- DWM (Gestione finestre desktop),composizione
- Composizione
- composizione del desktop
- Colorazione
- rendering di aree non client
- Gestione finestre desktop (DWM), colorazione
- DWM (Gestione finestre desktop),colorazione
- Gestione finestre desktop (DWM), rendering dell'area non client
- DWM (Gestione finestre desktop), rendering dell'area non client
- Gestione finestre desktop (DWM), messaggistica
- DWM (Gestione finestre desktop), messaggistica
- messaggi
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: e8c5df1778436e2cfe23df85483453b01fb80884adc9a6d8ff34955deb3e0c6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741581"
---
# <a name="enable-and-control-dwm-composition"></a>Abilitare e controllare la composizione DWM

Le API Gestione finestre desktop (DWM) forniscono diverse funzioni per l'impostazione e l'esecuzione di query per informazioni di base usate da DWM. Queste API consentono di eseguire query e modificare lo stato della composizione. Inoltre, è possibile impostare ed eseguire query nei criteri di rendering per diversi attributi della finestra DWM.

## <a name="retrieving-colorization-information"></a>Recupero delle informazioni sulla colorazione

Il colore dell'area non client di una finestra è determinato dal tema del colore di sistema corrente. Il valore di colorazione viene fornito tramite le API DWM per consentire all'applicazione di associare l'interfaccia utente client al tema del colore di sistema.

Per accedere a questo valore di colorazione e monitorare la modifica [**del**](wm-dwmcolorizationcolorchanged.md) colore, usare la funzione [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) e il WM_DWMCOLORIZATIONCOLORCHANGED messaggio.

Questo esempio illustra come gestire il messaggio di modifica del colore e accedere al nuovo colore.

```cpp
...
case WM_DWMCOLORIZATIONCOLORCHANGED:
{
    DWORD newColorizationColor{ (DWORD)wParam };
    BOOL isBlendedWithOpacity{ (BOOL)lParam };
}
break;
...
```

## <a name="controlling-non-client-region-rendering"></a>Controllo del rendering dell'area non client

Due degli effetti visivi abilitati da DWM sono la trasparenza dell'area non client di una finestra e gli effetti di transizione. L'applicazione potrebbe dover disabilitare o riattivare questi effetti per motivi di stile o compatibilità. Le funzioni seguenti vengono usate per gestire la trasparenza e il comportamento degli effetti di transizione.

- [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

Per recuperare lo stato di rendering non client corrente per la finestra di un'applicazione, chiamare [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) con *dwAttribute* impostato su [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute). Come si può vedere dalla documentazione per [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), quando si passa il flag a **DwmGetWindowAttribute**, il valore dell'attributo recuperato è di **tipo BOOL**. Flag diversi causano la restituzione di valori di tipi diversi da parte di **DwmGetWindowAttribute.** Ecco un esempio di codice.

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

Questo esempio successivo illustra come usare il flag [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) con **DwmGetWindowAttribute** per recuperare il rettangolo dei limiti di frame estesi di una finestra. La documentazione per tale flag indica che il valore dell'attributo recuperato è di tipo **RECT.**

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> Seguire lo stesso modello di programmazione illustrato in precedenza quando si chiama [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) con flag per attributi diversi. L'argomento di enumerazione [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) indica, nella riga per ogni flag, il tipo di valore a cui passare un puntatore nel parametro *pvAttribute* per **DwmGetWindowAttribute**. Il *parametro cbAttribute* contiene le dimensioni, in byte, dell'oggetto.

[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) consente all'applicazione di impostare i criteri di rendering dell'area non client. Questa funzione determina anche come l'applicazione deve gestire gli effetti di transizione DWM.

Nell'esempio seguente viene disabilitato il rendering non nell'area client. In questo modo tutte le chiamate precedenti a [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) o [a DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) vengono disabilitate.

```
HRESULT DisableNCRendering(HWND hWnd)
{
    HRESULT hr = S_OK;

    DWMNCRENDERINGPOLICY ncrp = DWMNCRP_DISABLED;

    // Disable non-client area rendering on the window.
    hr = ::DwmSetWindowAttribute(hWnd,
        DWMWA_NCRENDERING_POLICY,
        &ncrp,
        sizeof(ncrp));

    if (SUCCEEDED(hr))
    {
        // ...
    }

    return hr;
}
```

Oltre a controllare il rendering dell'area non client, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) può anche controllare gli effetti di transizione DWM. È possibile impostare il comportamento di transizione **usando DWMWA \_ TRANSITIONS \_ FORCEDISABLED** come *parametro dwAttribute.*

## <a name="messages"></a>Messaggi

I messaggi seguenti forniscono una notifica degli eventi DWM. Questi messaggi possono essere usati per monitorare le modifiche, ad esempio le modifiche dello stato della composizione e le modifiche del tema del colore di sistema.

- [**WM \_ DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md)
- [**WM \_ DWMCOMPOSITIONCHANGED**](wm-dwmcompositionchanged.md)
- [**WM \_ DWMNCRENDERINGCHANGED**](wm-dwmncrenderingchanged.md)
- [**WM \_ DWMWINDOWMAXIMIZEDCHANGE**](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows-7-and-earlier"></a>Disabilitazione della composizione DWM (Windows 7 e versioni precedenti)

> [!WARNING]
> Le informazioni in questa sezione si applicano solo ai Windows 7 e precedenti.

Poiché DWM usa l'unità di elaborazione grafica (GPU) per la composizione desktop, l'applicazione potrebbe dover disabilitare DWM per motivi di compatibilità. Le applicazioni che hanno il controllo completo del desktop, ad esempio i giochi eseguiti in modalità schermo intero, devono determinare se DWM è abilitato e, in caso contrario, disabilitarlo. A tale scopo, sono necessarie due funzioni.

- [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

Una chiamata a [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) con *fEnable* impostato su **DWM \_ EC \_ DISABLECOMPOSITION** disabilita la composizione DWM fino all'arresto del processo chiamante o alla riabilitazione della composizione chiamando **DwmEnableComposition** con *fEnable* impostato su **DWM \_ EC \_ ENABLECOMPOSITION**. La composizione DWM viene riavviata automaticamente non appena tutte le applicazioni che hanno disabilitato la composizione sono state arrestate o hanno riabilitato manualmente la composizione chiamando **DwmEnableComposition**.

> [!NOTE]  
> DWM disabilita automaticamente la composizione quando un'applicazione tenta di disegnare direttamente sulla superficie di visualizzazione primaria. La composizione verrà disabilitata fino a quando la superficie del dispositivo primario non viene rilasciata dall'applicazione.
