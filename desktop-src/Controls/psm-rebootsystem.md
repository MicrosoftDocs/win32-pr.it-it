---
title: Messaggio PSM_REBOOTSYSTEM (Prsht. h)
description: Indica che è necessario riavviare il sistema per rendere effettive le modifiche. È possibile inviare il \_ messaggio PSM REBOOTSYSTEM in modo esplicito o usando la \_ macro PropSheet REBOOTSYSTEM.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- Controlli di Windows Message PSM_REBOOTSYSTEM
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476060"
---
# <a name="psm_rebootsystem-message"></a><span data-ttu-id="a28b7-105">\_Messaggio REBOOTSYSTEM di PSM</span><span class="sxs-lookup"><span data-stu-id="a28b7-105">PSM\_REBOOTSYSTEM message</span></span>

<span data-ttu-id="a28b7-106">Indica che è necessario riavviare il sistema per rendere effettive le modifiche.</span><span class="sxs-lookup"><span data-stu-id="a28b7-106">Indicates the system needs to be restarted for the changes to take effect.</span></span> <span data-ttu-id="a28b7-107">È possibile inviare il messaggio **PSM \_ REBOOTSYSTEM** in modo esplicito o usando la macro [**PropSheet \_ REBOOTSYSTEM**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) .</span><span class="sxs-lookup"><span data-stu-id="a28b7-107">You can send the **PSM\_REBOOTSYSTEM** message explicitly or by using the [**PropSheet\_RebootSystem**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a28b7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a28b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a28b7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a28b7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a28b7-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a28b7-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a28b7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a28b7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a28b7-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a28b7-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a28b7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a28b7-113">Return value</span></span>

<span data-ttu-id="a28b7-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a28b7-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a28b7-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a28b7-115">Remarks</span></span>

<span data-ttu-id="a28b7-116">Un'applicazione deve inviare questo messaggio solo in risposta al messaggio di notifica [PSN \_ Apply](psn-apply.md) o [PSN \_ KILLACTIVE](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="a28b7-116">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification message.</span></span>

<span data-ttu-id="a28b7-117">Questo messaggio fa in modo che la funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) restituisca il \_ valore ID PSREBOOTSYSTEM, ma solo se l'utente fa clic sul pulsante **OK** per chiudere la finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a28b7-117">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSREBOOTSYSTEM value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="a28b7-118">È responsabilità dell'applicazione riavviare il sistema, operazione che può essere eseguita tramite la funzione [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="a28b7-118">It is the application's responsibility to reboot the system, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

<span data-ttu-id="a28b7-119">Questo messaggio sostituisce tutti i messaggi di [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) che lo precedono o lo seguono.</span><span class="sxs-lookup"><span data-stu-id="a28b7-119">This message supersedes all [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) messages that precede or follow it.</span></span>

> [!Note]  
> <span data-ttu-id="a28b7-120">Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="a28b7-120">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a28b7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a28b7-121">Requirements</span></span>



| <span data-ttu-id="a28b7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a28b7-122">Requirement</span></span> | <span data-ttu-id="a28b7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a28b7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a28b7-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a28b7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a28b7-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a28b7-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a28b7-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a28b7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a28b7-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a28b7-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a28b7-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a28b7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a28b7-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a28b7-129"><dt>Prsht.h</dt></span></span> </dl> |



 

