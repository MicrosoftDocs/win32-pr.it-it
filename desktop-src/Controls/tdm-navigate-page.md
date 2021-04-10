---
title: Messaggio TDM_NAVIGATE_PAGE (COMmctrl. h)
description: Ricrea una finestra di dialogo attività con nuovo contenuto, simulando la funzionalità di una procedura guidata a più pagine.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- Controlli di Windows Message TDM_NAVIGATE_PAGE
topic_type:
- apiref
api_name:
- TDM_NAVIGATE_PAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56fc86e0e4fe457a43e035ed5d568e91303c7fcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964849"
---
# <a name="tdm_navigate_page-message"></a><span data-ttu-id="23cd6-104">Messaggio della pagina di \_ spostamento TDM \_</span><span class="sxs-lookup"><span data-stu-id="23cd6-104">TDM\_NAVIGATE\_PAGE message</span></span>

<span data-ttu-id="23cd6-105">Ricrea una finestra di dialogo attività con nuovo contenuto, simulando la funzionalità di una procedura guidata a più pagine.</span><span class="sxs-lookup"><span data-stu-id="23cd6-105">Recreates a task dialog with new contents, simulating the functionality of a multi-page wizard.</span></span>

## <a name="parameters"></a><span data-ttu-id="23cd6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="23cd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23cd6-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23cd6-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23cd6-108">Non usato.</span><span class="sxs-lookup"><span data-stu-id="23cd6-108">Not used.</span></span> <span data-ttu-id="23cd6-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="23cd6-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="23cd6-110">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23cd6-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23cd6-111">Puntatore a una struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) che descrive la finestra di dialogo attività da creare.</span><span class="sxs-lookup"><span data-stu-id="23cd6-111">A pointer to a [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that describes the task dialog to create.</span></span> <span data-ttu-id="23cd6-112">L'applicazione chiamante deve allocare questa struttura e impostare i relativi membri.</span><span class="sxs-lookup"><span data-stu-id="23cd6-112">The calling application must allocate this structure and set its members.</span></span> <span data-ttu-id="23cd6-113">I valori dei membri variano a seconda del tipo di pagina a cui l'utente accede.</span><span class="sxs-lookup"><span data-stu-id="23cd6-113">The values of the members vary depending on the kind of page the user navigates to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23cd6-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23cd6-114">Return value</span></span>

<span data-ttu-id="23cd6-115">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="23cd6-115">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="23cd6-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="23cd6-116">Remarks</span></span>

<span data-ttu-id="23cd6-117">Per avviare una finestra di dialogo attività procedura guidata, usare la funzione [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="23cd6-117">To launch a wizard task dialog, use the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="23cd6-118">Quando l'utente accede tramite la procedura guidata, invia questo messaggio alla finestra di dialogo attività per visualizzare la pagina successiva.</span><span class="sxs-lookup"><span data-stu-id="23cd6-118">As the user navigates using the wizard, send this message to the task dialog to display the next page.</span></span> <span data-ttu-id="23cd6-119">Viene creata una nuova finestra di dialogo attività (simile a una nuova pagina) con gli elementi specificati nella struttura a cui punta *lParam*.</span><span class="sxs-lookup"><span data-stu-id="23cd6-119">A new task dialog (looks like a new page) is created with the elements specified in the structure pointed to by *lParam*.</span></span> <span data-ttu-id="23cd6-120">Al momento della creazione, l'intero contenuto del frame della finestra di dialogo viene eliminato e ricostruito.</span><span class="sxs-lookup"><span data-stu-id="23cd6-120">At creation, the entire contents of the dialog frame are destroyed and reconstructed.</span></span> <span data-ttu-id="23cd6-121">Di conseguenza, tutte le informazioni sullo stato contenute nei controlli (ad esempio, un indicatore di stato, un pulsante expando o una casella di controllo di verifica) nella finestra di dialogo andranno perse.</span><span class="sxs-lookup"><span data-stu-id="23cd6-121">As a result, any state information held by controls (for example, a progress bar, expando button, or verification checkbox) in the dialog is lost.</span></span>

<span data-ttu-id="23cd6-122">Il layout della finestra di dialogo attività potrebbe non riuscire e questo potrebbe non essere riflesso nel valore restituito.</span><span class="sxs-lookup"><span data-stu-id="23cd6-122">The layout of the task dialog may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="23cd6-123">Un valore restituito di S \_ OK riflette solo il fatto che la finestra di dialogo attività ha ricevuto il messaggio e ha tentato di elaborarlo.</span><span class="sxs-lookup"><span data-stu-id="23cd6-123">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="23cd6-124">Se il layout della finestra di dialogo attività ha esito negativo (non è possibile visualizzare la finestra di dialogo attività), la finestra di dialogo verrà chiusa e viene restituito un codice **HRESULT** nella funzione di callback registrata.</span><span class="sxs-lookup"><span data-stu-id="23cd6-124">If the layout of the task dialog fails (the task dialog cannot be displayed), the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="23cd6-125">Per ulteriori informazioni sulla sintassi della funzione di callback, vedere [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span><span class="sxs-lookup"><span data-stu-id="23cd6-125">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

## <a name="requirements"></a><span data-ttu-id="23cd6-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23cd6-126">Requirements</span></span>



| <span data-ttu-id="23cd6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="23cd6-127">Requirement</span></span> | <span data-ttu-id="23cd6-128">Valore</span><span class="sxs-lookup"><span data-stu-id="23cd6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23cd6-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23cd6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="23cd6-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23cd6-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23cd6-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23cd6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="23cd6-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="23cd6-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23cd6-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23cd6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="23cd6-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="23cd6-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

