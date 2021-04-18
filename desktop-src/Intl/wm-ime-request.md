---
description: Inviato a un'applicazione per fornire comandi e informazioni sulla richiesta. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: c5e9f256-eed2-46cb-bb33-0e640a975f1f
title: Messaggio WM_IME_REQUEST (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d0cea120d088fe1423b1d7dcb822307886675b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307277"
---
# <a name="wm_ime_request-message"></a><span data-ttu-id="6b4a6-104">Messaggio WM_IME_REQUEST</span><span class="sxs-lookup"><span data-stu-id="6b4a6-104">WM_IME_REQUEST message</span></span>

<span data-ttu-id="6b4a6-105">Inviato a un'applicazione per fornire comandi e informazioni sulla richiesta.</span><span class="sxs-lookup"><span data-stu-id="6b4a6-105">Sent to an application to provide commands and request information.</span></span> <span data-ttu-id="6b4a6-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6b4a6-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_REQUEST,  
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="6b4a6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b4a6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b4a6-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6b4a6-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6b4a6-109">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="6b4a6-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="6b4a6-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b4a6-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b4a6-111">Comando.</span><span class="sxs-lookup"><span data-stu-id="6b4a6-111">Command.</span></span> <span data-ttu-id="6b4a6-112">Per il parametro è possibile specificare uno dei valori riportati di seguito:</span><span class="sxs-lookup"><span data-stu-id="6b4a6-112">This parameter can have one of the following values:</span></span>

<dl> 
<dd><span data-ttu-id="6b4a6-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="6b4a6-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="6b4a6-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="6b4a6-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="6b4a6-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="6b4a6-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="6b4a6-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="6b4a6-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span></span></dd> 
<dd><span data-ttu-id="6b4a6-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span><span class="sxs-lookup"><span data-stu-id="6b4a6-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span></span></dd> 
<dd><span data-ttu-id="6b4a6-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span><span class="sxs-lookup"><span data-stu-id="6b4a6-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span></span></dd> 
<dd><span data-ttu-id="6b4a6-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="6b4a6-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="6b4a6-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b4a6-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b4a6-121">Dati specifici del comando.</span><span class="sxs-lookup"><span data-stu-id="6b4a6-121">Command-specific data.</span></span> <span data-ttu-id="6b4a6-122">Per ulteriori informazioni, vedere la descrizione di ogni comando.</span><span class="sxs-lookup"><span data-stu-id="6b4a6-122">For more information, see the description for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b4a6-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b4a6-123">Return value</span></span>

<span data-ttu-id="6b4a6-124">Restituisce un valore specifico del comando.</span><span class="sxs-lookup"><span data-stu-id="6b4a6-124">Returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b4a6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b4a6-125">Requirements</span></span>



| <span data-ttu-id="6b4a6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b4a6-126">Requirement</span></span> | <span data-ttu-id="6b4a6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6b4a6-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b4a6-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b4a6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6b4a6-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b4a6-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="6b4a6-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b4a6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6b4a6-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b4a6-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="6b4a6-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b4a6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b4a6-133"><dt>Winuser. h (include Windows. h); </dt> <dt>Imm. h (Includi Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b4a6-133"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b4a6-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b4a6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b4a6-135">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="6b4a6-135">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="6b4a6-136">Messaggi di gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="6b4a6-136">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="6b4a6-137">IMR_CANDIDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="6b4a6-137">IMR_CANDIDATEWINDOW</span></span>](imr-candidatewindow.md)
</dt> <dt>

[<span data-ttu-id="6b4a6-138">IMR_COMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="6b4a6-138">IMR_COMPOSITIONFONT</span></span>](imr-compositionfont.md)
</dt> <dt>

[<span data-ttu-id="6b4a6-139">IMR_COMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="6b4a6-139">IMR_COMPOSITIONWINDOW</span></span>](imr-compositionwindow.md)
</dt> <dt>

[<span data-ttu-id="6b4a6-140">IMR_CONFIRMRECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="6b4a6-140">IMR_CONFIRMRECONVERTSTRING</span></span>](imr-confirmreconvertstring.md)
</dt> <dt>

[<span data-ttu-id="6b4a6-141">IMR_DOCUMENTFEED</span><span class="sxs-lookup"><span data-stu-id="6b4a6-141">IMR_DOCUMENTFEED</span></span>](imr-documentfeed.md)
</dt> <dt>

[<span data-ttu-id="6b4a6-142">IMR_QUERYCHARPOSITION</span><span class="sxs-lookup"><span data-stu-id="6b4a6-142">IMR_QUERYCHARPOSITION</span></span>](imr-querycharposition.md)
</dt> <dt>

[<span data-ttu-id="6b4a6-143">IMR_RECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="6b4a6-143">IMR_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> </dl>

 

 
