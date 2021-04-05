---
title: Messaggio EM_LINELENGTH (winuser. h)
description: Recupera la lunghezza, in caratteri, di una riga in un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- Controlli di Windows Message EM_LINELENGTH
topic_type:
- apiref
api_name:
- EM_LINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cbf59cbe31886e55c34bce9f7c2421e431012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874273"
---
# <a name="em_linelength-message"></a><span data-ttu-id="a2df6-105">\_Messaggio LINELENGTH em</span><span class="sxs-lookup"><span data-stu-id="a2df6-105">EM\_LINELENGTH message</span></span>

<span data-ttu-id="a2df6-106">Recupera la lunghezza, in caratteri, di una riga in un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="a2df6-106">Retrieves the length, in characters, of a line in an edit control.</span></span> <span data-ttu-id="a2df6-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="a2df6-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a2df6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2df6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2df6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2df6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2df6-110">Indice dei caratteri di un carattere nella riga di cui è necessario recuperare la lunghezza.</span><span class="sxs-lookup"><span data-stu-id="a2df6-110">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="a2df6-111">Se questo parametro è maggiore del numero di caratteri nel controllo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="a2df6-111">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="a2df6-112">Questo parametro può essere-1.</span><span class="sxs-lookup"><span data-stu-id="a2df6-112">This parameter can be -1.</span></span> <span data-ttu-id="a2df6-113">In questo caso, il messaggio restituisce il numero di caratteri non selezionati nelle righe contenenti caratteri selezionati.</span><span class="sxs-lookup"><span data-stu-id="a2df6-113">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="a2df6-114">Se, ad esempio, la selezione è stata estesa dal quarto carattere di una riga attraverso l'ottavo carattere alla fine della riga successiva, il valore restituito sarà 10 (tre caratteri nella prima riga e sette nella successiva).</span><span class="sxs-lookup"><span data-stu-id="a2df6-114">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="a2df6-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2df6-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2df6-116">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="a2df6-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2df6-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2df6-117">Return value</span></span>

<span data-ttu-id="a2df6-118">Per i controlli di modifica su più righe, il valore restituito è la lunghezza, in **TCHAR** s, della riga specificata dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="a2df6-118">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter.</span></span> <span data-ttu-id="a2df6-119">Per testo ANSI, indica il numero di byte; per il testo Unicode, indica il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="a2df6-119">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="a2df6-120">Non include il carattere di ritorno a capo alla fine della riga.</span><span class="sxs-lookup"><span data-stu-id="a2df6-120">It does not include the carriage-return character at the end of the line.</span></span>

<span data-ttu-id="a2df6-121">Per i controlli di modifica a riga singola, il valore restituito è la lunghezza, in **TCHAR** s, del testo nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="a2df6-121">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="a2df6-122">Se *wParam* è maggiore del numero di caratteri nel controllo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="a2df6-122">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2df6-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2df6-123">Remarks</span></span>

<span data-ttu-id="a2df6-124">Usare il [**messaggio \_ LINEINDEX em**](em-lineindex.md) per recuperare un indice dei caratteri per un numero di riga specificato all'interno di un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="a2df6-124">Use the [**EM\_LINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control.</span></span>

<span data-ttu-id="a2df6-125">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a2df6-125">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="a2df6-126">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a2df6-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2df6-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2df6-127">Requirements</span></span>



| <span data-ttu-id="a2df6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2df6-128">Requirement</span></span> | <span data-ttu-id="a2df6-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a2df6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2df6-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2df6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a2df6-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2df6-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a2df6-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2df6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a2df6-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a2df6-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a2df6-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2df6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2df6-135"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2df6-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2df6-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2df6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2df6-137">**\_LINEINDEX em**</span><span class="sxs-lookup"><span data-stu-id="a2df6-137">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 





