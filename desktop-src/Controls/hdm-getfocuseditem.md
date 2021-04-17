---
title: Messaggio HDM_GETFOCUSEDITEM (COMmctrl. h)
description: Ottiene l'elemento in un controllo intestazione con lo stato attivo. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetFocusedItem dell'intestazione.
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- Controlli di Windows Message HDM_GETFOCUSEDITEM
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477585"
---
# <a name="hdm_getfocuseditem-message"></a><span data-ttu-id="9fc12-105">\_Messaggio HDM GETFOCUSEDITEM</span><span class="sxs-lookup"><span data-stu-id="9fc12-105">HDM\_GETFOCUSEDITEM message</span></span>

<span data-ttu-id="9fc12-106">Ottiene l'elemento in un controllo intestazione con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="9fc12-106">Gets the item in a header control that has the focus.</span></span> <span data-ttu-id="9fc12-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetFocusedItem dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) .</span><span class="sxs-lookup"><span data-stu-id="9fc12-107">Send this message explicitly or by using the [**Header\_GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9fc12-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fc12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc12-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9fc12-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9fc12-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="9fc12-110">Not used.</span></span> <span data-ttu-id="9fc12-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9fc12-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9fc12-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9fc12-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9fc12-113">Non usato.</span><span class="sxs-lookup"><span data-stu-id="9fc12-113">Not used.</span></span> <span data-ttu-id="9fc12-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9fc12-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc12-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fc12-115">Return value</span></span>

<span data-ttu-id="9fc12-116">Restituisce l'indice dell'elemento nello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="9fc12-116">Returns the index of the item in focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc12-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fc12-117">Requirements</span></span>



| <span data-ttu-id="9fc12-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fc12-118">Requirement</span></span> | <span data-ttu-id="9fc12-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9fc12-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc12-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fc12-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc12-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fc12-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9fc12-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fc12-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc12-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fc12-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9fc12-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9fc12-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fc12-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fc12-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc12-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fc12-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc12-127">Informazioni sui controlli intestazione</span><span class="sxs-lookup"><span data-stu-id="9fc12-127">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





