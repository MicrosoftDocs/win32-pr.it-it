---
title: Messaggio MCM_SETCALID (COMmctrl. h)
description: Imposta l'ID calendario per il controllo calendario specificato. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- Controlli di Windows Message MCM_SETCALID
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a661a685062fe737a1927c3a6ab455e8499c6ca9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047997"
---
# <a name="mcm_setcalid-message"></a><span data-ttu-id="d5309-105">Messaggio in MCM \_</span><span class="sxs-lookup"><span data-stu-id="d5309-105">MCM\_SETCALID message</span></span>

<span data-ttu-id="d5309-106">Imposta l'ID calendario per il controllo calendario specificato.</span><span class="sxs-lookup"><span data-stu-id="d5309-106">Sets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="d5309-107">È possibile inviare questo messaggio in modo esplicito o usando [**la \_ macro MonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) .</span><span class="sxs-lookup"><span data-stu-id="d5309-107">You can send this message explicitly or by using the [**MonthCal\_SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5309-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5309-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5309-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5309-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5309-110">ID del calendario.</span><span class="sxs-lookup"><span data-stu-id="d5309-110">The calendar ID.</span></span> <span data-ttu-id="d5309-111">Una delle costanti degli [identificatori del calendario](/windows/desktop/Intl/calendar-identifiers) .</span><span class="sxs-lookup"><span data-stu-id="d5309-111">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

</dd> <dt>

<span data-ttu-id="d5309-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5309-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5309-113">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d5309-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5309-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5309-114">Return value</span></span>

<span data-ttu-id="d5309-115">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d5309-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5309-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5309-116">Requirements</span></span>



| <span data-ttu-id="d5309-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5309-117">Requirement</span></span> | <span data-ttu-id="d5309-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d5309-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5309-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5309-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d5309-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5309-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5309-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5309-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d5309-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5309-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5309-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5309-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5309-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5309-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

