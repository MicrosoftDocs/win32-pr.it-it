---
description: Recupera un nome di tipo leggibile di questo IContextNode.
ms.assetid: 02031efd-1e9c-4e96-8dc1-280cc1a6e58f
title: 'Metodo IContextNode:: getTypeName (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetTypeName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9d7bc4a24b7abc3ee507d7bda0c547f4c55a787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129491"
---
# <a name="icontextnodegettypename-method"></a><span data-ttu-id="adba0-103">Metodo IContextNode:: getTypeName</span><span class="sxs-lookup"><span data-stu-id="adba0-103">IContextNode::GetTypeName method</span></span>

<span data-ttu-id="adba0-104">Recupera un nome di tipo leggibile di questo [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="adba0-104">Retrieves a human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="adba0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="adba0-105">Syntax</span></span>


```C++
HRESULT GetTypeName(
  [out] BSTR *pbstrContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="adba0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="adba0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adba0-107">*pbstrContextNodeType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="adba0-107">*pbstrContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="adba0-108">Nome di tipo leggibile di questo [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="adba0-108">A human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adba0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="adba0-109">Return value</span></span>

<span data-ttu-id="adba0-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="adba0-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="adba0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="adba0-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="adba0-112">Per evitare una perdita di memoria, chiamare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) su \* *pbstrContextNodeType* quando non è più necessario usare la stringa.</span><span class="sxs-lookup"><span data-stu-id="adba0-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrContextNodeType* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="adba0-113">Questo metodo, ad esempio, imposta *pbstrContextNodeType* su "InkWordNode" per un nodo di tipo input penna (vedere [tipi di nodo](context-node-types.md) [**IContextNode:: GetType**](icontextnode-gettype.md) e context).</span><span class="sxs-lookup"><span data-stu-id="adba0-113">For example, this method sets *pbstrContextNodeType* to "InkWordNode" for an ink word node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="adba0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="adba0-114">Requirements</span></span>



| <span data-ttu-id="adba0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="adba0-115">Requirement</span></span> | <span data-ttu-id="adba0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="adba0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adba0-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adba0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="adba0-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="adba0-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="adba0-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adba0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="adba0-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="adba0-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="adba0-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="adba0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="adba0-122"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="adba0-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="adba0-123">DLL</span><span class="sxs-lookup"><span data-stu-id="adba0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adba0-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adba0-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="adba0-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="adba0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adba0-126">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="adba0-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="adba0-127">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="adba0-127">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="adba0-128">Tipi di nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="adba0-128">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="adba0-129">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="adba0-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

