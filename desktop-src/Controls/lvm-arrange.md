---
title: Messaggio LVM_ARRANGE (COMmctrl. h)
description: Dispone gli elementi nella visualizzazione icone. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro Arrange di ListView.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- Controlli di Windows Message LVM_ARRANGE
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b6a081cf963a649329951358ea4c972f200f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119015"
---
# <a name="lvm_arrange-message"></a><span data-ttu-id="0f62a-105">\_Messaggio di disposizione LVM</span><span class="sxs-lookup"><span data-stu-id="0f62a-105">LVM\_ARRANGE message</span></span>

<span data-ttu-id="0f62a-106">Dispone gli elementi nella visualizzazione icone.</span><span class="sxs-lookup"><span data-stu-id="0f62a-106">Arranges items in icon view.</span></span> <span data-ttu-id="0f62a-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ Arrange di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) .</span><span class="sxs-lookup"><span data-stu-id="0f62a-107">You can send this message explicitly or by using the [**ListView\_Arrange**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f62a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f62a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f62a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f62a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f62a-110">Uno dei valori seguenti che specifica l'allineamento:</span><span class="sxs-lookup"><span data-stu-id="0f62a-110">One of the following values that specifies alignment:</span></span>



| <span data-ttu-id="0f62a-111">Valore</span><span class="sxs-lookup"><span data-stu-id="0f62a-111">Value</span></span>                                                                                                                                                            | <span data-ttu-id="0f62a-112">Significato</span><span class="sxs-lookup"><span data-stu-id="0f62a-112">Meaning</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <span data-ttu-id="0f62a-113"><dt>**\_ALIGNLEFT LVA**</dt></span><span class="sxs-lookup"><span data-stu-id="0f62a-113"><dt>**LVA\_ALIGNLEFT**</dt></span></span> </dl>    | <span data-ttu-id="0f62a-114">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="0f62a-114">Not implemented.</span></span> <span data-ttu-id="0f62a-115">Applicare invece lo stile [**\_ ALIGNLEFT di LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0f62a-115">Apply the [**LVS\_ALIGNLEFT**](list-view-window-styles.md) style instead.</span></span><br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <span data-ttu-id="0f62a-116"><dt>**\_ALIGNTOP LVA**</dt></span><span class="sxs-lookup"><span data-stu-id="0f62a-116"><dt>**LVA\_ALIGNTOP**</dt></span></span> </dl>       | <span data-ttu-id="0f62a-117">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="0f62a-117">Not implemented.</span></span> <span data-ttu-id="0f62a-118">Applicare invece lo stile [**\_ ALIGNTOP di LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0f62a-118">Apply the [**LVS\_ALIGNTOP**](list-view-window-styles.md) style instead.</span></span><br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <span data-ttu-id="0f62a-119"><dt>**\_impostazione predefinita LVA**</dt></span><span class="sxs-lookup"><span data-stu-id="0f62a-119"><dt>**LVA\_DEFAULT**</dt></span></span> </dl>          | <span data-ttu-id="0f62a-120">Allinea gli elementi in base agli stili di allineamento correnti del controllo visualizzazione elenco (valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="0f62a-120">Aligns items according to the list-view control's current alignment styles (the default value).</span></span><br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <span data-ttu-id="0f62a-121"><dt>**\_SNAPTOGRID LVA**</dt></span><span class="sxs-lookup"><span data-stu-id="0f62a-121"><dt>**LVA\_SNAPTOGRID**</dt></span></span> </dl> | <span data-ttu-id="0f62a-122">Blocca tutte le icone nella posizione della griglia più vicina.</span><span class="sxs-lookup"><span data-stu-id="0f62a-122">Snaps all icons to the nearest grid position.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="0f62a-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f62a-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f62a-124">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0f62a-124">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f62a-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f62a-125">Return value</span></span>

<span data-ttu-id="0f62a-126">Restituisce **true** se l'operazione ha esito positivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="0f62a-126">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f62a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f62a-127">Requirements</span></span>



| <span data-ttu-id="0f62a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f62a-128">Requirement</span></span> | <span data-ttu-id="0f62a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0f62a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f62a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f62a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0f62a-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f62a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f62a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f62a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0f62a-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f62a-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f62a-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f62a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f62a-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f62a-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





