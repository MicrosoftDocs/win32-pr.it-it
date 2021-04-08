---
title: Messaggio LVM_UPDATE (COMmctrl. h)
description: Aggiorna un elemento della visualizzazione elenco. Se il controllo elenco-visualizzazione dispone dello \_ stile LVS AutoArrange, questa macro causa la disposizione del controllo elenco-visualizzazione. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro di aggiornamento ListView.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- Controlli di Windows Message LVM_UPDATE
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873373"
---
# <a name="lvm_update-message"></a><span data-ttu-id="9c740-106">\_Messaggio di aggiornamento LVM</span><span class="sxs-lookup"><span data-stu-id="9c740-106">LVM\_UPDATE message</span></span>

<span data-ttu-id="9c740-107">Aggiorna un elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="9c740-107">Updates a list-view item.</span></span> <span data-ttu-id="9c740-108">Se il controllo elenco-visualizzazione dispone dello stile [**LVS \_ AutoArrange**](list-view-window-styles.md) , questa macro causa la disposizione del controllo elenco-visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9c740-108">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, this macro causes the list-view control to be arranged.</span></span> <span data-ttu-id="9c740-109">È possibile inviare questo messaggio in modo esplicito o usando la macro di [**\_ aggiornamento ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) .</span><span class="sxs-lookup"><span data-stu-id="9c740-109">You can send this message explicitly or by using the [**ListView\_Update**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c740-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c740-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c740-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c740-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c740-112">Indice dell'elemento da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="9c740-112">Index of the item to update.</span></span>

</dd> <dt>

<span data-ttu-id="9c740-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c740-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9c740-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9c740-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c740-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c740-115">Return value</span></span>

<span data-ttu-id="9c740-116">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9c740-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c740-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c740-117">Requirements</span></span>



| <span data-ttu-id="9c740-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c740-118">Requirement</span></span> | <span data-ttu-id="9c740-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9c740-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c740-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c740-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9c740-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c740-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c740-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c740-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9c740-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c740-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c740-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c740-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c740-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c740-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





