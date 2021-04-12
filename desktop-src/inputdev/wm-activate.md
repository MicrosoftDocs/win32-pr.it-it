---
title: Messaggio WM_ACTIVATE (winuser. h)
description: Inviato sia alla finestra attivata che alla finestra da disattivare.
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- Input della tastiera e del mouse WM_ACTIVATE messaggio
topic_type:
- apiref
api_name:
- WM_ACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec28662aa2219ee9b3ad2e8cc8efac861d292f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119514"
---
# <a name="wm_activate-message"></a><span data-ttu-id="a3ddf-104">\_Messaggio di attivazione WM</span><span class="sxs-lookup"><span data-stu-id="a3ddf-104">WM\_ACTIVATE message</span></span>

<span data-ttu-id="a3ddf-105">Inviato sia alla finestra attivata che alla finestra da disattivare.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-105">Sent to both the window being activated and the window being deactivated.</span></span> <span data-ttu-id="a3ddf-106">Se le finestre utilizzano la stessa coda di input, il messaggio viene inviato in modo sincrono, prima alla routine della finestra della finestra di primo livello da disattivare, quindi alla routine della finestra della finestra di primo livello attivata.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-106">If the windows use the same input queue, the message is sent synchronously, first to the window procedure of the top-level window being deactivated, then to the window procedure of the top-level window being activated.</span></span> <span data-ttu-id="a3ddf-107">Se le finestre utilizzano code di input diverse, il messaggio viene inviato in modo asincrono, quindi la finestra viene attivata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-107">If the windows use different input queues, the message is sent asynchronously, so the window is activated immediately.</span></span>


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a><span data-ttu-id="a3ddf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3ddf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3ddf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3ddf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3ddf-110">La parola di ordine inferiore specifica se la finestra viene attivata o disattivata.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-110">The low-order word specifies whether the window is being activated or deactivated.</span></span> <span data-ttu-id="a3ddf-111">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="a3ddf-112">La parola più ordinata specifica lo stato ridotto a icona della finestra attivata o disattivata.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-112">The high-order word specifies the minimized state of the window being activated or deactivated.</span></span> <span data-ttu-id="a3ddf-113">Un valore diverso da zero indica che la finestra è ridotta A icona.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-113">A nonzero value indicates the window is minimized.</span></span>



| <span data-ttu-id="a3ddf-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a3ddf-114">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="a3ddf-115">Significato</span><span class="sxs-lookup"><span data-stu-id="a3ddf-115">Meaning</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <span data-ttu-id="a3ddf-116"><dt>**WA \_ ATTIVO**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a3ddf-116"><dt>**WA\_ACTIVE**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="a3ddf-117">Attivato da un metodo diverso da un clic del mouse, ad esempio tramite una chiamata alla funzione [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) o usando l'interfaccia della tastiera per selezionare la finestra.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-117">Activated by some method other than a mouse click (for example, by a call to the [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) function or by use of the keyboard interface to select the window).</span></span><br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <span data-ttu-id="a3ddf-118"><dt>**WA \_ CLICKACTIVE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a3ddf-118"><dt>**WA\_CLICKACTIVE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="a3ddf-119">Attivato con un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-119">Activated by a mouse click.</span></span><br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <span data-ttu-id="a3ddf-120"><dt>**WA \_ Inattivo**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a3ddf-120"><dt>**WA\_INACTIVE**</dt> <dt>0</dt></span></span> </dl>          | <span data-ttu-id="a3ddf-121">Disattivato.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-121">Deactivated.</span></span><br/>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="a3ddf-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3ddf-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3ddf-123">Handle per la finestra da attivare o disattivare, a seconda del valore del parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="a3ddf-123">A handle to the window being activated or deactivated, depending on the value of the *wParam* parameter.</span></span> <span data-ttu-id="a3ddf-124">Se la parola più bassa di *wParam* è **WA \_ inactive**, *lParam* è l'handle per la finestra attivata.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-124">If the low-order word of *wParam* is **WA\_INACTIVE**, *lParam* is the handle to the window being activated.</span></span> <span data-ttu-id="a3ddf-125">Se la parola più bassa di *wParam* è **WA \_ Active** o **WA \_ CLICKACTIVE**, *lParam* è l'handle per la finestra da disattivare.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-125">If the low-order word of *wParam* is **WA\_ACTIVE** or **WA\_CLICKACTIVE**, *lParam* is the handle to the window being deactivated.</span></span> <span data-ttu-id="a3ddf-126">Questo handle può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-126">This handle can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3ddf-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3ddf-127">Return value</span></span>

<span data-ttu-id="a3ddf-128">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-128">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3ddf-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3ddf-129">Remarks</span></span>

<span data-ttu-id="a3ddf-130">Se la finestra viene attivata e non è ridotta a icona, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) imposta lo stato attivo della tastiera sulla finestra.</span><span class="sxs-lookup"><span data-stu-id="a3ddf-130">If the window is being activated and is not minimized, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets the keyboard focus to the window.</span></span> <span data-ttu-id="a3ddf-131">Se la finestra viene attivata con un clic del mouse, riceve anche un messaggio [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md) .</span><span class="sxs-lookup"><span data-stu-id="a3ddf-131">If the window is activated by a mouse click, it also receives a [**WM\_MOUSEACTIVATE**](wm-mouseactivate.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3ddf-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3ddf-132">Requirements</span></span>



| <span data-ttu-id="a3ddf-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3ddf-133">Requirement</span></span> | <span data-ttu-id="a3ddf-134">Valore</span><span class="sxs-lookup"><span data-stu-id="a3ddf-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3ddf-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3ddf-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a3ddf-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3ddf-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a3ddf-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3ddf-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a3ddf-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3ddf-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a3ddf-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3ddf-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3ddf-140"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3ddf-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3ddf-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3ddf-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="a3ddf-142">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a3ddf-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a3ddf-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="a3ddf-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="a3ddf-144">**SetActiveWindow**</span><span class="sxs-lookup"><span data-stu-id="a3ddf-144">**SetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[<span data-ttu-id="a3ddf-145">**\_MOUSEACTIVATE WM**</span><span class="sxs-lookup"><span data-stu-id="a3ddf-145">**WM\_MOUSEACTIVATE**</span></span>](wm-mouseactivate.md)
</dt> <dt>

[<span data-ttu-id="a3ddf-146">**\_NCACTIVATE WM**</span><span class="sxs-lookup"><span data-stu-id="a3ddf-146">**WM\_NCACTIVATE**</span></span>](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

<span data-ttu-id="a3ddf-147">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a3ddf-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a3ddf-148">Input da tastiera</span><span class="sxs-lookup"><span data-stu-id="a3ddf-148">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

