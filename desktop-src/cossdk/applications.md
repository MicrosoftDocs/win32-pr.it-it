---
description: Contiene un oggetto per ogni applicazione COM+ installata nel computer locale. Le proprietà esposte da questi oggetti contengono tutte le impostazioni effettuate a livello di applicazione.
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: Raccolta di applicazioni
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 54f286ae393e67d9732e21bc40cbb0f9c46d8c63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127171"
---
# <a name="applications-collection"></a><span data-ttu-id="8585e-104">Raccolta di applicazioni</span><span class="sxs-lookup"><span data-stu-id="8585e-104">Applications collection</span></span>

<span data-ttu-id="8585e-105">Contiene un oggetto per ogni applicazione COM+ installata nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="8585e-105">Contains an object for each COM+ application installed on the local computer.</span></span> <span data-ttu-id="8585e-106">Le proprietà esposte da questi oggetti contengono tutte le impostazioni effettuate a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-106">The properties exposed by these objects hold all settings made at the application level.</span></span>

<span data-ttu-id="8585e-107">Per impostare le proprietà per i componenti all'interno di un'applicazione, utilizzare la raccolta [**componenti**](components.md) correlati.</span><span class="sxs-lookup"><span data-stu-id="8585e-107">You set properties for components within an application by using the related [**Components**](components.md) collection.</span></span> <span data-ttu-id="8585e-108">I ruoli vengono assegnati a un'applicazione tramite la raccolta di [**ruoli**](roles.md) correlati.</span><span class="sxs-lookup"><span data-stu-id="8585e-108">You assign roles to an application by using the related [**Roles**](roles.md) collection.</span></span>

<span data-ttu-id="8585e-109">Per installare i componenti in un'applicazione, usare i metodi sull'oggetto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="8585e-109">To install components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="8585e-110">Per installare un'applicazione da un file o per arrestare o esportare un'applicazione, usare anche i metodi sull'oggetto **COMAdminCatalog** .</span><span class="sxs-lookup"><span data-stu-id="8585e-110">To install an application from a file or to shut down or export an application, also use methods on the **COMAdminCatalog** object.</span></span> <span data-ttu-id="8585e-111">In caso contrario, per creare una nuova applicazione, è possibile aggiungere un oggetto alla raccolta di **applicazioni** .</span><span class="sxs-lookup"><span data-stu-id="8585e-111">Otherwise, to create a new application, you can add an object to the **Applications** collection.</span></span>

<span data-ttu-id="8585e-112">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="8585e-112">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="8585e-113">Membri</span><span class="sxs-lookup"><span data-stu-id="8585e-113">Members</span></span>

<span data-ttu-id="8585e-114">La raccolta **Applications** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="8585e-114">The **Applications** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="8585e-115">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="8585e-115">Related Collections</span></span>

<span data-ttu-id="8585e-116">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="8585e-116">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="8585e-117">**ApplicationInstances**</span><span class="sxs-lookup"><span data-stu-id="8585e-117">**ApplicationInstances**</span></span>](applicationinstances.md)
-   [<span data-ttu-id="8585e-118">**Componenti**</span><span class="sxs-lookup"><span data-stu-id="8585e-118">**Components**</span></span>](components.md)
-   [<span data-ttu-id="8585e-119">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="8585e-119">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="8585e-120">**LegacyComponents**</span><span class="sxs-lookup"><span data-stu-id="8585e-120">**LegacyComponents**</span></span>](legacycomponents.md)
-   [<span data-ttu-id="8585e-121">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="8585e-121">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="8585e-122">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="8585e-122">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="8585e-123">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="8585e-123">**Roles**</span></span>](roles.md)

