---
title: Messaggio PSM_ISDIALOGMESSAGE (Prsht. h)
description: Passa un messaggio a una finestra di dialogo della finestra delle proprietà e indica se la finestra di dialogo ha elaborato il messaggio. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet IsDialogMessage.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- Controlli di Windows Message PSM_ISDIALOGMESSAGE
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b753fc849d76e3ac5071dd85bdd94950460fbb10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873889"
---
# <a name="psm_isdialogmessage-message"></a><span data-ttu-id="d784e-105">\_Messaggio ISDIALOGMESSAGE di PSM</span><span class="sxs-lookup"><span data-stu-id="d784e-105">PSM\_ISDIALOGMESSAGE message</span></span>

<span data-ttu-id="d784e-106">Passa un messaggio a una finestra di dialogo della finestra delle proprietà e indica se la finestra di dialogo ha elaborato il messaggio.</span><span class="sxs-lookup"><span data-stu-id="d784e-106">Passes a message to a property sheet dialog box and indicates whether the dialog box processed the message.</span></span> <span data-ttu-id="d784e-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) .</span><span class="sxs-lookup"><span data-stu-id="d784e-107">You can send this message explicitly or by using the [**PropSheet\_IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d784e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d784e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d784e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d784e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d784e-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d784e-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d784e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d784e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d784e-112">Puntatore a una struttura di [**messaggi**](/windows/win32/api/winuser/ns-winuser-msg) contenente il messaggio da verificare.</span><span class="sxs-lookup"><span data-stu-id="d784e-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d784e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d784e-113">Return value</span></span>

<span data-ttu-id="d784e-114">Restituisce **true** se il messaggio è stato elaborato oppure **false** se il messaggio non è stato elaborato.</span><span class="sxs-lookup"><span data-stu-id="d784e-114">Returns **TRUE** if the message has been processed, or **FALSE** if the message has not been processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d784e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d784e-115">Remarks</span></span>

<span data-ttu-id="d784e-116">Il ciclo di messaggi deve usare il messaggio **PSM \_ ISDIALOGMESSAGE** con finestre delle proprietà non modali per passare i messaggi alla finestra di dialogo della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d784e-116">Your message loop should use the **PSM\_ISDIALOGMESSAGE** message with modeless property sheets to pass messages to the property sheet dialog box.</span></span> <span data-ttu-id="d784e-117">Nei sistemi che supportano Unicode, utilizzare le versioni Unicode delle funzioni [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) e [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**GetMessageW** e **PeekMessageW**) per recuperare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="d784e-117">On systems that support Unicode, use the Unicode versions of the [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) functions (**GetMessageW** and **PeekMessageW**) to retrieve messages.</span></span>

<span data-ttu-id="d784e-118">Se il valore restituito indica che il messaggio è stato elaborato, non deve essere passato alla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) o [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .</span><span class="sxs-lookup"><span data-stu-id="d784e-118">If the return value indicates that the message was processed, it must not be passed to the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) or [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function.</span></span>

> [!Note]  
> <span data-ttu-id="d784e-119">Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="d784e-119">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d784e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d784e-120">Requirements</span></span>



| <span data-ttu-id="d784e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d784e-121">Requirement</span></span> | <span data-ttu-id="d784e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d784e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d784e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d784e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d784e-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d784e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d784e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d784e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d784e-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d784e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d784e-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d784e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d784e-128"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="d784e-128"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d784e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d784e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d784e-130">**PropertySheet**</span><span class="sxs-lookup"><span data-stu-id="d784e-130">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

