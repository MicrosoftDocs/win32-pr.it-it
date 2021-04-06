---
title: Messaggio BM_GETSTATE (winuser. h)
description: Recupera lo stato di un pulsante o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o usare il pulsante \_ GetState macro.
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- Controlli di Windows Message BM_GETSTATE
topic_type:
- apiref
api_name:
- BM_GETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b5e69f067acfc13cd8661be8a585fcfc8e6fe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963813"
---
# <a name="bm_getstate-message"></a><span data-ttu-id="46a06-105">\_Messaggio BM GETstate</span><span class="sxs-lookup"><span data-stu-id="46a06-105">BM\_GETSTATE message</span></span>

<span data-ttu-id="46a06-106">Recupera lo stato di un pulsante o di una casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="46a06-106">Retrieves the state of a button or check box.</span></span> <span data-ttu-id="46a06-107">È possibile inviare questo messaggio in modo esplicito o usare il [**pulsante \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) macro.</span><span class="sxs-lookup"><span data-stu-id="46a06-107">You can send this message explicitly or use the [**Button\_GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="46a06-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46a06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46a06-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46a06-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46a06-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="46a06-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="46a06-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46a06-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46a06-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="46a06-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46a06-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46a06-113">Return value</span></span>

<span data-ttu-id="46a06-114">Il valore restituito specifica lo stato corrente del pulsante.</span><span class="sxs-lookup"><span data-stu-id="46a06-114">The return value specifies the current state of the button.</span></span> <span data-ttu-id="46a06-115">Si tratta di una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="46a06-115">It is a combination of the following values.</span></span>



| <span data-ttu-id="46a06-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="46a06-116">Return code</span></span>                                                                                        | <span data-ttu-id="46a06-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46a06-117">Description</span></span>                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="46a06-118"><dt>**\_controllo BST**</dt></span><span class="sxs-lookup"><span data-stu-id="46a06-118"><dt>**BST\_CHECKED**</dt></span></span> </dl>        | <span data-ttu-id="46a06-119">Il pulsante è selezionato.</span><span class="sxs-lookup"><span data-stu-id="46a06-119">The button is checked.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="46a06-120"><dt>**\_DROPDOWNPUSHED BST**</dt></span><span class="sxs-lookup"><span data-stu-id="46a06-120"><dt>**BST\_DROPDOWNPUSHED**</dt></span></span> </dl> | <span data-ttu-id="46a06-121">[Windows Vista](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="46a06-121">[Windows Vista](common-control-versions.md).</span></span> <span data-ttu-id="46a06-122">Il pulsante si trova nello stato a discesa.</span><span class="sxs-lookup"><span data-stu-id="46a06-122">The button is in the drop-down state.</span></span> <span data-ttu-id="46a06-123">Si applica solo se il pulsante ha lo stile a [**\_ discesa TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="46a06-123">Applies only if the button has the [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span><br/> |
| <dl> <span data-ttu-id="46a06-124"><dt>**\_stato attivo BST**</dt></span><span class="sxs-lookup"><span data-stu-id="46a06-124"><dt>**BST\_FOCUS**</dt></span></span> </dl>          | <span data-ttu-id="46a06-125">Il pulsante ha lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="46a06-125">The button has the keyboard focus.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="46a06-126"><dt>**BST \_ attivo**</dt></span><span class="sxs-lookup"><span data-stu-id="46a06-126"><dt>**BST\_HOT**</dt></span></span> </dl>            | <span data-ttu-id="46a06-127">Il pulsante è attivo; ovvero il puntatore del mouse viene spostato su di esso.</span><span class="sxs-lookup"><span data-stu-id="46a06-127">The button is hot; that is, the mouse is hovering over it.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="46a06-128"><dt>**BST \_ INdeterminato**</dt></span><span class="sxs-lookup"><span data-stu-id="46a06-128"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl>  | <span data-ttu-id="46a06-129">Lo stato del pulsante è indeterminato.</span><span class="sxs-lookup"><span data-stu-id="46a06-129">The state of the button is indeterminate.</span></span> <span data-ttu-id="46a06-130">Si applica solo se il pulsante ha lo stile [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="46a06-130">Applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/>                    |
| <dl> <span data-ttu-id="46a06-131"><dt>**BST \_ push**</dt></span><span class="sxs-lookup"><span data-stu-id="46a06-131"><dt>**BST\_PUSHED**</dt></span></span> </dl>         | <span data-ttu-id="46a06-132">Il pulsante viene visualizzato nello stato push.</span><span class="sxs-lookup"><span data-stu-id="46a06-132">The button is being shown in the pushed state.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="46a06-133"><dt>**BST \_ DEselezionata**</dt></span><span class="sxs-lookup"><span data-stu-id="46a06-133"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>      | <span data-ttu-id="46a06-134">Nessuno stato speciale.</span><span class="sxs-lookup"><span data-stu-id="46a06-134">No special state.</span></span> <span data-ttu-id="46a06-135">Equivalente a zero.</span><span class="sxs-lookup"><span data-stu-id="46a06-135">Equivalent to zero.</span></span><br/>                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="46a06-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46a06-136">Requirements</span></span>



| <span data-ttu-id="46a06-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="46a06-137">Requirement</span></span> | <span data-ttu-id="46a06-138">Valore</span><span class="sxs-lookup"><span data-stu-id="46a06-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46a06-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46a06-139">Minimum supported client</span></span><br/> | <span data-ttu-id="46a06-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46a06-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="46a06-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46a06-141">Minimum supported server</span></span><br/> | <span data-ttu-id="46a06-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="46a06-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="46a06-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46a06-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="46a06-144"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46a06-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46a06-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46a06-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="46a06-146">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="46a06-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="46a06-147">**GetCheck BM \_**</span><span class="sxs-lookup"><span data-stu-id="46a06-147">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="46a06-148">**STATO di BM \_**</span><span class="sxs-lookup"><span data-stu-id="46a06-148">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





