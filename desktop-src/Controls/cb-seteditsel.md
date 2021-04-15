---
title: Messaggio CB_SETEDITSEL (winuser. h)
description: Un'applicazione invia un \_ messaggio CB SETEDITSEL per selezionare i caratteri nel controllo di modifica di una casella combinata.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- Controlli di Windows Message CB_SETEDITSEL
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54e09697e266b4e0c4260104e90f454a5e3edfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476631"
---
# <a name="cb_seteditsel-message"></a><span data-ttu-id="20cd8-104">\_Messaggio SETEDITSEL CB</span><span class="sxs-lookup"><span data-stu-id="20cd8-104">CB\_SETEDITSEL message</span></span>

<span data-ttu-id="20cd8-105">Un'applicazione invia un messaggio **CB \_ SETEDITSEL** per selezionare i caratteri nel controllo di modifica di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="20cd8-105">An application sends a **CB\_SETEDITSEL** message to select characters in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="20cd8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="20cd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20cd8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="20cd8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20cd8-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="20cd8-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="20cd8-109">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20cd8-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20cd8-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) di *lParam* specifica la posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="20cd8-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* specifies the starting position.</span></span> <span data-ttu-id="20cd8-111">Se **LOWORD** è-1, la selezione, se presente, viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="20cd8-111">If the **LOWORD** is -1, the selection, if any, is removed.</span></span>

<span data-ttu-id="20cd8-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) di *lParam* specifica la posizione finale.</span><span class="sxs-lookup"><span data-stu-id="20cd8-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of *lParam* specifies the ending position.</span></span> <span data-ttu-id="20cd8-113">Se **HIWORD** è-1, viene selezionato tutto il testo della posizione iniziale fino all'ultimo carattere del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="20cd8-113">If the **HIWORD** is -1, all text from the starting position to the last character in the edit control is selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20cd8-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20cd8-114">Return value</span></span>

<span data-ttu-id="20cd8-115">Se il messaggio ha esito positivo, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="20cd8-115">If the message succeeds, the return value is **TRUE**.</span></span> <span data-ttu-id="20cd8-116">Se il messaggio viene inviato a una casella combinata con lo stile di [**\_ DropDownList CBS**](combo-box-styles.md) , è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="20cd8-116">If the message is sent to a combo box with the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="20cd8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="20cd8-117">Remarks</span></span>

<span data-ttu-id="20cd8-118">Le posizioni sono in base zero.</span><span class="sxs-lookup"><span data-stu-id="20cd8-118">The positions are zero-based.</span></span> <span data-ttu-id="20cd8-119">Il primo carattere del controllo di modifica è nella posizione zero.</span><span class="sxs-lookup"><span data-stu-id="20cd8-119">The first character of the edit control is in the zero position.</span></span> <span data-ttu-id="20cd8-120">Il primo carattere dopo l'ultimo carattere selezionato è nella posizione finale.</span><span class="sxs-lookup"><span data-stu-id="20cd8-120">The first character after the last selected character is in the ending position.</span></span> <span data-ttu-id="20cd8-121">Per selezionare, ad esempio, i primi quattro caratteri del controllo di modifica, utilizzare una posizione iniziale pari a 0 e una posizione finale pari a 4.</span><span class="sxs-lookup"><span data-stu-id="20cd8-121">For example, to select the first four characters of the edit control, use a starting position of 0 and an ending position of 4.</span></span>

## <a name="requirements"></a><span data-ttu-id="20cd8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20cd8-122">Requirements</span></span>



| <span data-ttu-id="20cd8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="20cd8-123">Requirement</span></span> | <span data-ttu-id="20cd8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="20cd8-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20cd8-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20cd8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="20cd8-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20cd8-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="20cd8-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20cd8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="20cd8-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="20cd8-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="20cd8-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20cd8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="20cd8-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20cd8-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20cd8-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20cd8-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="20cd8-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="20cd8-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="20cd8-133">**CB \_ GETEDITSEL**</span><span class="sxs-lookup"><span data-stu-id="20cd8-133">**CB\_GETEDITSEL**</span></span>](cb-geteditsel.md)
</dt> <dt>

<span data-ttu-id="20cd8-134">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="20cd8-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="20cd8-135">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="20cd8-135">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

