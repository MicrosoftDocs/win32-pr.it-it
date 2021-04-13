---
title: Messaggio PSM_GETRESULT (Prsht. h)
description: Utilizzato dalle finestre delle proprietà non modali per recuperare le informazioni restituite alle finestre delle proprietà modali da PropertySheet. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetResult PropSheet.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- Controlli di Windows Message PSM_GETRESULT
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d41609f625cbd3938fa78e9a2f91ab70168ecc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518531"
---
# <a name="psm_getresult-message"></a><span data-ttu-id="663bd-105">\_Messaggio PSM GETresult</span><span class="sxs-lookup"><span data-stu-id="663bd-105">PSM\_GETRESULT message</span></span>

<span data-ttu-id="663bd-106">Utilizzato dalle finestre delle proprietà non modali per recuperare le informazioni restituite alle finestre delle proprietà modali da [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta).</span><span class="sxs-lookup"><span data-stu-id="663bd-106">Used by modeless property sheets to retrieve the information returned to modal property sheets by [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta).</span></span> <span data-ttu-id="663bd-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetResult PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) .</span><span class="sxs-lookup"><span data-stu-id="663bd-107">You can send this message explicitly or use the [**PropSheet\_GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="663bd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="663bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="663bd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="663bd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="663bd-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="663bd-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="663bd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="663bd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="663bd-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="663bd-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="663bd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="663bd-113">Return value</span></span>

<span data-ttu-id="663bd-114">Restituisce un valore positivo se ha esito positivo oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="663bd-114">Returns a positive value if successful, or -1 otherwise.</span></span> <span data-ttu-id="663bd-115">I valori restituiti riportati di seguito hanno un significato speciale.</span><span class="sxs-lookup"><span data-stu-id="663bd-115">The following return values have a special meaning.</span></span>



| <span data-ttu-id="663bd-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="663bd-116">Return code</span></span>                                                                                         | <span data-ttu-id="663bd-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="663bd-117">Description</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="663bd-118"><dt>**ID \_ PSREBOOTSYSTEM**</dt></span><span class="sxs-lookup"><span data-stu-id="663bd-118"><dt>**ID\_PSREBOOTSYSTEM**</dt></span></span> </dl>   | <span data-ttu-id="663bd-119">Una pagina ha inviato un messaggio [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) alla finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="663bd-119">A page sent a [**PSM\_REBOOTSYSTEM**](psm-rebootsystem.md) message to the property sheet.</span></span> <span data-ttu-id="663bd-120">Per rendere effettive le modifiche dell'utente, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="663bd-120">The computer must be restarted for the user's changes to take effect.</span></span><br/> |
| <dl> <span data-ttu-id="663bd-121"><dt>**ID \_ PSRESTARTWINDOWS**</dt></span><span class="sxs-lookup"><span data-stu-id="663bd-121"><dt>**ID\_PSRESTARTWINDOWS**</dt></span></span> </dl> | <span data-ttu-id="663bd-122">Una pagina ha inviato un messaggio [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) alla finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="663bd-122">A page sent a [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) message to the property sheet.</span></span> <span data-ttu-id="663bd-123">È necessario riavviare Windows per rendere effettive le modifiche dell'utente.</span><span class="sxs-lookup"><span data-stu-id="663bd-123">Windows must be restarted for the user's changes to take effect.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="663bd-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="663bd-124">Remarks</span></span>

<span data-ttu-id="663bd-125">Per recuperare informazioni estese sugli errori, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="663bd-125">To retrieve extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="663bd-126">Il valore restituito per questo messaggio è identico a quello restituito da [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) per una finestra delle proprietà modale.</span><span class="sxs-lookup"><span data-stu-id="663bd-126">The return value for this message is identical to what [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) returns for a modal property sheet.</span></span>

[<span data-ttu-id="663bd-127">Versione 5,80.</span><span class="sxs-lookup"><span data-stu-id="663bd-127">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="663bd-128">Il valore restituito [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) contiene informazioni diverse per le finestre delle proprietà modali e non modali.</span><span class="sxs-lookup"><span data-stu-id="663bd-128">The [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) return value carries different information for modal and modeless property sheets.</span></span> <span data-ttu-id="663bd-129">In alcuni casi, le finestre delle proprietà non modali possono richiedere le informazioni ricevute da **PropertySheet** se fossero modali.</span><span class="sxs-lookup"><span data-stu-id="663bd-129">In some cases, modeless property sheets may need the information they would have received from **PropertySheet** if they had been modal.</span></span> <span data-ttu-id="663bd-130">In particolare, potrebbe essere necessario sapere se \_ è stato restituito ID PSREBOOTSYSTEM o ID \_ PSRESTARTWINDOWS.</span><span class="sxs-lookup"><span data-stu-id="663bd-130">In particular, they may need to know whether ID\_PSREBOOTSYSTEM or ID\_PSRESTARTWINDOWS would have been returned.</span></span>

<span data-ttu-id="663bd-131">Per una finestra delle proprietà non modale, il ciclo di messaggi deve usare [**PSM \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md) per passare i messaggi alla finestra di dialogo della finestra delle proprietà e [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) per determinare quando eliminare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="663bd-131">For a modeless property sheet, your message loop should use [**PSM\_ISDIALOGMESSAGE**](psm-isdialogmessage.md) to pass messages to the property sheet dialog box, and [**PSM\_GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) to determine when to destroy the dialog box.</span></span> <span data-ttu-id="663bd-132">Quando l'utente fa clic sul pulsante **OK** o **Annulla** , **PSM \_ GETCURRENTPAGEHWND** restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="663bd-132">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**.</span></span> <span data-ttu-id="663bd-133">È quindi possibile recuperare il valore ricevuto da una finestra delle proprietà modale da [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) inviando un messaggio **PSM \_ GetResult** .</span><span class="sxs-lookup"><span data-stu-id="663bd-133">You can then retrieve the value that a modal property sheet would have received from [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) by sending a **PSM\_GETRESULT** message.</span></span>

> [!Note]  
> <span data-ttu-id="663bd-134">Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="663bd-134">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="663bd-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="663bd-135">Requirements</span></span>



| <span data-ttu-id="663bd-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="663bd-136">Requirement</span></span> | <span data-ttu-id="663bd-137">Valore</span><span class="sxs-lookup"><span data-stu-id="663bd-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="663bd-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="663bd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="663bd-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="663bd-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="663bd-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="663bd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="663bd-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="663bd-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="663bd-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="663bd-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="663bd-143"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="663bd-143"><dt>Prsht.h</dt></span></span> </dl> |



 

