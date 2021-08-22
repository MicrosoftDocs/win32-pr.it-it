---
title: Visualizzazione della barra multifunzione
description: Il Windows del framework della barra multifunzione espone un set di proprietà che consentono a un'applicazione di specificare la modalità di visualizzazione dell'interfaccia utente della barra multifunzione in fase di esecuzione.
ms.assetid: c6716183-ef32-4fb2-812a-2d8f27448db5
keywords:
- Windows Barra multifunzione, personalizzazione dei colori
- Barra multifunzione, personalizzazione dei colori
- personalizzazione dei Windows della barra multifunzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b61bae9bae5620d556f26f6c7103ef222f14892c8ce12acd21289dd7bc53b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964435"
---
# <a name="displaying-the-ribbon"></a>Visualizzazione della barra multifunzione

Il Windows del framework della barra multifunzione espone un set di proprietà che consentono a un'applicazione di specificare la modalità di visualizzazione dell'interfaccia utente della barra multifunzione in fase di esecuzione.

-   [Introduzione](#introduction)
-   [Ridurre a icona la barra multifunzione](#minimize-the-ribbon)
-   [Nascondere la barra multifunzione](#hide-the-ribbon)
-   [Esempio](#example)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Per ingrandire l'area disponibile per lo spazio del documento (o la porta di visualizzazione) di un'applicazione del framework della barra multifunzione, un'applicazione può specificare se l'interfaccia utente della barra multifunzione è visibile o nascosta e, quando visibile, se la barra multifunzione si trova in uno stato espanso o compresso.

Le [chiavi delle proprietà del framework](windowsribbon-reference-properties-framework.md) elencate nella tabella seguente vengono usate per impostare in modo esplicito le caratteristiche di visualizzazione dell'interfaccia utente della barra multifunzione in un'applicazione del framework della barra multifunzione. Queste proprietà non hanno alcun effetto sulla visualizzazione del [controllo Popup](windowsribbon-controls-contextpopup.md) di contesto.



| Stato di visualizzazione         | Chiave delle proprietà della barra multifunzione                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| Espanso o compresso | [Chiave \_ PKEY dell'interfaccia \_ utente ridotta a icona](windowsribbon-reference-properties-uipkey-minimized.md) |
| Visibile o nascosto     | [\_PKEY \_ visualizzabile dell'interfaccia utente](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a>Ridurre a icona la barra multifunzione

Un'applicazione del framework della barra multifunzione può impostare dinamicamente lo stato ridotto a icona della barra dei comandi della barra multifunzione impostando il valore della chiave della proprietà [ \_ UI PKEY \_ Minimized](windowsribbon-reference-properties-uipkey-minimized.md) su **true** o **false.**



| Stato di visualizzazione | Valore chiave proprietà |
|---------------|--------------------|
| Esteso      | **false**          |
| Collapsed     | **true**           |



 

Quando l'interfaccia utente della barra multifunzione si trova in uno stato ridotto a icona, la riga della scheda della barra multifunzione rimane visibile e completamente funzionante.

La schermata seguente mostra la barra multifunzione nello stato ridotto a icona.

![Screenshot che mostra l'interfaccia utente della barra multifunzione ridotta a icona.](images/overviews/ribbon-minimized.png)

> [!Note]  
> Il framework della barra multifunzione espone questa funzionalità all'utente finale tramite la selezione "Riduci a icona la barra multifunzione" del menu di scelta rapida della barra multifunzione.

 

## <a name="hide-the-ribbon"></a>Nascondere la barra multifunzione

Un'applicazione del framework della barra multifunzione può impostare dinamicamente lo stato visualizzabile della barra dei comandi della barra multifunzione impostando il valore della chiave della proprietà [ \_ UI PKEY \_ Viewable](windowsribbon-reference-properties-uipkey-viewable.md) su **true** o **false.**



| Stato di visualizzazione | Valore chiave proprietà |
|---------------|--------------------|
| Visible       | **false**          |
| Nascosto        | **true**           |



 

A differenza della proprietà [ \_ PKEY \_ Minimized](windowsribbon-reference-properties-uipkey-minimized.md) dell'interfaccia utente, l'impostazione di [UI \_ PKEY \_ Viewable](windowsribbon-reference-properties-uipkey-viewable.md) su **false** rende l'interfaccia utente della barra multifunzione invisibile e completamente inutilizzabile per un utente finale.

Lo screenshot seguente mostra la barra multifunzione nello stato nascosto.

![Screenshot che mostra l'interfaccia utente della barra multifunzione nascosta.](images/overviews/ribbon-viewable.png)

## <a name="example"></a>Esempio

L'esempio seguente illustra come impostare lo stato dell'interfaccia utente della barra multifunzione in fase di esecuzione.

In questo caso, la [**funzione IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) viene usata per espandere o comprimere l'interfaccia utente della barra multifunzione in base allo stato di attivazione/disattivazione di [un interruttore.](windowsribbon-controls-togglebutton.md)


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà della barra multifunzione](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 