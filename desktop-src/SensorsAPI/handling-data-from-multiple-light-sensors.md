---
description: Uso dei dati dei sensori di luce
ms.assetid: 98272df5-08c0-4392-a74b-2919bbdcb022
title: Uso dei dati dei sensori di luce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae4f7047301c7d31d18014bb09512d1f3944c418a34c153a87c001f95fb63a8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425129"
---
# <a name="using-light-sensor-data"></a>Uso dei dati dei sensori di luce

Esistono due modi consigliati per interpretare e usare i dati provenienti da sensori di luce ambientale.

-   Applicare una trasformazione ai dati in modo che il livello di luce normalizzato possa essere usato in proporzione diretta ai comportamenti o alle interazioni del programma. Un esempio potrebbe essere la modifica delle dimensioni di un pulsante nel programma in proporzione diretta ai dati normalizzati (o a un intervallo di dati normalizzati, ad esempio corrispondenti agli ambienti esterni). Questo approccio offre un'implementazione ottimale.
-   Gestire gli intervalli di dati dei programmi, mappare i comportamenti e le reazioni del programma alle soglie superiori e inferiori di questi intervalli di dati. Si tratta di un modo semplice per rispondere alle condizioni di illuminazione e potrebbe non produrre un'esperienza utente ottimale. Questo approccio, tuttavia, funziona correttamente se non sono possibili transizioni uniformi.

## <a name="handling-data-from-multiple-light-sensors"></a>Gestione dei dati da più sensori di luce

Per produrre l'approssimazione più accurata delle condizioni di illuminazione correnti, è possibile usare i dati di più sensori di luce ambientale. Poiché i sensori di luce ambientale possono essere parzialmente o completamente nascosti da ombreggiature o oggetti che coprono il sensore, più sensori posizionati a una certa distanza possono fornire un'approssimazione molto migliore delle condizioni di illuminazione correnti rispetto a un singolo sensore.

Per tenere traccia dei dati provenienti da più sensori, è possibile usare le due tecniche seguenti:

-   È possibile conservare il valore dei dati più recenti per ogni sensore di luce ambientale, insieme al timestamp del report dei dati del sensore per ognuna di queste letture. [**L'ultimo ISensorDataReport ricevuto**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) per ogni lettura del sensore può essere mantenuto e può fornire entrambi i valori per riferimento successivo. Facendo riferimento al timestamp per ogni report dei dati del sensore, i dati possono essere gestiti in base all'età. Ad esempio, se i dati hanno più di 2 secondi, potrebbero essere omessi. In base ai valori dei dati del sensore più recente, è possibile usare la lettura più elevata perché si presume che il sensore corrispondente non sia nascosto.
-   È possibile usare l'ultimo valore del sensore di luce ambientale segnalato. Questa implementazione non sarebbe ottimale perché i valori di più sensori non vengono confrontati tra loro per ottenere il risultato più accurato. Questo metodo non è consigliato.

## <a name="example-code"></a>Codice di esempio

Il codice di esempio seguente illustra un'implementazione per [**l'evento OnDataUpdated.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) Il gestore eventi chiama una funzione helper, denominata **UpdateUI,** che modifica l'interfaccia utente in base al valore di . La scrittura dell'implementazione di UpdateUI è l'utente.


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



 

 
