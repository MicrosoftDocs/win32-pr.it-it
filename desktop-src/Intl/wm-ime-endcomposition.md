---
description: Inviato a un'applicazione quando l'IME termina la composizione. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: Messaggio WM_IME_ENDCOMPOSITION (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ca9d1560810b22ae0d36010d2371e75b83a81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343631"
---
# <a name="wm_ime_endcomposition-message"></a><span data-ttu-id="e76cc-104">\_ \_ Messaggio ENDCOMPOSITION di WM IME</span><span class="sxs-lookup"><span data-stu-id="e76cc-104">WM\_IME\_ENDCOMPOSITION message</span></span>

<span data-ttu-id="e76cc-105">Inviato a un'applicazione quando l'IME termina la composizione.</span><span class="sxs-lookup"><span data-stu-id="e76cc-105">Sent to an application when the IME ends composition.</span></span> <span data-ttu-id="e76cc-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e76cc-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,      
  WM_IME_ENDCOMPOSITION,  
  WPARAM wParam,      
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="e76cc-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e76cc-107">Parameters</span></span>

<span data-ttu-id="e76cc-108">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="e76cc-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="e76cc-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e76cc-109">Return value</span></span>

<span data-ttu-id="e76cc-110">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="e76cc-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e76cc-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e76cc-111">Remarks</span></span>

<span data-ttu-id="e76cc-112">Un'applicazione deve elaborare questo messaggio se Visualizza caratteri di composizione.</span><span class="sxs-lookup"><span data-stu-id="e76cc-112">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="e76cc-113">Se l'applicazione ha creato una finestra IME, deve passare questo messaggio alla finestra.</span><span class="sxs-lookup"><span data-stu-id="e76cc-113">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="e76cc-114">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  elabora questo messaggio passandolo alla finestra IME predefinita.</span><span class="sxs-lookup"><span data-stu-id="e76cc-114">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="e76cc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e76cc-115">Requirements</span></span>



| <span data-ttu-id="e76cc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e76cc-116">Requirement</span></span> | <span data-ttu-id="e76cc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e76cc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e76cc-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e76cc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e76cc-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e76cc-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e76cc-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e76cc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e76cc-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e76cc-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e76cc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e76cc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e76cc-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e76cc-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e76cc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e76cc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e76cc-125">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="e76cc-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e76cc-126">Messaggi di gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="e76cc-126">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
