---
title: Messaggio WM_POINTERROUTEDTO
description: Inviato quando l'input del puntatore in corso, per un ID puntatore esistente, esegue la transizione da un processo a un altro tra i contenuti configurati per il concatenamento tra processi (AddContentWithCrossProcessChaining).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERROUTEDTO
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 7658aeef77a0f7e19f2449213e9332b4e60c9450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400500"
---
# <a name="wm_pointerroutedto-message"></a><span data-ttu-id="2a14a-104">Messaggio WM_POINTERROUTEDTO</span><span class="sxs-lookup"><span data-stu-id="2a14a-104">WM_POINTERROUTEDTO message</span></span>

<span data-ttu-id="2a14a-105">Inviato quando l'input del puntatore in corso, per un ID puntatore esistente, esegue la transizione da un processo a un altro tra i contenuti configurati per il concatenamento tra processi ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span><span class="sxs-lookup"><span data-stu-id="2a14a-105">Sent when ongoing pointer input, for an existing pointer ID, transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="2a14a-106">Questo messaggio viene inviato al processo che non riceve attualmente l'input del puntatore.</span><span class="sxs-lookup"><span data-stu-id="2a14a-106">This message is sent to the process not currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDTO       0x0251
```



## <a name="parameters"></a><span data-ttu-id="2a14a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a14a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a14a-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a14a-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a14a-109">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2a14a-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="2a14a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a14a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a14a-111">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2a14a-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a14a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a14a-112">Return value</span></span>

<span data-ttu-id="2a14a-113">NULL</span><span class="sxs-lookup"><span data-stu-id="2a14a-113">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="2a14a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a14a-114">Remarks</span></span>

<span data-ttu-id="2a14a-115">Questo messaggio non viene inviato quando viene pubblicato un messaggio di [**WM_POINTERDOWN**](wm-pointerdown.md) per un nuovo ID puntatore in un processo diverso.</span><span class="sxs-lookup"><span data-stu-id="2a14a-115">This message is not sent when a [**WM_POINTERDOWN**](wm-pointerdown.md) message is posted for a new pointer ID on a different process.</span></span>

<span data-ttu-id="2a14a-116">Se un messaggio di **WM_POINTERROUTEDTO** viene pubblicato per primo, un messaggio di [**WM_POINTERDOWN**](wm-pointerdown.md) non viene inviato.</span><span class="sxs-lookup"><span data-stu-id="2a14a-116">A [**WM_POINTERDOWN**](wm-pointerdown.md) message is not sent if a **WM_POINTERROUTEDTO** message is posted first.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a14a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a14a-117">Requirements</span></span>



| <span data-ttu-id="2a14a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a14a-118">Requirement</span></span> | <span data-ttu-id="2a14a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2a14a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a14a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a14a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2a14a-121">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2a14a-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2a14a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a14a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2a14a-123">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="2a14a-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2a14a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a14a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a14a-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a14a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a14a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a14a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a14a-127">Messaggi</span><span class="sxs-lookup"><span data-stu-id="2a14a-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="2a14a-128">**WM_POINTERROUTEDAWAY**</span><span class="sxs-lookup"><span data-stu-id="2a14a-128">**WM_POINTERROUTEDAWAY**</span></span>](wm-pointerroutedaway.md)
</dt> </dl>

 

