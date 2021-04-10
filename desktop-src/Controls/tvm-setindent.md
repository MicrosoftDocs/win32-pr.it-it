---
title: Messaggio TVM_SETINDENT (COMmctrl. h)
description: Imposta la larghezza del rientro per un controllo di visualizzazione albero e ridisegnato il controllo in modo da riflettere la nuova larghezza. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro di Sedentazione TreeView.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- Controlli di Windows Message TVM_SETINDENT
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85263c7c4330a692dc08949870a0eaa92f2b22c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120103"
---
# <a name="tvm_setindent-message"></a><span data-ttu-id="dcd9b-105">\_Messaggio di rientro TVM</span><span class="sxs-lookup"><span data-stu-id="dcd9b-105">TVM\_SETINDENT message</span></span>

<span data-ttu-id="dcd9b-106">Imposta la larghezza del rientro per un controllo di visualizzazione albero e ridisegnato il controllo in modo da riflettere la nuova larghezza.</span><span class="sxs-lookup"><span data-stu-id="dcd9b-106">Sets the width of indentation for a tree-view control and redraws the control to reflect the new width.</span></span> <span data-ttu-id="dcd9b-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro di [**\_ sedentazione TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) .</span><span class="sxs-lookup"><span data-stu-id="dcd9b-107">You can send this message explicitly or by using the [**TreeView\_SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dcd9b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcd9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcd9b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dcd9b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dcd9b-110">Larghezza, in pixel, del rientro.</span><span class="sxs-lookup"><span data-stu-id="dcd9b-110">Width, in pixels, of the indentation.</span></span> <span data-ttu-id="dcd9b-111">Se questo parametro è inferiore alla larghezza minima definita dal sistema, la nuova larghezza viene impostata sul valore minimo definito dal sistema.</span><span class="sxs-lookup"><span data-stu-id="dcd9b-111">If this parameter is less than the system-defined minimum width, the new width is set to the system-defined minimum.</span></span>

</dd> <dt>

<span data-ttu-id="dcd9b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dcd9b-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dcd9b-113">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="dcd9b-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcd9b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcd9b-114">Return value</span></span>

<span data-ttu-id="dcd9b-115">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="dcd9b-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcd9b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="dcd9b-116">Remarks</span></span>

<span data-ttu-id="dcd9b-117">Il valore di rientro minimo definito dal sistema è in genere di cinque pixel, ma non è corretto.</span><span class="sxs-lookup"><span data-stu-id="dcd9b-117">The system-defined minimum indent value is typically five pixels, but it is not fixed.</span></span> <span data-ttu-id="dcd9b-118">Per recuperare il valore esatto del rientro minimo in un particolare sistema, inviare un messaggio di **\_ sedentazione TVM** con *wParam* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="dcd9b-118">To retrieve the exact value of the minimum indent on a particular system, send a **TVM\_SETINDENT** message with *wParam* set to zero.</span></span> <span data-ttu-id="dcd9b-119">Inviare quindi un messaggio [**TVM \_ GetIndent**](tvm-getindent.md) per recuperare il valore di rientro minimo.</span><span class="sxs-lookup"><span data-stu-id="dcd9b-119">Then send a [**TVM\_GETINDENT**](tvm-getindent.md) message to retrieve the minimum indent value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcd9b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcd9b-120">Requirements</span></span>



| <span data-ttu-id="dcd9b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcd9b-121">Requirement</span></span> | <span data-ttu-id="dcd9b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="dcd9b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dcd9b-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcd9b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dcd9b-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dcd9b-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dcd9b-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcd9b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dcd9b-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dcd9b-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dcd9b-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcd9b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcd9b-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcd9b-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcd9b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcd9b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcd9b-130">**\_Sedentazione TreeView**</span><span class="sxs-lookup"><span data-stu-id="dcd9b-130">**TreeView\_SetIndent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





