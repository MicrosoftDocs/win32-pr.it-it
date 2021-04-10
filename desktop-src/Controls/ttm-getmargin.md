---
title: Messaggio TTM_GETMARGIN (COMmctrl. h)
description: Recupera i margini superiore, sinistro, inferiore e destro impostati per una finestra della descrizione comando. Un margine è la distanza, in pixel, tra il bordo della finestra della descrizione comando e il testo contenuto nella finestra della descrizione comando.
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- Controlli di Windows Message TTM_GETMARGIN
topic_type:
- apiref
api_name:
- TTM_GETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3e795d8eac14522f0994a342c7f781b7112ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964241"
---
# <a name="ttm_getmargin-message"></a><span data-ttu-id="bdb31-105">\_Messaggio GETMARGIN TTM</span><span class="sxs-lookup"><span data-stu-id="bdb31-105">TTM\_GETMARGIN message</span></span>

<span data-ttu-id="bdb31-106">Recupera i margini superiore, sinistro, inferiore e destro impostati per una finestra della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="bdb31-106">Retrieves the top, left, bottom, and right margins set for a tooltip window.</span></span> <span data-ttu-id="bdb31-107">Un margine è la distanza, in pixel, tra il bordo della finestra della descrizione comando e il testo contenuto nella finestra della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="bdb31-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdb31-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdb31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdb31-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdb31-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bdb31-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bdb31-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bdb31-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdb31-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdb31-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceverà le informazioni sul margine.</span><span class="sxs-lookup"><span data-stu-id="bdb31-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the margin information.</span></span> <span data-ttu-id="bdb31-113">I membri della struttura **Rect** non definiscono un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="bdb31-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="bdb31-114">Ai fini di questo messaggio, i membri della struttura vengono interpretati nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="bdb31-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="bdb31-115">Valore</span><span class="sxs-lookup"><span data-stu-id="bdb31-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="bdb31-116">Significato</span><span class="sxs-lookup"><span data-stu-id="bdb31-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="bdb31-117"><dt>**In alto**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb31-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="bdb31-118">Distanza tra il bordo superiore e il testo della descrizione comando, in pixel.</span><span class="sxs-lookup"><span data-stu-id="bdb31-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="bdb31-119"><dt>**sinistra**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb31-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="bdb31-120">Distanza tra il bordo sinistro e il lato sinistro del testo della descrizione comando, in pixel.</span><span class="sxs-lookup"><span data-stu-id="bdb31-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="bdb31-121"><dt>**parte inferiore**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb31-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="bdb31-122">Distanza tra il bordo inferiore e il testo della descrizione comando, in pixel.</span><span class="sxs-lookup"><span data-stu-id="bdb31-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="bdb31-123"><dt>**Ok**</dt></span><span class="sxs-lookup"><span data-stu-id="bdb31-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="bdb31-124">Distanza tra il bordo destro e l'estremità destra del testo della descrizione comando, in pixel.</span><span class="sxs-lookup"><span data-stu-id="bdb31-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdb31-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bdb31-125">Return value</span></span>

<span data-ttu-id="bdb31-126">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="bdb31-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdb31-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="bdb31-127">Remarks</span></span>

<span data-ttu-id="bdb31-128">Per impostazione predefinita, tutti e quattro i margini sono pari a zero quando si crea il controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="bdb31-128">All four margins default to zero when you create the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdb31-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdb31-129">Requirements</span></span>



| <span data-ttu-id="bdb31-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdb31-130">Requirement</span></span> | <span data-ttu-id="bdb31-131">Valore</span><span class="sxs-lookup"><span data-stu-id="bdb31-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb31-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdb31-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bdb31-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bdb31-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bdb31-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdb31-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bdb31-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bdb31-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bdb31-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bdb31-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdb31-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdb31-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdb31-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdb31-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb31-139">**TTM \_**</span><span class="sxs-lookup"><span data-stu-id="bdb31-139">**TTM\_SETMARGIN**</span></span>](ttm-setmargin.md)
</dt> </dl>

 

