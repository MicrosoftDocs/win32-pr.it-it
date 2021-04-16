---
title: Messaggio LB_SETITEMHEIGHT (winuser. h)
description: Imposta l'altezza, in pixel, degli elementi in una casella di riepilogo. Se la casella di riepilogo ha lo \_ stile OwnerDrawVariable lbs, questo messaggio imposta l'altezza dell'elemento specificato dal parametro wParam. In caso contrario, in questo messaggio viene impostata l'altezza di tutti gli elementi nella casella di riepilogo.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- Controlli di Windows Message LB_SETITEMHEIGHT
topic_type:
- apiref
api_name:
- LB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9985c5131a9eb1c8f0c45b6ab399b9e270f962cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478539"
---
# <a name="lb_setitemheight-message"></a><span data-ttu-id="fc195-106">\_Messaggio SETITEMHEIGHT lb</span><span class="sxs-lookup"><span data-stu-id="fc195-106">LB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="fc195-107">Imposta l'altezza, in pixel, degli elementi in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="fc195-107">Sets the height, in pixels, of items in a list box.</span></span> <span data-ttu-id="fc195-108">Se la casella di riepilogo ha lo stile [**\_ OwnerDrawVariable lbs**](list-box-styles.md) , questo messaggio imposta l'altezza dell'elemento specificato dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="fc195-108">If the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style, this message sets the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="fc195-109">In caso contrario, in questo messaggio viene impostata l'altezza di tutti gli elementi nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="fc195-109">Otherwise, this message sets the height of all items in the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc195-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc195-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc195-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc195-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc195-112">Specifica l'indice in base zero dell'elemento nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="fc195-112">Specifies the zero-based index of the item in the list box.</span></span> <span data-ttu-id="fc195-113">Usare questo parametro solo se la casella di riepilogo ha lo stile [**\_ OwnerDrawVariable lbs**](list-box-styles.md) . in caso contrario, impostarla su zero.</span><span class="sxs-lookup"><span data-stu-id="fc195-113">Use this parameter only if the list box has the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style; otherwise, set it to zero.</span></span>

<span data-ttu-id="fc195-114">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="fc195-114">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="fc195-115">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="fc195-115">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="fc195-116">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="fc195-116">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="fc195-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc195-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc195-118">Specifica l'altezza, in pixel, dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="fc195-118">Specifies the height, in pixels, of the item.</span></span> <span data-ttu-id="fc195-119">L'altezza massima è 255 pixel.</span><span class="sxs-lookup"><span data-stu-id="fc195-119">The maximum height is 255 pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc195-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc195-120">Return value</span></span>

<span data-ttu-id="fc195-121">Se l'indice o l'altezza non è valido, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="fc195-121">If the index or height is invalid, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc195-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc195-122">Requirements</span></span>



| <span data-ttu-id="fc195-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc195-123">Requirement</span></span> | <span data-ttu-id="fc195-124">Valore</span><span class="sxs-lookup"><span data-stu-id="fc195-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc195-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc195-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fc195-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc195-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fc195-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc195-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fc195-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fc195-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc195-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc195-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc195-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc195-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc195-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc195-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc195-132">**\_GETITEMHEIGHT lb**</span><span class="sxs-lookup"><span data-stu-id="fc195-132">**LB\_GETITEMHEIGHT**</span></span>](lb-getitemheight.md)
</dt> </dl>

 

 





