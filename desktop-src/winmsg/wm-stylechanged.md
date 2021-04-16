---
description: Inviato a una finestra dopo che la funzione SetWindowLong ha modificato uno o più stili della finestra.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: Messaggio WM_STYLECHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5429db06dea95dbbc003e432a2b619c5cf8d056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529833"
---
# <a name="wm_stylechanged-message"></a><span data-ttu-id="e7b7c-103">\_Messaggio STYLECHANGED WM</span><span class="sxs-lookup"><span data-stu-id="e7b7c-103">WM\_STYLECHANGED message</span></span>

<span data-ttu-id="e7b7c-104">Inviato a una finestra dopo che la funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) ha modificato uno o più stili della finestra.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-104">Sent to a window after the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function has changed one or more of the window's styles.</span></span>

<span data-ttu-id="e7b7c-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e7b7c-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a><span data-ttu-id="e7b7c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7b7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b7c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7b7c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7b7c-108">Indica se gli stili o gli stili della finestra estesa della finestra sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-108">Indicates whether the window's styles or extended window styles have changed.</span></span> <span data-ttu-id="e7b7c-109">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="e7b7c-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e7b7c-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="e7b7c-111">Significato</span><span class="sxs-lookup"><span data-stu-id="e7b7c-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="e7b7c-112"><dt>**GWL \_ EXSTYLE**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="e7b7c-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="e7b7c-113">Gli stili estesi della finestra sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-113">The extended window styles have changed.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="e7b7c-114"><dt>**GWL \_ STILE**</dt> <dt>-16</dt></span><span class="sxs-lookup"><span data-stu-id="e7b7c-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="e7b7c-115">Gli stili della finestra sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-115">The window styles have changed.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="e7b7c-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7b7c-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7b7c-117">Puntatore a una struttura [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) che contiene i nuovi stili per la finestra.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the new styles for the window.</span></span> <span data-ttu-id="e7b7c-118">Un'applicazione può esaminare gli stili, ma non modificarli.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-118">An application can examine the styles, but cannot change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b7c-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7b7c-119">Return value</span></span>

<span data-ttu-id="e7b7c-120">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e7b7c-120">Type: **LRESULT**</span></span>

<span data-ttu-id="e7b7c-121">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b7c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7b7c-122">Requirements</span></span>



| <span data-ttu-id="e7b7c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b7c-123">Requirement</span></span> | <span data-ttu-id="e7b7c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e7b7c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b7c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7b7c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e7b7c-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e7b7c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e7b7c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7b7c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e7b7c-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e7b7c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7b7c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7b7c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7b7c-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7b7c-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7b7c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7b7c-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7b7c-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e7b7c-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e7b7c-133">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="e7b7c-133">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[<span data-ttu-id="e7b7c-134">**STYLESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="e7b7c-134">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="e7b7c-135">**\_STYLECHANGING WM**</span><span class="sxs-lookup"><span data-stu-id="e7b7c-135">**WM\_STYLECHANGING**</span></span>](wm-stylechanging.md)
</dt> <dt>

<span data-ttu-id="e7b7c-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e7b7c-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e7b7c-137">Windows</span><span class="sxs-lookup"><span data-stu-id="e7b7c-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
