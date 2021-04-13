---
title: Messaggio TBM_SETRANGEMAX (COMmctrl. h)
description: Imposta la posizione logica massima per il dispositivo di scorrimento in un TrackBar.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- Controlli di Windows Message TBM_SETRANGEMAX
topic_type:
- apiref
api_name:
- TBM_SETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43997725e2fa88db3f9d4dc2fec1d51255cbb0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475136"
---
# <a name="tbm_setrangemax-message"></a><span data-ttu-id="4a78c-104">\_Messaggio SETRANGEMAX TBM</span><span class="sxs-lookup"><span data-stu-id="4a78c-104">TBM\_SETRANGEMAX message</span></span>

<span data-ttu-id="4a78c-105">Imposta la posizione logica massima per il dispositivo di scorrimento in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="4a78c-105">Sets the maximum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a78c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a78c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a78c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a78c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a78c-108">Ridisegni flag.</span><span class="sxs-lookup"><span data-stu-id="4a78c-108">Redraw flag.</span></span> <span data-ttu-id="4a78c-109">Se questo parametro è **true**, il TrackBar viene ridisegnato dopo l'impostazione dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="4a78c-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="4a78c-110">Se questo parametro è **false**, il messaggio imposta l'intervallo senza ricreare il TrackBar.</span><span class="sxs-lookup"><span data-stu-id="4a78c-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="4a78c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a78c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a78c-112">Posizione massima del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4a78c-112">Maximum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a78c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a78c-113">Return value</span></span>

<span data-ttu-id="4a78c-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="4a78c-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a78c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a78c-115">Remarks</span></span>

<span data-ttu-id="4a78c-116">Se la posizione corrente del dispositivo di scorrimento è maggiore del nuovo valore massimo, il messaggio **TBM \_ SETRANGEMAX** imposta la posizione del dispositivo di scorrimento sul nuovo valore massimo.</span><span class="sxs-lookup"><span data-stu-id="4a78c-116">If the current slider position is greater than the new maximum, the **TBM\_SETRANGEMAX** message sets the slider position to the new maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a78c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a78c-117">Requirements</span></span>



| <span data-ttu-id="4a78c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a78c-118">Requirement</span></span> | <span data-ttu-id="4a78c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4a78c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a78c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a78c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4a78c-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a78c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a78c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a78c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4a78c-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4a78c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a78c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a78c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a78c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a78c-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a78c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a78c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="4a78c-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4a78c-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4a78c-128">**\_SEtrange TBM**</span><span class="sxs-lookup"><span data-stu-id="4a78c-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="4a78c-129">**TBM \_ SETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="4a78c-129">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 

 





