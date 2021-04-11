---
title: Messaggio ACM_STOP (COMmctrl. h)
description: Interrompe la riproduzione di un clip AVI in un controllo Animation. È possibile inviare questo messaggio in modo esplicito o usando la macro di animazione \_ stop.
ms.assetid: ba39a579-665e-4d45-8f1f-f190acd76db7
keywords:
- Controlli di Windows Message ACM_STOP
topic_type:
- apiref
api_name:
- ACM_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81cfc92ac2778ae559fcd9fb8db2b0cd7bb866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119243"
---
# <a name="acm_stop-message"></a><span data-ttu-id="77cb8-105">\_Messaggio di arresto ACM</span><span class="sxs-lookup"><span data-stu-id="77cb8-105">ACM\_STOP message</span></span>

<span data-ttu-id="77cb8-106">Interrompe la riproduzione di un clip AVI in un controllo Animation.</span><span class="sxs-lookup"><span data-stu-id="77cb8-106">Stops playing an AVI clip in an animation control.</span></span> <span data-ttu-id="77cb8-107">È possibile inviare questo messaggio in modo esplicito o usando la macro di [**animazione \_ Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) .</span><span class="sxs-lookup"><span data-stu-id="77cb8-107">You can send this message explicitly or by using the [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="77cb8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="77cb8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77cb8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77cb8-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="77cb8-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="77cb8-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="77cb8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77cb8-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="77cb8-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="77cb8-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77cb8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="77cb8-113">Return value</span></span>

<span data-ttu-id="77cb8-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="77cb8-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="77cb8-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77cb8-115">Requirements</span></span>



| <span data-ttu-id="77cb8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="77cb8-116">Requirement</span></span> | <span data-ttu-id="77cb8-117">Valore</span><span class="sxs-lookup"><span data-stu-id="77cb8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77cb8-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77cb8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="77cb8-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77cb8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77cb8-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77cb8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="77cb8-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77cb8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77cb8-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77cb8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="77cb8-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77cb8-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





