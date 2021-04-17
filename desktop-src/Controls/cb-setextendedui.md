---
title: Messaggio CB_SETEXTENDEDUI (winuser. h)
description: Un'applicazione invia un \_ messaggio CB SETEXTENDEDUI per selezionare l'interfaccia utente predefinita o l'interfaccia utente estesa per una casella combinata con l' \_ elenco a discesa CBS o \_ lo stile DropDownList CBS.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- Controlli di Windows Message CB_SETEXTENDEDUI
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94c31c8bc5457799d0038ecd8340c03c55aed91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476636"
---
# <a name="cb_setextendedui-message"></a><span data-ttu-id="d1cf2-104">\_Messaggio SETEXTENDEDUI CB</span><span class="sxs-lookup"><span data-stu-id="d1cf2-104">CB\_SETEXTENDEDUI message</span></span>

<span data-ttu-id="d1cf2-105">Un'applicazione invia un messaggio **CB \_ SETEXTENDEDUI** per selezionare l'interfaccia utente predefinita o l'interfaccia utente estesa per una casella combinata con l' [**elenco a \_ discesa CBS**](combo-box-styles.md) o lo stile [**\_ DropDownList CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d1cf2-105">An application sends a **CB\_SETEXTENDEDUI** message to select either the default UI or the extended UI for a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1cf2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1cf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1cf2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1cf2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1cf2-108">**Bool** che specifica se la casella combinata utilizza l'interfaccia utente estesa (**true**) o l'interfaccia utente predefinita (**false**).</span><span class="sxs-lookup"><span data-stu-id="d1cf2-108">A **BOOL** that specifies whether the combo box uses the extended UI (**TRUE**) or the default UI (**FALSE**).</span></span>

</dd> <dt>

<span data-ttu-id="d1cf2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1cf2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1cf2-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="d1cf2-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1cf2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1cf2-111">Return value</span></span>

<span data-ttu-id="d1cf2-112">Se l'operazione ha esito positivo, il valore restituito è CB \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d1cf2-112">If the operation succeeds, the return value is CB\_OKAY.</span></span> <span data-ttu-id="d1cf2-113">Se si verifica un errore, è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="d1cf2-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1cf2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1cf2-114">Remarks</span></span>

<span data-ttu-id="d1cf2-115">Per impostazione predefinita, il tasto F4 apre o chiude l'elenco e la freccia in giù modifica la selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="d1cf2-115">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="d1cf2-116">Nell'interfaccia utente estesa il tasto F4 è disabilitato e il tasto freccia giù apre l'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="d1cf2-116">In the extended UI, the F4 key is disabled and the DOWN ARROW key opens the drop-down list.</span></span> <span data-ttu-id="d1cf2-117">La rotellina del mouse, che in genere scorre gli elementi nell'elenco, non ha alcun effetto quando viene impostata l'interfaccia utente estesa.</span><span class="sxs-lookup"><span data-stu-id="d1cf2-117">The mouse wheel, which normally scrolls through the items in the list, has no effect when the extended UI is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1cf2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1cf2-118">Requirements</span></span>



| <span data-ttu-id="d1cf2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1cf2-119">Requirement</span></span> | <span data-ttu-id="d1cf2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d1cf2-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1cf2-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1cf2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d1cf2-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1cf2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d1cf2-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1cf2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d1cf2-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d1cf2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d1cf2-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1cf2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1cf2-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1cf2-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1cf2-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1cf2-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1cf2-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d1cf2-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d1cf2-129">**CB \_ GETEXTENDEDUI**</span><span class="sxs-lookup"><span data-stu-id="d1cf2-129">**CB\_GETEXTENDEDUI**</span></span>](cb-getextendedui.md)
</dt> <dt>

<span data-ttu-id="d1cf2-130">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d1cf2-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d1cf2-131">Funzionalità della casella combinata</span><span class="sxs-lookup"><span data-stu-id="d1cf2-131">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





