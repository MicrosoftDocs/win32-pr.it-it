---
title: Messaggio SBM_SETRANGEREDRAW (winuser. h)
description: Un'applicazione invia il \_ messaggio SETRANGEREDRAW SBM a un controllo barra di scorrimento per impostare i valori minimo e massimo della posizione e per ricreare il controllo.
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- Controlli di Windows Message SBM_SETRANGEREDRAW
topic_type:
- apiref
api_name:
- SBM_SETRANGEREDRAW
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37c77a8f062ba3c7a8b73adc4338a11cdcf59442
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047846"
---
# <a name="sbm_setrangeredraw-message"></a><span data-ttu-id="b22ad-104">\_Messaggio SETRANGEREDRAW SBM</span><span class="sxs-lookup"><span data-stu-id="b22ad-104">SBM\_SETRANGEREDRAW message</span></span>

<span data-ttu-id="b22ad-105">Un'applicazione invia il **messaggio \_ SETRANGEREDRAW SBM** a un controllo barra di scorrimento per impostare i valori minimo e massimo della posizione e per ricreare il controllo.</span><span class="sxs-lookup"><span data-stu-id="b22ad-105">An application sends the **SBM\_SETRANGEREDRAW** message to a scroll bar control to set the minimum and maximum position values and to redraw the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b22ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b22ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b22ad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b22ad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b22ad-108">Specifica la posizione di scorrimento minima.</span><span class="sxs-lookup"><span data-stu-id="b22ad-108">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="b22ad-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b22ad-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b22ad-110">Specifica la posizione di scorrimento massima.</span><span class="sxs-lookup"><span data-stu-id="b22ad-110">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b22ad-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b22ad-111">Return value</span></span>

<span data-ttu-id="b22ad-112">**ComCtl32.dll versione 5,0**: se la posizione della casella di scorrimento è cambiata, il valore restituito è la posizione precedente della casella di scorrimento; in caso contrario, è zero.</span><span class="sxs-lookup"><span data-stu-id="b22ad-112">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="b22ad-113">**ComCtl32.dll versione 6,0**: la posizione corrente della casella di scorrimento, indipendentemente dal fatto che sia stata modificata.</span><span class="sxs-lookup"><span data-stu-id="b22ad-113">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="b22ad-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b22ad-114">Remarks</span></span>

<span data-ttu-id="b22ad-115">I valori di posizione minima e massima predefiniti sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="b22ad-115">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="b22ad-116">La differenza tra i valori specificati dai parametri *wParam* e *lParam* non deve essere maggiore di MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="b22ad-116">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="b22ad-117">Se i valori di posizione minima e massima sono uguali, il controllo barra di scorrimento è nascosto e, in effetti, disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b22ad-117">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="b22ad-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b22ad-118">Requirements</span></span>



| <span data-ttu-id="b22ad-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b22ad-119">Requirement</span></span> | <span data-ttu-id="b22ad-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b22ad-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b22ad-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b22ad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b22ad-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b22ad-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b22ad-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b22ad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b22ad-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b22ad-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b22ad-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b22ad-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b22ad-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b22ad-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b22ad-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b22ad-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b22ad-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b22ad-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b22ad-129">**\_GETPOS SBM**</span><span class="sxs-lookup"><span data-stu-id="b22ad-129">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="b22ad-130">**GetRange di SBM \_**</span><span class="sxs-lookup"><span data-stu-id="b22ad-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="b22ad-131">**\_SETPOS SBM**</span><span class="sxs-lookup"><span data-stu-id="b22ad-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="b22ad-132">**\_SEtrange SBM**</span><span class="sxs-lookup"><span data-stu-id="b22ad-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> </dl>

 

 





