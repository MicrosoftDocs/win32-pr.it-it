---
title: Messaggio di EM_GETCTFMODEBIAS (RichEdit. h)
description: Ottiene i valori di distorsione della modalità Framework dei servizi di testo per un controllo Microsoft Rich Edit.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- Controlli di Windows Message EM_GETCTFMODEBIAS
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d5eabbddca1c13fefae99c29d8c550fbd274e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120011"
---
# <a name="em_getctfmodebias-message"></a><span data-ttu-id="bb7dd-104">\_Messaggio GETCTFMODEBIAS em</span><span class="sxs-lookup"><span data-stu-id="bb7dd-104">EM\_GETCTFMODEBIAS message</span></span>

<span data-ttu-id="bb7dd-105">Ottiene i valori di distorsione della modalità Framework dei servizi di testo per un controllo Microsoft Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="bb7dd-105">Gets the Text Services Framework mode bias values for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb7dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb7dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb7dd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb7dd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb7dd-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bb7dd-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bb7dd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb7dd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb7dd-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bb7dd-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb7dd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb7dd-111">Return value</span></span>

<span data-ttu-id="bb7dd-112">Valore di distorsione della modalità del Framework dei servizi di testo corrente.</span><span class="sxs-lookup"><span data-stu-id="bb7dd-112">The current Text Services Framework mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb7dd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb7dd-113">Remarks</span></span>

<span data-ttu-id="bb7dd-114">Per ottenere la distorsione della modalità IME, chiamare [**em \_ GETIMEMODEBIAS**](em-getimemodebias.md).</span><span class="sxs-lookup"><span data-stu-id="bb7dd-114">To get the IME mode bias, call [**EM\_GETIMEMODEBIAS**](em-getimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb7dd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb7dd-115">Requirements</span></span>



| <span data-ttu-id="bb7dd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb7dd-116">Requirement</span></span> | <span data-ttu-id="bb7dd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bb7dd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb7dd-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb7dd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bb7dd-119">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb7dd-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb7dd-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb7dd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bb7dd-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb7dd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb7dd-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb7dd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb7dd-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb7dd-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb7dd-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb7dd-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb7dd-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="bb7dd-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bb7dd-126">**\_SETCTFMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="bb7dd-126">**EM\_SETCTFMODEBIAS**</span></span>](em-setctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="bb7dd-127">**\_GETIMEMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="bb7dd-127">**EM\_GETIMEMODEBIAS**</span></span>](em-getimemodebias.md)
</dt> </dl>

 

 





