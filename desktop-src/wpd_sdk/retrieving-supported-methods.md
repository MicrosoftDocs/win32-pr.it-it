---
description: Recupero dei metodi di servizio supportati
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: Recupero dei metodi di servizio supportati
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce058fcab000a90459dcce5310645088b40a2432d1de8c9852c84770db058300
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839048"
---
# <a name="retrieving-supported-service-methods"></a>Recupero dei metodi di servizio supportati

I metodi del servizio incapsulano le funzionalità che ogni servizio definisce e implementa. Sono specifici di ogni tipo di servizio e sono rappresentati da un GUID univoco.

Ad esempio, il servizio Contatti definisce un metodo **BeginSync** chiamato dalle applicazioni per preparare il dispositivo per la sincronizzazione degli oggetti Contact e un metodo **EndSync** per notificare al dispositivo che la sincronizzazione è stata completata.

Le applicazioni possono eseguire query a livello di codice sui metodi supportati e accedere a questi metodi e ai relativi attributi usando [**l'interfaccia IPortableDeviceServiceCapabilities.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)

I metodi di servizio non devono essere confusi con i comandi WPD. I comandi WPD fanno parte dell'interfaccia DDI (Device Driver Interface) WPD standard e sono il meccanismo per la comunicazione tra un'applicazione WPD e il driver. I comandi sono predefiniti, raggruppati per categorie, ad esempio WPD CATEGORY COMMON, e sono \_ rappresentati da una struttura \_ PROPERTYKEY. Per altre informazioni, vedere [**l'argomento**](commands.md) Comandi.

L'applicazione WpdServicesApiSample include codice che illustra come un'applicazione può recuperare i metodi supportati da un determinato servizio Contatti usando le interfacce nella tabella seguente.



| Interfaccia      | Descrizione         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Usato per recuperare **l'interfaccia IPortableDeviceServiceCapabilities** per accedere ai metodi di servizio supportati. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Fornisce l'accesso ai metodi supportati, agli attributi dei metodi e ai parametri del metodo.                             |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contiene l'elenco dei metodi supportati.                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contiene gli attributi per un metodo e per i parametri di un determinato metodo.                                      |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Contiene i parametri per un determinato metodo.                                                                    |



 

Quando l'utente sceglie l'opzione "5" nella riga di comando, l'applicazione richiama il metodo **ListSupportedMethods** disponibile nel modulo ServiceMethods.cpp.

Si noti che prima di recuperare l'elenco di eventi, l'applicazione di esempio apre un servizio Contatti in un dispositivo connesso.

In WPD un metodo è descritto dal nome, dai diritti di accesso, dai parametri e dai dati correlati. L'applicazione di esempio visualizza un nome descrittivo, ad esempio "CustomMethod" o un GUID. Il nome del metodo o il GUID è seguito dai dati di accesso ("Lettura/Scrittura"), dal nome di qualsiasi formato associato e dai dati dei parametri. Questi dati includono il nome del parametro, l'utilizzo, VARTYPE e il modulo.

Cinque metodi nel modulo ServiceMethods.cpp supportano il recupero di metodi (e dati correlati) per il servizio Contatti specificato: **ListSupportedMethods,** **DisplayMethod,** **DisplayMethodAccess,** **DisplayFormat** e **DisplayMethodParameters.** Il **metodo ListSupportedMethods** recupera un conteggio dei metodi supportati e l'identificatore GUID per ognuno; chiama quindi il **metodo DisplayMethod.** Il **metodo DisplayMethod** chiama il metodo [**IPortableDeviceServiceCapapbilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) per recuperare le opzioni, i parametri e così via del metodo specificato. Dopo che **DisplayMethod** recupera i dati del metodo, esegue il rendering del nome (o GUID), delle restrizioni di accesso, del formato associato (se presente) e delle descrizioni dei parametri. **DisplayMethodAccess,** **DisplayFormat** e **DisplayMethodParameters** sono funzioni helper che eseguono il rendering dei rispettivi campi di dati.

Il **metodo ListSupportedMethods** richiama il [**metodo IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare [**un'interfaccia IPortableDeviceServiceCapabilities.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Usando questa interfaccia, recupera i metodi supportati chiamando il metodo [**IPortableDeviceServiceCapabilities::GetSupportedMethods.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) Il **metodo GetSupportedMethods** recupera i GUID per ogni metodo supportato dal servizio e copia tale GUID in un [**oggetto IPortableDevicePropVariantCollection.**](iportabledevicepropvariantcollection.md)

Il codice seguente usa il **metodo ListSupportedMethods.**


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



Dopo che **il metodo ListSupportedMethods** recupera il GUID per ogni evento supportato dal servizio specificato, richiama il **metodo DisplayMethod** per recuperare gli attributi specifici del metodo. Questi attributi includono: il nome descrittivo del metodo, le restrizioni di accesso necessarie, qualsiasi formato associato e l'elenco di parametri.

Il **metodo DisplayMethod** richiama il metodo [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) per recuperare una raccolta di attributi per il metodo specificato. Chiama quindi il [**metodo IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) per recuperare il nome del metodo. **DisplayMethod chiama** [**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) per recuperare le restrction di accesso. Successivamente, chiama [**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md) per recuperare qualsiasi formato associato. Infine, **DisplayMethod** chiama [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) per recuperare i dati dei parametri. Passa i dati restituiti da questi metodi alle funzioni helper **DisplayMethodAccess,** **DisplayFormat** e **DisplayMethodParameters,** che eseguono il rendering delle informazioni per il metodo specificato.

Il codice seguente usa il **metodo DisplayMethod.**


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



La funzione helper **DisplayMethodAccess** riceve un valore DWORD che contiene le opzioni di accesso del metodo. Confronta questo valore con WPD COMMAND ACCESS READ e \_ \_ \_ WPD COMMAND ACCESS READWRITE per \_ \_ \_ determinare il privilegio di accesso del metodo. Usando il risultato, viene eseguito il rendering di una stringa che indica la restrizione di accesso per il metodo specificato.

Il codice seguente usa la funzione helper **DisplayMethodAccess.**


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



La funzione helper **DisplayMethod** riceve un [**oggetto IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) e il GUID del metodo come parametri. Usando l'oggetto **IPortableDeviceServiceCapabilities,** richiama il metodo [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) per recuperare gli attributi del metodo ed eseguirne il rendering nella finestra della console dell'applicazione.

La funzione helper **DisplayMethodParameters** riceve un [**oggetto IPortableDeviceServiceCapabilities,**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) il GUID del metodo e un oggetto IPortableDeviceKeyCollection contenente i parametri del metodo. Usando l'oggetto [**IPortableDeviceKeyCollection,**](iportabledevicekeycollection.md) richiama il metodo [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) per recuperare il nome, l'utilizzo, VARTYPE e il form del parametro. Esegue il rendering di queste informazioni nella finestra della console dell'applicazione.

Il codice seguente usa la funzione helper **DisplayMethodParameters.**


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

 

 



