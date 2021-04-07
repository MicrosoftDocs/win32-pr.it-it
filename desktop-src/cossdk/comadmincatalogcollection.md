---
description: Rappresenta qualsiasi raccolta nel catalogo COM+. Usarlo per enumerare, aggiungere, rimuovere e recuperare elementi in una raccolta e per accedere alle raccolte correlate.
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: Classe COMAdminCatalogCollection (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogCollection
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 985a6b947708542ec3ce1dc6ecc835c94259b315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748663"
---
# <a name="comadmincatalogcollection-class"></a><span data-ttu-id="9c6d2-104">Classe COMAdminCatalogCollection</span><span class="sxs-lookup"><span data-stu-id="9c6d2-104">COMAdminCatalogCollection class</span></span>

<span data-ttu-id="9c6d2-105">Rappresenta qualsiasi raccolta nel catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="9c6d2-105">Represents any collection in the COM+ catalog.</span></span> <span data-ttu-id="9c6d2-106">Usarlo per enumerare, aggiungere, rimuovere e recuperare elementi in una raccolta e per accedere alle raccolte correlate.</span><span class="sxs-lookup"><span data-stu-id="9c6d2-106">Use it to enumerate, add, remove, and retrieve items in a collection and to access related collections.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="9c6d2-107">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="9c6d2-107">When to implement</span></span>

<span data-ttu-id="9c6d2-108">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="9c6d2-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="9c6d2-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c6d2-109">Requirement</span></span> | <span data-ttu-id="9c6d2-110">Valore</span><span class="sxs-lookup"><span data-stu-id="9c6d2-110">Value</span></span> |
|------------|--------------------------------------------------|
| <span data-ttu-id="9c6d2-111">Interfacce</span><span class="sxs-lookup"><span data-stu-id="9c6d2-111">Interfaces</span></span> | [<span data-ttu-id="9c6d2-112">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="9c6d2-112">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a><span data-ttu-id="9c6d2-113">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="9c6d2-113">When to use</span></span>

<span data-ttu-id="9c6d2-114">Usare gli oggetti creati dalla classe **COMAdminCatalogCollection** quando si desidera modificare a livello di codice una raccolta nel catalogo com+.</span><span class="sxs-lookup"><span data-stu-id="9c6d2-114">Use objects created from the **COMAdminCatalogCollection** class when you want to programmatically manipulate a collection in the COM+ catalog.</span></span> <span data-ttu-id="9c6d2-115">Queste raccolte corrispondono alle cartelle dello strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="9c6d2-115">These collections correspond to folders in the Component Services administration tool.</span></span> <span data-ttu-id="9c6d2-116">Gli elementi all'interno delle cartelle corrispondono agli elementi delle raccolte, che è possibile rappresentare usando gli oggetti creati dalla classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="9c6d2-116">Items inside the folders correspond to items in collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="9c6d2-117">Per informazioni sulle raccolte nel catalogo e sulle relative proprietà, vedere la pagina relativa alle [raccolte di amministrazione com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="9c6d2-117">For information regarding the collections on the catalog and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="9c6d2-118">Per un'introduzione all'amministrazione a livello di codice di COM+, vedere [automazione dell'amministrazione com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="9c6d2-118">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9c6d2-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c6d2-119">Remarks</span></span>

<span data-ttu-id="9c6d2-120">Non è possibile creare direttamente un oggetto **COMAdminCatalogCollection** .</span><span class="sxs-lookup"><span data-stu-id="9c6d2-120">You cannot directly create a **COMAdminCatalogCollection** object.</span></span> <span data-ttu-id="9c6d2-121">Per usare i metodi di questo oggetto, è necessario creare un oggetto [**COMAdminCatalog**](comadmincatalog.md) , ottenere un riferimento a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)e quindi usare [**ICOMAdminCatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) per ottenere un riferimento a un'interfaccia [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) che rappresenta una raccolta di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="9c6d2-121">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection.</span></span> <span data-ttu-id="9c6d2-122">Questa operazione è illustrata nell'esempio seguente, in cui la "raccolta" deve essere sostituita dal nome di una delle raccolte di amministrazione COM+ di primo livello.</span><span class="sxs-lookup"><span data-stu-id="9c6d2-122">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```C++
    HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pCatalog->GetCollection(L"TopCollection", 
      (IDispatch**)&pTopColl);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
```



<span data-ttu-id="9c6d2-123">Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi amministratore COM+.</span><span class="sxs-lookup"><span data-stu-id="9c6d2-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="9c6d2-124">Un oggetto COMAdminCatalogCollection può essere creato chiamando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) su un oggetto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="9c6d2-124">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="9c6d2-125">Questa operazione è illustrata nell'esempio seguente, in cui la "raccolta" deve essere sostituita dal nome di una delle raccolte di amministrazione COM+ di primo livello.</span><span class="sxs-lookup"><span data-stu-id="9c6d2-125">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

```



## <a name="requirements"></a><span data-ttu-id="9c6d2-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c6d2-126">Requirements</span></span>



| <span data-ttu-id="9c6d2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c6d2-127">Requirement</span></span> | <span data-ttu-id="9c6d2-128">Valore</span><span class="sxs-lookup"><span data-stu-id="9c6d2-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c6d2-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c6d2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9c6d2-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9c6d2-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9c6d2-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c6d2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9c6d2-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9c6d2-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c6d2-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c6d2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c6d2-134"><dt>COMAdmin. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c6d2-134"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c6d2-135">IDL</span><span class="sxs-lookup"><span data-stu-id="9c6d2-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9c6d2-136"><dt>COMAdmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9c6d2-136"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c6d2-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c6d2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c6d2-138">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="9c6d2-138">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="9c6d2-139">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="9c6d2-139">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="9c6d2-140">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="9c6d2-140">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




