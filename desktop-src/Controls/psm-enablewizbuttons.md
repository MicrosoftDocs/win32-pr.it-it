---
title: Messaggio PSM_ENABLEWIZBUTTONS (Prsht. h)
description: Abilita o Disabilita uno dei pulsanti standard in una procedura guidata Aero. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro EnableWizButtons di PropSheet.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- Controlli di Windows Message PSM_ENABLEWIZBUTTONS
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01fb30fa3337aed369c2cd24a1296785bd6b3a79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964470"
---
# <a name="psm_enablewizbuttons-message"></a><span data-ttu-id="67986-105">\_Messaggio ENABLEWIZBUTTONS di PSM</span><span class="sxs-lookup"><span data-stu-id="67986-105">PSM\_ENABLEWIZBUTTONS message</span></span>

<span data-ttu-id="67986-106">Abilita o Disabilita uno dei pulsanti standard in una procedura guidata Aero.</span><span class="sxs-lookup"><span data-stu-id="67986-106">Enables or disables any of the standard buttons in an Aero wizard.</span></span> <span data-ttu-id="67986-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ EnableWizButtons di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) .</span><span class="sxs-lookup"><span data-stu-id="67986-107">You can send this message explicitly or use the [**PropSheet\_EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="67986-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="67986-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67986-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67986-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67986-110">Uno o più dei valori seguenti che specificano quali pulsanti della finestra delle proprietà devono essere abilitati.</span><span class="sxs-lookup"><span data-stu-id="67986-110">One or more of the following values that specify which property sheet buttons are to be enabled.</span></span> <span data-ttu-id="67986-111">Se il valore di un pulsante è incluso sia in questo parametro che in *lParam*, è abilitato.</span><span class="sxs-lookup"><span data-stu-id="67986-111">If a button value is included in both this parameter and *lParam*, it is enabled.</span></span>



| <span data-ttu-id="67986-112">Valore</span><span class="sxs-lookup"><span data-stu-id="67986-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="67986-113">Significato</span><span class="sxs-lookup"><span data-stu-id="67986-113">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="67986-114"><dt>**PSWIZB \_ indietro**</dt></span><span class="sxs-lookup"><span data-stu-id="67986-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="67986-115">Pulsante **indietro** .</span><span class="sxs-lookup"><span data-stu-id="67986-115">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="67986-116"><dt>**\_annullamento PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="67986-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="67986-117">Pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="67986-117">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="67986-118"><dt>**\_DISABLEDFINISH PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="67986-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="67986-119">Pulsante **fine** .</span><span class="sxs-lookup"><span data-stu-id="67986-119">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="67986-120"><dt>**\_fine PSWIZB**</dt></span><span class="sxs-lookup"><span data-stu-id="67986-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="67986-121">Pulsante **fine** .</span><span class="sxs-lookup"><span data-stu-id="67986-121">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="67986-122"><dt>**PSWIZB \_ successivo**</dt></span><span class="sxs-lookup"><span data-stu-id="67986-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="67986-123">Pulsante **Avanti** .</span><span class="sxs-lookup"><span data-stu-id="67986-123">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="67986-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67986-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="67986-125">Uno o più degli stessi valori utilizzati in *wParam*, che specificano quali pulsanti sono interessati da questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="67986-125">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="67986-126">Se il valore di un pulsante viene visualizzato in questo parametro ma non in *wParam*, significa che il pulsante deve essere disabilitato.</span><span class="sxs-lookup"><span data-stu-id="67986-126">If a button value appears in this parameter but not in *wParam*, it indicates that the button should be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67986-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67986-127">Return value</span></span>

<span data-ttu-id="67986-128">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="67986-128">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="67986-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67986-129">Requirements</span></span>



| <span data-ttu-id="67986-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="67986-130">Requirement</span></span> | <span data-ttu-id="67986-131">Valore</span><span class="sxs-lookup"><span data-stu-id="67986-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67986-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67986-132">Minimum supported client</span></span><br/> | <span data-ttu-id="67986-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67986-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="67986-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67986-134">Minimum supported server</span></span><br/> | <span data-ttu-id="67986-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="67986-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="67986-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67986-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="67986-137"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="67986-137"><dt>Prsht.h</dt></span></span> </dl> |



 

 





