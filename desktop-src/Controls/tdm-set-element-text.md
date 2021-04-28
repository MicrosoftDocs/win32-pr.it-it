---
title: TDM_SET_ELEMENT_TEXT messaggio (Commctrl.h)
description: 'TDM_SET_ELEMENT_TEXT: aggiorna un elemento di testo in una finestra di dialogo attività.'
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT di windows del messaggio
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0c8830a6d8a1057ab283a9e096434a6184151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104029"
---
# <a name="tdm_set_element_text-message"></a><span data-ttu-id="c71f6-104">TDM \_ SET ELEMENT TEXT \_ \_ message</span><span class="sxs-lookup"><span data-stu-id="c71f6-104">TDM\_SET\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="c71f6-105">Aggiorna un elemento di testo in una finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="c71f6-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="c71f6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c71f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c71f6-107">*wParam* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c71f6-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c71f6-108">Indica l'elemento da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="c71f6-108">Indicates the element to update.</span></span> <span data-ttu-id="c71f6-109">Per un'illustrazione, vedere [Informazioni sulle finestre di dialogo attività.](task-dialogs-overview.md) Questo parametro deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c71f6-109">(For an illustration, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values.</span></span>



| <span data-ttu-id="c71f6-110">Valore</span><span class="sxs-lookup"><span data-stu-id="c71f6-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="c71f6-111">Significato</span><span class="sxs-lookup"><span data-stu-id="c71f6-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="c71f6-112"><dt>**CONTENUTO \_ TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="c71f6-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="c71f6-113">Contenuto.</span><span class="sxs-lookup"><span data-stu-id="c71f6-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="c71f6-114"><dt>**INFORMAZIONI TDE \_ \_ ESPANSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c71f6-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="c71f6-115">Informazioni espanse.</span><span class="sxs-lookup"><span data-stu-id="c71f6-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="c71f6-116"><dt>**PIÈ DI PAGINA \_ TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="c71f6-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="c71f6-117">Testo del piè di pagina.</span><span class="sxs-lookup"><span data-stu-id="c71f6-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="c71f6-118"><dt>**ISTRUZIONE PRINCIPALE \_ TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c71f6-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="c71f6-119">Istruzione principale.</span><span class="sxs-lookup"><span data-stu-id="c71f6-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="c71f6-120">*lParam* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c71f6-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c71f6-121">Nuovo testo da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c71f6-121">The new text to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c71f6-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c71f6-122">Return value</span></span>

<span data-ttu-id="c71f6-123">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="c71f6-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="c71f6-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="c71f6-124">Remarks</span></span>

<span data-ttu-id="c71f6-125">Le dimensioni o il layout della finestra di dialogo attività possono cambiare in base al nuovo testo.</span><span class="sxs-lookup"><span data-stu-id="c71f6-125">The size or layout of the task dialog may change to accommodate the new text.</span></span>

## <a name="examples"></a><span data-ttu-id="c71f6-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="c71f6-126">Examples</span></span>

<span data-ttu-id="c71f6-127">Nell'esempio di codice seguente viene illustrato come impostare il testo del piè di pagina nella finestra di dialogo attività rappresentata da *hwnd*.</span><span class="sxs-lookup"><span data-stu-id="c71f6-127">The following example code shows how to set the footer text in the task dialog represented by *hwnd*.</span></span>


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a><span data-ttu-id="c71f6-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c71f6-128">Requirements</span></span>



| <span data-ttu-id="c71f6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c71f6-129">Requirement</span></span> | <span data-ttu-id="c71f6-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c71f6-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c71f6-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c71f6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c71f6-132">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c71f6-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c71f6-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c71f6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c71f6-134">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c71f6-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c71f6-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c71f6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c71f6-136"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="c71f6-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c71f6-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c71f6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c71f6-138">**TESTO DELL'ELEMENTO \_ UPDATE \_ TDM \_**</span><span class="sxs-lookup"><span data-stu-id="c71f6-138">**TDM\_UPDATE\_ELEMENT\_TEXT**</span></span>](tdm-update-element-text.md)
</dt> </dl>

 

 





