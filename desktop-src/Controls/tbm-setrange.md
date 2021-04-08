---
title: Messaggio TBM_SETRANGE (COMmctrl. h)
description: Imposta l'intervallo di posizioni logiche minime e massime per il dispositivo di scorrimento in un TrackBar.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- Controlli di Windows Message TBM_SETRANGE
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d870df628b06031374260c679f792f0b7218a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048115"
---
# <a name="tbm_setrange-message"></a><span data-ttu-id="22d9d-104">\_Messaggio SEtrange TBM</span><span class="sxs-lookup"><span data-stu-id="22d9d-104">TBM\_SETRANGE message</span></span>

<span data-ttu-id="22d9d-105">Imposta l'intervallo di posizioni logiche minime e massime per il dispositivo di scorrimento in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="22d9d-105">Sets the range of minimum and maximum logical positions for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="22d9d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="22d9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22d9d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22d9d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22d9d-108">Ridisegni flag.</span><span class="sxs-lookup"><span data-stu-id="22d9d-108">Redraw flag.</span></span> <span data-ttu-id="22d9d-109">Se questo parametro è **true**, il TrackBar viene ridisegnato dopo l'impostazione dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="22d9d-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="22d9d-110">Se questo parametro è **false**, il messaggio imposta l'intervallo senza ricreare il TrackBar.</span><span class="sxs-lookup"><span data-stu-id="22d9d-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="22d9d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22d9d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22d9d-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la posizione minima per il dispositivo di scorrimento e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione massima.</span><span class="sxs-lookup"><span data-stu-id="22d9d-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum position for the slider, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22d9d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22d9d-113">Return value</span></span>

<span data-ttu-id="22d9d-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="22d9d-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22d9d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="22d9d-115">Remarks</span></span>

<span data-ttu-id="22d9d-116">Se la posizione corrente del dispositivo di scorrimento non rientra nel nuovo intervallo, il messaggio di **\_ SetRange TBM** imposta la posizione del dispositivo di scorrimento sul nuovo valore massimo o minimo.</span><span class="sxs-lookup"><span data-stu-id="22d9d-116">If the current slider position is outside the new range, the **TBM\_SETRANGE** message sets the slider position to the new maximum or minimum value.</span></span>

<span data-ttu-id="22d9d-117">Poiché questo messaggio accetta valori Unsigned Integer a 2 16 bit, l'intervallo massimo che questo messaggio può specificare è compreso tra 0 e 65.535.</span><span class="sxs-lookup"><span data-stu-id="22d9d-117">Because this message takes two 16-bit unsigned integer values, the maximum range that this message can specify is from 0 to 65,535.</span></span> <span data-ttu-id="22d9d-118">Per specificare valori di intervallo maggiori, usare i messaggi [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md) e [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md) .</span><span class="sxs-lookup"><span data-stu-id="22d9d-118">To specify larger range values, use the [**TBM\_SETRANGEMIN**](tbm-setrangemin.md) and [**TBM\_SETRANGEMAX**](tbm-setrangemax.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="22d9d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22d9d-119">Requirements</span></span>



| <span data-ttu-id="22d9d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="22d9d-120">Requirement</span></span> | <span data-ttu-id="22d9d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="22d9d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22d9d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22d9d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="22d9d-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22d9d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22d9d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22d9d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="22d9d-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="22d9d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22d9d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22d9d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="22d9d-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="22d9d-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22d9d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22d9d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="22d9d-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="22d9d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="22d9d-130">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="22d9d-130">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> <dt>

[<span data-ttu-id="22d9d-131">**TBM \_ SETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="22d9d-131">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 

