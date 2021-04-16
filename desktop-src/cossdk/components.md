---
description: Contiene un oggetto per ogni componente nell'applicazione correlata.
ms.assetid: f502ba60-b2b1-4556-8f91-22a474e60e0d
title: Raccolta componenti
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Components
api_type:
- COM
api_location: ''
ms.openlocfilehash: f68013985beff427b5681c5b78c2c00df9e69263
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524217"
---
# <a name="components-collection"></a><span data-ttu-id="6e8b5-103">Raccolta componenti</span><span class="sxs-lookup"><span data-stu-id="6e8b5-103">Components collection</span></span>

<span data-ttu-id="6e8b5-104">Contiene un oggetto per ogni componente nell'applicazione correlata.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-104">Contains an object for each component in the related application.</span></span> <span data-ttu-id="6e8b5-105">La raccolta **Components** è sempre correlata a un oggetto nella raccolta [**Applications**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="6e8b5-105">The **Components** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="6e8b5-106">Le proprietà esposte da questi oggetti contengono impostazioni effettuate a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-106">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="6e8b5-107">Questa raccolta supporta il metodo [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , ma non il metodo [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="6e8b5-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="6e8b5-108">Per installare o importare componenti in un'applicazione, usare i metodi sull'oggetto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="6e8b5-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="6e8b5-109">Membri</span><span class="sxs-lookup"><span data-stu-id="6e8b5-109">Members</span></span>

<span data-ttu-id="6e8b5-110">La raccolta **Components** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-110">The **Components** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="6e8b5-111">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="6e8b5-111">Related Collections</span></span>

