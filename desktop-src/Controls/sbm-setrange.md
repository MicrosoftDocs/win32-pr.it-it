---
title: Messaggio SBM_SETRANGE (winuser. h)
description: Il \_ messaggio SBM SEtrange viene inviato per impostare i valori di posizione minimo e massimo per il controllo barra di scorrimento.
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- Controlli di Windows Message SBM_SETRANGE
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7a720531ae58fdb0712b8f23fd1aef88b3e4caa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874421"
---
# <a name="sbm_setrange-message"></a><span data-ttu-id="247f8-104">\_Messaggio SEtrange SBM</span><span class="sxs-lookup"><span data-stu-id="247f8-104">SBM\_SETRANGE message</span></span>

<span data-ttu-id="247f8-105">Il messaggio **SBM \_ SetRange** viene inviato per impostare i valori di posizione minimo e massimo per il controllo barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="247f8-105">The **SBM\_SETRANGE** message is sent to set the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="247f8-106">Le applicazioni non devono inviare direttamente questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="247f8-106">Applications should not send this message directly.</span></span> <span data-ttu-id="247f8-107">Devono invece usare la funzione [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) .</span><span class="sxs-lookup"><span data-stu-id="247f8-107">Instead, they should use the [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) function.</span></span> <span data-ttu-id="247f8-108">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="247f8-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="247f8-109">Le applicazioni che implementano un controllo barra di scorrimento personalizzato devono rispondere a questi messaggi affinché la funzione **SetScrollRange** funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="247f8-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="247f8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="247f8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="247f8-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="247f8-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="247f8-112">Specifica la posizione di scorrimento minima.</span><span class="sxs-lookup"><span data-stu-id="247f8-112">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="247f8-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="247f8-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="247f8-114">Specifica la posizione di scorrimento massima.</span><span class="sxs-lookup"><span data-stu-id="247f8-114">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="247f8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="247f8-115">Return value</span></span>

<span data-ttu-id="247f8-116">**ComCtl32.dll versione 5,0**: se la posizione della casella di scorrimento è cambiata, il valore restituito è la posizione precedente della casella di scorrimento; in caso contrario, è zero.</span><span class="sxs-lookup"><span data-stu-id="247f8-116">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="247f8-117">**ComCtl32.dll versione 6,0**: la posizione corrente della casella di scorrimento, indipendentemente dal fatto che sia stata modificata.</span><span class="sxs-lookup"><span data-stu-id="247f8-117">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="247f8-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="247f8-118">Remarks</span></span>

<span data-ttu-id="247f8-119">I valori di posizione minima e massima predefiniti sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="247f8-119">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="247f8-120">La differenza tra i valori specificati dai parametri *wParam* e *lParam* non deve essere maggiore di MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="247f8-120">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="247f8-121">Se i valori di posizione minima e massima sono uguali, il controllo barra di scorrimento è nascosto e, in effetti, disabilitato.</span><span class="sxs-lookup"><span data-stu-id="247f8-121">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="247f8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="247f8-122">Requirements</span></span>



| <span data-ttu-id="247f8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="247f8-123">Requirement</span></span> | <span data-ttu-id="247f8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="247f8-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="247f8-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="247f8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="247f8-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="247f8-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="247f8-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="247f8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="247f8-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="247f8-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="247f8-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="247f8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="247f8-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="247f8-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="247f8-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="247f8-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="247f8-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="247f8-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="247f8-133">**\_GETPOS SBM**</span><span class="sxs-lookup"><span data-stu-id="247f8-133">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="247f8-134">**GetRange di SBM \_**</span><span class="sxs-lookup"><span data-stu-id="247f8-134">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="247f8-135">**\_SETPOS SBM**</span><span class="sxs-lookup"><span data-stu-id="247f8-135">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="247f8-136">**\_SETRANGEREDRAW SBM**</span><span class="sxs-lookup"><span data-stu-id="247f8-136">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

