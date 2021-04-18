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
# <a name="using-com-services-through-cocreateactivity"></a><span data-ttu-id="fbc46-104">Uso dei servizi COM+ tramite CoCreateActivity</span><span class="sxs-lookup"><span data-stu-id="fbc46-104">Using COM+ Services Through CoCreateActivity</span></span>

<span data-ttu-id="fbc46-105">La funzione [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) viene usata per inviare il lavoro batch al sistema com+.</span><span class="sxs-lookup"><span data-stu-id="fbc46-105">The [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function is used to submit batch work to the COM+ system.</span></span> <span data-ttu-id="fbc46-106">Consente alle applicazioni basate su script di supportare una configurazione del servizio COM+ a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="fbc46-106">It allows script-based applications to support an application-wide COM+ service configuration.</span></span>

<span data-ttu-id="fbc46-107">I servizi COM+ desiderati vengono configurati tramite un oggetto [**CServiceConfig**](cserviceconfig.md) passato alla funzione.</span><span class="sxs-lookup"><span data-stu-id="fbc46-107">The desired COM+ services are configured through a [**CServiceConfig**](cserviceconfig.md) object that is passed in to the function.</span></span> <span data-ttu-id="fbc46-108">La funzione crea un oggetto attività e restituisce l'interfaccia [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fbc46-108">The function creates an activity object and returns the [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) interface of that object.</span></span> <span data-ttu-id="fbc46-109">Il lavoro batch può essere inviato in modalità sincrona o asincrona, usando rispettivamente i metodi [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) o [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) di **IServiceActivity**.</span><span class="sxs-lookup"><span data-stu-id="fbc46-109">The batch work can be submitted either synchronously or asynchronously, by using the [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) or [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) methods of **IServiceActivity**, respectively.</span></span> <span data-ttu-id="fbc46-110">Un puntatore a un'interfaccia [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) viene passato a ognuno di questi metodi e il lavoro batch viene implementato dallo sviluppatore nel metodo [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) dell'interfaccia **IServiceCall** .</span><span class="sxs-lookup"><span data-stu-id="fbc46-110">A pointer to an [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) interface is passed in to each of these methods, and the batch work is implemented by the developer in the [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) method of the **IServiceCall** interface.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="fbc46-111">Strumento di amministrazione Servizi componenti</span><span class="sxs-lookup"><span data-stu-id="fbc46-111">Component Services Administrative Tool</span></span>

<span data-ttu-id="fbc46-112">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="fbc46-112">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="fbc46-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="fbc46-113">Visual Basic</span></span>

<span data-ttu-id="fbc46-114">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="fbc46-114">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="fbc46-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="fbc46-115">C/C++</span></span>

<span data-ttu-id="fbc46-116">Nel frammento di codice seguente viene illustrato come utilizzare i servizi COM+ tramite [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity).</span><span class="sxs-lookup"><span data-stu-id="fbc46-116">The following code fragment illustrates how to use COM+ services through [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity).</span></span> <span data-ttu-id="fbc46-117">La gestione degli errori è stata omessa per brevità.</span><span class="sxs-lookup"><span data-stu-id="fbc46-117">Error handling is omitted for brevity.</span></span> <span data-ttu-id="fbc46-118">Questo frammento di codice usa l'oggetto [**CServiceConfig**](cserviceconfig.md) creato e configurato nella [configurazione dei servizi com+ con CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span><span class="sxs-lookup"><span data-stu-id="fbc46-118">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fbc46-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fbc46-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbc46-120">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="fbc46-120">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="fbc46-121">Configurazione dei servizi COM+ con CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="fbc46-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="fbc46-122">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="fbc46-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="fbc46-123">Uso dei servizi COM+ tramite CoEnterServiceDomain e CoLeaveServiceDomain</span><span class="sxs-lookup"><span data-stu-id="fbc46-123">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



