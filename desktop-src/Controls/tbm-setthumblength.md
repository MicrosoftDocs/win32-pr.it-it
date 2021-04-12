---
title: Messaggio TBM_SETTHUMBLENGTH (COMmctrl. h)
description: Imposta la lunghezza del dispositivo di scorrimento in un TrackBar. Questo messaggio viene ignorato se il TrackBar non ha lo \_ stile FIXEDLENGTH di TBS.
ms.assetid: 027fe341-a60a-4dbe-a48a-5ddaadef0b4a
keywords:
- Controlli di Windows Message TBM_SETTHUMBLENGTH
topic_type:
- apiref
api_name:
- TBM_SETTHUMBLENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d4ac33d2df43a267766e14ab95fb9729692bbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518741"
---
# <a name="tbm_setthumblength-message"></a><span data-ttu-id="5af59-105">\_Messaggio SETTHUMBLENGTH TBM</span><span class="sxs-lookup"><span data-stu-id="5af59-105">TBM\_SETTHUMBLENGTH message</span></span>

<span data-ttu-id="5af59-106">Imposta la lunghezza del dispositivo di scorrimento in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="5af59-106">Sets the length of the slider in a trackbar.</span></span> <span data-ttu-id="5af59-107">Questo messaggio viene ignorato se il TrackBar non ha lo stile [**\_ FIXEDLENGTH di TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5af59-107">This message is ignored if the trackbar does not have the [**TBS\_FIXEDLENGTH**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="5af59-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5af59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5af59-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5af59-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5af59-110">Lunghezza, in pixel, del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="5af59-110">Length, in pixels, of the slider.</span></span>

</dd> <dt>

<span data-ttu-id="5af59-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5af59-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5af59-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5af59-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5af59-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5af59-113">Return value</span></span>

<span data-ttu-id="5af59-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="5af59-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5af59-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5af59-115">Requirements</span></span>



| <span data-ttu-id="5af59-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5af59-116">Requirement</span></span> | <span data-ttu-id="5af59-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5af59-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5af59-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5af59-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5af59-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5af59-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5af59-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5af59-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5af59-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5af59-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5af59-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5af59-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5af59-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5af59-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5af59-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5af59-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af59-125">**TBM \_ GETTHUMBLENGTH**</span><span class="sxs-lookup"><span data-stu-id="5af59-125">**TBM\_GETTHUMBLENGTH**</span></span>](tbm-getthumblength.md)
</dt> </dl>

 

 





