---
title: Come implementare i gestori eventi
description: Questo argomento contiene codice di esempio che illustra come implementare interfacce che consentono ai client di ricevere e gestire gli eventi Automazione interfaccia utente Microsoft.
ms.assetid: 6b6549b8-795b-45a8-8fef-59842cc990e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09448bd9088b8338e9de14079b2ee446bf43f4e2c41e15ce17114eda958ed210
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098381"
---
# <a name="how-to-implement-event-handlers"></a>Come implementare i gestori eventi

Questo argomento contiene codice di esempio che illustra come implementare interfacce che consentono ai client di ricevere e gestire gli eventi Automazione interfaccia utente Microsoft. Vengono illustrati gli argomenti seguenti:

-   [Gestione degli eventi Automazione interfaccia utente generali](#handling-general-ui-automation-events)
-   [Gestione di Focus-Changed eventi](#handling-focus-changed-events)
-   [Gestione di Property-Changed eventi](#handling-property-changed-events)
-   [Gestione di Structure-Changed eventi](#handling-structure-changed-events)
-   [Argomenti correlati](#related-topics)

## <a name="handling-general-ui-automation-events"></a>Gestione degli eventi Automazione interfaccia utente generali

L'esempio di codice seguente è un'applicazione console di Microsoft Windows che implementa un gestore eventi Automazione interfaccia utente per gli eventi Automazione interfaccia utente generali. Questo esempio gestisce gli eventi di creazione e distruzione per le descrizioni comando e altre finestre.


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



## <a name="handling-focus-changed-events"></a>Gestione di Focus-Changed eventi

L'esempio di codice seguente è un'Windows console che implementa un gestore per gli eventi di modifica dello stato attivo.


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



## <a name="handling-property-changed-events"></a>Gestione di Property-Changed eventi

L'esempio di codice seguente è Windows'applicazione console che implementa un gestore per gli eventi di modifica delle proprietà.


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



## <a name="handling-structure-changed-events"></a>Gestione di Structure-Changed eventi

L'esempio di codice seguente è Windows'applicazione console che implementa un gestore per gli eventi di modifica della struttura.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Sottoscrizione a eventi Automazione interfaccia utente eventi](uiauto-eventsforclients.md)
</dt> <dt>

[Procedure per i Automazione interfaccia utente client](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




