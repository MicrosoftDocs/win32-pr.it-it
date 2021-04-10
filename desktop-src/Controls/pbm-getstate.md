---
title: Messaggio PBM_GETSTATE (COMmctrl. h)
description: Ottiene lo stato dell'indicatore di stato.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- Controlli di Windows Message PBM_GETSTATE
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07d4f7029fca46a046545efd1cea8e0eab99c757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964565"
---
# <a name="pbm_getstate-message"></a><span data-ttu-id="7496c-104">\_Messaggio GETstate di PBM</span><span class="sxs-lookup"><span data-stu-id="7496c-104">PBM\_GETSTATE message</span></span>

<span data-ttu-id="7496c-105">Ottiene lo stato dell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="7496c-105">Gets the state of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7496c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7496c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7496c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7496c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7496c-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7496c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7496c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7496c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7496c-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7496c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7496c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7496c-111">Return value</span></span>

<span data-ttu-id="7496c-112">Restituisce lo stato corrente dell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="7496c-112">Returns the current state of the progress bar.</span></span> <span data-ttu-id="7496c-113">Uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7496c-113">One of the following values.</span></span>



| <span data-ttu-id="7496c-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7496c-114">Return code</span></span>                                                                                 | <span data-ttu-id="7496c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7496c-115">Description</span></span>             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="7496c-116"><dt>**PBST \_ normale**</dt></span><span class="sxs-lookup"><span data-stu-id="7496c-116"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="7496c-117">Operazione in corso.</span><span class="sxs-lookup"><span data-stu-id="7496c-117">In progress.</span></span><br/> |
| <dl> <span data-ttu-id="7496c-118"><dt>**\_errore PBST**</dt></span><span class="sxs-lookup"><span data-stu-id="7496c-118"><dt>**PBST\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="7496c-119">Errore.</span><span class="sxs-lookup"><span data-stu-id="7496c-119">Error.</span></span><br/>       |
| <dl> <span data-ttu-id="7496c-120"><dt>**PBST \_ sospeso**</dt></span><span class="sxs-lookup"><span data-stu-id="7496c-120"><dt>**PBST\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="7496c-121">(sospeso)</span><span class="sxs-lookup"><span data-stu-id="7496c-121">Paused.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="7496c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7496c-122">Requirements</span></span>



| <span data-ttu-id="7496c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7496c-123">Requirement</span></span> | <span data-ttu-id="7496c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7496c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7496c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7496c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7496c-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7496c-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7496c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7496c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7496c-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7496c-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7496c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7496c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7496c-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7496c-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





