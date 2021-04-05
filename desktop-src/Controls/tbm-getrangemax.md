---
title: Messaggio TBM_GETRANGEMAX (COMmctrl. h)
description: Recupera la posizione massima per il dispositivo di scorrimento in un TrackBar.
ms.assetid: c0ae5f96-f4ce-46cd-84d0-9e7c473441a0
keywords:
- Controlli di Windows Message TBM_GETRANGEMAX
topic_type:
- apiref
api_name:
- TBM_GETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bdd9687b617759ab8b8fdea59ed06d7fcd78b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048392"
---
# <a name="tbm_getrangemax-message"></a><span data-ttu-id="119b6-104">\_Messaggio GETRANGEMAX TBM</span><span class="sxs-lookup"><span data-stu-id="119b6-104">TBM\_GETRANGEMAX message</span></span>

<span data-ttu-id="119b6-105">Recupera la posizione massima per il dispositivo di scorrimento in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="119b6-105">Retrieves the maximum position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="119b6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="119b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="119b6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="119b6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="119b6-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="119b6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="119b6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="119b6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="119b6-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="119b6-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="119b6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="119b6-111">Return value</span></span>

<span data-ttu-id="119b6-112">Restituisce un valore a 32 bit che specifica la posizione massima nell'intervallo compreso tra minimo e massimo del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="119b6-112">Returns a 32-bit value that specifies the maximum position in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="119b6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="119b6-113">Requirements</span></span>



| <span data-ttu-id="119b6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="119b6-114">Requirement</span></span> | <span data-ttu-id="119b6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="119b6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="119b6-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="119b6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="119b6-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="119b6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="119b6-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="119b6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="119b6-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="119b6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="119b6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="119b6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="119b6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="119b6-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="119b6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="119b6-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="119b6-123">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="119b6-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="119b6-124">**TBM \_ GETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="119b6-124">**TBM\_GETRANGEMIN**</span></span>](tbm-getrangemin.md)
</dt> <dt>

[<span data-ttu-id="119b6-125">**\_SEtrange TBM**</span><span class="sxs-lookup"><span data-stu-id="119b6-125">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="119b6-126">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="119b6-126">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





