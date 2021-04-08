---
title: Messaggio TDM_UPDATE_ICON (COMmctrl. h)
description: Aggiorna l'icona di una finestra di dialogo attività.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- Controlli di Windows Message TDM_UPDATE_ICON
topic_type:
- apiref
api_name:
- TDM_UPDATE_ICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2da73ebb3bf0355f50bc08a08f0b35de97576b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964936"
---
# <a name="tdm_update_icon-message"></a><span data-ttu-id="8828b-104">Messaggio dell'icona di \_ aggiornamento TDM \_</span><span class="sxs-lookup"><span data-stu-id="8828b-104">TDM\_UPDATE\_ICON message</span></span>

<span data-ttu-id="8828b-105">Aggiorna l'icona di una finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="8828b-105">Refreshes the icon of a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="8828b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8828b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8828b-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8828b-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8828b-108">Indica l'elemento icona da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="8828b-108">Indicates which icon element to update.</span></span> <span data-ttu-id="8828b-109">Questo parametro deve essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8828b-109">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="8828b-110">Valore</span><span class="sxs-lookup"><span data-stu-id="8828b-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="8828b-111">Significato</span><span class="sxs-lookup"><span data-stu-id="8828b-111">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <span data-ttu-id="8828b-112"><dt>**icona di TDIE \_ \_ principale**</dt></span><span class="sxs-lookup"><span data-stu-id="8828b-112"><dt>**TDIE\_ICON\_MAIN**</dt></span></span> </dl>       | <span data-ttu-id="8828b-113">Icona principale.</span><span class="sxs-lookup"><span data-stu-id="8828b-113">Main icon.</span></span><br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <span data-ttu-id="8828b-114"><dt>**piè di pagina \_ icona TDIe \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8828b-114"><dt>**TDIE\_ICON\_FOOTER**</dt></span></span> </dl> | <span data-ttu-id="8828b-115">Icona piè di pagina.</span><span class="sxs-lookup"><span data-stu-id="8828b-115">Footer icon.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8828b-116">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8828b-116">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8828b-117">Puntatore a una stringa (PCWSTR) o handle a un'icona (HICON) da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="8828b-117">A pointer to a string (PCWSTR) or handle to an icon (HICON) to display.</span></span> <span data-ttu-id="8828b-118">Se *lParam* è **null**, non viene visualizzata alcuna icona, indipendentemente dal valore di *wParam*.</span><span class="sxs-lookup"><span data-stu-id="8828b-118">If *lParam* is **NULL**, no icon is displayed, regardless of the value of *wParam*.</span></span>

<span data-ttu-id="8828b-119">Se il valore di *wParam* è TDIe \_ icona \_ principale e il TDF \_ usare \_ il \_ flag principale HICON è impostato sul membro **dwFlags** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizzata per creare la finestra di dialogo attività, *lParam* deve contenere un handle per un'icona (HICON) da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="8828b-119">If the value of *wParam* is TDIE\_ICON\_MAIN and the TDF\_USE\_HICON\_MAIN flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="8828b-120">Se il valore di *wParam* è il piè di pagina dell' \_ icona TDIe \_ e il TDF usa il flag di piè di pagina di \_ \_ HICON \_ è impostato sul membro **dwFlags** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizzata per creare la finestra di dialogo attività, *lParam* deve contenere un handle per un'icona (HICON) da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="8828b-120">If the value of *wParam* is TDIE\_ICON\_FOOTER and the TDF\_USE\_HICON\_FOOTER flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="8828b-121">Se il TDF \_ Usa \_ HICON \_ Main o TDF \_ usare \_ i \_ flag del piè di pagina HICON **non** sono impostati per il membro **dwFlags** , *lParam* deve puntare a una stringa Unicode con terminazione null (PCWSTR) che contiene un identificatore di risorsa valido passato attraverso la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="8828b-121">If the TDF\_USE\_HICON\_MAIN or TDF\_USE\_HICON\_FOOTER flags are **not** set on the **dwFlags** member, *lParam* must point to a null-terminated, Unicode string (PCWSTR) that contains a valid resource identifier passed through the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="8828b-122">L'icona viene visualizzata in base al valore di *wParam*: se il valore è TDIe \_ icona \_ principale, l'icona viene visualizzata nell'intestazione; se il valore è TDIe \_ icona \_ piè di pagina, l'icona viene visualizzata nel piè di pagina.</span><span class="sxs-lookup"><span data-stu-id="8828b-122">The icon is displayed based on the value of *wParam*: if the value is TDIE\_ICON\_MAIN, the icon is displayed in the header; if the value is TDIE\_ICON\_FOOTER, the icon is displayed in the footer.</span></span> <span data-ttu-id="8828b-123">La risorsa deve essere dal modulo delle risorse dell'applicazione (specificato nel membro **HINSTANCE** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) ) oppure, se **HINSTANCE** è **null**, dal modulo Resource del sistema (imageres.dll).</span><span class="sxs-lookup"><span data-stu-id="8828b-123">The resource must be either from the application's resource module (specified in the **hInstance** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure), or if **hInstance** is **NULL**, from the system's resource module (imageres.dll).</span></span> <span data-ttu-id="8828b-124">Per identificare una risorsa di sistema, usare un identificatore di sistema valido passato attraverso la macro **MAKEINTRESOURCE** o uno dei valori predefiniti seguenti da COMmctrl. h:</span><span class="sxs-lookup"><span data-stu-id="8828b-124">To identify a system resource, use a valid system identifier passed through the **MAKEINTRESOURCE** macro or one of the following predefined values from commctrl.h:</span></span>



