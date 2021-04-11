---
description: Rappresenta gli elementi nelle raccolte nel catalogo COM+. Usarlo per recuperare e modificare le proprietà esposte da un elemento in una raccolta.
ms.assetid: 1d7f248b-20ec-4b34-88ab-3c68bef72b5a
title: Classe COMAdminCatalogObject (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogObject
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 19fb873e29ad235b11dfe6e7a95b2ad47a8405b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126717"
---
# <a name="comadmincatalogobject-class"></a><span data-ttu-id="af366-104">Classe COMAdminCatalogObject</span><span class="sxs-lookup"><span data-stu-id="af366-104">COMAdminCatalogObject class</span></span>

<span data-ttu-id="af366-105">Rappresenta gli elementi nelle raccolte nel catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="af366-105">Represents items in collections in the COM+ catalog.</span></span> <span data-ttu-id="af366-106">Usarlo per recuperare e modificare le proprietà esposte da un elemento in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="af366-106">Use it to retrieve and modify properties exposed by an item in a collection.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="af366-107">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="af366-107">When to implement</span></span>

<span data-ttu-id="af366-108">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="af366-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="af366-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="af366-109">Requirement</span></span> | <span data-ttu-id="af366-110">Valore</span><span class="sxs-lookup"><span data-stu-id="af366-110">Value</span></span> |
|------------|------------------------------------------|
| <span data-ttu-id="af366-111">Interfacce</span><span class="sxs-lookup"><span data-stu-id="af366-111">Interfaces</span></span> | [<span data-ttu-id="af366-112">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="af366-112">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a><span data-ttu-id="af366-113">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="af366-113">When to use</span></span>

<span data-ttu-id="af366-114">Usare gli oggetti creati dalla classe **COMAdminCatalogObject** per modificare le proprietà degli elementi contenuti nelle raccolte nel catalogo com+.</span><span class="sxs-lookup"><span data-stu-id="af366-114">Use objects created from the **COMAdminCatalogObject** class to modify the properties of items contained in collections in the COM+ catalog.</span></span> <span data-ttu-id="af366-115">Questi elementi corrispondono agli elementi visualizzati all'interno delle cartelle nell'albero della console dello strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="af366-115">These items correspond to items shown inside folders in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="af366-116">Le cartelle dello strumento di amministrazione Servizi componenti corrispondono alle raccolte nel catalogo, che è possibile rappresentare usando gli oggetti creati dalla classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="af366-116">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span>

<span data-ttu-id="af366-117">Non tutte le raccolte e gli elementi esposti tramite [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e **COMAdminCatalogObject** sono disponibili nello strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="af366-117">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and **COMAdminCatalogObject** are available in the Component Services administration tool.</span></span>

<span data-ttu-id="af366-118">Per informazioni sulle raccolte specifiche e sulle relative proprietà, vedere la pagina relativa alle [raccolte di amministrazione com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="af366-118">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="af366-119">Per un'introduzione all'amministrazione a livello di codice di COM+, vedere [automazione dell'amministrazione com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="af366-119">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="af366-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="af366-120">Remarks</span></span>

<span data-ttu-id="af366-121">Non è possibile creare direttamente un oggetto **COMAdminCatalogObject** .</span><span class="sxs-lookup"><span data-stu-id="af366-121">You cannot directly create a **COMAdminCatalogObject** object.</span></span> <span data-ttu-id="af366-122">Per usare i metodi di questo oggetto, è necessario creare un oggetto [**COMAdminCatalog**](comadmincatalog.md) , ottenere un riferimento a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)e quindi usare [**ICOMAdminCatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) per ottenere un riferimento a un'interfaccia [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) che rappresenta una raccolta di livello superiore o usare [**ICatalogCollection:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) per accedere a raccolte che non sono di primo livello.</span><span class="sxs-lookup"><span data-stu-id="af366-122">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection or use [**ICatalogCollection::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) to access collections that are not top-level.</span></span>

<span data-ttu-id="af366-123">Quando si dispone di un riferimento all'interfaccia [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) della raccolta a cui si è interessati, chiamare [**ICatalogCollection::P ripopolamento**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) per popolare la raccolta con tutti i relativi elementi.</span><span class="sxs-lookup"><span data-stu-id="af366-123">After you have a reference to the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface of the collection in which you are interested, call [**ICatalogCollection::Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) to populate the collection with all of its items.</span></span> <span data-ttu-id="af366-124">Scorrere ogni elemento della raccolta chiamando [**ICatalogCollection:: Get \_ Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) per ottenere un riferimento a ogni interfaccia [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .</span><span class="sxs-lookup"><span data-stu-id="af366-124">Iterate through each of the items in the collection by calling [**ICatalogCollection::get\_Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) to get a reference to each [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span> <span data-ttu-id="af366-125">Quando si trova l'elemento di interesse, è possibile modificare le proprietà dell'elemento e uscire dall'iterazione.</span><span class="sxs-lookup"><span data-stu-id="af366-125">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="af366-126">Se si apportano modifiche a tutti gli elementi di una raccolta, è necessario chiamare [**ICatalogCollection:: SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) per salvare le modifiche apportate al catalogo com+.</span><span class="sxs-lookup"><span data-stu-id="af366-126">If you make any changes to any items in a collection, you must call [**ICatalogCollection::SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="af366-127">Questa operazione è illustrata nell'esempio seguente, in cui la "raccolta" deve essere sostituita dal nome di una delle raccolte di amministrazione COM+ di primo livello. "ItemName" deve essere sostituito con il nome dell'elemento a cui si è interessati. "PropertyName" deve essere sostituito dal nome della proprietà che si sta modificando nell'elemento. e varNewProp devono essere sostituiti da una variante che contiene il nuovo valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="af366-127">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and varNewProp must be replaced by a VARIANT that contains the new value for the property.</span></span>


```C++
// Convert ItemName to a BSTR.
bstrItemName = SysAllocString(L"ItemName");
HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
  CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
  (void**)&pCatalog); 
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pCatalog->GetCollection(L"TopCollection", 
  (IDispatch**)&pTopColl);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Populate the TopCollection collection.
hr = pTopColl->Populate();
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Get the number of items in the collection.
hr = pTopColl->get_Count(&lCount);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
VARIANT varName;
VariantInit(&varName);
// Iterate through each item in the collection.
for (LONG lIdx = 0; lIdx < lCount; lIdx++) {
    hr = pTopColl->get_Item(lIdx, (IDispatch**)&pItem);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    hr = pItem->get_Name(&varName);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    // Compare the item name to bstrItemName.
    hr = VarBstrCmp(varName.bstrVal, bstrItemName, 1024L, NULL);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    if (VARCMP_EQ == hr) {  // The strings are equal.
        // Use the put_Value method to modify properties of the item.
        hr = pItem->put_Value(L"PropertyName", varNewProp);
        if (FAILED(hr)) exit(0);  // Replace with specific error handling.
        break;  // Exit the iteration.
    }
}
hr = pTopColl->SaveChanges(&lNum);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
SysFreeString(bstrItemName);


```



<span data-ttu-id="af366-128">Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi amministratore COM+.</span><span class="sxs-lookup"><span data-stu-id="af366-128">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="af366-129">Un oggetto COMAdminCatalogCollection può essere creato chiamando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) su un oggetto [**COMAdminCatalog**](comadmincatalog.md) o [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="af366-129">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) or [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

<span data-ttu-id="af366-130">Chiamare il metodo [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) per popolare la raccolta con tutti i relativi elementi.</span><span class="sxs-lookup"><span data-stu-id="af366-130">Call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object to populate the collection with all of its items.</span></span> <span data-ttu-id="af366-131">Scorre ogni elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="af366-131">Iterate through each of the items in the collection.</span></span> <span data-ttu-id="af366-132">Quando si trova l'elemento di interesse, è possibile modificare le proprietà dell'elemento e uscire dall'iterazione.</span><span class="sxs-lookup"><span data-stu-id="af366-132">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="af366-133">Se si apportano modifiche a elementi di una raccolta, è necessario chiamare il metodo [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) dell'oggetto **COMAdminCatalogCollection** per salvare le modifiche apportate al catalogo com+.</span><span class="sxs-lookup"><span data-stu-id="af366-133">If you make any changes to any items in a collection, you must call the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method of the **COMAdminCatalogCollection** object to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="af366-134">Questa operazione è illustrata nell'esempio seguente, in cui la "raccolta" deve essere sostituita dal nome di una delle raccolte di amministrazione COM+ di primo livello. "ItemName" deve essere sostituito con il nome dell'elemento a cui si è interessati. "PropertyName" deve essere sostituito dal nome della proprietà che si sta modificando nell'elemento. e NewPropValue devono essere sostituiti dal nuovo valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="af366-134">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and NewPropValue must be replaced by the new value for the property.</span></span>


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")
objTopCollection.Populate
Dim objItem As COMAdmin.COMAdminCatalogObject
For Each objItem in objTopCollection
    If objItem.Name = "ItemName" Then
        objItem.Value("PropertyName") = NewPropValue
        Exit For
    End If
Next
objAppCollection.SaveChanges

```



## <a name="requirements"></a><span data-ttu-id="af366-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af366-135">Requirements</span></span>



| <span data-ttu-id="af366-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="af366-136">Requirement</span></span> | <span data-ttu-id="af366-137">Valore</span><span class="sxs-lookup"><span data-stu-id="af366-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af366-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af366-138">Minimum supported client</span></span><br/> | <span data-ttu-id="af366-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="af366-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="af366-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af366-140">Minimum supported server</span></span><br/> | <span data-ttu-id="af366-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="af366-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af366-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af366-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="af366-143"><dt>COMAdmin. h</dt></span><span class="sxs-lookup"><span data-stu-id="af366-143"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="af366-144">IDL</span><span class="sxs-lookup"><span data-stu-id="af366-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="af366-145"><dt>COMAdmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="af366-145"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af366-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af366-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af366-147">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="af366-147">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="af366-148">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="af366-148">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="af366-149">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="af366-149">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




