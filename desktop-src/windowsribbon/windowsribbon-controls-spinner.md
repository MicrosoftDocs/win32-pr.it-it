---
title: Spinner
description: Spinner è un controllo composito costituito da un pulsante di incremento, un pulsante di decremento e un controllo di modifica, tutti usati per fornire valori decimali all'applicazione.
ms.assetid: 63689ed3-7326-4f7a-b700-d89e9b501ef1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56103db221dfb8cc60783da20cf33a82c95ea17f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473767"
---
# <a name="spinner"></a>Spinner

Spinner è un controllo composito costituito da un pulsante di incremento, un pulsante di decremento e un controllo di modifica, tutti usati per fornire valori decimali all'applicazione.

-   [Dettagli](#details)
-   [Proprietà del selettore](#spinner-properties)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="details"></a>Dettagli

Nella schermata seguente viene illustrato lo spinner della barra multifunzione.

![Screenshot di un controllo casella di selezione nella barra multifunzione di Windows Live Moviemaker.](images/controls/spinner.png)

## <a name="spinner-properties"></a>Proprietà del selettore

Il framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo Spinner.

In genere, una proprietà Spinner viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) L'evento di invalidazione viene gestito e la proprietà viene aggiornata dal metodo di callback [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

Il metodo di callback [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha eseguito una query per un valore di proprietà aggiornato, fino a quando la proprietà non è richiesta dal framework. Ad esempio, quando una scheda viene attivata e un controllo viene visualizzato nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo Spinner.




| Chiave di proprietà | Note | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-decimalplaces.md">UI_PKEY_DecimalPlaces</a> | Può essere aggiornato solo tramite invalidazione. | 
| <a href="windowsribbon-reference-properties-uipkey-decimalvalue.md">UI_PKEY_DecimalValue</a> | Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.<blockquote>[!Note]<br />Se il comando associato al controllo viene invalidato tramite una chiamata a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, il framework esegue una query su questa proprietà quando viene passato come valore dei <code>UI_INVALIDATIONS_VALUE</code> <em>flag</em>.</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-formatstring.md">UI_PKEY_FormatString</a> | Può essere aggiornato solo tramite invalidazione. | 
| <a href="windowsribbon-reference-properties-uipkey-increment.md">UI_PKEY_Increment</a> | Può essere aggiornato solo tramite invalidazione. | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Può essere aggiornato solo tramite invalidazione. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Può essere aggiornato solo tramite invalidazione. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Può essere aggiornato solo tramite invalidazione. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Può essere aggiornato solo tramite invalidazione. | 
| <a href="windowsribbon-reference-properties-uipkey-maxvalue.md">UI_PKEY_MaxValue</a> | Può essere aggiornato solo tramite invalidazione. | 
| <a href="windowsribbon-reference-properties-uipkey-minvalue.md">UI_PKEY_MinValue</a> | Può essere aggiornato solo tramite invalidazione. | 
| <a href="windowsribbon-reference-properties-uipkey-representativestring.md">UI_PKEY_RepresentativeString</a> | Può essere aggiornato solo tramite invalidazione. | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Può essere aggiornato solo tramite invalidazione. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Può essere aggiornato solo tramite invalidazione. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Può essere aggiornato solo tramite invalidazione. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Può essere aggiornato solo tramite invalidazione. | 




 

La sezione di codice seguente illustra come vengono aggiornate le varie proprietà del controllo Spinner nel [**metodo IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)


```C++
//
//  FUNCTION:    UpdateProperty()
//
//  PURPOSE:    Called by the Ribbon framework when a command property needs 
//                to be updated.
//
//  COMMENTS:    This function is used to provide new command property values for 
//                the spinner when requested by the Ribbon framework.  
//    
STDMETHODIMP CCommandHandler::UpdateProperty(
    UINT nCmdID,
    REFPROPERTYKEY key,
    const PROPVARIANT* ppropvarCurrentValue,
    PROPVARIANT* ppropvarNewValue)
{
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;

    if (nCmdID == IDR_CMD_SPINNER_RESIZE)
    {
        // Set the minimum value
        if (IsEqualPropertyKey(key, UI_PKEY_MinValue))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(-10.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the maximum value
        else if (IsEqualPropertyKey(key, UI_PKEY_MaxValue))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(10.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the increment
        else if (IsEqualPropertyKey(key, UI_PKEY_Increment))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(2.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the number of decimal places
        else if (IsEqualPropertyKey(key, UI_PKEY_DecimalPlaces))
        {
            hr = InitPropVariantFromUInt32(1, ppropvarNewValue);
            hr = S_OK;
        }

        // Set the format string
        else if (IsEqualPropertyKey(key, UI_PKEY_FormatString))
        {
            hr = InitPropVariantFromString(L"px", ppropvarNewValue);
            hr = S_OK;
        }

        // Set the representative string
        else if (IsEqualPropertyKey(key, UI_PKEY_RepresentativeString))
        {
            hr = InitPropVariantFromString(L"AAAAAAA", ppropvarNewValue);
            hr = S_OK;
        }
    }
    return hr;
}
```



## <a name="remarks"></a>Commenti

Se il valore minimo ([UI \_ PKEY \_ MinValue](windowsribbon-reference-properties-uipkey-minvalue.md)) di un controllo Spinner viene inizializzato su 0,0, l'applicazione deve assicurarsi che qualsiasi valore successivo fornito dal controllo non sia uguale a -0,0 (zero negativo). Se lo spinner fornisce il valore -0.0, l'applicazione deve reimpostare questo valore su 0,0 (zero positivo) usando il metodo [**IUIFramework::SetUICommandProperty,**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) come illustrato nell'esempio seguente di un metodo [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) per un controllo Spinner.

> [!Note]  
> Se questo test non viene eseguito e il valore non viene modificato, nel campo di modifica del controllo viene visualizzata la stringa "Auto".

 


```C++
//
//  FUNCTION:    Execute()
//
//  PURPOSE:    Called by the Ribbon framework when a command is executed by the user.  
//                For this sample, when an increment or decrement button is pressed or
//                a new value is entered in the Spinner edit field.
//
STDMETHODIMP CCommandHandler::Execute(
      UINT nCmdID,
      UI_EXECUTIONVERB verb,
      const PROPERTYKEY* key,
      const PROPVARIANT* ppropvarValue,
      IUISimplePropertySet* pCommandExecutionProperties)
{
    UNREFERENCED_PARAMETER(pCommandExecutionProperties);

    HRESULT hr = E_NOTIMPL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        RenderParam param;
        g_renderer.GetRenderParam(&param);

        if (nCmdID == IDR_CMD_SPINNER_RESIZE)
        {
            // Spinner value is negative.
            if (!(ppropvarValue->decVal.sign == 0))
            {
                // Check if the value supplied by the Spinner is -0
                // and correct the value if necessary.
                // If this value is left uncorrected, the edit field 
                // of the control will display the string "Auto" when 
                // UI_PKEY_MinValue is set to 0.
                if (ppropvarValue->decVal.Lo64 == 0)
                {
                    // Initialize a new PROPVARIANT structure.
                    PROPVARIANT m_varNewVal;
                    PropVariantInit(&m_varNewVal);

                    // The replacement DECIMAL value.
                    DECIMAL m_dVal;
                    hr = VarDecFromI4(0, &m_dVal);
                    if (FAILED(hr))
                    {
                        return hr;
                    }
                    
                    // Initialize the new DECIMAL value.
                    UIInitPropertyFromDecimal(UI_PKEY_DecimalValue, m_dVal, &m_varNewVal);

                    // Set the UI_PKEY_DecimalValue to the new DECIMAL value.
                    hr = g_pFramework->SetUICommandProperty(nCmdID, UI_PKEY_DecimalValue, m_varNewVal);
                    if (FAILED(hr))
                    {
                        return hr;
                    }
                }
                // Decrease size of shape in document space.
                param.iShapeSizeIncrement = -ppropvarValue->intVal;
            }
            // Spinner value is positive.
            else
            {
                // Increase size of shape in document space.
                param.iShapeSizeIncrement = ppropvarValue->intVal;
            }
        }
        g_renderer.UpdateRenderParam(param);
    }

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Libreria di controlli Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup spinner**](windowsribbon-element-spinner.md)
</dt> </dl>

