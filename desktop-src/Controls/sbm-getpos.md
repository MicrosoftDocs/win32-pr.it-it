---
title: Messaggio SBM_GETPOS (winuser. h)
description: Il \_ messaggio GETPOS SBM viene inviato per recuperare la posizione corrente della casella di scorrimento di un controllo barra di scorrimento.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- Controlli di Windows Message SBM_GETPOS
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d088fc790985e57928f1ab56cd42254b1a087dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964633"
---
# <a name="sbm_getpos-message"></a><span data-ttu-id="78d80-104">\_Messaggio GETPOS SBM</span><span class="sxs-lookup"><span data-stu-id="78d80-104">SBM\_GETPOS message</span></span>

<span data-ttu-id="78d80-105">Il **messaggio \_ GETPOS SBM** viene inviato per recuperare la posizione corrente della casella di scorrimento di un controllo barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="78d80-105">The **SBM\_GETPOS** message is sent to retrieve the current position of the scroll box of a scroll bar control.</span></span> <span data-ttu-id="78d80-106">La posizione corrente è un valore relativo che dipende dall'intervallo di scorrimento corrente.</span><span class="sxs-lookup"><span data-stu-id="78d80-106">The current position is a relative value that depends on the current scrolling range.</span></span> <span data-ttu-id="78d80-107">Se, ad esempio, l'intervallo di scorrimento è compreso tra 0 e 100 e la casella di scorrimento si trova al centro della barra, la posizione corrente è 50.</span><span class="sxs-lookup"><span data-stu-id="78d80-107">For example, if the scrolling range is 0 through 100 and the scroll box is in the middle of the bar, the current position is 50.</span></span>

<span data-ttu-id="78d80-108">Le applicazioni non devono inviare direttamente questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="78d80-108">Applications should not send this message directly.</span></span> <span data-ttu-id="78d80-109">Devono invece usare la funzione [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="78d80-109">Instead, they should use the [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) function.</span></span> <span data-ttu-id="78d80-110">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="78d80-110">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="78d80-111">Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **GetScrollPos** funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="78d80-111">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollPos** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="78d80-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="78d80-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78d80-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78d80-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78d80-114">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="78d80-114">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="78d80-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78d80-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78d80-116">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="78d80-116">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78d80-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78d80-117">Return value</span></span>

<span data-ttu-id="78d80-118">Il valore restituito è la posizione corrente della casella di scorrimento nella barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="78d80-118">The return value is the current position of the scroll box in the scroll bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="78d80-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78d80-119">Requirements</span></span>



| <span data-ttu-id="78d80-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="78d80-120">Requirement</span></span> | <span data-ttu-id="78d80-121">Valore</span><span class="sxs-lookup"><span data-stu-id="78d80-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78d80-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78d80-122">Minimum supported client</span></span><br/> | <span data-ttu-id="78d80-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78d80-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="78d80-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78d80-124">Minimum supported server</span></span><br/> | <span data-ttu-id="78d80-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78d80-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="78d80-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78d80-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="78d80-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78d80-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78d80-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78d80-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="78d80-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="78d80-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="78d80-130">**GetRange di SBM \_**</span><span class="sxs-lookup"><span data-stu-id="78d80-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="78d80-131">**\_SETPOS SBM**</span><span class="sxs-lookup"><span data-stu-id="78d80-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="78d80-132">**\_SEtrange SBM**</span><span class="sxs-lookup"><span data-stu-id="78d80-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="78d80-133">**\_SETRANGEREDRAW SBM**</span><span class="sxs-lookup"><span data-stu-id="78d80-133">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

