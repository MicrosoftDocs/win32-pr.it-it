---
title: Messaggio EM_SETRECTNP (winuser. h)
description: Imposta il rettangolo di formattazione di un controllo di modifica su più righe.
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- Controlli di Windows Message EM_SETRECTNP
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e017bd4737c843c2452382918d71ef63345917cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964753"
---
# <a name="em_setrectnp-message"></a><span data-ttu-id="c1327-104">\_Messaggio SETRECTNP em</span><span class="sxs-lookup"><span data-stu-id="c1327-104">EM\_SETRECTNP message</span></span>

<span data-ttu-id="c1327-105">Imposta il [rettangolo di formattazione](about-edit-controls.md) di un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="c1327-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="c1327-106">Il **messaggio \_ SETRECTNP em** è identico al [**messaggio \_ serect em**](em-setrect.md) , ad eccezione del fatto che  **em \_ SETRECTNP** non ridisegnato la finestra di controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="c1327-106">The **EM\_SETRECTNP** message is identical to the [**EM\_SETRECT**](em-setrect.md) message, except that **EM\_SETRECTNP** does *not* redraw the edit control window.</span></span>

<span data-ttu-id="c1327-107">Il rettangolo di formattazione è il rettangolo di limitazione in cui il controllo disegna il testo.</span><span class="sxs-lookup"><span data-stu-id="c1327-107">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="c1327-108">Il rettangolo di limitazione è indipendente dalle dimensioni della finestra di controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="c1327-108">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="c1327-109">Questo messaggio viene elaborato solo dai controlli di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="c1327-109">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="c1327-110">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c1327-110">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1327-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1327-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1327-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1327-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1327-113">**Rich Edit 3,0 e versioni successive:** Indica se il nuovo rettangolo contiene coordinate assolute o relative.</span><span class="sxs-lookup"><span data-stu-id="c1327-113">**Rich Edit 3.0 and later:** Indicates whether the new rectangle contains absolute or relative coordinates.</span></span> <span data-ttu-id="c1327-114">Un valore pari a zero indica le coordinate assolute.</span><span class="sxs-lookup"><span data-stu-id="c1327-114">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="c1327-115">Il valore 1 indica gli offset relativi al rettangolo di formattazione corrente.</span><span class="sxs-lookup"><span data-stu-id="c1327-115">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="c1327-116">Gli offset possono essere positivi o negativi.</span><span class="sxs-lookup"><span data-stu-id="c1327-116">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="c1327-117">**Controlli di modifica:** Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c1327-117">**Edit controls:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1327-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1327-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1327-119">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica le nuove dimensioni del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="c1327-119">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="c1327-120">Se questo parametro è **null**, il rettangolo di formattazione viene impostato sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c1327-120">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1327-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1327-121">Return value</span></span>

<span data-ttu-id="c1327-122">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="c1327-122">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1327-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1327-123">Remarks</span></span>

<span data-ttu-id="c1327-124">**Modifica avanzata:** Supportato in Microsoft Rich Edit 3,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c1327-124">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="c1327-125">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c1327-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1327-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1327-126">Requirements</span></span>



| <span data-ttu-id="c1327-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1327-127">Requirement</span></span> | <span data-ttu-id="c1327-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c1327-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1327-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1327-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c1327-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1327-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c1327-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1327-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c1327-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c1327-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c1327-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1327-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1327-134"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1327-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1327-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1327-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1327-136">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c1327-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c1327-137">**serect EM \_**</span><span class="sxs-lookup"><span data-stu-id="c1327-137">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

<span data-ttu-id="c1327-138">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="c1327-138">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="c1327-139">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c1327-139">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

