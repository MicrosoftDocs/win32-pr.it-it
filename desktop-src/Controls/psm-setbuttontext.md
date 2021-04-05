---
title: Messaggio PSM_SETBUTTONTEXT (Prsht. h)
description: Imposta il testo su un pulsante in una procedura guidata Aero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet SetButtonText.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- Controlli di Windows Message PSM_SETBUTTONTEXT
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048256"
---
# <a name="psm_setbuttontext-message"></a><span data-ttu-id="2034c-105">\_Messaggio SETBUTTONTEXT di PSM</span><span class="sxs-lookup"><span data-stu-id="2034c-105">PSM\_SETBUTTONTEXT message</span></span>

<span data-ttu-id="2034c-106">Imposta il testo su un pulsante in una procedura guidata Aero.</span><span class="sxs-lookup"><span data-stu-id="2034c-106">Sets the text on a button in an Aero wizard.</span></span> <span data-ttu-id="2034c-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) .</span><span class="sxs-lookup"><span data-stu-id="2034c-107">You can send this message explicitly or by using the [**PropSheet\_SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2034c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2034c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2034c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2034c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2034c-110">Uno dei valori seguenti che specifica il pulsante il cui testo è impostato.</span><span class="sxs-lookup"><span data-stu-id="2034c-110">One of the following values specifying the button whose text is set.</span></span>



| <span data-ttu-id="2034c-111">Valore</span><span class="sxs-lookup"><span data-stu-id="2034c-111">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="2034c-112">Significato</span><span class="sxs-lookup"><span data-stu-id="2034c-112">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="2034c-113"><dt>**PSWIZB \_ indietro**</dt></span><span class="sxs-lookup"><span data-stu-id="2034c-113"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="2034c-114">Pulsante **indietro** .</span><span class="sxs-lookup"><span data-stu-id="2034c-114">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="2034c-115"><dt>**\_annullamento PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="2034c-115"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="2034c-116">Pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="2034c-116">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="2034c-117"><dt>**\_DISABLEDFINISH PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="2034c-117"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="2034c-118">Pulsante **fine** .</span><span class="sxs-lookup"><span data-stu-id="2034c-118">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="2034c-119"><dt>**\_fine PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="2034c-119"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="2034c-120">Pulsante **fine** .</span><span class="sxs-lookup"><span data-stu-id="2034c-120">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="2034c-121"><dt>**PSWIZB \_ successivo**</dt></span><span class="sxs-lookup"><span data-stu-id="2034c-121"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="2034c-122">Pulsante **Avanti** .</span><span class="sxs-lookup"><span data-stu-id="2034c-122">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="2034c-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2034c-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2034c-124">Testo da impostare.</span><span class="sxs-lookup"><span data-stu-id="2034c-124">The text to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2034c-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2034c-125">Return value</span></span>

<span data-ttu-id="2034c-126">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2034c-126">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2034c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2034c-127">Requirements</span></span>



| <span data-ttu-id="2034c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2034c-128">Requirement</span></span> | <span data-ttu-id="2034c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2034c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2034c-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2034c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2034c-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2034c-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2034c-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2034c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2034c-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2034c-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2034c-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2034c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2034c-135"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="2034c-135"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="2034c-136">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2034c-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2034c-137">**PSM \_ SETBUTTONTEXTW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="2034c-137">**PSM\_SETBUTTONTEXTW** (Unicode)</span></span><br/>                                       |



 

 





