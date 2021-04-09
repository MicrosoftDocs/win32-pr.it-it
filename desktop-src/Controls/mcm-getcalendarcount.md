---
title: Messaggio MCM_GETCALENDARCOUNT (COMmctrl. h)
description: Ottiene il numero di calendari attualmente visualizzati nel controllo Calendar. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetCalendarCount.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- Controlli di Windows Message MCM_GETCALENDARCOUNT
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a3be9e9bcc5db8c1aab32cacbcc2ded82727af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120522"
---
# <a name="mcm_getcalendarcount-message"></a><span data-ttu-id="31143-105">\_Messaggio GETCALENDARCOUNT MCM</span><span class="sxs-lookup"><span data-stu-id="31143-105">MCM\_GETCALENDARCOUNT message</span></span>

<span data-ttu-id="31143-106">Ottiene il numero di calendari attualmente visualizzati nel controllo Calendar.</span><span class="sxs-lookup"><span data-stu-id="31143-106">Gets the number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="31143-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) .</span><span class="sxs-lookup"><span data-stu-id="31143-107">You can send this message explicitly or by using the [**MonthCal\_GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="31143-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="31143-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31143-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31143-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31143-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="31143-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="31143-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31143-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31143-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="31143-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31143-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31143-113">Return value</span></span>

<span data-ttu-id="31143-114">Numero di calendari attualmente visualizzati nel controllo calendario.</span><span class="sxs-lookup"><span data-stu-id="31143-114">Number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="31143-115">Il numero massimo di calendari consentiti è 12.</span><span class="sxs-lookup"><span data-stu-id="31143-115">The maximum number of allowed calendars is 12.</span></span>

## <a name="requirements"></a><span data-ttu-id="31143-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31143-116">Requirements</span></span>



| <span data-ttu-id="31143-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="31143-117">Requirement</span></span> | <span data-ttu-id="31143-118">Valore</span><span class="sxs-lookup"><span data-stu-id="31143-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31143-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31143-119">Minimum supported client</span></span><br/> | <span data-ttu-id="31143-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="31143-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31143-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31143-121">Minimum supported server</span></span><br/> | <span data-ttu-id="31143-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="31143-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="31143-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31143-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="31143-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="31143-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





