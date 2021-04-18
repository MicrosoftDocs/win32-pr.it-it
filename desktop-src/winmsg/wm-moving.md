---
description: Inviato a una finestra che l'utente sta muovendo. Elaborando questo messaggio, un'applicazione può monitorare la posizione del rettangolo di trascinamento e, se necessario, modificarne la posizione.
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: Messaggio WM_MOVING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5847189d64601ec999321920ead716fbdf22e2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306658"
---
# <a name="wm_moving-message"></a><span data-ttu-id="b9ce2-104">\_Messaggio di trasferimento WM</span><span class="sxs-lookup"><span data-stu-id="b9ce2-104">WM\_MOVING message</span></span>

<span data-ttu-id="b9ce2-105">Inviato a una finestra che l'utente sta muovendo.</span><span class="sxs-lookup"><span data-stu-id="b9ce2-105">Sent to a window that the user is moving.</span></span> <span data-ttu-id="b9ce2-106">Elaborando questo messaggio, un'applicazione può monitorare la posizione del rettangolo di trascinamento e, se necessario, modificarne la posizione.</span><span class="sxs-lookup"><span data-stu-id="b9ce2-106">By processing this message, an application can monitor the position of the drag rectangle and, if needed, change its position.</span></span>

<span data-ttu-id="b9ce2-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b9ce2-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOVING                       0x0216
```



## <a name="parameters"></a><span data-ttu-id="b9ce2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9ce2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9ce2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b9ce2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9ce2-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="b9ce2-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b9ce2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9ce2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9ce2-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) con la posizione corrente della finestra, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="b9ce2-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the current position of the window, in screen coordinates.</span></span> <span data-ttu-id="b9ce2-113">Per modificare la posizione del rettangolo di trascinamento, un'applicazione deve modificare i membri di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="b9ce2-113">To change the position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9ce2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9ce2-114">Return value</span></span>

<span data-ttu-id="b9ce2-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="b9ce2-115">Type: **LRESULT**</span></span>

<span data-ttu-id="b9ce2-116">Un'applicazione deve restituire **true** se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="b9ce2-116">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ce2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9ce2-117">Requirements</span></span>



| <span data-ttu-id="b9ce2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9ce2-118">Requirement</span></span> | <span data-ttu-id="b9ce2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b9ce2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ce2-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9ce2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b9ce2-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b9ce2-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b9ce2-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9ce2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b9ce2-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b9ce2-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b9ce2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9ce2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9ce2-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9ce2-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9ce2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9ce2-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b9ce2-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b9ce2-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b9ce2-128">**\_spostamento WM**</span><span class="sxs-lookup"><span data-stu-id="b9ce2-128">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="b9ce2-129">**\_dimensionamento WM**</span><span class="sxs-lookup"><span data-stu-id="b9ce2-129">**WM\_SIZING**</span></span>](wm-sizing.md)
</dt> <dt>

<span data-ttu-id="b9ce2-130">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b9ce2-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b9ce2-131">Windows</span><span class="sxs-lookup"><span data-stu-id="b9ce2-131">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="b9ce2-132">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="b9ce2-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="b9ce2-133">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b9ce2-133">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 
