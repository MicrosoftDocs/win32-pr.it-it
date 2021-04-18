---
title: Messaggio UDM_GETPOS (COMmctrl. h)
description: Recupera la posizione corrente di un controllo di scorrimento con precisione a 16 bit.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- Controlli di Windows Message UDM_GETPOS
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e78ad19289d85b93ebcb39a244a896ddb4f33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301174"
---
# <a name="udm_getpos-message"></a><span data-ttu-id="c8594-104">\_Messaggio UDM GETPOS</span><span class="sxs-lookup"><span data-stu-id="c8594-104">UDM\_GETPOS message</span></span>

<span data-ttu-id="c8594-105">Recupera la posizione corrente di un controllo di scorrimento con precisione a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="c8594-105">Retrieves the current position of an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8594-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8594-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8594-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8594-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c8594-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c8594-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c8594-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8594-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c8594-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c8594-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8594-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8594-111">Return value</span></span>

<span data-ttu-id="c8594-112">Se ha esito positivo, [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è impostato su zero e [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è impostato sulla posizione corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="c8594-112">If successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is set to zero and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is set to the control's current position.</span></span> <span data-ttu-id="c8594-113">Se si verifica un errore, **HIWORD** viene impostato su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c8594-113">If an error occurs, the **HIWORD** is set to a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8594-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8594-114">Remarks</span></span>

<span data-ttu-id="c8594-115">Durante l'elaborazione di questo messaggio, il controllo di scorrimento aggiorna la posizione corrente in base alla didascalia della finestra di Buddy.</span><span class="sxs-lookup"><span data-stu-id="c8594-115">When processing this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="c8594-116">Il controllo di scorrimento restituisce un errore se non è presente alcuna finestra di Buddy o se la didascalia specifica un valore non valido o non compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="c8594-116">The up-down control returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span> <span data-ttu-id="c8594-117">Inoltre, un flag di errore viene impostato nel HIWORD della restituzione se il controllo viene creato senza lo [**stile \_ SETBUDDYINT di UDS**](up-down-control-styles.md) , anche se restituisce un valore di posizione valido nel LOWORD della restituzione.</span><span class="sxs-lookup"><span data-stu-id="c8594-117">Also, an error flag is set in the HIWORD of the return if the control is created without the [**UDS\_SETBUDDYINT**](up-down-control-styles.md) style, even though it returns a valid position value in the LOWORD of the return.</span></span>

<span data-ttu-id="c8594-118">Se sono stati abilitati i valori a 32 bit per un controllo di scorrimento con [**UDM \_ SETRANGE32**](udm-setrange32.md), questo messaggio restituisce solo i 16 bit inferiori della posizione.</span><span class="sxs-lookup"><span data-stu-id="c8594-118">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), this message returns only the lower 16 bits of the position.</span></span> <span data-ttu-id="c8594-119">Per recuperare la posizione completa a 32 bit, usare [**UDM \_ GETPOS32**](udm-getpos32.md).</span><span class="sxs-lookup"><span data-stu-id="c8594-119">To retrieve the full 32-bit position, use [**UDM\_GETPOS32**](udm-getpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8594-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8594-120">Requirements</span></span>



| <span data-ttu-id="c8594-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8594-121">Requirement</span></span> | <span data-ttu-id="c8594-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c8594-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8594-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8594-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c8594-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8594-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8594-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8594-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c8594-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c8594-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8594-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8594-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8594-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8594-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8594-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8594-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8594-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c8594-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c8594-131">**UDM \_ GETrange**</span><span class="sxs-lookup"><span data-stu-id="c8594-131">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="c8594-132">**\_GETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="c8594-132">**UDM\_GETRANGE32**</span></span>](udm-getrange32.md)
</dt> <dt>

[<span data-ttu-id="c8594-133">**\_SETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="c8594-133">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="c8594-134">**\_SETRANGE32 UDM**</span><span class="sxs-lookup"><span data-stu-id="c8594-134">**UDM\_SETRANGE32**</span></span>](udm-setrange32.md)
</dt> </dl>

 

