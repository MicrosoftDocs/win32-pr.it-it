---
title: Messaggio TTM_GETDELAYTIME (COMmctrl. h)
description: Recupera le durate iniziali, popup e reshow attualmente impostate per un controllo ToolTip.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- Controlli di Windows Message TTM_GETDELAYTIME
topic_type:
- apiref
api_name:
- TTM_GETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff8c75f078465646333cae1f519049733a0c9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301656"
---
# <a name="ttm_getdelaytime-message"></a><span data-ttu-id="eac94-104">\_Messaggio TTM GETDELAYTIME</span><span class="sxs-lookup"><span data-stu-id="eac94-104">TTM\_GETDELAYTIME message</span></span>

<span data-ttu-id="eac94-105">Recupera le durate iniziali, popup e reshow attualmente impostate per un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="eac94-105">Retrieves the initial, pop-up, and reshow durations currently set for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="eac94-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eac94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eac94-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eac94-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eac94-108">Flag che specifica quale valore Duration verrà recuperato.</span><span class="sxs-lookup"><span data-stu-id="eac94-108">Flag that specifies which duration value will be retrieved.</span></span> <span data-ttu-id="eac94-109">Per il parametro è possibile specificare uno dei valori riportati di seguito:</span><span class="sxs-lookup"><span data-stu-id="eac94-109">This parameter can have one of the following values:</span></span>



| <span data-ttu-id="eac94-110">Valore</span><span class="sxs-lookup"><span data-stu-id="eac94-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="eac94-111">Significato</span><span class="sxs-lookup"><span data-stu-id="eac94-111">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="eac94-112"><dt>**\_AUTOPOP TTDT**</dt></span><span class="sxs-lookup"><span data-stu-id="eac94-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl> | <span data-ttu-id="eac94-113">Recuperare la quantità di tempo in cui la finestra della descrizione comando rimane visibile se il puntatore è fermo all'interno del rettangolo di delimitazione di uno strumento.</span><span class="sxs-lookup"><span data-stu-id="eac94-113">Retrieve the amount of time the tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span><br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="eac94-114"><dt>**TTDT \_ iniziale**</dt></span><span class="sxs-lookup"><span data-stu-id="eac94-114"><dt>**TTDT\_INITIAL**</dt></span></span> </dl> | <span data-ttu-id="eac94-115">Recuperare l'intervallo di tempo in cui il puntatore deve rimanere fermo nel rettangolo di delimitazione di uno strumento prima che venga visualizzata la finestra della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="eac94-115">Retrieve the amount of time the pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span><br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="eac94-116"><dt>**TTDT \_ RImostra**</dt></span><span class="sxs-lookup"><span data-stu-id="eac94-116"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>    | <span data-ttu-id="eac94-117">Recuperare la quantità di tempo necessaria per la visualizzazione delle finestre di descrizione comando successive quando il puntatore passa da uno strumento all'altro.</span><span class="sxs-lookup"><span data-stu-id="eac94-117">Retrieve the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="eac94-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eac94-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eac94-119">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="eac94-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eac94-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eac94-120">Return value</span></span>

<span data-ttu-id="eac94-121">Restituisce e il valore INT con la durata specificata in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="eac94-121">Returns and INT value with the specified duration in milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="eac94-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eac94-122">Requirements</span></span>



| <span data-ttu-id="eac94-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="eac94-123">Requirement</span></span> | <span data-ttu-id="eac94-124">Valore</span><span class="sxs-lookup"><span data-stu-id="eac94-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eac94-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eac94-125">Minimum supported client</span></span><br/> | <span data-ttu-id="eac94-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eac94-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eac94-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eac94-127">Minimum supported server</span></span><br/> | <span data-ttu-id="eac94-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eac94-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eac94-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eac94-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="eac94-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eac94-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eac94-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eac94-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eac94-132">**\_SETDELAYTIME TTM**</span><span class="sxs-lookup"><span data-stu-id="eac94-132">**TTM\_SETDELAYTIME**</span></span>](ttm-setdelaytime.md)
</dt> </dl>

 

 





