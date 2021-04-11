---
description: Inviato a un'applicazione quando viene attivata una finestra. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: Messaggio WM_IME_SETCONTEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b36cb1e80127d1a451dabcc457dc364a27878ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226129"
---
# <a name="wm_ime_setcontext-message"></a><span data-ttu-id="00997-104">Messaggio di contesto di WM \_ IME \_</span><span class="sxs-lookup"><span data-stu-id="00997-104">WM\_IME\_SETCONTEXT message</span></span>

<span data-ttu-id="00997-105">Inviato a un'applicazione quando viene attivata una finestra.</span><span class="sxs-lookup"><span data-stu-id="00997-105">Sent to an application when a window is activated.</span></span> <span data-ttu-id="00997-106">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="00997-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
  WPARAM wParam,      
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="00997-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="00997-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00997-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="00997-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="00997-109">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="00997-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="00997-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00997-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00997-111">**True** se la finestra è attiva e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="00997-111">**TRUE** if the window is active, and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="00997-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00997-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00997-113">Opzioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="00997-113">Display options.</span></span> <span data-ttu-id="00997-114">Questo parametro può avere uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="00997-114">This parameter can have one or more of the following values.</span></span>



| <span data-ttu-id="00997-115">Valore</span><span class="sxs-lookup"><span data-stu-id="00997-115">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="00997-116">Significato</span><span class="sxs-lookup"><span data-stu-id="00997-116">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <span data-ttu-id="00997-117"><dt>**\_SHOWUICOMPOSITIONWINDOW ISC**</dt></span><span class="sxs-lookup"><span data-stu-id="00997-117"><dt>**ISC\_SHOWUICOMPOSITIONWINDOW**</dt></span></span> </dl> | <span data-ttu-id="00997-118">Mostra la finestra di composizione per interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="00997-118">Show the composition window by user interface window.</span></span><br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <span data-ttu-id="00997-119"><dt>**\_SHOWUIGUIDWINDOW ISC**</dt></span><span class="sxs-lookup"><span data-stu-id="00997-119"><dt>**ISC\_SHOWUIGUIDWINDOW**</dt></span></span> </dl>                      | <span data-ttu-id="00997-120">Mostra la finestra della Guida in base all'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="00997-120">Show the guide window by user interface window.</span></span><br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <span data-ttu-id="00997-121"><dt>**\_SHOWUISOFTKBD ISC**</dt></span><span class="sxs-lookup"><span data-stu-id="00997-121"><dt>**ISC\_SHOWUISOFTKBD**</dt></span></span> </dl>                               | <span data-ttu-id="00997-122">Mostra la finestra dell'interfaccia utente della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="00997-122">Show the soft keyboard by user interface window.</span></span><br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <span data-ttu-id="00997-123"><dt>**\_SHOWUICANDIDATEWINDOW ISC**</dt></span><span class="sxs-lookup"><span data-stu-id="00997-123"><dt>**ISC\_SHOWUICANDIDATEWINDOW**</dt></span></span> </dl>       | <span data-ttu-id="00997-124">Mostra la finestra candidata dell'indice 0 dalla finestra dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="00997-124">Show the candidate window of index 0 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="00997-125"><dt>ISC \_ SHOWUICANDIDATEWINDOW << 1</dt></span><span class="sxs-lookup"><span data-stu-id="00997-125"><dt>ISC\_SHOWUICANDIDATEWINDOW << 1</dt></span></span> </dl>                                                                                        | <span data-ttu-id="00997-126">Mostra la finestra candidata di index 1 dalla finestra dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="00997-126">Show the candidate window of index 1 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="00997-127"><dt>ISC \_ SHOWUICANDIDATEWINDOW << 2</dt></span><span class="sxs-lookup"><span data-stu-id="00997-127"><dt>ISC\_SHOWUICANDIDATEWINDOW << 2</dt></span></span> </dl>                                                                                        | <span data-ttu-id="00997-128">Mostra la finestra candidata di index 2 dalla finestra dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="00997-128">Show the candidate window of index 2 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="00997-129"><dt>ISC \_ SHOWUICANDIDATEWINDOW << 3</dt></span><span class="sxs-lookup"><span data-stu-id="00997-129"><dt>ISC\_SHOWUICANDIDATEWINDOW << 3</dt></span></span> </dl>                                                                                        | <span data-ttu-id="00997-130">Mostra la finestra candidata di index 3 dalla finestra dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="00997-130">Show the candidate window of index 3 by user interface window.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00997-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00997-131">Return value</span></span>

<span data-ttu-id="00997-132">Restituisce il valore restituito da [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="00997-132">Returns the value returned by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span>

## <a name="remarks"></a><span data-ttu-id="00997-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="00997-133">Remarks</span></span>

<span data-ttu-id="00997-134">Se l'applicazione ha creato una finestra IME, deve chiamare [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="00997-134">If the application has created an IME window, it should call [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="00997-135">In caso contrario, deve passare questo messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="00997-135">Otherwise, it should pass this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="00997-136">Se tramite l'applicazione viene disegnata la finestra di composizione, non è necessario che venga visualizzata la finestra di composizione predefinita della finestra IME.</span><span class="sxs-lookup"><span data-stu-id="00997-136">If the application draws the composition window, the default IME window does not have to show its composition window.</span></span> <span data-ttu-id="00997-137">In questo caso, l'applicazione deve cancellare il **valore \_ SHOWUICOMPOSITIONWINDOW di ISC** dal *parametro lParam* prima di passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span><span class="sxs-lookup"><span data-stu-id="00997-137">In this case, the application must clear the **ISC\_SHOWUICOMPOSITIONWINDOW** value from the *lParam* parameter before passing the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="00997-138">Per visualizzare una determinata finestra dell'interfaccia utente, un'applicazione deve rimuovere il valore corrispondente in modo che non venga visualizzato dall'IME.</span><span class="sxs-lookup"><span data-stu-id="00997-138">To display a certain user interface window, an application should remove the corresponding value so that the IME will not display it.</span></span>

## <a name="requirements"></a><span data-ttu-id="00997-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00997-139">Requirements</span></span>



| <span data-ttu-id="00997-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="00997-140">Requirement</span></span> | <span data-ttu-id="00997-141">Valore</span><span class="sxs-lookup"><span data-stu-id="00997-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00997-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00997-142">Minimum supported client</span></span><br/> | <span data-ttu-id="00997-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00997-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="00997-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00997-144">Minimum supported server</span></span><br/> | <span data-ttu-id="00997-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00997-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="00997-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00997-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="00997-147"><dt>Winuser. h (include Windows. h); </dt> <dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00997-147"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00997-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00997-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00997-149">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="00997-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="00997-150">Messaggi di gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="00997-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="00997-151">**ImmIsUIMessage**</span><span class="sxs-lookup"><span data-stu-id="00997-151">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
