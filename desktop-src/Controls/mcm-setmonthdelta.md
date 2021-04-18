---
title: Messaggio MCM_SETMONTHDELTA (COMmctrl. h)
description: Imposta la velocità di scorrimento per un controllo di calendario mensile. La velocità di scorrimento indica il numero di mesi durante i quali il controllo sposta la visualizzazione quando l'utente fa clic su un pulsante di scorrimento. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal SetMonthDelta.
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- Controlli di Windows Message MCM_SETMONTHDELTA
topic_type:
- apiref
api_name:
- MCM_SETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 123eddb55a7ee8ddf8e3f6d8136e9ee57dfc8681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302518"
---
# <a name="mcm_setmonthdelta-message"></a><span data-ttu-id="c536e-106">\_Messaggio SETMONTHDELTA MCM</span><span class="sxs-lookup"><span data-stu-id="c536e-106">MCM\_SETMONTHDELTA message</span></span>

<span data-ttu-id="c536e-107">Imposta la velocità di scorrimento per un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="c536e-107">Sets the scroll rate for a month calendar control.</span></span> <span data-ttu-id="c536e-108">La velocità di scorrimento indica il numero di mesi durante i quali il controllo sposta la visualizzazione quando l'utente fa clic su un pulsante di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="c536e-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="c536e-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) .</span><span class="sxs-lookup"><span data-stu-id="c536e-109">You can send this message explicitly or by using the [**MonthCal\_SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c536e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c536e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c536e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c536e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c536e-112">Valore che rappresenta il numero di mesi da impostare come velocità di scorrimento del controllo.</span><span class="sxs-lookup"><span data-stu-id="c536e-112">Value representing the number of months to be set as the control's scroll rate.</span></span> <span data-ttu-id="c536e-113">Se questo valore è zero, il Delta del mese viene reimpostato sul valore predefinito, ovvero sul numero di mesi visualizzato nel controllo.</span><span class="sxs-lookup"><span data-stu-id="c536e-113">If this value is zero, the month delta is reset to the default, which is the number of months displayed in the control.</span></span>

</dd> <dt>

<span data-ttu-id="c536e-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c536e-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c536e-115">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c536e-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c536e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c536e-116">Return value</span></span>

<span data-ttu-id="c536e-117">Restituisce un valore INT che rappresenta la velocità di scorrimento precedente.</span><span class="sxs-lookup"><span data-stu-id="c536e-117">Returns an INT value that represents the previous scroll rate.</span></span> <span data-ttu-id="c536e-118">Se la frequenza di scorrimento non è stata impostata in precedenza, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="c536e-118">If the scroll rate was not previously set, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c536e-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c536e-119">Remarks</span></span>

<span data-ttu-id="c536e-120">I tasti PGSU e PGGIÙ, \_ ovvero VK prima e VK, \_ cambiano il mese selezionato per uno, indipendentemente dal numero di mesi visualizzato o dal valore impostato da **MCM \_ SETMONTHDELTA**.</span><span class="sxs-lookup"><span data-stu-id="c536e-120">The PAGE UP and PAGE DOWN keys, VK\_PRIOR and VK\_NEXT, change the selected month by one, regardless of the number of months displayed or the value set by **MCM\_SETMONTHDELTA**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c536e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c536e-121">Requirements</span></span>



| <span data-ttu-id="c536e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c536e-122">Requirement</span></span> | <span data-ttu-id="c536e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c536e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c536e-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c536e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c536e-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c536e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c536e-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c536e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c536e-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c536e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c536e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c536e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c536e-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c536e-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





