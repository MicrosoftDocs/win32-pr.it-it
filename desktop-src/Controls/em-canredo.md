---
title: Messaggio di EM_CANREDO (RichEdit. h)
description: Determina se sono presenti azioni nella coda di rollforward del controllo.
ms.assetid: 4a76adc8-f815-4cf7-8742-b7695e5a0f64
keywords:
- Controlli di Windows Message EM_CANREDO
topic_type:
- apiref
api_name:
- EM_CANREDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfb12f8e72bdf5321151cd3a70b74f322a46591
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874125"
---
# <a name="em_canredo-message"></a><span data-ttu-id="1f6e9-104">\_Messaggio CANREDO em</span><span class="sxs-lookup"><span data-stu-id="1f6e9-104">EM\_CANREDO message</span></span>

<span data-ttu-id="1f6e9-105">Determina se sono presenti azioni nella coda di rollforward del controllo.</span><span class="sxs-lookup"><span data-stu-id="1f6e9-105">Determines whether there are any actions in the control redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f6e9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f6e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f6e9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f6e9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f6e9-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1f6e9-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1f6e9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f6e9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f6e9-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1f6e9-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f6e9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f6e9-111">Return value</span></span>

<span data-ttu-id="1f6e9-112">Se sono presenti azioni nella coda di rollforward del controllo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="1f6e9-112">If there are actions in the control redo queue, the return value is a nonzero value.</span></span>

<span data-ttu-id="1f6e9-113">Se la coda di rollforward è vuota, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="1f6e9-113">If the redo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f6e9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f6e9-114">Remarks</span></span>

<span data-ttu-id="1f6e9-115">Per ripetere l'operazione di annullamento più recente, inviare il messaggio di [**\_ ripetizione em**](em-redo.md) .</span><span class="sxs-lookup"><span data-stu-id="1f6e9-115">To redo the most recent undo operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f6e9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f6e9-116">Requirements</span></span>



| <span data-ttu-id="1f6e9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f6e9-117">Requirement</span></span> | <span data-ttu-id="1f6e9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1f6e9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f6e9-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f6e9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1f6e9-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f6e9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f6e9-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f6e9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1f6e9-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1f6e9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f6e9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f6e9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f6e9-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f6e9-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f6e9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f6e9-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="1f6e9-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1f6e9-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1f6e9-127">**\_GETredoname em**</span><span class="sxs-lookup"><span data-stu-id="1f6e9-127">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="1f6e9-128">**EM \_ GETundoname**</span><span class="sxs-lookup"><span data-stu-id="1f6e9-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="1f6e9-129">**\_ripetizione em**</span><span class="sxs-lookup"><span data-stu-id="1f6e9-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="1f6e9-130">**\_Annulla**</span><span class="sxs-lookup"><span data-stu-id="1f6e9-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





