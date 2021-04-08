---
description: Contiene un singolo oggetto che corrisponde al computer di cui si desidera accedere al catalogo. Questo oggetto include informazioni sulle impostazioni a livello di computer.
ms.assetid: 75f14cad-9cd5-44a6-9afa-2c8ad1e87027
title: Raccolta LocalComputer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocalComputer
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4e1ce08f3bf1fef74af0d77ada15716abb4530a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748999"
---
# <a name="localcomputer-collection"></a><span data-ttu-id="3ff88-104">Raccolta LocalComputer</span><span class="sxs-lookup"><span data-stu-id="3ff88-104">LocalComputer collection</span></span>

<span data-ttu-id="3ff88-105">Contiene un singolo oggetto che corrisponde al computer di cui si desidera accedere al catalogo.</span><span class="sxs-lookup"><span data-stu-id="3ff88-105">Contains a single object that corresponds to the computer whose catalog you are accessing.</span></span> <span data-ttu-id="3ff88-106">Questo oggetto include informazioni sulle impostazioni a livello di computer.</span><span class="sxs-lookup"><span data-stu-id="3ff88-106">This object holds computer level settings information.</span></span> <span data-ttu-id="3ff88-107">Se si chiama il metodo [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) su un oggetto creato dalla classe [**COMAdminCatalog**](comadmincatalog.md) , l'oggetto nella raccolta **LocalComputer** contiene informazioni sul computer remoto di cui si sta effettuando l'accesso.</span><span class="sxs-lookup"><span data-stu-id="3ff88-107">If you call the [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) method on an object created from the [**COMAdminCatalog**](comadmincatalog.md) class, the object in the **LocalComputer** collection contains information about the remote computer whose catalog you are accessing.</span></span>

<span data-ttu-id="3ff88-108">Questa raccolta non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="3ff88-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="3ff88-109">Membri</span><span class="sxs-lookup"><span data-stu-id="3ff88-109">Members</span></span>

<span data-ttu-id="3ff88-110">La raccolta **LocalComputer** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="3ff88-110">The **LocalComputer** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="3ff88-111">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="3ff88-111">Related Collections</span></span>

<span data-ttu-id="3ff88-112">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="3ff88-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="3ff88-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="3ff88-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="3ff88-114">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="3ff88-114">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="3ff88-115">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="3ff88-115">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="3ff88-116">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="3ff88-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="3ff88-117">**Radice**</span><span class="sxs-lookup"><span data-stu-id="3ff88-117">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="3ff88-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ff88-118">Properties</span></span>

