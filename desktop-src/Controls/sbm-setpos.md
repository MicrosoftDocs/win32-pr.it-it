---
title: Messaggio SBM_SETPOS (winuser. h)
description: Il \_ messaggio SETPOS SBM viene inviato per impostare la posizione della casella di scorrimento (Thumb) e, se richiesto, per ricreare la barra di scorrimento in modo da riflettere la nuova posizione della casella di scorrimento.
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- Controlli di Windows Message SBM_SETPOS
topic_type:
- apiref
api_name:
- SBM_SETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a7dc99da5f4b3dbb301f15ddd722f1d664932f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479156"
---
# <a name="sbm_setpos-message"></a><span data-ttu-id="df088-104">\_Messaggio SETPOS SBM</span><span class="sxs-lookup"><span data-stu-id="df088-104">SBM\_SETPOS message</span></span>

<span data-ttu-id="df088-105">Il **messaggio \_ SETPOS SBM** viene inviato per impostare la posizione della casella di scorrimento (Thumb) e, se richiesto, per ricreare la barra di scorrimento in modo da riflettere la nuova posizione della casella di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="df088-105">The **SBM\_SETPOS** message is sent to set the position of the scroll box (thumb) and, if requested, redraw the scroll bar to reflect the new position of the scroll box.</span></span>

<span data-ttu-id="df088-106">Le applicazioni non devono inviare direttamente questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="df088-106">Applications should not send this message directly.</span></span> <span data-ttu-id="df088-107">Devono invece usare la funzione [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="df088-107">Instead, they should use the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span> <span data-ttu-id="df088-108">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="df088-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="df088-109">Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **SetScrollPos** funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="df088-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollPos** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="df088-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="df088-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df088-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df088-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df088-112">Specifica la nuova posizione della casella di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="df088-112">Specifies the new position of the scroll box.</span></span> <span data-ttu-id="df088-113">Deve trovarsi all'interno dell'intervallo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="df088-113">It must be within the scrolling range.</span></span> <span data-ttu-id="df088-114">Se questo parametro è esterno all'intervallo di scorrimento, il valore viene arrotondato per eccesso o per difetto al valore valido più vicino.</span><span class="sxs-lookup"><span data-stu-id="df088-114">If this parameter is outside of the scrolling range, the value is rounded up or down to the nearest valid value.</span></span>

</dd> <dt>

<span data-ttu-id="df088-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df088-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df088-116">Specifica se la barra di scorrimento deve essere ridisegnato per riflettere la nuova posizione della casella di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="df088-116">Specifies whether the scroll bar should be redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="df088-117">Se questo parametro è **true**, la barra di scorrimento viene ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="df088-117">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="df088-118">Se è **false**, la barra di scorrimento non viene ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="df088-118">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df088-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df088-119">Return value</span></span>

<span data-ttu-id="df088-120">**ComCtl32.dll versione 5,0**: se la posizione della casella di scorrimento è cambiata, il valore restituito è la posizione precedente della casella di scorrimento; in caso contrario, è zero.</span><span class="sxs-lookup"><span data-stu-id="df088-120">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="df088-121">**ComCtl32.dll versione 6,0**: la posizione corrente della casella di scorrimento, indipendentemente dal fatto che sia stata modificata.</span><span class="sxs-lookup"><span data-stu-id="df088-121">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="df088-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="df088-122">Remarks</span></span>

<span data-ttu-id="df088-123">Se il controllo barra di scorrimento viene ridisegnato da una chiamata successiva a un'altra funzione, l'impostazione del parametro *lParam* su **false** è utile.</span><span class="sxs-lookup"><span data-stu-id="df088-123">If the scroll bar control is redrawn by a subsequent call to another function, setting the *lParam* parameter to **FALSE** is useful.</span></span>

## <a name="requirements"></a><span data-ttu-id="df088-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df088-124">Requirements</span></span>



| <span data-ttu-id="df088-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="df088-125">Requirement</span></span> | <span data-ttu-id="df088-126">Valore</span><span class="sxs-lookup"><span data-stu-id="df088-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df088-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df088-127">Minimum supported client</span></span><br/> | <span data-ttu-id="df088-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df088-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="df088-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df088-129">Minimum supported server</span></span><br/> | <span data-ttu-id="df088-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="df088-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="df088-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df088-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="df088-132"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df088-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df088-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df088-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="df088-134">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="df088-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="df088-135">**\_GETPOS SBM**</span><span class="sxs-lookup"><span data-stu-id="df088-135">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="df088-136">**GetRange di SBM \_**</span><span class="sxs-lookup"><span data-stu-id="df088-136">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="df088-137">**\_SEtrange SBM**</span><span class="sxs-lookup"><span data-stu-id="df088-137">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="df088-138">**\_SETRANGEREDRAW SBM**</span><span class="sxs-lookup"><span data-stu-id="df088-138">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

