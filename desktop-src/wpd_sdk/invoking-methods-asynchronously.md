---
description: Richiamo asincrono di metodi del servizio
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Richiamo asincrono di metodi del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d312cc76cf8cb737136629c1e2c8135d1b7bd1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232460"
---
# <a name="invoking-service-methods-asynchronously"></a><span data-ttu-id="da839-103">Richiamo asincrono di metodi del servizio</span><span class="sxs-lookup"><span data-stu-id="da839-103">Invoking Service Methods Asynchronously</span></span>

<span data-ttu-id="da839-104">L'applicazione WpdServiceApiSample include codice che illustra come un'applicazione può richiamare i metodi del servizio in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="da839-104">The WpdServiceApiSample application includes code that demonstrates how an application can invoke the service methods asynchronously.</span></span> <span data-ttu-id="da839-105">In questo esempio vengono utilizzate le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="da839-105">This sample uses the following interfaces.</span></span>



|                                                                                         |                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da839-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="da839-106">Interface</span></span>                                                                               | <span data-ttu-id="da839-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da839-107">Description</span></span>                                                                                                                                                             |
| [<span data-ttu-id="da839-108">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="da839-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | <span data-ttu-id="da839-109">Utilizzato per recuperare l'interfaccia **IPortableDeviceServiceMethods** per richiamare i metodi su un servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="da839-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="da839-110">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="da839-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | <span data-ttu-id="da839-111">Utilizzato per richiamare un metodo del servizio.</span><span class="sxs-lookup"><span data-stu-id="da839-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="da839-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="da839-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                                  | <span data-ttu-id="da839-113">Utilizzato per conservare i parametri del metodo in uscita e i risultati del metodo in arrivo.</span><span class="sxs-lookup"><span data-stu-id="da839-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="da839-114">Può essere **null** se il metodo non richiede parametri o restituisce alcun risultato.</span><span class="sxs-lookup"><span data-stu-id="da839-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |
| [<span data-ttu-id="da839-115">**IPortableDeviceServiceMethodCallback**</span><span class="sxs-lookup"><span data-stu-id="da839-115">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | <span data-ttu-id="da839-116">Implementata dall'applicazione per ricevere i risultati del metodo quando un metodo è stato completato.</span><span class="sxs-lookup"><span data-stu-id="da839-116">Implemented by the application to receive the method results when a method has completed.</span></span>                                                                               |



 

<span data-ttu-id="da839-117">Quando l'utente sceglie l'opzione "10" dalla riga di comando, l'applicazione richiama il metodo **InvokeMethodsAsync** trovato nel modulo ServiceMethods. cpp.</span><span class="sxs-lookup"><span data-stu-id="da839-117">When the user chooses option "10" at the command line, the application invokes the **InvokeMethodsAsync** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="da839-118">Si noti che prima di richiamare i metodi, l'applicazione di esempio apre un servizio di contatti in un dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="da839-118">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="da839-119">I metodi di servizio incapsulano le funzionalità che ogni servizio definisce e implementa.</span><span class="sxs-lookup"><span data-stu-id="da839-119">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="da839-120">Sono univoche per ogni tipo di servizio e sono rappresentate da un GUID.</span><span class="sxs-lookup"><span data-stu-id="da839-120">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="da839-121">Il servizio contatti, ad esempio, definisce un metodo **BeginSync** che le applicazioni chiamano per preparare il dispositivo per la sincronizzazione degli oggetti contatto e un metodo **EndSync** per notificare al dispositivo che la sincronizzazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="da839-121">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="da839-122">Le applicazioni eseguono un metodo di servizio del dispositivo portatile chiamando [**IPortableDeviceServiceMethods:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span><span class="sxs-lookup"><span data-stu-id="da839-122">Applications execute a portable device service method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="da839-123">I metodi del servizio non devono essere confusi con i comandi WPD.</span><span class="sxs-lookup"><span data-stu-id="da839-123">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="da839-124">I comandi WPD fanno parte dell'interfaccia DDI (WPD Device Driver Interface) standard e sono il meccanismo per la comunicazione tra un'applicazione WPD e il driver.</span><span class="sxs-lookup"><span data-stu-id="da839-124">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="da839-125">I comandi sono predefiniti, raggruppati per categorie (ad esempio, **\_ categoria WPD \_ comune**) e sono rappresentati da una struttura **PropertyKey** .</span><span class="sxs-lookup"><span data-stu-id="da839-125">Commands are predefined, grouped by categories (for example, **WPD\_CATEGORY\_COMMON**), and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="da839-126">Un'applicazione invia comandi al driver di dispositivo chiamando [**IPortableDeviceService:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="da839-126">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="da839-127">Per ulteriori informazioni, vedere l'argomento Commands (comandi).</span><span class="sxs-lookup"><span data-stu-id="da839-127">For more information, see the Commands topic.</span></span>

<span data-ttu-id="da839-128">Il metodo **InvokeMethodsAsync** richiama [**IPortableDeviceService:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare un'interfaccia [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="da839-128">The **InvokeMethodsAsync** method invokes [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="da839-129">Utilizzando questa interfaccia, viene richiamata la funzione helper **InvokeMethodAsync** due volte; una volta per il metodo **BeginSync** e una volta per il metodo **EndSync** .</span><span class="sxs-lookup"><span data-stu-id="da839-129">Using this interface, it invokes the **InvokeMethodAsync** helper function twice; once for the **BeginSync** method and once for the **EndSync** method.</span></span> <span data-ttu-id="da839-130">In questo esempio, **InvokeMethodAsync** attende indefinitamente che un evento globale venga segnalato quando viene chiamato [**IPortableDeviceServiceMethodCallback:: OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) .</span><span class="sxs-lookup"><span data-stu-id="da839-130">In this example, , **InvokeMethodAsync** waits indefinitely for a global event to be signaled when [**IPortableDeviceServiceMethodCallback::OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) is called.</span></span>

<span data-ttu-id="da839-131">Il codice seguente usa il metodo **InvokeMethodsAsync** .</span><span class="sxs-lookup"><span data-stu-id="da839-131">The following code uses the **InvokeMethodsAsync** method.</span></span>


```C++
// Invoke methods on the Contacts Service asynchornously.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethodsAsync(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke the BeginSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_BeginSync);

        // This method does not take any parameters, so we pass in NULL
        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_BeginSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_EndSync);

        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_EndSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
    }
}
```



<span data-ttu-id="da839-132">Per ogni metodo richiamato, la funzione helper **InvokeMethodAsync** esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="da839-132">The **InvokeMethodAsync** helper function does the following for each method that it invokes:</span></span>

-   <span data-ttu-id="da839-133">Crea un handle di evento globale che monitora per determinare il completamento del metodo.</span><span class="sxs-lookup"><span data-stu-id="da839-133">Creates a global event handle that it monitors to determine method completion.</span></span>
-   <span data-ttu-id="da839-134">Crea un oggetto **CMethodCallback** fornito come argomento per [**IPortableDeviceServiceMethods: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).</span><span class="sxs-lookup"><span data-stu-id="da839-134">Creates a **CMethodCallback** object that is supplied as an argument to [**IPortableDeviceServiceMethods:InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).</span></span>
-   <span data-ttu-id="da839-135">Chiama il metodo **IPortableDeviceServiceMethods:: InvokeAsync** per richiamare il metodo specificato.</span><span class="sxs-lookup"><span data-stu-id="da839-135">Calls the **IPortableDeviceServiceMethods::InvokeAsync** method to invoke the given method.</span></span>
-   <span data-ttu-id="da839-136">Esegue il monitoraggio dell'handle di evento globale per il completamento.</span><span class="sxs-lookup"><span data-stu-id="da839-136">Monitors the global event handle for completion.</span></span>
-   <span data-ttu-id="da839-137">Esegue la pulizia.</span><span class="sxs-lookup"><span data-stu-id="da839-137">Performs cleanup.</span></span>

<span data-ttu-id="da839-138">La classe **CMethodCallback** illustra come un'applicazione può implementare [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback).</span><span class="sxs-lookup"><span data-stu-id="da839-138">The **CMethodCallback** class demonstrates how an application can implement [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback).</span></span> <span data-ttu-id="da839-139">L'implementazione di **OnComplete** in questa classe segnala un evento per notificare all'applicazione che il metodo del servizio è stato completato.</span><span class="sxs-lookup"><span data-stu-id="da839-139">The implementation of **OnComplete** in this class signals an event to notify the application that the service method has completed.</span></span> <span data-ttu-id="da839-140">Oltre al metodo **OnComplete** , questa classe implementa **AddRef**, **QueryInterface** e **Release**, che vengono utilizzati per gestire il conteggio dei riferimenti dell'oggetto e le interfacce implementate.</span><span class="sxs-lookup"><span data-stu-id="da839-140">In addition to the **OnComplete** method, this class implements **AddRef**, **QueryInterface**, and **Release**, which are used to maintain the object's reference count and the interfaces that it implements.</span></span>


```C++
class CMethodCallback : public IPortableDeviceServiceMethodCallback
{
public:
   CMethodCallback () : m_cRef(1)
   {
   }

   ~CMethodCallback ()
   {
   }

public:
    // IPortableDeviceServiceMethodCallback::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE OnComplete(
        HRESULT                 hrStatus,
        IPortableDeviceValues*  /*pResults*/) // We are ignoring results as our methods will not return any results
    {
        printf("** Method completed, status HRESULT = 0x%lx **\n", hrStatus);

        if (g_hMethodCompleteEvent != NULL)
        {
            SetEvent(g_hMethodCompleteEvent);
        }          
        return S_OK;
    }

    // IUnknown::AddRef
    virtual ULONG STDMETHODCALLTYPE AddRef(void)
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    // IUnknown::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceServiceMethodCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            *ppvObj = NULL;
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    // IUnknown::Release
    virtual ULONG STDMETHODCALLTYPE Release(void)
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

private:
    DWORD   m_cRef;
};
```



## <a name="related-topics"></a><span data-ttu-id="da839-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da839-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da839-142">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="da839-142">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="da839-143">**IPortableDeviceServiceMethodCallback**</span><span class="sxs-lookup"><span data-stu-id="da839-143">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[<span data-ttu-id="da839-144">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="da839-144">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="da839-145">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="da839-145">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
