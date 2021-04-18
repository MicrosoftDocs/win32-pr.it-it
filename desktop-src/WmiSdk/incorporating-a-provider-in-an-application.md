---
description: Viene descritto come includere il provider COM WMI come componente all'interno di un'applicazione anziché in-process in WMI. Detto provider disaccoppiato, questo è il tipo consigliato di provider COM WMI da creare per i sistemi operativi Windows 2000 e versioni successive.
ms.assetid: a502f0dd-9add-4ebd-bc25-743a55eb78ac
ms.tgt_platform: multiple
title: Incorporamento di un provider in un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb544cd3b04cc75cef026bb2e4d2e579b8dbf135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568973"
---
# <a name="incorporating-a-provider-in-an-application"></a>Incorporamento di un provider in un'applicazione

Quando si crea un'applicazione da instrumentare, la procedura consigliata consiste nell'includere il provider come componente all'interno dell'applicazione stessa. Questa pratica consente a Strumentazione gestione Windows (WMI) di interagire direttamente con il provider di servizi anziché indirettamente tramite l'API del programma. Il disaccoppiamento del provider da WMI consente inoltre all'applicazione di controllare la durata del provider, invece di WMI. Per ulteriori informazioni sulla scrittura di un provider in esecuzione nel processo WMI, vedere la pagina relativa [alla fornitura di dati a WMI mediante la scrittura di un provider](supplying-data-to-wmi-by-writing-a-provider.md). Per ulteriori informazioni sul modello di hosting e le impostazioni di sicurezza per il provider, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).

Il diagramma seguente illustra la relazione tra WMI, un provider disaccoppiato e un'applicazione.

![relazione tra WMI, provider disaccoppiato e applicazione](images/decoupledprov.png)

Per ulteriori informazioni sui metodi del provider disaccoppiati, vedere [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) e [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).

> [!Note]  
> Il provider disaccoppiato supporta l'istanza, il metodo, i provider di eventi e i consumer di eventi. Non supporta i provider di classi e proprietà. Per ulteriori informazioni, vedere [scrittura di un provider di classi](writing-a-class-provider.md) e [scrittura di un provider di proprietà](writing-a-property-provider.md).

 

Negli esempi di codice di questo argomento sono necessari i riferimenti seguenti e le \# istruzioni di inclusione per la compilazione corretta.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



La procedura seguente usa esempi di codice C++ per descrivere come incorporare un provider disaccoppiato nell'applicazione. Il metodo di inizializzazione dell'applicazione esegue i passaggi seguenti in modo che WMI interagisce solo con un provider disaccoppiato registrato.

**Per implementare un provider disaccoppiato in un'applicazione C++**

1.  Inizializza la libreria COM per l'uso da parte del thread chiamante.

    Nell'esempio di codice riportato di seguito viene illustrato come inizializzare la libreria COM.

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  Imposta il livello di sicurezza del processo predefinito.

    Questo livello stabilisce il livello di sicurezza necessario per l'accesso alle informazioni del processo client da parte di altri processi. Il livello di autenticazione deve essere \_ il \_ valore predefinito del livello auth C di RPC \_ \_ . Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).

    Nell'esempio di codice riportato di seguito viene illustrato come impostare il livello di sicurezza predefinito.

    ```C++
    hr = CoInitializeSecurity (NULL, 
        -1, 
        NULL, 
        NULL,
        RPC_C_AUTHN_LEVEL_DEFAULT,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, 
        EOAC_DYNAMIC_CLOAKING, 
        NULL);

    if (FAILED(hr))
    {
      CoUninitialize();
      cout << "Failed to initialize security. Error code = 0x"
           << hex << hr << endl;
      return;
    }
    ```

    

3.  Registrare il registrar del provider disaccoppiato.

    Nell'esempio di codice seguente viene illustrato come registrare il registrar del provider disaccoppiato.

    ```C++
    CLSID CLSID_WbemDecoupledRegistrar;
    IID IID_IWbemDecoupledRegistrar;
    IWbemDecoupledRegistrar *myRegistrar = NULL;

    hr = CoCreateInstance(CLSID_WbemDecoupledRegistrar,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledRegistrar,
                          (void**)&myRegistrar);
    if (SUCCEEDED(hr))
    {
        IUnknown *pIUnknown = NULL;
        // CMyProv is the class added for WMI instance / event provider
        HRESULT hr = CMyProv::CreateInstance(NULL,&pIUnknown);
        if ( SUCCEEDED(hr))
        {
            hr = myRegistrar->Register(0,
                NULL,
                NULL,
                NULL,
                L"root\\cimv2",
                L"DecoupledInstanceProvider",
                pIUnknown);

                pIUnknown->Release();
        }
    }

    if (FAILED (hr))
    {
        if ( myRegistrar )
        {
            myRegistrar->Release () ;
        }
    }
    ```

    

4.  Registrare il provider di eventi disaccoppiato.

    Nell'esempio di codice seguente viene illustrato come registrare il provider di eventi disaccoppiato.

    ```C++
    IWbemDecoupledBasicEventProvider *myEvtRegistrar;

    // -- Create an instance of IWbemDecoupledEventProvider
    hr = CoCreateInstance(CLSID_WbemDecoupledBasicEventProvider,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledBasicEventProvider,
                          (void**)&myEvtRegistrar);

    if (SUCCEEDED(hr))
    {
       // -- Register the DecoupledEventProvider
       hr = myEvtRegistrar->Register(0,
                                     NULL,
                                     NULL,
                                     L"root\\cimv2",
                                     L"DecoupledEventProvider",
                                     NULL, NULL);
       if (SUCCEEDED(hr))
       {
          IWbemServices *pService = NULL;
          hr = myEvtRegistrar->GetService (0, NULL, &pService);
          if (SUCCEEDED(hr))
          {
             IWbemObjectSink *pSink = NULL;
             hr = myEvtRegistrar->GetSink ( 0, NULL, &pSink );
             if (SUCCEEDED(hr))
             {
                // Provide events
             }
          }
       } 
    }
    ```

    

5.  Eseguire le [chiamate a WMI](making-calls-to-wmi.md) richieste dalla funzionalità del provider. Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md). Per ulteriori informazioni se il provider servizi una richiesta di dati da uno script o un'applicazione, vedere [rappresentazione di un client](impersonating-a-client.md).

Appena prima della terminazione, l'applicazione deve eseguire la pulizia dopo se stessa. Nella procedura seguente viene descritto come annullare la registrazione del provider disaccoppiato in modo che WMI non tenti di eseguire query per ottenere informazioni.

Nella procedura seguente viene descritto come annullare la registrazione del provider disaccoppiato.

**Per annullare la registrazione del provider disaccoppiato**

1.  Annullare la registrazione e rilasciare il registrar.

    Nell'esempio di codice seguente viene illustrato come annullare la registrazione e rilasciare il registrar.

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  Annullare la registrazione e rilasciare il provider di eventi.

    Nell'esempio di codice seguente viene illustrato come annullare la registrazione e rilasciare il provider di eventi.

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  Pulire il server COM.

    Nell'esempio di codice seguente viene illustrato come annullare l'inizializzazione della libreria COM.

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sicurezza del provider](securing-your-provider.md)
</dt> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> </dl>

 

 



