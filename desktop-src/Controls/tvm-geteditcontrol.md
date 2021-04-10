---
title: Messaggio TVM_GETEDITCONTROL (COMmctrl. h)
description: Recupera l'handle per il controllo di modifica utilizzato per modificare il testo di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetEditControl di TreeView.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- Controlli di Windows Message TVM_GETEDITCONTROL
topic_type:
- apiref
api_name:
- TVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b4ce0beb125218e65c2c342caf59b57473088e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121291"
---
# <a name="tvm_geteditcontrol-message"></a><span data-ttu-id="77216-105">\_Messaggio GETEDITCONTROL TVM</span><span class="sxs-lookup"><span data-stu-id="77216-105">TVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="77216-106">Recupera l'handle per il controllo di modifica utilizzato per modificare il testo di un elemento della visualizzazione struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="77216-106">Retrieves the handle to the edit control being used to edit a tree-view item's text.</span></span> <span data-ttu-id="77216-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetEditControl di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) .</span><span class="sxs-lookup"><span data-stu-id="77216-107">You can send this message explicitly or by using the [**TreeView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="77216-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="77216-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77216-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77216-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="77216-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="77216-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="77216-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77216-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="77216-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="77216-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77216-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="77216-113">Return value</span></span>

<span data-ttu-id="77216-114">Restituisce l'handle per il controllo di modifica, se ha esito positivo, oppure **null** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="77216-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="77216-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="77216-115">Remarks</span></span>

<span data-ttu-id="77216-116">Quando viene avviata la modifica dell'etichetta, viene creato un controllo di modifica, ma non è posizionato o visualizzato.</span><span class="sxs-lookup"><span data-stu-id="77216-116">When label editing begins, an edit control is created, but not positioned or displayed.</span></span> <span data-ttu-id="77216-117">Prima che venga visualizzato, il controllo di visualizzazione albero Invia la finestra padre a un codice di notifica di [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="77216-117">Before it is displayed, the tree-view control sends its parent window an [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="77216-118">Per personalizzare la modifica delle etichette, implementare un gestore per [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) e fare in modo che invii un messaggio **TVM \_ GETEDITCONTROL** al controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="77216-118">To customize label editing, implement a handler for [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) and have it send a **TVM\_GETEDITCONTROL** message to the tree-view control.</span></span> <span data-ttu-id="77216-119">Se è in corso la modifica di un'etichetta, il valore restituito sarà un handle per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="77216-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="77216-120">Utilizzare questo handle per personalizzare il controllo di modifica inviando i normali messaggi **em \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="77216-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="77216-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77216-121">Requirements</span></span>



| <span data-ttu-id="77216-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="77216-122">Requirement</span></span> | <span data-ttu-id="77216-123">Valore</span><span class="sxs-lookup"><span data-stu-id="77216-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77216-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77216-124">Minimum supported client</span></span><br/> | <span data-ttu-id="77216-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77216-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77216-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77216-126">Minimum supported server</span></span><br/> | <span data-ttu-id="77216-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77216-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77216-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77216-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="77216-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77216-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





