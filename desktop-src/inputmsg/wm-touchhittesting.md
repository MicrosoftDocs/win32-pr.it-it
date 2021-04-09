---
title: Messaggio WM_TOUCHHITTESTING
description: Inviato a una finestra in un tocco per determinare la destinazione del tocco più probabile.
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- Messaggi e notifiche di input del messaggio WM_TOUCHHITTESTING
topic_type:
- apiref
api_name:
- WM_TOUCHHITTESTING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 83b6e564d692fb0223ec8871b99cefcb9fddf40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120355"
---
# <a name="wm_touchhittesting-message"></a><span data-ttu-id="7f594-104">Messaggio WM_TOUCHHITTESTING</span><span class="sxs-lookup"><span data-stu-id="7f594-104">WM_TOUCHHITTESTING message</span></span>

<span data-ttu-id="7f594-105">Inviato a una finestra in un tocco per determinare la destinazione del tocco più probabile.</span><span class="sxs-lookup"><span data-stu-id="7f594-105">Sent to a window on a touch down in order to determine the most probable touch target.</span></span>

> <span data-ttu-id="7f594-106">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="7f594-106">\[!Important\]</span></span>  
> <span data-ttu-id="7f594-107">Le applicazioni desktop devono essere compatibili con DPI.</span><span class="sxs-lookup"><span data-stu-id="7f594-107">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="7f594-108">Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI.</span><span class="sxs-lookup"><span data-stu-id="7f594-108">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="7f594-109">La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo).</span><span class="sxs-lookup"><span data-stu-id="7f594-109">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="7f594-110">Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7f594-110">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_TOUCHHITTESTING       0x024D
```



## <a name="parameters"></a><span data-ttu-id="7f594-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f594-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f594-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f594-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f594-113">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7f594-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="7f594-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f594-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f594-115">Puntatore alla struttura [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) che include i dati dell'area di contatto tocco.</span><span class="sxs-lookup"><span data-stu-id="7f594-115">Pointer to the [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) structure that holds the touch contact area data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f594-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f594-116">Return value</span></span>

<span data-ttu-id="7f594-117">Se uno o più elementi si trovano all'interno dell'area contatto tocco, un'applicazione deve restituire il risultato di [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).</span><span class="sxs-lookup"><span data-stu-id="7f594-117">If one or more elements are within the touch contact area, an application should return the result of [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).</span></span>

<span data-ttu-id="7f594-118">Se nessun elemento si trova all'interno dell'area contatto tocco, un'applicazione deve impostare il valore di **Score** in [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) su [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) e chiamare [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) per ottenere il valore restituito lResult.</span><span class="sxs-lookup"><span data-stu-id="7f594-118">If no elements are within the touch contact area, an application should set the value of **score** in [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) to [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) and call [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) to get the LRESULT return value.</span></span>

<span data-ttu-id="7f594-119">Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="7f594-119">If the application does not process this message, it must call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="7f594-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f594-120">Remarks</span></span>

<span data-ttu-id="7f594-121">Questo messaggio viene inviato a Windows che effettua la registrazione tramite la funzione [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="7f594-121">This message is sent to windows that register through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f594-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f594-122">Requirements</span></span>



| <span data-ttu-id="7f594-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f594-123">Requirement</span></span> | <span data-ttu-id="7f594-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7f594-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f594-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f594-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7f594-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7f594-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="7f594-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f594-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7f594-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7f594-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7f594-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f594-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f594-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f594-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f594-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f594-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f594-132">Messaggi</span><span class="sxs-lookup"><span data-stu-id="7f594-132">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="7f594-133">**Punteggi hit testing tocco**</span><span class="sxs-lookup"><span data-stu-id="7f594-133">**Touch Hit Testing Scores**</span></span>](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

