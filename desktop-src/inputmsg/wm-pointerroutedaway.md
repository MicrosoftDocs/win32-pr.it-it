---
title: Messaggio WM_POINTERROUTEDAWAY
description: Si verifica nel processo che riceve l'input quando l'input del puntatore viene indirizzato a un altro processo. AddContentWithCrossProcessChaining).
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERROUTEDAWAY
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDAWAY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3c099c02338aa70817d75717064e0b99ac13c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048531"
---
# <a name="wm_pointerroutedaway-message"></a><span data-ttu-id="14b60-104">Messaggio WM_POINTERROUTEDAWAY</span><span class="sxs-lookup"><span data-stu-id="14b60-104">WM_POINTERROUTEDAWAY message</span></span>

<span data-ttu-id="14b60-105">Si verifica nel processo che riceve l'input quando l'input del puntatore viene indirizzato a un altro processo.</span><span class="sxs-lookup"><span data-stu-id="14b60-105">Occurs on the process receiving input when the pointer input is routed to another process.</span></span>

<span data-ttu-id="14b60-106">Inviato quando l'input del puntatore passa da un processo a un altro tra i contenuti configurati per il concatenamento tra processi ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span><span class="sxs-lookup"><span data-stu-id="14b60-106">Sent when pointer input transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="14b60-107">Questo messaggio viene inviato al processo che riceve attualmente l'input del puntatore.</span><span class="sxs-lookup"><span data-stu-id="14b60-107">This message is sent to the process currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDAWAY       0x0252
```



## <a name="parameters"></a><span data-ttu-id="14b60-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="14b60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b60-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14b60-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14b60-110">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="14b60-110">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="14b60-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14b60-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14b60-112">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="14b60-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b60-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14b60-113">Return value</span></span>

<span data-ttu-id="14b60-114">NULL</span><span class="sxs-lookup"><span data-stu-id="14b60-114">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="14b60-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="14b60-115">Remarks</span></span>

<span data-ttu-id="14b60-116">Questo messaggio non viene inviato con un messaggio di [**WM_POINTERUP**](wm-pointerup.md) o un messaggio di [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="14b60-116">This message is not sent with either a [**WM_POINTERUP**](wm-pointerup.md) message or a [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b60-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14b60-117">Requirements</span></span>



| <span data-ttu-id="14b60-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="14b60-118">Requirement</span></span> | <span data-ttu-id="14b60-119">Valore</span><span class="sxs-lookup"><span data-stu-id="14b60-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14b60-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14b60-120">Minimum supported client</span></span><br/> | <span data-ttu-id="14b60-121">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="14b60-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="14b60-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14b60-122">Minimum supported server</span></span><br/> | <span data-ttu-id="14b60-123">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="14b60-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="14b60-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14b60-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="14b60-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14b60-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14b60-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14b60-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b60-127">Messaggi</span><span class="sxs-lookup"><span data-stu-id="14b60-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="14b60-128">**WM_POINTERROUTEDTO**</span><span class="sxs-lookup"><span data-stu-id="14b60-128">**WM_POINTERROUTEDTO**</span></span>](wm-pointerroutedto.md)
</dt> </dl>

 

