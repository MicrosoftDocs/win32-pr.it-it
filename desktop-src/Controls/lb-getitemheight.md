---
title: Messaggio LB_GETITEMHEIGHT (winuser. h)
description: Ottiene l'altezza degli elementi in una casella di riepilogo.
ms.assetid: ee96fce6-babd-4581-ac0e-2eb955fe543b
keywords:
- Controlli di Windows Message LB_GETITEMHEIGHT
topic_type:
- apiref
api_name:
- LB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44aa9e9b6d52c082a5f33a10280837a33372245
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873661"
---
# <a name="lb_getitemheight-message"></a><span data-ttu-id="2cafc-104">\_Messaggio GETITEMHEIGHT lb</span><span class="sxs-lookup"><span data-stu-id="2cafc-104">LB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="2cafc-105">Ottiene l'altezza degli elementi in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="2cafc-105">Gets the height of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="2cafc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2cafc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cafc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2cafc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cafc-108">Indice in base zero dell'elemento della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="2cafc-108">The zero-based index of the list box item.</span></span> <span data-ttu-id="2cafc-109">Questo indice viene usato solo se la casella di riepilogo ha lo stile [**\_ OwnerDrawVariable lbs**](list-box-styles.md) . in caso contrario, deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2cafc-109">This index is used only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, it must be zero.</span></span>

<span data-ttu-id="2cafc-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="2cafc-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="2cafc-111">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="2cafc-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="2cafc-112">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="2cafc-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="2cafc-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2cafc-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cafc-114">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="2cafc-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cafc-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2cafc-115">Return value</span></span>

<span data-ttu-id="2cafc-116">Il valore restituito è l'altezza, in pixel, di ogni elemento nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="2cafc-116">The return value is the height, in pixels, of each item in the list box.</span></span> <span data-ttu-id="2cafc-117">Il valore restituito è l'altezza dell'elemento specificato dal parametro *wParam* se la casella di riepilogo ha lo stile [**\_ OwnerDrawVariable lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2cafc-117">The return value is the height of the item specified by the *wParam* parameter if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style.</span></span> <span data-ttu-id="2cafc-118">Il valore restituito è LB \_ Err se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="2cafc-118">The return value is LB\_ERR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cafc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cafc-119">Requirements</span></span>



| <span data-ttu-id="2cafc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cafc-120">Requirement</span></span> | <span data-ttu-id="2cafc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2cafc-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cafc-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cafc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2cafc-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2cafc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2cafc-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cafc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2cafc-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2cafc-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2cafc-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2cafc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cafc-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2cafc-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cafc-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cafc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cafc-129">**\_SETITEMHEIGHT lb**</span><span class="sxs-lookup"><span data-stu-id="2cafc-129">**LB\_SETITEMHEIGHT**</span></span>](lb-setitemheight.md)
</dt> </dl>

 

 





