---
title: Messaggio TVM_ENDEDITLABELNOW (COMmctrl. h)
description: Termina la modifica dell'etichetta di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro EndEditLabelNow di TreeView.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- Controlli di Windows Message TVM_ENDEDITLABELNOW
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517589"
---
# <a name="tvm_endeditlabelnow-message"></a><span data-ttu-id="9fb46-105">\_Messaggio ENDEDITLABELNOW TVM</span><span class="sxs-lookup"><span data-stu-id="9fb46-105">TVM\_ENDEDITLABELNOW message</span></span>

<span data-ttu-id="9fb46-106">Termina la modifica dell'etichetta di un elemento della visualizzazione struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="9fb46-106">Ends the editing of a tree-view item's label.</span></span> <span data-ttu-id="9fb46-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ EndEditLabelNow di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) .</span><span class="sxs-lookup"><span data-stu-id="9fb46-107">You can send this message explicitly or by using the [**TreeView\_EndEditLabelNow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9fb46-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fb46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fb46-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9fb46-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fb46-110">Variabile che indica se la modifica viene annullata senza essere salvata nell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="9fb46-110">Variable that indicates whether the editing is canceled without being saved to the label.</span></span> <span data-ttu-id="9fb46-111">Se questo parametro è **true**, il sistema Annulla la modifica senza salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="9fb46-111">If this parameter is **TRUE**, the system cancels editing without saving the changes.</span></span> <span data-ttu-id="9fb46-112">In caso contrario, il sistema salva le modifiche nell'etichetta.</span><span class="sxs-lookup"><span data-stu-id="9fb46-112">Otherwise, the system saves the changes to the label.</span></span>

</dd> <dt>

<span data-ttu-id="9fb46-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9fb46-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9fb46-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9fb46-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fb46-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fb46-115">Return value</span></span>

<span data-ttu-id="9fb46-116">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9fb46-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fb46-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fb46-117">Remarks</span></span>

<span data-ttu-id="9fb46-118">Questo messaggio fa in modo che il codice di notifica di [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) venga inviato alla finestra padre del controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="9fb46-118">This message causes the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code to be sent to the parent window of the tree-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fb46-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fb46-119">Requirements</span></span>



| <span data-ttu-id="9fb46-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fb46-120">Requirement</span></span> | <span data-ttu-id="9fb46-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9fb46-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb46-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fb46-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9fb46-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fb46-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9fb46-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fb46-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9fb46-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9fb46-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9fb46-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9fb46-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fb46-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fb46-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





