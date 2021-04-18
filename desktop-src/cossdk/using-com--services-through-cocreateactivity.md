---
description: La funzione CoCreateActivity viene usata per inviare il lavoro batch al sistema COM+. Consente alle applicazioni basate su script di supportare una configurazione del servizio COM+ a livello di applicazione.
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: Uso dei servizi COM+ tramite CoCreateActivity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b3296756b91d0f8ea29b1d67c11c78c431cfcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305205"
---
# <a name="using-com-services-through-cocreateactivity"></a>Uso dei servizi COM+ tramite CoCreateActivity

La funzione [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) viene usata per inviare il lavoro batch al sistema com+. Consente alle applicazioni basate su script di supportare una configurazione del servizio COM+ a livello di applicazione.

I servizi COM+ desiderati vengono configurati tramite un oggetto [**CServiceConfig**](cserviceconfig.md) passato alla funzione. La funzione crea un oggetto attività e restituisce l'interfaccia [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) dell'oggetto. Il lavoro batch può essere inviato in modalità sincrona o asincrona, usando rispettivamente i metodi [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) o [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) di **IServiceActivity**. Un puntatore a un'interfaccia [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) viene passato a ognuno di questi metodi e il lavoro batch viene implementato dallo sviluppatore nel metodo [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) dell'interfaccia **IServiceCall** .

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Non è valida.

## <a name="visual-basic"></a>Visual Basic

Non è valida.

## <a name="cc"></a>C/C++

Nel frammento di codice seguente viene illustrato come utilizzare i servizi COM+ tramite [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity). La gestione degli errori è stata omessa per brevità. Questo frammento di codice usa l'oggetto [**CServiceConfig**](cserviceconfig.md) creato e configurato nella [configurazione dei servizi com+ con CServiceConfig](configuring-com--services-with-cserviceconfig.md).


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

 

 



