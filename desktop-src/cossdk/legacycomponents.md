---
description: Contiene un oggetto per ogni componente non configurato nella raccolta di applicazioni. I componenti non configurati non possono utilizzare i servizi COM+. Le proprietà esposte da questi oggetti contengono impostazioni effettuate a livello di componente.
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: Raccolta LegacyComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyComponents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5761950dcb0ceb5c857daf37ba2236733ec30c22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748175"
---
# <a name="legacycomponents-collection"></a><span data-ttu-id="244bc-105">Raccolta LegacyComponents</span><span class="sxs-lookup"><span data-stu-id="244bc-105">LegacyComponents collection</span></span>

<span data-ttu-id="244bc-106">Contiene un oggetto per ogni componente non configurato nella raccolta di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="244bc-106">Contains an object for each unconfigured component in the Applications collection.</span></span> <span data-ttu-id="244bc-107">I componenti non configurati non possono utilizzare i servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="244bc-107">Unconfigured components cannot make use of COM+ services.</span></span> <span data-ttu-id="244bc-108">Le proprietà esposte da questi oggetti contengono impostazioni effettuate a livello di componente.</span><span class="sxs-lookup"><span data-stu-id="244bc-108">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="244bc-109">Questa raccolta supporta il metodo [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , ma non il metodo [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="244bc-109">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="244bc-110">Per installare o importare componenti in un'applicazione, usare i metodi sull'oggetto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="244bc-110">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="244bc-111">Membri</span><span class="sxs-lookup"><span data-stu-id="244bc-111">Members</span></span>

<span data-ttu-id="244bc-112">La raccolta **LegacyComponents** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="244bc-112">The **LegacyComponents** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="244bc-113">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="244bc-113">Related Collections</span></span>

<span data-ttu-id="244bc-114">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="244bc-114">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="244bc-115">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="244bc-115">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="244bc-116">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="244bc-116">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="244bc-117">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="244bc-117">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="244bc-118">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="244bc-118">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="244bc-119">**Applicazioni**</span><span class="sxs-lookup"><span data-stu-id="244bc-119">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="244bc-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="244bc-120">Properties</span></span>

<span data-ttu-id="244bc-121">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="244bc-121">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="244bc-122">AccessPermissions</span><span class="sxs-lookup"><span data-stu-id="244bc-122">AccessPermissions</span></span>](#accesspermissions)
-   [<span data-ttu-id="244bc-123">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="244bc-123">ActivateAtStorage</span></span>](#activateatstorage)
-   [<span data-ttu-id="244bc-124">AppID</span><span class="sxs-lookup"><span data-stu-id="244bc-124">AppID</span></span>](#appid)
-   [<span data-ttu-id="244bc-125">AppName</span><span class="sxs-lookup"><span data-stu-id="244bc-125">AppName</span></span>](#appname)
-   [<span data-ttu-id="244bc-126">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="244bc-126">AuthenticationLevel</span></span>](#authenticationlevel)
-   [<span data-ttu-id="244bc-127">Numero di bit</span><span class="sxs-lookup"><span data-stu-id="244bc-127">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="244bc-128">ClassName</span><span class="sxs-lookup"><span data-stu-id="244bc-128">ClassName</span></span>](#classname)
-   [<span data-ttu-id="244bc-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="244bc-129">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="244bc-130">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="244bc-130">DllSurrogate</span></span>](#dllsurrogate)
-   [<span data-ttu-id="244bc-131">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="244bc-131">InprocHandler32</span></span>](#inprochandler32)
-   [<span data-ttu-id="244bc-132">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="244bc-132">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="244bc-133">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="244bc-133">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="244bc-134">LaunchPermissions</span><span class="sxs-lookup"><span data-stu-id="244bc-134">LaunchPermissions</span></span>](#launchpermissions)
-   [<span data-ttu-id="244bc-135">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="244bc-135">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="244bc-136">LocalService</span><span class="sxs-lookup"><span data-stu-id="244bc-136">LocalService</span></span>](#localservice)
-   [<span data-ttu-id="244bc-137">Password</span><span class="sxs-lookup"><span data-stu-id="244bc-137">Password</span></span>](#password)
-   [<span data-ttu-id="244bc-138">ProgID</span><span class="sxs-lookup"><span data-stu-id="244bc-138">ProgID</span></span>](#progid)
-   [<span data-ttu-id="244bc-139">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="244bc-139">RemoteServer</span></span>](#remoteserver)
-   [<span data-ttu-id="244bc-140">RunAs</span><span class="sxs-lookup"><span data-stu-id="244bc-140">RunAs</span></span>](#runas)
-   [<span data-ttu-id="244bc-141">ServiceParameter</span><span class="sxs-lookup"><span data-stu-id="244bc-141">ServiceParameter</span></span>](#serviceparameter)
-   [<span data-ttu-id="244bc-142">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="244bc-142">SRPTrustLevel</span></span>](#srptrustlevel)
-   [<span data-ttu-id="244bc-143">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="244bc-143">ThreadingModel</span></span>](#threadingmodel)

### <a name="accesspermissions"></a><span data-ttu-id="244bc-144">AccessPermissions</span><span class="sxs-lookup"><span data-stu-id="244bc-144">AccessPermissions</span></span>



| <span data-ttu-id="244bc-145">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-145">Entry</span></span> | <span data-ttu-id="244bc-146">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-146">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-147">Description</span></span>    | <span data-ttu-id="244bc-148">Specifica gli account utente a cui è consentito o negato l'accesso al componente.</span><span class="sxs-lookup"><span data-stu-id="244bc-148">Specifies the user accounts that are allowed or denied access to the component.</span></span> |
| <span data-ttu-id="244bc-149">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-149">Access</span></span>         | <span data-ttu-id="244bc-150">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-150">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="244bc-151">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-151">Type</span></span>           | <span data-ttu-id="244bc-152">string</span><span class="sxs-lookup"><span data-stu-id="244bc-152">String</span></span>                                                                          |
| <span data-ttu-id="244bc-153">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-153">Default</span></span>        | <span data-ttu-id="244bc-154">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-154">N/A</span></span>                                                                             |
| <span data-ttu-id="244bc-155">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-155">Minimum system</span></span> | <span data-ttu-id="244bc-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-156">Windows XP</span></span>                                                                      |



 

### <a name="activateatstorage"></a><span data-ttu-id="244bc-157">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="244bc-157">ActivateAtStorage</span></span>



| <span data-ttu-id="244bc-158">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-158">Entry</span></span> | <span data-ttu-id="244bc-159">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-159">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="244bc-160">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-160">Description</span></span>    | <span data-ttu-id="244bc-161">Specifica se eseguire il server nel computer di archiviazione dati.</span><span class="sxs-lookup"><span data-stu-id="244bc-161">Specifies whether to run the server on the data storage machine.</span></span> |
| <span data-ttu-id="244bc-162">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-162">Access</span></span>         | <span data-ttu-id="244bc-163">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-163">ReadWrite</span></span>                                                        |
| <span data-ttu-id="244bc-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="244bc-164">Type</span></span>           | <span data-ttu-id="244bc-165">Stringa valori possibili: "N" "Y"</span><span class="sxs-lookup"><span data-stu-id="244bc-165">String Possible values:"N""Y"</span></span>                                    |
| <span data-ttu-id="244bc-166">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-166">Default</span></span>        | <span data-ttu-id="244bc-167">"N"</span><span class="sxs-lookup"><span data-stu-id="244bc-167">"N"</span></span>                                                              |
| <span data-ttu-id="244bc-168">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-168">Minimum system</span></span> | <span data-ttu-id="244bc-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-169">Windows XP</span></span>                                                       |



 

### <a name="appid"></a><span data-ttu-id="244bc-170">AppID</span><span class="sxs-lookup"><span data-stu-id="244bc-170">AppID</span></span>



| <span data-ttu-id="244bc-171">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-171">Entry</span></span> | <span data-ttu-id="244bc-172">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-172">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="244bc-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-173">Description</span></span>    | <span data-ttu-id="244bc-174">ID applicazione.</span><span class="sxs-lookup"><span data-stu-id="244bc-174">The application ID.</span></span> |
| <span data-ttu-id="244bc-175">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-175">Access</span></span>         | <span data-ttu-id="244bc-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="244bc-176">ReadOnly</span></span>            |
| <span data-ttu-id="244bc-177">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-177">Type</span></span>           | <span data-ttu-id="244bc-178">string</span><span class="sxs-lookup"><span data-stu-id="244bc-178">String</span></span>              |
| <span data-ttu-id="244bc-179">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-179">Default</span></span>        | <span data-ttu-id="244bc-180">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-180">N/A</span></span>                 |
| <span data-ttu-id="244bc-181">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-181">Minimum system</span></span> | <span data-ttu-id="244bc-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-182">Windows XP</span></span>          |



 

### <a name="appname"></a><span data-ttu-id="244bc-183">AppName</span><span class="sxs-lookup"><span data-stu-id="244bc-183">AppName</span></span>



| <span data-ttu-id="244bc-184">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-184">Entry</span></span> | <span data-ttu-id="244bc-185">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-185">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="244bc-186">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-186">Description</span></span>    | <span data-ttu-id="244bc-187">Nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="244bc-187">The name of the application.</span></span> |
| <span data-ttu-id="244bc-188">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-188">Access</span></span>         | <span data-ttu-id="244bc-189">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="244bc-189">ReadOnly</span></span>                     |
| <span data-ttu-id="244bc-190">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-190">Type</span></span>           | <span data-ttu-id="244bc-191">string</span><span class="sxs-lookup"><span data-stu-id="244bc-191">String</span></span>                       |
| <span data-ttu-id="244bc-192">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-192">Default</span></span>        | <span data-ttu-id="244bc-193">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-193">N/A</span></span>                          |
| <span data-ttu-id="244bc-194">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-194">Minimum system</span></span> | <span data-ttu-id="244bc-195">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-195">Windows XP</span></span>                   |



 

### <a name="authenticationlevel"></a><span data-ttu-id="244bc-196">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="244bc-196">AuthenticationLevel</span></span>



| <span data-ttu-id="244bc-197">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-197">Entry</span></span> | <span data-ttu-id="244bc-198">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-198">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-199">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-199">Description</span></span>    | <span data-ttu-id="244bc-200">Imposta il livello di autenticazione per le chiamate, con i valori corrispondenti alle impostazioni di autenticazione RPC (Remote Procedure Call).</span><span class="sxs-lookup"><span data-stu-id="244bc-200">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="244bc-201">Quando si sceglie COMAdminAuthenticationDefault, viene utilizzata l'impostazione nella proprietà DefaultAuthenticationLevel all'interno della raccolta [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="244bc-201">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="244bc-202">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-202">Access</span></span>         | <span data-ttu-id="244bc-203">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-203">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="244bc-204">Tipo</span><span class="sxs-lookup"><span data-stu-id="244bc-204">Type</span></span>           | <span data-ttu-id="244bc-205">Valori lunghi possibili: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="244bc-205">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="244bc-206">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-206">Default</span></span>        | <span data-ttu-id="244bc-207">COMAdminAuthenticationDefault (0)</span><span class="sxs-lookup"><span data-stu-id="244bc-207">COMAdminAuthenticationDefault (0)</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="244bc-208">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-208">Minimum system</span></span> | <span data-ttu-id="244bc-209">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-209">Windows XP</span></span>                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> <span data-ttu-id="244bc-210">Si consiglia di usare le costanti nell'enumerazione e non i valori numerici.</span><span class="sxs-lookup"><span data-stu-id="244bc-210">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="bitness"></a><span data-ttu-id="244bc-211">Numero di bit</span><span class="sxs-lookup"><span data-stu-id="244bc-211">Bitness</span></span>



| <span data-ttu-id="244bc-212">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-212">Entry</span></span> | <span data-ttu-id="244bc-213">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-213">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-214">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-214">Description</span></span>    | <span data-ttu-id="244bc-215">Rappresenta il tipo binario bit del componente.</span><span class="sxs-lookup"><span data-stu-id="244bc-215">Represents the binary bitness type of the component.</span></span> <span data-ttu-id="244bc-216">Nei sistemi che utilizzano Windows a 64 bit, questa proprietà distingue tra i componenti a 64 bit e i componenti a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="244bc-216">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="244bc-217">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-217">Access</span></span>         | <span data-ttu-id="244bc-218">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="244bc-218">ReadOnly</span></span>                                                                                                                                                              |
| <span data-ttu-id="244bc-219">Tipo</span><span class="sxs-lookup"><span data-stu-id="244bc-219">Type</span></span>           | <span data-ttu-id="244bc-220">Valori lunghi possibili: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)</span><span class="sxs-lookup"><span data-stu-id="244bc-220">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                         |
| <span data-ttu-id="244bc-221">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-221">Default</span></span>        | <span data-ttu-id="244bc-222">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-222">N/A</span></span>                                                                                                                                                                   |
| <span data-ttu-id="244bc-223">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-223">Minimum system</span></span> | <span data-ttu-id="244bc-224">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-224">Windows XP</span></span>                                                                                                                                                            |



 

### <a name="classname"></a><span data-ttu-id="244bc-225">ClassName</span><span class="sxs-lookup"><span data-stu-id="244bc-225">ClassName</span></span>



| <span data-ttu-id="244bc-226">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-226">Entry</span></span> | <span data-ttu-id="244bc-227">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-227">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="244bc-228">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-228">Description</span></span>    | <span data-ttu-id="244bc-229">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="244bc-229">The name of the class.</span></span> |
| <span data-ttu-id="244bc-230">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-230">Access</span></span>         | <span data-ttu-id="244bc-231">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="244bc-231">ReadOnly</span></span>               |
| <span data-ttu-id="244bc-232">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-232">Type</span></span>           | <span data-ttu-id="244bc-233">string</span><span class="sxs-lookup"><span data-stu-id="244bc-233">String</span></span>                 |
| <span data-ttu-id="244bc-234">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-234">Default</span></span>        | <span data-ttu-id="244bc-235">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-235">N/A</span></span>                    |
| <span data-ttu-id="244bc-236">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-236">Minimum system</span></span> | <span data-ttu-id="244bc-237">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-237">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="244bc-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="244bc-238">CLSID</span></span>



| <span data-ttu-id="244bc-239">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-239">Entry</span></span> | <span data-ttu-id="244bc-240">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-240">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-241">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-241">Description</span></span>    | <span data-ttu-id="244bc-242">GUID per il componente.</span><span class="sxs-lookup"><span data-stu-id="244bc-242">A GUID for the component.</span></span> <span data-ttu-id="244bc-243">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="244bc-243">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="244bc-244">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-244">Access</span></span>         | <span data-ttu-id="244bc-245">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="244bc-245">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="244bc-246">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-246">Type</span></span>           | <span data-ttu-id="244bc-247">string</span><span class="sxs-lookup"><span data-stu-id="244bc-247">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="244bc-248">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-248">Default</span></span>        | <span data-ttu-id="244bc-249">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-249">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="244bc-250">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-250">Minimum system</span></span> | <span data-ttu-id="244bc-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-251">Windows XP</span></span>                                                                                                                                                |



 

### <a name="dllsurrogate"></a><span data-ttu-id="244bc-252">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="244bc-252">DllSurrogate</span></span>



| <span data-ttu-id="244bc-253">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-253">Entry</span></span> | <span data-ttu-id="244bc-254">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-254">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="244bc-255">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-255">Description</span></span>    | <span data-ttu-id="244bc-256">Specifica il percorso completo di un'applicazione server surragate.</span><span class="sxs-lookup"><span data-stu-id="244bc-256">Specifies the full path to a surragate server application.</span></span> |
| <span data-ttu-id="244bc-257">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-257">Access</span></span>         | <span data-ttu-id="244bc-258">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-258">ReadWrite</span></span>                                                  |
| <span data-ttu-id="244bc-259">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-259">Type</span></span>           | <span data-ttu-id="244bc-260">string</span><span class="sxs-lookup"><span data-stu-id="244bc-260">String</span></span>                                                     |
| <span data-ttu-id="244bc-261">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-261">Default</span></span>        | <span data-ttu-id="244bc-262">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-262">N/A</span></span>                                                        |
| <span data-ttu-id="244bc-263">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-263">Minimum system</span></span> | <span data-ttu-id="244bc-264">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-264">Windows XP</span></span>                                                 |



 

### <a name="inprochandler32"></a><span data-ttu-id="244bc-265">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="244bc-265">InprocHandler32</span></span>



| <span data-ttu-id="244bc-266">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-266">Entry</span></span> | <span data-ttu-id="244bc-267">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-267">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="244bc-268">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-268">Description</span></span>    | <span data-ttu-id="244bc-269">Specifica il percorso completo di una DLL del gestore personalizzato in-process a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="244bc-269">Specifies the full path to a 32-bit in-process custom handler DLL.</span></span> |
| <span data-ttu-id="244bc-270">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-270">Access</span></span>         | <span data-ttu-id="244bc-271">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-271">ReadWrite</span></span>                                                          |
| <span data-ttu-id="244bc-272">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-272">Type</span></span>           | <span data-ttu-id="244bc-273">string</span><span class="sxs-lookup"><span data-stu-id="244bc-273">String</span></span>                                                             |
| <span data-ttu-id="244bc-274">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-274">Default</span></span>        | <span data-ttu-id="244bc-275">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-275">N/A</span></span>                                                                |
| <span data-ttu-id="244bc-276">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-276">Minimum system</span></span> | <span data-ttu-id="244bc-277">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-277">Windows XP</span></span>                                                         |



 

### <a name="inprocserver32"></a><span data-ttu-id="244bc-278">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="244bc-278">InprocServer32</span></span>



| <span data-ttu-id="244bc-279">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-279">Entry</span></span> | <span data-ttu-id="244bc-280">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-280">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="244bc-281">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-281">Description</span></span>    | <span data-ttu-id="244bc-282">Specifica il percorso completo di una DLL del server in-process a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="244bc-282">Specifies the full path to a 32-bit in-process server DLL.</span></span> |
| <span data-ttu-id="244bc-283">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-283">Access</span></span>         | <span data-ttu-id="244bc-284">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-284">ReadWrite</span></span>                                                  |
| <span data-ttu-id="244bc-285">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-285">Type</span></span>           | <span data-ttu-id="244bc-286">string</span><span class="sxs-lookup"><span data-stu-id="244bc-286">String</span></span>                                                     |
| <span data-ttu-id="244bc-287">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-287">Default</span></span>        | <span data-ttu-id="244bc-288">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-288">N/A</span></span>                                                        |
| <span data-ttu-id="244bc-289">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-289">Minimum system</span></span> | <span data-ttu-id="244bc-290">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-290">Windows XP</span></span>                                                 |



 

### <a name="isenabled"></a><span data-ttu-id="244bc-291">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="244bc-291">IsEnabled</span></span>



| <span data-ttu-id="244bc-292">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-292">Entry</span></span> | <span data-ttu-id="244bc-293">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-293">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-294">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-294">Description</span></span>    | <span data-ttu-id="244bc-295">Se l'applicazione o il componente COM+ è disabilitato, IsEnabled è false.</span><span class="sxs-lookup"><span data-stu-id="244bc-295">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="244bc-296">Se l'applicazione o il componente COM+ è abilitato, IsEnabled è true.</span><span class="sxs-lookup"><span data-stu-id="244bc-296">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="244bc-297">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-297">Access</span></span>         | <span data-ttu-id="244bc-298">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-298">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="244bc-299">Tipo</span><span class="sxs-lookup"><span data-stu-id="244bc-299">Type</span></span>           | <span data-ttu-id="244bc-300">Bool</span><span class="sxs-lookup"><span data-stu-id="244bc-300">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="244bc-301">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-301">Default</span></span>        | <span data-ttu-id="244bc-302">Vero</span><span class="sxs-lookup"><span data-stu-id="244bc-302">True</span></span>                                                                                                                                      |
| <span data-ttu-id="244bc-303">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-303">Minimum system</span></span> | <span data-ttu-id="244bc-304">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-304">Windows XP</span></span>                                                                                                                                |



 

### <a name="launchpermissions"></a><span data-ttu-id="244bc-305">LaunchPermissions</span><span class="sxs-lookup"><span data-stu-id="244bc-305">LaunchPermissions</span></span>



| <span data-ttu-id="244bc-306">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-306">Entry</span></span> | <span data-ttu-id="244bc-307">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-307">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-308">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-308">Description</span></span>    | <span data-ttu-id="244bc-309">Specifica gli account utente per i quali è consentita o negata l'autorizzazione per avviare il componente.</span><span class="sxs-lookup"><span data-stu-id="244bc-309">Specifies user accounts that are allowed or denied permission to start this component.</span></span> |
| <span data-ttu-id="244bc-310">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-310">Access</span></span>         | <span data-ttu-id="244bc-311">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-311">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="244bc-312">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-312">Type</span></span>           | <span data-ttu-id="244bc-313">string</span><span class="sxs-lookup"><span data-stu-id="244bc-313">String</span></span>                                                                                 |
| <span data-ttu-id="244bc-314">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-314">Default</span></span>        | <span data-ttu-id="244bc-315">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-315">N/A</span></span>                                                                                    |
| <span data-ttu-id="244bc-316">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-316">Minimum system</span></span> | <span data-ttu-id="244bc-317">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-317">Windows XP</span></span>                                                                             |



 

### <a name="localserver32"></a><span data-ttu-id="244bc-318">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="244bc-318">LocalServer32</span></span>



| <span data-ttu-id="244bc-319">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-319">Entry</span></span> | <span data-ttu-id="244bc-320">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-320">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-321">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-321">Description</span></span>    | <span data-ttu-id="244bc-322">Specifica il percorso completo di un'applicazione server locale a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="244bc-322">Specifies the full path to a 32-bit local server application.</span></span> <span data-ttu-id="244bc-323">Per proteggere la sicurezza del sistema, usare stringhe tra virgolette nel percorso per indicare dove termina il nome file eseguibile e gli argomenti iniziano.</span><span class="sxs-lookup"><span data-stu-id="244bc-323">To help protect system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="244bc-324">Ad esempio, " \\ " C: \\ programmi \\ aziendali file \\Application.exe\\ "param1 param2".</span><span class="sxs-lookup"><span data-stu-id="244bc-324">For example, "\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2".</span></span> |
| <span data-ttu-id="244bc-325">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-325">Access</span></span>         | <span data-ttu-id="244bc-326">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="244bc-327">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-327">Type</span></span>           | <span data-ttu-id="244bc-328">string</span><span class="sxs-lookup"><span data-stu-id="244bc-328">String</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="244bc-329">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-329">Default</span></span>        | <span data-ttu-id="244bc-330">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-330">N/A</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="244bc-331">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-331">Minimum system</span></span> | <span data-ttu-id="244bc-332">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-332">Windows XP</span></span>                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a><span data-ttu-id="244bc-333">LocalService</span><span class="sxs-lookup"><span data-stu-id="244bc-333">LocalService</span></span>



| <span data-ttu-id="244bc-334">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-334">Entry</span></span> | <span data-ttu-id="244bc-335">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-335">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="244bc-336">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-336">Description</span></span>    | <span data-ttu-id="244bc-337">Specifica il percorso completo dell'applicazione di servizio.</span><span class="sxs-lookup"><span data-stu-id="244bc-337">Specifies the full path to the service application.</span></span> |
| <span data-ttu-id="244bc-338">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-338">Access</span></span>         | <span data-ttu-id="244bc-339">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-339">ReadWrite</span></span>                                           |
| <span data-ttu-id="244bc-340">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-340">Type</span></span>           | <span data-ttu-id="244bc-341">string</span><span class="sxs-lookup"><span data-stu-id="244bc-341">String</span></span>                                              |
| <span data-ttu-id="244bc-342">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-342">Default</span></span>        | <span data-ttu-id="244bc-343">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-343">N/A</span></span>                                                 |
| <span data-ttu-id="244bc-344">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-344">Minimum system</span></span> | <span data-ttu-id="244bc-345">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-345">Windows XP</span></span>                                          |



 

### <a name="password"></a><span data-ttu-id="244bc-346">Password</span><span class="sxs-lookup"><span data-stu-id="244bc-346">Password</span></span>



| <span data-ttu-id="244bc-347">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-347">Entry</span></span> | <span data-ttu-id="244bc-348">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-348">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-349">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-349">Description</span></span>    | <span data-ttu-id="244bc-350">Imposta la password utilizzata dal processo server per accedere con l'identità RunAs specificata.</span><span class="sxs-lookup"><span data-stu-id="244bc-350">Sets the password used by the server process to log on under the specified RunAs identity.</span></span> <span data-ttu-id="244bc-351">È necessario impostare la password contemporaneamente all'identità RunAs, prima di usare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), perché la password e l'identità vengono convalidate prima di essere salvate.</span><span class="sxs-lookup"><span data-stu-id="244bc-351">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="244bc-352">Se la password e l'identità non vengono sincronizzate, il componente non può essere avviato finché non viene reimpostato da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="244bc-352">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="244bc-353">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-353">Access</span></span>         | <span data-ttu-id="244bc-354">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="244bc-354">WriteOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="244bc-355">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-355">Type</span></span>           | <span data-ttu-id="244bc-356">string</span><span class="sxs-lookup"><span data-stu-id="244bc-356">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="244bc-357">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-357">Default</span></span>        | <span data-ttu-id="244bc-358">NULL</span><span class="sxs-lookup"><span data-stu-id="244bc-358">NULL</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="244bc-359">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-359">Minimum system</span></span> | <span data-ttu-id="244bc-360">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-360">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a><span data-ttu-id="244bc-361">ProgID</span><span class="sxs-lookup"><span data-stu-id="244bc-361">ProgID</span></span>



| <span data-ttu-id="244bc-362">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-362">Entry</span></span> | <span data-ttu-id="244bc-363">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-363">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-364">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-364">Description</span></span>    | <span data-ttu-id="244bc-365">Nome che identifica il componente.</span><span class="sxs-lookup"><span data-stu-id="244bc-365">A name identifying the component.</span></span> <span data-ttu-id="244bc-366">Questa proprietà viene restituita quando il metodo della proprietà Name viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="244bc-366">This property is returned when the Name property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="244bc-367">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-367">Access</span></span>         | <span data-ttu-id="244bc-368">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="244bc-368">ReadOnly</span></span>                                                                                                                             |
| <span data-ttu-id="244bc-369">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-369">Type</span></span>           | <span data-ttu-id="244bc-370">string</span><span class="sxs-lookup"><span data-stu-id="244bc-370">String</span></span>                                                                                                                               |
| <span data-ttu-id="244bc-371">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-371">Default</span></span>        | <span data-ttu-id="244bc-372">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-372">N/A</span></span>                                                                                                                                  |
| <span data-ttu-id="244bc-373">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-373">Minimum system</span></span> | <span data-ttu-id="244bc-374">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-374">Windows XP</span></span>                                                                                                                           |



 

### <a name="remoteserver"></a><span data-ttu-id="244bc-375">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="244bc-375">RemoteServer</span></span>



| <span data-ttu-id="244bc-376">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-376">Entry</span></span> | <span data-ttu-id="244bc-377">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-377">Value</span></span> |
|----------------|---------------------------------------|
| <span data-ttu-id="244bc-378">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-378">Description</span></span>    | <span data-ttu-id="244bc-379">Specifica il computer server remoto.</span><span class="sxs-lookup"><span data-stu-id="244bc-379">Specifies the remote server computer.</span></span> |
| <span data-ttu-id="244bc-380">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-380">Access</span></span>         | <span data-ttu-id="244bc-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-381">ReadWrite</span></span>                             |
| <span data-ttu-id="244bc-382">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-382">Type</span></span>           | <span data-ttu-id="244bc-383">string</span><span class="sxs-lookup"><span data-stu-id="244bc-383">String</span></span>                                |
| <span data-ttu-id="244bc-384">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-384">Default</span></span>        | <span data-ttu-id="244bc-385">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-385">N/A</span></span>                                   |
| <span data-ttu-id="244bc-386">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-386">Minimum system</span></span> | <span data-ttu-id="244bc-387">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-387">Windows XP</span></span>                            |



 

### <a name="runas"></a><span data-ttu-id="244bc-388">RunAs</span><span class="sxs-lookup"><span data-stu-id="244bc-388">RunAs</span></span>



| <span data-ttu-id="244bc-389">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-389">Entry</span></span> | <span data-ttu-id="244bc-390">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-391">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-391">Description</span></span>    | <span data-ttu-id="244bc-392">Specifica l'utente con la cui identità viene eseguito il componente.</span><span class="sxs-lookup"><span data-stu-id="244bc-392">Specifies the user under whose identity the component will run.</span></span> <span data-ttu-id="244bc-393">È necessario impostare la password contemporaneamente all'identità RunAs, prima di usare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), perché la password e l'identità vengono convalidate prima di essere salvate.</span><span class="sxs-lookup"><span data-stu-id="244bc-393">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="244bc-394">Se la password e l'identità non vengono sincronizzate, il componente non può essere avviato finché non viene reimpostato da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="244bc-394">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="244bc-395">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-395">Access</span></span>         | <span data-ttu-id="244bc-396">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-396">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="244bc-397">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-397">Type</span></span>           | <span data-ttu-id="244bc-398">string</span><span class="sxs-lookup"><span data-stu-id="244bc-398">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="244bc-399">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-399">Default</span></span>        | <span data-ttu-id="244bc-400">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-400">N/A</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="244bc-401">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-401">Minimum system</span></span> | <span data-ttu-id="244bc-402">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-402">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a><span data-ttu-id="244bc-403">ServiceParameter</span><span class="sxs-lookup"><span data-stu-id="244bc-403">ServiceParameter</span></span>



| <span data-ttu-id="244bc-404">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-404">Entry</span></span> | <span data-ttu-id="244bc-405">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-405">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-406">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-406">Description</span></span>    | <span data-ttu-id="244bc-407">Specifica i parametri passati all'applicazione quando vengono richiamati come applicazione di servizio.</span><span class="sxs-lookup"><span data-stu-id="244bc-407">Specifies the parameters passed to the application when invoked as a service application.</span></span> |
| <span data-ttu-id="244bc-408">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-408">Access</span></span>         | <span data-ttu-id="244bc-409">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-409">ReadWrite</span></span>                                                                                 |
| <span data-ttu-id="244bc-410">Type</span><span class="sxs-lookup"><span data-stu-id="244bc-410">Type</span></span>           | <span data-ttu-id="244bc-411">string</span><span class="sxs-lookup"><span data-stu-id="244bc-411">String</span></span>                                                                                    |
| <span data-ttu-id="244bc-412">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-412">Default</span></span>        | <span data-ttu-id="244bc-413">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-413">N/A</span></span>                                                                                       |
| <span data-ttu-id="244bc-414">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-414">Minimum system</span></span> | <span data-ttu-id="244bc-415">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-415">Windows XP</span></span>                                                                                |



 

### <a name="srptrustlevel"></a><span data-ttu-id="244bc-416">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="244bc-416">SRPTrustLevel</span></span>



| <span data-ttu-id="244bc-417">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-417">Entry</span></span> | <span data-ttu-id="244bc-418">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-418">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-419">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-419">Description</span></span>    | <span data-ttu-id="244bc-420">Indica il livello di attendibilità del componente per i criteri di restrizione software.</span><span class="sxs-lookup"><span data-stu-id="244bc-420">Indicates the software restriction policy (SRP) trust level of the component.</span></span> <span data-ttu-id="244bc-421">Il livello di attendibilità SRP si riferisce al livello di attendibilità che si è disposti a assegnare a un componente.</span><span class="sxs-lookup"><span data-stu-id="244bc-421">The SRP trust level refers to the level of trust that you are willing to give to a component.</span></span> <span data-ttu-id="244bc-422">Un livello di attendibilità Unrestricted SRP corrisponde \_ al \_ valore di enumerazione LEVELID FULLYTRUSTED più sicuro, mentre un livello di ATTENDIBILità SRP non consentito corrisponde al \_ valore di enumerazione non consentito LEVELID più sicuro \_ .</span><span class="sxs-lookup"><span data-stu-id="244bc-422">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="244bc-423">L'enumerazione per i livelli di attendibilità è definita in Winsafer. h.</span><span class="sxs-lookup"><span data-stu-id="244bc-423">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="244bc-424">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-424">Access</span></span>         | <span data-ttu-id="244bc-425">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="244bc-425">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="244bc-426">Tipo</span><span class="sxs-lookup"><span data-stu-id="244bc-426">Type</span></span>           | <span data-ttu-id="244bc-427">Valori lunghi possibili: SAFER \_ LEVELID non \_ consentita (0x0) Safer \_ LEVELID \_ FULLYTRUSTED (0x40000)</span><span class="sxs-lookup"><span data-stu-id="244bc-427">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="244bc-428">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-428">Default</span></span>        | <span data-ttu-id="244bc-429">\_FULLYTRUSTED LEVELID più sicuro \_</span><span class="sxs-lookup"><span data-stu-id="244bc-429">SAFER\_LEVELID\_FULLYTRUSTED</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="244bc-430">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-430">Minimum system</span></span> | <span data-ttu-id="244bc-431">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-431">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="244bc-432">Un componente di cui si è disposti a considerare attendibile l'accesso senza restrizioni deve disporre della sicurezza più rigorosa collegata.</span><span class="sxs-lookup"><span data-stu-id="244bc-432">A component that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="244bc-433">Le applicazioni senza restrizioni possono caricare solo componenti senza restrizioni, mentre le applicazioni non consentite non potranno essere eseguite e pertanto non potranno caricare alcun componente.</span><span class="sxs-lookup"><span data-stu-id="244bc-433">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

### <a name="threadingmodel"></a><span data-ttu-id="244bc-434">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="244bc-434">ThreadingModel</span></span>



| <span data-ttu-id="244bc-435">Voce</span><span class="sxs-lookup"><span data-stu-id="244bc-435">Entry</span></span> | <span data-ttu-id="244bc-436">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-436">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-437">Descrizione</span><span class="sxs-lookup"><span data-stu-id="244bc-437">Description</span></span>    | <span data-ttu-id="244bc-438">Determina il modo in cui le istanze del componente vengono assegnate ai thread per l'esecuzione del metodo.</span><span class="sxs-lookup"><span data-stu-id="244bc-438">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="244bc-439">I valori corrispondono ai modelli di threading COM.</span><span class="sxs-lookup"><span data-stu-id="244bc-439">Values correspond to COM threading models.</span></span>                                                  |
| <span data-ttu-id="244bc-440">Access</span><span class="sxs-lookup"><span data-stu-id="244bc-440">Access</span></span>         | <span data-ttu-id="244bc-441">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="244bc-441">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="244bc-442">Tipo</span><span class="sxs-lookup"><span data-stu-id="244bc-442">Type</span></span>           | <span data-ttu-id="244bc-443">Valori lunghi possibili: COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4)</span><span class="sxs-lookup"><span data-stu-id="244bc-443">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)</span></span> |
| <span data-ttu-id="244bc-444">Predefinito</span><span class="sxs-lookup"><span data-stu-id="244bc-444">Default</span></span>        | <span data-ttu-id="244bc-445">N/D</span><span class="sxs-lookup"><span data-stu-id="244bc-445">N/A</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="244bc-446">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="244bc-446">Minimum system</span></span> | <span data-ttu-id="244bc-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="244bc-447">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="244bc-448">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="244bc-448">See also</span></span>

<dl> <dt>

[<span data-ttu-id="244bc-449">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="244bc-449">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
