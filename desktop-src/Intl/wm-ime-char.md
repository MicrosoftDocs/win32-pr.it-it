---
description: Inviato a un'applicazione quando l'IME ottiene un carattere del risultato della conversione. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: Messaggio WM_IME_CHAR (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0e2df06d9d837b0c1fbc0f9c9d9eb852252c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401787"
---
# <a name="wm_ime_char-message"></a><span data-ttu-id="d68f4-104">\_ \_ Messaggio char IME WM</span><span class="sxs-lookup"><span data-stu-id="d68f4-104">WM\_IME\_CHAR message</span></span>

<span data-ttu-id="d68f4-105">Inviato a un'applicazione quando l'IME ottiene un carattere del risultato della conversione.</span><span class="sxs-lookup"><span data-stu-id="d68f4-105">Sent to an application when the IME gets a character of the conversion result.</span></span> <span data-ttu-id="d68f4-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d68f4-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,
 WM_IME_CHAR,
 WPARAM wParam,
 LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="d68f4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d68f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d68f4-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d68f4-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d68f4-109">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="d68f4-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="d68f4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d68f4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d68f4-111">**DBCS:** Valore di carattere A byte singolo o a byte doppio.</span><span class="sxs-lookup"><span data-stu-id="d68f4-111">**DBCS:** A single-byte or double-byte character value.</span></span> <span data-ttu-id="d68f4-112">Per un carattere a due byte, (BYTE) (wParam >> 8) contiene il byte di apertura.</span><span class="sxs-lookup"><span data-stu-id="d68f4-112">For a double-byte character, (BYTE)(wParam >> 8) contains the lead byte.</span></span> <span data-ttu-id="d68f4-113">Si noti che le parentesi sono necessarie perché l'operatore cast ha una precedenza più alta rispetto all'operatore Shift.</span><span class="sxs-lookup"><span data-stu-id="d68f4-113">Note that the parentheses are necessary because the cast operator has higher precedence than the shift operator.</span></span>

<span data-ttu-id="d68f4-114">**Unicode:** Valore del carattere Unicode.</span><span class="sxs-lookup"><span data-stu-id="d68f4-114">**Unicode:** A Unicode character value.</span></span>

</dd> <dt>

<span data-ttu-id="d68f4-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d68f4-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d68f4-116">Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato della chiave precedente e il flag di stato di transizione con i valori definiti di seguito.</span><span class="sxs-lookup"><span data-stu-id="d68f4-116">The repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, with values as defined below.</span></span>



| <span data-ttu-id="d68f4-117">bit</span><span class="sxs-lookup"><span data-stu-id="d68f4-117">Bit</span></span>   | <span data-ttu-id="d68f4-118">Significato</span><span class="sxs-lookup"><span data-stu-id="d68f4-118">Meaning</span></span>                                                                              |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d68f4-119">0-15</span><span class="sxs-lookup"><span data-stu-id="d68f4-119">0-15</span></span>  | <span data-ttu-id="d68f4-120">Numero di ripetizioni.</span><span class="sxs-lookup"><span data-stu-id="d68f4-120">Repeat count.</span></span> <span data-ttu-id="d68f4-121">Poiché il primo byte e il secondo byte sono continui, è sempre 1.</span><span class="sxs-lookup"><span data-stu-id="d68f4-121">Since the first byte and second byte are continuous, this is always 1.</span></span> |
| <span data-ttu-id="d68f4-122">16-23</span><span class="sxs-lookup"><span data-stu-id="d68f4-122">16-23</span></span> | <span data-ttu-id="d68f4-123">Analizza il codice per un carattere asiatico completo.</span><span class="sxs-lookup"><span data-stu-id="d68f4-123">Scan code for a complete Asian character.</span></span>                                            |
| <span data-ttu-id="d68f4-124">24</span><span class="sxs-lookup"><span data-stu-id="d68f4-124">24</span></span>    | <span data-ttu-id="d68f4-125">Chiave estesa.</span><span class="sxs-lookup"><span data-stu-id="d68f4-125">Extended key.</span></span>                                                                        |
| <span data-ttu-id="d68f4-126">25-28</span><span class="sxs-lookup"><span data-stu-id="d68f4-126">25-28</span></span> | <span data-ttu-id="d68f4-127">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d68f4-127">Not used.</span></span>                                                                            |
| <span data-ttu-id="d68f4-128">29</span><span class="sxs-lookup"><span data-stu-id="d68f4-128">29</span></span>    | <span data-ttu-id="d68f4-129">Codice del contesto.</span><span class="sxs-lookup"><span data-stu-id="d68f4-129">Context code.</span></span>                                                                        |
| <span data-ttu-id="d68f4-130">30</span><span class="sxs-lookup"><span data-stu-id="d68f4-130">30</span></span>    | <span data-ttu-id="d68f4-131">Stato precedente della chiave.</span><span class="sxs-lookup"><span data-stu-id="d68f4-131">Previous key state.</span></span>                                                                  |
| <span data-ttu-id="d68f4-132">31</span><span class="sxs-lookup"><span data-stu-id="d68f4-132">31</span></span>    | <span data-ttu-id="d68f4-133">Stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="d68f4-133">Transition state.</span></span>                                                                    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d68f4-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="d68f4-134">Remarks</span></span>

<span data-ttu-id="d68f4-135">A differenza del messaggio [**WM \_ char**](../inputdev/wm-char.md) per una finestra non Unicode, questo messaggio può includere valori di caratteri a doppio byte e a byte singolo.</span><span class="sxs-lookup"><span data-stu-id="d68f4-135">Unlike the [**WM\_CHAR**](../inputdev/wm-char.md) message for a non-Unicode window, this message can include double-byte and single-byte character values.</span></span> <span data-ttu-id="d68f4-136">Per una finestra Unicode, questo messaggio è uguale a WM \_ Char.</span><span class="sxs-lookup"><span data-stu-id="d68f4-136">For a Unicode window, this message is the same as WM\_CHAR.</span></span>

<span data-ttu-id="d68f4-137">Per una finestra non Unicode, se il messaggio WM \_ IME \_ char include un carattere a due byte e l'applicazione passa il messaggio a [**DEFWINDOWPROC**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), l'IME converte questo messaggio in due messaggi WM \_ Char, ognuno dei quali contiene un byte del carattere a byte doppio.</span><span class="sxs-lookup"><span data-stu-id="d68f4-137">For a non-Unicode window, if the WM\_IME\_CHAR message includes a double-byte character and the application passes this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the IME converts this message into two WM\_CHAR messages, each containing one byte of the double-byte character.</span></span>

## <a name="requirements"></a><span data-ttu-id="d68f4-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d68f4-138">Requirements</span></span>



| <span data-ttu-id="d68f4-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="d68f4-139">Requirement</span></span> | <span data-ttu-id="d68f4-140">Valore</span><span class="sxs-lookup"><span data-stu-id="d68f4-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d68f4-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d68f4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d68f4-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d68f4-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d68f4-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d68f4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d68f4-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d68f4-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d68f4-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d68f4-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="d68f4-146"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d68f4-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d68f4-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d68f4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d68f4-148">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="d68f4-148">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d68f4-149">Messaggi di gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="d68f4-149">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
