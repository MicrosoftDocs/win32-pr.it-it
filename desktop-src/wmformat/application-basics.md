---
title: Nozioni di base dell'applicazione
description: Nozioni di base dell'applicazione
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- Windows Sdk di formato multimediale, nozioni di base dell'applicazione DRM
- digital rights management (DRM), nozioni di base dell'applicazione
- DRM (digital rights management), nozioni di base dell'applicazione
- digital rights management (DRM), funzione WMDRMStartup
- DRM (digital rights management),funzione WMDRMStartup
- WMDRMStartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8356160565754764ac71cb152799a0fd9d1530e6e6969dc7a56e203b7504645d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086207"
---
# <a name="application-basics"></a>Nozioni di base dell'applicazione

È necessario eseguire un'ulteriore elaborazione per qualsiasi applicazione che usa le API estese Windows client DRM media. Questo argomento descrive i requisiti per una semplice applicazione.

Per prima cosa, è necessario inizializzare Windows API estese del client DRM multimediale chiamando la [**funzione WMDRMStartup.**](wmdrmstartup.md) Gli oggetti dell'SDK sono oggetti COM, ma non è necessario chiamare **CoIntialize**, perché la funzione **WMDRMStatup** inizializza AUTOMATICAMENTe COM.

> [!Note]  
> L Windows Media Format SDK usa solo un subset di COM, pertanto se si usano oggetti COM diversi da quelli nell'API estesa client di Windows Media DRM, è comunque necessario chiamare **CoInitialize**.

 

Tutti gli oggetti delle API estese Windows client DRM media vengono creati usando funzioni e metodi helper. Non è mai necessario chiamare **CoCreateInstance** per creare un oggetto. La prima interfaccia di cui creare un'istanza per qualsiasi applicazione che usa l'SDK è [**IWMDRMProvider,**](iwmdrmprovider.md)che è possibile usare per creare un'istanza di tutte le altre interfacce di base. Per ottenere un'istanza di **IWMDRMProvider,** è necessario chiamare [**WMDRMCreateProvider**](wmdrmcreateprovider.md) o [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md). La differenza tra queste funzioni è che **WMDRMCreateProvider** crea un oggetto che a sua volta può creare solo oggetti che non supportano metodi che richiedono la libreria stub.

Dopo aver creato un'istanza di **IWMDRMProvider,** è possibile creare gli altri oggetti necessari chiamando [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).

Quando si è pronti per uscire dall'applicazione, è necessario rilasciare le risorse del sottosistema DRM chiamando la funzione [**WMDRMShutdown.**](wmdrmshutdown.md) Questa funzione arresta anche COM automaticamente.

L'esempio di codice seguente illustra come inizializzare e concludere un'applicazione che usa le API estese del client DRM Windows media.


```C++
#include <wmdrmsdk.h>
// TODO: Include other headers here as needed.

// This example demonstrates the code required in a single, simple
// main function. You will most likely break this code up into appropriate
// functions.
void main(void)
{
    HRESULT hr = S_OK;

    IWMDRMProvider*     pProvider     = NULL;
    // For the sake of example, this code will instantiate the
    //  IWMDRMLicenseQuery interface. The process is the same for the
    //  other base interfaces.
    IWMDRMLicenseQuery* pLicenseQuery = NULL;

    // Initialize the DRM subsystem.
    hr = WMDRMStartup();

    // Create a provider object, that can be used to create the other
    //  objects.
    if (SUCCEEDED(hr))
    {
        hr = WMDRMCreateProvider(&pProvider);
    }

    if(SUCCEEDED(hr))
    {
        hr = pProvider->CreateObject(
            IID_IWMDRMLicenseQuery, 
            (void**)&pLicenseQuery);
    }

    // TODO: Use the methods of IWMDRMLicenseQuery as required.

    // Cleanup and shutdown.
    SAFE_RELEASE(pLicenseQuery);
    SAFE_RELEASE(pProvider);

    hr = WMDRMShutdown();
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività iniziali**](drm-getting-started.md)
</dt> </dl>

 

 




