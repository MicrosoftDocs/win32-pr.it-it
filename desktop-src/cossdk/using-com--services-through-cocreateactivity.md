---
description: La funzione CoCreateActivity viene usata per inviare il lavoro batch al sistema COM+. Consente alle applicazioni basate su script di supportare una configurazione del servizio COM+ a livello di applicazione.
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: Uso dei servizi COM+ tramite CoCreateActivity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b5452c99fa431e7c1927646eec7ad9b5e5fa930f3ba7d0bf242df7690325db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128663"
---
# <a name="using-com-services-through-cocreateactivity"></a>Uso dei servizi COM+ tramite CoCreateActivity

La [**funzione CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) viene usata per inviare il lavoro batch al sistema COM+. Consente alle applicazioni basate su script di supportare una configurazione del servizio COM+ a livello di applicazione.

I servizi COM+ desiderati vengono configurati tramite un [**oggetto CServiceConfig**](cserviceconfig.md) passato alla funzione. La funzione crea un oggetto attività e restituisce [**l'interfaccia IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) di tale oggetto. Il lavoro batch può essere inviato in modo sincrono o asincrono, usando rispettivamente i metodi [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) o [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) **di IServiceActivity.** Un puntatore a [**un'interfaccia IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) viene passato a ognuno di questi metodi e il lavoro batch viene implementato dallo sviluppatore nel metodo [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) **dell'interfaccia IServiceCall.**

## <a name="component-services-administrative-tool"></a>Strumento amministrativo servizi componenti

Non è valida.

## <a name="visual-basic"></a>Visual Basic

Non è valida.

## <a name="cc"></a>C/C++

Il frammento di codice seguente illustra come usare i servizi COM+ tramite [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity). La gestione degli errori è stata omessa per brevità. Questo frammento di codice usa [**l'oggetto CServiceConfig**](cserviceconfig.md) creato e configurato in [Configurazione dei servizi COM+ con CServiceConfig](configuring-com--services-with-cserviceconfig.md).


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER,
//   IID_IUnknown, (void**)&pUnknownCSC);

// Create the activity for our services.
HRESULT hr = CoCreateActivity(pUnknownCSC, IID_IServiceActivity, (void**)&pActivity);
if (FAILED(hr)) throw(hr);

// Do the batch work synchronously.
// The batch work is implemented in pServiceCall->OnCall().
hr = pActivity->SynchronousCall(pServiceCall);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[Configurazione dei servizi COM+ con CServiceConfig](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[Uso dei servizi COM+ tramite CoEnterServiceDomain e CoLeaveServiceDomain](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



