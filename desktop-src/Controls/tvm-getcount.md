---
title: Messaggio TVM_GETCOUNT (COMmctrl. h)
description: Recupera un conteggio degli elementi in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro di TreeView GetCount.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- Controlli di Windows Message TVM_GETCOUNT
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 870ca0d1e4bf04d054d29d78ab60371863648a8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478479"
---
# <a name="tvm_getcount-message"></a><span data-ttu-id="27032-105">\_Messaggio TVM GETcount</span><span class="sxs-lookup"><span data-stu-id="27032-105">TVM\_GETCOUNT message</span></span>

<span data-ttu-id="27032-106">Recupera un conteggio degli elementi in un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="27032-106">Retrieves a count of the items in a tree-view control.</span></span> <span data-ttu-id="27032-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro di [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) .</span><span class="sxs-lookup"><span data-stu-id="27032-107">You can send this message explicitly or by using the [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="27032-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="27032-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27032-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27032-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="27032-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="27032-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="27032-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27032-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="27032-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="27032-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27032-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27032-113">Return value</span></span>

<span data-ttu-id="27032-114">Restituisce il numero di elementi.</span><span class="sxs-lookup"><span data-stu-id="27032-114">Returns the count of items.</span></span>

## <a name="remarks"></a><span data-ttu-id="27032-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="27032-115">Remarks</span></span>

<span data-ttu-id="27032-116">Il numero di nodi restituito da [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) è limitato ai valori integer.</span><span class="sxs-lookup"><span data-stu-id="27032-116">The node count returned by [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) is limited to integer values.</span></span> <span data-ttu-id="27032-117">Se si aggiunge un nodo oltre 32767, la macro restituisce un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="27032-117">If you add a node beyond 32767 the macro returns a negative value.</span></span> <span data-ttu-id="27032-118">Dopo aver aggiunto i nodi 65536, il conteggio torna a zero.</span><span class="sxs-lookup"><span data-stu-id="27032-118">After adding 65536 nodes the count returns to zero.</span></span> <span data-ttu-id="27032-119">Quando si verifica questo problema, il controllo di visualizzazione albero appare vuoto senza barre di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="27032-119">When this occurs, the tree-view control appears empty with no scrollbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="27032-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27032-120">Requirements</span></span>



| <span data-ttu-id="27032-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="27032-121">Requirement</span></span> | <span data-ttu-id="27032-122">Valore</span><span class="sxs-lookup"><span data-stu-id="27032-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27032-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27032-123">Minimum supported client</span></span><br/> | <span data-ttu-id="27032-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27032-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27032-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27032-125">Minimum supported server</span></span><br/> | <span data-ttu-id="27032-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="27032-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27032-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27032-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="27032-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="27032-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





