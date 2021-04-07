---
title: Messaggio TBM_GETNUMTICS (COMmctrl. h)
description: Recupera il numero di segni di graduazione in un TrackBar.
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- Controlli di Windows Message TBM_GETNUMTICS
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963933"
---
# <a name="tbm_getnumtics-message"></a><span data-ttu-id="6589c-104">\_Messaggio GETNUMTICS TBM</span><span class="sxs-lookup"><span data-stu-id="6589c-104">TBM\_GETNUMTICS message</span></span>

<span data-ttu-id="6589c-105">Recupera il numero di segni di graduazione in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6589c-105">Retrieves the number of tick marks in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6589c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6589c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6589c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6589c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6589c-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6589c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6589c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6589c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6589c-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6589c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6589c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6589c-111">Return value</span></span>

<span data-ttu-id="6589c-112">Se non è impostato alcun [flag](trackbar-control-styles.md) di selezione, restituisce 2 per i cicli di inizio e fine.</span><span class="sxs-lookup"><span data-stu-id="6589c-112">If no [tick flag](trackbar-control-styles.md) is set, it returns 2 for the beginning and ending ticks.</span></span> <span data-ttu-id="6589c-113">Se è impostato TBS nosegni, viene restituito zero. [**\_**](trackbar-control-styles.md)</span><span class="sxs-lookup"><span data-stu-id="6589c-113">If [**TBS\_NOTICKS**](trackbar-control-styles.md) is set, it returns zero.</span></span> <span data-ttu-id="6589c-114">In caso contrario, prende la differenza tra il valore minimo e massimo dell'intervallo, divide in base alla frequenza di segno e aggiunge 2.</span><span class="sxs-lookup"><span data-stu-id="6589c-114">Otherwise, it takes the difference between the range minimum and maximum, divides by the tick frequency, and adds 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="6589c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6589c-115">Remarks</span></span>

<span data-ttu-id="6589c-116">Il messaggio **TBM \_ GETNUMTICS** conta tutti i segni di graduazione, inclusi il primo e l'ultimo segno di graduazione creato dal TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6589c-116">The **TBM\_GETNUMTICS** message counts all of the tick marks, including the first and last tick marks created by the trackbar.</span></span>

## <a name="requirements"></a><span data-ttu-id="6589c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6589c-117">Requirements</span></span>



| <span data-ttu-id="6589c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6589c-118">Requirement</span></span> | <span data-ttu-id="6589c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6589c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6589c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6589c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6589c-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6589c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6589c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6589c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6589c-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6589c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6589c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6589c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6589c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6589c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





