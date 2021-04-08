---
title: Messaggio WM_DESTROYCLIPBOARD (winuser. h)
description: Inviato al proprietario degli Appunti quando una chiamata alla funzione EmptyClipboard svuota gli Appunti. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 9f75b7fb-e9ae-4876-ba99-7db931b9c2ff
keywords:
- Scambio di dati del messaggio WM_DESTROYCLIPBOARD
topic_type:
- apiref
api_name:
- WM_DESTROYCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3e4b6c2e2d378d0f78cee1824b1e4ce17a433a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964949"
---
# <a name="wm_destroyclipboard-message"></a><span data-ttu-id="8dc69-105">\_Messaggio DESTROYCLIPBOARD WM</span><span class="sxs-lookup"><span data-stu-id="8dc69-105">WM\_DESTROYCLIPBOARD message</span></span>

<span data-ttu-id="8dc69-106">Inviato al proprietario degli Appunti quando una chiamata alla funzione [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) svuota gli Appunti.</span><span class="sxs-lookup"><span data-stu-id="8dc69-106">Sent to the clipboard owner when a call to the [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) function empties the clipboard.</span></span>

<span data-ttu-id="8dc69-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8dc69-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROYCLIPBOARD             0x0307
```



## <a name="parameters"></a><span data-ttu-id="8dc69-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8dc69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dc69-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8dc69-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc69-110">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8dc69-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8dc69-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8dc69-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8dc69-112">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8dc69-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dc69-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8dc69-113">Return value</span></span>

<span data-ttu-id="8dc69-114">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="8dc69-114">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dc69-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8dc69-115">Requirements</span></span>



| <span data-ttu-id="8dc69-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dc69-116">Requirement</span></span> | <span data-ttu-id="8dc69-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8dc69-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dc69-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8dc69-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8dc69-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8dc69-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8dc69-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8dc69-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8dc69-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8dc69-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8dc69-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8dc69-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dc69-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8dc69-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dc69-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8dc69-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="8dc69-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="8dc69-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8dc69-126">**EmptyClipboard**</span><span class="sxs-lookup"><span data-stu-id="8dc69-126">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

<span data-ttu-id="8dc69-127">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="8dc69-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8dc69-128">Appunti</span><span class="sxs-lookup"><span data-stu-id="8dc69-128">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

