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
# <a name="retrieving-a-sensor-object"></a>Recupero di un oggetto Sensor

Per recuperare un oggetto Sensor, usare l'interfaccia [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) . È possibile considerare questa interfaccia come l'interfaccia radice per l'API del sensore. Per usare **ISensorManager**, è prima necessario chiamare il metodo com **CoCreateInstance** .

Il codice di esempio seguente crea un'istanza di gestione sensori.


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



Dopo aver recuperato un puntatore a [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager), è possibile recuperare i sensori per categoria, tipo o ID. Se si recuperano i sensori per tipo o categoria, si riceve un puntatore a un'interfaccia [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) che contiene tutti i sensori disponibili che appartengono alla categoria o al tipo richiesto. Se si recupera un sensore in base al relativo ID, si riceve un puntatore a un'interfaccia [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) che rappresenta il sensore univoco richiesto.

Il codice di esempio seguente recupera una raccolta di sensori che appartengono alla categoria denominata SAMPLE \_ Sensor \_ Category \_ data \_ time. Il codice recupera quindi il primo sensore della raccolta in base al relativo indice.


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



Si noti che è possibile recuperare tutti i sensori disponibili usando SENSOR \_ Category \_ all.

In modo analogo, è possibile recuperare sensori di un determinato tipo.

Nell'esempio di codice riportato di seguito viene recuperato un insieme di sensori del tipo denominato tempo del tipo di sensore di esempio \_ \_ \_ . Il codice recupera quindi il primo sensore della raccolta in base al relativo indice.


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



Per recuperare un sensore in base al relativo ID, è necessario conoscerne l'ID univoco. I sensori generano in genere questo ID alla prima connessione per consentire di identificare più sensori della stessa marca e modello. Ciò significa che probabilmente l'ID del sensore non sarà noto in anticipo. Tuttavia, se è stata archiviata una copia di un ID sensore specifico recuperato in precedenza, ad esempio chiamando [**ISensor:: GetId**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), potrebbe essere necessario recuperare di nuovo lo stesso sensore.

Il codice di esempio seguente mostra come recuperare un sensore usando il relativo ID.


```C++
ISensor* pSensor = NULL;

// Get the sensor collection.
hr = pSensorManager->GetSensorByID(SAMPLE_SENSOR_TIME_ID, &pSensor);

```



È anche possibile recuperare i sensori quando diventano disponibili ricevendo un evento da Gestione sensori. Per ulteriori informazioni, vedere [**ISensorManager:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ISensorManagerEvents::OnSensorEnter**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter)
</dt> </dl>

 

 
