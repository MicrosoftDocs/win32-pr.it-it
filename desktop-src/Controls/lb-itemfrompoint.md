---
title: Messaggio LB_ITEMFROMPOINT (winuser. h)
description: Ottiene l'indice in base zero dell'elemento più vicino al punto specificato in una casella di riepilogo.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- Controlli di Windows Message LB_ITEMFROMPOINT
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743023"
---
# <a name="lb_itemfrompoint-message"></a><span data-ttu-id="d5da2-104">\_Messaggio ITEMFROMPOINT lb</span><span class="sxs-lookup"><span data-stu-id="d5da2-104">LB\_ITEMFROMPOINT message</span></span>

<span data-ttu-id="d5da2-105">Ottiene l'indice in base zero dell'elemento più vicino al punto specificato in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="d5da2-105">Gets the zero-based index of the item nearest the specified point in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5da2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5da2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5da2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5da2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5da2-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="d5da2-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d5da2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5da2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5da2-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la coordinata x di un punto, relativa all'angolo superiore sinistro dell'area client della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="d5da2-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

<span data-ttu-id="d5da2-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la coordinata y di un punto, relativa all'angolo superiore sinistro dell'area client della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="d5da2-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5da2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5da2-112">Return value</span></span>

<span data-ttu-id="d5da2-113">Il valore restituito contiene l'indice dell'elemento più vicino in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d5da2-113">The return value contains the index of the nearest item in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span> <span data-ttu-id="d5da2-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è zero se il punto specificato si trova nell'area client della casella di riepilogo o uno se è all'esterno dell'area client.</span><span class="sxs-lookup"><span data-stu-id="d5da2-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is zero if the specified point is in the client area of the list box, or one if it is outside the client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5da2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5da2-115">Requirements</span></span>



| <span data-ttu-id="d5da2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5da2-116">Requirement</span></span> | <span data-ttu-id="d5da2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d5da2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5da2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5da2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d5da2-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5da2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d5da2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5da2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d5da2-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d5da2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d5da2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5da2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5da2-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5da2-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5da2-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5da2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5da2-125">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="d5da2-125">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

