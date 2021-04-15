---
title: Messaggio di EM_REDO (RichEdit. h)
description: Invia un \_ messaggio di ripetizione em a un controllo Rich Edit per ripetere l'azione successiva nella coda di rollforward del controllo.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- Controlli di Windows Message EM_REDO
topic_type:
- apiref
api_name:
- EM_REDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba7a684db0d40ebcfeec4a540989c4dab4c5dd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477602"
---
# <a name="em_redo-message"></a><span data-ttu-id="3a985-104">\_Messaggio di ripetizione em</span><span class="sxs-lookup"><span data-stu-id="3a985-104">EM\_REDO message</span></span>

<span data-ttu-id="3a985-105">Invia un messaggio di **\_ ripetizione em** a un controllo Rich Edit per ripetere l'azione successiva nella coda di rollforward del controllo.</span><span class="sxs-lookup"><span data-stu-id="3a985-105">Sends an **EM\_REDO** message to a rich edit control to redo the next action in the control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a985-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a985-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a985-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a985-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a985-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3a985-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3a985-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a985-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a985-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3a985-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a985-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a985-111">Return value</span></span>

<span data-ttu-id="3a985-112">Se l'operazione di **rollforward** ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="3a985-112">If the **Redo** operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3a985-113">Se l'operazione di **rollforward** ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="3a985-113">If the **Redo** operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a985-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a985-114">Remarks</span></span>

<span data-ttu-id="3a985-115">Per determinare se sono presenti azioni nella coda di rollforward del controllo, inviare il messaggio [**\_ CANREDO em**](em-canredo.md) .</span><span class="sxs-lookup"><span data-stu-id="3a985-115">To determine whether there are any actions in the control's redo queue, send the [**EM\_CANREDO**](em-canredo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a985-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a985-116">Requirements</span></span>



| <span data-ttu-id="3a985-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a985-117">Requirement</span></span> | <span data-ttu-id="3a985-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3a985-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a985-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a985-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3a985-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a985-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a985-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a985-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3a985-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3a985-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a985-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a985-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a985-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a985-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a985-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a985-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a985-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3a985-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3a985-127">**\_CANREDO em**</span><span class="sxs-lookup"><span data-stu-id="3a985-127">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="3a985-128">**\_GETredoname em**</span><span class="sxs-lookup"><span data-stu-id="3a985-128">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="3a985-129">**EM \_ GETundoname**</span><span class="sxs-lookup"><span data-stu-id="3a985-129">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="3a985-130">**\_Annulla**</span><span class="sxs-lookup"><span data-stu-id="3a985-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





