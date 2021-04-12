---
title: Messaggio FINDMSGSTRING (COMMDLG. h)
description: Una finestra di dialogo Trova o Sostituisci invia il messaggio registrato FINDMSGSTRING alla procedura della finestra proprietaria quando l'utente fa clic sul pulsante Trova successivo, Sostituisci o Sostituisci tutto oppure chiude la finestra di dialogo.
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- Finestre di dialogo del messaggio FINDMSGSTRING
topic_type:
- apiref
api_name:
- FINDMSGSTRING
- FINDMSGSTRINGA
- FINDMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d3a73d8734d79d5ed0862f66bf9ba5c030e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518874"
---
# <a name="findmsgstring-message"></a><span data-ttu-id="2c824-104">Messaggio FINDMSGSTRING</span><span class="sxs-lookup"><span data-stu-id="2c824-104">FINDMSGSTRING message</span></span>

<span data-ttu-id="2c824-105">Una finestra di dialogo **trova** o **Sostituisci** invia il messaggio registrato **FINDMSGSTRING** alla procedura della finestra proprietaria quando l'utente fa clic sul pulsante **Trova successivo**, **Sostituisci** o **Sostituisci tutto** oppure chiude la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="2c824-105">A **Find** or **Replace** dialog box sends the **FINDMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Find Next**, **Replace**, or **Replace All** button, or closes the dialog box.</span></span>


```C++
#define FINDMSGSTRING TEXT("commdlg_FindReplace")
```



## <a name="parameters"></a><span data-ttu-id="2c824-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c824-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c824-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c824-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c824-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="2c824-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2c824-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c824-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c824-110">Puntatore a una struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) .</span><span class="sxs-lookup"><span data-stu-id="2c824-110">A pointer to a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure.</span></span> <span data-ttu-id="2c824-111">I membri di questa struttura contengono l'input dell'utente più recente, inclusa la stringa da cercare, la stringa di sostituzione (se presente) e le opzioni di ricerca e sostituzione.</span><span class="sxs-lookup"><span data-stu-id="2c824-111">The members of this structure contain the latest user input, including the string to search for, the replacement string (if any) and the search-and-replacement options.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c824-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c824-112">Return value</span></span>

<span data-ttu-id="2c824-113">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="2c824-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c824-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c824-114">Remarks</span></span>

<span data-ttu-id="2c824-115">È necessario specificare la costante **FINDMSGSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore del messaggio inviato dalla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="2c824-115">You must specify the **FINDMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="2c824-116">Quando si crea la finestra di dialogo, utilizzare il membro **hwndOwner** della struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) per identificare la finestra per la ricezione di messaggi **FINDMSGSTRING** .</span><span class="sxs-lookup"><span data-stu-id="2c824-116">When you create the dialog box, use the **hwndOwner** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure to identify the window to receive **FINDMSGSTRING** messages.</span></span>

<span data-ttu-id="2c824-117">Il membro **Flags** della struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) include uno dei flag seguenti per indicare l'evento che ha causato il messaggio.</span><span class="sxs-lookup"><span data-stu-id="2c824-117">The **Flags** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure includes one of the following flags to indicate the event that caused the message.</span></span>



| <span data-ttu-id="2c824-118">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="2c824-118">Flag</span></span>                            | <span data-ttu-id="2c824-119">Significato</span><span class="sxs-lookup"><span data-stu-id="2c824-119">Meaning</span></span>                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c824-120">**Fr \_ DIALOGTERM** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="2c824-120">**FR\_DIALOGTERM** (0x00000040)</span></span> | <span data-ttu-id="2c824-121">La finestra di dialogo sta per essere chiusa.</span><span class="sxs-lookup"><span data-stu-id="2c824-121">The dialog box is closing.</span></span> <span data-ttu-id="2c824-122">Quando la finestra proprietaria elabora questo messaggio, un handle per la finestra di dialogo non è più valido.</span><span class="sxs-lookup"><span data-stu-id="2c824-122">After the owner window processes this message, a handle to the dialog box is no longer valid.</span></span>                                                                                    |
| <span data-ttu-id="2c824-123">**Fr \_ TROVASUCCESSIVO** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="2c824-123">**FR\_FINDNEXT** (0x00000008)</span></span>   | <span data-ttu-id="2c824-124">L'utente ha fatto clic sul pulsante **Trova successivo** in una finestra di dialogo **trova** o **Sostituisci** .</span><span class="sxs-lookup"><span data-stu-id="2c824-124">The user clicked the **Find Next** button in a **Find** or **Replace** dialog box.</span></span> <span data-ttu-id="2c824-125">Il membro **lpstrFindWhat** specifica la stringa da cercare.</span><span class="sxs-lookup"><span data-stu-id="2c824-125">The **lpstrFindWhat** member specifies the string to search for.</span></span>                                                         |
| <span data-ttu-id="2c824-126">**Fr \_ SOSTITUISCi** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="2c824-126">**FR\_REPLACE** (0x00000010)</span></span>    | <span data-ttu-id="2c824-127">L'utente ha fatto clic sul pulsante **Sostituisci** in una finestra di dialogo **Sostituisci** .</span><span class="sxs-lookup"><span data-stu-id="2c824-127">The user clicked the **Replace** button in a **Replace** dialog box.</span></span> <span data-ttu-id="2c824-128">Il membro **lpstrFindWhat** specifica la stringa da sostituire e il membro **lpstrReplaceWith** specifica la stringa di sostituzione.</span><span class="sxs-lookup"><span data-stu-id="2c824-128">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span>     |
| <span data-ttu-id="2c824-129">**Fr \_ REPLACEALL** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="2c824-129">**FR\_REPLACEALL** (0x00000020)</span></span> | <span data-ttu-id="2c824-130">L'utente ha fatto clic sul pulsante **Sostituisci tutto** in una finestra di dialogo **Sostituisci** .</span><span class="sxs-lookup"><span data-stu-id="2c824-130">The user clicked the **Replace All** button in a **Replace** dialog box.</span></span> <span data-ttu-id="2c824-131">Il membro **lpstrFindWhat** specifica la stringa da sostituire e il membro **lpstrReplaceWith** specifica la stringa di sostituzione.</span><span class="sxs-lookup"><span data-stu-id="2c824-131">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span> |



 

