---
title: Popup contesto
description: Un popup del contesto è il controllo principale nella visualizzazione ContextPopup del Framework della barra multifunzione di Windows.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77441cc3cdcc9212d27d2230d76d2618f1831ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300052"
---
# <a name="context-popup"></a><span data-ttu-id="bc64a-103">Popup contesto</span><span class="sxs-lookup"><span data-stu-id="bc64a-103">Context Popup</span></span>

<span data-ttu-id="bc64a-104">Un popup del contesto è il controllo principale nella [**visualizzazione ContextPopup**](windowsribbon-element-contextpopup.md) del Framework della barra multifunzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="bc64a-104">A Context Popup is the principal control in the [**ContextPopup View**](windowsribbon-element-contextpopup.md) of the Windows Ribbon framework.</span></span> <span data-ttu-id="bc64a-105">Si tratta di un sistema di menu di scelta rapida che viene esposto solo dal Framework come estensione di un'implementazione della barra multifunzione: il Framework non espone il popup del contesto come controllo indipendente.</span><span class="sxs-lookup"><span data-stu-id="bc64a-105">It is a rich context menu system that is only exposed by the framework as an extension to a Ribbon implementation—the framework does not expose the Context Popup as an independent control.</span></span>

-   [<span data-ttu-id="bc64a-106">Componenti del popup di contesto</span><span class="sxs-lookup"><span data-stu-id="bc64a-106">Components of the Context Popup</span></span>](#context-popup)
-   [<span data-ttu-id="bc64a-107">Implementare il popup del contesto</span><span class="sxs-lookup"><span data-stu-id="bc64a-107">Implement the Context Popup</span></span>](#implement-the-context-popup)
    -   [<span data-ttu-id="bc64a-108">markup</span><span class="sxs-lookup"><span data-stu-id="bc64a-108">Markup</span></span>](#markup)
    -   [<span data-ttu-id="bc64a-109">Codice</span><span class="sxs-lookup"><span data-stu-id="bc64a-109">Code</span></span>](#code)
-   [<span data-ttu-id="bc64a-110">Proprietà popup del contesto</span><span class="sxs-lookup"><span data-stu-id="bc64a-110">Context Popup Properties</span></span>](#context-popup-properties)
-   [<span data-ttu-id="bc64a-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc64a-111">Related topics</span></span>](#related-topics)

## <a name="components-of-the-context-popup"></a><span data-ttu-id="bc64a-112">Componenti del popup di contesto</span><span class="sxs-lookup"><span data-stu-id="bc64a-112">Components of the Context Popup</span></span>

<span data-ttu-id="bc64a-113">Il popup del contesto è un contenitore logico per il menu di scelta rapida e Mini-Toolbar i controlli secondari esposti tramite gli elementi di markup [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**MiniToolbar**](windowsribbon-element-minitoolbar.md) , rispettivamente:</span><span class="sxs-lookup"><span data-stu-id="bc64a-113">The Context Popup is a logical container for the Context Menu and Mini-Toolbar sub-controls that are exposed through the [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) markup elements, respectively:</span></span>

-   <span data-ttu-id="bc64a-114">Il [**ContextMenu**](windowsribbon-element-contextmenu.md) espone un menu di comandi e raccolte.</span><span class="sxs-lookup"><span data-stu-id="bc64a-114">The [**ContextMenu**](windowsribbon-element-contextmenu.md) exposes a menu of Commands and galleries.</span></span>
-   <span data-ttu-id="bc64a-115">[**MiniToolbar**](windowsribbon-element-minitoolbar.md) espone una barra degli strumenti mobile di diversi comandi, raccolte e controlli complessi, ad esempio il [controllo del tipo di carattere](windowsribbon-controls-fontcontrol.md) e la [casella combinata](windowsribbon-controls-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="bc64a-115">The [**MiniToolbar**](windowsribbon-element-minitoolbar.md) exposes a floating toolbar of various Commands, galleries, and complex controls such as the [Font Control](windowsribbon-controls-fontcontrol.md) and the [Combo Box](windowsribbon-controls-combobox.md).</span></span>

<span data-ttu-id="bc64a-116">Ogni sottocontrollo può essere visualizzato al massimo una volta in un popup del contesto.</span><span class="sxs-lookup"><span data-stu-id="bc64a-116">Each sub-control can appear at most once in a Context Popup.</span></span>

<span data-ttu-id="bc64a-117">Lo screenshot seguente illustra il popup di contesto e i relativi controlli secondari.</span><span class="sxs-lookup"><span data-stu-id="bc64a-117">The following screen shot illustrates the Context Popup and its constituent sub-controls.</span></span>

![screenshot con callout che mostrano i componenti dell'interfaccia utente contestuale della barra multifunzione.](images/controls/contextpopup.png)

<span data-ttu-id="bc64a-119">Il contesto popup è puramente concettuale e non espone alcuna funzionalità dell'interfaccia utente, ad esempio il posizionamento o il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="bc64a-119">The Context Popup is purely conceptual and does not expose any UI functionality itself, such as positioning or sizing.</span></span>

> [!Note]  
> <span data-ttu-id="bc64a-120">Il popup di contesto viene in genere visualizzato facendo clic con il pulsante destro del mouse (o tramite il tasto di scelta rapida MAIUSC + F10) su un oggetto di interesse.</span><span class="sxs-lookup"><span data-stu-id="bc64a-120">The Context Popup is typically displayed by right-clicking the mouse (or through the keyboard shortcut SHIFT+F10) on an object of interest.</span></span> <span data-ttu-id="bc64a-121">Tuttavia, i passaggi necessari per visualizzare il popup del contesto sono definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc64a-121">However, the steps required to display the Context Popup are defined by the application.</span></span>

 

## <a name="implement-the-context-popup"></a><span data-ttu-id="bc64a-122">Implementare il popup del contesto</span><span class="sxs-lookup"><span data-stu-id="bc64a-122">Implement the Context Popup</span></span>

<span data-ttu-id="bc64a-123">Analogamente ad altri controlli Framework della barra multifunzione di Windows, il popup del contesto viene implementato tramite un componente di markup che specifica i dettagli di presentazione e un componente di codice che ne determina la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="bc64a-123">In similar fashion to other Windows Ribbon framework controls, the Context Popup is implemented through a markup component that specifies its presentation details and a code component that governs its functionality.</span></span>

<span data-ttu-id="bc64a-124">Nella tabella seguente sono elencati i controlli supportati da ogni sottocontrollo popup del contesto.</span><span class="sxs-lookup"><span data-stu-id="bc64a-124">The following table lists the controls that are supported by each Context Popup sub-control.</span></span>



| <span data-ttu-id="bc64a-125">Control</span><span class="sxs-lookup"><span data-stu-id="bc64a-125">Control</span></span>                                                                  | <span data-ttu-id="bc64a-126">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="bc64a-126">Mini-Toolbar</span></span> | <span data-ttu-id="bc64a-127">Menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="bc64a-127">Context Menu</span></span> |
|--------------------------------------------------------------------------|--------------|--------------|
| [<span data-ttu-id="bc64a-128">Button</span><span class="sxs-lookup"><span data-stu-id="bc64a-128">Button</span></span>](windowsribbon-controls-button.md)                              | <span data-ttu-id="bc64a-129">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-129">x</span></span>            | <span data-ttu-id="bc64a-130">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-130">x</span></span>            |
| [<span data-ttu-id="bc64a-131">Casella di controllo</span><span class="sxs-lookup"><span data-stu-id="bc64a-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)                         | <span data-ttu-id="bc64a-132">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-132">x</span></span>            | <span data-ttu-id="bc64a-133">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-133">x</span></span>            |
| [<span data-ttu-id="bc64a-134">ComboBox</span><span class="sxs-lookup"><span data-stu-id="bc64a-134">Combo Box</span></span>](windowsribbon-controls-combobox.md)                         | <span data-ttu-id="bc64a-135">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-135">x</span></span>            |              |
| [<span data-ttu-id="bc64a-136">Pulsante a discesa</span><span class="sxs-lookup"><span data-stu-id="bc64a-136">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)            | <span data-ttu-id="bc64a-137">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-137">x</span></span>            | <span data-ttu-id="bc64a-138">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-138">x</span></span>            |
| [<span data-ttu-id="bc64a-139">Selezione colori a discesa</span><span class="sxs-lookup"><span data-stu-id="bc64a-139">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | <span data-ttu-id="bc64a-140">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-140">x</span></span>            | <span data-ttu-id="bc64a-141">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-141">x</span></span>            |
| [<span data-ttu-id="bc64a-142">Raccolta a discesa</span><span class="sxs-lookup"><span data-stu-id="bc64a-142">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)          | <span data-ttu-id="bc64a-143">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-143">x</span></span>            | <span data-ttu-id="bc64a-144">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-144">x</span></span>            |
| [<span data-ttu-id="bc64a-145">Controllo carattere</span><span class="sxs-lookup"><span data-stu-id="bc64a-145">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | <span data-ttu-id="bc64a-146">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-146">x</span></span>            |              |
| [<span data-ttu-id="bc64a-147">Pulsante della Guida</span><span class="sxs-lookup"><span data-stu-id="bc64a-147">Help Button</span></span>](windowsribbon-controls-helpbutton.md)                     |              |              |
| [<span data-ttu-id="bc64a-148">Raccolta della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="bc64a-148">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)          |              |              |
| [<span data-ttu-id="bc64a-149">Spinner</span><span class="sxs-lookup"><span data-stu-id="bc64a-149">Spinner</span></span>](windowsribbon-controls-spinner.md)                            |              |              |
| [<span data-ttu-id="bc64a-150">Pulsante di divisione</span><span class="sxs-lookup"><span data-stu-id="bc64a-150">Split Button</span></span>](windowsribbon-controls-splitbutton.md)                   | <span data-ttu-id="bc64a-151">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-151">x</span></span>            | <span data-ttu-id="bc64a-152">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-152">x</span></span>            |
| [<span data-ttu-id="bc64a-153">Raccolta di pulsanti di suddivisione</span><span class="sxs-lookup"><span data-stu-id="bc64a-153">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)    | <span data-ttu-id="bc64a-154">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-154">x</span></span>            | <span data-ttu-id="bc64a-155">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-155">x</span></span>            |
| [<span data-ttu-id="bc64a-156">Interruttore</span><span class="sxs-lookup"><span data-stu-id="bc64a-156">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)                 | <span data-ttu-id="bc64a-157">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-157">x</span></span>            | <span data-ttu-id="bc64a-158">x</span><span class="sxs-lookup"><span data-stu-id="bc64a-158">x</span></span>            |



 

### <a name="markup"></a><span data-ttu-id="bc64a-159">markup</span><span class="sxs-lookup"><span data-stu-id="bc64a-159">Markup</span></span>

<span data-ttu-id="bc64a-160">Ogni sottocontrollo popup del contesto deve essere dichiarato singolarmente nel markup.</span><span class="sxs-lookup"><span data-stu-id="bc64a-160">Each Context Popup sub-control must be declared individually in markup.</span></span>

### <a name="mini-toolbar"></a><span data-ttu-id="bc64a-161">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="bc64a-161">Mini-Toolbar</span></span>

<span data-ttu-id="bc64a-162">Quando si aggiungono controlli a una mini barra degli strumenti popup del contesto, è necessario considerare le due raccomandazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc64a-162">When adding controls to a Context Popup Mini-Toolbar, the following two recommendations should be considered:</span></span>

-   <span data-ttu-id="bc64a-163">I controlli devono essere altamente riconoscibili e fornire funzionalità evidenti.</span><span class="sxs-lookup"><span data-stu-id="bc64a-163">Controls should be highly recognizable and provide obvious functionality.</span></span> <span data-ttu-id="bc64a-164">La familiarità è chiave, perché le etichette e le descrizioni comandi non vengono esposte per i controlli Mini-Toolbar.</span><span class="sxs-lookup"><span data-stu-id="bc64a-164">Familiarity is key, as labels and tooltips are not exposed for Mini-Toolbar controls.</span></span>
-   <span data-ttu-id="bc64a-165">Ogni comando esposto da un controllo deve essere presentato altrove nell'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="bc64a-165">Each Command exposed by a control should be presented elsewhere in the ribbon UI.</span></span> <span data-ttu-id="bc64a-166">Il Mini-Toolbar non supporta la navigazione da tastiera.</span><span class="sxs-lookup"><span data-stu-id="bc64a-166">The Mini-Toolbar does not support keyboard navigation.</span></span>

<span data-ttu-id="bc64a-167">Nell'esempio seguente viene illustrato il markup di base per un elemento [**MiniToolbar**](windowsribbon-element-minitoolbar.md) che contiene tre controlli [Button](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="bc64a-167">The following example demonstrates the basic markup for a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="bc64a-168">Viene specificato un elemento [**MenuGroup**](windowsribbon-element-menugroup.md) per ogni riga di controlli nella mini-barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="bc64a-168">One [**MenuGroup**](windowsribbon-element-menugroup.md) element is specified for each row of controls in the Mini-Toolbar.</span></span>

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a><span data-ttu-id="bc64a-169">Menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="bc64a-169">Context Menu</span></span>

<span data-ttu-id="bc64a-170">Nell'esempio seguente viene illustrato il markup di base per un elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) che contiene tre controlli [Button](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="bc64a-170">The following example demonstrates the basic markup for a [**ContextMenu**](windowsribbon-element-contextmenu.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="bc64a-171">Ogni set di controlli nell'elemento [**MenuGroup**](windowsribbon-element-menugroup.md) è separato da una barra orizzontale nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="bc64a-171">Each set of controls in the [**MenuGroup**](windowsribbon-element-menugroup.md) element is separated by a horizontal bar in the Context Menu.</span></span>

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



<span data-ttu-id="bc64a-172">Sebbene un popup del contesto possa contenere al massimo uno di ogni sottocontrollo, sono valide più dichiarazioni di elementi [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**MiniToolbar**](windowsribbon-element-minitoolbar.md) nel markup della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="bc64a-172">Although a Context Popup can contain at most one of each sub-control, multiple [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element declarations in the Ribbon markup are valid.</span></span> <span data-ttu-id="bc64a-173">Questo consente a un'applicazione di supportare diverse combinazioni di menu di scelta rapida e controlli Mini-Toolbar, in base ai criteri definiti dall'applicazione, ad esempio il contesto dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bc64a-173">This allows an application to support various combinations of Context Menu and Mini-Toolbar controls, based on criteria defined by the application, such as workspace context.</span></span>

<span data-ttu-id="bc64a-174">Per ulteriori informazioni, vedere l'elemento [**ContextMap**](windowsribbon-element-contextmap.md) .</span><span class="sxs-lookup"><span data-stu-id="bc64a-174">For more information, see the [**ContextMap**](windowsribbon-element-contextmap.md) element.</span></span>

<span data-ttu-id="bc64a-175">Nell'esempio seguente viene illustrato il markup di base per l'elemento [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="bc64a-175">The following example demonstrates the basic markup for the [**ContextPopup**](windowsribbon-element-contextpopup.md) element.</span></span>


```C++
<ContextPopup>
  <ContextPopup.MiniToolbars>
    <MiniToolbar Name="MiniToolbar">
      <MenuGroup>
        <Button CommandName="cmdButton1" />
        <Button CommandName="cmdButton2" />
        <Button CommandName="cmdButton3" />
      </MenuGroup>
    </MiniToolbar>
  </ContextPopup.MiniToolbars>
  <ContextPopup.ContextMenus>
    <ContextMenu Name="ContextMenu">
      <MenuGroup>
        <Button CommandName="cmdCut" />
        <Button CommandName="cmdCopy" />
        <Button CommandName="cmdPaste" />
      </MenuGroup>
    </ContextMenu>
  </ContextPopup.ContextMenus>
  <ContextPopup.ContextMaps>
    <ContextMap CommandName="cmdContextMap" ContextMenu="ContextMenu" MiniToolbar="MiniToolbar"/>
  </ContextPopup.ContextMaps>
</ContextPopup>
```



### <a name="code"></a><span data-ttu-id="bc64a-176">Codice</span><span class="sxs-lookup"><span data-stu-id="bc64a-176">Code</span></span>

<span data-ttu-id="bc64a-177">Per richiamare un popup del contesto, viene chiamato il metodo [**IUIContextualUI:: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) quando la finestra di primo livello dell'applicazione Ribbon riceve una notifica di WM \_ ContextMenu.</span><span class="sxs-lookup"><span data-stu-id="bc64a-177">To invoke a Context Popup, the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method is called when the top-level window of the Ribbon application receives a WM\_CONTEXTMENU notification.</span></span>

<span data-ttu-id="bc64a-178">Questo esempio illustra come gestire la notifica di WM \_ ContextMenu nel metodo WndProc () dell'applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="bc64a-178">This example demonstrates how to handle the WM\_CONTEXTMENU notification in the WndProc() method of the Ribbon application.</span></span>


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



<span data-ttu-id="bc64a-179">Nell'esempio seguente viene illustrato come un'applicazione Ribbon può mostrare il popup del contesto in una posizione dello schermo specifica usando il metodo [**IUIContextualUI:: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) .</span><span class="sxs-lookup"><span data-stu-id="bc64a-179">The following example demonstrates how a Ribbon application can show the Context Popup at a specific screen location using the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method.</span></span>

<span data-ttu-id="bc64a-180">GetCurrentContext () ha un valore `cmdContextMap` come definito nell'esempio di markup precedente.</span><span class="sxs-lookup"><span data-stu-id="bc64a-180">GetCurrentContext() has a value of `cmdContextMap` as defined in the preceding markup example.</span></span>

<span data-ttu-id="bc64a-181">g \_ pApplication è un riferimento all'interfaccia [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) .</span><span class="sxs-lookup"><span data-stu-id="bc64a-181">g\_pApplication is a reference to the [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) interface.</span></span>


```C++
HRESULT ShowContextualUI(POINT& ptLocation, HWND hWnd)
{
  GetDisplayLocation(ptLocation, hWnd);

  HRESULT hr = E_FAIL;

  IUIContextualUI* pContextualUI = NULL;
 
  if (SUCCEEDED(g_pFramework->GetView(
                                g_pApplication->GetCurrentContext(), 
                                IID_PPV_ARGS(&pContextualUI))))
  {
    hr = pContextualUI->ShowAtLocation(ptLocation.x, ptLocation.y);
    pContextualUI->Release();
  }

  return hr;
}
```



<span data-ttu-id="bc64a-182">Il riferimento a [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) può essere rilasciato prima che il popup del contesto venga eliminato, come illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="bc64a-182">The reference to [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) can be released before the Context Popup is dismissed, as shown in the preceding example.</span></span> <span data-ttu-id="bc64a-183">Tuttavia, il riferimento deve essere rilasciato a un certo punto per evitare perdite di memoria.</span><span class="sxs-lookup"><span data-stu-id="bc64a-183">However, the reference must be released at some point to avoid memory leaks.</span></span>

> [!Caution]  
> <span data-ttu-id="bc64a-184">Il Mini-Toolbar dispone di un effetto di dissolvenza incorporato basato sulla prossimità del puntatore del mouse.</span><span class="sxs-lookup"><span data-stu-id="bc64a-184">The Mini-Toolbar has a built-in fade effect that is based on the proximity of the mouse pointer.</span></span> <span data-ttu-id="bc64a-185">Per questo motivo, è consigliabile che il Mini-Toolbar venga visualizzato il più vicino possibile al puntatore del mouse.</span><span class="sxs-lookup"><span data-stu-id="bc64a-185">For this reason, it is recommended that the Mini-Toolbar be displayed as close to the mouse pointer as possible.</span></span> <span data-ttu-id="bc64a-186">In caso contrario, a causa dei meccanismi di visualizzazione in conflitto, è possibile che l'Mini-Toolbar non esegua il rendering come previsto.</span><span class="sxs-lookup"><span data-stu-id="bc64a-186">Otherwise, due to the conflicting display mechanisms, the Mini-Toolbar may not render as expected.</span></span>

 

## <a name="context-popup-properties"></a><span data-ttu-id="bc64a-187">Proprietà popup del contesto</span><span class="sxs-lookup"><span data-stu-id="bc64a-187">Context Popup Properties</span></span>

<span data-ttu-id="bc64a-188">Non sono presenti chiavi di proprietà associate al controllo popup del contesto.</span><span class="sxs-lookup"><span data-stu-id="bc64a-188">There are no property keys associated with the Context Popup control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc64a-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc64a-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc64a-190">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="bc64a-190">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="bc64a-191">Esempio ContextPopup</span><span class="sxs-lookup"><span data-stu-id="bc64a-191">ContextPopup Sample</span></span>](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 