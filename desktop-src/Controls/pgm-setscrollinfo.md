---
title: Messaggio PGM_SETSCROLLINFO (COMmctrl. h)
description: Imposta i parametri di scorrimento del controllo pager, inclusi il valore di timeout, le righe per ogni timeout e i pixel per riga. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro SetScrollInfo di cercapersone.
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- Controlli di Windows Message PGM_SETSCROLLINFO
topic_type:
- apiref
api_name:
- PGM_SETSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8fc230e1a12968d0eb29f8ba512848df42b64b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873654"
---
# <a name="pgm_setscrollinfo-message"></a><span data-ttu-id="838d2-105">\_Messaggio SETSCROLLINFO PGM</span><span class="sxs-lookup"><span data-stu-id="838d2-105">PGM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="838d2-106">\[Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="838d2-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="838d2-107">Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="838d2-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="838d2-108">Imposta i parametri di scorrimento del controllo pager, inclusi il valore di timeout, le righe per ogni timeout e i pixel per riga.</span><span class="sxs-lookup"><span data-stu-id="838d2-108">Sets the scrolling parameters of the pager control, including the timeout value, the lines per timeout, and the pixels per line.</span></span> <span data-ttu-id="838d2-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ SetScrollInfo di cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="838d2-109">You can send this message explicitly or by using the [**Pager\_SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="838d2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="838d2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="838d2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="838d2-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="838d2-112">**Uint** che specifica il valore di timeout per lo scorrimento, espresso in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="838d2-112">A **UINT** that specifies the timeout value for the scroll, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="838d2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="838d2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="838d2-114">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un **uint** che specifica il numero di righe da scorrere per ogni timeout.</span><span class="sxs-lookup"><span data-stu-id="838d2-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **UINT** that specifies the number of lines to scroll per timeout.</span></span> <span data-ttu-id="838d2-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è un **uint** che specifica il numero di pixel per riga.</span><span class="sxs-lookup"><span data-stu-id="838d2-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **UINT** that specifies the number of pixels per line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="838d2-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="838d2-116">Return value</span></span>

<span data-ttu-id="838d2-117">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="838d2-117">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="838d2-118">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="838d2-118">Security Considerations</span></span>

<span data-ttu-id="838d2-119">L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="838d2-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="838d2-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="838d2-120">Remarks</span></span>

<span data-ttu-id="838d2-121">Il valore di timeout *wParam* controlla la velocità con cui il controllo pager genera gli eventi di scorrimento quando il controllo ha acquisito l'input del mouse e viene premuto il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="838d2-121">The *wParam* timeout value controls the rate at which the pager control generates scrolling events when the control has captured the mouse input and the left mouse button is pressed.</span></span> <span data-ttu-id="838d2-122">I valori più piccoli generano uno scorrimento più veloce; i valori maggiori comportano uno scorrimento più lento.</span><span class="sxs-lookup"><span data-stu-id="838d2-122">Smaller values result in faster scrolling; larger values result in slower scrolling.</span></span> <span data-ttu-id="838d2-123">Il valore predefinito è un ottavo dell'ora di doppio clic.</span><span class="sxs-lookup"><span data-stu-id="838d2-123">The default value is one-eighth of the double-click time.</span></span> <span data-ttu-id="838d2-124">Per ulteriori informazioni, vedere [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).</span><span class="sxs-lookup"><span data-stu-id="838d2-124">For more information, see [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).</span></span>

<span data-ttu-id="838d2-125">Per impostazione predefinita, con ogni evento di scorrimento il controllo pager scorre una quantità uguale all'intera larghezza o altezza del controllo, a seconda che il controllo pager abbia un orientamento orizzontale o verticale.</span><span class="sxs-lookup"><span data-stu-id="838d2-125">By default, with each scrolling event the pager control scrolls an amount equal to the entire width or height of the control, depending on whether the pager control has a horizontal or vertical orientation.</span></span> <span data-ttu-id="838d2-126">I valori in *lParam* vengono utilizzati per eseguire l'override della quantità predefinita di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="838d2-126">The values in *lParam* are used to override the default scrolling amount.</span></span> <span data-ttu-id="838d2-127">Se vengono specificati valori diversi da zero, la quantità di scorrimento è il prodotto dei due valori (LOWORD (*lParam*) \* HIWORD (*lParam*)).</span><span class="sxs-lookup"><span data-stu-id="838d2-127">If nonzero values are provided, the scrolling amount is the product of the two values (LOWORD(*lParam*) \* HIWORD(*lParam*)).</span></span>

## <a name="requirements"></a><span data-ttu-id="838d2-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="838d2-128">Requirements</span></span>



| <span data-ttu-id="838d2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="838d2-129">Requirement</span></span> | <span data-ttu-id="838d2-130">Valore</span><span class="sxs-lookup"><span data-stu-id="838d2-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="838d2-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="838d2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="838d2-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="838d2-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="838d2-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="838d2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="838d2-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="838d2-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="838d2-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="838d2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="838d2-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="838d2-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="838d2-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="838d2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="838d2-138">**Cercapersone \_ SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="838d2-138">**Pager\_SetScrollInfo**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

