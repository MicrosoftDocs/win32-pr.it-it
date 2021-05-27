---
title: Messaggio SHAREVISTRING (Commdlg.h)
description: Una finestra di dialogo Apri o Salva con nome invia il messaggio registrato SHAREVISTRING alla procedura hook OFNHookProc, se si verifica una violazione di condivisione per il file selezionato quando l'utente fa clic sul pulsante OK.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- Finestre di dialogo del messaggio SHAREVISTRING
topic_type:
- apiref
api_name:
- SHAREVISTRING
- SHAREVISTRINGA
- SHAREVISTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043bed9edd08269e4e030482cbd44debea3a3695
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548766"
---
# <a name="sharevistring-message"></a><span data-ttu-id="94ee7-104">Messaggio SHAREVISTRING</span><span class="sxs-lookup"><span data-stu-id="94ee7-104">SHAREVISTRING message</span></span>

<span data-ttu-id="94ee7-105">\[A partire da Windows  Vista, le **finestre** di dialogo comuni Apri e Salva con nome sono state sostituite dalla [finestra di dialogo Elemento comune](../shell/common-file-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="94ee7-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="94ee7-106">È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo da Common Dialog Box Library.\]</span><span class="sxs-lookup"><span data-stu-id="94ee7-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="94ee7-107">Una **finestra** di dialogo Apri o Salva con nome invia il messaggio registrato **SHAREVISTRING** alla procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)se si verifica una violazione di condivisione per il file selezionato quando l'utente fa clic sul pulsante **OK.** </span><span class="sxs-lookup"><span data-stu-id="94ee7-107">An **Open** or **Save As** dialog box sends the **SHAREVISTRING** registered message to your hook procedure, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), if a sharing violation occurs for the selected file when the user clicks the **OK** button.</span></span>


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a><span data-ttu-id="94ee7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="94ee7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94ee7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94ee7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94ee7-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="94ee7-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="94ee7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94ee7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94ee7-112">Puntatore a una [**struttura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)</span><span class="sxs-lookup"><span data-stu-id="94ee7-112">A pointer to a [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="94ee7-113">Il **membro lpstrFile** di questa struttura contiene il nome file che ha causato la violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="94ee7-113">The **lpstrFile** member of this structure contains the file name that caused the sharing violation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94ee7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94ee7-114">Return value</span></span>

<span data-ttu-id="94ee7-115">La routine hook deve restituire uno dei valori seguenti per indicare in che modo la finestra di dialogo deve gestire la violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="94ee7-115">The hook procedure must return one of the following values to indicate how the dialog box should handle the sharing violation.</span></span>



| <span data-ttu-id="94ee7-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="94ee7-116">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="94ee7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94ee7-117">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="94ee7-118"><dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="94ee7-118"><dt>**OFN\_SHAREFALLTHROUGH**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="94ee7-119">Accettare il nome del file</span><span class="sxs-lookup"><span data-stu-id="94ee7-119">Accept the file name</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="94ee7-120"><dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="94ee7-120"><dt>**OFN\_SHARENOWARN**</dt> <dt>1</dt></span></span> </dl>      | <span data-ttu-id="94ee7-121">Rifiutare il nome del file ma non avvisare l'utente.</span><span class="sxs-lookup"><span data-stu-id="94ee7-121">Reject the file name but do not warn the user.</span></span> <span data-ttu-id="94ee7-122">L'applicazione è responsabile della visualizzazione di un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="94ee7-122">The application is responsible for displaying a warning message.</span></span><br/> |
| <dl> <span data-ttu-id="94ee7-123"><dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="94ee7-123"><dt>**OFN\_SHAREWARN**</dt> <dt>0</dt></span></span> </dl>        | <span data-ttu-id="94ee7-124">Rifiutare il nome del file e visualizzare un messaggio di avviso (lo stesso risultato di una procedura hook).</span><span class="sxs-lookup"><span data-stu-id="94ee7-124">Reject the file name and displays a warning message (the same result as if there were no hook procedure).</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="94ee7-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="94ee7-125">Remarks</span></span>

<span data-ttu-id="94ee7-126">La routine hook deve specificare la **costante SHAREVISTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore per il messaggio inviato dalla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="94ee7-126">The hook procedure must specify the **SHAREVISTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="94ee7-127">La finestra di dialogo invia il messaggio registrato **SHAREVISTRING** solo se non è stato specificato il flag **OFN \_ SHAREAWARE** nel membro **Flags** della struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) al momento della creazione della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="94ee7-127">The dialog box sends the **SHAREVISTRING** registered message only if you did not specify the **OFN\_SHAREAWARE** flag in the **Flags** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure when you created the dialog.</span></span>

<span data-ttu-id="94ee7-128">Se la routine hook restituisce un valore non definito, la finestra di dialogo risponde come se fosse stato restituito **OFN \_ SHAREWARN.**</span><span class="sxs-lookup"><span data-stu-id="94ee7-128">If the hook procedure returns an undefined value, the dialog box responds as if **OFN\_SHAREWARN** was returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="94ee7-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94ee7-129">Requirements</span></span>



| <span data-ttu-id="94ee7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="94ee7-130">Requirement</span></span> | <span data-ttu-id="94ee7-131">Valore</span><span class="sxs-lookup"><span data-stu-id="94ee7-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94ee7-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94ee7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="94ee7-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="94ee7-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="94ee7-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94ee7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="94ee7-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="94ee7-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="94ee7-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94ee7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="94ee7-137"><dt>Commdlg.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="94ee7-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="94ee7-138">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="94ee7-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="94ee7-139">**SHAREVISTRINGW** (Unicode) e **SHAREVISTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="94ee7-139">**SHAREVISTRINGW** (Unicode) and **SHAREVISTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="94ee7-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94ee7-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="94ee7-141">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="94ee7-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="94ee7-142">**CONDIVISIONE DELLA \_ RETE CDNVIOLATION**</span><span class="sxs-lookup"><span data-stu-id="94ee7-142">**CDN\_SHAREVIOLATION**</span></span>](cdn-shareviolation.md)
</dt> <dt>

[<span data-ttu-id="94ee7-143">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="94ee7-143">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="94ee7-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="94ee7-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="94ee7-145">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="94ee7-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="94ee7-146">Libreria di finestre di dialogo comune</span><span class="sxs-lookup"><span data-stu-id="94ee7-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

