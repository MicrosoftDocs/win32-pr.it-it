---
title: Messaggio LVM_GETGROUPSTATE (COMmctrl. h)
description: Ottiene lo stato di un gruppo specificato. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetGroupState di ListView.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- Controlli di Windows Message LVM_GETGROUPSTATE
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475376"
---
# <a name="lvm_getgroupstate-message"></a><span data-ttu-id="a2be5-105">\_Messaggio GETGROUPSTATE LVM</span><span class="sxs-lookup"><span data-stu-id="a2be5-105">LVM\_GETGROUPSTATE message</span></span>

<span data-ttu-id="a2be5-106">Ottiene lo stato di un gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="a2be5-106">Gets the state for a specified group.</span></span> <span data-ttu-id="a2be5-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetGroupState di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) .</span><span class="sxs-lookup"><span data-stu-id="a2be5-107">Send this message explicitly or by using the [**ListView\_GetGroupState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a2be5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2be5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2be5-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2be5-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2be5-110">Specifica il gruppo per **iGroupId** (vedere la struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).</span><span class="sxs-lookup"><span data-stu-id="a2be5-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="a2be5-111">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2be5-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2be5-112">Specifica i valori di stato da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a2be5-112">Specifies the state values to retrieve.</span></span> <span data-ttu-id="a2be5-113">Si tratta di una combinazione dei flag elencati per il membro di **stato** di [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).</span><span class="sxs-lookup"><span data-stu-id="a2be5-113">This is a combination of the flags listed for the **state** member of [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2be5-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2be5-114">Return value</span></span>

<span data-ttu-id="a2be5-115">Restituisce la combinazione di valori di stato impostati.</span><span class="sxs-lookup"><span data-stu-id="a2be5-115">Returns the combination of state values that are set.</span></span> <span data-ttu-id="a2be5-116">Se, ad esempio, *lParam* è LVGS \_ compresso e il valore restituito è zero, lo \_ stato compresso LVGS non è impostato.</span><span class="sxs-lookup"><span data-stu-id="a2be5-116">For example, if *lParam* is LVGS\_COLLAPSED and the value returned is zero, the LVGS\_COLLAPSED state is not set.</span></span> <span data-ttu-id="a2be5-117">Se il gruppo non viene trovato, viene restituito zero.</span><span class="sxs-lookup"><span data-stu-id="a2be5-117">Zero is returned if the group is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2be5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2be5-118">Requirements</span></span>



| <span data-ttu-id="a2be5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2be5-119">Requirement</span></span> | <span data-ttu-id="a2be5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a2be5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2be5-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2be5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2be5-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2be5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a2be5-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2be5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2be5-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a2be5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2be5-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2be5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2be5-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2be5-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





