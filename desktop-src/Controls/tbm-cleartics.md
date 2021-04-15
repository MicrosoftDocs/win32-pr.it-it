---
title: Messaggio TBM_CLEARTICS (COMmctrl. h)
description: Rimuove i segni di graduazione correnti da un TrackBar. Questo messaggio non rimuove il primo e l'ultimo segno di graduazione, che vengono creati automaticamente dal TrackBar.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- Controlli di Windows Message TBM_CLEARTICS
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1ecb4f9f931c976b2542a1f263fc069f1eca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475922"
---
# <a name="tbm_cleartics-message"></a><span data-ttu-id="6ccbd-105">\_Messaggio CLEARTICS TBM</span><span class="sxs-lookup"><span data-stu-id="6ccbd-105">TBM\_CLEARTICS message</span></span>

<span data-ttu-id="6ccbd-106">Rimuove i segni di graduazione correnti da un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6ccbd-106">Removes the current tick marks from a trackbar.</span></span> <span data-ttu-id="6ccbd-107">Questo messaggio non rimuove il primo e l'ultimo segno di graduazione, che vengono creati automaticamente dal TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6ccbd-107">This message does not remove the first and last tick marks, which are created automatically by the trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ccbd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ccbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ccbd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ccbd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ccbd-110">Ridisegni flag.</span><span class="sxs-lookup"><span data-stu-id="6ccbd-110">Redraw flag.</span></span> <span data-ttu-id="6ccbd-111">Se questo parametro è **true**, il TrackBar viene ridisegnato dopo la cancellazione dei segni di graduazione.</span><span class="sxs-lookup"><span data-stu-id="6ccbd-111">If this parameter is **TRUE**, the trackbar is redrawn after the tick marks are cleared.</span></span> <span data-ttu-id="6ccbd-112">Se questo parametro è **false**, il messaggio Cancella i segni di graduazione senza ricreare il TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6ccbd-112">If this parameter is **FALSE**, the message clears the tick marks but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="6ccbd-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ccbd-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6ccbd-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6ccbd-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ccbd-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ccbd-115">Return value</span></span>

<span data-ttu-id="6ccbd-116">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="6ccbd-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ccbd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ccbd-117">Requirements</span></span>



| <span data-ttu-id="6ccbd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ccbd-118">Requirement</span></span> | <span data-ttu-id="6ccbd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6ccbd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ccbd-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ccbd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6ccbd-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ccbd-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ccbd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6ccbd-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ccbd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ccbd-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ccbd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ccbd-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ccbd-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





