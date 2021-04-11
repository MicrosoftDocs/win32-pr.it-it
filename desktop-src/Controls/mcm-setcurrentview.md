---
title: Messaggio MCM_SETCURRENTVIEW (COMmctrl. h)
description: Imposta la visualizzazione corrente del calendario. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal SetCurrentView.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- Controlli di Windows Message MCM_SETCURRENTVIEW
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d383c984932c19805f452cb39841c2edf36809b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964856"
---
# <a name="mcm_setcurrentview-message"></a><span data-ttu-id="8d34d-105">\_Messaggio SETCURRENTVIEW MCM</span><span class="sxs-lookup"><span data-stu-id="8d34d-105">MCM\_SETCURRENTVIEW message</span></span>

<span data-ttu-id="8d34d-106">Imposta la visualizzazione corrente del calendario.</span><span class="sxs-lookup"><span data-stu-id="8d34d-106">Sets the current view of the calendar.</span></span> <span data-ttu-id="8d34d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="8d34d-107">You can send this message explicitly or by using the [**MonthCal\_SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d34d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d34d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d34d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d34d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d34d-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8d34d-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8d34d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d34d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d34d-112">Nuova vista.</span><span class="sxs-lookup"><span data-stu-id="8d34d-112">New view.</span></span> <span data-ttu-id="8d34d-113">Una delle seguenti costanti.</span><span class="sxs-lookup"><span data-stu-id="8d34d-113">One of the following constants.</span></span>



| <span data-ttu-id="8d34d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8d34d-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="8d34d-115">Significato</span><span class="sxs-lookup"><span data-stu-id="8d34d-115">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <span data-ttu-id="8d34d-116"><dt>**\_mese MCMV**</dt></span><span class="sxs-lookup"><span data-stu-id="8d34d-116"><dt>**MCMV\_MONTH**</dt></span></span> </dl>       | <span data-ttu-id="8d34d-117">Visualizzazione mensile.</span><span class="sxs-lookup"><span data-stu-id="8d34d-117">Monthly view.</span></span><br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <span data-ttu-id="8d34d-118"><dt>**MCMV \_ anno**</dt></span><span class="sxs-lookup"><span data-stu-id="8d34d-118"><dt>**MCMV\_YEAR**</dt></span></span> </dl>          | <span data-ttu-id="8d34d-119">Visualizzazione annuale.</span><span class="sxs-lookup"><span data-stu-id="8d34d-119">Annual view.</span></span><br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <span data-ttu-id="8d34d-120"><dt>**MCMV \_ decennio**</dt></span><span class="sxs-lookup"><span data-stu-id="8d34d-120"><dt>**MCMV\_DECADE**</dt></span></span> </dl>    | <span data-ttu-id="8d34d-121">Visualizzazione decade.</span><span class="sxs-lookup"><span data-stu-id="8d34d-121">Decade view.</span></span><br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <span data-ttu-id="8d34d-122"><dt>**MCMV \_ secolo**</dt></span><span class="sxs-lookup"><span data-stu-id="8d34d-122"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="8d34d-123">Visualizzazione secolo.</span><span class="sxs-lookup"><span data-stu-id="8d34d-123">Century view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d34d-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d34d-124">Return value</span></span>

<span data-ttu-id="8d34d-125">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8d34d-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d34d-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d34d-126">Requirements</span></span>



| <span data-ttu-id="8d34d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d34d-127">Requirement</span></span> | <span data-ttu-id="8d34d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8d34d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d34d-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d34d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8d34d-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d34d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d34d-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d34d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8d34d-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8d34d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d34d-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d34d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d34d-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d34d-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





