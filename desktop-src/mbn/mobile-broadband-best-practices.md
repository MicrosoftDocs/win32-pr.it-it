---
description: Quando si usa l'API Mobile Broadband, è consigliabile usare il set di procedure consigliate seguente per ottenere le migliori prestazioni possibili.
ms.assetid: 523e3ea4-1d4e-45d1-bc24-93aa2fb14390
title: Procedure consigliate per l'API Mobile Broadband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3a6c1e236a61dd2a5321be2edb7a68156f904605bd8a1da5fc169ea8b70e464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881655"
---
# <a name="mobile-broadband-api-best-practices"></a>Procedure consigliate per l'API Mobile Broadband

Quando si usa l'API Mobile Broadband, è consigliabile usare il set di procedure consigliate seguente per ottenere le migliori prestazioni possibili.

## <a name="do-not-cache-functional-objects"></a>Non memorizzare nella cache gli oggetti funzionali

Gli oggetti funzionali, ad [**esempio IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) e altri, vengono ottenuti da oggetti di gestione, ad esempio [**IMbnInterfaceManager,**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager)usando il metodo di enumerazione sull'oggetto manager corrispondente. Non memorizzare nella cache questi oggetti funzionali, poiché gli oggetti funzionali memorizzati nella cache contengono dati non obsoleti. Le operazioni sincrone eseguite su questi oggetti funzionali restituiranno gli stessi dati fino a quando gli oggetti funzionali non vengono ottenuti nuovamente.

Memorizzare invece nella cache gli oggetti di gestione e ottenere gli oggetti funzionali dall'oggetto manager usando di nuovo il metodo di enumerazione sull'oggetto manager corrispondente per ottenere i dati più recenti.

Nell'esempio di codice seguente viene illustrato il modo corretto per memorizzare nella cache gli oggetti di gestione.


```C++
#include <atlbase.h>
#include "mbnapi.h"
#include <tchar.h>

int main()
{
    HRESULT hr = E_FAIL;
    int returnVal = 0;

    do
    {
        hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);    
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;

        //Do the below once(cache the manager objects)
        hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        SAFEARRAY *psa = NULL;

        //Do the below each time(do not cache functional objects)
        hr = g_InterfaceMgr->GetInterfaces(&psa);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        LONG lLower;
        LONG lUpper;

        hr = SafeArrayGetLBound(psa, 1, &lLower);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        hr = SafeArrayGetUBound(psa, 1, &lUpper);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterface>  pInf = NULL;
        MBN_READY_STATE readyState;

        for (LONG l = lLower; l <= lUpper; l++)
        {
            hr = SafeArrayGetElement(psa, &l, (void*)(&pInf));
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            hr = pInf->GetReadyState(&readyState);
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            _tprintf(_T("Ready State = %d"), readyState); 
        }

        if (FAILED(hr))
        {
            break;
        }
    } while (FALSE);


    CoUninitialize();
    return returnVal;
}
```



## <a name="handle-all-notifications"></a>Gestire tutte le notifiche

Seguire e gestire tutte le notifiche, anche se non vengono attivate dall'applicazione. Questa operazione è necessaria per mantenere l'interfaccia utente sincronizzata con lo stato effettivo del dispositivo.

In un computer possono essere in esecuzione più di una gestione connessione. L'interfaccia utente nativa Visualizza interfaccia di rete disponibile fornita Windows 7 è una gestione connessione. Tutte le altre gestioni connessioni devono rispondere a tutte le notifiche per rimanere sincronizzate con Windows'interfaccia utente nativa. Un utente può scegliere di eseguire un'operazione in una delle gestioni connessioni che può comportare una modifica dello stato del dispositivo Mobile Broadband. Tuttavia, altre gestioni connessioni devono rimanere aggiornate per indicare correttamente lo stato modificato del dispositivo.

Ad esempio, l'esecuzione di una connessione tramite una delle gestioni connessioni modificherà lo stato del dispositivo da disponibile a connesso. Questa modifica dovrebbe essere visibile alle gestioni connessioni che non hanno avviato questa azione. Tutte le gestioni connessioni con interfaccia utente che indica lo stato di connessione del dispositivo devono restare in ascolto e gestire le notifiche dello stato di connessione per aggiornare correttamente l'interfaccia utente.

## <a name="sending-and-receiving-bytes"></a>Invio e ricezione di byte

Usare le funzioni helper IP [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) e [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) per inviare e ricevere byte.

## <a name="using-the-pin-unblock-api"></a>Uso dell'API di sblocco pin

Un'applicazione client chiamante deve essere elevata per poter richiamare [**correttamente IMbnPin::Unblock.**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock) Questo metodo è l'unica parte dell'API Mobile Broadband che richiede privilegi di amministratore o NCO. Per [altre informazioni, vedere A Description of the Network Configuration Operators Group]( https://support.microsoft.com/kb/297938/en-us) ( Descrizione del gruppo Network Configuration Operators).

## <a name="working-with-safearrays"></a>Uso di SafeArray

-   Usare ZeroMemory() prima di accedere a qualsiasi elemento in safearray.

-   Non controllare gli indici di un safearray. Possono essere negativi.

Nell'esempio di codice seguente viene illustrato come gestire correttamente safeArray.


```C++
#include <atlbase.h>
#include "mbnapi.h"

void CreateVisibleProviderList(LPCWSTR interfaceID)
{
    CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;
    SAFEARRAY *visibleProviders = NULL;
    long visibleLower = 0;
    long visibleUpper = 0;
    MBN_PROVIDER *pProvider = NULL;
    CComPtr<IMbnInterface> pInterface = NULL;

    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
    
    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = g_InterfaceMgr->GetInterface(interfaceID, & pInterface);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    ULONG age;

    hr = pInterface->GetVisibleProviders(&age, &visibleProviders);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetLBound(visibleProviders, 1, &visibleLower);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetUBound(visibleProviders, 1, &visibleUpper);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    //don't check on the indexes of safearray to be positive
    if (visibleLower > visibleUpper) 
    {
        // There are no visible providers in this case.
        hr = HRESULT_FROM_WIN32(ERROR_NOT_FOUND);
        goto ERROR_0;
    }

    DWORD size = (visibleUpper - visibleLower + 1) * sizeof(BOOL);
    DBG_UNREFERENCED_LOCAL_VARIABLE(size); 
    
    pProvider = (MBN_PROVIDER *)CoTaskMemAlloc(sizeof(MBN_PROVIDER));
    if (!pProvider) 
    {
        hr = E_OUTOFMEMORY;
        goto ERROR_0;
    }

    for (LONG vIndex = visibleLower; vIndex <= visibleUpper; vIndex++) 
    {
        //use zeromemory before accessing any elements in a safearray
        ZeroMemory(pProvider, sizeof(MBN_PROVIDER));
        hr = SafeArrayGetElement(visibleProviders, &vIndex, (void *)pProvider);
        if (FAILED(hr)) 
        {
            continue;
        }
    }

ERROR_0:
    if (visibleProviders) 
    {
        SafeArrayDestroy(visibleProviders);
        visibleProviders = NULL;
    }

    CoUninitialize();
}
```



 

 
