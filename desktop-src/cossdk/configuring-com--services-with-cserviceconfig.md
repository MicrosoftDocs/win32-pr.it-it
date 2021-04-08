---
description: Configurazione dei servizi COM+ con CServiceConfig
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: Configurazione dei servizi COM+ con CServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748050"
---
# <a name="configuring-com-services-with-cserviceconfig"></a><span data-ttu-id="8c494-103">Configurazione dei servizi COM+ con CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="8c494-103">Configuring COM+ Services with CServiceConfig</span></span>

<span data-ttu-id="8c494-104">La classe [**CServiceConfig**](cserviceconfig.md) viene utilizzata per configurare i servizi com+ che possono essere utilizzati senza componenti.</span><span class="sxs-lookup"><span data-stu-id="8c494-104">The [**CServiceConfig**](cserviceconfig.md) class is used to configure the COM+ services that can be used without components.</span></span> <span data-ttu-id="8c494-105">Aggrega il gestore di marshalling a thread libero, in modo che possa essere usato in diversi Apartment.</span><span class="sxs-lookup"><span data-stu-id="8c494-105">It aggregates the free-threaded marshaler, so it can be used in different apartments.</span></span> <span data-ttu-id="8c494-106">Per configurare un singolo servizio, è necessario chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per l'interfaccia associata al servizio e quindi chiamare i metodi su tale interfaccia per stabilire la configurazione appropriata.</span><span class="sxs-lookup"><span data-stu-id="8c494-106">To configure an individual service, you must call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span> <span data-ttu-id="8c494-107">Nella tabella seguente vengono descritte le interfacce implementate tramite la classe **CServiceConfig** .</span><span class="sxs-lookup"><span data-stu-id="8c494-107">The following table describes the interfaces that are implemented through the **CServiceConfig** class.</span></span>



| <span data-ttu-id="8c494-108">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="8c494-108">Interface</span></span>                                                                         | <span data-ttu-id="8c494-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c494-109">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c494-110">**IServiceInheritanceConfig**</span><span class="sxs-lookup"><span data-stu-id="8c494-110">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | <span data-ttu-id="8c494-111">Interfaccia predefinita per la classe.</span><span class="sxs-lookup"><span data-stu-id="8c494-111">The default interface for the class.</span></span> <span data-ttu-id="8c494-112">Viene usato per inizializzare rapidamente molti dei servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="8c494-112">It is used to quickly initialize many of the COM+ services.</span></span><br/>                                                                                              |
| [<span data-ttu-id="8c494-113">**IServiceComTIIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="8c494-113">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | <span data-ttu-id="8c494-114">Utilizzato per configurare le informazioni intrinseche COM Transaction Integrator (COMTI).</span><span class="sxs-lookup"><span data-stu-id="8c494-114">Used to configure the COM Transaction Integrator (COMTI) intrinsics information.</span></span> <span data-ttu-id="8c494-115">COMTI consente agli sviluppatori di integrare programmi di transazione basati su mainframe con applicazioni basate su componenti.</span><span class="sxs-lookup"><span data-stu-id="8c494-115">COMTI allows developers to integrate mainframe-based transaction programs with component-based applications.</span></span><br/> |
| [<span data-ttu-id="8c494-116">**IServiceIISIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="8c494-116">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | <span data-ttu-id="8c494-117">Utilizzato per configurare le informazioni intrinseche di Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="8c494-117">Used to configure the Internet Information Services (IIS) intrinsics information.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="8c494-118">**IServicePartitionConfig**</span><span class="sxs-lookup"><span data-stu-id="8c494-118">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | <span data-ttu-id="8c494-119">Utilizzato per configurare la modalità di utilizzo delle partizioni COM+ con i servizi.</span><span class="sxs-lookup"><span data-stu-id="8c494-119">Used to configure how COM+ partitions are used with the services.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="8c494-120">**IServiceSxSConfig**</span><span class="sxs-lookup"><span data-stu-id="8c494-120">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | <span data-ttu-id="8c494-121">Utilizzato per configurare gli assembly affiancati.</span><span class="sxs-lookup"><span data-stu-id="8c494-121">Used to configure side-by-side assemblies.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="8c494-122">**IServiceSynchronizationConfig**</span><span class="sxs-lookup"><span data-stu-id="8c494-122">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | <span data-ttu-id="8c494-123">Utilizzato per configurare i servizi di sincronizzazione COM+.</span><span class="sxs-lookup"><span data-stu-id="8c494-123">Used to configure COM+ synchronization services.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="8c494-124">**IServiceThreadPoolConfig**</span><span class="sxs-lookup"><span data-stu-id="8c494-124">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | <span data-ttu-id="8c494-125">Utilizzato per configurare il pool di thread per il servizio COM+.</span><span class="sxs-lookup"><span data-stu-id="8c494-125">Used to configure the thread pool for the COM+ service.</span></span> <span data-ttu-id="8c494-126">Il pool di thread può essere configurato solo quando si usa la funzione [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) .</span><span class="sxs-lookup"><span data-stu-id="8c494-126">The thread pool can be configured only when using the [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function.</span></span><br/>                          |
| [<span data-ttu-id="8c494-127">**IServiceTrackerConfig**</span><span class="sxs-lookup"><span data-stu-id="8c494-127">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | <span data-ttu-id="8c494-128">Utilizzato per configurare la proprietà Tracker.</span><span class="sxs-lookup"><span data-stu-id="8c494-128">Used to configure the Tracker property.</span></span> <span data-ttu-id="8c494-129">Tracker è un meccanismo di creazione di report utilizzato dal codice di monitoraggio per controllare quale codice viene eseguito quando.</span><span class="sxs-lookup"><span data-stu-id="8c494-129">Tracker is a reporting mechanism used by monitoring code to watch which code is running when.</span></span><br/>                                                         |
| [<span data-ttu-id="8c494-130">**IServiceTransactionConfig**</span><span class="sxs-lookup"><span data-stu-id="8c494-130">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | <span data-ttu-id="8c494-131">Utilizzato per configurare il servizio di transazione COM+.</span><span class="sxs-lookup"><span data-stu-id="8c494-131">Used to configure the COM+ transaction service.</span></span><br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="8c494-132">Strumento di amministrazione Servizi componenti</span><span class="sxs-lookup"><span data-stu-id="8c494-132">Component Services Administrative Tool</span></span>

<span data-ttu-id="8c494-133">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="8c494-133">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="8c494-134">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8c494-134">Visual Basic</span></span>

<span data-ttu-id="8c494-135">Non è valida.</span><span class="sxs-lookup"><span data-stu-id="8c494-135">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="8c494-136">C/C++</span><span class="sxs-lookup"><span data-stu-id="8c494-136">C/C++</span></span>

<span data-ttu-id="8c494-137">Nel frammento di codice seguente viene illustrato come creare e configurare un oggetto [**CServiceConfig**](cserviceconfig.md) per l'utilizzo di transazioni com+.</span><span class="sxs-lookup"><span data-stu-id="8c494-137">The following code fragment illustrates how to create and configure a [**CServiceConfig**](cserviceconfig.md) object to use COM+ transactions.</span></span>


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a><span data-ttu-id="8c494-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c494-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c494-139">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="8c494-139">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="8c494-140">Uso dei servizi COM+ tramite CoCreateActivity</span><span class="sxs-lookup"><span data-stu-id="8c494-140">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[<span data-ttu-id="8c494-141">Uso dei servizi COM+ tramite CoEnterServiceDomain e CoLeaveServiceDomain</span><span class="sxs-lookup"><span data-stu-id="8c494-141">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

