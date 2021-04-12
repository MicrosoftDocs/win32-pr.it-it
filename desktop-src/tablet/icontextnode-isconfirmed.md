---
description: Recupera un valore che indica se l'oggetto ConfirmationType passato a questo metodo è stato impostato su questo IContextNode.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'Metodo IContextNode:: IsValid (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 300e0126b4a1ff55d372ff31deebde0eab686645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526520"
---
# <a name="icontextnodeisconfirmed-method"></a><span data-ttu-id="ed07e-103">Metodo IContextNode:: IsValid</span><span class="sxs-lookup"><span data-stu-id="ed07e-103">IContextNode::IsConfirmed method</span></span>

<span data-ttu-id="ed07e-104">Recupera un valore che indica se l'oggetto ConfirmationType passato a questo metodo è stato impostato su questo IContextNode.</span><span class="sxs-lookup"><span data-stu-id="ed07e-104">Retrieves a value that indicates whether the ConfirmationType passed in to this method has been set on this IContextNode.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed07e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed07e-105">Syntax</span></span>


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a><span data-ttu-id="ed07e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed07e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed07e-107">*confirmedType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed07e-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed07e-108">Tipo di conferma sottoposto a test.</span><span class="sxs-lookup"><span data-stu-id="ed07e-108">The confirmation type being tested for.</span></span>

</dd> <dt>

<span data-ttu-id="ed07e-109">*pfTypeConfirmed* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ed07e-109">*pfTypeConfirmed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed07e-110">**Variante \_ TRUE** se il tipo passato in confirmedType è stato impostato su questo oggetto [**IContextNode**](icontextnode.md) ; in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="ed07e-110">**VARIANT\_TRUE** if the type passed in confirmedType has been set on this [**IContextNode**](icontextnode.md) object; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed07e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed07e-111">Return value</span></span>

<span data-ttu-id="ed07e-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ed07e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ed07e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed07e-113">Remarks</span></span>

<span data-ttu-id="ed07e-114">Questo valore viene impostato dal metodo [**IContextNode:: Confirm**](icontextnode-confirm.md) .</span><span class="sxs-lookup"><span data-stu-id="ed07e-114">This value is set by the [**IContextNode::Confirm**](icontextnode-confirm.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed07e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed07e-115">Requirements</span></span>



| <span data-ttu-id="ed07e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed07e-116">Requirement</span></span> | <span data-ttu-id="ed07e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ed07e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed07e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed07e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ed07e-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ed07e-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ed07e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed07e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ed07e-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ed07e-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ed07e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed07e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed07e-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ed07e-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ed07e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ed07e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed07e-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed07e-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ed07e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed07e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed07e-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ed07e-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ed07e-128">**IContextNode:: Confirm**</span><span class="sxs-lookup"><span data-stu-id="ed07e-128">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="ed07e-129">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ed07e-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




