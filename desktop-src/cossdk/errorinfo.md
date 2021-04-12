---
description: Recupera informazioni dettagliate sugli errori relativi ai metodi che gestiscono più oggetti, ad esempio popolamento e SaveChanges sull'oggetto COMAdminCatalogCollection, e metodi per installare, importare o esportare applicazioni o componenti nell'oggetto COMAdminCatalog.
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: Raccolta ErrorInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: ebcb4b89eee51b475869cfc62676feda10e53084
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483605"
---
# <a name="errorinfo-collection"></a><span data-ttu-id="ac321-103">Raccolta ErrorInfo</span><span class="sxs-lookup"><span data-stu-id="ac321-103">ErrorInfo collection</span></span>

<span data-ttu-id="ac321-104">Recupera informazioni dettagliate sugli errori relativi ai metodi che gestiscono più oggetti, ad esempio [**popolamento**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sull'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , e metodi per installare, importare o esportare applicazioni o componenti nell'oggetto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="ac321-104">Retrieves extended error information regarding methods that deal with multiple objects, such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, and methods to install, import, or export applications or components on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

<span data-ttu-id="ac321-105">Usare il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) su un [**COMAdminCatalogCollection**](comadmincatalogcollection.md) per accedere alla raccolta **errorInfo** associata alla raccolta originale che contiene un errore.</span><span class="sxs-lookup"><span data-stu-id="ac321-105">Use the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) to access the **ErrorInfo** collection associated with the original collection that has an error.</span></span>

<span data-ttu-id="ac321-106">È necessario chiamare [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) in **errorInfo** immediatamente dopo che si è verificato un errore. in caso contrario, le informazioni sull'errore andranno perse.</span><span class="sxs-lookup"><span data-stu-id="ac321-106">You must call [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on **ErrorInfo** immediately after an error occurs; otherwise, the error information is lost.</span></span>

<span data-ttu-id="ac321-107">Questa raccolta non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="ac321-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ac321-108">Membri</span><span class="sxs-lookup"><span data-stu-id="ac321-108">Members</span></span>

<span data-ttu-id="ac321-109">La raccolta **errorInfo** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="ac321-109">The **ErrorInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ac321-110">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="ac321-110">Related Collections</span></span>

