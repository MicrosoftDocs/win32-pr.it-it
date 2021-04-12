---
title: Messaggio WM_MOUSEACTIVATE (winuser. h)
description: Inviato quando il cursore si trova in una finestra inattiva e l'utente preme un pulsante del mouse. La finestra padre riceve questo messaggio solo se la finestra figlio la passa alla funzione DefWindowProc.
ms.assetid: 335c0819-a655-4dd1-9511-1f148b87271c
keywords:
- Input della tastiera e del mouse WM_MOUSEACTIVATE messaggio
topic_type:
- apiref
api_name:
- WM_MOUSEACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba74141f8d519541d1e63327179fff2f27ad403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119507"
---
# <a name="wm_mouseactivate-message"></a><span data-ttu-id="608a7-105">\_Messaggio MOUSEACTIVATE WM</span><span class="sxs-lookup"><span data-stu-id="608a7-105">WM\_MOUSEACTIVATE message</span></span>

<span data-ttu-id="608a7-106">Inviato quando il cursore si trova in una finestra inattiva e l'utente preme un pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="608a7-106">Sent when the cursor is in an inactive window and the user presses a mouse button.</span></span> <span data-ttu-id="608a7-107">La finestra padre riceve questo messaggio solo se la finestra figlio la passa alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="608a7-107">The parent window receives this message only if the child window passes it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="608a7-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="608a7-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEACTIVATE                0x0021
```



## <a name="parameters"></a><span data-ttu-id="608a7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="608a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="608a7-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="608a7-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="608a7-111">Handle per la finestra padre di primo livello della finestra attivata.</span><span class="sxs-lookup"><span data-stu-id="608a7-111">A handle to the top-level parent window of the window being activated.</span></span>

</dd> <dt>

<span data-ttu-id="608a7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="608a7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="608a7-113">La parola di ordine inferiore specifica il valore di hit test restituito dalla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) come risultato dell'elaborazione del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="608a7-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="608a7-114">Per un elenco dei valori di hit test, vedere **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="608a7-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="608a7-115">La parola più ordinata specifica l'identificatore del messaggio del mouse generato quando l'utente ha premuto un pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="608a7-115">The high-order word specifies the identifier of the mouse message generated when the user pressed a mouse button.</span></span> <span data-ttu-id="608a7-116">Il messaggio del mouse viene rimosso o inviato alla finestra, a seconda del valore restituito.</span><span class="sxs-lookup"><span data-stu-id="608a7-116">The mouse message is either discarded or posted to the window, depending on the return value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="608a7-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="608a7-117">Return value</span></span>

<span data-ttu-id="608a7-118">Il valore restituito specifica se la finestra deve essere attivata e se l'identificatore del messaggio del mouse deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="608a7-118">The return value specifies whether the window should be activated and whether the identifier of the mouse message should be discarded.</span></span> <span data-ttu-id="608a7-119">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="608a7-119">It must be one of the following values.</span></span>



| <span data-ttu-id="608a7-120">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="608a7-120">Return code/value</span></span>                                                                                                                                          | <span data-ttu-id="608a7-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="608a7-121">Description</span></span>                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="608a7-122"><dt>**Ma \_ ATTIVA**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="608a7-122"><dt>**MA\_ACTIVATE**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="608a7-123">Attiva la finestra e non rimuove il messaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="608a7-123">Activates the window, and does not discard the mouse message.</span></span><br/>         |
| <dl> <span data-ttu-id="608a7-124"><dt>**Ma \_ ACTIVATEANDEAT**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="608a7-124"><dt>**MA\_ACTIVATEANDEAT**</dt> <dt>2</dt></span></span> </dl>   | <span data-ttu-id="608a7-125">Attiva la finestra ed Elimina il messaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="608a7-125">Activates the window, and discards the mouse message.</span></span><br/>                 |
| <dl> <span data-ttu-id="608a7-126"><dt>**Ma \_ Noactivate**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="608a7-126"><dt>**MA\_NOACTIVATE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="608a7-127">Non attiva la finestra e non rimuove il messaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="608a7-127">Does not activate the window, and does not discard the mouse message.</span></span><br/> |
| <dl> <span data-ttu-id="608a7-128"><dt>**Ma \_ NOACTIVATEANDEAT**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="608a7-128"><dt>**MA\_NOACTIVATEANDEAT**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="608a7-129">Non attiva la finestra, ma elimina il messaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="608a7-129">Does not activate the window, but discards the mouse message.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="608a7-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="608a7-130">Remarks</span></span>

<span data-ttu-id="608a7-131">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passa il messaggio alla finestra padre di una finestra figlio prima che venga eseguita qualsiasi elaborazione.</span><span class="sxs-lookup"><span data-stu-id="608a7-131">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes the message to a child window's parent window before any processing occurs.</span></span> <span data-ttu-id="608a7-132">La finestra padre determina se attivare la finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="608a7-132">The parent window determines whether to activate the child window.</span></span> <span data-ttu-id="608a7-133">Se attiva la finestra figlio, la finestra padre deve restituire **ma \_ noactivate** o **ma \_ NOACTIVATEANDEAT** per impedire al sistema di elaborare ulteriormente il messaggio.</span><span class="sxs-lookup"><span data-stu-id="608a7-133">If it activates the child window, the parent window should return **MA\_NOACTIVATE** or **MA\_NOACTIVATEANDEAT** to prevent the system from processing the message further.</span></span>

## <a name="requirements"></a><span data-ttu-id="608a7-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="608a7-134">Requirements</span></span>



| <span data-ttu-id="608a7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="608a7-135">Requirement</span></span> | <span data-ttu-id="608a7-136">Valore</span><span class="sxs-lookup"><span data-stu-id="608a7-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="608a7-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="608a7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="608a7-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="608a7-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="608a7-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="608a7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="608a7-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="608a7-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="608a7-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="608a7-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="608a7-142"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="608a7-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="608a7-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="608a7-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="608a7-144">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="608a7-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="608a7-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="608a7-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="608a7-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="608a7-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="608a7-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="608a7-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="608a7-148">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="608a7-148">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

<span data-ttu-id="608a7-149">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="608a7-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="608a7-150">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="608a7-150">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

