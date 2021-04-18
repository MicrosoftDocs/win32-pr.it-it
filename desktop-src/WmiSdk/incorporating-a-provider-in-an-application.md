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
# <a name="incorporating-a-provider-in-an-application"></a><span data-ttu-id="7e15e-104">Incorporamento di un provider in un'applicazione</span><span class="sxs-lookup"><span data-stu-id="7e15e-104">Incorporating a Provider in an Application</span></span>

<span data-ttu-id="7e15e-105">Quando si crea un'applicazione da instrumentare, la procedura consigliata consiste nell'includere il provider come componente all'interno dell'applicazione stessa.</span><span class="sxs-lookup"><span data-stu-id="7e15e-105">When creating an application that is to be instrumented, the best practice is to include the provider as a component within the application itself.</span></span> <span data-ttu-id="7e15e-106">Questa pratica consente a Strumentazione gestione Windows (WMI) di interagire direttamente con il provider di servizi anziché indirettamente tramite l'API del programma.</span><span class="sxs-lookup"><span data-stu-id="7e15e-106">This practice permits Windows Management Instrumentation (WMI) to interact with the service provider directly instead of indirectly through the program API.</span></span> <span data-ttu-id="7e15e-107">Il disaccoppiamento del provider da WMI consente inoltre all'applicazione di controllare la durata del provider, invece di WMI.</span><span class="sxs-lookup"><span data-stu-id="7e15e-107">Decoupling the provider from WMI also puts the application in control of the provider lifespan, instead of WMI.</span></span> <span data-ttu-id="7e15e-108">Per ulteriori informazioni sulla scrittura di un provider in esecuzione nel processo WMI, vedere la pagina relativa [alla fornitura di dati a WMI mediante la scrittura di un provider](supplying-data-to-wmi-by-writing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7e15e-108">For more information about writing a provider that runs in the WMI process, see [Supplying Data to WMI by Writing a Provider](supplying-data-to-wmi-by-writing-a-provider.md).</span></span> <span data-ttu-id="7e15e-109">Per ulteriori informazioni sul modello di hosting e le impostazioni di sicurezza per il provider, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="7e15e-109">For more information about hosting model and security settings for the provider, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="7e15e-110">Il diagramma seguente illustra la relazione tra WMI, un provider disaccoppiato e un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e15e-110">The following diagram illustrates the relationship between WMI, a decoupled provider, and an application.</span></span>

![relazione tra WMI, provider disaccoppiato e applicazione](images/decoupledprov.png)

<span data-ttu-id="7e15e-112">Per ulteriori informazioni sui metodi del provider disaccoppiati, vedere [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) e [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).</span><span class="sxs-lookup"><span data-stu-id="7e15e-112">For more information about decoupled provider methods, see [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) and [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).</span></span>

> [!Note]  
> <span data-ttu-id="7e15e-113">Il provider disaccoppiato supporta l'istanza, il metodo, i provider di eventi e i consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="7e15e-113">The decoupled provider supports instance, method, event providers, and event consumers.</span></span> <span data-ttu-id="7e15e-114">Non supporta i provider di classi e proprietà.</span><span class="sxs-lookup"><span data-stu-id="7e15e-114">It does not support class and property providers.</span></span> <span data-ttu-id="7e15e-115">Per ulteriori informazioni, vedere [scrittura di un provider di classi](writing-a-class-provider.md) e [scrittura di un provider di proprietà](writing-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7e15e-115">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Property Provider](writing-a-property-provider.md).</span></span>

 

<span data-ttu-id="7e15e-116">Negli esempi di codice di questo argomento sono necessari i riferimenti seguenti e le \# istruzioni di inclusione per la compilazione corretta.</span><span class="sxs-lookup"><span data-stu-id="7e15e-116">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="7e15e-117">La procedura seguente usa esempi di codice C++ per descrivere come incorporare un provider disaccoppiato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e15e-117">The following procedure uses C++ code examples to describe how to incorporate a decoupled provider in your application.</span></span> <span data-ttu-id="7e15e-118">Il metodo di inizializzazione dell'applicazione esegue i passaggi seguenti in modo che WMI interagisce solo con un provider disaccoppiato registrato.</span><span class="sxs-lookup"><span data-stu-id="7e15e-118">The initialization method of the application performs the following steps so that WMI only interacts with a registered decoupled provider.</span></span>

<span data-ttu-id="7e15e-119">**Per implementare un provider disaccoppiato in un'applicazione C++**</span><span class="sxs-lookup"><span data-stu-id="7e15e-119">**To implement a decoupled provider in a C++ application**</span></span>

1.  <span data-ttu-id="7e15e-120">Inizializza la libreria COM per l'uso da parte del thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="7e15e-120">Initialize the COM library for use by the calling thread.</span></span>

    <span data-ttu-id="7e15e-121">Nell'esempio di codice riportato di seguito viene illustrato come inizializzare la libreria COM.</span><span class="sxs-lookup"><span data-stu-id="7e15e-121">The following code example shows how to initialize the COM library.</span></span>

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  <span data-ttu-id="7e15e-122">Imposta il livello di sicurezza del processo predefinito.</span><span class="sxs-lookup"><span data-stu-id="7e15e-122">Set the default process security level.</span></span>

    <span data-ttu-id="7e15e-123">Questo livello stabilisce il livello di sicurezza necessario per l'accesso alle informazioni del processo client da parte di altri processi.</span><span class="sxs-lookup"><span data-stu-id="7e15e-123">This level establishes the security level required of other processes to access the client process' information.</span></span> <span data-ttu-id="7e15e-124">Il livello di autenticazione deve essere \_ il \_ valore predefinito del livello auth C di RPC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7e15e-124">The authentication level should be RPC\_C\_AUTHN\_LEVEL\_DEFAULT.</span></span> <span data-ttu-id="7e15e-125">Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="7e15e-125">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="7e15e-126">Nell'esempio di codice riportato di seguito viene illustrato come impostare il livello di sicurezza predefinito.</span><span class="sxs-lookup"><span data-stu-id="7e15e-126">The following code example shows how to set the default security level.</span></span>

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

    

3.  <span data-ttu-id="7e15e-127">Registrare il registrar del provider disaccoppiato.</span><span class="sxs-lookup"><span data-stu-id="7e15e-127">Register the decoupled provider registrar.</span></span>

    <span data-ttu-id="7e15e-128">Nell'esempio di codice seguente viene illustrato come registrare il registrar del provider disaccoppiato.</span><span class="sxs-lookup"><span data-stu-id="7e15e-128">The following code example shows how to register the decoupled provider registrar.</span></span>

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

    

4.  <span data-ttu-id="7e15e-129">Registrare il provider di eventi disaccoppiato.</span><span class="sxs-lookup"><span data-stu-id="7e15e-129">Register the decoupled event provider.</span></span>

    <span data-ttu-id="7e15e-130">Nell'esempio di codice seguente viene illustrato come registrare il provider di eventi disaccoppiato.</span><span class="sxs-lookup"><span data-stu-id="7e15e-130">The following code example shows how to register the decoupled event provider.</span></span>

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

    

5.  <span data-ttu-id="7e15e-131">Eseguire le [chiamate a WMI](making-calls-to-wmi.md) richieste dalla funzionalità del provider.</span><span class="sxs-lookup"><span data-stu-id="7e15e-131">Make the [calls to WMI](making-calls-to-wmi.md) required by the provider's functionality.</span></span> <span data-ttu-id="7e15e-132">Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="7e15e-132">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span> <span data-ttu-id="7e15e-133">Per ulteriori informazioni se il provider servizi una richiesta di dati da uno script o un'applicazione, vedere [rappresentazione di un client](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="7e15e-133">For more information if the provider services a request for data from a script or application, see [Impersonating a Client](impersonating-a-client.md).</span></span>

<span data-ttu-id="7e15e-134">Appena prima della terminazione, l'applicazione deve eseguire la pulizia dopo se stessa.</span><span class="sxs-lookup"><span data-stu-id="7e15e-134">Just prior to terminating, the application must clean up after itself.</span></span> <span data-ttu-id="7e15e-135">Nella procedura seguente viene descritto come annullare la registrazione del provider disaccoppiato in modo che WMI non tenti di eseguire query per ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="7e15e-135">The following procedure describes how to unregister the decoupled provider so that WMI does not attempt to query it for information.</span></span>

<span data-ttu-id="7e15e-136">Nella procedura seguente viene descritto come annullare la registrazione del provider disaccoppiato.</span><span class="sxs-lookup"><span data-stu-id="7e15e-136">The following procedure describes how to unregister the decoupled provider.</span></span>

<span data-ttu-id="7e15e-137">**Per annullare la registrazione del provider disaccoppiato**</span><span class="sxs-lookup"><span data-stu-id="7e15e-137">**To unregister the decoupled provider**</span></span>

1.  <span data-ttu-id="7e15e-138">Annullare la registrazione e rilasciare il registrar.</span><span class="sxs-lookup"><span data-stu-id="7e15e-138">Unregister and release the registrar.</span></span>

    <span data-ttu-id="7e15e-139">Nell'esempio di codice seguente viene illustrato come annullare la registrazione e rilasciare il registrar.</span><span class="sxs-lookup"><span data-stu-id="7e15e-139">The following code example shows how to unregister and release the registrar.</span></span>

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  <span data-ttu-id="7e15e-140">Annullare la registrazione e rilasciare il provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="7e15e-140">Unregister and release the event provider.</span></span>

    <span data-ttu-id="7e15e-141">Nell'esempio di codice seguente viene illustrato come annullare la registrazione e rilasciare il provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="7e15e-141">The following code example shows how to unregister and release the event provider.</span></span>

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  <span data-ttu-id="7e15e-142">Pulire il server COM.</span><span class="sxs-lookup"><span data-stu-id="7e15e-142">Clean up the COM server.</span></span>

    <span data-ttu-id="7e15e-143">Nell'esempio di codice seguente viene illustrato come annullare l'inizializzazione della libreria COM.</span><span class="sxs-lookup"><span data-stu-id="7e15e-143">The following code example shows how to uninitialize the COM library.</span></span>

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a><span data-ttu-id="7e15e-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e15e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e15e-145">Impostazione di descrittori di sicurezza spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7e15e-145">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="7e15e-146">Sicurezza del provider</span><span class="sxs-lookup"><span data-stu-id="7e15e-146">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="7e15e-147">Sviluppo di un provider WMI</span><span class="sxs-lookup"><span data-stu-id="7e15e-147">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> </dl>

 

 



