---
title: Messaggio PBM_SETSTATE (COMmctrl. h)
description: Imposta lo stato dell'indicatore di stato.
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- Controlli di Windows Message PBM_SETSTATE
topic_type:
- apiref
api_name:
- PBM_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c91e94bcc909957264eff776e56d3580b2c36ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477908"
---
# <a name="pbm_setstate-message"></a><span data-ttu-id="4e3af-104">\_Messaggio di SEstato di PBM</span><span class="sxs-lookup"><span data-stu-id="4e3af-104">PBM\_SETSTATE message</span></span>

<span data-ttu-id="4e3af-105">Imposta lo stato dell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="4e3af-105">Sets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e3af-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e3af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e3af-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e3af-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e3af-108">Stato dell'indicatore di stato che viene impostato.</span><span class="sxs-lookup"><span data-stu-id="4e3af-108">State of the progress bar that is being set.</span></span> <span data-ttu-id="4e3af-109">Uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4e3af-109">One of the following values.</span></span>



| <span data-ttu-id="4e3af-110">Valore</span><span class="sxs-lookup"><span data-stu-id="4e3af-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="4e3af-111">Significato</span><span class="sxs-lookup"><span data-stu-id="4e3af-111">Meaning</span></span>                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="4e3af-112"><dt>**PBST \_ normale**</dt></span><span class="sxs-lookup"><span data-stu-id="4e3af-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="4e3af-113">Operazione in corso.</span><span class="sxs-lookup"><span data-stu-id="4e3af-113">In progress.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="4e3af-114"><dt>**\_errore PBST**</dt></span><span class="sxs-lookup"><span data-stu-id="4e3af-114"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="4e3af-115">Errore.</span><span class="sxs-lookup"><span data-stu-id="4e3af-115">Error.</span></span><br/>       |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="4e3af-116"><dt>**PBST \_ sospeso**</dt></span><span class="sxs-lookup"><span data-stu-id="4e3af-116"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="4e3af-117">(sospeso)</span><span class="sxs-lookup"><span data-stu-id="4e3af-117">Paused.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="4e3af-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e3af-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4e3af-119">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4e3af-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e3af-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e3af-120">Return value</span></span>

<span data-ttu-id="4e3af-121">Restituisce lo stato precedente.</span><span class="sxs-lookup"><span data-stu-id="4e3af-121">Returns the previous state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e3af-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e3af-122">Requirements</span></span>



| <span data-ttu-id="4e3af-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e3af-123">Requirement</span></span> | <span data-ttu-id="4e3af-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4e3af-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e3af-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e3af-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4e3af-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e3af-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e3af-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e3af-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4e3af-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e3af-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e3af-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e3af-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e3af-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e3af-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





