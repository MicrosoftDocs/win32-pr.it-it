---
title: Messaggio WM_POINTERACTIVATE
description: Inviato a una finestra inattiva quando un puntatore primario genera un WM_POINTERDOWN sulla finestra.
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERACTIVATE
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: b9bda11b5cb7a27f7744df6e20890a125a66bd88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302074"
---
# <a name="wm_pointeractivate-message"></a><span data-ttu-id="ced41-104">Messaggio WM_POINTERACTIVATE</span><span class="sxs-lookup"><span data-stu-id="ced41-104">WM_POINTERACTIVATE message</span></span>

<span data-ttu-id="ced41-105">Inviato a una finestra inattiva quando un puntatore primario genera un [**WM_POINTERDOWN**](wm-pointerdown.md) sulla finestra.</span><span class="sxs-lookup"><span data-stu-id="ced41-105">Sent to an inactive window when a primary pointer generates a [**WM_POINTERDOWN**](wm-pointerdown.md) over the window.</span></span> <span data-ttu-id="ced41-106">Finché il messaggio rimane non gestito, viene spostata verso l'alto nella catena della finestra padre fino a raggiungere la finestra di primo livello.</span><span class="sxs-lookup"><span data-stu-id="ced41-106">As long as the message remains unhandled, it travels up the parent window chain until it is reaches the top-level window.</span></span> <span data-ttu-id="ced41-107">Le applicazioni possono rispondere a questo messaggio per specificare se desiderano essere attivate.</span><span class="sxs-lookup"><span data-stu-id="ced41-107">Applications can respond to this message to specify whether they wish to be activated.</span></span>

<span data-ttu-id="ced41-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ced41-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a><span data-ttu-id="ced41-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ced41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ced41-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ced41-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ced41-111">Contiene l'identificatore del puntatore e informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="ced41-111">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="ced41-112">Usare le macro seguenti per recuperare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="ced41-112">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="ced41-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificatore del puntatore</span><span class="sxs-lookup"><span data-stu-id="ced41-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="ced41-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valore hit-test restituito dall'elaborazione del messaggio di [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="ced41-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="ced41-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ced41-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ced41-116">Contiene l'handle per la finestra di primo livello della finestra attivata.</span><span class="sxs-lookup"><span data-stu-id="ced41-116">Contains the handle to the top-level window of the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ced41-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ced41-117">Return value</span></span>

<span data-ttu-id="ced41-118">Se un'applicazione elabora il messaggio, deve restituire uno dei valori descritti nella sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ced41-118">If an application processes this message, it should return one of the values described in the Remarks section.</span></span>

<span data-ttu-id="ced41-119">Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="ced41-119">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="ced41-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="ced41-120">Remarks</span></span>

<span data-ttu-id="ced41-121">Un'applicazione può gestire questo messaggio e restituire uno dei valori seguenti per determinare il modo in cui il sistema elabora l'attivazione e l'input di attivazione:</span><span class="sxs-lookup"><span data-stu-id="ced41-121">An application can handle this message and return one of the following values to determine how the system processes the activation and the activating input:</span></span>

-   <span data-ttu-id="ced41-122">PA_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="ced41-122">PA_ACTIVATE</span></span>
-   <span data-ttu-id="ced41-123">PA_NOACTIVATE</span><span class="sxs-lookup"><span data-stu-id="ced41-123">PA_NOACTIVATE</span></span>

<span data-ttu-id="ced41-124">È importante notare che, quando l'utente interagisce con il sistema con più puntatori simultanei, l'opportunità di attivazione rappresentata dal messaggio di **WM_POINTERACTIVATE** è disponibile solo per le applicazioni per il primo di tali puntatori.</span><span class="sxs-lookup"><span data-stu-id="ced41-124">It is important to note that, when the user is interacting with the system with multiple simultaneous pointers, the activation opportunity that the **WM_POINTERACTIVATE** message represents is available to applications only for the first of those pointers.</span></span> <span data-ttu-id="ced41-125">Le applicazioni devono pertanto tenere presente che potrebbero continuare a ricevere input dai puntatori mentre sono inattive.</span><span class="sxs-lookup"><span data-stu-id="ced41-125">Applications should, therefore, be aware that they may still receive input from pointers while they are inactive.</span></span>

<span data-ttu-id="ced41-126">Se l'applicazione non gestisce questo messaggio, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) passa il messaggio alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="ced41-126">If the application does not handle this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) passes the message to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="ced41-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ced41-127">Requirements</span></span>



| <span data-ttu-id="ced41-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ced41-128">Requirement</span></span> | <span data-ttu-id="ced41-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ced41-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ced41-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ced41-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ced41-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ced41-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="ced41-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ced41-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ced41-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ced41-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ced41-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ced41-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ced41-135"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ced41-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ced41-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ced41-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ced41-137">Messaggi</span><span class="sxs-lookup"><span data-stu-id="ced41-137">Messages</span></span>](messages.md)
</dt> </dl>

 

