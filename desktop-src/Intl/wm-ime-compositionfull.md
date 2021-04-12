---
description: Inviato a un'applicazione quando la finestra IME non trova alcuno spazio per estendere l'area per la finestra di composizione. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: Messaggio WM_IME_COMPOSITIONFULL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33051ac3e4e893eb803d4b13d7bfbf53751258b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234187"
---
# <a name="wm_ime_compositionfull-message"></a><span data-ttu-id="194e7-104">\_ \_ Messaggio COMPOSITIONFULL di WM IME</span><span class="sxs-lookup"><span data-stu-id="194e7-104">WM\_IME\_COMPOSITIONFULL message</span></span>

<span data-ttu-id="194e7-105">Inviato a un'applicazione quando la finestra IME non trova alcuno spazio per estendere l'area per la finestra di composizione.</span><span class="sxs-lookup"><span data-stu-id="194e7-105">Sent to an application when the IME window finds no space to extend the area for the composition window.</span></span> <span data-ttu-id="194e7-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="194e7-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="194e7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="194e7-107">Parameters</span></span>

<span data-ttu-id="194e7-108">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="194e7-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="194e7-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="194e7-109">Return value</span></span>

<span data-ttu-id="194e7-110">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="194e7-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="194e7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="194e7-111">Remarks</span></span>

<span data-ttu-id="194e7-112">L'applicazione deve usare il comando [IMC \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) per specificare la modalità di visualizzazione della finestra.</span><span class="sxs-lookup"><span data-stu-id="194e7-112">The application should use the [IMC\_SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) command to specify how the window should be displayed.</span></span>

<span data-ttu-id="194e7-113">La finestra IME, anziché l'IME, invia questo messaggio di notifica tramite la funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="194e7-113">The IME window, instead of the IME, sends this notification message by the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="194e7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="194e7-114">Requirements</span></span>



| <span data-ttu-id="194e7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="194e7-115">Requirement</span></span> | <span data-ttu-id="194e7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="194e7-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="194e7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="194e7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="194e7-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="194e7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="194e7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="194e7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="194e7-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="194e7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="194e7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="194e7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="194e7-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="194e7-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="194e7-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="194e7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="194e7-124">Gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="194e7-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="194e7-125">Messaggi di gestione metodo di input</span><span class="sxs-lookup"><span data-stu-id="194e7-125">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="194e7-126">\_SETCOMPOSITIONWINDOW IMC</span><span class="sxs-lookup"><span data-stu-id="194e7-126">IMC\_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> </dl>

 

 
