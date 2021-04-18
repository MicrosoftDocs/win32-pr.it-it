---
description: Inviato a un'applicazione per notificare le modifiche apportate alla finestra IME. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 20e064b8-2baf-4b4c-8341-36c3e4643eff
title: Messaggio WM_IME_NOTIFY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5ab1b2a1fd62d159ab4f216bf9b1bb6892ed69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307278"
---
# <a name="wm_ime_notify-message"></a><span data-ttu-id="09475-104">Messaggio WM_IME_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="09475-104">WM_IME_NOTIFY message</span></span>

<span data-ttu-id="09475-105">Inviato a un'applicazione per notificare le modifiche apportate alla finestra IME.</span><span class="sxs-lookup"><span data-stu-id="09475-105">Sent to an application to notify it of changes to the IME window.</span></span> <span data-ttu-id="09475-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="09475-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_NOTIFY,   
  WPARAM wParam,   
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="09475-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="09475-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09475-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="09475-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="09475-109">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="09475-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="09475-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09475-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09475-111">Comando.</span><span class="sxs-lookup"><span data-stu-id="09475-111">The command.</span></span> <span data-ttu-id="09475-112">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="09475-112">This parameter can have one of the following values.</span></span>

<dl>
<dd><span data-ttu-id="09475-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="09475-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="09475-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="09475-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="09475-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="09475-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="09475-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span><span class="sxs-lookup"><span data-stu-id="09475-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span></span></dd> 
<dd><span data-ttu-id="09475-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="09475-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="09475-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="09475-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="09475-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="09475-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="09475-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="09475-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="09475-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="09475-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="09475-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span><span class="sxs-lookup"><span data-stu-id="09475-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span></span></dd> 
<dd><span data-ttu-id="09475-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="09475-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span></span></dd> 
<dd><span data-ttu-id="09475-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span><span class="sxs-lookup"><span data-stu-id="09475-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span></span></dd> 
<dd><span data-ttu-id="09475-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="09475-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="09475-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09475-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09475-127">Dati specifici del comando, con formato dipendente dal valore del parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="09475-127">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="09475-128">Per ulteriori informazioni, fare riferimento alla documentazione per ogni comando.</span><span class="sxs-lookup"><span data-stu-id="09475-128">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09475-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09475-129">Return value</span></span>

<span data-ttu-id="09475-130">Il valore restituito dipende dal comando inviato.</span><span class="sxs-lookup"><span data-stu-id="09475-130">The return value depends on the command sent.</span></span>

## <a name="remarks"></a><span data-ttu-id="09475-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="09475-131">Remarks</span></span>

<span data-ttu-id="09475-132">Un'applicazione elabora questo messaggio se è responsabile della gestione della finestra IME.</span><span class="sxs-lookup"><span data-stu-id="09475-132">An application processes this message if it is responsible for managing the IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="09475-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09475-133">Requirements</span></span>



| <span data-ttu-id="09475-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="09475-134">Requirement</span></span> | <span data-ttu-id="09475-135">Valore</span><span class="sxs-lookup"><span data-stu-id="09475-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09475-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09475-136">Minimum supported client</span></span><br/> | <span data-ttu-id="09475-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="09475-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="09475-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09475-138">Minimum supported server</span></span><br/> | <span data-ttu-id="09475-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="09475-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="09475-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09475-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="09475-141"><dt>Winuser. h (include Windows. h); </dt> <dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09475-141"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09475-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09475-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09475-143">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="09475-143">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="09475-144">Messaggi di gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="09475-144">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="09475-145">IMN_CHANGECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="09475-145">IMN_CHANGECANDIDATE</span></span>](imn-changecandidate.md)
</dt> <dt>

[<span data-ttu-id="09475-146">IMN_CLOSECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="09475-146">IMN_CLOSECANDIDATE</span></span>](imn-closecandidate.md)
</dt> <dt>

[<span data-ttu-id="09475-147">IMN_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="09475-147">IMN_CLOSESTATUSWINDOW</span></span>](imn-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="09475-148">IMN_GUIDELINE</span><span class="sxs-lookup"><span data-stu-id="09475-148">IMN_GUIDELINE</span></span>](imn-guideline.md)
</dt> <dt>

[<span data-ttu-id="09475-149">IMN_OPENCANDIDATE</span><span class="sxs-lookup"><span data-stu-id="09475-149">IMN_OPENCANDIDATE</span></span>](imn-opencandidate.md)
</dt> <dt>

[<span data-ttu-id="09475-150">IMN_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="09475-150">IMN_OPENSTATUSWINDOW</span></span>](imn-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="09475-151">IMN_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="09475-151">IMN_SETCANDIDATEPOS</span></span>](imn-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="09475-152">IMN_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="09475-152">IMN_SETCOMPOSITIONFONT</span></span>](imn-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="09475-153">IMN_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="09475-153">IMN_SETCOMPOSITIONWINDOW</span></span>](imn-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="09475-154">IMN_SETCONVERSIONMODE</span><span class="sxs-lookup"><span data-stu-id="09475-154">IMN_SETCONVERSIONMODE</span></span>](imn-setconversionmode.md)
</dt> <dt>

[<span data-ttu-id="09475-155">IMN_SETOPENSTATUS</span><span class="sxs-lookup"><span data-stu-id="09475-155">IMN_SETOPENSTATUS</span></span>](imn-setopenstatus.md)
</dt> <dt>

[<span data-ttu-id="09475-156">IMN_SETSENTENCEMODE</span><span class="sxs-lookup"><span data-stu-id="09475-156">IMN_SETSENTENCEMODE</span></span>](imn-setsentencemode.md)
</dt> <dt>

[<span data-ttu-id="09475-157">IMN_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="09475-157">IMN_SETSTATUSWINDOWPOS</span></span>](imn-setstatuswindowpos.md)
</dt> </dl>

 

 
