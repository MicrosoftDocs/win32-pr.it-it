---
title: Messaggio WM_MOUSELEAVE (winuser. h)
description: Inserito in una finestra quando il cursore esce dall'area client della finestra specificata in una chiamata precedente a TrackMouseEvent.
ms.assetid: b23d24ff-531a-4b6d-8848-f82ac5568995
keywords:
- Input della tastiera e del mouse WM_MOUSELEAVE messaggio
topic_type:
- apiref
api_name:
- WM_MOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc96022e94df7f518b21b1c9a46895fc9204b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476144"
---
# <a name="wm_mouseleave-message"></a><span data-ttu-id="30e85-104">Messaggio di WM \_ MOUSELEAVE</span><span class="sxs-lookup"><span data-stu-id="30e85-104">WM\_MOUSELEAVE message</span></span>

<span data-ttu-id="30e85-105">Inserito in una finestra quando il cursore esce dall'area client della finestra specificata in una chiamata precedente a [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="30e85-105">Posted to a window when the cursor leaves the client area of the window specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="30e85-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="30e85-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSELEAVE                   0x02A3
```



## <a name="parameters"></a><span data-ttu-id="30e85-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="30e85-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30e85-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30e85-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30e85-109">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="30e85-109">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="30e85-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30e85-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30e85-111">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="30e85-111">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30e85-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30e85-112">Return value</span></span>

<span data-ttu-id="30e85-113">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="30e85-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="30e85-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="30e85-114">Remarks</span></span>

<span data-ttu-id="30e85-115">Tutti i tracciati richiesti da [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) vengono annullati quando viene generato questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="30e85-115">All tracking requested by [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) is canceled when this message is generated.</span></span> <span data-ttu-id="30e85-116">L'applicazione deve chiamare **TrackMouseEvent** quando il mouse riimmette la finestra se è necessario un ulteriore rilevamento del comportamento del passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="30e85-116">The application must call **TrackMouseEvent** when the mouse reenters its window if it requires further tracking of mouse hover behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="30e85-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30e85-117">Requirements</span></span>



| <span data-ttu-id="30e85-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="30e85-118">Requirement</span></span> | <span data-ttu-id="30e85-119">Valore</span><span class="sxs-lookup"><span data-stu-id="30e85-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30e85-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30e85-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30e85-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="30e85-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="30e85-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30e85-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30e85-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="30e85-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30e85-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30e85-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30e85-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30e85-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30e85-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30e85-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="30e85-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="30e85-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="30e85-128">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="30e85-128">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="30e85-129">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="30e85-129">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="30e85-130">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="30e85-130">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="30e85-131">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="30e85-131">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="30e85-132">**\_NCMOUSELEAVE WM**</span><span class="sxs-lookup"><span data-stu-id="30e85-132">**WM\_NCMOUSELEAVE**</span></span>](wm-ncmouseleave.md)
</dt> <dt>

<span data-ttu-id="30e85-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="30e85-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="30e85-134">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="30e85-134">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