<span data-ttu-id="2c824-132">Per un messaggio **Trova successivo** o **Sostituisci tutto** , il membro **Flags** può includere uno o più dei flag seguenti per indicare le opzioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2c824-132">For a **Find Next** or **Replace All** message, the **Flags** member can include one or more of the following flags to indicate the search options.</span></span>



| <span data-ttu-id="2c824-133">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="2c824-133">Flag</span></span>                           | <span data-ttu-id="2c824-134">Significato</span><span class="sxs-lookup"><span data-stu-id="2c824-134">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c824-135">**Fr \_ GIÙ** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="2c824-135">**FR\_DOWN** (0x00000001)</span></span>      | <span data-ttu-id="2c824-136">Se impostato, viene selezionato il pulsante **giù** dei pulsanti di opzione direzione che indica che l'utente desidera eseguire la ricerca dalla posizione corrente fino alla fine del documento.</span><span class="sxs-lookup"><span data-stu-id="2c824-136">If set, the **Down** button of the direction radio buttons is selected indicating that user wants to search from the current location to the end of the document.</span></span> <span data-ttu-id="2c824-137">Se **fr \_ Down** non è impostato, viene selezionato il pulsante **su** in modo che l'utente desideri eseguire la ricerca all'inizio del documento.</span><span class="sxs-lookup"><span data-stu-id="2c824-137">If **FR\_DOWN** is not set, the **Up** button is selected so the user wants to search to the beginning of the document.</span></span>       |
| <span data-ttu-id="2c824-138">**Fr \_ MATCHCASE** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="2c824-138">**FR\_MATCHCASE** (0x00000004)</span></span> | <span data-ttu-id="2c824-139">Se impostato, viene selezionata la casella di controllo **maiuscole/minuscole** che indica che l'utente desidera che la ricerca venga fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2c824-139">If set, the **Match Case** check box is selected indicating that the user wants the search to be case-sensitive.</span></span> <span data-ttu-id="2c824-140">Se **fr \_ MATCHCASE** non è impostato, la casella di controllo è deselezionata, quindi la ricerca deve essere senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2c824-140">If **FR\_MATCHCASE** is not set, the check box is unselected so the search should be case-insensitive.</span></span>                                                                         |
| <span data-ttu-id="2c824-141">**Fr \_ WHOLEWORD** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="2c824-141">**FR\_WHOLEWORD** (0x00000002)</span></span> | <span data-ttu-id="2c824-142">Se impostata, la casella di controllo trova **solo parola intera** è selezionata indicando che l'utente desidera eseguire la ricerca solo di parole intere che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2c824-142">If set, the **Match Whole Word Only** check box is selected indicating that the user wants to search only for whole words that match the search string.</span></span> <span data-ttu-id="2c824-143">Se **fr \_ WHOLEWORD** non è impostato, la casella di controllo è deselezionata, quindi è necessario cercare anche frammenti di parola che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2c824-143">If **FR\_WHOLEWORD** is not set, the check box is unselected so you should also search for word fragments that match the search string.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="2c824-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c824-144">Requirements</span></span>



| <span data-ttu-id="2c824-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c824-145">Requirement</span></span> | <span data-ttu-id="2c824-146">Valore</span><span class="sxs-lookup"><span data-stu-id="2c824-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c824-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c824-147">Minimum supported client</span></span><br/> | <span data-ttu-id="2c824-148">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2c824-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2c824-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c824-149">Minimum supported server</span></span><br/> | <span data-ttu-id="2c824-150">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2c824-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c824-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c824-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c824-152"><dt>COMMDLG. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c824-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2c824-153">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2c824-153">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2c824-154">**FINDMSGSTRINGW** (Unicode) e **FINDMSGSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2c824-154">**FINDMSGSTRINGW** (Unicode) and **FINDMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="2c824-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c824-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c824-156">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2c824-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2c824-157">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="2c824-157">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="2c824-158">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="2c824-158">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="2c824-159">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="2c824-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2c824-160">Libreria finestra di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="2c824-160">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

