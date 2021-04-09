---
title: Messaggio PSM_CANCELTOCLOSE (Prsht. h)
description: Inviato da un'applicazione quando ha eseguito modifiche dopo la notifica di applicazione PSN più recente \_ che non può essere annullata. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet CancelToClose.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- Controlli di Windows Message PSM_CANCELTOCLOSE
topic_type:
- apiref
api_name:
- PSM_CANCELTOCLOSE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1377801fddeeb52badee55869ace7e9c2277c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120835"
---
# <a name="psm_canceltoclose-message"></a><span data-ttu-id="9517e-105">\_Messaggio CANCELTOCLOSE di PSM</span><span class="sxs-lookup"><span data-stu-id="9517e-105">PSM\_CANCELTOCLOSE message</span></span>

<span data-ttu-id="9517e-106">Inviato da un'applicazione quando ha eseguito modifiche dopo la notifica di applicazione [PSN \_ ](psn-apply.md) più recente che non può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="9517e-106">Sent by an application when it has performed changes since the most recent [PSN\_APPLY](psn-apply.md) notification that cannot be canceled.</span></span> <span data-ttu-id="9517e-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) .</span><span class="sxs-lookup"><span data-stu-id="9517e-107">You can send this message explicitly or by using the [**PropSheet\_CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9517e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9517e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9517e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9517e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9517e-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9517e-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9517e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9517e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9517e-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9517e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9517e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9517e-113">Return value</span></span>

<span data-ttu-id="9517e-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="9517e-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9517e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9517e-115">Remarks</span></span>

<span data-ttu-id="9517e-116">**PSM \_ CANCELTOCLOSE** Disabilita il pulsante **Annulla** e modifica il testo del pulsante **OK** in "close".</span><span class="sxs-lookup"><span data-stu-id="9517e-116">**PSM\_CANCELTOCLOSE** disables the **Cancel** button and changes the text of the **OK** button to "Close".</span></span>

<span data-ttu-id="9517e-117">La maggior parte delle finestre delle proprietà attende di eseguire modifiche irreversibili fino a quando non \_ viene ricevuta una notifica di applicazione PSN.</span><span class="sxs-lookup"><span data-stu-id="9517e-117">Most property sheets wait to perform irreversible changes until a PSN\_APPLY notification is received.</span></span> <span data-ttu-id="9517e-118">In alcune circostanze, tuttavia, una finestra delle proprietà può apportare modifiche irreversibili al di fuori della sequenza di reimpostazione di PSN \_ Apply/PSN standard \_ .</span><span class="sxs-lookup"><span data-stu-id="9517e-118">However, in some circumstances, a property sheet may make irreversible changes outside the standard PSN\_APPLY/PSN\_RESET sequence.</span></span> <span data-ttu-id="9517e-119">Un esempio è una finestra delle proprietà che contiene un pulsante **modifica** utilizzato per visualizzare una finestra di dialogo per la modifica di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="9517e-119">One example is a property sheet that contains an **Edit** button that is used to display a subdialog box for editing a property.</span></span> <span data-ttu-id="9517e-120">Quando l'utente fa clic su **OK** per inviare la modifica, nella pagina della finestra delle proprietà sono disponibili diverse opzioni.</span><span class="sxs-lookup"><span data-stu-id="9517e-120">When the user clicks **OK** to submit the change, the property sheet page has several options.</span></span>

-   <span data-ttu-id="9517e-121">Può registrare le modifiche, ma attendere fino a quando non riceve una \_ notifica di applicazione PSN per applicarle.</span><span class="sxs-lookup"><span data-stu-id="9517e-121">It can record the changes, but wait until it receives a PSN\_APPLY notification to apply them.</span></span> <span data-ttu-id="9517e-122">Si tratta dell'approccio preferito.</span><span class="sxs-lookup"><span data-stu-id="9517e-122">This is the preferred approach.</span></span>
-   <span data-ttu-id="9517e-123">È possibile applicare le modifiche immediatamente dopo aver chiuso la finestra di dialogo, ma ricordare le impostazioni originali.</span><span class="sxs-lookup"><span data-stu-id="9517e-123">It can apply the changes immediately after exiting the subdialog box, but remember the original settings.</span></span> <span data-ttu-id="9517e-124">Queste impostazioni possono essere usate per ripristinare lo stato originale se \_ viene ricevuta una notifica di reimpostazione di PSN.</span><span class="sxs-lookup"><span data-stu-id="9517e-124">Those settings can be used to restore the original state if a PSN\_RESET notification is received.</span></span>
-   <span data-ttu-id="9517e-125">Può applicare immediatamente le modifiche e non tentare di ripristinare le impostazioni originali quando riceve una notifica di [ \_ reimpostazione di PSN](psn-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="9517e-125">It can apply the changes immediately and not attempt to restore the original settings when it receives a [PSN\_RESET](psn-reset.md) notification.</span></span> <span data-ttu-id="9517e-126">Questo approccio non è consigliato, ma potrebbe essere necessario se le modifiche sono troppo ampie perché le altre due opzioni siano pratiche.</span><span class="sxs-lookup"><span data-stu-id="9517e-126">This approach is not recommended, but may be necessary if the changes are too far-reaching for the other two options to be practical.</span></span>

<span data-ttu-id="9517e-127">Per la terza opzione, le applicazioni devono inviare un messaggio **PSM \_ CANCELTOCLOSE** alla finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="9517e-127">For the third option, applications should send a **PSM\_CANCELTOCLOSE** message to the property sheet.</span></span> <span data-ttu-id="9517e-128">Indica all'utente che le modifiche apportate con la finestra di dialogo subdialog non possono essere annullate facendo clic sul pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="9517e-128">It indicates to the user that the changes made with the subdialog box cannot be reversed by clicking the **Cancel** button.</span></span>

> [!Note]  
> <span data-ttu-id="9517e-129">Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="9517e-129">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9517e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9517e-130">Requirements</span></span>



| <span data-ttu-id="9517e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9517e-131">Requirement</span></span> | <span data-ttu-id="9517e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9517e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9517e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9517e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9517e-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9517e-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9517e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9517e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9517e-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9517e-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9517e-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9517e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9517e-138"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="9517e-138"><dt>Prsht.h</dt></span></span> </dl> |



 

 





