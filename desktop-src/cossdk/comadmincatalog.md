---
description: Accede ai dati archiviati nel catalogo COM+.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: Classe COMAdminCatalog (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: fa6e71d13f5a3d157bd3ce1035d0616dc1e5a519
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483613"
---
# <a name="comadmincatalog-class"></a><span data-ttu-id="b7b4f-103">Classe COMAdminCatalog</span><span class="sxs-lookup"><span data-stu-id="b7b4f-103">COMAdminCatalog class</span></span>

<span data-ttu-id="b7b4f-104">Accede ai dati archiviati nel catalogo COM+.</span><span class="sxs-lookup"><span data-stu-id="b7b4f-104">Accesses the data that is stored in the COM+ catalog.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="b7b4f-105">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="b7b4f-105">When to implement</span></span>

<span data-ttu-id="b7b4f-106">Questa classe è implementata da COM+.</span><span class="sxs-lookup"><span data-stu-id="b7b4f-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="b7b4f-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7b4f-107">Requirement</span></span> | <span data-ttu-id="b7b4f-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b7b4f-108">Value</span></span> |
|------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b4f-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="b7b4f-109">CLSID</span></span>      | <span data-ttu-id="b7b4f-110">\_COMADMINCATALOG CLSID</span><span class="sxs-lookup"><span data-stu-id="b7b4f-110">CLSID\_COMAdminCatalog</span></span>                                                                                            |
| <span data-ttu-id="b7b4f-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="b7b4f-111">ProgID</span></span>     | <span data-ttu-id="b7b4f-112">L "COMAdmin. COMAdminCatalog"</span><span class="sxs-lookup"><span data-stu-id="b7b4f-112">L"COMAdmin.COMAdminCatalog"</span></span>                                                                                       |
| <span data-ttu-id="b7b4f-113">Interfacce</span><span class="sxs-lookup"><span data-stu-id="b7b4f-113">Interfaces</span></span> | [<span data-ttu-id="b7b4f-114">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="b7b4f-114">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [<span data-ttu-id="b7b4f-115">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="b7b4f-115">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="b7b4f-116">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b7b4f-116">When to use</span></span>

<span data-ttu-id="b7b4f-117">Gli oggetti creati dalla classe **COMAdminCatalog** vengono utilizzati per avviare l'accesso a livello di codice ai dati di configurazione com+ archiviati nel catalogo com+.</span><span class="sxs-lookup"><span data-stu-id="b7b4f-117">You use objects created from the **COMAdminCatalog** class to begin programmatic access to COM+ configuration data stored in the COM+ catalog.</span></span> <span data-ttu-id="b7b4f-118">Queste informazioni si basano sulle cartelle e sugli elementi nell'albero della console dello strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="b7b4f-118">This information underlies the folders and items in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="b7b4f-119">La classe **COMAdminCatalog** consente di accedere alle raccolte nel catalogo, installare componenti e applicazioni com+, avviare e arrestare i servizi e connettersi ai server remoti e gestirli.</span><span class="sxs-lookup"><span data-stu-id="b7b4f-119">The **COMAdminCatalog** class enables you to access collections in the catalog, install COM+ applications and components, start and stop services, and connect to and administer remote servers.</span></span>

<span data-ttu-id="b7b4f-120">Le cartelle dello strumento di amministrazione Servizi componenti corrispondono alle raccolte nel catalogo, che è possibile rappresentare usando gli oggetti creati dalla classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="b7b4f-120">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span> <span data-ttu-id="b7b4f-121">Gli elementi nelle cartelle corrispondono agli elementi delle raccolte, che è possibile rappresentare usando gli oggetti creati dalla classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="b7b4f-121">Items in the folders correspond to items in the collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="b7b4f-122">Non tutte le raccolte e gli elementi esposti tramite [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e [**COMAdminCatalogObject**](comadmincatalogobject.md) sono disponibili nello strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="b7b4f-122">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and [**COMAdminCatalogObject**](comadmincatalogobject.md) are available in the Component Services administration tool.</span></span>

<span data-ttu-id="b7b4f-123">Per informazioni sulle raccolte specifiche e sulle relative proprietà, vedere la pagina relativa alle [raccolte di amministrazione com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="b7b4f-123">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="b7b4f-124">Per un'introduzione all'amministrazione a livello di codice di COM+, vedere [automazione dell'amministrazione com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="b7b4f-124">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7b4f-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7b4f-125">Remarks</span></span>

<span data-ttu-id="b7b4f-126">Per creare questo oggetto, chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="b7b4f-126">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="b7b4f-127">Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi amministratore COM+.</span><span class="sxs-lookup"><span data-stu-id="b7b4f-127">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="b7b4f-128">Un oggetto COMAdminCatalog può essere dichiarato utilizzando "COMAdmin. COMAdminCatalog" come nome della classe.</span><span class="sxs-lookup"><span data-stu-id="b7b4f-128">A COMAdminCatalog object can be declared using "COMAdmin.COMAdminCatalog" as the class name.</span></span>

<span data-ttu-id="b7b4f-129">In COM+ 1,5, rilasciato con Windows XP, la classe **COMAdminCatalog** implementa l'interfaccia [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) .</span><span class="sxs-lookup"><span data-stu-id="b7b4f-129">In COM+ 1.5, released with Windows XP, the **COMAdminCatalog** class implements the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface.</span></span> <span data-ttu-id="b7b4f-130">Tuttavia, in COM+ 1,0, rilasciato con Windows 2000, la classe **COMAdminCatalog** implementa solo l'interfaccia [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .</span><span class="sxs-lookup"><span data-stu-id="b7b4f-130">However, in COM+ 1.0, released with Windows 2000, the **COMAdminCatalog** class implements only the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7b4f-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7b4f-131">Requirements</span></span>



| <span data-ttu-id="b7b4f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7b4f-132">Requirement</span></span> | <span data-ttu-id="b7b4f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b7b4f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b4f-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7b4f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b7b4f-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b7b4f-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b7b4f-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7b4f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b7b4f-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b7b4f-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b7b4f-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7b4f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7b4f-139"><dt>COMAdmin. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7b4f-139"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7b4f-140">IDL</span><span class="sxs-lookup"><span data-stu-id="b7b4f-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7b4f-141"><dt>COMAdmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7b4f-141"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7b4f-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7b4f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7b4f-143">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="b7b4f-143">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="b7b4f-144">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="b7b4f-144">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="b7b4f-145">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="b7b4f-145">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[<span data-ttu-id="b7b4f-146">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="b7b4f-146">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

