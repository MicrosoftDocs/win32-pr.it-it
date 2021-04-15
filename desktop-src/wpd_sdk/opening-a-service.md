---
description: Apertura di un servizio
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: Apertura di un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0bcccc6c3769173bfee72e73d7cbf68435b0ba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529526"
---
# <a name="opening-a-service"></a><span data-ttu-id="13644-103">Apertura di un servizio</span><span class="sxs-lookup"><span data-stu-id="13644-103">Opening a Service</span></span>

<span data-ttu-id="13644-104">Prima che l'applicazione possa eseguire operazioni su un servizio, ad esempio l'enumerazione del contenuto o il recupero di descrizioni di eventi o metodi supportati, deve aprire il servizio.</span><span class="sxs-lookup"><span data-stu-id="13644-104">Before your application can perform operations on a service, for example, enumerating content or retrieving descriptions of supported events or methods, it must open the service.</span></span> <span data-ttu-id="13644-105">Nell'applicazione WpdServicesApiSample questa attività è illustrata nel modulo ServiceEnumeration. cpp usando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="13644-105">In the WpdServicesApiSample application, this task is demonstrated in the ServiceEnumeration.cpp module using the interfaces described in the following table.</span></span>



|                                                                        |                                                    |
|------------------------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="13644-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="13644-106">Interface</span></span>                                                              | <span data-ttu-id="13644-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13644-107">Description</span></span>                                        |
| [<span data-ttu-id="13644-108">**IPortableDeviceServiceManager**</span><span class="sxs-lookup"><span data-stu-id="13644-108">**IPortableDeviceServiceManager**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | <span data-ttu-id="13644-109">Usato per enumerare i servizi in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13644-109">Used to enumerate the services on a device.</span></span>        |
| [<span data-ttu-id="13644-110">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="13644-110">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="13644-111">Consente di aprire una connessione a un servizio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13644-111">Used to open a connection to a device service.</span></span>     |
| [<span data-ttu-id="13644-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="13644-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="13644-113">Usato per conservare le informazioni sul client dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="13644-113">Used to hold the application's client information.</span></span> |



 

<span data-ttu-id="13644-114">Il metodo che apre un servizio è [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span><span class="sxs-lookup"><span data-stu-id="13644-114">The method that opens a service is [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span> <span data-ttu-id="13644-115">Questo metodo accetta due argomenti: un identificatore Plug-and-Play (PnP) per il servizio e un oggetto [**IPortableDeviceValues**](iportabledevicevalues.md) che contiene le informazioni sul client dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="13644-115">This method takes two arguments: a Plug-and-Play (PnP) identifier for the service and an [**IPortableDeviceValues**](iportabledevicevalues.md) object that contains the application's client information.</span></span>

<span data-ttu-id="13644-116">Per ottenere un identificatore PnP per un determinato servizio, l'applicazione chiama il metodo [**IPortableDeviceServiceManager:: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) .</span><span class="sxs-lookup"><span data-stu-id="13644-116">To obtain a PnP identifier for a given service, your application calls the [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) method.</span></span> <span data-ttu-id="13644-117">Questo metodo recupera una matrice di identificatori PnP per i servizi di un GUID della categoria di servizio, ad esempio i contatti del servizio.</span><span class="sxs-lookup"><span data-stu-id="13644-117">This method retrieves an array of PnP identifiers for services of a service category GUID (for example SERVICE Contacts).</span></span>

<span data-ttu-id="13644-118">L'applicazione di servizio di esempio recupera un identificatore PnP per i servizi Contacts all'interno del metodo **EnumerateContactsServices** nel modulo ServiceEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="13644-118">The sample Service application retrieves a PnP identifier for Contacts services within the **EnumerateContactsServices** method in the ServiceEnumeration.cpp module.</span></span> <span data-ttu-id="13644-119">Il codice di esempio seguente viene tratto da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="13644-119">The following code sample is taken from this method.</span></span>


```C++
// For each device found, find the contacts service
for (dwIndex = 0; dwIndex < cPnpDeviceIDs; dwIndex++)
{
    DWORD   cPnpServiceIDs = 0;
    PWSTR   pPnpServiceID  = NULL;

    // First, pass NULL as the PWSTR array pointer to get the total number
    // of contacts services (SERVICE_Contacts) found on the device.
    // To find the total number of all services on the device, use GUID_DEVINTERFACE_WPD_SERVICE.
    hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, NULL, &cPnpServiceIDs);
    
    if (SUCCEEDED(hr) && (cPnpServiceIDs > 0))
    {                               
        // For simplicity, we are only using the first contacts service on each device
        cPnpServiceIDs = 1;
        hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, &pPnpServiceID, &cPnpServiceIDs);

        if (SUCCEEDED(hr))
        {
            // We've found the service, display it and save its PnP Identifier
            ContactsServicePnpIDs.Add(pPnpServiceID);

            printf("[%d] ", static_cast<DWORD>(ContactsServicePnpIDs.GetCount()-1));

            // Display information about the device that contains this service.
            DisplayDeviceInformation(pServiceManager, pPnpServiceID);

            // ContactsServicePnpIDs now owns the memory for this string
            pPnpServiceID = NULL;
        }
        else
        {
            printf("! Failed to get the first contacts service from '%ws, hr = 0x%lx\n",pPnpDeviceIDs[dwIndex],hr);
        }
    }
}
```



<span data-ttu-id="13644-120">Quando l'applicazione recupera l'identificatore PnP per il servizio, può configurare le informazioni client e chiamare [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span><span class="sxs-lookup"><span data-stu-id="13644-120">After your application retrieves the PnP identifier for the service, it can set up the client information and call [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span>

<span data-ttu-id="13644-121">Nell'applicazione di esempio, questo metodo viene chiamato all'interno di **ChooseDeviceService** nel modulo ServiceEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="13644-121">In the sample application, this method is called within **ChooseDeviceService** in the ServiceEnumeration.cpp module.</span></span>

<span data-ttu-id="13644-122">[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) supporta due CLSID per **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="13644-122">[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="13644-123">**CLSID \_ PortableDeviceService** restituisce un puntatore **IPortableDeviceService** che non aggrega il gestore di marshalling a thread libero. **CLSID \_ PortableDeviceServiceFTM** è un nuovo CLSID che restituisce un puntatore **IPortableDeviceService** che aggrega il gestore di marshalling a thread libero.</span><span class="sxs-lookup"><span data-stu-id="13644-123">**CLSID\_PortableDeviceService** returns an **IPortableDeviceService** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceServiceFTM** is a new CLSID that returns an **IPortableDeviceService** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="13644-124">Entrambi i puntatori supportano la stessa funzionalità in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="13644-124">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="13644-125">Le applicazioni che si trovano in Apartment a thread singolo devono usare **CLSID \_ PortableDeviceServiceFTM** , in quanto in questo modo si elimina l'overhead del marshalling del puntatore di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="13644-125">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceServiceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="13644-126">**CLSID \_ PortableDeviceService** è ancora supportato per le applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="13644-126">**CLSID\_PortableDeviceService** is still supported for legacy applications.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDeviceServiceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pService));
if (SUCCEEDED(hr))
{
    hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the service for Read Write access, will open it for Read-only access instead\n");

            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);

            hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);

            if (FAILED(hr))
            {
                printf("! Failed to Open the service for Read access, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            printf("! Failed to Open the service, hr = 0x%lx\n",hr);
        }
    }
```



## <a name="related-topics"></a><span data-ttu-id="13644-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13644-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13644-128">**Interfaccia IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="13644-128">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="13644-129">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="13644-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="13644-130">**Interfaccia IPortableDeviceServiceManager**</span><span class="sxs-lookup"><span data-stu-id="13644-130">**IPortableDeviceServiceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[<span data-ttu-id="13644-131">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="13644-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



