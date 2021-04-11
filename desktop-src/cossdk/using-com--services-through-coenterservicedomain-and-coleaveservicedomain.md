---
description: Uso dei servizi COM+ tramite CoEnterServiceDomain e CoLeaveServiceDomain
ms.assetid: 763fb01e-5daf-4e9b-8ef1-9ae79c0a84cc
title: Uso dei servizi COM+ tramite CoEnterServiceDomain e CoLeaveServiceDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d87931628e177374dd07b40e9917a56c168a81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127134"
---
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a>Uso dei servizi COM+ tramite CoEnterServiceDomain e CoLeaveServiceDomain

[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) e [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) vengono utilizzati insieme per racchiudere un'area di codice in esecuzione nel proprio contesto e possono utilizzare i servizi com+ senza la necessità di componenti com+. I servizi COM+ usati in questo contesto vengono configurati tramite l'oggetto [**CServiceConfig**](cserviceconfig.md) passato a **CoEnterServiceDomain**. Il codice racchiuso tra **CoEnterServiceDomain** e **CoLeaveServiceDomain** si comporta come se fosse un metodo chiamato su un oggetto creato all'interno di questo contesto.

Un'applicazione di scripting può utilizzare questa coppia di funzioni per fornire supporto in fase di esecuzione dei servizi COM+ senza componenti. È ad esempio possibile sviluppare un'applicazione di scripting per fornire Tag che consentano agli autori di script di immettere e lasciare un dominio del servizio all'interno dello script. Quando il motore di scripting elabora lo script e rileva i tag, può chiamare [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) con un oggetto [**CServiceConfig**](cserviceconfig.md) preconfigurato, eseguire il codice necessario e quindi chiamare [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Non è valida.

## <a name="visual-basic"></a>Visual Basic

Non è valida.

## <a name="cc"></a>C/C++

Nel frammento di codice seguente viene illustrato come utilizzare i servizi COM+ tra le chiamate a [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) e [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain). La gestione degli errori è stata omessa per brevità. Questo frammento di codice usa l'oggetto [**CServiceConfig**](cserviceconfig.md) creato e configurato nella [configurazione dei servizi com+ con CServiceConfig](configuring-com--services-with-cserviceconfig.md).


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
//   IID_IUnknown, (void**)&pUnknownCSC);

// Enter the Service Domain.
HRESULT hr = CoEnterServiceDomain(pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Do the work that uses COM+ services here.
//DoMyWork();

// Leave the Service Domain.
CoLeaveServiceDomain(NULL);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[Configurazione dei servizi COM+ con CServiceConfig](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[Uso dei servizi COM+ tramite CoCreateActivity](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



