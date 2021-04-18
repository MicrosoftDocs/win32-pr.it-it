---
description: Uso dei dati del sensore chiaro
ms.assetid: 98272df5-08c0-4392-a74b-2919bbdcb022
title: Uso dei dati del sensore chiaro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ccf1c032b4100174afd6073d8c43db27bce3892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316091"
---
# <a name="using-light-sensor-data"></a><span data-ttu-id="4fb0b-103">Uso dei dati del sensore chiaro</span><span class="sxs-lookup"><span data-stu-id="4fb0b-103">Using Light Sensor Data</span></span>

<span data-ttu-id="4fb0b-104">Sono disponibili due modi per interpretare e usare i dati di Lux che provengono dai sensori di luce di ambiente.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-104">There are two recommended ways of interpreting and using lux data that comes from ambient light sensors.</span></span>

-   <span data-ttu-id="4fb0b-105">Applicare una trasformazione ai dati in modo che il livello di luce normalizzato possa essere usato in proporzione diretta ai comportamenti o alle interazioni del programma.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-105">Apply a transform to the data so that the normalized light level can be used in direct proportion to program behaviors or interactions.</span></span> <span data-ttu-id="4fb0b-106">Un esempio potrebbe essere quello di variare la dimensione di un pulsante del programma in proporzione diretta ai dati normalizzati (o a un intervallo di dati normalizzati, ad esempio, corrispondenti all'esterno).</span><span class="sxs-lookup"><span data-stu-id="4fb0b-106">An example would be to vary the size of a button in your program in direct proportion to the normalized data (or a range of the normalized data, corresponding to outdoors, for example).</span></span> <span data-ttu-id="4fb0b-107">Questo approccio fornisce l'implementazione ottimale.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-107">This approach gives the optimal implementation.</span></span>
-   <span data-ttu-id="4fb0b-108">Gestire intervalli di dati Lux ed eseguire il mapping dei comportamenti e delle reazioni dei programmi alle soglie superiore e inferiore di questi intervalli di dati Lux.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-108">Deal with ranges of lux data, and map program behaviors and reactions to the upper and lower thresholds of these ranges of lux data.</span></span> <span data-ttu-id="4fb0b-109">Si tratta di un modo semplice per rispondere alle condizioni di illuminazione e potrebbe non produrre l'esperienza utente ottimale.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-109">This is a simple way to respond to lighting conditions and may not yield the optimal user experience.</span></span> <span data-ttu-id="4fb0b-110">Questo approccio, tuttavia, funziona correttamente se non è possibile eseguire transizioni senza problemi.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-110">However, this approach works fine if smooth transitions are not feasible.</span></span>

## <a name="handling-data-from-multiple-light-sensors"></a><span data-ttu-id="4fb0b-111">Gestione dei dati da più sensori leggeri</span><span class="sxs-lookup"><span data-stu-id="4fb0b-111">Handling Data from Multiple Light Sensors</span></span>

<span data-ttu-id="4fb0b-112">Per produrre l'approssimazione più accurata delle condizioni di illuminazione correnti, è possibile usare i dati di più sensori di luce di ambiente.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-112">To produce the most accurate approximation of the current lighting conditions, you can use data from multiple ambient light sensors.</span></span> <span data-ttu-id="4fb0b-113">Poiché i sensori di luce di ambiente possono essere parzialmente o completamente nascosti da ombre o oggetti che coprono il sensore, più sensori posizionati a distanza possono fornire un'approssimazione molto migliore delle condizioni di illuminazione correnti rispetto a un singolo sensore.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-113">Because ambient light sensors can be partly or fully obscured by shadows or objects that cover the sensor, multiple sensors placed some distance apart can provide a much better approximation of the current lighting conditions than a single sensor.</span></span>

<span data-ttu-id="4fb0b-114">Per tenere traccia dei dati provenienti da più sensori, è possibile usare le due tecniche seguenti:</span><span class="sxs-lookup"><span data-stu-id="4fb0b-114">To keep track of the data coming from multiple sensors, you can use the following two techniques:</span></span>

