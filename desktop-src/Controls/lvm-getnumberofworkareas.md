---
title: Messaggio LVM_GETNUMBEROFWORKAREAS (COMmctrl. h)
description: Recupera il numero di aree di lavoro in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetNumberOfWorkAreas di ListView.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- Controlli di Windows Message LVM_GETNUMBEROFWORKAREAS
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964739"
---
# <a name="lvm_getnumberofworkareas-message"></a><span data-ttu-id="0f179-105">\_Messaggio GETNUMBEROFWORKAREAS LVM</span><span class="sxs-lookup"><span data-stu-id="0f179-105">LVM\_GETNUMBEROFWORKAREAS message</span></span>

<span data-ttu-id="0f179-106">Recupera il numero di aree di lavoro in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="0f179-106">Retrieves the number of working areas in a list-view control.</span></span> <span data-ttu-id="0f179-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetNumberOfWorkAreas di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) .</span><span class="sxs-lookup"><span data-stu-id="0f179-107">You can send this message explicitly or use the [**ListView\_GetNumberOfWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f179-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f179-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f179-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f179-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0f179-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0f179-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0f179-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f179-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f179-112">Puntatore a un valore UINT che riceve il numero di aree di lavoro nel controllo di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="0f179-112">Pointer to a UINT value that receives the number of working areas in the list-view control.</span></span> <span data-ttu-id="0f179-113">Se viene inserito zero in questa variabile, non sono attualmente impostate aree di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0f179-113">If zero is placed in this variable, then no working areas are currently set.</span></span> <span data-ttu-id="0f179-114">Questo valore non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="0f179-114">This value cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f179-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f179-115">Return value</span></span>

<span data-ttu-id="0f179-116">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="0f179-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f179-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f179-117">Requirements</span></span>



| <span data-ttu-id="0f179-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f179-118">Requirement</span></span> | <span data-ttu-id="0f179-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0f179-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f179-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f179-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0f179-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f179-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f179-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f179-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0f179-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f179-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f179-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f179-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f179-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f179-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f179-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f179-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f179-127">Uso di controlli List-View</span><span class="sxs-lookup"><span data-stu-id="0f179-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 





