---
title: Messaggio TCM_GETITEMRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione di una scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl GetItemRect.
ms.assetid: 6abd8cdf-5f19-4b7e-800e-970097bc891b
keywords:
- Controlli di Windows Message TCM_GETITEMRECT
topic_type:
- apiref
api_name:
- TCM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6c214efbeeaf58d1ff3def9f50f10011b41dfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874409"
---
# <a name="tcm_getitemrect-message"></a><span data-ttu-id="90402-105">\_Messaggio TCM GETITEMRECT</span><span class="sxs-lookup"><span data-stu-id="90402-105">TCM\_GETITEMRECT message</span></span>

<span data-ttu-id="90402-106">Recupera il rettangolo di delimitazione di una scheda in un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="90402-106">Retrieves the bounding rectangle for a tab in a tab control.</span></span> <span data-ttu-id="90402-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="90402-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="90402-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="90402-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90402-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90402-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90402-110">Indice della scheda.</span><span class="sxs-lookup"><span data-stu-id="90402-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="90402-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90402-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90402-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve il rettangolo delimitatore della scheda in coordinate del viewport.</span><span class="sxs-lookup"><span data-stu-id="90402-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the tab, in viewport coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90402-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90402-113">Return value</span></span>

<span data-ttu-id="90402-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="90402-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="90402-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90402-115">Requirements</span></span>



| <span data-ttu-id="90402-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="90402-116">Requirement</span></span> | <span data-ttu-id="90402-117">Valore</span><span class="sxs-lookup"><span data-stu-id="90402-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90402-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90402-118">Minimum supported client</span></span><br/> | <span data-ttu-id="90402-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90402-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90402-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90402-120">Minimum supported server</span></span><br/> | <span data-ttu-id="90402-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="90402-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90402-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90402-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="90402-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="90402-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

