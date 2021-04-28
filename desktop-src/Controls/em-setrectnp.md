---
title: EM_SETRECTNP messaggio (Winuser.h)
description: 'EM_SETRECTNP: imposta il rettangolo di formattazione di un controllo di modifica su più righe.'
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP di windows del messaggio
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
ms.openlocfilehash: e9a8c85d4f7abd58ed3adb33ede66254c190a7bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085989"
---
# <a name="em_setrectnp-message"></a><span data-ttu-id="4160c-104">Messaggio \_ EM SETRECTNP</span><span class="sxs-lookup"><span data-stu-id="4160c-104">EM\_SETRECTNP message</span></span>

<span data-ttu-id="4160c-105">Imposta il rettangolo [di formattazione](about-edit-controls.md) di un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="4160c-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="4160c-106">Il **messaggio EM \_ SETRECTNP** è identico al messaggio [**EM \_ SETRECT,**](em-setrect.md)  ad eccezione del fatto che **EM \_ SETRECTNP** non ridisegna la finestra del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="4160c-106">The **EM\_SETRECTNP** message is identical to the [**EM\_SETRECT**](em-setrect.md) message, except that **EM\_SETRECTNP** does *not* redraw the edit control window.</span></span>

<span data-ttu-id="4160c-107">Il rettangolo di formattazione è il rettangolo di limitazione in cui il controllo disegna il testo.</span><span class="sxs-lookup"><span data-stu-id="4160c-107">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="4160c-108">Il rettangolo di limitazione è indipendente dalle dimensioni della finestra del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="4160c-108">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="4160c-109">Questo messaggio viene elaborato solo da controlli di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="4160c-109">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="4160c-110">È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4160c-110">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4160c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="4160c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4160c-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4160c-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4160c-113">**Rich Edit 3.0 e versioni successive:** Indica se il nuovo rettangolo contiene coordinate assolute o relative.</span><span class="sxs-lookup"><span data-stu-id="4160c-113">**Rich Edit 3.0 and later:** Indicates whether the new rectangle contains absolute or relative coordinates.</span></span> <span data-ttu-id="4160c-114">Il valore zero indica coordinate assolute.</span><span class="sxs-lookup"><span data-stu-id="4160c-114">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="4160c-115">Il valore 1 indica gli offset rispetto al rettangolo di formattazione corrente.</span><span class="sxs-lookup"><span data-stu-id="4160c-115">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="4160c-116">Gli offset possono essere positivi o negativi.</span><span class="sxs-lookup"><span data-stu-id="4160c-116">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="4160c-117">**Controlli di modifica:** Questo parametro non viene usato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4160c-117">**Edit controls:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4160c-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4160c-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4160c-119">Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che specifica le nuove dimensioni del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="4160c-119">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="4160c-120">Se questo parametro è **NULL,** il rettangolo di formattazione viene impostato su valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="4160c-120">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4160c-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4160c-121">Return value</span></span>

<span data-ttu-id="4160c-122">Questo messaggio non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4160c-122">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4160c-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="4160c-123">Remarks</span></span>

<span data-ttu-id="4160c-124">**Rich Edit:** Supportato in Microsoft Rich Edit 3.0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4160c-124">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="4160c-125">Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)</span><span class="sxs-lookup"><span data-stu-id="4160c-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4160c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4160c-126">Requirements</span></span>



| <span data-ttu-id="4160c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4160c-127">Requirement</span></span> | <span data-ttu-id="4160c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="4160c-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4160c-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4160c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4160c-130">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4160c-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4160c-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4160c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4160c-132">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4160c-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4160c-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4160c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4160c-134"><dt>Winuser.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4160c-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4160c-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4160c-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="4160c-136">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4160c-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4160c-137">**EM \_ SETRECT**</span><span class="sxs-lookup"><span data-stu-id="4160c-137">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

<span data-ttu-id="4160c-138">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="4160c-138">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="4160c-139">[**Rect**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4160c-139">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

