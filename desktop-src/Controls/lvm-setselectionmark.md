---
title: Messaggio LVM_SETSELECTIONMARK (COMmctrl. h)
description: Imposta il contrassegno di selezione in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetSelectionMark di ListView.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- Controlli di Windows Message LVM_SETSELECTIONMARK
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739935"
---
# <a name="lvm_setselectionmark-message"></a><span data-ttu-id="c3f2c-105">\_Messaggio SETSELECTIONMARK LVM</span><span class="sxs-lookup"><span data-stu-id="c3f2c-105">LVM\_SETSELECTIONMARK message</span></span>

<span data-ttu-id="c3f2c-106">Imposta il contrassegno di selezione in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="c3f2c-106">Sets the selection mark in a list-view control.</span></span> <span data-ttu-id="c3f2c-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetSelectionMark di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) .</span><span class="sxs-lookup"><span data-stu-id="c3f2c-107">You can send this message explicitly or use the [**ListView\_SetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3f2c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3f2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3f2c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3f2c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c3f2c-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c3f2c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c3f2c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3f2c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3f2c-112">Indice in base zero del nuovo contrassegno di selezione.</span><span class="sxs-lookup"><span data-stu-id="c3f2c-112">Zero-based index of the new selection mark.</span></span> <span data-ttu-id="c3f2c-113">Se è impostato su-1, il contrassegno di selezione verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="c3f2c-113">If set to -1, the selection mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3f2c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3f2c-114">Return value</span></span>

<span data-ttu-id="c3f2c-115">Restituisce il contrassegno di selezione precedente oppure-1 se non è presente alcun contrassegno di selezione precedente.</span><span class="sxs-lookup"><span data-stu-id="c3f2c-115">Returns the previous selection mark, or -1 if there is no previous selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3f2c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3f2c-116">Remarks</span></span>

<span data-ttu-id="c3f2c-117">Il *contrassegno di selezione* è l'indice dell'elemento da cui inizia una selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="c3f2c-117">The *selection mark* is the item index from which a multiple selection starts.</span></span> <span data-ttu-id="c3f2c-118">Questo messaggio non influisce sullo stato di selezione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c3f2c-118">This message does not affect the selection state of the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f2c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3f2c-119">Requirements</span></span>



| <span data-ttu-id="c3f2c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3f2c-120">Requirement</span></span> | <span data-ttu-id="c3f2c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c3f2c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f2c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3f2c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c3f2c-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3f2c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3f2c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3f2c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c3f2c-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c3f2c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3f2c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c3f2c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3f2c-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3f2c-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3f2c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3f2c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f2c-129">**\_GETSELECTIONMARK LVM**</span><span class="sxs-lookup"><span data-stu-id="c3f2c-129">**LVM\_GETSELECTIONMARK**</span></span>](lvm-getselectionmark.md)
</dt> </dl>

 

 





