---
title: Messaggio LB_SETHORIZONTALEXTENT (winuser. h)
description: Imposta la larghezza, in pixel, in base alla quale è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole).
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- Controlli di Windows Message LB_SETHORIZONTALEXTENT
topic_type:
- apiref
api_name:
- LB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded17b9ea2d78a77b030950877047256d0e2a1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874338"
---
# <a name="lb_sethorizontalextent-message"></a><span data-ttu-id="c8122-104">\_Messaggio SETHORIZONTALEXTENT lb</span><span class="sxs-lookup"><span data-stu-id="c8122-104">LB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="c8122-105">Imposta la larghezza, in pixel, in base alla quale è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole).</span><span class="sxs-lookup"><span data-stu-id="c8122-105">Sets the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="c8122-106">Se la larghezza della casella di riepilogo è inferiore a questo valore, la barra di scorrimento orizzontale scorre orizzontalmente gli elementi nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="c8122-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="c8122-107">Se la larghezza della casella di riepilogo è maggiore o uguale a questo valore, la barra di scorrimento orizzontale viene nascosta.</span><span class="sxs-lookup"><span data-stu-id="c8122-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8122-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8122-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8122-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8122-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8122-110">Specifica il numero di pixel in base al quale è possibile scorrere la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="c8122-110">Specifies the number of pixels by which the list box can be scrolled.</span></span>

<span data-ttu-id="c8122-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="c8122-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span>

</dd> <dt>

<span data-ttu-id="c8122-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8122-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8122-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="c8122-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8122-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8122-114">Return value</span></span>

<span data-ttu-id="c8122-115">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="c8122-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8122-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8122-116">Remarks</span></span>

<span data-ttu-id="c8122-117">Per rispondere al messaggio **lb \_ SETHORIZONTALEXTENT** , è necessario che la casella di riepilogo sia stata definita con lo stile [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="c8122-117">To respond to the **LB\_SETHORIZONTALEXTENT** message, the list box must have been defined with the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style.</span></span>

<span data-ttu-id="c8122-118">Si noti che una casella di riepilogo non aggiorna in modo dinamico l'extent orizzontale.</span><span class="sxs-lookup"><span data-stu-id="c8122-118">Note that a list box does not update its horizontal extent dynamically.</span></span>

<span data-ttu-id="c8122-119">Questo messaggio non ha alcun effetto su una casella di riepilogo a più colonne.</span><span class="sxs-lookup"><span data-stu-id="c8122-119">This message has no effect on a multiple-column list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8122-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8122-120">Requirements</span></span>



| <span data-ttu-id="c8122-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8122-121">Requirement</span></span> | <span data-ttu-id="c8122-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c8122-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8122-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8122-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c8122-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8122-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c8122-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8122-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c8122-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c8122-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8122-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8122-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8122-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8122-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8122-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8122-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8122-130">**\_GETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="c8122-130">**LB\_GETHORIZONTALEXTENT**</span></span>](lb-gethorizontalextent.md)
</dt> </dl>

 

