---
description: È possibile utilizzare la procedura e l'esempio di codice in questo argomento per completare l'applicazione client WMI che esegue l'inizializzazione COM, si connette a WMI nel computer locale, riceve una notifica degli eventi e quindi esegue la pulizia.
ms.assetid: 4d581965-e22a-4205-908c-661eeeec88cf
ms.tgt_platform: multiple
title: 'Esempio: Ricezione di notifiche degli eventi tramite WMI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 759ed91ed1f7892b622089fa64fe8e8421a8b3bd73bf77ba2f60fa4199d25434
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119411881"
---
# <a name="example-receiving-event-notifications-through-wmi"></a>Esempio: Ricezione di notifiche degli eventi tramite WMI

È possibile utilizzare la procedura e l'esempio di codice in questo argomento per completare l'applicazione client WMI che esegue l'inizializzazione COM, si connette a WMI nel computer locale, riceve una notifica degli eventi e quindi esegue la pulizia. L'esempio invia una notifica all'utente di un evento quando viene creato un nuovo processo. Gli eventi vengono ricevuti in modo asincrono.

La procedura seguente viene utilizzata per eseguire l'applicazione WMI. I passaggi da 1 a 5 contengono tutti i passaggi necessari per configurare e connettersi a WMI e il passaggio 6 è il punto in cui vengono ricevute le notifiche degli eventi.

**Per ricevere una notifica degli eventi tramite WMI**

1.  Inizializzare i parametri COM con una chiamata a [**CoInitializeEx.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)

    Per altre informazioni, vedere [Inizializzazione di COM per un'applicazione WMI.](initializing-com-for-a-wmi-application.md)

2.  Inizializzare la sicurezza dei processi COM chiamando [**CoInitializeSecurity.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

    Per altre informazioni, vedere [Impostazione del livello di sicurezza del processo predefinito tramite C++.](setting-the-default-process-security-level-using-c-.md)

3.  Ottenere il localizzatore iniziale in WMI chiamando [**CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)

    Per altre informazioni, vedere [Creazione di una connessione a uno spazio dei nomi WMI.](creating-a-connection-to-a-wmi-namespace.md)

4.  Ottenere un puntatore [**a IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per lo spazio dei nomi radice cimv2 nel computer locale \\ chiamando [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Per connettersi a un computer remoto, vedere [Esempio: Recupero di dati WMI da un computer remoto.](example--getting-wmi-data-from-a-remote-computer.md)

    Per altre informazioni, vedere [Creazione di una connessione a uno spazio dei nomi WMI.](creating-a-connection-to-a-wmi-namespace.md)

5.  Impostare la sicurezza del proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) in modo che il servizio WMI possa rappresentare il client chiamando [**CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)

    Per altre informazioni, vedere [Impostazione dei livelli di sicurezza in una connessione WMI.](setting-the-security-levels-on-a-wmi-connection.md)

6.  Usare il [**puntatore IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per effettuare richieste a WMI. Questo esempio usa il [**metodo IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) per ricevere eventi asincroni. Quando si ricevono eventi asincroni, è necessario fornire un'implementazione di [**IWbemObjectSink.**](iwbemobjectsink.md) Questo esempio fornisce l'implementazione nella classe EventSink. Il codice di implementazione e il codice del file di intestazione per questa classe vengono forniti sotto l'esempio principale. Il **metodo IWbemServices::ExecNotificationQueryAsync** chiama il **metodo EventSink::Indicate** ogni volta che viene ricevuto un evento. Per questo esempio il **metodo EventSink::Indicate** viene chiamato ogni volta che viene creato un processo. Per testare questo esempio, eseguire il codice e avviare un processo, ad esempio Notepad.exe. In questo modo viene attivata una notifica degli eventi.

    Per altre informazioni sull'esecuzione di richieste di WMI, vedere [Modifica delle informazioni su](manipulating-class-and-instance-information.md) classi e istanze e Chiamata di un [metodo.](calling-a-method.md)

Il codice di esempio seguente riceve le notifiche degli eventi tramite WMI.


```C++
#include "eventsink.h"

int main(int iArgCnt, char ** argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
             << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM negotiates service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
             << hex << hres << endl;
        CoUninitialize();
        return 1;                      // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
             << "Err code = 0x"
             << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: ---------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(
        _bstr_t(L"ROOT\\CIMV2"), 
        NULL,
        NULL, 
        0, 
        NULL, 
        0, 
        0, 
        &pSvc
    );
     
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
        pSvc,                        // Indicates the proxy to set
        RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx 
        RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx 
        NULL,                        // Server principal name 
        RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
        NULL,                        // client identity
        EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: -------------------------------------------------
    // Receive event notifications -----------------------------

    // Use an unsecured apartment for security
    IUnsecuredApartment* pUnsecApp = NULL;

    hres = CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
        CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
        (void**)&pUnsecApp);
 
    EventSink* pSink = new EventSink;
    pSink->AddRef();

    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);

    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink,
        (void **) &pStubSink);

    // The ExecNotificationQueryAsync method will call
    // The EventQuery::Indicate method when an event occurs
    hres = pSvc->ExecNotificationQueryAsync(
        _bstr_t("WQL"), 
        _bstr_t("SELECT * " 
            "FROM __InstanceCreationEvent WITHIN 1 "
            "WHERE TargetInstance ISA 'Win32_Process'"), 
        WBEM_FLAG_SEND_STATUS, 
        NULL, 
        pStubSink);

    // Check for errors.
    if (FAILED(hres))
    {
        printf("ExecNotificationQueryAsync failed "
            "with = 0x%X\n", hres);
        pSvc->Release();
        pLoc->Release();
        pUnsecApp->Release();
        pStubUnk->Release();
        pSink->Release();
        pStubSink->Release();
        CoUninitialize();    
        return 1;
    }

    // Wait for the event
    Sleep(10000);
         
    hres = pSvc->CancelAsyncCall(pStubSink);

    // Cleanup
    // ========

    pSvc->Release();
    pLoc->Release();
    pUnsecApp->Release();
    pStubUnk->Release();
    pSink->Release();
    pStubSink->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



Il file di intestazione seguente viene usato per la classe EventSink. La classe EventSink viene usata nell'esempio di codice precedente.


```C++
// EventSink.h
#ifndef EVENTSINK_H
#define EVENTSINK_H

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

class EventSink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone;

public:
    EventSink() { m_lRef = 0; }
   ~EventSink() { bDone = true; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT 
        STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            LONG lObjectCount,
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};

#endif    // end of EventSink.h
```



Il codice di esempio seguente è un'implementazione della classe EventSink.


```C++
// EventSink.cpp
#include "eventsink.h"

ULONG EventSink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG EventSink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT EventSink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT EventSink::Indicate(long lObjectCount,
    IWbemClassObject **apObjArray)
{
 HRESULT hres = S_OK;

    for (int i = 0; i < lObjectCount; i++)
    {
        printf("Event occurred\n");
    }

    return WBEM_S_NO_ERROR;
}

HRESULT EventSink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    if(lFlags == WBEM_STATUS_COMPLETE)
    {
        printf("Call complete. hResult = 0x%X\n", hResult);
    }
    else if(lFlags == WBEM_STATUS_PROGRESS)
    {
        printf("Call in progress.\n");
    }

    return WBEM_S_NO_ERROR;
}    // end of EventSink.cpp
```



 

 
