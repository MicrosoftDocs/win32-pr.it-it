---
title: Messaggio SBM_GETRANGE (winuser. h)
description: Il \_ messaggio SBM GetRange viene inviato per recuperare i valori di posizione minimo e massimo per il controllo barra di scorrimento.
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- Controlli di Windows Message SBM_GETRANGE
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ca47e0474152a9771d2787c4a039fb2c868b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964632"
---
# <a name="sbm_getrange-message"></a><span data-ttu-id="db2ba-104">\_Messaggio GETrange di SBM</span><span class="sxs-lookup"><span data-stu-id="db2ba-104">SBM\_GETRANGE message</span></span>

<span data-ttu-id="db2ba-105">Il messaggio **SBM \_ GetRange** viene inviato per recuperare i valori di posizione minimo e massimo per il controllo barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="db2ba-105">The **SBM\_GETRANGE** message is sent to retrieve the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="db2ba-106">Le applicazioni non devono inviare direttamente questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="db2ba-106">Applications should not send this message directly.</span></span> <span data-ttu-id="db2ba-107">Devono invece usare la funzione [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) .</span><span class="sxs-lookup"><span data-stu-id="db2ba-107">Instead, they should use the [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) function.</span></span> <span data-ttu-id="db2ba-108">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="db2ba-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="db2ba-109">Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **GetScrollRange** funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="db2ba-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="db2ba-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="db2ba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db2ba-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db2ba-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db2ba-112">Puntatore a una variabile che riceve la posizione di scorrimento minima.</span><span class="sxs-lookup"><span data-stu-id="db2ba-112">Pointer to a variable that receives the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="db2ba-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db2ba-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db2ba-114">Puntatore a una variabile che riceve la posizione di scorrimento massima.</span><span class="sxs-lookup"><span data-stu-id="db2ba-114">Pointer to a variable that receives the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db2ba-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db2ba-115">Return value</span></span>

<span data-ttu-id="db2ba-116">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="db2ba-116">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="db2ba-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db2ba-117">Requirements</span></span>



| <span data-ttu-id="db2ba-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="db2ba-118">Requirement</span></span> | <span data-ttu-id="db2ba-119">Valore</span><span class="sxs-lookup"><span data-stu-id="db2ba-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db2ba-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db2ba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="db2ba-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db2ba-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="db2ba-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db2ba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="db2ba-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db2ba-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="db2ba-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db2ba-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="db2ba-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db2ba-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db2ba-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db2ba-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="db2ba-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="db2ba-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="db2ba-128">**\_GETPOS SBM**</span><span class="sxs-lookup"><span data-stu-id="db2ba-128">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="db2ba-129">**\_SETPOS SBM**</span><span class="sxs-lookup"><span data-stu-id="db2ba-129">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="db2ba-130">**\_SEtrange SBM**</span><span class="sxs-lookup"><span data-stu-id="db2ba-130">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="db2ba-131">**\_SETRANGEREDRAW SBM**</span><span class="sxs-lookup"><span data-stu-id="db2ba-131">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

