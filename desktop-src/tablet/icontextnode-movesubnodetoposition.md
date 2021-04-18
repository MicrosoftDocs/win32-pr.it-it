---
description: Riordina un oggetto IContextNode figlio specificato nell'indice specificato.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'Metodo IContextNode:: MoveSubNodeToPosition (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307421"
---
# <a name="icontextnodemovesubnodetoposition-method"></a><span data-ttu-id="7aaf3-103">Metodo IContextNode:: MoveSubNodeToPosition</span><span class="sxs-lookup"><span data-stu-id="7aaf3-103">IContextNode::MoveSubNodeToPosition method</span></span>

<span data-ttu-id="7aaf3-104">Riordina un oggetto [**IContextNode**](icontextnode.md) figlio specificato nell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="7aaf3-104">Reorders a specified child [**IContextNode**](icontextnode.md) object to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aaf3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7aaf3-105">Syntax</span></span>


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="7aaf3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7aaf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aaf3-107">*pSubnodeToMove* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7aaf3-107">*pSubnodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aaf3-108">Oggetto [**IContextNode**](icontextnode.md) da spostare.</span><span class="sxs-lookup"><span data-stu-id="7aaf3-108">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="7aaf3-109">*ulNewIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7aaf3-109">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aaf3-110">Indice per la nuova posizione del sottonodo.</span><span class="sxs-lookup"><span data-stu-id="7aaf3-110">The index for the new position of the subnode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aaf3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7aaf3-111">Return value</span></span>

<span data-ttu-id="7aaf3-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7aaf3-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7aaf3-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7aaf3-113">Remarks</span></span>

<span data-ttu-id="7aaf3-114">Restituisce **E \_ INVALIDARG** se *pSubnodeToMove* non è un nodo figlio di questo [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="7aaf3-114">Returns **E\_INVALIDARG** if *pSubnodeToMove* is not a child node of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7aaf3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7aaf3-115">Requirements</span></span>



| <span data-ttu-id="7aaf3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aaf3-116">Requirement</span></span> | <span data-ttu-id="7aaf3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7aaf3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7aaf3-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7aaf3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7aaf3-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7aaf3-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7aaf3-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7aaf3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7aaf3-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7aaf3-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7aaf3-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7aaf3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7aaf3-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7aaf3-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7aaf3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7aaf3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7aaf3-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7aaf3-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7aaf3-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7aaf3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aaf3-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="7aaf3-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="7aaf3-128">**IContextNode:: CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="7aaf3-128">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="7aaf3-129">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="7aaf3-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




