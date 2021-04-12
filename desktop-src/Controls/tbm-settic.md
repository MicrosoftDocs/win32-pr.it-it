---
title: Messaggio TBM_SETTIC (COMmctrl. h)
description: Imposta un segno di graduazione in un TrackBar nella posizione logica specificata.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- Controlli di Windows Message TBM_SETTIC
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119327"
---
# <a name="tbm_settic-message"></a><span data-ttu-id="846d8-104">\_Messaggio SETTIC TBM</span><span class="sxs-lookup"><span data-stu-id="846d8-104">TBM\_SETTIC message</span></span>

<span data-ttu-id="846d8-105">Imposta un segno di graduazione in un TrackBar nella posizione logica specificata.</span><span class="sxs-lookup"><span data-stu-id="846d8-105">Sets a tick mark in a trackbar at the specified logical position.</span></span>

## <a name="parameters"></a><span data-ttu-id="846d8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="846d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="846d8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="846d8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="846d8-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="846d8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="846d8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="846d8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="846d8-110">Posizione del segno di graduazione.</span><span class="sxs-lookup"><span data-stu-id="846d8-110">Position of the tick mark.</span></span> <span data-ttu-id="846d8-111">Questo parametro può essere uno qualsiasi dei valori integer nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="846d8-111">This parameter can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="846d8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="846d8-112">Return value</span></span>

<span data-ttu-id="846d8-113">Restituisce **true** se il segno di graduazione è impostato o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="846d8-113">Returns **TRUE** if the tick mark is set, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="846d8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="846d8-114">Remarks</span></span>

<span data-ttu-id="846d8-115">Un TrackBar crea il proprio primo e l'ultimo segno di graduazione.</span><span class="sxs-lookup"><span data-stu-id="846d8-115">A trackbar creates its own first and last tick marks.</span></span> <span data-ttu-id="846d8-116">Non utilizzare questo messaggio per impostare il primo e l'ultimo segno di graduazione.</span><span class="sxs-lookup"><span data-stu-id="846d8-116">Do not use this message to set the first and last tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="846d8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="846d8-117">Requirements</span></span>



| <span data-ttu-id="846d8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="846d8-118">Requirement</span></span> | <span data-ttu-id="846d8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="846d8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="846d8-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="846d8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="846d8-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="846d8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="846d8-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="846d8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="846d8-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="846d8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="846d8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="846d8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="846d8-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="846d8-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="846d8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="846d8-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="846d8-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="846d8-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="846d8-128">**TBM \_ GETPTICS**</span><span class="sxs-lookup"><span data-stu-id="846d8-128">**TBM\_GETPTICS**</span></span>](tbm-getptics.md)
</dt> <dt>

[<span data-ttu-id="846d8-129">**\_Getter TBM**</span><span class="sxs-lookup"><span data-stu-id="846d8-129">**TBM\_GETTIC**</span></span>](tbm-gettic.md)
</dt> </dl>

 

 





