---
title: Messaggio TDM_UPDATE_ELEMENT_TEXT (COMmctrl. h)
description: Aggiorna un elemento di testo in una finestra di dialogo attività.
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- Controlli di Windows Message TDM_UPDATE_ELEMENT_TEXT
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6dac6787c68d0cbe619bbf28fa1a6383606e99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121482"
---
# <a name="tdm_update_element_text-message"></a><span data-ttu-id="fa187-104">\_Messaggio di \_ testo dell'elemento di aggiornamento TDM \_</span><span class="sxs-lookup"><span data-stu-id="fa187-104">TDM\_UPDATE\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="fa187-105">Aggiorna un elemento di testo in una finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="fa187-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa187-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa187-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa187-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa187-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa187-108">Indica l'elemento da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="fa187-108">Indicates the element to update.</span></span> <span data-ttu-id="fa187-109">Per un'illustrazione degli elementi, vedere [informazioni sulle finestre di dialogo delle attività](task-dialogs-overview.md). Questo parametro deve essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="fa187-109">(For an illustration of the elements, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values:</span></span>



| <span data-ttu-id="fa187-110">Valore</span><span class="sxs-lookup"><span data-stu-id="fa187-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="fa187-111">Significato</span><span class="sxs-lookup"><span data-stu-id="fa187-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="fa187-112"><dt>**contenuto Transparent Data Encryption \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa187-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="fa187-113">Contenuto.</span><span class="sxs-lookup"><span data-stu-id="fa187-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="fa187-114"><dt>**\_informazioni espanse Transparent Data Encryption \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa187-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="fa187-115">Informazioni espanse.</span><span class="sxs-lookup"><span data-stu-id="fa187-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="fa187-116"><dt>**piè di pagina Transparent Data Encryption \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa187-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="fa187-117">Testo del piè di pagina.</span><span class="sxs-lookup"><span data-stu-id="fa187-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="fa187-118"><dt>**\_istruzione principale di Transparent Data Encryption \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa187-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="fa187-119">Istruzione principale.</span><span class="sxs-lookup"><span data-stu-id="fa187-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="fa187-120">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa187-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa187-121">Puntatore a una stringa Unicode che contiene il nuovo testo.</span><span class="sxs-lookup"><span data-stu-id="fa187-121">Pointer to a Unicode string that contains the new text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa187-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa187-122">Return value</span></span>

<span data-ttu-id="fa187-123">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="fa187-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa187-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa187-124">Remarks</span></span>

<span data-ttu-id="fa187-125">Per evitare il ritaglio, il nuovo testo non deve essere più lungo del testo esistente.</span><span class="sxs-lookup"><span data-stu-id="fa187-125">To avoid clipping, the new text must be no longer than the existing text.</span></span> <span data-ttu-id="fa187-126">Se si imposta il testo su una stringa più breve, la finestra di dialogo non verrà ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="fa187-126">Setting the text to a shorter string does not cause the dialog box to resize.</span></span>

<span data-ttu-id="fa187-127">Se il membro **pszExpandedInformation** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usata per creare la finestra di dialogo attività era **null** e si invia un messaggio di **\_ \_ \_ testo dell'elemento di aggiornamento TDM** con \_ informazioni espanse su \_ Transparent Data Encryption, non viene eseguita alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="fa187-127">If the **pszExpandedInformation** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog was **NULL**, and you send a **TDM\_UPDATE\_ELEMENT\_TEXT** message with TDE\_EXPANDED\_INFORMATION, nothing will happen.</span></span>

<span data-ttu-id="fa187-128">Quanto sopra si applica anche al piè di pagina di piè di pagina e di Data Encryption \_ .</span><span class="sxs-lookup"><span data-stu-id="fa187-128">The above also applies to the footer and TDE\_FOOTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa187-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa187-129">Requirements</span></span>



| <span data-ttu-id="fa187-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa187-130">Requirement</span></span> | <span data-ttu-id="fa187-131">Valore</span><span class="sxs-lookup"><span data-stu-id="fa187-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa187-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa187-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fa187-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa187-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa187-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa187-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fa187-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa187-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa187-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa187-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa187-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa187-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa187-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa187-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa187-139">**\_testo dell' \_ elemento del set TDM \_**</span><span class="sxs-lookup"><span data-stu-id="fa187-139">**TDM\_SET\_ELEMENT\_TEXT**</span></span>](tdm-set-element-text.md)
</dt> </dl>

 

 





