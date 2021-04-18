---
description: Recupera una raccolta di oggetti IContextLink che rappresenta relazioni con altri oggetti IContextNode.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: 'Metodo IContextNode:: GetContextLinks (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de62550a09d0a538ddc680f6d57c35a1016fe255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307439"
---
# <a name="icontextnodegetcontextlinks-method"></a><span data-ttu-id="b1686-103">Metodo IContextNode:: GetContextLinks</span><span class="sxs-lookup"><span data-stu-id="b1686-103">IContextNode::GetContextLinks method</span></span>

<span data-ttu-id="b1686-104">Recupera una raccolta di oggetti [**IContextLink**](icontextlink.md) che rappresenta relazioni con altri oggetti [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b1686-104">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1686-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1686-105">Syntax</span></span>


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a><span data-ttu-id="b1686-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1686-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1686-107">*ppContextLinks* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1686-107">*ppContextLinks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1686-108">Puntatore a una raccolta di oggetti [**IContextLink**](icontextlink.md) che rappresenta relazioni con altri oggetti [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b1686-108">A pointer to a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other [**IContextNode**](icontextnode.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1686-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1686-109">Return value</span></span>

<span data-ttu-id="b1686-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b1686-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1686-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1686-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b1686-112">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppContextLinks* quando non è più necessario usare la raccolta di collegamenti di contesto.</span><span class="sxs-lookup"><span data-stu-id="b1686-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLinks* when you no longer need to use the context links collection.</span></span>

 

<span data-ttu-id="b1686-113">Per ottenere informazioni sulle relazioni del nodo padre o figlio, utilizzare [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) o [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md).</span><span class="sxs-lookup"><span data-stu-id="b1686-113">To get information about parent or child node relationships, use [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) or [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md).</span></span>

<span data-ttu-id="b1686-114">Per ulteriori informazioni sui tipi di relazioni descritti dai collegamenti, vedere [**IContextLink**](icontextlink.md) e [**ContextLinkDirection**](contextlinkdirection.md).</span><span class="sxs-lookup"><span data-stu-id="b1686-114">For more information about the kinds of relationships that are described by links, see [**IContextLink**](icontextlink.md) and [**ContextLinkDirection**](contextlinkdirection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1686-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1686-115">Requirements</span></span>



| <span data-ttu-id="b1686-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1686-116">Requirement</span></span> | <span data-ttu-id="b1686-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b1686-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1686-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1686-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b1686-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b1686-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b1686-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1686-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b1686-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b1686-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b1686-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1686-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1686-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b1686-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b1686-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b1686-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1686-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1686-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b1686-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1686-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1686-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="b1686-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b1686-128">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="b1686-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="b1686-129">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="b1686-129">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="b1686-130">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="b1686-130">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="b1686-131">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="b1686-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

