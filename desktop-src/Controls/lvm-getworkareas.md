---
title: Messaggio LVM_GETWORKAREAS (COMmctrl. h)
description: Recupera le aree di lavoro da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetWorkAreas di ListView.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- Controlli di Windows Message LVM_GETWORKAREAS
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478503"
---
# <a name="lvm_getworkareas-message"></a><span data-ttu-id="72c30-105">\_Messaggio GETWORKAREAS LVM</span><span class="sxs-lookup"><span data-stu-id="72c30-105">LVM\_GETWORKAREAS message</span></span>

<span data-ttu-id="72c30-106">Recupera le aree di lavoro da un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="72c30-106">Retrieves the working areas from a list-view control.</span></span> <span data-ttu-id="72c30-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetWorkAreas di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) .</span><span class="sxs-lookup"><span data-stu-id="72c30-107">You can send this message explicitly or use the [**ListView\_GetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="72c30-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="72c30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72c30-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72c30-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72c30-110">Numero di strutture [**Rect**](/previous-versions//dd162897(v=vs.85)) nella matrice in *lParam*.</span><span class="sxs-lookup"><span data-stu-id="72c30-110">The number of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures in the array at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="72c30-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72c30-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72c30-112">Puntatore a una matrice di strutture [**Rect**](/previous-versions//dd162897(v=vs.85)) che ricevono le aree di lavoro correnti del controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="72c30-112">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that receive the current working areas of the list-view control.</span></span> <span data-ttu-id="72c30-113">I valori in queste strutture si trovano nelle coordinate del client.</span><span class="sxs-lookup"><span data-stu-id="72c30-113">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="72c30-114">*wParam* specifica il numero di strutture in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="72c30-114">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72c30-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72c30-115">Return value</span></span>

<span data-ttu-id="72c30-116">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="72c30-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="72c30-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72c30-117">Requirements</span></span>



| <span data-ttu-id="72c30-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="72c30-118">Requirement</span></span> | <span data-ttu-id="72c30-119">Valore</span><span class="sxs-lookup"><span data-stu-id="72c30-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72c30-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72c30-120">Minimum supported client</span></span><br/> | <span data-ttu-id="72c30-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72c30-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72c30-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72c30-122">Minimum supported server</span></span><br/> | <span data-ttu-id="72c30-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="72c30-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72c30-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72c30-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="72c30-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="72c30-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72c30-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72c30-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72c30-127">Uso di controlli List-View</span><span class="sxs-lookup"><span data-stu-id="72c30-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

