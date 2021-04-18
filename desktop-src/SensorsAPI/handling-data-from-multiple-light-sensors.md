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
# <a name="using-light-sensor-data"></a>Uso dei dati del sensore chiaro

Sono disponibili due modi per interpretare e usare i dati di Lux che provengono dai sensori di luce di ambiente.

-   Applicare una trasformazione ai dati in modo che il livello di luce normalizzato possa essere usato in proporzione diretta ai comportamenti o alle interazioni del programma. Un esempio potrebbe essere quello di variare la dimensione di un pulsante del programma in proporzione diretta ai dati normalizzati (o a un intervallo di dati normalizzati, ad esempio, corrispondenti all'esterno). Questo approccio fornisce l'implementazione ottimale.
-   Gestire intervalli di dati Lux ed eseguire il mapping dei comportamenti e delle reazioni dei programmi alle soglie superiore e inferiore di questi intervalli di dati Lux. Si tratta di un modo semplice per rispondere alle condizioni di illuminazione e potrebbe non produrre l'esperienza utente ottimale. Questo approccio, tuttavia, funziona correttamente se non è possibile eseguire transizioni senza problemi.

## <a name="handling-data-from-multiple-light-sensors"></a>Gestione dei dati da più sensori leggeri

Per produrre l'approssimazione più accurata delle condizioni di illuminazione correnti, è possibile usare i dati di più sensori di luce di ambiente. Poiché i sensori di luce di ambiente possono essere parzialmente o completamente nascosti da ombre o oggetti che coprono il sensore, più sensori posizionati a distanza possono fornire un'approssimazione molto migliore delle condizioni di illuminazione correnti rispetto a un singolo sensore.

Per tenere traccia dei dati provenienti da più sensori, è possibile usare le due tecniche seguenti:

-   Il valore dei dati più recente per ogni sensore di luminosità ambientale può essere mantenuto, insieme al timestamp del report dati del sensore per ognuna di queste letture. L'ultimo [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) ricevuto per ogni lettura del sensore può essere mantenuto e può fornire entrambi i valori per un riferimento successivo. Facendo riferimento al timestamp per ogni report sui dati dei sensori, i dati possono essere gestiti in base alla relativa età. Se, ad esempio, i dati sono più vecchi di 2 secondi, è possibile ometterli. In base ai valori più recenti dei dati del sensore, è possibile usare la lettura più elevata perché il sensore corrispondente verrebbe considerato non oscurato.
-   È possibile usare l'ultimo valore del sensore luce di ambiente segnalato. Questa implementazione non è ottimale perché i valori di più sensori non vengono confrontati tra loro per ottenere il risultato più accurato. Questo metodo non è consigliato.

## <a name="example-code"></a>Codice di esempio

Nell'esempio di codice seguente viene illustrata un'implementazione per l'evento [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) . Il gestore eventi chiama una funzione helper, denominata **UpdateUI**, che modifica l'interfaccia utente in base al valore Lux. La scrittura dell'implementazione di UpdateUI dipende dall'utente.


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



 

 
