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
# <a name="dwm-blur-behind-overview"></a><span data-ttu-id="6a5e9-116">Panoramica di DWM Blur behind</span><span class="sxs-lookup"><span data-stu-id="6a5e9-116">DWM Blur Behind Overview</span></span>

<span data-ttu-id="6a5e9-117">Uno degli effetti di Gestione finestre desktop della firma (DWM) è un'area non client trasparente e sfocata.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-117">One of the signature Desktop Window Manager (DWM) effects is a translucent and blurred non-client area.</span></span> <span data-ttu-id="6a5e9-118">Le API DWM consentono alle applicazioni di applicare questi effetti all'area client delle finestre di primo livello.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-118">The DWM APIs enable applications to apply these effects to the client area of their top-level windows.</span></span>

> [!Note]  
> <span data-ttu-id="6a5e9-119">Windows Vista Home Basic Edition non supporta l'effetto cristallo trasparente.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-119">Windows Vista Home Basic edition does not support the transparent glass effect.</span></span> <span data-ttu-id="6a5e9-120">Le aree che in genere eseguono il rendering con effetto cristallo trasparente sulle altre edizioni di Windows vengono visualizzate come opache.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-120">Areas that would typically render with the transparent glass effect on other Windows editions are rendered as opaque.</span></span>
> <span data-ttu-id="6a5e9-121">A partire da Windows 8, la chiamata a questa funzione non comporta un effetto sfocatura, a causa di una modifica dello stile nel modo in cui viene eseguito il rendering di Windows.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-121">Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>


 

<span data-ttu-id="6a5e9-122">In questo argomento vengono illustrati i seguenti scenari di sfocatura dei client abilitati da DWM.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-122">This topic discusses the following client blur-behind scenarios that the DWM enables.</span></span>

