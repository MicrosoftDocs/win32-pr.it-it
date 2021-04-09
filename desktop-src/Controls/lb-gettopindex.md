---
title: Messaggio LB_GETTOPINDEX (winuser. h)
description: Ottiene l'indice del primo elemento visibile in una casella di riepilogo.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- Controlli di Windows Message LB_GETTOPINDEX
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdeca8e3f40ab3105bb9703db9355d09a214f5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964257"
---
# <a name="lb_gettopindex-message"></a><span data-ttu-id="7a554-104">\_Messaggio GETTOPINDEX lb</span><span class="sxs-lookup"><span data-stu-id="7a554-104">LB\_GETTOPINDEX message</span></span>

<span data-ttu-id="7a554-105">Ottiene l'indice del primo elemento visibile in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="7a554-105">Gets the index of the first visible item in a list box.</span></span> <span data-ttu-id="7a554-106">Inizialmente l'elemento con indice 0 si trova nella parte superiore della casella di riepilogo, ma se il contenuto della casella di riepilogo è stato spostato, un altro elemento potrebbe trovarsi nella parte superiore.</span><span class="sxs-lookup"><span data-stu-id="7a554-106">Initially the item with index 0 is at the top of the list box, but if the list box contents have been scrolled another item may be at the top.</span></span> <span data-ttu-id="7a554-107">Il primo elemento visibile in una casella di riepilogo a più colonne è l'elemento in alto a sinistra.</span><span class="sxs-lookup"><span data-stu-id="7a554-107">The first visible item in a multiple-column list box is the top-left item.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a554-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a554-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a554-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a554-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a554-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7a554-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7a554-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a554-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a554-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7a554-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a554-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a554-113">Return value</span></span>

<span data-ttu-id="7a554-114">Il valore restituito è l'indice del primo elemento visibile nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="7a554-114">The return value is the index of the first visible item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a554-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a554-115">Requirements</span></span>



| <span data-ttu-id="7a554-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a554-116">Requirement</span></span> | <span data-ttu-id="7a554-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7a554-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a554-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a554-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7a554-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a554-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7a554-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a554-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7a554-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7a554-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7a554-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a554-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a554-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a554-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a554-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a554-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a554-125">**\_SETTOPINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="7a554-125">**LB\_SETTOPINDEX**</span></span>](lb-settopindex.md)
</dt> </dl>

 

 





