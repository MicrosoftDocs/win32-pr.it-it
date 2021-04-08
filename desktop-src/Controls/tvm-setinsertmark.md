---
title: Messaggio TVM_SETINSERTMARK (COMmctrl. h)
description: Imposta il segno di inserimento in un controllo di visualizzazione ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetInsertMark di TreeView.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- Controlli di Windows Message TVM_SETINSERTMARK
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5a9cc9b05e9cd7dc3281d778734bee1048ffd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874009"
---
# <a name="tvm_setinsertmark-message"></a><span data-ttu-id="dbe1f-105">\_Messaggio SETINSERTMARK TVM</span><span class="sxs-lookup"><span data-stu-id="dbe1f-105">TVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="dbe1f-106">Imposta il segno di inserimento in un controllo di visualizzazione ad albero.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-106">Sets the insertion mark in a tree-view control.</span></span> <span data-ttu-id="dbe1f-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetInsertMark di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) .</span><span class="sxs-lookup"><span data-stu-id="dbe1f-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dbe1f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dbe1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbe1f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dbe1f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dbe1f-110">Valore **bool** che specifica se il segno di inserimento viene inserito prima o dopo l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-110">**BOOL** value that specifies if the insertion mark is placed before or after the specified item.</span></span> <span data-ttu-id="dbe1f-111">Se questo argomento è diverso da zero, il segno di inserimento verrà inserito dopo l'elemento.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-111">If this argument is nonzero, the insertion mark will be placed after the item.</span></span> <span data-ttu-id="dbe1f-112">Se questo argomento è zero, il segno di inserimento verrà inserito prima dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-112">If this argument is zero, the insertion mark will be placed before the item.</span></span>

</dd> <dt>

<span data-ttu-id="dbe1f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dbe1f-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dbe1f-114">**HTREEITEM** che specifica in quale elemento verrà inserito il segno di inserimento.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-114">**HTREEITEM** that specifies at which item the insertion mark will be placed.</span></span> <span data-ttu-id="dbe1f-115">Se questo argomento è **null**, il segno di inserimento verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-115">If this argument is **NULL**, the insertion mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbe1f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dbe1f-116">Return value</span></span>

<span data-ttu-id="dbe1f-117">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-117">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbe1f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbe1f-118">Remarks</span></span>

<span data-ttu-id="dbe1f-119">In alcuni casi, il contrassegno di inserimento può essere visualizzato in due posizioni dopo l'espansione di un nodo.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-119">In some circumstances, the insert mark can appear in two places after a node is expanded.</span></span> <span data-ttu-id="dbe1f-120">Se si utilizzano segni di inserimento, è consigliabile forzare un aggiornamento del controllo dopo l'espansione di un nodo.</span><span class="sxs-lookup"><span data-stu-id="dbe1f-120">If you are using insertion marks, it is recommended that you force a refresh of the control after expanding a node.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe1f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbe1f-121">Requirements</span></span>



| <span data-ttu-id="dbe1f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbe1f-122">Requirement</span></span> | <span data-ttu-id="dbe1f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="dbe1f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe1f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbe1f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe1f-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dbe1f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dbe1f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbe1f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe1f-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dbe1f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dbe1f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dbe1f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbe1f-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe1f-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





