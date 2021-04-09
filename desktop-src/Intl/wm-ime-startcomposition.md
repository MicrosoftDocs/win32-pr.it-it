---
description: Inviato immediatamente prima che l'IME generi la stringa di composizione come risultato di una sequenza di tasti. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 2740d009-8685-4f70-9b01-67b71f4ddcbd
title: Messaggio WM_IME_STARTCOMPOSITION (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bd9a93b4c6c2e8dba6658c84b5f431dd9a54e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879290"
---
# <a name="wm_ime_startcomposition-message"></a><span data-ttu-id="8fb7d-104">\_ \_ Messaggio STARTCOMPOSITION di WM IME</span><span class="sxs-lookup"><span data-stu-id="8fb7d-104">WM\_IME\_STARTCOMPOSITION message</span></span>

<span data-ttu-id="8fb7d-105">Inviato immediatamente prima che l'IME generi la stringa di composizione come risultato di una sequenza di tasti.</span><span class="sxs-lookup"><span data-stu-id="8fb7d-105">Sent immediately before the IME generates the composition string as a result of a keystroke.</span></span> <span data-ttu-id="8fb7d-106">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8fb7d-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,                
  WM_IME_STARTCOMPOSITION,  
  WPARAM wParam,            
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="8fb7d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fb7d-107">Parameters</span></span>

<span data-ttu-id="8fb7d-108">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="8fb7d-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="8fb7d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fb7d-109">Return value</span></span>

<span data-ttu-id="8fb7d-110">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="8fb7d-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fb7d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fb7d-111">Remarks</span></span>

<span data-ttu-id="8fb7d-112">Questo messaggio è una notifica a una finestra IME per aprire la relativa finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="8fb7d-112">This message is a notification to an IME window to open its composition window.</span></span> <span data-ttu-id="8fb7d-113">Un'applicazione deve elaborare questo messaggio se Visualizza caratteri di composizione.</span><span class="sxs-lookup"><span data-stu-id="8fb7d-113">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="8fb7d-114">Se un'applicazione ha creato una finestra IME, deve passare questo messaggio a tale finestra.</span><span class="sxs-lookup"><span data-stu-id="8fb7d-114">If an application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="8fb7d-115">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) elabora il messaggio passandolo alla finestra IME predefinita.</span><span class="sxs-lookup"><span data-stu-id="8fb7d-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes the message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fb7d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fb7d-116">Requirements</span></span>



| <span data-ttu-id="8fb7d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fb7d-117">Requirement</span></span> | <span data-ttu-id="8fb7d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8fb7d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb7d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fb7d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8fb7d-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8fb7d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8fb7d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fb7d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8fb7d-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8fb7d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8fb7d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fb7d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fb7d-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8fb7d-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fb7d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fb7d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb7d-126">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="8fb7d-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="8fb7d-127">Messaggi di gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="8fb7d-127">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
