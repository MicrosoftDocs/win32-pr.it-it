---
description: Recupera le informazioni per le applicazioni importate.
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: Raccolta FilesForImport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8e7ba3b0bd44cf2f6bb40ecf89f86dd68c21cf3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127143"
---
# <a name="filesforimport-collection"></a><span data-ttu-id="18e91-103">Raccolta FilesForImport</span><span class="sxs-lookup"><span data-stu-id="18e91-103">FilesForImport collection</span></span>

<span data-ttu-id="18e91-104">Recupera le informazioni per le applicazioni importate.</span><span class="sxs-lookup"><span data-stu-id="18e91-104">Retrieves information for applications that are imported.</span></span>

<span data-ttu-id="18e91-105">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="18e91-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="18e91-106">Membri</span><span class="sxs-lookup"><span data-stu-id="18e91-106">Members</span></span>

<span data-ttu-id="18e91-107">La raccolta **FilesForImport** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="18e91-107">The **FilesForImport** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="18e91-108">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="18e91-108">Related Collections</span></span>

<span data-ttu-id="18e91-109">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="18e91-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="18e91-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="18e91-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="18e91-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="18e91-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="18e91-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="18e91-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="18e91-113">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="18e91-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="18e91-114">**Radice**</span><span class="sxs-lookup"><span data-stu-id="18e91-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="18e91-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="18e91-115">Properties</span></span>

