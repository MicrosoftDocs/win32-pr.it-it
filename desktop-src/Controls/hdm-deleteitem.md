---
title: Messaggio HDM_DELETEITEM (COMmctrl. h)
description: Elimina un elemento da un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DeleteItem dell'intestazione.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- Controlli di Windows Message HDM_DELETEITEM
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a3ec4b48c3dcc77579f70d26cd55b7127f5a6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048521"
---
# <a name="hdm_deleteitem-message"></a><span data-ttu-id="e66a2-105">\_Messaggio HDM DeleteItem</span><span class="sxs-lookup"><span data-stu-id="e66a2-105">HDM\_DELETEITEM message</span></span>

<span data-ttu-id="e66a2-106">Elimina un elemento da un controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="e66a2-106">Deletes an item from a header control.</span></span> <span data-ttu-id="e66a2-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DeleteItem dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="e66a2-107">You can send this message explicitly or use the [**Header\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e66a2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e66a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e66a2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e66a2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e66a2-110">Indice dell'elemento da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e66a2-110">An index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="e66a2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e66a2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e66a2-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e66a2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e66a2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e66a2-113">Return value</span></span>

<span data-ttu-id="e66a2-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e66a2-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e66a2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e66a2-115">Requirements</span></span>



| <span data-ttu-id="e66a2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e66a2-116">Requirement</span></span> | <span data-ttu-id="e66a2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e66a2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e66a2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e66a2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e66a2-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e66a2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e66a2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e66a2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e66a2-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e66a2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e66a2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e66a2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e66a2-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e66a2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





