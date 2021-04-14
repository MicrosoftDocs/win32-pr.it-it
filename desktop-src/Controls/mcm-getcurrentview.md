---
title: Messaggio MCM_GETCURRENTVIEW (COMmctrl. h)
description: Ottiene la visualizzazione corrente del calendario. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetCurrentView.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- Controlli di Windows Message MCM_GETCURRENTVIEW
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebbd6a2b33043294b64b8b65308520b52dbe449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478491"
---
# <a name="mcm_getcurrentview-message"></a><span data-ttu-id="4c6bc-105">\_Messaggio GETCURRENTVIEW MCM</span><span class="sxs-lookup"><span data-stu-id="4c6bc-105">MCM\_GETCURRENTVIEW message</span></span>

<span data-ttu-id="4c6bc-106">Ottiene la visualizzazione corrente del calendario.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-106">Gets the current view of the calendar.</span></span> <span data-ttu-id="4c6bc-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="4c6bc-107">You can send this message explicitly or by using the [**MonthCal\_GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c6bc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c6bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c6bc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c6bc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c6bc-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4c6bc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c6bc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c6bc-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c6bc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c6bc-113">Return value</span></span>

<span data-ttu-id="4c6bc-114">Visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-114">Current view.</span></span> <span data-ttu-id="4c6bc-115">Uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-115">One of the following values.</span></span>



| <span data-ttu-id="4c6bc-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4c6bc-116">Return code</span></span>                                                                                  | <span data-ttu-id="4c6bc-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c6bc-117">Description</span></span>              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="4c6bc-118"><dt>**\_mese MCMV**</dt></span><span class="sxs-lookup"><span data-stu-id="4c6bc-118"><dt>**MCMV\_MONTH**</dt></span></span> </dl>   | <span data-ttu-id="4c6bc-119">Visualizzazione mensile.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-119">Monthly view.</span></span><br/> |
| <dl> <span data-ttu-id="4c6bc-120"><dt>**MCMV \_ anno**</dt></span><span class="sxs-lookup"><span data-stu-id="4c6bc-120"><dt>**MCMV\_YEAR**</dt></span></span> </dl>    | <span data-ttu-id="4c6bc-121">Visualizzazione annuale.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-121">Annual view.</span></span><br/>  |
| <dl> <span data-ttu-id="4c6bc-122"><dt>**MCMV \_ decennio**</dt></span><span class="sxs-lookup"><span data-stu-id="4c6bc-122"><dt>**MCMV\_DECADE**</dt></span></span> </dl>  | <span data-ttu-id="4c6bc-123">Visualizzazione decade.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-123">Decade view.</span></span><br/>  |
| <dl> <span data-ttu-id="4c6bc-124"><dt>**MCMV \_ secolo**</dt></span><span class="sxs-lookup"><span data-stu-id="4c6bc-124"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="4c6bc-125">Visualizzazione secolo.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-125">Century view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4c6bc-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c6bc-126">Requirements</span></span>



| <span data-ttu-id="4c6bc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c6bc-127">Requirement</span></span> | <span data-ttu-id="4c6bc-128">Valore</span><span class="sxs-lookup"><span data-stu-id="4c6bc-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c6bc-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c6bc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4c6bc-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c6bc-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4c6bc-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c6bc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4c6bc-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c6bc-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c6bc-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c6bc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c6bc-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c6bc-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





