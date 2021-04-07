---
title: Messaggio MCM_SETMAXSELCOUNT (COMmctrl. h)
description: Imposta il numero massimo di giorni che possono essere selezionati in un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal SetMaxSelCount.
ms.assetid: 190453ab-e53b-4db7-82c1-f9d50188ad39
keywords:
- Controlli di Windows Message MCM_SETMAXSELCOUNT
topic_type:
- apiref
api_name:
- MCM_SETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c67bcb7191bb20b9688c2fe1ffc2b458ecb7b8a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874498"
---
# <a name="mcm_setmaxselcount-message"></a><span data-ttu-id="d5b41-105">\_Messaggio SETMAXSELCOUNT MCM</span><span class="sxs-lookup"><span data-stu-id="d5b41-105">MCM\_SETMAXSELCOUNT message</span></span>

<span data-ttu-id="d5b41-106">Imposta il numero massimo di giorni che possono essere selezionati in un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="d5b41-106">Sets the maximum number of days that can be selected in a month calendar control.</span></span> <span data-ttu-id="d5b41-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) .</span><span class="sxs-lookup"><span data-stu-id="d5b41-107">You can send this message explicitly or by using the [**MonthCal\_SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5b41-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5b41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5b41-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5b41-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5b41-110">Valore di tipo **int** che verrà impostato per rappresentare il numero massimo di giorni che è possibile selezionare.</span><span class="sxs-lookup"><span data-stu-id="d5b41-110">Value of type **int** that will be set to represent the maximum number of days that can be selected.</span></span>

</dd> <dt>

<span data-ttu-id="d5b41-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5b41-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d5b41-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d5b41-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5b41-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5b41-113">Return value</span></span>

<span data-ttu-id="d5b41-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d5b41-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="d5b41-115">Questo messaggio avrà esito negativo se applicato a un controllo calendario mensile che non usa lo stile [**\_ MultiSelect MCS**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d5b41-115">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5b41-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5b41-116">Requirements</span></span>



| <span data-ttu-id="d5b41-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5b41-117">Requirement</span></span> | <span data-ttu-id="d5b41-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d5b41-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b41-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5b41-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d5b41-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5b41-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5b41-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5b41-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d5b41-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d5b41-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5b41-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5b41-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5b41-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5b41-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





