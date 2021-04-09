---
title: Messaggio TBM_GETRANGEMIN (COMmctrl. h)
description: Recupera la posizione minima del dispositivo di scorrimento in un TrackBar.
ms.assetid: 64334aed-0403-4785-829e-693292734d10
keywords:
- Controlli di Windows Message TBM_GETRANGEMIN
topic_type:
- apiref
api_name:
- TBM_GETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddef597f7b129f8334f75136f56404a8ef117fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964252"
---
# <a name="tbm_getrangemin-message"></a><span data-ttu-id="41182-104">\_Messaggio GETRANGEMIN TBM</span><span class="sxs-lookup"><span data-stu-id="41182-104">TBM\_GETRANGEMIN message</span></span>

<span data-ttu-id="41182-105">Recupera la posizione minima del dispositivo di scorrimento in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="41182-105">Retrieves the minimum position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="41182-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41182-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41182-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41182-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="41182-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="41182-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="41182-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41182-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="41182-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="41182-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41182-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41182-111">Return value</span></span>

<span data-ttu-id="41182-112">Restituisce un valore a 32 bit che specifica la posizione minima nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="41182-112">Returns a 32-bit value that specifies the minimum position in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="41182-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41182-113">Requirements</span></span>



| <span data-ttu-id="41182-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="41182-114">Requirement</span></span> | <span data-ttu-id="41182-115">Valore</span><span class="sxs-lookup"><span data-stu-id="41182-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41182-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41182-116">Minimum supported client</span></span><br/> | <span data-ttu-id="41182-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41182-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41182-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41182-118">Minimum supported server</span></span><br/> | <span data-ttu-id="41182-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41182-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41182-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41182-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="41182-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41182-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41182-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41182-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="41182-123">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="41182-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="41182-124">**TBM \_ GETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="41182-124">**TBM\_GETRANGEMAX**</span></span>](tbm-getrangemax.md)
</dt> <dt>

[<span data-ttu-id="41182-125">**\_SEtrange TBM**</span><span class="sxs-lookup"><span data-stu-id="41182-125">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="41182-126">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="41182-126">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





