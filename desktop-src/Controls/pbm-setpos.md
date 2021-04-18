---
title: Messaggio PBM_SETPOS (COMmctrl. h)
description: Imposta la posizione corrente di un indicatore di stato e ridisegnato la barra in modo da riflettere la nuova posizione.
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- Controlli di Windows Message PBM_SETPOS
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302056"
---
# <a name="pbm_setpos-message"></a><span data-ttu-id="ed5a4-104">\_Messaggio SETPOS PBM</span><span class="sxs-lookup"><span data-stu-id="ed5a4-104">PBM\_SETPOS message</span></span>

<span data-ttu-id="ed5a4-105">Imposta la posizione corrente di un indicatore di stato e ridisegnato la barra in modo da riflettere la nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="ed5a4-105">Sets the current position for a progress bar and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed5a4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed5a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed5a4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed5a4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed5a4-108">Intero con segno che diventa la nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="ed5a4-108">Signed integer that becomes the new position.</span></span>

</dd> <dt>

<span data-ttu-id="ed5a4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed5a4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ed5a4-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ed5a4-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed5a4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed5a4-111">Return value</span></span>

<span data-ttu-id="ed5a4-112">Restituisce la posizione precedente.</span><span class="sxs-lookup"><span data-stu-id="ed5a4-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed5a4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed5a4-113">Remarks</span></span>

<span data-ttu-id="ed5a4-114">Se *wParam* non è compreso nell'intervallo del controllo, la posizione viene impostata sul limite più vicino.</span><span class="sxs-lookup"><span data-stu-id="ed5a4-114">If *wParam* is outside the range of the control, the position is set to the closest boundary.</span></span>

<span data-ttu-id="ed5a4-115">Non inviare questo messaggio a un controllo con stile di [**\_ selezione PBS**](progress-bar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="ed5a4-115">Do not send this message to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed5a4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed5a4-116">Requirements</span></span>



| <span data-ttu-id="ed5a4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed5a4-117">Requirement</span></span> | <span data-ttu-id="ed5a4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ed5a4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed5a4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed5a4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ed5a4-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed5a4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed5a4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed5a4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ed5a4-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ed5a4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed5a4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed5a4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed5a4-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed5a4-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





