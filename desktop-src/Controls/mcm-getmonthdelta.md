---
title: Messaggio MCM_GETMONTHDELTA (COMmctrl. h)
description: Recupera la velocità di scorrimento per un controllo di calendario mensile. La velocità di scorrimento indica il numero di mesi durante i quali il controllo sposta la visualizzazione quando l'utente fa clic su un pulsante di scorrimento. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetMonthDelta.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- Controlli di Windows Message MCM_GETMONTHDELTA
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01eaa40b930e6317cc2be6b674f0cea58115ae40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121758"
---
# <a name="mcm_getmonthdelta-message"></a><span data-ttu-id="d1772-106">\_Messaggio GETMONTHDELTA MCM</span><span class="sxs-lookup"><span data-stu-id="d1772-106">MCM\_GETMONTHDELTA message</span></span>

<span data-ttu-id="d1772-107">Recupera la velocità di scorrimento per un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="d1772-107">Retrieves the scroll rate for a month calendar control.</span></span> <span data-ttu-id="d1772-108">La velocità di scorrimento indica il numero di mesi durante i quali il controllo sposta la visualizzazione quando l'utente fa clic su un pulsante di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="d1772-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="d1772-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) .</span><span class="sxs-lookup"><span data-stu-id="d1772-109">You can send this message explicitly or by using the [**MonthCal\_GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1772-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1772-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1772-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1772-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d1772-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d1772-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d1772-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1772-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d1772-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d1772-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1772-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1772-115">Return value</span></span>

<span data-ttu-id="d1772-116">Se il Delta del mese è stato impostato in precedenza tramite il messaggio [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) , restituisce un valore int che rappresenta la frequenza di scorrimento corrente del calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="d1772-116">If the month delta was previously set using the [**MCM\_SETMONTHDELTA**](mcm-setmonthdelta.md) message, returns an INT value that represents the month calendar's current scroll rate.</span></span> <span data-ttu-id="d1772-117">Se il Delta del mese non è stato impostato in precedenza utilizzando il messaggio **MCM \_ SETMONTHDELTA** o il Delta del mese è stato reimpostato sull'impostazione predefinita, restituisce un valore int che rappresenta il numero corrente di mesi visibili.</span><span class="sxs-lookup"><span data-stu-id="d1772-117">If the month delta was not previously set using the **MCM\_SETMONTHDELTA** message, or the month delta was reset to the default, returns an INT value that represents the current number of months visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1772-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1772-118">Requirements</span></span>



| <span data-ttu-id="d1772-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1772-119">Requirement</span></span> | <span data-ttu-id="d1772-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d1772-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1772-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1772-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d1772-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1772-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1772-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1772-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d1772-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d1772-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1772-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1772-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1772-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1772-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





