---
title: Messaggio TBM_SETRANGEMIN (COMmctrl. h)
description: Imposta la posizione logica minima per il dispositivo di scorrimento in un TrackBar.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- Controlli di Windows Message TBM_SETRANGEMIN
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34c2e70aa6247cb970e576c915bdcd28cd18d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963753"
---
# <a name="tbm_setrangemin-message"></a><span data-ttu-id="444ea-104">\_Messaggio SETRANGEMIN TBM</span><span class="sxs-lookup"><span data-stu-id="444ea-104">TBM\_SETRANGEMIN message</span></span>

<span data-ttu-id="444ea-105">Imposta la posizione logica minima per il dispositivo di scorrimento in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="444ea-105">Sets the minimum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="444ea-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="444ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="444ea-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="444ea-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="444ea-108">Ridisegni flag.</span><span class="sxs-lookup"><span data-stu-id="444ea-108">Redraw flag.</span></span> <span data-ttu-id="444ea-109">Se questo parametro è **true**, il messaggio riestrae il TrackBar dopo l'impostazione dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="444ea-109">If this parameter is **TRUE**, the message redraws the trackbar after the range is set.</span></span> <span data-ttu-id="444ea-110">Se questo parametro è **false**, il messaggio imposta l'intervallo senza ricreare il TrackBar.</span><span class="sxs-lookup"><span data-stu-id="444ea-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="444ea-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="444ea-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="444ea-112">Posizione minima del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="444ea-112">Minimum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="444ea-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="444ea-113">Return value</span></span>

<span data-ttu-id="444ea-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="444ea-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="444ea-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="444ea-115">Remarks</span></span>

<span data-ttu-id="444ea-116">Se la posizione corrente del dispositivo di scorrimento è inferiore al nuovo valore minimo, il messaggio **TBM \_ SETRANGEMIN** imposta la posizione del dispositivo di scorrimento sul nuovo valore minimo.</span><span class="sxs-lookup"><span data-stu-id="444ea-116">If the current slider position is less than the new minimum, the **TBM\_SETRANGEMIN** message sets the slider position to the new minimum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="444ea-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="444ea-117">Requirements</span></span>



| <span data-ttu-id="444ea-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="444ea-118">Requirement</span></span> | <span data-ttu-id="444ea-119">Valore</span><span class="sxs-lookup"><span data-stu-id="444ea-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="444ea-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="444ea-120">Minimum supported client</span></span><br/> | <span data-ttu-id="444ea-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="444ea-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="444ea-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="444ea-122">Minimum supported server</span></span><br/> | <span data-ttu-id="444ea-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="444ea-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="444ea-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="444ea-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="444ea-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="444ea-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="444ea-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="444ea-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="444ea-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="444ea-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="444ea-128">**\_SEtrange TBM**</span><span class="sxs-lookup"><span data-stu-id="444ea-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="444ea-129">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="444ea-129">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





