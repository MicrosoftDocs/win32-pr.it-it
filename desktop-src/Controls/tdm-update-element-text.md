---
title: TDM_UPDATE_ELEMENT_TEXT messaggio (Commctrl.h)
description: 'TDM_UPDATE_ELEMENT_TEXT messaggio: aggiorna un elemento di testo in una finestra di dialogo attività.'
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- TDM_UPDATE_ELEMENT_TEXT messaggio controlli Windows
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
ms.openlocfilehash: c155b426b92645c0b9cdbabe00c44ffa722b89f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085809"
---
# <a name="tdm_update_element_text-message"></a><span data-ttu-id="19229-104">TDM \_ UPDATE ELEMENT TEXT \_ \_ message</span><span class="sxs-lookup"><span data-stu-id="19229-104">TDM\_UPDATE\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="19229-105">Aggiorna un elemento di testo in una finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="19229-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="19229-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="19229-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19229-107">*wParam* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="19229-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19229-108">Indica l'elemento da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="19229-108">Indicates the element to update.</span></span> <span data-ttu-id="19229-109">Per un'illustrazione degli elementi, vedere [Informazioni sui dialoghe attività.](task-dialogs-overview.md) Questo parametro deve essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="19229-109">(For an illustration of the elements, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values:</span></span>



| <span data-ttu-id="19229-110">Valore</span><span class="sxs-lookup"><span data-stu-id="19229-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="19229-111">Significato</span><span class="sxs-lookup"><span data-stu-id="19229-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="19229-112"><dt>**CONTENUTO \_ TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="19229-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="19229-113">Contenuto.</span><span class="sxs-lookup"><span data-stu-id="19229-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="19229-114"><dt>**INFORMAZIONI ESPANSE DI TDE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="19229-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="19229-115">Informazioni espanse.</span><span class="sxs-lookup"><span data-stu-id="19229-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="19229-116"><dt>**PIÈ DI PAGINA TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="19229-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="19229-117">Testo del piè di pagina.</span><span class="sxs-lookup"><span data-stu-id="19229-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="19229-118"><dt>**ISTRUZIONE PRINCIPALE \_ TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="19229-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="19229-119">Istruzione main.</span><span class="sxs-lookup"><span data-stu-id="19229-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="19229-120">*lParam* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="19229-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19229-121">Puntatore a una stringa Unicode contenente il nuovo testo.</span><span class="sxs-lookup"><span data-stu-id="19229-121">Pointer to a Unicode string that contains the new text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19229-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19229-122">Return value</span></span>

<span data-ttu-id="19229-123">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="19229-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="19229-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="19229-124">Remarks</span></span>

<span data-ttu-id="19229-125">Per evitare il ritaglio, il nuovo testo non deve essere più lungo del testo esistente.</span><span class="sxs-lookup"><span data-stu-id="19229-125">To avoid clipping, the new text must be no longer than the existing text.</span></span> <span data-ttu-id="19229-126">L'impostazione del testo su una stringa più breve non determina il ridimensionamento della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="19229-126">Setting the text to a shorter string does not cause the dialog box to resize.</span></span>

<span data-ttu-id="19229-127">Se il membro **pszExpandedInformation** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usato per creare la finestra di dialogo attività è **NULL** e si invia un messaggio **TDM \_ UPDATE ELEMENT \_ \_ TEXT** con TDE EXPANDED INFORMATION, non verrà fatto \_ \_ nulla.</span><span class="sxs-lookup"><span data-stu-id="19229-127">If the **pszExpandedInformation** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog was **NULL**, and you send a **TDM\_UPDATE\_ELEMENT\_TEXT** message with TDE\_EXPANDED\_INFORMATION, nothing will happen.</span></span>

<span data-ttu-id="19229-128">Il codice precedente si applica anche al piè di pagina e al piè di pagina \_ TDE.</span><span class="sxs-lookup"><span data-stu-id="19229-128">The above also applies to the footer and TDE\_FOOTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="19229-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19229-129">Requirements</span></span>



| <span data-ttu-id="19229-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="19229-130">Requirement</span></span> | <span data-ttu-id="19229-131">Valore</span><span class="sxs-lookup"><span data-stu-id="19229-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19229-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19229-132">Minimum supported client</span></span><br/> | <span data-ttu-id="19229-133">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="19229-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19229-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19229-134">Minimum supported server</span></span><br/> | <span data-ttu-id="19229-135">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="19229-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19229-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19229-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="19229-137"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="19229-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19229-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19229-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19229-139">**TESTO DELL'ELEMENTO SET TDM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="19229-139">**TDM\_SET\_ELEMENT\_TEXT**</span></span>](tdm-set-element-text.md)
</dt> </dl>

 

 





