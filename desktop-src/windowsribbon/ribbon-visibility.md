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
# <a name="displaying-the-ribbon"></a>Visualizzazione della barra multifunzione

Il Framework della barra multifunzione di Windows espone un set di proprietà che consentono a un'applicazione di specificare la modalità di visualizzazione dell'interfaccia utente della barra multifunzione in fase di esecuzione.

-   [Introduzione](#introduction)
-   [Ridurre a icona la barra multifunzione](#minimize-the-ribbon)
-   [Nascondi barra multifunzione](#hide-the-ribbon)
-   [Esempio](#example)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Per ingrandire l'area disponibile per lo spazio del documento (o la porta di visualizzazione) di un'applicazione di Framework della barra multifunzione, un'applicazione può specificare se l'interfaccia utente della barra multifunzione è visibile o nascosta e, quando è visibile, se la barra multifunzione è in uno stato espanso o compresso.

Le [chiavi di proprietà del Framework](windowsribbon-reference-properties-framework.md) elencate nella tabella seguente vengono usate per impostare in modo esplicito le caratteristiche di visualizzazione dell'interfaccia utente della barra multifunzione in un'applicazione di Framework della barra multifunzione. Queste proprietà non hanno effetto sulla visualizzazione del controllo [popup del contesto](windowsribbon-controls-contextpopup.md) .



| Stato di visualizzazione         | Chiave della proprietà Ribbon                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| Espanso o compresso | [Interfaccia utente \_ pkey \_ ridotta a icona](windowsribbon-reference-properties-uipkey-minimized.md) |
| Visibile o nascosto     | [Interfaccia utente \_ pkey \_ visualizzabile](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a>Ridurre a icona la barra multifunzione

Un'applicazione di Framework della barra multifunzione può impostare in modo dinamico lo stato ridotto a icona della barra dei comandi della barra multifunzione impostando il valore della chiave della proprietà [pkey dell'interfaccia utente \_ \_ ridotta](windowsribbon-reference-properties-uipkey-minimized.md) su **true** o **false**.



| Stato di visualizzazione | Valore chiave proprietà |
|---------------|--------------------|
| Esteso      | **false**          |
| Collapsed     | **true**           |



 

Quando l'interfaccia utente della barra multifunzione è in uno stato ridotto a icona, la riga della scheda della barra multifunzione rimane visibile e completamente funzionante.

Lo screenshot seguente mostra la barra multifunzione nello stato ridotto a icona.

![screenshot che mostra l'interfaccia utente della barra multifunzione ridotta a icona.](images/overviews/ribbon-minimized.png)

> [!Note]  
> Il Framework della barra multifunzione espone questa funzionalità all'utente finale tramite la selezione della barra multifunzione "Riduci a icona" del menu di scelta rapida della barra multifunzione.

 

## <a name="hide-the-ribbon"></a>Nascondi barra multifunzione

Un'applicazione Ribbon Framework può impostare in modo dinamico lo stato visualizzabile della barra dei comandi della barra multifunzione impostando il valore della chiave della proprietà [ \_ \_ visualizzabile pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-viewable.md) su **true** o **false**.



| Stato di visualizzazione | Valore chiave proprietà |
|---------------|--------------------|
| Visible       | **false**          |
| Nascosto        | **true**           |



 

Diversamente dalla proprietà [pkey dell'interfaccia utente ridotta a \_ \_ icona](windowsribbon-reference-properties-uipkey-minimized.md) , l'impostazione dell' [interfaccia utente \_ pkey \_ VISUALIZZAbile](windowsribbon-reference-properties-uipkey-viewable.md) su **false** rende invisibile l'interfaccia utente della barra multifunzione e completamente inutilizzabile per un utente finale.

Lo screenshot seguente mostra la barra multifunzione nello stato nascosto.

![screenshot che mostra l'interfaccia utente della barra multifunzione nascosta.](images/overviews/ribbon-viewable.png)

## <a name="example"></a>Esempio

Nell'esempio seguente viene illustrato come impostare lo stato dell'interfaccia utente della barra multifunzione in fase di esecuzione.

In questo caso, viene usata la funzione [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) per espandere o comprimere l'interfaccia utente della barra multifunzione in base allo stato di attivazione o [disattivazione](windowsribbon-controls-togglebutton.md)di un interruttore.


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

 

 