<span data-ttu-id="18e91-116">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="18e91-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="18e91-117">ApplicationFileName</span><span class="sxs-lookup"><span data-stu-id="18e91-117">ApplicationFileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="18e91-118">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="18e91-118">ApplicationName</span></span>](#applicationname)
-   [<span data-ttu-id="18e91-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e91-119">Description</span></span>](#partitiondescription)
-   [<span data-ttu-id="18e91-120">FileName</span><span class="sxs-lookup"><span data-stu-id="18e91-120">FileName</span></span>](#applicationfilename)
-   [<span data-ttu-id="18e91-121">HasUsers</span><span class="sxs-lookup"><span data-stu-id="18e91-121">HasUsers</span></span>](#hasusers)
-   [<span data-ttu-id="18e91-122">IsProxy</span><span class="sxs-lookup"><span data-stu-id="18e91-122">IsProxy</span></span>](#isproxy)
-   [<span data-ttu-id="18e91-123">IsService</span><span class="sxs-lookup"><span data-stu-id="18e91-123">IsService</span></span>](#isservice)
-   [<span data-ttu-id="18e91-124">PartitionDescription</span><span class="sxs-lookup"><span data-stu-id="18e91-124">PartitionDescription</span></span>](#partitiondescription)
-   [<span data-ttu-id="18e91-125">PartitionID</span><span class="sxs-lookup"><span data-stu-id="18e91-125">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="18e91-126">PartitionName</span><span class="sxs-lookup"><span data-stu-id="18e91-126">PartitionName</span></span>](#partitionname)

### <a name="applicationfilename"></a><span data-ttu-id="18e91-127">ApplicationFileName</span><span class="sxs-lookup"><span data-stu-id="18e91-127">ApplicationFileName</span></span>



| <span data-ttu-id="18e91-128">Voce</span><span class="sxs-lookup"><span data-stu-id="18e91-128">Entry</span></span> | <span data-ttu-id="18e91-129">Valore</span><span class="sxs-lookup"><span data-stu-id="18e91-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="18e91-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e91-130">Description</span></span>    | <span data-ttu-id="18e91-131">Nome del file MSI che contiene l'applicazione che può essere importata.</span><span class="sxs-lookup"><span data-stu-id="18e91-131">The name of the MSI file that contains the application that can be imported.</span></span> |
| <span data-ttu-id="18e91-132">Access</span><span class="sxs-lookup"><span data-stu-id="18e91-132">Access</span></span>         | <span data-ttu-id="18e91-133">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="18e91-133">ReadOnly</span></span>                                                                     |
| <span data-ttu-id="18e91-134">Type</span><span class="sxs-lookup"><span data-stu-id="18e91-134">Type</span></span>           | <span data-ttu-id="18e91-135">string</span><span class="sxs-lookup"><span data-stu-id="18e91-135">String</span></span>                                                                       |
| <span data-ttu-id="18e91-136">Predefinito</span><span class="sxs-lookup"><span data-stu-id="18e91-136">Default</span></span>        | <span data-ttu-id="18e91-137">N/D</span><span class="sxs-lookup"><span data-stu-id="18e91-137">N/A</span></span>                                                                          |
| <span data-ttu-id="18e91-138">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="18e91-138">Minimum system</span></span> | <span data-ttu-id="18e91-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18e91-139">Windows XP</span></span>                                                                   |



 

### <a name="applicationname"></a><span data-ttu-id="18e91-140">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="18e91-140">ApplicationName</span></span>



| <span data-ttu-id="18e91-141">Voce</span><span class="sxs-lookup"><span data-stu-id="18e91-141">Entry</span></span> | <span data-ttu-id="18e91-142">Valore</span><span class="sxs-lookup"><span data-stu-id="18e91-142">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="18e91-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e91-143">Description</span></span>    | <span data-ttu-id="18e91-144">Nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18e91-144">The name of the application.</span></span> |
| <span data-ttu-id="18e91-145">Access</span><span class="sxs-lookup"><span data-stu-id="18e91-145">Access</span></span>         | <span data-ttu-id="18e91-146">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="18e91-146">ReadOnly</span></span>                     |
| <span data-ttu-id="18e91-147">Type</span><span class="sxs-lookup"><span data-stu-id="18e91-147">Type</span></span>           | <span data-ttu-id="18e91-148">string</span><span class="sxs-lookup"><span data-stu-id="18e91-148">String</span></span>                       |
| <span data-ttu-id="18e91-149">Predefinito</span><span class="sxs-lookup"><span data-stu-id="18e91-149">Default</span></span>        | <span data-ttu-id="18e91-150">""</span><span class="sxs-lookup"><span data-stu-id="18e91-150">""</span></span>                           |
| <span data-ttu-id="18e91-151">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="18e91-151">Minimum system</span></span> | <span data-ttu-id="18e91-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18e91-152">Windows XP</span></span>                   |



 

### <a name="description"></a><span data-ttu-id="18e91-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e91-153">Description</span></span>



| <span data-ttu-id="18e91-154">Voce</span><span class="sxs-lookup"><span data-stu-id="18e91-154">Entry</span></span> | <span data-ttu-id="18e91-155">Valore</span><span class="sxs-lookup"><span data-stu-id="18e91-155">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="18e91-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e91-156">Description</span></span>    | <span data-ttu-id="18e91-157">Descrizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18e91-157">A description of the application.</span></span> |
| <span data-ttu-id="18e91-158">Access</span><span class="sxs-lookup"><span data-stu-id="18e91-158">Access</span></span>         | <span data-ttu-id="18e91-159">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="18e91-159">ReadOnly</span></span>                          |
| <span data-ttu-id="18e91-160">Type</span><span class="sxs-lookup"><span data-stu-id="18e91-160">Type</span></span>           | <span data-ttu-id="18e91-161">string</span><span class="sxs-lookup"><span data-stu-id="18e91-161">String</span></span>                            |
| <span data-ttu-id="18e91-162">Predefinito</span><span class="sxs-lookup"><span data-stu-id="18e91-162">Default</span></span>        | <span data-ttu-id="18e91-163">""</span><span class="sxs-lookup"><span data-stu-id="18e91-163">""</span></span>                                |
| <span data-ttu-id="18e91-164">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="18e91-164">Minimum system</span></span> | <span data-ttu-id="18e91-165">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18e91-165">Windows XP</span></span>                        |



 

### <a name="filename"></a><span data-ttu-id="18e91-166">FileName</span><span class="sxs-lookup"><span data-stu-id="18e91-166">FileName</span></span>



| <span data-ttu-id="18e91-167">Voce</span><span class="sxs-lookup"><span data-stu-id="18e91-167">Entry</span></span> | <span data-ttu-id="18e91-168">Valore</span><span class="sxs-lookup"><span data-stu-id="18e91-168">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18e91-169">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e91-169">Description</span></span>    | <span data-ttu-id="18e91-170">Nome della DLL o del file EXE che contiene l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18e91-170">The name of the DLL or EXE file that contains the application.</span></span> <span data-ttu-id="18e91-171">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="18e91-171">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="18e91-172">Access</span><span class="sxs-lookup"><span data-stu-id="18e91-172">Access</span></span>         | <span data-ttu-id="18e91-173">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="18e91-173">ReadOnly</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="18e91-174">Type</span><span class="sxs-lookup"><span data-stu-id="18e91-174">Type</span></span>           | <span data-ttu-id="18e91-175">string</span><span class="sxs-lookup"><span data-stu-id="18e91-175">String</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="18e91-176">Predefinito</span><span class="sxs-lookup"><span data-stu-id="18e91-176">Default</span></span>        | <span data-ttu-id="18e91-177">""</span><span class="sxs-lookup"><span data-stu-id="18e91-177">""</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="18e91-178">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="18e91-178">Minimum system</span></span> | <span data-ttu-id="18e91-179">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18e91-179">Windows XP</span></span>                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a><span data-ttu-id="18e91-180">HasUsers</span><span class="sxs-lookup"><span data-stu-id="18e91-180">HasUsers</span></span>



| <span data-ttu-id="18e91-181">Voce</span><span class="sxs-lookup"><span data-stu-id="18e91-181">Entry</span></span> | <span data-ttu-id="18e91-182">Valore</span><span class="sxs-lookup"><span data-stu-id="18e91-182">Value</span></span> |
|----------------|--------------------------------------------------|
| <span data-ttu-id="18e91-183">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e91-183">Description</span></span>    | <span data-ttu-id="18e91-184">Indica se l'applicazione dispone di utenti.</span><span class="sxs-lookup"><span data-stu-id="18e91-184">Indicates whether the application has any users.</span></span> |
| <span data-ttu-id="18e91-185">Access</span><span class="sxs-lookup"><span data-stu-id="18e91-185">Access</span></span>         | <span data-ttu-id="18e91-186">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="18e91-186">ReadOnly</span></span>                                         |
| <span data-ttu-id="18e91-187">Tipo</span><span class="sxs-lookup"><span data-stu-id="18e91-187">Type</span></span>           | <span data-ttu-id="18e91-188">Bool</span><span class="sxs-lookup"><span data-stu-id="18e91-188">Bool</span></span>                                             |
| <span data-ttu-id="18e91-189">Predefinito</span><span class="sxs-lookup"><span data-stu-id="18e91-189">Default</span></span>        | <span data-ttu-id="18e91-190">Falso</span><span class="sxs-lookup"><span data-stu-id="18e91-190">False</span></span>                                            |
| <span data-ttu-id="18e91-191">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="18e91-191">Minimum system</span></span> | <span data-ttu-id="18e91-192">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18e91-192">Windows XP</span></span>                                       |



 

### <a name="isproxy"></a><span data-ttu-id="18e91-193">IsProxy</span><span class="sxs-lookup"><span data-stu-id="18e91-193">IsProxy</span></span>



| <span data-ttu-id="18e91-194">Voce</span><span class="sxs-lookup"><span data-stu-id="18e91-194">Entry</span></span> | <span data-ttu-id="18e91-195">Valore</span><span class="sxs-lookup"><span data-stu-id="18e91-195">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="18e91-196">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e91-196">Description</span></span>    | <span data-ttu-id="18e91-197">Indica se l'applicazione è un proxy.</span><span class="sxs-lookup"><span data-stu-id="18e91-197">Indicates whether the application is a proxy.</span></span> |
| <span data-ttu-id="18e91-198">Access</span><span class="sxs-lookup"><span data-stu-id="18e91-198">Access</span></span>         | <span data-ttu-id="18e91-199">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="18e91-199">ReadOnly</span></span>                                      |
| <span data-ttu-id="18e91-200">Tipo</span><span class="sxs-lookup"><span data-stu-id="18e91-200">Type</span></span>           | <span data-ttu-id="18e91-201">Bool</span><span class="sxs-lookup"><span data-stu-id="18e91-201">Bool</span></span>                                          |
| <span data-ttu-id="18e91-202">Predefinito</span><span class="sxs-lookup"><span data-stu-id="18e91-202">Default</span></span>        | <span data-ttu-id="18e91-203">Falso</span><span class="sxs-lookup"><span data-stu-id="18e91-203">False</span></span>                                         |
| <span data-ttu-id="18e91-204">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="18e91-204">Minimum system</span></span> | <span data-ttu-id="18e91-205">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18e91-205">Windows XP</span></span>                                    |



 

### <a name="isservice"></a><span data-ttu-id="18e91-206">IsService</span><span class="sxs-lookup"><span data-stu-id="18e91-206">IsService</span></span>



| <span data-ttu-id="18e91-207">Voce</span><span class="sxs-lookup"><span data-stu-id="18e91-207">Entry</span></span> | <span data-ttu-id="18e91-208">Valore</span><span class="sxs-lookup"><span data-stu-id="18e91-208">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="18e91-209">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e91-209">Description</span></span>    | <span data-ttu-id="18e91-210">Indica se l'applicazione è un servizio.</span><span class="sxs-lookup"><span data-stu-id="18e91-210">Indicates whether the application is a service.</span></span> |
| <span data-ttu-id="18e91-211">Access</span><span class="sxs-lookup"><span data-stu-id="18e91-211">Access</span></span>         | <span data-ttu-id="18e91-212">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="18e91-212">ReadOnly</span></span>                                        |
| <span data-ttu-id="18e91-213">Tipo</span><span class="sxs-lookup"><span data-stu-id="18e91-213">Type</span></span>           | <span data-ttu-id="18e91-214">Bool</span><span class="sxs-lookup"><span data-stu-id="18e91-214">Bool</span></span>                                            |
| <span data-ttu-id="18e91-215">Predefinito</span><span class="sxs-lookup"><span data-stu-id="18e91-215">Default</span></span>        | <span data-ttu-id="18e91-216">Falso</span><span class="sxs-lookup"><span data-stu-id="18e91-216">False</span></span>                                           |
| <span data-ttu-id="18e91-217">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="18e91-217">Minimum system</span></span> | <span data-ttu-id="18e91-218">Windows XP</span><span class="sxs-lookup"><span data-stu-id="18e91-218">Windows XP</span></span>                                      |



 

### <a name="partitiondescription"></a><span data-ttu-id="18e91-219">PartitionDescription</span><span class="sxs-lookup"><span data-stu-id="18e91-219">PartitionDescription</span></span>



| <span data-ttu-id="18e91-220">Voce</span><span class="sxs-lookup"><span data-stu-id="18e91-220">Entry</span></span> | <span data-ttu-id="18e91-221">Valore</span><span class="sxs-lookup"><span data-stu-id="18e91-221">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="18e91-222">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e91-222">Description</span></span>    | <span data-ttu-id="18e91-223">Descrizione della partizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18e91-223">A description of the application's partition.</span></span> |
| <span data-ttu-id="18e91-224">Access</span><span class="sxs-lookup"><span data-stu-id="18e91-224">Access</span></span>         | <span data-ttu-id="18e91-225">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="18e91-225">ReadOnly</span></span>                                      |
| <span data-ttu-id="18e91-226">Type</span><span class="sxs-lookup"><span data-stu-id="18e91-226">Type</span></span>           | <span data-ttu-id="18e91-227">string</span><span class="sxs-lookup"><span data-stu-id="18e91-227">String</span></span>                                        |
| <span data-ttu-id="18e91-228">Predefinito</span><span class="sxs-lookup"><span data-stu-id="18e91-228">Default</span></span>        | <span data-ttu-id="18e91-229">""</span><span class="sxs-lookup"><span data-stu-id="18e91-229">""</span></span>                                            |
| <span data-ttu-id="18e91-230">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="18e91-230">Minimum system</span></span> | <span data-ttu-id="18e91-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18e91-231">Windows Server 2003</span></span>                           |



 

### <a name="partitionid"></a><span data-ttu-id="18e91-232">PartitionID</span><span class="sxs-lookup"><span data-stu-id="18e91-232">PartitionID</span></span>



| <span data-ttu-id="18e91-233">Voce</span><span class="sxs-lookup"><span data-stu-id="18e91-233">Entry</span></span> | <span data-ttu-id="18e91-234">Valore</span><span class="sxs-lookup"><span data-stu-id="18e91-234">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="18e91-235">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e91-235">Description</span></span>    | <span data-ttu-id="18e91-236">GUID della partizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18e91-236">The GUID of the application's partition.</span></span> |
| <span data-ttu-id="18e91-237">Access</span><span class="sxs-lookup"><span data-stu-id="18e91-237">Access</span></span>         | <span data-ttu-id="18e91-238">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="18e91-238">ReadOnly</span></span>                                 |
| <span data-ttu-id="18e91-239">Type</span><span class="sxs-lookup"><span data-stu-id="18e91-239">Type</span></span>           | <span data-ttu-id="18e91-240">string</span><span class="sxs-lookup"><span data-stu-id="18e91-240">String</span></span>                                   |
| <span data-ttu-id="18e91-241">Predefinito</span><span class="sxs-lookup"><span data-stu-id="18e91-241">Default</span></span>        | <span data-ttu-id="18e91-242">""</span><span class="sxs-lookup"><span data-stu-id="18e91-242">""</span></span>                                       |
| <span data-ttu-id="18e91-243">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="18e91-243">Minimum system</span></span> | <span data-ttu-id="18e91-244">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18e91-244">Windows Server 2003</span></span>                      |



 

### <a name="partitionname"></a><span data-ttu-id="18e91-245">PartitionName</span><span class="sxs-lookup"><span data-stu-id="18e91-245">PartitionName</span></span>



| <span data-ttu-id="18e91-246">Voce</span><span class="sxs-lookup"><span data-stu-id="18e91-246">Entry</span></span> | <span data-ttu-id="18e91-247">Valore</span><span class="sxs-lookup"><span data-stu-id="18e91-247">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="18e91-248">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18e91-248">Description</span></span>    | <span data-ttu-id="18e91-249">Nome della partizione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18e91-249">The name of the application's partition.</span></span> |
| <span data-ttu-id="18e91-250">Access</span><span class="sxs-lookup"><span data-stu-id="18e91-250">Access</span></span>         | <span data-ttu-id="18e91-251">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="18e91-251">ReadOnly</span></span>                                 |
| <span data-ttu-id="18e91-252">Type</span><span class="sxs-lookup"><span data-stu-id="18e91-252">Type</span></span>           | <span data-ttu-id="18e91-253">string</span><span class="sxs-lookup"><span data-stu-id="18e91-253">String</span></span>                                   |
| <span data-ttu-id="18e91-254">Predefinito</span><span class="sxs-lookup"><span data-stu-id="18e91-254">Default</span></span>        | <span data-ttu-id="18e91-255">""</span><span class="sxs-lookup"><span data-stu-id="18e91-255">""</span></span>                                       |
| <span data-ttu-id="18e91-256">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="18e91-256">Minimum system</span></span> | <span data-ttu-id="18e91-257">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18e91-257">Windows Server 2003</span></span>                      |



 

## <a name="see-also"></a><span data-ttu-id="18e91-258">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18e91-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e91-259">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="18e91-259">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
