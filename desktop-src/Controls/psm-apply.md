---
title: Messaggio PSM_APPLY (Prsht. h)
description: Simula la selezione del pulsante Applica, che indica che una o più pagine sono state modificate ed è necessario convalidare e registrare le modifiche.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- Controlli di Windows Message PSM_APPLY
topic_type:
- apiref
api_name:
- PSM_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d798d4a9a2f780ac81cc84c90a57d0efd4e299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874257"
---
# <a name="psm_apply-message"></a><span data-ttu-id="96300-104">\_Messaggio di applicazione PSM</span><span class="sxs-lookup"><span data-stu-id="96300-104">PSM\_APPLY message</span></span>

<span data-ttu-id="96300-105">Simula la selezione del pulsante **applica** , che indica che una o più pagine sono state modificate ed è necessario convalidare e registrare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="96300-105">Simulates the selection of the **Apply** button, indicating that one or more pages have changed and the changes need to be validated and recorded.</span></span>

## <a name="parameters"></a><span data-ttu-id="96300-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="96300-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96300-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96300-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96300-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="96300-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="96300-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96300-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96300-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="96300-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96300-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96300-111">Return value</span></span>

<span data-ttu-id="96300-112">Restituisce **true** se tutte le pagine hanno applicato correttamente le modifiche. in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="96300-112">Returns **TRUE** if all pages successfully applied the changes, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="96300-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="96300-113">Remarks</span></span>

<span data-ttu-id="96300-114">La finestra delle proprietà Invia il codice di notifica [ \_ KILLACTIVE PSN](psn-killactive.md) alla pagina corrente.</span><span class="sxs-lookup"><span data-stu-id="96300-114">The property sheet sends the [PSN\_KILLACTIVE](psn-killactive.md) notification code to the current page.</span></span> <span data-ttu-id="96300-115">Se la pagina corrente restituisce **false**, la finestra delle proprietà Invia il codice di notifica di [ \_ applicazione PSN](psn-apply.md) a tutte le pagine attive.</span><span class="sxs-lookup"><span data-stu-id="96300-115">If the current page returns **FALSE**, the property sheet sends the [PSN\_APPLY](psn-apply.md) notification code to all active pages.</span></span> <span data-ttu-id="96300-116">È possibile inviare il \_ messaggio di applicazione PSM in modo esplicito o usando la macro [**PropSheet \_ Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) .</span><span class="sxs-lookup"><span data-stu-id="96300-116">You can send the PSM\_APPLY message explicitly or by using the [**PropSheet\_Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) macro.</span></span>

> [!Note]  
> <span data-ttu-id="96300-117">Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="96300-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96300-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96300-118">Requirements</span></span>



| <span data-ttu-id="96300-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="96300-119">Requirement</span></span> | <span data-ttu-id="96300-120">Valore</span><span class="sxs-lookup"><span data-stu-id="96300-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96300-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96300-121">Minimum supported client</span></span><br/> | <span data-ttu-id="96300-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96300-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="96300-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96300-123">Minimum supported server</span></span><br/> | <span data-ttu-id="96300-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96300-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="96300-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96300-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="96300-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="96300-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





