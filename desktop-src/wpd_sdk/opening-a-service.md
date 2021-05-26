---
description: Apertura di un servizio
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: Apertura di un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b273b8709a4d750085f14075d605f88ed0faa6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423921"
---
# <a name="opening-a-service"></a>Apertura di un servizio

Prima che l'applicazione possa eseguire operazioni su un servizio, ad esempio l'enumerazione del contenuto o il recupero di descrizioni di eventi o metodi supportati, è necessario aprire il servizio. Nell'applicazione WpdServicesApiSample questa attività viene illustrata nel modulo ServiceEnumeration.cpp usando le interfacce descritte nella tabella seguente.



| Interfaccia                                                              | Descrizione                                        |
|------------------------------------------------------------------------|----------------------------------------------------|
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | Usato per enumerare i servizi in un dispositivo.        |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Usato per aprire una connessione a un servizio del dispositivo.     |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | Usato per contenere le informazioni client dell'applicazione. |



 

Il metodo che apre un servizio è [**IPortableDeviceService::Open.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) Questo metodo accetta due argomenti: un identificatore Plug-and-Play (PnP) per il servizio e un [**oggetto IPortableDeviceValues**](iportabledevicevalues.md) che contiene le informazioni client dell'applicazione.

Per ottenere un identificatore PnP per un determinato servizio, l'applicazione chiama il [**metodo IPortableDeviceServiceManager::GetDeviceServices.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) Questo metodo recupera una matrice di identificatori PnP per i servizi di un GUID di categoria di servizi (ad esempio, contatti SERVICE).

L'applicazione di servizio di esempio recupera un identificatore PnP per i servizi Contatti all'interno del metodo **EnumerateContactsServices** nel modulo ServiceEnumeration.cpp. L'esempio di codice seguente è tratto da questo metodo.


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



Dopo che l'applicazione ha recuperato l'identificatore PnP per il servizio, può configurare le informazioni client e chiamare [**IPortableDeviceService::Open.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)

Nell'applicazione di esempio questo metodo viene chiamato all'interno **di ChooseDeviceService** nel modulo ServiceEnumeration.cpp.

[**IPortableDeviceService supporta**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) due CLSID per **CoCreateInstance.** **CLSID \_ PortableDeviceService restituisce** un **puntatore IPortableDeviceService** che non aggrega il gestore di marshalling a thread libero. **CLSID \_ PortableDeviceServiceFTM è** un nuovo CLSID che restituisce un **puntatore IPortableDeviceService** che aggrega il gestore di marshalling a thread libero. In caso contrario, entrambi i puntatori supportano la stessa funzionalità.

Le applicazioni che si trovano in apartment a thread singolo devono usare **CLSID \_ PortableDeviceServiceFTM,** in quanto questo elimina l'overhead del marshalling dei puntatori a interfaccia. **CLSID \_ PortableDeviceService è** ancora supportato per le applicazioni legacy.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**Interfaccia IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



