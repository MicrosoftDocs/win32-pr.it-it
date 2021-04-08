---
title: Messaggio DTM_CLOSEMONTHCAL (COMmctrl. h)
description: Chiude un controllo di selezione data e ora (DTP). Inviare questo messaggio in modo esplicito o utilizzando la \_ macro DateTime CloseMonthCal.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- Controlli di Windows Message DTM_CLOSEMONTHCAL
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd79f33576490196bf29fd51316f8ce3daf4ad4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047942"
---
# <a name="dtm_closemonthcal-message"></a><span data-ttu-id="68af5-105">\_Messaggio CLOSEMONTHCAL DTM</span><span class="sxs-lookup"><span data-stu-id="68af5-105">DTM\_CLOSEMONTHCAL message</span></span>

<span data-ttu-id="68af5-106">Chiude un controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="68af5-106">Closes a date and time picker (DTP) control.</span></span> <span data-ttu-id="68af5-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .</span><span class="sxs-lookup"><span data-stu-id="68af5-107">Send this message explicitly or by using the [**DateTime\_CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="68af5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="68af5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68af5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68af5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68af5-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="68af5-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="68af5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68af5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="68af5-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="68af5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68af5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68af5-113">Return value</span></span>

<span data-ttu-id="68af5-114">Restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="68af5-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="68af5-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="68af5-115">Remarks</span></span>

<span data-ttu-id="68af5-116">Elimina il controllo e invia una notifica [del \_ primo piano DTN](dtn-closeup.md) che il controllo sta chiudendo anziché il controllo è in apertura (a discesa come nella notifica a [ \_ discesa DTN](dtn-dropdown.md) ) all'elemento padre del controllo.</span><span class="sxs-lookup"><span data-stu-id="68af5-116">Destroys the control and sends a [DTN\_CLOSEUP](dtn-closeup.md) notification that the control is closing as opposed to the control is opening (dropping-down as in the [DTN\_DROPDOWN](dtn-dropdown.md) notification) to the control's parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="68af5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68af5-117">Requirements</span></span>



| <span data-ttu-id="68af5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="68af5-118">Requirement</span></span> | <span data-ttu-id="68af5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="68af5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68af5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68af5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="68af5-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68af5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68af5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68af5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="68af5-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68af5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68af5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68af5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="68af5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68af5-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68af5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68af5-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="68af5-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="68af5-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="68af5-128">\_elenco a discesa DTN</span><span class="sxs-lookup"><span data-stu-id="68af5-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="68af5-129">primo piano DTN \_</span><span class="sxs-lookup"><span data-stu-id="68af5-129">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> </dl>

 

 





