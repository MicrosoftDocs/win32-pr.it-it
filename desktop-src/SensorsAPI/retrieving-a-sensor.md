---
description: Per recuperare un oggetto Sensor, usare l'interfaccia ISensorManager. È possibile considerare questa interfaccia come l'interfaccia radice per l'API del sensore. Per usare ISensorManager, è prima necessario chiamare il metodo COM CoCreateInstance.
ms.assetid: 36631bae-f237-4951-9959-6ab6286bd1f7
title: Recupero di un oggetto Sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cda6ea04d1a0580c38aef5a0b9c4186b908300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966574"
---
# <a name="retrieving-a-sensor-object"></a><span data-ttu-id="08e73-105">Recupero di un oggetto Sensor</span><span class="sxs-lookup"><span data-stu-id="08e73-105">Retrieving a Sensor Object</span></span>

<span data-ttu-id="08e73-106">Per recuperare un oggetto Sensor, usare l'interfaccia [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) .</span><span class="sxs-lookup"><span data-stu-id="08e73-106">To retrieve a sensor object, you use the [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) interface.</span></span> <span data-ttu-id="08e73-107">È possibile considerare questa interfaccia come l'interfaccia radice per l'API del sensore.</span><span class="sxs-lookup"><span data-stu-id="08e73-107">You can think of this interface as the root interface for the Sensor API.</span></span> <span data-ttu-id="08e73-108">Per usare **ISensorManager**, è prima necessario chiamare il metodo com **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="08e73-108">To use **ISensorManager**, you must first call the COM **CoCreateInstance** method.</span></span>

<span data-ttu-id="08e73-109">Il codice di esempio seguente crea un'istanza di gestione sensori.</span><span class="sxs-lookup"><span data-stu-id="08e73-109">The following example code creates an instance of the sensor manager.</span></span>


```C++
// Create the sensor manager.
hr = CoCreateInstance(CLSID_SensorManager, 
                        NULL, CLSCTX_INPROC_SERVER,
                        IID_PPV_ARGS(&pSensorManager));

if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DISABLED_BY_POLICY))
{
    // Unable to retrieve sensor manager due to 
    // group policy settings. Alert the user.
}
```



