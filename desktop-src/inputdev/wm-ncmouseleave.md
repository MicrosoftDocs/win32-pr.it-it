---
title: Messaggio WM_NCMOUSELEAVE (winuser. h)
description: Inserito in una finestra quando il cursore esce dall'area non client della finestra specificata in una chiamata precedente a TrackMouseEvent.
ms.assetid: b3ada6db-93ce-45d7-b408-d08692328aeb
keywords:
- Input della tastiera e del mouse WM_NCMOUSELEAVE messaggio
topic_type:
- apiref
api_name:
- WM_NCMOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf7f9d0931c2623d2e92010abfca96f391107b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301418"
---
# <a name="wm_ncmouseleave-message"></a><span data-ttu-id="38860-104">\_Messaggio NCMOUSELEAVE WM</span><span class="sxs-lookup"><span data-stu-id="38860-104">WM\_NCMOUSELEAVE message</span></span>

<span data-ttu-id="38860-105">Inserito in una finestra quando il cursore esce dall'area non client della finestra specificata in una chiamata precedente a [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="38860-105">Posted to a window when the cursor leaves the nonclient area of the window specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="38860-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="38860-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSELEAVE                 0x02A2
```



## <a name="parameters"></a><span data-ttu-id="38860-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="38860-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38860-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38860-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38860-109">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="38860-109">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="38860-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38860-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38860-111">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="38860-111">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38860-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38860-112">Return value</span></span>

<span data-ttu-id="38860-113">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="38860-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="38860-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="38860-114">Remarks</span></span>

<span data-ttu-id="38860-115">Tutti i tracciati richiesti da [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) vengono annullati quando viene generato questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="38860-115">All tracking requested by [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) is canceled when this message is generated.</span></span> <span data-ttu-id="38860-116">L'applicazione deve chiamare **TrackMouseEvent** quando il mouse riimmette la finestra se è necessario un ulteriore rilevamento del comportamento del passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="38860-116">The application must call **TrackMouseEvent** when the mouse reenters its window if it requires further tracking of mouse hover behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="38860-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38860-117">Requirements</span></span>



| <span data-ttu-id="38860-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="38860-118">Requirement</span></span> | <span data-ttu-id="38860-119">Valore</span><span class="sxs-lookup"><span data-stu-id="38860-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38860-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38860-120">Minimum supported client</span></span><br/> | <span data-ttu-id="38860-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38860-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="38860-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38860-122">Minimum supported server</span></span><br/> | <span data-ttu-id="38860-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38860-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="38860-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38860-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="38860-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38860-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38860-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38860-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="38860-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="38860-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="38860-128">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="38860-128">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="38860-129">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="38860-129">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="38860-130">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="38860-130">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="38860-131">**MOUSELEAVE di WM \_**</span><span class="sxs-lookup"><span data-stu-id="38860-131">**WM\_MOUSELEAVE**</span></span>](wm-mouseleave.md)
</dt> <dt>

<span data-ttu-id="38860-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="38860-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="38860-133">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="38860-133">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

