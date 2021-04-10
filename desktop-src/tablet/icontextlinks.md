---
description: Contiene una raccolta di oggetti che implementano l'interfaccia IContextLink.
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: Interfaccia IContextLinks (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b68563aad471a5420b1157e1c5c12d26da17b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966728"
---
# <a name="icontextlinks-interface"></a><span data-ttu-id="933e0-103">Interfaccia IContextLinks</span><span class="sxs-lookup"><span data-stu-id="933e0-103">IContextLinks interface</span></span>

<span data-ttu-id="933e0-104">Contiene una raccolta di oggetti che implementano l'interfaccia [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="933e0-104">Contains a collection of objects that implement the [**IContextLink**](icontextlink.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="933e0-105">Membri</span><span class="sxs-lookup"><span data-stu-id="933e0-105">Members</span></span>

<span data-ttu-id="933e0-106">L'interfaccia **IContextLinks** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="933e0-106">The **IContextLinks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="933e0-107">**IContextLinks** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="933e0-107">**IContextLinks** also has these types of members:</span></span>

-   [<span data-ttu-id="933e0-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="933e0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="933e0-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="933e0-109">Methods</span></span>

<span data-ttu-id="933e0-110">L'interfaccia **IContextLinks** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="933e0-110">The **IContextLinks** interface has these methods.</span></span>



| <span data-ttu-id="933e0-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="933e0-111">Method</span></span>                                                 | <span data-ttu-id="933e0-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="933e0-112">Description</span></span>                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="933e0-113">**GetContextLink**</span><span class="sxs-lookup"><span data-stu-id="933e0-113">**GetContextLink**</span></span>](icontextlinks-getcontextlink.md) | <span data-ttu-id="933e0-114">Recupera l'oggetto [**IContextLink**](icontextlink.md) in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="933e0-114">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span><br/>               |
| [<span data-ttu-id="933e0-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="933e0-115">**GetCount**</span></span>](icontextlinks-getcount.md)             | <span data-ttu-id="933e0-116">Recupera il numero di oggetti [**IContextLink**](icontextlink.md) in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="933e0-116">Retrieves the number of [**IContextLink**](icontextlink.md) objects in this collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="933e0-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="933e0-117">Remarks</span></span>

<span data-ttu-id="933e0-118">Questa operazione viene in genere utilizzata tramite il metodo [**IContextNode:: GetContextLinks**](icontextnode-getcontextlinks.md) .</span><span class="sxs-lookup"><span data-stu-id="933e0-118">This is usually accessed through the [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="933e0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="933e0-119">Requirements</span></span>



| <span data-ttu-id="933e0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="933e0-120">Requirement</span></span> | <span data-ttu-id="933e0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="933e0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="933e0-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="933e0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="933e0-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="933e0-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="933e0-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="933e0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="933e0-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="933e0-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="933e0-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="933e0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="933e0-127"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="933e0-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="933e0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="933e0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="933e0-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="933e0-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="933e0-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="933e0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="933e0-131">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="933e0-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="933e0-132">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="933e0-132">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="933e0-133">**IContextNode::D eleteContextLink**</span><span class="sxs-lookup"><span data-stu-id="933e0-133">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="933e0-134">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="933e0-134">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="933e0-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="933e0-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