<span data-ttu-id="3ff88-119">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="3ff88-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="3ff88-120">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="3ff88-120">ApplicationProxyRSN</span></span>](#applicationproxyrsn)
-   [<span data-ttu-id="3ff88-121">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-121">CISEnabled</span></span>](#cisenabled)
-   [<span data-ttu-id="3ff88-122">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-122">DCOMEnabled</span></span>](#dcomenabled)
-   [<span data-ttu-id="3ff88-123">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="3ff88-123">DefaultAuthenticationLevel</span></span>](#defaultauthenticationlevel)
-   [<span data-ttu-id="3ff88-124">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="3ff88-124">DefaultImpersonationLevel</span></span>](#defaultimpersonationlevel)
-   [<span data-ttu-id="3ff88-125">DefaultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="3ff88-125">DefaultToInternetPorts</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="3ff88-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-126">Description</span></span>](#description)
-   [<span data-ttu-id="3ff88-127">DSPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-127">DSPartitionLookupEnabled</span></span>](#dspartitionlookupenabled)
-   [<span data-ttu-id="3ff88-128">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="3ff88-128">InternetPortsListed</span></span>](#internetportslisted)
-   [<span data-ttu-id="3ff88-129">Routing</span><span class="sxs-lookup"><span data-stu-id="3ff88-129">IsRouter</span></span>](#isrouter)
-   [<span data-ttu-id="3ff88-130">LoadBalancingCLSID</span><span class="sxs-lookup"><span data-stu-id="3ff88-130">LoadBalancingCLSID</span></span>](#loadbalancingclsid)
-   [<span data-ttu-id="3ff88-131">LocalPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-131">LocalPartitionLookupEnabled</span></span>](#localpartitionlookupenabled)
-   [<span data-ttu-id="3ff88-132">Nome</span><span class="sxs-lookup"><span data-stu-id="3ff88-132">Name</span></span>](#name)
-   [<span data-ttu-id="3ff88-133">OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3ff88-133">OperatingSystem</span></span>](#operatingsystem)
-   [<span data-ttu-id="3ff88-134">PartitionsEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-134">PartitionsEnabled</span></span>](#partitionsenabled)
-   [<span data-ttu-id="3ff88-135">Ports</span><span class="sxs-lookup"><span data-stu-id="3ff88-135">Ports</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="3ff88-136">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-136">ResourcePoolingEnabled</span></span>](#resourcepoolingenabled)
-   [<span data-ttu-id="3ff88-137">RPCProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-137">RPCProxyEnabled</span></span>](#rpcproxyenabled)
-   [<span data-ttu-id="3ff88-138">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-138">SecureReferencesEnabled</span></span>](#securereferencesenabled)
-   [<span data-ttu-id="3ff88-139">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-139">SecurityTrackingEnabled</span></span>](#securitytrackingenabled)
-   [<span data-ttu-id="3ff88-140">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="3ff88-140">SRPActivateAsActivatorChecks</span></span>](#srpactivateasactivatorchecks)
-   [<span data-ttu-id="3ff88-141">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="3ff88-141">SRPRunningObjectChecks</span></span>](#srprunningobjectchecks)
-   [<span data-ttu-id="3ff88-142">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="3ff88-142">TransactionTimeout</span></span>](#transactiontimeout)

### <a name="applicationproxyrsn"></a><span data-ttu-id="3ff88-143">ApplicationProxyRSN</span><span class="sxs-lookup"><span data-stu-id="3ff88-143">ApplicationProxyRSN</span></span>



| <span data-ttu-id="3ff88-144">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-144">Entry</span></span> | <span data-ttu-id="3ff88-145">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-145">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="3ff88-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-146">Description</span></span>    | <span data-ttu-id="3ff88-147">Nome del server remoto usato dai proxy di applicazione per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3ff88-147">Remote server name used by application proxies by default.</span></span> |
| <span data-ttu-id="3ff88-148">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-148">Access</span></span>         | <span data-ttu-id="3ff88-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-149">ReadWrite</span></span>                                                  |
| <span data-ttu-id="3ff88-150">Type</span><span class="sxs-lookup"><span data-stu-id="3ff88-150">Type</span></span>           | <span data-ttu-id="3ff88-151">string</span><span class="sxs-lookup"><span data-stu-id="3ff88-151">String</span></span>                                                     |
| <span data-ttu-id="3ff88-152">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-152">Default</span></span>        | <span data-ttu-id="3ff88-153">""</span><span class="sxs-lookup"><span data-stu-id="3ff88-153">""</span></span>                                                         |
| <span data-ttu-id="3ff88-154">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-154">Minimum system</span></span> | <span data-ttu-id="3ff88-155">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-155">Windows 2000</span></span>                                               |



 

### <a name="cisenabled"></a><span data-ttu-id="3ff88-156">CISEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-156">CISEnabled</span></span>



| <span data-ttu-id="3ff88-157">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-157">Entry</span></span> | <span data-ttu-id="3ff88-158">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-158">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="3ff88-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-159">Description</span></span>    | <span data-ttu-id="3ff88-160">Indica se i servizi Internet COM sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="3ff88-160">Indicates whether COM Internet Services is enabled.</span></span> |
| <span data-ttu-id="3ff88-161">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-161">Access</span></span>         | <span data-ttu-id="3ff88-162">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-162">ReadWrite</span></span>                                           |
| <span data-ttu-id="3ff88-163">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-163">Type</span></span>           | <span data-ttu-id="3ff88-164">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-164">Bool</span></span>                                                |
| <span data-ttu-id="3ff88-165">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-165">Default</span></span>        | <span data-ttu-id="3ff88-166">Falso</span><span class="sxs-lookup"><span data-stu-id="3ff88-166">False</span></span>                                               |
| <span data-ttu-id="3ff88-167">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-167">Minimum system</span></span> | <span data-ttu-id="3ff88-168">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-168">Windows 2000</span></span>                                        |



 

### <a name="dcomenabled"></a><span data-ttu-id="3ff88-169">DCOMEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-169">DCOMEnabled</span></span>



| <span data-ttu-id="3ff88-170">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-170">Entry</span></span> | <span data-ttu-id="3ff88-171">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-171">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="3ff88-172">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-172">Description</span></span>    | <span data-ttu-id="3ff88-173">Impostare su true per abilitare DCOM nel computer.</span><span class="sxs-lookup"><span data-stu-id="3ff88-173">Set to True to enable DCOM on the computer.</span></span> |
| <span data-ttu-id="3ff88-174">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-174">Access</span></span>         | <span data-ttu-id="3ff88-175">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-175">ReadWrite</span></span>                                   |
| <span data-ttu-id="3ff88-176">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-176">Type</span></span>           | <span data-ttu-id="3ff88-177">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-177">Bool</span></span>                                        |
| <span data-ttu-id="3ff88-178">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-178">Default</span></span>        | <span data-ttu-id="3ff88-179">Vero</span><span class="sxs-lookup"><span data-stu-id="3ff88-179">True</span></span>                                        |
| <span data-ttu-id="3ff88-180">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-180">Minimum system</span></span> | <span data-ttu-id="3ff88-181">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-181">Windows 2000</span></span>                                |



 

### <a name="defaultauthenticationlevel"></a><span data-ttu-id="3ff88-182">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="3ff88-182">DefaultAuthenticationLevel</span></span>



| <span data-ttu-id="3ff88-183">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-183">Entry</span></span> | <span data-ttu-id="3ff88-184">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-184">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-185">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-185">Description</span></span>    | <span data-ttu-id="3ff88-186">Livello di autenticazione utilizzato dalle applicazioni per le quali l'autenticazione è impostata su default.</span><span class="sxs-lookup"><span data-stu-id="3ff88-186">Authentication level used by applications that have Authentication set to Default.</span></span> <span data-ttu-id="3ff88-187">I valori corrispondono alle impostazioni di autenticazione RPC (Remote Procedure Call).</span><span class="sxs-lookup"><span data-stu-id="3ff88-187">Values correspond to the Remote Procedure Call (RPC) authentication settings.</span></span>                                                                                         |
| <span data-ttu-id="3ff88-188">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-188">Access</span></span>         | <span data-ttu-id="3ff88-189">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-189">ReadWrite</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="3ff88-190">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-190">Type</span></span>           | <span data-ttu-id="3ff88-191">Valori lunghi possibili: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="3ff88-191">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span> |
| <span data-ttu-id="3ff88-192">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-192">Default</span></span>        | <span data-ttu-id="3ff88-193">COMAdminAuthenticationConnect (2)</span><span class="sxs-lookup"><span data-stu-id="3ff88-193">COMAdminAuthenticationConnect (2)</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="3ff88-194">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-194">Minimum system</span></span> | <span data-ttu-id="3ff88-195">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-195">Windows 2000</span></span>                                                                                                                                                                                                                                             |



 

> [!Note]  
> <span data-ttu-id="3ff88-196">COMAdminAuthenticationDefault viene mappato a COMAdminAuthenticationConnect quando COM chiama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="3ff88-196">COMAdminAuthenticationDefault is mapped to COMAdminAuthenticationConnect when COM calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="3ff88-197">Si consiglia di usare le costanti nell'enumerazione e non i valori numerici.</span><span class="sxs-lookup"><span data-stu-id="3ff88-197">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="defaultimpersonationlevel"></a><span data-ttu-id="3ff88-198">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="3ff88-198">DefaultImpersonationLevel</span></span>



| <span data-ttu-id="3ff88-199">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-199">Entry</span></span> | <span data-ttu-id="3ff88-200">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-200">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-201">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-201">Description</span></span>    | <span data-ttu-id="3ff88-202">Livello di rappresentazione per consentire se non ne è stato impostato uno.</span><span class="sxs-lookup"><span data-stu-id="3ff88-202">Impersonation level to allow if one is not set.</span></span>                                                                                                               |
| <span data-ttu-id="3ff88-203">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-203">Access</span></span>         | <span data-ttu-id="3ff88-204">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-204">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="3ff88-205">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-205">Type</span></span>           | <span data-ttu-id="3ff88-206">Valori lunghi possibili: COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4)</span><span class="sxs-lookup"><span data-stu-id="3ff88-206">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="3ff88-207">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-207">Default</span></span>        | <span data-ttu-id="3ff88-208">COMAdminImpersonationIdentify (2)</span><span class="sxs-lookup"><span data-stu-id="3ff88-208">COMAdminImpersonationIdentify (2)</span></span>                                                                                                                             |
| <span data-ttu-id="3ff88-209">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-209">Minimum system</span></span> | <span data-ttu-id="3ff88-210">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-210">Windows 2000</span></span>                                                                                                                                                  |



 

> [!Note]  
> <span data-ttu-id="3ff88-211">Si consiglia di usare le costanti nell'enumerazione e non i valori numerici.</span><span class="sxs-lookup"><span data-stu-id="3ff88-211">It is recommended that you use the constants in the enumeration, and not the numeric values.</span></span>

 

### <a name="defaulttointernetports"></a><span data-ttu-id="3ff88-212">DefaultToInternetPorts</span><span class="sxs-lookup"><span data-stu-id="3ff88-212">DefaultToInternetPorts</span></span>



| <span data-ttu-id="3ff88-213">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-213">Entry</span></span> | <span data-ttu-id="3ff88-214">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-214">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-215">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-215">Description</span></span>    | <span data-ttu-id="3ff88-216">Determina se il tipo predefinito di porta specificato deve essere Internet (true) o Intranet (false).</span><span class="sxs-lookup"><span data-stu-id="3ff88-216">Determines whether the default type of port provided should be Internet (True) or intranet (False).</span></span> |
| <span data-ttu-id="3ff88-217">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-217">Access</span></span>         | <span data-ttu-id="3ff88-218">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-218">ReadWrite</span></span>                                                                                           |
| <span data-ttu-id="3ff88-219">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-219">Type</span></span>           | <span data-ttu-id="3ff88-220">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-220">Bool</span></span>                                                                                                |
| <span data-ttu-id="3ff88-221">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-221">Default</span></span>        | <span data-ttu-id="3ff88-222">Falso</span><span class="sxs-lookup"><span data-stu-id="3ff88-222">False</span></span>                                                                                               |
| <span data-ttu-id="3ff88-223">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-223">Minimum system</span></span> | <span data-ttu-id="3ff88-224">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-224">Windows 2000</span></span>                                                                                        |



 

### <a name="description"></a><span data-ttu-id="3ff88-225">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-225">Description</span></span>



| <span data-ttu-id="3ff88-226">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-226">Entry</span></span> | <span data-ttu-id="3ff88-227">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-227">Value</span></span> |
|----------------|--------------------------------|
| <span data-ttu-id="3ff88-228">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-228">Description</span></span>    | <span data-ttu-id="3ff88-229">Descrizione del computer.</span><span class="sxs-lookup"><span data-stu-id="3ff88-229">A description of the computer.</span></span> |
| <span data-ttu-id="3ff88-230">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-230">Access</span></span>         | <span data-ttu-id="3ff88-231">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-231">ReadWrite</span></span>                      |
| <span data-ttu-id="3ff88-232">Type</span><span class="sxs-lookup"><span data-stu-id="3ff88-232">Type</span></span>           | <span data-ttu-id="3ff88-233">string</span><span class="sxs-lookup"><span data-stu-id="3ff88-233">String</span></span>                         |
| <span data-ttu-id="3ff88-234">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-234">Default</span></span>        | <span data-ttu-id="3ff88-235">""</span><span class="sxs-lookup"><span data-stu-id="3ff88-235">""</span></span>                             |
| <span data-ttu-id="3ff88-236">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-236">Minimum system</span></span> | <span data-ttu-id="3ff88-237">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-237">Windows 2000</span></span>                   |



 

### <a name="dspartitionlookupenabled"></a><span data-ttu-id="3ff88-238">DSPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-238">DSPartitionLookupEnabled</span></span>



| <span data-ttu-id="3ff88-239">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-239">Entry</span></span> | <span data-ttu-id="3ff88-240">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-240">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-241">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-241">Description</span></span>    | <span data-ttu-id="3ff88-242">Indica se l'utente dei mapping della partizione viene archiviato nell'archivio di dominio.</span><span class="sxs-lookup"><span data-stu-id="3ff88-242">Indicates whether the user of the partition mappings is checked into the domain store.</span></span> |
| <span data-ttu-id="3ff88-243">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-243">Access</span></span>         | <span data-ttu-id="3ff88-244">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-244">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="3ff88-245">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-245">Type</span></span>           | <span data-ttu-id="3ff88-246">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-246">Bool</span></span>                                                                                   |
| <span data-ttu-id="3ff88-247">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-247">Default</span></span>        | <span data-ttu-id="3ff88-248">Vero</span><span class="sxs-lookup"><span data-stu-id="3ff88-248">True</span></span>                                                                                   |
| <span data-ttu-id="3ff88-249">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-249">Minimum system</span></span> | <span data-ttu-id="3ff88-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ff88-250">Windows Server 2003</span></span>                                                                    |



 

### <a name="internetportslisted"></a><span data-ttu-id="3ff88-251">InternetPortsListed</span><span class="sxs-lookup"><span data-stu-id="3ff88-251">InternetPortsListed</span></span>



| <span data-ttu-id="3ff88-252">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-252">Entry</span></span> | <span data-ttu-id="3ff88-253">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-253">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-254">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-254">Description</span></span>    | <span data-ttu-id="3ff88-255">Determina se le porte elencate nella proprietà porte devono essere utilizzate per Internet (true) o per Intranet (false).</span><span class="sxs-lookup"><span data-stu-id="3ff88-255">Determines whether the ports listed in the Ports property are to be used for Internet (True) or for intranet (False).</span></span> |
| <span data-ttu-id="3ff88-256">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-256">Access</span></span>         | <span data-ttu-id="3ff88-257">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-257">ReadWrite</span></span>                                                                                                             |
| <span data-ttu-id="3ff88-258">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-258">Type</span></span>           | <span data-ttu-id="3ff88-259">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-259">Bool</span></span>                                                                                                                  |
| <span data-ttu-id="3ff88-260">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-260">Default</span></span>        | <span data-ttu-id="3ff88-261">Falso</span><span class="sxs-lookup"><span data-stu-id="3ff88-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="3ff88-262">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-262">Minimum system</span></span> | <span data-ttu-id="3ff88-263">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-263">Windows 2000</span></span>                                                                                                          |



 

### <a name="isrouter"></a><span data-ttu-id="3ff88-264">Routing</span><span class="sxs-lookup"><span data-stu-id="3ff88-264">IsRouter</span></span>



| <span data-ttu-id="3ff88-265">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-265">Entry</span></span> | <span data-ttu-id="3ff88-266">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-266">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-267">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-267">Description</span></span>    | <span data-ttu-id="3ff88-268">Impostare su true se il computer è un router per il servizio di bilanciamento del carico componente (CLB).</span><span class="sxs-lookup"><span data-stu-id="3ff88-268">Set to True if the computer is a router for the component load balancing (CLB) service.</span></span> <span data-ttu-id="3ff88-269">Questa proprietà può essere impostata su true solo se il servizio di bilanciamento del carico componente è attualmente installato nel computer. in caso contrario, gli errori con COMAdmin \_ e \_ richiedono una \_ \_ piattaforma diversa.</span><span class="sxs-lookup"><span data-stu-id="3ff88-269">This property can be set to True only if the component load balancing service is currently installed on the computer; otherwise, it errors with COMADMIN\_E\_REQUIRES\_DIFFERENT\_PLATFORM.</span></span> |
| <span data-ttu-id="3ff88-270">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-270">Access</span></span>         | <span data-ttu-id="3ff88-271">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-271">ReadWrite</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3ff88-272">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-272">Type</span></span>           | <span data-ttu-id="3ff88-273">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-273">Bool</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="3ff88-274">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-274">Default</span></span>        | <span data-ttu-id="3ff88-275">Falso</span><span class="sxs-lookup"><span data-stu-id="3ff88-275">False</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3ff88-276">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-276">Minimum system</span></span> | <span data-ttu-id="3ff88-277">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-277">Windows 2000</span></span>                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="3ff88-278">Se questa proprietà è impostata su true, il server CLB viene configurato e viene avviato all'avvio.</span><span class="sxs-lookup"><span data-stu-id="3ff88-278">If this property is set to True, the CLB server is configured and starts at startup.</span></span> <span data-ttu-id="3ff88-279">Il server viene aggiunto alla raccolta ApplicationCluster se non è già presente.</span><span class="sxs-lookup"><span data-stu-id="3ff88-279">The server is added to the ApplicationCluster collection if it is not already present.</span></span>

### <a name="loadbalancingclsid"></a><span data-ttu-id="3ff88-280">LoadBalancingCLSID</span><span class="sxs-lookup"><span data-stu-id="3ff88-280">LoadBalancingCLSID</span></span>



| <span data-ttu-id="3ff88-281">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-281">Entry</span></span> | <span data-ttu-id="3ff88-282">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-282">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="3ff88-283">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-283">Description</span></span>    | <span data-ttu-id="3ff88-284">CLSID dell'oggetto da bilanciare.</span><span class="sxs-lookup"><span data-stu-id="3ff88-284">The CLSID of the object to balance.</span></span> |
| <span data-ttu-id="3ff88-285">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-285">Access</span></span>         | <span data-ttu-id="3ff88-286">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-286">ReadWrite</span></span>                           |
| <span data-ttu-id="3ff88-287">Type</span><span class="sxs-lookup"><span data-stu-id="3ff88-287">Type</span></span>           | <span data-ttu-id="3ff88-288">string</span><span class="sxs-lookup"><span data-stu-id="3ff88-288">String</span></span>                              |
| <span data-ttu-id="3ff88-289">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-289">Default</span></span>        | <span data-ttu-id="3ff88-290">NULL</span><span class="sxs-lookup"><span data-stu-id="3ff88-290">NULL</span></span>                                |
| <span data-ttu-id="3ff88-291">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-291">Minimum system</span></span> | <span data-ttu-id="3ff88-292">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3ff88-292">Windows XP</span></span>                          |



 

### <a name="localpartitionlookupenabled"></a><span data-ttu-id="3ff88-293">LocalPartitionLookupEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-293">LocalPartitionLookupEnabled</span></span>



| <span data-ttu-id="3ff88-294">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-294">Entry</span></span> | <span data-ttu-id="3ff88-295">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-295">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-296">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-296">Description</span></span>    | <span data-ttu-id="3ff88-297">Indica se l'utente dei mapping della partizione viene archiviato nell'archivio locale.</span><span class="sxs-lookup"><span data-stu-id="3ff88-297">Indicates whether the user of the partition mappings is checked into the local store.</span></span> |
| <span data-ttu-id="3ff88-298">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-298">Access</span></span>         | <span data-ttu-id="3ff88-299">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-299">ReadWrite</span></span>                                                                             |
| <span data-ttu-id="3ff88-300">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-300">Type</span></span>           | <span data-ttu-id="3ff88-301">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-301">Bool</span></span>                                                                                  |
| <span data-ttu-id="3ff88-302">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-302">Default</span></span>        | <span data-ttu-id="3ff88-303">Vero</span><span class="sxs-lookup"><span data-stu-id="3ff88-303">True</span></span>                                                                                  |
| <span data-ttu-id="3ff88-304">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-304">Minimum system</span></span> | <span data-ttu-id="3ff88-305">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ff88-305">Windows Server 2003</span></span>                                                                   |



 

### <a name="name"></a><span data-ttu-id="3ff88-306">Nome</span><span class="sxs-lookup"><span data-stu-id="3ff88-306">Name</span></span>



| <span data-ttu-id="3ff88-307">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-307">Entry</span></span> | <span data-ttu-id="3ff88-308">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-308">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-309">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-309">Description</span></span>    | <span data-ttu-id="3ff88-310">Nome del computer.</span><span class="sxs-lookup"><span data-stu-id="3ff88-310">The name of the computer.</span></span> <span data-ttu-id="3ff88-311">Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="3ff88-311">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="3ff88-312">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-312">Access</span></span>         | <span data-ttu-id="3ff88-313">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="3ff88-313">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="3ff88-314">Type</span><span class="sxs-lookup"><span data-stu-id="3ff88-314">Type</span></span>           | <span data-ttu-id="3ff88-315">string</span><span class="sxs-lookup"><span data-stu-id="3ff88-315">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3ff88-316">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-316">Default</span></span>        | <span data-ttu-id="3ff88-317">"Computer locale"</span><span class="sxs-lookup"><span data-stu-id="3ff88-317">"My Computer"</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3ff88-318">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-318">Minimum system</span></span> | <span data-ttu-id="3ff88-319">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-319">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a><span data-ttu-id="3ff88-320">OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3ff88-320">OperatingSystem</span></span>



| <span data-ttu-id="3ff88-321">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-321">Entry</span></span> | <span data-ttu-id="3ff88-322">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-322">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-323">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-323">Description</span></span>    | <span data-ttu-id="3ff88-324">Sistema operativo installato nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="3ff88-324">The operating system installed on the local computer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="3ff88-325">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-325">Access</span></span>         | <span data-ttu-id="3ff88-326">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3ff88-327">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-327">Type</span></span>           | <span data-ttu-id="3ff88-328">Valori lunghi possibili: COMAdminOSNotInitialized (0) COMAdminOSWindows3 \_ 1 (1) COMAdminOSWindows9x (2) COMAdminOSWindows2000 (3) COMAdminOSWindows2000AdvancedServer (4) COMAdminOSWindows2000Unknown (5) COMAdminOSUnknown (6) COMAdminOSWindowsXPPersonal (11) COMAdminOSWindowsXPProfessional (12) COMAdminOSWindowsNETStandardServer (13) COMAdminOSWindowsNETEnterpriseServer (14) COMAdminOSWindowsNETDatacenterServer (15) COMAdminOSWindowsNETWebServer (16)</span><span class="sxs-lookup"><span data-stu-id="3ff88-328">Long Possible values:COMAdminOSNotInitialized (0)COMAdminOSWindows3\_1(1)COMAdminOSWindows9x (2)COMAdminOSWindows2000 (3)COMAdminOSWindows2000AdvancedServer (4)COMAdminOSWindows2000Unknown (5)COMAdminOSUnknown (6)COMAdminOSWindowsXPPersonal (11)COMAdminOSWindowsXPProfessional (12)COMAdminOSWindowsNETStandardServer (13)COMAdminOSWindowsNETEnterpriseServer (14)COMAdminOSWindowsNETDatacenterServer (15)COMAdminOSWindowsNETWebServer (16)</span></span> |
| <span data-ttu-id="3ff88-329">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-329">Default</span></span>        | <span data-ttu-id="3ff88-330">COMAdminOSNotInitialized (0)</span><span class="sxs-lookup"><span data-stu-id="3ff88-330">COMAdminOSNotInitialized (0)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3ff88-331">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-331">Minimum system</span></span> | <span data-ttu-id="3ff88-332">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-332">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a><span data-ttu-id="3ff88-333">PartitionsEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-333">PartitionsEnabled</span></span>



| <span data-ttu-id="3ff88-334">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-334">Entry</span></span> | <span data-ttu-id="3ff88-335">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-335">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-336">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-336">Description</span></span>    | <span data-ttu-id="3ff88-337">Indica se le partizioni COM+ possono essere utilizzate nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="3ff88-337">Indicates whether COM+ partitions can be used on the local computer.</span></span> <span data-ttu-id="3ff88-338">Se questa proprietà è false, qualsiasi tentativo di utilizzare le partizioni COM+ genera un errore.</span><span class="sxs-lookup"><span data-stu-id="3ff88-338">If this property is False, any attempt to use COM+ partitions results in an error.</span></span> |
| <span data-ttu-id="3ff88-339">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-339">Access</span></span>         | <span data-ttu-id="3ff88-340">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-340">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="3ff88-341">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-341">Type</span></span>           | <span data-ttu-id="3ff88-342">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-342">Bool</span></span>                                                                                                                                                    |
| <span data-ttu-id="3ff88-343">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-343">Default</span></span>        | <span data-ttu-id="3ff88-344">Falso</span><span class="sxs-lookup"><span data-stu-id="3ff88-344">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="3ff88-345">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-345">Minimum system</span></span> | <span data-ttu-id="3ff88-346">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ff88-346">Windows Server 2003</span></span>                                                                                                                                     |



 

### <a name="ports"></a><span data-ttu-id="3ff88-347">Porte</span><span class="sxs-lookup"><span data-stu-id="3ff88-347">Ports</span></span>



| <span data-ttu-id="3ff88-348">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-348">Entry</span></span> | <span data-ttu-id="3ff88-349">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-349">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-350">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-350">Description</span></span>    | <span data-ttu-id="3ff88-351">Stringa che descrive le porte utilizzate per Internet o Intranet, a seconda della proprietà InternetPortsListed. ad esempio, "500-599:600-800".</span><span class="sxs-lookup"><span data-stu-id="3ff88-351">A string describing ports that are for either Internet or intranet use, depending on the InternetPortsListed property; for example, "500-599: 600-800".</span></span> |
| <span data-ttu-id="3ff88-352">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-352">Access</span></span>         | <span data-ttu-id="3ff88-353">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-353">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="3ff88-354">Type</span><span class="sxs-lookup"><span data-stu-id="3ff88-354">Type</span></span>           | <span data-ttu-id="3ff88-355">string</span><span class="sxs-lookup"><span data-stu-id="3ff88-355">String</span></span>                                                                                                                                                  |
| <span data-ttu-id="3ff88-356">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-356">Default</span></span>        | <span data-ttu-id="3ff88-357">""</span><span class="sxs-lookup"><span data-stu-id="3ff88-357">""</span></span>                                                                                                                                                      |
| <span data-ttu-id="3ff88-358">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-358">Minimum system</span></span> | <span data-ttu-id="3ff88-359">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-359">Windows 2000</span></span>                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a><span data-ttu-id="3ff88-360">ResourcePoolingEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-360">ResourcePoolingEnabled</span></span>



| <span data-ttu-id="3ff88-361">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-361">Entry</span></span> | <span data-ttu-id="3ff88-362">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-362">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="3ff88-363">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-363">Description</span></span>    | <span data-ttu-id="3ff88-364">Consente l'uso dei distributori di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ff88-364">Enables use of resource dispensers.</span></span> |
| <span data-ttu-id="3ff88-365">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-365">Access</span></span>         | <span data-ttu-id="3ff88-366">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-366">ReadWrite</span></span>                           |
| <span data-ttu-id="3ff88-367">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-367">Type</span></span>           | <span data-ttu-id="3ff88-368">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-368">Bool</span></span>                                |
| <span data-ttu-id="3ff88-369">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-369">Default</span></span>        | <span data-ttu-id="3ff88-370">Vero</span><span class="sxs-lookup"><span data-stu-id="3ff88-370">True</span></span>                                |
| <span data-ttu-id="3ff88-371">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-371">Minimum system</span></span> | <span data-ttu-id="3ff88-372">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-372">Windows 2000</span></span>                        |



 

### <a name="rpcproxyenabled"></a><span data-ttu-id="3ff88-373">RPCProxyEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-373">RPCProxyEnabled</span></span>



| <span data-ttu-id="3ff88-374">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-374">Entry</span></span> | <span data-ttu-id="3ff88-375">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-375">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-376">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-376">Description</span></span>    | <span data-ttu-id="3ff88-377">Controlla se il proxy IIS RPC è abilitato.</span><span class="sxs-lookup"><span data-stu-id="3ff88-377">Controls whether the RPC IIS proxy is enabled.</span></span> <span data-ttu-id="3ff88-378">Il proxy IIS RPC viene utilizzato in combinazione con IIS per l'inoltro delle chiamate al meccanismo RPC da IIS ed è uno dei componenti principali dei servizi Internet COM, che viene abilitato impostando CISEnabled su true.</span><span class="sxs-lookup"><span data-stu-id="3ff88-378">The RPC IIS proxy is used in conjunction with IIS to forward calls to the RPC mechanism from IIS and is one of the core pieces of COM Internet Services, which is enabled by setting CISEnabled to True.</span></span> <span data-ttu-id="3ff88-379">Per ulteriori informazioni su RPCProxyEnabled, vedere [http RPC Security](/windows/desktop/Rpc/rpc-over-http-security).</span><span class="sxs-lookup"><span data-stu-id="3ff88-379">For more information on RPCProxyEnabled, see [HTTP RPC Security](/windows/desktop/Rpc/rpc-over-http-security).</span></span> |
| <span data-ttu-id="3ff88-380">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-380">Access</span></span>         | <span data-ttu-id="3ff88-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-381">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3ff88-382">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-382">Type</span></span>           | <span data-ttu-id="3ff88-383">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-383">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3ff88-384">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-384">Default</span></span>        | <span data-ttu-id="3ff88-385">Falso</span><span class="sxs-lookup"><span data-stu-id="3ff88-385">False</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3ff88-386">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-386">Minimum system</span></span> | <span data-ttu-id="3ff88-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-387">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a><span data-ttu-id="3ff88-388">SecureReferencesEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-388">SecureReferencesEnabled</span></span>



| <span data-ttu-id="3ff88-389">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-389">Entry</span></span> | <span data-ttu-id="3ff88-390">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-391">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-391">Description</span></span>    | <span data-ttu-id="3ff88-392">Impone nei computer DCOM che le chiamate tra più processi ai metodi [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) siano protette.</span><span class="sxs-lookup"><span data-stu-id="3ff88-392">Enforces in DCOM computers that cross-process calls to [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are secured.</span></span> |
| <span data-ttu-id="3ff88-393">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-393">Access</span></span>         | <span data-ttu-id="3ff88-394">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-394">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="3ff88-395">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-395">Type</span></span>           | <span data-ttu-id="3ff88-396">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-396">Bool</span></span>                                                                                                                                                                      |
| <span data-ttu-id="3ff88-397">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-397">Default</span></span>        | <span data-ttu-id="3ff88-398">Falso</span><span class="sxs-lookup"><span data-stu-id="3ff88-398">False</span></span>                                                                                                                                                                     |
| <span data-ttu-id="3ff88-399">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-399">Minimum system</span></span> | <span data-ttu-id="3ff88-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-400">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a><span data-ttu-id="3ff88-401">SecurityTrackingEnabled</span><span class="sxs-lookup"><span data-stu-id="3ff88-401">SecurityTrackingEnabled</span></span>



| <span data-ttu-id="3ff88-402">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-402">Entry</span></span> | <span data-ttu-id="3ff88-403">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-403">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="3ff88-404">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-404">Description</span></span>    | <span data-ttu-id="3ff88-405">Impostare su true se il rilevamento di sicurezza è abilitato per gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="3ff88-405">Set to True if security tracking is enabled on objects.</span></span> |
| <span data-ttu-id="3ff88-406">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-406">Access</span></span>         | <span data-ttu-id="3ff88-407">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-407">ReadWrite</span></span>                                               |
| <span data-ttu-id="3ff88-408">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-408">Type</span></span>           | <span data-ttu-id="3ff88-409">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-409">Bool</span></span>                                                    |
| <span data-ttu-id="3ff88-410">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-410">Default</span></span>        | <span data-ttu-id="3ff88-411">Vero</span><span class="sxs-lookup"><span data-stu-id="3ff88-411">True</span></span>                                                    |
| <span data-ttu-id="3ff88-412">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-412">Minimum system</span></span> | <span data-ttu-id="3ff88-413">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-413">Windows 2000</span></span>                                            |



 

### <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="3ff88-414">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="3ff88-414">SRPActivateAsActivatorChecks</span></span>



| <span data-ttu-id="3ff88-415">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-415">Entry</span></span> | <span data-ttu-id="3ff88-416">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-416">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-417">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-417">Description</span></span>    | <span data-ttu-id="3ff88-418">Determina il modo in cui i criteri di restrizione software gestiscono le connessioni Activate-As-Activator.</span><span class="sxs-lookup"><span data-stu-id="3ff88-418">Determines how the software restriction policy (SRP) handles activate-as-activator connections.</span></span> <span data-ttu-id="3ff88-419">Se è impostato su true, il livello di attendibilità SRP configurato per l'oggetto server viene confrontato con il livello di attendibilità SRP dell'oggetto client e il livello di attendibilità superiore (più rigoroso) viene utilizzato per eseguire l'oggetto server.</span><span class="sxs-lookup"><span data-stu-id="3ff88-419">If set to True, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and the higher (more stringent) trust level is used to run the server object.</span></span> <span data-ttu-id="3ff88-420">Se impostato su false, l'oggetto server viene eseguito con il livello di attendibilità SRP dell'oggetto client, indipendentemente dal livello di attendibilità SRP con cui è configurato il server.</span><span class="sxs-lookup"><span data-stu-id="3ff88-420">If set to False, the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which the server is configured.</span></span> |
| <span data-ttu-id="3ff88-421">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-421">Access</span></span>         | <span data-ttu-id="3ff88-422">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-422">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3ff88-423">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-423">Type</span></span>           | <span data-ttu-id="3ff88-424">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-424">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3ff88-425">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-425">Default</span></span>        | <span data-ttu-id="3ff88-426">Vero</span><span class="sxs-lookup"><span data-stu-id="3ff88-426">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3ff88-427">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-427">Minimum system</span></span> | <span data-ttu-id="3ff88-428">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3ff88-428">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a><span data-ttu-id="3ff88-429">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="3ff88-429">SRPRunningObjectChecks</span></span>



| <span data-ttu-id="3ff88-430">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-430">Entry</span></span> | <span data-ttu-id="3ff88-431">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-431">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-432">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-432">Description</span></span>    | <span data-ttu-id="3ff88-433">Determina il modo in cui il criterio di restrizione software gestisce i tentativi di connessione ai processi esistenti.</span><span class="sxs-lookup"><span data-stu-id="3ff88-433">Determines how the software restriction policy (SRP) handles attempted connections to existing processes.</span></span> <span data-ttu-id="3ff88-434">Se è impostato su false, i tentativi di connessione agli oggetti in esecuzione non vengono controllati per i livelli di attendibilità SRP appropriati.</span><span class="sxs-lookup"><span data-stu-id="3ff88-434">If set to False, attempts to connect to running objects are not checked for appropriate SRP trust levels.</span></span> <span data-ttu-id="3ff88-435">Se è impostato su true, l'oggetto in esecuzione deve disporre di un livello di attendibilità uguale o superiore (più rigoroso) SRP rispetto all'oggetto client.</span><span class="sxs-lookup"><span data-stu-id="3ff88-435">If set to True, the running object must have an equal or higher (more stringent) SRP trust level than the client object.</span></span> <span data-ttu-id="3ff88-436">Ad esempio, un oggetto client con un livello di attendibilità non limitato non può connettersi a un oggetto in esecuzione con un livello di attendibilità non consentito.</span><span class="sxs-lookup"><span data-stu-id="3ff88-436">For example, a client object with an Unrestricted SRP trust level cannot connect to a running object with a Disallowed SRP trust level.</span></span> |
| <span data-ttu-id="3ff88-437">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-437">Access</span></span>         | <span data-ttu-id="3ff88-438">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-438">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3ff88-439">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-439">Type</span></span>           | <span data-ttu-id="3ff88-440">Bool</span><span class="sxs-lookup"><span data-stu-id="3ff88-440">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3ff88-441">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-441">Default</span></span>        | <span data-ttu-id="3ff88-442">Vero</span><span class="sxs-lookup"><span data-stu-id="3ff88-442">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3ff88-443">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-443">Minimum system</span></span> | <span data-ttu-id="3ff88-444">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3ff88-444">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a><span data-ttu-id="3ff88-445">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="3ff88-445">TransactionTimeout</span></span>



| <span data-ttu-id="3ff88-446">Voce</span><span class="sxs-lookup"><span data-stu-id="3ff88-446">Entry</span></span> | <span data-ttu-id="3ff88-447">Valore</span><span class="sxs-lookup"><span data-stu-id="3ff88-447">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff88-448">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ff88-448">Description</span></span>    | <span data-ttu-id="3ff88-449">Deve essere impostato su un valore sufficiente in secondi se si eseguono numerose operazioni all'interno di una transazione.</span><span class="sxs-lookup"><span data-stu-id="3ff88-449">Should be set to a sufficient value in seconds if you are doing numerous operations within a transaction.</span></span> <span data-ttu-id="3ff88-450">Il periodo di timeout predefinito è di 60 secondi e il periodo di timeout massimo è di 3600 secondi (1 ora).</span><span class="sxs-lookup"><span data-stu-id="3ff88-450">The default time-out period is 60 seconds, and the maximum time-out period is 3600 seconds (1 hour).</span></span> <span data-ttu-id="3ff88-451">L'impostazione di questa proprietà su 0 Disabilita i timeout delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="3ff88-451">Setting this property to 0 disables transaction time-outs.</span></span> <span data-ttu-id="3ff88-452">Questa proprietà può essere sottoposta a override dai singoli componenti utilizzando la proprietà ComponentTransactionTimeout della raccolta [**Components**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="3ff88-452">This property can be overridden by individual components by using the ComponentTransactionTimeout property of the [**Components**](components.md) collection.</span></span> |
| <span data-ttu-id="3ff88-453">Access</span><span class="sxs-lookup"><span data-stu-id="3ff88-453">Access</span></span>         | <span data-ttu-id="3ff88-454">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ff88-454">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="3ff88-455">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff88-455">Type</span></span>           | <span data-ttu-id="3ff88-456">Long (0-3600)</span><span class="sxs-lookup"><span data-stu-id="3ff88-456">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3ff88-457">Predefinito</span><span class="sxs-lookup"><span data-stu-id="3ff88-457">Default</span></span>        | <span data-ttu-id="3ff88-458">60</span><span class="sxs-lookup"><span data-stu-id="3ff88-458">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3ff88-459">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="3ff88-459">Minimum system</span></span> | <span data-ttu-id="3ff88-460">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3ff88-460">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a><span data-ttu-id="3ff88-461">Esempio</span><span class="sxs-lookup"><span data-stu-id="3ff88-461">Example</span></span>

<span data-ttu-id="3ff88-462">Nell'esempio di Visual Basic Microsoft riportato di seguito viene illustrato come connettersi a un computer remoto e ottenere la relativa proprietà SecurityTrackingEnabled tramite la raccolta **LocalComputer** del computer remoto.</span><span class="sxs-lookup"><span data-stu-id="3ff88-462">The following Microsoft Visual Basic example demonstrates how to connect to a remote computer and get its SecurityTrackingEnabled property by using the **LocalComputer** collection of the remote computer.</span></span> <span data-ttu-id="3ff88-463">Per usare questo esempio, aggiungere la libreria dei tipi di amministrazione COM+ come riferimento al progetto Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3ff88-463">To use this example, add the COM+ Admin Type Library as a reference to your Visual Basic project.</span></span>


```VB
Function RemoteComputerConnect(strComputer As String _
) As Boolean  ' Return False if any errors occur.
    
    RemoteComputerConnect = False   ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim boolSTE As Boolean
    Dim objCatalog As COMAdminCatalog
    Dim objRemoteRootColl As COMAdminCatalogCollection
    Dim objRemoteComputerColl As COMAdminCatalogCollection
    Dim objRemoteComputerItem As COMAdminCatalogObject
    
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objRemoteRootColl = objCatalog.Connect(strComputer)
    Set objRemoteComputerColl = objRemoteRootColl.GetCollection( _
      "LocalComputer", objRemoteRootColl.Name)
    objRemoteComputerColl.Populate
    Set objRemoteComputerItem = objRemoteComputerColl.Item(0)
    boolSTE = objRemoteComputerItem.Value("SecurityTrackingEnabled")
    If boolSTE Then
        MsgBox "Security Tracking is enabled on " & strComputer
    Else
        MsgBox "Security Tracking is NOT enabled on " & strComputer
    End If

    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
    RemoteComputerConnect = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
End Function


```



<span data-ttu-id="3ff88-464">Per usare la funzione, fornire un valore stringa per il nome del computer remoto.</span><span class="sxs-lookup"><span data-stu-id="3ff88-464">To use the function, provide a string value for the name of the remote computer.</span></span> <span data-ttu-id="3ff88-465">Il codice di Visual Basic seguente illustra come connettersi al computer denominato "NomeComputerRemoto".</span><span class="sxs-lookup"><span data-stu-id="3ff88-465">The following Visual Basic code shows how to connect to the computer named "RemoteComputerName".</span></span>


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a><span data-ttu-id="3ff88-466">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ff88-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ff88-467">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="3ff88-467">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
