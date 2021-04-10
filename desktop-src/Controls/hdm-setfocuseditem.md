---
title: Messaggio HDM_SETFOCUSEDITEM (COMmctrl. h)
description: Imposta lo stato attivo su un elemento specificato in un controllo intestazione. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro SetFocusedItem dell'intestazione.
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- Controlli di Windows Message HDM_SETFOCUSEDITEM
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120846"
---
# <a name="hdm_setfocuseditem-message"></a><span data-ttu-id="7de4b-105">\_Messaggio HDM SETFOCUSEDITEM</span><span class="sxs-lookup"><span data-stu-id="7de4b-105">HDM\_SETFOCUSEDITEM message</span></span>

<span data-ttu-id="7de4b-106">Imposta lo stato attivo su un elemento specificato in un controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="7de4b-106">Sets the focus to a specified item in a header control.</span></span> <span data-ttu-id="7de4b-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ SetFocusedItem dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) .</span><span class="sxs-lookup"><span data-stu-id="7de4b-107">Send this message explicitly or by using the [**Header\_SetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7de4b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7de4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7de4b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7de4b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7de4b-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="7de4b-110">Not used.</span></span> <span data-ttu-id="7de4b-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7de4b-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7de4b-112">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7de4b-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7de4b-113">Indice dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7de4b-113">The index of item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7de4b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7de4b-114">Return value</span></span>

<span data-ttu-id="7de4b-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7de4b-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7de4b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7de4b-116">Requirements</span></span>



| <span data-ttu-id="7de4b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7de4b-117">Requirement</span></span> | <span data-ttu-id="7de4b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7de4b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7de4b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7de4b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7de4b-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7de4b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7de4b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7de4b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7de4b-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7de4b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7de4b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7de4b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7de4b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7de4b-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7de4b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7de4b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7de4b-126">Informazioni sui controlli intestazione</span><span class="sxs-lookup"><span data-stu-id="7de4b-126">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





