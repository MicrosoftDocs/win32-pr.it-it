---
title: Messaggio LVM_GETITEMSPACING (COMmctrl. h)
description: Determina la spaziatura tra gli elementi in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemSpacing di ListView.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- Controlli di Windows Message LVM_GETITEMSPACING
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08a7fc1004ffb46d710da6d1c2a8b0fb18e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964742"
---
# <a name="lvm_getitemspacing-message"></a><span data-ttu-id="32fe8-105">\_Messaggio GETITEMSPACING LVM</span><span class="sxs-lookup"><span data-stu-id="32fe8-105">LVM\_GETITEMSPACING message</span></span>

<span data-ttu-id="32fe8-106">Determina la spaziatura tra gli elementi in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="32fe8-106">Determines the spacing between items in a list-view control.</span></span> <span data-ttu-id="32fe8-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemSpacing di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) .</span><span class="sxs-lookup"><span data-stu-id="32fe8-107">You can send this message explicitly or by using the [**ListView\_GetItemSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="32fe8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="32fe8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32fe8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32fe8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32fe8-110">Visualizzazione per la quale recuperare la spaziatura dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="32fe8-110">View for which to retrieve the item spacing.</span></span> <span data-ttu-id="32fe8-111">Questo parametro è **true** per la visualizzazione icona piccola o **false** per la visualizzazione icone.</span><span class="sxs-lookup"><span data-stu-id="32fe8-111">This parameter is **TRUE** for small icon view, or **FALSE** for icon view.</span></span>

</dd> <dt>

<span data-ttu-id="32fe8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32fe8-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="32fe8-113">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="32fe8-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32fe8-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32fe8-114">Return value</span></span>

<span data-ttu-id="32fe8-115">Restituisce la quantità di spaziatura tra gli elementi.</span><span class="sxs-lookup"><span data-stu-id="32fe8-115">Returns the amount of spacing between items.</span></span> <span data-ttu-id="32fe8-116">La spaziatura orizzontale è contenuta in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e la spaziatura verticale è contenuta in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="32fe8-116">The horizontal spacing is contained in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the vertical spacing is contained in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="32fe8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32fe8-117">Requirements</span></span>



| <span data-ttu-id="32fe8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="32fe8-118">Requirement</span></span> | <span data-ttu-id="32fe8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="32fe8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32fe8-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32fe8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="32fe8-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32fe8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32fe8-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32fe8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="32fe8-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32fe8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32fe8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32fe8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="32fe8-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="32fe8-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

