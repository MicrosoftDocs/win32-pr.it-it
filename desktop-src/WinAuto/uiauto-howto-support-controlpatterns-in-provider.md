---
title: Supportare pattern di controllo in un provider di automazione interfaccia utente
description: Questo argomento illustra in che modo un provider di automazione interfaccia utente Microsoft implementa i pattern di controllo per un controllo. I pattern di controllo consentono alle applicazioni client di manipolare il controllo e ottenere informazioni su di esso.
ms.assetid: 504d0ed8-32c1-43ed-9f71-328a013ab350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54e75fa12dba891bc4eded5fd9763f7825eb7f88
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "104335399"
---
# <a name="support-control-patterns-in-a-ui-automation-provider"></a><span data-ttu-id="15635-104">Supportare pattern di controllo in un provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="15635-104">Support Control Patterns in a UI Automation Provider</span></span>

<span data-ttu-id="15635-105">Questo argomento illustra in che modo un provider di automazione interfaccia utente Microsoft implementa i pattern di controllo per un controllo.</span><span class="sxs-lookup"><span data-stu-id="15635-105">This topic shows how a Microsoft UI Automation provider implements control patterns for a control.</span></span> <span data-ttu-id="15635-106">I pattern di controllo consentono alle applicazioni client di manipolare il controllo e ottenere informazioni su di esso.</span><span class="sxs-lookup"><span data-stu-id="15635-106">Control patterns enable client applications to manipulate the control and get information about it.</span></span>

<span data-ttu-id="15635-107">Un provider implementa un pattern di controllo seguendo questi passaggi principali:</span><span class="sxs-lookup"><span data-stu-id="15635-107">A provider implements a control pattern by following these main steps:</span></span>

1.  <span data-ttu-id="15635-108">Implementare l'interfaccia del provider che supporta il pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="15635-108">Implement the provider interface that supports the control pattern.</span></span> <span data-ttu-id="15635-109">Ad esempio, per supportare il pattern di controllo [Selection](uiauto-implementingselection.md) , un provider per un controllo elenco personalizzato implementa l'interfaccia [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .</span><span class="sxs-lookup"><span data-stu-id="15635-109">For example, to support the [Selection](uiauto-implementingselection.md) control pattern, a provider for a custom list control would implement the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface.</span></span>
2.  <span data-ttu-id="15635-110">Restituisce un oggetto che contiene l'interfaccia del provider del pattern di controllo quando l'automazione interfaccia utente chiama il metodo [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) del provider.</span><span class="sxs-lookup"><span data-stu-id="15635-110">Return an object that contains the control pattern provider interface when UI Automation calls the provider's [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) method.</span></span>

<span data-ttu-id="15635-111">Nell'esempio seguente viene illustrata l'implementazione dell'interfaccia [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) per un controllo elenco personalizzato a selezione singola.</span><span class="sxs-lookup"><span data-stu-id="15635-111">The following example shows the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface implementation for a custom, single-selection list control.</span></span> <span data-ttu-id="15635-112">L'implementazione include metodi di recupero delle proprietà per le proprietà IsSelectionRequired e CanSelectMultiple e un metodo per recuperare il provider per l'elemento elenco selezionato.</span><span class="sxs-lookup"><span data-stu-id="15635-112">The implementation includes property-retrieval methods for the IsSelectionRequired and CanSelectMultiple properties, and a method for retrieving the provider for the selected list item.</span></span>


```C++
// Specifies whether the list control supports the selection of
// multiple items at the same time.
IFACEMETHODIMP ListProvider::get_CanSelectMultiple(BOOL *pRetVal)
{
    *pRetVal = FALSE;
    return S_OK;
} 

// Specifies whether the list must have an item selected at all times.
IFACEMETHODIMP ListProvider::get_IsSelectionRequired(BOOL *pRetVal)
{
   *pRetVal = TRUE;
   return S_OK;
}

// Retrieves the provider of the selected item in a custom list control. 
//
// m_pControl - pointer to an application-defined object for managing
//   the custom list control. 
//
// ListItemProvider - application-defined class that inherits the 
//   IRawElementProviderSimple interface.
//
// GetItemProviderByIndex - application-defined method that retrieves the 
//   IRawElementProviderSimple interface of the selected item.
IFACEMETHODIMP ListProvider::GetSelection(SAFEARRAY** pRetVal)
{
    // Create a safe array to store the IRawElementProviderSimple pointer.
    SAFEARRAY *psa = SafeArrayCreateVector(VT_UNKNOWN, 0, 1);

    // Retrieve the index of the selected list item. 
    int index = m_pControl->GetSelectedIndex(); 

    // Retrieve the IRawElementProviderSimple pointer of the selected list
    // item. ListItemProvider is an application-defined class that 
    // inherits the IRawElementProviderSimple interface. 
    ListItemProvider* pItem = GetItemProviderByIndex(index); 
    if (pItem != NULL)
    {
        LONG i = 0;
        SafeArrayPutElement(psa, &i, pItem);
    }
    *pRetVal = psa;
    return S_OK;
}
```



<span data-ttu-id="15635-113">Nell'esempio seguente viene illustrata un'implementazione di [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) che restituisce un oggetto che implementa [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="15635-113">The following example shows an implementation of [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) that returns an object that implements [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span> <span data-ttu-id="15635-114">La maggior parte dei controlli elenco supporta anche altri modelli, ma in questo esempio viene restituito un riferimento null per tutti gli altri identificatori del pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="15635-114">Most list controls would support other patterns as well, but this example returns a null reference for all other control pattern identifiers.</span></span>


```C++
// Retrieves an object that supports the control pattern provider interface 
// for the specified control pattern. 
IFACEMETHODIMP ListProvider::GetPatternProvider(PATTERNID patternId, IUnknown** pRetVal)
{
    *pRetVal = NULL;
    if (patternId == UIA_SelectionPatternId) 
    {
        // Return the object that implements ISelectionProvider. In this example, 
        // ISelectionProvider is implemented in the current object (this).
        *pRetVal = static_cast<IRawElementProviderSimple*>(this);
        AddRef();  
    }
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="15635-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="15635-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="15635-116">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="15635-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="15635-117">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="15635-117">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="15635-118">Procedure per i provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="15635-118">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




