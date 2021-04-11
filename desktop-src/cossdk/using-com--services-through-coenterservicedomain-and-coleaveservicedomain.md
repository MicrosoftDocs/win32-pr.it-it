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
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a><span data-ttu-id="7f812-103">Uso dei servizi COM+ tramite CoEnterServiceDomain e CoLeaveServiceDomain</span><span class="sxs-lookup"><span data-stu-id="7f812-103">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>

<span data-ttu-id="7f812-104">[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) e [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) vengono utilizzati insieme per racchiudere un'area di codice in esecuzione nel proprio contesto e possono utilizzare i servizi com+ senza la necessità di componenti com+.</span><span class="sxs-lookup"><span data-stu-id="7f812-104">[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) are used together to surround an area of code that runs in its own context and can use COM+ services without the need for COM+ components.</span></span> <span data-ttu-id="7f812-105">I servizi COM+ usati in questo contesto vengono configurati tramite l'oggetto [**CServiceConfig**](cserviceconfig.md) passato a **CoEnterServiceDomain**.</span><span class="sxs-lookup"><span data-stu-id="7f812-105">The COM+ services that are used in this context are configured through the [**CServiceConfig**](cserviceconfig.md) object that is passed in to **CoEnterServiceDomain**.</span></span> <span data-ttu-id="7f812-106">Il codice racchiuso tra **CoEnterServiceDomain** e **CoLeaveServiceDomain** si comporta come se fosse un metodo chiamato su un oggetto creato all'interno di questo contesto.</span><span class="sxs-lookup"><span data-stu-id="7f812-106">The code that is surrounded by **CoEnterServiceDomain** and **CoLeaveServiceDomain** behaves as though it were a method that is called on an object created within this context.</span></span>

<span data-ttu-id="7f812-107">Un'applicazione di scripting può utilizzare questa coppia di funzioni per fornire supporto in fase di esecuzione dei servizi COM+ senza componenti.</span><span class="sxs-lookup"><span data-stu-id="7f812-107">A scripting application can use this pair of functions to provide run-time support of COM+ services without components.</span></span> <span data-ttu-id="7f812-108">È ad esempio possibile sviluppare un'applicazione di scripting per fornire Tag che consentano agli autori di script di immettere e lasciare un dominio del servizio all'interno dello script.</span><span class="sxs-lookup"><span data-stu-id="7f812-108">For example, a scripting application can be developed to provide tags that allow the script writers to enter and leave a service domain within the script.</span></span> <span data-ttu-id="7f812-109">Quando il motore di scripting elabora lo script e rileva i tag, può chiamare [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) con un oggetto [**CServiceConfig**](cserviceconfig.md) preconfigurato, eseguire il codice necessario e quindi chiamare [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span><span class="sxs-lookup"><span data-stu-id="7f812-109">When the scripting engine processes the script and encounters the tags, it can call [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) with a preconfigured [**CServiceConfig**](cserviceconfig.md) object, run the necessary code, and then call [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="7f812-110">Strumento di amministrazione Servizi componenti</span><span class="sxs-lookup"><span data-stu-id="7f812-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="7f812-111">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="7f812-111">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="7f812-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7f812-112">Visual Basic</span></span>

<span data-ttu-id="7f812-113">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="7f812-113">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="7f812-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="7f812-114">C/C++</span></span>

<span data-ttu-id="7f812-115">Nel frammento di codice seguente viene illustrato come utilizzare i servizi COM+ tra le chiamate a [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) e [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span><span class="sxs-lookup"><span data-stu-id="7f812-115">The following code fragment illustrates how to use COM+ services between calls to [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span> <span data-ttu-id="7f812-116">La gestione degli errori è stata omessa per brevità.</span><span class="sxs-lookup"><span data-stu-id="7f812-116">Error handling is omitted for brevity.</span></span> <span data-ttu-id="7f812-117">Questo frammento di codice usa l'oggetto [**CServiceConfig**](cserviceconfig.md) creato e configurato nella [configurazione dei servizi com+ con CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span><span class="sxs-lookup"><span data-stu-id="7f812-117">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7f812-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f812-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f812-119">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="7f812-119">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="7f812-120">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="7f812-120">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="7f812-121">Configurazione dei servizi COM+ con CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="7f812-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="7f812-122">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="7f812-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="7f812-123">Uso dei servizi COM+ tramite CoCreateActivity</span><span class="sxs-lookup"><span data-stu-id="7f812-123">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



