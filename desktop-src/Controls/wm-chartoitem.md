---
title: Messaggio WM_CHARTOITEM (winuser. h)
description: Inviato da una casella di riepilogo con lo \_ stile WANTKEYBOARDINPUT lbs al relativo proprietario in risposta a un \_ messaggio WM Char.
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- Controlli di Windows Message WM_CHARTOITEM
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9df55dcf9f507cb57e91fe0214eab94c53f22
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353916"
---
# <a name="wm_chartoitem-message"></a><span data-ttu-id="19bcf-104">\_Messaggio CHARTOITEM WM</span><span class="sxs-lookup"><span data-stu-id="19bcf-104">WM\_CHARTOITEM message</span></span>

<span data-ttu-id="19bcf-105">Inviato da una casella di riepilogo con lo stile [**\_ WANTKEYBOARDINPUT lbs**](list-box-styles.md) al relativo proprietario in risposta a un messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="19bcf-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="19bcf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="19bcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19bcf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19bcf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19bcf-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il codice carattere della chiave che l'utente ha premuto.</span><span class="sxs-lookup"><span data-stu-id="19bcf-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the character code of the key the user pressed.</span></span> <span data-ttu-id="19bcf-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione corrente del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="19bcf-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="19bcf-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19bcf-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19bcf-111">Handle per la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="19bcf-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19bcf-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19bcf-112">Return value</span></span>

<span data-ttu-id="19bcf-113">Il valore restituito specifica l'azione eseguita dall'applicazione in risposta al messaggio.</span><span class="sxs-lookup"><span data-stu-id="19bcf-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="19bcf-114">Il valore restituito-1 o-2 indica che l'applicazione ha gestito tutti gli aspetti della selezione dell'elemento e non richiede ulteriori azioni da parte della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="19bcf-114">A return value of -1 or -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="19bcf-115">Un valore restituito pari a 0 o superiore specifica l'indice in base zero di un elemento nella casella di riepilogo e indica che la casella di riepilogo deve eseguire l'azione predefinita per la sequenza di tasti sull'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="19bcf-115">A return value of 0 or greater specifies the zero-based index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="19bcf-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="19bcf-116">Remarks</span></span>

<span data-ttu-id="19bcf-117">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce-1.</span><span class="sxs-lookup"><span data-stu-id="19bcf-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="19bcf-118">Solo le caselle di riepilogo create dal proprietario che non hanno lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) possono ricevere questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="19bcf-118">Only owner-drawn list boxes that do not have the [**LBS\_HASSTRINGS**](list-box-styles.md) style can receive this message.</span></span>

<span data-ttu-id="19bcf-119">Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **bool** e restituire direttamente il valore.</span><span class="sxs-lookup"><span data-stu-id="19bcf-119">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="19bcf-120">Il valore *DWL \_ MSGRESULT* impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="19bcf-120">The *DWL\_MSGRESULT* value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="19bcf-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19bcf-121">Requirements</span></span>



| <span data-ttu-id="19bcf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="19bcf-122">Requirement</span></span> | <span data-ttu-id="19bcf-123">Valore</span><span class="sxs-lookup"><span data-stu-id="19bcf-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19bcf-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19bcf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="19bcf-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19bcf-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="19bcf-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19bcf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="19bcf-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19bcf-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="19bcf-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19bcf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="19bcf-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19bcf-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19bcf-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19bcf-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="19bcf-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="19bcf-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="19bcf-132">**\_VKEYTOITEM WM**</span><span class="sxs-lookup"><span data-stu-id="19bcf-132">**WM\_VKEYTOITEM**</span></span>](wm-vkeytoitem.md)
</dt> <dt>

<span data-ttu-id="19bcf-133">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="19bcf-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="19bcf-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="19bcf-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="19bcf-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="19bcf-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="19bcf-136">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="19bcf-136">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="19bcf-137">**\_carattere WM**</span><span class="sxs-lookup"><span data-stu-id="19bcf-137">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

