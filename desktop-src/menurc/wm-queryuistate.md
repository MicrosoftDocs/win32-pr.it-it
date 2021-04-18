---
title: Messaggio WM_QUERYUISTATE (winuser. h)
description: Un'applicazione invia il \_ messaggio WM QUERYUISTATE per recuperare lo stato dell'interfaccia utente per una finestra.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- Menu del messaggio WM_QUERYUISTATE e altre risorse
topic_type:
- apiref
api_name:
- WM_QUERYUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1574fe0dab2a0885c8012bf19eed50facfd6cce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302726"
---
# <a name="wm_queryuistate-message"></a><span data-ttu-id="c19b6-104">\_Messaggio QUERYUISTATE WM</span><span class="sxs-lookup"><span data-stu-id="c19b6-104">WM\_QUERYUISTATE message</span></span>

<span data-ttu-id="c19b6-105">Un'applicazione invia il messaggio **WM \_ QUERYUISTATE** per recuperare lo stato dell'interfaccia utente per una finestra.</span><span class="sxs-lookup"><span data-stu-id="c19b6-105">An application sends the **WM\_QUERYUISTATE** message to retrieve the UI state for a window.</span></span>


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a><span data-ttu-id="c19b6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c19b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c19b6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c19b6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c19b6-108">Questo parametro non viene utilizzato e deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="c19b6-108">This parameter is not used and must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="c19b6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c19b6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c19b6-110">Questo parametro non viene utilizzato e deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="c19b6-110">This parameter is not used and must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c19b6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c19b6-111">Return value</span></span>

<span data-ttu-id="c19b6-112">Il valore restituito è **null** se gli indicatori di stato attivo e i tasti di scelta rapida sono visibili.</span><span class="sxs-lookup"><span data-stu-id="c19b6-112">The return value is **NULL** if the focus indicators and the keyboard accelerators are visible.</span></span> <span data-ttu-id="c19b6-113">In caso contrario, il valore restituito può essere uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c19b6-113">Otherwise, the return value can be one or more of the following values.</span></span>



| <span data-ttu-id="c19b6-114">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="c19b6-114">Return code/value</span></span>                                                                                                                                       | <span data-ttu-id="c19b6-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c19b6-115">Description</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c19b6-116"><dt>**UISF \_**</dt> <dt>0x4</dt> attivo</span><span class="sxs-lookup"><span data-stu-id="c19b6-116"><dt>**UISF\_ACTIVE**</dt> <dt>0x4</dt></span></span> </dl>    | <span data-ttu-id="c19b6-117">Un controllo deve essere disegnato nello stile usato per i controlli attivi.</span><span class="sxs-lookup"><span data-stu-id="c19b6-117">A control should be drawn in the style used for active controls.</span></span><br/> |
| <dl> <span data-ttu-id="c19b6-118"><dt>**UISF \_**</dt> <dt>0x2</dt> HIDEACCEL</span><span class="sxs-lookup"><span data-stu-id="c19b6-118"><dt>**UISF\_HIDEACCEL**</dt> <dt>0x2</dt></span></span> </dl> | <span data-ttu-id="c19b6-119">Gli acceleratori tastiera sono nascosti.</span><span class="sxs-lookup"><span data-stu-id="c19b6-119">Keyboard accelerators are hidden.</span></span><br/>                                |
| <dl> <span data-ttu-id="c19b6-120"><dt>**UISF \_**</dt> <dt>0x1</dt> hideFocus</span><span class="sxs-lookup"><span data-stu-id="c19b6-120"><dt>**UISF\_HIDEFOCUS**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="c19b6-121">Gli indicatori di stato attivo sono nascosti.</span><span class="sxs-lookup"><span data-stu-id="c19b6-121">Focus indicators are hidden.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="c19b6-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c19b6-122">Requirements</span></span>



| <span data-ttu-id="c19b6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c19b6-123">Requirement</span></span> | <span data-ttu-id="c19b6-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c19b6-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c19b6-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c19b6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c19b6-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c19b6-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c19b6-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c19b6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c19b6-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c19b6-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c19b6-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c19b6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c19b6-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c19b6-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c19b6-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c19b6-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="c19b6-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c19b6-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c19b6-133">**\_CHANGEUISTATE WM**</span><span class="sxs-lookup"><span data-stu-id="c19b6-133">**WM\_CHANGEUISTATE**</span></span>](wm-changeuistate.md)
</dt> <dt>

[<span data-ttu-id="c19b6-134">**\_UPDATEUISTATE WM**</span><span class="sxs-lookup"><span data-stu-id="c19b6-134">**WM\_UPDATEUISTATE**</span></span>](wm-updateuistate.md)
</dt> <dt>

<span data-ttu-id="c19b6-135">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c19b6-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c19b6-136">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="c19b6-136">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

 





