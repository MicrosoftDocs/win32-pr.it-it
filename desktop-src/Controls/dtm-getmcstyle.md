---
title: Messaggio DTM_GETMCSTYLE (COMmctrl. h)
description: Ottiene lo stile di un controllo di selezione data e ora (DTP). Inviare questo messaggio in modo esplicito o utilizzando la \_ macro DateTime GetMonthCalStyle.
ms.assetid: 8983898f-e23a-4247-838c-56364f695429
keywords:
- Controlli di Windows Message DTM_GETMCSTYLE
topic_type:
- apiref
api_name:
- DTM_GETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cae82d271d0e9aece54046527dfa3bedcef657f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964584"
---
# <a name="dtm_getmcstyle-message"></a><span data-ttu-id="6886a-105">\_Messaggio GETMCSTYLE DTM</span><span class="sxs-lookup"><span data-stu-id="6886a-105">DTM\_GETMCSTYLE message</span></span>

<span data-ttu-id="6886a-106">Ottiene lo stile di un controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="6886a-106">Gets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="6886a-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**DateTime \_ GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) .</span><span class="sxs-lookup"><span data-stu-id="6886a-107">Send this message explicitly or by using the [**DateTime\_GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6886a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6886a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6886a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6886a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6886a-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6886a-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6886a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6886a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6886a-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6886a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6886a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6886a-113">Return value</span></span>

<span data-ttu-id="6886a-114">Restituisce il valore di stile del controllo.</span><span class="sxs-lookup"><span data-stu-id="6886a-114">Returns the style value of the control.</span></span> <span data-ttu-id="6886a-115">Per altre informazioni, vedere [stili del controllo calendario mensile](month-calendar-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="6886a-115">For more information see [Month Calendar Control Styles](month-calendar-control-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6886a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6886a-116">Requirements</span></span>



| <span data-ttu-id="6886a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6886a-117">Requirement</span></span> | <span data-ttu-id="6886a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6886a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6886a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6886a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6886a-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6886a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6886a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6886a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6886a-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6886a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6886a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6886a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6886a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6886a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





