---
title: Messaggio LVM_GETITEMPOSITION (COMmctrl. h)
description: Recupera la posizione di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemPosition di ListView.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- Controlli di Windows Message LVM_GETITEMPOSITION
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40b5899634e2f357068caa6ef96339be82f600b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874329"
---
# <a name="lvm_getitemposition-message"></a><span data-ttu-id="effdd-105">\_Messaggio GETITEMPOSITION LVM</span><span class="sxs-lookup"><span data-stu-id="effdd-105">LVM\_GETITEMPOSITION message</span></span>

<span data-ttu-id="effdd-106">Recupera la posizione di un elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="effdd-106">Retrieves the position of a list-view item.</span></span> <span data-ttu-id="effdd-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemPosition di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) .</span><span class="sxs-lookup"><span data-stu-id="effdd-107">You can send this message explicitly or by using the [**ListView\_GetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="effdd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="effdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="effdd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="effdd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="effdd-110">Indice dell'elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="effdd-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="effdd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="effdd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="effdd-112">Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che riceve la posizione dell'angolo superiore sinistro dell'elemento, in coordinate della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="effdd-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="effdd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="effdd-113">Return value</span></span>

<span data-ttu-id="effdd-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="effdd-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="effdd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="effdd-115">Requirements</span></span>



| <span data-ttu-id="effdd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="effdd-116">Requirement</span></span> | <span data-ttu-id="effdd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="effdd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="effdd-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="effdd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="effdd-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="effdd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="effdd-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="effdd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="effdd-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="effdd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="effdd-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="effdd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="effdd-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="effdd-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

