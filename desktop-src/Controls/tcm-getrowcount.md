---
title: Messaggio TCM_GETROWCOUNT (COMmctrl. h)
description: Recupera il numero corrente di righe di schede in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TabCtrl GetRowCount.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- Controlli di Windows Message TCM_GETROWCOUNT
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bc3d9985591a08b96be2f21d55b8a6cade9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874406"
---
# <a name="tcm_getrowcount-message"></a><span data-ttu-id="b6e5b-105">TCM- \_ messaggio GETrowcount</span><span class="sxs-lookup"><span data-stu-id="b6e5b-105">TCM\_GETROWCOUNT message</span></span>

<span data-ttu-id="b6e5b-106">Recupera il numero corrente di righe di schede in un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="b6e5b-106">Retrieves the current number of rows of tabs in a tab control.</span></span> <span data-ttu-id="b6e5b-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**TabCtrl \_ GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) .</span><span class="sxs-lookup"><span data-stu-id="b6e5b-107">You can send this message explicitly or by using the [**TabCtrl\_GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6e5b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6e5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6e5b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6e5b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b6e5b-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b6e5b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b6e5b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6e5b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b6e5b-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b6e5b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6e5b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6e5b-113">Return value</span></span>

<span data-ttu-id="b6e5b-114">Restituisce il numero di righe di tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="b6e5b-114">Returns the number of rows of tabs.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6e5b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6e5b-115">Remarks</span></span>

<span data-ttu-id="b6e5b-116">Solo i controlli struttura a schede con lo stile [**\_ multiriga TCS**](tab-control-styles.md) possono avere più righe di schede.</span><span class="sxs-lookup"><span data-stu-id="b6e5b-116">Only tab controls that have the [**TCS\_MULTILINE**](tab-control-styles.md) style can have multiple rows of tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6e5b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6e5b-117">Requirements</span></span>



| <span data-ttu-id="b6e5b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6e5b-118">Requirement</span></span> | <span data-ttu-id="b6e5b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b6e5b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e5b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6e5b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e5b-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6e5b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6e5b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6e5b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e5b-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6e5b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6e5b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6e5b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6e5b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6e5b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





