---
title: Messaggio TCM_DELETEITEM (COMmctrl. h)
description: Rimuove un elemento da un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl DeleteItem.
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- Controlli di Windows Message TCM_DELETEITEM
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ad4f57b63c154ee98fc48a59ac81bf4fd61ba5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964794"
---
# <a name="tcm_deleteitem-message"></a><span data-ttu-id="f8e75-105">\_Messaggio TCM DeleteItem</span><span class="sxs-lookup"><span data-stu-id="f8e75-105">TCM\_DELETEITEM message</span></span>

<span data-ttu-id="f8e75-106">Rimuove un elemento da un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="f8e75-106">Removes an item from a tab control.</span></span> <span data-ttu-id="f8e75-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="f8e75-107">You can send this message explicitly or by using the [**TabCtrl\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8e75-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8e75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8e75-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8e75-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8e75-110">Indice dell'elemento da eliminare.</span><span class="sxs-lookup"><span data-stu-id="f8e75-110">Index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="f8e75-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8e75-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f8e75-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f8e75-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8e75-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8e75-113">Return value</span></span>

<span data-ttu-id="f8e75-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f8e75-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8e75-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8e75-115">Requirements</span></span>



| <span data-ttu-id="f8e75-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8e75-116">Requirement</span></span> | <span data-ttu-id="f8e75-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f8e75-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8e75-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8e75-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f8e75-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8e75-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8e75-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8e75-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f8e75-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f8e75-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8e75-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8e75-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8e75-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8e75-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





