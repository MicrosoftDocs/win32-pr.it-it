---
title: Messaggio TCM_HITTEST (COMmctrl. h)
description: Determina la scheda, se presente, che si trova in una posizione dello schermo specificata. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl HitTest.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- Controlli di Windows Message TCM_HITTEST
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302361"
---
# <a name="tcm_hittest-message"></a><span data-ttu-id="d70a2-105">Messaggio di TCM \_ HITTEST</span><span class="sxs-lookup"><span data-stu-id="d70a2-105">TCM\_HITTEST message</span></span>

<span data-ttu-id="d70a2-106">Determina la scheda, se presente, che si trova in una posizione dello schermo specificata.</span><span class="sxs-lookup"><span data-stu-id="d70a2-106">Determines which tab, if any, is at a specified screen position.</span></span> <span data-ttu-id="d70a2-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) .</span><span class="sxs-lookup"><span data-stu-id="d70a2-107">You can send this message explicitly or by using the [**TabCtrl\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d70a2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d70a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d70a2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d70a2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d70a2-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d70a2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d70a2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d70a2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d70a2-112">Puntatore a una struttura [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) che specifica la posizione dello schermo da verificare.</span><span class="sxs-lookup"><span data-stu-id="d70a2-112">Pointer to a [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) structure that specifies the screen position to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d70a2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d70a2-113">Return value</span></span>

<span data-ttu-id="d70a2-114">Restituisce l'indice della scheda oppure-1 se nessuna scheda si trova nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="d70a2-114">Returns the index of the tab, or -1 if no tab is at the specified position.</span></span>

## <a name="requirements"></a><span data-ttu-id="d70a2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d70a2-115">Requirements</span></span>



| <span data-ttu-id="d70a2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d70a2-116">Requirement</span></span> | <span data-ttu-id="d70a2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d70a2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d70a2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d70a2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d70a2-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d70a2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d70a2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d70a2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d70a2-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d70a2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d70a2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d70a2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d70a2-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d70a2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





