---
description: Quando si lavora con l'API Mobile Broadband, è necessario usare il set di procedure consigliate seguente per ottenere le migliori prestazioni possibili.
ms.assetid: 523e3ea4-1d4e-45d1-bc24-93aa2fb14390
title: Procedure consigliate per l'API broadband mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399c2ebc40a357eac9686bc3c2c9f471e3b853f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226195"
---
# <a name="mobile-broadband-api-best-practices"></a><span data-ttu-id="cbc7a-103">Procedure consigliate per l'API broadband mobile</span><span class="sxs-lookup"><span data-stu-id="cbc7a-103">Mobile Broadband API Best Practices</span></span>

<span data-ttu-id="cbc7a-104">Quando si lavora con l'API Mobile Broadband, è necessario usare il set di procedure consigliate seguente per ottenere le migliori prestazioni possibili.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-104">When working with the Mobile Broadband API the following set of best practices should be used in order to achieve the best possible performance.</span></span>

## <a name="do-not-cache-functional-objects"></a><span data-ttu-id="cbc7a-105">Non memorizzare nella cache oggetti funzionali</span><span class="sxs-lookup"><span data-stu-id="cbc7a-105">Do Not Cache Functional Objects</span></span>

<span data-ttu-id="cbc7a-106">Gli oggetti funzionali, ad esempio [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) e altri, vengono ottenuti da oggetti Manager, come [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), usando il metodo di enumerazione nell'oggetto gestione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-106">Functional objects, such as [**IMbnInterface**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) and others, are obtained from manager objects, like [**IMbnInterfaceManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), using the enumeration method on the corresponding manager object.</span></span> <span data-ttu-id="cbc7a-107">Non memorizzare nella cache questi oggetti funzionali, perché gli oggetti funzionali memorizzati nella cache contengono dati non aggiornati.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-107">Do not cache these functional objects, since cached functional objects contain stale data.</span></span> <span data-ttu-id="cbc7a-108">Le operazioni sincrone eseguite su questi oggetti funzionali restituiranno gli stessi dati finché gli oggetti funzionali non verranno nuovamente ottenuti.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-108">The synchronous operations performed on these functional objects will return the same data until the functional objects are obtained again.</span></span>

<span data-ttu-id="cbc7a-109">Al contrario, memorizzare nella cache gli oggetti Manager e ottenere gli oggetti funzionali dall'oggetto gestione usando il metodo di enumerazione sull'oggetto gestione corrispondente per ottenere i dati più recenti.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-109">Instead, cache the manager objects and obtain the functional objects from manager object using the enumeration method on the corresponding manager object again to get the latest data.</span></span>

<span data-ttu-id="cbc7a-110">Nell'esempio di codice riportato di seguito viene illustrato il modo corretto per memorizzare nella cache gli oggetti di gestione.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-110">The following code example demonstrates the proper way to cache manager objects.</span></span>


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



## <a name="handle-all-notifications"></a><span data-ttu-id="cbc7a-111">Gestisci tutte le notifiche</span><span class="sxs-lookup"><span data-stu-id="cbc7a-111">Handle All Notifications</span></span>

<span data-ttu-id="cbc7a-112">Seguire e gestire tutte le notifiche, anche se non vengono attivate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-112">Follow and handle all notifications, even if they are not triggered by your application.</span></span> <span data-ttu-id="cbc7a-113">Questa operazione è necessaria per sincronizzare l'interfaccia utente con lo stato effettivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-113">This is required to keep the UI in sync with the actual state of the device.</span></span>

<span data-ttu-id="cbc7a-114">In un computer può essere in esecuzione più di una gestione connessione.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-114">There can be more than one connection manager running on a computer.</span></span> <span data-ttu-id="cbc7a-115">L'interfaccia utente dell'interfaccia di rete disponibile per la visualizzazione nativa fornita da Windows 7 è una gestione connessione.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-115">The native View Available Network Interface UI provided by Windows 7 is a connection manager.</span></span> <span data-ttu-id="cbc7a-116">Tutte le altre gestioni connessioni devono rispondere a tutte le notifiche per rimanere sincronizzate con l'interfaccia utente nativa di Windows.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-116">Any other connection managers need to respond to all notifications to remain in sync the Windows native UI.</span></span> <span data-ttu-id="cbc7a-117">Un utente può scegliere di eseguire un'operazione su una delle gestioni connessioni che può comportare una modifica dello stato del dispositivo mobile broadband.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-117">A user may opt to perform some operation on one of the connection managers which may result in a state change of the Mobile Broadband device.</span></span> <span data-ttu-id="cbc7a-118">Tuttavia, altre gestioni connessioni devono rimanere aggiornate per indicare correttamente lo stato modificato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-118">However, other connection managers need to remain updated in order to properly indicate the modified state of the device.</span></span>

