---
title: Messaggio UDM_SETPOS32 (COMmctrl. h)
description: Imposta la posizione di un controllo di scorrimento con precisione a 32 bit.
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- Controlli di Windows Message UDM_SETPOS32
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0153305bb535a79dbed59e8d42a7c25157c30cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964543"
---
# <a name="udm_setpos32-message"></a><span data-ttu-id="92449-104">\_Messaggio UDM SETPOS32</span><span class="sxs-lookup"><span data-stu-id="92449-104">UDM\_SETPOS32 message</span></span>

<span data-ttu-id="92449-105">Imposta la posizione di un controllo di scorrimento con precisione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="92449-105">Sets the position of an up-down control with 32-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="92449-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="92449-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92449-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92449-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="92449-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="92449-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="92449-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92449-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92449-110">Variabile di tipo integer che specifica la nuova posizione per il controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="92449-110">Variable of type integer that specifies the new position for the up-down control.</span></span> <span data-ttu-id="92449-111">Se il parametro non è compreso nell'intervallo specificato del controllo, *lParam* viene impostato sul valore valido più vicino.</span><span class="sxs-lookup"><span data-stu-id="92449-111">If the parameter is outside the control's specified range, *lParam* is set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92449-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92449-112">Return value</span></span>

<span data-ttu-id="92449-113">Restituisce la posizione precedente.</span><span class="sxs-lookup"><span data-stu-id="92449-113">Returns the previous position.</span></span>

## <a name="requirements"></a><span data-ttu-id="92449-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92449-114">Requirements</span></span>



| <span data-ttu-id="92449-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="92449-115">Requirement</span></span> | <span data-ttu-id="92449-116">Valore</span><span class="sxs-lookup"><span data-stu-id="92449-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92449-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92449-117">Minimum supported client</span></span><br/> | <span data-ttu-id="92449-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92449-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92449-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92449-119">Minimum supported server</span></span><br/> | <span data-ttu-id="92449-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="92449-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92449-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92449-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="92449-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="92449-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92449-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92449-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="92449-124">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="92449-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="92449-125">**\_GETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="92449-125">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="92449-126">**\_SETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="92449-126">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="92449-127">**\_GETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="92449-127">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)
</dt> </dl>

 

 