<span data-ttu-id="6e8b5-112">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="6e8b5-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="6e8b5-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="6e8b5-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="6e8b5-114">**InterfacesForComponent**</span><span class="sxs-lookup"><span data-stu-id="6e8b5-114">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)
-   [<span data-ttu-id="6e8b5-115">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="6e8b5-115">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="6e8b5-116">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="6e8b5-116">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="6e8b5-117">**RolesForComponent**</span><span class="sxs-lookup"><span data-stu-id="6e8b5-117">**RolesForComponent**</span></span>](rolesforcomponent.md)
-   [<span data-ttu-id="6e8b5-118">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="6e8b5-118">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

<span data-ttu-id="6e8b5-119">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="6e8b5-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="6e8b5-120">**Applicazioni**</span><span class="sxs-lookup"><span data-stu-id="6e8b5-120">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="6e8b5-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6e8b5-121">Properties</span></span>

<span data-ttu-id="6e8b5-122">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="6e8b5-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="6e8b5-123">AllowInprocSubscribers</span><span class="sxs-lookup"><span data-stu-id="6e8b5-123">AllowInprocSubscribers</span></span>](#allowinprocsubscribers)
-   [<span data-ttu-id="6e8b5-124">ApplicationID</span><span class="sxs-lookup"><span data-stu-id="6e8b5-124">ApplicationID</span></span>](#applicationid)
-   [<span data-ttu-id="6e8b5-125">Numero di bit</span><span class="sxs-lookup"><span data-stu-id="6e8b5-125">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="6e8b5-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="6e8b5-126">CLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="6e8b5-127">ComponentAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-127">ComponentAccessChecksEnabled</span></span>](#componentaccesschecksenabled)
-   [<span data-ttu-id="6e8b5-128">ComponentTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="6e8b5-128">ComponentTransactionTimeout</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="6e8b5-129">ComponentTransactionTimeoutEnabled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-129">ComponentTransactionTimeoutEnabled</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="6e8b5-130">COMTIIntrinsics</span><span class="sxs-lookup"><span data-stu-id="6e8b5-130">COMTIIntrinsics</span></span>](#comtiintrinsics)
-   [<span data-ttu-id="6e8b5-131">ConstructionEnabled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-131">ConstructionEnabled</span></span>](#constructionenabled)
-   [<span data-ttu-id="6e8b5-132">ConstructorString</span><span class="sxs-lookup"><span data-stu-id="6e8b5-132">ConstructorString</span></span>](#constructorstring)
-   [<span data-ttu-id="6e8b5-133">CreationTimeout</span><span class="sxs-lookup"><span data-stu-id="6e8b5-133">CreationTimeout</span></span>](#creationtimeout)
-   [<span data-ttu-id="6e8b5-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-134">Description</span></span>](#description)
-   [<span data-ttu-id="6e8b5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6e8b5-135">DLL</span></span>](#dll)
-   [<span data-ttu-id="6e8b5-136">EventTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-136">EventTrackingEnabled</span></span>](#eventtrackingenabled)
-   [<span data-ttu-id="6e8b5-137">P:System.EnterpriseServices.ExceptionClassAttribute.Value</span><span class="sxs-lookup"><span data-stu-id="6e8b5-137">ExceptionClass</span></span>](#exceptionclass)
-   [<span data-ttu-id="6e8b5-138">FireInParallel</span><span class="sxs-lookup"><span data-stu-id="6e8b5-138">FireInParallel</span></span>](#fireinparallel)
-   [<span data-ttu-id="6e8b5-139">IISIntrinsics</span><span class="sxs-lookup"><span data-stu-id="6e8b5-139">IISIntrinsics</span></span>](#iisintrinsics)
-   [<span data-ttu-id="6e8b5-140">InitializeServerApplication</span><span class="sxs-lookup"><span data-stu-id="6e8b5-140">InitializeServerApplication</span></span>](#initializeserverapplication)
-   [<span data-ttu-id="6e8b5-141">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-141">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="6e8b5-142">IsEventClass</span><span class="sxs-lookup"><span data-stu-id="6e8b5-142">IsEventClass</span></span>](#iseventclass)
-   [<span data-ttu-id="6e8b5-143">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-143">IsInstalled</span></span>](#isinstalled)
-   [<span data-ttu-id="6e8b5-144">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="6e8b5-144">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="6e8b5-145">JustInTimeActivation</span><span class="sxs-lookup"><span data-stu-id="6e8b5-145">JustInTimeActivation</span></span>](#justintimeactivation)
-   [<span data-ttu-id="6e8b5-146">LoadBalancingSupported</span><span class="sxs-lookup"><span data-stu-id="6e8b5-146">LoadBalancingSupported</span></span>](#loadbalancingsupported)
-   [<span data-ttu-id="6e8b5-147">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="6e8b5-147">MaxPoolSize</span></span>](#maxpoolsize)
-   [<span data-ttu-id="6e8b5-148">MinPoolSize</span><span class="sxs-lookup"><span data-stu-id="6e8b5-148">MinPoolSize</span></span>](#minpoolsize)
-   [<span data-ttu-id="6e8b5-149">MultiInterfacePublisherFilterCLSID</span><span class="sxs-lookup"><span data-stu-id="6e8b5-149">MultiInterfacePublisherFilterCLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="6e8b5-150">MustRunInClientContext</span><span class="sxs-lookup"><span data-stu-id="6e8b5-150">MustRunInClientContext</span></span>](#mustruninclientcontext)
-   [<span data-ttu-id="6e8b5-151">MustRunInDefaultContext</span><span class="sxs-lookup"><span data-stu-id="6e8b5-151">MustRunInDefaultContext</span></span>](#mustrunindefaultcontext)
-   [<span data-ttu-id="6e8b5-152">ObjectPoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-152">ObjectPoolingEnabled</span></span>](#objectpoolingenabled)
-   [<span data-ttu-id="6e8b5-153">ProgID</span><span class="sxs-lookup"><span data-stu-id="6e8b5-153">ProgID</span></span>](#progid)
-   [<span data-ttu-id="6e8b5-154">PublisherID</span><span class="sxs-lookup"><span data-stu-id="6e8b5-154">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="6e8b5-155">SoapAssemblyName</span><span class="sxs-lookup"><span data-stu-id="6e8b5-155">SoapAssemblyName</span></span>](#soapassemblyname)
-   [<span data-ttu-id="6e8b5-156">SoapTypeName</span><span class="sxs-lookup"><span data-stu-id="6e8b5-156">SoapTypeName</span></span>](#soaptypename)
-   [<span data-ttu-id="6e8b5-157">Sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-157">Synchronization</span></span>](#synchronization)
-   [<span data-ttu-id="6e8b5-158">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="6e8b5-158">ThreadingModel</span></span>](#threadingmodel)
-   [<span data-ttu-id="6e8b5-159">Transazione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-159">Transaction</span></span>](#componenttransactiontimeout)
-   [<span data-ttu-id="6e8b5-160">Proprietà TxIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="6e8b5-160">TxIsolationLevel</span></span>](#txisolationlevel)
-   [<span data-ttu-id="6e8b5-161">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="6e8b5-161">VersionBuild</span></span>](#versionbuild)
-   [<span data-ttu-id="6e8b5-162">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="6e8b5-162">VersionMajor</span></span>](#versionmajor)
-   [<span data-ttu-id="6e8b5-163">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="6e8b5-163">VersionMinor</span></span>](#versionminor)
-   [<span data-ttu-id="6e8b5-164">VersionSubBuild</span><span class="sxs-lookup"><span data-stu-id="6e8b5-164">VersionSubBuild</span></span>](#versionsubbuild)

### <a name="allowinprocsubscribers"></a><span data-ttu-id="6e8b5-165">AllowInprocSubscribers</span><span class="sxs-lookup"><span data-stu-id="6e8b5-165">AllowInprocSubscribers</span></span>



| <span data-ttu-id="6e8b5-166">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-166">Entry</span></span> | <span data-ttu-id="6e8b5-167">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-167">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-168">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-168">Description</span></span>    | <span data-ttu-id="6e8b5-169">Abilita nei Sottoscrittori di processo se il componente è una classe di evento.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-169">Enables in process subscribers if the component is an event class.</span></span> |
| <span data-ttu-id="6e8b5-170">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-170">Access</span></span>         | <span data-ttu-id="6e8b5-171">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-171">ReadWrite</span></span>                                                          |
| <span data-ttu-id="6e8b5-172">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-172">Type</span></span>           | <span data-ttu-id="6e8b5-173">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-173">Bool</span></span>                                                               |
| <span data-ttu-id="6e8b5-174">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-174">Default</span></span>        | <span data-ttu-id="6e8b5-175">Vero</span><span class="sxs-lookup"><span data-stu-id="6e8b5-175">True</span></span>                                                               |
| <span data-ttu-id="6e8b5-176">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-176">Minimum system</span></span> | <span data-ttu-id="6e8b5-177">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-177">Windows 2000</span></span>                                                       |



 

### <a name="applicationid"></a><span data-ttu-id="6e8b5-178">ApplicationID</span><span class="sxs-lookup"><span data-stu-id="6e8b5-178">ApplicationID</span></span>



| <span data-ttu-id="6e8b5-179">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-179">Entry</span></span> | <span data-ttu-id="6e8b5-180">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-180">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-181">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-181">Description</span></span>    | <span data-ttu-id="6e8b5-182">GUID per l'applicazione contenente il componente.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-182">The GUID for the application containing the component.</span></span> <span data-ttu-id="6e8b5-183">Deve essere un GUID di un'applicazione valida, che viene verificato prima che venga chiamato [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) .</span><span class="sxs-lookup"><span data-stu-id="6e8b5-183">Must be a valid application's GUID, which is verified before [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) is called.</span></span> <span data-ttu-id="6e8b5-184">Se questo valore viene modificato in modo da essere un GUID per un'altra applicazione, il componente si sposta sull'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-184">If this value is changed to be a GUID for a different application, the component moves to that application.</span></span> |
| <span data-ttu-id="6e8b5-185">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-185">Access</span></span>         | <span data-ttu-id="6e8b5-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-186">ReadWrite</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6e8b5-187">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-187">Type</span></span>           | <span data-ttu-id="6e8b5-188">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-188">String</span></span>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6e8b5-189">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-189">Default</span></span>        | <span data-ttu-id="6e8b5-190">N/D</span><span class="sxs-lookup"><span data-stu-id="6e8b5-190">N/A</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6e8b5-191">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-191">Minimum system</span></span> | <span data-ttu-id="6e8b5-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-192">Windows 2000</span></span>                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a><span data-ttu-id="6e8b5-193">Numero di bit</span><span class="sxs-lookup"><span data-stu-id="6e8b5-193">Bitness</span></span>



| <span data-ttu-id="6e8b5-194">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-194">Entry</span></span> | <span data-ttu-id="6e8b5-195">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-195">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-196">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-196">Description</span></span>    | <span data-ttu-id="6e8b5-197">Rappresenta il tipo di bit binario di un componente.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-197">Represents the binary bitness type of a component.</span></span> <span data-ttu-id="6e8b5-198">Nei sistemi che utilizzano Windows a 64 bit, questa proprietà distingue tra i componenti a 64 bit e i componenti a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-198">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="6e8b5-199">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-199">Access</span></span>         | <span data-ttu-id="6e8b5-200">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6e8b5-200">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="6e8b5-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-201">Type</span></span>           | <span data-ttu-id="6e8b5-202">Valori lunghi possibili: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)</span><span class="sxs-lookup"><span data-stu-id="6e8b5-202">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                       |
| <span data-ttu-id="6e8b5-203">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-203">Default</span></span>        | <span data-ttu-id="6e8b5-204">N/D</span><span class="sxs-lookup"><span data-stu-id="6e8b5-204">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="6e8b5-205">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-205">Minimum system</span></span> | <span data-ttu-id="6e8b5-206">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6e8b5-206">Windows XP</span></span>                                                                                                                                                          |



 

### <a name="clsid"></a><span data-ttu-id="6e8b5-207">CLSID</span><span class="sxs-lookup"><span data-stu-id="6e8b5-207">CLSID</span></span>



| <span data-ttu-id="6e8b5-208">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-208">Entry</span></span> | <span data-ttu-id="6e8b5-209">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-209">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-210">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-210">Description</span></span>    | <span data-ttu-id="6e8b5-211">GUID per il componente.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-211">A GUID for the component.</span></span> <span data-ttu-id="6e8b5-212">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-212">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="6e8b5-213">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-213">Access</span></span>         | <span data-ttu-id="6e8b5-214">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6e8b5-214">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="6e8b5-215">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-215">Type</span></span>           | <span data-ttu-id="6e8b5-216">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-216">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="6e8b5-217">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-217">Default</span></span>        | <span data-ttu-id="6e8b5-218">N/D</span><span class="sxs-lookup"><span data-stu-id="6e8b5-218">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="6e8b5-219">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-219">Minimum system</span></span> | <span data-ttu-id="6e8b5-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-220">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a><span data-ttu-id="6e8b5-221">ComponentAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-221">ComponentAccessChecksEnabled</span></span>



| <span data-ttu-id="6e8b5-222">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-222">Entry</span></span> | <span data-ttu-id="6e8b5-223">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-223">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-224">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-224">Description</span></span>    | <span data-ttu-id="6e8b5-225">Indica se i controlli degli accessi in base al ruolo vengono eseguiti sulle chiamate al componente e funzionano insieme alle proprietà AccessChecksLevel e ApplicationAccessChecksEnabled nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-225">Indicates whether role-based access checks are performed on calls into the component and works in conjunction with the AccessChecksLevel and ApplicationAccessChecksEnabled properties on the application.</span></span> |
| <span data-ttu-id="6e8b5-226">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-226">Access</span></span>         | <span data-ttu-id="6e8b5-227">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-227">ReadWrite</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="6e8b5-228">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-228">Type</span></span>           | <span data-ttu-id="6e8b5-229">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-229">Bool</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="6e8b5-230">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-230">Default</span></span>        | <span data-ttu-id="6e8b5-231">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-231">False</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="6e8b5-232">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-232">Minimum system</span></span> | <span data-ttu-id="6e8b5-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-233">Windows 2000</span></span>                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a><span data-ttu-id="6e8b5-234">ComponentTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="6e8b5-234">ComponentTransactionTimeout</span></span>



| <span data-ttu-id="6e8b5-235">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-235">Entry</span></span> | <span data-ttu-id="6e8b5-236">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-236">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-237">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-237">Description</span></span>    | <span data-ttu-id="6e8b5-238">Se utilizzata in una transazione, specifica il periodo di tempo in cui il componente causa il timeout della transazione. Il valore predefinito è 60 secondi e non può essere più lungo di 3600 secondi (1 ora).</span><span class="sxs-lookup"><span data-stu-id="6e8b5-238">When used in a transaction, specifies the time period in which this component causes the transaction to time out. The default is 60 seconds and cannot be longer than 3600 seconds (1 hour).</span></span> <span data-ttu-id="6e8b5-239">Il valore di timeout può essere impostato su 0, specificando un periodo di timeout delle transazioni infinito.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-239">The time-out value can be set to 0, specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="6e8b5-240">Per usare questa proprietà, ComponentTransactionTimeoutEnabled deve essere true.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-240">For this property to be used, ComponentTransactionTimeoutEnabled must be True.</span></span> <span data-ttu-id="6e8b5-241">Il valore di questa proprietà esegue l'override del timeout della transazione globale specificato dalla proprietà TransactionTimeout della raccolta [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="6e8b5-241">The value of this property overrides the global transaction time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection.</span></span> |
| <span data-ttu-id="6e8b5-242">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-242">Access</span></span>         | <span data-ttu-id="6e8b5-243">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-243">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="6e8b5-244">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-244">Type</span></span>           | <span data-ttu-id="6e8b5-245">Long (0-3600)</span><span class="sxs-lookup"><span data-stu-id="6e8b5-245">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="6e8b5-246">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-246">Default</span></span>        | <span data-ttu-id="6e8b5-247">60</span><span class="sxs-lookup"><span data-stu-id="6e8b5-247">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6e8b5-248">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-248">Minimum system</span></span> | <span data-ttu-id="6e8b5-249">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-249">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a><span data-ttu-id="6e8b5-250">ComponentTransactionTimeoutEnabled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-250">ComponentTransactionTimeoutEnabled</span></span>



| <span data-ttu-id="6e8b5-251">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-251">Entry</span></span> | <span data-ttu-id="6e8b5-252">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-252">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-253">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-253">Description</span></span>    | <span data-ttu-id="6e8b5-254">Specifica se il periodo di timeout della transazione è abilitato per questo componente.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-254">Specifies whether the transaction time-out period is enabled for this component.</span></span> <span data-ttu-id="6e8b5-255">Per impostazione predefinita, la funzionalità di timeout della transazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-255">By default, the transaction time-out feature is disabled.</span></span> <span data-ttu-id="6e8b5-256">Quando questa proprietà è true, viene usato il timeout specificato da ComponentTransactionTimeout.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-256">When this property is True, the time-out specified by ComponentTransactionTimeout is used.</span></span> <span data-ttu-id="6e8b5-257">Quando questa proprietà è false, viene usato il timeout specificato dalla proprietà TransactionTimeout della raccolta [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="6e8b5-257">When this property is False, the time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="6e8b5-258">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-258">Access</span></span>         | <span data-ttu-id="6e8b5-259">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-259">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6e8b5-260">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-260">Type</span></span>           | <span data-ttu-id="6e8b5-261">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-261">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6e8b5-262">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-262">Default</span></span>        | <span data-ttu-id="6e8b5-263">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-263">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="6e8b5-264">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-264">Minimum system</span></span> | <span data-ttu-id="6e8b5-265">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-265">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a><span data-ttu-id="6e8b5-266">COMTIIntrinsics</span><span class="sxs-lookup"><span data-stu-id="6e8b5-266">COMTIIntrinsics</span></span>



| <span data-ttu-id="6e8b5-267">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-267">Entry</span></span> | <span data-ttu-id="6e8b5-268">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-268">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-269">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-269">Description</span></span>    | <span data-ttu-id="6e8b5-270">Consente il passaggio delle proprietà di contesto dal COM Transaction Integrator (COMTI) nel contesto per questa classe.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-270">Enables passing of context properties from the COM Transaction Integrator (COMTI) into the context for this class.</span></span> <span data-ttu-id="6e8b5-271">COMTI semplifica l'attività di wrapping delle transazioni mainframe e della logica di business come componenti COM.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-271">The COMTI eases the task of wrapping mainframe transactions and business logic as COM components.</span></span> |
| <span data-ttu-id="6e8b5-272">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-272">Access</span></span>         | <span data-ttu-id="6e8b5-273">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-273">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="6e8b5-274">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-274">Type</span></span>           | <span data-ttu-id="6e8b5-275">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-275">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="6e8b5-276">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-276">Default</span></span>        | <span data-ttu-id="6e8b5-277">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-277">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="6e8b5-278">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-278">Minimum system</span></span> | <span data-ttu-id="6e8b5-279">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-279">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a><span data-ttu-id="6e8b5-280">ConstructionEnabled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-280">ConstructionEnabled</span></span>



| <span data-ttu-id="6e8b5-281">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-281">Entry</span></span> | <span data-ttu-id="6e8b5-282">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-282">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-283">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-283">Description</span></span>    | <span data-ttu-id="6e8b5-284">Determina se ConstructorString viene passato all'oggetto quando viene costruito.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-284">Determines whether the ConstructorString is passed to the object when it is constructed.</span></span> |
| <span data-ttu-id="6e8b5-285">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-285">Access</span></span>         | <span data-ttu-id="6e8b5-286">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-286">ReadWrite</span></span>                                                                                |
| <span data-ttu-id="6e8b5-287">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-287">Type</span></span>           | <span data-ttu-id="6e8b5-288">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-288">Bool</span></span>                                                                                     |
| <span data-ttu-id="6e8b5-289">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-289">Default</span></span>        | <span data-ttu-id="6e8b5-290">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-290">False</span></span>                                                                                    |
| <span data-ttu-id="6e8b5-291">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-291">Minimum system</span></span> | <span data-ttu-id="6e8b5-292">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-292">Windows 2000</span></span>                                                                             |



 

### <a name="constructorstring"></a><span data-ttu-id="6e8b5-293">ConstructorString</span><span class="sxs-lookup"><span data-stu-id="6e8b5-293">ConstructorString</span></span>



| <span data-ttu-id="6e8b5-294">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-294">Entry</span></span> | <span data-ttu-id="6e8b5-295">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-295">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-296">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-296">Description</span></span>    | <span data-ttu-id="6e8b5-297">Stringa di inizializzazione per la costruzione di componenti.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-297">Initialization string for component construction.</span></span> <span data-ttu-id="6e8b5-298">È possibile creare oggetti diversi dallo stesso componente generico usando stringhe del costruttore di oggetti.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-298">You can create different objects from the same generic component by using object constructor strings.</span></span> <span data-ttu-id="6e8b5-299">Se ConstructionEnabled è false, questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-299">If ConstructionEnabled is False, this property is ignored.</span></span> |
| <span data-ttu-id="6e8b5-300">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-300">Access</span></span>         | <span data-ttu-id="6e8b5-301">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-301">ReadWrite</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="6e8b5-302">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-302">Type</span></span>           | <span data-ttu-id="6e8b5-303">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-303">String</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="6e8b5-304">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-304">Default</span></span>        | <span data-ttu-id="6e8b5-305">""</span><span class="sxs-lookup"><span data-stu-id="6e8b5-305">""</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="6e8b5-306">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-306">Minimum system</span></span> | <span data-ttu-id="6e8b5-307">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-307">Windows 2000</span></span>                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a><span data-ttu-id="6e8b5-308">CreationTimeout</span><span class="sxs-lookup"><span data-stu-id="6e8b5-308">CreationTimeout</span></span>



| <span data-ttu-id="6e8b5-309">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-309">Entry</span></span> | <span data-ttu-id="6e8b5-310">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-310">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-311">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-311">Description</span></span>    | <span data-ttu-id="6e8b5-312">Quando si crea l'oggetto, numero di millisecondi prima che venga restituito un errore di timeout.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-312">When creating the object, number of milliseconds before a time-out error is returned.</span></span> <span data-ttu-id="6e8b5-313">Il timeout massimo è pari a 2147483647 millisecondi (circa 25 giorni).</span><span class="sxs-lookup"><span data-stu-id="6e8b5-313">The maximum time-out is 2147483647 milliseconds (about 25 days).</span></span> |
| <span data-ttu-id="6e8b5-314">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-314">Access</span></span>         | <span data-ttu-id="6e8b5-315">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-315">ReadWrite</span></span>                                                                                                                                              |
| <span data-ttu-id="6e8b5-316">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-316">Type</span></span>           | <span data-ttu-id="6e8b5-317">Long (0-2147483647)</span><span class="sxs-lookup"><span data-stu-id="6e8b5-317">Long (0-2147483647)</span></span>                                                                                                                                    |
| <span data-ttu-id="6e8b5-318">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-318">Default</span></span>        | <span data-ttu-id="6e8b5-319">0</span><span class="sxs-lookup"><span data-stu-id="6e8b5-319">0</span></span>                                                                                                                                                      |
| <span data-ttu-id="6e8b5-320">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-320">Minimum system</span></span> | <span data-ttu-id="6e8b5-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-321">Windows 2000</span></span>                                                                                                                                           |



 

### <a name="description"></a><span data-ttu-id="6e8b5-322">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-322">Description</span></span>



| <span data-ttu-id="6e8b5-323">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-323">Entry</span></span> | <span data-ttu-id="6e8b5-324">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-324">Value</span></span> |
|----------------|--------------------------|
| <span data-ttu-id="6e8b5-325">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-325">Description</span></span>    | <span data-ttu-id="6e8b5-326">Descrive il componente.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-326">Describes the component.</span></span> |
| <span data-ttu-id="6e8b5-327">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-327">Access</span></span>         | <span data-ttu-id="6e8b5-328">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-328">ReadWrite</span></span>                |
| <span data-ttu-id="6e8b5-329">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-329">Type</span></span>           | <span data-ttu-id="6e8b5-330">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-330">String</span></span>                   |
| <span data-ttu-id="6e8b5-331">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-331">Default</span></span>        | <span data-ttu-id="6e8b5-332">""</span><span class="sxs-lookup"><span data-stu-id="6e8b5-332">""</span></span>                       |
| <span data-ttu-id="6e8b5-333">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-333">Minimum system</span></span> | <span data-ttu-id="6e8b5-334">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-334">Windows 2000</span></span>             |



 

### <a name="dll"></a><span data-ttu-id="6e8b5-335">DLL</span><span class="sxs-lookup"><span data-stu-id="6e8b5-335">DLL</span></span>



| <span data-ttu-id="6e8b5-336">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-336">Entry</span></span> | <span data-ttu-id="6e8b5-337">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-337">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="6e8b5-338">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-338">Description</span></span>    | <span data-ttu-id="6e8b5-339">Nome e percorso del file contenente il componente.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-339">The name and path of the file containing the component.</span></span> |
| <span data-ttu-id="6e8b5-340">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-340">Access</span></span>         | <span data-ttu-id="6e8b5-341">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6e8b5-341">ReadOnly</span></span>                                                |
| <span data-ttu-id="6e8b5-342">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-342">Type</span></span>           | <span data-ttu-id="6e8b5-343">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-343">String</span></span>                                                  |
| <span data-ttu-id="6e8b5-344">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-344">Default</span></span>        | <span data-ttu-id="6e8b5-345">N/D</span><span class="sxs-lookup"><span data-stu-id="6e8b5-345">N/A</span></span>                                                     |
| <span data-ttu-id="6e8b5-346">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-346">Minimum system</span></span> | <span data-ttu-id="6e8b5-347">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-347">Windows 2000</span></span>                                            |



 

### <a name="eventtrackingenabled"></a><span data-ttu-id="6e8b5-348">EventTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-348">EventTrackingEnabled</span></span>



| <span data-ttu-id="6e8b5-349">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-349">Entry</span></span> | <span data-ttu-id="6e8b5-350">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-350">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-351">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-351">Description</span></span>    | <span data-ttu-id="6e8b5-352">Determina se gli eventi vengono rilevati.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-352">Determines whether events are tracked.</span></span> <span data-ttu-id="6e8b5-353">Gli eventi includono azioni come l'arresto dell'applicazione. creazione e rilascio di oggetti; riferimenti a oggetti, coerenza, attivazione e disattivazione; chiamate al metodo, restituzione ed eccezioni; avvio della transazione, preparazione al commit e interruzione; connessione, allocazione e riciclo del dispenser di risorse; allocazione e riciclo di thread.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-353">Events include actions such as application shutdown; object creation and release; object references, consistency, activation, and deactivation; method calls, returns, and exceptions; transaction startup, preparing to commit, and abort; resource dispenser connection, allocation, and recycling; thread allocation and recycling.</span></span> |
| <span data-ttu-id="6e8b5-354">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-354">Access</span></span>         | <span data-ttu-id="6e8b5-355">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-355">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="6e8b5-356">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-356">Type</span></span>           | <span data-ttu-id="6e8b5-357">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-357">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="6e8b5-358">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-358">Default</span></span>        | <span data-ttu-id="6e8b5-359">Vero</span><span class="sxs-lookup"><span data-stu-id="6e8b5-359">True</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="6e8b5-360">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-360">Minimum system</span></span> | <span data-ttu-id="6e8b5-361">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-361">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a><span data-ttu-id="6e8b5-362">P:System.EnterpriseServices.ExceptionClassAttribute.Value</span><span class="sxs-lookup"><span data-stu-id="6e8b5-362">ExceptionClass</span></span>



| <span data-ttu-id="6e8b5-363">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-363">Entry</span></span> | <span data-ttu-id="6e8b5-364">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-364">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-365">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-365">Description</span></span>    | <span data-ttu-id="6e8b5-366">Il CLSID, che può essere un GUID o una stringa del moniker, per attivare un programma alternativo durante il processo di gestione di un programma di componenti in coda con errori ripetuti.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-366">The CLSID, which can be a GUID or a moniker string, to activate an alternative program during the process of dealing with a repeatedly failing queued components program.</span></span> |
| <span data-ttu-id="6e8b5-367">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-367">Access</span></span>         | <span data-ttu-id="6e8b5-368">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-368">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="6e8b5-369">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-369">Type</span></span>           | <span data-ttu-id="6e8b5-370">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-370">String</span></span>                                                                                                                                                                    |
| <span data-ttu-id="6e8b5-371">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-371">Default</span></span>        | <span data-ttu-id="6e8b5-372">""</span><span class="sxs-lookup"><span data-stu-id="6e8b5-372">""</span></span>                                                                                                                                                                        |
| <span data-ttu-id="6e8b5-373">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-373">Minimum system</span></span> | <span data-ttu-id="6e8b5-374">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-374">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="fireinparallel"></a><span data-ttu-id="6e8b5-375">FireInParallel</span><span class="sxs-lookup"><span data-stu-id="6e8b5-375">FireInParallel</span></span>



| <span data-ttu-id="6e8b5-376">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-376">Entry</span></span> | <span data-ttu-id="6e8b5-377">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-377">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-378">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-378">Description</span></span>    | <span data-ttu-id="6e8b5-379">Consente di attivare gli eventi in parallelo se il componente è una classe di evento.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-379">Enables events to be fired in parallel if the component is an event class.</span></span> |
| <span data-ttu-id="6e8b5-380">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-380">Access</span></span>         | <span data-ttu-id="6e8b5-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-381">ReadWrite</span></span>                                                                  |
| <span data-ttu-id="6e8b5-382">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-382">Type</span></span>           | <span data-ttu-id="6e8b5-383">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-383">Bool</span></span>                                                                       |
| <span data-ttu-id="6e8b5-384">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-384">Default</span></span>        | <span data-ttu-id="6e8b5-385">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-385">False</span></span>                                                                      |
| <span data-ttu-id="6e8b5-386">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-386">Minimum system</span></span> | <span data-ttu-id="6e8b5-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-387">Windows 2000</span></span>                                                               |



 

### <a name="iisintrinsics"></a><span data-ttu-id="6e8b5-388">IISIntrinsics</span><span class="sxs-lookup"><span data-stu-id="6e8b5-388">IISIntrinsics</span></span>



| <span data-ttu-id="6e8b5-389">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-389">Entry</span></span> | <span data-ttu-id="6e8b5-390">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-391">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-391">Description</span></span>    | <span data-ttu-id="6e8b5-392">Consente il passaggio di proprietà di contesto IIS, ad esempio un oggetto sessione dell'applicazione o un oggetto sessione utente, nel contesto di questa classe.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-392">Enables passing of IIS context properties, such as an application session object or a user session object, into the context for this class.</span></span> |
| <span data-ttu-id="6e8b5-393">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-393">Access</span></span>         | <span data-ttu-id="6e8b5-394">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-394">ReadWrite</span></span>                                                                                                                                   |
| <span data-ttu-id="6e8b5-395">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-395">Type</span></span>           | <span data-ttu-id="6e8b5-396">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-396">Bool</span></span>                                                                                                                                        |
| <span data-ttu-id="6e8b5-397">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-397">Default</span></span>        | <span data-ttu-id="6e8b5-398">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-398">False</span></span>                                                                                                                                       |
| <span data-ttu-id="6e8b5-399">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-399">Minimum system</span></span> | <span data-ttu-id="6e8b5-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-400">Windows 2000</span></span>                                                                                                                                |



 

### <a name="initializeserverapplication"></a><span data-ttu-id="6e8b5-401">InitializeServerApplication</span><span class="sxs-lookup"><span data-stu-id="6e8b5-401">InitializeServerApplication</span></span>



| <span data-ttu-id="6e8b5-402">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-402">Entry</span></span> | <span data-ttu-id="6e8b5-403">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-403">Value</span></span> |
|----------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-404">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-404">Description</span></span>    | <span data-ttu-id="6e8b5-405">Indica se il componente viene utilizzato per inizializzare un'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-405">Indicates whether the component is used to initialize a server application.</span></span> |
| <span data-ttu-id="6e8b5-406">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-406">Access</span></span>         | <span data-ttu-id="6e8b5-407">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-407">ReadWrite</span></span>                                                                   |
| <span data-ttu-id="6e8b5-408">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-408">Type</span></span>           | <span data-ttu-id="6e8b5-409">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-409">Bool</span></span>                                                                        |
| <span data-ttu-id="6e8b5-410">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-410">Default</span></span>        | <span data-ttu-id="6e8b5-411">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-411">False</span></span>                                                                       |
| <span data-ttu-id="6e8b5-412">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-412">Minimum system</span></span> | <span data-ttu-id="6e8b5-413">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e8b5-413">Windows Server 2003</span></span>                                                         |



 

### <a name="isenabled"></a><span data-ttu-id="6e8b5-414">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-414">IsEnabled</span></span>



| <span data-ttu-id="6e8b5-415">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-415">Entry</span></span> | <span data-ttu-id="6e8b5-416">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-416">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-417">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-417">Description</span></span>    | <span data-ttu-id="6e8b5-418">False se l'applicazione o il componente COM+ è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-418">False if the COM+ application or component is disabled.</span></span> <span data-ttu-id="6e8b5-419">Se l'applicazione o il componente COM+ è abilitato, IsEnabled è true.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-419">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="6e8b5-420">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-420">Access</span></span>         | <span data-ttu-id="6e8b5-421">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-421">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="6e8b5-422">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-422">Type</span></span>           | <span data-ttu-id="6e8b5-423">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-423">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="6e8b5-424">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-424">Default</span></span>        | <span data-ttu-id="6e8b5-425">Vero</span><span class="sxs-lookup"><span data-stu-id="6e8b5-425">True</span></span>                                                                                                                        |
| <span data-ttu-id="6e8b5-426">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-426">Minimum system</span></span> | <span data-ttu-id="6e8b5-427">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6e8b5-427">Windows XP</span></span>                                                                                                                  |



 

### <a name="iseventclass"></a><span data-ttu-id="6e8b5-428">IsEventClass</span><span class="sxs-lookup"><span data-stu-id="6e8b5-428">IsEventClass</span></span>



| <span data-ttu-id="6e8b5-429">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-429">Entry</span></span> | <span data-ttu-id="6e8b5-430">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-430">Value</span></span> |
|----------------|----------------------------------------------------|
| <span data-ttu-id="6e8b5-431">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-431">Description</span></span>    | <span data-ttu-id="6e8b5-432">Indica se il componente è una classe di evento.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-432">Indicates whether the component is an event class.</span></span> |
| <span data-ttu-id="6e8b5-433">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-433">Access</span></span>         | <span data-ttu-id="6e8b5-434">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6e8b5-434">ReadOnly</span></span>                                           |
| <span data-ttu-id="6e8b5-435">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-435">Type</span></span>           | <span data-ttu-id="6e8b5-436">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-436">Bool</span></span>                                               |
| <span data-ttu-id="6e8b5-437">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-437">Default</span></span>        | <span data-ttu-id="6e8b5-438">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-438">False</span></span>                                              |
| <span data-ttu-id="6e8b5-439">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-439">Minimum system</span></span> | <span data-ttu-id="6e8b5-440">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-440">Windows 2000</span></span>                                       |



 

### <a name="isinstalled"></a><span data-ttu-id="6e8b5-441">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-441">IsInstalled</span></span>



| <span data-ttu-id="6e8b5-442">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-442">Entry</span></span> | <span data-ttu-id="6e8b5-443">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-443">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="6e8b5-444">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-444">Description</span></span>    | <span data-ttu-id="6e8b5-445">Indica se il componente è installato in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-445">Indicates whether the component is installed in an application.</span></span> |
| <span data-ttu-id="6e8b5-446">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-446">Access</span></span>         | <span data-ttu-id="6e8b5-447">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6e8b5-447">ReadOnly</span></span>                                                        |
| <span data-ttu-id="6e8b5-448">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-448">Type</span></span>           | <span data-ttu-id="6e8b5-449">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-449">Bool</span></span>                                                            |
| <span data-ttu-id="6e8b5-450">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-450">Default</span></span>        | <span data-ttu-id="6e8b5-451">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-451">False</span></span>                                                           |
| <span data-ttu-id="6e8b5-452">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-452">Minimum system</span></span> | <span data-ttu-id="6e8b5-453">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e8b5-453">Windows Server 2003</span></span>                                             |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="6e8b5-454">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="6e8b5-454">IsPrivateComponent</span></span>



| <span data-ttu-id="6e8b5-455">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-455">Entry</span></span> | <span data-ttu-id="6e8b5-456">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-456">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-457">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-457">Description</span></span>    | <span data-ttu-id="6e8b5-458">Determina se un'applicazione server è un componente privato.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-458">Determines whether a server application is a private component.</span></span> <span data-ttu-id="6e8b5-459">Un componente privato in un'applicazione server può essere attivato solo dall'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-459">A private component in a server application can be activated only from within the application.</span></span> <span data-ttu-id="6e8b5-460">Se, ad esempio, si chiama [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) su un componente privato, l'operazione non riesce da out-of-process ma ha esito positivo in-process.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-460">For example, if you call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) on a private component, it fails from out-of-process but succeeds in-process.</span></span> <span data-ttu-id="6e8b5-461">Al contrario, se si chiama **CoCreateInstance** su un componente pubblico, l'operazione ha esito positivo sia in-process che out-of-process.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-461">In contrast, if you call **CoCreateInstance** on a public component, it succeeds both in-process and out-of-process.</span></span> |
| <span data-ttu-id="6e8b5-462">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-462">Access</span></span>         | <span data-ttu-id="6e8b5-463">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-463">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="6e8b5-464">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-464">Type</span></span>           | <span data-ttu-id="6e8b5-465">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-465">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6e8b5-466">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-466">Default</span></span>        | <span data-ttu-id="6e8b5-467">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-467">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="6e8b5-468">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-468">Minimum system</span></span> | <span data-ttu-id="6e8b5-469">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6e8b5-469">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a><span data-ttu-id="6e8b5-470">JustInTimeActivation</span><span class="sxs-lookup"><span data-stu-id="6e8b5-470">JustInTimeActivation</span></span>



| <span data-ttu-id="6e8b5-471">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-471">Entry</span></span> | <span data-ttu-id="6e8b5-472">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-472">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-473">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-473">Description</span></span>    | <span data-ttu-id="6e8b5-474">Determina se l' [attivazione JIT](enabling-jit-activation-for-a-component.md) è abilitata per il componente.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-474">Determines whether [JIT activation](enabling-jit-activation-for-a-component.md) is enabled for the component.</span></span> <span data-ttu-id="6e8b5-475">Questa proprietà è impostata su true quando il [supporto delle transazioni](setting-the-transaction-attribute.md) è impostato su Required, richiede New o supported.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-475">This property is set to True when [transaction support](setting-the-transaction-attribute.md) is set to Required, Requires New, or Supported.</span></span> <span data-ttu-id="6e8b5-476">Quando JustInTimeActivation è impostato su true, il [supporto della sincronizzazione](setting-the-synchronization-attribute.md) deve essere impostato su Required (impostazione predefinita) o richiede New.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-476">When JustInTimeActivation is set to True, [synchronization support](setting-the-synchronization-attribute.md) must be set to Required (the default) or Requires New.</span></span> |
| <span data-ttu-id="6e8b5-477">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-477">Access</span></span>         | <span data-ttu-id="6e8b5-478">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-478">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6e8b5-479">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-479">Type</span></span>           | <span data-ttu-id="6e8b5-480">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-480">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="6e8b5-481">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-481">Default</span></span>        | <span data-ttu-id="6e8b5-482">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-482">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="6e8b5-483">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-483">Minimum system</span></span> | <span data-ttu-id="6e8b5-484">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-484">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a><span data-ttu-id="6e8b5-485">LoadBalancingSupported</span><span class="sxs-lookup"><span data-stu-id="6e8b5-485">LoadBalancingSupported</span></span>



| <span data-ttu-id="6e8b5-486">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-486">Entry</span></span> | <span data-ttu-id="6e8b5-487">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-487">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-488">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-488">Description</span></span>    | <span data-ttu-id="6e8b5-489">Se il servizio di bilanciamento del carico dei componenti è installato e abilitato nel server, determina se il componente partecipa al bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-489">If the component load balancing service is installed and enabled on the server, determines whether the component participates in load balancing.</span></span> |
| <span data-ttu-id="6e8b5-490">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-490">Access</span></span>         | <span data-ttu-id="6e8b5-491">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-491">ReadWrite</span></span>                                                                                                                                        |
| <span data-ttu-id="6e8b5-492">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-492">Type</span></span>           | <span data-ttu-id="6e8b5-493">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-493">Bool</span></span>                                                                                                                                             |
| <span data-ttu-id="6e8b5-494">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-494">Default</span></span>        | <span data-ttu-id="6e8b5-495">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-495">False</span></span>                                                                                                                                            |
| <span data-ttu-id="6e8b5-496">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-496">Minimum system</span></span> | <span data-ttu-id="6e8b5-497">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-497">Windows 2000</span></span>                                                                                                                                     |



 

### <a name="maxpoolsize"></a><span data-ttu-id="6e8b5-498">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="6e8b5-498">MaxPoolSize</span></span>



| <span data-ttu-id="6e8b5-499">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-499">Entry</span></span> | <span data-ttu-id="6e8b5-500">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-500">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="6e8b5-501">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-501">Description</span></span>    | <span data-ttu-id="6e8b5-502">Numero massimo di oggetti in pool.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-502">Maximum number of objects pooled.</span></span> |
| <span data-ttu-id="6e8b5-503">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-503">Access</span></span>         | <span data-ttu-id="6e8b5-504">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-504">ReadWrite</span></span>                         |
| <span data-ttu-id="6e8b5-505">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-505">Type</span></span>           | <span data-ttu-id="6e8b5-506">Long (1-1048576)</span><span class="sxs-lookup"><span data-stu-id="6e8b5-506">Long (1-1048576)</span></span>                  |
| <span data-ttu-id="6e8b5-507">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-507">Default</span></span>        | <span data-ttu-id="6e8b5-508">1048576</span><span class="sxs-lookup"><span data-stu-id="6e8b5-508">1048576</span></span>                           |
| <span data-ttu-id="6e8b5-509">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-509">Minimum system</span></span> | <span data-ttu-id="6e8b5-510">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-510">Windows 2000</span></span>                      |



 

### <a name="minpoolsize"></a><span data-ttu-id="6e8b5-511">MinPoolSize</span><span class="sxs-lookup"><span data-stu-id="6e8b5-511">MinPoolSize</span></span>



| <span data-ttu-id="6e8b5-512">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-512">Entry</span></span> | <span data-ttu-id="6e8b5-513">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-513">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="6e8b5-514">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-514">Description</span></span>    | <span data-ttu-id="6e8b5-515">Numero minimo di oggetti in pool.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-515">Minimum number of objects pooled.</span></span> |
| <span data-ttu-id="6e8b5-516">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-516">Access</span></span>         | <span data-ttu-id="6e8b5-517">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-517">ReadWrite</span></span>                         |
| <span data-ttu-id="6e8b5-518">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-518">Type</span></span>           | <span data-ttu-id="6e8b5-519">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="6e8b5-519">Long (0-1048576)</span></span>                  |
| <span data-ttu-id="6e8b5-520">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-520">Default</span></span>        | <span data-ttu-id="6e8b5-521">0</span><span class="sxs-lookup"><span data-stu-id="6e8b5-521">0</span></span>                                 |
| <span data-ttu-id="6e8b5-522">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-522">Minimum system</span></span> | <span data-ttu-id="6e8b5-523">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-523">Windows 2000</span></span>                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a><span data-ttu-id="6e8b5-524">MultiInterfacePublisherFilterCLSID</span><span class="sxs-lookup"><span data-stu-id="6e8b5-524">MultiInterfacePublisherFilterCLSID</span></span>



| <span data-ttu-id="6e8b5-525">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-525">Entry</span></span> | <span data-ttu-id="6e8b5-526">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-526">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-527">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-527">Description</span></span>    | <span data-ttu-id="6e8b5-528">CLSID per il filtro del server di pubblicazione utilizzato se il componente è una classe di evento.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-528">CLSID for the publisher filter used if the component is an event class.</span></span> |
| <span data-ttu-id="6e8b5-529">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-529">Access</span></span>         | <span data-ttu-id="6e8b5-530">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-530">ReadWrite</span></span>                                                               |
| <span data-ttu-id="6e8b5-531">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-531">Type</span></span>           | <span data-ttu-id="6e8b5-532">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-532">String</span></span>                                                                  |
| <span data-ttu-id="6e8b5-533">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-533">Default</span></span>        | <span data-ttu-id="6e8b5-534">N/D</span><span class="sxs-lookup"><span data-stu-id="6e8b5-534">N/A</span></span>                                                                     |
| <span data-ttu-id="6e8b5-535">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-535">Minimum system</span></span> | <span data-ttu-id="6e8b5-536">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-536">Windows 2000</span></span>                                                            |



 

### <a name="mustruninclientcontext"></a><span data-ttu-id="6e8b5-537">MustRunInClientContext</span><span class="sxs-lookup"><span data-stu-id="6e8b5-537">MustRunInClientContext</span></span>



| <span data-ttu-id="6e8b5-538">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-538">Entry</span></span> | <span data-ttu-id="6e8b5-539">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-539">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-540">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-540">Description</span></span>    | <span data-ttu-id="6e8b5-541">Indica che il componente deve essere attivato nel contesto del chiamante originale.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-541">Indicates that component must be activated in its original caller's context.</span></span> <span data-ttu-id="6e8b5-542">In caso contrario, l'attivazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-542">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="6e8b5-543">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-543">Access</span></span>         | <span data-ttu-id="6e8b5-544">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-544">ReadWrite</span></span>                                                                                                 |
| <span data-ttu-id="6e8b5-545">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-545">Type</span></span>           | <span data-ttu-id="6e8b5-546">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-546">Bool</span></span>                                                                                                      |
| <span data-ttu-id="6e8b5-547">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-547">Default</span></span>        | <span data-ttu-id="6e8b5-548">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-548">False</span></span>                                                                                                     |
| <span data-ttu-id="6e8b5-549">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-549">Minimum system</span></span> | <span data-ttu-id="6e8b5-550">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6e8b5-550">Windows XP</span></span>                                                                                                |



 

### <a name="mustrunindefaultcontext"></a><span data-ttu-id="6e8b5-551">MustRunInDefaultContext</span><span class="sxs-lookup"><span data-stu-id="6e8b5-551">MustRunInDefaultContext</span></span>



| <span data-ttu-id="6e8b5-552">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-552">Entry</span></span> | <span data-ttu-id="6e8b5-553">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-553">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-554">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-554">Description</span></span>    | <span data-ttu-id="6e8b5-555">Indica che il componente deve essere attivato nel contesto del chiamante predefinito.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-555">Indicates that the component must be activated in the default caller's context.</span></span> <span data-ttu-id="6e8b5-556">In caso contrario, l'attivazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-556">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="6e8b5-557">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-557">Access</span></span>         | <span data-ttu-id="6e8b5-558">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-558">ReadWrite</span></span>                                                                                                    |
| <span data-ttu-id="6e8b5-559">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-559">Type</span></span>           | <span data-ttu-id="6e8b5-560">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-560">Bool</span></span>                                                                                                         |
| <span data-ttu-id="6e8b5-561">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-561">Default</span></span>        | <span data-ttu-id="6e8b5-562">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-562">False</span></span>                                                                                                        |
| <span data-ttu-id="6e8b5-563">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-563">Minimum system</span></span> | <span data-ttu-id="6e8b5-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-564">Windows 2000</span></span>                                                                                                 |



 

### <a name="objectpoolingenabled"></a><span data-ttu-id="6e8b5-565">ObjectPoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="6e8b5-565">ObjectPoolingEnabled</span></span>



| <span data-ttu-id="6e8b5-566">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-566">Entry</span></span> | <span data-ttu-id="6e8b5-567">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-567">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-568">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-568">Description</span></span>    | <span data-ttu-id="6e8b5-569">Determina se il [pool di oggetti com+](com--object-pooling.md) è abilitato per il componente.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-569">Determines whether [COM+ object pooling](com--object-pooling.md) is enabled for the component.</span></span> |
| <span data-ttu-id="6e8b5-570">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-570">Access</span></span>         | <span data-ttu-id="6e8b5-571">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-571">ReadWrite</span></span>                                                                                       |
| <span data-ttu-id="6e8b5-572">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-572">Type</span></span>           | <span data-ttu-id="6e8b5-573">Bool</span><span class="sxs-lookup"><span data-stu-id="6e8b5-573">Bool</span></span>                                                                                            |
| <span data-ttu-id="6e8b5-574">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-574">Default</span></span>        | <span data-ttu-id="6e8b5-575">Falso</span><span class="sxs-lookup"><span data-stu-id="6e8b5-575">False</span></span>                                                                                           |
| <span data-ttu-id="6e8b5-576">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-576">Minimum system</span></span> | <span data-ttu-id="6e8b5-577">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-577">Windows 2000</span></span>                                                                                    |



 

### <a name="progid"></a><span data-ttu-id="6e8b5-578">ProgID</span><span class="sxs-lookup"><span data-stu-id="6e8b5-578">ProgID</span></span>



| <span data-ttu-id="6e8b5-579">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-579">Entry</span></span> | <span data-ttu-id="6e8b5-580">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-580">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-581">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-581">Description</span></span>    | <span data-ttu-id="6e8b5-582">Nome descrittivo usato per identificare il componente.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-582">A friendly name used for identifying the component.</span></span> <span data-ttu-id="6e8b5-583">Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-583">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="6e8b5-584">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-584">Access</span></span>         | <span data-ttu-id="6e8b5-585">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6e8b5-585">ReadOnly</span></span>                                                                                                                                                                              |
| <span data-ttu-id="6e8b5-586">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-586">Type</span></span>           | <span data-ttu-id="6e8b5-587">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-587">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="6e8b5-588">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-588">Default</span></span>        | <span data-ttu-id="6e8b5-589">N/D</span><span class="sxs-lookup"><span data-stu-id="6e8b5-589">N/A</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="6e8b5-590">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-590">Minimum system</span></span> | <span data-ttu-id="6e8b5-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-591">Windows 2000</span></span>                                                                                                                                                                          |



 

### <a name="publisherid"></a><span data-ttu-id="6e8b5-592">PublisherID</span><span class="sxs-lookup"><span data-stu-id="6e8b5-592">PublisherID</span></span>



| <span data-ttu-id="6e8b5-593">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-593">Entry</span></span> | <span data-ttu-id="6e8b5-594">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-594">Value</span></span> |
|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-595">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-595">Description</span></span>    | <span data-ttu-id="6e8b5-596">Identificatore per l'autore di eventi se il componente è una classe di evento.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-596">Identifier for the event publisher if the component is an event class.</span></span> |
| <span data-ttu-id="6e8b5-597">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-597">Access</span></span>         | <span data-ttu-id="6e8b5-598">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-598">ReadWrite</span></span>                                                              |
| <span data-ttu-id="6e8b5-599">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-599">Type</span></span>           | <span data-ttu-id="6e8b5-600">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-600">String</span></span>                                                                 |
| <span data-ttu-id="6e8b5-601">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-601">Default</span></span>        | <span data-ttu-id="6e8b5-602">""</span><span class="sxs-lookup"><span data-stu-id="6e8b5-602">""</span></span>                                                                     |
| <span data-ttu-id="6e8b5-603">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-603">Minimum system</span></span> | <span data-ttu-id="6e8b5-604">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-604">Windows 2000</span></span>                                                           |



 

### <a name="soapassemblyname"></a><span data-ttu-id="6e8b5-605">SoapAssemblyName</span><span class="sxs-lookup"><span data-stu-id="6e8b5-605">SoapAssemblyName</span></span>



| <span data-ttu-id="6e8b5-606">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-606">Entry</span></span> | <span data-ttu-id="6e8b5-607">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-607">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-608">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-608">Description</span></span>    | <span data-ttu-id="6e8b5-609">GUID che identifica l'assembly GAC eseguito quando il componente viene richiamato come servizio SOAP.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-609">A GUID identifying the GAC assembly that is run when the component is invoked as a SOAP service.</span></span> |
| <span data-ttu-id="6e8b5-610">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-610">Access</span></span>         | <span data-ttu-id="6e8b5-611">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-611">ReadWrite</span></span>                                                                                        |
| <span data-ttu-id="6e8b5-612">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-612">Type</span></span>           | <span data-ttu-id="6e8b5-613">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-613">String</span></span>                                                                                           |
| <span data-ttu-id="6e8b5-614">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-614">Default</span></span>        | <span data-ttu-id="6e8b5-615">NULL</span><span class="sxs-lookup"><span data-stu-id="6e8b5-615">NULL</span></span>                                                                                             |
| <span data-ttu-id="6e8b5-616">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-616">Minimum system</span></span> | <span data-ttu-id="6e8b5-617">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e8b5-617">Windows Server 2003</span></span>                                                                              |



 

### <a name="soaptypename"></a><span data-ttu-id="6e8b5-618">SoapTypeName</span><span class="sxs-lookup"><span data-stu-id="6e8b5-618">SoapTypeName</span></span>



| <span data-ttu-id="6e8b5-619">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-619">Entry</span></span> | <span data-ttu-id="6e8b5-620">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-620">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-621">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-621">Description</span></span>    | <span data-ttu-id="6e8b5-622">Nome del tipo gestito per un componente che può essere richiamato come servizio SOAP.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-622">The managed type name for a component that can be invoked as a SOAP service.</span></span> |
| <span data-ttu-id="6e8b5-623">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-623">Access</span></span>         | <span data-ttu-id="6e8b5-624">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-624">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="6e8b5-625">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-625">Type</span></span>           | <span data-ttu-id="6e8b5-626">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-626">String</span></span>                                                                       |
| <span data-ttu-id="6e8b5-627">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-627">Default</span></span>        | <span data-ttu-id="6e8b5-628">NULL</span><span class="sxs-lookup"><span data-stu-id="6e8b5-628">NULL</span></span>                                                                         |
| <span data-ttu-id="6e8b5-629">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-629">Minimum system</span></span> | <span data-ttu-id="6e8b5-630">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e8b5-630">Windows Server 2003</span></span>                                                          |



 

### <a name="synchronization"></a><span data-ttu-id="6e8b5-631">Sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-631">Synchronization</span></span>



| <span data-ttu-id="6e8b5-632">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-632">Entry</span></span> | <span data-ttu-id="6e8b5-633">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-633">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-634">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-634">Description</span></span>    | <span data-ttu-id="6e8b5-635">Determina la [sincronizzazione](setting-the-synchronization-attribute.md) delle chiamate per il componente.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-635">Determines call [synchronization](setting-the-synchronization-attribute.md) for the component.</span></span>                                                                                                     |
| <span data-ttu-id="6e8b5-636">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-636">Access</span></span>         | <span data-ttu-id="6e8b5-637">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-637">ReadWrite</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="6e8b5-638">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-638">Type</span></span>           | <span data-ttu-id="6e8b5-639">Valori lunghi possibili: COMAdminSynchronizationIgnored (0) COMAdminSynchronizationNone (1) COMAdminSynchronizationSupported (2) COMAdminSynchronizationRequired (3) COMAdminSynchronizationRequiresNew (4)</span><span class="sxs-lookup"><span data-stu-id="6e8b5-639">Long Possible values:COMAdminSynchronizationIgnored (0)COMAdminSynchronizationNone (1)COMAdminSynchronizationSupported (2)COMAdminSynchronizationRequired (3)COMAdminSynchronizationRequiresNew (4)</span></span> |
| <span data-ttu-id="6e8b5-640">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-640">Default</span></span>        | <span data-ttu-id="6e8b5-641">COMAdminSynchronizationIgnored (0)</span><span class="sxs-lookup"><span data-stu-id="6e8b5-641">COMAdminSynchronizationIgnored (0)</span></span>                                                                                                                                                                  |
| <span data-ttu-id="6e8b5-642">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-642">Minimum system</span></span> | <span data-ttu-id="6e8b5-643">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-643">Windows 2000</span></span>                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a><span data-ttu-id="6e8b5-644">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="6e8b5-644">ThreadingModel</span></span>



| <span data-ttu-id="6e8b5-645">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-645">Entry</span></span> | <span data-ttu-id="6e8b5-646">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-646">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-647">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-647">Description</span></span>    | <span data-ttu-id="6e8b5-648">Determina il modo in cui le istanze del componente vengono assegnate ai thread per l'esecuzione del metodo.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-648">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="6e8b5-649">I valori corrispondono ai modelli di threading COM.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-649">Values correspond to COM threading models.</span></span>                                                                                        |
| <span data-ttu-id="6e8b5-650">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-650">Access</span></span>         | <span data-ttu-id="6e8b5-651">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6e8b5-651">ReadOnly</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="6e8b5-652">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-652">Type</span></span>           | <span data-ttu-id="6e8b5-653">Valori lunghi possibili: COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) COMAdminThreadingModelNotSpecified (5)</span><span class="sxs-lookup"><span data-stu-id="6e8b5-653">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)COMAdminThreadingModelNotSpecified (5)</span></span> |
| <span data-ttu-id="6e8b5-654">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-654">Default</span></span>        | <span data-ttu-id="6e8b5-655">N/D</span><span class="sxs-lookup"><span data-stu-id="6e8b5-655">N/A</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="6e8b5-656">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-656">Minimum system</span></span> | <span data-ttu-id="6e8b5-657">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-657">Windows 2000</span></span>                                                                                                                                                                                                              |



 

### <a name="transaction"></a><span data-ttu-id="6e8b5-658">Transazione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-658">Transaction</span></span>



| <span data-ttu-id="6e8b5-659">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-659">Entry</span></span> | <span data-ttu-id="6e8b5-660">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-660">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-661">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-661">Description</span></span>    | <span data-ttu-id="6e8b5-662">Determina il modo in cui un componente supporta [le transazioni](setting-the-transaction-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="6e8b5-662">Determines how a component supports [transactions](setting-the-transaction-attribute.md).</span></span> <span data-ttu-id="6e8b5-663">Si consiglia di usare le costanti nell'enumerazione e non i valori numerici.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-663">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="6e8b5-664">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-664">Access</span></span>         | <span data-ttu-id="6e8b5-665">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-665">ReadWrite</span></span>                                                                                                                                                                              |
| <span data-ttu-id="6e8b5-666">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-666">Type</span></span>           | <span data-ttu-id="6e8b5-667">Valori lunghi possibili: COMAdminTransactionIgnored (0) COMAdminTransactionNone (1) COMAdminTransactionSupported (2) COMAdminTransactionRequired (3) COMAdminTransactionRequiresNew (4)</span><span class="sxs-lookup"><span data-stu-id="6e8b5-667">Long Possible values:COMAdminTransactionIgnored (0)COMAdminTransactionNone (1)COMAdminTransactionSupported (2)COMAdminTransactionRequired (3)COMAdminTransactionRequiresNew (4)</span></span>        |
| <span data-ttu-id="6e8b5-668">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-668">Default</span></span>        | <span data-ttu-id="6e8b5-669">COMAdminTransactionNone (1)</span><span class="sxs-lookup"><span data-stu-id="6e8b5-669">COMAdminTransactionNone (1)</span></span>                                                                                                                                                            |
| <span data-ttu-id="6e8b5-670">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-670">Minimum system</span></span> | <span data-ttu-id="6e8b5-671">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-671">Windows 2000</span></span>                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a><span data-ttu-id="6e8b5-672">Proprietà TxIsolationLevel</span><span class="sxs-lookup"><span data-stu-id="6e8b5-672">TxIsolationLevel</span></span>



| <span data-ttu-id="6e8b5-673">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-673">Entry</span></span> | <span data-ttu-id="6e8b5-674">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-674">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8b5-675">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-675">Description</span></span>    | <span data-ttu-id="6e8b5-676">Indica i livelli di isolamento delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-676">Indicates the transaction isolation levels.</span></span> <span data-ttu-id="6e8b5-677">Sono disponibili cinque livelli di isolamento: nessuno, Read uncommitted, Read Committed, Repeatable Read e serialized.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-677">There are five isolation levels: none, read uncommitted, read committed, repeatable read, and serialized.</span></span> <span data-ttu-id="6e8b5-678">Il livello di isolamento predefinito viene serializzato.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-678">The default isolation level is serialized.</span></span>                           |
| <span data-ttu-id="6e8b5-679">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-679">Access</span></span>         | <span data-ttu-id="6e8b5-680">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e8b5-680">ReadWrite</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="6e8b5-681">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-681">Type</span></span>           | <span data-ttu-id="6e8b5-682">Valori lunghi possibili: COMAdminTxIsolationLevelAny (0) COMAdminTxIsolationLevelReadUnCommitted (1) COMAdminTxIsolationLevelReadCommitted (2) COMAdminTxIsolationLevelRepeatableRead (3) COMAdminTxIsolationLevelSerializable (4)</span><span class="sxs-lookup"><span data-stu-id="6e8b5-682">Long Possible values:COMAdminTxIsolationLevelAny (0)COMAdminTxIsolationLevelReadUnCommitted (1)COMAdminTxIsolationLevelReadCommitted (2)COMAdminTxIsolationLevelRepeatableRead (3)COMAdminTxIsolationLevelSerializable (4)</span></span> |
| <span data-ttu-id="6e8b5-683">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-683">Default</span></span>        | <span data-ttu-id="6e8b5-684">COMAdminTxIsolationLevelSerializable (4)</span><span class="sxs-lookup"><span data-stu-id="6e8b5-684">COMAdminTxIsolationLevelSerializable (4)</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="6e8b5-685">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-685">Minimum system</span></span> | <span data-ttu-id="6e8b5-686">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6e8b5-686">Windows XP</span></span>                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a><span data-ttu-id="6e8b5-687">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="6e8b5-687">VersionBuild</span></span>



| <span data-ttu-id="6e8b5-688">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-688">Entry</span></span> | <span data-ttu-id="6e8b5-689">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-689">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="6e8b5-690">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-690">Description</span></span>    | <span data-ttu-id="6e8b5-691">Identificatore di compilazione della versione.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-691">Version build identifier.</span></span> |
| <span data-ttu-id="6e8b5-692">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-692">Access</span></span>         | <span data-ttu-id="6e8b5-693">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6e8b5-693">ReadOnly</span></span>                  |
| <span data-ttu-id="6e8b5-694">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-694">Type</span></span>           | <span data-ttu-id="6e8b5-695">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-695">String</span></span>                    |
| <span data-ttu-id="6e8b5-696">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-696">Default</span></span>        | <span data-ttu-id="6e8b5-697">""</span><span class="sxs-lookup"><span data-stu-id="6e8b5-697">""</span></span>                        |
| <span data-ttu-id="6e8b5-698">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-698">Minimum system</span></span> | <span data-ttu-id="6e8b5-699">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-699">Windows 2000</span></span>              |



 

### <a name="versionmajor"></a><span data-ttu-id="6e8b5-700">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="6e8b5-700">VersionMajor</span></span>



| <span data-ttu-id="6e8b5-701">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-701">Entry</span></span> | <span data-ttu-id="6e8b5-702">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-702">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="6e8b5-703">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-703">Description</span></span>    | <span data-ttu-id="6e8b5-704">Identificatore di versione.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-704">Version identifier.</span></span> |
| <span data-ttu-id="6e8b5-705">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-705">Access</span></span>         | <span data-ttu-id="6e8b5-706">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6e8b5-706">ReadOnly</span></span>            |
| <span data-ttu-id="6e8b5-707">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-707">Type</span></span>           | <span data-ttu-id="6e8b5-708">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-708">String</span></span>              |
| <span data-ttu-id="6e8b5-709">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-709">Default</span></span>        | <span data-ttu-id="6e8b5-710">""</span><span class="sxs-lookup"><span data-stu-id="6e8b5-710">""</span></span>                  |
| <span data-ttu-id="6e8b5-711">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-711">Minimum system</span></span> | <span data-ttu-id="6e8b5-712">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-712">Windows 2000</span></span>        |



 

### <a name="versionminor"></a><span data-ttu-id="6e8b5-713">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="6e8b5-713">VersionMinor</span></span>



| <span data-ttu-id="6e8b5-714">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-714">Entry</span></span> | <span data-ttu-id="6e8b5-715">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-715">Value</span></span> |
|----------------|-------------------------|
| <span data-ttu-id="6e8b5-716">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-716">Description</span></span>    | <span data-ttu-id="6e8b5-717">Identificatore secondario della versione.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-717">Version sub-identifier.</span></span> |
| <span data-ttu-id="6e8b5-718">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-718">Access</span></span>         | <span data-ttu-id="6e8b5-719">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6e8b5-719">ReadOnly</span></span>                |
| <span data-ttu-id="6e8b5-720">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-720">Type</span></span>           | <span data-ttu-id="6e8b5-721">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-721">String</span></span>                  |
| <span data-ttu-id="6e8b5-722">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-722">Default</span></span>        | <span data-ttu-id="6e8b5-723">""</span><span class="sxs-lookup"><span data-stu-id="6e8b5-723">""</span></span>                      |
| <span data-ttu-id="6e8b5-724">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-724">Minimum system</span></span> | <span data-ttu-id="6e8b5-725">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-725">Windows 2000</span></span>            |



 

### <a name="versionsubbuild"></a><span data-ttu-id="6e8b5-726">VersionSubBuild</span><span class="sxs-lookup"><span data-stu-id="6e8b5-726">VersionSubBuild</span></span>



| <span data-ttu-id="6e8b5-727">Voce</span><span class="sxs-lookup"><span data-stu-id="6e8b5-727">Entry</span></span> | <span data-ttu-id="6e8b5-728">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8b5-728">Value</span></span> |
|----------------|-------------------------------|
| <span data-ttu-id="6e8b5-729">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8b5-729">Description</span></span>    | <span data-ttu-id="6e8b5-730">Identificatore della sottocompilazione della versione.</span><span class="sxs-lookup"><span data-stu-id="6e8b5-730">Version sub-build identifier.</span></span> |
| <span data-ttu-id="6e8b5-731">Access</span><span class="sxs-lookup"><span data-stu-id="6e8b5-731">Access</span></span>         | <span data-ttu-id="6e8b5-732">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6e8b5-732">ReadOnly</span></span>                      |
| <span data-ttu-id="6e8b5-733">Type</span><span class="sxs-lookup"><span data-stu-id="6e8b5-733">Type</span></span>           | <span data-ttu-id="6e8b5-734">string</span><span class="sxs-lookup"><span data-stu-id="6e8b5-734">String</span></span>                        |
| <span data-ttu-id="6e8b5-735">Predefinito</span><span class="sxs-lookup"><span data-stu-id="6e8b5-735">Default</span></span>        | <span data-ttu-id="6e8b5-736">""</span><span class="sxs-lookup"><span data-stu-id="6e8b5-736">""</span></span>                            |
| <span data-ttu-id="6e8b5-737">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="6e8b5-737">Minimum system</span></span> | <span data-ttu-id="6e8b5-738">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6e8b5-738">Windows 2000</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="6e8b5-739">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e8b5-739">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e8b5-740">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="6e8b5-740">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
