---
description: Uso di sensori logici
ms.assetid: 97f4c44e-27dd-4f2a-b987-060bb2d9bc00
title: Uso di sensori logici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb0493cfe8ff3a489e926792f9a101eb5d9db6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128738"
---
# <a name="using-logical-sensors"></a><span data-ttu-id="fa8c8-103">Uso di sensori logici</span><span class="sxs-lookup"><span data-stu-id="fa8c8-103">Using Logical Sensors</span></span>

<span data-ttu-id="fa8c8-104">Per creare un'istanza di un nodo di dispositivo per un sensore logico o per riconnettersi a un nodo del dispositivo del sensore logico esistente, un'applicazione o un servizio deve chiamare [**ILogicalSensorManager:: Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fa8c8-104">To instantiate a device node for a logical sensor, or to reconnect to an existing logical sensor device node, an application or service must call [**ILogicalSensorManager::Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span> <span data-ttu-id="fa8c8-105">Il parametro *pPropertyStore* per questo metodo richiede un puntatore a un'interfaccia [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) che contiene gli ID per i driver dei sensori a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="fa8c8-105">The *pPropertyStore* parameter for this method requires a pointer to an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface that contains the IDs for the sensor drivers to connect to.</span></span> <span data-ttu-id="fa8c8-106">Ciò significa che è necessario creare un archivio di proprietà e aggiungere questi dati all'archivio prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fa8c8-106">This means that you must create a property store and add this data to the store before calling this method.</span></span>

### <a name="connecting-to-the-logical-sensor"></a><span data-ttu-id="fa8c8-107">Connessione al sensore logico</span><span class="sxs-lookup"><span data-stu-id="fa8c8-107">Connecting to the Logical Sensor</span></span>

<span data-ttu-id="fa8c8-108">Per connettersi a un sensore logico, è necessario specificare almeno un ID hardware, come definito nel file inf del driver del sensore, e un **GUID** logico che identifichi il sensore.</span><span class="sxs-lookup"><span data-stu-id="fa8c8-108">To connect to a logical sensor, you must provide, at a minimum, a hardware ID, as defined in the sensor driver's .inf file, and a logical **GUID** that identifies the sensor.</span></span> <span data-ttu-id="fa8c8-109">La piattaforma usa questo **GUID** per identificare il sensore quando si sceglie di disconnettere, o disinstallare, il nodo del dispositivo del sensore.</span><span class="sxs-lookup"><span data-stu-id="fa8c8-109">The platform uses this **GUID** to identify the sensor when you choose to disconnect from, or uninstall, the sensor device node.</span></span>

<span data-ttu-id="fa8c8-110">Il codice di esempio seguente crea un metodo helper che si connette a un sensore logico specificato.</span><span class="sxs-lookup"><span data-stu-id="fa8c8-110">The following example code creates a helper method that connects to a specified logical sensor.</span></span> <span data-ttu-id="fa8c8-111">I parametri del metodo ricevono l'ID hardware del sensore e un **GUID** univoco per identificare il sensore.</span><span class="sxs-lookup"><span data-stu-id="fa8c8-111">The method parameters receive the sensor hardware ID and a unique **GUID** to identify the sensor.</span></span>


```C++
HRESULT ConnectToLogicalSensor(PCWSTR* wszHardwareID, GUID guidLogicalID)
{
    HRESULT hr = S_OK;
    
    ILogicalSensorManager* pLSM = NULL;
    IPropertyStore* pStore = NULL;
    PROPVARIANT pv = {};

    // Create the property store.
    hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pStore));

    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    // Fill in the values.
    if(SUCCEEDED(hr))
    {
        hr = InitPropVariantFromStringVector(wszHardwareID, 1, &pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_HardwareIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_CompatibleIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        // Connect to the logical sensor.
        hr = pLSM->Connect(guidLogicalID, pStore);
    }

    SafeRelease(&pStore);
    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="disconnecting-from-a-logical-sensor"></a><span data-ttu-id="fa8c8-112">Disconnessione da un sensore logico</span><span class="sxs-lookup"><span data-stu-id="fa8c8-112">Disconnecting from a Logical Sensor</span></span>

<span data-ttu-id="fa8c8-113">Per disconnettersi da un sensore logico, è necessario fornire lo stesso ID logico usato quando è stato chiamato [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fa8c8-113">To disconnect from a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="fa8c8-114">Il codice di esempio seguente crea una funzione di supporto che si disconnette da un sensore logico.</span><span class="sxs-lookup"><span data-stu-id="fa8c8-114">The following example code creates a helper function that disconnects from a logical sensor.</span></span>


```C++
HRESULT DisconnectFromLogicalSensor(GUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM = NULL;
 
    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    if(SUCCEEDED(hr))
    {
        hr = pLSM->Disconnect(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="uninstalling-a-logical-sensor"></a><span data-ttu-id="fa8c8-115">Disinstallazione di un sensore logico</span><span class="sxs-lookup"><span data-stu-id="fa8c8-115">Uninstalling a Logical Sensor</span></span>

<span data-ttu-id="fa8c8-116">Per disinstallare un sensore logico, è necessario fornire lo stesso ID logico usato quando è stato chiamato [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fa8c8-116">To uninstall a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="fa8c8-117">Il codice di esempio seguente crea una funzione di supporto che disinstalla un sensore logico.</span><span class="sxs-lookup"><span data-stu-id="fa8c8-117">The following example code creates a helper function that uninstalls a logical sensor.</span></span>


```C++
HRESULT UninstallLogicalSensor(REFGUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM;
 
    // Create the logical sensor manager.
    hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_PPV_ARGS(&pLSM));
 
    if(SUCCEEDED(hr))
    {
        hr = pLSM->Uninstall(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="fa8c8-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa8c8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa8c8-119">Informazioni sui sensori logici</span><span class="sxs-lookup"><span data-stu-id="fa8c8-119">About Logical Sensors</span></span>](about-logical-sensors.md)
</dt> </dl>

 

 
