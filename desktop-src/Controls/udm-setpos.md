---
title: Messaggio UDM_SETPOS (COMmctrl. h)
description: Imposta la posizione corrente per un controllo di scorrimento con precisione a 16 bit.
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- Controlli di Windows Message UDM_SETPOS
topic_type:
- apiref
api_name:
- UDM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b409f9e7468e3add89248b61b7b563ac592f0dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120491"
---
# <a name="udm_setpos-message"></a><span data-ttu-id="7e2fa-104">\_Messaggio UDM SETPOS</span><span class="sxs-lookup"><span data-stu-id="7e2fa-104">UDM\_SETPOS message</span></span>

<span data-ttu-id="7e2fa-105">Imposta la posizione corrente per un controllo di scorrimento con precisione a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="7e2fa-105">Sets the current position for an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e2fa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e2fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e2fa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e2fa-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7e2fa-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7e2fa-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7e2fa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e2fa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e2fa-110">Nuova posizione per il controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="7e2fa-110">New position for the up-down control.</span></span> <span data-ttu-id="7e2fa-111">Se il parametro non è compreso nell'intervallo specificato del controllo, *lParam* verrà impostato sul valore valido più vicino.</span><span class="sxs-lookup"><span data-stu-id="7e2fa-111">If the parameter is outside the control's specified range, *lParam* will be set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e2fa-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e2fa-112">Return value</span></span>

<span data-ttu-id="7e2fa-113">Il valore restituito è la posizione precedente.</span><span class="sxs-lookup"><span data-stu-id="7e2fa-113">The return value is the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e2fa-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e2fa-114">Remarks</span></span>

<span data-ttu-id="7e2fa-115">Questo messaggio supporta solo posizioni a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="7e2fa-115">This message only supports 16-bit positions.</span></span> <span data-ttu-id="7e2fa-116">Se sono stati abilitati i valori a 32 bit per un controllo di scorrimento con [**UDM \_ SETRANGE32**](udm-setrange32.md), usare [**UDM \_ SETPOS32**](udm-setpos32.md).</span><span class="sxs-lookup"><span data-stu-id="7e2fa-116">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), use [**UDM\_SETPOS32**](udm-setpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e2fa-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e2fa-117">Requirements</span></span>



| <span data-ttu-id="7e2fa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e2fa-118">Requirement</span></span> | <span data-ttu-id="7e2fa-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7e2fa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e2fa-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e2fa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7e2fa-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e2fa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e2fa-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e2fa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7e2fa-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7e2fa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e2fa-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e2fa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e2fa-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e2fa-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e2fa-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e2fa-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="7e2fa-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7e2fa-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7e2fa-128">**UDM \_ GETrange**</span><span class="sxs-lookup"><span data-stu-id="7e2fa-128">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="7e2fa-129">**\_GETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="7e2fa-129">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> </dl>

 

 