-   [<span data-ttu-id="6a5e9-123">Aggiunta della sfocatura a un'area specifica dell'area client</span><span class="sxs-lookup"><span data-stu-id="6a5e9-123">Adding Blur to a Specific Region of the Client Area</span></span>](#adding-blur-to-a-specific-region-of-the-client-area)
-   [<span data-ttu-id="6a5e9-124">Estensione della cornice della finestra nell'area client</span><span class="sxs-lookup"><span data-stu-id="6a5e9-124">Extending the Window Frame into the Client Area</span></span>](#extending-the-window-frame-into-the-client-area)
-   [<span data-ttu-id="6a5e9-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6a5e9-125">Related topics</span></span>](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a><span data-ttu-id="6a5e9-126">Aggiunta della sfocatura a un'area specifica dell'area client</span><span class="sxs-lookup"><span data-stu-id="6a5e9-126">Adding Blur to a Specific Region of the Client Area</span></span>

<span data-ttu-id="6a5e9-127">Un'applicazione può applicare l'effetto sfocatura dietro l'intera area client della finestra o a una specifica area secondaria.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-127">An application can apply the blur effect behind the whole client region of the window or to a specific subregion.</span></span> <span data-ttu-id="6a5e9-128">In questo modo, le applicazioni possono aggiungere barre di ricerca e percorso con stile separate visivamente dal resto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-128">This enables applications to add styled path and search bars that are visually separate from the rest of the application.</span></span>

<span data-ttu-id="6a5e9-129">L'API usata in questo scenario è la funzione [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) , che usa la [**sfocatura di DWM dietro le costanti**](dwm-bb-constants.md) e la struttura [**\_ BLURBEHIND di DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) .</span><span class="sxs-lookup"><span data-stu-id="6a5e9-129">The API used in this scenario is the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function, which makes use of the [**DWM Blur Behind Constants**](dwm-bb-constants.md) and the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure.</span></span>

<span data-ttu-id="6a5e9-130">La funzione di esempio seguente, `EnableBlurBehind` , illustra come applicare l'effetto Blur-behind all'intera finestra.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-130">The following example function, `EnableBlurBehind`, illustrates how to apply the blur-behind effect to the whole window.</span></span>


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



<span data-ttu-id="6a5e9-131">Si noti che il **valore null** è specificato nel parametro *hRgnBlur* .</span><span class="sxs-lookup"><span data-stu-id="6a5e9-131">Note that **NULL** is specified in the *hRgnBlur* parameter.</span></span> <span data-ttu-id="6a5e9-132">Ciò indica a DWM di applicare la sfocatura dietro l'intera finestra.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-132">This tells the DWM to apply the blur behind the whole window.</span></span>

<span data-ttu-id="6a5e9-133">Nell'immagine seguente viene illustrato l'effetto Blur-behind applicato all'intera finestra.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-133">The following image illustrates the blur-behind effect applied to the whole window.</span></span>

![effetto Blur-behind applicato a una finestra](images/dwm-blurbehindwindow.png)

<span data-ttu-id="6a5e9-135">Per applicare la sfocatura dietro un'area secondaria, applicare un handle di area valido (HRGN) al membro **hRgnBlur** della struttura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) e aggiungere il flag **DWM \_ BB \_ BLURREGION** al membro **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="6a5e9-135">To apply the blur behind a subregion, apply a valid region handle (HRGN) to the **hRgnBlur** member of the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure and add the **DWM\_BB\_BLURREGION** flag to the **dwFlags** member.</span></span>

<span data-ttu-id="6a5e9-136">Quando si applica l'effetto Blur-behind a un'area secondaria della finestra, viene usato il canale alfa della finestra per l'area non sfocata.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-136">When you apply the blur-behind effect to a subregion of the window, the alpha channel of the window is used for the nonblurred area.</span></span> <span data-ttu-id="6a5e9-137">Ciò può causare una trasparenza imprevista nell'area non sfocata di una finestra.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-137">This can cause an unexpected transparency in the nonblurred region of a window.</span></span> <span data-ttu-id="6a5e9-138">Pertanto, prestare attenzione quando si applica un effetto di sfocatura a un'area secondaria.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-138">Therefore, be careful when you apply a blur effect to a subregion.</span></span>

## <a name="extending-the-window-frame-into-the-client-area"></a><span data-ttu-id="6a5e9-139">Estensione della cornice della finestra nell'area client</span><span class="sxs-lookup"><span data-stu-id="6a5e9-139">Extending the Window Frame into the Client Area</span></span>

<span data-ttu-id="6a5e9-140">Un'applicazione può estendere la sfocatura della cornice della finestra nell'area client.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-140">An application can extend the blur of the window frame into the client area.</span></span> <span data-ttu-id="6a5e9-141">Questa operazione è utile quando si applica l'effetto di sfocatura dietro una finestra con una barra degli strumenti ancorata o si separano visivamente i controlli dal resto di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-141">This is useful when you apply the blur effect behind a window with a docked toolbar or visually separate controls from the rest of an application.</span></span> <span data-ttu-id="6a5e9-142">Questa funzionalità è esposta dalla funzione [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .</span><span class="sxs-lookup"><span data-stu-id="6a5e9-142">This functionality is exposed by the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span>

<span data-ttu-id="6a5e9-143">Per abilitare la sfocatura usando [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), usare la struttura dei [**margini**](/windows/win32/api/uxtheme/ns-uxtheme-margins) per indicare la quantità di estensione nell'area client.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-143">To enable blur by using [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), use the [**MARGINS**](/windows/win32/api/uxtheme/ns-uxtheme-margins) structure to indicate how much to extend into the client area.</span></span> <span data-ttu-id="6a5e9-144">La funzione di esempio seguente, `ExtendIntoClientBottom` , imposta l'estensione della sfocatura nella parte inferiore del frame non client nell'area client.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-144">The following example function, `ExtendIntoClientBottom`, toggles the blur extension on the bottom of the non-client frame into the client area.</span></span>


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



<span data-ttu-id="6a5e9-145">Nell'immagine seguente viene illustrato l'effetto Blur-behind esteso nella parte inferiore dell'area client.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-145">The following image illustrates the blur-behind effect extended into the bottom of the client area.</span></span>

![immagine che mostra l'effetto Blur-behind esteso nella parte inferiore di un'area client](images/dwm-extendedbottom.png)

<span data-ttu-id="6a5e9-147">Disponibile anche tramite il metodo [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) è l'effetto "foglio di vetro", in cui l'effetto di sfocatura viene applicato all'intera superficie della finestra senza bordo visibile della finestra.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-147">Also available through the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) method is the "sheet of glass" effect, where the blur effect is applied to the whole surface of the window without a visible window border.</span></span> <span data-ttu-id="6a5e9-148">Nell'esempio seguente viene illustrato questo effetto in cui viene eseguito il rendering dell'area client senza un bordo della finestra.</span><span class="sxs-lookup"><span data-stu-id="6a5e9-148">The following example demonstrates this effect where the client area is rendered without a window border.</span></span>


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



<span data-ttu-id="6a5e9-149">Nell'immagine seguente viene illustrata la sfocatura nello stile della finestra "foglio di vetro".</span><span class="sxs-lookup"><span data-stu-id="6a5e9-149">The following image illustrates the blur-behind in the "sheet of glass" window style.</span></span>

![immagine che illustra l'effetto Blur-behind nello stile della finestra "foglio di vetro"](images/dwm-sheetofglass.png)

## <a name="related-topics"></a><span data-ttu-id="6a5e9-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6a5e9-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a5e9-152">Cenni preliminari di Gestione finestre desktop</span><span class="sxs-lookup"><span data-stu-id="6a5e9-152">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> <dt>

[<span data-ttu-id="6a5e9-153">Abilitare e controllare la composizione DWM</span><span class="sxs-lookup"><span data-stu-id="6a5e9-153">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="6a5e9-154">Considerazioni sulle prestazioni e procedure consigliate</span><span class="sxs-lookup"><span data-stu-id="6a5e9-154">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 