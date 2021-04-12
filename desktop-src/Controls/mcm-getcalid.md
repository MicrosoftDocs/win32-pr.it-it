---
title: Messaggio MCM_GETCALID (COMmctrl. h)
description: Ottiene l'ID calendario per il controllo calendario specificato. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal GETcalid.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- Controlli di Windows Message MCM_GETCALID
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb4a780d5107a7761d7dcac9b27a7cb01f3de744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120010"
---
# <a name="mcm_getcalid-message"></a><span data-ttu-id="9a82a-105">\_Messaggio MCM GETcalid</span><span class="sxs-lookup"><span data-stu-id="9a82a-105">MCM\_GETCALID message</span></span>

<span data-ttu-id="9a82a-106">Ottiene l'ID calendario per il controllo calendario specificato.</span><span class="sxs-lookup"><span data-stu-id="9a82a-106">Gets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="9a82a-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**MonthCal \_ getcalid**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) .</span><span class="sxs-lookup"><span data-stu-id="9a82a-107">You can send this message explicitly or by using the [**MonthCal\_GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a82a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a82a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a82a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a82a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a82a-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9a82a-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9a82a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a82a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a82a-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9a82a-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a82a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a82a-113">Return value</span></span>

<span data-ttu-id="9a82a-114">ID del calendario corrente.</span><span class="sxs-lookup"><span data-stu-id="9a82a-114">ID of the current calendar.</span></span> <span data-ttu-id="9a82a-115">Una delle costanti degli [identificatori del calendario](/windows/desktop/Intl/calendar-identifiers) .</span><span class="sxs-lookup"><span data-stu-id="9a82a-115">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a82a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a82a-116">Requirements</span></span>



| <span data-ttu-id="9a82a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a82a-117">Requirement</span></span> | <span data-ttu-id="9a82a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9a82a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a82a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a82a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9a82a-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a82a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a82a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a82a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9a82a-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9a82a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a82a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a82a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a82a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a82a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

