---
title: Messaggio EM_GETLIMITTEXT (winuser. h)
description: Ottiene il limite di testo corrente per un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- Controlli di Windows Message EM_GETLIMITTEXT
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53da76f43716fd7934011a96d449ffa37c254cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873389"
---
# <a name="em_getlimittext-message"></a><span data-ttu-id="4ce69-105">\_Messaggio GETLIMITTEXT em</span><span class="sxs-lookup"><span data-stu-id="4ce69-105">EM\_GETLIMITTEXT message</span></span>

<span data-ttu-id="4ce69-106">Ottiene il limite di testo corrente per un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="4ce69-106">Gets the current text limit for an edit control.</span></span> <span data-ttu-id="4ce69-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4ce69-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ce69-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ce69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ce69-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ce69-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ce69-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4ce69-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4ce69-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ce69-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ce69-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4ce69-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ce69-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ce69-113">Return value</span></span>

<span data-ttu-id="4ce69-114">Il valore restituito è il limite di testo.</span><span class="sxs-lookup"><span data-stu-id="4ce69-114">The return value is the text limit.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ce69-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ce69-115">Remarks</span></span>

<span data-ttu-id="4ce69-116">**Modificare i controlli, rich edit 2,0 e versioni successive:** Il limite di testo è la quantità massima di testo, in **TCHAR** s, che il controllo può contenere.</span><span class="sxs-lookup"><span data-stu-id="4ce69-116">**Edit controls, Rich Edit 2.0 and later:** The text limit is the maximum amount of text, in **TCHAR** s, that the control can contain.</span></span> <span data-ttu-id="4ce69-117">Per testo ANSI, indica il numero di byte; per il testo Unicode, indica il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="4ce69-117">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="4ce69-118">Due documenti con lo stesso limite di caratteri produrranno lo stesso limite di testo, anche se uno è ANSI e l'altro è Unicode.</span><span class="sxs-lookup"><span data-stu-id="4ce69-118">Two documents with the same character limit will yield the same text limit, even if one is ANSI and the other is Unicode.</span></span>

<span data-ttu-id="4ce69-119">**Modifica dettagliata 1,0:** Il limite di testo è la quantità massima di testo, in byte, che il controllo Rich Edit può contenere.</span><span class="sxs-lookup"><span data-stu-id="4ce69-119">**Rich Edit 1.0:** The text limit is the maximum amount of text, in bytes, that the rich edit control can contain.</span></span>

<span data-ttu-id="4ce69-120">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4ce69-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="4ce69-121">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="4ce69-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ce69-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ce69-122">Requirements</span></span>



| <span data-ttu-id="4ce69-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ce69-123">Requirement</span></span> | <span data-ttu-id="4ce69-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4ce69-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce69-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ce69-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4ce69-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ce69-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4ce69-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ce69-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4ce69-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4ce69-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4ce69-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ce69-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ce69-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ce69-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ce69-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ce69-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ce69-132">**\_SETLIMITTEXT em**</span><span class="sxs-lookup"><span data-stu-id="4ce69-132">**EM\_SETLIMITTEXT**</span></span>](em-setlimittext.md)
</dt> </dl>

 

 





