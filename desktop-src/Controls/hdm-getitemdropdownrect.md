---
title: Messaggio HDM_GETITEMDROPDOWNRECT (COMmctrl. h)
description: Ottiene il rettangolo di delimitazione del pulsante di menu combinato per un elemento di intestazione con lo stile HDF \_ SPLITBUTTON. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetItemDropDownRect dell'intestazione.
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- Controlli di Windows Message HDM_GETITEMDROPDOWNRECT
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86f3df8de5224e79ca4e15ea18409e13972ca5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048396"
---
# <a name="hdm_getitemdropdownrect-message"></a><span data-ttu-id="a36dc-105">\_Messaggio HDM GETITEMDROPDOWNRECT</span><span class="sxs-lookup"><span data-stu-id="a36dc-105">HDM\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="a36dc-106">Ottiene il rettangolo di delimitazione del pulsante di menu combinato per un elemento di intestazione con lo stile **HDF \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="a36dc-106">Gets the bounding rectangle of the split button for a header item with style **HDF\_SPLITBUTTON**.</span></span> <span data-ttu-id="a36dc-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetItemDropDownRect dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) .</span><span class="sxs-lookup"><span data-stu-id="a36dc-107">Send this message explicitly or by using the [**Header\_GetItemDropDownRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a36dc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a36dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a36dc-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a36dc-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a36dc-110">Indice in base zero dell'elemento di controllo dell'intestazione per il quale recuperare il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="a36dc-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="a36dc-111">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a36dc-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a36dc-112">Puntatore a una struttura [**Rect**](/windows/win32/api/windef/ns-windef-rect) che riceve le informazioni sul rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="a36dc-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="a36dc-113">Il mittente del messaggio è responsabile dell'allocazione della struttura.</span><span class="sxs-lookup"><span data-stu-id="a36dc-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="a36dc-114">Le coordinate restituite nella struttura RECT sono espresse in relazione all'elemento padre del controllo Header.</span><span class="sxs-lookup"><span data-stu-id="a36dc-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a36dc-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a36dc-115">Return value</span></span>

<span data-ttu-id="a36dc-116">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a36dc-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a36dc-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a36dc-117">Remarks</span></span>

<span data-ttu-id="a36dc-118">L'elemento dell'intestazione deve avere lo stile **HDF \_ SPLITBUTTON**.</span><span class="sxs-lookup"><span data-stu-id="a36dc-118">The header item must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a36dc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a36dc-119">Requirements</span></span>



| <span data-ttu-id="a36dc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a36dc-120">Requirement</span></span> | <span data-ttu-id="a36dc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a36dc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a36dc-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a36dc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a36dc-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a36dc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a36dc-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a36dc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a36dc-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a36dc-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a36dc-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a36dc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a36dc-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a36dc-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a36dc-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a36dc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a36dc-129">Informazioni sui controlli intestazione</span><span class="sxs-lookup"><span data-stu-id="a36dc-129">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





