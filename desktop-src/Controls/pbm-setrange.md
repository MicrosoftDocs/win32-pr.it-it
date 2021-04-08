---
title: Messaggio PBM_SETRANGE (COMmctrl. h)
description: Imposta i valori minimo e massimo per un indicatore di stato e ridisegnato la barra in modo da riflettere il nuovo intervallo.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- Controlli di Windows Message PBM_SETRANGE
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e588170c80378082eab7e419e9425e716b8caf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874157"
---
# <a name="pbm_setrange-message"></a><span data-ttu-id="aff9e-104">\_Messaggio SEtrange PBM</span><span class="sxs-lookup"><span data-stu-id="aff9e-104">PBM\_SETRANGE message</span></span>

<span data-ttu-id="aff9e-105">Imposta i valori minimo e massimo per un indicatore di stato e ridisegnato la barra in modo da riflettere il nuovo intervallo.</span><span class="sxs-lookup"><span data-stu-id="aff9e-105">Sets the minimum and maximum values for a progress bar and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="aff9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aff9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aff9e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aff9e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aff9e-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="aff9e-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="aff9e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aff9e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aff9e-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il valore di intervallo minimo e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il valore di intervallo massimo.</span><span class="sxs-lookup"><span data-stu-id="aff9e-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum range value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum range value.</span></span> <span data-ttu-id="aff9e-111">Il valore minimo dell'intervallo non deve essere negativo.</span><span class="sxs-lookup"><span data-stu-id="aff9e-111">The minimum range value must not be negative.</span></span> <span data-ttu-id="aff9e-112">Per impostazione predefinita, il valore minimo è zero.</span><span class="sxs-lookup"><span data-stu-id="aff9e-112">By default, the minimum value is zero.</span></span> <span data-ttu-id="aff9e-113">Il valore di intervallo massimo deve essere maggiore del valore di intervallo minimo.</span><span class="sxs-lookup"><span data-stu-id="aff9e-113">The maximum range value must be greater than the minimum range value.</span></span> <span data-ttu-id="aff9e-114">Per impostazione predefinita, il valore di intervallo massimo è 100.</span><span class="sxs-lookup"><span data-stu-id="aff9e-114">By default, the maximum range value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aff9e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aff9e-115">Return value</span></span>

<span data-ttu-id="aff9e-116">Restituisce i valori di intervallo precedenti se l'operazione ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="aff9e-116">Returns the previous range values if successful, or zero otherwise.</span></span> <span data-ttu-id="aff9e-117">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il valore minimo precedente e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il valore massimo precedente.</span><span class="sxs-lookup"><span data-stu-id="aff9e-117">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the previous minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the previous maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aff9e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="aff9e-118">Remarks</span></span>

<span data-ttu-id="aff9e-119">Se non si impostano i valori di intervallo, il sistema imposta il valore minimo su 0 e il valore massimo su 100.</span><span class="sxs-lookup"><span data-stu-id="aff9e-119">If you do not set the range values, the system sets the minimum value to 0 and the maximum value to 100.</span></span> <span data-ttu-id="aff9e-120">Poiché questo messaggio esprime l'intervallo come Unsigned Integer a 16 bit, può estendersi da 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="aff9e-120">Because this message expresses the range as a 16-bit unsigned integer, it can extend from 0 to 65,535.</span></span> <span data-ttu-id="aff9e-121">Il valore minimo nell'intervallo può essere compreso tra 0 e 65.535.</span><span class="sxs-lookup"><span data-stu-id="aff9e-121">The minimum value in the range can be from 0 to 65,535.</span></span> <span data-ttu-id="aff9e-122">Analogamente, il valore massimo può essere compreso tra 0 e 65.535.</span><span class="sxs-lookup"><span data-stu-id="aff9e-122">Likewise, the maximum value can be from 0 to 65,535.</span></span>

<span data-ttu-id="aff9e-123">Per impostare un intervallo più ampio, chiamare [**PBM \_ SETRANGE32**](pbm-setrange32.md).</span><span class="sxs-lookup"><span data-stu-id="aff9e-123">To set a larger range, call [**PBM\_SETRANGE32**](pbm-setrange32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aff9e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aff9e-124">Requirements</span></span>



| <span data-ttu-id="aff9e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="aff9e-125">Requirement</span></span> | <span data-ttu-id="aff9e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="aff9e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aff9e-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aff9e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="aff9e-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aff9e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aff9e-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aff9e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="aff9e-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aff9e-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aff9e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aff9e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="aff9e-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff9e-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff9e-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aff9e-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="aff9e-134">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="aff9e-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aff9e-135">**GetRange PBM \_**</span><span class="sxs-lookup"><span data-stu-id="aff9e-135">**PBM\_GETRANGE**</span></span>](pbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="aff9e-136">**\_SETRANGE32 PBM**</span><span class="sxs-lookup"><span data-stu-id="aff9e-136">**PBM\_SETRANGE32**</span></span>](pbm-setrange32.md)
</dt> </dl>

 