<span data-ttu-id="cbc7a-119">Se ad esempio si esegue una connessione utilizzando una delle gestioni connessioni, lo stato del dispositivo viene modificato da disponibile a connesso.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-119">For example, performing a connect using one of the connection managers will change the state of the device from available to connected.</span></span> <span data-ttu-id="cbc7a-120">Questa modifica dovrebbe essere visibile alle gestioni connessioni che non hanno avviato l'azione.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-120">This change should be visible to the connection managers that didn’t initiate this action.</span></span> <span data-ttu-id="cbc7a-121">Tutte le gestioni connessioni con interfaccia utente che indica lo stato di connessione del dispositivo, devono rimanere in ascolto e gestire le notifiche dello stato della connessione per aggiornare correttamente l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-121">All connection managers that have UI that indicates the connection state of the device, need to listen to and handle the connection state notifications in order to properly update their user interface.</span></span>

## <a name="sending-and-receiving-bytes"></a><span data-ttu-id="cbc7a-122">Invio e ricezione di byte</span><span class="sxs-lookup"><span data-stu-id="cbc7a-122">Sending And Receiving Bytes</span></span>

<span data-ttu-id="cbc7a-123">Usare le funzioni helper IP [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) e [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) per inviare e ricevere byte.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-123">Use the IP Helper functions [GetlfEntry](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) and [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) to send and receive bytes.</span></span>

## <a name="using-the-pin-unblock-api"></a><span data-ttu-id="cbc7a-124">Uso dell'API di sblocco PIN</span><span class="sxs-lookup"><span data-stu-id="cbc7a-124">Using The Pin Unblock API</span></span>

<span data-ttu-id="cbc7a-125">Per poter richiamare [**IMbnPin:: Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock), un'applicazione client chiamante deve essere elevata.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-125">A calling client application must be elevated in order to successfully to invoke [**IMbnPin::Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock).</span></span> <span data-ttu-id="cbc7a-126">Questo metodo è l'unica parte dell'API broadband mobile che richiede privilegi di amministratore o NCO.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-126">This method is the only portion of the Mobile Broadband API that requires administrator or NCO privileges.</span></span> <span data-ttu-id="cbc7a-127">Per ulteriori informazioni, vedere [la descrizione del gruppo Network Configuration Operators]( https://support.microsoft.com/kb/297938/en-us) .</span><span class="sxs-lookup"><span data-stu-id="cbc7a-127">See [A Description of the Network Configuration Operators Group]( https://support.microsoft.com/kb/297938/en-us) for more information.</span></span>

## <a name="working-with-safearrays"></a><span data-ttu-id="cbc7a-128">Utilizzo di SafeArrays</span><span class="sxs-lookup"><span data-stu-id="cbc7a-128">Working With SafeArrays</span></span>

-   <span data-ttu-id="cbc7a-129">Utilizzare ZeroMemory () prima di accedere a qualsiasi elemento in un SafeArray.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-129">Use ZeroMemory() before accessing any elements in a SafeArray.</span></span>

-   <span data-ttu-id="cbc7a-130">Non controllare gli indici di un SafeArray.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-130">Don’t check on the indexes of a SafeArray.</span></span> <span data-ttu-id="cbc7a-131">Potrebbero essere negativi.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-131">They may be negative.</span></span>

<span data-ttu-id="cbc7a-132">Nell'esempio di codice seguente viene illustrato come gestire correttamente un SafeArray.</span><span class="sxs-lookup"><span data-stu-id="cbc7a-132">The following code example shows how to properly handle a SafeArray.</span></span>


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



 

 
