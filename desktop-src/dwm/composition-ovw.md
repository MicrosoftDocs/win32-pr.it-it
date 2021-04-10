---
title: Abilitare e controllare la composizione DWM
description: Le API di composizione di Gestione finestre desktop (DWM) forniscono diverse funzioni per l'impostazione e l'esecuzione di query per le informazioni di base utilizzate da DWM.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Gestione finestre desktop (DWM), composizione
- DWM (Gestione finestre desktop), composizione
- Composizione
- composizione del desktop
- colorazione
- rendering dell'area non client
- Gestione finestre desktop (DWM), colorazione
- DWM (Gestione finestre desktop), colorazione
- Gestione finestre desktop (DWM), rendering dell'area non client
- DWM (Gestione finestre desktop), rendering dell'area non client
- Gestione finestre desktop (DWM), messaggistica
- DWM (Gestione finestre desktop), messaggistica
- messaggi
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: 8d7654f479896002b4bc65df613fab9506caf2a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856761"
---
# <a name="enable-and-control-dwm-composition"></a>Abilitare e controllare la composizione DWM

Le API di composizione di Gestione finestre desktop (DWM) forniscono diverse funzioni per l'impostazione e l'esecuzione di query per le informazioni di base utilizzate da DWM. Queste API consentono di eseguire query e modificare lo stato di composizione. Inoltre, è possibile impostare ed eseguire una query sui criteri di rendering per diversi attributi della finestra DWM.

## <a name="retrieving-colorization-information"></a>Recupero delle informazioni di colorazione

Il colore dell'area non client di una finestra è determinato dal tema colori del sistema corrente. Il valore di colorazione viene fornito tramite le API di DWM per consentire all'applicazione di associare l'interfaccia utente del client al tema colori di sistema.

Per accedere a questo valore di colorazione e monitorare la modifica del colore, usare la funzione [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) e il messaggio [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) .

In questo esempio viene illustrato come gestire il messaggio del colore modificato e accedere al nuovo colore.

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

Due degli effetti visivi abilitati da DWM sono la trasparenza dell'area non client di una finestra e gli effetti di transizione. È possibile che l'applicazione debba disabilitare o riabilitare questi effetti per motivi di compatibilità o di stile. Le funzioni seguenti vengono utilizzate per gestire il comportamento di trasparenza e effetto di transizione.

- [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

Per recuperare lo stato di rendering non client corrente per la finestra di un'applicazione, chiamare [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) con *dwAttribute* impostato su [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute). Come si può notare dalla documentazione per [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), quando si passa il flag a **DwmGetWindowAttribute**, il valore dell'attributo recuperato è di tipo **bool**. Flag diversi provocano la restituzione di valori di tipi diversi da **DwmGetWindowAttribute** . Ecco un esempio di codice.

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

Nell'esempio seguente viene illustrato come utilizzare il flag di [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) con **DwmGetWindowAttribute** per recuperare il rettangolo esteso dei limiti del frame di una finestra. La documentazione relativa a tale flag indica che il valore dell'attributo recuperato è di tipo **Rect**.

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> Seguire lo stesso modello di programmazione illustrato in precedenza quando si chiama [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) con i flag per attributi diversi. L'argomento enumerazione [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) indica, nella riga per ogni flag, il tipo di valore a cui è necessario passare un puntatore nel parametro *pvAttribute* per **DwmGetWindowAttribute**. Il parametro *cbAttribute* contiene le dimensioni, in byte, di tale oggetto.

[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) consente all'applicazione di impostare i criteri di rendering dell'area non client. Questa funzione determina anche il modo in cui l'applicazione deve gestire gli effetti di transizione di DWM.

Nell'esempio seguente viene disabilitato il rendering dell'area non client. In questo modo, qualsiasi chiamata precedente a [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) o a [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) viene disabilitata.

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

Oltre a controllare il rendering dell'area non client, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) può controllare anche gli effetti di transizione di DWM. È possibile impostare il comportamento della transizione usando **DWMWA \_ Transitions \_ FORCEDISABLED** come parametro *dwAttribute* .

## <a name="messages"></a>Messaggi

I messaggi seguenti forniscono la notifica degli eventi DWM. Questi messaggi possono essere usati per monitorare le modifiche, ad esempio le modifiche dello stato di composizione e le modifiche ai temi dei colori di sistema.

- [**\_DWMCOLORIZATIONCOLORCHANGED WM**](wm-dwmcolorizationcolorchanged.md)
- [**\_DWMCOMPOSITIONCHANGED WM**](wm-dwmcompositionchanged.md)
- [**\_DWMNCRENDERINGCHANGED WM**](wm-dwmncrenderingchanged.md)
- [**\_DWMWINDOWMAXIMIZEDCHANGE WM**](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows7-and-earlier"></a>Disabilitazione della composizione DWM (Windows 7 e versioni precedenti)

> [!WARNING]
> Le informazioni in questa sezione si applicano solo ai sistemi Windows 7 e versioni precedenti.

Poiché DWM usa l'unità di elaborazione grafica (GPU) per la composizione del desktop, l'applicazione potrebbe dover disabilitare DWM per la compatibilità. Le applicazioni che hanno il controllo completo sul desktop, ad esempio i giochi eseguiti in modalità schermo intero, devono determinare se DWM è abilitato e, in caso contrario, disabilitarlo. A tale scopo, sono necessarie due funzioni.

- [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

Una chiamata a [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) con *FEnable* impostato su **DWM \_ EC \_ DISABLECOMPOSITION** Disabilita la composizione DWM fino a quando il processo chiamante non è stato arrestato o la composizione è stata riabilitata chiamando **DwmEnableComposition** con *fEnable* impostato su **DWM \_ EC \_ ENABLECOMPOSITION**. La composizione di DWM viene riavviata automaticamente non appena tutte le applicazioni che hanno disabilitato la composizione sono state arrestate o hanno riabilitato manualmente la composizione chiamando **DwmEnableComposition**.

> [!NOTE]  
> DWM Disabilita automaticamente la composizione quando un'applicazione tenta di creare direttamente l'area di visualizzazione primaria. La composizione verrà disabilitata fino a quando la superficie del dispositivo primario non verrà rilasciata da tale applicazione.
