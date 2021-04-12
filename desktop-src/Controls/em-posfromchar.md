---
title: Messaggio EM_POSFROMCHAR (winuser. h)
description: Recupera le coordinate dell'area client di un carattere specificato in un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- Controlli di Windows Message EM_POSFROMCHAR
topic_type:
- apiref
api_name:
- EM_POSFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d98968873ad006b2e91cf3add2429bf7630fae1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517980"
---
# <a name="em_posfromchar-message"></a><span data-ttu-id="03ef7-105">\_Messaggio POSFROMCHAR em</span><span class="sxs-lookup"><span data-stu-id="03ef7-105">EM\_POSFROMCHAR message</span></span>

<span data-ttu-id="03ef7-106">Recupera le coordinate dell'area client di un carattere specificato in un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="03ef7-106">Retrieves the client area coordinates of a specified character in an edit control.</span></span> <span data-ttu-id="03ef7-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="03ef7-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="03ef7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="03ef7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03ef7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03ef7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03ef7-110">**Rich Edit 1,0 e 3,0:** Puntatore a una struttura [**POINTL**](/previous-versions//dd162807(v=vs.85)) che riceve le coordinate dell'area client del carattere.</span><span class="sxs-lookup"><span data-stu-id="03ef7-110">**Rich Edit 1.0 and 3.0:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that receives the client area coordinates of the character.</span></span> <span data-ttu-id="03ef7-111">Le coordinate sono espresse in unità dello schermo e sono relative all'angolo superiore sinistro dell'area client del controllo.</span><span class="sxs-lookup"><span data-stu-id="03ef7-111">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="03ef7-112">**Modificare i controlli e rich edit 2,0:** Indice in base zero del carattere.</span><span class="sxs-lookup"><span data-stu-id="03ef7-112">**Edit controls and Rich Edit 2.0:** The zero-based index of the character.</span></span>

</dd> <dt>

<span data-ttu-id="03ef7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03ef7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03ef7-114">**Rich Edit 1,0 e 3,0:** Indice in base zero del carattere.</span><span class="sxs-lookup"><span data-stu-id="03ef7-114">**Rich Edit 1.0 and 3.0:** The zero-based index of the character.</span></span>

<span data-ttu-id="03ef7-115">**Modificare i controlli e rich edit 2,0:** Questo parametro non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="03ef7-115">**Edit controls and Rich Edit 2.0:** This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03ef7-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03ef7-116">Return value</span></span>

<span data-ttu-id="03ef7-117">**Rich Edit 1,0 e 3,0:** Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="03ef7-117">**Rich Edit 1.0 and 3.0:** The return value is not used.</span></span>

<span data-ttu-id="03ef7-118">**Modificare i controlli e rich edit 2,0:** Il valore restituito contiene le coordinate dell'area client del carattere.</span><span class="sxs-lookup"><span data-stu-id="03ef7-118">**Edit controls and Rich Edit 2.0:** The return value contains the client area coordinates of the character.</span></span> <span data-ttu-id="03ef7-119">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene la coordinata orizzontale e il [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene la coordinata verticale.</span><span class="sxs-lookup"><span data-stu-id="03ef7-119">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

## <a name="remarks"></a><span data-ttu-id="03ef7-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="03ef7-120">Remarks</span></span>

<span data-ttu-id="03ef7-121">Una coordinata restituita può essere un valore negativo se il carattere specificato non viene visualizzato nell'area client del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="03ef7-121">A returned coordinate can be a negative value if the specified character is not displayed in the edit control's client area.</span></span> <span data-ttu-id="03ef7-122">Le coordinate vengono troncate in base ai valori integer.</span><span class="sxs-lookup"><span data-stu-id="03ef7-122">The coordinates are truncated to integer values.</span></span>

<span data-ttu-id="03ef7-123">Se il carattere è un delimitatore di riga, le coordinate restituite indicano un punto appena oltre l'ultimo carattere visibile nella riga.</span><span class="sxs-lookup"><span data-stu-id="03ef7-123">If the character is a line delimiter, the returned coordinates indicate a point just beyond the last visible character in the line.</span></span> <span data-ttu-id="03ef7-124">Se l'indice specificato è maggiore dell'indice dell'ultimo carattere del controllo, il controllo restituisce-1.</span><span class="sxs-lookup"><span data-stu-id="03ef7-124">If the specified index is greater than the index of the last character in the control, the control returns -1.</span></span>

<span data-ttu-id="03ef7-125">**Rich Edit 3,0 e versioni successive:** Per compatibilità con le versioni precedenti, Microsoft Rich Edit 3,0 supporta la sintassi utilizzata da Microsoft Rich Edit 2,0.</span><span class="sxs-lookup"><span data-stu-id="03ef7-125">**Rich Edit 3.0 and later:** For backward compatibility, Microsoft Rich Edit 3.0 supports the syntax used by Microsoft Rich Edit 2.0.</span></span> <span data-ttu-id="03ef7-126">Se Microsoft Rich Edit 3,0 rileva che *wParam* non è un puntatore [**punto**](/previous-versions//dd162807(v=vs.85)) valido, presuppone che il messaggio sia stato inviato utilizzando la sintassi Microsoft Rich Edit 2,0.</span><span class="sxs-lookup"><span data-stu-id="03ef7-126">If Microsoft Rich Edit 3.0 detects that *wParam* is not a valid [**POINTL**](/previous-versions//dd162807(v=vs.85)) pointer, it assumes the message was sent using the Microsoft Rich Edit 2.0 syntax.</span></span> <span data-ttu-id="03ef7-127">In questo caso, usa il valore restituito per restituire le coordinate.</span><span class="sxs-lookup"><span data-stu-id="03ef7-127">In this case, it uses the return value to return the coordinates.</span></span>

<span data-ttu-id="03ef7-128">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="03ef7-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="03ef7-129">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="03ef7-129">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03ef7-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03ef7-130">Requirements</span></span>



| <span data-ttu-id="03ef7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="03ef7-131">Requirement</span></span> | <span data-ttu-id="03ef7-132">Valore</span><span class="sxs-lookup"><span data-stu-id="03ef7-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ef7-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03ef7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="03ef7-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03ef7-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="03ef7-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03ef7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="03ef7-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="03ef7-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="03ef7-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03ef7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="03ef7-138"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03ef7-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03ef7-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03ef7-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="03ef7-140">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="03ef7-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="03ef7-141">**\_CHARFROMPOS em**</span><span class="sxs-lookup"><span data-stu-id="03ef7-141">**EM\_CHARFROMPOS**</span></span>](em-charfrompos.md)
</dt> <dt>

<span data-ttu-id="03ef7-142">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="03ef7-142">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="03ef7-143">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="03ef7-143">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 

