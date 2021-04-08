---
title: Visualizzazione della barra multifunzione
description: Il Framework della barra multifunzione di Windows espone un set di proprietà che consentono a un'applicazione di specificare la modalità di visualizzazione dell'interfaccia utente della barra multifunzione in fase di esecuzione.
ms.assetid: c6716183-ef32-4fb2-812a-2d8f27448db5
keywords:
- Barra multifunzione di Windows, personalizzazione dei colori
- Barra multifunzione, personalizzazione dei colori
- personalizzazione dei colori della barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090c77c5b47afd673bc7132a87e3de336683d876
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047036"
---
# <a name="displaying-the-ribbon"></a><span data-ttu-id="0e016-106">Visualizzazione della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="0e016-106">Displaying the Ribbon</span></span>

<span data-ttu-id="0e016-107">Il Framework della barra multifunzione di Windows espone un set di proprietà che consentono a un'applicazione di specificare la modalità di visualizzazione dell'interfaccia utente della barra multifunzione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0e016-107">The Windows Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon UI is displayed at run time.</span></span>

-   [<span data-ttu-id="0e016-108">Introduzione</span><span class="sxs-lookup"><span data-stu-id="0e016-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="0e016-109">Ridurre a icona la barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="0e016-109">Minimize the Ribbon</span></span>](#minimize-the-ribbon)
-   [<span data-ttu-id="0e016-110">Nascondi barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="0e016-110">Hide the Ribbon</span></span>](#hide-the-ribbon)
-   [<span data-ttu-id="0e016-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="0e016-111">Example</span></span>](#example)
-   [<span data-ttu-id="0e016-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e016-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="0e016-113">Introduzione</span><span class="sxs-lookup"><span data-stu-id="0e016-113">Introduction</span></span>

<span data-ttu-id="0e016-114">Per ingrandire l'area disponibile per lo spazio del documento (o la porta di visualizzazione) di un'applicazione di Framework della barra multifunzione, un'applicazione può specificare se l'interfaccia utente della barra multifunzione è visibile o nascosta e, quando è visibile, se la barra multifunzione è in uno stato espanso o compresso.</span><span class="sxs-lookup"><span data-stu-id="0e016-114">To maximize the area available for the document space (or view port) of a Ribbon framework application, an application can specify whether the ribbon UI is visible or hidden and, when visible, whether the ribbon is in an expanded or collapsed state.</span></span>

<span data-ttu-id="0e016-115">Le [chiavi di proprietà del Framework](windowsribbon-reference-properties-framework.md) elencate nella tabella seguente vengono usate per impostare in modo esplicito le caratteristiche di visualizzazione dell'interfaccia utente della barra multifunzione in un'applicazione di Framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="0e016-115">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to explicitly set the display characteristics of the ribbon UI in a Ribbon framework application.</span></span> <span data-ttu-id="0e016-116">Queste proprietà non hanno effetto sulla visualizzazione del controllo [popup del contesto](windowsribbon-controls-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="0e016-116">These properties have no effect on the display of the [Context Popup](windowsribbon-controls-contextpopup.md) control.</span></span>



| <span data-ttu-id="0e016-117">Stato di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="0e016-117">Display State</span></span>         | <span data-ttu-id="0e016-118">Chiave della proprietà Ribbon</span><span class="sxs-lookup"><span data-stu-id="0e016-118">Ribbon Property Key</span></span>                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0e016-119">Espanso o compresso</span><span class="sxs-lookup"><span data-stu-id="0e016-119">Expanded or collapsed</span></span> | [<span data-ttu-id="0e016-120">Interfaccia utente \_ pkey \_ ridotta a icona</span><span class="sxs-lookup"><span data-stu-id="0e016-120">UI\_PKEY\_Minimized</span></span>](windowsribbon-reference-properties-uipkey-minimized.md) |
| <span data-ttu-id="0e016-121">Visibile o nascosto</span><span class="sxs-lookup"><span data-stu-id="0e016-121">Visible or hidden</span></span>     | [<span data-ttu-id="0e016-122">Interfaccia utente \_ pkey \_ visualizzabile</span><span class="sxs-lookup"><span data-stu-id="0e016-122">UI\_PKEY\_Viewable</span></span>](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a><span data-ttu-id="0e016-123">Ridurre a icona la barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="0e016-123">Minimize the Ribbon</span></span>

<span data-ttu-id="0e016-124">Un'applicazione di Framework della barra multifunzione può impostare in modo dinamico lo stato ridotto a icona della barra dei comandi della barra multifunzione impostando il valore della chiave della proprietà [pkey dell'interfaccia utente \_ \_ ridotta](windowsribbon-reference-properties-uipkey-minimized.md) su **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="0e016-124">A Ribbon framework application can dynamically set the minimized state of the ribbon command bar by setting the value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="0e016-125">Stato di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="0e016-125">Display State</span></span> | <span data-ttu-id="0e016-126">Valore chiave proprietà</span><span class="sxs-lookup"><span data-stu-id="0e016-126">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="0e016-127">Esteso</span><span class="sxs-lookup"><span data-stu-id="0e016-127">Expanded</span></span>      | <span data-ttu-id="0e016-128">**false**</span><span class="sxs-lookup"><span data-stu-id="0e016-128">**false**</span></span>          |
| <span data-ttu-id="0e016-129">Collapsed</span><span class="sxs-lookup"><span data-stu-id="0e016-129">Collapsed</span></span>     | <span data-ttu-id="0e016-130">**true**</span><span class="sxs-lookup"><span data-stu-id="0e016-130">**true**</span></span>           |



 

<span data-ttu-id="0e016-131">Quando l'interfaccia utente della barra multifunzione è in uno stato ridotto a icona, la riga della scheda della barra multifunzione rimane visibile e completamente funzionante.</span><span class="sxs-lookup"><span data-stu-id="0e016-131">When the ribbon UI is in a minimized state, the ribbon Tab row remains visible and fully functional.</span></span>

<span data-ttu-id="0e016-132">Lo screenshot seguente mostra la barra multifunzione nello stato ridotto a icona.</span><span class="sxs-lookup"><span data-stu-id="0e016-132">The following screen shot shows the ribbon in the minimized state.</span></span>

![screenshot che mostra l'interfaccia utente della barra multifunzione ridotta a icona.](images/overviews/ribbon-minimized.png)

> [!Note]  
> <span data-ttu-id="0e016-134">Il Framework della barra multifunzione espone questa funzionalità all'utente finale tramite la selezione della barra multifunzione "Riduci a icona" del menu di scelta rapida della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="0e016-134">The Ribbon framework exposes this functionality to the end user through the "Minimize the Ribbon" selection of the ribbon context menu.</span></span>

 

## <a name="hide-the-ribbon"></a><span data-ttu-id="0e016-135">Nascondi barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="0e016-135">Hide the Ribbon</span></span>

<span data-ttu-id="0e016-136">Un'applicazione Ribbon Framework può impostare in modo dinamico lo stato visualizzabile della barra dei comandi della barra multifunzione impostando il valore della chiave della proprietà [ \_ \_ visualizzabile pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-viewable.md) su **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="0e016-136">A Ribbon framework application can dynamically set the viewable state of the ribbon command bar by setting the value of the [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="0e016-137">Stato di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="0e016-137">Display State</span></span> | <span data-ttu-id="0e016-138">Valore chiave proprietà</span><span class="sxs-lookup"><span data-stu-id="0e016-138">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="0e016-139">Visible</span><span class="sxs-lookup"><span data-stu-id="0e016-139">Visible</span></span>       | <span data-ttu-id="0e016-140">**false**</span><span class="sxs-lookup"><span data-stu-id="0e016-140">**false**</span></span>          |
| <span data-ttu-id="0e016-141">Nascosto</span><span class="sxs-lookup"><span data-stu-id="0e016-141">Hidden</span></span>        | <span data-ttu-id="0e016-142">**true**</span><span class="sxs-lookup"><span data-stu-id="0e016-142">**true**</span></span>           |



 

<span data-ttu-id="0e016-143">Diversamente dalla proprietà [pkey dell'interfaccia utente ridotta a \_ \_ icona](windowsribbon-reference-properties-uipkey-minimized.md) , l'impostazione dell' [interfaccia utente \_ pkey \_ VISUALIZZAbile](windowsribbon-reference-properties-uipkey-viewable.md) su **false** rende invisibile l'interfaccia utente della barra multifunzione e completamente inutilizzabile per un utente finale.</span><span class="sxs-lookup"><span data-stu-id="0e016-143">In contrast to the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property, setting [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) to **false** renders the ribbon UI invisible and completely unusable to an end user.</span></span>

<span data-ttu-id="0e016-144">Lo screenshot seguente mostra la barra multifunzione nello stato nascosto.</span><span class="sxs-lookup"><span data-stu-id="0e016-144">The following screen shot shows the ribbon in the hidden state.</span></span>

![screenshot che mostra l'interfaccia utente della barra multifunzione nascosta.](images/overviews/ribbon-viewable.png)

## <a name="example"></a><span data-ttu-id="0e016-146">Esempio</span><span class="sxs-lookup"><span data-stu-id="0e016-146">Example</span></span>

<span data-ttu-id="0e016-147">Nell'esempio seguente viene illustrato come impostare lo stato dell'interfaccia utente della barra multifunzione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0e016-147">The following example demonstrates how to set the state of the ribbon UI at run time.</span></span>

<span data-ttu-id="0e016-148">In questo caso, viene usata la funzione [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) per espandere o comprimere l'interfaccia utente della barra multifunzione in base allo stato di attivazione o [disattivazione](windowsribbon-controls-togglebutton.md)di un interruttore.</span><span class="sxs-lookup"><span data-stu-id="0e016-148">In this case, the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) function is used to expand or collapse the ribbon UI based on the toggle state of a [Toggle Button](windowsribbon-controls-togglebutton.md).</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a Command is executed 
//           by the user. 
//           This example demonstrates a handler for a Toggle Button
//           that sets the minimized state of the ribbon UI.
//
//  NOTES: g_pFramework is a global pointer to an IUIFramework object 
//         that is assigned when the Ribbon framework is initialized.
//
//         g_pRibbon is a global pointer to the IUIRibbon object
//         that is assigned when the Ribbon framework is initialized.
//
STDMETHODIMP CCommandHandler::Execute(
    UINT nCmdID,
    UI_EXECUTIONVERB verb,
    __in_opt const PROPERTYKEY* key,
    __in_opt const PROPVARIANT* ppropvarValue,
    __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
    HRESULT hr = E_FAIL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        switch (nCmdID)
        {
            // Minimize ribbon Command handler.
            case IDR_CMD_MINIMIZE:
                if (g_pFramework)
                {
                    IPropertyStore *pPropertyStore = NULL;
                    hr = g_pRibbon->QueryInterface(__uuidof(IPropertyStore), 
                                                   (void**)&pPropertyStore);
                    if (SUCCEEDED(hr))
                    {
                        if (ppropvarValue != NULL)
                        {
                            // Is the ToggleButton state on or off?
                            BOOL fToggled;
                            hr = UIPropertyToBoolean(*key, *ppropvarValue, &fToggled);

                            if (SUCCEEDED(hr))
                            {
                                // Set the ribbon display state based on the toggle state.
                                PROPVARIANT propvar;
                                PropVariantInit(&propvar);
                                UIInitPropertyFromBoolean(UI_PKEY_Minimized, 
                                                          fToggled, 
                                                          &propvar);
                                hr = pPropertyStore->SetValue(UI_PKEY_Minimized, 
                                                              propvar);
                                pPropertyStore->Commit();
                            }
                            pPropertyStore->Release();
                        }
                    }
                }
                break;
        }
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="0e016-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e016-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e016-150">Proprietà della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="0e016-150">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 