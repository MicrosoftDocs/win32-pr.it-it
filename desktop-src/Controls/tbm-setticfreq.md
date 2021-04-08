---
title: Messaggio TBM_SETTICFREQ (COMmctrl. h)
description: Imposta la frequenza di intervallo per i segni di graduazione in un TrackBar.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- Controlli di Windows Message TBM_SETTICFREQ
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048114"
---
# <a name="tbm_setticfreq-message"></a><span data-ttu-id="32fba-104">\_Messaggio SETTICFREQ TBM</span><span class="sxs-lookup"><span data-stu-id="32fba-104">TBM\_SETTICFREQ message</span></span>

<span data-ttu-id="32fba-105">Imposta la frequenza di intervallo per i segni di graduazione in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="32fba-105">Sets the interval frequency for tick marks in a trackbar.</span></span> <span data-ttu-id="32fba-106">Se, ad esempio, la frequenza è impostata su due, viene visualizzato un segno di graduazione per ogni altro incremento nell'intervallo del TrackBar.</span><span class="sxs-lookup"><span data-stu-id="32fba-106">For example, if the frequency is set to two, a tick mark is displayed for every other increment in the trackbar's range.</span></span> <span data-ttu-id="32fba-107">L'impostazione predefinita per la frequenza è uno; ovvero ogni incremento nell'intervallo è associato a un segno di graduazione.</span><span class="sxs-lookup"><span data-stu-id="32fba-107">The default setting for the frequency is one; that is, every increment in the range is associated with a tick mark.</span></span>

## <a name="parameters"></a><span data-ttu-id="32fba-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="32fba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32fba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32fba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32fba-110">Frequenza dei segni di graduazione.</span><span class="sxs-lookup"><span data-stu-id="32fba-110">Frequency of the tick marks.</span></span>

</dd> <dt>

<span data-ttu-id="32fba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32fba-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="32fba-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="32fba-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32fba-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32fba-113">Return value</span></span>

<span data-ttu-id="32fba-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="32fba-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32fba-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="32fba-115">Remarks</span></span>

<span data-ttu-id="32fba-116">Per usare questo messaggio, il TrackBar deve avere lo stile per i segni di [**\_ scandili TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="32fba-116">The trackbar must have the [**TBS\_AUTOTICKS**](trackbar-control-styles.md) style to use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="32fba-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32fba-117">Requirements</span></span>



| <span data-ttu-id="32fba-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="32fba-118">Requirement</span></span> | <span data-ttu-id="32fba-119">Valore</span><span class="sxs-lookup"><span data-stu-id="32fba-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32fba-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32fba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="32fba-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32fba-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32fba-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32fba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="32fba-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32fba-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32fba-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32fba-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="32fba-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="32fba-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





