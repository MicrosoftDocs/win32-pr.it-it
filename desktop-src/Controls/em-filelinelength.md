---
title: Messaggio EM_FILELINELENGTH (CommCtrl. h)
description: Recupera la lunghezza, in caratteri, di una riga in un controllo di modifica, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- Controlli di Windows Message EM_FILELINELENGTH
topic_type:
- apiref
api_name:
- EM_FILELINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa50f4d9b49253a558095be78e0e781d7d4c7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517985"
---
# <a name="em_filelinelength-message"></a><span data-ttu-id="66b8d-104">\_Messaggio FILELINELENGTH em</span><span class="sxs-lookup"><span data-stu-id="66b8d-104">EM\_FILELINELENGTH message</span></span>

<span data-ttu-id="66b8d-105">Recupera la lunghezza, in caratteri, di una riga in un controllo di modifica, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="66b8d-105">Retrieves the length, in characters, of a line in an edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="66b8d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="66b8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66b8d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66b8d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66b8d-108">Indice dei caratteri di un carattere nella riga di cui è necessario recuperare la lunghezza.</span><span class="sxs-lookup"><span data-stu-id="66b8d-108">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="66b8d-109">Se questo parametro è maggiore del numero di caratteri nel controllo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="66b8d-109">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="66b8d-110">Questo parametro può essere-1.</span><span class="sxs-lookup"><span data-stu-id="66b8d-110">This parameter can be -1.</span></span> <span data-ttu-id="66b8d-111">In questo caso, il messaggio restituisce il numero di caratteri non selezionati nelle righe contenenti caratteri selezionati.</span><span class="sxs-lookup"><span data-stu-id="66b8d-111">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="66b8d-112">Se, ad esempio, la selezione è stata estesa dal quarto carattere di una riga attraverso l'ottavo carattere alla fine della riga successiva, il valore restituito sarà 10 (tre caratteri nella prima riga e sette nella successiva).</span><span class="sxs-lookup"><span data-stu-id="66b8d-112">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="66b8d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66b8d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66b8d-114">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="66b8d-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66b8d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66b8d-115">Return value</span></span>

<span data-ttu-id="66b8d-116">Per i controlli di modifica su più righe, il valore restituito è la lunghezza, in **TCHAR** s, della riga specificata dal parametro *wParam* , indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="66b8d-116">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="66b8d-117">Non include il carattere di ritorno a capo o di avanzamento riga alla fine della riga.</span><span class="sxs-lookup"><span data-stu-id="66b8d-117">It does not include the carriage-return or linefeed character at the end of the line.</span></span>

<span data-ttu-id="66b8d-118">Per i controlli di modifica a riga singola, il valore restituito è la lunghezza, in **TCHAR** s, del testo nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="66b8d-118">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="66b8d-119">Se *wParam* è maggiore del numero di caratteri nel controllo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="66b8d-119">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="66b8d-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="66b8d-120">Remarks</span></span>

<span data-ttu-id="66b8d-121">Usare il [**messaggio \_ FILELINEINDEX em**](em-lineindex.md) per recuperare un indice dei caratteri per un numero di riga specificato all'interno di un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="66b8d-121">Use the [**EM\_FILELINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="66b8d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66b8d-122">Requirements</span></span>



| <span data-ttu-id="66b8d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="66b8d-123">Requirement</span></span> | <span data-ttu-id="66b8d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="66b8d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66b8d-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66b8d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="66b8d-126">Solo app desktop Windows 10, 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="66b8d-126">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="66b8d-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66b8d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="66b8d-128">\[Solo app desktop Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="66b8d-128">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="66b8d-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66b8d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="66b8d-130"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66b8d-130"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66b8d-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66b8d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66b8d-132">**\_FILELINEINDEX em**</span><span class="sxs-lookup"><span data-stu-id="66b8d-132">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





