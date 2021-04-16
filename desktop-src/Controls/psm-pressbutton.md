---
title: Messaggio PSM_PRESSBUTTON (Prsht. h)
description: Simula la selezione di un pulsante della finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet PressButton.
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- Controlli di Windows Message PSM_PRESSBUTTON
topic_type:
- apiref
api_name:
- PSM_PRESSBUTTON
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b54b04dcc7b1263019f49ff8c1de0d2c21a12a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479409"
---
# <a name="psm_pressbutton-message"></a><span data-ttu-id="9df18-105">\_Messaggio PRESSBUTTON di PSM</span><span class="sxs-lookup"><span data-stu-id="9df18-105">PSM\_PRESSBUTTON message</span></span>

<span data-ttu-id="9df18-106">Simula la selezione di un pulsante della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="9df18-106">Simulates the selection of a property sheet button.</span></span> <span data-ttu-id="9df18-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) .</span><span class="sxs-lookup"><span data-stu-id="9df18-107">You can send this message explicitly or by using the [**PropSheet\_PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9df18-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9df18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9df18-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9df18-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9df18-110">Indice del pulsante da selezionare.</span><span class="sxs-lookup"><span data-stu-id="9df18-110">Index of the button to select.</span></span> <span data-ttu-id="9df18-111">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9df18-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="9df18-112">Valore</span><span class="sxs-lookup"><span data-stu-id="9df18-112">Value</span></span>                                                                                                                                                            | <span data-ttu-id="9df18-113">Significato</span><span class="sxs-lookup"><span data-stu-id="9df18-113">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <span data-ttu-id="9df18-114"><dt>**\_APPLYNOW PSBTN**</dt></span><span class="sxs-lookup"><span data-stu-id="9df18-114"><dt>**PSBTN\_APPLYNOW**</dt></span></span> </dl> | <span data-ttu-id="9df18-115">Seleziona il pulsante **applica** .</span><span class="sxs-lookup"><span data-stu-id="9df18-115">Selects the **Apply** button.</span></span> <span data-ttu-id="9df18-116">Questo valore non è valido quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="9df18-116">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <span data-ttu-id="9df18-117"><dt>**PSBTN \_ indietro**</dt></span><span class="sxs-lookup"><span data-stu-id="9df18-117"><dt>**PSBTN\_BACK**</dt></span></span> </dl>             | <span data-ttu-id="9df18-118">Consente di selezionare il pulsante **indietro** .</span><span class="sxs-lookup"><span data-stu-id="9df18-118">Selects the **Back** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <span data-ttu-id="9df18-119"><dt>**\_annullamento PSBTN**</dt></span><span class="sxs-lookup"><span data-stu-id="9df18-119"><dt>**PSBTN\_CANCEL**</dt></span></span> </dl>       | <span data-ttu-id="9df18-120">Consente di selezionare il pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="9df18-120">Selects the **Cancel** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <span data-ttu-id="9df18-121"><dt>**\_fine PSBTN**</dt></span><span class="sxs-lookup"><span data-stu-id="9df18-121"><dt>**PSBTN\_FINISH**</dt></span></span> </dl>       | <span data-ttu-id="9df18-122">Consente di selezionare il pulsante **fine** .</span><span class="sxs-lookup"><span data-stu-id="9df18-122">Selects the **Finish** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <span data-ttu-id="9df18-123"><dt>**Guida di PSBTN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9df18-123"><dt>**PSBTN\_HELP**</dt></span></span> </dl>             | <span data-ttu-id="9df18-124">**Consente** di selezionare il pulsante?.</span><span class="sxs-lookup"><span data-stu-id="9df18-124">Selects the **Help** button.</span></span> <span data-ttu-id="9df18-125">Questo valore non è valido quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="9df18-125">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <span data-ttu-id="9df18-126"><dt>**PSBTN \_ successivo**</dt></span><span class="sxs-lookup"><span data-stu-id="9df18-126"><dt>**PSBTN\_NEXT**</dt></span></span> </dl>             | <span data-ttu-id="9df18-127">Consente di selezionare il pulsante **Avanti** .</span><span class="sxs-lookup"><span data-stu-id="9df18-127">Selects the **Next** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <span data-ttu-id="9df18-128"><dt>**PSBTN \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9df18-128"><dt>**PSBTN\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="9df18-129">Seleziona il pulsante **OK** .</span><span class="sxs-lookup"><span data-stu-id="9df18-129">Selects the **OK** button.</span></span> <span data-ttu-id="9df18-130">Questo valore non è valido quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="9df18-130">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="9df18-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9df18-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9df18-132">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9df18-132">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9df18-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9df18-133">Return value</span></span>

<span data-ttu-id="9df18-134">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="9df18-134">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9df18-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9df18-135">Requirements</span></span>



| <span data-ttu-id="9df18-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="9df18-136">Requirement</span></span> | <span data-ttu-id="9df18-137">Valore</span><span class="sxs-lookup"><span data-stu-id="9df18-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9df18-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9df18-138">Minimum supported client</span></span><br/> | <span data-ttu-id="9df18-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9df18-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9df18-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9df18-140">Minimum supported server</span></span><br/> | <span data-ttu-id="9df18-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9df18-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9df18-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9df18-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="9df18-143"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="9df18-143"><dt>Prsht.h</dt></span></span> </dl> |



 

 





