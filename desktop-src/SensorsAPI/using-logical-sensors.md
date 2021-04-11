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
# <a name="using-logical-sensors"></a>Uso di sensori logici

Per creare un'istanza di un nodo di dispositivo per un sensore logico o per riconnettersi a un nodo del dispositivo del sensore logico esistente, un'applicazione o un servizio deve chiamare [**ILogicalSensorManager:: Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)). Il parametro *pPropertyStore* per questo metodo richiede un puntatore a un'interfaccia [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) che contiene gli ID per i driver dei sensori a cui connettersi. Ciò significa che è necessario creare un archivio di proprietà e aggiungere questi dati all'archivio prima di chiamare questo metodo.

### <a name="connecting-to-the-logical-sensor"></a>Connessione al sensore logico

Per connettersi a un sensore logico, è necessario specificare almeno un ID hardware, come definito nel file inf del driver del sensore, e un **GUID** logico che identifichi il sensore. La piattaforma usa questo **GUID** per identificare il sensore quando si sceglie di disconnettere, o disinstallare, il nodo del dispositivo del sensore.

Il codice di esempio seguente crea un metodo helper che si connette a un sensore logico specificato. I parametri del metodo ricevono l'ID hardware del sensore e un **GUID** univoco per identificare il sensore.


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



### <a name="disconnecting-from-a-logical-sensor"></a>Disconnessione da un sensore logico

Per disconnettersi da un sensore logico, è necessario fornire lo stesso ID logico usato quando è stato chiamato [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).

Il codice di esempio seguente crea una funzione di supporto che si disconnette da un sensore logico.


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



### <a name="uninstalling-a-logical-sensor"></a>Disinstallazione di un sensore logico

Per disinstallare un sensore logico, è necessario fornire lo stesso ID logico usato quando è stato chiamato [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).

Il codice di esempio seguente crea una funzione di supporto che disinstalla un sensore logico.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui sensori logici](about-logical-sensors.md)
</dt> </dl>

 

 
