---
title: Messaggio WM_CAPTURECHANGED (winuser. h)
description: Inviato alla finestra che sta perdendo l'acquisizione del mouse.
ms.assetid: 79c8f65e-31fa-4bdb-9e88-0160a52b5b7d
keywords:
- Input della tastiera e del mouse WM_CAPTURECHANGED messaggio
topic_type:
- apiref
api_name:
- WM_CAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050bc00a7ab19e22e0fe4ea1f35271707180d4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119511"
---
# <a name="wm_capturechanged-message"></a><span data-ttu-id="de237-104">\_Messaggio CAPTURECHANGED WM</span><span class="sxs-lookup"><span data-stu-id="de237-104">WM\_CAPTURECHANGED message</span></span>

<span data-ttu-id="de237-105">Inviato alla finestra che sta perdendo l'acquisizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="de237-105">Sent to the window that is losing the mouse capture.</span></span>

<span data-ttu-id="de237-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="de237-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CAPTURECHANGED               0x0215
```



## <a name="parameters"></a><span data-ttu-id="de237-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="de237-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de237-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de237-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de237-109">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="de237-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="de237-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de237-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de237-111">Handle per la finestra che acquisisce il mouse capture.</span><span class="sxs-lookup"><span data-stu-id="de237-111">A handle to the window gaining the mouse capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de237-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de237-112">Return value</span></span>

<span data-ttu-id="de237-113">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="de237-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="de237-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="de237-114">Remarks</span></span>

<span data-ttu-id="de237-115">Una finestra riceve questo messaggio anche se chiama [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) stesso.</span><span class="sxs-lookup"><span data-stu-id="de237-115">A window receives this message even if it calls [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) itself.</span></span> <span data-ttu-id="de237-116">Un'applicazione non deve tentare di impostare l'acquisizione del mouse in risposta a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="de237-116">An application should not attempt to set the mouse capture in response to this message.</span></span>

<span data-ttu-id="de237-117">Quando riceve questo messaggio, una finestra deve essere ridisegnata, se necessario, per riflettere il nuovo stato di acquisizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="de237-117">When it receives this message, a window should redraw itself, if necessary, to reflect the new mouse-capture state.</span></span>

## <a name="requirements"></a><span data-ttu-id="de237-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de237-118">Requirements</span></span>



| <span data-ttu-id="de237-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="de237-119">Requirement</span></span> | <span data-ttu-id="de237-120">Valore</span><span class="sxs-lookup"><span data-stu-id="de237-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de237-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de237-121">Minimum supported client</span></span><br/> | <span data-ttu-id="de237-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="de237-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="de237-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de237-123">Minimum supported server</span></span><br/> | <span data-ttu-id="de237-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="de237-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="de237-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de237-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="de237-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de237-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de237-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de237-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="de237-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="de237-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="de237-129">**ReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="de237-129">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

[<span data-ttu-id="de237-130">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="de237-130">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

<span data-ttu-id="de237-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="de237-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="de237-132">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="de237-132">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

