---
description: Specifica e configura i servizi che devono essere attivi nel dominio del servizio immesso quando si chiama CoCreateActivity o CoEnterServiceDomain.
ms.assetid: f546ded4-255e-4565-b588-f36175902778
title: Classe CServiceConfig (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CServiceConfig
api_type:
- COM
ms.openlocfilehash: e0b48b05be4afa1d42dbc8a16c4b596a08aba859
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304630"
---
# <a name="cserviceconfig-class"></a><span data-ttu-id="0abc0-103">Classe CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="0abc0-103">CServiceConfig class</span></span>

<span data-ttu-id="0abc0-104">Specifica e configura i servizi che devono essere attivi nel dominio del servizio immesso quando si chiama [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) o [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).</span><span class="sxs-lookup"><span data-stu-id="0abc0-104">Specifies and configures the services that are to be active in the service domain entered when calling either [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) or [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="0abc0-105">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="0abc0-105">When to implement</span></span>

<span data-ttu-id="0abc0-106">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="0abc0-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="0abc0-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="0abc0-107">Requirement</span></span> | <span data-ttu-id="0abc0-108">Valore</span><span class="sxs-lookup"><span data-stu-id="0abc0-108">Value</span></span> |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0abc0-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="0abc0-109">CLSID</span></span>      | <span data-ttu-id="0abc0-110">\_CSERVICECONFIG CLSID</span><span class="sxs-lookup"><span data-stu-id="0abc0-110">CLSID\_CServiceConfig</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="0abc0-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="0abc0-111">ProgID</span></span>     | <span data-ttu-id="0abc0-112">L "COMSVCS. CServiceConfig"</span><span class="sxs-lookup"><span data-stu-id="0abc0-112">L"COMSVCS.CServiceConfig"</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="0abc0-113">Interfacce</span><span class="sxs-lookup"><span data-stu-id="0abc0-113">Interfaces</span></span> | [<span data-ttu-id="0abc0-114">**IServiceComTIIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="0abc0-114">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> [<span data-ttu-id="0abc0-115">**IServiceIISIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="0abc0-115">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/> [<span data-ttu-id="0abc0-116">**IServiceInheritanceConfig**</span><span class="sxs-lookup"><span data-stu-id="0abc0-116">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/> [<span data-ttu-id="0abc0-117">**IServicePartitionConfig**</span><span class="sxs-lookup"><span data-stu-id="0abc0-117">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/> [<span data-ttu-id="0abc0-118">**IServiceSxSConfig**</span><span class="sxs-lookup"><span data-stu-id="0abc0-118">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/> [<span data-ttu-id="0abc0-119">**IServiceSynchronizationConfig**</span><span class="sxs-lookup"><span data-stu-id="0abc0-119">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> [<span data-ttu-id="0abc0-120">**IServiceThreadPoolConfig**</span><span class="sxs-lookup"><span data-stu-id="0abc0-120">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/> [<span data-ttu-id="0abc0-121">**IServiceTrackerConfig**</span><span class="sxs-lookup"><span data-stu-id="0abc0-121">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/> [<span data-ttu-id="0abc0-122">**IServiceTransactionConfig**</span><span class="sxs-lookup"><span data-stu-id="0abc0-122">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="0abc0-123">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0abc0-123">When to use</span></span>

<span data-ttu-id="0abc0-124">Utilizzare questa classe per configurare i servizi che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="0abc0-124">Use this class to configure the services that you want to use.</span></span> <span data-ttu-id="0abc0-125">[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) e [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) consentono di usare i servizi configurati da questa classe senza dover associare tali servizi a un componente prima di usarli.</span><span class="sxs-lookup"><span data-stu-id="0abc0-125">[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) and [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) enable you to use the services configured by this class without needing to tie those services to a component before using them.</span></span>

<span data-ttu-id="0abc0-126">Questa classe non è stata progettata per essere utilizzata in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0abc0-126">This class was not designed to be used in Visual Basic.</span></span>

## <a name="remarks"></a><span data-ttu-id="0abc0-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="0abc0-127">Remarks</span></span>

<span data-ttu-id="0abc0-128">Per creare questo oggetto, chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="0abc0-128">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="0abc0-129">Gli oggetti di cui è stata creata un'istanza dalla classe **CServiceConfig** aggregano il gestore di marshalling a thread libero in modo che possano essere archiviati dai runtime di sistema e riutilizzati in diversi Apartment.</span><span class="sxs-lookup"><span data-stu-id="0abc0-129">Objects instantiated from the **CServiceConfig** class aggregate the free-threaded marshaler so that they can be stored by system runtimes and reused in different apartments.</span></span>

<span data-ttu-id="0abc0-130">Per configurare un singolo servizio, chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per l'interfaccia associata al servizio e quindi chiamare i metodi su tale interfaccia per stabilire la configurazione appropriata.</span><span class="sxs-lookup"><span data-stu-id="0abc0-130">To configure an individual service, call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="0abc0-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0abc0-131">Requirements</span></span>



| <span data-ttu-id="0abc0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0abc0-132">Requirement</span></span> | <span data-ttu-id="0abc0-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0abc0-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0abc0-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0abc0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0abc0-135">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="0abc0-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0abc0-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0abc0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0abc0-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0abc0-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0abc0-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0abc0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0abc0-139"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="0abc0-139"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0abc0-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0abc0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abc0-141">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="0abc0-141">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="0abc0-142">**CoCreateFreeThreadedMarshaler**</span><span class="sxs-lookup"><span data-stu-id="0abc0-142">**CoCreateFreeThreadedMarshaler**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)
</dt> <dt>

[<span data-ttu-id="0abc0-143">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="0abc0-143">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="0abc0-144">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="0abc0-144">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="0abc0-145">Servizi COM+ senza componenti</span><span class="sxs-lookup"><span data-stu-id="0abc0-145">COM+ Services Without Components</span></span>](com--services-without-components.md)
</dt> </dl>

 

