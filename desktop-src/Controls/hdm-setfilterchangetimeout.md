---
title: Messaggio HDM_SETFILTERCHANGETIMEOUT (COMmctrl. h)
description: Imposta l'intervallo di timeout tra l'ora in cui viene apportata una modifica negli attributi di filtro e la pubblicazione di una \_ notifica FILTERCHANGE HDN. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetFilterChangeTimeout dell'intestazione.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- Controlli di Windows Message HDM_SETFILTERCHANGETIMEOUT
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9876634d12cd15001c296151694cb755ed1b34e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048613"
---
# <a name="hdm_setfilterchangetimeout-message"></a><span data-ttu-id="a8b73-105">\_Messaggio HDM SETFILTERCHANGETIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a8b73-105">HDM\_SETFILTERCHANGETIMEOUT message</span></span>

<span data-ttu-id="a8b73-106">Imposta l'intervallo di timeout tra l'ora in cui viene apportata una modifica negli attributi di filtro e la pubblicazione di una notifica [ \_ FILTERCHANGE HDN](hdn-filterchange.md) .</span><span class="sxs-lookup"><span data-stu-id="a8b73-106">Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification.</span></span> <span data-ttu-id="a8b73-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetFilterChangeTimeout dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) .</span><span class="sxs-lookup"><span data-stu-id="a8b73-107">You can send this message explicitly or use the [**Header\_SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8b73-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8b73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b73-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8b73-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a8b73-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a8b73-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a8b73-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8b73-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8b73-112">Valore di timeout in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="a8b73-112">The timeout value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b73-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8b73-113">Return value</span></span>

<span data-ttu-id="a8b73-114">Restituisce l'indice del controllo filtro da modificare.</span><span class="sxs-lookup"><span data-stu-id="a8b73-114">Returns the index of the filter control being modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b73-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8b73-115">Requirements</span></span>



| <span data-ttu-id="a8b73-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b73-116">Requirement</span></span> | <span data-ttu-id="a8b73-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a8b73-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b73-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8b73-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b73-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8b73-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8b73-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8b73-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b73-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8b73-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8b73-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8b73-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8b73-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b73-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b73-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8b73-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b73-125">\_FILTERCHANGE HDN</span><span class="sxs-lookup"><span data-stu-id="a8b73-125">HDN\_FILTERCHANGE</span></span>](hdn-filterchange.md)
</dt> </dl>

 

 





