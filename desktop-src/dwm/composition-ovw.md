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
# <a name="enable-and-control-dwm-composition"></a><span data-ttu-id="e6ba6-116">Abilitare e controllare la composizione DWM</span><span class="sxs-lookup"><span data-stu-id="e6ba6-116">Enable and control DWM composition</span></span>

<span data-ttu-id="e6ba6-117">Le API di composizione di Gestione finestre desktop (DWM) forniscono diverse funzioni per l'impostazione e l'esecuzione di query per le informazioni di base utilizzate da DWM.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-117">The Desktop Window Manager (DWM) composition APIs provide several functions for setting and querying for basic information that is used by the DWM.</span></span> <span data-ttu-id="e6ba6-118">Queste API consentono di eseguire query e modificare lo stato di composizione.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-118">These APIs enable you to query and change the composition state.</span></span> <span data-ttu-id="e6ba6-119">Inoltre, è possibile impostare ed eseguire una query sui criteri di rendering per diversi attributi della finestra DWM.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-119">Additionally, you can set and query the rendering policy for different DWM window attributes.</span></span>

## <a name="retrieving-colorization-information"></a><span data-ttu-id="e6ba6-120">Recupero delle informazioni di colorazione</span><span class="sxs-lookup"><span data-stu-id="e6ba6-120">Retrieving colorization information</span></span>

<span data-ttu-id="e6ba6-121">Il colore dell'area non client di una finestra è determinato dal tema colori del sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-121">The color of the non-client region of a window is determined by the current system color theme.</span></span> <span data-ttu-id="e6ba6-122">Il valore di colorazione viene fornito tramite le API di DWM per consentire all'applicazione di associare l'interfaccia utente del client al tema colori di sistema.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-122">The colorization value is provided through the DWM APIs to enable your application to match client UI with the system color theme.</span></span>

