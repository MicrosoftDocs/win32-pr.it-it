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
# <a name="retrieving-supported-service-methods"></a>Recupero di metodi di servizio supportati

I metodi di servizio incapsulano le funzionalità che ogni servizio definisce e implementa. Sono specifici di ogni tipo di servizio e sono rappresentati da un GUID univoco.

Il servizio contatti, ad esempio, definisce un metodo **BeginSync** che le applicazioni chiamano per preparare il dispositivo per la sincronizzazione degli oggetti contatto e un metodo **EndSync** per notificare al dispositivo che la sincronizzazione è stata completata.

Le applicazioni possono eseguire query a livello di codice sui metodi supportati e accedere a questi metodi e ai relativi attributi usando l'interfaccia [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .

I metodi del servizio non devono essere confusi con i comandi WPD. I comandi WPD fanno parte dell'interfaccia DDI (WPD Device Driver Interface) standard e sono il meccanismo per la comunicazione tra un'applicazione WPD e il driver. I comandi sono predefiniti, raggruppati per categorie, ad esempio, \_ la categoria WPD \_ comune e sono rappresentati da una struttura PropertyKey. Per ulteriori informazioni, vedere l'argomento [**Commands (comandi**](commands.md) ).

L'applicazione WpdServicesApiSample include codice che illustra come un'applicazione può recuperare i metodi supportati da un determinato servizio contatti usando le interfacce riportate nella tabella seguente.



|                                                                                      |                                                                                                                |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Interfaccia                                                                            | Descrizione                                                                                                    |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Utilizzato per recuperare l'interfaccia **IPortableDeviceServiceCapabilities** per accedere ai metodi del servizio supportati. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Fornisce l'accesso ai metodi supportati, agli attributi del metodo e ai parametri del metodo.                             |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contiene l'elenco dei metodi supportati.                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contiene gli attributi per un metodo e per i parametri di un metodo specificato.                                      |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Contiene i parametri per un determinato metodo.                                                                    |



 

Quando l'utente sceglie l'opzione "5" nella riga di comando, l'applicazione richiama il metodo **ListSupportedMethods** trovato nel modulo ServiceMethods. cpp.

Si noti che prima di recuperare l'elenco di eventi, l'applicazione di esempio apre un servizio contatti in un dispositivo connesso.

In WPD un metodo viene descritto in base al nome, ai diritti di accesso, ai parametri e ai dati correlati. Nell'applicazione di esempio viene visualizzato un nome descrittivo, ad esempio, "CustomMethod" o un GUID. Il nome o il GUID del metodo è seguito dai dati di accesso ("lettura/scrittura"), dal nome di qualsiasi formato associato e dai dati del parametro. Questi dati includono il nome del parametro, l'utilizzo, il VARTYPE e il form.

Cinque metodi del modulo ServiceMethods. cpp supportano il recupero di metodi (e dati correlati) per il servizio contatti specificato: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat** e **DisplayMethodParameters**. Il metodo **ListSupportedMethods** recupera un conteggio dei metodi supportati e l'identificatore GUID per ciascuna. chiama quindi il metodo **DisplayMethod** . Il metodo **DisplayMethod** chiama il metodo [**IPortableDeviceServiceCapapbilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) per recuperare le opzioni, i parametri e così via del metodo specificato. Dopo che **DisplayMethod** recupera i dati del metodo, esegue il rendering del nome (o del GUID), delle restrizioni di accesso, del formato associato (se presente) e delle descrizioni dei parametri. **DisplayMethodAccess**, **DisplayFormat** e **DisplayMethodParameters** sono funzioni helper che eseguono il rendering dei rispettivi campi di dati.

Il metodo **ListSupportedMethods** richiama il metodo [**IPortableDeviceService:: capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare un'interfaccia [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Utilizzando questa interfaccia, vengono recuperati i metodi supportati chiamando il metodo [**IPortableDeviceServiceCapabilities:: GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) . Il metodo **GetSupportedMethods** recupera i GUID per ogni metodo supportato dal servizio e copia il GUID in un oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .

Il codice seguente usa il metodo **ListSupportedMethods** .


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



Dopo che il metodo **ListSupportedMethods** Recupera il GUID per ogni evento supportato dal servizio specificato, richiama il metodo **DisplayMethod** per recuperare gli attributi specifici del metodo. Questi attributi includono: il nome descrittivo del metodo, le restrizioni di accesso necessarie, qualsiasi formato associato ed elenco di parametri.

Il metodo **DisplayMethod** richiama il metodo [**IPortableDeviceServiceCapabilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) per recuperare una raccolta di attributi per il metodo specificato. Chiama quindi il metodo [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) per recuperare il nome del metodo. **DisplayMethod** chiama [**IPortableDeviceValues:: GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) per recuperare il restrctions di accesso. Successivamente, viene chiamato [**IPortableDeviceValues:: GetGuidValue**](iportabledevicevalues-getguidvalue.md) per recuperare qualsiasi formato associato. Infine, **DisplayMethod** chiama [**IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) per recuperare i dati del parametro. Passa i dati restituiti da questi metodi alle funzioni di supporto **DisplayMethodAccess**, **DisplayFormat** e **DisplayMethodParameters** , che eseguono il rendering delle informazioni per il metodo specificato.

Il codice seguente usa il metodo **DisplayMethod** .


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



La funzione helper **DisplayMethodAccess** riceve un valore DWORD che contiene le opzioni di accesso del metodo. Questo valore viene confrontato con \_ il comando WPD \_ Access \_ Read e WPD \_ Command \_ Access \_ ReadWrite per determinare il privilegio di accesso del metodo. Usando il risultato, viene eseguito il rendering di una stringa che indica la restrizione di accesso per il metodo specificato.

Il codice seguente usa la funzione di supporto **DisplayMethodAccess** .


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



La funzione helper **DisplayMethod** riceve un oggetto [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) e il GUID del metodo come parametri. Utilizzando l'oggetto **IPortableDeviceServiceCapabilities** , viene richiamato il metodo [**IPortableDeviceServiceCapabilities:: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) per recuperare gli attributi del metodo ed eseguirne il rendering nella finestra della console dell'applicazione.

La funzione helper **DisplayMethodParameters** riceve un oggetto [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) , il GUID del metodo e un oggetto IPortableDeviceKeyCollection che contiene i parametri del metodo. Utilizzando l'oggetto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) , viene richiamato il metodo [**IPortableDeviceServiceCapabilities:: GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) per recuperare il nome del parametro, l'utilizzo, il VarType e il form. Esegue il rendering di queste informazioni nella finestra della console dell'applicazione.

Il codice seguente usa la funzione di supporto **DisplayMethodParameters** .


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



