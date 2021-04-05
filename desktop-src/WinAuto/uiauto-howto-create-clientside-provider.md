---
title: Come creare un provider di automazione interfaccia utente di Client-Side (proxy)
description: Questo argomento contiene codice di esempio che illustra come implementare un provider di automazione interfaccia utente Microsoft o un proxy sul lato client.
ms.assetid: 37e54a0f-3d41-4f47-ba73-7f1bf6c365e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a0b32ae60d6364ea6eac18fae991d1d600e61c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711326"
---
# <a name="how-to-create-a-client-side-proxy-ui-automation-provider"></a>Come creare un provider di automazione interfaccia utente di Client-Side (proxy)

Questo argomento contiene codice di esempio che illustra come implementare un provider di automazione interfaccia utente Microsoft o un proxy sul lato client.

-   [Esempio 1: enumerazione della tabella del proxy Factory](#example-1-enumerating-the-proxy-factory-table)
-   [Esempio 2: implementazione di un proxy semplice per i controlli Button](#example-2-implementing-a-simple-proxy-for-button-controls)
-   [Argomenti correlati](#related-topics)

## <a name="example-1-enumerating-the-proxy-factory-table"></a>Esempio 1: enumerazione della tabella del proxy Factory

Il codice di esempio seguente enumera le voci nella tabella Factory proxy e visualizza il nome della classe del controllo supportato. Per i proxy che non sono forniti con il sistema operativo, viene visualizzato il nome dell'immagine.


```C++
HRESULT GetProxyTable()
{
    IUIAutomationProxyFactoryMapping* pMap;
    IUIAutomationProxyFactoryEntry* pEntry;
    UINT count;
    BSTR className;
    BSTR imageName;

    HRESULT hr = g_pAutomation->get_ProxyFactoryMapping(&pMap);
    if (SUCCEEDED(hr))
    {
        if (SUCCEEDED(pMap->get_Count(&count)))
        {
            for (UINT x = 0; x < count; x++)
            {
                if (SUCCEEDED(pMap->GetEntry(x, &pEntry)))
                {
                    pEntry->get_ClassName(&className);
                    if (className)
                    {
                        std::wcout << className << L"\t";
                        SysFreeString(className);
                    }
                    if (SUCCEEDED(pEntry->get_ImageName(&imageName)))
                    {
                        if (imageName)
                        {
                            std::wcout << imageName;
                            SysFreeString(imageName);
                        }
                        std::wcout << L"\n";
                    }
                }
                pEntry->Release();
            }
        }
        pMap->Release();
    }

    return hr;
}
```



## <a name="example-2-implementing-a-simple-proxy-for-button-controls"></a>Esempio 2: implementazione di un proxy semplice per i controlli Button

Il codice di esempio seguente implementa un proxy semplice per i controlli che hanno il nome della classe "button" e aggiunge una voce per il proxy alla tabella del proxy Factory. In questo esempio viene utilizzata la finestra di dialogo tipo di carattere del blocco note per illustrare il proxy.


```C++
// Registers a proxy for controls with the class name "BUTTON" and
// demonstrates it on the Font dialog of Notepad (which should be
// open when running this code).
#include "stdafx.h"
#include <stdio.h>
#include <tchar.h>

#include <windows.h>
#include <UIAutomation.h>

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// A simple proxy for the proxy factory to create.
class ReallySimpleProxy : public IRawElementProviderSimple
{
public:
    ReallySimpleProxy(HWND hwnd):_refCount(1), _hWnd(hwnd) { }
    virtual ~ReallySimpleProxy() {}

    // IUnknown methods.
    IFACEMETHODIMP_(ULONG) AddRef() 
    { 
        return InterlockedIncrement(&_refCount);
    }
    IFACEMETHODIMP_(ULONG) Release()
    {
        long val = InterlockedDecrement(&_refCount);
        if(val == 0)
        {
            delete this;
        }
        return val;
    }

    IFACEMETHODIMP QueryInterface(REFIID riid, void** ppInterface)
    {
        if(riid == __uuidof(IUnknown))
            *ppInterface =(IUnknown*)((IRawElementProviderSimple*)this);
        else if(riid == __uuidof(IRawElementProviderSimple))
            *ppInterface =(IRawElementProviderSimple*)this;
        else
        {
            *ppInterface = NULL;
            return E_NOINTERFACE;
        }

        ((IUnknown*)(*ppInterface))->AddRef();
        return S_OK;
    }

    // IRawElementProviderSimple methods.
    IFACEMETHODIMP get_ProviderOptions(ProviderOptions * pRetVal)
    {
        *pRetVal = ProviderOptions_ClientSideProvider;
        return S_OK;
    }

    IFACEMETHODIMP GetPatternProvider(PATTERNID patternId, IUnknown ** pRetVal)
    {
        *pRetVal = NULL;
        return S_OK;
    }

    IFACEMETHODIMP GetPropertyValue(PROPERTYID propertyId, VARIANT * pRetVal)
    {
        pRetVal->vt = VT_EMPTY;

        // A String value to test
        if(propertyId == UIA_NamePropertyId)
        {
            pRetVal->vt = VT_BSTR;
            pRetVal->bstrVal = SysAllocString( L"ReallySimpleProxy Control" );
        }

        // Provider Id
        if(propertyId == UIA_ProviderDescriptionPropertyId)
        {
            pRetVal->vt = VT_BSTR;
            pRetVal->bstrVal = SysAllocString( L"Sample: ReallySimpleProxy" );
        }

        return S_OK;
    }

    IFACEMETHODIMP get_HostRawElementProvider(
        IRawElementProviderSimple ** pRetVal)
    {
        return UiaHostProviderFromHwnd(_hWnd, pRetVal); 
    }

private:
    ULONG _refCount;

    HWND _hWnd; // Window handle for this object.
};

// A simple proxy factory that creates a simple proxy.
class SimpleProxyFactory : public IUIAutomationProxyFactory
{
public:
    SimpleProxyFactory():_refCount(1) {}
    virtual ~SimpleProxyFactory() {}

    // IUnknown methods.
    IFACEMETHODIMP_(ULONG) AddRef() 
    { 
        return InterlockedIncrement(&_refCount);
    }
    IFACEMETHODIMP_(ULONG) Release()
    {
        long val = InterlockedDecrement(&_refCount);
        if(val == 0)
        {
            delete this;
        }
        return val;
    }

    IFACEMETHODIMP QueryInterface(REFIID riid, void** ppInterface)
    {
        if(riid == __uuidof(IUnknown))
            *ppInterface =(IUnknown*)((IUIAutomationProxyFactory*)this);
        else if(riid == __uuidof(IUIAutomationProxyFactory))
            *ppInterface =(IUIAutomationProxyFactory*)this;
        else
        {
            *ppInterface = NULL;
            return E_NOINTERFACE;
        }

        ((IUnknown*)(*ppInterface))->AddRef();
        return S_OK;
    }

    // IUIAutomationProxyFactory methods.
    IFACEMETHODIMP CreateProvider (UIA_HWND hwnd, LONG idObject, LONG idChild,
        IRawElementProviderSimple **ppRetVal )
    {
        *ppRetVal = new ReallySimpleProxy((HWND)hwnd);
        return S_OK;
    }

    IFACEMETHODIMP get_ProxyFactoryId ( BSTR *pRetVal )
    {
        *pRetVal = SysAllocString(L"Simple Proxy Factory");
        return S_OK;
    }

private:
    ULONG _refCount;
};


HRESULT CheckElement(IUIAutomation *uia, HWND hwnd)
{
    IUIAutomationElement * buttonEl = NULL;
    BSTR name = NULL;
    BSTR providerDescription = NULL;

    wprintf( L"Getting AutomationElement for the button...\n" );
    HRESULT hr = uia->ElementFromHandle(hwnd, &buttonEl);
    if (FAILED(hr))
        goto cleanup;
    if (buttonEl == NULL)
    {
        hr = E_FAIL;
        goto cleanup;
    }

    hr = buttonEl->get_CurrentName(&name);
    if (FAILED(hr))
        goto cleanup;

    hr = buttonEl->get_CurrentProviderDescription(&providerDescription);
    if (FAILED(hr))
        goto cleanup;

    wprintf( L"Got Element:\n  %s\n  %s\n\n", name, providerDescription);
cleanup:
    SysFreeString(providerDescription);
    SysFreeString(name);
    SafeRelease(&buttonEl);

    return hr;
}


int _tmain(int argc, _TCHAR* argv[])
{
    IUIAutomation * uia = NULL;
    IUIAutomationProxyFactoryMapping * proxyMapping = NULL;
    IUIAutomationProxyFactoryEntry * simpleEntry = NULL;
    IUIAutomationProxyFactory *simpleFactory = NULL;
    BSTR bstrClassName = NULL;

    wprintf( L"Initializing COM...\n" );
    HRESULT hr = CoInitializeEx( NULL, COINIT_APARTMENTTHREADED );
    if (FAILED(hr))
        goto cleanup;

    wprintf( L"CoCreating Automation Object...\n" );
    hr = CoCreateInstance(__uuidof(CUIAutomation), NULL, CLSCTX_INPROC_SERVER,
        __uuidof(IUIAutomation), (void **)&uia);
    if (FAILED(hr))
        goto cleanup;


    wprintf( L"Finding Notepad Font Window...\n" );
    HWND fontHwnd = FindWindow(NULL,L"Font");
    if (fontHwnd == NULL)
        goto cleanup;

    wprintf( L"Finding the OK button in Font Window...\n" );
    HWND buttonHwnd = FindWindowEx(fontHwnd, NULL, L"BUTTON", L"OK");
    if (buttonHwnd == NULL)
        goto cleanup;

    wprintf( L"Checking Name and Provider Description without our Proxy:\n" );
    CheckElement(uia, buttonHwnd);

    wprintf( L"Getting the Proxy Factory Mapping Object...\n" );
    hr = uia->get_ProxyFactoryMapping(&proxyMapping);
    if (FAILED(hr))
        goto cleanup;
    if (proxyMapping == NULL)
        goto cleanup;

    wprintf( L"Creating the Proxy Factory...\n" );
    simpleFactory = new SimpleProxyFactory();
    if (simpleFactory == NULL)
        goto cleanup;

    wprintf( L"Creating the Proxy Factory Entry...\n" );
    hr = uia->CreateProxyFactoryEntry(simpleFactory, &simpleEntry);
    if (FAILED(hr))
        goto cleanup;
   bstrClassName = SysAllocString(L"BUTTON");
    if (bstrClassName == NULL)
        goto cleanup;

    // Match HWNDs with Button class name.
    hr = simpleEntry->put_ClassName(bstrClassName);   
    if (FAILED(hr))
        goto cleanup;

    // Match any process ImageName.
    hr = simpleEntry->put_ImageName(NULL);            
    if (FAILED(hr))
        goto cleanup;

    // Do not allow substring matching.
    hr = simpleEntry->put_AllowSubstringMatch(FALSE); 
    if (FAILED(hr))
        goto cleanup;

    // Enter it into the mapping.
    hr = proxyMapping->InsertEntry(0, simpleEntry);
    if (FAILED(hr))
        goto cleanup;

    wprintf( L"Checking Name and Provider Description with our Proxy:\n" );
    CheckElement(uia, buttonHwnd);

cleanup:

    SafeRelease(&simpleEntry);
    SafeRelease(&simpleFactory);
    SafeRelease(&proxyMapping);
    SafeRelease(&uia);
    SysFreeString(bstrClassName);
    CoUninitialize();

    return 0;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di un provider di automazione interfaccia utente Client-Side](uiauto-serversideprovider.md)
</dt> <dt>

[Procedure per i provider di automazione interfaccia utente](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




