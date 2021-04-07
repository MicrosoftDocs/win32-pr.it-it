---
title: Messaggio UDM_SETACCEL (COMmctrl. h)
description: Imposta l'accelerazione per un controllo di scorrimento.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- Controlli di Windows Message UDM_SETACCEL
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43ed290ce1668ffcaa9fb086a99ad52e5129ad6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048761"
---
# <a name="udm_setaccel-message"></a><span data-ttu-id="cc156-104">\_Messaggio UDM SETACCEL</span><span class="sxs-lookup"><span data-stu-id="cc156-104">UDM\_SETACCEL message</span></span>

<span data-ttu-id="cc156-105">Imposta l'accelerazione per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="cc156-105">Sets the acceleration for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc156-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc156-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc156-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc156-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc156-108">Numero di strutture [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) specificate da *aAccels*.</span><span class="sxs-lookup"><span data-stu-id="cc156-108">Number of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures specified by *aAccels*.</span></span>

</dd> <dt>

<span data-ttu-id="cc156-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc156-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc156-110">Puntatore a una matrice di strutture [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) che contengono informazioni sull'accelerazione.</span><span class="sxs-lookup"><span data-stu-id="cc156-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that contain acceleration information.</span></span> <span data-ttu-id="cc156-111">Gli elementi devono essere ordinati in ordine crescente in base al membro **nsec** .</span><span class="sxs-lookup"><span data-stu-id="cc156-111">Elements should be sorted in ascending order based on the **nSec** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc156-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc156-112">Return value</span></span>

<span data-ttu-id="cc156-113">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cc156-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc156-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc156-114">Requirements</span></span>



| <span data-ttu-id="cc156-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc156-115">Requirement</span></span> | <span data-ttu-id="cc156-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cc156-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc156-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc156-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc156-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc156-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc156-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc156-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc156-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cc156-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc156-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc156-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc156-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc156-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc156-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc156-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc156-124">**\_GETACCEL UDM**</span><span class="sxs-lookup"><span data-stu-id="cc156-124">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)
</dt> </dl>

 

 





