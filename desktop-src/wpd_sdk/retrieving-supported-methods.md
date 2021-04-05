---
description: Recupero di metodi di servizio supportati
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: Recupero di metodi di servizio supportati
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6029af655a8835a4eee887d919c534856062ff13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883146"
---
# <a name="retrieving-supported-service-methods"></a><span data-ttu-id="f243a-103">Recupero di metodi di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="f243a-103">Retrieving Supported Service Methods</span></span>

<span data-ttu-id="f243a-104">I metodi di servizio incapsulano le funzionalità che ogni servizio definisce e implementa.</span><span class="sxs-lookup"><span data-stu-id="f243a-104">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="f243a-105">Sono specifici di ogni tipo di servizio e sono rappresentati da un GUID univoco.</span><span class="sxs-lookup"><span data-stu-id="f243a-105">They are specific to each type of service type and are represented by a unique GUID.</span></span>

<span data-ttu-id="f243a-106">Il servizio contatti, ad esempio, definisce un metodo **BeginSync** che le applicazioni chiamano per preparare il dispositivo per la sincronizzazione degli oggetti contatto e un metodo **EndSync** per notificare al dispositivo che la sincronizzazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f243a-106">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span>

<span data-ttu-id="f243a-107">Le applicazioni possono eseguire query a livello di codice sui metodi supportati e accedere a questi metodi e ai relativi attributi usando l'interfaccia [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="f243a-107">Applications can programmatically query the supported methods and access these methods and their attributes by using the [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span>

<span data-ttu-id="f243a-108">I metodi del servizio non devono essere confusi con i comandi WPD.</span><span class="sxs-lookup"><span data-stu-id="f243a-108">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="f243a-109">I comandi WPD fanno parte dell'interfaccia DDI (WPD Device Driver Interface) standard e sono il meccanismo per la comunicazione tra un'applicazione WPD e il driver.</span><span class="sxs-lookup"><span data-stu-id="f243a-109">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="f243a-110">I comandi sono predefiniti, raggruppati per categorie, ad esempio, \_ la categoria WPD \_ comune e sono rappresentati da una struttura PropertyKey.</span><span class="sxs-lookup"><span data-stu-id="f243a-110">Commands are predefined, grouped by categories, for example, WPD\_CATEGORY\_COMMON, and are represented by a PROPERTYKEY structure.</span></span> <span data-ttu-id="f243a-111">Per ulteriori informazioni, vedere l'argomento [**Commands (comandi**](commands.md) ).</span><span class="sxs-lookup"><span data-stu-id="f243a-111">For more information, see the [**Commands**](commands.md) topic.</span></span>

<span data-ttu-id="f243a-112">L'applicazione WpdServicesApiSample include codice che illustra come un'applicazione può recuperare i metodi supportati da un determinato servizio contatti usando le interfacce riportate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f243a-112">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the methods supported by a given Contacts service by using the interfaces in the following table.</span></span>



