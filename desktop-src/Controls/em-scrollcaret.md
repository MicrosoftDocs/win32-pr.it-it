---
title: Messaggio EM_SCROLLCARET (winuser. h)
description: Scorre il punto di inserimento nella visualizzazione in un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 7a33034d-9369-49f8-a881-0c1d2cedff6a
keywords:
- Controlli di Windows Message EM_SCROLLCARET
topic_type:
- apiref
api_name:
- EM_SCROLLCARET
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa9f4bd69605f5e8fad36a683c9be2894546cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121494"
---
# <a name="em_scrollcaret-message"></a><span data-ttu-id="7ea6a-105">\_Messaggio SCROLLCARET em</span><span class="sxs-lookup"><span data-stu-id="7ea6a-105">EM\_SCROLLCARET message</span></span>

<span data-ttu-id="7ea6a-106">Scorre il punto di inserimento nella visualizzazione in un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="7ea6a-106">Scrolls the caret into view in an edit control.</span></span> <span data-ttu-id="7ea6a-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="7ea6a-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7ea6a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ea6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ea6a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7ea6a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ea6a-110">Questo parametro è riservato.</span><span class="sxs-lookup"><span data-stu-id="7ea6a-110">This parameter is reserved.</span></span> <span data-ttu-id="7ea6a-111">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="7ea6a-111">It should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7ea6a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7ea6a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7ea6a-113">Questo parametro è riservato.</span><span class="sxs-lookup"><span data-stu-id="7ea6a-113">This parameter is reserved.</span></span> <span data-ttu-id="7ea6a-114">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="7ea6a-114">It should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ea6a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ea6a-115">Return value</span></span>

<span data-ttu-id="7ea6a-116">Il valore restituito non è significativo.</span><span class="sxs-lookup"><span data-stu-id="7ea6a-116">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ea6a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ea6a-117">Remarks</span></span>

<span data-ttu-id="7ea6a-118">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="7ea6a-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="7ea6a-119">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="7ea6a-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ea6a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ea6a-120">Requirements</span></span>



| <span data-ttu-id="7ea6a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ea6a-121">Requirement</span></span> | <span data-ttu-id="7ea6a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7ea6a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ea6a-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ea6a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7ea6a-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ea6a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7ea6a-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ea6a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7ea6a-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7ea6a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7ea6a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ea6a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ea6a-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ea6a-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ea6a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ea6a-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="7ea6a-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7ea6a-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7ea6a-131">**\_LINESCROLL em**</span><span class="sxs-lookup"><span data-stu-id="7ea6a-131">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="7ea6a-132">**\_scorrimento em**</span><span class="sxs-lookup"><span data-stu-id="7ea6a-132">**EM\_SCROLL**</span></span>](em-scroll.md)
</dt> <dt>

[<span data-ttu-id="7ea6a-133">**\_VSCROLL WM**</span><span class="sxs-lookup"><span data-stu-id="7ea6a-133">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

 





