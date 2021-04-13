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
# <a name="how-to-return-properties-from-a-ui-automation-provider"></a><span data-ttu-id="d6851-103">Come restituire proprietà da un provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d6851-103">How to Return Properties from a UI Automation Provider</span></span>

<span data-ttu-id="d6851-104">Questo argomento contiene codice di esempio che illustra in che modo un provider di automazione interfaccia utente Microsoft restituisce le proprietà di un elemento dell'interfaccia utente alle applicazioni client.</span><span class="sxs-lookup"><span data-stu-id="d6851-104">This topic contains example code that shows how a Microsoft UI Automation provider returns properties of a UI element to client applications.</span></span>

<span data-ttu-id="d6851-105">Per recuperare un valore di proprietà dal provider, l'automazione interfaccia utente chiama l'implementazione di un provider del metodo [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) , passando l'ID della proprietà da recuperare e un puntatore a una struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .</span><span class="sxs-lookup"><span data-stu-id="d6851-105">To retrieve a property value from the provider, UI Automation calls a provider's implementation of the [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) method, passing the ID of the property to retrieve, and a pointer to a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure.</span></span> <span data-ttu-id="d6851-106">Se il provider supporta la proprietà specificata, copia il tipo di dati e il valore della proprietà nella struttura **Variant** .</span><span class="sxs-lookup"><span data-stu-id="d6851-106">If the provider supports the specified property, it copies the data type and value of the property into the **VARIANT** structure.</span></span> <span data-ttu-id="d6851-107">Se la proprietà non è supportata, il provider imposta il membro **VT** della struttura **Variant** su VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="d6851-107">If the property is not supported, the provider sets the **vt** member of the **VARIANT** structure to VT\_EMPTY.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d6851-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d6851-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d6851-109">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d6851-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d6851-110">Cenni preliminari sulle proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d6851-110">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="d6851-111">Procedure per i provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d6851-111">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 