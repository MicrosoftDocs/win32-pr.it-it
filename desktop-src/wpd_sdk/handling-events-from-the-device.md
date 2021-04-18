---
description: Gestione degli eventi dal dispositivo
ms.assetid: 529a8b7a-08b4-47de-8ed3-28e8fff0ede2
title: Gestione degli eventi dal dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74692b73e39aa83286604408f3c556f5fbeb3f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319090"
---
# <a name="handling-events-from-the-device"></a><span data-ttu-id="9df09-103">Gestione degli eventi dal dispositivo</span><span class="sxs-lookup"><span data-stu-id="9df09-103">Handling Events from the Device</span></span>

<span data-ttu-id="9df09-104">Un'altra operazione eseguita da un'applicazione WPD è la gestione degli eventi generati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9df09-104">Another operation accomplished by a WPD application is the handling of events that are fired by the device.</span></span>

<span data-ttu-id="9df09-105">Le operazioni di gestione degli eventi vengono eseguite utilizzando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9df09-105">Event handling operations are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="9df09-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="9df09-106">Interface</span></span>                                                                      | <span data-ttu-id="9df09-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9df09-107">Description</span></span>                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="9df09-108">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="9df09-108">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                           | <span data-ttu-id="9df09-109">Consente all'applicazione di eseguire la registrazione per ricevere callback asincroni.</span><span class="sxs-lookup"><span data-stu-id="9df09-109">Lets the application register to receive asynchronous callbacks.</span></span> |
| [<span data-ttu-id="9df09-110">**Interfaccia IPortableDeviceEventCallback**</span><span class="sxs-lookup"><span data-stu-id="9df09-110">**IPortableDeviceEventCallback Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback) | <span data-ttu-id="9df09-111">Contiene il gestore eventi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9df09-111">Contains the application's event handler.</span></span>                        |



 

<span data-ttu-id="9df09-112">La classe CPortableDeviceEventsCallback nel modulo DeviceEvents. cpp dell'applicazione di esempio illustra come un'applicazione può implementare [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback).</span><span class="sxs-lookup"><span data-stu-id="9df09-112">The CPortableDeviceEventsCallback class in the sample application's DeviceEvents.cpp module demonstrates how an application can implement [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback).</span></span> <span data-ttu-id="9df09-113">L'implementazione del metodo [**OnEvent**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceeventcallback-onevent) in questa classe scrive i parametri per qualsiasi evento nella finestra della console dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9df09-113">The implementation of the [**OnEvent**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceeventcallback-onevent) method in this class writes the parameters for any event to the application's console window.</span></span> <span data-ttu-id="9df09-114">Oltre al metodo OnEvent, questa classe implementa AddRef e release, che vengono usati per gestire il conteggio dei riferimenti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9df09-114">In addition to the OnEvent method, this class implements AddRef and Release, which are used to maintain the object's reference count.</span></span>


```C++
class CPortableDeviceEventsCallback : public IPortableDeviceEventCallback
{
public:
    CPortableDeviceEventsCallback() : m_cRef(1)
    {
    }

    ~CPortableDeviceEventsCallback()
    {
    }

    HRESULT __stdcall QueryInterface(
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
            (riid == IID_IPortableDeviceEventCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    ULONG __stdcall AddRef()
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    ULONG __stdcall Release()
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

    HRESULT __stdcall OnEvent(
        IPortableDeviceValues* pEventParameters)
    {
        HRESULT hr = S_OK;

        if (pEventParameters != NULL)
        {
            printf("***************************\n** Device event received **\n***************************\n");
            DisplayStringProperty(pEventParameters, WPD_EVENT_PARAMETER_PNP_DEVICE_ID, L"WPD_EVENT_PARAMETER_PNP_DEVICE_ID");
            DisplayGuidProperty(pEventParameters, WPD_EVENT_PARAMETER_EVENT_ID, L"WPD_EVENT_PARAMETER_EVENT_ID");
        }

        return hr;
    }

    ULONG m_cRef;
};
```