| <span data-ttu-id="8828b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8828b-125">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="8828b-126">Significato</span><span class="sxs-lookup"><span data-stu-id="8828b-126">Meaning</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <span data-ttu-id="8828b-127"><dt>**\_icona di errore TD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8828b-127"><dt>**TD\_ERROR\_ICON**</dt></span></span> </dl>                   | <span data-ttu-id="8828b-128">Icona del segno di arresto.</span><span class="sxs-lookup"><span data-stu-id="8828b-128">A stop sign icon.</span></span><br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <span data-ttu-id="8828b-129"><dt>**\_icona di avviso TD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8828b-129"><dt>**TD\_WARNING\_ICON**</dt></span></span> </dl>             | <span data-ttu-id="8828b-130">Icona di punto esclamativo.</span><span class="sxs-lookup"><span data-stu-id="8828b-130">An exclamation point icon.</span></span><br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <span data-ttu-id="8828b-131"><dt>**\_icona informazioni \_ TD**</dt></span><span class="sxs-lookup"><span data-stu-id="8828b-131"><dt>**TD\_INFORMATION\_ICON**</dt></span></span> </dl> | <span data-ttu-id="8828b-132">Lettera minuscola "i" in un'icona a cerchio.</span><span class="sxs-lookup"><span data-stu-id="8828b-132">A lowercase letter "i" in a circle icon.</span></span><br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <span data-ttu-id="8828b-133"><dt>**\_icona scudo \_ TD**</dt></span><span class="sxs-lookup"><span data-stu-id="8828b-133"><dt>**TD\_SHIELD\_ICON**</dt></span></span> </dl>                | <span data-ttu-id="8828b-134">Icona dello scudo di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8828b-134">A security shield icon.</span></span><br/>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8828b-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8828b-135">Return value</span></span>

<span data-ttu-id="8828b-136">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="8828b-136">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="8828b-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="8828b-137">Remarks</span></span>

<span data-ttu-id="8828b-138">Il layout della finestra di dialogo attività con l'icona potrebbe non riuscire e questo potrebbe non essere riflesso nel valore restituito.</span><span class="sxs-lookup"><span data-stu-id="8828b-138">The layout of the task dialog with the icon may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="8828b-139">Un valore restituito di S \_ OK riflette solo il fatto che la finestra di dialogo attività ha ricevuto il messaggio e ha tentato di elaborarlo.</span><span class="sxs-lookup"><span data-stu-id="8828b-139">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="8828b-140">Se il layout della finestra di dialogo attività ha esito negativo, la finestra di dialogo verrà chiusa e viene restituito un codice **HRESULT** nella funzione di callback registrata.</span><span class="sxs-lookup"><span data-stu-id="8828b-140">If the layout of the task dialog fails, the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="8828b-141">Per ulteriori informazioni sulla sintassi della funzione di callback, vedere [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span><span class="sxs-lookup"><span data-stu-id="8828b-141">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

<span data-ttu-id="8828b-142">Se la finestra di dialogo attività viene creata senza un piè di pagina (ovvero i membri del piè di pagina appropriati della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usata per creare la finestra di dialogo attività sono **null**) e questo messaggio viene inviato, un piè di pagina non viene aggiunto dinamicamente alla finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="8828b-142">If the task dialog is created without a footer (that is, the appropriate footer members of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog are **NULL**) and this message is sent, a footer is not dynamically added to the task dialog.</span></span> <span data-ttu-id="8828b-143">Lo stesso vale per l'invio di questo messaggio per aggiornare un'icona di intestazione quando viene creata una finestra di dialogo attività senza un'intestazione.</span><span class="sxs-lookup"><span data-stu-id="8828b-143">The same is true for sending this message to update a header icon when a task dialog is created without a header.</span></span> <span data-ttu-id="8828b-144">Per aggiungere un'intestazione o un piè di pagina in fase di esecuzione, utilizzare la funzionalità [**TDM \_ Navigate \_ Page**](tdm-navigate-page.md) .</span><span class="sxs-lookup"><span data-stu-id="8828b-144">To add a header or footer at run time, use the [**TDM\_NAVIGATE\_PAGE**](tdm-navigate-page.md) functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="8828b-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8828b-145">Requirements</span></span>



| <span data-ttu-id="8828b-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="8828b-146">Requirement</span></span> | <span data-ttu-id="8828b-147">Valore</span><span class="sxs-lookup"><span data-stu-id="8828b-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8828b-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8828b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="8828b-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8828b-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8828b-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8828b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="8828b-151">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8828b-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8828b-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8828b-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="8828b-153"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8828b-153"><dt>Commctrl.h</dt></span></span> </dl> |



 

