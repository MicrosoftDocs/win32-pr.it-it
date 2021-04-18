---
description: Rappresenta una relazione tra due oggetti IContextNode.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: Interfaccia IContextLink (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df1e0d8717ba29532486277aced19f17adb1d79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307448"
---
# <a name="icontextlink-interface"></a><span data-ttu-id="e74e2-103">Interfaccia IContextLink</span><span class="sxs-lookup"><span data-stu-id="e74e2-103">IContextLink interface</span></span>

<span data-ttu-id="e74e2-104">Rappresenta una relazione tra due oggetti [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="e74e2-104">Represents a relationship between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="e74e2-105">Membri</span><span class="sxs-lookup"><span data-stu-id="e74e2-105">Members</span></span>

<span data-ttu-id="e74e2-106">L'interfaccia **IContextLink** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e74e2-106">The **IContextLink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e74e2-107">**IContextLink** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e74e2-107">**IContextLink** also has these types of members:</span></span>

-   [<span data-ttu-id="e74e2-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="e74e2-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e74e2-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="e74e2-109">Methods</span></span>

<span data-ttu-id="e74e2-110">L'interfaccia **IContextLink** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e74e2-110">The **IContextLink** interface has these methods.</span></span>



| <span data-ttu-id="e74e2-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="e74e2-111">Method</span></span>                                                                  | <span data-ttu-id="e74e2-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e74e2-112">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e74e2-113">**GetContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="e74e2-113">**GetContextLinkDirection**</span></span>](icontextlink-getcontextlinkdirection.md) | <span data-ttu-id="e74e2-114">Recupera il tipo di relazione rappresentata da questo **IContextLink** .</span><span class="sxs-lookup"><span data-stu-id="e74e2-114">Retrieves the type of relationship this **IContextLink** represents.</span></span><br/>                                         |
| [<span data-ttu-id="e74e2-115">**GetDestinationNode**</span><span class="sxs-lookup"><span data-stu-id="e74e2-115">**GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)           | <span data-ttu-id="e74e2-116">Recupera l'oggetto [**IContextNode**](icontextnode.md) che rappresenta la destinazione per questo **IContextLink**.</span><span class="sxs-lookup"><span data-stu-id="e74e2-116">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this **IContextLink**.</span></span><br/> |
| [<span data-ttu-id="e74e2-117">**GetSourceNode**</span><span class="sxs-lookup"><span data-stu-id="e74e2-117">**GetSourceNode**</span></span>](icontextlink-getsourcenode.md)                     | <span data-ttu-id="e74e2-118">Recupera l'oggetto [**IContextNode**](icontextnode.md) che rappresenta l'origine per questo **IContextLink**.</span><span class="sxs-lookup"><span data-stu-id="e74e2-118">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this **IContextLink**.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="e74e2-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e74e2-119">Remarks</span></span>

<span data-ttu-id="e74e2-120">Di seguito è riportato un esempio di una relazione rappresentata da un oggetto **IContextLink** :</span><span class="sxs-lookup"><span data-stu-id="e74e2-120">The following is an example of a relationship represented by an **IContextLink** object:</span></span>

-   <span data-ttu-id="e74e2-121">Quando si usa un nodo AnalysisHint nell'analisi dell'input penna, l'operazione di analisi dell'input penna crea un oggetto **IContextLink** di tipo AnalysisHint tra il nodo hint di analisi e il nodo che contiene la scrittura all'interno dell'area dell'hint.</span><span class="sxs-lookup"><span data-stu-id="e74e2-121">When an AnalysisHint node is used in ink analysis, the ink analysis operation creates an **IContextLink** object of type AnalysisHint between the analysis hint node and the node that contains writing within the area of the hint.</span></span> <span data-ttu-id="e74e2-122">Il nodo di origine è il nodo hint di analisi e il nodo di destinazione è il nodo che contiene la scrittura.</span><span class="sxs-lookup"><span data-stu-id="e74e2-122">The source node is the analysis hint node and the destination node is the node that contains writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e74e2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e74e2-123">Requirements</span></span>



| <span data-ttu-id="e74e2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e74e2-124">Requirement</span></span> | <span data-ttu-id="e74e2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e74e2-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e74e2-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e74e2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e74e2-127">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e74e2-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e74e2-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e74e2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e74e2-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e74e2-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e74e2-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e74e2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e74e2-131"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e74e2-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e74e2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e74e2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e74e2-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e74e2-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e74e2-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e74e2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e74e2-135">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="e74e2-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="e74e2-136">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="e74e2-136">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="e74e2-137">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="e74e2-137">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="e74e2-138">Tipi di nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="e74e2-138">Context Node Types</span></span>](context-node-types.md)
</dt> </dl>

 

