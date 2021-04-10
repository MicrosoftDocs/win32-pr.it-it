---
title: Messaggio SB_GETTEXTLENGTH (COMmctrl. h)
description: Recupera la lunghezza, in caratteri, del testo dalla parte specificata di una finestra di stato.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- Controlli di Windows Message SB_GETTEXTLENGTH
topic_type:
- apiref
api_name:
- SB_GETTEXTLENGTH
- SB_GETTEXTLENGTHA
- SB_GETTEXTLENGTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b08dd3b870c3c59e5aafbeb9d53baef3816a726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964640"
---
# <a name="sb_gettextlength-message"></a><span data-ttu-id="59e44-104">\_Messaggio GETTEXTLENGTH SB</span><span class="sxs-lookup"><span data-stu-id="59e44-104">SB\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="59e44-105">Recupera la lunghezza, in caratteri, del testo dalla parte specificata di una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="59e44-105">Retrieves the length, in characters, of the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="59e44-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="59e44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59e44-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59e44-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59e44-108">Indice in base zero della parte da cui recuperare il testo.</span><span class="sxs-lookup"><span data-stu-id="59e44-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="59e44-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59e44-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="59e44-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="59e44-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59e44-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59e44-111">Return value</span></span>

<span data-ttu-id="59e44-112">Restituisce un valore a 32 bit costituito da valori a 2 16 bit.</span><span class="sxs-lookup"><span data-stu-id="59e44-112">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="59e44-113">La parola low specifica la lunghezza, in caratteri, del testo.</span><span class="sxs-lookup"><span data-stu-id="59e44-113">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="59e44-114">La parola alta specifica il tipo di operazione utilizzata per creare il testo.</span><span class="sxs-lookup"><span data-stu-id="59e44-114">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="59e44-115">Il tipo può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="59e44-115">The type can be one of the following values:</span></span>



| <span data-ttu-id="59e44-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="59e44-116">Return code</span></span>                                                                                    | <span data-ttu-id="59e44-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59e44-117">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="59e44-118"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="59e44-118"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="59e44-119">Il testo viene disegnato con un bordo da visualizzare in basso rispetto al piano della finestra.</span><span class="sxs-lookup"><span data-stu-id="59e44-119">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>          |
| <dl> <span data-ttu-id="59e44-120"><dt>**\_NOborders SBT**</dt></span><span class="sxs-lookup"><span data-stu-id="59e44-120"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="59e44-121">Il testo viene disegnato senza bordi.</span><span class="sxs-lookup"><span data-stu-id="59e44-121">The text is drawn without borders.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="59e44-122"><dt>**\_OWNERDRAW SBT**</dt></span><span class="sxs-lookup"><span data-stu-id="59e44-122"><dt>**SBT\_OWNERDRAW**</dt></span></span> </dl>  | <span data-ttu-id="59e44-123">Il testo viene disegnato dalla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="59e44-123">The text is drawn by the parent window.</span></span><br/>                                                |
| <dl> <span data-ttu-id="59e44-124"><dt>**\_POPOUT SBT**</dt></span><span class="sxs-lookup"><span data-stu-id="59e44-124"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="59e44-125">Il testo viene disegnato con un bordo da visualizzare più in alto rispetto al piano della finestra.</span><span class="sxs-lookup"><span data-stu-id="59e44-125">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/>         |
| <dl> <span data-ttu-id="59e44-126"><dt>**\_RTLREADING SBT**</dt></span><span class="sxs-lookup"><span data-stu-id="59e44-126"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="59e44-127">Il testo verrà visualizzato nella direzione opposta al testo nella finestra padre.</span><span class="sxs-lookup"><span data-stu-id="59e44-127">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="59e44-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="59e44-128">Remarks</span></span>

<span data-ttu-id="59e44-129">Normale testo visualizzato da sinistra a destra (LTR).</span><span class="sxs-lookup"><span data-stu-id="59e44-129">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="59e44-130">È possibile eseguire il *mirroring* di Windows per visualizzare lingue quali l'ebraico o l'arabo con lettura da destra a sinistra (RTL).</span><span class="sxs-lookup"><span data-stu-id="59e44-130">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="59e44-131">Se \_ è impostato SBT RTLREADING, il testo della finestra di stato specificato verrà letto nella direzione opposta dal testo nella finestra padre.</span><span class="sxs-lookup"><span data-stu-id="59e44-131">If SBT\_RTLREADING is set, the specified status window text will read in the opposite direction from the text in the parent window.</span></span>

<span data-ttu-id="59e44-132">Questo messaggio restituisce una lunghezza massima della stringa di 65.535 caratteri.</span><span class="sxs-lookup"><span data-stu-id="59e44-132">This message returns a maximum string length of 65,535 characters.</span></span> <span data-ttu-id="59e44-133">Se la stringa di testo effettiva è più lunga, il messaggio [**SB \_ gettext**](sb-gettext.md) lo tronca.</span><span class="sxs-lookup"><span data-stu-id="59e44-133">If the actual text string is longer than that, the [**SB\_GETTEXT**](sb-gettext.md) message truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="59e44-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59e44-134">Requirements</span></span>



| <span data-ttu-id="59e44-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="59e44-135">Requirement</span></span> | <span data-ttu-id="59e44-136">Valore</span><span class="sxs-lookup"><span data-stu-id="59e44-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59e44-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59e44-137">Minimum supported client</span></span><br/> | <span data-ttu-id="59e44-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59e44-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59e44-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59e44-139">Minimum supported server</span></span><br/> | <span data-ttu-id="59e44-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59e44-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59e44-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59e44-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="59e44-142"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="59e44-142"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="59e44-143">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="59e44-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="59e44-144">**SB \_ GETTEXTLENGTHW** (Unicode) e **SB \_ GETTEXTLENGTHA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="59e44-144">**SB\_GETTEXTLENGTHW** (Unicode) and **SB\_GETTEXTLENGTHA** (ANSI)</span></span><br/>         |



 

 





