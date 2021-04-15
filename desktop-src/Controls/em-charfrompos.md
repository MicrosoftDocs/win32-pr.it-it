---
title: Messaggio EM_CHARFROMPOS (winuser. h)
description: Ottiene informazioni sul carattere più vicino a un punto specificato nell'area client di un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- Controlli di Windows Message EM_CHARFROMPOS
topic_type:
- apiref
api_name:
- EM_CHARFROMPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1156d69c012faa0141726c00ab880d954fe2857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477608"
---
# <a name="em_charfrompos-message"></a><span data-ttu-id="b6211-105">\_Messaggio CHARFROMPOS em</span><span class="sxs-lookup"><span data-stu-id="b6211-105">EM\_CHARFROMPOS message</span></span>

<span data-ttu-id="b6211-106">Ottiene informazioni sul carattere più vicino a un punto specificato nell'area client di un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="b6211-106">Gets information about the character closest to a specified point in the client area of an edit control.</span></span> <span data-ttu-id="b6211-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b6211-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6211-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6211-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6211-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6211-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6211-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="b6211-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b6211-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6211-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6211-112">Coordinate di un punto nell'area client del controllo.</span><span class="sxs-lookup"><span data-stu-id="b6211-112">The coordinates of a point in the control's client area.</span></span> <span data-ttu-id="b6211-113">Le coordinate sono espresse in unità dello schermo e sono relative all'angolo superiore sinistro dell'area client del controllo.</span><span class="sxs-lookup"><span data-stu-id="b6211-113">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="b6211-114">**Controlli Rich Edit:** Puntatore a una struttura [**POINTL**](/previous-versions//dd162807(v=vs.85)) che contiene le coordinate orizzontali e verticali.</span><span class="sxs-lookup"><span data-stu-id="b6211-114">**Rich edit controls:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that contains the horizontal and vertical coordinates.</span></span>

<span data-ttu-id="b6211-115">**Controlli di modifica:** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene la coordinata orizzontale.</span><span class="sxs-lookup"><span data-stu-id="b6211-115">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate.</span></span> <span data-ttu-id="b6211-116">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene la coordinata verticale.</span><span class="sxs-lookup"><span data-stu-id="b6211-116">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6211-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6211-117">Return value</span></span>

<span data-ttu-id="b6211-118">**Controlli Rich Edit:** Il valore restituito specifica l'indice dei caratteri in base zero del carattere più vicino al punto specificato.</span><span class="sxs-lookup"><span data-stu-id="b6211-118">**Rich edit controls:** The return value specifies the zero-based character index of the character nearest the specified point.</span></span> <span data-ttu-id="b6211-119">Il valore restituito indica l'ultimo carattere del controllo di modifica se il punto specificato è oltre l'ultimo carattere nel controllo.</span><span class="sxs-lookup"><span data-stu-id="b6211-119">The return value indicates the last character in the edit control if the specified point is beyond the last character in the control.</span></span>

<span data-ttu-id="b6211-120">**Controlli di modifica:** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica l'indice in base zero del carattere più vicino al punto specificato.</span><span class="sxs-lookup"><span data-stu-id="b6211-120">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the character nearest the specified point.</span></span> <span data-ttu-id="b6211-121">Questo indice è relativo all'inizio del controllo, non all'inizio della riga.</span><span class="sxs-lookup"><span data-stu-id="b6211-121">This index is relative to the beginning of the control, not the beginning of the line.</span></span> <span data-ttu-id="b6211-122">Se il punto specificato è oltre l'ultimo carattere del controllo di modifica, il valore restituito indica l'ultimo carattere del controllo.</span><span class="sxs-lookup"><span data-stu-id="b6211-122">If the specified point is beyond the last character in the edit control, the return value indicates the last character in the control.</span></span> <span data-ttu-id="b6211-123">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica l'indice in base zero della riga che contiene il carattere.</span><span class="sxs-lookup"><span data-stu-id="b6211-123">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the line that contains the character.</span></span> <span data-ttu-id="b6211-124">Per i controlli di modifica a riga singola, questo valore è zero.</span><span class="sxs-lookup"><span data-stu-id="b6211-124">For single-line edit controls, this value is zero.</span></span> <span data-ttu-id="b6211-125">L'indice indica il delimitatore di riga se il punto specificato è oltre l'ultimo carattere visibile in una riga.</span><span class="sxs-lookup"><span data-stu-id="b6211-125">The index indicates the line delimiter if the specified point is beyond the last visible character in a line.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6211-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6211-126">Remarks</span></span>

<span data-ttu-id="b6211-127">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b6211-127">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="b6211-128">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="b6211-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="b6211-129">Se un punto viene passato al **\_ CHARFROMPOS em** come *lParam* e il punto si trova all'esterno dei limiti del controllo di modifica, *LRESULT* è (65535, 65535).</span><span class="sxs-lookup"><span data-stu-id="b6211-129">If a point is passed to **EM\_CHARFROMPOS** as the *lParam* and the point is outside the bounds of the edit control, then the *lResult* is (65535, 65535).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6211-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6211-130">Requirements</span></span>



| <span data-ttu-id="b6211-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6211-131">Requirement</span></span> | <span data-ttu-id="b6211-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b6211-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6211-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6211-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b6211-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6211-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b6211-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6211-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b6211-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6211-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6211-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6211-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6211-138"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6211-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6211-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6211-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6211-140">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b6211-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b6211-141">**\_POSFROMCHAR em**</span><span class="sxs-lookup"><span data-stu-id="b6211-141">**EM\_POSFROMCHAR**</span></span>](em-posfromchar.md)
</dt> <dt>

<span data-ttu-id="b6211-142">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="b6211-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b6211-143">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="b6211-143">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

<span data-ttu-id="b6211-144">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6211-144">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 