<span data-ttu-id="08e73-110">Dopo aver recuperato un puntatore a [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager), è possibile recuperare i sensori per categoria, tipo o ID.</span><span class="sxs-lookup"><span data-stu-id="08e73-110">After successfully retrieving a pointer to [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager), you can retrieve sensors by category, type, or ID.</span></span> <span data-ttu-id="08e73-111">Se si recuperano i sensori per tipo o categoria, si riceve un puntatore a un'interfaccia [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) che contiene tutti i sensori disponibili che appartengono alla categoria o al tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="08e73-111">If you retrieve sensors by type or category, you receive a pointer to an [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) interface that contains all the available sensors that belong to the requested category or type.</span></span> <span data-ttu-id="08e73-112">Se si recupera un sensore in base al relativo ID, si riceve un puntatore a un'interfaccia [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) che rappresenta il sensore univoco richiesto.</span><span class="sxs-lookup"><span data-stu-id="08e73-112">If you retrieve a sensor by its ID, you receive a pointer to an [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface that represents the unique sensor you requested.</span></span>

<span data-ttu-id="08e73-113">Il codice di esempio seguente recupera una raccolta di sensori che appartengono alla categoria denominata SAMPLE \_ Sensor \_ Category \_ data \_ time.</span><span class="sxs-lookup"><span data-stu-id="08e73-113">The following example code retrieves a collection of sensors that belong to the category named SAMPLE\_SENSOR\_CATEGORY\_DATE\_TIME.</span></span> <span data-ttu-id="08e73-114">Il codice recupera quindi il primo sensore della raccolta in base al relativo indice.</span><span class="sxs-lookup"><span data-stu-id="08e73-114">The code then retrieves the first sensor in the collection by its index.</span></span>


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByCategory(SAMPLE_SENSOR_CATEGORY_DATE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested category.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



<span data-ttu-id="08e73-115">Si noti che è possibile recuperare tutti i sensori disponibili usando SENSOR \_ Category \_ all.</span><span class="sxs-lookup"><span data-stu-id="08e73-115">Note that you can retrieve all of the available sensors by using SENSOR\_CATEGORY\_ALL.</span></span>

<span data-ttu-id="08e73-116">In modo analogo, è possibile recuperare sensori di un determinato tipo.</span><span class="sxs-lookup"><span data-stu-id="08e73-116">In a similar way, you can retrieve sensors of a particular type.</span></span>

<span data-ttu-id="08e73-117">Nell'esempio di codice riportato di seguito viene recuperato un insieme di sensori del tipo denominato tempo del tipo di sensore di esempio \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="08e73-117">The following example code retrieves a collection of sensors of the type named SAMPLE\_SENSOR\_TYPE\_TIME.</span></span> <span data-ttu-id="08e73-118">Il codice recupera quindi il primo sensore della raccolta in base al relativo indice.</span><span class="sxs-lookup"><span data-stu-id="08e73-118">The code then retrieves the first sensor in the collection by its index.</span></span>


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested type.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



<span data-ttu-id="08e73-119">Per recuperare un sensore in base al relativo ID, è necessario conoscerne l'ID univoco.</span><span class="sxs-lookup"><span data-stu-id="08e73-119">To retrieve a sensor by its ID, you must know the unique ID for the sensor.</span></span> <span data-ttu-id="08e73-120">I sensori generano in genere questo ID alla prima connessione per consentire di identificare più sensori della stessa marca e modello.</span><span class="sxs-lookup"><span data-stu-id="08e73-120">Sensors usually generate this ID when first connected to enable you to identify multiple sensors of the same make and model.</span></span> <span data-ttu-id="08e73-121">Ciò significa che probabilmente l'ID del sensore non sarà noto in anticipo.</span><span class="sxs-lookup"><span data-stu-id="08e73-121">This means that you probably will not know the sensor ID in advance.</span></span> <span data-ttu-id="08e73-122">Tuttavia, se è stata archiviata una copia di un ID sensore specifico recuperato in precedenza, ad esempio chiamando [**ISensor:: GetId**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), potrebbe essere necessario recuperare di nuovo lo stesso sensore.</span><span class="sxs-lookup"><span data-stu-id="08e73-122">However, if you have stored a copy of a particular sensor ID that you previously retrieved, for example by calling [**ISensor::GetID**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), you may want to retrieve the same sensor again.</span></span>

<span data-ttu-id="08e73-123">Il codice di esempio seguente mostra come recuperare un sensore usando il relativo ID.</span><span class="sxs-lookup"><span data-stu-id="08e73-123">The following example code shows how to retrieve a sensor by using its ID.</span></span>


```C++
ISensor* pSensor = NULL;

// Get the sensor collection.
hr = pSensorManager->GetSensorByID(SAMPLE_SENSOR_TIME_ID, &pSensor);

```



<span data-ttu-id="08e73-124">È anche possibile recuperare i sensori quando diventano disponibili ricevendo un evento da Gestione sensori.</span><span class="sxs-lookup"><span data-stu-id="08e73-124">You can also retrieve sensors when they become available by receiving an event from the sensor manager.</span></span> <span data-ttu-id="08e73-125">Per ulteriori informazioni, vedere [**ISensorManager:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).</span><span class="sxs-lookup"><span data-stu-id="08e73-125">For more information, see [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="08e73-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08e73-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08e73-127">**ISensorManagerEvents::OnSensorEnter**</span><span class="sxs-lookup"><span data-stu-id="08e73-127">**ISensorManagerEvents::OnSensorEnter**</span></span>](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter)
</dt> </dl>

 

 
