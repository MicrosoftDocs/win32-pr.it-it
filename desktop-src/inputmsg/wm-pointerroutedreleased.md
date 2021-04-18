---
title: Messaggio WM_POINTERROUTEDRELEASED
description: Inviato a tutti i processi (configurato per il concatenamento tra processi tramite AddContentWithCrossProcessChaining e non gestisce l'input del puntatore) mai associato a un ID puntatore specifico, quando viene ricevuto un messaggio di WM_POINTERUP nel processo corrente.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERROUTEDRELEASED
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 8e24a0df1a2bbdf2b0a9df97057686aa6045eff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400637"
---
# <a name="wm_pointerroutedreleased-message"></a><span data-ttu-id="8c39e-104">Messaggio WM_POINTERROUTEDRELEASED</span><span class="sxs-lookup"><span data-stu-id="8c39e-104">WM_POINTERROUTEDRELEASED message</span></span>

<span data-ttu-id="8c39e-105">Inviato a tutti i processi (configurato per il concatenamento tra processi tramite [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) e non gestisce l'input del puntatore) mai associato a un ID puntatore specifico, quando viene ricevuto un messaggio di [**WM_POINTERUP**](wm-pointerup.md) nel processo corrente.</span><span class="sxs-lookup"><span data-stu-id="8c39e-105">Sent to all processes (configured for cross-process chaining through [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) and not currently handling pointer input) ever associated with a specific pointer ID, when a [**WM_POINTERUP**](wm-pointerup.md) message is received on the current process.</span></span>


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
```



## <a name="parameters"></a><span data-ttu-id="8c39e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c39e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c39e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c39e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c39e-108">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8c39e-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8c39e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c39e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c39e-110">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8c39e-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c39e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c39e-111">Return value</span></span>

<span data-ttu-id="8c39e-112">NULL</span><span class="sxs-lookup"><span data-stu-id="8c39e-112">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="8c39e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c39e-113">Requirements</span></span>



| <span data-ttu-id="8c39e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c39e-114">Requirement</span></span> | <span data-ttu-id="8c39e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8c39e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c39e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c39e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8c39e-117">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8c39e-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8c39e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c39e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8c39e-119">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="8c39e-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8c39e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c39e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c39e-121"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c39e-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c39e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c39e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c39e-123">Messaggi</span><span class="sxs-lookup"><span data-stu-id="8c39e-123">Messages</span></span>](messages.md)
</dt> </dl>

 

