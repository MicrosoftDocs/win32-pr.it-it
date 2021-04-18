---
description: Contiene una raccolta di oggetti che implementano l'interfaccia IContextNode e che sono il risultato di un'operazione di analisi dell'input penna.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: Interfaccia IContextNodes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 306abcd32dcb0ee55978a6b95ee9f8a2c22cd19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307411"
---
# <a name="icontextnodes-interface"></a><span data-ttu-id="c878b-103">Interfaccia IContextNodes</span><span class="sxs-lookup"><span data-stu-id="c878b-103">IContextNodes interface</span></span>

<span data-ttu-id="c878b-104">Contiene una raccolta di oggetti che implementano l'interfaccia [**IContextNode**](icontextnode.md) e che sono il risultato di un'operazione di analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="c878b-104">Contains a collection of objects that implement the [**IContextNode**](icontextnode.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="c878b-105">Membri</span><span class="sxs-lookup"><span data-stu-id="c878b-105">Members</span></span>

<span data-ttu-id="c878b-106">L'interfaccia **IContextNodes** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c878b-106">The **IContextNodes** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c878b-107">**IContextNodes** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c878b-107">**IContextNodes** also has these types of members:</span></span>

-   [<span data-ttu-id="c878b-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="c878b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c878b-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="c878b-109">Methods</span></span>

<span data-ttu-id="c878b-110">L'interfaccia **IContextNodes** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c878b-110">The **IContextNodes** interface has these methods.</span></span>



| <span data-ttu-id="c878b-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="c878b-111">Method</span></span>                                                       | <span data-ttu-id="c878b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c878b-112">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c878b-113">**AddContextNode**</span><span class="sxs-lookup"><span data-stu-id="c878b-113">**AddContextNode**</span></span>](icontextnodes-addcontextnode.md)       | <span data-ttu-id="c878b-114">Aggiunge un oggetto [**IContextNode**](icontextnode.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="c878b-114">Adds an [**IContextNode**](icontextnode.md) object to this collection.</span></span> <br/>                                  |
| [<span data-ttu-id="c878b-115">**Getcontextnode**</span><span class="sxs-lookup"><span data-stu-id="c878b-115">**GetContextNode**</span></span>](icontextnodes-getcontextnode.md)       | <span data-ttu-id="c878b-116">Recupera l'oggetto [**IContextNode**](icontextnode.md) in corrispondenza dell'indice specificato all'interno di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="c878b-116">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span> <br/> |
| [<span data-ttu-id="c878b-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="c878b-117">**GetCount**</span></span>](icontextnodes-getcount.md)                   | <span data-ttu-id="c878b-118">Recupera il numero di oggetti [**IContextNode**](icontextnode.md) contenuti in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="c878b-118">Retrieves the number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span> <br/>       |
| [<span data-ttu-id="c878b-119">**RemoveContextNode**</span><span class="sxs-lookup"><span data-stu-id="c878b-119">**RemoveContextNode**</span></span>](icontextnodes-removecontextnode.md) | <span data-ttu-id="c878b-120">Rimuove un oggetto [**IContextNode**](icontextnode.md) da questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="c878b-120">Removes an [**IContextNode**](icontextnode.md) object from this collection.</span></span> <br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="c878b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c878b-121">Requirements</span></span>



| <span data-ttu-id="c878b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c878b-122">Requirement</span></span> | <span data-ttu-id="c878b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c878b-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c878b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c878b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c878b-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c878b-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c878b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c878b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c878b-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c878b-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c878b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c878b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c878b-129"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c878b-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c878b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c878b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c878b-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c878b-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c878b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c878b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c878b-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="c878b-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c878b-134">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="c878b-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

