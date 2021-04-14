---
title: Messaggio HDM_GETOVERFLOWRECT (COMmctrl. h)
description: Ottiene il rettangolo di delimitazione del pulsante di overflow quando lo \_ stile di overflow HDS è impostato sul controllo intestazione e il pulsante di overflow è visibile. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetOverflowRect dell'intestazione.
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- Controlli di Windows Message HDM_GETOVERFLOWRECT
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f521bb6b188a10bb7af52ead46423e7ae0cf58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518118"
---
# <a name="hdm_getoverflowrect-message"></a><span data-ttu-id="46489-105">\_Messaggio HDM GETOVERFLOWRECT</span><span class="sxs-lookup"><span data-stu-id="46489-105">HDM\_GETOVERFLOWRECT message</span></span>

<span data-ttu-id="46489-106">Ottiene il rettangolo di delimitazione del pulsante di overflow quando lo stile di [**\_ overflow HDS**](header-control-styles.md) è impostato sul controllo intestazione e il pulsante di overflow è visibile.</span><span class="sxs-lookup"><span data-stu-id="46489-106">Gets the bounding rectangle of the overflow button when the [**HDS\_OVERFLOW**](header-control-styles.md) style is set on the header control and the overflow button is visible.</span></span> <span data-ttu-id="46489-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetOverflowRect dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) .</span><span class="sxs-lookup"><span data-stu-id="46489-107">Send this message explicitly or by using the [**Header\_GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="46489-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46489-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46489-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46489-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46489-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="46489-110">Not used.</span></span> <span data-ttu-id="46489-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="46489-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="46489-112">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46489-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46489-113">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) per ricevere le informazioni sul rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="46489-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="46489-114">Il mittente del messaggio è responsabile dell'allocazione della struttura.</span><span class="sxs-lookup"><span data-stu-id="46489-114">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="46489-115">Le coordinate restituite nella struttura **Rect** sono espresse come coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="46489-115">The coordinates returned in the **RECT** structure are expressed as screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46489-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46489-116">Return value</span></span>

<span data-ttu-id="46489-117">Restituisce **true** se l'operazione ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="46489-117">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="46489-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="46489-118">Remarks</span></span>

<span data-ttu-id="46489-119">Il controllo intestazione deve avere lo stile **HDF \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="46489-119">The header control must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="46489-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46489-120">Requirements</span></span>



| <span data-ttu-id="46489-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="46489-121">Requirement</span></span> | <span data-ttu-id="46489-122">Valore</span><span class="sxs-lookup"><span data-stu-id="46489-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46489-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46489-123">Minimum supported client</span></span><br/> | <span data-ttu-id="46489-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46489-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46489-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46489-125">Minimum supported server</span></span><br/> | <span data-ttu-id="46489-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46489-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46489-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46489-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="46489-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46489-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46489-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46489-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46489-130">Informazioni sui controlli intestazione</span><span class="sxs-lookup"><span data-stu-id="46489-130">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

