---
title: Messaggio SB_GETTEXT (COMmctrl. h)
description: Recupera il testo dalla parte specificata di una finestra di stato.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- Controlli di Windows Message SB_GETTEXT
topic_type:
- apiref
api_name:
- SB_GETTEXT
- SB_GETTEXTA
- SB_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e90b132c3f934188aea36afd86d53ab8f75bdadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048601"
---
# <a name="sb_gettext-message"></a><span data-ttu-id="321dd-104">\_Messaggio SB GETtext</span><span class="sxs-lookup"><span data-stu-id="321dd-104">SB\_GETTEXT message</span></span>

<span data-ttu-id="321dd-105">Recupera il testo dalla parte specificata di una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="321dd-105">Retrieves the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="321dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="321dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="321dd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="321dd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="321dd-108">Indice in base zero della parte da cui recuperare il testo.</span><span class="sxs-lookup"><span data-stu-id="321dd-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="321dd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="321dd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="321dd-110">Puntatore al buffer che riceve il testo come stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="321dd-110">Pointer to the buffer that receives the text as a null-terminated string.</span></span> <span data-ttu-id="321dd-111">Usare il messaggio [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) per determinare la dimensione richiesta del buffer.</span><span class="sxs-lookup"><span data-stu-id="321dd-111">Use the [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message to determine the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="321dd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="321dd-112">Return value</span></span>

<span data-ttu-id="321dd-113">Restituisce un valore a 32 bit costituito da valori a 2 16 bit.</span><span class="sxs-lookup"><span data-stu-id="321dd-113">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="321dd-114">La parola low specifica la lunghezza, in caratteri, del testo.</span><span class="sxs-lookup"><span data-stu-id="321dd-114">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="321dd-115">La parola alta specifica il tipo di operazione utilizzata per creare il testo.</span><span class="sxs-lookup"><span data-stu-id="321dd-115">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="321dd-116">Il tipo può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="321dd-116">The type can be one of the following values.</span></span>



| <span data-ttu-id="321dd-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="321dd-117">Return code</span></span>                                                                                    | <span data-ttu-id="321dd-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="321dd-118">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="321dd-119"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="321dd-119"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="321dd-120">Il testo viene disegnato con un bordo da visualizzare in basso rispetto al piano della finestra.</span><span class="sxs-lookup"><span data-stu-id="321dd-120">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>  |
| <dl> <span data-ttu-id="321dd-121"><dt>**\_NOborders SBT**</dt></span><span class="sxs-lookup"><span data-stu-id="321dd-121"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="321dd-122">Il testo viene disegnato senza bordi.</span><span class="sxs-lookup"><span data-stu-id="321dd-122">The text is drawn without borders.</span></span><br/>                                             |
| <dl> <span data-ttu-id="321dd-123"><dt>**\_POPOUT SBT**</dt></span><span class="sxs-lookup"><span data-stu-id="321dd-123"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="321dd-124">Il testo viene disegnato con un bordo da visualizzare più in alto rispetto al piano della finestra.</span><span class="sxs-lookup"><span data-stu-id="321dd-124">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/> |
| <dl> <span data-ttu-id="321dd-125"><dt>**\_RTLREADING SBT**</dt></span><span class="sxs-lookup"><span data-stu-id="321dd-125"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="321dd-126">Il testo viene visualizzato nella direzione opposta del testo nella finestra padre.</span><span class="sxs-lookup"><span data-stu-id="321dd-126">The text displays in the opposite direction of the text in the parent window.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="321dd-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="321dd-127">Remarks</span></span>

<span data-ttu-id="321dd-128">**Avviso di sicurezza:** L'uso errato di questo messaggio può compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="321dd-128">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="321dd-129">Questo messaggio non fornisce un modo per stabilire le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="321dd-129">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="321dd-130">Se si utilizza questo messaggio, chiamare prima [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) per ottenere il numero di caratteri necessari e quindi chiamare il messaggio per recuperare la stringa.</span><span class="sxs-lookup"><span data-stu-id="321dd-130">If you use this message, first call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="321dd-131">Se si attende prima di chiamare **SB \_ gettext** , il testo potrebbe cambiare, invalidando in tal modo il valore restituito di **SB \_ GETTEXTLENGTH**.</span><span class="sxs-lookup"><span data-stu-id="321dd-131">If you wait before calling **SB\_GETTEXT** the text could change, thereby invalidating the return value of **SB\_GETTEXTLENGTH**.</span></span> <span data-ttu-id="321dd-132">Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="321dd-132">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="321dd-133">Questo messaggio restituisce un massimo di 65.535 caratteri.</span><span class="sxs-lookup"><span data-stu-id="321dd-133">This message returns a maximum of 65,535 characters.</span></span> <span data-ttu-id="321dd-134">Se la stringa di testo è più lunga, viene troncata.</span><span class="sxs-lookup"><span data-stu-id="321dd-134">If the text string is longer than that, it is truncated.</span></span>

<span data-ttu-id="321dd-135">Se il testo presenta il \_ tipo di disegno SBT OWNERDRAW, questo messaggio restituisce il valore a 32 bit associato al testo anziché la lunghezza e il tipo di operazione.</span><span class="sxs-lookup"><span data-stu-id="321dd-135">If the text has the SBT\_OWNERDRAW drawing type, this message returns the 32-bit value associated with the text instead of the length and operation type.</span></span>

<span data-ttu-id="321dd-136">Normale testo visualizzato da sinistra a destra (LTR).</span><span class="sxs-lookup"><span data-stu-id="321dd-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="321dd-137">È possibile eseguire il *mirroring* di Windows per visualizzare lingue quali l'ebraico o l'arabo con lettura da destra a sinistra (RTL).</span><span class="sxs-lookup"><span data-stu-id="321dd-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="321dd-138">Se \_ è impostata la RTLREADING SBT, la stringa *lParam* viene letta nella direzione opposta dal testo nella finestra padre.</span><span class="sxs-lookup"><span data-stu-id="321dd-138">If SBT\_RTLREADING is set, the *lParam* string reads in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="321dd-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="321dd-139">Requirements</span></span>



| <span data-ttu-id="321dd-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="321dd-140">Requirement</span></span> | <span data-ttu-id="321dd-141">Valore</span><span class="sxs-lookup"><span data-stu-id="321dd-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="321dd-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="321dd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="321dd-143">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="321dd-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="321dd-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="321dd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="321dd-145">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="321dd-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="321dd-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="321dd-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="321dd-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="321dd-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="321dd-148">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="321dd-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="321dd-149">**SB \_ GETTEXTW** (Unicode) e **SB \_ gettexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="321dd-149">**SB\_GETTEXTW** (Unicode) and **SB\_GETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="321dd-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="321dd-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321dd-151">**\_testo SB**</span><span class="sxs-lookup"><span data-stu-id="321dd-151">**SB\_SETTEXT**</span></span>](sb-settext.md)
</dt> </dl>

 

 