|                                                                                      |                                                                                                                |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f243a-113">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="f243a-113">Interface</span></span>                                                                            | <span data-ttu-id="f243a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f243a-114">Description</span></span>                                                                                                    |
| [<span data-ttu-id="f243a-115">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="f243a-115">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="f243a-116">Utilizzato per recuperare l'interfaccia **IPortableDeviceServiceCapabilities** per accedere ai metodi del servizio supportati.</span><span class="sxs-lookup"><span data-stu-id="f243a-116">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported service methods.</span></span> |
| [<span data-ttu-id="f243a-117">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f243a-117">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="f243a-118">Fornisce l'accesso ai metodi supportati, agli attributi del metodo e ai parametri del metodo.</span><span class="sxs-lookup"><span data-stu-id="f243a-118">Provides access to the supported methods, method attributes and method parameters.</span></span>                             |
| [<span data-ttu-id="f243a-119">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="f243a-119">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="f243a-120">Contiene l'elenco dei metodi supportati.</span><span class="sxs-lookup"><span data-stu-id="f243a-120">Contains the list of supported methods.</span></span>                                                                        |
| [<span data-ttu-id="f243a-121">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f243a-121">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="f243a-122">Contiene gli attributi per un metodo e per i parametri di un metodo specificato.</span><span class="sxs-lookup"><span data-stu-id="f243a-122">Contains the attributes for a method and for a given method's parameters.</span></span>                                      |
| [<span data-ttu-id="f243a-123">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="f243a-123">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="f243a-124">Contiene i parametri per un determinato metodo.</span><span class="sxs-lookup"><span data-stu-id="f243a-124">Contains the parameters for a given method.</span></span>                                                                    |



 

<span data-ttu-id="f243a-125">Quando l'utente sceglie l'opzione "5" nella riga di comando, l'applicazione richiama il metodo **ListSupportedMethods** trovato nel modulo ServiceMethods. cpp.</span><span class="sxs-lookup"><span data-stu-id="f243a-125">When the user chooses option "5" at the command line, the application invokes the **ListSupportedMethods** method that is found in the ServiceMethods.cpp module.</span></span>

<span data-ttu-id="f243a-126">Si noti che prima di recuperare l'elenco di eventi, l'applicazione di esempio apre un servizio contatti in un dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="f243a-126">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="f243a-127">In WPD un metodo viene descritto in base al nome, ai diritti di accesso, ai parametri e ai dati correlati.</span><span class="sxs-lookup"><span data-stu-id="f243a-127">In WPD, a method is described by its name, access rights, parameters, and related data.</span></span> <span data-ttu-id="f243a-128">Nell'applicazione di esempio viene visualizzato un nome descrittivo, ad esempio, "CustomMethod" o un GUID.</span><span class="sxs-lookup"><span data-stu-id="f243a-128">The sample application displays a user-friendly name, for example, "CustomMethod", or a GUID.</span></span> <span data-ttu-id="f243a-129">Il nome o il GUID del metodo è seguito dai dati di accesso ("lettura/scrittura"), dal nome di qualsiasi formato associato e dai dati del parametro.</span><span class="sxs-lookup"><span data-stu-id="f243a-129">The method name or GUID is followed by access data ("Read/Write"), the name of any associated format, and the parameter data.</span></span> <span data-ttu-id="f243a-130">Questi dati includono il nome del parametro, l'utilizzo, il VARTYPE e il form.</span><span class="sxs-lookup"><span data-stu-id="f243a-130">This data includes the parameter name, usage, VARTYPE, and form.</span></span>

<span data-ttu-id="f243a-131">Cinque metodi del modulo ServiceMethods. cpp supportano il recupero di metodi (e dati correlati) per il servizio contatti specificato: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat** e **DisplayMethodParameters**.</span><span class="sxs-lookup"><span data-stu-id="f243a-131">Five methods in the ServiceMethods.cpp module support the retrieval of methods (and related data) for the given Contacts service: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters**.</span></span> <span data-ttu-id="f243a-132">Il metodo **ListSupportedMethods** recupera un conteggio dei metodi supportati e l'identificatore GUID per ciascuna. chiama quindi il metodo **DisplayMethod** .</span><span class="sxs-lookup"><span data-stu-id="f243a-132">The **ListSupportedMethods** method retrieves a count of supported methods and the GUID identifier for each; it then calls the **DisplayMethod** method.</span></span> <span data-ttu-id="f243a-133">Il metodo **DisplayMethod** chiama il metodo [**IPortableDeviceServiceCapapbilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) per recuperare le opzioni, i parametri e così via del metodo specificato.</span><span class="sxs-lookup"><span data-stu-id="f243a-133">The **DisplayMethod** method calls the [**IPortableDeviceServiceCapapbilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve the given method's options, parameters, and so on.</span></span> <span data-ttu-id="f243a-134">Dopo che **DisplayMethod** recupera i dati del metodo, esegue il rendering del nome (o del GUID), delle restrizioni di accesso, del formato associato (se presente) e delle descrizioni dei parametri.</span><span class="sxs-lookup"><span data-stu-id="f243a-134">After the **DisplayMethod** retrieves the method data, it renders the name (or GUID), the access restrictions, the associated format (if any), and the parameter descriptions.</span></span> <span data-ttu-id="f243a-135">**DisplayMethodAccess**, **DisplayFormat** e **DisplayMethodParameters** sono funzioni helper che eseguono il rendering dei rispettivi campi di dati.</span><span class="sxs-lookup"><span data-stu-id="f243a-135">The **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** are helper functions that render their respective fields of data.</span></span>

<span data-ttu-id="f243a-136">Il metodo **ListSupportedMethods** richiama il metodo [**IPortableDeviceService:: capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare un'interfaccia [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="f243a-136">The **ListSupportedMethods** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="f243a-137">Utilizzando questa interfaccia, vengono recuperati i metodi supportati chiamando il metodo [**IPortableDeviceServiceCapabilities:: GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) .</span><span class="sxs-lookup"><span data-stu-id="f243a-137">Using this interface, it retrieves the supported methods by calling the [**IPortableDeviceServiceCapabilities::GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="f243a-138">Il metodo **GetSupportedMethods** recupera i GUID per ogni metodo supportato dal servizio e copia il GUID in un oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="f243a-138">The **GetSupportedMethods** method retrieves the GUIDs for each method supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="f243a-139">Il codice seguente usa il metodo **ListSupportedMethods** .</span><span class="sxs-lookup"><span data-stu-id="f243a-139">The following code uses the **ListSupportedMethods** method.</span></span>


```C++
// List all supported methods on the service
void ListSupportedMethods(IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumMethods    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all methods supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedMethods(&pMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get supported methods from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported methods found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pMethods->GetCount(&dwNumMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported methods, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Methods Found on the service\n\n", dwNumMethods);

    // Loop through each method and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumMethods; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pMethods->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a method.  It is assumed that
                // methods are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayMethod(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }    
}
```



<span data-ttu-id="f243a-140">Dopo che il metodo **ListSupportedMethods** Recupera il GUID per ogni evento supportato dal servizio specificato, richiama il metodo **DisplayMethod** per recuperare gli attributi specifici del metodo.</span><span class="sxs-lookup"><span data-stu-id="f243a-140">After the **ListSupportedMethods** method retrieves the GUID for each event supported by the given service, it invokes the **DisplayMethod** method to retrieve the method-specific attributes.</span></span> <span data-ttu-id="f243a-141">Questi attributi includono: il nome descrittivo del metodo, le restrizioni di accesso necessarie, qualsiasi formato associato ed elenco di parametri.</span><span class="sxs-lookup"><span data-stu-id="f243a-141">These attributes include: the method's script-friendly name , required access restrictions, any associated format, and list of parameters.</span></span>

<span data-ttu-id="f243a-142">Il metodo **DisplayMethod** richiama il metodo [**IPortableDeviceServiceCapabilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) per recuperare una raccolta di attributi per il metodo specificato.</span><span class="sxs-lookup"><span data-stu-id="f243a-142">The **DisplayMethod** method invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method to retrieve a collection of attributes for the given method.</span></span> <span data-ttu-id="f243a-143">Chiama quindi il metodo [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) per recuperare il nome del metodo.</span><span class="sxs-lookup"><span data-stu-id="f243a-143">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method to retrieve the method's name.</span></span> <span data-ttu-id="f243a-144">**DisplayMethod** chiama [**IPortableDeviceValues:: GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) per recuperare il restrctions di accesso.</span><span class="sxs-lookup"><span data-stu-id="f243a-144">The **DisplayMethod** calls the [**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) to retrieve the access restrctions.</span></span> <span data-ttu-id="f243a-145">Successivamente, viene chiamato [**IPortableDeviceValues:: GetGuidValue**](iportabledevicevalues-getguidvalue.md) per recuperare qualsiasi formato associato.</span><span class="sxs-lookup"><span data-stu-id="f243a-145">After this, it calls [**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md) to retrieve any associated format.</span></span> <span data-ttu-id="f243a-146">Infine, **DisplayMethod** chiama [**IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) per recuperare i dati del parametro.</span><span class="sxs-lookup"><span data-stu-id="f243a-146">And, finally, the **DisplayMethod** calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the parameter data.</span></span> <span data-ttu-id="f243a-147">Passa i dati restituiti da questi metodi alle funzioni di supporto **DisplayMethodAccess**, **DisplayFormat** e **DisplayMethodParameters** , che eseguono il rendering delle informazioni per il metodo specificato.</span><span class="sxs-lookup"><span data-stu-id="f243a-147">It passes the data returned by these methods to the **DisplayMethodAccess**, **DisplayFormat**, and **DisplayMethodParameters** helper functions, which render the information for the given method.</span></span>

<span data-ttu-id="f243a-148">Il codice seguente usa il metodo **DisplayMethod** .</span><span class="sxs-lookup"><span data-stu-id="f243a-148">The following code uses the **DisplayMethod** method.</span></span>


```C++
// Display basic information about a method
void DisplayMethod(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the method attributes which describe the method
    HRESULT hr = pCapabilities->GetMethodAttributes(Method, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the method attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR   pszMethodName  = NULL;
        DWORD   dwMethodAccess = WPD_COMMAND_ACCESS_READ;
        GUID    guidFormat     = GUID_NULL;

        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the method if available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_METHOD_ATTRIBUTE_NAME, &pszMethodName);
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszMethodName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Method));
        }       

        // Display the method access if available, otherwise default to WPD_COMMAND_ACCESS_READ access
        hr = pAttributes->GetUnsignedIntegerValue(WPD_METHOD_ATTRIBUTE_ACCESS, &dwMethodAccess);
        if (FAILED(hr))
        {
            dwMethodAccess = WPD_COMMAND_ACCESS_READ;
            hr = S_OK;
        }
        printf("\n\tAccess: ");
        DisplayMethodAccess(dwMethodAccess);

        // Display the associated format if specified.
        // Methods that have an associated format may only be supported for that format.
        // Methods that don't have associated formats generally apply to the entire service.
        hr = pAttributes->GetGuidValue(WPD_METHOD_ATTRIBUTE_ASSOCIATED_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("\n\tAssociated Format: ");
            DisplayFormat(pCapabilities, guidFormat);
        }

        // Display the method parameters, if available
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_METHOD_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayMethodParameters(pCapabilities, Method, pParameters);
        }
        
        CoTaskMemFree(pszMethodName);
        pszMethodName = NULL;

    }
}
```



<span data-ttu-id="f243a-149">La funzione helper **DisplayMethodAccess** riceve un valore DWORD che contiene le opzioni di accesso del metodo.</span><span class="sxs-lookup"><span data-stu-id="f243a-149">The **DisplayMethodAccess** helper function receives a DWORD value that contains the method's access options.</span></span> <span data-ttu-id="f243a-150">Questo valore viene confrontato con \_ il comando WPD \_ Access \_ Read e WPD \_ Command \_ Access \_ ReadWrite per determinare il privilegio di accesso del metodo.</span><span class="sxs-lookup"><span data-stu-id="f243a-150">It compares this value to WPD\_COMMAND\_ACCESS\_READ and WPD\_COMMAND\_ACCESS\_READWRITE to determine the method's access privilege.</span></span> <span data-ttu-id="f243a-151">Usando il risultato, viene eseguito il rendering di una stringa che indica la restrizione di accesso per il metodo specificato.</span><span class="sxs-lookup"><span data-stu-id="f243a-151">Using the result, it renders a string indicating the access restriction for the given method.</span></span>

<span data-ttu-id="f243a-152">Il codice seguente usa la funzione di supporto **DisplayMethodAccess** .</span><span class="sxs-lookup"><span data-stu-id="f243a-152">The following code uses the **DisplayMethodAccess** helper function.</span></span>


```C++
void DisplayMethodAccess(
    DWORD   dwAccess)
{
    switch(static_cast<WPD_COMMAND_ACCESS_TYPES>(dwAccess))
    {
        case WPD_COMMAND_ACCESS_READ:
            printf("Read");
            break;
            
        case WPD_COMMAND_ACCESS_READWRITE:
            printf("Read/Write");
            break;

        default:
            printf("Unknown Access");
            break;
    }
}
```



<span data-ttu-id="f243a-153">La funzione helper **DisplayMethod** riceve un oggetto [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) e il GUID del metodo come parametri.</span><span class="sxs-lookup"><span data-stu-id="f243a-153">The **DisplayMethod** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object and the method's GUID as parameters.</span></span> <span data-ttu-id="f243a-154">Utilizzando l'oggetto **IPortableDeviceServiceCapabilities** , viene richiamato il metodo [**IPortableDeviceServiceCapabilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) per recuperare gli attributi del metodo ed eseguirne il rendering nella finestra della console dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f243a-154">Using the **IPortableDeviceServiceCapabilities** object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method to retrieve the method attributes and render them in the application's console window.</span></span>

<span data-ttu-id="f243a-155">La funzione helper **DisplayMethodParameters** riceve un oggetto [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) , il GUID del metodo e un oggetto IPortableDeviceKeyCollection che contiene i parametri del metodo.</span><span class="sxs-lookup"><span data-stu-id="f243a-155">The **DisplayMethodParameters** helper function receives an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) object, the method's GUID, and an IPortableDeviceKeyCollection object containing the method parameters.</span></span> <span data-ttu-id="f243a-156">Utilizzando l'oggetto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) , viene richiamato il metodo [**IPortableDeviceServiceCapabilities:: GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) per recuperare il nome del parametro, l'utilizzo, il VarType e il form.</span><span class="sxs-lookup"><span data-stu-id="f243a-156">Using the [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) object, it invokes the [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) method to retrieve the parameter's name, usage, VARTYPE, and form.</span></span> <span data-ttu-id="f243a-157">Esegue il rendering di queste informazioni nella finestra della console dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f243a-157">It renders this information in the application's console window.</span></span>

<span data-ttu-id="f243a-158">Il codice seguente usa la funzione di supporto **DisplayMethodParameters** .</span><span class="sxs-lookup"><span data-stu-id="f243a-158">The following code uses the **DisplayMethodParameters** helper function.</span></span>


```C++
// Display the method parameters.
void DisplayMethodParameters(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method,
    IPortableDeviceKeyCollection*       pParameters)
{
    DWORD   dwNumParameters = 0;

    // Get the number of parameters for this event.
    HRESULT hr = pParameters->GetCount(&dwNumParameters);
    if (FAILED(hr))
    {
        printf("! Failed to get number of parameters, hr = 0x%lx\n",hr);
    }

    printf("\n\t%d Method Parameters:\n", dwNumParameters);

    // Loop through each parameter and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumParameters; dwIndex++)
        {
            PROPERTYKEY parameter;
            hr = pParameters->GetAt(dwIndex, &parameter);

            if (SUCCEEDED(hr))
            {
                CComPtr<IPortableDeviceValues> pAttributes;

                // Display the parameter's Name, Usage, Vartype, and Form
                hr = pCapabilities->GetMethodParameterAttributes(Method, parameter, &pAttributes);
                if (FAILED(hr))
                {
                    printf("! Failed to get the method parameter attributes, hr = 0x%lx\n",hr);
                }

                if (SUCCEEDED(hr))
                {
                    PWSTR   pszParameterName    = NULL;
                    DWORD   dwAttributeVarType  = 0;
                    DWORD   dwAttributeForm     = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                    DWORD   dwAttributeUsage    = (DWORD)-1;

                    hr = pAttributes->GetStringValue(WPD_PARAMETER_ATTRIBUTE_NAME, &pszParameterName);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tName: %ws\n", pszParameterName);
                    }
                    else
                    {
                        printf("! Failed to get the method parameter name, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_USAGE value, if specified. 
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_USAGE, &dwAttributeUsage);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tUsage: ");
                        DisplayParameterUsage(dwAttributeUsage);
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter usage, hr = 0x%lx\n",hr);
                    }

                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_VARTYPE, &dwAttributeVarType);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tVARTYPE: ");
                        DisplayVarType(static_cast<VARTYPE>(dwAttributeVarType));
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter VARTYPE, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_FORM value.
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_FORM, &dwAttributeForm);
                    if (FAILED(hr))
                    {
                        // If the read fails, assume WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED
                        dwAttributeForm = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                        hr = S_OK;
                    }

                    printf("\t\tForm: ");
                    DisplayParameterForm(dwAttributeForm);
                    printf("\n");

                    CoTaskMemFree(pszParameterName);
                    pszParameterName = NULL;
                }
                
                printf("\n");
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="f243a-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f243a-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f243a-160">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="f243a-160">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="f243a-161">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="f243a-161">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="f243a-162">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f243a-162">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="f243a-163">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f243a-163">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f243a-164">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="f243a-164">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



