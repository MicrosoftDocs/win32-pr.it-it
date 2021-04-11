---
description: Inviato a un'applicazione dall'IME per notificare all'applicazione la pressione di un tasto e per mantenere l'ordine dei messaggi. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: Messaggio WM_IME_KEYDOWN (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3089af3c839f70e7f55895ae13158e7b2240605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226131"
---
# <a name="wm_ime_keydown-message"></a><span data-ttu-id="38b48-104">\_ \_ Messaggio KeyDown IME WM</span><span class="sxs-lookup"><span data-stu-id="38b48-104">WM\_IME\_KEYDOWN message</span></span>

<span data-ttu-id="38b48-105">Inviato a un'applicazione dall'IME per notificare all'applicazione la pressione di un tasto e per mantenere l'ordine dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="38b48-105">Sent to an application by the IME to notify the application of a key press and to keep message order.</span></span> <span data-ttu-id="38b48-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="38b48-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,        
  WM_IME_KEYDOWN,  
  WPARAM wParam, 
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="38b48-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="38b48-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38b48-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="38b48-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="38b48-109">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="38b48-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="38b48-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38b48-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38b48-111">Codice chiave virtuale della chiave.</span><span class="sxs-lookup"><span data-stu-id="38b48-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="38b48-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38b48-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38b48-113">Numero di ripetizioni, codice di analisi, flag di chiave estesa, codice del contesto, flag di stato della chiave precedente e flag di stato di transizione, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="38b48-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown in the following table.</span></span>



| <span data-ttu-id="38b48-114">bit</span><span class="sxs-lookup"><span data-stu-id="38b48-114">Bit</span></span>   | <span data-ttu-id="38b48-115">Significato</span><span class="sxs-lookup"><span data-stu-id="38b48-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="38b48-116">0-15</span><span class="sxs-lookup"><span data-stu-id="38b48-116">0-15</span></span>  | <span data-ttu-id="38b48-117">Numero di ripetizioni.</span><span class="sxs-lookup"><span data-stu-id="38b48-117">Repeat count.</span></span>                                                               |
| <span data-ttu-id="38b48-118">16-23</span><span class="sxs-lookup"><span data-stu-id="38b48-118">16-23</span></span> | <span data-ttu-id="38b48-119">Analizzare il codice.</span><span class="sxs-lookup"><span data-stu-id="38b48-119">Scan code.</span></span>                                                                  |
| <span data-ttu-id="38b48-120">24</span><span class="sxs-lookup"><span data-stu-id="38b48-120">24</span></span>    | <span data-ttu-id="38b48-121">Chiave estesa.</span><span class="sxs-lookup"><span data-stu-id="38b48-121">Extended key.</span></span> <span data-ttu-id="38b48-122">Questo valore è 1 se è una chiave estesa.</span><span class="sxs-lookup"><span data-stu-id="38b48-122">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="38b48-123">Negli altri casi è 0.</span><span class="sxs-lookup"><span data-stu-id="38b48-123">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="38b48-124">25-28</span><span class="sxs-lookup"><span data-stu-id="38b48-124">25-28</span></span> | <span data-ttu-id="38b48-125">Non usato.</span><span class="sxs-lookup"><span data-stu-id="38b48-125">Not used.</span></span>                                                                   |
| <span data-ttu-id="38b48-126">29</span><span class="sxs-lookup"><span data-stu-id="38b48-126">29</span></span>    | <span data-ttu-id="38b48-127">Codice del contesto.</span><span class="sxs-lookup"><span data-stu-id="38b48-127">Context code.</span></span> <span data-ttu-id="38b48-128">Il valore è sempre 0 .</span><span class="sxs-lookup"><span data-stu-id="38b48-128">This value is always 0.</span></span>                                       |
| <span data-ttu-id="38b48-129">30</span><span class="sxs-lookup"><span data-stu-id="38b48-129">30</span></span>    | <span data-ttu-id="38b48-130">Stato precedente della chiave.</span><span class="sxs-lookup"><span data-stu-id="38b48-130">Previous key state.</span></span> <span data-ttu-id="38b48-131">Questo valore è 1 se la chiave è inattiva o 0 se è attiva.</span><span class="sxs-lookup"><span data-stu-id="38b48-131">This value is 1 if the key is down or 0 if it is up.</span></span>    |
| <span data-ttu-id="38b48-132">31</span><span class="sxs-lookup"><span data-stu-id="38b48-132">31</span></span>    | <span data-ttu-id="38b48-133">Stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="38b48-133">Transition state.</span></span> <span data-ttu-id="38b48-134">Il valore è sempre 0 .</span><span class="sxs-lookup"><span data-stu-id="38b48-134">This value is always 0.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38b48-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38b48-135">Return value</span></span>

<span data-ttu-id="38b48-136">Un'applicazione deve restituire 0 se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="38b48-136">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="38b48-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="38b48-137">Remarks</span></span>

<span data-ttu-id="38b48-138">Un'applicazione può elaborare questo messaggio o passarlo alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  per generare un messaggio [**WM \_ KeyDown**](../inputdev/wm-keydown.md) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="38b48-138">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="38b48-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38b48-139">Requirements</span></span>



| <span data-ttu-id="38b48-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="38b48-140">Requirement</span></span> | <span data-ttu-id="38b48-141">Valore</span><span class="sxs-lookup"><span data-stu-id="38b48-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38b48-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38b48-142">Minimum supported client</span></span><br/> | <span data-ttu-id="38b48-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38b48-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="38b48-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38b48-144">Minimum supported server</span></span><br/> | <span data-ttu-id="38b48-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38b48-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="38b48-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38b48-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="38b48-147"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38b48-147"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38b48-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38b48-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38b48-149">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="38b48-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="38b48-150">Messaggi di gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="38b48-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
