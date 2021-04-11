---
title: Messaggio LVM_SETWORKAREAS (COMmctrl. h)
description: Imposta le aree di lavoro all'interno di un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetWorkAreas di ListView.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- Controlli di Windows Message LVM_SETWORKAREAS
topic_type:
- apiref
api_name:
- LVM_SETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4166238c97b5766a5f2bbb19e0de853526d83385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964731"
---
# <a name="lvm_setworkareas-message"></a><span data-ttu-id="8ef88-105">\_Messaggio SETWORKAREAS LVM</span><span class="sxs-lookup"><span data-stu-id="8ef88-105">LVM\_SETWORKAREAS message</span></span>

<span data-ttu-id="8ef88-106">Imposta le aree di lavoro all'interno di un controllo di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="8ef88-106">Sets the working areas within a list-view control.</span></span> <span data-ttu-id="8ef88-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetWorkAreas di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) .</span><span class="sxs-lookup"><span data-stu-id="8ef88-107">You can send this message explicitly or use the [**ListView\_SetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ef88-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ef88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ef88-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ef88-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ef88-110">Numero di strutture nella matrice in corrispondenza di *LPRC*.</span><span class="sxs-lookup"><span data-stu-id="8ef88-110">The number of structures in the array at *lprc*.</span></span> <span data-ttu-id="8ef88-111">Il numero massimo di aree di lavoro consentito è definito dal \_ valore LV Max \_ WORKAREAS.</span><span class="sxs-lookup"><span data-stu-id="8ef88-111">The maximum number of working areas allowed is defined by the LV\_MAX\_WORKAREAS value.</span></span>

</dd> <dt>

<span data-ttu-id="8ef88-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ef88-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ef88-113">Puntatore a una matrice di strutture [**Rect**](/previous-versions//dd162897(v=vs.85)) che contengono le nuove aree di lavoro del controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="8ef88-113">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that contain the new working areas of the list-view control.</span></span> <span data-ttu-id="8ef88-114">I valori in queste strutture si trovano nelle coordinate del client.</span><span class="sxs-lookup"><span data-stu-id="8ef88-114">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="8ef88-115">Se questo parametro è **null**, l'area di lavoro verrà impostata sull'area client del controllo.</span><span class="sxs-lookup"><span data-stu-id="8ef88-115">If this parameter is **NULL**, the working area will be set to the client area of the control.</span></span> <span data-ttu-id="8ef88-116">*wParam* specifica il numero di strutture in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="8ef88-116">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ef88-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ef88-117">Return value</span></span>

<span data-ttu-id="8ef88-118">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8ef88-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ef88-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ef88-119">Requirements</span></span>



| <span data-ttu-id="8ef88-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ef88-120">Requirement</span></span> | <span data-ttu-id="8ef88-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8ef88-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef88-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ef88-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8ef88-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ef88-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ef88-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ef88-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8ef88-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8ef88-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ef88-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ef88-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ef88-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ef88-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ef88-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ef88-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ef88-129">Uso di controlli List-View</span><span class="sxs-lookup"><span data-stu-id="8ef88-129">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