<span data-ttu-id="e6ba6-123">Per accedere a questo valore di colorazione e monitorare la modifica del colore, usare la funzione [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) e il messaggio [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="e6ba6-123">To access this colorization value, and monitor the color change, use the [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) function and the [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) message.</span></span>

<span data-ttu-id="e6ba6-124">In questo esempio viene illustrato come gestire il messaggio del colore modificato e accedere al nuovo colore.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-124">This example demonstrates how to handle the color changed message and access the new color.</span></span>

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

## <a name="controlling-non-client-region-rendering"></a><span data-ttu-id="e6ba6-125">Controllo del rendering dell'area non client</span><span class="sxs-lookup"><span data-stu-id="e6ba6-125">Controlling non-client region rendering</span></span>

<span data-ttu-id="e6ba6-126">Due degli effetti visivi abilitati da DWM sono la trasparenza dell'area non client di una finestra e gli effetti di transizione.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-126">Two of the visual effects that DWM enables are transparency of the non-client region of a window, and transition effects.</span></span> <span data-ttu-id="e6ba6-127">È possibile che l'applicazione debba disabilitare o riabilitare questi effetti per motivi di compatibilità o di stile.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-127">Your application might have to disable or re-enable these effects for styling or compatibility reasons.</span></span> <span data-ttu-id="e6ba6-128">Le funzioni seguenti vengono utilizzate per gestire il comportamento di trasparenza e effetto di transizione.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-128">The following functions are used to manage transparency and transition effect behavior.</span></span>

- [<span data-ttu-id="e6ba6-129">**DwmGetWindowAttribute**</span><span class="sxs-lookup"><span data-stu-id="e6ba6-129">**DwmGetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [<span data-ttu-id="e6ba6-130">**DwmSetWindowAttribute**</span><span class="sxs-lookup"><span data-stu-id="e6ba6-130">**DwmSetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

<span data-ttu-id="e6ba6-131">Per recuperare lo stato di rendering non client corrente per la finestra di un'applicazione, chiamare [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) con *dwAttribute* impostato su [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute).</span><span class="sxs-lookup"><span data-stu-id="e6ba6-131">To retrieve the current non-client rendering state for an application's window, call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with *dwAttribute* set to [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute).</span></span> <span data-ttu-id="e6ba6-132">Come si può notare dalla documentazione per [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), quando si passa il flag a **DwmGetWindowAttribute**, il valore dell'attributo recuperato è di tipo **bool**.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-132">As you can see from the documentation for [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), when you pass that flag to **DwmGetWindowAttribute**, the retrieved attribute value is of type **BOOL**.</span></span> <span data-ttu-id="e6ba6-133">Flag diversi provocano la restituzione di valori di tipi diversi da **DwmGetWindowAttribute** .</span><span class="sxs-lookup"><span data-stu-id="e6ba6-133">Different flags cause **DwmGetWindowAttribute** to return values of different types.</span></span> <span data-ttu-id="e6ba6-134">Ecco un esempio di codice.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-134">Here's a code example.</span></span>

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

<span data-ttu-id="e6ba6-135">Nell'esempio seguente viene illustrato come utilizzare il flag di [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) con **DwmGetWindowAttribute** per recuperare il rettangolo esteso dei limiti del frame di una finestra.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-135">This next example shows how to use the [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) flag with **DwmGetWindowAttribute** to retrieve the extended frame bounds rectangle of a window.</span></span> <span data-ttu-id="e6ba6-136">La documentazione relativa a tale flag indica che il valore dell'attributo recuperato è di tipo **Rect**.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-136">The documentation for that flag tells us that the retrieved attribute value is of type **RECT**.</span></span>

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> <span data-ttu-id="e6ba6-137">Seguire lo stesso modello di programmazione illustrato in precedenza quando si chiama [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) con i flag per attributi diversi.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-137">Follow the same programming pattern shown above when you call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with flags for different attributes.</span></span> <span data-ttu-id="e6ba6-138">L'argomento enumerazione [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) indica, nella riga per ogni flag, il tipo di valore a cui è necessario passare un puntatore nel parametro *pvAttribute* per **DwmGetWindowAttribute**.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-138">The [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) enumeration topic indicates, in the row for each flag, what type of value you should pass a pointer to in the *pvAttribute* parameter for **DwmGetWindowAttribute**.</span></span> <span data-ttu-id="e6ba6-139">Il parametro *cbAttribute* contiene le dimensioni, in byte, di tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-139">The *cbAttribute* parameter contains the size, in bytes, of that object.</span></span>

<span data-ttu-id="e6ba6-140">[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) consente all'applicazione di impostare i criteri di rendering dell'area non client.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-140">[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) enables your application to set the non-client area rendering policy.</span></span> <span data-ttu-id="e6ba6-141">Questa funzione determina anche il modo in cui l'applicazione deve gestire gli effetti di transizione di DWM.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-141">That function also determines how your application should handle DWM transition effects.</span></span>

<span data-ttu-id="e6ba6-142">Nell'esempio seguente viene disabilitato il rendering dell'area non client.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-142">This next example disables non-client area rendering.</span></span> <span data-ttu-id="e6ba6-143">In questo modo, qualsiasi chiamata precedente a [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) o a [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) viene disabilitata.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-143">This causes any previous calls to [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) or to [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) to be disabled.</span></span>

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

<span data-ttu-id="e6ba6-144">Oltre a controllare il rendering dell'area non client, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) può controllare anche gli effetti di transizione di DWM.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-144">In addition to controlling the non-client area rendering, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) can also control DWM transition effects.</span></span> <span data-ttu-id="e6ba6-145">È possibile impostare il comportamento della transizione usando **DWMWA \_ Transitions \_ FORCEDISABLED** come parametro *dwAttribute* .</span><span class="sxs-lookup"><span data-stu-id="e6ba6-145">You can set transition behavior by using **DWMWA\_TRANSITIONS\_FORCEDISABLED** as the *dwAttribute* parameter.</span></span>

## <a name="messages"></a><span data-ttu-id="e6ba6-146">Messaggi</span><span class="sxs-lookup"><span data-stu-id="e6ba6-146">Messages</span></span>

<span data-ttu-id="e6ba6-147">I messaggi seguenti forniscono la notifica degli eventi DWM.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-147">The following messages provide notification of DWM events.</span></span> <span data-ttu-id="e6ba6-148">Questi messaggi possono essere usati per monitorare le modifiche, ad esempio le modifiche dello stato di composizione e le modifiche ai temi dei colori di sistema.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-148">These messages can be used to monitor changes such as composition state changes and system color theme changes.</span></span>

- [<span data-ttu-id="e6ba6-149">**\_DWMCOLORIZATIONCOLORCHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="e6ba6-149">**WM\_DWMCOLORIZATIONCOLORCHANGED**</span></span>](wm-dwmcolorizationcolorchanged.md)
- [<span data-ttu-id="e6ba6-150">**\_DWMCOMPOSITIONCHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="e6ba6-150">**WM\_DWMCOMPOSITIONCHANGED**</span></span>](wm-dwmcompositionchanged.md)
- [<span data-ttu-id="e6ba6-151">**\_DWMNCRENDERINGCHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="e6ba6-151">**WM\_DWMNCRENDERINGCHANGED**</span></span>](wm-dwmncrenderingchanged.md)
- [<span data-ttu-id="e6ba6-152">**\_DWMWINDOWMAXIMIZEDCHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="e6ba6-152">**WM\_DWMWINDOWMAXIMIZEDCHANGE**</span></span>](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows7-and-earlier"></a><span data-ttu-id="e6ba6-153">Disabilitazione della composizione DWM (Windows 7 e versioni precedenti)</span><span class="sxs-lookup"><span data-stu-id="e6ba6-153">Disabling DWM composition (Windows 7 and earlier)</span></span>

> [!WARNING]
> <span data-ttu-id="e6ba6-154">Le informazioni in questa sezione si applicano solo ai sistemi Windows 7 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-154">The info in this section applies only to Windows 7 and earlier systems.</span></span>

<span data-ttu-id="e6ba6-155">Poiché DWM usa l'unità di elaborazione grafica (GPU) per la composizione del desktop, l'applicazione potrebbe dover disabilitare DWM per la compatibilità.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-155">Because DWM uses the graphics processing unit (GPU) for desktop composition, your application might have to disable DWM for compatibility.</span></span> <span data-ttu-id="e6ba6-156">Le applicazioni che hanno il controllo completo sul desktop, ad esempio i giochi eseguiti in modalità schermo intero, devono determinare se DWM è abilitato e, in caso contrario, disabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-156">Applications that take full control of the desktop, such as games that run in full-screen mode, must determine whether the DWM is enabled and if it is, disable it.</span></span> <span data-ttu-id="e6ba6-157">A tale scopo, sono necessarie due funzioni.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-157">To do this, two functions are needed.</span></span>

- [<span data-ttu-id="e6ba6-158">**DwmIsCompositionEnabled**</span><span class="sxs-lookup"><span data-stu-id="e6ba6-158">**DwmIsCompositionEnabled**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [<span data-ttu-id="e6ba6-159">**DwmEnableComposition**</span><span class="sxs-lookup"><span data-stu-id="e6ba6-159">**DwmEnableComposition**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

<span data-ttu-id="e6ba6-160">Una chiamata a [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) con *FEnable* impostato su **DWM \_ EC \_ DISABLECOMPOSITION** Disabilita la composizione DWM fino a quando il processo chiamante non è stato arrestato o la composizione è stata riabilitata chiamando **DwmEnableComposition** con *fEnable* impostato su **DWM \_ EC \_ ENABLECOMPOSITION**.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-160">A call to [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) with *fEnable* set to **DWM\_EC\_DISABLECOMPOSITION** disables DWM composition until either the calling process has shut down, or composition has been re-enabled by calling **DwmEnableComposition** with *fEnable* set to **DWM\_EC\_ENABLECOMPOSITION**.</span></span> <span data-ttu-id="e6ba6-161">La composizione di DWM viene riavviata automaticamente non appena tutte le applicazioni che hanno disabilitato la composizione sono state arrestate o hanno riabilitato manualmente la composizione chiamando **DwmEnableComposition**.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-161">DWM composition restarts automatically as soon as all applications that have disabled composition have either shut down or have manually re-enabled composition by calling **DwmEnableComposition**.</span></span>

> [!NOTE]  
> <span data-ttu-id="e6ba6-162">DWM Disabilita automaticamente la composizione quando un'applicazione tenta di creare direttamente l'area di visualizzazione primaria.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-162">The DWM automatically disables composition when an application attempts to draw directly to the primary display surface.</span></span> <span data-ttu-id="e6ba6-163">La composizione verrà disabilitata fino a quando la superficie del dispositivo primario non verrà rilasciata da tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="e6ba6-163">Composition will be disabled until the primary device surface is released by that application.</span></span>
