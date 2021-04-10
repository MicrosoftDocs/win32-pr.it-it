---
title: Messaggio di EM_SETUNDOLIMIT (RichEdit. h)
description: Imposta il numero massimo di azioni che possono essere archiviate nella coda di annullamento di un controllo Rich Edit.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- Controlli di Windows Message EM_SETUNDOLIMIT
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b668d047f1de6d8720f09af5baf23e7cfc9cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964384"
---
# <a name="em_setundolimit-message"></a><span data-ttu-id="882b7-104">\_Messaggio SETUNDOLIMIT em</span><span class="sxs-lookup"><span data-stu-id="882b7-104">EM\_SETUNDOLIMIT message</span></span>

<span data-ttu-id="882b7-105">Imposta il numero massimo di azioni che possono essere archiviate nella coda di annullamento di un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="882b7-105">Sets the maximum number of actions that can stored in the undo queue of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="882b7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="882b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="882b7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="882b7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="882b7-108">Specifica il numero massimo di azioni che possono essere archiviate nella coda di annullamento.</span><span class="sxs-lookup"><span data-stu-id="882b7-108">Specifies the maximum number of actions that can be stored in the undo queue.</span></span>

</dd> <dt>

<span data-ttu-id="882b7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="882b7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="882b7-110">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="882b7-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="882b7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="882b7-111">Return value</span></span>

<span data-ttu-id="882b7-112">Il valore restituito è il nuovo numero massimo di azioni di annullamento per il controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="882b7-112">The return value is the new maximum number of undo actions for the rich edit control.</span></span> <span data-ttu-id="882b7-113">Se la memoria è limitata, questo valore può essere inferiore a *wParam* .</span><span class="sxs-lookup"><span data-stu-id="882b7-113">This value may be less than *wParam* if memory is limited.</span></span>

## <a name="remarks"></a><span data-ttu-id="882b7-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="882b7-114">Remarks</span></span>

<span data-ttu-id="882b7-115">Per impostazione predefinita, il numero massimo di azioni nella coda di annullamento è 100.</span><span class="sxs-lookup"><span data-stu-id="882b7-115">By default, the maximum number of actions in the undo queue is 100.</span></span> <span data-ttu-id="882b7-116">Se si aumenta questo numero, è necessario che la memoria disponibile sia sufficiente per contenere il nuovo numero.</span><span class="sxs-lookup"><span data-stu-id="882b7-116">If you increase this number, there must be enough available memory to accommodate the new number.</span></span> <span data-ttu-id="882b7-117">Per ottenere prestazioni migliori, impostare il limite sul valore più piccolo possibile.</span><span class="sxs-lookup"><span data-stu-id="882b7-117">For better performance, set the limit to the smallest possible value.</span></span>

<span data-ttu-id="882b7-118">Se si imposta il limite su zero, la funzionalità di **annullamento** viene disabilitata.</span><span class="sxs-lookup"><span data-stu-id="882b7-118">Setting the limit to zero disables the **Undo** feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="882b7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="882b7-119">Requirements</span></span>



| <span data-ttu-id="882b7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="882b7-120">Requirement</span></span> | <span data-ttu-id="882b7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="882b7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="882b7-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="882b7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="882b7-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="882b7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="882b7-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="882b7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="882b7-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="882b7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="882b7-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="882b7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="882b7-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="882b7-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="882b7-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="882b7-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="882b7-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="882b7-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="882b7-130">**\_CANREDO em**</span><span class="sxs-lookup"><span data-stu-id="882b7-130">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="882b7-131">**\_GETredoname em**</span><span class="sxs-lookup"><span data-stu-id="882b7-131">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="882b7-132">**EM \_ GETundoname**</span><span class="sxs-lookup"><span data-stu-id="882b7-132">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="882b7-133">**\_ripetizione em**</span><span class="sxs-lookup"><span data-stu-id="882b7-133">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="882b7-134">**\_Annulla**</span><span class="sxs-lookup"><span data-stu-id="882b7-134">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





