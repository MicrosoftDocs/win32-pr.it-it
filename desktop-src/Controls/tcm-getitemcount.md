---
title: Messaggio TCM_GETITEMCOUNT (COMmctrl. h)
description: Recupera il numero di schede nel controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl GetItemCount.
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- Controlli di Windows Message TCM_GETITEMCOUNT
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d638a9be81581605b978695c8504f538967c77f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121146"
---
# <a name="tcm_getitemcount-message"></a><span data-ttu-id="4223f-105">\_Messaggio TCM GETITEMCOUNT</span><span class="sxs-lookup"><span data-stu-id="4223f-105">TCM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="4223f-106">Recupera il numero di schede nel controllo Struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="4223f-106">Retrieves the number of tabs in the tab control.</span></span> <span data-ttu-id="4223f-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="4223f-107">You can send this message explicitly or by using the [**TabCtrl\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4223f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4223f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4223f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4223f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4223f-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4223f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4223f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4223f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4223f-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4223f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4223f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4223f-113">Return value</span></span>

<span data-ttu-id="4223f-114">Restituisce il numero di elementi in caso di esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4223f-114">Returns the number of items if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4223f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4223f-115">Requirements</span></span>



| <span data-ttu-id="4223f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4223f-116">Requirement</span></span> | <span data-ttu-id="4223f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4223f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4223f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4223f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4223f-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4223f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4223f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4223f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4223f-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4223f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4223f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4223f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4223f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4223f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