<span data-ttu-id="9df09-115">L'applicazione di esempio crea un'istanza della classe CPortableDeviceEventsCallback nella relativa funzione helper RegisterForEventNotifications.</span><span class="sxs-lookup"><span data-stu-id="9df09-115">The sample application instantiates the CPortableDeviceEventsCallback class in its RegisterForEventNotifications helper function.</span></span> <span data-ttu-id="9df09-116">Questa funzione crea un'istanza dell'oggetto callback usando l'operatore new.</span><span class="sxs-lookup"><span data-stu-id="9df09-116">This function creates an instance of the callback object using the new operator.</span></span> <span data-ttu-id="9df09-117">Chiama quindi il metodo [**IPortableDevice:: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) per registrare il callback e iniziare a ricevere gli eventi.</span><span class="sxs-lookup"><span data-stu-id="9df09-117">It then calls the [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) method to register the callback and begin receiving events.</span></span>


```C++
void RegisterForEventNotifications(IPortableDevice* pDevice)
{
    HRESULT                        hr = S_OK;
    LPWSTR                         wszEventCookie = NULL;
    CPortableDeviceEventsCallback* pCallback = NULL;

    if (pDevice == NULL)
    {
        return;
    }

    // Check to see if we already have an event registration cookie.  If so,
    // then avoid registering again.
    // NOTE: An application can register for events as many times as they want.
    //       This sample only keeps a single registration cookie around for
    //       simplicity.
    if (g_strEventRegistrationCookie.GetLength() > 0)
    {
        printf("This application has already registered to receive device events.\n");
        return;
    }

    // Create an instance of the callback object.  This will be called when events
    // are received.
    if (hr == S_OK)
    {
        pCallback = new CPortableDeviceEventsCallback();
        if (pCallback == NULL)
        {
            hr = E_OUTOFMEMORY;
            printf("Failed to allocate memory for IPortableDeviceEventsCallback object, hr = 0x%lx\n",hr);
        }
    }

    // Call Advise to register the callback and receive events.
    if (hr == S_OK)
    {
        hr = pDevice->Advise(0, pCallback, NULL, &wszEventCookie);
        if (FAILED(hr))
        {
            printf("! Failed to register for device events, hr = 0x%lx\n",hr);
        }
    }

    // Save the event registration cookie if event registration was successful.
    if (hr == S_OK)
    {
        g_strEventRegistrationCookie = wszEventCookie;
    }

    // Free the event registration cookie, if one was returned.
    if (wszEventCookie != NULL)
    {
        CoTaskMemFree(wszEventCookie);
        wszEventCookie = NULL;
    }

    if (hr == S_OK)
    {
        printf("This application has registered for device event notifications and was returned the registration cookie '%ws'", g_strEventRegistrationCookie.GetString());
    }

    // If a failure occurs, remember to delete the allocated callback object, if one exists.
    if (pCallback != NULL)
    {
        pCallback->Release();
    }
```



<span data-ttu-id="9df09-118">Quando l'applicazione di esempio riceve gli eventi, chiama la funzione di supporto UnregisterForEventNotifications.</span><span class="sxs-lookup"><span data-stu-id="9df09-118">Once the sample application is through receiving events, it calls the UnregisterForEventNotifications helper function.</span></span> <span data-ttu-id="9df09-119">Questa funzione, a sua volta, chiama il metodo [**IPortableDevice:: Unadvise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-unadvise) per annullare la registrazione del callback dalla ricezione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="9df09-119">This function, in turn, calls the [**IPortableDevice::Unadvise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-unadvise) method to unregister the callback from receiving events.</span></span>


```C++
void UnregisterForEventNotifications(IPortableDevice* pDevice)
{
    HRESULT hr = S_OK;

    if (pDevice == NULL)
    {
        return;
    }

    hr = pDevice->Unadvise(g_strEventRegistrationCookie);
    if (FAILED(hr))
    {
        printf("! Failed to unregister for device events using registration cookie '%ws', hr = 0x%lx\n",g_strEventRegistrationCookie.GetString(), hr);
    }

    if (hr == S_OK)
    {
        printf("This application used the registration cookie '%ws' to unregister from receiving device event notifications", g_strEventRegistrationCookie.GetString());
    }

    g_strEventRegistrationCookie = L"";
}
```



## <a name="related-topics"></a><span data-ttu-id="9df09-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9df09-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9df09-121">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="9df09-121">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="9df09-122">**Interfaccia IPortableDeviceEventCallback**</span><span class="sxs-lookup"><span data-stu-id="9df09-122">**IPortableDeviceEventCallback Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)
</dt> <dt>

[<span data-ttu-id="9df09-123">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="9df09-123">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



