---
description: Recupero degli eventi supportati da un dispositivo
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: Recupero degli eventi supportati da un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a542a34d0938c7e2ff86118818714f18b1224f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530252"
---
# <a name="retrieving-the-events-supported-by-a-device"></a>Recupero degli eventi supportati da un dispositivo

Alcuni driver WPD supportano la notifica degli eventi. Ciò significa che un'applicazione può eseguire la registrazione con il driver per ricevere una notifica quando si verifica un'azione specifica. Ad esempio, un'applicazione può registrarsi per ricevere una notifica quando un oggetto viene aggiunto o rimosso.

Sono disponibili dieci eventi predefiniti che possono essere monitorati da un'applicazione. descritti nella tabella seguente.



| Event                       | Descrizione                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Funzionalità del dispositivo aggiornate | Si verifica quando le funzionalità del dispositivo sono state modificate.                                                                                      |
| Dispositivo rimosso              | Si verifica quando il dispositivo viene scollegato.                                                                                                   |
| Reimpostazione del dispositivo                | Si verifica quando il dispositivo è stato reimpostato.                                                                                                 |
| Oggetto aggiunto                | Si verifica dopo che un nuovo oggetto diventa disponibile nel dispositivo.                                                                             |
| Oggetto rimosso              | Si verifica dopo che un oggetto è stato rimosso dal dispositivo.                                                                               |
| Trasferimento oggetti richiesto   | Indica che è stata effettuata una richiesta di trasferimento di un oggetto.                                                                          |
| Oggetto aggiornato              | Si verifica dopo l'aggiornamento di un oggetto o dei relativi elementi figlio. (I client connessi devono aggiornare la visualizzazione dell'oggetto specificato). |
| Formato di archiviazione in corso  | Si verifica quando viene formattata l'archiviazione del dispositivo.                                                                                     |



 

Per un elenco delle costanti associate a questi eventi, vedere l'argomento relativo alle [costanti di evento](event-constants.md) .

La funzione ListSupportedEvents nel modulo DeviceCapabilities. cpp illustra il recupero degli eventi supportati da un determinato dispositivo.

L'applicazione può recuperare gli identificatori per gli eventi supportati da un dispositivo usando le interfacce descritte nella tabella seguente.



| Interfaccia                                                                                      | Descrizione                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [**Interfaccia IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fornisce l'accesso ai metodi di recupero degli eventi supportati. |
| [**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Utilizzato per enumerare e archiviare i dati della categoria funzionale.     |



 

La prima attività eseguita dall'applicazione di esempio è il recupero di un oggetto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , che viene usato per recuperare gli eventi supportati dal dispositivo specificato.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pEvents;
DWORD dwNumEvents = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}
```



Gli eventi supportati vengono recuperati chiamando il metodo [**IPortableDeviceCapabilities:: GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) . Questo metodo recupera una raccolta di identificatori di evento per il dispositivo specificato e li archivia in un oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) a cui punta l'argomento pEvents.


```C++
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetSupportedEvents(&pEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get supported events from the device, hr = 0x%lx\n",hr);
    }
}
```



Il passaggio successivo consiste nel recuperare il conteggio degli eventi supportati in modo che l'applicazione possa scorrere l'oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) e recuperare l'identificatore per ogni.


```C++
if (SUCCEEDED(hr))
{
    hr = pEvents->GetCount(&dwNumEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Supported Events Found on the device\n\n", dwNumEvents);

// Loop through each event and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pEvents->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have an event.  It is assumed that
            // events are returned as VT_CLSID VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the event name
                DisplayEvent(*pv.puuid);
                printf("\n");
                // Display the event options
                DisplayEventOptions(pCapabilities, *pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti evento**](event-constants.md)
</dt> <dt>

[**Interfaccia IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaccia IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 



