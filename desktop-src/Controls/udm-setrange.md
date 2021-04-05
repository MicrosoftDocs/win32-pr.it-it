---
title: Messaggio UDM_SETRANGE (COMmctrl. h)
description: Imposta le posizioni minime e massime (intervallo) per un controllo di scorrimento.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- Controlli di Windows Message UDM_SETRANGE
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb32a72ca8ca5182e87e2c0346cbc44ab25300e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048543"
---
# <a name="udm_setrange-message"></a><span data-ttu-id="59ac0-104">\_Messaggio SEtrange UDM</span><span class="sxs-lookup"><span data-stu-id="59ac0-104">UDM\_SETRANGE message</span></span>

<span data-ttu-id="59ac0-105">Imposta le posizioni minime e massime (intervallo) per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="59ac0-105">Sets the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="59ac0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="59ac0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59ac0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59ac0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="59ac0-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="59ac0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="59ac0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59ac0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59ac0-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **short** che specifica la posizione massima per il controllo di scorrimento e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è un valore **short** che specifica la posizione minima.</span><span class="sxs-lookup"><span data-stu-id="59ac0-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **short** that specifies the maximum position for the up-down control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **short** that specifies the minimum position.</span></span> <span data-ttu-id="59ac0-111">La posizione non può essere maggiore del \_ valore MaxVal di UD o minore del \_ valore MINVAL di UD.</span><span class="sxs-lookup"><span data-stu-id="59ac0-111">Neither position can be greater than the UD\_MAXVAL value or less than the UD\_MINVAL value.</span></span> <span data-ttu-id="59ac0-112">Inoltre, la differenza tra le due posizioni non può superare il \_ MaxVal UD.</span><span class="sxs-lookup"><span data-stu-id="59ac0-112">In addition, the difference between the two positions cannot exceed UD\_MAXVAL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59ac0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59ac0-113">Return value</span></span>

<span data-ttu-id="59ac0-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="59ac0-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59ac0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="59ac0-115">Remarks</span></span>

<span data-ttu-id="59ac0-116">La posizione massima può essere minore della posizione minima.</span><span class="sxs-lookup"><span data-stu-id="59ac0-116">The maximum position can be less than the minimum position.</span></span> <span data-ttu-id="59ac0-117">Facendo clic sul pulsante freccia su viene spostata la posizione corrente più vicina alla posizione massima e facendo clic sul pulsante freccia giù si sposta verso la posizione minima.</span><span class="sxs-lookup"><span data-stu-id="59ac0-117">Clicking the up arrow button moves the current position closer to the maximum position, and clicking the down arrow button moves toward the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ac0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59ac0-118">Requirements</span></span>



| <span data-ttu-id="59ac0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="59ac0-119">Requirement</span></span> | <span data-ttu-id="59ac0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="59ac0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59ac0-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59ac0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="59ac0-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59ac0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59ac0-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59ac0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="59ac0-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59ac0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59ac0-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59ac0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="59ac0-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="59ac0-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59ac0-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59ac0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ac0-128">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="59ac0-128">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="59ac0-129">**\_SEtrange UDM**</span><span class="sxs-lookup"><span data-stu-id="59ac0-129">**UDM\_SETRANGE**</span></span>](udm-setrange.md)
</dt> </dl>

 

