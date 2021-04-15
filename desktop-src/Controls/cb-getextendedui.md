---
title: Messaggio CB_GETEXTENDEDUI (winuser. h)
description: Determina se una casella combinata dispone dell'interfaccia utente predefinita o dell'interfaccia utente estesa.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- Controlli di Windows Message CB_GETEXTENDEDUI
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476655"
---
# <a name="cb_getextendedui-message"></a><span data-ttu-id="a63a8-104">\_Messaggio GETEXTENDEDUI CB</span><span class="sxs-lookup"><span data-stu-id="a63a8-104">CB\_GETEXTENDEDUI message</span></span>

<span data-ttu-id="a63a8-105">Determina se una casella combinata dispone dell'interfaccia utente predefinita o dell'interfaccia utente estesa.</span><span class="sxs-lookup"><span data-stu-id="a63a8-105">Determines whether a combo box has the default user interface or the extended user interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="a63a8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a63a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a63a8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a63a8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a63a8-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a63a8-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a63a8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a63a8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a63a8-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a63a8-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a63a8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a63a8-111">Return value</span></span>

<span data-ttu-id="a63a8-112">Se la casella combinata dispone dell'interfaccia utente estesa, il valore restituito è **true**; in caso contrario, è **false**.</span><span class="sxs-lookup"><span data-stu-id="a63a8-112">If the combo box has the extended user interface, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a63a8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a63a8-113">Remarks</span></span>

<span data-ttu-id="a63a8-114">Per impostazione predefinita, il tasto F4 apre o chiude l'elenco e la freccia in giù modifica la selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="a63a8-114">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="a63a8-115">In una casella combinata con l'interfaccia utente estesa, il tasto F4 è disabilitato e premendo il tasto freccia giù si apre l'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="a63a8-115">In a combo box with the extended user interface, the F4 key is disabled and pressing the DOWN ARROW key opens the drop-down list.</span></span>

## <a name="requirements"></a><span data-ttu-id="a63a8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a63a8-116">Requirements</span></span>



| <span data-ttu-id="a63a8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a63a8-117">Requirement</span></span> | <span data-ttu-id="a63a8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a63a8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a63a8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a63a8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a63a8-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a63a8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a63a8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a63a8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a63a8-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a63a8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a63a8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a63a8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a63a8-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a63a8-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a63a8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a63a8-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="a63a8-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a63a8-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a63a8-127">**CB \_ SETEXTENDEDUI**</span><span class="sxs-lookup"><span data-stu-id="a63a8-127">**CB\_SETEXTENDEDUI**</span></span>](cb-setextendedui.md)
</dt> <dt>

<span data-ttu-id="a63a8-128">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a63a8-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a63a8-129">Funzionalità della casella combinata</span><span class="sxs-lookup"><span data-stu-id="a63a8-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





