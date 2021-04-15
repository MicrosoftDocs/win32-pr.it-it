---
title: Messaggio LB_GETCOUNT (winuser. h)
description: Ottiene il numero di elementi in una casella di riepilogo.
ms.assetid: 1fbe44fc-8b9d-4bfa-a8bb-06817eecf064
keywords:
- Controlli di Windows Message LB_GETCOUNT
topic_type:
- apiref
api_name:
- LB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddedbd7b9165e00e722edbadbb8806a68417551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478964"
---
# <a name="lb_getcount-message"></a><span data-ttu-id="9905e-104">LB \_ GETcount-messaggio</span><span class="sxs-lookup"><span data-stu-id="9905e-104">LB\_GETCOUNT message</span></span>

<span data-ttu-id="9905e-105">Ottiene il numero di elementi in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="9905e-105">Gets the number of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="9905e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9905e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9905e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9905e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9905e-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9905e-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9905e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9905e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9905e-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9905e-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9905e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9905e-111">Return value</span></span>

<span data-ttu-id="9905e-112">Il valore restituito è il numero di elementi nella casella di riepilogo oppure LB \_ Err se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="9905e-112">The return value is the number of items in the list box, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="9905e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9905e-113">Remarks</span></span>

<span data-ttu-id="9905e-114">Il conteggio restituito è maggiore di uno rispetto al valore di indice dell'ultimo elemento (l'indice è in base zero).</span><span class="sxs-lookup"><span data-stu-id="9905e-114">The returned count is one greater than the index value of the last item (the index is zero-based).</span></span>

## <a name="requirements"></a><span data-ttu-id="9905e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9905e-115">Requirements</span></span>



| <span data-ttu-id="9905e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9905e-116">Requirement</span></span> | <span data-ttu-id="9905e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9905e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9905e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9905e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9905e-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9905e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9905e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9905e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9905e-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9905e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9905e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9905e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9905e-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9905e-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9905e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9905e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9905e-125">**\_conteggio lb**</span><span class="sxs-lookup"><span data-stu-id="9905e-125">**LB\_SETCOUNT**</span></span>](lb-setcount.md)
</dt> </dl>

 

 





