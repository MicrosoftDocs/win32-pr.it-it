---
title: Come implementare i gestori eventi
description: Questo argomento contiene codice di esempio che illustra come implementare le interfacce che consentono ai client di ricevere e gestire gli eventi di automazione interfaccia utente Microsoft.
ms.assetid: 6b6549b8-795b-45a8-8fef-59842cc990e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159e95e739ae73f1c37d99ae065032fd680f0720
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331876"
---
# <a name="how-to-implement-event-handlers"></a><span data-ttu-id="dbf5a-103">Come implementare i gestori eventi</span><span class="sxs-lookup"><span data-stu-id="dbf5a-103">How to Implement Event Handlers</span></span>

<span data-ttu-id="dbf5a-104">Questo argomento contiene codice di esempio che illustra come implementare le interfacce che consentono ai client di ricevere e gestire gli eventi di automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-104">This topic contains example code that shows how to implement interfaces that enable clients to receive and handle Microsoft UI Automation events.</span></span> <span data-ttu-id="dbf5a-105">Vengono illustrati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbf5a-105">It discusses the following topics:</span></span>

-   [<span data-ttu-id="dbf5a-106">Gestione degli eventi di automazione interfaccia utente generali</span><span class="sxs-lookup"><span data-stu-id="dbf5a-106">Handling General UI Automation Events</span></span>](#handling-general-ui-automation-events)
-   [<span data-ttu-id="dbf5a-107">Gestione degli eventi di Focus-Changed</span><span class="sxs-lookup"><span data-stu-id="dbf5a-107">Handling Focus-Changed Events</span></span>](#handling-focus-changed-events)
-   [<span data-ttu-id="dbf5a-108">Gestione degli eventi di Property-Changed</span><span class="sxs-lookup"><span data-stu-id="dbf5a-108">Handling Property-Changed Events</span></span>](#handling-property-changed-events)
-   [<span data-ttu-id="dbf5a-109">Gestione degli eventi di Structure-Changed</span><span class="sxs-lookup"><span data-stu-id="dbf5a-109">Handling Structure-Changed Events</span></span>](#handling-structure-changed-events)
-   [<span data-ttu-id="dbf5a-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dbf5a-110">Related topics</span></span>](#related-topics)

## <a name="handling-general-ui-automation-events"></a><span data-ttu-id="dbf5a-111">Gestione degli eventi di automazione interfaccia utente generali</span><span class="sxs-lookup"><span data-stu-id="dbf5a-111">Handling General UI Automation Events</span></span>

<span data-ttu-id="dbf5a-112">L'esempio di codice seguente è un'applicazione console di Microsoft Windows che implementa un gestore eventi di automazione interfaccia utente per eventi di automazione interfaccia utente generali.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-112">The following code example is a Microsoft Windows console application that implements a UI Automation event handler for general UI Automation events.</span></span> <span data-ttu-id="dbf5a-113">Questo esempio gestisce gli eventi di creazione e distruzione per le descrizioni comandi e altre finestre.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-113">This example handles creation and destruction events for tooltips and other windows.</span></span>


```C++
// Defines an event handler for general UI Automation events. It listens for
// tooltip and window creation and destruction events. 
#include <windows.h>
#include <stdio.h>
#include <UIAutomation.h>

class EventHandler:
    public IUIAutomationEventHandler
{
private:
    LONG _refCount;

public:
    int _eventCount;

    // Constructor.
    EventHandler(): _refCount(1), _eventCount(0) 
    {
    }

    // IUnknown methods.
    ULONG STDMETHODCALLTYPE AddRef() 
    {
        ULONG ret = InterlockedIncrement(&_refCount);
        return ret;
    }

    ULONG STDMETHODCALLTYPE Release() 
    {
        ULONG ret = InterlockedDecrement(&_refCount);
        if (ret == 0) 
        {
            delete this;
            return 0;
        }
        return ret;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppInterface) 
    {
        if (riid == __uuidof(IUnknown)) 
            *ppInterface=static_cast<IUIAutomationEventHandler*>(this);
        else if (riid == __uuidof(IUIAutomationEventHandler)) 
            *ppInterface=static_cast<IUIAutomationEventHandler*>(this);
        else 
        {
            *ppInterface = NULL;
            return E_NOINTERFACE;
        }
        this->AddRef();
        return S_OK;
    }

    // IUIAutomationEventHandler methods
    HRESULT STDMETHODCALLTYPE HandleAutomationEvent(IUIAutomationElement * pSender, EVENTID eventID)
    {
        _eventCount++;
        switch (eventID) 
        {
            case UIA_ToolTipOpenedEventId:
                wprintf(L">> Event ToolTipOpened Received! (count: %d)\n", _eventCount);
                break;
            case UIA_ToolTipClosedEventId:
                wprintf(L">> Event ToolTipClosed Received! (count: %d)\n", _eventCount);
                break;
            case UIA_Window_WindowOpenedEventId:
                wprintf(L">> Event WindowOpened Received! (count: %d)\n", _eventCount);
                break;
            case UIA_Window_WindowClosedEventId:
                wprintf(L">> Event WindowClosed Received! (count: %d)\n", _eventCount);
                break;
            default:
                wprintf(L">> Event (%d) Received! (count: %d)\n", eventID, _eventCount);
                break;
        }
        return S_OK;
    }
};

int main(int argc, char* argv[])
{
    HRESULT hr;
    int ret = 0;
    IUIAutomationElement* pTargetElement = NULL;
    EventHandler* pEHTemp = NULL;

    CoInitializeEx(NULL,COINIT_MULTITHREADED);
    IUIAutomation* pAutomation = NULL;
    hr = CoCreateInstance(__uuidof(CUIAutomation), NULL,CLSCTX_INPROC_SERVER, __uuidof(IUIAutomation), (void**)&pAutomation);
    if(FAILED(hr) || pAutomation==NULL) 
    {
        ret = 1;
        goto cleanup;
    }
    // Use root element for listening to window and tooltip creation and destruction.
    hr = pAutomation->GetRootElement(&pTargetElement);
    if (FAILED(hr) || pTargetElement==NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    pEHTemp = new EventHandler();
    if (pEHTemp == NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Adding Event Handlers.\n");
    hr = pAutomation->AddAutomationEventHandler(UIA_ToolTipOpenedEventId, pTargetElement, TreeScope_Subtree, NULL, (IUIAutomationEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }
    hr = pAutomation->AddAutomationEventHandler(UIA_ToolTipClosedEventId, pTargetElement, TreeScope_Subtree, NULL, (IUIAutomationEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }
    hr = pAutomation->AddAutomationEventHandler(UIA_Window_WindowOpenedEventId, pTargetElement, TreeScope_Subtree, NULL, (IUIAutomationEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }
    hr = pAutomation->AddAutomationEventHandler(UIA_Window_WindowClosedEventId, pTargetElement, TreeScope_Subtree, NULL, (IUIAutomationEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Press any key to remove event handlers and exit\n");
    getchar();

    wprintf(L"-Removing Event Handlers.\n");

cleanup:
    // Remove event handlers, release resources, and terminate
    if (pAutomation != NULL) 
    {
        hr = pAutomation->RemoveAllEventHandlers();
        if (FAILED(hr))
            ret = 1;
        pAutomation->Release();
    }

    if (pEHTemp != NULL) 
        pEHTemp->Release();

    if (pTargetElement != NULL) 
        pTargetElement->Release();

    CoUninitialize();
    return ret;
}
```



## <a name="handling-focus-changed-events"></a><span data-ttu-id="dbf5a-114">Gestione degli eventi di Focus-Changed</span><span class="sxs-lookup"><span data-stu-id="dbf5a-114">Handling Focus-Changed Events</span></span>

<span data-ttu-id="dbf5a-115">L'esempio di codice seguente è un'applicazione console di Windows che implementa un gestore per gli eventi di modifica dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-115">The following code example is a Windows console application that implements a handler for focus-changed events.</span></span>


```C++
// Defines an event handler for focus changed events and starts
// listening to them.
#include <windows.h>
#include <stdio.h>
#include <UIAutomation.h>

class EventHandler:
    public IUIAutomationFocusChangedEventHandler
{
private:
    LONG _refCount;

public:
    int _eventCount;

    //Constructor.
    EventHandler(): _refCount(1), _eventCount(0) 
    {
    }

    //IUnknown methods.
    ULONG STDMETHODCALLTYPE AddRef() 
    {
        ULONG ret = InterlockedIncrement(&_refCount);
        return ret;
    }

    ULONG STDMETHODCALLTYPE Release() 
    {
        ULONG ret = InterlockedDecrement(&_refCount);
        if (ret == 0) 
        {
            delete this;
            return 0;
        }
        return ret;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppInterface) 
    {
        if (riid == __uuidof(IUnknown))
            *ppInterface = static_cast<IUIAutomationFocusChangedEventHandler*>(this);
        else if(riid == __uuidof(IUIAutomationFocusChangedEventHandler)) 
            *ppInterface=static_cast<IUIAutomationFocusChangedEventHandler*>(this);
        else 
        {
            *ppInterface = NULL;
            return E_NOINTERFACE;
        }
        this->AddRef();
        return S_OK;
    }

    // IUIAutomationFocusChangedEventHandler methods.
    HRESULT STDMETHODCALLTYPE HandleFocusChangedEvent(IUIAutomationElement * pSender) 
    {
        _eventCount++;
        wprintf(L">> FocusChangedEvent Received! (count: %d)\n", _eventCount);
        return S_OK;
    }
};

int main(int argc, char* argv[]) 
{
    HRESULT hr;
    int ret = 0;
    EventHandler* pEHTemp = NULL;

    CoInitializeEx(NULL,COINIT_MULTITHREADED);
    IUIAutomation* pAutomation = NULL;
    hr = CoCreateInstance(__uuidof(CUIAutomation), NULL,CLSCTX_INPROC_SERVER, __uuidof(IUIAutomation), (void**)&pAutomation);
    if (FAILED(hr) || pAutomation == NULL)
    {
        ret = 1;
        goto cleanup;
    }

    pEHTemp = new EventHandler();
    if (pEHTemp == NULL)
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Adding Event Handlers.\n");
    hr = pAutomation->AddFocusChangedEventHandler(NULL, (IUIAutomationFocusChangedEventHandler*) pEHTemp); 
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Press any key to remove event handler and exit\n");
    getchar();

    wprintf(L"-Removing Event Handlers.\n");
    hr = pAutomation->RemoveFocusChangedEventHandler((IUIAutomationFocusChangedEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    // Release resources and terminate.
cleanup:
    if (pEHTemp != NULL) 
        pEHTemp->Release();

    if (pAutomation != NULL) 
        pAutomation->Release();

    CoUninitialize();
    return ret;
}
```



## <a name="handling-property-changed-events"></a><span data-ttu-id="dbf5a-116">Gestione degli eventi di Property-Changed</span><span class="sxs-lookup"><span data-stu-id="dbf5a-116">Handling Property-Changed Events</span></span>

<span data-ttu-id="dbf5a-117">L'esempio di codice seguente è un'applicazione console di Windows che implementa un gestore per gli eventi di modifica delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-117">The following code example is a Windows console application that implements a handler for property-changed events.</span></span>


```C++
// Defines an event handler for property-changed events, and listens for
// ToggleState property changes on the element specifies by the user.
#include <windows.h>
#include <stdio.h>
#include <UIAutomation.h>

class EventHandler:
    public IUIAutomationPropertyChangedEventHandler
{
private:
    LONG _refCount;

public:
    int _eventCount;

    //Constructor.
    EventHandler(): _refCount(1), _eventCount(0) 
    {
    }

    //IUnknown methods.
    ULONG STDMETHODCALLTYPE AddRef() 
    {
        ULONG ret = InterlockedIncrement(&_refCount);
        return ret;
    }

    ULONG STDMETHODCALLTYPE Release() 
    {
        ULONG ret = InterlockedDecrement(&_refCount);
        if (ret == 0) 
        {
            delete this;
            return 0;
        }
        return ret;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppInterface) 
    {
        if (riid == __uuidof(IUnknown))
            *ppInterface=static_cast<IUIAutomationPropertyChangedEventHandler*>(this);
        else if (riid == __uuidof(IUIAutomationPropertyChangedEventHandler)) 
            *ppInterface=static_cast<IUIAutomationPropertyChangedEventHandler*>(this);
        else 
        {
            *ppInterface = NULL;
            return E_NOINTERFACE;
        }
        this->AddRef();
        return S_OK;
    }

    // IUIAutomationPropertyChangedEventHandler methods.
    HRESULT STDMETHODCALLTYPE HandlePropertyChangedEvent(IUIAutomationElement* pSender, PROPERTYID propertyID, VARIANT newValue) 
    {
        _eventCount++;
        if (propertyID == UIA_ToggleToggleStatePropertyId) 
            wprintf(L">> Property ToggleState changed! ");
        else 
            wprintf(L">> Property (%d) changed! ", propertyID);

        if (newValue.vt == VT_I4) 
            wprintf(L"(0x%0.8x) ", newValue.lVal);

        wprintf(L"(count: %d)\n", _eventCount);
        return S_OK;
    }
};

int main(int argc, char* argv[]) 
{
    HRESULT hr;
    int ret = 0;
    IUIAutomationElement* pTargetElement = NULL;
    EventHandler* pEHTemp = NULL;

    CoInitializeEx(NULL,COINIT_MULTITHREADED);

    IUIAutomation* pAutomation = NULL;
    hr = CoCreateInstance(__uuidof(CUIAutomation), NULL, CLSCTX_INPROC_SERVER, __uuidof(IUIAutomation), (void**)&pAutomation);
    if (FAILED(hr) || pAutomation==NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Use the mouse to point to the element you want to listen from.\n");
    Sleep(3000);

    // Make this application dots-per-inch (DPI) aware.
    SetProcessDPIAware();

    // Get mouse cursor position and get element from point.
    POINT pt;
    GetPhysicalCursorPos(&pt);
    hr = pAutomation->ElementFromPoint(pt, &pTargetElement);
    if (FAILED(hr) || pTargetElement==NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    pEHTemp = new EventHandler();
    if (pEHTemp == NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    PROPERTYID pPIDProperties[] = { UIA_ToggleToggleStatePropertyId };

    wprintf(L"-Adding Event Handler.\n");
    hr = pAutomation->AddPropertyChangedEventHandlerNativeArray(pTargetElement, TreeScope_Subtree, NULL, (IUIAutomationPropertyChangedEventHandler*) pEHTemp, pPIDProperties, sizeof(pPIDProperties) / sizeof(pPIDProperties[0]));
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Press any key to remove event handler and exit\n");
    getchar();

    wprintf(L"-Removing Event Handler.\n");
    hr = pAutomation->RemovePropertyChangedEventHandler(pTargetElement, (IUIAutomationPropertyChangedEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    // Release resources and terminate.
cleanup:
    if (pEHTemp != NULL) 
        pEHTemp->Release();

    if (pTargetElement != NULL) 
        pTargetElement->Release();

    if (pAutomation != NULL) 
        pAutomation->Release();

    CoUninitialize();
    return ret;
}
```



## <a name="handling-structure-changed-events"></a><span data-ttu-id="dbf5a-118">Gestione degli eventi di Structure-Changed</span><span class="sxs-lookup"><span data-stu-id="dbf5a-118">Handling Structure-Changed Events</span></span>

<span data-ttu-id="dbf5a-119">L'esempio di codice seguente è un'applicazione console di Windows che implementa un gestore per gli eventi di modifica della struttura.</span><span class="sxs-lookup"><span data-stu-id="dbf5a-119">The following code example is a Windows console application that implements a handler for structure-changed events.</span></span>


```C++
// Defines an event handler for structure-changed events, and 
// listens for them on the element specifies by the user.
#include <windows.h>
#include <stdio.h>
#include <UIAutomation.h>

class EventHandler:
    public IUIAutomationStructureChangedEventHandler
{
private:
    LONG _refCount;

public:
    int _eventCount;

    // Constructor.
    EventHandler(): _refCount(1), _eventCount(0) 
    {
    }

    // IUnknown methods.
    ULONG STDMETHODCALLTYPE AddRef() 
    {
        ULONG ret = InterlockedIncrement(&_refCount);
        return ret;
    }

    ULONG STDMETHODCALLTYPE Release() 
    {
        ULONG ret = InterlockedDecrement(&_refCount);
        if (ret == 0) 
        {
            delete this;
            return 0;
        }
        return ret;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppInterface) 
    {
        if (riid == __uuidof(IUnknown))
            *ppInterface=static_cast<IUIAutomationStructureChangedEventHandler*>(this);
        else if (riid == __uuidof(IUIAutomationStructureChangedEventHandler)) 
            *ppInterface=static_cast<IUIAutomationStructureChangedEventHandler*>(this);
        else 
        {
            *ppInterface = NULL;
            return E_NOINTERFACE;
        }
        this->AddRef();
        return S_OK;
    }

    // IUIAutomationStructureChangedEventHandler methods
    HRESULT STDMETHODCALLTYPE HandleStructureChangedEvent(IUIAutomationElement* pSender, StructureChangeType changeType, SAFEARRAY* pRuntimeID) {
        _eventCount++;
        switch (changeType) 
        {
            case StructureChangeType_ChildAdded:
                wprintf(L">> Structure Changed: ChildAdded! (count: %d)\n", _eventCount);
                break;
            case StructureChangeType_ChildRemoved:
                wprintf(L">> Structure Changed: ChildRemoved! (count: %d)\n", _eventCount);
                break;
            case StructureChangeType_ChildrenInvalidated:
                wprintf(L">> Structure Changed: ChildrenInvalidated! (count: %d)\n", _eventCount);
                break;
            case StructureChangeType_ChildrenBulkAdded:
                wprintf(L">> Structure Changed: ChildrenBulkAdded! (count: %d)\n", _eventCount);
                break;
            case StructureChangeType_ChildrenBulkRemoved:
                wprintf(L">> Structure Changed: ChildrenBulkRemoved! (count: %d)\n", _eventCount);
                break;
            case StructureChangeType_ChildrenReordered:
                wprintf(L">> Structure Changed: ChildrenReordered! (count: %d)\n", _eventCount);
                break;
        }
        return S_OK;
    }
};

int main(int argc, char* argv[]) 
{
    HRESULT hr;
    int ret = 0;
    IUIAutomationElement* pTargetElement = NULL;
    EventHandler* pEHTemp = NULL;

    CoInitializeEx(NULL,COINIT_MULTITHREADED);

    IUIAutomation* pAutomation=NULL;
    hr = CoCreateInstance(__uuidof(CUIAutomation), NULL, CLSCTX_INPROC_SERVER, __uuidof(IUIAutomation), (void**)&pAutomation);
    if (FAILED(hr) || pAutomation == NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Use the mouse to point to the element you want to listen from.\n");
    Sleep(3000);

    // Make this application dots-per-inch (DPI) aware.
    SetProcessDPIAware();

    // Get mouse cursor position and get element from point.
    POINT pt;
    GetPhysicalCursorPos(&pt);
    hr = pAutomation->ElementFromPoint(pt, &pTargetElement);
    if (FAILED(hr) || pTargetElement == NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    pEHTemp = new EventHandler();
    if (pEHTemp == NULL) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Adding Event Handler.\n");
    hr = pAutomation->AddStructureChangedEventHandler(pTargetElement, TreeScope_Subtree, NULL, (IUIAutomationStructureChangedEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    wprintf(L"-Press any key to remove event handler and exit\n");
    getchar();

    wprintf(L"-Removing Event Handler.\n");
    hr = pAutomation->RemoveStructureChangedEventHandler(pTargetElement, (IUIAutomationStructureChangedEventHandler*) pEHTemp);
    if (FAILED(hr)) 
    {
        ret = 1;
        goto cleanup;
    }

    // Release resources and terminate.
cleanup:
    if (pEHTemp != NULL) 
        pEHTemp->Release();

    if (pTargetElement != NULL) 
        pTargetElement->Release();

    if (pAutomation != NULL) 
        pAutomation->Release();

    CoUninitialize();
    return ret;
}
```



## <a name="related-topics"></a><span data-ttu-id="dbf5a-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dbf5a-120">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dbf5a-121">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="dbf5a-121">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dbf5a-122">Sottoscrizione degli eventi di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="dbf5a-122">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
</dt> <dt>

[<span data-ttu-id="dbf5a-123">Procedure per i client di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="dbf5a-123">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




