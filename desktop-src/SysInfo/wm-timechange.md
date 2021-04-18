---
description: Messaggio inviato ogni volta che viene apportata una modifica all'ora di sistema.
ms.assetid: 94b5b6f7-04bb-4e0a-848b-e2b31ffc2938
title: Messaggio WM_TIMECHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d43bb5cd4284813c45ab074a93a9cd9699883aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310722"
---
# <a name="wm_timechange-message"></a><span data-ttu-id="89ced-103">\_Messaggio TIMECHANGE WM</span><span class="sxs-lookup"><span data-stu-id="89ced-103">WM\_TIMECHANGE message</span></span>

<span data-ttu-id="89ced-104">Messaggio inviato ogni volta che viene apportata una modifica all'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="89ced-104">A message that is sent whenever there is a change in the system time.</span></span>

<span data-ttu-id="89ced-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="89ced-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // message identifier
  WPARAM wParam,   // not used; must be zero
  LPARAM lParam    // not used; must be zero
);
```



## <a name="parameters"></a><span data-ttu-id="89ced-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="89ced-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89ced-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="89ced-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="89ced-108">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="89ced-108">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="89ced-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="89ced-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="89ced-110">**WM \_ Identificatore TIMECHANGE** .</span><span class="sxs-lookup"><span data-stu-id="89ced-110">**WM\_TIMECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="89ced-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89ced-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89ced-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="89ced-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="89ced-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89ced-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89ced-114">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="89ced-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89ced-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89ced-115">Return value</span></span>

<span data-ttu-id="89ced-116">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="89ced-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="89ced-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="89ced-117">Remarks</span></span>

<span data-ttu-id="89ced-118">Un'applicazione non deve trasmettere questo messaggio, perché il sistema trasmette questo messaggio quando l'applicazione cambia l'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="89ced-118">An application should not broadcast this message, because the system will broadcast this message when the application changes the system time.</span></span>

## <a name="requirements"></a><span data-ttu-id="89ced-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89ced-119">Requirements</span></span>



| <span data-ttu-id="89ced-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="89ced-120">Requirement</span></span> | <span data-ttu-id="89ced-121">Valore</span><span class="sxs-lookup"><span data-stu-id="89ced-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89ced-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89ced-122">Minimum supported client</span></span><br/> | <span data-ttu-id="89ced-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="89ced-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="89ced-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89ced-124">Minimum supported server</span></span><br/> | <span data-ttu-id="89ced-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="89ced-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="89ced-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89ced-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="89ced-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89ced-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89ced-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89ced-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89ced-129">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="89ced-129">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