-   <span data-ttu-id="4fb0b-115">Il valore dei dati più recente per ogni sensore di luminosità ambientale può essere mantenuto, insieme al timestamp del report dati del sensore per ognuna di queste letture.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-115">The most recent data value for each ambient light sensor can be retained, along with the time stamp from the sensor data report for each of these readings.</span></span> <span data-ttu-id="4fb0b-116">L'ultimo [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) ricevuto per ogni lettura del sensore può essere mantenuto e può fornire entrambi i valori per un riferimento successivo.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-116">The last [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) received for each sensor reading could be retained and could provide both values for later reference.</span></span> <span data-ttu-id="4fb0b-117">Facendo riferimento al timestamp per ogni report sui dati dei sensori, i dati possono essere gestiti in base alla relativa età.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-117">By referring to the time stamp for each sensor data report, the data can be managed based on its age.</span></span> <span data-ttu-id="4fb0b-118">Se, ad esempio, i dati sono più vecchi di 2 secondi, è possibile ometterli.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-118">For example, if the data is more than 2 seconds old, it could be omitted.</span></span> <span data-ttu-id="4fb0b-119">In base ai valori più recenti dei dati del sensore, è possibile usare la lettura più elevata perché il sensore corrispondente verrebbe considerato non oscurato.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-119">Based on the newer sensor data values, the highest reading could be used because the corresponding sensor would be presumed not to be obscured.</span></span>
-   <span data-ttu-id="4fb0b-120">È possibile usare l'ultimo valore del sensore luce di ambiente segnalato.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-120">You can use the last ambient light sensor value reported.</span></span> <span data-ttu-id="4fb0b-121">Questa implementazione non è ottimale perché i valori di più sensori non vengono confrontati tra loro per ottenere il risultato più accurato.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-121">This implementation would not be optimal because the values from multiple sensors are not compared to one another to obtain the most accurate result.</span></span> <span data-ttu-id="4fb0b-122">Questo metodo non è consigliato.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-122">We do not recommend this method.</span></span>

## <a name="example-code"></a><span data-ttu-id="4fb0b-123">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="4fb0b-123">Example Code</span></span>

<span data-ttu-id="4fb0b-124">Nell'esempio di codice seguente viene illustrata un'implementazione per l'evento [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) .</span><span class="sxs-lookup"><span data-stu-id="4fb0b-124">The following example code shows an implementation for the [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) event.</span></span> <span data-ttu-id="4fb0b-125">Il gestore eventi chiama una funzione helper, denominata **UpdateUI**, che modifica l'interfaccia utente in base al valore Lux.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-125">The event handler calls a helper function, named **UpdateUI**, that changes the user interface based on the lux value.</span></span> <span data-ttu-id="4fb0b-126">La scrittura dell'implementazione di UpdateUI dipende dall'utente.</span><span class="sxs-lookup"><span data-stu-id="4fb0b-126">Writing the implementation of UpdateUI is up to you.</span></span>


```C++
// Override of ISensorEvents::OnDataUpdated
// Part of an event sink implementation for ISensorEvents
STDMETHODIMP CALSEventSink::OnDataUpdated(
    ISensor* pSensor, 
    ISensorDataReport* pNewData)
{
    HRESULT hr = S_OK;
   
    if(pSensor == NULL ||
       pNewData == NULL)
    {
         return E_POINTER;
    }

    // Declare and initialize the PROPVARIANT
    PROPVARIANT lightLevel;
    PropVariantInit(&lightLevel);

    // Get the sensor reading from the ISensorDataReport object
    hr = pNewData->GetSensorValue(
        SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX, 
        &lightLevel);

    if(SUCCEEDED(hr))
    {
        if(lightlevel.vt == VT_R4)
        {
            // Extract the float value from the PROPVARIANT object
            float luxValue = lightLevel.fltVal;

            // Normalize the light sensor data
            double lightNormalized = ::log10(luxValue) / 5.0;

            // Handle UI changes based on the normalized LUX data
            // which ranges from 0.0 - 1.0 for a lux range of 
            // 0 lux to 100,000 lux. 
            UpdateUI(lightNormalized);
        }
    }

    // Release the variant.     
    PropVariantClear(&lightLevel);

    return hr;
}
```



 

 
