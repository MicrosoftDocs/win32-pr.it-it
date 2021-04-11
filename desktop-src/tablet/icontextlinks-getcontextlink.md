---
description: Recupera l'oggetto IContextLink in corrispondenza dell'indice specificato.
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: 'Metodo IContextLinks:: GetContextLink (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ecc0ed9ba457a7a91cb2e1b615ac7419ce5a94c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129510"
---
# <a name="icontextlinksgetcontextlink-method"></a><span data-ttu-id="34a06-103">Metodo IContextLinks:: GetContextLink</span><span class="sxs-lookup"><span data-stu-id="34a06-103">IContextLinks::GetContextLink method</span></span>

<span data-ttu-id="34a06-104">Recupera l'oggetto [**IContextLink**](icontextlink.md) in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="34a06-104">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a06-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34a06-105">Syntax</span></span>


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a><span data-ttu-id="34a06-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34a06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34a06-107">*ulIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34a06-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a06-108">Indice in base zero dell'oggetto [**IContextLink**](icontextlink.md) da ottenere.</span><span class="sxs-lookup"><span data-stu-id="34a06-108">The zero-based index of the [**IContextLink**](icontextlink.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="34a06-109">*ppContextLink* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="34a06-109">*ppContextLink* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34a06-110">Puntatore all'oggetto [**IContextLink**](icontextlink.md) in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="34a06-110">A pointer to the [**IContextLink**](icontextlink.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34a06-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34a06-111">Return value</span></span>

<span data-ttu-id="34a06-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="34a06-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="34a06-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="34a06-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="34a06-114">Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *ppContextLink* quando non è più necessario usare il collegamento di contesto.</span><span class="sxs-lookup"><span data-stu-id="34a06-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLink* when you no longer need to use the context link.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="34a06-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34a06-115">Requirements</span></span>



| <span data-ttu-id="34a06-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="34a06-116">Requirement</span></span> | <span data-ttu-id="34a06-117">Valore</span><span class="sxs-lookup"><span data-stu-id="34a06-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34a06-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34a06-118">Minimum supported client</span></span><br/> | <span data-ttu-id="34a06-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="34a06-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="34a06-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34a06-120">Minimum supported server</span></span><br/> | <span data-ttu-id="34a06-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="34a06-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="34a06-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34a06-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="34a06-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="34a06-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="34a06-124">DLL</span><span class="sxs-lookup"><span data-stu-id="34a06-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34a06-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34a06-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="34a06-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34a06-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a06-127">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="34a06-127">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="34a06-128">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="34a06-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="34a06-129">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="34a06-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

