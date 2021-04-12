---
title: Messaggio WM_VKEYTOITEM (winuser. h)
description: Inviato da una casella di riepilogo con lo \_ stile WANTKEYBOARDINPUT di lbs al suo proprietario in risposta a un messaggio del KeyDown di WM \_ .
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- Controlli di Windows Message WM_VKEYTOITEM
topic_type:
- apiref
api_name:
- WM_VKEYTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1685682d8305fff5d9d93ef59d8859e099e6ce
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "104351731"
---
# <a name="wm_vkeytoitem-message"></a><span data-ttu-id="0a129-104">\_Messaggio VKEYTOITEM WM</span><span class="sxs-lookup"><span data-stu-id="0a129-104">WM\_VKEYTOITEM message</span></span>

<span data-ttu-id="0a129-105">Inviato da una casella di riepilogo con lo stile [**\_ WANTKEYBOARDINPUT di lbs**](list-box-styles.md) al suo proprietario in risposta a un messaggio del [**\_ KeyDown di WM**](/windows/desktop/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="0a129-105">Sent by a list box with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style to its owner in response to a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span>


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0a129-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a129-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a129-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a129-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a129-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il codice della chiave virtuale della chiave che l'utente ha premuto.</span><span class="sxs-lookup"><span data-stu-id="0a129-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the virtual-key code of the key the user pressed.</span></span> <span data-ttu-id="0a129-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione corrente del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="0a129-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="0a129-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a129-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a129-111">Handle per la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="0a129-111">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a129-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a129-112">Return value</span></span>

<span data-ttu-id="0a129-113">Il valore restituito specifica l'azione eseguita dall'applicazione in risposta al messaggio.</span><span class="sxs-lookup"><span data-stu-id="0a129-113">The return value specifies the action that the application performed in response to the message.</span></span> <span data-ttu-id="0a129-114">Un valore restituito pari a-2 indica che l'applicazione ha gestito tutti gli aspetti della selezione dell'elemento e non richiede ulteriori azioni da parte della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="0a129-114">A return value of -2 indicates that the application handled all aspects of selecting the item and requires no further action by the list box.</span></span> <span data-ttu-id="0a129-115">(Vedere la sezione Osservazioni). Un valore restituito-1 indica che la casella di riepilogo deve eseguire l'azione predefinita in risposta alla sequenza di tasti.</span><span class="sxs-lookup"><span data-stu-id="0a129-115">(See Remarks.) A return value of -1 indicates that the list box should perform the default action in response to the keystroke.</span></span> <span data-ttu-id="0a129-116">Un valore restituito pari a 0 o superiore specifica l'indice di un elemento nella casella di riepilogo e indica che la casella di riepilogo deve eseguire l'azione predefinita per la sequenza di tasti sull'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="0a129-116">A return value of 0 or greater specifies the index of an item in the list box and indicates that the list box should perform the default action for the keystroke on the specified item.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a129-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a129-117">Remarks</span></span>

<span data-ttu-id="0a129-118">Un valore restituito di-2 è valido solo per le chiavi non convertite in caratteri dal controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="0a129-118">A return value of -2 is valid only for keys that are not translated into characters by the list box control.</span></span> <span data-ttu-id="0a129-119">Se il messaggio [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) viene convertito in un messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) e l'applicazione elabora il messaggio **WM \_ VKEYTOITEM** generato come risultato della pressione della chiave, la casella di riepilogo ignora il valore restituito ed esegue l'elaborazione predefinita per tale carattere.</span><span class="sxs-lookup"><span data-stu-id="0a129-119">If the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message translates to a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message and the application processes the **WM\_VKEYTOITEM** message generated as a result of the key press, the list box ignores the return value and does the default processing for that character).</span></span> <span data-ttu-id="0a129-120">**WM \_** I messaggi KeyDown generati da chiavi quali VK \_ up, VK \_ Down, VK \_ Next e VK \_ Previous non vengono convertiti in messaggi **WM \_ char** .</span><span class="sxs-lookup"><span data-stu-id="0a129-120">**WM\_KEYDOWN** messages generated by keys such as VK\_UP, VK\_DOWN, VK\_NEXT, and VK\_PREVIOUS are not translated to **WM\_CHAR** messages.</span></span> <span data-ttu-id="0a129-121">In questi casi, l'intercettazione del messaggio **WM \_ VKEYTOITEM** e la restituzione di-2 impedisce alla casella di riepilogo di eseguire l'elaborazione predefinita per tale chiave.</span><span class="sxs-lookup"><span data-stu-id="0a129-121">In such cases, trapping the **WM\_VKEYTOITEM** message and returning -2 prevents the list box from doing the default processing for that key.</span></span>

<span data-ttu-id="0a129-122">Per intercettare le chiavi che generano un messaggio char ed eseguire un'elaborazione speciale, l'applicazione deve sottocreare una sottoclasse della casella di riepilogo, intercettare i messaggi [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) e [**WM \_ char**](/windows/desktop/inputdev/wm-char) ed elaborare i messaggi in modo appropriato nella procedura di sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="0a129-122">To trap keys that generate a char message and do special processing, the application must subclass the list box, trap both the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) and [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages, and process the messages appropriately in the subclass procedure.</span></span>

<span data-ttu-id="0a129-123">Le osservazioni precedenti si applicano alle caselle di riepilogo normali create con lo stile [**\_ WANTKEYBOARDINPUT di lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0a129-123">The preceding remarks apply to regular list boxes that are created with the [**LBS\_WANTKEYBOARDINPUT**](list-box-styles.md) style.</span></span> <span data-ttu-id="0a129-124">Se la casella di riepilogo è disegnata dal proprietario, l'applicazione deve elaborare il messaggio [**WM \_ CHARTOITEM**](wm-chartoitem.md) .</span><span class="sxs-lookup"><span data-stu-id="0a129-124">If the list box is owner-drawn, the application must process the [**WM\_CHARTOITEM**](wm-chartoitem.md) message.</span></span>

<span data-ttu-id="0a129-125">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce-1.</span><span class="sxs-lookup"><span data-stu-id="0a129-125">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns -1.</span></span>

<span data-ttu-id="0a129-126">Se una routine della finestra di dialogo gestisce questo messaggio, deve eseguire il cast del valore restituito desiderato a un **bool** e restituire direttamente il valore.</span><span class="sxs-lookup"><span data-stu-id="0a129-126">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="0a129-127">Il \_ valore DWL MSGRESULT impostato dalla funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="0a129-127">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a129-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a129-128">Requirements</span></span>



| <span data-ttu-id="0a129-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a129-129">Requirement</span></span> | <span data-ttu-id="0a129-130">Valore</span><span class="sxs-lookup"><span data-stu-id="0a129-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a129-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a129-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0a129-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a129-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0a129-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a129-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0a129-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0a129-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0a129-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a129-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a129-136"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a129-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a129-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a129-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="0a129-138">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="0a129-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0a129-139">**\_CHARTOITEM WM**</span><span class="sxs-lookup"><span data-stu-id="0a129-139">**WM\_CHARTOITEM**</span></span>](wm-chartoitem.md)
</dt> <dt>

<span data-ttu-id="0a129-140">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="0a129-140">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="0a129-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0a129-141">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0a129-142">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0a129-142">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0a129-143">**KeyDown di WM \_**</span><span class="sxs-lookup"><span data-stu-id="0a129-143">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

