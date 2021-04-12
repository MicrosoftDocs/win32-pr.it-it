---
title: Nozioni fondamentali sulle applicazioni
description: Nozioni fondamentali sulle applicazioni
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- Windows Media Format SDK, nozioni fondamentali sulle applicazioni DRM
- Digital Rights Management (DRM), nozioni fondamentali sulle applicazioni
- DRM (Digital Rights Management), nozioni fondamentali sulle applicazioni
- Digital Rights Management (DRM), funzione WMDRMStartup
- DRM (Digital Rights Management), funzione WMDRMStartup
- WMDRMStartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182a9e54e077c174c4f4cbe74ba392aa44ce5112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220981"
---
# <a name="application-basics"></a>Nozioni fondamentali sulle applicazioni

È necessario eseguire alcune operazioni di elaborazione aggiuntive per tutte le applicazioni che usano le API estese del client Windows Media DRM. In questo argomento vengono descritti i requisiti per una semplice applicazione.

Per prima cosa, è necessario inizializzare le API estese del client Windows Media DRM chiamando la funzione [**WMDRMStartup**](wmdrmstartup.md) . Gli oggetti dell'SDK sono oggetti COM, ma non è necessario chiamare **CoIntialize**, perché la funzione **WMDRMStatup** Inizializza com.

> [!Note]  
> Windows Media Format SDK utilizza solo un subset di COM, pertanto se si utilizzano oggetti COM diversi da quelli nell'API Windows Media DRM client Extended, è comunque necessario chiamare **CoInitialize**.

 

Tutti gli oggetti delle API estese del client Windows Media DRM vengono creati usando funzioni e metodi helper. Non è mai necessario chiamare **CoCreateInstance** per creare un oggetto. La prima interfaccia di cui creare un'istanza per qualsiasi applicazione che usa l'SDK è [**IWMDRMProvider**](iwmdrmprovider.md), che è possibile usare per creare un'istanza di tutte le altre interfacce di base. Per ottenere un'istanza di **IWMDRMProvider**, è necessario chiamare [**WMDRMCreateProvider**](wmdrmcreateprovider.md) o [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md). La differenza tra queste funzioni è che **WMDRMCreateProvider** crea un oggetto che può a sua volta creare solo oggetti che non supportano metodi che richiedono la libreria stub.

Dopo avere creato un'istanza di **IWMDRMProvider**, è possibile creare gli altri oggetti necessari chiamando [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).

Quando si è pronti per uscire dall'applicazione, è necessario rilasciare le risorse del sottosistema DRM chiamando la funzione [**WMDRMShutdown**](wmdrmshutdown.md) . Questa funzione arresta anche COM.

Nell'esempio di codice riportato di seguito viene illustrato come inizializzare e concludere un'applicazione che utilizza le API estese del client Windows Media DRM.


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

[**Introduzione**](drm-getting-started.md)
</dt> </dl>

 

 