<span data-ttu-id="ac321-111">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="ac321-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ac321-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ac321-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ac321-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="ac321-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="ac321-114">È possibile passare a questa raccolta da ogni raccolta, ad eccezione di **errorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**root**](root.md)e [**WOWInprocServers**](wowinprocservers.md).</span><span class="sxs-lookup"><span data-stu-id="ac321-114">You can navigate to this collection from every collection except for **ErrorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**Root**](root.md), and [**WOWInprocServers**](wowinprocservers.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ac321-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ac321-115">Properties</span></span>

<span data-ttu-id="ac321-116">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="ac321-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ac321-117">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="ac321-117">ErrorCode</span></span>](#errorcode)
-   [<span data-ttu-id="ac321-118">MajorRef</span><span class="sxs-lookup"><span data-stu-id="ac321-118">MajorRef</span></span>](#majorref)
-   [<span data-ttu-id="ac321-119">MinorRef</span><span class="sxs-lookup"><span data-stu-id="ac321-119">MinorRef</span></span>](#minorref)
-   [<span data-ttu-id="ac321-120">Nome</span><span class="sxs-lookup"><span data-stu-id="ac321-120">Name</span></span>](#name)

### <a name="errorcode"></a><span data-ttu-id="ac321-121">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="ac321-121">ErrorCode</span></span>



| <span data-ttu-id="ac321-122">Voce</span><span class="sxs-lookup"><span data-stu-id="ac321-122">Entry</span></span> | <span data-ttu-id="ac321-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ac321-123">Value</span></span> |
|----------------|----------------------------------------|
| <span data-ttu-id="ac321-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac321-124">Description</span></span>    | <span data-ttu-id="ac321-125">Codice di errore relativo all'oggetto o al file.</span><span class="sxs-lookup"><span data-stu-id="ac321-125">The error code for the object or file.</span></span> |
| <span data-ttu-id="ac321-126">Access</span><span class="sxs-lookup"><span data-stu-id="ac321-126">Access</span></span>         | <span data-ttu-id="ac321-127">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac321-127">ReadOnly</span></span>                               |
| <span data-ttu-id="ac321-128">Type</span><span class="sxs-lookup"><span data-stu-id="ac321-128">Type</span></span>           | <span data-ttu-id="ac321-129">string</span><span class="sxs-lookup"><span data-stu-id="ac321-129">String</span></span>                                 |
| <span data-ttu-id="ac321-130">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ac321-130">Default</span></span>        | <span data-ttu-id="ac321-131">nessuno</span><span class="sxs-lookup"><span data-stu-id="ac321-131">None</span></span>                                   |
| <span data-ttu-id="ac321-132">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ac321-132">Minimum system</span></span> | <span data-ttu-id="ac321-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ac321-133">Windows 2000</span></span>                           |



 

### <a name="majorref"></a><span data-ttu-id="ac321-134">MajorRef</span><span class="sxs-lookup"><span data-stu-id="ac321-134">MajorRef</span></span>



| <span data-ttu-id="ac321-135">Voce</span><span class="sxs-lookup"><span data-stu-id="ac321-135">Entry</span></span> | <span data-ttu-id="ac321-136">Valore</span><span class="sxs-lookup"><span data-stu-id="ac321-136">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac321-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac321-137">Description</span></span>    | <span data-ttu-id="ac321-138">Valore della proprietà [**chiave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) per l'oggetto che contiene un errore.</span><span class="sxs-lookup"><span data-stu-id="ac321-138">The [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property value for the object that has an error.</span></span> <span data-ttu-id="ac321-139">Se, ad esempio, una chiamata a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) per una raccolta ha esito negativo su un particolare oggetto della raccolta, il valore della proprietà **chiave** per l'oggetto viene segnalato come valore MajorRef.</span><span class="sxs-lookup"><span data-stu-id="ac321-139">For example, if a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) call for a collection fails on a particular object in the collection, the **Key** property value for that object is reported as the MajorRef value.</span></span> <span data-ttu-id="ac321-140">Utilizzare questa proprietà per esaminare l'elemento che non è possibile aggiornare o per trovare il componente o la DLL che non viene installata.</span><span class="sxs-lookup"><span data-stu-id="ac321-140">Use this property to look at the item that fails to update or to find the component or DLL that fails to install.</span></span> |
| <span data-ttu-id="ac321-141">Access</span><span class="sxs-lookup"><span data-stu-id="ac321-141">Access</span></span>         | <span data-ttu-id="ac321-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac321-142">ReadOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ac321-143">Type</span><span class="sxs-lookup"><span data-stu-id="ac321-143">Type</span></span>           | <span data-ttu-id="ac321-144">string</span><span class="sxs-lookup"><span data-stu-id="ac321-144">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ac321-145">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ac321-145">Default</span></span>        | <span data-ttu-id="ac321-146">nessuno</span><span class="sxs-lookup"><span data-stu-id="ac321-146">None</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ac321-147">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ac321-147">Minimum system</span></span> | <span data-ttu-id="ac321-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ac321-148">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a><span data-ttu-id="ac321-149">MinorRef</span><span class="sxs-lookup"><span data-stu-id="ac321-149">MinorRef</span></span>



| <span data-ttu-id="ac321-150">Voce</span><span class="sxs-lookup"><span data-stu-id="ac321-150">Entry</span></span> | <span data-ttu-id="ac321-151">Valore</span><span class="sxs-lookup"><span data-stu-id="ac321-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac321-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac321-152">Description</span></span>    | <span data-ttu-id="ac321-153">Specifica precisa dell'elemento che presenta un errore, ad esempio un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="ac321-153">A precise specification of the item that has an error, such as a property name.</span></span> <span data-ttu-id="ac321-154">Se si verificano più errori o in contesti in cui questo non è applicabile, MinorRef è <Invalid> .</span><span class="sxs-lookup"><span data-stu-id="ac321-154">If multiple errors occur or in contexts in which this doesn't apply, MinorRef is <Invalid>.</span></span> |
| <span data-ttu-id="ac321-155">Access</span><span class="sxs-lookup"><span data-stu-id="ac321-155">Access</span></span>         | <span data-ttu-id="ac321-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac321-156">ReadOnly</span></span>                                                                                                                                                                          |
| <span data-ttu-id="ac321-157">Type</span><span class="sxs-lookup"><span data-stu-id="ac321-157">Type</span></span>           | <span data-ttu-id="ac321-158">string</span><span class="sxs-lookup"><span data-stu-id="ac321-158">String</span></span>                                                                                                                                                                            |
| <span data-ttu-id="ac321-159">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ac321-159">Default</span></span>        | <span data-ttu-id="ac321-160">nessuno</span><span class="sxs-lookup"><span data-stu-id="ac321-160">None</span></span>                                                                                                                                                                              |
| <span data-ttu-id="ac321-161">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ac321-161">Minimum system</span></span> | <span data-ttu-id="ac321-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ac321-162">Windows 2000</span></span>                                                                                                                                                                      |



 

### <a name="name"></a><span data-ttu-id="ac321-163">Nome</span><span class="sxs-lookup"><span data-stu-id="ac321-163">Name</span></span>



| <span data-ttu-id="ac321-164">Voce</span><span class="sxs-lookup"><span data-stu-id="ac321-164">Entry</span></span> | <span data-ttu-id="ac321-165">Valore</span><span class="sxs-lookup"><span data-stu-id="ac321-165">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac321-166">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac321-166">Description</span></span>    | <span data-ttu-id="ac321-167">Nome dell'oggetto o del file in cui si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="ac321-167">The name of the object or file that has an error.</span></span> <span data-ttu-id="ac321-168">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="ac321-168">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ac321-169">Access</span><span class="sxs-lookup"><span data-stu-id="ac321-169">Access</span></span>         | <span data-ttu-id="ac321-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ac321-170">ReadOnly</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="ac321-171">Type</span><span class="sxs-lookup"><span data-stu-id="ac321-171">Type</span></span>           | <span data-ttu-id="ac321-172">string</span><span class="sxs-lookup"><span data-stu-id="ac321-172">String</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="ac321-173">Predefinito</span><span class="sxs-lookup"><span data-stu-id="ac321-173">Default</span></span>        | <span data-ttu-id="ac321-174">nessuno</span><span class="sxs-lookup"><span data-stu-id="ac321-174">None</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="ac321-175">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="ac321-175">Minimum system</span></span> | <span data-ttu-id="ac321-176">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ac321-176">Windows 2000</span></span>                                                                                                                                                                                                             |



 

## <a name="see-also"></a><span data-ttu-id="ac321-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac321-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac321-178">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="ac321-178">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