<span data-ttu-id="8585e-124">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="8585e-124">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="8585e-125">**Partizioni**</span><span class="sxs-lookup"><span data-stu-id="8585e-125">**Partitions**</span></span>](partitions.md)
-   [<span data-ttu-id="8585e-126">**Radice**</span><span class="sxs-lookup"><span data-stu-id="8585e-126">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="8585e-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8585e-127">Properties</span></span>

<span data-ttu-id="8585e-128">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="8585e-128">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="8585e-129">3GigSupportEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-129">3GigSupportEnabled</span></span>](#3gigsupportenabled)
-   [<span data-ttu-id="8585e-130">AccessChecksLevel</span><span class="sxs-lookup"><span data-stu-id="8585e-130">AccessChecksLevel</span></span>](#accesscheckslevel)
-   [<span data-ttu-id="8585e-131">Activation</span><span class="sxs-lookup"><span data-stu-id="8585e-131">Activation</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="8585e-132">ApplicationAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-132">ApplicationAccessChecksEnabled</span></span>](#applicationaccesschecksenabled)
-   [<span data-ttu-id="8585e-133">ApplicationDirectory</span><span class="sxs-lookup"><span data-stu-id="8585e-133">ApplicationDirectory</span></span>](#applicationdirectory)
-   [<span data-ttu-id="8585e-134">ApplicationProxy</span><span class="sxs-lookup"><span data-stu-id="8585e-134">ApplicationProxy</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="8585e-135">ApplicationProxyServerName</span><span class="sxs-lookup"><span data-stu-id="8585e-135">ApplicationProxyServerName</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="8585e-136">AppPartitionID</span><span class="sxs-lookup"><span data-stu-id="8585e-136">AppPartitionID</span></span>](#apppartitionid)
-   [<span data-ttu-id="8585e-137">autenticazione</span><span class="sxs-lookup"><span data-stu-id="8585e-137">Authentication</span></span>](#authenticationcapability)
-   [<span data-ttu-id="8585e-138">AuthenticationCapability</span><span class="sxs-lookup"><span data-stu-id="8585e-138">AuthenticationCapability</span></span>](#authenticationcapability)
-   [<span data-ttu-id="8585e-139">Modificabili</span><span class="sxs-lookup"><span data-stu-id="8585e-139">Changeable</span></span>](#changeable)
-   [<span data-ttu-id="8585e-140">CommandLine</span><span class="sxs-lookup"><span data-stu-id="8585e-140">CommandLine</span></span>](#commandline)
-   [<span data-ttu-id="8585e-141">ConcurrentApps</span><span class="sxs-lookup"><span data-stu-id="8585e-141">ConcurrentApps</span></span>](#concurrentapps)
-   [<span data-ttu-id="8585e-142">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="8585e-142">CreatedBy</span></span>](#createdby)
-   [<span data-ttu-id="8585e-143">CRMEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-143">CRMEnabled</span></span>](#crmenabled)
-   [<span data-ttu-id="8585e-144">CRMLogFile</span><span class="sxs-lookup"><span data-stu-id="8585e-144">CRMLogFile</span></span>](#crmlogfile)
-   [<span data-ttu-id="8585e-145">Cancellabile</span><span class="sxs-lookup"><span data-stu-id="8585e-145">Deleteable</span></span>](#deleteable)
-   [<span data-ttu-id="8585e-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-146">Description</span></span>](#description)
-   [<span data-ttu-id="8585e-147">DumpEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-147">DumpEnabled</span></span>](#dumpenabled)
-   [<span data-ttu-id="8585e-148">DumpOnException</span><span class="sxs-lookup"><span data-stu-id="8585e-148">DumpOnException</span></span>](#dumponexception)
-   [<span data-ttu-id="8585e-149">DumpOnFailfast</span><span class="sxs-lookup"><span data-stu-id="8585e-149">DumpOnFailfast</span></span>](#dumponfailfast)
-   [<span data-ttu-id="8585e-150">DumpPath</span><span class="sxs-lookup"><span data-stu-id="8585e-150">DumpPath</span></span>](#dumppath)
-   [<span data-ttu-id="8585e-151">EventsEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-151">EventsEnabled</span></span>](#eventsenabled)
-   [<span data-ttu-id="8585e-152">ID</span><span class="sxs-lookup"><span data-stu-id="8585e-152">ID</span></span>](#applications-collection)
-   [<span data-ttu-id="8585e-153">Identità</span><span class="sxs-lookup"><span data-stu-id="8585e-153">Identity</span></span>](#identity)
-   [<span data-ttu-id="8585e-154">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="8585e-154">ImpersonationLevel</span></span>](#impersonationlevel)
-   [<span data-ttu-id="8585e-155">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-155">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="8585e-156">IsSystem</span><span class="sxs-lookup"><span data-stu-id="8585e-156">IsSystem</span></span>](#issystem)
-   [<span data-ttu-id="8585e-157">MaxDumpCount</span><span class="sxs-lookup"><span data-stu-id="8585e-157">MaxDumpCount</span></span>](#maxdumpcount)
-   [<span data-ttu-id="8585e-158">Nome</span><span class="sxs-lookup"><span data-stu-id="8585e-158">Name</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="8585e-159">Password</span><span class="sxs-lookup"><span data-stu-id="8585e-159">Password</span></span>](#password)
-   [<span data-ttu-id="8585e-160">QCAuthenticateMsgs</span><span class="sxs-lookup"><span data-stu-id="8585e-160">QCAuthenticateMsgs</span></span>](#qcauthenticatemsgs)
-   [<span data-ttu-id="8585e-161">QCListenerMaxThreads</span><span class="sxs-lookup"><span data-stu-id="8585e-161">QCListenerMaxThreads</span></span>](#qclistenermaxthreads)
-   [<span data-ttu-id="8585e-162">QueueListenerEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-162">QueueListenerEnabled</span></span>](#queuelistenerenabled)
-   [<span data-ttu-id="8585e-163">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-163">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="8585e-164">RecycleActivationLimit</span><span class="sxs-lookup"><span data-stu-id="8585e-164">RecycleActivationLimit</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="8585e-165">RecycleCallLimit</span><span class="sxs-lookup"><span data-stu-id="8585e-165">RecycleCallLimit</span></span>](#recyclecalllimit)
-   [<span data-ttu-id="8585e-166">RecycleExpirationTimeout</span><span class="sxs-lookup"><span data-stu-id="8585e-166">RecycleExpirationTimeout</span></span>](#recycleexpirationtimeout)
-   [<span data-ttu-id="8585e-167">RecycleLifetimeLimit</span><span class="sxs-lookup"><span data-stu-id="8585e-167">RecycleLifetimeLimit</span></span>](#recyclelifetimelimit)
-   [<span data-ttu-id="8585e-168">RecycleMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="8585e-168">RecycleMemoryLimit</span></span>](#recyclememorylimit)
-   [<span data-ttu-id="8585e-169">Replicabile</span><span class="sxs-lookup"><span data-stu-id="8585e-169">Replicable</span></span>](#replicable)
-   [<span data-ttu-id="8585e-170">RunForever</span><span class="sxs-lookup"><span data-stu-id="8585e-170">RunForever</span></span>](#runforever)
-   [<span data-ttu-id="8585e-171">ServiceName</span><span class="sxs-lookup"><span data-stu-id="8585e-171">ServiceName</span></span>](#servicename)
-   [<span data-ttu-id="8585e-172">ShutdownAfter</span><span class="sxs-lookup"><span data-stu-id="8585e-172">ShutdownAfter</span></span>](#shutdownafter)
-   [<span data-ttu-id="8585e-173">SoapActivated</span><span class="sxs-lookup"><span data-stu-id="8585e-173">SoapActivated</span></span>](#soapactivated)
-   [<span data-ttu-id="8585e-174">SoapBaseUrl</span><span class="sxs-lookup"><span data-stu-id="8585e-174">SoapBaseUrl</span></span>](#soapbaseurl)
-   [<span data-ttu-id="8585e-175">SoapMailTo</span><span class="sxs-lookup"><span data-stu-id="8585e-175">SoapMailTo</span></span>](#soapmailto)
-   [<span data-ttu-id="8585e-176">SoapVRoot</span><span class="sxs-lookup"><span data-stu-id="8585e-176">SoapVRoot</span></span>](#soapvroot)
-   [<span data-ttu-id="8585e-177">SRPEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-177">SRPEnabled</span></span>](#srpenabled)
-   [<span data-ttu-id="8585e-178">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="8585e-178">SRPTrustLevel</span></span>](#srptrustlevel)

### <a name="3gigsupportenabled"></a><span data-ttu-id="8585e-179">3GigSupportEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-179">3GigSupportEnabled</span></span>



| <span data-ttu-id="8585e-180">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-180">Entry</span></span> | <span data-ttu-id="8585e-181">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-181">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-182">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-182">Description</span></span>    | <span data-ttu-id="8585e-183">Indica se l'applicazione può utilizzare 3 GB di memoria nel processo.</span><span class="sxs-lookup"><span data-stu-id="8585e-183">Indicates whether the application can use 3 GB of memory in its process.</span></span> <span data-ttu-id="8585e-184">Se questa funzionalità non è abilitata, l'applicazione può utilizzare solo 2 GB di memoria.</span><span class="sxs-lookup"><span data-stu-id="8585e-184">If this is not enabled, the application can use only 2 GB of memory.</span></span> |
| <span data-ttu-id="8585e-185">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-185">Access</span></span>         | <span data-ttu-id="8585e-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-186">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="8585e-187">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-187">Type</span></span>           | <span data-ttu-id="8585e-188">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-188">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="8585e-189">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-189">Default</span></span>        | <span data-ttu-id="8585e-190">Falso</span><span class="sxs-lookup"><span data-stu-id="8585e-190">False</span></span>                                                                                                                                         |
| <span data-ttu-id="8585e-191">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-191">Minimum system</span></span> | <span data-ttu-id="8585e-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-192">Windows 2000</span></span>                                                                                                                                  |



 

### <a name="accesscheckslevel"></a><span data-ttu-id="8585e-193">AccessChecksLevel</span><span class="sxs-lookup"><span data-stu-id="8585e-193">AccessChecksLevel</span></span>



| <span data-ttu-id="8585e-194">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-194">Entry</span></span> | <span data-ttu-id="8585e-195">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-195">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-196">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-196">Description</span></span>    | <span data-ttu-id="8585e-197">Indica se i controlli di accesso vengono eseguiti solo a livello di processo o a livello di processo e di componente.</span><span class="sxs-lookup"><span data-stu-id="8585e-197">Indicates whether access checks are performed at only the process level or at both the process and component level.</span></span> <span data-ttu-id="8585e-198">Si consiglia di usare le costanti nell'enumerazione e non i valori numerici.</span><span class="sxs-lookup"><span data-stu-id="8585e-198">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="8585e-199">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-199">Access</span></span>         | <span data-ttu-id="8585e-200">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-200">ReadWrite</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="8585e-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-201">Type</span></span>           | <span data-ttu-id="8585e-202">Valori possibili lunghi: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)</span><span class="sxs-lookup"><span data-stu-id="8585e-202">Long Possible values: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                |
| <span data-ttu-id="8585e-203">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-203">Default</span></span>        | <span data-ttu-id="8585e-204">COMAdminAccessChecksApplicationComponentLevel (1)</span><span class="sxs-lookup"><span data-stu-id="8585e-204">COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                                                                               |
| <span data-ttu-id="8585e-205">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-205">Minimum system</span></span> | <span data-ttu-id="8585e-206">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-206">Windows 2000</span></span>                                                                                                                                                                                                    |



 

### <a name="activation"></a><span data-ttu-id="8585e-207">Activation</span><span class="sxs-lookup"><span data-stu-id="8585e-207">Activation</span></span>



| <span data-ttu-id="8585e-208">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-208">Entry</span></span> | <span data-ttu-id="8585e-209">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-209">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-210">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-210">Description</span></span>    | <span data-ttu-id="8585e-211">L'attivazione locale indica che gli oggetti all'interno dell'applicazione vengono eseguiti in un processo server locale dedicato (applicazione server).</span><span class="sxs-lookup"><span data-stu-id="8585e-211">Local activation indicates that objects within the application run within a dedicated local server process (server application).</span></span> <span data-ttu-id="8585e-212">L'attivazione in-process indica che gli oggetti vengono eseguiti nel processo del creatore (applicazione libreria).</span><span class="sxs-lookup"><span data-stu-id="8585e-212">In-process activation indicates that objects run in their creator's process (library application).</span></span> |
| <span data-ttu-id="8585e-213">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-213">Access</span></span>         | <span data-ttu-id="8585e-214">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-214">ReadWrite</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="8585e-215">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-215">Type</span></span>           | <span data-ttu-id="8585e-216">Valori possibili lunghi: COMAdminActivationInproc (0) COMAdminActivationLocal (1)</span><span class="sxs-lookup"><span data-stu-id="8585e-216">Long Possible values:COMAdminActivationInproc (0)COMAdminActivationLocal (1)</span></span>                                                                                                                                                        |
| <span data-ttu-id="8585e-217">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-217">Default</span></span>        | <span data-ttu-id="8585e-218">COMAdminActivationLocal (1)</span><span class="sxs-lookup"><span data-stu-id="8585e-218">COMAdminActivationLocal (1)</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="8585e-219">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-219">Minimum system</span></span> | <span data-ttu-id="8585e-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-220">Windows 2000</span></span>                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a><span data-ttu-id="8585e-221">ApplicationAccessChecksEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-221">ApplicationAccessChecksEnabled</span></span>



| <span data-ttu-id="8585e-222">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-222">Entry</span></span> | <span data-ttu-id="8585e-223">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-223">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-224">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-224">Description</span></span>    | <span data-ttu-id="8585e-225">Indica se vengono eseguiti controlli di accesso per l'applicazione quando i client effettuano chiamate al suo interno.</span><span class="sxs-lookup"><span data-stu-id="8585e-225">Indicates whether access checks are performed for the application when clients make calls into it.</span></span> |
| <span data-ttu-id="8585e-226">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-226">Access</span></span>         | <span data-ttu-id="8585e-227">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-227">ReadWrite</span></span>                                                                                          |
| <span data-ttu-id="8585e-228">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-228">Type</span></span>           | <span data-ttu-id="8585e-229">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-229">Bool</span></span>                                                                                               |
| <span data-ttu-id="8585e-230">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-230">Default</span></span>        | <span data-ttu-id="8585e-231">Vero</span><span class="sxs-lookup"><span data-stu-id="8585e-231">True</span></span>                                                                                               |
| <span data-ttu-id="8585e-232">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-232">Minimum system</span></span> | <span data-ttu-id="8585e-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-233">Windows 2000</span></span>                                                                                       |



 

### <a name="applicationdirectory"></a><span data-ttu-id="8585e-234">ApplicationDirectory</span><span class="sxs-lookup"><span data-stu-id="8585e-234">ApplicationDirectory</span></span>



| <span data-ttu-id="8585e-235">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-235">Entry</span></span> | <span data-ttu-id="8585e-236">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-236">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-237">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-237">Description</span></span>    | <span data-ttu-id="8585e-238">Percorso completo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-238">The full path to the application.</span></span> <span data-ttu-id="8585e-239">Queste informazioni sono necessarie per la configurazione di assembly side-by-Side (SxS).</span><span class="sxs-lookup"><span data-stu-id="8585e-239">This information is needed when you configure Side-by-Side (SxS) assemblies.</span></span> <span data-ttu-id="8585e-240">Gli assembly side-by-Side (SxS) consentono alle applicazioni ASP di specificare quale versione di una DLL di sistema supportata da SxS usare, ad esempio MSVCRT, MSXML, COMCTL, GDIPLUS e così via.</span><span class="sxs-lookup"><span data-stu-id="8585e-240">Side-by-side (SxS) assemblies allow ASP applications to specify which version of an SxS-supported system DLL to use, such as MSVCRT, MSXML, COMCTL, GDIPLUS, and so on.</span></span> <span data-ttu-id="8585e-241">Se, ad esempio, l'applicazione ASP si basa su MSVCRT versione 2,0, è possibile assicurarsi che l'applicazione utilizzi ancora MSVCRT versione 2,0 anche dopo l'applicazione dei Service Pack al server.</span><span class="sxs-lookup"><span data-stu-id="8585e-241">For example, if your ASP application relies on MSVCRT version 2.0, you can ensure that your application still uses MSVCRT version 2.0 even after service packs are applied to the server.</span></span> <span data-ttu-id="8585e-242">Qualsiasi nuova versione di MSVCRT è ancora installata nel computer, ma la versione 2,0 rimane e viene usata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-242">Any new version of MSVCRT is still installed on the computer, but version 2.0 remains and is used by your application.</span></span> <span data-ttu-id="8585e-243">Le DLL supportate da SxS sono archiviate in% WINDIR% \\ WinSxS.</span><span class="sxs-lookup"><span data-stu-id="8585e-243">SxS-supported DLLs are stored in %WINDIR%\\WinSxS.</span></span> |
| <span data-ttu-id="8585e-244">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-244">Access</span></span>         | <span data-ttu-id="8585e-245">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-245">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8585e-246">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-246">Type</span></span>           | <span data-ttu-id="8585e-247">string</span><span class="sxs-lookup"><span data-stu-id="8585e-247">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8585e-248">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-248">Default</span></span>        | <span data-ttu-id="8585e-249">""</span><span class="sxs-lookup"><span data-stu-id="8585e-249">""</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8585e-250">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-250">Minimum system</span></span> | <span data-ttu-id="8585e-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-251">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="8585e-252">È possibile utilizzare una sola versione di una DLL di sistema in qualsiasi pool di applicazioni, anche se questa funzionalità è configurabile a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-252">Only one version of a system DLL can be used in any application pool, even though this feature is configurable at the application level.</span></span> <span data-ttu-id="8585e-253">Se ad esempio l'applicazione App1 usa MSVCRT, la versione 2,5 e l'applicazione App2 usano MSVCRT, versione 2,4, App1 e App2 non devono trovarsi nello stesso pool di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="8585e-253">For example, if application App1 uses MSVCRT, version 2.5 and application App2 uses MSVCRT, version 2.4, then App1 and App2 should not be in the same application pool.</span></span> <span data-ttu-id="8585e-254">In caso affermativo, l'applicazione caricata per prima dispone della versione di MSVCRT caricata e l'altra applicazione viene forzata a utilizzarla finché le applicazioni non vengono scaricate.</span><span class="sxs-lookup"><span data-stu-id="8585e-254">If they are, the application that is loaded first has its version of MSVCRT loaded, and the other application is forced to use it until the applications are unloaded.</span></span>

 

<span data-ttu-id="8585e-255">Per ulteriori informazioni, vedere "assembly affiancati" nelle [modifiche apportate ai servizi com+ in IIS 6,0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="8585e-255">For more information, see "Side-by-Side Assemblies" in [Changes in COM+ Services in IIS 6.0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).</span></span>

### <a name="applicationproxy"></a><span data-ttu-id="8585e-256">ApplicationProxy</span><span class="sxs-lookup"><span data-stu-id="8585e-256">ApplicationProxy</span></span>



| <span data-ttu-id="8585e-257">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-257">Entry</span></span> | <span data-ttu-id="8585e-258">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-258">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="8585e-259">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-259">Description</span></span>    | <span data-ttu-id="8585e-260">Indica se l'applicazione è un proxy di applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-260">Indicates whether the application is an application proxy.</span></span> |
| <span data-ttu-id="8585e-261">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-261">Access</span></span>         | <span data-ttu-id="8585e-262">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8585e-262">ReadOnly</span></span>                                                   |
| <span data-ttu-id="8585e-263">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-263">Type</span></span>           | <span data-ttu-id="8585e-264">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-264">Bool</span></span>                                                       |
| <span data-ttu-id="8585e-265">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-265">Default</span></span>        | <span data-ttu-id="8585e-266">Falso</span><span class="sxs-lookup"><span data-stu-id="8585e-266">False</span></span>                                                      |
| <span data-ttu-id="8585e-267">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-267">Minimum system</span></span> | <span data-ttu-id="8585e-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-268">Windows 2000</span></span>                                               |



 

### <a name="applicationproxyservername"></a><span data-ttu-id="8585e-269">ApplicationProxyServerName</span><span class="sxs-lookup"><span data-stu-id="8585e-269">ApplicationProxyServerName</span></span>



| <span data-ttu-id="8585e-270">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-270">Entry</span></span> | <span data-ttu-id="8585e-271">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-271">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-272">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-272">Description</span></span>    | <span data-ttu-id="8585e-273">Nome del server remoto utilizzato per l'esportazione del proxy di applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-273">A remote server name used when exporting the application proxy.</span></span> <span data-ttu-id="8585e-274">Si tratta del nome del server a cui punta il proxy applicazione quando viene installato in un computer client.</span><span class="sxs-lookup"><span data-stu-id="8585e-274">It is this server name that the application proxy points to when it is installed on a client computer.</span></span> |
| <span data-ttu-id="8585e-275">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-275">Access</span></span>         | <span data-ttu-id="8585e-276">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-276">ReadWrite</span></span>                                                                                                                                                              |
| <span data-ttu-id="8585e-277">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-277">Type</span></span>           | <span data-ttu-id="8585e-278">string</span><span class="sxs-lookup"><span data-stu-id="8585e-278">String</span></span>                                                                                                                                                                 |
| <span data-ttu-id="8585e-279">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-279">Default</span></span>        | <span data-ttu-id="8585e-280">""</span><span class="sxs-lookup"><span data-stu-id="8585e-280">""</span></span>                                                                                                                                                                     |
| <span data-ttu-id="8585e-281">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-281">Minimum system</span></span> | <span data-ttu-id="8585e-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-282">Windows 2000</span></span>                                                                                                                                                           |



 

### <a name="apppartitionid"></a><span data-ttu-id="8585e-283">AppPartitionID</span><span class="sxs-lookup"><span data-stu-id="8585e-283">AppPartitionID</span></span>



| <span data-ttu-id="8585e-284">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-284">Entry</span></span> | <span data-ttu-id="8585e-285">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-285">Value</span></span> |
|----------------|---------------------------------------------------|
| <span data-ttu-id="8585e-286">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-286">Description</span></span>    | <span data-ttu-id="8585e-287">GUID che rappresenta l'ID della partizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-287">A GUID representing the application partition ID.</span></span> |
| <span data-ttu-id="8585e-288">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-288">Access</span></span>         | <span data-ttu-id="8585e-289">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8585e-289">ReadOnly</span></span>                                          |
| <span data-ttu-id="8585e-290">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-290">Type</span></span>           | <span data-ttu-id="8585e-291">string</span><span class="sxs-lookup"><span data-stu-id="8585e-291">String</span></span>                                            |
| <span data-ttu-id="8585e-292">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-292">Default</span></span>        | <Generated>                                 |
| <span data-ttu-id="8585e-293">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-293">Minimum system</span></span> | <span data-ttu-id="8585e-294">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8585e-294">Windows Server 2003</span></span>                               |



 

### <a name="authentication"></a><span data-ttu-id="8585e-295">Authentication</span><span class="sxs-lookup"><span data-stu-id="8585e-295">Authentication</span></span>



| <span data-ttu-id="8585e-296">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-296">Entry</span></span> | <span data-ttu-id="8585e-297">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-297">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-298">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-298">Description</span></span>    | <span data-ttu-id="8585e-299">Imposta il livello di autenticazione per le chiamate, con i valori corrispondenti alle impostazioni di autenticazione RPC (Remote Procedure Call).</span><span class="sxs-lookup"><span data-stu-id="8585e-299">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="8585e-300">Quando si sceglie COMAdminAuthenticationDefault, viene utilizzata l'impostazione nella proprietà DefaultAuthenticationLevel all'interno della raccolta [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="8585e-300">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="8585e-301">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-301">Access</span></span>         | <span data-ttu-id="8585e-302">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-302">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="8585e-303">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-303">Type</span></span>           | <span data-ttu-id="8585e-304">Valori lunghi possibili: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="8585e-304">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="8585e-305">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-305">Default</span></span>        | <span data-ttu-id="8585e-306">COMAdminAuthenticationPacket (4)</span><span class="sxs-lookup"><span data-stu-id="8585e-306">COMAdminAuthenticationPacket (4)</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8585e-307">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-307">Minimum system</span></span> | <span data-ttu-id="8585e-308">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-308">Windows 2000</span></span>                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> <span data-ttu-id="8585e-309">Per le applicazioni di libreria (in-process), le uniche impostazioni valide sono COMAdminAuthenticationDefault e COMAdminAuthenticationNone.</span><span class="sxs-lookup"><span data-stu-id="8585e-309">For library (in-process) applications, the only valid settings here are COMAdminAuthenticationDefault and COMAdminAuthenticationNone .</span></span> <span data-ttu-id="8585e-310">Si consiglia di usare le costanti nell'enumerazione e non i valori numerici.</span><span class="sxs-lookup"><span data-stu-id="8585e-310">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="authenticationcapability"></a><span data-ttu-id="8585e-311">AuthenticationCapability</span><span class="sxs-lookup"><span data-stu-id="8585e-311">AuthenticationCapability</span></span>



| <span data-ttu-id="8585e-312">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-312">Entry</span></span> | <span data-ttu-id="8585e-313">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-313">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-314">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-314">Description</span></span>    | <span data-ttu-id="8585e-315">Determina quale identità viene presentata quando vengono rappresentate le chiamate.</span><span class="sxs-lookup"><span data-stu-id="8585e-315">Determines what identity is presented when calls are impersonated.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="8585e-316">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-316">Access</span></span>         | <span data-ttu-id="8585e-317">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-317">ReadWrite</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="8585e-318">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-318">Type</span></span>           | <span data-ttu-id="8585e-319">Valori lunghi possibili: COMAdminAuthenticationCapabilitiesNone (0x0) COMAdminAuthenticationCapabilitiesSecureReference (0x2) COMAdminAuthenticationCapabilitiesStaticCloaking (0x20) COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span><span class="sxs-lookup"><span data-stu-id="8585e-319">Long Possible values:COMAdminAuthenticationCapabilitiesNone (0x0)COMAdminAuthenticationCapabilitiesSecureReference (0x2)COMAdminAuthenticationCapabilitiesStaticCloaking (0x20)COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span> |
| <span data-ttu-id="8585e-320">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-320">Default</span></span>        | <span data-ttu-id="8585e-321">COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span><span class="sxs-lookup"><span data-stu-id="8585e-321">COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span>                                                                                                                                                                                |
| <span data-ttu-id="8585e-322">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-322">Minimum system</span></span> | <span data-ttu-id="8585e-323">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-323">Windows 2000</span></span>                                                                                                                                                                                                                            |



 

### <a name="changeable"></a><span data-ttu-id="8585e-324">Modificabili</span><span class="sxs-lookup"><span data-stu-id="8585e-324">Changeable</span></span>



| <span data-ttu-id="8585e-325">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-325">Entry</span></span> | <span data-ttu-id="8585e-326">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-326">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-327">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-327">Description</span></span>    | <span data-ttu-id="8585e-328">Determina se le modifiche apportate alle impostazioni dell'applicazione o ai relativi componenti sono consentite, a livello di codice o tramite lo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="8585e-328">Determines whether changes to the application settings or those of its components are allowed, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="8585e-329">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-329">Access</span></span>         | <span data-ttu-id="8585e-330">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-330">ReadWrite</span></span>                                                                                                                                                                     |
| <span data-ttu-id="8585e-331">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-331">Type</span></span>           | <span data-ttu-id="8585e-332">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-332">Bool</span></span>                                                                                                                                                                          |
| <span data-ttu-id="8585e-333">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-333">Default</span></span>        | <span data-ttu-id="8585e-334">Vero</span><span class="sxs-lookup"><span data-stu-id="8585e-334">True</span></span>                                                                                                                                                                          |
| <span data-ttu-id="8585e-335">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-335">Minimum system</span></span> | <span data-ttu-id="8585e-336">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-336">Windows 2000</span></span>                                                                                                                                                                  |



 

### <a name="commandline"></a><span data-ttu-id="8585e-337">CommandLine</span><span class="sxs-lookup"><span data-stu-id="8585e-337">CommandLine</span></span>



| <span data-ttu-id="8585e-338">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-338">Entry</span></span> | <span data-ttu-id="8585e-339">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-339">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-340">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-340">Description</span></span>    | <span data-ttu-id="8585e-341">Stringa della riga di comando da utilizzare per il debug.</span><span class="sxs-lookup"><span data-stu-id="8585e-341">A command-line string for use in debugging.</span></span> <span data-ttu-id="8585e-342">L'applicazione può essere avviata in un debugger con la riga di comando specificata.</span><span class="sxs-lookup"><span data-stu-id="8585e-342">The application can be launched in a debugger with the specified command line.</span></span> |
| <span data-ttu-id="8585e-343">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-343">Access</span></span>         | <span data-ttu-id="8585e-344">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-344">ReadWrite</span></span>                                                                                                                  |
| <span data-ttu-id="8585e-345">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-345">Type</span></span>           | <span data-ttu-id="8585e-346">string</span><span class="sxs-lookup"><span data-stu-id="8585e-346">String</span></span>                                                                                                                     |
| <span data-ttu-id="8585e-347">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-347">Default</span></span>        | <span data-ttu-id="8585e-348">""</span><span class="sxs-lookup"><span data-stu-id="8585e-348">""</span></span>                                                                                                                         |
| <span data-ttu-id="8585e-349">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-349">Minimum system</span></span> | <span data-ttu-id="8585e-350">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-350">Windows 2000</span></span>                                                                                                               |



 

### <a name="concurrentapps"></a><span data-ttu-id="8585e-351">ConcurrentApps</span><span class="sxs-lookup"><span data-stu-id="8585e-351">ConcurrentApps</span></span>



| <span data-ttu-id="8585e-352">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-352">Entry</span></span> | <span data-ttu-id="8585e-353">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-353">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-354">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-354">Description</span></span>    | <span data-ttu-id="8585e-355">Specifica il numero massimo di applicazioni in pool che possono essere eseguite simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="8585e-355">Specifies the maximum number of poolable applications that can run concurrently.</span></span> |
| <span data-ttu-id="8585e-356">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-356">Access</span></span>         | <span data-ttu-id="8585e-357">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-357">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="8585e-358">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-358">Type</span></span>           | <span data-ttu-id="8585e-359">Long (1-1048576)</span><span class="sxs-lookup"><span data-stu-id="8585e-359">Long (1-1048576)</span></span>                                                                 |
| <span data-ttu-id="8585e-360">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-360">Default</span></span>        | <span data-ttu-id="8585e-361">1</span><span class="sxs-lookup"><span data-stu-id="8585e-361">1</span></span>                                                                                |
| <span data-ttu-id="8585e-362">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-362">Minimum system</span></span> | <span data-ttu-id="8585e-363">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-363">Windows XP</span></span>                                                                       |



 

### <a name="createdby"></a><span data-ttu-id="8585e-364">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="8585e-364">CreatedBy</span></span>



| <span data-ttu-id="8585e-365">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-365">Entry</span></span> | <span data-ttu-id="8585e-366">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-366">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="8585e-367">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-367">Description</span></span>    | <span data-ttu-id="8585e-368">Stringa informativa per descrivere chi ha creato l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-368">Informational string to describe who created the application.</span></span> |
| <span data-ttu-id="8585e-369">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-369">Access</span></span>         | <span data-ttu-id="8585e-370">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-370">ReadWrite</span></span>                                                     |
| <span data-ttu-id="8585e-371">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-371">Type</span></span>           | <span data-ttu-id="8585e-372">string</span><span class="sxs-lookup"><span data-stu-id="8585e-372">String</span></span>                                                        |
| <span data-ttu-id="8585e-373">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-373">Default</span></span>        | <span data-ttu-id="8585e-374">""</span><span class="sxs-lookup"><span data-stu-id="8585e-374">""</span></span>                                                            |
| <span data-ttu-id="8585e-375">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-375">Minimum system</span></span> | <span data-ttu-id="8585e-376">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-376">Windows 2000</span></span>                                                  |



 

### <a name="crmenabled"></a><span data-ttu-id="8585e-377">CRMEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-377">CRMEnabled</span></span>



| <span data-ttu-id="8585e-378">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-378">Entry</span></span> | <span data-ttu-id="8585e-379">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-379">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="8585e-380">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-380">Description</span></span>    | <span data-ttu-id="8585e-381">Determina se il Gestione risorse di compensazione è abilitato.</span><span class="sxs-lookup"><span data-stu-id="8585e-381">Determines whether the Compensating Resource Manager is enabled.</span></span> |
| <span data-ttu-id="8585e-382">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-382">Access</span></span>         | <span data-ttu-id="8585e-383">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-383">ReadWrite</span></span>                                                        |
| <span data-ttu-id="8585e-384">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-384">Type</span></span>           | <span data-ttu-id="8585e-385">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-385">Bool</span></span>                                                             |
| <span data-ttu-id="8585e-386">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-386">Default</span></span>        | <span data-ttu-id="8585e-387">Falso</span><span class="sxs-lookup"><span data-stu-id="8585e-387">False</span></span>                                                            |
| <span data-ttu-id="8585e-388">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-388">Minimum system</span></span> | <span data-ttu-id="8585e-389">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-389">Windows 2000</span></span>                                                     |



 

### <a name="crmlogfile"></a><span data-ttu-id="8585e-390">CRMLogFile</span><span class="sxs-lookup"><span data-stu-id="8585e-390">CRMLogFile</span></span>



| <span data-ttu-id="8585e-391">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-391">Entry</span></span> | <span data-ttu-id="8585e-392">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-392">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-393">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-393">Description</span></span>    | <span data-ttu-id="8585e-394">Nome e percorso del file per il mantenimento del log per il CRM (Compensating Resource Manager).</span><span class="sxs-lookup"><span data-stu-id="8585e-394">Name and path of file for keeping the log for the compensating resource manager (CRM).</span></span> |
| <span data-ttu-id="8585e-395">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-395">Access</span></span>         | <span data-ttu-id="8585e-396">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-396">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="8585e-397">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-397">Type</span></span>           | <span data-ttu-id="8585e-398">string</span><span class="sxs-lookup"><span data-stu-id="8585e-398">String</span></span>                                                                                 |
| <span data-ttu-id="8585e-399">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-399">Default</span></span>        | <span data-ttu-id="8585e-400">""</span><span class="sxs-lookup"><span data-stu-id="8585e-400">""</span></span>                                                                                     |
| <span data-ttu-id="8585e-401">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-401">Minimum system</span></span> | <span data-ttu-id="8585e-402">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-402">Windows 2000</span></span>                                                                           |



 

### <a name="deleteable"></a><span data-ttu-id="8585e-403">Cancellabile</span><span class="sxs-lookup"><span data-stu-id="8585e-403">Deleteable</span></span>



| <span data-ttu-id="8585e-404">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-404">Entry</span></span> | <span data-ttu-id="8585e-405">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-405">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-406">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-406">Description</span></span>    | <span data-ttu-id="8585e-407">Consente di specificare se l'applicazione può essere eliminata, a livello di codice o tramite lo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="8585e-407">Sets whether the application can be deleted, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="8585e-408">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-408">Access</span></span>         | <span data-ttu-id="8585e-409">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-409">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="8585e-410">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-410">Type</span></span>           | <span data-ttu-id="8585e-411">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-411">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="8585e-412">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-412">Default</span></span>        | <span data-ttu-id="8585e-413">Vero</span><span class="sxs-lookup"><span data-stu-id="8585e-413">True</span></span>                                                                                                                        |
| <span data-ttu-id="8585e-414">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-414">Minimum system</span></span> | <span data-ttu-id="8585e-415">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-415">Windows 2000</span></span>                                                                                                                |



 

### <a name="description"></a><span data-ttu-id="8585e-416">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-416">Description</span></span>



| <span data-ttu-id="8585e-417">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-417">Entry</span></span> | <span data-ttu-id="8585e-418">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-418">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="8585e-419">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-419">Description</span></span>    | <span data-ttu-id="8585e-420">Descrive l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-420">Describes the application.</span></span> |
| <span data-ttu-id="8585e-421">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-421">Access</span></span>         | <span data-ttu-id="8585e-422">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-422">ReadWrite</span></span>                  |
| <span data-ttu-id="8585e-423">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-423">Type</span></span>           | <span data-ttu-id="8585e-424">string</span><span class="sxs-lookup"><span data-stu-id="8585e-424">String</span></span>                     |
| <span data-ttu-id="8585e-425">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-425">Default</span></span>        | <span data-ttu-id="8585e-426">""</span><span class="sxs-lookup"><span data-stu-id="8585e-426">""</span></span>                         |
| <span data-ttu-id="8585e-427">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-427">Minimum system</span></span> | <span data-ttu-id="8585e-428">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-428">Windows 2000</span></span>               |



 

### <a name="dumpenabled"></a><span data-ttu-id="8585e-429">DumpEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-429">DumpEnabled</span></span>



| <span data-ttu-id="8585e-430">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-430">Entry</span></span> | <span data-ttu-id="8585e-431">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-431">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-432">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-432">Description</span></span>    | <span data-ttu-id="8585e-433">Consente di eseguire il dump dello stato di un'applicazione COM+ al momento dell'errore in una directory designata.</span><span class="sxs-lookup"><span data-stu-id="8585e-433">Enables the dump of the state of a COM+ application at the time of failure to a designated directory.</span></span> |
| <span data-ttu-id="8585e-434">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-434">Access</span></span>         | <span data-ttu-id="8585e-435">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-435">ReadWrite</span></span>                                                                                             |
| <span data-ttu-id="8585e-436">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-436">Type</span></span>           | <span data-ttu-id="8585e-437">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-437">Bool</span></span>                                                                                                  |
| <span data-ttu-id="8585e-438">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-438">Default</span></span>        | <span data-ttu-id="8585e-439">Falso</span><span class="sxs-lookup"><span data-stu-id="8585e-439">False</span></span>                                                                                                 |
| <span data-ttu-id="8585e-440">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-440">Minimum system</span></span> | <span data-ttu-id="8585e-441">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-441">Windows XP</span></span>                                                                                            |



 

> [!Note]  
> <span data-ttu-id="8585e-442">A partire da Windows Server 2003, solo gli amministratori dispongono di privilegi di accesso in lettura ai file di dump COM+.</span><span class="sxs-lookup"><span data-stu-id="8585e-442">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="dumponexception"></a><span data-ttu-id="8585e-443">DumpOnException</span><span class="sxs-lookup"><span data-stu-id="8585e-443">DumpOnException</span></span>



| <span data-ttu-id="8585e-444">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-444">Entry</span></span> | <span data-ttu-id="8585e-445">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-445">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-446">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-446">Description</span></span>    | <span data-ttu-id="8585e-447">Consente il dump dello stato di un'applicazione COM+ quando l'applicazione causa un'eccezione non gestita e viene terminata dal runtime COM+.</span><span class="sxs-lookup"><span data-stu-id="8585e-447">Enables the dump of the state of a COM+ application when the application causes an unhandled exception and is terminated by the COM+ runtime.</span></span> |
| <span data-ttu-id="8585e-448">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-448">Access</span></span>         | <span data-ttu-id="8585e-449">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-449">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="8585e-450">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-450">Type</span></span>           | <span data-ttu-id="8585e-451">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-451">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="8585e-452">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-452">Default</span></span>        | <span data-ttu-id="8585e-453">Falso</span><span class="sxs-lookup"><span data-stu-id="8585e-453">False</span></span>                                                                                                                                         |
| <span data-ttu-id="8585e-454">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-454">Minimum system</span></span> | <span data-ttu-id="8585e-455">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-455">Windows XP</span></span>                                                                                                                                    |



 

### <a name="dumponfailfast"></a><span data-ttu-id="8585e-456">DumpOnFailfast</span><span class="sxs-lookup"><span data-stu-id="8585e-456">DumpOnFailfast</span></span>



| <span data-ttu-id="8585e-457">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-457">Entry</span></span> | <span data-ttu-id="8585e-458">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-458">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-459">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-459">Description</span></span>    | <span data-ttu-id="8585e-460">Abilita il dump dello stato di un'applicazione COM+ in caso di errore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-460">Enables the dump of the state of a COM+ application when the application fails.</span></span> |
| <span data-ttu-id="8585e-461">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-461">Access</span></span>         | <span data-ttu-id="8585e-462">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-462">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="8585e-463">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-463">Type</span></span>           | <span data-ttu-id="8585e-464">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-464">Bool</span></span>                                                                            |
| <span data-ttu-id="8585e-465">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-465">Default</span></span>        | <span data-ttu-id="8585e-466">Falso</span><span class="sxs-lookup"><span data-stu-id="8585e-466">False</span></span>                                                                           |
| <span data-ttu-id="8585e-467">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-467">Minimum system</span></span> | <span data-ttu-id="8585e-468">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-468">Windows XP</span></span>                                                                      |



 

### <a name="dumppath"></a><span data-ttu-id="8585e-469">DumpPath</span><span class="sxs-lookup"><span data-stu-id="8585e-469">DumpPath</span></span>



| <span data-ttu-id="8585e-470">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-470">Entry</span></span> | <span data-ttu-id="8585e-471">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-471">Value</span></span> |
|----------------|--------------------------------------------------------------|
| <span data-ttu-id="8585e-472">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-472">Description</span></span>    | <span data-ttu-id="8585e-473">Percorso della directory in cui vengono salvati i file di dump.</span><span class="sxs-lookup"><span data-stu-id="8585e-473">The path of the directory in which the dump files are saved.</span></span> |
| <span data-ttu-id="8585e-474">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-474">Access</span></span>         | <span data-ttu-id="8585e-475">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-475">ReadWrite</span></span>                                                    |
| <span data-ttu-id="8585e-476">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-476">Type</span></span>           | <span data-ttu-id="8585e-477">string</span><span class="sxs-lookup"><span data-stu-id="8585e-477">String</span></span>                                                       |
| <span data-ttu-id="8585e-478">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-478">Default</span></span>        | <span data-ttu-id="8585e-479">"% SystemRoot% \\ system32 \\ com \\ "</span><span class="sxs-lookup"><span data-stu-id="8585e-479">"%systemroot%\\system32\\com\\dmp"</span></span>                           |
| <span data-ttu-id="8585e-480">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-480">Minimum system</span></span> | <span data-ttu-id="8585e-481">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-481">Windows XP</span></span>                                                   |



 

> [!Note]  
> <span data-ttu-id="8585e-482">A partire da Windows Server 2003, solo gli amministratori dispongono di privilegi di accesso in lettura ai file di dump COM+.</span><span class="sxs-lookup"><span data-stu-id="8585e-482">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="eventsenabled"></a><span data-ttu-id="8585e-483">EventsEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-483">EventsEnabled</span></span>



| <span data-ttu-id="8585e-484">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-484">Entry</span></span> | <span data-ttu-id="8585e-485">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-485">Value</span></span> |
|----------------|-----------------------------------------------------------|
| <span data-ttu-id="8585e-486">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-486">Description</span></span>    | <span data-ttu-id="8585e-487">Indica se gli eventi sono abilitati per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-487">Indicates whether events are enabled for the application.</span></span> |
| <span data-ttu-id="8585e-488">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-488">Access</span></span>         | <span data-ttu-id="8585e-489">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-489">ReadWrite</span></span>                                                 |
| <span data-ttu-id="8585e-490">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-490">Type</span></span>           | <span data-ttu-id="8585e-491">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-491">Bool</span></span>                                                      |
| <span data-ttu-id="8585e-492">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-492">Default</span></span>        | <span data-ttu-id="8585e-493">Vero</span><span class="sxs-lookup"><span data-stu-id="8585e-493">True</span></span>                                                      |
| <span data-ttu-id="8585e-494">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-494">Minimum system</span></span> | <span data-ttu-id="8585e-495">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-495">Windows 2000</span></span>                                              |



 

### <a name="id"></a><span data-ttu-id="8585e-496">ID</span><span class="sxs-lookup"><span data-stu-id="8585e-496">ID</span></span>



| <span data-ttu-id="8585e-497">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-497">Entry</span></span> | <span data-ttu-id="8585e-498">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-498">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-499">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-499">Description</span></span>    | <span data-ttu-id="8585e-500">GUID che rappresenta l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-500">A GUID representing the application.</span></span> <span data-ttu-id="8585e-501">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="8585e-501">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="8585e-502">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-502">Access</span></span>         | <span data-ttu-id="8585e-503">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="8585e-503">WriteOnce</span></span>                                                                                                                                                            |
| <span data-ttu-id="8585e-504">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-504">Type</span></span>           | <span data-ttu-id="8585e-505">string</span><span class="sxs-lookup"><span data-stu-id="8585e-505">String</span></span>                                                                                                                                                               |
| <span data-ttu-id="8585e-506">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-506">Default</span></span>        | <Generated>                                                                                                                                                    |
| <span data-ttu-id="8585e-507">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-507">Minimum system</span></span> | <span data-ttu-id="8585e-508">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-508">Windows 2000</span></span>                                                                                                                                                         |



 

### <a name="identity"></a><span data-ttu-id="8585e-509">Identità</span><span class="sxs-lookup"><span data-stu-id="8585e-509">Identity</span></span>



| <span data-ttu-id="8585e-510">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-510">Entry</span></span> | <span data-ttu-id="8585e-511">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-511">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-512">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-512">Description</span></span>    | <span data-ttu-id="8585e-513">Imposta l'identità del processo server per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-513">Sets the server process identity for the application.</span></span> <span data-ttu-id="8585e-514">Specificare un account utente valido o "utente interattivo" per fare in modo che l'applicazione presupponga l'identità dell'utente che ha eseguito l'accesso corrente.</span><span class="sxs-lookup"><span data-stu-id="8585e-514">Specify a valid user account or "Interactive User" to have the application assume the identity of the current logged-on user.</span></span> <span data-ttu-id="8585e-515">È inoltre possibile specificare le stringhe "NT Authority \\ LocalService", "NT Authority \\ NetworkService" e "NT Authority \\ System".</span><span class="sxs-lookup"><span data-stu-id="8585e-515">You can also specify the strings "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system".</span></span> <span data-ttu-id="8585e-516">La password predefinita per questi tre account è "" (stringa vuota).</span><span class="sxs-lookup"><span data-stu-id="8585e-516">The default password for these three accounts is "" (empty string).</span></span> |
| <span data-ttu-id="8585e-517">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-517">Access</span></span>         |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="8585e-518">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-518">Type</span></span>           |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="8585e-519">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-519">Default</span></span>        |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="8585e-520">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-520">Minimum system</span></span> | <span data-ttu-id="8585e-521">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-521">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="8585e-522">La proprietà Identity non è abilitata per le applicazioni di libreria, che vengono eseguite nel processo client.</span><span class="sxs-lookup"><span data-stu-id="8585e-522">The Identity property is not enabled for library applications, which run in the client process.</span></span>

<span data-ttu-id="8585e-523">È necessario impostare la proprietà password contemporaneamente a Identity, prima di usare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), perché la password e l'identità vengono convalidate prima di essere salvate.</span><span class="sxs-lookup"><span data-stu-id="8585e-523">The Password property should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="8585e-524">Se la password e l'identità non vengono sincronizzate, l'applicazione non può essere avviata finché non vengono reimpostati da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="8585e-524">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="impersonationlevel"></a><span data-ttu-id="8585e-525">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="8585e-525">ImpersonationLevel</span></span>



| <span data-ttu-id="8585e-526">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-526">Entry</span></span> | <span data-ttu-id="8585e-527">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-527">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-528">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-528">Description</span></span>    | <span data-ttu-id="8585e-529">Imposta il livello di rappresentazione usato per le chiamate effettuate ad altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="8585e-529">Sets impersonation level used for calls made to other applications.</span></span>                                                                                           |
| <span data-ttu-id="8585e-530">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-530">Access</span></span>         | <span data-ttu-id="8585e-531">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-531">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="8585e-532">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-532">Type</span></span>           | <span data-ttu-id="8585e-533">Valori lunghi possibili: COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4)</span><span class="sxs-lookup"><span data-stu-id="8585e-533">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="8585e-534">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-534">Default</span></span>        | <span data-ttu-id="8585e-535">COMAdminImpersonationImpersonate (3)</span><span class="sxs-lookup"><span data-stu-id="8585e-535">COMAdminImpersonationImpersonate (3)</span></span>                                                                                                                          |
| <span data-ttu-id="8585e-536">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-536">Minimum system</span></span> | <span data-ttu-id="8585e-537">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-537">Windows 2000</span></span>                                                                                                                                                  |



 

### <a name="isenabled"></a><span data-ttu-id="8585e-538">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-538">IsEnabled</span></span>



| <span data-ttu-id="8585e-539">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-539">Entry</span></span> | <span data-ttu-id="8585e-540">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-540">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-541">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-541">Description</span></span>    | <span data-ttu-id="8585e-542">Se l'applicazione o il componente COM+ è disabilitato, IsEnabled è false.</span><span class="sxs-lookup"><span data-stu-id="8585e-542">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="8585e-543">Se l'applicazione o il componente COM+ è abilitato, IsEnabled è true.</span><span class="sxs-lookup"><span data-stu-id="8585e-543">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="8585e-544">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-544">Access</span></span>         | <span data-ttu-id="8585e-545">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-545">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="8585e-546">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-546">Type</span></span>           | <span data-ttu-id="8585e-547">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-547">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="8585e-548">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-548">Default</span></span>        | <span data-ttu-id="8585e-549">Vero</span><span class="sxs-lookup"><span data-stu-id="8585e-549">True</span></span>                                                                                                                                      |
| <span data-ttu-id="8585e-550">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-550">Minimum system</span></span> | <span data-ttu-id="8585e-551">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-551">Windows XP</span></span>                                                                                                                                |



 

### <a name="issystem"></a><span data-ttu-id="8585e-552">IsSystem</span><span class="sxs-lookup"><span data-stu-id="8585e-552">IsSystem</span></span>



| <span data-ttu-id="8585e-553">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-553">Entry</span></span> | <span data-ttu-id="8585e-554">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-554">Value</span></span> |
|----------------|--------------------------------------|
| <span data-ttu-id="8585e-555">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-555">Description</span></span>    | <span data-ttu-id="8585e-556">Identifica le applicazioni di sistema COM+.</span><span class="sxs-lookup"><span data-stu-id="8585e-556">Identifies COM+ system applications.</span></span> |
| <span data-ttu-id="8585e-557">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-557">Access</span></span>         | <span data-ttu-id="8585e-558">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8585e-558">ReadOnly</span></span>                             |
| <span data-ttu-id="8585e-559">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-559">Type</span></span>           | <span data-ttu-id="8585e-560">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-560">Bool</span></span>                                 |
| <span data-ttu-id="8585e-561">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-561">Default</span></span>        | <span data-ttu-id="8585e-562">Falso</span><span class="sxs-lookup"><span data-stu-id="8585e-562">False</span></span>                                |
| <span data-ttu-id="8585e-563">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-563">Minimum system</span></span> | <span data-ttu-id="8585e-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-564">Windows 2000</span></span>                         |



 

### <a name="maxdumpcount"></a><span data-ttu-id="8585e-565">MaxDumpCount</span><span class="sxs-lookup"><span data-stu-id="8585e-565">MaxDumpCount</span></span>



| <span data-ttu-id="8585e-566">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-566">Entry</span></span> | <span data-ttu-id="8585e-567">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-567">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-568">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-568">Description</span></span>    | <span data-ttu-id="8585e-569">Indica il numero massimo di file da generare prima che si verifichi la sovrascrittura.</span><span class="sxs-lookup"><span data-stu-id="8585e-569">Indicates the maximum number of files to be generated before overwriting occurs.</span></span> |
| <span data-ttu-id="8585e-570">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-570">Access</span></span>         | <span data-ttu-id="8585e-571">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-571">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="8585e-572">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-572">Type</span></span>           | <span data-ttu-id="8585e-573">Long (1-200)</span><span class="sxs-lookup"><span data-stu-id="8585e-573">Long (1-200)</span></span>                                                                     |
| <span data-ttu-id="8585e-574">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-574">Default</span></span>        | <span data-ttu-id="8585e-575">5</span><span class="sxs-lookup"><span data-stu-id="8585e-575">5</span></span>                                                                                |
| <span data-ttu-id="8585e-576">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-576">Minimum system</span></span> | <span data-ttu-id="8585e-577">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-577">Windows XP</span></span>                                                                       |



 

### <a name="name"></a><span data-ttu-id="8585e-578">Nome</span><span class="sxs-lookup"><span data-stu-id="8585e-578">Name</span></span>



| <span data-ttu-id="8585e-579">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-579">Entry</span></span> | <span data-ttu-id="8585e-580">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-580">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-581">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-581">Description</span></span>    | <span data-ttu-id="8585e-582">Nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-582">The name of the application.</span></span> <span data-ttu-id="8585e-583">Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="8585e-583">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="8585e-584">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-584">Access</span></span>         | <span data-ttu-id="8585e-585">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-585">ReadWrite</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="8585e-586">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-586">Type</span></span>           | <span data-ttu-id="8585e-587">string</span><span class="sxs-lookup"><span data-stu-id="8585e-587">String</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="8585e-588">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-588">Default</span></span>        | <span data-ttu-id="8585e-589">"Nuova applicazione"</span><span class="sxs-lookup"><span data-stu-id="8585e-589">"New Application"</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="8585e-590">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-590">Minimum system</span></span> | <span data-ttu-id="8585e-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-591">Windows 2000</span></span>                                                                                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="8585e-592">I nomi univoci devono essere scelti per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="8585e-592">Unique names should be chosen for applications.</span></span> <span data-ttu-id="8585e-593">Se vengono create più applicazioni con lo stesso nome, può interferire con il riferimento alle applicazioni in base al nome, causando un comportamento imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="8585e-593">If multiple applications are created with the same name, it can interfere with referencing the applications by name, resulting in unpredictable behavior.</span></span>

 

### <a name="password"></a><span data-ttu-id="8585e-594">Password</span><span class="sxs-lookup"><span data-stu-id="8585e-594">Password</span></span>



| <span data-ttu-id="8585e-595">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-595">Entry</span></span> | <span data-ttu-id="8585e-596">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-596">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="8585e-597">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-597">Description</span></span>    | <span data-ttu-id="8585e-598">Imposta la password utilizzata dal processo server per accedere con l'identità.</span><span class="sxs-lookup"><span data-stu-id="8585e-598">Sets the password used by the server process to log on under the identity.</span></span> |
| <span data-ttu-id="8585e-599">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-599">Access</span></span>         | <span data-ttu-id="8585e-600">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="8585e-600">WriteOnly</span></span>                                                                  |
| <span data-ttu-id="8585e-601">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-601">Type</span></span>           | <span data-ttu-id="8585e-602">string</span><span class="sxs-lookup"><span data-stu-id="8585e-602">String</span></span>                                                                     |
| <span data-ttu-id="8585e-603">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-603">Default</span></span>        | <span data-ttu-id="8585e-604">""</span><span class="sxs-lookup"><span data-stu-id="8585e-604">""</span></span>                                                                         |
| <span data-ttu-id="8585e-605">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-605">Minimum system</span></span> | <span data-ttu-id="8585e-606">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-606">Windows 2000</span></span>                                                               |



 

<span data-ttu-id="8585e-607">È necessario impostare la password nello stesso momento dell'identità, prima di usare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), perché la password e l'identità vengono convalidate prima di essere salvate.</span><span class="sxs-lookup"><span data-stu-id="8585e-607">Password should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="8585e-608">Se la password e l'identità non vengono sincronizzate, l'applicazione non può essere avviata finché non vengono reimpostati da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="8585e-608">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="qcauthenticatemsgs"></a><span data-ttu-id="8585e-609">QCAuthenticateMsgs</span><span class="sxs-lookup"><span data-stu-id="8585e-609">QCAuthenticateMsgs</span></span>



| <span data-ttu-id="8585e-610">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-610">Entry</span></span> | <span data-ttu-id="8585e-611">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-611">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-612">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-612">Description</span></span>    | <span data-ttu-id="8585e-613">Indica in quali circostanze vengono autenticate le richieste accodate a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-613">Indicates under what circumstances queued requests to an application are authenticated.</span></span>                                                 |
| <span data-ttu-id="8585e-614">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-614">Access</span></span>         | <span data-ttu-id="8585e-615">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-615">ReadWrite</span></span>                                                                                                                               |
| <span data-ttu-id="8585e-616">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-616">Type</span></span>           | <span data-ttu-id="8585e-617">Valori lunghi possibili: COMAdminQCMessageAuthenticateSecureApps (0) COMAdminQCMessageAuthenticateOff (1) COMAdminQCMessageAuthenticateOn (2)</span><span class="sxs-lookup"><span data-stu-id="8585e-617">Long Possible values:COMAdminQCMessageAuthenticateSecureApps (0)COMAdminQCMessageAuthenticateOff (1)COMAdminQCMessageAuthenticateOn (2)</span></span> |
| <span data-ttu-id="8585e-618">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-618">Default</span></span>        | <span data-ttu-id="8585e-619">COMAdminQCMessageAuthenticateSecureApps (0)</span><span class="sxs-lookup"><span data-stu-id="8585e-619">COMAdminQCMessageAuthenticateSecureApps (0)</span></span>                                                                                             |
| <span data-ttu-id="8585e-620">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-620">Minimum system</span></span> | <span data-ttu-id="8585e-621">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-621">Windows XP</span></span>                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a><span data-ttu-id="8585e-622">QCListenerMaxThreads</span><span class="sxs-lookup"><span data-stu-id="8585e-622">QCListenerMaxThreads</span></span>



| <span data-ttu-id="8585e-623">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-623">Entry</span></span> | <span data-ttu-id="8585e-624">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-624">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-625">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-625">Description</span></span>    | <span data-ttu-id="8585e-626">Indica il numero massimo di thread di listener simultanei.</span><span class="sxs-lookup"><span data-stu-id="8585e-626">Indicates the maximum number of concurrent listener threads.</span></span> <span data-ttu-id="8585e-627">L'intervallo valido per questa proprietà è compreso tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="8585e-627">The valid range for this property is 0 to 1000.</span></span> <span data-ttu-id="8585e-628">Per un'applicazione appena creata, l'impostazione è derivata dall'algoritmo attualmente utilizzato per determinare il numero predefinito di thread del listener: 16 volte il numero di CPU nel server.</span><span class="sxs-lookup"><span data-stu-id="8585e-628">For a newly created application, the setting is derived from the algorithm currently used for determining the default number of listener threads: 16 times the number of CPUs in the server.</span></span> |
| <span data-ttu-id="8585e-629">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-629">Access</span></span>         | <span data-ttu-id="8585e-630">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-630">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="8585e-631">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-631">Type</span></span>           | <span data-ttu-id="8585e-632">Long (0-1000)</span><span class="sxs-lookup"><span data-stu-id="8585e-632">Long (0-1000)</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="8585e-633">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-633">Default</span></span>        | <span data-ttu-id="8585e-634">0</span><span class="sxs-lookup"><span data-stu-id="8585e-634">0</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8585e-635">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-635">Minimum system</span></span> | <span data-ttu-id="8585e-636">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-636">Windows XP</span></span>                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="8585e-637">Questa proprietà è disponibile anche con funzionalità di lettura/scrittura dalla scheda **Accodamento** dello strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="8585e-637">This property is also available with read/write capability from the **Queuing** tab of the Component Services administrative tool.</span></span>

 

### <a name="queuelistenerenabled"></a><span data-ttu-id="8585e-638">QueueListenerEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-638">QueueListenerEnabled</span></span>



| <span data-ttu-id="8585e-639">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-639">Entry</span></span> | <span data-ttu-id="8585e-640">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-640">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-641">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-641">Description</span></span>    | <span data-ttu-id="8585e-642">Indica se il listener dei componenti in coda è abilitato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-642">Indicates whether the queued components listener is enabled for the application.</span></span> <span data-ttu-id="8585e-643">Se abilitata, il listener viene avviato all'avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-643">If enabled, the listener is launched when the application starts.</span></span> <span data-ttu-id="8585e-644">Questa proprietà ha effetto solo se QueuingEnabled è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="8585e-644">This property takes effect only if QueuingEnabled is set to True.</span></span> |
| <span data-ttu-id="8585e-645">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-645">Access</span></span>         | <span data-ttu-id="8585e-646">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-646">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="8585e-647">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-647">Type</span></span>           | <span data-ttu-id="8585e-648">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-648">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="8585e-649">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-649">Default</span></span>        | <span data-ttu-id="8585e-650">Falso</span><span class="sxs-lookup"><span data-stu-id="8585e-650">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="8585e-651">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-651">Minimum system</span></span> | <span data-ttu-id="8585e-652">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-652">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a><span data-ttu-id="8585e-653">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-653">QueuingEnabled</span></span>



| <span data-ttu-id="8585e-654">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-654">Entry</span></span> | <span data-ttu-id="8585e-655">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-655">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-656">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-656">Description</span></span>    | <span data-ttu-id="8585e-657">Indica se il servizio COM+ Queued Components è abilitato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-657">Indicates whether the COM+ Queued Components service is enabled for the application.</span></span> |
| <span data-ttu-id="8585e-658">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-658">Access</span></span>         | <span data-ttu-id="8585e-659">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-659">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="8585e-660">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-660">Type</span></span>           | <span data-ttu-id="8585e-661">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-661">Bool</span></span>                                                                                 |
| <span data-ttu-id="8585e-662">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-662">Default</span></span>        | <span data-ttu-id="8585e-663">Falso</span><span class="sxs-lookup"><span data-stu-id="8585e-663">False</span></span>                                                                                |
| <span data-ttu-id="8585e-664">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-664">Minimum system</span></span> | <span data-ttu-id="8585e-665">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-665">Windows 2000</span></span>                                                                         |



 

### <a name="recycleactivationlimit"></a><span data-ttu-id="8585e-666">RecycleActivationLimit</span><span class="sxs-lookup"><span data-stu-id="8585e-666">RecycleActivationLimit</span></span>



| <span data-ttu-id="8585e-667">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-667">Entry</span></span> | <span data-ttu-id="8585e-668">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-668">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-669">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-669">Description</span></span>    | <span data-ttu-id="8585e-670">Indica il numero massimo di attivazioni di oggetti configurati nell'applicazione da accettare prima del riciclo del processo.</span><span class="sxs-lookup"><span data-stu-id="8585e-670">Indicates the maximum number of activations of configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="8585e-671">Il numero predefinito di attivazioni è 0.</span><span class="sxs-lookup"><span data-stu-id="8585e-671">The default number of activations is 0.</span></span> |
| <span data-ttu-id="8585e-672">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-672">Access</span></span>         | <span data-ttu-id="8585e-673">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-673">ReadWrite</span></span>                                                                                                                                                            |
| <span data-ttu-id="8585e-674">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-674">Type</span></span>           | <span data-ttu-id="8585e-675">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="8585e-675">Long (0-1048576)</span></span>                                                                                                                                                     |
| <span data-ttu-id="8585e-676">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-676">Default</span></span>        | <span data-ttu-id="8585e-677">0</span><span class="sxs-lookup"><span data-stu-id="8585e-677">0</span></span>                                                                                                                                                                    |
| <span data-ttu-id="8585e-678">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-678">Minimum system</span></span> | <span data-ttu-id="8585e-679">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-679">Windows XP</span></span>                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a><span data-ttu-id="8585e-680">RecycleCallLimit</span><span class="sxs-lookup"><span data-stu-id="8585e-680">RecycleCallLimit</span></span>



| <span data-ttu-id="8585e-681">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-681">Entry</span></span> | <span data-ttu-id="8585e-682">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-682">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-683">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-683">Description</span></span>    | <span data-ttu-id="8585e-684">Indica il numero massimo di chiamate che consentono agli oggetti configurati nell'applicazione di accettare prima di riciclare il processo.</span><span class="sxs-lookup"><span data-stu-id="8585e-684">Indicates the maximum number of calls to allow configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="8585e-685">Il numero predefinito di chiamate è 0.</span><span class="sxs-lookup"><span data-stu-id="8585e-685">The default number of calls is 0.</span></span> |
| <span data-ttu-id="8585e-686">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-686">Access</span></span>         | <span data-ttu-id="8585e-687">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-687">ReadWrite</span></span>                                                                                                                                                      |
| <span data-ttu-id="8585e-688">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-688">Type</span></span>           | <span data-ttu-id="8585e-689">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="8585e-689">Long (0-1048576)</span></span>                                                                                                                                               |
| <span data-ttu-id="8585e-690">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-690">Default</span></span>        | <span data-ttu-id="8585e-691">0</span><span class="sxs-lookup"><span data-stu-id="8585e-691">0</span></span>                                                                                                                                                              |
| <span data-ttu-id="8585e-692">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-692">Minimum system</span></span> | <span data-ttu-id="8585e-693">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-693">Windows XP</span></span>                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a><span data-ttu-id="8585e-694">RecycleExpirationTimeout</span><span class="sxs-lookup"><span data-stu-id="8585e-694">RecycleExpirationTimeout</span></span>



| <span data-ttu-id="8585e-695">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-695">Entry</span></span> | <span data-ttu-id="8585e-696">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-696">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-697">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-697">Description</span></span>    | <span data-ttu-id="8585e-698">Indica la quantità di tempo (in minuti) per consentire l'esecuzione di un processo riciclato prima di arrestarlo.</span><span class="sxs-lookup"><span data-stu-id="8585e-698">Indicates the amount of time (in minutes) to allow a recycled process to run before shutting it down.</span></span> <span data-ttu-id="8585e-699">Il conto alla rovescia inizia subito dopo il riciclo del processo.</span><span class="sxs-lookup"><span data-stu-id="8585e-699">The countdown begins immediately after the process is recycled.</span></span> <span data-ttu-id="8585e-700">Il timeout di scadenza massimo è di 1440 minuti (24 ore) e il valore predefinito è 15 minuti.</span><span class="sxs-lookup"><span data-stu-id="8585e-700">The maximum expiration time-out is 1440 minutes (24 hours), and the default is 15 minutes.</span></span> |
| <span data-ttu-id="8585e-701">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-701">Access</span></span>         | <span data-ttu-id="8585e-702">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-702">ReadWrite</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8585e-703">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-703">Type</span></span>           | <span data-ttu-id="8585e-704">Long (1-1440)</span><span class="sxs-lookup"><span data-stu-id="8585e-704">Long (1-1440)</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="8585e-705">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-705">Default</span></span>        | <span data-ttu-id="8585e-706">15</span><span class="sxs-lookup"><span data-stu-id="8585e-706">15</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8585e-707">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-707">Minimum system</span></span> | <span data-ttu-id="8585e-708">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-708">Windows XP</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a><span data-ttu-id="8585e-709">RecycleLifetimeLimit</span><span class="sxs-lookup"><span data-stu-id="8585e-709">RecycleLifetimeLimit</span></span>



| <span data-ttu-id="8585e-710">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-710">Entry</span></span> | <span data-ttu-id="8585e-711">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-711">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-712">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-712">Description</span></span>    | <span data-ttu-id="8585e-713">Indica il numero massimo di minuti per consentire l'esecuzione di un processo prima del riciclo.</span><span class="sxs-lookup"><span data-stu-id="8585e-713">Indicates the maximum number of minutes to allow a process to run before recycling it.</span></span> <span data-ttu-id="8585e-714">Il limite massimo di durata è di 30240 minuti (21 giorni) e il valore predefinito è 0 minuti.</span><span class="sxs-lookup"><span data-stu-id="8585e-714">The maximum lifetime limit is 30240 minutes (21 days), and the default is 0 minutes.</span></span> |
| <span data-ttu-id="8585e-715">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-715">Access</span></span>         | <span data-ttu-id="8585e-716">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-716">ReadWrite</span></span>                                                                                                                                                                   |
| <span data-ttu-id="8585e-717">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-717">Type</span></span>           | <span data-ttu-id="8585e-718">Long (0-30240)</span><span class="sxs-lookup"><span data-stu-id="8585e-718">Long (0-30240)</span></span>                                                                                                                                                              |
| <span data-ttu-id="8585e-719">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-719">Default</span></span>        | <span data-ttu-id="8585e-720">0</span><span class="sxs-lookup"><span data-stu-id="8585e-720">0</span></span>                                                                                                                                                                           |
| <span data-ttu-id="8585e-721">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-721">Minimum system</span></span> | <span data-ttu-id="8585e-722">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-722">Windows XP</span></span>                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a><span data-ttu-id="8585e-723">RecycleMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="8585e-723">RecycleMemoryLimit</span></span>



| <span data-ttu-id="8585e-724">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-724">Entry</span></span> | <span data-ttu-id="8585e-725">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-725">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-726">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-726">Description</span></span>    | <span data-ttu-id="8585e-727">Indica la quantità massima di utilizzo di memoria (in kilobyte) consentita prima che venga riciclata.</span><span class="sxs-lookup"><span data-stu-id="8585e-727">Indicates the maximum amount of memory usage (in kilobytes) allowed a process before it's recycled.</span></span> <span data-ttu-id="8585e-728">Se l'utilizzo della memoria del processo supera il numero specificato per un periodo più lungo di un minuto, il processo viene riciclato.</span><span class="sxs-lookup"><span data-stu-id="8585e-728">If the process memory usage exceeds the specified number for a period longer than one minute, the process is recycled.</span></span> <span data-ttu-id="8585e-729">La quantità predefinita di utilizzo della memoria è 0 KB.</span><span class="sxs-lookup"><span data-stu-id="8585e-729">The default amount of memory usage is 0 KB.</span></span> |
| <span data-ttu-id="8585e-730">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-730">Access</span></span>         | <span data-ttu-id="8585e-731">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-731">ReadWrite</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8585e-732">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-732">Type</span></span>           | <span data-ttu-id="8585e-733">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="8585e-733">Long (0-1048576)</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="8585e-734">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-734">Default</span></span>        | <span data-ttu-id="8585e-735">0</span><span class="sxs-lookup"><span data-stu-id="8585e-735">0</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8585e-736">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-736">Minimum system</span></span> | <span data-ttu-id="8585e-737">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-737">Windows XP</span></span>                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a><span data-ttu-id="8585e-738">Replicabile</span><span class="sxs-lookup"><span data-stu-id="8585e-738">Replicable</span></span>



| <span data-ttu-id="8585e-739">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-739">Entry</span></span> | <span data-ttu-id="8585e-740">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-740">Value</span></span> |
|----------------|------------------------------------------------------|
| <span data-ttu-id="8585e-741">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-741">Description</span></span>    | <span data-ttu-id="8585e-742">Indica se l'applicazione può essere replicata.</span><span class="sxs-lookup"><span data-stu-id="8585e-742">Indicates whether the application can be replicated.</span></span> |
| <span data-ttu-id="8585e-743">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-743">Access</span></span>         | <span data-ttu-id="8585e-744">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-744">ReadWrite</span></span>                                            |
| <span data-ttu-id="8585e-745">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-745">Type</span></span>           | <span data-ttu-id="8585e-746">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-746">Bool</span></span>                                                 |
| <span data-ttu-id="8585e-747">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-747">Default</span></span>        | <span data-ttu-id="8585e-748">Vero</span><span class="sxs-lookup"><span data-stu-id="8585e-748">True</span></span>                                                 |
| <span data-ttu-id="8585e-749">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-749">Minimum system</span></span> | <span data-ttu-id="8585e-750">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-750">Windows XP</span></span>                                           |



 

### <a name="runforever"></a><span data-ttu-id="8585e-751">RunForever</span><span class="sxs-lookup"><span data-stu-id="8585e-751">RunForever</span></span>



| <span data-ttu-id="8585e-752">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-752">Entry</span></span> | <span data-ttu-id="8585e-753">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-753">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-754">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-754">Description</span></span>    | <span data-ttu-id="8585e-755">Consente a un processo server di continuare se un'applicazione è inattiva.</span><span class="sxs-lookup"><span data-stu-id="8585e-755">Enables a server process to continue if an application is idle.</span></span> <span data-ttu-id="8585e-756">Se impostato su true, il processo server non viene arrestato quando viene lasciato inattivo.</span><span class="sxs-lookup"><span data-stu-id="8585e-756">If set to True, the server process does not shut down when left idle.</span></span> <span data-ttu-id="8585e-757">Se impostato su false, il processo viene arrestato in base al valore impostato dalla proprietà ShutdownAfter.</span><span class="sxs-lookup"><span data-stu-id="8585e-757">If set to False, the process shuts down according to the value set by the ShutdownAfter property.</span></span> <span data-ttu-id="8585e-758">RunForever non è abilitato per le applicazioni di libreria (in-process).</span><span class="sxs-lookup"><span data-stu-id="8585e-758">RunForever is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="8585e-759">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-759">Access</span></span>         | <span data-ttu-id="8585e-760">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-760">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="8585e-761">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-761">Type</span></span>           | <span data-ttu-id="8585e-762">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-762">Bool</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8585e-763">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-763">Default</span></span>        | <span data-ttu-id="8585e-764">Falso</span><span class="sxs-lookup"><span data-stu-id="8585e-764">False</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="8585e-765">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-765">Minimum system</span></span> | <span data-ttu-id="8585e-766">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-766">Windows 2000</span></span>                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a><span data-ttu-id="8585e-767">ServiceName</span><span class="sxs-lookup"><span data-stu-id="8585e-767">ServiceName</span></span>



| <span data-ttu-id="8585e-768">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-768">Entry</span></span> | <span data-ttu-id="8585e-769">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-769">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-770">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-770">Description</span></span>    | <span data-ttu-id="8585e-771">Nome del servizio corrispondente all'applicazione configurata per l'esecuzione come applicazione di servizio.</span><span class="sxs-lookup"><span data-stu-id="8585e-771">The service name corresponding to the application configured to run as a service application.</span></span> <span data-ttu-id="8585e-772">Se questo valore è **null**, l'applicazione non è configurata per l'esecuzione come servizio.</span><span class="sxs-lookup"><span data-stu-id="8585e-772">If this value is **NULL**, the application is not configured to run as a service.</span></span> <span data-ttu-id="8585e-773">In caso contrario, è possibile trovare le informazioni di configurazione per il servizio utilizzando il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="8585e-773">Otherwise, the configuration information for the service can be found by using the service name.</span></span> |
| <span data-ttu-id="8585e-774">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-774">Access</span></span>         | <span data-ttu-id="8585e-775">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8585e-775">ReadOnly</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8585e-776">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-776">Type</span></span>           | <span data-ttu-id="8585e-777">string</span><span class="sxs-lookup"><span data-stu-id="8585e-777">String</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="8585e-778">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-778">Default</span></span>        | <span data-ttu-id="8585e-779">""</span><span class="sxs-lookup"><span data-stu-id="8585e-779">""</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8585e-780">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-780">Minimum system</span></span> | <span data-ttu-id="8585e-781">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-781">Windows XP</span></span>                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a><span data-ttu-id="8585e-782">ShutdownAfter</span><span class="sxs-lookup"><span data-stu-id="8585e-782">ShutdownAfter</span></span>



| <span data-ttu-id="8585e-783">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-783">Entry</span></span> | <span data-ttu-id="8585e-784">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-784">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-785">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-785">Description</span></span>    | <span data-ttu-id="8585e-786">Imposta il ritardo prima di arrestare un processo server dopo che diventa inattivo.</span><span class="sxs-lookup"><span data-stu-id="8585e-786">Sets the delay before shutting down a server process after it becomes idle.</span></span> <span data-ttu-id="8585e-787">La latenza di arresto è compresa tra 0 e 1440 minuti (24 ore).</span><span class="sxs-lookup"><span data-stu-id="8585e-787">Shutdown latency ranges from 0 to 1440 minutes (24 hours).</span></span> <span data-ttu-id="8585e-788">Se RunForever è impostato su true, questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="8585e-788">If RunForever is set to True, this property is ignored.</span></span> <span data-ttu-id="8585e-789">ShutdownAfter non è abilitato per le applicazioni di libreria (in-process).</span><span class="sxs-lookup"><span data-stu-id="8585e-789">ShutdownAfter is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="8585e-790">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-790">Access</span></span>         | <span data-ttu-id="8585e-791">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-791">ReadWrite</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="8585e-792">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-792">Type</span></span>           | <span data-ttu-id="8585e-793">Long (0-1440)</span><span class="sxs-lookup"><span data-stu-id="8585e-793">Long (0-1440)</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8585e-794">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-794">Default</span></span>        | <span data-ttu-id="8585e-795">3</span><span class="sxs-lookup"><span data-stu-id="8585e-795">3</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8585e-796">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-796">Minimum system</span></span> | <span data-ttu-id="8585e-797">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8585e-797">Windows 2000</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a><span data-ttu-id="8585e-798">SoapActivated</span><span class="sxs-lookup"><span data-stu-id="8585e-798">SoapActivated</span></span>



| <span data-ttu-id="8585e-799">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-799">Entry</span></span> | <span data-ttu-id="8585e-800">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-800">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-801">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-801">Description</span></span>    | <span data-ttu-id="8585e-802">Indica se l'applicazione viene esposta per l'utilizzo tramite il protocollo SOAP.</span><span class="sxs-lookup"><span data-stu-id="8585e-802">Indicates whether this application is exposed for consumption via the SOAP protocol.</span></span> |
| <span data-ttu-id="8585e-803">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-803">Access</span></span>         | <span data-ttu-id="8585e-804">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-804">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="8585e-805">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-805">Type</span></span>           | <span data-ttu-id="8585e-806">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-806">Bool</span></span>                                                                                 |
| <span data-ttu-id="8585e-807">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-807">Default</span></span>        | <span data-ttu-id="8585e-808">Falso</span><span class="sxs-lookup"><span data-stu-id="8585e-808">False</span></span>                                                                                |
| <span data-ttu-id="8585e-809">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-809">Minimum system</span></span> | <span data-ttu-id="8585e-810">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8585e-810">Windows Server 2003</span></span>                                                                  |



 

### <a name="soapbaseurl"></a><span data-ttu-id="8585e-811">SoapBaseUrl</span><span class="sxs-lookup"><span data-stu-id="8585e-811">SoapBaseUrl</span></span>



| <span data-ttu-id="8585e-812">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-812">Entry</span></span> | <span data-ttu-id="8585e-813">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-813">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-814">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-814">Description</span></span>    | <span data-ttu-id="8585e-815">Endpoint URL in corrispondenza del quale l'applicazione viene esposta tramite il protocollo SOAP.</span><span class="sxs-lookup"><span data-stu-id="8585e-815">The URL endpoint at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="8585e-816">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-816">Access</span></span>         | <span data-ttu-id="8585e-817">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-817">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="8585e-818">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-818">Type</span></span>           | <span data-ttu-id="8585e-819">string</span><span class="sxs-lookup"><span data-stu-id="8585e-819">String</span></span>                                                                       |
| <span data-ttu-id="8585e-820">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-820">Default</span></span>        | <span data-ttu-id="8585e-821">""</span><span class="sxs-lookup"><span data-stu-id="8585e-821">""</span></span>                                                                           |
| <span data-ttu-id="8585e-822">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-822">Minimum system</span></span> | <span data-ttu-id="8585e-823">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8585e-823">Windows Server 2003</span></span>                                                          |



 

### <a name="soapmailto"></a><span data-ttu-id="8585e-824">SoapMailTo</span><span class="sxs-lookup"><span data-stu-id="8585e-824">SoapMailTo</span></span>



| <span data-ttu-id="8585e-825">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-825">Entry</span></span> | <span data-ttu-id="8585e-826">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-826">Value</span></span> |
|----------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-827">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-827">Description</span></span>    | <span data-ttu-id="8585e-828">Indirizzo di posta elettronica in cui l'applicazione viene esposta tramite il protocollo SOAP.</span><span class="sxs-lookup"><span data-stu-id="8585e-828">The email address at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="8585e-829">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-829">Access</span></span>         | <span data-ttu-id="8585e-830">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-830">ReadWrite</span></span>                                                                     |
| <span data-ttu-id="8585e-831">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-831">Type</span></span>           | <span data-ttu-id="8585e-832">string</span><span class="sxs-lookup"><span data-stu-id="8585e-832">String</span></span>                                                                        |
| <span data-ttu-id="8585e-833">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-833">Default</span></span>        | <span data-ttu-id="8585e-834">""</span><span class="sxs-lookup"><span data-stu-id="8585e-834">""</span></span>                                                                            |
| <span data-ttu-id="8585e-835">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-835">Minimum system</span></span> | <span data-ttu-id="8585e-836">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8585e-836">Windows Server 2003</span></span>                                                           |



 

### <a name="soapvroot"></a><span data-ttu-id="8585e-837">SoapVRoot</span><span class="sxs-lookup"><span data-stu-id="8585e-837">SoapVRoot</span></span>



| <span data-ttu-id="8585e-838">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-838">Entry</span></span> | <span data-ttu-id="8585e-839">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-839">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-840">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-840">Description</span></span>    | <span data-ttu-id="8585e-841">Directory radice virtuale di IIS in cui risiedono gli script di accesso che espongono l'applicazione tramite il protocollo SOAP.</span><span class="sxs-lookup"><span data-stu-id="8585e-841">The IIS virtual root directory in which the access scripts that expose the application via the SOAP protocol reside.</span></span> |
| <span data-ttu-id="8585e-842">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-842">Access</span></span>         | <span data-ttu-id="8585e-843">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-843">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="8585e-844">Type</span><span class="sxs-lookup"><span data-stu-id="8585e-844">Type</span></span>           | <span data-ttu-id="8585e-845">string</span><span class="sxs-lookup"><span data-stu-id="8585e-845">String</span></span>                                                                                                               |
| <span data-ttu-id="8585e-846">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-846">Default</span></span>        | <span data-ttu-id="8585e-847">""</span><span class="sxs-lookup"><span data-stu-id="8585e-847">""</span></span>                                                                                                                   |
| <span data-ttu-id="8585e-848">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-848">Minimum system</span></span> | <span data-ttu-id="8585e-849">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8585e-849">Windows Server 2003</span></span>                                                                                                  |



 

### <a name="srpenabled"></a><span data-ttu-id="8585e-850">SRPEnabled</span><span class="sxs-lookup"><span data-stu-id="8585e-850">SRPEnabled</span></span>



| <span data-ttu-id="8585e-851">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-851">Entry</span></span> | <span data-ttu-id="8585e-852">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-852">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-853">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-853">Description</span></span>    | <span data-ttu-id="8585e-854">Determina i criteri di restrizione software per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-854">Determines the software restriction policy (SRP) for the application.</span></span> <span data-ttu-id="8585e-855">Se è impostato su true, viene usata la proprietà SRPTrustLevel per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-855">If set to True, the SRPTrustLevel property for the application is used.</span></span> <span data-ttu-id="8585e-856">Se è impostato su false, vengono usati i criteri di restrizione software dalle impostazioni di sicurezza locali.</span><span class="sxs-lookup"><span data-stu-id="8585e-856">If set to False, the software restriction policies from the local security settings are used.</span></span> <span data-ttu-id="8585e-857">Le impostazioni di sicurezza locali vengono controllate tramite lo snap-in criteri di sicurezza locali di Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="8585e-857">The local security settings are controlled through the Local Security Policy snap-in of the Microsoft Management Console.</span></span> |
| <span data-ttu-id="8585e-858">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-858">Access</span></span>         | <span data-ttu-id="8585e-859">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-859">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="8585e-860">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-860">Type</span></span>           | <span data-ttu-id="8585e-861">Bool</span><span class="sxs-lookup"><span data-stu-id="8585e-861">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8585e-862">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-862">Default</span></span>        | <span data-ttu-id="8585e-863">Falso</span><span class="sxs-lookup"><span data-stu-id="8585e-863">False</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="8585e-864">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-864">Minimum system</span></span> | <span data-ttu-id="8585e-865">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-865">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a><span data-ttu-id="8585e-866">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="8585e-866">SRPTrustLevel</span></span>



| <span data-ttu-id="8585e-867">Voce</span><span class="sxs-lookup"><span data-stu-id="8585e-867">Entry</span></span> | <span data-ttu-id="8585e-868">Valore</span><span class="sxs-lookup"><span data-stu-id="8585e-868">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8585e-869">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8585e-869">Description</span></span>    | <span data-ttu-id="8585e-870">Indica il livello di attendibilità del criterio di restrizione software dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-870">Indicates the software restriction policy (SRP) trust level of the application.</span></span> <span data-ttu-id="8585e-871">Questa proprietà viene utilizzata solo se la proprietà SRPEnabled è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="8585e-871">This property is used only if the SRPEnabled property is set to True.</span></span> <span data-ttu-id="8585e-872">Il livello di attendibilità SRP si riferisce al livello di attendibilità che si è disposti a assegnare a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8585e-872">The SRP trust level refers to the level of trust that you are willing to give to an application.</span></span> <span data-ttu-id="8585e-873">Un livello di attendibilità Unrestricted SRP corrisponde \_ al \_ valore di enumerazione LEVELID FULLYTRUSTED più sicuro, mentre un livello di ATTENDIBILità SRP non consentito corrisponde al \_ valore di enumerazione non consentito LEVELID più sicuro \_ .</span><span class="sxs-lookup"><span data-stu-id="8585e-873">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="8585e-874">L'enumerazione per i livelli di attendibilità è definita in Winsafer. h.</span><span class="sxs-lookup"><span data-stu-id="8585e-874">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="8585e-875">Access</span><span class="sxs-lookup"><span data-stu-id="8585e-875">Access</span></span>         | <span data-ttu-id="8585e-876">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8585e-876">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8585e-877">Tipo</span><span class="sxs-lookup"><span data-stu-id="8585e-877">Type</span></span>           | <span data-ttu-id="8585e-878">Valori lunghi possibili: SAFER \_ LEVELID non \_ consentita (0x0) Safer \_ LEVELID \_ FULLYTRUSTED (0x40000)</span><span class="sxs-lookup"><span data-stu-id="8585e-878">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="8585e-879">Predefinito</span><span class="sxs-lookup"><span data-stu-id="8585e-879">Default</span></span>        | <span data-ttu-id="8585e-880">SAFER \_ LEVELID \_ FULLYTRUSTED (0x40000)</span><span class="sxs-lookup"><span data-stu-id="8585e-880">SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="8585e-881">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="8585e-881">Minimum system</span></span> | <span data-ttu-id="8585e-882">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8585e-882">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

<span data-ttu-id="8585e-883">Un'applicazione che si è disposti a considerare attendibile con accesso senza restrizioni deve avere la protezione più rigorosa collegata.</span><span class="sxs-lookup"><span data-stu-id="8585e-883">An application that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="8585e-884">Le applicazioni senza restrizioni possono caricare solo componenti senza restrizioni, mentre le applicazioni non consentite non potranno essere eseguite e pertanto non potranno caricare alcun componente.</span><span class="sxs-lookup"><span data-stu-id="8585e-884">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

## <a name="see-also"></a><span data-ttu-id="8585e-885">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8585e-885">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8585e-886">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="8585e-886">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
