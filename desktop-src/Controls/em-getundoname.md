---
title: Messaggio di EM_GETUNDONAME (RichEdit. h)
description: Microsoft Rich Edit 2,0 e versioni successive Recupera il tipo della successiva azione di annullamento, se disponibile. Microsoft Rich Edit 1,0 questo messaggio non è supportato.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- Controlli di Windows Message EM_GETUNDONAME
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c29b5815da5569059ba80c007d6af39d1e389f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964652"
---
# <a name="em_getundoname-message"></a><span data-ttu-id="3eb07-104">\_Messaggi GETundoname em</span><span class="sxs-lookup"><span data-stu-id="3eb07-104">EM\_GETUNDONAME message</span></span>

<span data-ttu-id="3eb07-105">Microsoft Rich Edit 2,0 e versioni successive: Recupera il tipo della successiva azione di annullamento, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="3eb07-105">Microsoft Rich Edit 2.0 and later: Retrieves the type of the next undo action, if any.</span></span>

<span data-ttu-id="3eb07-106">Microsoft Rich Edit 1,0: questo messaggio non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3eb07-106">Microsoft Rich Edit 1.0: This message is not supported.</span></span>

## <a name="parameters"></a><span data-ttu-id="3eb07-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3eb07-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eb07-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3eb07-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3eb07-109">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3eb07-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3eb07-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3eb07-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3eb07-111">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3eb07-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eb07-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3eb07-112">Return value</span></span>

<span data-ttu-id="3eb07-113">Se è presente un'azione di annullamento, il valore restituito è un valore di enumerazione [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) che indica il tipo dell'azione successiva nella coda di annullamento del controllo.</span><span class="sxs-lookup"><span data-stu-id="3eb07-113">If there is an undo action, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's undo queue.</span></span>

<span data-ttu-id="3eb07-114">Se non sono presenti azioni che possono essere annullate o il tipo della successiva azione di annullamento è sconosciuto, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="3eb07-114">If there are no actions that can be undone or the type of the next undo action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3eb07-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3eb07-115">Remarks</span></span>

<span data-ttu-id="3eb07-116">I tipi di azioni che possono essere annullati o ripetuti includono operazioni di digitazione, eliminazione, trascinamento, riduzione e incolla.</span><span class="sxs-lookup"><span data-stu-id="3eb07-116">The types of actions that can be undone or redone include typing, delete, drag, drop, cut, and paste operations.</span></span> <span data-ttu-id="3eb07-117">Queste informazioni possono essere utili per le applicazioni che forniscono un'interfaccia utente estesa per operazioni di annullamento e ripristino, ad esempio una casella di riepilogo a discesa di azioni che possono essere annullate.</span><span class="sxs-lookup"><span data-stu-id="3eb07-117">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of actions that can be undone.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eb07-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3eb07-118">Requirements</span></span>



| <span data-ttu-id="3eb07-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eb07-119">Requirement</span></span> | <span data-ttu-id="3eb07-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3eb07-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3eb07-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3eb07-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3eb07-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3eb07-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3eb07-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3eb07-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3eb07-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3eb07-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3eb07-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3eb07-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3eb07-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eb07-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eb07-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3eb07-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="3eb07-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3eb07-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3eb07-129">**\_GETredoname em**</span><span class="sxs-lookup"><span data-stu-id="3eb07-129">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="3eb07-130">**\_ripetizione em**</span><span class="sxs-lookup"><span data-stu-id="3eb07-130">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="3eb07-131">**\_Annulla**</span><span class="sxs-lookup"><span data-stu-id="3eb07-131">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="3eb07-132">**UNDONAMEID**</span><span class="sxs-lookup"><span data-stu-id="3eb07-132">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





