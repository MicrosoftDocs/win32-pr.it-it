---
title: Messaggio SBM_ENABLE_ARROWS (winuser. h)
description: Un'applicazione invia il \_ messaggio di abilitazione della \_ freccia SBM per abilitare o disabilitare una o entrambe le frecce di un controllo barra di scorrimento.
ms.assetid: 9646826a-3a7c-490b-822d-7511e4ef2262
keywords:
- Controlli di Windows Message SBM_ENABLE_ARROWS
topic_type:
- apiref
api_name:
- SBM_ENABLE_ARROWS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78895b43ec7908172a6164917b33ac8549088db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964635"
---
# <a name="sbm_enable_arrows-message"></a><span data-ttu-id="1403a-104">\_Messaggio di abilitazione delle frecce di SBM \_</span><span class="sxs-lookup"><span data-stu-id="1403a-104">SBM\_ENABLE\_ARROWS message</span></span>

<span data-ttu-id="1403a-105">Un'applicazione invia il messaggio di **\_ Abilitazione della \_ freccia SBM** per abilitare o disabilitare una o entrambe le frecce di un controllo barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="1403a-105">An application sends the **SBM\_ENABLE\_ARROWS** message to enable or disable one or both arrows of a scroll bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1403a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1403a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1403a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1403a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1403a-108">Specifica se le frecce della barra di scorrimento sono abilitate o disabilitate e indicano quali frecce sono abilitate o disabilitate.</span><span class="sxs-lookup"><span data-stu-id="1403a-108">Specifies whether the scroll bar arrows are enabled or disabled and indicates which arrows are enabled or disabled.</span></span> <span data-ttu-id="1403a-109">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1403a-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="1403a-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1403a-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="1403a-111">Significato</span><span class="sxs-lookup"><span data-stu-id="1403a-111">Meaning</span></span>                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="ESB_DISABLE_BOTH"></span><span id="esb_disable_both"></span><dl> <span data-ttu-id="1403a-112"><dt>**ESB \_ Disabilita \_ entrambi**</dt></span><span class="sxs-lookup"><span data-stu-id="1403a-112"><dt>**ESB\_DISABLE\_BOTH**</dt></span></span> </dl> | <span data-ttu-id="1403a-113">Disabilita entrambe le frecce su una barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="1403a-113">Disables both arrows on a scroll bar.</span></span><br/>                                                           |
| <span id="ESB_DISABLE_DOWN"></span><span id="esb_disable_down"></span><dl> <span data-ttu-id="1403a-114"><dt>**\_disabilitazione \_ ESB**</dt></span><span class="sxs-lookup"><span data-stu-id="1403a-114"><dt>**ESB\_DISABLE\_DOWN**</dt></span></span> </dl> | <span data-ttu-id="1403a-115">Disabilita la freccia giù su una barra di scorrimento verticale.</span><span class="sxs-lookup"><span data-stu-id="1403a-115">Disables the down arrow on a vertical scroll bar.</span></span><br/>                                               |
| <span id="ESB_DISABLE_LTUP"></span><span id="esb_disable_ltup"></span><dl> <span data-ttu-id="1403a-116"><dt>**ESB \_ disabilitare \_ LTUP**</dt></span><span class="sxs-lookup"><span data-stu-id="1403a-116"><dt>**ESB\_DISABLE\_LTUP**</dt></span></span> </dl> | <span data-ttu-id="1403a-117">Disabilita la freccia sinistra su una barra di scorrimento orizzontale o la freccia su su una barra di scorrimento verticale.</span><span class="sxs-lookup"><span data-stu-id="1403a-117">Disables the left arrow on a horizontal scroll bar or the up arrow on a vertical scroll bar.</span></span><br/>    |
| <span id="ESB_DISABLE_LEFT"></span><span id="esb_disable_left"></span><dl> <span data-ttu-id="1403a-118"><dt>**ESB \_ Disable \_ Left**</dt></span><span class="sxs-lookup"><span data-stu-id="1403a-118"><dt>**ESB\_DISABLE\_LEFT**</dt></span></span> </dl> | <span data-ttu-id="1403a-119">Disabilita la freccia sinistra su una barra di scorrimento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="1403a-119">Disables the left arrow on a horizontal scroll bar.</span></span><br/>                                             |
| <span id="ESB_DISABLE_RTDN"></span><span id="esb_disable_rtdn"></span><dl> <span data-ttu-id="1403a-120"><dt>**ESB \_ disabilitare \_ RTDN**</dt></span><span class="sxs-lookup"><span data-stu-id="1403a-120"><dt>**ESB\_DISABLE\_RTDN**</dt></span></span> </dl> | <span data-ttu-id="1403a-121">Disabilita la freccia destra su una barra di scorrimento orizzontale o sulla freccia in giù su una barra di scorrimento verticale.</span><span class="sxs-lookup"><span data-stu-id="1403a-121">Disables the right arrow on a horizontal scroll bar or the down arrow on a vertical scroll bar.</span></span><br/> |
| <span id="ESB_DISABLE_UP"></span><span id="esb_disable_up"></span><dl> <span data-ttu-id="1403a-122"><dt>**\_disabilitazione \_ ESB**</dt></span><span class="sxs-lookup"><span data-stu-id="1403a-122"><dt>**ESB\_DISABLE\_UP**</dt></span></span> </dl>       | <span data-ttu-id="1403a-123">Disabilita la freccia su su una barra di scorrimento verticale.</span><span class="sxs-lookup"><span data-stu-id="1403a-123">Disables the up arrow on a vertical scroll bar.</span></span><br/>                                                 |
| <span id="ESB_ENABLE_BOTH"></span><span id="esb_enable_both"></span><dl> <span data-ttu-id="1403a-124"><dt>**ESB \_ Abilita \_ entrambi**</dt></span><span class="sxs-lookup"><span data-stu-id="1403a-124"><dt>**ESB\_ENABLE\_BOTH**</dt></span></span> </dl>    | <span data-ttu-id="1403a-125">Abilita entrambe le frecce su una barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="1403a-125">Enables both arrows on a scroll bar.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="1403a-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1403a-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1403a-127">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="1403a-127">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1403a-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1403a-128">Return value</span></span>

<span data-ttu-id="1403a-129">Se il messaggio ha esito positivo, il valore restituito è **true**; in caso contrario, è **false**.</span><span class="sxs-lookup"><span data-stu-id="1403a-129">If the message succeeds, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1403a-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1403a-130">Requirements</span></span>



| <span data-ttu-id="1403a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1403a-131">Requirement</span></span> | <span data-ttu-id="1403a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="1403a-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1403a-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1403a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1403a-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1403a-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1403a-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1403a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1403a-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1403a-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1403a-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1403a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1403a-138"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1403a-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





