---
title: Messaggio EM_GETRECT (winuser. h)
description: Ottiene il rettangolo di formattazione di un controllo di modifica.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- Controlli di Windows Message EM_GETRECT
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8192fd4c3aa7fbe953a36217f6b1408f055d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873934"
---
# <a name="em_getrect-message"></a><span data-ttu-id="34746-104">\_Messaggio GETRECT em</span><span class="sxs-lookup"><span data-stu-id="34746-104">EM\_GETRECT message</span></span>

<span data-ttu-id="34746-105">Ottiene il [rettangolo di formattazione](about-edit-controls.md) di un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="34746-105">Gets the [formatting rectangle](about-edit-controls.md) of an edit control.</span></span> <span data-ttu-id="34746-106">Il rettangolo di formattazione è il rettangolo di limitazione in cui il controllo disegna il testo.</span><span class="sxs-lookup"><span data-stu-id="34746-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="34746-107">Il rettangolo di limitazione è indipendente dalle dimensioni della finestra di modifica del controllo.</span><span class="sxs-lookup"><span data-stu-id="34746-107">The limiting rectangle is independent of the size of the edit-control window.</span></span> <span data-ttu-id="34746-108">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="34746-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="34746-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="34746-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34746-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34746-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34746-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="34746-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="34746-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34746-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34746-113">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve il rettangolo di formattazione.</span><span class="sxs-lookup"><span data-stu-id="34746-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the formatting rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34746-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34746-114">Return value</span></span>

<span data-ttu-id="34746-115">Il valore restituito non è significativo.</span><span class="sxs-lookup"><span data-stu-id="34746-115">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="34746-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="34746-116">Remarks</span></span>

<span data-ttu-id="34746-117">È possibile modificare il rettangolo di formattazione di un controllo di modifica su più righe usando i messaggi [**em \_ serect**](em-setrect.md) e [**em \_ SETRECTNP**](em-setrectnp.md) .</span><span class="sxs-lookup"><span data-stu-id="34746-117">You can modify the formatting rectangle of a multiline edit control by using the [**EM\_SETRECT**](em-setrect.md) and [**EM\_SETRECTNP**](em-setrectnp.md) messages.</span></span>

<span data-ttu-id="34746-118">In determinate condizioni, **em \_ GetRect** potrebbe non restituire i valori esatti impostati da [**em \_ serect**](em-setrect.md) o [**em \_ SETRECTNP**](em-setrectnp.md) , che saranno approssimativamente corretti, ma possono essere disattivati con pochi pixel.</span><span class="sxs-lookup"><span data-stu-id="34746-118">Under certain conditions, **EM\_GETRECT** might not return the exact values that [**EM\_SETRECT**](em-setrect.md) or [**EM\_SETRECTNP**](em-setrectnp.md) set it will be approximately correct, but it can be off by a few pixels.</span></span>

<span data-ttu-id="34746-119">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="34746-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="34746-120">Il rettangolo di formattazione non include la barra di selezione, ovvero un'area non contrassegnata a sinistra di ogni paragrafo.</span><span class="sxs-lookup"><span data-stu-id="34746-120">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="34746-121">Quando si fa clic sulla barra di selezione, la riga viene selezionata.</span><span class="sxs-lookup"><span data-stu-id="34746-121">When clicked, the selection bar selects the line.</span></span> <span data-ttu-id="34746-122">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="34746-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34746-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34746-123">Requirements</span></span>



| <span data-ttu-id="34746-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="34746-124">Requirement</span></span> | <span data-ttu-id="34746-125">Valore</span><span class="sxs-lookup"><span data-stu-id="34746-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34746-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34746-126">Minimum supported client</span></span><br/> | <span data-ttu-id="34746-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34746-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="34746-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34746-128">Minimum supported server</span></span><br/> | <span data-ttu-id="34746-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="34746-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="34746-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34746-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="34746-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34746-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34746-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34746-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="34746-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="34746-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="34746-134">**serect EM \_**</span><span class="sxs-lookup"><span data-stu-id="34746-134">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

[<span data-ttu-id="34746-135">**\_SETRECTNP em**</span><span class="sxs-lookup"><span data-stu-id="34746-135">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="34746-136">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="34746-136">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="34746-137">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34746-137">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

