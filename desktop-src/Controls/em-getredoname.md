---
title: Messaggio di EM_GETREDONAME (RichEdit. h)
description: Recupera il tipo dell'eventuale azione successiva nella coda di rollforward del controllo Rich Edit.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- Controlli di Windows Message EM_GETREDONAME
topic_type:
- apiref
api_name:
- EM_GETREDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea44257344b9ebdb8ffe91ad97e939aae0db9b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964332"
---
# <a name="em_getredoname-message"></a><span data-ttu-id="25218-104">\_Messaggi GETredoname em</span><span class="sxs-lookup"><span data-stu-id="25218-104">EM\_GETREDONAME message</span></span>

<span data-ttu-id="25218-105">Recupera il tipo dell'eventuale azione successiva nella coda di rollforward del controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="25218-105">Retrieves the type of the next action, if any, in the rich edit control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="25218-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="25218-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25218-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25218-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25218-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="25218-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="25218-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25218-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25218-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="25218-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25218-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25218-111">Return value</span></span>

<span data-ttu-id="25218-112">Se la coda di rollforward per il controllo non è vuota, il valore restituito è un valore di enumerazione [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) che indica il tipo dell'azione successiva nella coda di rollforward del controllo.</span><span class="sxs-lookup"><span data-stu-id="25218-112">If the redo queue for the control is not empty, the value returned is an [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) enumeration value that indicates the type of the next action in the control's redo queue.</span></span>

<span data-ttu-id="25218-113">Se non sono presenti azioni ripristinabili o il tipo della successiva azione ripetibile è sconosciuto, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="25218-113">If there are no redoable actions or the type of the next redoable action is unknown, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="25218-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="25218-114">Remarks</span></span>

<span data-ttu-id="25218-115">I tipi di azioni che possono essere annullati o ripetuti includono operazioni di digitazione, eliminazione, trascinamento, taglia e incolla.</span><span class="sxs-lookup"><span data-stu-id="25218-115">The types of actions that can be undone or redone include typing, delete, drag-drop, cut, and paste operations.</span></span> <span data-ttu-id="25218-116">Queste informazioni possono essere utili per le applicazioni che forniscono un'interfaccia utente estesa per operazioni di annullamento e ripristino, ad esempio una casella di riepilogo a discesa di azioni ripristinabili.</span><span class="sxs-lookup"><span data-stu-id="25218-116">This information can be useful for applications that provide an extended user interface for undo and redo operations, such as a drop-down list box of redoable actions.</span></span>

## <a name="requirements"></a><span data-ttu-id="25218-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25218-117">Requirements</span></span>



| <span data-ttu-id="25218-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="25218-118">Requirement</span></span> | <span data-ttu-id="25218-119">Valore</span><span class="sxs-lookup"><span data-stu-id="25218-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25218-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25218-120">Minimum supported client</span></span><br/> | <span data-ttu-id="25218-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25218-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25218-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25218-122">Minimum supported server</span></span><br/> | <span data-ttu-id="25218-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="25218-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25218-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25218-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="25218-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="25218-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25218-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25218-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="25218-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="25218-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="25218-128">**EM \_ GETundoname**</span><span class="sxs-lookup"><span data-stu-id="25218-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="25218-129">**\_ripetizione em**</span><span class="sxs-lookup"><span data-stu-id="25218-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="25218-130">**\_Annulla**</span><span class="sxs-lookup"><span data-stu-id="25218-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

[<span data-ttu-id="25218-131">**UNDONAMEID**</span><span class="sxs-lookup"><span data-stu-id="25218-131">**UNDONAMEID**</span></span>](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





