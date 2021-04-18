---
description: Inviato a un'applicazione dall'IME per notificare all'applicazione una versione della chiave e per Mantenete l'ordine dei messaggi. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: Messaggio WM_IME_KEYUP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0eb6c6701510a373573ff6d85d5b50a8541b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307279"
---
# <a name="wm_ime_keyup-message"></a><span data-ttu-id="50604-104">\_ \_ Messaggio KEYUP di WM IME</span><span class="sxs-lookup"><span data-stu-id="50604-104">WM\_IME\_KEYUP message</span></span>

<span data-ttu-id="50604-105">Inviato a un'applicazione dall'IME per notificare all'applicazione una versione della chiave e per Mantenete l'ordine dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="50604-105">Sent to an application by the IME to notify the application of a key release and to keep message order.</span></span> <span data-ttu-id="50604-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="50604-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_KEYUP,    
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="50604-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="50604-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50604-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="50604-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="50604-109">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="50604-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="50604-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50604-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50604-111">Codice chiave virtuale della chiave.</span><span class="sxs-lookup"><span data-stu-id="50604-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="50604-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50604-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50604-113">Numero di ripetizioni, codice di analisi, flag di chiave estesa, codice del contesto, flag di stato della chiave precedente e flag di stato di transizione, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="50604-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown below.</span></span>



| <span data-ttu-id="50604-114">bit</span><span class="sxs-lookup"><span data-stu-id="50604-114">Bit</span></span>   | <span data-ttu-id="50604-115">Significato</span><span class="sxs-lookup"><span data-stu-id="50604-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="50604-116">0-15</span><span class="sxs-lookup"><span data-stu-id="50604-116">0-15</span></span>  | <span data-ttu-id="50604-117">Numero di ripetizioni.</span><span class="sxs-lookup"><span data-stu-id="50604-117">Repeat count.</span></span> <span data-ttu-id="50604-118">Il valore è sempre 1.</span><span class="sxs-lookup"><span data-stu-id="50604-118">This value is always 1.</span></span>                                       |
| <span data-ttu-id="50604-119">16-23</span><span class="sxs-lookup"><span data-stu-id="50604-119">16-23</span></span> | <span data-ttu-id="50604-120">Analizzare il codice.</span><span class="sxs-lookup"><span data-stu-id="50604-120">Scan code.</span></span>                                                                  |
| <span data-ttu-id="50604-121">24</span><span class="sxs-lookup"><span data-stu-id="50604-121">24</span></span>    | <span data-ttu-id="50604-122">Chiave estesa.</span><span class="sxs-lookup"><span data-stu-id="50604-122">Extended key.</span></span> <span data-ttu-id="50604-123">Questo valore è 1 se è una chiave estesa.</span><span class="sxs-lookup"><span data-stu-id="50604-123">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="50604-124">Negli altri casi è 0.</span><span class="sxs-lookup"><span data-stu-id="50604-124">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="50604-125">25-28</span><span class="sxs-lookup"><span data-stu-id="50604-125">25-28</span></span> | <span data-ttu-id="50604-126">Non usato.</span><span class="sxs-lookup"><span data-stu-id="50604-126">Not used.</span></span>                                                                   |
| <span data-ttu-id="50604-127">29</span><span class="sxs-lookup"><span data-stu-id="50604-127">29</span></span>    | <span data-ttu-id="50604-128">Codice del contesto.</span><span class="sxs-lookup"><span data-stu-id="50604-128">Context code.</span></span> <span data-ttu-id="50604-129">Il valore è sempre 0 .</span><span class="sxs-lookup"><span data-stu-id="50604-129">This value is always 0.</span></span>                                       |
| <span data-ttu-id="50604-130">30</span><span class="sxs-lookup"><span data-stu-id="50604-130">30</span></span>    | <span data-ttu-id="50604-131">Stato precedente della chiave.</span><span class="sxs-lookup"><span data-stu-id="50604-131">Previous key state.</span></span> <span data-ttu-id="50604-132">Il valore è sempre 1.</span><span class="sxs-lookup"><span data-stu-id="50604-132">This value is always 1.</span></span>                                 |
| <span data-ttu-id="50604-133">31</span><span class="sxs-lookup"><span data-stu-id="50604-133">31</span></span>    | <span data-ttu-id="50604-134">Stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="50604-134">Transition state.</span></span> <span data-ttu-id="50604-135">Il valore è sempre 1.</span><span class="sxs-lookup"><span data-stu-id="50604-135">This value is always 1.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50604-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50604-136">Return value</span></span>

<span data-ttu-id="50604-137">Un'applicazione deve restituire 0 se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="50604-137">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="50604-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="50604-138">Remarks</span></span>

<span data-ttu-id="50604-139">Un'applicazione può elaborare questo messaggio o passarlo alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  per generare un messaggio [**WM \_ KEYUP**](../inputdev/wm-keyup.md) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="50604-139">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYUP**](../inputdev/wm-keyup.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="50604-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50604-140">Requirements</span></span>



| <span data-ttu-id="50604-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="50604-141">Requirement</span></span> | <span data-ttu-id="50604-142">Valore</span><span class="sxs-lookup"><span data-stu-id="50604-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50604-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50604-143">Minimum supported client</span></span><br/> | <span data-ttu-id="50604-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="50604-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="50604-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50604-145">Minimum supported server</span></span><br/> | <span data-ttu-id="50604-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="50604-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="50604-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50604-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="50604-148"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50604-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50604-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50604-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50604-150">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="50604-150">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="50604-151">Messaggi di gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="50604-151">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
