---
title: Messaggio PSM_RESTARTWINDOWS (Prsht. h)
description: Indica che è necessario riavviare Windows per rendere effettive le modifiche.
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- Controlli di Windows Message PSM_RESTARTWINDOWS
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb12126ae0a2b9187a941ccc1aff53186a0cda7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873653"
---
# <a name="psm_restartwindows-message"></a><span data-ttu-id="1dd87-104">\_Messaggio RESTARTWINDOWS di PSM</span><span class="sxs-lookup"><span data-stu-id="1dd87-104">PSM\_RESTARTWINDOWS message</span></span>

<span data-ttu-id="1dd87-105">Indica che è necessario riavviare Windows per rendere effettive le modifiche.</span><span class="sxs-lookup"><span data-stu-id="1dd87-105">Indicates that Windows needs to be restarted for the changes to take effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="1dd87-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1dd87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dd87-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1dd87-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1dd87-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1dd87-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1dd87-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1dd87-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1dd87-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1dd87-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dd87-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1dd87-111">Return value</span></span>

<span data-ttu-id="1dd87-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="1dd87-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dd87-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1dd87-113">Remarks</span></span>

<span data-ttu-id="1dd87-114">Un'applicazione deve inviare questo messaggio solo in risposta al codice di notifica [PSN \_ Apply](psn-apply.md) o [PSN \_ KILLACTIVE](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="1dd87-114">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span> <span data-ttu-id="1dd87-115">È possibile inviare il messaggio **PSM \_ RESTARTWINDOWS** in modo esplicito o usando la macro [**PropSheet \_ RESTARTWINDOWS**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) .</span><span class="sxs-lookup"><span data-stu-id="1dd87-115">You can send the **PSM\_RESTARTWINDOWS** message explicitly or by using the [**PropSheet\_RestartWindows**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) macro.</span></span>

<span data-ttu-id="1dd87-116">Questo messaggio fa in modo che la funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) restituisca il \_ valore ID PSRESTARTWINDOWS, ma solo se l'utente fa clic sul pulsante **OK** per chiudere la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="1dd87-116">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSRESTARTWINDOWS value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="1dd87-117">È responsabilità dell'applicazione riavviare Windows, operazione che può essere eseguita tramite la funzione [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="1dd87-117">It is the application's responsibility to restart Windows, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

> [!Note]  
> <span data-ttu-id="1dd87-118">Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="1dd87-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1dd87-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dd87-119">Requirements</span></span>



| <span data-ttu-id="1dd87-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dd87-120">Requirement</span></span> | <span data-ttu-id="1dd87-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1dd87-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd87-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dd87-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1dd87-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1dd87-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1dd87-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dd87-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1dd87-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1dd87-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1dd87-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1dd87-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dd87-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd87-127"><dt>Prsht.h</dt></span></span> </dl> |



 

