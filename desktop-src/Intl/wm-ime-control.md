---
description: Inviato da un'applicazione per indirizzare la finestra IME per eseguire il comando richiesto.
ms.assetid: 5d3b7f8a-57c9-41e3-8022-9a3f515fc32e
title: Messaggio WM_IME_CONTROL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd0adc534883bc0b31984c8d3e9b57a04b555987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879294"
---
# <a name="wm_ime_control-message"></a><span data-ttu-id="f79dd-103">Messaggio WM_IME_CONTROL</span><span class="sxs-lookup"><span data-stu-id="f79dd-103">WM_IME_CONTROL message</span></span>

<span data-ttu-id="f79dd-104">Inviato da un'applicazione per indirizzare la finestra IME per eseguire il comando richiesto.</span><span class="sxs-lookup"><span data-stu-id="f79dd-104">Sent by an application to direct the IME window to carry out the requested command.</span></span> <span data-ttu-id="f79dd-105">L'applicazione utilizza questo messaggio per controllare la finestra IME creata.</span><span class="sxs-lookup"><span data-stu-id="f79dd-105">The application uses this message to control the IME window that it has created.</span></span> <span data-ttu-id="f79dd-106">Per inviare questo messaggio, l'applicazione chiama la funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="f79dd-106">To send this message, the application calls the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage(
  HWND   hwnd,
  WM_IME_CONTROL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="f79dd-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f79dd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f79dd-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="f79dd-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f79dd-109">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="f79dd-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="f79dd-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f79dd-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f79dd-111">Comando.</span><span class="sxs-lookup"><span data-stu-id="f79dd-111">The command.</span></span> <span data-ttu-id="f79dd-112">Per il parametro è possibile specificare uno dei valori riportati di seguito:</span><span class="sxs-lookup"><span data-stu-id="f79dd-112">This parameter can have one of the following values:</span></span>

<dl>
<dd><span data-ttu-id="f79dd-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="f79dd-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="f79dd-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="f79dd-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="f79dd-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="f79dd-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="f79dd-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="f79dd-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="f79dd-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="f79dd-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span></span></dd> 
<dd><span data-ttu-id="f79dd-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="f79dd-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="f79dd-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="f79dd-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="f79dd-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span><span class="sxs-lookup"><span data-stu-id="f79dd-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span></span></dd> 
<dd><span data-ttu-id="f79dd-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="f79dd-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="f79dd-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="f79dd-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl>
</dd>

<dt>

<span data-ttu-id="f79dd-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f79dd-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f79dd-124">Dati specifici del comando, con formato dipendente dal valore del parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f79dd-124">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="f79dd-125">Per ulteriori informazioni, fare riferimento alla documentazione per ogni comando.</span><span class="sxs-lookup"><span data-stu-id="f79dd-125">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f79dd-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f79dd-126">Return value</span></span>

<span data-ttu-id="f79dd-127">Il messaggio restituisce un valore specifico del comando.</span><span class="sxs-lookup"><span data-stu-id="f79dd-127">The message returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f79dd-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f79dd-128">Requirements</span></span>



| <span data-ttu-id="f79dd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f79dd-129">Requirement</span></span> | <span data-ttu-id="f79dd-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f79dd-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f79dd-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f79dd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f79dd-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f79dd-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="f79dd-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f79dd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f79dd-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f79dd-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="f79dd-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f79dd-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f79dd-136"><dt>Winuser. h (include Windows. h); </dt> <dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f79dd-136"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f79dd-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f79dd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f79dd-138">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="f79dd-138">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="f79dd-139">Messaggi di gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="f79dd-139">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="f79dd-140">IMC_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="f79dd-140">IMC_CLOSESTATUSWINDOW</span></span>](imc-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="f79dd-141">IMC_GETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="f79dd-141">IMC_GETCANDIDATEPOS</span></span>](imc-getcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="f79dd-142">IMC_GETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="f79dd-142">IMC_GETCOMPOSITIONFONT</span></span>](imc-getcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="f79dd-143">IMC_GETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="f79dd-143">IMC_GETCOMPOSITIONWINDOW</span></span>](imc-getcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="f79dd-144">IMC_GETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="f79dd-144">IMC_GETSTATUSWINDOWPOS</span></span>](imc-getstatuswindowpos.md)
</dt> <dt>

[<span data-ttu-id="f79dd-145">IMC_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="f79dd-145">IMC_OPENSTATUSWINDOW</span></span>](imc-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="f79dd-146">IMC_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="f79dd-146">IMC_SETCANDIDATEPOS</span></span>](imc-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="f79dd-147">IMC_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="f79dd-147">IMC_SETCOMPOSITIONFONT</span></span>](imc-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="f79dd-148">IMC_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="f79dd-148">IMC_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="f79dd-149">IMC_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="f79dd-149">IMC_SETSTATUSWINDOWPOS</span></span>](imc-setstatuswindowpos.md)
</dt> </dl>

 

 
