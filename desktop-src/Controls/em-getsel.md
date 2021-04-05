---
title: Messaggio EM_GETSEL (winuser. h)
description: Ottiene le posizioni dei caratteri iniziali e finali (in TCHARs) della selezione corrente in un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- Controlli di Windows Message EM_GETSEL
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28ba97c9043866c3e97c1c51389447498562455
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048304"
---
# <a name="em_getsel-message"></a><span data-ttu-id="4a945-105">\_Messaggio GETSEL em</span><span class="sxs-lookup"><span data-stu-id="4a945-105">EM\_GETSEL message</span></span>

<span data-ttu-id="4a945-106">Ottiene le posizioni dei caratteri iniziali e finali (in **TCHAR** s) della selezione corrente in un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="4a945-106">Gets the starting and ending character positions (in **TCHAR** s) of the current selection in an edit control.</span></span> <span data-ttu-id="4a945-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4a945-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a945-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a945-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a945-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a945-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a945-110">Puntatore a un valore **DWORD** che riceve la posizione iniziale della selezione.</span><span class="sxs-lookup"><span data-stu-id="4a945-110">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="4a945-111">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4a945-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4a945-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a945-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a945-113">Puntatore a un valore **DWORD** che riceve la posizione del primo carattere non selezionato dopo la fine della selezione.</span><span class="sxs-lookup"><span data-stu-id="4a945-113">A pointer to a **DWORD** value that receives the position of the first unselected character after the end of the selection.</span></span> <span data-ttu-id="4a945-114">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4a945-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a945-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a945-115">Return value</span></span>

<span data-ttu-id="4a945-116">Il valore restituito è un valore in base zero con la posizione iniziale della selezione in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e la posizione del primo **TCHAR** dopo l'ultimo **TCHAR** selezionato in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4a945-116">The return value is a zero-based value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the position of the first **TCHAR** after the last selected **TCHAR** in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="4a945-117">Se uno di questi valori supera 65.535, il valore restituito è-1.</span><span class="sxs-lookup"><span data-stu-id="4a945-117">If either of these values exceeds 65,535, the return value is -1.</span></span>

<span data-ttu-id="4a945-118">È preferibile usare i valori restituiti in *wParam* e *lParam* perché sono valori a 32 bit completi.</span><span class="sxs-lookup"><span data-stu-id="4a945-118">It is better to use the values returned in *wParam* and *lParam* because they are full 32-bit values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a945-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a945-119">Remarks</span></span>

<span data-ttu-id="4a945-120">Se non è presente alcuna selezione, i valori iniziale e finale sono entrambi la posizione del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="4a945-120">If there is no selection, the starting and ending values are both the position of the caret.</span></span>

<span data-ttu-id="4a945-121">**Controlli Rich Edit:** È anche possibile usare il [**messaggio \_ EXGETSEL em**](em-exgetsel.md) per recuperare le stesse informazioni.</span><span class="sxs-lookup"><span data-stu-id="4a945-121">**Rich edit controls:** You can also use the [**EM\_EXGETSEL**](em-exgetsel.md) message to retrieve the same information.</span></span> <span data-ttu-id="4a945-122">**Em \_ EXGETSEL** restituisce anche le posizioni dei caratteri iniziale e finale come valori a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4a945-122">**EM\_EXGETSEL** also returns starting and ending character positions as 32-bit values.</span></span>

<span data-ttu-id="4a945-123">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4a945-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="4a945-124">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="4a945-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a945-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a945-125">Requirements</span></span>



| <span data-ttu-id="4a945-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a945-126">Requirement</span></span> | <span data-ttu-id="4a945-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4a945-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a945-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a945-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4a945-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a945-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4a945-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a945-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4a945-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4a945-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4a945-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a945-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a945-133"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a945-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a945-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a945-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="4a945-135">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4a945-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4a945-136">**\_EXGETSEL em**</span><span class="sxs-lookup"><span data-stu-id="4a945-136">**EM\_EXGETSEL**</span></span>](em-exgetsel.md)
</dt> <dt>

[<span data-ttu-id="4a945-137">**\_SETSEL em**</span><span class="sxs-lookup"><span data-stu-id="4a945-137">**EM\_SETSEL**</span></span>](em-setsel.md)
</dt> </dl>

 

