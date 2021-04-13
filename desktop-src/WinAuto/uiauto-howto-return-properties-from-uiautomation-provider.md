---
title: Come restituire proprietà da un provider di automazione interfaccia utente
description: Questo argomento contiene codice di esempio che illustra in che modo un provider di automazione interfaccia utente Microsoft restituisce le proprietà di un elemento dell'interfaccia utente alle applicazioni client.
ms.assetid: 6932de16-5548-4aa3-9f29-5daa57bb202b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4133a53df3c59e6d5c93b1c9cd8e6aa942b4bd56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399082"
---
# <a name="how-to-return-properties-from-a-ui-automation-provider"></a>Come restituire proprietà da un provider di automazione interfaccia utente

Questo argomento contiene codice di esempio che illustra in che modo un provider di automazione interfaccia utente Microsoft restituisce le proprietà di un elemento dell'interfaccia utente alle applicazioni client.

Per recuperare un valore di proprietà dal provider, l'automazione interfaccia utente chiama l'implementazione di un provider del metodo [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) , passando l'ID della proprietà da recuperare e un puntatore a una struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) . Se il provider supporta la proprietà specificata, copia il tipo di dati e il valore della proprietà nella struttura **Variant** . Se la proprietà non è supportata, il provider imposta il membro **VT** della struttura **Variant** su VT \_ Empty.


```C++
IFACEMETHODIMP Provider::GetPropertyValue(PROPERTYID propertyId, VARIANT* pRetVal)
{
    // The Name property is typically the same as the Caption property of the 
    // control window, if it has one. Here, the Name is overridden for the 
    // sake of illustration. 
    if (propertyId == UIA_NamePropertyId) 
    {
        pRetVal->vt = VT_BSTR;
        pRetVal->bstrVal = SysAllocString(L"Custom button");
    }
    
    else if (propertyId == UIA_ControlTypePropertyId) 
    {
        pRetVal->vt = VT_I4;
        pRetVal->lVal = UIA_ButtonControlTypeId; 
    }

    else if (propertyId == UIA_IsContentElementPropertyId) 
    {
        pRetVal->vt = VT_BOOL;
        pRetVal->lVal = TRUE; 
    }

    else if (propertyId == UIA_IsControlElementPropertyId) 
    {
        pRetVal->vt = VT_BOOL;
        pRetVal->lVal = TRUE; 
    }

    //
    // Return other properties as appropriate for the control type. 
    //

    else
    {
        pRetVal->vt = VT_EMPTY;
        // UI Automation will attempt to get the property from the  
        // provider for window that hosts the control.
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sulle proprietà di automazione interfaccia utente](uiauto-propertiesoverview.md)
</dt> <dt>

[Procedure per i provider di automazione interfaccia utente](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 