---
title: Messaggio LVM_APPROXIMATEVIEWRECT (COMmctrl. h)
description: Calcola la larghezza e l'altezza approssimative richieste per visualizzare un determinato numero di elementi. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ApproximateViewRect di ListView.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- Controlli di Windows Message LVM_APPROXIMATEVIEWRECT
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be929d34acad46b75a53a9e0cc8825ec9801e998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963771"
---
# <a name="lvm_approximateviewrect-message"></a><span data-ttu-id="693b3-105">\_Messaggio APPROXIMATEVIEWRECT LVM</span><span class="sxs-lookup"><span data-stu-id="693b3-105">LVM\_APPROXIMATEVIEWRECT message</span></span>

<span data-ttu-id="693b3-106">Calcola la larghezza e l'altezza approssimative richieste per visualizzare un determinato numero di elementi.</span><span class="sxs-lookup"><span data-stu-id="693b3-106">Calculates the approximate width and height required to display a given number of items.</span></span> <span data-ttu-id="693b3-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ApproximateViewRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) .</span><span class="sxs-lookup"><span data-stu-id="693b3-107">You can send this message explicitly or use the [**ListView\_ApproximateViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="693b3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="693b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="693b3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="693b3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="693b3-110">Numero di elementi da visualizzare nel controllo.</span><span class="sxs-lookup"><span data-stu-id="693b3-110">The number of items to be displayed in the control.</span></span> <span data-ttu-id="693b3-111">Se questo parametro è impostato su-1, il messaggio utilizza il numero totale di elementi nel controllo.</span><span class="sxs-lookup"><span data-stu-id="693b3-111">If this parameter is set to -1, the message uses the total number of items in the control.</span></span>

</dd> <dt>

<span data-ttu-id="693b3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="693b3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="693b3-113">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è la dimensione x proposta del controllo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="693b3-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the proposed x-dimension of the control, in pixels.</span></span> <span data-ttu-id="693b3-114">Questo parametro può essere impostato su-1 per consentire al messaggio di usare il valore della larghezza corrente.</span><span class="sxs-lookup"><span data-stu-id="693b3-114">This parameter can be set to -1 to allow the message to use the current width value.</span></span>

<span data-ttu-id="693b3-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è la dimensione y proposta del controllo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="693b3-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the proposed y-dimension of the control, in pixels.</span></span> <span data-ttu-id="693b3-116">Questo parametro può essere impostato su-1 per consentire al messaggio di usare il valore di altezza corrente.</span><span class="sxs-lookup"><span data-stu-id="693b3-116">This parameter can be set to -1 to allow the message to use the current height value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="693b3-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="693b3-117">Return value</span></span>

<span data-ttu-id="693b3-118">Restituisce un valore **DWORD** che include la larghezza approssimativa (in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) e l'altezza (in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) necessarie per visualizzare gli elementi, in pixel.</span><span class="sxs-lookup"><span data-stu-id="693b3-118">Returns a **DWORD** value that holds the approximate width (in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) and height (in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) needed to display the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="693b3-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="693b3-119">Remarks</span></span>

<span data-ttu-id="693b3-120">L'impostazione delle dimensioni del controllo di visualizzazione elenco in base alle dimensioni fornite da questo messaggio può ottimizzare il riprogetto e ridurre lo sfarfallio.</span><span class="sxs-lookup"><span data-stu-id="693b3-120">Setting the size of the list-view control based on the dimensions provided by this message can optimize redraw and reduce flicker.</span></span>

## <a name="requirements"></a><span data-ttu-id="693b3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="693b3-121">Requirements</span></span>



| <span data-ttu-id="693b3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="693b3-122">Requirement</span></span> | <span data-ttu-id="693b3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="693b3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="693b3-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="693b3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="693b3-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="693b3-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="693b3-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="693b3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="693b3-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="693b3-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="693b3-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="693b3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="693b3-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="693b3-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

